# Treminutersdemo v3 — implementerad baseline, separat draft v2

Manusdatum: 14 oktober 2026. Taltexten nedan gäller **baseline-appen**, inte en genomförd v3-import. Taltexten är **302 ord**. Detta är ett tidsatt manus; en live repetition har inte genomförts i detta pass.

## Version och förberedelse

- Preview: https://id-preview--2ebd52fa-131b-4aba-9934-92d1e2646935.lovable.app/
- Apprepo: https://github.com/MysteriousGuardian/hackathon-mdd; senaste kod inspekterad read-only vid `8158fec0dcfe5674689dba88a92c7d4e8afab7ed` på main. Data/draft är oförändrade från planens d97f7c1-snapshot. Manusreferensen justerades före första publicering.
- Baseline data-blob: `3212a9159e69725d56aa74770dbec80ee5fd0082`; appens draft v2-blob: `dd023d56c004674cf9640db715b2cb0c5afa2cb1`.
- Runtime-underlag: [QA:s rapport](../qa/qa-report.md) vid researchbas `6b3813b3ec9fe513e6f7f5092b3b4adf7f75cf65`, Strawberry-pass ungefär 11:55–11:59 Stockholm. Observerad bundle: `/assets/index-DO3HIn-1.js`. Sambandet mellan bundle och kodcommit är **inte verifierat**. Senare QA körde lokala kopior på d97f7c1/8008474, verifierade linked-support-modulen på 8158 och trace-/fokusvägar på 1b11f9c0ee03d6834a53344af384272944261f67. Det är ingen ny deployed-preview-kontroll av 8158. Rena modulchecks i detta researchpass ersätter inte en egen browserretest eller repetition.
- Baseline-rankning: O01/O02/O03/O05/O04, summor **11/10/10/8/8**. O06 finns bara i draft v2, utan granskad poäng eller aktiv rang. V3 föreslår **O01/O02/O03/O06/O05, 9/9/9/9/8**, men detta visas ännu inte i appens granskade jämförelse.

