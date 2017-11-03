---
title: "Kaasa füüsiline väärtus"
description: "Märkeruutu Kaasa füüsiline väärtus kiirkaardil Laomudel või lehel Kauba mudeligrupid kasutatakse määramiseks, kas füüsiliselt värskendatud kandeid arvestatakse kauba jooksva keskmise omahinna arvutuses."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 79033
ms.assetid: 1928c145-bf82-436d-87ca-e7a173e31923
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 4ea8fe31588dd0768e0651c9e1e332212a00cde2
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="include-physical-value"></a><span data-ttu-id="f243d-103">Kaasa füüsiline väärtus</span><span class="sxs-lookup"><span data-stu-id="f243d-103">Include physical value</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f243d-104">Märkeruutu Kaasa füüsiline väärtus kiirkaardil Laomudel või lehel Kauba mudeligrupid kasutatakse määramiseks, kas füüsiliselt värskendatud kandeid arvestatakse kauba jooksva keskmise omahinna arvutuses.</span><span class="sxs-lookup"><span data-stu-id="f243d-104">You use the Include physical value check box on the Inventory model FastTab of the Item model groups page to specify whether physically updated transactions are considered when the running average cost price is calculated for an item.</span></span>

<span data-ttu-id="f243d-105">Märkeruudul **Kaasa füüsiline väärtus** on järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="f243d-105">The **Include physical value** check box has the following values.</span></span>

| <span data-ttu-id="f243d-106">Väärtus</span><span class="sxs-lookup"><span data-stu-id="f243d-106">Value</span></span>    | <span data-ttu-id="f243d-107">Tulemus</span><span class="sxs-lookup"><span data-stu-id="f243d-107">Result</span></span>                                                                                                                          |
|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f243d-108">Valitud</span><span class="sxs-lookup"><span data-stu-id="f243d-108">Selected</span></span> | <span data-ttu-id="f243d-109">Jooksva keskmise omahinna arvutamiseks kasutatakse nii füüsiliselt kui ka rahaliselt värskendatud kandeid.</span><span class="sxs-lookup"><span data-stu-id="f243d-109">Both physically updated transactions and financially updated transactions are used to calculate the running average cost price.</span></span> |
| <span data-ttu-id="f243d-110">Tühjendatud</span><span class="sxs-lookup"><span data-stu-id="f243d-110">Cleared</span></span>  | <span data-ttu-id="f243d-111">Jooksva keskmise omahinna arvutamiseks kasutatakse ainult rahaliselt värskendatud kandeid.</span><span class="sxs-lookup"><span data-stu-id="f243d-111">Only financially updated transactions are used to calculate the running average cost price.</span></span>                                     |

<span data-ttu-id="f243d-112">Märkeruudul on veidi erinevad mõjud, olenevalt kasutatavast laomudelist.</span><span class="sxs-lookup"><span data-stu-id="f243d-112">The check box has slightly different effects, depending on the inventory model that you use.</span></span>

-   <span data-ttu-id="f243d-113">Kui märgite ruudu **Kaasa füüsiline väärtus** laomudeli FIFO (elavjärjekorra), LIFO (viimaste esmaväljastamine) või LIFO kasutamisel, korrigeerib lao sulgemine ka füüsiliselt värskendatud kandeid.</span><span class="sxs-lookup"><span data-stu-id="f243d-113">If you select the **Include physical value** check box when you use the FIFO (First in, first out), LIFO (Last in, first out), or LIFO date inventory model, inventory close also makes adjustments to physically updated transactions.</span></span>
-   <span data-ttu-id="f243d-114">Kui te ei märgi laomudelite kasutamisel ruutu **Kaasa füüsiline väärtus**, teeb lao sulgemine tasakaalustusi ainult rahaliselt värskendatud kannetes.</span><span class="sxs-lookup"><span data-stu-id="f243d-114">If you don't select the **Include physical value** check box when you use these inventory models, inventory close makes settlements only to financially updated transactions.</span></span>
-   <span data-ttu-id="f243d-115">Kui kasutate kaalutud keskmise või kaalutud keskmise kuupäeva laomudelit, tasakaalustab lao sulgemine vaid rahaliselt värskendatud kanded, olenemata sellest, kas märgite ruudu **Kaasa füüsiline väärtus**.</span><span class="sxs-lookup"><span data-stu-id="f243d-115">When you use the weighted average or weighted average date inventory model, inventory close settles only financially updated transactions, regardless of whether you select the **Include physical value** check box.</span></span>

<span data-ttu-id="f243d-116">**Näide 1** Olete märkinud ruudu**Kaasa füüsiline väärtus** ja saate järgmised ostutellimused.</span><span class="sxs-lookup"><span data-stu-id="f243d-116">**Example 1** You've selected the **Include physical value** check box and receive the following purchase orders:</span></span>

-   <span data-ttu-id="f243d-117">Ostutellimus kogusele 2 omahinnaga 10.00 USA dollarit, mis on saatelehega sisestatud</span><span class="sxs-lookup"><span data-stu-id="f243d-117">A purchase order for a quantity of 2 and a cost price of USD 10.00 that has been packing slip–updated</span></span>
-   <span data-ttu-id="f243d-118">Ostutellimus kogusele 3 omahinnaga 12.00 USA dollarit, mis on arvega sisestatud</span><span class="sxs-lookup"><span data-stu-id="f243d-118">A purchase order for a quantity of 3 and a cost price of USD 12.00 that has been invoice-updated</span></span>

<span data-ttu-id="f243d-119">Sellisel juhul on jooksev keskmine omahind 11.20 USD, sest omahinna arvutamiseks kasutatakse nii füüsiliselt kui ka rahaliselt värskendatud kandeid.</span><span class="sxs-lookup"><span data-stu-id="f243d-119">In this case, the running average cost price will be USD 11.20, because both physically updated transactions and financially updated transactions are used to calculate the cost price.</span></span> <span data-ttu-id="f243d-120">**Näide 2** Te pole märkinud ruutu **Kaasa füüsiline väärtus** ja kauba seadistuse omahind on 10.00 USD.</span><span class="sxs-lookup"><span data-stu-id="f243d-120">**Example 2** You haven't selected the **Include physical value** check box, and the cost price on the item setup is USD 10.00.</span></span> <span data-ttu-id="f243d-121">Saate ostutellimuse kogusele 20 omahinnaga 12.00 USA dollarit, mis on saatelehega sisestatud</span><span class="sxs-lookup"><span data-stu-id="f243d-121">You receive a purchase order for a quantity of 20 and a cost price of USD 12.00 that has been packing slip–updated.</span></span> <span data-ttu-id="f243d-122">Müügitellimuse sisestamisel sisestatakse kulusumma 10.00 USD kulusumma, sest jooksev keskmine omahind ei hõlma füüsiliselt sisestatud kandeid.</span><span class="sxs-lookup"><span data-stu-id="f243d-122">When a sales order is posted, the posted cost amount is USD 10.00, because the running average cost price won't include physically posted transactions.</span></span> <span data-ttu-id="f243d-123">**Märkus:** võrdluseks, kui märgite selle kauba puhul müügitellimuse sisestamisel ruudu **Kaasa füüsiline väärtus**, on sisestatav kulusumma 12.00 USD.</span><span class="sxs-lookup"><span data-stu-id="f243d-123">**Note:** For comparison, if you select the **Include physical value** check box for this item, when a sales order is posted, the posted cost amount will be USD 12.00.</span></span>




