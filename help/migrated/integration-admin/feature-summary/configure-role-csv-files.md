---
jcr-language: en_us
title: Aangepaste rollen beheren via CSV-bestanden
description: De integratiebeheerder kan via CSV een aantal aangepaste rollen in bulk aan zijn/haar account toevoegen en hetzelfde aan verschillende gebruikers toewijzen. Deze aanpak automatiseert het maken van aangepaste rollen.
contentowner: saghosh
source-git-commit: ab6737e8b43222a6538921b0628a504a5f15859d
workflow-type: tm+mt
source-wordcount: '908'
ht-degree: 0%

---



# Aangepaste rollen beheren via CSV-bestanden

De integratiebeheerder kan via CSV een aantal aangepaste rollen in bulk aan zijn/haar account toevoegen en hetzelfde aan verschillende gebruikers toewijzen. Deze aanpak automatiseert het maken van aangepaste rollen.

U kunt rollen configureren via de Learning Manager FTP- en Box-connectoren.

Nadat u zich hebt aangemeld bij uw Box- of ExaVault-opslagaccount, kan de integratiebeheerder de volgende CSV&#39;s aan het account toevoegen:

* role.csv
* user_role.csv

Download de CSV&#39;s en wijzig de waarden volgens uw vereisten om aan de slag te gaan.

**role.csv**
[Voorbeeldbestand - role.csv](assets/role.csv) [Voorbeeldbestand- user_role.csv](assets/user-role.csv)

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
    <p>Rol in CSV identificeren die aan gebruikers moet worden toegewezen.</p></td>
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
    <p>De kolomnamen komen overeen met de namen van de entiteitstypen, zoals Catalogus, Cursus, Leerplan enz.</p>
    <p>Eén kolom voor elk type entiteit komt voor in de CSV. Entiteiten waarvoor geen toestemming wordt gegeven, moeten worden opgenomen met de waarde NONE</p></td>
  </tr>
  <tr>
   <td>
    <p>Catalogusbereikspecificatie</p></td>
   <td>
    <p>Naam van één catalogus of een door PIPE (|) gescheiden lijst met catalogusnamen die het bereik van deze rol bepalen.</p></td>
   <td>
    <p>Verkoopcatalogus | Algemene catalogus</p></td>
  </tr>
  <tr>
   <td>
    <p>Specifier voor Bereik gebruikersgroep</p></td>
   <td>
    <p>Naam en waarde van kenmerk Gebruikersgroep die het bereik bepalen van de gebruikers van deze rol.</p>
    <p>Zie de onderstaande sectie voor het bereik.</p></td>
   <td>
    <p>location=London</p></td>
  </tr>
  <tr>
   <td>
    <p>Beschrijving</p></td>
   <td>
    <p>Optionele gebruiksvriendelijke beschrijving om inzicht te krijgen in het doel van de rol en latere referentie.</p></td>
   <td>
    <p>Volledige auteurstoegang tot LO's in de verkoopcatalogus</p></td>
  </tr>
 </tbody>
</table>

Alle kolommen behalve Beschrijving zijn verplicht.

## Bereik van gebruikersgroepen definiëren {#definescopeofusergroups}

U kunt op de volgende manieren het bereik voor gebruikersgroepen voor verschillende soorten groepen opgeven:

* Naam gebruikersgroep zoals deze is (bijvoorbeeld Alle auteurs, Mijn aangepaste groep)
* Bladkenmerk en waarde (bijvoorbeeld Department=HR)
* Zelfregistratie profielgroepen (self_registration=profilename)
* Externe profielgroepen registratie (ext_registration=profilename)
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
    <p>E-mail-ID van de gebruiker waaraan een configureerbare rol moet worden toegewezen.</p></td>
   <td>
    <p>Als aan de gebruiker al een configureerbare rol is toegewezen, wordt de rol vervangen door een nieuwe rol die in de CSV is opgegeven. Er is geen fout gemeld.</p></td>
  </tr>
  <tr>
   <td>
    <p>CustomRole</p></td>
   <td>
    <p>Naam van de configureerbare rol die aan de gebruiker moet worden toegewezen</p></td>
   <td>
    <p>De rolnaam moet een bestaande rol zijn, zoals opgegeven in de CSV. Rollen die door de beheerder via de UI zijn gemaakt, kunnen hier worden gebruikt.</p></td>
  </tr>
 </tbody>
