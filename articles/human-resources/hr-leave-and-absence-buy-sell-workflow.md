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
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 15cedc16fbdbb5d25daa262f094a56bb8fe2f5cc
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892701"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="00ef6-103">Puhkuse ostu- ja- müügitaotluste töövoo loomine</span><span class="sxs-lookup"><span data-stu-id="00ef6-103">Create a buy and sell leave request workflow</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="00ef6-104">Saate luua töövoo rakenduses Dynamics 365 Human Resources, et järjepidevalt hallata oma puhkuse ostu- ja müügitaotlusi.</span><span class="sxs-lookup"><span data-stu-id="00ef6-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your buy and sell leave requests.</span></span> <span data-ttu-id="00ef6-105">Töövoog **Puhkuse ostmine ja müümine** võimaldab teil teha järgmist.</span><span class="sxs-lookup"><span data-stu-id="00ef6-105">A **Buy and sell leave** workflow lets you:</span></span>

- <span data-ttu-id="00ef6-106">Ülesannete määratlemine</span><span class="sxs-lookup"><span data-stu-id="00ef6-106">Define tasks</span></span>
- <span data-ttu-id="00ef6-107">Määramine, kes peab ülesanded lõpule viima</span><span class="sxs-lookup"><span data-stu-id="00ef6-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="00ef6-108">Täpsustamine, kes saab taotlusi kinnitada või tagasi lükata</span><span class="sxs-lookup"><span data-stu-id="00ef6-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="00ef6-109">Puhkuse ostu- ja- müügitaotluste töövoo loomine</span><span class="sxs-lookup"><span data-stu-id="00ef6-109">Create a buy and sell leave request workflow</span></span>

1. <span data-ttu-id="00ef6-110">Lehel **Puhkused ja puudumised** valige vahekaart **Lingid**.</span><span class="sxs-lookup"><span data-stu-id="00ef6-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="00ef6-111">Jaotises **Seadistus** valige suvand **Inimressursside töövood**.</span><span class="sxs-lookup"><span data-stu-id="00ef6-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="00ef6-112">Valige suvand **Uus** ja seejärel valige **Puhkuse ostu- ja müügitaotlus**.</span><span class="sxs-lookup"><span data-stu-id="00ef6-112">Select **New**, and then select **Buy and sell leave request**.</span></span> 

