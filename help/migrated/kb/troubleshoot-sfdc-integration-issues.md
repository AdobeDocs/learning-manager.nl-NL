---
jcr-language: en_us
title: Salesforce (SFDC)-integratieproblemen met Adobe Learning Manager oplossen
description: Algemene Salesforce-integratieproblemen (SFDC) met Adobe Learning Manager (ALM) oplossen, zoals niet-geëxporteerde bestanden, problemen met veldmachtigingen in aangepaste SFDC-objecten en belangrijke opmerkingen over SFDC-ALM-compatibiliteit.
contentowner: saghosh
source-git-commit: c57896abd8f00ca4a7b26c981eb490cd53ce437b
workflow-type: tm+mt
source-wordcount: '587'
ht-degree: 0%

---


## Problemen met exporteren naar SFDC oplossen (geen export meer dan 2-3 uur)

Als de uitvoer SFDC niet met succes meer dan **2-3 uren** heeft voltooid, gebruik de stappen hieronder om de kwestie te identificeren en te begrijpen.

1. Ga naar de **Startpagina van Salesforce**.
2. In het **Snelle de onderzoeksvakje van de Vondst**, type **`Bulk Data Load Jobs`** en open het.
3. De pagina toont bulkgegevenstaken voor de **laatste 7 dagen**.
4. Zoek banen met betrekking tot **Adobe Learning Manager (ALM) voorwerpen**.
5. Klik op de specifieke taak die u wilt onderzoeken.
6. De rol aan de **bodem** van de pagina van het taakdetail om het **foutenbericht** en extra details te bekijken.

In veel gevallen, is de worteloorzaak **ontoereikende gebied-vlakke toestemmingen in SFDC**. De naam van het falende veld kan er als volgt uitzien:

- `cp_Module_ID`
- of andere `cp_...` -velden die verwant zijn aan aangepaste ALM-objecten.

Als dergelijke velden worden weergegeven in de fout, gaat u verder naar de volgende sectie.

## Veldmachtigingen verlenen voor aangepaste ALM-objectvelden in SFDC

Gebruik de **eigenschap van de Toegankelijkheid van het Gebied** om toestemmingskwesties op specifieke gebieden (bijvoorbeeld, `cp_Module_ID`) te bevestigen.

### Stappen

1. Ga naar de **Startpagina van Salesforce**.
2. In het **Snelle de onderzoeksvakje van de Vondst**, type **`Field Accessibility`** en open het.
3. Van de lijst van voorwerpen, selecteer het relevante **rapporttype/voorwerp**.
   - Voorbeeld: `cp_LearnerTranscript_xxxx_xxxx` voor het LT-rapport (Studenttranscript).
4. Voor de volgende pagina, kies **&quot;Mening door gebieden&quot;**.
5. In het **gebied drop-down**, selecteer het gebied dat in de uitvoerfout verscheen
   - Voorbeeld: `cp_Module_ID` .
6. In de toegangsmatrijs, klik **&quot;Verborgen&quot;** ingang voor het **profiel van de Beheerder van het Systeem** (en andere relevante profielen, indien nodig).
7. Op de volgende pagina:
   - Laat **&quot;Zichtbaar&quot;** toe waar aangewezen.
   - Klik **sparen** bij de bodem van de pagina.
8. Na het opslaan gaat u terug naar de weergave voor toegankelijkheid van het veld. Het gebied zou nu als **&quot;Editable&quot;** voor **Beheerder van het Systeem** (en om het even welke andere profielen moeten tonen u) bijwerkte.

## Herhaal deze bewerking voor alle betrokken velden en probeer het exporteren opnieuw

1. **herhaal** de stappen van de gebiedstoegankelijkheid in sectie 2 voor **elk gebied** dat als het hebben van toestemmingskwesties in **de Banen van de Lading van Gegevens** wordt gemeld.
2. Zodra alle problematische velden de juiste zichtbaarheid en bewerkingsmachtigingen hebben:
   - Ga terug naar **Adobe Learning Manager**.
   - In de **configuratie van de 1&rbrace; schakelaar SFDC,** probeer de uitvoer **opnieuw.**


## Belangrijke opmerkingen en beperkingen

Houd rekening met deze SFDC-ALM-specifieke kenmerken wanneer u integraties ontwerpt of problemen oplost.

### Geen automatisch object/veld maken in SFDC

- De **schakelaar SFDC leidt tot geen nieuwe voorwerpen of gebieden in Salesforce**.
- Als het a **nieuwe gebied in ALM** wordt toegevoegd en u wilt het in SFDC verschijnen:
   - Handmatig **creeer het overeenkomstige douanegebied** in SFDC.
   - **Kaart** het SFDC douanegebied aan het **aangewezen ALM gebied** in de schakelaarconfiguratie.
   - Verzeker het nieuwe gebied **juiste gebied-vlakke toestemmingen** (gebruiks sectie 2) heeft.

### Callback-URL voor ALM-accounts met aangepaste domeinen

- Als de rekening ALM a **douanedomein** gebruikt, moet het technische team **toevoegen dat douanedomein** aan de **callback URL allowlist** voor de OAuth productie-app van de schakelaar SFDC.
- Dit wordt gedaan via a **verzoek van Jira** aan techniek.
- Zonder dit, kan de stroom OAuth voor de schakelaar ontbreken.

### Tijdzonebeperking (alleen UTC)

- Als de organisatie SFDC a **tijdzone buiten UTC** gebruikt, **voltooiing en inschrijvingsgegevens kunnen worden gemist** tijdens synchronisatie.
- Reden: ALM **steunt momenteel slechts de UTC tijdzone** voor integratie SFDC.
- Interne referentie: PAPI-24525 wordt verhoogd om extra tijdzones te ondersteunen.

### Datatype-beperking filteren (picklist versus checklist)

- ALM steunt het invoeren **filters SFDC die met picklist gebieden** worden gecreeerd.
- ALM **steunt** geen filters die op checklist/multi-select checkbox gebieden worden gebaseerd.
- Reden: ALM **steunt slechts koorddatatypes** voor filters SFDC.
