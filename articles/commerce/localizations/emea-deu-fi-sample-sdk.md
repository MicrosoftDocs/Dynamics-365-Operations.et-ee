---
title: Saksamaa maksuregistreerimisteenuse integratsioonivalimi kasutuselevõtu juhised (pärand)
description: See teema annab juhised Saksamaa fiskaalintegratsiooni valimi juurutamiseks jaemüügi tarkvaraarenduskomplektist Microsoft Dynamics 365 Commerce (SDK).
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 98641f9989322feb77ab683df66c2c1f9ad50a0d
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2022
ms.locfileid: "8077061"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-germany-legacy"></a>Saksamaa maksuregistreerimisteenuse integratsioonivalimi kasutuselevõtu juhised (pärand)

[!include [banner](../includes/banner.md)]

See teema annab juhised saksamaa fiskaalregistreerimisteenuse integreerimise näidise juurutamiseks jaemüügi tarkvaraarenduskomplektist Microsoft Dynamics 365 Commerce (SDK) arendaja virtuaalses masinas Microsoft Dynamics (VM) lifecycle Services (LCS). Lisateavet selle fiskaalintegratsiooni valimi kohta leiate teemast [Saksamaa eelarve registreerimisteenuse integratsioonivalim](emea-deu-fi-sample.md). 

Saksamaa fiskaalintegratsiooni valim on osa jaemüügi SDK-st. SDK installimise ja kasutamise kohta leiate teavet teemast [Jaemüügi tarkvaraarenduskomplekti (SDK) arhitektuur](../dev-itpro/retail-sdk/retail-sdk-overview.md). See proov koosneb Commerce'i käitusaja (CRT) ja riistvarajaama laiendustest. Selle proovi käivitamiseks peate muutma ja ehitama CRT ja riistvarajaama projekte. Soovitame selles teemas kirjeldatud muudatuste tegemiseks kasutada modifitseerimata Retail SDK-d. Samuti soovitame kasutada allika juhtimissüsteemi, näiteks Azure DevOps kui ühtegi faili pole veel muudetud.

## <a name="development-environment"></a>Arenduskeskkonnad

Arengukeskkonna seadistamiseks järgige neid juhiseid, et saaksite proovi testida ja pikendada.

### <a name="enable-commerce-runtime-extensions"></a>Commerce'i käitusajalaiendite lubamine

Laienduskomponendid CRT sisalduvad proovides CRT. Järgmiste protseduuride lõpuleviimiseks avage **CommerceRuntimeSamples.sln** lahendus jaotises **RetailSdk\\SampleExtensions\\CommerceRuntime**.

#### <a name="documentproviderefrsample-component"></a>DocumentProvider.EFRSample komponent

1. **Leidke projekt Runtime.Extensions.DocumentProvider.EFRSample** ja ehitage see.
2. Otsige kaustast **Runtime.Extensions.DocumentProvider.EFRSample\\bin\\Debug** üles **assemblerifail Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll** assemblerfaili.
3. Kopeerige assemblerifail CRT kausta Laiendused.

    - **Commerce Scale Unit:** kopeerige fail internetiteabeteenuste (IIS) Commerce Scale Uniti saidi asukoha all olevasse **\\bin\\ext** kausta.
    - **Kohalik CRT kaasaegses kassas:** kopeerige fail **\\ ext** kausta kohaliku CRT kliendimaakleri asukoha all.

4. Leidke laiendi konfiguratsioonifail:CRT

    - **Commerce Scale Unit:** faili nimi **on commerceruntime.ext.config** ja see asub prügikasti **\\ kaustas** IIS Commerce Scale Unit saidi asukoha all.
    - **Kohalik CRT kaasaegses kassas:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku CRT kliendimaakleri asukoha all.

