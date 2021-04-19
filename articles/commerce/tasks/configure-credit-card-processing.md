---
title: " Krediitkaardi töötlemise konfigureerimine"
description: See protseduur selgitab, kuidas vaadata makseteenuste pakkujate loendit ja konfigureerida müügireskontro maksekontot.
author: jashanno
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 13aa59ab1c6b0170ae9ab8972fb00bcf47e2b754
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5789752"
---
# <a name="configure-credit-card-processing"></a><span data-ttu-id="1b145-103"> Krediitkaardi töötlemise konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="1b145-103">Configure credit card processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1b145-104">See protseduur selgitab, kuidas vaadata makseteenuste pakkujate loendit ja konfigureerida müügireskontro maksekontot.</span><span class="sxs-lookup"><span data-stu-id="1b145-104">This procedure walks through how to view the list of payment providers and how to configure a payment account for accounts receivable.</span></span> <span data-ttu-id="1b145-105">See protseduur kasutab demoettevõtte USRT andmed ning on mõeldud administraatoritele ja IT-spetsialistidele.</span><span class="sxs-lookup"><span data-stu-id="1b145-105">This procedure uses the USRT company in demo data and is intended for Administrators and IT Professionals.</span></span>


## <a name="view-a-list-of-payment-providers"></a><span data-ttu-id="1b145-106">Makseteenuse pakkujate loendi kuvamine</span><span class="sxs-lookup"><span data-stu-id="1b145-106">View a list of payment providers</span></span>
1. <span data-ttu-id="1b145-107">Avage Müügireskontro > Maksete seadistus > Makseteenused.</span><span class="sxs-lookup"><span data-stu-id="1b145-107">Go to Accounts receivable > Payments setup > Payment services.</span></span>
2. <span data-ttu-id="1b145-108">Klõpsake suvandit Kuva saadaolevad pakkujad.</span><span class="sxs-lookup"><span data-stu-id="1b145-108">Click View available providers.</span></span>

## <a name="configure-payment-account"></a><span data-ttu-id="1b145-109">Maksekonto konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="1b145-109">Configure payment account</span></span>
1. <span data-ttu-id="1b145-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="1b145-110">Click New.</span></span>
2. <span data-ttu-id="1b145-111">Sisestage väärtus väljale Makseteenus.</span><span class="sxs-lookup"><span data-stu-id="1b145-111">In the Payment service field, type a value.</span></span>
3. <span data-ttu-id="1b145-112">Valige suvand väljal Makse ülekandmine.</span><span class="sxs-lookup"><span data-stu-id="1b145-112">In the Payment connector field, select an option.</span></span>
4. <span data-ttu-id="1b145-113">Laiendage jaotist Makseteenuse konto.</span><span class="sxs-lookup"><span data-stu-id="1b145-113">Toggle the expansion of the Payment service account section.</span></span>
5. <span data-ttu-id="1b145-114">Sisestage väljale Keskkond: väärtus PROD.</span><span class="sxs-lookup"><span data-stu-id="1b145-114">In the Environment: field, type 'PROD'.</span></span>
6. <span data-ttu-id="1b145-115">Klõpsake suvandit Krediitkaarditüübid.</span><span class="sxs-lookup"><span data-stu-id="1b145-115">Click Credit card types.</span></span>
7. <span data-ttu-id="1b145-116">Klõpsake väljal Maksete tööleht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="1b145-116">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="1b145-117">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="1b145-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="1b145-118">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="1b145-118">Click Add.</span></span>
10. <span data-ttu-id="1b145-119">Sisestage väärtus väljale Valuuta.</span><span class="sxs-lookup"><span data-stu-id="1b145-119">In the Currency field, type a value.</span></span>
11. <span data-ttu-id="1b145-120">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="1b145-120">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="1b145-121">Klõpsake väljal Maksete tööleht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="1b145-121">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="1b145-122">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="1b145-122">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="1b145-123">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="1b145-123">Click Add.</span></span>
15. <span data-ttu-id="1b145-124">Sisestage väärtus väljale Valuuta.</span><span class="sxs-lookup"><span data-stu-id="1b145-124">In the Currency field, type a value.</span></span>
16. <span data-ttu-id="1b145-125">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="1b145-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="1b145-126">Saate neid etappe korrata nii paljude kaarditüüpide puhul kui vaja.</span><span class="sxs-lookup"><span data-stu-id="1b145-126">You can repeat these steps for as many card types as you need.</span></span>  
17. <span data-ttu-id="1b145-127">Klõpsake väljal Maksete tööleht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="1b145-127">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="1b145-128">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="1b145-128">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="1b145-129">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="1b145-129">Click Add.</span></span>
20. <span data-ttu-id="1b145-130">Sisestage väärtus väljale Valuuta.</span><span class="sxs-lookup"><span data-stu-id="1b145-130">In the Currency field, type a value.</span></span>
21. <span data-ttu-id="1b145-131">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="1b145-131">Click Save.</span></span>
22. <span data-ttu-id="1b145-132">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="1b145-132">Close the page.</span></span>
23. <span data-ttu-id="1b145-133">Klõpsake suvandit Kinnita.</span><span class="sxs-lookup"><span data-stu-id="1b145-133">Click Validate.</span></span>
24. <span data-ttu-id="1b145-134">Märkige ruut Uute krediitkaartide vaiketöötleja.</span><span class="sxs-lookup"><span data-stu-id="1b145-134">Click the Default processor for new credit cards checkbox.</span></span>
25. <span data-ttu-id="1b145-135">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="1b145-135">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]