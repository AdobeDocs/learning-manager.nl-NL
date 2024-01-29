---
jcr-language: en_us
title: De CSV van het Studenttranscript interpreteren
description: De CSV van het Studenttranscript interpreteren
contentowner: saghosh
preview: true
source-git-commit: fba5e5ddc1964b485be473bf356806f234688cf4
workflow-type: tm+mt
source-wordcount: '2997'
ht-degree: 0%

---



# De CSV van het Studenttranscript interpreteren

Het Studenttranscript is een van de populairste rapporten die worden gebruikt in Adobe Learning Manager. Met dit rapport kunt u vrijwel elk mogelijk detail in één CSV-indeling krijgen.

Naast een rapport dat gebruikers kunnen ophalen om leergedrag te volgen en te analyseren, kan het rapport ook worden gezien als de indeling waarin Leermanager kan worden ingesteld om gegevens over leergedrag naar externe toepassingen/systemen te exporteren.

Doorgaans bestaat het ondernemingsscenario uit het periodiek exporteren van studenttranscripten voor Leermanager, het analyseren om studenten die een belangrijk leerprogramma voltooien uit te pakken en het plaatsen van een opdracht voor een cadeaubon om tijdige voltooiing te herkennen en te belonen.

Een ander gebruiksgeval is het toevoegen van de gegevens van het leergedrag aan een entrepot van ondernemingsgegevens, waar men het leren gegevens met andere ondernemingsgegevens kan willen combineren om correlaties tussen het leren gedrag en andere procesgegevens te analyseren.

In de rest van het document beschrijven we kort hoe je het Studenttranscript kunt ophalen van Leermanager. Ga vervolgens verder met het geven van details over hoe elke rij en kolom van het rapport moet worden geïnterpreteerd.

Deze informatie kan nuttig zijn voor elke ontwikkelaar die van plan is om Learning Manager te integreren met andere systemen door de geëxporteerde studenttranscriptgegevens te verwerken.

## Studenttranscript ophalen vanuit de gebruikersinterface {#fetchlearnertranscriptfromtheuserinterface}

Een student kan zijn/haar transcript downloaden via de profielinstellingen. Zie *** voor meer informatie [Studenttranscript downloaden](../../administrators/feature-summary/learner-transcripts.md)***.

Beheerders kunnen Studenttranscripten genereren voor de hele organisatie, een specifieke set gebruikers of een specifieke set leerobjecten, of een specifieke set gebruikers en leerobjecten. Ze kunnen ook alle leerrecords ophalen voor een tijdsintervalduur en aangeven of informatie op moduleniveau vereist is (standaard wordt informatie op moduleniveau weggelaten). Zie voor meer informatie [***Studenttranscripten downloaden***](../../administrators/feature-summary/learner-transcripts.md).

<!--Update above link?-->

Beheerders kunnen het systeem ook zo instellen dat het Studenttranscript periodiek wordt verzonden via e-mail.

Het Studenttranscript dat via de UI wordt gegenereerd, is een Excel-bestand dat ook het &quot;Vaardigheidtranscript&quot; bevat. In dit document verwijzen we naar wat wordt gegenereerd in de CSV-indeling, een rapport met leeractiviteiten met betrekking tot inschrijving, start, voortgang of voltooiing van een leerobject.

## Studenttranscript exporteren {#exportlearnertranscript}

Wanneer het Studenttranscript door een extern systeem moet worden gebruikt, biedt Learning Manager de functie Gegevens exporteren, waarbij het Studenttranscript een van de soorten gegevens is die kunnen worden geëxporteerd. Zoals in de preambule wordt uitgelegd, is dit vereist voor de integratie van Learning Manager met een extern systeem dat leergedragsgegevens moet verwerken of voor het vullen van een bedrijfsdatawarehouse met leergedragsgegevens.

Zie voor meer informatie over hoe de connectoren die ondersteuning bieden voor Exporteren van Studenttranscript, de [Sectie Gegevens exporteren](/help/migrated/integration-admin/feature-summary/connectors.md) in de FTP-, Box- en PowerBI-connectoren.

