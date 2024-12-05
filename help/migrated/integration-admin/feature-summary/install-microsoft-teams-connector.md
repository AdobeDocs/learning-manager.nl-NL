---
description: Microsoft Teams-connector installeren in Adobe Learning Manager
jcr-language: en_us
title: Microsoft Teams-connector installeren in Adobe Learning Manager
contentowner: saghosh
exl-id: 68092187-ac69-4727-a3dc-f3047a1e164d
source-git-commit: 6192559436074c3270644850b202589961e7b81b
workflow-type: tm+mt
source-wordcount: '1138'
ht-degree: 17%

---

# Microsoft Teams-connector installeren in Adobe Learning Manager

## Overzicht

Microsoft Teams® is een permanent op chat gebaseerd samenwerkingsplatform dat volledig het delen van documenten, online vergaderingen, en andere eigenschappen voor bedrijfsmededelingen steunt.

Adobe Learning Manager maakt gebruik van een connector voor virtuele lesruimten die kan worden gebruikt om Microsoft Teams-vergaderingen te integreren met Learning Manager.

De Microsoft Teams-connector verbindt Learning Manager- en Microsoft Teams-systemen om automatische synchronisatie van virtuele vergaderingen mogelijk te maken. Hier volgt een lijst met de mogelijkheden van de Microsoft Teams-connector:

**de virtuele zittingen van de opstelling gebruikend Microsoft Teams**

Deze connector helpt uw Adobe Learning Manager-account te integreren met uw Microsoft Teams-account. Na de integratie kan een auteur in Learning Manager met de connector Microsoft Teams gebruiken als technologieserviceprovider voor de virtuele klassikale modules die in Learning Manager zijn gemaakt.

**sta Microsoft Teams toe om studenten voor authentiek te verklaren wanneer het ingaan van virtuele klas**

Deze connector helpt de organisator van vergaderingen van Microsoft Teams vanuit Leermanager in te stellen tijdens het maken van een vergadering. De organisator van de vergadering kan de lobby beheren om toegang tot een vergadering te beperken of toe te staan en andere vergaderopties beheren die door Microsoft Teams worden geboden.

**de geautomatiseerde synchronisatie van de gebruikersvoltooiing van het gebruik**

Met het geautomatiseerde proces voor het synchroniseren van gebruikersvoltooide bewerkingen kan een beheerder van een leermanager automatisch de voltooiingsrecords en de opname-URL voor de vergadering van Microsoft Teams ophalen.

## Rollen in Microsoft Teams

Als u een vergadering met meerdere deelnemers organiseert, kunt u rollen aan elke deelnemer toewijzen, zodat een deelnemer kan weten wat hij/zij in de vergadering kan doen.

Er zijn twee rollen om van te kiezen: **presentator** en **aanwezige**.

