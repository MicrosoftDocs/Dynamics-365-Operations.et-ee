---
title: " Töötaja konfigureerimine"
description: See protseduur näitab, kuidas konfigureerida töötajat müügiesindajana, kellel on õigus komisjonitasule kassa müügilt.
author: jblucher
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CommissionSalesGroup, CommissionSalesMember, DirPartyLookup, HcmWorker
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aee84f2dc39d2225985992fac0f9c20985ed9804
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022234"
---
# <a name="configure-a-worker"></a><span data-ttu-id="3eb1d-103"> Töötaja konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="3eb1d-103">Configure a worker</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="3eb1d-104">See protseduur näitab, kuidas konfigureerida töötajat müügiesindajana, kellel on õigus komisjonitasule kassa müügilt.</span><span class="sxs-lookup"><span data-stu-id="3eb1d-104">This procedure demonstrates how to configure a worker as a sales representative who is eligible for commission on sales in POS.</span></span> <span data-ttu-id="3eb1d-105">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="3eb1d-105">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-commission-sales-group-for-the-worker"></a><span data-ttu-id="3eb1d-106">Komisjonimüügi grupi loomine töötajale</span><span class="sxs-lookup"><span data-stu-id="3eb1d-106">Create a commission sales group for the worker</span></span>
1. <span data-ttu-id="3eb1d-107">Tehke valik Müük ja turundus > Komisjonitasud > Müügigrupid.</span><span class="sxs-lookup"><span data-stu-id="3eb1d-107">Go to Sales and marketing > Commissions > Sales groups.</span></span>
    * <span data-ttu-id="3eb1d-108">Töötajad saab määrata vähemalt ühte müügigruppi.</span><span class="sxs-lookup"><span data-stu-id="3eb1d-108">Workers can be assigned to one or more sales groups.</span></span> <span data-ttu-id="3eb1d-109">Kassas saate valida kaupluse aadressiraamatust mis tahes töötajaid sisaldava müügigrupi.</span><span class="sxs-lookup"><span data-stu-id="3eb1d-109">In POS, you can choose any sales group that contains workers from the store's address book.</span></span>  
2. <span data-ttu-id="3eb1d-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="3eb1d-110">Click New.</span></span>
3. <span data-ttu-id="3eb1d-111">Sisestage väärtus väljale Grupp.</span><span class="sxs-lookup"><span data-stu-id="3eb1d-111">In the Group field, type a value.</span></span>
4. <span data-ttu-id="3eb1d-112">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="3eb1d-112">In the Name field, type a value.</span></span>
5. <span data-ttu-id="3eb1d-113">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="3eb1d-113">Click Save.</span></span>
6. <span data-ttu-id="3eb1d-114">Klõpsake toimingupaanil valikut Üldine.</span><span class="sxs-lookup"><span data-stu-id="3eb1d-114">On the Action Pane, click General.</span></span>
7. <span data-ttu-id="3eb1d-115">Klõpsake valikut Müügiesindaja.</span><span class="sxs-lookup"><span data-stu-id="3eb1d-115">Click Sales rep.</span></span>
    * <span data-ttu-id="3eb1d-116">Müügigrupp võib sisaldada mitut töötajat.</span><span class="sxs-lookup"><span data-stu-id="3eb1d-116">A sales group can contain more than one worker.</span></span> <span data-ttu-id="3eb1d-117">Komisjonitasud saab töötajate vahel jagada selle põhjal, kuidas komisjonitasu jagamise määratlete.</span><span class="sxs-lookup"><span data-stu-id="3eb1d-117">Commissions can be split between workers based on how you define the commission share.</span></span>  
8. <span data-ttu-id="3eb1d-118">Sisestage või valige väärtus väljal Nimi.</span><span class="sxs-lookup"><span data-stu-id="3eb1d-118">In the Name field, enter or select a value.</span></span>
9. <span data-ttu-id="3eb1d-119">Sisestage number väljale Komisjonitasu osa.</span><span class="sxs-lookup"><span data-stu-id="3eb1d-119">In the Commission share field, enter a number.</span></span>
10. <span data-ttu-id="3eb1d-120">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="3eb1d-120">Click Save.</span></span>
11. <span data-ttu-id="3eb1d-121">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="3eb1d-121">Close the page.</span></span>
12. <span data-ttu-id="3eb1d-122">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="3eb1d-122">Close the page.</span></span>

## <a name="assign-the-workers-default-sales-group"></a><span data-ttu-id="3eb1d-123">Töötajatele müügi vaikegrupi määramine</span><span class="sxs-lookup"><span data-stu-id="3eb1d-123">Assign the workers default sales group</span></span>
1. <span data-ttu-id="3eb1d-124">Avage Jaemüük ja kaubandus > Töövõtjad > Töötajad.</span><span class="sxs-lookup"><span data-stu-id="3eb1d-124">Go to Retail and Commerce > Employees > Workers.</span></span>
2. <span data-ttu-id="3eb1d-125">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="3eb1d-125">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="3eb1d-126">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="3eb1d-126">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="3eb1d-127">Klõpsake vahekaarti Kaubandus.</span><span class="sxs-lookup"><span data-stu-id="3eb1d-127">Click the Commerce tab.</span></span>
    * <span data-ttu-id="3eb1d-128">Töötaja saab määrata müügi vaikegruppi.</span><span class="sxs-lookup"><span data-stu-id="3eb1d-128">A worker can be assigned to a default sales group.</span></span> <span data-ttu-id="3eb1d-129">Müügi vaikegrupp lisatakse kassas automaatselt müügiridadele, kui see valik on kaupluse funktsiooniprofiilis lubatud.</span><span class="sxs-lookup"><span data-stu-id="3eb1d-129">The default sales group will be automatically added to sales lines in POS if the option is enabled in the functionality profile for the store.</span></span>  
5. <span data-ttu-id="3eb1d-130">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="3eb1d-130">Click Edit.</span></span>
6. <span data-ttu-id="3eb1d-131">Valige või sisestage väärtus väljal Vaikegrupp.</span><span class="sxs-lookup"><span data-stu-id="3eb1d-131">In the Default group field, enter or select a value.</span></span>
7. <span data-ttu-id="3eb1d-132">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="3eb1d-132">Click Save.</span></span>
