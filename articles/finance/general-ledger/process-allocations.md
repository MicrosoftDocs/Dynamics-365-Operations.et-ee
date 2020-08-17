---
title: Eraldiste töötlemine
description: Selles artiklis antakse teavet eraldamiste kohta, nende töötlemise võimaluste kohta Microsoft Dynamics 365 Financeis ja nende kasutamise kohta eelarve planeerimisel. Eraldamisi kasutatakse summade jaotamiseks mitme pearaamatukonto kombinatsiooni lõikes. Need aitavad tagada seda, et raamatupidamises esitatakse kulud või tulud õigele objektile.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4c8216ebdd1f26601743e6b35849be0813d06b4a
ms.sourcegitcommit: 4676ea9646fa1a182103ecab93e78a69001f0b8d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/21/2020
ms.locfileid: "3612658"
---
# <a name="process-allocations"></a><span data-ttu-id="b3360-105">Eraldiste töötlemine</span><span class="sxs-lookup"><span data-stu-id="b3360-105">Process allocations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b3360-106">Selles artiklis antakse teavet eraldamiste kohta, nende töötlemise võimaluste kohta is ja nende kasutamise kohta eelarve planeerimisel.</span><span class="sxs-lookup"><span data-stu-id="b3360-106">This article provides information about allocations, the options for processing them, and how they can be used in budget planning.</span></span> <span data-ttu-id="b3360-107">Eraldamisi kasutatakse summade jaotamiseks mitme pearaamatukonto kombinatsiooni lõikes.</span><span class="sxs-lookup"><span data-stu-id="b3360-107">Allocations are used to distribute amounts across multiple ledger account combinations.</span></span> <span data-ttu-id="b3360-108">Need aitavad tagada seda, et raamatupidamises esitatakse kulud või tulud õigele objektile.</span><span class="sxs-lookup"><span data-stu-id="b3360-108">They help ensure that expenses or revenues are charged to the correct object in accounting.</span></span>

<span data-ttu-id="b3360-109">Seda protsessi toetavad järgmised võimalused:</span><span class="sxs-lookup"><span data-stu-id="b3360-109">The following capabilities support this process:</span></span>

-   <span data-ttu-id="b3360-110">Kandesummade käsitsi eraldamine, kasutades arvestuse jaotustes tükeldamise toimingut või rakendades dokumendile finantsdimensiooni vaikemalle.</span><span class="sxs-lookup"><span data-stu-id="b3360-110">Manually allocate transaction amounts by using the Split action in accounting distributions, or by applying financial dimension default templates to a document.</span></span> <span data-ttu-id="b3360-111">Lisateavet vt [Arvestuse jaotused](../accounts-payable/accounting-distributions.md).</span><span class="sxs-lookup"><span data-stu-id="b3360-111">For more information, see [Accounting distributions](../accounts-payable/accounting-distributions.md).</span></span>
-   <span data-ttu-id="b3360-112">Saate eraldada automaatselt kandesummasid eraldi põhikontol määratletud eraldustingimuste põhjal.</span><span class="sxs-lookup"><span data-stu-id="b3360-112">Automatically allocate transactions amounts based on allocation terms defined on individual main account.</span></span> <span data-ttu-id="b3360-113">Eraldamise konto kanded luuakse iga töölehe jaoks protsendi ja siht-pearaamatukonto põhjal, alati kui raamatupidamiskirje vastab lähte-pearaamatukontona määratletud kriteeriumidele.</span><span class="sxs-lookup"><span data-stu-id="b3360-113">Allocation account entries will be generated for each journal based on the percentage and destination ledger account whenever an accounting entry meets the criteria defined as the source ledger account.</span></span> <span data-ttu-id="b3360-114">Lisateabe jaoks vt [Põhikonto eraldustingimused](../general-ledger/main-account-allocation-terms.md)</span><span class="sxs-lookup"><span data-stu-id="b3360-114">For more information, see [Main account allocation terms](../general-ledger/main-account-allocation-terms.md)</span></span>
-   <span data-ttu-id="b3360-115">Saate eraldada automaatselt pearaamatu saldosid või fikseeritud summasid pearaamatu eraldamisreeglite põhjal.</span><span class="sxs-lookup"><span data-stu-id="b3360-115">Automatically allocate ledger balances or fixed amounts based on ledger allocation rules.</span></span> <span data-ttu-id="b3360-116">Pearaamatu eraldamisreegleid töödeldakse perioodiliselt, kasutades eraldamise töölehti.</span><span class="sxs-lookup"><span data-stu-id="b3360-116">The ledger allocation rules are processed on a periodic basis using allocation journals.</span></span> <span data-ttu-id="b3360-117">Lisateavet leiate jaotisest [Eraldusreeglid](../general-ledger/ledger-allocation-rules.md).</span><span class="sxs-lookup"><span data-stu-id="b3360-117">For more information, see [Allocation rules](../general-ledger/ledger-allocation-rules.md).</span></span>

###  <a name="allocations-in-budget-planning"></a><span data-ttu-id="b3360-118">Eelarve plaanimise eraldamised</span><span class="sxs-lookup"><span data-stu-id="b3360-118">Allocations in budget planning</span></span>

<span data-ttu-id="b3360-119">Pearaamatu eraldamisreegleid saab kasutada eelarveplaanide puhul.</span><span class="sxs-lookup"><span data-stu-id="b3360-119">Ledger allocation rules can be used for budget plans.</span></span> <span data-ttu-id="b3360-120">Eelarve plaanimisel pearaamatu eraldamisreeglite kasutamise korral toimivad eraldamisreeglid samal moel kui pearaamatus, kuid lähteandmed ja sihtandmed tulevad eelarveplaanist.</span><span class="sxs-lookup"><span data-stu-id="b3360-120">When you use ledger allocation rules in budget planning, the allocation rules work the same way they would in the ledger, but the source data and destination data comes from the budget plan.</span></span> <span data-ttu-id="b3360-121">Eelarveplaanides kasutatavad pearaamatu eraldamisreeglid saate valida käsitsi.</span><span class="sxs-lookup"><span data-stu-id="b3360-121">You can manually select ledger allocation rules to use for budget plans.</span></span> <span data-ttu-id="b3360-122">Teise võimalusena saate kasutada eraldamisgraafikut, mida käitatakse osana töövooprotsessist.</span><span class="sxs-lookup"><span data-stu-id="b3360-122">Alternatively, you can use an allocation schedule that runs as part of a workflow process.</span></span>

> [!NOTE]
> <span data-ttu-id="b3360-123">Eelarve plaanimiseks ei saa kasutada kontsernisiseseid pearaamatu eraldamisreegleid.</span><span class="sxs-lookup"><span data-stu-id="b3360-123">You can’t use intercompany ledger allocation rules for budget planning.</span></span>

