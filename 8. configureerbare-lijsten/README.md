## Doel

Het per Zaakdossier kunnen configuren van kolommen in de Zaakdossier lijst. 

## Context / achtergrond

Standaard bestaat de dossier-lijst uit een aantal kolommen: 'referentienummer', 'aangemaakt door', 'aangemaakt op', en 'laatst gewijzigd op'. De eindgebruiker heeft met deze kolommen dus nooit een goed beeld van waar het dossier inhoudelijk over gaat.

Dossier-lijst kolommen zijn op dit moment aan te passen. Echter, dit vereist een configuratie-wijziging in de frontend-code. Die wijziging is relatief eenvoudig, omdat het om configuratie gaat en niet om een custom frontend component. Het configureren van lijst-kolommen in de beheeromgeving brengt de wens voor zo weinig mogelijk code in een implementatie een stap dichterbij.

Deze wens is sterk gerelateerd aan 'verbeteren Zaakdossier filtering'

## Wat moet er gebeuren - wat is er nog niet en hebben we wel nodig? En wat is het eindresultaat?

### Wat moet er gebeuren - in alle scenario's:
- De kolomdefinities niet ophalen uit de frontend configuratie maar via de API
- Onderscheid maken tussen kolom-typen: text, datum, boolean, ...

| Scenario      | Wat moet er gebeuren | Wat is het eindresultaat | Impact (eerste PO inschatting) |
| :--           | :-----------         | :----------- | :-- |
| 1             | Ophalen configuratie lijstkolommen uit database, autodeployment vanuit configuratie-file in backend code | Het implementatie team zorgt voor de configuratie, wel exporteerbaar | M |
| 2             | Scenario 2 + API/UI ondersteuning voor het beheren van de kolommen | De beheerder vult zelf het pad naar de velden in | M |
| 3             | Scenario 3 + API/UI ondersteuning voor het uitlezen en tonen van de gedefinieerde velden uit het schema | De beheerder kiest de kolommen uit de velden die gedefinieerd zijn in het schema | L |

### Wat is het eindresultaat - in alle scenario's:
- Een lijst met Zaakdossiers waarvan de kolommen configureerbaar zijn. 
- Een tijdsbesparing voor implementatieteams per Zaakdossier, iets wat veel wordt gedaan en wel optelt. 
- Grotere eindgebruikerstevredenheid. Het configureren van een goed dossier-overzicht wordt niet vergeten. Er moet nu een story voor worden geschreven, dat schiet er wel eens bij in, waardoor er zonder extra kolommen wordt opgeleverd. 

## Wat valt er buiten scope?

- Het standaard tonen van data die niet in het Zaakdetail zit. Het tonen van bijvoorbeeld Zaaknummer uit de Zaken API brengt een performance vraagstuk met zich mee.