</table>

**Functies van het volledige bereik**

Wanneer Volledige machtiging is toegewezen voor een van de volgende functies (functies op accountniveau), worden Bereik gebruikersgroep en Catalogusbereik automatisch als VOLLEDIG beschouwd, omdat de gebruiker geen beperkte toegang tot deze functies kan hebben.

Als er catalogusnamen of gebruikersgroepnamen in de CSV staan, worden deze overschreven met de machtiging VOLLEDIG.

* Aankondigingen
* Vaardigheden
* Gamification
* Gebruikers
* Leerplannen
* E-mailsjablonen

## Voeg de rol-CSV&#39;s toe aan het account {#addtherolecsvsintheaccount}

Kies in uw Box-account de optie **Importeren > gebruiker > intern** en upload de bestanden role.csv en user_role.csv.

* De aangepaste CSV&#39;s moeten worden gekopieerd in de map &quot;import->user->internal->user_role&quot;
* De gebruikers-CSV moet worden gekopieerd in de map &quot;import->user->internal&quot;

Beide CSV&#39;s moeten alleen via Box of FTP worden geüpload en kunnen niet via UI worden geüpload.

>[!NOTE]
>
>Het CSV-bestand van Users is verplicht. De CSV&#39;s van de aangepaste rol zijn optioneel. Alle aanwezige bestanden worden verwerkt en andere worden overgeslagen.

De aangepaste rollen die zijn gemaakt met behulp van het CSV-bestand zijn niet zichtbaar voor beheerders in de UI. Deze rollen worden niet gerelateerd aan of beïnvloed door rollen die door de UI zijn gemaakt (of later zullen worden gemaakt).

Aangepaste rollen die door een CSV zijn gemaakt, kunnen volledig via de CSV zelf worden beheerd. Dit omvat het toevoegen, wijzigen en verwijderen van rollen.

Toegewezen rollen kunnen worden ingetrokken door toewijzingen te verwijderen uit user_role csv. Dit heeft echter geen invloed op toewijzingen die via de beheerdersinterface worden gedaan.

Werk de CSV-bestanden bij om een aangepaste rol toe te wijzen en in te trekken.

## Synchronisatie van aangepaste rollen {#synchronizationofcustomroles}

Nadat de integratiebeheerder de op rollen gebaseerde CSV&#39;s in de Connector-opslag heeft geüpload, kan de beheerder synchronisatie met de CSV&#39;s inschakelen. Telkens wanneer een aangepaste rol wordt bijgewerkt, toegevoegd of verwijderd in de CSV&#39;s, kan de beheerder de informatie in de bestanden synchroniseren en de lijst met rollen actueel maken.

Klik op de pagina Aan de slag in het deelvenster Beheerder op **[!UICONTROL Instellingen]** > **[!UICONTROL Gegevensbronnen]**.

Schakel in de sectie Instellingen synchroniseren de optie **[!UICONTROL Automatisch synchroniseren inschakelen]**.

![](assets/sync-settings.png)

*Selecteer de optie Automatisch synchroniseren inschakelen*

Wanneer u deze optie kiest, kunt u de synchronisatietijd plannen op het exacte tijdstip dat u opgeeft in het veld Synchronisatietijd. Als u de synchronisatietijd opgeeft als 12:00 uur, worden de aangepaste rollen elke dag precies op het opgegeven tijdstip bijgewerkt.

Als u de gegevens op verzoek wilt synchroniseren, klikt u op **[!UICONTROL Nu synchroniseren]**.

## Beperkingen tijdens het configureren van rollen {#constraintswhileconfiguringroles}

In elk account moet de naam van een rol uniek zijn. Een rol die via UI of CSV is gemaakt, mag daarom niet dezelfde naam hebben als een andere rol die al door UI of CSV is gemaakt.

Op dezelfde manier kan een gebruiker, vanuit de beheerinterface, geen configureerbare rol toegewezen krijgen die via CSV is gemaakt, omdat deze rollen niet beschikbaar zijn.

De gebruikerstoewijzing CSV kan echter worden gebruikt om rollen toe te wijzen die door de UI zijn gemaakt.
