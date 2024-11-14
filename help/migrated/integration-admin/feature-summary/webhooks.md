---
jcr-language: en_us
title: Webhooks
description: Meer informatie over Webhooks om real-time informatie, zoals cursusinschrijvingen, het maken van cursussen en andere informatie, naar een specifieke URL te verzenden
contentowner: chandrum
exl-id: 472aaf2b-9c2f-4f43-a791-2b2d81e69471
source-git-commit: e4c3489db8207ead0416656161b918eba42f4582
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 0%

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
