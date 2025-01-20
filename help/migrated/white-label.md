---
jcr-language: en_us
title: Witte labels in de mobiele app van Adobe learning Manager
description: Wit labelen is een praktijk waarbij u een app of service opnieuw brandt met uw eigen merk en deze aanpast alsof u de oorspronkelijke maker bent. In Adobe Learning Manager kunt u witte labels toepassen op de mobiele app, zodat u de app een nieuw merk kunt geven en de app onder uw eigen merk beschikbaar kunt maken voor uw gebruikers.
contentowner: saghosh
exl-id: f37c86e6-d4e3-4095-9e9d-7a5cd0d45e43
source-git-commit: 25c4873f6d01c5832c213b6f225172f3dbcba1ee
workflow-type: tm+mt
source-wordcount: '1987'
ht-degree: 0%

---

# Witte labels in de mobiele app van Adobe learning Manager

De mobiele Adobe Learning Manager-app ondersteunt nu witte labels, wat betekent dat u de app nu kunt vrijgeven onder uw eigen branding.

ALM zal bijgewerkte wit geëtiketteerde binaire dossiers volgens de volgende chronologie beschikbaar maken:

1. Voor belangrijke releases naar de mobiele app worden bestanden twee weken van tevoren beschikbaar gesteld.
2. Voor geplande updates voor urgente oplossingen worden de bestanden één week van tevoren beschikbaar gesteld.
3. Voor niet-geplande, urgente en onmiddellijke oplossingen worden bestanden beschikbaar gesteld met de beste inspanning.

Binaire bestanden worden beschikbaar gesteld in de door de klant aangewezen mappen. Neem contact op met uw CSM&#39;s om de bestanden te openen. De klant is verantwoordelijk voor tijdige publicatie en verwante processen.

## Hoe je je voorbereidt om je wit gelabelde app te starten

Voer de volgende stappen uit om uw eigen witte app met labels te implementeren en te beheren:

1. Bereid de elementen voor (zoals een afbeelding op het welkomstscherm) en de tekst zodat deze beide kunnen worden gebruikt in de app en de beschrijving in de app/play store.

1. Wijs een technische hulpbron toe die in staat is om:

   * Certificaatbestanden voor pushmeldingen genereren.
   * De app-binaire bestanden van het ALM-team ondertekenen.
   * Uploaden en het publicatieproces beheren. Het publicatieproces vereist communicatie tussen uw app-manager en app/play store-teams dat uw app voldoet aan alle publicatierichtlijnen. Vanuit ALM ontvangt u een volledig compatibele binaire app.

## Overzicht

Wit labelen is een praktijk waarbij u een app of service opnieuw brandt met uw eigen merk en deze aanpast alsof u de oorspronkelijke maker bent. In Adobe Learning Manager kunt u witte labels toepassen op de mobiele app, zodat u de app een nieuw merk kunt geven en de app onder uw eigen merk beschikbaar kunt maken voor uw gebruikers.

## Wat kan worden aangepast

U kunt het volgende aanpassen:

### Velden

