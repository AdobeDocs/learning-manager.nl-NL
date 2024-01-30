---
description: Dit document biedt een aanbevolen aanpak voor organisaties om Adobe Learning Manager op te zetten en te configureren. Het Learning Manager-team stelt voor om met een gefaseerde aanpak aan de slag te gaan met de toepassing. Het is niet verplicht om alle fasen in een bepaalde volgorde te volgen.
jcr-language: en_us
title: Gids met beste praktijken voor het opzetten van Learning Manager
contentowner: jayakarr
preview: true
source-git-commit: 46afb6603456ced9d7e2aaf98d07ec92fee30c0b
workflow-type: tm+mt
source-wordcount: '3387'
ht-degree: 71%

---



# Gids met beste praktijken voor het opzetten van Learning Manager

Dit document biedt een aanbevolen aanpak voor organisaties om Adobe Learning Manager op te zetten en te configureren. Het Learning Manager-team stelt voor om met een gefaseerde aanpak aan de slag te gaan met de toepassing. Het is niet verplicht om alle fasen in een bepaalde volgorde te volgen.

Deze fasen kunnen worden uitgevoerd door drie verschillende rollen, door een of meer personen op basis van uw organisatie-instelling. De drie rollen zijn als volgt:

1. **IT-beheerder** - De IT-beheerder voert activerings- of integratiegerelateerde activiteiten uit die verband houden met de toepassing van Learning Manager in een organisatie. De IT-beheerder kan ook enkele of meerdere gebruikers toevoegen en de rol van integratiebeheerder vervullen.
1. **Auteur** - De auteur maakt leerinhoud die nodig is voor de leerbehoeften van de organisatie. Auteurs van trainings- of leerinhoud van uw organisatie kunnen beginnen met het maken van de basisinhoud die nodig is voor de toepassing van de Learning Manager.
1. **Beheerder van Learning Manager** - De beheerder van de Leerbeheertoepassing voert configuratie- en instellingsactiviteiten uit. Bij sommige bedrijven kan de IT-beheerder ook de rol van Learning Manager-toepassingbeheerder op zich nemen.

U kunt de onderstaande infographic bekijken om een overzicht te krijgen van de fasen en bijbehorende taken.

![](assets/learning-manager-getting-started.jpg)

In dit stadium gaan we ervan uit dat uw organisatie de licentiesleutel al heeft ontvangen en dat u het Learning Manager-account hebt geactiveerd. Zoals vermeld in de infographic worden de drie sporen als volgt uitgelegd:

## Fase 1 - Technische installatie (IT-beheerder) {#phase1technicalsetupitadministrator}

In Track 1 kan de IT-beheerder van uw organisatie overschakelen op de rol van integratiebeheerder in de toepassing Learning Manager en enkele activeringen en integraties als volgt uitvoeren:

### Actieve velden inschakelen/toevoegen (Learning Manager-beheerder) {#enableaddactivefieldscaptivateprimeadministrator}

