---
title: Põhjusekoodide häälestamine
description: Dynamics 365 Human Resources kasutab põhjuse koode, et selgitada, miks töövõtja soodustused muutuvad.
author: andreabichsel
manager: tfehr
ms.date: 01/25/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c799a81f38a5dbd5996afbda9529fa83d7fe5cf9
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5468391"
---
# <a name="set-up-reason-codes"></a><span data-ttu-id="d5cfa-103">Põhjusekoodide häälestamine</span><span class="sxs-lookup"><span data-stu-id="d5cfa-103">Set up reason codes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="d5cfa-104">Dynamics 365 Human Resources kasutab põhjuse koode, et selgitada, miks töövõtja soodustused muutuvad.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-104">Dynamics 365 Human Resources uses reason codes to explain why an employee’s benefits are changing.</span></span>

> [!NOTE]
> <span data-ttu-id="d5cfa-105">Alates 2021. jaanuarist migreeritakse põhjusekoodid tööruumi **Personalihaldus** mitte tööruumi **Soodustuste haldus**.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-105">As of January 2021, reason codes are migrating to the **Personnel management** workspace instead of the **Benefits management** workspace.</span></span> <span data-ttu-id="d5cfa-106">Lisateavet vt teemast [Põhjusekoodide käsitsi migreerimine personalihaldusesse](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).</span><span class="sxs-lookup"><span data-stu-id="d5cfa-106">For more information, see [Manually migrate reason codes to Personnel management](hr-benefits-setup-reason-codes.md#manually-migrate-reason-codes-to-personnel-management).</span></span>

## <a name="create-reason-codes"></a><span data-ttu-id="d5cfa-107">Põhjusekoodide loomine</span><span class="sxs-lookup"><span data-stu-id="d5cfa-107">Create reason codes</span></span>

1. <span data-ttu-id="d5cfa-108">Kui teie põhjusekoodid ei ole veel migreeritud valige tööruumis **Personalihaldus** (või tööruumis **Soodustuste haldus**, kui teie põhjusekoodid ei ole veel migreeritud) jaotis **Lingid** ja seejärel valige **Põhjusekoodid**.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-108">In the **Personnel management** workspace (or **Benefits management** workspace if your reason codes haven't yet migrated), select **Links**, and then select **Reason codes**.</span></span>

2. <span data-ttu-id="d5cfa-109">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-109">Select **New**.</span></span>

3. <span data-ttu-id="d5cfa-110">Määrake järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-110">Specify values for the following fields:</span></span>

   | <span data-ttu-id="d5cfa-111">Väli</span><span class="sxs-lookup"><span data-stu-id="d5cfa-111">Field</span></span> | <span data-ttu-id="d5cfa-112">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="d5cfa-112">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="d5cfa-113">**Põhjuse kood**</span><span class="sxs-lookup"><span data-stu-id="d5cfa-113">**Reason code**</span></span> | <span data-ttu-id="d5cfa-114">Kordumatu nimi, et tuvastada põhjus, miks töövõtja muudaks soodustuse plaani registreerimist.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-114">A unique name to identify the reason an employee would change a benefit plan enrollment.</span></span> |
   | <span data-ttu-id="d5cfa-115">**Kirjeldus**</span><span class="sxs-lookup"><span data-stu-id="d5cfa-115">**Description**</span></span> | <span data-ttu-id="d5cfa-116">Põhjuse koodi kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-116">A description of the reason code.</span></span> |

4. <span data-ttu-id="d5cfa-117">Seadke jaotises **Rakendatavad stsenaariumid** suvand **Soodustuste haldus** väärtusele **Jah**.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-117">Under **Applicable scenarios**, set **Benefits management** to **Yes**.</span></span> <span data-ttu-id="d5cfa-118">(Pole kohaldatav, kui põhjusekoode pole veel tööruumi **Personalihaldus** migreeritud.)</span><span class="sxs-lookup"><span data-stu-id="d5cfa-118">(Not applicable if your reason codes haven't yet migrated to the **Personnel management** workspace.)</span></span>

5. <span data-ttu-id="d5cfa-119">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-119">Select **Save**.</span></span>

## <a name="manually-migrate-reason-codes-to-personnel-management"></a><span data-ttu-id="d5cfa-120">Põhjusekoodide käsitsi migreerimine Personalihaldusesse</span><span class="sxs-lookup"><span data-stu-id="d5cfa-120">Manually migrate reason codes to Personnel management</span></span>

