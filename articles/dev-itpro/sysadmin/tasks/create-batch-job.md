--- 
title: "Pakett-tööde loomine"
description: "Pakett-töö on tööülesannete grupp, mis on edastatud rakendusobjekti serveri (AOS) eksemplarile automaatseks töötluseks."
author: maertenm
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: maertenm
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e782d33f3748524491dace28008cd9148ae70529
ms.openlocfilehash: b32c16a0c0045e22128746f81c6e9fd03370ac1f
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---
# <a name="create-batch-jobs"></a><span data-ttu-id="8f732-103">Pakett-tööde loomine</span><span class="sxs-lookup"><span data-stu-id="8f732-103">Create batch jobs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8f732-104">Pakett-töö on tööülesannete grupp, mis on edastatud rakendusobjekti serveri (AOS) eksemplarile automaatseks töötluseks.</span><span class="sxs-lookup"><span data-stu-id="8f732-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="8f732-105">Pakett-töid käitatakse, kasutades töö loonud kasutaja turvamandaate.</span><span class="sxs-lookup"><span data-stu-id="8f732-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="8f732-106">Kasutage pakett-töö loomiseks järgmist protseduuri.</span><span class="sxs-lookup"><span data-stu-id="8f732-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="8f732-107">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="8f732-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="8f732-108">Pakett-töö loomine</span><span class="sxs-lookup"><span data-stu-id="8f732-108">Create the batch job</span></span>
1. <span data-ttu-id="8f732-109">Avage Süsteemihaldus > Päringud > Pakett-tööd.</span><span class="sxs-lookup"><span data-stu-id="8f732-109">Go to System administration > Inquiries > Batch jobs.</span></span>
2. <span data-ttu-id="8f732-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="8f732-110">Click New.</span></span>
3. <span data-ttu-id="8f732-111">Sisestage väärtus väljale Töö kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="8f732-111">In the Job description field, type a value.</span></span>
4. <span data-ttu-id="8f732-112">Sisestage väljale Plaanitud alguskuupäev ja -kellaaeg kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="8f732-112">In the Scheduled start date/time field, enter a date and time.</span></span>
5. <span data-ttu-id="8f732-113">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="8f732-113">Click Save.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="8f732-114">Korduvuse loomine</span><span class="sxs-lookup"><span data-stu-id="8f732-114">Create a recurrence</span></span>
1. <span data-ttu-id="8f732-115">Klõpsake tegumiribal valikut Pakett-töö.</span><span class="sxs-lookup"><span data-stu-id="8f732-115">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="8f732-116">Klõpsake valikut Korduvus.</span><span class="sxs-lookup"><span data-stu-id="8f732-116">Click Recurrence.</span></span>
    * <span data-ttu-id="8f732-117">Kasutage neid valikuid korduvuse vahemiku ja mustri sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="8f732-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="8f732-118">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="8f732-118">Click OK.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="8f732-119">Teatiste lisamine</span><span class="sxs-lookup"><span data-stu-id="8f732-119">Add alerts</span></span>
1. <span data-ttu-id="8f732-120">Klõpsake tegumiribal valikut Pakett-töö.</span><span class="sxs-lookup"><span data-stu-id="8f732-120">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="8f732-121">Klõpsake valikut Teatised.</span><span class="sxs-lookup"><span data-stu-id="8f732-121">Click Alerts.</span></span>
    * <span data-ttu-id="8f732-122">Näidake, kas soovite, et teated saadetakse, kui pakett-töö lõpeb, kui selles on tõrge või kui see tühistatakse.</span><span class="sxs-lookup"><span data-stu-id="8f732-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="8f732-123">Seejärel määrake, kas soovite, et teated kuvatakse hüpikteadetena.</span><span class="sxs-lookup"><span data-stu-id="8f732-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="8f732-124">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="8f732-124">Click OK.</span></span>


