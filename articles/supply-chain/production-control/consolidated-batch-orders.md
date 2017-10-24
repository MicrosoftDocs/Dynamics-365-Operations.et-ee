---
title: Konsolideeritud partiitellimused
description: "Selles artiklis kirjeldatakse konsolideeritud partiitellimuste mõistet."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PmfAddToConsOrder, PmfBulkItemConv, PmfBulkPackOnHand, PmfConsOrderListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19291
ms.assetid: e97f1d3d-1306-4c42-b2bc-d1755fe574d5
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 3ca9c920ea333bd21defebc29b40243d3a618a3d
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="consolidated-batch-orders"></a><span data-ttu-id="219c5-103">Konsolideeritud partiitellimused</span><span class="sxs-lookup"><span data-stu-id="219c5-103">Consolidated batch orders</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="219c5-104">Selles artiklis kirjeldatakse konsolideeritud partiitellimuste mõistet.</span><span class="sxs-lookup"><span data-stu-id="219c5-104">This article describes the concept of consolidated batch orders.</span></span>

<span data-ttu-id="219c5-105">Toodetud hulgikaup on emaüksus ja pakitud kaup on tütarüksus.</span><span class="sxs-lookup"><span data-stu-id="219c5-105">A bulk item that is produced is considered a parent item, whereas a packed item is considered a child item.</span></span> <span data-ttu-id="219c5-106">Hulgikauba ja pakitud kauba seost väljendab hulgikauba teisendamine.</span><span class="sxs-lookup"><span data-stu-id="219c5-106">The relation between the bulk item and the packed item is expressed in a bulk item conversion.</span></span> <span data-ttu-id="219c5-107">See hulgikauba teisendamine on määratletud hulgikaubas endas.</span><span class="sxs-lookup"><span data-stu-id="219c5-107">This bulk item conversion is defined on the bulk item itself.</span></span>  

<span data-ttu-id="219c5-108">Pakitud kaubad võib pakkida ühe või mitme suurusega konteineritesse, mida loetakse üheks ühikuks.</span><span class="sxs-lookup"><span data-stu-id="219c5-108">Packed items can be packaged into containers of either a single size or multiple sizes that are considered one unit.</span></span> <span data-ttu-id="219c5-109">Hulgikauba tellimuste konsolideerimisel saate vaadata kõiki seotud partiitellimusi ühes vaates,mis aitab teil tuvastada tööd, mis tuleb lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="219c5-109">By consolidating the orders for a bulk item, you can see all the related batch orders in a single view that can help you determine any remaining work that must be completed.</span></span>  

<span data-ttu-id="219c5-110">Konsolideeritud partiitellimus võib sisaldada järgmiste tellimuste mis tahes kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="219c5-110">A consolidated batch order can contain any combination of the following orders:</span></span>

-   <span data-ttu-id="219c5-111">Üks hulgitellimus ja mitu pakitud tellimust</span><span class="sxs-lookup"><span data-stu-id="219c5-111">A single bulk order and multiple packed orders</span></span>
-   <span data-ttu-id="219c5-112">Mitu hulgitellimust ja mitu pakitud tellimust</span><span class="sxs-lookup"><span data-stu-id="219c5-112">Multiple bulk orders and multiple packed orders</span></span>
-   <span data-ttu-id="219c5-113">Mitu hulgitellimust ja üks pakitud tellimust</span><span class="sxs-lookup"><span data-stu-id="219c5-113">Multiple bulk orders and a single packed order</span></span>
-   <span data-ttu-id="219c5-114">Ainult pakitud tellimused</span><span class="sxs-lookup"><span data-stu-id="219c5-114">Only packed orders</span></span>





