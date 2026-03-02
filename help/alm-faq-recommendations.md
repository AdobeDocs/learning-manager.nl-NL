---
title: Levenscyclus van administratieve account voor Adobe Learning Manager
description: Dit document bevat een uitgebreid overzicht van het beheer, de configuratie en de compatibiliteitsfuncties van de beveiligingsaccount van Adobe Learning Manager (ALM), die zijn afgestemd op de FedRAMP-aanbevelingen.
jcr-language: en-us
source-git-commit: 06051e44c0a6bc8ae60e44272ba088f2f6ff281f
workflow-type: tm+mt
source-wordcount: '1706'
ht-degree: 0%

---


# Adobe Learning Manager-beveiligingsaanbevelingen

## Welke veiligheid-relevante montages kunnen slechts door de Beheerders van de Douane of de Beheerders van de Integratie in Adobe Learning Manager worden in werking gesteld, en wat zijn hun veiligheidsimplicaties?

De twee geprivilegieerde accounttypen van Adobe Learning Manager — Aangepaste beheerder en integratiebeheerder — hebben elk een gedefinieerde set beveiligingsrelevante instellingen met gedocumenteerde implicaties.

### Aangepaste beheerder: wat ze kunnen doen:

* Aangepaste rollen worden geconfigureerd door de volledige beheerder bij ALM-beheerder > Gebruikers > Aangepaste rollen. Een aangepaste beheerder kan toegang krijgen tot een of meer van deze machtigingencategorieën: Accountbevoegdheden (aankondigingen, gamification, vaardigheden, gebruikersbeheer), Functieprivileges (catalogi, rapporten, tags) en Leerobjectrechten (cursussen, certificeringen, leerpaden).
* Bereik is de meest beveiligingsgevoelige instelling: een aangepaste rol kan worden beperkt tot specifieke gebruikersgroepen en/of specifieke catalogi. Zonder bereikbeperkingen heeft een aangepaste rol in feite platformbrede toegang tot de toegewezen functies, waardoor de voetafdruk van een volledige beheerder nadert.
* Als een aangepaste rol Settings-toegang krijgt onder Accountbevoegdheden, kan die aangepaste beheerder aanmeldingsmethoden, meldingsinstellingen en configuraties op accountniveau wijzigen. Dit is een voorrecht met een hoog effect dat alleen mag worden toegekend met expliciete zakelijke uitvulling.
* Een aangepaste beheerder met Settings-toegang die ook toegang tot de gebruikersentiteit heeft, kan de volledige beheerdersrol aan zichzelf toewijzen, zodat deze effectief escaleert naar volledige beheercontrole.

### Integratiebeheerder: wat ze kunnen doen:

* Integratiebeheerders beheren OAuth 2.0-toepassingsregistraties bij Integratiebeheerder > Toepassingen > Registreren. Ze selecteren een van de zes OAuth-bereiken, variërend van leestoegang tot beheerdersrol voor lees- en schrijftoegang voor studenten. Het lees-/schrijfbereik van de beheerder verleent de geregistreerde toepassing dezelfde rechten als een volledige beheerder via de API.
* Integratiebeheerders configureren FTP, SFTP, Salesforce, Workday en andere connectoren die gebruikersrecords, rollentoewijzingen en cursusvoltooiing importeren en platformgegevens exporteren naar externe systemen.
* OAuth scope for registered applications: minimum required scope. Bied de beheerdersrol nooit lees- en schrijftoegang tenzij strikt noodzakelijk.
* Integratiebeheerders configureren webhooks die realtime ALM-gebeurtenisgegevens (inschrijvingen, voltooide bewerkingen, rolwijzigingen) naar externe URL&#39;s verzenden. Een gecompromitteerd of onjuist gevormd webhook eindpunt is een risico van de gegevensextractie.
* Integratiebeheerders kunnen LTI-integraties configureren. Als deze optie eenmaal is ingeschakeld, kan LTI niet worden uitgeschakeld. Ongeautoriseerde toegang tot cursusinhoud via externe LMS-platforms is nu mogelijk.


## Wat zijn de geadviseerde veilige gebreken voor hoogste administratieve en bevoorrechte rekeningen in Adobe Learning Manager, en waar worden zij gevormd?

