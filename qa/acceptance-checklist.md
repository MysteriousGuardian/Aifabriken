# QA: acceptanschecklista för Lovable-preview

Körs i Strawberry Browser mot Lovable-preview-URL:en efter varje byggsteg. Utgå från ett nytt fönster och viewport 1366×768 om inget annat anges. Kriterierna 1–9 kommer från `research/first-lovable-prompt.md`. Bocka av, och skriv ett fel enligt mallen längst ner för varje underkänd punkt.

**Preview-URL:** _____ **Commit/version:** _____ **Testare:** _____ **Tid:** _____

## Inkrement 1: utforskaren

| # | Steg | Förväntat resultat | OK |
|---|---|---|---|
| 1 | Ladda sidan. | PLAN är förvald. Titeln är ”Customer Job Twin: Early-entry Concrete Joint Cutting”. ”Curated public research · reviewed 14 October 2026” syns. | ☐ |
| 2 | Klicka i tur och ordning på PLAN, PREPARE, MOVE, OPERATE och FINISH. | Ordningen är exakt den. Varje steg visar aktörer, uppgifter, utrustning, beroenden, smärtpunkter och **evidensluckor**. MOVE visar P04 och luckan om transporter/hållning. FINISH visar P05 och luckan om bortskaffning och kvittering. | ☐ |
| 3 | PLAN → klicka P01. | Panelen har tre separata sektioner: ”Observed evidence” (A), ”Interpretation” (B) och ”Response hypotheses” (C). De går att skilja åt visuellt utan att läsa rubrikerna noga. | ☐ |
| 4 | I P01: hitta kortet **E03a**. | Kortet visar ID, parafras, källtitel och typ (”NRMCA CIP 6 …”, industry association guidance), datum ”2014”, locator ”PDF p.2: item c and rules 1–3”, aktör, uppgift, villkor och begränsningar. | ☐ |
| 5 | Klicka ”Open source” på E03a. | En ny flik öppnas till exakt `https://urmca.org/wp-content/uploads/2018/09/06pr.pdf`. Appen ligger kvar i originalfliken. | ☐ |
| 6 | Gå från P01 till dess möjlighet. | **O01 Readiness and handoff support** visas med märkningen ”Untested hypothesis” och valideringsexperimentet. | ☐ |
| 7 | Öppna möjlighetsjämförelsen. | Varje möjlighet visar de fyra komponenterna och en summa som är **deras summa**. Utan import gäller O01 11, O02 10, O03 10, O05 8, O04 8. Ordningen är O01, O02, O03, O05, O04. Etiketten ”Provisional judgment” och rubriken syns. | ☐ |
| 8 | Öppna källan E04, E05, E06 och E07, som alla saknar datum. | Datum visas som ”Unknown”, inte som tomt fält, dagens datum eller ”1970”. | ☐ |
| 9 | Öppna E02 (`2007`), E08 (`2017-12`) och E10 (`2010-04`). | Datum visas som år eller år-månad, inte som ett påhittat fullständigt datum (till exempel ”1 Dec 2017”) och inte förskjutet till föregående år eller månad. | ☐ |
| 10 | Öppna E08 (OSHA). | Begränsningen syns: wet-saw-fact-sheet, etablerar inte lämplighet eller efterlevnad för dry Soff-Cut-setup, inte svensk rättslig rådgivning. | ☐ |
| 11 | Titta på räknare för källor och observationer, till exempel vid P04 och P05. | Källfamiljer och observationer räknas separat. P04 och P05 har **1 källfamilj** (E01 och E04 är samma familj). Ordet ”prevalence” eller ”vanlighet” används aldrig om antal. | ☐ |
| 12 | Sök `skid`. | Träffar finns i observationer och möjligheter: E01b, E02a, E04a, O02 och O04. Ingen smärtpunkt innehåller ordet. Kandidaterna E09a och E10a visas inte i det valda jobbets resultat. Sök också `handoff` och kontrollera att träffar även i smärtpunkter visas (P01). | ☐ |
| 13 | Sök `xyzzy`. | Ett tomt läge med hjälptext och ett sätt att rensa visas. Ingen tom vit yta och inget fel. | ☐ |
| 14 | Sätt ett stegfilter plus en sökning och klicka sedan återställ/rensa. | Allt innehåll kommer tillbaka och fältet är tomt. Inga kvarhängande filter syns. | ☐ |
| 15 | Leta efter automationsdisclosure. | Det står att laddning, sökning, spårning och poäng är automatiska, medan urval, extraktion och tolkning är kuraterade. Automatisk upptäckt av nya källor är **inte** implementerad. | ☐ |
| 16 | Sök efter belopp, procent, ROI eller ”saves”. | Inga besparingar, kostnader, skadetal, ROI eller prevalens finns någonstans. | ☐ |
| 17 | Bara tangentbord: ladda om och tabba igenom hela sidan. | Fokus syns hela tiden, och ordningen är logisk: steg, smärtpunkter, panel, möjligheter. Enter eller Space väljer steg och öppnar smärtpunkt. Esc, eller en fokuserbar stängknapp, stänger panelen och fokus återgår. ”Open source” går att nå och aktivera. | ☐ |
| 18 | Viewport 1366×768 och 1280×800, zoom 100 % och 125 %. | Ingen horisontell scroll. Text och kontrast är läsbara, även på grått och färgat. Panelen täcker inte navigeringen så att den blir oåtkomlig. | ☐ |
| 19 | Klicka ”Open source” för E01–E10. | Rätt URL öppnas. E07 och E08 kan blockeras av webbplatsen (403 mot skript). Om sidan blockeras: kategori **extern**, inte appfel, så länge URL:en är exakt den i datan. | ☐ |

## Endast om importförslaget har integrerats

| # | Steg | Förväntat resultat | OK |
|---|---|---|---|
| 20 | Öppna möjlighetsjämförelsen. | Fyra aktiva: O01, O03, O06 och O05 (summorna 9, 9, 9, 8). O02 är märkt ”superseded by O06” och O04 ”backlog”. Inga av dem ligger i den aktiva rangordningen. | ☐ |
| 21 | Titta på hur rang 1–3 förklaras. | Det framgår att lika summa bryts redaktionellt (O01, O03, O06). | ☐ |
| 22 | Öppna O06 → P06. | E01e, E01f, E18a och E19a är märkta draft eller ej granskade. De räknas inte som granskad evidens och höjer inga räknare för granskat stöd. | ☐ |
| 23 | OPERATE och PREPARE. | De nya observationerna syns under rätt steg, eller är tydligt draft-märkta. Stegen och observationerna pekar på varandra. | ☐ |

## Felrapportmall

```
QA-NN · Prioritet: P0 | P1 | P2 | P3 · Kategori: appfel | extern källa
Preview/version:
Steg för att reproducera:
  1.
  2.
Förväntat:
Faktiskt:
Skärmdump:
Kriterium (#):
```

- **P0:** blockerar demon (vit sida, krasch, steg går inte att nå, PLAN → P01 → E03a → O01 bruten).
- **P1:** felaktigt påstående eller bruten spårbarhet (fel summa, draft eller kandidat som granskad, påhittat datum, länk till fel URL, saknad A/B/C-separation).
- **P2:** användbarhet och tillgänglighet (fokus, tangentbord, tomt läge, overflow).
- **P3:** kosmetiskt.
- **Extern källa:** URL:en i appen är korrekt men webbplatsen blockerar eller är nere. Det är inget appfel, men det noteras för demon (öppna en annan källa eller visa locatorn).
