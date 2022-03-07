---
title: Fiskaalprinteri integratsiooni näidise juurutuse juhised Itaalia jaoks (pärand)
description: See teema annab juhised fiskaalprinteri integreerimise näidiste juurutamiseks Itaalia jaoks jaemüügi Microsoft Dynamics 365 Commerce tarkvara arenduskomplektist (SDK).
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: a7b5f4f042aa5457ff33e9762f0902c5c72f5921
ms.sourcegitcommit: 0d2de52e12fdb9928556d37a4813a67b303695dc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/21/2021
ms.locfileid: "7944836"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-italy-legacy"></a>Fiskaalprinteri integratsiooni näidise juurutuse juhised Itaalia jaoks (pärand)

[!include[banner](../includes/banner.md)]

See teema annab juhised fiskaalprinteri integreerimise näidiste juurutamiseks Itaalia jaoks jaemüügi tarkvara arenduskomplektist (SDK) arendaja virtuaalmasinasse (VM) elutsükli Microsoft Dynamics 365 Commerce Microsoft Dynamics teenustes (LCS). Lisateavet fiskaalintegratsiooni näidiste kohta vt Itaalia [fiskaalprinteri integratsiooni näidist](emea-ita-fpi-sample.md). 

Itaalia fiskaalintegratsiooni näidis on jaemüügi SDK osa. Lisateavet selle kohta, kuidas installida ja kasutada SDK-d, vt [jaemüügi tarkvara arenduskomplekti (SDK) ülesehitust](../dev-itpro/retail-sdk/retail-sdk-overview.md). See näidis koosneb Commerce Runtime' CRT () ja riistvarajaama laiendustest. Selle näidisprojekti käivitamiseks peate muutma ja ehitama CRT riistvarajaama projekte. Selles teemas kirjeldatud muudatuste vaatamiseks on soovitatav kasutada jaemüügi SDK-d, mida pole võimalik muuta. Soovitame kasutada ka allikakontrollisüsteemi, näiteks Azure DevOps sellistena, kus faile pole veel muudetud.

## <a name="development-environment"></a>Arenduskeskkonnad

Järgige neid samme arenduskeskkonna häälestamiseks, et saate testida ja laiendada näidist.

### <a name="commerce-runtime-extension-components"></a>Äri käitusaja laienduse komponendid

CRT Laienduskomponendid on kaasatud retail SDK-sse. Järgmiste protseduuride lõpule viimiseks avage **CommerceRuntimeSamples.sln lahendus** **retailSdk \\ SampleExtensions \\ CommerceRuntime'i** all.

1. Leidke **projekt Runtime.Extensions.DocumentProvider.EpsonFP90IIISample ja** koostage see.
2. Leidke **kaustast Extensions.DocumentProvider.EpsonFP90IIISample bin Debug find \\\\ the** **Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll** assemblerfail.
3. Kopeerige assemblerifail CRT laiendite kausta:

    - **Commerce Scale Unit:** kopeerige fail **\\ bin \\ ext kausta** teenuse Internet Information Services (IIS) Commerce Scale Unit saidi asukoha all.
    - **Kohalik CRT modern POS-s:** kopeerige fail kohaliku kliendi **\\** maakleri asukoha ext-kausta. CRT

4. Leidke laiendi CRT konfiguratsioonifail:

    - **Commerce Scale Unit: faili nimi on** **commerceruntime.ext.config ja see on IIS Commerce Scale Uniti saidi asukoha** bin **\\** ext-kaustas.
    - **Modern CRT POS-is kohalik: faili nimi on** **CommerceRuntime.MPOSOffline.Ext.config ja see on kohaliku kliendi** maakleri CRT asukoha all.

5. Registreerige CRT muudatus laiendi konfiguratsioonifailis.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
    ```

6. Taaskäivitage Commerce Scale Unit:

    - **Commerce Scale Unit:** taaskäivitage Commerce Scale Uniti sait IIS-i halduri kaudu.
    - **Kliendi** maakler: **lõpetage dllhost.exe** protsess ülesandehalduris ja taaskäivitage Modern POS.

### <a name="hardware-station-extension-components"></a>Riistvarajaama laienduse komponendid

Riistvarajaama laienduse komponendid on kaasatud Jaemüügi SDK-sse. Järgmiste protseduuride sooritamiseks **avage** **RetailSdk \\ SampleExtensions \\ HardwareStationis konfiguratsioonilahendus HardwareStationSamples.sln.**

1. Leidke **projekt HardwareStation.Extensions.EpsonFP90IIIFiscalDeviceSample ja** koostage see.
2. Leidke **kaustast Extensions.EpsonFP90IIIFiscalDeviceSample bin Silumine assemblerifail \\\\** **Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll.**
3. Kopeerige assemblerifail juurutatud riistvarajaama arvutisse:

    - **Kaug riistvarajaam:** kopeerige fail **IIS**-i riistvarajaama saidi asukoha bin-kausta.
    - **Kohalik riistvarajaam:** kopeerige fail Modern POS-i kliendi maakleri asukohta.

4. Leidke riistvarajaama laienduste konfiguratsioonifail. Faili nimi on **HardwareStation.Extension.config:**

    - **Kaug** riistvarajaam: fail asub IIS-i riistvarajaama asukoha all.
    - **Kohalik riistvarajaam:** fail asub Modern POS-i kliendi maakleri asukoha all.

5. Lisage konfiguratsioonifaili **koostise** jaotisse järgmine jaotis.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
    ```

6. Taaskäivitage riistvarajaama teenus:

    - **Kaug riistvarajaam:** taaskäivitage riistvarajaama sait IIS-i haldurist.
    - **Kohalik riistvarajaam:** lõpetage **protsess dllhost.exe** ülesandehalduris ja taaskäivitage modern POS.

