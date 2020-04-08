---
title: " Krediitkaardi töötlemise konfigureerimine"
description: See protseduur selgitab, kuidas vaadata makseteenuste pakkujate loendit ja konfigureerida müügireskontro maksekontot.
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2cfec44bc1c767dff1109c4ecd4e2862443fb1d0
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141495"
---
# <a name="configure-credit-card-processing"></a><span data-ttu-id="1086a-103"> Krediitkaardi töötlemise konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="1086a-103">Configure credit card processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1086a-104">See protseduur selgitab, kuidas vaadata makseteenuste pakkujate loendit ja konfigureerida müügireskontro maksekontot.</span><span class="sxs-lookup"><span data-stu-id="1086a-104">This procedure walks through how to view the list of payment providers and how to configure a payment account for accounts receivable.</span></span> <span data-ttu-id="1086a-105">See protseduur kasutab demoettevõtte USRT andmed ning on mõeldud administraatoritele ja IT-spetsialistidele.</span><span class="sxs-lookup"><span data-stu-id="1086a-105">This procedure uses the USRT company in demo data and is intended for Administrators and IT Professionals.</span></span>


## <a name="view-a-list-of-payment-providers"></a><span data-ttu-id="1086a-106">Makseteenuse pakkujate loendi kuvamine</span><span class="sxs-lookup"><span data-stu-id="1086a-106">View a list of payment providers</span></span>
1. <span data-ttu-id="1086a-107">Avage Müügireskontro > Maksete seadistus > Makseteenused.</span><span class="sxs-lookup"><span data-stu-id="1086a-107">Go to Accounts receivable > Payments setup > Payment services.</span></span>
2. <span data-ttu-id="1086a-108">Klõpsake suvandit Kuva saadaolevad pakkujad.</span><span class="sxs-lookup"><span data-stu-id="1086a-108">Click View available providers.</span></span>

## <a name="configure-payment-account"></a><span data-ttu-id="1086a-109">Maksekonto konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="1086a-109">Configure payment account</span></span>
1. <span data-ttu-id="1086a-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="1086a-110">Click New.</span></span>
2. <span data-ttu-id="1086a-111">Sisestage väärtus väljale Makseteenus.</span><span class="sxs-lookup"><span data-stu-id="1086a-111">In the Payment service field, type a value.</span></span>
3. <span data-ttu-id="1086a-112">Valige suvand väljal Makse ülekandmine.</span><span class="sxs-lookup"><span data-stu-id="1086a-112">In the Payment connector field, select an option.</span></span>
4. <span data-ttu-id="1086a-113">Laiendage jaotist Makseteenuse konto.</span><span class="sxs-lookup"><span data-stu-id="1086a-113">Toggle the expansion of the Payment service account section.</span></span>
5. <span data-ttu-id="1086a-114">Sisestage väljale Keskkond: väärtus PROD.</span><span class="sxs-lookup"><span data-stu-id="1086a-114">In the Environment: field, type 'PROD'.</span></span>
6. <span data-ttu-id="1086a-115">Klõpsake suvandit Krediitkaarditüübid.</span><span class="sxs-lookup"><span data-stu-id="1086a-115">Click Credit card types.</span></span>
7. <span data-ttu-id="1086a-116">Klõpsake väljal Maksete tööleht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="1086a-116">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="1086a-117">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="1086a-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="1086a-118">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="1086a-118">Click Add.</span></span>
10. <span data-ttu-id="1086a-119">Sisestage väärtus väljale Valuuta.</span><span class="sxs-lookup"><span data-stu-id="1086a-119">In the Currency field, type a value.</span></span>
11. <span data-ttu-id="1086a-120">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="1086a-120">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="1086a-121">Klõpsake väljal Maksete tööleht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="1086a-121">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="1086a-122">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="1086a-122">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="1086a-123">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="1086a-123">Click Add.</span></span>
15. <span data-ttu-id="1086a-124">Sisestage väärtus väljale Valuuta.</span><span class="sxs-lookup"><span data-stu-id="1086a-124">In the Currency field, type a value.</span></span>
16. <span data-ttu-id="1086a-125">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="1086a-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1086a-126">Saate neid etappe korrata nii paljude kaarditüüpide puhul kui vaja.</span><span class="sxs-lookup"><span data-stu-id="1086a-126">You can repeat these steps for as many card types as you need.</span></span>  
17. <span data-ttu-id="1086a-127">Klõpsake väljal Maksete tööleht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="1086a-127">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="1086a-128">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="1086a-128">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="1086a-129">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="1086a-129">Click Add.</span></span>
20. <span data-ttu-id="1086a-130">Sisestage väärtus väljale Valuuta.</span><span class="sxs-lookup"><span data-stu-id="1086a-130">In the Currency field, type a value.</span></span>
21. <span data-ttu-id="1086a-131">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="1086a-131">Click Save.</span></span>
22. <span data-ttu-id="1086a-132">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="1086a-132">Close the page.</span></span>
23. <span data-ttu-id="1086a-133">Klõpsake suvandit Kinnita.</span><span class="sxs-lookup"><span data-stu-id="1086a-133">Click Validate.</span></span>
24. <span data-ttu-id="1086a-134">Märkige ruut Uute krediitkaartide vaiketöötleja.</span><span class="sxs-lookup"><span data-stu-id="1086a-134">Click the Default processor for new credit cards checkbox.</span></span>
25. <span data-ttu-id="1086a-135">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="1086a-135">Click Save.</span></span>

