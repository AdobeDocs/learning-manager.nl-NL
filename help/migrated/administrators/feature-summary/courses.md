---
description: Dit document bestaat uit Help om cursusmodules, instanties en cursussen voor de beheerdersrol te maken.
jcr-language: en_us
title: Cursusmodules, instanties en leerprogramma's maken
contentowner: manochan
source-git-commit: 0052ccb2f5a8f9617bca2c7bad91c0cd18338b66
workflow-type: tm+mt
source-wordcount: '4544'
ht-degree: 0%

---



# Cursusmodules, instanties en leerprogramma&#39;s maken

Dit document bestaat uit Help om cursusmodules, instanties en cursussen voor de beheerdersrol te maken.

Auteurs maken cursussen. Studenten kunnen de cursussen volgen en beheerders kunnen de prestaties van de studenten volgen op basis van het cursusverbruik.

## Overzicht {#overview}

Auteurs maken cursussen. Studenten volgen de cursussen en beheerders kunnen de prestaties van de studenten volgen op basis van het cursusverbruik. Beheerders kunnen de cursussen die door auteurs zijn gemaakt bekijken en sommige activiteiten uitvoeren zoals uitgelegd in deze sectie. Als beheerder kunt u unieke leerprogramma&#39;s maken met een vooraf gedefinieerde set cursussen voor studenten.

## Instantie van een cursus maken {#createinstanceofacourse}

Nadat een auteur een cursus heeft gemaakt, kunt u instanties van de cursus maken. Door instanties van een cursus te maken, kunt u dezelfde cursus op verschillende tijdstippen aan uw studenten aanbieden. Studenten kunnen elke gewenste instantie kiezen en zich inschrijven. U kunt elke instantie configureren voor een eigen set badges, feedback en andere instellingen.

Een instantie maken:

1. Klik in de beheerderswebapp op **[!UICONTROL Cursussen]** in het linkerdeelvenster.
1. Kies in de lijst de gewenste cursus en klik op **[!UICONTROL Cursus weergeven]**.

   ![](assets/view-course.png)

   *Een cursus weergeven*

1. Klik op **[!UICONTROL Instanties]** in het linkerdeelvenster. Elke cursus heeft standaard een instantie. U kunt de standaardinstantie wijzigen of instanties toevoegen. U kunt deze cursusinstantie niet verwijderen.
1. Klik op **[!UICONTROL Nieuwe instantie toevoegen]** rechtsboven in de cursusinformatie. Er wordt een nieuwe instantie van de cursus weergegeven.
1. Voer de eigenschappen van de instantie in:

   * In het dialoogvenster **[!UICONTROL Instantienaam]** voert u de naam in van de instantie die u aan de cursus wilt koppelen. Zorg ervoor dat u een unieke naam voor de instantie gebruikt.
   * Geef de voltooiingsdeadline voor de instantie op. Studenten moeten op deze datum de voltooiingsstatus van de cursus hebben bereikt.
   * Klikken **[!UICONTROL Meer opties tonen]** om andere deadline-opties weer te geven.
   * **[!UICONTROL Deadline voor inschrijving]:** Dit is de datum waarop een student zich moet inschrijven voor een leerobject in geval van zelfinschrijving.
   * **[!UICONTROL Deadline voor uitschrijving]:** U kunt uitschrijving door de student zelf beperken door een uitschrijvingsdeadline te hebben.

   Een beheerder kan besluiten om voltooiingsdeadlines voor een cursus of leerprogramma te hebben op basis van vereisten. Het wordt echter aanbevolen om er een te hebben voor klassikale/virtuele klassikale trainingen.

   ![](assets/create-an-instance.png)

   *Einddeadline instellen*

## Eigenschappen van de instantie weergeven {#viewpropertiesoftheinstance}

![](assets/properties-of-aninstance.png)

*Eigenschappen van de instantie weergeven*

1. **Modules:** Het aantal modules dat door de auteur van de cursus is gemaakt
1. **Ingeschreven studenten:** Het aantal studenten dat door de beheerder voor de cursus is ingeschreven.
1. **Sessies:** Het aantal virtuele klassikale en klassikale modules in de cursus.
1. **Feedback ingeschakeld:** Geeft aan of L1-, L2- en L3-feedback voor deze cursus is ingeschakeld.

## Een instantie archiveren {#retireaninstance}

Voer de onderstaande stappen uit om een instantie te archiveren;

1. Klik op het vervolgkeuzemenu en kies de optie **[!UICONTROL Retire-instantie]**.

   ![](assets/retire-an-instance.png)

   *Een instantie archiveren*

1. Als u naar alle gearchiveerde instanties wilt zoeken, klikt u op het tabblad **[!UICONTROL Gearchiveerd]** op de pagina Instanties.

## Instantie herstellen {#restoreaninstance}

Voer de volgende stappen uit om een gearchiveerde instantie te herstellen naar een activeringsstatus:

1. Klik op het vervolgkeuzemenu en kies de optie **[!UICONTROL Instantie opnieuw openen]**.

   ![](assets/restore-an-instance.png)

   *Instantie herstellen*

1. De instantie wordt nu teruggezet naar een actieve modus.

## E-mails op instantieniveau verzenden

