--- 
title: " Masinõppele tuginevate tootesoovituste konfigureerimine"
description: "See protseduur värskendab andmeid üksuse kaupluses, mida tootesoovituste aluseks olev masinõppesüsteem kasutab, ja aktiveerib siis tootesoovitused kassa klientidel."
author: ashishmsft
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e32c7cf1283487cb7a52f7d8e261b6b587b76364
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="configure-machine-learning-powered-product-recommendations"></a><span data-ttu-id="be5c5-103"> Masinõppele tuginevate tootesoovituste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="be5c5-103">Configure machine learning-powered product recommendations</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="be5c5-104">See protseduur värskendab andmeid üksuse kaupluses, mida tootesoovituste aluseks olev masinõppesüsteem kasutab, ja aktiveerib siis tootesoovitused kassa klientidel.</span><span class="sxs-lookup"><span data-stu-id="be5c5-104">This procedure refreshes the data in the Entity store that is used by the machine learning system that powers product recommendations, and then enables product recommendations on POS clients.</span></span> <span data-ttu-id="be5c5-105">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="be5c5-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="be5c5-106">Minge jaotisse Süsteemihaldus > Häälestamine > Üksuse kauplus.</span><span class="sxs-lookup"><span data-stu-id="be5c5-106">Go to System administration > Setup > Entity Store.</span></span>
2. <span data-ttu-id="be5c5-107">Otsige loendist üles ja valige kirje RetailSales.</span><span class="sxs-lookup"><span data-stu-id="be5c5-107">In the list, find and select the record 'RetailSales'.</span></span>
3. <span data-ttu-id="be5c5-108">Klõpsake käsku Värskenda.</span><span class="sxs-lookup"><span data-stu-id="be5c5-108">Click Refresh.</span></span>
4. <span data-ttu-id="be5c5-109">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="be5c5-109">Click OK.</span></span>
5. <span data-ttu-id="be5c5-110">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="be5c5-110">Close the page.</span></span>
6. <span data-ttu-id="be5c5-111">Minge jaotisse Jaemüük ja kaubandus > Peakontori seadistamine > Parameetrid > Jaemüügi parameetrid.</span><span class="sxs-lookup"><span data-stu-id="be5c5-111">Go to Retail and commerce > Headquarters setup > Parameters > Retail parameters.</span></span>
7. <span data-ttu-id="be5c5-112">Klõpsake vahekaarti Masinõpe.</span><span class="sxs-lookup"><span data-stu-id="be5c5-112">Click the Machine learning tab.</span></span>
8. <span data-ttu-id="be5c5-113">Tehke väljal Luba tootesoovitused valik Jah.</span><span class="sxs-lookup"><span data-stu-id="be5c5-113">Select 'Yes' in the Enable product recommendations field.</span></span>
    * <span data-ttu-id="be5c5-114">Kui saate sõnumi „Soovitatud mudeleid ei saanud tuua”, on see sellepärast, et värskendasite väga hiljuti üksuse kauplust ja süsteem pole võib-olla uute andmete vastuvõtmist lõpetanud.</span><span class="sxs-lookup"><span data-stu-id="be5c5-114">If you receive the message "The recommendation models couldn't be retrieved", it’s because you refreshed the Entity Store very recently and the system may not have finished assimilating the new data.</span></span> <span data-ttu-id="be5c5-115">Oodake 2-3 tundi ning proovige uuesti.</span><span class="sxs-lookup"><span data-stu-id="be5c5-115">Wait 2-3 hours and try again.</span></span>  
9. <span data-ttu-id="be5c5-116">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="be5c5-116">Click Save.</span></span>
10. <span data-ttu-id="be5c5-117">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="be5c5-117">Close the page.</span></span>


