---
jcr-language: en_us
title: Aanmeldproblemen in Learning Manager
description: Aanmeldingsproblemen in Adobe Learning Manager
contentowner: nluke
source-git-commit: ec79aa3dd6225cc424721afb50702963c1b125eb
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 87%

---



# Aanmeldproblemen in Learning Manager

## Probleem

Ik kan me niet aanmelden bij Adobe Learning Manager.

## Fout

Als u zich probeert aan te melden bij Adobe Learning Manager, wordt de onderstaande foutmelding weergegeven:

![](assets/cp-error.png)

*Foutbericht voor een verlopen sessie*

## Reden

Wanneer een gebruiker zich aanmeldt via SSO, wordt een sessiecookie gemaakt die in de browser wordt opgeslagen. Hiermee kan de gebruiker zich ook aanmelden bij andere toepassingen. De meeste SSO&#39;s zijn zo geconfigureerd dat een gebruiker na 24 uur wordt afgemeld. De gebruiker moet zich opnieuw verifiëren voor een nieuwe sessie.

In bepaalde gevallen heeft een gebruiker geen toegang tot het systeem vanwege verouderde SSO-cookies. Deze cookies worden ter verificatie doorgestuurd naar Adobe Learning Manager. De sessie wordt niet beëindigd als een gebruiker de browser lange tijd niet sluit of zich niet heeft afgemeld.

Adobe Learning Manager wijst deze verouderde cookies af, wat resulteert in een fout.

## Resolutie

Als een verouderde cookie wordt afgewezen door Adobe Learning Manager, probeer dan de onderstaande opties:

1. Wis de cookies en cache van uw browser. Zie dit [document](unable-log-in-learning-manager.md) voor meer informatie.

   Als alternatief kan de IDP-beheerder een gedwongen afmelding definiëren na een bepaalde ingestelde tijd. Met deze stap wordt de gebruiker opnieuw geverifieerd om een nieuwe sessie te starten.

Er zijn andere redenen waarom deze fout optreedt, maar het bovenstaande is een veelvoorkomend scenario.

## Verwijzingskoppelingen:

[Microsoft: voorwaardelijke toegangssessie gedurende een levensduur](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/howto-conditional-access-session-lifetime)
