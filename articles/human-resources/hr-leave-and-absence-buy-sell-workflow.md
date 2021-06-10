---
title: Puhkuse ostu- ja- müügitaotluste töövoo loomine
description: Looge puhkuse ostu- ja müügitaotluste töövoog, et hallata puhkuse ostu- ja müügitaotlusi rakenduses Dynamics 365 Human Resources järjepidevalt.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5bc31740218e3f171d89debace339dee0177d826
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053967"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="b2a1d-103">Puhkuse ostu- ja- müügitaotluste töövoo loomine</span><span class="sxs-lookup"><span data-stu-id="b2a1d-103">Create a buy and sell leave request workflow</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b2a1d-104">Saate luua töövoo rakenduses Dynamics 365 Human Resources, et järjepidevalt hallata oma puhkuse ostu- ja müügitaotlusi.</span><span class="sxs-lookup"><span data-stu-id="b2a1d-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your buy and sell leave requests.</span></span> <span data-ttu-id="b2a1d-105">Töövoog **Puhkuse ostmine ja müümine** võimaldab teil teha järgmist.</span><span class="sxs-lookup"><span data-stu-id="b2a1d-105">A **Buy and sell leave** workflow lets you:</span></span>

- <span data-ttu-id="b2a1d-106">Ülesannete määratlemine</span><span class="sxs-lookup"><span data-stu-id="b2a1d-106">Define tasks</span></span>
- <span data-ttu-id="b2a1d-107">Määramine, kes peab ülesanded lõpule viima</span><span class="sxs-lookup"><span data-stu-id="b2a1d-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="b2a1d-108">Täpsustamine, kes saab taotlusi kinnitada või tagasi lükata</span><span class="sxs-lookup"><span data-stu-id="b2a1d-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="b2a1d-109">Puhkuse ostu- ja- müügitaotluste töövoo loomine</span><span class="sxs-lookup"><span data-stu-id="b2a1d-109">Create a buy and sell leave request workflow</span></span>

1. <span data-ttu-id="b2a1d-110">Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="b2a1d-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="b2a1d-111">Jaotises **Seadistus** valige suvand **Inimressursside töövood**.</span><span class="sxs-lookup"><span data-stu-id="b2a1d-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="b2a1d-112">Valige suvand **Uus** ja seejärel valige **Puhkuse ostu- ja müügitaotlus**.</span><span class="sxs-lookup"><span data-stu-id="b2a1d-112">Select **New**, and then select **Buy and sell leave request**.</span></span> 

