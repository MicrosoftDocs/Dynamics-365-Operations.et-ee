---
title: Koondplaneerimise töö tühistamine
description: See teema selgitab, kuidas tühistada aktiivne plaanimistöö, mis kasutab sisseehitatud planeerimise funktsioone.
author: ChristianRytt
manager: AnnBe
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 66d5b10e1471b98274d4049df18a2e53873f789a
ms.sourcegitcommit: 92cd55028be556a0bd41b6972c9c6d14b695dfa0
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/10/2020
ms.locfileid: "2947476"
---
# <a name="cancel-a-master-planning-job"></a><span data-ttu-id="1ddf0-103">Koondplaneerimise töö tühistamine</span><span class="sxs-lookup"><span data-stu-id="1ddf0-103">Cancel a master planning job</span></span>

<span data-ttu-id="1ddf0-104">Rakenduses Microsoft Dynamics 365 Supply Chain Managementon koondplaneerimise töö tühistamiseks mitu võimalust.</span><span class="sxs-lookup"><span data-stu-id="1ddf0-104">In Microsoft Dynamics 365 Supply Chain Management, there are multiple options for canceling a master planning job.</span></span> <span data-ttu-id="1ddf0-105">Näiteks võite soovida tühistada koondplaneerimise töö, kui see käivitati kogemata või kui see töötab oodatust kauem ja soovite selle lõpetada.</span><span class="sxs-lookup"><span data-stu-id="1ddf0-105">For example, you may want to cancel a master planning job if it was started by mistake or is running longer than expected and you want to end it.</span></span> <span data-ttu-id="1ddf0-106">Parim viis planeerimise töö tühistamiseks on alates **lõpetamata planeerimise protsesside** leheküljest.</span><span class="sxs-lookup"><span data-stu-id="1ddf0-106">The best way to cancel a planning job is from  the **Unfinished planning processes** page.</span></span> <span data-ttu-id="1ddf0-107">**Pakett-tööde** ja **pakett-tööde täiustatud** lehti tuleks kasutada ainult juhul, kui koondplaneerimise töö tühistamine lehel **lõpetamata planeerimise protsessid** ei ole lõppenud mõne minuti jooksul.</span><span class="sxs-lookup"><span data-stu-id="1ddf0-107">Alternative options from the **Batch jobs** and **Batch jobs enhanced** pages should only be used if canceling the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

## <a name="preferred-cancel-option"></a><span data-ttu-id="1ddf0-108">Eelistatud tühistamise suvand</span><span class="sxs-lookup"><span data-stu-id="1ddf0-108">Preferred cancel option</span></span>
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a><span data-ttu-id="1ddf0-109">Tühista koondplaneerimise töö **lõpetamata planeerimise protsesside** lehelt</span><span class="sxs-lookup"><span data-stu-id="1ddf0-109">Cancel master planning job from **Unfinished planning processes** page</span></span>
1. <span data-ttu-id="1ddf0-110">Avage **Koondplaneerimine > Päringud ja aruanded > Koondplaneerimine > Lõpetamata planeerimise protsessid**.</span><span class="sxs-lookup"><span data-stu-id="1ddf0-110">Go to **Master planning > Inquiries and reports > Master planning > Unfinished planning processes**.</span></span>
2. <span data-ttu-id="1ddf0-111">Valige parandusrida koos planeerimisprotsessiga, mida soovite lõpetada.</span><span class="sxs-lookup"><span data-stu-id="1ddf0-111">Select the line with the planning process that you want to cancel.</span></span>
3. <span data-ttu-id="1ddf0-112">Klõpsake **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="1ddf0-112">Click **Cancel**.</span></span>

## <a name="additional-cancel-options"></a><span data-ttu-id="1ddf0-113">Tühistamise lisavalikud</span><span class="sxs-lookup"><span data-stu-id="1ddf0-113">Additional cancel options</span></span>
<span data-ttu-id="1ddf0-114">Neid tohib kasutada ainult juhul, kui **lõpetamata planeerimise protsesside** lehelt tühistatud planeerimistöid ei lõpetatud mõne minuti jooksul.</span><span class="sxs-lookup"><span data-stu-id="1ddf0-114">These should only be used iif cancelin the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a><span data-ttu-id="1ddf0-115">Koondplaneerimise töö kustutamine **pakett-tööde** lehelt</span><span class="sxs-lookup"><span data-stu-id="1ddf0-115">Delete master planning job from the **Batch jobs** page</span></span>
1. <span data-ttu-id="1ddf0-116">Avage **Süsteemihaldus > Päringud > Pakett-tööd**.</span><span class="sxs-lookup"><span data-stu-id="1ddf0-116">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="1ddf0-117">Valige rida koos planeerimistööga, mida soovite lõpetada.</span><span class="sxs-lookup"><span data-stu-id="1ddf0-117">Select the line with the planning job that you want to delete.</span></span>
3. <span data-ttu-id="1ddf0-118">Klõpsake  **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="1ddf0-118">Click **Delete**.</span></span>

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a><span data-ttu-id="1ddf0-119">Koondplaneerimise töö kustutamine **pakett-tööde täiustatud** lehelt</span><span class="sxs-lookup"><span data-stu-id="1ddf0-119">Abort master planning job task from the **Batch jobs enhanced** page</span></span>
1. <span data-ttu-id="1ddf0-120">Avage **Süsteemihaldus > Päringud > Pakett-tööd**.</span><span class="sxs-lookup"><span data-stu-id="1ddf0-120">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="1ddf0-121">Kui töö ID-d loendis ei kuvata, klõpsake käsku **Aktiveeri täiustatud vormile**, muul juhul jätkake järgmise juhisega.</span><span class="sxs-lookup"><span data-stu-id="1ddf0-121">If the job ID is not shown in the list, click **Switch to enhanced form**, otherwise proceed with the next step.</span></span>
3. <span data-ttu-id="1ddf0-122">Avage pakett-töö.</span><span class="sxs-lookup"><span data-stu-id="1ddf0-122">Open the batch job.</span></span> <span data-ttu-id="1ddf0-123">Klõpsake **töö ID** -d pakett-töö jaoks, mille ülesandeid soovite lõpetada.</span><span class="sxs-lookup"><span data-stu-id="1ddf0-123">Click the **Job ID** for the batch job with tasks that you want to end.</span></span>
4. <span data-ttu-id="1ddf0-124">Valige **pakett-töö**-s ülesanded, mida soovite lõpetada.</span><span class="sxs-lookup"><span data-stu-id="1ddf0-124">In **Batch tasks**, select the tasks to end.</span></span>
5. <span data-ttu-id="1ddf0-125">Klõpsake **partii ülesanded** kiirvalikul nuppu **Katkesta**.</span><span class="sxs-lookup"><span data-stu-id="1ddf0-125">On the **Batch tasks** FastTab, click **Abort**.</span></span>