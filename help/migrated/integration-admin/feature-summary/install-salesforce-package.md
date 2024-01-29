---
jcr-language: en_us
title: Salesforce-pakket installeren
description: Learning Manager biedt een Salesforce App-pakket. Als de software eenmaal is geïnstalleerd en geconfigureerd in SFDC, kunnen verkoopmedewerkers hun trainingsactiviteiten uitvoeren in de SFDC-portal. Met deze app kunnen SFDC-gebruikers nieuwe trainingen verkennen, aanbevelingen bekijken en volgen, rechtstreeks in de SFDC-portal. Gebruikers ontvangen de aankondigingen die door beheerders worden verzonden in de vorm van mastheads rechtstreeks binnen de app in de SFDC-portal.
contentowner: saghosh
source-git-commit: ab6737e8b43222a6538921b0628a504a5f15859d
workflow-type: tm+mt
source-wordcount: '979'
ht-degree: 0%

---



# Salesforce-pakket installeren

## Overzicht

Learning Manager biedt een Salesforce App-pakket. Als de software eenmaal is geïnstalleerd en geconfigureerd in SFDC, kunnen verkoopmedewerkers hun trainingsactiviteiten uitvoeren in de SFDC-portal. Met deze app kunnen SFDC-gebruikers nieuwe trainingen verkennen, aanbevelingen bekijken en volgen, rechtstreeks in de SFDC-portal. Gebruikers ontvangen de aankondigingen die door beheerders worden verzonden in de vorm van mastheads rechtstreeks binnen de app in de SFDC-portal.

### Instellen in de app Learning Manager

1. Meld u als integratiebeheerder aan bij uw Leermanager-account.
1. Klikken **[!UICONTROL Toepassingen]** > **[!UICONTROL Aanbevolen apps]**.
1. Klikken **[!UICONTROL Salesforce]**.
1. Let op de toepassingspagina van Salesforce op de toepassings-id (ook wel client-id genoemd) en het clientgeheim dat in de beschrijving wordt vermeld.
1. Klikken **[!UICONTROL Goedkeuren]** en uw app moet zijn goedgekeurd.
1. Klikken **[!UICONTROL Bronnen voor ontwikkelaars]** > **[!UICONTROL Toegangstokens voor testen en ontwikkelen]**.
1. In de sectie OAuth Code ophalen moeten de client-id en het bereik worden ingesteld op - admin:read,admin:write. Klikken **[!UICONTROL Verzenden]**.
1. Voer bij Token Vernieuwen ophalen de client-id en het clientgeheim in. Klikken **[!UICONTROL Verzenden]** en noteer het vernieuwingstoken.

### Account maken in Salesforce-app

