---
title: Aanstaande wijzigingen in Adobe Learning Manager
description: Lees meer over de nieuwe functies, verbeteringen en belangrijke updates die binnenkort in Adobe Learning Manager verschijnen. Blijf op de hoogte van wat er verandert, zodat je vooruit kunt plannen en optimaal kunt profiteren van de nieuwste verbeteringen.
source-git-commit: 97c52c188612b7ad7233a13bd90bcb174fdc60bc
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 1%

---


# Aanstaande wijzigingen in Adobe Learning Manager

We zijn blij dat we verschillende belangrijke updates voor Adobe Learning Manager kunnen delen met de komende releases. Deze verbeteringen zijn gericht op het stroomlijnen van beheerworkflows, het verbeteren van de nauwkeurigheid van datarapportage en het versterken van op rollen gebaseerde controles.

Deze wijzigingen zijn bedoeld om handmatige inspanningen te verminderen, automatisering te ondersteunen en het beheer van alle trainingsactiviteiten te verbeteren.

## Voltooiingen die zijn gemarkeerd als docent vastleggen in Studenttranscript (M44)

### Doelgroep

Eigenaars van beheerders en automatisering

### Overzicht

Wanneer in Adobe Learning Manager incrementele studenttranscripten (LT) worden gebruikt voor automatiseringsworkflows, worden voltooiingen die zijn gemarkeerd als een docent en die na de sessiedatum zijn gemaakt, niet vastgelegd. Het tijdstempel voor voltooiing geeft de oorspronkelijke eindtijd van de sessie weer (niet de tijd waarop de docent de voltooiing heeft gemarkeerd). Aangezien deze updates buiten het wijzigingsvenster van één dag vallen dat voor incrementele LT-generatie wordt gebruikt, worden de aanwezigheids- en voltooiingsgegevens van studenten uitgesloten van rapporten, wat leidt tot onjuiste of onvolledige downstream-rapportage en mogelijke nalevingshiaten.

### Wat is er veranderd

LT-rapporten (Studenttranscript) bevatten voltooiingen die door docenten na de sessiedatum zijn gemarkeerd. Dit zorgt ervoor dat vertraagde aanwezigheidsmarkering correct wordt weerspiegeld in de transcriptexport.

Aanwezigheidsstatussen zoals &quot;Bijgewoond met slagen/ontbreken&quot; worden automatisch weergegeven in incrementele LT-exports.

### Nieuwe functies

* Nieuwe kolom: Datum markeren voltooid (tijdzone UTC).
* Voltooiingsbron is beschikbaar op moduleniveau.
* Compatibel met op een connector gebaseerde of door API gegenereerde LT-rapporten.

![](assets/capture-instructor.png)

**Vereiste Actie**

* Als de automatisering afhankelijk is van kolomposities, moet u ervoor zorgen dat er logische accounts zijn voor de nieuwe kolom.
* Als u kolomnamen gebruikt, hoeft u deze niet te wijzigen.
* Retrofit-voltooiingen (handmatige invoer) zijn niet inbegrepen.

## Koppelingen downloaden in het Taakhulpenrapport (M44)

### Doelgroep

Beheerders, aangepaste beheerders en eigenaars van automatiseringsprogramma&#39;s

### Overzicht

Het Taakhulpenrapport bevat een directe downloadkoppeling voor elke taakhulp, zodat u snel toegang hebt vanaf het rapport zelf.

### Nieuwe functies

Een nieuwe kolom, **[!UICONTROL Verbinding van de Hulp van de Taak]**, is toegevoegd aan de derde positie in het rapport. Het is rechtstreeks gekoppeld aan de taakhulp als deze een bestand is of de externe URL toont die door de auteur is opgegeven.

Gebruikers met toegang (beheerder/auteurs en aangepaste rollen) kunnen de taakhulp downloaden via deze koppeling.

![](assets/download-links-for-job-aid.png)

### Vereiste actie

* Bekijk geautomatiseerde workflows met behulp van Taakhulpenrapporten (met behulp van de Jobs API).
* Als het script is gebaseerd op de kolompositie, moet u de scripts dienovereenkomstig bijwerken.
* Er is geen actie nodig als u kolomnamen gebruikt.

## Interne gebruikers-id en e-mailkolommen voor manager toegevoegd aan gebruikersrapport (M44)

### Doelgroep

Beheerders (en douanebeheerders) gebruikend het **[!UICONTROL Rapport van de Gebruiker]** (**[!UICONTROL Admin]** > **[!UICONTROL Gebruikers]** > **[!UICONTROL Intern]** > **[!UICONTROL gegevens van de Gebruiker van de Uitvoer]**) gedownload van het gebruikersinterface van de beheerder.

### Overzicht

Om in gebruikersidentificatie en integratiewerkschema&#39;s bij te staan, zijn twee kolommen, **[!UICONTROL Interne identiteitskaart van de Gebruiker]** en **[!UICONTROL E-mail van de Manager]** toegevoegd aan het gebruikersrapport, via het Gebruikersinterface wordt uitgevoerd.

### Nieuwe functies

Het gebruikersrapport bevat de interne gebruikers-id van een gebruiker en het e-mailadres van de manager, zodat deze gebruikers op unieke wijze kunnen worden toegewezen aan verschillende gereedschappen of API-eindpunten.

### Vereiste actie

* Als u dit rapport gebruikt in geautomatiseerde stromen, moet u deze nieuwe kolom in de automatisering gebruiken.
* Er zijn geen wijzigingen nodig als de workflows niet worden beïnvloed.

## Machtigingen voor uitgebreide aankondigingen voor aangepaste beheerders (M44)

### Doelgroep

Aangepaste beheerders

### Overzicht

Aangepaste beheerders kunnen alleen aankondigingen maken voor gebruikersgroepen of catalogi binnen het door hen gedefinieerde bereik.

### Nieuwe functies

* Met bereikregels kunnen aangepaste beheerders alleen aankondigingen voor specifieke gebruikersgroepen of catalogi maken.
* Bij het definiëren van een aangepaste rol kunnen beheerders aankondigingsmachtigingen met een bereik toewijzen aan gebruikersgroepen of catalogi.
* Aangepaste beheerders kunnen alleen aankondigingen maken binnen het opgegeven bereik.
* Het meldingsmeldingsrapport voor aangepaste beheerders geeft alleen studenten weer binnen het toegewezen bereik.

### Vereiste actie

* De vorm van het rapport blijft ongewijzigd. Als aangepaste beheerders het van de Gebruikersinterface downloaden, zal de inhoud van het rapport onderworpen zijn aan hun werkingsgebied.
* Er zijn geen wijzigingen nodig als dit rapport niet wordt gebruikt in een geautomatiseerde of downstreamworkflow.
