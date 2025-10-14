---
title: Niet-aangemelde ervaring voor studenten
description: De eigen Adobe Learning Manager-portal biedt ondersteuning voor een niet-gelogde manier om toegang te krijgen tot de trainingssite. Als deze modus is ingeschakeld, kunnen studenten de trainingssite vinden en openen en verschillende beschikbare cursussen en inhoud uitchecken. Met de niet-aangemelde ervaring kunnen studenten naar cursussen bladeren zonder in een portal te zijn aangemeld.
exl-id: 12260cca-d2d2-4e7c-991d-9b09690d4c0a
source-git-commit: 664b9c867fc767e11d4d91e3be9ae172e7e85035
workflow-type: tm+mt
source-wordcount: '619'
ht-degree: 39%

---

# Niet-aangemelde ervaring voor studenten

De eigen Adobe Learning Manager-portal biedt ondersteuning voor een niet-gelogde manier om toegang te krijgen tot de trainingssite. Als deze modus is ingeschakeld, kunnen studenten de trainingssite vinden en openen en verschillende beschikbare cursussen en inhoud uitchecken.

Met de niet-aangemelde ervaring kunnen studenten naar cursussen bladeren zonder in een portal te zijn aangemeld.

Voor het inschakelen van de niet-aangemelde startpagina moet de integratiebeheerder de [Training Data-connector](/help/migrated/integration-admin/feature-summary/connectors.md#training-data-access) inschakelen en configureren.

De training kan vervolgens uit de connector worden geëxporteerd.

>[!NOTE]
>
>Zorg ervoor dat de optie Native Learning Manager is geselecteerd.

De beheerder kan de startpagina aanpassen en configureren, die bedoeld is voor gebruikers die niet zijn aangemeld.

## Student-API&#39;s

Adobe Learning Manager - Met API&#39;s voor studenten kunt u een aangepaste leerervaring voor uw gebruikers maken. Het gebruik van deze API&#39;s vereist een geldig gebruikerstoken en moet alleen worden gebruikt voor workflows waarbij een volledig gelicentieerde/geregistreerde student aanwezig is.

>[!IMPORTANT]
>
>Ze mogen niet worden gebruikt, zoals bij het ophalen van gegevens, om niet-aangemelde gebruikers/gedeelde gebruikers of andere dergelijke gevallen te ondersteunen. Neem contact met ons op als u een headless of AEM gebaseerde, niet-aangemelde ervaring wilt opbouwen. Wij zullen de juiste benadering voorstellen op basis van uw eisen.

Voor de niet-aangemelde gebruiksscenario&#39;s is een speciale afhandeling vereist.

**Bereik uit aan het team van de Architectuur van de Oplossing, voor het geval u om het even welke vragen over het aangewezen gebruik van deze APIs hebt en ervoor zorgt dat een Architect van de Oplossing een oplossing heeft onderzocht alvorens u het opstelt**.

## Opties voor de startpagina starten

Voor de homepage van Adobe Learning Manager, uitgezochte **Branding**. Selecteer vervolgens Niet-aangemelde startpagina in het linkerdeelvenster.

![&#x200B; homepage opties &#x200B;](assets/non-logged-in-homepage.png)

*selecteer de optie niet-het programma geopende Homepage*

## Banner toevoegen

Voeg een banner toe voor elke marketingaankondiging of voor het trending onderwerp van de dag. Selecteer **banner** toevoegen.

![&#x200B; banner &#x200B;](assets/add-banner-image.png)

*voeg een banner toe*

Blader naar de locatie van de afbeelding die als banner moet worden gebruikt. Geef vervolgens een koppeling op als actieknop op de bannerafbeelding.

## Categorieën toevoegen

Dit onderdeel kan worden gebruikt om de catalogus te filteren op tags, vaardigheden en catalogus. Deze sectie bevat een kop en een beschrijving voor elke categorie. Na klikken komt de gebruiker bij de cataloguspagina met de toegepaste filters.

Selecteer **[!UICONTROL voeg categorie]** toe. Voer vervolgens de gegevens voor de categorie in.

![&#x200B; voeg categorie &#x200B;](assets/add-category.png) toe

*voeg de categorieën* toe

Sla de categorie op. Vervolgens wordt de categorie aan de sectie toegevoegd.

## Catalogus toevoegen

Voeg een catalogus toe voor gebruikers die niet zijn aangemeld, zodat ze door alle trainingen op het platform kunnen bladeren.

![&#x200B; voeg catalogus &#x200B;](assets/add-catalog.png) toe

*voeg een catalogus toe*

Alle geëxporteerde trainingen zijn aanwezig.

## Niet-ondersteunde functies

* Taakhulpen worden niet geëxporteerd. Studenten kunnen ze echter zien nadat ze zich hebben aangemeld.
* Sorteren op in de component catalog.
* Standaardinstelling voor weergave gebruikt in de beheertoepassing (Instellingen > Algemeen > Lijstweergave).
* Sterrenclassificatie/effectiviteit.
* Instelling kaartpictogram.
* Instelling voor relevante vaardigheden en tags.
* Student-appweergave die per catalogus wordt weergegeven.
* Trainingsoverzicht-pagina&#39;s - Als u op de kaart klikt, wordt u naar  Aanmelden geleid, waarna een gebruiker wordt doorgeleid naar de pagina met trainingsoverzicht/instantie.
* Alle ingeschakelde catalogi zijn aanwezig. Studenten die geen toegang tot een catalogus hebben, kunnen de catalogus na aanmelding niet zien of gebruiken.
* Voor de native optie worden wijzigingen in een cursus of leerpad pas na 24 uur in plaats van in real-time weerspiegeld, terwijl voor de premium aanbieding ze na minimaal 3 uur worden weergegeven.
