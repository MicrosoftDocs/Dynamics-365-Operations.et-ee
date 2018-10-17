---
title: Plaanitud tellimuste haldamine
description: "See teema pakub teavet plaanitud tellimuste haldamise kohta. See kirjeldab, kuidas plaanitud tellimuste olekut värskendada, neid kinnitada ja filtreerida plaanitud tellimusi, millel on sama olek, nagu valitud plaanitud tellimusel."
author: roxanadiaconu
manager: AnnBe
ms.date: 10/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19151
ms.assetid: 54123f4c-b4ca-4ce4-9358-b067aa04c968
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 657c19896b20a514dc5308bf7fb086085b482fec
ms.openlocfilehash: bf578d98abc4825c5607ec031da6ab6737c3183a
ms.contentlocale: et-ee
ms.lasthandoff: 10/08/2018

---

# <a name="maintain-planned-orders"></a><span data-ttu-id="2ab5f-104">Plaanitud tellimuste haldamine</span><span class="sxs-lookup"><span data-stu-id="2ab5f-104">Maintain planned orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ab5f-105">See teema pakub teavet plaanitud tellimuste haldamise kohta.</span><span class="sxs-lookup"><span data-stu-id="2ab5f-105">This topic provides information about how to manage planned orders.</span></span> <span data-ttu-id="2ab5f-106">See kirjeldab, kuidas plaanitud tellimuste olekut värskendada, neid kinnitada ja filtreerida plaanitud tellimusi, millel on sama olek, nagu valitud plaanitud tellimusel.</span><span class="sxs-lookup"><span data-stu-id="2ab5f-106">It describes how you can update the status of planned orders, firm them, and filter for planned orders that have the same status as a selected planned order.</span></span>

<span data-ttu-id="2ab5f-107">Saate planeeritud tellimusi hallata tööruumis **Koondplaneerimine**, loendis **Plaanitud tellimus** või loendites **Plaanitud tootmistellimused**, **Plaanitud ostutellimused** ja **Plaanitud üleviimised**.</span><span class="sxs-lookup"><span data-stu-id="2ab5f-107">You can manage planned orders from the **Master planning** workspace, the **Planned order** list, or the **Planned production orders**, **Planned purchase orders**, and **Planned transfer** lists.</span></span> <span data-ttu-id="2ab5f-108">Saate edenemist jälgida välja **Olek** abil.</span><span class="sxs-lookup"><span data-stu-id="2ab5f-108">You can use the **Status** field to help track your progress.</span></span> <span data-ttu-id="2ab5f-109">Kasutatakse järgmisi väärtusi.</span><span class="sxs-lookup"><span data-stu-id="2ab5f-109">The following values are used:</span></span>

-   <span data-ttu-id="2ab5f-110">Kui koondplaneerimine loob plaanitud tellimused, on nende olek **Töötlemata**.</span><span class="sxs-lookup"><span data-stu-id="2ab5f-110">When master planning generates planned orders, the planned orders have a status of **Unprocessed**.</span></span>
-   <span data-ttu-id="2ab5f-111">Kui otsustate plaanitud tellimust mitte kinnitada, saate sellele määrata oleku **Lõpule viidud**.</span><span class="sxs-lookup"><span data-stu-id="2ab5f-111">If you decide not to firm a planned order, you can give it a status of **Completed**.</span></span>
-   <span data-ttu-id="2ab5f-112">Kui otsustate plaanitud tellimuse kinnitada, saate sellele määrata oleku **Heaks kiidetud**.</span><span class="sxs-lookup"><span data-stu-id="2ab5f-112">When you decide to firm a planned order, you can give it a status of **Approved**.</span></span> <span data-ttu-id="2ab5f-113">See olek näitab, et olete plaanitud tellimuse kinnitamisega nõus, kuid see pole veel kinnitatud.</span><span class="sxs-lookup"><span data-stu-id="2ab5f-113">This status indicates that you approve firming of the planned order, but it isn't firmed yet.</span></span>

<span data-ttu-id="2ab5f-114">**Märkus.** Kinnitatud plaanitud tellimus kantakse järgmise koondplaani arvutamisse üle praeguses olekus.</span><span class="sxs-lookup"><span data-stu-id="2ab5f-114">**Note:** An approved planned order is transferred, in its current state, to the next master planning calculation.</span></span> <span data-ttu-id="2ab5f-115">Plaanitud tellimused saate kinnitada, klõpsates käsku **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="2ab5f-115">You can firm planned orders by clicking **Firm**.</span></span> <span data-ttu-id="2ab5f-116">Kinnitada saab järgmisi plaanitud tellimusi:</span><span class="sxs-lookup"><span data-stu-id="2ab5f-116">You can firm the following planned orders:</span></span>

-   <span data-ttu-id="2ab5f-117">Valitud plaanitud tellimus.</span><span class="sxs-lookup"><span data-stu-id="2ab5f-117">The planned order that is selected.</span></span>
-   <span data-ttu-id="2ab5f-118">Mitu plaanitud tellimust.</span><span class="sxs-lookup"><span data-stu-id="2ab5f-118">Multiple planned orders.</span></span>
-   <span data-ttu-id="2ab5f-119">Lehel **Koosnevusarvutus** tehtud koosnevusarvutusega loodud plaanitud tellimused.</span><span class="sxs-lookup"><span data-stu-id="2ab5f-119">Planned orders that are generated by an explosion from the **Explosion** page.</span></span> <span data-ttu-id="2ab5f-120">Klõpsake nuppu **Plaanitud tellimused**, valige plaanitud tellimus ja seejärel klõpsake käsku **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="2ab5f-120">Click **Planned orders**, select the planned order, and then click **Firm**.</span></span>

<span data-ttu-id="2ab5f-121">Kui plaanitud tellimus on kinnitatud, teisaldatakse see asjakohase mooduli tellimuste jaotisse.</span><span class="sxs-lookup"><span data-stu-id="2ab5f-121">When a planned order is firmed, it's moved to the orders section of the relevant module.</span></span> 

<a name="additional-resources"></a><span data-ttu-id="2ab5f-122">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="2ab5f-122">Additional resources</span></span>
--------

[<span data-ttu-id="2ab5f-123">Koondplaanid</span><span class="sxs-lookup"><span data-stu-id="2ab5f-123">Master plans</span></span>](master-plans.md)




