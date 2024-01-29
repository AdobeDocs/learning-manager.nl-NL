---
title: Meerdere inschrijvingen in Adobe Learning Manager
description: Als accountbeheerder is een van uw primaire taken het maken van verschillende exemplaren van VILT-sessies in verschillende tijdzones en het mogelijk maken van sessies voor specifieke gebruikersgroepen.
source-git-commit: fc5b5afd8dd42ac3aa0e5190d6f421035df41a89
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 0%

---

# Meerdere inschrijvingen in Adobe Learning Manager

In Adobe Learning Manager kan elke cursus verschillende instanties hebben. Als accountbeheerder is een van uw primaire taken het maken van verschillende exemplaren van VILT-sessies in verschillende tijdzones en het mogelijk maken van sessies voor specifieke gebruikersgroepen.

Vóór de release van juli 2023 konden een beheerder een student inschrijven en zich in slechts één instantie inschrijven. Als een student een cursus in verschillende instanties wilde volgen, zou de beheerder veel cursussen maken, één voor elke instantie.

Met de functie voor meervoudige aanmelding van Adobe Learning Manager kan een beheerder dergelijke scenario&#39;s vermijden.

## Wat is meervoudige inschrijving?

Meerdere inschrijvingen schrijven een student meerdere keren in een cursus in via verschillende beschikbare instanties.  Een student kan zich in meerdere cursusinstanties inschrijven, ongeacht de status waarvoor hij of zij zich heeft ingeschreven, die is voltooid of nog moet starten. Wanneer de auteur de [!UICONTROL Meerdere inschrijvingen] schakelt, kan een student zich vervolgens in meerdere instanties van de cursus inschrijven.

![afbeelding met meerdere inschrijvingen](assets/multi-enrollment-author.png)
*Meerdere inschrijvingen starten vanuit instellingen*

De voortgang van elke instantie kan afzonderlijk worden bijgehouden en er kan een rapport worden geëxporteerd om de voortgang van elke instantie bij te houden.

## Belangrijke punten

* Meerdere inschrijvingen is alleen van toepassing wanneer een cursus meerdere instanties heeft.
* Als de optie voor meerdere inschrijvingen is ingeschakeld en gebruikers in meerdere instanties zijn ingeschreven, worden voor elke cursus nieuwe rijen gemaakt in het rapport Studenttranscript (één rij voor elke instantie en elke student)
* Als de rapportautomatisering is ingesteld die slechts één rij per cursus verwacht, moet u de vereiste aanpassingen aanbrengen in de rapportautomatisering voordat u de functie voor meervoudige inschrijving inschakelt.

## Meerdere inschrijvingen inschakelen

1. Meld u als auteur aan bij uw Adobe Learning Manager-account.
1. Selecteer de cursus waarvoor u studenten meerdere keren wilt inschrijven.
1. Selecteer in het linkerdeelvenster de optie **[!UICONTROL Instellingen]** > **[!UICONTROL Bewerken]** > **[!UICONTROL Instantieconfiguratie]** > **[!UICONTROL Meerdere inschrijvingen inschakelen]**.

![afbeelding met meerdere inschrijvingen](assets/multi-enrollment-author.png)
*Meerdere inschrijvingen inschakelen*

>[!NOTE]
>
>Als auteur kunt u niet tegelijkertijd Instantie wisselen en Meerdere inschrijvingen inschakelen.

## Studentenweergave

Meerdere inschrijvingen zijn handig wanneer een student zich wil inschrijven voor een klassikale of VC-cursus of een cursus opnieuw wil voltooien voordat hij/zij naar een andere cursus gaat.

Voor studenten die zich niet hebben ingeschreven, zien ze, wanneer ze een cursus selecteren, het scherm onder de cursus met meerdere instanties. Vervolgens kunnen ze elke instantie selecteren en zich inschrijven.

![afbeelding van studentenweergave](assets/learner-view.png)
*De instanties weergeven*

Nadat ze zich in één instantie hebben ingeschreven, kunnen ze zich in andere gevallen inschrijven door de optie Alle instanties weergeven in het rechterdeelvenster te selecteren.

![afbeelding van meerdere inschrijvingscursussen](assets/enroll-instance.png)
*Inschrijven voor een instantie*

De voortgang van elke instantie kan als volgt worden bijgehouden:

![voortgang bijhouden](assets/check-progress.png)
*Voortgang van elke instantie bijhouden*

## Wijzigingen in meerdere inschrijvingen in de beheerder

**Inschrijving:**

Tijdens het inschrijven van de studenten kunt u het volgende selectievakje inschakelen:

*&quot;Geselecteerde studenten zijn mogelijk al ingeschreven voor andere cursusinstanties. Laat deze studenten ook voor het exemplaar inschrijven...&quot;*

![wijzigingen in beheer](assets/admin-changes.png)
*Inschrijvingsoptie voor beheerders*

Als de student al voor één instantie is ingeschreven en u als beheerder probeert de student in te schrijven voor een andere cursusinstantie, selecteert u Ja.

## Rapportage

Voor een student die voor twee instanties van dezelfde cursus is ingeschreven, worden voor elke cursusinstantie twee rijen gemaakt. Het rapport geeft ook de voortgang van de instanties weer.
