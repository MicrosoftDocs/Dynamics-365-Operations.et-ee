---
title: Fiskaalregistreerimisteenuse integreerimise näidisjuhised Saksamaa jaoks (pärand)
description: See teema annab juhised Saksamaa fiskaalintegratsiooni näidiste juurutamiseks jaemüügi tarkvara Microsoft Dynamics 365 Commerce arenduskomplektist (SDK).
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 51107731090b77e75a0e5a8c91b052d494b452e4
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: MT
ms.contentlocale: et-EE
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944911"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-germany-legacy"></a>Fiskaalregistreerimisteenuse integreerimise näidisjuhised Saksamaa jaoks (pärand)

[!include [banner](../includes/banner.md)]

See teema annab juhised Fiskaalregistreerimise teenuse integreerimise näidiste juurutamiseks Saksamaa jaoks jaemüügi tarkvara arenduskomplektist (SDK) arendaja virtuaalmasinas (VM) elutsükli Microsoft Dynamics 365 Commerce Microsoft Dynamics teenustes (LCS). Lisateavet fiskaalintegratsiooni näidiste kohta vt [Saksamaa fiskaalteenuste integreerimise näidist](emea-deu-fi-sample.md). 

Saksamaa fiskaalintegratsiooni näidis on jaemüügi SDK osa. Lisateavet selle kohta, kuidas installida ja kasutada SDK-d, vt [jaemüügi tarkvara arenduskomplekti (SDK) ülesehitust](../dev-itpro/retail-sdk/retail-sdk-overview.md). See näidis koosneb Commerce Runtime' CRT () ja riistvarajaama laiendustest. Selle näidisprojekti käivitamiseks peate muutma ja ehitama CRT riistvarajaama projekte. Selles teemas kirjeldatud muudatuste vaatamiseks on soovitatav kasutada jaemüügi SDK-d, mida pole võimalik muuta. Soovitame kasutada ka allikakontrollisüsteemi, näiteks Azure DevOps sellistena, kus faile pole veel muudetud.

## <a name="development-environment"></a>Arenduskeskkonnad

Järgige neid samme arenduskeskkonna häälestamiseks, et saate testida ja laiendada näidist.

### <a name="enable-commerce-runtime-extensions"></a>Luba Äri käitusaja laiendid

CRT Laienduskomponendid kaasatakse CRT näidiste hulka. Järgmiste protseduuride lõpule viimiseks avage **CommerceRuntimeSamples.sln lahendus** **retailSdk \\ SampleExtensions \\ CommerceRuntime'i** all.

#### <a name="documentproviderefrsample-component"></a>DocumentProvider.EFRSample'i komponent

1. Leidke projekt **Runtime.Extensions.DocumentProvider.EFRSample** ja koostage see.
2. Leidke kaustast **Runtime.Extensions.DocumentProvider.EFRSample \\ bin \\ Silumine** **Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll** assemblerifail.
3. Kopeerige assemblerifail CRT laiendite kausta:

    - **Commerce Scale Unit:** kopeerige fail **\\ bin \\ ext kausta** teenuse Internet Information Services (IIS) Commerce Scale Unit saidi asukoha all.
    - **Kohalik CRT modern POS-s:** kopeerige fail kohaliku kliendi **\\** maakleri asukoha ext-kausta. CRT

4. Leidke laiendi CRT konfiguratsioonifail:

    - **Commerce Scale Unit: faili nimi on** **commerceruntime.ext.config ja see on IIS Commerce Scale Uniti saidi asukoha** bin **\\** ext-kaustas.
    - **Modern CRT POS-is kohalik: faili nimi on** **CommerceRuntime.MPOSOffline.Ext.config ja see on kohaliku kliendi** maakleri CRT asukoha all.

5. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
    ```

#### <a name="documentproviderdatamodelefr-component"></a>DocumentProvider.DataModelEFR komponent

1. Leidke projekt **Runtime.Extensions.DocumentProvider.DataModelEFR** ja koostage see.
2. Leidke kaustast **Runtime.Extensions.DocumentProvider.DataModelEFR \\ bin \\ Silumine** **Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll** assemblerifail.
3. Kopeerige assemblerifail CRT laiendite kausta:

    - **Commerce Scale Unit:** kopeerige fail **\\ bin \\ ext kausta** IIS Commerce Scale Uniti saidi asukoha all.
    - **Kohalik CRT modern POS-s:** kopeerige fail kohaliku kliendi **\\** maakleri asukoha ext-kausta. CRT

4. Leidke laiendi CRT konfiguratsioonifail:

    - **Commerce Scale Unit: faili nimi on** **commerceruntime.ext.config ja see on IIS Commerce Scale Uniti saidi asukoha** bin **\\** ext-kaustas.
    - **Modern CRT POS-is kohalik: faili nimi on** **CommerceRuntime.MPOSOffline.Ext.config ja see on kohaliku kliendi** maakleri CRT asukoha all.

5. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
    ```

