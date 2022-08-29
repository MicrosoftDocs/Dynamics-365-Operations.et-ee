---
title: Fiskaalprinteri integratsiooni näidise juurutuse juhised Poola jaoks (pärand)
description: See artikkel annab juhised fiskaalprinteri integreerimisnäidi juurutamiseks Poola jaoks jaemüügi Microsoft Dynamics 365 Commerce tarkvara arenduskomplektist (SDK).
author: EvgenyPopovMBS
ms.date: 08/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 178301e6d8e5f87376ed893e4bf5f966260cad62
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337217"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-poland-legacy"></a>Fiskaalprinteri integratsiooni näidise juurutuse juhised Poola jaoks (pärand)

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> Järgige selle artikli juhiseid ainult juhul, kui kasutate versiooni Microsoft Dynamics 365 Commerce 10.0.28 või varasemat versiooni. Äriversiooni 10.0.29 kohaselt on Poola fiskaalprinteri integratsiooni näidis saadaval Commerce’i tarkvara arenduskomplektis (SDK). Lisateavet vt kanali komponentide [konfigureerimine](./emea-pol-fpi-sample.md#configure-channel-components).

See artikkel annab juhised Fiskaalprinteri Dynamics 365 Commerce integreerimise näidiste juurutamiseks Poola jaoks jaemüügi SDK-st arendaja virtuaalmasinas (VM) Microsoft Dynamics elutsükli teenustes (LCS). Lisateavet selle fiskaalintegratsiooni näidiste kohta vt Poola fiskaalprinteri [integratsiooni näidist](emea-pol-fpi-sample.md). 

Poola fiskaalintegratsiooni näidis on jaemüügi SDK osa. Lisateavet selle kohta, kuidas installida ja kasutada SDK-d, vt jaemüügi [tarkvara arenduskomplekti (SDK) ülesehitust](../dev-itpro/retail-sdk/retail-sdk-overview.md). See näidis koosneb Commerce Runtime’i (CRT) ja riistvarajaama laiendustest. Selle näidisprojekti käivitamiseks peate muutma ja ehitama CRT riistvarajaama projekte. Soovitame kasutada jaemüügi SDK-d, et teha selles artiklis kirjeldatud muudatused. Soovitame kasutada ka allikakontrollisüsteemi, näiteks sellistena, Azure DevOps kus faile pole veel muudetud.

## <a name="development-environment"></a>Arenduskeskkond

Järgige neid samme arenduskeskkonna häälestamiseks, et saate testida ja laiendada näidist.

### <a name="commerce-runtime-extension-components"></a>Äri käitusaja laienduse komponendid

Laienduskomponendid CRT on kaasatud retail SDK-sse. Järgmiste protseduuride sooritamiseks avage CommerceRuntimeSamples.sln **lahendus** retailSdk **SampleExtensions\\ CommerceRuntime’i all\\.**

1. Leidke projekt **Runtime.Extensions.DocumentProvider.PosnetSample** ja koostage see.
2. Leidke kaustast Extensions.DocumentProvider.PosnetSample **bin\\ Silumine\\** contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll **assemblerifail**.
3. Kopeerige assemblerifail laienduskausta CRT:

    - **Commerce Scale Unit:** kopeerige fail **\\ bin ext\\ kausta** teenuse Internet Information Services (IIS) Commerce Scale Unit saidi asukoha all.
    - **Kohalik CRT modern POS-s:** kopeerige fail kohaliku **\\ kliendi maakleri asukoha ext-kausta** CRT.

4. Leidke laiendi konfiguratsioonifail:CRT

    - **Commerce Scale Unit:** faili nimi **on commerceruntime.ext.config** **\\ ja see on IIS Commerce Scale Uniti saidi asukoha bin ext-kaustas**.
    - **Modern CRT POS-is kohalik:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku kliendi maakleri CRT asukoha all.

5. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
    ```

6. Taaskäivitage Commerce Service:

    - **Commerce Scale Unit: taaskäivitage** Commerce Service’i sait IIS-i halduri kaudu.
    - **Kliendi maakler:** lõpetage **dllhost.exe** protsess ülesandehalduris ja taaskäivitage Modern POS.

### <a name="hardware-station-extension-components"></a>Riistvarajaama laienduse komponendid

Riistvarajaama laienduse komponendid on kaasatud Jaemüügi SDK-sse. Järgmiste protseduuride sooritamiseks avage **RetailSdk** SampleExtensions **HardwareStationis\\ konfiguratsioonilahendusHardwareStations.sln\\**.

1. Leidke projekt **HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample** ja koostage see.
2. Leidke kaustast Extension.Posnet.UuendavFiscalPrinterSample **bin\\ Silumine\\** assemblerifail Contoso.Commerce.HardwareStation.PosnetThermalFFiscalPrinterSample.dll **·**.
3. Kopeerige assemblerifail juurutatud riistvarajaama arvutisse:

    - **Kaug riistvarajaam:** kopeerige fail **IIS-i** riistvarajaama saidi asukoha bin-kausta. Kopeerige printeri draiveriteegid (**sysposcmbth.dll**, **thecmbth\_ serial.dll** ja **cmbth\_ pl.dll**).

4. Leidke riistvarajaama laienduste konfiguratsioonifail. Faili nimi on **HardwareStation.Extension.config**:

    - **Kaug riistvarajaam:** fail asub IIS-i riistvarajaama asukoha all.

5. Lisage konfiguratsioonifaili koostise **jaotisse** järgmine rida.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
    ```

6. Taaskäivitage riistvarajaama teenus:

    - **Kaug riistvarajaam: taaskäivitage** riistvarajaama sait IIS-i haldurist.

## <a name="production-environment"></a>Tootmiskeskkond

Eelmises protseduuris lubate laiendused, mis on fiskaalregistreerimise teenuse integratsiooni näidiskomponendid. Lisaks peate järgima neid samme Commerce’i komponente sisaldavate juurutatavate pakendite loomiseks ja nende pakendite rakendamiseks tootmiskeskkonnas.

1. Tehke paketi konfiguratsioonifailides kausta **RetailSdk Assets\\ all järgmised** muudatused:

    - **Commerceruntime.ext.config** **ja CommerceRuntime.MPOSOffline.Ext.config** konfiguratsioonifailides lisage koostise jaotisele **järgmine** rida.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
        ```

    - Konfiguratsioonifailis **HardwareStation.Extension.config** lisage koostise jaotisele järgmine **rida**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
        ```

1. Tehke kausta BuildTools **all** kohanduspaketi **kohandamise konfiguratsioonifailis** järgmised muudatused:

    - Lisage järgmine rida, et kaasata CRT laiend juurutatavatesse pakettidesse.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll"/>
        ```

    - Lisage järgmine rida, et kaasata riistvarajaama laiend juurutatavatesse pakendisse.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll"/>
        ```

1. Käivitage rakenduse MSBuild käsuviip Visual Studio **utiliidi jaoks ja käivitage msbuild** kausta Retail SDK all juurutatavate pakettide loomiseks.
1. Rakendage pakendid LCS-i kaudu või käsitsi. Lisateavet vt teemast Juurutatavate [pakendite loomine](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

## <a name="design-of-extensions"></a>Laienduste kujundus

Poola fiskaalprinteri integratsiooni näidis põhineb fiskaalintegratsiooni [funktsioonil](fiscal-integration-for-retail-channel.md). Lisateavet fiskaalintegratsiooni lahenduse kujunduse kohta vt fiskaalintegratsiooni [näidiskujunduse ülevaatest](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

### <a name="commerce-runtime-extension-design"></a>Äri käitusaja laiendi kujundus

Fiskaaldokumendi pakkujaks olemise laiend on luua printeripõhiseid dokumente ja käsitleda fiskaalprinteri vastuseid.

CRT Laiend on **Runtime.Extensions.DocumentProvider.PosnetSample**. See laiend loob Printerispetsiifiliste käskude komplekti JavaScripti objekti notationi (JSON) vormingus, mille on määranud POSNET-i spetsifikatsioon 19-3678.

Lisateavet fiskaalintegratsiooni lahenduse kujunduse kohta vt fiskaalregistreerimisprotsessist [ja fiskaalseadmete ja -teenuste fiskaalintegratsiooni näidised.](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services)

#### <a name="request-handler"></a>Nõudeohjur

DocumentProviderPosnetProtocol **taotluseohjur** on fiskaalprinterist dokumentide loomise nõude sisenemispunkt.

Ohjur pärineb INamedRequestHandler **liideselt**. Meetod **HandlerName** vastutab ohjuri nime tagastamise eest. Ohjuri nimi peab vastama Commerce Headquartersis määratud konnektori dokumendi pakkuja nimele.

Konnektor toetab järgmisi taotlusi:

- **GetFiscalDocumentDocumentProviderRequest** – see taotlus sisaldab teavet selle kohta, milline dokument tuleks luua. See tagastab printeripõhise dokumendi, mis tuleb registreerida fiskaalprinteris.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – see taotlus tagastab tellitavate sündmuste loendi. Praegu toetatakse järgmisi sündmusi: müük, X-aruande printimine ja Z-aruande printimine.

#### <a name="configuration"></a>Konfiguratsioon

Konfiguratsioonifail asub laiendusprojekti **konfiguratsioonikaustas**. Faili eesmärk on lubada dokumendipakkuja sätted rakendusest Commerce headquarters konfigureerimist. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetele. Lisatakse järgmised sätted:

- KM-määrade vastendamine
- Maksevahendi tüübi vastendamine
- Deposiitmakse tüüp

### <a name="hardware-station-extension-design"></a>Riistvarajaama laienduse kujundus

Fiskaalühenduseks olemise laiendi eesmärgiks on side fiskaalprinteriga.

Riistvarajaama laiend on **HardwareStation.Extension.PosnetThermalFFiscalPrinterSample**. See laiend kutsub POSNET-i draiveri funktsioone esitama käske, mida CRT laiend fiskaalprinterile loob. Samuti käsitletakse selles seadme tõrkeid.

#### <a name="request-handler"></a>Nõudeohjur

FiscalPrinterHandler **taotluseohjur** on sisenemispunkt fiskaalseadme perifeerseadme taotluse käsitlemiseks.

Ohjur pärineb INamedRequestHandler **liideselt**. Meetod **HandlerName** vastutab ohjuri nime tagastamise eest. Ohjuri nimi peab ühtima Commerce Headquartersis määratud fiskaalühenduse nimega.

Konnektor toetab järgmisi taotlusi:

- **SubmitDocumentFiscalDeviceRequest** – see taotlus saadab dokumendid printerisse ja tagastab vastuse fiskaalprinterist.
- **IsReadyFiscalDeviceRequest** – seda taotlust kasutatakse seadme seisundikontrolliks.
- **InitializeFiscalDeviceRequest** – seda taotlust kasutatakse printeri lähtestamiseks.

#### <a name="configuration"></a>Konfiguratsioon

Konfiguratsioonifail asub laiendusprojekti **konfiguratsioonikaustas**. Faili eesmärk on lubada ühenduse sätete konfigureerimine rakendusest Commerce headquarters. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetele. Lisatakse järgmised sätted:

- **Ühendusstring** – string, mis kirjeldab seadmega ühenduse üksikasju vormingus, mida draiver toetab. Lisateavet vt POSNET-i draiveri dokumentatsioonist.
- **Kuupäeva ja kellaaja sünkroonimine** – väärtus, mis määrab, kas printeri kuupäev ja kellaaeg tuleb sünkroonida ühendatud riistvarajaamaga.
- **Seadme ajalõpp** – aja hulk millisekundites, mille juht ootab seadmelt vastuse ootamist. Lisateavet vt POSNET-i draiveri dokumentatsioonist.
