--- 
title: " Töötaja konfigureerimine"
description: "See protseduur näitab, kuidas konfigureerida jaemüügi töötajat müügiesindajana, kellel on õigus komisjonitasule kassa müügilt."
author: jblucher
manager: AnnBe
ms.date: 02/22/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: 27b075cf1152f16fc4726b224e877eacb2f2572c
ms.contentlocale: et-ee
ms.lasthandoff: 02/07/2018

---
# <a name="configure-a-worker"></a><span data-ttu-id="23d67-103"> Töötaja konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="23d67-103">Configure a worker</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="23d67-104">See protseduur näitab, kuidas konfigureerida jaemüügi töötajat müügiesindajana, kellel on õigus komisjonitasule kassa müügilt.</span><span class="sxs-lookup"><span data-stu-id="23d67-104">This procedure demonstrates how to configure a retail worker as a sales representative who is eligible for commission on sales in POS.</span></span> <span data-ttu-id="23d67-105">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="23d67-105">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-commission-sales-group-for-the-worker"></a><span data-ttu-id="23d67-106">Komisjonimüügi grupi loomine töötajale</span><span class="sxs-lookup"><span data-stu-id="23d67-106">Create a commission sales group for the worker</span></span>
1. <span data-ttu-id="23d67-107">Tehke valik Müük ja turundus > Komisjonitasud > Müügigrupid.</span><span class="sxs-lookup"><span data-stu-id="23d67-107">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="23d67-108">Töötajad saab määrata vähemalt ühte müügigruppi.</span><span class="sxs-lookup"><span data-stu-id="23d67-108">Workers can be assigned to one or more sales groups.</span></span> <span data-ttu-id="23d67-109">Kassas saate valida kaupluse aadressiraamatust mis tahes töötajaid sisaldava müügigrupi.</span><span class="sxs-lookup"><span data-stu-id="23d67-109">In POS, you can choose any sales group that contains workers from the store's address book.</span></span>  
2. <span data-ttu-id="23d67-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="23d67-110">Click New.</span></span>
3. <span data-ttu-id="23d67-111">Sisestage väärtus väljale Grupp.</span><span class="sxs-lookup"><span data-stu-id="23d67-111">In the Group field, type a value.</span></span>
4. <span data-ttu-id="23d67-112">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="23d67-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="23d67-113">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="23d67-113">Click Save.</span></span>
6. <span data-ttu-id="23d67-114">Klõpsake toimingupaanil valikut Üldine.</span><span class="sxs-lookup"><span data-stu-id="23d67-114">On the Action Pane, click General.</span></span>
7. <span data-ttu-id="23d67-115">Klõpsake valikut Müügiesindaja.</span><span class="sxs-lookup"><span data-stu-id="23d67-115">Click Sales rep.</span></span>
    * <span data-ttu-id="23d67-116">Müügigrupp võib sisaldada mitut töötajat.</span><span class="sxs-lookup"><span data-stu-id="23d67-116">A sales group can contain more than one worker.</span></span> <span data-ttu-id="23d67-117">Komisjonitasud saab töötajate vahel jagada selle põhjal, kuidas komisjonitasu jagamise määratlete.</span><span class="sxs-lookup"><span data-stu-id="23d67-117">Commissions can be split between workers based on how you define the commission share.</span></span>  
8. <span data-ttu-id="23d67-118">Sisestage või valige väärtus väljal Nimi.</span><span class="sxs-lookup"><span data-stu-id="23d67-118">In the Name field, enter or select a value.</span></span>
9. <span data-ttu-id="23d67-119">Sisestage number väljale Komisjonitasu osa.</span><span class="sxs-lookup"><span data-stu-id="23d67-119">In the Commission share field, enter a number.</span></span>
10. <span data-ttu-id="23d67-120">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="23d67-120">Click Save.</span></span>
11. <span data-ttu-id="23d67-121">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="23d67-121">Close the page.</span></span>
12. <span data-ttu-id="23d67-122">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="23d67-122">Close the page.</span></span>

## <a name="assign-the-workers-default-sales-group"></a><span data-ttu-id="23d67-123">Töötajatele müügi vaikegrupi määramine</span><span class="sxs-lookup"><span data-stu-id="23d67-123">Assign the workers default sales group</span></span>
1. <span data-ttu-id="23d67-124">Avage Jaemüük ja kaubandus > Töötajad > Töötajad.</span><span class="sxs-lookup"><span data-stu-id="23d67-124">Go to Retail and commerce > Employees > Workers.</span></span>
2. <span data-ttu-id="23d67-125">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="23d67-125">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="23d67-126">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="23d67-126">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="23d67-127">Klõpsake vahekaarti Jaemüük.</span><span class="sxs-lookup"><span data-stu-id="23d67-127">Click the Retail tab.</span></span>
    * <span data-ttu-id="23d67-128">Töötaja saab määrata müügi vaikegruppi.</span><span class="sxs-lookup"><span data-stu-id="23d67-128">A worker can be assigned to a default sales group.</span></span> <span data-ttu-id="23d67-129">Müügi vaikegrupp lisatakse kassas automaatselt müügiridadele, kui see valik on kaupluse funktsiooniprofiilis lubatud.</span><span class="sxs-lookup"><span data-stu-id="23d67-129">The default sales group will be automatically added to sales lines in POS if the option is enabled in the functionality profile for the store.</span></span>  
5. <span data-ttu-id="23d67-130">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="23d67-130">Click Edit.</span></span>
6. <span data-ttu-id="23d67-131">Valige või sisestage väärtus väljal Vaikegrupp.</span><span class="sxs-lookup"><span data-stu-id="23d67-131">In the Default group field, enter or select a value.</span></span>
7. <span data-ttu-id="23d67-132">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="23d67-132">Click Save.</span></span>


