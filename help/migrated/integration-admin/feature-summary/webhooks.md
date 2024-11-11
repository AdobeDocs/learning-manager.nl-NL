---
jcr-language: en_us
title: Webhooks
description: Meer informatie over Webhooks om real-time informatie, zoals cursusinschrijvingen, het maken van cursussen en andere informatie, naar een specifieke URL te verzenden
contentowner: chandrum
source-git-commit: e4b0526e11083d116bf4ca4b0816892e0e8f0f9d
workflow-type: tm+mt
source-wordcount: '1695'
ht-degree: 1%

---

# Webhooks

Met een webhook kan een entiteit automatisch realtime gegevens of meldingen naar een andere entiteit verzenden wanneer een specifieke gebeurtenis plaatsvindt. Zo kan een toepassing andere toepassingen informatie verschaffen zonder er voortdurend om te vragen. Als een gebruiker bijvoorbeeld een cursus LMS (Learning Management System) voltooit, kan een webhook die informatie automatisch naar een ander platform verzenden, zoals een CRM- of rapportagetool. Webhooks worden vaak gebruikt in integraties om processen te automatiseren en de behoefte aan handmatige updates tussen systemen te verminderen. Stel webhooks in door een callback-URL op te geven waarnaar u de gegevens wilt verzenden.

## Webhooks vs API&#39;s

Webhooks en API&#39;s helpen beide systemen met elkaar te communiceren, maar ze werken op verschillende manieren. Met API&#39;s wordt de informatie alleen gedeeld wanneer de gebruiker hierom verzoekt. Als een student bijvoorbeeld voortgangsgegevens van een cursus nodig heeft, stuurt hij of zij een aanvraag naar de API, die de informatie vervolgens verstrekt. Webhooks daarentegen verzenden automatisch gegevens onmiddellijk wanneer een gebeurtenis plaatsvindt. Als een student bijvoorbeeld een cursus voltooit, stuurt hij de gegevens onmiddellijk naar de URL van de listener zonder handmatig verzoeken.

## Wat zijn real-time API’s?

Met real-time API&#39;s kunnen toepassingen direct gegevens uitwisselen wanneer een gebeurtenis plaatsvindt. In tegenstelling tot traditionele API&#39;s, die wachten tot een gebruiker informatie aanvraagt, delen real-time API&#39;s gegevens op het moment dat het gebeurt. Webhooks fungeren als een real-time API en helpen de gegevens direct te delen wanneer de opgegeven gebeurtenis plaatsvindt. De real-time API zorgt ervoor dat deze gegevensoverdracht onmiddellijk plaatsvindt zonder dat een handmatig verzoek nodig is, zodat systemen onmiddellijk kunnen worden bijgewerkt.

## Webhook-gebeurtenissen

Webhookgebeurtenissen zijn specifieke acties die plaatsvinden in een systeem dat automatisch gegevens verzendt naar een listener-URL. Wanneer een student zich bijvoorbeeld voor een cursus inschrijft, wordt een webhookgebeurtenis getriggerd en worden de inschrijvingsgegevens naar de URL van de listener gestuurd.
Webhookgebeurtenissen zijn geclassificeerd in twee categorieën:

* **Real-time gebeurtenissen**: De gebeurtenissen worden verwerkt en in real time verzonden naar een doel URL
* **niet gebeurtenissen in real time**: De gebeurtenissen worden verwerkt in partijen en verzonden op gespecificeerde tijden in plaats van in real time

## Listener-URL

Een URL van de Listener is een eindpunt of een doel dat gegevensinformatie ontvangt wanneer een gebeurtenis plaatsvindt. Wanneer een specifieke gebeurtenis plaatsvindt, zoals een gebruiker die zich voor een cursus inschrijft, stuurt het systeem automatisch de gegevens naar deze URL zonder handmatig verzoek. De listener-URL is het adres waar al deze updates worden geleverd.
Webhook verzendt de relevante informatie in JSON-indeling. Hier volgt een voorbeeld van een lading voor een gebeurtenis die in Adobe Learning Manager wordt geactiveerd:

```
{
  "accountId": 1010,
  "events": [
    {
      "eventId": "d5fb7071-10a9-46b2-9f9e-79dde346c052",
      "eventName": "COURSE_ENROLLMENT_BATCH",
      "timestamp": 1727414643000,
      "eventInfo": "1727414643000-047210-84242-0",
      "data": {
        "userId": 4279332,
        "loId": "course:7374992",
        "loInstanceId": "course:7376092_10250977",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": 1727414643
      }
    }
  ]
}
```

## Webhooks maken en beheren - integratiebeheerder

Volg de onderstaande stappen om Webhooks-integratie te maken in Adobe Learning Manager:

1. Login als **[!UICONTROL Admin van de Integratie]**.
2. Voor de homepage, uitgezochte **[!UICONTROL Webhooks]** > **[!UICONTROL voeg Webhook]** toe.

   ![](assets/create-webhook.png)
   _voeg een webhook_ toe

3. Typ de **[!UICONTROL Naam]** en **[!UICONTROL Beschrijving]** van de Webhook.
4. Typ de luisteraar URL als a **[!UICONTROL Doel URL]** waar u de gebeurtenisgegevens wilt overgaan.
5. Selecteer een van de verificatiemethoden:
Verificatie in Webhooks is een beveiligingsmethode om ervoor te zorgen dat de gegevens die naar een listener-URL worden verzonden, afkomstig zijn van een vertrouwde bron.
   * **[!UICONTROL niets]**: Geen vereiste authentificatie.
   * **[!UICONTROL Basis]**: Dit is op referentie-gebaseerde authentificatie. Voer de gebruikersnaam en het wachtwoord in.
   * **[!UICONTROL Handtekening]**: Het systeem leidt tot een speciale handtekening en voegt het aan de webhookgegevens toe. De ontvangende server controleert deze code om ervoor te zorgen dat de gegevens echt zijn en niet zijn veranderd. Genereer een handtekening en gebruik deze voor verificatie. Download de handtekening als JSON.
6. Selecteer de gebeurtenissen Webhook van de **[!UICONTROL gebeurtenissen van de Trekker]** dropdown.

   >[!NOTE]
   >
   >U kunt de webhooks ook testen door de optie Webhooks testen te selecteren op de pagina Webhook toevoegen.

7. Selecteer de **[!UICONTROL knevel van de Status van de Activering]** om webhook toe te laten. Als deze optie is ingeschakeld, worden gegevens doorgegeven wanneer de geselecteerde gebeurtenissen plaatsvinden.

>[!NOTE]
>
>U kunt maximaal vijf webhooks maken en beheren.

### Webhooks bewerken - integratiebeheerder

Ga als volgt te werk om Webhooks uit Adobe Learning Manager te bewerken:

1. Login als **[!UICONTROL Admin van de Integratie.]**
2. Selecteer **[!UICONTROL Webhooks]** op de homepage.
3. Selecteer de webhook die u wilt bewerken.

   ![](assets/edit-webhook.png)
   _geef webhook_ uit
4. Selecteer **[!UICONTROL uitgeven]** om de details van webhook te wijzigen en **[!UICONTROL sparen]** te selecteren.

### Webhooks verwijderen - integratiebeheerder

Ga als volgt te werk om Webhooks uit Adobe Learning Manager te bewerken:

1. Login als **[!UICONTROL Admin van de Integratie]**.
2. Selecteer **[!UICONTROL Webhooks]** op de homepage.
3. Selecteer de webhook die u wilt verwijderen.
4. Selecteer **[!UICONTROL Schrapping]** om de webhooks te verwijderen.

![](assets/delete-webhooks.png)
_verwijder webhook_

### Webhooks van Adobe - integratiebeheerder

Ga als volgt te werk om de webhooks te archiveren:

1. Login als **[!UICONTROL Admin van de Integratie]**.
2. Selecteer **[!UICONTROL Webhooks]** op de homepage.
3. Selecteer de webhook die u wilt bewerken.
4. Selecteer **[!UICONTROL uitgeven]** en maak de **[!UICONTROL Status van de Activering]** onbruikbaar om webhook te archiveren.

