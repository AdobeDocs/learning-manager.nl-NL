---
title: Nieuwe functies in deze release (november 2022)
description: Meer informatie over de nieuwe functies en verbeteringen in Adobe Learning Manager
hidefromtoc: true
source-git-commit: 1da0911a4d0c2ae5cb01bbb2b7955675b0dfcdde
workflow-type: tm+mt
source-wordcount: '1994'
ht-degree: 77%

---

# Nieuwe functies in deze release (november 2022)

<!--
IN-PROGRESS

<https://helpx.adobe.com/learning-manager/whats-new-nov-2022.html>
-->

## Configuratie van meerdere SSO&#39;s

Adobe Learning Manager ondersteunt momenteel één aanmeldingsmethode voor interne gebruikers en één aanmeldingsmethode voor externe gebruikers. Dit zorgt voor beperkingen wanneer klanten hun medewerkers en eigen klanten en kanaalpartners in hetzelfde account hebben.

Adobe Learning Manager ondersteunt nu meerdere aanmeldingsmethoden via meerdere SSO-configuraties voor zowel interne als externe gebruikers, met de bedoeling om aanmelding bij het platform door meerdere typen gebruikersgroepen te ondersteunen.

Zie [Meerdere SSO-aanmeldingen](/help/migrated/administrators/feature-summary/multiple-sso-logins.md) voor meer informatie.

## Ondersteuning voor niet-aangemelde functie

De native Adobe Learning Manager-portal ondersteunt nu een niet-aangemelde modus voor toegang tot een trainingsportal.

Studenten kunnen de trainingssite nu verkennen en openen, verschillende beschikbare cursussen en content bekijken, en besluiten zich aan te melden om de cursussen te gebruiken.

Met deze functie is het gemakkelijker om een klantgerichte leerportal te maken waar studenten naar diverse cursussen kunnen zoeken zonder zich meteen aan te melden.

Zie [Niet-aangemelde ervaring voor studenten](/help/migrated/administrators/feature-summary/non-logged-in-experience-learners.md) voor meer informatie.

## Verbeteringen in de pagina met trainingsoverzicht

De pagina met het trainingsoverzicht heeft nu een vernieuwde gebruikersinterface, zodat de studenten een betere ervaring hebben tijdens het gebruik van een cursus.

Andere verbeteringen zijn:

* U kunt nu bladwijzers voor trainingen instellen.
* Aanbevelingen van gerelateerde cursussen.
* Informatie over leerpad(en) voor cursussen en leerpaden.
* Klikbare auteursnamen.
* Navigatiepad voor eenvoudiger navigeren.

## Verbeteringen in de pagina met trainingsoverzicht

De pagina met het trainingsoverzicht heeft nu een vernieuwde gebruikersinterface, zodat de studenten een betere ervaring hebben tijdens het gebruik van een cursus.

Andere verbeteringen zijn:

* U kunt nu bladwijzers voor trainingen instellen.
* Aanbevelingen van gerelateerde cursussen.
* Informatie over leerpad(en) voor cursussen en leerpaden.
* Klikbare auteursnamen.
* Navigatiepad voor eenvoudiger navigeren.

## Pagina met auteursprofiel

De pagina met auteursprofiel toont alle trainingen die een bepaalde auteur heeft gemaakt.

Studenten kunnen gemakkelijk auteurspecifieke informatie vinden, en alle trainingen die deze auteur heeft gemaakt.

## Trainingen die met een bladwijzer zijn gemarkeerd

Studenten kunnen een training opslaan (met behulp van de knop Opslaan) of een bladwijzer plaatsen vanaf de cursustegel of de overzichtspagina. Alle cursussen met bladwijzer zijn beschikbaar op de startpagina van de student.

## Speler aanpassen

In deze versie kunt u de Fluidic Player aanpassen aan de brandingsvereisten van een cursus.

U kunt verschillende instellingen en opties van de speler tonen en verbergen op basis van de contentvereisten, en controle aan studenten verlenen op basis van type content. U kunt deze wijziging toepassen voor zowel native als headless implementaties.

De verschillende opties die u kunt wijzigen:

* Inhoudsopgave in-/uitschakelen
* Opmerkingen
* Taal
* Snelheid
* Bijschrift
* Volume
* Besturingselementen voor afspelen

## Nabootsing van student en manager

Beheerders kunnen een nabootsingssessie starten waar ze zich kunnen aanmelden namens iedere gebruiker in hun account, in de rol van student en manager.

Zie [Nabootsing van student en manager](/help/migrated/administrators/feature-summary/impersonation-learner-manager.md) voor meer informatie.

## Verdere verbeteringen

### Controlelogboek van e-mails

Beheerders hebben nu toegang tot alle logboeken met e-mails die vanaf het systeem zijn verzonden via een controlespoorrapport voor e-mail.

