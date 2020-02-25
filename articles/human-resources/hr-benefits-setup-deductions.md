---
title: Mahaarvamiste konfigureerimine
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7ee9e8f3bc0e9027e41d3aa91bd097a3f046cbb4
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008772"
---
# <a name="configure-deductions"></a><span data-ttu-id="d8451-102">Mahaarvamiste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="d8451-102">Configure deductions</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="d8451-103">Kasutage rakenduses Microsoft Dynamics 365 Human Resources mahaarvamisi, et määrata kui palju, kui üldse, arvatakse maha töövõtja palgast iga soodustuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="d8451-103">Use deductions in Microsoft Dynamics 365 Human Resources to determine how much, if any, to deduct from an employee’s paycheck for each benefit.</span></span> <span data-ttu-id="d8451-104">Mahaarvamised on kuupäevapõhised, nii et saate säilitada mahaarvamise teabe kohta ajaloolise kirje.</span><span class="sxs-lookup"><span data-stu-id="d8451-104">Deductions are date effective, so you can keep a historical record of deduction information.</span></span> 

1. <span data-ttu-id="d8451-105">Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Mahaarvamised**.</span><span class="sxs-lookup"><span data-stu-id="d8451-105">In the **Benefits management** workspace, under **Setup**, select **Deductions**.</span></span>

2. <span data-ttu-id="d8451-106">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="d8451-106">Select **New**.</span></span>