4. <span data-ttu-id="b2a1d-113">Kui kuvatakse teateaken **Kas avada see fail?**, valige käsk **Ava** ja logige oma ettevõtte mandaatidega sisse.</span><span class="sxs-lookup"><span data-stu-id="b2a1d-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="b2a1d-114">Kasutage töövoo redaktorit, et luua puhkusetaotluste jaoks töövoog.</span><span class="sxs-lookup"><span data-stu-id="b2a1d-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="b2a1d-115">Lisateavet töövoogudega töötamise kohta vt teemast [Töövoogude loomise ülevaade](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)</span><span class="sxs-lookup"><span data-stu-id="b2a1d-115">For more information about working with workflows, see [Create workflows overview](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="b2a1d-116">Puhkuse- ja puudumistaotluste töövoo andmeelemendid</span><span class="sxs-lookup"><span data-stu-id="b2a1d-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="b2a1d-117">Te saate töövoos puhkuse ostu- ja müügitaotluste tingimuslike või automaatsete kinnituste loomiseks kasutada järgmisi andmeelemente.</span><span class="sxs-lookup"><span data-stu-id="b2a1d-117">You can use the following data elements to create conditional or automatic approvals in workflows for buy and sell leave requests:</span></span>

- <span data-ttu-id="b2a1d-118">**summa**</span><span class="sxs-lookup"><span data-stu-id="b2a1d-118">**Amount**</span></span>
- <span data-ttu-id="b2a1d-119">**Puhkuse ostmise ja müümise poliitika**</span><span class="sxs-lookup"><span data-stu-id="b2a1d-119">**Buy and sell leave policy**</span></span>
- <span data-ttu-id="b2a1d-120">**Ettevõte**</span><span class="sxs-lookup"><span data-stu-id="b2a1d-120">**Company**</span></span>
- <span data-ttu-id="b2a1d-121">**Looja:**</span><span class="sxs-lookup"><span data-stu-id="b2a1d-121">**Created by**</span></span>
- <span data-ttu-id="b2a1d-122">**Loodud kuupäev ja kellaaeg**</span><span class="sxs-lookup"><span data-stu-id="b2a1d-122">**Created date and time**</span></span>
- <span data-ttu-id="b2a1d-123">**Lõppkuupäev**</span><span class="sxs-lookup"><span data-stu-id="b2a1d-123">**End date**</span></span>
- <span data-ttu-id="b2a1d-124">**Puhkuse tüüp**</span><span class="sxs-lookup"><span data-stu-id="b2a1d-124">**Leave type**</span></span>
- <span data-ttu-id="b2a1d-125">**Muutja**</span><span class="sxs-lookup"><span data-stu-id="b2a1d-125">**Modified by**</span></span>
- <span data-ttu-id="b2a1d-126">**Muutmise kuupäev ja kellaaeg**</span><span class="sxs-lookup"><span data-stu-id="b2a1d-126">**Modified date and time**</span></span>
- <span data-ttu-id="b2a1d-127">**Taotluse ID**</span><span class="sxs-lookup"><span data-stu-id="b2a1d-127">**Request ID**</span></span>
- <span data-ttu-id="b2a1d-128">**Alguskuupäev**</span><span class="sxs-lookup"><span data-stu-id="b2a1d-128">**Start date**</span></span>
- <span data-ttu-id="b2a1d-129">**Olek**</span><span class="sxs-lookup"><span data-stu-id="b2a1d-129">**Status**</span></span> 
- <span data-ttu-id="b2a1d-130">**Edastuskuupäev**</span><span class="sxs-lookup"><span data-stu-id="b2a1d-130">**Submission date**</span></span>
- <span data-ttu-id="b2a1d-131">**Esitas**</span><span class="sxs-lookup"><span data-stu-id="b2a1d-131">**Submitted by**</span></span>
- <span data-ttu-id="b2a1d-132">**Inimressursside edastatud**</span><span class="sxs-lookup"><span data-stu-id="b2a1d-132">**Submitted by Human resources**</span></span>
- <span data-ttu-id="b2a1d-133">**Halduri edastatud**</span><span class="sxs-lookup"><span data-stu-id="b2a1d-133">**Submitted by Manager**</span></span>
- <span data-ttu-id="b2a1d-134">**Esitatud järgmise isiku nimel**</span><span class="sxs-lookup"><span data-stu-id="b2a1d-134">**Submitted on behalf**</span></span>
- <span data-ttu-id="b2a1d-135">**Töötaja**</span><span class="sxs-lookup"><span data-stu-id="b2a1d-135">**Worker**</span></span>

## <a name="workflow-examples"></a><span data-ttu-id="b2a1d-136">Töövoo näited</span><span class="sxs-lookup"><span data-stu-id="b2a1d-136">Workflow examples</span></span>

<span data-ttu-id="b2a1d-137">Need näited näitavad, kuidas saate luua erinevat tüüpi töövoo tingimusi, kasutades järgmisi andmeelemente:</span><span class="sxs-lookup"><span data-stu-id="b2a1d-137">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="b2a1d-138">Kasutage automaatses tegevuses suvandeid **Inimressursside edastatud** ja **Halduri edastatud**, et kinnitada automaatselt puhkuse ostu- ja müügitaotlused, mida need rollid töötajate nimel esitavad.</span><span class="sxs-lookup"><span data-stu-id="b2a1d-138">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve buy and sell leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="b2a1d-139">Automaatsete tegevuste kohta lisateabe saamiseks vt teemat [Kinnitusprotsesside konfigureerimine töövoos](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="b2a1d-139">For more information about automatic actions, see [Configure approval processes in a workflow](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).</span></span>

- <span data-ttu-id="b2a1d-140">Kasutage tingimuslikus väljavõttes või automaatses tegevuses suvandit **Puhkuse tüüp**, et kontrollida, kuidas töövoog suunab teatud puhkuse tüübiga taotlusi.</span><span class="sxs-lookup"><span data-stu-id="b2a1d-140">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="b2a1d-141">Vt ka</span><span class="sxs-lookup"><span data-stu-id="b2a1d-141">See also</span></span>

[<span data-ttu-id="b2a1d-142">Puhkuste ja puudumiste ülevaade</span><span class="sxs-lookup"><span data-stu-id="b2a1d-142">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)<br>
[<span data-ttu-id="b2a1d-143">Puhkuse ostu ja müügi poliitikate haldamine</span><span class="sxs-lookup"><span data-stu-id="b2a1d-143">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]