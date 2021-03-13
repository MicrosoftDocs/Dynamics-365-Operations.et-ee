---
title: Puhkusetaotluse töövoo loomine
description: Looge puhkuse- ja puudumistaotluse töövoog, et hallata puhkusetaotlusi rakenduses Dynamics 365 Human Resources järjepidevalt.
author: andreabichsel
manager: tfehr
ms.date: 05/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e1907ca9cc578737341e52f89453e3d6ae3d0bec
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115048"
---
# <a name="create-a-leave-request-workflow"></a><span data-ttu-id="e7147-103">Puhkusetaotluse töövoo loomine</span><span class="sxs-lookup"><span data-stu-id="e7147-103">Create a leave request workflow</span></span>

<span data-ttu-id="e7147-104">Saate luua töövoo rakenduses Dynamics 365 Human Resources, et järjepidevalt hallata oma puhkuse- ja puudumistaotlusi.</span><span class="sxs-lookup"><span data-stu-id="e7147-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your leave and absence requests.</span></span> <span data-ttu-id="e7147-105">Töövoog **Puhkused ja puudumised** võimaldab teil teha järgmist.</span><span class="sxs-lookup"><span data-stu-id="e7147-105">A **Leave and absence** workflow lets you:</span></span>

- <span data-ttu-id="e7147-106">Ülesannete määratlemine</span><span class="sxs-lookup"><span data-stu-id="e7147-106">Define tasks</span></span>
- <span data-ttu-id="e7147-107">Määramine, kes peab ülesanded lõpule viima</span><span class="sxs-lookup"><span data-stu-id="e7147-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="e7147-108">Täpsustamine, kes saab taotlusi kinnitada või tagasi lükata</span><span class="sxs-lookup"><span data-stu-id="e7147-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-leave-and-absence-request-workflow"></a><span data-ttu-id="e7147-109">Puhkuse- ja puudumistaotluste töövoo loomine</span><span class="sxs-lookup"><span data-stu-id="e7147-109">Create a Leave and absence request workflow</span></span>

1. <span data-ttu-id="e7147-110">Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="e7147-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="e7147-111">Jaotises **Seadistus** valige suvand **Inimressursside töövood**.</span><span class="sxs-lookup"><span data-stu-id="e7147-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="e7147-112">Valige suvand **Uus** ja seejärel valige **Puhkuse- ja puudumistaotlus**.</span><span class="sxs-lookup"><span data-stu-id="e7147-112">Select **New**, and then select **Leave and absence request**.</span></span> 

