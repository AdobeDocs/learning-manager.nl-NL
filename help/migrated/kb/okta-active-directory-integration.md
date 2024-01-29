---
jcr-language: en_us
title: Integratie van Okta Active Directory met Adobe Learning Manager
description: Integratie van Okta Active Directory met Adobe Learning Manager
contentowner: nluke
source-git-commit: 6abc118c6ad7e66e3ded5bd26b9167c3a0b99e4b
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 0%

---



# Integratie van Okta Active Directory met Adobe Learning Manager {#okta-active-directory-integration-with-adobe-learning-manager}

In dit document leert u hoe u Adobe Learning Manager kunt integreren met Okta Active Directory (AD). Wanneer u Adobe Learning Manager integreert met Okta AD, kunt u:

* Controleer en beheer de toegang van gebruikers van de Learning Manager in Okta AD.
* Laat gebruikers automatisch worden aangemeld bij de Adobe Leermanager met hun Okta AD-accounts.
* Beheer je accounts op één centrale locatie - het Okta-portaal.

Adobe Learning Manager ondersteunt Identity Provider (IdP) en Service Provider (SP) waarmee SSO is geïnitieerd.

## Een toepassing maken in OKTA

1. Meld u aan als beheerder op Okta AD.
1. Klikken **[!UICONTROL Toepassingen]**. Hierdoor wordt de toepassingswinkel in Okta geopend.

   ![](assets/cp-application-store.png)

   *Toepassingsarchief in Okta weergeven*

1. Klikken **[!UICONTROL App-integratie maken]**.

   ![](assets/cp-app-integrations.png)

   *Selecteer App-integratie maken*

1. Selecteren **[!UICONTROL SAML 2.0]** uit het nieuwe app-integratievenster.

   ![](assets/cp-saml2.0.png)

   *De optie SAML2.0 selecteren*

1. Selecteren **[!UICONTROL SAML-integratie maken]** > **[!UICONTROL Pagina Algemene instellingen]**. Voer een toepassingsnaam in.

   Let op: dit kan elke naam zijn om uw toepassing uniek te identificeren. Klik op **[!UICONTROL Volgende]**.

   ![](assets/cp-saml-integration.png)

   *Voer de naam van de toepassing in*

1. Voer de volgende stappen uit op de pagina SAML-instellingen configureren:

   **Voor IDP-instelling:**

   1. Typ de URL in het veld Single Sign-on URL: [https://learningmanager.adobe.com/saml/SSO](https://learningmanager.adobe.com/saml/SSO)
   1. Typ de URL in het veld Audience URL: [https://learningmanager.adobe.com](https://learningmanager.adobe.com/)
   1. In het dialoogvenster **Naam-id-indeling** vervolgkeuzelijst, selecteert u **E-mailadres**.
   1. In het dialoogvenster **Gebruikersnaam van toepassing** en selecteer Okta-gebruikersnaam.
   1. Als u aanvullende kenmerken wilt doorgeven, kunt u de kenmerken onder de **Instructie Attributen** (Optioneel)

   ![](assets/cp-saml-integration-step1.png)

   *SAML-kenmerken toevoegen*

   **Voor SP-instelling:**

   1. Typ de URL in het veld Single Sign-on URL: [https://learningmanager.adobe.com/saml/SSO](https://learningmanager.adobe.com/saml/SSO)
   1. Typ de URL in het veld Audience URL: [https://learningmanager.adobe.com](https://learningmanager.adobe.com/)
   1. Selecteer in de vervolgkeuzelijst Naam-id-indeling de optie **E-mailadres**.
   1. Selecteer in de vervolgkeuzelijst Gebruikersnaam de gebruikersnaam Okta-gebruikersnaam.
   1. Klik op **Geavanceerde instellingen tonen**.
   1. Onder **Handtekeningalgoritme**, selecteer RSA-SHA256
   1. In het dialoogvenster **Bevestigingsalgoritme**, selecteer SHA256
   1. In het dialoogvenster **Assertion Encryption** dropbox, selecteren **Gecodeerd**.

   1. In het dialoogvenster **Versleutelingscertificaat** uploadt u het certificaatbestand dat wordt gedeeld door de Adobe.
   1. Als u aanvullende kenmerken wilt doorgeven, kunt u de kenmerken onder de **Instructie Attributen** (Optioneel).

   ![](assets/cp-saml-integration-step2.png)

   *Extra kenmerken toevoegen*

   Klik op **[!UICONTROL Volgende]**.

1. De **Feedback**  is optioneel. Nadat u de opties hebt geselecteerd en feedback hebt gegeven, klikt u op **[!UICONTROL Voltooien]**.

   ![](assets/cp-saml-integration-step3.png)

   *Volledige SAML-installatie*

## Door IDP geïnitieerde URL- en metagegevensbestand extraheren

Voer de volgende stappen uit om het door IdP/SP geïnitieerde URL- en metagegevensbestand weer te geven:

1. Open de toepassing die u hebt gemaakt.
1. Onder de **Single Sign-On** tabblad, klikt u op **[!UICONTROL Instructies weergeven]**.

   ![](assets/cp-prime-sso.png)

   *Tabblad SSO selecteren*

   **Voor IDP:**

   1. De eenmalige aanmelding-URL van identiteitsprovider is de door IdP geïnitieerde URL.
   1. Kopieer alle tekst die aanwezig is onder de **Optioneel** veld.
   1. Open een nieuw notitieblokdocument en plak de gekopieerde tekst.
   1. Klikken **[!UICONTROL Bestand]** > **[!UICONTROL Opslaan als]** > &quot;filename.xml&quot;. Dit wordt het metagegevensbestand.

   **Voor SP:**

   1. De eenmalige aanmelding-URL van identiteitsprovider is de door IdP geïnitieerde URL.
   1. Uitgever van identiteitsprovider is de entiteit-id.
   1. Kopieer alle tekst die aanwezig is onder de **Optioneel** veld.
   1. Open een nieuw notitieblokdocument en plak de gekopieerde tekst.
   1. Klikken **[!UICONTROL Bestand]** > **[!UICONTROL Opslaan als]** > **[!UICONTROL filename.xml]**. Dit wordt het metagegevensbestand.

   ![](assets/cp-saml-integration-step4.png)

   *SP XML-bestand opslaan*

   U moet dit bestand opslaan in XML-indeling.

## SSO configureren voor Adobe Learning Manager

Om Adobe Learning Manager SSO te configureren, voert u de stappen uit die in het onderstaande artikel worden vermeld.

<!--

article not in TOC

[SSO Authentication](/help/migrated/kb/sso-authentication-for-learning-manager.md)
-->