---
description: Meer informatie over het leegmaken van gebruikersgegevens in Learning Manager.
jcr-language: en_us
title: Gebruikers leegmaken
contentowner: dvenkate
source-git-commit: 53c1a5283295b56424d697bc26c5db31c2edca0f
workflow-type: tm+mt
source-wordcount: '849'
ht-degree: 0%

---



# Gebruikers leegmaken

Meer informatie over het leegmaken van gebruikersgegevens in Learning Manager.

## Overzicht {#overview}

Gebruik de functie Gebruikers leegmaken om persoonlijke, identificeerbare gegevens en leerrecords van de gebruiker te verwijderen uit de Leermanager. Gebruikers verwijderen en leegmaken zijn twee verschillende functies. Hoewel een verwijderde gebruiker kan worden hersteld, kunnen niet alle gebruikersgegevens en leerrecords die aan een leeggemaakte gebruiker zijn gekoppeld, worden hersteld.

De actie van de gebruiker leegmaken kan de volgende resultaten hebben:

* Als een gebruiker wordt leeggemaakt, werken de koppelingen in importlogboeken niet om het downloaden van oude CSV&#39;s te voorkomen en de gebruikersgegevens opnieuw in het systeem te plaatsen.
* Als een auteur wordt leeggemaakt, wordt zijn naam vervangen door de naam van de beheerder die die gebruiker leeggemaakt heeft.
* Als docenten worden leeggemaakt, worden ze uit de sessies verwijderd. De beheerder moet voor dergelijke sessies docenten vervangen/toevoegen.
* Als u een gebruiker in Leermanager leegmaakt, wordt de gebruiker niet verwijderd in externe toepassingen (systemen van derden of andere door u geschreven toepassingen). Neem contact op met externe eigenaars van toepassingen om de gebruikers uit dergelijke toepassingen te verwijderen.
* Als in de configuratie-instellingen van een connector naar een leeggemaakte gebruiker wordt verwezen, is de connector uitgeschakeld. De connector moet opnieuw worden geconfigureerd door de beheerder om te kunnen worden hervat.

Volg deze stappen om gebruikers leeg te maken:

1. Als beheerder selecteert u **[!UICONTROL Gebruikers]** in het linkerdeelvenster. De **[!UICONTROL Interne gebruikers]** wordt geopend.
1. Verwijder de gebruikers die u wilt leegmaken. Selecteer een of meer gebruikers met behulp van het selectievakje om te verwijderen. Open de **[!UICONTROL Handeling]** en selecteert u **[!UICONTROL Gebruiker verwijderen.]**
1. Selecteer in het linkerdeelvenster **[!UICONTROL Gebruikersopschoning]**. De **[!UICONTROL Gebruikersopschoning]** wordt weergegeven met de lijst met verwijderde gebruikers. Gebruik de keuzerondjes om de gebruiker te selecteren die u wilt leegmaken. U kunt slechts één gebruiker tegelijk leegmaken.

   ![](assets/purge-1.png)

   *Selecteer een gebruiker die u wilt leegmaken*

1. Open de **[!UICONTROL Handelingen]** en selecteert u **[!UICONTROL Gebruiker leegmaken]**.

   ![](assets/purge-2.png)

   *Selecteer de optie Gebruikers leegmaken*

1. Er verschijnt een dialoogvenster waarin u om bevestiging kunt vragen. Wanneer de gebruiker is leeggemaakt, worden alle gebruikersgegevens en leerrecords die aan de geselecteerde gebruiker zijn gekoppeld, permanent verwijderd. Nadat de handeling is leeggemaakt, kan deze niet meer ongedaan worden gemaakt. Klik ter bevestiging op **[!UICONTROL Leegmaken]**.

   ![](assets/purge-3.png)

   *Bevestigingsbericht na leegmaken van een gebruiker*

1. Zodra u bevestigt en op Leegmaken klikt, wordt het verzoek tot leegmaken geaccepteerd. U ontvangt een melding zodra de handeling is voltooid. Er is ook een aanvraag-id voor leegmaken opgegeven. U kunt deze id aan de CSM verstrekken om het verzoek te volgen.

## Gebruikers in bulk leegmaken