<span data-ttu-id="d5cfa-121">Alates 2021. jaanuarist migreeritakse põhjusekoodid tööruumi **Personalihaldus** mitte tööruumi **Soodustuste haldus**.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-121">In January 2021, reason codes are migrating to the **Personnel management** workspace instead of the **Benefits management** workspace.</span></span> <span data-ttu-id="d5cfa-122">Enamik põhjusekoodide andmeid migreeritakse automaatselt teie keskkonda.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-122">Most reason code data will automatically migrate in your environment.</span></span> <span data-ttu-id="d5cfa-123">Mõned põhjusekoodide andmed ei pruugi migreeruda.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-123">Some reason code data might not migrate.</span></span> <span data-ttu-id="d5cfa-124">Näiteks on põhjusekoodide suurim lubatud tähemärkide arv 15 märki, seega ei migreerita ühtegi üle 15-tähemärgilist põhjusekoodi automaatselt.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-124">For example, reason codes now have a 15-character maximum, so any reason codes longer than 15 characters won't migrate automatically.</span></span>

<span data-ttu-id="d5cfa-125">Näete bännerit lehel **Lingid** tööruumis **Soodustuste haldus**, mis teavitab teid migratsioonist ja sellest, kas mõni põhjusekood ei migreerunud.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-125">You'll see a banner on the **Links** page of the **Benefits management** workspace informing you about the migration and whether any reason codes didn't migrate.</span></span>

1. <span data-ttu-id="d5cfa-126">Valige migatsiooni oleku kohta üksikasjade saamiseks **Põhjusekoodid**.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-126">Select **Reason codes** for details about migration status.</span></span>

   <span data-ttu-id="d5cfa-127">[![Põhjuse koodid](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)</span><span class="sxs-lookup"><span data-stu-id="d5cfa-127">[![Reason codes](./media/hr-benefits-setup-reason-codes-link.png)](./media/hr-benefits-setup-reason-codes-link.png)</span></span>

2. <span data-ttu-id="d5cfa-128">Valige põhjusekood, mida ei saanud migreerida.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-128">Select a reason code that failed to migrate.</span></span>

   <span data-ttu-id="d5cfa-129">[![Põhjusekoodi migreerimise olek](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)</span><span class="sxs-lookup"><span data-stu-id="d5cfa-129">[![Reason code migration status](./media/hr-benefits-setup-reason-codes-status.png)](./media/hr-benefits-setup-reason-codes-status.png)</span></span>

3. <span data-ttu-id="d5cfa-130">Valige **Migreeri põhjusekood**.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-130">Select **Migrate reason code**.</span></span>

   <span data-ttu-id="d5cfa-131">[![Migreeri põhjusekood](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)</span><span class="sxs-lookup"><span data-stu-id="d5cfa-131">[![Migrate reason code](./media/hr-benefits-setup-reason-codes-migrate.png)](./media/hr-benefits-setup-reason-codes-migrate.png)</span></span>

4. <span data-ttu-id="d5cfa-132">Teil on paanil **Soodustuse põhjusekoodide migreerimine** kaks võimalust Personalihalduse põhjusekoodi vastendamiseks.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-132">In the **Benefit reason code migration** pane, you have two options for mapping to a Personnel management reason code:</span></span>

   - <span data-ttu-id="d5cfa-133">Olemasoleva põhjusekoodi kasutamiseks Personalihalduses valige üks ripploendist **Kasuta olemasolevat põhjusekoodi**.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-133">To use an existing reason code in Personnel management, choose one from the **Use existing reason code** dropdown.</span></span>
     > [!NOTE]
     > <span data-ttu-id="d5cfa-134">Personalihalduses saate kasutada olemasolevat põhjusekoodi ainult siis, kui mõnda muud Soodustuste halduse põhjusekoodi pole juba sinna migreeritud.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-134">You can only use an existing reason code in Personnel management if another Benefits management reason code hasn't already migrated to it.</span></span>
   - <span data-ttu-id="d5cfa-135">Personalihalduses uue põhjusekoodi loomiseks sisestage uus põhjusekood väljale **Uus põhjusekood** ja seejärel sisestage kirjeldus väljale **Uus kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-135">To create a new reason code in Personnel management, enter a new one in **New reason code**, and then enter a description in **New description**.</span></span>

   <span data-ttu-id="d5cfa-136">[![Personalihalduse põhjusekoodile vastendamine](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)</span><span class="sxs-lookup"><span data-stu-id="d5cfa-136">[![Map to a Personnel management reason code](./media/hr-benefits-setup-reason-codes-mapping.png)](./media/hr-benefits-setup-reason-codes-mapping.png)</span></span>

<span data-ttu-id="d5cfa-137">Kui põhjusekoodid on Personalihaldusse migreeritud, seadistatakse nende kasutamise valiku Soodustuste halduses automaatselt väärtusele **Jah**.</span><span class="sxs-lookup"><span data-stu-id="d5cfa-137">After reason codes migrate to Personnel management, the option for using them in Benefits management is automatically set to **Yes**.</span></span>

<span data-ttu-id="d5cfa-138">[![Põhjusekoodi kasutamine Soodustuste halduses](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)</span><span class="sxs-lookup"><span data-stu-id="d5cfa-138">[![Use reason code in Benefits management](./media/hr-benefits-setup-reason-codes-use.png)](./media/hr-benefits-setup-reason-codes-use.png)</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]