---
jcr-language: en_us
title: Implementatiehandleiding voor Learning Manager
description: Learning Manager is een LMS (Learning Management System) waarmee trainingsprofessionals aansprekend en aanpasbaar leermateriaal kunnen leveren dat kan bijdragen aan de behoeften of doelstellingen van een organisatie. Met Learning Manager kunnen trainers of managers in de eerste plaats cursussen en andere leerobjecten in een bepaalde volgorde toewijzen aan studenten.
contentowner: shhivkum
preview: true
source-git-commit: 2317aa899a82abe24d38c4e40a06df3646fde310
workflow-type: tm+mt
source-wordcount: '3246'
ht-degree: 0%

---



# Implementatiehandleiding voor Learning Manager

## Inleiding {#introduction}

Learning Manager is een LMS (Learning Management System) waarmee trainingsprofessionals aansprekend en aanpasbaar leermateriaal kunnen leveren dat kan bijdragen aan de behoeften of doelstellingen van een organisatie. Met Learning Manager kunnen trainers of managers in de eerste plaats cursussen en andere leerobjecten in een bepaalde volgorde toewijzen aan studenten. Dit gereedschap biedt ook verschillende krachtige functies, zoals een Fluidic Player in meerdere indelingen, gamification, badges en een gebruiksvriendelijk dashboard voor studenten. Als u echter al deze functies wilt benutten, is het van essentieel belang dat u Leerbeheer eerst configureert en instelt.

Deze handleiding bevat stapsgewijze instructies voor het aan de slag gaan met Learning Manager. Dit document bevat ook gedetailleerde configuratie- en instellingsgegevens. Lees verder om te weten te komen hoe je aan de slag gaat met Learning Manager.

## Voor wie is deze gids bedoeld? {#whoisthisguideintendedfor}

Als gebruiker van een leermanager kunt u de hoed van een beheerder, auteur, docent, manager of student dragen. Deze handleiding is bedoeld voor gebruikers die waarschijnlijk betrokken zijn bij het instellen van een LMS voor een organisatie of een klant:

* **IT-beheerder** - Als ICT-beheerder kunt u Learning Manager activeren of integreren in uw organisatie. Een IT-beheerder kan ook een of meer gebruikers toevoegen en kan de rol van integratiebeheerder of beheerder vervullen die Learning Manager integreert met toepassingen van derden.
* **Auteur** - Als auteur van een leermanager kunt u leerinhoud maken die vereist is voor de leervereisten van een organisatie. Een auteur is betrokken bij het maken van de basisinhoud die wordt geüpload in Learning Manager.

* **Beheerder van Learning Manager** - Een leermanbeheerder voert de configuratie- en instellingsactiviteiten uit die betrekking hebben op de toepassing. In sommige bedrijven kan een IT-beheerder ook de rol van beheerder van een leermanager vervullen.

## Aan de slag met de implementatie van Learning Manager {#getstartedwithcaptivateprimedeployment}

Nadat u Leermanager hebt aangeschaft, activeert u uw Leermiddelaccount met behulp van de licentiecode die u hebt ontvangen. Ga naar de volgende configuraties, zoals aangegeven in het volgende visuele voorbeeld:

![](assets/getting-started-withcaptivateprime.jpg)

## Uw site configureren in Leerbeheer {#configureyoursiteincaptivateprime}

Voordat u begint met het toevoegen en implementeren van leerobjecten in Learning Manager, zijn er een aantal belangrijke configuraties vereist. Begin met het configureren van uw site op basis van uw organisatie. De siteconfiguratie bestaat uit de volgende stappen:

* Branding en logo voor uw organisatie instellen
* E-mailsjablonen configureren
* Basisaccountinstellingen configureren
* Feedbackinstellingen configureren
* Instellingen van het dashboard van studenten configureren

### Branding en logo instellen {#setupbrandingandlogo}

Als beheerder kunt u de branding en de thema&#39;s instellen zodat deze aansluiten bij de brandvereisten van uw organisatie. Ga als volgt te werk om de branding en thema&#39;s voor uw site in te stellen:

### Het logo en de banner instellen: {#settingthelogoandbanner}

Gebruik de logo- en bannerinstellingen om het logo van uw bedrijf weer te geven in Learning Manager. Configureer de brandingopties om het domein van het bedrijf in de URL in te stellen, de organisatienaam weer te geven en kleurenschema&#39;s weer te geven die overeenkomen met het merk van de organisatie. De branding-instellingen configureren:

* Meld u als beheerder aan bij uw Learning Manager-account.
* Klik in het linkerdeelvenster op **Branding**.
* Op de Branding-pagina kunt u de volgende opties configureren door op **Bewerken** tegen de optie die u wilt wijzigen:

   * **Naam organisatie** : De waarde die u hier opgeeft, bepaalt de naam die op de banner op elke pagina van uw site wordt weergegeven.
   * **Subdomein**: Deze waarde bepaalt de URL voor uw site.
   * **Logostijlen**: De afbeelding in dit veld verschijnt als het logo in de rechterbovenhoek van elke pagina. Hier kunt u kiezen of u alleen het logo of de naam van uw organisatie wilt weergeven, of het logo en de naam van de organisatie.

![](assets/setting-the-themesforyoursite.png)

>[!NOTE]
>
>U kunt de naam en het logo alleen configureren met Branding. U kunt de positie van het logo of de afbeelding niet wijzigen.

***Learning Manager ondersteunt de volgende bestandsindelingen voor logo-afbeeldingen: .png, .jpeg, .jpg, .gif, .bmp***

### De thema&#39;s voor uw site instellen {#settingthethemesforyoursite}

Met Learning Manager kunt u het uiterlijk van uw site wijzigen met Thema&#39;s. De toepassing biedt de volgende kleurthema&#39;s die u kunt kiezen:

* Prime-standaard
* Kiezels
* Carnaval
* Herfst
* Winter lucht

U kunt een van de kleurenschema&#39;s kiezen en deze op uw bedrijfsmerken afstemmen.

1. Klik in het linkernavigatievenster van Leermanager op **[!UICONTROL Branding]**.
1. In het dialoogvenster **Thema&#39;s** sectie, klik op **[!UICONTROL Bewerken]**. Met de toepassing kunt u een nieuw thema kiezen. Terwijl u een thema selecteert, ziet u direct de kleurschema&#39;s die worden gebruikt voor de belangrijkste interface-elementen.

   ![](assets/setting-the-themesforyoursite.png)

1. U kunt de opdracht **Kleur bovenste balk**, **Accentkleur** en de **Helderheid zijbalk**.  U kunt uw eigen merkkleuren gebruiken voor deze belangrijke interface-elementen.
1. Als u de waarden weer wilt instellen op het standaardkleurenschema voor uw thema, klikt u op **[!UICONTROL Thema opnieuw instellen]**. De kleuren voor de belangrijkste UI-elementen worden ingesteld op de standaardopties voor het gekozen thema.
1. Klik op **[!UICONTROL Hints tonen]** om de labels of hints in de voorvertoning weer te geven.

   ![](assets/setting-the-themesforyoursite-step5.png)

   Er wordt een presentatie weergegeven met verschillende afbeeldingen in het deelvenster **Thema&#39;s** sectie. Met deze presentatie kunt u direct een voorvertoning van het thema of het kleurenschema weergeven. U kunt onmiddellijk een voorvertoning weergeven van geselecteerde pagina&#39;s zoals de startpagina, het dashboard voor studenten enzovoort.

1. Als u een voorvertoning van de wijzigingen in een browser wilt weergeven, klikt u op **[!UICONTROL Live voorvertoning]**. Er verschijnt een pop-upvenster Voorvertoning van livethema waarin u het kleurschema kunt wijzigen of kunt doorgaan met de standaardopties. Als u uw opties in een browser wilt bekijken, klikt u op **[!UICONTROL Voorvertoning]** in dit pop-upvenster.

   ![](assets/setting-the-themesforyoursite-step6.png)

