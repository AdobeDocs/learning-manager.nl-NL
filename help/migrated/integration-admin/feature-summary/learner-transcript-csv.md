---
jcr-language: en_us
title: Hoe u de CSV van het Studenttranscript moet interpreteren
description: Hoe u de CSV van het Studenttranscript moet interpreteren
contentowner: saghosh
preview: true
source-git-commit: fcc50e80f94bdcbc8de2cddac92f1a12b55e1e18
workflow-type: tm+mt
source-wordcount: '2997'
ht-degree: 88%

---



# Hoe u de CSV van het Studenttranscript moet interpreteren

Het Studenttranscript is een van de populairste rapporten van Adobe Learning Manager. Met dit rapport is het mogelijk om bijna alle details in slechts één CSV-rapport op te nemen.

Behalve dat het een rapport is dat gebruikers kunnen ophalen om leergedrag bij te houden en te analyseren, wordt het rapport ook gezien als model waarin Learning Manager kan worden ingesteld om gegevens over leergedrag te exporteren naar externe toepassingen/systemen.

Voor een doorsnee bedrijfsscenario wordt een periodieke export van het Learning Manager studenttranscript gemaakt, die geanalyseerd wordt om studenten die een belangrijk leerprogramma voltooien eruit te filteren en een cadeaubon te bestellen om ze te belonen als ze het programma op tijd af hebben.

Een andere gebruikscase is om leergedraggegevens toe te voegen aan een datawarehouse van een onderneming, waar leergegevens kunnen worden gecombineerd met andere bedrijfsgegevens om de samenhang tussen het leergedrag en andere procesgegevens te analyseren.

In de rest van dit document beschrijven we kort hoe u aan het Studenttranscript van Learning Manager komt; vervolgens geven we aan hoe elke rij en elke kolom in het rapport geïnterpreteerd moet worden.

Deze informatie kan nuttig zijn voor elke ontwikkelaar die Learning Manager met andere systemen wil integreren door de geëxporteerde studenttranscriptgegevens te verwerken.

## Download Studenttranscript uit de gebruikersinterface {#fetchlearnertranscriptfromtheuserinterface}

