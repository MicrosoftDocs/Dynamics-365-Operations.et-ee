---
title: Finantsdimensioonikomplektid
description: See teema kirjeldab finantsdimensioonide komplekte ja annab näpunäiteid nende kasutamise optimeerimiseks.
author: yukonpeegs
manager: AnnBe
ms.date: 03/23/2021
ms.topic: article
ems.prod: ''
ms.technology: ''
ms.search.form: DimensionFocus, LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 25871
ms.search.region: Global
ms.author: epegors
ms.search.validFrom: 2021-03-23
ms.dyn365.ops.version: 10.0.16
ms.openlocfilehash: b719d8eb868cb1722b470be4443d01181078ce21
ms.sourcegitcommit: 97ada5d52ed1829dcf030dad254096cd8df25da8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/06/2021
ms.locfileid: "5864408"
---
# <a name="financial-dimension-sets"></a><span data-ttu-id="83ee2-103">Finantsdimensioonikomplektid</span><span class="sxs-lookup"><span data-stu-id="83ee2-103">Financial dimension sets</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="83ee2-104">See teema kirjeldab finantsdimensioonide komplekte ja annab näpunäiteid nende kasutamise optimeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="83ee2-104">This topic describes financial dimension sets and provides some tips for optimizing their use.</span></span>

<span data-ttu-id="83ee2-105">Dimensioonikomplekt on finantsdimensioonide järjestatud loend, mida saab kasutada pearaamatu andmete summeerimiseks kasutaja määratletud viisil.</span><span class="sxs-lookup"><span data-stu-id="83ee2-105">A dimension set is an ordered list of financial dimensions that can be used to summarize General ledger data in a user-defined way.</span></span> <span data-ttu-id="83ee2-106">Dimensioonikogumite esmane kasutamine on proovibilansi määratlemine.</span><span class="sxs-lookup"><span data-stu-id="83ee2-106">A primary use of dimension sets is to define a trial balance.</span></span>

<span data-ttu-id="83ee2-107">Ainus standardne dimensioonikogum on dimensioonikogum, mis sisaldab ainult põhikontot.</span><span class="sxs-lookup"><span data-stu-id="83ee2-107">The only standard dimension set is the dimension set that contains only the main account.</span></span>

<span data-ttu-id="83ee2-108">Finantsdimensioonikogumite loomiseks ja haldamiseks kasutage lehte **Finantsdimensioonikogumid**.</span><span class="sxs-lookup"><span data-stu-id="83ee2-108">You use the **Financial dimension sets** page to create and manage financial dimension sets.</span></span>

## <a name="dimension-set-balances"></a><span data-ttu-id="83ee2-109">Dimensiooni määratud saldod</span><span class="sxs-lookup"><span data-stu-id="83ee2-109">Dimension set balances</span></span>

<span data-ttu-id="83ee2-110">Dimensioonikogumil võivad olla finantsdimensioonidel põhinevad saldod.</span><span class="sxs-lookup"><span data-stu-id="83ee2-110">A dimension set can have balances that are based on its financial dimensions.</span></span> <span data-ttu-id="83ee2-111">Saldod on pearaamatus olemas ja põhinevad dimensioonikogumi määratlusel.</span><span class="sxs-lookup"><span data-stu-id="83ee2-111">The balances exist in General ledger and are based on the dimension set definition.</span></span> <span data-ttu-id="83ee2-112">Saldod summeeritakse pearaamatu andmetest, et aidata parandada jõudlust nende toomisel (nt proovibilansi loomisel).</span><span class="sxs-lookup"><span data-stu-id="83ee2-112">The balances are summarized from the General ledger data to help improve performance when they are retrieved (for example, when a trial balance is generated).</span></span>

## <a name="create-balances"></a><span data-ttu-id="83ee2-113">Saldode loomine</span><span class="sxs-lookup"><span data-stu-id="83ee2-113">Create balances</span></span>

<span data-ttu-id="83ee2-114">Kasutage nuppu **Loo saldod**, et lähtestada saldod dimensioonikogumi jaoks, millel pole praegu saldosid.</span><span class="sxs-lookup"><span data-stu-id="83ee2-114">Use the **Create balances** button to initialize the balances for a dimension set that doesn't currently have balances.</span></span>

> [!NOTE]
> <span data-ttu-id="83ee2-115">Soovitame piirata saldodega dimensioonikogumite arvu, kuna saldouuendused mõjutavad kõiki pearaamatu konteerimistegevusi.</span><span class="sxs-lookup"><span data-stu-id="83ee2-115">We recommend that you limit the number of dimension sets that have balances, because balance updates affect all General ledger posting activities.</span></span>

