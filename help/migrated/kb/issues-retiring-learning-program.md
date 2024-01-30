---
jcr-language: en_us
title: Problemen bij het archiveren van een leerprogramma
description: Problemen met het archiveren van een leerprogramma in Adobe Learning Manager
contentowner: nluke
source-git-commit: 66dfaaaf723382eada39e2be29dfd49b795107a0
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 55%

---



# Problemen bij het archiveren van een leerprogramma

## Probleem

Een leerprogramma wordt automatisch gearchiveerd.

## Oorzaak

Er zijn situaties waarin een leerprogramma is gearchiveerd zonder dat een beheerder/auteur het leerprogramma expliciet heeft gearchiveerd.

Dit probleem treedt op omdat een leerprogramma een verzameling van cursussen is. De trainingen op hoger niveau worden gearchiveerd als een van de cursussen daarin een gearchiveerde instantie bevat of als de cursusinstantie wordt gearchiveerd.

## Resolutie

Volg de onderstaande stappen om de cursus te controleren die een gearchiveerde instantie bevat:

1. Meld u aan als beheerder en start het relevante leerprogramma.

1. Klikken **[!UICONTROL Instanties]** > **Cdagbladen**. De pagina bevat alle cursussen die deel uitmaken van dit leerprogramma. U kunt de cursus met een gearchiveerd exemplaar bekijken.

   ![](assets/retired-instance.png)

   *Lijst met alle cursussen weergeven*

1. Nadat u de gearchiveerde cursusinstantie hebt uitgezocht, klikt u op **[!UICONTROL Cursussen]** > **[!UICONTROL De cursus openen]**.

1. Klikken **[!UICONTROL Instanties]**. Klik op de gearchiveerde instantie op **[!UICONTROL Bewerken]** en bewerk vervolgens de voltooiingsdatum naar een toekomstige datum waarop de instantie moet worden gearchiveerd.

   ![](assets/completion-date.png)

   *De voltooiingsdatum van een cursus bewerken*

1. Wanneer u klaar bent, klikt u op de vervolgkeuzelijst zoals weergegeven op de onderstaande afbeelding. Klik vervolgens op **[!UICONTROL Instantie opnieuw openen]**.

   ![](assets/re-open-instance.png)

   *Instantie van een cursus weergeven*

1. Ga naar het relevante leerprogramma. Klikken **[!UICONTROL Instanties]** en voer de vorige stap uit om de instantie van het leerprogramma opnieuw te openen.
