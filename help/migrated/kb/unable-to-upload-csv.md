---
description: Tijdens het uploaden van een CSV verschijnt een foutmelding. Lees verder om het probleem op te lossen.
jcr-language: en_us
title: Kan geen CSV uploaden
contentowner: saghosh
source-git-commit: 8b29ac996962e7ce8fbda51f3421c9a5f248fcf6
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 71%

---



# Kan geen CSV uploaden

## Fout: Gegevens afgekapt: Gegevens te lang voor kolom

Als u een CSV uploadt in Adobe Learning Manager, ziet u de volgende foutmelding.

![](assets/csv-upload-failed.png)

*Foutbericht dat de CSV-verwerking is mislukt*

## Oorzaak

De fout treedt op als de gegevens in de opgegeven kolom de tekenlimiet overschrijden die is gedefinieerd voor de kolom.

## Resolutie

* Open de CSV.
* Controleer de gegevens in de kolom die wordt genoemd in de foutmelding.
* Als er een waarde is die veel tekens bevat (bijvoorbeeld meer dan 60 tekens), wijzigt u de waarde om de gegevens te corrigeren.

## Fout: Eerste kolom in de CSV geeft een speciaal teken weer

U kunt een CSV niet uploaden, omdat in de eerste kolom een speciaal teken staat wanneer u de kolommen toewijst.

![](assets/csv-2.png)

*Speciaal teken in de kolom Naam*

## Oorzaak

Het probleem treedt op wanneer de CSV wordt opgeslagen in een UTF-8-indeling in Excel. Als u een CSV in Excel opslaat als UTF-8, wordt het bestand opgeslagen in een UTF-BOM-indeling. U kunt dit verifiëren met Notepad++ of door een CSV te uploaden naar Learning Manager. Bij het toewijzen van de kolommen wordt in de eerste kolom een speciaal teken weergegeven.

## Resolutie

* **A:** Opslaan via Excel:

   1. Open de CSV in Excel.
   1. Sla het bestand op als een normale CSV.

* **B:** Opslaan via Kladblok of Kladblok++:

   * Open de CSV in Notepad of Notepad++.
   * Sla het bestand op in een UTF-8-indeling.

## Fout: E-mailadres of gebruiker bestaat al in het systeem

U kunt een CSV niet uploaden, omdat het verwerken van de CSV is mislukt. U ziet het onderstaande foutbericht:

![](assets/csv-3.png)

*Foutbericht voor een dubbele gebruiker*

## Oorzaak

Dit probleem treedt op als er een gebruiker is die al in het systeem staat met hetzelfde e-mailadres of dezelfde UUID.

## Resolutie

### Scenario 1

**Accounts waarvoor UUID niet is ingeschakeld.**

In dit scenario zijn er twee redenen voor deze fout:

1. De gebruiker die u probeert toe te voegen, is een manager van een extern profiel. Open het externe profiel waarvan de gebruiker deel uitmaakt, selecteer de gebruiker en klik op **[!UICONTROL Handelingen]** > **[!UICONTROL Rol toewijzen]** > **[!UICONTROL Manager]** en wijzig de manager van het profiel.
1. De gebruiker die u wilt toevoegen, is gewist. In dit scenario kunt u de gebruiker pas met hetzelfde e-mailadres toevoegen als het leegmaken is voltooid. Als tijdelijke oplossing**: a**voeg de gebruiker een secundair e-mailadres toe om toegang tot het platform te bieden. Wanneer het opschoningsproces is voltooid, bewerkt u de gebruiker en wijzigt u het e-mailadres naar het juiste e-mailadres.

### Scenario 2

**Voor UUID ingeschakelde accounts.**

Dit probleem kan optreden bij accounts waarvoor UUID is ingeschakeld als een gebruiker is toegewezen aan een UUID die al wordt gebruikt door een andere gebruiker van het account of als de gebruiker een ander e-mailadres heeft.

Stel dat er twee gebruikers zijn, A en B, met e-mailadressen,  <a@xyz.com> en <b@xyz.com> met UUID 1 respectievelijk 2.

Als u een CSV uploadt met de UUID van A als 3 en de UUID van gebruiker B als 2, krijgt u een foutmelding te zien.

>[!TIP]
>
>U lost dit probleem als volgt op: **u moet hetzelfde e-mailadres en dezelfde UUID voor de gebruiker hebben op de CSV en het systeem.**

