---
title: Põhivarade praagi likvideerimine
description: Selles teemas kirjeldatakse praagina likvideeritud põhivara kannete likvideerimise protsessi.
author: moaamer
ms.date: 08/14/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-08-14
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 413847d350ca6b2bdd6153a598ea5b3f34a33818
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826271"
---
# <a name="dispose-of-a-fixed-asset-as-scrap"></a><span data-ttu-id="fc89c-103">Põhivarade praagi likvideerimine</span><span class="sxs-lookup"><span data-stu-id="fc89c-103">Dispose of a fixed asset as scrap</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fc89c-104">Selles teemas kirjeldatakse praagina likvideeritud põhivara kannete likvideerimise protsessi.</span><span class="sxs-lookup"><span data-stu-id="fc89c-104">The topic describes the process of eliminating transactions for a fixed asset that was disposed of as scrap.</span></span> <span data-ttu-id="fc89c-105">Kandetüübid, mida saab kõrvaldada, on ka vara soetamise ja kogunenud kulumi kanded ja muud põhivara kanded.</span><span class="sxs-lookup"><span data-stu-id="fc89c-105">The transaction types that can be eliminated include an asset's acquisition and accumulated depreciation transactions and other fixed asset transactions.</span></span> <span data-ttu-id="fc89c-106">Nende kannete likvideerimine mõjutab bilansikontosid, nagu soetamise korrigeerimine, kulumi korrigeerimine, ümberhindamise, üleshindamise ja allahindamise kontod.</span><span class="sxs-lookup"><span data-stu-id="fc89c-106">Elimination of these transactions affects balance sheet accounts, such as acquisition adjustment, depreciation adjustment, revaluation, write-up, and write-down accounts.</span></span>

| <span data-ttu-id="fc89c-107">Kanne</span><span class="sxs-lookup"><span data-stu-id="fc89c-107">Transaction</span></span>                                         | <span data-ttu-id="fc89c-108">Deebet (Dr.)</span><span class="sxs-lookup"><span data-stu-id="fc89c-108">Debit (Dr.)</span></span> | <span data-ttu-id="fc89c-109">Krediit (Cr.)</span><span class="sxs-lookup"><span data-stu-id="fc89c-109">Credit (Cr.)</span></span> |
|-----------------------------------------------------|-------------|--------------|
| <span data-ttu-id="fc89c-110">Dr. Kogunenud kulum</span><span class="sxs-lookup"><span data-stu-id="fc89c-110">Dr. Accumulated depreciation</span></span>                        | <span data-ttu-id="fc89c-111">X</span><span class="sxs-lookup"><span data-stu-id="fc89c-111">X</span></span>           |              |
| <span data-ttu-id="fc89c-112">Cr. Põhivara kasum/kahjum</span><span class="sxs-lookup"><span data-stu-id="fc89c-112">Cr. Fixed assets gain/loss</span></span>                          |             | <span data-ttu-id="fc89c-113">X</span><span class="sxs-lookup"><span data-stu-id="fc89c-113">X</span></span>            |
| <span data-ttu-id="fc89c-114">Dr. Põhivara kasum/kahjum</span><span class="sxs-lookup"><span data-stu-id="fc89c-114">Dr. Fixed assets gain/loss</span></span>                          | <span data-ttu-id="fc89c-115">X</span><span class="sxs-lookup"><span data-stu-id="fc89c-115">X</span></span>           |              |
| <span data-ttu-id="fc89c-116">Cr. Põhivara soetamise kontod</span><span class="sxs-lookup"><span data-stu-id="fc89c-116">Cr. Fixed asset acquisition account</span></span>                 |             | <span data-ttu-id="fc89c-117">X</span><span class="sxs-lookup"><span data-stu-id="fc89c-117">X</span></span>            |
| <span data-ttu-id="fc89c-118">Dr. Põhivara kasum/kahjum (raamatupidamislik jääkväärtus \[NBV)\]</span><span class="sxs-lookup"><span data-stu-id="fc89c-118">Dr. Fixed assets gain/loss (net book value \[NBV\])</span></span> | <span data-ttu-id="fc89c-119">X</span><span class="sxs-lookup"><span data-stu-id="fc89c-119">X</span></span>           |              |
| <span data-ttu-id="fc89c-120">Cr. Põhivara kasum/kahjum (NBV)</span><span class="sxs-lookup"><span data-stu-id="fc89c-120">Cr. Fixed assets gain/loss (NBV)</span></span>                    |             | <span data-ttu-id="fc89c-121">X</span><span class="sxs-lookup"><span data-stu-id="fc89c-121">X</span></span>            |

