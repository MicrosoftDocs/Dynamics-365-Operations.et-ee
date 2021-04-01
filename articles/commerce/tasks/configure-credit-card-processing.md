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
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d365dfce8e8fbd332111d96eeb2a431151d7a342
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5234217"
---
# <a name="configure-credit-card-processing"></a><span data-ttu-id="9caba-103"> Krediitkaardi töötlemise konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="9caba-103">Configure credit card processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9caba-104">See protseduur selgitab, kuidas vaadata makseteenuste pakkujate loendit ja konfigureerida müügireskontro maksekontot.</span><span class="sxs-lookup"><span data-stu-id="9caba-104">This procedure walks through how to view the list of payment providers and how to configure a payment account for accounts receivable.</span></span> <span data-ttu-id="9caba-105">See protseduur kasutab demoettevõtte USRT andmed ning on mõeldud administraatoritele ja IT-spetsialistidele.</span><span class="sxs-lookup"><span data-stu-id="9caba-105">This procedure uses the USRT company in demo data and is intended for Administrators and IT Professionals.</span></span>


## <a name="view-a-list-of-payment-providers"></a><span data-ttu-id="9caba-106">Makseteenuse pakkujate loendi kuvamine</span><span class="sxs-lookup"><span data-stu-id="9caba-106">View a list of payment providers</span></span>
1. <span data-ttu-id="9caba-107">Avage Müügireskontro > Maksete seadistus > Makseteenused.</span><span class="sxs-lookup"><span data-stu-id="9caba-107">Go to Accounts receivable > Payments setup > Payment services.</span></span>
2. <span data-ttu-id="9caba-108">Klõpsake suvandit Kuva saadaolevad pakkujad.</span><span class="sxs-lookup"><span data-stu-id="9caba-108">Click View available providers.</span></span>

## <a name="configure-payment-account"></a><span data-ttu-id="9caba-109">Maksekonto konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="9caba-109">Configure payment account</span></span>
1. <span data-ttu-id="9caba-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="9caba-110">Click New.</span></span>
2. <span data-ttu-id="9caba-111">Sisestage väärtus väljale Makseteenus.</span><span class="sxs-lookup"><span data-stu-id="9caba-111">In the Payment service field, type a value.</span></span>
3. <span data-ttu-id="9caba-112">Valige suvand väljal Makse ülekandmine.</span><span class="sxs-lookup"><span data-stu-id="9caba-112">In the Payment connector field, select an option.</span></span>
4. <span data-ttu-id="9caba-113">Laiendage jaotist Makseteenuse konto.</span><span class="sxs-lookup"><span data-stu-id="9caba-113">Toggle the expansion of the Payment service account section.</span></span>
5. <span data-ttu-id="9caba-114">Sisestage väljale Keskkond: väärtus PROD.</span><span class="sxs-lookup"><span data-stu-id="9caba-114">In the Environment: field, type 'PROD'.</span></span>
6. <span data-ttu-id="9caba-115">Klõpsake suvandit Krediitkaarditüübid.</span><span class="sxs-lookup"><span data-stu-id="9caba-115">Click Credit card types.</span></span>
7. <span data-ttu-id="9caba-116">Klõpsake väljal Maksete tööleht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="9caba-116">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="9caba-117">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="9caba-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="9caba-118">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="9caba-118">Click Add.</span></span>
10. <span data-ttu-id="9caba-119">Sisestage väärtus väljale Valuuta.</span><span class="sxs-lookup"><span data-stu-id="9caba-119">In the Currency field, type a value.</span></span>
11. <span data-ttu-id="9caba-120">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="9caba-120">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="9caba-121">Klõpsake väljal Maksete tööleht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="9caba-121">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="9caba-122">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="9caba-122">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="9caba-123">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="9caba-123">Click Add.</span></span>
15. <span data-ttu-id="9caba-124">Sisestage väärtus väljale Valuuta.</span><span class="sxs-lookup"><span data-stu-id="9caba-124">In the Currency field, type a value.</span></span>
16. <span data-ttu-id="9caba-125">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="9caba-125">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9caba-126">Saate neid etappe korrata nii paljude kaarditüüpide puhul kui vaja.</span><span class="sxs-lookup"><span data-stu-id="9caba-126">You can repeat these steps for as many card types as you need.</span></span>  
17. <span data-ttu-id="9caba-127">Klõpsake väljal Maksete tööleht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="9caba-127">In the Payment journal field, click the drop-down button to open the lookup.</span></span>
18. <span data-ttu-id="9caba-128">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="9caba-128">In the list, click the link in the selected row.</span></span>
19. <span data-ttu-id="9caba-129">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="9caba-129">Click Add.</span></span>
20. <span data-ttu-id="9caba-130">Sisestage väärtus väljale Valuuta.</span><span class="sxs-lookup"><span data-stu-id="9caba-130">In the Currency field, type a value.</span></span>
21. <span data-ttu-id="9caba-131">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="9caba-131">Click Save.</span></span>
22. <span data-ttu-id="9caba-132">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9caba-132">Close the page.</span></span>
23. <span data-ttu-id="9caba-133">Klõpsake suvandit Kinnita.</span><span class="sxs-lookup"><span data-stu-id="9caba-133">Click Validate.</span></span>
24. <span data-ttu-id="9caba-134">Märkige ruut Uute krediitkaartide vaiketöötleja.</span><span class="sxs-lookup"><span data-stu-id="9caba-134">Click the Default processor for new credit cards checkbox.</span></span>
25. <span data-ttu-id="9caba-135">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="9caba-135">Click Save.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]