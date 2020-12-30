---
title: Vähendamispäevade näide
description: Vähendamispäevade näide,
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMASubscriptionTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 87c46cd7ee7410e1c7cb88868cd19f5075482f8c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426002"
---
# <a name="reduction-days-example"></a><span data-ttu-id="8ba7e-103">Vähendamispäevade näide</span><span class="sxs-lookup"><span data-stu-id="8ba7e-103">Reduction days example</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="8ba7e-104">Olete loonud kordustellimuse kande kliendi kordustellimuse haldamiseks, nagu kirjeldatud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="8ba7e-104">You have created a subscription transaction for a customer's maintenance subscription, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="8ba7e-105">Kuupäevast</span><span class="sxs-lookup"><span data-stu-id="8ba7e-105">From date</span></span></p></th>
<th><p><span data-ttu-id="8ba7e-106">Kuupäevani</span><span class="sxs-lookup"><span data-stu-id="8ba7e-106">To date</span></span></p></th>
<th><p><span data-ttu-id="8ba7e-107">Korduv tellimus</span><span class="sxs-lookup"><span data-stu-id="8ba7e-107">Subscription</span></span></p></th>
<th><p><span data-ttu-id="8ba7e-108">Kordustellimuse tüüp</span><span class="sxs-lookup"><span data-stu-id="8ba7e-108">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="8ba7e-109">Project</span><span class="sxs-lookup"><span data-stu-id="8ba7e-109">Project</span></span></p></th>
<th><p><span data-ttu-id="8ba7e-110">Kategooria</span><span class="sxs-lookup"><span data-stu-id="8ba7e-110">Category</span></span></p></th>
<th><p><span data-ttu-id="8ba7e-111">Müügivaluuta</span><span class="sxs-lookup"><span data-stu-id="8ba7e-111">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="8ba7e-112">Müügihind</span><span class="sxs-lookup"><span data-stu-id="8ba7e-112">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8ba7e-113">01. märts 2011</span><span class="sxs-lookup"><span data-stu-id="8ba7e-113">March 01, 2011</span></span></p></td>
<td><p><span data-ttu-id="8ba7e-114">31. märts 2011</span><span class="sxs-lookup"><span data-stu-id="8ba7e-114">March 31, 2011</span></span></p></td>
<td><p><span data-ttu-id="8ba7e-115">NR-2</span><span class="sxs-lookup"><span data-stu-id="8ba7e-115">NR-2</span></span></p></td>
<td><p><span data-ttu-id="8ba7e-116"><strong>Tavaline</strong></span><span class="sxs-lookup"><span data-stu-id="8ba7e-116"><strong>Regular</strong></span></span></p></td>
<td><p><span data-ttu-id="8ba7e-117">9013</span><span class="sxs-lookup"><span data-stu-id="8ba7e-117">9013</span></span></p></td>
<td><p><span data-ttu-id="8ba7e-118">SubCat2</span><span class="sxs-lookup"><span data-stu-id="8ba7e-118">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="8ba7e-119"> eurot</span><span class="sxs-lookup"><span data-stu-id="8ba7e-119">EUR</span></span></p></td>
<td><p><span data-ttu-id="8ba7e-120">200,00</span><span class="sxs-lookup"><span data-stu-id="8ba7e-120">200.00</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8ba7e-121">Klient teatab, et ei vaja teenust kahel päeval (10. ja 11. märtsil).</span><span class="sxs-lookup"><span data-stu-id="8ba7e-121">The customer reports that it does not need service coverage for two days (March 10 and March 11).</span></span> <span data-ttu-id="8ba7e-122">Nõustute vähendama kordustellimust nende kahe päeva võrra.</span><span class="sxs-lookup"><span data-stu-id="8ba7e-122">You agree to reduce the subscription by these two days.</span></span>