### Standaardwaarden voor beheerdersaccount op hoofdniveau (geconfigureerd bij eerste provisioning):

* Aanmeldingsmethode voor interne gebruikers: Single Sign-On (SSO) via SAML 2.0: geconfigureerd op ALM-beheerder > Instellingen > Aanmeldingsmethoden. Gebruik Adobe ID niet voor medewerkers of beheerders.
* Verificatie in twee stappen (2FA): afgedwongen voor alle gebruikers: geconfigureerd in Adobe Admin Console > Instellingen > Privacy en beveiliging > Verificatie-instellingen.
* Maximale sessieduur: 8 uur (of per organisatiebeleid): geconfigureerd op Adobe Admin Console > Instellingen > Privacy en beveiliging > Geavanceerde instellingen.
* Maximale inactieve tijd: 30 minuten (of per organisatiebeleid): dezelfde locatie als hierboven.
* Inactieve gebruiker automatisch verwijderen: Ingeschakeld met een door de organisatie gedefinieerde retentieperiode (bijvoorbeeld 90 dagen inactiviteit): ALM-beheerder > Instellingen > Algemeen.
* Vervaldatum van extern gebruikersprofiel: Stel de instelling in op elk extern profiel bij het maken - ALM-beheerder > Gebruikers > Extern. Geen onbepaalde externe profielen.
* Beperkingen voor IP-toegang: Beperk waar mogelijk tot goedgekeurde IP-bereiken: Admin Console > Instellingen > Geavanceerde instellingen.

### Standaardwaarden voor aangepaste beheerdersrol (geconfigureerd bij het maken van elke rol):

* OAuth scope for registered applications: minimum required scope. Bied de beheerdersrol nooit lees- en schrijftoegang tenzij strikt noodzakelijk.
* Bereik aangepaste rol: beperkt tot specifieke gebruikersgroepen en specifieke catalogi. Maak geen aangepaste rollen met het bereik Alle gebruikers en Alle catalogi, tenzij de functie deze vereist.
* Instellingstoegang in aangepaste rollen: niet verlenen, tenzij de specifieke functie dit vereist, gezien het escalatierisico met bevoegdheden.

### Standaardwaarden integratiebeheerder:

* API OAuth-bereik: selecteer het meest restrictieve bereik dat voldoet aan de vereisten van de integratie. Geef de beheerder geen lees- en schrijfrechten voor toepassingen die alleen studenten lezen.
* Verbindingsgegevens, LTI-referenties en webhook-URL&#39;s: behandelen als gevoelige geheimen — delen nooit via e-mail of toewijzen aan bronbesturing.

## Biedt Adobe Learning Manager beheerders een manier om de huidige accountinstellingen te vergelijken met de aanbevolen beveiligde standaardinstellingen?

Adobe Learning Manager heeft geen speciaal vergelijkingsdashboard dat automatisch naast de aanbevolen beveiligde standaardinstellingen de huidige instellingen toont. Met drie platformmogelijkheden kunnen beheerders huidige configuraties echter handmatig of programmatisch controleren en vergelijken.

### Rapport aangepaste rol - huidige geprivilegieerde roltoewijzingen:

Navigeer in ALM naar Beheer > Gebruikers > Aangepaste rollen en klik op Downloaden (rechtsboven) om een CSV te exporteren van alle aangepaste rollen, hun machtigingensets en hun bereiktoewijzingen.

### ALM REST API-programmatische configuratiereeks:

* Het GET /account-eindpunt retourneert configuratiegegevens op accountniveau in JSON-indeling, toegankelijk via het OAuth-bereik van de beheerdersrol. Klanten kunnen dit eindpunt programmatisch aanroepen.
* Het GET /users eindpunt (met include=role filter) retourneert de huidige roltoewijzingen voor alle gebruikers, waardoor automatische detectie van onverwachte roltoewijzingen mogelijk is. Gebruik de Jobs-API voor bulkgebruikersexport.

## Kunnen beheerders de huidige beveiligingsinstellingen en -configuraties vanuit Adobe Learning Manager exporteren in een machinaal leesbare indeling?

Adobe Learning Manager ondersteunt het exporteren van beveiligingsgerelateerde configuratiegegevens via verschillende mechanismen. Geen enkele export geeft een volledige momentopname van alle beveiligingsinstellingen tegelijk, maar de volgende exportbewerkingen beslaan samen het volledige bereik van voor de beveiliging relevante gegevens.

