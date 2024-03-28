---
jcr-language: en_us
title: Locaties van klaslokalen toevoegen
description: Beheerders kunnen nu een bibliotheek met locaties van klaslokalen instellen. Voor elke locatie van een klaslokaal kunnen de beheerders de metadata instellen, waaronder de locatienaam, het aantal plaatsen en aanvullende informatie zoals de locatie-URL. Auteurs en beheerders kunnen deze vooraf geconfigureerde locaties van klaslokalen vervolgens gebruiken voor het instellen van door een docent geleide trainingsgebeurtenissen (klaslokaalmodules).
contentowner: saghosh
exl-id: 51a1e38f-d4e2-4c19-bbf7-6696505c0dfd
source-git-commit: b882c22da029cdc4c8bcc4ab1b6d861f06f83f0f
workflow-type: tm+mt
source-wordcount: '1240'
ht-degree: 77%

---

# Klaslokaal

## Overzicht

Beheerders kunnen nu een bibliotheek met locaties van klaslokalen instellen. Voor elke locatie van een klaslokaal kunnen de beheerders de metadata instellen, waaronder de locatienaam, het aantal plaatsen en aanvullende informatie zoals de locatie-URL. Auteurs en beheerders kunnen deze vooraf geconfigureerde locaties van klaslokalen vervolgens gebruiken voor het instellen van door een docent geleide trainingsgebeurtenissen (klaslokaalmodules).

U kunt op de volgende twee manieren een locatie van een klaslokaal toevoegen.

## Klaslokaal toevoegen met behulp van de gebruikersinterface

U kunt een locatie voor een lesruimte toevoegen via de gebruikersinterface:

1. Klik in de Admin-app (de gebruikersinterface voor beheerdersrollen) op **[!UICONTROL Instellingen]** > **[!UICONTROL Locaties van lesruimte]**.

1. Klikken **[!UICONTROL Toevoegen]** > **[!UICONTROL Nieuwe locatie]**.

1. Voer in het dialoogvenster **[!UICONTROL Locatie van klaslokaal]** de volgende gegevens in:

   * Typ de **[!UICONTROL Locatienaam]**. Gebruik een unieke naam. Anders verschijnt er een foutmelding in Learning Manager.
   * Typ de locatiebeschrijving in het veld **[!UICONTROL Locatiegegevens]**. Dit veld is optioneel.
   * Typ de **[!UICONTROL locatie-URL]**. De student kan deze informatie zien in de klaslokaaldetails. Indien nodig kan de URL ook een locatie-URL van een kaart zijn. Dit veld is optioneel.
   * Typ en selecteer de **[!UICONTROL Locatiegebied]**. Dit veld is optioneel.
   * Typ het aantal beschikbare plaatsen in het veld **[!UICONTROL Plaatslimiet]**. Dit geeft de plaatscapaciteit van het klaslokaal aan. Deze waarde kan worden gewijzigd bij het maken van de daadwerkelijke door een docent geleide trainingsgebeurtenis.

   ![](assets/add-classroom-location.png)

   *Een locatie voor een lesruimte toevoegen*

Nadat u de locatie hebt toegevoegd, **[!UICONTROL Instellingen]** > **[!UICONTROL Locaties van lesruimte]** bevat een lijst met de vergaderruimten:

![](assets/list-meeting-rooms.png)

*Alle vergaderruimten weergeven*

De lijst bevat de volgende velden:

**[!UICONTROL Locatienaam]** - Naam van de locatie van de lesruimte.

**[!UICONTROL Toekomstige sessies]** - Aantal gebeurtenissen dat op de corresponderende locatie zal optreden. Klik op het aantal om de details in een dialoogvenster te bekijken.

![](assets/sessions-list.png)

*Bekijk toekomstige sessies*

Het dialoogvenster toont de details van elke sessie, waaronder de naam van de sessie, de naam van de training die de sessie omvat en het sessieschema. De getoonde tijd komt overeen met de systeemtijdzone van de student.

