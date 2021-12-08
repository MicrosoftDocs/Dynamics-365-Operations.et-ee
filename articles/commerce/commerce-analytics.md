---
title: Commerce Analytics (eelvaade)
description: See teema kirjeldab, kuidas installida ja kasutada analüüsi võimalusi Microsoft Dynamics 365 Commerce.
author: AamirAllaq
ms.date: 11/23/2021
audience: Application user
ms.reviewer: sericks
ms.search.region: Global
ms.author: aamiral
ms.search.validFrom: 2021-11-12
ms.openlocfilehash: 8cfe2af756315b5be3eb22d99376a96166fffc52
ms.sourcegitcommit: f9fca3d55b47e615e5ef64669dab184e057ec234
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 11/23/2021
ms.locfileid: "7862769"
---
# <a name="commerce-analytics-preview"></a>Commerce Analytics (eelvaade)

[!include [banner](includes/banner.md)]

See teema kirjeldab Commerce'i analüüsi (Eelvaade) installimist, mis sisaldab funktsionaalse analüüsi võimalusi Microsoft Dynamics 365 Commerce.

## <a name="commerce-analytics-preview-live-demo"></a>Commerce Analyticsi (eelvaade) reaalajas demo

Saate vaadata commerce [Analyticsi reaalajas demo (eelvaade)](https://aka.ms/CommerceAnalyticsDemo).

![Commerce Analytics (eelvaade) Kokkuvõte](media/CommerceAnalytics_Summary.png)
![Commerce Analytics (Eelvaade) Maksed](media/CommerceAnalytics_Payments.png)
![Commerce Analytics (eelvaade) veebitegevus](media/CommerceAnalytics_WebActivity.png)


## <a name="commerce-analytics-preview-system-architecture"></a>Commerce Analyticsi (eelvaade) süsteemi ülesehitus

### <a name="key-components"></a>Põhikomponendid

Commerce Analytics (Eelvaade) koosneb järgmistest võtmekomponentidest:

- Valmis kasutama interaktiivseid Power BI aruandeid
- SQL-i vaated Azure Synapse analüüsis
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
- Andmeid toodetakse teistes süsteemides, Dynamics 365 Connected Spaces nt.

#### <a name="step-2-ingestion-and-pre-processing"></a>2. etapp: sisseseadmine ja eeltöötlus

Kandeandmed lähevad Commerce HQ-sse kas otse (kui tellimused kogutakse otse Commerce HQ kliendis) või Commerce Scale Uniti kaudu (kassas, e-kaubanduses või Kohandatud klientarvutis, mis kasutavad Peakontorit hõivatud tellimuste korral).

Funktsiooni Andmetesse eksportimine kasutatakse siis kandeandmete kopeerimiseks toorandmetena teie andmetele. Toorandmed talletatakse andmekaustas Tabelid.

E-äri veebitegevuse andmed saadetakse otse andmetesse. Teiste süsteemide toodetud andmed, nagu näiteks, saadetakse nende süsteemide Dynamics 365 Connected Spaces kaudu otse andmesüsteemi.

#### <a name="step-3-transformation-and-aggregation"></a>3. etapp: teisendamine ja liitmine

Kui toorandmed on teie andmes, loeb Commerce Analytics Service selle, teisendab ja koondab need tagasi andmesilt loogiliste olemite kujul (üksuste kaustas) ja koondmõõdulistena (kaustas Ontologies).

#### <a name="step-4-querying"></a>4. etapp: päringud

Azure Synapse Analüüsi kasutatakse andmete päringuks transact-SQL-i (T-SQL) liidese kaudu. Liides hõlmab SQL-vaateid. SQL-vaated võimaldavad andmete liitpäringuid kas otse T-SQL-i kliendi (sihtanalüüsi) või sellise visualiseerimistööriista kaudu nagu Power BI.

#### <a name="step-5-modeling-and-serving"></a>5. etapp: modelleerimine ja teenimine

Analüüsi esitatud päringu andmed Azure Synapse lähevad Power BI semantilisele mudelile. Olenevalt andmetüübist on see perioodiliselt imporditud mälust käitusajal või otse Power BI päringusse.

Lõpuks renderdatakse andmeid Power BI visuaalsetes andmetes, nii et kasutajad saaksid neid vaadata ja nendega suhelda.

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

####  <a name="top-level-filters"></a><a name="TopLevelFilters"></a> Ülemise taseme filtrid

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

####  <a name="products"></a><a name="ProductsPage"></a> Tooted

- Müük
- Marginaal
- Tagastused

####  <a name="customers"></a><a name="CustomersPage"></a> Külalised

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
    - Kauplus
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
    - Kauplus
    - Terminal
    - Makseviis

### <a name="customers"></a><a name="CustomersPage"></a> Külalised

- Eluea väärtus (LTV)

    LTV arvutatakse kogusumma alusel, mille klient kulutab kõikidesse müügikanalitesse (kaasa arvatud Dynamics 365 Commerce POS, e-kaubandus ja kõnekeskus).

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
    - Lisa korvi
    - Maksmine
    - Ost

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

        LTV arvutatakse kogusumma alusel, mille klient kulutab kõikidesse müügikanalitesse (kaasa arvatud Dynamics 365 Commerce POS, e-kaubandus ja kõnekeskus).

    - Sageduse järgi

        Sagedus arvutatakse kliendi tehingupõhise seotuse alusel organisatsiooniga. Praegu ei arvesta sagedus mittekandeväliseid lekse märguandeid, nt e-kaubanduse sirvimistegevus.

#### <a name="impressions"></a>Muljed

Esmamulje on toote visuaalne vaade e-kaubanduse kaudu. Näiteks viib rakendus e-commerce commerce oma e-äri veebisaidi avalehele ja vaadete kohta kursuste mati toote top **müügiloendi** moodulis. Seejärel vaadetakseallikas sama mati toode **loendimoodulis Valik** teie jaoks. Sel juhul on kaks tootemuljet. 

Praegu jälgitakse esmamuljet järgmistel pinnal:

- Loendid (nt **Soovitatav**, **Tippmüümine**, **Valikuid teile** ja **Trendimine)**
- Ostukorvimoodul
- Otsingutulemuse konteiner
- Kategooria otsingutulemuse konteiner

Praegu ei arvestata neid tooteid, mida renderdatakse puus või kohandatud visuaalis, esmamuljega seotud meetermõõdulistes toodetes.

**Näitamise** aruandeleht sisaldab järgmisi mõõdulehti:

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
> Commerce analytics (Preview) on eelvaade Ameerika Ühendriikides, Kanadas, Ühendkuningriigis, Euroopas, Lõuna-Ida-Aasias, Ida-Aasias, Austraalias ja Jaapanis. Kui teie keskkond asub mis tahes regioonis, saate lubada selle funktsiooni oma keskkonnas, kasutades Finance and Operations Microsoft Dynamics elutsükli teenuseid (LCS). Enne selle funktsiooni kasutamist vaadake teemat Ekspordi [konfigureerimine Azure Data Sisestasse.](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md)

### <a name="enable-and-configure-commerce-analytics-preview"></a><a name="enableCommerceAnalytics"></a> Commerce Analyticsi lubamine ja konfigureerimine (eelvaade)

Commerce Analyticsi (Eelvaade) installimiseks peavad teil olema luba Azure'i kordustellimuses ressursside loomiseks. Samuti peavad teil olema LCS-i lisandmoodulite installimise õigused. Siin antakse ülevaade sammudest:

1. [Commerce Analyticsi eelvaatevormi esitamine](#joinPreview) (eelvaade)
2. [Lubage ja konfigureerige export to Data](#enableExportToDataLake) Seejärel.
3. [Commerce Analyticsi (Preview) lisandmooduli lubamine ja](#enableCommerceAnalyticsAddin) konfigureerimine.
4. [Looge oma ladustamiskontole ühiskasutuses juurdepääsu allkirja (SAS)](#getSASToken) luba.
5. [Laadige vaadete jaoks alla Azure Synapse juurutusskriptid.](#downloadSynapseDeploymentScripts)
6. [Installige ja konfigureerige Azure Synapse](#configureAzureSynapse) tööruum.
7. [Installige Power BI malli](#powerbi) rakendus.

### <a name="submit-the-preview-intake-form-for-commerce-analytics-preview"></a><a name="joinPreview"></a> Commerce Analyticsi eelvaate vormi esitamine (eelvaade)

Commerce [Analyticsi eelvaatevormi esitamine (eelvaade)](https://forms.office.com/r/vW5VLJGXZ2) Lubage vormi töötlemiseks kuni kolm tööpäeva. Pärast selle töötlemist saadetakse kinnitusmeil meiliaadressile, mille vormis edastasite.

### <a name="enable-and-configure-export-to-data-lake"></a><a name="enableExportToDataLake"></a> Andmetesse eksportimise lubamine ja konfigureerimine Selle teabega

Commerce analytics (Eelvaade) põhineb funktsioonil Ekspordi Data Excelisse, et eksportida Commerce HQ-andmed Data Excelisse ja hoida andmed värskena. Enne commerce analyticsi (Eelvaade) konfigureerimist lubage ja konfigureerige Andmete Loendisse eksportimine, järgides [azure Data Tõrketeadese eksportimise konfigureerimise etappe.](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md)

Andmetesse Ekspordi konfigureerimisel tehke märkus järgmise teabe kohta, sest peate selle sisestama hiljem:

- <a name="keyVault"></a> Võtme hoidla domeeninimede süsteemi (DNS) nimi ja rakenduse ID ja rakenduse salanimed, kuhu te rakenduse ID salvestate. Lisateavet vt jaotisest [Turvahoidlasse saladuste](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#addsecrets) lisamine.
- <a name="storageAccount"></a> Ladustamiskonto nimi Eksemplari Data Saate jaoks. Lisateavet vt tellimuses [konto Data Storage (Gen2) loomine](../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md#createsubscription).

### <a name="enable-and-configure-the-commerce-analytics-preview-add-in"></a><a name="enableCommerceAnalyticsAddin"></a> Commerce Analyticsi (Preview) lisandmooduli lubamine ja konfigureerimine

Commerce Analyticsi (Preview) lisandmooduli LCS-i installimiseks peate olema kasutust planeeriva keskkonna puhul LCS-i keskkonnaadministraator.

Commerce Analyticsi (Preview) lisandmooduli installimiseks ja konfigureerimiseks järgige neid samme.

1. Logige [LCS-i](https://lcs.dynamics.com/) sisse ja minge keskkonda.
2. Valige **keskkonna** lehe vahekaardil Keskkonna **lisandmoodulid suvand Installi uus** **lisandmoodul**.
3. Valige dialoogiboksis commerce **analytics (Preview)** (eelvaade).

    Kui **ärianalüüsi** (Eelvaade) loendis pole, veenduge, et olete Insider Programmiga ühendatud.

4. Sisestage **dialoogiboksis** Häälestusprogrammi lisandmoodul järgmise teabe.

    | Teave | Allikas | Näidisväärtus |
    |---|---|---|
    | Azure AD Rentniku ID teie keskkonna jaoks | Logige sisse [Azure'i portaali](https://portal.azure.com/) ja avage **Azure Active Directory** teenus. Seejärel avage **lehekülg Atribuudid ja** kopeerige väärtus väljale Kausta **ID**. | 72f988bf-0000-0000-00000-2d7cd011db47 |
    | Teie võtme VAUlt DNS-i nimi | Sisestage [oma võtme](#keyVault) vault'i DNS-i nimi. Oleks pidanud eelmises jaotises selle väärtuse kohta märkuse tegema. | `https://contosod365datafeedpoc.vault.azure.net/` |
    | Avalduse ID-d sisaldav saladus | Sisestage [avalduse ID talletamissaladuse](#keyVault) nimi. Oleks pidanud eelmises jaotises selle väärtuse kohta märkuse tegema. | app-id |
    | Rakendussaladust sisaldav saladus | Sisestage [rakendussaladust talletav](#keyVault) salanimi. Oleks pidanud eelmises jaotises selle väärtuse kohta märkuse tegema. | app-secret |

5. Nõustuge pakkumise tingimustega, märkides ruudu ja seejärel valige **Installi**.

    Süsteem installib ja konfigureerib commerce analyticsi (Preview) lisandmooduli keskkonna jaoks. Selleks protsessiks võib olla mõni minut. Kui see on lõpetatud, tuleks commerce analytics (Preview) loetleda lehel Keskkond ja olek **tuleks** **·** **installida**.

### <a name="generate-a-sas-token-for-your-storage-account"></a><a name="getSASToken"></a> Ladustamise konto JAOKS SAS-i loa loomine

SAS-i luba võimaldab välisüksustel pääseda juurde teie ladustamiskontole ja omab kindlaid privileegide kogumeid piiratud aja jooksul. Azure Synapse kasutab SAS-i luba, et pääseda juurde Data Varade aluseks olevatele andmetele.

> [!NOTE]
> Ärianalüüsi (Preview) teadaoleva piirangu tõttu kaotab eksemplar juurdepääsu SAS-i loa Azure Synapse aegumisel andmetele. Seepärast peaksite SAS-i loa loomisel seadistama maksimaalse aegumiskuupäeva, mida teie organisatsiooni turvapoliitika lubab.

SAS-i loa loomiseks järgige neid samme.

1. Azure'i portaalis minge [laokontole, mille](#storageAccount) lõite AndmeteSse eksportimise konfigureerimisel.
2. Valige vasakul paanil ladustamiskonto all **ühiskasutusega juurdepääsu allkiri.**
3. Seadke **SAS-i** valikute lehel järgmised väljad.

    | Field | Väärtus |
    |---|---|
    | Lubatud teenused | Valige **bloobi** valik. |
    | Lubatud ressursitüübid | Valige **teenus**, **konteiner** ja **objekt**. |
    | Lubatud õigused | Valige **lugemine**, **kirjutamine**, **kustutamine**, **·** **loend**, lisamine ja **loomine**. |
    | Bloobiversioonide õigused | Lubab **versioonide** kustutamise. |
    | Alguskuupäev ja aegumiskuupäev/-kellaaeg | Seadistage VASTAVALT vajadusele SAS-loa algus- ja lõppkuupäev ning kellaaeg. |
    | Lubatud IP-aadressid | Jätke see väli tühjaks. |
    | Lubatud protokollid | Valige **ainult** HTTPS. |
    | Eelistatud protsessikiht | Valige **baas** (vaikimisi). |
    | Allkirjastamisvõti | Valige **vastavalt** vajadusele võti **1 või** võti2. |

4. Valige **Loo SAS ja ühendusstring.**
5. Kopeerige väärtus **SAS-i loa** väljalt ja kleepige see tekstiredaktorisse nagu Notepad.

### <a name="download-the-deployment-scripts-for-azure-synapse-views"></a><a name="downloadSynapseDeploymentScripts"></a> Laadi vaate jaoks alla Azure Synapse juurutusskriptid

Nõutud vaadete loomiseks ja Azure Synapse avaldamiseks tööruumis peate käitama skriptide komplekti. Skriptide allalaadimiseks järgige neid samme.

1. Minge GitHub-is [microsoft/Dynamics365Commerce.Solutionsi](https://github.com/microsoft/Dynamics365Commerce.Solutions) hoidlasse (repo).
2. Laadige skriptid alla kohalikku arvutisse, laadides selle uuesti sisse või laadides sihtfailina alla.

### <a name="install-and-configure-an-azure-synapse-workspace"></a><a name="configureAzureSynapse"></a> Tööruumi installimine ja Azure Synapse konfigureerimine

Tööruumi installimiseks ja Azure Synapse konfigureerimiseks järgige neid samme.

1. Installige Azure Synapse tööruum oma Azure'i kordustellimuses. Lisateavet vt [Kiirkäivitus: Sünonapse tööruumi](/azure/synapse-analytics/quickstart-create-workspace) loomine.
2. Notepadis või mõnes muus tekstiredaktoris avage oma kohaliku arvuti kaustast fail **SetupSapse.sql, kuhu te olete Dynamics365Commerce.Solutionsi uuesti vastu võtnud või alla** laadinud. Skriptifail asub kaustas /Pipeline/CommerceAnalyticsSexiapse/. Asendage skriptis kohatäite tekst järgmises tabelis näidatud väärtustega.

    | Kohatäite tekst | Asendusväärtus |
    |---|---|
    | placeholder_storageaccount | Ladustamise konto [nimi,](#storageAccount) mille lõite Andmete eksportimist konfigureerides. |
    | <a name="phContainer"></a> placeholder_container | Hoidla ümbrise nimi, mis loodi teie Data Sql Serveri eksemplaris pärast seda, kui installisite edukalt LCS-i lisandmooduli Ekspordi dataKasutaja. Konteineri nime saamiseks peate talletuskonto sirvimiseks Kasutama Azure'i portaalis storage Explorerit. |
    | placeholder_sastoken | Loodud [SAS](#getSASToken)-i luba. Eemaldage kindlasti **küsimärk** (?) SAS-i loa väärtuse algusest. |
    | <a name="phUserPwd"></a> placeholder_password | Teie valitud kindel parool. Tehke selle parooli kohta märkus. See seadistatakse skripti loodud uue **kasutajaaruande kasutaja** parooliks. Ärge **sisestage** **sqladminuser konto** parooli. |

3. Kopeerib skriptifaili uuendatud sisu.
4. Minge Azure'i portaalis uude Azure Synapse tööruumi. Valige **ülevaate lehel** Suvand Ava **Sünapse** Studio.
5. Sünapse Studios valige uus SQL-skript ja kleepige **\>** skriptifaili sisu SQL-skripti redaktorisse.
6. Veenduge, et väli **Kasuta andmebaasi oleks seatud** **koondiks.**
7. Valige **Käsk Käivita ja** oodake, kuni skript töötab. Skripti edukas käivitamine loob Commerce Analyticsi jaoks andmebaasi, mandaatide juurdepääsuks andmete pääsuks andmetega ja kirjutuskaitstud kasutajakonto, mida kasutatakse eksemplariga Power BI Azure Synapse ühenduse loomiseks.
8. Avage oma kohalikus arvutis Windows PowerShell haldusrežiimis ja minge kausta /Pipeline/CommerceAnalyticsSapiapse/ kaustas, kuhu dynamics365Commerce.Solutions uuesti vastu võtnud või alla laadisite.
9. Windows PowerShelli käivitamispoliitika häälestamiseks käivitage järgmine käsk.

    ```powershell
    Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
    ```

10. Kui SQL Server PowerShelli moodulit pole veel installitud, installige see, käivitades järgmise käsu.

    ```powershell
    Install-Module sqlserver
    ```

    > [!NOTE]
    > Mooduli installimise ajal võidakse teilt küsida pakkuja NuGet installimist. Sellisel juhul valige pakkuja **installimiseks** NuGet Y. Teil võidakse paluda ka kinnitada, et installite moodulid ebausalduse hoidlast uuesti. Sellisel juhul valige **installiga** jätkamiseks Y. Võite valikuliselt käivitada **parameetri Set-PSRepository** cmdleti, et usaldada **PSHoidlat**.

11. Avaldage Azure Synapse vaated, kasutades järgmist käsku.

    ```powershell
    .\PublishSynapseViews.ps1 -serverName SERVER_NAME -password PASSWORD -storageAccount STORAGE_ACCOUNT -containerName CONTAINER_NAME -datarootpath DATA_ROOT_PATH
    ```

    Selle käsu käivitamisel asendage kohatäite väärtused, nagu näidatud järgmises tabelis.

    | Kohatäite väärtus | Asendusväärtus |
    |---|---|
    | SERVER_NAME | Serverita Azure Synapse SQL-i lõpp-punkti nimi. Selle väärtuse saate **Azure'i** portaali tööruumi lehele Azure Synapse Ülevaade. |
    | PAROOL | **Sqladminuseri konto** parool. |
    | STORAGE_ACCOUNT | Talletuskonto nimi DataSalvestile. |
    | CONTAINER_NAME | Konteineri nimi, mille lõi funktsioon Ekspordi andmetesse. See konteiner on sama konteiner, mille määras [sammus 2 placeholder_container](#phContainer) väärtuseks. |
    | DATA_ROOT_PATH | Kogu andmeid sisaldava konteineri all kausta nimi. |

    > [!NOTE]
    > Talletuskonto nime, konteineri nime ja andmete juurtee leiate Azure'i salvestusbrauselija ja Andmete Seli salvestuskonto abil Azure'i portaalist.

12. Oodake, kuni skript töötab. Skripti edukas käivitamine loob serverita SQL-i Azure Synapse eksemplaris SQL-i vaated.

### <a name="install-the-power-bi-template-app"></a><a name="powerbi"></a> Mallirakenduse Power BI installimine

Commerce Power BI Analyticsi mallirakenduse installimiseks (eelvaade) järgige neid samme.

1. Logige oma organisatsiooni [Power BI](https://powerbi.microsoft.com/) ID abil portaali sisse.
2. Installige rakenduse Commerce analytics (Preview) Power BI mall, niues [https://aka.ms/cdireport-installapp](https://aka.ms/cdireport-installapp). Võite saada hoiatuse, mis hoiatab, et rakendust ei ole loendis AppSource. Valige **Installi**.
3. Kui installite rakenduse esmakordselt uuesti, minge edasi sammuni 5. Kui olete rakenduse enne installinud, kuvatakse rakenduse uuendamiseks järgmised valikud:

    - **Värskendage tööruumi ja rakendust – värskendage olemasolevat mallirakendust ja kirjutake üle olemasolevad rakendusesätted, nt rakenduse eksemplari** nimi ja õiguste konfiguratsioonid.
    - **Värskendage ainult tööruumi sisu ilma rakendust** värskendamata – värskendage olemasolevat mallirakendust, kuid säilitage olemasolevad rakendusesätted. *See valik on rakenduse uuenduste soovitatav valik.*
    - **Installige rakenduse teine koopia uude tööruumi – looge uus tööruum ja seejärel looge seal** olemasolevast mallirakendusest koopia. Olemasolev tööruum jääb alles.

4. Valige üks värskendusvalikust ja seejärel **installi**.
5. Avage installitud rakendus, **valides** vasakul paanil valiku Rakendused ja valides seejärel rakenduse.
6. Ühendage rakendus andmeallikaga, valides **ühenduse**. Kui olete rakenduse varem installinud, valige **kollases teateribal** suvand Ühenda oma andmelink.
7. Seadistage järgmised väljad.

    | Field | Väärtus |
    |---|---|
    | Server | Sisestage eelmises Azure Synapse jaotises loodud Serverita SQL-i lõpp-punkti nimi. Selle väärtuse saate **Azure'i** portaali tööruumi lehele Azure Synapse Ülevaade. |
    | Andmebaas | Sisestage **CommerceAnalytics.** |
    | Keel | Valige loendist väärtus. Seda välja kasutatakse lokaliseeritud toote- ja kategoorianimede puhul. Väärtus on case-tundlik. |
    | Kuupäevavahemik | Valige loendist väärtus. Valitud kuude arvu andmed imporditakse Power BI andmekomplekti. Teie valitud väärtus mõjutab andmekomplekti suurust ja sünkroonimiseks vajalikku aega. |

8. Valige **Edasi**. Teil palutakse sisestada mandaadid SQL-andmebaasiga ühenduse Azure Synapse loomiseks. Seadke väljad nii, nagu näidatud järgmises tabelis.

    | Field | Väärtus |
    |---|---|
    | Autentimismeetod | Valige **põhiline**. |
    | Kasutajanimi | Sisestage **reportreadonlyuser.** |
    | Parool | Sisestage väärtus, mille asendate [placeholder_password](#phUserPwd) SetupSexiapse.sql skriptis. See parool on kasutaja **reportreadonlyuser** parooliks. |

9. Valige **sisselogimine ja looge** ühendus.
10. Oodake, kuni andmekomplekti on edukalt uuendatud. Seejärel valige nupp **Redigeeri** rakendust, et avada rakenduse tööruum, kus saate vaadata andmekomplekti värskenduse olekut. Rakenduse tööruumis saate soovi korral seadistada oma andmekomplektile automaatsed uuendusgraafikud, hallata õigusi ja rakenduseeksemplari ümber nimetada.

### <a name="privacy"></a><a name="privacy"></a>Privaatsus

Teie privaatsus on meie jaoks oluline. Lisateabe saamiseks lugege meie [privaatsusavaldust](https://go.microsoft.com/fwlink/?LinkId=521839).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
