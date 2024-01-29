---
description: Beheerders kunnen een gepersonaliseerde sessie starten waarin ze zich kunnen aanmelden namens elke gebruiker in hun account in hun student- en managerrollen.
jcr-language: en_us
title: Imitatie van student en manager
contentowner: saghosh
source-git-commit: d59e748472c77527c22b286aea5412f776f6441b
workflow-type: tm+mt
source-wordcount: '538'
ht-degree: 0%

---



# Imitatie van student en manager {#impersonation-of-learner-and-manager}

In grote organisaties hebben medewerkers van de klantenondersteuning behoefte aan imitatiemogelijkheden om fouten op te sporen waarmee studenten worden geconfronteerd.

Dankzij deze mogelijkheid om zich voor te doen voor andere gebruikers, kunnen beheerders en aangepaste beheerders alle activiteiten van studenten en managers van hun organisatie identificeren en uitvoeren.

## Hoe werkt het?

Beheerders (en/of aangepaste beheerders) kunnen zoeken naar een gebruiker (intern of extern) en zich vervolgens als gebruiker manifesteren. De beheerder wordt vervolgens omgeleid naar de pagina van de gebruiker (indien van toepassing de beheerdersapp of een andere Learner-app) en meldt de beheerder vervolgens af van zijn sessie. De beheerder wordt vervolgens omgeleid naar de pagina Voltooien van uw profiel, voor het geval dat is ingesteld voor de gebruiker die door de beheerder is nagemaakt.

Als een aangepaste beheerder toestemming heeft om toegang te krijgen tot de pagina van een gebruiker, kunnen ze zoeken naar gebruikers die ze willen nadoen.

Houd rekening met het volgende wanneer u een gebruiker imiteert:

* Alle beheerders zien deze functie standaard.
* Alleen actieve gebruikers in het account kunnen worden nagemaakt.
* Een beheerder kan zichzelf niet imiteren.
* Een aangepaste beheerder die toegang heeft tot de pagina Gebruikers, kan zich als gebruikers gedragen.
* Een beheerder/aangepaste beheerder kan zich slechts 60 minuten imiteren.

## Een gebruiker personaliseren

Volg de onderstaande stappen om een gebruiker te imiteren:

1. Meld u als beheerder aan bij de app.
1. Selecteer Profiel > Gebruiker verpersoonlijken.

   U kunt zich per keer maar één gebruiker voorstellen.

1. Zoek naar een gebruiker (intern/extern) in het zoekvak dat aanwezig is in het modale venster. U kunt zich per keer maar één gebruiker voorstellen. Selecteer Doorgaan.

   U kunt ook zoeken met e-mail van de gebruiker, UUID, enzovoort.

1. Er wordt een bericht weergegeven met de bevestiging dat u zich als gebruiker zult gedragen.

   Selecteer Doorgaan.

   Een bevestigingsbericht, &quot;Imitatiemodus: U bent aangemeld als &quot;gebruikersnaam (e-mail van de gebruiker). Afmelden&quot; wordt weergegeven op de koptekst van de pagina.

**Een gepersonaliseerde sessie duurt 60 minuten.**

Wanneer u overschakelt naar een student- of managerrol, verschijnt een bericht waarin wordt aangegeven dat de beheerder/aangepaste beheerder zich in een imitatiemodus van de gebruiker bevindt.

## Aanmeldings- en toegangsrapport

De aanmelding en toegang van een beheerder worden vastgelegd in aanmeldings- en toegangsrapporten. Voor elke gebruiker die door de beheerder is nagemaakt, wordt in het rapport een record gemaakt.

De kolommen die deel uitmaken van deze functie zijn:

* Voorzien van een gebruikersnaam
* Gepersonaliseerd door e-mail van de gebruiker

Deze kolommen worden aan het einde van het rapport toegevoegd.

Elke aanmelding wordt afzonderlijk meegeteld in het rapport.

## Wat wordt niet ondersteund

* Imitatie van AEM componenten.
* Imitatie in de mobiele app.
* Imitatie in mobiele immersive.
* Imitatie van immersive Apps. Het is alleen van toepassing op ALM-apps.

## Veelgestelde vragen

+++Kan ik me aanmelden bij Adobe Learning Manager, zelfs als ik imiteer?

Ja, gebruikersaanmelding is onafhankelijk van imitatie.
+++

+++Zijn imitatiegebeurtenissen uniek geteld?

Ja, elke aanmeldingstoegang/elk bezoek van de beheerder tijdens de imitatie wordt apart geteld.
+++

+++Wat is de imitatietime-out?

Het is 60 minuten. Als een gebruiker die zich imiteert het browservenster sluit en binnen 60 minuten naar een prime-URL navigeert, wordt de imitatieactiviteit voortgezet en moet het bannerbericht worden weergegeven.
+++