E-mails op instantieniveau naar ingeschreven studenten verzenden:

1. Selecteer de gewenste opties op de pagina Instanties en klik op **[!UICONTROL Ingeschreven studenten e-mailen]**.

![e-mails op instantieniveau](assets/adhoc-email.png)

*E-mailstudenten ingeschreven voor instantie*

1. Selecteer in het dialoogvenster Aankondiging maken de optie Type als e-mail. Geef het onderwerp op, typ het bericht en klik op Opslaan. De training wordt automatisch geselecteerd.

   ![Aankondiging maken als e-mail](assets/email-announcement.png)

   *Aankondiging maken als e-mail*

1. Nadat u op **[!UICONTROL Opslaan]** verschijnt, ziet u een bevestigingsbericht voor het succesvol maken van de aankondiging. Klik op **[!UICONTROL Nu publiceren]**.

   ![Aankondiging is gemaakt](assets/announcement-successful.png)

### Studenten in verschillende instanties inschrijven

1. Selecteer een cursus in de lijst met cursussen.
1. Selecteren **[!UICONTROL Studenten]** in het linkerdeelvenster.
1. Selecteren **[!UICONTROL Inschrijven]**.

   ![Studenten inschrijven](assets/enroll-learners-new.png)

   *Cursus publiceren*

1. In het dialoogvenster [!UICONTROL **Studenten inschrijven**] kunt u:

   * Selecteer een instantie om een student in te schrijven in het vervolgkeuzemenu Instantie selecteren.
   * Selecteer de gebruiker of gebruikersgroepen of beide in het veld Inclusief studenten.
   * Selecteer in het veld Studenten uitsluiten de studenten die u van de instantie wilt uitsluiten.
   * Selecteer onder aan het dialoogvenster Ja als u een of meer studenten voor de geselecteerde instantie wilt inschrijven.

1. Selecteren **[!UICONTROL Doorgaan]**.

   ![doorgaan](assets/proceed.png)

   *Ga door met het inschrijven van studenten*

### Inschrijvingsrapport van een instantie weergeven

1. Selecteer een cursus in de lijst met cursussen.
1. Selecteren **[!UICONTROL Studenten]** in het linkerdeelvenster.
1. Selecteren **[!UICONTROL Handelingen]** > **[!UICONTROL Exporteren]**.

Het Excel-bestand bevat werkbladen voor elke instantie. Een werkblad bestaat uit de volgende velden:

* Studenten
* E-mail
* Unieke gebruikersnaam
* Cursusnaam
* LO Unique ID
* Status
* Selectiecriteria
* Inschrijvingsdatum / Uitschrijvingsdatum (tijdzone UTC)
* Voltooiingsdatum (UTC-tijdzone)
* Vervaldatum (UTC-tijdzone)
* Begindatum (UTC-tijdzone)
* Quiz Score
* Naam manager
* Adres
* userState
* Deskundigheidsgebied
* Opmerkingen
* Aantal bezoeken
* Bezoekdatums
* Tijdstempels (UTC-tijdzone)
* Tijd besteed (min)

>[!NOTE]
>
>Opmerking: Als u meervoudige inschrijving inschakelt, worden voor elke cursus meerdere rijen toegevoegd aan het Studenttranscriptrapport (één rij voor elke instantie).
>
>Als u een automatiseringsinstelling hebt ingesteld die slechts één rij per cursus verwacht, moet u de vereiste aanpassingen in de rapportautomatisering aanbrengen voordat u de functie voor meervoudige inschrijving inschakelt.

## escalatieniveau instellen {#escalation}

Voor het verzenden van de e-mailmeldingen moet een beheerder expliciet het escalatieniveau kiezen naar:

* Manager
* Manager &amp; Niveaubeheer overslaan

![](assets/escalation-notification.png)

*escalatieniveau instellen*

## Cursusmoderatie {#coursemoderation}

Telkens wanneer een auteur modules toevoegt, bijwerkt of verwijdert en een cursus opnieuw publiceert, ontvangen alle beheerders hierover een melding. Als beheerder kunt u vervolgens de wijzigingen bekijken, de oude en nieuwe inhoud vergelijken door op de koppeling te klikken en de wijzigingen goedkeuren of afwijzen.

Klik op **[!UICONTROL Instellingen]** > **[!UICONTROL Algemeen]**. Selecteer de **[!UICONTROL Cursusmoderatie]** schakel dit selectievakje in.

![](assets/2.png)

*Cursusmoderatie inschakelen*

Klik op de melding om de wijzigingen te bekijken die de auteur in de cursus heeft aangebracht. Vervolgens keurt u de door de auteur aangebrachte wijzigingen goed of wijst u deze af. Als u besluit om uw cursus goed te keuren, wordt deze opnieuw gepubliceerd. Als u de updates afwijst, blijft de vorige versie van de cursus bestaan. In beide gevallen wordt een melding naar de auteur verzonden.

![](assets/1.png)

*Aanvragen van auteurs voor cursusupdates*

Als er meerdere auteurs zijn die dezelfde cursus bijwerken, wordt de laatste of laatst uitgevoerde wijziging weergegeven in de beheerdersmelding. U kunt vervolgens de laatste wijzigingen goedkeuren of afwijzen.

