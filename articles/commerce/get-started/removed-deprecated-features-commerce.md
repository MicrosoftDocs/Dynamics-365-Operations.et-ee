---
title: Dynamics 365 Commercei eemaldatud või aegunud funktsioonid
description: See teema kirjeldab funktsioone, mis on eemaldatud või plaanitakse eemaldada Dynamics 365 Commerce'ist.
author: josaw
manager: AnnBe
ms.date: 12/07/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-04-30
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 37b541ff5037a38b60dbfd6a6c071f55afcc1304
ms.sourcegitcommit: 069ed5789517b550065e5e2317658fec4027359e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/07/2020
ms.locfileid: "4689523"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Dynamics 365 Commercei eemaldatud või aegunud funktsioonid

[!include [banner](../includes/banner.md)]

See teema kirjeldab funktsioone, mis on eemaldatud või plaanitakse eemaldada Dynamics 365 Commerce'ist.

- *Eemaldatud* funktsioon pole tootes enam saadaval.
- *Aegunud* funktsioon ei ole aktiivses arenduses ja vee võidakse tulevases värskenduses eemaldada.

See loend peaks aitama teil neid eemaldusi ja aegumisi oma plaanides arvesse võtta. 

> [!NOTE]
> Üksikasjalikku teavet rakenduse Finance and Operationsi rakenduste objektide kohta leiate teemast [Tehnilise teabe aruanded](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Saate võrrelda nende aruannete eri versioone, et õppida objektide kohta, mida on igas Finance and Operationsi rakenduste versioonis muudetud või eemaldatud.

## <a name="features-removed-or-deprecated-in-the-commerce-10015-release"></a>Commerce'i väljalaskest 10.0.15 eemaldatud või aegunud funktsioonid

### <a name="internet-explorer-11-support-for-dynamics-365-is-deprecated"></a>Internet Explorer 11 Dynamics 365 tugi on iganenud

|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Kehtib alates 2020. detsembrist, Microsoft Internet Explorer 11 tugi kõigile Dynamics 365 toodetele on iganenud ja Internet Explorer 11 ei toetata pärast 2021. aasta augustit.<br><br>See mõjutab kliente, kes kasutavad Dynamics 365 tooteid, mis on mõeldud kasutamiseks Internet Explorer 11 liidese kaudu. Pärast 2021. aasta augustit, Internet Explorer 11 ei toetata selliste Dynamics 365 toodete puhul. |
| **Asendatud teise funktsiooniga?**   | Soovitame klientide minna üle Microsoft Edge-le.|
| **Mõjutatud tootealad**         | Kõik Dynamics 365 tooted |
| **Juurutamissuvand**              | Kõik|
| **Olek**                         | Aegunud. Internet Explorer 11 ei toetata pärast 2021. aasta augustit.|

## <a name="features-removed-or-deprecated-in-the-commerce-10011-release"></a>Commerce'i väljalaskest 10.0.11 eemaldatud või aegunud funktsioonid
### <a name="data-action-hooks"></a>Andmetegevuse konksud
|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Andmetegevuse konksude funktsioon on jõudlusprobleemide tõttu iganenud. |
| **Asendatud teise funktsiooniga?**   | Soovitatame kasutada andmetegevuse kihis äriloogika muutmiseks [andmetegevuse alistamisi](../e-commerce-extensibility/data-action-overrides.md).|
| **Mõjutatud tootealad**         | e-kaubanduse laiendatavuse andmetegevused |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Iganenud: alates väljaandest 10.0.11 |

### <a name="retail-sdk-support-for-visual-studio-2015-msbuild-140-and-retail-sdkreference-libraries-and-tools"></a>Jaemüügi SDK tugi Visual Studio 2015, msbuild 14.0 ja jaemüügi SDK\viiteteekide ja tööriistade jaoks
|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Jaemüügi SDK tugi Visual Studio 2015 jaoks on iganenud ja uuendatud, et toetada VS 2017, msbuild 15.0 ja kõiki viiteteeke ning kaumbanduse puhvrigeneraatori tööriistad kaustas RetailSDK\References on teisaldatud NuGeti pakettidesse, et lihtsustada laienduse mudeli ja SDK värskendamise protsessi.|
| **Asendatud teise funktsiooniga?**   | Soovitame teil süsteemi värskendamiseks järgida teavet teemas [Jaemüügi SDK migreerimine Visual Studio 2015-st Visual Studio 2017-sse](../dev-itpro/retail-sdk/migrate-sdk.md). |
| **Mõjutatud tootealad**         | Jaemüügi SDK laiendused |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Iganenud: alates väljaandest 10.0.11 |

### <a name="retail-server-extension-using-iedmmodelextender-and-commercecontroller"></a>Jaemüügi serveri laiendus, mis kasutab üksusi IEdmModelExtender ja CommerceController
|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Jaemüügi serveri laiendus, mis kasutab üksusi IEdmModelExtender ja CommerceController, on iganenud, et pakkuda lihtsustatud laienduse mudelit. Uuel juurutusel on ainult kontrolleri klass, millel puudub täiendav klassi IEdmModelExtender juurutus. See väldib ka sõltuvust konkreetse OData versiooniga (OData versiooni värskendamisel võidakse laiendusi lõhkuda). |
| **Asendatud teise funktsiooniga?**   |  Soovitame kasutada IControlleri klassi laienduse mudelit, importides NuGeti (Microsoft.Dynamics.Commerce.Hosting.Contracts) paketi. |
| **Mõjutatud tootealad**         | Jaemüügi serveri laiendused |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Iganenud: alates väljaandest 10.0.11 |

### <a name="hardware-station-extension-using-ihardwarestationcontroller"></a>Riistvarajaama laiendus, mis kasutab üksust IHardwareStationController
|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Riistvarajaama laiendus, mis kasutab üksust IHardwareStationController on iganenud, et pakkuda lihtsustatud laienduse mudelit. Uuel juurutusel on ainult IControlleri klass ilma täiendavate klasside juurutusteta ja põhiriistvara jaamateekidega sõltuvuste vältimiseks pidi laiendus varasemalt viitama mitmele teegile.) |
| **Asendatud teise funktsiooniga?**   | Soovitatav on kasutada IControlleri klassi laienduse mudelit, importides NuGeti (Microsoft.Dynamics.Commerce.Hosting.Contracts) paketi. |
| **Mõjutatud tootealad**         | Riistvarajaama laiendused |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Iganenud: alates väljaandest 10.0.11 |

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a>Commerce'i väljalaskest 10.0.10 eemaldatud või aegunud funktsioonid
### <a name="pos-operation-803---picking-and-receiving"></a>Kassatoiming 803 – komplekteerimine ja vastuvõtmine
|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Toimingute komplekteerimine ja vastuvõtmine peatatakse uue toimingu ümberkujundamise tõttu. |
| **Asendatud teise funktsiooniga?**   | Jah. See asendatakse kahe uue kassatoiminguga: sissetulev toiming (804) ja väljaminev toiming (805).|
| **Mõjutatud tootealad**         | Kassarakendus |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Aegunud: alates väljalaskest 10.0.10 ei saa komplekteerimise ja vastuvõtmise toiming enam uusi funktsiooniuuendusi. Tulevastes väljalasetes tehakse selle toimingu jaoks vaid olulisemaid veaparandusi. Kõikidel uutel klientidel soovitatakse liikuda uue [sissetuleva toimingu](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) ja [väljamineva toimingu](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation) kasutamisele, mis on jätkuvalt osa meie pikaajalisest toodete tegevuskavast. |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a>Commerce'i väljalaskest 10.0.7 eemaldatud või aegunud funktsioonid
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a>Commerce'i GetProductAvailabilities ja GetAvailableInventoryNearby API-d
|   |  |
|------------|--------------------|
| **Aegumise/eemaldamise põhjus** | Uued optimeeritud API-d on loodud asendama API-sid GetProductAvailabilities ja GetAvailableInventoryNearby. |
| **Asendatud teise funktsiooniga?**   | Jah: see asendatakse API-dega GetEstimatedAvailability ja GetEstimatedProductWarehouseAvailability. |
| **Mõjutatud tootealad**         | e-Commerce'i rakenduse SDK |
| **Juurutamissuvand**              | Kõik |
| **Olek**                         | Aegunud: alates väljalaskest 10.0.7 ei tehta enam API-de GetProductAvailabilities ja GetAvailableInventoryNearby jaoks insenerindusalaseid investeeringuid. Organisatsioonid, mis kasutavad antud API-sid oma e-Commerce'i rakendustes peaksid minema üle uutele API-dele GetEstimatedAvailabilty ja GetEstimatedProductWarehouseAvailability ning lubama [optimeeritud toote saadavuse arvutusfunktsiooni](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Varasemad teatised eemaldatud või aegunud funktsioonidest
Lisateavet funktsioonide kohta, mis on eelnevatest versioonidest eemaldatud või aegunud, vt teemat [Varasematest versioonidest eemaldatud või aegunud funktsioonid](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).
