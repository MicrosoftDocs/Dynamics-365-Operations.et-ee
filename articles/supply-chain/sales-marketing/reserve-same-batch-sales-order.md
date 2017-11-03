---
title: "Sama partii reserveerimine müügitellimuse jaoks"
description: "Selles artiklis selgitatakse, kuidas seadistada toodet lubama varude reserveerimist üksiku varude partii suhtes."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: aef3a52f4cb2d5af47a8c25a67e6c2076fa1ff03
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="reserve-the-same-batch-for-a-sales-order"></a><span data-ttu-id="6e6be-103">Sama partii reserveerimine müügitellimuse jaoks</span><span class="sxs-lookup"><span data-stu-id="6e6be-103">Reserve the same batch for a sales order</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6e6be-104">Selles artiklis selgitatakse, kuidas seadistada toodet lubama varude reserveerimist üksiku varude partii suhtes.</span><span class="sxs-lookup"><span data-stu-id="6e6be-104">This article explains how to set up a product to allow reservation of inventory against a single batch of inventory.</span></span>

<span data-ttu-id="6e6be-105">Sama partii reserveerimisel saate reserveerida müügitellimuse rea varusid ühe varupartii suhtes.</span><span class="sxs-lookup"><span data-stu-id="6e6be-105">Same batch reservation lets you reserve inventory for a sales order line against a single batch of inventory.</span></span> <span data-ttu-id="6e6be-106">Näiteks võib tapeeti telliv klient soovida, et kogu tellimus täidetaks samast partiist, et vältida rullidevahelist erinevust.</span><span class="sxs-lookup"><span data-stu-id="6e6be-106">For example, a customer who orders wallpaper can request that the whole order be filled from the same batch or lot, to avoid inconsistencies among the rolls.</span></span> <span data-ttu-id="6e6be-107">Toote seadistamiseks nii, et kasutataks sama partii reserveerimist, peavad järgmised sätted olema tootele määratavas kauba mudeligrupis, jälgimisdimensioonide grupis ja laoala dimensioonigrupis aktiivsed.</span><span class="sxs-lookup"><span data-stu-id="6e6be-107">To set up a product to use same batch reservation, the following settings must be active in the item model group, tracking dimension group, and storage dimension group that you assign to the product:</span></span>

-   <span data-ttu-id="6e6be-108">**Kauba mudeligrupid** – kauba mudeligrupil peavad olema varude poliitikate väljagrupis **Reserveerimine** valitud väljad **Sama partii valimine** ja **Konsolideeri vajadus**.</span><span class="sxs-lookup"><span data-stu-id="6e6be-108">**Item model groups** – The item model group must have the **Same batch selection** and **Consolidate requirement** fields selected in the **Reservation** field group for inventory policies.</span></span>
-   <span data-ttu-id="6e6be-109">**Jälgimisdimensioonide grupid** – jälgimisdimensiooni grupil peab olema partiinumbri puhul valitud väli **Laovarude planeerimine dimensioonide kaupa**.</span><span class="sxs-lookup"><span data-stu-id="6e6be-109">**Tracking dimensions groups** – The tracking dimension group must have the **Coverage plan by dimension** field selected for the batch number.</span></span>
-   <span data-ttu-id="6e6be-110">**Laodimensioonide grupid** – laodimensiooni grupil peab olema väljadele **Laoala** ja **Ladu** valitud väli **Laovarude planeerimine dimensioonide kaupa**.</span><span class="sxs-lookup"><span data-stu-id="6e6be-110">**Storage dimensions groups** – The storage dimension group must have the **Coverage plan by dimension** field selected for **Site** and **Warehouse**.</span></span>

<span data-ttu-id="6e6be-111">Kui reserveerite sama partii valikuga müügitellimuse real olevale tootele varusid, püüab Finance and Operations reserveerida tellitud kogust ühest varude partiist.</span><span class="sxs-lookup"><span data-stu-id="6e6be-111">When you reserve inventory for a product on a sales order line that is set up for same batch selection, Microsoft Dynamics 365 for Finance and Operations tries to reserve the ordered quantity from a single inventory batch.</span></span> <span data-ttu-id="6e6be-112">Arvestatakse ka konkreetse partii atribuudi nõudeid.</span><span class="sxs-lookup"><span data-stu-id="6e6be-112">Any specific batch attribute requirements are also considered.</span></span> <span data-ttu-id="6e6be-113">Kui kogust ei saa ühest partiist täita, kuvatakse leht **Sama partii reserveerimise konflikt**.</span><span class="sxs-lookup"><span data-stu-id="6e6be-113">If the quantity can't be filled from a single batch, the **Same batch reservation conflict** page appears.</span></span> <span data-ttu-id="6e6be-114">See leht kirjeldab probleeme ja ka tegevusi, mida saate reserveerimise jätkamiseks teha.</span><span class="sxs-lookup"><span data-stu-id="6e6be-114">This page describes the issues and also the actions that you can take to continue with the reservation.</span></span> <span data-ttu-id="6e6be-115">Järgmised tingimused võivad partii reserveerimist takistada.</span><span class="sxs-lookup"><span data-stu-id="6e6be-115">The following conditions might prevent the batch from being reserved:</span></span>

-   <span data-ttu-id="6e6be-116">Partii likvideerimiskoodil on müügi väljal **Blokeeri reserveering** lipp **Blokeeritud**.</span><span class="sxs-lookup"><span data-stu-id="6e6be-116">The batch disposition code has **Block reservation** for sales flagged as **Blocked**.</span></span>
-   <span data-ttu-id="6e6be-117">Partii on aegumiskuupäeva ja kehtivate kliendi müümispäevade alusel aegunud.</span><span class="sxs-lookup"><span data-stu-id="6e6be-117">The batch has expired, based on the expiration date and any applicable customer sellable days.</span></span> <span data-ttu-id="6e6be-118">Kaupa saab siiski reserveerimisel arvestada, kui kauba mudeligrupp on selle kauba puhul arvestatakse „esimesena aegunud esimesena välja” (FEFO) kuupäeva ja kui komplekteerimise kriteeriumina on valitud parim-enne kuupäev.</span><span class="sxs-lookup"><span data-stu-id="6e6be-118">The item can still be considered for reservation if the item model group for the item is First Expiry First Out (FEFO) date–controlled, and if the best-before date is selected as the pick criterion.</span></span>
-   <span data-ttu-id="6e6be-119">Partiil pole jäänud järele piisavalt kõlblikkusaja päevi, tuginedes aegumiskuupäevale ja parim-enne kuupäevale, millele on liidetud kliendi müümispäevad.</span><span class="sxs-lookup"><span data-stu-id="6e6be-119">The batch doesn't have enough shelf-life days remaining, based on the expiration date and best-before date, plus any customer sellable days.</span></span>





