---
description: Microsoft Teams-connector installeren in Adobe Learning Manager
jcr-language: en_us
title: Microsoft Teams-connector installeren in Adobe Learning Manager
contentowner: saghosh
source-git-commit: ab6737e8b43222a6538921b0628a504a5f15859d
workflow-type: tm+mt
source-wordcount: '1258'
ht-degree: 24%

---



# Microsoft Teams-connector installeren in Adobe Learning Manager

## Overzicht

Microsoft® Teams® is een permanent op chat gebaseerd samenwerkingsplatform dat het delen van documenten, online vergaderingen en andere functies voor zakelijke communicatie volledig ondersteunt.

Adobe Leermanager maakt gebruik van een connector voor virtuele lesruimten die kan worden gebruikt om Microsoft Teams-vergaderingen te integreren met Learning Manager.

De Microsoft Teams-connector verbindt Learning Manager- en Microsoft Teams-systemen om automatische synchronisatie van virtuele vergaderingen mogelijk te maken. Hier volgt een lijst met de mogelijkheden van de Microsoft Teams-connector:

**Virtuele sessies instellen met Microsoft Teams**

Deze connector helpt uw Adobe Learning Manager-account te integreren met uw Microsoft Teams-account. Na de integratie kan een auteur in Learning Manager met de connector Microsoft Teams gebruiken als technologieserviceprovider voor de virtuele klassikale modules die in Learning Manager zijn gemaakt.

**Laat Microsoft Teams studenten verifiëren bij het betreden van de virtuele lesruimte**

Deze connector helpt de organisator van vergaderingen van Microsoft Teams vanuit Leermanager in te stellen tijdens het maken van een vergadering. De organisator van de vergadering kan de lobby beheren om toegang tot een vergadering te beperken of toe te staan en andere vergaderopties beheren die door Microsoft Teams worden geboden.

**Synchronisatie van geautomatiseerde gebruikersvoltooiing gebruiken**

Met het geautomatiseerde proces voor het synchroniseren van gebruikersvoltooide bewerkingen kan een beheerder van een leermanager automatisch de voltooiingsrecords en de opname-URL voor de vergadering van Microsoft Teams ophalen.

## Rollen in Microsoft Teams

Als u een vergadering met meerdere deelnemers organiseert, kunt u rollen aan elke deelnemer toewijzen, zodat een deelnemer kan weten wat hij/zij in de vergadering kan doen.

U kunt uit twee rollen kiezen: **presentator** en **deelnemer**.

