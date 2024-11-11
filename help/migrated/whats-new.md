---
description: Meer informatie over de nieuwe functies en verbeteringen in de november 2024-versie van Adobe Learning Manager
jcr-language: en_us
title: Overzicht van nieuwe functies
source-git-commit: bfe77d838340f94e072f9d7346576e3034a66a66
workflow-type: tm+mt
source-wordcount: '3133'
ht-degree: 2%

---

# Overzicht van nieuwe functies {#new-features-summary}

Meer informatie over de nieuwe functies en verbeteringen in de november 2024-versie van Adobe Learning Manager.

* **AI-gedreven Onderzoek:** combineert lexicaal en semantisch onderzoek naar slimmere, context-bewuste resultaten.
* **Webhooks**: Integreer met Webhooks om informatie in real time naar specifieke URLs te verzenden.
* **het Leren Interoperabiliteit van Hulpmiddelen (LTI)**: Steunt LTI voor interoperabiliteit met andere platforms LMS.
* **Geloofsintegratie**: beheer en deel externe badges via Credly.
* **verbeteringen van het dashboard van de Naleving**: Deel dashboards met andere beheerders en plaats standaard nalevingswidgets op studentenhomepages.
* **steun van de meertaligheid**: Creeer taal-specifieke instanties voor de modules van de Lesruimte en van de Virtuele Klaslokaal.
* **de rollen van de Douane**: Verbeterde controle over gebruikersrollen en toestemmingen.
* **Commentaar van de Voltooiing**: voeg commentaren toe wanneer het merken van studenten als volledig.
* **rapport van de Groep van de Gebruiker**: Beheer gebruikersgroepen met gedetailleerde rapporten.
* **Wachtlijstrapport**: Download de wachtlijst studentenlijst voor cursusinstanties.
* **de verhogingen van de Toegankelijkheid**: Steun voor alt tekst op mastheads en bedrijflogo&#39;s.
* **Steun voor Hindi**: De taalsteun van de interface voor Hindi.
* **de controle van de Rendabiliteit**: Blok sociale berichten die verboden woorden bevatten.
* **optimalisering van het E-mailmalplaatje**: Gecombineerde en geoptimaliseerde e-mailmalplaatjes voor instructeurtoewijzingen en zittingsannuleringen.
* **de voltooiingscriteria van de Teams van MS**: Vastgestelde minimumaanwezigheidstijd voor zittingen VILT.
* **Nieuwe migratiewerkschema&#39;s**: De veranderingen van de migratie omvatten voltooiingscriteria voor cursussen en modules en het migreren modules in omslagen.

## AI-gedreven zoekfunctie in Adobe Learning Manager

Adobe Learning Manager vernieuwt de manier waarop studenten naar cursussen of trainingen zoeken. Het introduceert een AI-gedreven zoekfunctie die lexicale en semantische zoekopdrachten combineert. Het zoeken is nu slimmer, omdat het zoekt naar specifieke termen en de context en bedoeling achter die termen begrijpt. De geavanceerde zoekopdracht begrijpt de betekenis van uw zoekopdracht en levert relevante resultaten op. Het geeft de belangrijkste focus van de zoekopdracht aan, zodat je de meest volledige set resultaten krijgt.

Verwijs dit artikel [ Geavanceerd Onderzoek ](/help/migrated/learners/feature-summary/advanced-search.md) voor meer informatie.

## Webhooks

Met Adobe Learning Manager kunt u integreren met Webhooks en realtime informatie, zoals cursusinschrijvingen, het maken van cursussen en andere informatie, naar een specifieke URL verzenden.

Met een webhook in ALM kan een entiteit automatisch gegevens naar een andere toepassing verzenden via HTTP. Zo kan een toepassing andere toepassingen informatie verschaffen zonder er voortdurend om te vragen. Als een gebruiker bijvoorbeeld een LMS-cursus (Learning Management System) voltooit, kan een webhook die informatie automatisch naar een ander platform verzenden, zoals een CRM- of rapportagetool. Webhooks worden vaak gebruikt in integraties om processen te automatiseren en de behoefte aan handmatige updates tussen systemen te verminderen. Stel webhooks in door een callback-URL op te geven waarnaar u de gegevens wilt verzenden.

Verwijs dit artikel [ Webhooks ](/help/migrated/integration-admin/feature-summary/webhooks.md) voor meer informatie.

## Interoperabiliteit leergereedschappen