Dit logboek legt alle gegevens vast in verband met e-mails die de afgelopen 30 dagen zijn verzonden, en wordt dagelijks vernieuwd. Daarnaast bevat het rapport informatie, bijvoorbeeld metadata over afleverstatus, afzender, ontvanger, onderwerp en content.

Download het rapport via Rapporten > Aangepaste rapporten > Excel-rapporten > E-mailrapport. Er verschijnt een melding waarmee u het rapport kunt downloaden.

Dit rapport bevat de volgende velden:

* Tijdstip waarop e-mail is geactiveerd (UTC-tijdzone)
* Tijdstip van laatste status gebeurtenis (UTC-tijdzone)
* Leveringsstatus
* E-mailadres ontvanger
* Gebruikers-id verzender
* Onderwerp van e-mail
* Entiteitstype
* Entiteitsnaam
* Entiteits-id

### Bericht voor studenten op de wachtlijst

Als een auteur een nieuwe instantie toevoegt, kan de auteur een e-mail activeren om studenten op de wachtlijst te berichten over andere instanties. De studenten krijgen een e-mail over de wijziging.

### E-mailsjablonen instantieniveau

U kunt e-mails aanpassen voor elke instantie van een training.

Wanneer de auteur of beheerder een nieuwe instantie mag toevoegen, kan de sjabloon voor een individuele instantie worden bewerkt.

Als een cursus bijvoorbeeld verschillende doelgroeptypen heeft, kunt u de e-mailsjabloon dienovereenkomstig wijzigen.

![e-mailsjablonen](assets/email-template.png)

De prioriteit van de sjabloon wordt hieronder weergegeven:

1. Sjabloon op instantieniveau
2. Sjabloon op trainingsniveau
3. Sjabloon op accountniveau

### Docent geeft commentaar bij het accepteren van ingeleverd werk

Docenten kunnen nu opmerkingen toevoegen terwijl ze het ingezonden werk door studenten accepteren. De student ontvangt een e-mailbericht en een in-appmelding (indien ingeschakeld) zodra het verzoek is goedgekeurd door de docent. De opmerkingen met betrekking tot het ingezonden werk worden voor de beheerder en de student weergegeven in de studenttranscripten.

### Verbeteringen op gebied van zoekopdrachten

De recente zoekgeschiedenis van een student verschijnt, zodat deze alle vorige zoekacties kan bekijken.

De zoekresultaten zijn nu consistent tussen al het formele en informele lesmateriaal (sociaal leren). De resultaten omvatten training, sociaal leren en matches van Inhoudsmarktplaats.

Het zoeken is gerichter en doelgerichter, waarbij u de zoekresultaten op drie plaatsen kunt bekijken: formeel leren, sociaal leren en Inhoudsmarktplaats.

![zoeken](assets/search-image.png)

#### Zoeken op basis van zinnen

In deze versie van Adobe Learning Manager hebben we Typeahead-zoeken vervangen door zoeken op basis van zinnen.

#### Recente zoekopdrachten

Een student kan hun recente zoekopdrachten alleen in de huidige sessie bekijken.

### Catalogus met gratis cursussen in de Inhoudsmarktplaats

Een kant-en-klare, uitgezochte, hoogwaardige, gratis catalogus met 50 gratis cursussen is nu verkrijgbaar op de Inhoudsmarktplaats voor studenten.

### Ondersteuning voor de Indonesische taal

Bahasa Indonesia is nu toegevoegd als interfacetaal in de apps voor student en manager.

### Verplicht veld Auteur

Tijdens het maken van een cursus is het veld Auteur verplicht.

### Wijzigingen in de Inhoudsmarktplaats

* Nieuw gemaakte proefaccounts bevatten een nieuwe catalogus voor 50 gratis cursussen in de Content Marketplace, die beschikbaar zijn voor gebruikers.
* Een student kan nu het aantal zoekresultaten zien en ingesloten koppelingen koppelen om over te gaan naar Content Marketplace.

### Mobile Immersive-wijzigingen

In deze release kunnen Mobile Immersive-webgebruikers de hieronder vermelde taken uitvoeren:

* Maken - Berichten peilen
* Bericht bewerken - alle typen, RTE
* E-commerce-workflow.
* Een voorvertoning van een module weergeven: studenten beschikken over de functie Modulevoorvertoning in Mobile Immersive. Door deze wijziging kunnen studenten een voorvertoning van de module bekijken voordat ze zich voor een cursus inschrijven.
* Kopieer een URL.
* Verwijder een bord.

### Zoomconnectorwijzigingen

Het JWT-app-type wordt in juni 2023 vervangen. We raden u aan om Server-to-Server OAuth- of OAuth-apps te maken om de functionaliteit van een JWT-app in uw account te vervangen.

