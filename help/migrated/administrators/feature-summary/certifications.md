---
description: Leer hoe u certificeringen maakt, studenten inschrijft en gepubliceerde certificeringen bewerkt.
jcr-language: en_us
title: Certificeringen
contentowner: manochan
source-git-commit: 0052ccb2f5a8f9617bca2c7bad91c0cd18338b66
workflow-type: tm+mt
source-wordcount: '991'
ht-degree: 0%

---



# Certificeringen

Leer hoe u certificeringen maakt, studenten inschrijft en gepubliceerde certificeringen bewerkt.

Certificeer uw studenten één keer of op een terugkerend tijdstip met deze functie. Alleen beheerders kunnen de certificeringen voor studenten definiëren.

Als beheerder kunt u een certificeringsprogramma maken dat intern wordt gehost of door een derde partij wordt uitgevoerd. In het geval van een interne certificering, definieert u de cursussen die een student moet voltooien om te worden gecertificeerd. Publiceer het programma en wijs het vervolgens toe aan studenten.

## Een certificering maken {#createacertification}

1. Klikken **[!UICONTROL Certificering]** in het linkerdeelvenster.\
   Er wordt een pagina weergegeven met een lijst van alle concepten en gepubliceerde certificeringen.

1. Certificeringen weergeven in verschillende modi:

   1. Klikken **[!UICONTROL Concept]** om alle certificeringen in conceptstatus te zien. U moet het maken ervan voltooien.
   1. Klikken **[!UICONTROL Gepubliceerd]** om alle certificeringen te zien die door u zijn gepubliceerd.
   1. Klikken **[!UICONTROL Alles]** om de certificeringen in alle staten weer te geven.
   1. Sorteer en bekijk de lijst met certificeringen in oplopende of aflopende volgorde of op basis van de datum waarop u ze hebt bijgewerkt.

1. Klikken **[!UICONTROL Toevoegen]**.

   Er verschijnt een nieuwe certificeringspagina.

![](assets/add-new-certification.png)

*De pagina weergeven om een certificering toe te voegen*

1. Certificaatnaam en -beschrijving toevoegen.

<table>
 <tbody>
  <tr>
   <th>Veld</th>
   <th>Beschrijving</th>
  </tr>
  <tr>
   <td>Aantal dagen dat moet worden voltooid</td>
   <td>De deadline voor de certificering. Voer een numerieke waarde in.</td>
  </tr>
  <tr>
   <td>Type</td>
   <td>
    <p>Het type certificering:</p>
    <ul>
     <li><b>Herhaling</b>- Kies deze optie als de certificering na elk jaar, twee jaar of drie jaar moet plaatsvinden.</li>
     <li><b>Perpetueel</b>- Kies deze optie als de certificering eenmalig moet zijn.</li>
    </ul></td>
  </tr>
  <tr>
   <td>Opnieuw toewijzen</td>
   <td>Kies of u het certificaat opnieuw wilt toewijzen op basis van de voltooiingsdatum of op basis van de inschrijvingsdatum.<br></td>
  </tr>
  <tr>
   <td>Geldigheid (in maanden) <br></td>
   <td>Geef op hoe lang de certificering geldig blijft.</td>
  </tr>
  <tr>
   <td>Opeenvolging van cursussen<br></td>
   <td>Bepaal of studenten de cursussen op volgorde of op ongeordende wijze moeten volgen.<br></td>
  </tr>
  <tr>
   <td>Uitschrijving<br></td>
   <td>Schakel de optie in of uit om de studenten in staat te stellen zichzelf uit te schrijven.</td>
  </tr>
  <tr>
   <td>Uitgever van certificering<br></td>
   <td>
    <p>Kies <b>Intern</b> als het bij uw organisatie hoort, of kies <b>Extern</b> voor certificeringen van externe organisaties.</p>
    <p>Wanneer u <b>Externe certificering</b>ziet u nog twee opties-</p>
    <ul>
     <li>Zelfde als goedgekeurde datum<br></li>
     <li>Verzonden door student<br></li>
    </ul>
    <p>Studenten kunnen de juiste voltooiingsdatum voor externe certificeringen opgeven. In eerdere versies werd de voltooiingsdatum standaard door Prime ingesteld op basis van de goedkeuringsdatum van de manager. Voltooiingsdatum die door de student is opgegeven, moet groter zijn dan aanmaakdatum van het certificaat<span>.</span></p></td>
  </tr>
  <tr>
   <td>Duur</td>
   <td>Als u Externe certificering hebt gekozen, geeft u de duur op in minuten.</td>
  </tr>
  <tr>
   <td>Labels</td>
   <td>Voer de tags in die u aan het certificaat wilt koppelen. Tags zijn handig wanneer u naar het certificaat wilt zoeken.</td>
  </tr>
  <tr>
   <td>Catalogi selecteren<br></td>
   <td>Kies de catalogus waar het certificaat deel van uitmaakt.</td>
  </tr>
 </tbody>
</table>

Kies uit de cursussen die u aan de certificering wilt toevoegen **[!UICONTROL Cursussen]** > **[!UICONTROL Catalogus]** tabblad.

