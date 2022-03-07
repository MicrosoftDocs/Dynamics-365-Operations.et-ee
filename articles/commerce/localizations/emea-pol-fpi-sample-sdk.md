---
title: Fiskaalprinteri integratsiooni näidise juurutuse juhised Poola jaoks (pärand)
description: Selles teemas antakse juhised fiskaalprinteri integreerimisnäidi juurutamiseks Poola jaoks Microsoft Dynamics 365 Commerce jaemüügi tarkvara arenduskomplektist (SDK).
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: bff3a6ad74d50e7b706d4df92b17a4a3af36521b
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944811"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-poland-legacy"></a>Fiskaalprinteri integratsiooni näidise juurutuse juhised Poola jaoks (pärand)

[!include[banner](../includes/banner.md)]

Selles teemas antakse juhised, kuidas juurutada Fiskaalprinteri integreerimisnäidik Poola jaoks jaemüügi tarkvara arenduskomplektist (SDK) arendaja virtuaalmasinasse Microsoft Dynamics 365 Commerce (VM) Microsoft Dynamics elutsükli teenustes (LCS). Lisateavet selle fiskaalintegratsiooni näidiste kohta vt Poola [fiskaalprinteri integratsiooni näidist](emea-pol-fpi-sample.md). 

Poola fiskaalintegratsiooni näidis on jaemüügi SDK osa. Lisateavet selle kohta, kuidas installida ja kasutada SDK-d, vt [jaemüügi tarkvara arenduskomplekti (SDK) ülesehitust](../dev-itpro/retail-sdk/retail-sdk-overview.md). See näidis koosneb Commerce Runtime' CRT () ja riistvarajaama laiendustest. Selle näidisprojekti käivitamiseks peate muutma ja ehitama CRT riistvarajaama projekte. Selles teemas kirjeldatud muudatuste vaatamiseks on soovitatav kasutada jaemüügi SDK-d, mida pole võimalik muuta. Soovitame kasutada ka allikakontrollisüsteemi, näiteks Azure DevOps sellistena, kus faile pole veel muudetud.

## <a name="development-environment"></a>Arenduskeskkonnad

Järgige neid samme arenduskeskkonna häälestamiseks, et saate testida ja laiendada näidist.

### <a name="commerce-runtime-extension-components"></a>Äri käitusaja laienduse komponendid

CRT Laienduskomponendid on kaasatud retail SDK-sse. Järgmiste protseduuride lõpule viimiseks avage **CommerceRuntimeSamples.sln lahendus** **retailSdk \\ SampleExtensions \\ CommerceRuntime'i** all.

1. Leidke projekt **Runtime.Extensions.DocumentProvider.PosnetSample** ja koostage see.
2. Leidke **kaustast Extensions.DocumentProvider.PosnetSample \\ bin \\ Silumine** **contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll** assemblerifail.
3. Kopeerige assemblerifail CRT laienduskausta:

    - **Commerce Scale Unit:** kopeerige fail **\\ bin \\ ext kausta** teenuse Internet Information Services (IIS) Commerce Scale Unit saidi asukoha all.
    - **Kohalik CRT modern POS-s:** kopeerige fail kohaliku kliendi **\\** maakleri asukoha ext-kausta. CRT

4. Leidke laiendi CRT konfiguratsioonifail:

    - **Commerce Scale Unit: faili nimi on** **commerceruntime.ext.config ja see on IIS Commerce Scale Uniti saidi asukoha** bin **\\** ext-kaustas.
    - **Modern CRT POS-is kohalik: faili nimi on** **CommerceRuntime.MPOSOffline.Ext.config ja see on kohaliku kliendi** maakleri CRT asukoha all.

5. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
    ```

6. Taaskäivitage Commerce Service:

    - **Commerce Scale Unit:** taaskäivitage Commerce Service'i sait IIS-i halduri kaudu.
    - **Kliendi** maakler: **lõpetage dllhost.exe** protsess ülesandehalduris ja taaskäivitage Modern POS.

### <a name="hardware-station-extension-components"></a>Riistvarajaama laienduse komponendid

Riistvarajaama laienduse komponendid on kaasatud Jaemüügi SDK-sse. Järgmiste protseduuride sooritamiseks **avage** **RetailSdk \\ SampleExtensions \\ HardwareStationis konfiguratsioonilahendus HardwareStationSamples.sln.**

1. Leidke **projekt HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample ja** koostage see.
2. Leidke kaustast **Extension.Posnet.UuendavFiscalPrinterSample \\ bin \\ Silumine** assemblerifail **Contoso.Commerce.HardwareStation.PosnetThermalFFiscalPrinterSample.dll.**
3. Kopeerige assemblerifail juurutatud riistvarajaama arvutisse:

    - **Kaug riistvarajaam:** kopeerige fail **IIS**-i riistvarajaama saidi asukoha bin-kausta. Kopeerige printeri draiveriteegid (**libposcmbth.dll**, **libcmbth\_serial.dll** ja **cmbth\_pl.lng**).

4. Leidke riistvarajaama laienduste konfiguratsioonifail. Faili nimi on **HardwareStation.Extension.config:**

    - **Kaug** riistvarajaam: fail asub IIS-i riistvarajaama asukoha all.

5. Lisage konfiguratsioonifaili **koostise** jaotisse järgmine rida.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
    ```

6. Taaskäivitage riistvarajaama teenus:

    - **Kaug riistvarajaam:** taaskäivitage riistvarajaama sait IIS-i haldurist.

## <a name="production-environment"></a>Tootmiskeskkond

Eelmises protseduuris lubate laiendused, mis on fiskaalregistreerimise teenuse integratsiooni näidiskomponendid. Lisaks peate järgima neid samme Commerce'i komponente sisaldavate juurutatavate pakendite loomiseks ja nende pakendite rakendamiseks tootmiskeskkonnas.

1. Tehke paketi konfiguratsioonifailides kausta **RetailSdk Assets all järgmised \\** muudatused:

    - **Commerceruntime.ext.config ja** **CommerceRuntime.MPOSOffline.Ext.config konfiguratsioonifailides lisage koostise** jaotisele **järgmine** rida.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
        ```

    - **Konfiguratsioonifailis HardwareStation.Extension.config** lisage koostise jaotisele **järgmine** rida.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
        ```

1. Tehke kausta **BuildTools all kohanduspaketi** kohandamise konfiguratsioonifailis **järgmised** muudatused:

    - Lisage järgmine rida, et kaasata CRT laiend juurutatavatesse pakettidesse.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll"/>
        ```

    - Lisage järgmine rida, et kaasata riistvarajaama laiend juurutatavatesse pakendisse.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll"/>
        ```

1. Käivitage rakenduse MSBuild käsuviip utiliidi jaoks ja käivitage Visual Studio **msbuild kausta** Retail SDK all juurutatavate pakettide loomiseks.
1. Rakendage pakendid LCS-i kaudu või käsitsi. Lisateavet vt teemast [Juurutatavate pakendite](../dev-itpro/retail-sdk/retail-sdk-packaging.md) loomine.

## <a name="design-of-extensions"></a>Laienduste kujundus

Poola fiskaalprinteri integratsiooni näidis põhineb [fiskaalintegratsiooni](fiscal-integration-for-retail-channel.md) funktsioonil. Lisateavet fiskaalintegratsiooni lahenduse kujunduse kohta vt [fiskaalintegratsiooni näidiskujunduse](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) ülevaatest.

### <a name="commerce-runtime-extension-design"></a>Äri käitusaja laiendi kujundus

Fiskaaldokumendi pakkujaks olemise laiend on luua printeripõhiseid dokumente ja käsitleda fiskaalprinteri vastuseid.

Laiend CRT on **Runtime.Extensions.DocumentProvider.PosnetSample.** See laiend loob Printerispetsiifiliste käskude komplekti JavaScripti objekti notationi (JSON) vormingus, mille on määranud POSNET-i spetsifikatsioon 19-3678.