#### <a name="extension-configuration-file"></a>Laiendi konfiguratsioonifail

1. Leidke laiendi CRT konfiguratsioonifail:

    - **Commerce Scale Unit: faili nimi on** **commerceruntime.ext.config ja see on IIS Commerce Scale Uniti saidi asukoha** bin **\\** ext-kaustas.
    - **Modern CRT POS-is kohalik: faili nimi on** **CommerceRuntime.MPOSOffline.Ext.config ja see on kohaliku kliendi** maakleri CRT asukoha all.

2. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsGermany" />
    ```

### <a name="enable-hardware-station-extensions"></a>Riistvarajaama laienduste lubamine

Riistvarajaama laienduse komponendid sisalduvad riistvarajaama näidises. Järgmiste protseduuride sooritamiseks **avage** **RetailSdk \\ SampleExtensions \\ HardwareStationis konfiguratsioonilahendus HardwareStationSamples.sln.**

#### <a name="efrsample-component"></a>EFRSample'i komponent

1. Otsige üles **projekt HardwareStation.Extension.EFRSample** ja koostage see.
2. Leidke **kaustast Extension.EFRSample \\ bin \\** Silumine järgmised assemblerifailid:

    - Contoso.Commerce.HardwareStation.EFRSample.dll
    - Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll

3. Kopeerige assemblerifailid riistvarajaama laienduste kausta:

    - **Ühiskasutatav riistvarajaam:** kopeerige failid **IIS**-i riistvarajaama saidi asukoha bin-kausta.
    - **Modern POS-i sihtotstarbeline riistvarajaam:** kopeerige failid Modern POS-i kliendi maakleri asukohta.

4. Leidke riistvarajaama laienduste laiendite konfiguratsioonifail. Faili nimi on **HardwareStation.Extension.config.**

    - **Ühiskasutatav riistvarajaam:** fail asub IIS-i riistvarajaama saidi asukohas.
    - **Modern POS-i sihtotstarbeline riistvarajaam:** fail asub Modern POS-i kliendi maakleri asukoha all

5. Lisage konfiguratsioonifaili **koostise** jaotisse järgmine rida.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample.dll" />
    ```

### <a name="production-environment"></a>Tootmiskeskkond

Eelmises protseduuris lubate laiendused, mis on fiskaalregistreerimise teenuse integratsiooni näidiskomponendid. Lisaks peate järgima neid samme Commerce'i komponente sisaldavate juurutatavate pakendite loomiseks ja nende pakendite rakendamiseks tootmiskeskkonnas.

