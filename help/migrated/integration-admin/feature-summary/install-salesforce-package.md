---
jcr-language: en_us
title: Het Salesforce-pakket installeren
description: Learning Manager biedt een Salesforce App-pakket. Na de installatie en configuratie in SFDC kunnen verkoopmedewerkers hun trainingsactiviteiten uitvoeren in de SFDC-portal. Met deze app kunnen SFDC-gebruikers nieuwe trainingen verkennen, aanbevelingen bekijken en deze rechtstreeks in de SFDC-portal gebruiken. Gebruikers ontvangen de aankondigingen die door beheerders worden verzonden in de vorm van mastheads rechtstreeks binnen de app in de SFDC-portal.
contentowner: saghosh
exl-id: 2b1c32e7-81af-4c13-a2bd-66684cde084e
source-git-commit: 25c4873f6d01c5832c213b6f225172f3dbcba1ee
workflow-type: tm+mt
source-wordcount: '1057'
ht-degree: 47%

---

# Het Salesforce-pakket installeren

## Overzicht

Learning Manager biedt een Salesforce App-pakket. Na de installatie en configuratie in SFDC kunnen verkoopmedewerkers hun trainingsactiviteiten uitvoeren in de SFDC-portal. Met deze app kunnen SFDC-gebruikers nieuwe trainingen verkennen, aanbevelingen bekijken en deze rechtstreeks in de SFDC-portal gebruiken. Gebruikers ontvangen de aankondigingen die door beheerders worden verzonden in de vorm van mastheads rechtstreeks binnen de app in de SFDC-portal.

### Instellen in de Learning Manager-app.

1. Meld u als integratiebeheerder bij uw Learning Manager-beheerdersaccount aan.
1. Klik **[!UICONTROL Toepassingen]** > **[!UICONTROL Aanbevolen Apps]**.
1. Klik **[!UICONTROL Salesforce]**.
1. Let op de toepassingspagina van Salesforce op de toepassings-id (ook wel client-id genoemd) en het clientgeheim dat in de beschrijving wordt vermeld.
1. Klik **[!UICONTROL goedkeuren]** en uw app moet met succes worden goedgekeurd.
1. Klik {de Middelen van de Ontwikkelaar 1} > **[!UICONTROL Tokens van de Toegang voor het Testen en Ontwikkeling]**.****
1. In de sectie OAuth Code ophalen moeten de client-id en het bereik worden ingesteld op - admin:read,admin:write. Klik **[!UICONTROL voorleggen]**.
1. Voer bij Vernieuwingstoken ophalen de client-ID en het clientgeheim in. Klik **[!UICONTROL voorleggen]** en neem nota van het vernieuwingstoken.

### Account aanmaken in de Salesforce-app

