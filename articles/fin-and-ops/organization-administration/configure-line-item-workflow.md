---
title: "Rea kauba töövoogude konfigureerimine"
description: "Selles teemas selgitatakse, kuidas konfigureerida rea kauba töövoo elementi."
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: 66e79389bba4566176330914ace462110cd0aa22
ms.contentlocale: et-ee
ms.lasthandoff: 12/18/2018

---

# <a name="configure-line-item-workflows"></a><span data-ttu-id="3c386-103">Rea kauba töövoogude konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="3c386-103">Configure line-item workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3c386-104">Selles teemas selgitatakse, kuidas konfigureerida rea kauba töövoo elementi.</span><span class="sxs-lookup"><span data-stu-id="3c386-104">This topic explains how to configure a line-item workflow element.</span></span>

<span data-ttu-id="3c386-105">Töövooredaktoris rea kauba töövoo elemendi konfigureerimiseks paremklõpsake elementi ja seejärel klõpsake valikut **Atribuudid**, et avada leht **Atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="3c386-105">To configure a line-item workflow element, in the workflow editor, right-click the element, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="3c386-106">Seejärel kasutage rea kauba töövoo elemendi atribuutide konfigureerimiseks järgmisi protseduure.</span><span class="sxs-lookup"><span data-stu-id="3c386-106">Then use the following procedures to configure the properties of the line-item workflow element.</span></span>

## <a name="name-the-line-item-workflow-element"></a><span data-ttu-id="3c386-107">Rea kauba töövoo elemendile nime andmine</span><span class="sxs-lookup"><span data-stu-id="3c386-107">Name the line-item workflow element</span></span>

<span data-ttu-id="3c386-108">Tehke rea kauba töövoo elemendile nime sisestamiseks järgmist.</span><span class="sxs-lookup"><span data-stu-id="3c386-108">Follow these steps to enter a name for the line-item workflow element.</span></span>

1. <span data-ttu-id="3c386-109">Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.</span><span class="sxs-lookup"><span data-stu-id="3c386-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="3c386-110">Sisestage väljale **Nimi** rea kauba töövoo elemendi jaoks kordumatu nimi.</span><span class="sxs-lookup"><span data-stu-id="3c386-110">In the **Name** field, enter a unique name for the line-item workflow element.</span></span>

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a><span data-ttu-id="3c386-111">Määrake, kas sama töövoogu kasutatakse kõigi rea kaupade töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="3c386-111">Specify whether the same workflow is used to process all line items</span></span>

<span data-ttu-id="3c386-112">Järgige neid etappe, et määrata, kas sama töövoogu kasutatakse dokumendi kõigi rea kaupade töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="3c386-112">Follow these steps to specify whether the same workflow is used to process all the line items on a document.</span></span>

1. <span data-ttu-id="3c386-113">Klõpsake vasakpoolsel paanil suvandit **Põhisätted**.</span><span class="sxs-lookup"><span data-stu-id="3c386-113">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="3c386-114">Kui sama töövoog peab töötlema dokumendi kõiki rea kaupu, klõpsake valikut **Kutsu üksik töövoog kõigile rea kaupadele**.</span><span class="sxs-lookup"><span data-stu-id="3c386-114">If the same workflow should process all the line items on a document, click **Invoke a single workflow for all line-items**.</span></span> <span data-ttu-id="3c386-115">Seejärel valige töövoog, millega rea kaupu töödelda.</span><span class="sxs-lookup"><span data-stu-id="3c386-115">Then select the workflow to use to process the line items.</span></span>
3. <span data-ttu-id="3c386-116">Kui teatud töövoog peaks töötlema rea kaupu, mis vastavad määratud tingimustele, klõpsake valikut **Kutsu töövoog igale rea kaubale**.</span><span class="sxs-lookup"><span data-stu-id="3c386-116">If a specific workflow should process line items that meet a specific set of conditions, click **Invoke a workflow for each line-item**.</span></span> <span data-ttu-id="3c386-117">Järgige neid etappe tingimustekogumi määratlemiseks.</span><span class="sxs-lookup"><span data-stu-id="3c386-117">Then follow these steps to define the set of conditions:</span></span>

    1. <span data-ttu-id="3c386-118">Klõpsake vahekaarti **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="3c386-118">Click **Add**.</span></span>
    2. <span data-ttu-id="3c386-119">Valige tabelist tingimus.</span><span class="sxs-lookup"><span data-stu-id="3c386-119">Select the condition in the table.</span></span>
    3. <span data-ttu-id="3c386-120">Sisestage vahekaardil **Tingimuse nimi** määratletava tingimustekogumi nimi.</span><span class="sxs-lookup"><span data-stu-id="3c386-120">On the **Condition name** tab, enter a name for the set of conditions that you're defining.</span></span>
    4. <span data-ttu-id="3c386-121">Tingimuse sisestamiseks klõpsake valikut **Lisa tingimus**.</span><span class="sxs-lookup"><span data-stu-id="3c386-121">Click **Add condition** to enter a condition.</span></span>
    5. <span data-ttu-id="3c386-122">Sisestage täiendavad vajalikud tingimused.</span><span class="sxs-lookup"><span data-stu-id="3c386-122">Enter any additional conditions that are required.</span></span>
    6. <span data-ttu-id="3c386-123">Kontrollimaks, kas sisestatud tingimustekogum on õigesti konfigureeritud, klõpsake käsku **Katseta**.</span><span class="sxs-lookup"><span data-stu-id="3c386-123">To verify that the set of conditions that you entered is configured correctly, click **Test**.</span></span> <span data-ttu-id="3c386-124">Lehel **Töövoo tingimuse katsetamine** alas **Kontrolli tingimust** valige kirje ja seejärel klõpsake käsku **Katseta**.</span><span class="sxs-lookup"><span data-stu-id="3c386-124">On the **Test workflow condition** page, in the **Validate condition** area, select a record, and then click **Test**.</span></span> <span data-ttu-id="3c386-125">Süsteem hindab kirjet otsustamaks, kas see vastab teie määratud tingimustele.</span><span class="sxs-lookup"><span data-stu-id="3c386-125">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span> <span data-ttu-id="3c386-126">Klõpsake **OK** või valikut **Tühista**, et naasta lehele **Atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="3c386-126">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

    <span data-ttu-id="3c386-127">Vahekaardil **Töövoog** valige töövoog, mida kasutada teie määratletud tingimustekogumile vastavate rea kaupade töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="3c386-127">On the **Workflow** tab, select the workflow select the workflow to use to process line items that meet the set of conditions that you defined.</span></span>

