---
title: Rootsi kontrollüksuse integratsioonivalimi kasutuselevõtu juhised (pärand)
description: Selles teemas antakse juhised juhtüksuse integratsioonivalimi kasutuselevõtuks Rootsi jaoks retail SDK-st
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: b8d60f32d986dec6bb26d78ebdfe8cee3a6b688a
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2022
ms.locfileid: "8077034"
---
# <a name="deployment-guidelines-for-the-control-unit-integration-sample-for-sweden-legacy"></a>Rootsi kontrollüksuse integratsioonivalimi kasutuselevõtu juhised (pärand)

[!include [banner](../includes/banner.md)]

See teema annab juhised juhtüksuse integreerimise proovi juurutamiseks Rootsi jaoks jaemüügi tarkvaraarenduskomplektist (SDK) arendaja virtuaalses masinas Microsoft Dynamics (VM) lifecycle Services (LCS). Lisateavet selle fiskaalintegratsiooni valimi kohta leiate Rootsi [juhtüksuse integratsioonivalimist](emea-swe-fi-sample.md). 

Rootsi fiskaalintegratsiooni valim on osa jaemüügi SDK-st. SDK installimise ja kasutamise kohta leiate teavet teemast [Jaemüügi tarkvaraarenduskomplekti (SDK) arhitektuur](../dev-itpro/retail-sdk/retail-sdk-overview.md). See proov koosneb Commerce'i käitusaja (CRT), riistvarajaama ja müügikoha (KASSA) laiendustest. Selle proovi käitamiseks peate muutma ja ehitama CRT, riistvarajaama ja kassaprojekte. Soovitame selles teemas kirjeldatud muudatuste tegemiseks kasutada modifitseerimata Retail SDK-d. Samuti soovitame kasutada allika juhtimissüsteemi, näiteks Azure DevOps kui ühtegi faili pole veel muudetud.

## <a name="development-environment"></a>Arenduskeskkonnad

Arengukeskkonna seadistamiseks järgige neid juhiseid, et saaksite proovi testida ja pikendada.

### <a name="enable-crt-extensions"></a>Laienduste lubamine CRT

Laienduskomponendid CRT sisalduvad proovides CRT. Järgmiste protseduuride lõpuleviimiseks avage  **CommerceRuntimeSamples.sln** lahendus jaotises **RetailSdk\\SampleExtensions\\CommerceRuntime**.

#### <a name="documentprovidercleancashsample-component"></a>DocumentProvider.CleanCashSample komponent

1. **Leidke projekt Runtime.Extensions.DocumentProvider.CleanCashSample** ja ehitage see.
2. Leidke kaustast **Runtime.Extensions.DocumentProvider.CleanCashSample\\bin\\Debug** assemblerifail **Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll**.
3. Kopeerige assemblerifail CRT kausta Laiendused.

    - **Commerce Scale Unit:** kopeerige fail internetiteabeteenuste (IIS) Commerce Scale Uniti saidi asukoha all olevasse **\\bin\\ext** kausta.
    - **Kohalik CRT kaasaegses kassas:** kopeerige fail **\\ ext** kausta kohaliku CRT kliendimaakleri asukoha all.

4. Leidke laiendi konfiguratsioonifail:CRT

    - **Commerce Scale Unit:** faili nimi **on commerceruntime.ext.config** ja see asub prügikasti **\\ kaustas** IIS Commerce Scale Unit saidi asukoha all.
    - **Kohalik CRT kaasaegses kassas:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku CRT kliendimaakleri asukoha all.