De **[!UICONTROL Toekomstige sessies]** veldweergaven **nul** als de lesruimte niet wordt gebruikt voor een sessie of als de lesruimte is gekoppeld aan eerdere sessies.

**[!UICONTROL Zitlimiet]** - Geeft de capaciteit van de stoelen van de lesruimte weer.

**Locatie-URL** - URL die u hebt opgegeven bij het maken van de locatie van de lesruimte.

**Locatie-informatie** - De lesruimtegegevens die u hebt opgegeven bij het maken van de lesruimte.

## Een lesruimte toevoegen met behulp van CSV

U kunt ook een of meer klaslokalen toevoegen door een CSV te importeren die de klaslokaalinformatie bevat.

In **[!UICONTROL Admin-app]** > **[!UICONTROL Instellingen]** > **[!UICONTROL Locaties van lesruimte]** > **[!UICONTROL Toevoegen]**, klikt u op **[!UICONTROL Locaties voor bulkimport]** knop. Blader naar de locatie met het CSV-bestand en selecteer het bestand.

Het CSV-bestand maakt gebruik van deze velden om details over een of meer klaslokalen op te slaan:

* name
* info
* url
* seatLimit

U kunt de koppen aanpassen.

Het CSV-bestand moet verplicht alle kolommen in dezelfde volgorde bevatten zoals hier aangegeven.

Nadat het systeem het CSV-bestand heeft geïmporteerd, worden de locaties toegevoegd aan de bibliotheek.

## Klaslokalen zoeken

Een auteur of beheerder kan beginnen met het typen van de locatienaam, waarna de relevante resultaten worden weergegeven. Vervolgens kan de auteur of beheerder een locatie selecteren uit de weergegeven resultaten. Als er geen locatie in de typeahead-resultaten wordt weergegeven, kan de gebruiker nog steeds de nieuwe locatienaam van het klaslokaal toevoegen. Houd er rekening mee dat deze locatienaam die is gemaakt met behulp van de workflow voor het maken van sessies niet wordt toegevoegd aan de bibliotheek met locaties die door de beheerder is gemaakt.

Wanneer een klaslokaal wordt toegevoegd, geeft het leerplatform ook aan of het klaslokaal al is geboekt voor de aangegeven periode. Er worden zelfs alternatieve periodes geboden als suggestie. Hierdoor kan de auteur de vergadertijd aanpassen als hij of zij besluit dezelfde locatie van een klaslokaal te gebruiken.

![](assets/classroom-search.png)

*Zoeken naar lesruimten*

## Beperken tot een vooraf bepaalde lijst met docenten

Momenteel kunnen de gebruikers elke geregistreerde gebruiker als docent toevoegen bij het maken van een klassikale of virtuele sessie. Deze functionaliteit blijft ongewijzigd in deze release.

Beheerders hebben nu echter een extra optie om verder te bepalen wie als docent wordt toegewezen op het leerplatform. Zo wordt voorkomen dat er per ongeluk een nieuwe docent wordt toegevoegd bij het maken van een sessie.

## Beheerder

Een beheerder kan de **[!UICONTROL Beheer van docenten]** optie (beschikbaar onder **[!UICONTROL Admin-app]** > **[!UICONTROL Instellingen]** > **[!UICONTROL Algemeen]**) om ervoor te zorgen dat alleen gebruikers die vooraf bepaalde docenten zijn, kunnen worden toegevoegd als docent voor een sessie.

Beheerders kunnen een docent instellen door **[!UICONTROL BEHEREN]** > **[!UICONTROL Gebruikers]** om de pagina Gebruikersbeheer te openen, selecteert u een gebruiker en wijst u vervolgens de rol van docent toe aan de gebruiker (met **[!UICONTROL Handelingen]** > **[!UICONTROL Rol toewijzen]**).

## Auteur

