---
title: Valemi kopeerimine
description: See protseduur keskendub valemi loomisele, mis sisaldab samu koostisosi kui olemasolev valem, kuid väikese erinevusega.
author: ShylaThompson
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: dd87ded3bcc20b94fae723424d9cc6b94049a1a5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558762"
---
# <a name="copy-a-formula"></a><span data-ttu-id="e1376-103">Valemi kopeerimine</span><span class="sxs-lookup"><span data-stu-id="e1376-103">Copy a formula</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e1376-104">See protseduur keskendub valemi loomisele, mis sisaldab samu koostisosi kui olemasolev valem, kuid väikese erinevusega.</span><span class="sxs-lookup"><span data-stu-id="e1376-104">This procedure focuses on creating a formula that includes the same ingredients as an existing formula, but with minor differences.</span></span> <span data-ttu-id="e1376-105">Valemi ridade loomiseks saate kasutada funktsiooni Kopeeri, et kopeerida olemasolev valem, millel on enamik koostisainetest, mida vajate.</span><span class="sxs-lookup"><span data-stu-id="e1376-105">To create the formula lines, you can use the Copy function to copy an existing formula that has most of the ingredients that you need.</span></span> <span data-ttu-id="e1376-106">Seejärel saate uue versiooni üksikutele ridadele mis tahes vajalikke muudatusi teha.</span><span class="sxs-lookup"><span data-stu-id="e1376-106">You can then make any necessary changes to the individual lines in the new version.</span></span> <span data-ttu-id="e1376-107">Funktsiooni Kopeeri kasutades ei pea te mitut peaaegu ühesugust valemit looma.</span><span class="sxs-lookup"><span data-stu-id="e1376-107">By using the Copy function, you do not have to create multiple formulas that are almost identical.</span></span> <span data-ttu-id="e1376-108">Selle ülesande loomiseks kasutati demoettevõtte USP2 andmeid.</span><span class="sxs-lookup"><span data-stu-id="e1376-108">The demo data company used to create this task is USP2.</span></span>


## <a name="create-a-formula"></a><span data-ttu-id="e1376-109">Valemi loomine</span><span class="sxs-lookup"><span data-stu-id="e1376-109">Create a formula</span></span>
1. <span data-ttu-id="e1376-110">Avage Tooteteabe haldus > Kooslused ja valemid > Valemid.</span><span class="sxs-lookup"><span data-stu-id="e1376-110">Go to Product information management > Bills of materials and formulas > Formulas.</span></span>
2. <span data-ttu-id="e1376-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e1376-111">Click New.</span></span>
3. <span data-ttu-id="e1376-112">Sisestage väärtus väljale Valem.</span><span class="sxs-lookup"><span data-stu-id="e1376-112">In the Formula field, type a value.</span></span>
4. <span data-ttu-id="e1376-113">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="e1376-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="e1376-114">Sisestage valemile tähenduslik nimi.</span><span class="sxs-lookup"><span data-stu-id="e1376-114">Type a meaningful name for the formula.</span></span>  
5. <span data-ttu-id="e1376-115">Klõpsake väljal Koht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e1376-115">In the Site field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="e1376-116">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e1376-116">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="e1376-117">Klõpsake väljal Kaubagrupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e1376-117">In the Item group field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="e1376-118">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e1376-118">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="e1376-119">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e1376-119">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="e1376-120">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e1376-120">Click Save.</span></span>

## <a name="copy-formula-lines"></a><span data-ttu-id="e1376-121">Valemiridade kopeerimine</span><span class="sxs-lookup"><span data-stu-id="e1376-121">Copy formula lines</span></span>
1. <span data-ttu-id="e1376-122">Klõpsake toimingupaanil suvandit Valem.</span><span class="sxs-lookup"><span data-stu-id="e1376-122">On the Action Pane, click Formula.</span></span>
2. <span data-ttu-id="e1376-123">Klõpsake käsku Kopeeri.</span><span class="sxs-lookup"><span data-stu-id="e1376-123">Click Copy.</span></span>
3. <span data-ttu-id="e1376-124">Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e1376-124">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="e1376-125">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e1376-125">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="e1376-126">Klõpsake väljal Valemiversioon otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e1376-126">In the Formula version field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="e1376-127">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e1376-127">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="e1376-128">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e1376-128">Click OK.</span></span>

## <a name="adjust-copied-formula-lines"></a><span data-ttu-id="e1376-129">Kopeeritud valemiridade korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="e1376-129">Adjust copied formula lines</span></span>
1. <span data-ttu-id="e1376-130">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="e1376-130">In the list, mark the selected row.</span></span>
2. <span data-ttu-id="e1376-131">Klõpsake  Kustuta.</span><span class="sxs-lookup"><span data-stu-id="e1376-131">Click Delete.</span></span>
3. <span data-ttu-id="e1376-132">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="e1376-132">Click Yes.</span></span>

## <a name="approve-formula"></a><span data-ttu-id="e1376-133">Kinnita valem</span><span class="sxs-lookup"><span data-stu-id="e1376-133">Approve formula</span></span>
1. <span data-ttu-id="e1376-134">Klõpsake toimingupaanil suvandit Valem.</span><span class="sxs-lookup"><span data-stu-id="e1376-134">On the Action Pane, click Formula.</span></span>
2. <span data-ttu-id="e1376-135">Klõpsake suvandit Kinnita valem.</span><span class="sxs-lookup"><span data-stu-id="e1376-135">Click Approve formula.</span></span>
3. <span data-ttu-id="e1376-136">Klõpsake väljal Kinnitaja otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e1376-136">In the Approved by field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="e1376-137">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e1376-137">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="e1376-138">Klõpsake Vali.</span><span class="sxs-lookup"><span data-stu-id="e1376-138">Click Select.</span></span>
6. <span data-ttu-id="e1376-139">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e1376-139">Click OK.</span></span>

