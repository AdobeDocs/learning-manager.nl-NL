---
description: Dit document bevat basistips voor probleemoplossing om enkele van de veelvoorkomende problemen op te lossen die u kunt tegenkomen bij het migreren van gegevens en inhoud van een bestaand LMS naar Learning Manager.
jcr-language: en_us
title: Migratieproblemen oplossen
contentowner: jayakarr
source-git-commit: 6abc118c6ad7e66e3ded5bd26b9167c3a0b99e4b
workflow-type: tm+mt
source-wordcount: '854'
ht-degree: 71%

---



# Migratieproblemen oplossen

Dit document bevat basistips voor probleemoplossing om enkele van de veelvoorkomende problemen op te lossen die u kunt tegenkomen bij het migreren van gegevens en inhoud van een bestaand LMS naar Learning Manager.

## Algemene migratieproblemen {#genericmigrationissues}

### Ik kan me niet aanmelden bij de FTP-map of inhoudsmap {#unabletologintoftpfolderorcontentfolder}

Zorg ervoor dat uw accounts zijn aangemaakt in de FTP- en Box-services. Wanneer u een migratieproject aanmaakt, vraagt u aan dat deze twee services moeten worden ingesteld. Zodra u de services aanmaakt, ontvangt u e-mails van Exavault en Box om de wachtwoorden (opnieuw) in te stellen. Als u de wachtwoorden niet meer weet, kunt u deze opnieuw instellen door naar de websites van Exavault en Box te gaan.

### Taken worden niet weergegeven, zelfs niet nadat u op de knop Vernieuwen hebt geklikt {#jobsarenotreflectedevenafterclickingrefreshbutton}

* Zorg ervoor dat de CSV-bestanden naar de juiste map in Exavault FTP worden geüpload. De padstructuur moet als volgt zijn:

`code Account>Project>Sprint location`

* Zorg ervoor dat de bestandsnamen van de CSV-bestanden overeenkomen met de CSV-specificatienamen:

   * course.csv
   * course_instance.csv
   * course_module.csv
   * enrollment.csv
   * module.csv
   * module_version.csv
   * user_course_grade.csv

### Fouten worden weergegeven voor taken met foutrecords {#failuresareshownforjobswitherrorrecords}

1. Download de foutenlogboeken door op de link **Foutrecords downloaden** te klikken
1. Corrigeer de originele CSV&#39;s op basis van de gerapporteerde fouten en
1. Voer de sprint opnieuw uit met de gewijzigde CSV&#39;s.

U kunt het beste aangepaste CSV&#39;s in een nieuwe sprint uitvoeren als het aantal wijzigingen lager is dan het totale aantal records.

### Ik kan me niet aanmelden bij de Learning Manager-toepassing, zelfs niet na het stoppen van de sprintmigratie {#unabletologintocaptivateprimeapplicationevenafterstoppingthesprintmigration}

Het kan 10 tot 15 minuten duren om een account te ontgrendelen nadat een sprintrun is gestopt of voltooid. Probeer de toepassing na 15 minuten te openen.

### Bij sommige migratietaken wordt de status &#39;In uitvoering&#39; weergegeven, zelfs nadat &#39;Stoppen&#39; is geactiveerd. {#someofthemigrationjobsdisplayinprogressstatusevenafterstopistriggered}

Het kan 10 tot 15 minuten duren om te stoppen met het uitvoeren van alle taken nadat een taak zich in de status &#39;In uitvoering&#39; bevindt. Controleer de status na 10 minuten opnieuw.

### Ik kan geen sprint maken, omdat de knop is uitgeschakeld {#unabletocreateasprintasthebuttonisdisabled}

Zorg ervoor dat de huidige sprint als voltooid is gemarkeerd voordat u een sprint maakt. Klikken **[!UICONTROL Mark Sprint voltooid]** boven aan de pagina om een sprintmigratie te voltooien.

### Ik kan een migratieproject niet als voltooid markeren, omdat de knop is uitgeschakeld {#unabletomarkamigrationprojectascompleteasthebuttonisdisabled}

Zorg ervoor dat de huidige sprint als voltooid is gemarkeerd voordat u het migratieproject als voltooid markeert. Klikken **[!UICONTROL Mark Sprint voltooid]** boven aan de pagina om een sprintmigratie te voltooien.

## CSV-problemen {#csvissues}

### De migratie van het bestand module_version.csv is mislukt en de inhoud is nog niet gemigreerd {#moduleversioncsvfilemigrationisfailingandcontentisnotmigratedyet}

