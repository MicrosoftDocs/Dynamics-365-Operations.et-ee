---
title: Kaupade kvaliteedi kontrollimine
description: Selles teemas selgitatakse, kuidas kvaliteettellimusi töödelda.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ec67e7864db12178c0f3cfe8b93d510a46e8a0d4
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956130"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="b07fb-103">Kaupade kvaliteedi kontrollimine</span><span class="sxs-lookup"><span data-stu-id="b07fb-103">Inspect the quality of goods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b07fb-104">Selles teemas selgitatakse, kuidas kvaliteettellimusi töödelda.</span><span class="sxs-lookup"><span data-stu-id="b07fb-104">This topic describes how to process quality orders.</span></span> <span data-ttu-id="b07fb-105">Kvaliteedikontrolle teeb üldjuhul kvaliteediametnik.</span><span class="sxs-lookup"><span data-stu-id="b07fb-105">Quality inspections are typically done by a quality clerk.</span></span>

<span data-ttu-id="b07fb-106">Kui standardsed demoandmed on installitud, saate seda kasutada selle teema protseduuride lõpule viimiseks.</span><span class="sxs-lookup"><span data-stu-id="b07fb-106">If the standard demo data is installed, you can use it to complete the procedures in this topic.</span></span> <span data-ttu-id="b07fb-107">Demoandmete kasutamiseks peate valima ka juriidilise isiku *USMF-i*.</span><span class="sxs-lookup"><span data-stu-id="b07fb-107">To use the demo data, select the *USMF* legal entity before you begin.</span></span> <span data-ttu-id="b07fb-108">Seejärel peate kinnitama ostutellimuse *000016* ja sisestama toote vastuvõtu.</span><span class="sxs-lookup"><span data-stu-id="b07fb-108">You must then confirm purchase order *000016* and post a product receipt.</span></span> <span data-ttu-id="b07fb-109">Kvaliteeditellimus luuakse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="b07fb-109">A quality order is automatically generated.</span></span>

## <a name="step-1-select-a-quality-order"></a><span data-ttu-id="b07fb-110">Samm 1. Kvaliteettellimuse valimine</span><span class="sxs-lookup"><span data-stu-id="b07fb-110">Step 1: Select a quality order</span></span>

<span data-ttu-id="b07fb-111">Kvaliteeditellimuse valimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="b07fb-111">To select a quality order, follow these steps.</span></span>

1. <span data-ttu-id="b07fb-112">Avage **Varude haldus \> Perioodilised ülesanded \> Kvaliteedijuhtimine \> Kvaliteettellimused**.</span><span class="sxs-lookup"><span data-stu-id="b07fb-112">Go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>
1. <span data-ttu-id="b07fb-113">Valige kvaliteettellimus, mis loodi enne selle protseduuri käivitamist.</span><span class="sxs-lookup"><span data-stu-id="b07fb-113">Select the quality order that was generated before you started this procedure.</span></span>

## <a name="step-2-record-test-results"></a><span data-ttu-id="b07fb-114">Samm 2. Testitulemuste salvestamine</span><span class="sxs-lookup"><span data-stu-id="b07fb-114">Step 2: Record test results</span></span>

<span data-ttu-id="b07fb-115">Testitulemuste salvestamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="b07fb-115">To record test results, follow these steps.</span></span>

1. <span data-ttu-id="b07fb-116">Valige **Tulemid**.</span><span class="sxs-lookup"><span data-stu-id="b07fb-116">Select **Results**.</span></span>
1. <span data-ttu-id="b07fb-117">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="b07fb-117">Select **Edit**.</span></span>
1. <span data-ttu-id="b07fb-118">Sisestage number väljale **Tulemuse kogus**.</span><span class="sxs-lookup"><span data-stu-id="b07fb-118">In the **Result quantity** field, enter a number.</span></span>
1. <span data-ttu-id="b07fb-119">Valige väljal **Tulemus** soovitud ettevõte.</span><span class="sxs-lookup"><span data-stu-id="b07fb-119">In the **Outcome** field, select the desired record.</span></span> <span data-ttu-id="b07fb-120">Selles näites põhineb tulemus eelmääratletud tulemusel.</span><span class="sxs-lookup"><span data-stu-id="b07fb-120">In this example, the result is based on a predefined outcome.</span></span> <span data-ttu-id="b07fb-121">Tavaliselt saate salvestada täpsema katse tulemuse, nt suuruse või muu dimensiooni.</span><span class="sxs-lookup"><span data-stu-id="b07fb-121">Usually, you will record a more specific test result, such as a size or other dimension.</span></span>
1. <span data-ttu-id="b07fb-122">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="b07fb-122">Select **Save**.</span></span>
1. <span data-ttu-id="b07fb-123">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b07fb-123">Close the page.</span></span>

## <a name="step-3-validate-the-quality-order"></a><span data-ttu-id="b07fb-124">3. samm. Kvaliteettellimuse õigsuse kontrollimine</span><span class="sxs-lookup"><span data-stu-id="b07fb-124">Step 3: Validate the quality order</span></span>

<span data-ttu-id="b07fb-125">Kvaliteeditellimuse valideerimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="b07fb-125">To validate the quality order, follow these steps.</span></span>

1. <span data-ttu-id="b07fb-126">Valige **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="b07fb-126">Select **Validate**.</span></span>
1. <span data-ttu-id="b07fb-127">Valige väljal **Valideerija** kasutaja, kes inspektsiooni läbi viib.</span><span class="sxs-lookup"><span data-stu-id="b07fb-127">In the **Validated by** field, select the user who is doing the inspection.</span></span>
1. <span data-ttu-id="b07fb-128">Valige käsk **Vali**.</span><span class="sxs-lookup"><span data-stu-id="b07fb-128">Select **Select**.</span></span>
1. <span data-ttu-id="b07fb-129">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="b07fb-129">Select **OK**.</span></span>
1. <span data-ttu-id="b07fb-130">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b07fb-130">Close the page.</span></span>

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