Het doel van deze connectoren is om periodiek gegevens naar een downstreamtoepassing te exporteren (eenmaal in N dagen). Deze connectoren exporteren dus alleen de incrementele leergedragsgegevens in elke run. Merk op dat deze connectoren het niet mogelijk maken om records op te halen die betrekking hebben op specifieke subsets van gebruikers of leerobjecten - het zijn altijd gegevens over alle gebruikers en alle leerobjecten in dat account.

In het geval van PowerBI moet de klant een werkruimte bieden waar Learning Manager deze gegevens stapsgewijs kan exporteren naar een dynamisch gemaakte dataset. Deze connector exporteert alleen gegevens, en de klanten moeten zo nodig hun eigen rapporten/dashboards bouwen op basis van deze dataset.

In het volgende gedeelte worden de details gegeven over hoe een downstream-systeem de records in het studenttranscript moet interpreteren.

## Het Studenttranscript interpreteren {#interpretthelearnertranscript}

Elke rij in een Studenttranscript kan worden beschouwd als leergedrag dat in een bepaalde periode is vastgelegd in Leermanager. Doorgaans exporteren de connectoren &#39;incrementele gegevens&#39;. De rijen vertegenwoordigen de leeractiviteiten die plaatsvonden tussen de laatste run van de connector en de huidige run.

Met de connectoren kunt u natuurlijk ook het studenttranscript op aanvraag ophalen. In dit geval kan de gebruiker een startdatum opgeven en wordt aangenomen dat de einddatum nu is. Meestal zou men dit eerst doen en dan de connector instellen voor het exporteren van het incrementele studenttranscript op een bepaald tijdstip, eenmaal in N dagen (de standaardwaarde van N, 1).

Laten we nu definiëren wat wordt verstaan onder incrementeel studenttranscript

In het studenttranscript vertegenwoordigt elke rij een specifieke activiteit met een specifieke student en een specifiek leerobject. We zijn vooral geïnteresseerd in de status van een student ten opzichte van het leerobject - **Ingeschreven**, **Gestart**, **In uitvoering**, en **Voltooid**. Daarom legt het studenttranscript ook vier corresponderende datums vast.

Er zijn nu drie typen leerobjecten, waarbij Leermanager de voortgang van de studenten bijhoudt en de geëxporteerde gegevens voortgangsinformatie op moduleniveau bevatten, de meest gedetailleerde inhoudseenheid die een student in Leerbeheer kan ervaren.

* **Cursus** - een samenstelling van een of meer modules;
* **Leerprogramma** - een samenstelling van een of meer cursussen
* **Certificering** - een samenstelling van een of meer cursussen.

Elke rij in het Studenttranscript kan betrekking hebben op de betrokkenheid van een specifieke gebruiker met een module, cursus, leerprogramma of certificering. Wanneer een gebruiker voor een leerprogramma is ingeschreven, geeft het transcript aan dat de gebruiker

De kolommen van het Studenttranscript bevatten verschillende informatie over elke leeractiviteit en de volgende tabellen beschrijven de semantiek van elke kolom.

## Studenttranscript

