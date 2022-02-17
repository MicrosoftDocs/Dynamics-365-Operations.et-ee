---
title: Fiskaalüksuse registreerimisteenuse integratsiooni näide Saksamaa jaoks
description: Selles teemas antakse ülevaade Saksamaa eelarveintegratsiooni proovist Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2020-5-29
ms.openlocfilehash: 128c94407a283bf45e5626de060cee82430f087b
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2022
ms.locfileid: "8076858"
---
# <a name="fiscal-registration-service-integration-sample-for-germany"></a>Fiskaalüksuse registreerimisteenuse integratsiooni näide Saksamaa jaoks

[!include[banner](../includes/banner.md)]

Selles teemas antakse ülevaade Saksamaa eelarveintegratsiooni proovist Microsoft Dynamics 365 Commerce.

Saksamaa Microsoft Dynamics 365 Commerce kassaaparaatide kohalike maksunõuete täitmiseks hõlmab Saksamaa funktsionaalsus müügikoha näidisi integreerimist välise maksuregistreerimisteenusega. Valim laiendab fiskaalintegratsiooni [funktsiooni](fiscal-integration-for-retail-channel.md). See põhineb EFSTA [EFR (Electronic Fiscal Register)](https://www.efsta.eu/de/fiskalloesungen/deutschland) lahendusel [ja](https://www.efsta.eu/de/) võimaldab EFR-teenusega suhelda HTTPS-protokolli kaudu. EFR-teenust tuleks majutada kas jaemüügi riistvarajaamas või eraldi arvutis, millega saab riistvarajaamast ühendada. Proov on esitatud lähtekoodi kujul ja see on osa jaemüügi tarkvaraarenduskomplektist (SDK).

Microsoft ei väljasta EFSTA-st riist-, tarkvara ega dokumente. EFR-lahenduse saamiseks ja selle käitamiseks võtke ühendust EFSTA-ga [...](https://www.efsta.eu/de/kontakt/kontakt).

## <a name="scenarios"></a>Stsenaariumid

Saksamaa maksuregistreerimisteenuse integratsioonivalim hõlmab järgmisi stsenaariume.

### <a name="sales-operations"></a>Müügitoimingud

- **Sularaha ja kandega müügi ja tagastuste registreerimine maksuregistreerimisteenuses:**

    Müügitoimingute registreerimine hõlmab järgmisi samme:

    1. Kande alguse registreerimine

        Iga tehingu algus registreeritakse tehnilises turvaelemendis (TSE), mis on ühendatud EFR-teenusega. Registreerimise tulemusena määrab TSE tehingu ID (TID).

    2. Kande lõpu registreerimine

        Kui tehing tehakse kassas, registreeritakse see sama TID abil, mis määrati tehingu käivitamise registreerimisel. Sel hetkel saadetakse üksikasjalikud tehinguandmed fiskaalregistreerimisteenusele. Need andmed sisaldavad müügirea teavet ning teavet allahindluste, maksete ja maksude kohta.

    3. Vastuse hõivamine fiskaalregistreerimisteenusest

        Turbeandmed võetakse TSE-lt vastuse osana ja salvestatakse kandesse kanali andmebaasis. Turvaandmed koosnevad järgmisest teabest:

        - TID
        - Kande alguse kuupäev ja kellaaeg
        - Kande lõpu kuupäev ja kellaaeg
        - Allkirjaloendur
        - Kontrolli väärtust
        - TSE seerianumber

- **Klienditellimuste registreerimine finantsregistreerimisteenuses:** registreerimisprotsess on sama, mis sularaha ja müügi ja tagastuste protsess.
- **Kinkekaarte ja hoiuseid hõlmavate toimingute registreerimine:** registreerimisprotsess on sama, mis sularaha ja müügi ja tagastuste protsess.

#### <a name="notifying-users-about-fiscal-registration-failures"></a>Kasutajate teavitamine finantsregistreerimise tõrgetest

On kaks võimalust, kuidas maksuregistreerimisteenus saab kasutajaid finantsregistreerimisel ilmnenud tõrgetest teavitada.

- Saate printida vastusest **kviitungite väljal Teave**.
- Saate kassas kuvada eelarvepoliitika teatised kasutajasõnumitena.

    > [!NOTE]
    > See teavitusmehhanism nõuab, et **lehel Konnektori tehniliste profiilide parameeter** Kuva fiskaalregistreerimisteatised **oleks sisse lülitatud**.

#### <a name="printing-receipts"></a>Kviitungite printimine

Kviitungite printimine on Saksamaal kohustuslik. Kõik kviitungid peavad sisaldama vähemalt järgmist teavet:

- Ettevõtte nimi ja aadress
- Teave kaupade, sealhulgas nende hindade ja koguste kohta
- Teave saadud maksete kohta
- Teave maksude kohta, sealhulgas kogusummad maksumäära kohta
- Turbeandmed:

    - TID
    - Kande alguse kuupäev ja kellaaeg
    - Kande lõpu kuupäev ja kellaaeg
    - Allkirjaloendur
    - Kontrolli väärtust
    - TSE seerianumber

- Informatiivne sõnum

> [!NOTE]
> Kviitungitele saab printida ka QR-koodi. Kuigi QR-kood on valikuline, on see väga soovitatav. Lisateavet selle kohta, kuidas saada QR-koodi osana fiskaalregistreerimisteenuse vastusest, leiate EFSTA dokumentatsiooni\[ veebisaidil avaldatud \] dokumendist "EFR Guide [DE](https://public.efsta.net/efr/)".
>
> **Kviitungite väljal Teave** kuvatakse finantsregistreerimisteenuse teatis. Näiteks kui allkirjaseade on katki, saab kviitungile printida eriteksti.

#### <a name="voided-suspended-and-recalled-transactions"></a>Tühistatud, peatatud ja tagasikutsutud kanded

- Tühistatud kanne registreeritakse taotlusena lõpetada kanne finantsregistreerimisteenuses.
- Peatatud kanne registreeritakse taotlusena lõpetada tehing finantsregistreerimisteenuses.
- Peatatud kande tagasikutsumine registreeritakse uue kande algusena finantsregistreerimisteenuses.

### <a name="non-sales-transactions-and-shift-closing"></a>Müügivälised kanded ja vahetuste sulgemine

Järgmised müügivälised kanded registreeritakse finantsregistreerimisteenuses mitte fiscal-operatsioonidena, kasutades **NFS-silti**:

- Deklareeri algsumma
- Sularaha sissemakse
- Väljamakse
- Seifi viidav raha
- Raha hoiustamine panka
- Tulukontod
- Kulukontod

Operatsioon **Sule vahetus** registreeritakse ka mitte-fiskaalse toiminguna fiskaalregistreerimisteenuses, kasutades **NFS-silti**.

### <a name="data-export-and-audit"></a>Andmete eksportimine ja auditeerimine

Kõik tehingud peab olema allkirjastatud TSE poolt, et tagada nende terviklikkus, autentsus ja täielikkus ning aidata vältida salvestatud andmetega manipuleerimist.

> [!WARNING]
> Kasutada saab ainult sertifitseeritud TSE-d. Lisateavet EFR-lahenduses toetatavate TSE-de tüüpide ja mudelite kohta leiate EFSTA dokumentatsiooni\[ veebisaidil avaldatud dokumendist \]"EFR Guide [DE](https://public.efsta.net/efr/)". TSE valimise ja hankimise kohta lisateabe saamiseks võtke ühendust EFSTA-ga [...](https://www.efsta.eu/at/kontakt).

Saksamaa määrused nõuavad toetust DSFinV-K ekspordile. DSFinV-K ekspordi saab käivitada EFR-lahenduses. Lisateavet DSFinV-K ekspordi kohta leiate EFSTA dokumentatsiooni\[ veebisaidil avaldatud dokumendist \]"EFR Guide [DE](https://public.efsta.net/efr/)".

### <a name="limitations-of-the-sample"></a>Proovi piirangud

Maksuregistreerimisteenus toetab ainult stsenaariume, kus käibemaks sisaldub hindades. Seetõttu **peab suvand Hinnad sisaldavad käibemaksu** seadma nii **kaupluste kui ka klientide jaoks jah**.

Rahandusteenus ei toeta olukordi, kus samale kandereale rakendatakse rohkem kui ühte käibemaksukoodi.

Fiskaalintegratsiooni raamistik ei toeta müügipakkumisi. Seetõttu ei ole need toimingud fiskaalteenistuses registreeritud.

## <a name="set-up-commerce-for-germany"></a>Saksamaa kaubanduse häälestamine

Selles jaotises kirjeldatakse Saksamaale omast ja soovitatavat kaubandussätteid. Lisateavet häälestusteabe kohta leiate teemast [Commerce'i avaleht](../index.md).

Saksamaale omaste funktsioonide kasutamiseks peate määrama järgmised sätted.

- Määrake **juriidilise isiku esmasel aadressil väli Riik/regioon** väljaks **DEU** (Saksamaa).
- Seadke **iga Saksamaal asuva kaupluse kassafunktsioonide profiilis välja ISO tähis** tähiseks **DE** (Saksamaa).

Samuti peate määrama Saksamaa jaoks järgmised sätted. Käivitage kindlasti sobivad jaotustööd pärast seadistuse lõpuleviimist.

### <a name="set-up-vat-per-german-requirements"></a>Km häälestamine Saksa nõuete kohta

Peate looma käibemaksukoodid, käibemaksugrupid ja kauba käibemaksugrupid. Samuti peate seadistama toodete ja teenuste käibemaksuteabe. Lisateavet käibemaksufunktsioonide seadistamise ja kasutamise kohta leiate teemast [Käibemaksu ülevaade](../../finance/general-ledger/indirect-taxes-overview.md).

Müügikviitungitel saate printida käibemaksukoodi lühendatud koodi (näiteks "A" või "B"). Selle funktsiooni kättesaadavaks tegemiseks seadke **välja** Tähis printimiseks **lehel Käibemaksukoodid**.

### <a name="set-up-stores"></a>Kaupluste häälestamine

Värskendage **lehel Kõik kauplused** poe üksikasju. Täpsemalt määrake järgmised parameetrid.

- Määrake väljal **Käibemaksugrupp** käibemaksugrupp, mida tuleks kasutada vaikekliendile müügiks.
- Määrake **suvandi Hinnad sisaldavad käibemaksu** valikuks **Jah**.
- Määrake **väli Nimi** ettevõtte nimeks. See muudatus aitab tagada, et ettevõtte nimi kuvatakse müügikviitungil. Teise võimalusena saate ettevõtte nime lisada müügikviitungi paigutusele vabas vormis tekstina.
- **Määrake välja Maksu ID-number (TIN)** ettevõtte ID-numbriks. See muudatus aitab tagada, et ettevõtte ID-number kuvatakse müügikviitungil. Teise võimalusena saate ettevõtte ID-numbri lisada müügikviitungi paigutusele vabas vormis tekstina.

### <a name="set-up-functionality-profiles"></a>Funktsiooniprofiilide häälestamine

Kassafunktsioonide profiilide häälestamine. Seadistage **kiirkaardil Tarne nummerdamine** kviitungi nummerdamine, luues või värskendades kirjeid müügi **-,** müügitellimuse **- ja** tagastustarne **kandetüüpide jaoks**.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Kohandatud väljade konfigureerimine nii, et neid saaks kasutada müügi sissetulekute vormingutes

Saate konfigureerida keeleteksti ja kohandatud väljad, mida kasutatakse kassa kviitungi vormingutes. Kviitungi häälestuse loonud kasutaja vaikeettevõte peaks olema sama juriidiline isik, kus keeleteksti häälestus luuakse. Teise võimalusena tuleks luua samad keeletekstid nii kasutaja vaikeettevõttes kui ka selle poe juriidilises isikus, kellele häälestus on loodud.

**Lisage lehel Keeletekst** kviitungipaigutuste kohandatud väljade siltide jaoks järgmised kirjed. Pange tähele, et **tabelis kuvatavad keele ID**, **teksti ID** ja **tekstiväärtused** on vaid näited. Saate neid muuta, et need vastaksid teie vajadustele. Kasutatavad teksti ID **väärtused peavad siiski** olema kordumatud ja need peavad olema võrdsed või suuremad kui 900001.

Lisage järgmised kassasildid **lehe Keele tekstijaotise** jaotisse **Kassa**.

| Keele ID | Teksti ID | Tekst                                  |
|-------------|---------|---------------------------------------|
| EN-US       | 900001  | QR-kood                               |
| EN-US       | 900002  | Kande ID                        |
| EN-US       | 900003  | Maksu jaemüügi prindikood                 |
| EN-US       | 900004  | Maksusumma (müük)                    |
| EN-US       | 900005  | Maksu alus (müük)                     |
| EN-US       | 900006  | Kande alguskuupäeva kellaaeg           |
| EN-US       | 900007  | Kande lõppkuupäeva kellaaeg             |
| EN-US       | 900008  | Turvaelemendi seerianumber |
| EN-US       | 900009  | Allkirjaloendur                     |
| EN-US       | 900010  | Kontrolli väärtust                           |
| EN-US       | 900011  | Infoteade                          |

**Lisage lehel Kohandatud väljad** kviitungipaigutuste kohandatud väljadele järgmised kirjed. Pange tähele, et **pealdise teksti ID** väärtused peavad vastama **lehel Keele tekst** määratud teksti ID **väärtustele**.

| Nimi                            | Tüüp    | Pealdise teksti ID |
|---------------------------------|---------|-----------------|
| QRCODEDE\_                      | Sissetulek | 900001          |
| TRANSACTIONIDDE\_               | Sissetulek | 900002          |
| RETAILPRINTCODEDE\_             | Sissetulek | 900003          |
| SALESTAXAMOUNTDE\_              | Sissetulek | 900004          |
| SALESTAXBASISDE\_               | Sissetulek | 900005          |
| TRANSACTIONSTARTDATETIMEDE\_    | Sissetulek | 900006          |
| TRANSACTIONENDDATETIMEDE\_      | Sissetulek | 900007          |
| SECURITYELEMENTSERIALNUMBERDE\_ | Sissetulek | 900008          |
| SIGNCOUNTERDE\_                 | Sissetulek | 900009          |
| SIGNDE\_                        | Sissetulek | 900010          |
| INFOMESSAGEDE\_                 | Sissetulek | 900011          |

> [!NOTE]
> On oluline määrata õiged kohandatud väljanimed, nagu on loetletud eelmises tabelis. Vale kohandatud välja nimi põhjustab kviitungitel puuduvaid andmeid.

### <a name="configure-receipt-formats"></a>Sissetulekuvormingute konfigureerimine

Muutke iga nõutava kviitungivormingu väärtuseks **Prindi käitumine** väärtuseks **Alati printimine**.

Lisage kviitungivormingu kujundaja vastavatele kviitungi jaotistele järgmised kohandatud väljad. Pange tähele, et väljanimed vastavad eelmises jaotises määratletud keeletekstidele.

- **Päis:** Lisage järgmised väljad.

    - **Kaupluse nimi** ja **MAKSUID-number** väljad, mida kasutatakse ettevõtte nime ja identifitseerimisnumbri printimiseks sissetulekutele. Teise võimalusena saate vabas vormis tekstina lisada paigutusele ettevõtte nime ja identifitseerimisnumbri.
    - **Kaupluse aadress**, **kuupäev**, **kellaaeg 24H**, **Kviitungi number** ja **Registri numbri** väljad.

- **read:** Lisage järgmised väljad:

    - **Asja nimi** valdkonnas
    - **Kogus** valdkonnas
    - **Hind kokku koos käibemaksuga** valdkonnas
    - **Maksu jaemüügi prindikood** välja, mida kasutatakse kaubale kehtivale käibemaksukoodile vastava lühendkoodi printimiseks

- **Jalus:** Lisage järgmised väljad:

    - Makseväljad, et prinditaks iga makseviisi maksesummad. Näiteks lisage **Pakkumise nimi** ja **Pakkumise summa** väljad paigutuse ühele reale.
    - Väljad **Maksude lõhkumine** väli rühm. Kõik selle väljarühma väljad tuleb trükkida ühele eraldi reale.

        - **Maksu ID** väli, mis on standardväli, mis võimaldab printida iga käibemaksukoodi kohta käibemaksu kokkuvõtte. Välja tuleb lisada uuele reale.
        - **Maksuprotsent** väli, mis on standardväli, mida kasutatakse müügimaksu koodi tegeliku maksumäära printimiseks.
        - **Maksubaas (müük)** välja, mida kasutatakse müügimaksu koodi jaoks kviitungi sularaha müügi kogusumma printimiseks. Ettemaksed ja kinkekaarditoimingud on välistatud.
        - **Maksusumma (müük)** väli, mida kasutatakse käibemaksukoodi sularahamüügi kviitungi maksusumma printimiseks.
        - **Maksu jaemüügi prindikood** välja, mida kasutatakse käibemaksukoodile vastava lühendatud koodi printimiseks.

    - Väljad, mis sisaldavad kaitstud tehinguandmeid, mille maksuregistri teenus tagastab:

        - **Tehingu ID** väli, mis identifitseerib sularahatehingu numbri maksuregistreerimise teenuses
        - **Tehingu alguskuupäeva kellaaeg** valdkonnas
        - **Tehingu lõppkuupäeva kellaaeg** valdkonnas
        - **Turvaelemendi seerianumber** valdkonnas
        - **Allkirjade loendur** valdkonnas
        - **Kontrolli väärtust** valdkonnas
        - **QR kood** väljale, mida kasutatakse registreeritud sularahatehingu viite printimiseks QR-koodi kujul

        > [!NOTE]
        > The **QR kood** väärtus saadakse fiskaalregistri vastusest. EFR tagastab vastuses QR-koodi ainult siis, kui väärtus on **Atribuudid** välja EFR konfiguratsioonis on kirjeldatud EFSTA dokumentatsioonis. QR-koodi vorming rakenduses **Atribuudid** EFR konfiguratsiooni väli peab olema seatud väärtusele **BMP**.

    - **Info sõnum** väljal, et kviitungitel oleks võimalik kuvada maksuregistreerimisteenuse teated. Näiteks kui allkirjaseade on katki, saab kviitungile printida eriteksti.

Kviitungivormingutega töötamise kohta lisateabe saamiseks vt [Kviitungivormingute seadistamine ja kujundamine](../receipt-templates-printing.md).

## <a name="set-up-fiscal-integration-for-germany"></a>Seadistage Saksamaa jaoks fiskaalintegratsioon

Saksamaa maksuregistreerimisteenuse integreerimise näidis põhineb [fiskaalintegratsiooni funktsionaalsus](fiscal-integration-for-retail-channel.md) ja on osa jaemüügi SDK-st. Näidis asub aadressil **src\\ Fiskaalintegratsioon\\ Efr** kaust [Dynamics 365 Commerce Lahendused](https://github.com/microsoft/Dynamics365Commerce.Solutions/) hoidla (näiteks [väljalaskes olev näidis/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). [Näidis koosneb](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskaaldokumendi pakkujast, mis on Commerce'i käitusaja CRT () laiendus, ja fiskaalse konnektori, mis on Commerce'i riistvarajaama laiendus. Lisateavet jaemüügi SDK kasutamise kohta leiate teemast [Retail SDK arhitektuur](../dev-itpro/retail-sdk/retail-sdk-overview.md) ja [Sõltumatu pakendiga SDK](../dev-itpro/build-pipeline.md) ehitustorustiku seadistamine.

> [!WARNING]
> Uue sõltumatu pakendi- [ja laiendusmudeli](../dev-itpro/build-pipeline.md) piirangute tõttu ei saa seda praegu selle fiskaalse integratsiooni valimi jaoks kasutada. Peate kasutama Retail SDK eelmist versiooni arendaja virtuaalses masinas (VM) elutsükli teenustes Microsoft Dynamics (LCS). Lisateabe saamiseks vt [Saksamaa fiskaalintegratsiooni valimi kasutuselevõtu juhised (pärand)](emea-deu-fi-sample-sdk.md).
>
> Eelarveintegratsiooni näidiste uue sõltumatu pakendi- ja laiendusmudeli toetamine on kavandatud hilisematele versioonidele.

Viige fiskaalintegratsiooni seadistamise etapid lõpule, nagu on kirjeldatud jaotises [Seadistage kaubanduskanalite fiskaalintegratsioon](setting-up-fiscal-integration-for-retail-channel.md):

1. [Saate häälestada finantsregistreerimise protsessi](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Märkige üles ka fiskaalse registreerimise protsessi sätted [selle maksuregistriteenuse integratsiooninäidise spetsiifiline](#set-up-the-registration-process).
1. [Saate määrata tõrkekäsitluse sätted](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

    > [!WARNING]
    > Eelarveintegratsiooni raamistiku vigade käsitlemise võimalused ei pruugi olla kohalike maksueeskirjadega täielikult kooskõlas.
    >
    > - Soovitame teil lahkuda **Jätkake veaga** valik peal **Maksustamise registreerimise protsess** leht välja lülitatud, sest kõik tehingud peavad olema korrektselt registreeritud, isegi kui esimene fiskaalse registreerimise katse ei õnnestunud.
    > - Enne kui lülitate sisse **Vahele jätma** või **Märgi registreerituks** valik peal **Maksustamise registreerimise protsess** lehel, peaksite arutama neid maksuregistreerimisprotsessi muudatusi oma maksukonsultandi või kohaliku maksuametiga.

1. [Lubage edasilükatud finantsregistreerimise käsitsi käivitamine](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Kanali komponentide](#configure-channel-components) konfigureerimine.

### <a name="set-up-the-registration-process"></a>Registreerimisprotsessi häälestamine

Registreerimisprotsessi lubamiseks järgige Commerce'i peakontori seadistamiseks neid juhiseid. Lisateavet vt teemast [Fiscal Integration for Commerce channels](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process) häälestamine.

1. Laadige alla rahandusdokumendi pakkuja ja fiskaalse konnektori konfiguratsioonifailid.

    1. Avage lahenduste [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) hoidla.
    1. Valige õige väljalaskeharu versioon vastavalt oma SDK/rakenduse versioonile (nt **[release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Avatud **src \> Fiskaalintegratsioon \> Efr**.
    1. Laadige alla maksudokumendi pakkuja konfiguratsioonifail aadressilt **Konfiguratsioonid \> Dokumendipakkujad \> DocumentProviderFiscalEFRSampleGermany.xml** (näiteks, [vabastamise fail/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders/DocumentProviderFiscalEFRSampleGermany.xml)).
    1. Laadige alla maksuühenduse konfiguratsioonifail aadressilt **Konfiguratsioonid \> Ühendused \> ConnectorEFRSample.xml** (näiteks, [vabastamise fail/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)).

    > [!WARNING]
    > Uue sõltumatu pakendi- [ja laiendusmudeli](../dev-itpro/build-pipeline.md) piirangute tõttu ei saa seda praegu selle fiskaalse integratsiooni valimi jaoks kasutada. Peate kasutama Retail SDK eelmist versiooni arendaja VM-is LCS-is. Selle fiskaalse integratsiooni näidise konfiguratsioonifailid asuvad LCS-i arendaja VM-i jaemüügi SDK järgmistes kaustades.
    >
    > - **Maksudokumendi pakkuja konfiguratsioonifail:** RetailSdk\\ Näidislaiendid\\ CommerceRuntime\\ Extensions.DocumentProvider.EFRSample\\ Seadistamine\\ DocumentProviderFiscalEFRSampleGermany.xml
    > - **Fiskaalse konnektori konfiguratsioonifail:** RetailSdk\\ Näidislaiendid\\ Riistvarajaam\\ Laiendus.EFRSnäidis\\ Seadistamine\\ ConnectorEFRSample.xml
    > 
    > Eelarveintegratsiooni näidiste uue sõltumatu pakendi- ja laiendusmudeli toetamine on kavandatud hilisematele versioonidele.

1. Valige suvandid **Jaemüük ja kaubandus \> Headquartersi häälestus \> Parameetrid \> Commerce’i ühiskasutuses parameetrid**. peal **Kindral** vahekaardil määrake **Luba maksuintegratsioon** võimalus **Jah**.
1. Minema **Jaemüük ja kaubandus \> Kanali seadistamine \> Fiskaalne integratsioon \> Maksudokumentide pakkujad** ja laadige varem alla laaditud maksudokumendi pakkuja konfiguratsioonifail.
1. Minema **Jaemüük ja kaubandus \> Kanali seadistamine \> Fiskaalne integratsioon \> Fiskaalühendused** ja laadige varem alla laaditud fiskaalse konnektori konfiguratsioonifail.
1. Minema **Jaemüük ja kaubandus \> Kanali seadistamine \> Fiskaalne integratsioon \> Konnektori funktsionaalsed profiilid**. Looge uus konnektori funktsionaalne profiil. Valige dokumendipakkuja ja varem laaditud konnektor. Värskendage andmete vastendamise [sätteid](#default-data-mapping) vastavalt vajadusele.
1. Minema **Jaemüük ja kaubandus \> Kanali seadistamine \> Fiskaalne integratsioon \> Konnektori tehnilised profiilid**. Looge uus konnektori tehniline profiil ja valige varem laaditud fiskaalkonnektor. Värskendage [konnektori sätteid](#fiscal-connector-settings) vastavalt vajadusele.
1. **Avage jaemüügi- ja kaubanduskanali \> häälestus \> Fiskaalintegratsioon \> Fiskaalkonnektorigrupid**. Looge varem loodud konnektori funktsionaalse profiili jaoks uus fiskaalse konnektori rühm.
1. Minema **Jaemüük ja kaubandus \> Kanali seadistamine \> Fiskaalne integratsioon \> Fiskaalsed registreerimise protsessid**. Looge uus maksuregistreerimisprotsess ja fiskaalse registreerimise protsessi etapp ning valige varem loodud maksuühenduse rühm.
1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassaprofiilid \> Funktsiooniprofiilid**. Valige funktsiooniprofiil, mis on lingitud poega, kus registreerimisprotsess tuleks aktiveerida. peal **Maksustamise registreerimise protsess** FastTab, valige varem loodud maksuregistreerimisprotsess.
1. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassaprofiilid \> Riistvaraprofiilid**. Valige riistvaraprofiil, mis on lingitud riistvarajaamaga, millega fiskaalprinter ühendatakse. Valige kiirkaardil **Fiskaalsed välisseadmed** varem loodud konnektori tehniline profiil.
1. Avage jaotusgraafik (**jae- ja kaubandus \> - ja kaubandus-kaubanduse IT-jaotuse \> ajakava**) ning valige tööd **1070** ja **1090**, et edastada andmeid kanali andmebaasi.

#### <a name="default-data-mapping"></a>Andmete vaikevastendus

Rahandusdokumendi pakkuja konfiguratsioonis, mis on esitatud fiskaalse integratsiooni valimi osana, kaasatakse järgmine andmete vaikevastendus.

- **Pakkumise tüübi kaardistamine** – Makseviiside vastendamine väärtustele **PayG** (maksegrupp) atribuut taotlustes, mis saadetakse maksuteenistusele. Siin on vaikevastendus.

    ```
    1: 0; 2: 1; 3: 3; 4: 8; 5: 2; 6: 0; 7: 7; 8: 6; 9: 0; 10: 8; 11: 1
    ```

    Iga paari esimene komponent tähistab kaupluse jaoks seadistatud makseviisi. Teine komponent tähistab vastavat maksegruppi, mida toetab EFR-i maksuregistreerimise teenus. Lisateavet maksegruppide kohta, mida EFR Saksamaal toetab, leiate aadressilt [EFR viide](https://public.efsta.net/efr/).

    Makseviiside näidiskaardistus vastab poe makseviisidele, mis on konfigureeritud standardsetes demoandmetes.

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
    | 11             | Mittekohalikud kontrollid    |

    Seetõttu peate näidisvastastust muutma vastavalt teie rakenduses konfigureeritud makseviisidele.

- **Kaasake kliendiandmed** – Kui see parameeter on sisse lülitatud, sisaldavad maksuteenistuse päringud klienditeavet (nt nimed ja aadressid) juhul, kui tehingusse lisatakse klient.
- **Käibemaksu (KM) määrade kaardistamine** – käibemaksukoodide jaoks seadistatud maksuprotsentide väärtuste vastendamine väärtustega **TaxG** (maksugrupp) atribuut taotlustes, mis saadetakse maksuteenistusele. Siin on vaikevastendus.

    ```
    A: 19.00; B: 7.00; C: 10.70; D: 5.50; E: 0.00
    ```

    Iga paari esimene komponent esindab käibemaksurühma, mida toetab EFR-i maksuregistreerimise teenus. Teine komponent tähistab vastavat KÄIBEMAKSUmäära. Lisateavet käibemaksugruppide kohta, mida EFR Saksamaal toetab, leiate veebisaidilt [EFR viide](https://public.efsta.net/efr/).

- **Kinkekaartide ja sissemaksete maksugrupp** – väärtus **TaxG** atribuut maksuteenistusele saadetavates päringutes, mis põhinevad toimingutel, mis hõlmavad kinkekaarte või sissemakseid. Siin on vaikevastendus.

    ```
    G
    ```

- **Maksugrupp käibemaksuvabaks** – väärtus **TaxG** atribuut maksuteenistusele saadetavates päringutes, mis põhinevad maksukohustustest vabastatud toimingutel. Siin on vaikevastendus.

    ```
    F
    ```

> [!NOTE]
> Vaikimisi andmete kaardistamise maksusätted vastutavad süsteemi maksusätete ja EFR-teenuse maksugruppide sobitamise eest. Maksugruppe saab kviitungitele printida ainult siis, kui **Kood printimiseks** väli on määratud **Müügimaksu koodid** lehel.

#### <a name="fiscal-connector-settings"></a>Fiskaalse konnektori sätted

Fiskaalse konnektori konfiguratsiooni kuuluvad järgmised sätted, mis on esitatud fiskaalse integratsiooni valimi osana.

- **Lõpp-punkti aadress** – maksuregistreerimisteenuse URL.
- **Aeg maha** – Aeg millisekundites, mille jooksul fiskaalne konnektor ootab maksuregistreerimisteenuse vastust.
- **Näita maksuregistreerimise teatisi** – See lipp juhib, kas operaatorile tuleks näidata teatisi, mille maksuregistri teenus tagastab.

### <a name="configure-channel-components"></a>Kanali komponentide seadistamine

> [!WARNING]
> Uue sõltumatu pakendi- [ja laiendusmudeli](../dev-itpro/build-pipeline.md) piirangute tõttu ei saa seda praegu selle fiskaalse integratsiooni valimi jaoks kasutada. Peate kasutama Retail SDK eelmist versiooni arendaja VM-is LCS-is. Lisateabe saamiseks vt [Saksamaa fiskaalintegratsiooni valimi kasutuselevõtu juhised (pärand)](emea-deu-fi-sample-sdk.md).
>
> Eelarveintegratsiooni näidiste uue sõltumatu pakendi- ja laiendusmudeli toetamine on kavandatud hilisematele versioonidele.

#### <a name="set-up-the-development-environment"></a>Seadistage arenduskeskkond

Näidise testimiseks ja laiendamiseks arenduskeskkonna seadistamiseks toimige järgmiselt.

1. Kloonige või laadige alla [Dynamics 365 Commerce Lahendused](https://github.com/microsoft/Dynamics365Commerce.Solutions) hoidla. Valige õige väljalaske haru versioon vastavalt oma SDK/rakenduse versioonile. Lisateabe saamiseks vt [Laadige alla jaemüügi SDK näidised ja viitepaketid GitHubist ja NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Avage EFR-lahendus aadressil **Dynamics365Commerce.Solutions\\ Fiskaalintegratsioon\\ Efr\\ EFR.sln**, ja ehitada see.
1. Installige Commerce'i käitusaja laiendused:

    1. Otsige üles CRT laienduse paigaldaja:

        - **Kaubanduse mastaabiüksus:** Aastal **Efr\\ Skaalaühik\\ ScaleUnit.EFR.Installer\\ prügikast\\ Silumine\\ net461** kaust, otsige üles **ScaleUnit.EFR.Installer** paigaldaja.
        - **Kohalik CRT kaasaegses POS-is:** Aastal **Efr\\ Kaasaegne POS\\ ModernPOS.EFR.Installer\\ prügikast\\ Silumine\\ net461** kaust, otsige üles **ModernPOS.EFR.Installer** paigaldaja.

    1. Alustage CRT laienduse installija käsurealt:

        - **Kaubanduse mastaabiüksus:**

            ```Console
            ScaleUnit.EFR.Installer.exe install --verbosity 0
            ```

        - **Kohalik CRT kaasaegses POS-is:**

            ```Console
            ModernPOS.EFR.Installer.exe install --verbosity 0
            ```

1. Installige riistvarajaama laiendused:

    - Aastal **Efr\\ Riistvarajaam\\ HardwareStation.EFR.Installer\\ prügikast\\ Silumine\\ net461** kaust, otsige üles **HardwareStation.EFR.Installer** paigaldaja.
    - Käivitage laienduse installija käsurealt:

        ```Console
        HardwareStation.EFR.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Tootmiskeskkond

Järgige juhiseid [Seadistage fiskaalintegratsiooni näidise jaoks ehituskonveier](fiscal-integration-sample-build-pipeline.md) luua ja vabastada Cloud Scale Unit ja iseteenindusega juurutatavad paketid fiskaalintegratsiooni näidise jaoks. The **EFR build-pipeline.yml** malli YAML-faili leiate **Torujuhe\\ YAML_Files** kaust [Dynamics 365 Commerce Lahendused](https://github.com/microsoft/Dynamics365Commerce.Solutions) hoidla.

## <a name="design-of-extensions"></a>Laienduste kujundus

Saksamaa maksuregistreerimisteenuse integreerimise näidis põhineb [fiskaalintegratsiooni funktsionaalsus](fiscal-integration-for-retail-channel.md) ja on osa jaemüügi SDK-st. Näidis asub aadressil **src\\ Fiskaalintegratsioon\\ Efr** kaust [Dynamics 365 Commerce Lahendused](https://github.com/microsoft/Dynamics365Commerce.Solutions/) hoidla (näiteks [väljalaskes olev näidis/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Näidis [koosneb](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskaaldokumentide pakkuja, mis on laiendus CRT ja fiskaalne pistik, mis on Commerce Hardware Stationi laiendus. Lisateavet jaemüügi SDK kasutamise kohta leiate teemast [Retail SDK arhitektuur](../dev-itpro/retail-sdk/retail-sdk-overview.md) ja [Sõltumatu pakendiga SDK](../dev-itpro/build-pipeline.md) ehitustorustiku seadistamine.

> [!WARNING]
> Uue sõltumatu pakendi- [ja laiendusmudeli](../dev-itpro/build-pipeline.md) piirangute tõttu ei saa seda praegu selle fiskaalse integratsiooni valimi jaoks kasutada. Peate kasutama Retail SDK eelmist versiooni arendaja VM-is LCS-is. Lisateabe saamiseks vt [Saksamaa fiskaalintegratsiooni valimi kasutuselevõtu juhised (pärand)](emea-deu-fi-sample-sdk.md). Eelarveintegratsiooni näidiste uue sõltumatu pakendi- ja laiendusmudeli toetamine on kavandatud hilisematele versioonidele.

### <a name="crt-extension-design"></a>CRT laienduse disain

Fiskaaldokumendi pakkuja laienduse eesmärk on luua teenusepõhiseid dokumente ja käsitleda fiskaalregistreerimisteenuse vastuseid.

#### <a name="request-handler"></a>Taotluse käitleja

Dokumendipakkuja **jaoks on üks päringukäsitleja DocumentProviderEFRFiscalDEU**. Seda käitlejat kasutatakse finantsregistreerimisteenuse finantsdokumentide loomiseks. See on päritud **INamedRequestHandleri** liidesest. **Käitleja nime tagastamise eest vastutab meetod HandlerName**. Käitleja nimi peaks vastama Commerce'i peakontoris määratud konnektori dokumendipakkuja nimele.

Konnektor toetab järgmisi taotlusi.

- **GetFiscalDocumentDocumentProviderRequest** – see taotlus sisaldab teavet selle kohta, milline dokument tuleks luua. See tagastab teenusepõhise dokumendi, mis tuleks registreerida maksuregistreerimisteenuses.
- **GetFiscalTransactionExtendedDataDocumentProviderRequest** – see taotlus tagastab vastuse koos laiendatud andmetega.

#### <a name="configuration"></a>Konfiguratsioon

Maksudokumendi pakkuja konfiguratsioonifail asub aadressil **src\\ Fiskaalintegratsioon\\ Efr\\ Konfiguratsioonid\\ Dokumendipakkujad\\ DocumentProviderFiscalEFRSampleGermany.xml** aastal [Dynamics 365 Commerce Lahendused](https://github.com/microsoft/Dynamics365Commerce.Solutions/) hoidla. Faili eesmärk on võimaldada fiskaaldokumentide pakkuja seadeid konfigureerida Commerce'i peakorteris. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetega.

### <a name="hardware-station-extension-design"></a>Riistvarajaama laienduse disain

Fiskaalühenduseks oleva laienduse eesmärk on suhelda maksuregistriteenusega.

Riistvarajaama laiendus on **HardwareStation.Extension.EFRSample**. See kasutab HTTP-protokolli dokumentide esitamiseks, mis CRT laiendus genereerib maksuregistreerimisteenuse. Samuti käsitleb see maksuregistreerimisteenuselt saadud vastuseid.

#### <a name="request-handler"></a>Taotluse käitleja

The **EFRHandler** päringu töötleja on maksuregistreerimisteenuse taotluste käsitlemise sisenemispunkt. See töötleja on päritud **INamedRequestHandler** liides. **Käitleja nime tagastamise eest vastutab meetod HandlerName**. Töötleja nimi peaks ühtima fiskaalse konnektori nimega, mis on määratud Commerce'i peakorteris.

Konnektor toetab järgmisi taotlusi.

- **SubmitDocumentFiscalDeviceRequest** – See päring saadab dokumendid maksuregistreerimisteenistusele ja saadab sealt vastuse.
- **IsReadyFiscalDeviceRequest** – Seda päringut kasutatakse maksuregistriteenuse tervisekontrolliks.
- **InitializeFiscalDeviceRequest** – Seda päringut kasutatakse maksuregistreerimisteenuse lähtestamiseks.

#### <a name="configuration"></a>Konfiguratsioon

Fiskaalse konnektori konfiguratsioonifail asub aadressil **src\\ Fiskaalintegratsioon\\ Efr\\ Konfiguratsioonid\\ Ühendused\\ ConnectorEFRSample.xml** aastal [Dynamics 365 Commerce Lahendused](https://github.com/microsoft/Dynamics365Commerce.Solutions/) hoidla. Faili eesmärk on võimaldada fiskaalühenduse seadete konfigureerimist Commerce'i peakorteris. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetega.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
