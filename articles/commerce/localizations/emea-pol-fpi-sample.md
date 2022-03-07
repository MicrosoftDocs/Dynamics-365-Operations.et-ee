---
title: Fiskaalprinteri integratsiooni näide Poola jaoks
description: Selles teemas antakse ülevaade Poola fiskaalintegratsiooni näidistest Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-2-1
ms.openlocfilehash: 1b3d7d59494b215ae47f710e200e7e0c57e4ca29
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944861"
---
# <a name="fiscal-printer-integration-sample-for-poland"></a>Fiskaalprinteri integratsiooni näide Poola jaoks

[!include[banner](../includes/banner.md)]

Selles teemas antakse ülevaade Poola fiskaalintegratsiooni näidistest Microsoft Dynamics 365 Commerce.

Poola Dynamics 365 Commerce funktsioon hõlmab kassa (POS) näidisintegratsiooni fiskaalprinteriga. Näidis laiendab fiskaalintegratsiooni funktsioone ja toetab [POSNET](fiscal-integration-for-retail-channel.md) HD 2.02 protokolli [Posnet Polska S.A fiskaalprinterite jaoks.](https://www.posnet.com.pl) Näidis võimaldab sidet fiskaalprinteriga, mis on ühendatud COM-pordi kaudu, kasutades ematarkvaradraiverit. See rakendati ja testiti, kasutades Posnetile Posnet Hd HD FV EJ fiskaalprinteri jaoks antud tarkvara emulaatorit. Näidis esitatakse lähtekoodina ja on osa jaemüügi tarkvara arenduskomplektist (SDK).

Microsoft ei vabasta posneti riistvara, tarkvara ega dokumentatsiooni. Lisateabe saamiseks fiskaalprinteri toomiseks ja selle käsitsemiseks võtke ühendust [Posnet Polska S.A-ga.](https://www.posnet.com.pl)

## <a name="scenarios"></a>Stsenaariumid

Järgmisi stsenaariume hõlmab Fiskaalprinteri integreerimisnäide Poola jaoks:

- Müügistsenaariumid:

    - Printige fiskaalsissetulek sularaha ja edasimüügi ning tagastuste jaoks.
    - Fikseerige fiskaalprinteri vastus ja salvestage see kanali andmebaasi.
    - Maksud:

        - Vastendage fiskaalprinteri maksukoodidega (osakonnad).
        - Vastendatud maksuandmete ülekandmine fiskaalprinterisse.

    - Maksed:

        - Vastendage fiskaalprinteri makseviisid.
        - Prindib maksed fiskaalsissetulekutele.
        - Prindib muudatuse teabe.

    - Saate printida rea allahindlused.
    - Kinkekaardid:

        - Välistage müügi fiskaalsissetulekult väljastatud/uuesti küsitud kinkekaardi rida.
        - Printige makse, mis kasutab tavalise makseviisina kinkekaarti.

    - Prindib klienditellimuse toimingute fiskaalsissetulekud:

        - Klienditellimuse deposiidi jaoks ei prindita fiskaalsissetulekit.
        - Printige klienditellimuse tarneridade fiskaalsissetulek.
        - Printige klienditellimuse vastuvõtmise toimingu fiskaalsissetulek.
        - Printige tagastustellimuse fiskaalsissetulek.

    - [Printige](emea-pol-customer-information.md) fiskaalsissetuleku müügikande jaoks määratud klienditeave. Selle teabe näiteks on kliendi KM-kood.

- Päeva lõpetamise laused (fiskaal X- ja fiskaal-Z-aruanded).
- Tõrkekäsitlus, nt järgmised valikud:

    - Kui on võimalik, et fiskaalprinterit saab uuesti registreerida, nt kui fiskaalprinter ei ole ühendatud, ei ole valmis või ei vasta sellele, on printerist paber paber väljas või on paberi jada.
    - Finantsregistreerimise edasilükkamine.
    - Jätte fiskaalregistreerimise vahele või märgite kande registreeritud koodina ja kaasate teabekoodid, et hõivata tõrke põhjus ja lisateave.
    - Kontrollige fiskaalprinteri saadavust enne uue müügikande avamist või müügikande sulgemist.

### <a name="gift-cards"></a>Kinkekaardid

Fiskaalprinteri integreerimise näidis juurutab järgmised kinkekaartidega seotud reeglid:

- Välistage fiskaalsissetuleku kinkekaardi toimingutesse *väljastamise* *kinkekaardiga* seotud müügiread.
- Kui see koosneb ainult kinkekaardi ridadest, siis ärge printige fiskaalkviitungit.
- Lahutage fiskaalsissetuleku makseridadelt kandes väljastatud või uuesti sisse küsitavate kinkekaartide kogusumma.
- Salvestage makseridade arvutatud korrigeerimised kanali andmebaasis viitega vastavale fiskaalkandele.
- Kinkekaardiga maksmine on tavamakse.

### <a name="customer-deposits-and-customer-order-deposits"></a>Kliendi deposiitid ja kliendi tellimuse deposiidid

Fiskaalprinteri integratsiooni näidis juurutab järgmised kliendi deposiitide ja klienditellimuse deposiittega seotud reeglid:

- Ärge printige fiskaalsissetulekit, kui kanne on kliendi deposiit.
- Ärge printige fiskaalsissetulekit, kui kanne sisaldab ainult klienditellimuse deposiiti või klienditellimuse deposiidi tagasimakset.
- Prindib kliendi tellimuse vastuvõtmise toimingu jaoks eelnevalt makstud deposiidi summa fiskaalsissetulekil.
- Klienditellimuse deposiidisumma arvatakse hankija tellimuse loomisel maha makseridadelt.
- Salvestage makseridade arvutatud korrigeerimised kanali andmebaasis viitega klienditellimuse fiskaalkandele.

### <a name="limitations-of-the-sample"></a>Näidiste piirangud

- Fiskaalprinter toetab ainult stsenaariume, kus hind sisaldab käibemaksu. Seetõttu peab nii kaupluste kui ka klientide puhul valik Hind **sisaldama** käibemaksu **väärtuseks** olema seatud Jah.
- Päevaaruanded (rahandus X ja fiskaal Z) prinditakse manustatud vahetuse *aruandevormingu* abil.
- Vöötkoodi printimist fiskaalsissetulekutele peetakse potentsiaalseks kohandamiseks, sest seda funktsiooni ei toetata manustatud vormingutes ja seda saab rakendada ainult kohandatava **ülevorminguaruande** abil.
- Fiskaalprinter ei toeta segatud kandeid. Valik **Keela müügi ja tagastuste segamine ühes kviitungis tuleks kassa funktsiooniprofiilides seada** **väärtusele** Jah.

## <a name="set-up-fiscal-integration-for-poland"></a>Häälestage Poola fiskaalintegratsioon.

Poola fiskaalprinteri integratsiooni näidis põhineb [fiskaalintegratsiooni funktsioonil ja](fiscal-integration-for-retail-channel.md) on osa Jaemüügi SDK-st. Näidis asub lahenduste hoidla **\\ kaustas FiscalIntegration \\ Posnet (nt vabastamisnäide/9.33).**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/)[...](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Posnet) Näidis [koosneb fiskaaldokumendi pakkujast, mis on Commerce Runtime'i () laiendus, ja fiskaalühendusest, mis](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices)CRT on Commerce Hardware Stationi laiendus. Lisateavet Retail SDK kasutamise kohta vt [Retail SDK arhitektuurist](../dev-itpro/retail-sdk/retail-sdk-overview.md) ja [iseseisva pakendamise SDK koostamisvõimaluste häälestamisest](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Uue sõltumatu pakendi- ja laiendusmudeli piirangute tõttu ei saa seda praegu selle [fiskaalintegratsiooni](../dev-itpro/build-pipeline.md) näidise jaoks kasutada. Retail SDK eelmist versiooni peate kasutama arendaja virtuaalmasinas (VM) Microsoft Dynamics elutsükli teenustes (LCS). Lisateavet vt Poola [(pärand) fiskaalprinteri integratsiooni näidise juurutuse juhised](emea-pol-fpi-sample-sdk.md).
>
> Uutesse versioonidesse planeeritakse fiskaalintegratsiooni valimite uue sõltumatu pakendi- ja laiendusmudeli tugi.

Viige finantsintegratsiooni seadistuse etapid lõpule, nagu [on kirjeldatud Ärikanalite fiskaalintegratsiooni seadistamises](setting-up-fiscal-integration-for-retail-channel.md).

1. [Seadistage fiskaalregistreerimise protsess](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Lisaks tehke märkus fiskaalregistreerimise protsessi sätete kohta, mis on sellele [fiskaalprinteri integreerimisnäidsele spetsiifilised](#set-up-the-registration-process).
1. [Tõrke käsitlemise sätete](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings) seadistamine.
1. [Seadistage kassast finants-X/Z-aruanded.](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos)
1. [Luba edasilükatud fiskaalregistreerimise käsitsi](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration) käivitamine.
1. [Kanali komponentide](#configure-channel-components) konfigureerimine.

### <a name="set-up-the-registration-process"></a>Registreerimisprotsessi häälestamine

Registreerimisprotsessi lubamiseks järgige neid samme Commerce headquartersi häälestamiseks. Lisateavet vt Commerce'i [kanalite fiskaalintegratsiooni](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process) häälestamine.

1. Laadige alla finantsdokumendi pakkuja ja fiskaalkonnektori konfiguratsioonifailid:

    1. Lahenduste [Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) hoidla avamine.
    1. Valige õige väljalaske haruversioon vastavalt oma SDK-le/rakenduse versioonile (nt **[vabastamine/9.33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**
    1. Saate **avada src \> FiscalIntegration \> Posneti.**
    1. Laadige alla finantsdokumendi pakkuja **konfiguratsioonifail vormingus CommerceRuntime \> DocumentProvider.PosnetSample \> Configuration \> DocumentProviderPosnetSample.xml (näiteks väljalaske**[fail/9.33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Posnet/CommerceRuntime/DocumentProvider.PosnetSample/Configuration/DocumentProviderPosnetSample.xml)
    1. Laadige alla fiskaalkonnektori **konfiguratsioonifail HardwareStationIstViceSample \> Configuration \>\> ConnectorPosnetThermalFISOLATSIOONI.xml (nt väljalaske**[fail/9.33).](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Posnet/HardwareStation/ThermalDeviceSample/Configuration/ConnectorPosnetThermalFVEJ.xml)

    > [!WARNING]
    > Uue sõltumatu pakendi- ja laiendusmudeli piirangute tõttu ei saa seda praegu selle [fiskaalintegratsiooni](../dev-itpro/build-pipeline.md) näidise jaoks kasutada. Retail SDK eelmist versiooni peate kasutama LCS-i arendaja VM-s. Selle fiskaalintegratsiooni näidiskonfiguratsiooni failid asuvad Retail SDK arendaja VM LCS-i kaustades:
    >
    > - **Fiskaaldokumendi pakkuja konfiguratsioonifail:** RetailSdk \\ SampleExtensions \\ CommerceRuntime \\ Extension.DocumentProvider.PosnetSample \\ Configuration \\ DocumentProviderPosnetSample.xml
    > - **Fiskaalkonnektori** konfiguratsioonifail: RetailSdk \\ SampleExtensions \\ HardwareStation \\ Extension.Posnet.ViceSample \\ Configuration \\ ConnectorPosnetThermalFFS.xml
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

- **Käibemaksumäärade vastendamine käibemaksumääradega – käibemaksukoodide jaoks seadistatud maksuprotsendi väärtuste vastendamine** fiskaalprinterile omaste KM-määradega. Siin on vaikevastendus:

    ```
    0 : 23.00 ; 1 : 8.00 ; 2 : 5.00 ; 3 : 0.00
    ```

    Iga paari esimene komponent tähistab FIskaalprinteris konfigureeritud KM-määra numbrit. Teine komponent esindab vastavat KM-määra. Fiskaalprinteri KM-määra konfiguratsiooni kohta lisateabe saamiseks vt POSNETi draiveri dokumentatsiooni.

- **Maksevahendi tüübi** vastendamine – kaupluse jaoks konfigureeritud makseviiside vastendamine fiskaalprinteri toetatud maksevormidega. Siin on vaikevastendus:

    ```
    0 : 0 ; 1 : 0 ; 2 : 2 ; 3 : 2 ; 4 : 0 ; 5 : 0 ; 6 : 0 ; 7 : 2 ; 8 : 0
    ```

    Iga paari esimene komponent esindab kauplusele seadistatud makseviisi. Teine komponent tähistab vastavat maksevormi, mida toetab fiskaalprinter. Lisateavet maksevormide kohta, mida fiskaalprinter toetab, vt POSNET-i draiveri dokumentatsioonist. Peate muutma näidisvastendust vastavalt maksemeetoditele, mis on teie rakenduses konfigureeritud.

#### <a name="fiscal-connector-settings"></a>Fiskaalühenduse sätted

Järgmised sätted on kaasatud fiskaalkonnektori konfiguratsiooni, mis on antud fiskaalintegratsiooni näidisosana:

- **Ühendusstring** – string, mis kirjeldab seadmega ühenduse üksikasju vormingus, mida draiver toetab. Lisateavet vt POSNET-i draiveri dokumentatsioonist.
- **Kuupäeva ja kellaaja sünkroonimine – väärtus, mis määrab, kas printeri kuupäev ja kellaaeg tuleb** sünkroonida ühendatud riistvarajaamaga.
- **Seadme** ajalõpp – aja hulk millisekundites, mille juht ootab seadmelt vastuse ootamist. Lisateavet vt POSNET-i draiveri dokumentatsioonist.

### <a name="configure-channel-components"></a>Kanali komponentide konfigureerimine

> [!WARNING]
> Uue sõltumatu pakendi- ja laiendusmudeli piirangute tõttu ei saa seda praegu selle [fiskaalintegratsiooni](../dev-itpro/build-pipeline.md) näidise jaoks kasutada. Retail SDK eelmist versiooni peate kasutama LCS-i arendaja VM-s. Lisateavet vt Poola [(pärand) fiskaalprinteri integratsiooni näidise juurutuse juhised](emea-pol-fpi-sample-sdk.md).
>
> Uutesse versioonidesse planeeritakse fiskaalintegratsiooni valimite uue sõltumatu pakendi- ja laiendusmudeli tugi.

#### <a name="set-up-the-development-environment"></a>Saate häälestada arenduskeskkonda.

Arenduskeskkonna katsetada ja näidist laiendada, järgige neid samme.

1. Rakenduste hoidla [Dynamics 365 Commerce leidmine](https://github.com/microsoft/Dynamics365Commerce.Solutions) või allalaadimine. Valige õige väljalaske haruversioon vastavalt oma SDK-le/rakenduse versioonile. Lisateavet vt jaotisest Jaemüügi SDK näidised ja viitepakendid alla laadida [GitHub-st ja NuGet](../dev-itpro/retail-sdk/sdk-github.md).
1. Avage fiskaalprinteri integreerimislahendus **dynamics365Commerce.Solutions \\ FiscalIntegration \\\\ Posnet Posnet.sln** ja koostage see.
1. Installi CRT laiendid:

    1. Leidke laiendi CRT installer:

        - **Commerce Scale Unit: otsige kaustast** **Posnet \\\\ ScaleUnit ScaleUnit.Posnet.Installer \\ bin \\ Debug \\ net461** üles **ScaleUnit.Posnet.Installer.**
        - **Kohalik CRT modern POS-is:** leidke **posnet \\\\ ModernPOS ModernPOS.Posnet.Installeri \\ bin \\ Silumine \\ net461** **kaustast ModernPOS.Posnet.Installer.**

    1. Käivitage CRT laiendiinstall käsurealt:

        - **Commerce Scalei üksus:**

            ```Console
            ScaleUnit.Posnet.Installer.exe install --verbosity 0
            ```

        - **Kohalik CRT Modern POS-s:**

            ```Console
            ModernPOS.Posnet.Installer.exe install --verbosity 0
            ```

1. Riistvarajaama laienduste installimine:

    1. Posnet **\\ HardwareStation \\ HardwareStation.PosnetThermalFVFiscalPrinter.Installeri \\ bin \\ Silumine \\ net461** leidke kaust **HardwareStation.PosnetThermalFVFiscalPrinter.Installer.**
    1. Käivitage laiendiinstall käsurealt:

        ```Console
        HardwareStation.PosnetThermalFVFiscalPrinter.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Tootmiskeskkond

Järgige fiskaalintegratsiooni näidise jaoks koostevõimaluste häälestamise etappe, et luua ja vabastada pilveskaala üksus ja iseteeninduse juurutatavad paketid [fiskaalintegratsiooni](fiscal-integration-sample-build-pipeline.md) näidiskomplekti jaoks. **Posneti build-pipeline.yml malli JAML faili leiate lahenduste** **YAML_Files \\**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions) kaustast Müügivõimalustest.

## <a name="design-of-extensions"></a>Laienduste kujundus

Poola fiskaalprinteri integratsiooni näidis põhineb [fiskaalintegratsiooni funktsioonil ja](fiscal-integration-for-retail-channel.md) on osa Jaemüügi SDK-st. Näidis asub lahenduste hoidla **\\ kaustas FiscalIntegration \\ Posnet (nt vabastamisnäide/9.33).**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/)[...](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Posnet) Näidis [koosneb](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) fiskaaldokumendi pakkujast, mis on CRT laiendiks, ja fiskaalühendusest, mis on Commerce Hardware Stationi laiendus. Lisateavet Retail SDK kasutamise kohta vt [Retail SDK arhitektuurist](../dev-itpro/retail-sdk/retail-sdk-overview.md) ja [iseseisva pakendamise SDK koostamisvõimaluste häälestamisest](../dev-itpro/build-pipeline.md).

> [!WARNING]
> Uue sõltumatu pakendi- ja laiendusmudeli piirangute tõttu ei saa seda praegu selle [fiskaalintegratsiooni](../dev-itpro/build-pipeline.md) näidise jaoks kasutada. Retail SDK eelmist versiooni peate kasutama LCS-i arendaja VM-s. Lisateavet vt Poola [(pärand) fiskaalprinteri integratsiooni näidise juurutuse juhised](emea-pol-fpi-sample-sdk.md). Uutesse versioonidesse planeeritakse fiskaalintegratsiooni valimite uue sõltumatu pakendi- ja laiendusmudeli tugi.

### <a name="commerce-runtime-extension-design"></a>Äri käitusaja laiendi kujundus

Fiskaaldokumendi pakkujaks olemise laiend on luua printeripõhiseid dokumente ja käsitleda fiskaalprinteri vastuseid. See laiend loob Printerispetsiifiliste käskude komplekti JavaScripti objekti notationi (JSON) vormingus, mille on määranud POSNET-i spetsifikatsioon 19-3678.

#### <a name="request-handler"></a>Nõudeohjur

**DocumentProviderPosnetProtocol** taotluseohjur on fiskaalprinterist dokumentide loomise nõude sisenemispunkt.

Ohjur pärineb **INamedRequestHandler** liideselt. Meetod **HandlerName** vastutab ohjuri nime tagastamise eest. Ohjuri nimi peab vastama Commerce Headquartersis määratud konnektori dokumendi pakkuja nimele.

Konnektor toetab järgmisi taotlusi:

- **GetFiscalDocumentDocumentProviderRequest** – see taotlus sisaldab teavet selle kohta, milline dokument tuleks luua. See tagastab printeripõhise dokumendi, mis tuleb registreerida fiskaalprinteris.
- **GetSupportedRegistrableEventsDocumentProviderRequest – see taotlus tagastab** tellitavate sündmuste loendi. Praegu toetatakse järgmisi sündmusi: müük, X-aruande printimine ja Z-aruande printimine.

#### <a name="configuration"></a>Konfiguratsioon

Fiskaaldokumendi pakkuja konfiguratsioonifail asub lahenduste hoidlas **src \\ FiscalIntegration \\ Posnet \\\\ CommerceRuntime DocumentProvider.PosnetSample \\ Configuration \\ DocumentProviderPosnetSample.xml.**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Faili eesmärk on lubada finantsdokumendi pakkuja sätete konfigureerimist rakendusest Commerce headquarters. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetele.

### <a name="hardware-station-extension-design"></a>Riistvarajaama laienduse kujundus

Fiskaalühenduseks olemise laiendi eesmärgiks on side fiskaalprinteriga. See laiend kutsub POSNET-i draiveri funktsioone esitama käske, mida CRT laiend fiskaalprinterile loob. Samuti käsitletakse selles seadme tõrkeid.

#### <a name="request-handler"></a>Nõudeohjur

**FiscalPrinterHandler** taotluseohjur on sisenemispunkt fiskaalseadme perifeerseadme taotluse käsitlemiseks.

Ohjur pärineb **INamedRequestHandler** liideselt. Meetod **HandlerName** vastutab ohjuri nime tagastamise eest. Ohjuri nimi peab ühtima Commerce Headquartersis määratud fiskaalühenduse nimega.

Konnektor toetab järgmisi taotlusi:

- **SubmitDocumentFiscalDeviceRequest – see taotlus saadab dokumendid printerisse ja** tagastab vastuse fiskaalprinterist.
- **IsReadyFiscalDeviceRequest** – seda taotlust kasutatakse seadme seisundikontrolliks.
- **InitializeFiscalDeviceRequest** – seda taotlust kasutatakse printeri lähtestamiseks.

#### <a name="configuration"></a>Konfiguratsioon

Fiskaalkonnektori konfiguratsioonifail asub lahenduste **hoidlas src \\ FiscalIntegration \\ Posnet \\\\ HardwareStationIsolatsiooniDeviceSample \\ Configuration \\ ConnectorPosnetThermalFAAAA.xml.**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Faili eesmärk on lubada finantsühenduse sätete konfigureerimist rakendusest Commerce headquarters. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetele.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
