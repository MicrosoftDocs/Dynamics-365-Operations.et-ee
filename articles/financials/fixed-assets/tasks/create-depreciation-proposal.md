---
title: Kulumisoovituse koostamine
description: "See protseduur kirjeldab, kuidas töötavad kulumi partiisoovitused, ja selles selgitatakse, kuidas põhivarade kulumit soovitada."
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: d11554ee5f26ef5a85e799194d2f75757a31c254
ms.contentlocale: et-ee
ms.lasthandoff: 09/14/2018

---

# <a name="create-depreciation-proposal"></a><span data-ttu-id="27671-103">Kulumisoovituse koostamine</span><span class="sxs-lookup"><span data-stu-id="27671-103">Create depreciation proposal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="27671-104">See protseduur kirjeldab, kuidas töötavad kulumi partiisoovitused, ja selles selgitatakse, kuidas põhivarade kulumit soovitada.</span><span class="sxs-lookup"><span data-stu-id="27671-104">This procedure describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="27671-105">See ülesanne kasutab demoettevõtet USMF ja raamatupidaja rolli.</span><span class="sxs-lookup"><span data-stu-id="27671-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-depreciation-proposal"></a><span data-ttu-id="27671-106">Kulumisoovituse koostamine</span><span class="sxs-lookup"><span data-stu-id="27671-106">Create depreciation proposal</span></span>
1. <span data-ttu-id="27671-107">Avage Põhivarad > Töölehe kirjed > Kulumisoovituse koostamine.</span><span class="sxs-lookup"><span data-stu-id="27671-107">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span>
2. <span data-ttu-id="27671-108">Klõpsake väljal Töölehe nimi otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="27671-108">In the Name of journal field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="27671-109">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="27671-109">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="27671-110">Sisestage kuupäev väljale Lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="27671-110">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="27671-111">Valige suvand Summeeri kulum, et esitada igakuiste kulumite kokkuvõte ühel töölehe real.</span><span class="sxs-lookup"><span data-stu-id="27671-111">Select the Summarize depreciation option to summarize monthly depreciations into one journal line.</span></span>  
    * <span data-ttu-id="27671-112">Näiteks, kui lõpukuupäeva väärtus on 31. märts 2015, siis luuakse järgmine kirjeldus: "Kulum alates 31. jaanuar 2015."</span><span class="sxs-lookup"><span data-stu-id="27671-112">For example, if the To date value is March 31, 2015, the following description is generated: “Depreciation since January 31, 2015.”</span></span> <span data-ttu-id="27671-113">Soovitatud tööleheridade kuupäevavälja väärtuseks seatakse siis 31. märts 2015.</span><span class="sxs-lookup"><span data-stu-id="27671-113">The Date field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    * <span data-ttu-id="27671-114">Kulumisoovitust saab filtrida vara, varagrupi või muude kriteeriumide järgi, kasutades suvandit Filtri.</span><span class="sxs-lookup"><span data-stu-id="27671-114">The depreciation proposal can be filtered by asset, asset group, or other criteria using the Filter option.</span></span>  
    * <span data-ttu-id="27671-115">Kui kasutate vormi Looge põhivara soetamise või kulumi pakkumisi, saate soovitada kulumit partiidena.</span><span class="sxs-lookup"><span data-stu-id="27671-115">When you use the Create acquisition or depreciation proposals for fixed assets form, you can propose depreciation in batches.</span></span> <span data-ttu-id="27671-116">See on soovitatav suuremate soovituste puhul, mis kasutavad rohkem süsteemi ressursse.</span><span class="sxs-lookup"><span data-stu-id="27671-116">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="27671-117">Kui valite partii suvandi, saate töö ajal endiselt muid ülesandeid teha.</span><span class="sxs-lookup"><span data-stu-id="27671-117">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="27671-118">Kui soovitate kulumit sel moel, arvutatakse põhivarade väärtusmudelite kulum.</span><span class="sxs-lookup"><span data-stu-id="27671-118">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  
5. <span data-ttu-id="27671-119">Klõpsake suvandit Loo tööleht.</span><span class="sxs-lookup"><span data-stu-id="27671-119">Click Create journal.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="27671-120">Kulumiraamatu kannete ülevaade</span><span class="sxs-lookup"><span data-stu-id="27671-120">Review depreciation entries</span></span>
1. <span data-ttu-id="27671-121">Avage Põhivarad > Töölehe sisestused > Põhivarade tööleht.</span><span class="sxs-lookup"><span data-stu-id="27671-121">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="27671-122">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="27671-122">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="27671-123">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="27671-123">Click Lines.</span></span>
4. <span data-ttu-id="27671-124">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="27671-124">Click Post.</span></span>


