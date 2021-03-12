---
title: Vabas vormis arve malli loomine
description: See protseduur kirjeldab, kuidas luua vabas vormis arve malli.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee4fff7b148396faecef899c7a75365d3e1f47f3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991155"
---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="8c94e-103">Vabas vormis arve malli loomine</span><span class="sxs-lookup"><span data-stu-id="8c94e-103">Create a free text invoice template</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8c94e-104">Selle juhendava tutvustuse jaoks kasutage demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="8c94e-104">For this walkthrough, use the USMF demo company.</span></span> <span data-ttu-id="8c94e-105">See protseduur on mõeldud müügireskontro arvete haldamise ja töötlemise eest vastutavale kasutajale.</span><span class="sxs-lookup"><span data-stu-id="8c94e-105">This procedure is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="8c94e-106">Loo mall</span><span class="sxs-lookup"><span data-stu-id="8c94e-106">Create a template</span></span>

1. <span data-ttu-id="8c94e-107">Avage Müügireskontro > Arved > Korduvad arved > Vabas vormis arve mallid.</span><span class="sxs-lookup"><span data-stu-id="8c94e-107">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="8c94e-108">Kasutage seda vormi vabas vormis arve mallide loomiseks, mis võivad sisaldada arveridu, tasusid, arvestuse jaotuse malli ja pearaamatukonto teavet.</span><span class="sxs-lookup"><span data-stu-id="8c94e-108">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="8c94e-109">Uue vabas vormis arve malli loomiseks klõpsake suvandit Uus.</span><span class="sxs-lookup"><span data-stu-id="8c94e-109">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="8c94e-110">Sisestage väärtus väljale Malli nimi.</span><span class="sxs-lookup"><span data-stu-id="8c94e-110">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="8c94e-111">Malli nimi tuvastab kordumatult vabas vormis arve malli.</span><span class="sxs-lookup"><span data-stu-id="8c94e-111">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="8c94e-112">Kahel mallil ei tohi olla sama malli nimi.</span><span class="sxs-lookup"><span data-stu-id="8c94e-112">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="8c94e-113">Sisestage malli kirjeldus väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="8c94e-113">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="8c94e-114">Laiendage vahekaarti Arve read.</span><span class="sxs-lookup"><span data-stu-id="8c94e-114">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="8c94e-115">Sisestage arverea kirjeldus väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="8c94e-115">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="8c94e-116">Valige tulukonto väljalt Põhikonto.</span><span class="sxs-lookup"><span data-stu-id="8c94e-116">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="8c94e-117">Saate valida arve kogusumma jaoks kliendikrediidi vastaskande konto lehel Kliendi sisestusreeglid.</span><span class="sxs-lookup"><span data-stu-id="8c94e-117">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="8c94e-118">Klõpsake väljal Käibemaks otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="8c94e-118">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="8c94e-119">Praeguse arverea käibemaksugrupp on kliendi konto vaike-käibemaksugrupp.</span><span class="sxs-lookup"><span data-stu-id="8c94e-119">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="8c94e-120">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="8c94e-120">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="8c94e-121">Valige väljalt Käibemaksugrupp praeguse arverea kauba käibemaksugrupp.</span><span class="sxs-lookup"><span data-stu-id="8c94e-121">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="8c94e-122">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="8c94e-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="8c94e-123">Sisestage arverea hind ühiku kohta või vaadake seda väljal Ühiku hind.</span><span class="sxs-lookup"><span data-stu-id="8c94e-123">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="8c94e-124">See summa korrutatakse arve rea summa määramiseks väärtusega väljal Kogus.</span><span class="sxs-lookup"><span data-stu-id="8c94e-124">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="8c94e-125">Lisage vabas vormis arve malli uus rida.</span><span class="sxs-lookup"><span data-stu-id="8c94e-125">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="8c94e-126">Sisestage arverea kirjeldus väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="8c94e-126">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="8c94e-127">Valige tulukonto väljalt Põhikonto.</span><span class="sxs-lookup"><span data-stu-id="8c94e-127">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="8c94e-128">Saate valida arve kogusumma jaoks kliendikrediidi vastaskande konto lehel Kliendi sisestusreeglid.</span><span class="sxs-lookup"><span data-stu-id="8c94e-128">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="8c94e-129">Klõpsake väljal Käibemaks otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="8c94e-129">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="8c94e-130">Praeguse arverea käibemaksugrupp on kliendi konto vaike-käibemaksugrupp.</span><span class="sxs-lookup"><span data-stu-id="8c94e-130">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="8c94e-131">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="8c94e-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="8c94e-132">Klõpsake väljal Kauba käibemaksugrupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="8c94e-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="8c94e-133">Selle arverea kauba käibemaksugrupp.</span><span class="sxs-lookup"><span data-stu-id="8c94e-133">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="8c94e-134">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="8c94e-134">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="8c94e-135">Arverea ühikute arvu sisestamine või vaatamine</span><span class="sxs-lookup"><span data-stu-id="8c94e-135">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="8c94e-136">See arv korrutatakse arve rea summa määramiseks väljal Ühiku hind oleva väärtusega.</span><span class="sxs-lookup"><span data-stu-id="8c94e-136">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="8c94e-137">Sisestage arve reale hind ühiku kohta või vaadake seda.</span><span class="sxs-lookup"><span data-stu-id="8c94e-137">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="8c94e-138">See summa korrutatakse arve rea summa määramiseks väärtusega väljal Kogus.</span><span class="sxs-lookup"><span data-stu-id="8c94e-138">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="8c94e-139">Vaadake ja muutke arvestuse jaotusi üksiku rea ja tütarridade puhul.</span><span class="sxs-lookup"><span data-stu-id="8c94e-139">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="8c94e-140">Arvestuse jaotused määratlevad, kuidas summat arvestatakse, näiteks tulu, maksude või tasude arvestamisel vabas vormis arvel.</span><span class="sxs-lookup"><span data-stu-id="8c94e-140">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="8c94e-141">Värskendage valitud arverea arvestuse jaotusi.</span><span class="sxs-lookup"><span data-stu-id="8c94e-141">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="8c94e-142">Klõpsake valikut Sule.</span><span class="sxs-lookup"><span data-stu-id="8c94e-142">Click Close.</span></span>

## <a name="save-a-free-text-invoice-as-a-template"></a><span data-ttu-id="8c94e-143">Vabas vormis arve salvestamine mallina</span><span class="sxs-lookup"><span data-stu-id="8c94e-143">Save a free text invoice as a template</span></span>
<span data-ttu-id="8c94e-144">Samuti saate salvestada olemasoleva vabas vormis arve mallina.</span><span class="sxs-lookup"><span data-stu-id="8c94e-144">You can also save an existing free text invoice as a template.</span></span> <span data-ttu-id="8c94e-145">Kui valite vahekaardil Arve suvandi Salvesta malli, lisage mallile nimi ja kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="8c94e-145">When you select Save to template from the Invoice tab, provide a name and a description for the template.</span></span> <span data-ttu-id="8c94e-146">Kui selle nimega mall on juba olemas, näete teatist, et selle nimega mall on juba olemas.</span><span class="sxs-lookup"><span data-stu-id="8c94e-146">If a template with the name already exists, you will see a notification that a template with that name already exists.</span></span> <span data-ttu-id="8c94e-147">Saate klõpsata nuppu OK malli asendamiseks.</span><span class="sxs-lookup"><span data-stu-id="8c94e-147">You can still click on Ok to replace it.</span></span> 
