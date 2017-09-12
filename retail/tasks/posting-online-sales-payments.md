--- 
title: " Veebimüügi ja -maksete sisestamine"
description: "See protseduur selgitab korduva pakett-töö konfigureerimist ja käitamist veebipoe kannete jaoks müügitellimuste ja maksete loomiseks."
author: jashanno
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: e8c3f861a53a3f5c2de29248523ff4efd5e1d072
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="post-online-sales-and-payments"></a><span data-ttu-id="9452f-103"> Veebimüügi ja -maksete sisestamine</span><span class="sxs-lookup"><span data-stu-id="9452f-103">Post online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="9452f-104">See protseduur selgitab korduva pakett-töö konfigureerimist ja käitamist veebipoe kannete jaoks müügitellimuste ja maksete loomiseks.</span><span class="sxs-lookup"><span data-stu-id="9452f-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="9452f-105">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="9452f-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="9452f-106">Avage Kõik tööruumid > Jaekaupluse rahandus.</span><span class="sxs-lookup"><span data-stu-id="9452f-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="9452f-107">Klõpsake suvandit Tellimuste sünkroonimine.</span><span class="sxs-lookup"><span data-stu-id="9452f-107">Click Synchronize orders.</span></span>
3. <span data-ttu-id="9452f-108">Valige väljal Organisatsiooni hierarhia suvand Jaekauplused piirkonniti.</span><span class="sxs-lookup"><span data-stu-id="9452f-108">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="9452f-109">Valige kindel veebipood või sõlm, kui soovite pakett-töö luua kaupluste grupi jaoks.</span><span class="sxs-lookup"><span data-stu-id="9452f-109">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="9452f-110">Klõpsake valiku lisamiseks noolt.</span><span class="sxs-lookup"><span data-stu-id="9452f-110">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="9452f-111">Klõpsake vahekaarti Käivita taustal.</span><span class="sxs-lookup"><span data-stu-id="9452f-111">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="9452f-112">Märkige või tühjendage ruut Pakktöötlus.</span><span class="sxs-lookup"><span data-stu-id="9452f-112">Check or uncheck the Batch processing checkbox.</span></span>
6. <span data-ttu-id="9452f-113">Klõpsake valikut Korduvus.</span><span class="sxs-lookup"><span data-stu-id="9452f-113">Click Recurrence.</span></span>
7. <span data-ttu-id="9452f-114">Valige suvand Lõppkuupäev puudub.</span><span class="sxs-lookup"><span data-stu-id="9452f-114">Select the No end date option.</span></span>
8. <span data-ttu-id="9452f-115">Sisestage number väljale Arv.</span><span class="sxs-lookup"><span data-stu-id="9452f-115">In the Count field, enter a number.</span></span>
9. <span data-ttu-id="9452f-116">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9452f-116">Click OK.</span></span>
10. <span data-ttu-id="9452f-117">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="9452f-117">Click OK.</span></span>


