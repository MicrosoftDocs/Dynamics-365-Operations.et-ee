---
title: "Teenuse tellimuste ühendamine"
description: "Saate hooldustellimusi ühendada."
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: b94d81c431a068e891a0e05e996594f7e0be19f9
ms.contentlocale: et-ee
ms.lasthandoff: 08/07/2018

---

# <a name="combine-service-orders"></a><span data-ttu-id="0d96e-103">Teenuse tellimuste ühendamine</span><span class="sxs-lookup"><span data-stu-id="0d96e-103">Combine service orders</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="0d96e-104">Kui loote hooldustellimuse read automaatselt vormil **Hoolduslepped**, saate valida ühe järgmistest suvanditest, et määrata, kuidas neid grupeerida.</span><span class="sxs-lookup"><span data-stu-id="0d96e-104">When you create service order lines automatically in the **Service agreements** form, you can choose one of the following options to specify how you want to group them:</span></span>

  - <span data-ttu-id="0d96e-105">**Hooldusleppe alusel**</span><span class="sxs-lookup"><span data-stu-id="0d96e-105">**By service agreement**</span></span>

  - <span data-ttu-id="0d96e-106">**Hooldustoimingu alusel**</span><span class="sxs-lookup"><span data-stu-id="0d96e-106">**By service task**</span></span>

  - <span data-ttu-id="0d96e-107">**Töövõtja alusel**</span><span class="sxs-lookup"><span data-stu-id="0d96e-107">**By employee**</span></span>

  - <span data-ttu-id="0d96e-108">**Teenuse objekti alusel**</span><span class="sxs-lookup"><span data-stu-id="0d96e-108">**By service object**</span></span>

## <a name="example"></a><span data-ttu-id="0d96e-109">Näide</span><span class="sxs-lookup"><span data-stu-id="0d96e-109">Example</span></span>

<span data-ttu-id="0d96e-110">Loote hooldusleppe alguskuupäevaga 31.03.2007.</span><span class="sxs-lookup"><span data-stu-id="0d96e-110">You create a service agreement that has a start date on 03-31-2007.</span></span> <span data-ttu-id="0d96e-111">Määrate väljal **Hooldustellimuste ühendamine** valiku **Teenuse objekti alusel**.</span><span class="sxs-lookup"><span data-stu-id="0d96e-111">In the **Combine service orders** field, you specify **By service object**.</span></span> <span data-ttu-id="0d96e-112">Seejärel saate luua järgmised teenuselepingu read:</span><span class="sxs-lookup"><span data-stu-id="0d96e-112">You then create the following service agreement lines:</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="0d96e-113">Lepperea number</span><span class="sxs-lookup"><span data-stu-id="0d96e-113">Agreement line number</span></span></p></th>
<th><p><span data-ttu-id="0d96e-114">Kande tüüp</span><span class="sxs-lookup"><span data-stu-id="0d96e-114">Transaction type</span></span></p></th>
<th><p><span data-ttu-id="0d96e-115">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="0d96e-115">Description</span></span></p></th>
<th><p><span data-ttu-id="0d96e-116">Intervall</span><span class="sxs-lookup"><span data-stu-id="0d96e-116">Interval</span></span></p></th>
<th><p><span data-ttu-id="0d96e-117">Teenuse objekt</span><span class="sxs-lookup"><span data-stu-id="0d96e-117">Service object</span></span></p></th>
<th><p><span data-ttu-id="0d96e-118">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="0d96e-118">Start date</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0d96e-119">1</span><span class="sxs-lookup"><span data-stu-id="0d96e-119">1</span></span></p></td>
<td><p><span data-ttu-id="0d96e-120"><strong>Tund</strong></span><span class="sxs-lookup"><span data-stu-id="0d96e-120"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="0d96e-121">SAL1</span><span class="sxs-lookup"><span data-stu-id="0d96e-121">SAL1</span></span></p></td>
<td><p><span data-ttu-id="0d96e-122">Iganädalane</span><span class="sxs-lookup"><span data-stu-id="0d96e-122">Weekly</span></span></p></td>
<td><p><span data-ttu-id="0d96e-123">X-1</span><span class="sxs-lookup"><span data-stu-id="0d96e-123">X-1</span></span></p></td>
<td><p><span data-ttu-id="0d96e-124">1.04.2007</span><span class="sxs-lookup"><span data-stu-id="0d96e-124">04-01-2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0d96e-125">2</span><span class="sxs-lookup"><span data-stu-id="0d96e-125">2</span></span></p></td>
<td><p><span data-ttu-id="0d96e-126"><strong>Tund</strong></span><span class="sxs-lookup"><span data-stu-id="0d96e-126"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="0d96e-127">SAL2</span><span class="sxs-lookup"><span data-stu-id="0d96e-127">SAL2</span></span></p></td>
<td><p><span data-ttu-id="0d96e-128">Üle nädala</span><span class="sxs-lookup"><span data-stu-id="0d96e-128">Biweekly</span></span></p></td>
<td><p><span data-ttu-id="0d96e-129">X-2</span><span class="sxs-lookup"><span data-stu-id="0d96e-129">X-2</span></span></p></td>
<td><p><span data-ttu-id="0d96e-130">1.04.2007</span><span class="sxs-lookup"><span data-stu-id="0d96e-130">04-01-2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0d96e-131">3</span><span class="sxs-lookup"><span data-stu-id="0d96e-131">3</span></span></p></td>
<td><p><span data-ttu-id="0d96e-132"><strong>Tund</strong></span><span class="sxs-lookup"><span data-stu-id="0d96e-132"><strong>Hour</strong></span></span></p></td>
<td><p><span data-ttu-id="0d96e-133">SAL3</span><span class="sxs-lookup"><span data-stu-id="0d96e-133">SAL3</span></span></p></td>
<td><p><span data-ttu-id="0d96e-134">Iganädalane</span><span class="sxs-lookup"><span data-stu-id="0d96e-134">Weekly</span></span></p></td>
<td><p><span data-ttu-id="0d96e-135">X-2</span><span class="sxs-lookup"><span data-stu-id="0d96e-135">X-2</span></span></p></td>
<td><p><span data-ttu-id="0d96e-136">1.04.2007</span><span class="sxs-lookup"><span data-stu-id="0d96e-136">04-01-2007</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="0d96e-137">Te ei määra kellaaja aknaid ühelegi teenuseleppe reale.</span><span class="sxs-lookup"><span data-stu-id="0d96e-137">You do not specify time windows for any of the service agreement lines.</span></span> <span data-ttu-id="0d96e-138">Seega ei liigu hooldustellimuse read arvutatud päevalt, millele nad langevad.</span><span class="sxs-lookup"><span data-stu-id="0d96e-138">Therefore, the service order lines will not move from the calculated day on which they fall.</span></span>