### Auditlogbestand van Admin Console — CSV-export van alle verificatie- en rolwijzigingen:

* In Adobe Admin Console, navigeer aan **Inzichten > Logboeken > Logboek van de Controle**, pas filters toe zoals nodig, en klik **Uitvoer CSV**
* De geëxporteerde CSV registreert elke administratieve handeling, inclusief: wijzigingen in 2FA-handhaving, wijzigingen in sessielimieten, toewijzingen en verwijderingen van beheerdersrol, verwijderingen van gebruikers en wijzigingen in productmachtigingen — allemaal met tijdstempels en actoridentiteit.
* De gegevens worden 90 dagen bewaard. Gebruikers van Global Admin Consoles kunnen logboeken exporteren in alle organisaties.

### ALM REST API — JSON-export van huidige roltoewijzingen en accountconfiguratie:

* `GET /account` — retourneert instellingen op accountniveau in JSON, inclusief actieve aanmeldingsconfiguratiegegevens en accountmetagegevens.
* `GET /users?include=role` — retourneert alle gebruikers met hun rollen die momenteel zijn toegewezen in JSON.
* `GET /userGroups` — retourneert alle gebruikersgroepen en hun lidmaatschap, relevant voor de controle van het aangepaste rolbereik.
* Alle API-reacties zijn JSON (`vnd.api+json`). Verificatie gebruikt OAuth 2.0 met lees-/schrijfbereik van beheerdersrol.

### CSV-export van aangepaste rol — huidige geprivilegieerde roldefinities:

* ALM-beheerder > Gebruikers > Aangepaste rollen > Downloaden exporteert een CSV van alle aangepaste roldefinities, hun machtigingencategorieën en bereiktoewijzingen.
* Deze export kan worden gebruikt als een machinaal leesbare momentopname van de huidige geprivilegieerde accountconfiguratie.

### Banen-API — bulkgebruikers- en rolgegevens:

* De API voor ALM-taken ondersteunt het op aanvraag genereren van gebruikersrapporten (inclusief roltoewijzingen) in CSV-indeling. Deze kunnen worden gepland en verbruikt door externe compliance- of SIEM-tools.

