---
title: Pearaamatu eraldamisreeglid
description: Selles artiklis antakse teavet pearaamatu eraldamisreeglite kohta. See kirjeldab nende eraldamisreeglite mitmesuguseid komponente ja eraldamismeetodeid, mida nende puhul kasutada saab.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerAllocation, LedgerAllocationBasisRule, LedgerAllocationRequest, LedgerAllocationRule
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 15402
ms.assetid: 8147e148-7c11-45ef-95c6-f9889a875b54
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 63562cde3f2813fdcfc9df7ccbfc623aa2fbe9b1
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="ledger-allocation-rules"></a><span data-ttu-id="b376b-104">Pearaamatu eraldamisreeglid</span><span class="sxs-lookup"><span data-stu-id="b376b-104">Ledger allocation rules</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b376b-105">Selles artiklis antakse teavet pearaamatu eraldamisreeglite kohta.</span><span class="sxs-lookup"><span data-stu-id="b376b-105">This article provides information about ledger allocation rules.</span></span> <span data-ttu-id="b376b-106">See kirjeldab nende eraldamisreeglite mitmesuguseid komponente ja eraldamismeetodeid, mida nende puhul kasutada saab.</span><span class="sxs-lookup"><span data-stu-id="b376b-106">It describes the various components of these allocation rules and the allocation methods that can be used for them.</span></span>

<span data-ttu-id="b376b-107">Pearaamatu eraldamisreegleid kasutatakse eraldamistöölehtede ja kontokannete automaatseks arvutamiseks ja loomiseks pearaamatu saldode või fikseeritud summade eraldamise eesmärgil.</span><span class="sxs-lookup"><span data-stu-id="b376b-107">Ledger allocation rules are used to automatically calculate and generate allocation journals and account entries for the allocation of ledger balances or fixed amounts.</span></span> <span data-ttu-id="b376b-108">Eraldamismeetodid võivad olla muutuvad või fikseeritud.</span><span class="sxs-lookup"><span data-stu-id="b376b-108">Allocation methods can be variable or fixed.</span></span> <span data-ttu-id="b376b-109">Pearaamatu eraldamisreeglite jaoks saab kasutada järgmisi eraldamismeetodeid.</span><span class="sxs-lookup"><span data-stu-id="b376b-109">The following allocation methods can be used for ledger allocation rules:</span></span>

-   <span data-ttu-id="b376b-110">**Alus** – seda muutujameetodit kasutatakse, kui eraldamine sõltub tegelikust pearaamatu saldost, võttes aluseks filtreerimiskriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="b376b-110">**Basis** – This variable method is used when the allocation depends on the actual ledger balance, based on filter criteria.</span></span> <span data-ttu-id="b376b-111">Näiteks saab eraldada reklaamikulusid iga osakonna müügitulemuste põhjal osakondade kogu müügitulu suhtes.</span><span class="sxs-lookup"><span data-stu-id="b376b-111">For example, advertising expenses can be allocated based on each department's sales in proportion to the total departmental sales.</span></span>
-   <span data-ttu-id="b376b-112">**Fikseeritud protsent** ja **fikseeritud mass** – nende meetodite puhul määratletakse reegli jaoks otse eraldamisprotsent või -mass.</span><span class="sxs-lookup"><span data-stu-id="b376b-112">**Fixed percentage** and **Fixed weight** – For these methods, the allocation percentage or weight is defined directly for the rule.</span></span> <span data-ttu-id="b376b-113">Näiteks saab reklaamikulusid eraldada nii, et osakond A saab 70 protsenti ja osakond B 30 protsenti reklaamikulust.</span><span class="sxs-lookup"><span data-stu-id="b376b-113">For example, advertising expenses can be allocated so that Department A receives 70 percent of the advertising expense and Department B receives 30 percent.</span></span>
-   <span data-ttu-id="b376b-114">**Võrdne** – see meetod jaotab summa võrdselt iga määratud sihtkoha vahel.</span><span class="sxs-lookup"><span data-stu-id="b376b-114">**Equally** – This method distributes the amount equally to each defined destination.</span></span> <span data-ttu-id="b376b-115">Näiteks kui osakonna A ja osakonna B jaoks on sihtkohad määratletud, saab reklaamikulusid eraldada nii, et nii osakond A kui ka osakond B saavad 50 protsenti reklaamikuludest.</span><span class="sxs-lookup"><span data-stu-id="b376b-115">For example, if destinations are defined for Department A and Department B, advertising expenses can be allocated so that both Department A and Department B receive 50 percent of the advertising expense.</span></span>

<span data-ttu-id="b376b-116">Kui eraldamisreegli puhul on eraldamismeetodiks Alus, peate määratlema ka eraldi pearaamatu eraldamise põhised reeglid.</span><span class="sxs-lookup"><span data-stu-id="b376b-116">If Basis is used as the allocation method for an allocation rule, you must also define separate ledger allocation basis rules.</span></span> <span data-ttu-id="b376b-117">Eraldamistaotluse töötlemise protsess võimaldab kasutajatel töödelda pearaamatu eraldamisreeglit ja saadud eraldustöölehe kandeid eelvaadata, enne kui need arvutatud eraldused kas sisestavad või kustutavad.</span><span class="sxs-lookup"><span data-stu-id="b376b-117">The "Process allocation request" process lets users process the ledger allocation rule and preview the resulting allocation journal entries before they either post or delete the calculated allocations.</span></span>

