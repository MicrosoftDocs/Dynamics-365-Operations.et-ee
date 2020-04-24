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
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c9d2407fde9dc586d296b0ddd61478aa84a71132
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204443"
---
# <a name="reduction-days-example"></a><span data-ttu-id="8ed6c-103">Vähendamispäevade näide</span><span class="sxs-lookup"><span data-stu-id="8ed6c-103">Reduction days example</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="8ed6c-104">Olete loonud kordustellimuse kande kliendi kordustellimuse haldamiseks, nagu kirjeldatud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="8ed6c-104">You have created a subscription transaction for a customer's maintenance subscription, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="8ed6c-105">Kuupäevast</span><span class="sxs-lookup"><span data-stu-id="8ed6c-105">From date</span></span></p></th>
<th><p><span data-ttu-id="8ed6c-106">Kuupäevani</span><span class="sxs-lookup"><span data-stu-id="8ed6c-106">To date</span></span></p></th>
<th><p><span data-ttu-id="8ed6c-107">Korduv tellimus</span><span class="sxs-lookup"><span data-stu-id="8ed6c-107">Subscription</span></span></p></th>
<th><p><span data-ttu-id="8ed6c-108">Kordustellimuse tüüp</span><span class="sxs-lookup"><span data-stu-id="8ed6c-108">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="8ed6c-109">Project</span><span class="sxs-lookup"><span data-stu-id="8ed6c-109">Project</span></span></p></th>
<th><p><span data-ttu-id="8ed6c-110">Kategooria</span><span class="sxs-lookup"><span data-stu-id="8ed6c-110">Category</span></span></p></th>
<th><p><span data-ttu-id="8ed6c-111">Müügivaluuta</span><span class="sxs-lookup"><span data-stu-id="8ed6c-111">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="8ed6c-112">Müügihind</span><span class="sxs-lookup"><span data-stu-id="8ed6c-112">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8ed6c-113">01. märts 2011</span><span class="sxs-lookup"><span data-stu-id="8ed6c-113">March 01, 2011</span></span></p></td>
<td><p><span data-ttu-id="8ed6c-114">31. märts 2011</span><span class="sxs-lookup"><span data-stu-id="8ed6c-114">March 31, 2011</span></span></p></td>
<td><p><span data-ttu-id="8ed6c-115">NR-2</span><span class="sxs-lookup"><span data-stu-id="8ed6c-115">NR-2</span></span></p></td>
<td><p><span data-ttu-id="8ed6c-116"><strong>Tavaline</strong></span><span class="sxs-lookup"><span data-stu-id="8ed6c-116"><strong>Regular</strong></span></span></p></td>
<td><p><span data-ttu-id="8ed6c-117">9013</span><span class="sxs-lookup"><span data-stu-id="8ed6c-117">9013</span></span></p></td>
<td><p><span data-ttu-id="8ed6c-118">SubCat2</span><span class="sxs-lookup"><span data-stu-id="8ed6c-118">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="8ed6c-119"> eurot</span><span class="sxs-lookup"><span data-stu-id="8ed6c-119">EUR</span></span></p></td>
<td><p><span data-ttu-id="8ed6c-120">200,00</span><span class="sxs-lookup"><span data-stu-id="8ed6c-120">200.00</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8ed6c-121">Klient teatab, et ei vaja teenust kahel päeval (10. ja 11. märtsil).</span><span class="sxs-lookup"><span data-stu-id="8ed6c-121">The customer reports that it does not need service coverage for two days (March 10 and March 11).</span></span> <span data-ttu-id="8ed6c-122">Nõustute vähendama kordustellimust nende kahe päeva võrra.</span><span class="sxs-lookup"><span data-stu-id="8ed6c-122">You agree to reduce the subscription by these two days.</span></span>

