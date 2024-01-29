---
jcr-language: en_us
title: Veelgestelde vragen voor beheerders
description: Veelgestelde vragen voor Adobe Leermanager-beheerders
contentowner: manochan
source-git-commit: 0052ccb2f5a8f9617bca2c7bad91c0cd18338b66
workflow-type: tm+mt
source-wordcount: '2398'
ht-degree: 0%

---



# Veelgestelde vragen voor beheerders

<table>
 <tbody>
  <tr>
   <td><img src="assets/administrator2.png"></td>
   <td>
    <p>Lees verder om te weten te komen welke veelgestelde vragen de leermanager heeft over de beheerdersrol. </p></td>
  </tr>
 </tbody>
</table>

+++Kan ik gebruikers in bulk toevoegen? Hoe?

Ja, u kunt gebruikers in bulk toevoegen met behulp van de CSV-uploadfunctie. Klikken  [hier](/help/migrated/administrators/add-users-in-bulk.md) voor meer informatie.

+++

+++I e-mail-ID met een fout-type tijdens het maken van een aanmelding voor mijn studenten, hoe kan ik deze corrigeren?

Als u gebruikersaanmelding wilt corrigeren, moet u CSV importeren in Leerbeheer. Onder aan deze pagina vindt u een voorbeeld van een CSV-bestand ter referentie. Aangezien e-mail wordt beschouwd als een unieke ID voor een persoon, kan deze niet worden bewerkt. Voer de volgende stappen uit:

1. Voeg dezelfde gebruiker met de juiste e-mail-ID toe in CSV en zorg ervoor dat hij manager van andere gebruikers blijft door zijn e-mail-ID toe te voegen aan de kolom &quot;E-mail van de manager van de werknemer&quot; in het voorbeeld CSV.
1. Andere gebruikers in uw account toevoegen aan de CSV, inclusief uzelf
1. Importeer dit bestand in de Admin-app van Learning Manager->Gebruikers->Toevoegen->CSV importeren
1. Wijs alle velden, zoals gevraagd in het dialoogvenster, toe aan de corresponderende CSV-kolommen.
1. Klik op Opslaan.

Gebruikers moeten worden toegevoegd aan de pagina Studenten.

