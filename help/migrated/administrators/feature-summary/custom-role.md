---
jcr-language: en_us
title: Aangepaste rollen
description: Met de functie Leerpaden kunt u aangepaste rollen definiëren en specifieke verantwoordelijkheden toewijzen aan een gebruikersset. Met deze functie kunt u verantwoordelijkheden toewijzen die buiten de bestaande rol van de persoon vallen.
contentowner: dvenkate
exl-id: dcc84f91-4e51-4ae2-b7cb-9eb29b398bc1
source-git-commit: 3af4224f82f14342a298ce39088be874a2372817
workflow-type: tm+mt
source-wordcount: '2223'
ht-degree: 65%

---

# Aangepaste rollen

Met deze functie kunt u aangepaste rollen definiëren en specifieke verantwoordelijkheden toewijzen aan een gebruikersset. Met deze functie kunt u verantwoordelijkheden toewijzen die buiten de bestaande rol van de persoon vallen.

U kunt een aangepaste rol maken om auteursmogelijkheden te bieden die beperkt zijn tot een bepaalde catalogus. U kunt ook een rol maken voor rapportagebeheer. Dergelijke rollen kunnen dan worden toegewezen aan personen die geacht worden deze specifieke verantwoordelijkheden op zich te nemen.

## Een aangepaste rol maken {#create-role}

1. Meld u aan als beheerder. Openen **[!UICONTROL Gebruikers]** > **[!UICONTROL Aangepaste rol]**.
1. Selecteren **[!UICONTROL Rol maken]**. Het tabblad **[!UICONTROL Nieuwe rol maken]** wordt geopend.

   ![](assets/create-new-role.png)

   *Een aangepaste rol maken*

1. Voer de naam in het dialoogvenster **[!UICONTROL Naam van de rol]** veld.
1. **[!UICONTROL Accountbevoegdheden]**: Deze bevoegdheden geven de roleigenaars toegang tot specifieke aspecten van de systeemconfiguratie en die op het gehele account werken. Kies de toegangsrechten. De gebruiker krijgt volledige controle over de toegewezen rechten.

>[!NOTE]
>
>   Bereik is niet van toepassing op deze rechten.


![](assets/account-privileges.png)

*Bereik instellen*

1. **Functiebevoegdheden - Kernfuncties**: Wordt gebruikt om toegang te verlenen tot specifieke functies voor het beheer van leeractiviteiten. Met deze optie kan toestemming worden gegeven voor de volgende functies.

   * Catalogi
   * Rapporten
   * Tags

   ![](assets/core-features.png)

   *Bereik instellen voor catalogi, rapporten en tags*

1. **Functiebevoegdheden - Leerobjecten:**  Gebruik deze optie om toegang te verlenen tot functies die gerelateerd zijn aan LO&#39;s. U kunt toegang verlenen tot de volgende LO&#39;s.

   * Certificeringen
   * Cursussen
   * Taakhulpen
   * Leerprogramma&#39;s

   U kunt ook specifieke besturingselementen voor de LO&#39;s toekennen. De toestemming kan een van de volgende zijn:

   * Volledig beheer
   * Bewerken en verwijderen
   * Inschrijving
   * Rapport

   ![](assets/learning-objects.png)

   *Specifieke machtigingen verlenen*