Adobe Learning Manager ondersteunt nu LTI om de interoperabiliteit tussen Adobe Learning Manager en andere Learning Management Systems (LMS) te verbeteren.

### Wat is LTI?

LTI (Learning Tools Interoperability) is een standaard waarmee tools en contentproviders van derden verbinding kunnen maken met een LMS (Learning Management System). Gebruikers hebben rechtstreeks vanuit hun LMS toegang tot externe leerinhoud van externe inhoudsproviders zonder zich aan te melden bij of naar een ander LMS te navigeren.

LTI als toolprovider: met LTI als toolprovider kunnen externe systemen worden geïntegreerd met een LMS. Adobe Learning Manager fungeert als LTI Tool Provider, waardoor andere LMS-platforms rechtstreeks vanuit hun LMS toegang hebben tot cursussen, certificaten of leerpaden van de Adobe Learning Manager.

LTI als toolconsument: LTI als toolconsument staat LMS toe om externe tools te integreren via Learning Tools Interoperability (LTI). In dit scenario is LMS een consument van diensten die door externe instrumenten worden geleverd. Adobe Learning Manager fungeert als consument van een LTI-tool, waardoor het programma leermiddelen van derden kan integreren. Op deze manier kunnen Adobe Learning Manager-studenten cursussen, certificaten of leerpaden volgen met de tools van derden in de Adobe Learning Manager.

Verwijs dit artikel [ het Leren Interoperabiliteit van het Hulpmiddel ](/help/migrated/integration-admin/feature-summary/learning-tools-interoperability.md) voor meer informatie.

## Credly

Met behulp van Credly kan een beheerder in ALM studenten externe badges beheren en delen via verschillende social-mediakanalen.

### Wat is Credly?

Credly is een digitaal aanmeldingsplatform waarmee studenten en organisaties professionele prestaties kunnen verdienen, delen en verifiëren, zoals badges of certificeringen. Studenten kunnen badges beheren en delen via hun aanmeldingsprofiel op sociale media en andere plaatsen.

### Integreer Credly met Adobe Learning Manager

Voeg eerst de Credly-connector in Adobe Learning Manager (ALM) toe. Migreer vervolgens de bestaande badges van Credly om de continuïteit van de prestaties van de student te garanderen. Maak ten slotte in Adobe Learning Manager een vaardigheid om de ontwikkeling en herkenning van studenten te verbeteren.

Verwijs naar dit artikel [ Credly ](/help/migrated/integration-admin/feature-summary/credly-integration.md) voor meer informatie

## Nalevingsdashboard