<table> 
 <tbody> 
  <tr> 
   <th width="158" valign="bottom"><p><b>Kolomnaam</b></p></th> 
   <th width="160" valign="bottom"><p><b>Type waarde</b></p></th> 
   <th width="306" valign="bottom"><p><b>Beschrijving</b></p></th> 
  </tr> 
  <tr> 
   <td><p><b>Naam</b></p></td> 
   <td><p>Nooit leeg</p></td> 
   <td><p>Naam van de student</p></td> 
  </tr> 
  <tr> 
   <td><p><b>email</b></p></td> 
   <td><p>Nooit leeg</p></td> 
   <td><p>E-mailadres van de student</p></td> 
  </tr> 
  <tr> 
   <td valign="bottom"><b>Adobe ID</b></td> 
   <td valign="bottom">Kan leeg zijn</td> 
   <td valign="bottom">Adobe ID van de student</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Unieke gebruikersnaam</b></td> 
   <td height="19" width="283">Kan leeg zijn</td> 
   <td height="19" width="728">Unieke gebruikersnaam van de student. Deze kolom is gebaseerd op de back-endinstelling of deze op accountniveau is in- of uitgeschakeld.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Naam leerplan</b></p></td> 
   <td valign="middle"><p>Kan leeg zijn</p></td> 
   <td valign="middle">Naam van het (eventuele) leerplan waarmee de gebruiker automatisch is toegewezen.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>LP/Certificering/Cursus</b></p></td> 
   <td valign="middle"><p>Nooit leeg</p></td> 
   <td valign="middle"><p>Naam van het leerprogramma, certificering of cursus</p></td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Type</b></p></td> 
   <td valign="middle">Nooit leeg</td> 
   <td valign="middle"><p>Het type van het leerobject waarvoor de gebruiker is ingeschreven.</p></td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Cursus</b></p></td> 
   <td valign="middle"><p>Kan leeg zijn</p></td> 
   <td valign="middle">Naam van de cursus waarvoor de gebruiker is ingeschreven. Als de rij leeg is, geeft deze een certificering of een leerprogramma weer. </td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>LO Unique ID</b></td> 
   <td height="19" width="283">Kan leeg zijn</td> 
   <td height="19" width="728">Unieke ID van het leerobject van de LO. Deze kolom is gebaseerd op de instelling voor in- en uitschakelen op accountniveau</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Instantie  </b></p></td> 
   <td valign="middle">Nooit leeg</td> 
   <td valign="middle">Naam van de instantie van de LO-gebruiker is ingeschreven. </td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Selectiecriteria</b></p></td> 
   <td valign="middle"><p>Nooit leeg</p></td> 
   <td valign="middle"><p>Basis van inschrijving (hoe deze leerling is ingeschreven voor deze LO).</p></td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Module</b></p></td> 
   <td valign="middle"><p>Kan leeg zijn</p></td> 
   <td valign="middle">Naam van module in de cursussen. Als deze rij leeg is, staat deze voor een cursus, leerprogramma of certificering.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Versie</b></td> 
   <td height="19" width="283">Kan leeg zijn</td> 
   <td height="19" width="728">Versie van de module</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Type levering</b></td> 
   <td height="19" width="283">Kan leeg zijn</td> 
   <td height="19" width="728">Leveringstype van de module - eLearning, F2F, VC, Activiteit.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Taal</b></td> 
   <td height="19" width="283">Kan leeg zijn</td> 
   <td height="19" width="728">Taal waarin de module door de student wordt gebruikt. In deze kolom wordt alleen de waarde voor eLearning-modules weergegeven.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Opmerking</b></td> 
   <td height="19" width="283">Kan leeg zijn</td> 
   <td height="19" width="728">Opmerkingen toegevoegd door beheerder, docent voor de student tijdens het markeren van de aanwezigheid van de gebruiker.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Inschrijvingsdatum (tijdzone Azië/Calcutta)</b></td> 
   <td height="19" width="283">Nooit leeg</td> 
   <td height="19" width="728">Datum van inschrijving door de student voor het LO-type.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Begindatum (tijdzone Azië/Calcutta)</b></td> 
   <td><p>Kan leeg zijn</p></td> 
   <td height="19" width="728">Datum waarop de student de LO heeft gestart. Leeg betekent dat de student dit nog niet heeft gestart.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Voltooiingsdatum (Tijdzone Azië/Calcutta)</b></td> 
   <td><p>Kan leeg zijn</p></td> 
   <td><p>Datum waarop de leerling dit heeft voltooid. Leeg betekent dat de student dit nog niet heeft voltooid.</p></td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Deadline (Tijdzone Azië/Calcutta)</b></td> 
   <td><p>Kan leeg zijn</p></td> 
   <td height="19" width="728">Datum waarop de student deze LO naar verwachting zal voltooien. Lege impliceert dat er geen termijn voor is.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Achterstallig</b></td> 
   <td height="19" width="283">Ja/Nee</td> 
   <td height="19" width="728">Status verstreken tijd van de leerling die is ingeschreven voor de LO. Ja/Nee</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Status</b></p></td> 
   <td valign="middle">Niet gestart/Voltooid/In bewerking/Uitgeschreven</td> 
   <td valign="middle">Huidige voortgang % van de leerling die is ingeschreven voor de LO.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Voortgang %</b></p></td> 
   <td valign="middle">Kan leeg zijn</td> 
   <td valign="middle"><p>Geeft aan in welke mate de student dit heeft voltooid.</p></td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Tijd besteed (minuten)</b></td> 
   <td height="38" width="283">Kan leeg zijn</td> 
   <td height="38" width="728">De leertijd die de student in de LO heeft doorgebracht, wordt in de rijen op moduleniveau weergegeven met de afzonderlijke rijen voor de leertijd. In de rijen op cursus-, programma- of certificaatniveau wordt de totale leertijd weergegeven.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Graad</b></p></td> 
   <td valign="middle">Doorgeven/zakken</td> 
   <td valign="middle">Geeft aan dat de student is geslaagd. 'Doorgeven' als de gebruiker heeft voldaan aan de succescriteria hiervoor, 'Mislukt' in andere gevallen.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Quiz Score</b></p></td> 
   <td valign="middle">Kan leeg zijn</td> 
   <td valign="middle">De meest recente quizscore die de student heeft behaald. Kan leeg zijn als de student de quiz niet heeft geprobeerd of de inhoud geen quiz heeft of als beheerder/docent geen score heeft toegewezen.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Quiz_score_max</b></td> 
   <td height="38" width="283">Kan leeg zijn</td> 
   <td height="38" width="728">De meest recente maximale quizscore die mogelijk is voor de module. Kan leeg zijn als de student de quiz niet heeft geprobeerd of de inhoud geen quiz bevat.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Highest_Quiz_score</b></td> 
   <td height="38" width="283">Kan leeg zijn</td> 
   <td height="38" width="728">De hoogste quizscore die de student heeft behaald bij meerdere pogingen. Kan leeg zijn als de student de quiz niet heeft geprobeerd of de inhoud geen quiz heeft of als beheerder/docent geen score heeft toegewezen.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Highest_Quiz_score_max</b></td> 
   <td height="38" width="283">Kan leeg zijn</td> 
   <td height="38" width="728">De hoogst mogelijke quizscore die mogelijk is voor de module. Kan leeg zijn als de student de quiz niet heeft geprobeerd of de inhoud geen quiz bevat.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Gezette pogingen</b></td> 
   <td height="19" width="283">Kan leeg zijn</td> 
   <td height="19" width="728">Het totale aantal pogingen dat de student tot nu toe heeft uitgevoerd voor deze module.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Maximaal toegestane pogingen</b></td> 
   <td height="19" width="283">Kan leeg zijn</td> 
   <td height="19" width="728">Het maximumaantal toegestane pogingen dat de student mag uitvoeren om de module te gebruiken.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>userState</b></p></td> 
   <td valign="middle">Nooit leeg</td> 
   <td valign="middle">Status gebruiker van de student: Actief / Verwijderd / Opgeschort.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Groepsgebonden actief veld</b></td> 
   <td height="38" width="283">Kan leeg zijn</td> 
   <td height="38" width="728">Voor elk groeperbaar actief veld in account is er een kolom, waarin de kolomnaam het veld Actief veld is en de waarde de specifieke waarde is die de student voor dat veld heeft.</td> 
  </tr> 
  <tr> 
   <td><p><b>Naam manager</b></p></td> 
   <td><p><i>Kan leeg zijn</i></p></td> 
   <td height="19" width="728">Naam van manager van de student</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Aantal inschrijvingen</b></td> 
   <td height="38" width="283">1 of 0</td> 
   <td height="38" width="728">Aantal inschrijvingen van de student voor de LO. In de LO-rij op het hoogste niveau wordt de waarde = '1' weergegeven. De subtrainingen geven de waarde 0 weer.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Aantal begonnen</b></td> 
   <td height="19" width="283">1 of 0</td> 
   <td height="19" width="728">Aantal startstudenten voor de LO. In de LO-rij op het hoogste niveau wordt de waarde = '1' weergegeven. De subtrainingen geven de waarde 0 weer.</td> 
  </tr> 
  <tr> 
   <td height="58" width="283"><b>Aantal gereed</b></td> 
   <td height="58" width="283">1 of 0</td> 
   <td height="58" width="728">Aantal voltooide studenten voor de LO. In de LO-rij op het hoogste niveau wordt de waarde = '1' weergegeven als de student in afwachting is van voltooiing in die training. De subtrainingen geven de waarde 0 weer, zelfs als de status In behandeling is. De LO-rij op het hoogste niveau heeft de waarde = '0' als de student de training heeft voltooid.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Vereist in N Days</b></td> 
   <td height="38" width="283">1 of 0</td> 
   <td height="38" width="728">Dit geeft de waarde '1' of '0' weer, afhankelijk van de deadline van de instantie waarvoor de student is ingeschreven. Het hangt af van de waarde die is ingevoerd op het leeroverzicht op het blad I &gt; Vervaldatum komt in veld.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Verwacht in N dagen voor gebruiker</b></td> 
   <td height="38" width="283">1 of 0</td> 
   <td height="38" width="728">Dit geeft de waarde '1' of '0' weer, afhankelijk van de deadline van de instantie waarvoor de student is ingeschreven. Dit is afhankelijk van de waarde die is ingevoerd op het Leeroverzicht II-blad &gt; Vervaldatum komt in het veld.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Aantal (voortgang groter dan N %)</b></td> 
   <td height="38" width="283">1 of 0</td> 
   <td height="38" width="728">Dit geeft de waarde '1' of '0' weer, afhankelijk van de voortgang van de student in de training. Dit is afhankelijk van de waarde die is ingevoerd op het leeroverzicht van het blad I &gt; veld Voortgang groter dan.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Aantal (voortgang groter dan N %) voor gebruiker</b></td> 
   <td height="38" width="283">1 of 0</td> 
   <td height="38" width="728">Dit geeft de waarde '1' of '0' weer, afhankelijk van de voortgang van de student in de training. Dit is afhankelijk van de waarde die is ingevoerd op het Leeroverzicht II-blad &gt; veld Voortgang groter dan.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283">T<b>trainings-id</b></td> 
   <td height="19" width="283">Nooit leeg</td> 
   <td height="19" width="728">Opleidings-id van de training.</td> 
  </tr> 
  <tr> 
   <td height="20" width="283"><b>Training- of moduleduur (min.)</b></td> 
   <td height="20" width="283">Nooit leeg</td> 
   <td height="20" width="728">Totale trainings- of moduleduur (min) van de standaardinstantie van de training.</td> 
  </tr> 
 </tbody> 
