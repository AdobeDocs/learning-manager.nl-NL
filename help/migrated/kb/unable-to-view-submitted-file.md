---
jcr-language: en_us
title: Kan ingezonden bestanden niet weergeven in Adobe Learning Manager
description: Docenten kunnen geen bestanden bekijken die studenten hebben geüpload in de module Verzendactiviteit.
contentowner: nluke
source-git-commit: 8b29ac996962e7ce8fbda51f3421c9a5f248fcf6
workflow-type: tm+mt
source-wordcount: '205'
ht-degree: 50%

---



# Kan ingezonden bestanden niet weergeven in Adobe Learning Manager

## Probleem

Een docent kan ingezonden bestanden niet bekijken die een student heeft geüpload.

## Beschrijving

Docenten kunnen geen bestanden bekijken die studenten hebben geüpload in de **activiteitenmodule voor inzendingen**

Een student heeft zich bijvoorbeeld ingeschreven voor een instantie genaamd **Testinstantie** van een cursus, zoals hieronder getoond:

![](assets/test-instance.png)

*Instantie weergeven*

De student opent daarna de cursus en uploadt een bestand in de activiteitenmodule.

Als de docent de inzending wil goedkeuren, lukt dat niet.

![](assets/activity.png)

*Een bestand uploaden in de module Activiteit*

## Oorzaak

Als er geen docent is in de cursusinstantie waarvoor de student is ingeschreven, verschijnt het probleem.

## Resolutie

Voer de onderstaande stappen uit om te controleren of er een docent is toegevoegd aan de cursusinstantie:

1. Ga naar de cursusinstellingen.
1. In het dialoogvenster **Beheren** sectie, klik op **[!UICONTROL Instanties].**
1. Klik in de instantie waar de student is ingeschreven op **[!UICONTROL Sessies]**.

   ![](assets/check-instructor.png)

   *Sessies selecteren in de instantie*

   Er is geen docent toegewezen aan deze sessie.

1. Klikken **[!UICONTROL Bewerken]**. Voeg de docent toe die de inzending van het bestand goedkeurt.

   ![](assets/assign-instructor.png)

   *Voeg de docent toe*
1. Sla de wijzigingen op.

