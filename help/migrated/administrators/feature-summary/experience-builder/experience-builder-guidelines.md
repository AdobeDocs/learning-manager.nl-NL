---
title: Richtlijnen en beperkingen van Experience Builder in Adobe Learning Manager
description: Richtlijnen en beperkingen van Experience Builder bieden gepersonaliseerde cursus- en contentsuggesties aan studenten die AI-gedreven algoritmen gebruiken.
jcr-language: en-us
source-git-commit: b3124c47d56a50437cb284fe809828bcd4c4008d
workflow-type: tm+mt
source-wordcount: '796'
ht-degree: 0%

---


# Richtlijnen en beperkingen van Experience Builder

Experience Builder is een krachtige tool waarmee gebruikers eenvoudig dynamische en boeiende webpagina’s kunnen maken. Voor optimale prestaties, bruikbaarheid en beveiliging is het van essentieel belang dat u bepaalde richtlijnen en aanbevelingen opvolgt bij het configureren van pagina&#39;s, het gebruik van widgets en het aanpassen van lay-outs. Dit document biedt een gedetailleerd overzicht van belangrijke opmerkingen en punten die gebruikers moeten overwegen wanneer ze met Experience Builder werken.

De hier geschetste informatie bestrijkt belangrijke aspecten zoals pagina- en widgetconfiguraties, aanpassingsopties, het verwerken van aangepaste code en beveiligingsoverwegingen. Door aan deze aanbevelingen te voldoen, kunnen gebruikers de efficiëntie van hun Experience Builder-projecten maximaliseren, gemeenschappelijke valkuilen vermijden en zich naadloos aanpassen aan updates en wijzigingen.

## Configuratie van pagina en widget

### Maximum aantal pagina&#39;s

Je kunt maximaal 1000 pagina’s maken in Experience Builder. Dit is de bovengrens, maar het wordt geadviseerd om pagina&#39;s strategisch te plannen om onnodige ingewikkeldheid te vermijden.

### Widgets per pagina

* **Harde grens**: Een maximum van 25 widgets kan aan één enkele pagina worden toegevoegd.
* **geadviseerde grens**: Voor betere prestaties, wordt het geadviseerd om niet meer dan 10 widgets per pagina te gebruiken.
* **API-based widgets**: widgets afhankelijk van ALM APIs (b.v., Cursussen en wegen, Categorie, Mijn Leren, Sociaal Leren, Kalender, Naleving, Leaderboard) zouden tot 10 per pagina moeten worden beperkt.
* **Onafhankelijke widgets**: Widgets zoals de doos van de HTML en van de Inhoud, die niet op ALM APIs baseren, kunnen tot de harde grens van 25 widgets worden gebruikt.

### Widgets voor eenmalig gebruik

Bepaalde widgets, zoals agenda, Sociaal leren, Naleving en Leaderboard, mogen slechts eenmaal per pagina worden gebruikt. Als u deze meerdere keren gebruikt, kan dit leiden tot prestatieproblemen, met name voor widgets zoals de kalender. Voor het laden van sessies zijn veel bronnen nodig.

### Richtlijnen voor grootte van widgets

Widgets zoals Kalender, Leaderboard, Sociaal en Compatibiliteit moeten worden geplaatst in lay-outs met een minimale breedte van een derde van de pagina. Single Card-widgets zijn het meest geschikt voor deze breedte voor een optimale weergave. Widgets zoals de agenda en de uitgebreide weergave Naleving zijn ontworpen voor lay-outs van halve breedte om een betere gebruikerservaring te bieden. Voor andere layoutgrootten worden widgets responsief aangepast aan de beschikbare ruimte en blijven ze bruikbaar.

Het gebruik van widgets binnen deze aanbevolen grootterichtlijnen verbetert de algemene gebruikersinteractie.

## Richtlijnen voor aanpassing

### Standaardpixelafstanden

