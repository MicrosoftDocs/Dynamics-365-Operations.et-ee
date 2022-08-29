---
title: Fiskaalregistreerimisteenuse integreerimise näidisjuhised Saksamaa jaoks (pärand)
description: See artikkel annab juhised Saksamaa fiskaalintegratsiooni näidiste juurutamiseks jaemüügi tarkvara Microsoft Dynamics 365 Commerce arenduskomplektist (SDK).
author: EvgenyPopovMBS
ms.date: 08/17/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 7315b6bb145ccdc5631a558af88de55660ebf877
ms.sourcegitcommit: 0feb5d0b06e04f99903069ff2801577be86b8555
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 08/18/2022
ms.locfileid: "9313851"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-germany-legacy"></a>Fiskaalregistreerimisteenuse integreerimise näidisjuhised Saksamaa jaoks (pärand)

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

> [!IMPORTANT]
> Järgige selle artikli juhiseid ainult juhul, kui kasutate versiooni Microsoft Dynamics 365 Commerce 10.0.28 või varasemat versiooni. Vastavalt Versioonile Commerce 10.0.29 on Saksamaa fiskaalregistreerimisteenuse integreerimise näidis saadaval Commerce’i tarkvara arenduskomplektis (SDK). Lisateavet vt kanali komponentide [konfigureerimine](./emea-deu-fi-sample.md#configure-channel-components).

See artikkel annab juhised Dynamics 365 Commerce Fiskaalregistreerimise teenuse integreerimise näidiste juurutamiseks Saksamaa jaoks jaemüügi SDK-st arendaja virtuaalmasinas (VM) Microsoft Dynamics elutsükli teenustes (LCS). Lisateavet fiskaalintegratsiooni näidiste kohta vt Saksamaa [fiskaalteenuste integreerimise näidist](emea-deu-fi-sample.md). 

Saksamaa fiskaalintegratsiooni näidis on jaemüügi SDK osa. Lisateavet selle kohta, kuidas installida ja kasutada SDK-d, vt jaemüügi [tarkvara arenduskomplekti (SDK) ülesehitust](../dev-itpro/retail-sdk/retail-sdk-overview.md). See näidis koosneb Commerce Runtime’i (CRT) ja riistvarajaama laiendustest. Selle näidisprojekti käivitamiseks peate muutma ja ehitama CRT riistvarajaama projekte. Soovitame kasutada jaemüügi SDK-d, et teha selles artiklis kirjeldatud muudatused. Soovitame kasutada ka allikakontrollisüsteemi, näiteks sellistena, Azure DevOps kus faile pole veel muudetud.

## <a name="development-environment"></a>Arenduskeskkond

Järgige neid samme arenduskeskkonna häälestamiseks, et saate testida ja laiendada näidist.

### <a name="enable-commerce-runtime-extensions"></a>Luba Äri käitusaja laiendid

Laienduskomponendid CRT kaasatakse näidiste CRT hulka. Järgmiste protseduuride sooritamiseks avage CommerceRuntimeSamples.sln **lahendus** retailSdk **SampleExtensions\\ CommerceRuntime’i all\\.**

#### <a name="documentproviderefrsample-component"></a>DocumentProvider.EFRSample’i komponent

1. Leidke projekt **Runtime.Extensions.DocumentProvider.EFRSample** ja koostage see.
2. Leidke kaustast Runtime.Extensions.DocumentProvider.EFRSample **bin\\ Silumine\\** Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll **assemblerifail**.
3. Kopeerige assemblerifail laiendite CRT kausta:

    - **Commerce Scale Unit:** kopeerige fail **\\ bin ext\\ kausta** teenuse Internet Information Services (IIS) Commerce Scale Unit saidi asukoha all.
    - **Kohalik CRT modern POS-s:** kopeerige fail kohaliku **\\ kliendi maakleri asukoha ext-kausta** CRT.

4. Leidke laiendi konfiguratsioonifail:CRT

    - **Commerce Scale Unit:** faili nimi **on commerceruntime.ext.config** **\\ ja see on IIS Commerce Scale Uniti saidi asukoha bin ext-kaustas**.
    - **Modern CRT POS-is kohalik:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku kliendi maakleri CRT asukoha all.

5. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
    ```

#### <a name="documentproviderdatamodelefr-component"></a>DocumentProvider.DataModelEFR komponent

1. Leidke projekt **Runtime.Extensions.DocumentProvider.DataModelEFR** ja koostage see.
2. Leidke kaustast Runtime.Extensions.DocumentProvider.DataModelEFR **bin\\ Silumine\\** Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll **assemblerifail**.
3. Kopeerige assemblerifail laiendite CRT kausta:

    - **Commerce Scale Unit:** kopeerige fail **\\ bin ext\\ kausta** IIS Commerce Scale Uniti saidi asukoha all.
    - **Kohalik CRT modern POS-s:** kopeerige fail kohaliku **\\ kliendi maakleri asukoha ext-kausta** CRT.

4. Leidke laiendi konfiguratsioonifail:CRT

    - **Commerce Scale Unit:** faili nimi **on commerceruntime.ext.config** **\\ ja see on IIS Commerce Scale Uniti saidi asukoha bin ext-kaustas**.
    - **Modern CRT POS-is kohalik:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku kliendi maakleri CRT asukoha all.

5. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
    ```

#### <a name="extension-configuration-file"></a>Laiendi konfiguratsioonifail

1. Leidke laiendi konfiguratsioonifail:CRT

    - **Commerce Scale Unit:** faili nimi **on commerceruntime.ext.config** **\\ ja see on IIS Commerce Scale Uniti saidi asukoha bin ext-kaustas**.
    - **Modern CRT POS-is kohalik:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku kliendi maakleri CRT asukoha all.

2. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsGermany" />
    ```

### <a name="enable-fiscal-connector-extensions"></a>Fiskaalühenduse laienduste lubamine

Fiskaalühenduse laiendusi saate lubada riistvarajaamas [või](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station) kassaregistris [...](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network).

#### <a name="enable-hardware-station-extensions"></a>Riistvarajaama laienduste lubamine

Riistvarajaama laienduse komponendid sisalduvad riistvarajaama näidises. Järgmiste protseduuride sooritamiseks avage **RetailSdk** SampleExtensions **HardwareStationis\\ konfiguratsioonilahendusHardwareStations.sln\\**.

##### <a name="efrsample-component"></a>EFRSample’i komponent

1. Otsige üles **projekt HardwareStation.Extension.EFRSample** ja koostage see.
2. Leidke kaustast **Extension.EFRSample\\ bin\\ Silumine** järgmised assemblerifailid:

    - Contoso.Commerce.HardwareStation.EFRSample.dll
    - Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll

3. Kopeerige assemblerifailid riistvarajaama laienduste kausta:

    - **Ühiskasutatav riistvarajaam:** kopeerige failid **IIS-i** riistvarajaama saidi asukoha bin-kausta.
    - **Modern POS-i sihtotstarbeline riistvarajaam:** kopeerige failid Modern POS-i kliendi maakleri asukohta.

4. Leidke riistvarajaama laienduste laiendite konfiguratsioonifail. Faili nimi on **HardwareStation.Extension.config**.

    - **Ühiskasutatav riistvarajaam:** fail asub IIS-i riistvarajaama saidi asukohas.
    - **Modern POS-i sihtotstarbeline riistvarajaam:** fail asub Modern POS-i kliendi maakleri asukoha all

5. Lisage konfiguratsioonifaili koostise **jaotisse** järgmine rida.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample.dll" />
    ```

#### <a name="enable-pos-extensions"></a>Luba müügikoha laiendused

Kassa laienduse näidis asub lahenduste **hoidla kaustas FiscalIntegration\\ PosFiscalConnectorSample\\**[Dynamics 365 Commerce.](https://github.com/microsoft/Dynamics365Commerce.Solutions/)

Pärand-SDK-s kassa laienduse näidiste kasutamiseks järgige neid samme.

1. Kopeerige **kaust Pos.Extension** pärand-SDK **·**(nt ) kassalaiendite kausta`C:\RetailSDK\src\POS\Extensions`.
1. Nimetage kausta **Pos.Extension koopia** **PosFiscalConnectori ümber**.
1. Eemaldage kaustast **PosFiscalConnector** järgmised kaustad ja failid:

    - koht
    - DataService
    - devDependencies
    - Teegid
    - Obj
    - Contoso.PosFiscalConnectorSample.Pos.csproj
    - Tabeli RetailServerEdmxModel.g.xml
    - tsconfig.json

1. **Avage lahendus CloudPos.sln** või **ModernPos.sln**.
1. Projektis **Pos.Extensions** lisage kaust **PosFiscalConnector**.
1. Avage fail **extensions.json** ja lisage laiend **PosFiscalConnector**.
1. Koostage SDK.

### <a name="production-environment"></a>Tootmiskeskkond

Eelmises protseduuris lubate laiendused, mis on fiskaalregistreerimise teenuse integratsiooni näidiskomponendid. Lisaks peate järgima neid samme Commerce’i komponente sisaldavate juurutatavate pakendite loomiseks ja nende pakendite rakendamiseks tootmiskeskkonnas.

1. Tehke paketi konfiguratsioonifailides kausta **RetailSdk Assets\\ all järgmised** muudatused:

    - **Lisage konfiguratsioonifailides commerceruntime.ext.config** **ja CommerceRuntime.MPOSOffline.Ext.config** koostise jaotisele **järgmised** read.

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsGermany" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        ```

    - Konfiguratsioonifailis **HardwareStation.Extension.config** lisage koostise jaotisele järgmised **read**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        ```

2. Tehke kausta BuildTools **all** kohanduspaketi **kohandamise konfiguratsioonifailis** järgmised muudatused:

    - Lisage järgmised read, et kaasata CRT laiendused juurutatavatesse pakendisse.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

    - Lisage järgmised read riistvarajaama laienduste kaasamiseks juurutatavatesse pakendisse.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

3. Käivitage rakenduse MSBuild käsuviip Visual Studio **utiliidi jaoks ja käivitage msbuild** kausta Retail SDK all juurutatavate pakettide loomiseks.
4. Rakendage pakendid LCS-i kaudu või käsitsi. Lisateavet vt teemast Juurutatavate [pakendite loomine](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
5. Täitke kõik nõutud seadistustoimingud, mida on kirjeldatud [Saksamaa häälestamisprogrammis](emea-deu-fi-sample.md#set-up-commerce-for-germany).

## <a name="design-of-extensions"></a>Laienduste kujundus

Fiskaalregistreerimisteenuse integreerimise näidis Saksamaa jaoks põhineb fiskaalintegratsiooni [funktsioonil](fiscal-integration-for-retail-channel.md). Lisateavet fiskaalintegratsiooni lahenduse kujunduse kohta vt fiskaalintegratsiooni [näidiskujunduse ülevaatest](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

### <a name="commerce-runtime-extension-design"></a>Äri käitusaja laiendi kujundus

Fiskaaldokumendi pakkuja laiendi eesmärk on luua teenusepõhiseid dokumente ja käsitleda fiskaalregistreerimise teenuse vastuseid.

CRT Laiend on **Runtime.Extensions.DocumentProvider.EFRSample**. Lisateavet fiskaalintegratsiooni lahenduse kujunduse kohta vt ärikanalite [fiskaalintegratsiooni ülevaadet](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

#### <a name="request-handler"></a>Nõudeohjur

Dokumendipakkujal DocumentProviderEFRFiscalDEU **on üks taotluseohjur**. Seda ohjurit kasutatakse fiskaaldokumentide loomiseks fiskaalregistreerimise teenusele. See pärineb INamedRequestHandler **liideselt**. Meetod **HandlerName** vastutab ohjuri nime tagastamise eest. Ohjuri nimi peab vastama Commerce Headquartersis määratud konnektori dokumendi pakkuja nimele.

Konnektor toetab järgmisi taotlusi:

- **GetFiscalDocumentDocumentProviderRequest** – see taotlus sisaldab teavet selle kohta, milline dokument tuleks luua. See tagastab teenusepõhise dokumendi, mis tuleb registreerida fiskaalregistreerimise teenuses.
- **GetFiscalTransactionExtendedDataDocumentProviderRequest** – see taotlus tagastab vastuse koos laiendatud andmetega.

#### <a name="configuration"></a>Konfiguratsioon

**Konfiguratsioonifail DocumentProviderFiscalEFRSampleGermany** asub **laiendusprojekti** konfiguratsioonikaustas. Selle faili eesmärk on lubada dokumendipakkuja sätted rakendusest Commerce headquarters konfigureerimist. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetele.

Lisatakse järgmised sätted:

- **KM-määrade** **vastendamine – käibemaksukoodide jaoks seadistatud maksu protsendiväärtuste vastendamine fiskaalteenusele saadetud taotlustes atribuudi TaxG** (maksugrupp) väärtustega.
- **Maksugrupp kinkekaartide ja deposiitide** jaoks – **TaxG** atribuudi väärtus fiskaalteenusele saadetud taotlustes, mis põhinevad kinkekaarte või deposiite kaasatud toimingutel.
- **Maksevahendi tüübi** vastendamine: **makseviiside vastendamine atribuudi PayG** (maksegrupp) väärtustega fiskaalteenusesse saadetud taotlustes.
- **Käibemaksuvabastuse maksugrupp** – **atribuudi TaxG** väärtus fiskaalteenusele saadetud taotlustes, mis põhinevad maksukohustustest vabastatud toimingutel.
- **Kaasa kliendiandmed** – kui see parameeter on sisse lülitatud, sisaldavad rahandusteenuse taotlused klienditeavet, nt nimesid ja aadresse, juhul kui klient lisatakse kandesse.

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

Konfiguratsioonifail asub laiendusprojekti **konfiguratsioonikaustas**. Faili eesmärk on lubada finantsühenduse sätete konfigureerimist rakendusest Commerce headquarters. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetele.

Lisatakse järgmised sätted:

- **Lõpp-punkti** aadress – fiskaalregistreerimise teenuse URL.
- **Ajalõpp** – aja hulk millisekundites (ms), mille juht ootab fiskaalregistreerimise teenuselt vastust.
- **Kuva fiskaalregistreerimise teatised – kui see parameeter on sisse lülitatud, kuvatakse fiskaalteenuse teatised kassas** kasutajateadetega.

### <a name="pos-fiscal-connector-extension-design"></a>Müügikoha fiskaalkonnektori laienduse kujundus

Kassa fiskaalühenduse laienduse eesmärk on kassast fiskaalregistreerimise teenusega sideühendus. See kasutab side jaoks HTTPS-protokolli.

#### <a name="fiscal-connector-factory"></a>Fiskaalühenduse tehas

Fiskaalühenduse tehas vastendab konnektori nime fiskaalühenduse **rakendusega ja asub failis Pos.Extension\\ Connectors\\ FiscalConnectorFactory.ts**. Konnektori nimi peab kattuma Commerce Headquartersis määratud fiskaalühenduse nimega.

#### <a name="efr-fiscal-connector"></a>EFR-i fiskaalühendus

EFR-i fiskaalühendus asub **failis Pos.Extension\\ Connectors\\ Efr\\ EfrFiscalConnector.ts**. See juurutab **IFiscalConnectori** liidest, mis toetab järgmisi taotlusi:

- **FiscalRegisterSubmitDocumentClientRequest** – see taotlus saadab dokumendid fiskaalregistreerimise teenusesse ja tagastab sellelt vastuse.
- **FiscalRegisterIsReadyClientRequest** – seda taotlust kasutatakse fiskaalregistreerimise teenuse seisundikontrolliks.
- **FiscalRegisterInitializeClientRequest** – seda taotlust kasutatakse fiskaalregistreerimise teenuse lähtestamiseks.

#### <a name="configuration"></a>Konfiguratsioon

Konfiguratsioonifail asub lahenduste hoidla src **FiscalIntegration\\ Efr\\ Configurations\\ Connectorite\\ kaustas**[Dynamics 365 Commerce.](https://github.com/microsoft/Dynamics365Commerce.Solutions/) Faili eesmärk on lubada finantsühenduse sätete konfigureerimist rakendusest Commerce headquarters. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetele. Lisatakse järgmised sätted:

- **Lõpp-punkti** aadress – fiskaalregistreerimise teenuse URL.
- **Ajalõpp** – aeg millisekundites, mille konnektor ootab fiskaalregistreerimise teenuselt vastust.
