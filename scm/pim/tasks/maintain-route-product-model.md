--- 
title: Tootemudeli protsessi haldamine
description: "Selle protseduuri käitamine nõuab toote konfiguratsioonimudeli olemasolu."
author: BibiSp
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bibis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bibis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 55b22d246d6bfa9e8159fb844da95f61fcf07c62
ms.openlocfilehash: 3f6bacc54664c32a7d42f2befc51c420e29ada56
ms.contentlocale: et-ee
ms.lasthandoff: 07/28/2017

---
# <a name="maintain-a-route-for-a-product-model"></a><span data-ttu-id="4cc91-103">Tootemudeli protsessi haldamine</span><span class="sxs-lookup"><span data-stu-id="4cc91-103">Maintain a route for a product model</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4cc91-104">Selle protseduuri käitamine nõuab toote konfiguratsioonimudeli olemasolu.</span><span class="sxs-lookup"><span data-stu-id="4cc91-104">Running this procedure requires that a product configuration model exists.</span></span> <span data-ttu-id="4cc91-105">See protseduur kasutab tipptasemel kõlari mudelit demoettevõttes USMF, et juhatada teid läbi protsessi.</span><span class="sxs-lookup"><span data-stu-id="4cc91-105">This procedure uses the High end speaker model in the demo company USMF to walk you through the process.</span></span>


## <a name="add-a-route-operation"></a><span data-ttu-id="4cc91-106">Lisage protsessitoiming</span><span class="sxs-lookup"><span data-stu-id="4cc91-106">Add a route operation</span></span>
1. <span data-ttu-id="4cc91-107">Klõpsake valikut Tootevariandi mudeli määratlus.</span><span class="sxs-lookup"><span data-stu-id="4cc91-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="4cc91-108">Klõpsake valikut Toote konfiguratsioonimudelid.</span><span class="sxs-lookup"><span data-stu-id="4cc91-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="4cc91-109">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="4cc91-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4cc91-110">Valige selle harjutuse jaoks tipptasemel kõlari mudel.</span><span class="sxs-lookup"><span data-stu-id="4cc91-110">Select the High end speaker model for this exercise.</span></span>  
4. <span data-ttu-id="4cc91-111">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="4cc91-111">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="4cc91-112">Laiendage jaotist Protsessitoimingud.</span><span class="sxs-lookup"><span data-stu-id="4cc91-112">Expand the Route operations section.</span></span>
6. <span data-ttu-id="4cc91-113">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="4cc91-113">Click Add.</span></span>
7. <span data-ttu-id="4cc91-114">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="4cc91-114">In the Name field, type a value.</span></span>
8. <span data-ttu-id="4cc91-115">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="4cc91-115">In the Description field, type a value.</span></span>
9. <span data-ttu-id="4cc91-116">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="4cc91-116">Click Save.</span></span>

## <a name="enter-route-operation-details"></a><span data-ttu-id="4cc91-117">Sisestage protsessitoimingu üksikasjad</span><span class="sxs-lookup"><span data-stu-id="4cc91-117">Enter route operation details</span></span>
1. <span data-ttu-id="4cc91-118">Klõpsake valikut Protsessitoimingu üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="4cc91-118">Click Route operation details.</span></span>
2. <span data-ttu-id="4cc91-119">Sisestage või valige väärtus väljal Toiming.</span><span class="sxs-lookup"><span data-stu-id="4cc91-119">In the Operation field, enter or select a value.</span></span>
3. <span data-ttu-id="4cc91-120">Sisestage väljale Toimingu</span><span class="sxs-lookup"><span data-stu-id="4cc91-120">In the Oper.</span></span> <span data-ttu-id="4cc91-121">Nr</span><span class="sxs-lookup"><span data-stu-id="4cc91-121">No.</span></span> <span data-ttu-id="4cc91-122">number.</span><span class="sxs-lookup"><span data-stu-id="4cc91-122">field, enter a number.</span></span>
    * <span data-ttu-id="4cc91-123">Toimingunumbrid määravad protsessi järjekorra.</span><span class="sxs-lookup"><span data-stu-id="4cc91-123">Operation numbers determine the route sequence.</span></span>  
    * <span data-ttu-id="4cc91-124">Iga protsessitoimingu atribuut võib saada statistilise väärtuse või olla vastendatud atribuudiga.</span><span class="sxs-lookup"><span data-stu-id="4cc91-124">Each property on a route operation can get a static value or be mapped to an attribute.</span></span> <span data-ttu-id="4cc91-125">Atribuudiga vastendamisel määratakse väärtus konfiguratsiooni osaks.</span><span class="sxs-lookup"><span data-stu-id="4cc91-125">Mapping to an attribute will result in the value being set as part of the configuration.</span></span>  