Naast de actieve velden die gebruikers tijdens de registratie opgeven, kan de beheerder meer actieve velden toevoegen. De beheerder kan ook de gebruikersvelden in- en uitschakelen. De waarden voor deze actieve velden worden gegenereerd uit de metagegevens van verschillende gegevensbronnen die bij gebruikersaccounts horen. Raadpleeg [Help bij actieve velden](feature-summary/add-users-user-groups.md#active-fields) voor meer informatie.

### Single Sign-On (SSO) {#singlesignonsso}

U kunt de Learning Manager-toepassing openen met behulp van Adobe ID of eenmalige aanmelding. Eenmalige aanmelding is een mechanisme waarmee een gebruiker zich eenmalig kan authenticeren om meerdere keren toegang te krijgen tot meerdere toepassingen. Deze configuratie is niet verplicht voor de organisatie. Als uw organisatie een SAML 2.0 gebaseerde SSO-provider heeft, kunt u deze gebruiken om de Learning Manager-toepassing te configureren. De configuratie is vereist op organisatieniveau en op Learning Manager-niveau. Kiest u voor SSO, neem dan contact op met de Adobe-ondersteuning voor configuratie-instructies. Raadpleeg [Help bij Instellingen](feature-summary/settings.md) voor meer informatie.

### Gebruikers in bulk importeren {#bulkimportofusers}

Wanneer u veel gebruikers in uw organisatie hebt, kunt u alle gebruikers in bulk importeren in de Learning Manager-toepassing, met behulp van een .CSV-bestand. Voordat u deze taak uitvoert, raden we u aan de lijst met gebruikers uit de HR-toepassing van uw organisatie te exporteren in een CSV-indeling. Ook als u de gebruikers in dit stadium niet in grote hoeveelheden importeert, kunt u zich vertrouwd maken met het CSV-formaat. Om te beginnen met het importproces in Learning Manager, uploadt u het CSV-bestand en wijst u de toepassingsgegevensvelden toe aan de CSV-kolommen van uw organisatie. Raadpleeg [Help voor bulkimport](add-users-in-bulk.md) voor meer informatie.

### FTP-connectorintegratie {#ftpconnectorintegration}

Als u continu werknemers in uw organisatie moet toevoegen of verwijderen, kunt u ervoor kiezen om de bulkimport van gebruikers te automatiseren met behulp van de FTP-connector. U moet eerst een verbinding tot stand brengen, daarna kunt u een CSV uploaden en de kenmerken van de CSV aan de overeenkomstige Learning Manager-velden toewijzen. U kunt het automatische importproces plannen en het ook synchroniseren als en wanneer dat nodig is. Raadpleeg [Help bij FTP-connector](../integration-admin/feature-summary/connectors.md#ftpconnector) voor meer informatie.

### Integratie van Salesforce-connector {#salesforceconnectorintegration}

Als u binnen uw organisatie een Salesforce-account in hebt, kunt u het proces waarbij alle gebruikers van Salesforce in de Learning Manager-toepassing worden geïmporteerd, automatiseren. Als u deze functie wilt gebruiken, kunt u de Salesforce-connector gebruiken om Learning Manager met het Salesforce-account te integreren en de synchronisatie van gegevens te automatiseren. Gebruik de functie voor automatische planning om de automatische gebruikersimport regelmatig uit te voeren. U kunt ook dagelijks synchroniseren. Raadpleeg de [Help voor Salesforce-connector](../integration-admin/feature-summary/connectors.md#sfconnector) voor meer informatie.

### Adobe Connect-integratie {#adobeconnectintegration}

Als u binnen uw organisatie Adobe Connect gebruikt, kunt u het integreren met de Adobe Learning Manager-toepassing om een studenten een naadloze gebruikerservaring te bieden. De integratie stelt uw studenten in staat om met één klik toegang te krijgen tot virtuele klassen binnen de Learning Manager-toepassing, zonder zich opnieuw aan te melden bij Adobe Connect. Met behulp van deze functie kunnen uw studenten ook de opgenomen virtuele klassikale sessies binnen de Learning Manager-toepassing gebruiken. Integreer eerst de instellingen om te kunnen integreren. Gebruik **Instellingen > Adobe Connect > Nu configureren** om Connect URL en aanmeldingsgegevens op te geven en te integreren. Raadpleeg de [Help voor Adobe Connect-integratie](feature-summary/adobeconnect-integration.md) voor meer informatie.

### Registratie via Salesforce-app {#salesforceappregistration}

Uw studenten kunnen binnen hun Salesforce-account naadloos toegang krijgen tot de Learning Manager-app. Studenten binnen de Salesforce-toepassing toegang tot de leerinhoud die aan hen is toegewezen, zoals cursussen, leerprogramma&#39;s, taakhulpen, en dergelijke. Gebruikers hebben binnen Salesforce ook toegang tot meldingen en aankondigingen van de Learning Manager-app. Om deze functionaliteit te kunnen gebruiken, moet u de Salesforce-toepassing in Learning Manager registreren. Raadpleeg de [Help voor Salesforce-app](../integration-admin/feature-summary/sfdc-app.md) voor meer informatie over de installatie- en gebruiksinstructies.

## Fase 2 - Configuratie van de locatie (Learning Manager-beheerder) {#phase2siteconfigurationcaptivateprimeadministrator}

De Learning Manager-toepassingbeheerder in uw organisatie moet een aantal van de functies configureren of instellen voordat u kunt beginnen met de implementatie ervan voor uw studenten.

### Branding {#branding}

Een organisatie kan het bedrijfslogo in de toepassing Learning Manager willen weergeven, een eigen domein in de URL hebben, de naam van de organisatie weergeven en kleurenschema&#39;s weergeven die overeenkomen met het merk van een organisatie. Learning Manager stelt organisaties in staat om al deze functies te gebruiken. Als u de instellingen wilt aanpassen en uw eigen branding wilt gebruiken, klik dan op het gedeelte Branding in het linkerdeelvenster. Klik op Bewerken naast al deze opties en pas deze aan uw wensen aan. Raadpleeg [Help voor Branding en thema&#39;s](feature-summary/themes.md) voor meer informatie.

### Gebruikers/gebruikersgroepen toevoegen {#addusersusergroups}

Aangezien studenten de hoofdgebruikers van uw leerinhoud zijn, is het toevoegen van gebruikers in het LMS de eerste stap. Voeg gebruikers toe aan de Learning Manager-toepassing en wijs rollen aan hen toe. U kunt op de volgende manieren gebruikers toevoegen:

#### Gebruikers toevoegen (intern) {#addusersinternal}

* **Als één enkele gebruiker** - Door afzonderlijke gebruikers toe te voegen aan Learning Manager-toepassing kunt u deze functie eerst met een aantal gebruikers uittesten voordat u ze in bulk toevoegt. Deze optie is ook handig wanneer u meer individuele gebruikers wilt toevoegen op basis van behoefte, na bulkimport van gebruikers.
* **Zelfregistratie** - Met deze optie kunnen beheerders hun werknemers toestaan zich te registreren bij Leermanager.
* **In bulk importeren** (met behulp van CSV-upload) - Met deze optie kunt u gebruikers in bulk importeren in de toepassing Learning Manager. U moet de gebruikerslijst altijd in CSV-indeling bij de hand houden voordat u deze functie kunt gebruiken.

#### Gebruikers toevoegen (externe profielen) {#addusersexternalprofiles}

* Via externe inschrijving - Met deze optie kunt u externe afdelingsleden of externe medewerkers van uw organisatie inschrijven voor de toepassing.

#### Gebruikersgroepen toevoegen {#addusergroups}

De Learning Manager-toepassing genereert standaardgebruikersgroepen op basis van vergelijkbare attributen. Naast de standaardgroepen kunt u aangepaste gebruikersgroepen genereren op basis van parameters zoals benoeming en locatie, zodat u deze groepen onder andere kunt gebruiken in voor Gamification en rapporten. Raadpleeg de [Help voor Gebruikers toevoegen](feature-summary/add-users-user-groups.md) voor meer informatie.

### Rollen toewijzen {#assignroles}

Nadat de gebruikers zijn toegevoegd aan Learning Manager, kan de beheerder beginnen met het toewijzen van auteurs-, beheerders- of integratiebeheerdersrollen aan de gebruikers volgens de vereisten van de organisatie. Als u rollen wilt toewijzen aan gebruikers, klikt u in de beheerdersaanmelding op **[!UICONTROL Gebruikers]**  in het linkerdeelvenster selecteert u het selectievakje naast elke gebruikersnaam en klikt u op **[!UICONTROL Handelingen]** de rol die u wilt toewijzen. Managerrollen worden aan gebruikers toegewezen door Adobe Learning Manager op basis van de rollen/privileges die door uw organisatie in het CSV-bestand worden vermeld. U kunt ook de rollen van gebruikers als managers wijzigen met behulp van de workflow Gebruikers bewerken. Raadpleeg de [Help voor Gebruikers toevoegen](feature-summary/add-users-user-groups.md) voor meer informatie.

### Meldingssjablonen {#notificationtemplates}

Meldingen kunnen nuttig zijn voor gebruikers in een LMS om te weten wat hun status is of om geïnformeerd te worden over de gebeurtenissen/activiteiten. Bij het maken van cursussen, het configureren van de functies of het gebruik van cursussen, doorlopen gebruikers verschillende gebeurtenissen waardoor meldingen voor de studenten, hun managers, beheerders of auteurs geactiveerd worden. Learning Manager biedt verschillende e-mailmeldingssjablonen in de toepassing. Als beheerder kunt u ze aanpassen volgens de vereisten van uw organisatie. Kies, om e-mailmeldingen aan te maken, in het linkerdeelvenster **E-mailsjablonen** en klik op de naam van het sjabloon. Raadpleeg de [Help voor E-mailsjablonen](feature-summary/email-templates.md) voor meer informatie

**E-mailmeldingen uitschakelen (aanbevolen)**

Meldingen zijn standaard ingeschakeld in de Learning Manager-toepassing. U kunt meldingen in dit stadium uitschakelen als u uw medewerkers niet op de hoogte wilt stellen van de organisatie.

### Badges {#badges}

Werknemers kunnen badges verdienen wanneer ze een cursus voltooien en deze laten zien hoe de werknemer presteert. Professionals wereldwijd gebruiken deze badges om te laten zien dat ze een bepaalde vaardigheid beheersen of een leerprestatie hebben behaald. U kunt een verzameling badges maken, zodat u ze na voltooiing van de leerinhoud aan de studenten kunt toewijzen. Om te beginnen met het maken van badges, kunt u op de functie **[!UICONTROL Badges]** in het linkerdeelvenster klikken. Raadpleeg  [Help voor Badges](feature-summary/badges.md) voor meer informatie.

### Feedback {#feedback}

Feedback is een van de belangrijke factoren in een LMS om de leervoortgang van studenten te meten en de kwaliteit van de leerinhoud te waarborgen. Learning Manager biedt twee soorten feedbackopties voor gebruikers.

* L1-feedback is de feedback die de studenten na afloop van de cursus geven.
* L3-feedback is de feedback die managers aan studenten geven op basis van de impact van de cursus op het gedrag en de dagelijkse activiteiten van de studenten.

Het is optioneel voor organisaties om deze functie te gebruiken. Beheerders kunnen de feedbacksjablonen aanpassen aan de eisen van hun organisatie. De beheerder moet de L1- en L3-feedbackopties op het niveau van de cursusinstantie inschakelen om deze functie te kunnen gebruiken. Kies een willekeurige cursus om de feedback te configureren, klik vervolgens op de standaardinstellingen voor de instantie in het linkerdeelvenster en schakel de feedbackoptie in. Raadpleeg de [Help voor Feedback](feature-summary/courses.md) voor meer informatie.

### Gamification {#gamification}

Een van de uitdagingen waar organisaties mee te maken hebben, is de studenten betrokken houden bij de inhoud. Gamification verhoogt het aantal studenten dat de cursus afrondt doordat ze door middel van gametechnieken worden gemotiveerd hun doelen te bereiken. Studenten kunnen met hun collega&#39;s wedijveren om punten te scoren voor verschillende leeractiviteiten en bronzen, zilveren, gouden en platina niveaus te behalen. Beheerders kunnen elke gamificationtaak in-/uitschakelen en de punttoewijzing per taak wijzigen. Learning Manager biedt de gamificationfunctie met enkele standaardinstellingen. U kunt de functie met de standaardinstellingen enige tijd gebruiken en daarna kunt u ervoor kiezen om de functie aan te passen. U hebt de mogelijkheid om de instellingen voor deze functie te configureren/wijzigen. Als er voor dit onderwerp een deskundige binnen uw organisatie is, adviseren wij u de instellingen te configureren voordat u deze gebruikt. Raadpleeg de [Help voor Gamification](feature-summary/gamification.md) voor meer informatie.

### Leerobjecten maken {#createlearningobjects}

Dit is de logische fase waarin alle drie de sporen (spoor 1, spoor 2 en spoor 3) samenkomen om de volgende stap te zetten.

Nadat u modules en cursussen hebt gemaakt, kunt u beginnen met het maken van leerobjecten van een hoger niveau, zoals certificeringen, leerprogramma&#39;s of taakhulpen, om verder te gaan. Voordat u van start gaat met het maken van leerobjecten moet u er zeker van zijn dat u al enkele gebruikers in de Learning Manager-toepassing hebt toegevoegd, en dat u enkele modules en cursussen hebt gemaakt.

#### Certificeringen maken {#createcertifications}

Certificering is het bewijs dat bepaalde leerinhoud is voltooid of het bewijs van een eenmalige of terugkerende prestatie van studenten. Het verstrekken van certificeringen na afloop van een cursus heeft een gunstige invloed op het aantal studenten dat zich inschrijft voor een bepaalde cursus. Als beheerder kunt u een certificeringsprogramma maken dat intern of door een derde partij wordt gehost. In het geval van een interne certificering, definieert u de cursussen die een student moet volgen om zich te laten certificeren. Controleer voordat u een certificering maakt dat er een aantal cursussen beschikbaar zijn in het account. Raadpleeg  [Help voor certificering](feature-summary/certifications.md) voor meer informatie over het maken van certificeringen.

#### Taakhulpen maken {#createjobaids}

Taakhulpen is een opslagplaats van trainingsinhoud die zonder enige inschrijvings- of voltooiingscriteria toegankelijk is voor studenten. Studenten kunnen deze taakhulpen gebruiken om hulp te krijgen bij het uitvoeren van een activiteit of taak in een organisatie. Ook al is het niet verplicht om taakhulpen te gebruiken als onderdeel van het maken van een cursus, het Learning Manager-team adviseert toch taakhulpen te maken als best practice voor uw organisatie. Raadpleeg de  [Help bij taakhulpen](../authors/feature-summary/job-aids.md) voor informatie over het maken van taakhulpen.

#### Leerprogramma’s maken {#createlearningprograms}

Leerprogramma&#39;s zijn een reeks uniek ontworpen cursussen die voldoen aan specifieke leerdoelen. Voordat u leerprogramma&#39;s maakt, moet u ervoor zorgen dat u al enkele cursussen hebt gemaakt of dat er bestaande cursussen beschikbaar zijn in uw account.  Hoewel het voor een organisatie optioneel is om deze functie te gebruiken, raadt het Learning Manager-team u aan deze functie te gebruiken om gericht leren voor uw werknemers op te nemen. Klik op Leerprogramma in het linkerdeelvenster om de leerprogramma&#39;s te gebruiken, kies vervolgens een reeks cursussen uit de catalogus en publiceer deze. Raadpleeg de [Help bij leerprogramma&#39;s](feature-summary/learning-programs.md) voor specifieke instructies.

### Catalogi maken {#createcatalogs}

U kunt binnen een organisatie catalogi gebruiken om gerichte inhoud te maken of om inhoud te classificeren voor een gedefinieerde groep studenten. In Learning Manager is een catalogus een verzameling van leerobjecten, zoals cursussen, certificeringen of leerprogramma&#39;s. U kunt leerobjecten naar keuze toevoegen aan uw catalogi. Zorg ervoor dat u al een reeks cursussen, certificeringen of leerprogramma&#39;s hebt gemaakt voordat u de catalogi aanmaakt. U kunt aangepaste catalogi maken met een set leerobjecten als u ze aan interne of externe gebruikersgroepen wilt toewijzen. Raadpleeg de  [Help Catalogi](feature-summary/catalogs.md) voor meer informatie over catalogi.

### E-mailmeldingen/gebruikerstoegang inschakelen {#turnonemailnotificationsuseraccess}

In dit stadium kunt u e-mailmeldingen voor de gebruikers van uw toepassingen inschakelen en ook gebruikerstoegang inschakelen.

## Fase 3 - Cursussen opstellen (Auteur) {#phase3authoringcoursesauthor}

Inhoudsontwikkelaars of -auteurs in uw organisatie kunnen beginnen met het maken van de leerinhoud. Het is verplicht om modules en cursussen te maken omdat deze de basis vormen voor al uw leerinhoud in de toepassing Leermanager.

### Modules maken {#createmodules}

Modules zijn de bouwstenen van de Learning Manager-toepassing. Start met het maken van modules als auteur om uw leerinhoud te organiseren. Met Learning Manager kunt u een van de vier soorten cursusmodules kiezen, zoals klassikale modules, modules op eigen tempo, activiteiten- en virtuele klassikale modules. Raadpleeg  [Help voor modules](../authors/how-to-choose-modules.md) om te weten te komen welk type cursusmodule het meest geschikt is voor de behoeften van uw organisatie.

### Cursussen maken {#createcourses}

Beheerders kunnen een auteursrol op zich nemen in de Learning Manager-toepassing en cursussen maken. In de Learning Manager-toepassing is een Cursus een basiseenheid met een set modules, die aan de student kan worden toegewezen. Studenten volgen cursussen. U kunt beginnen met het maken van cursussen door de modules te kiezen die u eerder hebt gemaakt, er vaardigheden aan koppelen waarvan u wenst dat de studenten ze beheersen na voltooiing van de cursus, niveaus, punten en badges aan een cursus koppelen, taakhulpen, voorwaarden en leermiddelen selecteren op basis van uw keuze en vervolgens de cursus publiceren. U kunt ook meerdere instanties van een cursus aanmaken zodat u de cursusinstanties kunt toewijzen aan meerdere studenten in verschillende tijdzones, schema&#39;s en dergelijke. Raadpleeg de  [Help Cursussen](../authors/feature-summary/courses.md)voor meer informatie over het maken van een cursus.

### Leerobjecten maken {#Createlearningobjects-1}

Dit is de logische fase waarin alle drie de sporen (spoor 1, spoor 2 en spoor 3) samenkomen om de volgende stap te zetten.

Nadat u modules en cursussen hebt gemaakt, kunt u beginnen met het maken van leerobjecten van een hoger niveau, zoals certificeringen, leerprogramma&#39;s of taakhulpen, om verder te gaan. Voordat u van start gaat met het maken van leerobjecten moet u er zeker van zijn dat u al enkele gebruikers in de Learning Manager-toepassing hebt toegevoegd, en dat u een aantal modules en cursussen hebt gemaakt.

#### Certificeringen maken {#Createcertifications-1}

Certificering is het bewijs dat bepaalde leerinhoud is voltooid of het bewijs van een eenmalige of terugkerende prestatie van studenten. Het verstrekken van certificeringen na afloop van een cursus heeft een gunstige invloed op het aantal studenten dat zich inschrijft voor een bepaalde cursus. Als beheerder kunt u een certificeringsprogramma maken dat intern of door een derde partij wordt gehost. In het geval van een interne certificering, definieert u de cursussen die een student moet volgen om zich te laten certificeren. Controleer voordat u een certificering maakt dat er een aantal cursussen beschikbaar zijn in het account. Raadpleeg  [Help voor certificering](feature-summary/certifications.md) voor meer informatie over het maken van certificeringen.

#### Taakhulpen maken {#CreateJobaids-1}

Taakhulpen is een opslagplaats van trainingsinhoud die zonder enige inschrijvings- of voltooiingscriteria toegankelijk is voor studenten. Studenten kunnen deze taakhulpen gebruiken om hulp te krijgen bij het uitvoeren van een activiteit of taak in een organisatie. Ook al is het niet verplicht om taakhulpen te gebruiken als onderdeel van het maken van een cursus, het Learning Manager-team adviseert toch taakhulpen te maken als best practice voor uw organisatie. Raadpleeg de  [Help bij taakhulpen](../authors/feature-summary/job-aids.md) voor informatie over het maken van taakhulpen.

#### Leerprogramma’s maken {#Createlearningprograms-1}

Leerprogramma&#39;s zijn een reeks uniek ontworpen cursussen die voldoen aan specifieke leerdoelen. Voordat u leerprogramma&#39;s maakt, moet u ervoor zorgen dat u al enkele cursussen hebt gemaakt of dat er bestaande cursussen beschikbaar zijn in uw account.  Hoewel het voor een organisatie optioneel is om deze functie te gebruiken, raadt het Learning Manager-team u aan deze functie te gebruiken om gericht leren voor uw werknemers op te nemen. Klik op Leerprogramma in het linkerdeelvenster om de leerprogramma&#39;s te gebruiken, kies vervolgens een reeks cursussen uit de catalogus en publiceer deze. Raadpleeg de [Help bij leerprogramma&#39;s](feature-summary/learning-programs.md) voor specifieke instructies.

## Fase 4 - Beheer van uw LMS (Learning Manager-beheerder) {#phase4managingyourlmscaptivateprimeadministrator}

### Aankondigingen {#announcements}

Met aankondigingen kan uw organisatie alle belangrijke informatie in één keer aan alle studenten van een account verspreiden. In de Learning Manager-toepassing is een aankondiging een multimediabericht (tekst, beeld of video) dat een beheerder kan maken en uitzenden naar een specifieke groep gebruikers en leerobjecten. U kunt direct aankondigingen versturen of deze automatisch op een bepaalde datum laten activeren. Als u deze functie wilt gebruiken in de Learning Manager-toepassing, kiest u Aankondigingen in het linkerdeelvenster en klikt u op Toevoegen om aankondigingen te maken. Raadpleeg [Help voor aankondigingen](feature-summary/announcements.md) voor meer informatie.

### Inschrijving van gebruikers {#userenrollment}

De inschrijving van gebruikers is een belangrijke stap voor een LMS-toepassing. U kunt nu beginnen met het inschrijven van de studenten voor verschillende leerobjecten van de Learning Manager-toepassing. U kunt studenten handmatig of geautomatiseerd inschrijven door gebruik te maken van leerplannen.

#### Handmatige inschrijving {#manualenrollment}

* **Zelfinschrijving -** Als u deze optie inschakelt tijdens het maken van een leerobject, kunnen studenten zichzelf inschrijven voor de leerobjecten.
* **Goedkeuring van manager** - Als u deze optie kiest bij het inschrijvingstype terwijl u een cursus maakt, moeten managers de inschrijving van de studenten goedkeuren.
* **Benoeming manager** - Als u dit inschrijvingstype kiest tijdens het maken van een cursus, moeten dergelijke cursussen worden aangewezen door managers.
* **Beheerderinschrijving** - In dit geval kan de beheerder een aantal studenten inschrijven op basis van de vereisten van de organisatie.

Raadpleeg [Help voor gebruikersinschrijving](feature-summary/courses.md)voor meer informatie.

Schrijf studenten op de volgende vier manieren handmatig in voor leerobjecten:

### Geautomatiseerde inschrijving {#automatedenrollment}

Automatiseer de inschrijving van de studenten voor leerobjecten met behulp van leerplannen.

#### Leerplannen (op basis van activeringen) {#learningplansbasedontriggers}

U kunt leerplannen gebruiken om automatisch cursussen, leerprogramma&#39;s of certificeringen toe te wijzen aan studenten, op basis van het voorvallen van bepaalde gebeurtenissen. Bijvoorbeeld:

* Er wordt een nieuwe gebruiker toegevoegd
* Een gebruiker verandert van gebruikersgroep
* Een student voltooit een leerobject
* Een gebruiker voltooit een vaardigheid

Raadpleeg [Help bij leerplannen](feature-summary/learning-plans.md)  voor meer informatie.

### Rapporten maken {#createreports}

Nu kunt u beginnen met het maken en beheren van verschillende soorten rapporten.

Met Adobe Learning Manager kunt u meerdere rapporten aanmaken om leeractiviteiten te volgen, monitoren en beheren. U kunt de volgende drie typen rapportagefuncties gebruiken om rapporten te genereren:

* **Dashboard Rapporten** - Maak samenvattingsrapporten om actiegerichte inzichten te krijgen in het gebruik van leerinhoud door uw studenten, op basis van verschillende categorieën zoals gebruikersgroepen, effectiviteit, cursustijd voor studenten enzovoort.
* **Studenttranscripten** - Maak centrale rapporten voor studenten met een volledige geschiedenis van studenten van de registratiedag tot aan de datum.
* **Cursusrapporten** - Statistieken over het cursusverbruik van studenten op basis van individuele cursussen maken. U kunt ook quizrapporten op cursusniveau maken.

Raadpleeg  [Help bij rapporten](feature-summary/reports.md) voor meer informatie over het genereren van rapporten.

Voor andere informatie over het gebruik van de functies van de LMS-toepassing raadpleegt u [Help bij Learning Manager](../topics.md) op basis van elke rol.
