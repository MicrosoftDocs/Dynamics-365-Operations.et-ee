---
title: Fiskaalüksuse registreerimisteenuse integratsiooni näide Saksamaa jaoks
description: Selles teemas antakse ülevaade Fiskaalintegratsiooni näidistest Saksamaa jaoks Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2020-5-29
ms.openlocfilehash: 65315a9fd6bc1af26bc225220e096aee4da09be2
ms.sourcegitcommit: b80692c3521dad346c9cbec8ceeb9612e4e07d64
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 03/05/2022
ms.locfileid: "8388155"
---
# <a name="fiscal-registration-service-integration-sample-for-germany"></a>Fiskaalüksuse registreerimisteenuse integratsiooni näide Saksamaa jaoks

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

Selles teemas antakse ülevaade Fiskaalintegratsiooni näidistest Saksamaa jaoks Microsoft Dynamics 365 Commerce.

Saksamaa kassaraamatute kohalike fiskaalnõuete täitmiseks hõlmab Saksamaa funktsioon kassa (POS) näidisintegratsiooni välise fiskaalregistreerimise Microsoft Dynamics 365 Commerce teenusega. Näidis laiendab fiskaalintegratsiooni [funktsioone](fiscal-integration-for-retail-channel.md). See põhineb [EFSTA](https://www.efsta.eu/de/fiskalloesungen/deutschland) EFR-i (elektroonilise finantsregistri) [lahendusel](https://www.efsta.eu/de/) ja võimaldab HTTPS-protokolli kaudu sidet EFR-teenusega. EFR-teenus peab olema majutatud kas jaemüügi riistvarajaamas või eraldi arvutis, mida saab ühendada riistvarajaamaga. Näidis esitatakse lähtekoodina ja on osa jaemüügi tarkvara arenduskomplektist (SDK).

Microsoft ei vabasta EFSTA-st riistvara, tarkvara ega dokumentatsiooni. Lisateabeks selle kohta, kuidas saada EFR-lahendust ja seda kasutada, võtke ühendust [EFSTA-ga](https://www.efsta.eu/de/kontakt/kontakt).

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

- **Klienditellimuste registreerimine fiskaalregistreerimise teenuses on** sama, mis sularaha ja edasimüügi müügi ja tagastuste protsess.
- **Operatsioonide registreerimine, mis hõlmab kinkekaarte ja deposiite.** Registreerimisprotsess on sama, mis sularaha ja kandke müügi ja tagastuste protsess.

#### <a name="notifying-users-about-fiscal-registration-failures"></a>Kasutajate teatamine fiskaalregistreerimise tõrgetest

Fiskaalregistreerimisteenus saab kasutajaid fiskaalregistreerimise ajal ilmnenud tõrgetest teavitada kahel viisil:

- Prindib vastusest lisateavet kviitungite **teabeväljale**.
- Kuvage fiskaalteenuse teatised kassas kasutajateadetena.

    > [!NOTE]
    > Selle teavitusmehhanismi puhul peab fiskaalregistreerimise **teatiste** parameetri kuvamine **lehel Konnektori tehnilised profiilid** olema sisse lülitatud.

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
> Kviitungitele saab printida ka QR-koodi. Kuigi QR-kood on valikuline, on see väga soovitatav. Lisateavet selle kohta, kuidas saada QR-koodi fiskaalregistreerimise teenuse vastuse osana, vt EFSTA\[ dokumentatsiooni veebisaidil avaldatud dokumenti "EFR Guide \] DE ["](https://public.efsta.net/efr/).
>
> Sissetulekute **teabeteate** väli näitab fiskaalregistreerimise teenuse teatist. Näiteks allkirjaseadme katkemisel saab kviitungil printida eriteksti.

#### <a name="voided-suspended-and-recalled-transactions"></a>Tühistatud, peatatud ja tühistatud kanded

- Tühistatud kanne registreeritakse taotlusena fiskaalregistreerimise teenuses kande lõpetamiseks.
- Peatatud kanne on registreeritud taotlusena lõpetada kanne fiskaalregistreerimise teenuses.
- Peatatud kande tagasikutsumine registreeritakse uue kande alguses fiskaalregistreerimise teenuses.

### <a name="non-sales-transactions-and-shift-closing"></a>Mittemüügikanded ja vahetuse sulgemine

Järgmised mittemüügikanded registreeritakse fiskaaltoimingutena fiskaalregistreerimise **teenuses NFS-sildi** abil:

- Deklareeri algsumma
- Sularaha sissemakse
- Väljamakse
- Seifi viidav raha
- Raha hoiustamine panka
- Tulukontod
- Kulukontod

**Vahetuse sulgemise** toiming on registreeritud ka mittefiskaalse toiminguna fiskaalregistreerimise teenuses, kasutades **NFS-silti**.

### <a name="data-export-and-audit"></a>Andmete eksport ja audit

Kõik kanded peab OLEMA TSE allkirjastatud, et tagada nende terviklikkus, autentsus ja terviklikkus ning ennetada kirjendatud andmete manipulatsioone.

> [!WARNING]
> Kasutada saab ainult sertifitseeritud TSE-d. Teavet EFR-i lahenduses toetatud TSE-de tüüpide ja mudelite kohta vt EFSTA\[ dokumentatsiooni veebisaidil avaldatud dokumendist "EFR Guide \] DE [...](https://public.efsta.net/efr/)". Lisateabe saamiseks TSE valiku ja hankimise kohta võtke ühendust EFSTA-ga [...](https://www.efsta.eu/at/kontakt).

Saksamaa määrustega nõutakse eksporti DSFinV-K tuge. DSFinV-K ekspordi saab käivitada EFR-i lahenduses. Lisateavet DSFinV-K ekspordi kohta vt EFSTA\[ dokumentatsiooni veebisaidil avaldatud dokumendist "EFR Guide \] DE [...](https://public.efsta.net/efr/)".

### <a name="limitations-of-the-sample"></a>Näidiste piirangud

Fiskaalregistreerimisteenus toetab ainult stsenaariume, kus hindades sisaldub käibemaks. Seetõttu peab nii **kaupluste kui ka** klientide puhul valiku Hinnad **sisaldavad** käibemaksu väärtuseks olema seatud Jah.

Fiskaalteenus ei toeta olukordi, kus samale kandereale rakendatakse rohkem kui ühte käibemaksukoodi.

Fiskaalintegratsiooni raamistik ei toeta müügipakkumist. Seetõttu ei ole neid toiminguid fiskaalteenuses registreeritud.

## <a name="set-up-commerce-for-germany"></a>Häälestage Saksamaa äri

See jaotis kirjeldab Ärisätteid, mis on Saksamaale spetsiifilised ja soovitatavad. Lisateavet häälestuse kohta vt [Commerce'i kodulehelt](../index.md).

Saksamaale omase funktsiooni kasutamiseks peate määrama järgmised sätted.

- Määrake juriidilise isiku esmasel aadressil väli Riik/**regioon** **DEU-ks** (Saksamaa).
- Seadke iga Saksamaal asuv kaupluse kassa funktsiooniprofiilis **ISO-koodi väli** väärtusele **DE** (Saksamaa).

Peate määrama ka Saksamaa jaoks järgmised sätted. Käitage vastavad jaotustööd kindlasti pärast seadistuse lõpule viimist.

### <a name="set-up-vat-per-german-requirements"></a>KM-i seadistamine Saksa nõuete kohta

Peate looma käibemaksukoodid, käibemaksugrupid ja kauba käibemaksugrupid. Samuti peate häälestama toodete ja teenuste käibemaksuteabe. Lisateavet käibemaksu funktsioonide seadistamis- ja kasutus kohta leiate käibemaksu [ülevaatest](../../finance/general-ledger/indirect-taxes-overview.md).

Müügikviitungitele saate printida käibemaksukoodi lühendi (nt "A" või "B"). Selle funktsiooni kasutamiseks seadistage käibemaksukoodide **lehel** välja printimiseks **kood**.

### <a name="set-up-stores"></a>Kaupluste häälestamine

Lehel Kõik **kauplused** värskendage kaupluse üksikasju. Konkreetselt määrake järgmised parameetrid:

- **Määrake väljal Käibemaksugrupp** käibemaksugrupp, mida tuleks kasutada vaikekliendile müügi puhul.
- Seadke valiku **Hinnad sisaldavad käibemaksu väärtuseks** **Jah**.
- Seadke välja **Nimi** väärtuseks ettevõtte nimi. See muudatus aitab tagada, et ettevõtte nimi ilmub müügikviitungil. Teise võimalusena saate ettevõtte nime lisada müügikviitungi kavandile vabas vormis tekstina.
- Seadistage **maksu ID-koodi (TIN)** väli ettevõtte ID-koodile. See muudatus aitab tagada, et ettevõtte ID-kood ilmub müügikviitungil. Teise võimalusena saate vabas vormis tekstina lisada müügikviitungi kavandile ettevõtte ID-koodi.

### <a name="set-up-functionality-profiles"></a>Funktsiooniprofiilide seadistamine

Kassa funktsiooniprofiilide seadistamine. Kiirkaardil **Kviitungi** nummerdamine seadistage kviitungite **nummerdamine**, luues või värskendades kirjeid kandetüüpide Müük, **Müügitellimus** ja Tagastatud **sissetulek** jaoks.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Kohandatud väljade konfigureerimine, et neid saaks kasutada müügikviitungite kviitungi vormingutes

Saate konfigureerida keele teksti ja kohandatud väljad, mida kassa kviitungi vormingutes kasutatakse. Kviitungi häälestuse loonud kasutaja vaikeettevõte peaks olema sama juriidiline isik, kus keele teksti häälestus on loodud. Teise võimalusena tuleks samad keeletekstid luua nii kasutaja vaikeettevõttes kui ka kaupluse juriidilises isikus, mille jaoks häälestus on loodud.

Lisage keele **teksti lehel** kviitungi kavandite kohandatud väljade siltidele järgmised kirjed. Pange tähele **, et tabelis kuvatavad** keele **-,** **teksti-ID**- ja tekstiväärtused on vaid näited. Saate neid vastavalt oma nõuetele muuta. Teksi **ID väärtused** peavad siiski olema kordumatud ning võrduma või olema rohkem kui 900001.

Lisage keele tekstilehe müügikoha **jaotisse** järgmised **müügikoha sildid**.

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

**Lisage kviitungi** kavandite kohandatud väljade jaoks kohandatud väljadele järgmised kirjed lehel Kohandatud väljad. Pange tähele, **et pealdise teksti ID** väärtused peavad vastama teksti **ID** väärtustele, mille määrate keele **teksti** lehel.

| Nimi                            | Tüüp    | Pealdise teksti ID |
|---------------------------------|---------|-----------------|
| QRCODEDE\_                      | Sissetulek | 900001          |
| TRANSACTIONIDDE\_               | Sissetulek | 900002          |
| RETAILPRINTCODEDE\_             | Sissetulek | 900003          |
| SALESTAMOUNTDE\_              | Sissetulek | 900004          |
| SALESTAXBASISDE\_               | Sissetulek | 900005          |
| KANDEDTARTDATETIMEDE\_    | Sissetulek | 900006          |
| KANDEENDDATETIMEDE\_      | Sissetulek | 900007          |
| VÄLI SECURITYELEMENTSERIALNUMBERDE\_ | Sissetulek | 900008          |
| SIGNCOUNTERDE\_                 | Sissetulek | 900009          |
| ALLKIRJASTA\_                        | Sissetulek | 900010          |
| INFOMESSAGEDE\_                 | Sissetulek | 900011          |

> [!NOTE]
> On oluline määrata õiged kohandatud väljanimed, nagu on loetletud eelmises tabelis. Vale kohandatud välja nimi põhjustab sissetulekutes puuduvate andmete.

### <a name="configure-receipt-formats"></a>Kviitungi vormingute konfigureerimine

Muutke iga nõutava kviitungi vormingu välja Prindikäitumine **väärtuseks** Alati **prindi**.

Lisage kviitungi vormingu kujundajasse järgmised kohandatud väljad asjakohastele kviitungi jaotistele. Pange tähele, et väljanimed vastavad eelmises jaotises määratletud keeletekstidele.

- **Päis:** lisage järgmised väljad:

    - **Kaupluse nime** ja **maksu ID-koodi** väljad, mida kasutatakse ettevõtte nime ja ID-koodi printimiseks kviitungitele. Soovi korral saate kavandile lisada ka ettevõtte nime ja ID-koodi vabas vormis tekstina.
    - **Kaupluse aadressi**, kuupäeva **,** kellaaja **24 h**, **kviitungi numbri ja** registri **numbriväljad**.

- **Read:** lisage järgmised väljad:

    - **Kauba nime** väli
    - **Koguse** väli
    - **Hind kokku maksuväljaga**
    - **Maksu jaemüügi prindikoodi** väli, mida kasutatakse kaubale kehtivale käibemaksukoodile vastava lühendatud koodi printimiseks

- **Jalus:** lisage järgmised väljad:

    - Makseväljad, nii et prinditakse iga makseviisi maksesummad. Lisage näiteks maksevahendi **nimi ja** maksevahendi **summa** väljad kavandi ühele reale.
    - Maksuväljade **väljagrupi väljad**. Kõik selle väljagrupi väljad tuleb printida ühele eraldi reale.

        - **Maksu ID** väli, mis on standardne väli, mis võimaldab printida käibemaksu kokkuvõtte iga käibemaksukoodi kohta. See väli tuleb lisada uuele reale.
        - **Maksuprotsendi** väli, mis on standardväli, mida kasutatakse käibemaksukoodi efektiivse maksumäära printimiseks.
        - **Välja Maksu alus** (müük), mida kasutatakse sissetuleku sularahamüügi kogusumma printimiseks käibemaksukoodi kohta. Ettemaksed ja kinkekaarditoimingud on välja jäetud.
        - **Maksusumma (müük),** mida kasutatakse selle käibemaksukoodi puhul sularahamüügi sissetuleku maksusumma printimiseks.
        - **Maksu jaemüügi prindikoodi** väli, mida kasutatakse käibemaksukoodile vastava lühendatud koodi printimiseks.

    - Väljad, mis sisaldavad fiskaalregistreerimise teenuse tagastatud turvatud kandeandmeid:

        - **Kande ID** väli, mis tuvastab kassakande numbri fiskaalregistreerimise teenuses
        - **Kande alguskuupäeva kellaaja** väli
        - **Kande lõppkuupäeva kellaaja** väli
        - **Turvaelemendi välja seerianumber**
        - **Allkirjaloenduri** väli
        - **Kontrolli väärtuse** välja
        - **QR-koodi** väli, mida kasutatakse viite printimiseks registreeritud sularahakandele QR-koodina

        > [!NOTE]
        > **QR-koodi** väärtus tuuakse fiskaalregistri vastusest. EFR tagastab oma vastuses QR-koodi **ainult siis, kui EFR-i konfiguratsiooni atribuutide** välja väärtust on kirjeldatud EFSTA dokumentatsioonis. EFR-i konfiguratsiooni atribuutide **väljal** tuleb QR-koodi vorming seada **BMP-le**.

    - **Teabeteate** väli, nii et fiskaalregistreerimisteenuse teavitusteateid saab kuvada kviitungitel. Näiteks allkirjaseadme katkemisel saab kviitungil printida eriteksti.

Lisateavet kviitungi vormingutega töötades vt Kviitungi vormingute [häälestamine ja kujundamine](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-germany"></a>Saate häälestada Saksamaa fiskaalintegratsiooni.

Saksamaa fiskaalregistreerimisteenuse integreerimise näidis põhineb fiskaalintegratsiooni [funktsioonil](fiscal-integration-for-retail-channel.md) ja on osa Retail SDK-st. Näidis asub lahenduste **hoidla kaustas srcFiscalIntegrationEfr\\\\**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/)([nt näidis väljalaskes/9.33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr) Näidis koosneb [fiskaaldokumendi](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) pakkujast, mis on Commerce Runtime'i (CRT) laiendus, ja fiskaalühendusest, mis on Commerce Hardware Stationi laiendus. Lisateavet Retail SDK [kasutamise kohta vt Retail SDK arhitektuurist ja sõltumatult pakendatud SDK-st](../dev-itpro/retail-sdk/retail-sdk-overview.md)[koostevõimaluste häälestamise kohta](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Uue sõltumatu pakendi- ja [laiendusmudeli piirangute tõttu](../dev-itpro/build-pipeline.md) ei saa seda praegu selle fiskaalintegratsiooni näidise jaoks kasutada. Retail SDK eelmist versiooni peate kasutama arendaja virtuaalmasinas (VM) elutsükli Microsoft Dynamics teenustes (LCS). Lisateavet vt Saksamaa fiskaalintegratsiooni [näidise juurutuse juhistest (pärand).](emea-deu-fi-sample-sdk.md)
>
> Uutesse versioonidesse planeeritakse fiskaalintegratsiooni valimite uue sõltumatu pakendi- ja laiendusmudeli tugi.

Viige finantsintegratsiooni seadistuse etapid lõpule, nagu on kirjeldatud [ärikanalite fiskaalintegratsiooni seadistamises](setting-up-fiscal-integration-for-retail-channel.md):

1. [Seadistage fiskaalregistreerimise protsess](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Lisaks tehke märkus fiskaalregistreerimise protsessi sätete kohta, mis on omased [sellele fiskaalregistreerimise teenuse integratsiooni näidisele](#set-up-the-registration-process).
1. [Tõrke käsitlemise sätete seadistamine](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

    > [!WARNING]
    > Fiskaalintegratsiooni raamistiku tõrke käsitlemise võimalused ei pruugi olla täielikult joondatud kohalike finantseeskirjadega.
    >
    > - Soovitame **jätta** **suvand** Jätka tõrke korral fiskaalregistreerimise protsessi lehel välja lülitatud, sest kõik kanded peavad olema korrektselt registreeritud, isegi kui fiskaalregistreerimise esimene katse ei õnnestunud.
    > - Enne kui lülitate fiskaalregistreerimise protsessi lehel sisse suvandi Skip või **Mark** **registreeritud, peaksite käsitlema neid fiskaalregistreerimise protsessi muudatusi oma maksunõustaja või kohaliku maksuametiga.** **·**

1. [Saate lubada edasilükatud fiskaalregistreerimise käsitsi käivitamise](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Kanali komponentide konfigureerimine](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Registreerimisprotsessi häälestamine

Registreerimisprotsessi lubamiseks järgige neid samme Commerce headquartersi häälestamiseks. Lisateavet vt Commerce'i [kanalite fiskaalintegratsiooni häälestamist](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process).

1. Laadige alla finantsdokumendi pakkuja ja fiskaalkonnektori konfiguratsioonifailid:

    1. [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Lahenduste hoidla avamine.
    1. Valige õige väljalaske haruversioon vastavalt oma SDK-le/rakenduse versioonile (nt **[vabastamine/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Avatud **src \> FiscalIntegration \> Efr**.
    1. Laadige alla finantsdokumendi **pakkuja konfiguratsioonifail konfiguratsioonifailis Configurations \> DocumentProviders \> DocumentProviderFiscalEFRSampleGermany.xml** ([nt väljalaske fail/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders/DocumentProviderFiscalEFRSampleGermany.xml)).
    1. Laadige alla fiskaalkonnektori **konfiguratsioonifail Configurations \> Connectors \> ConnectorEFRSample.xml** ([nt väljalaskefail/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)).

    > [!WARNING]
    > Uue sõltumatu pakendi- ja [laiendusmudeli piirangute tõttu](../dev-itpro/build-pipeline.md) ei saa seda praegu selle fiskaalintegratsiooni näidise jaoks kasutada. Retail SDK eelmist versiooni peate kasutama LCS-i arendaja VM-s. Selle fiskaalintegratsiooni näidiskonfiguratsiooni failid asuvad Retail SDK arendaja VM LCS-i kaustades:
    >
    > - **Fiskaaldokumendi pakkuja konfiguratsioonifail:** RetailSdkSampleExtensionsCommerceRuntimeExtensions.DocumentProvider.EFRSampleConfigurationDocumentProviderFiscalEFRSampleGermany.xml\\\\\\\\\\
    > - **Fiskaalkonnektori konfiguratsioonifail:** RetailSdkSampleExtensionsHardwareStationExtension.EFRSampleConfigurationConnectorEFRSample.xml\\\\\\\\\\
    > 
    > Uutesse versioonidesse planeeritakse fiskaalintegratsiooni valimite uue sõltumatu pakendi- ja laiendusmudeli tugi.

1. Valige suvandid **Jaemüük ja kaubandus \> Headquartersi häälestus \> Parameetrid \> Commerce’i ühiskasutuses parameetrid**. Seadke vahekaardil **Üldine** suvand Luba fiskaalintegratsioon **väärtusele** **Jah**.
1. Minge jaemüügi ja **ärikanali häälestuse \> fiskaalintegratsiooni \>\> finantsdokumendi pakkujate** juurde ja laadige varem alla laaditud finantsdokumendi pakkuja konfiguratsioonifail.
1. Minge jaemüügi- **ja ärikanali häälestuse \> fiskaalintegratsiooni \>\> fiskaalkonnektori ja laadige varem alla laaditud fiskaalkonnektori** konfiguratsioonifail.
1. Minge jaemüügi ja **ärikanali häälestuse \> fiscal \> integration Connectori funktsiooniprofiilidesse \>**. Looge uus konnektori funktsiooniprofiil. Valige dokumendipakkuja ja ühendus, mille varem laadisite. Värskendage andmevastendussätted [vastavalt](#default-data-mapping) vajadusele.
1. Minge jaemüügi ja **ärikanali häälestuse \> finantsintegratsiooni \> konnektori \> tehnilistesse profiilidesse**. Looge uus konnektori tehniline profiil ja valige varem laaditud fiskaalühendus. Uuendage konnektori [sätteid](#fiscal-connector-settings) vastavalt vajadusele.
1. Minge jaemüügi ja **ärikanali häälestuse \> fiskaalintegratsiooni \> fiskaalühenduse \> gruppidesse**. Looge varem loodud konnektori funktsiooniprofiilile uus fiskaalühenduse grupp.
1. Minge jaemüügi ja **ärikanali häälestuse \> fiskaalintegratsiooni \> fiskaalregistreerimisprotsessidesse \>**. Looge uus fiskaalregistreerimise protsess ja fiskaalregistreerimise protsessi samm ning valige varem loodud fiskaalühenduse grupp.
1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassaprofiilid \> Funktsiooniprofiilid**. Valige funktsiooniprofiil, mis on lingitud kauplusega, kus registreerimisprotsess tuleks aktiveerida. Valige finants **registreerimisprotsessi kiirkaardil** varem loodud fiskaalregistreerimise protsess.
1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassaprofiilid \> Riistvaraprofiilid**. Valige riistvaraprofiil, mis on lingitud riistvarajaamaga, millega fiskaalprinter on ühendatud. Valige kiirkaardil **Fiscal peripherals** varem loodud konnektori tehniline profiil.
1. Avage jaotusgraafik (**Retail ja Commerce Retail ja Commerce \> IT \> Distribution schedule**) **ning valige tööd 1070** **ja 1090** andmete edastamiseks kanali andmebaasi.

#### <a name="default-data-mapping"></a>Vaikeandmete vastendamine

Järgmine vaikeandmete vastendamine on kaasatud fiskaaldokumendi pakkuja konfiguratsiooni, mis antakse fiskaalintegratsiooni näidisosana:

- **Maksevahendi tüübi** vastendamine: **makseviiside vastendamine atribuudi PayG** (maksegrupp) väärtustega fiskaalteenusesse saadetud taotlustes. Siin on vaikevastendus:

    ```
    1: 0; 2: 1; 3: 3; 4: 8; 5: 2; 6: 0; 7: 7; 8: 6; 9: 0; 10: 8; 11: 1
    ```

    Iga paari esimene komponent esindab kauplusele seadistatud makseviisi. Teine komponent tähistab vastavat maksegruppi, mida toetab EFR-i fiskaalregistreerimisteenus. Lisateavet maksegruppide kohta, mida EFR Saksamaale toetab, vt EFR-i [viidet](https://public.efsta.net/efr/).

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

- **Kaasa kliendiandmed** – kui see parameeter on sisse lülitatud, sisaldavad rahandusteenuse taotlused klienditeavet, nt nimesid ja aadresse, juhul kui klient lisatakse kandesse.
- **Käibemaksumäärade vastendamine** : **käibemaksukoodide jaoks seadistatud maksu protsendiväärtuste vastendamine fiskaalteenusele saadetud taotlustes atribuudi TaxG** (maksugrupp) väärtustega. Siin on vaikevastendus:

    ```
    A: 19.00; B: 7.00; C: 10.70; D: 5.50; E: 0.00
    ```

    Iga paari esimene komponent esindab käibemaksugruppi, mida toetab EFR-i fiskaalregistreerimisteenus. Teine komponent esindab vastavat KM-määra. Lisateavet käibemaksugruppide kohta, mida EFR Saksamaale toetab, vt EFR-i [viidet](https://public.efsta.net/efr/).

- **Maksugrupp kinkekaartide ja deposiitide** jaoks – **TaxG** atribuudi väärtus fiskaalteenusele saadetud taotlustes, mis põhinevad kinkekaarte või deposiite kaasatud toimingutel. Siin on vaikevastendus:

    ```
    G
    ```

- **Käibemaksuvabastuse maksugrupp** – **atribuudi TaxG** väärtus fiskaalteenusele saadetud taotlustes, mis põhinevad maksukohustustest vabastatud toimingutel. Siin on vaikevastendus:

    ```
    F
    ```

> [!NOTE]
> Vaikeandmete vastenduse maksusätted vastutavad vastavate maksusätete eest süsteemis ja maksugruppide eest EFR-teenuses. Maksugruppe saab kviitungitele printida ainult **siis, kui prinditav** kood on seadistatud **käibemaksukoodide lehele**.

#### <a name="fiscal-connector-settings"></a>Fiskaalühenduse sätted

Järgmised sätted on kaasatud fiskaalkonnektori konfiguratsiooni, mis on antud fiskaalintegratsiooni näidisosana:

- **Lõpp-punkti** aadress – fiskaalregistreerimise teenuse URL.
- **Ajalõpp** – aja hulk millisekundites, mida fiskaalkonnektor fiskaalregistreerimise teenuse vastuse ootab.
- **Kuva fiskaalregistreerimise** teatised – see lipp kontrollib, kas fiskaalregistreerimise teenuse tagastused tuleb operaatorile kuvada.

### <a name="configure-channel-components"></a>Kanali komponentide konfigureerimine

> [!WARNING]
> Uue sõltumatu pakendi- ja [laiendusmudeli piirangute tõttu](../dev-itpro/build-pipeline.md) ei saa seda praegu selle fiskaalintegratsiooni näidise jaoks kasutada. Retail SDK eelmist versiooni peate kasutama LCS-i arendaja VM-s. Lisateavet vt Saksamaa fiskaalintegratsiooni [näidise juurutuse juhistest (pärand).](emea-deu-fi-sample-sdk.md)
>
> Uutesse versioonidesse planeeritakse fiskaalintegratsiooni valimite uue sõltumatu pakendi- ja laiendusmudeli tugi.

#### <a name="set-up-the-development-environment"></a>Saate häälestada arenduskeskkonda.

Arenduskeskkonna katsetada ja näidist laiendada, järgige neid samme.

1. Rakenduste hoidla leidmine [Dynamics 365 Commerce või](https://github.com/microsoft/Dynamics365Commerce.Solutions) allalaadimine. Valige õige väljalaske haruversioon vastavalt oma SDK-le/rakenduse versioonile. Lisateavet vt jaotisest Jaemüügi [SDK näidised ja viitepakendid alla laadida GitHub-st ja NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Avage EFR-i lahendus rakenduses **Dynamics365Commerce.SolutionsFiscalIntegrationEfrEFR.sln\\\\\\** ja koostage see.
1. Commerce'i käitusaja laienduste installimine:

    1. Leidke laiendi CRT installer:

        - **Commerce Scale Unit:** leidke kaustast EfrScaleUnitScaleUnit.EFR.InstallerbinDebugnet461 **\\\\\\\\\\** installer ScaleUnit.EFR.Installer.**·**
        - **Kohalik CRT modern POS-is:** **leidke kaustast EfrModernPOSModernPOS.EFR.InstallerbinDebugnet461\\\\\\\\\\** **ModernPOS.EFR.Installer.**

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

        1. Leidke kaustast **EfrHardwareStationHardwareStation.EFR.InstallerbinDebugnet461\\\\\\\\\\** **riistvarajaam.EFR.Installeri installer.**
        1. Käivitage laiendinstall käsurealt, käivitades järgmise käsu.

            ```Console
            HardwareStation.EFR.Installer.exe install --verbosity 0
            ```

    1. Installige müügikoha laiendused:

        1. Avage kassa fiskaalkonnektori **näidislahendus Dynamics365Commerce.SolutionsFiscalIntegrationPosFiscalConnectorSampleContpuhvri.PosFiscalConnectorSample.sln\\\\\\** ja koostage see.
        1. Leidke kaustast **PosFiscalConnectorSampleStoreCommerce.InstallerbinDebugnet461\\\\\\\\** **contoso.PosFiscalConnectorSample.StoreCommerce.Installer.**
        1. Käivitage laiendinstall käsurealt, käivitades järgmise käsu.

            ```Console
            Contoso.PosFiscalConnectorSample.StoreCommerce.Installer.exe install --verbosity 0
            ```

#### <a name="production-environment"></a>Tootmiskeskkond

Järgige fiskaalintegratsiooni [näidise](fiscal-integration-sample-build-pipeline.md) jaoks koostevõimaluste häälestamise etappe, et luua ja vabastada pilveskaala üksus ja iseteeninduse juurutatavad paketid fiskaalintegratsiooni näidiskomplekti jaoks. **EFR-i build-pipeline.yml** malli JAML **\\ faili leiate lahenduste YAML_Files**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions) kaustast Müügivõimalustest.

## <a name="design-of-extensions"></a>Laienduste kujundus

Saksamaa fiskaalregistreerimisteenuse integreerimise näidis põhineb fiskaalintegratsiooni [funktsioonil](fiscal-integration-for-retail-channel.md) ja on osa Retail SDK-st. Näidis asub lahenduste **hoidla kaustas srcFiscalIntegrationEfr\\\\**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/)([nt näidis väljalaskes/9.33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr) Näidis koosneb [fiskaaldokumendi](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) pakkujast, mis on CRT laiendiks, ja fiskaalühendusest, mis on Commerce Hardware Stationi laiendus. Lisateavet Retail SDK [kasutamise kohta vt Retail SDK arhitektuurist ja sõltumatult pakendatud SDK-st](../dev-itpro/retail-sdk/retail-sdk-overview.md)[koostevõimaluste häälestamise kohta](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Uue sõltumatu pakendi- ja [laiendusmudeli piirangute tõttu](../dev-itpro/build-pipeline.md) ei saa seda praegu selle fiskaalintegratsiooni näidise jaoks kasutada. Retail SDK eelmist versiooni peate kasutama LCS-i arendaja VM-s. Lisateavet vt Saksamaa fiskaalintegratsiooni [näidise juurutuse juhistest (pärand).](emea-deu-fi-sample-sdk.md) Uutesse versioonidesse planeeritakse fiskaalintegratsiooni valimite uue sõltumatu pakendi- ja laiendusmudeli tugi.

### <a name="crt-extension-design"></a>CRT laiendi kujundus

Fiskaaldokumendi pakkuja laiendi eesmärk on luua teenusepõhiseid dokumente ja käsitleda fiskaalregistreerimise teenuse vastuseid.

#### <a name="request-handler"></a>Nõudeohjur

Dokumendipakkujal DocumentProviderEFRFiscalDEU **on üks taotluseohjur**. Seda ohjurit kasutatakse fiskaaldokumentide loomiseks fiskaalregistreerimise teenusele. See pärineb INamedRequestHandler **liideselt**. Meetod **HandlerName** vastutab ohjuri nime tagastamise eest. Ohjuri nimi peab vastama Commerce Headquartersis määratud konnektori dokumendi pakkuja nimele.

Konnektor toetab järgmisi taotlusi:

- **GetFiscalDocumentDocumentProviderRequest** – see taotlus sisaldab teavet selle kohta, milline dokument tuleks luua. See tagastab teenusepõhise dokumendi, mis tuleb registreerida fiskaalregistreerimise teenuses.
- **GetFiscalTransactionExtendedDataDocumentProviderRequest** – see taotlus tagastab vastuse koos laiendatud andmetega.

#### <a name="configuration"></a>Konfiguratsioon

Fiskaaldokumendi **pakkuja konfiguratsioonifail asub lahenduste hoidlas srcFiscalIntegrationEfrConfigpftionsDocumentProvidersDocumentProviderFiscalEFRSampleGermany.xml\\\\\\\\\\**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Faili eesmärk on lubada finantsdokumendi pakkuja sätete konfigureerimist rakendusest Commerce headquarters. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetele.

### <a name="hardware-station-extension-design"></a>Riistvarajaama laienduse kujundus

Fiskaalühenduseks olemise laiendi eesmärgiks on fiskaalregistreerimise teenusega suhtlemine.

Riistvarajaama laiend onHardwareStation.Extension.EFRSample **·**. See kasutab HTTP-protokolli, et esitada dokumente, mida CRT laiend finantsregistreerimise teenusele loob. Samuti käsitletakse fiskaalregistreerimisteenuselt saadud vastuseid.

#### <a name="request-handler"></a>Nõudeohjur

EFRHandler-i **taotluseohjur** on sisenemispunkt fiskaalregistreerimise teenuse taotluste käsitlemiseks. See ohjur on päritud **INamedRequestHandler liideselt**. Meetod **HandlerName** vastutab ohjuri nime tagastamise eest. Ohjuri nimi peab ühtima Commerce Headquartersis määratud fiskaalühenduse nimega.

Konnektor toetab järgmisi taotlusi:

- **SubmitDocumentFiscalDeviceRequest** – see taotlus saadab dokumendid fiskaalregistreerimise teenusesse ja tagastab sellelt vastuse.
- **IsReadyFiscalDeviceRequest** – seda taotlust kasutatakse fiskaalregistreerimise teenuse seisundikontrolliks
- **InitializeFiscalDeviceRequest** – seda taotlust kasutatakse fiskaalregistreerimise teenuse lähtestamiseks

#### <a name="configuration"></a>Konfiguratsioon

Fiskaalkonnektori **konfiguratsioonifail asub lahenduste\\ hoidlas srcFiscalIntegrationEfrConfigtionsConnectorsConnectorEFRSample.xml\\\\\\\\**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Faili eesmärk on lubada finantsühenduse sätete konfigureerimist rakendusest Commerce headquarters. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetele.

### <a name="pos-fiscal-connector-extension-design"></a>Müügikoha fiskaalkonnektori laienduse kujundus

Kassa fiskaalühenduse laienduse eesmärk on kassast fiskaalregistreerimise teenusega sideühendus. See kasutab side jaoks HTTPS-protokolli.

#### <a name="fiscal-connector-factory"></a>Fiskaalühenduse tehas

Fiskaalühenduse tehas vastendab konnektori nime fiskaalühenduse **rakendusega ja asub failis Pos.ExtensionConnectorsFiscalConnectorFactory.ts\\\\**. Konnektori nimi peab kattuma Commerce Headquartersis määratud fiskaalühenduse nimega.

#### <a name="efr-fiscal-connector"></a>EFR-i fiskaalühendus

EFR-i fiskaalühendus asub **failis Pos.ExtensionConnectorsEfrEfrFiscalConnector.ts\\\\\\**. See juurutab **IFiscalConnectori** liidest, mis toetab järgmisi taotlusi:

- **FiscalRegisterSubmitDocumentClientRequest** – see taotlus saadab dokumendid fiskaalregistreerimise teenusesse ja tagastab sellelt vastuse.
- **FiscalRegisterIsReadyClientRequest** – seda taotlust kasutatakse fiskaalregistreerimise teenuse seisundikontrolliks.
- **FiscalRegisterInitializeClientRequest** – seda taotlust kasutatakse fiskaalregistreerimise teenuse lähtestamiseks.

#### <a name="configuration"></a>Konfiguratsioon

Konfiguratsioonifail asub lahenduste **hoidla kaustas srcFiscalIntegrationEfrConfigtionsConnectors\\\\\\\\**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Faili eesmärk on lubada finantsühenduse sätete konfigureerimist rakendusest Commerce headquarters. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetele. Lisatakse järgmised sätted:

- **Lõpp-punkti** aadress – fiskaalregistreerimise teenuse URL.
- **Ajalõpp** – aeg millisekundites, mille konnektor ootab fiskaalregistreerimise teenuselt vastust.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
