---
jcr-language: en_us
title: Sociale aanmelding in Learning Manager
description: Sociale aanmelding in Learning Manager
contentowner: saghosh
preview: true
source-git-commit: ccdb222228f76fdae63ebb0a808824ad6ac1db7f
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---



# Sociale aanmelding in Learning Manager

U kunt uw aanmeldingsgegevens voor Facebook, LinkedIn of Twitter gebruiken om u aan te melden bij Learning Manager.

## Sociaal aanmelden instellen {#setupsociallogin}

1. Neem contact op met uw Customer Success Manager als u wilt dat hij of zij het account instelt.

   Volg anders de onderstaande stappen.

1. Zoek naar het account waar u aanmelden voor een sociaal account wilt instellen.
1. Wijzig de aanmelding in SSO.
1. Klik op Geavanceerd. Geef de volgende JSON op.

   ```
   \{"linkedIn":true,"microsoft":true,"twitter":true,"facebook":true,"editingAllowed":true
   ```

   Als het een onjuiste JSON is, zal er een uitzondering zijn.

   Deze functie voor aanmelden via sociale media wordt alleen gebruikt voor INTERNE gebruikers.