![](assets/retire-webhook.png)
_band webhook_

## Real-time gebeurtenissen

| S.No | Webhook-gebeurtenissen | Beschrijving |
|---|---|---|
| 1 | CI_STATS | Wordt geactiveerd wanneer de beschikbaarheid van de licentie of wachtlijst voor een cursusinstantie wordt gewijzigd. |
| 2 | COURSE_ENROLLMENT | Wordt geactiveerd wanneer een student zich voor een cursus inschrijft. |
| 3 | CURSE_COMPLETED | Wordt geactiveerd wanneer een student een cursus heeft voltooid. |
| 4 | LEREN_PATH_ENROLLMENT | Wordt geactiveerd wanneer een student zich inschrijft voor een leerpad. |
| 5 | LEREN_PATH_COMPLETED | Wordt geactiveerd wanneer een student een leerpad heeft voltooid. |
| 6 | CERTIFICATION_ENROLLMENT | Wordt geactiveerd wanneer een student zich inschrijft voor een certificering. |
| 7 | CERTIFICATION_COMPLETED | Wordt geactiveerd wanneer een student een certificering heeft voltooid. |
| 8 | CURSE_UNENROLLMENT | Wordt geactiveerd wanneer een student zich uitschrijft voor een cursus. |
| 9 | LEARNING_PATH_UNENROLLMENT | Wordt geactiveerd wanneer een student zich uitschrijft vanuit een leerpad. |
| 10 | CERTIFICATION_UNENROLLMENT | Wordt geactiveerd wanneer een student zich uitschrijft voor een certificering. |
| 11 | LEARNING_OBJECT_DRAFT | Wordt geactiveerd tijdens het maken van een leerobject in conceptstatus. |
| 12 | LEARNING_OBJECT_DELETION | Wordt geactiveerd tijdens het verwijderen van een leerobject. |
| 13 | LEREN_OBJECT_MODIFICATION | Wordt geactiveerd tijdens de wijziging van een leerobject. |
| 14 | LEARNING_OBJECT_INSTANCE_MODIFICATION | Wordt geactiveerd tijdens het maken of wijzigen van een leerobjectinstantie.<div><b> Nota:</b> het wordt geadviseerd om cursusinstanties slechts te gebruiken nadat de cursus wordt gepubliceerd.</div> |
| 15 | LEARNING_OBJECT_INSTANCE_DELETION | Wordt geactiveerd tijdens het verwijderen van een leerobjectinstantie. |

## Niet-realtime gebeurtenissen

| S.No | Webhook-gebeurtenissen | Beschrijving |
|---|---|---|
| 1 | COURSE_ENROLLMENT_BATCH | Wordt geactiveerd wanneer een beheerder/manager/platform studenten voor een cursus inschrijft. |
| 2 | CURSE_COMPLETED_BATCH | Wordt geactiveerd wanneer een beheerder/manager/platform een cursus als voltooid markeert. |
| 3 | LEREN_PATH_ENROLLMENT_BATCH | Wordt geactiveerd wanneer een beheerder/manager/platform studenten inschrijft in een leerpad. |
| 4 | LEREN_PATH_COMPLETED_BATCH | Wordt geactiveerd wanneer een beheerder/manager een leerpad als voltooid markeert. |
| 5 | CERTIFICATION_ENROLLMENT_BATCH | Wordt geactiveerd wanneer een beheerder/manager/platform studenten voor een certificering inschrijft. |
| 6 | CERTIFICATION_COMPLETED_BATCH | Wordt geactiveerd wanneer een beheerder/manager/platform een certificering als voltooid markeert. |
| 7 | LEARNER_PROGRESS | Traceert de voortgang van een student wanneer een module is voltooid. |
| 8 | CURSE_UNENROLLMENT_BATCH | Wordt geactiveerd wanneer een beheerder/manager/platform studenten van een cursus uitschrijft. |
| 9 | LEREN_PATH_UNENROLLMENT_BATCH | Wordt geactiveerd wanneer een beheerder/manager/platform studenten uitschrijft van een leerpad. |
| 10 | CERTIFICATION_UNENROLLMENT_BATCH | Wordt geactiveerd wanneer een beheerder/manager/platform studenten van een certificering uitschrijft. |
| 11 | LEREN_OBJECT_MODIFICATION_BATCH | Wordt geactiveerd tijdens de wijziging van een leerobject via de migratieworkflow. |
| 12 | LEARNING_OBJECT_INSTANCE_MODIFICATION_BATCH | Wordt geactiveerd tijdens het maken of wijzigen van een leerobjectinstantie via de migratieworkflow. |