3. <span data-ttu-id="d8451-107">Määrake järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="d8451-107">Specify values for the following fields:</span></span>

   | <span data-ttu-id="d8451-108">Väli</span><span class="sxs-lookup"><span data-stu-id="d8451-108">Field</span></span> | <span data-ttu-id="d8451-109">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="d8451-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="d8451-110">Mahaarvamine</span><span class="sxs-lookup"><span data-stu-id="d8451-110">Deduction</span></span> | <span data-ttu-id="d8451-111">Kordumatu ID, mida kasutatakse soodustuse mahaarvamise tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="d8451-111">A unique ID that is used to identify the benefit deduction.</span></span> |
   | <span data-ttu-id="d8451-112">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="d8451-112">Description</span></span> | <span data-ttu-id="d8451-113">Mahaarvamise kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="d8451-113">A description for the deduction.</span></span> |
   | <span data-ttu-id="d8451-114">Jõustunud</span><span class="sxs-lookup"><span data-stu-id="d8451-114">Effective</span></span> | <span data-ttu-id="d8451-115">Alguskuupäev.</span><span class="sxs-lookup"><span data-stu-id="d8451-115">The start date.</span></span> <span data-ttu-id="d8451-116">Vaikeväärtus on praegune süsteemikuupäev.</span><span class="sxs-lookup"><span data-stu-id="d8451-116">The default value is the current system date.</span></span> |
   | <span data-ttu-id="d8451-117">Aegumine</span><span class="sxs-lookup"><span data-stu-id="d8451-117">Expiration</span></span> | <span data-ttu-id="d8451-118">Lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="d8451-118">The end date.</span></span> <span data-ttu-id="d8451-119">Vaikeväärtus on 12/31/2154, mis tähendab, et mitte kunagi.</span><span class="sxs-lookup"><span data-stu-id="d8451-119">The default value is 12/31/2154, which signifies never.</span></span> |
   | <span data-ttu-id="d8451-120">Pealkiri</span><span class="sxs-lookup"><span data-stu-id="d8451-120">Heading</span></span> | <span data-ttu-id="d8451-121">Palgaarvestussüsteemi päise kood, mida kasutatakse palgasoodustuste töötlemisel antud mahaarvamises töövõtja osana mahaarvamisest.</span><span class="sxs-lookup"><span data-stu-id="d8451-121">The heading code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="d8451-122">Seda kasutatakse, kui kasutate kolmanda osapoole palgaarvestuse pakkujat.</span><span class="sxs-lookup"><span data-stu-id="d8451-122">This is used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="d8451-123">Töövõtja palga mahaarvamise viide</span><span class="sxs-lookup"><span data-stu-id="d8451-123">Employee payroll deduction reference</span></span> | <span data-ttu-id="d8451-124">Palgaarvestussüsteemi mahaarvamise kood, mida kasutatakse palgasoodustuste töötlemisel antud mahaarvamises töövõtja osana mahaarvamisest.</span><span class="sxs-lookup"><span data-stu-id="d8451-124">The deduction code from the payroll system that this deduction will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> |
   | <span data-ttu-id="d8451-125">Summa päis</span><span class="sxs-lookup"><span data-stu-id="d8451-125">Amount heading</span></span> | <span data-ttu-id="d8451-126">Palgaarvestussüsteemi päise kood, mida see mahaarvamise summa kasutab palgasoodustuste töötlemisel antud mahaarvamises töövõtja osana mahaarvamisest.</span><span class="sxs-lookup"><span data-stu-id="d8451-126">The heading code from the payroll system that this deduction amount will use for the employee portion of the deduction when processing the benefits to payroll.</span></span> <span data-ttu-id="d8451-127">Seda kasutatakse tavaliselt, kui kasutate kolmanda osapoole palgaarvestuse pakkujat.</span><span class="sxs-lookup"><span data-stu-id="d8451-127">This is normally used when you use a third party payroll provider.</span></span> |
   | <span data-ttu-id="d8451-128">Saab kustutada</span><span class="sxs-lookup"><span data-stu-id="d8451-128">Can delete</span></span> | <span data-ttu-id="d8451-129">Määrab, kas rakenduse Dynamics 365 for Finance and Operations ekspordiväärtus võib põhjustada väärtuse kustutamise palgaarvestussüsteemist.</span><span class="sxs-lookup"><span data-stu-id="d8451-129">Specifies whether an exported value from Dynamics 365 for Finance and Operations can cause the value to be deleted in the payroll system.</span></span> |
   | <span data-ttu-id="d8451-130">Paarisveerud</span><span class="sxs-lookup"><span data-stu-id="d8451-130">Paired columns</span></span> | <span data-ttu-id="d8451-131">Määrab, kas eksportida päis ja mahaarvamise summa seotud külgnevate veergudena palgaarvestuse süsteemi.</span><span class="sxs-lookup"><span data-stu-id="d8451-131">Specifies whether to export heading and deduction amount in paired adjacent columns to the payroll system.</span></span> |
   | <span data-ttu-id="d8451-132">Jõustumiskuupäeva muutmine</span><span class="sxs-lookup"><span data-stu-id="d8451-132">Change effective date</span></span> | <span data-ttu-id="d8451-133">Soodustuse mahaarvamise muudatuse jõustumise kuupäev,</span><span class="sxs-lookup"><span data-stu-id="d8451-133">The date when the benefit deduction change will become effective.</span></span> <span data-ttu-id="d8451-134">Sellel kuupäeval muudab süsteem automaatselt soodustuste mahaarvamist ja uuendab kõiki selle mahaarvamisega seotud soodustuse plaane, kui käitate mahaarvamise muutmise uuendamise töötluse.</span><span class="sxs-lookup"><span data-stu-id="d8451-134">On this date the system will automatically change the benefit deduction and update all benefit plans associated with this deduction, as long as you run Deduction change update processing.</span></span> |
   | <span data-ttu-id="d8451-135">Mahaarvamise muudatus on lõpule viidud</span><span class="sxs-lookup"><span data-stu-id="d8451-135">Deduction change completed</span></span> | <span data-ttu-id="d8451-136">Kui soodustuse mahaarvamise muudatused on mahaarvamise muutmise uuendamise töötlusel lõpule viidud, valitakse automaatselt märkeruut Mahaarvamise muutmine lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="d8451-136">The Deduction change completed check box will be automatically selected once the benefit deduction changes have been completed by Deduction update change processing.</span></span> |
   
4. <span data-ttu-id="d8451-137">Soodustuse määra häälestuse muudatuste jälgimiseks ja säilitamiseks valige suvand **Tegevused** ning seejärel valige suvand **Versioonide haldamine**.</span><span class="sxs-lookup"><span data-stu-id="d8451-137">To track and maintain changes to the benefit rate setup, select **Actions**, and then select **Maintain versions**.</span></span>

5. <span data-ttu-id="d8451-138">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d8451-138">Select **Save**.</span></span> 