</table>

### Overzicht van leermateriaal I

<table cellpadding="1" cellspacing="0" border="1"> 
 <tbody> 
  <tr> 
   <th>Kolomnaam<br></th> 
   <th>Type waarde</th> 
   <th>Beschrijving</th> 
  </tr> 
  <tr> 
   <td height="19" width="264">Type</td> 
   <td height="19" width="253">Alle, Leerprogramma, Certificaat, Cursus.</td> 
   <td height="19" width="412">Het LO-type waarvoor de tabel Leeroverzicht gegevens moet weergeven.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Groepsbaar veld (profiel)</td> 
   <td height="19" width="253">Nooit leeg</td> 
   <td height="19" width="412">Het profiel waarvoor de overzichtstabel met leergegevens moet worden weergegeven.</td> 
  </tr> 
  <tr> 
   <td height="38" width="264">Naam manager</td> 
   <td height="38" width="253">Nooit leeg</td> 
   <td height="38" width="412">De naam van de manager, waarvan de onderliggende LO-betrokkenheidsgegevens moeten worden weergegeven in de overzichtstabel Leermateriaal.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Rijlabels</td> 
   <td height="19" width="253">Nooit leeg</td> 
   <td height="19" width="412">De LO-naam met de lijst met studenten die zijn ingeschreven voor de LO.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Aantal ingeschreven studenten</td> 
   <td height="19" width="253">Nooit leeg</td> 
   <td height="19" width="412">Aantal studenten dat voor de LO is ingeschreven.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Aantal studenten dat is gestart</td> 
   <td height="19" width="253">Nooit leeg</td> 
   <td height="19" width="412">Aantal studenten dat met de LO is begonnen.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Aantal studenten dat is voltooid</td> 
   <td height="19" width="253">Nooit leeg</td> 
   <td height="19" width="412">Aantal studenten dat de LO heeft voltooid.</td> 
  </tr> 
  <tr> 
   <td height="38" width="264">Aantal studenten dat vooruitgang heeft geboekt &gt;= N %</td> 
   <td height="38" width="253">Nooit leeg</td> 
   <td height="38" width="412">Aantal studenten met progressie &gt;= N % (waarden).</td> 
  </tr> 
  <tr> 
   <td height="39" width="264">Aantal studenten met vervaldatum in N dagen</td> 
   <td height="39" width="253">Nooit leeg</td> 
   <td height="39" width="412">Aantal studenten met vervaldatum in N dagen (waarden).</td> 
  </tr> 
 </tbody> 
