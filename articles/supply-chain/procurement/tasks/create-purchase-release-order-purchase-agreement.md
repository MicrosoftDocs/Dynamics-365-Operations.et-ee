---
title: Ostu väljalaskeorderi loomine ostulepingu põhjal
description: See protseduur selgitab, kuidas kasutada ostulepingut ostutellimuse loomisel.
author: mkirknel
manager: tfehr
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee0c40dfc3c820343c7054238cc2da47e8203d59
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204809"
---
# <a name="create-a-purchase-release-order-from-a-purchase-agreement"></a><span data-ttu-id="b6745-103">Ostu väljalaskeorderi loomine ostulepingu põhjal</span><span class="sxs-lookup"><span data-stu-id="b6745-103">Create a purchase release order from a purchase agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b6745-104">See protseduur selgitab, kuidas kasutada ostulepingut ostutellimuse loomisel.</span><span class="sxs-lookup"><span data-stu-id="b6745-104">This procedure shows how to use a purchase agreement when you create a purchase order.</span></span> <span data-ttu-id="b6745-105">Ostutellimuse loomisel tuleb rakendada ostulepingut, kuna see sisaldab üldtingimusi, mis tuleb kopeerida ostutellimuse päisesse.</span><span class="sxs-lookup"><span data-stu-id="b6745-105">The purchase agreement has to be applied when you create the purchase order because there are general terms that should be copied to the purchase order header.</span></span> <span data-ttu-id="b6745-106">Seda ülesannet täidab üldjuhul ostuagent.</span><span class="sxs-lookup"><span data-stu-id="b6745-106">Typically this task would be carried out by a purchasing agent.</span></span> <span data-ttu-id="b6745-107">Juhendi eeltingimusena peab teil olema kehtiv ostuleping koos toote koguse kohustusega hankija ja kaupade kohta.</span><span class="sxs-lookup"><span data-stu-id="b6745-107">As a prerequisite for this guide, you must have an effective purchase agreement with a product quantity commitment for a vendor and items.</span></span> <span data-ttu-id="b6745-108">Sama protseduuri saab kasutada, kui teil on ostuleping, millel on muud tüüpi kohustusi.</span><span class="sxs-lookup"><span data-stu-id="b6745-108">The same procedure can be used if you have a purchase agreement with other types of commitments.</span></span> <span data-ttu-id="b6745-109">Saate selle juhendi käitada demoettevõtte USMF andmetega.</span><span class="sxs-lookup"><span data-stu-id="b6745-109">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="b6745-110">Kui kasutate USMF-i, saate esmalt käivitada juhendi „Ostulepingu loomine”, et seadistada selle juhendi jaoks vajalikud eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="b6745-110">If you're using USMF, you can run the "Create a purchase agreement" guide first to set up the necessary preconditions for this guide.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="b6745-111">Ostutellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="b6745-111">Create a purchase order</span></span>
1. <span data-ttu-id="b6745-112">Paanil **Navigeerimispaan** avage **Tööruumid > Ostutellimuse ettevalmistus**.</span><span class="sxs-lookup"><span data-stu-id="b6745-112">In the **Navigation pane**, go to **Workspaces > Purchase order preparation**.</span></span> 
2. <span data-ttu-id="b6745-113">Klõpsake **Uus ostutellimus**.</span><span class="sxs-lookup"><span data-stu-id="b6745-113">Click **New purchase order**.</span></span>
3. <span data-ttu-id="b6745-114">Klõpsake väljal **Hankija konto** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="b6745-114">In the **Vendor account** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="b6745-115">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="b6745-115">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="b6745-116">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="b6745-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="b6745-117">Suurendage vahekaarti **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="b6745-117">Expand the **General** fastTab.</span></span>
7. <span data-ttu-id="b6745-118">Väljal **Ostuleping** klõpsake rippmenüü nuppu, et avada otsing.</span><span class="sxs-lookup"><span data-stu-id="b6745-118">In the **Purchase agreement** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="b6745-119">Siin loetletakse kõik hankija puhul saadaolevad lepped.</span><span class="sxs-lookup"><span data-stu-id="b6745-119">All available agreements for the vendor are listed here.</span></span> <span data-ttu-id="b6745-120">Leidke kehtiv lepe, mida soovite kasutada.</span><span class="sxs-lookup"><span data-stu-id="b6745-120">Find the effective agreement that you want to use.</span></span>  
8. <span data-ttu-id="b6745-121">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="b6745-121">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="b6745-122">Klõpsake nuppu **Jah**.</span><span class="sxs-lookup"><span data-stu-id="b6745-122">Click **Yes**.</span></span>
10. <span data-ttu-id="b6745-123">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6745-123">Click **OK**.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="b6745-124">Rea lisamine</span><span class="sxs-lookup"><span data-stu-id="b6745-124">Add a line</span></span>
1. <span data-ttu-id="b6745-125">Sisestage väärtus väljale **Kaubakood**.</span><span class="sxs-lookup"><span data-stu-id="b6745-125">In the **Item number** field, type a value.</span></span> <span data-ttu-id="b6745-126">Kui kohustusel on kindlad varud või asukoha dimensioonid, peate leppe kasutamiseks sisestama sama väärtuse ostutellimuse reale.</span><span class="sxs-lookup"><span data-stu-id="b6745-126">If there are specific inventory or location dimensions on the commitment you must enter the same values on the purchase order line to make use of the agreement.</span></span>  
2. <span data-ttu-id="b6745-127">Klõpsake väljal **Sait** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="b6745-127">In the **Site** field, click the drop-down button to open the lookup.</span></span> <span data-ttu-id="b6745-128">Tegevuskoht võib olla juba täidetud vaikeväärtusega tellimuselt või hankijalt.</span><span class="sxs-lookup"><span data-stu-id="b6745-128">The site may already be populated with the default value from the order, or from the vendor.</span></span> <span data-ttu-id="b6745-129">Sellisel juhul jätke see etapp vahele.</span><span class="sxs-lookup"><span data-stu-id="b6745-129">If this is the case, skip this step.</span></span>  
3. <span data-ttu-id="b6745-130">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="b6745-130">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="b6745-131">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="b6745-131">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="b6745-132">Sisestage arv väljale **Kogus**.</span><span class="sxs-lookup"><span data-stu-id="b6745-132">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="b6745-133">Kontrollige, kas hind on kohustusest kopeeritud.</span><span class="sxs-lookup"><span data-stu-id="b6745-133">Validate that the price is copied from the commitment.</span></span>  

