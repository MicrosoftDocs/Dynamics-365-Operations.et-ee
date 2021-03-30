---
title: Toote elutsükli vaikeoleku loomine
description: See protseduur näitab, kuidas luua toote elutsükli vaikeolekut ja kuidas seostada vaikeolekut väljastatud toodetega.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b65f34c1d7a0fd22201df5b48f8d42d452d6b8ef
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216077"
---
# <a name="create-a-default-product-lifecycle-state"></a><span data-ttu-id="ccac1-103">Toote elutsükli vaikeoleku loomine</span><span class="sxs-lookup"><span data-stu-id="ccac1-103">Create a default product lifecycle state</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ccac1-104">See protseduur näitab, kuidas luua toote elutsükli vaikeolekut ja kuidas seostada vaikeolekut väljastatud toodetega.</span><span class="sxs-lookup"><span data-stu-id="ccac1-104">This procedure shows how to create a default product lifecycle state as well as how to associate the default state with released products.</span></span>


## <a name="create-a-default-lifecycle-state"></a><span data-ttu-id="ccac1-105">Elutsükli vaikeoleku loomine</span><span class="sxs-lookup"><span data-stu-id="ccac1-105">Create a default lifecycle state</span></span>
1. <span data-ttu-id="ccac1-106">Avage Tooteteabe haldus > Häälestus > Toote elutsükli olek.</span><span class="sxs-lookup"><span data-stu-id="ccac1-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="ccac1-107">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ccac1-107">Click New.</span></span>
3. <span data-ttu-id="ccac1-108">Tippige väärtus väljale Olek.</span><span class="sxs-lookup"><span data-stu-id="ccac1-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="ccac1-109">Väljal Vaikesäte juriidilisele isikule väljastamisel valige Jah.</span><span class="sxs-lookup"><span data-stu-id="ccac1-109">Select Yes in the Default when released to legal entity field.</span></span>
5. <span data-ttu-id="ccac1-110">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="ccac1-110">In the Description field, type a value.</span></span>
6. <span data-ttu-id="ccac1-111">Valige Ei väljal On planeerimiseks aktiivne.</span><span class="sxs-lookup"><span data-stu-id="ccac1-111">Select No in the Is active for planning field.</span></span>

> [!NOTE]
> <span data-ttu-id="ccac1-112">Kui uut väljastatud toodet ei ole vaja koondplaneerimisse kaasta, valige Ei.</span><span class="sxs-lookup"><span data-stu-id="ccac1-112">If a new released product should not be included in Master planning, select No.</span></span> <span data-ttu-id="ccac1-113">Kui see tuleks koondplaneerimisse kaasata, säilitage juhtelemendi vaikeväärtus Jah.</span><span class="sxs-lookup"><span data-stu-id="ccac1-113">If it should be included in Master planning, leave the control at its default value Yes.</span></span>  

## <a name="create-a-new-released-product"></a><span data-ttu-id="ccac1-114">Uue väljastatud toote loomine</span><span class="sxs-lookup"><span data-stu-id="ccac1-114">Create a new released product</span></span>
1. <span data-ttu-id="ccac1-115">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ccac1-115">Close the page.</span></span>
2. <span data-ttu-id="ccac1-116">Avage Tooteteabe haldus > Tooted > Väljastatud tooted.</span><span class="sxs-lookup"><span data-stu-id="ccac1-116">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="ccac1-117">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ccac1-117">Click New.</span></span>
4. <span data-ttu-id="ccac1-118">Sisestage väärtus väljale Toote number.</span><span class="sxs-lookup"><span data-stu-id="ccac1-118">In the Product number field, type a value.</span></span>
5. <span data-ttu-id="ccac1-119">Sisestage väärtus väljale Toote nimi.</span><span class="sxs-lookup"><span data-stu-id="ccac1-119">In the Product name field, type a value.</span></span>
6. <span data-ttu-id="ccac1-120">Sisestage väärtus väljale Otsingunimi.</span><span class="sxs-lookup"><span data-stu-id="ccac1-120">In the Search name field, type a value.</span></span>
7. <span data-ttu-id="ccac1-121">Sisestage või valige väärtus väljal Kauba mudeligrupp.</span><span class="sxs-lookup"><span data-stu-id="ccac1-121">In the Item model group field, enter or select a value.</span></span>
8. <span data-ttu-id="ccac1-122">Sisestage või valige väärtus väljal Kaubagrupp.</span><span class="sxs-lookup"><span data-stu-id="ccac1-122">In the Item group field, enter or select a value.</span></span>
9. <span data-ttu-id="ccac1-123">Sisestage või valige väärtus väljal Laoala dimensioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="ccac1-123">In the Storage dimension group field, enter or select a value.</span></span>
10. <span data-ttu-id="ccac1-124">Sisestage või valige väärtus väljal Jälgimisdimensioonigrupp.</span><span class="sxs-lookup"><span data-stu-id="ccac1-124">In the Tracking dimension group field, enter or select a value.</span></span>
11. <span data-ttu-id="ccac1-125">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="ccac1-125">Click OK.</span></span>

> [!NOTE]
> <span data-ttu-id="ccac1-126">Toote elutsükli vaikeolek on globaalne määratlus.</span><span class="sxs-lookup"><span data-stu-id="ccac1-126">The default product lifecycle state is a global definition.</span></span>  

## <a name="change-the-product-to-an-active-state"></a><span data-ttu-id="ccac1-127">Toote aktiivsesse olekusse määramine</span><span class="sxs-lookup"><span data-stu-id="ccac1-127">Change the product to an active state</span></span>
1. <span data-ttu-id="ccac1-128">Väljal Toote elutsükli olek sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="ccac1-128">In the Product lifecycle state field, enter or select a value.</span></span>

> [!NOTE]
> <span data-ttu-id="ccac1-129">Oletame, et aktiivne olek on seadistatud, mis tähendab, et saate nüüd aktiivse oleku valida ja lubada toodet kasutada koondplaneerimisel ja koosluse taseme arvutamisel.</span><span class="sxs-lookup"><span data-stu-id="ccac1-129">Assume that you have set up an active state, you can now select the active state to allow the product to be used in Master planning and BOM-level calculation.</span></span> <span data-ttu-id="ccac1-130">See on loogiline ainult juhul, kui kõik ühtse planeerimise jaoks vajalikud toodete üksikasjad on määratud.</span><span class="sxs-lookup"><span data-stu-id="ccac1-130">Obviously, this only makes sense if all the product details that are required for consistent planning are specified.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]