## L1- en L3-feedback toevoegen {#addl1andl3feedback}

U kunt L1- en L3-feedbackopties toevoegen tijdens het maken van de cursussen:

1. Klik op Cursussen in het linkerdeelvenster nadat u zich als beheerder hebt aangemeld. Rechts op de pagina verschijnt een lijst met alle cursussen.
1. Klik op de cursustegel waarvoor u L1- of L3-feedback wilt toevoegen
1. Klik op standaard instantie in het linkerdeelvenster.
1. Klik op de cirkel op de wisselknop naast L1- of L3-feedback om deze in te schakelen.
1. Voeg de L3-feedbackvraag toe in het tekstgebied onder L3-vraag.

## Verplicht L1-feedback {#mandatory-l1-feedback}

In L1-feedback kunt u alle vragen of de eerste vraag verplicht stellen.

![](assets/make-all-questionsmandatory.png)

*Alle vragen of de eerste vraag verplicht stellen in L1-feedback*

Nu kun je de vragen maken, die nu verplicht worden.

![](assets/create-mandatoryquestions.png)

*Vragen maken*

Als de twee verplichte vragen om een bepaalde reden geen tekst hebben, worden de vragen niet weergegeven in het feedbackformulier.

>[!NOTE]
>
>Het is niet voldoende dat u deze instellingen inschakelt in de leerprogrammainstantie. U moet deze instellingen ook op cursusinstantieniveau inschakelen voor elke cursus in het leerprogramma.

Als u deze optie inschakelt, wordt op de pagina Standaardinstellingen **[!UICONTROL Alle vragen verplicht stellen]** worden deze instellingen overgenomen door alle nieuwe instanties die daarna worden gemaakt.

![](assets/instance-defaults-makeallquestionsmandatory.png)

*De pagina Standaardinstellingen voor instanties weergeven*

## L1-feedback op cursusniveau {#l1-feedback-course-level}

In eerdere versies van Learning Manager kon een beheerder L1-feedback voor het leerprogramma inschakelen.

In deze release van Learning Manager kan de beheerder L1-feedback sturen voor alle cursussen die deel uitmaken van het leerprogramma. De beheerder moet ervoor zorgen dat L1-feedback is ingeschakeld voor alle cursussen op cursusinstantieniveau.

