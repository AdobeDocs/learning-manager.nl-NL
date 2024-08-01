---
description: Adobe Learning Manager ondersteunt meerdere aanmeldingsmethoden via meerdere SSO-configuraties voor zowel interne als externe gebruikers.
title: Meerdere SSO-aanmeldingen
contentowner: saghosh
exl-id: 398816e8-a144-459b-8c39-6517ce4573b4
source-git-commit: 71bfc978c7ec58599c1f5c6afca6c082bc8b3569
workflow-type: tm+mt
source-wordcount: '782'
ht-degree: 39%

---

# Meerdere SSO-aanmeldingen {#multiple-sso-logins}

Een beheerder kan meerdere aanmeldingsmethoden via meerdere SSO-configuraties voor zowel interne als externe gebruikers configureren. Adobe Learning Manager ondersteunt meerdere SSO-aanmeldingen waarmee beheerders de aanmeldingsmethode kunnen configureren op basis van hun wensen en gebruiksscenario&#39;s.

De bedoeling is dat beheerders voor verschillende gebruikersgroepen een SSO kunnen configureren op basis van hun locatie, organisatie, enz.

Er kunnen tot 20 SSO-configuraties aan een account worden toegevoegd. Deze kunnen zowel voor het instellen van interne als externe gebruikers worden gebruikt.

>[!NOTE]
>
>Als u multiSSO inschakelt, kunt u waarden of gebruikersgroepen kiezen in het zelfregistratieprofiel. Wanneer u een waarde kiest, wordt een gebruikersgroep met nul gebruikers gemaakt. Een dergelijke gebruikersgroep heeft geen gebruiker. Wanneer de volgende CSV wordt geïmporteerd, wordt deze gebruikersgroep verwijderd.

## Meerdere SSO&#39;s inschakelen

Om veelvoudige SSO toe te laten, selecteer **Montages** > **Aanmeldingsmethodes**.

Schakel op de installatiepagina het selectievakje &#39;Multiple Single Sign-On (SSO) inschakelen&#39; in voor interne of externe gebruikers.

Als Multi SSO is ingeschakeld, wordt de aanmeldingsmethode die is geselecteerd voor &#39;Standaardaanmeldingsmethode&#39; het standaardaanmeldingstype voor gebruikersgroepen/profielen die niet zijn gekoppeld aan een SSO-configuratie. De standaard aanmelding kan Adobe ID of SSO of ALM ID (externe gebruikers) zijn.

Volg onderstaande stappen om een SSO te configureren:

1. Klik op SSO (Single Sign-On) configureren.
1. Klik op Nieuwe SSO-configuratie toevoegen.
1. Voeg in het dialoogvenster SSO-configuratie het volgende toe:

   * Geef de naam van de SSO op.
   * Selecteer het type SSO: Door IDP geïnitieerd of Door SP geïnitieerd.

      * Als u IDP hebt geselecteerd in werking gesteld, dan ga IDP URL in. Deze URL is de unieke identificatie voor uw applicatie en bevat informatie die door uw IDP-serviceprovider wordt geleverd. Dit is de URL waarnaar alle Adobe Learning Manager-gebruikers worden omgeleid nadat ze zich hebben aangemeld.
      * Upload de IDP-Metadata-xml van uw IDP-provider. Dit bestand bevat informatie over de IdP waardoor Adobe Learning Manager er SAML-beweringen uit kan accepteren
      * Als u SP hebt geselecteerd, ga identiteitskaart van de Entiteit in De entiteits-ID is een URL die de serviceprovider (SP) opgeeft.
      * Geef de SP-aanmeldings-URL op. Deze URL wordt door gebruikers gebruikt om zich aan te melden bij de applicatie.

1. De SSO-configuratie wordt toegevoegd aan de lijst.

## SSO instellen voor interne gebruikers

### Gebruikers uit een CSV

Volg onderstaande stappen:

1. Importeer de CSV die de actieve velden en de bijbehorende waarden bevat.
1. Klik op Instellingen > Aanmeldingsmethoden.
1. Selecteer **[!UICONTROL toelaten Meervoudig Enige Sign-On (SSO)]** voor login checkbox.
1. Wijs de configuraties SSO aan de waarden van het actieve gebied toe.
1. Sla de instellingen op. Importeer de CSV nogmaals.

### Eén gebruiker

Volg onderstaande stappen:

1. Klik op Instellingen > Aanmeldingsmethoden.
1. Selecteer **[!UICONTROL toelaten Meervoudig Enige Sign-On (SSO)]** voor login checkbox.
1. Selecteer een actief veld voor een SSO.
1. Koppel de SSO-configuraties aan de waarden van het veld.
1. Sla de instellingen op. Voeg één gebruiker toe en wijs een waarde toe voor het actieve veld.

### Zelfgeregistreerde gebruikers

Volg onderstaande stappen:

1. Klik op Instellingen > Aanmeldingsmethoden.
1. Selecteer **[!UICONTROL toelaten Meervoudig Enige Sign-On (SSO)]** voor login checkbox.
1. Koppel de SSO-configuraties aan de waarden van het veld.
1. Sla de instellingen op. Voeg één gebruiker toe en wijs een waarde toe voor het actieve veld.
1. Voeg een zelfregistratieprofiel toe.
1. Selecteer een waarde voor het geconfigureerde SSO-veld.

Nadat u de profielinstellingen hebt opgeslagen, leidt de gekopieerde URL de gebruikers om naar de SSO die is gekoppeld aan de voor het profiel gekozen waarde.

### SSO instellen voor externe gebruikers

Volg onderstaande stappen:

1. Maak een extern profiel.
1. Klik op Instellingen > Aanmeldingsmethoden.
1. Selecteer **[!UICONTROL toelaten Meervoudig Enige Sign-On (SSO)]** voor login checkbox.
1. Koppel de SSO-configuratie aan het gemaakte externe profiel.
1. Sla de instellingen op.

Nadat u de profielinstellingen hebt opgeslagen, leidt de gekopieerde URL van het externe profiel de gebruikers om naar de SSO die aan het profiel is gekoppeld.

## Veelgestelde vragen

+++ Wie kan meerdere SSO&#39;s inschakelen voor gebruikers?

Zowel de beheerder als de aangepaste beheerder kan meerdere SSO&#39;s inschakelen.
+++

+++Kan ik een bestaand of een nieuw actief veld met één waarde gebruiken?

Ja, u kunt een bestaand of nieuw actief veld met één waarde gebruiken om meerdere SSO&#39;s in te stellen.
+++

+++Als er uitgeschakelde velden in een CSV zijn, mislukt het instellen van meerdere SSO&#39;s?

Nee, dat heeft geen invloed op het instellen van de SSO&#39;s. Gebruikers worden doorgeleid naar een geconfigureerde SSO.
+++

+++Kan een beheerder nieuwe waarden toevoegen aan het actieve veld op de pagina tijdens het instellen van de multi-SSO?

Ja, een beheerder kan nieuwe waarden toevoegen aan de actieve velden.
+++

+++Kan ik velden die gekoppeld zijn aan SSO uitschakelen of verwijderen?

Ja, u kunt velden die zijn gekoppeld aan de SSO uitschakelen of verwijderen totdat u de velden ontkoppelt van de instellingspagina van de SSO.
+++