</table>

### Overzicht van leermateriaal II

| Kolomnaam | Type waarde | Beschrijving |
|---|---|---|
| Type | Alle, Leerprogramma, Certificaat, Cursus. | Het LO-type waarvoor de tabel Leeroverzicht gegevens moet weergeven. |
| Groepsbaar veld (profiel) | Nooit leeg | Het profiel waarvoor de overzichtstabel met leergegevens moet worden weergegeven. |
| Naam manager | Nooit leeg | De naam van de manager, waarvan de onderliggende LO-betrokkenheidsgegevens moeten worden weergegeven in de overzichtstabel Leermateriaal. |
| Rijlabels | Nooit leeg | De naam van de student met de lijst LO&#39;s waaraan de student is ingeschreven. |
| Aantal ingeschreven leerobjecten | Nooit leeg | Aantal leerobjecten waarvoor de student is ingeschreven. |
| Aantal begonnen leerobjecten | Nooit leeg | Het aantal leerobjecten dat de student heeft gestart. |
| Aantal voltooide leerobjecten | Nooit leeg | Aantal leerobjecten dat de student heeft voltooid. |
| Aantal voortschrijdende leerobjecten >= N % | Nooit leeg | Aantal studenten Studenten Student heeft voortgang >= N %. |
| Aantal leerobjecten met vervaldatum in N dagen | Nooit leeg | Aantal leerobjecten met vervaldatum in N dagen. |

