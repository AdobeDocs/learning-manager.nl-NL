---
description: Lees dit artikel om te weten te komen hoe u e-mailsjablonen kunt configureren voor gebeurtenissen die betrekking hebben op alle leerobjecten.
jcr-language: en_us
title: E-mailsjablonen
source-git-commit: fda58bc18bee6d21ee904a442884e4759587d053
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---



# E-mailsjablonen

Lees dit artikel om te weten te komen hoe u e-mailsjablonen kunt configureren voor gebeurtenissen die betrekking hebben op alle leerobjecten.

De toepassing Learning Manager verzendt e-mailmeldingen naar meerdere rollen van gebruikers op basis van gebeurtenissen.

Als auteur kunt u e-mailsjablonen aanpassen door inhoud toe te voegen of te wijzigen en meldingen naar gebruikers te sturen voor verschillende gebeurtenissen die worden geactiveerd door studenten, managers en auteursactiviteiten. U kunt bijvoorbeeld een aangepaste e-mail verzenden wanneer een student zich voor uw cursus inschrijft. Bij inschrijving ontvangt de student automatisch de cursusspecifieke e-mail.

U kunt er ook voor kiezen om geen e-mailmeldingen voor bepaalde gebeurtenissen te verzenden door de optie voor de e-mailsjabloon uit te schakelen.

## E-mailmeldingen instellen {#settingemailnotifications}

1. Klik in de auteurstoepassing op het leerobject waarvoor u de e-mailsjabloon wilt configureren. Bijvoorbeeld Cursussen.
1. Klik op de pagina Leerobject op de cursus, certificering of leerprogramma die u wilt configureren voor de e-mailinstellingen.
1. Klik op E-mailsjablonen op de pagina met gegevens over leerobjecten.

   U kunt de lijst met sjablonen zien die beschikbaar zijn voor het leerobject dat u hebt gekozen.

   ![](assets/email-templates-forlearningprograms.png)
   *Lijst met sjablonen*

1. Klik op de naam van de gebeurtenis om de sjabloon in de voorvertoningsmodus weer te geven.

   ![](assets/preview-the-emailtemplateforyourlearningobject.png)

   *Zie voorbeeld sjabloon*

   U kunt elke sjabloon aanpassen door op de tekst in de hoofdtekst van de sjabloon te klikken. U kunt variabelen in de tekst invoegen door op de juiste pictogrammen te klikken, zoals te zien in de afbeelding. Houd de muis boven elk pictogram om de namen weer te geven.

   ![](assets/insert-variable.png)
   *Een variabele invoegen*

   De volgende variabelen zijn beschikbaar:

   * LPName
   * LPCompletionDeadline
   * LearnerName
   * LearnerEmail
   * CourseName
   * CourseDescription
   * CourseCompletionDeadline
   * CourseSkillDetails
   * CourseBadge

   U kunt het bericht op de standaardinhoud herstellen door op Origineel herstellen boven de sjabloon te klikken.

   Zoals u boven aan de sjabloon ziet, kunt u de sjabloon voor meerdere rollen aanpassen (manager, student, enzovoort), afhankelijk van het type e-mailmelding.

1. Klik op Opslaan onder aan de pagina met sjablonen.
1. Klik op de pagina E-mailsjablonen op de cirkelwisselknop Ja/Nee om de melding te verzenden of uit te schakelen.

![](assets/email-notification-e1437624109719.png)
*E-mailmelding in- of uitschakelen*

Als de cirkel in de meldingsknop naast elke gebeurtenisnaam naast Ja staat (met blauwe tint als achtergrond), is de melding ingeschakeld. Als de achtergrondkleur grijs is en de cirkel grenst aan Nee, is de melding uitgeschakeld.

Wanneer u een e-mailsjabloon op cursusniveau configureert, krijgt deze voor die specifieke cursus voorrang op de instellingen op beheerdersniveau.
