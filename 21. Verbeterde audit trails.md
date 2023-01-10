## Doel
Grip krijgen op wat voor acties er uit worden gevoerd, door wie ze zijn uitgevoegd en wat de context van de acties waren op dat moment. 

## Context / achtergrond
Momenteel worden bepaalde acties voor een dossier geaudit. Alles buiten de context van een dossier wordt echter niet geaudit. Als meerdere
documenten tegelijkertijd in de gaten moeten worden gehouden, dan moeten de audit logs van de dossiers individueel worden bekeken. Vragen
als "Wie heeft de meest recente versie van het BPMN model geupload?", "Wanneer is de OpenZaak plugin voor het laatst geconfigureerd?" en
"Wie heeft het dossier verwijderd?" kunnen momenteel allemaal niet worden beantwoord binnen Valtimo. Er is een duidelijke noodzaak voor
betere auditing.

## Wat moet er gebeuren - wat is er nog niet en hebben we wel nodig?
1. Ondersteuning voor audit records moet worden toegevoegd. Audit records horen in ieder geval de volgende elementen te bevatten:
  * Actie type (view, create, edit, delete).
  * Actie status (success, failure).
  * Wie de actie uit heeft gevoerd.
  * Van waaruit de actie is uitgevoerd (IP).
  * De gerelateerde objecten (dossier, dossier definitie, taak, formulier, etc).
  * De event die de auditing heeft getriggered (bijvoorbeeld wat de wijziging was in het document).
2. Bestaande auditing moet worden vervangen worden door de nieuwe auditing:
  * Succesvolle en gefaalde acties moeten beide worden gelogd.
  * Koppelingen met gerelateerde objecten moeten worden vastgelegd.
  * Bestaande audit records migreren naar het nieuwe auditing formaat.
3. De bestaande auditing tab moet aansluiten op de nieuwe auditing.
4. Een admin pagina toevoegen waar alle audit records (paginated) zichtbaar zijn.
5. Audit records moeten doorzoekbaar zijn op bepaalde velden.
6. Auditing toepassen op alle bestaande modules. Kan gefaseerd aan worden gepakt.


## Wat is het eindresultaat?
Grip op auditing, met de mogelijkheid om dit verder uit te breiden (bijvoorbeeld door filtering toe te voegen, nieuwe soorten acties te kunnen
auditen, etc).

## Wat valt er buiten scope?

## Impact - hoeveel inspanning kost dit? 
Inschatting door PO: S/M/L/XL  

Inschatting door SA, uitgaande van punten 1, 2, 3, 4, 6: M

5 kan afhankelijk van invulling de scope vergroten.

## Besluiten roadmap overleg
