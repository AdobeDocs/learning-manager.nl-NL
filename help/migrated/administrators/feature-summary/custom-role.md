---
jcr-language: en_us
title: Aangepaste rollen
description: Met de functie Leerpaden kunt u aangepaste rollen definiëren en specifieke verantwoordelijkheden toewijzen aan een gebruikersset. Met deze functie kunt u verantwoordelijkheden toewijzen die buiten de bestaande rol van de persoon vallen.
contentowner: dvenkate
exl-id: dcc84f91-4e51-4ae2-b7cb-9eb29b398bc1
source-git-commit: 7c21986eff480f15cb788cf9a1cb51644bc083c8
workflow-type: tm+mt
source-wordcount: '3466'
ht-degree: 32%

---

# Aangepaste rollen

Met deze functie kunt u aangepaste rollen definiëren en specifieke verantwoordelijkheden toewijzen aan een gebruikersset. Met deze functie kunt u verantwoordelijkheden toewijzen die buiten de bestaande rol van de persoon vallen.

U kunt een aangepaste rol maken om auteursmogelijkheden te bieden die beperkt zijn tot een bepaalde catalogus. U kunt ook een rol maken voor rapportagebeheer. Dergelijke rollen kunnen dan worden toegewezen aan personen die geacht worden deze specifieke verantwoordelijkheden op zich te nemen.

>[!NOTE]
>
>Het toevoegen van een nieuwe aangepaste rol heeft geen invloed op bestaande aangepaste gebruikersgroepen of op op rollen gebaseerde groepen zoals Alle beheerders, Alle auteurs, enz.

Beheerders kunnen aangepaste beheerders- en aangepaste auteursrollen maken met op maat gemaakte machtigingen voor elke rol. Hieronder ziet u een overzicht van de machtigingen die aan elke rol zijn gekoppeld:

**Toestemmingen van de Rol van de Auteur van 0&rbrace;**

Aangepaste auteurs kunnen de volgende taken uitvoeren:

* Open de inhoudsbibliotheek om kerninhoud toe te voegen, te bewerken of te verwijderen.
* Maken, bewerken en verwijderen:
   * Cursussen
   * Taakhulpen
   * Certificeringen
   * Leerpaden
   * Leerplannen