Houd de muis op elke cursustegel en klik op + om deze aan de certificering toe te voegen. Klikken **[!UICONTROL Voorvertoning]** om de cursus als student weer te geven voordat u deze toevoegt.

1. Klikken **[!UICONTROL Studieprogramma]** om de lijst met cursussen die u hebt toegevoegd te bekijken/verifiëren.
1. Klikken **[!UICONTROL Publiceren]**.

## Toewijzing van cursusinstanties voor certificeringen {#courseinstancemappingforcertifications}

De cursus en instantie toewijzen voor certificeringen:

1. Klik op Certificeringen in het linkerdeelvenster.
1. Selecteer Certificering van de certificering weergeven in de lijst met certificeringen waar u de cursus en de instantie wilt toewijzen.
1. Klik in het linkerdeelvenster op Cursussen. De cursussen voor de certificering worden weergegeven. Klik op Bewerken.
1. Houd de muis boven de cursus waarin u de instantietoewijzing wilt instellen, selecteer Toewijzing cursusinstantie.
1. Selecteer in het pop-upvenster dat verschijnt de instantie van de cursus die moet worden geleverd voor de certificering die u hebt gekozen.
1. Klik op Opslaan.

Een beheerder kan klassikale en virtuele klassikale cursussen toevoegen aan een leerprogramma. Elke sessie die de auteur tijdens het maken van de cursus heeft gegeven, wordt de standaardinstelling. Wanneer de beheerder cursussen aan een leerprogramma toevoegt, wordt deze standaard toegewezen aan de standaardinstantie van alle cursussen, maar de beheerder kan de instantietoewijzing wijzigen. Het aantal cursussen dat aan een leerprogramma is toegevoegd, is ook zichtbaar op de instantiepagina, zoals hieronder getoond.

## Volledig besturingselement voor catalogus inschakelen {#catalog}

Zoals volledig verlenen [catalogusbeheer voor leermateriaal of modules](shared-catalog-full-control.md)kunt u ook volledige cataloguscontrole inschakelen voor certificeringen.

## Schrijf studenten in of uit voor de certificering {#enrollorunenrolllearnerstothecertification}

Ga voor meer informatie over het inschrijven van studenten en de te volgen stappen naar [Studenten inschrijven](courses.md#main-pars_header_1058138132).

## Uitschrijving voor studenten {#unenrollmentforlearners}

Tijdens het maken van certificeringen heeft de beheerder de mogelijkheid om te selecteren of studenten zichzelf kunnen uitschrijven voor de certificering. Als de beheerder de optie selecteert, kan de student zichzelf uitschrijven.

![](assets/unenrollment.png)

*Kies ervoor om studenten uit te schrijven*

## Voltooiing markeren {#markcompletion}

Beheerders kunnen een certificering als voltooid markeren met de optie die voor hen beschikbaar is. Volg de volgende stappen om de voltooiing van een certificering te markeren.

1. Openen **[!UICONTROL Certificering]** > **[!UICONTROL Studenten]**.

   De pagina Studenten wordt geopend met de lijst van ingeschreven studenten.

1. Selecteer één/meerdere/alle studenten om de voltooiing van de certificering te markeren met behulp van het selectievakje dat beschikbaar is voor elke student.
1. Klikken  **[!UICONTROL Handeling]** > **[!UICONTROL Voltooiing markeren.]**

   Houd er rekening mee dat als een certificering meerdere cursussen heeft, de voltooiing voor alle cursussen wordt gemarkeerd.

## Verplichte cursussen voor externe certificering {#mandatory}

In eerdere versies van Learning Manager was voltooiing van een cursus door de student in Externe certificering niet verplicht om een certificaat te voltooien.

U kunt cursussen nu verplicht maken door de optie **[!UICONTROL Vereiste cursussen instellen als Verplicht voor voltooiing van certificaat]** op het tabblad Curriculum tijdens het bewerken van de certificering.

## Een gepubliceerde certificering bewerken {#editingapublishedcertification}

Een certificering kan door een beheerder worden bewerkt in een gepubliceerde status. In deze status kan de beheerder alle onderdelen van een certificering bewerken en opnieuw publiceren.

Als u een gepubliceerde certificering wilt bewerken, klikt u op de certificeringskaart en klikt u op **[!UICONTROL Bewerken]** rechtsboven op de pagina.

Als u tijdens het bewerken van de onderdelen van een certificering de pagina moet verlaten, moet u de certificering opnieuw publiceren. U ontvangt een bevestiging in een dialoogvenster waarin u wordt gevraagd de certificering opnieuw te publiceren.

## Abonnement {#subscription}

Een beheerder kan quizscore en statusrapporten van studenten ophalen. Ze kunnen de rapportfrequentie, het onderwerp van de e-mail en de e-mail-ID van de ontvangers instellen. Afhankelijk van de ingestelde frequentie krijgt de ontvanger een e-mail met het rapport als bijlage.

![](assets/report-subscription.jpeg)

*Rapportfrequentie en andere eigenschappen instellen*
