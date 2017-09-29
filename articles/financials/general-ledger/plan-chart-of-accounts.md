---
title: Kontoplaani kavandamine
description: Selles artiklis antakse teavet, mis aitab teil planeerida organisatsiooni kontoplaane.
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: robinr
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 848da7ec8f4a7915f3b78945b808b564f4510434
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---

# <a name="plan-your-chart-of-accounts"></a><span data-ttu-id="221d0-103">Kontoplaani kavandamine</span><span class="sxs-lookup"><span data-stu-id="221d0-103">Plan your chart of accounts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="221d0-104">Selles artiklis antakse teavet, mis aitab teil planeerida organisatsiooni kontoplaane.</span><span class="sxs-lookup"><span data-stu-id="221d0-104">This article provides information that will help you plan the chart of accounts for your organization.</span></span>

<span data-ttu-id="221d0-105">Organisatsiooni finantsteabe jälgimiseks ja säilitamiseks saate seadistada kontoplaani.</span><span class="sxs-lookup"><span data-stu-id="221d0-105">To track and maintain financial information in an organization, you can set up a chart of accounts.</span></span> <span data-ttu-id="221d0-106">Kontoplaan on finantsraamistikku määratlevate kontode kogum.</span><span class="sxs-lookup"><span data-stu-id="221d0-106">A chart of accounts is a collection of accounts that define a financial framework.</span></span> <span data-ttu-id="221d0-107">Nende kontode kannete edasiseks jälgimiseks saate lisada segmente, mida nimetatakse finantsdimensioonideks.</span><span class="sxs-lookup"><span data-stu-id="221d0-107">To further track the transactions in these accounts, you can add segments, which are known as financial dimensions.</span></span> <span data-ttu-id="221d0-108">Näiteks võib kulukonto sisaldada finantsdimensioone nimedega Osakond, Kulukeskus ja Eesmärk.</span><span class="sxs-lookup"><span data-stu-id="221d0-108">For example, an expense account might include financial dimensions that are named Department, Cost center, and Purpose.</span></span> <span data-ttu-id="221d0-109">Kasutaja määratud reeglid, mida nimetatakse konto struktuurideks ja täpsemateks reegliteks, määravad, kuidas finantsdimensioonid on seotud põhikontode ja muude finantsdimensioonidega ning kuidas kandeid sisestatakse.</span><span class="sxs-lookup"><span data-stu-id="221d0-109">User-defined rules, which are known as account structures and advanced rules, determine how financial dimensions are attached to the main accounts and other financial dimensions, and also how transactions are entered.</span></span> 

<span data-ttu-id="221d0-110">Kontoplaan on juriidilise isiku pearaamatukontode struktureeritud loend.</span><span class="sxs-lookup"><span data-stu-id="221d0-110">The chart of accounts is a structured list of a legal entity’s general ledger accounts.</span></span> <span data-ttu-id="221d0-111">Seda loendit kasutatakse ametivõimudele ja omanikele finantsaruannete ettevalmistamiseks.</span><span class="sxs-lookup"><span data-stu-id="221d0-111">The list is used to prepare financial reports for authorities and owners.</span></span> <span data-ttu-id="221d0-112">Kontod on grupeeritud kontotüüpide järgi ja seejärel koondatud suurematesse kategooriatesse.</span><span class="sxs-lookup"><span data-stu-id="221d0-112">The accounts are grouped into types of accounts and then further aggregated into larger categories.</span></span> <span data-ttu-id="221d0-113">Kõige üldisemal tasandil on kontod grupeeritud tulude ja kuludena (kasutusel olevad kontod) ning varade ja kohustustena (bilansikontod).</span><span class="sxs-lookup"><span data-stu-id="221d0-113">At the most general level, the accounts are grouped as revenues and costs (operating accounts), and assets and liabilities (balance accounts).</span></span> 

<span data-ttu-id="221d0-114">Kontoplaani saavad jagada ja kasutada kõik organisatsiooni juriidilised isikud.</span><span class="sxs-lookup"><span data-stu-id="221d0-114">A chart of accounts can be shared and used by any legal entity in an organization.</span></span> <span data-ttu-id="221d0-115">Kontoplaan, mida juriidiline isik kasutab, on määratletud lehel **Pearaamat**.</span><span class="sxs-lookup"><span data-stu-id="221d0-115">The chart of accounts that is used by a legal entity is defined on the **Ledger** page.</span></span> 

<span data-ttu-id="221d0-116">Järgmiselt on toodud mõni tegur, millega peate oma organisatsiooni kontoplaani struktuuri plaanimisel arvestama.</span><span class="sxs-lookup"><span data-stu-id="221d0-116">Here are some of the factors that you must consider when you plan the structure of the chart of accounts for your organization:</span></span>

-   <span data-ttu-id="221d0-117">Organisatsiooni riigi/regiooni aruandluse nõuded</span><span class="sxs-lookup"><span data-stu-id="221d0-117">The reporting requirements of the country/region where your organization is based</span></span>
-   <span data-ttu-id="221d0-118">Teie juriidilise isiku aruandluse nõuded</span><span class="sxs-lookup"><span data-stu-id="221d0-118">The reporting requirements of your legal entity</span></span>
-   <span data-ttu-id="221d0-119">Nõutav üksikasjalik täpsustustase nii muude organisatsioonide kui ka teie organisatsiooni jaoks</span><span class="sxs-lookup"><span data-stu-id="221d0-119">The degree of specification that is required, both for both external organizations and for your organization</span></span>