## Aanbevolen werkwijzen voor webhooks

Webhooks bieden real-time gebeurtenisgestuurde communicatie tussen services. Onjuiste implementatie kan echter leiden tot verloren gebeurtenissen, trage systeemprestaties of beveiligingsrisico&#39;s. Hieronder vindt u de beste werkwijzen voor het implementeren van webhooks, waarbij de nadruk ligt op fouttolerantie, betrouwbaarheid en beveiliging.

### Fouttolerantie

De fout-verdraagzaamheid van het ALM webhooksysteem verstrekt aanbevelingen voor abonnees om potentiële kwesties, zoals gebeurtenisverlies, dubbele gebeurtenissen, en uit-van-orde levering te behandelen.

Voor ALM is een time-out voor de verbinding ingesteld op 10 seconden en een time-out voor de socket ingesteld op 5 seconden. De verwachting is dat de client het bericht erkent zodra het het ontvangt. Dit moet ervoor zorgen dat de client niet vertraagt tijdens het verwerken van berichten. Als er enige downstream-verwerking is die tijdrovend is, moet de klant de gebeurtenis nog steeds onmiddellijk erkennen en de downstream-verwerking aan het einde afhandelen.

#### Gegevensbehoud

Gebeurtenissen worden 7 dagen bewaard. Als ze niet binnen deze tijd worden verwerkt, gaan ze definitief verloren. Als de terugwinning op de laatste dag gebeurt en meer tijd nodig is, zal het systeem niet de retentieperiode verlengen.
Als gebeurtenissen sneller worden geproduceerd dan ze worden gebruikt, kunnen sommige gebeurtenissen verloren gaan. Hoewel dit niet gebruikelijk is, moeten abonnees erop toezien dat dit geen langetermijnprobleem wordt.

#### Webhooks uitschakelen

Wanneer een abonnee niet reageert op webhookgebeurtenissen, probeert het ALM-systeem de webhooks opnieuw met exponentiële back-up om te voorkomen dat de abonnee overweldigt.

Het proces voor opnieuw proberen begint met een eerste interval van 5 seconden. Als de abonnee niet antwoordt, verdubbelt de wachttijd aan 10, 20, 40, en 80 seconden, uiteindelijk stijgend tot een maximum van 5 minuten. Zodra het 5 minuten bereikt, zal het systeem elke 5 minuten opnieuw proberen tot de retentieperiode van 7 dagen voorbij is. Als de abonnee nog steeds niet reageert tijdens deze hele periode, wordt de webhook automatisch uitgeschakeld. Er wordt regelmatig een herinnerings-e-mail naar de abonnee verzonden.

#### Gebeurtenissen dupliceren

Als een abonnee na het verwerken van een gebeurtenis meer dan 5 seconden nodig heeft om te reageren, probeert het systeem dezelfde gebeurtenis mogelijk opnieuw te verwerken. Het wordt aanbevolen om gebeurtenis-id&#39;s te gebruiken om bij te houden welke gebeurtenissen al zijn verwerkt. Ook als de webhook vastloopt na het verzenden van de gebeurtenis, maar voordat het opslaan is voltooid, kan dezelfde groep gebeurtenissen opnieuw worden geprobeerd. Het wordt aanbevolen batch-id&#39;s of afzonderlijke gebeurtenis-id&#39;s te gebruiken om eventuele duplicaten te herkennen en te negeren.

