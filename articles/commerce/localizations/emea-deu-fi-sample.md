---
title: Fiskaalüksuse registreerimisteenuse integratsiooni näide Saksamaa jaoks
description: Selles teemas antakse ülevaade Fiskaalintegratsiooni näidistest Saksamaa jaoks Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2020-5-29
ms.openlocfilehash: ca747215a8dfb85237365880ad5bdd49e57ec949
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944684"
---
# <a name="fiscal-registration-service-integration-sample-for-germany"></a>Fiskaalüksuse registreerimisteenuse integratsiooni näide Saksamaa jaoks

[!include[banner](../includes/banner.md)]

Selles teemas antakse ülevaade Fiskaalintegratsiooni näidistest Saksamaa jaoks Microsoft Dynamics 365 Commerce.

Saksamaa kassaraamatute kohalike fiskaalnõuete täitmiseks hõlmab Saksamaa funktsioon kassa (POS) näidisintegratsiooni Microsoft Dynamics 365 Commerce välise fiskaalregistreerimise teenusega. Näidis laiendab [fiskaalintegratsiooni funktsioone](fiscal-integration-for-retail-channel.md). See põhineb [EFSTA](https://www.efsta.eu/de/) [EFR-i (elektroonilise finantsregistri)](https://www.efsta.eu/de/fiskalloesungen/deutschland) lahendusel ja võimaldab HTTPS-protokolli kaudu sidet EFR-teenusega. EFR-teenus peab olema majutatud kas jaemüügi riistvarajaamas või eraldi arvutis, mida saab ühendada riistvarajaamaga. Näidis esitatakse lähtekoodina ja on osa jaemüügi tarkvara arenduskomplektist (SDK).

Microsoft ei vabasta EFSTA-st riistvara, tarkvara ega dokumentatsiooni. Lisateabeks selle kohta, kuidas saada EFR-lahendust ja seda kasutada, võtke ühendust [EFSTA-ga.](https://www.efsta.eu/de/kontakt/kontakt)

## <a name="scenarios"></a>Stsenaariumid

Järgmisi stsenaariume hõlmab Fiskaalregistreerimise teenuse integreerimisnäide Saksamaa jaoks.

### <a name="sales-operations"></a>Müügitoimingud

- **Sularaha ja müügi müügi ning tagastuste registreerimine fiskaalregistreerimisteenuses:**

    Müügitoimingute registreerimine sisaldab järgmisi samme:

    1. Kande alguse registreerimine

        Iga kande algus registreeritakse EFR-teenusega ühendatud tehnilises turvaelemendis (TSE). Registreerimise tulemusena määrab TID kande ID.

    2. Kande lõpu registreerimine

        Kui kanne müügikohas lõpetatakse, registreeritakse see, kasutades sama TID-d, mis määrati kande alguse registreerimiseks. Sel hetkel saadetakse üksikasjalikud kandeandmed fiskaalregistreerimise teenusesse. Need andmed sisaldavad müügirea teavet ning allahindluste, maksete ja maksude teavet.

    3. Fiskaalregistreerimisteenuse vastuse kogumine

        Turbeandmed on saadud TSE-st vastuse osana ja salvestatakse kandesse kanali andmebaasis. Turbeandmed sisaldavad järgmist teavet.

        - TID
        - Kande alguse kuupäev ja kellaaeg
        - Kande lõppkuupäev ja -kellaaeg
        - Allkirjaloendur
        - Kontrolli väärtust
        - TSE seerianumber

- **Klienditellimuste registreerimine fiskaalregistreerimise teenuses on sama, mis sularaha** ja edasimüügi müügi ja tagastuste protsess.
- **Operatsioonide registreerimine, mis hõlmab kinkekaarte ja deposiite. Registreerimisprotsess on sama, mis sularaha** ja kandke müügi ja tagastuste protsess.

#### <a name="notifying-users-about-fiscal-registration-failures"></a>Kasutajate teatamine fiskaalregistreerimise tõrgetest

Fiskaalregistreerimisteenus saab kasutajaid fiskaalregistreerimise ajal ilmnenud tõrgetest teavitada kahel viisil:

- Prindib vastusest lisateavet **kviitungite** teabeväljale.
- Kuvage fiskaalteenuse teatised kassas kasutajateadetena.

    > [!NOTE]
    > Selle teavitusmehhanismi puhul peab **fiskaalregistreerimise teatiste** parameetri kuvamine lehel **Konnektori tehnilised** profiilid olema sisse lülitatud.

#### <a name="printing-receipts"></a>Kviitungite printimine

Kviitungi printimine on Saksamaal kohustuslik. Kõik sissetulekud peavad sisaldama vähemalt järgmist teavet:

- Ettevõtte nimi ja aadress
- Kaupade teave, k.a nende hinnad ja kogused
- Saadud maksete teave
- Maksude teave, k.a kogusummad maksumäära kohta
- Turvaandmed:

    - TID
    - Kande alguse kuupäev ja kellaaeg
    - Kande lõppkuupäev ja -kellaaeg
    - Allkirjaloendur
    - Kontrolli väärtust
    - TSE seerianumber

- Teade

> [!NOTE]
> Kviitungitele saab printida ka QR-koodi. Kuigi QR-kood on valikuline, on see väga soovitatav. Lisateavet selle kohta, kuidas saada QR-koodi fiskaalregistreerimise teenuse vastuse osana, vt "EFR-i juhend \[\] DE", mis avaldatakse [EFSTA dokumentatsiooni](https://public.efsta.net/efr/) veebisaidil.
>
> **Sissetulekute** teabeteate väli näitab fiskaalregistreerimise teenuse teatist. Näiteks allkirjaseadme katkemisel saab kviitungil printida eriteksti.

#### <a name="voided-suspended-and-recalled-transactions"></a>Tühistatud, peatatud ja tühistatud kanded

- Tühistatud kanne registreeritakse taotlusena fiskaalregistreerimise teenuses kande lõpetamiseks.
- Peatatud kanne on registreeritud taotlusena lõpetada kanne fiskaalregistreerimise teenuses.
- Peatatud kande tagasikutsumine registreeritakse uue kande alguses fiskaalregistreerimise teenuses.

### <a name="non-sales-transactions-and-shift-closing"></a>Mittemüügikanded ja vahetuse sulgemine

Järgmised mittemüügikanded registreeritakse fiskaaltoimingutena fiskaalregistreerimise teenuses **NFS-sildi** abil:

- Deklareeri algsumma
- Sularaha sissemakse
- Väljamakse
- Seifi viidav raha
- Raha hoiustamine panka
- Tulukontod
- Kulukontod

Vahetuse **sulgemise toiming on registreeritud ka** mittefiskaalse toiminguna fiskaalregistreerimise **teenuses, kasutades NFS-silti.**

### <a name="data-export-and-audit"></a>Andmete eksport ja audit

Kõik kanded peab OLEMA TSE allkirjastatud, et tagada nende terviklikkus, autentsus ja terviklikkus ning ennetada kirjendatud andmete manipulatsioone.

> [!WARNING]
> Kasutada saab ainult sertifitseeritud TSE-d. Teavet EFR-i lahenduses toetatud TSE-de tüüpide ja mudelite kohta vt "EFR-i juhend \[\] DE", mis avaldatakse [EFSTA dokumentatsiooni](https://public.efsta.net/efr/) veebisaidil. Lisateabe saamiseks TSE valiku ja hankimise kohta võtke ühendust [EFSTA-ga.](https://www.efsta.eu/at/kontakt)

Saksamaa määrustega nõutakse eksporti DSFinV-K tuge. DSFinV-K ekspordi saab käivitada EFR-i lahenduses. Lisateavet DSFinV-K ekspordi kohta vt "EFR-i juhend \[\] DE", mis avaldatakse [EFSTA dokumentatsiooni](https://public.efsta.net/efr/) veebisaidil.

### <a name="limitations-of-the-sample"></a>Näidiste piirangud

Fiskaalregistreerimisteenus toetab ainult stsenaariume, kus hindades sisaldub käibemaks. Seetõttu peab nii kaupluste kui ka klientide puhul valiku Hinnad sisaldavad **käibemaksu** **väärtuseks** olema seatud Jah.

Fiskaalteenus ei toeta olukordi, kus samale kandereale rakendatakse rohkem kui ühte käibemaksukoodi.

Fiskaalintegratsiooni raamistik ei toeta müügipakkumist. Seetõttu ei ole neid toiminguid fiskaalteenuses registreeritud.

## <a name="set-up-commerce-for-germany"></a>Häälestage Saksamaa äri

See jaotis kirjeldab Ärisätteid, mis on Saksamaale spetsiifilised ja soovitatavad. Lisateavet häälestuse kohta vt [Commerce'i](../index.md) kodulehelt.

Saksamaale omase funktsiooni kasutamiseks peate määrama järgmised sätted.

- Määrake juriidilise isiku esmasel aadressil väli **Riik/regioon** DEU-ks **·** (Saksamaa).
- Seadke iga Saksamaal asuv kaupluse kassa funktsiooniprofiilis **ISO-koodi väli** väärtusele **DE** (Saksamaa).

Peate määrama ka Saksamaa jaoks järgmised sätted. Käitage vastavad jaotustööd kindlasti pärast seadistuse lõpule viimist.

### <a name="set-up-vat-per-german-requirements"></a>KM-i seadistamine Saksa nõuete kohta

Peate looma käibemaksukoodid, käibemaksugrupid ja kauba käibemaksugrupid. Samuti peate häälestama toodete ja teenuste käibemaksuteabe. Lisateavet käibemaksu funktsioonide seadistamis- ja kasutus kohta leiate käibemaksu [ülevaatest](../../finance/general-ledger/indirect-taxes-overview.md).

Müügikviitungitele saate printida käibemaksukoodi lühendi (nt "A" või "B"). Selle funktsiooni kasutamiseks seadistage **käibemaksukoodide** lehel välja **printimiseks** kood.

### <a name="set-up-stores"></a>Kaupluste häälestamine

Lehel **Kõik** kauplused värskendage kaupluse üksikasju. Konkreetselt määrake järgmised parameetrid:

- Määrake **väljal** Käibemaksugrupp käibemaksugrupp, mida tuleks kasutada vaikekliendile müügi puhul.
- Seadke valiku **Hinnad sisaldavad käibemaksu** väärtuseks **Jah**.
- Seadke **välja** Nimi väärtuseks ettevõtte nimi. See muudatus aitab tagada, et ettevõtte nimi ilmub müügikviitungil. Teise võimalusena saate ettevõtte nime lisada müügikviitungi kavandile vabas vormis tekstina.
- Seadistage **maksu ID-koodi (TIN)** väli ettevõtte ID-koodile. See muudatus aitab tagada, et ettevõtte ID-kood ilmub müügikviitungil. Teise võimalusena saate vabas vormis tekstina lisada müügikviitungi kavandile ettevõtte ID-koodi.

### <a name="set-up-functionality-profiles"></a>Funktsiooniprofiilide seadistamine

Kassa funktsiooniprofiilide seadistamine. Kiirkaardil Kviitungi nummerdamine seadistage kviitungite nummerdamine, luues või värskendades kirjeid **kandetüüpide** **·** **Müük**, Müügitellimus ja **Tagastatud** sissetulek jaoks.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Kohandatud väljade konfigureerimine, et neid saaks kasutada müügikviitungite kviitungi vormingutes

Saate konfigureerida keele teksti ja kohandatud väljad, mida kassa kviitungi vormingutes kasutatakse. Kviitungi häälestuse loonud kasutaja vaikeettevõte peaks olema sama juriidiline isik, kus keele teksti häälestus on loodud. Teise võimalusena tuleks samad keeletekstid luua nii kasutaja vaikeettevõttes kui ka kaupluse juriidilises isikus, mille jaoks häälestus on loodud.

Lisage **keele teksti** lehel kviitungi kavandite kohandatud väljade siltidele järgmised kirjed. Pange **tähele, et tabelis kuvatavad keele ID, teksti ID ja teksti väärtused** **on vaid** **näited**. Saate neid vastavalt oma nõuetele muuta. Teksi ID väärtused peavad siiski olema kordumatud ning võrduma või **olema** rohkem kui 900001.

Lisage keele tekstilehe **müügikoha** jaotisse järgmised **müügikoha** sildid.

| Keele ID | Teksti ID | Tekst                                  |
|-------------|---------|---------------------------------------|
| en-US       | 900001  | QR-kood                               |
| en-US       | 900002  | Kande ID                        |
| en-US       | 900003  | Maksu jaemüügi prindikood                 |
| en-US       | 900004  | Maksusumma (müük)                    |
| en-US       | 900005  | Maksu alus (müük)                     |
| en-US       | 900006  | Kande alguskuupäeva kellaaeg           |
| en-US       | 900007  | Kande lõppkuupäeva kellaaeg             |
| en-US       | 900008  | Turbeelemendi seerianumber |
| en-US       | 900009  | Allkirjaloendur                     |
| en-US       | 900010  | Kontrolli väärtust                           |
| en-US       | 900011  | Teabeteade                          |

Lisage **kviitungi** kavandite kohandatud väljade jaoks kohandatud väljadele järgmised kirjed lehel Kohandatud väljad. Pange tähele, **et pealdise teksti ID** väärtused peavad vastama teksti ID **väärtustele, mille** määrate keele teksti **lehel**.

| Nimi                            | Tüüp    | Pealdise teksti ID |
|---------------------------------|---------|-----------------|
| QRCODE \_ DE                      | Sissetulek | 900001          |
| TRANSACTIONID \_ DE               | Sissetulek | 900002          |
| PROGRAMMI RETAILPRINTCODE \_ DE             | Sissetulek | 900003          |
| SALESTAMOUNT \_ DE              | Sissetulek | 900004          |
| SALESTAXBASIS \_ DE               | Sissetulek | 900005          |
| KANNETEARTDATETIME \_ DE    | Sissetulek | 900006          |
| KANDEENDDATETIME \_ DE      | Sissetulek | 900007          |
| SECURITYELEMENTSERIALNUMBER \_ DE | Sissetulek | 900008          |
| SIGNCOUNTER \_ DE                 | Sissetulek | 900009          |
| ALLKIRJASTA \_ DE                        | Sissetulek | 900010          |
| TEABEMESSAGE \_ DE                 | Sissetulek | 900011          |

> [!NOTE]
> On oluline määrata õiged kohandatud väljanimed, nagu on loetletud eelmises tabelis. Vale kohandatud välja nimi põhjustab sissetulekutes puuduvate andmete.

### <a name="configure-receipt-formats"></a>Kviitungi vormingute konfigureerimine

Muutke iga nõutava kviitungi vormingu välja Prindikäitumine **väärtuseks** Alati **prindi**.

Lisage kviitungi vormingu kujundajasse järgmised kohandatud väljad asjakohastele kviitungi jaotistele. Pange tähele, et väljanimed vastavad eelmises jaotises määratletud keeletekstidele.

- **Päis:** lisage järgmised väljad:

    - **Kaupluse nime** ja **maksu ID-koodi** väljad, mida kasutatakse ettevõtte nime ja ID-koodi printimiseks kviitungitele. Soovi korral saate kavandile lisada ka ettevõtte nime ja ID-koodi vabas vormis tekstina.
    - **Kaupluse** aadressi, **kuupäeva**, **kellaaja 24** h, **kviitungi** numbri ja registri **numbriväljad**

- **Read:** lisage järgmised väljad:

    - **Kauba nime** väli
    - **Koguse** väli
    - **Hind kokku** maksuväljaga
    - **Maksu jaemüügi prindikoodi väli, mida kasutatakse kaubale kehtivale käibemaksukoodile vastava** lühendatud koodi printimiseks

- **Jalus:** lisage järgmised väljad:

    - Makseväljad, nii et prinditakse iga makseviisi maksesummad. Lisage näiteks maksevahendi **nimi** ja **maksevahendi summa** väljad kavandi ühele reale.
    - Maksuväljade **väljagrupi** väljad. Kõik selle väljagrupi väljad tuleb printida ühele eraldi reale.

        - **Maksu ID** väli, mis on standardne väli, mis võimaldab printida käibemaksu kokkuvõtte iga käibemaksukoodi kohta. See väli tuleb lisada uuele reale.
        - **Maksuprotsendi** väli, mis on standardväli, mida kasutatakse käibemaksukoodi efektiivse maksumäära printimiseks.
        - **Välja Maksu alus** (müük), mida kasutatakse sissetuleku sularahamüügi kogusumma printimiseks käibemaksukoodi kohta. Ettemaksed ja kinkekaarditoimingud on välja jäetud.
        - **Maksusumma (müük), mida kasutatakse selle käibemaksukoodi puhul sularahamüügi** sissetuleku maksusumma printimiseks.
        - **Maksu jaemüügi prindikoodi väli, mida kasutatakse käibemaksukoodile vastava lühendatud** koodi printimiseks.

    - Väljad, mis sisaldavad fiskaalregistreerimise teenuse tagastatud turvatud kandeandmeid:

        - **Kande ID** väli, mis tuvastab kassakande numbri fiskaalregistreerimise teenuses
        - **Kande alguskuupäeva kellaaja** väli
        - **Kande lõppkuupäeva kellaaja** väli
        - **Turvaelemendi välja** seerianumber
        - **Allkirjaloenduri** väli
        - **Kontrolli väärtuse** välja
        - **QR-koodi väli, mida kasutatakse viite printimiseks registreeritud** sularahakandele QR-koodina

        > [!NOTE]
        > **QR-koodi** väärtus tuuakse fiskaalregistri vastusest. EFR tagastab oma vastuses QR-koodi ainult siis, kui EFR-i konfiguratsiooni atribuutide välja väärtust on **kirjeldatud** EFSTA dokumentatsioonis. EFR-i konfiguratsiooni **atribuutide väljal tuleb** QR-koodi vorming seada **BMP-le.**

    - **Teabeteate** väli, nii et fiskaalregistreerimisteenuse teavitusteateid saab kuvada kviitungitel. Näiteks allkirjaseadme katkemisel saab kviitungil printida eriteksti.

Lisateavet kviitungi vormingutega töötades vt Kviitungi [vormingute häälestamine ja](../receipt-templates-printing.md) kujundamine.

## <a name="set-up-fiscal-integration-for-germany"></a>Saate häälestada Saksamaa fiskaalintegratsiooni.

Saksamaa fiskaalregistreerimisteenuse integreerimise näidis põhineb [fiskaalintegratsiooni funktsioonil ja](fiscal-integration-for-retail-channel.md) on osa Retail SDK-st. Näidis asub lahenduste hoidla **\\ kaustas FiscalIntegration \\ Efr (nt vabastamisnäide/9.33).**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/)[...](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr) Näidis [koosneb fiskaaldokumendi pakkujast, mis on Commerce Runtime'i () laiendus, ja fiskaalühendusest, mis](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices)CRT on Commerce Hardware Stationi laiendus. Lisateavet Retail SDK kasutamise kohta vt [Retail SDK arhitektuurist](../dev-itpro/retail-sdk/retail-sdk-overview.md) ja [iseseisva pakendamise SDK koostamisvõimaluste häälestamisest](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Uue sõltumatu pakendi- ja laiendusmudeli piirangute tõttu ei saa seda praegu selle [fiskaalintegratsiooni](../dev-itpro/build-pipeline.md) näidise jaoks kasutada. Retail SDK eelmist versiooni peate kasutama arendaja virtuaalmasinas (VM) Microsoft Dynamics elutsükli teenustes (LCS). Lisateavet vt Saksamaa [fiskaalintegratsiooni näidise juurutuse juhistest](emea-deu-fi-sample-sdk.md) (pärand).
>
> Uutesse versioonidesse planeeritakse fiskaalintegratsiooni valimite uue sõltumatu pakendi- ja laiendusmudeli tugi.

Viige finantsintegratsiooni seadistuse etapid lõpule, nagu on [kirjeldatud ärikanalite fiskaalintegratsiooni seadistamises:](setting-up-fiscal-integration-for-retail-channel.md)

1. [Seadistage fiskaalregistreerimise protsess](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Lisaks tehke märkus fiskaalregistreerimise protsessi sätete kohta, mis on sellele [fiskaalregistreerimise teenuse integreerimis näidisele omased.](#set-up-the-registration-process)
1. [Tõrke käsitlemise sätete](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings) seadistamine.

    > [!WARNING]
    > Fiskaalintegratsiooni raamistiku tõrke käsitlemise võimalused ei pruugi olla täielikult joondatud kohalike finantseeskirjadega.
    >
    > - Soovitame jätta suvand Jätka tõrke korral fiskaalregistreerimise protsessi lehel välja lülitatud, sest kõik kanded peavad olema korrektselt registreeritud, isegi kui fiskaalregistreerimise esimene katse **ei** **õnnestunud**.
    > - Enne kui lülitate fiskaalregistreerimise protsessi lehel sisse suvandi Skip või Mark registreeritud, peaksite käsitlema neid fiskaalregistreerimise protsessi muudatusi oma maksunõustaja või **kohaliku** **·** **maksuametiga**.

1. [Luba edasilükatud fiskaalregistreerimise käsitsi](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration) käivitamine.
1. [Kanali komponentide](#configure-channel-components) konfigureerimine.

### <a name="set-up-the-registration-process"></a>Registreerimisprotsessi häälestamine

Registreerimisprotsessi lubamiseks järgige neid samme Commerce headquartersi häälestamiseks. Lisateavet vt Commerce'i [kanalite fiskaalintegratsiooni](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process) häälestamine.

1. Laadige alla finantsdokumendi pakkuja ja fiskaalkonnektori konfiguratsioonifailid:

    1. Lahenduste [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) hoidla avamine.
    1. Valige õige väljalaske haruversioon vastavalt oma SDK-le/rakenduse versioonile (nt **[vabastamine/9.33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**
    1. Avatud **src \> FiscalIntegration \>** Efr.
    1. Laadige alla finantsdokumendi pakkuja konfiguratsioonifail konfiguratsioonifailis **\> Configurations DocumentProviders \> DocumentProviderFiscalEFRSampleGermany.xml (nt väljalaske**[fail/9.33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders/DocumentProviderFiscalEFRSampleGermany.xml)
    1. Laadige alla fiskaalkonnektori **\> konfiguratsioonifail Configurations Connectors \> ConnectorEFRSample.xml** -is (nt [väljalaskefail/9.33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)

    > [!WARNING]
    > Uue sõltumatu pakendi- ja laiendusmudeli piirangute tõttu ei saa seda praegu selle [fiskaalintegratsiooni](../dev-itpro/build-pipeline.md) näidise jaoks kasutada. Retail SDK eelmist versiooni peate kasutama LCS-i arendaja VM-s. Selle fiskaalintegratsiooni näidiskonfiguratsiooni failid asuvad Retail SDK arendaja VM LCS-i kaustades:
    >
    > - **Fiskaaldokumendi pakkuja konfiguratsioonifail:** RetailSdk \\ SampleExtensions \\ CommerceRuntime \\ Extensions.DocumentProvider.EFRSample \\ Configuration \\ DocumentProviderFiscalEFRSampleGermany.xml
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

- **Maksevahendi tüübi vastendamine: makseviiside vastendamine** **atribuudi PayG (maksegrupp) väärtustega fiskaalteenusesse** saadetud taotlustes. Siin on vaikevastendus:

    ```
    1: 0; 2: 1; 3: 3; 4: 8; 5: 2; 6: 0; 7: 7; 8: 6; 9: 0; 10: 8; 11: 1
    ```

    Iga paari esimene komponent esindab kauplusele seadistatud makseviisi. Teine komponent tähistab vastavat maksegruppi, mida toetab EFR-i fiskaalregistreerimisteenus. Lisateavet maksegruppide kohta, mida EFR Saksamaale toetab, vt [EFR-i viidet](https://public.efsta.net/efr/).

    Makseviiside näidisvastendus vastab kaupluse maksemeetoditele, mis on konfigureeritud standardsete demoandmetega.

    | Makseviis | Makseviisi nimi |
    |----------------|---------------------|
    | 1              | Sularaha                |
    | 2              | Kontroll               |
    | 3              | Kaart                |
    | 4              | Kliendi konto    |
    | 5              | Muud               |
    | 6              | Valuuta            |
    | 7              | Vautšer             |
    | 8              | Kinkekaart           |
    | 9              | Väljamakse-/vahetusraha |
    | 10             | Kliendikaardid       |
    | 11             | Mitte kohalikud tšekid    |

    Seega peate muutma näidisvastendust vastavalt maksemeetoditele, mis on teie rakenduses konfigureeritud.

- **Kaasa kliendiandmed – kui see parameeter on sisse lülitatud, sisaldavad rahandusteenuse taotlused klienditeavet, nt nimesid ja aadresse, juhul kui klient lisatakse** kandesse.
- **Käibemaksumäärade vastendamine: käibemaksukoodide jaoks seadistatud maksu protsendiväärtuste vastendamine fiskaalteenusele saadetud taotlustes** **atribuudi TaxG** (maksugrupp) väärtustega. Siin on vaikevastendus:

    ```
    A: 19.00; B: 7.00; C: 10.70; D: 5.50; E: 0.00
    ```

    Iga paari esimene komponent esindab käibemaksugruppi, mida toetab EFR-i fiskaalregistreerimisteenus. Teine komponent esindab vastavat KM-määra. Lisateavet käibemaksugruppide kohta, mida EFR Saksamaale toetab, vt [EFR-i](https://public.efsta.net/efr/) viidet.

- **Maksugrupp kinkekaartide ja deposiitide jaoks – TaxG atribuudi väärtus fiskaalteenusele saadetud taotlustes, mis põhinevad kinkekaarte või** **deposiite** kaasatud toimingutel. Siin on vaikevastendus:

    ```
    G
    ```

- **Käibemaksuvabastuse maksugrupp – atribuudi TaxG väärtus fiskaalteenusele saadetud taotlustes, mis põhinevad maksukohustustest** **vabastatud** toimingutel. Siin on vaikevastendus:

    ```
    F
    ```

> [!NOTE]
> Vaikeandmete vastenduse maksusätted vastutavad vastavate maksusätete eest süsteemis ja maksugruppide eest EFR-teenuses. Maksugruppe saab kviitungitele printida ainult siis, **kui** prinditav kood on **seadistatud käibemaksukoodide** lehele.

#### <a name="fiscal-connector-settings"></a>Fiskaalühenduse sätted

Järgmised sätted on kaasatud fiskaalkonnektori konfiguratsiooni, mis on antud fiskaalintegratsiooni näidisosana:

- **Lõpp**-punkti aadress – fiskaalregistreerimise teenuse URL.
- **Ajalõpp** – aja hulk millisekundites, mida fiskaalkonnektor fiskaalregistreerimise teenuse vastuse ootab.
- **Kuva fiskaalregistreerimise teatised – see lipp** kontrollib, kas fiskaalregistreerimise teenuse tagastused tuleb operaatorile kuvada.

### <a name="configure-channel-components"></a>Kanali komponentide konfigureerimine

> [!WARNING]
> Uue sõltumatu pakendi- ja laiendusmudeli piirangute tõttu ei saa seda praegu selle [fiskaalintegratsiooni](../dev-itpro/build-pipeline.md) näidise jaoks kasutada. Retail SDK eelmist versiooni peate kasutama LCS-i arendaja VM-s. Lisateavet vt Saksamaa [fiskaalintegratsiooni näidise juurutuse juhistest](emea-deu-fi-sample-sdk.md) (pärand).
>
> Uutesse versioonidesse planeeritakse fiskaalintegratsiooni valimite uue sõltumatu pakendi- ja laiendusmudeli tugi.

#### <a name="set-up-the-development-environment"></a>Saate häälestada arenduskeskkonda.

Arenduskeskkonna katsetada ja näidist laiendada, järgige neid samme.

1. Rakenduste hoidla [Dynamics 365 Commerce leidmine](https://github.com/microsoft/Dynamics365Commerce.Solutions) või allalaadimine. Valige õige väljalaske haruversioon vastavalt oma SDK-le/rakenduse versioonile. Lisateavet vt jaotisest Jaemüügi SDK näidised ja viitepakendid alla laadida [GitHub-st ja NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Avage EFR-i lahendus **rakenduses Dynamics365Commerce.Solutions \\ FiscalIntegration \\\\ EFR.sln** ja koostage see.
1. Commerce'i käitusaja laienduste installimine:

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

    - Leidke **Efr \\ HardwareStation \\ HardwareStation.EFR.Installeri \\ bin \\ Silumine \\ net461 kaustast** **HardwareStation.EFR.Installer.**
    - Käivitage laiendiinstall käsurealt:

        ```Console
        HardwareStation.EFR.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Tootmiskeskkond

Järgige fiskaalintegratsiooni näidise jaoks koostevõimaluste häälestamise etappe, et luua ja vabastada pilveskaala üksus ja iseteeninduse juurutatavad paketid [fiskaalintegratsiooni](fiscal-integration-sample-build-pipeline.md) näidiskomplekti jaoks. **EFR-i build-pipeline.yml malli JAML faili leiate lahenduste** **YAML_Files \\**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions) kaustast Müügivõimalustest.

## <a name="design-of-extensions"></a>Laienduste kujundus

Saksamaa fiskaalregistreerimisteenuse integreerimise näidis põhineb [fiskaalintegratsiooni funktsioonil ja](fiscal-integration-for-retail-channel.md) on osa Retail SDK-st. Näidis asub lahenduste hoidla **\\ kaustas FiscalIntegration \\ Efr (nt vabastamisnäide/9.33).**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/)[...](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr) Näidis [koosneb](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) fiskaaldokumendi pakkujast, mis on CRT laiendiks, ja fiskaalühendusest, mis on Commerce Hardware Stationi laiendus. Lisateavet Retail SDK kasutamise kohta vt [Retail SDK arhitektuurist](../dev-itpro/retail-sdk/retail-sdk-overview.md) ja [iseseisva pakendamise SDK koostamisvõimaluste häälestamisest](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Uue sõltumatu pakendi- ja laiendusmudeli piirangute tõttu ei saa seda praegu selle [fiskaalintegratsiooni](../dev-itpro/build-pipeline.md) näidise jaoks kasutada. Retail SDK eelmist versiooni peate kasutama LCS-i arendaja VM-s. Lisateavet vt Saksamaa [fiskaalintegratsiooni näidise juurutuse juhistest](emea-deu-fi-sample-sdk.md) (pärand). Uutesse versioonidesse planeeritakse fiskaalintegratsiooni valimite uue sõltumatu pakendi- ja laiendusmudeli tugi.

### <a name="crt-extension-design"></a>CRT laiendi kujundus

Fiskaaldokumendi pakkuja laiendi eesmärk on luua teenusepõhiseid dokumente ja käsitleda fiskaalregistreerimise teenuse vastuseid.

#### <a name="request-handler"></a>Nõudeohjur

Dokumendipakkujal **DocumentProviderEFRFiscalDEU on üks** taotluseohjur. Seda ohjurit kasutatakse fiskaaldokumentide loomiseks fiskaalregistreerimise teenusele. See pärineb **INamedRequestHandler** liideselt. Meetod **HandlerName** vastutab ohjuri nime tagastamise eest. Ohjuri nimi peab vastama Commerce Headquartersis määratud konnektori dokumendi pakkuja nimele.

Konnektor toetab järgmisi taotlusi:

- **GetFiscalDocumentDocumentProviderRequest** – see taotlus sisaldab teavet selle kohta, milline dokument tuleks luua. See tagastab teenusepõhise dokumendi, mis tuleb registreerida fiskaalregistreerimise teenuses.
- **GetFiscalTransactionExtendedDataDocumentProviderRequest – see taotlus tagastab vastuse** koos laiendatud andmetega.

#### <a name="configuration"></a>Konfiguratsioon

Fiskaaldokumendi pakkuja konfiguratsioonifail asub lahenduste **hoidlas src \\ FiscalIntegration \\ Efr \\ Konfiguratsioonide \\\\ DocumentProviderFiscalEFRSampleGermany.xml.**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Faili eesmärk on lubada finantsdokumendi pakkuja sätete konfigureerimist rakendusest Commerce headquarters. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetele.

### <a name="hardware-station-extension-design"></a>Riistvarajaama laienduse kujundus

Fiskaalühenduseks olemise laiendi eesmärgiks on fiskaalregistreerimise teenusega suhtlemine.

Riistvarajaama laiend **onHardwareStation.Extension.EFRSample.** See kasutab HTTP-protokolli, et esitada dokumente, CRT mida laiend finantsregistreerimise teenusele loob. Samuti käsitletakse fiskaalregistreerimisteenuselt saadud vastuseid.

#### <a name="request-handler"></a>Nõudeohjur

**EFRHandler-i** taotluseohjur on sisenemispunkt fiskaalregistreerimise teenuse taotluste käsitlemiseks. See ohjur on päritud **INamedRequestHandler** liideselt. Meetod **HandlerName** vastutab ohjuri nime tagastamise eest. Ohjuri nimi peab ühtima Commerce Headquartersis määratud fiskaalühenduse nimega.

Konnektor toetab järgmisi taotlusi:

- **SubmitDocumentFiscalDeviceRequest – see taotlus saadab dokumendid fiskaalregistreerimise teenusesse ja** tagastab sellelt vastuse.
- **IsReadyFiscalDeviceRequest – seda taotlust kasutatakse** fiskaalregistreerimise teenuse seisundikontrolliks
- **InitializeFiscalDeviceRequest** – seda taotlust kasutatakse fiskaalregistreerimise teenuse lähtestamiseks

#### <a name="configuration"></a>Konfiguratsioon

Fiskaalkonnektori konfiguratsioonifail asub lahenduste **hoidlas src \\ FiscalIntegration \\ Efr \\\\ Configurations Connectors \\ ConnectorEFRSample.xml.**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Faili eesmärk on lubada finantsühenduse sätete konfigureerimist rakendusest Commerce headquarters. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetele.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
