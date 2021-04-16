---
title: Puhkusetaotluse töövoo loomine
description: Looge puhkuse- ja puudumistaotluse töövoog, et hallata puhkusetaotlusi rakenduses Dynamics 365 Human Resources järjepidevalt.
author: andreabichsel
ms.date: 05/08/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 218e5a6fc95e92bb631ee568a79b7dfe05f425e6
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794537"
---
# <a name="create-a-leave-request-workflow"></a><span data-ttu-id="6aca5-103">Puhkusetaotluse töövoo loomine</span><span class="sxs-lookup"><span data-stu-id="6aca5-103">Create a leave request workflow</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="6aca5-104">Saate luua töövoo rakenduses Dynamics 365 Human Resources, et järjepidevalt hallata oma puhkuse- ja puudumistaotlusi.</span><span class="sxs-lookup"><span data-stu-id="6aca5-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your leave and absence requests.</span></span> <span data-ttu-id="6aca5-105">Töövoog **Puhkused ja puudumised** võimaldab teil teha järgmist.</span><span class="sxs-lookup"><span data-stu-id="6aca5-105">A **Leave and absence** workflow lets you:</span></span>

- <span data-ttu-id="6aca5-106">Ülesannete määratlemine</span><span class="sxs-lookup"><span data-stu-id="6aca5-106">Define tasks</span></span>
- <span data-ttu-id="6aca5-107">Määramine, kes peab ülesanded lõpule viima</span><span class="sxs-lookup"><span data-stu-id="6aca5-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="6aca5-108">Täpsustamine, kes saab taotlusi kinnitada või tagasi lükata</span><span class="sxs-lookup"><span data-stu-id="6aca5-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-leave-and-absence-request-workflow"></a><span data-ttu-id="6aca5-109">Puhkuse- ja puudumistaotluste töövoo loomine</span><span class="sxs-lookup"><span data-stu-id="6aca5-109">Create a Leave and absence request workflow</span></span>

1. <span data-ttu-id="6aca5-110">Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="6aca5-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="6aca5-111">Jaotises **Seadistus** valige suvand **Inimressursside töövood**.</span><span class="sxs-lookup"><span data-stu-id="6aca5-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="6aca5-112">Valige suvand **Uus** ja seejärel valige **Puhkuse- ja puudumistaotlus**.</span><span class="sxs-lookup"><span data-stu-id="6aca5-112">Select **New**, and then select **Leave and absence request**.</span></span> 