Voor meer informatie, zie [ Rollen in een Vergadering van Teams Microsoft ](https://support.microsoft.com/nl-nl/office/rollen-in-een-teams-vergadering-c16fa7d0-1666-4dde-8686-0a0bfe16e019).

## De Microsoft Teams-connector instellen

>[!NOTE]
>
>Onderstaande items met de markering &lt;Developer/Optioneel> zijn optioneel en voornamelijk voor het instellen van huurders voor proefversies/ontwikkelaars met Microsoft voor het geval de gebruiker geen productietenant heeft. Deze zijn optioneel omdat ze meestal al door de beheerder van uw team zijn uitgevoerd.

## E5 Microsoft-account voor ontwikkelaars maken &lt;Developer/Optional>

U kunt tot de schakelaar van Microsoft Teams toegang hebben als u Office 365 E3 of Office 365 E5 hebt. De aanbevolen optie is Office 365 E5.

* Bezoek de [ pagina van de plannen van Microsoft ](https://www.microsoft.com/en-in/microsoft-365/enterprise/compare-office-365-plans?&amp;ef_id=CjwKCAjw8cCGBhB6EiwAgORey9Tjrae-dyAsBrzvXdVJ5WCcoQ55wySzUBMoo-EkPt7CoIqAtcWc0xoC9RcQAvD_BwE:G:s&amp;OCID=AID2100137_SEM_CjwKCAjw8cCGBhB6EiwAgORey9Tjrae-dyAsBrzvXdVJ5WCcoQ55wySzUBMoo-EkPt7CoIqAtcWc0xoC9RcQAvD_BwE:G:s&amp;lnkd=Google_O365SMB_Brand&amp;gclid=CjwKCAjw8cCGBhB6EiwAgORey9Tjrae-dyAsBrzvXdVJ5WCcoQ55wySzUBMoo-EkPt7CoIqAtcWc0xoC9RcQAvD_BwE). Op de webpagina kunt u een E3- of E5-account kopen of op Gratis uitproberen klikken.
* Vul de benodigde gegevens in en maak een account aan.

>[!NOTE]
>
>Het account moet de indeling `<username>@<company name>.onmicrosoft.com` gebruiken.

## Toepassing maken voor Microsoft Teams-connector

1. Bezoek het [ Microsoft Azure® portaal ](https://portal.azure.com/).
1. Meld u aan met de Microsoft E5-account die u in de vorige sectie hebt gemaakt.
1. Zoek naar **Azure Actieve Folder**.
1. Klik **[!UICONTROL Registraties van de Toepassing]**.
1. Klik **[!UICONTROL Nieuwe Registratie]**, ga de volgende details in, en registreer de toepassing:

   1. **Naam** - om het even welke naam van uw keus.
   1. **Gesteunde accounttypes** - Rekeningen in om het even welke organisatorische folder (Om het even welke Azure Actieve Folder - Multitenant).
   1. **Redirect URI (facultatief)** - Facultatief gebied dat op het antwoord URL wijst.

1. In de **kolom van de Hoofdzaak**, neem nota van volgende IDs, die verder tijdens de integratie zal worden gebruikt:

   1. **identiteitskaart van de Toepassing (cliënt)**
   1. **Folder (huurder) identiteitskaart**

1. Zoek naar cliëntgeloofsbrieven en klik **[!UICONTROL voeg een certificaat of een geheim]** toe.
1. Klik **[!UICONTROL Nieuw geheim van de Cliënt]** en voeg de volgende details toe:

   1. **Beschrijving** - ga om het even welke naam in.
   1. **vervalt** - reeks aan om het even welke waarde (geadviseerde waarde is 24 maanden. Zorg ervoor dat nieuwe clientreferenties worden gegenereerd zodra de vorige verlopen).

Let op het clientgeheim, dat tijdens de integratie verder wordt gebruikt.

## Toegang verkrijgen tot Microsoft Teams-connector

1. Bezoek het [ Microsoft Azure portaal ](https://portal.azure.com/).
1. Meld u aan met de Microsoft E5 die u eerder hebt gemaakt.
1. Zoek naar **Azure Actieve Folder**.
1. Klik **[!UICONTROL Registraties van de Toepassing]**.
1. Klik op de app die u in het vorige gedeelte hebt gemaakt.
1. Klik **[!UICONTROL API toestemmingen]**.
1. Klik **[!UICONTROL voeg een toestemming]** toe.
1. Selecteer **[!UICONTROL de Grafiek van Microsoft]** > **[!UICONTROL toestemmingen van de Toepassing]** en voeg de volgende toestemmingen toe:

   1. Chat.Read.All
   1. Directory.Read.All
   1. OnlineMeetingArtifact.Read.All
   1. OnlineMeetings.Read.All
   1. OnlineMeetings.ReadWrite.All
   1. User.Read.All
   1. OnlineMeetingRecording.Read.All

1. Klik {de beheerdertoegang van 0} verlenen voor Adobe ]**.**[!UICONTROL 
1. Klik **[!UICONTROL de rollen van de Toepassing]** > **[!UICONTROL creeer app rol]**.
1. Voer de volgende waarden in:

   1. **Naam van de Vertoning** - Naam van de API/Naam van de Toestemming (bijvoorbeeld, Calendars.ReadWrite).

   1. **Toegestane lidtypes** - specificeer zowel gebruikers als toepassingen (Gebruikers/Groepen + Toepassingen).

   1. **Waarde** - Naam van de API/Naam van de Toestemming (bijvoorbeeld, Calendars.ReadWrite).

   1. **Beschrijving** - Naam van de API/Naam van de Toestemming (bijvoorbeeld, Calendars.ReadWrite).

   1. **Wilt u deze toepassingsrol inschakelen?** - Selecteer dit selectievakje.

1. Herhaal de vorige stappen voor alle negen API/machtigingen die zijn toegevoegd.

## Vorm toegangsbeleid door manuscripten te gebruiken PowerShell

Om het beleid van de toepassingstoegang voor de schakelaar van Microsoft Teams te vormen door manuscripten in werking te stellen PowerShell, volg de procedure die in dit [ wordt beschreven document ](https://docs.microsoft.com/en-us/graph/cloud-communication-online-meeting-application-access-policy).

Hiermee wordt de connector ingeschakeld voor toegang tot Microsoft Teams-onlinevergaderingen.

>[!NOTE]
>
>In het bovenstaande document voert u Optionele stap 5 uit om ervoor te zorgen dat elke actieve gebruiker vanuit de ontwerpapp van de Learning Manager de rol van de organisator kan krijgen. Als deze stap niet wordt uitgevoerd, hebben gebruikers niet de vereiste toegangsmachtigingen om organisatoren te zijn en mislukt het maken van de vergadering (Microsoft API&#39;s beschouwen de organisator als de maker van een Teamvergadering).

## Microsoft Teams-connector instellen in Learning Manager

1. Meld u aan bij Leermanager als **integratiebeheerder** .

1. In de pagina van Connectors, selecteer de schakelaar van Microsoft Teams en klik **[!UICONTROL verbind]**.

1. Voer de volgende waarden in:

   1. **Naam van de Verbinding** - geef de naam die de auteur tijdens het creëren van de zitting zal zien.

   1. **identiteitskaart van de Microsoft Teams van de Trekker** - ga de eerder bepaalde waarde in.

   1. **Identiteitskaart van de Cliënt van Microsoft Teams** - ga de eerder bepaalde waarde in.

   1. **Geheim van de Cliënt van Microsoft Teams** - ga de eerder bepaalde waarde in.

   1. **E-mail van de Gebruiker van Admin van Microsoft Teams** - ga de standaard organisator e-mail in. Deze gebruiker (doorgaans een servicegebruiker) zou de maker van de vergadering zijn als er geen expliciete organisator is geselecteerd in de ontwerpapp voor leermanagers.

## Licenties toewijzen aan gebruikers &lt;Developer/Optional>

1. Bezoek [ https://admin.microsoft.com/#/homepage ](https://admin.microsoft.com/#/homepage).
1. Klik **[!UICONTROL Gebruikers]** > **[!UICONTROL Actieve Gebruikers]**.
1. Klik **[!UICONTROL Meer acties voor Gebruikers]** voor de gebruikers aan wie u toegang tot Microsoft Teams wilt verlenen.
1. Klik **[!UICONTROL leiden de Vergunningen van het Product]**.
1. Licentie inschakelen voor Office 365 E5 zonder audioconferentie.

<!--## Record a session

The API used for recording a session is a protected API. To access the API, you must request access from Microsoft. For more information, see this  [document](https://docs.microsoft.com/en-us/graph/teams-protected-apis).

In the document,

*"To request access to these protected APIs, complete the following  [request form](https://aka.ms/teamsgraph/requestaccess). We review access requests every Wednesday and deploy approvals every Friday, except during major holiday weeks in the U.S. Submissions during those weeks will be processed the following non-holiday week. To verify whether your request has been approved, test your application access on the next applicable Monday."*

For learners, the recording URL is displayed on the VC course overview page.

After 30 minutes of completing a course, the attendance for the learner gets marked. -->

## Veelgestelde vragen

+++Wie is een Organizer en een presentator?

Zie de [ documentatie ](https://support.microsoft.com/nl-nl/office/rollen-in-een-teams-vergadering-c16fa7d0-1666-4dde-8686-0a0bfe16e019) van Microsoft voor verschillende rollen en mogelijkheden die door Microsoft Teams worden gesteund.

+++

+++Moet een organisator een geregistreerde gebruiker zijn in zowel Learning Manager als Microsoft Teams?

Ja, de organisator moet ook een account hebben bij zowel Learning Manager als Microsoft Teams. Bovendien moet de organisator deel uitmaken van dezelfde Microsoft-tenant, die is geconfigureerd in de integratiebeheerapp.

+++

+++Moet een presentator een geregistreerde gebruiker zijn in zowel Learning Manager als Microsoft Teams?

Ja, de presentator moet ook deel uitmaken van zowel de Learning Manager als de Microsoft Teams. De presentator moet een Azure Active Directory-id hebben (kan onderdeel zijn van dezelfde tenant als de organisator of een deel van een andere tenant). Bovendien kunnen zelfs anonieme gebruikers (gebruikers die zich alleen met de gebruikersnaam aanmelden en geen deel uitmaken van Active Directory) tijdens de vergadering presentatoren maken door de organisator/bestaande presentatoren.

+++

+++Microsoft Teams heeft vergaderingen, webinars en live-gebeurtenissen. Wat ondersteunt de Teams-connector?

Momenteel ondersteunt de connector Teams alleen vergaderingen in Microsoft Teams. Voor meer informatie, zie dit [ document ](https://docs.microsoft.com/en-us/microsoftteams/quick-start-meetings-live-events).

+++
