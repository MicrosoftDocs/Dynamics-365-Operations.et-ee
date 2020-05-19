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
# <a name="removed-or-deprecated-features-in-dynamics-365-commerce"></a><span data-ttu-id="9d31b-103">Dynamics 365 Commercei eemaldatud või aegunud funktsioonid</span><span class="sxs-lookup"><span data-stu-id="9d31b-103">Removed or deprecated features in Dynamics 365 Commerce</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9d31b-104">See teema kirjeldab funktsioone, mis on eemaldatud või plaanitakse eemaldada Dynamics 365 Commerce'ist.</span><span class="sxs-lookup"><span data-stu-id="9d31b-104">This topic describes features that have been removed, or that are planned for removal from Dynamics 365 Commerce.</span></span>

- <span data-ttu-id="9d31b-105">*Eemaldatud* funktsioon pole tootes enam saadaval.</span><span class="sxs-lookup"><span data-stu-id="9d31b-105">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="9d31b-106">*Aegunud* funktsioon ei ole aktiivses arenduses ja vee võidakse tulevases värskenduses eemaldada.</span><span class="sxs-lookup"><span data-stu-id="9d31b-106">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="9d31b-107">See loend peaks aitama teil neid eemaldusi ja aegumisi oma plaanides arvesse võtta.</span><span class="sxs-lookup"><span data-stu-id="9d31b-107">This list is intended to help you consider these removals and deprecations for your own planning.</span></span> 

