---
title: Pakktöö loomine
description: Pakett-töö on tööülesannete grupp, mis on edastatud rakendusobjekti serveri (AOS) eksemplarile automaatseks töötluseks.
author: maertenm
ms.date: 06/21/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: BatchJob, SysRecurrence, BatchAlerts
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f498014555e0beccbc8965dd43e5162944867978
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745857"
---
# <a name="create-a-batch-job"></a><span data-ttu-id="506fc-103">Pakktöö loomine</span><span class="sxs-lookup"><span data-stu-id="506fc-103">Create a batch job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="506fc-104">Pakett-töö on tööülesannete grupp, mis on edastatud rakendusobjekti serveri (AOS) eksemplarile automaatseks töötluseks.</span><span class="sxs-lookup"><span data-stu-id="506fc-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="506fc-105">Pakett-töid käitatakse, kasutades töö loonud kasutaja turvamandaate.</span><span class="sxs-lookup"><span data-stu-id="506fc-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="506fc-106">Kasutage pakett-töö loomiseks järgmist protseduuri.</span><span class="sxs-lookup"><span data-stu-id="506fc-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="506fc-107">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="506fc-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="506fc-108">Pakett-töö loomine</span><span class="sxs-lookup"><span data-stu-id="506fc-108">Create the batch job</span></span>
1. <span data-ttu-id="506fc-109">Avage **Navigatsioonipaan > Moodulid > Süsteemihaldus > Päringud > Pakett-tööd**.</span><span class="sxs-lookup"><span data-stu-id="506fc-109">Go to **Navigation pane > Modules > System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="506fc-110">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="506fc-110">Click **New**.</span></span>
3. <span data-ttu-id="506fc-111">Sisestage väärtus väljale **Töö kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="506fc-111">In the **Job description** field, type a value.</span></span>
4. <span data-ttu-id="506fc-112">Sisestage väljale **Plaanitud alguskuupäev/kellaaeg** kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="506fc-112">In the **Scheduled start date/time** field, enter a date and time.</span></span>
5. <span data-ttu-id="506fc-113">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="506fc-113">Click **Save**.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="506fc-114">Korduvuse loomine</span><span class="sxs-lookup"><span data-stu-id="506fc-114">Create a recurrence</span></span>
1. <span data-ttu-id="506fc-115">Klõpsake tegumiribal valikut **Pakett-töö**.</span><span class="sxs-lookup"><span data-stu-id="506fc-115">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="506fc-116">Klõpsake valikul **Korduvus**.</span><span class="sxs-lookup"><span data-stu-id="506fc-116">Click **Recurrence**.</span></span> <span data-ttu-id="506fc-117">Kasutage neid valikuid korduvuse vahemiku ja mustri sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="506fc-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="506fc-118">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="506fc-118">Click **OK**.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="506fc-119">Teatiste lisamine</span><span class="sxs-lookup"><span data-stu-id="506fc-119">Add alerts</span></span>
1. <span data-ttu-id="506fc-120">Klõpsake tegumiribal valikut **Pakett-töö**.</span><span class="sxs-lookup"><span data-stu-id="506fc-120">On the Action Pane, click **Batch job**.</span></span>
2. <span data-ttu-id="506fc-121">Klõpsake valikut **Teatised**.</span><span class="sxs-lookup"><span data-stu-id="506fc-121">Click **Alerts**.</span></span> <span data-ttu-id="506fc-122">Näidake, kas soovite, et teated saadetakse, kui pakett-töö lõpeb, kui selles on tõrge või kui see tühistatakse.</span><span class="sxs-lookup"><span data-stu-id="506fc-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="506fc-123">Seejärel määrake, kas soovite, et teated kuvatakse hüpikteadetena.</span><span class="sxs-lookup"><span data-stu-id="506fc-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="506fc-124">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="506fc-124">Click **OK**.</span></span>

## <a name="adjust-batch-job-status"></a><span data-ttu-id="506fc-125">Pakett-töö oleku reguleerimine</span><span class="sxs-lookup"><span data-stu-id="506fc-125">Adjust batch job status</span></span>
1. <span data-ttu-id="506fc-126">Avage **Süsteemihaldus > Päringud > Pakett-tööd**.</span><span class="sxs-lookup"><span data-stu-id="506fc-126">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="506fc-127">Valige sobiv pakett-töö.</span><span class="sxs-lookup"><span data-stu-id="506fc-127">Select the appropriate batch job.</span></span>
3. <span data-ttu-id="506fc-128">Klõpsake tegumiribal valikut **Pakett-töö > Funktsioonid > Muuda olekut**.</span><span class="sxs-lookup"><span data-stu-id="506fc-128">On the Action Pane, click **Batch job > Functions > Change status**.</span></span>
4. <span data-ttu-id="506fc-129">Valige asjassepuutuv olek.</span><span class="sxs-lookup"><span data-stu-id="506fc-129">Select the appropriate status:</span></span>
    - <span data-ttu-id="506fc-130">**Kinnipeetud**: seadke pakett-töö olekuks **kinnipeetud** nii, et see on pakett-töö toiminguajastist kinni peetud.</span><span class="sxs-lookup"><span data-stu-id="506fc-130">**Withhold**: Set the batch job as **withhold** so it is withheld from the batch job scheduler.</span></span> <span data-ttu-id="506fc-131">Sama kui *peatus*.</span><span class="sxs-lookup"><span data-stu-id="506fc-131">Equivalent to *stop*.</span></span>
    - <span data-ttu-id="506fc-132">**Ootel**: seadistage pakett-töö olekuks **ootel**, et see ootaks pakett-töö ajasti poolt üleskorjamist.</span><span class="sxs-lookup"><span data-stu-id="506fc-132">**Waiting**: Set the batch job as **waiting** so it is waiting to be picked up by the batch job scheduler.</span></span> <span data-ttu-id="506fc-133">Sama kui *mine*.</span><span class="sxs-lookup"><span data-stu-id="506fc-133">Equivalent to *go*.</span></span>
5. <span data-ttu-id="506fc-134">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="506fc-134">Click **OK**.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]