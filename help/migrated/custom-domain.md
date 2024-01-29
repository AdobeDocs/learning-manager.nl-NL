---
jcr-language: en_us
title: Ondersteuning voor aangepast domein
description: Aangepaste domeinen worden niet ondersteund in een Azure-instantie van Leermanager.
contentowner: saghosh
source-git-commit: 8635072782253cbac3f913953797cae7c0bc5ef4
workflow-type: tm+mt
source-wordcount: '446'
ht-degree: 0%

---



# Ondersteuning voor aangepast domein

Aangepaste domeinen worden niet ondersteund in een Azure-instantie van Leermanager.

## Overzicht {#overview}

Dankzij aangepaste domeinondersteuning kunnen klanten volledige controle verkrijgen over de domeinnaam die ze in Learning Manager voor hun account kunnen gebruiken. Een klant moet het aangepaste domein afzonderlijk aanschaffen en met het Adobe-team samenwerken om het in te stellen als aanmeldings-URL voor zijn of haar leerplatform.

Zo kan de klant de aanmeldingsgegevens en de toegangservaring wit labelen, zodat de gebruikers geen Adobe of Adobe Learning Manager zien.

U wilt bijvoorbeeld uw domein zodanig aanpassen dat uw gebruikers dezelfde ervaring krijgen als wanneer ze zich op het domein van de Adobe bevinden. Als ABC Inc hun klanten wil trainen, zou het graag zien dat ze landen op een domein genaamd `abc.com/mylearning`, in plaats van `learningmanager.adobe.com/abc-inc/mylearning`.

>[!NOTE]
>
>U moet het domein registreren, waarna de Adobe u door het aanpassen van de URL leidt.


De functie voor aangepaste domeinen is beschikbaar tegen extra kosten. Neem contact op met uw Customer Success-manager voor meer informatie.

* Voor de studentrol begint het domein met `https://cdn.<customer_custom_domain>/` Bijvoorbeeld: `https://cdn.elearningstage1.cpdomaintest.in/`
* Voor alle andere rollen begint het domein met `https://<customer_custom_domain>/`. Bijvoorbeeld: `https://elearningstage1.cpdomaintest.in/`

`<customer_custom_domain>` is het aanpasbare onderdeel.

## Een aangepast domein instellen voor een account {#howtosetupacustomdomainonanaccount}

Een klant moet altijd eigenaar zijn van een domeinnaam en het domein kopen bij een provider.

Laten we bijvoorbeeld bedenken dat een klant een fictief domein heeft. **acme.com**. De klant wenst dat leermaninhoud wordt bediend door **learning.acme.com**.

Volg de onderstaande stappen om een aangepast domein in te stellen.

1. De klant moet **drie CNAME toevoegen** records in het domein:

   * **learning.acme.com:** openbaar ALB-eindpunt van leermanager gedeeld door Adobe
   * **lrs.learning.acme.com:** Openbaar eindpunt van ALB-bestand waarnaar wordt verwezen op learning.acme.com
   * **cdn.learning.acme.com:** CDN-eindpunt gedeeld door Adobe

1. De klant moet SSL-certificaten opgeven voor deze domeinen:

   * learning.acme.com
   * lrs.learning.acme.com
   * cdn.learning.acme.com

1. Adobe uploadt deze SSL-certificaten naar AWS ALB voor het verzenden van aanvragen naar de domeinen.
1. Adobe voegt learning.acme.com toe aan het SAN-certificaat.
1. Adobe genereert de SP-metagegevens voor de klant omdat de metagegevens de aangepaste hoofd-URL&#39;s bevatten.

   * Als de klant zich wil aanmelden voor een sociaal netwerk, moet de Adobe de URL-omleidingspatronen van de sociale sites opnemen in de lijst met toegestane URL&#39;s.
   * Als de klant SSO heeft ingeschakeld, moet de klant met hun IDP samenwerken om hun domeinen op te nemen in de omleidingsURL&#39;s. De klant moet de XML-metagegevens van de IDP met Adobe delen. Adobe moet dan de SSO-instellingen van het account van de klant bijwerken.

1. Adobe zal dan de S3 regels van CORS wijzigen om het domein van de klant te omvatten.
