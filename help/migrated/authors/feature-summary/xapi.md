---
jcr-language: en_us
title: xAPI in Learning Manager
description: De Experience API (xAPI) is een e-learningsoftwarespecificatie waarmee leerinhoud en leersystemen met elkaar kunnen communiceren op een manier die alle soorten leerervaringen opslaat en bijhoudt.
source-git-commit: 0fabd369e70e15ba22fead0177a24aafd851d88d
workflow-type: tm+mt
source-wordcount: '755'
ht-degree: 0%

---



# xAPI in Learning Manager

## Wat is xAPI? {#whatisxapi}

De Experience API (xAPI) is een e-learningsoftwarespecificatie waarmee leerinhoud en leersystemen met elkaar kunnen communiceren op een manier die alle soorten leerervaringen opslaat en bijhoudt. Leerervaringen worden vastgelegd in een LRS (Learning Record Store). LRS’s kunnen bestaan binnen traditionele LMS’s of op zichzelf.

Zie voor meer informatie over xAPI:  [https://github.com/adlnet/xAPI-Spec](https://github.com/adlnet/xAPI-Spec).

## Hoe ondersteunt Learning Manager xAPI? {#howdoescaptivateprimesupportxapi}

Learning Manager heeft een ingebouwde Learning Record Store. Dit LRS heeft de volledige mogelijkheid om xAPI-statements te accepteren van inhoud die is gehost in Learning Manager. Het accepteert zelfs xAPI-statements die door derden worden gegenereerd. Deze xAPI-statements worden opgeslagen in Learning Manager en kunnen vervolgens buiten Learning Manager worden geëxporteerd om te worden weergegeven in elk extern datawarehuisvestingssysteem.

## Wanneer gebruikt u xAPI? {#whendoyouusexapi}

Er is steeds meer behoefte aan het vastleggen van leerervaringen van de eindgebruiker die zich uitstrekken over meerdere systemen.  Het is ook nodig om de exacte betrokkenheid van de student bij trainingsinhoud te volgen. Het gaat verder dan Start, In bewerking en Voltooiing (de enige kenmerken die worden vastgelegd door SCORM).

## xAPI gebruiken in Leerbeheer {#usingxapiinprime}

## Uw toepassing instellen {#setupyourapplication}

1. Meld u aan als integratiebeheerder. Selecteren **[!UICONTROL Toepassingen]** > **[!UICONTROL Registreren]**.

   ![](assets/appregistration.png)

1. Registreer een nieuwe toepassing.

   ![](assets/appregistration.png)

1. Bepaal het bereik voor de toepassing.

   * Als **[!UICONTROL xAPI-lees- en schrijftoegang voor de beheerdersrol]** is ingeschakeld, kan de beheerder xAPI-statements en -documenten plaatsen en ophalen.
   * Als **[!UICONTROL xAPI-lees- en schrijftoegang studentrol]** is ingeschakeld, kan de beheerder xAPI-statements en -documenten plaatsen en ophalen.

1. Wijzigingen opslaan. Je krijgt je ontwikkelaars-ID en -geheim.

**Eindpunten**:

Klik op de onderstaande koppeling om het xAPI-swagerdocument te bekijken:

[https://learningmanagereu.adobe.com/docs/primeapi/xapi/](https://learningmanagereu.adobe.com/docs/primeapi/xapi/)

Opmerking: xAPI-versie die wordt ondersteund in Learning Manager is 1.0.3.

## API-verificatie {#apiauthentication}

De xAPI van Learning Manager gebruikt het OAuth 2.0-framework om uw clienttoepassingen te verifiëren en autoriseren. Zodra u uw toepassing registreert, kunt u clientId en clientSecret krijgen. De URL ophalen wordt in de browser gebruikt omdat deze de gebruikers van de Leermanager verifieert met behulp van hun vooraf geconfigureerde accounts zoals SSO, Adobe ID.

```
GET https://learningmanager.adobe.com/oauth/o/authorize?client_id=<Enter your clientId>&redirect_uri=<Enter a url to redirect to>&state=<Any String data>&scope=<admin:xapi or learner:xapi>&response_type=CODE.
```

## xAPI-statements bijhouden als LO van Learning Manager {#trackingxapistatementsasprimelo}

Als auteur kunt u nu de xAPI-module kiezen terwijl u cursussen maakt om de gebruikerservaring buiten Leerbeheer te volgen. U kunt deze functie bijvoorbeeld gebruiken om de activiteiten te evalueren van gebruikers op een extern platform dat wordt gebruikt voor het volgen van cursussen.

1. Tijdens het maken van **[!UICONTROL Activiteitenmodule]**, in de **[!UICONTROL Type]**gebruiken, selecteert u in het pop-upmenu  **[!UICONTROL xAPI-module.]**

   ![](assets/xapimodulecreation.png)

1. U wordt gevraagd een IRI op te geven. Indien niet beschikbaar, genereert Leermanager er automatisch een.

   IRI voor een activiteit is uniek in een account. Dat betekent dat twee modules in Learning Manager niet dezelfde IRI kunnen hebben. In de volgende gevallen wordt een nieuwe IRI gegenereerd:

   * Wanneer een cursus met xAPI-module wordt gedeeld tussen accounts.
   * Wanneer een certificering met xAPI-module terugkeert



   Een xAPI-instructie met de vermelde IRI wordt bijgehouden in de bovenstaande module en wordt weergegeven in de rapporten van de Learning Manager.

1. Ga naar de pagina Activiteitenmodule om de automatisch gegenereerde IRI te kopiëren.
1. Publiceer de module.

**Opmerkingen:**

* Leerbeheer ondersteunt momenteel alleen mbox als id. Andere ID&#39;s, zoals mboz_sha1, openid, account, worden niet ondersteund.

* De stateId en profileId zijn een UUID wanneer ze worden gebruikt met Learning Manager.
* PUT request does not overwrite the document for xAPIs agents/profile, activity/profile, and activity/state
* Niet-geïdentificeerde groep wordt niet ondersteund in Actor.
* De parameter &quot;related_activities&quot; wordt niet ondersteund in de instructie GET.
* De parameters &#39;format=ids&#39; en &#39;format=canonical&#39; worden niet ondersteund in instructies GET.
* Het verwijderen van de xAPI-instructie maakt geen acties ongedaan die zijn uitgevoerd in Learning Manager toen de instructie werd geplaatst.

## Rapporten genereren {#generatereports}

xAPI-rapporten kunnen worden gegenereerd als Excel-rapporten. Als beheerder opent u **[!UICONTROL Rapporten]** > **[!UICONTROL Excel-rapporten]** > **[!UICONTROL xAPI-activiteitsrapport]**.

Het gedownloade rapport haalt alle informatie op die door de student en beheerder voor een bepaalde instructie is geplaatst.

Dezelfde rapporten kunnen worden gegenereerd/gepland met behulp van FTP- en Box-connectoren voor elke integratie met derden. Voer de volgende stappen uit:

Meld u aan als integratiebeheerder > FTP/Box-connector openen > xAPI-activiteitsrapport selecteren in het linkerdeelvenster > Kies om een rapport te plannen/genereren.

![](assets/xapischedule.png)

* Wanneer alleen de onbewerkte score wordt verzonden in een xAPI-instructie zonder maximale score, wordt de quizscore niet weergegeven in LT.

* Om de percentagescore op te halen in Learning Manager, worden geschaalde scores verzonden via xAPI.

## Voorbeeldrapport {#samplereport}

[Voorbeeld xAPI-rapport.](assets/xapireport8842560559890766717csv.zip)
