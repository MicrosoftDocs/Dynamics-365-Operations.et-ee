---
title: Puhkuse ostu- ja- müügitaotluste töövoo loomine
description: Looge puhkuse ostu- ja müügitaotluste töövoog, et hallata puhkuse ostu- ja müügitaotlusi rakenduses Dynamics 365 Human Resources järjepidevalt.
author: andreabichsel
manager: tfehr
ms.date: 08/20/2020
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
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 4732b5dafc8074c5c59f10f02bbee7e22f51960a
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2021
ms.locfileid: "5116040"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="63414-103">Puhkuse ostu- ja- müügitaotluste töövoo loomine</span><span class="sxs-lookup"><span data-stu-id="63414-103">Create a buy and sell leave request workflow</span></span>

<span data-ttu-id="63414-104">Saate luua töövoo rakenduses Dynamics 365 Human Resources, et järjepidevalt hallata oma puhkuse ostu- ja müügitaotlusi.</span><span class="sxs-lookup"><span data-stu-id="63414-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your buy and sell leave requests.</span></span> <span data-ttu-id="63414-105">Töövoog **Puhkuse ostmine ja müümine** võimaldab teil teha järgmist.</span><span class="sxs-lookup"><span data-stu-id="63414-105">A **Buy and sell leave** workflow lets you:</span></span>

- <span data-ttu-id="63414-106">Ülesannete määratlemine</span><span class="sxs-lookup"><span data-stu-id="63414-106">Define tasks</span></span>
- <span data-ttu-id="63414-107">Määramine, kes peab ülesanded lõpule viima</span><span class="sxs-lookup"><span data-stu-id="63414-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="63414-108">Täpsustamine, kes saab taotlusi kinnitada või tagasi lükata</span><span class="sxs-lookup"><span data-stu-id="63414-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="63414-109">Puhkuse ostu- ja- müügitaotluste töövoo loomine</span><span class="sxs-lookup"><span data-stu-id="63414-109">Create a buy and sell leave request workflow</span></span>

1. <span data-ttu-id="63414-110">Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="63414-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="63414-111">Jaotises **Seadistus** valige suvand **Inimressursside töövood**.</span><span class="sxs-lookup"><span data-stu-id="63414-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="63414-112">Valige suvand **Uus** ja seejärel valige **Puhkuse ostu- ja müügitaotlus**.</span><span class="sxs-lookup"><span data-stu-id="63414-112">Select **New**, and then select **Buy and sell leave request**.</span></span> 