1. Maak een account aan op de aanmeldingspagina van Salesforce. U moet een Salesforce-account maken in de editie voor ontwikkelaars of ondernemingen.  [ de inschrijver URL van de Ontwikkelaar ](https://developer.salesforce.com/signup). Zorg ervoor dat u de e-mail-ID gebruikt om u aan te melden voor Salesforce die u voor Leerbeheer hebt gebruikt.
1. Verifieer uw account via de verificatie-e-mail.
1. Maak een wachtwoord aan en meld u aan bij Salesforce.
1. Noteer de Salesforce-URL na aanmelding (bijvoorbeeld site.lightning.force.com)

### Installeer het Learning Manager-pakket

Als u het pakket wilt installeren, moet u eerst het bestaande pakket in Salesforce verwijderen. Voordat u de installatie ongedaan maakt, moet u de instellingen inschakelen, zoals hieronder weergegeven. U moet deze instellingen toepassen, anders kunt u het pakket niet installeren.

![](assets/uninstall-package.png)

*installeer het Lerende pakket van de Manager*

>[!NOTE]
>
>De Adobe Learning Manager-app wordt alleen ondersteund in de Salesforce Lightning-weergave.

1. Lanceer het [ het pakket url van de Manager van het Leren (Reparatie M42 2) ](https://login.salesforce.com/packaging/installPackage.apexp?p0=04tDb000000LSlG).
1. In de **Login** pagina, klik **[!UICONTROL het Domein van de Douane van het Gebruik]**.
1. Ga het pakket URL in en klik **[!UICONTROL verdergaan]**. Op de installatiepagina moet de optie Installeren voor alleen beheerders zijn geselecteerd. Wijzig deze optie niet.
1. Klik **[!UICONTROL installeer]**. Zodra het pakket wordt geïnstalleerd, klik **[!UICONTROL Gedaan]**. U wordt naar de pagina Geïnstalleerde pakketten geleid en u kunt het geïnstalleerde Adobe Learning Manager-pakket zien.

1. Ga naar het startprogramma voor apps (naast Configuratie) en zoek naar Adobe Learning Manager.
1. Om app te vormen, klik **[!UICONTROL vormen]**.
1. Klik **[!UICONTROL Nieuw]** en voeg de volgende details toe:

   * **Configuratie:** Voer een naam naar keuze in.
   * **ClientID**: Ga de waarde in die u van de eerste sectie had verkregen.
   * **ClientSecret:** ga de waarde in die u van de eerste sectie had verkregen.
   * **RefreshToken:** ga de waarde in die u van de eerste sectie had verkregen.
   * **LearningManagerBaseURL:** URL van de plaats waar het Leren Manager wordt ontvangen.
   * **Disable Redirect:** Omleiden naar de studentenstartpagina in Learning Manager uitschakelen.

>[!NOTE]
>
>U kunt slechts één configuratie maken. Als u nog een configuratie probeert toe te voegen, verschijnt er een foutmelding. In de configuratie kunt u het Salesforce-account met het studentenaccount verbinden.

### Instellingen voor externe site toevoegen

1. In de hoger-juiste hoek van de pagina, klik **[!UICONTROL Opstelling]**.
1. In **Snelle Vondst**, onderzoek naar de Montages van de Verre Plaats.
1. Klik **[!UICONTROL Nieuwe Verre Plaats]**.
1. Voer de gegevens in:

   1. **Naam van externe site:** Voer een naam naar keuze in.
   1. **Remote Site URL:** De URL van de site waar Learning Manager wordt gehost.

1. Start Learning Manager.

### Het domein Adobe toevoegen aan door Salesforce vertrouwde URL&#39;s

Ga als volgt te werk om het domein van de Adobe toe te voegen aan vertrouwde URL&#39;s:

1. In de console Salesforce, ga naar **[!UICONTROL Opstelling]** > **[!UICONTROL Snelle Vondst]**.
1. Onderzoek naar **[!UICONTROL Vertrouwde URLs]** en selecteer **[!UICONTROL Nieuwe Vertrouwde URL]**.
1. Typ een naam op het **[!UICONTROL API gebied van de Naam]**.
1. Typ `*.adobe.com` in het veld URL.
1. Selecteer alle controledozen in **CSP Richtlijnen** en sla de veranderingen op.
1. Bewerk het vernieuwingstoken van de Salesforce-app en sla deze op.
1. Start de Salesforce-app opnieuw.

### Schakel meldingen in voor de Learning Manager-app

1. In de hoger-juiste hoek, klik **Opstelling**.
1. Zoek naar aangepaste meldingen.
1. Klik **[!UICONTROL Nieuw]**.
1. Voer de volgende gegevens in:

   1. **Naam van het Bericht van de Douane:** LearningManagerNotification
   1. **API Naam:** LearningManagerNotification

1. Selecteer zowel **Desktop** als **Mobiel** als Gesteunde kanalen.

1. Klik op **[!UICONTROL Opslaan]**.
1. Volg de onderstaande stappen om pushmeldingen voor mobiele apparaten in te schakelen:

   1. Installeer de mobiele Salesforce-app op uw mobiele telefoon.
   1. Meld u aan bij de app met uw gegevens.
   1. Ga naar **Opstelling** > **Montages van de Levering van het Bericht**.
   1. Voeg Salesforce toe voor iOS en Android.

### Deïnstalleer Learning Manager bij Salesforce

1. Ga in de Salesforce-app naar Geïnstalleerde pakketten.
1. Klik **[!UICONTROL Uninstall]**.

## Learning Manager configureren voor Salesforce-gebruikers

De Learning Manager-app is ook beschikbaar voor gebruikers die in een Salesforce-account aanwezig zijn. De beheerder van Salesforce kan gebruikers toevoegen op basis van de profielen. De Salesforce-profielen komen overeen met die in Learning Manager. Bijvoorbeeld beheerder, integratiebeheerder, docent enzovoort. De Salesforce-beheerder kan ook een aangepast profiel maken.

### Profiel

Als Salesforce-beheerder kunt u de profielen aan gebruikers toewijzen of een aangepast profiel maken.

>[!NOTE]
>
>De gebruikers moeten zowel in Salesforce als in Leermanager aanwezig zijn.

![](assets/create-profile.png)

*wijs een profiel aan een student toe*

Wanneer u een student toevoegt, moet u een specifiek profiel aan de student toewijzen. Ga dan naar dat profiel en verleen de vereiste toegang.

Studenten kunnen de app Leermanager alleen weergeven als u de app voor alle studenten inschakelt.

Vervolgens geeft u toegang tot de Learning Manager-app.

![](assets/permission-set.png)

*voeg toestemmingen toe om tot app van de Leermanager toegang te hebben*

Wanneer u het pakket installeert, wordt een nieuwe toestemmingsreeks gecreeerd, **Gebruiker van Adobe Learning Manager**. Ga naar de machtigingenset en voeg de gebruikers toe.

Selecteer de gebruikers en wijs de betreffende machtigingen toe. De studenten hebben nu toegang tot de Learning Manager-app.

Nu selecteert u een profiel, een standaard profiel van een gebruiker bijvoorbeeld, en klikt u op het profiel. Klik **[!UICONTROL uitgeven]** en in de **sectie van de Montages van de Toepassing van de Douane**, laat de controle-doos **Adobe Learning Manager** toe. Hierdoor heeft de student toegang tot de app.

In de vervolgkeuzelijst **Startpagina voor studenten** selecteert u in de sectie **Aangepaste tabbladinstellingen** de optie **[!UICONTROL Standaard ingeschakeld]**.

U moet de app voor alle profielen zichtbaar maken.

Klik **[!UICONTROL sparen]** en de studenten die tot alle profielen behoren zullen tot de app van de Leermanager toegang hebben.
