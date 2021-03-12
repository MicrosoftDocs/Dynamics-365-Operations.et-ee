---
title: " Reeglite ja parameetrite seadistamine ristlaadimise ja kesklaost jaotuse jaoks"
description: See protseduur tutvustab täiendamisreeglite loomise etappe.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailReplenishmentRuleTable, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bc5404e5eb1679659604a6268fa09519a7a4282e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5003714"
---
# <a name="set-up-rules-and-parameters-for-cross-docking-and-buyers-push"></a><span data-ttu-id="28250-103"> Reeglite ja parameetrite seadistamine ristlaadimise ja kesklaost jaotuse jaoks</span><span class="sxs-lookup"><span data-stu-id="28250-103">Set up rules and parameters for cross docking and buyer's push</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="28250-104">See protseduur tutvustab täiendamisreeglite loomise etappe.</span><span class="sxs-lookup"><span data-stu-id="28250-104">This procedure demonstrates the steps to create Replenishment rules.</span></span> <span data-ttu-id="28250-105">Täiendamisreegleid saab kasutada, et juhtida seda, kuidas tooted ristlaadimise ja kesklaost jaotusega kauplustesse jaotatakse.</span><span class="sxs-lookup"><span data-stu-id="28250-105">Replenishment rules can be used to control how products are distributed to stores when using Cross-docking and Buyer´s push.</span></span> <span data-ttu-id="28250-106">Täiendamisreegleid saab määrata kauplustele või kauplusegruppidele.</span><span class="sxs-lookup"><span data-stu-id="28250-106">Replenishment rules can be set up for stores or store groups.</span></span> <span data-ttu-id="28250-107">Reegli igale reale määratud kaal määrab, kuidas toodete kogused kaupluste vahel jaotatakse, kui ristlaadimisel või kesklaost jaotamisel kasutatakse jaotamismeetodina täiendamisreegleid.</span><span class="sxs-lookup"><span data-stu-id="28250-107">The weight defined for each line in a rule will control how the quantities of products will get distributed between the stores when using Replenishment rules as the distribution method in Cross-docking or Buyer´s push.</span></span> <span data-ttu-id="28250-108">See protsess kasutab demoettevõtte USRT-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="28250-108">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="28250-109">Tehke valik Täiendamisreeglid.</span><span class="sxs-lookup"><span data-stu-id="28250-109">Go to Replenishment rules.</span></span>
2. <span data-ttu-id="28250-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="28250-110">Click New.</span></span>
3. <span data-ttu-id="28250-111">Sisestage väärtus väljale Täiendamisreegel.</span><span class="sxs-lookup"><span data-stu-id="28250-111">In the Replenishment rule field, type a value.</span></span>
4. <span data-ttu-id="28250-112">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="28250-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="28250-113">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="28250-113">Click Save.</span></span>
6. <span data-ttu-id="28250-114">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="28250-114">Click Add.</span></span>
7. <span data-ttu-id="28250-115">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="28250-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="28250-116">Saate selle tüübi jaoks valida Täiendamise hierarhia ja Kanali vahel.</span><span class="sxs-lookup"><span data-stu-id="28250-116">You can choose Replenishment hierarchy or Channel for the type.</span></span> <span data-ttu-id="28250-117">Väärtus juhib seda, kas Nime all tehtud valik on kanalite hierarhia või üks kindel kanal.</span><span class="sxs-lookup"><span data-stu-id="28250-117">The value controls whether the selection in Name will be a hierarchy of channels or a specific channel.</span></span>  <span data-ttu-id="28250-118">Selle näite puhul, jätke selle väärtuseks Täiendamise hierarhia.</span><span class="sxs-lookup"><span data-stu-id="28250-118">For this example, leave it set as Replenishment hierarchy.</span></span>  
8. <span data-ttu-id="28250-119">Valige väärtus väljal Nimi.</span><span class="sxs-lookup"><span data-stu-id="28250-119">In the Name field, select a value.</span></span>
    * <span data-ttu-id="28250-120">Kaalu vaikeväärtus tuletatakse laos täpsustatud kaalu põhjal.</span><span class="sxs-lookup"><span data-stu-id="28250-120">The default weight value is populated from the weight defined on the warehouse.</span></span>  <span data-ttu-id="28250-121">Seda kaalu saab kasutada täiendamisreegli määramiseks või võite soovi korral sisestada väljale Kaal uue kaalu.</span><span class="sxs-lookup"><span data-stu-id="28250-121">This weight can be used for the Replenishment rule or you can enter a new weight in the Weight field.</span></span>  
9. <span data-ttu-id="28250-122">Sisestage number väljale Kaal.</span><span class="sxs-lookup"><span data-stu-id="28250-122">In the Weight field, enter a number.</span></span>
10. <span data-ttu-id="28250-123">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="28250-123">Click Add.</span></span>
11. <span data-ttu-id="28250-124">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="28250-124">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="28250-125">Tehke väljal Tüüp valik Kanal.</span><span class="sxs-lookup"><span data-stu-id="28250-125">In the Type field, select 'Channel'.</span></span>
13. <span data-ttu-id="28250-126">Sisestage või valige väärtus väljal Nimi.</span><span class="sxs-lookup"><span data-stu-id="28250-126">In the Name field, enter or select a value.</span></span>
14. <span data-ttu-id="28250-127">Sisestage number väljale Kaal.</span><span class="sxs-lookup"><span data-stu-id="28250-127">In the Weight field, enter a number.</span></span>
15. <span data-ttu-id="28250-128">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="28250-128">Click Save.</span></span>

