---
description: Lees dit artikel om te weten te komen hoe u de profielinstellingen van de student instelt en een profielfoto toevoegt. Leer hoe u het studenttranscript voor uw profiel kunt downloaden.
jcr-language: en_us
title: Profielinstellingen
contentowner: manochan
source-git-commit: a495c86f8dff3ebc51e7700a3f3bcf7ce57d1311
workflow-type: tm+mt
source-wordcount: '783'
ht-degree: 0%

---



# Profielinstellingen

Lees dit artikel om te weten te komen hoe u de profielinstellingen van de student instelt en een profielfoto toevoegt. Leer hoe u het studenttranscript voor uw profiel kunt downloaden.

## Profielinstellingen configureren {#configuringprofilesettings}

1. Klik in de rechterbovenhoek van de pagina op de vervolgkeuzepijl naast uw profiel of foto.
1. Selecteer Profielinstellingen.
1. In het pop-upvenster dat verschijnt, kunt u de volgende handelingen uitvoeren:

   * Profielfoto toevoegen/bijwerken: houd de muis boven de foto. Klik op Uploaden en voeg een foto toe. Klik op Bewerken om de foto te wijzigen.
   * Foto verwijderen: houd de muis boven de profielfoto. Klik op Verwijderen.
   * Voeg de inhoud Over mij toe door op het tekstgebied eronder te klikken.
   * Wijzig de inhoud van Over mij door op Bewerken naast het veld te klikken.
   * Stel de landinstelling voor uw profiel in. Selecteer in de vervolgkeuzelijst Landinstelling de taal van uw keuze.
   * Stel de huidige landinstelling voor uw profiel in.
   * Stel de tijdzone voor uw profiel in.
   * Download het Studenttranscript met uw gegevens.

   ![](assets/learner-preferences.png)
   *Voorkeuren voor studenten weergeven*

   Wanneer u op de link Mijn leertranscript-XLS downloaden klikt, wordt een Excel-blad naar uw systeem gedownload. Dit Excel-blad bevat gegevens over de leerobjecten die u hebt gebruikt, de voltooiingsstatus van elk leerobject, de bijbehorende vervaldatums, de behaalde vaardigheden enzovoort. Download dit blad om snel wat algemene gegevens voor uw leerprofiel te krijgen.

1. Als een beheerder Digest-e-mail heeft ingeschakeld en u niet in de DND-lijst staat, kunt u zich al dan niet abonneren op digest-e-mails. Schakel de onderstaande optie in.

   ![](assets/digest-email-option-learner.png)
   *Abonneren op of afmelden voor digest-e-mails*

   Op basis van de frequentie die door de beheerder is ingesteld, ontvangt de student het e-mailbericht elke twee weken of maandelijks.

## Abonnement op digest-e-mails opzeggen {#unsubscribefromdigestemails}

Als u een e-mail ontvangt, kunt u uw abonnement op de digest-e-mail opzeggen door op de knop **Abonnement opzeggen** onderaan in de e-mail.

Nadat u op **[!UICONTROL Abonnement opzeggen]**, wordt u omgeleid naar uw **Profielinstellingen** pagina, waar u de optie voor het ontvangen van e-mails kunt uitschakelen.

## Anatomie van een digest-e-mail {#anatomyofadigestemail}

Een overzicht-e-mail bestaat uit de volgende secties:

<table>
 <tbody>
  <tr>
   <td>
    <p><b>Sectie</b></p></td>
   <td>
    <p><b>Beschrijving</b></p></td>
  </tr>
  <tr>
   <td>
    <p>Persoonlijke trainingsoverzicht</p></td>
   <td>
    <p>In deze sectie worden de trainingsmetrics van een student gepersonaliseerd door het aantal minuten te vermelden dat aan trainingen is besteed.</p>
    <p>Op basis van de tijd die de student heeft doorgebracht, wordt de inhoud aangepast volgens de onderstaande regels:</p>
    <p>Als (time_bracht) &gt;= 60 minuten, dan verschijnt de volgende tekst:</p>
    <p><i>"In de afgelopen twee weken/1 maand hebt u <b>(tijd_besteed)</b> minuten training om uzelf te helpen. Hieronder staan enkele aanbevelingen waarmee u meer te weten kunt komen." </i></p>
    <p> Als (time_gebruikte) &lt; 60 minuten, wordt de volgende tekst weergegeven:</p>
    <p><i>"In de afgelopen twee weken/1 maand hebt u <b>(tijd_besteed)</b> minuten training om uzelf te helpen. Hieronder staan een paar aanbevelingen waarvan we hopen dat ze nuttig zijn om aan de slag te gaan."</i></p></td>
  </tr>
  <tr>
   <td>
    <p>Trainingsactiviteit</p></td>
   <td>
    <p>In deze sectie wordt een overzicht op organisatieniveau van de trainingsactiviteiten voor dat account weergegeven.</p>
    <p>Het overzicht van de trainingsactiviteiten bestaat uit: </p>
    <ul>
     <li>Aantal beschikbare trainingen in het account.</li>
     <li>Aantal co-studenten die actief hebben deelgenomen aan de trainingsactiviteiten.</li>
     <li>Aantal leeruren dat de medewerkers doorbrengen.</li>
     <li>Gemiddelde tijd (in minuten) besteed door medewerkers die het account upskilling.</li>
    </ul></td>
  </tr>
  <tr>
   <td>
    <p>Aanbevolen cursussen</p></td>
   <td>
    <p>Dit is een gepersonaliseerde sectie met de aanbevolen trainingen voor studenten. In deze sectie ziet een student drie trainingen die zijn gekozen door de engine voor aanbevelingen.</p>
    <p>Elke training heeft een knop Verkennen, die wanneer erop wordt geklikt, wordt omgeleid naar de startpagina van de Learner-app.  </p></td>
  </tr>
  <tr>
   <td>
    <p>Leaderboard</p></td>
   <td>
    <p>Hiermee wordt een staafdiagram weergegeven met elke balk die een student en gamificationpunten van elke student vertegenwoordigt (alleen als de beheerder Gamification voor alle studenten heeft ingeschakeld).</p>
    <p>Het leaderboard geeft het volgende weer:</p>
    <ul>
     <li>Punten verdiend door een student.</li>
     <li>Punten die nodig zijn om het volgende niveau te bereiken.</li>
    </ul>
    <p>Er is ook een mini-leaderboard met de leader en twee studenten die het dichtst bij de student staan in dat gebruikersbereik.</p>
    <p>Als het leaderboard leeg is, wordt deze sectie niet weergegeven in de e-mail.</p></td>
  </tr>
  <tr>
   <td>
    <p><a>Sociale berichten</a></p></td>
   <td>
    <p>In deze sectie worden de drie meest recente posts op social media weergegeven.</p>
    <p>Een student kan de aanmaakdatum, de boardnaam, de eventuele titel van het bericht, de gebruikersnaam en het pictogram van de maker zien. Het bericht kan ook een video, document, pdf of een ander bestand bevatten.</p>
    <p>Elk bericht heeft koppelingen om de student om te leiden naar de pagina Sociaal leren in de Learner-app.</p>
    <p>Als er geen recente berichten zijn, is deze sectie in de e-mail niet zichtbaar voor de student.</p></td>
  </tr>
 </tbody>
</table>

## Veelgestelde vragen {#frequentlyaskedquestions}

**1. Hoe kan ik een studenttranscript downloaden als student?**

Klik rechtsboven op uw **[!UICONTROL gebruikersprofiel]** > **[!UICONTROL Profielinstellingen]**. Klik in het dialoogvenster dat verschijnt op **Mijn leertranscript (XLS) downloaden**.

![](assets/dowload-lt.png)
*Studenttranscript downloaden*
