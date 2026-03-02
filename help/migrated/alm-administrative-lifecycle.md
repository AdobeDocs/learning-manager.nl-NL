---
title: Levenscyclus van administratieve account voor Adobe Learning Manager
description: Dit document biedt uitgebreide richtlijnen voor het veilig beheren van administratieve accounts van het hoogste niveau in Adobe Learning Manager (ALM) om te voldoen aan de FedRAMP-standaarden en best security practices.
jcr-language: en-us
source-git-commit: db3ed4dc44da75b418e923999bdf3776bf81b11f
workflow-type: tm+mt
source-wordcount: '2122'
ht-degree: 0%

---


# Beheerdersaccounttypen in Adobe Learning Manager

## ALM-roltoewijzing

In Adobe Learning Manager is de beheerdersrol de bovenste beheerdersaccount. Dit is de rol waarnaar wordt verwezen wanneer in deze handleiding de FedRAMP-term &#39;administratieve account op hoofdniveau&#39; wordt gebruikt. Aangepaste beheerders en integratiebeheerders worden behandeld als geprivilegieerde (bereikbare) accounts.

In de onderstaande tabel worden FedRAMP-accountlagen toegewezen aan de specifieke rollen die in Adobe Learning Manager worden gebruikt:

| FedRAMP Term | ALM Rolnaam | Beschrijving |
|--------------------------------------|----------------------------|-------------|
| Toonaangevende beheeraccount | Beheerder | Rol met de hoogste bevoegdheden in ALM. Volledige controle over gebruikers, rollen, leerinhoud, rapportage, integraties en alle systeemconfiguraties. Hiermee wordt rechtstreeks toegewezen aan de FedRAMP-definitie voor beheeraccounts op hoofdniveau. |
| Geprivilegieerde account (bereik) | Aangepaste beheerder | Een gedefinieerde subset van beheerdersmachtigingen die is ingesteld voor specifieke functies (bijvoorbeeld rapportage, catalogusbeheer). Heeft geen volledige controle op accountniveau. |
| Geprivilegieerde account (integratie) | Integratiebeheerder | Beheert integraties en API-gebaseerde toegang tussen ALM en externe systemen. Verhoogde bevoegdheden die alleen zijn bedoeld voor integratiebeheer. |


Adobe Learning Manager gebruikt een op rollen gebaseerd toegangsbeheermodel (RBAC) om administratieve toegang te beheren. Administratieve rollen worden alleen toegewezen door geautoriseerde beheerders.

