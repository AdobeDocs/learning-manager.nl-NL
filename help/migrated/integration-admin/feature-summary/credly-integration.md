---
jcr-language: en_us
title: Credly
description: Meer informatie over de integratie van Credly met ALM voor het beheren en delen van externe badges vanaf het platform via verschillende social-mediakanalen
contentowner: chandrum
source-git-commit: a27c1566678d697512a75d94804b8804b5dc9b2b
workflow-type: tm+mt
source-wordcount: '364'
ht-degree: 0%

---

# Credly

[ Geloofsbrieven ](https://info.credly.com/) is een digitaal geloofsbrieven platform dat studenten en organisaties toestaat om, professionele prestaties, zoals badges of certificeringen te verdienen te delen en te verifiëren. Studenten kunnen badges beheren en delen via hun aanmeldingsprofiel op sociale media en andere plaatsen.

## Vereisten

Stel een Credly-account in voor uw organisatie. Voeg studenten toe aan Credly met behulp van hun e-mailadressen in Adobe Learning Manager. Zo kunnen de studenten de badges op Credly en Adobe Learning Manager zien.

## Voeg de Credly-connector toe aan Adobe Learning Manager

Ga als volgt te werk om de Credly-connector aan Adobe Learning Manager toe te voegen:

1. Login als **[!UICONTROL Admin van de Integratie]**.
2. Selecteer **[!UICONTROL Credly]** > **verbind** om de **[!UICONTROL Credly]** schakelaar aan Adobe Learning Manager toe te voegen.

   ![](assets/connector-credly.png)
   _voeg Geloofsschakelaar_ toe

3. Typ de **[!UICONTROL Naam van de Verbinding]**.
4. Typ het **[!UICONTROL identiteitskaart van de Organisatie]** en **[!UICONTROL token van de Vergunning]**.

   >[!NOTE]
   >
   >Elke badge in Credly wordt geleverd met een organisatie-id en machtigingstoken. Kopieer deze waarden uit Credly.

5. Typ **[!UICONTROL Hostname]** en selecteer **[!UICONTROL verbind]**.

## Badges migreren van Credly

Met badge.csv in Adobe Learning Manager kunt u badges migreren van het bestaande LMS of externe systeem. De badge.csv is bijgewerkt met twee nieuwe kolommen:

* Externe badge-id
* Externe badgeprovider.

Externe badge-id verwijst naar de badgesjabloon-id in het Referentieplatform en de externe badgeprovider is Credly. Voeg deze waarden in badge.csv toe en volg de stappen die in het [ handboek van de Migratie ](https://experienceleague.adobe.com/en/docs/learning-manager/using/integration/migration-manual#migrationprocedure) worden vermeld om csv te migreren.

## Vaardigheid maken - Beheerder

Zodra de badge is geïmporteerd in Adobe Learning Manager, kan de beheerder deze badges als een vaardigheid maken. Om te weten hoe te om een vaardigheid tot stand te brengen, zie [ Vaardigheden ](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/skills-levels) creëren en wijzigen.

### De vaardigheid/badge toewijzen aan het leerobject - Auteur

De auteur/beheerder kan deze door Credly geïmporteerde ALM-badges toewijzen aan een cursus, leerpad of certificering (niet alleen vaardigheden). Bij gebruik van deze leerobjecten wordt de badge behaald en weergegeven in Credly en ALM App.

Studenten kunnen zich aanmelden bij Credly en de badges bekijken op het Credly-platform. Vanuit Credly kunnen ze de badges delen op externe platforms zoals LinkedIn en andere social media.