1. De gekozen opties worden tijdelijk toegepast op uw site. Als u het geselecteerde thema en de kleurinstellingen wilt opslaan, klikt u op **[!UICONTROL Toepassen]**.
1. Nadat u een thema hebt geselecteerd en toegepast, klikt u op ****[!UICONTROL Opslaan]**** om uw keuze op te slaan.

## E-mailsjablonen configureren {#configureemailtemplates}

Als beheerder is het uw volgende stap om e-mailsjablonen voor verschillende gebeurtenissen te configureren. U kunt e-mailsjablonen die naar gebruikers moeten worden verzonden, in- en uitschakelen en wijzigen. Er zijn drie hoofdcategorieën e-mailsjablonen:

* Algemene e-mailsjablonen: deze e-mails worden geactiveerd voor algemene gebeurtenissen. Bijvoorbeeld een welkomstmelding wanneer een gebruiker zich voor het eerst aanmeldt.
* E-mailsjablonen die zijn gekoppeld aan een leerobject of -activiteit: deze e-mails worden naar studenten, auteurs of managers verzonden wanneer er een leeractiviteit is. Bijvoorbeeld e-mails die worden geactiveerd na inschrijving van de cursus, deelname aan de lesruimte, voltooiing van de cursus, enzovoort.
* Herinneringen en updates: deze e-mails worden geactiveerd wanneer gebruikers updates of herinneringen voor een gebeurtenis nodig hebben. Bijvoorbeeld een student die een herinnering voor een komende cursus ontvangt, of een beheerder die een e-mailmelding ontvangt voor een gedeeld rapport.

U kunt al deze e-mailmeldingen via het beheerdersdashboard inschakelen en configureren. Ga als volgt te werk om te leren hoe u e-mailsjablonen instelt:

1. Klik in het linkerdeelvenster op **[!UICONTROL ** E-mailsjablonen **.]**
1. Klik op een van de volgende tabbladen:**[!UICONTROL ** Algemeen **/** Leeractiviteit **/** Herinneringen en updates **.]** Laten we er bijvoorbeeld van uitgaan dat u op **[!UICONTROL ** Leeractiviteit **.]**
1. Klik op de schakelknop voor de activiteit die u wilt activeren. In dit voorbeeld, veronderstellen wij u klikt **[!UICONTROL ** Leerprogramma - Ingeschreven door beheerder/manager **.]**

   ![](assets/configure-email-templates-step3.png)

   Het systeem geeft het pop-upbericht &quot;Ingeschakeld met succes&quot; weer. Telkens wanneer een manager of beheerder een student voor een cursus inschrijft, ontvangt de student een e-mail van dit Learning Manager-account.

1. U kunt de standaard e-mailsjabloon wijzigen. Klik hiertoe op de gebeurtenis. In dit voorbeeld klikt u op **[!UICONTROL Leerprogramma - Ingeschreven door beheerder/manager.]**
1. In het dialoogvenster **[!UICONTROL Sjabloonvoorbeeld]** weergegeven, ziet u twee tabbladen: [!UICONTROL Student] en [!UICONTROL Manager].

   ![](assets/configure-email-templates-step5.png)

   Klik voor elk van deze tabbladen op de hoofdtekst van de e-mail om de inhoud te wijzigen. Als u de wijzigingen in de e-mailsjabloon wilt opslaan, klikt u op **[!UICONTROL Opslaan]**.

   Telkens wanneer een student door de manager of beheerder voor een cursus is ingeschreven, ontvangen de student en zijn manager een e-mailmelding.

   ***Opmerking: de wijzigingen zijn alleen van toepassing op de e-mailsjabloon die is gekoppeld aan de geselecteerde gebeurtenis.***