**Verticale afstand**: De standaard verticale afstand tussen widgets is 80 pixel.
**Horizontale afstand**: De standaard horizontale afstand tussen widgets is 20 pixel.

### Aangepaste CSS

Gebruikers kunnen standaardafstanden en andere visuele eigenschappen overschrijven met behulp van aangepaste CSS.

Stappen voor aanpassing:

* Inspect de pagina-elementen om CSS-klassen te identificeren.
* Wijzigingen toepassen op algemeen niveau, widgetniveau of paginaniveau.

Als u bijvoorbeeld de verticale afstand tussen widgets wilt verkleinen, wijzigt u de CSS-eigenschap voor de desbetreffende klasse.

## Menupositionering

U kunt menu&#39;s boven of links op de pagina plaatsen. Met aangepaste CSS kunnen verdere aanpassingen worden aangebracht.

## Functiespecifieke aanbevelingen

### Widgets Sociaal leren en Gamification

* Als deze functies zijn uitgeschakeld, moeten beheerders de overeenkomende widgets handmatig uit pagina&#39;s verwijderen.
* Pagina&#39;s moeten opnieuw worden ontworpen om ervoor te zorgen dat ze functioneel en visueel intact blijven nadat ze zijn uitgeschakeld.

## Aangepaste code verwerken

### Gevolgen van updates

* Bestaande aangepaste code (HTML, CSS, JS) die in de back-end wordt geïnjecteerd, werkt mogelijk niet zoals verwacht na updates van Experience Builder.
* Gebruikers moeten hun code herschrijven om deze uit te lijnen op nieuwe wijzigingen in de gebruikersinterface, zoals bijgewerkte klassennamen.

### Ondersteuning voor front-end

* Voeg rechtstreeks in de beheerportal aangepaste code toe met behulp van HTML-widgets of CSS/JS-blokken op accountniveau.

### Disclaimer

* Aangepaste code werkt mogelijk niet zoals verwacht bij toekomstige releases, waardoor aanpassingen nodig zijn. Bereid je voor om hun code na elke release bij te werken.

## Algemene aanbevelingen

### Prestatieoverwegingen

* Overschrijd de aanbevolen widgetlimieten niet om verslechtering van de prestaties te voorkomen.
* Het gebruik van bronintensieve widgets (bijvoorbeeld een kalender) meerdere keren op een pagina kan een aanzienlijke invloed hebben op de laadtijden van de pagina.

### Beveiligingsoverwegingen

* **widgets van de HTML**: U moet ervoor zorgen de de veiligheidskwesties van de codehandvatten zoals het dwars-plaats scripting (XSS) aanvallen, aangezien deze buiten het werkingsgebied van de controle van de Bouwer van de Ervaring zijn.
* **Douane footer**: Wanneer het aanpassen van footer gebruikend HTML of CSS, zorg ervoor dat de code aan veiligheid beste praktijken volgt.

### Wijzigingen verbreken

Updates voor Experience Builder kunnen baanbrekende wijzigingen voor aanpassingen introduceren. U moet:

* Pas de code aan aan de nieuwe UI-elementen.
* Test de aanpassingen na elke update.

## Aanvullende opmerkingen

### Aangepaste CSS-implementatie

* U kunt pagina-elementen inspecteren, CSS-klassen kopiëren en de gewenste eigenschappen ervan toepassen om layouts globaal, op widgetniveau of op paginaniveau aan te passen.

### Widget-id&#39;s en pagina-id&#39;s

Elke widget en pagina hebben unieke id&#39;s die kunnen worden gebruikt voor beoogde CSS-wijzigingen. Zo kunt u de instellingen op verschillende niveaus aanpassen:

* Algemeen niveau: CSS-wijzigingen toepassen op alle pagina&#39;s.
* Widgetniveau: CSS-wijzigingen toepassen op specifieke widgets.
* Paginaniveau: CSS-wijzigingen toepassen op alle widgets binnen een specifieke pagina.










