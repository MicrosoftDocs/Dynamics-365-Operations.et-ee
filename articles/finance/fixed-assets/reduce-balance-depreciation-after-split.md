---
title: Väheneva jääkväärtuse kuluarvestusmeetod pärast tükeldamist
description: Selles teemas kirjeldatakse meetodit, mida kasutatakse põhivarades kulumi arvutamiseks pärast seda, kui vara tükeldatakse väheneva jääkväärtuse meetodil.
author: moaamer
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-17
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 056808b7d4d490bc4d60aa058108d159c1d4867c
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5826247"
---
# <a name="reduce-balance-depreciation-after-a-split"></a><span data-ttu-id="f58db-103">Väheneva jääkväärtuse kuluarvestusmeetod pärast tükeldamist</span><span class="sxs-lookup"><span data-stu-id="f58db-103">Reduce balance depreciation after a split</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f58db-104">Selles teemas kirjeldatakse meetodit, mida kasutatakse põhivarades kulumi arvutamiseks pärast seda, kui vara tükeldatakse teiseks varaks väheneva jääkväärtuse meetodil.</span><span class="sxs-lookup"><span data-stu-id="f58db-104">This topic describes the method that is used in Fixed assets to calculate depreciation after an asset is split to another asset by using the reduce balance method.</span></span> <span data-ttu-id="f58db-105">Vararaamatus konfigureeritud kulumiaastaks on finantsaasta.</span><span class="sxs-lookup"><span data-stu-id="f58db-105">The depreciation year that is configured in the asset book is the fiscal year.</span></span> <span data-ttu-id="f58db-106">Lisateavet vt teemast [Saldo kulumi vähendamine](reduce-balance-depreciation.md) ja [Põhivara tükeldamine](tasks/split-fixed-asset.md).</span><span class="sxs-lookup"><span data-stu-id="f58db-106">For more information, see [Reduce balance depreciation](reduce-balance-depreciation.md) and [Split a fixed asset](tasks/split-fixed-asset.md).</span></span>

<span data-ttu-id="f58db-107">Kui tükeldate põhivara eelarveperioodi jooksul, mis on vara soetamise perioodist hilisem kui periood, arvestatakse vähendatud saldoga kulumit eelmise aasta vara raamatupidamisliku jääkväärtuse (NBV) alusel.</span><span class="sxs-lookup"><span data-stu-id="f58db-107">If you split a fixed asset during a fiscal period that is later than the period when the asset was acquired, the reduced balance depreciation will account for the asset's net book value (NBV) for the previous year.</span></span> <span data-ttu-id="f58db-108">See arvestab ka soetamise ja kulumi korrigeerimise kandeid, mis loodi vara tükeldamise kandest.</span><span class="sxs-lookup"><span data-stu-id="f58db-108">It will also account for the acquisition and depreciation adjustment transactions that were generated from the transaction that split the asset.</span></span> <span data-ttu-id="f58db-109">Selline käitumine eeldab, et vara soetati ühel finantsaastal ja tükeldatakse hilisemal finantsaastal.</span><span class="sxs-lookup"><span data-stu-id="f58db-109">This behavior assumes that the asset was acquired in one fiscal year and split in a later fiscal year.</span></span> <span data-ttu-id="f58db-110">Summa, mis tuleb amortiseerida algse vara puhul pärast tükeldamist peegeldab vara raamatupidamislikku jääkväärtust enne vara tükeldamist ja tükeldamiseks sisestatud soetamise ja kulumi korrigeerimise kannet.</span><span class="sxs-lookup"><span data-stu-id="f58db-110">The amount that must be depreciated for the original asset after the split reflects the asset's NBV before the asset was split, and the acquisition and depreciation adjustment transaction that was posted for the split.</span></span>

<span data-ttu-id="f58db-111">Näiteks kehtivad järgmised tingimused.</span><span class="sxs-lookup"><span data-stu-id="f58db-111">For example, the following conditions are in effect:</span></span>

- <span data-ttu-id="f58db-112">Finantsperiood on 30. juuni kuni 1. juuli.</span><span class="sxs-lookup"><span data-stu-id="f58db-112">The fiscal period is from June 30 to July 1.</span></span>
- <span data-ttu-id="f58db-113">Väheneva saldo protsent on 18 protsenti ja vara soetatakse 2019. aasta juunis soetamismaksumusega 10 000 USD.</span><span class="sxs-lookup"><span data-stu-id="f58db-113">The reducing balance percentage is 18 percent, and an asset is acquired in June 2019 at an acquisition price of $10,000.</span></span>
- <span data-ttu-id="f58db-114">Esimese finantsaasta kulum võrdub 18 000 USD-ga, igakuine kulum võrdub 150 USD-ga ja vara amortiseeritakse seejärel summas 738.75 USD kuni novembrini 2019.</span><span class="sxs-lookup"><span data-stu-id="f58db-114">The depreciation of the first fiscal year equals $18,000, the monthly depreciation equals $150, and the asset is then depreciated until November 2019, in the amount of $738.75.</span></span>
- <span data-ttu-id="f58db-115">Novembris 2019 tükeldatakse 80 protsenti varast teiseks põhivaraks.</span><span class="sxs-lookup"><span data-stu-id="f58db-115">In November 2019, 80 percent of the asset is split to another fixed asset.</span></span>

<span data-ttu-id="f58db-116">[![Väheneva jääkväärtuse kuluarvestusmeetod pärast tükeldamist](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)</span><span class="sxs-lookup"><span data-stu-id="f58db-116">[![Reduce balance depreciation after a split](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)</span></span>

<span data-ttu-id="f58db-117">Algse vara kulumi summa on $1822.25.</span><span class="sxs-lookup"><span data-stu-id="f58db-117">The amount to depreciate for the original asset is $1,822.25.</span></span> <span data-ttu-id="f58db-118">See summa võrdub raamatupidamisliku jääkväärtusega enne tükeldatud kande sisestamist (9111.25 USD), pluss soetuse korrigeerimine, mis luuakse tükeldatud kande (8000 USD) sisestamisel, pluss kulumi korrigeerimine, mis luuakse tükeldatud kande (711 USD) jooksul.</span><span class="sxs-lookup"><span data-stu-id="f58db-118">This amount equals the NBV before the split transaction is posted ($9,111.25), plus the acquisition adjustment that is generated during posting of the split transaction (-$8,000), plus the depreciation adjustment that is generated during the split transaction ($711).</span></span> <span data-ttu-id="f58db-119">Seetõttu on teise aasta kulum (1822.25 × 18 protsenti) ÷ 12 = 27.33 USD.</span><span class="sxs-lookup"><span data-stu-id="f58db-119">Therefore, the depreciation for the second year is (1,822.25 × 18 percent) ÷ 12 = $27.33.</span></span>

<span data-ttu-id="f58db-120">Uue põhivara kulumiarvestuse summa esimesel aastal on (8000 × 18 protsenti) ÷ 12 = 120 USD.</span><span class="sxs-lookup"><span data-stu-id="f58db-120">The amount to depreciate for the new fixed asset in the first year is (8,000 × 18 percent) ÷ 12 = $120.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]