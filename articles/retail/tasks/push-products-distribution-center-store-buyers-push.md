--- 
title: " Toodete jaotamine jaotuskeskusest kauplusse kesklaost jaotuse abil"
description: "See protseduur tutvustab, kuidas luua ja töödelda jaotust kesklaost toodete laialisaatmiseks ühest kohast ühte või mitmesse kauplusesse."
author: rubencdelgado
manager: AnnBe
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: f827cae291644bea0e6a1af8af9f692b118534ad
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---
# <a name="push-products-from-distribution-center-to-store-using-buyers-push"></a><span data-ttu-id="c511e-103"> Toodete jaotamine jaotuskeskusest kauplusse kesklaost jaotuse abil</span><span class="sxs-lookup"><span data-stu-id="c511e-103">Push products from distribution center to store using buyer's push</span></span>

[!INCLUDE [task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="c511e-104">See protseduur tutvustab, kuidas luua ja töödelda jaotust kesklaost toodete laialisaatmiseks ühest kohast ühte või mitmesse kauplusesse.</span><span class="sxs-lookup"><span data-stu-id="c511e-104">This procedure walks through the steps to create and process a Buyer´s push to distribute products from one location to one or many stores.</span></span> <span data-ttu-id="c511e-105">Kasutaja saab määrata mitu konfiguratsiooni ja lasta süsteemil soovitada, kuidas tooted laiali saata, või käsitsi sisestada, kuhu tooted saadetakse ja kui suure koguse iga kauplus saab.</span><span class="sxs-lookup"><span data-stu-id="c511e-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="c511e-106">See protseduur ei sisalda andmete seadistust, mida kesklaost jaotamisel kasutada nagu täiendamise reeglid, organisatsioonihierarhiad ja kaupluse kaalud.</span><span class="sxs-lookup"><span data-stu-id="c511e-106">This procedure doesn't include setup of data that can be used in the Buyer´s push, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="c511e-107">See protsess kasutab demoettevõtte USRT-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="c511e-107">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="c511e-108">Valige Buyer's push (Kesklaost jaotus).</span><span class="sxs-lookup"><span data-stu-id="c511e-108">Go to Buyer's push.</span></span>
2. <span data-ttu-id="c511e-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="c511e-109">Click New.</span></span>
3. <span data-ttu-id="c511e-110">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="c511e-110">In the Description field, type a value.</span></span>
4. <span data-ttu-id="c511e-111">Sisestage või valige väärtus väljal Koht.</span><span class="sxs-lookup"><span data-stu-id="c511e-111">In the Site field, enter or select a value.</span></span>
5. <span data-ttu-id="c511e-112">Sisestage või valige väljal Ladu ladu, milles on vajalikud kaubakogused käepärast.</span><span class="sxs-lookup"><span data-stu-id="c511e-112">In the Warehouse field, enter or select a warehouse that has products with on-hand quantities.</span></span>
6. <span data-ttu-id="c511e-113">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="c511e-113">Click Add.</span></span>
7. <span data-ttu-id="c511e-114">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="c511e-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="c511e-115">Sisestage või valige väljal Item (Kaup) number või toode.</span><span class="sxs-lookup"><span data-stu-id="c511e-115">In the Item number field, enter or select a product.</span></span>
9. <span data-ttu-id="c511e-116">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="c511e-116">Click Add.</span></span>
10. <span data-ttu-id="c511e-117">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="c511e-117">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="c511e-118">Sisestage või valige väljal Item number (Kauba number) tootevariant.</span><span class="sxs-lookup"><span data-stu-id="c511e-118">In the Item number field, enter or select a variant product.</span></span>
    * <span data-ttu-id="c511e-119">Tootevariandi sisestamisel luuakse iga variandi jaoks rida.</span><span class="sxs-lookup"><span data-stu-id="c511e-119">When entering a variant product, lines will be created for each variant.</span></span>  
12. <span data-ttu-id="c511e-120">Märkige loendis rida.</span><span class="sxs-lookup"><span data-stu-id="c511e-120">In the list, mark a row.</span></span>
13. <span data-ttu-id="c511e-121">Sisestage väljale Jaotatud kogus, mitut valitud toodet soovite laiali saata.</span><span class="sxs-lookup"><span data-stu-id="c511e-121">In the Pushed quantity field, type how many of the selected product you want to distribute.</span></span>
14. <span data-ttu-id="c511e-122">Sisestage väljale Lisakogus jaotamiseks toodete kogus, mis on jaotamiseks piisavas koguses saadaval.</span><span class="sxs-lookup"><span data-stu-id="c511e-122">In the Additional quantity to push field, enter the quantity of the products that have available quantity to distribute.</span></span>
15. <span data-ttu-id="c511e-123">Sisestage väljale Distribution (Jaotus) asukoha kaal.</span><span class="sxs-lookup"><span data-stu-id="c511e-123">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="c511e-124">Saate teisi tüüpe valida teiste jaotusreeglite kasutamiseks.</span><span class="sxs-lookup"><span data-stu-id="c511e-124">You can select the other types to use other rules for the distribution.</span></span>  
16. <span data-ttu-id="c511e-125">Sisestage väljale Täiendamise hierarhia väärtus.</span><span class="sxs-lookup"><span data-stu-id="c511e-125">In the Replenishment hierarchy field, select a value.</span></span>
17. <span data-ttu-id="c511e-126">Valige Jah väljal Respect assortments (Sortimendi tunnustamine).</span><span class="sxs-lookup"><span data-stu-id="c511e-126">Select Yes in the Respect assortments field.</span></span>
18. <span data-ttu-id="c511e-127">Klõpsake valikut Arvuta kogused ja vaadake üle jaotise Ladu ridadesse lisatud kogused.</span><span class="sxs-lookup"><span data-stu-id="c511e-127">Click Calculate quantities and review the quantities that are added to the rows in the Warehouse section.</span></span>
19. <span data-ttu-id="c511e-128">Klõpsake valikut Create order (Loo tellimus).</span><span class="sxs-lookup"><span data-stu-id="c511e-128">Click Create order.</span></span>
20. <span data-ttu-id="c511e-129">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="c511e-129">Click Yes.</span></span>


