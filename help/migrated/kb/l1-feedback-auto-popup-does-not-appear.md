---
jcr-language: en_us
title: L1-feedback automatisch pop-upmenu verschijnt niet
description: Fout bij het oplossen van 'automatisch pop-upvenster voor L1-feedback wordt niet weergegeven'
contentowner: saghosh
source-git-commit: ec79aa3dd6225cc424721afb50702963c1b125eb
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 0%

---



# L1-feedback automatisch pop-upmenu verschijnt niet

## Probleem

De automatische pop-up voor L1-feedback verschijnt niet voor een student na het voltooien van de cursus.

## Oorzaak

Soms kan het gebeuren dat een student de L1-feedback na het voltooien van een bepaalde cursus niet ontvangt of een bericht ontvangt zoals hieronder wordt getoond:

![](assets/l1-feedback.png)

*Kan geen L1-feedback ontvangen*

Dit kan om de volgende redenen gebeuren:

1. Feedback is niet ingesteld om na voltooiing van de cursus weer te geven.
1. Herinneringen zijn uitgeschakeld.
1. Een herinnering wordt gepland om na een bepaalde hoeveelheid tijd te verschijnen.

## Resolutie

1. Zorg ervoor dat de optie Vragenlijst direct tonen na voltooiing van de cursus is ingeschakeld in **Cursus** > **Instanties** > **L1-feedback**.
   <!--![](assets/l1-feedback.png)-->
1. Ga als beheerder naar **Instellingen > Feedback**. Controleer wanneer de herinnering is gepland. Als het programma is gepland voor **Na de cursus** voltooiing, wijzig de optie in **Op cursus** voltooiing.
1. Schakel de volgende e-mailsjablonen in: **E-mailsjablonen > Herinneringen en updates > Feedback van student vragen voor cursus**. Als de optie is uitgeschakeld, moet u deze inschakelen en vervolgens testen.
1. Als de bovenstaande stappen niet werken, verwijdert u de herinnering die aanwezig is in **Beheer > Instellingen > Feedback**. Maak er een voor &#39;Bij voltooiing van cursus&#39; en stel de herhaling in op basis van de vereiste waarde.
