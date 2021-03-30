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
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: db601be192b57fbec220193d3c9fde1a4f50c085
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213504"
---
# <a name="split-a-fixed-asset"></a><span data-ttu-id="773e3-103">Põhivara tükeldamine</span><span class="sxs-lookup"><span data-stu-id="773e3-103">Split a fixed asset</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="773e3-104">See teema selgitab, kuidas tükeldada ühe vararaamatu protsenti uude vararaamatusse.</span><span class="sxs-lookup"><span data-stu-id="773e3-104">This topic explains how to split a percentage of one asset book to a new asset book.</span></span> <span data-ttu-id="773e3-105">See kasutab raamatupidaja rolli ja USMF-i demoandmeid.</span><span class="sxs-lookup"><span data-stu-id="773e3-105">It uses the Accountant role and USMF demo data.</span></span>

## <a name="create-a-new-fixed-asset"></a><span data-ttu-id="773e3-106">Uue põhivara loomine</span><span class="sxs-lookup"><span data-stu-id="773e3-106">Create a new fixed asset</span></span>

1. <span data-ttu-id="773e3-107">Avage navigeerimispaanil jaotis **Moodulid \> Põhivarad \> Põhivarad \> Põhivarad**.</span><span class="sxs-lookup"><span data-stu-id="773e3-107">In the navigation pane, go to **Modules \> Fixed assets \> Fixed assets \> Fixed assets**.</span></span>
2. <span data-ttu-id="773e3-108">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="773e3-108">Select **New**.</span></span>
3. <span data-ttu-id="773e3-109">Väljale **Põhivara grupp** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="773e3-109">In the **Fixed asset group** field, enter or select a value.</span></span> <span data-ttu-id="773e3-110">Märkige põhivara kood hilisemaks tükeldamisprotsessis kasutamiseks üles.</span><span class="sxs-lookup"><span data-stu-id="773e3-110">Note the fixed asset number to use in the split process later.</span></span>
4. <span data-ttu-id="773e3-111">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="773e3-111">In the **Name** field, enter a value.</span></span>
5. <span data-ttu-id="773e3-112">Sulgege vorm.</span><span class="sxs-lookup"><span data-stu-id="773e3-112">Close the form.</span></span>

## <a name="split-a-fixed-asset"></a><span data-ttu-id="773e3-113">Põhivara tükeldamine</span><span class="sxs-lookup"><span data-stu-id="773e3-113">Split a fixed asset</span></span>

<span data-ttu-id="773e3-114">Enne täielikult amortiseeritud vara tükeldamist tuleb vara raamatu olek **Suletud** muuta käsitsi olekuks **Avatud**.</span><span class="sxs-lookup"><span data-stu-id="773e3-114">Before a fully depreciated asset is split, the asset book status should be manually changed from **Closed** to **Open**.</span></span> <span data-ttu-id="773e3-115">See etapp on nõutav, kuna raamatu olek peab olema **Avatud**, kui peate sisestama varale kandeid (nt likvideerimismüük).</span><span class="sxs-lookup"><span data-stu-id="773e3-115">This step is required because the book status has to be **Open** if you must post transactions for the asset (for example, for a disposal sale).</span></span> <span data-ttu-id="773e3-116">Samuti peate sisse lülitama parameetri **Luba ühe kande raames mitut kannet** vahekaardil **Üldine** lehel **Pearaamatu parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="773e3-116">You must also turn on the **Allow multiple transactions within one voucher** parameter on the **General** tab of the **General ledger parameters** page.</span></span> <span data-ttu-id="773e3-117">Pärast vararaamatu oleku muutmist ja mitme kande lubamist ühe kande raames tehke vara tükeldamiseks järgmised toimingud.</span><span class="sxs-lookup"><span data-stu-id="773e3-117">After the asset book status is changed and multiple transactions within one voucher have been allowed, complete the following steps to split the asset.</span></span>