5. Registreerige CRT laienduse konfiguratsioonifaili muudatus.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
    ```

#### <a name="documentproviderdatamodelefr-component"></a>DocumentProvider.DataModelEFR komponent

1. **Leidke projekt Runtime.Extensions.DocumentProvider.DataModelEFR** ja ehitage see.
2. Otsige üles kaust **Runtime.Extensions.DocumentProvider.DataModelEFR\\bin\\Debug** assemblerifail **Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll** assemblerifail.
3. Kopeerige assemblerifail CRT kausta Laiendused.

    - **Commerce Scale Unit:** kopeerige fail **\\bin\\ext** IIS Commerce'i skaala ühiku saidi asukoha all.
    - **Kohalik CRT kaasaegses kassas:** kopeerige fail **\\ ext** kausta kohaliku CRT kliendimaakleri asukoha all.

4. Leidke laiendi konfiguratsioonifail:CRT

    - **Commerce Scale Unit:** faili nimi **on commerceruntime.ext.config** ja see asub prügikasti **\\ kaustas** IIS Commerce Scale Unit saidi asukoha all.
    - **Kohalik CRT kaasaegses kassas:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku CRT kliendimaakleri asukoha all.

5. Registreerige CRT laienduse konfiguratsioonifaili muudatus.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
    ```

#### <a name="extension-configuration-file"></a>Laienduse konfiguratsioonifail

1. Leidke laiendi konfiguratsioonifail:CRT

    - **Commerce Scale Unit:** faili nimi **on commerceruntime.ext.config** ja see asub prügikasti **\\ kaustas** IIS Commerce Scale Unit saidi asukoha all.
    - **Kohalik CRT kaasaegses kassas:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku CRT kliendimaakleri asukoha all.

2. Registreerige CRT laienduse konfiguratsioonifaili muudatus.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsGermany" />
    ```

### <a name="enable-hardware-station-extensions"></a>Riistvarajaama laienduste lubamine

Riistvarajaama laienduse komponendid sisalduvad riistvarajaama näidistes. Järgmiste protseduuride lõpuleviimiseks avage **HardwareStationSamples.sln** lahendus jaotises **RetailSdk\\SampleExtensions\\HardwareStation**.

#### <a name="efrsample-component"></a>EFRSample komponent

1. **Leidke projekt HardwareStation.Extension.EFRSample** ja ehitage see.
2. Leidke kaustast **Extension.EFRSample\\bin\\Debug** järgmised assemblerifailid.

    - Contoso.Commerce.HardwareStation.EFRSample.dll
    - Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll

3. Kopeerige assemblerifailid kausta Riistvarajaama laiendused.

    - **Ühiskasutusega riistvarajaam:** kopeerige failid IIS-i riistvarajaama saidi asukoha all olevasse **prügikasti** kausta.
    - **Spetsiaalne riistvarajaam kaasaegses kassas:** kopeerige failid Kaasaegse kassa kliendimaakleri asukohta.

4. Leidke riistvarajaama laienduste konfiguratsioonifail. Faili nimi **on HardwareStation.Extension.config**.

    - **Jagatud riistvarajaam:** fail asub IIS-i riistvarajaama saidi asukoha all.
    - **Spetsiaalne riistvarajaam kaasaegses kassas:** fail asub Kaasaegse kassa kliendimaakleri asukoha all.

5. Lisage konfiguratsioonifaili kompositsioonijaotisse **järgmine** rida.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample.dll" />
    ```

### <a name="production-environment"></a>Tootmiskeskkond

Eelmises protseduuris lubasite laiendused, mis on finantsregistreerimisteenuse integratsioonivalimi komponendid. Lisaks peate järgima neid juhiseid, et luua juurutatavad paketid, mis sisaldavad Commerce'i komponente, ja rakendada need paketid tootmiskeskkonnas.

