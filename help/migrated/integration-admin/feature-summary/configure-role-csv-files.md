---
jcr-language: en_us
title: Aangepaste rollen via CSV-bestanden beheren
description: De integratiebeheerder kan via CSV een aantal aangepaste rollen in bulk aan zijn/haar account toevoegen en deze aan verschillende gebruikers toewijzen. Deze aanpak automatiseert het maken van aangepaste rollen.
contentowner: saghosh
exl-id: fce2f457-2834-491a-8331-64086f5a51b5
source-git-commit: f328076016d8c41455cad71f00d1dc9a1531e007
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 81%

---

# Aangepaste rollen via CSV-bestanden beheren

De integratiebeheerder kan via CSV een aantal aangepaste rollen in bulk aan zijn/haar account toevoegen en deze aan verschillende gebruikers toewijzen. Deze aanpak automatiseert het maken van aangepaste rollen.

U kunt rollen configureren via de Learning Manager FTP en Box-connectors.

Nadat u zich hebt aangemeld bij uw Box-opslagaccount, kan de integratiebeheerder de volgende CSV&#39;s toevoegen aan het account:

* user.csv
* role.csv
* user_role.csv

Download om te beginnen de CSV&#39;s en pas de waarden aan uw vereisten aan.

* Voorbeeldbestand: [role.csv](assets/role.csv)
* Voorbeeldbestand: [user_role.csv](assets/user_role.csv)

**role.csv**

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Kolomnaam</b></p></td>
   <td>
    <p><b>Beschrijving</b></p></td>
   <td>
    <p><b>Voorbeeldwaarden</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Naam</p></td>
   <td>
    <p>Geef een rol op binnen CSV om aan gebruikers toe te wijzen.</p></td>
   <td>
    <p>Verkoopauteur</p></td>
  </tr>
  <tr>
   <td>
    <p>&lt;Entity&gt;</p></td>
   <td>
    <p>Identificeer Toegangstype (VOLLEDIG, SCHRIJVEN, INSCHRIJVEN, RAPPORTEREN, GEEN) voor elk entiteitstype zoals CURSUS, CATALOGUS, enz.</p></td>
   <td>
    <p>VOLLEDIG</p>
    <p>GEEN</p>
    <p>SCHRIJVEN | RAPPORT</p>
    <p>De kolomnamen komen overeen met de namen van de entiteitstypen zoals Catalogus, Cursus, Leerplan enz.</p>
    <p>In de CSV verschijnt één kolom voor elk entiteittype. Entiteiten waarvoor geen toestemming moet worden gegeven, moeten worden opgenomen met de waarde NONE</p></td>
  </tr>
  <tr>
   <td>
    <p>Specificatie van catalogusbereik</p></td>
   <td>
    <p>Naam van één catalogus of door streepjes (PIPE (|)) gescheiden lijst van catalogusnamen die het bereik van deze rol bepalen.</p></td>
   <td>
    <p>Verkoopcatalogus | Algemene catalogus</p></td>
  </tr>
  <tr>
   <td>
    <p>Specifier voor Bereik gebruikersgroep</p></td>
   <td>
    <p>Naam en waarde kenmerk gebruikersgroep die het bereik van de gebruikers van deze rol bepalen.</p>
    <p>Zie de onderstaande sectie voor de bereiken.</p></td>
   <td>
    <p>locatie=Londen</p></td>
  </tr>
  <tr>
   <td>
    <p>Beschrijving</p></td>
   <td>
    <p>Optionele gebruiksvriendelijke beschrijving om het doel van de rol te verduidelijken en ter referentie.</p></td>
   <td>
    <p>Volledige auteurstoegang tot LO's in de verkoopcatalogus</p></td>
  </tr>
 </tbody>
</table>

Alle kolommen behalve Beschrijving zijn verplicht.

## Het bereik van gebruikersgroepen opgeven {#definescopeofusergroups}

U kunt op de volgende manieren het bereik voor gebruikersgroepen voor verschillende soorten groepen opgeven:

* Naam van de gebruikersgroep zoals deze is (bijvoorbeeld: Alle auteurs, Mijn aangepaste groep)
* Bladattribuut en waarde (bijvoorbeeld: Department=HR)
* Zelfregistratie profielgroepen (self_registration=profilename)
* Externe registratie profielgroepen (ext_registration=profilename)
* Het team van directe rapporteurs van een manager (manager_direct=`<emailid>`)
* De volledige organisatie van een manager (manager_org=`<emailid>`)

