---
title: Pearaamatu ja finantsaruandluse avaleht
description: "Pearaamatu abil saate määratleda ja hallata juriidilise isiku finantskirjeid."
author: twheeloc
manager: AnnBe
ms.date: 08/31/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 65431
ms.assetid: d2c604df-daae-42cd-82d9-c80e3dee4a60
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e544c592429d00b1ce464740f4e82cb75d10412b
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="general-ledger"></a><span data-ttu-id="ac678-103">Pearaamat</span><span class="sxs-lookup"><span data-stu-id="ac678-103">General ledger</span></span> 

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ac678-104">Pearaamatu abil saate määratleda ja hallata juriidilise isiku finantskirjeid.</span><span class="sxs-lookup"><span data-stu-id="ac678-104">Use General ledger to define and manage the legal entity’s financial records.</span></span> <span data-ttu-id="ac678-105">Pearaamat on deebet- ja kreeditkirjete register.</span><span class="sxs-lookup"><span data-stu-id="ac678-105">The general ledger is a register of debit and credit entries.</span></span> <span data-ttu-id="ac678-106">Need kirjed liigitatakse kontoplaanis loetletud kontode abil.</span><span class="sxs-lookup"><span data-stu-id="ac678-106">These entries are classified using the accounts that are listed in a chart of accounts.</span></span> 

 - [<span data-ttu-id="ac678-107">Kontoplaanide plaanimine</span><span class="sxs-lookup"><span data-stu-id="ac678-107">Plan your chart of accounts</span></span>](plan-chart-of-accounts.md)
 - [<span data-ttu-id="ac678-108">Põhikonto tüübid</span><span class="sxs-lookup"><span data-stu-id="ac678-108">Main account types</span></span>](main-account-types.md)

<span data-ttu-id="ac678-109">Saate eraldada või jaotada rahalisi summasid ühele või mitmele kontole või konto ja dimensiooni kombinatsioonile vastavalt eraldamise reeglitele.</span><span class="sxs-lookup"><span data-stu-id="ac678-109">You can allocate, or distribute, monetary amounts to one or more accounts or account and dimension combinations based on allocation rules.</span></span> <span data-ttu-id="ac678-110">Eraldamisi on kahte tüüpi: fikseeritud ja muutuvad.</span><span class="sxs-lookup"><span data-stu-id="ac678-110">There are two types of allocations: fixed and variable.</span></span> <span data-ttu-id="ac678-111">Saate ka pearaamatukontode vahelisi kandeid tasakaalustada ja valuutasummasid ümber hinnata.</span><span class="sxs-lookup"><span data-stu-id="ac678-111">You can also settle transactions between ledger accounts and revalue currency amounts.</span></span> <span data-ttu-id="ac678-112">Rahandusaasta lõpus tuleb teil luua sulgemiskanded ja valmistada kontod ette järgmiseks rahandusaastaks.</span><span class="sxs-lookup"><span data-stu-id="ac678-112">At the end of a fiscal year, you must generate closing transactions and prepare your accounts for the next fiscal year.</span></span> <span data-ttu-id="ac678-113">Konsolideerimisfunktsiooniga saate kombineerida mitme allüksuse juriidiliste isikute tulemused ühe konsolideeritud organisatsiooni tulemusteks.</span><span class="sxs-lookup"><span data-stu-id="ac678-113">You can use the consolidation functionality to combine the financial results for several subsidiary legal entities into results for a single, consolidated organization.</span></span> <span data-ttu-id="ac678-114">Allüksused võivad olla Microsoft Dynamics 365 for Finance and Operationsi samas andmebaasis või eraldi andmebaasides.</span><span class="sxs-lookup"><span data-stu-id="ac678-114">The subsidiaries can be in the same Microsoft Dynamics 365 for Finance and Operations database or in separate databases.</span></span>