1. U kunt de account-URL of de handtekening niet wijzigen in de e-mailsjabloon. Als u de **[!UICONTROL Account-URL]** of **[!UICONTROL Handtekening]**, klikt u op **[!UICONTROL Instellingen]** tabblad. Op dit tabblad kunt u de e-mailbanner, e-mailhandtekening en de account-URL wijzigen.

   De link URL van het account wordt in alle e-mails weergegeven, vlak voor de handtekening. Voer de gewenste URL in en klik op **[!UICONTROL Opslaan]**. Deze URL is alleen zichtbaar voor de interne gebruikers.

   Voor E-mailbanner kunt u de kleur van de banner wijzigen door  **[!UICONTROL ** Bannerachtergrond **.]** U kunt een aangepaste afbeelding ook als een banner gebruiken door het **[!UICONTROL Aangepaste afbeelding]** gebruiken. Klikken  **[!UICONTROL Opslaan]** na het aanbrengen van de wijzigingen.

   ***Opmerking: de aangepaste afbeeldingsgrootte voor de e-mailbanner moet 1240 x 200 px zijn. Afbeeldingen die groter zijn dan de aanbevolen grootte, worden uitgesneden.***

   ***Learning Manager ondersteunt alleen .jpg-, .jpeg- en .png-bestandstypen voor e-mailbanners.***

   ![](assets/configure-email-templates-step6.png)

1. U kunt ook Optionele manager-e-mails inschakelen. Als u **[!UICONTROL Inschakelen]** selectievakje, wanneer een direct rapport een e-mail van dit Prime-account ontvangt, wordt de manager ook opgenomen in de mailinglijst.

   ***Opmerking: De instellingen op dit tabblad zijn van toepassing op alle sjablonen, globaal.***

### E-mailsjablonen configureren voor een leerobject {#configureemailtemplatesforalearningobject}

Naast het instellen van e-mailsjablonen op algemeen niveau, kunt u als beheerder ook e-mailsjablonen configureren voor een specifiek leerobject. In dit geval zijn wijzigingen die u aanbrengt in de e-mailsjabloon alleen van toepassing op dat leerobject.

Deze optie is ook beschikbaar voor auteurs, wanneer auteurs een leerobject instellen.

E-mailsjablonen configureren voor een leerobject:

1. Klik op de cursus, het leerprogramma of de certificering waarvoor u de e-mailsjabloon wilt configureren.
1. Klik in het linkerdeelvenster op **[!UICONTROL ** E-mailsjablonen **.]** Het systeem geeft een ****[!UICONTROL Sjabloonvoorbeeld]**** pop-upvenster.
1. Wijzig het onderwerp of de hoofdtekst van de e-mailsjabloon en klik op **[!UICONTROL **Opslaan**]**om de wijzigingen toe te passen.
1. Klik op **[!UICONTROL ** Origineel herstellen **.]**

### Gebruikers beperken in het ontvangen van e-mails {#restrictusersfromreceivingemails}

Als beheerder kunt u selecteren wie e-mails van Leermanager ontvangt en wie niet. U kunt dit bereiken met de ****[!UICONTROL Beperkte gebruiker]**** optie onder ****[!UICONTROL Instellingen]** **tab. Gebruikers kunnen aan deze lijst worden toegevoegd met hun naam, e-mail-ID of unieke gebruikers-ID. De gebruikers die onder deze optie worden vermeld, ontvangen geen e-mailcommunicatie van Leermanager.

## Uw accountinstellingen configureren {#configureyouraccountsettings}

Met Learning Manager kunt u een aantal accountinstellingen configureren, zoals basisinstellingen, feedbackinstellingen, algemene instellingen en instellingen voor het Studentendashboard. De volgende procedures vertellen u hoe te om elk van deze montages te vormen:

### Basisinstellingen configureren {#configurebasicsettings}

1. Klik op de startpagina van Learning Manager op ****[!UICONTROL Instellingen]****. Standaard geeft het systeem de pagina Basisinformatie weer met de standaardtaal en -locatievelden.
1. Klikken ****[!UICONTROL Wijzigen]**** in de rechterbovenhoek van de pagina om de basisinformatie te bewerken.
1. Configureer de volgende opties:

   * **Land**: Selecteer het land in deze vervolgkeuzelijst.
   * **Tijdzone**: Stel de juiste tijdzone in voor uw locatie.
   * **Landinstelling**: Selecteer de gewenste taal. Als u de taal in dit veld wijzigt, wordt de wijziging toegepast op alle gebruikers die deze toepassing gebruiken. Elke gebruiker kan echter afzonderlijk de taal van de voorkeur wijzigen.
   * **Het boekjaar begint bij**: Selecteer de maand waarin het boekjaar voor uw organisatie begint.



   ![](assets/configure-basic-settings-step3.png)

