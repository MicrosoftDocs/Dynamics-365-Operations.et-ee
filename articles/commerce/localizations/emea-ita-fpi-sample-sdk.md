---
title: Fiskaalprinteri integratsiooni näidise juurutuse juhised Itaalia jaoks (pärand)
description: See artikkel annab juhised fiskaalprinteri integreerimise näidiste juurutamiseks Itaalia jaoks jaemüügi Microsoft Dynamics 365 Commerce tarkvara arenduskomplektist (SDK).
author: EvgenyPopovMBS
ms.date: 08/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 46d42a2c2a5f8f40fc8b9693f26a182c8f2e6352
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/23/2022
ms.locfileid: "9337214"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-italy-legacy"></a>Fiskaalprinteri integratsiooni näidise juurutuse juhised Itaalia jaoks (pärand)

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> Järgige selle artikli juhiseid ainult juhul, kui kasutate versiooni Microsoft Dynamics 365 Commerce 10.0.28 või varasemat versiooni. Äriversiooni 10.0.29 kohaselt on Itaalia fiskaalprinteri integratsiooni näidis saadaval Commerce’i tarkvara arenduskomplektis (SDK). Lisateavet vt kanali komponentide [konfigureerimine](./emea-ita-fpi-sample.md#configure-channel-components).

See artikkel annab juhised fiskaalprinteri Dynamics 365 Commerce integreerimise näidiste juurutamiseks Itaalia jaoks jaemüügi SDK-st arendaja virtuaalmasinas (VM) Microsoft Dynamics elutsükli teenustes (LCS). Lisateavet fiskaalintegratsiooni näidiste kohta vt Itaalia fiskaalprinteri [integratsiooni näidist](emea-ita-fpi-sample.md). 

Itaalia fiskaalintegratsiooni näidis on jaemüügi SDK osa. Lisateavet selle kohta, kuidas installida ja kasutada SDK-d, vt jaemüügi [tarkvara arenduskomplekti (SDK) ülesehitust](../dev-itpro/retail-sdk/retail-sdk-overview.md). See näidis koosneb Commerce Runtime’i (CRT) ja riistvarajaama laiendustest. Selle näidisprojekti käivitamiseks peate muutma ja ehitama CRT riistvarajaama projekte. Soovitame kasutada jaemüügi SDK-d, et teha selles artiklis kirjeldatud muudatused. Soovitame kasutada ka allikakontrollisüsteemi, näiteks sellistena, Azure DevOps kus faile pole veel muudetud.

## <a name="development-environment"></a>Arenduskeskkond

Järgige neid samme arenduskeskkonna häälestamiseks, et saate testida ja laiendada näidist.

### <a name="commerce-runtime-extension-components"></a>Äri käitusaja laienduse komponendid

Laienduskomponendid CRT on kaasatud retail SDK-sse. Järgmiste protseduuride sooritamiseks avage CommerceRuntimeSamples.sln **lahendus** retailSdk **SampleExtensions\\ CommerceRuntime’i all\\.**

1. Leidke projekt **Runtime.Extensions.DocumentProvider.EpsonFP90IIISample ja** koostage see.
2. Leidke kaustast Extensions.DocumentProvider.EpsonFP90IIISample **bin\\ Debug\\ find the** Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll **assemblerfail**.
3. Kopeerige assemblerifail laiendite CRT kausta:

    - **Commerce Scale Unit:** kopeerige fail **\\ bin ext\\ kausta** teenuse Internet Information Services (IIS) Commerce Scale Unit saidi asukoha all.
    - **Kohalik CRT modern POS-s:** kopeerige fail kohaliku **\\ kliendi maakleri asukoha ext-kausta** CRT.

4. Leidke laiendi konfiguratsioonifail:CRT

    - **Commerce Scale Unit:** faili nimi **on commerceruntime.ext.config** **\\ ja see on IIS Commerce Scale Uniti saidi asukoha bin ext-kaustas**.
    - **Modern CRT POS-is kohalik:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku kliendi maakleri CRT asukoha all.

5. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
    ```

6. Taaskäivitage Commerce Scale Unit:

    - **Commerce Scale Unit: taaskäivitage** Commerce Scale Uniti sait IIS-i halduri kaudu.
    - **Kliendi maakler:** lõpetage **dllhost.exe** protsess ülesandehalduris ja taaskäivitage Modern POS.

### <a name="hardware-station-extension-components"></a>Riistvarajaama laienduse komponendid

Riistvarajaama laienduse komponendid on kaasatud Jaemüügi SDK-sse. Järgmiste protseduuride sooritamiseks avage **RetailSdk** SampleExtensions **HardwareStationis\\ konfiguratsioonilahendusHardwareStations.sln\\**.

1. Leidke projekt **HardwareStation.Extensions.EpsonFP90IIIFiscalDeviceSample** ja koostage see.
2. Leidke kaustast Extensions.EpsonFP90IIIFiscalDeviceSample **bin\\ Silumine\\** assemblerifail Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll **·**.
3. Kopeerige assemblerifail juurutatud riistvarajaama arvutisse:

    - **Kaug riistvarajaam:** kopeerige fail **IIS-i** riistvarajaama saidi asukoha bin-kausta.
    - **Kohalik riistvarajaam: kopeerige** fail Modern POS-i kliendi maakleri asukohta.

4. Leidke riistvarajaama laienduste konfiguratsioonifail. Faili nimi on **HardwareStation.Extension.config**:

    - **Kaug riistvarajaam:** fail asub IIS-i riistvarajaama asukoha all.
    - **Kohalik riistvarajaam:** fail asub Modern POS-i kliendi maakleri asukoha all.

5. Lisage konfiguratsioonifaili koostise **jaotisse** järgmine jaotis.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
    ```

6. Taaskäivitage riistvarajaama teenus:

    - **Kaug riistvarajaam: taaskäivitage** riistvarajaama sait IIS-i haldurist.
    - **Kohalik riistvarajaam: lõpetage** protsess **dllhost.exe** ülesandehalduris ja taaskäivitage modern POS.

## <a name="production-environment"></a>Tootmiskeskkond

Commerce’i komponente sisaldavate juurutatavate pakendite loomiseks ja nende pakendite rakendamiseks tootmiskeskkonnas järgige neid samme.

1. Viige lõpule selle artikli varasemas arenduskeskkonna [jaotises](#development-environment) kirjeldatud sammud.
2. Tehke paketi konfiguratsioonifailides kausta **RetailSdk Assets\\ all järgmised** muudatused:

    1. **Commerceruntime.ext.config** **ja CommerceRuntime.MPOSOffline.Ext.config** konfiguratsioonifailides lisage koostise jaotisele **järgmine** rida.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
        ```

    1. Konfiguratsioonifailis **HardwareStation.Extension.config** lisage koostise jaotisele järgmine **rida**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
        ```

3. Tehke kausta BuildTools **all** kohanduspaketi **kohandamise konfiguratsioonifailis** järgmised muudatused:

    1. Lisage järgmine rida, et kaasata CRT laiend juurutatavatesse pakettidesse.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll"/>
        ```

    1. Lisage järgmine rida, et kaasata riistvarajaama laiend juurutatavatesse pakendisse.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll"/>
        ```

4. Tehke järgmised muudatused **Sdk.ModernPos.Shared.csproj** **failis kausta Packages SharedPackagingProjectComponents\_ all, et kaasata Itaalia ressursifailid juurutatavatesse** pakettidesse:

    1. Lisage jaotis **ItemGroup**, mis sisaldab sõlmpunkte, mis osutavad soovitud tõlgete ressursifailidele. Veenduge, et määrate õiged nimeruumid ja näidisnimed. Järgmises näites lisatakse selle **ja** **it-CH lokaadile ressursisõlmed**.

        ```xml
        <ItemGroup>
            <ResourcesIt Include="$(SdkReferencesPath)\it\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
            <ResourcesItCh Include="$(SdkReferencesPath)\it-CH\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
        </ItemGroup>
        ```

    1. Jaotises Target **Name="CopyPackageFiles"** lisage üks rida iga lokaadi jaoks, nagu näha järgmises näites.

        ```xml
        <Copy SourceFiles="@(ResourcesIt)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\it" SkipUnchangedFiles="true" />
        <Copy SourceFiles="@(ResourcesItCh)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\it-CH" SkipUnchangedFiles="true" />
        ```

5. Juurutatavatesse pakettidesse **Itaalia ressursifailide kaasamiseks tehke kaustas Packages SharedPackagingProjectComponents** failis **Sdk.RetailServerSetup.proj\_** järgmised muudatused:

    1. Lisage jaotis **ItemGroup**, mis sisaldab sõlmpunkte, mis osutavad soovitud tõlgete ressursifailidele. Veenduge, et määrate õiged nimeruumid ja näidisnimed. Järgmises näites lisatakse selle **ja** **it-CH lokaadile ressursisõlmed**.

        ```xml
        <ItemGroup>
            <ResourcesIt Include="$(SdkReferencesPath)\it\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
            <ResourcesItCh Include="$(SdkReferencesPath)\it-CH\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
        </ItemGroup>
        ```

    1. Jaotises Target **Name="CopyPackageFiles"** lisage üks rida iga lokaadi jaoks, nagu näha järgmises näites.

        ``` xml
        <Copy SourceFiles="@(ResourcesIt)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\it" SkipUnchangedFiles="true" />
        <Copy SourceFiles="@(ResourcesItCh)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\it-CH" SkipUnchangedFiles="true" />
        ```

6. Käivitage rakenduse MSBuild käsuviip Visual Studio **utiliidi jaoks ja käivitage seejärel juurutatavate pakettide loomiseks msbuild** kausta Retail SDK all.
7. Rakendage pakendid LCS-i kaudu või käsitsi. Lisateavet vt teemast Juurutatavate [pakendite loomine](../dev-itpro/retail-sdk/retail-sdk-packaging.md).

## <a name="design-of-extensions"></a>Laienduste kujundus

### <a name="commerce-runtime-extension-design"></a>Äri käitusaja laiendi kujundus

Fiskaaldokumendi pakkujaks olemise laiend on luua printeripõhiseid dokumente ja käsitleda fiskaalprinteri vastuseid.

CRT Laiend on **Runtime.Extensions.DocumentProvider.EpsonFP90IIISample**.

Lisateavet fiskaalintegratsiooni lahenduse kujunduse kohta vt fiskaalregistreerimisprotsessist [ja fiskaalseadmete ja -teenuste fiskaalintegratsiooni näidised.](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services)

#### <a name="request-handler"></a>Nõudeohjur

DocumentProviderEpsonFP90III **taotluseohjur** on fiskaalprinterist dokumentide loomise nõude sisenemispunkt.

Ohjur pärineb INamedRequestHandler **liideselt**. Meetod **HandlerName** vastutab ohjuri nime tagastamise eest. Ohjuri nimi peab vastama Commerce Headquartersis määratud konnektori dokumendi pakkuja nimele.

Konnektor toetab järgmisi taotlusi:

- **GetFiscalDocumentDocumentProviderRequest** – see taotlus sisaldab teavet selle kohta, milline dokument tuleks luua. See tagastab printeripõhise dokumendi, mis tuleb registreerida fiskaalprinteris.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – see taotlus tagastab tellitavate sündmuste loendi. Praegu toetatakse järgmisi sündmusi: müük, X-aruande printimine ja Z-aruande printimine.

#### <a name="configuration"></a>Konfiguratsioon

Konfiguratsioonifail asub laiendusprojekti **konfiguratsioonikaustas**. Faili eesmärk on lubada dokumendipakkuja sätted rakendusest Commerce headquarters konfigureerimist. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetele. Lisatakse järgmised sätted:

- KM-koodide vastendamine
- KM-määrade vastendamine
- Maksevahendi tüübi vastendamine
- Kviitungi numbri vöötkoodi tüüp
- Deposiitmakse tüüp

### <a name="hardware-station-extension-design"></a>Riistvarajaama laienduse kujundus

Fiskaalühenduseks olemise laiendi eesmärgiks on side fiskaalprinteriga.

Riistvarajaama laiend on **HardwareStation.Extension.EpsonFP90IIIFiscalDeviceSample**. See laiend kasutab HTTP-protokolli, et esitada dokumente, CRT mida laiend fiskaalprinterile loob. Samuti käsitletakse fiskaalprinterilt saadud vastuseid.

#### <a name="request-handler"></a>Nõudeohjur

**EpsonFP90IIISample’i** taotluseohjur on fiskaalseadme nõude käsitlemise sisenemispunkt.

Ohjur pärineb INamedRequestHandler **liideselt**. Meetod **HandlerName** vastutab ohjuri nime tagastamise eest. Ohjuri nimi peab ühtima Commerce Headquartersis määratud fiskaalühenduse nimega.

Konnektor toetab järgmisi taotlusi:

- **SubmitDocumentFiscalDeviceRequest** – see taotlus saadab dokumendid printerisse ja tagastab vastuse fiskaalprinterist.
- **IsReadyFiscalDeviceRequest** – seda taotlust kasutatakse seadme seisundikontrolliks.
- **InitializeFiscalDeviceRequest** – seda taotlust kasutatakse printeri lähtestamiseks.

#### <a name="configuration"></a>Konfiguratsioon

Konfiguratsioonifail asub laiendusprojekti **konfiguratsioonikaustas**. Faili eesmärk on lubada ühenduse sätete konfigureerimine rakendusest Commerce headquarters. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetele. Lisatakse järgmised sätted:

- **Lõpp-punkti** aadress – printeri URL.
- **Kuupäeva ja kellaaja sünkroonimine** – väärtus, mis määrab, kas printeri kuupäev ja kellaaeg tuleb sünkroonida ühendatud riistvarajaamaga.
