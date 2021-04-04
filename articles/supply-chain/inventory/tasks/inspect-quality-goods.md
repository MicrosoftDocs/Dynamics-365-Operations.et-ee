---
title: Kaupade kvaliteedi kontrollimine
description: Selles teemas selgitatakse, kuidas kvaliteettellimust töödelda.
author: perlynne
manager: tfehr
ms.date: 08/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e37ac8c9320d427b9f9a3ca32b0e4667c7023339
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5244419"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="f3723-103">Kaupade kvaliteedi kontrollimine</span><span class="sxs-lookup"><span data-stu-id="f3723-103">Inspect the quality of goods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f3723-104">Selles teemas selgitatakse, kuidas kvaliteettellimust töödelda.</span><span class="sxs-lookup"><span data-stu-id="f3723-104">This topic explains how to process a quality order.</span></span> <span data-ttu-id="f3723-105">Saate selle juhendi käitada demoettevõtte USMF andmetega.</span><span class="sxs-lookup"><span data-stu-id="f3723-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="f3723-106">Enne selle näidisprotseduuri käivitamist peate ostutellimuse 000016 kinnitama ja toote sissetuleku sisestama.</span><span class="sxs-lookup"><span data-stu-id="f3723-106">Before you start this example procedure, you need to confirm purchase order "000016" and post a product receipt.</span></span> <span data-ttu-id="f3723-107">See loob kvaliteettellimuse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="f3723-107">This will automatically create a quality order.</span></span> <span data-ttu-id="f3723-108">Kvaliteedikontrolle teeb üldjuhul kvaliteediametnik.</span><span class="sxs-lookup"><span data-stu-id="f3723-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="f3723-109">Kvaliteettellimuse valimine</span><span class="sxs-lookup"><span data-stu-id="f3723-109">Select a quality order</span></span>
1. <span data-ttu-id="f3723-110">Navigeerimispaanil avage **Moodulid > Varud > Perioodilised ülesanded > Kvaliteethaldus > Kvaliteettellimus**.</span><span class="sxs-lookup"><span data-stu-id="f3723-110">In the navigation pane, go to **Modules > Inventory management > Periodic tasks > Quality management > Quality orders**.</span></span>
2. <span data-ttu-id="f3723-111">Valige kvaliteettellimus, mis loodi enne selle protseduuri käivitamist.</span><span class="sxs-lookup"><span data-stu-id="f3723-111">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="f3723-112">Testitulemuste salvestamine</span><span class="sxs-lookup"><span data-stu-id="f3723-112">Record test results</span></span>
1. <span data-ttu-id="f3723-113">Valige **Tulemid**.</span><span class="sxs-lookup"><span data-stu-id="f3723-113">Select **Results**.</span></span>
2. <span data-ttu-id="f3723-114">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="f3723-114">Select **Edit**.</span></span>
3. <span data-ttu-id="f3723-115">Sisestage number väljale **Tulemuse kogus**.</span><span class="sxs-lookup"><span data-stu-id="f3723-115">In the **Result quantity** field, enter a number.</span></span>
4. <span data-ttu-id="f3723-116">Valige otsingu avamiseks väljal **Väljundteade** ripploendi nupp.</span><span class="sxs-lookup"><span data-stu-id="f3723-116">In the **Outcome** field, select the desired record in the drop-down menu.</span></span>  
- <span data-ttu-id="f3723-117">Selles näites põhineb tulemus eelmääratletud tulemusel.</span><span class="sxs-lookup"><span data-stu-id="f3723-117">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="f3723-118">Üldjuhul saate salvestada täpsema katse tulemuse, nt suuruse või muu dimensiooni.</span><span class="sxs-lookup"><span data-stu-id="f3723-118">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
5. <span data-ttu-id="f3723-119">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="f3723-119">Select **Save**.</span></span>
6. <span data-ttu-id="f3723-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f3723-120">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="f3723-121">Kontrolli kvaliteettellimuse õigsust</span><span class="sxs-lookup"><span data-stu-id="f3723-121">Validate the quality order</span></span>
1. <span data-ttu-id="f3723-122">Valige **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="f3723-122">Select **Validate**.</span></span>
2. <span data-ttu-id="f3723-123">Väljal **Kinnitaja** valige kasutaja, kes teostab kontrolli rippmenüüs.</span><span class="sxs-lookup"><span data-stu-id="f3723-123">In the **Validated by** field, select the user performing the inspection from the drop-down menu.</span></span>  
3. <span data-ttu-id="f3723-124">Klõpsake **Vali**.</span><span class="sxs-lookup"><span data-stu-id="f3723-124">Click **Select**.</span></span>
4. <span data-ttu-id="f3723-125">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="f3723-125">Select **OK**.</span></span>
5. <span data-ttu-id="f3723-126">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="f3723-126">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]