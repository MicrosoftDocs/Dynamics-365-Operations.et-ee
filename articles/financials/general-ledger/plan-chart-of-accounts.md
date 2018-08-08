---
title: Kontoplaanide plaanimine
description: Selles teemas antakse teavet, mis aitab teil planeerida organisatsiooni kontoplaane.
author: aprilolson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DimensionConfigureAccountStructure, LedgerChartOfAccounts
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 14051
ms.assetid: 10edb129-33f0-4cf9-b2a7-4b7ffa09b229
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 93d5ef19a4b1cb2885c611c8675ac06fd841ac56
ms.contentlocale: et-ee
ms.lasthandoff: 08/07/2018

---

# <a name="plan-your-chart-of-accounts"></a><span data-ttu-id="955e9-103">Kontoplaanide plaanimine</span><span class="sxs-lookup"><span data-stu-id="955e9-103">Plan your chart of accounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="955e9-104">Selles teemas antakse teavet, mis aitab teil planeerida organisatsiooni kontoplaane.</span><span class="sxs-lookup"><span data-stu-id="955e9-104">This topic provides information that will help you plan the chart of accounts for your organization.</span></span>

<span data-ttu-id="955e9-105">Organisatsiooni finantsteabe jälgimiseks ja säilitamiseks saate seadistada kontoplaani.</span><span class="sxs-lookup"><span data-stu-id="955e9-105">To track and maintain financial information in an organization, you can set up a chart of accounts.</span></span> <span data-ttu-id="955e9-106">Kontoplaan on finantsraamistikku määratlevate kontode kogum.</span><span class="sxs-lookup"><span data-stu-id="955e9-106">A chart of accounts is a collection of accounts that define a financial framework.</span></span> <span data-ttu-id="955e9-107">Nende kontode kannete edasiseks jälgimiseks saate lisada segmente.</span><span class="sxs-lookup"><span data-stu-id="955e9-107">To further track the transactions in these accounts, you can add segments.</span></span> <span data-ttu-id="955e9-108">Neid segmente nimetatakse finantsdimensioonideks.</span><span class="sxs-lookup"><span data-stu-id="955e9-108">These segments are known as financial dimensions.</span></span> <span data-ttu-id="955e9-109">Näiteks võib kulukonto sisaldada finantsdimensioone nimedega Osakond, Kulukeskus ja Eesmärk.</span><span class="sxs-lookup"><span data-stu-id="955e9-109">For example, an expense account might include financial dimensions that are named Department, Cost center, and Purpose.</span></span> <span data-ttu-id="955e9-110">Kasutaja määratud reeglid määravad, kuidas finantsdimensioonid on seotud põhikontode ja muude finantsdimensioonidega ning kuidas kandeid sisestatakse.</span><span class="sxs-lookup"><span data-stu-id="955e9-110">User-defined rules determine how financial dimensions are attached to the main accounts and to other financial dimensions, and also how transactions are entered.</span></span> <span data-ttu-id="955e9-111">Neid kasutaja määratud reegleid nimetatakse konto struktuurideks ja täpsemateks reegliteks.</span><span class="sxs-lookup"><span data-stu-id="955e9-111">These user-defined rules are known as account structures and advanced rules.</span></span>

<span data-ttu-id="955e9-112">Kontoplaan on juriidilise isiku pearaamatukontode struktureeritud loend.</span><span class="sxs-lookup"><span data-stu-id="955e9-112">The chart of accounts is a structured list of a legal entity's general ledger accounts.</span></span> <span data-ttu-id="955e9-113">Seda loendit kasutatakse ametivõimudele ja omanikele finantsaruannete ettevalmistamiseks.</span><span class="sxs-lookup"><span data-stu-id="955e9-113">The list is used to prepare financial reports for authorities and owners.</span></span> <span data-ttu-id="955e9-114">Kontod grupeeritakse kõigepealt kontotüüpide järgi ja seejärel koondatakse suurematesse kategooriatesse.</span><span class="sxs-lookup"><span data-stu-id="955e9-114">The accounts are first grouped into types of accounts and then further aggregated into larger categories.</span></span> <span data-ttu-id="955e9-115">Kõige üldisemal tasandil on kontod grupeeritud tulude ja kuludena (kasutusel olevad kontod) ning varade ja kohustustena (bilansikontod).</span><span class="sxs-lookup"><span data-stu-id="955e9-115">At the most general level, the accounts are grouped as revenues and costs (operating accounts), and assets and liabilities (balance accounts).</span></span>

