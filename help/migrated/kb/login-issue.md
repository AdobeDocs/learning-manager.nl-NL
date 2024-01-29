---
jcr-language: en_us
title: Aanmeldingsproblemen in Learning Manager
description: Aanmeldingsproblemen in Adobe Learning Manager
contentowner: nluke
source-git-commit: ec79aa3dd6225cc424721afb50702963c1b125eb
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---



# Aanmeldingsproblemen in Learning Manager

## Probleem

Kan niet aanmelden bij Adobe Learning Manager.

## Fout

Wanneer u zich aanmeldt bij Adobe Learning Manager, wordt het onderstaande foutbericht weergegeven:

![](assets/cp-error.png)

*Foutbericht voor een verlopen sessie*

## Reden

Wanneer een gebruiker zich aanmeldt via SSO, wordt een sessiecookie gemaakt die in de browser wordt opgeslagen. Ook kan de gebruiker zich aanmelden bij andere toepassingen. De meeste SSO&#39;s zijn geconfigureerd om zich na 24 uur af te melden. De gebruiker moet zich opnieuw verifiëren voor een nieuwe sessie.

In bepaalde gevallen heeft een gebruiker geen toegang tot het systeem vanwege verouderde SSO-cookies. Deze cookies worden ter verificatie doorgestuurd naar de Adobe Learning Manager. De sessie wordt niet beëindigd als een gebruiker de browser niet lang sluit of zich niet heeft afgemeld.

Adobe Learning Manager wijst deze verouderde cookies af, wat resulteert in een fout.

## Resolutie

Als een verouderde cookie wordt afgewezen door Adobe Learning Manager, kunt u de volgende opties proberen:

1. Wis de browsercookies en cache. Zie deze voor meer informatie [document](unable-log-in-learning-manager.md).

   De IDP-beheerder kan ook na een bepaalde ingestelde tijd een afmeldingsstatus voor de kracht definiëren. In deze stap wordt de gebruiker opnieuw geverifieerd om een nieuwe sessie te starten.

Er zijn andere redenen waarom deze fout optreedt, maar het bovenstaande is een algemeen scenario.

## Verwijzingskoppelingen:

[Microsoft: voorwaardelijke toegangssessie gedurende een levensduur](https://docs.microsoft.com/en-us/azure/active-directory/conditional-access/howto-conditional-access-session-lifetime)