[Voorbeeld van Learning Manager CSV.csv](https://helpx.adobe.com/content/dam/help/en/captivate_prime/learning-manager-sample-csv.zip)

+++

+++Hoe stel ik waarschuwingen in?

In de release Adobe Learning Manager 1.0 kunt u meldingen maken. Verwijzen  [meldingsvraag](/help/migrated/administrators/feature-summary/user-notifications.md) voor meer informatie.

+++

+++Hoe voeg ik certificaten toe voor de cursussen?

Adobe Learning Manager biedt geen certificaten voor de cursussen. De beheerder kan echter voor elke cursus badges maken door in het linkerdeelvenster op het tabblad Badges te klikken. Wanneer de beheerder studenten voor een cursus inschrijft, kan hij er ook een badge aan koppelen.

+++

+++Hoe kan ik handtekeningen voor de certificaten importeren?

In Adobe Learning Manager is er geen functie om handtekeningen voor de certificering of badge te importeren.

+++

+++Kan ik een kalender voor de cursussen instellen? Hoe?

In de Adobe Learning Manager 1.0-versie hebben we geen voorzieningen om een agenda voor de cursussen in te stellen.

+++

+++Hoe schrijf ik de studenten op de wachtlijst rechtstreeks in?

Studenten worden op de wachtlijst geplaatst voor een klassikale cursus wanneer de plaatsen beperkt zijn, op basis van de volgorde van hun inschrijving. Beheerders kunnen studenten op de wachtlijst selecteren en plaatsen toewijzen die de plaatslimiet voor een klaslokaalcursus overschrijden. Studenten worden voor de cursus ingeschreven zodra de beheerder een licentie heeft toegewezen.

1. Klik op Cursussen in het linkerdeelvenster nadat u zich als beheerder hebt aangemeld.
1. Klik in de lijst met beschikbare cursussen op de cursusnaam van een klaslokaalcursus. Er verschijnt een nieuwe pagina met gedetailleerde informatie over de cursus.
1. Klik op Wachtlijst in het linkerdeelvenster van de pagina met cursusdetails. Op de pagina verschijnt een wachtlijst met studenten.
1. Selecteer de studenten en klik op Plaatsen toewijzen om de studenten rechtstreeks voor de cursussen in te schrijven, zodat de plaatslimiet niet wordt overschreden.

Raadpleeg voor meer informatie  [wachtlijst en aanwezigheid](/help/migrated/administrators/feature-summary/waitlist-attendance-management.md) gebruiken.

+++

+++Hoe registreer ik aanwezigheid voor studenten van de klaslokaalmodule?

Ja, u kunt aanwezigheid als volgt registreren:

1. Klik op Cursussen in het linkerdeelvenster nadat u zich als beheerder hebt aangemeld.
1. Klik in de lijst met beschikbare cursussen op de cursusnaam van een klaslokaalmodule/cursus van uw keuze. Er verschijnt een nieuwe pagina met gedetailleerde informatie over de cursus.
1. Selecteer de studenten en klik op Opslaan om de voltooiing van de cursus vast te leggen.

Als een cursus uit meerdere modules bestaat en de student er slechts één heeft voltooid, kunt u één module selecteren en op Opslaan klikken om de voltooiing voor de student te markeren. Als de student alle modules van een cursus heeft voltooid, kunt u op Alles selecteren klikken en op Opslaan klikken.

Raadpleeg voor meer informatie  [wachtlijst en aanwezigheid](/help/migrated/administrators/feature-summary/waitlist-attendance-management.md) gebruiken.

+++

+++Hoe voeg ik de L3-feedbackoptie toe?

U kunt L3-feedback toevoegen terwijl u studenten voor de cursussen inschrijft. Voer de onderstaande stappen uit om L3-feedbackvraag toe te voegen:

1. Klik op Cursussen in het linkerdeelvenster nadat u zich als beheerder hebt aangemeld. Rechts op de pagina ziet u een lijst met alle cursussen.
1. Klik op de cursustegel waarvoor u L3-feedback wilt toevoegen
1. Klik op standaard instantie in het linkerdeelvenster.
1. Klik op de cirkel op de wisselknop naast L3 - Feedback gedragswijziging om deze te selecteren.
1. Voeg de L3-feedbackvraag toe in het tekstgebied onder L3-vraag.

+++

+++Hoe zoek ik naar de aanwijzing van de manager voor een manager-aangewezen cursus?

Als beheerder kunt u de aanwijzing van de manager voor de cursussen opvragen door de onderstaande stappen te volgen:

1. Klik op Cursussen in het linkerdeelvenster
1. Houd de muis boven een door manager aangewezen cursus en klik op **[!UICONTROL Aanwijzing van zoekmanager]**.

1. Klik in de lijst met instanties op **[!UICONTROL Aangewezen managers]** link gevolgd door **[!UICONTROL Managers toevoegen]** koppeling.

1. Voeg de naam van de manager en het aantal toegewezen plaatsen toe en klik op het vinkje om de wijzigingen op te slaan.

Tijdens het maken van de cursussen kiest de auteur het type cursus als Manager-aangewezen.

+++

+++Hoe schrijf ik een student in voor een bepaalde cursus?

Volg onderstaande stappen om studenten voor cursussen in te schrijven:

1. Klik op Cursussen in het linkerdeelvenster nadat u zich als beheerder hebt aangemeld. Rechts op de pagina ziet u een lijst met alle cursussen.
1. Kies de cursus waaraan u studenten wilt toevoegen en houd de muis erop.
1. Klik op Studenten inschrijven en voeg de naam van de studenten toe. **Opmerking:** U kunt een of meer studenten tegelijk toevoegen.

+++

+++Hoe kan ik studenten aan een bepaalde vaardigheid toewijzen?

Volg onderstaande stappen om studenten aan competenties toe te wijzen:

1. Klikken **[!UICONTROL Vaardigheden]** in het linkerdeelvenster nadat u zich als beheerder hebt aangemeld.
1. Selecteer een of meer vaardigheden door op selectievakjes naast elke competentie te klikken en klik op **[!UICONTROL Handelingen]** rechtsboven op de pagina.
1. Klik op Toewijzen aan gebruikers.
1. Typ de naam van de gebruiker, kies een optie in de vervolgkeuzelijst en klik op **[!UICONTROL Opslaan]**.

   >[!NOTE]
   >
   >U kunt meerdere studenten voor vaardigheden inschrijven door op Meer gebruikers toevoegen te klikken en de vierde stap te herhalen.

+++

+++How to create learning program session?

Volg de onderstaande stappen om een leerprogramma te maken:

1. Klik op Leerprogramma in het linkerdeelvenster. De pagina Leerprogramma&#39;s verschijnt met een lijst van bestaande leerprogramma&#39;s.
1. Klik op Toevoegen rechtsboven op de pagina.\
   Voer de programmanaam, het overzicht en de beschrijving in en klik op Opslaan.
1. Klik op Cursussen in het linkerdeelvenster.
1. Voeg een of meer cursussen toe door op + op elke cursustegel te klikken.

   >[!NOTE]
   >
   >U moet het leerprogramma publiceren voordat u studenten of een instantie inschrijft.

1. Klik op Instanties in het linkerdeelvenster en klik op **[!UICONTROL Nieuwe instanties toevoegen]** rechts op de pagina om details van de instantie op te nemen.

Raadpleeg voor meer informatie over leerprogramma&#39;s  [Leerprogramma&#39;s](/help/migrated/administrators/feature-summary/learning-programs.md)

+++

+++Hoe kan ik rapporten voor alle rollen wijzigen of aanpassen?

Klik op de vervolgkeuzepijl in de rechterbovenhoek van elk rapport om rapporten te bewerken/wijzigen. Klik op Opslaan na het voltooien van de wijzigingen en bekijk het gewijzigde rapport.

+++

+++Hoe wijzig ik cursussen, leerprogramma&#39;s en het bedrijfsprofiel?

U kunt cursussen of leerprogramma&#39;s ook bewerken nadat u ze hebt gepubliceerd. Raadpleeg voor meer informatie  [Cursussen](/help/migrated/administrators/feature-summary/courses.md) en  [leerprogramma&#39;s](/help/migrated/administrators/feature-summary/learning-programs.md) Help content.

Als u het bedrijfsprofiel wilt wijzigen, klikt u op **[!UICONTROL Instellingen]** in het linkerdeelvenster en klik op **[!UICONTROL Wijzigen]** rechtsboven op de pagina.

+++

+++Hoe zoek ik naar de cursussen?

Klik op Cursussen in het linkerdeelvenster nadat u zich als beheerder hebt aangemeld. Er verschijnt een lijst met alle beschikbare cursussen.

U kunt op twee manieren naar cursussen zoeken:

1. Klik op het zoekpictogram in de rechterbovenhoek. Er wordt een zoekveld weergegeven. Typ de naam van de cursus of eventuele trefwoorden die bij uw cursussen horen om uw cursussen te vinden.
1. Door de lijst van cursussen met de filters te filteren.

U kunt de cursussen filteren op status zoals Alle, Gepubliceerd en Gearchiveerd door op elk van deze opties te klikken. U kunt ook zoeken op basis van competenties door op Competenties te klikken en een van deze te kiezen.

Afhankelijk van uw keuze kunt u de gefilterde lijst met cursussen bekijken en de vereiste cursussen selecteren.

+++

+++Kan ik de thema&#39;s voor de toepassing wijzigen? Hoe?

Ja, u kunt de thema&#39;s en branding van de toepassing Learning Manager aanpassen aan de vereisten van uw organisatie. Er zijn vijf representatieve afbeeldingen beschikbaar om een voorvertoning te bekijken van de wijzigingen in uw kleurthema voordat u deze toepast op uw toepassing. Blader door deze afbeeldingen door op de symbolen &lt; en > links en rechts van de afbeeldingen te klikken om een voorvertoning weer te geven.

Klikken **[!UICONTROL Branding]** in het linkerdeelvenster om de naam van uw organisatie bij te werken, wijzigt u het subdomein, de logstijlen en de thema&#39;s. Klikken **[!UICONTROL Bewerken]** naast elk van deze onderwerpen om de inhoud te wijzigen.

Raadpleeg  [Help voor kleurthema&#39;s en branding](/help/migrated/administrators/feature-summary/themes.md) voor meer informatie.

+++

+++Hoe stel ik badges in voor de cursussen?

1. Klik op Badges in het linkerdeelvenster nadat u zich als beheerder hebt aangemeld.
1. Klik op Toevoegen rechtsboven op de pagina die wordt weergegeven.
1. Naam badge toevoegen.
1. Upload de badge door op Badge uploaden te klikken en op Opslaan te klikken.

+++

+++Hoe stel ik gamificationpunten in voor de cursussen?

U kunt gamificationpunten voor studenten instellen door de onderstaande stappen te volgen:

1. Klik op Gamification nadat u zich als beheerder hebt aangemeld. Er verschijnt een pagina met een lijst van bronzen, zilveren, gouden en platina niveaus en de vereiste punten voor elk niveau. Er is een lijst met taken en bijbehorende punten beschikbaar.
1. Klik op het pictogram Bewerken naast elke taak om de punten in te stellen/te wijzigen.

Verwijzen  [Gamification, functie](/help/migrated/administrators/feature-summary/gamification.md) voor meer informatie.

+++

+++Hoe maak ik rapporten voor managers en studenten?

U kunt rapporten maken door de onderstaande stappen te volgen:

1. Klik op Rapporten in het linkerdeelvenster. De pagina Rapportoverzicht wordt weergegeven.
1. Klik op de pagina Rapporten op **[!UICONTROL Toevoegen]** rechtsboven.

   **[!UICONTROL Rapport toevoegen]** wordt weergegeven.

1. Vul alle verplichte velden in en klik op Opslaan.

Alleen beheerders en managers kunnen rapporten maken of bekijken. Raadpleeg [rapportfunctie](/help/migrated/administrators/feature-summary/reports.md) voor meer informatie.

+++

+++Hoe wijzig ik in de rollen student, manager en auteur?

U kunt uw accountaanmelding overzetten naar andere rollen zoals student, manager en auteur zonder u af te melden bij uw account.

1. Klik op de vervolgkeuzepijl naast uw profielfoto rechtsboven op de pagina.\
   Er verschijnt een pop-upmenu.
1. Selecteer elke beschikbare rol om toegang te krijgen tot de respectieve rolaccounts.

+++

+++Hoe neem ik meldingen voor de gebruikers op?

Managers, auteurs en studenten kunnen meldingen zien op basis van de cursusactiviteiten. De beheerder kan meldingen voor alle gebruikers in- en uitschakelen door de onderstaande stappen te volgen:

1. Klik in het linkerdeelvenster op E-mailsjablonen en kies de tabbladen Algemeen, Gebruikersinschrijving, Voltooiingen en Feedback.
1. Klik in de onderstaande lijst met gebeurtenissen op de schakelknoppen Nee/Ja naast **elke **gebeurtenis en kies Ja om melding in te schakelen. Klik op Nee om het verzenden van meldingen voor een bepaalde gebeurtenis uit te schakelen.

+++

+++Hoe sta ik externe inschrijving voor de cursussen toe?

Adobe Learning Manager biedt u de mogelijkheid om externe afdelingsleden of externe medewerkers van uw organisatie in te schrijven voor de toepassing.

1. Klikken **[!UICONTROL Gebruikers]** in het linkerdeelvenster.
1. Klikken **[!UICONTROL Extern]** in het linkerdeelvenster.
1. Klikken **[!UICONTROL Toevoegen]** rechtsboven op de pagina.

   Het dialoogvenster Gebruiker toevoegen verschijnt.

1. Voeg de profielnaam, het e-mailadres van de manager, de toegewezen plaatsen en de vervaldatum toe. U kunt ook een afbeelding aan het externe profiel toevoegen.
1. Klikken **[!UICONTROL Opslaan]**.

De beheerder kan de registratie-URL kopiëren en naar de externe inschrijvingsgroep verzenden. De externe gebruikers kunnen zich registreren, zich aanmelden bij de toepassing Leermanager en hun cursussen openen.

+++

+++Hoe voeg ik een vragenlijst toe voor de L1-feedback?

Maak een feedbackvragenlijst die studenten na het afronden van de cursussen kunnen gebruiken. Standaard zijn er drie voorbeeldvragen beschikbaar. Volg de onderstaande stappen om een vragenlijst te maken.

1. Klik op Feedback in het linkerdeelvenster. Er verschijnt een venster met feedbackvragenlijsten.
1. Klikken **[!UICONTROL Bewerken]** om de vragenlijst toe te voegen of te wijzigen.

U kunt een set vragenlijsten toevoegen en ervoor kiezen deze niet weer te geven als u ze niet nodig hebt. Klik op het selectievakje om een bepaalde vraag in of uit te schakelen.

+++

+++Hoe stel ik de vaardigheden en niveaus in?

1. Klik op Competenties in het linkerdeelvenster van het venster Beheerder.
1. Klik op Toevoegen om nieuwe competenties toe te voegen.
1. Voeg overeenkomstig de naam van de competentie, de beschrijving en de bijbehorende punten toe aan elk niveau.

   Standaard is voor elke competentie één niveau met 0 punten beschikbaar.

1. Klikken [!UICONTROL **Niveau toevoegen**] om een nieuw niveau aan elke competentie toe te voegen en klik op Opslaan. U kunt maximaal vijf niveaus toevoegen.

Als de competentie eenmaal is opgeslagen, kunt u geen niveaus meer uit de competentie verwijderen. De beheerder kan ook studenten aan een bepaalde competentie en een bepaald niveau toewijzen.

+++

+++Hoe stel ik een factureringssysteem in voor de cursussen van mijn organisatie?

1. Klikken [!UICONTROL **Facturering**] in het linkerdeelvenster.

   Factureringsgegevens worden op de pagina weergegeven.

1. Klik op de knop [!UICONTROL **Abonneren**] tabblad.
1. Typ het aantal pakketten dat u wilt bestellen in het veld voor studentpakketten en klik op Bestelling plaatsen rechtsboven op de pagina.

   Kies het aantal pakketten op basis van het aantal studenten in uw organisatie en plaats uw bestelling. Voor een proces dat wordt aangestuurd door een inkooporder, kunt u ons schrijven op  [learningmanagersales@adobe.com](mailto:learningmanagersales@adobe.com).

1. Voer uw contactgegevens in, kies het type creditcard, geef uw creditcardgegevens op en klik op Bestelling voltooien.

Verwijzen [Factureringsbeheer](/help/migrated/administrators/feature-summary/billing-management.md) voor meer informatie.

+++

+++Kan ik het certificaatontwerp aanpassen? Hoe?

In Adobe Learning Manager kunt u studenten herkennen door badges uit te geven. Raadpleeg de functie Badges voor meer informatie.  Raadpleeg ook de functie Certificering.

+++

+++Hoe stel ik mijn bedrijfsprofiel in?

1. Nadat u zich als beheerder hebt aangemeld, klikt u op **[!UICONTROL Bedrijfsinformatie]** in het linkerdeelvenster.
1. Voeg Bedrijfsprofiel, subdomein en logo toe door op elk van deze opties op de pagina te klikken.

+++

+++Hoe voeg ik cursussen toe?

Als u cursussen wilt toevoegen, moet u uw rol als auteur veranderen. U kunt de lijst met beschikbare cursussen alleen weergeven op basis van hun status als **[!UICONTROL Voltooid]**, **[!UICONTROL Gepubliceerd]**, en **[!UICONTROL Gearchiveerd]**.

Als u cursussen wilt weergeven, klikt u op **[!UICONTROL Cursussen]** in het linkerdeelvenster. Verwijzen  [Cursussen maken](/help/migrated/administrators/feature-summary/courses.md)voor meer informatie

+++

+++Hoe voeg ik verschillende rollen toe aan de toepassing?

Volg de onderstaande stappen om nieuwe gebruikers toe te voegen:

1. Klik op Gebruikers in het linkerdeelvenster nadat u zich als beheerder hebt aangemeld. U kunt ook gebruikers toevoegen door op Aan de slag in het linkerdeelvenster van het venster te klikken en op Gebruikers toevoegen te klikken.
1. Klik op Toevoegen rechtsboven op de pagina om nieuwe gebruikers toe te voegen.

Standaard krijgen alle nieuwe gebruikers de rol van student. U kunt beheerders- of auteursrollen aan de studenten toewijzen door op **[!UICONTROL Handelingen]** in de rechterbovenhoek van de pagina en kies **[!UICONTROL Rol toewijzen]** > **[!UICONTROL Auteur maken]** of **[!UICONTROL Beheerder maken]**.

Verwijzen  [Nieuwe gebruikers toevoegen](/help/migrated/administrators/feature-summary/add-users-user-groups.md) voor gedetailleerde informatie over het toevoegen van studenten, auteurs en beheerders.

+++

+++Hoe kan ik een achtergrondafbeelding voor een student wijzigen?

Neem contact op met het ondersteuningsteam van Leermanager.

+++

+++Waar vind ik mijn LMS-account-id?

U kunt de account-id ophalen vanuit de browser waarin Leerbeheer is geopend.

*/app/admin?i_qp_user_id=12761637&amp;**accountId=6849***

+++
