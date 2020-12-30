---
title: Rendiraamatute seadistamine
description: Selles teemas kirjeldatakse rendiraamatutes hoitavat teavet. Rendiraamatud sisaldavad arvestuspõhimõtteid, mis määravad, kuidas rendilepingut süsteemis arvestatakse.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations, Retail
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 28518341544327f1983e563b719b0f455b6e1c43
ms.sourcegitcommit: aeee39c01d3f93a6dfcf2013965fa975a740596a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/28/2020
ms.locfileid: "4442564"
---
# <a name="set-up-lease-books"></a><span data-ttu-id="2f59e-104">Rendiraamatute seadistamine</span><span class="sxs-lookup"><span data-stu-id="2f59e-104">Set up lease books</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2f59e-105">Rendiraamatud sisaldavad arvestuspõhimõtteid, mis määravad, kuidas rendilepingut süsteemis arvestatakse.</span><span class="sxs-lookup"><span data-stu-id="2f59e-105">Lease books contain the accounting policies that determine how a lease is accounted for in the system.</span></span> <span data-ttu-id="2f59e-106">Lisaks sularahapõhisele raamatupidamisele toetab vara rentimine järgmiseid standardeid.</span><span class="sxs-lookup"><span data-stu-id="2f59e-106">In addition to cash basis accounting, Asset leasing supports the following standards:</span></span>

- <span data-ttu-id="2f59e-107">Üldtunnustatud raamatupidamispõhimõtted Ameerika Ühendriikides (USA RAAMATUPIDAMISTAVA)</span><span class="sxs-lookup"><span data-stu-id="2f59e-107">Generally Accepted Accounting Principles in the United States (US GAAP)</span></span>
- <span data-ttu-id="2f59e-108">Raamatupidamisstandardite kodeerimise teema 842 (ASC 842)</span><span class="sxs-lookup"><span data-stu-id="2f59e-108">Accounting Standards Codification Topic 842 (ASC 842)</span></span>
- <span data-ttu-id="2f59e-109">ASC 840</span><span class="sxs-lookup"><span data-stu-id="2f59e-109">ASC 840</span></span>
- <span data-ttu-id="2f59e-110">Rahvusvaheline finantsaruandluse Standard 16 (IFRS 16)</span><span class="sxs-lookup"><span data-stu-id="2f59e-110">International Financial Reporting Standard 16 (IFRS 16)</span></span>
- <span data-ttu-id="2f59e-111">Rahvusvaheline raamatupidamisstandard 17 (IAS 17)</span><span class="sxs-lookup"><span data-stu-id="2f59e-111">International Accounting Standard 17 (IAS 17)</span></span>

<span data-ttu-id="2f59e-112">Rendiraamatu loomiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="2f59e-112">To create a lease book, follow these steps.</span></span>