> [!NOTE]
> <span data-ttu-id="fc89c-122">Soovitame teil teha tihedat koostööd ettevõtte finantsjuhi (CFO) või kontrollijaga, et tuvastada õiged kontod, mida tuleks kasutada iga kandetüübi puhul, ja samuti kinnitada, et likvideerimisprotsess ja selle loodud kanded värskendatakse nendel kontodel õigesti.</span><span class="sxs-lookup"><span data-stu-id="fc89c-122">We recommend that you work closely with your company's chief financial officer (CFO) or controller to identify the correct accounts that should be used for each transaction type, and also to verify that the disposal process and the transactions that it generates update those accounts correctly.</span></span>

<span data-ttu-id="fc89c-123">Enne põhivara praagina likvideerimist peate looma pearaamatukontod, mis on seotud vara soetamise väärtusega, jooksva aasta kulumiga, eelmiste aastate kulumiga ja vara NBV-ga.</span><span class="sxs-lookup"><span data-stu-id="fc89c-123">Before you dispose of a fixed asset as scrap, you must create ledger accounts that are associated with the asset's acquisition value, depreciation for the current year, depreciation for previous years, and the asset's NBV.</span></span> <span data-ttu-id="fc89c-124">Põhivara kandetüübid on loetletud lehel **Põhivarade sisestusreeglid**.</span><span class="sxs-lookup"><span data-stu-id="fc89c-124">The fixed asset transaction types are listed on the **Fixed assets posting profile** page.</span></span> <span data-ttu-id="fc89c-125">Valige **Põhivarad \> Seadistus \> Põhivarade sisestusreeglid** ja seejärel valige kiirkaardi **Likvideerimine** väljal ruudusliku kohal olev valik **Praak**.</span><span class="sxs-lookup"><span data-stu-id="fc89c-125">Go to **Fixed assets \> Setup \> Fixed asset posting profiles**, and then, on the **Disposal** FastTab, select **Scrap** in the field above the grid.</span></span> <span data-ttu-id="fc89c-126">Järgneval joonisel kujutatakse põhivara kanndetüüpide loendit lehel **Põhivara sisestusreeglid**.</span><span class="sxs-lookup"><span data-stu-id="fc89c-126">The following illustration shows the list of fixed asset transaction types on the **Fixed asset posting profiles** page.</span></span>