4. <span data-ttu-id="00ef6-113">Kui kuvatakse teateaken **Kas avada see fail?**, valige käsk **Ava** ja logige oma ettevõtte mandaatidega sisse.</span><span class="sxs-lookup"><span data-stu-id="00ef6-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="00ef6-114">Kasutage töövoo redaktorit, et luua puhkusetaotluste jaoks töövoog.</span><span class="sxs-lookup"><span data-stu-id="00ef6-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="00ef6-115">Lisateavet töövoogudega töötamise kohta vt teemast [Töövoogude loomise ülevaade](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)</span><span class="sxs-lookup"><span data-stu-id="00ef6-115">For more information about working with workflows, see [Create workflows overview](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="00ef6-116">Puhkuse- ja puudumistaotluste töövoo andmeelemendid</span><span class="sxs-lookup"><span data-stu-id="00ef6-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="00ef6-117">Te saate töövoos puhkuse ostu- ja müügitaotluste tingimuslike või automaatsete kinnituste loomiseks kasutada järgmisi andmeelemente.</span><span class="sxs-lookup"><span data-stu-id="00ef6-117">You can use the following data elements to create conditional or automatic approvals in workflows for buy and sell leave requests:</span></span>

- <span data-ttu-id="00ef6-118">**summa**</span><span class="sxs-lookup"><span data-stu-id="00ef6-118">**Amount**</span></span>
- <span data-ttu-id="00ef6-119">**Puhkuse ostmise ja müümise poliitika**</span><span class="sxs-lookup"><span data-stu-id="00ef6-119">**Buy and sell leave policy**</span></span>
- <span data-ttu-id="00ef6-120">**Ettevõte**</span><span class="sxs-lookup"><span data-stu-id="00ef6-120">**Company**</span></span>
- <span data-ttu-id="00ef6-121">**Looja:**</span><span class="sxs-lookup"><span data-stu-id="00ef6-121">**Created by**</span></span>
- <span data-ttu-id="00ef6-122">**Loodud kuupäev ja kellaaeg**</span><span class="sxs-lookup"><span data-stu-id="00ef6-122">**Created date and time**</span></span>
- <span data-ttu-id="00ef6-123">**Lõppkuupäev**</span><span class="sxs-lookup"><span data-stu-id="00ef6-123">**End date**</span></span>
- <span data-ttu-id="00ef6-124">**Puhkuse tüüp**</span><span class="sxs-lookup"><span data-stu-id="00ef6-124">**Leave type**</span></span>
- <span data-ttu-id="00ef6-125">**Muutja**</span><span class="sxs-lookup"><span data-stu-id="00ef6-125">**Modified by**</span></span>
- <span data-ttu-id="00ef6-126">**Muutmise kuupäev ja kellaaeg**</span><span class="sxs-lookup"><span data-stu-id="00ef6-126">**Modified date and time**</span></span>
- <span data-ttu-id="00ef6-127">**Taotluse ID**</span><span class="sxs-lookup"><span data-stu-id="00ef6-127">**Request ID**</span></span>
- <span data-ttu-id="00ef6-128">**Alguskuupäev**</span><span class="sxs-lookup"><span data-stu-id="00ef6-128">**Start date**</span></span>
- <span data-ttu-id="00ef6-129">**Olek**</span><span class="sxs-lookup"><span data-stu-id="00ef6-129">**Status**</span></span> 
- <span data-ttu-id="00ef6-130">**Edastuskuupäev**</span><span class="sxs-lookup"><span data-stu-id="00ef6-130">**Submission date**</span></span>
- <span data-ttu-id="00ef6-131">**Esitas**</span><span class="sxs-lookup"><span data-stu-id="00ef6-131">**Submitted by**</span></span>
- <span data-ttu-id="00ef6-132">**Inimressursside edastatud**</span><span class="sxs-lookup"><span data-stu-id="00ef6-132">**Submitted by Human resources**</span></span>
- <span data-ttu-id="00ef6-133">**Halduri edastatud**</span><span class="sxs-lookup"><span data-stu-id="00ef6-133">**Submitted by Manager**</span></span>
- <span data-ttu-id="00ef6-134">**Esitatud järgmise isiku nimel**</span><span class="sxs-lookup"><span data-stu-id="00ef6-134">**Submitted on behalf**</span></span>
- <span data-ttu-id="00ef6-135">**Töötaja**</span><span class="sxs-lookup"><span data-stu-id="00ef6-135">**Worker**</span></span>

## <a name="workflow-examples"></a><span data-ttu-id="00ef6-136">Töövoo näited</span><span class="sxs-lookup"><span data-stu-id="00ef6-136">Workflow examples</span></span>

<span data-ttu-id="00ef6-137">Need näited näitavad, kuidas saate luua erinevat tüüpi töövoo tingimusi, kasutades järgmisi andmeelemente:</span><span class="sxs-lookup"><span data-stu-id="00ef6-137">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="00ef6-138">Kasutage automaatses tegevuses suvandeid **Inimressursside edastatud** ja **Halduri edastatud**, et kinnitada automaatselt puhkuse ostu- ja müügitaotlused, mida need rollid töötajate nimel esitavad.</span><span class="sxs-lookup"><span data-stu-id="00ef6-138">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve buy and sell leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="00ef6-139">Automaatsete tegevuste kohta lisateabe saamiseks vt teemat [Kinnitusprotsesside konfigureerimine töövoos](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="00ef6-139">For more information about automatic actions, see [Configure approval processes in a workflow](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).</span></span>

- <span data-ttu-id="00ef6-140">Kasutage tingimuslikus väljavõttes või automaatses tegevuses suvandit **Puhkuse tüüp**, et kontrollida, kuidas töövoog suunab teatud puhkuse tüübiga taotlusi.</span><span class="sxs-lookup"><span data-stu-id="00ef6-140">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="00ef6-141">Vt ka</span><span class="sxs-lookup"><span data-stu-id="00ef6-141">See also</span></span>

[<span data-ttu-id="00ef6-142">Puhkuste ja puudumiste ülevaade</span><span class="sxs-lookup"><span data-stu-id="00ef6-142">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)<br>
[<span data-ttu-id="00ef6-143">Puhkuse ostu ja müügi poliitikate haldamine</span><span class="sxs-lookup"><span data-stu-id="00ef6-143">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]