4. <span data-ttu-id="4cc91-126">Sisestage või valige väärtus väljal Protsessigrupp.</span><span class="sxs-lookup"><span data-stu-id="4cc91-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="4cc91-127">Protsessigrupp määrab kuluarvutuse, tarbimise ja seadistuse põhikäitumise.</span><span class="sxs-lookup"><span data-stu-id="4cc91-127">The route group determines essential behavior for costing, consumption, and setup.</span></span>  
5. <span data-ttu-id="4cc91-128">Klõpsake vahekaarti Seadistus.</span><span class="sxs-lookup"><span data-stu-id="4cc91-128">Click the Setup tab.</span></span>
6. <span data-ttu-id="4cc91-129">Klõpsake vahekaarti Ajad.</span><span class="sxs-lookup"><span data-stu-id="4cc91-129">Click the Times tab.</span></span>
7. <span data-ttu-id="4cc91-130">Sisestage väljale Protsessikogus</span><span class="sxs-lookup"><span data-stu-id="4cc91-130">In the Process qty.</span></span> <span data-ttu-id="4cc91-131">number.</span><span class="sxs-lookup"><span data-stu-id="4cc91-131">field, enter a number.</span></span>
    * <span data-ttu-id="4cc91-132">Määrake, mitu ühe toimingu käigus töödeldakse.</span><span class="sxs-lookup"><span data-stu-id="4cc91-132">Determine how many will be processed during one operation.</span></span>  
8. <span data-ttu-id="4cc91-133">Sisestage number väljale Tunnid/aeg.</span><span class="sxs-lookup"><span data-stu-id="4cc91-133">In the Hours/time field, enter a number.</span></span>
    * <span data-ttu-id="4cc91-134">Sisestage aja suhe.</span><span class="sxs-lookup"><span data-stu-id="4cc91-134">Enter the time ratio.</span></span>  
9. <span data-ttu-id="4cc91-135">Märkige ruut Määra.</span><span class="sxs-lookup"><span data-stu-id="4cc91-135">Select the Set check box.</span></span>
10. <span data-ttu-id="4cc91-136">Sisestage number väljale Käitusaeg.</span><span class="sxs-lookup"><span data-stu-id="4cc91-136">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="4cc91-137">Määrake määratud koguse töötlemisaeg.</span><span class="sxs-lookup"><span data-stu-id="4cc91-137">Determine the processing time for the quantity that you have specified.</span></span>  
11. <span data-ttu-id="4cc91-138">Klõpsake vahekaarti Ressursinõuded.</span><span class="sxs-lookup"><span data-stu-id="4cc91-138">Click the Resource requirements tab.</span></span>
12. <span data-ttu-id="4cc91-139">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="4cc91-139">Click Add.</span></span>
13. <span data-ttu-id="4cc91-140">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="4cc91-140">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="4cc91-141">Valige suvand väljal Nõude tüüp.</span><span class="sxs-lookup"><span data-stu-id="4cc91-141">In the Requirement type field, select an option.</span></span>
    * <span data-ttu-id="4cc91-142">Otsustage, kas soovite määrata konkreetseid ressursse või võimalusi, mis neil peavad olema.</span><span class="sxs-lookup"><span data-stu-id="4cc91-142">Decide if you want to specify specific resources or capabilities that they must possess.</span></span>  
15. <span data-ttu-id="4cc91-143">Valige või sisestage väärtus väljal Nõue.</span><span class="sxs-lookup"><span data-stu-id="4cc91-143">In the Requirement field, enter or select a value.</span></span>
16. <span data-ttu-id="4cc91-144">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="4cc91-144">Click OK.</span></span>


