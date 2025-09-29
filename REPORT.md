# 📌 Rättningsrapport – fed24d-case-af-jobtech-team-14

## 🎯 Uppgiftens Krav:
[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/6VsM7MHT)
# Skapa en egen Platsbanken för ert drömscenario 

Dokumentation om Arbetsförmedlingens öppna data finns på https://jobtechdev.se. All öppna data från arbetsförmedlingen och andra offentliga organisationen går även att hitta direkt på dataportal.se. 
I detta dokument ges två förslag på användningsfall som vi tror är lämpliga för studenter som vill utveckla en applikation på riktig data. All data som är öppna data får vem som helst använda utan att fråga myndigheten om lov, så ingen är begränsad till de exempel vi ger.

Läs först igenom kom-igång hjälpen 

-  [Övergripande dokumentation API:etJobSearch](https://jobtechdev.se/sv/components/jobsearch)
-  [Kom-igång guide](https://gitlab.com/arbetsformedlingen/education/education-api/-/blob/main/GETTING_STARTED.md)

## Prova att utforska datan med vår interaktiva tjänst 

Görs genom att öppna Swagger-sidan för API:et (för att enkelt testa olika endpoints i API:et och läsa dokumentation för respektive endpoint): Search job ads (jobtechdev.se) 

## Uppgift 

Använd endpoint https://jobsearch.api.jobtechdev.se/ för att använda/söka bland befintliga annonser. 
Det går även bra att använda historiska annonser om ni vill jämföra aktuella annonser med hur det har sett ut tidigare. Detta api finns här: Historical job ads (jobtechdev.se)

Om möjligt, använd en grafisk presentation av era resultat genom t.ex. stapeldiagram eller linjegrafer.

**Observera**
Er slutprodukt ska ej innehålla Arbetsförmedlingens logga eller färger. Anpassa gärna efter eget tycke och smak så att ni har en färgpalett och en god tanke bakom. 

## Betygskriterier 

### Need-to-have (G) 
- Ni har hämtat data på ett strukturerat sätt med hjälp av antingen fetch eller axios. 
- Ni har skapat en tjänst som ni använder för att hämta data. 
- Ni använder react-koncept vi har pratat om för att göra datan tillgänglig (context, state, routing et.c.). 
- Ni använder den syntax, namngivningsstandard samt skrivsätt som vi har lärt er.  
- Ni använder designsystemet för presentation. 

### Nice-to-have (Extra bonus) 
- Styled components (som drar nytta av designsystemet) 
- Grafisk presentation av datat 
- Användning av custom hook där det finns möjlighet

## 🔍 ESLint-varningar:
- C:\Work\AssignmentCorrector\backend\repos\fed24d-case-af-jobtech-team-14\src\contexts\SavedJobsContext.ts - no-unused-vars - 'job' is defined but never used.,no-unused-vars - 'id' is defined but never used.,no-unused-vars - 'id' is defined but never used.
- C:\Work\AssignmentCorrector\backend\repos\fed24d-case-af-jobtech-team-14\src\contexts\recentSearchesContext.ts - no-unused-vars - 'q' is defined but never used.
- C:\Work\AssignmentCorrector\backend\repos\fed24d-case-af-jobtech-team-14\src\services\adsService.ts - no-console - Unexpected console statement.,no-console - Unexpected console statement.
- C:\Work\AssignmentCorrector\backend\repos\fed24d-case-af-jobtech-team-14\src\services\filteringServices.ts - no-console - Unexpected console statement.,no-console - Unexpected console statement.,no-console - Unexpected console statement.,no-console - Unexpected console statement.,no-console - Unexpected console statement.,no-console - Unexpected console statement.,no-console - Unexpected console statement.,no-console - Unexpected console statement.

## 🏆 **Betyg: G**
📌 **Motivering:** Ni hämtar data strukturerat via axios från Jobtech JobSearch och Taxonomy, har tydliga tjänster (services), använder React Router, Context/State samt egna custom hooks. Designsystmet (Digi-komponenterna) används genomgående. Extra plus för caching i localStorage/sessionStorage och sparade annonser/senaste sökningar. Dock finns några viktiga brister: Arbetsförmedlingens logotyp används (strider mot uppgiften), några typnings-/importmissar samt mindre kodkvalitetsfrågor.

💡 **Förbättringsförslag:**  
- Ta bort Arbetsförmedlingens logga (och undvik AF-färger). Använd egen neutral logotyp/brand enligt uppgiften.
- Rätta TypeScript-typer och importer:
  • OccupationField/OccupationGroup har felaktiga literal-typer ('string'); använd string.
  • I JobListCard importeras IJob från './JobList' – ska komma från '../models/IJob'.
- Konsistens i Digi-eventprops: använd onAfOnClick (och onAfOnChange) konsekvent i stället för onClick där Digi-komponenten kräver det.
- Korrigera prop-namn: använd afVariation (camelCase) i React-wrapper i stället för af-variation.
- Lägg till dependency-array i useEffect där det är avsett (ex. [] vid init-fetch) för att undvika onödiga re-renders/varningar.
- Importera React Router-API från 'react-router-dom' (Link, NavLink, RouterProvider, createBrowserRouter) för webbmiljö.
- Förbättra fel- och laddningshantering i UI (t.ex. visa felmeddelande om API-fel, skeletons/spinners vid laddning).
- Lägg till grafisk presentation (diagram) av data för extra poäng (t.ex. antal annonser per län/yrkesgrupp med Chart.js/Recharts).
- Städa mindre UI/CSS-detaljer:
  • Undvik inline-styles (använd CSS/klass eller :nth-child för randiga listor).
  • Undvik tomma länkar ('#'); använd riktiga href eller button.
  • Säkerställ meningsfull alt-text på bilder eller markera som dekorativa aria-hidden.
- Typa API-svar strikt i TypeScript (definiera typer för JobSearch-svar i stället för object/any). Typa även SearchContext.ads.
- Överväg paginering/ladda fler (offset/limit) och debouncing av sök för bättre UX.
- Små stavnings-/namnfel: döp om SearcPanel -> SearchPanel för tydlighet.

## 👥 Gruppbidrag

| Deltagare | Antal commits | Commit % | Uppgiftskomplettering | Totalt bidrag |
| --------- | -------------- | -------- | ---------------------- | ------------- |
| JanisSeibutis | 50 | 47.6% | 0.25 | 0.34 |
| mikaelakihl | 38 | 36.2% | 0.25 | 0.29 |
| Alexandra | 14 | 13.3% | 0.25 | 0.2 |
| JanisSeibutis | 3 | 2.9% | 0.25 | 0.16 |


### 📊 Förklaring
- **Antal commits**: Antalet commits som personen har gjort
- **Commit %**: Procentuell andel av totala commits
- **Uppgiftskomplettering**: Poäng baserad på mappning av README-krav mot kodbidrag 
- **Totalt bidrag**: Viktad bedömning av personens totala bidrag (40% commits, 60% uppgiftskomplettering)
