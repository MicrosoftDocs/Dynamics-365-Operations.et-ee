---
title: Juhtseadme integratsiooni näidis Rootsi jaoks
description: Selles teemas antakse ülevaade Rootsi fiskaalintegratsiooni näidistest Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-10-08
ms.openlocfilehash: 32c2cf31d82d17d3391536e7a9f1722e1462c336
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944762"
---
# <a name="control-unit-integration-sample-for-sweden"></a>Juhtseadme integratsiooni näidis Rootsi jaoks

[!include [banner](../includes/banner.md)]

Selles teemas antakse ülevaade Rootsi fiskaalintegratsiooni näidistest Microsoft Dynamics 365 Commerce.

> [!NOTE]
> Fiskaalintegratsiooni näidisfunktsioon asendab kassa [integratsiooni varasema näidist Rootsi kontrollüksustega](retail-sdk-control-unit-sample.md). Varasem näidis ei kasuta fiskaalintegratsiooni [raamistikku](./fiscal-integration-for-retail-channel.md) ja see aegub hilisemates värskendustes. Lisateabe saamiseks selle kohta, kuidas varasemast näidisst üle siirdada Dynamics 365 Commerce **versioonile 10.0.22 ja varasemale versioonile vastavasse näidisse, vaadake** varasemast integratsiooninäidandist [migreerimist](emea-swe-fi-sample-sdk.md#migrating-from-the-earlier-integration-sample).

Rootsi Commerce'i funktsioonid hõlmavad kassa (POS) näidisintegratsiooni Rootsispetsiifiliste finantsseadmetega, mida nimetatakse *kontrollüksusteks*. See näidis laiendab [fiskaalintegratsiooni](fiscal-integration-for-retail-channel.md) funktsiooni. Eeldatakse, et juhtüksus on füüsiliselt ühendatud riistvarajaamaga, millega kassa on ühendatud. Näiteks kasutab see näidis Retail [HTT AB CleanCash Type A kontrollüksuse rakenduse](https://www.retailinnovation.se/produkter) programmeerimisliidest (API). Kasutatakse CleanCash API versiooni 1.1.4.

Näidis esitatakse lähtekoodina ja on osa jaemüügi tarkvara arenduskomplektist (SDK).

Microsoft ei vabasta rakenduse Retail Retail HTT AB riistvara, tarkvara ega dokumentatsiooni. Lisateabeks kontrollüksuse toomiseks ja selle tööks võtke ühendust rakenduse [Retail HTT ABga.](https://www.retailinnovation.se/)

## <a name="scenarios"></a>Stsenaariumid

Rootsi kontrollüksuse integratsiooni näidis hõlmab järgmisi võimalusi.

- Müügi-, tagastuste ja kviitungikoopiad registreeritakse automaatselt kontrollüksuses, mis on ühendatud müügikohaga ühendatud riistvarajaamaga.
- Kontrollkood ja registreeritud kande kontrollüksuse tootmisnumber fikseeritakse kontrollüksusest ja salvestatakse kandesse. Neid andmeid nimetatakse ka *fiskaalvastuseks.* Fiskaalvastust saab vaadata lehel **Kaupluse** kanded.
- Kontrollkoodi kohandatud välju ja kontrollühiku tootmisnumbrit saab kviitungi kavandisse lisada. Sel viisil saate printida sissetulekukande fiskaalvastuse.
- Kande fiskaalvastus kuvatakse elektroonilisel **töölehel (Rootsi)** kanali aruandes.
- Saadaval on mitu tõrke käsitlemise võimalust. Järgmisena on toodud mõned näited.

    - Fiskaalregistreerimist saab uuesti teha, kui see on võimalik. Kui näiteks juhtüksus ei ole ühendatud, ei ole valmis või ei vasta sellele, saate fiskaalregistreerimist uuesti käivitada.
    - Finantsregistreerimise edasilükkamine.
    - Jätte fiskaalregistreerimise vahele või märgite kande registreeritud koodina ja kaasate teabekoodid, et hõivata tõrke põhjus ja lisateave.
    - Kontrollige kontrollüksuse saadavust enne uue müügikande avamist või müügikande lõpetamist.

### <a name="limitations-of-the-sample"></a>Näidiste piirangud

Rootsi kontrollüksuse integratsiooni näidis ei toeta praegu klienditellimuse stsenaariume.

## <a name="setting-up-the-integration-with-control-units"></a>Kontrollüksustega integreerimise seadistamine

Lisateavet rootsi jaoks nõutava häälestuse kohta vt [Jaotisest Rootsi äri](./emea-swe-cash-registers.md#setting-up-commerce-for-sweden) seadistamine.

### <a name="configuring-swedenspecific-receipts"></a>Rootsi kindlate sissetulekute konfigureerimine

#### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Kohandatud väljade konfigureerimine, et neid saaks kasutada müügikviitungite kviitungi vormingutes

Saate konfigureerida keele teksti ja kohandatud väljad, mida kasutatakse kassa kviitungi vormingutes. Kviitungi häälestuse loonud kasutaja vaikeettevõte peaks olema sama juriidiline isik, kus keele teksti häälestus on loodud. Teise võimalusena tuleks samad keeletekstid luua nii kasutaja vaikeettevõttes kui ka kaupluse juriidilises isikus, mille jaoks häälestus on loodud.

Lisage **keele teksti** lehel kviitungi kavandite kohandatud väljade siltidele järgmised kirjed. Pange **tähele, et tabelis kuvatavad keele ID, teksti ID ja teksti väärtused** **on vaid** **näited**. Saate neid vastavalt oma nõuetele muuta. Teksi ID väärtused peavad siiski olema kordumatud ning olema võrdsed või **suuremad** kui 900001.

Lisage keele tekstilehe **müügikoha** jaotisesse järgmised **müügikoha** sildid.

| Keele ID | Teksti ID | Tekst                  |
|-------------|---------|-----------------------|
| en-US       | 900001  | Registri kontrollkood |
| en-US       | 900002  | Registreeri seade       |

Lisage **kviitungi** kavandite kohandatud väljade jaoks kohandatud väljadele järgmised kirjed lehel Kohandatud väljad. Pange **tähele, et pealdise teksti ID väärtused peavad vastama teksti** **ID** väärtustele, mille **määrate keele teksti** lehel.

| Nimi                         | Tüüp    | Pealdise teksti ID |
|------------------------------|---------|-----------------|
| SE_FISCALREGISTERCONTROLCODE | Sissetulek | 900001          |
| SE_FISCALREGISTERID          | Sissetulek | 900002          |

> [!NOTE]
> On oluline määrata õiged kohandatud väljanimed, nagu on loetletud ülaltoodud tabelis. Vale kohandatud välja nimi põhjustab sissetulekutes puuduvate andmete.

#### <a name="configure-receipt-formats"></a>Kviitungi vormingute konfigureerimine

Muutke iga nõutava kviitungi vormingu välja Prindikäitumine **väärtuseks** Alati **prindi**.

Lisage kviitungi vormingu kujundajasse jaluse jaotisse järgmised kohandatud **väljad**. Pange tähele, et väljanimed vastavad selle teema eelmises jaotises määratletud keeletekstidele.

- **Registri kontrollkood** – see väli prindib kontrollkoodi.
- **Registriseade** – see väli prindib kontrollüksuse tootmisnumbri.

Lisateavet kviitungi vormingutega töötades vt Kviitungi [mallidest ja](../receipt-templates-printing.md) printimisest.

### <a name="set-up-fiscal-integration-for-sweden"></a>Häälestage Rootsi finantsintegratsioon.

Rootsi kontrollüksuse integratsiooni näidis põhineb [fiskaalintegratsiooni](fiscal-integration-for-retail-channel.md) funktsioonil ja on osa Retail SDK-st. Näidis asub lahenduste hoidla **\\ kaustas FiscalIntegration \\ CleanCash (nt näidis**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/)[väljalaskes/9.33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash) Näidis [koosneb fiskaaldokumendi pakkujast, mis on Commerce Runtime'i () laiendus, ja fiskaalühendusest, mis](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices)CRT on Commerce Hardware Stationi laiendus. Lisateavet Retail SDK kasutamise kohta vt [Retail SDK arhitektuurist](../dev-itpro/retail-sdk/retail-sdk-overview.md) ja [iseseisva pakendamise SDK koostamisvõimaluste häälestamisest](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Uue sõltumatu pakendi- ja laiendusmudeli piirangute tõttu ei saa seda praegu selle [fiskaalintegratsiooni](../dev-itpro/build-pipeline.md) näidise jaoks kasutada. Retail SDK eelmist versiooni peate kasutama arendaja virtuaalmasinas (VM) Microsoft Dynamics elutsükli teenustes (LCS). Lisateavet vt Jaotisest [Juurutuse juhised kontrollühiku integreerimise näidis Rootsi jaoks](emea-swe-fi-sample-sdk.md) (pärand).
>
> Uutesse versioonidesse planeeritakse fiskaalintegratsiooni valimite uue sõltumatu pakendi- ja laiendusmudeli tugi.

Viige finantsintegratsiooni seadistuse etapid lõpule, nagu [on kirjeldatud Ärikanalite fiskaalintegratsiooni seadistamises](setting-up-fiscal-integration-for-retail-channel.md).

1. [Seadistage fiskaalregistreerimise protsess](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Lisaks tehke märkus fiskaalregistreerimise protsessi sätete kohta, mis on sellele [kontrollüksuse integreerimis näidisele omased.](#set-up-the-registration-process)
1. [Tõrke käsitlemise sätete](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings) seadistamine.
1. [Luba edasilükatud fiskaalregistreerimise käsitsi](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration) käivitamine.
1. [Kanali komponentide](#configure-channel-components) konfigureerimine.

### <a name="set-up-the-registration-process"></a>Registreerimisprotsessi häälestamine

Registreerimisprotsessi lubamiseks järgige neid samme Commerce headquartersi häälestamiseks. Lisateavet vt Commerce'i [kanalite fiskaalintegratsiooni](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process) häälestamine.

1. Laadige alla finantsdokumendi pakkuja ja fiskaalkonnektori konfiguratsioonifailid:

    1. Lahenduste [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) hoidla avamine.
    1. Valige õige väljalaske haruversioon vastavalt oma SDK-le/rakenduse versioonile (nt **[vabastamine/9.33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**
    1. Saate **avada src \> FiscalIntegration \> CleanCash.**
    1. Laadige alla finantsdokumendi pakkuja konfiguratsioonifail **commerceRuntime \> DocumentProvider.CleanCashSample \> Configuration \> DocumentProviderFiscalCleanCashSample.xml (nt väljalaske**[9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/CommerceRuntime/DocumentProvider.CleanCashSample/Configuration/DocumentProviderFiscalCleanCashSample.xml) fail).
    1. Laadige alla fiskaalkonnektori **konfiguratsioonifail HardwareStation \> Connectoris.CleanCashSample \> Configuration \> ConnectorCleanCashSample.xml (näiteks väljalaske**[fail/9.33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/HardwareStation/Connector.CleanCashSample/Configuration/ConnectorCleanCashSample.xml)

    > [!WARNING]
    > Uue sõltumatu pakendi- ja laiendusmudeli piirangute tõttu ei saa seda praegu selle [fiskaalintegratsiooni](../dev-itpro/build-pipeline.md) näidise jaoks kasutada. Retail SDK eelmist versiooni peate kasutama LCS-i arendaja VM-s. Selle fiskaalintegratsiooni näidiskonfiguratsiooni failid asuvad Retail SDK arendaja VM LCS-i kaustades:
    >
    > - **Fiskaaldokumendi pakkuja konfiguratsioonifail:** RetailSdk \\ SampleExtensions \\ CommerceRuntime \\ Extensions.DocumentProvider.CleanCashSample \\ Configuration \\ DocumentProviderFiscalCleanCashSample.xml
    > - **Fiskaalkonnektori** konfiguratsioonifail: RetailSdk \\ SampleExtensions \\ HardwareStation \\ Extension.CleanCashSample \\ Configuration \\ ConnectorCleanCashSample.xml
    > 
    > Uutesse versioonidesse planeeritakse fiskaalintegratsiooni valimite uue sõltumatu pakendi- ja laiendusmudeli tugi.

1. Valige suvandid **Jaemüük ja kaubandus \> Headquartersi häälestus \> Parameetrid \> Commerce’i ühiskasutuses parameetrid**. Seadke **vahekaardil** Üldine suvand Luba **fiskaalintegratsioon** väärtusele **Jah**.
1. Minge jaemüügi **ja ärikanali häälestuse \>\> fiskaalintegratsiooni finantsdokumendi pakkujate juurde ja laadige varem alla \>** laaditud finantsdokumendi pakkuja konfiguratsioonifail.
1. Minge **jaemüügi- ja ärikanali \>\>\> häälestuse fiskaalintegratsiooni fiskaalkonnektori ja laadige varem alla** laaditud fiskaalkonnektori konfiguratsioonifail.
1. Minge jaemüügi ja **ärikanali \> häälestuse \> fiskaalintegratsiooni \> konnektori** funktsiooniprofiilidesse. Looge uus konnektori funktsiooniprofiil. Valige dokumendipakkuja ja ühendus, mille varem laadisite. Värskendage [andmevastendussätted](#default-data-mapping) vastavalt vajadusele.
1. Minge jaemüügi ja **ärikanali \> häälestuse \> finantsintegratsiooni \> konnektori tehnilistesse** profiilidesse. Looge uus konnektori tehniline profiil ja valige varem laaditud fiskaalühendus. Uuendage [konnektori](#fiscal-connector-settings) sätteid vastavalt vajadusele.
6. Minge jaemüügi ja **ärikanali \> häälestuse \> fiskaalintegratsiooni \> fiskaalühenduse gruppidesse**. Looge varem loodud konnektori funktsiooniprofiilile uus fiskaalühenduse grupp.
7. Minge jaemüügi **ja ärikanali häälestuse \> fiskaalintegratsiooni \>\> fiskaalregistreerimisprotsessidesse.** Looge uus fiskaalregistreerimise protsess ja fiskaalregistreerimise protsessi samm ning valige varem loodud fiskaalühenduse grupp.
8. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassaprofiilid \> Funktsiooniprofiilid**. Valige funktsiooniprofiil, mis on lingitud kauplusega, kus registreerimisprotsess tuleks aktiveerida. Valige **finants registreerimisprotsessi** kiirkaardil varem loodud fiskaalregistreerimise protsess.
9. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassaprofiilid \> Riistvaraprofiilid**. Valige riistvaraprofiil, mis on lingitud riistvarajaamaga, millega fiskaalprinter on ühendatud. Valige **kiirkaardil Fiscal** peripherals varem loodud konnektori tehniline profiil.
10. Avage jaotusgraafik (Retail ja Commerce Retail ja Commerce IT Distribution schedule) ning valige tööd **\>\>** **1070 ja** **1090 andmete** edastamiseks kanali andmebaasi.

#### <a name="default-data-mapping"></a>Vaikeandmete vastendamine

Järgmine vaikeandmete vastendamine on kaasatud fiskaaldokumendi pakkuja konfiguratsiooni, mis antakse fiskaalintegratsiooni näidisosana:

- **Käibemaksu (KM) koodi vastendamine** – see vastendab seadmepõhised käibemaksukoodid vastavatele käibemaksukoodidele. KM-koodi vastendamiseks peab olema järgmine vorming:

    ```
    1 : code1 ; 2 : code2
    ```

    Siin on selle vormingu kohta selgitus.

    - *1* ja *2 on* seadmepõhised KM-koodid.
    - Semikoolon (;) - kasutatakse eraldajana.
    - *kood1* ja *kood2 on rakenduse Commerce headquarters* konfigureeritud käibemaksukoodid. Peate muutma näidisvastendust vastavalt rakenduses konfigureeritud maksukoodidele.

    Kontrollüksused toetavad kuni nelja erinevat KM-koodi. Seetõttu võib KM-koodi vastendamine olla seadistatud järgmiselt:

    ```
    1 : code1 ; 2 : code2 ; 3 : code3 ; 4 : code4
    ```

    > [!NOTE]
    > Mitu käibemaksukoodi saab vastendada sama seadmepõhise KM-koodiga.

#### <a name="fiscal-connector-settings"></a>Fiskaalühenduse sätted

Järgmised sätted on kaasatud fiskaalkonnektori konfiguratsiooni, mis on antud fiskaalintegratsiooni näidisosana:

- **Ühenduste string** – juhtüksuse ühenduse sätted.
- **Ajalõpp** – aja hulk millisekundites, mille juht ootab kontrollüksuselt vastuse ootamist.

### <a name="configure-channel-components"></a>Kanali komponentide konfigureerimine

> [!WARNING]
> Uue sõltumatu pakendi- ja laiendusmudeli piirangute tõttu ei saa seda praegu selle [fiskaalintegratsiooni](../dev-itpro/build-pipeline.md) näidise jaoks kasutada. Retail SDK eelmist versiooni peate kasutama LCS-i arendaja VM-s. Lisateavet vt Jaotisest [Juurutuse juhised kontrollühiku integreerimise näidis Rootsi jaoks](emea-swe-fi-sample-sdk.md) (pärand).
>
> Uutesse versioonidesse planeeritakse fiskaalintegratsiooni valimite uue sõltumatu pakendi- ja laiendusmudeli tugi.

#### <a name="set-up-the-development-environment"></a>Saate häälestada arenduskeskkonda.

Arenduskeskkonna katsetada ja näidist laiendada, järgige neid samme.

1. Rakenduste hoidla [Dynamics 365 Commerce leidmine](https://github.com/microsoft/Dynamics365Commerce.Solutions) või allalaadimine. Valige õige väljalaske haruversioon vastavalt oma SDK-le/rakenduse versioonile. Lisateavet vt jaotisest Jaemüügi SDK näidised ja viitepakendid alla laadida [GitHub-st ja NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Avage kontrollüksuse integreerimislahendus **dynamics365Commerce.Solutions \\ FiscalIntegration \\\\ CleanCash CleanCash.sln ja koostage** see.
1. Installi CRT laiendid:

    1. Leidke laiendi CRT installer:

        - **Commerce Scale Unit: kaustas** **CleanCash \\\\ ScaleUnit ScaleUnit.CleanCash.Installer \\ bin \\ Debug \\ net461** leidke **ScaleUnit.CleanCash.Installer.**
        - **Kohalik modern POS-s: leidke kaustast CRT** **CleanCash \\\\ ModernPOS.CleanCash.Installer \\ bin \\ Silumine \\ net461 kaust** **ModernPOS.CleanCash.Installer.**

    2. Käivitage CRT laiendiinstall käsurealt:

        - **Commerce Scalei üksus:**

            ```Console
            ScaleUnit.CleanCash.Installer.exe install --verbosity 0
            ```

        - **Kohalik CRT Modern POS-s:**

            ```Console
            ModernPOS.CleanCash.Installer.exe install --verbosity 0
            ```

1. Riistvarajaama laienduste installimine:

    1. Leidke kaustast **CleanCash \\\\ HardwareStation.CleanCash.Installer \\ bin \\ Debug \\ net461** kaust **HardwareStation.CleanCash.Installer.**
    1. Käivitage laiendiinstall käsurealt:

        ```Console
        HardwareStation.CleanCash.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Tootmiskeskkond

Järgige fiskaalintegratsiooni näidise jaoks koostevõimaluste häälestamise etappe, et luua ja vabastada pilveskaala üksus ja iseteeninduse juurutatavad paketid [fiskaalintegratsiooni](fiscal-integration-sample-build-pipeline.md) näidiskomplekti jaoks. **CleanCash build-pipeline.yml malli JAML faili leiate lahenduste** **\\ hoidla YAML_Files**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions) müügivõimalustest.

## <a name="design-of-the-extensions"></a>Laienduste kujundus

Rootsi kontrollüksuse integratsiooni näidis põhineb [fiskaalintegratsiooni](fiscal-integration-for-retail-channel.md) funktsioonil ja on osa Retail SDK-st. Näidis asub lahenduste hoidla **\\ kaustas FiscalIntegration \\ CleanCash (nt näidis**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/)[väljalaskes/9.33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash) Näidis [koosneb](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) fiskaaldokumendi pakkujast, mis on CRT laiendiks, ja fiskaalühendusest, mis on Commerce Hardware Stationi laiendus. Lisateavet Retail SDK kasutamise kohta vt [Retail SDK arhitektuurist](../dev-itpro/retail-sdk/retail-sdk-overview.md) ja [iseseisva pakendamise SDK koostamisvõimaluste häälestamisest](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Uue sõltumatu pakendi- ja laiendusmudeli piirangute tõttu ei saa seda praegu selle [fiskaalintegratsiooni](../dev-itpro/build-pipeline.md) näidise jaoks kasutada. Retail SDK eelmist versiooni peate kasutama LCS-i arendaja VM-s. Lisateavet vt Jaotisest [Juurutuse juhised kontrollühiku integreerimise näidis Rootsi jaoks](emea-swe-fi-sample-sdk.md) (pärand). Uutesse versioonidesse planeeritakse fiskaalintegratsiooni valimite uue sõltumatu pakendi- ja laiendusmudeli tugi.

### <a name="crt-extension-design"></a>CRT laiendi kujundus

Fiskaaldokumendi pakkuja laiendi eesmärk on luua teenusepõhiseid dokumente ja käsitseda kontrollüksuse vastuseid.

#### <a name="request-handler"></a>Nõudeohjur

Dokumendipakkuja jaoks **on olemas üks DocumentProviderCleanCash** taotluseohjur. Seda ohjurit kasutatakse finantsdokumentide loomiseks kontrollühiku jaoks.

See ohjur on päritud **INamedRequestHandler** liideselt. Meetod **HandlerName** vastutab ohjuri nime tagastamise eest. Ohjuri nimi peab vastama Commerce Headquartersis määratud konnektori dokumendi pakkuja nimele.

Konnektor toetab järgmisi taotlusi:

- **GetFiscalDocumentDocumentProviderRequest** – see taotlus sisaldab teavet selle kohta, milline dokument tuleks luua. See tagastab teenuseomase dokumendi, mis tuleb registreerida kontrollüksuses.
- **GetSupportedRegistrableEventsDocumentProviderRequest – see taotlus tagastab** tellitavate sündmuste loendi. Praegu toetatakse müügisündmusi ja auditi sündmusi.

#### <a name="configuration"></a>Konfiguratsioon

Fiskaaldokumendi pakkuja konfiguratsioonifail asub **lahenduste hoidlas src \\ FiscalIntegration \\ CleanCash \\ CommerceRuntime \\ DocumentProvider.CleanCashSample \\ Configuration \\ DocumentProviderFiscalCleanCashSample.xml.**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Selle faili eesmärk on lubada dokumendipakkuja sätted rakendusest Commerce headquarters konfigureerimist. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetele.

### <a name="hardware-station-extension-design"></a>Riistvarajaama laienduse kujundus

Fiskaalühenduseks olemise laiendi eesmärk on pidada ühendust kontrollüksusega. See kasutab HTTP-protokolli, et esitada dokumente, CRT mida laiend kontrollüksusele loob. Samuti käsitletakse kontrollüksuselt saadud vastuseid.

#### <a name="request-handler"></a>Nõudeohjur

**CleanCashHandler** taotluseohjur on sisenemispunkt kontrollüksuse käsitsemise taotluste jaoks.

Ohjur pärineb **INamedRequestHandler** liideselt. Meetod **HandlerName** vastutab ohjuri nime tagastamise eest. Ohjuri nimi peab ühtima Commerce Headquartersis määratud fiskaalühenduse nimega.

Konnektor toetab järgmisi taotlusi:

- **SubmitDocumentFiscalDeviceRequest – see taotlus saadab** dokumendid kontrollüksusesse ja tagastab sellelt vastuse.
- **IsReadyFiscalDeviceRequest – seda taotlust** kasutatakse kontrollüksuse seisundikontrolliks.
- **InitializeFiscalDeviceRequest** – seda taotlust kasutatakse kontrollüksuse lähtestamiseks.

#### <a name="configuration"></a>Konfiguratsioon

Fiskaalkonnektori konfiguratsioonifail asub **src \\ FiscalIntegration \\ CleanCash \\ HardwareStation \\ Connectoris.CleanCashSample \\ Configuration \\ ConnectorCleanCashSample.xml** lahenduste [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) hoidlas. Faili eesmärk on lubada finantsühenduse sätete konfigureerimist rakendusest Commerce headquarters. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetele.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