<span data-ttu-id="955e9-116">Kontoplaani saavad jagada ja kasutada kõik organisatsiooni juriidilised isikud.</span><span class="sxs-lookup"><span data-stu-id="955e9-116">A chart of accounts can be shared and used by any legal entity in an organization.</span></span> <span data-ttu-id="955e9-117">Kontoplaan, mida juriidiline isik kasutab, on määratletud lehel **Pearaamat**.</span><span class="sxs-lookup"><span data-stu-id="955e9-117">The chart of accounts that is used by a legal entity is defined on the **Ledger** page.</span></span>

<span data-ttu-id="955e9-118">Järgmiselt on toodud mõni tegur, millega peate oma organisatsiooni kontoplaani struktuuri plaanimisel arvestama.</span><span class="sxs-lookup"><span data-stu-id="955e9-118">Here are some of the factors that you must consider when you plan the structure of the chart of accounts for your organization:</span></span>

- <span data-ttu-id="955e9-119">Organisatsiooni riigi või regiooni aruandluse nõuded</span><span class="sxs-lookup"><span data-stu-id="955e9-119">The reporting requirements of the country or region where your organization is based</span></span>
- <span data-ttu-id="955e9-120">Teie juriidilise isiku aruandluse nõuded</span><span class="sxs-lookup"><span data-stu-id="955e9-120">The reporting requirements of your legal entity</span></span>
- <span data-ttu-id="955e9-121">Nõutav üksikasjalik täpsustustase nii muude organisatsioonide kui ka teie organisatsiooni jaoks</span><span class="sxs-lookup"><span data-stu-id="955e9-121">The degree of specification that is required, both for both external organizations and for your organization</span></span>

<span data-ttu-id="955e9-122">Saate luua kontoplaani lehel **Kontoplaan**.</span><span class="sxs-lookup"><span data-stu-id="955e9-122">You create the chart of accounts on the **Chart of accounts** page.</span></span> <span data-ttu-id="955e9-123">Saate luua põhikontosid lehel **Kontoplaan** või lehel **Põhikontod**.</span><span class="sxs-lookup"><span data-stu-id="955e9-123">You can create main accounts from the **Chart of accounts** page or the **Main accounts** page.</span></span> <span data-ttu-id="955e9-124">Põhikontodel ei tohiks kasutada erimärke, mida kasutatakse kontoplaani eraldajatena.</span><span class="sxs-lookup"><span data-stu-id="955e9-124">Your main accounts shouldn't use any special characters that are used as delimiters for chart of accounts.</span></span> <span data-ttu-id="955e9-125">Vastasel juhul võib konto ja dimensiooni kombinatsioonide sisestamisel ilmneda ebastabiilsus või vajalik olla alati otsingute või dialoogiboksi kasutamine.</span><span class="sxs-lookup"><span data-stu-id="955e9-125">Otherwise, you might experience instability, or you might always have to use lookups or the dialog box when you enter combinations of accounts and dimensions.</span></span> <span data-ttu-id="955e9-126">Lisateabe jaoks vt [Põhikonto loomine](tasks/create-main-account.md).</span><span class="sxs-lookup"><span data-stu-id="955e9-126">For more information, see [Create a main account](tasks/create-main-account.md).</span></span>

