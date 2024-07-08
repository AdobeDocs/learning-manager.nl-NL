---
jcr-language: en_us
title: Het Salesforce-pakket installeren
description: Learning Manager biedt een Salesforce-apppakket aan. Na de installatie en configuratie in SFDC kunnen verkoopmedewerkers hun trainingsactiviteiten uitvoeren in de SFDC-portal. Met deze app kunnen SFDC-gebruikers nieuwe trainingen verkennen, aanbevelingen bekijken en deze rechtstreeks in de SFDC-portal gebruiken. Gebruikers ontvangen de aankondigingen ook door beheerders in de vorm van mastheads rechtstreeks in de app binnen de SFDC-portal.
contentowner: saghosh
exl-id: 2b1c32e7-81af-4c13-a2bd-66684cde084e
source-git-commit: dffa765061b35d4559388e4120e51943768c8db8
workflow-type: tm+mt
source-wordcount: '1054'
ht-degree: 47%

---

# Het Salesforce-pakket installeren

## Overzicht

Learning Manager biedt een Salesforce-apppakket aan. Na de installatie en configuratie in SFDC kunnen verkoopmedewerkers hun trainingsactiviteiten uitvoeren in de SFDC-portal. Met deze app kunnen SFDC-gebruikers nieuwe trainingen verkennen, aanbevelingen bekijken en deze rechtstreeks in de SFDC-portal gebruiken. Gebruikers ontvangen de aankondigingen ook door beheerders in de vorm van mastheads rechtstreeks in de app binnen de SFDC-portal.

### Instellen in de Learning Manager-app.