4. <span data-ttu-id="63414-113">Kui kuvatakse teateaken **Kas avada see fail?**, valige käsk **Ava** ja logige oma ettevõtte mandaatidega sisse.</span><span class="sxs-lookup"><span data-stu-id="63414-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="63414-114">Kasutage töövoo redaktorit, et luua puhkusetaotluste jaoks töövoog.</span><span class="sxs-lookup"><span data-stu-id="63414-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="63414-115">Lisateavet töövoogudega töötamise kohta vt teemast [Töövoogude loomise ülevaade](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span><span class="sxs-lookup"><span data-stu-id="63414-115">For more information about working with workflows, see [Create workflows overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="63414-116">Puhkuse- ja puudumistaotluste töövoo andmeelemendid</span><span class="sxs-lookup"><span data-stu-id="63414-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="63414-117">Te saate töövoos puhkuse ostu- ja müügitaotluste tingimuslike või automaatsete kinnituste loomiseks kasutada järgmisi andmeelemente.</span><span class="sxs-lookup"><span data-stu-id="63414-117">You can use the following data elements to create conditional or automatic approvals in workflows for buy and sell leave requests:</span></span>

- <span data-ttu-id="63414-118">**summa**</span><span class="sxs-lookup"><span data-stu-id="63414-118">**Amount**</span></span>
- <span data-ttu-id="63414-119">**Puhkuse ostmise ja müümise poliitika**</span><span class="sxs-lookup"><span data-stu-id="63414-119">**Buy and sell leave policy**</span></span>
- <span data-ttu-id="63414-120">**Ettevõte**</span><span class="sxs-lookup"><span data-stu-id="63414-120">**Company**</span></span>
- <span data-ttu-id="63414-121">**Looja:**</span><span class="sxs-lookup"><span data-stu-id="63414-121">**Created by**</span></span>
- <span data-ttu-id="63414-122">**Loodud kuupäev ja kellaaeg**</span><span class="sxs-lookup"><span data-stu-id="63414-122">**Created date and time**</span></span>
- <span data-ttu-id="63414-123">**Lõppkuupäev**</span><span class="sxs-lookup"><span data-stu-id="63414-123">**End date**</span></span>
- <span data-ttu-id="63414-124">**Puhkuse tüüp**</span><span class="sxs-lookup"><span data-stu-id="63414-124">**Leave type**</span></span>
- <span data-ttu-id="63414-125">**Muutja**</span><span class="sxs-lookup"><span data-stu-id="63414-125">**Modified by**</span></span>
- <span data-ttu-id="63414-126">**Muutmise kuupäev ja kellaaeg**</span><span class="sxs-lookup"><span data-stu-id="63414-126">**Modified date and time**</span></span>
- <span data-ttu-id="63414-127">**Taotluse ID**</span><span class="sxs-lookup"><span data-stu-id="63414-127">**Request ID**</span></span>
- <span data-ttu-id="63414-128">**Alguskuupäev**</span><span class="sxs-lookup"><span data-stu-id="63414-128">**Start date**</span></span>
- <span data-ttu-id="63414-129">**Olek**</span><span class="sxs-lookup"><span data-stu-id="63414-129">**Status**</span></span> 
- <span data-ttu-id="63414-130">**Edastuskuupäev**</span><span class="sxs-lookup"><span data-stu-id="63414-130">**Submission date**</span></span>
- <span data-ttu-id="63414-131">**Esitas**</span><span class="sxs-lookup"><span data-stu-id="63414-131">**Submitted by**</span></span>
- <span data-ttu-id="63414-132">**Inimressursside edastatud**</span><span class="sxs-lookup"><span data-stu-id="63414-132">**Submitted by Human resources**</span></span>
- <span data-ttu-id="63414-133">**Halduri edastatud**</span><span class="sxs-lookup"><span data-stu-id="63414-133">**Submitted by Manager**</span></span>
- <span data-ttu-id="63414-134">**Esitatud järgmise isiku nimel**</span><span class="sxs-lookup"><span data-stu-id="63414-134">**Submitted on behalf**</span></span>
- <span data-ttu-id="63414-135">**Töötaja**</span><span class="sxs-lookup"><span data-stu-id="63414-135">**Worker**</span></span>

## <a name="workflow-examples"></a><span data-ttu-id="63414-136">Töövoo näited</span><span class="sxs-lookup"><span data-stu-id="63414-136">Workflow examples</span></span>

<span data-ttu-id="63414-137">Need näited näitavad, kuidas saate luua erinevat tüüpi töövoo tingimusi, kasutades järgmisi andmeelemente:</span><span class="sxs-lookup"><span data-stu-id="63414-137">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="63414-138">Kasutage automaatses tegevuses suvandeid **Inimressursside edastatud** ja **Halduri edastatud**, et kinnitada automaatselt puhkuse ostu- ja müügitaotlused, mida need rollid töötajate nimel esitavad.</span><span class="sxs-lookup"><span data-stu-id="63414-138">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve buy and sell leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="63414-139">Automaatsete tegevuste kohta lisateabe saamiseks vt teemat [Kinnitusprotsesside konfigureerimine töövoos](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span><span class="sxs-lookup"><span data-stu-id="63414-139">For more information about automatic actions, see [Configure approval processes in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span></span>

- <span data-ttu-id="63414-140">Kasutage tingimuslikus väljavõttes või automaatses tegevuses suvandit **Puhkuse tüüp**, et kontrollida, kuidas töövoog suunab teatud puhkuse tüübiga taotlusi.</span><span class="sxs-lookup"><span data-stu-id="63414-140">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="63414-141">Vt ka</span><span class="sxs-lookup"><span data-stu-id="63414-141">See also</span></span>

[<span data-ttu-id="63414-142">Puhkuste ja puudumiste ülevaade</span><span class="sxs-lookup"><span data-stu-id="63414-142">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)<br>
[<span data-ttu-id="63414-143">Puhkuse ostu ja müügi poliitikate haldamine</span><span class="sxs-lookup"><span data-stu-id="63414-143">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)