4. <span data-ttu-id="e7147-113">Kui kuvatakse teateaken **Kas avada see fail?**, valige käsk **Ava** ja logige oma ettevõtte mandaatidega sisse.</span><span class="sxs-lookup"><span data-stu-id="e7147-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="e7147-114">Kasutage töövoo redaktorit, et luua puhkusetaotluste jaoks töövoog.</span><span class="sxs-lookup"><span data-stu-id="e7147-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="e7147-115">Lisateavet töövoogudega töötamise kohta vt teemast [Töövoogude loomise ülevaade](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span><span class="sxs-lookup"><span data-stu-id="e7147-115">For more information about working with workflows, see [Create workflows overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="e7147-116">Puhkuse- ja puudumistaotluste töövoo andmeelemendid</span><span class="sxs-lookup"><span data-stu-id="e7147-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="e7147-117">Te saate töövoos puhkuse- ja puudumistaotluste tingimuslike või automaatsete kinnituste loomiseks kasutada järgmisi andmeelemente.</span><span class="sxs-lookup"><span data-stu-id="e7147-117">You can use the following data elements to create conditional or automatic approvals in workflows for leave and absence requests:</span></span>

- <span data-ttu-id="e7147-118">**summa**</span><span class="sxs-lookup"><span data-stu-id="e7147-118">**Amount**</span></span>
- <span data-ttu-id="e7147-119">**Kommentaar**</span><span class="sxs-lookup"><span data-stu-id="e7147-119">**Comment**</span></span>
- <span data-ttu-id="e7147-120">**Ettevõte**</span><span class="sxs-lookup"><span data-stu-id="e7147-120">**Company**</span></span>
- <span data-ttu-id="e7147-121">**Looja**</span><span class="sxs-lookup"><span data-stu-id="e7147-121">**Created by**</span></span>
- <span data-ttu-id="e7147-122">**Loodud kuupäev ja kellaaeg**</span><span class="sxs-lookup"><span data-stu-id="e7147-122">**Created date and time**</span></span>
- <span data-ttu-id="e7147-123">**Lõppkuupäev**</span><span class="sxs-lookup"><span data-stu-id="e7147-123">**End date**</span></span>
- <span data-ttu-id="e7147-124">**Puhkuse tüüp**</span><span class="sxs-lookup"><span data-stu-id="e7147-124">**Leave type**</span></span>
- <span data-ttu-id="e7147-125">**Muutja:**</span><span class="sxs-lookup"><span data-stu-id="e7147-125">**Modified by**</span></span>
- <span data-ttu-id="e7147-126">**Muutmise kuupäev ja kellaaeg**</span><span class="sxs-lookup"><span data-stu-id="e7147-126">**Modified date and time**</span></span>
- <span data-ttu-id="e7147-127">**Põhjuse kood**</span><span class="sxs-lookup"><span data-stu-id="e7147-127">**Reason code**</span></span>
- <span data-ttu-id="e7147-128">**Taotluse ID**</span><span class="sxs-lookup"><span data-stu-id="e7147-128">**Request ID**</span></span>
- <span data-ttu-id="e7147-129">**Alguskuupäev**</span><span class="sxs-lookup"><span data-stu-id="e7147-129">**Start date**</span></span>
- <span data-ttu-id="e7147-130">**Olek**</span><span class="sxs-lookup"><span data-stu-id="e7147-130">**Status**</span></span> 
- <span data-ttu-id="e7147-131">**Edastuskuupäev**</span><span class="sxs-lookup"><span data-stu-id="e7147-131">**Submission date**</span></span>
- <span data-ttu-id="e7147-132">**Esitas**</span><span class="sxs-lookup"><span data-stu-id="e7147-132">**Submitted by**</span></span>
- <span data-ttu-id="e7147-133">**Inimressursside edastatud**</span><span class="sxs-lookup"><span data-stu-id="e7147-133">**Submitted by Human resources**</span></span>
- <span data-ttu-id="e7147-134">**Halduri edastatud**</span><span class="sxs-lookup"><span data-stu-id="e7147-134">**Submitted by Manager**</span></span>
- <span data-ttu-id="e7147-135">**Esitatud järgmise isiku nimel**</span><span class="sxs-lookup"><span data-stu-id="e7147-135">**Submitted on behalf**</span></span>
- <span data-ttu-id="e7147-136">**Töötaja**</span><span class="sxs-lookup"><span data-stu-id="e7147-136">**Worker**</span></span>
- <span data-ttu-id="e7147-137">**Töötaja tüüp**</span><span class="sxs-lookup"><span data-stu-id="e7147-137">**Worker type**</span></span>

<span data-ttu-id="e7147-138">Need näited näitavad, kuidas saate luua erinevat tüüpi töövoo tingimusi, kasutades järgmisi andmeelemente:</span><span class="sxs-lookup"><span data-stu-id="e7147-138">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="e7147-139">Kasutage tingimuslikus väljavõttes suvandit **Põhjusekood**, et suunata põhjusekoodiga **Operatsioon** haiguslehe taotlused inimressursside üksusele, suunates samas kõik muud põhjusekoodid haldurile.</span><span class="sxs-lookup"><span data-stu-id="e7147-139">Use **Reason code** in a conditional statement to route sick leave requests with the reason code **Surgery** to HR for approval, while routing all other reason codes to the manager.</span></span> <span data-ttu-id="e7147-140">Tingimuslike väljavõtete kohta lisateabe saamiseks vt teemat [Tingimuslike otsuste konfigureerimine töövoos](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow).</span><span class="sxs-lookup"><span data-stu-id="e7147-140">For more information about conditional statements, see [Configure conditional decisions in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow).</span></span> 

- <span data-ttu-id="e7147-141">Kasutage automaatses tegevuses suvandeid **Inimressursside edastatud** ja **Halduri edastatud**, et kinnitada automaatselt puhkusetaotlused, mida need rollid töötajate nimel esitavad.</span><span class="sxs-lookup"><span data-stu-id="e7147-141">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="e7147-142">Automaatsete tegevuste kohta lisateabe saamiseks vt teemat [Kinnitusprotsesside konfigureerimine töövoos](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span><span class="sxs-lookup"><span data-stu-id="e7147-142">For more information about automatic actions, see [Configure approval processes in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span></span>

- <span data-ttu-id="e7147-143">Kasutage tingimuslikus väljavõttes või automaatses tegevuses suvandit **Puhkuse tüüp**, et kontrollida, kuidas töövoog suunab teatud puhkuse tüübiga taotlusi.</span><span class="sxs-lookup"><span data-stu-id="e7147-143">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="e7147-144">Vt ka</span><span class="sxs-lookup"><span data-stu-id="e7147-144">See also</span></span>

- [<span data-ttu-id="e7147-145">Puhkuste ja puudumiste ülevaade</span><span class="sxs-lookup"><span data-stu-id="e7147-145">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
