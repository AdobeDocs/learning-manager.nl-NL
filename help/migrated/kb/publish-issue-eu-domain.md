---
jcr-language: en_us
title: Kan niet publiceren naar het EU-domein van Learning Manager
description: Kan niet publiceren van Adobe Captivate naar Adobe Learning Manager EU domein in Adobe Learning Manager.
contentowner: nluke
source-git-commit: 69ac8f8ce5a0c077f31569571f9d9fbf16ecb943
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 0%

---



# Kan niet publiceren naar het EU-domein van Learning Manager {#unable-to-publish-to-learning-manager-eu-domain}

## Probleem

Kan niet publiceren van Adobe Captivate naar Adobe Learning Manager EU domein.

## Fout

Geen accounts gevonden

## Beschrijving

Er zijn scenario&#39;s waarin auteurs proberen een cursus te publiceren van Adobe Captivate naar Adobe Learning Manager. Ze kunnen dit echter niet doen omdat ze het foutbericht &quot;Geen account gevonden&quot; zien.

## Oorzaak

Dit probleem doet zich voor omdat Adobe Captivate standaard is geconfigureerd om inhoud te publiceren naar het Amerikaanse domein van Adobe Learning Manager.

## Resolutie:

Notities:

* Sluit de Adobe Captivate-toepassing als deze is geopend.
* U hebt beheerderstoegang op uw computer nodig om de onderstaande stappen uit te voeren. Als u geen beheerdersrechten hebt, neemt u contact op met uw IT-team voor hulp.

Voer de onderstaande stappen uit:

1. Ga naar de installatiemap voor Adobe Captivate.

   Bijvoorbeeld:  `kbd C:\\Program Files\\Adobe\\Adobe Captivate 2019 x64` (2019 is de versie van de Captivate. Verschil als u een andere versie van Adobe Captivate gebruikt).

1. Het configuratiebestand kopiëren **AdobeCaptivate.ini** op uw bureaublad.

   ![](assets/cp-captivate.ini.png)
   *Het configuratiebestand weergeven*

1. Open het gekopieerde bestand van uw bureaublad op een Kladblok.
1. Wijzig de waarde van LearningManagerBaseUrl = `https://learningmanager.adobe.com/inappstarter` to LearningManagerBaseUrl = `https://learningmanagereu.adobe.com/inappstarter`

   ![](assets/cp-primebaseurl.png)
   *PrimeBaseURL weergeven*

1. Sla de wijzigingen op die in het Kladblok zijn aangebracht.
1. Kopieer het opgeslagen bestand dat u hebt bewerkt en plak het weer in het bestandspad. Het oorspronkelijke bestand vervangen in  `kbd C:\\Program Files\\Adobe\\Adobe Captivate 2019 x64`
1. Start Adobe Captivate en probeer vervolgens te publiceren naar Adobe Learning Manager.
