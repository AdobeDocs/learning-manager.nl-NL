---
description: Beheerders kunnen een nabootsingssessie starten waar ze zich namens elke gebruiker kunnen aanmelden bij diens account in een student- of managerrol.
jcr-language: en_us
title: Een student en een manager nabootsen
contentowner: saghosh
source-git-commit: d59e748472c77527c22b286aea5412f776f6441b
workflow-type: tm+mt
source-wordcount: '538'
ht-degree: 71%

---



# Een student en een manager nabootsen {#impersonation-of-learner-and-manager}

In grote organisaties hebben medewerkers van de klantenondersteuning behoefte aan imitatiemogelijkheden om fouten op te sporen waarmee studenten worden geconfronteerd.

Met deze mogelijkheid om andere gebruikers na te bootsen kunnen beheerders en aangepaste beheerders alle activiteiten die studenten en managers van hun organisatie uitvoeren, identificeren en uitvoeren.

## Zo werkt het

Beheerders (en/of aangepaste beheerders) kunnen een gebruiker zoeken (intern of extern) en deze vervolgens nabootsen. De beheerder wordt vervolgens doorgeleid naar de gebruikerspagina (manager-app indien van toepassing, of anders student-app), en de beheerder wordt afgemeld bij de sessie. De beheerder wordt vervolgens doorgeleid naar de pagina Profiel voltooien, als dit is ingesteld voor de gebruiker die door de beheerder wordt nagebootst.

Als een aangepaste beheerder toestemming heeft om toegang te krijgen tot de pagina van een gebruiker, kunnen ze zoeken naar gebruikers die ze willen nadoen.

Houd rekening met het volgende wanneer u een gebruiker imiteert:

* Alle beheerders kunnen standaard deze functie zien.
* Alleen actieve gebruikers in het account kunnen worden nagebootst.
* Een beheerder kan niet zichzelf nabootsen.
* Een aangepaste beheerder met toegang tot de pagina Gebruikers kan gebruikers nabootsen.
* Een beheerder/aangepaste beheerder kan maximaal 60 minuten nabootsen.

## Een gebruiker nabootsen

Volg de onderstaande stappen om een gebruiker na te bootsen:

1. Meld u als beheerder aan bij de app.
1. Selecteer Profiel > Gebruiker verpersoonlijken.

   U kunt zich per keer maar één gebruiker voorstellen.

1. Zoek een gebruiker (intern/extern) in het zoekvak in het modale venster. U kunt slechts één gebruiker tegelijk nabootsen. Selecteer Doorgaan.

   U kunt ook zoeken met e-mail van de gebruiker, UUID, enzovoort.

1. Er verschijnt een bericht met de bevestiging dat u een gebruiker gaat nabootsen.

   Selecteer Doorgaan.

   Een bevestigingsbericht, &quot;Imitatiemodus: U bent aangemeld als &quot;gebruikersnaam (e-mail van de gebruiker). Afmelden&quot; wordt weergegeven op de koptekst van de pagina.

**Een gepersonaliseerde sessie duurt 60 minuten.**

Bij het wisselen naar een student- of managerrol wordt een bericht weergegeven dat de beheerder/aangepaste beheerder de gebruiker nabootst.

## Aanmelden en rapport openen

De aanmelding en toegang van een beheerder worden vastgelegd in aanmeldings- en toegangsrapporten. Voor elke gebruiker die door een beheerder wordt nagebootst, wordt in het rapport een record gemaakt.

De kolommen die bij deze functie horen:

* Nagebootst door gebruikersnaam
* Nagebootst door gebruikers-e-mail

Deze kolommen worden toegevoegd aan het eind van het rapport.

Elke aanmelding wordt in het rapport afzonderlijk geteld.

## Wat wordt niet ondersteund

* Nabootsing van AEM-onderdelen.
* Nabootsing in de mobiele app.
* Mobile Immersive-nabootsing.
* Nabootsing van immersieve apps. Dit geldt alleen voor ALM-apps.

## Veelgestelde vragen

+++Kan ik me aanmelden bij Adobe Learning Manager, zelfs als ik imiteer?

Ja, gebruikersaanmelding is onafhankelijk van imitatie.
+++

+++Zijn imitatiegebeurtenissen uniek geteld?

Ja, elke aanmeldingstoegang/bezoek van een beheerder als nabootsing wordt afzonderlijk geteld.
+++

+++Wat is de imitatietime-out?

Dat is 60 minuten. Als een nabootsende gebruiker het browservenster sluit en binnen 60 minuten naar een primaire URL gaat, wordt de nabootsingsactiviteit voortgezet en moet het bannerbericht worden getoond.
+++
