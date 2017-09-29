--- 
title: "Lähteandmete töötlemine ja jälgimine"
description: "Kogu andmete töötlust käitavad tööd."
author: YuyuScheller
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 7093338fd306e90df79a787f9de9861b3fe49dd5
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="process-and-trace-source-data"></a><span data-ttu-id="7fca1-103">Lähteandmete töötlemine ja jälgimine</span><span class="sxs-lookup"><span data-stu-id="7fca1-103">Process and trace source data</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7fca1-104">Kogu andmete töötlust käitavad tööd.</span><span class="sxs-lookup"><span data-stu-id="7fca1-104">All data processing is run by jobs.</span></span> <span data-ttu-id="7fca1-105">Iga töö ja andmepakkuja jaoks luuakse tööleht, et dokumenteerida protsessi käitust ja sisestuste töötlemist praeguses töös.</span><span class="sxs-lookup"><span data-stu-id="7fca1-105">For each job and data provider, a journal is created to document that the process has been run, and that the entries were processed in the current job.</span></span> <span data-ttu-id="7fca1-106">Selle toimingu abil saate seadistada andmeallika ning seejärel jälgida kindla kulusisestuse päritolu.</span><span class="sxs-lookup"><span data-stu-id="7fca1-106">Use this procedure to set up a data source and then  trace the origin of a specific cost entry.</span></span> <span data-ttu-id="7fca1-107">See salvestis kasutab USP2 demoandmete ettevõtet USP2.</span><span class="sxs-lookup"><span data-stu-id="7fca1-107">This recording uses the USP2 demo data company USP2.</span></span> <span data-ttu-id="7fca1-108">Enne selle ülesande täitmist veenduge, et tutvute ülesandejuhenditega Kuluarvestuse pearaamatu loomine ja Kulu juhtseadmete määratlemine.</span><span class="sxs-lookup"><span data-stu-id="7fca1-108">Before you complete this task, make sure that you play the following task guides: "Create a cost accounting ledger," "Define cost control units," and "Manage data source for the cost accounting ledger."</span></span>

1. <span data-ttu-id="7fca1-109">Avage Kuluarvestus > Pearaamatu häälestamine > Kuluarvestuse pearaamatud.</span><span class="sxs-lookup"><span data-stu-id="7fca1-109">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="7fca1-110">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="7fca1-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7fca1-111">Valige varem loodud kuluarvestuse pearaamat.</span><span class="sxs-lookup"><span data-stu-id="7fca1-111">Select the cost accounting ledger that you created earlier.</span></span>  
3. <span data-ttu-id="7fca1-112">Klõpsake suvandit Tegelikud versioonid.</span><span class="sxs-lookup"><span data-stu-id="7fca1-112">Click Actual versions.</span></span>
4. <span data-ttu-id="7fca1-113">Klõpsake tegumiribal suvandit Lähteandmete töötlemine.</span><span class="sxs-lookup"><span data-stu-id="7fca1-113">On the Action Pane, click Source data processing.</span></span>
5. <span data-ttu-id="7fca1-114">Klõpsake suvandit Pearaamatusisestuse ülekandmistöölehed.</span><span class="sxs-lookup"><span data-stu-id="7fca1-114">Click General ledger entry transfer journals.</span></span>
6. <span data-ttu-id="7fca1-115">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="7fca1-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="7fca1-116">Klõpsake suvandit Töölehe sisestused.</span><span class="sxs-lookup"><span data-stu-id="7fca1-116">Click Journal entries.</span></span>
8. <span data-ttu-id="7fca1-117">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="7fca1-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="7fca1-118">Klõpsake valikut Kulukirjed.</span><span class="sxs-lookup"><span data-stu-id="7fca1-118">Click Cost entries.</span></span>
10. <span data-ttu-id="7fca1-119">Klõpsake suvandit Lähtesisestus.</span><span class="sxs-lookup"><span data-stu-id="7fca1-119">Click Source entry.</span></span>
11. <span data-ttu-id="7fca1-120">Klõpsake tegumiribal suvandit Lähteandmete töötlemine.</span><span class="sxs-lookup"><span data-stu-id="7fca1-120">On the Action Pane, click Source data processing.</span></span>
12. <span data-ttu-id="7fca1-121">Klõpsake suvandit Pearaamat.</span><span class="sxs-lookup"><span data-stu-id="7fca1-121">Click General ledger.</span></span>
13. <span data-ttu-id="7fca1-122">Sisestage või valige väärtus väljal Rahanduskalendri periood.</span><span class="sxs-lookup"><span data-stu-id="7fca1-122">In the Fiscal calendar period field, enter or select a value.</span></span>
    * <span data-ttu-id="7fca1-123">Näiteks saate valida rahandusaasta 2017 perioodi 9.</span><span class="sxs-lookup"><span data-stu-id="7fca1-123">For this example, select Fiscal 2017 Period 9.</span></span>  
14. <span data-ttu-id="7fca1-124">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="7fca1-124">Click OK.</span></span>