1. Tehke paketi konfiguratsioonifailides kausta **RetailSdk Assets all järgmised \\** muudatused:

    - Lisage **konfiguratsioonifailides commerceruntime.ext.config ja** **CommerceRuntime.MPOSOffline.Ext.config koostise** jaotisele **järgmised** read.

        ``` xml
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsGermany" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        ```

    - **Konfiguratsioonifailis HardwareStation.Extension.config** lisage koostise jaotisele järgmised **read**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        ```

2. Tehke kausta **BuildTools all kohanduspaketi** kohandamise konfiguratsioonifailis **järgmised** muudatused:

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

3. Käivitage rakenduse MSBuild käsuviip utiliidi jaoks ja käivitage Visual Studio **msbuild kausta** Retail SDK all juurutatavate pakettide loomiseks.
4. Rakendage pakendid LCS-i kaudu või käsitsi. Lisateavet vt teemast [Juurutatavate pakendite](../dev-itpro/retail-sdk/retail-sdk-packaging.md) loomine.
5. Täitke kõik nõutud seadistustoimingud, mida on kirjeldatud [Saksamaa häälestamisprogrammis.](emea-deu-fi-sample.md#set-up-commerce-for-germany)

## <a name="design-of-extensions"></a>Laienduste kujundus

Fiskaalregistreerimisteenuse integreerimise näidis Saksamaa jaoks põhineb [fiskaalintegratsiooni](fiscal-integration-for-retail-channel.md) funktsioonil. Lisateavet fiskaalintegratsiooni lahenduse kujunduse kohta vt [fiskaalintegratsiooni näidiskujunduse](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) ülevaatest.

### <a name="commerce-runtime-extension-design"></a>Äri käitusaja laiendi kujundus

Fiskaaldokumendi pakkuja laiendi eesmärk on luua teenusepõhiseid dokumente ja käsitleda fiskaalregistreerimise teenuse vastuseid.

Laiend CRT on **Runtime.Extensions.DocumentProvider.EFRSample.** Lisateavet fiskaalintegratsiooni lahenduse kujunduse kohta vt [ärikanalite fiskaalintegratsiooni](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) ülevaadet.

#### <a name="request-handler"></a>Nõudeohjur

Dokumendipakkujal **DocumentProviderEFRFiscalDEU on üks** taotluseohjur. Seda ohjurit kasutatakse fiskaaldokumentide loomiseks fiskaalregistreerimise teenusele. See pärineb **INamedRequestHandler** liideselt. Meetod **HandlerName** vastutab ohjuri nime tagastamise eest. Ohjuri nimi peab vastama Commerce Headquartersis määratud konnektori dokumendi pakkuja nimele.

Konnektor toetab järgmisi taotlusi:

- **GetFiscalDocumentDocumentProviderRequest** – see taotlus sisaldab teavet selle kohta, milline dokument tuleks luua. See tagastab teenusepõhise dokumendi, mis tuleb registreerida fiskaalregistreerimise teenuses.
- **GetFiscalTransactionExtendedDataDocumentProviderRequest – see taotlus tagastab vastuse** koos laiendatud andmetega.

#### <a name="configuration"></a>Konfiguratsioon

**Konfiguratsioonifail DocumentProviderFiscalEFRSampleGermany** asub **laiendusprojekti** konfiguratsioonikaustas. Selle faili eesmärk on lubada dokumendipakkuja sätted rakendusest Commerce headquarters konfigureerimist. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetele.

Lisatakse järgmised sätted:

- **KM-määrade vastendamine – käibemaksukoodide jaoks seadistatud maksu protsendiväärtuste vastendamine fiskaalteenusele saadetud taotlustes** **atribuudi TaxG** (maksugrupp) väärtustega.
- **Maksugrupp kinkekaartide ja deposiitide jaoks – TaxG atribuudi väärtus fiskaalteenusele saadetud taotlustes, mis põhinevad kinkekaarte või** **deposiite** kaasatud toimingutel.
- **Maksevahendi tüübi vastendamine: makseviiside vastendamine** **atribuudi PayG (maksegrupp) väärtustega fiskaalteenusesse** saadetud taotlustes.
- **Käibemaksuvabastuse maksugrupp – atribuudi TaxG väärtus fiskaalteenusele saadetud taotlustes, mis põhinevad maksukohustustest** **vabastatud** toimingutel.
- **Kaasa kliendiandmed – kui see parameeter on sisse lülitatud, sisaldavad rahandusteenuse taotlused klienditeavet, nt nimesid ja aadresse, juhul kui klient lisatakse** kandesse.

### <a name="hardware-station-extension-design"></a>Riistvarajaama laienduse kujundus

Fiskaalühenduseks olemise laiendi eesmärgiks on fiskaalregistreerimise teenusega suhtlemine.

Riistvarajaama laiend **onHardwareStation.Extension.EFRSample.** See kasutab HTTP-protokolli, et esitada dokumente, CRT mida laiend finantsregistreerimise teenusele loob. Samuti käsitletakse fiskaalregistreerimisteenuselt saadud vastuseid.

#### <a name="request-handler"></a>Nõudeohjur

**EFRHandler-i** taotluseohjur on sisenemispunkt fiskaalregistreerimise teenuse taotluste käsitlemiseks. See ohjur on päritud **INamedRequestHandler** liideselt. Meetod **HandlerName** vastutab ohjuri nime tagastamise eest. Ohjuri nimi peab ühtima Commerce Headquartersis määratud fiskaalühenduse nimega.

Konnektor toetab järgmisi taotlusi:

- **SubmitDocumentFiscalDeviceRequest – see taotlus saadab dokumendid fiskaalregistreerimise teenusesse ja** tagastab sellelt vastuse.
- **IsReadyFiscalDeviceRequest – seda taotlust kasutatakse** fiskaalregistreerimise teenuse seisundikontrolliks
- **InitializeFiscalDeviceRequest** – seda taotlust kasutatakse fiskaalregistreerimise teenuse lähtestamiseks

#### <a name="configuration"></a>Konfiguratsioon

Konfiguratsioonifail asub **laiendusprojekti** konfiguratsioonikaustas. Faili eesmärk on lubada finantsühenduse sätete konfigureerimist rakendusest Commerce headquarters. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetele.

Lisatakse järgmised sätted:

- **Lõpp**-punkti aadress – fiskaalregistreerimise teenuse URL.
- **Ajalõpp – aja hulk millisekundites (ms), mille juht ootab** fiskaalregistreerimise teenuselt vastust.
- **Kuva fiskaalregistreerimise teatised – kui see parameeter on sisse lülitatud, kuvatakse** fiskaalteenuse teatised kassas kasutajateadetega.
