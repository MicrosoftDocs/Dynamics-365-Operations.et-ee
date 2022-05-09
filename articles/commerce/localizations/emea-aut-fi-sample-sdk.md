---
title: Fiskaalregistreerimise teenuse integreerimise näidis Austria juurutuse juhised (pärand)
description: See teema annab juhised Austria fiskaalintegratsiooni näidiste juurutamiseks jaemüügi tarkvara Microsoft Dynamics 365 Commerce arenduskomplektist (SDK).
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 7cb0e7b665add397b12e1a841b6a2e9565528d6d
ms.sourcegitcommit: 7faf82fa7ce269c0201abb8473af861ef7ce00bf
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 04/19/2022
ms.locfileid: "8613932"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-austria-legacy"></a>Fiskaalregistreerimise teenuse integreerimise näidis Austria juurutuse juhised (pärand)

[!include [banner](../includes/banner.md)]

See teema annab juhised Austria fiskaalregistreerimise teenuse integreerimise näidiste juurutamiseks jaemüügi Microsoft Dynamics 365 Commerce tarkvara arenduskomplektist (SDK) arendaja virtuaalmasinasse (VM) Microsoft Dynamics elutsükli teenustes (LCS). Lisateavet fiskaalintegratsiooni näidiste kohta vt Austria [fiskaalteenuste integreerimise näidist](emea-aut-fi-sample.md). 

Austria fiskaalintegratsiooni näidis on osa jaemüügi SDK-st. Lisateavet selle kohta, kuidas installida ja kasutada SDK-d, vt jaemüügi [tarkvara arenduskomplekti (SDK) ülesehitust](../dev-itpro/retail-sdk/retail-sdk-overview.md). Fiskaalintegratsiooni näidis koosneb Commerce Runtime'i (CRT), riistvarajaama ja kassa laiendustest. Selle näidisprojekti käivitamiseks peate muutma ja üles ehitada CRT projektid Riistvarajaam ja Müügikoha projektid. Selles teemas kirjeldatud muudatuste vaatamiseks on soovitatav kasutada jaemüügi SDK-d, mida pole võimalik muuta. Soovitame kasutada ka allikakontrollisüsteemi, näiteks sellistena, Azure DevOps kus faile pole veel muudetud.

## <a name="development-environment"></a>Arenduskeskkond

Järgige neid samme arenduskeskkonna häälestamiseks, et saate testida ja laiendada näidist.

### <a name="enable-commerce-runtime-extensions"></a>Luba Äri käitusaja laiendid

Laienduskomponendid CRT kaasatakse näidiste CRT hulka. Järgmiste protseduuride lõpule viimiseks avage CommerceRuntimeSamples.sln **lahendus jaotises RetailSdkSampleExtensionsCommerceRuntime** **\\.\\**

#### <a name="documentproviderefrsample-component"></a>DocumentProvider.EFRSample'i komponent

1. Leidke projekt **Runtime.Extensions.DocumentProvider.EFRSample** ja koostage see.
2. Leidke kaustas **Runtime.Extensions.DocumentProvider.EFRSamplebinDebug\\\\** **contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll** assemblerifail.
3. Kopeerige assemblerifail laiendite CRT kausta:

    - **Commerce Scale Unit:** kopeerige fail **\\ binexti\\** kausta teenuse Internet Information Services (IIS) Commerce Scale Unit saidi asukoha all.
    - **Kohalik CRT modern POS-s:** kopeerige fail kohaliku **\\ kliendi maakleri asukoha ext-kausta** CRT.

4. Leidke laiendi konfiguratsioonifail:CRT

    - **Commerce Scale Unit:** faili nimi **on commerceruntime.ext.config** **ja see on binexti\\** kaustas IIS Commerce Scale Uniti saidi asukoha all.
    - **Modern CRT POS-is kohalik:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku kliendi maakleri CRT asukoha all.

5. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
    ```

#### <a name="documentproviderdatamodelefr-component"></a>DocumentProvider.DataModelEFR komponent

1. Leidke projekt **Runtime.Extensions.DocumentProvider.DataModelEFR** ja koostage see.
2. Leidke kaustast **Runtime.Extensions.DocumentProvider.DataModelEFRbinDebug\\\\** **contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll** assemblerifail.
3. Kopeerige assemblerifail laiendite CRT kausta:

    - **Commerce Scale Unit:** kopeerige fail **\\ binexti\\** kausta IIS Commerce Scale Uniti saidi asukoha all.
    - **Kohalik CRT modern POS-s:** kopeerige fail kohaliku **\\ kliendi maakleri asukoha ext-kausta** CRT.

4. Leidke laiendi konfiguratsioonifail:CRT

    - **Commerce Scale Unit:** faili nimi **on commerceruntime.ext.config** **ja see on binexti\\** kaustas IIS Commerce Scale Uniti saidi asukoha all.
    - **Modern CRT POS-is kohalik:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku kliendi maakleri CRT asukoha all.

5. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
    ```

#### <a name="extension-configuration-file"></a>Laiendi konfiguratsioonifail

1. Leidke laiendi konfiguratsioonifail:CRT

    - **Commerce Scale Unit:** faili nimi **on commerceruntime.ext.config** **ja see on binexti\\** kaustas IIS Commerce Scale Uniti saidi asukoha all.
    - **Modern CRT POS-is kohalik:** faili nimi **on CommerceRuntime.MPOSOffline.Ext.config** ja see on kohaliku kliendi maakleri CRT asukoha all.

2. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsAustria" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventAustria" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.XZReportsAustria" />
    ```

### <a name="enable-fiscal-connector-extensions"></a>Fiskaalühenduse laienduste lubamine

Fiskaalühenduse laiendusi saate lubada riistvarajaamas [või](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station) kassaregistris [...](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network).

#### <a name="enable-hardware-station-extensions"></a>Riistvarajaama laienduste lubamine

Riistvarajaama laienduse komponendid sisalduvad riistvarajaama näidises. Järgmiste protseduuride sooritamiseks avage **lahendus HardwareStationSamples.sln** **jaotises RetailSdkSampleExtensionsHardwareStation\\\\**.

##### <a name="efrsample-component"></a>EFRSample'i komponent

1. Otsige üles **projekt HardwareStation.Extension.EFRSample** ja koostage see.
2. Leidke kaustast **Extension.EFRSamplebinDebug\\\\** järgmised assemblerifailid:

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

Kassa laienduse näidis asub **lahenduste hoidla kaustas srcFiscalIntegrationPosFiscalConnectorSample\\\\**[Dynamics 365 Commerce.](https://github.com/microsoft/Dynamics365Commerce.Solutions/)

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

### <a name="enable-modern-pos-extension-components"></a>Modern POS-i laienduse komponentide lubamine

1. Avage jaotises **RetailSdkPOS ModernPOS.sln** **\\ lahendus** ja veenduge, et seda saab kompileerida tõrgeteta. Lisaks veenduge, et saate Modern POS-i käivitada Visual Studio käsuga **Käivita**.

    > [!NOTE]
    > Tänapäevane kassa ei tohi olla kohandatud. Peate kasutajakonto juhtelemendi (UAC) lubama ja vastavalt vajadusele desinstallima modern POS-i varem installitud eksemplarid.

2. Lubage laienduste laadimine, lisades failile **extensions.json järgmised** read.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.AT"
            }
        ]
    }
    ```

    > [!NOTE]
    > Lisateavet ja näidiseid, mis näitavad lähtekoodi kaustade kaasamist ja laiendite laadimist, leiate readme.md **müügikoha laienduste projekti juhistest**.

3. Saate lahenduse uuesti luua.
4. Käivitage Modern POS siluris ja katsege funktsioone.

### <a name="enable-cloud-pos-extension-components"></a>Pilve kassa laienduse komponentide lubamine