1. Klik in de Admin-app op **[!UICONTROL Leerprogramma&#39;s]** > **[!UICONTROL Leerprogramma weergeven]**.

1. Klikken **[!UICONTROL Instanties]** > **[!UICONTROL L1-feedback ingeschakeld]**.

1. De optie inschakelen **[!UICONTROL Inschakelen voor elke cursus]**.

   ![](assets/enable-l1-feedbackforcourse.png)

   *Cursusfeedback inschakelen*

   Alleen als u deze schakelknop op het niveau van het leerprogramma inschakelt, wordt de L1-feedback voor de cursussen in dit programma niet geactiveerd. Als u L1-feedback wilt inschakelen, gaat u naar elke cursus in het leerprogramma en schakelt u de L1-feedbackschakelaar in.

   ![](assets/l1-reaction-feedback.png)

   *L1-feedback voor elke cursus inschakelen*

   Als L1-feedback voor alle cursussen is ingeschakeld, maar in de leerprogrammainstantie is uitgeschakeld, wordt de L1-feedback niet geactiveerd voor de cursussen.

## Taalspecifieke quizrapporten

Quizrapporten helpen bij het evalueren van de prestaties van een student na voltooiing van een leerprogramma of cursus.

Leermanager vereenvoudigt momenteel het leren in 13 interfacetalen en 32 inhoudstalen. Hoewel deze optie studentvriendelijk is en onze studenten wereldwijd eenvoudig kan ondersteunen, is het voor beheerders moeilijk om rapporten op te halen die in verschillende landinstellingen worden geprobeerd.

Quizrapporten, gegevens in verschillende talen weergeven, vooropgesteld dat de cursus in meerdere talen wordt aangeboden. Tot nu toe werden in rapporten die zijn gegenereerd door de beheerder onder elkaar reacties weergegeven, ongeacht de taal waarin de quiz is uitgevoerd. **Bijvoorbeeld** Als een gebruiker een quiz in het Nederlands heeft afgelegd, kan de beheerder alleen die quizrapporten bekijken die gebruikers in het Nederlands hebben geprobeerd. De beheerder die Engels als interfacetaal heeft geselecteerd, kon geen rapporten voor alle gebruikers tegelijk bekijken, ongeacht de landinstelling die is opgegeven.

Dit is nu gecorrigeerd, omdat de beheerder nu alle rapporten kan bekijken in de respectieve taal die de leerling heeft geprobeerd tegelijk, ongeacht de gekozen landinstelling voor de inhoud. Quizpogingen in verschillende talen worden als extra kolommen toegevoegd aan het quizrapport.

## L1-feedback op accountniveau inschakelen {#l1-feedback-account-level}

*L1-feedback op accountniveau inschakelen*

Een beheerder kan L1-feedback inschakelen voor nieuwe cursussen en leerprogramma&#39;s door deze instelling op accountniveau in te schakelen. Deze instelling heeft echter geen invloed op de bestaande cursussen en leerprogramma&#39;s

Indien ingeschakeld wordt de feedback standaard ingeschakeld voor alle nieuwe trainingen en nieuwe exemplaren. Als een auteur/beheerder de instantie bezoekt, wordt de instantie standaard ingesteld en handmatig uitgeschakeld, maar wordt de instantie gerespecteerd.

Klik in de Admin-app op **[!UICONTROL Instellingen]** > **[!UICONTROL Feedback]**.

![](assets/l1-feedback-settings.png)

*De pagina Feedbackinstellingen weergeven*

Klikken **[!UICONTROL Bewerken]** in de rechterbovenhoek en schakel de optie in om L1-feedback in te schakelen.

Wanneer een auteur een cursus maakt, wordt op de Instantiepagina van de Admin-app het **[!UICONTROL L1-feedback]** wordt automatisch ingeschakeld voor de nieuwe cursus.

<!--![](assets/l1-feedback-enabled.png)-->

U kunt de L1-feedback ook uitschakelen door de **[!UICONTROL Inschakelen]** zoals hieronder weergegeven:

![](assets/disable-l1-feedback.png)

*L1-feedback in- of uitschakelen*

## Beschrijvende vragen toevoegen voor L1- en L3-feedback {#descriptive}

Als onderdeel van de november-release van Learning Manager beschikt u over een optie om beschrijvende vragen toe te voegen. Beheerders kunnen deze vragen aan studenten toevoegen. Deze voorziening is een aanvulling op de standaardset vragen van de Learning Manager. U kunt deze desgewenst ook verplicht maken door de optie onder de vraag te kiezen.

U kunt twee beschrijvende vragen toevoegen voor L1-feedback en één beschrijvende vraag voor L3-feedback.

Als u L1-feedback hebt ingeschakeld, kunt u de opties bekijken zoals weergegeven in de volgende afbeelding.

![](assets/l1-feedback-desc-questions.png)

*Beschrijvende vragen toevoegen voor L1- en L3-feedback*

Als u de vragenlijst onmiddellijk na het voltooien van de cursus aan de student wilt laten zien, kunt u de optie dienovereenkomstig kiezen.

Hieronder vindt u ter referentie een voorbeeld van de L1-vragenlijst. Studenten kunnen de vragenlijst in de onderstaande indeling bekijken. Test-1 en Test-2 zijn de beschrijvende vragen.

![](assets/l1-output.png)

*Een voorbeeld van feedbackvragen voor een cursus*

Nadat u L3-feedback hebt ingeschakeld, kunt u de opties bekijken zoals weergegeven in de onderstaande afbeelding:

![](assets/l3-feedback-desc-questions.png)

*L3-feedback inschakelen*

Vraag 2 is de beschrijvende vraag voor L3-feedback. U kunt dit verplicht maken door op de bijbehorende optie onder de vraag te klikken.

Hieronder vindt u ter referentie een voorbeeld van de L3-vragenlijst. Studenten kunnen de vragenlijst in de onderstaande indeling bekijken.

![](assets/l3-output.png)

*L3-feedbackuitvoer weergeven*

## vragenlijst voor L1- en L3-feedback instellen {#setupl1andl3feedbackquestionnaire}

U kunt de vragenlijst voor L1- en L3-feedback instellen en ook herinneringen op accountniveau instellen.

1. Klikken **[!UICONTROL Instellingen]** en dan **[!UICONTROL Feedback]** in het linkerdeelvenster nadat u zich als beheerder hebt aangemeld.\
   De pagina Feedbackinstellingen wordt weergegeven met twee tabbladen: **[!UICONTROL L1-feedback]** en **[!UICONTROL L3-feedback]**.\
   **[!UICONTROL L1-feedback]** tab bestaat uit een lijst met standaardinstellingen **[!UICONTROL L1-feedback]** vragenlijst voor klaslokalen en cursussen op eigen tempo, samen met herinneringsinstellingen. In **[!UICONTROL L3-feedback]** kunt u de standaardinstellingen voor L3-feedback en herinneringen weergeven.

1. Klik op Bewerken in de rechterbovenhoek van de pagina om de bestaande vragenlijst te wijzigen.\
   In **[!UICONTROL L1-feedback]** kunt u elke vraag in- of uitschakelen door op de schakelknop Ja/Nee te klikken.\
   In **[!UICONTROL L3-feedback]** kunt u de standaardfeedbackinstructie wijzigen.\
   Klikken **[!UICONTROL Nieuwe herinnering toevoegen]** onder aan de pagina en kies wanneer u de herinneringen wilt verzenden.

1. Klikken **[!UICONTROL Opslaan]** rechtsboven op de pagina.

In L1-feedback ziet u twee sets vragenlijsten samen met een standaardvraag. De eerste set vragenlijsten heeft betrekking op cursussen op eigen tempo die ook kunnen worden gebruikt voor cursussen op basis van activiteit. De tweede set vragenlijsten kan worden gebruikt voor cursussen van het type klaslokaal en virtuele lesruimte.

## Gegevens in controlelijst exporteren {#export-checklist-data}

Open in de lijst met cursussen een cursus die een checklist bevat. In het linkerdeelvenster ziet u een optie **[!UICONTROL Checklist]**.

![](assets/export-checklist.png)

*Gegevens in controlelijst exporteren*

Klik op de optie en voer op de cursuspagina het volgende uit:

1. Selecteer de instantie en de module.
1. Klikken **[!UICONTROL Handelingen]** > **[!UICONTROL Exporteren]** en exporteer vervolgens het controlelijstrapport voor studenten.

Op de **[!UICONTROL Checklist]** een docent het controlelijstrapport kan exporteren vanuit de **[!UICONTROL Handelingen]** vervolgkeuzelijst.

Het CSV-rapport bevat de volgende velden:

* Gebruikersnaam
* E-mailadres gebruiker
* Naam van manager en e-mail
* Naam van training
* Trainingsinstantie
* Naam docent en e-mail
* Verzonden op
* Beoordelingsstatus
* Vragen met werkelijke tekst
* Gebruikersstatus
* Profiel
* Actief(e) veld(en)

Wanneer u een rapport downloadt nadat u een statusfilter hebt geselecteerd, bevat het gedownloade rapport Studenttranscripten de studentgegevens op basis van het toegepaste statusfilter. Dit extra filter wordt ook weergegeven als aangepaste beheerder en manager wanneer deze op het punt staan een studenttranscript te genereren.

## Cursussen weergeven {#viewingcourses}

Als beheerder kunt u een lijst met alle beschikbare cursussen weergeven.   Klikken **[!UICONTROL Cursussen]** in het linkerdeelvenster om de lijst met cursussen met zoek- en filteropties weer te geven. U kunt ook het effectiviteitspercentage van elke cursus bekijken op de cursusminiaturen.

>[!NOTE]
>
>U kunt een cursus archiveren nadat deze door studenten is gevolgd of wanneer u een bepaalde cursus na publicatie wilt uitstellen. U kunt een cursus alleen archiveren als deze de status Gepubliceerd heeft. Klik op de knop **[!UICONTROL Gearchiveerd]** tabblad.

## Quizscores weergeven {#viewquizscores}

1. Klik op de cursusnaam op de cursusminiatuur.
1. Klik op Quizscore in het linkerdeelvenster.

U kunt de quizscores van een bepaalde cursus bekijken op basis van de gebruikersnaam of op basis van elke vraag. Kies overeenkomstig de tabbladen Op gebruiker of Op vraag.

Kies het type instantie in de vervolgkeuzelijst om de scores weer te geven op basis van elke instantie van de cursus.

## Studentenlijst voor een cursus beheren {#managelearnerslistforacourse}

1. Klik op de cursusnaam op de cursusminiatuur.
1. Klik in het linkerdeelvenster op **[!UICONTROL Studenten]**.

![](assets/courses-learners.png)

*Studenten in een cursus selecteren*

U kunt de volgende handelingen uitvoeren vanaf de pagina Studenten:

* Selecteer de student die u wilt verwijderen en klik op [!UICONTROL **Handelingen**] > [!UICONTROL **Verwijderen**].
* Selecteer de student van wie u de aanwezigheid wilt markeren en klik op [!UICONTROL **Handelingen**] > [!UICONTROL **Markeren als voltooid**].

Als u studenten wilt toestaan een module opnieuw in te stellen en de module opnieuw te gebruiken, klikt u op [!UICONTROL **Herstellen**]. Klik in het pop-updialoogvenster op Ja om het opnieuw instellen te bevestigen. Modules die zijn voltooid, kunnen niet opnieuw worden ingesteld. Alleen mislukte of onvolledige modules kunnen opnieuw worden ingesteld.

U kunt de lijst met studenten ook exporteren in een Excel-blad. Als u de lijst met studenten wilt exporteren, klikt u op [!UICONTROL **Handelingen**] > [!UICONTROL **Exporteren**].

>[!NOTE]
>
>Als een cursus meerdere instanties heeft, wordt de lijst met studenten in Excel op elk tabblad afzonderlijk weergegeven. De studentenlijst bestaat uit de naam, status en selectiecriteria van de student. De status van studenten kan **Niet gestart**, of **In uitvoering**, of **Voltooid**.

## Aanwezigheid van studenten exporteren {#attendance}

Voor elke klaslokaal en VC-cursus kunt u de lijst downloaden met studenten die deze cursus hebben bijgewoond, voor elke instantie.

Klik op de pagina met cursusgegevens op **[!UICONTROL Aanwezigheid en scores]** in het rechterdeelvenster.

Klik in de rechterbovenhoek van de pagina op de knop **[!UICONTROL Handelingen]** vervolgkeuzelijst. Klik vervolgens op de optie **[!UICONTROL Studentenlijst exporteren (PDF)]**.

![](assets/export-list-of-learners.png)

*Lijst met studenten exporteren als PDF*

Op de PDF kunt u dezelfde set studenten bekijken als een docent.

Wanneer u de PDF downloadt, ziet u de tijdzone (in UTC) die is gebruikt bij het maken van de cursus.

## Studenten exporteren in status voor goedkeuring in behandeling

Een beheerder, manager of aangepaste beheerder kan gegevens exporteren van studenten die zich in de inschrijvingsstatus voor goedkeuring bevinden. U kunt de gegevens exporteren via **Cursus > Student** en klik op de vervolgkeuzelijst Handeling.

De optie is aanwezig wanneer geen enkele student is ingeschreven voor/goedkeuring wacht op goedkeuring voor de door de manager goedgekeurde cursus en er een leeg rapport wordt gegenereerd. U kunt ook exporteren wanneer studenten zich in de status In afwachting van goedkeuring, Ingeschreven, In afwachting en Uitgeschreven bevinden.

Het rapport bevat gegevens van actieve, verwijderde en geschorste gebruikers als deze nog moeten worden goedgekeurd. Het rapport bevat ook gegevens van interne en externe gebruikers die zich in de goedkeuringsstatus bevinden.

Als een student die zich eerder in de goedkeuringsstatus bevond, uitschrijft, is zijn/haar record niet aanwezig in het rapport. Ook als een student die zich eerder in de goedkeuringsstatus bevond, door een beheerder/manager/aangepaste beheerder voor de cursus is ingeschreven, wordt zijn/haar record in het rapport weergegeven.

## L1- en L3-feedback weergeven {#viewl1andl3feedback}

U kunt de L1-feedback van studenten voor een cursus en de L3-feedback van managers voor studenten bekijken.

1. Klik op een willekeurige cursustegel in de lijst Cursussen.
1. Klik op L1-feedback of L3-feedback in het linkerdeelvenster om de ontvangen feedback te bekijken.
1. Selecteer de instantie in de vervolgkeuzelijst om de feedback voor die instantie te bekijken.

## Cursussen voorvertonen {#previewcourses}

Beheerder kan een voorbeeld van cursussen bekijken door op de knop **[!UICONTROL Voorvertonen als student]** tijdens het bekijken van de cursusmodules.

1. Klikken **[!UICONTROL Cursussen]** in het linkerdeelvenster nadat u zich als beheerder hebt aangemeld.
1. Klik op een willekeurige cursustegel in de lijst met cursussen op de pagina.
1. Klik op Voorbeeld bekijken als student in het linkerdeelvenster en klik op de modulenaam op de pagina om een voorvertoning van de cursusmodule in de speler weer te geven.

## Cursuseffectiviteit {#courseeffectiveness}

De effectiviteit van de cursus wordt geëvalueerd om inzicht te krijgen in het nut van een cursus voor de student. Het is een combinatie van de resultaten van feedback van de student over de cursusinhoud, de quizresultaten van de cursus voor een student en feedback van de manager die een student evalueert op basis van de verworven kennis.

De beheerder kan de effectiviteitsscore van de cursus op de cursusminiaturen bekijken, zoals weergegeven in de onderstaande afbeelding. U kunt de score voor deze cursus zien als 100.

<!--![](assets/course-effectiveness-tag1.png)-->

De effectiviteitsscore van de cursus wordt bepaald op basis van de L1-, L2- en L3-feedbackwaarden. Klik op de effectiviteitswaarde van de cursus om het overzicht van elke feedback weer te geven. Er verschijnt een pop-up, zoals hieronder weergegeven.

![](assets/course-effectiveness.png)

*Cursuseffectiviteit bekijken voor L1-, L2- en L3-feedback*

In deze voorbeeldmomentopname kregen 1 van de 1 gebruikers alle drie feedbacks, vandaar dat de score 100/100 is. Uit deze tabel kunt u opmaken dat als een van de drie feedbacks (L1, L2 en L3 ) niet voor een cursus wordt gegeven, dit een negatief effect heeft op de algehele effectiviteit. Klik op de pijl-omlaag in de rechterbenedenhoek van het pop-upvenster om te zien hoe de effectiviteitsberekeningen van de cursus zijn uitgevoerd.

![](assets/course-effectiveness-calculations.png)

*Berekening van cursuseffectiviteit*

Volgens het bovenstaande cirkeldiagram wordt meer gewicht gegeven aan L3-feedback van de manager.

## Cursussen en leerprogramma&#39;s zoeken {#searchingcoursesandlearningprograms}

Met Adobe Learning Manager kunt u gemakkelijker snel de gewenste cursussen/leerprogramma&#39;s vinden. U kunt op twee manieren naar uw cursussen zoeken:

1. Zoekveld gebruiken. Klik op het zoekpictogram in de rechterbovenhoek. Er wordt een zoekveld weergegeven. Typ de naam van de cursus of eventuele trefwoorden die bij uw cursussen horen om uw cursussen/leerprogramma&#39;s te vinden. U kunt ook zoeken met vooraf gedefinieerde tags, zoals Captivate, C, Java en HTML. U kunt naar tags zoeken in het veld Zoeken, wat betekent dat de tags in het zoekveld worden weergegeven terwijl u ze typt.
1. Door de lijst van cursussen/leerprogramma&#39;s met de filters te filteren. U kunt de cursussen filteren op status zoals Alle, Gepubliceerd, Concept en Gearchiveerd. Conceptiefilter wordt niet weergegeven in de beheerdersmodus.

U kunt zoeken op basis van competenties door op Competenties te klikken en ze te kiezen. Als beheerder kunt u de cursussen op vier manieren sorteren om de gewenste cursus beter te vinden. Klik op Sorteren op en kies alfabetische oplopende volgorde, alfabetische aflopende volgorde, datum waarop cursus is bijgewerkt of effectiviteit van cursussen.

<!--![](assets/admin-sortby.png)-->

U kunt leerprogramma&#39;s op drie manieren sorteren: alfabetisch oplopend, alfabetisch aflopend en op basis van bijgewerkte datum.

## Studenten inschrijven {#enrollinglearners}

U kunt dezelfde stappen volgen om studenten in te schrijven voor cursussen, leerprogramma&#39;s en certificeringen. Managers kunnen ook studenten onder hem inschrijven door de volgende stappen uit te voeren.

Beheerder schrijft sommige studenten in voor verplichte cursussen volgens de vereisten van de organisatie:

1. Houd de muis boven gepubliceerde tegels van cursussen en klik op Studenten inschrijven.\
   U kunt ook op een gepubliceerde cursustegel klikken en op de studenten in het linkerdeelvenster klikken. Er verschijnt een pagina met een lijst met studenten. Klik op Inschrijven.\
   Het dialoogvenster Studenten inschrijven verschijnt.

1. Selecteer de instantie in de vervolgkeuzelijst Instantie selecteren. De vervolgkeuzelijst bevat alle instanties, inclusief actieve, gearchiveerde en verlopen instanties.

>[!NOTE]
>
>Beheerder kan alle geregistreerde studenten van een cursus verwijderen door op de studentenpagina op de vervolgkeuzepijl te klikken en op **[!UICONTROL Handelingen]** > **[!UICONTROL Verwijderen]**.

![](assets/enroll-learners.png)

*Opmerkingen toevoegen tijdens het inschrijven van studenten*

*Studenten inschrijven*

## Gebruikers

+++Inclusief studenten

Selecteer de gebruikersgroepen en individuele studenten (met behulp van e-mail-ID of naam) die u wilt opnemen. Voeg alle gebruikersgroepen toe in een doorsnede onder dezelfde set. Gebruik een nieuwe opnameset om een andere gebruikersgroep toe te voegen aan de vereniging.

+++

+++Studenten uitsluiten

Selecteer de gebruikersgroepen en individuele studenten (met e-mail-ID of naam) die u wilt uitsluiten. Voeg alle gebruikersgroepen toe in een doorsnede onder dezelfde set. Gebruik een nieuwe opnameset om een andere gebruikersgroep in een union toe te voegen.

+++

## E-mailadres gebruiker

+++E-mail-id

Kopieer e-mail-id&#39;s van studenten die u wilt inschrijven, gescheiden door puntkomma&#39;s, komma&#39;s of regelafstand. Gebruik de **[!UICONTROL E-mail-ID&#39;s valideren]** optie om de items te valideren. Alle ongeldige items worden rood gemarkeerd. Verwijder of corrigeer deze items en ga verder door op **[!UICONTROL Ga verder.]**

![](assets/email-id-option.png)

*Studenten inschrijven*

Het dialoogvenster Overzicht verschijnt met het aantal gebruikers uit de opnameset, de uitsluitingsset en de gebruikers die al zijn ingeschreven voor de cursusinstantie.

+++

### Opmerkingen toevoegen tijdens het inschrijven van studenten {#enroll-comments}

<!---![](assets/enroll-learners-dialog.png)-->

Als beheerder of manager kunt u opmerkingen toevoegen terwijl u studenten voor een cursus inschrijft. U kunt aanvullende informatie opgeven over de cohort van gebruikers die zich inschrijven. Deze gegevens worden geëxporteerd in cursusrapporten.

De opmerking is **niet** weergegeven aan de student.

Wanneer een beheerder het cursusrapport van de student genereert, worden eventuele opmerkingen, indien toegevoegd, weergegeven in het rapport. Het dialoogvenster Overzicht verschijnt met het aantal gebruikers uit de opnameset, de uitsluitingsset en de gebruikers die al zijn ingeschreven voor de cursusinstantie.

Op de **[!UICONTROL Studenten inschrijven]** dialoogvenster, optie uitvouwen **[!UICONTROL Geavanceerde opties]**. In het dialoogvenster **[!UICONTROL Aanvullende opmerking]** voert u de gewenste opmerking in.

![](assets/comment-for-learner.png)

*Opmerkingen voor studenten toevoegen*

## Zoeken naar ingeschreven gebruikers {#searchforusers}

Zoek naar ingeschreven gebruikers in de sectie Student van het leerobject met automatisch aangevulde zoeksuggesties. Met automatisch aangevulde zoeksuggesties kunt u geleidelijk zoeken naar ingeschreven gebruikers op naam, e-mail-ID en uuid.

![](assets/typeahead.gif)

*Analyse van het zoeken naar ingeschreven gebruikers*

Dit type zoekopdracht wordt ook wel automatisch aanvullen, incrementeel zoeken, zoeken terwijl u typt, inline zoeken of onmiddellijk zoeken genoemd.

Terwijl u een student of een gebruikersgroep in het zoekveld typt, worden een of meer overeenkomsten voor de zoekterm(en) gevonden en onmiddellijk weergegeven.

Dankzij dit proces kun je sneller en minder omslachtig zoeken naar wat je zoekt dan een aantal zoekopdrachten achter elkaar uitvoeren.

Studenten of gebruikersgroepen in alle instanties worden na een zoekopdracht weergegeven. Voor elke student wordt de instantie waarin de student is ingeschreven, weergegeven in de **[!UICONTROL Instantie]** kolom.

![](assets/search-result.png)

*Zoekresultaten weergeven*

Met behulp van automatisch aangevulde zoeksuggesties kunt u:

* Alle ingeschreven gebruikers weergeven, ongeacht instanties.
* Alle gebruikersgroepen met een of meer ingeschreven gebruikers weergeven.

Nadat een zoekopdracht is uitgevoerd, kunt u studenten niet filteren op instanties. Selecteer een instantie in het menu **[!UICONTROL Instantie selecteren]** is uitgeschakeld.

Bovendien kunt u met de zoekresultaten een student of een gebruikersgroep kiezen en de volgende handelingen uitvoeren:

* Uitschrijven
* Voltooiing markeren
* Module opnieuw instellen

Tijdens het uitvoeren van een zoekopdracht is de optie Uitschrijven > Bulk in de vervolgkeuzelijst Acties uitgeschakeld voor de cursus/het leerprogramma.

## QR-code delen met studenten voor inschrijven, voltooien of beide {#shareqrcodewithlearnerstoenrollcompleteorboth}

Beheerders in Adobe Learning Manager kunnen de QR-codes met studenten delen om zich snel voor de cursus in te schrijven. De drie verschillende QR-codes worden gebruikt om de &#39;inschrijving&#39;, &#39;voltooiing&#39; of &#39;inschrijving en voltooiing&#39; van een cursus te markeren.

Studenten kunnen gewoon de Adobe Learning Manager-apparaatapp gebruiken om de betreffende QR-code te scannen.

**U kunt als volgt de QR-code downloaden**:

1. Klikken **[!UICONTROL Cursussen]** in de sectie Leren in het linkernavigatievenster.
1. Selecteer een cursus > **[!UICONTROL Cursus weergeven]**.
1. Klikken **[!UICONTROL Instanties]** > **[!UICONTROL Meer]** > **[!UICONTROL QR-code]**.

   <!--![](assets/admin-instance-edit.png)-->

1. Schakel QR-code in en klik vervolgens op de downloadpictogrammen &#39;Inschrijven&#39;, &#39;Voltooien&#39; en &#39;Inschrijven en voltooien&#39; om een PDF te downloaden met de QR-code voor elke code. De beheerder kan de QR-code vervolgens met de studenten delen.

   ![](assets/qr-code-download-01.png)

   *QR-code delen met markeringen*

## Levenscyclus van cursus {#courselifecycle}

De levenscyclus van een cursus ziet er meestal als volgt uit:

**Concept** - Wanneer een auteur een cursus heeft gemaakt en opgeslagen. Op dit punt is de cursus nog niet beschikbaar voor studenten. U kunt een cursus op deze status verwijderen.

**Gepubliceerd** - Wanneer een auteur een cursus heeft gepubliceerd. Studenten kunnen zich nu inschrijven voor de cursus.

**Gearchiveerd** - Een auteur kan een cursus na publicatie archiveren als hij niet wil dat de cursus in de cursuscatalogus voor studenten verschijnt. U kunt een cursus op dit punt opnieuw publiceren of verwijderen.

**Verwijderd** - Een cursus heeft de status Verwijderd wanneer deze volledig is verwijderd uit de Adobe Learning Manager-toepassing. Auteurs kunnen alleen cursussen met de status Concept verwijderen. U kunt cursussen ook uit gearchiveerde status verwijderen.

![](assets/lifecycle-03.png)

*Workflow van een cursuslevenscyclus*

## Meldingsinstellingen {#notificationsettings}

Als beheerder kunt u de meldingsinstellingen aanpassen. Zie voor meer informatie [Meldingen.](user-notifications.md)

## Veelgestelde vragen {#frequentlyaskedquestions}

+++Module herstellen als beheerder?

Kies op de pagina Studenten voor een cursus de student of studenten of een groep en klik op **[!UICONTROL Handelingen]** > **[!UICONTROL Modules opnieuw instellen]**.

![](assets/reset-modules.png)

*Optie weergeven om modules opnieuw in te stellen*

Nadat u op de optie hebt geklikt, wordt de status van de modules van alle geselecteerde studenten opnieuw ingesteld. De modules die worden voltooid, worden niet opnieuw ingesteld.

+++

+++Hoe voeg ik een cursus-URL toe zodat studenten rechtstreeks naar de cursus worden omgeleid?

Plaats de muis op een cursuskaart en klik op **[!UICONTROL URL kopiëren]**. Nadat u de URL hebt gekopieerd, hebben studenten rechtstreeks via de URL toegang tot de cursus.

+++

+++Een instantie opnieuw openen?

Als u een gearchiveerde instantie opnieuw wilt openen, klikt u op de vervolgkeuzelijst in de instantie en klikt u op **[!UICONTROL Instantie opnieuw openen]**.

+++