Lisateavet fiskaalintegratsiooni lahenduse kujunduse kohta vt [fiskaalregistreerimise protsessist ja fiskaalseadmete fiskaalintegratsiooni](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) näidised.

#### <a name="request-handler"></a>Nõudeohjur

**DocumentProviderPosnetProtocol** taotluseohjur on fiskaalprinterist dokumentide loomise nõude sisenemispunkt.

Ohjur pärineb **INamedRequestHandler** liideselt. Meetod **HandlerName** vastutab ohjuri nime tagastamise eest. Ohjuri nimi peab vastama Commerce Headquartersis määratud konnektori dokumendi pakkuja nimele.

Konnektor toetab järgmisi taotlusi:

- **GetFiscalDocumentDocumentProviderRequest** – see taotlus sisaldab teavet selle kohta, milline dokument tuleks luua. See tagastab printeripõhise dokumendi, mis tuleb registreerida fiskaalprinteris.
- **GetSupportedRegistrableEventsDocumentProviderRequest – see taotlus tagastab** tellitavate sündmuste loendi. Praegu toetatakse järgmisi sündmusi: müük, X-aruande printimine ja Z-aruande printimine.

#### <a name="configuration"></a>Konfiguratsioon

Konfiguratsioonifail asub **laiendusprojekti** konfiguratsioonikaustas. Faili eesmärk on lubada dokumendipakkuja sätted rakendusest Commerce headquarters konfigureerimist. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetele. Lisatakse järgmised sätted:

- KM-määrade vastendamine
- Maksevahendi tüübi vastendamine
- Deposiitmakse tüüp

### <a name="hardware-station-extension-design"></a>Riistvarajaama laienduse kujundus

Fiskaalühenduseks olemise laiendi eesmärgiks on side fiskaalprinteriga.

Riistvarajaama laiend on **HardwareStation.Extension.PosnetThermalFFiscalPrinterSample.** See laiend kutsub POSNET-i draiveri funktsioone esitama käske, mida CRT laiend fiskaalprinterile loob. Samuti käsitletakse selles seadme tõrkeid.

#### <a name="request-handler"></a>Nõudeohjur

**FiscalPrinterHandler** taotluseohjur on sisenemispunkt fiskaalseadme perifeerseadme taotluse käsitlemiseks.

Ohjur pärineb **INamedRequestHandler** liideselt. Meetod **HandlerName** vastutab ohjuri nime tagastamise eest. Ohjuri nimi peab ühtima Commerce Headquartersis määratud fiskaalühenduse nimega.

Konnektor toetab järgmisi taotlusi:

- **SubmitDocumentFiscalDeviceRequest – see taotlus saadab dokumendid printerisse ja** tagastab vastuse fiskaalprinterist.
- **IsReadyFiscalDeviceRequest** – seda taotlust kasutatakse seadme seisundikontrolliks.
- **InitializeFiscalDeviceRequest** – seda taotlust kasutatakse printeri lähtestamiseks.

#### <a name="configuration"></a>Konfiguratsioon

Konfiguratsioonifail asub **laiendusprojekti** konfiguratsioonikaustas. Faili eesmärk on lubada ühenduse sätete konfigureerimine rakendusest Commerce headquarters. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetele. Lisatakse järgmised sätted:

- **Ühendusstring** – string, mis kirjeldab seadmega ühenduse üksikasju vormingus, mida draiver toetab. Lisateavet vt POSNET-i draiveri dokumentatsioonist.
- **Kuupäeva ja kellaaja sünkroonimine – väärtus, mis määrab, kas printeri kuupäev ja kellaaeg tuleb** sünkroonida ühendatud riistvarajaamaga.
- **Seadme** ajalõpp – aja hulk millisekundites, mille juht ootab seadmelt vastuse ootamist. Lisateavet vt POSNET-i draiveri dokumentatsioonist.