#### Gebeurtenissen buiten bestelling

ALM probeert gebeurtenissen in de juiste volgorde te houden, maar soms kunnen gebeurtenissen op volgorde worden geleverd, vooral tussen real-time en niet-real-time gebeurtenissen.

Als een beheerder meerdere studenten tegelijk voor een cursus inschrijft, worden de inschrijvingsgebeurtenissen gemarkeerd als niet-real-time. Als een student de cursus echter snel voltooit, wordt die voltooiingsgebeurtenis gemarkeerd als real-time en kan deze vóór de inschrijvingsgebeurtenissen worden afgeleverd.

#### Aanbeveling voor fouttolerantie

Om deze fouten te voorkomen, moeten abonnees webhookgebeurtenissen actief controleren en waarschuwingen instellen voor problemen zoals gemiste gebeurtenissen, dubbele leveringen of reeksen die niet op volgorde staan.

## Specifieke richtlijnen voor Webhook-gebeurtenissen

1. Als u eerst een LEARNER_PROGRESS-gebeurtenis krijgt, negeert u de onderstaande gebeurtenissen:

   * COURSE_ENROLLMENT
   * COURSE_ENROLLMENT_BATCH
   * LEREN_PATH_ENROLLMENT
   * LEREN_PATH_ENROLLMENT_BATCH
   * CERTIFICATION_ENROLLMENT
   * CERTIFICATION_ENROLLMENT_BATCH

2. Negeer de gebeurtenis LEARNER_PROGRESS als deze na de volgende gebeurtenissen komt:

   * CURSE_COMPLETED
   * CURSE_COMPLETED_BATCH
   * LEREN_PATH_COMPLETED
   * LEREN_PATH_COMPLETED_BATCH
   * CERTIFICATION_COMPLETED
   * CERTIFICATION_COMPLETED_BATCH

3. Gebruik het tijdstempelveld om te bepalen of de gebeurtenis moet worden genegeerd of verwerkt, behalve voor de gebeurtenis LEARNER_PROGRESS.


## Voorbeelden van ladingen voor de gebeurtenissen

+++CI_STATS

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "01234567-0458-4450-b5dd-6bc1edr4560",
      "eventName": "CI_STATS",
      "timestamp": 1725604147,
      "eventInfo": "1725604145-LoSt",
      "data": {
        "loInstanceId": "course:1234567_123456775",
        "waitlistCount": 0,
        "enrollmentCount": 10,
        "seatLimit": 30
      }
    }
  ]
}
```

+++

+++COURSE_ENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "29123ec1-4576-4ec5-a057-3a6dr45t9d6",
      "eventName": "COURSE_ENROLLMENT",
      "timestamp": 1725524713,
      "eventInfo": "1725524713000-040366-10488-0",
      "data": {
        "userId": 1234567,
        "loId": "course:1234567",
        "loInstanceId": "course:1234567_1234567",
        "loType": "course",
        "enrollmentSource": "SELF_ENROLL",
        "dateEnrolled": 1725524713
      }
    }
  ]
  }
```

+++

+++COURSE_ENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "29572ec1-4576-4ec5-a057-3wsd43r59d6",
      "eventName": "COURSE_ENROLLMENT_BATCH",
      "timestamp": 1725524713,
      "eventInfo": "1725524713000-040366-10488-0",
      "data": {
        "userId": 1234567,
        "loId": "course:1234567",
        "loInstanceId": "course:12345678_123456788",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": 1725524713
      }
    }
  ]
  }
```

+++

+++COURSE_COMPLETED

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "c1a3168c-6c98-4ed3-b0b0-ba3da5087c1c",
      "eventName": "COURSE_COMPLETED",
      "timestamp": 1725523823,
      "eventInfo": "1725523823000-040363-12018-0",
      "data": {
        "userId": 12345678,
        "loId": "course:12345671",
        "loInstanceId": "course:1234567_12345674",
        "loType": "course",
        "enrollmentSource": "SELF_ENROLL",
        "dateCompleted": 1725523818,
        "hasPassed": true
      }
    }
  ]
}
```