## <a name="look-up-the-commitment"></a><span data-ttu-id="b6745-134">Kohustuse otsimine</span><span class="sxs-lookup"><span data-stu-id="b6745-134">Look up the commitment</span></span>
1. <span data-ttu-id="b6745-135">Klõpsake nuppu **Värskenda rida**.</span><span class="sxs-lookup"><span data-stu-id="b6745-135">Click **Update line**.</span></span>
2. <span data-ttu-id="b6745-136">Klõpsake nuppu **Manustatud**.</span><span class="sxs-lookup"><span data-stu-id="b6745-136">Click **Attached**.</span></span> <span data-ttu-id="b6745-137">Siin saate hankida ostulepingu üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="b6745-137">Here you can get details for the purchase agreement.</span></span> <span data-ttu-id="b6745-138">Näiteks saate vaadata hinda ning seda, kas hind ja allahindlus on fikseeritud, mis tähendab, et kui muudate ostutellimusel hinna või allahindluse muutmisel muule väärtusele kui on kohustusel, eemaldab süsteem lingi, nii et ostutellimuse rida ei täida kohustust.</span><span class="sxs-lookup"><span data-stu-id="b6745-138">For example, you can see the price and whether the price and discount are fixed, which means that if you change price or discount on the purchase order to a different value than on the commitment, the system will remove the link so the purchase order line does not fulfill the commitment.</span></span> <span data-ttu-id="b6745-139">Näete ka seda, kas suvand Maksimaalne on jõustatud on valitud, mis tähendab, et kohustusel olevat kogust ei saa ületada, summeerides kõik kohustust täitvad ostud.</span><span class="sxs-lookup"><span data-stu-id="b6745-139">You can also see if the Max is enforced option is selected, which means that the quantity on the commitment cannot be exceeded by summing all of the purchases that fulfill the commitment.</span></span>  
3. <span data-ttu-id="b6745-140">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b6745-140">Close the page.</span></span>

## <a name="look-up-the-purchase-agreement"></a><span data-ttu-id="b6745-141">Ostulepingu otsimine</span><span class="sxs-lookup"><span data-stu-id="b6745-141">Look up the purchase agreement</span></span>
1. <span data-ttu-id="b6745-142">Paanil **Toimingupaan** klõpsake **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="b6745-142">On the **Action Pane**, click **General**.</span></span>
2. <span data-ttu-id="b6745-143">Klõpsake **Ostutellimus**.</span><span class="sxs-lookup"><span data-stu-id="b6745-143">Click **Purchase agreement**.</span></span>
3. <span data-ttu-id="b6745-144">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b6745-144">Close the page.</span></span>
4. <span data-ttu-id="b6745-145">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b6745-145">Close the page.</span></span>

