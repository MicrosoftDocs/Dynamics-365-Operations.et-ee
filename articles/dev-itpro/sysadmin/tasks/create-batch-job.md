--- 
title: "Pakktöö loomine"
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
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 31c8e2ba87ef8c17a3147e1159104585258d4164
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-batch-job"></a><span data-ttu-id="bec5b-103">Pakktöö loomine</span><span class="sxs-lookup"><span data-stu-id="bec5b-103">Create a batch job</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bec5b-104">Pakett-töö on tööülesannete grupp, mis on edastatud rakendusobjekti serveri (AOS) eksemplarile automaatseks töötluseks.</span><span class="sxs-lookup"><span data-stu-id="bec5b-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="bec5b-105">Pakett-töid käitatakse, kasutades töö loonud kasutaja turvamandaate.</span><span class="sxs-lookup"><span data-stu-id="bec5b-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="bec5b-106">Kasutage pakett-töö loomiseks järgmist protseduuri.</span><span class="sxs-lookup"><span data-stu-id="bec5b-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="bec5b-107">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="bec5b-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="bec5b-108">Pakett-töö loomine</span><span class="sxs-lookup"><span data-stu-id="bec5b-108">Create the batch job</span></span>
1. <span data-ttu-id="bec5b-109">Avage Süsteemihaldus > Päringud > Pakett-tööd.</span><span class="sxs-lookup"><span data-stu-id="bec5b-109">Go to System administration > Inquiries > Batch jobs.</span></span>
2. <span data-ttu-id="bec5b-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="bec5b-110">Click New.</span></span>
3. <span data-ttu-id="bec5b-111">Sisestage väärtus väljale Töö kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="bec5b-111">In the Job description field, type a value.</span></span>
4. <span data-ttu-id="bec5b-112">Sisestage väljale Plaanitud alguskuupäev ja -kellaaeg kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="bec5b-112">In the Scheduled start date/time field, enter a date and time.</span></span>
5. <span data-ttu-id="bec5b-113">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="bec5b-113">Click Save.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="bec5b-114">Korduvuse loomine</span><span class="sxs-lookup"><span data-stu-id="bec5b-114">Create a recurrence</span></span>
1. <span data-ttu-id="bec5b-115">Klõpsake tegumiribal valikut Pakett-töö.</span><span class="sxs-lookup"><span data-stu-id="bec5b-115">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="bec5b-116">Klõpsake valikut Korduvus.</span><span class="sxs-lookup"><span data-stu-id="bec5b-116">Click Recurrence.</span></span>
    * <span data-ttu-id="bec5b-117">Kasutage neid valikuid korduvuse vahemiku ja mustri sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="bec5b-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="bec5b-118">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="bec5b-118">Click OK.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="bec5b-119">Teatiste lisamine</span><span class="sxs-lookup"><span data-stu-id="bec5b-119">Add alerts</span></span>
1. <span data-ttu-id="bec5b-120">Klõpsake tegumiribal valikut Pakett-töö.</span><span class="sxs-lookup"><span data-stu-id="bec5b-120">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="bec5b-121">Klõpsake valikut Teatised.</span><span class="sxs-lookup"><span data-stu-id="bec5b-121">Click Alerts.</span></span>
    * <span data-ttu-id="bec5b-122">Näidake, kas soovite, et teated saadetakse, kui pakett-töö lõpeb, kui selles on tõrge või kui see tühistatakse.</span><span class="sxs-lookup"><span data-stu-id="bec5b-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="bec5b-123">Seejärel määrake, kas soovite, et teated kuvatakse hüpikteadetena.</span><span class="sxs-lookup"><span data-stu-id="bec5b-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="bec5b-124">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="bec5b-124">Click OK.</span></span>