**user_role.csv**

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Kolomnaam</b></p></td>
   <td>
    <p><b>Beschrijving</b></p></td>
   <td>
    <p><b>Opmerking</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Id</p></td>
   <td>
    <p>E-mail-id van de gebruiker die aan een configureerbare rol moet worden toegewezen.</p></td>
   <td>
    <p>Als de gebruiker al aan een configureerbare rol is toegewezen, wordt de rol vervangen door een nieuwe rol die in de CSV is gespecificeerd. Er is geen fout gemeld.</p></td>
  </tr>
  <tr>
   <td>
    <p>Aangepaste rol</p></td>
   <td>
    <p>Naam van de configureerbare rol die aan de gebruiker moet worden toegewezen</p></td>
   <td>
    <p>De rolnaam moet een bestaande rol zijn, zoals gespecificeerd in de CSV. Rollen die via de UI door de beheerder zijn aangemaakt, kunnen hier worden gebruikt.</p></td>
  </tr>
 </tbody>
</table>

**Volledig bereik functies**

Telkens wanneer Volledige machtiging voor een van de volgende functies (functies op accountniveau) wordt verleend, worden Bereik gebruikersgroep en Catalogusbereik automatisch als VOLLEDIG beschouwd, omdat de gebruiker geen beperkte toegang tot deze functies kan hebben.

Als er Catalogusnamen of namen van Gebruikersgroepen in de CSV worden vermeld, worden deze met de machtiging VOLLEDIG overschreven.

* Aankondigingen
* Vaardigheden
* Gamification
* Gebruikers
* Leerplannen
* E-mailsjablonen

## De rol CSV&#39;s toevoegen aan het account {#addtherolecsvsintheaccount}

Kies in uw Box-account **Importeren > gebruiker > intern** en upload de bestanden role.csv en user_role.csv.

* De bestanden role.csv en user_role.csv moeten naar de map worden gekopieerd **Importeren** > **gebruiker** > **internal** > **user_role**.
* De user.csv moet in de map worden gekopieerd **Importeren** > **gebruiker** > **internal**.

Beide CSV&#39;s moeten alleen via Box worden geüpload en kunnen niet via UI worden geüpload.

>[!NOTE]
>
>Het CSV-bestand van Users is verplicht. De CSV&#39;s van de aangepaste rol zijn optioneel. Alle aanwezige bestanden worden verwerkt en andere worden overgeslagen.

De configuratierollen die met behulp van het CSV-bestand zijn gemaakt, zijn niet zichtbaar voor beheerders in de UI. Deze rollen worden niet gekoppeld aan of beïnvloed door rollen die zijn gemaakt (of later zullen worden gemaakt) door de UI.

Aangepaste rollen die door een CSV zijn gemaakt, kunnen volledig via de CSV zelf worden beheerd. Dit omvat het toevoegen, wijzigen en verwijderen van rollen.

Toegewezen rollen kunnen worden ingetrokken door toewijzingen uit user_role csv te verwijderen. Dit heeft geen invloed op toewijzingen vanuit de beheerinterface.

Werk de CSV-bestanden bij om een aangepaste rol toe te wijzen en in te trekken.

## Synchronisatie van aangepaste rollen {#synchronizationofcustomroles}

Nadat de integratiebeheerder de rolgebaseerde CSV&#39;s in de Connector-opslag heeft geüpload, kan de beheerder synchronisatie met de CSV&#39;s inschakelen. Telkens wanneer een aangepaste rol in de CSV&#39;s wordt bijgewerkt, toegevoegd of verwijderd, kan de beheerder de informatie in de bestanden synchroniseren en de lijst met rollen actueel maken.

Klik op de pagina Aan de slag in het deelvenster Beheerder op **[!UICONTROL Instellingen]** > **[!UICONTROL Gegevensbronnen]**.

Schakel in de sectie Synchronisatie-instellingen de optie **[!UICONTROL Automatisch synchroniseren inschakelen]** in.

![](assets/sync-settings.png)

*Selecteer de optie Automatisch synchroniseren inschakelen*

Wanneer u deze optie kiest, kunt u de synchronisatie laten uitvoeren op het exacte tijdstip dat u in het veld Synchronisatietijd opgeeft. Als u de synchronisatietijd opgeeft als 12:00 uur, worden de aangepaste rollen elke dag precies op dat tijdstip bijgewerkt.

Als u de gegevens op verzoek wilt synchroniseren, klikt u op **[!UICONTROL Nu synchroniseren]**.

## Beperkingen tijdens het configureren van rollen {#constraintswhileconfiguringroles}

In elk account moet de naam van een rol uniek zijn. Een rol die via UI of CSV wordt gemaakt, mag dus niet dezelfde naam hebben als een andere rol die al via UI of CSV is gemaakt.

Het is ook niet mogelijk een configureerbare rol die via CSV is gemaakt, aan een gebruiker toe te wijzen via de beheerinterface, omdat deze rollen niet beschikbaar zijn.

Het gebruikerstoewijzings-CSV kan echter wel worden gebruikt om rollen toe te wijzen die door de UI zijn gemaakt.