Als de beheerder de optie **[!UICONTROL Docentbeheer]** selecteert, kan een auteur alleen gebruikers met de rol Docent zoeken en toevoegen aan de klassikale sessies, virtuele sessies, checklists en de modules voor het verzenden van bestanden.

Daarnaast kan een auteur:

* Docenten toevoegen aan en verwijderen uit de bestaande sessies.
* Docenten toevoegen aan de bestaande sessies die al een of meer docenten hebben.

Daarom kunnen alleen de gebruikers met de rol Docent worden toegevoegd als docent nadat een beheerder de optie **[!UICONTROL Docentbeheer]** heeft ingeschakeld.

>[!NOTE]
>
>Dit is niet van toepassing wanneer u sessies migreert met het CSV-bestand voor sessies. In dit geval kan een gebruiker die niet de rol van docent heeft, worden toegevoegd als docent.

## Bestaande sessie annuleren

Een auteur of beheerder kan een sessie annuleren en indien nodig opnieuw plannen.

Wanneer een gebruiker een sessie annuleert, stuurt het systeem een e-mail voor het annuleren van een vergadering naar alle ingeschreven studenten en docenten. De e-mail bevat de bijgewerkte sessiedetails.

Er is een sjabloon met de naam **[!UICONTROL Sessie annuleren]** die helpt bij het annuleren van een sessie.

Op de pagina **[!UICONTROL Cursusinstantie]** staat voor elke sessie die onder een cursusinstantie wordt vermeld een optie om de sessie te annuleren.

![](assets/cancel-session.png)

*Een bestaande sessie annuleren*

Wanneer u op de link **[!UICONTROL Sessie annuleren]** klikt, verschijnt er een waarschuwingsbericht.

Als u in het dialoogvenster voor het waarschuwingsbericht op **[!UICONTROL Doorgaan]** klikt, annuleert het systeem de sessie.

Het systeem wist ook de volgende gegevens na het annuleren van een sessie:

* Begindatum van de sessie
* Einddatum van de sessie
* Begintijd van de sessie
* Eindtijd van de sessie
* Docenten die aan de sessie zijn toegevoegd
* URL van virtueel klaslokaal
* Locatie die aan de sessie is toegevoegd
* Wachtlijstlimiet die door de docent is toegevoegd

## Beheerder

Op de pagina **[!UICONTROL Cursusinstantie]** kan een beheerder een of meer sessies annuleren. Nadat de beheerder een sessie heeft geannuleerd, wist het systeem alle sessiedetails behalve de plaatslimiet.

Daarnaast kan een beheerder:

* De ingeschreven studenten en studenten op de wachtlijst van een sessie bekijken.
* Studenten uitschrijven van een cursus met een of meer geannuleerde sessies.
* Aanwezigheid voor sessies markeren die zijn geannuleerd.
* Een cursus als voltooid markeren die een of meer geannuleerde sessies bevat.
* Een geannuleerde sessie opnieuw plannen.
* Een docent toevoegen aan een geannuleerde sessie wanneer deze opnieuw wordt gepland.

Houd er rekening mee dat zelfs na annulering de studenten die zijn ingeschreven voor de trainingsinstantie ingeschreven blijven. Hun inschrijvingsstatus - inclusief bevestigde inschrijving, wachtlijst en wachtrijgoedkeuring van de manager - verandert niet. Dit is handig omdat de beheerder de geannuleerde sessie in de toekomst kan instellen en opnieuw kan plannen.

## Auteur

Op de pagina **[!UICONTROL Cursusinstantie]** kan een auteur een of meer sessies annuleren. Nadat de auteur een sessie heeft geannuleerd, wist het systeem alle sessiedetails behalve de plaatslimiet.

Daarom kan een auteur de opdracht **[!UICONTROL Sessie annuleren]** koppelingen om een of meer klassikale sessies of virtuele klassikale sessies te annuleren die beschikbaar zijn in dezelfde of verschillende cursusinstanties.