### Overzicht van compatibiliteit

| Kolomnaam | Type waarde | Beschrijving |
|---|---|---|
| Type | Alle, Leerprogramma, Certificaat, Cursus. | Het LO-type waarvoor de tabel Leeroverzicht gegevens moet weergeven. |
| Rijlabels (linkerkolom) | Nooit leeg | De naam van de student met de lijst LO&#39;s waaraan de student is ingeschreven. |
| Rijlabels (linkerkolom) | Nooit leeg | De naam van de student met de lijst LO&#39;s waaraan de student is ingeschreven. |

### Vaardigheidtranscriptie

| .Kolomnaam | Type waarde | Beschrijving |
|---|---|---|
| Naam | Nooit leeg | Naam van de student |
| email | Nooit leeg | E-mailadres van de student |
| Adobe ID | Kan leeg zijn | Adobe ID van de student |
| Unieke gebruikersnaam | Kan leeg zijn | Unieke gebruikersnaam van de student. Deze kolom is gebaseerd op de back-endinstelling of deze op accountniveau is in- of uitgeschakeld. |
| Vaardigheid | Nooit leeg | Naam van toegewezen vaardigheid aan de student. |
| Vaardigheidsniveau | Nooit leeg | Toegewezen vaardigheidsniveau aan de student. |
| Vereiste crediteringen | Nooit leeg | Totaal aantal studiepunten dat de student nodig heeft om de vaardigheid te behalen. |
| Verdiende tegoeden | Nooit leeg | Totaal aantal studiepunten verdiend door student voor de vaardigheid. |
| Voltooiingspercentage | Nooit leeg | Percentage voortgang om de vaardigheid te bereiken. |
| Toegewezen datum (UTC-tijdzone) | Nooit leeg | Datum waarop de vaardigheid aan de student is toegewezen. |
| Datum bereikt (UTC-tijdzone) | Nooit leeg | Datum waarop de student de vaardigheid heeft behaald. |
| userState | Nooit leeg | Status gebruiker van de student: Actief / Verwijderd / Opgeschort. |
| Groepsgebonden actief veld | Kan leeg zijn | Voor elk groeperbaar actief veld in account is er een kolom, waarin de kolomnaam het veld Actief veld is en de waarde de specifieke waarde is die de student voor dat veld heeft. |
| Naam manager | Kan leeg zijn | Naam van manager van de student. |

