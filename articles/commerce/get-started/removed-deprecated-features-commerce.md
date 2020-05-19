---
title: Dynamics 365 Commercei eemaldatud või aegunud funktsioonid
description: See teema kirjeldab funktsioone, mis on eemaldatud või plaanitakse eemaldada Dynamics 365 Commerce'ist.
author: josaw
manager: AnnBe
ms.date: 05/04/2020
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
ms.openlocfilehash: c47c5430a8f5d67e13c95db609a95d5ad66933ae
ms.sourcegitcommit: a8b6cd799eddaf5be9aec9ea3c2b55e2c3231652
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/05/2020
ms.locfileid: "3335272"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a>Dynamics 365 Commercei eemaldatud või aegunud funktsioonid

[!include [banner](../includes/banner.md)]

See teema kirjeldab funktsioone, mis on eemaldatud või plaanitakse eemaldada Dynamics 365 Commerce'ist.

- *Eemaldatud* funktsioon pole tootes enam saadaval.
- *Aegunud* funktsioon ei ole aktiivses arenduses ja vee võidakse tulevases värskenduses eemaldada.

See loend peaks aitama teil neid eemaldusi ja aegumisi oma plaanides arvesse võtta. 

> [!NOTE]
> Üksikasjalikku teavet rakenduse Finance and Operationsi rakenduste objektide kohta leiate teemast [Tehnilise teabe aruanded](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Saate võrrelda nende aruannete eri versioone, et õppida objektide kohta, mida on igas Finance and Operationsi rakenduste versioonis muudetud või eemaldatud.

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
