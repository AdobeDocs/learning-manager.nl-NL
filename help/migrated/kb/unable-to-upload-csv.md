---
description: Tijdens het uploaden van een CSV-bestand wordt een fout weergegeven. Lees verder om het probleem op te lossen.
jcr-language: en_us
title: Kan CSV niet uploaden
contentowner: saghosh
source-git-commit: 8b29ac996962e7ce8fbda51f3421c9a5f248fcf6
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---



# Kan CSV niet uploaden

## Fout: gegevens afbreken: gegevens te lang voor kolom

Wanneer u probeert een CSV te uploaden in Adobe Learning Manager, wordt het volgende foutbericht weergegeven.

![](assets/csv-upload-failed.png)

*Foutbericht dat de CSV-verwerking is mislukt*

## Oorzaak

De fout treedt op als de gegevens in de opgegeven kolom de tekenlimiet overschrijden die is gedefinieerd voor de kolom.

## Resolutie

* Open de CSV.
* Controleer de gegevens in de kolom die in de fout wordt vermeld.
* Wanneer een waarde groot is (bijvoorbeeld groter dan 60 tekens), wijzigt u de waarde om de gegevens te corrigeren.

## Fout: in de eerste kolom van de CSV wordt een speciaal teken weergegeven

U kunt een CSV niet uploaden omdat in de eerste kolom een speciaal teken wordt weergegeven wanneer de kolommen worden toegewezen.

![](assets/csv-2.png)

*Speciaal teken in de kolom Naam*

## Oorzaak

Dit probleem doet zich voor wanneer de CSV wordt opgeslagen als een UTF-8-indeling in Excel. Als u een CSV in Excel opslaat als UTF-8, wordt het bestand opgeslagen in een UTF-BOM-indeling. U kunt dit verifiëren met Kladblok++ of wanneer u een CSV uploadt naar Leermanager, terwijl u de kolommen toewijst, geeft de eerste kolom een speciaal teken weer.

## Resolutie

* **A:** Opslaan via Excel:

   1. Open CSV in Excel.
   1. Sla het bestand op als een normale CSV.

* **B:** Opslaan via Kladblok of Kladblok++:

   * Open CSV in Kladblok of Kladblok++.
   * Sla het bestand op in een UTF-8-indeling.

## Fout: e-mailadres van gebruiker al aanwezig in systeem

U kunt een CSV niet uploaden omdat de CSV-verwerking is mislukt. U ziet hieronder het foutbericht:

![](assets/csv-3.png)

*Foutbericht voor een dubbele gebruiker*

## Oorzaak

Dit probleem treedt op als er een gebruiker met hetzelfde e-mailadres of dezelfde UUID aanwezig is op het systeem.

## Resolutie

### Scenario 1

**Accounts waarvoor UUID niet is ingeschakeld.**

In dit scenario zijn er twee redenen voor deze fout:

1. De gebruiker die u wilt toevoegen, is een manager van een extern profiel. Open het externe profiel waarvan de gebruiker deel uitmaakt, selecteer de gebruiker en klik op **[!UICONTROL Handelingen]** > **[!UICONTROL Rol toewijzen]** > **[!UICONTROL Manager]** en wijzig de manager van het profiel.
1. De gebruiker die u wilt toevoegen, is gewist. In dit scenario kunt u de gebruiker pas met hetzelfde e-mailadres toevoegen als het leegmaken is voltooid. Als tijdelijke oplossing**: a**voeg de gebruiker een secundair e-mailadres toe om toegang tot het platform te bieden. Als het leegmaken is voltooid, bewerkt u de gebruiker en wijzigt u het e-mailadres in het juiste e-mailadres.

### Scenario 2

**Voor UUID ingeschakelde accounts.**

Voor UUID-accounts kan dit probleem optreden als aan een gebruiker een UUID is toegewezen die al door een andere gebruiker in het account wordt gebruikt of als de gebruiker een ander e-mailadres heeft.

Stel dat er twee gebruikers zijn, A en B, met e-mailadressen,  <a@xyz.com> en <b@xyz.com> met UUID 1 respectievelijk 2.

Als u nu een CSV uploadt met de UUID van gebruiker A als 3 en de UUID van gebruiker B als 2, dan verschijnt er een fout.

>[!TIP]
>
>U lost dit probleem als volgt op: **u moet hetzelfde e-mailadres en dezelfde UUID voor de gebruiker hebben op de CSV en het systeem.**

