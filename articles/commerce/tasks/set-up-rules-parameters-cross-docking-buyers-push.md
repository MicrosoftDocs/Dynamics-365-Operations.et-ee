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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9bccd92946783628dce37c3fd018e4dd927efd49
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141127"
---
# <a name="set-up-rules-and-parameters-for-cross-docking-and-buyers-push"></a><span data-ttu-id="04d41-103"> Reeglite ja parameetrite seadistamine ristlaadimise ja kesklaost jaotuse jaoks</span><span class="sxs-lookup"><span data-stu-id="04d41-103">Set up rules and parameters for cross docking and buyer's push</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="04d41-104">See protseduur tutvustab täiendamisreeglite loomise etappe.</span><span class="sxs-lookup"><span data-stu-id="04d41-104">This procedure demonstrates the steps to create Replenishment rules.</span></span> <span data-ttu-id="04d41-105">Täiendamisreegleid saab kasutada, et juhtida seda, kuidas tooted ristlaadimise ja kesklaost jaotusega kauplustesse jaotatakse.</span><span class="sxs-lookup"><span data-stu-id="04d41-105">Replenishment rules can be used to control how products are distributed to stores when using Cross-docking and Buyer´s push.</span></span> <span data-ttu-id="04d41-106">Täiendamisreegleid saab määrata kauplustele või kauplusegruppidele.</span><span class="sxs-lookup"><span data-stu-id="04d41-106">Replenishment rules can be set up for stores or store groups.</span></span> <span data-ttu-id="04d41-107">Reegli igale reale määratud kaal määrab, kuidas toodete kogused kaupluste vahel jaotatakse, kui ristlaadimisel või kesklaost jaotamisel kasutatakse jaotamismeetodina täiendamisreegleid.</span><span class="sxs-lookup"><span data-stu-id="04d41-107">The weight defined for each line in a rule will control how the quantities of products will get distributed between the stores when using Replenishment rules as the distribution method in Cross-docking or Buyer´s push.</span></span> <span data-ttu-id="04d41-108">See protsess kasutab demoettevõtte USRT-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="04d41-108">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="04d41-109">Tehke valik Täiendamisreeglid.</span><span class="sxs-lookup"><span data-stu-id="04d41-109">Go to Replenishment rules.</span></span>
2. <span data-ttu-id="04d41-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="04d41-110">Click New.</span></span>
3. <span data-ttu-id="04d41-111">Sisestage väärtus väljale Täiendamisreegel.</span><span class="sxs-lookup"><span data-stu-id="04d41-111">In the Replenishment rule field, type a value.</span></span>
4. <span data-ttu-id="04d41-112">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="04d41-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="04d41-113">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="04d41-113">Click Save.</span></span>
6. <span data-ttu-id="04d41-114">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="04d41-114">Click Add.</span></span>
7. <span data-ttu-id="04d41-115">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="04d41-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="04d41-116">Saate selle tüübi jaoks valida Täiendamise hierarhia ja Kanali vahel.</span><span class="sxs-lookup"><span data-stu-id="04d41-116">You can choose Replenishment hierarchy or Channel for the type.</span></span> <span data-ttu-id="04d41-117">Väärtus juhib seda, kas Nime all tehtud valik on kanalite hierarhia või üks kindel kanal.</span><span class="sxs-lookup"><span data-stu-id="04d41-117">The value controls whether the selection in Name will be a hierarchy of channels or a specific channel.</span></span>  <span data-ttu-id="04d41-118">Selle näite puhul, jätke selle väärtuseks Täiendamise hierarhia.</span><span class="sxs-lookup"><span data-stu-id="04d41-118">For this example, leave it set as Replenishment hierarchy.</span></span>  
8. <span data-ttu-id="04d41-119">Valige väärtus väljal Nimi.</span><span class="sxs-lookup"><span data-stu-id="04d41-119">In the Name field, select a value.</span></span>
    * <span data-ttu-id="04d41-120">Kaalu vaikeväärtus tuletatakse laos täpsustatud kaalu põhjal.</span><span class="sxs-lookup"><span data-stu-id="04d41-120">The default weight value is populated from the weight defined on the warehouse.</span></span>  <span data-ttu-id="04d41-121">Seda kaalu saab kasutada täiendamisreegli määramiseks või võite soovi korral sisestada väljale Kaal uue kaalu.</span><span class="sxs-lookup"><span data-stu-id="04d41-121">This weight can be used for the Replenishment rule or you can enter a new weight in the Weight field.</span></span>  
9. <span data-ttu-id="04d41-122">Sisestage number väljale Kaal.</span><span class="sxs-lookup"><span data-stu-id="04d41-122">In the Weight field, enter a number.</span></span>
10. <span data-ttu-id="04d41-123">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="04d41-123">Click Add.</span></span>
11. <span data-ttu-id="04d41-124">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="04d41-124">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="04d41-125">Tehke väljal Tüüp valik Kanal.</span><span class="sxs-lookup"><span data-stu-id="04d41-125">In the Type field, select 'Channel'.</span></span>
13. <span data-ttu-id="04d41-126">Sisestage või valige väärtus väljal Nimi.</span><span class="sxs-lookup"><span data-stu-id="04d41-126">In the Name field, enter or select a value.</span></span>
14. <span data-ttu-id="04d41-127">Sisestage number väljale Kaal.</span><span class="sxs-lookup"><span data-stu-id="04d41-127">In the Weight field, enter a number.</span></span>
15. <span data-ttu-id="04d41-128">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="04d41-128">Click Save.</span></span>

