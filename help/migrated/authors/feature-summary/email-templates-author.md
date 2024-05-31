---
description: Lees dit artikel om te weten te komen hoe u e-mailsjablonen kunt configureren voor gebeurtenissen die betrekking hebben op alle leerobjecten.
jcr-language: en_us
title: E-mailsjablonen
exl-id: 3b17f889-52be-4073-ab91-7c76dd79f1d2
source-git-commit: 6862dc1958a34a369f0e0e7218f28151a47beb3b
workflow-type: tm+mt
source-wordcount: '475'
ht-degree: 72%

---

# E-mailsjablonen

Lees dit artikel om te weten te komen hoe u e-mailsjablonen kunt configureren voor gebeurtenissen die betrekking hebben op alle leerobjecten.

Learning Manager-toepassing verstuurt e-mailnotificaties naar meerdere gebruikersrollen gebaseerd op gebeurtenissen.

Als auteur kunt u e-mailsjablonen aanpassen door inhoud toe te voegen of te wijzigen en meldingen naar gebruikers te sturen voor verschillende gebeurtenissen die door activiteiten van studenten, managers en auteurs worden geactiveerd. U kunt bijvoorbeeld een aangepaste e-mail sturen wanneer een student zich inschrijft voor uw cursus. Na de inschrijving ontvangt de student automatisch de cursusspecifieke e-mail.

U kunt er ook voor kiezen om voor bepaalde gebeurtenissen geen e-mailnotificaties te versturen door de optie voor het e-mailsjabloon uit te schakelen.

## E-mailmeldingen configureren {#settingemailnotifications}

1. Selecteer in de auteurstoepassing het leerobject waarvoor u de e-mailsjabloon wilt configureren. Cursussen, bijvoorbeeld.

1. Klik vanuit de pagina Leerobject op de cursus, de certificering of het leerprogramma waarvoor u de e-mailinstellingen wilt configureren.

1. Selecteer op de pagina met leerobjectdetails de optie **E-mailsjablonen** > **Alle sjablonen**. E-mailsjablonen zijn beschikbaar voor **Standaardinstantie** en **Huidige cursus**. U kunt schakelen tussen de twee met behulp van het vervolgkeuzemenu rechtsboven.

   U kunt de lijst met sjablonen zien die beschikbaar zijn voor het leerobject dat u hebt gekozen.

   ![](assets/email-templates-forlearningprograms.png)
   *Lijst met sjablonen*

1. Klik op de naam van de gebeurtenis om de sjabloon in de voorbeeldmodus te bekijken.

   ![](assets/preview-the-emailtemplateforyourlearningobject.png)

   *Zie voorbeeld sjabloon*

   U kunt elke sjabloon aanpassen door op de tekst in de hoofdtekst van de sjabloon te klikken. U kunt variabelen in de tekst invoegen door op de toepasselijke pictogrammen te klikken, zoals te zien in de afbeelding. Beweeg uw muis over elk pictogram om de namen te bekijken.

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

   U kunt het bericht op de standaardinhoud terugzetten door op Origineel herstellen boven het sjabloon te klikken.

   Zoals u boven aan de sjabloon ziet, kunt u de sjabloon voor meerdere rollen aanpassen (manager, student, enzovoort), afhankelijk van het type e-mailmelding.

1. Klik op Opslaan onderaan de pagina met sjablonen.
1. Klik op de pagina E-mailsjablonen op de schuifknop Ja/Nee om de melding te verzenden of uit te schakelen.

![](assets/email-notification-e1437624109719.png)
*E-mailmelding in- of uitschakelen*

Als de schuifknop bij elke gebeurtenisnaam naast Ja staat (blauwe achtergrond), is de melding ingeschakeld. Staat de knop naast Nee (grijze achtergrond), dan is de melding uitgeschakeld.

Wanneer u op cursusniveau een e-mailsjabloon configureert, krijgt deze sjabloon voor die specifieke cursus voorrang op instellingen op beheerdersniveau.

## E-mailsjablooninstellingen

De auteur kan het volgende instellen in de instellingen van de e-mailsjabloon:

* **E-mailbanner**: Hiermee kunt u de e-mailbanner wijzigen.

* **E-mailhandtekening**: Hiermee kunt u de e-mailhandtekening toevoegen of bewerken.
