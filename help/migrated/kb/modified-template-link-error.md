---
jcr-language: en_us
title: E-mailkoppelingen die zijn geactiveerd vanuit gewijzigde sjablonen genereren een fout in Leerbeheer
description: E-mailkoppelingen die zijn geactiveerd vanuit gewijzigde sjablonen, veroorzaken een fout in Adobe Learning Manager
contentowner: nluke
preview: true
source-git-commit: 6abc118c6ad7e66e3ded5bd26b9167c3a0b99e4b
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---



# E-mailkoppelingen die zijn geactiveerd vanuit gewijzigde sjablonen genereren een fout in Leerbeheer

## Probleem

Er treedt een fout op nadat u op een koppeling hebt geklikt voor een geautomatiseerde e-mail/welkomstmail/inschrijvingsmail.

**Fout**

HTTP-status 400 - Onjuiste aanvraag

![](assets/email-404.png)

## Oorzaak

Dit gebeurt gewoonlijk wanneer de e-mailsjablonen niet goed zijn aangepast.

**Oplossing**

Volg de onderstaande stappen om fouten te voorkomen die betrekking hebben op verbroken koppelingen en die kunnen optreden als gevolg van aanpassingen:

1. Meld u aan als beheerder.
1. Klik in het linkerdeelvenster op **[!UICONTROL E-mailsjablonen]**.

1. Navigeer naar de gewenste sjabloon en klik om deze te wijzigen.

   Hiermee opent u het dialoogvenster **Sjabloonvoorbeeld** venster.

   ![](assets/email-template.png)

   Houd rekening met de punten bij het bewerken van een e-mailsjabloon:

   * We raden u aan een e-mailsjabloon te wijzigen vanuit de LMS-interface.
   * Kopieer de gewijzigde sjabloon naar een Kladblok/Word-bestand om een kopie van de aangebrachte wijzigingen op te slaan.
   * Vervang geen dynamische tekst in de sjabloon die in blauw is gemarkeerd. Bijvoorbeeld &quot;**Naam organisatie**&quot;, &quot;**Student**&quot;, &quot;**hier klikken**&quot;, &quot;**CertificateName**&quot; enzovoort.

1. Klikken **[!UICONTROL Opslaan]** om de wijzigingen te bevestigen die op de sjabloon zijn toegepast.
1. Trigger de e-mail om te verifiëren of de verbindingen zoals verwacht werken.
1. Terugkeren naar origineel door op de optie te klikken **Origineel herstellen** voor de gewijzigde sjabloon.
