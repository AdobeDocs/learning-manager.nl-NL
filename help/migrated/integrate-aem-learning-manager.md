---
jcr-language: en_us
title: Learning Manager integreren met AEM
description: 'Learning Manager is Learning Management System met een geïntegreerd Learning Content Management System. Gebruikers beheren hun leerinhoud door deze naar Learning Manager te uploaden, zodat Learning Manager het volgende uitvoert: versiebeheer, toewijzingen aan cursussen, het bepalen van de zichtbaarheid voor studenten, traceren van gevolgde cursussen en rapportage naar beheerders.'
contentowner: saghosh
exl-id: 61fae7bd-1703-4ed1-9bd9-07387d67a91c
source-git-commit: 45e9b9cd291e180a3d29d6635ec81bc362eb3e96
workflow-type: tm+mt
source-wordcount: '1082'
ht-degree: 45%

---

# Learning Manager integreren met AEM

Learning Manager is Learning Management System met een geïntegreerd Learning Content Management System. Gebruikers beheren hun leerinhoud door deze naar Learning Manager te uploaden, zodat Learning Manager het volgende uitvoert: versiebeheer, toewijzingen aan cursussen, het bepalen van de zichtbaarheid voor studenten, traceren van gevolgde cursussen en rapportage naar beheerders.

Er zijn echter gebruikers die hun inhoud in activabeheersystemen opslaan en beheren. De inhoud wordt dan opnieuw gebruikt voor diverse andere functies.

De diverse stroken in de Learner-app kunnen in de AEM-sites worden ingesloten. Elke student die zich aanmeldt op de AEM-site, ziet zijn of haar specifieke trainingsgegevens in deze stroken.

## Het inhoudspakket downloaden {#downloadthecontentpackage}