Vanuit de Profielinstellingen kan een student diens transcript downloaden. Voor meer informatie, zie *** [&#x200B; Transcriptie van de Student van de Download &#x200B;](/help/migrated/administrators/feature-summary/reports/learner-transcripts.md) &#x200B;***.

Beheerders kunnen Studenttranscripts genereren voor de hele organisatie, een bepaalde set gebruikers of leerobjecten, of een bepaalde set gebruikers én leerobjecten. Ze kunnen ook alle leerrecords opvragen voor een bepaalde tijdsduur en aangeven of er informatie op moduleniveau nodig is (standaard wordt deze informatie weggelaten). Voor meer informatie, zie [***Studenttranscripten downloaden***](/help/migrated/administrators/feature-summary/reports/learner-transcripts.md).

<!--Update above link?-->

Beheerders kunnen het systeem ook zo instellen dat het Studenttranscript periodiek wordt gemaild.

Het Studenttranscript dat via de UI wordt gegenereerd, is een Excel-bestand dat ook het &quot;Vaardigheidtranscript&quot; bevat. In dit document verwijzen we naar het gegenereerde CSV-rapport, met leeractiviteiten die betrekking hebben op de inschrijving, de start, de voortgang of de voltooiing van een leerobject.

## Studenttranscript exporteren {#exportlearnertranscript}

Als het Studenttranscript door een extern systeem moet worden gebruikt, biedt Learning Manager een functie die Gegevens exporteren heet, waarbij het Studenttranscript een van de soorten gegevens is die kunnen worden geëxporteerd. Zoals in de preambule wordt uitgelegd, is dit vereist voor de integratie van Learning Manager met een extern systeem dat leergedragsgegevens moet verwerken of voor het vullen van een bedrijfsdatawarehouse met leergedragsgegevens.

Voor details over de connectoren die Studenttranscripten exporteren, zie [Gegevens exporteren](/help/migrated/integration-admin/feature-summary/connectors.md) in de FTP-, Box- en PowerBI-connectoren.

Het doel van deze connectoren is om periodiek (één keer per N dagen) gegevens te exporteren naar een downstream-toepassing. Deze connectoren exporteren alleen de incrementele leergedraggegevens in elke run. Merk op dat deze connectoren het niet mogelijk maken om records op te halen die betrekking hebben op specifieke subsets van gebruikers of leerobjecten - het zijn altijd gegevens over alle gebruikers en alle leerobjecten in dat account.

In het geval van PowerBI moet de klant een werkruimte bieden waar Learning Manager deze gegevens stapsgewijs kan exporteren naar een dynamisch gemaakte dataset. Deze connector exporteert uitsluitend gegevens, waarbij de klanten desgewenst hun eigen rapporten/dashboards bouwen op basis van deze dataset.

Het volgende deel geeft aan hoe een downstream-systeem de records in het studenttranscript moet interpreteren.

## Hoe u het Studenttranscript moet interpreteren {#interpretthelearnertranscript}

Elke rij in een Studenttranscript kan worden beschouwd als leergedrag dat in een bepaalde periode is vastgelegd in Leermanager. Doorgaans exporteren de connectoren &#39;incrementele gegevens&#39;. De rijen vertegenwoordigen de leeractiviteiten die plaatsvonden tussen de laatste run van de connector en de huidige run.

Natuurlijk kunt u met de connectoren ook het studenttranscript aanvragen; in dat geval kan de gebruiker een begindatum opgeven en wordt ervan uitgegaan dat de einddatum de huidige datum is. Dit doet men doorgaans eenmalig en vervolgens stelt men de connector in om het incrementele studenttranscript op een specifiek tijdstip te exporteren, één keer per N dagen (standaardwaarde van N is 1).

Nu bespreken we wat bedoeld wordt met het Incrementele studenttranscript

In het studenttranscript staat elke rij voor een specifieke activiteit waarbij een specifieke leerling en een specifiek leerobject betrokken zijn. Wij zijn hoofdzakelijk geinteresseerd in welke staat een student met betrekking tot het het leren voorwerp is - **Ingeschreven**, **Begonnen**, **in voortgang**, en **Voltooid**. Daarom documenteert het studenttranscript ook vier overeenkomende data.

Er zijn nu drie typen leerobjecten, waarbij Leermanager de voortgang van de studenten bijhoudt en de geëxporteerde gegevens voortgangsinformatie op moduleniveau bevatten, de meest gedetailleerde inhoudseenheid die een student in Leerbeheer kan ervaren.

* **Cursus** - een samenstelling van één of meerdere modules
* **het Leren Programma** - een samenstelling van één of meerdere cursussen
* **Certificatie** - een samenstelling van één of meerdere cursussen.

Elke rij in het Studenttranscript kan betrekking hebben op de betrokkenheid van een specifieke gebruiker met een module, cursus, leerprogramma of certificering. Zodra een gebruiker is ingeschreven in een leerprogramma, zal het transcript aangeven dat de gebruiker is ingeschreven.

De kolommen van het Studenttranscript geven informatie over elke leeractiviteit en de volgende tabellen geven aan waar elke kolom voor staat.

## Studenttranscript

<table> 
 <tbody> 
  <tr> 
   <th width="158" valign="bottom"><p><b>Kolomnaam</b></p></th> 
   <th width="160" valign="bottom"><p><b>Soort waarde</b></p></th> 
   <th width="306" valign="bottom"><p><b>Beschrijving</b></p></th> 
  </tr> 
  <tr> 
   <td><p><b>Naam</b></p></td> 
   <td><p>Kan nooit leeg zijn</p></td> 
   <td><p>Naam van de student</p></td> 
  </tr> 
  <tr> 
   <td><p><b>e-mail</b></p></td> 
   <td><p>Kan nooit leeg zijn</p></td> 
   <td><p>E-mailadres van de student</p></td> 
  </tr> 
  <tr> 
   <td valign="bottom"><b>Adobe ID</b></td> 
   <td valign="bottom">Kan leeg zijn</td> 
   <td valign="bottom">Adobe ID van de student</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Unieke ID van gebruiker</b></td> 
   <td height="19" width="283">Kan leeg zijn</td> 
   <td height="19" width="728">Unieke ID van gebruiker van de student. Deze kolom is gebaseerd op de back-endinstelling, al dan niet ingeschakeld/uitgeschakeld op accountniveau.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Naam van het leerplan</b></p></td> 
   <td valign="middle"><p>Kan leeg zijn</p></td> 
   <td valign="middle">Naam van het leerplan (indien van toepassing), waarmee de gebruiker automatisch is toegewezen.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Leerplan/certificatie/cursus</b></p></td> 
   <td valign="middle"><p>Kan nooit leeg zijn</p></td> 
   <td valign="middle"><p>Naam van het leerpogramma, het certificaat of de cursus</p></td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Type</b></p></td> 
   <td valign="middle">Kan nooit leeg zijn</td> 
   <td valign="middle"><p>Het type leerobject, waarvoor de gebruiker is ingeschreven.</p></td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Cursus</b></p></td> 
   <td valign="middle"><p>Kan leeg zijn</p></td> 
   <td valign="middle">Naam van de cursus waarvoor de gebruiker is ingeschreven. Als de rij leeg is, staat deze voor een certificering of een leerprogramma. </td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Unieke ID van LO</b></td> 
   <td height="19" width="283">Kan leeg zijn</td> 
   <td height="19" width="728">Unieke leerobject-ID van het LO. Deze kolom is gebaseerd op de instelling, al dan niet ingeschakeld/uitgeschakeld op accountniveau</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Instantie  </b></p></td> 
   <td valign="middle">Kan nooit leeg zijn</td> 
   <td valign="middle">Naam van de instantie waarvoor de gebruiker van het leerobject is ingeschreven. </td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Selectiecriteria</b></p></td> 
   <td valign="middle"><p>Kan nooit leeg zijn</p></td> 
   <td valign="middle"><p>Basis van de inschrijving (hoe deze student is ingeschreven in dit leerobject).</p></td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Module</b></p></td> 
   <td valign="middle"><p>Kan leeg zijn</p></td> 
   <td valign="middle">Naam van de module binnen de cursussen. Als deze rij leeg is, staat deze voor een cursus, een leerprogramma of een certificering.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Versie</b></td> 
   <td height="19" width="283">Kan leeg zijn</td> 
   <td height="19" width="728">Versie van de module</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Leveringstype</b></td> 
   <td height="19" width="283">Kan leeg zijn</td> 
   <td height="19" width="728">Leveringstype van de module - eLearning, F2F, VC, activiteit.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Taal</b></td> 
   <td height="19" width="283">Kan leeg zijn</td> 
   <td height="19" width="728">Taal waarin de module door de student wordt gevolgd. Deze kolom toont alleen waarde voor eLearning-modules.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Opmerking</b></td> 
   <td height="19" width="283">Kan leeg zijn</td> 
   <td height="19" width="728">Opmerkingen die zijn toegevoegd door beheerder, instructeur voor de student terwijl hij of zij de aanwezigheid van de gebruiker markeert.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Inschrijvingsdatum (tijdzone Asia/Calcutta)</b></td> 
   <td height="19" width="283">Kan nooit leeg zijn</td> 
   <td height="19" width="728">Datum van inschrijving door de student voor het type LO.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Startdatum (tijdzone Asia/Calcutta)</b></td> 
   <td><p>Kan leeg zijn</p></td> 
   <td height="19" width="728">De datum waarop de student aan het LO is begonnen. Leeg betekent dat de student dit nog niet is begonnen.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Voltooiingsdatum (tijdzone Asia/Calcutta)</b></td> 
   <td><p>Kan leeg zijn</p></td> 
   <td><p>De datum waarop de student dit heeft voltooid. Leeg betekent dat de student dit nog niet heeft voltooid.</p></td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Deadline (tijdzone Asia/Calcutta)</b></td> 
   <td><p>Kan leeg zijn</p></td> 
   <td height="19" width="728">Datum waarop de student dit leerobject moet voltooien. Leeg betekent dat er geen deadline voor is.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Vervaldatum verstreken</b></td> 
   <td height="19" width="283">Ja/nee</td> 
   <td height="19" width="728">Huidige achterstallige status van de student die is ingeschreven voor het LO. Ja/nee</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Status</b></p></td> 
   <td valign="middle">Niet gestart/voltooid/in uitvoering/uitgeschreven</td> 
   <td valign="middle">Huidige voortgang % van de student die is ingeschreven voor het LO.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Voortgang %</b></p></td> 
   <td valign="middle">Kan leeg zijn</td> 
   <td valign="middle"><p>Geeft aan in hoeverre de student dit heeft voltooid.</p></td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Bestede tijd (minuten)</b></td> 
   <td height="38" width="283">Kan leeg zijn</td> 
   <td height="38" width="728">Door de student bestede studietijd in het LO, de rijen op moduleniveau geven de individuele studietijd per module weer. De rijen Cursus/Programma/Certificaatniveau geven de totale bestede studietijd weer.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Cijfer</b></p></td> 
   <td valign="middle">Geslaagd/niet geslaagd</td> 
   <td valign="middle">Geeft het succes van de student aan. 'Geslaagd' als de gebruiker aan de succescriteria heeft voldaan, anders 'Niet geslaagd'.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>Quizscore</b></p></td> 
   <td valign="middle">Kan leeg zijn</td> 
   <td valign="middle">De laatste door de student behaalde quizscore. Kan leeg zijn als de student de quiz niet heeft geprobeerd of als de inhoud geen quiz bevat of als de beheerder/docent geen score heeft gegeven.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Quiz_score_max</b></td> 
   <td height="38" width="283">Kan leeg zijn</td> 
   <td height="38" width="728">De laatst mogelijke maximale quizscore voor de module. Kan leeg zijn als de student de quiz niet heeft geprobeerd of als de inhoud geen quiz bevat.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Highest_Quiz_score</b></td> 
   <td height="38" width="283">Kan leeg zijn</td> 
   <td height="38" width="728">De hoogste quizscore die de student na meerdere pogingen heeft behaald. Kan leeg zijn als de student de quiz niet heeft geprobeerd of als de inhoud geen quiz bevat of als de beheerder/docent geen score heeft gegeven.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Highest_Quiz_score_max</b></td> 
   <td height="38" width="283">Kan leeg zijn</td> 
   <td height="38" width="728">De hoogst mogelijke maximale quizscore voor de module. Kan leeg zijn als de student de quiz niet heeft geprobeerd of als de inhoud geen quiz bevat.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Aantal pogingen</b></td> 
   <td height="19" width="283">Kan leeg zijn</td> 
   <td height="19" width="728">Het totale aantal pogingen van de student voor deze module, tot nu toe.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Maximaal toegestane pogingen</b></td> 
   <td height="19" width="283">Kan leeg zijn</td> 
   <td height="19" width="728">Het maximale aantal toegestane pogingen voor de student om de module te volgen.</td> 
  </tr> 
  <tr> 
   <td valign="middle"><p><b>userState</b></p></td> 
   <td valign="middle">Kan nooit leeg zijn</td> 
   <td valign="middle">Gebruikersstatus van de student: Actief/Verwijderd/Opgeschort.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Groepeerbaar Actief veld</b></td> 
   <td height="38" width="283">Kan leeg zijn</td> 
   <td height="38" width="728">Voor elk groepeerbaar Actief veld in het account is er een kolom, waarvan de kolomnaam Actief veld is en de waarde de specifieke waarde is die de student voor dat veld heeft.</td> 
  </tr> 
  <tr> 
   <td><p><b>Naam van manager</b></p></td> 
   <td><p><i>Kan leeg zijn</i></p></td> 
   <td height="19" width="728">Naam van manager van de student</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Inschrijvingsaantal</b></td> 
   <td height="38" width="283">1 of 0</td> 
   <td height="38" width="728">Inschrijvingsaantal student voor het LO. De LO-rij van het hoogste niveau geeft de waarde = '1' weer. De subtrainingen geven de waarde 0 weer.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283"><b>Aantal gestart</b></td> 
   <td height="19" width="283">1 of 0</td> 
   <td height="19" width="728">Aantal gestart student voor het LO. De LO-rij van het hoogste niveau geeft de waarde = '1' weer. De subtrainingen geven de waarde 0 weer.</td> 
  </tr> 
  <tr> 
   <td height="58" width="283"><b>Voltooiingsaantal</b></td> 
   <td height="58" width="283">1 of 0</td> 
   <td height="58" width="728">Voltooiingsaantal student voor het LO. De LO-rij van het hoogste niveau geeft de waarde = '1' weer als de student in afwachting is van voltooiing van die training. De subtrainingen geven de waarde 0 weer, zelfs in de status Openstaand. De LO-rij van het hoogste niveau geeft de waarde = '0' weer als de student de training heeft voltooid.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Deadline over N dagen</b></td> 
   <td height="38" width="283">1 of 0</td> 
   <td height="38" width="728">Er wordt een waarde van '1' of '0' weergegeven, afhankelijk van de deadline van de instantie waarvoor de student is ingeschreven. Dit hangt af van de waarde die is ingevoerd op het blad Leermateriaaloverzicht I &gt; veld 'Vervaldatum over'.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Deadline over N dagen voor gebruiker</b></td> 
   <td height="38" width="283">1 of 0</td> 
   <td height="38" width="728">Er wordt een waarde van '1' of '0' weergegeven, afhankelijk van de deadline van de instantie waarvoor de student is ingeschreven. Dit hangt af van de waarde die is ingevoerd op het blad Leermateriaaloverzicht II &gt; veld 'Vervaldatum over'.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Aantal van (voortgang groter dan N %)</b></td> 
   <td height="38" width="283">1 of 0</td> 
   <td height="38" width="728">Er wordt een waarde van '1' of '0' weergegeven, afhankelijk van de voortgang van de student in de training. Dit hangt af van de waarde die is ingevoerd op het blad Leermateriaaloverzicht I &gt; veld 'Voortgang meer dan'.</td> 
  </tr> 
  <tr> 
   <td height="38" width="283"><b>Aantal van (voortgang groter dan N %) voor gebruiker</b></td> 
   <td height="38" width="283">1 of 0</td> 
   <td height="38" width="728">Er wordt een waarde van '1' of '0' weergegeven, afhankelijk van de voortgang van de student in de training. Dit hangt af van de waarde die is ingevoerd op het blad Leermateriaaloverzicht II &gt; veld 'Voortgang meer dan'.</td> 
  </tr> 
  <tr> 
   <td height="19" width="283">T<b>raining-ID</b></td> 
   <td height="19" width="283">Kan nooit leeg zijn</td> 
   <td height="19" width="728">Training-ID van de training.</td> 
  </tr> 
  <tr> 
   <td height="20" width="283"><b>Duur training of module (minuten)</b></td> 
   <td height="20" width="283">Kan nooit leeg zijn</td> 
   <td height="20" width="728">Totale duur training of module (minuten) van de standaardinstantie van de training.</td> 
  </tr> 
 </tbody> 
</table>

### Leermateriaaloverzicht I

<table cellpadding="1" cellspacing="0" border="1"> 
 <tbody> 
  <tr> 
   <th>Kolomnaam<br></th> 
   <th>Soort waarde</th> 
   <th>Beschrijving</th> 
  </tr> 
  <tr> 
   <td height="19" width="264">Type</td> 
   <td height="19" width="253">Alle, Leerprogramma, Certificaat, Cursus.</td> 
   <td height="19" width="412">Het LO-type waarvoor de tabel Leermateriaaloverzicht gegevens weergeeft.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Groepeerbaar veld (profiel)</td> 
   <td height="19" width="253">Kan nooit leeg zijn</td> 
   <td height="19" width="412">Het profiel waarvoor de tabel Leermateriaaloverzicht gegevens weergeeft.</td> 
  </tr> 
  <tr> 
   <td height="38" width="264">Naam van manager</td> 
   <td height="38" width="253">Kan nooit leeg zijn</td> 
   <td height="38" width="412">De naam van de manager van wie de LO-gegevens van zijn of haar ondergeschikten moeten worden getoond in de tabel Leermateriaaloverzicht.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Rijlabels</td> 
   <td height="19" width="253">Kan nooit leeg zijn</td> 
   <td height="19" width="412">De LO-naam met de lijst met studenten die zijn ingeschreven voor het LO.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Aantal ingeschreven studenten</td> 
   <td height="19" width="253">Kan nooit leeg zijn</td> 
   <td height="19" width="412">Aantal studenten die voor het leerobject zijn ingeschreven.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Aantal studenten die het volgende hebben gestart</td> 
   <td height="19" width="253">Kan nooit leeg zijn</td> 
   <td height="19" width="412">Aantal studenten die het leerobject hebben gestart.</td> 
  </tr> 
  <tr> 
   <td height="19" width="264">Aantal studenten die het volgende hebben voltooid</td> 
   <td height="19" width="253">Kan nooit leeg zijn</td> 
   <td height="19" width="412">Aantal studenten die het leerobject hebben voltooid.</td> 
  </tr> 
  <tr> 
   <td height="38" width="264">Aantal studenten met een voortgang &gt;= N %</td> 
   <td height="38" width="253">Kan nooit leeg zijn</td> 
   <td height="38" width="412">Aantal studenten met een voortgang &gt;= N % (waarden).</td> 
  </tr> 
  <tr> 
   <td height="39" width="264">Aantal studenten met een vervaldatum over N dagen</td> 
   <td height="39" width="253">Kan nooit leeg zijn</td> 
   <td height="39" width="412">Aantal studenten met een vervaldatum over N dagen (waarden).</td> 
  </tr> 
 </tbody> 
</table>

### Leermateriaaloverzicht II

| Kolomnaam | Soort waarde | Beschrijving |
|---|---|---|
| Type | Alle, Leerprogramma, Certificaat, Cursus. | Het LO-type waarvoor de tabel Leermateriaaloverzicht gegevens weergeeft. |
| Groepeerbaar veld (profiel) | Kan nooit leeg zijn | Het profiel waarvoor de tabel Leermateriaaloverzicht gegevens weergeeft. |
| Naam van manager | Kan nooit leeg zijn | De naam van de manager van wie de LO-gegevens van zijn of haar ondergeschikten moeten worden getoond in de tabel Leermateriaaloverzicht. |
| Rijlabels | Kan nooit leeg zijn | De naam van de student met de lijst met LO&#39;s waarvoor de student is ingeschreven. |
| Aantal ingeschreven leerobjecten | Kan nooit leeg zijn | Aantal leerobjecten waarvoor een student is ingeschreven. |
| Aantal gestarte leerobjecten | Kan nooit leeg zijn | Aantal leerobjecten dat een student heeft gestart. |
| Aantal voltooide leerobjecten | Kan nooit leeg zijn | Aantal leerobjecten dat een student heeft voltooid. |
| Aantal leerobjecten met een voortgang >= N % | Kan nooit leeg zijn | Aantal leerobjecten van een student met een voortgang >= N % |
| Aantal leerobjecten met een vervaldatum over N dagen | Kan nooit leeg zijn | Aantal leerobjecten met een vervaldatum over N dagen. |

### Nalevingsoverzicht

| Kolomnaam | Soort waarde | Beschrijving |
|---|---|---|
| Type | Alle, Leerprogramma, Certificaat, Cursus. | Het LO-type waarvoor de tabel Leermateriaaloverzicht gegevens weergeeft. |
| Rijlabels (linkerkolom) | Kan nooit leeg zijn | De naam van de student met de lijst met LO&#39;s waarvoor de student is ingeschreven. |
| Rijlabels (linkerkolom) | Kan nooit leeg zijn | De naam van de student met de lijst met LO&#39;s waarvoor de student is ingeschreven. |

### Vaardighedentranscript

| .Kolomnaam | Soort waarde | Beschrijving |
|---|---|---|
| Naam | Kan nooit leeg zijn | Naam van de student |
| e-mail | Kan nooit leeg zijn | E-mailadres van de student |
| Adobe ID | Kan leeg zijn | Adobe ID van de student |
| Unieke ID van gebruiker | Kan leeg zijn | Unieke ID van gebruiker van de student. Deze kolom is gebaseerd op de back-endinstelling, al dan niet ingeschakeld/uitgeschakeld op accountniveau. |
| Vaardigheid | Kan nooit leeg zijn | Naam van vaardigheid toegewezen aan de student. |
| Vaardigheidsniveau | Kan nooit leeg zijn | Niveau van vaardigheid toegewezen aan de student. |
| Punten vereist | Kan nooit leeg zijn | Totaal aantal punten dat de student nodig heeft om de vaardigheid te behalen. |
| Punten verdiend | Kan nooit leeg zijn | Totaal aantal door de student verdiende punten voor de vaardigheid. |
| Voltooiingspercentage | Kan nooit leeg zijn | Voortgangspercentage om de vaardigheid te behalen. |
| Datum Toegewezen (tijdzone UTC) | Kan nooit leeg zijn | De datum waarop de vaardigheid aan de student is toegewezen. |
| Datum Bereikt (tijdzone UTC) | Kan nooit leeg zijn | De datum waarop de student de vaardigheid heeft behaald. |
| userState | Kan nooit leeg zijn | Gebruikersstatus van de student: Actief/Verwijderd/Opgeschort. |
| Groepeerbaar Actief veld | Kan leeg zijn | Voor elk groepeerbaar Actief veld in het account is er een kolom, waarvan de kolomnaam Actief veld is en de waarde de specifieke waarde is die de student voor dat veld heeft. |
| Naam van manager | Kan leeg zijn | Naam van manager van de student. |

### Vaardigheidsoverzicht I

| Kolomnaam | Soort waarde | Beschrijving |
|---|---|---|
| Na | Kan nooit leeg zijn | Het aantal studenten dat de vaardigheid heeft behaald vóór de ingevoerde (waarde) aantal dagen en deze moet opfrissen. |
| Naam | Een of meer of alle namen van studenten | De naam van de student aan wie een vaardigheid is toegewezen. |
| Naam van manager | Kan nooit leeg zijn | De naam van de manager van wie de vaardigheidsgegevens van zijn of haar ondergeschikten moeten worden getoond in de samenvattingstabel Vaardigheden. |
| Rijlabels | Kan nooit leeg zijn | De vaardigheidsnaam met de lijst met studenten aan wie de vaardigheid is toegewezen. |
| Aantal gebruikers die deze vaardigheid moeten hebben | Kan nooit leeg zijn | Aantal studenten die aan de vaardigheid zijn toegewezen. |
| Aantal gebruikers die deze vaardigheid hebben opgedaan | Kan nooit leeg zijn | Aantal studenten die de vaardigheid hebben behaald. |
| Aantal studenten die vaardigheden moeten opfrissen | Kan nooit leeg zijn | Aantal studenten die vaardigheden moeten opfrissen. |
| Nalevingspercentage (gebaseerd op opgedane vaardigheden) | Kan nooit leeg zijn | Het vooruitgangspercentage van de toegewezen vaardigheid. |

### Vaardigheidsoverzicht II

| Kolomnaam | Soort waarde | Beschrijving |
|---|---|---|
| Na | Kan nooit leeg zijn | Het aantal studenten dat de vaardigheid heeft behaald vóór de ingevoerde (waarde) aantal dagen en deze moet opfrissen. |
| Vaardigheid | Een of meer of alle vaardigheidsnamen | De namen van vaardigheden die zijn toegewezen aan studenten. |
| Naam van manager | Kan nooit leeg zijn | De naam van de manager van wie de vaardigheidsgegevens van zijn of haar ondergeschikten moeten worden getoond in de samenvattingstabel Vaardigheden. |
| Rijlabels | Kan nooit leeg zijn | De naam van de student met de toegewezen vaardigheden. |
| Aantal vaardigheden dat elke gebruiker moet hebben | Kan nooit leeg zijn | Aantal aan de student toegewezen vaardigheden. |
| Aantal vaardigheden dat elke gebruiker heeft | Kan nooit leeg zijn | Aantal vaardigheden behaald door de student. |
| Aantal vaardigheden dat moet worden opgefrist | Kan nooit leeg zijn | Aantal studenten die vaardigheden moeten opfrissen. |
| Nalevingspercentage | Kan nooit leeg zijn | Het vooruitgangspercentage van de toegewezen vaardigheid. |

* Soms kunnen beheerders een leerobject handmatig voltooien (vooral bij klassikale cursussen), vaak lang na de les. In een dergelijk scenario, als Gegevens exporteren is ingesteld om dagelijks Studenttranscipten te exporteren, kan de werkelijke voltooiingsdatum al voorbij zijn en dus zal de export nooit zulke voltooiingsrecords krijgen die gemarkeerd zijn als voltooid, vaak lang na de les. Wanneer dit wordt gedetecteerd, kunt u overwegen de transcriptie van een bepaalde startdatum naar de gebruikersinterface te exporteren (op verzoek). Vervolgens kunt u de transcriptie meenemen naar de downstreamtoepassing voor &quot;late verwerking&quot;. Tijdens dit proces moet u mogelijk de records negeren die al zijn verwerkt.
* Meerdere pogingen doen om een module te voltooien is alleen mogelijk als dat voor dit Leerobject is ingeschakeld. Als deze optie is ingeschakeld, ziet u nu per CSV-rij één poging tot een module. Niet alle pogingen op één dag kunnen worden gerapporteerd en dus kan het zijn dat het totale aantal pogingen met meer dan één toeneemt. Bovendien hoeft een poging niet per se de score te verbeteren, zodat u op een gegeven moment alleen de beste score te zien krijgt.
