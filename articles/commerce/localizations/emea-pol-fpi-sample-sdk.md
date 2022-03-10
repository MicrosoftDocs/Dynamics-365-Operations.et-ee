---
title: Poola fiskaalprinterite integratsioonivalimi juurutusjuhised (pärand)
description: Selles teemas antakse juhised poola fiskaalprinterite integreerimise näidise juurutamiseks jaemüügi tarkvaraarenduskomplektist Microsoft Dynamics 365 Commerce (SDK).
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 45cae498df8157b9561c54e9859daadcaedd7823
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2022
ms.locfileid: "8076984"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-poland-legacy"></a>Poola fiskaalprinterite integratsioonivalimi juurutusjuhised (pärand)

[!include[banner](../includes/banner.md)]

See teema annab juhised poola fiskaalprinteri integratsiooni näidise juurutamiseks jaemüügi tarkvaraarenduskomplektist Microsoft Dynamics 365 Commerce (SDK) arendaja virtuaalses masinas (VM) elutsükli teenustes Microsoft Dynamics (LCS). Lisateavet selle fiskaalintegratsiooni näidise kohta leiate teemast [Fiskaalprinteri integreerimise näidis Poola jaoks](emea-pol-fpi-sample.md). 

Poola eelarveintegratsiooni valim on osa jaemüügi SDK-st. SDK installimise ja kasutamise kohta leiate teavet teemast [Jaemüügi tarkvaraarenduskomplekti (SDK) arhitektuur](../dev-itpro/retail-sdk/retail-sdk-overview.md). See proov koosneb Commerce'i käitusaja (CRT) ja riistvarajaama laiendustest. Selle proovi käivitamiseks peate muutma ja ehitama CRT ja riistvarajaama projekte. Soovitame selles teemas kirjeldatud muudatuste tegemiseks kasutada modifitseerimata Retail SDK-d. Samuti soovitame kasutada allika juhtimissüsteemi, näiteks Azure DevOps kui ühtegi faili pole veel muudetud.

## <a name="development-environment"></a>Arenduskeskkonnad

Arengukeskkonna seadistamiseks järgige neid juhiseid, et saaksite proovi testida ja pikendada.

### <a name="commerce-runtime-extension-components"></a>Commerce'i käitusaja laiendi komponendid

Laienduskomponendid CRT sisalduvad jaotises Retail SDK. Järgmiste protseduuride lõpuleviimiseks avage  **CommerceRuntimeSamples.sln** lahendus jaotises **RetailSdk\\SampleExtensions\\CommerceRuntime**.

1. **Leidke projekt Runtime.Extensions.DocumentProvider.PosnetSample** ja ehitage see.
2. Otsige kaustast **Extensions.DocumentProvider.PosnetSample\\bin\\Debug** üles **assemblerifail Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll** assemblerifail.
3. Kopeerige assemblerifail CRT laienduskausta.

    - **Commerce Scale Unit:** kopeerige fail internetiteabeteenuste (IIS) Commerce Scale Uniti saidi asukoha all olevasse **\\bin\\ext** kausta.
    - **Kohalik CRT kaasaegses kassas:** kopeerige fail **\\ ext** kausta kohaliku CRT kliendimaakleri asukoha all.

4. Leidke laiendi konfiguratsioonifail:CRT

    - **Commerce Scale Unit:** faili nimi **on commerceruntime.ext.config** ja see asub prügikasti **\\ kaustas** IIS Commerce Scale Unit saidi asukoha all.
    - **Kohalik CRT kaasaegses kassas:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku CRT kliendimaakleri asukoha all.