4. <span data-ttu-id="6aca5-113">Kui kuvatakse teateaken **Kas avada see fail?**, valige käsk **Ava** ja logige oma ettevõtte mandaatidega sisse.</span><span class="sxs-lookup"><span data-stu-id="6aca5-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="6aca5-114">Kasutage töövoo redaktorit, et luua puhkusetaotluste jaoks töövoog.</span><span class="sxs-lookup"><span data-stu-id="6aca5-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="6aca5-115">Lisateavet töövoogudega töötamise kohta vt teemast [Töövoogude loomise ülevaade](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span><span class="sxs-lookup"><span data-stu-id="6aca5-115">For more information about working with workflows, see [Create workflows overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="6aca5-116">Puhkuse- ja puudumistaotluste töövoo andmeelemendid</span><span class="sxs-lookup"><span data-stu-id="6aca5-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="6aca5-117">Te saate töövoos puhkuse- ja puudumistaotluste tingimuslike või automaatsete kinnituste loomiseks kasutada järgmisi andmeelemente.</span><span class="sxs-lookup"><span data-stu-id="6aca5-117">You can use the following data elements to create conditional or automatic approvals in workflows for leave and absence requests:</span></span>

- <span data-ttu-id="6aca5-118">**summa**</span><span class="sxs-lookup"><span data-stu-id="6aca5-118">**Amount**</span></span>
- <span data-ttu-id="6aca5-119">**Kommentaar**</span><span class="sxs-lookup"><span data-stu-id="6aca5-119">**Comment**</span></span>
- <span data-ttu-id="6aca5-120">**Ettevõte**</span><span class="sxs-lookup"><span data-stu-id="6aca5-120">**Company**</span></span>
- <span data-ttu-id="6aca5-121">**Looja**</span><span class="sxs-lookup"><span data-stu-id="6aca5-121">**Created by**</span></span>
- <span data-ttu-id="6aca5-122">**Loodud kuupäev ja kellaaeg**</span><span class="sxs-lookup"><span data-stu-id="6aca5-122">**Created date and time**</span></span>
- <span data-ttu-id="6aca5-123">**Lõppkuupäev**</span><span class="sxs-lookup"><span data-stu-id="6aca5-123">**End date**</span></span>
- <span data-ttu-id="6aca5-124">**Puhkuse tüüp**</span><span class="sxs-lookup"><span data-stu-id="6aca5-124">**Leave type**</span></span>
- <span data-ttu-id="6aca5-125">**Muutja:**</span><span class="sxs-lookup"><span data-stu-id="6aca5-125">**Modified by**</span></span>
- <span data-ttu-id="6aca5-126">**Muutmise kuupäev ja kellaaeg**</span><span class="sxs-lookup"><span data-stu-id="6aca5-126">**Modified date and time**</span></span>
- <span data-ttu-id="6aca5-127">**Põhjuse kood**</span><span class="sxs-lookup"><span data-stu-id="6aca5-127">**Reason code**</span></span>
- <span data-ttu-id="6aca5-128">**Taotluse ID**</span><span class="sxs-lookup"><span data-stu-id="6aca5-128">**Request ID**</span></span>
- <span data-ttu-id="6aca5-129">**Alguskuupäev**</span><span class="sxs-lookup"><span data-stu-id="6aca5-129">**Start date**</span></span>
- <span data-ttu-id="6aca5-130">**Olek**</span><span class="sxs-lookup"><span data-stu-id="6aca5-130">**Status**</span></span> 
- <span data-ttu-id="6aca5-131">**Edastuskuupäev**</span><span class="sxs-lookup"><span data-stu-id="6aca5-131">**Submission date**</span></span>
- <span data-ttu-id="6aca5-132">**Esitas**</span><span class="sxs-lookup"><span data-stu-id="6aca5-132">**Submitted by**</span></span>
- <span data-ttu-id="6aca5-133">**Inimressursside edastatud**</span><span class="sxs-lookup"><span data-stu-id="6aca5-133">**Submitted by Human resources**</span></span>
- <span data-ttu-id="6aca5-134">**Halduri edastatud**</span><span class="sxs-lookup"><span data-stu-id="6aca5-134">**Submitted by Manager**</span></span>
- <span data-ttu-id="6aca5-135">**Esitatud järgmise isiku nimel**</span><span class="sxs-lookup"><span data-stu-id="6aca5-135">**Submitted on behalf**</span></span>
- <span data-ttu-id="6aca5-136">**Töötaja**</span><span class="sxs-lookup"><span data-stu-id="6aca5-136">**Worker**</span></span>
- <span data-ttu-id="6aca5-137">**Töötaja tüüp**</span><span class="sxs-lookup"><span data-stu-id="6aca5-137">**Worker type**</span></span>

<span data-ttu-id="6aca5-138">Need näited näitavad, kuidas saate luua erinevat tüüpi töövoo tingimusi, kasutades järgmisi andmeelemente:</span><span class="sxs-lookup"><span data-stu-id="6aca5-138">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="6aca5-139">Kasutage tingimuslikus väljavõttes suvandit **Põhjusekood**, et suunata põhjusekoodiga **Operatsioon** haiguslehe taotlused inimressursside üksusele, suunates samas kõik muud põhjusekoodid haldurile.</span><span class="sxs-lookup"><span data-stu-id="6aca5-139">Use **Reason code** in a conditional statement to route sick leave requests with the reason code **Surgery** to HR for approval, while routing all other reason codes to the manager.</span></span> <span data-ttu-id="6aca5-140">Tingimuslike väljavõtete kohta lisateabe saamiseks vt teemat [Tingimuslike otsuste konfigureerimine töövoos](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow).</span><span class="sxs-lookup"><span data-stu-id="6aca5-140">For more information about conditional statements, see [Configure conditional decisions in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow).</span></span> 

- <span data-ttu-id="6aca5-141">Kasutage automaatses tegevuses suvandeid **Inimressursside edastatud** ja **Halduri edastatud**, et kinnitada automaatselt puhkusetaotlused, mida need rollid töötajate nimel esitavad.</span><span class="sxs-lookup"><span data-stu-id="6aca5-141">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="6aca5-142">Automaatsete tegevuste kohta lisateabe saamiseks vt teemat [Kinnitusprotsesside konfigureerimine töövoos](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span><span class="sxs-lookup"><span data-stu-id="6aca5-142">For more information about automatic actions, see [Configure approval processes in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span></span>

- <span data-ttu-id="6aca5-143">Kasutage tingimuslikus väljavõttes või automaatses tegevuses suvandit **Puhkuse tüüp**, et kontrollida, kuidas töövoog suunab teatud puhkuse tüübiga taotlusi.</span><span class="sxs-lookup"><span data-stu-id="6aca5-143">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="6aca5-144">Vt ka</span><span class="sxs-lookup"><span data-stu-id="6aca5-144">See also</span></span>

- [<span data-ttu-id="6aca5-145">Puhkuste ja puudumiste ülevaade</span><span class="sxs-lookup"><span data-stu-id="6aca5-145">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]