1. **Bereik voor functiebevoegdheden:** Het bereik van de functiebevoegdheden die aan deze rol zijn toegewezen, kan worden beperkt tot een specifieke gebruikersgroep of een of meer catalogi.

   Catalogi: gebruik het keuzerondje om controle te geven over **[!UICONTROL Alle catalogi]** of gebruik de optie **[!UICONTROL Toegang instellen per catalogus]** om toegang te bieden tot specifieke catalogi. U kunt ook meerdere catalogi selecteren.

   Gebruikersgroepen: verleen toegang tot **[!UICONTROL Alle gebruikersgroepen]** of gebruik de optie **[!UICONTROL Toegang instellen per gebruikersgroep]** om toegang te verlenen tot specifieke gebruikersgroepen. Er kan slechts één enkele gebruikersgroep worden opgegeven.

   >[!NOTE]
   >
   >Als u Aankondiging, Gamification, E-mailsjablonen, Vaardigheden en Gebruikers onder Accountbevoegdheden hebt geselecteerd, wordt de toegang tot de gebruikersgroep standaard aan alle gebruikersgroepen verleend en is deze optie uitgeschakeld.

   Als u leerplannen hebt geselecteerd onder Accountbevoegdheden, wordt standaard toegang tot alle catalogi en gebruikersgroepen verstrekt en zijn deze opties onder Omvang uitgeschakeld.

   ![](assets/define-scope-of-privileges.png)

   *Omvang van rechten definiëren*

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

   **Gebruikers toevoegen aan CSV-upload met aangepaste rol:** Als u gebruikers via CSV-update wilt toevoegen, voegt u een kolom CustomRole toe aan het CSV-bestand dat de beheerder heeft gebruikt om gebruikers te importeren. Voer de rol van de gebruiker onder de kolom CustomRole in voor de gebruikers aan wie u een aangepaste rol wilt toewijzen. Klik op  **[!UICONTROL Toevoegen > Een CSV uploaden]**.

   CustomRole columnNote:

* U kunt geen gebruikersgroepen zoeken.
* U kunt geen gebruikers zoeken die al een beheerderrol toegewezen gekregen hebben.
* Het toewijzen van een nieuwe aangepaste rol aan een gebruiker heeft voorrang op de vorige aangepaste rol van de gebruiker.

  <!--![](assets/users.png)-->

* Een aangepaste beheerder met de machtiging Instellingen kan het schema configureren voor synchronisatie of synchronisatie van gebruikers vanuit de gegevensbron, zelfs als deze geen toestemming hebben voor de gebruikersentiteit.
* Als een aangepaste beheerder toestemming heeft voor de gebruikersentiteit, kan hij of zij zichzelf de rol van beheerder toewijzen en een standaardbeheerder worden.

## Toegang tot mappen beperken voor aangepaste auteurs {#folder-custom-author}

Leerbeheer ondersteunt al de mogelijkheid om toegang te verlenen tot de inhoudsbibliotheek met behulp van aangepaste rollen. Alle aangepaste auteurs die al toegang hebben tot de inhoudsbibliotheek, blijven toegang tot alle inhoudsbestanden hebben, zelfs nadat de inhoudsmappen zijn geconfigureerd. Zo kunnen ze verder met hun bestaand gedrag. Beheerders hoeven geen wijzigingen aan te brengen voor het geval ze het huidige gedrag willen blijven gebruiken.

Als beheerders de toegang tot deze aangepaste auteurs willen beperken, moeten ze de bestaande aangepaste rol bewerken en configureren door alleen toegang te bieden tot specifieke inhoudsmappen.

![](assets/folder-access-forcustomauthors.png)

*Toegang tot mappen beperken voor aangepaste auteurs*

Terwijl u een aangepaste auteur aanmaakt, kunt u nu inhoudsmappen aan de auteur toewijzen. Kies de optie **Geselecteerde mappen**.

Nadat u op de optie hebt geklikt, verschijnt een nieuw dialoogvenster waarin u de mappen aan de aangepaste auteur kunt toewijzen.

![](assets/choose-folder.png)

*Selecteer de mappen voor de aangepaste auteur*

Kies de mappen en klik op **[!UICONTROL OK]**.

## Dashboard met overzicht van leermateriaal voor aangepaste beheerder {#custom-admin-dashboard}

Aangepaste beheerders kunnen dezelfde weergave zien als de beheerder. Een aangepaste beheerder kan gegevens buiten dit bereik plaatsen. Dit is alleen van toepassing als de aangepaste beheerder een volledig bereik heeft. Als u een volledig bereik wilt toekennen terwijl u een aangepaste beheerder maakt, schakelt u de optie **[!UICONTROL Volledig beheer]** in het rapport Accountoverzicht.

![](assets/create-custom-role.png)

*Een aangepaste rol maken*

Als gevolg hiervan zijn de opties **[!UICONTROL Alle catalogi]** en **[!UICONTROL Alle gebruikersgroepen]** wordt geselecteerd en de rest wordt uitgeschakeld.

