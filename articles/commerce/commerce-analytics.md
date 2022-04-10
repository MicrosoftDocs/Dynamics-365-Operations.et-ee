---
title: Commerce‘i analüütika (eelversioon)
description: See teema kirjeldab, kuidas installida ja kasutada analüüsi võimalusi Microsoft Dynamics 365 Commerce.
author: AamirAllaq
ms.date: 02/24/2022
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2021-11-12
ms.openlocfilehash: 7e3721421e15bc3e5937691cdbaee51e4d3cdd17
ms.sourcegitcommit: d2e5d38ed1550287b12c90331fc4136ed546b14c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/25/2022
ms.locfileid: "8349739"
---
# <a name="commerce-analytics-preview"></a>Commerce‘i analüütika (eelversioon)

[!include [banner](includes/banner.md)]

See teema kirjeldab Commerce'i analüüsi (Eelvaade) installimist, mis sisaldab funktsionaalse analüüsi võimalusi Microsoft Dynamics 365 Commerce.

## <a name="commerce-analytics-preview-live-demo"></a>Commerce Analyticsi (eelvaade) reaalajas demo

Saate vaadata commerce Analyticsi [reaalajas demo (eelvaade)](https://aka.ms/CommerceAnalyticsDemo).

![Commerce Analytics (eelvaade) Kokkuvõte](media/CommerceAnalytics_Summary.png)
![Commerce Analytics (eelvaade) Maksed](media/CommerceAnalytics_Payments.png)
![Commerce Analytics (eelvaade) veebitegevus](media/CommerceAnalytics_WebActivity.png)

## <a name="commerce-analytics-preview-system-architecture"></a>Commerce Analyticsi (eelvaade) süsteemi ülesehitus

### <a name="key-components"></a>Põhikomponendid

Commerce Analytics (Eelvaade) koosneb järgmistest võtmekomponentidest:

- Valmis kasutama interaktiivseid Power BI aruandeid
- SQL-i vaated: Azure Synapse Analytics
- Üksus ja ontoloogiaandmed teenuses Azure DataEtt
- Toorandmed andmetes

![Commerce Analyticsi süsteemi arhitektuuri võtmekomponendid](media/CommerceAnalyticsArchitecture_v2.png)

### <a name="data-flow"></a>Andmevoog

#### <a name="step-1-data-generation"></a>1. etapp: andmete loomine

Andmed pärinevad kas kandeandmetena või käitumusandmetena ühest järgmistest allikatest:

- Kõnekeskuse seostaja kasutab müügitellimuste töötlemiseks Commerce HQ klienti.
- Kassa kassapidaja töötleb müügikandeid.
- Müüke luuakse kohandatud rakendustes, kasutades Headless Commerce'i (Commerce Scale Unit).
- E-kaubanduse ostja sirvib teie e-äri veebisaiti.
- E-äri ostja edab tellimuse teie e-äri veebisaidil.
- Andmeid toodetakse teistes süsteemides, nt.Dynamics 365 Connected Spaces

#### <a name="step-2-ingestion-and-pre-processing"></a>2. etapp: sisseseadmine ja eeltöötlus

Kandeandmed lähevad Commerce HQ-sse kas otse (kui tellimused kogutakse otse Commerce HQ kliendis) või Commerce Scale Uniti kaudu (kassas, e-kaubanduses või Kohandatud klientarvutis, mis kasutavad Peakontorit hõivatud tellimuste korral).

Funktsiooni Andmetesse eksportimine kasutatakse siis kandeandmete kopeerimiseks toorandmetena teie andmetele. Toorandmed talletatakse andmekaustas Tabelid.

E-äri veebitegevuse andmed saadetakse otse andmetesse. Teiste süsteemide toodetud andmed, nagu näiteks Dynamics 365 Connected Spaces, saadetakse nende süsteemide kaudu otse andmesüsteemi.

#### <a name="step-3-transformation-and-aggregation"></a>3. etapp: teisendamine ja liitmine

Kui toorandmed on teie andmes, loeb Commerce Analytics Service selle, teisendab ja koondab need tagasi andmesilt loogiliste olemite kujul (üksuste kaustas) ja koondmõõdulistena (kaustas Ontologies).

#### <a name="step-4-querying"></a>4. etapp: päringud

Azure Synapse Analytics- kasutatakse andmete päringuks transact-SQL-i (T-SQL) liidese kaudu. Liides hõlmab SQL-vaateid. SQL-vaated võimaldavad andmete liitpäringuid kas otse T-SQL-i kliendi (sihtanalüüsi) või sellise visualiseerimistööriista kaudu nagu Power BI.

#### <a name="step-5-modeling-and-serving"></a>5. etapp: modelleerimine ja teenimine

Päringuks esitatud andmed läheb Azure Synapse Analytics Power BI semantilisele mudelile. Olenevalt andmetüübist on see perioodiliselt imporditud Power BI mälust käitusajal või otse päringusse.

Lõpuks renderdatakse andmeid visuaalsetes Power BI andmetes, nii et kasutajad saaksid neid vaadata ja nendega suhelda.

## <a name="commerce-analytics-preview-functional-overview"></a>Commerce Analyticsi (Eelvaade) funktsionaalne ülevaade

### <a name="summary"></a>Kokkuvõte

Commerce Analyticsi malli rakendus sisaldab järgmisi põhiaruande lehekülgi:

1. [Ülemise taseme filtrid](#TopLevelFilters)
2. [Tooted](#ProductsPage)
3. [Kliendid](#CustomersPage)
4. [Kanalid](#ChannelsPage)
5. [Müük](#SalesPage)
6. [Veerised](#MarginsPage)
7. [Tagastused](#ReturnsPage)
8. [Allahindlused](#DiscountsPage)
9. [Maksed](#PaymentsPage)
10. [Kliendid](#CustomersPage)
11. [Võrdlus](#ComparisonPage)
12. [Veebitegevus](#WebActivityPage)
13. [Veebitegevus – ülataseme filter](#WebActivityTopLevelFilters)

#### <a name="top-level-filters"></a><a name="TopLevelFilters"></a> Ülemise taseme filtrid

- Kuupäevasätted

    - Aasta
    - Kvartal
    - Kuu
    - Nädal
    - Päev

- Kanali sätted

    - Juriidiline isik
    - Kanali tüüp
    - Kliendi tüüp
    - Müügi tüüp
    - Kanal
    - Organisatsiooni hierarhia

- Tootesätted

    - Kategooriahierarhia
    - Kategooria

#### <a name="products"></a><a name="ProductsPage"></a> Tooted

- Müük
- Marginaal
- Tagastused

#### <a name="customers"></a><a name="CustomersPage"></a> Külalised

- Müük
- Marginaal
- Tagastused

#### <a name="channels"></a><a name="ChannelsPage"></a> Kanalite

- Müük
- Marginaal
- Tagastused

### <a name="sales"></a>Müük<a name="SalesPage"></a>

- Tarne asukoha järgi
- Kanali/kaupluse/terminali järgi
- Töövõtja alusel
- Kuupäeva järgi
- Tunni järgi
- Tootekategooria alusel

### <a name="margins"></a><a name="MarginsPage"></a> Veerised

- Tarne asukoha järgi
- Kõrvalsaadus
- Kuupäeva järgi

### <a name="returns"></a><a name="ReturnsPage"></a> Tagastab

- Tagastus summa järgi

    - Kaupluse alusel
    - Kõrvalsaadus
    - Kuupäeva järgi

- Tagastus kande alusel

    - Kaupluse alusel
    - Kõrvalsaadus
    - Kuupäeva järgi

### <a name="discounts"></a><a name="DiscountsPage"></a> Allahindlused

- Kaupluse alusel
- Kõrvalsaadus
- Kuupäeva järgi
- Eraldamine

    - Juriidiline isik
    - Pood
    - Allahindluse tüüp
    - Allahindluse nimi
    - Toode

### <a name="payments"></a><a name="PaymentsPage"></a> Maksed

- Kanali/terminali järgi
- Makseviisi/-tüübi alusel
- Kuupäeva järgi
- Eraldamine

    - Juriidiline isik
    - Kanali tüüp
    - Pood
    - Terminal
    - Makseviis

### <a name="customers"></a><a name="CustomersPage"></a> Külalised

- Eluea väärtus (LTV)

    LTV arvutatakse kogusumma alusel, mille klient kulutab kõikidesse müügikanalitesse Dynamics 365 Commerce (kaasa arvatud POS, e-kaubandus ja kõnekeskus).

- Recency

    Recency arvutatakse päevade arvu alusel, mis on möödunud kliendi viimasest tehingust organisatsiooniga. Hiljutisuse (recency) puhul ei arvestata kandeväliseid sõltuvusi (nt e-kaubanduse sirvimistegevus).

- Sagedus

    Sagedus arvutatakse kliendi tehingupõhise seotuse alusel organisatsiooniga. Praegu ei arvesta sagedus mittekandeväliseid lekse märguandeid, nt e-kaubanduse sirvimistegevus.

- Seose pikkus

    Suhte pikkus arvutatakse päevade arvu põhjal alates kliendi kirje loomisest süsteemis.

- Kannete arv

### <a name="comparison"></a><a name="ComparisonPage"></a> Võrdlus

- Toote võrdlus ajaperioodi alusel

    - Müügi- ja müügierinevus
    - Marginaali ja marginaali erinevus

- Klient ajaperioodi alusel

    - Müügi- ja müügierinevus
    - Marginaali ja marginaali erinevus

### <a name="web-activity"></a><a name="WebActivityPage"></a> Veebitegevus

#### <a name="top-level-filters"></a><a name="WebActivityTopLevelFilters"></a> Ülemise taseme filtrid

- Kuupäevavahemik
- Kanali tüüp
- Kanal
- Kategooriahierarhia

#### <a name="acquisitions"></a>Soetamised

- Lehekülje vaated

    - Riigi või regiooni järgi
    - Kõrvalsaadus
    - Kasutaja sisse logitud olek
    - Kuupäeva järgi

- E-äri tellimused
- Valuutakurss

    - Kuupäeva järgi

- Teisenduse leht

    - Lehevaade lehe tüübi järgi (avaleht, kategooria lehekülg või toote üksikasjade leht)
    - Lisa ostukorvi
    - Registreeri välja
    - Osta

#### <a name="sessions"></a>Seansid

Seanss on kasutaja külastus e-äri veebisaidile. Seanss loetakse lõpetatuks pärast 30 minutit passiivsust või 24 tundi aktiivset kasutamist.

- Riigi või regiooni järgi
- Päritolu järgi (väline viitaja)
- Kasutaja sisse logitud olek
- Seansiloendus

    - Kuupäeva järgi
    - Sisestuslehe järgi

- Tellimus seansi kohta

    - Kuupäeva järgi

- Seansi käivitamismäär

    Sessioon on seanss, kus kasutaja lahkub kohe pärast teie e-äri veebisaidi külastust. Lisateavet vt [vahetuskurssi](https://en.wikipedia.org/wiki/Bounce_rate).

- Klõpsab seansi kohta

#### <a name="visitors"></a>Külastajaid

Teie e-kaubanduse saidi anonüümne nimi tuvastatakse kordumatult konkreetse brauseri ja konkreetse kasutaja kasutatava seadme alusel. Ärianalüüsis ei jälgita anonüümseid vihjeid erinevate brauserite või seadmete vahel. Anonüümne vihje, kes kasutab sama brauserit samal seadmel määratakse kordumatult mitme kasutajaseansi lõikes, kuni brauseri vahemällu talletatud andmed on tühjendatud või kui üks periood (tavaliselt 12 kuud) läbib, mis toimub esimesena.

Kui poodide sirvivad sisse logides oma e-kaubanduse saiti, saab Commerce Analytics nende kohta lisateavet anda. See teave põhineb olemasolevatel suhetel, mis on teie organisatsioonil oma eelnevate ostude tulemusel kõikides müügikanalites Dynamics 365 Commerce (sh kassa, e-äri ja kõnekeskus). Lisateave hõlmab hiljutisuse, seose pikkuse, eluea väärtuse ja sageduse andmeid.

- Veeris
- Keskmised ligemahinnaga tellimused
- Keskmine keskmine müügisumma
- E-commerce'i countus

    - Kuupäeva järgi
    - Asukoha järgi

        Praegu saab Commerce'i analüüs anda ainult riigi/regiooni tasandi granulaarsust e-kaubanduse vihjete asukohaülevaadete jaoks.

    - Recency järgi

        Recency arvutatakse päevade arvu alusel, mis on möödunud kliendi viimasest tehingust organisatsiooniga. Hiljutisuse (recency) puhul ei arvestata kandeväliseid sõltuvusi (nt e-kaubanduse sirvimistegevus).

    - Seose pikkuse järgi

        Suhte pikkus arvutatakse päevade arvu põhjal alates kliendi kirje loomisest süsteemis.

    - Eluea väärtuse alusel (LTV)

        LTV arvutatakse kogusumma alusel, mille klient kulutab kõikidesse müügikanalitesse Dynamics 365 Commerce (kaasa arvatud POS, e-kaubandus ja kõnekeskus).

    - Sageduse järgi

        Sagedus arvutatakse kliendi tehingupõhise seotuse alusel organisatsiooniga. Praegu ei arvesta sagedus mittekandeväliseid lekse märguandeid, nt e-kaubanduse sirvimistegevus.

#### <a name="impressions"></a>Muljed

Esmamulje on toote visuaalne vaade e-kaubanduse kaudu. Näiteks viib rakendus e-commerce commerce oma e-äri veebisaidi avalehele ja vaadete kohta kursuste mati **toote top müügiloendi** moodulis. Seejärel vaadetakseallikas sama mati toode loendimoodulis **Valik** teie jaoks. Sel juhul on kaks tootemuljet.

Praegu jälgitakse esmamuljet järgmistel pinnal:

- Loendid (nt **Soovitatav**, Tippmüümine **·**, **Vali teie jaoks** ja **Trendimine**)
- Ostukorvimoodul
- Otsingutulemuse konteiner
- Kategooria otsingutulemuse konteiner

Praegu ei arvestata neid tooteid, mida renderdatakse puus või kohandatud visuaalis, esmamuljega seotud meetermõõdulistes toodetes.

Näitamise **aruandeleht** sisaldab järgmisi mõõdulehti:

- Näitamiste arv

    - Lehe tüübi ja mooduli järgi

        Lehe tüüp on üldine lehe tüüp, mis on määratud iga lehe kohta teie e-äri veebisaidil. Mooduli tüüp on selle e-kaubanduse visuaalse mooduli tüüp, kus toode kuvatakse.

        Selleks, et vaadata esmamuljeid moodulite järgi, peate võib-olla süvitsi minna lehekülje- ja mooduli visuaaliks.

    - Kõrvalsaadus
    - Kasutaja sisse logitud olek
    - Kuupäeva järgi

- Näitamist klõpsamiste arv

    Esmamulje klõpsake, kui e-äri portaal valib toote visuaalse. Harilikult võetakse koosnemine seejärel toote üksikasjade lehele.

- Näitamist läbiv määr (CTR)

    CTR arvutatakse esmamuljekide koguarvu jagatuna esmamuljete koguarvu jagatuna.

## <a name="commerce-analytics-preview-installation"></a>Commerce Analyticsi (Eelvaade) installimine

> [!NOTE]
> Commerce analytics (Preview) on eelvaade Ameerika Ühendriikides, Kanadas, Ühendkuningriigis, Euroopas, Lõuna-Ida-Aasias, Ida-Aasias, Austraalias ja Jaapanis. Kui teie finants- ja operatsioonide keskkond asub mingis nimetatud regioonis, Microsoft Dynamics saate lubada selle funktsiooni oma keskkonnas, kasutades elutsükli teenuseid (LCS). Enne selle funktsiooni kasutamist vaadake teemat Ekspordi konfigureerimine [Azure Data Sisestasse](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

### <a name="enable-and-configure-commerce-analytics-preview"></a><a name="enableCommerceAnalytics"></a> Commerce Analyticsi lubamine ja konfigureerimine (eelvaade)

Commerce Analyticsi (Eelvaade) installimiseks peavad teil olema luba Azure'i kordustellimuses ressursside loomiseks. Samuti peavad teil olema LCS-i lisandmoodulite installimise õigused. 

Commerce Analyticsi (Eelvaade) lubamiseks ja konfigureerimiseks järgige neid samme.

1. [Lubage ja konfigureerige andmetesse eksportimise lisandmoodul](#enableExportToDataLake).
1. [Installige ja konfigureerige Azure Synapse tööruum](#configureAzureSynapse).
1. [Lisage võtme hoidlasse saladusi](#addSecrets).
1. [Lubage ja konfigureerige Commerce Analyticsi (Eelvaade) lisandmoodul](#enableCommerceAnalyticsAddin).
1. [Installige Power BI malli rakendus](#powerbi).

### <a name="enable-and-configure-the-export-to-data-lake-add-in"></a><a name="enableExportToDataLake"></a> Andmetesse eksportimise lisandmooduli lubamine ja konfigureerimine

> [!IMPORTANT]
> Kui konfigureerite andmetesse eksportimise lisandmooduli, **tühjendage märkeruut Reaalajas** andmete muudatused lehel AndmeteSse eksportimise lisandmooduli häälestus, et reaalajas andmete muudatused ei oleks lubatud. Reaalajas **andmete muudatuste funktsioon** on eelvaates ja commerce Analytics ei toeta seda praegu. Kui lubate selle funktsiooni, ei saa Commerce Analytics töödelda teie andmeid andmetes ning Power BI enamike aruannete andmetest ei näita andmeid.

Commerce analytics (Eelvaade) põhineb funktsioonil Ekspordi data Excelisse, et eksportida Commerce headquartersi andmed DataEkspordisse ja hoida andmed värskena. Enne commerce analyticsi (Eelvaade) konfigureerimist lubage ja konfigureerige Andmete Loendisse [eksportimine, järgides Azure Data Theti eksportimise konfigureerimise etappe](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).

Kui konfigureerite add-ina Ekspordi andmetesse, tehke märkus järgmise teabe kohta, sest peate selle sisestama hiljem:

- <a name="keyVault"></a> Esitatud võtmehoidla domeeninime süsteemi (DNS) nimi.
- Teie antud salanimed, mis sisaldavad rakenduse ID-d ja rakenduse saladust. Lisateavet vt teemast "Lisa [võtme hoidlasse saladused"](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#addsecrets).

### <a name="install-and-configure-an-azure-synapse-workspace"></a><a name="configureAzureSynapse"></a> Tööruumi installimine ja konfigureerimine Azure Synapse

Commerce Analytics (Preview) nõuab, et Sünapse SQL-i nõudmisel tuleks teie tööruumis ette näha Azure Synapse. Tööruumi installimiseks ja konfigureerimiseks Azure Synapse järgige neid samme.

1. Installige tööruum Azure Synapse oma Azure'i kordustellimuses. Lisateavet vt Kiirkäivitus [: Sünonapse tööruumi loomine](/azure/synapse-analytics/quickstart-create-workspace).
1. <a name="serverlessep"></a> Kui tööruum on uuesti ette eeritud, avage ressursi ülevaate leht ja märkige üles serverita **SQL-i lõpp-punkti** väärtus. Selle väärtuse peate salvestama järgmise jaotise võtmehoidlasse.
1. Ülevaate lehel valige link Open **Synapse Studio**, et avada Studio Azure Synapse oma tööruumile.
1. Valige **vasakul** menüül suvand Haldamine. Menüünimede avamiseks võib olla vaja valida laiendamislink vasakul menüül.
1. Jaotises **Turvagrupp** valige **Juurdepääsukontroll**. 
1. Valige **Lisa**.
1. Seadke rollimäärangu **paanil** valikud järgmises tabelis kirjeldatud viisil.

    | Suvand | Väärtus |
    |--------|-------|
    | Ulatus | Valige **tööruum**. |
    | Roll | Valige **Sünapse SQL-i administraator**.|
    | Vali kasutaja | Otsige rakenduse nime, mille lõite [add-ina Andmete eksportimine installimisel](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createapplication). Kui rakendus ilmub otsingutulemustesse, valige see. Rakendus kuvatakse nüüd jaotises Valitud kasutajad **, grupid või teenuse subjektid**. |

1. Valige **Rakenda** rollimäärangu lõpetamiseks. Rakendusele antakse Sünapse SQL-i administraatori privileegid. Seetõttu saab see luua commerce Analyticsi (Preview) LCS-i lisandmooduli konfigureerimisel nõutavaid vaateid.

### <a name="add-secrets-to-the-key-vault"></a><a name="addSecrets"></a> Lisage võtme hoidlasse saladusi.

Samas [võtmehoidlas](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createkeyvault), mida kasutasite AndmeteSse Eksportimise lisandmooduli konfigureerimisel, peate lisama järgmises tabelis kuvatavad saladused. Iga sala puhul tuleb sisestada salanimi ja määratud väärtus.

| Soovitatud salanimi | Salajane väärtus | Salaväärtuse näide |
|---------|---------|---------|
| sünapse-SQL-server | Serverita SQL-i lõpp-punkti väärtus, mille märkisid [tööruumi konfigureerimisel Azure Synapse](#serverlessep). | `test-ondemand.sql.azuresynapse.net` |
| <a name="roUser"></a> readonly-SQL-pwd | Sql-i kirjutuskaitstud kasutaja määratav parool. Aruanne Power BI kasutab seda parooli serverita SQL-iga ühenduse loomiseks. Parooli miseks järgige oma organisatsiooni paroolipoliitikaid. | |

### <a name="enable-and-configure-the-commerce-analytics-preview-add-in"></a><a name="enableCommerceAnalyticsAddin"></a> Commerce Analyticsi (Preview) lisandmooduli lubamine ja konfigureerimine

Commerce Analyticsi (Preview) lisandmooduli LCS-i installimiseks peate olema kasutust planeeriva keskkonna puhul LCS-i keskkonnaadministraator.

Commerce Analyticsi (Preview) lisandmooduli installimiseks ja konfigureerimiseks järgige neid samme.

1. Logige LCS-i [sisse](https://lcs.dynamics.com/) ja minge keskkonda.
2. Valige keskkonna **lehe vahekaardil Keskkonna** lisandmoodulid **suvand** Installi uus lisandmoodul **.**
3. Valige dialoogiboksis commerce analytics **(Preview) (eelvaade**).
4. **Sisestage dialoogiboksis Häälestusprogrammi** lisandmoodul järgmise teabe.

    | Teave | Allikas | Näidisväärtus |
    |---|---|---|
    | Azure Active Directory(Azure AD) Rentniku ID | Logige sisse Azure'i [portaali](https://portal.azure.com/) ja avage **Azure Active Directory** teenus. Seejärel avage lehekülg **Atribuudid** ja kopeerige väärtus väljalt **Rentniku ID**. | `72f988bf-0000-0000-00000-2d7cd011db47` |
    | Azure'i võtme vault DNS-i nimi | Sisestage oma võtme vault'i DNS-i nimi. Peaksite selle väärtuse kohta märkuse tegema, kui konfigureerinud [lisandmooduli Andmetesse Ekspordi](#keyVault). | `https://contosod365datafeedpoc.vault.azure.net/` |
    | Avalduse ID-d sisaldav salanimi | Sisestage avalduse ID talletamissaladuse nimi. Peaksite selle väärtuse kohta märkuse tegema, kui konfigureerinud [lisandmooduli Andmetesse Ekspordi](#keyVault). | `app-id` |
    | Avalduse saladust sisaldav salanimi | Sisestage avalduse saladust talletav salanimi. Peaksite selle väärtuse kohta märkuse tegema, kui konfigureerinud [lisandmooduli Andmetesse Ekspordi](#keyVault). | `app-secret` |
    | Salanimi, mis sisaldab serverita SQL-lõpp-punkti <a0/& jaoks Azure Synapse | Sisestage saladusnimi, mis talletab serverita SQL-i lõpp-punkti. Te oleks pidanud loonud saladuse, kuni [lisate saladused võtmeväärtusele](#addSecrets). | `synapse-sql-server` |
    | Salanimi, mis sisaldab parooli, mis seadistatakse SQL-i kirjutuskaitstud kasutajatele Azure Synapse | Sisestage serverita SQL-i kirjutuskaitstud kasutaja parooli talletav salanimi. See kasutaja luuakse teie jaoks ja seda tuleks kasutada aruandes Power BI serverita SQL-serveriga ühenduse loomiseks. Oleks pidanud loonud sala, kui [lisate turvavõtme väärtusele saladusi](#addSecrets). | `readonly-sql-pwd` |

1. Nõustuge pakkumise tingimustega, märkides ruudu ja seejärel valige **Installi**.

    Süsteem installib ja konfigureerib commerce analyticsi (Preview) lisandmooduli keskkonna jaoks. Selleks protsessiks võib olla mõni minut. Kui see on lõpetatud, **tuleks commerce analytics (Preview)** loetleda **lehel Keskkond** ja olek tuleb **installida**.

### <a name="install-the-power-bi-template-app"></a><a name="powerbi"></a>Power BI Mallirakenduse installimine

Commerce Analyticsi Power BI mallirakenduse installimiseks (eelvaade) järgige neid samme.

1. Logige oma organisatsiooni [Power BI](https://powerbi.microsoft.com/) ID abil portaali sisse.
1. Installige rakenduse Commerce analytics (Preview) Power BI mall, niues .[https://aka.ms/cdireport-installapp](https://aka.ms/cdireport-installapp) Teise võimalusena külastage [AppSource Analüüsi lehekülge Dynamics 365 Commerce](https://appsource.microsoft.com/product/power-bi/dynamics-365-commerce.dydnamics-365-commerce-analytics) ja valige hangi **see kohe**.
1. Kui installite rakenduse esmakordselt uuesti, minge edasi sammuni 5. Kui olete selle enne installinud, rakenduvad rakenduse uuendamiseks järgmised valikud:

    - **Värskendage tööruumi ja rakendust** – värskendage olemasolevat mallirakendust ja kirjutake üle olemasolevad rakendusesätted, nt rakenduse eksemplari nimi ja õiguste konfiguratsioonid.
    - **Värskendage ainult tööruumi sisu ilma rakendust värskendamata** – värskendage olemasolevat mallirakendust, kuid säilitage olemasolevad rakendusesätted. *See valik on rakenduse uuenduste soovitatav valik.*
    - **Installige rakenduse teine koopia uude tööruumi** – looge uus tööruum ja seejärel looge seal olemasolevast mallirakendusest koopia. Olemasolev tööruum jääb alles.

1. Valige üks värskendusvalikust ja seejärel installi **.**
1. Avage installitud rakendus, **valides** vasakul paanil valiku Rakendused ja valides seejärel rakenduse.
1. Looge rakendus andmeallikaga ühenduse loomiseks käsk **Ühenda**. Kui olete rakenduse varem installinud, valige kollases **teateribal** suvand Ühenda oma andmelink.
1. Seadistage järgmised väljad.

    | Väli | Väärtus |
    |---|---|
    | Server | Sisestage serverita SQL-i lõpp-punkt, mille tegite märkuse pärast tööruumi [Azure Synapse loomist](#serverlessep). |
    | Andmebaas | Sisestage **CommerceAnalytics**. |
    | Keel | Valige loendist väärtus. Seda välja kasutatakse lokaliseeritud toote- ja kategoorianimede puhul. Väärtus on case-tundlik. |
    | Kuupäevavahemik | Valige loendist väärtus. Valitud kuude arvu andmed imporditakse andmekomplekti Power BI. Teie valitud väärtus mõjutab andmekomplekti suurust ja sünkroonimiseks vajalikku aega. |

1. Valige **Edasi**. Kui teil palutakse sisestada mandaadid Azure Synapse SQL-andmebaasiga ühenduse loomiseks, seadke väljaväärtused, nagu näidatud järgmises tabelis.

    | Väli | Väärtus |
    |---|---|
    | Autentimismeetod | Valige **baas**. |
    | Kasutajanimi | Sisestage **kasutaja reportreadonlyuser**. |
    | Parool | Sisestage võtmehoidlasse [sql-i kirjutuskaitstud kasutaja jaoks salvestatud parool](#roUser). |

1. Valige **sisselogimine ja looge ühendus**.
1. Oodake, kuni andmekomplekti on edukalt uuendatud. Seejärel valige **rakenduse redigeerimine**, et avada rakenduse tööruum, kus saate vaadata andmekomplekti värskenduse olekut. Rakenduse tööruumis saate soovi korral seadistada oma andmekomplektile automaatsed uuendusgraafikud, hallata õigusi ja rakenduseeksemplari ümber nimetada.

### <a name="privacy"></a><a name="privacy"></a>Privaatsus

Teie privaatsus on meie jaoks oluline. Lisateabe saamiseks lugege meie [privaatsusavaldust](https://go.microsoft.com/fwlink/?LinkId=521839).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
