---
title: Adobe Learning Manager - Handleiding voor veilig beheer
description: In deze handleiding worden beveiligingsinstellingen, rollen en best practices voor het beheer van de administratieve beveiliging en toegangscontrole in Adobe Learning Manager beschreven om naleving en beveiliging te garanderen.
jcr-language: en-us
source-git-commit: 76a231b5d178a43a2e217d442481e6fd77f12390
workflow-type: tm+mt
source-wordcount: '2354'
ht-degree: 0%

---


# Administratieve beveiligingsinstellingen en gevolgen voor de beveiliging

## Administratieve rollen met gevolgen voor de beveiliging

Adobe Learning Manager gebruikt een op rollen gebaseerd toegangsbeheermodel (RBAC). In de volgende tabel worden FedRAMP-accountlagen toegewezen aan de ALM-rollen waarnaar in dit document wordt verwezen:

| FedRAMP Term | ALM-rol | Beveiligingsrelevantie |
|-------------|---------|------------------|
| Toonaangevende beheeraccount | Beheerder | Volledig beheer op accountniveau. Exclusieve toegang tot alle beveiligingsrelevante instellingen die in dit document worden beschreven. Dit is de rol waarnaar in deze handleiding wordt verwezen wanneer de term &#39;administratieve rekening van het hoogste niveau&#39; wordt gebruikt. |
| Geprivilegieerde account (bereik) | Aangepaste beheerder | Gedelegeerde beheertoegang die is ingesteld voor specifieke functies, gebruikersgroepen of catalogi. Kan geen toegang krijgen tot beveiligingsinstellingen op accountniveau, tenzij dit expliciet wordt toegestaan. |
| Geprivilegieerde account (integratie) | Integratiebeheerder | Beheert integraties, API-registraties en verbindingsconfiguraties. Verhoogde bevoegdheden binnen het bereik van integratiebeheer. Kan de beveiligingsinstellingen op accountniveau niet wijzigen. |

>[!NOTE]
>
>Alleen gebruikers aan wie deze rollen expliciet zijn toegewezen, kunnen instellingen voor beheer of beveiliging wijzigen. De instellingen die in secties 3-7 worden beschreven, zijn exclusief toegankelijk voor de beheerdersrol, tenzij anders vermeld.

## Aanmeldings- en verificatie-instellingen

De instellingen voor aanmelding en verificatie bepalen hoe alle gebruikers, inclusief beheerders, toegang krijgen tot het ALM-platform. Deze instellingen worden uitsluitend geconfigureerd door de beheerdersrol en hebben een directe en aanzienlijke invloed op de beveiligingspositie van het gehele account.

### Configuratie van de aanmeldingsmethode

**Plaats:** ALM Admin > Montages > Login Methoden

De beheerder beheert de verificatiemethode die wordt gebruikt voor alle interne en externe gebruikers. De volgende opties zijn beschikbaar:

- **Adobe ID:** de Gebruikers verifieert via hun persoonlijke rekening van de Adobe. Beheerd door Adobe, niet door de organisatie.
- **Enige Sign-On (SSO) via SAML 2.0:** De gebruikers verklaren zich via de identiteitsprovider van de organisatie (IdP) voor authentiek. De organisatie beheert volledig verificatie-, MFA- en sessiebeleid.
- **het Leren identiteitskaart van de Manager:** Beschikbaar voor externe slechts gebruikers. Gebruikers maken een platformspecifieke gebruikersnaam en wachtwoord.
- **Veelvoudige configuraties SSO:** tot 20 configuraties SSO kunnen worden toegevoegd om verschillende gebruikersgroepen, plaatsen, of organisatorische afdelingen te steunen