<span data-ttu-id="8ed6c-123">Loote uue, tüübi **Vähendamispäevad** kande, nagu kirjeldatud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="8ed6c-123">You create a new transaction of the **Reduction days** type, as described in the following table.</span></span>

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
<th><p><span data-ttu-id="8ed6c-124">Kuupäevast</span><span class="sxs-lookup"><span data-stu-id="8ed6c-124">From date</span></span></p></th>
<th><p><span data-ttu-id="8ed6c-125">Kuupäevani</span><span class="sxs-lookup"><span data-stu-id="8ed6c-125">To date</span></span></p></th>
<th><p><span data-ttu-id="8ed6c-126">Korduv tellimus</span><span class="sxs-lookup"><span data-stu-id="8ed6c-126">Subscription</span></span></p></th>
<th><p><span data-ttu-id="8ed6c-127">Kordustellimuse tüüp</span><span class="sxs-lookup"><span data-stu-id="8ed6c-127">Subscription type</span></span></p></th>
<th><p><span data-ttu-id="8ed6c-128">Project</span><span class="sxs-lookup"><span data-stu-id="8ed6c-128">Project</span></span></p></th>
<th><p><span data-ttu-id="8ed6c-129">Kategooria</span><span class="sxs-lookup"><span data-stu-id="8ed6c-129">Category</span></span></p></th>
<th><p><span data-ttu-id="8ed6c-130">Müügivaluuta</span><span class="sxs-lookup"><span data-stu-id="8ed6c-130">Sales currency</span></span></p></th>
<th><p><span data-ttu-id="8ed6c-131">Müügihind</span><span class="sxs-lookup"><span data-stu-id="8ed6c-131">Sales price</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8ed6c-132">10. märts 2011</span><span class="sxs-lookup"><span data-stu-id="8ed6c-132">March 10, 2011</span></span></p></td>
<td><p><span data-ttu-id="8ed6c-133">11. märts 2011</span><span class="sxs-lookup"><span data-stu-id="8ed6c-133">March 11, 2011</span></span></p></td>
<td><p><span data-ttu-id="8ed6c-134">NR-2</span><span class="sxs-lookup"><span data-stu-id="8ed6c-134">NR-2</span></span></p></td>
<td><p><span data-ttu-id="8ed6c-135"><strong>Vähendamispäevad</strong></span><span class="sxs-lookup"><span data-stu-id="8ed6c-135"><strong>Reduction days</strong></span></span></p></td>
<td><p><span data-ttu-id="8ed6c-136">9013</span><span class="sxs-lookup"><span data-stu-id="8ed6c-136">9013</span></span></p></td>
<td><p><span data-ttu-id="8ed6c-137">SubCat2</span><span class="sxs-lookup"><span data-stu-id="8ed6c-137">SubCat2</span></span></p></td>
<td><p><span data-ttu-id="8ed6c-138"> eurot</span><span class="sxs-lookup"><span data-stu-id="8ed6c-138">EUR</span></span></p></td>
<td><p><span data-ttu-id="8ed6c-139">-12,90</span><span class="sxs-lookup"><span data-stu-id="8ed6c-139">-12.90</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8ed6c-140">Kui 2011. aasta märtsi kanded arveldatakse, vähendatakse müügihinda 200 eurot 12.90 euro võrra.</span><span class="sxs-lookup"><span data-stu-id="8ed6c-140">When the transactions for March 2011 are invoiced, the sales price of EUR 200 is reduced by EUR 12.90.</span></span> <span data-ttu-id="8ed6c-141">Kordustellimuse kande arveldatav summa on seega 187.10 eurot ja kahe kande eest esitatakse kokku arve summas 187.10 eurot.</span><span class="sxs-lookup"><span data-stu-id="8ed6c-141">The chargeable amount for the subscription transaction is therefore EUR 187.10, and two transactions are invoiced at a total of EUR 187.10.</span></span>

## <a name="see-also"></a><span data-ttu-id="8ed6c-142">Vt ka</span><span class="sxs-lookup"><span data-stu-id="8ed6c-142">See also</span></span>

[<span data-ttu-id="8ed6c-143">Kordustellimuste tasude päevade vähendamine</span><span class="sxs-lookup"><span data-stu-id="8ed6c-143">Reduce the days on subscription fees</span></span>](reduce-the-days-on-subscription-fees.md)

  