- [<span data-ttu-id="ac678-115">Konsolideerimise ja eemaldamise ülevaade</span><span class="sxs-lookup"><span data-stu-id="ac678-115">Consolidation and elimination overview</span></span>](../budgeting/consolidation-elimination-overview.md)
- [<span data-ttu-id="ac678-116">Pearaamatukonto saldod</span><span class="sxs-lookup"><span data-stu-id="ac678-116">General ledger account balances</span></span>](general-ledger-account-balances.md)
- [<span data-ttu-id="ac678-117">Finantsdimensioonid</span><span class="sxs-lookup"><span data-stu-id="ac678-117">Financial dimensions</span></span>](financial-dimensions.md)

<span data-ttu-id="ac678-118">[![Äriprotsess](./media/GL-process.PNG)](./media/GL-process.PNG)</span><span class="sxs-lookup"><span data-stu-id="ac678-118">[![Business process](./media/GL-process.PNG)](./media/GL-process.PNG)</span></span>

# <a name="sales-tax"></a><span data-ttu-id="ac678-119">Käibemaks</span><span class="sxs-lookup"><span data-stu-id="ac678-119">Sales tax</span></span>
<span data-ttu-id="ac678-120">Kõik ettevõtted koguvad ja maksavad makse erinevatele maksuametitele.</span><span class="sxs-lookup"><span data-stu-id="ac678-120">Every company collects and pays taxes to various tax authorities.</span></span> <span data-ttu-id="ac678-121">Reeglid ja määrad erinevad riikide/regioonide, maakondade, valdade ja linnade lõikes.</span><span class="sxs-lookup"><span data-stu-id="ac678-121">The rules and rates vary by country/region, state, county, and city.</span></span>
<span data-ttu-id="ac678-122">Lisaks tuleb reegleid regulaarselt uuendada, kui maksuasutused oma nõudeid muudavad.</span><span class="sxs-lookup"><span data-stu-id="ac678-122">In addition, the rules must be updated periodically when tax authorities change their requirements.</span></span> <span data-ttu-id="ac678-123">Käibemaksukoodid sisaldavad baasteavet maksuametile kogutavate ja tasutavate maksude suuruse kohta.</span><span class="sxs-lookup"><span data-stu-id="ac678-123">Sales tax codes contain the basic information about how much you collect and pay to the authorities.</span></span> <span data-ttu-id="ac678-124">Käibemaksukoodide häälestamise saate määratleda summad või protsendid, mis tuleb koguda.</span><span class="sxs-lookup"><span data-stu-id="ac678-124">When you set up sales tax codes, you define the amounts or percentages that must be collected.</span></span> <span data-ttu-id="ac678-125">Samuti saate määratleda mitmesugused viisid, kuidas summad või protsendid rakendatakse kannete summadele.</span><span class="sxs-lookup"><span data-stu-id="ac678-125">You also define the various methods by which those amounts or percentages are applied to transaction amounts.</span></span> <span data-ttu-id="ac678-126">Selle jaotise teemad annavad teavet selle kohta, kuidas seadistada käibemaksukoode maksuameti nõutavatele makseviisidele ja maksumääradele.</span><span class="sxs-lookup"><span data-stu-id="ac678-126">The topics in this section provide information about how to set up sales tax codes for the methods and rates that your tax authorities require.</span></span>

 - [<span data-ttu-id="ac678-127">Käibemaksu ülevaade</span><span class="sxs-lookup"><span data-stu-id="ac678-127">Sales tax overview</span></span>](indirect-taxes-overview.md)
 - [<span data-ttu-id="ac678-128">Käibemaksumäärad väljade Marginaali alus ja Arvutusmeetod põhjal</span><span class="sxs-lookup"><span data-stu-id="ac678-128">Sales tax rates based on the Marginal base and Calculation methods</span></span>](marginal-base-field.md)
 - [<span data-ttu-id="ac678-129">Käibemaksu maksed ja ümardamisreeglid</span><span class="sxs-lookup"><span data-stu-id="ac678-129">Sales tax payments and rounding rules</span></span>](round-sales-tax-payments.md)


### <a name="additional-resources"></a><span data-ttu-id="ac678-130">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="ac678-130">Additional resources</span></span>

