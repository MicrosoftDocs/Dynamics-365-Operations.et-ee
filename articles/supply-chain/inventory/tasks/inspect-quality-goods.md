---
title: Kaupade kvaliteedi kontrollimine
description: Selles teemas selgitatakse, kuidas kvaliteettellimust töödelda.
author: perlynne
manager: AnnBe
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10acb9aadfeb11ede1d66dd525ace7b70db3bd1c
ms.sourcegitcommit: fbaccf72df82e6b6927f0c9f0d35af0ca3ecbc2d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/02/2019
ms.locfileid: "1855682"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="56baf-103">Kaupade kvaliteedi kontrollimine</span><span class="sxs-lookup"><span data-stu-id="56baf-103">Inspect the quality of goods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="56baf-104">Selles teemas selgitatakse, kuidas kvaliteettellimust töödelda.</span><span class="sxs-lookup"><span data-stu-id="56baf-104">This topic explains how to process a quality order.</span></span> <span data-ttu-id="56baf-105">Saate selle juhendi käitada demoettevõtte USMF andmetega.</span><span class="sxs-lookup"><span data-stu-id="56baf-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="56baf-106">Enne selle näidisprotseduuri käivitamist peate ostutellimuse 000016 kinnitama ja toote sissetuleku sisestama.</span><span class="sxs-lookup"><span data-stu-id="56baf-106">Before you start this example procedure, you need to confirm purchase order “000016” and post a product receipt.</span></span> <span data-ttu-id="56baf-107">See loob kvaliteettellimuse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="56baf-107">This will automatically create a quality order.</span></span> <span data-ttu-id="56baf-108">Kvaliteedikontrolle teeb üldjuhul kvaliteediametnik.</span><span class="sxs-lookup"><span data-stu-id="56baf-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="56baf-109">Kvaliteettellimuse valimine</span><span class="sxs-lookup"><span data-stu-id="56baf-109">Select a quality order</span></span>
1. <span data-ttu-id="56baf-110">Navigeerimispaanil avage **Moodulid > Varud > Perioodilised ülesanded > Kvaliteethaldus > Kvaliteettellimus**.</span><span class="sxs-lookup"><span data-stu-id="56baf-110">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="56baf-111">Valige kvaliteettellimus, mis loodi enne selle protseduuri käivitamist.</span><span class="sxs-lookup"><span data-stu-id="56baf-111">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="56baf-112">Testitulemuste salvestamine</span><span class="sxs-lookup"><span data-stu-id="56baf-112">Record test results</span></span>
1. <span data-ttu-id="56baf-113">Valige **Tulemid**.</span><span class="sxs-lookup"><span data-stu-id="56baf-113">Select **Results**.</span></span>
2. <span data-ttu-id="56baf-114">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="56baf-114">Select **Edit**.</span></span>
3. <span data-ttu-id="56baf-115">Sisestage number väljale **Tulemuse kogus**.</span><span class="sxs-lookup"><span data-stu-id="56baf-115">In the **Result quantity** field, enter a number.</span></span>
4. <span data-ttu-id="56baf-116">Valige otsingu avamiseks väljal **Väljundteade** ripploendi nupp.</span><span class="sxs-lookup"><span data-stu-id="56baf-116">In the **Outcome** field, select the desired record in the drop-down menu.</span></span>  
- <span data-ttu-id="56baf-117">Selles näites põhineb tulemus eelmääratletud tulemusel.</span><span class="sxs-lookup"><span data-stu-id="56baf-117">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="56baf-118">Üldjuhul saate salvestada täpsema katse tulemuse, nt suuruse või muu dimensiooni.</span><span class="sxs-lookup"><span data-stu-id="56baf-118">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
5. <span data-ttu-id="56baf-119">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="56baf-119">Select **Save**.</span></span>
6. <span data-ttu-id="56baf-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="56baf-120">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="56baf-121">Kontrolli kvaliteettellimuse õigsust</span><span class="sxs-lookup"><span data-stu-id="56baf-121">Validate the quality order</span></span>
1. <span data-ttu-id="56baf-122">Valige **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="56baf-122">Select **Validate**.</span></span>
2. <span data-ttu-id="56baf-123">Väljal **Kinnitaja** valige kasutaja, kes teostab kontrolli rippmenüüs.</span><span class="sxs-lookup"><span data-stu-id="56baf-123">In the **Validated by** field, select the user performing the inspection from the drop-down menu.</span></span>  
3. <span data-ttu-id="56baf-124">Klõpsake **Vali**.</span><span class="sxs-lookup"><span data-stu-id="56baf-124">Click **Select**.</span></span>
4. <span data-ttu-id="56baf-125">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="56baf-125">Select **OK**.</span></span>
5. <span data-ttu-id="56baf-126">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="56baf-126">Close the page.</span></span>

