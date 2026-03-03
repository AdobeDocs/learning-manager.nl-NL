---
title: Adobe Learning Manager - beveiligingsinstellingen en configuratiebeheer
description: In dit document worden de beheeraccounttypen, beveiligingsinstellingen, aanbevolen beveiligingsstandaardinstellingen, API-mogelijkheden, exportfunctionaliteit, vergelijkingsmethoden voor configuratie, publicatiepraktijken en versiehistorie van Adobe Learning Manager beschreven. Het verstrekt gedetailleerde begeleiding op hoe de bevoorrechte rekeningen werken, hun veiligheidsimplicaties, en hoe het configuratiebeheer over het platform wordt gesteund.
jcr-language: en-us
exl-id: a2e34104-c417-407f-af85-9f3f4b2a9fcb
source-git-commit: 8b4ac7a99a9bf0cbeaa4ed07fd979deb7130302d
workflow-type: tm+mt
source-wordcount: '1944'
ht-degree: 0%

---

# Beveiligingsinstellingen en configuratiebeheer

Deze handleiding bevat gedetailleerde antwoorden op FedRAMP-aanbevelingen (FRR-RSC-03 tot FRR-RSC-08) voor Adobe Learning Manager (ALM). Hierin worden best practices voor beveiliging, aanbevolen beveiligde standaardinstellingen en tools voor het controleren, exporteren en beheren van geprivilegieerde accountinstellingen beschreven. Het document is ontworpen voor beheerders en compatibiliteitsteams om een veilige configuratie en beheer van ALM-accounts te garanderen.

Ook worden gebieden gemarkeerd waarop ALM geheel of gedeeltelijk voldoet aan FedRAMP-standaarden, met verwijzingen naar ondersteunende documentatie en bronnen die beschikbaar zijn op Adobe Experience League.

+++Welke veiligheid-relevante montages kunnen slechts door de Beheerders van de Douane of de Beheerders van de Integratie in Adobe Learning Manager worden in werking gesteld, en wat zijn hun veiligheidsimplicaties?

Adobe Learning Manager&#39;s twee geprivilegieerde accounttypen: Aangepaste beheerder en integratiebeheerder. Elk object heeft een gedefinieerde set beveiligingsrelevante instellingen met gedocumenteerde implicaties.

**Beheerder van de Douane — wat zij** kunnen in werking stellen:

* Aangepaste rollen worden geconfigureerd door de volledige beheerder bij ALM-beheerder > Gebruikers > Aangepaste rollen. Een aangepaste beheerder kan toegang krijgen tot een of meer van deze machtigingencategorieën: Accountbevoegdheden (aankondigingen, gamification, vaardigheden, gebruikersbeheer), Functieprivileges (catalogi, rapporten, tags) en Leerobjectrechten (cursussen, certificeringen, leerpaden).
* Bereik is de meest beveiligingsgevoelige instelling: een aangepaste rol kan worden beperkt tot specifieke gebruikersgroepen en/of specifieke catalogi. Zonder bereikbeperkingen heeft een aangepaste rol in feite platformbrede toegang tot de toegewezen functies, waardoor de voetafdruk van een volledige beheerder nadert.
* Als een aangepaste rol Settings-toegang krijgt onder Accountbevoegdheden, kan die aangepaste beheerder aanmeldingsmethoden, meldingsinstellingen en configuraties op accountniveau wijzigen. Dit is een voorrecht met een hoog effect dat alleen mag worden toegekend met expliciete zakelijke uitvulling.

**Beheerder van de Integratie — wat zij** kunnen in werking stellen:

