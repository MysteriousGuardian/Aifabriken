# Husqvarna hackathon — börja här

Detta paket innehåller allt granskat forsknings- och planeringsunderlag för teamet. Deadline är **16:00, 14 oktober 2026, Stockholmstid**. Vi är **tre personer**.

## Senaste komplettering — läs först

[Granskning av ny research och rättad verktygsplan](research/research-review-and-tooling.md). Teamet har Claude Code, Codex, Lovable via MCP och Strawberry Browser med extra credits. Lovable i Vibeathon är huvudspåret för appbygget. Kompletteringen rättar flera för starka researchslutsatser och delar av den bifogade Claude-prompten; kopiera inte dess utökade dataset som verifierat utan granskning.

## Rekommenderat scope

En professionell operatör sågar initiala kontraktionsfogar i en nygjuten utomhusplatta med en early-entry-såg. Utforska hela jobbet: PLAN → PREPARE → MOVE → OPERATE → FINISH. Stöd för startförutsättningar och överlämning är första prioritet; verktygsskick och utsugssystem är ytterligare R&D-hypoteser.

## Läs och använd

- [Fullständig plan](research/research-plan.md): briefens krav, kandidatjämförelse, rekommendation, källregister, arbetsflöde, prioriteringar, tidsplan och treminutersdemo.
- [Separat källregister](research/evidence-register.md): granskade källor med observationer, lokalisering och begränsningar.
- [Data för prototypen](research/research.json): tio källor, tretton observationer, fem steg, fem smärtpunkter och fem möjligheter. Två observationer avser alternativa jobb och ska inte blandas in i valt workflow.
- [Första Lovable-prompten](research/first-lovable-prompt.md): färdig att skicka med JSON-filen när teamet beslutat scope.

## Arbetsfördelning

1. **Person 1 — forskning/produkt:** äger data, källor, tolkningar och demo-story. Codex hjälper med struktur och kontroll.
2. **Person 2 — Lovable/UI:** enda personen som skickar byggprompter; granskar preview efter varje avgränsat steg.
3. **Person 3 — teknik/QA:** äger relationsvalidering, eventuell avgränsad import, kodgranskning och funktionskontroll med Codex.

Ingen skriver samtidigt i samma filer. Vänta tills Lovable är klar innan ändringar i dess filer mergas. Bygg fungerande stegvis; reparera specifika fel och behåll fungerande funktioner.

## Credits och byggstatus

Användaren uppger cirka **15 000 Lovable-credits** och nämner även **2 100 credits per person**. Verktygstillhörighet/fördelning är inte entydigt klargjord; siffrorna är rapporterade och inte verifierat saldo eller en summerad budget. Låt en person äga byggandet och följ upp faktisk förbrukning efter varje request. Tillgängliga credits är inte ett skäl att bredda scope före deadline.

**Ingen Lovable-app har skapats och inga byggrequests har skickats i denna research.** Vibeathon är verifierat tillgängligt. Paketet är förberett för nästa byggsteg.

## GitHub och Lovable

Aifabriken är teamets underlagsrepo. Enligt [Lovables dokumenterade workflow](https://docs.lovable.dev/integrations/github#limitations) kan befintliga GitHub-repon inte importeras som Lovable-projekt: anslutningen skapar ett nytt apprepo. När bygget startar i Vibeathon används en godkänd GitHub-anslutning och det nya apprepot länkas här. Member-access till workspace bevisar inte rätt att skapa en ny anslutning; stäm av tillgänglig anslutning med arrangören.

## Vad kollegorna måste behålla

- A: observation, B: tolkning och C: förslag visas separat.
- Varje möjlighet ska gå att spåra tillbaka till en observation, källa och arbetssteg.
- Okända datum och evidensluckor visas tydligt. Inga påhittade citat, besparingar eller prevalens.
- Förslagen är oprövade hypoteser; poängen är provisoriska bedömningar.
- Första prototypen använder kuraterad forskning. Automatisk sökning/filter/rankning är inte automatisk upptäckt av nya kundinsikter.
- Reddit-källan blockerades och används inte; inga videor påstås vara granskade.

Alla registrerade källor är offentliga. Inga proprietära underlag eller kopior av hela källdokument ingår.
