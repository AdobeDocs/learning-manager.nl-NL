---
description: Leer hoe u het studenttranscript kunt downloaden op basis van gebruikers, leerobjecten of vaardigheden in Leermanager.
jcr-language: en_us
title: Studenttranscripten
source-git-commit: a495c86f8dff3ebc51e7700a3f3bcf7ce57d1311
workflow-type: tm+mt
source-wordcount: '917'
ht-degree: 0%

---



# Studenttranscripten

Leer hoe u het studenttranscript kunt downloaden op basis van gebruikers, leerobjecten of vaardigheden in Leermanager.

Met Adobe Learning Manager kunnen de managers van een organisatie de transcripten genereren die aan studenten zijn gekoppeld.

## Studenttranscripten genereren {#generatelearnertranscripts}

1. Klik op **[!UICONTROL Rapporten]** in het linkerdeelvenster in de manageraanmelding.
1. Klikken **[!UICONTROL Mijn rapporten]** op de pagina.
1. Klikken **[!UICONTROL Studenttranscripten]** koppeling.

   ![](assets/learner-transcripts.png)

   *Rapporten maken voor studenttranscripten*

1. Het dialoogvenster Studenttranscripten verschijnt. Kies het datumbereik waarvoor het transcript moet worden gegenereerd.

   >[!NOTE]
   >
   >Standaard is de startdatum de registratiedatum van de student en is de einddatum altijd de huidige datum. U kunt alleen de begindatum wijzigen vanaf wanneer u de gegevens nodig hebt.

1. Kies de namen van de studenten in het veld Studenten selecteren en klik op **[!UICONTROL Genereren]**.

U kunt één student of groepen studenten kiezen. Klik op Meer studenten toevoegen om meer dan één student toe te voegen.

Transcripties worden als XLS-bestanden gegenereerd en naar uw computer gedownload. Elk Excel-bestand (.xls) heeft zeven bladen, waarvan de details hieronder worden vermeld:

## Studenttranscript downloaden op basis van tijdzone {#lt-timezone}

Net als een beheerder kan een manager ook de kolommen kiezen die u wilt exporteren. Bovendien kan een manager het Studenttranscript downloaden op basis van de tijdzone die hij/zij in de profielinstellingen heeft geselecteerd.

Als de manager deze optie inschakelt, wordt de tijdzone gekozen uit de tijdzone die is ingesteld op de pagina Profielinstellingen, die hieronder wordt weergegeven.

>[!NOTE]
>
>Voor een nieuwe manager is het selectievakje Tijdzone uitgeschakeld.

![](assets/image030.png)

*Studenttranscripten voor een bepaald tijdbereik downloaden*

## Inhoud van het studenttranscriptbestand {#learnertranscriptfilecontent}

Een typisch studenttranscriptbestand bestaat uit zes Excel-bladen in één bestand. De studenttranscriptbladen bieden een algemeen inzicht in gegevens, waaronder het aantal studenten per cursus, hun vaardigheden, het competitiepercentage op basis van de cursus of student en een dashboard Naleving. De volgende dashboards zijn beschikbaar in studenttranscripten:

**Studenttranscript**

In het Excel-blad van het studenttranscript worden naast profielgegevens over de student ook de consumptiedetails van leerobjecten gegeven, zoals inschrijvingsdatum, startdatum, behaalde score, behaalde quizscore enzovoort. Als cursussen deel uitmaken van een leerprogramma, worden ze apart vermeld, los van de individuele gegevens over het cursusverbruik.

**1 - Dashboard Leeractiviteit**

In dit LO-specifieke dashboard kunt u het aantal studenten voor elke cursus, leerprogramma of certificering bekijken. U kunt het voortgangsblad voor studenten voor een bepaald leerobject bekijken. Op dit blad staan gegevens zoals het aantal studenten dat de cursus of het leerprogramma heeft voltooid, de studenten die bezig zijn en de vervaldatums van de studenten.

De voortgang van gebruikers voor de specifieke cursus wordt berekend op basis van de invoervelden waarin u de vervaldatum en drempels voor voortgangspercentages opgeeft. Als u bijvoorbeeld 7 dagen en 70% opgeeft als de waarden in uw invoerveld, wordt de voortgang van de cursus weergegeven voor cursussen die over 7 dagen moeten worden afgerond en voor cursussen die meer dan 70% vooruit zijn. U kunt ook de tijdsperiode wijzigen in dit blad, waar de gewijzigde gegevens automatisch worden weergegeven op dit dashboard.

**2 - Dashboard Leeractiviteit**

Dit leerdashboard geeft gegevens voor een specifieke gebruiker weer. Vanuit dit dashboard kunt u de cursussen, leerprogramma&#39;s of certificeringen zien waarvoor een bepaalde gebruiker zich heeft ingeschreven. De tabel bevat ook gegevens over de leerobjecten die de gebruiker heeft voltooid, de leerobjecten die worden uitgevoerd en de aanstaande vervaldatums voor de gebruiker.

De voortgang van de gebruikers voor elke cursus wordt berekend op basis van de invoer die u opgeeft. Dat wil zeggen, de vervaldatum en het voortgangspercentage. Als u bijvoorbeeld 7 dagen en 70% opgeeft als de waarden in uw invoerveld, wordt de voortgang van de gebruiker weergegeven voor verschillende cursussen die over 7 dagen moeten worden afgerond en voor cursussen die meer dan 70% vooruit zijn.

**Vaardigheid**

Op het vaardighedenblad worden de vaardigheidsnaam, het vaardigheidsniveau, de vereiste studiepunten, de behaalde studiepunten, het voltooiingspercentage en andere profielgegevens vermeld. Hieronder vindt u ter referentie een voorbeeld van het vaardighedenExcel-blad.

**Vaardigheidsdashboard**

In dit dashboard kunt u zien of uw organisatie is uitgerust met verschillende vaardigheden. Voor een specifieke vaardigheid kunt u het aantal gebruikers in een organisatie controleren die geacht worden deze vaardigheid te hebben versus het aantal dat de vaardigheid eigenlijk heeft. Dit dashboard specificeert ook de gebruikers die hun vaardigheden zouden kunnen moeten verfrissen. Deze waarde wordt berekend op basis van de invoer die u invoert in het invoerveld. Als u bijvoorbeeld 50 dagen invoert, bevat het dashboard gegevens over gebruikers die na 50 dagen hun vaardigheden moeten vernieuwen.

Dit vaardigheidsdashboard is meer gebruikersspecifiek. U kunt een specifieke gebruiker of meerdere gebruikers filteren en hun vaardigheidsniveau als een dashboard bekijken. Dit blad kan managers en beheerders helpen bij het volgen van de vaardigheden van elke student in vergelijking met de vaardigheden die ze moeten hebben. Het dashboard Vaardigheden laat ook zien welke studenten hun vaardigheden moeten vernieuwen. De lijst voor het vernieuwen van studenten wordt berekend op basis van het aantal dagen dat u in het invoerveld invoert.

**Dashboard Naleving**

Het dashboard Naleving bestaat uit twee delen: nalevingsrapport per gebruiker en nalevingsrapport per training. Voor het op gebruikers gebaseerde rapport kunt u het dashboard Naleving gebruiken om gebruikers bij te houden met aanstaande vervaldatums voor belangrijke nalevingsinitiatieven. Voor het trainingsgebaseerde rapport kunt u filteren op leerprogramma of certificering.

Voor beide compatibiliteitsrapporten filtert u op de vervaldatum om de juiste gegevens te bekijken.
