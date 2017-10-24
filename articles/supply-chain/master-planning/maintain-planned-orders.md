---
title: Plaanitud tellimuste haldamine
description: "See artikkel pakub teavet plaanitud tellimuste haldamise kohta. See kirjeldab, kuidas plaanitud tellimuste olekut värskendada, neid kinnitada ja filtreerida plaanitud tellimusi, millel on sama olek, nagu valitud plaanitud tellimusel."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3ec45e7426f65827f161245870f9114e52e035ab
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="maintain-planned-orders"></a><span data-ttu-id="62b79-104">Plaanitud tellimuste haldamine</span><span class="sxs-lookup"><span data-stu-id="62b79-104">Maintain planned orders</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="62b79-105">See artikkel pakub teavet plaanitud tellimuste haldamise kohta.</span><span class="sxs-lookup"><span data-stu-id="62b79-105">This article provides information about how to manage planned orders.</span></span> <span data-ttu-id="62b79-106">See kirjeldab, kuidas plaanitud tellimuste olekut värskendada, neid kinnitada ja filtreerida plaanitud tellimusi, millel on sama olek, nagu valitud plaanitud tellimusel.</span><span class="sxs-lookup"><span data-stu-id="62b79-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="62b79-107">Saate planeeritud tellimusi hallata tööruumis **Koondplaneerimine**, loendis **Plaanitud tellimus** või loendites **Plaanitud tootmistellimused**, **Plaanitud ostutellimused** ja **Plaanitud üleviimised**.</span><span class="sxs-lookup"><span data-stu-id="62b79-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> <span data-ttu-id="62b79-108">Saate edenemist jälgida välja **Olek** abil.</span><span class="sxs-lookup"><span data-stu-id="62b79-108">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="62b79-109">Kasutatakse järgmisi väärtusi.</span><span class="sxs-lookup"><span data-stu-id="62b79-109">The following values are used:</span></span>

-   <span data-ttu-id="62b79-110">Kui koondplaneerimine loob plaanitud tellimused, on nende olek **Töötlemata**.</span><span class="sxs-lookup"><span data-stu-id="62b79-110">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="62b79-111">Kui otsustate plaanitud tellimust mitte kinnitada, saate sellele määrata oleku **Lõpule viidud**.</span><span class="sxs-lookup"><span data-stu-id="62b79-111">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="62b79-112">Kui otsustate plaanitud tellimuse kinnitada, saate sellele määrata oleku **Heaks kiidetud**.</span><span class="sxs-lookup"><span data-stu-id="62b79-112">When you decide to firm a planned order, you can give it a status of **Approved**.</span></span> <span data-ttu-id="62b79-113">See olek näitab, et olete plaanitud tellimuse kinnitamisega nõus, kuid see pole veel kinnitatud.</span><span class="sxs-lookup"><span data-stu-id="62b79-113">This status indicates that you approve firming of the planned order, but it isn't firmed yet.</span></span>

<span data-ttu-id="62b79-114">**Märkus.** Kinnitatud plaanitud tellimus kantakse järgmise koondplaani arvutamisse üle praeguses olekus.</span><span class="sxs-lookup"><span data-stu-id="62b79-114">**Note:** An approved planned order is transferred, in its current state, to the next master planning calculation.</span></span> <span data-ttu-id="62b79-115">Plaanitud tellimused saate kinnitada, klõpsates käsku **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="62b79-115">You can firm planned orders by clicking **Firm**.</span></span> <span data-ttu-id="62b79-116">Kinnitada saab järgmisi plaanitud tellimusi:</span><span class="sxs-lookup"><span data-stu-id="62b79-116">You can firm the following planned orders:</span></span>

-   <span data-ttu-id="62b79-117">Valitud plaanitud tellimus.</span><span class="sxs-lookup"><span data-stu-id="62b79-117">The planned order that is selected.</span></span>
-   <span data-ttu-id="62b79-118">Mitu plaanitud tellimust.</span><span class="sxs-lookup"><span data-stu-id="62b79-118">Multiple planned orders.</span></span>
-   <span data-ttu-id="62b79-119">Lehel **Koosnevusarvutus** tehtud koosnevusarvutusega loodud plaanitud tellimused.</span><span class="sxs-lookup"><span data-stu-id="62b79-119">Planned orders that are generated by an explosion from the **Explosion** page.</span></span> <span data-ttu-id="62b79-120">Klõpsake nuppu **Plaanitud tellimused**, valige plaanitud tellimus ja seejärel klõpsake käsku **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="62b79-120">Click **Planned orders**, select the planned order, and then click **Firm**.</span></span>

<span data-ttu-id="62b79-121">Kui plaanitud tellimus on kinnitatud, teisaldatakse see asjakohase mooduli tellimuste jaotisse.</span><span class="sxs-lookup"><span data-stu-id="62b79-121">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span> <span data-ttu-id="62b79-122">**Märkus.** Saate paremklõpsata teatud olekuga plaanitud tellimusel ja filtreerida teisi sama olekuga plaanitud tellimusi.</span><span class="sxs-lookup"><span data-stu-id="62b79-122">**Note:** You can right-click a planned order that has a particular status and filter for other planned orders that have the same status.</span></span> <span data-ttu-id="62b79-123">See funktsioon on kasulik, kui soovite näiteks filtreerida kõik plaanitud tellimused, mille olek on **Heaks kiidetud**, et saaksite need seejärel kinnitada.</span><span class="sxs-lookup"><span data-stu-id="62b79-123">This functionality is useful if, for example, you want to filter for all planned orders that have a status of **Approved**, so that you can then firm them.</span></span>

<a name="see-also"></a><span data-ttu-id="62b79-124">Vt ka</span><span class="sxs-lookup"><span data-stu-id="62b79-124">See also</span></span>
--------

[<span data-ttu-id="62b79-125">Koondplaanid</span><span class="sxs-lookup"><span data-stu-id="62b79-125">Master plans</span></span>](master-plans.md)