Zie [&#x200B; Adobe Learning Manager - de ontwikkelaarshandleiding van de Toepassing &#x200B;](https://experienceleague.adobe.com/nl/docs/learning-manager/using/integration/developer-manual) voor meer informatie.

## Biedt Adobe Learning Manager een API waarmee beveiligingsrelevante instellingen via programmacode kunnen worden weergegeven en aangepast?

Adobe Learning Manager biedt een volledige REST API v2 die programmatisch het bekijken en aanpassen van beveiligingsrelevante instellingen mogelijk maakt met OAuth 2.0-verificatie. Hieronder vindt u de specifieke API-mogelijkheden die relevant zijn voor beveiligingsinstellingen:

### Verificatie en bereik

* De toepassingen worden geregistreerd door de Beheerder van de Integratie bij **Admin van de Integratie > Toepassingen > Registreren**. OAuth 2.0 Client ID en Secret worden uitgegeven per toepassing.
* Er zijn zes bereiken beschikbaar. Voor het beheer van veiligheidsmontages, **wordt de lees-schrijftoegang van de rol Admin** &lbrace;vereist. Hierdoor krijgt de toepassing dezelfde toegang als een volledige beheerder via de API.
* Toegangstokens worden verkregen via de standaard OAuth-verificatiecode of de workflow voor clientreferenties.\
  **Basis URL:**\
  `https://learningmanager.adobe.com/primeapi/v2/`

### Gebruiker- en rolbeheer via API

* `GET /users` — alle gebruikers en hun huidige rollen ophalen
* `POST /users` — programmatisch nieuwe gebruikers voorzien
* `PATCH /users/{id}` — update gebruikerskenmerken, inclusief roltoewijzingen
* `DELETE /users/{id}` — een gebruikersaccount uitschakelen
* `POST /users/{id}/purge` — leegmaken van een gebruiker en alle bijbehorende records definitief

### Ophalen accountconfiguratie

* `GET /account` — retourneert configuratie op accountniveau, inclusief accountinstellingsgegevens in JSON-indeling, waaronder velden zoals:
   * `complianceLabelDefaultID`
   * `showComplianceLabel`
   * `custom_injections`

### Adobe User Management API (laag Admin Console)

* De UMAPI (Adobe User Management API) biedt programmatische toegang tot bewerkingen van Admin Consoles:
   * Gebruikersinrichting
   * Toewijzing van productrechten
   * Systeembeheerder-roltoewijzing op organisatieniveau
* UMAPI staat los van de ALM REST-API en werkt op organisatieniveau van de Adobe. Gebruik dit schema voor het automatiseren van de roltoewijzingen van Admin Consoles en gebruikersprovisioning.

## Publiceert Adobe Learning Manager zijn veilige configuratie-richtlijnen — de aanbevolen standaardinstellingen — in een machinaal leesbare indeling zoals OSCAL, JSON of YAML?

Adobe Learning Manager publiceert momenteel de Secure Configuration Guide niet in een voor computers leesbare indeling.

## Is de veilige Gids van de Configuratie van Adobe Learning Manager openbaar beschikbaar zonder een login of een speciale toegang te vereisen?

Ja. Adobe Learning Manager&#39;s Secure Configuration Guide is openbaar beschikbaar op Adobe Experience League. Er is geen account, aanmelding of licentie vereist om toegang te krijgen tot deze account.

Wat openbaar beschikbaar is:

* FRR-RSC-01: Veilige handleiding voor beheer: volledige levenscyclusbegeleiding voor beheeraccounts op topniveau.
* FRR-RSC-02: Administratieve Montages van de Veiligheid en Implicaties — alle veiligheidsrelevante montages, hun implicaties, en geadviseerde gebreken.

## Biedt Adobe Learning Manager versiebeheer en een releasegeschiedenis waarmee bureaus wijzigingen in beveiligingsrelevante instellingen en aanbevolen standaardinstellingen kunnen bijhouden?

Adobe Learning Manager houdt een openbaar beschikbare, gedetailleerde releasegeschiedenis bij voor elke productupdate. Beveiligingsrelevante wijzigingen in beheerinstellingen, verificatiemogelijkheden, API-eindpunten en functies voor rolbeheer worden in elke release gedocumenteerd.

### Opmerkingen bij de ALM-release — Genummerde, cumulatieve wijzigingshistorie

* De Adobe publiceert genummerde versienota&#39;s voor elke update van Adobe Learning Manager (b.v., *Update 100*, *Update 99*).
* Deze worden gepubliceerd op **Experience League** en document:
   * Nieuwe functies
   * Wijzigingen in bestaande instellingen
   * API-toevoegingen en -verwijderingen
   * Connectorveranderingen
   * Verouderde mogelijkheden
* Elke versienota omvat een specifieke sectie voor **API veranderingen**, een lijst makend:
   * Nieuwe eindpunten
   * Gewijzigde antwoordvelden
   * Afwijkingen
   * Deze zijn direct relevant voor veiligheid-relevante configuratiemogelijkheden.

### &quot;Nieuwe functies&quot;-pagina&#39;s — overzichtssamenvattingen per release

* Elke belangrijke versie heeft een specifieke **&quot;Wat is Nieuw&quot;** pagina documenterend nieuwe veiligheid-relevante eigenschappen met context.
* Voorbeelden van gedocumenteerde beveiligingsupdates zijn:
   * Wijzigingen in de verwerking van aangepaste rolmachtigingen
   * Toevoeging van de zichtbaarheid van door CSV gemaakte machtigingen voor aangepaste rollen
   * Wijzigingen in API-snelheid beperken

### Lijst met API-implementaties — gezaghebbende record van verwijderde API-mogelijkheden

* De Adobe handhaaft een specifieke **API pagina van Afschrijvingen** die van alle afgekeurde en verwijderde eindpunten ALM API, met inbegrip van de versieversie een lijst maken waarin elke afschrijving voorkwam.
* Voorbeelden van voor de beveiliging relevante afwijzingen zijn:
   * Wijzigingen in het sorteergedrag van het eindpunt van `GET /users` en overschrijven
   * Melding, filtervereisten voor rapportdatum

