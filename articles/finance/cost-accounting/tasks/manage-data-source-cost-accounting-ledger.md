---
title: Kuluarvestuse pearaamatu andmeallika haldamine
description: Selle toimingu abil saate hallata kuluarvestuse pearaamatu andmeallikat.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4cf53e905cf32557f4671477b173b1c5072d186e
ms.sourcegitcommit: c69926b4285cb2ec2d9ce1ad72d1cb852024dd5e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3137817"
---
# <a name="manage-a-data-source-for-the-cost-accounting-ledger"></a><span data-ttu-id="e8ab2-103">Kuluarvestuse pearaamatu andmeallika haldamine</span><span class="sxs-lookup"><span data-stu-id="e8ab2-103">Manage a data source for the cost accounting ledger</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e8ab2-104">Selle toimingu abil saate hallata kuluarvestuse pearaamatu andmeallikat.</span><span class="sxs-lookup"><span data-stu-id="e8ab2-104">Use this procedure to manage the general ledger data source for a cost accounting ledger.</span></span> <span data-ttu-id="e8ab2-105">Enne selle ülesande täitmist veenduge, et tutvute ülesandejuhenditega Kuluarvestuse pearaamatu loomine ja Kulu juhtseadmete määratlemine.</span><span class="sxs-lookup"><span data-stu-id="e8ab2-105">Before you complete this task, make sure that you play the "Create a cost accounting ledger" and "Define cost control units" task guides.</span></span> <span data-ttu-id="e8ab2-106">See salvestis kasutab USP2 demoandmete ettevõtet.</span><span class="sxs-lookup"><span data-stu-id="e8ab2-106">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="e8ab2-107">Avage Kuluarvestus > Pearaamatu häälestamine > Kuluarvestuse pearaamatud.</span><span class="sxs-lookup"><span data-stu-id="e8ab2-107">Go to Cost accounting > Ledger setup > Cost accounting ledgers.</span></span>
2. <span data-ttu-id="e8ab2-108">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e8ab2-108">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="e8ab2-109">Klõpsake suvandit Tegelikud versioonid.</span><span class="sxs-lookup"><span data-stu-id="e8ab2-109">Click Actual versions.</span></span>
4. <span data-ttu-id="e8ab2-110">Klõpsake tegumiribal valikut Haldamine.</span><span class="sxs-lookup"><span data-stu-id="e8ab2-110">On the Action Pane, click Manage.</span></span>
5. <span data-ttu-id="e8ab2-111">Klõpsake suvandit Pearaamat.</span><span class="sxs-lookup"><span data-stu-id="e8ab2-111">Click General ledger.</span></span>
6. <span data-ttu-id="e8ab2-112">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e8ab2-112">Click New.</span></span>
7. <span data-ttu-id="e8ab2-113">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="e8ab2-113">In the Name field, type a value.</span></span>
8. <span data-ttu-id="e8ab2-114">Sisestage või valige väärtus väljal Andmepakkuja.</span><span class="sxs-lookup"><span data-stu-id="e8ab2-114">In the Data provider field, enter or select a value.</span></span>
    * <span data-ttu-id="e8ab2-115">Näiteks valige Dynamics 365 Finance - Pearaamatu sisestused.</span><span class="sxs-lookup"><span data-stu-id="e8ab2-115">For this example, select Dynamics 365 Finance - General ledger entries.</span></span>  
9. <span data-ttu-id="e8ab2-116">Sisestage või valige väärtus väljal Kuluelemendi dimensioon.</span><span class="sxs-lookup"><span data-stu-id="e8ab2-116">In the Cost element dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="e8ab2-117">Selles näites valige Kuluelemendid.</span><span class="sxs-lookup"><span data-stu-id="e8ab2-117">For this example, select Cost elements.</span></span>  
10. <span data-ttu-id="e8ab2-118">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e8ab2-118">Click Save.</span></span>
11. <span data-ttu-id="e8ab2-119">Klõpsake suvandit Andmepakkuja konfigureerimine.</span><span class="sxs-lookup"><span data-stu-id="e8ab2-119">Click Configure data provider.</span></span>
12. <span data-ttu-id="e8ab2-120">Sisestage või valige väärtus väljal Juriidiline isik.</span><span class="sxs-lookup"><span data-stu-id="e8ab2-120">In the Legal entity field, enter or select a value.</span></span>
    * <span data-ttu-id="e8ab2-121">Selles näites valige USP2.</span><span class="sxs-lookup"><span data-stu-id="e8ab2-121">For this example, select USP2.</span></span>  
13. <span data-ttu-id="e8ab2-122">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e8ab2-122">Click New.</span></span>
14. <span data-ttu-id="e8ab2-123">Valige väljal Sisestamiskiht väärtus Praegune.</span><span class="sxs-lookup"><span data-stu-id="e8ab2-123">In the Posting layer field, select Current.</span></span>
15. <span data-ttu-id="e8ab2-124">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e8ab2-124">Click OK.</span></span>