5. Registreerige CRT laienduse konfiguratsioonifaili muudatus.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
    ```

6. Taaskäivitage Commerce'i teenus.

    - **Commerce Scale Unit:** taaskäivitage Commerce'i teenusesait IIS Managerist.
    - **Kliendimaakler:** lõpetage **dllhost.exe** protsess Task Manageris ja taaskäivitage seejärel kaasaegne kassa.

### <a name="hardware-station-extension-components"></a>Riistvarajaama laienduse komponendid

Riistvarajaama laienduse komponendid sisalduvad retail SDK-s. Järgmiste protseduuride lõpuleviimiseks avage **HardwareStationSamples.sln** lahendus jaotises **RetailSdk\\SampleExtensions\\HardwareStation**.

1. **Leidke projekt HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample** ja ehitage see.
2. Leidke kaustast **Extension.Posnet.ThermalFVFiscalPrinterSample\\bin\\Debug** assemblerifail **Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll** assemblerifail.
3. Assemblerifaili kopeerimine juurutatud riistvarajaama masinasse.

    - **Remote Hardware station:** kopeerige fail IIS-i riistvarajaama saidi asukoha all olevasse **prügikasti** kausta. Kopeerige printeri draiverite teegid (**libposcmbth.dll**, **libcmbthserial\_.dll** ja **cmbthpl.lng\_**).

4. Leidke riistvarajaama laienduste konfiguratsioonifail. Faili nimi **on HardwareStation.Extension.config**:

    - **Kaugriistvarajaam:** fail asub IIS-i riistvarajaama saidi asukoha all.

5. Lisage konfiguratsioonifaili kompositsioonijaotisse **järgmine** rida.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
    ```

6. Taaskäivitage riistvarajaama teenus.

    - **Remote Hardware station:** taaskäivitage riistvarajaama sait IIS Managerist.

## <a name="production-environment"></a>Tootmiskeskkond

Eelmises protseduuris lubasite laiendused, mis on finantsregistreerimisteenuse integratsioonivalimi komponendid. Lisaks peate järgima neid juhiseid, et luua juurutatavad paketid, mis sisaldavad Commerce'i komponente, ja rakendada need paketid tootmiskeskkonnas.

1. Tehke paketi konfiguratsioonifailides kausta RetailSdkAssets **\\ all** järgmised muudatused.

    - **Lisage konfiguratsioonifailidesse commerceruntime.ext.config** ja **CommerceRuntime.MPOSOffline.Ext.config** kompositsioonijaotisele **järgmine** rida.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
        ```

    - Lisage konfiguratsioonifaili HardwareStation.Extension.config **kompositsioonijaotisesse** **järgmine** rida.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
        ```

1. Tehke kausta BuildTools all **paketi kohandamise konfiguratsioonifailis** Customization.settings **konfiguratsioonifailis** järgmised muudatused.

    - Lisage järgmine rida, et lisada CRT laiendus juurutatavatesse pakettidesse.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll"/>
        ```

    - Lisage järgmine rida, et lisada juurutatavatesse pakettidesse riistvarajaama laiendus.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll"/>
        ```

