---
title: Põhivara tükeldamine
description: See teema selgitab, kuidas tükeldada ühe vararaamatu protsenti uude vararaamatusse.
author: saraschi2
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetTable, AssetBook, AssetSplit, AssetBookLookup, LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a4e001a6fdf390c6211ba85aa327b60dcdf16d9e
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177318"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="cd91b-103">Põhivara tükeldamine</span><span class="sxs-lookup"><span data-stu-id="cd91b-103">Split a fixed asset</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cd91b-104">See teema selgitab, kuidas tükeldada ühe vararaamatu protsenti uude vararaamatusse.</span><span class="sxs-lookup"><span data-stu-id="cd91b-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="cd91b-105">See kasutab raamatupidaja rolli ja USMF-i demoandmeid.</span><span class="sxs-lookup"><span data-stu-id="cd91b-105">It uses the Accountant role and USMF demo data.</span></span>


## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="cd91b-106">Uue põhivara loomine</span><span class="sxs-lookup"><span data-stu-id="cd91b-106">Create a new fixed asset</span></span>
1. <span data-ttu-id="cd91b-107">Navigeerimispaanil avage **Moodulid > Põhivarad > Põhivarad > Põhivarad**.</span><span class="sxs-lookup"><span data-stu-id="cd91b-107">In the navigation pane, go to **Modules > Fixed assets > Fixed assets > Fixed assets**.</span></span>
2. <span data-ttu-id="cd91b-108">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="cd91b-108">Select **New**.</span></span>
3. <span data-ttu-id="cd91b-109">Väljale **Põhivara grupp** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="cd91b-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="cd91b-110">Märkige põhivara kood hilisemaks tükeldamisprotsessis kasutamiseks üles.</span><span class="sxs-lookup"><span data-stu-id="cd91b-110">Note the fixed asset number to use in the split process later.</span></span>  
4. <span data-ttu-id="cd91b-111">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="cd91b-111">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="cd91b-112">Sulgege vorm.</span><span class="sxs-lookup"><span data-stu-id="cd91b-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="cd91b-113">Põhivara tükeldamine</span><span class="sxs-lookup"><span data-stu-id="cd91b-113">Split a fixed asset</span></span>
1. <span data-ttu-id="cd91b-114">Leidke loendist tükeldatav põhivara ja valige selle link.</span><span class="sxs-lookup"><span data-stu-id="cd91b-114">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="cd91b-115">Valige **Raamatud**.</span><span class="sxs-lookup"><span data-stu-id="cd91b-115">Select **Books**.</span></span> <span data-ttu-id="cd91b-116">Valige uuele varale tükeldatav raamat.</span><span class="sxs-lookup"><span data-stu-id="cd91b-116">Select the book to split to the new asset.</span></span>  
3. <span data-ttu-id="cd91b-117">Valige **Funktsioonid**.</span><span class="sxs-lookup"><span data-stu-id="cd91b-117">Select **Functions**.</span></span>
4. <span data-ttu-id="cd91b-118">Valige **Tükelda põhivara**.</span><span class="sxs-lookup"><span data-stu-id="cd91b-118">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="cd91b-119">Sisestage väärtus väljale **Põhivarasse** või valige sellelt väljalt.</span><span class="sxs-lookup"><span data-stu-id="cd91b-119">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="cd91b-120">Klõpsake väljal **Raamatusse** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="cd91b-120">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="cd91b-121">Sisestage kuupäev väljale **Kande kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="cd91b-121">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="cd91b-122">Sisestage number väljale **Protsent**.</span><span class="sxs-lookup"><span data-stu-id="cd91b-122">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="cd91b-123">Valige või sisestage väärtus väljal **Töölehe nimi**.</span><span class="sxs-lookup"><span data-stu-id="cd91b-123">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="cd91b-124">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="cd91b-124">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="cd91b-125">Töölehekande sisestamine</span><span class="sxs-lookup"><span data-stu-id="cd91b-125">Post the journal transaction</span></span>
1. <span data-ttu-id="cd91b-126">Avage navigeerimispaneelil **Moodulid > Põhivarad > Töölehe kanded > Põhivarade tööleht**.</span><span class="sxs-lookup"><span data-stu-id="cd91b-126">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="cd91b-127">Valige loendist tükeldamise protsessis loodud tööleht.</span><span class="sxs-lookup"><span data-stu-id="cd91b-127">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="cd91b-128">Valige **Read**.</span><span class="sxs-lookup"><span data-stu-id="cd91b-128">Select **Lines**.</span></span>

    - <span data-ttu-id="cd91b-129">Kontrollige loodud töölehe ridu.</span><span class="sxs-lookup"><span data-stu-id="cd91b-129">Verify the journal lines created.</span></span>  
    - <span data-ttu-id="cd91b-130">Soetamise korrigeerimiskanne luuakse algse vara puhul väärtuse vähendamiseks tükeldamisprotsessis määratud protsendi võrra.</span><span class="sxs-lookup"><span data-stu-id="cd91b-130">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>  
    - <span data-ttu-id="cd91b-131">Soetamiskanne luuakse uue vara puhul samas summas.</span><span class="sxs-lookup"><span data-stu-id="cd91b-131">An Acquisition transaction is created for the new asset for the same amount.</span></span>  

4. <span data-ttu-id="cd91b-132">Valige **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="cd91b-132">Select **Post**.</span></span>