<span data-ttu-id="0d96e-139">Järgmiseks loote hooldustellimuse read vormist **Hooldustellimuste loomine** alates 01.04.2007 kuni 30.04.2007.</span><span class="sxs-lookup"><span data-stu-id="0d96e-139">Next, you generate service order lines from the **Create service orders** form from 04-01-2007 until 04-30-2007.</span></span>

<span data-ttu-id="0d96e-140">Kokku luuakse 10 teenusetellimust.</span><span class="sxs-lookup"><span data-stu-id="0d96e-140">In total, 10 service orders are created.</span></span> <span data-ttu-id="0d96e-141">Kuna teie valitud kombineeritud säte oli **Teenuse objekti alusel**, on kõigil loodud hooldustellimustel üksnes hooldustellimuse read ühe konkreetse hooldusobjektiga.</span><span class="sxs-lookup"><span data-stu-id="0d96e-141">Because the combined setting that you selected was **By service object**, all service orders that are created have only service order lines with one specific service object.</span></span> <span data-ttu-id="0d96e-142">Hooldustellimuse read, mis luuakse hooldusleppest ja millel on sama hoolduskuupäev ja hooldusobjekt, kombineeritakse samale hooldustellimusele.</span><span class="sxs-lookup"><span data-stu-id="0d96e-142">Service order lines that are generated from the service agreement and have the same service date and object are combined on the same service order.</span></span>


> [!NOTE]
> <P><span data-ttu-id="0d96e-143">Käesolevas näites pole kalendris, mis on määratud vormis <STRONG>Teenuste halduse parameetrid</STRONG>, suletud päevi.</span><span class="sxs-lookup"><span data-stu-id="0d96e-143">In this example, the calendar that is specified in the <STRONG>Service management parameters</STRONG> form has no closed days.</span></span></P>



<span data-ttu-id="0d96e-144">Hooldustellimuse ridade edasine grupeerimine hooldustellimustesse toimub hooldusleppe ridadel määratud kellaaja akna kohaselt.</span><span class="sxs-lookup"><span data-stu-id="0d96e-144">Additional grouping of service order lines into service orders occurs according to any time window that you specify on the service agreement lines.</span></span>

## <a name="see-also"></a><span data-ttu-id="0d96e-145">Vt ka</span><span class="sxs-lookup"><span data-stu-id="0d96e-145">See also</span></span>

[<span data-ttu-id="0d96e-146">Hooldustellimuste loomine automaatselt</span><span class="sxs-lookup"><span data-stu-id="0d96e-146">Create service orders automatically</span></span>](create-service-orders-automatically.md)

  



