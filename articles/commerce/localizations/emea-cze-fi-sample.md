---
title: Fiskaalregistreerimisteenuse integreerimise näidis Tšehhi Vabariigi jaoks
description: See artikkel annab ülevaate Tšehhi Vabariigi fiskaalintegratsiooni näidistest Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 08/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-04-01
ms.openlocfilehash: 3838792c0a420fb88ea9daab0a67c2e644c80681
ms.sourcegitcommit: 0feb5d0b06e04f99903069ff2801577be86b8555
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/18/2022
ms.locfileid: "9313744"
---
# <a name="fiscal-registration-service-integration-sample-for-the-czech-republic"></a>Fiskaalregistreerimisteenuse integreerimise näidis Tšehhi Vabariigi jaoks

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

See artikkel annab ülevaate Tšehhi Vabariigi fiskaalintegratsiooni näidistest Microsoft Dynamics 365 Commerce.

Tšehhi Vabariigi kassaraamatute kohalike fiskaalnõuete täitmiseks hõlmab Tšehhi Vabariigi funktsioon kassa (POS) näidisintegratsiooni välise fiskaalregistreerimisteenusega Dynamics 365 Commerce. Näidis laiendab fiskaalintegratsiooni [funktsioone](fiscal-integration-for-retail-channel.md). See põhineb [EFSTA](https://efsta.org/sicherheitsloesungen/) EFR-i (elektroonilise finantsregistri) [lahendusel](https://efsta.org/) ja võimaldab HTTPS-protokolli kaudu sidet EFR-teenusega. EFR-teenus tagab müügi elektroonilise registreerimise (Elektro müügitellimuse tõendus trpfb \[EET\]). See tagab seega müügiandmete võrguedastuse maksuameti fiskaalteenustele. EFR-teenus peab olema majutatud kas Commerce Hardware’i jaamas või eraldi masinas, mida saab ühendada riistvarajaamaga. Näidis esitatakse lähtekoodina ja on osa Commerce’i tarkvara arenduskomplektist (SDK).

Microsoft ei vabasta EFSTA-st riistvara, tarkvara ega dokumentatsiooni. Lisateabeks selle kohta, kuidas saada EFR-lahendust ja seda kasutada, võtke ühendust [EFSTA-ga](https://efsta.org/kontakt/).

## <a name="scenarios"></a>Stsenaariumid

Järgmisi stsenaariume hõlmab Tšehhi Vabariiki fiskaalregistreerimise teenuse integreerimisteenuse näidis.

- Sularahakannete registreerimine fiskaalregistreerimise teenuses.

    - Saada üksikasjalikud kandeandmed fiskaalregistreerimise teenusesse. Need andmed sisaldavad müügirea teavet ning allahindluste, maksete ja maksude teavet. Fiskaalregistreerimise teenus saadab seejärel andmed maksuameti veebiteenusele ja saab sellelt kinnituse, mis sisaldab kande fiskaal-ID koodi.
    - Fikseerige fiskaalregistreerimise teenuse vastus. Vastus hõlmab rahandusandmeid, nt fiskaal-ID-koodi ja kande turvakoodi jne.
    - Printige kviitungil registreeritud kande finantsandmed.

- Kinkekaarditoimingute ja kliendi deposiitide registreerimine fiskaalregistreerimise teenuses.

    - Väljastage kinkekaardile raha või lisage see.
    - Registreerige kliendikonto deposiit.
    - Looge klienditellimus ja registreerige tellimusele deposiit.
    - Redigeerige klienditellimust ja alistage tellimuse deposiit.
    - Tühistage klienditellimus ja tagastage tellimuse deposiit.

- Tõrkekäsitlus, nt järgmised valikud.

    - Kui on võimalik uuesti teha fiskaalregistreerimist, nt kui fiskaalregistreerimisteenus ei ole saadaval, ei ole valmis või ei vasta sellele, saate seda uuesti teha.
    - Finantsregistreerimise edasilükkamine.
    - Jätte fiskaalregistreerimise vahele või märgite kande registreeritud koodina ja kaasate teabekoodid, et hõivata tõrke põhjus ja lisateave.
    - Kontrollige fiskaalregistreerimisteenuse saadavust enne uue müügikande avamist või müügikande sulgemist.

### <a name="gift-cards"></a>Kinkekaardid

Fiskaalregistreerimisteenuse integreerimise näidis rakendab järgmised kinkekaartidega seotud reeglid.

- Müügiread, mis *·* *on* seotud kinkekaardi väljastamise või kinkekaardi toimingutega müügikandes, märgitakse spetsiaalse atribuudiga, kui kanne on fiskaalregistreerimise teenuses registreeritud.
- Kinkekaardiga maksmine on tavamakse ja märgitud spetsiaalse atribuudiga, kui kanne on fiskaalregistreerimise teenuses registreeritud.

### <a name="customer-account-deposits-and-customer-order-deposits"></a>Kliendikonto deposiidid ja kliendi tellimuse deposiidid

Fiskaalregistreerimisteenuse integreerimise näidis juurutab järgmised reeglid, mis on seotud kliendikonto deposiitide ja klienditellimuse deposiitdega.

- Kliendikonto deposiidi või kliendi tellimuse deposiidiga seotud kanne registreeritakse fiskaalregistreerimisteenuses ühe rea kandena ja märgitakse eriatribuudiga. Deposiidi KM-grupp on sellel real määratud.
- Kliendi tellimuse loomisel, s.t kliendi tellimusena, mis sisaldab tooteid, mida klient saab kauplusest välja viia, ning tooteid, mida klient saab peale võtta või lähetada, sisaldab fiskaalregistreerimisteenuses registreeritud kanne ka teostatud toodete ridu ja tellimuse deposiidi rida.
- Makse kliendi kontolt loetakse tavaliseks makseks ja märgitakse spetsiaalse atribuudiga, kui kanne on fiskaalregistreerimise teenuses registreeritud.
- Kliendi tellimuse deposiidisummat, mida rakendatakse kliendi tellimuse pealeppimise toimingule, peetakse tavaliseks makseks ja märgitakse spetsiaalse atribuudiga, kui kanne on fiskaalregistreerimise teenuses registreeritud.

### <a name="offline-registration"></a>Võrguühenduseta registreerimine

Kui fiskaalregistreerimise teenus ei suuda kandeandmeid edastada maksuameti fiskaalveebiteenusele (nt vastuse ajalõpu tõttu) ja saada kinnitust veebiteenuselt (st kande fiskaal-ID kood), loob see kandele kohaliku allkirja ning kaasab selle ja vastuses spetsiaalse tõrkekoodi. Fiskaalregistreerimisteenus taassedab kanded algses järjestuses võrguühenduse taastamisel.

### <a name="limitations-of-the-sample"></a>Näidiste piirangud

Fiskaalregistreerimisteenus toetab ainult stsenaariume, kus hind sisaldab käibemaksu. Seetõttu peab nii **kaupluste kui ka** klientide puhul **valik** Hind sisaldama käibemaksu väärtuseks olema seatud Jah.

## <a name="set-up-commerce-for-the-czech-republic"></a>Häälestage Kaubandus Tšehhi Vabariigile.

See jaotis kirjeldab Kaubandussätteid, mis on Tšehhi Vabariigile omased ja soovitatavad. Lisateavet vt Commerce’i [kodulehelt](../index.md).

Tšehhi-põhise funktsiooni kasutamiseks peate määrama järgmised sätted.

- Juriidilise isiku esmasel aadressil seadke välja Riik/regioon **väärtuseks** **CZECH** (Tšehhi Vabariik).
- Määrake iga Tšehhi Vabariigis paikneva kaupluse kassa funktsiooniprofiilis **ISO-koodi** **välja väärtuseks CZ (Tšehhi** Vabariik).

Samuti peate määrama Tšehhi Vabariigi jaoks järgmised sätted. Pidage meeles, et pärast seadistuse lõpule viimist peate käivitama vastavad jaotustööd.

### <a name="set-up-vat-per-czech-republic-requirements"></a>KM-i seadistamine Tšehhi Vabariigi nõuete kohta


Peate looma käibemaksukoodid, käibemaksugrupid ja kauba käibemaksugrupid. Samuti peate häälestama toodete ja teenuste käibemaksuteabe. Lisateavet käibemaksu funktsioonide seadistamis- ja kasutus kohta leiate käibemaksu [ülevaatest](../../finance/general-ledger/indirect-taxes-overview.md).

### <a name="set-up-stores"></a>Kaupluste häälestamine

Lehel Kõik **kauplused** värskendage kaupluse üksikasju. Konkreetselt seadke järgmised parameetrid.

- **Määrake väljal Käibemaksugrupp** käibemaksugrupp, mida tuleks kasutada vaikekliendile müügi puhul.
- Seadke valiku **Hinnad sisaldavad käibemaksu väärtuseks** **Jah**.
- Seadke välja **Nimi** väärtuseks ettevõtte nimi. See muudatus aitab tagada, et ettevõtte nimi ilmub müügikviitungil. Teise võimalusena saate ettevõtte nime lisada müügikviitungi kavandile vabas vormis tekstina.
- Seadistage **maksu ID-koodi (TIN)** väli ettevõtte ID-koodile. See muudatus aitab tagada, et ettevõtte ID-number ilmub müügikviitungil. Teise võimalusena saate vabas vormis tekstina lisada müügikviitungi kavandile ettevõtte ID-koodi.

### <a name="set-up-functionality-profiles"></a>Funktsiooniprofiilide häälestus

Kassa funktsiooniprofiilide seadistamine.

- Kiirkaardil **Kviitungi** nummerdamine seadistage kviitungite **nummerdamine**, luues või värskendades kirjeid kandetüüpide Müük, **Müügitellimus** ja Tagastatud **sissetulek** jaoks.

### <a name="set-up-registration-numbers"></a>Saate häälestada registreerimisnumbreid.

1. Minge organisatsiooni **halduse globaalse \> aadressiraamatu registreerimistüüpide \> registreerimise \> tüüpidele**. Saate luua uue registreerimistüübi. Määrake riigi **/regiooni väli** **CZECH-le** (Tšehhi Vabariik) ja piirage see organisatsiooniga.
2. Minge organisatsiooni **halduse globaalse \> aadressiraamatu registreerimistüüpide \> registreerimise kategooriatesse \>**. Looge uus registreerimiskategooria. Valige eelmisest juhist registreerimise tüüp ja määrake registreerimiskategooria **väärtuseks** **Ettevõttesisese ID**.
3. Avage **Organisatsiooni haldamine \> Organisatsioonid \> Tootmisüksused**. Valige igale Tšehhi Vabariigis paiknevale kauplusele kauplusega seotud ühik. Laiendage **aadressi** kiirkaardil ripploendit **Veel** valikuid ja valige suvand **Täpsem**. 
4. Avatud aadresside **haldamise lehel** tuleb määrata järgmised sätted:

    - Seadke aadressi **kiirkaardil** välja **Riik/regioon** väärtuseks **KUVA KUVA.**
    - Looge registreerimis **ID** kiirkaardil uus kirje. Valige varem loodud registreerimistüüp ja määrake registreerimisnumber.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Kohandatud väljade konfigureerimine, et neid saaks kasutada müügikviitungite kviitungi vormingutes

Saate konfigureerida keele teksti ja kohandatud väljad, mida kassa kviitungi vormingutes kasutatakse. Kviitungi häälestuse loonud kasutaja vaikeettevõte peaks olema sama juriidiline isik, kus keele teksti häälestus on loodud. Teise võimalusena tuleks samad keeletekstid luua nii kasutaja vaikeettevõttes kui ka kaupluse juriidilises isikus, mille jaoks häälestus on loodud.

Lisage keele **teksti lehel** kviitungi kavandite kohandatud väljade siltidele järgmised kirjed. Pange tähele **, et tabelis kuvatavad** keele **-,** **teksti-ID**- ja tekstiväärtused on vaid näited. Saate neid vastavalt oma nõuetele muuta. Teksi **ID väärtused** peavad siiski olema kordumatud ning võrduma või olema rohkem kui 900001.

Lisage tabelist keeleteksti müügikoha **jaotisse** **järgmised müügikoha** sildid:

| Keele ID | Teksti ID | Tekst                   |
|-------------|---------|------------------------|
| et       | 900001  | ID prov selle provania id/poklad id |
| et       | 900002  | BKP                    |
| et       | 900003  | PKP                    |
| et       | 900004  | FIK                    |
| et       | 900005  | Teave                   |
| et       | 900006  | Järjekorranumber        |

**Lisage kviitungi** kavandite kohandatud väljade jaoks kohandatud väljadele järgmised kirjed lehel Kohandatud väljad. Pange tähele **, et pealdise teksti ID** väärtused peavad vastama **teksti ID** väärtustele, mille määrate keele **tekstilehel**:

| Nimi                 | Tüüp    | Pealdise teksti ID |
|----------------------|---------|-----------------|
| TLT                  | Sissetulek | 900001          |
| Sec                  | Sissetulek | 900002          |
| MÄRK                 | Sissetulek | 900003          |
| EELARVE               | Sissetulek | 900004          |
| INFO                 | Sissetulek | 900005          |
| PIDEV NUMMERDAMINE     | Sissetulek | 900006          |

> [!NOTE]
> On oluline määrata õiged kohandatud väljanimed, nagu on loetletud eelmises tabelis. Vale kohandatud välja nimi põhjustab sissetulekutes puuduvate andmete.

### <a name="configure-receipt-formats"></a>Kviitungi vormingute konfigureerimine

Muutke iga nõutava kviitungi vormingu puhul välja Prindikäitumine **väärtus** väärtuseks Alati **prindi**.

Lisage kviitungi vormingu kujundajasse järgmised kohandatud väljad asjakohastele kviitungi jaotistele. Pange tähele, et väljanimed vastavad eelmises jaotises määratletud keeletekstidele.

- **Päis:** lisage järgmised väljad.

    - **Kaupluse nimi** ja **maksu ID-kood**: neid välju kasutatakse ettevõtte nime ja ID-numbri printimiseks kviitungitele. Soovi korral saate kavandile lisada ka ettevõtte nime ja ID-numbri vabas vormis tekstina.
    - **Kaupluse aadress**, **kuupäev**, **kellaaeg: 24 h**, **kviitungi number** ja **registri number**.
    - **Järjekorranumber**: see väli tuvastab sularahakande numbri fiskaalregistreerimise teenuses.

- **Read:** lisage järgmised väljad.

    - **Kauba nimetus**
    - **Kogus**
    - **Hind kokku maksudega**

- **Jalus:** lisage järgmised väljad.

    - Makseväljad, nii et prinditakse iga makseviisi maksesummad. Lisage näiteks maksevahendi **nimi ja** maksevahendi **summa** väljad kavandi ühele reale.
    - **ID provfsovekvivalendi/pokladekvivalendi**: see väli prindib ettevõtte valduste identifikaatorid ja kassaraamatu.
    - **BKP**: see väli prindib maksukohuslase turvakoodi, mille on määranud fiskaalregistreerimise teenus.
    - **FIK**: see väli prindib maksuameti veebiteenuse määratud kande fiskaal-ID koodi eduka võrgus registreerimise korral.
    - **PKP**: see väli prindib maksukohuslase allkirjakoodi, mille fiskaalregistreerimise teenus võrguühenduseta registreerimise korral loonud on.
    - **Teave**: see väli prindib fiskaalregistreerimise teenusest lisateavet.

Lisateavet kviitungi vormingutega töötades vt Kviitungi vormingute [häälestamine ja kujundamine](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-the-czech-republic"></a>SeadistaGe Tšehhi Vabariigile fiskaalintegratsioon

Tšehhi Vabariigi fiskaalregistreerimisteenuse integratsiooni näidis põhineb [fiskaalintegratsiooni funktsioonil](fiscal-integration-for-retail-channel.md) ja on Osa Commerce SDK-st. Näidis asub lahenduste hoidla **kaustas FiscalIntegration\\\\ Efr**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Näidis [koosneb](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskaaldokumendi pakkujast, mis on Commerce Runtime’i (CRT) laiendus, ja fiskaalühendusest, mis on Commerce Hardware Stationi laiendus. Lisateavet Commerce SDK kasutamise kohta vt commerce SDK [näidised ja viitepakendite allalaadimine GitHub-st NuGet](../dev-itpro/retail-sdk/sdk-github.md)[ja koostevõimaluste kohta sõltumatu pakendamise SDK-le](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Tšehhi Vabariigi fiskaalregistreerimisteenuse integreerimise näidis on saadaval Commerce SDK-s versiooni 10.0.29 alusel. Commerce’i versioonis 10.0.28 või varem peate kasutama Retail SDK eelmist versiooni arendaja virtuaalmasinas (VM) Microsoft Dynamics elutsükli teenustes (LCS). Lisateavet vt Tšehhi Vabariigi ([pärand) fiskaalintegratsiooni näidise juurutamise juhised](emea-cze-fi-sample-sdk.md).

Viige finantsintegratsiooni seadistuse etapid lõpule, nagu on kirjeldatud [ärikanalite fiskaalintegratsiooni seadistamises](setting-up-fiscal-integration-for-retail-channel.md):

1. [Seadistage fiskaalregistreerimise protsess](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Lisaks tehke märkus fiskaalregistreerimise protsessi sätete kohta, mis on omased [sellele fiskaalregistreerimise teenuse integratsiooni näidisele](#set-up-the-registration-process).
1. [Tõrke käsitlemise sätete seadistamine](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Saate lubada edasilükatud fiskaalregistreerimise käsitsi käivitamise](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Kanali komponentide konfigureerimine](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Registreerimisprotsessi häälestamine

Registreerimisprotsessi lubamiseks järgige neid samme Commerce headquartersi häälestamiseks. Lisateavet vt Commerce’i [kanalite fiskaalintegratsiooni häälestamist](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Laadige alla finantsdokumendi pakkuja ja fiskaalkonnektori konfiguratsioonifailid:

    1. [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Lahenduste hoidla avamine.
    1. Valige õige väljalaske haruversioon vastavalt oma SDK-le/rakenduse versioonile.
    1. Avatud **src \> FiscalIntegration \> Efr**.
    1. Laadige alla fiskaaldokumendi pakkuja konfiguratsioonifail konfiguratsioonifailis Configurations **DocumentProviderFiscalEFRSamplePfch.xml \>\>.**
    1. Laadige alla finantskonnektori konfiguratsioonifail **configurations \> Connectors \> ConnectorEFRSample.xml-is**.

    > [!NOTE]
    > Commerce’i versioonis 10.0.28 või varem peate kasutama Retail SDK eelmist versiooni arendaja VM-s LCS-s. Selle fiskaalintegratsiooni näidiskonfiguratsiooni failid asuvad Retail SDK arendaja VM LCS-i kaustades:
    >
    > - **Fiskaaldokumendi pakkuja konfiguratsioonifail:** RetailSdk\\ SampleExtensions\\ CommerceRuntime\\ Extensions.DocumentProvider.EFRSample\\ Configuration\\ DocumentProviderFiscalEFRSampleKliendich.xml
    > - **Fiskaalkonnektori konfiguratsioonifail:** RetailSdk\\ SampleExtensions\\ HardwareStation\\ Extension.EFRSample\\ Configuration\\ ConnectorEFRSample.xml

1. Valige suvandid **Jaemüük ja kaubandus \> Headquartersi häälestus \> Parameetrid \> Commerce’i ühiskasutuses parameetrid**. Seadke vahekaardil **Üldine** suvand Luba fiskaalintegratsioon **väärtusele** **Jah**.
1. Minge jaemüügi ja **ärikanali häälestuse \> fiskaalintegratsiooni \>\> finantsdokumendi pakkujate** juurde ja laadige varem alla laaditud finantsdokumendi pakkuja konfiguratsioonifail.
1. Minge jaemüügi- **ja ärikanali häälestuse \> fiskaalintegratsiooni \>\> fiskaalkonnektori ja laadige varem alla laaditud fiskaalkonnektori** konfiguratsioonifail.
1. Minge jaemüügi ja **ärikanali häälestuse \> fiscal \> integration Connectori funktsiooniprofiilidesse \>**. Looge uus konnektori funktsiooniprofiil. Valige dokumendipakkuja ja ühendus, mille varem laadisite. Värskendage andmevastendussätted [vastavalt](#default-data-mapping) vajadusele.
1. Minge jaemüügi ja **ärikanali häälestuse \> finantsintegratsiooni \> konnektori \> tehnilistesse profiilidesse**. Looge uus konnektori tehniline profiil ja valige varem laaditud fiskaalühendus. Uuendage konnektori [sätteid](#fiscal-connector-settings) vastavalt vajadusele.
1. Minge jaemüügi ja **ärikanali häälestuse \> fiskaalintegratsiooni \> fiskaalühenduse \> gruppidesse**. Looge varem loodud konnektori funktsiooniprofiilile uus fiskaalühenduse grupp.
1. Minge jaemüügi ja **ärikanali häälestuse \> fiskaalintegratsiooni \> fiskaalregistreerimisprotsessidesse \>**. Looge uus fiskaalregistreerimise protsess ja fiskaalregistreerimise protsessi samm ning valige varem loodud fiskaalühenduse grupp.
1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassaprofiilid \> Funktsiooniprofiilid**. Valige funktsiooniprofiil, mis on lingitud kauplusega, kus registreerimisprotsess tuleks aktiveerida. Valige finants **registreerimisprotsessi kiirkaardil** varem loodud fiskaalregistreerimise protsess.
1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassaprofiilid \> Riistvaraprofiilid**. Valige riistvaraprofiil, mis on seotud riistvarajaamaga, millega fiskaalregistreerimise teenus on ühendatud. Valige kiirkaardil **Fiscal peripherals** varem loodud konnektori tehniline profiil.
1. Avage jaotusgraafik (**Retail ja Commerce Retail ja Commerce \> IT \> Distribution schedule**) **ning valige tööd 1070** **ja 1090** andmete edastamiseks kanali andmebaasi.

#### <a name="default-data-mapping"></a>Vaikeandmete vastendamine

Järgmine vaikeandmete vastendamine on kaasatud fiskaaldokumendi pakkuja konfiguratsiooni, mis antakse fiskaalintegratsiooni näidisosana:

- **Käibemaksumäärade vastendamine** : **käibemaksukoodide jaoks seadistatud maksu protsendiväärtuste vastendamine fiskaalteenusele saadetud taotlustes atribuudi TaxG** (maksugrupp) väärtustega. Siin on vaikevastendus:

    ```
    A: 21.00; B: 15.00; C: 10.00; Z: 0.00
    ```

    Iga paari esimene komponent esindab käibemaksugruppi, mida toetab EFR-i fiskaalregistreerimisteenus. Teine komponent esindab vastavat KM-määra. Lisateavet käibemaksugruppide kohta, mida EFR Tšehhi Vabariigile toetab, vt EFR-i [viidet](https://public.efsta.net/efr/).

- **KM-grupi vaikevastendus** – kõik KM-summad, mida ei saa vastendada ühe ettemääratud KM-grupiga, seostatakse vaikimisi (baas)KM-grupiga. Siin on vaikevastendus:

    ```
    A
    ```

- **Deposiitide KM-grupi** vastendamine – kliendi deposiidisummad ja kliendi tellimuse deposiidisummad seostatakse deposiidi KM-grupiga. Siin on vaikevastendus:

    ```
    Z
    ```

#### <a name="fiscal-connector-settings"></a>Fiskaalühenduse sätted

Järgmised sätted on kaasatud fiskaalkonnektori konfiguratsiooni, mis on antud fiskaalintegratsiooni näidisosana:

- **Lõpp-punkti** aadress – fiskaalregistreerimise teenuse URL.
- **Ajalõpp** – aja hulk millisekundites, mida fiskaalkonnektor fiskaalregistreerimise teenuse vastuse ootab.

### <a name="configure-channel-components"></a>Kanali komponentide konfigureerimine

> [!NOTE]
> - Tšehhi Vabariigi fiskaalregistreerimisteenuse integreerimise näidis on saadaval Commerce SDK-s versiooni 10.0.29 alusel. Commerce’i versioonis 10.0.28 või varem peate kasutama Retail SDK eelmist versiooni arendaja VM-s LCS-s. Lisateavet vt Tšehhi Vabariigi ([pärand) fiskaalintegratsiooni näidise juurutamise juhised](emea-cze-fi-sample-sdk.md).
> - Teie keskkonnas juurutatud ärinäidiseid ei uuendata automaatselt, kui rakendate commerce’i komponentidele teenust või kvaliteediuuendusi. Nõutavad näidised tuleb käsitsi uuendada.

#### <a name="set-up-the-development-environment"></a>Saate häälestada arenduskeskkonda.

Arenduskeskkonna katsetada ja näidist laiendada, järgige neid samme.

1. Rakenduste hoidla leidmine [Dynamics 365 Commerce või](https://github.com/microsoft/Dynamics365Commerce.Solutions) allalaadimine. Valige õige väljalaske haruversioon vastavalt oma SDK-le/rakenduse versioonile. Lisateavet vt commerce [SDK näidised ja viitepakendid alla laadida GitHub-st ja NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Avage EFR-i lahendus dynamics365Commerce.Solutions **\\ FiscalIntegration\\ EFR.sln\\** ja koostage see.
1. Installi CRT laiendid:

    1. Leidke laiendi CRT installer:

        - **Commerce Scale Unit:** leidke kaustast Efr **ScaleUnit ScaleUnit.EFR.Installer\\\\ bin\\ Debug\\ net461\\** scaleUnit.EFR.Installer **.**
        - **Kohalik CRT modern POS-s:** **leidke Efr\\ ModernPOS\\ ModernPOS.EFR.Installeri\\ bin\\ Silumine\\ net461** **kaustast ModernPOS.EFR.Installer**.

    1. Käivitage CRT laiendiinstall käsurealt:

        - **Commerce Scalei üksus:**

            ```Console
            ScaleUnit.EFR.Installer.exe install --verbosity 0
            ```

        - **Kohalik CRT Modern POS-s:**

            ```Console
            ModernPOS.EFR.Installer.exe install --verbosity 0
            ```

1. Installige fiskaalühenduse laiendid:

    Fiskaalühenduse laiendusi saate installida riistvarajaama [või kassaregistrisse](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station)[...](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network).

    1. Riistvarajaama laienduste installimine:

        1. Leidke Efr **\\ HardwareStation\\ HardwareStation.EFR.Installeri\\ bin\\ Silumine\\ net461** **kaustast HardwareStation.EFR.Installer**.
        1. Käivitage laiendinstall käsurealt, käivitades järgmise käsu.

            ```Console
            HardwareStation.EFR.Installer.exe install --verbosity 0
            ```

    1. Installige müügikoha laiendused:

        1. Avage kassa fiskaalühenduse **näidislahendus Dynamics365Commerce.Solutions\\ FiscalIntegration\\ PosFiscalConnectorSample\\ Contoso.PosFiscalConnectorSample.sln** ja koostage see.
        1. Kaustas **PosFiscalConnectorSample\\ StoreCommerce.Installer\\ bin\\ Debug\\ net461** **leidke Contoso.PosFiscalConnectorSample.StoreCommerce.Installer**.
        1. Käivitage laiendinstall käsurealt, käivitades järgmise käsu.

            ```Console
            Contoso.PosFiscalConnectorSample.StoreCommerce.Installer.exe install --verbosity 0
            ```

#### <a name="production-environment"></a>Tootmiskeskkond

Järgige fiskaalintegratsiooni [näidise](fiscal-integration-sample-build-pipeline.md) jaoks koostevõimaluste häälestamise etappe, et luua ja vabastada pilveskaala üksus ja iseteeninduse juurutatavad paketid fiskaalintegratsiooni näidiskomplekti jaoks. **EFR-i build-pipeline.yml** malli JAML **\\ faili leiate lahenduste YAML_Files** kaustast [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions) Müügivõimalustest.

## <a name="design-of-extensions"></a>Laienduste kujundus

Tšehhi Vabariigi fiskaalregistreerimisteenuse integratsiooni näidis põhineb [fiskaalintegratsiooni funktsioonil](fiscal-integration-for-retail-channel.md) ja on Osa Commerce SDK-st. Näidis asub lahenduste hoidla **kaustas FiscalIntegration\\\\ Efr**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Näidis [koosneb](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskaaldokumendi pakkujast, mis on CRT laiendiks, ja fiskaalühendusest, mis on Commerce Hardware Stationi laiendus. Lisateavet Commerce SDK kasutamise kohta vt commerce SDK [näidised ja viitepakendite allalaadimine GitHub-st NuGet](../dev-itpro/retail-sdk/retail-sdk-overview.md)[ja koostevõimaluste kohta sõltumatu pakendamise SDK-le](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Tšehhi Vabariigi fiskaalregistreerimisteenuse integreerimise näidis on saadaval Commerce SDK-s versiooni 10.0.29 alusel. Commerce’i versioonis 10.0.28 või varem peate kasutama Retail SDK eelmist versiooni arendaja VM-s LCS-s. Lisateavet vt Tšehhi Vabariigi ([pärand) fiskaalintegratsiooni näidise juurutamise juhised](emea-cze-fi-sample-sdk.md).

### <a name="commerce-runtime-extension-design"></a>Äri käitusaja laiendi kujundus

Fiskaaldokumendi pakkuja laiendi eesmärk on luua teenusepõhiseid dokumente ja käsitleda fiskaalregistreerimise teenuse vastuseid.

#### <a name="request-handler"></a>Nõudeohjur

Dokumendipakkuja jaoks on **üks DocumentProviderEFRFiscalPF** taotluseohjur, mida kasutatakse fiskaaldokumentide loomiseks fiskaalregistreerimise teenuse jaoks.

See ohjur on päritud **INamedRequestHandler liideselt**. Meetod **HandlerName** vastutab ohjuri nime tagastamise eest. Ohjuri nimi peab vastama Commerce Headquartersis määratud konnektori dokumendi pakkuja nimele.

Konnektor toetab järgmisi taotlusi.

- **GetFiscalDocumentDocumentProviderRequest** – see taotlus sisaldab teavet selle kohta, milline dokument tuleks luua. See tagastab teenusepõhise dokumendi, mis tuleb registreerida fiskaalregistreerimise teenuses.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – see taotlus tagastab tellitavate sündmuste loendi. Praegu toetatakse järgmisi sündmusi: müük, kliendikonto deposiidid ja kliendi tellimuse deposiitid.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – see taotlus tagastab fiskaalregistreerimise teenuse vastuse. See vastus järjestatakse stringi moodustamiseks nii, et see on salvestamiseks valmis.

#### <a name="configuration"></a>Konfiguratsioon

Fiskaaldokumendi **pakkuja konfiguratsioonifail asub lahenduste hoidlas\\ src\\ FiscalIntegration\\ Efr\\ Konfiguratsioonide DocumentProviderFiscalEFRSampleValdaja.xml\\**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Faili eesmärk on lubada finantsdokumendi pakkuja sätete konfigureerimist rakendusest Commerce headquarters. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetele.

### <a name="hardware-station-extension-design"></a>Riistvarajaama laienduse kujundus

Fiskaalühenduseks olemise laiendi eesmärgiks on fiskaalregistreerimise teenusega suhtlemine. Riistvarajaama laiend kasutab HTTP-protokolli, et esitada dokumente, mida CRT laiend fiskaalregistreerimise teenusele loob. Samuti käsitletakse fiskaalregistreerimisteenuselt saadud vastuseid.

#### <a name="request-handler"></a>Nõudeohjur

EFRHandler-i **taotluseohjur** on sisenemispunkt fiskaalregistreerimise teenuse taotluste käsitlemiseks.

Ohjur pärineb INamedRequestHandler **liideselt**. Meetod **HandlerName** vastutab ohjuri nime tagastamise eest. Ohjuri nimi peab ühtima Commerce Headquartersis määratud fiskaalühenduse nimega.

Konnektor toetab järgmisi taotlusi.

- **SubmitDocumentFiscalDeviceRequest** – see taotlus saadab dokumendid fiskaalregistreerimise teenusesse ja tagastab sellelt vastuse.
- **IsReadyFiscalDeviceRequest** – seda taotlust kasutatakse fiskaalregistreerimise teenuse seisundikontrolliks
- **InitializeFiscalDeviceRequest** – seda taotlust kasutatakse fiskaalregistreerimise teenuse lähtestamiseks

#### <a name="configuration"></a>Konfiguratsioon

Fiskaalkonnektori konfiguratsioonifail asub **lahenduste hoidlas src\\ FiscalIntegration\\ Efr\\ Configurations\\ Connectors\\ ConnectorEFRSample.xml**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Faili eesmärk on lubada finantsühenduse sätete konfigureerimist rakendusest Commerce headquarters. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetele.

### <a name="pos-fiscal-connector-extension-design"></a>Müügikoha fiskaalkonnektori laienduse kujundus

Kassa fiskaalühenduse laienduse eesmärk on kassast fiskaalregistreerimise teenusega sideühendus. See kasutab side jaoks HTTPS-protokolli.

#### <a name="fiscal-connector-factory"></a>Fiskaalühenduse tehas

Fiskaalühenduse tehas vastendab konnektori nime fiskaalühenduse **rakendusega ja asub failis Pos.Extension\\ Connectors\\ FiscalConnectorFactory.ts**. Konnektori nimi peab kattuma Commerce Headquartersis määratud fiskaalühenduse nimega.

#### <a name="efr-fiscal-connector"></a>EFR-i fiskaalühendus

EFR-i fiskaalühendus asub **failis Pos.Extension\\ Connectors\\ Efr\\ EfrFiscalConnector.ts**. See juurutab **IFiscalConnectori** liidest, mis toetab järgmisi taotlusi:

- **FiscalRegisterSubmitDocumentClientRequest** – see taotlus saadab dokumendid fiskaalregistreerimise teenusesse ja tagastab sellelt vastuse.
- **FiscalRegisterIsReadyClientRequest** – seda taotlust kasutatakse fiskaalregistreerimise teenuse seisundikontrolliks.
- **FiscalRegisterInitializeClientRequest** – seda taotlust kasutatakse fiskaalregistreerimise teenuse lähtestamiseks.

#### <a name="configuration"></a>Konfiguratsioon

Konfiguratsioonifail asub lahenduste hoidla src **FiscalIntegration\\ Efr\\ Configurations\\ Connectorite\\ kaustas**[Dynamics 365 Commerce.](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Faili eesmärk on lubada finantsühenduse sätete konfigureerimist rakendusest Commerce headquarters. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetele. Lisatakse järgmised sätted:

- **Lõpp-punkti** aadress – fiskaalregistreerimise teenuse URL.
- **Ajalõpp** – aeg millisekundites, mille konnektor ootab fiskaalregistreerimise teenuselt vastust.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