1. <span data-ttu-id="773e3-118">Leidke loendist tükeldatav põhivara ja valige selle link.</span><span class="sxs-lookup"><span data-stu-id="773e3-118">In the list, find and select the link of the fixed asset to split.</span></span>
2. <span data-ttu-id="773e3-119">Valige **Raamatud**.</span><span class="sxs-lookup"><span data-stu-id="773e3-119">Select **Books**.</span></span> <span data-ttu-id="773e3-120">Valige uuele varale tükeldatav raamat.</span><span class="sxs-lookup"><span data-stu-id="773e3-120">Select the book to split to the new asset.</span></span>
3. <span data-ttu-id="773e3-121">Valige **Funktsioonid**.</span><span class="sxs-lookup"><span data-stu-id="773e3-121">Select **Functions**.</span></span>
4. <span data-ttu-id="773e3-122">Valige **Tükelda põhivara**.</span><span class="sxs-lookup"><span data-stu-id="773e3-122">Select **Split fixed asset**.</span></span>
5. <span data-ttu-id="773e3-123">Sisestage väärtus väljale **Põhivarasse** või valige sellelt väljalt.</span><span class="sxs-lookup"><span data-stu-id="773e3-123">In the **To fixed asset** field, enter or select a value.</span></span>
6. <span data-ttu-id="773e3-124">Klõpsake väljal **Raamatusse** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="773e3-124">In the **To book** field, select the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="773e3-125">Sisestage kuupäev väljale **Kande kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="773e3-125">In the **Transaction date** field, enter a date.</span></span>
8. <span data-ttu-id="773e3-126">Sisestage number väljale **Protsent**.</span><span class="sxs-lookup"><span data-stu-id="773e3-126">In the **Percent** field, enter a number.</span></span>
9. <span data-ttu-id="773e3-127">Valige või sisestage väärtus väljal **Töölehe nimi**.</span><span class="sxs-lookup"><span data-stu-id="773e3-127">In the **Journal name** field, enter or select a value.</span></span>
10. <span data-ttu-id="773e3-128">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="773e3-128">Select **OK**.</span></span>

## <a name="post-the-journal-transaction"></a><span data-ttu-id="773e3-129">Töölehekande sisestamine</span><span class="sxs-lookup"><span data-stu-id="773e3-129">Post the journal transaction</span></span>

1. <span data-ttu-id="773e3-130">Avage navigeerimispaanil jaotis **Moodulid \> Põhivarad \> Töölehe kanded \> Põhivarade tööleht**.</span><span class="sxs-lookup"><span data-stu-id="773e3-130">In the navigation pane, go to **Modules \> Fixed assets \> Journal entries \> Fixed assets journal**.</span></span>
2. <span data-ttu-id="773e3-131">Valige loendist tükeldamise protsessis loodud tööleht.</span><span class="sxs-lookup"><span data-stu-id="773e3-131">In the list, select the journal created with the split process.</span></span>
3. <span data-ttu-id="773e3-132">Valige **Read**.</span><span class="sxs-lookup"><span data-stu-id="773e3-132">Select **Lines**.</span></span>

    - <span data-ttu-id="773e3-133">Kontrollige loodud töölehe ridu.</span><span class="sxs-lookup"><span data-stu-id="773e3-133">Verify the journal lines created.</span></span>
    - <span data-ttu-id="773e3-134">Soetamise korrigeerimiskanne luuakse algse vara puhul väärtuse vähendamiseks tükeldamisprotsessis määratud protsendi võrra.</span><span class="sxs-lookup"><span data-stu-id="773e3-134">An Acquisition adjustment transaction is created for the original asset to decrease the value by the percentage specified during the split process.</span></span>
    - <span data-ttu-id="773e3-135">Soetamiskanne luuakse uue vara puhul samas summas.</span><span class="sxs-lookup"><span data-stu-id="773e3-135">An Acquisition transaction is created for the new asset for the same amount.</span></span>

4. <span data-ttu-id="773e3-136">Valige **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="773e3-136">Select **Post**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]