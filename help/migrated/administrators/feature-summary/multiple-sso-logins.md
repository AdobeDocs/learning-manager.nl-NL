---
description: Adobe Learning Manager ondersteunt meerdere aanmeldingsmethoden via meerdere SSO-configuraties voor zowel interne als externe gebruikers.
title: Meerdere SSO-aanmeldingen
contentowner: saghosh
source-git-commit: d59e748472c77527c22b286aea5412f776f6441b
workflow-type: tm+mt
source-wordcount: '782'
ht-degree: 0%

---


# Meerdere SSO-aanmeldingen {#multiple-sso-logins}

Een beheerder kan meerdere aanmeldingsmethoden configureren voor zowel interne als externe gebruikers. Adobe Learning Manager ondersteunt meerdere SSO-aanmeldingen waarmee beheerders de aanmeldingsmethode kunnen configureren op basis van hun behoeften en gebruiksscenario&#39;s.

De bedoeling is om beheerders toe te staan om verschillende SSO voor verschillende gebruikersgroepen te vormen die op hun plaats, organisatie, enz. worden gebaseerd.

U kunt maximaal 20 SSO-configuraties toevoegen aan een account. Deze kunnen worden gebruikt om SSO in te stellen voor zowel interne als externe gebruikers.

>[!NOTE]
>
>Als u multiSSO inschakelt, kunt u waarden of gebruikersgroepen kiezen in het zelfregistratieprofiel. Wanneer u een waarde kiest, wordt een gebruikersgroep met nul gebruikers gemaakt. Een dergelijke gebruikersgroep heeft geen gebruiker. Wanneer de volgende CSV wordt geïmporteerd, wordt deze gebruikersgroep verwijderd.

## Meerdere SSO&#39;s inschakelen

Selecteer **Instellingen** > **Aanmeldingsmethoden**.

Schakel op de installatiepagina het selectievakje &#39;Multiple Single Sign-On (SSO) inschakelen&#39; in voor interne of externe gebruikers.

Als Multi SSO is ingeschakeld, wordt de aanmeldingsmethode die is geselecteerd voor &#39;Standaardaanmeldingsmethode&#39; het standaardaanmeldingstype voor gebruikersgroepen/profielen die niet zijn gekoppeld aan een SSO-configuratie. De standaardaanmelding kan Adobe ID, SSO of ALM ID (Externe gebruikers) zijn.

Volg onderstaande stappen om een SSO te configureren:

1. Klik op SSO (Single Sign-On) configureren.
1. Klik op Nieuwe SSO-configuratie toevoegen.
1. Voeg het volgende toe in het dialoogvenster SSO-configuratie:

   * Voer de naam van de SSO in.
   * Selecteer het type SSO-IDP geïnitieerd, of SP geïnitieerd.

      * Als u IDP hebt geselecteerd in werking gesteld, dan ga IDP URL in. Dit is de URL die de unieke id voor uw toepassing zal zijn en die informatie is die wordt verstrekt door uw IDP-serviceprovider. Dit is de URL waarnaar alle gebruikers van de Adobe Learning Manager worden omgeleid nadat ze zich hebben aangemeld.
      * Upload de IDP-metagegevens-XML van uw IDP-provider. Dit bestand bevat informatie over de IdP waarmee Adobe Learning Manager SAML-beweringen kan accepteren
      * Als u SP hebt geselecteerd, ga identiteitskaart van de Entiteit in De entiteit-id is een URL die door de Serviceprovider (SP) wordt verschaft.
      * Voer de URL voor de SP-aanmelding in. Deze URL wordt door de gebruikers gebruikt om u aan te melden bij de toepassing.

1. De SSO-configuratie wordt toegevoegd aan de lijst.

## SSO instellen voor interne gebruikers

### Gebruikers van een CSV

Volg de onderstaande stappen:

1. Importeer de CSV die de actieve velden en de bijbehorende waarden bevat.
1. Klik op Instellingen > Aanmeldingsmethoden.
1. Schakel het selectievakje Meerdere eenmalige aanmelding (Single Sign-On, SSO) inschakelen in voor aanmelding.
1. Wijs de configuraties SSO aan de waarden van het actieve gebied toe.
1. Sla de instellingen op. Importeer de CSV opnieuw.

### Eén gebruiker

Volg de onderstaande stappen:

1. Klik op Instellingen > Aanmeldingsmethoden.
1. Schakel het selectievakje Meerdere eenmalige aanmelding (Single Sign-On, SSO) inschakelen in voor aanmelding.
1. Selecteer een actief veld voor een SSO.
1. Koppel de SSO-configuraties aan de waarden van het veld.
1. Sla de instellingen op. Voeg één gebruiker toe en wijs een waarde toe voor het actieve veld.

### Zelfgeregistreerde gebruikers

Volg de onderstaande stappen:

1. Klik op Instellingen > Aanmeldingsmethoden.
1. Schakel het selectievakje Meerdere eenmalige aanmelding (Single Sign-On, SSO) inschakelen in voor aanmelding.
1. Koppel de SSO-configuraties aan de waarden van het veld.
1. Sla de instellingen op. Voeg één gebruiker toe en wijs een waarde toe voor het actieve veld.
1. Voeg een zelfregistratieprofiel toe.
1. Selecteer een waarde voor het geconfigureerde SSO-veld.

Nadat u de profielinstellingen hebt opgeslagen, leidt de gekopieerde URL de gebruikers om naar de SSO die is gekoppeld aan de voor het profiel gekozen waarde.

### SSO instellen voor externe gebruikers

Volg de onderstaande stappen:

1. Maak een extern profiel.
1. Klik op Instellingen > Aanmeldingsmethoden.
1. Schakel het selectievakje Meerdere eenmalige aanmelding (Single Sign-On, SSO) inschakelen in voor aanmelding.
1. Koppel de SSO-configuratie aan het gemaakte externe profiel.
1. Sla de instellingen op.

Nadat u de profielinstellingen hebt opgeslagen, leidt de gekopieerde URL van het externe profiel de gebruikers om naar de SSO die aan het profiel is gekoppeld.

## Veelgestelde vragen

+++ Wie kan meerdere SSO&#39;s inschakelen voor gebruikers?

Zowel de beheerder als de aangepaste beheerder kunnen meerdere SSO&#39;s inschakelen.
+++

+++Kan ik een bestaand of een nieuw actief veld met één waarde gebruiken?

Ja, u kunt een bestaand of een nieuw enkel getaxeerd actief veld gebruiken om meerdere SSO&#39;s in te stellen.
+++

+++Als er uitgeschakelde velden in een CSV zijn, mislukt het instellen van meerdere SSO&#39;s?

Nee, het heeft geen invloed op de instelling van de SSO&#39;s. Gebruikers worden omgeleid naar een reeds geconfigureerde SSO.
+++

+++Kan een beheerder nieuwe waarden toevoegen aan het actieve veld op de pagina tijdens het instellen van de multi-SSO?

Ja, een beheerder kan nieuwe waarden toevoegen aan de actieve velden.
+++

+++Kan ik velden die gekoppeld zijn aan SSO uitschakelen of verwijderen?

Ja, u kunt velden die zijn gekoppeld aan de SSO uitschakelen of verwijderen totdat u de velden ontkoppelt van de instellingspagina van de SSO.
+++