## <a name="update-balances"></a><span data-ttu-id="83ee2-116">Värskenda saldosid</span><span class="sxs-lookup"><span data-stu-id="83ee2-116">Update balances</span></span>

<span data-ttu-id="83ee2-117">Viimase pearaamatu konteerimistegevuse kaasamiseks saldodesse kasutage nuppu **Uuenda saldosid**.</span><span class="sxs-lookup"><span data-stu-id="83ee2-117">Use the **Update balances** button to include the latest General ledger posting activity in the balances.</span></span> <span data-ttu-id="83ee2-118">Saldouuendused on kerge koormusega toimingud.</span><span class="sxs-lookup"><span data-stu-id="83ee2-118">Balance updates are light operations.</span></span> <span data-ttu-id="83ee2-119">Nad peavad töötlema ainult pearaamatu konteerimistegevust, mis on toimunud pärast viimast uuendamist.</span><span class="sxs-lookup"><span data-stu-id="83ee2-119">They must process only the General ledger posting activity that has occurred since the last update.</span></span>

> [!NOTE]
> <span data-ttu-id="83ee2-120">Proovibilansi kuvamine nõuab värskendust veendumaks, et kuvatavad saldod on ajakohased.</span><span class="sxs-lookup"><span data-stu-id="83ee2-120">Display of the trial balance forces an update, to ensure that the balances that are shown are current.</span></span> <span data-ttu-id="83ee2-121">Kaaluge korduva pakett-töö kasutamist, et teie kõige sagedamini kasutatavate dimensioonikogumite uuendused oleks kiired.</span><span class="sxs-lookup"><span data-stu-id="83ee2-121">Consider using a recurring batch job so that updates to your most frequently used dimension sets are quick.</span></span> <span data-ttu-id="83ee2-122">Sel viisil aitate minimeerida aega, mida proovibilansi kasutajad peavad ootama.</span><span class="sxs-lookup"><span data-stu-id="83ee2-122">In this way, you help minimize the time that trial balance users must wait.</span></span>

## <a name="rebuild-balances"></a><span data-ttu-id="83ee2-123">Taasta saldod</span><span class="sxs-lookup"><span data-stu-id="83ee2-123">Rebuild balances</span></span>

<span data-ttu-id="83ee2-124">Saldode nullist uuesti loomiseks kasutage nuppu **Loo saldod uuesti**.</span><span class="sxs-lookup"><span data-stu-id="83ee2-124">Use the **Rebuild balances** button to re-create the balances from scratch.</span></span> <span data-ttu-id="83ee2-125">Sel viisil aitate tagate, et need vastaksid pearaamatu andmetele.</span><span class="sxs-lookup"><span data-stu-id="83ee2-125">In this way, you help ensure that they match the data in General ledger.</span></span> <span data-ttu-id="83ee2-126">Saldode taastamine nõuab palju töötlemist ja seda ei tohiks tavaliselt nõuda.</span><span class="sxs-lookup"><span data-stu-id="83ee2-126">A rebuild of balances requires lots of processing and should not usually be required.</span></span>

> [!NOTE]
> <span data-ttu-id="83ee2-127">Kui teil on stsenaarium, mis nõuab regulaarselt saldode taastamist, soovitame teil pöörduda klienditoe poole.</span><span class="sxs-lookup"><span data-stu-id="83ee2-127">If you have a scenario that regularly requires a rebuild of balances, we recommend that you contact customer support.</span></span> <span data-ttu-id="83ee2-128">Klienditugi aitab teil määratleda, miks saldod pearaamatu andmetega ei ühti.</span><span class="sxs-lookup"><span data-stu-id="83ee2-128">Customer support can help you determine why balances don't match the data in General ledger.</span></span>

## <a name="clear-balances"></a><span data-ttu-id="83ee2-129">Saldode tasaarvestus</span><span class="sxs-lookup"><span data-stu-id="83ee2-129">Clear balances</span></span>

<span data-ttu-id="83ee2-130">Saldode eemaldamiseks ja edasiste värskenduste peatamiseks kasutage nuppu **Tühjenda saldod**.</span><span class="sxs-lookup"><span data-stu-id="83ee2-130">Use the **Clear balances** button to remove the balances and stop any further updates.</span></span> <span data-ttu-id="83ee2-131">Dimensioonikomplekt ei mõjuta enam pearaamatu konteerimistegevusi.</span><span class="sxs-lookup"><span data-stu-id="83ee2-131">The dimension set will no longer have an impact on General ledger posting activities.</span></span>

<span data-ttu-id="83ee2-132">Lisateavet leiate jaotisest [Finantsdimensioonid](financial-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="83ee2-132">For more information, see [Financial dimensions](financial-dimensions.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