## <a name="production-environment"></a>Tootmiskeskkond

Commerce'i komponente sisaldavate juurutatavate pakendite loomiseks ja nende pakendite rakendamiseks tootmiskeskkonnas järgige neid samme.

1. Viige lõpule selle teema varasemas [teemas kirjeldatud](#development-environment) arenduskeskkonnas kirjeldatud sammud.
2. Tehke paketi konfiguratsioonifailides kausta **RetailSdk Assets all järgmised \\** muudatused:

    - **Commerceruntime.ext.config ja** **CommerceRuntime.MPOSOffline.Ext.config konfiguratsioonifailides lisage koostise** jaotisele **järgmine** rida.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
        ```

    - **Konfiguratsioonifailis HardwareStation.Extension.config** lisage koostise jaotisele **järgmine** rida.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
        ```

3. Tehke kausta **BuildTools all kohanduspaketi** kohandamise konfiguratsioonifailis **järgmised** muudatused:

    - Lisage järgmine rida, et kaasata CRT laiend juurutatavatesse pakettidesse.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll"/>
        ```

    - Lisage järgmine rida, et kaasata riistvarajaama laiend juurutatavatesse pakendisse.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll"/>
        ```

4. Käivitage rakenduse MSBuild käsuviip utiliidi jaoks ja käivitage seejärel juurutatavate pakettide loomiseks Visual Studio **msbuild kausta** Retail SDK all.
5. Rakendage pakendid LCS-i kaudu või käsitsi. Lisateavet vt teemast [Juurutatavate pakendite](../dev-itpro/retail-sdk/retail-sdk-packaging.md) loomine.

## <a name="design-of-extensions"></a>Laienduste kujundus

### <a name="commerce-runtime-extension-design"></a>Äri käitusaja laiendi kujundus

Fiskaaldokumendi pakkujaks olemise laiend on luua printeripõhiseid dokumente ja käsitleda fiskaalprinteri vastuseid.

Laiend CRT on **Runtime.Extensions.DocumentProvider.EpsonFP90IIISample.**

Lisateavet fiskaalintegratsiooni lahenduse kujunduse kohta vt [fiskaalregistreerimise protsessist ja fiskaalseadmete fiskaalintegratsiooni](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices) näidised.

#### <a name="request-handler"></a>Nõudeohjur

**DocumentProviderEpsonFP90III taotluseohjur on fiskaalprinterist** dokumentide loomise nõude sisenemispunkt.

Ohjur pärineb **INamedRequestHandler** liideselt. Meetod **HandlerName** vastutab ohjuri nime tagastamise eest. Ohjuri nimi peab vastama Commerce Headquartersis määratud konnektori dokumendi pakkuja nimele.

Konnektor toetab järgmisi taotlusi:

- **GetFiscalDocumentDocumentProviderRequest** – see taotlus sisaldab teavet selle kohta, milline dokument tuleks luua. See tagastab printeripõhise dokumendi, mis tuleb registreerida fiskaalprinteris.
- **GetSupportedRegistrableEventsDocumentProviderRequest – see taotlus tagastab** tellitavate sündmuste loendi. Praegu toetatakse järgmisi sündmusi: müük, X-aruande printimine ja Z-aruande printimine.

#### <a name="configuration"></a>Konfiguratsioon

Konfiguratsioonifail asub **laiendusprojekti** konfiguratsioonikaustas. Faili eesmärk on lubada dokumendipakkuja sätted rakendusest Commerce headquarters konfigureerimist. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetele. Lisatakse järgmised sätted:

- KM-koodide vastendamine
- KM-määrade vastendamine
- Maksevahendi tüübi vastendamine
- Kviitungi numbri vöötkoodi tüüp
- Deposiitmakse tüüp

### <a name="hardware-station-extension-design"></a>Riistvarajaama laienduse kujundus

Fiskaalühenduseks olemise laiendi eesmärgiks on side fiskaalprinteriga.

Riistvarajaama laiend on **HardwareStation.Extension.EpsonFP90IIIFiscalDeviceSample.** See laiend kasutab HTTP-protokolli, et esitada dokumente, CRT mida laiend fiskaalprinterile loob. Samuti käsitletakse fiskaalprinterilt saadud vastuseid.

#### <a name="request-handler"></a>Nõudeohjur

**EpsonFP90IIISample'i taotluseohjur on fiskaalseadme nõude** käsitlemise sisenemispunkt.

Ohjur pärineb **INamedRequestHandler** liideselt. Meetod **HandlerName** vastutab ohjuri nime tagastamise eest. Ohjuri nimi peab ühtima Commerce Headquartersis määratud fiskaalühenduse nimega.

Konnektor toetab järgmisi taotlusi:

- **SubmitDocumentFiscalDeviceRequest – see taotlus saadab dokumendid printerisse ja** tagastab vastuse fiskaalprinterist.
- **IsReadyFiscalDeviceRequest** – seda taotlust kasutatakse seadme seisundikontrolliks.
- **InitializeFiscalDeviceRequest** – seda taotlust kasutatakse printeri lähtestamiseks.

#### <a name="configuration"></a>Konfiguratsioon

Konfiguratsioonifail asub **laiendusprojekti** konfiguratsioonikaustas. Faili eesmärk on lubada ühenduse sätete konfigureerimine rakendusest Commerce headquarters. Failivorming on joondatud fiskaalintegratsiooni konfiguratsiooni nõuetele. Lisatakse järgmised sätted:

- **Lõpp**-punkti aadress – printeri URL.
- **Kuupäeva ja kellaaja sünkroonimine – väärtus, mis määrab, kas printeri kuupäev ja kellaaeg tuleb** sünkroonida ühendatud riistvarajaamaga.