Zie voor meer informatie  [Rollen in een teamvergadering - Microsoft](https://support.microsoft.com/nl-nl/office/rollen-in-een-teams-vergadering-c16fa7d0-1666-4dde-8686-0a0bfe16e019).

## De Microsoft Teams-connector instellen

>[!NOTE]
>
>Gemarkeerde items &lt;developer optional=&quot;&quot;> hieronder zijn optioneel en voornamelijk voor het instellen van huurders voor proefversies/ontwikkelaars met Microsoft voor het geval de gebruiker geen productiehuurder heeft. Deze zijn optioneel omdat ze meestal al door de beheerder van uw team zijn uitgevoerd.

## E5 Microsoft-account voor ontwikkelaars maken &lt;developer optional=&quot;&quot;>

U kunt tot de schakelaar van Microsoft Teams toegang hebben als u Office 365 E3 of Office 365 E5 hebt. De aanbevolen optie is Office 365 E5.

* Bezoek de [Microsoft plans page](https://www.microsoft.com/en-in/microsoft-365/enterprise/compare-office-365-plans?&amp;ef_id=CjwKCAjw8cCGBhB6EiwAgORey9Tjrae-dyAsBrzvXdVJ5WCcoQ55wySzUBMoo-EkPt7CoIqAtcWc0xoC9RcQAvD_BwE:G:s&amp;OCID=AID2100137_SEM_CjwKCAjw8cCGBhB6EiwAgORey9Tjrae-dyAsBrzvXdVJ5WCcoQ55wySzUBMoo-EkPt7CoIqAtcWc0xoC9RcQAvD_BwE:G:s&amp;lnkd=Google_O365SMB_Brand&amp;gclid=CjwKCAjw8cCGBhB6EiwAgORey9Tjrae-dyAsBrzvXdVJ5WCcoQ55wySzUBMoo-EkPt7CoIqAtcWc0xoC9RcQAvD_BwE) . Op de webpagina kunt u een E3- of E5-account kopen of op Gratis uitproberen klikken.

* Vul de benodigde gegevens in en maak een account aan.

>[!NOTE]
>
>De account moet de indeling gebruiken `<username>@<company name>.onmicrosoft.com`.

## Toepassing maken voor Microsoft Teams-connector

1. Bezoek de  [Microsoft Azure®-portal](https://portal.azure.com/).
1. Meld u aan met de Microsoft E5-account die u in de vorige sectie hebt gemaakt.
1. Zoeken naar **Azure Active Directory**.
1. Klikken **[!UICONTROL Toepassingsregistraties]**.
1. Klikken **[!UICONTROL Nieuwe registratie]**, voert u de volgende gegevens in en registreert u de toepassing:

   1. **Naam** - Elke gewenste naam.
   1. **Ondersteunde accounttypen** - Accounts in elke willekeurige organisatiemap (Any Azure Active Directory - Multitenant).
   1. **URI omleiden (optioneel)** - Optioneel veld dat de antwoordURL aangeeft.

1. In het dialoogvenster **Essentiële elementen** kolom, bekijk de volgende id&#39;s, die tijdens de integratie verder worden gebruikt:

   1. **Toepassings-id (client)**
   1. **Directory (tenant)-id**

1. Zoek naar clientreferenties en klik op **[!UICONTROL Een certificaat of geheim toevoegen]**.
1. Klikken **[!UICONTROL Nieuw clientgeheim]** en voeg de volgende details toe:

   1. **Beschrijving** - Voer een willekeurige naam in.
   1. **Verloopt** - Stel dit in op een waarde (aanbevolen waarde is 24 maanden. Zorg ervoor dat nieuwe clientreferenties worden gegenereerd zodra de vorige verlopen).

Let op het clientgeheim, dat tijdens de integratie verder wordt gebruikt.

## Toegang verkrijgen tot Microsoft Teams-connector

1. Bezoek de  [Microsoft Azure-portal](https://portal.azure.com/).
1. Meld u aan met de Microsoft E5 die u eerder hebt gemaakt.
1. Zoeken naar **Azure Active Directory**.
1. Klikken **[!UICONTROL Toepassingsregistraties]**.
1. Klik op de app die u in het vorige gedeelte hebt gemaakt.
1. Klikken **[!UICONTROL API-machtigingen]**.
1. Klikken **[!UICONTROL Een machtiging toevoegen]**.
1. Selecteren **[!UICONTROL Microsoft Graph]** > **[!UICONTROL Toepassingsmachtigingen]** en voeg de volgende machtigingen toe:

   1. Chat.Read.All
   1. Directory.Read.All
   1. OnlineMeetingArtifact.Read.All
   1. OnlineMeetings.Read.All
   1. OnlineMeetings.ReadWrite.All
   1. User.Read.All

1. Klikken **[!UICONTROL Beheertoegang verlenen voor Adobe]**.
1. Klikken **[!UICONTROL Toepassingsrollen]** > **[!UICONTROL App-rol maken]**.
1. Voer de volgende waarden in:

   1. **Weergavenaam** - Naam van de API/machtigingsnaam (bijvoorbeeld Calendars.ReadWrite).

   1. **Toegestane lidtypen** - Geef zowel gebruikers als toepassingen op (gebruikers/groepen + toepassingen).

   1. **Waarde** - Naam van de API/machtigingsnaam (bijvoorbeeld Calendars.ReadWrite).

   1. **Beschrijving** - Naam van de API/machtigingsnaam (bijvoorbeeld Calendars.ReadWrite).

   1. **Wilt u deze toepassingsrol inschakelen?** - Selecteer dit selectievakje.

1. Herhaal de vorige stappen voor alle negen API/machtigingen die zijn toegevoegd.

## Vorm toegangsbeleid door manuscripten te gebruiken PowerShell

Om het beleid van de toepassingstoegang voor de schakelaar van Microsoft Teams te vormen door manuscripten in werking te stellen PowerShell, volg de procedure die in dit wordt beschreven  [document](https://docs.microsoft.com/en-us/graph/cloud-communication-online-meeting-application-access-policy).

Hiermee wordt de connector ingeschakeld voor toegang tot Microsoft Teams-onlinevergaderingen.

>[!NOTE]
>
>In het bovenstaande document voert u Optionele stap 5 uit om ervoor te zorgen dat elke actieve gebruiker vanuit de ontwerpapp van de Learning Manager de rol van de organisator kan krijgen. Als deze stap niet wordt uitgevoerd, hebben gebruikers niet de vereiste toegangsmachtigingen om organisatoren te zijn en mislukt het maken van de vergadering (Microsoft API&#39;s beschouwen de organisator als de maker van een Teamvergadering).

## Microsoft Teams-connector instellen in Learning Manager

1. Meld u aan bij Learning Manager als integratiebeheerder.

1. Selecteer in de pagina Connectors de connector Microsoft Teams en klik op **[!UICONTROL Verbinden]**.

1. Voer de volgende waarden in:

   1. **Verbindingsnaam** - Geef de naam die de auteur tijdens het maken van de sessie zal zien.

   1. **Microsoft Teams Tenant-id** - Voer de eerder vastgestelde waarde in.

   1. **Client-id Microsoft Teams** - Voer de eerder vastgestelde waarde in.

   1. **Microsoft Teams-clientgeheim** - Voer de eerder vastgestelde waarde in.

   1. **E-mailadres Microsoft Teams Admin-gebruiker** - Voer de standaardorganizer-e-mail in. Deze gebruiker (doorgaans een servicegebruiker) zou de maker van de vergadering zijn als er geen expliciete organisator is geselecteerd in de ontwerpapp voor leermanagers.

## Licenties toewijzen aan gebruikers &lt;developer optional=&quot;&quot;>

1. Bezoek [https://admin.microsoft.com/#/homepage](https://admin.microsoft.com/#/homepage).
1. Klikken **[!UICONTROL Gebruikers]** > **[!UICONTROL Actieve gebruikers]**.
1. Klikken **[!UICONTROL Meer handelingen voor gebruikers]** voor de gebruikers aan wie u toegang tot Microsoft Teams wilt verlenen.
1. Klikken **[!UICONTROL Productlicenties beheren]**.
1. Licentie inschakelen voor Office 365 E5 zonder audioconferentie.

## Een sessie opnemen

De API die wordt gebruikt voor het opnemen van een sessie is een beveiligde API. U moet Microsoft om toegang vragen voor toegang tot de API. Zie deze voor meer informatie  [document](https://docs.microsoft.com/en-us/graph/teams-protected-apis).

Uit het document:

*&quot;Voer de volgende handelingen uit om toegang tot deze beveiligde API&#39;s aan te vragen  [aanvraagformulier](https://aka.ms/teamsgraph/requestaccess). We beoordelen elke woensdag toegangsaanvragen en implementeren elke vrijdag goedkeuringen, behalve tijdens belangrijke vakantieweken in de VS. Inzendingen tijdens die weken worden verwerkt in de volgende week die niet in de vakantie valt. Als u wilt controleren of uw verzoek is goedgekeurd, test u de toegang tot uw toepassing op de volgende toepasselijke maandag.&quot;*

Voor studenten wordt de opname-URL weergegeven op de overzichtspagina van de VC-cursus.

Dertig minuten na het voltooien van een cursus wordt de aanwezigheid van de student gemarkeerd.

## Veelgestelde vragen

+++Wie is een Organizer en een presentator?

Zie de  [documentatie](https://support.microsoft.com/nl-nl/office/rollen-in-een-teams-vergadering-c16fa7d0-1666-4dde-8686-0a0bfe16e019) van Microsoft voor verschillende rollen en mogelijkheden die door Microsoft Teams worden ondersteund.

+++

+++Moet een organisator een geregistreerde gebruiker zijn in zowel Learning Manager als Microsoft Teams?

Ja, de organisator moet ook een account hebben bij zowel Learning Manager als Microsoft Teams. Bovendien moet de organisator deel uitmaken van dezelfde Microsoft-tenant, die is geconfigureerd in de integratiebeheerapp.

+++

+++Moet een presentator een geregistreerde gebruiker zijn in zowel Learning Manager als Microsoft Teams?

Ja, de presentator moet ook deel uitmaken van zowel de Learning Manager als de Microsoft Teams. De presentator moet een Azure Active Directory-id hebben (kan onderdeel zijn van dezelfde tenant als de organisator of een deel van een andere tenant). Bovendien kunnen zelfs anonieme gebruikers (gebruikers die zich alleen met de gebruikersnaam aanmelden en geen deel uitmaken van Active Directory) tijdens de vergadering presentatoren maken door de organisator/bestaande presentatoren.

+++

+++Microsoft Teams heeft vergaderingen, webinars en live-gebeurtenissen. Wat ondersteunt de Teams-connector?

Momenteel ondersteunt de connector Teams alleen vergaderingen in Microsoft Teams. Zie deze voor meer informatie  [document](https://docs.microsoft.com/en-us/microsoftteams/quick-start-meetings-live-events).

+++