1. Avage jaotises **RetailSdkPOS CloudPOS.sln** **\\ lahendus** ja veenduge, et seda saab kompileerida tõrgeteta.
2. Lubage laienduste laadimine, lisades failile **extensions.json järgmised** read.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.AT"
            }
        ]
    }
    ```

    > [!NOTE]
    > Lisateavet ja näidiseid, mis näitavad lähtekoodi kaustade kaasamist ja laiendite laadimist, leiate readme.md **müügikoha laienduste projekti juhistest**.

3. Saate lahenduse uuesti luua.
4. Käivitage lahendus, kasutades käsku **Käivita** ja järgides Jaemüügi SDK kasutusjuhend.

## <a name="production-environment"></a>Tootmiskeskkond

Eelmine protseduur võimaldab laiendusi, mis on fiskaalregistreerimise teenuse integratsiooni näidise komponendid. Lisaks peate järgima neid samme Commerce'i komponente sisaldavate juurutatavate pakendite loomiseks ja nende pakendite rakendamiseks tootmiskeskkonnas.

1. Tehke paketi konfiguratsioonifailides kausta **RetailSdkAssets all\\ järgmised** muudatused:

    - **Lisage konfiguratsioonifailides commerceruntime.ext.config** **ja CommerceRuntime.MPOSOffline.Ext.config** koostise jaotisele **järgmised** read.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsAustria" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventAustria" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.XZReportsAustria" />
        ```

    - Konfiguratsioonifailis **HardwareStation.Extension.config** lisage koostise jaotisele järgmine **rida**.

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

    - Lisage järgmine rida, et kaasata riistvarajaama laiend juurutatavatesse pakendisse.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