<span data-ttu-id="8ba7e-123">Loote uue, tüübi **Vähendamispäevad** kande, nagu kirjeldatud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="8ba7e-123">You create a new transaction of the **Reduction days** type, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="8ba7e-124">Kuupäevast</span><span class="sxs-lookup"><span data-stu-id="8ba7e-124">From date</span></span></p></th>
<th><p><span data-ttu-id="8ba7e-125">Kuupäevani</span><span class="sxs-lookup"><span data-stu-id="8ba7e-125">To date</span></span></p></th>
<th><p><span data-ttu-id="8ba7e-126">Korduv tellimus</span><span class="sxs-lookup"><span data-stu-id="8ba7e-126">Subscription</span></span></p></th>
<th><p><span data-ttu-id="8ba7e-127">Kordustellimuse tüüp</span><span class="sxs-lookup"><span data-stu-id="8ba7e-127">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="8ba7e-128">Project</span><span class="sxs-lookup"><span data-stu-id="8ba7e-128">Project</span></span></p></th>
<th><p><span data-ttu-id="8ba7e-129">Kategooria</span><span class="sxs-lookup"><span data-stu-id="8ba7e-129">Category</span></span></p></th>
<th><p><span data-ttu-id="8ba7e-130">Müügivaluuta</span><span class="sxs-lookup"><span data-stu-id="8ba7e-130">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="8ba7e-131">Müügihind</span><span class="sxs-lookup"><span data-stu-id="8ba7e-131">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8ba7e-132">10. märts 2011</span><span class="sxs-lookup"><span data-stu-id="8ba7e-132">March 10, 2011</span></span></p></td>
<td><p><span data-ttu-id="8ba7e-133">11. märts 2011</span><span class="sxs-lookup"><span data-stu-id="8ba7e-133">March 11, 2011</span></span></p></td>
<td><p><span data-ttu-id="8ba7e-134">NR-2</span><span class="sxs-lookup"><span data-stu-id="8ba7e-134">NR-2</span></span></p></td>
<td><p><span data-ttu-id="8ba7e-135"><strong>Vähendamispäevad</strong></span><span class="sxs-lookup"><span data-stu-id="8ba7e-135"><strong>Reduction days</strong></span></span></p></td>
<td><p><span data-ttu-id="8ba7e-136">9013</span><span class="sxs-lookup"><span data-stu-id="8ba7e-136">9013</span></span></p></td>
<td><p><span data-ttu-id="8ba7e-137">SubCat2</span><span class="sxs-lookup"><span data-stu-id="8ba7e-137">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="8ba7e-138"> eurot</span><span class="sxs-lookup"><span data-stu-id="8ba7e-138">EUR</span></span></p></td>
<td><p><span data-ttu-id="8ba7e-139">-12,90</span><span class="sxs-lookup"><span data-stu-id="8ba7e-139">-12.90</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8ba7e-140">Kui 2011. aasta märtsi kanded arveldatakse, vähendatakse müügihinda 200 eurot 12.90 euro võrra.</span><span class="sxs-lookup"><span data-stu-id="8ba7e-140">When the transactions for March 2011 are invoiced, the sales price of EUR 200 is reduced by EUR 12.90.</span></span> <span data-ttu-id="8ba7e-141">Kordustellimuse kande arveldatav summa on seega 187.10 eurot ja kahe kande eest esitatakse kokku arve summas 187.10 eurot.</span><span class="sxs-lookup"><span data-stu-id="8ba7e-141">The chargeable amount for the subscription transaction is therefore EUR 187.10, and two transactions are invoiced at a total of EUR 187.10.</span></span>

## <a name="see-also"></a><span data-ttu-id="8ba7e-142">Vt ka</span><span class="sxs-lookup"><span data-stu-id="8ba7e-142">See also</span></span>

[<span data-ttu-id="8ba7e-143">Kordustellimuste tasude päevade vähendamine</span><span class="sxs-lookup"><span data-stu-id="8ba7e-143">Reduce the days on subscription fees</span></span>](reduce-the-days-on-subscription-fees.md)

  


