---
description: Lees hoe u certificeringen kunt maken, studenten kunt inschrijven en gepubliceerde certificeringen kunt bewerken.
jcr-language: en_us
title: Certificeringen
contentowner: manochan
exl-id: 406d1c33-aac3-47e1-9b32-83874976ce54
source-git-commit: 69ef7d1e27fac3db49cbb4b9f9403f74e146efb5
workflow-type: tm+mt
source-wordcount: '1024'
ht-degree: 67%

---

# Certificeringen

Lees hoe u certificeringen kunt maken, studenten kunt inschrijven en gepubliceerde certificeringen kunt bewerken.

Gebruik deze functie om uw studenten eenmalig of volgens een vast schema te certificeren. Alleen beheerders kunnen de certificeringen voor studenten definiëren.

Als beheerder kunt u een certificeringsprogramma maken dat intern of door een derde partij wordt gehost. In het geval van een interne certificering, definieert u de cursussen die een student moet volgen om zich te laten certificeren. Publiceer het programma en wijs het vervolgens toe aan de studenten.

## Een certificering maken {#createacertification}

1. Klikken **[!UICONTROL Certificering]** in het linkerdeelvenster.\
   Er wordt een pagina weergegeven met een lijst van alle concepten en gepubliceerde certificeringen.

1. Certificeringen weergeven in verschillende modi:

   1. Klikken **[!UICONTROL Concept]** om alle certificeringen in conceptstatus te zien. U moet het maken van certificeringen voltooien.
   1. Klikken **[!UICONTROL Gepubliceerd]** om alle certificeringen te zien die door u zijn gepubliceerd.
   1. Klikken **[!UICONTROL Alles]** om de certificeringen in alle staten weer te geven.
   1. Sorteer en bekijk de lijst met certificeringen in oplopende of aflopende volgorde of op basis van de datum waarop u ze hebt bijgewerkt.

1. Klik op **[!UICONTROL Toevoegen]**.

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
   <td>Dagen voor voltooiing</td>
   <td>De deadline voor de certificering. Voer een numerieke waarde in.</td>
  </tr>
  <tr>
   <td>Type</td>
   <td>
    <p>Kies het type certificering:</p>
    <ul>
     <li><b>Terugkerend</b> - Kies deze optie als de certificering na elk jaar, twee jaar of drie jaar moet plaatsvinden.</li>
     <li><b>Permanent</b> - Kies deze optie als de certificering eenmalig moet plaatsvinden.</li>
    </ul></td>
  </tr>
  <tr>
   <td>Hertoewijzing</td>
   <td>Kies of u het certificaat opnieuw wilt toewijzen op basis van de voltooiingsdatum of op basis van de inschrijvingsdatum.<br></td>
  </tr>
  <tr>
   <td>Geldigheid (in maanden) <br></td>
   <td>Geef op hoe lang de certificering geldig is.</td>
  </tr>
  <tr>
   <td>Volgorde van de cursussen<br></td>
   <td>Bepaal of studenten zich wel of niet aan de volgorde van de cursussen moeten houden.<br></td>
  </tr>
  <tr>
   <td>Uitschrijving<br></td>
   <td>Schakel de optie waarmee studenten zichzelf kunnen uitschrijven in of uit.</td>
  </tr>
  <tr>
   <td>Certificeringsuitgever<br></td>
   <td>
    <p>Kies <b>Intern</b> als het bij uw organisatie hoort, of kies <b>Extern</b> voor certificeringen van externe organisaties.</p>
    <p>Wanneer u <b>Externe certificering</b> kiest, zijn er twee verdere opties.</p>
    <ul>
     <li>Zelfde als goedkeuringsdatum<br></li>
     <li>Ingediend door student<br></li>
    </ul>
    <p>Studenten kunnen de juiste voltooiingsdatum voor externe certificeringen opgeven. In eerdere versies werd de voltooiingsdatum standaard door Prime ingesteld op basis van de goedkeuringsdatum van de manager. De door de student opgegeven voltooiingsdatum moet later zijn dan de aanmaakdatum van het certificaat<span>.</span></p></td>
  </tr>
  <tr>
   <td>Duur</td>
   <td>Als u voor externe certificering hebt gekozen, geeft u de duur op in minuten.</td>
  </tr>
  <tr>
   <td>Tags</td>
   <td>Voer de tags in die u aan het certificaat wilt koppelen. Tags zijn hulpmiddelen om naar het certificaat te zoeken.</td>
  </tr>
  <tr>
   <td>Catalogi selecteren<br></td>
   <td>Kies de catalogus waar het certificaat onderdeel van is.</td>
  </tr>
 </tbody>
</table>

Selecteer de producten, rollen en rolniveau van het **[!UICONTROL Aanbevelen voor]** om dit leerpad voor te stellen aan de gebruikers die belangstelling hebben getoond voor deze producten en rollen.

![](assets/recommend-for.png)

*Aanbeveling*

Kies uit de cursussen die u aan de certificering wilt toevoegen **[!UICONTROL Cursussen]** > **[!UICONTROL Catalogus]** tabblad.