U kunt de eerste 50 gebruikers selecteren en de gebruikers in één opname leegmaken. Hiermee kunnen beheerders 50 gebruikers tegelijk selecteren en leegmaken. Dit helpt beheerders wanneer ze gebruikers in bulk willen leegmaken. Het is altijd raadzaam om de gebruikers te controleren die zijn geselecteerd voor leegmaken. Dit is belangrijk om ervoor te zorgen dat alleen de juiste set gebruikers wordt leeggemaakt.

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
   <td>Verwijder de geselecteerde gebruiker uit het aanvragende ondernemingsaccount.<br></td>
   <td>Ja</td>
  </tr>
  <tr>
   <td>Verwijder alle gebruikers uit alle proefaccounts waarvan de e-mail en de Adobe-id overeenkomen met de e-mail van geselecteerde gebruikers.</td>
   <td>Ja</td>
  </tr>
  <tr>
   <td>Verwijder alle gebruikers uit alle proefaccounts waarvan de e-mail en de Adobe-id overeenkomen met de e-mail van geselecteerde gebruikers en hij/zij de maker van het proefaccount is.</td>
   <td>Nee</td>
  </tr>
  <tr>
   <td>Verwijder de e-mail van de gebruiker uit alle andere velden van het aanvragende Enterprise-account en alle proefaccounts.</td>
   <td>Ja</td>
  </tr>
  <tr>
   <td>Stel de aanvrager op de hoogte van de verwijderingsbevestiging.</td>
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
   <td>Verwijder alle gebruikers uit alle proefaccounts waarvan de e-mail en de Adobe-id overeenkomen met de e-mail van geselecteerde gebruikers.</td>
   <td>Ja</td>
  </tr>
  <tr>
   <td>Verwijder alle gebruikers uit alle proefaccounts waarvan de e-mail en de Adobe-id overeenkomen met de e-mail van geselecteerde gebruikers en hij/zij de maker van het proefaccount is.</td>
   <td>Nee</td>
  </tr>
  <tr>
   <td>Verwijder de e-mail van de gebruiker uit alle andere velden van de Alle proefaccounts.</td>
   <td>Ja</td>
  </tr>
  <tr>
   <td>Stel de aanvrager op de hoogte van de verwijderingsbevestiging.</td>
   <td>Ja</td>
  </tr>
  <tr>
   <td><strong>Andere gebruikers leegmaken - Enterprise (personen die geen interne of externe gebruikers van de Learning Manager zijn)</strong></td>
   <td> </td>
  </tr>
  <tr>
   <td>Verwijder de geselecteerde gebruiker uit alle andere velden van het aanvragende Enterprise-account en Alle proefaccounts.</td>
   <td>Ja</td>
  </tr>
  <tr>
   <td>Gebruiker verwijderen uit accounts.</td>
   <td>Nee</td>
  </tr>
  <tr>
   <td>Stel de aanvrager op de hoogte van de verwijderingsbevestiging. </td>
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
   <td>Gebruiker verwijderen uit accounts.</td>
   <td>Nee</td>
  </tr>
  <tr>
   <td>Stel de aanvrager op de hoogte van de verwijderingsbevestiging.</td>
   <td>Ja</td>
  </tr>
  <tr>
   <td><strong>Leegmaken met Adobe IMS - Enterprise</strong></td>
   <td> </td>
  </tr>
  <tr>
   <td>Stel de Enterprise-beheerder op de hoogte van de aanvraag.</td>
   <td>Ja</td>
  </tr>
  <tr>
   <td>Controleer de e-mailvelden voor het verzenden van meldingen.</td>
   <td>Nee</td>
  </tr>
  <tr>
   <td><strong>Leegmaken met Adobe IMS - Non-Enterprise</strong></td>
   <td> </td>
  </tr>
  <tr>
   <td>Verwijder alle gebruikers met de meegeleverde Adobe-id/e-mail uit Alle proefaccounts.</td>
   <td>Ja</td>
  </tr>
  <tr>
   <td>Verwijder alle gebruikers van een proefaccount als de opgegeven e-mail/Adobe-id de maker van het account was.</td>
   <td>Ja</td>
  </tr>
  <tr>
   <td>Verwijder de geselecteerde e-mail-ID uit alle andere velden van alle proefaccounts.</td>
   <td>Ja</td>
  </tr>
 </tbody>
</table>

+++

Learning Manager voldoet nu aan de AVG. Zie voor meer informatie over AVG-naleving  [Compatibiliteit van Learning Manager met AVG](../../kb/prime-gdpr.md).

## Veelgestelde vragen {#frequentlyaskedquestions}

+++Hoeveel dagen duurt het om een zuiveringsverzoek te voltooien?

Het voltooien van een verzoek om gebruikers leeg te maken duurt maximaal 30 dagen.
+++

+++Kan je bulksgewijs leegmaken in Learning Manager?

Ja, je kunt bulksgewijs leegmaken. U kunt echter slechts 50 gebruikers bulksgewijs leegmaken.
+++
