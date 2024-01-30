---
description: Lees hoe u in Learning Manager een studenttranscript voor managers kunt downloaden op basis van gebruikers, leerobjecten of vaardigheden.
jcr-language: en_us
title: Studenttranscripten
source-git-commit: a495c86f8dff3ebc51e7700a3f3bcf7ce57d1311
workflow-type: tm+mt
source-wordcount: '917'
ht-degree: 84%

---



# Studenttranscripten

Lees hoe u in Learning Manager een studenttranscript voor managers kunt downloaden op basis van gebruikers, leerobjecten of vaardigheden.

Adobe Learning Manager stelt de beheerders van een organisatie in staat om de transcripten van de studenten te genereren.

## Studenttranscripten genereren {#generatelearnertranscripts}

1. Klik op **[!UICONTROL Rapporten]** in het linkerdeelvenster in de manageraanmelding.
1. Klikken **[!UICONTROL Mijn rapporten]** op de pagina.
1. Klikken **[!UICONTROL Studenttranscripten]** koppeling.

   ![](assets/learner-transcripts.png)

   *Rapporten maken voor studenttranscripten*

1. Het dialoogvenster Studenttranscripten verschijnt. Kies het datumbereik waarvoor het transcript moet worden gegenereerd.

   >[!NOTE]
   >
   >Standaard is de startdatum de registratiedatum van de student en is de einddatum altijd de huidige datum. U kunt alleen wijzigen vanaf welke begindatum u de gegevens nodig hebt.

1. Kies de namen van de studenten in het veld Studenten selecteren en klik op **[!UICONTROL Genereren]**.

U kunt kiezen voor één student of groepen studenten. Klik op Meer studenten toevoegen om meer dan een student toe te voegen.

Transcripten worden als XLS-bestanden gegenereerd en naar uw computer gedownload. Elk Excel-bestand (.xls) heeft zeven bladen, waarvan de details hieronder worden vermeld:

## Studenttranscript downloaden op basis van de tijdzone {#lt-timezone}

Een Manager kan, net als een Beheerder, ook kolommen kiezen die geëxporteerd moeten worden. Bovendien kan een manager het Studenttranscript downloaden op basis van de tijdzone die hij/zij in de profielinstellingen heeft geselecteerd.

Als de manager deze optie inschakelt, wordt de tijdzone gekozen uit de tijdzone die is ingesteld op de pagina Profielinstellingen, die hieronder wordt weergegeven.

>[!NOTE]
>
>Voor een nieuwe manager is het selectievakje Tijdzone uitgeschakeld.

![](assets/image030.png)

*Studenttranscripten voor een bepaald tijdbereik downloaden*

## Inhoud van het studenttranscriptbestand {#learnertranscriptfilecontent}

Een typisch studenttranscriptbestand bestaat uit zes Excel-bladen in één bestand. De studenttranscriptbladen geven een algemeen inzicht in gegevens, waaronder het aantal studenten per cursus, hun vaardigheden, het competitiepercentage op basis van de cursus of student, en een dashboard Naleving. De volgende dashboards zijn beschikbaar in studenttranscripten:

**Studenttranscript**

Naast profielgegevens van de student staan in het Excel-blad van het studenttranscript details van gevolgde leerobjecten, zoals inschrijvingsdatum, startdatum, behaalde cijfers, behaalde quizscore, enzovoort. Als cursussen deel uitmaken van een leerprogramma, worden ze apart vermeld, los van de individuele volggegevens van de cursus.

**1- Dashboard Leeractiviteit**

Op dit LO-specifieke dashboard ziet u het aantal studenten per cursus, leerprogramma of certificering. U kunt het voortgangsblad voor studenten voor een bepaald leerobject bekijken. Op dit blad staan gegevens zoals het aantal studenten dat de cursus of het leerprogramma heeft voltooid, studenten die nog bezig zijn en de vervaldatums voor studenten.

De voortgang van de gebruikers voor de specifieke cursus wordt berekend op basis van de invoervelden waar u de vervaldatum en drempels voor voortgangspercentages opgeeft. Als u bijvoorbeeld 7 dagen en 70% als de waarden in uw invoerveld opgeeft, wordt de cursusvoortgang voor cursussen die over 7 dagen moeten zijn afgerond en voor cursussen waarvoor meer dan 70% vooruitgang is geboekt, weergegeven. U kunt in dit blad ook de tijdperiode wijzigen. De gewijzigde gegevens worden vervolgens automatisch op dit dashboard weergegeven.

**2- Dashboard Leeractiviteit**

Dit dashboard toont gegevens voor een specifieke gebruiker. Via dit dashboard kunt u zien voor welke cursussen, leerprogramma&#39;s of certificeringen een bepaalde gebruiker zich heeft ingeschreven. De tabel toont ook gegevens over de leerobjecten die de gebruiker heeft voltooid, de lopende leerobjecten en aanstaande vervaldatums voor de gebruiker.

De voortgang van de gebruikers voor elke cursus wordt berekend op basis van de ingangen die u opgeeft. Dat wil zeggen, de vervaldatum en voortgangspercentages. Als u bijvoorbeeld 7 dagen en 70% als de waarden in uw invoerveld opgeeft, wordt de cursusvoortgang van de gebruiker voor verschillende cursussen die over 7 dagen moeten zijn afgerond en voor cursussen waarvoor meer dan 70% vooruitgang is geboekt, weergegeven.

**Vaardigheid**

Op het vaardighedenblad staan de vaardigheidsnaam, het vaardigheidsniveau, de vereiste studiepunten, de behaalde studiepunten, het voltooiingspercentage en andere profielgegevens. Hieronder ziet u ter referentie een voorbeeld van een vaardighedenblad in Excel.

**Dashboard Vaardigheden**

Op dit dashboard kunt u zien of uw organisatie over verschillende vaardigheden beschikt. U kunt voor een specifieke vaardigheid controleren hoeveel gebruikers in een organisatie geacht worden deze vaardigheid te hebben, tegenover het aantal gebruikers dat de vaardigheid daadwerkelijk heeft. Dit dashboard geeft ook aan welke gebruikers hun vaardigheden moeten opfrissen. Deze waarde wordt berekend op basis van wat u in het invoerveld invoert. Als u bijvoorbeeld 50 dagen invoert, toont het dashboard gegevens van gebruikers die over 50 dagen hun vaardigheden moeten opfrissen.

Dit dashboard is meer gebruikersspecifiek. U kunt hier filteren op een specifieke gebruiker of meerdere gebruikers en hun vaardigheidsniveau als een dashboard bekijken. Dit blad kan managers en beheerders helpen om de vaardigheidsniveaus van iedere student bij te houden ten opzichte van het niveau dat van hen wordt verwacht. Het dashboard Vaardigheden laat ook zien welke studenten hun kennis moeten opfrissen. De lijst met studenten die hun kennis moeten opfrissen, wordt berekend op basis van het aantal dagen dat u in het invoerveld opgeeft.

**Dashboard Naleving**

Het dashboard Naleving bestaat uit twee delen - nalevingsrapport per gebruiker en nalevingsrapport per training. Voor het gebruikersgebaseerde rapport aan de hand van het dashboard Naleving gebruikers volgen met aanstaande vervaldatums voor belangrijke nalevingsinitiatieven. Voor het trainingsgebaseerde rapport kunt u op leerprogramma of certificering filteren.

Filter voor beide nalevingsrapporten op de vervaldatum om de relevante gegevens te bekijken.
