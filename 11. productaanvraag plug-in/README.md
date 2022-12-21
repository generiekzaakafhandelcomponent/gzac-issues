## Doel

Het verkrijgen van inzicht over onvolledige Zaakdossiers, zowel de aanwezigheid als de oorzaak. Het verder kunnen brengen van die onvolledige Zaakdossiers door de beheerder. Meer mogelijkheden om het verwerken van de productaanvraag te configureren.

## Context / achtergrond

GZAC maakt bij het verwerken van de Productaanvraag het Zaakdossier aan. Dat houdt in dat de volgende stappen worden doorlopen:
1. Aanmaken dossier in GZAC
2. Aanmaken Zaak in Open Zaak
3. Aanmaken Rol bij de Zaak
4. Koppelen Documenten aan de Zaak
5. Opstarten BPMN-proces
6. Verwijderen Productaanvraag uit de Objecten API
Als een van deze stappen mislukken hebben we te maken met een onvolledig Zaakdossier.

Door het aanmaken van een Zaakdossier door een Camunda proces te laten doen kunnen we gebruik maken van de ondersteuning die Camunda biedt. Zo kan er per taak een retry-policy worden ingesteld en kunnen acties die wel teruggedraaid kunnen worden gemodelleerd worden met een compensation event. Ook biedt de Camunda Cockpit de mogelijkheid om een retry te forceren, bijvoorbeeld als een probleem in een van de andere componenten is opgelost. Mits er op elke taak een ‘async’ wordt ingesteld kan met dit proces altijd bekeken worden wat de status is en welke acties er wel en niet gelukt zijn. Op die manier geeft het beheerders inzage in wat er eventueel fout is gegaan.

## Wat moet er gebeuren - wat is er nog niet en hebben we wel nodig?

- Ontwikkeling van de Notificaties API plugin
- Ontwikkeling van de Productaanvraag plugin
- Ontwikkelen van een standaard systeem-proces die alle stappen van het aanmaken van een Zaakdossier bevat

## Wat is het eindresultaat?

Meer inzicht in de problemen van een onvolledig Zaakdossier. De mogelijkheid (via de Camunda Cockpit) om een onvolledig Zaakdossier alsnog verder te brengen, waar mogelijk.

## Wat valt er buiten scope?
- Het uitbreiden van de Zaken API plugin voor het aanmaken van de Zaak. Dit wordt waarschijnlijk eerder in een andere feature ontwikkeld.

## Impact - hoeveel inspanning kost dit? 
Inschatting door PO: M/L  
Inschatting door SA: L  

Toevoegen besluit roadmap meeting - hoge prio, onvolledige zaken grote gevolgen