1. Maak een account op de aanmeldingspagina van Salesforce. U moet een Salesforce-account maken in de editie voor ontwikkelaars of ondernemingen.  [URL voor ontwikkelaarsaanmelding](https://developer.salesforce.com/signup). Zorg ervoor dat u de e-mail-ID gebruikt om u aan te melden voor Salesforce die u voor Leerbeheer hebt gebruikt.
1. Verifieer uw account via de verificatie-e-mail.
1. Maak een wachtwoord en meld u aan bij Salesforce.
1. Noteer de Salesforce-URL na aanmelding (bijvoorbeeld site.lightning.force.com)

### Leerbeheerpakket installeren

Als u het pakket wilt installeren, moet u eerst het bestaande pakket in Salesforce verwijderen. Voordat u de installatie ongedaan maakt, moet u de instellingen inschakelen, zoals hieronder wordt weergegeven. U moet deze instellingen toepassen, anders kunt u het pakket niet installeren.

![](assets/uninstall-package.png)

*Het pakket Leerbeheer installeren*

>[!NOTE]
>
>De app Adobe Learning Manager wordt alleen ondersteund in de Salesforce Lightning-weergave.

1. Start de  [Learning Manager-pakket-URL](https://nam04.safelinks.protection.outlook.com/?url=https%3A%2F%2Ftest.salesforce.com%2Fpackaging%2FinstallPackage.apexp%3Fp0%3D04t1k0000008YWn&amp;data=04%7C01%7Ckillamse%40adobe.com%7Cf588f553fc694d2edee108d9a5c74711%7Cfa7b1b5a7b34438794aed2c178decee1%7C0%7C0%7C637723097572585825%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=mhYKVdwvS4F7WPruy0Kvw%2FsqgWxzTQpaZJyEACu8CNw%3D&amp;reserved=0).
1. In het dialoogvenster **Aanmelden** pagina, klikken **[!UICONTROL Aangepast domein gebruiken]**.

1. Voer de URL van het pakket in en klik op **[!UICONTROL Doorgaan]**. Op de installatiepagina moet de optie Installeren voor alleen beheerders zijn geselecteerd. Wijzig deze optie niet.
1. Klikken **Inshoog**. Nadat het pakket is geïnstalleerd, klikt u op **[!UICONTROL Gereed]**. U wordt begeleid naar de pagina Geïnstalleerde pakketten en u kunt het geïnstalleerde pakket van Adobe Learning Manager zien.

1. Ga naar de App Launcher (naast Setup) en zoek naar Adobe Learning Manager.
1. Klik op **[!UICONTROL Configureren]**.
1. Klikken **[!UICONTROL Nieuw]** en voeg de volgende details toe:

   * **Configuratie:** Voer een naam van uw keuze in.
   * **ClientID**: Voer de waarde in die u in de eerste sectie hebt gekregen.
   * **ClientSecret:** Voer de waarde in die u in de eerste sectie hebt gekregen.
   * **Vernieuwingstoken:** Voer de waarde in die u in de eerste sectie hebt gekregen.
   * **LearningManagerBaseURL:** De URL van de site waarop Leerbeheer wordt gehost.
   * **Omleiding uitschakelen:** Omleiding naar de startpagina van de student in Leerbeheer uitschakelen.

>[!NOTE]
>
>U kunt slechts één configuratie maken. Als u een andere configuratie probeert toe te voegen, wordt er een foutbericht weergegeven. De configuratie wijst het Salesforce-account toe aan het studentenaccount.

### Externe site-instellingen toevoegen

1. Klik rechtsboven op de pagina op **[!UICONTROL Instellen]**.
1. In **Snel zoeken**, zoek naar instellingen voor externe site.
1. Klikken **[!UICONTROL Nieuwe externe site]**.
1. Voer de details in:

   1. **Naam externe site:** Voer een naam van uw keuze in.
   1. **URL externe site:** De URL van de site waarop Leerbeheer wordt gehost.

1. Leerbeheer starten.

### Meldingen inschakelen voor de app Leermanager

1. Klik rechtsboven op **Instellen**.
1. Zoek naar aangepaste meldingen.
1. Klikken **[!UICONTROL Nieuw]**.
1. Voer de volgende gegevens in:

   1. **Naam aangepaste melding:** LearningManagerNotification
   1. **API-naam:** LearningManagerNotification

1. Beide selecteren **Desktop** en **Mobiel** als ondersteunde kanalen.

1. Klikken **[!UICONTROL Opslaan]**.
1. Volg de onderstaande stappen om pushmeldingen in te schakelen voor mobiele apparaten:

   1. Installeer de mobiele Salesforce-app in uw mobiele telefoon.
   1. Meld u met uw referenties aan bij de app.
   1. Ga naar **Instellen** > **Leveringsinstellingen voor meldingen**.
   1. Voeg Salesforce toe voor iOS en Android.

### Leermanager verwijderen uit Salesforce

1. Ga in de Salesforce-app naar Geïnstalleerde pakketten.
1. Klikken **[!UICONTROL Verwijderen]**.

## Leerbeheer voor Salesforce-gebruikers configureren

De app Leermanager is ook beschikbaar voor gebruikers die aanwezig zijn in een Salesforce-account. De Salesforce-beheerder kan gebruikers toevoegen op basis van de profielen. De Salesforce-profielen zijn vergelijkbaar met de profielen in Leerbeheer. Bijvoorbeeld Beheerder, Integratiebeheerder, Docent, enzovoort. De Salesforce-beheerder kan ook een aangepast profiel maken.

### Profiel

Als Salesforce-beheerder kunt u de profielen toewijzen aan gebruikers of een aangepast profiel maken.

>[!NOTE]
>
>De gebruikers moeten zowel in Salesforce als in Leermanager aanwezig zijn.

![](assets/create-profile.png)

*Een profiel toewijzen aan een student*

Wanneer u een student toevoegt, moet u een specifiek profiel aan de student toewijzen. Ga dan naar dat profiel en verleen de vereiste toegang.

Studenten kunnen de app Leermanager alleen weergeven als u de app voor alle studenten inschakelt.

De volgende stap bestaat uit het verlenen van toestemming voor toegang tot de app Leermanager.

![](assets/permission-set.png)

*Machtigingen toevoegen om toegang te krijgen tot de app Learning Manager*

Wanneer u het pakket installeert, wordt een nieuwe machtigingenset gemaakt, **Adobe Leermanager-gebruiker**. Ga naar de machtigingenset en voeg de gebruikers toe.

Selecteer de gebruikers en wijs de toestemmingen dienovereenkomstig toe. De studenten hebben nu toegang tot de app Leermanager.

Selecteer nu een profiel, bijvoorbeeld Standaardprofiel van een gebruiker, en klik op het profiel. Klikken **[!UICONTROL Bewerken]** en in de **Aangepaste app-instellingen** schakelt u het selectievakje **Adobe Learning Manager**. Hierdoor is de app toegankelijk voor de gebruiker.

In het dialoogvenster **Aangepaste tabinstellingen** in de **Startpagina student** vervolgkeuzelijst, selecteer de optie **[!UICONTROL Standaard ingeschakeld]**.

U moet de app zichtbaar maken voor alle profielen.

Klikken **[!UICONTROL Opslaan]** en de studenten die tot alle profielen behoren, krijgen toegang tot de app Leermanager.
