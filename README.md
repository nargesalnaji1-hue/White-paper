# White-paper
WeatherNow är inte ett stort företag och de gör en väderapp. Det som appen visar är temperatur, regn och prognoser. Syftet eller målet med appen är att användaren snabbt ska kunna se vädret utan reklam eller något annat. Appen är populär, men tyvärr har företaget haft många problem med sina releaser. Kod släpps för snabbt, tester saknas och buggar hamnar i produktion. Det gör att appen ibland visar fel väder eller slutar fungera helt. Detta skapar stress för utvecklarna och irritation hos användarna.

De flesta problemen i företaget beror på att företaget saknar en bra och tydlig arbetsprocess. Utvecklarna jobbar direkt i main-branchen, och det finns ingen staging-miljö där man kan testa saker innan det går live. Ibland körs inga tester alls och ibland körs tester inte automatiskt. När de har bråttom släpper de ut koden utan att kontrollera kvaliteten, vilket gör att fel slinker igenom.

För att lösa detta behövs en modern och automatiserad release-pipeline. Företaget använder C#/.NET, MongoDB och GitHub, så GitHub Actions passar bra. Utvecklarna ska jobba i egna feature branches istället för direkt i main. När kod pushas ska automatiska unit tests köras direkt. Om testerna inte går igenom stoppas processen.

När en pull request skapas ska en annan utvecklare göra code review innan koden får mergas. Detta är viktigt för att minska risken för fel och säkerställa att koden följer standard. När koden är godkänd och mergad körs en ny pipeline som bygger projektet och kör integrationstester. Efter det deployas systemet till en testmiljö där man kan verifiera funktioner.

Om allt fungerar skickas koden vidare till en staging-miljö som liknar produktion. Där körs enklare E2E-tester för att kontrollera viktiga användarflöden, till exempel att väderdata laddas korrekt och visas rätt i appen. Först efter detta görs en manuell godkänning innan produktion.

Teststrategin ska vara uppdelad i 70% unit tests, 20% integrationstester och 10% E2E-tester. Unit tester är viktigast eftersom de fångar fel tidigt och är snabba att köra vid varje ändring.

Detta kallas Continuous Delivery, vilket betyder att kod alltid är redo att släppas men att en person godkänner innan produktion. Detta minskar risken för att fel påverkar användare direkt.

Jag har lärt mig hur en release‑kedja fungerar och varför automatisering är viktigt. Nu vet jag att tester och pipelines hjälper till att stoppa buggar innan de når användarna. Det här kommer vara nyttigt när jag söker LIA eller jobb. detta va det so jag gjorde och fick ig på de samt så fick jag detta komnetraret från min lärare Det här är alldeles för kortfattat för att vara en "strategi" som företaget kan följa. Det framgår t.ex. inte för en utvecklare HUR de ska göra, i vilken utsträckning och på vilket sätt.
