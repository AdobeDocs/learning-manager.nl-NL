---
jcr-language: en_us
title: Ondersteuning voor aangepast domein
description: Aangepaste domeinen worden niet ondersteund in een Azure-instantie van Learning Manager.
contentowner: saghosh
exl-id: 162ce268-48e3-4c7e-acb1-5181cebbb18d
source-git-commit: a09c81a6dacbfc4bb55db39e64820ba87ce53d09
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 66%

---

# Ondersteuning voor aangepast domein

Aangepaste domeinen worden niet ondersteund in een Azure-instantie van Learning Manager.

## Overzicht {#overview}

Met ondersteuning voor aangepast domein kunnen klanten de volledige controle krijgen over de domeinnaam die ze kunnen gebruiken voor hun account in Learning Manager. De klant moet het aangepaste domein afzonderlijk aanschaffen en met een Adobe-team samenwerken om het in te stellen als aanmeldings-URL voor het leerplatform.

Hiermee kan de klant de aanmeld- en toegangservaring blanco maken, zodat gebruikers de aanwezigheid van Adobe of Adobe Learning Manager niet zien.

U wilt bijvoorbeeld uw domein zodanig aanpassen dat uw gebruikers dezelfde ervaring krijgen als wanneer ze zich op het domein van de Adobe bevinden. Als ABC Inc hun klanten wil trainen, zou het graag zien dat ze landen op een domein met de naam `abc.com/mylearning` in plaats van `learningmanager.adobe.com/abc-inc/mylearning` .

>[!NOTE]
>
>U moet het domein registreren, waarna de Adobe u door het aanpassen van de URL leidt.


De functie voor aangepaste domeinen is beschikbaar tegen extra kosten. Neem contact op met uw Customer Success-manager voor meer informatie.

* Voor de studentrol begint het domein met `https://cdn.<customer_custom_domain>/` Bijvoorbeeld: `https://cdn.elearningstage1.cpdomaintest.in/`
* Voor alle andere rollen begint het domein met `https://<customer_custom_domain>/` . Bijvoorbeeld: `https://elearningstage1.cpdomaintest.in/`
* De werkelijke aanmeldings-URL is `https://<customer_custom_domain>/acapindex` of `https://<customer_custom_domain>/login` .

>[!NOTE]
>
>Vervang `<customer_custom_domain>` door het werkelijke domein van uw organisatie.

## Een aangepast domein instellen voor een account {#howtosetupacustomdomainonanaccount}

Een klant moet altijd eigenaar zijn van een domeinnaam en het domein kopen bij een provider.

Laten we als voorbeeld aannemen dat een klant een fictief domein bezit, genaamd **acme.com**. De klant wil Learning Manager-content leveren vanaf **learning.acme.com**.

Volg de onderstaande stappen om een aangepast domein in te stellen.

1. De klant moet **drie CNAME**-bestanden toevoegen aan het domein:

   * **learning.acme.com:** openbaar die eindpunt ALB van het Leren Manager door Adobe wordt gedeeld
   * **lrs.learning.acme.com:** openbaar eindpunt ALB dat door learning.acme.com wordt gericht
   * **cdn.learning.acme.com:** CDN eindpunt dat door Adobe wordt gedeeld

1. De klant moet SSL-certificaten leveren voor deze domeinen:

   * learning.acme.com
   * lrs.learning.acme.com
   * cdn.learning.acme.com

1. Adobe uploadt deze SSL-certificaten naar AWS ALB voor het leveren van verzoeken aan de domeinen.
1. Adobe voegt learning.acme.com toe aan zijn SAN-certificaat.
1. Adobe genereert de SP-metadata voor de klant, aangezien de metadata de URL&#39;s van de aangepaste domeinen bevatten.

   * Als de klant over aanmelden via sociale media wenst te beschikken, moet Adobe de patronen van de omleidings-URL&#39;s van de socialemediasites toevoegen aan de lijst met toegestane URL&#39;s.
   * Als de klant SSO heeft ingeschakeld, moet de klant met zijn IDP samenwerken om zijn domeinen toe te voegen aan de omleidings-URL&#39;s. De klant moet de XML met IDP-metadata delen met Adobe. Adobe moet vervolgens de SSO-instellingen van het account van de klant bijwerken.

1. Adobe wijzigt dan de S3 CORS-regels zodat het domein van de klant wordt toegevoegd.
