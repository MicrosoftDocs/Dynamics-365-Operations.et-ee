---
title: "Eraldiste töötlemine"
description: "Selles artiklis antakse teavet eraldamiste kohta, nende töötlemise võimaluste kohta Microsoft Dynamics 365 for Finance and Operations, Enterprise editionis ja nende kasutamise kohta eelarve plaanimisel. Eraldamisi kasutatakse summade jaotamiseks mitme pearaamatukonto kombinatsiooni lõikes. Need aitavad tagada seda, et raamatupidamises esitatakse kulud või tulud õigele objektile."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: cb12e24fcb8e8c91f90b91e2fdb3039dd1735ca3
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="process-allocations"></a><span data-ttu-id="60045-105">Eraldiste töötlemine</span><span class="sxs-lookup"><span data-stu-id="60045-105">Process allocations</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="60045-106">Selles artiklis antakse teavet eraldamiste kohta, nende töötlemise võimaluste kohta Microsoft Dynamics 365 for Finance and Operations, Enterprise editionis ja nende kasutamise kohta eelarve plaanimisel.</span><span class="sxs-lookup"><span data-stu-id="60045-106">This article provides information about allocations, the options for processing them in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, and how they can be used in budget planning.</span></span> <span data-ttu-id="60045-107">Eraldamisi kasutatakse summade jaotamiseks mitme pearaamatukonto kombinatsiooni lõikes.</span><span class="sxs-lookup"><span data-stu-id="60045-107">Allocations are used to distribute amounts across multiple ledger account combinations.</span></span> <span data-ttu-id="60045-108">Need aitavad tagada seda, et raamatupidamises esitatakse kulud või tulud õigele objektile.</span><span class="sxs-lookup"><span data-stu-id="60045-108">They help guarantee that expenses or revenue is charged to the correct object in accounting.</span></span>

<span data-ttu-id="60045-109">Microsoft Dynamics 365 for Finance and Operations annab selle protsessi toetamiseks järgmised võimalused.</span><span class="sxs-lookup"><span data-stu-id="60045-109">Microsoft Dynamics 365 for Finance and Operations provides the following capabilities to support this process:</span></span>

-   <span data-ttu-id="60045-110">Kandesummade käsitsi eraldamine, kasutades arvestuse jaotustes tükeldamise toimingut või rakendades dokumendile finantsdimensiooni vaikemalle.</span><span class="sxs-lookup"><span data-stu-id="60045-110">Manually allocate transaction amounts by using the Split action in accounting distributions, or by applying financial dimension default templates to a document.</span></span> <span data-ttu-id="60045-111">Lisateavet kuluarvestuse kohta vt jaotisest [Arvestuse jaotused.](../accounts-payable/accounting-distributions.md)</span><span class="sxs-lookup"><span data-stu-id="60045-111">For more information, see [Accounting distributions.](../accounts-payable/accounting-distributions.md)</span></span>
-   <span data-ttu-id="60045-112">Saate eraldada automaatselt kandesummasid eraldi põhikontol määratletud eraldustingimuste põhjal.</span><span class="sxs-lookup"><span data-stu-id="60045-112">Automatically allocate transactions amounts based on allocation terms defined on individual main account.</span></span> <span data-ttu-id="60045-113">Eraldamise konto kanded luuakse iga töölehe jaoks protsendi ja siht-pearaamatukonto põhjal, alati kui raamatupidamiskirje vastab lähte-pearaamatukontona määratletud kriteeriumidele.</span><span class="sxs-lookup"><span data-stu-id="60045-113">Allocation account entries will be generated for each journal based on the percentage and destination ledger account whenever an accounting entry meets the criteria defined as the source ledger account.</span></span>
-   <span data-ttu-id="60045-114">Saate eraldada automaatselt pearaamatu saldosid või fikseeritud summasid pearaamatu eraldamisreeglite põhjal.</span><span class="sxs-lookup"><span data-stu-id="60045-114">Automatically allocate ledger balances or fixed amounts based on ledger allocation rules.</span></span> <span data-ttu-id="60045-115">Pearaamatu eraldamisreegleid töödeldakse perioodiliselt, kasutades eraldamise töölehti.</span><span class="sxs-lookup"><span data-stu-id="60045-115">The ledger allocation rules are processed on a periodic basis using allocation journals.</span></span> 

###  <a name="allocations-in-budget-planning"></a><span data-ttu-id="60045-116">Eelarve plaanimise eraldamised</span><span class="sxs-lookup"><span data-stu-id="60045-116">Allocations in budget planning</span></span>

<span data-ttu-id="60045-117">Pearaamatu eraldamisreegleid saab kasutada eelarveplaanide puhul.</span><span class="sxs-lookup"><span data-stu-id="60045-117">Ledger allocation rules can be used for budget plans.</span></span> <span data-ttu-id="60045-118">Eelarve plaanimisel pearaamatu eraldamisreeglite kasutamise korral toimivad eraldamisreeglid samal moel kui pearaamatus, kuid lähteandmed ja sihtandmed tulevad eelarveplaanist.</span><span class="sxs-lookup"><span data-stu-id="60045-118">When you use ledger allocation rules in budget planning, the allocation rules work the same way they would in the ledger, but the source data and destination data comes from the budget plan.</span></span> <span data-ttu-id="60045-119">Eelarveplaanides kasutatavad pearaamatu eraldamisreeglid saate valida käsitsi.</span><span class="sxs-lookup"><span data-stu-id="60045-119">You can manually select ledger allocation rules to use for budget plans.</span></span> <span data-ttu-id="60045-120">Teise võimalusena saate kasutada eraldamisgraafikut, mida käitatakse osana töövooprotsessist.</span><span class="sxs-lookup"><span data-stu-id="60045-120">Alternatively, you can use an allocation schedule that runs as part of a workflow process.</span></span>

> [!NOTE]
> <span data-ttu-id="60045-121">Eelarve plaanimiseks ei saa kasutada kontsernisiseseid pearaamatu eraldamisreegleid.</span><span class="sxs-lookup"><span data-stu-id="60045-121">You can’t use intercompany ledger allocation rules for budget planning.</span></span>






