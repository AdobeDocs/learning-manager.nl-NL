---
jcr-language: en_us
title: Learning Manager-integratie met Slack
description: Learning Manager-integratie met Slack
contentowner: dvenkate
source-git-commit: 864b1796f1ca99ae7b5643e8c58d1756ff2461a1
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 44%

---



# Learning Manager-integratie met Slack

We hebben **verwijderd** **Slack** als een connector in Learning Manager. U hebt geen toegang meer tot de Slack-connector.

Als Slack-gebruiker kunt u de Adobe Learning Manager-app via de Slack App Directory in uw Slack-teams installeren, en Learning Manager-inhoud in Slack ontdekken. U kunt met Primebot communiceren om te zoeken naar nieuwe cursussen, aanbevelingen te bekijken en op de hoogte te worden gesteld van aanstaande deadlines in Learning Manager. U kunt u ook inschrijven en rechtstreeks naar uw leermateriaal gaan vanuit Slack.

De app Learning Manager voor Slack wordt niet ondersteund in een Azure-instantie van Learning Manager.

## Installeer de Adobe Learning Manager-app {#installingadobecaptivateprimeapp}

U kunt de CP Prime-app in uw Slack-account installeren als student. Om de app te installeren, opent u de App Directory in uw Slack-account en zoekt u naar Learning Manager. Download en installeer de app. Als de app niet in uw account is goedgekeurd, neemt u contact op met uw integratiebeheerder voor goedkeuring. Als het reeds is goedgekeurd, kunt u zich aanmelden.

## Aanmelding student als integratiebeheerder goedkeuren {#approvinglearnersigninasanintegrationadmin}

Volg deze stappen om als integratiebeheerder de machtiging goed te keuren waarmee een student Prime-toepassing op Slack kan gebruiken.

1. Selecteer **[!UICONTROL Toepassingen]** in het linkerdeelvenster en klik op het tabblad met **[!UICONTROL uitgelichte apps]**.

   ![](assets/featuredapps.jpg)

1. Klik op de **[!UICONTROL Slack]**-tegel. Hiermee opent u de Slack-integratiepagina. Klikken **[!UICONTROL Goedkeuren]** rechtsboven om de toepassing goed te keuren.

   ![](assets/approval.png)

1. Ga terug naar de **[!UICONTROL Toepassingen]** pagina. Na goedkeuring dient Slack te worden weergegeven in de **[!UICONTROL Externe apps]** tabblad.
1. Studenten kunnen zich nu via Slack aanmelden bij hun Prime-account.

## Primebot-functionaliteiten {#primebotfunctionalities}

Je kunt nu beginnen met interactie met de Primebot. Dit zijn de functionaliteiten van de bot:

1 - Opdracht

&#42;/prime&#42; kan worden gebruikt voor eenmalige, gerichte vragen over uw Adobe Learning Manager-account.

De beschikbare subopdrachten zijn:

/prime find `<query>` - zoeken naar cursussen, certificeringen, enz.

/prime recommend - aanbevelingen weergeven

/prime deadlines - verstreken en aanstaande deadlines weergeven

/prime enrollments - inschrijvingen weergeven

/prime skills - vaardigheden weergeven

/prime notifications - meldingen weergeven

/prime catalogs - catalogi weergeven

/prime uitnodiging - [Alleen beheerder] Slack-gebruikers uitnodigen in het huidige team om primebot uit te proberen

/prime profile - profiel weergeven

/prime logout - meld u af bij uw Prime-account voor dit Slack-team

/prime help - helpbericht weergeven

2 - Aanbevelen

Je kunt een woordgroep als `show my recommendations` om een gepersonaliseerde lijst met aanbevolen cursussen, certificeringen en leerprogramma&#39;s op te halen van uw Adobe Learning Manager-account.

3 - Zoeken

U kunt woorden als `search for machine learning` of `search for artificial intelligence`. U kunt het soort leerobject opgeven met zinnen als `search for machine learning certifications`, `search for artificial intelligence courses` of `search for adobe photoshop job aids`. U kunt ook in een catalogus zoeken met zinnen als `search for machine learning in Lynda catalog`.

4 - Termijnen

Woorden gebruiken als `show my deadlines` om een lijst met verstreken en aanstaande deadlines op te halen uit uw Adobe Learning Manager-account. U kunt verstreken of aanstaande deadlines filteren met zinnen als `show my overdue deadlines` of `show my upcoming deadlines`.
