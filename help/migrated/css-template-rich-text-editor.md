---
jcr-language: en_us
title: CSS-sjabloon voor Rich Text Editor
description: CSS-sjabloon voor Rich Text Editor
contentowner: saghosh
preview: true
source-git-commit: 9325abb9cda8c8a019c9d72c1944a8284f38f83e
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---



# CSS-sjabloon voor Rich Text Editor

## Waarom is CSS vereist?

RTF-tekst bestaat uit HTML-opmaakcodes. Als de markering op de huidige manier wordt weergegeven, wordt de standaardstijl toegepast door de browser. Dit gaat vaak niet goed met de stijlrichtlijnen van het bedrijf. CSS is vereist om aan de richtlijnen te voldoen.

## Standaardstijl

De gekoppelde CSS-stijlpagina bevat de opmaak die wordt toegepast door Learning Manager. De stijl wordt getweend op basis van de meeste gebruikstoepassingen. Download het bijgevoegde CSS-bestand en importeer het naar uw webapp volgens uw conventies en buildsysteem. De gedefinieerde CSS-klassen worden benoemd in de klasse ql-editor en veroorzaken geen problemen met uw bestaande stijlen.

## Stijlen aanpassen

De standaardstijl voldoet mogelijk niet aan de behoeften van iedereen. U kunt de aanpassingen uitvoeren door de meegeleverde CSS te overschrijven. Alle stijlen worden onder de ql-editor geplaatst als afstammende kiezers. De volgende klassen worden gebruikt:

* **Inspringen**: li.ql-indent-$number. $getal varieert van 1-9
* **grootte**: ql-size-small, ql-size-large, ql-size-large
* **uitlijning**: ql-align-center, ql-align-justify, ql-align-right
* **kleur**: ql-color-$color. $color = wit, rood, oranje, geel, groen, blauw, paars
* **achtergrond**: ql-bg-$color. $color = zwart, rood, oranje, geel, groen, blauw, paars
* **html-tags**: p, ol, ul, pre, blockquote, h1, h2, h3, h4, h5, h6

[CSS-bestand voor aanpassing.](assets/ql-headless.css)
