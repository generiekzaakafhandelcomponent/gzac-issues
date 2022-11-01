## Doel

Het doel is om de Objecten in de 'Overige Objecten Regisistratie (https://vng.nl/projecten/overige-objecten-registratie-api), kortweg Objecten API, toegankelijk te 
maken via een menu-item in GZAC. 

## Context / achtergrond

Objecten zijn in de Haagse referentie architectuur opgedeeld in Objecten die bestaan in reletatie tot een Zaakdossier (gerelateerde zaakobjecten) en objecten die opzichzelf (ook) bestaan (zelfstandig zaakobjecten). De VNG kent dit onderscheid (nog) niet, maar onderkent wel de Overige Objecten. Dit zijn Objecten die op zichzelf staan, zonder dat daar een Zaak aan gerelateerd is. Overigens worden dit weer Zaakobjecten als ze aan een Zaak gekoppeld worden. 
Voorbeelden van objecten zijn laadpalen, parkeerplaatsen en bomen. 

De wens is om deze Objecten te kunnen benaderen vanuit een menu-item, zonder dat er een Zaak voor bestaat. De concrete case zijn nu mensen op de wachtlijst voor een Woonwagenplaats em de lijst van Objecten met woonwagenplaatsen. Een eerste variant van dit concept is te vinden in het proces 'SSV'. 

De UX wordt aangeleverd voor start dev. 

## Wat moet er gebeuren - wat is er nog niet en hebben we wel nodig?

- Te configureren (zichtbaar/niet zichtbaar) hoofdmenu-item 'Objecten'
- Daaronder te configureren (zichtbaar/niet zichtbaar) submenu-item 'Naam_van_Object_type' (bijvoorbeeld 'Laadpalen'). Deze lijst toont alle Objecten van 1 type. 
- Een lijstscherm van Objecten, met in code/configuratie te configureren kolommen, waarbij elke kolom 1 waarde uit het Object toont
- Een detailscherm van een object, waarbij de data wordt getoond dmv een formio definitie. 
- De mogelijkheid deze data te wijzigen en op te slaan. Elke gebruiker met toegang heeft volledige rechten in MVP. 
- Een MVP zoek op 1 in te stellen waarde, zodat gezocht kan worden in Objecten.
- De mogelijkheid om een proces te starten vanuit een Object. Daarbij wordt in code/configuratie gezet: 
-- welk proces wordt gestart
-- welke variabelen aan dat proces worden meegegeven

## Wat is het eindresultaat?

Een lijst / zoek /detailscherm voor Objecten. 

## Wat valt er buiten scope?

- Uitgebreide zoek / filtering
- PBAC
- No-code configuratie
- Het editten van delen van een Object
- Het zien van Zaken die gerealteerd zijn aan een Object

## Impact - hoeveel inspanning kost dit? 
Inschatting door PO: M/L
Inschatting door SA: 
