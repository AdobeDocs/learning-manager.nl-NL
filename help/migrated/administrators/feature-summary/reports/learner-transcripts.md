---
description: Met de ALM (Studenttranscripten in Adobe Learning Manager) kunnen beheerders de voortgang van studenten in cursussen, modules, leerpaden en certificeringen volgen. Het steunt prestatiesevaluaties, nalevingscontrole, controles, en externe rapportering. Het rapport biedt een volledig overzicht van de betrokkenheid en prestaties van een student.
jcr-language: en_us
title: Studenttranscripten in Adobe Learning Manager
source-git-commit: a01ec6117ad49a1f9af0b31d48ad19ddc8443dde
workflow-type: tm+mt
source-wordcount: '4221'
ht-degree: 8%

---


# Studenttranscripten in Adobe Learning Manager

## Overzicht

Met de Studenttranscripten in Adobe Learning Manager (ALM) kunnen beheerders de voortgang van de studenten op granulair niveau bijhouden in cursussen, modules, leerpaden en certificeringen. De transcriptgegevens helpen bij prestatiebeoordelingen, nalevingstracering, audits en externe rapportagebehoeften.

>[!NOTE]
>
>Studenttranscripten kunnen worden gedownload door beheerders, aangepaste beheerders, managers of studenten.

In het geval van studenten moeten ze hun profielinstellingen starten en vervolgens hun leertranscripten downloaden als Excel-bestand. Dit transcript, gegenereerd voor een individuele student, geeft details over hun persoonlijke leertraject. Het omvat de namen van leerpaden, cursussen, instanties en modules, samen met belangrijke datums zoals inschrijving, voltooiing en deadlines. Ook wordt de voortgang bijgehouden via status, scores, quizscores (inclusief hoogste scores en maximum’s) en pogingen die zijn ondernomen. Bovendien ziet u hier trainings-id&#39;s, tijdsduur, uitschrijvingsdatums, prijzen en eventuele opmerkingen bij de indiening. Dit rapport biedt een uitgebreid overzicht van de betrokkenheid en prestaties van één student.

Organisaties kunnen de Studenttranscripten gebruiken om de leergedragsgegevens toe te voegen aan een bedrijfsdatawarehouse, waarin je leergegevens wilt combineren met andere bedrijfsgegevens om de correlaties tussen leergedrag en andere procesgegevens te analyseren.

## Doel en voordelen

* Hiermee maakt u auditklare records voor regelgevingsvereisten met tijdstempels en bewijs van voltooiing.
* Verbindt leeractiviteiten met werknemersontwikkeling en vaardigheidsverwerving.
* Volgt certificeringsstatus voor rollen waarvoor een verplichte training is vereist.
* Ondersteunt kwantitatieve meting van de effectiviteit van leerprogramma&#39;s.

## Gebruik voorbeelden van studenttranscripten

Studenttranscripten in Adobe Learning Manager volgen training, naleving en ontwikkeling van vaardigheden, zodat afdelingen de voltooiing kunnen controleren en de effectiviteit van het programma in de hele organisatie kunnen beoordelen.  Hier volgen enkele gebruiksscenario&#39;s voor Studenttranscripten:

* Een organisatie voor financiële diensten moet aantonen dat alle klantgerichte werknemers vóór de wettelijke deadline de verplichte nalevingsopleiding hebben voltooid.
* De IT-afdeling moet de huidige Java-programmeermogelijkheden afwegen tegen de toekomstige projectvereisten.
* HR wil de effectiviteit van het nieuwe wervingsprogramma voor medewerkers voor verschillende afdelingen evalueren.
* Het vluchthandteam moet ervoor zorgen dat alle veldtechnici de vereiste veiligheidscertificaten bijhouden.

## Toegangsbeheer en machtigingen

**Beheerders**

* Kan transcripten genereren voor alle studenten in alle catalogi.
* Heeft toegang tot alle rapportagefuncties, maar heeft mogelijk beperkingen met betrekking tot catalogus of gebruikersgroepen.
* Aangepaste beheerders: Toegang beperkt door toegewezen bereik en machtigingen.

**op bereik-gebaseerde beperkingen**

* Aangepaste beheerders kunnen alleen transcripten voor studenten in hun toegewezen gebruikersgroepen bekijken.
* Rapporten bevatten alleen leerobjecten uit catalogi waartoe de beheerder toegang heeft.

## Studenttranscripten genereren