| Aanmeldingsmethode | Security Implication | Aanbeveling |
|-------------|---------------------|----------------|
| **Adobe ID** | Organisatie heeft geen controle over wachtwoordbeleid, MFA of accountherstel. Een gecompromitteerd account voor persoonlijke Adobe verleent toegang tot het ALM-platform. | **NIET AANBEVOLEN** voor administratieve of interne gebruikers. Alleen gebruiken als SSO niet beschikbaar is. |
| **SSO (SAML 2.0 / Federated ID)** | De verificatie wordt volledig beheerd door de IdP van de organisatie. MFA, sessietime-outs en beleid voor voorwaardelijke toegang worden afgedwongen op IdP-niveau. Onmiddellijke intrekking bij het verlaten van de gebruiker. | **AANBEVOLEN** voor alle interne gebruikers en beheerders. Biedt het hoogste niveau van organisatorische controle. |
| **het Leren identiteitskaart van de Manager** | Gebruikers kunnen zelf wachtwoorden beheren buiten de identiteitsinfrastructuur van de organisatie. Kan MFA niet via ALM afdwingen. De sterkte van het wachtwoord hangt af van het gedrag van de gebruiker. | Alleen acceptabel voor externe gebruikers. Niet geschikt voor werknemers of beheerders. |

>[!CAUTION]
>
>Als de aanmeldingsmethode voor interne gebruikers is ingesteld op Adobe ID, kan de organisatie niet langer multifactorverificatie afdwingen, de complexiteit van wachtwoorden regelen of de toegang onmiddellijk intrekken wanneer een gebruiker verlaat. Dit verhoogt het risico op ongeoorloofde toegang aanzienlijk.

Zie [ de rollen van de Douane ](https://experienceleague.adobe.com/en/docs/learning-manager/using/admin/custom-role) voor meer informatie.

### Multi-Factor Authentication (MFA)

**Plaats:** Adobe Admin Console > Montages > Privacy en Veiligheid > de Montages van de Authentificatie

MFA handhaving voor **Adobe ID** en **Enterprise ID** gebruikers wordt gevormd door de **Beheerder van het Systeem** in Adobe Admin Console, niet binnen de toepassing ALM zelf.  Voor **Federated ID/SSO** gebruikers, wordt MFA afgedwongen bij de identiteitsleverancier van de organisatie.

- **Afgedwongen 2FA:** de gebruikers kunnen geen controle onbruikbaar maken in twee stappen. Biedt een sterke bescherming tegen diefstal van referenties en phishing.
- **Facultatieve 2FA:** de gebruikers kiezen of om controle in twee stappen toe te laten. Een aanzienlijk zwakkere beveiligingspositie.
- **MFA niet gevormd:** Wachtwoorden alleen beschermen toegang. Hoge risico&#39;s, met name voor administratieve rekeningen.

>[!IMPORTANT]
>
>Administratieve rekeningen zonder gedwongen MFB lopen een aanzienlijk hoger risico op ongeoorloofde toegang. Een aangetaste beheerdersreferentie zonder MFA biedt volledige accountcontrole, inclusief de mogelijkheid om alle beveiligingsinstellingen te wijzigen.

### Sessielevensduur en inactieve time-out

**Plaats:** Adobe Admin Console > Montages > Privacy en Veiligheid > Geavanceerde Montages

De **Beheerder van het Systeem** vormt het maximum actieve zittingsleven en de nutteloze zittingsonderbreking voor de organisatie. Deze instellingen zijn van toepassing op alle gebruikers, inclusief beheerders.

- **Max het Leven van de Zitting:** Forces re-authentificatie na een bepaalde periode ongeacht activiteit. Hiermee beperkt u het opportuniteitsvenster wanneer een sessie wordt gecompromitteerd.
- **Max Niet-actieve Tijd:** beëindigt zittingen die voor een bepaalde periode inactief zijn geweest. Hiermee beschermt u tegen onbeheerde geverifieerde sessies op gedeelde of ontgrendelde apparaten.

## Instellingen voor roltoewijzing en bevoegdheidsbereik

De instellingen voor roltoewijzing en machtigingsbereik bepalen wie beheertoegang heeft in ALM en wat ze kunnen doen. Deze behoren tot de beveiligingsinstellingen met de grootste impact op het platform. Alleen de beheerdersrol kan beheerdersrollen maken, toewijzen, wijzigen of intrekken.

### Toewijzing administratieve rol

**Plaats:** ALM Admin > Gebruikers > Intern > Acties > Rol toewijzen / Rol verwijderen

De **Beheerder** kan de volgende rollen verlenen of intrekken:

- **Beheerder:** Volledige toegang op account-niveau
- **Auteur:** toegang van de inhoudsverwezenlijking
- **Beheerder van de Douane:** Reeks administratieve toegang (zie Sectie 4.2)
- **de Beheerder van de Integratie:** Integratie en API toegang (zie Sectie 7)

| Instellen / Handeling | Security Implication | Aanbevolen praktijk |
|---|---|---|
| **het verlenen van de rol van de Beheerder** | Volledig accountbeheer. Een gebruiker met deze rol kan alle instellingen in dit document wijzigen, inclusief het opnieuw configureren van verificatie en het intrekken van de toegang van andere beheerders. | Wijs slechts aan een minimumaantal gebruikers met een geverifieerde bedrijfsbehoefte toe. Bewaar een gedocumenteerde lijst van alle beheerders-rolhouders. |
| **verzuimend om rollen op vertrek terug te trekken** | Uitgeschakelde gebruikers behouden de toegang tot beheerfuncties. Risico van ongeoorloofde toegang, data-exfiltratie of sabotage. | Verwijder rollen onmiddellijk wanneer de werk- of administratieve verantwoordelijkheden van een gebruiker veranderen. Voer periodieke toegangsbeoordelingen uit. |
| **over-het toewijzen van brede rollen** | Brede administratieve toegang vergroot de potentiële impact van een gecompromitteerd account en vermindert de verantwoordingsplicht voor administratieve handelingen. | Pas het principe van minst bevoorrecht toe. Voorkeur voor bereikrollen (bijvoorbeeld Aangepaste beheerder) waar mogelijk. |

### Configuratie van aangepaste beheerdersrollen

**Plaats:** ALM Admin > Gebruikers > de Rollen van de Douane > creëren Rol

Pas het beginsel van **minste voorrecht** toe. Gebruik **rollen van de Beheerder van 0} Douane aan afgevaardigde specifieke functies (zie Sectie 4.2).**

