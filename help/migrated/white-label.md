---
jcr-language: en_us
title: API-implementaties in Adobe Learning Manager
description: Wit labelen is een praktijk waarbij u een app of service opnieuw brandt met uw eigen merk en deze aanpast alsof u de oorspronkelijke maker bent. In Adobe Learning Manager kunt u witte labels toepassen op de mobiele app, zodat u de app een nieuw merk kunt geven en de app onder uw eigen merk beschikbaar kunt maken voor uw gebruikers.
contentowner: saghosh
source-git-commit: 7bd9877aa32c78988a5195116d2a0f25ded05c90
workflow-type: tm+mt
source-wordcount: '1049'
ht-degree: 0%

---


# Witte labels in de mobiele app van Adobe learning Manager

De mobiele app van Adobe Learning Manager ondersteunt nu witte labels, wat betekent dat u de app nu onder uw eigen merknaam kunt uitbrengen.

## Hoe je begint met de voorbereidingen om je app met witlabel te starten

Voer de volgende stappen uit om uw eigen whitelabel app te distribueren en te beheren:

1. Bereid de middelen (bijvoorbeeld in het welkomstscherm) en de tekst voor, zodat beide kunnen worden gebruikt in de app en de beschrijving in de app/Play Store.

1. Wijs een technische bron toe die in staat is om:

* Het genereren van de certificaatbestanden voor pushmeldingen.
* Het ondertekenen van de binaire bestanden van de app die worden geleverd door het ALM-team.
* Het uploaden en beheren van het publicatieproces. Het publicatieproces vereist een communicatie tussen uw app-manager en de teams in de app/Play Store dat uw app voldoet aan alle publicatierichtlijnen. Van ALM ontvangt u een volledig compatibel binair bestand van een app.

## Overzicht

White labelen is een gewoonte waarbij u een nieuwe merknaam aan een app of service toegeeft aan uw eigen merk en deze aan te passen alsof u de oorspronkelijke maker bent. In Adobe Learning Manager kunt u whitelabels toepassen op de mobiele app, zodat u de app een nieuwe naam kunt wijzigen en de app onder uw eigen merk beschikbaar maken voor uw gebruikers.

## Wat kan worden aangepast

U kunt het volgende aanpassen:

### Velden

<table>

    <tbody>

    <tr>

   <td>

    <p>Account-id</p></td>

   <td>

    <p>De id van uw account. Let op: de witte gelabelde app is niet toegankelijk voor studenten die tot een ander account behoren.</p></td>

  </tr>

  <tr>

   <td>

    <p>Aanvullende account-id's</p></td>

   <td>

    <p>Voeg desgewenst meerdere accounts (subdomeinen) toe. Voeg de subdomeinen toe als komma's gescheiden zonder spaties. Bijvoorbeeld acc01,acc02,acc03 enzovoort.<br> <b>Opmerking:</b> U moet de account-id toevoegen wanneer u de subdomeinen opgeeft.</br> </p></td>

  </tr>

  <tr>

  <td>

  <p>Toepassingsnaam</p></td>

  <td>

  <p>De naam die u voor de app wilt gebruiken.</p></td>

  </tr>

  <tr>

  <td>

  <p>Korte naam app</p></td>

  <td>

  <p>Als de naam van de app lang is, geeft u de app een korte naam die op het apparaat wordt weergegeven.</p></td>

  </tr>

   <tr>

  <td>

  <p>Interne toepassingsnaam</p></td>

  <td>

  <p>De naam waarmee het besturingssysteem de app identificeert. Meestal wordt de volgende indeling gebruikt: com.company-name.product-name.</p></td>

  </tr>

  <tr>

  <td>

  <p>Interne toepassingsnaam-iOS</p></td>

  <td>

  <p>Geef de app een andere naam als uw gebruikers zich op iOS bevinden. We raden u aan dezelfde naam te gebruiken voor zowel iOS als Android.</p></td>

  </tr>

  <tr>

  <td>

  <p>App-pictogram</p></td>

  <td>

  <p>Het app-pictogram als png. Dit pictogram wordt weergegeven in uw app. De naamnotatie is account-id_appIcon.png.</p></td>

  </tr>

  <tr>

  <td>

  <p>App-welkomstscherm</p></td>

  <td>

  <p>Geef voor het welkomstscherm van uw app een afbeelding (png) op die wordt weergegeven wanneer uw gebruikers de app starten. De naamnotatie is account-id_splashIcon.png.</p></td>

  </tr>

  <tr>

  <td>

  <p>Client-id en clientgeheim</p></td>

  <td>

  <p>De integratiebeheerder van uw account geeft de gegevens op tijdens de registratie van de app. De integratiebeheerder moet het volgende gebruiken: * student:read,student:write als rol * interne app name://redirect as redirect URL

  </p></td>

  </tr>

  <tr>

  <td>

  <p>Accountlogo</p></td>

  <td>

  <p>De URL die het logo van uw organisatie host. Geef een link naar inhoud op als het accountlogo. De URL moet via webcodering worden gecodeerd.</p></td>

  </tr>

  <tr>

  <td>

  <p>App Store-id voor de app (iOS)</p></td>

  <td>

  <p>De id die is vereist voor het implementeren van de geforceerde update. De app moet weten dat de student moet worden omgeleid naar de App Store om de app bij te werken.</p></td>

  </tr>

   <tr>

  <td>

  <p>Google Play Store-id voor de app (Android)</p></td>

  <td>

  <p>De id die is vereist voor het implementeren van de geforceerde update.</p></td>

  </tr>

  <tr>

  <td>

  <p>Hostnaam voor deep linking</p></td>

  <td>

  <p>Gebruik Learningmanager om uw diepe koppelingen te hosten. Geef de URL van de host op als u een andere hostnaam-URL wilt gebruiken als een diepe koppeling. Bijvoorbeeld learningmanager.adobe.com.</p></td>

  </tr>

    </tbody>