Zie [&#x200B; de rollen van de Douane in Adobe Learning Manager &#x200B;](https://experienceleague.adobe.com/nl/docs/learning-manager/using/admin/custom-role) voor meer informatie

## Identiteitstypen en aanbevolen verificatie

Adobe Admin Console ondersteunt drie identiteitstypen voor beheeraccounts. De keuze van het type identiteit heeft directe gevolgen voor de beveiliging:

| Identiteitstype | Beschrijving | Beveiligingsaanbeveling |
|---------------------------|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| Adobe ID (persoonlijke id) | Standaardtype; beheerd door Adobe. Iedereen kan er een maken. | NIET AANBEVOLEN voor beheerders. De organisatie heeft geen controle over dit accounttype. |
| Enterprise ID | Het account dat eigendom is van een Admin Console, wordt beheerd door de systeembeheerder. | Accepteerbaar als Federated ID/SSO niet beschikbaar is. 2FA afdwingen. |
| Federated ID (SSO) | Org-owned; geïntegreerd met SAML 2.0 SSO. Organisatie beheert verificatie volledig. | AANBEVOLEN. Verifieert via IdP van organisatie; ondersteunt MFA-handhaving op het niveau van de identiteitsleverancier. |

Zie het volgende voor meer informatie:

* [Identiteitstypen](https://helpx.adobe.com/nl/enterprise/using/admin-console.html)
* [Gebruikersverificatie en wachtwoorden beveiligen](https://helpx.adobe.com/nl/enterprise/using/authentication-settings.html)

## Roltoewijzing en toegangsbeheer

De toegang tot administratieve rekeningen in Adobe Learning Manager wordt gecontroleerd door expliciete [&#x200B; roltoewijzing &#x200B;](https://experienceleague.adobe.com/nl/docs/learning-manager/using/admin/user-management/add-users-user-groups) door een bestaande beheerder. De belangrijkste kenmerken van veilige administratieve toegang zijn:

* Administratieve rollen worden alleen toegewezen door geautoriseerde beheerders.
* Toegang is op rollen gebaseerd en is afhankelijk van toegewezen machtigingen.
* Organisaties zijn verantwoordelijk voor het beperken van administratieve toegang tot gebruikers met een legitieme bedrijfsbehoefte.

Adobe raadt klanten aan om de beheerstoegang regelmatig te evalueren om ervoor te zorgen dat het beginsel van het minst bevoorrecht wordt nageleefd.

## Multifactorverificatie (MFA) afdwingen

Adobe raadt beheerders ten zeerste aan verificatie in twee stappen (2FA) in de hele organisatie af te dwingen. MFA is van toepassing op Enterprise ID- en Adobe ID-gebruikers. Federated ID-gebruikers moeten MFA afdwingen bij de identiteitsprovider van hun organisatie.

2FA afdwingen in de Adobe Admin Console:

1. Aanmelden bij de Adobe Admin Console.
2. Ga naar Instellingen > Privacy en beveiliging > Verificatie-instellingen.
3. Schakel in twee stappen verificatie in en selecteer de optie Afdwingen om te voorkomen dat gebruikers deze uitschakelen.
4. Configureer desgewenst op IP gebaseerde toegangsbeperkingen en geavanceerde sessieinstellingen (Max Session Life / Max Idle Time).

>[!IMPORTANT]
>
>Adobe raadt aan 2FA af te dwingen en deze niet voor gebruikers optioneel te laten. 2FA kan tot 24 uur duren. Voor Federated ID-gebruikers moet u MFA afdwingen bij uw identiteitsprovider.

Zie [&#x200B; Veilige gebruikersauthentificatie voor meer informatie &#x200B;](https://helpx.adobe.com/nl/enterprise/using/authentication-settings.html) voor meer informatie.


## Aanmelden als beheerder

ALM [&#x200B; Beheerders &#x200B;](https://experienceleague.adobe.com/nl/docs/learning-manager/using/get-started/getting-started-admin) onderteken binnen rechtstreeks aan het platform ALM gebruikend organisatorische geloofsbrieven die door de Admin Console worden beheerd.

### Een beheerdersrol toewijzen

Binnen het platform ALM, vormen de beheerders administratieve toegang door rollen te creëren en te beheren, toestemmingen aan gebruikers toe te wijzen, en toestemmingswerkingsgebied te bepalen dat op operationele verantwoordelijkheden wordt gebaseerd.

De beheerdersrol in ALM toewijzen:

1. Meld u als bestaande beheerder aan bij Adobe Learning Manager.
2. Navigeer naar Gebruikers > Intern.
3. Zoek naar of selecteer de doelgebruiker.
4. Selecteer Acties > Rol toewijzen > Beheerder maken.

Met aangepaste beheerrollen kunnen klanten beheertaken delegeren terwijl ze de gecentraliseerde controle over bevoegdheden op accountniveau behouden. Aangepaste beheerders kunnen het bereik bepalen van specifieke gebruikersgroepen of catalogi.

Zie [&#x200B; gebruikers en gebruikersgroepen &#x200B;](https://experienceleague.adobe.com/nl/docs/learning-manager/using/admin/user-management/add-users-user-groups) voor meer informatie toevoegen.

## Aanmeldingsmethoden en SSO configureren

ALM-beheerders beheren de aanmeldingsmethoden die beschikbaar zijn voor alle gebruikers via Instellingen > Aanmeldingsmethoden, een kritieke configuratie die relevant is voor de beveiliging:

* **Interne gebruikers**: plaats login wijze aan Adobe ID of Enige Sign-On (SSO). SSO via SAML 2.0 wordt sterk aanbevolen.
* **Externe gebruikers**: Plaats login wijze aan Adobe ID, SSO, of het Leren identiteitskaart van de Manager. Lijn de geselecteerde methode uit met het beveiligingsbeleid van uw organisatie.

Adobe raadt aan Federated ID / SAML 2.0 SSO te gebruiken als aanmeldingsmethode voor alle interne gebruikers. Dit zorgt ervoor dat de verificatie volledig wordt gecontroleerd door de identiteitsprovider van uw organisatie, waardoor gecentraliseerde MFA-handhaving en onmiddellijke intrekking van accounts bij vertrek van de gebruiker mogelijk zijn.

Zie [&#x200B; Montages &#x200B;](https://experienceleague.adobe.com/nl/docs/learning-manager/using/admin/settings) voor meer informatie.

## Aanbevolen veilige standaardinstellingen voor provisioning

Wanneer voor het eerst een ALM-account wordt ingericht, raadt de Adobe aan de volgende standaardinstellingen te controleren voordat een gebruiker met administratieve bevoegdheden toegang krijgt tot de toepassing:

| Instelling | Aanbevolen beveiligingsstandaard | Locatie voor configureren |
|------------------------------|------------------------------------------------------------------|-------------------------------------------------|
| Aanmeldingsmethode — interne gebruikers | Single Sign-On (SSO) / Federated ID | ALM > Instellingen > Aanmeldingsmethoden |
| Verificatie in twee stappen (2FA) | Afgedwongen (niet optioneel voor gebruikers) | Admin Console > Instellingen > Privacy en beveiliging |
| Max. sessielevensduur | 8 uur of per organisatiebeleid | Admin Console > Instellingen > Geavanceerde instellingen |
| Maximale inactieve tijd | 30 minuten of per organisatiebeleid | Admin Console > Instellingen > Geavanceerde instellingen |
| Bereik beheerdersrol | Minder bevoegdheden; gebruik waar mogelijk aangepaste beheerdersrollen | ALM > Gebruikers > Aangepaste rollen |
| Vervaldatum externe gebruiker | Een vervaldatum instellen voor elk extern gebruikersprofiel | ALM > Gebruikers > Extern |

### Eerste configuratiecontrolelijst voor nieuwe beheerders

Wanneer u een nieuwe beheerdersaccount op hoofdniveau instelt, moet u het volgende voltooien voordat u operationele toegang verleent:

* Bevestig het identiteitstype is Enterprise ID of Federated ID — geen persoonlijke Adobe ID.
* 2FA afdwingen op het niveau van de Admin Console (Instellingen > Verificatie-instellingen).
* Configureer SSO/Federated ID als deze nog niet is ingeschakeld.
* Stel Max. sessielevensduur en Max. inactieve tijd in in Admin Console > Instellingen > Geavanceerde instellingen.
* Beperk het bereik van de beheerdersrol — wijs alleen de machtigingen toe die nodig zijn voor de verantwoordelijkheden van de gebruiker.
* Controleer of het beheerdersaccount is gekoppeld aan een organisatie-e-mailadres dat wordt beheerd door uw IT-team.
* Documenteer het account in het geprivilegieerde toegangsregister van uw organisatie.

## Werking van de administratieve rekeningen

### Dagelijkse beheertaken

Administratieve rekeningen worden gebruikt voor het uitvoeren van dagelijkse operationele taken, waaronder:

* **het levenscyclusbeheer van de Gebruiker**: Het creëren van gebruikers, het bijwerken van profielen, en het aanbrengen van rolveranderingen.
* **het Leren inhoudsbeheer**: Het leiden van cursussen, het leren programma&#39;s, certificeringen, en catalogi.
* **Rapportering en analytics**: Het produceren van en het herzien van rapporten over de vooruitgang van de student en platformgebruik.
* **Integraties en systeemconfiguratie**: Het leiden van schakelaars, op API-gebaseerde toegang, en systeem-vlakke montages.

Van beheerders wordt verwacht dat ze het interne toegangsbeheer van hun organisatie volgen en het beheerbeleid wijzigen wanneer ze administratieve handelingen uitvoeren.

Zie [&#x200B; vaak Gestelde Vragen voor de Beheerders van Adobe Learning Manager &#x200B;](https://experienceleague.adobe.com/nl/docs/learning-manager/using/faq/frequently-asked-questions-for-administrators)


### Rolhiërarchie en -delegatie

Adobe Admin Console gebruikt een hiërarchische beheerstructuur. De Beheerders van het systeem kunnen verantwoordelijkheden aan laag-voorrechtrollen delegeren om de aanvalsoppervlakte van de top-level administratieve rekening te verminderen:

* Productbeheerder: beheert de toegang tot specifieke Adobe producten (bijvoorbeeld Adobe Learning Manager).
* Beheerder van productprofiel: beheert gebruikerslidmaatschap voor specifieke productprofielen.
* Gebruikersgroepsbeheerder: beheert lidmaatschap van gebruikersgroep.
* Aangepaste ALM-beheerder: gereed voor beheerder binnen ALM met configureerbare machtigingen per catalogus en gebruikersgroep.

### Lopende governance praktijken

Organisaties die ALM-beheeraccounts blijven gebruiken, moeten de volgende praktijken volgen:

* **Periodieke toegangsoverzicht**: controleer regelmatig de lijst van de Admins van het Systeem in Admin Console (Gebruikers > Beheerders) en de Admins ALM (Gebruikers > Intern) om slechts huidig, geoorloofd personeel te verzekeren houden deze rollen.
* **het logboek van de Controle controle**: Het Logboek van de Controle van de Admin Console registreert alle veranderingen die door beheerders worden aangebracht. Systeembeheerders hebben volledige zichtbaarheid. Controleer het logboek regelmatig op ongeoorloofde wijzigingen.
* **Minimale permanente toegang**: Vermijd gebruikend top-level admin rekeningen voor routinetaken. Behoud volledige beheerderstoegang voor taken die deze specifiek vereisen.
* **veiligheid van de Zitting**: Vorm het Maximale Levensduur van de Zitting en Maximum Niet-actieve Tijd in Admin Console > Montages > Geavanceerde Montages om blootstelling van onbeheerde zittingen te beperken.

Zie [&#x200B; overzicht van de Admin console &#x200B;](https://helpx.adobe.com/nl/enterprise/using/admin-console.html) voor meer informatie.

### Gebruikersaccounts beheren onder Beheer

ALM-beheerders beheren interne en externe gebruikersaccounts. Beveiligingsgerelateerde bewerkingen omvatten:

* Gebruiker automatisch verwijderen: in Instellingen kunnen beheerders inactieve interne gebruikers configureren om na een opgegeven aantal dagen automatisch te worden verwijderd, waardoor het risico op inactieve accounts wordt verminderd.
* Vervaldatum externe gebruiker: beheerders stellen een vervaldatum in wanneer ze externe gebruikersprofielen maken. Verlopen accounts worden automatisch naar een niet-actieve status verplaatst.
* Gebruikers verwijderen: beheerders kunnen gebruikers handmatig verwijderen via Gebruikers > Intern > Acties > Gebruiker verwijderen.
* Gebruiker leegmaken: na verwijdering kunnen beheerders gebruikersrecords permanent leegmaken om te voldoen aan het beleid voor gegevensbehoud en ongeoorloofde toegang tot verouderde gebruikersgegevens voorkomen.

Zie het volgende voor meer informatie:

* [Gebruiker en gebruikersgroepen toevoegen](https://experienceleague.adobe.com/nl/docs/learning-manager/using/admin/user-management/add-users-user-groups)
* [Gebruikers leegmaken](https://experienceleague.adobe.com/nl/docs/learning-manager/using/admin/purge-users)

## Afsplitsing van administratieve rekeningen

De administratieve toegang moet worden verwijderd wanneer het niet meer wordt vereist. Ontmanteling van administratieve rekeningen kan omvatten:

* Beheersrollen van gebruikers intrekken.
* Het verminderen van voorrechten wanneer volledige administratieve toegang niet meer noodzakelijk is.
* Indien van toepassing gebruikers uit het systeem verwijderen.

Regelmatige controle en verwijdering van onnodige administratieve toegang helpen de minst bevoorrechte toegang handhaven.

### Systeembeheerdersrechten verwijderen (Admin Console)

Wanneer een systeembeheerder de organisatie verlaat of rollen verandert, moeten de voorrechten onmiddellijk worden ingetrokken:

1. Meld u als systeembeheerder aan bij de Adobe Admin Console.
2. Ga naar Gebruikers > Beheerders.
3. Selecteer de beheerder die u wilt verwijderen.
4. Klik op het pictogram Meer opties (...) > Beheer bewerken en verwijder vervolgens de rol Systeembeheerder - OF selecteer Gebruiker verwijderen om de gebruiker volledig uit de organisatie te verwijderen.
5. Als de beheerder andere rollen had (productbeheerder, ondersteuningsbeheerder, enz.), moet u die ook intrekken.

>[!IMPORTANT]
>
>Als de vertrekkende beheerder de Contracteigenaar voor de organisatie is, moet de rol Contracteigenaar worden overgedragen aan een andere persoon voordat deze kan worden verwijderd. Neem indien nodig contact op met de ondersteuning van de Adobe.

Zie het volgende voor meer informatie:

* [Gebruikersaccounts op de Admin Console maken, bijwerken of verwijderen](https://helpx.adobe.com/nl/enterprise/using/manage-users-individually.html)
* [Uw eigen account verlaten](https://helpx.adobe.com/nl/enterprise/using/leave-organization.html)

### De ALM-beheerdersrol verwijderen

De toegang tot ALM-beheerders intrekken zonder het account van de gebruiker te verwijderen (bijvoorbeeld wanneer de persoon een student blijft):

1. Meld u als beheerder aan bij Adobe Learning Manager.
2. Navigeer naar Gebruikers > Intern.
3. Zoek en selecteer de gebruiker.
4. Selecteer Acties > Rol verwijderen > Beheerder verwijderen.

De gebruiker keert terug naar de studentrol. Hun leergeschiedenis en cursusinschrijvingen blijven behouden.

Zie [&#x200B; gebruiker en gebruikersgroepen &#x200B;](https://experienceleague.adobe.com/nl/docs/learning-manager/using/admin/user-management/add-users-user-groups) voor meer informatie toevoegen.

### Gebruikers verwijderen en leegmaken

Wanneer een gebruiker de organisatie volledig verlaat en zijn account van het platform moet worden verwijderd:

* Verwijder de gebruiker: Gebruikers > Intern > Gebruiker selecteren > Acties > Gebruiker verwijderen. Hierdoor wordt het account uitgeschakeld en wordt actieve toegang verwijderd.
* Wis de gebruiker: na verwijdering gaat u naar Gebruikers > Gebruikers opschonen, selecteert u de maand waarin de gebruiker is verwijderd, selecteert u de gebruiker en kiest u Handelingen > Gebruiker wissen. Met leegmaken worden alle gebruikersrecords definitief verwijderd.

Zie [&#x200B; gebruikers &#x200B;](https://experienceleague.adobe.com/nl/docs/learning-manager/using/admin/purge-users) voor meer informatie leegmaken.


## Veiligheid en gedeelde verantwoordelijkheid

Adobe Learning Manager werkt volgens een model van gedeelde verantwoordelijkheid:

* Adobe is verantwoordelijk voor het beveiligen van het onderliggende ALM-platform en de onderliggende infrastructuur.
* Klanten zijn verantwoordelijk voor het beheer van beheertoegang, roltoewijzingen en activiteiten in de levenscyclus van gebruikers binnen hun ALM-account.

De extra informatie over de veiligheidspraktijken van Adobe Learning Manager is beschikbaar in [&#x200B; Overzicht van de Veiligheid van Adobe Learning Manager (PDF) &#x200B;](https://experienceleague.adobe.com/docs/learning-manager/assets/alm-security-whitepaper-2024.pdf?lang=nl-NL)

## Documentonderhoud

Dit document kan periodiek worden bijgewerkt om de wijzigingen in Adobe Learning Manager-functionaliteit of best practices voor beheerders te weerspiegelen. De versie en de datum die het laatst is bijgewerkt, blijven behouden in de metagegevens van het document en in het FedRAMP-autorisatiepakket. Klanten dienen de openbaar beschikbare versie op Adobe Experience League te raadplegen om ervoor te zorgen dat ze de meest actuele richtlijnen gebruiken.

## Verbeterde beveiliging, dekking

### SCG-ENH-CMP

Adobe onderhoudt gedocumenteerde processen voor componentinventarisatie, eigendom en levenscyclusbeheer om te zorgen voor gecontroleerde configuratie en naleving van alle systeemcomponenten.

### SCG-ENH-API

Adobe dwingt gestandaardiseerde API-beveiligingscontroles af, waaronder verificatie, autorisatie en bewaking, ondersteund door gedocumenteerde governance- en platformbeveiligingsfuncties.

### SCG-ENH-MRG

Adobe past formele processen voor het beheer van wijzigingen en samenvoegingen toe, waaronder controle en goedkeuringscontroles, om de systeemintegriteit te behouden en het implementatierisico te beperken.

### SCG-ENH-VRH

Adobe volgt een gedefinieerd kwetsbaarheidsbeheer- en herstelproces dat identificatie, prioritering, tracering en tijdige oplossing omvat.
