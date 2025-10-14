---
description: Leer hoe te om de interfacetaal met SAML te vormen
jcr-language: en_us
title: Interface instellen via SAML
contentowner: chandrum
exl-id: 726cb45e-1c37-42b1-924a-565c84c82852
source-git-commit: 7b84a4565ccf109ed4789f4963d6e250f5d0a852
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 0%

---

# Interface instellen via SAML

Adobe Learning Manager (ALM) accepteert nu een SAML-kenmerk voor de taal. Dit kenmerk wordt vervolgens toegewezen aan de interface- en inhoudstaal-instellingen van de gebruiker, zodat de interactie met het LMS in de voorkeurstaal soepel verloopt. De configuratie van deze taalinstellingen wordt beheerd via het platform Identity and Access Management (IAM), dat SAML gebruikt voor Single Sign-On (SSO). Dit biedt ondersteuning voor door de Service Provider (SP) geïnitieerde aanmeldingen en IdP-aanmeldingen (Identity Provider), zodat gebruikers de interface en inhoud in hun gekozen taal kunnen zien. De workflow ziet er als volgt uit:

1. Toepassing maken in Okta
2. Een gebruiker toevoegen in Okta
3. SSO configureren in ALM

## Toepassing maken in Okta

Ga als volgt te werk om een toepassing te maken in Okta:

1. Maak een ontwikkelaarsaccount in Okta met behulp van de e-mail van uw bedrijf en meld u aan bij uw account.
2. Selecteer **[!UICONTROL Toepassingen]** > **[!UICONTROL creeer de Integratie van de Toepassing]**.
3. Selecteer **[!UICONTROL SAML 2.0]** en selecteer dan **[!UICONTROL daarna]**.
4. Typ een naam voor de toepassing en selecteer Volgende.
5. Configureer de volgende velden:

   * **[!UICONTROL Enige Sign-On URL]**: Type het specifieke domein URL waaraan u de toepassing wilt verbinden (bijvoorbeeld, [&#x200B; https://learningmanagerstage.adobe.com/saml/SSO &#x200B;](https://learningmanagerstage.adobe.com/saml/SSO)). Wijzig indien nodig de URL van de omgeving.
   * **[!UICONTROL Audience URI (identiteitskaart van de Entiteit van SP)]**: Gebruik het zelfde milieu URL zoals hierboven.
   * **[!UICONTROL Formaat van identiteitskaart van de Naam]**: Selecteer e-mailadres.
   * **[!UICONTROL Gebruikersnaam van de Toepassing]**: Selecteer Gebruikersbenaming Okta.

6. Voeg onder Kenmerkinstructies de volgende (of aanvullende velden indien nodig) toe:
   * **Naam**: scène
   * **Formaat van de Naam**: Onbepaald
   * **Waarde**: user.locale

7. Selecteer Volgende en vervolgens Voltooien.
8. Ga als volgt naar SAML Signing Certificates:

   * Vind de rij waar de status **[!UICONTROL Actief]** is.
   * Selecteer **[!UICONTROL Acties]** > **[!UICONTROL Meta-gegevens van de Mening IdP]**.
   * Hiermee wordt een XML-bestand op een nieuw tabblad geopend. Kopieer de XML-code en sla deze lokaal op als een .xml-bestand.

## Een gebruiker toevoegen in Okta

Ga als volgt te werk om een gebruiker in Okta te maken:

1. Selecteer **[!UICONTROL Folder]** > **[!UICONTROL Mensen]** en selecteer dan **[!UICONTROL Add Persoon]**.
2. Typ de noodzakelijke details voor de gebruiker en selecteer **[!UICONTROL sparen]**.
3. Zoek en selecteer de gebruikersnaam van de nieuwe gebruiker.
4. Selecteer **[!UICONTROL Wijs Toepassing]** toe.
5. Selecteer de toepassing u vroeger creeerde en selecteer dan **[!UICONTROL sparen]**.
6. Navigeer aan het profiel van de gebruiker en selecteer **[!UICONTROL uitgeven]**.
7. Op het scènegebied, typ de vereiste waarde (bijvoorbeeld, fr_FR, en_US) en selecteer **[!UICONTROL sparen]**.

## SSO configureren in ALM

Voer de volgende stappen uit om de SSO in ALM te configureren:

1. Meld u aan als beheerder.
2. Selecteer **[!UICONTROL Montages]** > **[!UICONTROL Login Methoden]**.
3. Ga naar de **[!UICONTROL Enige Sign-On (SSO) Configuratie]** tabel.
4. Selecteer **[!UICONTROL voeg nieuwe configuratie SSO]** toe.

   ![](assets/sso-add.PNG)
   _voeg sso in ALM_ toe

5. Configureer de volgende gegevens en selecteer Opslaan.
   * Typ een naam voor de configuratie.
   * Selecteer **[!UICONTROL IDP in werking gesteld]** van **[!UICONTROL Enige Sign-On (SSO) Montages]** dropdown.
   * Voor **[!UICONTROL IDP-In werking gestelde authentificatie URL]**:

      * Open het XML-metagegevensbestand dat u eerder hebt gedownload.
      * Zoek de locatiewaarde en kopieer deze.
      * Plak deze waarde in het veld Id-geïnitieerde verificatie-URL.

   * Voor **[!UICONTROL Dossier van XML van Meta-gegevens]**: Upload het .xml dossier u vroeger downloadde.

6. Ga terug naar de **[!UICONTROL Opstelling]** tabel.
7. Van dropdown, selecteer **[!UICONTROL Enige Sign-On Configuratie]**.
8. In het **dropdown van de Opstelling van 0&rbrace; SSO, selecteer de configuratienaam u vroeger creeerde.**
9. Selecteer **[!UICONTROL Opslaan]**.

## Gebruikersaanmelding en taalinstellingen

Wanneer een gebruiker zich aanmeldt met behulp van de referenties via SSO, wordt het taalkenmerk dat van de IDP is doorgegeven toegewezen aan de interface- en inhoudstaalvelden van de gebruiker in ALM. De taalinstellingen worden meteen weerspiegeld in de gebruikersinterface en de inhoud, zonder dat er tijd nodig is om de inhoud in cache te plaatsen.

Gebruikers kunnen hun taalinstellingen in de sectie Gebruikersprofiel handmatig bijwerken. Deze handmatig bijgewerkte taalvoorkeuren blijven van kracht en worden tijdens toekomstige aanmeldingen niet overschreven door de IDP-instellingen.

Als een gebruiker zacht uit ALM wordt verwijderd, blijven de taalinstellingen in de database behouden. Wanneer dezelfde gebruiker opnieuw wordt toegevoegd, wordt de eerder ingestelde taal hersteld.

Beheerders kunnen de gebruikersactiviteit-, leeroverzicht- en nalevingsdashboardrapporten controleren op taalspecifieke details.

## Voorkeursupdate voor gebruikerstaal bij aanmelding via SAML

Adobe Learning Manager is een meertalig platform dat de taalvoorkeuren van studenten op verschillende manieren ondersteunt, via de interface-, content- en cursusmodules, allemaal beschikbaar in meerdere talen.

Dankzij deze verbetering verbetert Adobe Learning Manager de just-in-time gebruikersprovisioning voor native platformgebruikers. Wanneer nieuwe gebruikers accounts maken en zich voor het eerst aanmelden, worden hun taalvoorkeuren nauwkeurig vastgelegd en automatisch toegepast.

### Belangrijkste voordelen

* Hiermee werkt u de taalvoorkeuren van gebruikers automatisch bij tijdens het aanmelden.
* Biedt een gepersonaliseerde ervaring door de interface en inhoud weer te geven in de voorkeurstaal van de gebruiker.
* Kan naadloos worden geïntegreerd met het SAML-verificatieproces.

Wanneer gebruikers zich via SAML aanmelden, wordt hun taalvoorkeur (interface- en inhoudstaal) gecontroleerd en bijgewerkt op basis van de informatie die tijdens het aanmeldingsproces wordt verstrekt.

De functie integreert met het SAML-aanmeldingsproces om de taalvoorkeur van de gebruiker naadloos vast te leggen en bij te werken.