> [!NOTE]
> <span data-ttu-id="955e9-127">Rakenduse Microsoft Dynamics for Finance and Operations versioonis 8.0 (aprill 2018) saate muuta kontoplaani eraldajat lehel **Üldised pearaamatu parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="955e9-127">In Microsoft Dynamics for Finance and Operations version 8.0 (April 2018), you can modify the chart of accounts delimiter from the **General ledger parameters** page.</span></span>

<span data-ttu-id="955e9-128">Soovitatav on siduda põhikontod põhikonto kategooriatega, nii et saate kasutada vaikimisi finantsaruandeid ega pea muudatusi tegema.</span><span class="sxs-lookup"><span data-stu-id="955e9-128">It's a good idea to link the main accounts to main account categories, so that you can take advantage of the default financial reports without having to make any modifications.</span></span> <span data-ttu-id="955e9-129">Seetõttu saate aruandeid kiiremini ja hõlpsamini kujundada ja säilitada.</span><span class="sxs-lookup"><span data-stu-id="955e9-129">Therefore, you can more quickly and easily design and maintain reports.</span></span>

<span data-ttu-id="955e9-130">Saate luua konto struktuure lehel **Konto struktuuride konfigureerimine**.</span><span class="sxs-lookup"><span data-stu-id="955e9-130">You create account structures on the **Configure account structures** page.</span></span> <span data-ttu-id="955e9-131">Konto struktuurid määratlevad kehtivaid kombinatsioone.</span><span class="sxs-lookup"><span data-stu-id="955e9-131">Account structures define valid combinations.</span></span> <span data-ttu-id="955e9-132">Need kombinatsioonid koos põhikontodega moodustavad kontoplaani.</span><span class="sxs-lookup"><span data-stu-id="955e9-132">These combinations, together with main accounts, form a chart of accounts.</span></span> <span data-ttu-id="955e9-133">Lisateabe jaoks vt [Konto struktuuride loomine](tasks/create-account-structures.md).</span><span class="sxs-lookup"><span data-stu-id="955e9-133">For more information, see [Create account structures](tasks/create-account-structures.md).</span></span>

<span data-ttu-id="955e9-134">**Juriidilise isiku alistamised**</span><span class="sxs-lookup"><span data-stu-id="955e9-134">**Legal entity overrides**</span></span>

<span data-ttu-id="955e9-135">Kõik põhikontod ei kehti kõikide juriidiliste isikute puhul ja mõni põhikonto võib olla asjakohased ainult konkreetse perioodi puhul.</span><span class="sxs-lookup"><span data-stu-id="955e9-135">Not all main accounts are valid for all legal entities, and some main account might be relevant only for a specific period.</span></span> <span data-ttu-id="955e9-136">Sel juhul saab kasutada jaotist **Juriidilise isiku tühistamised** tuvastamiseks, milliste ettevõtete põhikonto tuleks peatada, kes on omanik ja mis ajaperioodil on dimensioon aktiivne.</span><span class="sxs-lookup"><span data-stu-id="955e9-136">In this scenario, you can use the **Legal entity overrides** section to identify the companies that the main account should be suspended for, the owner, and the period when the dimension is active.</span></span> <span data-ttu-id="955e9-137">Ühiskasutuse tasandil alistamised ei saa olla piiravamad kui alistamised juriidilise isiku tasandil.</span><span class="sxs-lookup"><span data-stu-id="955e9-137">The overrides at the shared level can't be more restrictive than the overrides at the legal entity level.</span></span>

<span data-ttu-id="955e9-138">Lisateavet vt järgmistest teemadest:</span><span class="sxs-lookup"><span data-stu-id="955e9-138">For more information, see the following topics:</span></span>

- [<span data-ttu-id="955e9-139">Finantsdimensioonid</span><span class="sxs-lookup"><span data-stu-id="955e9-139">Financial dimensions</span></span>](financial-dimensions.md)
- [<span data-ttu-id="955e9-140">Täpsemate reeglistruktuuride loomine ja määramine</span><span class="sxs-lookup"><span data-stu-id="955e9-140">Create and assign advanced rule structures</span></span>](tasks/create-assign-advanced-rule-structures.md)

