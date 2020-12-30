---
title: Kulumisoovituse koostamine
description: Teemas kirjeldatakse, kuidas töötavad kulumi pakettsoovitused, ja selgitatakse, kuidas soovitada põhivarade kulumit.
author: abruer
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransAsset
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 07337063c01f146c72ca6d9e0f9096907cdc9638
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442456"
---
# <a name="create-a-depreciation-proposal"></a><span data-ttu-id="e1708-103">Kulumisoovituse koostamine</span><span class="sxs-lookup"><span data-stu-id="e1708-103">Create a depreciation proposal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e1708-104">Teemas kirjeldatakse, kuidas töötavad kulumi pakettsoovitused, ja selgitatakse, kuidas soovitada põhivarade kulumit.</span><span class="sxs-lookup"><span data-stu-id="e1708-104">This topic describes how depreciation batch proposals work and explains how to propose depreciation for fixed assets.</span></span> <span data-ttu-id="e1708-105">See ülesanne kasutab demoettevõtet USMF ja raamatupidaja rolli.</span><span class="sxs-lookup"><span data-stu-id="e1708-105">This task uses the USMF demo company and the accountant role.</span></span>


## <a name="create-a-depreciation-proposal"></a><span data-ttu-id="e1708-106">Kulumisoovituse koostamine</span><span class="sxs-lookup"><span data-stu-id="e1708-106">Create a depreciation proposal</span></span>
1. <span data-ttu-id="e1708-107">Navigeerimispaanil avage **Moodulid > Põhivarad > Töölehe kanded > Loo kulumisoovitus**.</span><span class="sxs-lookup"><span data-stu-id="e1708-107">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Create depreciation proposal**.</span></span>
2. <span data-ttu-id="e1708-108">Väljal **Töölehe nimi** valige suvand rippmenüüst.</span><span class="sxs-lookup"><span data-stu-id="e1708-108">In the **Name of journal** field, select an option from the drop-down menu.</span></span>
3. <span data-ttu-id="e1708-109">Sisestage kuupäev väljale **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="e1708-109">In the **To date** field, enter a date.</span></span>

    - <span data-ttu-id="e1708-110">Valige suvand **Summeeri kulum**, et summerida igakuised kulumid ühele töölehe reale.</span><span class="sxs-lookup"><span data-stu-id="e1708-110">Select the **Summarize depreciation** option to summarize monthly depreciations into one journal line.</span></span>  
    - <span data-ttu-id="e1708-111">Näiteks, kui lõpukuupäeva väärtus on 31. märts 2015, siis luuakse järgmine kirjeldus: „Kulum alates 31. jaanuar 2015”.</span><span class="sxs-lookup"><span data-stu-id="e1708-111">For example, if the To date value is March 31, 2015, the following description is generated: "Depreciation since January 31, 2015."</span></span> <span data-ttu-id="e1708-112">Soovitud töölehe ridade väljale **Kuupäev** sisestatakse 31. märts 2015.</span><span class="sxs-lookup"><span data-stu-id="e1708-112">The **Date** field on the proposed journal lines is then set to March 31, 2015.</span></span>  
    - <span data-ttu-id="e1708-113">Kulumi soovitust saab filtreerida vara, vara grupi või muude kriteeriumide alusel, kasutades suvandit **Filter**.</span><span class="sxs-lookup"><span data-stu-id="e1708-113">The depreciation proposal can be filtered by asset, asset group, or other criteria using the **Filter** option.</span></span>  
    - <span data-ttu-id="e1708-114">Kui kasutate vormi **Looge põhivara soetamise või kulumi pakkumisi** saate koostada kulumisoovitusi partiina.</span><span class="sxs-lookup"><span data-stu-id="e1708-114">When you use the **Create acquisition or depreciation proposals for fixed assets** form, you can propose depreciation in batches.</span></span> <span data-ttu-id="e1708-115">See on soovitatav suuremate soovituste puhul, mis kasutavad rohkem süsteemi ressursse.</span><span class="sxs-lookup"><span data-stu-id="e1708-115">This is recommended for larger proposals that will use more system resources.</span></span> <span data-ttu-id="e1708-116">Kui valite partii suvandi, saate töö ajal endiselt muid ülesandeid teha.</span><span class="sxs-lookup"><span data-stu-id="e1708-116">If you select the batch option, you can still complete other tasks during that time.</span></span> <span data-ttu-id="e1708-117">Kui soovitate kulumit sel moel, arvutatakse põhivarade väärtusmudelite kulum.</span><span class="sxs-lookup"><span data-stu-id="e1708-117">When you propose depreciation in this way, depreciation is calculated for value models for fixed assets.</span></span>  

4. <span data-ttu-id="e1708-118">Valige käsk **Loo tööleht**.</span><span class="sxs-lookup"><span data-stu-id="e1708-118">Select **Create journal**.</span></span>

## <a name="review-depreciation-entries"></a><span data-ttu-id="e1708-119">Kulumiraamatu kannete ülevaade</span><span class="sxs-lookup"><span data-stu-id="e1708-119">Review depreciation entries</span></span>
1. <span data-ttu-id="e1708-120">Avage navigeerimispaneelil **Moodulid > Põhivarad > Töölehe kanded > Põhivarade tööleht**.</span><span class="sxs-lookup"><span data-stu-id="e1708-120">In the navigation pane, go to **Modules > Fixed assets > Journal entries > Fixed assets journal**.</span></span>
2. <span data-ttu-id="e1708-121">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e1708-121">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="e1708-122">Valige **Read**.</span><span class="sxs-lookup"><span data-stu-id="e1708-122">Select **Lines**.</span></span>
4. <span data-ttu-id="e1708-123">Valige **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="e1708-123">Select **Post**.</span></span>

