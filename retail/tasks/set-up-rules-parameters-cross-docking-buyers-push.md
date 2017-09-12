--- 
title: " Reeglite ja parameetrite seadistamine ristlaadimise ja kesklaost jaotuse jaoks"
description: "See protseduur tutvustab täiendamisreeglite loomise etappe."
author: josaw1
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 1ff41a18be066b6f32c5172bda38c389e7f34128
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="set-up-rules-and-parameters-for-cross-docking-and-buyers-push"></a><span data-ttu-id="339dd-103"> Reeglite ja parameetrite seadistamine ristlaadimise ja kesklaost jaotuse jaoks</span><span class="sxs-lookup"><span data-stu-id="339dd-103">Set up rules and parameters for cross docking and buyer's push</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="339dd-104">See protseduur tutvustab täiendamisreeglite loomise etappe.</span><span class="sxs-lookup"><span data-stu-id="339dd-104">This procedure demonstrates the steps to create Replenishment rules.</span></span> <span data-ttu-id="339dd-105">Täiendamisreegleid saab kasutada, et juhtida seda, kuidas tooted ristlaadimise ja kesklaost jaotusega kauplustesse jaotatakse.</span><span class="sxs-lookup"><span data-stu-id="339dd-105">Replenishment rules can be used to control how products are distributed to stores when using Cross-docking and Buyer´s push.</span></span> <span data-ttu-id="339dd-106">Täiendamisreegleid saab määrata kauplustele või kauplusegruppidele.</span><span class="sxs-lookup"><span data-stu-id="339dd-106">Replenishment rules can be set up for stores or store groups.</span></span> <span data-ttu-id="339dd-107">Reegli igale reale määratud kaal määrab, kuidas toodete kogused kaupluste vahel jaotatakse, kui ristlaadimisel või kesklaost jaotamisel kasutatakse jaotamismeetodina täiendamisreegleid.</span><span class="sxs-lookup"><span data-stu-id="339dd-107">The weight defined for each line in a rule will control how the quantities of products will get distributed between the stores when using Replenishment rules as the distribution method in Cross-docking or Buyer´s push.</span></span> <span data-ttu-id="339dd-108">See protsess kasutab demoettevõtte USRT-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="339dd-108">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="339dd-109">Tehke valik Täiendamisreeglid.</span><span class="sxs-lookup"><span data-stu-id="339dd-109">Go to Replenishment rules.</span></span>
2. <span data-ttu-id="339dd-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="339dd-110">Click New.</span></span>
3. <span data-ttu-id="339dd-111">Sisestage väärtus väljale Täiendamisreegel.</span><span class="sxs-lookup"><span data-stu-id="339dd-111">In the Replenishment rule field, type a value.</span></span>
4. <span data-ttu-id="339dd-112">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="339dd-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="339dd-113">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="339dd-113">Click Save.</span></span>
6. <span data-ttu-id="339dd-114">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="339dd-114">Click Add.</span></span>
7. <span data-ttu-id="339dd-115">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="339dd-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="339dd-116">Saate selle tüübi jaoks valida Täiendamise hierarhia ja Kanali vahel.</span><span class="sxs-lookup"><span data-stu-id="339dd-116">You can choose Replenishment hierarchy or Channel for the type.</span></span> <span data-ttu-id="339dd-117">Väärtus juhib seda, kas Nime all tehtud valik on kanalite hierarhia või üks kindel kanal.</span><span class="sxs-lookup"><span data-stu-id="339dd-117">The value controls whether the selection in Name will be a hierarchy of channels or a specific channel.</span></span>  <span data-ttu-id="339dd-118">Selle näite puhul, jätke selle väärtuseks Täiendamise hierarhia.</span><span class="sxs-lookup"><span data-stu-id="339dd-118">For this example, leave it set as Replenishment hierarchy.</span></span>  
8. <span data-ttu-id="339dd-119">Valige väärtus väljal Nimi.</span><span class="sxs-lookup"><span data-stu-id="339dd-119">In the Name field, select a value.</span></span>
    * <span data-ttu-id="339dd-120">Kaalu vaikeväärtus tuletatakse laos täpsustatud kaalu põhjal.</span><span class="sxs-lookup"><span data-stu-id="339dd-120">The default weight value is populated from the weight defined on the warehouse.</span></span>  <span data-ttu-id="339dd-121">Seda kaalu saab kasutada täiendamisreegli määramiseks või võite soovi korral sisestada väljale Kaal uue kaalu.</span><span class="sxs-lookup"><span data-stu-id="339dd-121">This weight can be used for the Replenishment rule or you can enter a new weight in the Weight field.</span></span>  
9. <span data-ttu-id="339dd-122">Sisestage number väljale Kaal.</span><span class="sxs-lookup"><span data-stu-id="339dd-122">In the Weight field, enter a number.</span></span>
10. <span data-ttu-id="339dd-123">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="339dd-123">Click Add.</span></span>
11. <span data-ttu-id="339dd-124">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="339dd-124">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="339dd-125">Tehke väljal Tüüp valik Kanal.</span><span class="sxs-lookup"><span data-stu-id="339dd-125">In the Type field, select 'Channel'.</span></span>
13. <span data-ttu-id="339dd-126">Sisestage või valige väärtus väljal Nimi.</span><span class="sxs-lookup"><span data-stu-id="339dd-126">In the Name field, enter or select a value.</span></span>
14. <span data-ttu-id="339dd-127">Sisestage number väljale Kaal.</span><span class="sxs-lookup"><span data-stu-id="339dd-127">In the Weight field, enter a number.</span></span>
15. <span data-ttu-id="339dd-128">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="339dd-128">Click Save.</span></span>


