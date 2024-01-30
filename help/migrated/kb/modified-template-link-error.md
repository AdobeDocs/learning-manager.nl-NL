---
jcr-language: en_us
title: E-maillinks die worden geactiveerd vanuit gewijzigde sjablonen geven een fout in Learning Manager
description: E-mailkoppelingen die zijn geactiveerd vanuit gewijzigde sjablonen, veroorzaken een fout in Adobe Learning Manager
contentowner: nluke
preview: true
source-git-commit: 6abc118c6ad7e66e3ded5bd26b9167c3a0b99e4b
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 73%

---



# E-maillinks die worden geactiveerd vanuit gewijzigde sjablonen geven een fout in Learning Manager

## Probleem

Er treedt een fout op na het klikken op een link voor een geautomatiseerde e-mail/welkomstmail/inschrijvingse-mail.

**Fout**

HTTP-status 400: Ongeldige aanvraag

![](assets/email-404.png)

## Oorzaak

Dit gebeurt meestal wanneer de e-mailsjablonen onjuist zijn aangepast.

**Oplossing**

Volg de onderstaande stappen om fouten te voorkomen die verband houden met verbroken links, die u kunt zien als gevolg van aanpassing:

1. Meld u aan als beheerder.
1. Klik in het linkerdeelvenster op **[!UICONTROL E-mailsjablonen]**.

1. Ga naar de gewenste sjabloon en klik om deze te wijzigen.

   Hiermee wordt het venster **Voorbeeld van sjabloon** geopend.

   ![](assets/email-template.png)

   Let op de volgende punten bij het bewerken van een e-mailsjabloon:

   * Het is raadzaam een e-mailsjabloon aan te passen vanuit de Learning Manager-interface.
   * Kopieer en plak de gewijzigde sjabloon in een Kladblok/Word-bestand om een kopie van de aangebrachte wijzigingen op te slaan.
   * Voorkom dat u dynamische tekst in de sjabloon vervangt die blauw is gemarkeerd. Bijvoorbeeld &quot;**Naam organisatie**&quot;, &quot;**Student**&quot;, &quot;**hier klikken**&quot;, &quot;**CertificateName**&quot; enzovoort.

1. Klikken **[!UICONTROL Opslaan]** om de wijzigingen te bevestigen die op de sjabloon zijn toegepast.
1. Activeer de e-mail om te controleren of de links naar behoren werken.
1. Terugkeren naar origineel door op de optie te klikken **Origineel herstellen** voor de gewijzigde sjabloon.