<span data-ttu-id="fc89c-127">[![Vara likvideerimine praagina, joonis 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)</span><span class="sxs-lookup"><span data-stu-id="fc89c-127">[![Disposing of an asset as scap, Fig. 1](./media/Fixed_asset_Disposal_scrap_scenario_1.png)](./media/Fixed_asset_Disposal_scrap_scenario_1.png)</span></span>

<span data-ttu-id="fc89c-128">Järgmise näite puhul soetati põhivara 1. jaanuaril 2018 ja see kantakse maha 31. märtsil 2019.</span><span class="sxs-lookup"><span data-stu-id="fc89c-128">For the following example, a fixed asset was acquired on January 1, 2018, and it will be scrapped on March 31, 2019.</span></span>

- <span data-ttu-id="fc89c-129">**Soetamise hind:** 24 000,00 USA dollarit (USD)</span><span class="sxs-lookup"><span data-stu-id="fc89c-129">**Acquisition price:** 24,000.00 US dollars (USD)</span></span>
- <span data-ttu-id="fc89c-130">**Tööiga:** Kaks aastat</span><span class="sxs-lookup"><span data-stu-id="fc89c-130">**Service life:** Two years</span></span>
- <span data-ttu-id="fc89c-131">**Kulumiarvestusviis:** Lineaarne tööiga</span><span class="sxs-lookup"><span data-stu-id="fc89c-131">**Depreciation method:** Straight line service life</span></span>
- <span data-ttu-id="fc89c-132">**Kulumi summa:** 1000,00 USD kuus</span><span class="sxs-lookup"><span data-stu-id="fc89c-132">**Depreciation amount:** 1,000.00 USD per month</span></span>

<span data-ttu-id="fc89c-133">Põhivara NVB arvutatakse järgmist valemit kasutades.</span><span class="sxs-lookup"><span data-stu-id="fc89c-133">The NBV of a fixed asset is calculated by using the following formula:</span></span>

<span data-ttu-id="fc89c-134">Raamatupidamislik jääkväärtus = soetamise hind - kulum</span><span class="sxs-lookup"><span data-stu-id="fc89c-134">Net book value = Acquisition price – Depreciation</span></span>

<span data-ttu-id="fc89c-135">Selles näites soetati põhivara ja amortiseeriti 15 kuuks, 2018. aasta jaanuarist kuni 2019. aasta märtsini.</span><span class="sxs-lookup"><span data-stu-id="fc89c-135">In this example, the fixed asset was acquired and was depreciated for 15 months, from January 2018 through March 2019.</span></span> <span data-ttu-id="fc89c-136">Seetõttu on vara NBV 9000,00 USD (24 000,00 USD – 15 000,00 USD).</span><span class="sxs-lookup"><span data-stu-id="fc89c-136">Therefore, the asset's NBV is 9,000.00 USD (24,000.00 USD – 15,000.00 USD).</span></span>

<span data-ttu-id="fc89c-137">[![Põhivara kulumiarvestuse näide](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)</span><span class="sxs-lookup"><span data-stu-id="fc89c-137">[![Fixed asset depreciation example](./media/Fixed_asset_Disposal_scrap_scenario_2.png)](./media/Fixed_asset_Disposal_scrap_scenario_2.png)</span></span>


<span data-ttu-id="fc89c-138">Likvideerimise töölehe loomiseks avage **Põhivarad \> Töölehe kanded \> Põhivarade tööleht** ja seejärel valige Tegevuspaanil **Read**.</span><span class="sxs-lookup"><span data-stu-id="fc89c-138">To create a disposal journal, go to **Fixed assets \> Journal entries \> Fixed assets journal**, and then, on the Action Pane, select **Lines**.</span></span> <span data-ttu-id="fc89c-139">Valige **Likvideerimine – praak** ja seejärel valige põhivara ID.</span><span class="sxs-lookup"><span data-stu-id="fc89c-139">Select **Disposal – scrap**, and then select a fixed asset ID.</span></span> <span data-ttu-id="fc89c-140">Vara täielikuks likvideerimiseks ärge sisestage väärtust väljale **Deebet** ega **Kreedit**.</span><span class="sxs-lookup"><span data-stu-id="fc89c-140">To fully dispose of the asset, don't enter a value in either the **Debit** field or the **Credit** field.</span></span>

<span data-ttu-id="fc89c-141">[![Põhivarade tööleht](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)</span><span class="sxs-lookup"><span data-stu-id="fc89c-141">[![Fixed assets journal](./media/Fixed_asset_Disposal_scrap_scenario_3.png)](./media/Fixed_asset_Disposal_scrap_scenario_3.png)</span></span>

<span data-ttu-id="fc89c-142">Põhivara praagina likvideerimise kanne muudab põhivara raamatu välja väärtusi järgmistel viisidel.</span><span class="sxs-lookup"><span data-stu-id="fc89c-142">The fixed asset disposal scrap transaction changes the field values for the fixed asset book in the following ways:</span></span>

- <span data-ttu-id="fc89c-143">Jaotises **Saldo** muudetakse välja **Olek** väärtuseks **Praagitud**.</span><span class="sxs-lookup"><span data-stu-id="fc89c-143">In the **Balance** section, the **Status** field is updated to **Scrapped**.</span></span>
- <span data-ttu-id="fc89c-144">Jaotises **Väljastamine** muudetakse välja **Likvideerimise kuupäev** väärtuseks kuupäev, millal vara praagiti.</span><span class="sxs-lookup"><span data-stu-id="fc89c-144">In the **Issue** section, the **Disposal date** field is set to the date when the asset was scrapped.</span></span>

<span data-ttu-id="fc89c-145">[![Põhivarade töölehe üksikasjad](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)</span><span class="sxs-lookup"><span data-stu-id="fc89c-145">[![Fixed assets journal detail](./media/Fixed_asset_Disposal_scrap_scenario_4.png)](./media/Fixed_asset_Disposal_scrap_scenario_4.png)</span></span>

<span data-ttu-id="fc89c-146">Järgmisel joonisel näidatakse põhivara saldot.</span><span class="sxs-lookup"><span data-stu-id="fc89c-146">The following illustration shows the fixed asset balance.</span></span>

<span data-ttu-id="fc89c-147">[![Põhivara saldo](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)</span><span class="sxs-lookup"><span data-stu-id="fc89c-147">[![Fixed asset balance](./media/Fixed_asset_Disposal_scrap_scenario_5.png)](./media/Fixed_asset_Disposal_scrap_scenario_5.png)</span></span>

<span data-ttu-id="fc89c-148">Järgmisel joonisel näidatakse postitatavat kupongi.</span><span class="sxs-lookup"><span data-stu-id="fc89c-148">The following illustration shows the voucher that is posted.</span></span>

<span data-ttu-id="fc89c-149">[![Arvestuslik jääkväärtus](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)</span><span class="sxs-lookup"><span data-stu-id="fc89c-149">[![Net book value](./media/Fixed_asset_Disposal_scrap_scenario_6.png)](./media/Fixed_asset_Disposal_scrap_scenario_6.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]