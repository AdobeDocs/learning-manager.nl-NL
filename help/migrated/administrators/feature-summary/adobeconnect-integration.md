---
jcr-language: en_us
title: Adobe Connect-integratie
description: Auteurs kunnen virtuele klassikale cursussen met Adobe Connect maken tijdens het maken van cursussen. Neem contact op met de beheerder van uw organisatie om Adobe Connect in te schakelen voor uw LMS-account.
contentowner: jayakarr
source-git-commit: 0052ccb2f5a8f9617bca2c7bad91c0cd18338b66
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---



# Adobe Connect-integratie

Beheerders van een organisatie kunnen de instellingen van het Learning Manager-account configureren om Adobe Connect-integratie in te schakelen.

## Adobe Connect configureren {#configureadobeconnect}

1. Klik in Beheerdersaanmelding op **[!UICONTROL Instellingen]** in het linkerdeelvenster om de basisinformatie over uw bedrijf weer te geven. Klikken **[!UICONTROL Adobe Connect]** in het linkerdeelvenster.

   ![](assets/left-pane.png)

   *Adobe Connect selecteren in het linkerdeelvenster*

1. Klikken **[!UICONTROL Nu configureren]** link in **[!UICONTROL Adobe Connect-configuratie]** sectie.

   <!--![](assets/configure-now-connect.png)-->

1. Geef de Adobe Connect-domeinnaam van uw bedrijf op en meld u aan met uw gegevens.

   ![](assets/adobeconnect-config.png)

   *Domeinnaam en referenties toevoegen*

   Een voorbeeld van een Adobe Connect-URL: mycompany.adobeconnect.com\
   U moet de e-mail-ID van de beheerder van het Connect-account van de Adobe opgeven.

   Alleen door Adobe gehoste Connect-accounts worden ondersteund in Learning Manager. Voorbeeld; &#39;.adobeconnect.com&#39;.

1. Klikken **[!UICONTROL Integreren].**

   Nadat de e-mail-ID is geverifieerd, geeft Learning Manager het bericht weer als Connect is geïntegreerd. U kunt uw virtuele klassikale cursussen automatisch bekijken met Adobe Connect.

   De accountbeheerder van Adobe Connect dient de Voorwaarden voor het gebruik van Adobe Connect te accepteren. Als dit niet wordt geaccepteerd, kan uw aanmeldingsverificatie mislukken. Meld u eenmaal aan bij het account nadat u het Adobe Connect-account hebt gemaakt. Tijdens de eerste aanmelding wordt een pagina met voorwaarden en bepalingen weergegeven.

   <!--![](assets/mail-confirmation.png)-->

## Sessiegegevens van virtuele lesruimten toevoegen {#addvirtualclassroomsessioninformation}

Als de auteur van een virtuele klassikale cursus de sessiegegevens niet heeft verstrekt, kan de beheerder de sessiedetails opnemen.

Klik in Beheerdersaanmelding op de naam van de VC-cursus. Klikken **[!UICONTROL Instanties]** in het linkerdeelvenster en klik op **[!UICONTROL Sessiedetails]**.  Klik op het pictogram Bewerken in de rechterhoek van de pagina Sessiedetails om de sessiegegevens toe te voegen.

![](assets/session-creation-admin.png)

*Sessiegegevens van virtuele lesruimten toevoegen*

Dankzij de integratie van Adobe Learning Manager en Adobe Connect voor het maken van virtuele klassikale modules of sessies, moet uw Connect-account ondersteuning bieden voor vergaderruimten met een passend aantal ruimten en gelijktijdige gebruikers voor uw gebruiksscenario. Deze vergaderruimten worden gebruikt om virtuele lesruimtemodules van de Learning Manager te hosten. Er wordt dynamisch een nieuwe Connect-vergaderruimte gemaakt door Leermanager voor elke virtuele klassikale module of sessie in Leerbeheer.

U moet Adobe Connect apart aanschaffen, behalve Adobe Learning Manager.

## Aanwezigheid van studenten {#learnersattendance}

Als de gastheer van de virtuele klassikale cursus de sessie niet bijwoont, wordt de aanwezigheid niet automatisch geregistreerd voor studenten die de sessie hebben bijgewoond. In dergelijke gevallen kan de beheerder de aanwezigheid handmatig vastleggen.

Klik op de virtuele klassikale cursus, klik op Aanwezigheid in het linkerdeelvenster van de volgende pagina en neem de aanwezigheid op.