## Feedbackinstellingen configureren {#configurefeedbacksettings}

Met Learning Manager kunt u feedback voor een cursus verzamelen van studenten. Het is ook mogelijk om feedback over studenten te verzamelen met behulp van Learning Manager. Om feedback te vragen, moet u eerst L1- en L3-typen feedback configureren.

L3-feedback is de feedback die een manager geeft over een student. U kunt dit type feedback gebruiken om de prestaties van de studenten in de loop der tijd te volgen. L1-feedback is de feedback die een student over een cursus geeft. Met dit type feedback kan een beheerder rechtstreeks feedback over een cursus verzamelen.

Als beheerder kunt u de feedbackinstellingen globaal configureren. Hiervoor volgt u de volgende procedure:

1. Klik op de startpagina van Learning Manager op **[!UICONTROL Instellingen]**.
1. Klik in het linkerdeelvenster op **[!UICONTROL Algemeen]**.
1. Klik op de knop **[!UICONTROL L1-feedback]** tabblad. U ziet de opties voor het configureren van één verplichte vraag en verschillende optionele vragen. Dit zijn de vragen die een student bekijkt terwijl hij feedback geeft na het afronden van een cursus. De vragen zijn geformuleerd als instructies, zodat studenten hun antwoord op een schaal van 1 tot 5 kunnen selecteren.

   Het eerste deel van de L1-feedback is een verplichte vraag hoe een student deze cursus aan een vriend of collega kan aanbevelen.

   ***Opmerking: u kunt de verplichte vraag niet bewerken of wijzigen.***

   ![](assets/configure-feedbacksettings-step3.png)

1. Klik op de vragen in het ****[!UICONTROL Zelfgeplaatste cursussen]****, of ****[!UICONTROL Cursussen in lesruimte]****. Als u op een vraag klikt, kunt u de standaardvragen bewerken.



   ![](assets/configure-feedbacksettings-step4.png)

1. U kunt de standaardvragen in- of uitschakelen of de standaardvragen volledig aanpassen aan uw wensen. U kunt bijvoorbeeld de standaardvraag &quot;De trainingsvraag was relevant voor mij&quot; verwijderen en de vraag vervangen door &quot;Ik vond de training nuttig en relevant.&quot;
1. Nadat u de vragen voor studenten hebt beantwoord, kunt u de herinneringsinstellingen configureren. Standaard is er een bestaande herinnering, waarbij de toepassing na het voltooien van een cursus automatisch herinneringen naar studenten stuurt. Deze herinnering wordt ook ingesteld om de twee weken opnieuw te verschijnen totdat de student reageert. U kunt de bestaande herinnering wijzigen door op de herinnering te klikken of een nieuwe herinnering toevoegen.

   ![](assets/configure-feedbacksettings-step6.png)

1. Configureer de herinneringsinstellingen door de volgende opties in te vullen:

   * **Wanneer verzenden**: Geef op of u de feedbackaanvraag wilt verzenden na voltooiing van de cursus of na voltooiing van de cursus.
   * **Dagen na voltooiing**: Geef het aantal dagen op waarna u de feedbackaanvraag wilt verzenden. Dit veld is alleen zichtbaar als deze optie is geselecteerd ****[!UICONTROL Na voltooiing van de cursus]****.

   * **Herhaling**: Geef op of u de feedbackherinnering elke dag, elke week of elke maand wilt verzenden. U kunt ook opgeven voor hoeveel weken u de herinnering wilt verzenden.

1. Klik op het vinkje om de herinneringsinstellingen op te slaan.
1. Klik op ** nadat u alle feedbackinstellingen hebt voltooid [!UICONTROL **Opslaan**]**rechtsboven op de pagina.

## L3-feedback configureren: {#configurel3feedback}