Beheerders en auteurs, inclusief aangepaste beheerders en aangepaste auteurs, kunnen leerobjecten (LO&#39;s) delen met extern gedeelde catalogi. Beheerders en auteurs moeten kunnen zoeken naar extern gedeelde catalogi tijdens het maken van leerobjecten (LO&#39;s).

**de toestemmingen van de beheerderrol van de Douane**

De aangepaste beheerdersrol repliceert een reeks beheerdersverantwoordelijkheden, waaronder toegang tot bevoegdheden op accountniveau. Aangepaste beheerders krijgen machtigingen voor het beheer van belangrijke functies met betrekking tot leeractiviteiten, zoals:

* Leerplannen
* Catalogi
* Rapporten
* Tags

Bovendien kunnen aangepaste beheerders:

* Beheer cursussen en taakhulpen, waaronder gebruikers inschrijven en verwijderen.
* Creëer, bewerk en verwijder certificeringen, leerpaden en leerplannen.
* Toegang tot rapportage- en inschrijvingsfuncties voor alle leerobjecten (LO&#39;s).

Beheerders kunnen nu door CSV gemaakte machtigingen bekijken in Adobe Learning Manager. Met dit filter filtert u aangepaste rollen op beheerder die is gemaakt en op beheerders die via een CSV zijn geïmporteerd. Nadat u een aangepaste rol hebt geselecteerd, kunt u de bijbehorende machtigingen zien.

![](assets/filter.png)
_de douanerollen van de Filter_

## Een aangepaste rol maken {#create-role}

1. Meld u aan als beheerder. Open **[!UICONTROL Gebruikers]** > **[!UICONTROL Rol van de Douane]**.
2. Selecteer **[!UICONTROL creeer Rol]**. Het tabblad **[!UICONTROL Nieuwe rol maken]** wordt geopend.

   ![](assets/create-new-role.png)

   *creeer een douanerol*

3. Ga de naam in de **[!UICONTROL Naam van het gebied van de Rol]** in.
4. **[!UICONTROL de voorrechten van de Rekening]**: Deze voorrechten geven de roleigenaars toegang tot specifieke aspecten van de systeemconfiguratie en die op de volledige rekening handelen. Kies de toegangsrechten. De gebruiker krijgt volledige controle over de toegewezen rechten.

   Beheerders kunnen gedetailleerde machtigingen verlenen voor de sectie Gebruiker, die interne/externe gebruikers, gebruikersgroepen en geavanceerde gebruikers heeft.

   >[!NOTE]
   >
   >   Bereik is niet van toepassing op deze rechten.


   ![](assets/account-privileges.png)

   *plaats het werkingsgebied*

5. **de voorrechten van de Eigenschap - de eigenschappen van de Kern**: Gebruikt om toegang tot specifieke eigenschappen voor het beheren van het leren activiteiten te verlenen. Met deze optie kan toestemming worden gegeven voor de volgende functies.

   Beheerders kunnen gedetailleerde machtigingen voor de catalogi opgeven, zoals alleen-lezen, machtigingen voor de catalogi maken, bewerken en verwijderen.

   * Catalogi
   * Rapporten
   * Tags

   ![](assets/core-features.png)

   *plaats werkingsgebied voor Catalogi, Rapporten, en Markeringen*

6. **de voorrechten van de Eigenschap - het Leren Objecten:** gebruik deze optie om toegang tot verwante eigenschappen te verlenen LOs. Beheerders kunnen gedetailleerde machtigingen bieden voor alle leerobjecten, inclusief cursussen, leerpaden, certificeringen en taakhulpen. Ze kunnen gebruikersmachtigingen toewijzen, zoals maken, bewerken, verwijderen of alleen-lezen toegang.

   * Certificeringen
   * Cursussen
   * Taakhulpen
   * Leerprogramma&#39;s

   U kunt ook specifieke besturingselementen voor de leerobjecten toekennen. De toestemming kan een van de volgende zijn:

   * Alleen-lezen
   * Creëer
   * Bewerken
   * Verwijderen
   * Inschrijving
   * Rapport

   U kunt de LO&#39;s ook volledig besturen.

   ![](assets/learningobjects.png)

   *Verleen specifieke toestemmingen*

7. **Reikwijdte voor eigenschapvoorrechten:** het werkingsgebied van de voorrechten van de Eigenschap die aan deze rol worden toegewezen kan tot een specifieke Groep van de Gebruiker of één of meerdere Catalogi worden beperkt.

   Catalogi: gebruik het keuzerondje om controle te geven over **[!UICONTROL Alle catalogi]** of gebruik de optie **[!UICONTROL Toegang instellen per catalogus]** om toegang te bieden tot specifieke catalogi. U kunt ook meerdere catalogi selecteren.

   Gebruikersgroepen: verleen toegang tot **[!UICONTROL Alle gebruikersgroepen]** of gebruik de optie **[!UICONTROL Toegang instellen per gebruikersgroep]** om toegang te verlenen tot specifieke gebruikersgroepen. Er kan slechts één enkele gebruikersgroep worden opgegeven.

   >[!NOTE]
   >
   >Als u Aankondiging, Gamification, E-mailsjablonen, Vaardigheden en Gebruikers onder Accountbevoegdheden hebt geselecteerd, wordt de toegang tot de gebruikersgroep standaard aan alle gebruikersgroepen verleend en is deze optie uitgeschakeld.

   Als u leerplannen hebt geselecteerd onder Accountbevoegdheden, wordt standaard toegang tot alle catalogi en gebruikersgroepen verstrekt en zijn deze opties onder Omvang uitgeschakeld.

   ![](assets/define-scope-of-privileges.png)

   *bepaal werkingsgebied van voorrechten*

>[!NOTE]
>
>   In Learning Manager 27.6 kunt u een aangepaste rol voor meerdere catalogi instellen, waarbij aan elke catalogus verschillende machtigingen worden toegewezen.


Volg de onderstaande stappen om verschillende machtigingen aan de catalogi toe te wijzen:

1. Klik op de optie **[!UICONTROL Toegang instellen per catalogus]**.
1. Kies de catalogi om het machtigingenniveau voor elke catalogus zien. De machtigingen zijn als volgt:

   <table>
        <tbody>
        <tr>
          <td>
          <p><b>Machtiging</b></p></td>
          <td>
          <p><b>Beschrijving</b></p></td>
        </tr>
        <tr>
          <td>
          <p>Volledig beheer</p></td>
          <td>
          <p>Geeft Volledig beheer over alle leerobjecten. Machtigingen zijn onder andere Toevoegen, Bewerken, Verwijderen, Lezen, Inschrijven en Rapporteren.<br></p></td>
        </tr>
        <tr>
          <td>
          <p>Rapport</p></td>
          <td>
          <p>Geeft alleen toegang tot het tabblad Rapporten van het leerobject.</p></td>
        </tr>
        <tr>
          <td>
          <p>Inschrijven</p></td>
          <td>
          <p>Verleent machtigingen voor inschrijving voor het leerobject.</p></td>
        </tr>
        <tr>
          <td>
          <p>Alleen lezen</p></td>
          <td>
          <p>Verleent machtigingen waarmee leerobjecten in de catalogus alleen bekeken kunnen worden.</p></td>
        </tr>
        </tbody>
      </table>

1. Schakel de machtigingen in of uit afhankelijk van uw vereisten.
1. Klik op **[!UICONTROL Opslaan]** om de wijzigingen op te slaan. Klik vervolgens op **[!UICONTROL Opslaan]** om de wijzigingen voor de aangepaste rol op te slaan.

Kijk bijvoorbeeld eens naar het volgende scenario.

De resulterende machtiging die een aangepaste gebruiker voor een leerobject zou hebben, is een doorsnede van de leerobject- en catalogusmachtiging.

Een aangepaste gebruiker heeft Volledige machtiging voor cursussen en enkel Alleen lezen-toegang voor catalogus A, maar Volledige machtiging voor catalogus B. Het resultaat is Alleen lezen-toegang voor de cursussen van catalogus A en Volledig beheer over de cursussen van catalogus B.

Een gebruiker met een aangepaste rol kan:

* alleen inhoud bekijken van de catalogi waartoe hij/zij toegang heeft.
* Toegang tot elk leerobject op basis van de machtigingen van de catalogus waar het leerobject deel van uitmaakt.

  Als beheerder kunt u:

* meer dan een catalogus voor een aangepaste rol kiezen.
* de machtigingen van een catalogus op elk moment wijzigen.
* de catalogi verwijderen uit een bereik waarvoor u niet langer machtigingen wilt verlenen.
* een impliciete Alleen lezen-machtiging voor een catalogus verlenen, wanneer u machtigingen voor de catalogus verleent.

  De onderstaande tabel illustreert hoe de machtigingen worden verleend.

  <table>
    <tbody>
     <tr>
      <td>
       <p><strong> </strong></p></td>
      <td>
       <p><strong>Machtiging op catalogusniveau</strong></p></td>
     </tr>
     <tr>
      <td>
       <p><strong>Machtiging op leerobjectniveau</strong></p>
       <p><strong>(Bijv.: Cursussen)</strong></p></td>
      <td>
       <p>Volledig beheer</p></td>
      <td>
       <p>Inschrijven</p></td>
      <td>
       <p>Rapport</p></td>
      <td>
       <p>Alleen lezen</p></td>
     </tr>
     <tr>
      <td>
       <p>Volledig beheer</p></td>
      <td>
       <p>Volledig beheer</p></td>
      <td>
       <p>Inschrijven</p></td>
      <td>
       <p>Rapport</p></td>
      <td>
       <p>Alleen lezen</p></td>
     </tr>
     <tr>
      <td>
       <p>Inschrijven</p></td>
      <td>
       <p>Inschrijven</p></td>
      <td>
       <p>Inschrijven</p></td>
      <td>
       <p>Alleen lezen</p></td>
      <td>
       <p>Alleen lezen</p></td>
     </tr>
     <tr>
      <td>
       <p>Bewerken en verwijderen</p></td>
      <td>
       <p>Bewerken en verwijderen</p></td>
      <td>
       <p>Alleen lezen</p></td>
      <td>
       <p>Alleen lezen</p></td>
      <td>
       <p>Alleen lezen</p></td>
     </tr>
     <tr>
      <td>
       <p>Rapport</p></td>
      <td>
       <p>Rapport</p></td>
      <td>
       <p>Alleen lezen</p></td>
      <td>
       <p>Rapport</p></td>
      <td>
       <p>Alleen lezen</p></td>
     </tr>
    </tbody>
   </table>

1. **Gebruikers:** gebruik deze optie om te bepalen welke gebruikers deze rol toegewezen krijgen. U kunt een of meer gebruikers kiezen met behulp van het zoekvak.

   **voeg gebruikers aan de upload CSV van de douanerol toe:** om gebruikers via geüploade CSV toe te voegen, voeg een kolom CustomRole aan het .csv dossier toe dat de Beheerder gebruikte om gebruikers in te voeren. Voer de rol van de gebruiker onder de kolom CustomRole in voor de gebruikers aan wie u een aangepaste rol wilt toewijzen. Om het Csv- dossier te uploaden, klik **[!UICONTROL toevoegen > upload een CSV]**.

   * U kunt geen gebruikersgroepen zoeken.
   * U kunt niet zoeken naar gebruikers waaraan al een beheerdersrol is toegewezen.
   * Het toewijzen van een nieuwe aangepaste rol aan een gebruiker heeft voorrang op de vorige aangepaste rol van de gebruiker.

   <!--![](assets/users.png)-->

   * Een aangepaste beheerder met de machtiging Instellingen kan het schema configureren voor synchronisatie of synchronisatie van gebruikers vanuit de gegevensbron, zelfs als deze geen toestemming hebben voor de gebruikersentiteit.
   * Als een aangepaste beheerder machtigingen heeft voor de gebruikersentiteit, kunnen deze beheerder de rol van beheerder aan zichzelf toewijzen en een standaardbeheerder worden.

## Meerdere aangepaste rollen toewijzen aan een gebruiker

U kunt op de volgende manieren meerdere aangepaste rollen aan gebruikers toewijzen:

* UI gebruiken: U kunt meer dan één aangepaste rol rechtstreeks vanuit de Adobe Learning Manager-interface toewijzen aan een gebruiker.
* CSV-upload gebruiken: u kunt een CSV-bestand uploaden om meerdere aangepaste rollen tegelijk aan meerdere gebruikers toe te wijzen.

Hierdoor is het gemakkelijker om gebruikerstoegang en -machtigingen op het hele systeem te beheren.

### Meerdere aangepaste rollen toewijzen via de gebruikersinterface

Het toewijzen van meerdere aangepaste rollen via de Admin Console in Adobe Learning Manager is een snelle en intuïtieve optie die ideaal is voor onboarding, machtigingsaanpassingen of kleinere updates. Rollen kunnen visueel worden toegewezen, zonder dat CSV-uploads nodig zijn. Dit vermindert het risico op fouten en zorgt voor real-time zichtbaarheid. Deze methode ondersteunt snelle updates wanneer verantwoordelijkheden verschuiven en maakt het mogelijk om naar behoefte te schakelen tussen rollen en delegeren.

Ga als volgt te werk om meerdere aangepaste rollen aan een gebruiker toe te wijzen:

1. Login als beheerder en selecteer **[!UICONTROL Gebruikers]**.
2. Selecteer **[!UICONTROL de Rollen van de Douane]** op het linkerpaneel.
3. Maak een nieuwe aangepaste rol en voeg accountbevoegdheden, catalogi, leerobjecten of bereiken toe. Verwijs de vermelde stappen [ hier ](#create-a-custom-role).
4. Voeg gebruikers toe aan de aangepaste rol.

   ![](assets/add-users-in-custom-roles.png)
   _wijs gebruikers aan een douanerol toe_

5. Selecteer **[!UICONTROL Opslaan]**.

Selecteer desgewenst meerdere aangepaste rollen voor een gebruiker. Elke gebruiker kan maximaal 50 aangepaste roltoewijzingen hebben. Het aantal beschikbare rollen neemt bij elke toewijzing af.

Nadat u gebruikers hebt toegewezen aan een extra aangepaste rol, kunt u zien hoeveel roltoewijzingen beschikbaar blijven voor elke gebruiker.

>[!NOTE]
>
>U kunt maximaal 50 rollen aan elke gebruiker toewijzen en maximaal 500 gebruikers aan elke rol toevoegen.

### Meerdere aangepaste rollen toewijzen met behulp van CSV

Wanneer u een CSV-bestand in Adobe Learning Manager uploadt, kunt u op een efficiënte manier aangepaste rollen bulksgewijs toewijzen. Dit proces is met name gunstig voor het werven van een groot aantal werknemers, het reorganiseren van teams of het bijwerken van de toegang voor nieuwe training. CSV-import bespaart handmatige inspanningen, zorgt voor consistente toewijzingen en beperkt fouten. Deze methode is vooral handig bij fusies, afdelingwijde updates of algemene trainingstrajecten. Met deze methode kunnen beheerders tijd besparen, rollen standaardiseren en governance behouden.

U kunt nu via CSV-import meerdere rollen aan een gebruiker toewijzen door twee bestanden naar Box te uploaden:

* role.csv
* user_role.csv.

Het bestand user_role.csv bevat de velden Aangepaste rol en Gebruiker-id&#39;s.

Het bestand role.csv bevat de velden Aangepaste rol, Aanmaakbron en gedetailleerde informatie voor catalogi, gebruikers, cursussen, leerpaden en meer.

Als het CSV-bestand onjuiste gegevens heeft of de limiet overschrijdt (50 rollen per gebruiker en 500 gebruikers per rol), verschijnt er een bericht met de fouten.

![](assets/error-custom-role.png)
_Bericht van de Fout voor douanerollen_
Gebruikers ontvangen e-mailmeldingen wanneer rollen worden toegewezen, inclusief de naam van de rol.

### Aangepaste rollen beheren

Beheerders kunnen aangepaste rollen voor gebruikers in Adobe Learning Manager bijwerken, toevoegen of verwijderen als de verantwoordelijkheden veranderen. Hierdoor wordt de toegang afgestemd op de huidige rollen zonder dat dit van invloed is op de leergeschiedenis of inschrijvingsgegevens. Van de **[!UICONTROL pagina van Gebruikers]**, kan de beheerder naar gebruikers zoeken, hun rollen bekijken, en hen aanpassen gebruikend de Manage optie van de Rollen van de Douane. Met deze begeleide interface kunt u eenvoudig rollen toevoegen of verwijderen met behoud van governance en beveiliging.

>[!NOTE]
>
>Aangepaste beheerders kunnen geen aangepaste rollen beheren (aangepaste rol toevoegen of verwijderen) of zichzelf promoveren tot de beheerdersrol.

Nadat u douanerollen aan gebruikers toewijst, kunt u douanerollen toevoegen of verwijderen uit de **[!UICONTROL pagina van Gebruikers]**.

1. Zoek naar een gebruiker op de **[!UICONTROL pagina van Gebruikers]**.

   ![](assets/search-user-role.png)
   _Onderzoek naar een gebruiker in de pagina van Gebruikers_

2. Selecteer de drop-down pijl aan het eind van de rij waar de gebruikersnaam wordt getoond, en selecteer dan **[!UICONTROL leiden douanerollen]**.

   ![](assets/select-manage-custom-roles.png)
   _Uitgezochte beheert douanerollen in gebruikerspagina_

3. Er wordt een dialoogvenster weergegeven met de lijst met aangepaste rollen die aan de gebruiker zijn toegewezen. Selecteer **[!UICONTROL toevoegen/verwijderen rollen]** om douanerollen toe te voegen of te verwijderen die aan de gebruiker worden toegewezen.

   ![](assets/add-remove-roles.png)
   _Uitgezochte voeg/verwijder rollen in de Manage herinnering van de Rollen van de Douane toe_

4. Zoek naar andere aangepaste rollen die aan de gebruiker moeten worden toegewezen. Nadat u er een hebt gevonden, selecteert u de aangepaste rol.

   ![](assets/add-new-custom-role.png)
   _selecteer de douanerol_

5. Selecteer **[!UICONTROL sparen]**. Er verschijnt een bevestigingsvenster voor de wijziging in de aangepaste rol. Selecteer **[!UICONTROL ja]**.

   ![](assets/confirmation-prompt.png)
   _selecteer ja in de bevestigingsherinnering_

Een derde aangepaste rol wordt toegewezen aan de gebruiker.

Ga als volgt te werk om de aangepaste rollen te verwijderen:

1. Zoek naar een gebruiker op de **[!UICONTROL pagina van Gebruikers]**.
2. Selecteer dropdown dichtbij de gebruiker en selecteer **[!UICONTROL leiden douanerollen]**.
3. Selecteer **[!UICONTROL toevoegen/verwijderen rollen]** om douanerollen toe te voegen of te verwijderen.
4. Selecteer **[!UICONTROL verwijder pictogram]** om de douanerol te schrappen.

   ![](assets/remove-custom-roles.png)
   _verwijder douanerollen_

### Aangepaste rollen wisselen

Om om het even welke douanerollen te bekijken en te selecteren die aan u worden toegewezen, gebruik de **[!UICONTROL optie van de de douanerol van de Schakelaar]**.

![](assets/switch-roles.png)
_Uitgezochte douanerollen_

Gebruikers ontvangen e-mailmeldingen wanneer de aangepaste rollen aan hen zijn toegewezen. De e-mails bevatten nu rolnamen voor meer duidelijkheid.

## Het aangepaste rolrapport downloaden

Beheerders kunnen een CSV-rapport downloaden met alle aangepaste rollen en de bijbehorende machtigingen. Het rapport geeft aan of elke rol handmatig of via CSV-upload is gemaakt en geeft een overzicht van de toegangsrechten en bevoegdheden die aan elke rol zijn toegewezen.

Ga als volgt te werk om het rapport te downloaden:

1. Login als **[!UICONTROL Admin]**.
2. Selecteer **[!UICONTROL Gebruikers]** > **[!UICONTROL de Rollen van de Douane]**.
3. Selecteer de **[!UICONTROL optie van de Download]** om het CSV- rapport te downloaden.

![](assets/download-report.png)
_Rapport van de Download van douanerollen_

Het rapport heeft twee CSV-bestanden: role.csv en user_role.csv. Het bestand role.csv bevat:

* Aangepaste rol
* Gebruikers-id&#39;s
* Bron van ontwerp.

Het bestand user_role.csv bevat de velden, de aangepaste rol, de aanmaakbron en gedetailleerde informatie voor catalogi, gebruikers, cursussen, leerpaden en meer.

## Audittrail voor aangepaste rollen

Beheerders kunnen het controlerapport voor de aangepaste rol downloaden om alle wijzigingen te volgen die zijn aangebracht in de aangepaste rollen, zoals het maken, wijzigen en verwijderen van aangepaste rollen en de bijbehorende functietoegang.

Verwijs dit artikel [ spoor van de Controle voor douanerollen ](/help/migrated/administrators/feature-summary/reports.md#audit-trail-for-custom-roles) voor meer informatie.

## Toegang tot mappen beperken voor aangepaste auteurs {#folder-custom-author}

Leerbeheer ondersteunt al de mogelijkheid om toegang te verlenen tot de inhoudsbibliotheek met behulp van aangepaste rollen. Alle aangepaste auteurs die al toegang hebben tot de inhoudsbibliotheek, blijven toegang tot alle inhoudsbestanden hebben, zelfs nadat de inhoudsmappen zijn geconfigureerd. Zo kunnen ze verder met hun bestaand gedrag. Beheerders hoeven geen wijzigingen aan te brengen voor het geval ze het huidige gedrag willen blijven gebruiken.

Als beheerders de toegang tot deze aangepaste auteurs willen beperken, moeten ze de bestaande aangepaste rol bewerken en configureren door alleen toegang te bieden tot specifieke inhoudsmappen.

![](assets/folder-access-forcustomauthors.png)

*Toegang tot mappen beperken voor aangepaste auteurs*

Terwijl u een aangepaste auteur aanmaakt, kunt u nu inhoudsmappen aan de auteur toewijzen. Kies de optie **Geselecteerde Omslagen**.

Nadat u op de optie hebt geklikt, verschijnt een nieuw dialoogvenster waarin u de mappen aan de aangepaste auteur kunt toewijzen.

![](assets/choose-folder.png)

*selecteer de omslagen voor de douaneauteur*

Kies de omslagen en klik **[!UICONTROL OK]**.

## Leeroverzichtdashboard voor aangepaste beheerder {#custom-admin-dashboard}

Aangepaste beheerders kunnen dezelfde weergave zien als de beheerder. Een aangepaste beheerder kan gegevens buiten dit bereik plaatsen. Dit is alleen van toepassing als de aangepaste beheerder een volledig bereik heeft. Om volledig werkingsgebied te verlenen, terwijl het creëren van een douane admin, laat de optie **[!UICONTROL Volledige Controle]** in het Rapport van de Rekening toe.

![](assets/create-custom-role.png)

*creeer een douanerol*

Dientengevolge, zullen de opties, **[!UICONTROL Alle Catalogi]** en **[!UICONTROL Alle Gebruikersgroepen]** worden geselecteerd en de rest gehandicapt.

![](assets/scope-of-featureprivileges.png)

*bepaal werkingsgebied van voorrechten*

## Impliciete toestemmingen {#implicitpermissions}

Wanneer een gebruiker een rol krijgt toegewezen aan een specifieke entiteit, kunnen er gevallen zijn waarin hij/zij toegang moet hebben tot andere entiteiten om taken op de toegewezen entiteit te kunnen uitvoeren. Als een gebruiker bijvoorbeeld toegang tot Maken krijgt op cursusentiteit, hebben ze toegang nodig tot Vaardigheid- en Tag-entiteiten zodat ze deze kunnen koppelen aan de cursus die wordt gemaakt. Deze lijsten geven u informatie van dergelijke impliciete toestemmingen.

<table>
 <tbody>
  <tr>
   <th>Toegangstype</th>
   <th>Entiteitstoestemming verleend door de beheerder</th>
   <th>Impliciete entiteitstoestemming</th>
   <th>Impliciete toegang</th>
  </tr>
  <tr>
   <td>Beheer</td>
   <td>Gebruiker</td>
   <td>Groep</td>
   <td>Crud</td>
  </tr>
  <tr>
   <td>Inschrijven</td>
   <td>Alle IO’s (cursus, taakhulp, leerprogramma, certificering)</td>
   <td>Gebruiker <br>
     Leerplan</td>
   <td>Lees</td>
  </tr>
  <tr>
   <td>Creëer</td>
   <td>
    <p>Inhoudsgroep <br>
      Taakhulp<br></p></td>
   <td>Tag</td>
   <td>Lees</td>
  </tr>
  <tr>
   <td>Creëer</td>
   <td>Cursus</td>
   <td>Inhoudsgroep <br>
     Tag <br>
     Vaardigheid <br>
     Badge <br>
     Taakhulp</td>
   <td>Lees op alle</td>
  </tr>
  <tr>
   <td>Creëer</td>
   <td>Leerprogramma <br>
     Certificering<br></td>
   <td>Cursus <br>
     Tag <br>
     Vaardigheid <br>
     Badge</td>
   <td>Lees</td>
  </tr>
  <tr>
   <td>Creëer</td>
   <td>Leerplan</td>
   <td>Catalogus <br>
     Groep <br>
     Vaardigheid <br>
     Alle verliezen (cursus, taakhulp, leerprogramma, certificering)</td>
   <td>Lees</td>
  </tr>
  <tr>
   <td>Creëer</td>
   <td>Aankondiging</td>
   <td>Gebruiker <br>
     Groep <br>
     Alle verliezen (cursus, taakhulp, leerprogramma, certificering)</td>
   <td>Lees</td>
  </tr>
  <tr>
   <td>Creëer</td>
   <td>Gamification</td>
   <td>Branding</td>
   <td>Schrijven</td>
  </tr>
  <tr>
   <td>*</td>
   <td>Gebruiker</td>
   <td>Facturering</td>
   <td>Lees</td>
  </tr>
  <tr>
   <td>*</td>
   <td>Catalogus</td>
   <td>Groep <br>
     Alle verliezen (cursus, taakhulp, leerprogramma, certificering)</td>
   <td>Lees</td>
  </tr>
  <tr>
   <td>*</td>
   <td>Instelling</td>
   <td>Branding <br>
     Gebruiker</td>
   <td>Lees</td>
  </tr>
  <tr>
   <td>*</td>
   <td>Branding</td>
   <td>Instelling</td>
   <td>Lees</td>
  </tr>
  <tr>
   <td>*</td>
   <td>Facturering <br>
     Gamification</td>
   <td>Gebruiker</td>
   <td>Lees</td>
  </tr>
 </tbody>
</table>

## Toegang tot een aangepaste rol {#accessacustomrole}

Wanneer een beheerder een aangepaste rol toewijst, ontvangt u een e-mailbericht.

Opmerking: Als u al bent ingelogd bij Learning Manager onder een aangepaste rol, moet u zich opnieuw aanmelden bij Learning Manager om toegang te krijgen tot de nieuwe rol.

Klik in de rechterbovenhoek van Learning Manager op uw profielpictogram en selecteer de rol als u tussen rollen wilt schakelen.

## Bereik van leerprogramma’s op basis van rollen {#scopeconfigure}

In eerdere versies van Learning Manager kon elke Aangepaste rol met toestemming om leerprogramma&#39;s te maken de omvang van het leerprogramma voor alle typen gebruikersgroepen en Leerobjecten vaststellen.

De bereikinstelling werd eerst uitgeschakeld toen leerplantoegang werd verleend, waardoor de gebruiker standaard toegang had tot Alle catalogi en Alle gebruikersgroepen.

Alle leerplannen die door een beheerder zijn gemaakt, zijn standaard van toepassing op alle gebruikers. Gebruikers kunnen aan ieder leerobject worden toegewezen. Anderzijds hebben gebruikers met Aangepaste rollen toegang tot het volledige bereik, zoals Alle catalogi, Leerobjecten of Gebruikersgroepen. Dit betekende dat beheerders geen aangepaste rollen konden maken zoals verwacht en gebruikers met een beperkt bereik toegang tot leerplannen mochten krijgen.

Met deze update van Learning Manager kunt u Aangepaste rollen maken voor Leerprogramma&#39;s om het bereik van gebruikers en Leerobjecten vast te stellen. Met andere woorden, u kunt leerprogramma&#39;s maken met een beperkt bereik op basis van door de beheerder ingestelde rollen.

Een beheerder kan nu het bereik definiëren of beperken terwijl toegang tot het leerplanbeheer wordt verleend.

Aangepaste beheerders kunnen leerplannen maken met een beperkt bereik, dat wordt bepaald door het bereik van de configureerbare rol van de aangepaste beheerder. Dergelijke leerplannen zijn alleen toegankelijk voor aangepaste beheerders met dezelfde rol, maar zijn ook toegankelijk voor gewone beheerders. Bovendien kunnen aangepaste beheerders geen andere leerplannen in het account zien.

Bestaande aangepaste beheerders met toegang tot leerplannen hebben altijd het volledige bereik (per definitie). Ze hebben toegang tot alle leerplannen in het account, net als gewone beheerders. Nieuwe aangepaste rollen die met een volledig bereik zijn gemaakt en nieuwe aangepaste beheerders die aan dergelijke rollen zijn toegevoegd, blijven toegang tot alle leerplannen hebben.

De leerplannen die door de beheerder worden gemaakt en de beheerders van het volledige werkingsgebied zullen worden gecreeerd zoals gebruikelijk en zullen niet door werkingsgebied worden beperkt.

Geef in de sectie **Omvang van functiebevoegdheden** toegang tot Gebruikersgroepen en/of Catalogus voor de Aangepaste rol.

![](assets/scope-for-featureprivileges.png)

*toegang van de Verlening tot de Groepen van de Gebruiker en/of Catalogus voor de Rol van de Douane*

Een gebruiker toewijzen aan de aangepaste rol.

![](assets/assign-users-to-customrole.png)

*wijs een gebruiker aan een Rol van de Douane toe*

De gebruiker meldt zich nu aan bij Learning Manager als aangepaste beheerder en voegt nu een leerplan toe.

Wanneer een nieuwe student wordt toegevoegd, kan de aangepaste beheerder alleen een training selecteren uit de bereikcatalogi van de configureerbare rol.

Dit leerplan is nu alleen van toepassing op de student als de gebruiker ook wordt toegevoegd aan de groep binnen de bereikgroep van het leerplan. Alle andere studenten worden vrijgesteld van dit leerprogramma.

## Student wordt toegevoegd aan de groep {#learnergetsaddedtothegroup}

<!--![](assets/add-learner-to-thegroup.png)-->

De aangepaste beheerder kan elke gebruikersgroep selecteren die gebruikers heeft binnen de omvang van de gebruikersgroep van de rol.

Wanneer een gebruiker wordt toegevoegd aan de opgegeven groep, worden alleen gebruikers toegewezen aan het Leerobject die al onderdeel zijn van de omvang van de gebruikersgroep van het leerprogramma, en tevens aan de opgegeven gebruikersgroep zijn toegevoegd.

## Wijziging van omvang {#changeinscope}

Wanneer de beheerder het bereik van de aangepaste rol wijzigt, wordt de wijziging ook trapsgewijs doorgevoerd in de aangepaste beheerder. Wanneer de beheerder van de Douane een Leerplan kiest dat reeds bereikbaar was door een vorige douanerol, wordt een bericht getoond, zoals hieronder getoond:

![](assets/change-scope.png)

*Bericht na werkingsgebiedveranderingen*

De aangepaste beheerder moet nu het eerdere bereik bijwerken of vernieuwen naar het nieuwe bereik.

Klik op **[!UICONTROL Omvang vernieuwen]** om de omvang bij te werken. Er verschijnt een waarschuwingsbericht.

![](assets/refresh-scope-message.png)

*het bericht van de Waarschuwing na het vernieuwen van een werkingsgebied*

Klik op **[!UICONTROL Ja]** om de omvang bij te werken.

## Gamificationrapport toevoegen aan een aangepaste rol {#gamification-custom}

Een beheerder kan gamificationrapporten inschakelen voor een aangepaste gebruiker.

1. Voer op de pagina **[!UICONTROL Aangepaste rollen]** de naam van de aangepaste rol in.
1. In de **[!UICONTROL Privileges van de Eigenschap: De sectie van de Eigenschappen van de Kern]**, laat de optie **[!UICONTROL Volledige Controle]** voor de categorie **[!UICONTROL Rapporten]** toe.

1. Selecteer in de sectie **[!UICONTROL Gebruikers]** de gebruiker die wordt toegewezen aan de nieuwe aangepaste rol.
1. Klik op **[!UICONTROL Opslaan]**.

Wanneer een gebruiker het programma opent als beheerder van de Douane en **[!UICONTROL Rapporten]** op de linkerruit klikt, verschijnen de transcripten, zoals hieronder getoond:

![](assets/download-gamificationtranscripts.png)

*Download de gamificationtranscripten*

Klik op **[!UICONTROL Gamificationtranscripten]**, kies een gebruiker en genereer het rapport.

Als een beheerder de niveaupunten wijzigt, worden in de rapporten de niveaus weergegeven op basis van de huidige punten.

Wanneer u gamification opnieuw instelt, wordt de datum voor het bereikte niveau niet opnieuw ingesteld.

## Veelgestelde vragen {#frequentlyaskedquestions}

+++Een aangepaste rol maken?

Een aangepaste rol is als een subset van een auteurs- of beheerdersrol. Sta een of enkele privileges toe, definieer het bereik en wijs de rol toe aan een gebruiker.

Klik **[!UICONTROL Gebruikers]** > **[!UICONTROL de Rollen van de Douane]**. Klik op de pagina Aangepaste rollen op **[!UICONTROL Rol maken]**. Voer de naam van de aangepaste rol in en stel de bevoegdheden voor de rol in. Zie [Een aangepaste rol maken](custom-role.md#create-role) voor meer informatie.
+++