De **Beheerder** kan douanerollen tot stand brengen die een bepaalde ondergroep van administratieve toestemmingen verlenen. Aangepaste rollen kunnen worden beperkt tot specifieke gebruikersgroepen, catalogi of functiesets, waardoor het bereik van gedelegeerde beheertoegang wordt beperkt.

**Beschikbare toestemmingscategorieën omvatten:**

- **de voorrechten van de Rekening:** Toegang tot configuraties voor het hele systeem zoals aankondigingen, gamification, vaardigheden, en gebruikersbeheer.
- **de voorrechten van de Eigenschap (kern):** Toegang tot catalogi, rapporten, en markeringen.
- **de voorrechten van de Eigenschap (het leren voorwerpen):** Toegang tot cursussen, certificeringen, het leren wegen, en taakhulpmiddelen.
- **Reikwijdte:** Beperk de rol tot specifieke gebruikersgroepen en/of catalogi.

| Configuratiebesluit | Security Implication | Aanbevolen praktijk |
|---|---|---|
| **Creërend een te brede douanefunctie** | Een aangepaste rol met bovenmatige bevoegdheden biedt weinig zekerheid over de volledige beheerdersrol en vergroot de blastaire straal van een gecompromitteerd account. | Bereik aangepaste rollen tot de minimale set machtigingen die nodig is voor de specifieke functie. Voorkeur voor rollen met het bereik van catalogi en gebruikersgroepen. |
| **het verlenen van de toegang van Montages tot een douane admin** | Aangepaste beheerders met Settings-toegang kunnen aanmeldingsmethoden, meldingsinstellingen en andere configuraties op accountniveau wijzigen. | Bied Settings alleen toegang tot aangepaste rollen wanneer dit expliciet is vereist. Controleer regelmatig welke aangepaste rollen dit voorrecht hebben. |
| **controleert de geen taken van de douanerol** | Niet-gedocumenteerde of niet-gereviseerde aangepaste rollen kunnen zich in de loop van de tijd ophopen, wat leidt tot kneep met bevoegdheden. | Download periodiek het Rapport van de Rol van de Douane (**Gebruikers > de Rollen van de Douane > Download**) en herzie alle actieve taken van de douanerol. |

