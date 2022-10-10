## Doel

Het samenvoegen van de twee 'proceskoppelingen' pagina's, zodat het voor de beheerder duidelijk is waar de proceskoppelingen ingesteld kunnen worden.

## Context / achtergrond

Bij de introductie van het plugin framework is gekozen om een nieuw-naast-oud strategie te hanteren. Op het 'oude' proceskoppelingen scherm kunnen de Open Zaak connector acties geconfigureerd worden, en worden formulieren/form flows aan BPMN taken gekoppeld. In het nieuwe proceskoppelingen scherm kunnen de proceskoppelingen op basis van plugins worden ingesteld.

Hoewel de nieuw-naast-oud strategie goed werkte voor de introductie van de nieuwe feature, is het nu tijd om de volgende stap te zetten. Beide schermen moeten worden samengevoegd en alle scenario's moeten ondersteund worden.

## Wat moet er gebeuren - wat is er nog niet en hebben we wel nodig?

- Implementatie van de laatste Open Zaak acties in de Zaken API plugin (Zaak aanmaken, zetten Zaakstatus, zetten Zaakresultaat en maken Zaakbesluit)
- Implementatie van Form en Form Flow als proceskoppeling
- Samenvoegen van de twee proceskoppelingen schermen

## Wat is het eindresultaat?

Een eenduidige pagina waar de beheerder alle proceskoppelingen kan instellen.

## Wat valt er buiten scope?

- Meer proceskoppelingen, bijvoorbeeld op message events en subprocessen

## Impact - hoeveel inspanning kost dit? 
Inschatting door PO: M  
Inschatting door SA: S/M/X/XL  
