---
jcr-language: en_us
title: Kan niet registreren als externe gebruiker
description: Externe studenten kunnen zich niet registreren bij een profiel in Adobe Learning Manager.
contentowner: nluke
source-git-commit: 6abc118c6ad7e66e3ded5bd26b9167c3a0b99e4b
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 0%

---



# Kan niet registreren als externe gebruiker

## Probleem

Externe studenten kunnen zich niet registreren bij een profiel.

## Fout

E-mail-ID is al geregistreerd. Gebruik een andere e-mail.

![](assets/cp-register-profile.png)

*Foutbericht van een reeds geregistreerde e-mail*

## Beschrijving

Er zijn scenario&#39;s waarin een gebruiker zich niet kan registreren bij een extern profiel. De gebruiker ontvangt de bovenstaande fout tijdens het aanmelden.

## Oorzaak

Dit probleem doet zich voor in een van de volgende scenario&#39;s:

* De gebruiker is al geregistreerd bij een ander extern profiel.
* De gebruiker is al een interne student.
* De gebruiker heeft een verwijderde status.

## Resolutie:

**Scenario 1** De gebruiker is al geregistreerd bij een ander extern profiel.

1. Meld u aan als beheerder.
1. Onder **Beheren**, klik op **[!UICONTROL Gebruikers]** > **[!UICONTROL Extern]**.
1. Open het profiel waarvan de gebruiker al deel uitmaakt door op de gebruikte plaatsen te klikken

   ![](assets/cp-seats-used.png)

   *Profiel van gebruiker openen*

1. Selecteer de gebruiker, klik op **[!UICONTROL Handelingen]** > **[!UICONTROL Profiel wijzigen]**.

   ![](assets/cp-change-profile.png)

   *Profiel van gebruiker wijzigen*

   Hiermee wordt een venster geopend waarin u een nieuw profiel kunt selecteren, zoals hieronder weergegeven.

   ![](assets/cp-select-profiles.png)

   *Gebruikersprofiel selecteren*

1. Klik op **[!UICONTROL Wijzigen]**.

**Scenario 2** De gebruiker is aanwezig als interne student.

1. Meld u aan als beheerder.
1. Onder **Beheren**, klik op **[!UICONTROL Gebruikers]** > **[!UICONTROL Intern]**.
1. Klik om een studentprofiel te openen en klik op het pictogram Bewerken.

   ![](assets/cp-internal-learner.png)

   *Een intern studentenprofiel openen*

1. Wijzig het e-mailadres van de student of voeg *_old* naar het bestaande e-mailadres. Hiermee maakt u het e-mailadres vrij.

   Als het e-mailadres van de student bijvoorbeeld *<abc@adobe.com>,* wijzigen in *<abc_old@adobe.com>*

1. Klikken **Opslaan** om de aangebrachte wijzigingen te behouden.

**Scenario 3**: De gebruiker heeft een verwijderde status.

1. Meld u aan als beheerder.
1. Onder **Beheren**, klik op **[!UICONTROL Gebruikers]** > **[!UICONTROL Gebruikersopschoning]**.
1. Selecteer de student en klik op het pictogram Bewerken.

   ![](assets/cp-deleted-learner.png)

   *E-mailadres van gebruiker bewerken*

1. Wijzig het e-mailadres van de student of voeg *_old* naar het bestaande e-mailadres. Hiermee maakt u het e-mailadres vrij.

   Als het e-mailadres van de student bijvoorbeeld **<abc@adobe.com>** wijzigen in **<abc_old@adobe.com>**.
