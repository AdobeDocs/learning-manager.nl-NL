---
jcr-language: en_us
title: Module is als onvolledig gemarkeerd bij voltooiing van de cursus in Adobe Learning Manager
description: Zelfs nadat een student een cursus heeft voltooid in Adobe Learning Manager, wordt de module als onvolledig gemarkeerd.
contentowner: nluke
source-git-commit: ec79aa3dd6225cc424721afb50702963c1b125eb
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 0%

---



# Module is als onvolledig gemarkeerd bij voltooiing van de cursus in Adobe Learning Manager

## Probleem

Zelfs nadat een student een cursus heeft voltooid in Adobe Learning Manager, wordt de module als onvolledig gemarkeerd.

## Oorzaak

SCORM 2004 definieert de criteria voor succes en voltooiing en verzendt de instructies voor beide afzonderlijk.

Stel dat u een inhoudsset met een **Voltooiingscriteria** van 100% diaweergaven en **Succescriteria** ingesteld als &quot;Quiz wordt doorgegeven&quot;.

Een student voltooit de cursus, maar mislukt de quiz. In dit geval is de voortgang 100%, maar wordt de module als onvolledig gemarkeerd omdat de student niet voldoet aan de **Succescriteria**.

## Oplossing

De kwestie houdt verband met de rapportage **Voorkeuren** voor het project. De auteur moet de criteria verifiëren die zijn ingesteld voor de voltooiing en het succes van de cursus.

Als er wijzigingen zijn vereist, kan de auteur dit doen met een programma voor het schrijven van inhoud, zoals Adobe Captivate Classic. De auteur kan de module vervolgens dienovereenkomstig bijwerken.

![](assets/scorm.png)

*Voorkeuren voor klassieke rapportage Captivate weergeven*
