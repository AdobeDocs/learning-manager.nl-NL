---
description: Meer weten over het leegmaken van gebruikersgegevens in Learning Manager.
jcr-language: en_us
title: Gebruikers leegmaken
contentowner: dvenkate
source-git-commit: 53c1a5283295b56424d697bc26c5db31c2edca0f
workflow-type: tm+mt
source-wordcount: '849'
ht-degree: 75%

---



# Gebruikers leegmaken

Meer weten over het leegmaken van gebruikersgegevens in Learning Manager.

## Overzicht {#overview}

Gebruik de functie voor gebruikers leegmaken om persoonlijke identificeerbare informatie en leergegevens van de gebruiker uit Learning Manager te verwijderen. Let op: Gebruiker verwijderen en Gebruiker leegmaken zijn twee verschillende functies. Hoewel een verwijderde gebruiker kan worden hersteld, kunnen niet alle gebruikersgegevens en leerrecords die aan leeggemaakte gebruikers zijn gekoppeld, worden hersteld.

Gebruikers leegmaken kan resulteren in het volgende:

* Als een gebruiker wordt leeggemaakt, werken de koppelingen in importlogboeken niet om het downloaden van oude CSV&#39;s te voorkomen en de gebruikersgegevens opnieuw in het systeem te plaatsen.
* Als auteurs worden leeggemaakt, wordt de naam vervangen door de naam van de beheerder die de gebruiker heeft leeggemaakt.
* Als de docenten worden leeggemaakt, worden ze uit de sessies verwijderd. De beheerder moet voor dergelijke sessies docenten vervangen/toevoegen.
* Als u een gebruiker in Learning Manager leegmaakt, wordt de gebruiker niet uit externe toepassingen (systemen van derden of andere door u geschreven toepassingen) verwijderd. Neem contact op met de eigenaar van de externe toepassing om de gebruikers uit dergelijke toepassingen te laten verwijderen.
* Als in de configuratie-instellingen van een connector naar een leeggemaakte gebruiker wordt verwezen, wordt de connector uitgeschakeld. De connector moet opnieuw worden geconfigureerd door de beheerder om te kunnen worden hervat.

Volg deze stappen om gebruikers leeg te maken:

1. Als beheerder selecteert u **[!UICONTROL Gebruikers]** in het linkerdeelvenster. De pagina **[!UICONTROL Interne gebruikers]** wordt geopend.
1. Verwijder de gebruikers die u wilt leegmaken. Selecteer een of meer gebruikers met behulp van het selectievakje om deze te verwijderen. Open de **[!UICONTROL Handeling]** en selecteert u **[!UICONTROL Gebruiker verwijderen.]**
1. Selecteer in het linkerdeelvenster de optie **[!UICONTROL Gebruikers opschonen]**. De pagina **[!UICONTROL Gebruikers opschonen]** verschijnt met een lijst met verwijderde gebruikers. Gebruik de keuzerondjes om de leeg te maken gebruiker te selecteren. U kunt slechts één gebruiker tegelijk leegmaken.

   ![](assets/purge-1.png)

   *Selecteer een gebruiker die u wilt leegmaken*

1. Open de **[!UICONTROL Handelingen]** en selecteert u **[!UICONTROL Gebruiker leegmaken]**.

   ![](assets/purge-2.png)

   *Selecteer de optie Gebruikers leegmaken*

1. Er verschijnt een dialoogvenster dat waarin om bevestiging wordt gevraagd. Zodra de gebruiker is leeggemaakt, worden alle gebruikersgegevens en leerrecords van de geselecteerde gebruiker permanent verwijderd. Na leegmaken kan de actie niet meer ongedaan worden gemaakt. Klik ter bevestiging op **[!UICONTROL Leegmaken]**.

   ![](assets/purge-3.png)

   *Bevestigingsbericht na leegmaken van een gebruiker*

1. Zodra u deze actie bevestigt en op Leegmaken klikt, wordt het verzoek tot leegmaken geaccepteerd. U ontvangt een melding zodra de actie is voltooid. Er wordt ook een ID voor het verzoek verstrekt. U kunt het ID aan de CSM verstrekken om het verzoek te volgen.

## Gebruikers in bulk leegmaken

U kunt de eerste 50 gebruikers selecteren en de gebruikers in één keer leegmaken. Hierdoor kunnen beheerders 50 gebruikers tegelijkertijd selecteren en leegmaken. Op deze manier kunnen beheerders gebruikers in bulk leegmaken wanneer ze dat willen. Het is het beste om de gebruikers te controleren die zijn geselecteerd voor leegmaken. Dit is belangrijk om ervoor te zorgen dat alleen de juiste groep gebruikers wordt leeggemaakt.

![](assets/bulk-purge-users.png)

*Gebruikers in bulk leegmaken*

+++Lees over de resultaten van de actie Gebruiker leegmaken