1. Meld u als integratiebeheerder bij uw Learning Manager-beheerdersaccount aan.
1. Klik op **[!UICONTROL Applicaties]** > **[!UICONTROL Aanbevolen apps]**.
1. Klik op **[!UICONTROL Salesforce]**.
1. Noteer op de pagina van de Salesforce-app de toepassings-id (ook wel client-id genoemd) en het clientgeheim dat in de beschrijving wordt vermeld.
1. Klik op **[!UICONTROL Goedkeuren]** en de app moet zijn goedgekeurd.
1. Klik op **[!UICONTROL Bronnen]** voor ontwikkelaars > **[!UICONTROL Toegangstokens voor testen en ontwikkelen]**.
1. In de sectie OAuth-code ophalen moeten de Client-id en het bereik zijn ingesteld op - admin:read,admin:write. Klik op **[!UICONTROL Verzenden]**.
1. Voer bij Vernieuwingstoken ophalen de client-ID en het clientgeheim in. Klik op Verzenden ]**en let op**[!UICONTROL  de vernieuwingstoken.

### Account aanmaken in de Salesforce-app

1. Maak een account aan op de aanmeldingspagina van Salesforce. U moet een Salesforce-account maken in de Developer of Enterprise Edition.  [Aanmeldings-URL voor ontwikkelaars](https://developer.salesforce.com/signup). Zorg ervoor dat u de e-mail-id moet gebruiken om u te registreren voor Salesforce die u voor Learning Manager hebt gebruikt.
1. Verifieer uw account via de verificatie-e-mail.
1. Maak een wachtwoord aan en meld u aan bij Salesforce.
1. Noteer de Salesforce-URL na aanmelding (bijvoorbeeld site.lightning.force.com)

### Installeer het Learning Manager-pakket

Als u het pakket wilt installeren, moet u eerst het bestaande pakket in Salesforce verwijderen. Voordat u de installatie ongedaan maakt, moet u de instellingen inschakelen, zoals hieronder weergegeven. U moet deze instellingen toepassen, anders kunt u het pakket niet installeren.

![](assets/uninstall-package.png)

*Het pakket Learning Manager installeren*

>[!NOTE]
>
>De Adobe Learning Manager-app wordt alleen ondersteund in de Salesforce Lightning-weergave.

1. Start de  [Pakket-URL](https://test.salesforce.com/packaging/installPackage.apexp?p0=04tDb000000LRvP) van Learning Manager.
1. Klik op de **pagina Aanmelden** op **[!UICONTROL Aangepast domein gebruiken]**.

1. Voer de pakket-URL in en klik op **[!UICONTROL Doorgaan]**. Op de installatiepagina moet de optie Installeren voor alleen beheerders zijn geselecteerd. Wijzig deze optie niet.
1. Klik op **Ins tall (Install**). Nadat het pakket is geïnstalleerd, klikt u op **[!UICONTROL Gereed]**. U wordt naar de pagina Geïnstalleerde pakketten geleid en u kunt het geïnstalleerde Adobe Learning Manager-pakket zien.

1. Ga naar het startprogramma voor apps (naast Configuratie) en zoek naar Adobe Learning Manager.
1. Klik op **[!UICONTROL Configureren]** om de app te configureren.
1. Klik op **[!UICONTROL Nieuw]** en voeg de volgende gegevens toe:

   * **Configuratie:** Voer een naam naar keuze in.
   * **ClientID**: voer de waarde in die u uit de eerste sectie hebt verkregen.
   * **Clientsecret:** voer de waarde in die u hebt verkregen uit de eerste sectie.
   * **RefreshToken:** voer de waarde in die u hebt opgehaald uit de eerste sectie.
   * **LearningManagerBaseURL:** de URL van de site waar Learning Manager wordt gehost.
   * **Disable Redirect:** Omleiden naar de studentenstartpagina in Learning Manager uitschakelen.

>[!NOTE]
>
>U kunt slechts één configuratie maken. Als u nog een configuratie probeert toe te voegen, verschijnt er een foutmelding. In de configuratie kunt u het Salesforce-account met het studentenaccount verbinden.

### Instellingen voor externe site toevoegen

1. Klik in de rechterbovenhoek van de pagina op **[!UICONTROL Instellingen]**.
1. **Ga in Snel zoeken** naar instellingen voor externe site.
1. Klik op **[!UICONTROL Nieuwe externe site]**.
1. Voer de gegevens in:

   1. **Naam van externe site:** Voer een naam naar keuze in.
   1. **Remote Site URL:** De URL van de site waar Learning Manager wordt gehost.

1. Start Learning Manager.

### Voeg het Adobe-domein toe aan de vertrouwde Salesforce-URL&#39;s

Ga als volgt te werk om het Adobe-domein toe te voegen aan vertrouwde URL&#39;s:

1. Ga in de Salesforce-console naar **[!UICONTROL Setup]** > **[!UICONTROL Snel zoeken]**.
1. **[!UICONTROL Zoek naar vertrouwde URL&#39;s]** en selecteer **[!UICONTROL Nieuwe vertrouwde URL]**.
1. Typ een naam in het **[!UICONTROL veld API-naam]** .
1. Voeg de URL toe als `{}.adobe.com{*}`.
1. Selecteer alle selectievakjes in **CSP-aanwijzingen** en sla de wijzigingen op.
1. Bewerk de vernieuwingstoken van de Salesforce-app en sla deze op.
1. Start de Salesforce-app opnieuw.

### Schakel meldingen in voor de Learning Manager-app

1. Klik in de rechterbovenhoek op **Instellen**.
1. Zoek naar aangepaste meldingen.
1. Klik op **[!UICONTROL Nieuw]**.
1. Voer de volgende gegevens in:

   1. **Aangepaste naam melding:** LearningManagerNotification
   1. **API-naam:** LearningManagerNotification

1. Selecteer kanalen voor bureaublad **** en **mobiel** als ondersteunde kanalen.

1. Klik op **[!UICONTROL Opslaan]**.
1. Volg de onderstaande stappen om pushmeldingen voor mobiele apparaten in te schakelen:

   1. Installeer de mobiele Salesforce-app op uw mobiele telefoon.
   1. Meld u aan bij de app met uw gegevens.
   1. Ga naar **Instellingen** > Voor levering **van** meldingen.
   1. Voeg Salesforce toe voor iOS en Android.

### Deïnstalleer Learning Manager bij Salesforce

1. Ga in de Salesforce-app naar Geïnstalleerde pakketten.
1. Klik op **[!UICONTROL Verwijderen]**.

## Learning Manager configureren voor Salesforce-gebruikers

De Learning Manager-app is ook beschikbaar voor gebruikers die in een Salesforce-account aanwezig zijn. De beheerder van Salesforce kan gebruikers toevoegen op basis van de profielen. De Salesforce-profielen komen overeen met die in Learning Manager. Bijvoorbeeld beheerder, integratiebeheerder, docent enzovoort. De Salesforce-beheerder kan ook een aangepast profiel maken.

### Profiel

Als Salesforce-beheerder kunt u de profielen aan gebruikers toewijzen of een aangepast profiel maken.

>[!NOTE]
>
>De gebruikers moeten zowel aanwezig zijn in Salesforce als in Learning Manager.

![](assets/create-profile.png)

*Een profiel toewijzen aan een leerling*

Wanneer u een leerling toevoegt, moet u een specifiek profiel toewijzen aan de leerling. Ga vervolgens naar dat profiel en ververleent u de vereiste toegang.

Als u wilt dat studenten de app Learning Manager kunnen weergeven, moet u de app voor alle studenten inschakelen.

Vervolgens geeft u toegang tot de Learning Manager-app.

![](assets/permission-set.png)

*Machtigingen toevoegen voor toegang tot de app Learning Manager*

Wanneer u het pakket installeert, wordt er een nieuwe machtigingenset gemaakt, **Adobe Learning Manager User**. Ga naar de machtigingenset en voeg de gebruikers toe.

Selecteer de gebruikers en wijs de betreffende machtigingen toe. De studenten hebben nu toegang tot de Learning Manager-app.

Nu selecteert u een profiel, een standaard profiel van een gebruiker bijvoorbeeld, en klikt u op het profiel. Klik op **[!UICONTROL Bewerken]** en schakel in het **gedeelte Aangepaste app-instellingen** het selectievakje **Adobe Learning Manager** in. Hierdoor heeft de student toegang tot de app.

In de vervolgkeuzelijst **Startpagina voor studenten** selecteert u in de sectie **Aangepaste tabbladinstellingen** de optie **[!UICONTROL Standaard ingeschakeld]**.

U moet de app voor alle profielen zichtbaar maken.

Klik op **[!UICONTROL Opslaan]** , waarna de leerlingen die tot alle profielen behoren, toegang krijgen tot de app Leerbeheer.
