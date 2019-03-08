---
title: Projekti ostutellimused
description: See artikkel kirjeldab erinevaid meetodeid, mille abil saate luua projekti ostutellimusi. Kasutatav meetod sõltub ostutellimuse eesmärgist ja sellest, millal ostetud kaupu tarbitakse ja nende eest projektile kulud arvestatakse.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 767a1805e7a2609c5c28bed891b42f7c8c3aaffc
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "348683"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="c9843-104">Projekti ostutellimused</span><span class="sxs-lookup"><span data-stu-id="c9843-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c9843-105">See artikkel kirjeldab erinevaid meetodeid, mille abil saate luua projekti ostutellimusi.</span><span class="sxs-lookup"><span data-stu-id="c9843-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="c9843-106">Kasutatav meetod sõltub ostutellimuse eesmärgist ja sellest, millal ostetud kaupu tarbitakse ja nende eest projektile kulud arvestatakse.</span><span class="sxs-lookup"><span data-stu-id="c9843-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

<span data-ttu-id="c9843-107">Microsoft Dynamics 365 for Finance and Operationsis saate kasutada projekti ostutellimuste loomiseks mitut meetodit.</span><span class="sxs-lookup"><span data-stu-id="c9843-107">In Microsoft Dynamics 365 for Finance and Operations, you can use multiple methods to create purchase orders for a project.</span></span> <span data-ttu-id="c9843-108">Kasutatav meetod sõltub ostutellimuse eesmärgist, sellest, millal ostetud kaupu tarbitakse ja millal ostetud kaupade eest projektile kulud arvestatakse.</span><span class="sxs-lookup"><span data-stu-id="c9843-108">The method that you use depends on the purpose of the purchase order, when the purchased items are consumed, and when the purchased items are charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="c9843-109">Ostutellimuse loomise meetodid</span><span class="sxs-lookup"><span data-stu-id="c9843-109">Methods for creating a purchase order</span></span>

<span data-ttu-id="c9843-110">Saate projekti haldamise ja raamatupidamise ostutellimuse loomiseks kasutada üht järgmistest meetoditest.</span><span class="sxs-lookup"><span data-stu-id="c9843-110">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="c9843-111">Ostutellimuse eesmärk määratleb, millal ostutellimust tarbitakse, ning seega ka selle, millal kaubad projekti kuludesse kantakse.</span><span class="sxs-lookup"><span data-stu-id="c9843-111">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c9843-112">Meetod</span><span class="sxs-lookup"><span data-stu-id="c9843-112">Method</span></span></th>
<th><span data-ttu-id="c9843-113">Eesmärk</span><span class="sxs-lookup"><span data-stu-id="c9843-113">Purpose</span></span></th>
<th><span data-ttu-id="c9843-114">Kaupade tarbimine</span><span class="sxs-lookup"><span data-stu-id="c9843-114">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c9843-115">Ostutellimuse loomine otse projektist.</span><span class="sxs-lookup"><span data-stu-id="c9843-115">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="c9843-116">Kasutage seda meetodit välishankijalt kaupade ostmiseks projektis tarbimiseks.</span><span class="sxs-lookup"><span data-stu-id="c9843-116">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="c9843-117">Ostutellimust saab luua kahel viisil.</span><span class="sxs-lookup"><span data-stu-id="c9843-117">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="c9843-118">Otse projekti kaudu.</span><span class="sxs-lookup"><span data-stu-id="c9843-118">From the project itself.</span></span> <span data-ttu-id="c9843-119">Sel juhul on projekt juba ostutellimuse jaoks määratletud.</span><span class="sxs-lookup"><span data-stu-id="c9843-119">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="c9843-120">Liikudes projekti ostutellimusele.</span><span class="sxs-lookup"><span data-stu-id="c9843-120">By navigating to the project purchase order.</span></span> <span data-ttu-id="c9843-121">Valida tuleb nii hankija kui projekt, mille jaoks ostutellimus luuakse.</span><span class="sxs-lookup"><span data-stu-id="c9843-121">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="c9843-122">Kaubad tarbitakse kui hankijaarve on uuendatud.</span><span class="sxs-lookup"><span data-stu-id="c9843-122">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9843-123">Ostutellimuse loomine müügitellimuse põhjal</span><span class="sxs-lookup"><span data-stu-id="c9843-123">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="c9843-124">Kasutage seda meetodit kaupade ostmiseks projekti müügitellimuse loomisel.</span><span class="sxs-lookup"><span data-stu-id="c9843-124">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="c9843-125">Kaubad tarbitakse siis, kui kliendile esitatakse müügitellimuse arve.</span><span class="sxs-lookup"><span data-stu-id="c9843-125">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="c9843-126">Ostutellimuse loomine kaubavajaduse põhjal</span><span class="sxs-lookup"><span data-stu-id="c9843-126">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="c9843-127">Kasutage seda meetodit kaupade ostmiseks projekti kaubavajaduse loomisel.</span><span class="sxs-lookup"><span data-stu-id="c9843-127">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="c9843-128">Kaubad tarbitakse kui kaubavajaduse saateleht on uuendatud.</span><span class="sxs-lookup"><span data-stu-id="c9843-128">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="c9843-129">Hankijaarve või saatelehe uuendamisel palutakse teil uuendada ka kaubavajaduse saateleht.</span><span class="sxs-lookup"><span data-stu-id="c9843-129">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="c9843-130">Lisateabe saamiseks vt [Kaubavajaduse ostutellimuse kaupade vastuvõtt](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="c9843-130">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>