+++

+++COURSE_COMPLETED_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "c1a3168c-6c98-4ed3-b0b0-ba3da5087c1c",
      "eventName": "COURSE_COMPLETED_BATCH",
      "timestamp": 1725523823,
      "eventInfo": "1725523823000-040363-12018-0",
      "data": {
        "userId": 112345678,
        "loId": "course:12345678",
        "loInstanceId": "course:1234567_12345678",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateCompleted": 1725523818,
        "hasPassed": true
      }
    }
  ]
}
```

+++

+++LEARNING_PATH_ENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "96ed0791-338f-4c4c-83bc-9fwfr4564965",
      "eventName": "LEARNING_PATH_ENROLLMENT",
      "timestamp": 1725604249,
      "eventInfo": "1725604248000-040653-71396-0",
      "data": {
        "userId": 11234567,
        "loId": "learningProgram:123456",
        "loInstanceId": "learningProgram:12345_134567",
        "loType": "learningProgram",
        "enrollmentSource": "SELF_ENROLL",
        "dateEnrolled": 1725604248
      }
    }
  ]
}
```

+++

+++LEARNING_PATH_ENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "96edft791-338f-4c4c-83bc-9f7erf94965",
      "eventName": "LEARNING_PATH_ENROLLMENT",
      "timestamp": 1725604249,
      "eventInfo": "1725604248000-040653-71396-0",
      "data": {
        "userId": 12345678,
        "loId": "learningProgram:12347",
        "loInstanceId": "learningProgram:12345_12345",
        "loType": "learningProgram",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": 1725604248
      }
    }
  ]
  }
```

+++

+++LEARNING_PATH_COMPLETED

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "e207104e-d554-4027-944b-08fty6fdddf",
      "eventName": "LEARNING_PATH_COMPLETED",
      "timestamp": 1725604392,
      "eventInfo": "1725604391000-040653-314618-0",
      "data": {
        "userId": 11080928,
        "loId": "learningProgram:12345",
        "loInstanceId": "learningProgram:12345_95662",
        "loType": "learningProgram",
        "enrollmentSource": "SELF_ENROLL",
        "dateCompleted": 1725604380,
        "hasPassed": true
      }
    }
  ]
  }
```

+++

+++LEARNING_PATH_COMPLETED_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "e207104e-d554-4027-944b-086debefdddf",
      "eventName": "LEARNING_PATH_COMPLETED",
      "timestamp": 1725604392,
      "eventInfo": "1725604391000-040653-314618-0",
      "data": {
        "userId": 12345678,
        "loId": "learningProgram:12345",
        "loInstanceId": "learningProgram:12345_95662",
        "loType": "learningProgram",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateCompleted": 1725604380,
        "hasPassed": true
      }
    } 
    ]
    }
```

+++

+++CERTIFICATION_ENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "8bdfr76-148e-4128-80e9-b89123456755",
      "eventName": "CERTIFICATION_ENROLLMENT",
      "timestamp": 1725604672,
      "eventInfo": "1725604672000-040654-559128-0",
      "data": {
        "userId": 12345678,
        "loId": "certification:1234567",
        "loInstanceId": "certification:123456_160299",
        "loType": "certification",
        "enrollmentSource": "SELF_ENROLL",
        "dateEnrolled": 1725604672
      }
    }
  ]
}
```

+++

+++CERTIFICATION_ENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "8b2ee776-148e-4128-80e9-12345678",
      "eventName": "CERTIFICATION_ENROLLMENT_BATCH",
      "timestamp": 1725604672,
      "eventInfo": "1725604672000-040654-559128-0",
      "data": {
        "userId": 123456788,
        "loId": "certification:1234567",
        "loInstanceId": "certification:12345678_160299",
        "loType": "certification",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateEnrolled": 1725604672
      }
    }
  ]
  }
