---
title: Mahaarvamiste konfigureerimine
description: Kasutage rakenduses Microsoft Dynamics 365 Human Resources mahaarvamisi, et määrata kui palju, kui üldse, arvatakse maha töövõtja palgast iga soodustuse jaoks.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4fac1624ce3a88b9fb4adcf303860e82f9d9165b
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6055552"
---
# <a name="configure-deductions"></a><span data-ttu-id="7157b-103">Mahaarvamiste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="7157b-103">Configure deductions</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="7157b-104">Kasutage rakenduses Microsoft Dynamics 365 Human Resources mahaarvamisi, et määrata kui palju, kui üldse, arvatakse maha töövõtja palgast iga soodustuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="7157b-104">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="7157b-105">Mahaarvamised on kuupäevapõhised, nii et saate säilitada mahaarvamise teabe kohta ajaloolise kirje.</span><span class="sxs-lookup"><span data-stu-id="7157b-105">Deductions are date-effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="7157b-106">Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Mahaarvamised**.</span><span class="sxs-lookup"><span data-stu-id="7157b-106">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="7157b-107">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="7157b-107">Select **New**.</span></span>

3. <span data-ttu-id="7157b-108">Määrake järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="7157b-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="7157b-109">Väli</span><span class="sxs-lookup"><span data-stu-id="7157b-109">Field</span></span> | <span data-ttu-id="7157b-110">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="7157b-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="7157b-111">**Mahaarvamine**</span><span class="sxs-lookup"><span data-stu-id="7157b-111">**Deduction**</span></span> | <span data-ttu-id="7157b-112">Kordumatu ID, mida kasutatakse soodustuse mahaarvamise tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="7157b-112">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="7157b-113">**Kirjeldus**</span><span class="sxs-lookup"><span data-stu-id="7157b-113">**Description**</span></span> | <span data-ttu-id="7157b-114">Mahaarvamise kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="7157b-114">A description for the deduction.</span></span> |
   | <span data-ttu-id="7157b-115">**Jõustunud**</span><span class="sxs-lookup"><span data-stu-id="7157b-115">**Effective**</span></span> | <span data-ttu-id="7157b-116">Alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="7157b-116">The start date.</span></span> <span data-ttu-id="7157b-117">Vaikeväärtus on praegune süsteemikuupäev.</span><span class="sxs-lookup"><span data-stu-id="7157b-117">The default value is the current system date.</span></span> |
   | <span data-ttu-id="7157b-118">**Aegumine**</span><span class="sxs-lookup"><span data-stu-id="7157b-118">**Expiration**</span></span> | <span data-ttu-id="7157b-119">Lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="7157b-119">The end date.</span></span> <span data-ttu-id="7157b-120">Vaikeväärtus on 12/31/2154, mis tähendab, et mitte kunagi.</span><span class="sxs-lookup"><span data-stu-id="7157b-120">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="7157b-121">**Pealkiri**</span><span class="sxs-lookup"><span data-stu-id="7157b-121">**Heading**</span></span> | <span data-ttu-id="7157b-122">Palgaarvestussüsteemi päise kood, mida kasutatakse palgasoodustuste töötlemisel antud mahaarvamises töövõtja osana mahaarvamisest.</span><span class="sxs-lookup"><span data-stu-id="7157b-122">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="7157b-123">Seda kasutatakse, kui kasutate kolmanda osapoole palgaarvestuse pakkujat.</span><span class="sxs-lookup"><span data-stu-id="7157b-123">This is used when you use a third-party payroll provider.</span></span> |
   | <span data-ttu-id="7157b-124">**Töövõtja palga mahaarvamise viide**</span><span class="sxs-lookup"><span data-stu-id="7157b-124">**Employee payroll deduction reference**</span></span> | <span data-ttu-id="7157b-125">Palgaarvestussüsteemi mahaarvamise kood, mida kasutatakse palgasoodustuste töötlemisel antud mahaarvamises töövõtja osana mahaarvamisest.</span><span class="sxs-lookup"><span data-stu-id="7157b-125">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="7157b-126">**Summa päis**</span><span class="sxs-lookup"><span data-stu-id="7157b-126">**Amount heading**</span></span> | <span data-ttu-id="7157b-127">Palgaarvestussüsteemi päise kood, mida see mahaarvamise summa kasutab palgasoodustuste töötlemisel antud mahaarvamises töövõtja osana mahaarvamisest.</span><span class="sxs-lookup"><span data-stu-id="7157b-127">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="7157b-128">Seda kasutatakse tavaliselt, kui kasutate kolmanda osapoole palgaarvestuse pakkujat.</span><span class="sxs-lookup"><span data-stu-id="7157b-128">This is normally used when you use a third-party payroll provider.</span></span> |
   | <span data-ttu-id="7157b-129">**Saab kustutada**</span><span class="sxs-lookup"><span data-stu-id="7157b-129">**Can delete**</span></span> | <span data-ttu-id="7157b-130">Määrab, kas rakenduse Dynamics 365 for Finance and Operations ekspordiväärtus võib põhjustada väärtuse kustutamise palgaarvestussüsteemist.</span><span class="sxs-lookup"><span data-stu-id="7157b-130">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="7157b-131">**Paarisveerud**</span><span class="sxs-lookup"><span data-stu-id="7157b-131">**Paired columns**</span></span> | <span data-ttu-id="7157b-132">Määrab, kas eksportida päis ja mahaarvamise summa seotud külgnevate veergudena palgaarvestuse süsteemi.</span><span class="sxs-lookup"><span data-stu-id="7157b-132">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="7157b-133">**Jõustumiskuupäeva muutmine**</span><span class="sxs-lookup"><span data-stu-id="7157b-133">**Change effective date**</span></span> | <span data-ttu-id="7157b-134">Soodustuse mahaarvamise muudatuse jõustumise kuupäev,</span><span class="sxs-lookup"><span data-stu-id="7157b-134">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="7157b-135">Sellel kuupäeval muudab süsteem automaatselt soodustuste mahaarvamist ja uuendab kõiki selle mahaarvamisega seotud soodustuse plaane, kui käitate **mahaarvamise muutmise uuendamise** töötluse.</span><span class="sxs-lookup"><span data-stu-id="7157b-135">On this date, the system automatically changes the benefit deduction and updates all benefit plans associated with this deduction, as long as you run **Deduction change update** processing.</span></span> |
   | <span data-ttu-id="7157b-136">**Mahaarvamise muudatus on lõpule viidud**</span><span class="sxs-lookup"><span data-stu-id="7157b-136">**Deduction change completed**</span></span> | <span data-ttu-id="7157b-137">Kui soodustuse mahaarvamise muudatused on **mahaarvamise muutmise uuendamise** töötlusel lõpule viidud, valitakse automaatselt märkeruut Mahaarvamise muutmine lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="7157b-137">The **Deduction change completed** check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="7157b-138">Soodustuse määra häälestuse muudatuste jälgimiseks ja säilitamiseks valige suvand **Tegevused** ning seejärel valige suvand **Versioonide haldamine**.</span><span class="sxs-lookup"><span data-stu-id="7157b-138">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="7157b-139">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="7157b-139">Select **Save**.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]