</table>


#### Site-koppeling bijwerken

Als u een aangepast domein of leermanager als host gebruikt, hoeft u geen actie te ondernemen. Als u echter een aangepaste oplossing of een specifieke hostnaam voor de URL&#39;s gebruikt, voegt u de sitegekoppelde bestanden toe.

Raadpleeg de volgende koppelingen voor meer informatie:

- [Android](https://learningmanager.adobe.com/.well-known/assetlinks.json)

- [iOS](https://learningmanager.adobe.com/.well-known/apple-app-site-association)

## Certificaat voor pushmeldingen genereren

### Certificaat voor pushmeldingen op iOS

In de ontwikkeling van een iOS-app is een certificaat voor pushmeldingen een cryptografische referentie die door Apple is uitgegeven waarmee een server op een veilige manier pushmeldingen naar een iOS-apparaat kan verzenden via APN&#39;s (Apple Push Notification service).

Het certificaat zorgt voor een veilige communicatie tussen uw server (of provider) en Apple APNs bij het verzenden van pushberichten naar iOS-apparaten.

Zowel Android als iOS gebruiken Firebase Cloud Messaging (FCM) als service voor het verzenden van pushmeldingen naar apparaten.

### Het certificaat genereren op iOS

Volg de procedure:

1. Genereer of download de **Pushmeldingscertificaat** en persoonlijke sleutel (.p12). Raadpleeg het [Apple-document voor ontwikkelaars](https://developer.apple.com/documentation/usernotifications/setting_up_a_remote_notification_server/establishing_a_certificate-based_connection_to_apns) voor meer informatie.

1. Installeer het p12-bestand nadat het bestand is gedownload. Gebruik het wachtwoord om uw **Keychain-toegang** te installeren.

1. Navigeer naar **Mijn certificaten** en exporteer het certificaat. Zorg ervoor dat u het MIME-type selecteert .cer.

1. Zodra het p12-bestand en het cer-bestand beschikbaar zijn, voert u de volgende opdrachten uit:

```
- openssl pkcs12 -in privatekey.p12 -out myapnappkey.pem -nodes –clcerts

- openssl x509 -in privatekey.cer -inform DER -out myapnsappcert.pem 

- openssl s_client -connect gateway.sandbox.push.apple.com:2195 -cert myapnsappcert.pem -key myapnappkey.pem 
```

Als u verbinding kunt maken met de server, is het certificaat dat u hebt gemaakt geldig. Kopieer vanuit het bestand myapnappkey.pem het certificaat en de waarden van de persoonlijke sleutel.

1. Neem contact op met het CSM-team en ontvang de bestanden die zijn toegevoegd aan de SNS-services op AWS. Gebruikers moeten voor de pushmelding een vermelding ophalen die is geregistreerd in de SNS-service, waardoor ze de hierboven gegenereerde certificaten moeten delen voor validatie.

>[!NOTE]
>
>Voor Android moet de gebruiker de serversleutel opgeven van het Firebase-project dat ze voor Android hebben gemaakt om de vermelding in de SNS-service toe te voegen.


## Het project toevoegen aan Firebase

### Android

[Het project toevoegen](https://learn.microsoft.com/en-us/xamarin/android/data-cloud/google-messaging/firebase-cloud-messaging) in Firebase en haalt het ***google-services.json*** bestand.

### iOS

[Het project toevoegen](https://firebase.google.com/docs/ios/setup) naar Firebase en haalt de ***GoogleService-Info.plist*** bestand.

## De ondertekende binaire bestanden genereren

### iOS

```
sh""" xcodebuild -exportArchive -archivePath ./mobile-app-embedding-immersive/build/ios/archive/Runner.xcarchive -exportPath "ipa_path/" -exportOptionsPlist ./deviceAppBuildScripts/${ExportFile} 

mv ipa_path/*.ipa "${env.AppName}_signed.ipa" """ 
```

>[!NOTE]
>
>U hebt XCode 14.2 of hoger nodig om de ondertekende binaire bestanden te maken.


## Android

```
sh""" ~/Library/Android/sdk/build-tools/30.0.3/apksigner sign --ks $storeFile --ks-pass "pass:$store\_password" --ks-key-alias $key\_alias --key-pass "pass:$key\_password" --out app-release-signed.apk -v app-release.apk """
```

>[!NOTE]
>
>U hebt Android SDK-hulpprogramma&#39;s nodig om de ondertekende binaire bestanden te maken.

**Volgende stappen**

Nadat u de binaire bestanden hebt gegenereerd, drukt u de binaire bestanden naar de Play Store of App Store.

## Hoe pas ik de wijzigingen toe

Verzendt de vereiste middelen en bestanden naar het CSM-team. Het CSM-team vult vervolgens de [formulier](https://forms.office.com/r/bJRRaRBvSh) met de vereiste wijzigingen en voegt de vereiste elementen als bijlage toe. Het team zal dan de technische teams van de veranderingen evalueren en informeren. Het technische team genereert vervolgens een build en deelt deze met het CSM-team.

Het CSM-team zal de build met de klant delen.

## Wat kan niet worden aangepast

- Scherm Wachtwoord bijwerken
- Een accountscherm maken