<span data-ttu-id="221d0-120">Looge kontoplaan lehel **Kontoplaan**.</span><span class="sxs-lookup"><span data-stu-id="221d0-120">Create the chart of accounts on the **Chart of accounts** page.</span></span> <span data-ttu-id="221d0-121">Põhikontosid saab luua lehel **Kontoplaan** või lehel **Põhikontod**.</span><span class="sxs-lookup"><span data-stu-id="221d0-121">Main accounts can be created from the **Chart of accounts** page or the **Main accounts** page.</span></span> <span data-ttu-id="221d0-122">Põhikontodel ei tohiks kasutada erimärke, mida kasutatakse kontoplaani eraldajatena.</span><span class="sxs-lookup"><span data-stu-id="221d0-122">Your main accounts shouldn't use any special characters that are used as chart of accounts delimiters.</span></span> <span data-ttu-id="221d0-123">Erimärgi olemasolul, mis vastab teie kontoplaani eraldajale, võib konto ja dimensiooni kombinatsioonide sisestamisel ilmneda ebastabiilsus või olla alati vaja otsinguid või hüpikut kasutada.</span><span class="sxs-lookup"><span data-stu-id="221d0-123">If you do have a special character that is the same as your chart of accounts delimiter, you may experience instability, or the need to always use lookups or the flyout when entering account and dimension combinations.</span></span> <span data-ttu-id="221d0-124">Lisateabe jaoks vt [Põhikonto loomine](tasks/create-account-structures.md).</span><span class="sxs-lookup"><span data-stu-id="221d0-124">For more information, see [Create a main account](tasks/create-account-structures.md).</span></span>


<span data-ttu-id="221d0-125">Soovitatav on siduda põhikontod põhikonto kategooriatega, nii et saate kasutada vaikimisi finantsaruandeid ega pea muudatusi tegema.</span><span class="sxs-lookup"><span data-stu-id="221d0-125">It's a good idea to link the main accounts to main account categories, so that you can take advantage of the default financial reports without having to make any modifications.</span></span> <span data-ttu-id="221d0-126">Seetõttu saate aruandeid kiiremini ja hõlpsamini kujundada ja säilitada.</span><span class="sxs-lookup"><span data-stu-id="221d0-126">Therefore, you can more quickly and easily design and maintain reports.</span></span> 

<span data-ttu-id="221d0-127">Kasutage konto struktuuride loomiseks lehte **Konto struktuuride konfigureerimine**.</span><span class="sxs-lookup"><span data-stu-id="221d0-127">Use the **Configure account structures** page to create account structures.</span></span> <span data-ttu-id="221d0-128">Konto struktuurid määratlevad kehtivaid kombinatsioone.</span><span class="sxs-lookup"><span data-stu-id="221d0-128">Account structures define valid combinations.</span></span> <span data-ttu-id="221d0-129">Need kombinatsioonid koos põhikontodega moodustavad kontoplaani.</span><span class="sxs-lookup"><span data-stu-id="221d0-129">The combinations, together with main accounts, form a chart of accounts.</span></span>  <span data-ttu-id="221d0-130">Lisateabe jaoks vt [Konto struktuuride loomine](tasks/create-main-account.md).</span><span class="sxs-lookup"><span data-stu-id="221d0-130">For more information, see [Create account structures](tasks/create-main-account.md).</span></span>

<span data-ttu-id="221d0-131">**Juriidilise isiku alistamised**</span><span class="sxs-lookup"><span data-stu-id="221d0-131">**Legal entity overrides**</span></span> 

<span data-ttu-id="221d0-132">Kõik põhikontod ei kehti kõikide juriidiliste isikute puhul ja mõned võivad olla asjakohased ainult konkreetse ajaperioodi puhul.</span><span class="sxs-lookup"><span data-stu-id="221d0-132">Not all main accounts are valid for all legal entities and some may only be relevant for a specific time period.</span></span> <span data-ttu-id="221d0-133">Sellisel juhul saab jaotist Juriidilise isiku alistamised kasutada tuvastamaks, milliste ettevõtete põhikonto tuleks peatada, kes on omanik ja mis ajaperioodil on dimensioon aktiivne.</span><span class="sxs-lookup"><span data-stu-id="221d0-133">In this scenario the Legal entity overrides section can be used to identify which companies the main account should be suspended for, who the owner is and the time period the dimension is active.</span></span> <span data-ttu-id="221d0-134">Ühiskasutuse tasandil alistamised ei saa olla piiravamad kui alistamised juriidilise isiku tasandil.</span><span class="sxs-lookup"><span data-stu-id="221d0-134">The overrides at the shared level cannot be more restrictive than the overrides at the legal entity level.</span></span>

<span data-ttu-id="221d0-135">Lisateavet saate lugeda järgmistest teemadest. [Finantsdimensioonid](financial-dimensions.md)
[Täpsemate reegli struktuuride loomine ja määramine](tasks/create-assign-advanced-rule-structures.md)</span><span class="sxs-lookup"><span data-stu-id="221d0-135">For more information, see the following topics: [Financial dimensions](financial-dimensions.md)
[Create and assign advanced rule structures](tasks/create-assign-advanced-rule-structures.md)</span></span>




