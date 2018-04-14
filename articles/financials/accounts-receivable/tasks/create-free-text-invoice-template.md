--- 
title: Vabas vormis arve malli loomine
description: "Salvestamisel kasutatakse demoettevõtte USMF-i."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d785922d1c6775d95ad5697eb6a872434e59c8e4
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="e766a-103">Vabas vormis arve malli loomine</span><span class="sxs-lookup"><span data-stu-id="e766a-103">Create a free text invoice template</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e766a-104">Salvestamisel kasutatakse demoettevõtte USMF-i.</span><span class="sxs-lookup"><span data-stu-id="e766a-104">This recording uses the USMF demo company.</span></span> <span data-ttu-id="e766a-105">Registreerimine on mõeldud müügireskontro arvete haldamise ja töötlemise eest vastutavale kasutajale.</span><span class="sxs-lookup"><span data-stu-id="e766a-105">The recording is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="e766a-106">Avage Müügireskontro > Arved > Korduvad arved > Vabas vormis arve mallid.</span><span class="sxs-lookup"><span data-stu-id="e766a-106">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="e766a-107">Kasutage seda vormi vabas vormis arve mallide loomiseks, mis võivad sisaldada arveridu, tasusid, arvestuse jaotuse malli ja pearaamatukonto teavet.</span><span class="sxs-lookup"><span data-stu-id="e766a-107">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="e766a-108">Uue vabas vormis arve malli loomiseks klõpsake suvandit Uus.</span><span class="sxs-lookup"><span data-stu-id="e766a-108">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="e766a-109">Sisestage väärtus väljale Malli nimi.</span><span class="sxs-lookup"><span data-stu-id="e766a-109">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="e766a-110">Malli nimi tuvastab kordumatult vabas vormis arve malli.</span><span class="sxs-lookup"><span data-stu-id="e766a-110">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="e766a-111">Kahel mallil ei tohi olla sama malli nimi.</span><span class="sxs-lookup"><span data-stu-id="e766a-111">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="e766a-112">Sisestage malli kirjeldus väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="e766a-112">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="e766a-113">Laiendage vahekaarti Arve read.</span><span class="sxs-lookup"><span data-stu-id="e766a-113">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="e766a-114">Sisestage arverea kirjeldus väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="e766a-114">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="e766a-115">Valige tulukonto väljalt Põhikonto.</span><span class="sxs-lookup"><span data-stu-id="e766a-115">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="e766a-116">Saate valida arve kogusumma jaoks kliendikrediidi vastaskande konto lehel Kliendi sisestusreeglid.</span><span class="sxs-lookup"><span data-stu-id="e766a-116">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="e766a-117">Klõpsake väljal Käibemaks otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e766a-117">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="e766a-118">Praeguse arverea käibemaksugrupp on kliendi konto vaike-käibemaksugrupp.</span><span class="sxs-lookup"><span data-stu-id="e766a-118">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="e766a-119">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e766a-119">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="e766a-120">Valige väljalt Käibemaksugrupp praeguse arverea kauba käibemaksugrupp.</span><span class="sxs-lookup"><span data-stu-id="e766a-120">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="e766a-121">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e766a-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="e766a-122">Sisestage arverea hind ühiku kohta või vaadake seda väljal Ühiku hind.</span><span class="sxs-lookup"><span data-stu-id="e766a-122">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="e766a-123">See summa korrutatakse arve rea summa määramiseks väärtusega väljal Kogus.</span><span class="sxs-lookup"><span data-stu-id="e766a-123">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="e766a-124">Lisage vabas vormis arve malli uus rida.</span><span class="sxs-lookup"><span data-stu-id="e766a-124">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="e766a-125">Sisestage arverea kirjeldus väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="e766a-125">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="e766a-126">Valige tulukonto väljalt Põhikonto.</span><span class="sxs-lookup"><span data-stu-id="e766a-126">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="e766a-127">Saate valida arve kogusumma jaoks kliendikrediidi vastaskande konto lehel Kliendi sisestusreeglid.</span><span class="sxs-lookup"><span data-stu-id="e766a-127">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="e766a-128">Klõpsake väljal Käibemaks otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e766a-128">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="e766a-129">Praeguse arverea käibemaksugrupp on kliendi konto vaike-käibemaksugrupp.</span><span class="sxs-lookup"><span data-stu-id="e766a-129">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="e766a-130">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e766a-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="e766a-131">Klõpsake väljal Kauba käibemaksugrupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e766a-131">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="e766a-132">Selle arverea kauba käibemaksugrupp.</span><span class="sxs-lookup"><span data-stu-id="e766a-132">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="e766a-133">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e766a-133">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="e766a-134">Arverea ühikute arvu sisestamine või vaatamine</span><span class="sxs-lookup"><span data-stu-id="e766a-134">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="e766a-135">See arv korrutatakse arve rea summa määramiseks väljal Ühiku hind oleva väärtusega.</span><span class="sxs-lookup"><span data-stu-id="e766a-135">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="e766a-136">Sisestage arve reale hind ühiku kohta või vaadake seda.</span><span class="sxs-lookup"><span data-stu-id="e766a-136">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="e766a-137">See summa korrutatakse arve rea summa määramiseks väärtusega väljal Kogus.</span><span class="sxs-lookup"><span data-stu-id="e766a-137">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="e766a-138">Vaadake ja muutke arvestuse jaotusi üksiku rea ja tütarridade puhul.</span><span class="sxs-lookup"><span data-stu-id="e766a-138">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="e766a-139">Arvestuse jaotused määratlevad, kuidas summat arvestatakse, näiteks tulu, maksude või tasude arvestamisel vabas vormis arvel.</span><span class="sxs-lookup"><span data-stu-id="e766a-139">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="e766a-140">Värskendage valitud arverea arvestuse jaotusi.</span><span class="sxs-lookup"><span data-stu-id="e766a-140">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="e766a-141">Klõpsake valikut Sule.</span><span class="sxs-lookup"><span data-stu-id="e766a-141">Click Close.</span></span>