### Vaardigheidsoverzicht I

| Kolomnaam | Type waarde | Beschrijving |
|---|---|---|
| Na | Nooit leeg | Aantal studenten dat de vaardigheid heeft bereikt, voor het ingevoerde (waarde)aantal dagen dat moet worden vernieuwd. |
| Naam | Alle of elke naam van de student | De naam van de student waaraan een vaardigheid is toegewezen. |
| Naam manager | Nooit leeg | De managernaam, de waarvan ondergeschikte vaardigheidsconferentiegegevens op de overzichtstabel van de Vaardigheid moeten worden getoond. |
| Rijlabels | Nooit leeg | De vaardigheidsnaam met de lijst van studenten die aan de Vaardigheid worden toegewezen. |
| Aantal gebruikers dat deze vaardigheid moet hebben | Nooit leeg | Aantal studenten dat aan de vaardigheid is toegewezen. |
| Aantal gebruikers dat deze vaardigheid heeft bereikt | Nooit leeg | Aantal studenten dat de vaardigheid heeft bereikt. |
| Aantal studenten waarvan de vaardigheid moet worden vernieuwd | Nooit leeg | Aantal studenten waarvan vaardigheden moeten worden vernieuwd. |
| Percentage van naleving (gebaseerd op behaalde vaardigheid) | Nooit leeg | Het voortgangspercentage van de toegewezen vaardigheid. |

### Overzicht van vaardigheden II

| Kolomnaam | Type waarde | Beschrijving |
|---|---|---|
| Na | Nooit leeg | Aantal studenten dat de vaardigheid heeft bereikt vóór het ingevoerde (waarde)aantal dagen dat moet worden vernieuwd. |
| Vaardigheid | Alle of elke vaardigheidsnaam | De vaardigheidsnamen die aan studenten worden toegewezen. |
| Naam manager | Nooit leeg | De managernaam, de waarvan ondergeschikte vaardigheidsconferentiegegevens op de overzichtstabel van de Vaardigheid moeten worden getoond. |
| Rijlabels | Nooit leeg | De naam van de student met de lijst met toegewezen vaardigheden. |
| Aantal vaardigheden dat elke gebruiker moet hebben | Nooit leeg | Aantal aan de student toegewezen vaardigheden. |
| Aantal vaardigheden dat elke gebruiker heeft | Nooit leeg | Aantal door de student behaalde vaardigheden. |
| Aantal vaardigheden dat moet worden vernieuwd | Nooit leeg | Aantal studenten waarvan vaardigheden moeten worden vernieuwd. |
| Percentage naleving | Nooit leeg | Het voortgangspercentage van de toegewezen vaardigheid. |

* Soms kunnen beheerders de voltooiing van een leerobject handmatig markeren (met name voor cursussen in de klas), veel na de klasse. In een dergelijk scenario is het mogelijk dat, als Exportgegevens zijn ingesteld om dagelijks LT uit te voeren, de feitelijke voltooiingsdatum al is verstreken en dat de exportgegevens dan nooit zulke voltooiingsrecords krijgen als voltooid lang nadat de klasse is uitgevoerd. Wanneer dit wordt gedetecteerd, kunt u overwegen de transcriptie van een bepaalde startdatum naar de gebruikersinterface te exporteren (op verzoek). Vervolgens kunt u de transcriptie meenemen naar de downstreamtoepassing voor &quot;late verwerking&quot;. Tijdens dit proces moet u mogelijk de records negeren die al zijn verwerkt.
* Meerdere pogingen voor een module zijn afhankelijk van of dat is ingeschakeld voor die LO. Wanneer deze optie is ingeschakeld, ziet u nu één poging in een CSV-rij die betrekking heeft op een module. Mogelijk worden niet alle pogingen in een dag gemeld en ziet u dus het totale aantal pogingen met meer dan één toename. Een poging hoeft niet noodzakelijkerwijs tot een betere score bij te dragen, en op een bepaald moment zult u alleen de beste score behalen.
