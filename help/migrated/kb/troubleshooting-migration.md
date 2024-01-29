---
description: Dit document bevat basistips voor het oplossen van problemen om een aantal typische problemen op te lossen die u kunt tegenkomen tijdens het migreren van gegevens en inhoud van bestaand LMS naar Leermanager.
jcr-language: en_us
title: Problemen met migratie oplossen
contentowner: jayakarr
source-git-commit: 6abc118c6ad7e66e3ded5bd26b9167c3a0b99e4b
workflow-type: tm+mt
source-wordcount: '854'
ht-degree: 0%

---



# Problemen met migratie oplossen

Dit document bevat basistips voor het oplossen van problemen om een aantal typische problemen op te lossen die u kunt tegenkomen tijdens het migreren van gegevens en inhoud van bestaand LMS naar Leermanager.

## Algemene migratiekwesties {#genericmigrationissues}

### Kan niet aanmelden bij FTP-map of -inhoudsmap {#unabletologintoftpfolderorcontentfolder}

Zorg ervoor dat uw accounts zijn gemaakt in de FTP- en Box-services. Wanneer u een migratieproject maakt, vraagt u deze twee services in te stellen. Zodra u de services maakt, ontvangt u e-mails van Exavault en Box om de wachtwoorden opnieuw in te stellen of in te stellen. Als u de wachtwoorden niet meer onthoudt, kunt u deze opnieuw instellen op de Exavault- en Box-websites.

### Taken worden niet weergegeven, zelfs niet nadat op de knop Vernieuwen is geklikt {#jobsarenotreflectedevenafterclickingrefreshbutton}

* Zorg ervoor dat de CSV-bestanden naar de juiste map in Exavault FTP worden geüpload. De padstructuur moet als volgt zijn:

`code Account>Project>Sprint location`

* Zorg ervoor dat de bestandsnamen van CSV-bestanden overeenkomen met de CSV-specificatienamen:

   * course.csv
   * course_instance.csv
   * course_module.csv
   * enrollment.csv
   * module.csv
   * module_version.csv
   * user_course_grade.csv

### Fouten worden weergegeven voor taken met foutrecords {#failuresareshownforjobswitherrorrecords}

1. Download de foutenlogboeken door te klikken **Foutrecords downloaden** link
1. De oorspronkelijke CSV&#39;s corrigeren op basis van de gerapporteerde fouten, en
1. Voer de sprint opnieuw uit met de gewijzigde CSV&#39;s.

U kunt het beste aangepaste CSV&#39;s in een nieuwe sprint uitvoeren als het aantal wijzigingen lager is dan het totale aantal records.

### Aanmelden bij Leerbeheertoepassing is niet mogelijk, zelfs niet nadat de sprintmigratie is gestopt {#unabletologintocaptivateprimeapplicationevenafterstoppingthesprintmigration}

Het kan 10 tot 15 minuten duren om een account te ontgrendelen zodra een sprintrun is gestopt of voltooid. Probeer de toepassing na 15 minuten te openen.

### Sommige migratietaken geven de status &#39;In bewerking&#39; weer, zelfs nadat &#39;Stoppen&#39; is geactiveerd. {#someofthemigrationjobsdisplayinprogressstatusevenafterstopistriggered}

Het kan 10 tot 15 minuten duren voordat de uitvoering van alle taken is gestopt als de status &#39;In bewerking&#39; is bereikt. Controleer de status na 10 minuten opnieuw.

### Kan geen sprint maken omdat de knop is uitgeschakeld {#unabletocreateasprintasthebuttonisdisabled}

Zorg ervoor dat de huidige sprint is gemarkeerd als voltooid voordat u een sprint maakt. Klikken **[!UICONTROL Mark Sprint voltooid]** boven aan de pagina om een sprintmigratie te voltooien.

### Kan een migratieproject niet als voltooid markeren omdat de knop is uitgeschakeld {#unabletomarkamigrationprojectascompleteasthebuttonisdisabled}

Zorg ervoor dat de huidige sprint als voltooid is gemarkeerd voordat u de voltooiing van het migratieproject markeert. Klikken **[!UICONTROL Mark Sprint voltooid]** boven aan de pagina om een sprintmigratie te voltooien.

## CSV-problemen {#csvissues}

### module_version.csv de dossiermigratie ontbreekt en de inhoud wordt nog niet gemigreerd {#moduleversioncsvfilemigrationisfailingandcontentisnotmigratedyet}