<table>

 <tbody>

  <tr>

   <td>

    <p>Account-id</p>

   </td>

   <td>

    <p>De id van uw account. Let op: de witte gelabelde app is niet toegankelijk voor studenten die tot een ander account behoren.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Aanvullende account-id's</p>

   </td>

   <td>

    <p>Voeg desgewenst meerdere accounts (subdomeinen) toe. Voeg de subdomeinen toe als komma's gescheiden zonder spaties. Bijvoorbeeld acc01,acc02,acc03 enzovoort.<br> <b> Nota:</b> u moet accountidentiteitskaart toevoegen wanneer het specificeren van sub-domeinen.</br> </p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Toepassingsnaam</p></td>

   <td>

    <p>De naam die u voor de app wilt gebruiken.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Korte naam app</p>

   </td>

   <td>

    <p>Als de naam van de app lang is, geeft u de app een korte naam die op het apparaat wordt weergegeven.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Interne toepassingsnaam</p></td>

   <td>

    <p>De naam waarmee het besturingssysteem de app identificeert. Meestal wordt de volgende indeling gebruikt: com.company-name.product-name.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Interne toepassingsnaam-iOS</p>

   </td>

   <td>

    <p>Geef de app een andere naam als uw gebruikers zich op iOS bevinden. We raden u aan dezelfde naam te gebruiken voor zowel iOS als Android.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>App-pictogram</p>

   </td>

   <td>

    <p>Het app-pictogram als png. Dit pictogram wordt weergegeven in uw app. De naamnotatie is account-id_appIcon.png. De afmetingen van het app-pictogram zijn 512 x 512 pixels.<div>Houd er rekening mee dat Apple Alpha in app-pictogrammen niet toestaat. Verwijder dus het kanaal van de Alpha uit het element voordat u het verzendt.</div></p>

   </td>

  </tr>

  <tr>

   <td>

    <p>App-welkomstscherm</p></td>

   <td>

    <p>Geef voor het welkomstscherm van uw app een afbeelding (png) op die wordt weergegeven wanneer uw gebruikers de app starten. De naamnotatie is account-id_splashIcon.png. De afmetingen van de op vierkant gebaseerde welkomstschermen zijn 1052 × 1052 pixels en de cirkelvormige welkomstschermen zijn 768 x 768 pixels.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Client-id en clientgeheim</p>

   </td>

   <td>

    <p>De integratiebeheerder van uw account geeft de gegevens op tijdens de registratie van de app. De integratiebeheerder moet het volgende gebruiken:<ul><li>student:lezen,student:schrijven als rol</li><li>interne app name://redirect als redirect URL</li></ul></p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Accountlogo</p>

   </td>

   <td>

    <p>De URL die het logo van uw organisatie host. Geef een link naar inhoud op als het accountlogo. De URL moet via webcodering worden gecodeerd.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>App Store-id voor de app (iOS)</p>

   </td>

   <td>

    <p>De id die is vereist voor het implementeren van de geforceerde update. De app moet weten dat de student moet worden omgeleid naar de App Store om de app bij te werken.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Google Play Store-id voor de app (Android)</p>

   </td>

   <td>

    <p>De id die is vereist voor het implementeren van de geforceerde update.</p>

   </td>

  </tr>

  <tr>

   <td>

    <p>Hostnaam voor deep linking</p>

   </td>

   <td>

    <p>Gebruik Learningmanager om uw diepe koppelingen te hosten. Geef de URL van de host op als u een andere hostnaam-URL wilt gebruiken als een diepe koppeling. Bijvoorbeeld learningmanager.adobe.com.</p>

   </td>

  </tr>

 </tbody>

</table>

>[!NOTE]
>
>Geef de gegevens op aan uw CSAM&#39;s, zodat ze deze kunnen toevoegen aan uw aangepaste binaire toepassingscode.


#### Koppeling naar sites bijwerken om aangepaste diepte te verwerken

Als u een aangepast domein of leermanager als host gebruikt, hoeft u geen actie te ondernemen. Als u echter een aangepaste oplossing of een specifieke hostnaam voor de URL&#39;s gebruikt, voegt u de sitegekoppelde bestanden toe.

>[!CAUTION]
>
>Als de bestanden niet aanwezig zijn, werken de vervormingen niet. Zorg ervoor dat de bestanden aanwezig zijn.


Raadpleeg de volgende koppelingen voor meer informatie:

* [ Android ](https://learningmanager.adobe.com/.well-known/assetlinks.json)
* [ iOS ](https://learningmanager.adobe.com/.well-known/apple-app-site-association)

## Pushmeldingen genereren

Voor het verzenden van pushmeldingen naar Android- en iOS-apps zijn twee verschillende mechanismen vereist.

* Voor iOS genereert u de certificaten voor pushmeldingen.
* Geef voor Android een serversleutel op die is gegenereerd uit het Firebase-project.

Volg de onderstaande instructies om de projecten in Firebase in te stellen:

### Pushmeldingen op iOS

In de ontwikkeling van een iOS-app is een certificaat voor pushmeldingen een cryptografische referentie die door Apple is uitgegeven waarmee een server op een veilige manier pushmeldingen naar een iOS-apparaat kan verzenden via APN&#39;s (Apple Push Notification service).

Het certificaat zorgt voor een veilige communicatie tussen uw server (of provider) en Apple APNs bij het verzenden van pushberichten naar iOS-apparaten.

Zowel Android als iOS gebruiken Firebase Cloud Messaging (FCM) als service voor het verzenden van pushmeldingen naar apparaten.

### Het certificaat genereren op iOS

Volg de procedure:

1. Genereer of download het **Push meldingscertificaat** en privé sleutel (.p12). Voor meer informatie, zie het [ document van de ontwikkelaar van Apple ](https://developer.apple.com/documentation/usernotifications/setting_up_a_remote_notification_server/establishing_a_certificate-based_connection_to_apns).

1. Installeer het p12-bestand nadat het bestand is gedownload. Gebruik het wachtwoord in uw **toegang Keychain** te installeren.

1. Navigeer aan **Mijn certificaten** en voer het certificaat uit. Zorg ervoor dat u het mime-type .cer selecteert.

1. Zodra u het p12-bestand en het cer-bestand beschikbaar hebt, voert u de volgende opdrachten uit:

```
- openssl pkcs12 -in privatekey.p12 -out myapnappkey.pem -nodes –clcerts

- openssl x509 -in privatekey.cer -inform DER -out myapnsappcert.pem 

- openssl s_client -connect gateway.sandbox.push.apple.com:2195 -cert myapnsappcert.pem -key myapnappkey.pem 
```

Als u verbinding kunt maken met de server, is het certificaat dat u hebt gemaakt geldig. Kopieer het certificaat en de waarden voor de persoonlijke sleutel uit het bestand myapnappkey.pem.

### Pushmeldingen op Android

Voor Android moet de gebruiker het bestand services.json uit het Firebase-project leveren om de vermelding toe te voegen aan de SNS-service.

Maak een project in Firebase en deel het bestand services.json met het CSM-team. Dit dossier is nodig voor op token-gebaseerde ingang in SNS. De serversleutel wordt niet meer gebruikt. Zie [ project in Vuurbasis ](#create-project-in-firebase) creëren.

Ga als volgt te werk om het bestand services.json te downloaden:

1. Login aan de **console van het Vuurwerk**.
1. Ga naar **montages van het Project** en selecteer **het Overseinen van de Wolk**.
1. Vind **het Overseinen API van de Wolk van de Wolk van de Vuurstand** en selecteer **leiden de Rekeningen van de Dienst**.
1. In de **pagina van de Rekening van de Dienst**, selecteer de **Rekeningen van de Dienst** in het linkerpaneel.
1. Vind uw projectingang, en selecteer **leiden details** onder acties.

   >[!NOTE]
   >
   >   De indeling voor het invoeren van projecten is &lt;-accountnaam->@appspot.gserviceaccount.com.

1. Ga naar het **lusje van Sleutels** en selecteer **Sleutel** toevoegen.
1. Als er geen sleutel is, creeer **nieuwe sleutel** en selecteer **JSON** als zeer belangrijk type. Hiermee wordt het JSON-bestand gegenereerd en gedownload.
1. Als er reeds een sleutel is, uitgezochte **upload bestaande sleutel**, kleef de sleutel, en upload het. Hiermee wordt het JSON-bestand gegenereerd en gedownload.

<!-- Set up a project in Firebase and share the server key with the CSAM.-->

Neem contact op met het CSM-team en deel het JSON-bestand om de vermelding toe te voegen aan de SNS-services op AWS. Gebruikers moeten de vermelding bij de SNS-service laten registreren voor de pushmelding, waardoor ze de hierboven gegenereerde certificaten moeten delen voor validatie.

## Project maken in Firebase {#create-project-in-firebase}

### Android

Hergebruik hetzelfde project dat u in de bovenstaande stappen hebt gemaakt voor pushmeldingen.

[ voeg het project ](https://learn.microsoft.com/en-us/xamarin/android/data-cloud/google-messaging/firebase-cloud-messaging) in Vuurbasis toe en wint het {***dossier 2} google-services.json terug.***

### iOS

[ voeg het project ](https://firebase.google.com/docs/ios/setup) aan Firebase toe en wint het {***dossier 2} GoogleService-Info.plist terug.***

>[!IMPORTANT]
>
>Verzend de bestanden naar het Adobe Learning Manager CSAM-team om de bestanden op te nemen voor de build van uw binaire bestand voor de app.


## De ondertekende binaire bestanden genereren

### iOS

<!--```
sh""" xcodebuild -exportArchive -archivePath Runner.xcarchive -exportPath "ipa_path/" -exportOptionsPlist {ExportFile} 

mv ipa_path/*.ipa "${env.AppName}_signed.ipa" """ 
```-->

De `<root>` omslag bevat het {**dossier 1} Runner.xcarchive.zip.** Voer de onderstaande opdrachten uit om het ondertekende binaire getal te genereren:

1. Voer de volgende opdracht uit om het archief te decomprimeren:

   ```
   unzip Runner.xcarchive.zip
   ```

2. Navigeer naar de map met apps:

   ```
   cd Runner.xcarchive/Products/Applications/Runner.app
   ```

3. Kopieer het mobiele inrichtingsbestand:

   ```
   cp <path>/<mobile-provisioningfile>.mobileprovision embedded.mobileprovision
   ```

4. Voer de volgende opdracht uit om uw ondertekeningsgegevens bij te werken naar de frameworkbibliotheek:

   ```
   codesign -f -s "Distribution Certificate Name" Frameworks/*
   ```

5. Ga terug naar de map `<root>` (waar Runner.xcarchive.zip zich bevindt):

   ```
   cd <root>
   ```

6. Het archief exporteren met Xcodebuild:

   ```
   xcodebuild -exportArchive -archivePath Runner.xcarchive -exportPath ipa_path/ -exportOptionsPlist <path>/<ExportOptions-file>.plist
   ```

7. Zoek het .ipa-bestand in de map ipa_path.
8. Upload het .ipa-bestand naar de `Diawi` -website.
9. Zodra volledig geupload, selecteer **[!UICONTROL verzend]** knoop.
10. Na voltooiing, zult u een QR code en een verbinding ontvangen.
11. Open de QR-code of de koppeling rechtstreeks in Safari.

Als het apparaat is opgenomen in het inrichtingsprofiel, moet de installatie op het apparaat worden uitgevoerd.

>[!NOTE]
>
>U hebt XCode 15.2 of hoger nodig om de ondertekende binaire bestanden te maken.


### Android

**voor apk- dossier**

>[!IMPORTANT]
>
>Voordat u de opdracht `apksigner` uitvoert, voert u de volgende opdrachten uit om uw keystore-wachtwoord en key-aliaswachtwoord te exporteren als omgevingsvariabelen:
>
>```
>export KS_PASS=your_keystore_password
>export KEY_PASS=your_key_password
>```

```
sh""" <path>/apksigner sign --ks $storeFile. --ks-pass env:KS_PASS --ks-key-alias $key_alias --key-pass env:KEY_PASS --out app-release-signed.apk -v app-release.apk """
```

>[!NOTE]
>
>Het pad naar het gereedschap `apksigner` ziet er meestal als volgt uit: ~/Library/Android/sdk/build-tools/30.0.3/apksigner.

**voor aab dossier**

>[!NOTE]
>
>U hebt Android SDK-hulpprogramma&#39;s nodig om de ondertekende binaire bestanden te maken.

De Play Store vereist voor publicatie Android-binaire bestanden in de tabbladindeling. Daarom zullen wij het niet ondertekende .aab dossier verstrekken.

>[!NOTE]
>
>Wanneer u een sleutelarchiefbestand maakt, moet u een keystore-wachtwoord, een alias voor de ondertekeningssleutel en een aliaswachtwoord voor de ondertekeningssleutel genereren.

Volg de onderstaande stappen om het Ab-bestand te ondertekenen:

Voer de volgende opdracht uit:

```
<path>/jarsigner -verbose -sigalg SHA256withRSA -digestalg SHA-256 -keystore <keystore-file> app-release.aab <signingKeyAlias>
```

>[!NOTE]
>
>**[!UICONTROL jarsigner]** is inbegrepen met Java. Zorg ervoor dat u Java 21 gebruikt.

Voer bij de aanwijzing de volgende wachtwoorden in:

* Wachtwoord sleutelarchief
* wachtwoord voor het ondertekenen van sleutelalias

U kunt de meegeleverde apk gebruiken. Als u echter een apk wilt genereren op basis van een abb-bestand, voert u de volgende stappen uit:

>[!NOTE]
>
>U zult **[!UICONTROL bundletool]** moeten installeren om APKs te produceren.


Voer de volgende opdracht uit om het apk-bestand te maken:

```
java -jar <path>/bundletool-all.jar  build-apks --bundle=app-release.aab --output=my_app.apks --mode=universal
```

Als u het bestand wilt uitpakken, voert u de volgende opdracht uit:

```
unzip my_app.apks -d output_dir
```

U zult het apk dossier van de **[!UICONTROL output_dir]** omslag krijgen.

**Wat is volgende**

Nadat u de binaire bestanden hebt gegenereerd, drukt u de binaire bestanden naar de Play Store of App Store.

### Apps naar de winkel sturen voor revisie

Nadat u de definitieve binaire bestanden hebt ontvangen, kunt u deze uploaden naar de respectievelijke App Store (iOS of Android) voor revisie. Voer de volgende stappen uit om de binaire bestanden te uploaden naar de App Store.

**iOS**

1. Meld u met uw App Store-gegevens aan bij de Transporter-app.
2. Selecteer **+** knoop bij de linkerbovenkant en upload het productiecertificaat (.ipa dossier).
3. Als het .ipa-bestand correct is, wordt u gevraagd om de app te uploaden naar de App Store.
4. Meld u aan bij de App Store nadat de app is geleverd. Binnen een paar uur, zal het binaire getal in de sectie TestFlight verschijnen. U kunt de app inschakelen voor het testen van de uiteindelijke hygiëne in TestFlight vóór de revisie van de app en deze IPA als binair bestand gebruiken bij het indienen van de app voor een nieuwe release.

**Android**

1. Open de Google Play Store Console.
2. Ga naar **[!UICONTROL Dashboard]** > **[!UICONTROL de Versies van de App van de Mening]** > **[!UICONTROL Dashboard van de Versie]** en selecteer dan **[!UICONTROL creeer Nieuwe Versie]**.
3. Upload het gegenereerde .aab-bestand als de appbundel en typ releasedetails zoals het versienummer en de nieuwe functies.
4. Sla uw wijzigingen op en verzend de app voor revisie.
5. Stel de distributie van de app in op 100% (Google stelt deze standaard in op 20%).

#### Nuttige koppelingen voor het publiceren van apps

**Android**

[ creeer en opstelling uw app ](https://support.google.com/googleplay/android-developer/answer/9859152?hl=en)
[ Bereid uw app voor overzicht ](https://support.google.com/googleplay/android-developer/answer/9859455?sjid=2454409340679630327-AP) voor

**iOS**

[ legt voor overzicht ](https://developer.apple.com/help/app-store-connect/manage-submissions-to-app-review/submit-for-review) voor

## Hoe pas ik de wijzigingen toe

Verzendt de vereiste middelen en bestanden naar het CSM-team. Het team CSM vult dan de [ vorm ](https://forms.office.com/r/bJRRaRBvSh) met de vereiste veranderingen en maakt de vereiste activa vast. Het team zal dan de technische teams van de veranderingen evalueren en informeren. Het technische team genereert vervolgens een build en deelt deze met het CSM-team.

Het CSM-team zal de build met de klant delen.

## Wat kan niet worden aangepast

* Scherm Wachtwoord bijwerken
* Een accountscherm maken