## Gebruikerprovisioning en instellingen voor toegangsbeheer

De instellingen voor gebruikersprovisioning bepalen hoe gebruikers aan het platform worden toegevoegd, hoe lang ze actief blijven en wanneer hun gegevens worden verwijderd. Deze instellingen worden uitsluitend geconfigureerd door de beheerdersrol en hebben directe gevolgen voor de beveiliging van de gegevensblootstelling en het toegangsbeheer.

| Instelling | Locatie | Security Implication | Aanbevolen standaard |
|---|---|---|---|
| **Inactieve gebruiker automatisch-schrapping** | ALM Admin > Settings > General | Zonder automatische verwijdering accumuleren inactieve accounts. Mislukte accounts vormen een gemeenschappelijk doel voor ongeoorloofde toegang, omdat ze mogelijk niet worden gecontroleerd. | Inschakelen. Stel een retentieperiode in die overeenkomt met het organisatiebeleid (bijvoorbeeld 90 dagen inactiviteit). |
| **Externe het verstrijken van het gebruikersprofiel** | ALM-beheerder > Gebruikers > Extern > Profiel toevoegen | Externe gebruikersprofielen zonder vervaldatum blijven voor onbepaalde tijd toegankelijk. Partners of contractanten die geen toegang meer nodig hebben, behouden een actief ingangspunt. | Stel een vervaldatum in voor elk extern gebruikersprofiel tijdens het maken. |
| **zelfregistratie verbindingscontroles** | ALM-beheerder > Gebruikers > Intern > Toevoegen > Zelfregistratie | Met een zelfregistratielink kan elke gebruiker met de URL een studentaccount maken. Als deze optie niet wordt beheerd, kan dit ertoe leiden dat onbevoegde of onverwachte gebruikers platformtoegang krijgen. | Genereer alleen zelfregistratielinks als dat nodig is. Ongebruikte koppelingen direct uit- of intrekken. |
| **Externe profielpauze/hervat** | ALM Admin > Users > External > Actions > Pause | Als u een extern profiel pauzeert, voorkomt u dat nieuwe gebruikers zich registreren, maar dit heeft geen invloed op gebruikers die al zijn geregistreerd. Als inactieve externe profielen niet worden gepauzeerd, kunnen ongewenste registraties worden toegestaan. | Pauzeer externe profielen wanneer registratie niet meer nodig is. Verwijder profielen die permanent inactief zijn. |
| **de schrapping en zuivering van de Gebruiker** | ALM Admin > Users > Internal > Actions > Delete / User Cleanup > Leegmaken | Verwijderde gebruikers worden gedeactiveerd, maar hun gegevens blijven behouden. Bij leegmaken worden alle gebruikersgegevens definitief verwijderd. Als vertrekkende gebruikers niet worden leeggemaakt, kunnen gevoelige leerrecords en PII na de vereiste retentieperiode worden bewaard. | Wis gebruikersrecords in overeenstemming met het beleid voor het bewaren van organisatiegegevens en privacy. Leegmaken is onomkeerbaar. |

>[!IMPORTANT]
>
>Leegmaken is permanent en onomkeerbaar. Alle leerrecords, inschrijvingsgegevens en gebruikersgegevens worden verwijderd. Als er in verbindingsconfiguraties wordt verwezen naar een leeggemaakte gebruiker, worden deze connectoren uitgeschakeld. Bevestig de selectie zorgvuldig voordat u leegmaakt.

## Instellingen voor rapportage en gegevenstoegang

Met instellingen voor rapportage en gegevenstoegang bepaalt u welke gebruikers platformgegevens kunnen weergeven, genereren en exporteren. Een verkeerde configuratie van deze instellingen kan leiden tot de blootstelling aan gevoelige persoonlijke, organisatorische of nalevingsgerelateerde informatie.