<table>
 <tbody>
  <tr>
   <th><strong>Leegmaken met Leermanager UI - Enterprise</strong></th>
   <th> </th>
  </tr>
  <tr>
   <td>Verwijder de geselecteerde gebruiker uit het aangevraagde Enterprise-account.<br></td>
   <td>Ja</td>
  </tr>
  <tr>
   <td>Verwijder alle gebruikers van alle proefaccounts waarvan de e-mail en de Adobe-ID overeenkomt met de e-mail van geselecteerde gebruikers.</td>
   <td>Ja</td>
  </tr>
  <tr>
   <td>Verwijder alle gebruikers van alle proefaccounts waarvan de e-mail en de Adobe-ID overeenkomt met de e-mail van geselecteerde gebruikers en hij/zij het proefaccount heeft aangemaakt.</td>
   <td>Nee</td>
  </tr>
  <tr>
   <td>Verwijder de e-mail van de gebruiker uit alle andere velden van het aanvragende Enterprise-account en alle proefaccounts.</td>
   <td>Ja</td>
  </tr>
  <tr>
   <td>Stel de initiatiefnemer op de hoogte van de verwijderingsbevestiging.</td>
   <td>Ja</td>
  </tr>
  <tr>
   <td><strong>Leegmaken met Learning Manager UI - Non-Enterprise</strong></td>
   <td> </td>
  </tr>
  <tr>
   <td>Verwijder de geselecteerde gebruiker uit het aangevraagde proefaccount.</td>
   <td>Ja</td>
  </tr>
  <tr>
   <td>Verwijder alle gebruikers van alle proefaccounts waarvan de e-mail en de Adobe-ID overeenkomt met de e-mail van geselecteerde gebruikers.</td>
   <td>Ja</td>
  </tr>
  <tr>
   <td>Verwijder alle gebruikers van alle proefaccounts waarvan de e-mail en de Adobe-ID overeenkomt met de e-mail van geselecteerde gebruikers en hij/zij het proefaccount heeft aangemaakt.</td>
   <td>Nee</td>
  </tr>
  <tr>
   <td>Verwijder de e-mail van de gebruiker uit alle andere velden van de Alle proefaccounts.</td>
   <td>Ja</td>
  </tr>
  <tr>
   <td>Stel de initiatiefnemer op de hoogte van de verwijderingsbevestiging.</td>
   <td>Ja</td>
  </tr>
  <tr>
   <td><strong>Andere gebruikers leegmaken - Enterprise (personen die geen interne of externe gebruikers van de Learning Manager zijn)</strong></td>
   <td> </td>
  </tr>
  <tr>
   <td>Verwijder de geselecteerde gebruiker uit alle andere velden van het aanvragende Enterprise-account en alle proefaccounts.</td>
   <td>Ja</td>
  </tr>
  <tr>
   <td>Gebruiker verwijderen van accounts.</td>
   <td>Nee</td>
  </tr>
  <tr>
   <td>Stel de initiatiefnemer op de hoogte van de verwijderingsbevestiging. </td>
   <td>Ja</td>
  </tr>
  <tr>
   <td><strong>Leegmaken</strong> <strong>andere gebruikers - Non-Enterprise (personen die geen interne of externe gebruikers van de Learning Manager zijn)</strong></td>
   <td> </td>
  </tr>
  <tr>
   <td>Verwijder de geselecteerde gebruiker uit alle andere velden van alle proefaccounts.</td>
   <td>Ja</td>
  </tr>
  <tr>
   <td>Gebruiker verwijderen van accounts.</td>
   <td>Nee</td>
  </tr>
  <tr>
   <td>Stel de initiatiefnemer op de hoogte van de verwijderingsbevestiging.</td>
   <td>Ja</td>
  </tr>
  <tr>
   <td><strong>Leegmaken met behulp van Adobe IMS-Enterprise</strong></td>
   <td> </td>
  </tr>
  <tr>
   <td>Informeer de Enterprise-beheerder over het verzoek.</td>
   <td>Ja</td>
  </tr>
  <tr>
   <td>Controleer de e-mailvelden voor het verzenden van meldingen.</td>
   <td>Nee</td>
  </tr>
  <tr>
   <td><strong>Leegmaken met behulp van Adobe IMS- Non-enterprise</strong></td>
   <td> </td>
  </tr>
  <tr>
   <td>Verwijder alle gebruikers die het bijgeleverde Adobe-ID/e-mail hebben van alle proefaccounts.</td>
   <td>Ja</td>
  </tr>
  <tr>
   <td>Verwijder alle gebruikers van een proefaccount als het/de verstrekte e-mail of Adobe-ID van de persoon is die het account heeft aangemaakt.</td>
   <td>Ja</td>
  </tr>
  <tr>
   <td>Verwijder het geselecteerde e-mail-ID uit alle andere velden van alle proefaccounts.</td>
   <td>Ja</td>
  </tr>
 </tbody>
</table>

+++

Learning Manager voldoet nu aan de AVG. Zie voor meer informatie over AVG-naleving  [Compatibiliteit van Learning Manager met AVG](../../kb/prime-gdpr.md).

## Veelgestelde vragen {#frequentlyaskedquestions}

+++Hoeveel dagen duurt het om een zuiveringsverzoek te voltooien?

De voltooiing van een aanvraag voor het leegmaken van gebruikers duurt maximaal 30 dagen.
+++

+++Kan je bulksgewijs leegmaken in Learning Manager?

Ja, u kunt leegmaken in bulk. Maar u kunt alleen 50 gebruikers leegmaken in bulk.
+++