Zorg ervoor dat de inhoud beschikbaar is in de map Inhoud (Box-account onder het opgegeven migratieproject, sprintpad). Zorg er ook voor dat u de optie **Ja** for **Wilt u inhoud voor deze sprint migreren?** vraag op de pagina Sprint maken.

Als u vergeet te selecteren **Ja** en verder te gaan in deze sprint, moet u wachten tot u deze sprint hebt voltooid. Maak een andere sprint en klik op **[!UICONTROL Ja]**.

### enrollment.csv- of user_course_grade.csv-records mislukken met het foutbericht &#39;Geen geldige Leermanager-id&#39; {#enrollmentcsvorusercoursegradecsvrecordsfailwithanerrormessagenotavalidprimeid}

Zorg ervoor dat de e-mail-ID die als onderdeel van de gebruikers-ID, toegewezenByUserID-velden, bij geldige gebruikers van de Learning Manager hoort. Zo niet, voeg dan de gebruiker toe en maak een nieuwe sprint met **Gebruikers synchroniseren** geselecteerd. Als de gebruiker geen deel uitmaakt van de organisatie, voegt u de gebruiker toe als een verwijderde gebruiker in Leerbeheer met de CSV-specificatie Gebruikers toevoegen. Hieronder vindt u een voorbeeld van een CSV-specificatie om verwijderde gebruikers toe te voegen.

[Users.csv](assets/users.zip) Raadpleeg **CSV-specificaties en voorbeeld-CSV&#39;s** sectie in [Migratiehandleiding](../integration-admin/feature-summary/migration-manual.md) om een volledige set CSV-specificaties en voorbeeld-CSV-bestanden te downloaden.

### Er worden lege of onjuiste modules voor een gemigreerde cursus afgespeeld {#coursesappearblankorincorrectmodulesplayforamigratedcourse}

Zorg ervoor dat de **moduleOrderInCourse** sleutelwaarde voor een cursus begint met **0** en in doorlopende volgorde is. De volgorde voor courseModuleType moet PRETEST, TESTOUT, CONTENT zijn

Zorg er ook voor dat twee versies van Activiteit, Lesruimte en VC niet zijn gekoppeld aan de bestaande Cursus.

### Een bericht ontvangen als &#39;Module is al gekoppeld aan een bestaande cursus&#39; {#receivingamessageasmoduleisalreadylinkedwithanexistingcourse}

Leermanager staat het koppelen van de module Activiteit/VC/Lesruimte aan meer dan één cursus niet toe. Zorg ervoor dat de module niet is gekoppeld aan andere cursussen.

### Alle cursussen tonen de nieuwste versie van de modules Activiteit/VC/Lesruimte, ook al zijn de cursussen gekoppeld aan verschillende moduleversies {#allthecoursesshowthelatestversionofactivityvcclassroommoduleseventhoughthecoursesarelinkedwithdifferentmoduleversions}

Versioning van de modules Activiteit, Lesruimte en Virtuele lesruimte wordt niet ondersteund in Leerbeheer. Als u versies aanbiedt via het bestand moduleVersion.csv, wordt het bestaande bestand bijgewerkt en wordt er geen nieuwe versie gemaakt.

### Gewenste duur wordt niet weergegeven voor gemigreerde activiteit/VC/klassikale module {#desireddurationdoesnotappearforamigratedactivityvcclassroommodule}

Gewenste duur is geen geldige waarde voor de module Activiteit/VC/Lesruimte.

### De hyperlink-URL wordt niet geopend in Leerbeheer {#hyperlinkurldoesntopenupincaptivateprime}

Zorg ervoor dat de beschikbare koppelingen vooraf zijn vastgelegd met &#39;http://&#39; of &#39;https://&#39;

### Migratie van moduleVersion mislukt met fouten &#39;Bestand niet gevonden&#39; {#moduleversionmigrationfailswithfilenotfounderrors}

Zorg ervoor dat het bestand waarnaar wordt verwezen aanwezig is in de inhoudsmap en dat het is gemigreerd.

### De migratie van de moduleVersion mislukt met een foutbericht als &#39;Er is een interne fout opgetreden - voor Module : x en moduleVersion : y&#39; {#moduleversionmigrationfailswithanerrormessageasaninternalerrorhasoccurredformodulexandmoduleversiony}

Voer de sprint opnieuw uit om het probleem op te lossen.
