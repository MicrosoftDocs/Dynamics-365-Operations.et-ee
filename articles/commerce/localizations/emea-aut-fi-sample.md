---
title: Fiskaalüksuse registreerimisteenuse integratsiooni näide Austria jaoks
description: See artikkel annab Ülevaate Austria fiskaalintegratsiooni näidistest Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 10/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 603316ea07e5951b3bc5f96af28f549bdafd3b0e
ms.sourcegitcommit: 2bc6680dc6b12d20532d383a0edb84d180885b62
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 10/06/2022
ms.locfileid: "9631338"
---
# <a name="fiscal-registration-service-integration-sample-for-austria"></a>Fiskaalüksuse registreerimisteenuse integratsiooni näide Austria jaoks

[!include [banner](../includes/banner.md)]

See artikkel annab Ülevaate Austria fiskaalintegratsiooni näidistest Microsoft Dynamics 365 Commerce.

Austria Dynamics 365 Retail kassaraamatute kohalike fiskaalnõuete täitmiseks hõlmab Austria funktsioon kassa (POS) näidisintegratsiooni välise fiskaalregistreerimise teenusega. Näidis laiendab fiskaalintegratsiooni [funktsioone](fiscal-integration-for-retail-channel.md). See põhineb [EFSTA](https://www.efsta.eu/at/fiskalloesungen/oesterreich) EFR-i (elektroonilise finantsregistri) [lahendusel](https://www.efsta.eu/at/) ja võimaldab HTTPS-protokolli kaudu sidet EFR-teenusega. EFR-teenus peab olema majutatud kas jaemüügi riistvarajaamas või eraldi masinas, mida saab ühendada riistvarajaamaga. Näidis esitatakse lähtekoodina ja on osa Commerce’i tarkvara arenduskomplektist (SDK).

Microsoft ei vabasta EFSTA-st riistvara, tarkvara ega dokumentatsiooni. Lisateabeks selle kohta, kuidas saada EFR-lahendust ja seda kasutada, võtke ühendust [EFSTA-ga](https://www.efsta.eu/at/kontakt).

## <a name="scenarios"></a>Stsenaariumid

Järgmisi stsenaariume hõlmab Austria fiskaalregistreerimise teenuse integreerimise näidis:

- Sularahakannete registreerimine fiskaalregistreerimise teenuses:

    - Saada üksikasjalikud kandeandmed fiskaalregistreerimise teenusesse. Need andmed sisaldavad müügirea teavet ning allahindluste, maksete ja maksude teavet.
    - Fikseerige fiskaalregistreerimise teenuse vastus. Vastus hõlmab digitaalallkirja ja linki registreeritud kandele.
    - Registreerige maksud ja vastendage need fiskaalregistreerimisteenuse maksukoodidega.
    - Printige kviitungil registreeritud kande QR-kood.

- Kinkekaarditoimingute ja kliendi deposiitide registreerimine fiskaalregistreerimise teenuses sularahata kannetena:

    - Väljastage kinkekaardile raha või lisage see.
    - Registreerige kliendikonto deposiit.
    - Registreerige klienditellimuse deposiit.

- Mittemüügikannete ja sündmuste registreerimine fiskaalregistreerimisteenuses sularahaväliste kannetena:

    - Avatud vahetus ja sule vahetus
    - Algussumma, float-kirje ja maksevahendi eemaldamine
    - Hinnaerand
    - Maksu tühistamine
    - Kviitungi prinditud koopia
    - Sahtli avamine
    - Prindi X-aruanne
    - Prindi Z-aruanne

- Austria-spetsiifiliste väljadega päeva lõpetamise väljavõtete (X/Z-aruanded) printimine:

    - Klientidele tarnitud toodete või teenuste koguarv
    - Müügi jaotus maksumäära järgi
    - Maksete jaotus kassapidaja/kassapidaja järgi
    - Igapäevaseid müüki vähendavad hinna allahindlused ja tagastused
    - Nullmüük (anna sellele alla)

- Tõrkekäsitlus, nt järgmised valikud:

    - Kui on võimalik uuesti teha fiskaalregistreerimist, nt kui fiskaalregistreerimisteenus ei ole saadaval, ei ole valmis või ei vasta sellele, saate seda uuesti teha.
    - Viitvõlgnev fiskaalregistreerimine.
    - Jätte fiskaalregistreerimise vahele või märgite kande registreeritud koodina ja kaasate teabekoodid, et hõivata tõrke põhjus ja lisateave.
    - Kontrollige fiskaalregistreerimisteenuse saadavust enne uue müügikande avamist või müügikande sulgemist.

### <a name="gift-cards"></a>Kinkekaardid

Fiskaalregistreerimisteenuse integreerimise näidis rakendab järgmised kinkekaartidega seotud reeglid:

- Välistage sularahakandest kinkekaardi *väljastamisega ja* *kinkekaardi toimingutega* seotud müügiread. Nende ridade registreerimisel kassakande osana registreerige need fiskaalregistreerimise teenuses eraldi sularahata kandena.
- Ärge printige maksugrupi liigendust ja QR-koodi kviitungil, kui kviitung koosneb ainult kinkekaardi ridadest.
- Printige kinkekaartide kogusumma, mis on kandes väljastatud või uuesti sisse küsitud, kviitungil olevast sularahakande summast eraldi.
- Salvestage makseridade arvutatud korrigeerimised kanali andmebaasis viitega vastavale fiskaalkandele.
- Kinkekaardiga maksmine on tavamakse.

### <a name="customer-deposits-and-customer-order-deposits"></a>Kliendi deposiitid ja kliendi tellimuse deposiidid

Fiskaalregistreerimisteenuse integreerimise näidis juurutab järgmised kliendi deposiitide ja klienditellimuse deposiittega seotud reeglid:

- Registreerige sularahata kanne, kui kanne on kliendi deposiit.
- Registreerige sularahata kanne, kui kanne sisaldab ainult kliendi tellimuse deposiiti või klienditellimuse deposiidi tagasimakset.
- Klienditellimuse deposiidisumma arvatakse hankija tellimuse loomisel maha makseridadelt.
- Salvestage makseridade arvutatud korrigeerimised kanali andmebaasis viitega klienditellimuse fiskaalkandele.

### <a name="limitations-of-the-sample"></a>Näidiste piirangud

Fiskaalregistreerimisteenus toetab ainult stsenaariume, kus hind sisaldab käibemaksu. Seetõttu peab nii **kaupluste kui ka** klientide puhul **valik** Hind sisaldama käibemaksu väärtuseks olema seatud Jah.

## <a name="set-up-commerce-for-austria"></a>Häälestage Austria kaubandus.

See jaotis kirjeldab Austriale omased ja soovitatavad ärisätteid. Lisateavet seadistamise kohta vt Commerce’i [kodulehelt](../index.md).

Austria-põhise funktsiooni kasutamiseks peate määrama järgmised sätted:

- Juriidilise isiku esmasel aadressil seadke riigi/regiooni **väli** **AUT-le** (Austria).
- Määrake igas Austrias paikneva kaupluse kassa funktsiooniprofiilis ISO-koodi **väljaks** **AT** (Austria).

Peate määrama ka Austria jaoks järgmised sätted. Pidage meeles, et pärast seadistuse lõpule viimist peate käivitama vastavad jaotustööd.

### <a name="enable-features-for-austria"></a>Austria funktsioonide lubamine

Funktsioonihalduse tööruumis tuleb lubada **järgmised funktsioonid**:

- (Austria) Täiendavate auditisündmuste lubamine kassas
- (Austria) Kassas päevalõpu väljavõtetes lisateabe lubamine

### <a name="set-up-vat-per-austrian-requirements"></a>Saate häälestada KÄIBEMAKSU Austria nõuete kohta.

Peate looma käibemaksukoodid, käibemaksugrupid ja kauba käibemaksugrupid. Samuti peate häälestama toodete ja teenuste käibemaksuteabe. Lisateavet käibemaksu funktsioonide seadistamis- ja kasutus kohta leiate käibemaksu [ülevaatest](../../finance/general-ledger/indirect-taxes-overview.md).

Müügikviitungitele saate printida käibemaksukoodi lühendi (nt "A" või "B"). Funktsiooni kättesaadavaks miseks seadistage **käibemaksukoodide** lehel prindikoodi **väli**.

### <a name="set-up-stores"></a>Kaupluste häälestamine

Lehel Kõik **kauplused** värskendage kaupluse üksikasju. Konkreetselt määrake järgmised parameetrid:

- **Määrake väljal Käibemaksugrupp** käibemaksugrupp, mida tuleks kasutada vaikekliendile müügi puhul.
- Seadke valiku **Hinnad sisaldavad käibemaksu väärtuseks** **Jah**.
- Seadke välja **Nimi** väärtuseks ettevõtte nimi. See muudatus aitab tagada, et ettevõtte nimi ilmub müügikviitungil. Teise võimalusena saate ettevõtte nime lisada müügikviitungi kavandile vabas vormis tekstina.
- Seadistage **maksu ID-koodi (TIN)** väli ettevõtte ID-koodile. See muudatus aitab tagada, et ettevõtte ID-number ilmub müügikviitungil. Teise võimalusena saate vabas vormis tekstina lisada müügikviitungi kavandile ettevõtte ID-koodi.

### <a name="set-up-functionality-profiles"></a>Funktsiooniprofiilide häälestus

Kassa funktsiooniprofiilide seadistamine:

- Kiirkaardil **Kviitungi** nummerdamine seadistage kviitungite **nummerdamine**, luues või värskendades kirjeid kandetüüpide Müük, **Müügitellimus** ja Tagastatud **sissetulek** jaoks.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Kohandatud väljade konfigureerimine, et neid saaks kasutada müügikviitungite kviitungi vormingutes

Saate konfigureerida keele teksti ja kohandatud väljad, mida kassa kviitungi vormingutes kasutatakse. Kviitungi häälestuse loonud kasutaja vaikeettevõte peaks olema sama juriidiline isik, kus keele teksti häälestus on loodud. Teise võimalusena tuleks samad keeletekstid luua nii kasutaja vaikeettevõttes kui ka kaupluse juriidilises isikus, mille jaoks häälestus on loodud.

Lisage keele **teksti lehel** kviitungi kavandite kohandatud väljade siltidele järgmised kirjed. Pange tähele **, et tabelis kuvatavad** keele **-,** **teksti-ID**- ja tekstiväärtused on vaid näited. Saate neid vastavalt oma nõuetele muuta. Teksi **ID väärtused** peavad siiski olema kordumatud ning võrduma või olema rohkem kui 900001.

Lisage tabelist keeleteksti müügikoha **jaotisse** **järgmised müügikoha** sildid:

| Keele ID | Teksti ID | Tekst                      |
|-------------|---------|---------------------------|
| et       | 900001  | QR-kood                   |
| et       | 900002  | Pidev number         |
| et       | 900003  | Maksu jaemüügi prindikood     |
| et       | 900004  | Kokku (müük)             |
| et       | 900005  | Maks kokku (müük)         |
| et       | 900006  | Summa kaasa maks (müük) |
| et       | 900007  | Maksusumma (müük)        |
| et       | 900008  | Maksu alus (müük)         |

**Lisage kviitungi** kavandite kohandatud väljade jaoks kohandatud väljadele järgmised kirjed lehel Kohandatud väljad. Pange tähele **, et pealdise teksti ID** väärtused peavad vastama **teksti ID** väärtustele, mille määrate keele **tekstilehel**:

| Nimi                 | Tüüp    | Pealdise teksti ID |
|----------------------|---------|-----------------|
| QRCODE               | Sissetulek | 900001          |
| PIDEV NUMMERDAMINE     | Sissetulek | 900002          |
| RETAILPRINTCODE      | Sissetulek | 900003          |
| SALESTOTAL           | Sissetulek | 900004          |
| SALESTOTALTAX        | Sissetulek | 900005          |
| SALESTOTALINCLUDETAX | Sissetulek | 900006          |
| SALESTAMOUNTMOUNT       | Sissetulek | 900007          |
| SALESTAXBASIS        | Sissetulek | 900008          |

> [!NOTE]
> On oluline määrata õiged kohandatud väljanimed, nagu on loetletud eelmises tabelis. Vale kohandatud välja nimi põhjustab sissetulekutes puuduvate andmete.

### <a name="configure-receipt-formats"></a>Kviitungi vormingute konfigureerimine

Muutke iga nõutava kviitungi vormingu puhul välja Prindikäitumine **väärtus** väärtuseks Alati **prindi**.

Lisage kviitungi vormingu kujundajasse järgmised kohandatud väljad asjakohastele kviitungi jaotistele. Pange tähele, et väljanimed vastavad eelmises jaotises määratletud keeletekstidele.

- **Päis:** lisage järgmised väljad:

    - **Kaupluse nime** ja **maksu ID-koodi** väljad, mida kasutatakse ettevõtte nime ja ID-koodi printimiseks kviitungitele. Soovi korral saate kavandile lisada ka ettevõtte nime ja ID-numbri vabas vormis tekstina.
    - **Kaupluse aadressi**, kuupäeva **,** kellaaja **24 h**, **kviitungi numbri ja** registri **numbriväljad**.
    - **Pideva numbri** väljad fiskaalregistreerimise teenuses sularahakande numbri tuvastamiseks

- **Read:** lisage järgmised väljad:

    - **Kauba nimetus**.
    - **Kogus**
    - **Hind kokku maksudega**.
    - **Maksu jaemüügi prindikood**, mida kasutatakse kaubale kehtivale käibemaksukoodile vastava lühendatud koodi printimiseks.

- **Jalus:** lisage järgmised väljad:

    - Makseväljad, nii et prinditakse iga makseviisi maksesummad. Lisage näiteks maksevahendi **nimi ja** maksevahendi **summa** väljad kavandi ühele reale.
    - **Väljagrupi** Müük kokku:

        - **Väli Kokku (** müük), mida kasutatakse sissetuleku sularahamüügi kogusumma printimiseks. Summa ei sisalda maksu. Ettemaksed ja kinkekaarditoimingud on välja jäetud.
        - **Väli Kaasa maks** (müük), mida kasutatakse sissetuleku sularahamüügi kogusumma printimiseks. Summa sisaldab maksu. Ettemaksed ja kinkekaarditoimingud on välja jäetud.
        - **Väli Maks kokku** (müük), mida kasutatakse sularahamüügi sissetuleku käibemaksu kogusumma printimiseks. Ettemaksed ja kinkekaarditoimingud on välja jäetud.

    - **Maksu katkestuse** väljagrupp. Kõik selle väljagrupi väljad tuleb printida ühele eraldi reale.

        - **Maksu ID** väli, mis on standardne väli, mis võimaldab printida käibemaksu kokkuvõtte iga käibemaksukoodi kohta. See väli tuleb lisada uuele reale.
        - **Maksuprotsendi** väli, mis on standardväli, mida kasutatakse käibemaksukoodi efektiivse maksumäära printimiseks.
        - **Välja Maksu alus** (müük), mida kasutatakse sissetuleku sularahamüügi kogusumma printimiseks käibemaksukoodi kohta. Ettemaksed ja kinkekaarditoimingud on välja jäetud.
        - **Maksusumma (müük),** mida kasutatakse selle käibemaksukoodi puhul sularahamüügi sissetuleku maksusumma printimiseks.
        - **Maksu jaemüügi prindikoodi** väli, mida kasutatakse käibemaksukoodile vastava lühendatud koodi printimiseks.

    - **Väli QR-kood**, mida kasutatakse registreeritud sularahakande viite printimiseks QR-koodina.

        > [!NOTE]
        > **QR-koodi** väärtus tuuakse fiskaalregistri vastusest. EFR tagastab oma vastuses QR-koodi **ainult siis, kui EFR-i konfiguratsiooni atribuutide** välja väärtust on kirjeldatud EFSTA dokumentatsioonis. EFR-i konfiguratsiooni atribuutide **väljal** tuleb QR-koodi vorming seada **BMP-le**.

Lisateavet kviitungi vormingutega töötades vt Kviitungi vormingute [häälestamine ja kujundamine](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-austria"></a>Austria rahandusintegratsiooni häälestamine

Austria fiskaalregistreerimisteenuse integreerimise näidis põhineb fiskaalintegratsiooni [funktsioonil](fiscal-integration-for-retail-channel.md) ja on osa Commerce SDK-st. Näidis asub lahenduste hoidla **kaustas FiscalIntegration\\\\ Efr**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Näidis [koosneb](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskaaldokumendi pakkujast, mis on Commerce Runtime’i (CRT) laiendus, ja fiskaalühendusest, mis on Commerce Hardware Stationi laiendus. Lisateavet Commerce SDK kasutamise kohta vt commerce SDK [näidised ja viitepakendite allalaadimine GitHub-st NuGet](../dev-itpro/retail-sdk/sdk-github.md)[ja koostevõimaluste kohta sõltumatu pakendamise SDK-le](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Austria fiskaalregistreerimisteenuse integreerimise näidis on commerce SDK-s saadaval versiooni 10.0.29 alusel. Commerce’i versioonis 10.0.28 või varem peate kasutama Retail SDK eelmist versiooni arendaja virtuaalmasinas (VM) Microsoft Dynamics elutsükli teenustes (LCS). Lisateavet vt Austria fiskaalintegratsiooni [näidise juurutuse juhistest (pärand).](emea-aut-fi-sample-sdk.md)

Viige finantsintegratsiooni seadistuse etapid lõpule, nagu on kirjeldatud [ärikanalite fiskaalintegratsiooni seadistamises](setting-up-fiscal-integration-for-retail-channel.md):

1. [Seadistage fiskaalregistreerimise protsess](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Lisaks tehke märkus fiskaalregistreerimise protsessi sätete kohta, mis on omased [sellele fiskaalregistreerimise teenuse integratsiooni näidisele](#set-up-the-registration-process).
1. [Tõrke käsitlemise sätete seadistamine](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Luba edasilükatud fiskaalregistreerimise käsitsi käivitamine](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-deferred-fiscal-registration).
1. [Kanali komponentide konfigureerimine](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Registreerimisprotsessi häälestamine

Registreerimisprotsessi lubamiseks järgige neid samme Commerce headquartersi häälestamiseks. Lisateavet vt Commerce’i [kanalite fiskaalintegratsiooni häälestamist](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Laadige alla finantsdokumendi pakkuja ja fiskaalkonnektori konfiguratsioonifailid:

    1. [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Lahenduste hoidla avamine.
    1. Valige õige väljalaske haruversioon vastavalt oma SDK-le/rakenduse versioonile.
    1. Avatud **src \> FiscalIntegration \> Efr**.
    1. Avage **konfiguratsioonid \> DocumentProviders ja** laadige alla finantsdokumendi pakkuja konfiguratsioonifailid: 

        - DocumentProviderFiscalEFRSampleAustria.xml
        - Xml-fail DocumentProviderNonFiscalEFRSampleAustria.xml

    1. Laadige alla finantskonnektori konfiguratsioonifail **configurations \> Connectors \> ConnectorEFRSample.xml-is**.

    > [!NOTE]
    > Commerce’i versioonis 10.0.28 või varem peate kasutama Retail SDK eelmist versiooni arendaja VM-s LCS-s. Selle fiskaalintegratsiooni näidiskonfiguratsiooni failid asuvad Retail SDK arendaja VM LCS-i kaustades:
    >
    > - **Fiskaaldokumendi pakkuja konfiguratsioonifailid:** RetailSdk\\ SampleExtensions\\ CommerceRuntime\\ Extensions.DocumentProvider.EFRSample\\ konfiguratsioon
    > - **Fiskaalkonnektori konfiguratsioonifail:** RetailSdk\\ SampleExtensions\\ HardwareStation Extension.EFRSample\\ konfiguratsioon\\

1. Valige suvandid **Jaemüük ja kaubandus \> Headquartersi häälestus \> Parameetrid \> Commerce’i ühiskasutuses parameetrid**. Seadke vahekaardil **Üldine** suvand Luba fiskaalintegratsioon **väärtusele** **Jah**.
1. Minge jaemüügi ja **ärikanali häälestuse \> finantsintegratsiooni \>\> finantsdokumendi pakkujate** juurde ja laadige varem alla laaditud finantsdokumendi pakkuja konfiguratsioonifailid.
1. Minge jaemüügi- **ja ärikanali häälestuse \> fiskaalintegratsiooni \>\> fiskaalkonnektori ja laadige varem alla laaditud fiskaalkonnektori** konfiguratsioonifail.
1. Minge jaemüügi ja **ärikanali häälestuse \> fiscal \> integration Connectori funktsiooniprofiilidesse \>**. Looge kaks uut konnektori funktsiooniprofiili, üks igale varem laaditud fiskaaldokumendi pakkujale ja valige varem laaditud fiskaalühendus. Värskendage andmevastendussätted [vastavalt](#default-data-mapping) vajadusele.
1. Minge jaemüügi ja **ärikanali häälestuse \> finantsintegratsiooni \> konnektori \> tehnilistesse profiilidesse**. Looge uus konnektori tehniline profiil ja valige varem laaditud fiskaalühendus. Uuendage konnektori [sätteid](#fiscal-connector-settings) vastavalt vajadusele.
1. Minge jaemüügi ja **ärikanali häälestuse \> fiskaalintegratsiooni \> fiskaalühenduse \> gruppidesse**. Looge kaks uut fiskaalühenduse gruppi, üks iga varem loodud konnektori funktsiooniprofiili jaoks.
1. Minge jaemüügi ja **ärikanali häälestuse \> fiskaalintegratsiooni \> fiskaalregistreerimisprotsessidesse \>**. Looge uus fiskaalregistreerimise protsess ja kaks fiskaalregistreerimise protsessi etappi ning valige varem loodud fiskaalühenduse grupid.
1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassaprofiilid \> Funktsiooniprofiilid**. Valige funktsiooniprofiil, mis on lingitud kauplusega, kus registreerimisprotsess tuleks aktiveerida. Valige finants **registreerimisprotsessi kiirkaardil** varem loodud fiskaalregistreerimise protsess. Mitterahaliste sündmuste registreerimise lubamiseks kassas **seadke** funktsiooni **kiirkaardi** **kassas** valiku Audit väärtuseks **Jah.**
1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassaprofiilid \> Riistvaraprofiilid**. Valige riistvaraprofiil, mis on seotud riistvarajaamaga, millega fiskaalregistreerimise teenus on ühendatud. Valige kiirkaardil **Fiscal peripherals** varem loodud konnektori tehniline profiil.
1. Avage jaotusgraafik (**Retail ja Commerce Retail ja Commerce \> IT \> Distribution schedule**) **ning valige tööd 1070** **ja 1090** andmete edastamiseks kanali andmebaasi.

#### <a name="default-data-mapping"></a>Vaikeandmete vastendamine

Järgmine vaikeandmete vastendamine on kaasatud fiskaaldokumendi pakkuja konfiguratsiooni, mis antakse fiskaalintegratsiooni näidisosana:

- **Käibemaksumäärade vastendamine** : **käibemaksukoodide jaoks seadistatud maksu protsendiväärtuste vastendamine fiskaalteenusele saadetud taotlustes atribuudi TaxG** (maksugrupp) väärtustega. Siin on vaikevastendus:

    ```
    A: 20.00; B: 10.00; C: 13.00; D: 0.00; E: 19.00; F: 7.00
    ```

    Iga paari esimene komponent esindab käibemaksugruppi, mida toetab EFR-i fiskaalregistreerimisteenus. Teine komponent esindab vastavat KM-määra. Lisateavet Käibemaksugruppide kohta, mida EFR Austriale toetab, vt EFR-i [viidet](https://public.efsta.net/efr/).

#### <a name="fiscal-connector-settings"></a>Fiskaalühenduse sätted

Järgmised sätted on kaasatud fiskaalkonnektori konfiguratsiooni, mis on antud fiskaalintegratsiooni näidisosana:

- **Lõpp-punkti** aadress – fiskaalregistreerimise teenuse URL.
- **Seadme ajalõpp** – aja hulk millisekundites, mida fiskaalühendus ootab fiskaalregistreerimise teenuselt vastust.
- **Kuva fiskaalregistreerimise** teatised – see lipp kontrollib, kas fiskaalregistreerimise teenuse tagastused tuleb operaatorile kuvada.

### <a name="configure-channel-components"></a>Kanali komponentide konfigureerimine

> [!NOTE]
> - Austria fiskaalregistreerimisteenuse integreerimise näidis on commerce SDK-s saadaval versiooni 10.0.29 alusel. Commerce’i versioonis 10.0.28 või varem peate kasutama Retail SDK eelmist versiooni arendaja VM-s LCS-s. Lisateavet vt Austria fiskaalintegratsiooni [näidise juurutuse juhistest (pärand).](emea-aut-fi-sample-sdk.md)
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
        1. Käivitage laiendiinstall käsurealt, mis käitab järgmist käsku.

            ```Console
            Contoso.PosFiscalConnectorSample.StoreCommerce.Installer.exe install --verbosity 0
            ```

#### <a name="production-environment"></a>Tootmiskeskkond

Järgige fiskaalintegratsiooni [näidise](fiscal-integration-sample-build-pipeline.md) jaoks koostevõimaluste häälestamise etappe, et luua ja vabastada pilveskaala üksus ja iseteeninduse juurutatavad paketid fiskaalintegratsiooni näidiskomplekti jaoks. **EFR-i build-pipeline.yml** malli JAML **\\ faili leiate lahenduste YAML_Files** kaustast [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions) Müügivõimalustest.

## <a name="design-of-extensions"></a>Laienduste kujundus

Austria fiskaalregistreerimisteenuse integreerimise näidis põhineb fiskaalintegratsiooni [funktsioonil](fiscal-integration-for-retail-channel.md) ja on osa Commerce SDK-st. Näidis asub lahenduste hoidla **kaustas FiscalIntegration\\\\ Efr**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Näidis koosneb [fiskaaldokumendi](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) pakkujast, mis on CRT laiendiks, ja fiskaalühendusest, mis on Commerce Hardware Stationi laiendus. Lisateavet Commerce SDK kasutamise kohta vt commerce SDK [näidised ja viitepakendite allalaadimine GitHub-st NuGet](../dev-itpro/retail-sdk/retail-sdk-overview.md)[ja koostevõimaluste kohta sõltumatu pakendamise SDK-le](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Austria fiskaalregistreerimisteenuse integreerimise näidis on commerce SDK-s saadaval versiooni 10.0.29 alusel. Commerce’i versioonis 10.0.28 või varem peate kasutama Retail SDK eelmist versiooni arendaja VM-s LCS-s. Lisateavet vt Austria fiskaalintegratsiooni [näidise juurutuse juhistest (pärand).](emea-aut-fi-sample-sdk.md)

### <a name="commerce-runtime-extension-design"></a>Äri käitusaja laiendi kujundus 

Fiskaaldokumendi pakkuja laiendi eesmärk on luua teenusepõhiseid dokumente ja käsitleda fiskaalregistreerimise teenuse vastuseid.

#### <a name="request-handler"></a>Nõudeohjur

Dokumendi pakkujatel on kaks nõudeohjureid:

- **DocumentProviderEFRFiscalAUT** – seda ohjurit kasutatakse fiskaaldokumentide loomiseks fiskaalregistreerimise teenusele.
- **DocumentProviderEFRNonFiscalAUT** – seda ohjurit kasutatakse fiskaalregistreerimise teenuse mittefiskaalsete dokumentide loomiseks.

Need ohjurid on päritud **INamedRequestHandler liideselt**. Meetod **HandlerName** vastutab ohjuri nime tagastamise eest. Ohjuri nimi peab vastama Commerce Headquartersis määratud konnektori dokumendi pakkuja nimele.

Konnektor toetab järgmisi taotlusi:

- **GetFiscalDocumentDocumentProviderRequest** – see taotlus sisaldab teavet selle kohta, milline dokument tuleks luua. See tagastab teenusepõhise dokumendi, mis tuleb registreerida fiskaalregistreerimise teenuses.
- **GetNonFiscalDocumentDocumentProviderRequest** – see taotlus sisaldab teavet mittefiskaalse dokumendi genereerimise kohta. See tagastab teenusepõhise dokumendi, mis tuleb registreerida fiskaalregistreerimise teenuses.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – see taotlus tagastab tellitavate sündmuste loendi. Praegu toetatakse järgmisi sündmusi: müük, X-aruande printimine, Z-aruande printimine, kliendikonto deposiitid, kliendi tellimuse deposiitid, auditi sündmused ja mittemüügikanded.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – see taotlus tagastab fiskaalregistreerimise teenuse vastuse. See vastus järjestatakse stringi moodustamiseks nii, et see on salvestamiseks valmis.

#### <a name="configuration"></a>Konfiguratsioon

Fiskaaldokumendi pakkuja konfiguratsioonifailid asuvad **lahenduste hoidla kaustas FiscalIntegration\\ Efr\\ Configurations\\ DocumentProviders\\**[Dynamics 365 Commerce:](https://github.com/microsoft/Dynamics365Commerce.Solutions/)

- **DocumentProviderFiscalEFRSampleAustria** – finantsdokumentide finantsdokumendi pakkuja konfiguratsioonifail.
- **DocumentProviderNonFiscalEFRSampleAustria** – mittefiskaalse dokumendi finantsdokumendi pakkuja konfiguratsioonifail.

Nende failide eesmärk on lubada finantsdokumendi pakkuja sätete konfigureerimist rakendusest Commerce headquarters. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetele.

### <a name="hardware-station-extension-design"></a>Riistvarajaama laienduse kujundus

Fiskaalühenduse laienduse eesmärk on suhelda fiskaalregistreerimisteenusega. Riistvarajaama laiend kasutab HTTP- ja HTTPS-protokolle, et edastada dokumente, CRT mida laiend loob fiskaalregistreerimise teenusele. Samuti käsitletakse fiskaalregistreerimisteenuselt saadud vastuseid.

#### <a name="request-handler"></a>Nõudeohjur

EFRHandler-i **taotluseohjur** on sisenemispunkt fiskaalregistreerimise teenuse taotluste käsitlemiseks.

Ohjur pärineb INamedRequestHandler **liideselt**. Meetod **HandlerName** vastutab ohjuri nime tagastamise eest. Ohjuri nimi peab ühtima Commerce Headquartersis määratud fiskaalühenduse nimega.

Fiskaalühendus toetab järgmisi taotlusi:

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
