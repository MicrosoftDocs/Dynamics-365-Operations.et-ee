---
title: Loo laenuartikleid
description: Laenuartiklid on kirjed, mis aitavad teil jälgida füüsilisi kaupu, näiteks telefone või arvuteid, mida teie ettevõte töötajatele laenab.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmLoanType, DefaultDashboard, HcmLoanItem, HcmWorkerLookUp
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 75b2f17eb41ead7422276f72429eb6ede2ef4759
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/19/2019
ms.locfileid: "856227"
---
# <a name="create-loan-items"></a><span data-ttu-id="9b4f3-103">Loo laenuartikleid</span><span class="sxs-lookup"><span data-stu-id="9b4f3-103">Create loan items</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9b4f3-104">Laenuartiklid on kirjed, mis aitavad teil jälgida füüsilisi kaupu, näiteks telefone või arvuteid, mida teie ettevõte töötajatele laenab.</span><span class="sxs-lookup"><span data-stu-id="9b4f3-104">Loan items are records that help you track physical items, such as phones or computers, that your company lends to workers.</span></span> <span data-ttu-id="9b4f3-105">Iga füüsiline kaup peab laenuartiklile vastama.</span><span class="sxs-lookup"><span data-stu-id="9b4f3-105">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="9b4f3-106">Iga laenuartikli kirjel tuleb kirjeldada, mida laenatakse, kes on laenu eest vastutav ja mitmeks päevaks võib artiklit laenata.</span><span class="sxs-lookup"><span data-stu-id="9b4f3-106">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can be on loan.</span></span> <span data-ttu-id="9b4f3-107">Saate luua mitu laenuartiklit, nagu võtmed, pääsukaardid või vormirõivad, samal ajal.</span><span class="sxs-lookup"><span data-stu-id="9b4f3-107">You can create multiple loan items, such as keys, access cards, or uniforms, at the same time.</span></span> <span data-ttu-id="9b4f3-108">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="9b4f3-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-loan-types"></a><span data-ttu-id="9b4f3-109">Laenutüüpide loomine</span><span class="sxs-lookup"><span data-stu-id="9b4f3-109">Create Loan types</span></span>
1. <span data-ttu-id="9b4f3-110">Avage Inimressursid > Töötajad > Laenuartiklid > Laenutüübid.</span><span class="sxs-lookup"><span data-stu-id="9b4f3-110">Go to Human resources > Workers > Loan items > Loan types.</span></span>
2. <span data-ttu-id="9b4f3-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="9b4f3-111">Click New.</span></span>
3. <span data-ttu-id="9b4f3-112">Sisestage väärtus väljale Laenu tüüp.</span><span class="sxs-lookup"><span data-stu-id="9b4f3-112">In the Loan type field, type a value.</span></span>
4. <span data-ttu-id="9b4f3-113">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="9b4f3-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9b4f3-114">Sisestage päevade arv, mille võrra võib seda tüüpi laenuartiklite tagastamine tähtaja ületada.</span><span class="sxs-lookup"><span data-stu-id="9b4f3-114">Enter the number of days that items assigned to this loan type can be overdue.</span></span> 
6. <span data-ttu-id="9b4f3-115">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="9b4f3-115">Click Save.</span></span>
7. <span data-ttu-id="9b4f3-116">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9b4f3-116">Close the page.</span></span>
8. <span data-ttu-id="9b4f3-117">Värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="9b4f3-117">Refresh the page.</span></span>

## <a name="create-loan-items"></a><span data-ttu-id="9b4f3-118">Laenuartiklite loomine</span><span class="sxs-lookup"><span data-stu-id="9b4f3-118">Create Loan items</span></span>
1. <span data-ttu-id="9b4f3-119">Avage Inimressursid > Töötajad > Laenuartiklid > Laenuartiklid.</span><span class="sxs-lookup"><span data-stu-id="9b4f3-119">Go to Human resources > Workers > Loan items > Loan items.</span></span>
2. <span data-ttu-id="9b4f3-120">Klõpsake suvandit Loo laenuartikleid.</span><span class="sxs-lookup"><span data-stu-id="9b4f3-120">Click Create loan items.</span></span>
3. <span data-ttu-id="9b4f3-121">Väljale Kogus väljale Protsessi kogus.</span><span class="sxs-lookup"><span data-stu-id="9b4f3-121">In the Qty. field, enter a number.</span></span>
4. <span data-ttu-id="9b4f3-122">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="9b4f3-122">In the Description field, type a value.</span></span>
5. <span data-ttu-id="9b4f3-123">Klõpsake väljal Laenu tüüp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="9b4f3-123">In the Loan type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="9b4f3-124">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="9b4f3-124">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="9b4f3-125">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="9b4f3-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="9b4f3-126">Sisestage päevade arv, mille jooksul artikkel võib olla välja laenatud.</span><span class="sxs-lookup"><span data-stu-id="9b4f3-126">Enter the number of days the item can be on loan.</span></span>
    * <span data-ttu-id="9b4f3-127">Lehe Laenatud seadmed välja Plaanitud tagastus vaikeväärtus arvutatakse, liites tänasele kuupäevale selle numbri.</span><span class="sxs-lookup"><span data-stu-id="9b4f3-127">The default value for the Planned return field on the Loaned equipment page is calculated as the current date plus this number.</span></span>  
9. <span data-ttu-id="9b4f3-128">Klõpsake väljal Vastutav isik otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="9b4f3-128">In the Person in charge field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="9b4f3-129">Klõpsake Vali.</span><span class="sxs-lookup"><span data-stu-id="9b4f3-129">Click Select.</span></span>
11. <span data-ttu-id="9b4f3-130">Sisestage number väljale Algväärtus.</span><span class="sxs-lookup"><span data-stu-id="9b4f3-130">In the Starting value field, enter a number.</span></span>
12. <span data-ttu-id="9b4f3-131">Sisestage number väljale Intervall.</span><span class="sxs-lookup"><span data-stu-id="9b4f3-131">In the Interval field, enter a number.</span></span>
13. <span data-ttu-id="9b4f3-132">Sisestage väärtus väljale Vorming.</span><span class="sxs-lookup"><span data-stu-id="9b4f3-132">In the Format field, type a value.</span></span>
    * <span data-ttu-id="9b4f3-133">Näiteks kui laenuartikli algusnumber on 10, sisestage väljale Vorming kaks numbri sümbolit.</span><span class="sxs-lookup"><span data-stu-id="9b4f3-133">For example, if the starting number for a loan item is 10, enter two number symbols symbols in the Format field.</span></span>  
14. <span data-ttu-id="9b4f3-134">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9b4f3-134">Click OK.</span></span>
15. <span data-ttu-id="9b4f3-135">Värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="9b4f3-135">Refresh the page.</span></span>