```

+++

+++CERTIFICATION_COMPLETED

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "b8b63bf8-7521-4bc0-bc51-7f951ff63ea9",
      "eventName": "CERTIFICATION_COMPLETED",
      "timestamp": 1725604769,
      "eventInfo": "1725604768000-040654-756257-0",
      "data": {
        "userId": 12345678,
        "loId": "certification:1245678",
        "loInstanceId": "certification:1234567_160299",
        "loType": "certification",
        "enrollmentSource": "SELF_ENROLL",
        "dateCompleted": 1725604740
      }
    }
  ]
  }
```

+++

+++CERTIFICATION_COMPLETED_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "b8b63bf8-7521-4bc0-bc51-7f951ff63ea9",
      "eventName": "CERTIFICATION_COMPLETED_BATCH",
      "timestamp": 1725604769,
      "eventInfo": "1725604768000-040654-756257-0",
      "data": {
        "userId": 12345678,
        "loId": "certification:134567",
        "loInstanceId": "certification:1234567_160299",
        "loType": "certification",
        "enrollmentSource": "ADMIN_ENROLL",
        "dateCompleted": 1725604740
      }
    }
  ]
  }
```

+++

+++LEARNER_PROGRESS

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "dd04d3a4-c3df-44fa-a1cf-7edd6e3d2075",
      "eventName": "LEARNER_PROGRESS",
      "timestamp": 1725604552,
      "eventInfo": "1725604551000-297002-5823-0",
      "data": {
        "loId": "course:7542090",
        "loType": "course",
        "userId": 12345678,
        "loInstanceId": "course:1234567_11234567",
        "dateStarted": 1725604380,
        "progressPercent": 50
      }
}
]
}
```

+++

+++COURSE_UNENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "f3417817-8cb8-40ea-a441-813bec1c7724",
      "eventName": "COURSE_UNENROLLMENT",
      "timestamp": 1725515824,
      "eventInfo": "1725506253000-040298-24078-0",
      "data": {
        "userId": 12345671,
        "loId": "course:12345678",
        "loInstanceId": "course:12345678_14450088",
        "loType": "course",
        "enrollmentSource": "ADMIN_ENROLL",
      }
    }
  ]
}
```

+++

+++COURSE_UNENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "f3417817-8cb8-40ea-a441-8123e45724",
      "eventName": "COURSE_UNENROLLMENT_BATCH",
      "timestamp": 1725515824,
      "eventInfo": "1725506253000-040298-24078-0",
      "data": {
        "userId": 123456781,
        "loId": "course:12345678",
        "loInstanceId": "course:12345678_14450088",
        "loType": "course",
        "enrollmentSource": "SELF_ENROLL"
    }
   }
  ]
}
```

+++

+++LEARNING_PATH_UNENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "8e5df878-1dfd-47ac-9bfe-7d123456d1",
      "eventName": "LEARNING_PATH_UNENROLLMENT",
      "timestamp": 1725516573,
      "eventInfo": "1725506667000-040299-28209-0",
      "data": {
        "userId": 12345678,
        "loId": "learning_program:1234567",
        "loInstanceId": "learning_program:1234567_109139",
        "loType": "learning_program",
        "enrollmentSource": "SELF_ENROLL",
       
      }
    }
]
}
```

+++

+++LEARNING_PATH_UNENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "8e5df878-1dfd-47ac-9bfe-7d4952e3edd1",
      "eventName": "LEARNING_PATH_UNENROLLMENT",
      "timestamp": 1725516573,
      "eventInfo": "1725506667000-040299-28209-0",
      "data": {
        "userId": 1234567,
        "loId": "learning_program:1234567",
        "loInstanceId": "learning_program:1234567_109139",
        "loType": "learning_program",
        "enrollmentSource": "ADMIN_ENROLL"
      }
    }
]
}
```

+++

