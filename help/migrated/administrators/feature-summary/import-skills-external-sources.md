---
jcr-language: en_us
title: Vaardigheden importeren uit externe bronnen
description: Importeer Vaardigheden van contentproviders, zoals LinkedIn en Go1, met behulp van de respectievelijke connectoren.  De geïmporteerde vaardigheden worden toegevoegd aan de door de beheerder gedefinieerde vaardigheden in Leerbeheer en zijn beschikbaar voor auteurs tijdens de workflow voor het maken van de cursus.
contentowner: saghosh
exl-id: 3bcd8fc6-16e4-4f66-a5c6-15b3d606f0c2
source-git-commit: d96b25245daadaa0f5a330bcf8a7ab5bba995876
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 0%

---

# Vaardigheden importeren uit externe bronnen

Importeer Vaardigheden van contentproviders, zoals LinkedIn en Go1, met behulp van de respectievelijke connectoren. Deze verbetering maakt deel uit van de doelstelling van de Learning Manager om te integreren met externe Skills Clouds en Talent Management Systems. De geïmporteerde vaardigheden worden toegevoegd aan de door de beheerder gedefinieerde vaardigheden in Leerbeheer en zijn beschikbaar voor auteurs tijdens de workflow voor het maken van de cursus. Er zijn ook verbeteringen aangebracht in de zoekfunctionaliteit voor vaardigheden op het hele platform om een betere zoekervaring te bieden wanneer het account een groot aantal vaardigheden heeft.

## Vaardigheidsimport configureren

Voer de stappen in de procedure uit om het importeren van vaardigheden in het account mogelijk te maken.

1. In Admin app, selecteer **Montages** op de linkerruit.
1. Selecteer **Algemeen**.
1. In de **invoer van Vaardigheden** sectie, uitgezocht **laat** toe. Indien ingeschakeld kunt u een externe bron kiezen om vaardigheden te importeren. Als deze optie is ingeschakeld, worden de vaardigheden voor alle volgende importeerbewerkingen van leermiddelen geïmporteerd in de vaardigheidsopslagplaats voor nieuw geïmporteerde items. De vaardigheden voor bestaande leermiddelen kunnen één keer worden geïmporteerd in de vaardigheidsrepository en neem contact op met uw CSM om deze eerste run uit te voeren.
1. Selecteer een inhoudsprovider in de vervolgkeuzelijst.

Als beheerder kunt u vaardigheden slechts uit één vaardigheidsbron importeren.

### Standaardvaardigheidsniveau

Het standaardvaardigheidsniveau is één en Credit is 10 nadat de vaardigheden zijn gemigreerd.

U kunt de naam van de vaardigheid, beschrijving en niveaus toevoegen aan externe vaardigheden niet bewerken. U kunt echter wel domein, badges en credits toevoegen.

### Standaardcursusvaardigheden en studiepunten

Nadat u vaardigheden hebt geïmporteerd, worden deze toegevoegd aan de leermiddelen die uit de bron zijn geïmporteerd en die als vaardigheidsbron zijn geselecteerd. Als uw vaardigheidsbron bijvoorbeeld LinkedIn Learning was, zullen alle leermiddelen die uit LinkedIn Learning zijn geïmporteerd de vaardigheden hebben die door Learning worden geboden. Als elke leerbron wordt geïmporteerd in leermiddelen, krijgt deze standaard 10 studiepunten.

#### Rapportage

De kolom **Bron** met waarden - intern, LinkedIn Leren, Go1, die op de bron van vaardigheidsinvoer wijst.

De recent toegevoegde vaardigheden staan bovenaan.

Om de cursus plaatsende pagina, de kolom **Toegewezen door** bevattende waarden, Intern, en Leverancier van de Inhoud bevat.


## Workflow voor integratiebeheer

De integratiebeheerder uploadt de CSV&#39;s (vaardigheid, vaardigheidsniveau en cursus) en migreert de cursussen vervolgens naar het account. Nadat de beheerder bijvoorbeeld LinkedIn Learning heeft geselecteerd, kan de integratiebeheerder een activiteit plannen waarbij zowel vaardigheden als niveaus worden geïmporteerd naar Adobe Learning Manager.

## De vaardigheden exporteren

Als beheerder

1. Selecteer **Vaardigheden** op de linkerruit.
1. Selecteer de bron voor een vaardigheid. U kunt de cursussen, taakhulpen, ingeschreven studenten en docenten van de cursus bekijken.

### Vaardigheid bewerken

Selecteer een vaardigheid. In **geef een Vaardigheid** pop-up uit, kunt u niet de naam en de beschrijving van de vaardigheid uitgeven. U kunt echter vaardigheidsdomeinen en een badge voor de vaardigheid toevoegen.