3. Käivitage rakenduse MSBuild käsuviip Visual Studio **utiliidi jaoks ja käivitage msbuild** kausta Retail SDK all juurutatavate pakettide loomiseks.
4. Rakendage pakendid LCS-i kaudu või käsitsi. Lisateavet vt teemast Juurutatavate [pakendite loomine](../dev-itpro/retail-sdk/retail-sdk-packaging.md).
5. Täitke kõik nõutavad seadistustoimingud, mida kirjeldatakse [Austria häälestamise äris](emea-aut-fi-sample.md#set-up-commerce-for-austria).

## <a name="design-of-extensions"></a>Laienduste kujundus

Fiskaalregistreerimisteenuse integreerimise näidis Austria jaoks põhineb fiskaalintegratsiooni [funktsioonil](fiscal-integration-for-retail-channel.md). Lisateavet fiskaalintegratsiooni lahenduse kujunduse kohta vt fiskaalintegratsiooni [näidiskujunduse ülevaatest](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services).

### <a name="commerce-runtime-extension-design"></a>Äri käitusaja laiendi kujundus

Fiskaaldokumendi pakkuja laiendi eesmärk on luua teenusepõhiseid dokumente ja käsitleda fiskaalregistreerimise teenuse vastuseid.

CRT Laiend on **Runtime.Extensions.DocumentProvider.EFRSample**.

#### <a name="request-handler"></a>Nõudeohjur

Dokumendi pakkujatel on kaks nõudeohjureid:

- **DocumentProviderEFRFiscalAUT** – seda ohjurit kasutatakse fiskaaldokumentide loomiseks fiskaalregistreerimise teenusele.
- **DocumentProviderEFRNonFiscalAUT** – seda ohjurit kasutatakse fiskaalregistreerimise teenuse mittefiskaalsete dokumentide loomiseks.

Need ohjurid on päritud **INamedRequestHandler liideselt**. Meetod **HandlerName** vastutab ohjuri nime tagastamise eest. Ohjuri nimi peab vastama Commerce Headquartersis määratud konnektori dokumendi pakkuja nimele.

Konnektor toetab järgmisi taotlusi:

- **GetFiscalDocumentDocumentProviderRequest** – see taotlus sisaldab teavet selle kohta, milline dokument tuleks luua. See tagastab teenusepõhise dokumendi, mis tuleb registreerida fiskaalregistreerimise teenuses.
- **GetNonFiscalDocumentDocumentProviderRequest** – see taotlus sisaldab teavet mittefiskaalse dokumendi genereerimise kohta. See tagastab teenusepõhise dokumendi, mis tuleb registreerida fiskaalregistreerimise teenuses.
- **GetSupportedRegistrableEventsDocumentProviderRequest** – see taotlus tagastab tellitavate sündmuste loendi. Praegu toetatakse järgmisi sündmusi: müük, X-aruande printimine, Z-aruande printimine, kliendikonto deposiitid, kliendi tellimuse deposiitid, auditi sündmused ja mittemüügikanded.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest** – see taotlus tagastab fiskaalregistreerimise teenuse vastuse. See vastus järjestatakse stringi moodustamiseks nii, et see on salvestamiseks valmis.

#### <a name="configuration"></a>Konfiguratsioon

Konfiguratsioonifailid asuvad laiendusprojekti **konfiguratsioonikaustas**:

- **DocumentProviderFiscalEFRSampleAustria** – finantsdokumentide jaoks.
- **DocumentProviderNonFiscalEFRSampleAustria** – mittefiskaalsetele dokumentidele.

Nende failide eesmärk on lubada dokumendipakkuja sätted rakendusest Commerce headquarters konfigureerimist. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetele. Lisatakse järgmine säte:

- KM-määrade vastendamine

### <a name="hardware-station-extension-design"></a>Riistvarajaama laienduse kujundus

Fiskaalühenduse laienduse eesmärk on suhelda fiskaalregistreerimisteenusega. Riistvarajaama laienduse nimi on **HardwareStation.Extension.EFRSample**. See kasutab HTTP- või HTTPS-protokolli, et esitada dokumente, CRT mida laiend fiskaalregistreerimise teenusele loob. Samuti käsitletakse fiskaalregistreerimisteenuselt saadud vastuseid.

#### <a name="request-handler"></a>Nõudeohjur

EFRHandler-i **taotluseohjur** on sisenemispunkt fiskaalregistreerimise teenuse taotluste käsitlemiseks.

Ohjur pärineb INamedRequestHandler **liideselt**. Meetod **HandlerName** vastutab ohjuri nime tagastamise eest. Ohjuri nimi peab ühtima Commerce Headquartersis määratud fiskaalühenduse nimega.

Konnektor toetab järgmisi taotlusi:

- **SubmitDocumentFiscalDeviceRequest** – see taotlus saadab dokumendid fiskaalregistreerimise teenusesse ja tagastab sellelt vastuse.
- **IsReadyFiscalDeviceRequest** – seda taotlust kasutatakse fiskaalregistreerimise teenuse seisundikontrolliks
- **InitializeFiscalDeviceRequest** – seda taotlust kasutatakse fiskaalregistreerimise teenuse lähtestamiseks

#### <a name="configuration"></a>Konfiguratsioon

Konfiguratsioonifail asub laiendusprojekti **konfiguratsioonikaustas**. Faili eesmärk on lubada finantsühenduse sätete konfigureerimist rakendusest Commerce headquarters. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetele. Lisatakse järgmised sätted:

- **Lõpp-punkti** aadress – fiskaalregistreerimise teenuse URL.
- **Ajalõpp** – aja hulk millisekundites, mille juht fiskaalregistreerimise teenusest vastust ootab.

### <a name="pos-fiscal-connector-extension-design"></a>Müügikoha fiskaalkonnektori laienduse kujundus

Kassa fiskaalühenduse laienduse eesmärk on kassast fiskaalregistreerimise teenusega sideühendus. See kasutab side jaoks HTTPS-protokolli.

#### <a name="fiscal-connector-factory"></a>Fiskaalühenduse tehas

Fiskaalühenduse tehas vastendab konnektori nime fiskaalühenduse **rakendusega ja asub failis Pos.ExtensionConnectorsFiscalConnectorFactory.ts\\\\**. Konnektori nimi peab kattuma Commerce Headquartersis määratud fiskaalühenduse nimega.

#### <a name="efr-fiscal-connector"></a>EFR-i fiskaalühendus

EFR-i fiskaalühendus asub **failis Pos.ExtensionConnectorsEfrEfrFiscalConnector.ts\\\\\\**. See juurutab **IFiscalConnectori** liidest, mis toetab järgmisi taotlusi:

- **FiscalRegisterSubmitDocumentClientRequest** – see taotlus saadab dokumendid fiskaalregistreerimise teenusesse ja tagastab sellelt vastuse.
- **FiscalRegisterIsReadyClientRequest** – seda taotlust kasutatakse fiskaalregistreerimise teenuse seisundikontrolliks.
- **FiscalRegisterInitializeClientRequest** – seda taotlust kasutatakse fiskaalregistreerimise teenuse lähtestamiseks.

#### <a name="configuration"></a>Konfiguratsioon

Konfiguratsioonifail asub lahenduste **hoidla kaustas srcFiscalIntegrationEfrConfigtionsConnectors\\\\\\\\**[Dynamics 365 Commerce](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Faili eesmärk on lubada finantsühenduse sätete konfigureerimist rakendusest Commerce headquarters. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetele. Lisatakse järgmised sätted:

- **Lõpp-punkti** aadress – fiskaalregistreerimise teenuse URL.
- **Ajalõpp** – aeg millisekundites, mille konnektor ootab fiskaalregistreerimise teenuselt vastust.