![](assets/scope-of-featureprivileges.png)

*Omvang van rechten definiëren*

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
   <td>Gebruiker<br>
     Leerplan</td>
   <td>Lees</td>
  </tr>
  <tr>
   <td>Creëer</td>
   <td>
    <p>Inhoudsgroep<br>
      Taakhulp<br></p></td>
   <td>Tag</td>
   <td>Lees</td>
  </tr>
  <tr>
   <td>Creëer</td>
   <td>Cursus</td>
   <td>Inhoudsgroep<br>
     Tag<br>
     Vaardigheid<br>
     Badge<br>
     Taakhulp</td>
   <td>Lees op alle</td>
  </tr>
  <tr>
   <td>Creëer</td>
   <td>Leerprogramma<br>
     Certificering<br></td>
   <td>Cursus<br>
     Tag<br>
     Vaardigheid<br>
     Badge</td>
   <td>Lees</td>
  </tr>
  <tr>
   <td>Creëer</td>
   <td>Leerplan</td>
   <td>Catalogus<br>
     Groep<br>
     Vaardigheid<br>
     Alle verliezen (cursus, taakhulp, leerprogramma, certificering)</td>
   <td>Lees</td>
  </tr>
  <tr>
   <td>Creëer</td>
   <td>Aankondiging</td>
   <td>Gebruiker<br>
     Groep<br>
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
   <td>Groep<br>
     Alle verliezen (cursus, taakhulp, leerprogramma, certificering)</td>
   <td>Lees</td>
  </tr>
  <tr>
   <td>*</td>
   <td>Instelling</td>
   <td>Branding<br>
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
   <td>Facturering<br>
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

Alle leerprogramma&#39;s die door een beheerder zijn gemaakt, zijn standaard van toepassing op alle gebruikers. Gebruikers kunnen aan ieder leerobject worden toegewezen. Anderzijds hebben gebruikers met Aangepaste rollen toegang tot het volledige bereik, zoals Alle catalogi, Leerobjecten of Gebruikersgroepen. Dit hield in dat beheerders niet zoals verwacht Aangepaste rollen konden maken om gebruikers met een beperkt bereik toegang te geven tot leerprogramma&#39;s.

Met deze update van Learning Manager kunt u Aangepaste rollen maken voor Leerprogramma&#39;s om het bereik van gebruikers en Leerobjecten vast te stellen. Met andere woorden, u kunt leerprogramma&#39;s maken met een beperkt bereik op basis van door de beheerder ingestelde rollen.

Een beheerder kan nu het bereik definiëren of beperken en tegelijkertijd toegang verlenen voor het beheer van leerprogramma&#39;s.

Aangepaste beheerders kunnen leerprogramma&#39;s met een beperkt bereik maken op basis van het bereik van de configureerbare rol van de aangepaste beheerder. Zulke leerprogramma&#39;s zijn alleen toegankelijk voor normale beheerders en aangepaste beheerders met dezelfde rol. Bovendien kunnen de aangepaste beheerders geen andere Leerprogramma&#39;s in het account zien.

Bestaande aangepaste beheerders met toegang tot Leerprogramma&#39;s hebben altijd het volledige bereik (standaard). Ze hebben toegang tot alle leerprogramma&#39;s in het account, net als normale beheerders. Nieuwe aangepaste rollen die met het volledige bereik zijn gemaakt en nieuwe aangepaste beheerders die aan dergelijke rollen zijn toegevoegd, houden toegang tot alle leerprogramma&#39;s.

Leerprogramma&#39;s die zijn gemaakt door beheerders en aangepaste beheerders met volledige omvang, worden zoals gewoonlijk gemaakt en zijn niet beperkt door de omvang.

Geef in de sectie **Omvang van functiebevoegdheden** toegang tot Gebruikersgroepen en/of Catalogus voor de Aangepaste rol.

![](assets/scope-for-featureprivileges.png)

*Toegang verlenen tot gebruikersgroepen en/of catalogus voor de aangepaste rol*

Een gebruiker toewijzen aan de aangepaste rol.