> [!NOTE]
> <span data-ttu-id="9d31b-108">Üksikasjalikku teavet rakenduse Finance and Operationsi rakenduste objektide kohta leiate teemast [Tehnilise teabe aruanded](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span><span class="sxs-lookup"><span data-stu-id="9d31b-108">Detailed information about objects in Finance and Operations apps can be found in the [Technical reference reports](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep).</span></span> <span data-ttu-id="9d31b-109">Saate võrrelda nende aruannete eri versioone, et õppida objektide kohta, mida on igas Finance and Operationsi rakenduste versioonis muudetud või eemaldatud.</span><span class="sxs-lookup"><span data-stu-id="9d31b-109">You can compare the different versions of these reports to learn about objects that have changed or been removed in each version of Finance and Operations apps.</span></span>

## <a name="features-removed-or-deprecated-in-the-commerce-10010-release"></a><span data-ttu-id="9d31b-110">Commerce'i väljalaskest 10.0.10 eemaldatud või aegunud funktsioonid</span><span class="sxs-lookup"><span data-stu-id="9d31b-110">Features removed or deprecated in the Commerce 10.0.10 release</span></span>
### <a name="pos-operation-803---picking-and-receiving"></a><span data-ttu-id="9d31b-111">Kassatoiming 803 – komplekteerimine ja vastuvõtmine</span><span class="sxs-lookup"><span data-stu-id="9d31b-111">POS operation 803 - Picking and receiving</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="9d31b-112">**Aegumise/eemaldamise põhjus**</span><span class="sxs-lookup"><span data-stu-id="9d31b-112">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="9d31b-113">Toimingute komplekteerimine ja vastuvõtmine peatatakse uue toimingu ümberkujundamise tõttu.</span><span class="sxs-lookup"><span data-stu-id="9d31b-113">Picking and receiving operations is being deprecated due to new operation redesign.</span></span> |
| <span data-ttu-id="9d31b-114">**Asendatud teise funktsiooniga?**</span><span class="sxs-lookup"><span data-stu-id="9d31b-114">**Replaced by another feature?**</span></span>   | <span data-ttu-id="9d31b-115">Jah.</span><span class="sxs-lookup"><span data-stu-id="9d31b-115">Yes.</span></span> <span data-ttu-id="9d31b-116">See asendatakse kahe uue kassatoiminguga: sissetulev toiming (804) ja väljaminev toiming (805).</span><span class="sxs-lookup"><span data-stu-id="9d31b-116">It is replaced by two new POS operations: inbound operation (804) and outbound operation (805).</span></span>|
| <span data-ttu-id="9d31b-117">**Mõjutatud tootealad**</span><span class="sxs-lookup"><span data-stu-id="9d31b-117">**Product areas affected**</span></span>         | <span data-ttu-id="9d31b-118">Kassarakendus</span><span class="sxs-lookup"><span data-stu-id="9d31b-118">Point of sale (POS) application</span></span> |
| <span data-ttu-id="9d31b-119">**Juurutamissuvand**</span><span class="sxs-lookup"><span data-stu-id="9d31b-119">**Deployment option**</span></span>              | <span data-ttu-id="9d31b-120">Kõik</span><span class="sxs-lookup"><span data-stu-id="9d31b-120">All</span></span> |
| <span data-ttu-id="9d31b-121">**Olek**</span><span class="sxs-lookup"><span data-stu-id="9d31b-121">**Status**</span></span>                         | <span data-ttu-id="9d31b-122">Aegunud: alates väljalaskest 10.0.10 ei saa komplekteerimise ja vastuvõtmise toiming enam uusi funktsiooniuuendusi.</span><span class="sxs-lookup"><span data-stu-id="9d31b-122">Deprecated: As of release 10.0.10, the picking and receiving operation will no longer receive any new feature updates.</span></span> <span data-ttu-id="9d31b-123">Tulevastes väljalasetes tehakse selle toimingu jaoks vaid olulisemaid veaparandusi.</span><span class="sxs-lookup"><span data-stu-id="9d31b-123">Only critical bug fixes will be done for this operation in future releases.</span></span> <span data-ttu-id="9d31b-124">Kõikidel uutel klientidel soovitatakse liikuda uue [sissetuleva toimingu](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) ja [väljamineva toimingu](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation) kasutamisele, mis on jätkuvalt osa meie pikaajalisest toodete tegevuskavast.</span><span class="sxs-lookup"><span data-stu-id="9d31b-124">All customers are encouraged to move to the new [Inbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-inbound-inventory-operation) and [Outbound operations](https://docs.microsoft.com/dynamics365/commerce/pos-outbound-inventory-operation), which will continue to be part of our long-term product roadmap.</span></span> |


## <a name="features-removed-or-deprecated-in-the-commerce-1007-release"></a><span data-ttu-id="9d31b-125">Commerce'i väljalaskest 10.0.7 eemaldatud või aegunud funktsioonid</span><span class="sxs-lookup"><span data-stu-id="9d31b-125">Features removed or deprecated in the Commerce 10.0.7 release</span></span>
### <a name="commerce-getproductavailabilities-and-getavailableinventorynearby-apis"></a><span data-ttu-id="9d31b-126">Commerce'i GetProductAvailabilities ja GetAvailableInventoryNearby API-d</span><span class="sxs-lookup"><span data-stu-id="9d31b-126">Commerce GetProductAvailabilities and GetAvailableInventoryNearby API's</span></span>
|   |  |
|------------|--------------------|
| <span data-ttu-id="9d31b-127">**Aegumise/eemaldamise põhjus**</span><span class="sxs-lookup"><span data-stu-id="9d31b-127">**Reason for deprecation/removal**</span></span> | <span data-ttu-id="9d31b-128">Uued optimeeritud API-d on loodud asendama API-sid GetProductAvailabilities ja GetAvailableInventoryNearby.</span><span class="sxs-lookup"><span data-stu-id="9d31b-128">New optimized APIs have been created to replace the GetProductAvailabilities and GetAvailableInventoryNearby APIs.</span></span> |
| <span data-ttu-id="9d31b-129">**Asendatud teise funktsiooniga?**</span><span class="sxs-lookup"><span data-stu-id="9d31b-129">**Replaced by another feature?**</span></span>   | <span data-ttu-id="9d31b-130">Jah: see asendatakse API-dega GetEstimatedAvailability ja GetEstimatedProductWarehouseAvailability.</span><span class="sxs-lookup"><span data-stu-id="9d31b-130">Yes: It is replaced by GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs.</span></span> |
| <span data-ttu-id="9d31b-131">**Mõjutatud tootealad**</span><span class="sxs-lookup"><span data-stu-id="9d31b-131">**Product areas affected**</span></span>         | <span data-ttu-id="9d31b-132">e-Commerce'i rakenduse SDK</span><span class="sxs-lookup"><span data-stu-id="9d31b-132">e-Commerce application SDK</span></span> |
| <span data-ttu-id="9d31b-133">**Juurutamissuvand**</span><span class="sxs-lookup"><span data-stu-id="9d31b-133">**Deployment option**</span></span>              | <span data-ttu-id="9d31b-134">Kõik</span><span class="sxs-lookup"><span data-stu-id="9d31b-134">All</span></span> |
| <span data-ttu-id="9d31b-135">**Olek**</span><span class="sxs-lookup"><span data-stu-id="9d31b-135">**Status**</span></span>                         | <span data-ttu-id="9d31b-136">Aegunud: alates väljalaskest 10.0.7 ei tehta enam API-de GetProductAvailabilities ja GetAvailableInventoryNearby jaoks insenerindusalaseid investeeringuid.</span><span class="sxs-lookup"><span data-stu-id="9d31b-136">Deprecated: As of release 10.0.7, there will no longer be engineering investments made for GetProductAvailabilities and GetAvailableInventoryNearby.</span></span> <span data-ttu-id="9d31b-137">Organisatsioonid, mis kasutavad antud API-sid oma e-Commerce'i rakendustes peaksid minema üle uutele API-dele GetEstimatedAvailabilty ja GetEstimatedProductWarehouseAvailability ning lubama [optimeeritud toote saadavuse arvutusfunktsiooni](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="9d31b-137">Organizations that use these APIs in their e-Commerce deployments should convert to the new GetEstimatedAvailabilty and GetEstimatedProductWarehouseAvailability APIs and enable the [Optimized product availability calculation feature](https://docs.microsoft.com/dynamics365/commerce/calculated-inventory-retail-channels).</span></span>  |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a><span data-ttu-id="9d31b-138">Varasemad teatised eemaldatud või aegunud funktsioonidest</span><span class="sxs-lookup"><span data-stu-id="9d31b-138">Previous announcements about removed or deprecated features</span></span>
<span data-ttu-id="9d31b-139">Lisateavet funktsioonide kohta, mis on eelnevatest versioonidest eemaldatud või aegunud, vt teemat [Varasematest versioonidest eemaldatud või aegunud funktsioonid](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="9d31b-139">To learn more about features that have been removed or deprecated in previous releases, see [Removed or deprecated features in previous releases](../../fin-ops-core/dev-itpro/migration-upgrade/deprecated-features.md?toc=/dynamics365/commerce/toc.json).</span></span>
