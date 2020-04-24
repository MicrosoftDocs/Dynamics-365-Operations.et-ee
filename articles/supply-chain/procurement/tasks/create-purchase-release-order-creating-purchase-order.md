---
title: Ostu väljalaskeorderi loomine ostutellimuse koostamisel
description: See protseduur selgitab, kuidas kasutada ostulepingut ostutellimuse loomisel.
author: mkirknel
manager: tfehr
ms.date: 11/14/2016
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
ms.openlocfilehash: e3e02bd4aaef8da7838c92199c28b1e298078c57
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204857"
---
# <a name="create-a-purchase-release-order-when-creating-the-purchase-order"></a><span data-ttu-id="107e7-103">Ostu väljalaskeorderi loomine ostutellimuse koostamisel</span><span class="sxs-lookup"><span data-stu-id="107e7-103">Create a purchase release order when creating the purchase order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="107e7-104">See protseduur selgitab, kuidas kasutada ostulepingut ostutellimuse loomisel.</span><span class="sxs-lookup"><span data-stu-id="107e7-104">This procedure shows how to use a purchase agreement when you create a purchase order.</span></span> <span data-ttu-id="107e7-105">Ostutellimuse loomisel tuleb rakendada ostulepingut, kuna see sisaldab üldtingimusi, mis tuleb kopeerida ostutellimuse päisesse.</span><span class="sxs-lookup"><span data-stu-id="107e7-105">The purchase agreement has to be applied when you create the purchase order because there are general terms that should be copied to the purchase order header.</span></span> <span data-ttu-id="107e7-106">Seda ülesannet täidab üldjuhul ostuagent.</span><span class="sxs-lookup"><span data-stu-id="107e7-106">Typically this task would be carried out by a purchasing agent.</span></span> <span data-ttu-id="107e7-107">Juhendi eeltingimusena peab teil olema kehtiv ostuleping koos toote koguse kohustusega hankija ja kaupade kohta.</span><span class="sxs-lookup"><span data-stu-id="107e7-107">As a prerequisite for this guide, you must have an effective purchase agreement with a product quantity commitment for a vendor and items.</span></span> <span data-ttu-id="107e7-108">Sama protseduuri saab kasutada, kui teil on ostuleping, millel on muud tüüpi kohustusi.</span><span class="sxs-lookup"><span data-stu-id="107e7-108">The same procedure can be used if you have a purchase agreement with other types of commitments.</span></span> <span data-ttu-id="107e7-109">Saate selle juhendi käitada demoettevõtte USMF andmetega.</span><span class="sxs-lookup"><span data-stu-id="107e7-109">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="107e7-110">Kui kasutate USMF-i, saate esmalt käivitada juhendi „Ostulepingu loomine”, et seadistada selle juhendi jaoks vajalikud eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="107e7-110">If you're using USMF, you can run the "Create a purchase agreement" guide first to set up the necessary preconditions for this guide.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="107e7-111">Ostutellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="107e7-111">Create a purchase order</span></span>
1. <span data-ttu-id="107e7-112">Avage ostutellimuse ettevalmistamise tööruum.</span><span class="sxs-lookup"><span data-stu-id="107e7-112">Open the purchase order preparation workspace.</span></span>
2. <span data-ttu-id="107e7-113">Klõpsake suvandit Uus ostutellimus.</span><span class="sxs-lookup"><span data-stu-id="107e7-113">Click New purchase order.</span></span>
3. <span data-ttu-id="107e7-114">Klõpsake väljal Hankija konto otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="107e7-114">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="107e7-115">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="107e7-115">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="107e7-116">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="107e7-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="107e7-117">Lülitage jaotise Üldine laiendamist.</span><span class="sxs-lookup"><span data-stu-id="107e7-117">Toggle the expansion of the General section.</span></span>
7. <span data-ttu-id="107e7-118">Klõpsake väljal Ostuleping otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="107e7-118">In the Purchase agreement field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="107e7-119">Siin loetletakse kõik hankija puhul saadaolevad lepped.</span><span class="sxs-lookup"><span data-stu-id="107e7-119">All available agreements for the vendor are listed here.</span></span> <span data-ttu-id="107e7-120">Leidke kehtiv lepe, mida soovite kasutada.</span><span class="sxs-lookup"><span data-stu-id="107e7-120">Find the effective agreement that you want to use.</span></span>  
8. <span data-ttu-id="107e7-121">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="107e7-121">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="107e7-122">Klõpsake nuppu Jah.</span><span class="sxs-lookup"><span data-stu-id="107e7-122">Click Yes.</span></span>
10. <span data-ttu-id="107e7-123">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="107e7-123">Click OK.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="107e7-124">Rea lisamine</span><span class="sxs-lookup"><span data-stu-id="107e7-124">Add a line</span></span>
1. <span data-ttu-id="107e7-125">Sisestage väärtus väljale Kaubakood.</span><span class="sxs-lookup"><span data-stu-id="107e7-125">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="107e7-126">Kui kohustusel on kindlad varud või asukoha dimensioonid, peate leppe kasutamiseks sisestama sama väärtuse ostutellimuse reale.</span><span class="sxs-lookup"><span data-stu-id="107e7-126">If there are specific inventory or location dimensions on the commitment you must enter the same values on the purchase order line to make use of the agreement.</span></span>  
2. <span data-ttu-id="107e7-127">Klõpsake väljal Koht otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="107e7-127">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="107e7-128">Tegevuskoht võib olla juba täidetud vaikeväärtusega tellimuselt või hankijalt.</span><span class="sxs-lookup"><span data-stu-id="107e7-128">The site may already be populated with the default value from the order, or from the vendor.</span></span> <span data-ttu-id="107e7-129">Sellisel juhul jätke see etapp vahele.</span><span class="sxs-lookup"><span data-stu-id="107e7-129">If this is the case, skip this step.</span></span>  
3. <span data-ttu-id="107e7-130">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="107e7-130">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="107e7-131">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="107e7-131">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="107e7-132">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="107e7-132">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="107e7-133">Kontrollige, kas hind on kohustusest kopeeritud.</span><span class="sxs-lookup"><span data-stu-id="107e7-133">Validate that the price is copied from the commitment.</span></span>  

