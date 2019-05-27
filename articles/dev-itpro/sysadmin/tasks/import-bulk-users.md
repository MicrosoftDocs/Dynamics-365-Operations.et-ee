---
title: Kasutajate hulgiimport
description: Süsteemiadministraatorid saavad seda toimingut kasutada suure hulga kasutajate importimiseks Azure Active Directoryst.
author: maertenm
manager: AnnBe
ms.date: 07/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 339cc1d3bcdc1dc93b796c385d2165f45f8f7ecf
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1548081"
---
# <a name="import-users-in-bulk"></a><span data-ttu-id="f62fc-103">Kasutajate hulgiimport</span><span class="sxs-lookup"><span data-stu-id="f62fc-103">Import users in bulk</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f62fc-104">Süsteemiadministraatorid saavad seda toimingut kasutada suure hulga kasutajate importimiseks Azure Active Directoryst.</span><span class="sxs-lookup"><span data-stu-id="f62fc-104">This procedure can be used by system administrators to import a large number of users from Azure Active Directory.</span></span>


## <a name="run-as-a-batch-job"></a><span data-ttu-id="f62fc-105">Käivita pakett-tööna</span><span class="sxs-lookup"><span data-stu-id="f62fc-105">Run as a batch job</span></span>
1. <span data-ttu-id="f62fc-106">Minge jaotisse Süsteemihaldus > Kasutajad > Kasutajad.</span><span class="sxs-lookup"><span data-stu-id="f62fc-106">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="f62fc-107">Klõpsake suvandit Partii import.</span><span class="sxs-lookup"><span data-stu-id="f62fc-107">Click Batch import.</span></span>
3. <span data-ttu-id="f62fc-108">Laiendage jaotist Käivita taustal.</span><span class="sxs-lookup"><span data-stu-id="f62fc-108">Expand the Run in the background section.</span></span>
4. <span data-ttu-id="f62fc-109">Valige suvand Jah väljal Pakktöötlus.</span><span class="sxs-lookup"><span data-stu-id="f62fc-109">Select Yes in the Batch processing field.</span></span>
5. <span data-ttu-id="f62fc-110">Tippige väärtus väljale Ülesande kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="f62fc-110">In the Task description field, type a value.</span></span>
6. <span data-ttu-id="f62fc-111">Sisestage või valige väärtus väljal Partiigrupp.</span><span class="sxs-lookup"><span data-stu-id="f62fc-111">In the Batch group field, enter or select a value.</span></span>
    * <span data-ttu-id="f62fc-112">See on valikuline etapp.</span><span class="sxs-lookup"><span data-stu-id="f62fc-112">This is an optional step.</span></span>  
7. <span data-ttu-id="f62fc-113">Valige väljal Privaatne väärtus Jah.</span><span class="sxs-lookup"><span data-stu-id="f62fc-113">Select Yes in the Private field.</span></span>
    * <span data-ttu-id="f62fc-114">See on valikuline etapp.</span><span class="sxs-lookup"><span data-stu-id="f62fc-114">This is an optional step.</span></span>  
8. <span data-ttu-id="f62fc-115">Valige väljal Kriitiline töö väärtus Jah.</span><span class="sxs-lookup"><span data-stu-id="f62fc-115">Select Yes in the Critical Job field.</span></span>
    * <span data-ttu-id="f62fc-116">See on valikuline etapp.</span><span class="sxs-lookup"><span data-stu-id="f62fc-116">This is an optional step.</span></span>  
9. <span data-ttu-id="f62fc-117">Valige väljal Jälgimiskategooria soovitud suvand.</span><span class="sxs-lookup"><span data-stu-id="f62fc-117">In the Monitoring category field, select an option.</span></span>
10. <span data-ttu-id="f62fc-118">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f62fc-118">Click OK.</span></span>

## <a name="run-in-a-sandbox-environment"></a><span data-ttu-id="f62fc-119">Liivakastikeskkonna käitamine</span><span class="sxs-lookup"><span data-stu-id="f62fc-119">Run in a sandbox environment</span></span>
1. <span data-ttu-id="f62fc-120">Klõpsake suvandit Partii import.</span><span class="sxs-lookup"><span data-stu-id="f62fc-120">Click Batch import.</span></span>
2. <span data-ttu-id="f62fc-121">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f62fc-121">Click OK.</span></span>