Het installatieprogramma wordt als een AEM-inhoudspakket verzonden. [***Download het pakket*** ](https://github.com/adobe/adobe-learning-manager-reference-site).

Het inhoudspakket is beschikbaar als ZIP-bestand en is compatibel met AEM 6.4 en AEM 6.5.

## Installeer het Learning Manager-component {#installcaptivateprimecomponent}

Installeer het Captivate Prime-inhoudspakket met AEM-pakketbeheer:

>[!NOTE]
>
>Voor informatie bij het installeren van pakketten, zie [***hoe te met Pakketten*** werken ](https://experienceleague.adobe.com/docs/experience-manager-65/administering/contentmanagement/package-manager.html?lang=en#how-to-work-with-packages).

1. Open AEM Package Manager als AEM-auteur.
1. Klik op de knop **[!UICONTROL Pakket uploaden]**.
1. Klik **[!UICONTROL doorbladeren]** en upload het inhoudspakket.
1. Klik op **[!UICONTROL Uploaden]**.
1. Als u het pakket hebt geüpload, installeert u het inhoudspakket door dit te selecteren en te klikken op **[!UICONTROL Installeren]**.

   ![](assets/install-package.jpg)

   *installeer het inhoudspakket*

## Het vernieuwingstoken genereren {#generatetherefreshtoken}

Voor de AEM-beheerder is een vernieuwingstoken vereist van het Learning Manager account. De integratiebeheerder van Learning Manager genereert het vernieuwingstoken.

1. Keur de uitgelichte app van de AEM-sites goed.

   Klik **[!UICONTROL Toepassingen]** > **[!UICONTROL Aanbevolen Apps]** > **[!UICONTROL Adobe Experience Manager - Plaatsen]**.

   ![](assets/launch-aem.jpg)

   *keur app* goed

1. Klik **[!UICONTROL Toepassingen]** > **[!UICONTROL Aanbevolen Apps]**, en open de AEM plaatstoepassing.

   Kopieer de toepassings-ID en de beschrijving.

1. Klik **[!UICONTROL de Middelen van de Ontwikkelaar]** > **[!UICONTROL Tokens van de Toegang]**.

   ![](assets/click-tokens.jpg)

   *produceer de toegangstokens*

1. Voer de volgende gegevens in:

   * Client-ID, dit is de toepassings-ID.
   * Client-geheim, dit staat in Beschrijving.

1. Haal de OAuth-code op. U moet de API van versie 2 gebruiken in de doorverwijzings-URI.
1. Klik **[!UICONTROL voorleggen]** en krijg het vernieuwingstoken.

## De widget in AEM configureren {#configurethewidgetinaem}

Voor de widgetconfiguratie vereist de AEM auteur alleen het vernieuwingstoken van de Learning Manager Integration-beheerder.

U kunt ook meerdere accountconfiguraties op meerdere pagina&#39;s instellen.

1. Klik **[!UICONTROL Hulpmiddelen]** > **[!UICONTROL Cloud Servicen]** > **[!UICONTROL het Leren de Configuratie van de Widget van de Manager]**.
1. Klik op **[!UICONTROL Maken]**.
1. Voer het vernieuwingstoken hier in. Stel de andere instellingen in.
1. Hostnaam moet voor EU-regio&#39;s worden gewijzigd in &quot;learningmanager&quot;.
1. Sla de configuratie op en sluit deze af.
1. Selecteer een configuratie en publiceer de configuratie.

## AEM-auteur {#aemauthor}

De AEM-auteur moet de component eerst toevoegen aan het AEM-sjabloon

Vervolgens kan de AEM-auteur het Adobe Learning Manager-component slepen en neerzetten en naar wens configureren.

De component Learning Manager vereist dat de configuratie die in de bovenstaande stap is gemaakt, wordt toegewezen aan de pagina.  De auteur kan de configuratie in kaart brengen door de Eigenschappen van de Pagina onder **[!UICONTROL Geavanceerde]** > **[!UICONTROL Configuratie]** > **[!UICONTROL Configuratie van de Wolk]** uit te geven en weg van configuratie te verstrekken. Op deze manier kan de auteur configuraties aanmaken voor meerdere Captivate Prime-accounts en elke account toewijzen aan een andere Sites-pagina. Als een configuratie niet aan de pagina is toegewezen, leest de component de configuratie van de bovenliggende pagina recursief totdat er een is gevonden.

## Student {#learner}

De student kan de cursussen op deze pagina volgen.

Om toegang te krijgen tot de Learning Manager-widget, moet de student aangemeld zijn als een AEM-gebruiker. Ook, zou het bezit **e-mail** in &quot;/profiel&quot;knoop van de lezer moeten aanwezig zijn:de knoop van de Gebruiker. Dit e-mailadres moet exact hetzelfde zijn als het e-mailadres in het Learning Manager-account.

De student kan de cursussen op deze pagina volgen.

De cursusvoortgang wordt ook opgeslagen.

De volgende widgets zijn beschikbaar:

1. Gamification
1. Studentenagenda
1. Sociale widget
1. Cataloguswidget
1. Mijn leermateriaal
1. Aanbeveling op basis van wat collega&#39;s leren
1. Aanbeveling door de beheerder
1. Aanbeveling op basis van interesses van student

Als er geen aanbevelingen zijn, is de widget leeg.

## Ondersteuning voor Skyline

Skyline is de cloudversie van AEM. U moet Skyline eerst installeren vanuit pakketbeheer. Als u de component Skyline in AEM wilt gebruiken, moet een gebruiker aanwezig zijn in het Leerbeheerdersaccount. Met andere woorden, het e-mailadres van de gebruiker moet in het account bestaan.

### Skyline implementeren

De stappen om Skyline te vormen worden vermeld in de [ reactie GitHub ](https://github.com/adobe/captivate-prime-aem-components).

## Mijn leerwidget

**[!UICONTROL Mijn het Leren]** widget staat u toe om opleiding van een specifieke of een reeks catalogi aan een gebruiker te tonen.

In de **[!UICONTROL sectie van Eigenschappen]** in de paginaeigenschappen, selecteer **[!UICONTROL Catalogus]** van de vermelde opties.

<!--![](assets/catalog-widget.png)-->

De catalogusopties bevatten de volgende opties:

* **[!UICONTROL Catalogus ids ]:** komma-gescheiden catalogusids waarvoor de opleiding moet worden getoond.
* **[!UICONTROL Soort ]:** de orde van de Soort voor de opleiding. De opties zijn: naam, datum, aanmaakdatum, datumIngeschreven, enzovoort.
* **[!UICONTROL Staat van de Student ]:** keert al opleiding terug die het volgende als ingeschreven filters gebruikt, begonnen, voltooid, en niet ingeschreven. De zoekresultaten worden niet weergegeven als de sorteeroptie dateEnrolled, dueDate of dateEnrolled is.
* **[!UICONTROL Naam van de Vaardigheid ]:** de vaardigheid die wordt gebruikt om nauwkeurige opleiding te filtreren.
* **[!UICONTROL naam van de markering ]:** De markering die wordt gebruikt om nauwkeurige resultaten te filtreren.

Hier volgen enkele aanvullende componenten die u kunt aanpassen:

**[!UICONTROL het Leren de Types van Objecten ]:** Filter volgens het type van het Leren Voorwerp. De ondersteunde typen zijn: cursus, certificering, jobAid en learningProgram.

In AEM is de titel van een kaart in een strip aanvankelijk leeg. Typ in eigenschappen de naam van de titel in widgets.html.

**Aanpassing**

U kunt het uiterlijk van de lay-out aanpassen met widgets.html. U kunt de weergave van de kaarten die worden weergegeven wijzigen en het thema aanpassen.

In de **[!UICONTROL Algemene sectie van Montages]**, kunt u de primaire en secundaire kleuren voor de kaarten kiezen en de eigenschappen specificeren om het thema aan te passen.

```
{ 
 "globalCssText":"@import url('https://fonts.googleapis.com/css2?family=Grandstander:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&family=Montserrat:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap');", 
 "fontNames":"Grandstander", 
 "cardLayout":{ 
 "cardLayoutName":"compact", 
 "cardPrimaryColor":"#376BA4", 
 "cardSecondaryColor":"#F98EB0", 
 "startedStateTextColor":"#ffffff", 
 "continueStateTextColor":"#ffffff", 
 "revisitStateTextColor":"#ffffff", 
 "startedStateColor":"#a0a0a0", 
 "continueStateColor":"#f9a122", 
 "revisitedStateColor":"#7fbc64", 
 "textPrimaryColor":"#ffffff", 
 "textSecondaryColor":"#d93f3f", 
 "navIconColor":"#a0a0a0" 
 } 
}
```

### LO-inschrijving van hogere volgorde negeren

Als **LO van de Hogere Inschrijving van de Orde** wordt toegelaten en een gebruiker direct in een het Leren Programma of Certificatie wordt ingeschreven, zullen de cursussen voor dat certificatie of Leerprogramma voor de gebruiker in widgets verschijnen.

Als het selectievakje is uitgeschakeld, worden de cursussen in het leerprogramma of de certificering waarvoor de gebruiker zich niet rechtstreeks heeft ingeschreven, niet weergegeven.

![](assets/higher-order-lo.png)

*Selecteer het selectievakje LO-inschrijving voor hogere volgorde negeren.

De instelling wordt dan toegepast op de widget.

### Beveiliging

De velden Client-ID en Client-geheim worden toegevoegd. Bovendien wordt het vernieuwingstoken gemaskeerd. Nadat een gebruiker de volledige configuratie heeft gemaakt, als de gebruiker de configuratie opnieuw opent om deze te bewerken, of als een andere gebruiker deze configuratie opent, wordt het vernieuwingstoken gemaskeerd.