| Instelling | Locatie | Security Implication | Aanbevolen standaard |
|---|---|---|---|
| **het verlenen van rapporttoegang tot douanerollen** | ALM-beheerder > Gebruikers > Aangepaste rollen > Functiebevoegdheden > Rapporten | Rapporten kunnen persoonlijk identificeerbare informatie (PII), gegevens over het voltooien van een cursus, beoordelingsscores en de voortgang van de student bevatten. Toegang tot rapportagefuncties moet beperkt blijven tot gebruikers met een geverifieerde zakelijke behoefte. | Toegang tot rapporten alleen verlenen voor rollen met een specifieke, gedocumenteerde behoefte. Gebruik alleen-lezen-toegang wanneer schrijftoegang niet vereist is. |
| **Volledige Controle vs. lezen slechts rapportwerkingsgebied** | ALM-beheerder > Gebruikers > Aangepaste rollen > Accountoverzichtsrapport | Met Volledig beheer van het accountoverzichtsrapport krijgt de aangepaste beheerder inzicht in alle gebruikersgroepen en catalogi, ongeacht het rolbereik. Dit kan gegevens buiten het beoogde bereik van een beheerdersrol blootstellen. | Verleen Volledig Controle op het Rapport van de Samenvatting van de Rekening slechts aan rollen die echt organisatie-breed rapporterend zicht vereisen. |
| **xAPI en e-mailrapporttoegang** | ALM-beheerder > Gebruikers > Aangepaste rollen | xAPI-rapporten en e-mailrapporten zijn alleen beschikbaar voor de volledige beheerdersrol. Deze rapporten kunnen gedetailleerde gedrags- en communicatiegegevens bevatten. Toegang is beperkt door ontwerp. | Probeer niet xAPI- of e-mailrapporttoegang te delegeren via aangepaste rollen. Dit zijn alleen beheerders. |
| **Geëxporteerde gebruikersgegevens** | ALM-beheerder > Gebruikers > Intern > Gebruikersgegevens exporteren | De functie Gebruikersgegevens exporteren genereert een downloadbaar bestand met alle interne gebruikersrecords. Deze gegevens moeten worden verwerkt in overeenstemming met het beveiligingsbeleid en het privacybeleid van de organisatie. | Exportmogelijkheden beperken tot bevoegd personeel. Geëxporteerde gegevens behandelen als gevoelig. Bewaren of verzenden niet buiten goedgekeurde systemen. |

## Instellingen voor integratie en API-toegang

De instellingen voor integratie en API-toegang bepalen hoe externe systemen verbinding maken met Adobe Learning Manager. Deze instellingen breiden de toegang uit tot buiten de ALM-gebruikersinterface en kunnen, indien verkeerd geconfigureerd, platformgegevens en -functionaliteit beschikbaar maken voor niet-geautoriseerde systemen.  Integratie-instellingen worden beheerd door de integratiebeheerder. Met de volledige beheerdersrol kunt u geregistreerde toepassingen beoordelen, goedkeuren en intrekken.