### Rapport voor gamification

In deze release krijgt u toegang tot een rapport dat verschillende cursussen weergeeft waarin gamification is ingeschakeld.

### Taalvoorkeur importeren via CSV-bestand

Wanneer u een CSV importeert, bevat de CSV Interfacetaal, Inhoudstaal en Tijdzone als velden.

De beheerder kan het rapport ook exporteren en dit bevat dan dezelfde velden als hierboven.

* Taal van interface
* Inhoudstaal
* Tijdzone

Naast beheerders kunnen aangepaste beheerder dit rapport ook exporteren.

![taalrapport](assets/language-report.png)

#### Invloed op lokalisatie

* De kolomnamen kunnen niet worden gelokaliseerd en moeten blijven zoals ze zijn (Interface Language, Content Language, Timezone).
* De landinstellingen zijn hoofdlettergevoelig.
* Omdat er geen beperking geldt voor het invoeren van de landcode kunt u alleen de taalcode opgeven. Zo zijn zowel &quot;it_IT&quot; als &quot;it&quot; geldig.
* Als er vanwege een onjuiste landinstelling een verschil bestaat in het rapport, dan gaat de verwerking van het CSV-bestand gewoon door en dit heeft geen invloed op de andere gegevens in het CSV-bestand. De voorkeurslandinstelling van de gebruiker met een onjuiste landinstelling wordt niet bijgewerkt. De overige gegevens worden wel bijgewerkt.

## API-veranderingen en verbeteringen

### VC-connectoren

Als een e-mail-ID van een beheerder wordt gebruikt om de VC-connector te configureren, moet deze beheerder toestemming hebben voor het volgende:

* Een bijeenkomst maken
* Bijeenkomst updaten
* Aanwezigheidsrapport ophalen

Tijdens het maken of bijwerken van de VC-vergadering moeten docenten de vergadering beëindigen binnen 30 minuten na de geplande eindtijd van de vergadering.

### Bladwijzers plaatsen

De volgende API&#39;s zijn toegevoegd om een bladwijzer te plaatsen bij een cursus op de pagina met trainingsoverzicht:

* Alle bladwijzers ophalen: `primeapi/v2/bookmarks`
* Een bladwijzer maken: `primeapi/v2/learningObjects/{id}/bookmark`
* Een bladwijzer verwijderen: `primeapi/v2/learningObjects/{id}/bookmark`

### Ondersteuning voor metadata en inhoud in meerdere locaties door migratie

Voor alle typen training die op het platform worden ondersteund (cursus, leerpaden, modules, certificaten en taakhulpen), wordt migratie naar meerdere talen nu ondersteund via CSV-bestanden met extra kolommen voor extra talen.

#### Vereisten

Maak het migratieproject als integratiebeheerder en deel de migrationProjectId met het ALM-ondersteuningsteam, zodat de markering voor meerdere landinstellingen kan worden ingeschakeld vanaf de back-end.

#### Bereik van migratieobjecten met meerdere landinstellingen

* Module
* Cursus
* Moduleversie
* Certificering
* Leerprogramma
* Taakhulp
* Versie taakhulp

#### CSV-specificatie

Learning Manager biedt u een set standaard CSV-specificaties voor migratie in meerdere landinstellngen. Het is verstandig om deze CSV-specificaties door te nemen voordat u het migratieproces start. De integratiebeheerder van uw organisatie kan de bestaande gegevensindelingen analyseren en toewijzen in overeenstemming met de CSV-sjabloonitems van Learning Manager.

#### Wijzigingen met ondersteuning voor meerdere landinstellingen

* De kolom module_version wordt niet ondersteund in module_version.csv en course_module.csv.
* Kan module_version niet bijwerken in dezelfde run (in dezelfde run kan de module niet worden gemigreerd met twee versies met dezelfde module).
* Update van inhoud of metadata wordt beschouwd als moduleversie-update van de module_version.csv.
* Kan geen update van job_Aid_Version via job_aid_version.csv ondersteunen

### Automatische tokens en cookies intrekken

Een headless LMS-applicatie ontvangt een refresh_token bij de eerste aanmelding. Daarna wordt de refresh_token gebruikt voor het genereren van een access_token voor de clientapplicaties om API-oproepen te doen. Zo wordt door het afspelen van content ook een oauth-eindpunt gebruikt om een cookie te genereren voor het beheer van afspelen, waarbij meerdere contentbestanden en API-aanroepen door bestanden die de cookie gebruiken, betrokken zijn. De cookie die door oauth wordt gegenereerd, heeft dezelfde geldigheid als de access_token, namelijk zeven dagen. Zodra de cookie is gegenereerd, kan deze niet meer worden gewist, in tegenstelling tot bij gebruikelijke webapplicatieafmelding. De Oauth-cookie en de webapplicatiecookie zijn twee verschillende cookies die geen interactie met elkaar hebben.

