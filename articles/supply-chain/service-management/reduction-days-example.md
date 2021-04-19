---
title: Vähendamispäevade näide
description: Vähendamispäevade näide,
author: ShylaThompson
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 90a2efff0add508ddb3d750bb3ca27ea35bf113a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836058"
---
# <a name="reduction-days-example"></a><span data-ttu-id="1ed70-103">Vähendamispäevade näide</span><span class="sxs-lookup"><span data-stu-id="1ed70-103">Reduction days example</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="1ed70-104">Olete loonud kordustellimuse kande kliendi kordustellimuse haldamiseks, nagu kirjeldatud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="1ed70-104">You have created a subscription transaction for a customer's maintenance subscription, as described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1ed70-105">Kuupäevast</span><span class="sxs-lookup"><span data-stu-id="1ed70-105">From date</span></span></p></th>
<th><p><span data-ttu-id="1ed70-106">Kuupäevani</span><span class="sxs-lookup"><span data-stu-id="1ed70-106">To date</span></span></p></th>
<th><p><span data-ttu-id="1ed70-107">Korduv tellimus</span><span class="sxs-lookup"><span data-stu-id="1ed70-107">Subscription</span></span></p></th>
<th><p><span data-ttu-id="1ed70-108">Kordustellimuse tüüp</span><span class="sxs-lookup"><span data-stu-id="1ed70-108">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="1ed70-109">Project</span><span class="sxs-lookup"><span data-stu-id="1ed70-109">Project</span></span></p></th>
<th><p><span data-ttu-id="1ed70-110">Kategooria</span><span class="sxs-lookup"><span data-stu-id="1ed70-110">Category</span></span></p></th>
<th><p><span data-ttu-id="1ed70-111">Müügivaluuta</span><span class="sxs-lookup"><span data-stu-id="1ed70-111">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="1ed70-112">Müügihind</span><span class="sxs-lookup"><span data-stu-id="1ed70-112">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1ed70-113">01. märts 2011</span><span class="sxs-lookup"><span data-stu-id="1ed70-113">March 01, 2011</span></span></p></td>
<td><p><span data-ttu-id="1ed70-114">31. märts 2011</span><span class="sxs-lookup"><span data-stu-id="1ed70-114">March 31, 2011</span></span></p></td>
<td><p><span data-ttu-id="1ed70-115">NR-2</span><span class="sxs-lookup"><span data-stu-id="1ed70-115">NR-2</span></span></p></td>
<td><p><span data-ttu-id="1ed70-116"><strong>Tavaline</strong></span><span class="sxs-lookup"><span data-stu-id="1ed70-116"><strong>Regular</strong></span></span></p></td>
<td><p><span data-ttu-id="1ed70-117">9013</span><span class="sxs-lookup"><span data-stu-id="1ed70-117">9013</span></span></p></td>
<td><p><span data-ttu-id="1ed70-118">SubCat2</span><span class="sxs-lookup"><span data-stu-id="1ed70-118">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="1ed70-119"> eurot</span><span class="sxs-lookup"><span data-stu-id="1ed70-119">EUR</span></span></p></td>
<td><p><span data-ttu-id="1ed70-120">200,00</span><span class="sxs-lookup"><span data-stu-id="1ed70-120">200.00</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1ed70-121">Klient teatab, et ei vaja teenust kahel päeval (10. ja 11. märtsil).</span><span class="sxs-lookup"><span data-stu-id="1ed70-121">The customer reports that it does not need service coverage for two days (March 10 and March 11).</span></span> <span data-ttu-id="1ed70-122">Nõustute vähendama kordustellimust nende kahe päeva võrra.</span><span class="sxs-lookup"><span data-stu-id="1ed70-122">You agree to reduce the subscription by these two days.</span></span>

<span data-ttu-id="1ed70-123">Loote uue, tüübi **Vähendamispäevad** kande, nagu kirjeldatud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="1ed70-123">You create a new transaction of the **Reduction days** type, as described in the following table.</span></span>

