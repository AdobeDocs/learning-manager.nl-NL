---
jcr-language: en_us
title: Veelgestelde vragen voor beheerders
description: Veelgestelde vragen voor Adobe Learning Manager-beheerders
contentowner: manochan
exl-id: 8b113a4e-73f4-4cd5-982a-cefdf5388e91
source-git-commit: 0dade561e53e46f879e22b53835b42d20b089b31
workflow-type: tm+mt
source-wordcount: '2517'
ht-degree: 52%

---

# Veelgestelde vragen voor beheerders

<table>
 <tbody>
  <tr>
   <td><img src="assets/administrator2.png"></td>
   <td>
    <p>Lees verder voor veelgestelde vragen over de beheerdersrol in Learning Manager. </p></td>
  </tr>
 </tbody>
</table>

+++Kan ik gebruikers in bulk toevoegen? Hoe?

Ja, u kunt gebruikers in bulk toevoegen door de functie CSV-upload te gebruiken. Verwijs naar dit [ artikel ](/help/migrated/administrators/feature-summary/add-users-user-groups.md#bulk-upload-internal-users) voor meer informatie.

+++

+++I e-mail-ID met een fout-type tijdens het maken van een aanmelding voor mijn studenten, hoe kan ik deze corrigeren?

U moet CSV in Learning Manager importeren om een gebruikersaanmelding te corrigeren. Onderaan deze pagina vindt u een voorbeeld van een CSV-bestand ter referentie. Aangezien e-mail wordt beschouwd als een unieke ID voor een persoon, kan deze niet worden bewerkt. Volg deze stappen:

1. Voeg dezelfde gebruiker met de juiste e-mail-ID toe in CSV en zorg ervoor dat hij manager van andere gebruikers blijft door zijn e-mail-ID toe te voegen aan de kolom &quot;E-mail van de manager van de werknemer&quot; in het voorbeeld CSV.
1. Voeg andere gebruikers in uw account aan de CSV toe, inclusief uzelf
1. Importeer dit bestand in de Learning Manager beheerder-app->Gebruikers->Toevoegen->CSV importeren
1. Wijs alle velden, zoals gevraagd in het dialoogvenster, aan de corresponderende CSV-kolommen toe.
1. Klik op Opslaan.

Gebruikers moeten worden toegevoegd aan de pagina Studenten.

[ het Leren Manager Voorbeeld CSV.csv ](https://helpx.adobe.com/content/dam/help/en/captivate_prime/learning-manager-sample-csv.zip)

+++

+++Hoe stel ik waarschuwingen in?

In de release Adobe Learning Manager 1.0 kunt u meldingen maken. Verwijs [ meldingsvraag ](/help/migrated/administrators/feature-summary/user-notifications.md) voor meer informatie.

+++

+++Hoe voeg ik certificaten toe voor de cursussen?

Adobe Learning Manager biedt geen certificaten voor de cursussen. De beheerder kan echter voor elke cursus badges maken door in het linkerdeelvenster op het tabblad Badges te klikken. Wanneer de beheerder studenten voor een cursus inschrijft, kan hij hier ook een badge aan koppelen.

+++

+++Hoe kan ik handtekeningen voor de certificaten importeren?

In Adobe Learning Manager is er geen functie om handtekeningen voor de certificering of badge te importeren.

+++

+++Kan ik een kalender voor de cursussen instellen? Hoe?

In de Adobe Learning Manager 1.0-versie hebben we geen voorzieningen om een kalender voor de cursussen in te stellen.

+++

+++Hoe schrijf ik de studenten op de wachtlijst rechtstreeks in?

Wanneer de plaatsen beperkt zijn, worden studenten op de wachtlijst gezet voor een klassikale cursus op volgorde van inschrijving. Beheerders kunnen studenten op de wachtlijst selecteren en plaatsen toewijzen, waarmee ze de plaatslimiet voor een klaslokaalcursus kunnen overschrijden. Studenten worden voor de cursus ingeschreven zodra de beheerder een plaats toewijst.

1. Klik op Cursussen in het linkerdeelvenster nadat u zich als beheerder hebt aangemeld.
1. Klik in de lijst met beschikbare cursussen op de cursusnaam van een klaslokaalcursus. Er verschijnt een nieuwe pagina met gedetailleerde informatie over de cursus.
1. Klik op Wachtlijst in het linkerdeelvenster van de pagina met cursusdetails. Op de pagina verschijnt een wachtlijst van studenten.
1. Selecteer de studenten en klik op Plaatsen toewijzen om hen direct in te schrijven voor de cursussen en daarbij de plaatslimiet te overschrijden.

Voor meer informatie, verwijs [ wachtlijst en aanwezigheid ](/help/migrated/administrators/feature-summary/waitlist-attendance-management.md) eigenschap.

+++

+++Hoe registreer ik aanwezigheid voor studenten van de klaslokaalmodule?

U kunt aanwezigheid als volgt registreren:

1. Klik op Cursussen in het linkerdeelvenster nadat u zich als beheerder hebt aangemeld.
1. Klik in de lijst met beschikbare cursussen op de cursusnaam van een klaslokaalmodule/cursus. Er verschijnt een nieuwe pagina met gedetailleerde informatie over de cursus.
1. Selecteer de studenten en klik op Opslaan om voltooiing van de cursus te registreren.

Als een cursus uit meerdere modules bestaat en de student er slechts één heeft voltooid, kunt u één module selecteren en op Opslaan klikken om dit voor de student te markeren. Als de student alle modules van een cursus heeft voltooid, kunt u op Alles selecteren klikken en vervolgens op Opslaan.

Voor meer informatie, verwijs [ wachtlijst en aanwezigheid ](/help/migrated/administrators/feature-summary/waitlist-attendance-management.md) eigenschap.

+++

+++Hoe voeg ik de L3-feedbackoptie toe?

U kunt L3-feedback toevoegen terwijl u studenten inschrijft voor de cursussen. Volg onderstaande stappen om L3-feedback toe te voegen:

1. Klik op Cursussen in het linkerdeelvenster nadat u zich als Administrator hebt aangemeld. Rechts op de pagina verschijnen lijsten van alle cursussen.
1. Klik op de cursustegel waarvoor u L3-feedback wilt toevoegen
1. Klik op standaardinstantie in het linkerdeelvenster.
1. Klik op de cirkel op de wisselknop naast L3 - Feedback gedragswijziging om deze te selecteren.
1. Voeg de L3-feedbackvraag in het tekstgebied onder L3-vraag toe.

+++

+++Hoe zoek ik naar de aanwijzing van de manager voor een manager-aangewezen cursus?

Als beheerder kunt u de aanwijzing van de manager voor de cursussen opvragen door de onderstaande stappen te volgen:

1. Klik op Cursussen in het linkerdeelvenster
1. Beweeg de muis op om het even welke manager aangewezen cursus en klik **[!UICONTROL de Aanwijzing van de Manager van het Onderzoek]**.

1. In de lijst van instanties, klik **[!UICONTROL Managers nomineerde]** verbinding die door **[!UICONTROL wordt gevolgd voeg Managers]** verbinding toe.

1. Voeg de naam van de manager en het aantal toegewezen plaatsen toe en klik op het vinkje om de wijzigingen op te slaan.

Bij het maken van de cursussen kiest de auteur het type cursus als Manager-aangewezen.

+++

+++Hoe schrijf ik een student in voor een bepaalde cursus?

Volg onderstaande stappen om studenten voor cursussen in te schrijven:

1. Klik op Cursussen in het linkerdeelvenster nadat u zich als Administrator hebt aangemeld. Rechts op de pagina verschijnen lijsten van alle cursussen.
1. Kies de cursus waaraan u studenten wilt toevoegen en zet uw muis hierop.
1. Klik op Studenten inschrijven en voeg de naam van de studenten toe. **Nota:** u kunt één of vele studenten tegelijkertijd toevoegen.

+++

+++Hoe kan ik studenten aan een bepaalde vaardigheid toewijzen?

Volg de onderstaande stappen om studenten aan competenties toe te wijzen:

1. Klik **[!UICONTROL Vaardigheden]** bij de linkerruit nadat u login als Beheerder.
1. Selecteer één of veelvoudige vaardigheden door controledozen tegen elke competentie te klikken en **[!UICONTROL drop-down Acties]** bij de hoger-juiste hoek van de pagina te klikken.
1. Klik op Toewijzen aan gebruikers.
1. Begin de naam van de gebruiker te typen, verkies van de drop-down lijst en klik **[!UICONTROL sparen]**.

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

1. Klik Instanties op de linkerruit en klik **[!UICONTROL voeg nieuwe instanties]** op de juiste hoek van de pagina toe om details van de instantie te omvatten.

Voor meer informatie over het leren van programma&#39;s, verwijs [ het Leren programmaeigenschap.](/help/migrated/administrators/feature-summary/learning-programs.md)

+++

+++Hoe kan ik rapporten voor alle rollen wijzigen of aanpassen?

Klik op het omlaagwijzende pijltje in de rechterbovenhoek van elk rapport om dit te bewerken/wijzigen. Klik op Opslaan nadat u de wijzigingen hebt aangebracht en bekijk het gewijzigde rapport.

+++

+++Hoe wijzig ik cursussen, leerprogramma&#39;s en het bedrijfsprofiel?

U kunt cursussen of leerprogramma&#39;s ook na publicatie bewerken. Voor meer informatie, verwijs naar [ Cursussen ](/help/migrated/administrators/feature-summary/courses.md) en [ het leren van programma&#39;s ](/help/migrated/administrators/feature-summary/learning-programs.md) inhoud van de Hulp.

Om bedrijfprofiel te wijzigen, klik **[!UICONTROL Montages]** bij de linkerruit en klik **[!UICONTROL Verandering]** op de hoger-juiste hoek van de pagina.

+++

+++Hoe zoek ik naar de cursussen?

Klik op Cursussen in het linkerdeelvenster nadat u zich als beheerder hebt aangemeld. Er verschijnt een lijst van alle beschikbare cursussen.

U kunt op twee manieren naar cursussen zoeken:

1. Klik op het zoekpictogram in de rechterbovenhoek. Er verschijnt een zoekveld. Typ de naam van de cursus of eventuele trefwoorden die bij uw cursussen horen om uw cursussen te vinden.
1. Door de lijst van cursussen met de filters te filteren.

U kunt de cursussen filteren op status zoals Alle, Gepubliceerd en Gearchiveerd door op elk van deze opties te klikken. U kunt ook zoeken op basis van competenties door op Competenties te klikken en een van deze te kiezen.

U krijgt een gefilterde lijst met cursussen waarin u de gewenste cursussen kunt selecteren.

+++

+++Kan ik de thema&#39;s voor de toepassing wijzigen? Hoe?

Ja, u kunt de thema&#39;s en branding van de toepassing Learning Manager aanpassen aan de vereisten van uw organisatie. Een set van vijf representatieve afbeeldingen is meegeleverd, zodat u een voorbeeld van uw kleurenthema kunt bekijken voordat u het op uw toepassing toepast. Klik op de symbolen &lt; en > links en rechts van de afbeeldingen om deze vooraf te bekijken.

Klik **[!UICONTROL Branding]** op de linkerruit om uw organisatienaam bij te werken, subdomein, logboekstijlen en thema&#39;s te veranderen. Klik **[!UICONTROL geef]** naast elk van deze onderwerpen uit om de inhoud te wijzigen.

Verwijs naar [ de thema&#39;s van de Kleur en brandingHulp ](/help/migrated/administrators/feature-summary/themes.md) voor meer informatie.

+++

+++Hoe stel ik badges in voor de cursussen?

1. Klik op Badges in het linkerdeelvenster nadat u zich als beheerder hebt aangemeld.
1. Klik op Toevoegen rechtsboven op de pagina die verschijnt.
1. Voeg de naam van de badge toe.
1. Upload de badge door op Badge uploaden te klikken vervolgens op Opslaan.

+++

+++Hoe stel ik gamificationpunten in voor de cursussen?

Volg onderstaande stappen om gamificationpunten voor studenten in te stellen:

1. Klik op Gamification nadat u zich als Beheerder hebt aangemeld. Er verschijnt een pagina met een lijst van bronzen, zilveren, gouden en platina niveaus en de vereiste punten om elk overeenkomstig niveau te behalen. Er is een lijst met taken en bijbehorende punten beschikbaar.
1. Klik op het pictogram Bewerken naast elke taak om de punten in te stellen/te wijzigen.

Verwijs [ eigenschap van de Gamification ](/help/migrated/administrators/feature-summary/gamification.md) voor meer informatie.

+++

+++Hoe maak ik rapporten voor managers en studenten?

Volg onderstaande stappen om rapporten te maken:

1. Klik op Rapporten in het linkerdeelvenster. De pagina Rapportoverzicht wordt geopend.
1. Voor de pagina van Rapporten, voegt de klik **&#x200B;**&#x200B;bij de hoger-juiste hoek toe.

   **[!UICONTROL voeg de dialoog van het Rapport]** toe verschijnt.

1. Vul alle verplichte velden in en klik op Opslaan.

Alleen beheerders en managers kunnen rapporten maken of bekijken. Verwijs naar [ rapporteigenschap ](/help/migrated/administrators/feature-summary/reports.md) voor meer informatie.

+++

+++Hoe wijzig ik in de rollen student, manager en auteur?

Wanneer u zich aanmeldt bij uw account, kunt u naar andere rollen zoals student, manager en auteur overstappen zonder u bij uw account af te melden.

1. Klik op het omlaagwijzende pijltje naast uw profielfoto in de rechterbovenhoek van de pagina.\
   Er verschijnt een pop-upmenu.
1. Selecteer elke beschikbare rol om toegang te krijgen tot de respectieve rolaccounts.

+++

+++Hoe neem ik meldingen voor de gebruikers op?

Managers, auteurs en studenten kunnen meldingen zien op basis van de cursusactiviteiten. De beheerder kan meldingen voor alle gebruikers in-/uitschakelen door de onderstaande stappen te volgen:

1. Klik in het linkerdeelvenster op E-mailsjablonen en kies de tabbladen Algemeen, Gebruikersinschrijving, Voltooiingen en Feedback.
1. Klik in de onderstaande lijst met gebeurtenissen op de knoppen Nee/Ja naast elke gebeurtenis en kies Ja om de melding in te schakelen. Klik op Nee om het verzenden van meldingen voor een bepaalde gebeurtenis uit te schakelen.

+++

+++Hoe sta ik externe inschrijving voor de cursussen toe?

Adobe Learning Manager biedt u de mogelijkheid om externe afdelingsleden of externe medewerkers van uw organisatie in te schrijven voor de toepassing.

1. Klik **[!UICONTROL Gebruikers]** op de linkerruit.
1. Klik **[!UICONTROL Extern]** op de linkerruit.
1. Klik **[!UICONTROL toevoegen]** bij de hoger-juiste hoek van de pagina.

   Het dialoogvenster Gebruiker toevoegen verschijnt.

1. Voeg profielnaam, e-mailadres van manager, toegewezen plaatsen en vervaldatum toe. U kunt ook een afbeelding aan het externe profiel toevoegen.
1. Klik op **[!UICONTROL Opslaan]**.

Beheerder kan de registratie-URL kopiëren en naar de externe inschrijvingsgroep verzenden. De externe gebruikers kunnen zich registreren, aanmelden bij de Learning Manager-toepassing en hun cursussen openen.

+++

+++Hoe voeg ik een vragenlijst toe voor de L1-feedback?

Maak een feedbackvragenlijst aan die studenten na het afronden van de cursussen kunnen invullen. Standaard zijn er drie voorbeeldvragen beschikbaar. Volg de onderstaande stappen om een vragenlijst te maken.

1. Klik op Feedback in het linkerdeelvenster. Er verschijnt een venster met feedbackvragenlijsten.
1. Klik **[!UICONTROL uitgeven]** om de vragenlijst toe te voegen/te wijzigen.

U kunt een set vragenlijsten toevoegen en ervoor kiezen deze niet te tonen als u ze niet nodig hebt. Klik op het selectievakje om een bepaalde vraag in of uit te schakelen.

+++

+++Hoe stel ik de vaardigheden en niveaus in?

1. Klik op Competenties in het linkerdeelvenster van het venster Beheerder.
1. Klik op Toevoegen om nieuwe competenties toe te voegen.
1. Voeg aan elk niveau de naam van de competentie, de beschrijving en de bijbehorende punten toe.

   Standaard is er voor elke competentie één niveau met 0 punten beschikbaar.

1. Klik [!UICONTROL **voeg niveau**] toe om nieuw niveau aan elke competentie toe te voegen en klik sparen. U kunt maximaal 5 niveaus toevoegen.

Nadat de competentie is opgeslagen, kunt u de niveaus van de competentie niet meer verwijderen. De beheerder kan ook studenten aan een bepaalde competentie en een bepaald niveau toewijzen.

+++

+++Hoe stel ik een factureringssysteem in voor de cursussen van mijn organisatie?

1. Klik [!UICONTROL **Facturering**] bij de linkerruit.

   Factureringsgegevens worden op de pagina weergegeven.

1. Klik het [!UICONTROL **Abonneren**] lusje.
1. Voer het aantal pakketten in dat u wilt bestellen in het veld voor studentenpakketten en klik op Bestelling plaatsen rechtsboven op de pagina.

   Kies het aantal pakketten op basis van het aantal studenten in uw organisatie en plaats uw bestelling. Voor een bestelde proces van de kooporde, schrijf aan ons in [ learningmanagersales@adobe.com ](mailto:learningmanagersales@adobe.com).

1. Voer uw contactgegevens in, kies het type creditcard, geef uw creditcardgegevens op en klik op Bestelling voltooien.

Verwijs [ eigenschap van het 0&rbrace; Factureringsbeheer voor meer informatie.](/help/migrated/administrators/feature-summary/billing-management.md)

+++

+++Kan ik het certificaatontwerp aanpassen? Hoe?

In Adobe Learning Manager kunt u studenten herkennen door badges uit te geven. Raadpleeg de functie Badges voor meer informatie.  Raadpleeg ook de functie Certificering.

+++

+++Hoe stel ik mijn bedrijfsprofiel in?

1. Nadat u login als Beheerder, klik **[!UICONTROL Info van het Bedrijf]** bij de linkerruit.
1. Voeg Bedrijfsprofiel, subdomein en logo toe door elk van deze opties op de pagina aan te klikken.

+++

+++Hoe voeg ik cursussen toe?

U moet uw rol als auteur veranderen om cursussen toe te voegen. U kunt de lijst van beschikbare cursussen slechts bekijken die op hun staat worden gebaseerd zoals **[!UICONTROL Voltooid]**, **[!UICONTROL Gepubliceerd]**, en **[!UICONTROL Gearchiveerd]**.

Om cursussen te bekijken, klik **[!UICONTROL Cursussen]** op linkerruit. Verwijs [ Creërend cursussen ](/help/migrated/administrators/feature-summary/courses.md) voor meer informatie

+++

+++Hoe voeg ik verschillende rollen toe aan de toepassing?

Volg de onderstaande stappen om nieuwe gebruikers toe te voegen:

1. Klik op Gebruikers in het linkerdeelvenster nadat u zich als beheerder hebt aangemeld. U kunt ook gebruikers toevoegen door in het linkerdeelvenster van het venster op Aan de slag te klikken en vervolgens op Gebruikers toevoegen.
1. Klik op Toevoegen rechtsboven op de pagina om nieuwe gebruikers toe te voegen.

Standaard wordt aan alle nieuwe gebruikers de rol student toegewezen. U kunt Admin of auteursrollen aan de studenten toewijzen door **[!UICONTROL Acties]** bij de hoger-juiste hoek van de pagina te klikken en **[!UICONTROL te kiezen wijs Rol]** toe > **[!UICONTROL maakt Auteur]** of **[!UICONTROL maak Admin]**.

Verwijs [ nieuwe gebruikers ](/help/migrated/administrators/feature-summary/add-users-user-groups.md) eigenschap voor gedetailleerde informatie bij het toevoegen van studenten, auteurs en beheerders toevoegen.

+++

+++Hoe kan ik een achtergrondafbeelding voor een student wijzigen?

Neem contact op met het ondersteuningsteam van Leermanager.

+++

+++Waar vind ik mijn LMS-account-id?

U kunt de account-ID vinden in de browser waarin Learning Manager is geopend.

*/app/admin?i_qp_user_id=12761637 &amp;**accountId=6849***

+++

+++Is er een rapport dat ik kan opvragen, of een rapport dat iemand voor mij kan opvragen, dat me een lijst zal laten zien van alle cursussen in het LMS?

Ja, kunt u het Rapport van de a **[!UICONTROL Opleiding]** trekken dat alle Cursussen, het Leren Programma, Certificatie in LMS bevat. Volg de onderstaande stappen om het rapport te downloaden:

1. Meld u aan als beheerder.
2. Klik op **[!UICONTROL Rapporten]** > **[!UICONTROL de Rapporten van de Douane]** > **[!UICONTROL Rapporten van Excel]** > **[!UICONTROL Rapport van de Leeringen]**.
3. Selecteer **[!UICONTROL Alle Opleidingen]** van dropdown.
4. Klik op **[!UICONTROL Download]**.

+++

+++Waar kan ik de desktopversie van de app downloaden?

Volg de onderstaande stappen om de bureaubladversie te downloaden:

1. Meld u aan als beheerder.
2. Klik op **[!UICONTROL Sociaal Leren]** > **[!UICONTROL Montages]**.
3. Onder **[!UICONTROL Configuratie van de Download]**, klik op hyperlink afhankelijk van uw Werkende Systeem.

+++