1. Meld u als beheerder aan bij Adobe Learning Manager.
2. Selecteer **[!UICONTROL Rapporten]** van het linkernavigatiemenu.
3. Selecteer **[!UICONTROL de Rapporten van de Douane]** binnen Rapporten en selecteer dan **[!UICONTROL de Rapporten van Excel]**.
4. Selecteer **[!UICONTROL Transcripten van de Student]**.

   ![] ()

5. Selecteer **[!UICONTROL produceer Nieuw]**.
6. Selecteer het datumbereik waarvoor het transcript moet worden gegenereerd. Door gebrek, is de **[!UICONTROL Van]** datum de de registratiedatum van de student, en de **[!UICONTROL aan]** datum is altijd de huidige datum. U kunt alleen wijzigen vanaf welke begindatum u de gegevens nodig hebt.
7. Selecteer het volgende:
a. Selecteer de namen van de studenten in de **[!UICONTROL sectie Studenten selecteren]** . U kunt gebruikers of gebruikersgroepen selecteren of u kunt de e-mailadressen kopiëren en plakken van de studenten voor wie u transcripten wilt genereren. Zie de sectie [ het transcript van de Student ](#generate-learner-transcript-using-copy-paste) gebruikend exemplaar-kleef voor meer informatie.
b.Selecteer specifieke catalogi van de **[!UICONTROL Uitgezochte drop-down lijst van Catalogi]**. Het transcript wordt alleen gedownload voor de opgegeven catalogi.\
   c. Selecteer de **[!UICONTROL Status van de Inschrijving]**. Dit dropdownmenu heeft de volgende opties:

       * Alles selecteren 
       * Voltooid 
       * In bewerking 
       * Niet gestart 
       * Uitgeschreven 
   &#x200B;8. Geavanceerde opties: Selecteer **[!UICONTROL Geavanceerde opties]** om de transcripties te downloaden om het volgende te omvatten:

   a. Download transcripten voor studenten die uit een account zijn verwijderd door het selectievakje **[!UICONTROL Inclusief verwijderde studenten]** in te schakelen.
b. De informatie van het moduleniveau van de download in het transcript van de Student door **[!UICONTROL toe te laten de informatie van het moduleniveau]** checkbox. In dit geval worden de modulenamen en de tijd die aan elke module wordt doorgebracht als onderdeel van het transcript opgehaald als deze optie is ingeschakeld.
c. Download vaardigheidsgegevens en samenvattingsbladen door de optie **[!UICONTROL toe te laten omvat vaardigheidsgegevens en samenvattingsbladen]** checkbox. Zie de sectie van de Rapporten van Excel voor meer informatie.
&#x200B;9. U kunt ook de kolomwaarden selecteren die in het rapport moeten worden ingevuld. Dit biedt flexibiliteit om rapporten met specifieke kolomwaarden te downloaden zoals vereist. Selecteer de kolommen in de vervolgkeuzelijst.

   

Transcripties worden als zip-bestanden gegenereerd en naar uw computer gedownload wanneer de vaardigheidsgegevens niet worden opgenomen. Als het selectievakje Vaardigheden is ingeschakeld, worden transcripten gegenereerd en gedownload als . xlsx-bestanden

### Studenttranscripten genereren met kopiëren en plakken

Studenttranscripten ophalen is een moeizaam proces, omdat dit enkel voor één afzonderlijke student of gebruikersgroep per keer kan. Met de kopiëren- en plakkenfunctie kunt u nu in één keer de lijst met e-mail-ID&#39;s van studenten kopiëren en plakken.

1. Selecteer **[!UICONTROL E-mail IDs]** lusje om de gekopieerde lijst van unieke e-mailidentiteitskaart in te gaan

   

2. Plak unieke e-mailadressen van studenten die u wilt toevoegen, gescheiden door een komma, puntkomma of regeleinde.
3. Selecteer **[!UICONTROL bevestigen E-mails ID]** om te controleren als e-mail identiteitskaart u hebt ingevoerd geldig is. Als de ingevoerde e-mail-ID onjuist is, wordt deze rood gemarkeerd, samen met een validatiebericht.

   >[!NOTE]
   >
   >De knop Genereren blijft uitgeschakeld, tenzij alle ingevoerde e-mail-id&#39;s correct zijn.

4. Selecteer **[!UICONTROL produceer]** om de Transcripten van de Student voor alle vermelde e-mailidentiteitskaart te produceren

   >[!NOTE]
   >
   >Het genereren van studenttranscripten kan worden gecombineerd voor e-mail-id&#39;s die zijn ingevoerd op het tabblad Gebruikers en E-mail-id&#39;s.

### Wat bevat het rapport Studenttranscripten

Het rapport Studenttranscript is een combinatie van informatie over gebruikers, inschrijvingen en leerobjecten.
De volgende tabellen beschrijven elk type:

**gebruiker-verwante informatie**

In de volgende kolommen wordt de student geïdentificeerd.

| Veld | Beschrijving |
|---|---|
| Naam | Naam van de student. |
| E-mail | E-mailadres van student. |
| Adobe ID | Dit veld wordt alleen ingevuld wanneer gebruikers zich met hun Adobe ID aanmelden. Als zij tot Adobe Learning Manager door een organisatie-bepaalde [ Enige Sign-On (SSO) ](/help/migrated/administrators/feature-summary/multiple-sso-logins.md) toegang hebben, zal het gebied van Adobe ID leeg blijven. |
| Unieke ID van gebruiker | De unieke gebruikers-id is een externe id die wordt gegenereerd door accounts voor het geval dat deze geen e-mail-ID&#39;s van alle gebruikers of unieke e-mail-ID&#39;s van alle gebruikers hebben. <br> Het veld Unieke gebruikersnaam is een optioneel veld dat voor een account kan worden ingeschakeld. Het hoofddoel van het veld is om accounts toe te staan elke gebruiker een unieke id toe te wijzen om deze bij te houden, gebruikersrecords via API&#39;s bij te werken, gegevens te controleren of te synchroniseren in geautomatiseerde workflows. Het labelen van elke gebruiker gebeurt via CSV-import van gebruikers.</br><br> als een rekening voor Unieke Gebruiker - identiteitskaart heeft gekozen, dan rapporten, zoals de Transcripten van de Student, verstrekt Adobe Learning Manager de kolom in de rapporten.</br> |

**op inschrijving betrekking hebbende informatie**

In de volgende kolommen worden activiteit, voortgang of pogingen vastgelegd.

| Veld | Beschrijving |
|---|---|
| Inschrijvingsdatum (tijdzone UTC) | Datum- en tijdstempel van inschrijving door de student voor het type leerobject, te weten cursus, certificering of leerpad. |
| Datum markeren voltooid (tijdzone UTC) | Datum en tijdstempel van wanneer een docent een sessie of module als voltooid markeert. Als er geen sessie is gebeurd, wordt de kolom leeg weergegeven in het rapport. Ook, als een zitting is gebeurd en de instructeur niet de zitting als volledig heeft gemerkt, verschijnt de kolom leeg in het rapport. |
| Datum gestart (tijdzone UTC) | Datum en tijdstip waarop de leerling het leerobject heeft gestart. Leeg betekent dat de student dit nog niet is begonnen. |
| Voltooiingsdatum (tijdzone UTC) | Datum en tijd waarop de leerling dit heeft voltooid. Leeg betekent dat de student dit nog niet heeft voltooid. |
| Deadline (Tijdzone UTC) | Datum en tijd waarop de student dit leerobject moet voltooien. Leeg betekent dat er geen deadline voor is. |
| Vervaldatum verstreken | Huidige status van de student die is ingeschreven voor het leerobject. Ja/nee |
| Status | Geeft de status van de student aan tijdens het volgen van de cursus, certificering of leerpad.  De beschikbare statussen worden niet gestart, uitgeschreven, in uitvoering of voltooid. |
| Voortgang % | Huidige voortgang % van de leerling die de cursus, certificering of leerpad aflegt. |
| Bestede tijd (minuten) | De leertijd die de student in de LO heeft doorgebracht, wordt in de rijen op moduleniveau weergegeven met de afzonderlijke rijen voor de leertijd. In de rijen op cursus-/leerpad-/certificaatniveau wordt de totale leertijd weergegeven. |
| Cijfer | Hiermee wordt het succes van de student aangegeven. &#39;Geslaagd&#39; als de gebruiker aan de succescriteria heeft voldaan, anders &#39;Niet geslaagd&#39;. |
| Quiz_score | De meest recente quizscore die de student heeft behaald. Dit kan leeg zijn als de student de quiz niet heeft geprobeerd of als er geen quiz in staat of als de beheerder/docent geen score heeft toegewezen. |
| Quiz_score_max | De meest recente maximale quizscores die mogelijk zijn voor de module. Deze kan leeg zijn als de student de quiz niet heeft geprobeerd of als de inhoud geen quizzen bevat. |
| Highest_Quiz_score | De hoogste quizscore die de student na meerdere pogingen heeft behaald. Dit kan leeg zijn als de student de quiz niet heeft geprobeerd of als de inhoud geen quiz bevat of als de beheerder of docent geen score heeft toegewezen. |
| Highest_Quiz_score_max | De hoogst mogelijke quizscores die mogelijk zijn voor de module. Deze kan leeg zijn als de student de quiz niet heeft geprobeerd of als de inhoud geen quizzen bevat. |
| Aantal pogingen | Het totale aantal pogingen dat de student tot nu toe heeft uitgevoerd voor deze module. |
| Maximaal toegestane pogingen | Het maximumaantal pogingen dat de student mag uitvoeren om de module te gebruiken. |
| Opmerkingen bij inzending | Opmerkingen van de manager van een student nadat deze een leerobject hebben voltooid.<br> De gegevens van de inzendopmerkingen die door de docent zijn verstrekt, zijn opgenomen in de module voor het indienen van bestanden. Zie <a href="https://experienceleague.adobe.com/nl/docs/learning-manager/using/instructor/modules#filesubmissionforactivitymodules"> modules-Adobe Learning Manager voor meer informatie.</a></br> |
| Voltooiingsbron | <b> Nota:</b> voor VC de werkschema&#39;s van de schakelaaraanwezigheid, wanneer een student automatisch zoals aanwezig wordt gemerkt, zal de bron &quot;SELF, (student_email)&quot;tonen. |
| Opmerking bij voltooiing | De opmerkingen die de beheerder heeft gemaakt wanneer een student als voltooid wordt gemarkeerd nadat deze een cursus, certificering of leerpad heeft voltooid. De beheerder kan de voltooiingsopmerkingen voor een of meerdere studenten toevoegen. Zie <a href="https://experienceleague.adobe.com/nl/docs/learning-manager/using/admin/courses#completion-comments"> commentaren van de Voltooiing </a> voor meer informatie. |

**het Leren objecten-verwante informatie**

Deze hebben betrekking op cursussen, modules, leerpaden, certificeringen, enzovoort.

| Veld | Beschrijving |
|---|---|
| Naam van het leerplan | Titel van het leerplan. |
| Leerplan/certificatie/cursus | De titel van het leerobject. |
| Type | Het type leerobject waarvoor de gebruiker is ingeschreven. Bijvoorbeeld:<ul><li>Leerpad</li><li>Certificering</li><li>Cursus</li></ul> |
| Ingesloten pad | Een ingesloten pad is een type leerpad dat is opgenomen als onderdeel van een andere cursus     of een leerpad. Het veld geeft aan dat een student dat leerpad voltooit als onderdeel van een ander leerpad in plaats van als zelfstandige toewijzing. |
| Cursus | Naam van de cursus waarvoor de gebruiker is ingeschreven. Als de rij leeg is, geeft deze een certificerings- of leerpad weer. <br><b> Nota:</b> hoewel het Leren Wegen en Certificeringen    zijn samengesteld uit afzonderlijke cursussen of geneste leerpaden, behoudt elke component zijn eigen onafhankelijke record. Dit zorgt ervoor dat de vooruitgang, de voltooiing, en het melden van gegevens afzonderlijk voor zowel de ouder als de kindelementen worden gevolgd.</br> |
| Unieke ID van LO | De unieke id van het leerobject. Dit is nodig als de klant de LO in een extern systeem met een eigen id heeft. Dit is handig als u de LO-id en de Adobe Learning Manager LO van het externe systeem wilt toewijzen.<br> Een beheerder kan de optie Unieke ID&#39;s voor leerobjecten inschakelen op de pagina Instellingen. Als deze optie is ingeschakeld, wijst Adobe Learning Manager elke keer dat een auteur een cursus, certificering of leerpad maakt, een unieke id toe aan een leerobject. </br> |
| Instantie | De naam van de instantie van de leerobjectgebruiker is ingeschreven. |
| Selectiecriteria | Basis van inschrijving (hoe deze leerling is ingeschreven voor dit leerobject).<br> In Adobe Learning Manager kunnen studenten zich via verschillende methoden inschrijven voor leerobjecten: door manager aangewezen inschrijving: managers wijzen studenten aan voor specifieke cursussen. Studenten kunnen zich niet zelf inschrijven voor deze cursussen.</br><ul><li>Goedgekeurde inschrijving voor manager: studenten melden zich aan voor cursussen, maar voor inschrijving is goedkeuring van de manager vereist.</li><li>Zelfingeschreven: studenten schrijven zichzelf rechtstreeks in voor cursussen zonder goedkeuring.</li><li>Beheerder ingeschreven: beheerders schrijven studenten handmatig in voor cursussen.</li></ul> |
| Module | Naam van module in de cursussen. Alleen de modules met de status Voltooid of In bewerking worden in het rapport weergegeven. Als de status Niet gestart of Uitgeschreven is, blijft de kolom Module leeg.<br> download module-vlakke informatie in het transcript van de Student door <b> te selecteren laat de informatie van het moduleniveau </b> checkbox toe. In dit geval, worden de modulenamen en de tijd die aan elke module wordt doorgebracht als deel van het transcript opgehaald als deze optie wordt toegelaten.</br> |
| Module-ID | De unieke id van de module.<br><b> Nota:</b> de kolom van identiteitskaart van de Module verschijnt in het rapport slechts als u het Include vakje van de de moduleinformatie van de module terwijl het produceren van het transcript hebt geselecteerd.</br> |
| Versie | De moduleversie verwijst naar de specifieke versie van een module waarmee een student heeft gewerkt. Dit is vooral handig wanneer een module updates of wijzigingen heeft ondergaan, omdat beheerders zo kunnen bijhouden welke versie van de module door de student is geopend.<br> wanneer een auteur een nieuwe versie van een module uploadt, behandelt Adobe Learning Manager het als een nieuwe versie van de bestaande module. Zo kan inhoud worden bijgewerkt zonder dat dit alle studenten verstoort.</br><br> de Versie verschijnt als <b> de informatie van het moduleniveau </b> checkbox werd geselecteerd terwijl het produceren van het rapport.</br><br> zie <a href="https://elearning.adobe.com/2023/03/updating-the-module-in-adobe-learning-manager-how-to-replace-a-content-module-in-a-course-without-disturbing-the-users-progress" /> Bijwerkend een module in Adobe Learning Manager </a> voor meer informatie.</br> |
| Leveringstype | Geeft aan hoe de module wordt geleverd: Overvloeien, Lesruimte of Virtueel klaslokaal. |
| Taal | Taal waarin de module door de student wordt gebruikt. Deze kolom toont alleen waarde voor eLearning-modules. |
| Vervaldatum verstreken | Huidige status van de student die is ingeschreven voor het leerobject. Ja/nee |
| Cijfer | Hiermee wordt het succes van de student aangegeven. &#39;Geslaagd&#39; als de gebruiker aan de succescriteria heeft voldaan, anders &#39;Niet geslaagd&#39;. |

>[!INFO]
>
>De volgende kolommen zijn verborgen in de Studenttranscripten:
>
>* Inschrijvingsaantal
>* Aantal gestart
>* Voltooiingsaantal
>* Deadline over N dagen
>* Deadline over N dagen voor gebruiker
>* Aantal van (voortgang groter dan N %)
>* Aantal van (voortgang groter dan N %) voor gebruiker
>
>Deze kolommen worden alleen weergegeven als u tijdens het genereren van het transcript de optie Inclusief vaardigheidsgegevens en overzichtsbladen hebt geselecteerd. Deze kolommen worden gebruikt om samenvattingsdetails van een student te berekenen die is ingeschreven voor een leerobject.

| Velden | Beschrijving |
|---|---|
| Training-ID | Een door het systeem gegenereerde unieke id die is toegewezen aan de inschrijving van elke student in een specifieke cursus, certificering of leerpad. Als een student zich opnieuw voor dezelfde cursus inschrijft, wordt een nieuwe trainings-id gegenereerd. Eén student kan meerdere trainings-id&#39;s voor dezelfde cursus hebben. |
| Duur training of module (minuten) | Deze kolom toont de verwachte duur (in minuten) van een cursus, module of trainingsactiviteit zoals gedefinieerd bij het maken van de cursus. Het is niet de werkelijke tijd die een student doorbrengt, maar de geconfigureerde/toegewezen duur die aangeeft hoe lang de training moet duren. <br> Deze kolom toont de totale duur (in notulen) van het toegewezen leerpunt, dat of een leerweg of een individuele cursus kan zijn.</br><br><b> het Leren de duur van de Weg:<b> als het trainingspunt een het leren weg is, wordt zijn duur berekend als som de duur van alle cursussen binnen de het leren weg.</br><br> Voorbeeld: als Cursus 1 = 50 minuten en Cursus 2 = 60 minuten, dan de Duur van het Leerpad = 110 minuten.</br><br><b> Individuele cursusduur:</b> als het opleidingspunt een individuele cursus (geen deel van een het leren weg) is, wijst de duur op de tijd die voor die cursus alleen wordt vereist.</br> |
| Embedded_Course_ID | De id voor de cursus die onderdeel is van een leerpad of onderdeel van een andere cursus.<br> de kolom wordt bevolkt wanneer de rij een het Leren Weg of certificatie zelf vertegenwoordigt. Het toont de id&#39;s van de afzonderlijke cursussen die zijn ingesloten in het leerpad of de certificering. Het is niet bevolkt wanneer de rij zelf een cursus op slechts is, aangezien er geen ingebedde punten zijn.</br> |
| Ingesloten pad-ID | De id voor het pad waarin de ingesloten cursus bestaat.<br> de kolom identificeert unieke identiteitskaart van ingebedde Leerwegen. Het helpt cursussen binnen Leerpaden bij te houden en biedt inzicht in de hiërarchische structuur van leerpaden.</br> |
| Uitschrijvingsdatum (tijdzone UTC) | Datum van uitschrijving door de student voor het type leerobject. |
| Prijs ($) | De prijs van het leerobject waarvoor het is aangeschaft in de cursuscatalogus. Deze kolom komt alleen in het Studenttranscript te staan als de beheerder het selectievakje Prijzen voor cursussen/leerpaden/certificeringen inschakelen uit accountinstellingen heeft ingeschakeld. |

## Excel-rapporten

In het dialoogvenster Studenttranscripten kunt u ook vaardigheidsgegevens en overzichtsbladen downloaden als Excel-bestanden. Selecteer **[!UICONTROL omvatten de gegevens van Vaardigheden en summiere bladen]** checkbox en selecteer dan **&#x200B;**&#x200B;produceren om een Excel dossier met de volgende bladen te downloaden:

* Leermateriaaloverzicht I
* Leermateriaaloverzicht II
* Nalevingsoverzicht
* Vaardighedentranscript
* Vaardigheidsoverzicht I
* Vaardigheidsoverzicht II



### Wat bevat het leeroverzicht I-blad

Volg leerpaden, cursussen of certificeringen die actief worden gebruikt. Volg de lopende activiteit en eventuele geplande data voor de training.

* Aantal ingeschreven studenten: Geeft aan hoeveel studenten zijn ingeschreven voor een bepaald leerobject (cursus, leerpad of certificering), ongeacht of ze zijn gestart.
* Aantal studenten dat is gestart: toont het aantal studenten dat de cursus, certificering of het leerpad heeft gestart of gestart.
* Aantal leerlingen dat is voltooid: toont hoeveel studenten de training hebben voltooid en aan alle voltooiingscriteria hebben voldaan.
* Aantal studenten met progressie ≥ N%: geeft het aantal studenten weer dat ten minste de opgegeven voortgangsdrempel (bijvoorbeeld 70%) in de training heeft bereikt, zelfs als ze deze nog niet hebben voltooid.
* Aantal studenten met vervaldatum in N-dagen: geeft aan hoeveel studenten binnen de volgende &quot;N&quot;-dagen (bijvoorbeeld 7 dagen) een opleiding moeten volgen, wat handig is om aanstaande deadlines te identificeren.

### De gegevens interpreteren

Dit leeroverzicht I-rapport bevat twee leerpaden die aan de student zijn toegewezen.
In het voorbeeld:



* De gebruiker is ingeschreven voor twee leerpaden en is beide gestart.
* Geen van de leerpaden is nog voltooid.
* De leerling heeft in geen van beide paden verder gewerkt dan de drempel van 70%.
* Geen van beide trainingen heeft een vervaldatum binnen de volgende zeven dagen.

### Wat bevat het leeroverzicht II-blad

Volg de leeractiviteiten per student. Volg inschrijvingen, lopende activiteiten en vervaldatums voor studenten.

* Aantal ingeschreven leerobjecten: totaal aantal leerobjecten (LO&#39;s) waarvoor de leerling is ingeschreven voor elke cursus, certificering of leerpad. afzonderlijk tellen.
* Aantal begonnen leerobjecten: Geeft aan hoeveel van de ingeschreven leerobjecten de student heeft gestart of gestart.
* Aantal voltooide leerobjecten: toont hoeveel van de begonnen LO&#39;s de student volledig heeft voltooid.
* Aantal leerobjecten met progressie ≥ N%: geeft het aantal LO&#39;s weer waarin de leerling ten minste de opgegeven voortgangsdrempel heeft bereikt (in dit geval 70%).
* Aantal leerobjecten met vervaldatum in N dagen: identificeert LO&#39;s die binnen het volgende aantal dagen (in dit geval 7 dagen) moeten worden uitgevoerd, zodat deadlines dichterbij kunnen komen.

### De gegevens interpreteren

In het voorbeeld:



* De student is ingeschreven voor twee leerobjecten en is beide gestart.
* Er zijn geen leerobjecten voltooid.
* De student heeft nog geen 70% vooruitgang geboekt.
* Geen van de leerobjecten hoeft in de komende 7 dagen te worden uitgevoerd.

### Wat bevat het samenvattingsblad voor naleving

Volg studenten met aanstaande vervaldatums voor belangrijke cursussen, leerpaden of certificeringen.

| Kolom | Beschrijving |
|---|---|
| Type | Het LO-type waarvoor de tabel Leeroverzicht gegevens moet weergeven. |
| Rijlabels (linkerkolom) | De naam van de student met de lijst van LO&#39;s waarvoor de student is ingeschreven. |

### Wat bevat het vaardigheidtranscriptblad

| Kolom | Beschrijving |
|---|---|
| Naam | Volledige naam van de student die is gekoppeld aan het vaardigheidstranscript. |
| E-mail | E-mailadres van de student. |
| Unieke ID van gebruiker | Door de organisatie gedefinieerde unieke id voor de student. |
| Vaardigheid | De naam van de vaardigheid die aan de student is toegewezen (bijvoorbeeld Java Programming, Leadership). |
| Vaardigheidsniveau | Het expertiseniveau binnen de vaardigheid die de student verwacht te bereiken (bijvoorbeeld Beginner, Intermediate, Geavanceerd). |
| Punten vereist | Aantal leerpunten dat nodig is om het toegewezen vaardigheidsniveau te bereiken. |
| Punten verdiend | Aantal punten dat de leerling heeft verdiend voor het voltooien van het toegewezen vaardigheidsniveau. |
| Voltooiingspercentage | Het percentage vereiste punten dat de leerling heeft voltooid. |
| Toegewezen datum (UTC) | De datum waarop de vaardigheid aan de student is toegewezen. |
| Datum bereikt (UTC) | De datum waarop de leerling de vereiste punten heeft behaald en aan de criteria voor het vaardigheidsniveau heeft voldaan. |
| Naam van manager | Naam van de manager van de student die toezicht houdt op de leervoortgang. |

### Wat bevat het vaardigheidsoverzicht I blad

| Kolom | Beschrijving |
|---|---|
| Na | Geeft het aantal studenten aan dat een vaardigheid heeft bereikt vóór een gedefinieerde periode (in dagen), waarna de vaardigheid als verouderd wordt beschouwd of moet worden vernieuwd. Handig voor het identificeren van studenten met naderende of verlopen vaardigheidsresultaten.<br> zie <a href="https://experienceleague.adobe.com/nl/docs/learning-manager/using/admin/skills-levels"> vaardigheidsniveaus </a> voor meer informatie. |
| Naam | Volledige naam van de leerling aan wie de vaardigheid is toegewezen. |
| Naam van manager | Naam van de rapportmanager van de student. |
| Rijlabels | De specifieke vaardigheidsnaam die is toegewezen aan studenten die in deze rij worden weergegeven. Wordt gebruikt als koptekst voor groepen om de vaardigheidsgegevens van studenten in elke vaardigheidscategorie samen te vatten. |
| Aantal gebruikers die deze vaardigheid moeten hebben | Het totale aantal studenten aan wie de specifieke vaardigheid is toegewezen. |
| Aantal gebruikers die deze vaardigheid hebben opgedaan | Aantal studenten dat de vereiste leerobjecten met succes heeft voltooid om de vaardigheid te bereiken. |
| Aantal studenten die vaardigheden moeten opfrissen | Het aantal studenten waarvan de vaardigheidsprestatiedata de gedefinieerde vernieuwingsdrempel overschrijden. |
| Nalevingspercentage (gebaseerd op opgedane vaardigheden) | De compliance- of adoptiefrequentie voor de vaardigheid. |


### Wat bevat het Vaardigheids Summiere II blad

| Kolom | Beschrijving |
|---|---|
| Na | Aantal vaardigheden dat de student heeft behaald vóór de gedefinieerde vernieuwingsdrempel (in dagen). Dit identificeert vaardigheden die misschien verouderd zijn en moeten worden vernieuwd. |
| Vaardigheid | Naam van de vaardigheden die aan studenten zijn toegewezen. Dit kan worden gekoppeld aan een of meer leerobjecten, zoals cursussen, certificeringen of leerpaden. |
| Naam van manager | De naam van de directe manager van de student. |
| Rijlabels | De volledige naam van de student. Voor elke student worden de vaardigheden en de voortgang weergegeven in de volgende kolommen. |
| Aantal vaardigheden dat elke gebruiker moet hebben | Het totale aantal vaardigheden dat aan de student is toegewezen. |
| Aantal vaardigheden dat elke gebruiker heeft | Het totale aantal vaardigheden dat de leerling met succes heeft behaald door voltooiing van het/de bijbehorende leerobject(en). |
| Aantal vaardigheden dat moet worden opgefrist | Het aantal behaalde vaardigheden dat de vernieuwingsduur heeft overschreden en nu opnieuw moet worden gevalideerd. Deze waarde helpt de behoeften van de trainingsvernieuwing voor compliance of continue ontwikkeling bij te houden. |
| Nalevingspercentage | Geeft het algehele nalevingsniveau van de student aan op basis van het behalen van de vaardigheid. |

## Geschiedenis van studenttranscript downloaden

Met de geschiedenis van het downloaden van studenttranscripten kunnen beheerders bijhouden wie het transcript van elke student heeft gedownload en welke gebruikers ze hebben geopend. Deze functie is vooral handig in bedrijfs- en nalevingsgerichte instellingen waar verschillende belanghebbenden leerrecords moeten bekijken.

Na het downloaden van een Studenttranscript wordt op de pagina Studenttranscripten een lijst weergegeven met alle transcripten die door iedereen op het platform worden gegenereerd.



De lijst bevat de volgende kenmerken:

* Van en naar: Duur van de transcripten die moeten worden gedownload.
* Gegenereerd door: De e-mail van de gebruiker die het rapport heeft gedownload of om het downloaden heeft verzocht.
* Studenten: de studenten of studentengroepen waarvan de transcripten moeten worden gedownload.
* Toegepaste filters: de filters die zijn toegepast voor de inschrijvingsstatus.
* Extra gegevens inbegrepen: de extra gegevens (verwijderde studenten, informatie over de module, vaardigheidsgegevens en overzichtsbladen) die de beheerder had aangevraagd bij de optie Geavanceerd in het modale transcriptvenster Student toevoegen
* Status: gedownload, in de wachtrij geplaatst of actief.
* Annuleren: het genereren van het rapport op elk gewenst moment annuleren.

## Aanvullende overwegingen voor studenttranscripten

Studenttranscripten bevatten verschillende gedragingen die beheerders moeten onthouden:

**het Leren Weg en van de cursusvooruitgang vertoning**

Alle cursussen die deel uitmaken van een leerpad (LP) worden weergegeven in het Studenttranscript, zelfs als de student slechts in een van de cursussen voortgang heeft geboekt. Dit zorgt ervoor dat een leerpad volledig zichtbaar is, zelfs als de voortgang gedeeltelijk is voltooid.

**Gegevens voor geschrapte studenten**

Als een student uit het platform is verwijderd, worden zijn of haar records niet weergegeven in rapporten die zijn gegenereerd voor de gebruikersgroep waarvan hij of zij deel uitmaakte. Dit betekent dat de records van verwijderde studenten worden uitgesloten van gefilterde rapporten die zijn gemaakt met gebruikersgroepfilters.

U kunt echter wel de gegevens van de verwijderde studenten downloaden. Als u de optie **[!UICONTROL schrapte studenten]** terwijl het plaatsen van de filters voor het produceren van het rapport hebt geselecteerd omvat, kunt u het rapport voor de geschrapte studenten downloaden.



**Gedrag voor douanebeheerders**

Aangepaste beheerders met een gedefinieerd bereik (bijvoorbeeld beperkt tot specifieke catalogi of gebruikersgroepen) krijgen gefilterde transcriptgegevens te zien op basis van hun bereik:

* Bereik gebruikersgroep: Alleen studenten in de bereikbereikgroep van de aangepaste beheerder worden opgenomen in het rapport.
* Bereik van catalogus: Alleen leerobjecten (cursussen, certificeringen en leerpaden) die zijn toegewezen aan de bereikcatalogi, worden opgenomen in het rapport.
* Gefilterde kolommen: kolommen blijven hetzelfde. Alleen de rijen worden binnen het bereik geplaatst op basis van het bereik van catalogi en gebruikersgroepen.

Dit zorgt ervoor dat bereikbare aangepaste beheerders alleen de gegevens en leerinhoud van de student bekijken die ze mogen beheren.

**steun van de Verbindingsschakelaar**

Het rapport van het Transcriptie van de Student kan door beheerderGebruikersinterface, [ FTP, Doos, Baan API, of Power BI ](/help/migrated/integration-admin/feature-summary/connectors.md) worden betreden. Het is niet opgenomen in de geïntegreerde rapporten van Salesforce, Power BI en Marketo Engage.

Uniforme rapporten die zijn gedownload van Salesforce, Marketo Engage en Power BI bevatten minder kolommen dan Studenttranscripten.