1. <span data-ttu-id="2f59e-113">Avage **Vara rentimine \> Seadistus \> Rendiraamatud**.</span><span class="sxs-lookup"><span data-stu-id="2f59e-113">Go to **Asset leasing \> Setup \> Lease books**.</span></span>
2. <span data-ttu-id="2f59e-114">Raamatu lisamiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="2f59e-114">Select **New** to add a book.</span></span>
3. <span data-ttu-id="2f59e-115">Seadistage järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="2f59e-115">Set the following fields.</span></span>

    | <span data-ttu-id="2f59e-116">Nimi</span><span class="sxs-lookup"><span data-stu-id="2f59e-116">Name</span></span>                                     | <span data-ttu-id="2f59e-117">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="2f59e-117">Description</span></span> |
    |------------------------------------------|-------------|
    | <span data-ttu-id="2f59e-118">Sisestamiskiht</span><span class="sxs-lookup"><span data-stu-id="2f59e-118">Posting layer</span></span>                            | <span data-ttu-id="2f59e-119">Valige kasutatav sisestamiskiht.</span><span class="sxs-lookup"><span data-stu-id="2f59e-119">Select the posting layer to use.</span></span> <span data-ttu-id="2f59e-120">Iga rendilepinguga seotud raamat seadistatakse kindla sisestuskihi jaoks.</span><span class="sxs-lookup"><span data-stu-id="2f59e-120">Each book that is attached to a lease is set up for a specific posting layer.</span></span> <span data-ttu-id="2f59e-121">Igal sisestuskihil on erinevad sisestamise eesmärgid.</span><span class="sxs-lookup"><span data-stu-id="2f59e-121">Each posting layer has different posting purposes.</span></span> |
    | <span data-ttu-id="2f59e-122">Rendi tüüp</span><span class="sxs-lookup"><span data-stu-id="2f59e-122">Lease type</span></span>                               | <span data-ttu-id="2f59e-123">Valige, kas rendileping tuleb klassifitseerida automaatselt või kas see peaks olema eelmääratletud kui kapitali- või kasutusrent.</span><span class="sxs-lookup"><span data-stu-id="2f59e-123">Select whether the lease should be classified automatically, or whether it should be predefined as a finance or operating lease.</span></span> |
    | <span data-ttu-id="2f59e-124">Raamatupidamisraamistik</span><span class="sxs-lookup"><span data-stu-id="2f59e-124">Accounting framework</span></span>                     | <span data-ttu-id="2f59e-125">Valige raamatuga seotud raamistik.</span><span class="sxs-lookup"><span data-stu-id="2f59e-125">Select the framework that is associated with the book.</span></span> |
    | <span data-ttu-id="2f59e-126">Rendiperioodi/kasuliku tööea häälestus</span><span class="sxs-lookup"><span data-stu-id="2f59e-126">Lease term/Useful life Set Up</span></span>          | <span data-ttu-id="2f59e-127">Süsteem liigitab rendi kapitalirendiks, kui rendi tüüp on seadistatud **Automaatseks** ja kui rendiperiood vara kasuliku tööea jooksul on suurem kui siin väljal määratletud protsent või sellega võrdne.</span><span class="sxs-lookup"><span data-stu-id="2f59e-127">The system will classify the lease as a finance lease if the lease type is set to **Automatic**, and if the lease term over useful life of the asset is greater than or equal to the percentage entered in this field.</span></span>  |
    | <span data-ttu-id="2f59e-128">Praeguse väärtuse / vara õiglase väärtuse häälestamine</span><span class="sxs-lookup"><span data-stu-id="2f59e-128">Present value / Asset fair value setup</span></span>   | <span data-ttu-id="2f59e-129">Sisestage täisarv, et määratleda lävi, mis määrab rendi tüübi.</span><span class="sxs-lookup"><span data-stu-id="2f59e-129">Enter a whole number to define the threshold that will determine the lease type.</span></span> <span data-ttu-id="2f59e-130">Kui tulevaste minimaalsete rendimaksete praegune väärtus on suurem kui kasutaja määratud väärtus raamatu seadistusest ja kui raamatu rendi klassifikatsioon on seadistatud automaatseks, klassifitseerib süsteem rendi kapitalirendina.</span><span class="sxs-lookup"><span data-stu-id="2f59e-130">If the present value of future minimum lease payments is more than the user-defined value from the book setup, and if the book's lease classification is set to automatic, the system will classify the lease as a finance lease.</span></span> |
    | <span data-ttu-id="2f59e-131">Lühiajaline künnis</span><span class="sxs-lookup"><span data-stu-id="2f59e-131">Short-term threshold</span></span>                     | <span data-ttu-id="2f59e-132">Sisestage kuude arv lühiajaliste rendilepingute lävena kasutamiseks.</span><span class="sxs-lookup"><span data-stu-id="2f59e-132">Enter the number of months to use as a threshold for short-term leases.</span></span> <span data-ttu-id="2f59e-133">Kui rendileping on siin sisestatud kuude arvust lühem või sellega võrdne, klassifitseerib süsteem rendi lühiajalise rendina ja rakendatakse edasilükatud rendi käsitlust.</span><span class="sxs-lookup"><span data-stu-id="2f59e-133">If the lease term is less than or equal to the number of months that you enter here, the system will classify the lease as a short-term lease, and the deferred rent treatment will be applied.</span></span> |
    | <span data-ttu-id="2f59e-134">Väikese väärtuse künnis</span><span class="sxs-lookup"><span data-stu-id="2f59e-134">Low value threshold</span></span>                      | <span data-ttu-id="2f59e-135">Sisestage summa, mida kasutatakse väikese väärtusega rendilepingute lävena.</span><span class="sxs-lookup"><span data-stu-id="2f59e-135">Enter an amount to use as a threshold for low-value leases.</span></span> <span data-ttu-id="2f59e-136">Kui vara õiglane väärtus on väiksem või võrdne siia sisestatud väärtusega, klassifitseerib süsteem rendi väikese väärtusega rendina ja rakendatakse edasilükatud rendi käsitlust.</span><span class="sxs-lookup"><span data-stu-id="2f59e-136">If the fair value of the asset is less than or equal or the value that you enter here, the system will classify the lease as a low-value lease, and the deferred rent treatment will be applied.</span></span> |
    | <span data-ttu-id="2f59e-137">Tasumine hankijale</span><span class="sxs-lookup"><span data-stu-id="2f59e-137">Pay to vendor</span></span>                            | <span data-ttu-id="2f59e-138">Seadke see suvand väärtusele **Jah**, et lubada rendimaksete sisestamist arvena igale rendilepingul määratud hankija kontole.</span><span class="sxs-lookup"><span data-stu-id="2f59e-138">Set this option to **Yes** to allow lease payments to be posted, as an invoice, to the vendor account that is specified on each lease.</span></span> <span data-ttu-id="2f59e-139">Kui rendimakse sisestatakse, krediteeritakse hankija kontot.</span><span class="sxs-lookup"><span data-stu-id="2f59e-139">When a lease payment is posted, the vendor account will be credited.</span></span> <span data-ttu-id="2f59e-140">Kui see valik on seadistatud väärtusele **Ei**, krediteeritakse selle asemel konto, mis on määratud **Rendimakse** sisestustüübile lehel **Rendi sisestamise parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="2f59e-140">If this option is set to **No**, the account that is specified for the **Lease payment** posting type on the **Lease posting parameters** page will be credited instead.</span></span> |