## <a name="look-up-the-commitment"></a><span data-ttu-id="107e7-134">Kohustuse otsimine</span><span class="sxs-lookup"><span data-stu-id="107e7-134">Look up the commitment</span></span>
1. <span data-ttu-id="107e7-135">Klõpsake käsku Värskenda rida.</span><span class="sxs-lookup"><span data-stu-id="107e7-135">Click Update line.</span></span>
2. <span data-ttu-id="107e7-136">Klõpsake valikut Seotud.</span><span class="sxs-lookup"><span data-stu-id="107e7-136">Click Attached.</span></span>
    * <span data-ttu-id="107e7-137">Siin saate hankida ostulepingu üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="107e7-137">Here you can get details for the purchase agreement.</span></span> <span data-ttu-id="107e7-138">Näiteks saate vaadata hinda ning seda, kas hind ja allahindlus on fikseeritud, mis tähendab, et kui muudate ostutellimusel hinna või allahindluse muutmisel muule väärtusele kui on kohustusel, eemaldab süsteem lingi, nii et ostutellimuse rida ei täida kohustust.</span><span class="sxs-lookup"><span data-stu-id="107e7-138">For example, you can see the price and whether the price and discount are fixed, which means that if you change price or discount on the purchase order to a different value than on the commitment, the system will remove the link so the purchase order line does not fulfill the commitment.</span></span> <span data-ttu-id="107e7-139">Näete ka seda, kas suvand Maksimaalne on jõustatud on valitud, mis tähendab, et kohustusel olevat kogust ei saa ületada, summeerides kõik kohustust täitvad ostud.</span><span class="sxs-lookup"><span data-stu-id="107e7-139">You can also see if the Max is enforced option is selected, which means that the quantity on the commitment cannot be exceeded by summing all of the purchases that fulfill the commitment.</span></span>  
3. <span data-ttu-id="107e7-140">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="107e7-140">Close the page.</span></span>

## <a name="look-up-the-purchase-agreement"></a><span data-ttu-id="107e7-141">Ostulepingu otsimine</span><span class="sxs-lookup"><span data-stu-id="107e7-141">Look up the purchase agreement</span></span>
1. <span data-ttu-id="107e7-142">Klõpsake toimingupaanil valikut Üldine.</span><span class="sxs-lookup"><span data-stu-id="107e7-142">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="107e7-143">Klõpsake suvandit Ostuleping.</span><span class="sxs-lookup"><span data-stu-id="107e7-143">Click Purchase agreement.</span></span>
3. <span data-ttu-id="107e7-144">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="107e7-144">Close the page.</span></span>
4. <span data-ttu-id="107e7-145">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="107e7-145">Close the page.</span></span>