L3-feedback bevat de vragen die naar de manager van een student worden verzonden nadat de student een cursus heeft voltooid. Met L3-feedback kan een beheerder wijzigingen bijhouden in het gedrag of de vaardigheid van een student in de loop der tijd. Klik op de pagina Feedback om deze feedback te configureren op de knop ****[!UICONTROL L3-feedback]**** tabblad. Je ziet er een, standaardvraag. De manager moet deze vraag beantwoorden met een beoordelingsschaal van vijf punten.

![](assets/configure-l3-feedback.png)

Net als bij L1-feedback kunt u de herinneringen voor L3-feedback configureren. U kunt de bestaande herinnering wijzigen of een nieuwe feedbackherinnering toevoegen.

Nadat u de feedbackvraag en de herinneringsinstellingen hebt voltooid, klikt u ****[!UICONTROL Opslaan]**** om uw instellingen toe te passen.

## Feedback op instantieniveau configureren {#configurefeedbackataninstancelevel}

De vorige procedure schetste de stappen om de feedbackinstellingen op globaal niveau te configureren. Dat wil zeggen dat de instellingen worden toegepast op alle cursussen. Naast deze algemene vragen kunt u als beheerder of auteur extra L1- en L3-feedbackvragen op instantieniveau configureren.

De feedbackinstellingen op instantieniveau configureren:

1. Klik op de startpagina van Learning Manager op **[!UICONTROL Cursussen]**.
1. Houd de muis boven de cursus waarin u de feedbackinstellingen wilt configureren. Klikken [!UICONTROL **Cursus weergeven**.]

   ![](assets/configure-feedbackataninstancelevel.png)

1. Klik op de pagina met cursusgegevens op **[!UICONTROL Standaardinstellingen voor instanties]** in de sectie Configureren.
1. In het dialoogvenster [!UICONTROL **Taal**] de taal waarin u de feedbackvragenlijst wilt weergeven.
1. Schakel de L1-reactiefeedback in als u om feedback van studenten wilt vragen. In deze sectie kunt u maximaal twee vragen toevoegen. Leerlingen kunnen deze vragen beschrijvende antwoorden geven.
1. Selecteer de **[!UICONTROL Verplicht maken]** Schakel het selectievakje in als u een of beide vragen verplicht wilt stellen.
1. Selecteer de **[!UICONTROL Vragenlijst direct na voltooiing van de cursus weergeven]** als u wilt dat studenten de feedbackvragenlijst direct kunnen bekijken nadat ze de cursus hebben voltooid.

   ![](assets/configure-feedbackataninstancelevel-step7.png)

1. De L3-feedback over gedragswijziging op instantieniveau configureren ****[!UICONTROL Inschakelen]**** de L3-feedback. De toepassing geeft een vooraf gedefinieerde, verplichte vraag en een lege vraag weer waar u een vraag naar keuze kunt invoeren.
1. Voor de vooraf gedefinieerde vraag over de verbetering van de student na het volgen van de cursus, heeft het antwoord de Likert-schaal-indeling. Dat wil zeggen dat managers een optie moeten kiezen op een schaal van sterk overeenkomen met sterk afwijzend.
1. Geef de tweede vraag voor de manager op. Managers kunnen een beschrijvend antwoord op deze vraag geven.
1. Selecteer de ****[!UICONTROL Verplicht maken]**** Schakel het selectievakje in als u de tweede vraag verplicht wilt stellen.

   ![](assets/configure-feedbackataninstancelevel-step11.png)

1. Configureer desgewenst de herinneringsinstellingen op instantieniveau. Als u hier geen herinneringsinstellingen configureert, worden de algemene herinneringsinstellingen automatisch toegewezen.
1. Klik op ** nadat u de feedbackvragen en de herinneringsinstellingen hebt voltooid [!UICONTROL **Opslaan**]**om uw instellingen toe te passen.

   ***Opmerking: feedbackinstellingen zijn niet van toepassing op certificeringen.***

## Algemene instellingen configureren {#configuregeneralsettings}

