## Doel

Het per Zaakdossier kunnen configuren van filters op de Zaakdossier lijst. 

## Context / achtergrond

Het filteren van Zaakdossier bestaat standaard uit het filteren op een case-nummer en vrije tekst. Gebruikers hebben de behoefte om hun Zaakdossiers verfijnder te filteren op specifieke eigenschappen. Voorbeeld: 'een lijst van alle zaakdossiers van behandelaar X, met betrekking tot buurt Y, ouder dan datum Z'. Op dit moment wordt deze wens in implementatie-code ingevuld, de wens is dat generiek te doen. 

## Wat moet er gebeuren - wat is er nog niet en hebben we wel nodig? En wat is het eindresultaat?

### Wat moet er gebeuren - in alle scenario's:
- Het filterscherm in de UI verplaatsen naar boven het lijstscherm, de huidige locatie is onconventioneel en wordt slecht gevonden. 
- Onderscheid maken tussen like-search en exact-search
- Onderscheid maken tussen OR-search en AND-search

| Scenario      | Wat moet er gebeuren | Wat is het eindresultaat | Impact (eerste PO inschatting) |
| :--           | :-----------         | :----------- | :-- |
| 1             | Ophalen configuratie filterscherm vanuit configuratie-file in frontend code | Het development team implementeert, niet exporteerbaar | S |
| 2             | Ophalen configuratie filterscherm uit database, autodeployment vanuit configuratie-file in backend code | Het development team implementeert, wel exporteerbaar | M |
| 3             | Scenario 2 + API/UI ondersteuning voor het beheren van de velden | De beheerder vult zelf het pad naar de velden in | L |
| 4             | Scenario 3 + API/UI ondersteuning voor het uitlezen en tonen van de gedefinieerde velden uit het schema | De beheerder kiest uit de velden die gedefinieerd zijn in het schema | XL |

### Wat is het eindresultaat - in alle scenario's:
- Een configureerbaar, standaard filter op de Zaakdossierlijst. 
- Een tijdsbesparing voor implementatieteams per Zaakdossier, iets wat veel wordt gedaan en wel optelt. 
- Grotere eindgebruikerstevredenheid. Het configureren van een goede filter wordt niet vergeten. Er moet nu een story voor worden geschreven, dat schiet er wel eens bij in, waardoor er zonder filter wordt opgeleverd. 

## Wat valt er buiten scope?

- Het configurabel maken van de lijst via settings.
- Het filteren op eigenschappen van andere gerelateerde informatie (objecten), zoals Zaakobjecten, Haalcentraal, Klant. Dus: filteren = data in Zaakdetail Object, ook als dat duplicaat data oplevert. 