![](assets/assign-users-to-customrole.png)

*Een gebruiker toewijzen aan een aangepaste rol*

De gebruiker meldt zich nu aan bij Learning Manager als aangepaste beheerder en voegt een Leerprogramma toe.

Als er een nieuwe student wordt toegevoegd, kan de aangepaste beheerder alleen een training selecteren uit de omvang van de catalogi van de configureerbare rol.

Dit leerplan is nu alleen van toepassing op de student als de gebruiker ook wordt toegevoegd aan de groep binnen de bereikgroep van het leerplan. Alle andere studenten worden vrijgesteld van dit leerprogramma.

## Student wordt toegevoegd aan de groep {#learnergetsaddedtothegroup}

<!--![](assets/add-learner-to-thegroup.png)-->

De aangepaste beheerder kan elke gebruikersgroep selecteren die gebruikers heeft binnen de omvang van de gebruikersgroep van de rol.

Wanneer een gebruiker wordt toegevoegd aan de opgegeven groep, worden alleen gebruikers toegewezen aan het Leerobject die al onderdeel zijn van de omvang van de gebruikersgroep van het leerprogramma, en tevens aan de opgegeven gebruikersgroep zijn toegevoegd.

## Wijziging van omvang {#changeinscope}

Wanneer de beheerder de omvang van de aangepaste rol wijzigt, heeft deze wijziging ook gevolgen voor de aangepaste beheerder. Wanneer de aangepaste beheerder een Leerprogramma kiest dat al binnen de omvang van een eerdere aangepaste rol valt, wordt het volgende bericht weergegeven:

![](assets/change-scope.png)

*Bericht na bereikwijzigingen*

De aangepaste beheerder moet de eerdere omvang nu bijwerken of vernieuwen naar de nieuwe omvang.

Klik op **[!UICONTROL Omvang vernieuwen]** om de omvang bij te werken. Er verschijnt een waarschuwingsbericht.

![](assets/refresh-scope-message.png)

*Waarschuwingsbericht na vernieuwen van bereik*

Klik op **[!UICONTROL Ja]** om de omvang bij te werken.

## Gamificationrapport toevoegen aan een aangepaste rol {#gamification-custom}

Een beheerder kan gamificationrapporten inschakelen voor een aangepaste gebruiker.

1. Voer op de pagina **[!UICONTROL Aangepaste rollen]** de naam van de aangepaste rol in.
1. In het dialoogvenster **[!UICONTROL Functieprivileges: kernfuncties]** de optie **[!UICONTROL Volledig beheer]** voor de categorie **[!UICONTROL Rapporten]**.

1. Selecteer in de sectie **[!UICONTROL Gebruikers]** de gebruiker die wordt toegewezen aan de nieuwe aangepaste rol.
1. Klik op **[!UICONTROL Opslaan]**.

Wanneer een gebruiker zich als aangepaste beheerder aanmeldt en op **[!UICONTROL Rapporten]** in het linkerdeelvenster klikt, worden de transcripten als volgt weergegeven:

![](assets/download-gamificationtranscripts.png)

*De gamificationtranscripten downloaden*

Klik op **[!UICONTROL Gamificationtranscripten]**, kies een gebruiker en genereer het rapport.

Als een beheerder de niveaupunten wijzigt, worden in de rapporten de niveaus weergegeven op basis van de huidige punten.

Wanneer u gamification opnieuw instelt, wordt de datum voor het bereikte niveau niet opnieuw ingesteld.

## Veelgestelde vragen {#frequentlyaskedquestions}

+++Een aangepaste rol maken?

Een aangepaste rol is als een subset van een auteurs- of beheerdersrol. Sta een of enkele privileges toe, definieer het bereik en wijs de rol toe aan een gebruiker.

Klikken **[!UICONTROL Gebruikers]** > **[!UICONTROL Aangepaste rollen]**. Klik op de pagina Aangepaste rollen op **[!UICONTROL Rol maken]**. Voer de naam van de aangepaste rol in en stel de bevoegdheden voor de rol in. Zie [Een aangepaste rol maken](custom-role.md#create-role) voor meer informatie.
+++