## <a name="components-of-ledger-allocation-rules"></a><span data-ttu-id="b376b-118">Pearaamatu eraldamisreeglite komponendid</span><span class="sxs-lookup"><span data-stu-id="b376b-118">Components of ledger allocation rules</span></span>
<span data-ttu-id="b376b-119">Igal eraldamisreeglil on neli komponenti: üldine, allikas, sihtkoht ja vastaskonto.</span><span class="sxs-lookup"><span data-stu-id="b376b-119">Each allocation rule has four components: general, source, destination, and offset.</span></span> <span data-ttu-id="b376b-120">Kui eraldamismeetodiks on Alus, on nõutav täiendav komponent, pearaamatu eraldamispõhised reeglid.</span><span class="sxs-lookup"><span data-stu-id="b376b-120">An additional component, ledger allocation bases rules, is required if Basis is used as the allocation method.</span></span> <span data-ttu-id="b376b-121">Iga komponent annab olulise osa eraldamiste töötlemiseks vajalikust teabest.</span><span class="sxs-lookup"><span data-stu-id="b376b-121">Each component provides a critical piece of the information that is required in order to process allocations.</span></span>

-   <span data-ttu-id="b376b-122">**Üldine** – selles komponendis määrab kasutaja valikud, nagu eraldamismeetod, kontsernisisesed reeglisätted ja see, kas reegel on aktiivne või mitte.</span><span class="sxs-lookup"><span data-stu-id="b376b-122">**General** – This component is where the user specifies options such as the allocation method, intercompany rule settings, and whether the rule is active.</span></span>
-   <span data-ttu-id="b376b-123">**Allikas** – selles komponendis määrab kasutaja eraldamise lähteandmed.</span><span class="sxs-lookup"><span data-stu-id="b376b-123">**Source** – This component is where the user specifies the source data for the allocation.</span></span> <span data-ttu-id="b376b-124">Eraldamine võib toimuda pearaamatu saldode (**Andmeallikas** = **peaaamat**) või fikseeritud summade (**Andmeallikas** = **fikseeritud väärtus**) põhjal.</span><span class="sxs-lookup"><span data-stu-id="b376b-124">Allocation can be based on ledger balances (**Data source** = **Ledger**) or fixed amounts (**Data source** = **Fixed value**).</span></span> <span data-ttu-id="b376b-125">Kui suvandi **Andmeallikas** sätteks on valitud **Pearaamat**, tuleb pearaamatu eraldamisreegli jaoks määratleda allika filtreerimiskriteeriumid (nt reklaamikulude jaoks).</span><span class="sxs-lookup"><span data-stu-id="b376b-125">When **Data source** is set to **Ledger**, source filter criteria must be defined for the ledger allocation rule (for example, for the advertising expenses).</span></span>
-   <span data-ttu-id="b376b-126">**Sihtkoht** – see komponent määratleb, kuidas tuleks eraldamisarvutuse tulemus jaotada ja arvestada.</span><span class="sxs-lookup"><span data-stu-id="b376b-126">**Destination** – This component defines how the result of the allocation calculation should be distributed and accounted for.</span></span> <span data-ttu-id="b376b-127">Näiteks saab olla iga osakonna kohta üks sihtkoharida.</span><span class="sxs-lookup"><span data-stu-id="b376b-127">For example, there can be one destination line for each department.</span></span>
-   <span data-ttu-id="b376b-128">**Vastaskonto** – see komponent määratleb, kuidas tuleks põhikontod ja dimensioonid sihkohakandeid tasakaalustavate vastaskonto kannete kohta määrata.</span><span class="sxs-lookup"><span data-stu-id="b376b-128">**Offset** – This component defines how main accounts and dimensions should be determined for the offset entries that balance the destination entries.</span></span> <span data-ttu-id="b376b-129">Allikal põhinevate kontode ja dimensioonide asemel kasutatakse tavaliselt kasutaja määratletud suvandeid.</span><span class="sxs-lookup"><span data-stu-id="b376b-129">User-defined options are typically used instead of accounts and dimensions that are based on the source.</span></span> <span data-ttu-id="b376b-130">Kui suvandi **Andmeallikas** sätteks on valitud **Fikseeritud väärtus**, ei saa suvandit **Allikas** kasutada.</span><span class="sxs-lookup"><span data-stu-id="b376b-130">When **Data source** is set to **Fixed value**, **Source** can't be used as an option.</span></span>
-   <span data-ttu-id="b376b-131">**Pearaamatu eraldamispõhised reeglid** – need reeglid määratlevad oma allika filtreerimiskriteerumite alusel, milliseid pearaamatu saldosid tuleks eraldamiseks kasutada (nt eelarve osakonna kohta).</span><span class="sxs-lookup"><span data-stu-id="b376b-131">**Ledger allocation basis rules** – These rules use their own source filter criteria to determine which ledger balances should be used for allocation (for example, the revenue per department).</span></span> <span data-ttu-id="b376b-132">Iga eralduspõhist reeglit saab kasutada mitme eraldusreegliga.</span><span class="sxs-lookup"><span data-stu-id="b376b-132">Each allocation basis rule can be used with multiple allocation rules.</span></span>





