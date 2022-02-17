---
title: Juhtseadme integratsiooni näidis Rootsi jaoks
description: See teema annab ülevaate Rootsi eelarveintegratsiooni proovist Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-10-08
ms.openlocfilehash: ace1bd5b1a06317b6753a34779ecfa96e519a63e
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2022
ms.locfileid: "8077009"
---
# <a name="control-unit-integration-sample-for-sweden"></a>Juhtseadme integratsiooni näidis Rootsi jaoks

[!include [banner](../includes/banner.md)]

See teema annab ülevaate Rootsi eelarveintegratsiooni proovist Microsoft Dynamics 365 Commerce.

> [!NOTE]
> See fiskaalse integratsiooni näidisfunktsioon asendab varasema [pos-integratsiooni valimi Rootsi juhtüksustega](retail-sdk-control-unit-sample.md). Varasem valim ei kasuta fiskaalintegratsiooni [raamistikku](./fiscal-integration-for-retail-channel.md) ja aegub hilisemates värskendustes. Lisateavet selle kohta, kuidas migreerida varasemast proovist proovi, mis vastab versioonile 10.0.22 ja varasemale Dynamics 365 Commerce versioonile **, leiate** teemast Varasema integratsioonivalimi [migreerimine.](emea-swe-fi-sample-sdk.md#migrating-from-the-earlier-integration-sample)

Rootsi kaubandusfunktsioon hõlmab müügikoha näidisintegratsiooni Rootsi-spetsiifiliste fiskaalseadmetega, mida nimetatakse *juhtüksusteks*. See valim laiendab fiskaalintegratsiooni [funktsiooni](fiscal-integration-for-retail-channel.md). Eeldatakse, et juhtseade on füüsiliselt ühendatud riistvarajaamaga, millega kassa on seotud. Näiteks kasutab see proov Rakenduse programmeerimisliidest (API) CleanCashi A-tüüpi [juhtseadmest](https://www.retailinnovation.se/produkter) retail Innovation HTT AB poolt. Kasutatakse CleanCashi API versiooni 1.1.4.

Proov on esitatud lähtekoodi kujul ja see on osa jaemüügi tarkvaraarenduskomplektist (SDK).

Microsoft ei väljasta rakenduses Retail Innovation HTT AB riistvara, tarkvara ega dokumente. Juhtseadme hankimiseks ja käitamiseks võtke ühendust rakendusega [Retail Innovation HTT AB](https://www.retailinnovation.se/).

## <a name="scenarios"></a>Stsenaariumid

Rootsi juhtüksuse integratsiooninäidis sisaldab järgmisi võimalusi.

- Müügi-, tagastus- ja kviitungikoopiad registreeritakse automaatselt juhtseadmes, mis on ühendatud müügikohaga seotud riistvarajaamaga.
- Registreeritud kande juhtseadme kontrollkood ja tootmisnumber võetakse juhtseadmest kinni ja salvestatakse tehingusse. Neid andmeid nimetatakse ka fiskaalseks *vastuseks*. Fiskaalvastust **saab vaadata lehel Poekanded**.
- Juhtkoodi kohandatud väljad ja juhtseadme tootmisnumbri saab kviitungi paigutusele lisada. Sel viisil saate printida kande fiskaalvastuse kviitungile.
- Kande fiskaalne vastus kuvatakse **elektroonilise töölehe (Rootsi)** kanali aruandes.
- Saadaval on mitu tõrke käsitlemise võimalust. Järgmisena on toodud mõned näited.

    - Kui on võimalik uuesti proovida, proovi uuesti maksu registreerimist. Kui juhtseade pole ühendatud, pole valmis või ei reageeri.
    - Lükake finantsregistreerimine edasi.
    - Jätke finantsregistreerimine vahele või märkige kanne registreerituks ning lisage tõrke põhjuse ja lisateabe jäädvustamiseks infokoodid.
    - Kontrollige juhtseadme saadavust enne uue müügikande avamist või müügikande lõpuleviimist.

### <a name="limitations-of-the-sample"></a>Proovi piirangud

Rootsi juhtüksuse integratsiooninäidis ei toeta praegu klienditellimuse stsenaariume.

## <a name="setting-up-the-integration-with-control-units"></a>Integratsiooni häälestamine juhtüksustega

Lisateavet Rootsi jaoks vajaliku seadistuse kohta leiate teemast [Rootsi kaubanduse](./emea-swe-cash-registers.md#setting-up-commerce-for-sweden) häälestamine.

### <a name="configuring-swedenspecific-receipts"></a>Rootsi-spetsiifiliste kviitungite konfigureerimine

#### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Kohandatud väljade konfigureerimine nii, et neid saaks kasutada müügi sissetulekute vormingutes

Saate konfigureerida keeleteksti ja kohandatud väljad, mida kasutatakse kassa kviitungi vormingutes. Kviitungi häälestuse loonud kasutaja vaikeettevõte peaks olema sama juriidiline isik, kus keeleteksti häälestus luuakse. Teise võimalusena tuleks luua samad keeletekstid nii kasutaja vaikeettevõttes kui ka selle poe juriidilises isikus, kellele häälestus on loodud.

**Lisage lehel Keeletekst** kviitungipaigutuste kohandatud väljade siltide jaoks järgmised kirjed. Pange tähele, et **tabelis kuvatavad keele ID**, **teksti ID** ja **tekstiväärtused** on vaid näited. Saate neid vastavalt oma vajadustele muuta. Kasutatavad teksti ID **väärtused peavad siiski** olema kordumatud ja need peavad olema võrdsed või suuremad kui 900001.

Lisage järgmised kassasildid **lehe** Keele teksti **jaotises Kassa**.

| Keele ID | Teksti ID | Tekst                  |
|-------------|---------|-----------------------|
| EN-US       | 900001  | Registreeri kontrollkood |
| EN-US       | 900002  | Registreeri seade       |

**Lisage lehel Kohandatud väljad** kviitungipaigutuste kohandatud väljadele järgmised kirjed. Pange tähele, et **pealdise teksti ID** väärtused peavad vastama **lehel Keele tekst** määratud teksti ID **väärtustele**.

| Nimi                         | Tüüp    | Pealdise teksti ID |
|------------------------------|---------|-----------------|
| SE_FISCALREGISTERCONTROLCODE | Sissetulek | 900001          |
| SE_FISCALREGISTERID          | Sissetulek | 900002          |

> [!NOTE]
> On oluline, et määraksite ülaltoodud tabelis loetletud õiged kohandatud väljanimed. Vale kohandatud välja nimi põhjustab kviitungitel puuduvaid andmeid.

#### <a name="configure-receipt-formats"></a>Sissetulekuvormingute konfigureerimine

Muutke iga nõutava kviitungivormingu väärtuseks **Prindi käitumine** väärtuseks **Alati printimine**.

Lisage kviitungivormingu kujundaja jaotisse **Jalus järgmised kohandatud väljad**. Pange tähele, et väljanimed vastavad selle teema eelmises jaotises määratletud keeletekstidele.

- **Registri kontrollkood** – see väli prindib juhtkoodi.
- **Registriseade** – see väli prindib juhtseadme tootmisnumbri.

Lisateavet kviitungivormingutega töötamise kohta leiate teemast [Kviitungimallid ja printimine](../receipt-templates-printing.md).

### <a name="set-up-fiscal-integration-for-sweden"></a>Saate häälestada Rootsi eelarveintegratsiooni.

Rootsi juhtüksuse integreerimise näidis põhineb fiskaalintegratsiooni [funktsioonil](fiscal-integration-for-retail-channel.md) ja on osa jaemüügi SDK-st. Proov asub lahenduste hoidla kaustas **src\\FiscalIntegration\\CleanCash**[Dynamics 365 Commerce (näiteks](https://github.com/microsoft/Dynamics365Commerce.Solutions/) proov väljalaskes/9.33 [).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash) [Näidis koosneb](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskaaldokumendi pakkujast, mis on Commerce'i käitusaja CRT () laiendus, ja fiskaalse konnektori, mis on Commerce'i riistvarajaama laiendus. Lisateavet jaemüügi SDK kasutamise kohta leiate teemast [Retail SDK arhitektuur](../dev-itpro/retail-sdk/retail-sdk-overview.md) ja [Sõltumatu pakendiga SDK](../dev-itpro/build-pipeline.md) ehitustorustiku seadistamine.

> [!WARNING]
> Uue sõltumatu pakendi- [ja laiendusmudeli](../dev-itpro/build-pipeline.md) piirangute tõttu ei saa seda praegu selle fiskaalse integratsiooni valimi jaoks kasutada. Peate kasutama Retail SDK eelmist versiooni arendaja virtuaalses masinas (VM) elutsükli teenustes Microsoft Dynamics (LCS). Lisateavet vt [rootsi juhtüksuse integratsioonivalimi juurutusjuhistest (pärand)](emea-swe-fi-sample-sdk.md).
>
> Eelarveintegratsiooni näidiste uue sõltumatu pakendi- ja laiendusmudeli toetamine on kavandatud hilisematele versioonidele.

Täitke fiskaalintegratsiooni häälestusetapid, nagu on kirjeldatud jaotises [Commerce'i kanalite](setting-up-fiscal-integration-for-retail-channel.md) fiskaalintegratsiooni häälestamine.

1. [Saate häälestada finantsregistreerimise protsessi](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Samuti märkige selle juhtüksuse integratsioonivalimile [omased finantsregistreerimise protsessi](#set-up-the-registration-process) sätted.
1. [Saate määrata tõrkekäsitluse sätted](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Lubage edasilükatud finantsregistreerimise käsitsi käivitamine](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Kanali komponentide](#configure-channel-components) konfigureerimine.

### <a name="set-up-the-registration-process"></a>Registreerimisprotsessi häälestamine

Registreerimisprotsessi lubamiseks järgige Commerce'i peakontori seadistamiseks neid juhiseid. Lisateavet vt teemast [Fiscal Integration for Commerce channels](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process) häälestamine.

1. Laadige alla rahandusdokumendi pakkuja ja fiskaalse konnektori konfiguratsioonifailid.

    1. Avage lahenduste [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) hoidla.
    1. Valige õige väljalaskeharu versioon vastavalt oma SDK/rakenduse versioonile (nt **[release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Avage **src \> FiscalIntegration \> CleanCash**.
    1. Laadige alla rahandusdokumendi pakkuja konfiguratsioonifail aadressil CommerceRuntime DocumentProvider.CleanCashSample Configuration DocumentProviderFiscalCleanCashSample.xml **(nt \> väljalaskefail/9.33 \>).\>**[...](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/CommerceRuntime/DocumentProvider.CleanCashSample/Configuration/DocumentProviderFiscalCleanCashSample.xml)
    1. Laadige fiskaalse konnektori konfiguratsioonifail alla aadressil **HardwareStation \> Connector.CleanCashSample \> Configuration \> ConnectorCleanCashSample.xml** (näiteks [väljalaskefail/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/HardwareStation/Connector.CleanCashSample/Configuration/ConnectorCleanCashSample.xml)).

    > [!WARNING]
    > Uue sõltumatu pakendi- [ja laiendusmudeli](../dev-itpro/build-pipeline.md) piirangute tõttu ei saa seda praegu selle fiskaalse integratsiooni valimi jaoks kasutada. Peate kasutama Retail SDK eelmist versiooni arendaja VM-is LCS-is. Selle fiskaalse integratsiooni näidise konfiguratsioonifailid asuvad LCS-i arendaja VM-i jaemüügi SDK järgmistes kaustades.
    >
    > - **Fiskaaldokumendi pakkuja konfiguratsioonifail:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.CleanCashSample\\Configuration\\DocumentProviderFiscalCleanCashSample.xml
    > - **Fiscal connectori konfiguratsioonifail:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.CleanCashSample\\Configuration\\ConnectorCleanCashSample.xml
    > 
    > Eelarveintegratsiooni näidiste uue sõltumatu pakendi- ja laiendusmudeli toetamine on kavandatud hilisematele versioonidele.

1. Valige suvandid **Jaemüük ja kaubandus \> Headquartersi häälestus \> Parameetrid \> Commerce’i ühiskasutuses parameetrid**. peal **Kindral** vahekaardil määrake **Luba maksuintegratsioon** võimalus **Jah**.
1. Minema **Jaemüük ja kaubandus \> Kanali seadistamine \> Fiskaalne integratsioon \> Maksudokumentide pakkujad** ja laadige varem alla laaditud maksudokumendi pakkuja konfiguratsioonifail.
1. Minema **Jaemüük ja kaubandus \> Kanali seadistamine \> Fiskaalne integratsioon \> Fiskaalühendused** ja laadige varem alla laaditud fiskaalse konnektori konfiguratsioonifail.
1. Minema **Jaemüük ja kaubandus \> Kanali seadistamine \> Fiskaalne integratsioon \> Konnektori funktsionaalsed profiilid**. Looge uus konnektori funktsionaalne profiil. Valige dokumendipakkuja ja varem laaditud konnektor. Värskendage andmete vastendamise [sätteid](#default-data-mapping) vastavalt vajadusele.
1. Minema **Jaemüük ja kaubandus \> Kanali seadistamine \> Fiskaalne integratsioon \> Konnektori tehnilised profiilid**. Looge uus konnektori tehniline profiil ja valige varem laaditud fiskaalkonnektor. Värskendage [konnektori sätteid](#fiscal-connector-settings) vastavalt vajadusele.
6. **Avage jaemüügi- ja kaubanduskanali \> häälestus \> Fiskaalintegratsioon \> Fiskaalkonnektorigrupid**. Looge varem loodud konnektori funktsionaalse profiili jaoks uus fiskaalse konnektori rühm.
7. Minema **Jaemüük ja kaubandus \> Kanali seadistamine \> Fiskaalne integratsioon \> Fiskaalsed registreerimise protsessid**. Looge uus maksuregistreerimisprotsess ja fiskaalse registreerimise protsessi etapp ning valige varem loodud maksuühenduse rühm.
8. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassaprofiilid \> Funktsiooniprofiilid**. Valige funktsiooniprofiil, mis on lingitud poega, kus registreerimisprotsess tuleks aktiveerida. peal **Maksustamise registreerimise protsess** FastTab, valige varem loodud maksuregistreerimisprotsess.
9. Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Kassaprofiilid \> Riistvaraprofiilid**. Valige riistvaraprofiil, mis on lingitud riistvarajaamaga, millega fiskaalprinter ühendatakse. Valige kiirkaardil **Fiskaalsed välisseadmed** varem loodud konnektori tehniline profiil.
10. Avage jaotusgraafik (**jae- ja kaubandus \> - ja kaubandus-kaubanduse IT-jaotuse \> ajakava**) ning valige tööd **1070** ja **1090**, et edastada andmeid kanali andmebaasi.

#### <a name="default-data-mapping"></a>Andmete vaikevastendus

Rahandusdokumendi pakkuja konfiguratsioonis, mis on esitatud fiskaalse integratsiooni valimi osana, kaasatakse järgmine andmete vaikevastendus.

- **Käibemaksukoodi vastendamine** – see vastendab seadmepõhised käibemaksukoodid vastavatele käibemaksukoodidele. KM-koodi vastendusel peaks olema järgmine vorming.

    ```
    1 : code1 ; 2 : code2
    ```

    Siin on selle vormingu kohta selgitus.

    - *1* ja *2* on seadmepõhised KÄIBEMAKSUkoodid.
    - Semikoolon (;) Kasutatakse eraldajana.
    - *code1* ja *code2* on käibemaksukoodid, mis on konfigureeritud Commerce'i peakontoris. Näidisvastendust tuleb muuta vastavalt rakenduses konfigureeritud maksukoodidele.

    Juhtüksused toetavad kuni nelja erinevat KM-koodi. Seetõttu võib KM-koodi vastenduse seadistada järgmiselt.

    ```
    1 : code1 ; 2 : code2 ; 3 : code3 ; 4 : code4
    ```

    > [!NOTE]
    > Sama seadmepõhise KM-koodiga saab vasteda mitu käibemaksukoodi.

#### <a name="fiscal-connector-settings"></a>Fiskaalse konnektori sätted

Fiskaalse konnektori konfiguratsiooni kuuluvad järgmised sätted, mis on esitatud fiskaalse integratsiooni valimi osana.

- **Ühenduste string** – Juhtseadme ühenduse seaded.
- **Aeg maha** – Aeg millisekundites, mille jooksul juht ootab juhtseadme vastust.

### <a name="configure-channel-components"></a>Kanali komponentide seadistamine

> [!WARNING]
> Uue sõltumatu pakendi- [ja laiendusmudeli](../dev-itpro/build-pipeline.md) piirangute tõttu ei saa seda praegu selle fiskaalse integratsiooni valimi jaoks kasutada. Peate kasutama Retail SDK eelmist versiooni arendaja VM-is LCS-is. Lisateavet vt [rootsi juhtüksuse integratsioonivalimi juurutusjuhistest (pärand)](emea-swe-fi-sample-sdk.md).
>
> Eelarveintegratsiooni näidiste uue sõltumatu pakendi- ja laiendusmudeli toetamine on kavandatud hilisematele versioonidele.

#### <a name="set-up-the-development-environment"></a>Seadistage arenduskeskkond

Näidise testimiseks ja laiendamiseks arenduskeskkonna seadistamiseks toimige järgmiselt.

1. Kloonige või laadige alla [Dynamics 365 Commerce Lahendused](https://github.com/microsoft/Dynamics365Commerce.Solutions) hoidla. Valige õige väljalaske haru versioon vastavalt oma SDK/rakenduse versioonile. Lisateabe saamiseks vt [Laadige alla jaemüügi SDK näidised ja viitepaketid GitHubist ja NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Avage juhtüksuse integreerimise lahendus aadressil **Dynamics365Commerce.Solutions\\FiscalIntegration\\CleanCash\\CleanCash.sln** ja ehitage see.
1. Installige CRT laiendused:

    1. Otsige üles CRT laienduse paigaldaja:

        - **Kaubanduse skaala üksus: leidke kaustast** **CleanCash\\ScaleUnit\\ScaleUnit.CleanCash.Installer\\bin\\Debug\\net461** installer **ScaleUnit.CleanCash.Installer**. 
        - **Kohalik CRT kaasaegses kassas:** kaustas **CleanCash\\ModernPOS\\ModernPOS.CleanCash.Installer\\bin\\Debug\\net461** leidke **modernpos.CleanCash.Installer** installer.

    2. Alustage CRT laienduse installija käsurealt:

        - **Kaubanduse mastaabiüksus:**

            ```Console
            ScaleUnit.CleanCash.Installer.exe install --verbosity 0
            ```

        - **Kohalik CRT kaasaegses POS-is:**

            ```Console
            ModernPOS.CleanCash.Installer.exe install --verbosity 0
            ```

1. Installige riistvarajaama laiendused:

    1. Otsige kaustast **CleanCash\\HardwareStation\\HardwareStation.CleanCash.Installer\\bin\\Debug\\net461** üles **installer HardwareStation.CleanCash.Installer.**
    1. Käivitage laienduse installija käsurealt:

        ```Console
        HardwareStation.CleanCash.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Tootmiskeskkond

Järgige juhiseid [Seadistage fiskaalintegratsiooni näidise jaoks ehituskonveier](fiscal-integration-sample-build-pipeline.md) luua ja vabastada Cloud Scale Unit ja iseteenindusega juurutatavad paketid fiskaalintegratsiooni näidise jaoks. **CleanCashi build-pipeline.yml** malli YAML-faili leiate **lahenduste\\ hoidla kaustast** Pipeline [Dynamics 365 Commerce YAML_Files](https://github.com/microsoft/Dynamics365Commerce.Solutions).

## <a name="design-of-the-extensions"></a>Laienduste kujundus

Rootsi juhtüksuse integreerimise näidis põhineb fiskaalintegratsiooni [funktsioonil](fiscal-integration-for-retail-channel.md) ja on osa jaemüügi SDK-st. Proov asub lahenduste hoidla kaustas **src\\FiscalIntegration\\CleanCash** [Dynamics 365 Commerce (näiteks](https://github.com/microsoft/Dynamics365Commerce.Solutions/) proov väljalaskes/9.33 [).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash) Näidis [koosneb](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskaaldokumentide pakkuja, mis on laiendus CRT ja fiskaalne pistik, mis on Commerce Hardware Stationi laiendus. Lisateavet jaemüügi SDK kasutamise kohta leiate teemast [Retail SDK arhitektuur](../dev-itpro/retail-sdk/retail-sdk-overview.md) ja [Sõltumatu pakendiga SDK](../dev-itpro/build-pipeline.md) ehitustorustiku seadistamine.

> [!WARNING]
> Uue sõltumatu pakendi- [ja laiendusmudeli](../dev-itpro/build-pipeline.md) piirangute tõttu ei saa seda praegu selle fiskaalse integratsiooni valimi jaoks kasutada. Peate kasutama Retail SDK eelmist versiooni arendaja VM-is LCS-is. Lisateavet vt [rootsi juhtüksuse integratsioonivalimi juurutusjuhistest (pärand)](emea-swe-fi-sample-sdk.md). Eelarveintegratsiooni näidiste uue sõltumatu pakendi- ja laiendusmudeli toetamine on kavandatud hilisematele versioonidele.

### <a name="crt-extension-design"></a>CRT laienduse disain

Finantsdokumendi pakkuja laienduse eesmärk on luua teenusepõhiseid dokumente ja käsitleda juhtüksuse vastuseid.

#### <a name="request-handler"></a>Taotluse käitleja

Dokumendipakkuja jaoks on üks **documentProviderCleanCashi** päringukäsitleja. Seda käitlejat kasutatakse juhtseadmele rahandusdokumentide loomiseks.

See töötleja on päritud **INamedRequestHandler** liides. **Käitleja nime tagastamise eest vastutab meetod HandlerName**. Käitleja nimi peaks vastama Commerce'i peakontoris määratud konnektori dokumendipakkuja nimele.

Konnektor toetab järgmisi taotlusi.

- **GetFiscalDocumentDocumentProviderRequest** – see taotlus sisaldab teavet selle kohta, milline dokument tuleks luua. See tagastab teenusepõhise dokumendi, mis tuleks juhtseadmes registreerida.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – See päring tagastab tellitavate sündmuste loendi. Praegu toetatakse müügiüritusi ja auditiüritusi.

#### <a name="configuration"></a>Konfiguratsioon

Rahandusdokumendi pakkuja konfiguratsioonifail asub aadressil **src\\FiscalIntegration\\CleanCash\\CommerceRuntime\\DocumentProvider.CleanCashSample\\Configuration\\DocumentProviderFiscalCleanCashSample.xml** lahenduste [Dynamics 365 Commerce hoidlas.](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Selle faili eesmärk on lubada dokumendipakkuja sätete konfigureerimine Commerce'i peakontorist. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetega.

### <a name="hardware-station-extension-design"></a>Riistvarajaama laienduse disain

Fiskaalse konnektori laienduse eesmärk on suhelda juhtseadmega. See kasutab HTTP-protokolli, et esitada juhtseadmele dokumente, mille CRT laiendus loob. Samuti tegeleb see juhtseadmelt saadud vastustega.

#### <a name="request-handler"></a>Taotluse käitleja

**CleanCashHandleri** päringukäitleja on juhtseadmele esitatud taotluste käsitlemise sisenemispunkt.

Käitleja on päritud **INamedRequestHandler** liides. **Käitleja nime tagastamise eest vastutab meetod HandlerName**. Töötleja nimi peaks ühtima fiskaalse konnektori nimega, mis on määratud Commerce'i peakorteris.

Konnektor toetab järgmisi taotlusi.

- **SubmitDocumentFiscalDeviceRequest** – See päring saadab dokumendid juhtplokile ja tagastab sealt vastuse.
- **IsReadyFiscalDeviceRequest** – Seda päringut kasutatakse juhtploki tervisekontrolliks.
- **InitializeFiscalDeviceRequest** – Seda päringut kasutatakse juhtseadme lähtestamiseks.

#### <a name="configuration"></a>Konfiguratsioon

Fiskaalse konnektori konfiguratsioonifail asub aadressil **src\\ Fiskaalintegratsioon\\ CleanCash\\ Riistvarajaam\\ Connector.CleanCashSample\\ Seadistamine\\ ConnectorCleanCashSample.xml** aastal [Dynamics 365 Commerce Lahendused](https://github.com/microsoft/Dynamics365Commerce.Solutions/) hoidla. Faili eesmärk on lubada fiskaalse konnektori sätteid Commerce'i peakorteris konfigureerida. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetega.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