Met de algemene instellingen in Leerbeheer kunnen beheerders algemene instellingen configureren die van invloed zijn op andere functies in de toepassing. U kunt bijvoorbeeld algemene instellingen gebruiken om op te geven of cursuseffectiviteit zichtbaar kan worden gemaakt voor studenten. De algemene instellingen configureren:

1. Klik op de startpagina van Learning Manager op ****[!UICONTROL Instellingen]****.
1. Klik in het linkerdeelvenster op ****[!UICONTROL Algemeen]****.
1. Op de pagina Algemene instellingen kunt u de volgende opties configureren:

   Voor al deze opties is de functie waarop elke optie betrekking heeft, verschillend. We kunnen desgewenst kruisverwijzingen naar elk van de gedetailleerde functies geven.

   * **Cursuseffectiviteit tonen**: Schakel deze optie in als u wilt dat studenten de effectiviteit van een cursus op de titel van de cursus zien.
   * **Module herstellen, optie**: Schakel deze optie in als u studenten de mogelijkheid wilt geven een module opnieuw in te stellen. Studenten kunnen hun modules dan opnieuw instellen als ze niet zijn geslaagd of als ze de module gedeeltelijk hebben voltooid en opnieuw willen beginnen.
   * **Cursusmoderatie**: Schakel deze optie in als u wilt dat de wijzigingen in een cursus worden goedgekeurd door een beheerder voordat de wijzigingen zichtbaar zijn voor studenten.
   * **Discussieboard**: Schakel deze optie in als u wilt dat studenten de discussieboards voor cursussen kunnen bekijken en eraan kunnen deelnemen. Als u de **Discussieboard** kunnen studenten en docenten opmerkingen voor cursussen plaatsen. Als de instellingen op cursusniveau echter aangeven dat deze functie niet is geselecteerd, hebben de instellingen op cursusniveau voorrang op de beheerdersinstellingen.

   * **Optie Vaardigheden verkennen**: Schakel deze optie in als u wilt dat studenten de vaardigheden van collega&#39;s en leidinggevenden verkennen.
   * **Unieke ID&#39;s voor leerobjecten**: Schakel deze optie in als u auteurs de mogelijkheid wilt geven unieke id&#39;s toe te voegen aan leerobjecten.
   * **Cataloguslijst tonen**: Schakel deze optie in als u wilt dat studenten alle beschikbare catalogi zien. Met deze optie kunnen studenten hun leerobjectlijst verfijnen.



   ![](assets/configure-generalsettings-step3.png)

## Studentendashboardinstellingen configureren {#configurelearnerdashboardsettings}

Studentendashboard in Leermanager stelt studenten in staat hun verplichte en aanbevolen cursussen los van hun prestaties, vaardigheden en aankondigingen te bekijken. Beheerders kunnen bepalen hoe dit Studentendashboard moet worden weergegeven door de instellingen voor het Studentendashboard te configureren. Met deze instellingen kunnen beheerders de widgets instellen op de studentenpagina. Deze instellingen bepalen ook hoe en waar de widgets op het Studentendashboard worden geplaatst. Als beheerder kunt u een voorvertoning van de schermindeling van het Studentendashboard bekijken voordat u de instellingen toepast.

1. Klik op de startpagina van Learning Manager op **[!UICONTROL Instellingen]**.
1. Klik in het linkerdeelvenster op **[!UICONTROL ** Studentendashboard **.]**
1. Selecteer de widgets die u wilt inschakelen. Als u een widget deselecteert, wordt de widget direct uit de voorvertoning verwijderd. Studenten kunnen deze widget niet op hun dashboard zien.
1. Klikken ****[!UICONTROL Opslaan]**** om de instellingen toe te passen

   ![](assets/configure-learnerdashboardsettings-step4.png)

1. Klik op **[!UICONTROL Standaardinstellingen herstellen.]** In dit geval worden alle widgets behalve **[!UICONTROL Welkom en Sticky-aankondigingen]** zijn zichtbaar.

   ***Zelfs nadat u de instellingen voor het Studentendashboard hebt ingeschakeld, kunnen studenten widgets in hun respectieve dashboards wijzigen en verplaatsen.***