+++CERTIFICATION_UNENROLLMENT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "7902766b-54d8-472d-b933-7e89d1b75ef8",
      "eventName": "CERTIFICATION_UNENROLLMENT",
      "timestamp": 1725517341,
      "eventInfo": "1725507900000-040304-1065-0",
      "data": {
        "userId": 12345678,
        "loId": "certification:1234567",
        "loInstanceId": "certification:12345678_162078",
        "loType": "certification",
        "enrollmentSource": "SELF_ENROLL"
      }
    }
  ]
}
```

+++

+++CERTIFICATION_UNENROLLMENT_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "7902766b-54d8-472d-b933-7e89d1b75ef8",
      "eventName": "CERTIFICATION_UNENROLLMENT_BATCH",
      "timestamp": 1725517341,
      "eventInfo": "1725507900000-040304-1065-0",
      "data": {
        "userId": 12345678,
        "loId": "certification:1234567",
        "loInstanceId": "certification:1234567_162078",
        "loType": "certification",
        "enrollmentSource": "SELF_ENROLL"
      }
    }
  ]
}
```

+++

+++LEARNING_OBJECT_DRAFT

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1712349f-26ec-453c-b56a-cdf18a841948",
      "eventName": "LEARNING_OBJECT_DRAFT",
      "timestamp": 1725519188,
      "eventInfo": "1725519188000-040344-48604-0",
      "data": {
        "loId": "course:12345671",
        "loType": "course"
      }
    }
  ]
}
```

+++

+++LEARNING_OBJECT_DELETION

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "023456-5517-4c09-9cde-d953cdd8582c",
      "eventName": "LEARNING_OBJECT_DELETION",
      "timestamp": 1725605296,
      "eventInfo": "1234567800-040656-662792-0",
      "data": {
        "loId": "course:1234567",
        "loType": "course"
      }
    }
   ]
}
```

+++

+++LEARNING_OBJECT_MODIFICATION

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "22345668-af3e-4dd3-a515-ce19d7234873",
      "eventName": "LEARNING_OBJECT_MODIFICATION_BATCH",
      "timestamp": 1725523081,
      "eventInfo": "123456000-039736-54153-0",
      "data": {
        "loId": "learningProgram:1234567",
        "loType": "learningProgram"

      }
    }
  ]
}
```

+++

+++LEARNING_OBJECT_MODIFICATION_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "2234567068-af3e-4dd3-a515-ce19d7234873",
      "eventName": "LEARNING_OBJECT_MODIFICATION_BATCH",
      "timestamp": 1725523081,
      "eventInfo": "123456700-039736-54153-0",
      "data": {
        "loId": "learningProgram:1234567",
        "loType": "learningProgram"

      }
    }
  ]
}
```

+++

+++LEARNING_OBJECT_INSTANCE_MODIFICATION

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "b131da98-ab8d-43e9-b671-e79131cd69dc",
      "eventName": "LEARNING_OBJECT_INSTANCE_MODIFICATION",
      "timestamp": 1725603298,
      "eventInfo": "1723456000-040649-741781-0",
      "data": {
        "loInstanceId": "course:12345678_14453691",
        "loId": "course:12345678",
        "loType": "course"
        
      }
    }
  ]
}
```

+++

+++LEARNING_OBJECT_INSTANCE_MODIFICATION_BATCH

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "b23458-ab8d-43e9-b671-e79131cd69dc",
      "eventName": "LEARNING_OBJECT_INSTANCE_MODIFICATION_BATCH",
      "timestamp": 1725603298,
      "eventInfo": "112345000-040649-741781-0",
      "data": {
        "loInstanceId": "course:12345678_14453691",
        "loId": "course:1234568",
        "loType": "course"

      }
    }
  ]
}
```

+++

+++LEARNING_OBJECT_INSTANCE_DELETION

```
{
  "accountId": 1234,
  "events": [
    {
      "eventId": "1234560-d73a-457b-83f3-666ba9654edb",
      "eventName": "LEARNING_OBJECT_INSTANCE_DELETION",
      "timestamp": 1725605491,
      "eventInfo": "17223456700-040657-236307-0",
      "data": {
        "loInstanceId": "course:1234567_14453849",
        "loId": "course:1234567",
        "loType": "course"

      }
    }
  ]
}
```

+++