#### <a name="whats-new-and-in-development"></a><span data-ttu-id="ac678-131">Mis on uut ja mis on arendamisel</span><span class="sxs-lookup"><span data-stu-id="ac678-131">What's new and in development</span></span>

<span data-ttu-id="ac678-132">Avage [Microsoft Dynamics 365 sisukaart](https://roadmap.dynamics.com/), et näha, millised uued funktsioonid on välja antud ja millised uued funktsioonid on arendamisel.</span><span class="sxs-lookup"><span data-stu-id="ac678-132">Go to the [Microsoft Dynamics 365 Roadmap](https://roadmap.dynamics.com/) to see what new features have been released and what new features are in development.</span></span> 

#### <a name="blogs"></a><span data-ttu-id="ac678-133">Ajaveebid</span><span class="sxs-lookup"><span data-stu-id="ac678-133">Blogs</span></span>

<span data-ttu-id="ac678-134">Ostureskontro ja muude lahendustega seotud arvamused, uudised ja muu teabe leiate [Microsoft Dynamics 365 ajaveebist](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise).</span><span class="sxs-lookup"><span data-stu-id="ac678-134">You can find opinions, news, and other information about Accounts payable and other solutions on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise).</span></span>

<span data-ttu-id="ac678-135">Palju postitusi pearaamatu kohta leiate ka [Microsoft Dynamics AX-i tootemeeskonna ajaveebist](https://blogs.msdn.microsoft.com/dax/).</span><span class="sxs-lookup"><span data-stu-id="ac678-135">There are many posts about General ledger on the [Microsoft Dynamics AX product team blog](https://blogs.msdn.microsoft.com/dax/).</span></span> <span data-ttu-id="ac678-136">Kuigi mõni neist sisestustest on kirjutatud pearaamatu eelmise versiooni jaoks, kehtivad samad mõisted sellegipoolest ja protseduurid on praeguses versioonis sarnased.</span><span class="sxs-lookup"><span data-stu-id="ac678-136">Although some of these posts were written for the previous version of General ledger, the same concepts still apply, and the procedures are also similar in the current version.</span></span>

<span data-ttu-id="ac678-137">[Microsoft Dynamics Operationsi partnerite kogukonna ajaveeb](https://community.dynamics.com/partner/b/operationspartnercommunityblog) on Microsoft Dynamicsi partnerite jaoks kõikehõlmav ressurss, kust nad saavad teada, mis on rakenduses MBS Operations uut ja põnevat.</span><span class="sxs-lookup"><span data-stu-id="ac678-137">The [Microsoft Dynamics Operations Partner Community Blog](https://community.dynamics.com/partner/b/operationspartnercommunityblog) gives Microsoft Dynamics Partners a single resource where they can learn what is new and trending in MBS Operations.</span></span>

#### <a name="task-guides"></a><span data-ttu-id="ac678-138">Tegevuse juhised</span><span class="sxs-lookup"><span data-stu-id="ac678-138">Task guides</span></span>
<span data-ttu-id="ac678-139">Täiendav spikker on saadaval tegevuse juhistena rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ac678-139">Additional help is available as task guides inside Finance and Operations.</span></span> <span data-ttu-id="ac678-140">Tegevuse juhistele juurdepääsemiseks klõpsake ükskõik millisel lehel nuppu Spikker.</span><span class="sxs-lookup"><span data-stu-id="ac678-140">To access task guides, click the Help button on any page.</span></span>

#### <a name="videos"></a><span data-ttu-id="ac678-141">Videod</span><span class="sxs-lookup"><span data-stu-id="ac678-141">Videos</span></span>

<span data-ttu-id="ac678-142">Vaadake õppevideoid, mis on saadaval [Microsoft Dynamics 365 YouTube’i kanalil](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span><span class="sxs-lookup"><span data-stu-id="ac678-142">Check out the how-to videos that are now available on the [Microsoft Dynamics 365 YouTube Channel](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).</span></span>


