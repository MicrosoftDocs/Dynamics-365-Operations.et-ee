---
title: Dynamics 365 Commercei eemaldatud või aegunud funktsioonid
description: See teema kirjeldab funktsioone, mis on eemaldatud või plaanitakse eemaldada Dynamics 365 Commerce'ist.
author: josaw
ms.date: 09/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: b582b8b95fcf2ad45aa1bb49eb5594d30874e0f4
ms.sourcegitcommit: 12e26ef25c492e5032260733b50cd642cbd6164d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/28/2021
ms.locfileid: "7559555"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Dynamics 365 Commercei eemaldatud või aegunud funktsioonid

[!include [banner](../includes/banner.md)]

See teema kirjeldab funktsioone, mis on eemaldatud või plaanitakse eemaldada Dynamics 365 Commerce'ist.

- *Eemaldatud* funktsioon pole tootes enam saadaval.
- *Aegunud* funktsioon ei ole aktiivses arenduses ja vee võidakse tulevases värskenduses eemaldada.

See loend peaks aitama teil neid eemaldusi ja aegumisi oma plaanides arvesse võtta. 

> [!NOTE]
> Üksikasjalikku teavet rakenduse Finance and Operationsi rakenduste objektide kohta leiate teemast [Tehnilise teabe aruanded](/dynamics/s-e/). Saate võrrelda nende aruannete eri versioone, et õppida objektide kohta, mida on igas Finance and Operationsi rakenduste versioonis muudetud või eemaldatud.

## <a name="features-removed-or-deprecated-in-the-commerce-10021-release"></a>Commerce'i väljalaskest 10.0.21 eemaldatud või aegunud funktsioonid

[!include [banner](../includes/preview-banner.md)]

### <a name="overlapping-discounts-handling-setting-in-commerce-parameters"></a>Kattuvate allahindluste käsitlemise säte Commerce'i parameetrites

**Kattuvate allahindluste käsitlemine** säte lehel **Commerce'i parameetrid** on Commerce'i versiooni 10.0.21 väljalaskes aegunud. Commerce'i hinnakujunduse mootor kasutab ühte algoritmi, et määrata kattuvate allahindluste optimaalne kombinatsioon.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | <p>**Kattuvate allahindluste käsitlemise** säte Commerce'i parameetrites reguleerib Commerce'i hinnakujunduse mootori otsinguid ja määrab kattuvate allahindluste optimaalse kombinatsiooni. Praegu pakub see kolme valikut:<p><ul><li> **Parim jõudlus** – See valik kasutab täpsemat heuristilise algoritmi ja [marginaali väärtuse reitingu](../optimal-combination-overlapping-discounts.md) meetodit, et õigeaegselt määrata prioriteedid, hinnata ja määrata parim allahindluskombinatsioon.</li><li>**Tasakaalustatud kalkulatsioon** – Praeguse koodi alusel toimib see valik nagu **Parim jõudlus** suvand. Seetõttu on see põhiliselt topeltvalik.</li><li>**Ammendav arvutamine** – See valik kasutab vana algoritmi, mis läheb hinna arvutamisel läbi kõigist võimalikest allahindluse kombinatsioonidest. Suurte ridade ja kogustega tellimuste puhul võib see valik põhjustada jõudluse probleeme.</li></ul><p>Konfiguratsiooni lihtsustamiseks, jõudluse parandamiseks ja vana algoritmi põhjustatud juhtumite vähendamiseks eemaldame täielikult **Kattuvate allahindluste käsitlemise** sätte ja uuendame Commerce'i hinnakujundusmootori siseloogikat, et see kasutaks nüüd ainult täpsemat algoritmi (st **Parima jõudluse** suvandi algoritmi taga).</p> |
| **Asendatud teise funktsiooniga?**   | Ei. Soovitame, et organisatsioonid, mis kasutavad **Tasakaalustatud arvutuse** või **Ammendava arvutuse** suvandit lülituvad **Parim jõudluse** suvandile enne selle funktsiooni eemaldamist. |
| **Mõjutatud tootealad**         | Hinnad ja allahindlused |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Alates 10.0.21 väljaandest eemaldatakse **Kattuvate allahindluste käsitlemise** säte Commerce'i parameetritest 2022 aasta oktoobris. |

### <a name="retail-sdk-distributed-by-using-lifecycle-services"></a>Teenusega Lifecycle Services jaotatud Retail SDK

