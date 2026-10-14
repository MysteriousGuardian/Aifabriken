# QA: datagranskning av research.json och importförslag

Granskat 14 oktober 2026 av Person 3 (teknik/QA). Underlaget är Aifabriken `c377396`. Granskningen var skrivskyddad, och inga filer i `research/` har ändrats. Fynden riktar sig till ägaren av respektive fil.

## Sammanfattning

- **`research/research.json` (baseline, blob `3212a91…`):** inga blockerande datafel. Den kan användas som den är för första Lovable-inkrementet.
- **`research/research-import-proposal.json`:** strukturellt rent (inga ID-kollisioner, baseline-SHA stämmer). Tre punkter måste lösas **innan** det integreras, nämligen I3, I4 och I5.
- **Käll-URL:er:** 8 av 10 svarar. E07 och E08 returnerar 403 till skript, troligen botskydd. Det är externa källor och inga appfel, och de verifieras i browser.

## Kontrollerat i baseline

| Kontroll | Resultat |
|---|---|
| Unika IDs över källor, observationer, steg, smärtpunkter och möjligheter | OK, 0 dubbletter |
| `observation.sourceId`, `stageIds`, `stage.observationIds`, `painPoint.observationIds`, `opportunity.painPointIds` | OK, 0 brutna referenser |
| Speglade länkar stage ↔ observation | OK åt båda hållen |
| `accessStatus` och `reviewStatus` | Alla källor `inspected`, alla observationer `reviewed` |
| Kandidatobservationer (E09a, E10a) | `candidateOnly: true`. De finns varken i steg eller smärtpunkter, så OK |
| Poäng | Alla heltal 1–3. Summorna är O01 11, O02 10, O03 10, O05 8, O04 8. `scores.total` saknas, vilket är avsett |
| Rang mot summa | Konsekvent. Lika summor (O02/O03, O05/O04) bryts med `rank` |
| Varje möjlighet når en granskad observation och källa | OK för O01–O05 |

## Fynd

Prioritet: **Hög** = måste åtgärdas före integration eller demo. **Medel** = UI-krav som lätt blir fel. **Info** = avsiktligt, ska bara inte misstolkas.

| ID | Prio | Fil | Fynd | Ägare | Minsta åtgärd |
|---|---|---|---|---|---|
| D1 | Medel | research.json | E04 har samma `familyId` som E01. P04 och P05 har därför två observationer men **en** källfamilj. | Person 2 (UI) | Räkna och visa unika `familyId`, inte observationer, som ”källfamiljer”. Kalla det aldrig prevalens. |
| D2 | Medel | research.json | Datumen `"2007"`, `"2014"`, `"2017-12"` och `"2010-04"` är delvisa. `new Date("2017-12")` blir 1 december, och i vissa tidszoner föregående dag. | Person 2 (UI) | Visa strängen som den är, eller formatera bara de delar som finns. `null` visas som ”Unknown”. |
| D3 | Info | research.json | E08a (OSHA) ligger i PREPARE och OPERATE men i ingen smärtpunkt. | — | Avsiktligt, eftersom den är en scope-gräns. Ingen åtgärd. |
| D4 | Info | research.json | Blockerade källor (Reddit) finns bara som text i `meta.excludedAccess`. Det finns ingen access-logg i datan. | Person 1 | Ingen åtgärd krävs för inkrement 1. Om appen ska visa en access-logg behövs en egen lista, inte nya källposter med `inspected`. |
| I1 | Info | import-proposal | Inga ID-kollisioner. E11–E17 är reserverade och oanvända. Baseline-SHA stämmer. | — | — |
| I2 | Medel | import-proposal | `stages[].observationIds` uppdateras inte för E01e, E01f, E18a, E18b och E19a. Efter import pekar de nya observationerna på steg som inte pekar tillbaka. | Person 1 | Lägg till de fem ID:na i respektive stegs `observationIds` vid integration (förslagets steg 6). Validatorn varnar om det glöms. |
| I3 | **Hög** | import-proposal | Rang 2 blir dubblett. Inaktiva O02 behåller `rank: 2` och O03 får `rank: 2`. | Person 1 | Sätt `rank: null` på inaktiva O02 och O04, eller kräv unik rang bara bland aktiva och skriv det i datan. |
| I4 | **Hög** | import-proposal + UI | Inaktiva O02 har summan 10. Om UI:t sorterar på summa utan att filtrera på `active` hamnar O02 överst bland de aktiva 9:orna. | Person 2 (UI) | Visa bara `active !== false` i rangordningen. Visa O02 och O04 separat som ”superseded” respektive ”backlog”. |
| I5 | **Hög** | import-proposal | O06 länkar till P06 och P02. Allt stöd i P06 är `draft`, men O06 får tre granskade evidensvägar via P02 (E01b, E02a, E04a). Appen kan därmed visa O06 som granskat underbyggd. | Person 1 + Person 2 | Visa evidensstatus per smärtpunkt. Markera P06 som ”draft, ej granskad” tills Person 1 godkänt. Överväg att ta bort P02 från O06, eftersom O02 redan är superseded. |
| I6 | Medel | import-proposal | Det finns ett nytt värde, `accessStatus: "inspected-page-text"`, och ett nytt fält, `integrationReviewStatus: "draft"`, på E18 och E19. | Person 3 (validator) | Validatorn räknar en källa med `integrationReviewStatus: "draft"` som ej granskad evidens oavsett `accessStatus`. |
| I7 | Medel | import-proposal | O01:s evidenspoäng ändras från 3 till 1, och summan från 11 till 9. Det gäller bara med den skärpta E-rubriken i `rubricUpdate`. | Person 1 + Person 2 | Inför poäng och rubriktext i samma ändring. UI:t ska förklara att rang 1–3 är redaktionell prioritet vid lika summa, som `rankPolicy` anger. |

## Käll-URL:er (kontrollerat med curl, 14 okt)

| Källa | HTTP | Kommentar |
|---|---|---|
| E01, E02, E03, E04, E09, E10 | 200 (PDF) | OK |
| E05, E06 | 200 (HTML) | OK |
| E07 Ruwac | **403** | Externt, troligen botskydd mot skript. Verifiera i Strawberry. Om browsern också blockeras: rapportera som extern källa, inte appfel. |
| E08 OSHA | **403** | Som E07. |

Nya URL:er i importförslaget (E18 och E19) har inte kontrollerats här. Det görs vid integration.

## Vad som inte är granskat

Att en referens resolverar visar inte att observationen faktiskt stöder smärtpunkten. Innehållsgranskningen av parafraser och begränsningar ägs av Person 1. Inga källdokument har lästs om i denna QA-runda.
