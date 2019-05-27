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
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1507885"
---
# <a name="create-loan-items"></a><span data-ttu-id="3fc15-103">Loo laenuartikleid</span><span class="sxs-lookup"><span data-stu-id="3fc15-103">Create loan items</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3fc15-104">Laenuartiklid on kirjed, mis aitavad teil jälgida füüsilisi kaupu, näiteks telefone või arvuteid, mida teie ettevõte töötajatele laenab.</span><span class="sxs-lookup"><span data-stu-id="3fc15-104">Loan items are records that help you track physical items, such as phones or computers, that your company lends to workers.</span></span> <span data-ttu-id="3fc15-105">Iga füüsiline kaup peab laenuartiklile vastama.</span><span class="sxs-lookup"><span data-stu-id="3fc15-105">Each physical item must have a corresponding loan item.</span></span> <span data-ttu-id="3fc15-106">Iga laenuartikli kirjel tuleb kirjeldada, mida laenatakse, kes on laenu eest vastutav ja mitmeks päevaks võib artiklit laenata.</span><span class="sxs-lookup"><span data-stu-id="3fc15-106">Each loan item record should describe what is being loaned, who is responsible for the loan, and the number of days the item can be on loan.</span></span> <span data-ttu-id="3fc15-107">Saate luua mitu laenuartiklit, nagu võtmed, pääsukaardid või vormirõivad, samal ajal.</span><span class="sxs-lookup"><span data-stu-id="3fc15-107">You can create multiple loan items, such as keys, access cards, or uniforms, at the same time.</span></span> <span data-ttu-id="3fc15-108">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="3fc15-108">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-loan-types"></a><span data-ttu-id="3fc15-109">Laenutüüpide loomine</span><span class="sxs-lookup"><span data-stu-id="3fc15-109">Create Loan types</span></span>
1. <span data-ttu-id="3fc15-110">Avage Inimressursid > Töötajad > Laenuartiklid > Laenutüübid.</span><span class="sxs-lookup"><span data-stu-id="3fc15-110">Go to Human resources > Workers > Loan items > Loan types.</span></span>
2. <span data-ttu-id="3fc15-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="3fc15-111">Click New.</span></span>
3. <span data-ttu-id="3fc15-112">Sisestage väärtus väljale Laenu tüüp.</span><span class="sxs-lookup"><span data-stu-id="3fc15-112">In the Loan type field, type a value.</span></span>
4. <span data-ttu-id="3fc15-113">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="3fc15-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="3fc15-114">Sisestage päevade arv, mille võrra võib seda tüüpi laenuartiklite tagastamine tähtaja ületada.</span><span class="sxs-lookup"><span data-stu-id="3fc15-114">Enter the number of days that items assigned to this loan type can be overdue.</span></span> 
6. <span data-ttu-id="3fc15-115">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="3fc15-115">Click Save.</span></span>
7. <span data-ttu-id="3fc15-116">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="3fc15-116">Close the page.</span></span>
8. <span data-ttu-id="3fc15-117">Värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="3fc15-117">Refresh the page.</span></span>

## <a name="create-loan-items"></a><span data-ttu-id="3fc15-118">Laenuartiklite loomine</span><span class="sxs-lookup"><span data-stu-id="3fc15-118">Create Loan items</span></span>
1. <span data-ttu-id="3fc15-119">Avage Inimressursid > Töötajad > Laenuartiklid > Laenuartiklid.</span><span class="sxs-lookup"><span data-stu-id="3fc15-119">Go to Human resources > Workers > Loan items > Loan items.</span></span>
2. <span data-ttu-id="3fc15-120">Klõpsake suvandit Loo laenuartikleid.</span><span class="sxs-lookup"><span data-stu-id="3fc15-120">Click Create loan items.</span></span>
3. <span data-ttu-id="3fc15-121">Väljale Kogus väljale Protsessi kogus.</span><span class="sxs-lookup"><span data-stu-id="3fc15-121">In the Qty. field, enter a number.</span></span>
4. <span data-ttu-id="3fc15-122">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="3fc15-122">In the Description field, type a value.</span></span>
5. <span data-ttu-id="3fc15-123">Klõpsake väljal Laenu tüüp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="3fc15-123">In the Loan type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="3fc15-124">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="3fc15-124">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="3fc15-125">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="3fc15-125">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="3fc15-126">Sisestage päevade arv, mille jooksul artikkel võib olla välja laenatud.</span><span class="sxs-lookup"><span data-stu-id="3fc15-126">Enter the number of days the item can be on loan.</span></span>
    * <span data-ttu-id="3fc15-127">Lehe Laenatud seadmed välja Plaanitud tagastus vaikeväärtus arvutatakse, liites tänasele kuupäevale selle numbri.</span><span class="sxs-lookup"><span data-stu-id="3fc15-127">The default value for the Planned return field on the Loaned equipment page is calculated as the current date plus this number.</span></span>  
9. <span data-ttu-id="3fc15-128">Klõpsake väljal Vastutav isik otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="3fc15-128">In the Person in charge field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="3fc15-129">Klõpsake Vali.</span><span class="sxs-lookup"><span data-stu-id="3fc15-129">Click Select.</span></span>
11. <span data-ttu-id="3fc15-130">Sisestage number väljale Algväärtus.</span><span class="sxs-lookup"><span data-stu-id="3fc15-130">In the Starting value field, enter a number.</span></span>
12. <span data-ttu-id="3fc15-131">Sisestage number väljale Intervall.</span><span class="sxs-lookup"><span data-stu-id="3fc15-131">In the Interval field, enter a number.</span></span>
13. <span data-ttu-id="3fc15-132">Sisestage väärtus väljale Vorming.</span><span class="sxs-lookup"><span data-stu-id="3fc15-132">In the Format field, type a value.</span></span>
    * <span data-ttu-id="3fc15-133">Näiteks kui laenuartikli algusnumber on 10, sisestage väljale Vorming kaks numbri sümbolit.</span><span class="sxs-lookup"><span data-stu-id="3fc15-133">For example, if the starting number for a loan item is 10, enter two number symbols symbols in the Format field.</span></span>  
14. <span data-ttu-id="3fc15-134">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="3fc15-134">Click OK.</span></span>
15. <span data-ttu-id="3fc15-135">Värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="3fc15-135">Refresh the page.</span></span>