1. Tehke paketi konfiguratsioonifailides kausta RetailSdkAssets **\\ all** järgmised muudatused.

    - **Lisage konfiguratsioonifailidesse commerceruntime.ext.config** ja **CommerceRuntime.MPOSOffline.Ext.config** kompositsioonijaotisesse **järgmised** read.

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsGermany" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        ```

    - Lisage konfiguratsioonifaili HardwareStation.Extension.config **kompositsioonijaotisesse** **järgmised** read.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        ```

2. Tehke kausta BuildTools all **paketi kohandamise konfiguratsioonifailis** Customization.settings **konfiguratsioonifailis** järgmised muudatused.

    - Lisage järgmised read, et lisada CRT laiendused juurutatavatesse pakettidesse.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

    - Lisage järgmised read, et lisada juurutatavatesse pakettidesse riistvarajaama laiendused.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

3. Käivitage utiliidi jaoks Visual Studio käsuviip MSBuild ja käivitage **msbuild** kausta Retail SDK all juurutatavate pakettide loomiseks.
4. Rakendage paketid LCS-i kaudu või käsitsi. Lisateavet vt teemast [Create deployable packages](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
5. Täitke kõik vajalikud seadistustoimingud, mida on kirjeldatud jaotises [Saksamaa](emea-deu-fi-sample.md#set-up-commerce-for-germany) kaubanduse häälestamine.

## <a name="design-of-extensions"></a>Laienduste kujundus

Saksamaa maksuregistreerimisteenuse integreerimise näidis põhineb fiskaalintegratsiooni [funktsioonil](fiscal-integration-for-retail-channel.md). Lisateavet fiskaalintegratsiooni lahenduse kujunduse kohta leiate [fiskaalintegratsiooni näidisprojekti](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) ülevaatest.

### <a name="commerce-runtime-extension-design"></a>Commerce'i käitusaja laienduse kujundus

Fiskaaldokumendi pakkuja laienduse eesmärk on luua teenusepõhiseid dokumente ja käsitleda fiskaalregistreerimisteenuse vastuseid.

Laiendus CRT on **Runtime.Extensions.DocumentProvider.EFRSample**. Lisateavet fiskaalintegratsiooni lahenduse kujunduse kohta leiate teemast [Ülevaade Commerce'i kanalite](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskaalintegratsioonist.

#### <a name="request-handler"></a>Taotluse käitleja

Dokumendipakkuja **jaoks on üks päringukäsitleja DocumentProviderEFRFiscalDEU**. Seda käitlejat kasutatakse finantsregistreerimisteenuse finantsdokumentide loomiseks. See on päritud **INamedRequestHandleri** liidesest. **Käitleja nime tagastamise eest vastutab meetod HandlerName**. Käitleja nimi peaks vastama Commerce'i peakontoris määratud konnektori dokumendipakkuja nimele.

Konnektor toetab järgmisi taotlusi.

- **GetFiscalDocumentDocumentProviderRequest** – see taotlus sisaldab teavet selle kohta, milline dokument tuleks luua. See tagastab teenusepõhise dokumendi, mis tuleks registreerida maksuregistreerimisteenuses.
- **GetFiscalTransactionExtendedDataDocumentProviderRequest** – see taotlus tagastab vastuse koos laiendatud andmetega.

#### <a name="configuration"></a>Konfiguratsioon

**DocumentProviderFiscalEFRSampleGermany** konfiguratsioonifail asub laiendusprojekti kaustas **Konfiguratsioon**. Selle faili eesmärk on lubada dokumendipakkuja sätete konfigureerimine Commerce'i peakontorist. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetega.

Lisatakse järgmised sätted.

- **KM-i maksumäärade vastendamine** – maksu protsendiväärtuste vastendamine, mis on seadistatud käibemaksukoodide jaoks maksuteenusele saadetud taotluste atribuudi TaxG **(maksugrupp) väärtustega**.
- **Kinkekaartide ja sissemaksete maksugrupp** – väärtus **TaxG** atribuut maksuteenistusele saadetavates päringutes, mis põhinevad toimingutel, mis hõlmavad kinkekaarte või sissemakseid.
- **Pakkumise tüübi kaardistamine** – Makseviiside vastendamine väärtustele **PayG** (maksegrupp) atribuut taotlustes, mis saadetakse maksuteenistusele.
- **Maksugrupp käibemaksuvabaks** – väärtus **TaxG** atribuut maksuteenistusele saadetavates päringutes, mis põhinevad maksukohustustest vabastatud toimingutel.
- **Kaasake kliendiandmed** – Kui see parameeter on sisse lülitatud, sisaldavad maksuteenistuse päringud klienditeavet (nt nimed ja aadressid) juhul, kui tehingusse lisatakse klient.

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

Konfiguratsioonifail asub **Seadistamine** laiendusprojekti kaust. Faili eesmärk on lubada fiskaalse konnektori sätteid Commerce'i peakorteris konfigureerida. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetega.

Lisatakse järgmised sätted.

- **Lõpp-punkti aadress** – maksuregistreerimisteenuse URL.
- **Aeg maha** – Aeg millisekundites (ms), mille jooksul juht ootab maksuregistreerimisteenuse vastust.
- **Näita maksuregistreerimise teatisi** – Kui see parameeter on sisse lülitatud, kuvatakse maksuteenuse märguanded müügikohas kasutajateadetena.