Houd de muis op elke cursustegel en klik op + om deze aan de certificering toe te voegen. Klikken **[!UICONTROL Voorvertoning]** om de cursus als student weer te geven voordat u deze toevoegt.

1. Klikken **[!UICONTROL Studieprogramma]** om de lijst met cursussen die u hebt toegevoegd te bekijken/verifiëren.
1. Klikken **[!UICONTROL Publiceren]**.

## Toewijzen van cursusinstanties voor certificeringen {#courseinstancemappingforcertifications}

Om de cursus en instanties toe te wijzen voor certificeringen:

1. Klik op Certificeringen in het linkerdeelvenster.
1. Selecteer in de lijst met certificeringen de optie Certificering weergeven voor de certificering waar u de cursus en instantie aan wilt toewijzen.
1. Klik in het linkerdeelvenster op Cursussen. De cursussen voor de certificering worden weergegeven. Klik op Bewerken.
1. Beweeg over de cursus waar u de instantietoewijzing wilt instellen, selecteer vervolgens Toewijzen van cursusinstantie.
1. Selecteer in de pop-up die verschijnt, de instantie van de cursus die moet worden gegeven voor de certificering die u hebt gekozen.
1. Klik op Opslaan.

Een beheerder kan klassikale en virtuele klassikale cursussen toevoegen aan een leerprogramma. De sessie die de auteur heeft opgegeven tijdens het maken van de cursus wordt de standaardinstantie. Wanneer de beheerder cursussen aan een leerprogramma toevoegt, worden deze standaard toegewezen aan de standaardinstantie van alle cursussen, maar de beheerder kan de instantietoewijzing wijzigen. Het aantal cursussen dat in een leerprogramma wordt toegevoegd is ook zichtbaar in de instantiepagina zoals hieronder getoond.

## Volledig beheer van catalogi inschakelen {#catalog}

Net als het verlenen van volledig [beheer van catalogi voor leermateriaal of modules](shared-catalog-full-control.md) kunt u ook volledig beheer van catalogi voor certificeringen inschakelen.

## Schrijf studenten in of uit voor de certificering {#enrollorunenrolllearnerstothecertification}

Raadpleeg [Studenten inschrijven](courses.md#main-pars_header_1058138132) voor meer informatie over het inschrijven van studenten en de te volgen stappen.

## Uitschrijving voor studenten {#unenrollmentforlearners}

Bij het aanmaken van certificeringen heeft de beheerder de mogelijkheid om te selecteren of studenten zichzelf kunnen uitschrijven voor de certificering. Als de beheerder de optie selecteert, dan kan de student zichzelf uitschrijven.

![](assets/unenrollment.png)

*Kies ervoor om studenten uit te schrijven*

## Voltooiing markeren {#markcompletion}

Beheerders kunnen een certificering als voltooid markeren met behulp van de optie die voor hen beschikbaar is. Volg de volgende stappen om een certificering als voltooid te markeren.

1. Openen **[!UICONTROL Certificering]** > **[!UICONTROL Studenten]**.

   De pagina Studenten wordt geopend met de lijst van ingeschreven studenten.

1. Selecteer één/meerdere/alle studenten en markeer de certificering als voltooid met het selectievakje dat voor elke deelnemer beschikbaar is.
1. Klikken  **[!UICONTROL Handeling]** > **[!UICONTROL Voltooiing markeren.]**

   Houd er rekening mee dat als de certificering van toepassing is op meerdere cursussen, alle cursussen als voltooid gemarkeerd zullen worden.

## Verplichte cursussen voor externe certificering {#mandatory}

In eerdere versies van Learning Manager was voltooiing van een cursus niet verplicht voor studenten in Externe certificering om een certificaat te voltooien.

U kunt cursussen nu verplicht maken door de optie **[!UICONTROL Vereiste cursussen instellen als Verplicht voor voltooiing van certificaat]** op het tabblad Curriculum tijdens het bewerken van de certificering.

## Een gepubliceerde certificering bewerken {#editingapublishedcertification}

Een certificering in de status Gepubliceerd kan worden bewerkt door een beheerder. In deze status kan de beheerder alle onderdelen van een certificering bewerken en opnieuw publiceren.

Als u een gepubliceerde certificering wilt bewerken, klikt u op de certificeringskaart en klikt u op **[!UICONTROL Bewerken]** rechtsboven op de pagina.

Als u tijdens het bewerken van de onderdelen van een certificering de pagina moet verlaten, moet u de certificering opnieuw publiceren. U krijgt een bevestiging in een dialoogvenster waarin u wordt gevraagd om de certificering opnieuw te publiceren.

![](assets/edit-a-certificate.png)

*Een certificaat bewerken*

## Abonnement {#subscription}

Een beheerder kan quizscore en statusrapporten van de student ophalen. Zij kunnen de rapportfrequentie, het onderwerp van de e-mail en de e-mail-ID van de ontvanger instellen. Afhankelijk van de ingestelde frequentie krijgt de ontvanger een e-mail met het rapport als bijlage.

![](assets/report-subscription.jpeg)

*Rapportfrequentie en andere eigenschappen instellen*