1. Käivitage utiliidi jaoks Visual Studio käsuviip MSBuild ja käivitage **msbuild** kausta Retail SDK all juurutatavate pakettide loomiseks.
1. Rakendage paketid LCS-i kaudu või käsitsi. Lisateavet vt teemast [Create deployable packages](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

## <a name="design-of-extensions"></a>Laienduste kujundus

Poola fiskaalprinterite integratsiooninäidis põhineb fiskaalintegratsiooni [funktsioonil](fiscal-integration-for-retail-channel.md). Lisateavet fiskaalintegratsiooni lahenduse kujunduse kohta leiate [fiskaalintegratsiooni näidisprojekti](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) ülevaatest.

### <a name="commerce-runtime-extension-design"></a>Commerce'i käitusaja laienduse kujundus

Maksudokumentide pakkuja laienduse eesmärk on luua printeripõhiseid dokumente ja käsitleda fiskaalprinteri vastuseid.

Laiendus CRT on **Runtime.Extensions.DocumentProvider.PosnetSample**. See laiendus loob printerispetsiifiliste käskude komplekti JavaScript Object Notation (JSON) vormingus, mis on määratletud POSNETi spetsifikatsiooniga 19-3678.

Lisateavet fiskaalintegratsiooni lahenduse kujunduse kohta leiate teemast [Fiskaalne registreerimisprotsess ja fiskaalseadmete ja -teenuste](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskaalintegratsiooni näidised.

#### <a name="request-handler"></a>Taotluse käitleja

The **DocumentProviderPosnetProtocol** päringu töötleja on maksuprinterist dokumentide genereerimise päringu sisenemispunkt.

Käitleja on päritud **INamedRequestHandler** liides. **Käitleja nime tagastamise eest vastutab meetod HandlerName**. Käitleja nimi peaks vastama Commerce'i peakontoris määratud konnektori dokumendipakkuja nimele.

Konnektor toetab järgmisi taotlusi.

- **GetFiscalDocumentDocumentProviderRequest** – see taotlus sisaldab teavet selle kohta, milline dokument tuleks luua. See tagastab printerispetsiifilise dokumendi, mis tuleks fiskaalprinteris registreerida.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – See päring tagastab tellitavate sündmuste loendi. Praegu toetatakse järgmisi sündmusi: müük, X-aruande printimine ja Z-aruande printimine.

#### <a name="configuration"></a>Konfiguratsioon

Konfiguratsioonifail asub **laiendusprojekti kaustas Konfiguratsioon**. Faili eesmärk on lubada dokumendipakkuja sätete konfigureerimine Commerce'i peakontorist. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetega. Lisatakse järgmised sätted.

- KM-määrade vastendamine
- Maksevahendi tüübi vastendamine
- Deposiitmakse tüüp

### <a name="hardware-station-extension-design"></a>Riistvarajaama laienduse disain

Fiskaalpistikuks oleva laienduse eesmärk on suhelda fiskaalprinteriga.

Riistvarajaama laiendus on **HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample**. See laiendus kutsub POSNETi draiveri funktsioone, et edastada käske, mida CRT laiendus genereerib fiskaalprinterile. Samuti käsitleb see seadme vigu.

#### <a name="request-handler"></a>Taotluse käitleja

The **FiscalPrinterHandler** päringu töötleja on sisenemispunkt päringu käsitlemiseks maksuvälisseadmesse.

Käitleja on päritud **INamedRequestHandler** liides. **Käitleja nime tagastamise eest vastutab meetod HandlerName**. Töötleja nimi peaks ühtima fiskaalse konnektori nimega, mis on määratud Commerce'i peakorteris.

Konnektor toetab järgmisi taotlusi.

- **SubmitDocumentFiscalDeviceRequest** – See päring saadab dokumendid printeritele ja tagastab fiskaalprinterilt vastuse.
- **IsReadyFiscalDeviceRequest** – Seda päringut kasutatakse seadme tervisekontrolliks.
- **InitializeFiscalDeviceRequest** – Seda päringut kasutatakse printeri lähtestamiseks.

#### <a name="configuration"></a>Konfiguratsioon

Konfiguratsioonifail asub **Seadistamine** laiendusprojekti kaust. Faili eesmärk on lubada konnektori sätete konfigureerimine Commerce'i peakontorist. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetega. Lisatakse järgmised sätted.

- **Ühendusstring** – string, mis kirjeldab seadmega ühenduse üksikasju vormingus, mida draiver toetab. Lisateavet leiate POSNETi draiveri dokumentatsioonist.
- **Kuupäeva ja kellaaja sünkroonimine** – Väärtus, mis määrab, kas printeri kuupäev ja kellaaeg tuleb ühendatud riistvarajaamaga sünkroonida.
- **Seadme ajalõpp** – Aeg millisekundites, mille jooksul juht ootab seadmelt vastust. Lisateavet leiate POSNETi draiveri dokumentatsioonist.
