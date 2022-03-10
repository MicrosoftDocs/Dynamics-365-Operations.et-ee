---
title: Fiskaalprinteri integratsiooni näide Poola jaoks
description: Selles teemas antakse ülevaade Poola eelarveintegratsiooni proovist Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-2-1
ms.openlocfilehash: 43d9a54334d97a65a1f9a356daf54154f6c069b3
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2022
ms.locfileid: "8076832"
---
# <a name="fiscal-printer-integration-sample-for-poland"></a>Fiskaalprinteri integratsiooni näide Poola jaoks

[!include[banner](../includes/banner.md)]

Selles teemas antakse ülevaade Poola eelarveintegratsiooni proovist Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce Poola funktsionaalsus hõlmab müügikoha näidisintegratsiooni fiskaalprinteriga. Proov laiendab fiskaalseintegratsiooni [funktsionaalsust](fiscal-integration-for-retail-channel.md) ja toetab Posnet Polska S.A. fiskaalprinterite protokolli [POSNET THERMAL HD 2.02.](https://www.posnet.com.pl) Proov võimaldab suhelda fiskaalprinteriga, mis on ühendatud COM-porti kaudu, kasutades kohalikku tarkvaradraivereid. Seda rakendati ja testiti tarkvara emulaatori abil, mille Posnet pakkus Posnet Thermal HD FV EJ fiskaalprinterile. Proov on esitatud lähtekoodi kujul ja see on osa jaemüügi tarkvaraarenduskomplektist (SDK).

Microsoft ei väljasta Posnetist ühtegi riist-, tarkvara ega dokumentatsiooni. Lisateavet fiskaalprinteri hankimise ja käitamise kohta võtke ühendust [Posnet Polska S.A.-ga.](https://www.posnet.com.pl)

## <a name="scenarios"></a>Stsenaariumid

Poola fiskaalprinterite integratsioonivalim hõlmab järgmisi stsenaariume.

- Müügistsenaariumid:

    - Saate printida kassa- ja müügi- ja tagastustarne.
    - Jäädvustage fiskaalprinteri vastus ja salvestage see kanali andmebaasi.
    - Maksud:

        - Vastendage fiskaalprinteri maksukoodidega (osakondadega).
        - Saate vastendusega maksuandmed finantsprinterisse üle kanda.

    - Maksed:

        - Vastendage fiskaalprinteri makseviisidega.
        - Saate printida maksed finantskviitungile.
        - Saate printida muudatuste teabe.

    - Saate printida rea hinnaalandid.
    - Kinkekaardid:

        - Välista väljastatud/uuesti laetud kinkekaardi rida müügi finantskviitungilt.
        - Prindi makse, mis kasutab kinkekaarti tavalise makseviisina.

    - Saate printida klienditellimuse toimingute finantstarned.

        - Klienditellimuse deposiidi jaoks pole finantskviitungit prinditud.
        - Saate printida hübriidklienditellimuse tarneridade finantstarne.
        - Saate printida klienditellimuse pealevõtmistoimingu finantstšeki.
        - Saate printida tagastustellimuse finantstarne.

    - [Saate printida finantskviitungile müügikande jaoks määratud klienditeabe](emea-pol-customer-information.md). Selle teabe näiteks on kliendi KM-number.

- Päevalõpuaruanded (X- ja eelarve Z-eelarvearuanded).
- Tõrkekäsitlus ( nt järgmised suvandid)

    - Kui fiskaalprinter pole ühendatud, pole valmis või ei reageeri, printer on paberist väljas või on paberimoosi.
    - Lükake finantsregistreerimine edasi.
    - Jätke finantsregistreerimine vahele või märkige kanne registreerituks ning lisage tõrke põhjuse ja lisateabe jäädvustamiseks infokoodid.
    - Kontrollige fiskaalprinteri saadavust enne uue müügikande avamist või müügikande lõpuleviimist.

### <a name="gift-cards"></a>Kinkekaardid

Fiskaalprinteri integratsiooni näidis rakendab järgmisi kinkekaartidega seotud reegleid.

- Välista finantskviitungilt müügiread, mis on seotud *kinkekaardiGa* Väljasta ja *Lisa kinkekaardi* toimingutesse.
- Ärge printige finantskviitungit, kui see koosneb ainult kinkekaardi ridadest.
- Lahutage finantskviitungi makseridadelt kandes väljastatud või uuesti laetud kinkekaartide kogusumma.
- Salvestage kanaliandmebaasi makseridade arvutatud korrigeerimised viitega vastavale finantskandele.
- Kinkekaardiga maksmist loetakse regulaarseks makseks.

### <a name="customer-deposits-and-customer-order-deposits"></a>Kliendihoiused ja klienditellimuse hoiused

Fiskaalprinteri integratsiooninäidis rakendab järgmisi reegleid, mis on seotud kliendihoiuste ja klienditellimuse hoiustega.

- Ärge printige finantskviitungit, kui kanne on kliendihoius.
- Ärge printige finantskviitungit, kui kanne sisaldab ainult klienditellimuse deposiiti või klienditellimuse deposiidi tagasimakset.
- Saate printida klienditellimuse pealevõtmistoimingu finantstarnele varem tasutud deposiidi summa.
- Hübriidkliendi tellimuse loomisel lahutage klienditellimuse deposiidi summa makseridadelt.
- Salvestage kanaliandmebaasi makseridade arvutatud korrigeerimised viitega hübriidklienditellimuse finantskandele.

### <a name="limitations-of-the-sample"></a>Proovi piirangud

- Fiskaalprinter toetab ainult stsenaariume, kus hinnas sisaldub käibemaks. Seetõttu **peab hinnas sisaldatav käibemaksusuvand** olema seatud **nii kaupluste kui ka klientide jaoks jah**.
- Igapäevased aruanded (rahandus X ja fiskaalne Z) prinditakse manustatud *Shifti aruandevormingu* abil.
- Vöötkoodi printimist fiskaalkviitungitele peetakse potentsiaalseks kohandamiseks, kuna seda funktsiooni ei toetata manustatud vormingutes ja seda saab rakendada ainult kohandatava **Super-vormingu** aruande abil.
- Fiskaalprinter ei toeta segakandeid. Suvand **Keela müügi ja tagastuste segamine ühes kviitungis** peaks olema seatud väärtusele **Jah** kassa funktsioonide profiilides.

## <a name="set-up-fiscal-integration-for-poland"></a>Poola fiskaalintegratsiooni häälestamine

Poola fiskaalprinterite integreerimise näidis põhineb fiskaalintegratsiooni [funktsioonil](fiscal-integration-for-retail-channel.md) ja on osa retail SDK-st. Proov asub lahenduste hoidla kaustas **src\\FiscalIntegration\\Posnet** [Dynamics 365 Commerce (näiteks](https://github.com/microsoft/Dynamics365Commerce.Solutions/) proov väljalaskes/9.33 [).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Posnet) [Näidis koosneb](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskaaldokumendi pakkujast, mis on Commerce'i käitusaja CRT () laiendus, ja fiskaalse konnektori, mis on Commerce'i riistvarajaama laiendus. Lisateavet jaemüügi SDK kasutamise kohta leiate teemast [Retail SDK arhitektuur](../dev-itpro/retail-sdk/retail-sdk-overview.md) ja [Sõltumatu pakendiga SDK](../dev-itpro/build-pipeline.md) ehitustorustiku seadistamine.

> [!WARNING]
> Uue sõltumatu pakendi- [ja laiendusmudeli](../dev-itpro/build-pipeline.md) piirangute tõttu ei saa seda praegu selle fiskaalse integratsiooni valimi jaoks kasutada. Peate kasutama Retail SDK eelmist versiooni arendaja virtuaalses masinas (VM) elutsükli teenustes Microsoft Dynamics (LCS). Lisateavet vt [teemast Juurutamisjuhised poola eelarveprinteri integratsiooni näidise jaoks (pärand)](emea-pol-fpi-sample-sdk.md).
>
> Eelarveintegratsiooni näidiste uue sõltumatu pakendi- ja laiendusmudeli toetamine on kavandatud hilisematele versioonidele.

Täitke fiskaalintegratsiooni häälestusetapid, nagu on kirjeldatud jaotises [Commerce'i kanalite](setting-up-fiscal-integration-for-retail-channel.md) fiskaalintegratsiooni häälestamine.

1. [Saate häälestada finantsregistreerimise protsessi](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Samuti märkige ära finantsregistreerimise protsessi sätted, mis on selle fiskaalprinteri integratsioonivalimi jaoks [spetsiifilised](#set-up-the-registration-process).
1. [Saate määrata tõrkekäsitluse sätted](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Saate kassast häälestada X/Z-fiskaalaruandeid](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
1. [Lubage edasilükatud finantsregistreerimise käsitsi käivitamine](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Kanali komponentide](#configure-channel-components) konfigureerimine.

### <a name="set-up-the-registration-process"></a>Registreerimisprotsessi häälestamine

Registreerimisprotsessi lubamiseks järgige Commerce'i peakontori seadistamiseks neid juhiseid. Lisateavet vt teemast [Fiscal Integration for Commerce channels](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process) häälestamine.

1. Laadige alla rahandusdokumendi pakkuja ja fiskaalse konnektori konfiguratsioonifailid.

    1. Avage lahenduste [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) hoidla.
    1. Valige õige väljalaskeharu versioon vastavalt oma SDK/rakenduse versioonile (nt **[release/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Avage **src \> FiscalIntegration \> Posnet**.
    1. Laadige alla rahandusdokumendi pakkuja konfiguratsioonifail aadressil CommerceRuntime DocumentProvider.PosnetSample **Configuration \> DocumentProviderPosnetSample.xml \> (nt \> väljalaskefail/9.33**[).](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Posnet/CommerceRuntime/DocumentProvider.PosnetSample/Configuration/DocumentProviderPosnetSample.xml)
    1. Laadige fiskaalse konnektori konfiguratsioonifail alla aadressil HardwareStation ThermalDeviceSample **Configuration \> ConnectorPosnetThermalFVEJ.xml \> (näiteks \> väljalaskefail/9.33**).[...](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Posnet/HardwareStation/ThermalDeviceSample/Configuration/ConnectorPosnetThermalFVEJ.xml)

    > [!WARNING]
    > Uue sõltumatu pakendi- [ja laiendusmudeli](../dev-itpro/build-pipeline.md) piirangute tõttu ei saa seda praegu selle fiskaalse integratsiooni valimi jaoks kasutada. Peate kasutama Retail SDK eelmist versiooni arendaja VM-is LCS-is. Selle fiskaalse integratsiooni näidise konfiguratsioonifailid asuvad LCS-i arendaja VM-i jaemüügi SDK järgmistes kaustades.
    >
    > - **Fiscal document provider configuration file:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extension.DocumentProvider.PosnetSample\\Configuration\\DocumentProviderPosnetSample.xml
    > - **Fiscal connectori konfiguratsioonifail:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.Posnet.ThermalDeviceSample\\Configuration\\ConnectorPosnetThermalFVEJ.xml
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

- **Käibemaksumäärade vastendamine** – käibemaksukoodide jaoks fiskaalprinterile seadistatud maksuprotsendi väärtuste vastendamine fiskaalprinteri spetsiifilistele KM-määradele. Siin on vaikevastendus.

    ```
    0 : 23.00 ; 1 : 8.00 ; 2 : 5.00 ; 3 : 0.00
    ```

    Iga paari esimene komponent tähistab km määra numbrit, mis on konfigureeritud fiskaalprinteris. Teine komponent tähistab vastavat KÄIBEMAKSUmäära. Lisateavet fiskaalprinteri KM määra konfiguratsiooni kohta leiate POSNETi draiveri dokumentatsioonist.

- **Maksevahendi tüübi vastendamine** – kaupluse jaoks konfigureeritud makseviiside vastendamine maksevormidele, mida toetab fiskaalprinter. Siin on vaikevastendus.

    ```
    0 : 0 ; 1 : 0 ; 2 : 2 ; 3 : 2 ; 4 : 0 ; 5 : 0 ; 6 : 0 ; 7 : 2 ; 8 : 0
    ```

    Iga paari esimene komponent tähistab kaupluse jaoks seadistatud makseviisi. Teine komponent tähistab vastavat maksevormi, mida toetab fiskaalprinter. Lisateavet fiskaalprinteri toetatavate maksevormide kohta leiate POSNETi draiveri dokumentatsioonist. Näidisvastendust tuleb muuta vastavalt rakenduses konfigureeritud makseviisile.

#### <a name="fiscal-connector-settings"></a>Fiskaalse konnektori sätted

Fiskaalse konnektori konfiguratsiooni kuuluvad järgmised sätted, mis on esitatud fiskaalse integratsiooni valimi osana.

- **Ühendusstring** – string, mis kirjeldab seadmega ühenduse üksikasju vormingus, mida draiver toetab. Lisateavet leiate POSNETi draiveri dokumentatsioonist.
- **Kuupäeva ja kellaaja sünkroonimine** – Väärtus, mis määrab, kas printeri kuupäev ja kellaaeg tuleb ühendatud riistvarajaamaga sünkroonida.
- **Seadme ajalõpp** – Aeg millisekundites, mille jooksul juht ootab seadmelt vastust. Lisateavet leiate POSNETi draiveri dokumentatsioonist.

### <a name="configure-channel-components"></a>Kanali komponentide seadistamine

> [!WARNING]
> Uue sõltumatu pakendi- [ja laiendusmudeli](../dev-itpro/build-pipeline.md) piirangute tõttu ei saa seda praegu selle fiskaalse integratsiooni valimi jaoks kasutada. Peate kasutama Retail SDK eelmist versiooni arendaja VM-is LCS-is. Lisateavet vt [teemast Juurutamisjuhised poola eelarveprinteri integratsiooni näidise jaoks (pärand)](emea-pol-fpi-sample-sdk.md).
>
> Eelarveintegratsiooni näidiste uue sõltumatu pakendi- ja laiendusmudeli toetamine on kavandatud hilisematele versioonidele.

#### <a name="set-up-the-development-environment"></a>Seadistage arenduskeskkond

Näidise testimiseks ja laiendamiseks arenduskeskkonna seadistamiseks toimige järgmiselt.

1. Kloonige või laadige alla [Dynamics 365 Commerce Lahendused](https://github.com/microsoft/Dynamics365Commerce.Solutions) hoidla. Valige õige väljalaske haru versioon vastavalt oma SDK/rakenduse versioonile. Lisateabe saamiseks vt [Laadige alla jaemüügi SDK näidised ja viitepaketid GitHubist ja NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Avage fiskaalprinteri integreerimislahendus aadressil **Dynamics365Commerce.Solutions\\ Fiskaalintegratsioon\\ Posnet\\ Posnet.sln** ja ehitage see üles.
1. Installige CRT laiendused:

    1. Otsige üles CRT laienduse paigaldaja:

        - **Kaubanduse mastaabiüksus:** Aastal **Posnet\\ Skaalaühik\\ ScaleUnit.Posnet.Installer\\ prügikast\\ Silumine\\ net461** kaust, otsige üles **ScaleUnit.Posnet.Installer** paigaldaja.
        - **Kohalik CRT kaasaegses POS-is:** Aastal **Posnet\\ Kaasaegne POS\\ ModernPOS.Posnet.Installer\\ prügikast\\ Silumine\\ net461** kaust, otsige üles **ModernPOS.Posnet.Installer** paigaldaja.

    1. Alustage CRT laienduse installija käsurealt:

        - **Kaubanduse mastaabiüksus:**

            ```Console
            ScaleUnit.Posnet.Installer.exe install --verbosity 0
            ```

        - **Kohalik CRT kaasaegses POS-is:**

            ```Console
            ModernPOS.Posnet.Installer.exe install --verbosity 0
            ```

1. Installige riistvarajaama laiendused:

    1. Aastal **Posnet\\ Riistvarajaam\\ HardwareStation.PosnetThermalFVFiscalPrinter.Installer\\ prügikast\\ Silumine\\ net461** kaust, otsige üles **HardwareStation.PosnetThermalFVFiscalPrinter.Installer** paigaldaja.
    1. Käivitage laienduse installija käsurealt:

        ```Console
        HardwareStation.PosnetThermalFVFiscalPrinter.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Tootmiskeskkond

Järgige juhiseid [Seadistage fiskaalintegratsiooni näidise jaoks ehituskonveier](fiscal-integration-sample-build-pipeline.md) luua ja vabastada Cloud Scale Unit ja iseteenindusega juurutatavad paketid fiskaalintegratsiooni näidise jaoks. The **Posnet build-pipeline.yml** malli YAML-faili leiate **Torujuhe\\ YAML_Files** kaust [Dynamics 365 Commerce Lahendused](https://github.com/microsoft/Dynamics365Commerce.Solutions) hoidla.

## <a name="design-of-extensions"></a>Laienduste kujundus

Poola fiskaalprinterite integreerimise näidis põhineb fiskaalintegratsiooni [funktsioonil](fiscal-integration-for-retail-channel.md) ja on osa retail SDK-st. Proov asub **src\\FiscalIntegration\\Posnet** [Dynamics 365 Commerce (näiteks](https://github.com/microsoft/Dynamics365Commerce.Solutions/) proov väljalaskes/9.33 [).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Posnet) Näidis [koosneb](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskaaldokumentide pakkuja, mis on laiendus CRT ja fiskaalne pistik, mis on Commerce Hardware Stationi laiendus. Lisateavet jaemüügi SDK kasutamise kohta leiate teemast [Retail SDK arhitektuur](../dev-itpro/retail-sdk/retail-sdk-overview.md) ja [Sõltumatu pakendiga SDK](../dev-itpro/build-pipeline.md) ehitustorustiku seadistamine.

> [!WARNING]
> Uue sõltumatu pakendi- [ja laiendusmudeli](../dev-itpro/build-pipeline.md) piirangute tõttu ei saa seda praegu selle fiskaalse integratsiooni valimi jaoks kasutada. Peate kasutama Retail SDK eelmist versiooni arendaja VM-is LCS-is. Lisateavet vt [teemast Juurutamisjuhised poola eelarveprinteri integratsiooni näidise jaoks (pärand)](emea-pol-fpi-sample-sdk.md). Eelarveintegratsiooni näidiste uue sõltumatu pakendi- ja laiendusmudeli toetamine on kavandatud hilisematele versioonidele.

### <a name="commerce-runtime-extension-design"></a>Commerce'i käitusaja laienduse kujundus

Maksudokumentide pakkuja laienduse eesmärk on luua printeripõhiseid dokumente ja käsitleda fiskaalprinteri vastuseid. See laiendus loob printerispetsiifiliste käskude komplekti JavaScript Object Notation (JSON) vormingus, mis on määratletud POSNETi spetsifikatsiooniga 19-3678.

#### <a name="request-handler"></a>Taotluse käitleja

The **DocumentProviderPosnetProtocol** päringu töötleja on maksuprinterist dokumentide genereerimise päringu sisenemispunkt.

Käitleja on päritud **INamedRequestHandler** liides. **Käitleja nime tagastamise eest vastutab meetod HandlerName**. Käitleja nimi peaks vastama Commerce'i peakontoris määratud konnektori dokumendipakkuja nimele.

Konnektor toetab järgmisi taotlusi.

- **GetFiscalDocumentDocumentProviderRequest** – see taotlus sisaldab teavet selle kohta, milline dokument tuleks luua. See tagastab printerispetsiifilise dokumendi, mis tuleks fiskaalprinteris registreerida.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – See päring tagastab tellitavate sündmuste loendi. Praegu toetatakse järgmisi sündmusi: müük, X-aruande printimine ja Z-aruande printimine.

#### <a name="configuration"></a>Konfiguratsioon

Maksudokumendi pakkuja konfiguratsioonifail asub aadressil **src\\ Fiskaalintegratsioon\\ Posnet\\ CommerceRuntime\\ DocumentProvider.PosnetSample\\ Seadistamine\\ DocumentProviderPosnetSample.xml** aastal [Dynamics 365 Commerce Lahendused](https://github.com/microsoft/Dynamics365Commerce.Solutions/) hoidla. Faili eesmärk on võimaldada fiskaaldokumentide pakkuja seadeid konfigureerida Commerce'i peakorteris. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetega.

### <a name="hardware-station-extension-design"></a>Riistvarajaama laienduse disain

Fiskaalpistikuks oleva laienduse eesmärk on suhelda fiskaalprinteriga. See laiendus kutsub POSNETi draiveri funktsioone, et edastada käske, mida CRT laiendus genereerib fiskaalprinterile. Samuti käsitleb see seadme vigu.

#### <a name="request-handler"></a>Taotluse käitleja

The **FiscalPrinterHandler** päringu töötleja on sisenemispunkt päringu käsitlemiseks maksuvälisseadmesse.

Käitleja on päritud **INamedRequestHandler** liides. **Käitleja nime tagastamise eest vastutab meetod HandlerName**. Töötleja nimi peaks ühtima fiskaalse konnektori nimega, mis on määratud Commerce'i peakorteris.

Konnektor toetab järgmisi taotlusi.

- **SubmitDocumentFiscalDeviceRequest** – See päring saadab dokumendid printeritele ja tagastab fiskaalprinterilt vastuse.
- **IsReadyFiscalDeviceRequest** – Seda päringut kasutatakse seadme tervisekontrolliks.
- **InitializeFiscalDeviceRequest** – Seda päringut kasutatakse printeri lähtestamiseks.

#### <a name="configuration"></a>Konfiguratsioon

Fiskaalse konnektori konfiguratsioonifail asub aadressil **src\\ Fiskaalintegratsioon\\ Posnet\\ Riistvarajaam\\ ThermalDeviceSample\\ Seadistamine\\ ConnectorPosnetThermalFVEJ.xml** aastal [Dynamics 365 Commerce Lahendused](https://github.com/microsoft/Dynamics365Commerce.Solutions/) hoidla. Faili eesmärk on võimaldada fiskaalühenduse seadete konfigureerimist Commerce'i peakorteris. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetega.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