Zorg ervoor dat de inhoud beschikbaar is in de inhoudsmap (Box-account onder het opgegeven migratieproject, sprintpad). Zorg er ook voor dat u de optie **Ja** for **Wilt u inhoud voor deze sprint migreren?** vraag op de pagina Sprint maken.

Als u vergeet **Ja** te selecteren en doorgaat in deze sprint, dan moet u wachten tot u deze sprint hebt voltooid. Maak een andere sprint en klik op **[!UICONTROL Ja]**.

### enrollment.csv- of user_course_grade.csv-records mislukken met het foutbericht &#39;Geen geldige Leermanager-id&#39; {#enrollmentcsvorusercoursegradecsvrecordsfailwithanerrormessagenotavalidprimeid}

Zorg ervoor dat de opgegeven e-mail-ID onderdeel is van userId en de velden assignedByUserID tot geldige Learning Manager-gebruikers horen. Als dit niet het geval is, voeg dan de gebruiker toe en maak een nieuwe sprint met de optie **Gebruikers synchroniseren** geselecteerd. Als de gebruiker geen deel uitmaakt van de organisatie, voegt u de gebruiker toe als een verwijderde gebruiker in Leerbeheer met de CSV-specificatie Gebruikers toevoegen. Hieronder vindt u een voorbeeld van een CSV-specificatie om verwijderde gebruikers toe te voegen.

[Users.csv](assets/users.zip) Raadpleeg **CSV-specificaties en voorbeeld-CSV&#39;s** sectie in [Migratiehandleiding](../integration-admin/feature-summary/migration-manual.md) om een volledige set CSV-specificaties en voorbeeld-CSV-bestanden te downloaden.

### Cursussen worden leeg weergegeven of er worden onjuiste modules afgespeeld voor een gemigreerde cursus {#coursesappearblankorincorrectmodulesplayforamigratedcourse}

Zorg ervoor dat de **moduleOrderInCourse** sleutelwaarde voor een cursus begint met **0** en in doorlopende volgorde is. De volgorde voor courseModuleType moet PRETEST, TESTOUT, CONTENT zijn

Zorg er ook voor dat er niet twee versies van Activiteiten, Klaslokaal en VC aan de bestaande cursus zijn gekoppeld.

### Een bericht ontvangen als &#39;Module is al gekoppeld aan een bestaande cursus&#39; {#receivingamessageasmoduleisalreadylinkedwithanexistingcourse}

In Learning Manager kan de module Activiteiten/VC/Klaslokaal niet aan meer dan één cursus worden gekoppeld. Zorg ervoor dat de module niet aan andere cursussen is gekoppeld.

### Alle cursussen tonen de nieuwste versie van de modules Activiteiten/VC/Klaslokaal, ook al zijn de cursussen gekoppeld aan verschillende moduleversies {#allthecoursesshowthelatestversionofactivityvcclassroommoduleseventhoughthecoursesarelinkedwithdifferentmoduleversions}

Versiebeheer van de modules Activiteiten, Klaslokaal en Virtueel klaslokaal wordt niet ondersteund in Learning Manager. Als u versies opgeeft via het bestand moduleVersion.csv, wordt het bestaande bestand bijgewerkt in plaats van dat er een nieuwe versie wordt gemaakt.

### Gewenste duur wordt niet weergegeven voor de gemigreerde module Activiteiten/VC/Klaslokaal {#desireddurationdoesnotappearforamigratedactivityvcclassroommodule}

Gewenste duur is geen geldige invoer voor de module Activiteiten/VC/Klaslokaal.

### De hyperlink-URL wordt niet geopend in Leerbeheer {#hyperlinkurldoesntopenupincaptivateprime}

Zorg ervoor dat de beschikbare koppelingen vooraf zijn vastgelegd met &#39;http://&#39; of &#39;https://&#39;

### Migratie van moduleVersion mislukt met fouten &#39;Bestand niet gevonden&#39; {#moduleversionmigrationfailswithfilenotfounderrors}

Zorg ervoor dat het bestand waarnaar wordt verwezen, aanwezig is in de inhoudsmap en dat het is gemigreerd.

### De migratie van de moduleVersion mislukt met een foutbericht als &#39;Er is een interne fout opgetreden - voor Module : x en moduleVersion : y&#39; {#moduleversionmigrationfailswithanerrormessageasaninternalerrorhasoccurredformodulexandmoduleversiony}

Voer de sprint opnieuw uit om het probleem op te lossen.
