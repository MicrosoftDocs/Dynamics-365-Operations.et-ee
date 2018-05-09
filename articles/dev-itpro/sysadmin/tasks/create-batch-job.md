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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 55b153e6044f61f16e19ae0b264e3f23538e004a
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-batch-job"></a><span data-ttu-id="cffdd-103">Pakktöö loomine</span><span class="sxs-lookup"><span data-stu-id="cffdd-103">Create a batch job</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cffdd-104">Pakett-töö on tööülesannete grupp, mis on edastatud rakendusobjekti serveri (AOS) eksemplarile automaatseks töötluseks.</span><span class="sxs-lookup"><span data-stu-id="cffdd-104">A batch job is a group of tasks that are submitted to an Application Object Server (AOS) instance for automatic processing.</span></span> <span data-ttu-id="cffdd-105">Pakett-töid käitatakse, kasutades töö loonud kasutaja turvamandaate.</span><span class="sxs-lookup"><span data-stu-id="cffdd-105">Batch jobs are run by using the security credentials of the user who created the job.</span></span> <span data-ttu-id="cffdd-106">Kasutage pakett-töö loomiseks järgmist protseduuri.</span><span class="sxs-lookup"><span data-stu-id="cffdd-106">Use the following procedure to create a batch job.</span></span> <span data-ttu-id="cffdd-107">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="cffdd-107">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-the-batch-job"></a><span data-ttu-id="cffdd-108">Pakett-töö loomine</span><span class="sxs-lookup"><span data-stu-id="cffdd-108">Create the batch job</span></span>
1. <span data-ttu-id="cffdd-109">Avage Süsteemihaldus > Päringud > Pakett-tööd.</span><span class="sxs-lookup"><span data-stu-id="cffdd-109">Go to System administration > Inquiries > Batch jobs.</span></span>
2. <span data-ttu-id="cffdd-110">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="cffdd-110">Click New.</span></span>
3. <span data-ttu-id="cffdd-111">Sisestage väärtus väljale Töö kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="cffdd-111">In the Job description field, type a value.</span></span>
4. <span data-ttu-id="cffdd-112">Sisestage väljale Plaanitud alguskuupäev ja -kellaaeg kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="cffdd-112">In the Scheduled start date/time field, enter a date and time.</span></span>
5. <span data-ttu-id="cffdd-113">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="cffdd-113">Click Save.</span></span>

## <a name="create-a-recurrence"></a><span data-ttu-id="cffdd-114">Korduvuse loomine</span><span class="sxs-lookup"><span data-stu-id="cffdd-114">Create a recurrence</span></span>
1. <span data-ttu-id="cffdd-115">Klõpsake tegumiribal valikut Pakett-töö.</span><span class="sxs-lookup"><span data-stu-id="cffdd-115">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="cffdd-116">Klõpsake valikut Korduvus.</span><span class="sxs-lookup"><span data-stu-id="cffdd-116">Click Recurrence.</span></span>
    * <span data-ttu-id="cffdd-117">Kasutage neid valikuid korduvuse vahemiku ja mustri sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="cffdd-117">Use these options to enter a range and pattern for the recurrence.</span></span>  
3. <span data-ttu-id="cffdd-118">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="cffdd-118">Click OK.</span></span>

## <a name="add-alerts"></a><span data-ttu-id="cffdd-119">Teatiste lisamine</span><span class="sxs-lookup"><span data-stu-id="cffdd-119">Add alerts</span></span>
1. <span data-ttu-id="cffdd-120">Klõpsake tegumiribal valikut Pakett-töö.</span><span class="sxs-lookup"><span data-stu-id="cffdd-120">On the Action Pane, click Batch job.</span></span>
2. <span data-ttu-id="cffdd-121">Klõpsake valikut Teatised.</span><span class="sxs-lookup"><span data-stu-id="cffdd-121">Click Alerts.</span></span>
    * <span data-ttu-id="cffdd-122">Näidake, kas soovite, et teated saadetakse, kui pakett-töö lõpeb, kui selles on tõrge või kui see tühistatakse.</span><span class="sxs-lookup"><span data-stu-id="cffdd-122">Indicate if you want alert messages sent when the batch job ends, has an error, or is canceled.</span></span> <span data-ttu-id="cffdd-123">Seejärel määrake, kas soovite, et teated kuvatakse hüpikteadetena.</span><span class="sxs-lookup"><span data-stu-id="cffdd-123">Then specify if you want the alerts to be displayed as pop-up messages.</span></span>   
3. <span data-ttu-id="cffdd-124">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="cffdd-124">Click OK.</span></span>