| Instelling | Locatie | Security Implication | Aanbevolen standaard |
|---|---|---|---|
| **API toepassingsregistratie** | Integratiebeheerder > Toepassingen > Registreren | Bij het registreren van een toepassing worden OAuth 2.0-referenties (client-id en geheim) gemaakt waarmee via programmacode toegang kan worden verkregen tot ALM-gegevens en -functies. Te brede OAuth-bereiken (bijvoorbeeld lezen/schrijven van de beheerdersrol) bieden volledige beheer-API-toegang. | Verleen het minimaal vereiste OAuth-bereik. Reviseer en herhaal periodiek niet-gebruikte of verouderde toepassingsregistraties. Behandel de aanmeldingsgegevens van de client als vertrouwelijke gegevens. |
| **OAuth toepassingswerkingsgebied** | Integratiebeheerder > Toepassingen > Registreren > Bereiken | Het beschikbare OAuth-bereik varieert van leestoegang tot leestoegang van de student tot lees- en schrijftoegang van de beheerder. Met de lees- en schrijfrol van de beheerder kan een toepassing alle gegevens wijzigen die een beheerder kan wijzigen, inclusief gebruikersrollen en beveiligingsinstellingen. | Gebruik het meest restrictieve OAuth-bereik dat voldoet aan de vereisten van de integratie. Bied de beheerdersrol nooit lees- en schrijftoegang tenzij strikt noodzakelijk. |
| **Configuratie van de Verbinding (FTP, Salesforce, HRIS, enz.)** | Integratiebeheerder > Connectoren | Connectoren maken het automatisch importeren en exporteren van gebruikersgegevens, vaardigheden en cursusvoltooiing mogelijk. Niet-geconfigureerde connectoren kunnen onjuiste gebruikersgegevens importeren, onbedoelde rollen toewijzen of gevoelige gegevens exporteren naar onbevoegde doelen. | Bekijk regelmatig alle actieve verbindingsconfiguraties. Zorg ervoor dat databronnen en -bestemmingen zijn geautoriseerd. Schakel connectoren uit die niet meer in gebruik zijn. |
| **configuratie van de Webhook** | Integratiebeheerder > Webhooks | Webhooks verzenden real-time ALM-gebeurtenisgegevens (inschrijvingen, voltooiing, gebruikerswijzigingen) naar een opgegeven externe URL. Een onjuist geconfigureerd of gecompromitteerd webhook eindpunt kan leiden tot gegevensexfiltratie of blootstelling aan gevoelige studentgebeurtenissen. | Registreer alleen geverifieerde, door de organisatie goedgekeurde webhook-URL&#39;s. Bekijk regelmatig actieve webhookconfiguraties. Verwijder inactieve of niet-herkende webhooks direct. |
| **LTI integratieconfiguratie** | Integratiebeheerder > LTI-integraties | Dankzij LTI-integratie kan ALM optreden als LTI-provider of als consument, waardoor externe LMS-platforms toegang hebben tot ALM-cursussen. Als deze optie eenmaal is ingeschakeld, kan LTI niet worden uitgeschakeld. De blootgestelde geloofsbrieven van LTI kunnen onbevoegde toegang tot cursusinhoud toestaan. | Schakel LTI alleen in als er een geverifieerde integratievereiste bestaat. Behandel LTI-aanmeldgegevens als gevoelig. U kunt alleen referenties delen met geautoriseerde LMS-beheerders. |

## Beheerdersconfiguratiemogelijkheden en gedeelde verantwoordelijkheid

De administratieve montages in Adobe Learning Manager zijn configureerbaar door klanten en maken deel uit van de klant-geleide veiligheidscontroles onder het gedeelde verantwoordelijkheidsmodel van de Adobe.

| Verantwoordelijkheden Adobe | Verantwoordelijkheden klant |
|---|---|
| Veilige werking van het ALM-platform en de onderliggende infrastructuur. | Configuratie van alle administratieve rollen en machtigingen. |
| Handhaving van het rolgebaseerde toegangsbeheermodel. | Aangepaste aanmeldingsmethoden en MFA selecteren en afdwingen. |

Aanvullende informatie over de beveiligingsmethoden van Adobe Learning Manager is beschikbaar in:

**Verwijzing:** [ het Overzicht van de Veiligheid van Adobe Learning Manager (PDF) ](https://experienceleague.adobe.com/docs/learning-manager/assets/alm-security-whitepaper-2024.pdf)

## Documentonderhoud

Dit document kan periodiek worden bijgewerkt om de wijzigingen in Adobe Learning Manager-functionaliteit of beveiligingsrichtlijnen te weerspiegelen. De versie en de datum die het laatst is bijgewerkt, blijven behouden in de metagegevens van het document en in het FedRAMP-autorisatiepakket. Klanten dienen de openbaar beschikbare versie op Adobe Experience League te raadplegen om ervoor te zorgen dat ze de meest actuele richtlijnen gebruiken.

