## Doel

Het kunnen toewijzen van een zaakdossier aan een specifieke gebruiker, zodat andere gebruikers kunnen zien dat het desbetreffende zaakdossier al onderhanden is.  

## Context / achtergrond

Veel gemeentelijke gebruikers werken in teams van personen met dezelfde rol. Deze gebruikers kunnen dus elk willekeurig nieuw zaakdossier dat binnenkomt oppakken. Het kan een poosje duren voordat een gebruiker de eerste gebruikerstaak die klaarstaat in het zaakdossier afrondt, omdat de gebruiker eerst de inhoud van het zaakdossier tot zich moet nemen. In de tussentijd kan een collega hetzelfde zaakdossier openen en ook beginnen met het tot zich nemen van de inhoud van het zaakdossier. Op dat moment zijn er dus 2 medewerkers met hetzelfde zaakdossier bezig zonder dat ze dat van elkaar weten. Dit is niet wenselijk. 

Daarnaast is het wenselijk om een zogenaamde ‘werkverdeler’ om zaakdossiers toe te laten wijzen aan bepaalde behandelaars. Dit is vooral van belang omdat bepaalde behandelaars beter in staat zijn om de meer ‘complexere’ zaken op te pakken dan andere behandelaars.

## Wat moet er gebeuren - wat is er nog niet en hebben we wel nodig?

- Toevoegen van een eigenschap 'behandelaar' aan de tabel 'documents'
- Aanpassing user interface:
  - Dropdown met gebruikers uit Keycloak (dossier detail scherm)
  - Weergave huidige behandelaar (dossier detail scherm)
  - Weergave huidige behandelaar (dossier lijst scherm)
- API ondersteuning voor bovenstaande aanpassingen
- Standaard code beschikbaar voor het instellen van een behandelaar vanuit een proces

## Wat is het eindresultaat?

- Het is in GZAC mogelijk om een behandelaar aan een zaakdossier toe te wijzen, te wijzigen en te verwijderen
- Behandelaar kan worden geselecteerd uit de lijst van gebruikers
- De behandelaar is zichtbaar in het dossier detail scherm en het dossier lijst scherm
- In implementaties kan de behandelaar worden ingesteld met behulp van een expressie in een BPMN model

## Wat valt er buiten scope?

- Het opslaan en ophalen van de behandelaar uit de Zaken API

## Impact - hoeveel inspanning kost dit? 
Inschatting door PO: S
