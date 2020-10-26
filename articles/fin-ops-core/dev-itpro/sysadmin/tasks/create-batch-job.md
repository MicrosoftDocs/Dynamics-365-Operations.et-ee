---
title: Pakktöö loomine
description: Pakett-töö on tööülesannete grupp, mis on edastatud rakendusobjekti serveri (AOS) eksemplarile automaatseks töötluseks.
author: maertenm
manager: AnnBe
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4903724adc9deaa40b6cd04c215273dd4b0522d4
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982522"
---
# <a name="create-a-batch-job"></a><span data-ttu-id="c5279-103">Pakktöö loomine</span><span class="sxs-lookup"><span data-stu-id="c5279-103">Create a batch job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c5279-104">Pakett-töö on tööülesannete grupp, mis on edastatud rakendusobjekti serveri (AOS) eksemplarile automaatseks töötluseks.</span><span class="sxs-lookup"><span data-stu-id="c5279-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="c5279-105">Pakett-töid käitatakse, kasutades töö loonud kasutaja turvamandaate.</span><span class="sxs-lookup"><span data-stu-id="c5279-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="c5279-106">Kasutage pakett-töö loomiseks järgmist protseduuri.</span><span class="sxs-lookup"><span data-stu-id="c5279-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="c5279-107">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="c5279-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="c5279-108">Pakett-töö loomine</span><span class="sxs-lookup"><span data-stu-id="c5279-108">Create the batch job</span></span>
1. <span data-ttu-id="c5279-109">Avage **Navigatsioonipaan > Moodulid > Süsteemihaldus > Päringud > Pakett-tööd**.</span><span class="sxs-lookup"><span data-stu-id="c5279-109">Go to **Navigation pane > Modules > System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="c5279-110">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c5279-110">Click **New**.</span></span>
3. <span data-ttu-id="c5279-111">Sisestage väärtus väljale **Töö kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="c5279-111">In the **Job description** field, type a value.</span></span>
4. <span data-ttu-id="c5279-112">Sisestage väljale **Plaanitud alguskuupäev/kellaaeg** kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="c5279-112">In the **Scheduled start date/time** field, enter a date and time.</span></span>
5. <span data-ttu-id="c5279-113">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="c5279-113">Click **Save**.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="c5279-114">Korduvuse loomine</span><span class="sxs-lookup"><span data-stu-id="c5279-114">Create a recurrence</span></span>
1. <span data-ttu-id="c5279-115">Klõpsake tegumiribal valikut **Pakett-töö**.</span><span class="sxs-lookup"><span data-stu-id="c5279-115">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="c5279-116">Klõpsake valikul **Korduvus**.</span><span class="sxs-lookup"><span data-stu-id="c5279-116">Click **Recurrence**.</span></span> <span data-ttu-id="c5279-117">Kasutage neid valikuid korduvuse vahemiku ja mustri sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="c5279-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="c5279-118">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="c5279-118">Click **OK**.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="c5279-119">Teatiste lisamine</span><span class="sxs-lookup"><span data-stu-id="c5279-119">Add alerts</span></span>
1. <span data-ttu-id="c5279-120">Klõpsake tegumiribal valikut **Pakett-töö**.</span><span class="sxs-lookup"><span data-stu-id="c5279-120">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="c5279-121">Klõpsake valikut **Teatised**.</span><span class="sxs-lookup"><span data-stu-id="c5279-121">Click **Alerts**.</span></span> <span data-ttu-id="c5279-122">Näidake, kas soovite, et teated saadetakse, kui pakett-töö lõpeb, kui selles on tõrge või kui see tühistatakse.</span><span class="sxs-lookup"><span data-stu-id="c5279-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="c5279-123">Seejärel määrake, kas soovite, et teated kuvatakse hüpikteadetena.</span><span class="sxs-lookup"><span data-stu-id="c5279-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="c5279-124">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="c5279-124">Click **OK**.</span></span>

## <a name="adjust-batch-job-status"></a><span data-ttu-id="c5279-125">Pakett-töö oleku reguleerimine</span><span class="sxs-lookup"><span data-stu-id="c5279-125">Adjust batch job status</span></span>
1. <span data-ttu-id="c5279-126">Avage **Süsteemihaldus > Päringud > Pakett-tööd**.</span><span class="sxs-lookup"><span data-stu-id="c5279-126">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="c5279-127">Valige sobiv pakett-töö.</span><span class="sxs-lookup"><span data-stu-id="c5279-127">Select the appropriate batch job.</span></span>
3. <span data-ttu-id="c5279-128">Klõpsake tegumiribal valikut **Pakett-töö > Funktsioonid > Muuda olekut**.</span><span class="sxs-lookup"><span data-stu-id="c5279-128">On the Action Pane, click **Batch job > Functions > Change status**.</span></span>
4. <span data-ttu-id="c5279-129">Valige asjassepuutuv olek.</span><span class="sxs-lookup"><span data-stu-id="c5279-129">Select the appropriate status:</span></span>
    - <span data-ttu-id="c5279-130">**Kinnipeetud**: seadke pakett-töö olekuks **kinnipeetud** nii, et see on pakett-töö toiminguajastist kinni peetud.</span><span class="sxs-lookup"><span data-stu-id="c5279-130">**Withhold**: Set the batch job as **withhold** so it is withheld from the batch job scheduler.</span></span> <span data-ttu-id="c5279-131">Sama kui *peatus*.</span><span class="sxs-lookup"><span data-stu-id="c5279-131">Equivalent to *stop*.</span></span>
    - <span data-ttu-id="c5279-132">**Ootel**: seadistage pakett-töö olekuks **ootel**, et see ootaks pakett-töö ajasti poolt üleskorjamist.</span><span class="sxs-lookup"><span data-stu-id="c5279-132">**Waiting**: Set the batch job as **waiting** so it is waiting to be picked up by the batch job scheduler.</span></span> <span data-ttu-id="c5279-133">Sama kui *mine*.</span><span class="sxs-lookup"><span data-stu-id="c5279-133">Equivalent to *go*.</span></span>
5. <span data-ttu-id="c5279-134">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="c5279-134">Click **OK**.</span></span>
