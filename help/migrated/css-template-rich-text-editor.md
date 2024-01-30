---
jcr-language: en_us
title: CSS-sjabloon voor Rich Text Editor
description: CSS-sjabloon voor Rich Text Editor
contentowner: saghosh
preview: true
source-git-commit: 9325abb9cda8c8a019c9d72c1944a8284f38f83e
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 70%

---



# CSS-sjabloon voor Rich Text Editor

## Waarom is CSS vereist?

RTF-tekst bestaat uit HTML-opmaak. Als de opmaak wordt weergegeven zonder wijzigingen, past de browser de standaardstijl toe. Dit past vaak niet goed bij de stijlrichtlijnen van het bedrijf. Een CSS is dus vereist om te voldoen aan de richtlijnen.

## Standaardstijl

Het bijgevoegde CSS-opmaakmodel bevat de stijl die wordt toegepast door Learning Manager. De stijl is geoptimaliseerd met het oog op de meeste gebruiksgevallen. Download het bijgevoegde CSS-bestand en importeer het in uw web-app volgens uw conventies en systeem. De gedefinieerde CSS-klassen worden benoemd in de klasse ql-editor en veroorzaken geen problemen met uw bestaande stijlen.

## Stijl aanpassen

De standaardstijl werkt misschien niet voor iedereen. De stijl kan worden aangepast door de geleverde CSS te overschrijven. De stijlvormgeving staat in de wrapper onder ql-editor als afhankelijke opties. De volgende klassen worden gebruikt:

* **Inspringen**: li.ql-indent-$number. $nummer varieert van 1-9
* **grootte**: ql-size-small, ql-size-large, ql-size-large
* **uitlijning**: ql-align-center, ql-align-justify, ql-align-right
* **kleur**: ql-color-$color. $kleur = white (wit), red (rood), orange (oranje), yellow (geel), green (groen), blue (blauw), purple (paars)
* **achtergrond**: ql-bg-$color. $kleur = black (zwart), red (rood), orange (oranje), yellow (geel), green (groen), blue (blauw), purple (paars)
* **html-tags**: p, ol, ul, pre, blockquote, h1, h2, h3, h4, h5, h6

[Voor aanpassing te gebruiken CSS-bestand.](assets/ql-headless.css)
