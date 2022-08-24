## Doel

Het per Zaakdossier kunnen configuren van filters op de Zaakdossier lijst. 

## Context / achtergrond

Het filteren van Zaakdossier bestaat standaard uit het filteren op een case-nummer en vrije tekst. Gebruikers hebben de behoefte om hun Zaakdossiers verfijnder te filteren op specifieke eigenschappen. Voorbeeld: 'een lijst van alle zaakdossiers van behandelaar X, met betrekking tot buurt Y, ouder dan datum Z'. Op dit moment wordt deze wens in implementatie-code ingevuld, de wens is dat generiek te doen. 

## Wat moet er gebeuren - wat is er nog niet en hebben we wel nodig?

- Het filterscherm in de UI verplaatsen naar boven het lijstscherm, de huidige locatie is onconfentioneel en wordt slecht gevonden. 
- Het mogelijk maken om te filteren op eigenschappen uit het Zaakdetail Object (document).
- Het mogelijk maken om te filteren op eigenschappen uit de Zaak - indien aanwezig. (geen must voor MVP)
- Via een configuratie, zonder code (maar niet via de UI)

## Wat is het eindresultaat?

- Een configureerbaar, standaard filter op de Zaakdossierlijst. 
- Een kleine tijdsbesparing voor implementatieteams per Zaakdossier, iets wat veel wordt gedaan en wel optelt. 
- Grotere eindgebruikerstevredenheid. Het configureren van een goede filter wordt niet vergeten. Er moet nu een story voor worden geschreven, dat schiet er wel eens bij in, waardoor er zonder filter wordt opgeleverd. 

## Wat valt er buiten scope?

- Het configurabel maken van de lijst via settings.
- Het filteren op eigenschappen van andere gerelateerde informatie (objecten), zoals Zaakobjecten, Haalcentraal, Klant. Dus: filteren = data in Zaakdetail Object, ook als dat duplicaat data oplevert. 

## Impact - hoeveel inspanning kost dit, eerste inschatting van de PO?

M
