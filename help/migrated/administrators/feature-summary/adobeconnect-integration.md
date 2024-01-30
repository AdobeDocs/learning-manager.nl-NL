---
jcr-language: en_us
title: Adobe Connect-integratie
description: Auteurs kunnen virtuele klassikale cursussen maken met Adobe Connect tijdens het maken van cursussen. U moet contact opnemen met de beheerder van uw organisatie om Adobe Connect voor uw Learning Manager-account in te schakelen.
contentowner: jayakarr
source-git-commit: 0052ccb2f5a8f9617bca2c7bad91c0cd18338b66
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 70%

---



# Adobe Connect-integratie

Beheerders van een organisatie kunnen de instellingen van het Learning Manager-account configureren om Adobe Connect-integratie mogelijk te maken.

## Adobe Connect configureren {#configureadobeconnect}

1. Klik in Beheerdersaanmelding op **[!UICONTROL Instellingen]** in het linkerdeelvenster om de basisinformatie over uw bedrijf te bekijken. Klikken **[!UICONTROL Adobe Connect]** in het linkerdeelvenster.

   ![](assets/left-pane.png)

   *Adobe Connect selecteren in het linkerdeelvenster*

1. Klikken **[!UICONTROL Nu configureren]** link in **[!UICONTROL Adobe Connect-configuratie]** sectie.

   <!--![](assets/configure-now-connect.png)-->

1. Geef de Adobe Connect-domeinnaam van uw bedrijf en meld u aan met uw bedrijfsgegevens.

   ![](assets/adobeconnect-config.png)

   *Domeinnaam en referenties toevoegen*

   Een voorbeeld van een Adobe Connect-URL: mycompany.adobeconnect.com\
   U moet de e-mail-ID van de beheerder van het Connect-account van de Adobe opgeven.

   Alleen door Adobe gehoste accounts worden ondersteund in Learning Manager. Voorbeeld; &#39;.adobeconnect.com&#39;.

1. Klikken **[!UICONTROL Integreren].**

   Nadat de e-mail-ID is geverifieerd, geeft Learning Manager het bericht weer als Connect is geïntegreerd. U kunt uw virtuele klassikale cursussen automatisch bekijken met behulp van Adobe Connect.

   De Adobe Connect-accountbeheerder moet de algemene gebruiksvoorwaarden van Adobe Connect accepteren. Als deze niet worden geaccepteerd, mislukt uw aanmeldpoging mogelijk. Meld u na het aanmaken van het Adobe Connect-account eenmaal aan op het account. Bij de eerste aanmeldpoging verschijnt er een pagina met de Algemene voorwaarden.

   <!--![](assets/mail-confirmation.png)-->

## Sessie-informatie voor virtueel klaslokaal toevoegen {#addvirtualclassroomsessioninformation}

Als de auteur van een virtuele klassikale cursus de sessie-informatie niet heeft verstrekt, dan kan de beheerder de sessiedetails opnemen.

Klik op de naam van de VC-cursus in Beheerdersaanmelding. Klikken **[!UICONTROL Instanties]** in het linkerdeelvenster en klik op **[!UICONTROL Sessiedetails]**.  Klik op het pictogram Bewerken in de rechterhoek van de pagina Sessiedetails om de sessiegegevens toe te voegen.

![](assets/session-creation-admin.png)

*Sessiegegevens van virtuele lesruimten toevoegen*

Met de integratie van Adobe Learning Maanger en Adobe Connect voor het maken van virtuele klassikale modules of sessies, moet uw Connect-account ondersteuning bieden voor vergaderzalen met een voldoende aantal ruimten en gelijktijdige gebruikers voor uw use case. Deze vergaderzalen worden gebruikt om virtuele klassikale modules van Learning Manager te hosten. Er wordt door Learning Manager dynamisch een nieuwe Connect vergaderzaal aangemaakt voor elke virtuele klasmodule of sessie binnen Learning Manager.

U moet Adobe Connect apart aanschaffen, los van Adobe Learning Manager.

## Aanwezigheid van studenten {#learnersattendance}

Als de host van de virtuele klassikale cursus de sessie niet bijwoont, dan wordt de aanwezigheid van de studenten die de sessie hebben bijgewoond niet automatisch geregistreerd. In dergelijke gevallen kan de beheerder de aanwezigheid handmatig vastleggen.

Klik op de virtuele klassikale cursus, klik op Aanwezigheid in het linkerdeelvenster van de volgende pagina en neem de aanwezigheid op.