Voor het wissen van de cookie hebben we dus een nieuw eindpunt geïntroduceerd dat de refresh_token, cookie en zowel cookie als refresh token herroept.

**Details**

**Eindpunt**

`POST oauth/o/revoke`

**Query-parameters**

* `cookie=true|false` - geeft aan dat cookie moet worden ingetrokken
* `refresh_token=true|false` - hiermee wordt aangegeven dat vernieuwen

**Verzoek om body**

Hoofdtekst vereist voor herroepen van refresh_token of (refresh_token en cookie)

```
{
      "client_id": <>,
      "client_secret": <>,
      "refresh_token": <>
}
Body required for revoking oauth cookie only
{
      "access_token": <>
}
```

### Openbaar gemaakte API&#39;s

In deze release hebben we een paar API&#39;s publiek gemaakt.

| API | Type | Beschrijving |
|---|---|---|
| /social/search | GET | Zoek in social media. |
| /aankondigingen | GET | Krijg gedetailleerde informatie over de aankondiging op de masthead die aan de student is toegewezen. |
| /aankondigingen/`{id}` | GET | Krijg gedetailleerde informatie over de aankondiging op de masthead die aan de student is toegewezen. |
| /learningObjects/`{id}`/loResources/{loResourcesId} | GET | Upload url van het bestand voor loResource van resourceType &#39;Activity&#39; waarbij het bestand moet worden ingediend. |
| /jobAid/`{jobAidId}`/jobAidDownloaded | GET | Downloadrapport voor taakhulp instellen. |
| /bulkimport/startrun | POST | Voer bulkimport uit. |
| /bulkimport/cansync | GET | Synchroniseer bulkimport. |
| /search | GET | DELETEMEBOB |
| /uploadInfo | GET | Verwante informatie over contentupdate ophalen. |
| /uploadSigner | GET | Ontvang de handtekening van de te_ondertekenen inhoud. |
| /avatar | POST | Hiermee wordt de avatar-afbeelding van de student bijgewerkt met een nieuwe afbeelding. |
| /avatar | DELETE | Verwijdert de avatar-afbeelding van de student. |

### Salesforce-app

De **LO voor hogere volgorde negeren** moet zijn ingeschakeld in de Salesforce-app, zodat alle cursussen, leerprogramma&#39;s en certificaten tegelijkertijd kunnen worden weergegeven.

### API&#39;s voor aanpassing van speler

In deze release zijn API&#39;s opgenomen waarmee u een speler kunt aanpassen. U kunt:

* De speler starten of laden.
* Naar een bepaalde module navigeren.
* De inhoudsopgave in- en uitschakelen.
* De taal kiezen.
* De speler sluiten.
* Afspelen, pauzeren, vooruitspringen, achteruitspringen, zoeken, volume wijzigen of snelheid wijzigen.
* Gebeurtenissen vastleggen die afkomstig zijn uit de speler.

### De wachtlijstpositie van een student weergeven

Met de API GET /enrollments/{id}/waitlistPosition bij de LO-API wordt de wachtlijstpositie van een gebruiker opgehaald voor een opgegeven inschrijving.

### Verzending van voltooiingsdatum in externe certificeringen

De API /primeapi/v2/learningObjects/certification:xxxxx bevat het attribuut &quot;completionDateSameAsApprovalDate&quot; waarmee wordt aangegeven of voor de certificering &quot;Voltooiingsdatum van certificering&quot; is ingeschakeld voor de student, samen met de vlag waar/niet waar.

### LO-voorbeeldgegevens ophalen

De GET /preview/learningObjects/{id} API wordt toegevoegd om voorvertoningsinformatie over een leerobject op te halen.

### Externe gebruikers verplaatsen binnen profielen

De `PUT primeapi/v2/externalProfiles/{currentep}/users/{userid}?` call helpt een gebruiker naar een ander extern profiel verplaatsen door een nieuwe externalProfile ID te specificeren.

### Gebruikers toevoegen aan externe profielen

De `POST /externalProfiles/{id}/users` voegt externe gebruikers toe aan een extern profiel.

## Aanvullende informatie

Voor informatie over de huidige en vorige releases van de webapp en de apparaatapp van Learning Manager raadpleegt u de [Opmerkingen bij de release](/help/migrated/release-note/release-notes.md).

## Foutoplossingen

Als u de fouten wilt zien die in deze update zijn gecorrigeerd, raadpleegt u de [Grenzen van lijst](release-note/release-notes.md#bugs-fixed-in-this-release).

## Systeemvereisten

[Learning Manager-systeemvereisten](/help/migrated/system-requirements.md)