Retail SDK saadetakse teenusega Lifecycle Services (LCS). See jaotusviis aegus väljalaskes 10.0.21. Edaspidi avaldatakse Retail SDK viitepaketid, teegid ja näidised GitHub-i avalikus hoidlas.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Retail SDK saadetakse LCS-is. LCS-i protsessi lõpule viimine võtab mõne tunni aega ja protsessi tuleb korrata iga värskenduse puhul. Edaspidi avaldatakse Retail SDK viitepaketid, teegid ja näidised GitHub-i avalikus hoidlas. Laiendinäidiseid ja viitepakette saab hõlpsasti tarbida ning uuendused viiakse lõpuni mõne minuti jooksul. |
| **Asendatud teise funktsiooniga?**   |  [Laadige Retail SDK näidised ja viitepaketid alla teenusest GitHub ja NuGet](../dev-itpro/retail-sdk/sdk-github.md) |
| **Mõjutatud tootealad**         | Retail SDK |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Aegunud: alates väljalaskest 10.0.21 eemaldatakse LCS-i VM-i kaudu saadetav SDK (oktoobris 2022). |

### <a name="retail-deployable-package-and-combined-pos-hardware-station-and-cloud-scale-unit-installers"></a>Retaili juurutatav pakett ja koondkassa, riistvarajaam ning pilvskaalaüksuse installerid

Retaili juurutatavad paketid, mis on loodud rakenduse Retail SDK MSBuild abil, on versioonis 10.0.21 aegunud. Edaspidi kasutage pilvskaalaüksuse (CSU) paketti pilvskaalaüksuse laiendite jaoks (Commerce Runtime, kanali andmebaas, kaugadministreeritava kaubanduse API-d, maksed ja pilvekassa). Kasutage kassa, riistvarajaama ja isehostitud pilvskaalaüksuse puhul ainult laiendusega installereid.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Retaili juurutatav pakett on koondpakett, mis sisaldab täielikku pakettide ja installerite komplekti. See koondpakett muudab juurutuse keerukaks, kuna CSU laiendid lähevad pilvskaalaüksusesse ja installerid juurutatakse kauplustes. Installerid sisaldavad laiendust ja põhitoodet, mis muudab värskendused keeruliseks. Iga täienduse puhul on vaja koodi ühendamist ja paketi loomist. Protsessi hõlbustamiseks eraldatakse nüüd laiendipaketid osadeks, et juurutus ja haldus oleks lihtsamad. Uue lähenemisega eraldatakse laiendid ja põhitoote installerid ning neid saab sõltumatult hooldada ja uuendada ilma koodi ühendamise või ümberpakkimiseta.|
| **Asendatud teise funktsiooniga?**   | CSU laiendid, kassalaiendite installerid, riistvarajaama laienduse installerid |
| **Mõjutatud tootealad**         | Rakenduse Dynamics 365 Commerce laiendus ja juurutamine |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Aegunud: alates väljalaskest 10.0.21 eemaldatakse paketi RetailDeployablePackage juurutamise tugi LCS-is (oktoobris 2022). |

Lisateabe saamiseks vt:

+ [Commerce’i pilvskaalaüksuse (CSU) jaoks eraldi paketi loomine](../dev-itpro/retail-sdk/retail-sdk-packaging.md#generate-a-separate-package-for-commerce-cloud-scale-unit-csu)
+ [Modern POS-i laienduspaketi loomine](../dev-itpro/pos-extension/mpos-extension-packaging.md)
+ [Kassa integreerimine uue riistvaraseadmega](../dev-itpro/hardware-device-extension.md)
+ Koodinäidised
    + [Pilvskaalaüksus](https://github.com/microsoft/Dynamics365Commerce.ScaleUnit)
    + [Kassa, CSU ja riistvarajaam](https://github.com/microsoft/Dynamics365Commerce.InStore)

### <a name="modernpossln-and-cloudpossln-in-the-retail-sdk"></a>ModernPos.Sln ja CloudPOs.sln rakenduses Retail SDK

Kassalaiendi juurutus ModernPos.sln, CloudPOs.sln, POS.Extension.csproj ja kassakausta abil aegus väljalaskes 10.0.21. Edaspidi kasutage kassalaiendite jaoks kassast sõltumatut pakendamise SDK-d.

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Retail SDK varasemates versioonides on kassalaiendite korral vaja kassa uusimale versioonile värskendamiseks koodi ühendamist ja ümberpakkimist. Koodi ühendamine oli aeganõudev täiendusprotsess ja te pidite säilitama täielikku Retail SDK-d hoidlas. Samuti pidite kompileerima tuumprojekti POS.App. Sõltumatu pakendamise mudeli kasutamisel peate hooldama ainult oma laiendust. Kassalaiendite uusimale versioonile uuendamise protsess on sama lihtne, kui teie projekti tarbitava NuGeti paketi versiooni uuendamine. Laiendeid saab juurutada iseseisvalt ja teenused kasutavad laienduse installereid. Põhikassat saab juurutada ja hooldada eraldi ning koodi ühendamist ega ümberpakkimist põhiinstalleri või koodiga pole vaja. |
| **Asendatud teise funktsiooniga?**   | [Kassa sõltumatu pakendamise SDK](../dev-itpro/pos-extension/pos-extension-getting-started.md) |
| **Mõjutatud tootealad**         | Rakenduse Dynamics 365 Commerce kassalaiend ja juurutamine |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Aegunud: alates väljalaskest 10.0.21, eemaldatakse tugi kassa koondpakettidelt ja laiendimudelilt, mis kasutavad rakenduses Retail SDK üksusi ModernPos.Sln, CloudPOs.sln ja POS.Extensons.csproj (oktoobris 2022). |

## <a name="features-removed-or-deprecated-in-the-commerce-10017-release"></a>Commerce'i väljalaskest 10.0.17 eemaldatud või aegunud funktsioonid

### <a name="full-dataset-generation-interval-is-deprecated"></a>Kogu andmekomplekti loomise intervall on iganenud.

|  &nbsp; | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Alates sellest väljalaskest on Dynamics 365 peakontori vormil **Kaubanduse andmeedastaja parameetrid** väli **Kogu andmekomplekti loomise intervall päevades** iganenud. Lisaks on alates sellest väljalaskest väli visuaalselt eemaldatud, nii et väärtust ei saa redigeerida. See jääb väärtuseks **0**. |
| **Asendatud teise funktsiooniga?**   | Ei |
| **Mõjutatud tootealad**         | Dynamics 365 Commerce |
| **Juurutamissuvand**              | Kõik|
| **Olek**                         | Aegunud. Ärge kasutage seda välja ega muutke selle väärtust.|

## <a name="features-removed-or-deprecated-in-the-commerce-10015-release"></a>Commerce'i väljalaskest 10.0.15 eemaldatud või aegunud funktsioonid

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11 Dynamics 365 tugi on iganenud

| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Alates 2020. detsembrist, Microsoft Internet Explorer 11 tugi kõigile Dynamics 365 toodetele on iganenud ja Internet Explorer 11 ei toetata pärast 2021. aasta augustit.<br><br>See mõjutab kliente, kes kasutavad Dynamics 365 tooteid, mis on mõeldud kasutamiseks Internet Explorer 11 liidese kaudu. Pärast 2021. aasta augustit, Internet Explorer 11 ei toetata selliste Dynamics 365 toodete puhul. |
| **Asendatud teise funktsiooniga?**   | Soovitame klientide minna üle Microsoft Edge-le.|
| **Mõjutatud tootealad**         | Kõik Dynamics 365 tooted |
| **Juurutamissuvand**              | Kõik|
| **Olek**                         | Aegunud. Internet Explorer 11 ei toetata pärast 2021. aasta augustit.|

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a>Commerce'i väljalaskest 10.0.11 eemaldatud või aegunud funktsioonid
### <a name="data-action-hooks"></a>Andmetegevuse konksud
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Andmetegevuse konksude funktsioon on jõudlusprobleemide tõttu iganenud. |
| **Asendatud teise funktsiooniga?**   | Soovitatame kasutada andmetegevuse kihis äriloogika muutmiseks [andmetegevuse alistamisi](../e-commerce-extensibility/data-action-overrides.md).|
| **Mõjutatud tootealad**         | e-kaubanduse laiendatavuse andmetegevused |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Iganenud: alates väljaandest 10.0.11 |

### <a name="retail-sdk-support-for-visual-studio-2015-msbuild-140-and-retail-sdkreference-libraries-and-tools"></a>Jaemüügi SDK tugi Visual Studio 2015, msbuild 14.0 ja jaemüügi SDK\viiteteekide ja tööriistade jaoks
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Jaemüügi SDK tugi Visual Studio 2015 jaoks on iganenud ja uuendatud, et toetada VS 2017, msbuild 15.0 ja kõiki viiteteeke ning kaumbanduse puhvrigeneraatori tööriistad kaustas RetailSDK\References on teisaldatud NuGeti pakettidesse, et lihtsustada laienduse mudeli ja SDK värskendamise protsessi.|
| **Asendatud teise funktsiooniga?**   | Soovitame teil süsteemi värskendamiseks järgida teavet teemas [Jaemüügi SDK migreerimine Visual Studio 2015-st Visual Studio 2017-sse](../dev-itpro/retail-sdk/migrate-sdk.md). |
| **Mõjutatud tootealad**         | Jaemüügi SDK laiendused |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Iganenud: alates väljaandest 10.0.11 |

### <a name="retail-server-extension-using-iedmmodelextender-and-commercecontroller"></a>Jaemüügi serveri laiendus, mis kasutab üksusi IEdmModelExtender ja CommerceController
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Jaemüügi serveri laiendus, mis kasutab üksusi IEdmModelExtender ja CommerceController, on iganenud, et pakkuda lihtsustatud laienduse mudelit. Uuel juurutusel on ainult kontrolleri klass, millel puudub täiendav klassi IEdmModelExtender juurutus. See väldib ka sõltuvust konkreetse OData versiooniga (OData versiooni värskendamisel võidakse laiendusi lõhkuda). |
| **Asendatud teise funktsiooniga?**   |  Soovitame kasutada IControlleri klassi laienduse mudelit, importides NuGeti (Microsoft.Dynamics.Commerce.Hosting.Contracts) paketi. |
| **Mõjutatud tootealad**         | Jaemüügi serveri laiendused |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Iganenud: alates väljaandest 10.0.11 |

### <a name="hardware-station-extension-using-ihardwarestationcontroller"></a>Riistvarajaama laiendus, mis kasutab üksust IHardwareStationController
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Riistvarajaama laiendus, mis kasutab üksust IHardwareStationController on iganenud, et pakkuda lihtsustatud laienduse mudelit. Uuel juurutusel on ainult IControlleri klass ilma täiendavate klasside juurutusteta ja põhiriistvara jaamateekidega sõltuvuste vältimiseks pidi laiendus varasemalt viitama mitmele teegile.) |
| **Asendatud teise funktsiooniga?**   | Soovitatav on kasutada IControlleri klassi laienduse mudelit, importides NuGeti (Microsoft.Dynamics.Commerce.Hosting.Contracts) paketi. |
| **Mõjutatud tootealad**         | Riistvarajaama laiendused |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Iganenud: alates väljaandest 10.0.11 |

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a>Commerce'i väljalaskest 10.0.10 eemaldatud või aegunud funktsioonid
### <a name="pos-operation-803---picking-and-receiving"></a>Kassatoiming 803 – komplekteerimine ja vastuvõtmine
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Toimingute komplekteerimine ja vastuvõtmine peatatakse uue toimingu ümberkujundamise tõttu. |
| **Asendatud teise funktsiooniga?**   | Jah. See asendatakse kahe uue kassatoiminguga: sissetulev toiming (804) ja väljaminev toiming (805).|
| **Mõjutatud tootealad**         | Kassarakendus |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Aegunud: alates väljalaskest 10.0.10 ei saa komplekteerimise ja vastuvõtmise toiming enam uusi funktsiooniuuendusi. Tulevastes väljalasetes tehakse selle toimingu jaoks vaid olulisemaid veaparandusi. Kõikidel uutel klientidel soovitatakse liikuda uue [sissetuleva toimingu](../pos-inbound-inventory-operation.md) ja [väljamineva toimingu](../pos-outbound-inventory-operation.md) kasutamisele, mis on jätkuvalt osa meie pikaajalisest toodete tegevuskavast. |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a>Commerce'i väljalaskest 10.0.7 eemaldatud või aegunud funktsioonid
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a>Commerce'i GetProductAvailabilities ja GetAvailableInventoryNearby API-d
| &nbsp;  | &nbsp; |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Uued optimeeritud API-d on loodud asendama API-sid GetProductAvailabilities ja GetAvailableInventoryNearby. |
| **Asendatud teise funktsiooniga?**   | Jah: see asendatakse API-dega GetEstimatedAvailability ja GetEstimatedProductWarehouseAvailability. |
| **Mõjutatud tootealad**         | e-Commerce'i rakenduse SDK |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Aegunud: alates väljalaskest 10.0.7 ei tehta enam API-de GetProductAvailabilities ja GetAvailableInventoryNearby jaoks insenerindusalaseid investeeringuid. Organisatsioonid, mis kasutavad antud API-sid oma e-Commerce'i rakendustes peaksid minema üle uutele API-dele GetEstimatedAvailabilty ja GetEstimatedProductWarehouseAvailability ning lubama [optimeeritud toote saadavuse arvutusfunktsiooni](../calculated-inventory-retail-channels.md).  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Varasemad teatised eemaldatud või aegunud funktsioonidest
Lisateavet funktsioonide kohta, mis on eelnevatest versioonidest eemaldatud või aegunud, vt teemat [Varasematest versioonidest eemaldatud või aegunud funktsioonid](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
