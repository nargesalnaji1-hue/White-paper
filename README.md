# White-paper
WeatherNow
WeatherNow är inte ett stort företag och de gör en väderapp. Det som appen visar är temperatur, regn och prognoser. Syftet eller målet med appen är att användaren snabbt ska kunna se vädret utan reklam eller något annat. Appen är populär, men tyvärr har företaget haft många problem med sina releaser. Kod släpps för snabbt, tester saknas och buggar hamnar i produktion. Det gör att appen ibland visar fel väder eller slutar fungera helt. Detta skapar stress för utvecklarna och irritation hos användarna.
De flesta problemen i företaget beror på att företaget saknar en bra och tydlig arbetsprocess. Utvecklarna jobbar direkt i main‑branchen, och det finns ingen staging‑miljö där man kan testa saker innan det går live. Ibland körs inga tester alls och ibland körs tester inte automatiskt. När de har bråttom släpper de ut koden utan att kontrollera kvaliteten, vilket gör att fel slinker igenom.
För att lösa detta behövs en modern och automatiserad release‑pipeline. Företaget använder C#/.NET, MongoDB och GitHub, så GitHub Actions passar bra. En bra pipeline börjar med att utvecklaren jobbar i en egen branch. När man pushar kod körs automatiskt enhetstester. Sedan, när de är klara med koden, gör de en pull request. Det betyder att någon annan i teamet snabbt kollar igenom koden så att inget blir fel.
När koden blir godkänd och mergas till main körs allt automatiskt. Projektet byggs automatiskt och skickas till en testmiljö, och där kan man testa om appen fungerar och att allt är rätt. Om testerna är okej och allt fungerar kan en person klicka på ”godkänn”. Då skickas koden vidare till produktion. Detta kallas Continuous Delivery. Det betyder att koden alltid är redo att släppas, men att en människa bestämmer när den faktiskt går ut. Det passar företaget eftersom de vill undvika misstag.
En enkel trigger kan se ut så här:
on:
  push:
    branches: ["main"]

Jag har lärt mig hur en release‑kedja fungerar och varför automatisering är viktigt. Nu vet jag att tester och pipelines hjälper till att stoppa buggar innan de når användarna. Det här kommer vara nyttigt när jag söker LIA eller jobb.