* Integratiebeheerders beheren OAuth 2.0-toepassingsregistraties bij Integratiebeheerder > Toepassingen > Registreren. Ze selecteren een van de zes OAuth-bereiken, variërend van leestoegang tot beheerdersrol voor lees- en schrijftoegang voor studenten. Het lees-/schrijfbereik van de beheerder verleent de geregistreerde toepassing dezelfde rechten als een volledige beheerder via de API.
* Integratiebeheerders configureren FTP, SFTP, Salesforce, Workday en andere connectoren die gebruikersrecords, roltoewijzingen en cursusvoltooiing importeren en platformgegevens exporteren naar externe systemen.
* Integratiebeheerders configureren webhooks die realtime ALM-gebeurtenisgegevens (inschrijvingen, voltooide bewerkingen, rolwijzigingen) naar externe URL&#39;s verzenden. Een gecompromitteerd of onjuist gevormd webhook eindpunt is een risico van de gegevensextractie.
* Integratiebeheerders kunnen LTI-integraties configureren. Als deze optie eenmaal is ingeschakeld, kan LTI niet worden uitgeschakeld.

**Verwijzingen**:

* [Aangepaste rollen | Adobe Learning Manager](https://experienceleague.adobe.com/nl/docs/learning-manager/using/admin/custom-role)
* [Aangepaste rollen beheren via CSV | Adobe Learning Manager](https://experienceleague.adobe.com/nl/docs/learning-manager/using/integration/configure-role-csv-files)
* [ Handleiding voor ontwikkelaars van toepassingen | Adobe Learning Manager ][ https://experienceleague.adobe.com/nl/docs/learning-manager/using/integration/developer-manual ]
* [Adobe Learning Manager-connectoren](https://experienceleague.adobe.com/nl/docs/learning-manager/using/integration/connectors)

+++

+++Wat zijn de geadviseerde veilige gebreken voor hoogste administratieve en bevoorrechte rekeningen in Adobe Learning Manager, en waar worden zij gevormd?

Adobe Learning Manager-documenten bieden specifieke aanbevolen beveiligde standaardinstellingen voor zowel de beheerdersrol als de geprivilegieerde accounttypen.

* **top-level de rekeningsgebreken van de Beheerder (die bij eerste levering worden gevormd)**:

* Aanmeldingsmethode voor interne gebruikers: Single Sign-On (SSO) via SAML 2.0: geconfigureerd op ALM-beheerder > Instellingen > Aanmeldingsmethoden. Gebruik Adobe ID niet voor medewerkers of beheerders.
* Verificatie in twee stappen (2FA): afgedwongen voor alle gebruikers: geconfigureerd in Adobe Admin Console > Instellingen > Privacy en beveiliging > Verificatie-instellingen.
* Maximale sessieduur: 8 uur (of per organisatiebeleid): geconfigureerd op Adobe Admin Console > Instellingen > Privacy en beveiliging > Geavanceerde instellingen.
* Maximale inactieve tijd: 30 minuten (of per organisatiebeleid): dezelfde locatie als hierboven.
* Inactieve gebruiker automatisch verwijderen: Ingeschakeld met een door de organisatie gedefinieerde retentieperiode (bijvoorbeeld 90 dagen inactiviteit): ALM-beheerder > Instellingen > Algemeen.
* Vervaldatum van extern gebruikersprofiel: Stel dit in op elk extern profiel bij het maken: ALM-beheerder > Gebruikers > Extern. Geen onbepaalde externe profielen.
* Beperkingen voor IP-toegang: Beperk waar mogelijk tot goedgekeurde IP-bereiken: Admin Console > Instellingen > Geavanceerde instellingen.

**de rolgebreken van de Beheerder van de Douane (gevormd wanneer het creëren van elke rol)**:

* OAuth scope for registered applications: minimum required scope. Bied de beheerdersrol nooit lees- en schrijftoegang tenzij strikt noodzakelijk.
* Bereik aangepaste rol: beperkt tot specifieke gebruikersgroepen en specifieke catalogi. Maak geen aangepaste rollen met het bereik Alle gebruikers en Alle catalogi, tenzij de functie deze vereist.
* Instellingstoegang in aangepaste rollen: niet verlenen, tenzij de specifieke functie dit vereist, gezien het escalatierisico met bevoegdheden.

**standaardwaarden van de Beheerder van de Integratie**:

* API OAuth-bereik: selecteer het meest restrictieve bereik dat voldoet aan de vereisten van de integratie. Geef de beheerder geen lees- en schrijfrechten voor toepassingen die alleen studenten lezen.
* Verbindingsgegevens, LTI-referenties en webhook-URL&#39;s: behandelen als gevoelige geheimen — delen nooit via e-mail of toewijzen aan bronbesturing.

**Verwijzingen**:

* [Instellingen | Adobe Learning Manager](https://experienceleague.adobe.com/nl/docs/learning-manager/using/admin/custom-role)
* [Gebruikersverificatie en wachtwoorden beveiligen | Adobe Admin Console](https://helpx.adobe.com/nl/enterprise/using/authentication-settings.html)
* [Aangepaste rollen | Adobe Learning Manager](https://experienceleague.adobe.com/nl/docs/learning-manager/using/admin/custom-role)

+++

+++Biedt Adobe Learning Manager beheerders een manier om de huidige accountinstellingen te vergelijken met de aanbevolen beveiligde standaardinstellingen?

Adobe Learning Manager heeft geen speciaal vergelijkingsdashboard dat automatisch naast de aanbevolen beveiligde standaardinstellingen de huidige instellingen toont.

**Rapport van de Rol van de Douane: huidige bevoorrechte roltoewijzingen**:

* Navigeer in ALM naar Beheer > Gebruikers > Aangepaste rollen en klik op Downloaden (rechtsboven) om een CSV te exporteren van alle aangepaste rollen, hun machtigingensets en hun bereiktoewijzingen.
* Vergelijk deze export met de aanbevolen standaardinstellingen in FRR-RSC-02 Section 8 — waarbij u specifiek controleert of een aangepaste rol Settings-toegang, het bereik Alle gebruikers of het bereik Alle catalogi heeft zonder gedocumenteerde uitvulling.

**ALM REST API: programmatic configuratiereeks**:

* Het GET /account-eindpunt retourneert configuratiegegevens op accountniveau in JSON-indeling, toegankelijk via het OAuth-bereik van de beheerdersrol. De klanten kunnen dit eindpunt programmatically roepen en de reactie tegen een basislijn afschilderen die van de geadviseerde gebreken in FRR-RSC-02 Sectie 8 wordt afgeleid.
* Het GET /users eindpunt (met include=role filter) retourneert de huidige roltoewijzingen voor alle gebruikers, waardoor automatische detectie van onverwachte roltoewijzingen mogelijk is.

>[!NOTE]
>
>Adobe Learning Manager biedt geen native interface voor het naast elkaar vergelijken van afbeeldingen. Klanten die een geautomatiseerde controle op de naleving van de configuratie nodig hebben, moeten de ALM REST-API integreren met hun bestaande tools.

**Verwijzing**

* [Handleiding voor toepassingsontwikkelaars | Adobe Learning Manager](https://experienceleague.adobe.com/nl/docs/learning-manager/using/integration/developer-manual)

+++

+++Kunnen beheerders de huidige beveiligingsinstellingen en -configuraties vanuit Adobe Learning Manager exporteren in een machinaal leesbare indeling?

Adobe Learning Manager ondersteunt het exporteren van beveiligingsgerelateerde configuratiegegevens via verschillende mechanismen. Geen enkele export geeft een volledige momentopname van alle beveiligingsinstellingen tegelijk, maar de volgende exportbewerkingen beslaan samen het volledige bereik van voor de beveiliging relevante gegevens.

**ALM REST API: de uitvoer van JSON van huidige roltoewijzingen en rekeningsconfiguratie**:

* GET/account: retourneert instellingen op accountniveau in JSON, inclusief actieve aanmeldingsconfiguratiegegevens en accountmetagegevens.
* GET /users?include=role: retourneert alle gebruikers met hun momenteel toegewezen rollen in JSON.
* GET /userGroups — retourneert alle gebruikersgroepen en hun lidmaatschap, relevant voor de controle van het bereik van de aangepaste rol.
* Alle API-reacties zijn JSON (vnd.api+json). Verificatie gebruikt OAuth 2.0 met lees-/schrijfbereik van beheerdersrol.

**de uitvoer van CSV van de Rol van de Douane: huidige bevoorrechte roldefinities**:

* ALM-beheerder > Gebruikers > Aangepaste rollen > Downloaden exporteert een CSV van alle aangepaste roldefinities, hun machtigingencategorieën en bereiktoewijzingen.
* Deze export kan worden gebruikt als een machinaal leesbare momentopname van de huidige geprivilegieerde accountconfiguratie.
**

**Banen API: bulkgebruiker en rolgegevens**:

* De API voor ALM-taken ondersteunt het op aanvraag genereren van gebruikersrapporten (inclusief roltoewijzingen) in CSV-indeling. Deze kunnen worden gepland en verbruikt door externe compliance- of SIEM-tools.

**Verwijzing**

* [Handleiding voor toepassingsontwikkelaars | Adobe Learning Manager](https://experienceleague.adobe.com/nl/docs/learning-manager/using/integration/developer-manual)

+++

+++Biedt Adobe Learning Manager een API waarmee beveiligingsrelevante instellingen via programmacode kunnen worden weergegeven en aangepast?

Adobe Learning Manager biedt een volledige REST API v2 die programmatisch het bekijken en aanpassen van beveiligingsrelevante instellingen mogelijk maakt met OAuth 2.0-verificatie. Hieronder vindt u de specifieke API-mogelijkheden die relevant zijn voor beveiligingsinstellingen:

**authentificatie en werkingsgebied**:

* Toepassingen worden geregistreerd door de integratiebeheerder bij Integratiebeheerder > Toepassingen > Registreren. OAuth 2.0 Client ID en Secret worden uitgegeven per toepassing.
* Er zijn zes bereiken beschikbaar. Voor het beheer van beveiligingsinstellingen is lees- en schrijftoegang voor de beheerdersrol vereist. Hierdoor krijgt de toepassing dezelfde toegang als een volledige beheerder via de API.
* Toegangstokens worden verkregen via de standaard OAuth-verificatiecode of de workflow voor clientreferenties. Basis-URL: https://learningmanager.adobe.com/primeapi/v2/

**Gebruiker en rolbeheer via API**:

* GET/gebruikers: alle gebruikers en hun huidige rollen ophalen
* POST /gebruikers: programmatically voorziening nieuwe gebruikers
* PATCH /users/{id}: update gebruikersattributen met inbegrip van roltoewijzingen
* DELETE /users/{id}: een gebruikersaccount uitschakelen
* POST /users/{id}/purge: leegmaken een gebruiker en alle bijbehorende records definitief

Ophalen accountconfiguratie:

* GET/account: retourneert configuratie op accountniveau, inclusief accountinstellingsgegevens in JSON-indeling, inclusief velden zoals complianceLabelDefaultID, showComplianceLabel en custom_injections.

+++

+++Publiceert Adobe Learning Manager zijn veilige configuratiebegeleiding in een machine-leesbare formaat zoals OSCAL, JSON, of YAML?

Adobe Learning Manager publiceert momenteel de Secure Configuration Guide niet in een voor computers leesbare indeling. De begeleiding in [&#x200B; FRR-RSC-01 &#x200B;](/help/migrated/alm-administrative-lifecycle.md) en [&#x200B; FRR-RSC-02 &#x200B;](/help/migrated/alm-secure-administration-guide.md) wordt gepubliceerd als mens-leesbare documentatie op Adobe Experience League in HTML en downloadbare documentformaten.

Er is geen openbaar beschikbare OSCAL-componentdefinitie, YAML-basislijn of JSON-beleidsbestand waarmee de aanbevolen veilige standaardinstellingen voor Adobe Learning Manager worden gecodeerd.

Klanten die geautomatiseerde vergelijking van huidige montages tegen geadviseerde basislijnen nodig hebben zouden [&#x200B; ALM REST API &#x200B;](https://experienceleague.adobe.com/nl/docs/learning-manager/using/integration/developer-manual) moeten gebruiken om huidige configuratiegegevens in formaat terug te winnen JSON.

+++

+++Is de veilige Gids van de Configuratie van Adobe Learning Manager openbaar beschikbaar zonder een login of een speciale toegang te vereisen?

**wat openbaar beschikbaar** is:

* [&#x200B; FRR-RSC-01: Veilige Gids van het Beleid &#x200B;](/help/migrated/alm-administrative-lifecycle.md): volledige levenscyclusbegeleiding voor top-level administratieve rekeningen.
* [&#x200B; FRR-RSC-02: De administratieve Montages van de Veiligheid en Implicaties &#x200B;](/help/migrated/alm-secure-administration-guide.md): alle veiligheid-relevante montages, hun implicaties, en geadviseerde gebreken.
* FRR-RSC-03-10 (dit document) — Antwoorden van vragen en antwoorden op alle acht FedRAMP MOETEN aanbevelingen doen.

+++

+++Biedt Adobe Learning Manager versiebeheer en een releasegeschiedenis waarmee bureaus wijzigingen in beveiligingsrelevante instellingen en aanbevolen standaardinstellingen kunnen bijhouden?

Adobe Learning Manager houdt een openbaar beschikbare, gedetailleerde releasegeschiedenis bij voor elke productupdate. Beveiligingsrelevante wijzigingen in beheerinstellingen, verificatiemogelijkheden, API-eindpunten en functies voor rolbeheer worden in elke release gedocumenteerd.

**ALM de Nota&#39;s van de Versie: genummerde, cumulatieve veranderingshistorie**:

* Adobe publiceert genummerde opmerkingen bij elke Adobe Learning Manager-update (bijvoorbeeld Update 100, Update 99). Deze worden op Experience League gepubliceerd en documenteren alle nieuwe functies, wijzigingen in bestaande instellingen, API-toevoegingen en -verwijderingen, connectorwijzigingen en verouderde mogelijkheden.
* Elke releaseopmerking bevat een speciale sectie voor API-wijzigingen, met een overzicht van nieuwe eindpunten, gewijzigde reactievelden en afgekeurde toepassingen, die direct relevant zijn voor beveiligingsgerelateerde configuratiemogelijkheden.

**wat Nieuwe pagina&#39;s is: samenvattingen per-versieeigenschap**:

* Elke belangrijke release heeft een speciale &#39;Nieuwe functies&#39;-pagina met nieuwe, voor de beveiliging relevante functies met context. De opmerkingen bij de release bevatten bijvoorbeeld wijzigingen in de verwerking van aangepaste machtigingen voor rollen, de toevoeging van door CSV gemaakte zichtbaarheid van machtigingen voor aangepaste rollen en wijzigingen in API-snelheden.

**API Lijst van Afschrijvingen: gebiedend verslag van verwijderde API mogelijkheden** s:

* Adobe onderhoudt een speciale pagina voor API-implementaties met alle verouderde en verwijderde ALM API-eindpunten met de releaseversie waarin elke afschrijving plaatsvond.

**Verwijzingen**:

* [Opmerkingen bij de release van Adobe Learning Manager](https://experienceleague.adobe.com/nl/docs/learning-manager/using/introduction/release-notes)
* [Nieuwe functies in Adobe Learning Manager](https://experienceleague.adobe.com/nl/docs/learning-manager/using/introduction/whats-new-july-2024)
* [API-implementaties in Adobe Learning Manager](https://experienceleague.adobe.com/nl/docs/learning-manager/using/introduction/api-deprecations-list)

+++
