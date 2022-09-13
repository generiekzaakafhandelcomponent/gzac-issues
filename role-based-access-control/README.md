## Doel

Een generieke oplossing leveren waarmee op zero-trust base finegrained toegang wordt verleend aan resources in de Haagse referentie architectuur. 

## Context / achtergrond

Binnen de Haagse referentie architectuur is de authenticatie (wie ben je) goed geborgd. De authorisatie (wat mag je) is in de individuele micro services ingebouwd. Daarin wordt onvoldoende geboden: 

- Het is niet fine grained: er kan op onvoldoende detailniveau worden bepaald wie welke toegang heeft. 
- Het is niet consistent, per micro service wordt een specifieke aanpak gekozen. 
- Er wordt veel gewerkt met machine2machine authenticatie: een machine krijgt volledige toegang tot een resource. 
- De rechten zijn vastgelegd in de code of een database en kunnen (dus) niet automatisch worden getest.
- Als de rechten zijn aangepast in code zijn ze lastig aanpasbaar en slecht verifieerbaar. 
- Rechten-structuren zijn niet uitwisselbaar. 

Er is dus behoefte aan een architectuur gebaseerd op een open standaard, inpasbaar in alle micro services, centraal te beheren, zero-trust. 

## Wat moet er gebeuren - wat is er nog niet en hebben we wel nodig?

Application layer:
 
1. Converting a RBAC-requirements from (existing) project specification to a Policy-file. Take a real live example, ask a business analyst for the best project.
2.  Common Ground Layer 1 / 2: deploy a sidecar with Envoy, Istio and OPA next to OpenZaak (screenshot). (this is the alternative to having a centralized API GW).  
3. Common Ground Layer 4: deploy a sidecar with Envoy, OPA next to GZAC. (screenshot). (this is without Istio, having the application communicating directly with OPA).
3. Common Ground Layer 4 part 2: Proof of a SQL query in GZAC can be altered based on OPA-policy.
4. Common Ground Layer 5: Proof of a function the Angular UI can be shown/hidden based on the OPA-policy. (note – location of this OPA tbd, could be second sidecar or same as used for backend).
 
Networking / DevOps:
 
1. Proof integration OPA with Broadcom API GW Den Haag on prem.  
2. Proof integration OPA with Kubernetes native centralized API Gateway Istio (compared to the Kong setup that’s already proven). Come up with a short pro’s/con’s list to compare both. https://stackshare.io/stackups/istio-vs-kong#:~:text=Istio%20has%20an%20inbuilt%20turn%20key%20solution%20with%20Rancher%20whereas,blue%2Dgreen%2C%20proxy%20caching.
3. Setup Envoy / Istio / OPA

## Wat is het eindresultaat?

Een MVP, draaiende op de infra van Den Haag, voorzien van OPA, gekoppeld aan Styra. Een productiewaardig minimale setup (MVP): 
- in de UI in GZAC alleen de Zaakdossier-types (in het linkermenu) te zien zijn waar de gebruiker recht op heeft.  
- in het lijstscherm van Zaakdossiers alleen die instances van Zaken worden getoond waar de gebruiker recht op heeft. 
- in het lijstscherm van Zaakobjecten binnen een Zaakdossier alleen die Objecten waar de gebruiker rechten voor heeft. 

Een kort verslag & advies op basis van de opgedane ervaring, met antwoorden op: 

- Algemene indruk: advies om door te gaan?
- Is OPA beheerbaar zonder Styra? Tot welk niveau van complexiteit. 
- Performance voldoende? 
- Vanuit DevOps perspectief beheerbaar tegen acceptabele instapping?
- Memo-load acceptabel?
- Is de complexiteit van de Policy files te beheersen?
- Kong of Istio?

## Wat valt er buiten scope?

- Testen met NLX
- OpenKlant
- Alle niet genoemde queries
- Een visie op Governance

## Impact - hoeveel inspanning kost dit?

Inschatting business (RH): L