Person 2 låser en tillgänglig demoversion och fastställer gärna preview/commit-kopplingen. Kandidatfiltret och linked-support-grinden finns i 8158-koden; verifiera vald importversion och exakt O06→P06 innan någon godkänd import. Kontrollera före visning att ovanstående baseline och draft fortfarande stämmer. Om app/data eller bundle har ändrats: skapa ett nytt versionsmärkt manus efter kontroll, utan att skriva om detta överlämnade manus. Använd en redan öppen appflik och återställ till PLAN. Förbered källfliken [NRMCA CIP 6, PDF s.2](https://urmca.org/wp-content/uploads/2018/09/06pr.pdf#page=2); snabbvisningen av källan ska inte kräva sökning på scen.

## 0:00–0:25 — Kundjobbet och fem steg

**Klick:** Visa startsidan. Peka på PLAN, PREPARE, MOVE, OPERATE och FINISH; klicka till sist PLAN. Stegordningen är navigering, inte bevis för en bevittnad hel arbetsdag.

**Taltext:**

> Kunden är en professionell operatör som sågar de första kontraktionsfogarna i en nygjuten utomhusplatta. Målet är rätt foglayout och godtagbara kanter vid lämpliga förutsättningar. Här modellerar vi hela jobbet: planera, förbereda, flytta, såga och avsluta. Vi visar både dokumenterade uppgifter och det vi ännu inte vet om arbetet.

## 0:25–1:10 — En spårbar evidenskedja

**Klick:** PLAN → P01 → E03a. Visa A, B och C, samt källpanelens datum **2014**, locator och begränsningar. Klicka källtiteln med ↗; visa PDF s.2 kort och återgå till appfliken. Klicka O01-länken under C eller visa den i tabellen.

**Taltext:**

> Följ kedjan från PLAN till P01 och observation E03a. A är vad den öppnade branschvägledningen säger: fogar och timing behöver planeras. B är vår tolkning att readiness kräver flera uppgifter och överlämning. C är O01, ett oprövat förslag om stöd. Källans plats och begränsningar går att kontrollera. Vägledningen bevisar inte att en verklig besättning har haft ett överlämningsproblem, och appen ger ingen universell starttid.

## 1:10–1:45 — Verktyg, transport och avslut

**Klick:** PREPARE och P02; visa därefter MOVE/P04 och FINISH/P05. Peka på Evidence gaps. Visa inte en påhittad familjeräknare: den saknades i den observerade versionen.

**Taltext:**

> Förberedelsen omfattar verktygssystem och skick. MOVE och FINISH visar att jobbet också kräver transport och skötsel. Instruktionerna belägger uppgifterna, men vi har inte mätt antal transporter, fysisk belastning eller rengöringsbörda. P04 och P05 har två observationer vardera från samma källfamilj. Det betyder inte två oberoende behovsfynd. O02:s inspektionsstöd och O06:s åtkomst till felsökning är separata hypoteser.

## 1:45–2:15 — Prioriterad möjlighet och osäkerhet

**Klick:** Scrolla till Opportunities och O01. Peka på de fyra komponenterna, **11/12**, märkningen om provisorisk bedömning och validation-texten.

**Taltext:**

> Vi prioriterar O01, readiness och överlämning. Den implementerade baselinen visar elva av tolv, baserat på den äldre evidensrubriken. V3 föreslår nio av tolv med en striktare definition: belagda tekniska villkor räcker inte för att bevisa ett kundbehov. Det är ett separat, ännu inte importgodkänt förslag. Poäng, rubricering och rang måste ändras tillsammans.

## 2:15–2:40 — Motbevis och draft

**Klick:** Öppna "Draft import proposal v2 — not reviewed, excluded from ranking". Peka på E01e och O06 med P06, rank none och no reviewed score. Stanna i denna befintliga draftvy; E01g och v3-rankningen är inte appfunktioner ännu.

**Taltext:**

> Här ligger v2 separat som draft. Manualen har redan felsökning för dåliga fogkanter, och Husqvarna har även en befintlig navigator. O06 kan därför bara pröva ett möjligt mervärde i åtkomst och tillämpning. Det är ingen unik eller korrekthetsvaliderad diagnosmotor. Draften höjer inte den granskade rankningen.

## 2:40–3:00 — Fungerande automation och nästa test

**Klick:** Sök `handoff` i Search evidence och peka på P01/O01. Läs automationsbegränsningen högt; den observerade appens disclosure anger inte alla automatiska/kuraterade moment.

**Taltext:**

> Laddning, sökning, spårning och poängräkning är automatiska. Urval, extraktion, kopplingar, tolkningar och poängunderlag är kuraterade; ny research upptäcks inte automatiskt. Nästa steg är att testa readiness-kortet med operatör och arbetsledare och registrera saknade uppgifter, ansvar och användbarhet.

## Reservvägar och repetitionskontroll

- Om källsidan inte öppnas: visa E03a:s exakta locator och paraphrase i appen. Säg att länken inte gick att öppna i denna visning; hävda ingen ny källinspektion. Använd ingen blockeringsbypass.
- Om källfliken saknar rätt sida: gå direkt till förberedd PDF-flik eller återgå till appens locator. Lägg inte demotid på att leta.
- Om panelen inte stängs: välj nästa steg eller Reset. Den observerade versionen saknade Esc/stängkontroll; detta är inget påstående om att felet är åtgärdat.
- Om preview kräver login eller saknar åtkomst: framför manus som researchgenomgång med tydlig uppgift att liveappen inte kunde visas. Kalla inte dokumentet en fungerande live demonstration.
- Om v2-panelen har ersatts eller en import är genomförd: avbryt versionsmatchningen och skapa ett nytt manus. Visa inte v3-data som om den redan fanns i denna baseline.
- Person 3 verifierar versionen och demovägen; Person 1 gör två tidsatta repetitioner före 15:50. Detta är kvarstående teamarbete, inte utförd QA. Mät faktisk tal-/klicktid; korta klickpauser om det behövs, utan att ta bort draft-, behovs- eller automationsbegränsningarna.

Påstå inte att källfamiljer visar prevalens, att fotobaserad expertöverensstämmelse bevisar korrekt diagnos, eller att researchen är human reviewed/teamgodkänd. Frivilliga intervjuer och framtida valideringsexperiment är planerade aktiviteter, inte genomförda resultat.