5. Registreerige CRT laienduse konfiguratsioonifaili muudatus.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    ```

#### <a name="extension-configuration-file"></a>Laienduse konfiguratsioonifail

1. Leidke laiendi konfiguratsioonifail:CRT

    - **Commerce Scale Unit:** faili nimi **on commerceruntime.ext.config** ja see asub prügikasti **\\ kaustas** IIS Commerce Scale Unit saidi asukoha all.
    - **Kohalik CRT kaasaegses kassas:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku CRT kliendimaakleri asukoha all.

2. Registreerige CRT laienduse konfiguratsioonifaili muudatus.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

### <a name="enable-hardware-station-extensions"></a>Riistvarajaama laienduste lubamine

Riistvarajaama laienduse komponendid sisalduvad riistvarajaama näidistes. Järgmiste protseduuride lõpuleviimiseks avage **HardwareStationSamples.sln** lahendus jaotises **RetailSdk\\SampleExtensions\\HardwareStation**.

#### <a name="cleancash-component"></a>CleanCashi komponent

1. **Leidke projekt HardwareStation.Extension.CleanCashSample** ja ehitage see.
2. Otsige kaustast **Extension.CleanCashSample\\bin\\Debug** üles **contoso.Commerce.HardwareStation.CleanCashSample.dll** ja **Interop.CleanCash11\_\_.dll** assemblerifailid.
3. Kopeerige assemblerifailid kausta Riistvarajaama laiendused.

    - **Ühiskasutusega riistvarajaam:** kopeerige failid IIS-i riistvarajaama saidi asukoha all olevasse **prügikasti** kausta.
    - **Spetsiaalne riistvarajaam kaasaegses kassas:** kopeerige failid Kaasaegse kassa kliendimaakleri asukohta.

4. Leidke riistvarajaama laienduste konfiguratsioonifail. Faili nimi **on HardwareStation.Extension.config**.

    - **Jagatud riistvarajaam:** fail asub IIS-i riistvarajaama saidi asukoha all.
    - **Spetsiaalne riistvarajaam Kaasaegses kassas:** fail on kaasaegse kassa kliendimaakleri asukoha all.

5. Lisage konfiguratsioonifaili kompositsioonijaotisse **järgmine** rida.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

### <a name="enable-modern-pos-extension-components"></a>Kaasaegsete kassalaiendi komponentide lubamine

1. **Avage rakenduses RetailSdkPOS** **modernpos.sln\\ lahendus** ja veenduge, et seda saab vigadeta koostada. Lisaks veenduge, et saate käivitada modernse Visual Studio kassa, kasutades **käsku Käivita**.

    > [!NOTE]
    > Kaasaegset kassat ei tohi kohandada. Peate lubama kasutajakonto juhtimise (UAC) ja vajaduse korral desinstallima varem installitud kaasaegse kassa eksemplarid.

2. Lubage laiendused, mis tuleb laadida, lisades faili extensions.json **järgmised** read.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

    > [!NOTE]
    > Lisateavet ja näidiste kohta, mis näitavad lähtekoodi kaustade kaasamist ja laienduste laadimist, leiate projekti Pos.Extensions **readme.md faili juhistest**.

3. Taastage lahendus uuesti.
4. Käivitage siluris kaasaegne müügikoha ja testige funktsionaalsust.

### <a name="enable-cloud-pos-extension-components"></a>Pilveteenuse müügikoha laienduskomponentide lubamine

1. **Avage CloudPOS.sln** lahendus jaotises **RetailSdk\\POS** ja veenduge, et seda saab vigadeta koostada.
2. Lubage laiendused, mis tuleb laadida, lisades faili extensions.json **järgmised** read.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

    > [!NOTE]
    > Lisateavet ja näidiste kohta, mis näitavad lähtekoodi kaustade kaasamist ja laienduste laadimist, leiate projekti Pos.Extensions **readme.md faili juhistest**.

3. Taastage lahendus uuesti.
4. Käivitage lahendus käsu Run **abil** ja järgides rakenduse Retail SDK juhiseid.

## <a name="production-environment"></a>Tootmiskeskkond

Eelmine protseduur võimaldab laiendusi, mis on juhtüksuse integratsioonivalimi komponendid. Lisaks peate järgima neid juhiseid, et luua juurutatavad paketid, mis sisaldavad Commerce'i komponente, ja rakendada need paketid tootmiskeskkonnas.

1. Tehke paketi konfiguratsioonifailides kausta RetailSdkAssets **\\ all** järgmised muudatused.

    - **Lisage konfiguratsioonifailidesse commerceruntime.ext.config** ja **CommerceRuntime.MPOSOffline.Ext.config** kompositsioonijaotisesse **järgmised** read.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
        ```

    - Lisage konfiguratsioonifaili HardwareStation.Extension.config **kompositsioonijaotisesse** **järgmine** rida.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
        ```

2. Tehke kausta BuildTools all **paketi kohandamise konfiguratsioonifailis** Customization.settings **konfiguratsioonifailis** järgmised muudatused.

    - Lisage juurutatavatesse pakettidesse laienduste lisamiseks CRT järgmine rida.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
        ```

    - Lisage juurutatavatesse pakettidesse riistvarajaama laienduse kaasamiseks järgmised read.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
        ```

3. Kassalaiendi lubamine, lisades kausta RetailSDKPOSExtensions faili extensions.json **järgmised** read.**RetailSDK\\POS\\Extensions**

    ``` json
    {
        "extensionPackages": [
            {
            "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

4. Käivitage utiliidi jaoks Visual Studio käsuviip MSBuild ja käivitage **msbuild** kausta Retail SDK all juurutatavate pakettide loomiseks.
5. Rakendage paketid LCS-i kaudu või käsitsi. Lisateavet vt teemast [Create deployable packages](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
6. Täitke kõik vajalikud seadistustoimingud, mida kirjeldatakse jaotises [Juhtüksustega](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units) integreerimise häälestamine.

## <a name="design-of-the-extensions"></a>Laienduste kujundus

### <a name="crt-extension-design"></a>CRT laienduse disain

Finantsdokumendi pakkuja laienduse eesmärk on luua teenusepõhiseid dokumente ja käsitleda juhtüksuse vastuseid.

Laiendus CRT on **Runtime.Extensions.DocumentProvider.CleanCashSample**.

Lisateavet fiskaalintegratsiooni lahenduse kujunduse kohta leiate teemast [Fiskaalne registreerimisprotsess ja fiskaalseadmete ja -teenuste](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) fiskaalintegratsiooni näidised.

#### <a name="request-handler"></a>Taotluse käitleja

Dokumendipakkuja jaoks on üks **documentProviderCleanCashi** päringukäsitleja. Seda käitlejat kasutatakse juhtseadmele rahandusdokumentide loomiseks.

See töötleja on päritud **INamedRequestHandler** liides. **Käitleja nime tagastamise eest vastutab meetod HandlerName**. Käitleja nimi peaks vastama Commerce'i peakontoris määratud konnektori dokumendipakkuja nimele.

Konnektor toetab järgmisi taotlusi.

- **GetFiscalDocumentDocumentProviderRequest** – see taotlus sisaldab teavet selle kohta, milline dokument tuleks luua. See tagastab teenusepõhise dokumendi, mis tuleks juhtseadmes registreerida.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – See päring tagastab tellitavate sündmuste loendi. Praegu toetatakse müügiüritusi ja auditiüritusi.

#### <a name="configuration"></a>Konfiguratsioon

**DocumentProviderFiscalCleanCashSample'i konfiguratsioonifail** asub laiendusprojekti kaustas **Konfiguratsioon**. Selle faili eesmärk on lubada dokumendipakkuja sätete konfigureerimine Commerce'i peakontorist. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetega. Lisatakse järgmised sätted.

- KM-koodide vastendamine

### <a name="hardware-station-extension-design"></a>Riistvarajaama laienduse disain

Fiskaalse konnektori laienduse eesmärk on suhelda juhtseadmega.

Riistvarajaama laiendus on **HardwareStation.Extension.CleanCashSample**. See kasutab HTTP-protokolli, et esitada juhtseadmele dokumente, mille CRT laiendus loob. Samuti tegeleb see juhtseadmelt saadud vastustega.

#### <a name="request-handler"></a>Taotluse käitleja

**CleanCashHandleri** päringukäitleja on juhtseadmele esitatud taotluste käsitlemise sisenemispunkt.

Käitleja on päritud **INamedRequestHandler** liides. **Käitleja nime tagastamise eest vastutab meetod HandlerName**. Töötleja nimi peaks ühtima fiskaalse konnektori nimega, mis on määratud Commerce'i peakorteris.

Konnektor toetab järgmisi taotlusi.

- **SubmitDocumentFiscalDeviceRequest** – See päring saadab dokumendid juhtplokile ja tagastab sealt vastuse.
- **IsReadyFiscalDeviceRequest** – Seda päringut kasutatakse juhtploki tervisekontrolliks.
- **InitializeFiscalDeviceRequest** – Seda päringut kasutatakse juhtseadme lähtestamiseks.

#### <a name="configuration"></a>Konfiguratsioon

Konfiguratsioonifail asub **Seadistamine** laiendusprojekti kaust. Faili eesmärk on lubada fiskaalse konnektori sätteid Commerce'i peakorteris konfigureerida. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetega. Lisatakse järgmised sätted.

- **Ühenduste string** – Juhtseadme ühenduse seaded.
- **Aeg maha** – Aeg millisekundites, mille jooksul juht ootab juhtseadme vastust.

## <a name="migrating-from-the-earlier-integration-sample"></a>Varasemast integratsiooniproovist üleminek

Kui kasutate varasemat [näidis POS-i integreerimiseks juhtseadmetega Rootsi jaoks](retail-sdk-control-unit-sample.md), peate võib-olla sellelt praegusele integratsiooninäidisele üle minema. Muudatuse kasutuselevõtuks ja Rootsi funktsioonide õigeaegsete värskenduste saamiseks tulevikus peate võib-olla uuendama, tegema väiksemaid koodi ja konfiguratsiooni muudatusi loodud laiendustes ning oma lahendusi uuesti ehitama. Teie loodud laiendusloogikas pole suuri muudatusi vaja. Varasem integratsiooninäidis ja teie kohandused töötavad edasi, kui teie poolt muudatusi ei tehta. Seetõttu saate oma keskkonda planeerida, selleks valmistuda ja sellega tegeleda.

### <a name="migration-process"></a>Migratsiooniprotsess

Varasemalt integreerimise valimilt praegusele juhtploki integreerimisvalimile üleminek peaks põhinema järkjärgulise värskendamise kontseptsioonil. Teisisõnu tuleks kõiki Commerce'i peakorteri ja Commerce Scale Unit'i komponente värskendada juba enne POS-i ja riistvarajaama komponentide värskendamist.

Et vältida olukorda, kus sündmus või tehing allkirjastatakse kaks korda (st see on allkirjastatud nii varasema kui ka praeguse laienduse poolt) või kui sündmust või tehingut ei saa allkirjastada puuduva konfiguratsiooni tõttu, soovitame lülitate välja kõik kassa- ja riistvarajaama seadmed, mis kasutavad varasemat näidist, ja seejärel värskendate neid samaaegselt. Seda samaaegset värskendust saab teha näiteks poepõhiselt, uuendades poe funktsionaalsusprofiili ja Riistvarajaama riistvaraprofiili.

Migratsiooniprotsess peaks koosnema järgmistest etappidest.

1. Värskendage Commerce'i peakorteri komponente.
1. Värskendage Commerce Scale Unit komponente ja lubage praeguse näidise laiendused.
1. Veenduge, et kõik võrguühenduseta tehingud oleksid võrguühenduseta MPOS-seadmetest sünkroonitud.
1. Lülitage välja kõik seadmed, mis kasutavad eelmise proovi komponente.
1. Täitke kõik vajalikud seadistustoimingud, mida kirjeldatakse jaotises [Juhtüksustega](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units) integreerimise häälestamine.
1. Värskendage kassa- ja riistvarajaama komponente, keelake laiendused, mis on varasema näidise osad, ja lubage praeguse näidise laiendused.

    > [!NOTE]
    > Olenevalt keskkonna tüübist leiate rohkem tehnilisi üksikasju migratsiooniprotsessi kohta mõlemast [Ränne arenduskeskkonnas](#migration-in-a-development-environment) jaotis või [Ränne tootmiskeskkonnas](#migration-in-a-production-environment) selle teema osa.

### <a name="migration-in-a-development-environment"></a>Ränne arenduskeskkonnas

#### <a name="update-crt"></a>Uuenda CRT

1. **Leidke projekt Runtime.Extensions.DocumentProvider.CleanCashSample** ja ehitage see.
2. Leidke kaustast **Runtime.Extensions.DocumentProvider.CleanCashSample\\bin\\Debug** assemblerifail **Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll**.
3. Kopeerige assemblerifail CRT kausta Laiendused.

    - **Commerce Scale Unit:** kopeerige fail **\\bin\\ext** IIS Commerce'i skaala ühiku saidi asukoha all.
    - **Kohalik CRT kaasaegses kassas:** kopeerige fail **\\ ext** kausta kohaliku CRT kliendimaakleri asukoha all.

4. Leidke laiendi konfiguratsioonifail:CRT

    - **Kaubanduse mastaabiüksus:** Failile antakse nimi **CommerceRuntime.ext.config**, ja see asub **prügikast\\ ext** kausta IIS Commerce Scale Unit saidi asukoha all.
    - **Kohalik CRT kaasaegses POS-is:** Failile antakse nimi **CommerceRuntime.MPOSOffline.Ext.config**, ja see asub **prügikast\\ ext** kaust kohaliku all CRT kliendi maakleri asukoht.

    > [!WARNING]
    > Tee **mitte** redigeerige faile CommerceRuntime.config ja CommerceRuntime.MPOSOffline.config. Need failid ei ole mõeldud kohandamiseks.

5. Otsige üles ja eemaldage varasem CRT laiendi konfiguratsioonifailist.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > Ärge viige seda sammu lõpule enne, kui värskendate kõiki sellega töötavaid kassaseadmeid CRT näiteks.

6. Registreerige praegune proov CRT laiendite konfiguratsioonifailis, lisades järgmised read.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

#### <a name="update-hardware-station"></a>Värskendage riistvarajaama

1. **Leidke projekt HardwareStation.Extension.CleanCashSample** ja ehitage see.
2. Otsige kaustast **Extension.CleanCashSample\\bin\\Debug** üles **contoso.Commerce.HardwareStation.CleanCashSample.dll** ja **Interop.CleanCash11\_\_.dll** assemblerifailid.
3. Kopeerige assemblerifailid kausta Riistvarajaama laiendused.

    - **Ühiskasutusega riistvarajaam:** kopeerige failid IIS-i riistvarajaama saidi asukoha all olevasse **prügikasti** kausta.
    - **Spetsiaalne riistvarajaam kaasaegses kassas:** kopeerige failid Kaasaegse kassa kliendimaakleri asukohta.

4. Otsige üles **HardwareStation.Extension.config** laiendi konfiguratsioonifail:

    - **Kaugriistvarajaam:** Fail asub IIS-i riistvarajaama saidi asukoha all.
    - **Kohalik riistvarajaam kaasaegses POS-is:** Fail asub Modern POS-kliendi maakleri asukoha all.

    > [!WARNING]
    > Tee **mitte** redigeerige faile CommerceRuntime.config ja CommerceRuntime.MPOSOffline.config. Need failid ei ole mõeldud kohandamiseks.

5. Otsige üles ja eemaldage laienduse konfiguratsioonifailist varasem riistvarajaama laiendus.

    # <a name="retail-73-and-earlier"></a>[Jaemüük 7.3 ja varasemad](#tab/retail-7-3)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[Jaemüük 7.3.1 ja uuemad](#tab/retail-7-3-1)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[Jaemüük 10.0 ja uuemad](#tab/retail-10-0)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---

6. Lisage järgmine rida **koostis** laiendi konfiguratsioonifaili jaotises.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

#### <a name="update-modern-pos"></a>Värskendage kaasaegset POS-i

1. Ava **CloudPOS.sln** lahendus all **RetailSdk\\ POS**.
2. Keelake varasem POS-laiendus, eemaldades loendist järgmised read **extensions.json** faili.

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. Lubage praegune näidis POS-laiend, lisades järgmised read **extensions.json** faili.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="update-cloud-pos"></a>Värskendage Cloud POS-i

1. Ava **ModernPOS.sln** lahendus all **RetailSdk\\ POS**.
2. Keelake varasem POS-laiendus, eemaldades loendist järgmised read **extensions.json** faili.

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. Lubage praegune näidis POS-laiend, lisades järgmised read **extensions.json** faili.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

### <a name="migration-in-a-production-environment"></a>Ränne tootmiskeskkonnas

#### <a name="update-crt"></a>Uuenda CRT

1. Eemaldage varasem CRT laiendus alates **CommerceRuntime.ext.config** ja **CommerceRuntime.MPOSOffline.Ext.config** konfiguratsioonifailid all **RetailSdk\\ Varad** kausta.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > Ärge viige seda sammu lõpule enne, kui värskendate kõiki sellega töötavaid kassaseadmeid CRT näiteks.

2. Luba praegune näidis CRT laiendusi, tehes rakenduses järgmised muudatused **CommerceRuntime.ext.config** ja **CommerceRuntime.MPOSOffline.Ext.config** konfiguratsioonifailid all **RetailSdk\\ Varad** kausta.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

3. Aastal **Kohandamine.seaded** paketi kohandamise konfiguratsioonifaili all **Ehitustööriistad** kausta, lisage praeguse näidise kaasamiseks järgmine rida CRT laiendus juurutatavates pakettides.

    ``` xml
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
    ```

#### <a name="update-hardware-station"></a>Värskendage riistvarajaama

1. Eemaldage varasem riistvarajaama laiendus, muutes faili **HardwareStation.Extension.config** konfiguratsioonifail.

    # <a name="retail-73-and-earlier"></a>[Jaemüük 7.3 ja varasemad](#tab/retail-7-3)

    Eemaldage jaotisest järgmine jaotis **HardwareStation.Shared.config** ja **HardwareStation.Dedicated.config** konfiguratsioonifailid.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[Jaemüük 7.3.1 ja uuemad](#tab/retail-7-3-1)

    Eemaldage jaotisest järgmine jaotis **HardwareStation.Extension.config** konfiguratsioonifail.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[Jaemüük 10.0 ja uuemad](#tab/retail-10-0)

    Eemaldage jaotisest järgmine jaotis **HardwareStation.Extension.config** konfiguratsioonifail.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---

2. Lubage praegune näidisriistvarajaama laiendus, lisades järgmise rea **koostis** jaotises **HardwareStation.Extension.config** konfiguratsioonifail.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

3. Tehke kausta BuildTools all **paketi kohandamise konfiguratsioonifailis** Customization.settings **konfiguratsioonifailis** järgmised muudatused.

    - Eemaldage järgmine rida, et välistada juurutatavatest pakettidest varasem riistvarajaama laiendus.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample.dll" />
        ```

    - Lisage järgmised read, et lisada juurutatavatesse pakettidesse praegune riistvarajaama laienduse näidis.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
        ```

#### <a name="update-modern-pos"></a>Värskendage kaasaegset POS-i

1. Ava **CloudPOS.sln** lahendus juures **RetailSdk\\ POS**.
2. Keela varasem POS-laiendus:

    - Aastal **tsconfig.json** faili, lisage **FiscalRegisterSample** kausta välistamisloendisse.
    - Eemaldage järgmised read **extensions.json** faili all **JaemüügiSDK\\ POS\\ Laiendused** kausta.

        ``` json
        {
            "baseUrl": "FiscalRegisterSample"
        }
        ```

3. Lubage praegune näidis POS-laiend, lisades järgmised read **extensions.json** faili all **JaemüügiSDK\\ POS\\ Laiendused** kausta.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="update-cloud-pos"></a>Värskendage Cloud POS-i

1. Ava **ModernPOS.sln** lahendus all **RetailSdk\\ POS**.
2. Keela varasem POS-laiendus:

    - Aastal **tsconfig.json** faili, lisage **FiscalRegisterSample** kausta välistamisloendisse.
    - Eemaldage järgmised read **extensions.json** faili all **JaemüügiSDK\\ POS\\ Laiendused** kausta.

        ``` json
        {
            "baseUrl": "FiscalRegisterSample"
        }
        ```

3. Lubage praegune näidis POS-laiend, lisades järgmised read **extensions.json** faili all **JaemüügiSDK\\ POS\\ Laiendused** kausta.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="create-deployable-packages"></a>Juurutatavate pakettide loomine

Jookse **msbuild** kogu jaemüügi SDK jaoks juurutavate pakettide loomiseks. Rakendage paketid LCS-i kaudu või käsitsi. Lisateabe saamiseks vt [Jaemüügi SDK pakend](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
