---
jcr-language: en_us
title: Kan niet als een Externe gebruiker registreren
description: Externe studenten kunnen zich niet registreren bij een profiel in Adobe Learning Manager.
contentowner: nluke
source-git-commit: 6abc118c6ad7e66e3ded5bd26b9167c3a0b99e4b
workflow-type: tm+mt
source-wordcount: '328'
ht-degree: 50%

---



# Kan niet als een Externe gebruiker registreren

## Probleem

Externe gebruikers kunnen zich niet registreren voor een profiel.

## Fout

E-mail-ID is al geregistreerd. Gebruik een ander e-mailadres.

![](assets/cp-register-profile.png)

*Foutbericht van een reeds geregistreerde e-mail*

## Beschrijving

Er bestaan scenario&#39;s waarin een gebruiker zich niet kan registreren voor een Extern profiel. De gebruiker krijgt bovenstaande fout bij het aanmelden.

## Oorzaak

Dit probleem doet zich voor bij één van de onderstaande scenario&#39;s:

* De gebruiker is al geregistreerd voor een ander extern profiel.
* De gebruiker is al een interne student.
* De gebruiker is verwijderd.

## Oplossing:

**Scenario 1** De gebruiker is al geregistreerd bij een ander extern profiel.

1. Meld u aan als beheerder.
1. Onder **Beheren**, klik op **[!UICONTROL Gebruikers]** > **[!UICONTROL Extern]**.
1. Klik op Gebruikte plaatsen om het profiel te openen waarvan de gebruiker al deel uitmaakt

   ![](assets/cp-seats-used.png)

   *Profiel van gebruiker openen*

1. Selecteer de gebruiker, klik op **[!UICONTROL Handelingen]** > **[!UICONTROL Profiel wijzigen]**.

   ![](assets/cp-change-profile.png)

   *Profiel van gebruiker wijzigen*

   Hierdoor wordt een venster geopend om een nieuw profiel, zoals hieronder, te selecteren.

   ![](assets/cp-select-profiles.png)

   *Gebruikersprofiel selecteren*

1. Klik op **[!UICONTROL Wijzigen]** nadat u een selectie hebt gemaakt.

**Scenario 2** De gebruiker is aanwezig als interne student.

1. Meld u aan als beheerder.
1. Onder **Beheren**, klik op **[!UICONTROL Gebruikers]** > **[!UICONTROL Intern]**.
1. Klik op een Studentenprofiel en klik op het pictogram Bewerken.

   ![](assets/cp-internal-learner.png)

   *Een intern studentenprofiel openen*

1. Wijzig het e-mailadres van de student of voeg *_old* naar het bestaande e-mailadres. Hiermee maakt u het e-mailadres vrij.

   Als het e-mailadres van de student bijvoorbeeld *<abc@adobe.com>,* wijzigen in *<abc_old@adobe.com>*

1. Klikken **Opslaan** om de aangebrachte wijzigingen te behouden.

**Scenario 3**: de gebruiker is verwijderd.

1. Meld u aan als Beheerder.
1. Onder **Beheren**, klik op **[!UICONTROL Gebruikers]** > **[!UICONTROL Gebruikersopschoning]**.
1. Selecteer de Student en klik op de knop Bewerken.

   ![](assets/cp-deleted-learner.png)

   *E-mailadres van gebruiker bewerken*

1. Wijzig het e-mailadres van de student of voeg *_old* naar het bestaande e-mailadres. Hiermee maakt u het e-mailadres vrij.

   Als het e-mailadres van de student bijvoorbeeld **<abc@adobe.com>** wijzigen in **<abc_old@adobe.com>**.
