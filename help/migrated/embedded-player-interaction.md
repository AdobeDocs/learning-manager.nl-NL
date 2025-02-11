---
jcr-language: en_us
title: API-documentatie voor interactie ingesloten speler
description: Leer meer over verschillende API's om naar gebeurtenissen te luisteren en handelingen in de ingesloten speler te activeren
contentowner: chandrum
exl-id: 4734ecc1-cc8a-40b0-8997-32a31ec661ec
source-git-commit: 3d183dc40e4d1962d25160b74d8cf6cfa26e3171
workflow-type: tm+mt
source-wordcount: '833'
ht-degree: 69%

---

# API-documentatie voor interactie ingesloten speler

Adobe Learning Manager beschikt over een bibliotheek die kan worden geïntegreerd in een app. Deze bibliotheek biedt verschillende API&#39;s om gebeurtenissen te tracken en acties in de ingesloten speler te activeren.

Met de beschikbare API&#39;s kunt u afspelen, pauzeren en andere acties uitvoeren in de speler.

## De bibliotheek laden

U vindt de bibliotheek op deze [locatie](https://cpcontents.adobe.com/public/publiccdn/playerInteractionLib.min.js).

Volg de onderstaande stappen om de bibliotheek te laden:

1. Laad het JS-bestand in de toepassing voor consumenten.
2. Bij het laden van de bibliotheek wordt window.cpPlayerLib ingevuld.

>[!NOTE]
>
>Als u geen prod US gebruikt, stelt u de params cpPlayerLib.env en cpPlayerLib.sourceOrigin in op basis van uw env.

De standaardwaarden zijn:

* window.cpPlayerLib.env = [https://learningmanager.adobe.com/app/player](https://learningmanager.adobe.com/app/player);
* window.cpPlayerLib.sourceOrigin = &quot;[https://cpcontents.adobe.com](https://cpcontents.adobe.com/)&quot;;

### Beschikbare methoden

De cpPlayerLib-bibliotheek bestaat uit de volgende functies:

**startPlayer**

<table>
<tbody>
<tr>
<td>Naam methode</td>
<td>startPlayer</td>
</tr>
<tr>
<td>Beschrijving</td>
<td>Laadt een speler in de app.</td>
</tr>
<tr>
<td>Parameters</td>
<td><li>loId: de ID van het leerobject.</li><li>accountId: de account-ID van het ALM-account.</li><li>userId: de gebruikers-ID.</li><li>accessToken: het toegangstoken.</li><li>domRefId: de ID van de div-container waarin de speler moet worden weergegeven.</li><li>onModuleLoaded: deze functie wordt aangeroepen wanneer de modules met de onderstaande details worden geladen.</li><br><li>contentType</li><li>loID</li><li>moduleId</li><li>completed</li><li>currentLanguage</li><li>availableLanguages</li><li>isCCAvailable</li><li>ccEnabled</li></br></td>
</tr>
<tr>
<td>Resultaten</td>
<td>Geeft een belofte als resultaat. Bij het oplossen van de belofte wordt een playerObj doorgegeven.</td>
</tr>
<tr>
<td>Uitzondering</td>
<td>De belofte resulteert in een uitzondering.</td>
</tr>
<tr>
<td>Voorbeeldcode</td>
<td>cpPlayerLib.startPlayer(loId, accountId, userId, accessToken, domRefId, onModuleLoaded).then((playerObj) =&gt; {//playerObj heeft de API voor interactie met de speler}) &gt;</td>
</tr>
</tbody>
</table>

**getAllPlayers**

<table>
<tbody>
<tr>
<td>Naam van methode</td>
<td>getAllPlayers</td>
</tr>
<tr>
<td>Beschrijving</td>
<td>Retourneert alle spelerobjecten op de huidige pagina.</td>
</tr>
<tr>
<td>Parameters</td>
<td>Geen</td>
</tr>
</tr>
<tr>
<td>Voorbeeldcode</td>
<td>cpPlayerLib.getAllPlayers()</td>
</tr>
</tbody>
</table>

**getPlayer**


<table>
<tbody>
<tr>
<td>Naam van methode</td>
<td>getPlayer</td>
</tr>
<tr>
<td>Beschrijving</td>
<td>Retourneert een Player-object met de opgegeven leerobject-id.</td>
</tr>
<tr>
<td>Parameters</td>
<td><li>loId: de ID van het leerobject.</li></td>
</tr>
</tr>
<tr>
<td>Voorbeeldcode</td>
<td>cpPlayerLib.getPlayer(loId)</td>
</tr>
</tbody>
</table>

**navigateToModule**

<table>
<tbody>
<tr>
<td>Naam van methode</td>
<td>navigateToModule</td>
</tr>
<tr>
<td>Beschrijving</td>
<td>Navigeer naar de volgende module.</td>
</tr>
<tr>
<td>Parameters</td>
<td><li>moduleId: De module-id.</li></td>
</tr>
</tr>
<tr>
<td>Voorbeeldcode</td>
<td>playerObj.navigateToModule(moduleID)</td>
</tr>
</tbody>
</table>

**volgende**

<table>
<tbody>
<tr>
<td>Naam van methode</td>
<td>next</td>
</tr>
<tr>
<td>Beschrijving</td>
<td>Navigeer naar de volgende module.</td>
</tr>
<tr>
<td>Parameters</td>
<td><li>Geen</li></td>
</tr>
</tr>
<tr>
<td>Voorbeeldcode</td>
<td>playerObj.next()</td>
</tr>
</tbody>
</table>

**vorige**

<table>
<tbody>
<tr>
<td>Naam van methode</td>
<td>previous</td>
</tr>
<tr>
<td>Beschrijving</td>
<td>Navigeer naar de vorige module.</td>
</tr>
<tr>
<td>Parameters</td>
<td><li>Geen</li></td>
</tr>
</tr>
<tr>
<td>Voorbeeldcode</td>
<td>playerObj.previous()</td>
</tr>
</tbody>
</table>

**toggleTOC**

<table>
<tbody>
<tr>
<td>Naam van methode</td>
<td>toggleTOC</td>
</tr>
<tr>
<td>Beschrijving</td>
<td>Schakel het deelvenster met inhoudsopgave van de speler in.</td>
</tr>
<tr>
<td>Parameters</td>
<td><li>Geen</li></td>
</tr>
</tr>
<tr>
<td>Voorbeeldcode</td>
<td>playerObj.toggleTOC()</td>
</tr>
</tbody>
</table>

**toggleNotes**

<table>
<tbody>
<tr>
<td>Naam van methode</td>
<td>toggleNotes</td>
</tr>
<tr>
<td>Beschrijving</td>
<td>Schakel het deelvenster Notities van de speler in.</td>
</tr>
<tr>
<td>Parameters</td>
<td><li>Geen</li></td>
</tr>
</tr>
<tr>
<td>Voorbeeldcode</td>
<td>playerObj.toggleNotes()</td>
</tr>
</tbody>
</table>

**toggleClosedCaption**

<table>
<tbody>
<tr>
<td>Naam van methode</td>
<td>toggleClosedCaption</td>
</tr>
<tr>
<td>Beschrijving</td>
<td>Weergave van ondertiteling in- en uitschakelen op de speler.</td>
</tr>
<tr>
<td>Parameters</td>
<td><li>Geen</li></td>
</tr>
</tr>
<tr>
<td>Voorbeeldcode</td>
<td>playerObj.toggleClosedCaption()</td>
</tr>
</tbody>
</table>

**changeLanguage**

<table>
<tbody>
<tr>
<td>Naam van methode</td>
<td>changeLanguage</td>
</tr>
<tr>
<td>Beschrijving</td>
<td>Wijzig de taal van de inhoud op de speler.</td>
</tr>
<tr>
<td>Parameters</td>
<td><li>language: de taalcode die moet worden opgegeven.</li></td>
</tr>
</tr>
<tr>
<td>Voorbeeldcode</td>
<td>playerObj.changeLanguage("es")</td>
</tr>
</tbody>
</table>

**closePlayer**

<table>
<tbody>
<tr>
<td>Naam van methode</td>
<td>closePlayer</td>
</tr>
<tr>
<td>Beschrijving</td>
<td>Sluit de speler en verwijder de speler van de pagina. </td>
</tr>
<tr>
<td>Parameters</td>
<td><li>Geen</li></td>
</tr>
</tr>
<tr>
<td>Voorbeeldcode</td>
<td>playerObj.closePlayer()</td>
</tr>
</tbody>
</table>

**togglePlayPause**

<table>
<tbody>
<tr>
<td>Naam van methode</td>
<td>togglePlayPause</td>
</tr>
<tr>
<td>Beschrijving</td>
<td>Schakel tussen het afspelen en pauzeren van de inhoud op de speler.</td>
</tr>
<tr>
<td>Parameters</td>
<td><li>Geen</li></td>
</tr>
</tr>
<tr>
<td>Voorbeeldcode</td>
<td>playerObj.togglePlayPause()</td>
</tr>
</tbody>
</table>

**setVolume**

<table>
<tbody>
<tr>
<td>Naam van methode</td>
<td>setVolume</td>
</tr>
<tr>
<td>Beschrijving</td>
<td>Stel het volume van de speler in. De waarde moet tussen 0 en 1 liggen.</td>
</tr>
<tr>
<td>Parameters</td>
<td><li>volume: de waarde van het volume. Het geldige bereik is 0-1. </li></td>
</tr>
</tr>
<tr>
<td>Voorbeeldcode</td>
<td>playerObj.setVolume(0.5)</td>
</tr>
</tbody>
</table>

**setPlayBackSpeed**

<table>
<tbody>
<tr>
<td>Naam van methode</td>
<td>setPlayBackSpeed</td>
</tr>
<tr>
<td>Beschrijving</td>
<td>Stel de afspeelsnelheid in de speler in.</td>
</tr>
<tr>
<td>Parameters</td>
<td><li>speed: de waarde van de snelheid die moet worden opgegeven. Geldige waarden zijn 0,25, 0,5, 0,75, 1, 1,25, 1,5, 1,75, 2.</li></td>
</tr>
</tr>
<tr>
<td>Voorbeeldcode</td>
<td>playerObj.setPlayBackSpeed(1.25)</td>
</tr>
</tbody>
</table>

**zoek**

<table>
<tbody>
<tr>
<td>Naam van methode</td>
<td>seek</td>
</tr>
<tr>
<td>Beschrijving</td>
<td>Ga naar een willekeurig moment in de video.</td>
</tr>
<tr>
<td>Parameters</td>
<td><li>time: de tijd om naartoe te springen. De tijd wordt in seconden weergegeven.</li></td>
</tr>
</tr>
<tr>
<td>Voorbeeldcode</td>
<td>playerObj.seek(50)</td>
</tr>
</tbody>
</table>

**voorwaarts**

<table>
<tbody>
<tr>
<td>Naam van methode</td>
<td>forward</td>
</tr>
<tr>
<td>Beschrijving</td>
<td>Spring 10 seconden vooruit in de video.</td>
</tr>
<tr>
<td>Parameters</td>
<td><li>Geen</li></td>
</tr>
</tr>
<tr>
<td>Voorbeeldcode</td>
<td>playerObj.forward()</td>
</tr>
</tbody>
</table>

**achteruit**

<table>
<tbody>
<tr>
<td>Naam van methode</td>
<td>backward</td>
</tr>
<tr>
<td>Beschrijving</td>
<td>Spring 10 seconden terug in de video.</td>
</tr>
<tr>
<td>Parameters</td>
<td><li>Geen</li></td>
</tr>
</tr>
<tr>
<td>Voorbeeldcode</td>
<td>playerObj.backward()</td>
</tr>
</tbody>
</table>

**navigateToPage**

<table>
<tbody>
<tr>
<td>Naam van methode</td>
<td>navigateToPage</td>
</tr>
<tr>
<td>Beschrijving</td>
<td>Ga naar de opgegeven pagina op de PPT/PDF.</td>
</tr>
<tr>
<td>Parameters</td>
<td><li>pageNumber: Het paginanummer waar naartoe moet worden gegaan.</li></td>
</tr>
</tr>
<tr>
<td>Voorbeeldcode</td>
<td>playerObj.navigateToPage (5)</td>
</tr>
</tbody>
</table>

**nextPage**

<table>
<tbody>
<tr>
<td>Naam van methode</td>
<td>nextPage</td>
</tr>
<tr>
<td>Beschrijving</td>
<td>Ga naar de volgende pagina in de PPT/PDF.</td>
</tr>
<tr>
<td>Parameters</td>
<td><li>Geen</li></td>
</tr>
</tr>
<tr>
<td>Voorbeeldcode</td>
<td>playerObj.nextPage()</td>
</tr>
</tbody>
</table>

**previousPage**

<table>
<tbody>
<tr>
<td>Naam van methode</td>
<td>previousPage</td>
</tr>
<tr>
<td>Beschrijving</td>
<td>Ga naar de vorige pagina in de PPT/PDF.</td>
</tr>
<tr>
<td>Parameters</td>
<td><li>Geen</li></td>
</tr>
</tr>
<tr>
<td>Voorbeeldcode</td>
<td>playerObj.previousPage()</td>
</tr>
</tbody>
</table>

**zoomIn**

<table>
<tbody>
<tr>
<td>Naam van methode</td>
<td>zoomIn</td>
</tr>
<tr>
<td>Beschrijving</td>
<td>Zoom in op de inhoud van een PPT/PDF.</td>
</tr>
<tr>
<td>Parameters</td>
<td><li>Geen</li></td>
</tr>
</tr>
<tr>
<td>Voorbeeldcode</td>
<td>playerObj.zoomIn()</td>
</tr>
</tbody>
</table>

**zoomOut**

<table>
<tbody>
<tr>
<td>Naam van methode</td>
<td>zoomOut</td>
</tr>
<tr>
<td>Beschrijving</td>
<td>Zoom uit op de inhoud van een PPT/PDF.</td>
</tr>
<tr>
<td>Parameters</td>
<td><li>Geen</li></td>
</tr>
</tr>
<tr>
<td>Voorbeeldcode</td>
<td>playerObj.zoomOut()</td>
</tr>
</tbody>
</table>

**downloadJobAid**

<table>
<tbody>
<tr>
<td>Naam van methode</td>
<td>downloadJobAid</td>
</tr>
<tr>
<td>Beschrijving</td>
<td>Download een taakhulp van een cursus.</td>
</tr>
<tr>
<td>Parameters</td>
<td><li>Geen</li></td>
</tr>
</tr>
<tr>
<td>Voorbeeldcode</td>
<td>playerObj.downloadJobAid()</td>
</tr>
</tbody>
</table>

**toggleJobAidPullout**

<table>
<tbody>
<tr>
<td>Naam van methode</td>
<td>toggleJobAidPullout</td>
</tr>
<tr>
<td>Beschrijving</td>
<td>Of u een taakhulp wilt downloaden of niet.</td>
</tr>
<tr>
<td>Parameters</td>
<td><li>Geen</li></td>
</tr>
</tr>
<tr>
<td>Voorbeeldcode</td>
<td>playerObj.toggleJobAidPullout()</td>
</tr>
</tbody>
</table>

**fullScreen**

<table>
<tbody>
<tr>
<td>Naam van methode</td>
<td>fullScreen</td>
</tr>
<tr>
<td>Beschrijving</td>
<td>Stel de speler in op de modus Volledig scherm.</td>
</tr>
<tr>
<td>Parameters</td>
<td><li>Geen</li></td>
</tr>
</tr>
<tr>
<td>Voorbeeldcode</td>
<td>playerObj.fullScreen()</td>
</tr>
</tbody>
</table>

## Lijst met gebeurtenissen

**onPlayerEvents (callBack)**

Bij de registratie wordt de callback-functie aangeroepen voor alle spelergebeurtenissen. De namen van de gebeurtenissen zijn als volgt:

* PLAY (video/audio/CP)
* PAUSE (video/audio/CP)
* TIMEUPDATE (video/audio/CP)
* PAGECHANGE (PPT/PDF)
* NOTEADDED (alle inhoud)
* LAUNCHED (alle inhoud)
* STARTED (alle inhoud)
* COMPLETED (alle inhoud)
* PASSED (alle inhoud)
* FAILED (alle inhoud)

**onStreamingEvents (callBack)**

Bij de registratie wordt de callback-functie aangeroepen voor alle instructies van de speler die worden verzonden om de gebruikersactiviteit te volgen.
