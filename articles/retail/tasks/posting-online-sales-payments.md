--- 
title: "Veebimüügi ja -maksete sisestamine"
description: "See protseduur selgitab korduva pakett-töö konfigureerimist ja käitamist veebipoe kannete jaoks müügitellimuste ja maksete loomiseks."
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 13839bbe6ca03f3cfc7036fce87477bf7d5af2a7
ms.contentlocale: et-ee
ms.lasthandoff: 09/14/2018

---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="e8894-103">Veebimüügi ja -maksete sisestamine</span><span class="sxs-lookup"><span data-stu-id="e8894-103">Posting of online sales and payments</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="e8894-104">See protseduur selgitab korduva pakett-töö konfigureerimist ja käitamist veebipoe kannete jaoks müügitellimuste ja maksete loomiseks.</span><span class="sxs-lookup"><span data-stu-id="e8894-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="e8894-105">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="e8894-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="e8894-106">Avage Kõik tööruumid > Jaekaupluse rahandus.</span><span class="sxs-lookup"><span data-stu-id="e8894-106">Go to All workspaces > Retail store financials.</span></span>
2. <span data-ttu-id="e8894-107">Klõpsake suvandit Tellimuste sünkroonimine.</span><span class="sxs-lookup"><span data-stu-id="e8894-107">Click Synchronize orders.</span></span>
3. <span data-ttu-id="e8894-108">Valige väljal Organisatsiooni hierarhia suvand Jaekauplused piirkonniti.</span><span class="sxs-lookup"><span data-stu-id="e8894-108">In the Organization hierarchy field, select 'Retail Stores by Region'.</span></span>
    * <span data-ttu-id="e8894-109">Valige kindel veebipood või sõlm, kui soovite pakett-töö luua kaupluste grupi jaoks.</span><span class="sxs-lookup"><span data-stu-id="e8894-109">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="e8894-110">Klõpsake valiku lisamiseks noolt.</span><span class="sxs-lookup"><span data-stu-id="e8894-110">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="e8894-111">Klõpsake vahekaarti Käivita taustal.</span><span class="sxs-lookup"><span data-stu-id="e8894-111">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="e8894-112">Märkige või tühjendage ruut Pakktöötlus.</span><span class="sxs-lookup"><span data-stu-id="e8894-112">Check or uncheck the Batch processing checkbox.</span></span>
6. <span data-ttu-id="e8894-113">Klõpsake valikut Korduvus.</span><span class="sxs-lookup"><span data-stu-id="e8894-113">Click Recurrence.</span></span>
7. <span data-ttu-id="e8894-114">Valige suvand Lõppkuupäev puudub.</span><span class="sxs-lookup"><span data-stu-id="e8894-114">Select the No end date option.</span></span>
8. <span data-ttu-id="e8894-115">Sisestage number väljale Arv.</span><span class="sxs-lookup"><span data-stu-id="e8894-115">In the Count field, enter a number.</span></span>
9. <span data-ttu-id="e8894-116">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e8894-116">Click OK.</span></span>
10. <span data-ttu-id="e8894-117">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e8894-117">Click OK.</span></span>


