---
title: Fiskaalregistreerimisteenuse integreerimise näidis Tšehhi Vabariigi jaoks
description: Selles teemas antakse ülevaade Tšehhi Vabariigi fiskaalintegratsiooni näidistest Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-4-1
ms.dyn365.ops.version: 10.0.2
ms.openlocfilehash: 0a04ebb7685ff0b72207d9268b4aea980679572e
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944985"
---
# <a name="fiscal-registration-service-integration-sample-for-the-czech-republic"></a>Fiskaalregistreerimisteenuse integreerimise näidis Tšehhi Vabariigi jaoks

[!include[banner](../includes/banner.md)]

Selles teemas antakse ülevaade Tšehhi Vabariigi fiskaalintegratsiooni näidistest Microsoft Dynamics 365 Commerce.

Tšehhi Vabariigi kassaraamatute kohalike fiskaalnõuete täitmiseks hõlmab Tšehhi Vabariigi funktsioon kassa (POS) näidisintegratsiooni välise Dynamics 365 Commerce fiskaalregistreerimisteenusega. Näidis laiendab [fiskaalintegratsiooni funktsioone](fiscal-integration-for-retail-channel.md). See põhineb [EFSTA](https://efsta.org/) [EFR-i (elektroonilise finantsregistri)](https://efsta.org/sicherheitsloesungen/) lahendusel ja võimaldab HTTPS-protokolli kaudu sidet EFR-teenusega. EFR-i teenus tagab müügi elektroonilise registreerimise (EET - Elektro müügitellimuse tõenduse trtulub), st müügiandmete elektroonilise edastamise maksuameti fiskaalveebiteenusele.

EFR-teenus peab olema majutatud kas Commerce Hardware'i jaamas või eraldi masinas, mida saab ühendada riistvarajaamaga. Näidis esitatakse lähtekoodina ja on osa jaemüügi tarkvara arenduskomplektist (SDK).

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

- Müügiread, mis on seotud kinkekaardi väljastamise või kinkekaardi toimingutega müügikandes, märgitakse spetsiaalse atribuudiga, kui kanne on *fiskaalregistreerimise* *teenuses* registreeritud.
- Kinkekaardiga maksmine on tavamakse ja märgitud spetsiaalse atribuudiga, kui kanne on fiskaalregistreerimise teenuses registreeritud.

### <a name="customer-account-deposits-and-customer-order-deposits"></a>Kliendikonto deposiidid ja kliendi tellimuse deposiidid

Fiskaalregistreerimisteenuse integreerimise näidis juurutab järgmised reeglid, mis on seotud kliendikonto deposiitide ja klienditellimuse deposiitdega.

- Kliendikonto deposiidi või kliendi tellimuse deposiidiga seotud kanne registreeritakse fiskaalregistreerimisteenuses ühe rea kandena ja märgitakse eriatribuudiga. Deposiidi KM-grupp on sellel real määratud.
- Kliendi tellimuse loomisel, s.t kliendi tellimusena, mis sisaldab tooteid, mida klient saab kauplusest välja viia, ning tooteid, mida klient saab peale võtta või lähetada, sisaldab fiskaalregistreerimisteenuses registreeritud kanne ka teostatud toodete ridu ja tellimuse deposiidi rida.
- Makse kliendi kontolt loetakse tavaliseks makseks ja märgitakse spetsiaalse atribuudiga, kui kanne on fiskaalregistreerimise teenuses registreeritud.
- Kliendi tellimuse deposiidisummat, mida rakendatakse kliendi tellimuse peale võtta toimingule, peetakse tavaliseks makseks ja märgitakse spetsiaalse atribuudiga, kui kanne *on fiskaalregistreerimisteenuses* registreeritud.

### <a name="offline-registration"></a>Võrguühenduseta registreerimine

Kui fiskaalregistreerimise teenus ei suuda kandeandmeid edastada maksuameti fiskaalveebiteenusele (nt vastuse ajalõpu tõttu) ja saada kinnitust veebiteenuselt (st kande fiskaal-ID kood), loob see kandele kohaliku allkirja ning kaasab selle ja vastuses spetsiaalse tõrkekoodi. Fiskaalregistreerimisteenus taassedab kanded algses järjestuses võrguühenduse taastamisel.

### <a name="limitations-of-the-sample"></a>Näidiste piirangud

Fiskaalregistreerimisteenus toetab ainult stsenaariume, kus hind sisaldab käibemaksu. Seetõttu peab nii kaupluste kui ka klientide puhul valik Hind **sisaldama** käibemaksu **väärtuseks** olema seatud Jah.

## <a name="set-up-commerce-for-the-czech-republic"></a>Häälestage Kaubandus Tšehhi Vabariigile.

See jaotis kirjeldab Kaubandussätteid, mis on Tšehhi Vabariigile omased ja soovitatavad. Lisateavet vt [Commerce'i](../index.md) kodulehelt.

Tšehhi-põhise funktsiooni kasutamiseks peate määrama järgmised sätted.

- Juriidilise isiku esmasel aadressil seadke välja **Riik/regioon** väärtuseks **CZECH** (Tšehhi Vabariik).
- Määrake iga Tšehhi Vabariigis paikneva kaupluse kassa funktsiooniprofiilis ISO-koodi välja väärtuseks **CZ** **·** (Tšehhi Vabariik).

Samuti peate määrama Tšehhi Vabariigi jaoks järgmised sätted. Pidage meeles, et pärast seadistuse lõpule viimist peate käivitama vastavad jaotustööd.

### <a name="set-up-vat-per-czech-republic-requirements"></a>KM-i seadistamine Tšehhi Vabariigi nõuete kohta


Peate looma käibemaksukoodid, käibemaksugrupid ja kauba käibemaksugrupid. Samuti peate häälestama toodete ja teenuste käibemaksuteabe. Lisateavet käibemaksu funktsioonide seadistamis- ja kasutus kohta leiate käibemaksu [ülevaatest](../../finance/general-ledger/indirect-taxes-overview.md).

### <a name="set-up-stores"></a>Kaupluste häälestamine

Lehel **Kõik** kauplused värskendage kaupluse üksikasju. Konkreetselt seadke järgmised parameetrid.

- Määrake **väljal** Käibemaksugrupp käibemaksugrupp, mida tuleks kasutada vaikekliendile müügi puhul.
- Seadke valiku **Hinnad sisaldavad käibemaksu** väärtuseks **Jah**.
- Seadke **välja** Nimi väärtuseks ettevõtte nimi. See muudatus aitab tagada, et ettevõtte nimi ilmub müügikviitungil. Teise võimalusena saate ettevõtte nime lisada müügikviitungi kavandile vabas vormis tekstina.
- Seadistage **maksu ID-koodi (TIN)** väli ettevõtte ID-koodile. See muudatus aitab tagada, et ettevõtte ID-number ilmub müügikviitungil. Teise võimalusena saate vabas vormis tekstina lisada müügikviitungi kavandile ettevõtte ID-koodi.

### <a name="set-up-functionality-profiles"></a>Funktsiooniprofiilide seadistamine

Kassa funktsiooniprofiilide seadistamine.

- Kiirkaardil Kviitungi nummerdamine seadistage kviitungite nummerdamine, luues või värskendades kirjeid **kandetüüpide** **·** **Müük**, Müügitellimus ja **Tagastatud** sissetulek jaoks.

### <a name="set-up-registration-numbers"></a>Saate häälestada registreerimisnumbreid.

1. Minge organisatsiooni **halduse \> globaalse aadressiraamatu \> registreerimistüüpide registreerimise \>** tüüpidele. Saate luua uue registreerimistüübi. Määrake **riigi/regiooni väli** **CZECH-le** (Tšehhi Vabariik) ja piirage see organisatsiooniga.
2. Minge organisatsiooni **halduse \> globaalse aadressiraamatu \> registreerimistüüpide registreerimise \>** kategooriatesse. Looge uus registreerimiskategooria. Valige eelmisest juhist registreerimise tüüp ja määrake **registreerimiskategooria** **väärtuseks Ettevõttesisese** ID.
3. Avage **Organisatsiooni haldamine \> Organisatsioonid \> Tootmisüksused**. Valige igale Tšehhi Vabariigis paiknevale kauplusele kauplusega seotud ühik. Laiendage **aadressi** kiirkaardil **ripploendit Veel** valikuid ja valige suvand **Täpsem**. 
4. Lehel **Aadresside haldamine** avatud peate määrama järgmise sätte.

    - Määrake aadressi **kiirkaardil** välja **Riik/regioon** väärtuseks **KUVA KUVA**.
    - Looge **registreerimis ID** kiirkaardil uus kirje. Valige varem loodud registreerimistüüp ja määrake registreerimisnumber.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Kohandatud väljade konfigureerimine, et neid saaks kasutada müügikviitungite kviitungi vormingutes

Saate konfigureerida keele teksti ja kohandatud väljad, mida kassa kviitungi vormingutes kasutatakse. Kviitungi häälestuse loonud kasutaja vaikeettevõte peaks olema sama juriidiline isik, kus keele teksti häälestus on loodud. Teise võimalusena tuleks samad keeletekstid luua nii kasutaja vaikeettevõttes kui ka kaupluse juriidilises isikus, mille jaoks häälestus on loodud.

Lisage **keele teksti** lehel kviitungi kavandite kohandatud väljade siltidele järgmised kirjed. Pange **tähele, et tabelis kuvatavad keele ID, teksti ID ja teksti väärtused** **on vaid** **näited**. Saate neid vastavalt oma nõuetele muuta. Teksi ID väärtused peavad siiski olema kordumatud ning võrduma või **olema** rohkem kui 900001.

Lisage tabelist keeleteksti **müügikoha** jaotisse **järgmised** müügikoha sildid:

| Keele ID | Teksti ID | Tekst                   |
|-------------|---------|------------------------|
| en-US       | 900001  | ID prov selle provania id/poklad id |
| en-US       | 900002  | BKP                    |
| en-US       | 900003  | PKP                    |
| en-US       | 900004  | FIK                    |
| en-US       | 900005  | Teave                   |
| en-US       | 900006  | Järjekorranumber        |

Lisage **kviitungi** kavandite kohandatud väljade jaoks kohandatud väljadele järgmised kirjed lehel Kohandatud väljad. Pange **tähele, et pealdise teksti ID väärtused peavad vastama teksti ID väärtustele, mille** **määrate** **keele** tekstilehel:

| Nimi                 | Tüüp    | Pealdise teksti ID |
|----------------------|---------|-----------------|
| TLT                  | Sissetulek | 900001          |
| SEC                  | Sissetulek | 900002          |
| MÄRK                 | Sissetulek | 900003          |
| EELARVE               | Sissetulek | 900004          |
| INFO                 | Sissetulek | 900005          |
| PIDEV NUMMERDAMINE     | Sissetulek | 900006          |

> [!NOTE]
> On oluline määrata õiged kohandatud väljanimed, nagu on loetletud eelmises tabelis. Vale kohandatud välja nimi põhjustab sissetulekutes puuduvate andmete.

### <a name="configure-receipt-formats"></a>Kviitungi vormingute konfigureerimine

Muutke iga nõutava kviitungi vormingu puhul välja **Prindikäitumine** väärtus väärtuseks Alati **prindi**.

Lisage kviitungi vormingu kujundajasse järgmised kohandatud väljad asjakohastele kviitungi jaotistele. Pange tähele, et väljanimed vastavad eelmises jaotises määratletud keeletekstidele.

- **Päis:** lisage järgmised väljad.

    - **Kaupluse nimi** ja **maksu** ID-kood: neid välju kasutatakse ettevõtte nime ja ID-numbri printimiseks sissetulekutele. Soovi korral saate kavandile lisada ka ettevõtte nime ja ID-numbri vabas vormis tekstina.
    - **Kaupluse** aadress, **kuupäev**, **kellaaeg 24** h, **kviitungi** number ja registri **number**.
    - **Järjekorranumber** : see väli tuvastab sularahakande numbri fiskaalregistreerimise teenuses.

- **Read:** lisage järgmised väljad.

    - **Kauba nimetus**
    - **Kogus**
    - **Hind kokku maksudega**

- **Jalus**: lisage järgmised väljad.

    - Makseväljad, nii et prinditakse iga makseviisi maksesummad. Lisage näiteks maksevahendi **nimi** ja **maksevahendi summa** väljad kavandi ühele reale.
    - **ID provfsovekvivalendi/poklad nii: sellel väljal prinditakse** ettevõtte valduste identifikaatorid ja kassaregister.
    - **BKP:** see väli prindib maksukohuslase turvakoodi, mille on määranud fiskaalregistreerimise teenus.
    - **FIK: see väli prindib maksuameti veebiteenuse määratud kande fiskaal-ID koodi eduka** võrgus registreerimise korral.
    - **PKP: see väli prindib maksukohuslase allkirjakoodi, mille** fiskaalregistreerimise teenus võrguühenduseta registreerimise korral loonud on.
    - **Teave:** see väli prindib fiskaalregistreerimise teenusest lisateavet.

Lisateavet kviitungi vormingutega töötades vt Kviitungi [vormingute häälestamine ja](../receipt-templates-printing.md) kujundamine.

## <a name="set-up-fiscal-integration-for-the-czech-republic"></a>SeadistaGe Tšehhi Vabariigile fiskaalintegratsioon

Tšehhi Vabariigi fiskaalregistreerimisteenuse integratsiooni näidis põhineb fiskaalintegratsiooni funktsioonil ja on osa [Retail](fiscal-integration-for-retail-channel.md) SDK-st. Näidis asub lahenduste hoidla **\\ kaustas FiscalIntegration \\ Efr (nt vabastamisnäide/9.33).**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/)[...](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr) Näidis [koosneb fiskaaldokumendi pakkujast, mis on Commerce Runtime'i () laiendus, ja fiskaalühendusest, mis](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices)CRT on Commerce Hardware Stationi laiendus. Lisateavet Retail SDK kasutamise kohta vt [Retail SDK arhitektuurist](../dev-itpro/retail-sdk/retail-sdk-overview.md) ja [iseseisva pakendamise SDK koostamisvõimaluste häälestamisest](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Uue sõltumatu pakendi- ja laiendusmudeli piirangute tõttu ei saa seda praegu selle [fiskaalintegratsiooni](../dev-itpro/build-pipeline.md) näidise jaoks kasutada. Retail SDK eelmist versiooni peate kasutama arendaja virtuaalmasinas (VM) Microsoft Dynamics elutsükli teenustes (LCS). Lisateavet vt Tšehhi Vabariigi [(pärand) fiskaalintegratsiooni näidise juurutuse](emea-cze-fi-sample-sdk.md) juhised.
>
> Uutesse versioonidesse planeeritakse fiskaalintegratsiooni valimite uue sõltumatu pakendi- ja laiendusmudeli tugi.

Viige finantsintegratsiooni seadistuse etapid lõpule, nagu on [kirjeldatud ärikanalite fiskaalintegratsiooni seadistamises:](setting-up-fiscal-integration-for-retail-channel.md)

1. [Seadistage fiskaalregistreerimise protsess](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Lisaks tehke märkus fiskaalregistreerimise protsessi sätete kohta, mis on sellele [fiskaalregistreerimise teenuse integreerimis näidisele omased.](#set-up-the-registration-process)
1. [Tõrke käsitlemise sätete](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings) seadistamine.
1. [Luba edasilükatud fiskaalregistreerimise käsitsi](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration) käivitamine.
1. [Kanali komponentide](#configure-channel-components) konfigureerimine.

### <a name="set-up-the-registration-process"></a>Registreerimisprotsessi häälestamine

Registreerimisprotsessi lubamiseks järgige neid samme Commerce headquartersi häälestamiseks. Lisateavet vt Commerce'i [kanalite fiskaalintegratsiooni](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process) häälestamine.

1. Laadige alla finantsdokumendi pakkuja ja fiskaalkonnektori konfiguratsioonifailid:

    1. Lahenduste [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) hoidla avamine.
    1. Valige õige väljalaske haruversioon vastavalt oma SDK-le/rakenduse versioonile (nt **[vabastamine/9.33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**
    1. Avatud **src \> FiscalIntegration \>** Efr.
    1. Laadige alla finantsdokumendi pakkuja konfiguratsioonifail konfiguratsioonifailis **\> Configurations DocumentProviders \> DocumentProviderFiscalEFRSampleTagemch.xml (nt väljalaske**[fail/9.33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders/DocumentProviderFiscalEFRSampleCzech.xml)
    1. Laadige alla fiskaalkonnektori **\> konfiguratsioonifail Configurations Connectors \> ConnectorEFRSample.xml** -is (nt [väljalaskefail/9.33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)

    > [!WARNING]
    > Uue sõltumatu pakendi- ja laiendusmudeli piirangute tõttu ei saa seda praegu selle [fiskaalintegratsiooni](../dev-itpro/build-pipeline.md) näidise jaoks kasutada. Retail SDK eelmist versiooni peate kasutama LCS-i arendaja VM-s. Selle fiskaalintegratsiooni näidiskonfiguratsiooni failid asuvad Retail SDK arendaja VM LCS-i kaustades:
    >
    > - **Fiskaaldokumendi pakkuja konfiguratsioonifail:** RetailSdk \\ SampleExtensions \\ CommerceRuntime \\ Extensions.DocumentProvider.EFRSample \\ Configuration \\ DocumentProviderFiscalEFRSampleKliendich.xml
    > - **Fiskaalkonnektori**\\ konfiguratsioonifail: RetailSdk SampleExtensions \\ HardwareStation \\ Extension.EFRSample \\ Configuration \\ ConnectorEFRSample.xml
    > 
    > Uutesse versioonidesse planeeritakse fiskaalintegratsiooni valimite uue sõltumatu pakendi- ja laiendusmudeli tugi.

1. Valige suvandid **Jaemüük ja kaubandus \> Headquartersi häälestus \> Parameetrid \> Commerce’i ühiskasutuses parameetrid**. Seadke **vahekaardil** Üldine suvand Luba **fiskaalintegratsioon** väärtusele **Jah**.
1. Minge jaemüügi **ja ärikanali häälestuse \>\> fiskaalintegratsiooni finantsdokumendi pakkujate juurde ja laadige varem alla \>** laaditud finantsdokumendi pakkuja konfiguratsioonifail.
1. Minge **jaemüügi- ja ärikanali \>\>\> häälestuse fiskaalintegratsiooni fiskaalkonnektori ja laadige varem alla** laaditud fiskaalkonnektori konfiguratsioonifail.
1. Minge jaemüügi ja **ärikanali \> häälestuse \> fiskaalintegratsiooni \> konnektori** funktsiooniprofiilidesse. Looge uus konnektori funktsiooniprofiil. Valige dokumendipakkuja ja ühendus, mille varem laadisite. Värskendage [andmevastendussätted](#default-data-mapping) vastavalt vajadusele.
1. Minge jaemüügi ja **ärikanali \> häälestuse \> finantsintegratsiooni \> konnektori tehnilistesse** profiilidesse. Looge uus konnektori tehniline profiil ja valige varem laaditud fiskaalühendus. Uuendage [konnektori](#fiscal-connector-settings) sätteid vastavalt vajadusele.
1. Minge jaemüügi ja **ärikanali \> häälestuse \> fiskaalintegratsiooni \> fiskaalühenduse gruppidesse**. Looge varem loodud konnektori funktsiooniprofiilile uus fiskaalühenduse grupp.
1. Minge jaemüügi **ja ärikanali häälestuse \> fiskaalintegratsiooni \>\> fiskaalregistreerimisprotsessidesse.** Looge uus fiskaalregistreerimise protsess ja fiskaalregistreerimise protsessi samm ning valige varem loodud fiskaalühenduse grupp.
1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassaprofiilid \> Funktsiooniprofiilid**. Valige funktsiooniprofiil, mis on lingitud kauplusega, kus registreerimisprotsess tuleks aktiveerida. Valige **finants registreerimisprotsessi** kiirkaardil varem loodud fiskaalregistreerimise protsess.
1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassaprofiilid \> Riistvaraprofiilid**. Valige riistvaraprofiil, mis on lingitud riistvarajaamaga, millega fiskaalprinter on ühendatud. Valige **kiirkaardil Fiscal** peripherals varem loodud konnektori tehniline profiil.
1. Avage jaotusgraafik (Retail ja Commerce Retail ja Commerce IT Distribution schedule) ning valige tööd **\>\>** **1070 ja** **1090 andmete** edastamiseks kanali andmebaasi.

#### <a name="default-data-mapping"></a>Vaikeandmete vastendamine

Järgmine vaikeandmete vastendamine on kaasatud fiskaaldokumendi pakkuja konfiguratsiooni, mis antakse fiskaalintegratsiooni näidisosana:

- **Käibemaksumäärade vastendamine: käibemaksukoodide jaoks seadistatud maksu protsendiväärtuste vastendamine fiskaalteenusele saadetud taotlustes** **atribuudi TaxG** (maksugrupp) väärtustega. Siin on vaikevastendus:

    ```
    A: 21.00; B: 15.00; C: 10.00; Z: 0.00
    ```

    Iga paari esimene komponent esindab käibemaksugruppi, mida toetab EFR-i fiskaalregistreerimisteenus. Teine komponent esindab vastavat KM-määra. Lisateavet käibemaksugruppide kohta, mida EFR Tšehhi Vabariigile toetab, vt [EFR-i](https://public.efsta.net/efr/) viidet.

- **KM-grupi vaikevastendus – kõik KM-summad, mida ei saa vastendada ühe ettemääratud KM-grupiga, seostatakse vaikimisi** (baas)KM-grupiga. Siin on vaikevastendus:

    ```
    A
    ```

- **Deposiitide** KM-grupi vastendamine – kliendi deposiidisummad ja kliendi tellimuse deposiidisummad seostatakse deposiidi KM-grupiga. Siin on vaikevastendus:

    ```
    Z
    ```

#### <a name="fiscal-connector-settings"></a>Fiskaalühenduse sätted

Järgmised sätted on kaasatud fiskaalkonnektori konfiguratsiooni, mis on antud fiskaalintegratsiooni näidisosana:

- **Lõpp**-punkti aadress – fiskaalregistreerimise teenuse URL.
- **Ajalõpp** – aja hulk millisekundites, mida fiskaalkonnektor fiskaalregistreerimise teenuse vastuse ootab.

### <a name="configure-channel-components"></a>Kanali komponentide konfigureerimine

> [!WARNING]
> Uue sõltumatu pakendi- ja laiendusmudeli piirangute tõttu ei saa seda praegu selle [fiskaalintegratsiooni](../dev-itpro/build-pipeline.md) näidise jaoks kasutada. Retail SDK eelmist versiooni peate kasutama LCS-i arendaja VM-s. Lisateavet vt Tšehhi Vabariigi [(pärand) fiskaalintegratsiooni näidise juurutuse](emea-cze-fi-sample-sdk.md) juhised.
>
> Uutesse versioonidesse planeeritakse fiskaalintegratsiooni valimite uue sõltumatu pakendi- ja laiendusmudeli tugi.

#### <a name="set-up-the-development-environment"></a>Saate häälestada arenduskeskkonda.

Arenduskeskkonna katsetada ja näidist laiendada, järgige neid samme.

1. Rakenduste hoidla [Dynamics 365 Commerce leidmine](https://github.com/microsoft/Dynamics365Commerce.Solutions) või allalaadimine. Valige õige väljalaske haruversioon vastavalt oma SDK-le/rakenduse versioonile. Lisateavet vt jaotisest Jaemüügi SDK näidised ja viitepakendid alla laadida [GitHub-st ja NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Avage EFR-i lahendus **rakenduses Dynamics365Commerce.Solutions \\ FiscalIntegration \\\\ EFR.sln** ja koostage see.
1. Installi CRT laiendid:

    1. Leidke laiendi CRT installer:

        - **Commerce Scale Unit: leidke kaustast** **Efr \\ ScaleUnit \\ ScaleUnit.EFR.Installer \\ bin \\ Debug \\ net461** **scaleUnit.EFR.Installer.**
        - **Kohalik CRT modern POS-s:** leidke **Efr \\\\ ModernPOS ModernPOS.EFR.Installeri \\ bin \\ Silumine \\ net461** **kaustast ModernPOS.EFR.Installer.**

    1. Käivitage CRT laiendiinstall käsurealt:

        - **Commerce Scalei üksus:**

            ```Console
            ScaleUnit.EFR.Installer.exe install --verbosity 0
            ```

        - **Kohalik CRT Modern POS-s:**

            ```Console
            ModernPOS.EFR.Installer.exe install --verbosity 0
            ```

1. Riistvarajaama laienduste installimine:

    1. Leidke **Efr \\ HardwareStation \\ HardwareStation.EFR.Installeri \\ bin \\ Silumine \\ net461 kaustast** **HardwareStation.EFR.Installer.**
    1. Käivitage laiendiinstall käsurealt:

        ```Console
        HardwareStation.EFR.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Tootmiskeskkond

Järgige fiskaalintegratsiooni näidise jaoks koostevõimaluste häälestamise etappe, et luua ja vabastada pilveskaala üksus ja iseteeninduse juurutatavad paketid [fiskaalintegratsiooni](fiscal-integration-sample-build-pipeline.md) näidiskomplekti jaoks. **EFR-i build-pipeline.yml malli JAML faili leiate lahenduste** **YAML_Files \\**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions) kaustast Müügivõimalustest.

## <a name="design-of-extensions"></a>Laienduste kujundus

Tšehhi Vabariigi fiskaalregistreerimisteenuse integratsiooni näidis põhineb fiskaalintegratsiooni funktsioonil ja on osa [Retail](fiscal-integration-for-retail-channel.md) SDK-st. Näidis asub lahenduste hoidla **\\ kaustas FiscalIntegration \\ Efr (nt vabastamisnäide/9.33).**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/)[...](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr) Näidis [koosneb](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) fiskaaldokumendi pakkujast, mis on CRT laiendiks, ja fiskaalühendusest, mis on Commerce Hardware Stationi laiendus. Lisateavet Retail SDK kasutamise kohta vt [Retail SDK arhitektuurist](../dev-itpro/retail-sdk/retail-sdk-overview.md) ja [iseseisva pakendamise SDK koostamisvõimaluste häälestamisest](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Uue sõltumatu pakendi- ja laiendusmudeli piirangute tõttu ei saa seda praegu selle [fiskaalintegratsiooni](../dev-itpro/build-pipeline.md) näidise jaoks kasutada. Retail SDK eelmist versiooni peate kasutama LCS-i arendaja VM-s. Lisateavet vt Tšehhi Vabariigi [(pärand) fiskaalintegratsiooni näidise juurutuse](emea-cze-fi-sample-sdk.md) juhised. Uutesse versioonidesse planeeritakse fiskaalintegratsiooni valimite uue sõltumatu pakendi- ja laiendusmudeli tugi.

### <a name="commerce-runtime-extension-design"></a>Äri käitusaja laiendi kujundus

Fiskaaldokumendi pakkuja laiendi eesmärk on luua teenusepõhiseid dokumente ja käsitleda fiskaalregistreerimise teenuse vastuseid.

#### <a name="request-handler"></a>Nõudeohjur

Dokumendipakkuja jaoks on üks **DocumentProviderEFRFiscalPF taotluseohjur, mida kasutatakse fiskaaldokumentide loomiseks** fiskaalregistreerimise teenuse jaoks.

See ohjur on päritud **INamedRequestHandler** liideselt. Meetod **HandlerName** vastutab ohjuri nime tagastamise eest. Ohjuri nimi peab vastama Commerce Headquartersis määratud konnektori dokumendi pakkuja nimele.

Konnektor toetab järgmisi taotlusi.

- **GetFiscalDocumentDocumentProviderRequest** – see taotlus sisaldab teavet selle kohta, milline dokument tuleks luua. See tagastab teenusepõhise dokumendi, mis tuleb registreerida fiskaalregistreerimise teenuses.
- **GetSupportedRegistrableEventsDocumentProviderRequest – see taotlus tagastab** tellitavate sündmuste loendi. Praegu toetatakse järgmisi sündmusi: müük, kliendikonto deposiidid ja kliendi tellimuse deposiitid.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest – see taotlus tagastab** fiskaalregistreerimise teenuse vastuse. See vastus järjestatakse stringi moodustamiseks nii, et see on salvestamiseks valmis.

#### <a name="configuration"></a>Konfiguratsioon

Fiskaaldokumendi pakkuja konfiguratsioonifail asub **lahenduste hoidlas src \\ FiscalIntegration \\ Efr \\ Konfiguratsioonide \\\\ DocumentProviderFiscalEFRSampleValdaja.xml.**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Faili eesmärk on lubada finantsdokumendi pakkuja sätete konfigureerimist rakendusest Commerce headquarters. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetele.

### <a name="hardware-station-extension-design"></a>Riistvarajaama laienduse kujundus

Fiskaalühenduseks olemise laiendi eesmärgiks on fiskaalregistreerimise teenusega suhtlemine. Riistvarajaama laiend kasutab HTTP-protokolli, et esitada dokumente, CRT mida laiend fiskaalregistreerimise teenusele loob. Samuti käsitletakse fiskaalregistreerimisteenuselt saadud vastuseid.

#### <a name="request-handler"></a>Nõudeohjur

**EFRHandler-i** taotluseohjur on sisenemispunkt fiskaalregistreerimise teenuse taotluste käsitlemiseks.

Ohjur pärineb **INamedRequestHandler** liideselt. Meetod **HandlerName** vastutab ohjuri nime tagastamise eest. Ohjuri nimi peab ühtima Commerce Headquartersis määratud fiskaalühenduse nimega.

Konnektor toetab järgmisi taotlusi.

- **SubmitDocumentFiscalDeviceRequest – see taotlus saadab dokumendid fiskaalregistreerimise teenusesse ja** tagastab sellelt vastuse.
- **IsReadyFiscalDeviceRequest – seda taotlust kasutatakse** fiskaalregistreerimise teenuse seisundikontrolliks
- **InitializeFiscalDeviceRequest** – seda taotlust kasutatakse fiskaalregistreerimise teenuse lähtestamiseks

#### <a name="configuration"></a>Konfiguratsioon

Fiskaalkonnektori konfiguratsioonifail asub lahenduste **hoidlas src \\ FiscalIntegration \\ Efr \\\\ Configurations Connectors \\ ConnectorEFRSample.xml.**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Faili eesmärk on lubada finantsühenduse sätete konfigureerimist rakendusest Commerce headquarters. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetele.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
