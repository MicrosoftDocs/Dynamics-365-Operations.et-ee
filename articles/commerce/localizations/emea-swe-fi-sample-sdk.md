---
title: Rootsi kontrollüksuse integratsiooni näidisüksuse juurutuse juhised (pärand)
description: See artikkel annab juhised rootsi kontrollühiku integreerimise näidiste juurutamiseks jaemüügi SDK-st.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 05a49de43282c449c7b99072d8ac3ac4a5f2a67f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870543"
---
# <a name="deployment-guidelines-for-the-control-unit-integration-sample-for-sweden-legacy"></a>Rootsi kontrollüksuse integratsiooni näidisüksuse juurutuse juhised (pärand)

[!include [banner](../includes/banner.md)]

See artikkel annab juhised Rootsi kontrollühiku integreerimise näidiste juurutamiseks jaemüügi tarkvara arenduskomplektist (SDK) arendaja virtuaalmasinas (VM) Microsoft Dynamics elutsükli teenustes (LCS). Lisateavet fiskaalintegratsiooni näidiste kohta vt Rootsi [kontrollüksuse integreerimise näidist](emea-swe-fi-sample.md). 

Rootsi fiskaalintegratsiooni näidis on jaemüügi SDK osa. Lisateavet selle kohta, kuidas installida ja kasutada SDK-d, vt jaemüügi [tarkvara arenduskomplekti (SDK) ülesehitust](../dev-itpro/retail-sdk/retail-sdk-overview.md). See näidis koosneb Commerce'i käitusaja (CRT), riistvarajaama ja kassa laiendustest. Selle näidisprojekti käivitamiseks peate muutma ja üles ehitada CRT projektid Riistvarajaam ja Müügikoha projektid. Soovitame kasutada jaemüügi SDK-d, et teha selles artiklis kirjeldatud muudatused. Soovitame kasutada ka allikakontrollisüsteemi, näiteks sellistena, Azure DevOps kus faile pole veel muudetud.

## <a name="development-environment"></a>Arenduskeskkond

Järgige neid samme arenduskeskkonna häälestamiseks, et saate testida ja laiendada näidist.

### <a name="enable-crt-extensions"></a>Laienduste CRT lubamine

Laienduskomponendid CRT kaasatakse näidiste CRT hulka. Järgmiste protseduuride sooritamiseks avage CommerceRuntimeSamples.sln **lahendus** retailSdk **SampleExtensions\\ CommerceRuntime'i all\\.**

#### <a name="documentprovidercleancashsample-component"></a>DocumentProvider.CleanCashSample komponent

1. Leidke projekt **Runtime.Extensions.DocumentProvider.CleanCashSample** ja koostage see.
2. Leidke kaustast Runtime.Extensions.DocumentProvider.CleanCashSample **bin\\ Silumine\\** contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll **assemblerifail**.
3. Kopeerige assemblerifail laiendite CRT kausta:

    - **Commerce Scale Unit:** kopeerige fail **\\ bin ext\\ kausta** teenuse Internet Information Services (IIS) Commerce Scale Unit saidi asukoha all.
    - **Kohalik CRT modern POS-s:** kopeerige fail kohaliku **\\ kliendi maakleri asukoha ext-kausta** CRT.

4. Leidke laiendi konfiguratsioonifail:CRT

    - **Commerce Scale Unit:** faili nimi **on commerceruntime.ext.config** **\\ ja see on IIS Commerce Scale Uniti saidi asukoha bin ext-kaustas**.
    - **Modern CRT POS-is kohalik:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku kliendi maakleri CRT asukoha all.

5. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    ```

#### <a name="extension-configuration-file"></a>Laiendi konfiguratsioonifail

1. Leidke laiendi konfiguratsioonifail:CRT

    - **Commerce Scale Unit:** faili nimi **on commerceruntime.ext.config** **\\ ja see on IIS Commerce Scale Uniti saidi asukoha bin ext-kaustas**.
    - **Modern CRT POS-is kohalik:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku kliendi maakleri CRT asukoha all.

2. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

### <a name="enable-hardware-station-extensions"></a>Riistvarajaama laienduste lubamine

Riistvarajaama laienduse komponendid sisalduvad riistvarajaama näidises. Järgmiste protseduuride sooritamiseks avage **RetailSdk** SampleExtensions **HardwareStationis\\ konfiguratsioonilahendusHardwareStations.sln \\**.

#### <a name="cleancash-component"></a>CleanCash komponent

1. Leidke projekt **HardwareStation.Extension.CleanCashSample** ja koostage see.
2. **Leidke extension.CleanCashSample\\ bin\\ Silumiskaustas** **Contoso.Commerce.HardwareStation.CleanCashSample.dll** ja **Interop.CleanCash\_ 1\_ 1.dll assemblerifailid**.
3. Kopeerige assemblerifailid riistvarajaama laienduste kausta:

    - **Ühiskasutatav riistvarajaam:** kopeerige failid **IIS-i** riistvarajaama saidi asukoha bin-kausta.
    - **Modern POS-i sihtotstarbeline riistvarajaam:** kopeerige failid Modern POS-i kliendi maakleri asukohta.

4. Leidke riistvarajaama laienduste laiendite konfiguratsioonifail. Faili nimi on **HardwareStation.Extension.config**.

    - **Ühiskasutatav riistvarajaam:** fail asub IIS-i riistvarajaama saidi asukohas.
    - **Modern POS-i sihtotstarbeline riistvarajaam:** fail on Modern POS-i kliendi maakleri asukohas

5. Lisage konfiguratsioonifaili koostise **jaotisse** järgmine rida.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

### <a name="enable-modern-pos-extension-components"></a>Modern POS-i laienduse komponentide lubamine

1. Avage RetailSdk **POS-i all** ModernPOS.slni **\\ lahendus** ja veenduge, et seda saab kompileerida tõrgeteta. Lisaks veenduge, et saate Modern POS-i käivitada Visual Studio käsuga **Käivita**.

    > [!NOTE]
    > Tänapäevane kassa ei tohi olla kohandatud. Peate kasutajakonto juhtelemendi (UAC) lubama ja vastavalt vajadusele desinstallima modern POS-i varem installitud eksemplarid.

2. Lubage laiendid, mis tuleb laadida, lisades failile **extensions.json järgmised** read.

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
    > Lisateavet ja näidiseid, mis näitavad lähtekoodi kaustade kaasamist ja laiendite laadimist, leiate readme.md **müügikoha laienduste projekti juhistest**.

3. Saate lahenduse uuesti luua.
4. Käivitage Modern POS siluris ja katsege funktsioone.

### <a name="enable-cloud-pos-extension-components"></a>Pilve kassa laienduse komponentide lubamine

1. **Avage retailSdk POS-i all** CloudPOS.slni **\\ lahendus** ja veenduge, et seda saab kompileerida tõrgeteta.
2. Lubage laiendid, mis tuleb laadida, lisades failile **extensions.json järgmised** read.

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
    > Lisateavet ja näidiseid, mis näitavad lähtekoodi kaustade kaasamist ja laiendite laadimist, leiate readme.md **müügikoha laienduste projekti juhistest**.

3. Saate lahenduse uuesti luua.
4. Käivitage lahendus, kasutades käsku **Käivita** ja järgides Jaemüügi SDK kasutusjuhend.

## <a name="production-environment"></a>Tootmiskeskkond

Eelmine protseduur võimaldab laiendusi, mis on kontrollühiku integratsiooni näidiskomponendid. Lisaks peate järgima neid samme Commerce'i komponente sisaldavate juurutatavate pakendite loomiseks ja nende pakendite rakendamiseks tootmiskeskkonnas.

1. Tehke paketi konfiguratsioonifailides kausta **RetailSdk Assets\\ all järgmised** muudatused:

    - **Lisage konfiguratsioonifailides commerceruntime.ext.config** **ja CommerceRuntime.MPOSOffline.Ext.config** koostise jaotisele **järgmised** read.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
        ```

    - Konfiguratsioonifailis **HardwareStation.Extension.config** lisage koostise jaotisele järgmine **rida**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
        ```

2. Tehke kausta BuildTools **all** kohanduspaketi **kohandamise konfiguratsioonifailis** järgmised muudatused:

    - Lisage järgmine rida, et kaasata CRT laiendused juurutatavatesse pakendisse.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
        ```

    - Lisage järgmised read, et kaasata riistvarajaama laiend juurutatavatesse pakendisse.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
        ```

3. Lubage müügikoha laiend, lisades järgmised read **faili extensions.json** kausta **RetailSDK\\ POS\\ Extensions** alla.

    ``` json
    {
        "extensionPackages": [
            {
            "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

4. Käivitage rakenduse MSBuild käsuviip Visual Studio **utiliidi jaoks ja käivitage msbuild** kausta Retail SDK all juurutatavate pakettide loomiseks.
5. Rakendage pakendid LCS-i kaudu või käsitsi. Lisateavet vt teemast Juurutatavate [pakendite loomine](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
6. Viige lõpule kõik nõutud seadistustoimingud, mida on kirjeldatud [integratsiooni seadistamisel kontrollüksustega](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units).

## <a name="design-of-the-extensions"></a>Laienduste kujundus

### <a name="crt-extension-design"></a>CRT laiendi kujundus

Fiskaaldokumendi pakkuja laiendi eesmärk on luua teenusepõhiseid dokumente ja käsitseda kontrollüksuse vastuseid.

CRT Laiend on **Runtime.Extensions.DocumentProvider.CleanCashSample**.

Lisateavet fiskaalintegratsiooni lahenduse kujunduse kohta vt fiskaalregistreerimisprotsessist [ja fiskaalseadmete ja -teenuste fiskaalintegratsiooni näidised.](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services)

#### <a name="request-handler"></a>Nõudeohjur

Dokumendipakkuja jaoks on **olemas üks DocumentProviderCleanCash** taotluseohjur. Seda ohjurit kasutatakse finantsdokumentide loomiseks kontrollühiku jaoks.

See ohjur on päritud **INamedRequestHandler liideselt**. Meetod **HandlerName** vastutab ohjuri nime tagastamise eest. Ohjuri nimi peab vastama Commerce Headquartersis määratud konnektori dokumendi pakkuja nimele.

Konnektor toetab järgmisi taotlusi:

- **GetFiscalDocumentDocumentProviderRequest** – see taotlus sisaldab teavet selle kohta, milline dokument tuleks luua. See tagastab teenuseomase dokumendi, mis tuleb registreerida kontrollüksuses.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – see taotlus tagastab tellitavate sündmuste loendi. Praegu toetatakse müügisündmusi ja auditi sündmusi.

#### <a name="configuration"></a>Konfiguratsioon

**Konfiguratsioonifail DocumentProviderFiscalCleanCashSample** on **laiendusprojekti** konfiguratsioonikaustas. Selle faili eesmärk on lubada dokumendipakkuja sätted rakendusest Commerce headquarters konfigureerimist. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetele. Lisatakse järgmised sätted:

- KM-koodide vastendamine

### <a name="hardware-station-extension-design"></a>Riistvarajaama laienduse kujundus

Fiskaalühenduseks olemise laiendi eesmärk on pidada ühendust kontrollüksusega.

Riistvarajaama laiend on **HardwareStation.Extension.CleanCashSample**. See kasutab HTTP-protokolli, et esitada dokumente, CRT mida laiend kontrollüksusele loob. Samuti käsitletakse kontrollüksuselt saadud vastuseid.

#### <a name="request-handler"></a>Nõudeohjur

CleanCashHandler **taotluseohjur** on sisenemispunkt kontrollüksuse käsitsemise taotluste jaoks.

Ohjur pärineb INamedRequestHandler **liideselt**. Meetod **HandlerName** vastutab ohjuri nime tagastamise eest. Ohjuri nimi peab ühtima Commerce Headquartersis määratud fiskaalühenduse nimega.

Konnektor toetab järgmisi taotlusi:

- **SubmitDocumentFiscalDeviceRequest** – see taotlus saadab dokumendid kontrollüksusesse ja tagastab sellelt vastuse.
- **IsReadyFiscalDeviceRequest** – seda taotlust kasutatakse kontrollüksuse seisundikontrolliks.
- **InitializeFiscalDeviceRequest** – seda taotlust kasutatakse kontrollüksuse lähtestamiseks.

#### <a name="configuration"></a>Konfiguratsioon

Konfiguratsioonifail on laiendusprojekti **konfiguratsioonikaustas**. Faili eesmärk on lubada finantsühenduse sätete konfigureerimist rakendusest Commerce headquarters. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetele. Lisatakse järgmised sätted:

- **Ühenduste string** – juhtüksuse ühenduse sätted.
- **Ajalõpp** – aja hulk millisekundites, mille juht ootab kontrollüksuselt vastuse ootamist.

## <a name="migrating-from-the-earlier-integration-sample"></a>Varasemast integratsiooninäidandist migreerimine

Kui kasutate varasemat näidist [kassa integreerimiseks Rootsi kontrollüksustega](retail-sdk-control-unit-sample.md), peate võib-olla sellelt üle kandma praegusele integratsiooni näidisele. Selleks, et uuendada muudatusi ja saada rootsi funktsioonide kohta õigeaegselt värskendusi tulevikus, peate võib-olla uuendama, tegema vähem tähtsaid koodi- ja konfiguratsiooni korrigeerimisi oma loodud laiendustes ja taaslooma oma lahendused. Teie loodud laiendiloogikas pole vajalikke olulisi muudatusi. Varasem integratsiooni näidis ja teie kohandused jätkavad tööd, kui teie poolelt ei ole muudatusi tehtud. Seetõttu saate oma keskkonda planeerida, ette valmistada ja seda kasutada.

### <a name="migration-process"></a>Migreerimisprotsess

Varasema integratsiooninäidi siirded praeguse kontrollüksuse integratsiooni näidisse peaksid põhinema värskendamispõhimõttel. Teiste sõnadega, kõik Commerce headquarters ja Commerce Scale Uniti komponendid tuleb juba uuendada enne, kui alustate kassa ja riistvarajaama komponentide uuendamist.

Et vältida olukorda, kus sündmus või kanne on allkirjastatud kaks korda (st selle on allkirjastanud nii varasem laiend kui ka praegune laiend), või kus sündmust või kannet ei saa puuduva konfiguratsiooni tõttu allkirjastada, on soovitatav lülitada välja kõik kassa ja riistvarajaama seadmed, mis kasutavad varasemat näidist. ja seejärel uuendage neid samaaegselt. Seda samaaegset uuendamist saab teha näiteks kaupluse kaupa, uuendades kaupluse funktsiooniprofiili ja riistvarajaama riistvaraprofiili.

Migreerimisprotsess peaks koosnema järgmistest sammudest.

1. Värskendage Commerce headquartersi komponente.
1. Värskendage Commerce Scale Uniti komponente ja lubage praeguse näidis laiendid.
1. Veenduge, et kõik võrguühenduseta kanded sünkroonitakse ühenduseta lubatud MPOS-seadmetest.
1. Lülitage välja kõik seadmed, mis kasutavad varasema näidiskomponendi komponente.
1. Viige lõpule kõik nõutud seadistustoimingud, mida on kirjeldatud [integratsiooni seadistamisel kontrollüksustega](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units).
1. Uuendage kassa ja riistvarajaama komponente, keelake laiendused, mis on varasema näidis osad, ja lubage praeguse näidis laiendid.

    > [!NOTE]
    > Olenevalt keskkonna tüübist leiate [migratsiooniprotsessi kohta täpsemaid üksikasju kas arenduskeskkonna jaotisest Migreerimine](#migration-in-a-development-environment)[või](#migration-in-a-production-environment) Selle artikli tootmiskeskkonna jaotisest Migreerimine.

### <a name="migration-in-a-development-environment"></a>Migratsioon arenduskeskkonnas

#### <a name="update-crt"></a>Uuenda CRT

1. Leidke projekt **Runtime.Extensions.DocumentProvider.CleanCashSample** ja koostage see.
2. Leidke kaustast Runtime.Extensions.DocumentProvider.CleanCashSample **bin\\ Silumine\\** contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll **assemblerifail**.
3. Kopeerige assemblerifail laiendite CRT kausta:

    - **Commerce Scale Unit:** kopeerige fail **\\ bin ext\\ kausta** IIS Commerce Scale Uniti saidi asukoha all.
    - **Kohalik CRT modern POS-s:** kopeerige fail kohaliku **\\ kliendi maakleri asukoha ext-kausta** CRT.

4. Leidke laiendi konfiguratsioonifail:CRT

    - **Commerce Scale Unit:** faili nimi **on CommerceRuntime.ext.config** **\\ ja see on BIN ext-kaustas** IIS Commerce Scale Uniti saidi asukoha all.
    - **Kohalik CRT modern POS-is:** **faili nimi on CommerceRuntime.MPOSOffline.Ext.config** **\\ ja see on kohaliku kliendi maakleri asukoha bin ext-kaustas.** CRT

    > [!WARNING]
    > Ärge **redigeerige** faile CommerceRuntime.config ja CommerceRuntime.MPOSOffline.config. Need failid ei ole mõeldud kohandamiseks.

5. Otsige ja eemaldage varasem CRT laiend laiendi konfiguratsioonifailist.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > Ärge viige seda sammu lõpule enne, kui värskendate kõik selle eksemplariga töötavad kassaseadmed CRT.

6. Registreerige praegused näidislaiendid CRT laiendi konfiguratsioonifailis, lisades järgmised read.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

#### <a name="update-hardware-station"></a>Riistvarajaama värskendamine

1. Leidke projekt **HardwareStation.Extension.CleanCashSample** ja koostage see.
2. **Leidke extension.CleanCashSample\\ bin\\ Silumiskaustas** **Contoso.Commerce.HardwareStation.CleanCashSample.dll** ja **Interop.CleanCash\_ 1\_ 1.dll assemblerifailid**.
3. Kopeerige assemblerifailid riistvarajaama laienduste kausta:

    - **Ühiskasutatav riistvarajaam:** kopeerige failid **IIS-i** riistvarajaama saidi asukoha bin-kausta.
    - **Modern POS-i sihtotstarbeline riistvarajaam:** kopeerige failid Modern POS-i kliendi maakleri asukohta.

4. **Leidke konfiguratsioonifail HardwareStation.Extension.config**:

    - **Kaug riistvarajaam:** fail asub IIS-i riistvarajaama saidi asukohas.
    - **Modern POS-i kohalik riistvarajaam:** fail on Modern POS-i kliendi maakleri asukohas

    > [!WARNING]
    > Ärge **redigeerige** faile CommerceRuntime.config ja CommerceRuntime.MPOSOffline.config. Need failid ei ole mõeldud kohandamiseks.

5. Otsige ja eemaldage varasema riistvarajaama laiend laiendi konfiguratsioonifailist.

    # <a name="retail-73-and-earlier"></a>[Jaemüügi 7.3 ja varasemad](#tab/retail-7-3)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[Jaemüügi 7.3.1 ja uuem](#tab/retail-7-3-1)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[Jaemüügi 10.0 ja uuem](#tab/retail-10-0)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---

6. Lisage laiendi konfiguratsioonifaili **koostise** jaotisse järgmine rida.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

#### <a name="update-modern-pos"></a>Uuenda tänapäevast kassat

1. **Avage RetailSdk POS-i** all **CloudPOS.sln lahendus\\**.
2. Keelake varasem müügikoha laiend, eemaldades failist **extensions.json järgmised** read.

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. Lubage praegune kassa näidislaiend, lisades failile **extensions.json järgmised** read.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="update-cloud-pos"></a>Värskenda pilve kassa

1. Avage RetailSdk POS-i **all** ModernPOS.sln lahendus **\\.**
2. Keelake varasem müügikoha laiend, eemaldades failist **extensions.json järgmised** read.

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. Lubage praegune kassa näidislaiend, lisades failile **extensions.json järgmised** read.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

### <a name="migration-in-a-production-environment"></a>Migreerimine tootmiskeskkonnas

#### <a name="update-crt"></a>Uuenda CRT

1. Eemaldage varasem CRT laiend CommerceRuntime.ext.config **ja** CommerceRuntime.MPOSOffline.Ext.config **konfiguratsioonifailidest** RetailSdk Assets kaustast **\\.**

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > Ärge viige seda sammu lõpule enne, kui värskendate kõik selle eksemplariga töötavad kassaseadmed CRT.

2. Lubage praegused näidislaiendid CRT, muutes järgmised muudatused kaustades CommerceRuntime.ext.config **ja** CommerceRuntime.MPOSOffline.Ext.config **konfiguratsioonifailid** kausta RetailSdk **Assets\\** all.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

3. **Kausta BuildTools** paketi kohandamise **konfiguratsioonifailis Customization.settings** lisage järgmine rida, et kaasata praegune näidislaiend CRT juurutatavatesse pakettidesse.

    ``` xml
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
    ```

#### <a name="update-hardware-station"></a>Riistvarajaama värskendamine

1. Eemaldage varasem riistvarajaama laiend, muutes **konfiguratsioonifaili HardwareStation.Extension.config**.

    # <a name="retail-73-and-earlier"></a>[Jaemüügi 7.3 ja varasemad](#tab/retail-7-3)

    Eemaldage järgmine jaotis konfiguratsioonifailidest **HardwareStation.Shared.config** ja **HardwareStation.Dedicated.config**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[Jaemüügi 7.3.1 ja uuem](#tab/retail-7-3-1)

    Eemaldage konfiguratsioonifailist **HardwareStation.Extension.config** järgmine jaotis.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[Jaemüügi 10.0 ja uuem](#tab/retail-10-0)

    Eemaldage konfiguratsioonifailist **HardwareStation.Extension.config** järgmine jaotis.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---

2. Lubage praegune riistvarajaama näidislaiend, **·** **lisades järgmise rea konfiguratsioonifaili HardwareStation.Extension.config koostise** jaotisesse.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

3. Tehke kausta BuildTools **all** kohanduspaketi **kohandamise konfiguratsioonifailis** järgmised muudatused:

    - Eemaldage järgmine rida, et välistada varasema riistvarajaama laiend juurutatavatest pakenditest.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample.dll" />
        ```

    - Lisage järgmised read, et kaasata praegune riistvarajaama näidislaiend juurutatavatesse pakettidesse.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
        ```

#### <a name="update-modern-pos"></a>Uuenda tänapäevast kassat

1. **Avage RetailSdk POS-i** **cloudPOS.sln lahendus\\**.
2. Keelake varasem müügikoha laiend:

    - Lisage failis **tsconfig.json** kaust **FiscalRegisterSample** välistamisloendisse.
    - Eemaldage järgmised read failist **extensions.json** kausta **RetailSDK\\ POS\\ extensions all**.

        ``` json
        {
            "baseUrl": "FiscalRegisterSample"
        }
        ```

3. Lubage praegune näidiskassa laiend, lisades **järgmised read faili extensions.json** kausta **RetailSDK\\ POS\\ Extensions** alla.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="update-cloud-pos"></a>Värskenda pilve kassa

1. Avage RetailSdk POS-i **all** ModernPOS.sln lahendus **\\.**
2. Keelake varasem müügikoha laiend:

    - Lisage failis **tsconfig.json** kaust **FiscalRegisterSample** välistamisloendisse.
    - Eemaldage järgmised read failist **extensions.json** kausta **RetailSDK\\ POS\\ extensions all**.

        ``` json
        {
            "baseUrl": "FiscalRegisterSample"
        }
        ```

3. Lubage praegune näidiskassa laiend, lisades **järgmised read faili extensions.json** kausta **RetailSDK\\ POS\\ Extensions** alla.

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

Juurutatavate **pakendite loomiseks käivitage msbuild** kogu Retail SDK jaoks. Rakendage pakendid LCS-i kaudu või käsitsi. Lisateavet vt Jaemüügi [SDK-pakendist](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
