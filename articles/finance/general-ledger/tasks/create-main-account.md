---
title: Põhikonto loomine
description: See ülesandejuhend kirjeldab olemasolevale kontoplaanile põhikonto lisamise etappe.
author: aprilolson
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: MainAccount, CompanyInfoList
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f1d1bfe358bbff1720e7d013c3bfeaba1a598ed0
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5216469"
---
# <a name="create-a-main-account"></a><span data-ttu-id="7b113-103">Põhikonto loomine</span><span class="sxs-lookup"><span data-stu-id="7b113-103">Create a main account</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7b113-104">See ülesandejuhend kirjeldab olemasolevale kontoplaanile põhikonto lisamise etappe.</span><span class="sxs-lookup"><span data-stu-id="7b113-104">This task guide steps through adding a main account to an existing chart of accounts.</span></span> <span data-ttu-id="7b113-105">Salvestamisel kasutatakse demoettevõtte USMF-i.</span><span class="sxs-lookup"><span data-stu-id="7b113-105">This recording uses the USMF demo company.</span></span>  

1. <span data-ttu-id="7b113-106">Avage **Navigeerimispaan > Moodulid > Pearaamat > Kontoplaan > Kontdd > Põhikontod**.</span><span class="sxs-lookup"><span data-stu-id="7b113-106">Go to **Navigation pane > Modules > General ledger > Chart of accounts > Accounts > Main accounts**.</span></span>
2. <span data-ttu-id="7b113-107">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="7b113-107">Click **New**.</span></span>
3. <span data-ttu-id="7b113-108">Sisestage väärtus väljale **Põhikonto**.</span><span class="sxs-lookup"><span data-stu-id="7b113-108">In the **Main account** field, type a value.</span></span>
4. <span data-ttu-id="7b113-109">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="7b113-109">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="7b113-110">Väljal **Põhikonto tüüp** valige kontode saldot ja asukohta finantsaruannetes kõige paremini kirjeldav tüüp.</span><span class="sxs-lookup"><span data-stu-id="7b113-110">In the **Main account type** field, select the type that best represents the accounts balance and location on financial statements.</span></span>
6. <span data-ttu-id="7b113-111">Valige loendist kontokategooria, millesse põhikonto kuulub.</span><span class="sxs-lookup"><span data-stu-id="7b113-111">In the list, select the account category the main account belongs to.</span></span> <span data-ttu-id="7b113-112">Kontokategooriat kasutatakse vaikefinantsaruannete ja Power BI armatuurlaua sisu jaoks.</span><span class="sxs-lookup"><span data-stu-id="7b113-112">Account category is used for default financial reports and Power BI dashboard content.</span></span>  
7. <span data-ttu-id="7b113-113">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="7b113-113">In the list, click the link in the selected row.</span></span> <span data-ttu-id="7b113-114">Saate muuta deebet- või kreeditsaldo vaikeväärtust.</span><span class="sxs-lookup"><span data-stu-id="7b113-114">Change the default debit or credit balance.</span></span>  
8. <span data-ttu-id="7b113-115">Väljal **Vaikevaluuta** valige valuutade loendist soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="7b113-115">In the **Default currency** field, select a value from the list of currencies.</span></span>
9. <span data-ttu-id="7b113-116">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="7b113-116">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="7b113-117">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="7b113-117">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="7b113-118">Lülitage ümber jaotise **Juriidilise isiku tühistamised** laienduses.</span><span class="sxs-lookup"><span data-stu-id="7b113-118">Toggle the expansion of the **Legal entity overrides** section.</span></span>
12. <span data-ttu-id="7b113-119">Juriidilise isiku valimiseks klõpsake **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="7b113-119">Click **Add** to select a legal entity.</span></span>
13. <span data-ttu-id="7b113-120">Valige loendist suvand Juriidiline isik.</span><span class="sxs-lookup"><span data-stu-id="7b113-120">In the list, select the Legal entity.</span></span>
14. <span data-ttu-id="7b113-121">Klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="7b113-121">Click **Add**.</span></span>
15. <span data-ttu-id="7b113-122">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="7b113-122">In the list, mark the selected row.</span></span>
16. <span data-ttu-id="7b113-123">Märkige või tühjendage märkeruut **Peatatud**.</span><span class="sxs-lookup"><span data-stu-id="7b113-123">Check or uncheck the **Suspended** checkbox.</span></span>
17. <span data-ttu-id="7b113-124">Laiendage jaotist **Rahanduse aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="7b113-124">Expand the **Financial reporting** section.</span></span>
18. <span data-ttu-id="7b113-125">Klõpsake väljal **Vahetuskursi tüüp** otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="7b113-125">In the **Exchange rate type** field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="7b113-126">Valige loendist **Konto vahetuskursi tüüp**.</span><span class="sxs-lookup"><span data-stu-id="7b113-126">In the list, select the **Exchange rate type for the account**.</span></span>
20. <span data-ttu-id="7b113-127">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="7b113-127">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="7b113-128">Väljal **Valuutateisenduse tüüp** valige konto vahetuskursside arvutamise meetod.</span><span class="sxs-lookup"><span data-stu-id="7b113-128">In the **Currency translation type** field, select the method for calculating exchange rates for the account.</span></span>
22. <span data-ttu-id="7b113-129">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="7b113-129">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]