<table>
<colgroup>
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
<col style="width: 12%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="1ed70-124">Kuupäevast</span><span class="sxs-lookup"><span data-stu-id="1ed70-124">From date</span></span></p></th>
<th><p><span data-ttu-id="1ed70-125">Kuupäevani</span><span class="sxs-lookup"><span data-stu-id="1ed70-125">To date</span></span></p></th>
<th><p><span data-ttu-id="1ed70-126">Korduv tellimus</span><span class="sxs-lookup"><span data-stu-id="1ed70-126">Subscription</span></span></p></th>
<th><p><span data-ttu-id="1ed70-127">Kordustellimuse tüüp</span><span class="sxs-lookup"><span data-stu-id="1ed70-127">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="1ed70-128">Project</span><span class="sxs-lookup"><span data-stu-id="1ed70-128">Project</span></span></p></th>
<th><p><span data-ttu-id="1ed70-129">Kategooria</span><span class="sxs-lookup"><span data-stu-id="1ed70-129">Category</span></span></p></th>
<th><p><span data-ttu-id="1ed70-130">Müügivaluuta</span><span class="sxs-lookup"><span data-stu-id="1ed70-130">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="1ed70-131">Müügihind</span><span class="sxs-lookup"><span data-stu-id="1ed70-131">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1ed70-132">10. märts 2011</span><span class="sxs-lookup"><span data-stu-id="1ed70-132">March 10, 2011</span></span></p></td>
<td><p><span data-ttu-id="1ed70-133">11. märts 2011</span><span class="sxs-lookup"><span data-stu-id="1ed70-133">March 11, 2011</span></span></p></td>
<td><p><span data-ttu-id="1ed70-134">NR-2</span><span class="sxs-lookup"><span data-stu-id="1ed70-134">NR-2</span></span></p></td>
<td><p><span data-ttu-id="1ed70-135"><strong>Vähendamispäevad</strong></span><span class="sxs-lookup"><span data-stu-id="1ed70-135"><strong>Reduction days</strong></span></span></p></td>
<td><p><span data-ttu-id="1ed70-136">9013</span><span class="sxs-lookup"><span data-stu-id="1ed70-136">9013</span></span></p></td>
<td><p><span data-ttu-id="1ed70-137">SubCat2</span><span class="sxs-lookup"><span data-stu-id="1ed70-137">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="1ed70-138"> eurot</span><span class="sxs-lookup"><span data-stu-id="1ed70-138">EUR</span></span></p></td>
<td><p><span data-ttu-id="1ed70-139">-12,90</span><span class="sxs-lookup"><span data-stu-id="1ed70-139">-12.90</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1ed70-140">Kui 2011. aasta märtsi kanded arveldatakse, vähendatakse müügihinda 200 eurot 12.90 euro võrra.</span><span class="sxs-lookup"><span data-stu-id="1ed70-140">When the transactions for March 2011 are invoiced, the sales price of EUR 200 is reduced by EUR 12.90.</span></span> <span data-ttu-id="1ed70-141">Kordustellimuse kande arveldatav summa on seega 187.10 eurot ja kahe kande eest esitatakse kokku arve summas 187.10 eurot.</span><span class="sxs-lookup"><span data-stu-id="1ed70-141">The chargeable amount for the subscription transaction is therefore EUR 187.10, and two transactions are invoiced at a total of EUR 187.10.</span></span>

## <a name="see-also"></a><span data-ttu-id="1ed70-142">Vt ka</span><span class="sxs-lookup"><span data-stu-id="1ed70-142">See also</span></span>

[<span data-ttu-id="1ed70-143">Kordustellimuste tasude päevade vähendamine</span><span class="sxs-lookup"><span data-stu-id="1ed70-143">Reduce the days on subscription fees</span></span>](reduce-the-days-on-subscription-fees.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]