In deze release kunnen beheerders nu het dashboard delen met andere beheerders, aangepaste beheerders en winkelmanagers, zodat ze direct toegang hebben tot de dashboards voor compliance. Ze kunnen nu de standaardcompatibiliteitswidget op de startpagina van de student instellen, zodat studenten hun nalevingsvereisten kunnen volgen. Verwijs naar dit artikel [ dashboard van de Naleving ](/help/migrated/administrators/feature-summary/reports.md#share-compliance-dashboard-with-admins-and-custom-admins) voor meer informatie.

## Ondersteuning voor meerdere talen

Met Adobe Learning Manager (ALM) kunnen auteurs nu taalspecifieke instanties maken met taalcodering voor klassikale en virtuele klassikale modules. Studenten hebben in hun voorkeurstaal toegang tot CR/VC-modules. Een auteur kan bijvoorbeeld een CR/VC-module maken met twee instanties: een in het Engels en een in het Frans. Studenten kunnen de instanties in hun voorkeurstaal selecteren.

Verwijs naar dit artikel [ Leerobjecten in verschillende scènes ](/help/migrated/authors/feature-summary/add-new-language-learning-objects.md#multi-language-support-for-crvc-instances-with-language-tagging) voor meer informatie toevoegen.

## Aangepaste rollen

Met aangepaste rollen kunnen beheerders specifieke rollen en verantwoordelijkheden voor verschillende gebruikersgroepen definiëren, zodat ze een beter beheer en een betere controle hebben. In deze versie verbetert ALM aangepaste rollen door gedetailleerdere controle over de volgende secties te bieden.

* Gebruikers
* Cursussen
* Leerpaden
* Certificeringen
* Taakhulpen
* Catalogi

Beheerders kunnen nauwkeurige machtigingen toewijzen op basis van gebruikersverantwoordelijkheden, zodat elke groep alleen toegang heeft tot relevante functies en inhoud. Deze verbeterde controles staan meer korrelig beheer van zeer belangrijke secties toe.

Login als beheerder en navigeer aan **[!UICONTROL Gebruikers]** > **[!UICONTROL de Rollen van de Douane]** om de Rollen van de Douane te creëren en te beheren.

Verwijs dit artikel [ de rollen van de Douane ](/help/migrated/administrators/feature-summary/custom-role.md) voor meer informatie.

## Opmerkingen bij voltooiing

Beheerders kunnen nu opmerkingen toevoegen wanneer studenten als voltooid worden gemarkeerd in cursussen, leerpaden of certificeringen. Beheerders kunnen tegelijkertijd opmerkingen toevoegen voor een of meerdere studenten en de opmerkingen verschijnen in het rapport ](/help/migrated/administrators/feature-summary/reports.md#learner-transcripts) Studenttranscripten.[

Verwijs dit artikel [ commentaren van de Voltooiing ](/help/migrated/administrators/feature-summary/courses.md#completion-comments) voor meer informatie.

## Rapport voor gebruikersgroep

Het nieuwe **[!UICONTROL Rapport van de Groep van de Gebruiker van Adobe Learning Manager]** helpt gebruikersgroepen beheren door zicht in groepen te verstrekken verlaten unmanaged wanneer beheerders verlaten. Beheerders kunnen tot de rapporten onder de **[!UICONTROL Gebruikers]** toegang hebben > **[!UICONTROL sectie van de Groep van de Gebruiker]**. Het biedt gedetailleerde informatie over elke groep, waaronder:

* Type gebruikersgroep
* Groepsnaam
* Beschrijving
* Gemaakt door (naam)
* Gemaakt door (e-mail)
* Gemaakt op (UTC-tijdzone)
* Aantal gebruikers

Verwijs dit artikel [ rapport van de gebruikersgroep ](/help/migrated/administrators/feature-summary/add-users-user-groups.md#user-group-report) voor meer informatie.

## Wachtlijstrapport

Het nieuwe **[!UICONTROL Wachtlijstrapport van Adobe Learning Manager]** staat beheerders toe om wachtlijst studentenlijst voor alle instanties van een cursus te downloaden. Beheerders en instructeurs kunnen tot dit rapport van de **[!UICONTROL sectie van de Wachtlijst]** op de **[!UICONTROL Cursus]** of **[!UICONTROL pagina van het Overzicht van de Zitting]** toegang hebben. Het wachtlijstrapport kan worden gedownload van de secties Beheer en Docent.

De volgende kolommen zijn beschikbaar in het rapport Wachtlijst:

* Cursusnaam
* Instantienaam
* Instantie-ID
* Instantiestatus
* Gebruikersnaam
* E-mail
* Unieke ID van gebruiker
* Datum ingeschreven (tijdzone UTC)
* Status
* Wachtlijstnummer
* Wachtlijstlimiet
* Plaatslimiet

Verwijs dit artikel [ Wachtlijst rapport ](/help/migrated/administrators/feature-summary/courses.md#waitlist-report) en [ rapport Wachtlijst ](/help/migrated/instructors/feature-summary/learners.md#waitlist-report) om rapport van Admin en de sectie van de Instructeur te downloaden.

## Toegankelijkheid op studentstartpagina

Adobe Learning Manager ondersteunt nu alt-tekst voor alle mastheads om de toegankelijkheid voor studenten te verbeteren. Zo kunnen studenten met speciale behoeften de alt-tekst lezen en de afbeelding begrijpen met behulp van schermlezers. U kunt meerdere talen selecteren en voor elke taal alternatieve tekst bieden. Voeg de alt-tekst toe in de desbetreffende talen. Zorg ervoor dat het bedrijfslogo in uw account ook alt-tekst met de bedrijfsnaam bevat.
Verwijs dit artikel [ Bekendmaking ](/help/migrated/administrators/feature-summary/announcements.md#masthead) voor meer informatie.

## Ondersteuning voor Hindi

Adobe Learning Manager introduceert nu Hindi als een van de interfacetalen van het platform en ondersteunt de groei van het platform in India. Ondersteuning voor native Hindi-luidsprekers zorgt ervoor dat alle functies, rapporten en de algemene gebruikerservaring volledig toegankelijk zijn voor de gebruikers.

Ga als volgt te werk om de interfacetaal te wijzigen:

1. Login als **[!UICONTROL Admin]**.
2. Ga naar **[!UICONTROL Montages van het Profiel]** > **[!UICONTROL Taal van de Interface]**.
3. Selecteer **[!UICONTROL Hindi]** als interfacetaal.


## Winstcontrole voor sociale berichten

Adobe Learning Manager blokkeert nu sociale berichten in de Learners-app die niet-toegestane woorden bevatten. Dit helpt dingen professioneel en conform te houden, vooral op gevoelige gebieden zoals gezondheidszorg.

## E-mailsjabloonoptimalisatie

### E-mailstudenten wanneer een docent is toegewezen

De bestaande e-mails **[!UICONTROL u zijn toegevoegd als de Details van de Sessie van de Instructeur]** en **[!UICONTROL VCProvider]** zijn gecombineerd in één e-mail **[!UICONTROL u als UserType]** bent toegevoegd. **[!UICONTROL UserType]** zal of **[!UICONTROL Instructeur]** of **[!UICONTROL Organisator]** zijn, gebaseerd op de rol van de gebruiker. Deze e-mails waren voorheen niet beschikbaar in de gebruikersinterface. Ze zijn nu gecombineerd in één e-mail en toegevoegd aan de gebruikersinterface. Beheerders kunnen tot dit malplaatje in de **[!UICONTROL E-mailMalplaatje]** sectie toegang hebben. Deze wordt standaard ingeschakeld voor alle nieuwe en bestaande accounts, maar beheerders kunnen deze functie in dezelfde sectie uitschakelen of inschakelen. Deze e-mail wordt verzonden wanneer een sessie wordt gemaakt en een docent wordt toegewezen, ongeacht of het gaat om sessies zoals Zoomen, Teams, Connect of andere services.

### Studenten e-mailen wanneer een sessie wordt geannuleerd

De docenten die uit een sessie zijn verwijderd, ontvangen nu alleen een e-mail over de annulering van de sessie. Eerder ontvingen ze zowel een annulerings- als een update-e-mail. Docenten die in een sessie blijven ontvangen een e-mail met een sessieupdate samen met een nieuwe uitnodiging voor de sessie.

## Voltooiingscriteria voor MS Teams

Studenten worden op dit moment als bijgewoond gemarkeerd, zelfs als ze gedurende een paar seconden deelnemen aan een VILT-sessie (Virtual Instructor-Led Training). Met deze release hebben we voltooiingscriteria voor Teams-modules geïntroduceerd om een nauwkeuriger aanwezigheid te garanderen. Auteurs kunnen nu een minimumtijd instellen dat studenten in een VILT-sessie moeten doorbrengen om hun aanwezigheid te kunnen tellen.

Dit is een back-endfunctie die standaard is uitgeschakeld. Neem contact op met uw CSM om deze functie in te schakelen.

## Migratiewijzigingen

De migratieworkflow bevat de volgende wijzigingen:

* Migreer modules naar specifieke mappen.
* Voltooiingscriteria voor modules toegevoegd.
* Voltooiingscriteria voor cursussen toegevoegd

### Wijzigingen in de migratie van modules

Wanneer u modules naar ALM migreert, worden deze standaard in de openbare map opgeslagen. In deze versie, voegden wij een nieuwe kolom genoemd `folder` in het [ module_version.csv ](assets/module_version.csv) dossier toe. Beheerders kunnen deze kolom gebruiken om de mapnaam op te geven voor de modules die na de migratie moeten worden gebruikt. Beheerders kunnen ook één module in meerdere mappen plaatsen door de mapnamen gescheiden door komma&#39;s weer te geven.

De mapkolom gebruikt het gegevenstype String en is een optionele kolom. Hieronder volgen de voorwaarden voor de mappenkolom:

* De mapnaam die u toevoegt, moet een bestaande inhoudsmap in het ALM-account zijn.
* De waarden moeten een door komma&#39;s gescheiden tekenreeks zijn.
* Als u een nieuwe mapnaam toevoegt voor een module die al in een andere map staat, wordt de toegewezen map niet overschreven of vervangen door de nieuwe waarde. De module wordt toegevoegd aan de nieuwe map en blijft ook beschikbaar in de bestaande map.
* Als de waarde leeg is, zal de omslag aan **[!UICONTROL Openbaar]** in gebreke blijven.

Verwijs [ module_version csv specificc ](assets/4-module_version.xlsx) dossier voor meer informatie.

### Wijzigingen in de migratie van modules - voltooiingscriteria

Beheerders kunnen de voltooiingscriteria voor de modules tijdens de moduleverigratie opgeven. In deze versie, hebben wij een nieuwe kolommen `completionCriteria`, `viewPercent` en `quizData` in [ module_version.csv ](assets/module_version.csv) toegevoegd.

Hier volgen de voorwaarden voor de nieuwe kolommen:

1. `completionCriteria`:

   * Het gegevenstype moet een tekenreekswaarde zijn en ondersteunde waarden zijn:
      * `LAUNCH_CONTENT`
      * `VIEW_PERCENT`
      * `QUIZ`
      * `MARK_COMPLETE`
   * Voeg alleen voltooiingscriteria op moduleniveau toe voor moduletypen op eigen tempo.
   * De ondersteunde waarden voor statische inhoud zijn `LAUNCH_CONTENT` en `VIEW_PERCENT` .
   * De ondersteunde waarden voor interactieve inhoud zijn `LAUNCH_CONTENT` , `VIEW_PERCENT` en `QUIZ` .
   * De ondersteunde waarden voor HTML5-inhoud zijn `LAUNCH_CONTENT` en `MARK_COMPLETE` .

2. `viewPercent`:

   * Het gegevenstype voor deze kolom moet een geheel getal zijn en de waarde moet tussen 0 en 100 liggen.
   * Wanneer de completionCriteria aan `VIEW_PERCENT` wordt geplaatst, ga het vereiste meningspercentage in deze kolom in of verlaat het leeg.

3. `quizData`:

   * Het gegevenstype moet een tekenreekswaarde zijn en de ondersteunde waarden zijn `QUIZ_ATTEMPTED` , `QUIZ_PASSED` en `QUIZPASSED_OR_LIMITREACHED` .
   * Als `completionCriteria` is ingesteld op `QUIZ` , voert u de desbetreffende quizwaarde in de kolom `quizData` in.

Verwijs [ module_version csv specificc ](assets/4-module_version.xlsx) dossier voor meer informatie.

### Wijzigingen in cursusmigratie - Voltooiingscriteria

Beheerders kunnen de voltooiingscriteria voor de cursussen tijdens de cursusmigratie opgeven. In deze versie, hebben wij een nieuwe kolom toegevoegd genoemd `completionCriteria` in [ course.csv ](assets/course.csv).

Hier volgen de voorwaarden voor de kolom `completionCriteria` :

* Het gegevenstype moet een tekenreeks of getal zijn en het is een optioneel veld.
* De waarden moeten `ALL`, `X` en `SELECTEDMODULES` zijn.
* X is een geheel getal dat groter dan 0 en kleiner dan het totale aantal modules moet zijn.
* Als u `completionCriteria` aan `SELECTEDMODULES` plaatst, moet u de verplichte modules in het {](assets/course_module.csv) dossier 2} course_module.csv merken.[
* Typ `TRUE` of `FALSE` in de kolom `optionalCriteria` . Als u de waarde instelt als `TRUE` , wordt de module verplicht.

Verwijs [ cursus csv spec ](assets/3-course.xlsx) en [ course_module csv spec ](assets/6-course_module.xlsx) dossier voor meer informatie.

## API-wijzigingen

Hieronder vindt u de API-wijzigingen:

* **Onderzoek API**:
   * Filter in nieuwe modus met opties: klassiek zoeken en geavanceerde zoekmogelijkheden.
   * Nieuwe loMetadata-optie voor snippetTypes.
* **Aankondiging API**:
   * Omvat het altText-kenmerk voor mastheadbeschrijvingen.
* **Instantie APIs**:
   * Nieuw kenmerk voor landinstelling om de details van de landinstelling op te halen.
* **Controle van de Winst**:
   * Bijgewerkte API&#39;s om te controleren op verboden woorden in opmerkingen en reacties op sociale berichten:
* **RPM en de Beperking van de Brandwond**:
   * Toegevoegde RPM (verzoeken per minuut) en burst-limieten voor alle API&#39;s.
* **Badge APIs**:
   * Nieuw kenmerk externalProvider om informatie over externe badges op te halen.
* **Baan API**:
   * Download het rapport Gebruikersgroep en het controlerapport Aangepaste rol met behulp van de taak-API.

### Wijzigingen in zoekAPI

De API voor zoeken heeft nu een nieuw modusfilter met twee opties: `classicSearch` en `advanceSearch` . Er is ook een nieuwe optie `loMetadata` voor `snippetTypes` . Voor de beste resultaten neemt u `loMetadata` op in `snippetTypes` wanneer u de `advanceSearch` -modus gebruikt.

### Wijzigingen in aankondigings-API

Het `GET /announcements API` bevat nu het `altText` -kenmerk voor het opgeven van de mastheadbeschrijving.

#### Voorbeeldverzoek met cURL:

```
curl -X GET --header 'Accept: application/vnd.api+json' --header 'Authorization: oauth 12345678' 'https://abcd.adobe.com/primeapi/v2/announcements/123456'
```

#### Monsterreactie:

```
{
  "links": {
    "self": "https://abcd.adobe.com/primeapi/v2/announcements/123456"
  },
  "data": {
    "id": "12345",
    "type": "adminAnnouncement",
    "attributes": {
      "actionUrl": "google.com",
      "announcementType": "MASTHEAD",
      "expiryDate": "2038-01-19T03:14:07.000Z",
      "liveDate": "2024-07-31T11:11:30.000Z",
      "contentMetaData": [
        {
          "contentType": "IMAGE",
          "contentUrl": "https://abcd.adobe.com",
          "locale": "en-US",
          "altText": "Moonlight - english changed new",
          "thumbnailUrl": "https://abcd.adobe.com/"
        },      ]
    }
  }
}
```

### Wijzigingen in instantie-API&#39;s

Het nieuwe `locale` -kenmerk is toegevoegd aan de volgende API&#39;s om de locatiedetails op te halen.

* `GET /learningObjects/{loId}/instances/{loInstanceId}`
* `GET /learningObjects/{id}?include=instances,enrollment.loInstance`
* `GET /learningObjects?include=instances,enrollment.loInstance`
* `GET /learningObjects/{id}/relatedLOs?include=instances,enrollment.loInstance`
* `POST /learningObjects/query?include=instances,enrollment.loInstance`
* `POST /search/query?include=model.instances`
* `GET /search?include=model.instances`

#### Voorbeeldverzoek met cURL:

```
curl --location 'http://abcd.com/primeapi/v2/learningObjects/course:1234567/instances/course:1234567_1234567' \
```

#### Voorbeeldverzoek:

```
{
    "links": {
        "self": "http://abcd.com/primeapi/v2/learningObjects/course:1234567/instances/course:1234567_1234567"
    },
    "data": {
        "id": "course:1234567_1234567",
        "type": "learningObjectInstance",
        "attributes": {
            "dateCreated": "2024-02-27T09:21:25.000Z",
            "isAET": false,
            "isDefault": true,
            "isFlexible": false,
            "locale": "en-US",
            "state": "Active",
            "localizedMetadata": [
                {
                    "locale": "en-US",
                    "name": "Default instance"
                }
            ]
        },
        "relationships": {
            "learningObject": {
                "data": {
                    "id": "course:1234567",
                    "type": "learningObject"
                }
            },
            "loResources": {
                "data": [
                    {
                        "id": "course:123456_1234567_1234567_1",
                        "type": "learningObjectResource"
                    }
                ]
            }
        }
    }
}
```

### Openbare API-wijzigingen voor diepgaande controle

De volgende API&#39;s zijn bijgewerkt om diepgaande controles uit te voeren op opmerkingen en reacties op sociale berichten.

* `POST /boards/{id}/posts `
* `PATCH /posts/{id}`
* `POST /posts/{id}/comments`
* `PATCH /comments/{id}`
* `POST /comments/{id}/replies`
* `PATCH /replies/{id}`

Als er een beperkt woord in het bericht wordt gevonden, wordt de volgende reactie verzonden.

#### Monsterreactie:

```
{
  "status": "FORBIDDEN",
  "title": "BAD_WORD_FOUND",
  "source": {
    "info": "Unacceptable word found in post"
  }
}
```

### Wijzigingen in RPM en burstbeperking

In deze release zijn voor alle API&#39;s RPM (Requests per minuut) en burst-limieten toegevoegd. De maximale RPM voor elke API kan op de Swagger-pagina worden gecontroleerd.

RPM is het aantal verzoeken dat u in één minuut naar de API-server kunt verzenden. De burst limit staat een hoger aantal verzoeken voor een korte tijd toe, die verder gaan dan de gebruikelijke tarieflimiet. De `learningObject` API staat bijvoorbeeld maximaal 15 verzoeken per minuut toe. Als deze limiet wordt overschreden, retourneert de API een foutbericht.

### Wijzigingen in badge-API&#39;s

Het nieuwe kenmerk `externalProvider` is toegevoegd aan de volgende API&#39;s om informatie op te halen over externe badges, zoals de badge-id en de providernaam.

* `GET /badges `
* `GET /badges/{id}`
* `GET /skills?include=levels.badge`
* `GET /skills/{id}?include=levels.badge`
* `GET /learningObjects/{loId}/instances/{loInstanceId}?include=badge`
* `GET /users/{userId}/userBadges`
* `GET /users/{userId}/userBadges/{id}`

#### Voorbeeldverzoek met cURL:

```
curl -X GET --header 'Accept: application/vnd.api+json' --header 'Authorization: oauth 123456789' 'https://abcd.adobe.com/primeapi/v2/badges/44'
```

#### Monsterreactie:

```
{
  "links": {
    "self": "https://abcd.adobe.com/primeapi/v2/badges/44"
  },
  "data": {
    "id": "44",
    "type": "badge",
    "attributes": {
      "imageUrl": "https://abcd.com/accountassets/1/badges/download.png",
      "name": "external badge",
      "state": "Active",
      "externalProvider": {
        "id": "1234sjd-b272-4de1-9b60-1234567",
        "provider": "credly"
      }
    }
  }
}
```

### Download gebruikersgroep- en aangepaste rolcontrolerapporten via taak-API

De gebruiker kan het **[!UICONTROL Rapport van de Groep van de Gebruiker]** en **[!UICONTROL Rapport van de Controle van de Rol van de Douane downloaden]** gebruikend `Job API`.

#### Voorbeeldverzoek voor downloaden van rapport gebruikersgroep:

```
curl -X POST --header 'Content-Type: application/vnd.api+json;charset=UTF-8' --header 'Accept: application/vnd.api+json' --header 'Authorization: oauth 12345678' -d '{ \ 
     "data": { \ 
         "type": "job", \ 
         "attributes": { \ 
             "jobType": "generateUserGroupReport" \ 
         } \ 
    } \ 
 }' 'https://abcd.adobe.com/primeapi/v2/jobs'
```

#### Voorbeeld voor download van controlerapport voor aangepaste rol:

```
curl -X POST --header 'Content-Type: application/vnd.api+json;charset=UTF-8' --header 'Accept: application/vnd.api+json' --header 'Authorization: oauth 1234567' -d '{
    "data": {
        "type": "job",
        "attributes": {
            "description": "description of your choice",
            "jobType": "generateCustomRoleAuditReport",
            "payload":{
                 "fromDate": "2020-01-01T18:30:00.000Z",
                 "toDate": "2024-09-31T18:30:00.000Z",
                 "locale":  "en-US"
            }
        }
   }
}
```

### Foutberichten voor geen aanvraagtekst

We hebben specifieke foutberichten geïntroduceerd voor gevallen waarin de aanvraaginstantie verplicht is, maar niet in de API is opgenomen.

#### Voorbeeldfoutbericht:

```
{
    "status": "BAD_REQUEST",
    "title": "Generic Error"
}
```

## Verbeterde rapportage

Beheerders kunnen deze rapporteringsveranderingen in **Admin** > **sectie van Rapporten** vinden.

### Rapport over leertranscripten

Het **[!UICONTROL Lerende rapport van Transcripten]** zal twee nieuwe kolommen bevatten:

* **[!UICONTROL identiteitskaart van de Module]**: Toont het unieke herkenningsteken voor elke module. Deze nieuwe kolom is toegevoegd na de bestaande **[!UICONTROL kolom van de Module]**.
* **[!UICONTROL identiteitskaart van de Instantie van de Cursus]**: Toont het unieke herkenningsteken voor elke cursusinstantie.Deze nieuwe kolom is toegevoegd na de bestaande **[!UICONTROL kolom van de Instantie]**.
* **[!UICONTROL Commentaar van de Voltooiing]**: Deze kolom vangt de commentaren die door admin zijn ingegaan wanneer het merken van gebruikersvoltooiing. Deze nieuwe kolom is toegevoegd aan het einde van het rapport.


### Overzichtsrapport van de sessie

Het **[!UICONTROL Samenvatting van de Zitting]** rapport zal drie nieuwe kolommen bevatten:

* ]**de kolom van identiteitskaart van de Module**[!UICONTROL  is toegevoegd vóór de **[!UICONTROL kolom van de Naam van de Zitting]**.
* ]**de kolom van identiteitskaart van de Zitting**[!UICONTROL  is toegevoegd vóór de **[!UICONTROL kolom van de Naam van de Zitting]**.
* ]**kolom van identiteitskaart van de Instantie van 0} Cursus is toegevoegd na de**[!UICONTROL  kolom van de Naam van de Instantie ]**.**[!UICONTROL 
* ]**de kolom van de Telling van 0} Voltooiing {is toegevoegd na de**[!UICONTROL  kolom van de Telling van de Inschrijving ]**.**[!UICONTROL 

## Bugfixes in deze update

* Oplossing voor de fout die optrad tijdens het uploaden van video&#39;s van de activiteitenmodule tijdens het verzenden van bestanden op Android- en iOS-apparaten.
* Het probleem met het openen van cursussen in de mobiele app is opgelost; de webversie werkt goed.
* Het probleem met het weergeven van taakhulpen en andere bronnen in Safari is opgelost.
* Probleem opgelost waarbij gebruikers geen taakhulpen konden downloaden naar de mobiele app.
* De fout in de documentatie voor de Patch User API is opgelost.
* Probleem verholpen waarbij organisatoren geen e-mailmeldingen ontvingen wanneer een sessie uit de cursus werd verwijderd.
* Probleem verholpen waarbij organisatoren geen e-mails ontvangen waarin een sessie wordt geannuleerd wanneer een module uit de cursus wordt verwijderd en opnieuw wordt gepubliceerd.
* Extra ondersteuning voor het opnemen van speciale tekens &quot;+&quot; en &quot;-&quot; in e-mailadressen tijdens het maken van externe gebruikers.
* Probleem verholpen waarbij de geïntegreerde rapportsynchronisatie van de Marketo-connector mislukt als het gebruikersvaardigheidsrapport dubbele aanhalingstekens bevat in de CSV-recordwaarde
* Het probleem waarbij het eindpunt van `/skills` de juiste status voor de beheerder-API retourneert, maar de student-API consistent onjuiste of in cache opgeslagen gegevens weergeeft, is opgelost.
* Probleem met Go1-onboarding voor gratis cursussen is opgelost als de Go1-connector niet is ingesteld voor het account.
* Probleem verholpen waarbij cursussen in het leerpad (LP) niet via migratie toegankelijk zijn als de student de LP al heeft voltooid.
* Probleem verholpen waarbij de incrementele user-CSV mislukt wanneer zowel de manager van de gebruiker als de manager op skip-niveau zijn ingesteld als SU (Super User) in plaats van als beheerder en niet zijn opgenomen in de CSV.
* Oplossing voor de bereikproblemen voor winkelmanagers in dashboardrapporten.
* Probleem opgelost waarbij xapi_iri niet werd verwijderd wanneer een conceptcursus werd verwijderd.
* Oplossing voor het probleem waarbij in bepaalde scenario&#39;s geen unieke LO-id kon worden toegevoegd.
* Probleem opgelost waarbij de eigenschap IsEmbeddable in het leerplan niet correct werd bijgewerkt in gedeelde leerplannen.
* Oplossing voor het probleem dat van invloed was op de totale weergave van leerpaden in de weergave Student.
* Probleem verholpen waarbij studenten zich via zelfregistratiekoppelingen kunnen registreren of aanmelden, zelfs nadat hun accounts zijn verwijderd.
* Het probleem waarbij `www` werd verwijderd tijdens het toevoegen van koppelingen in de cursusbeschrijving tijdens het maken van de cursus, is opgelost.
* Probleem verholpen waarbij het verbergen van gegevens en het downloaden van taakhulpen niet goed functioneert.
* Probleem opgelost waarbij Single Sign-On (SSO) niet functioneerde voor nieuwe gebruikers die via de zelfregistratielink met een IP-id zijn toegevoegd.
* Probleem verholpen waarbij berichtberichtgegevens niet worden opgehaald nadat een aankondiging is verwijderd.
* Probleem verholpen waarbij er onvoldoende zoekresultaten werden weergegeven wanneer gebruikers per e-mail werden gezocht.

## Systeemvereisten

De systeemvereisten van de mening [ Adobe Learning Manager ](/help/migrated/system-requirements.md).

## Eerdere releases van Adobe Learning Manager

* [Versie van juli 2024](/help/migrated/whats-new-july-2024.md)
* [Versie van maart 2024](/help/migrated/whats-new-march-2024.md)
