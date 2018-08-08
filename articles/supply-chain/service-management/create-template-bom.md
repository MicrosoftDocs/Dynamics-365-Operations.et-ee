---
title: "Käsitsi koostatava mallkoosluse loomine"
description: Saate luua mallkoosluse, kasutades mitmesuguseid meetodeid.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 89c5d45ac27a8678c51fb63c0326c2802a094596
ms.contentlocale: et-ee
ms.lasthandoff: 08/07/2018

---

# <a name="create-a-template-bom"></a><span data-ttu-id="8ee20-103">Käsitsi koostatava mallkoosluse loomine</span><span class="sxs-lookup"><span data-stu-id="8ee20-103">Create a template BOM</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="8ee20-104">Saate luua mallkoosluse, kasutades üht järgmistest meetoditest.</span><span class="sxs-lookup"><span data-stu-id="8ee20-104">You can create a template BOM by using any of the following methods.</span></span> <span data-ttu-id="8ee20-105">Kõikide meetodite puhul on väljad **Kuupäevast** ja **Kuupäevani** valikulised ja ainult informatiivsed.</span><span class="sxs-lookup"><span data-stu-id="8ee20-105">For all methods, the **From date** and **To date** fields are optional and for information only.</span></span>

## <a name="create-a-template-bom-manually"></a><span data-ttu-id="8ee20-106">Mallkoosluse loomine käsitsi</span><span class="sxs-lookup"><span data-stu-id="8ee20-106">Create a template BOM manually</span></span>

1.  <span data-ttu-id="8ee20-107">Klõpsake valikut **Teenuste halduse** \> **Seadistus** \> **Teenuse objektid** \> **Mallkooslused**.</span><span class="sxs-lookup"><span data-stu-id="8ee20-107">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="8ee20-108">Vormi **Mallkoosluse loomine** avamiseks vajutage klahvikombinatsiooni CTRL + N.</span><span class="sxs-lookup"><span data-stu-id="8ee20-108">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="8ee20-109">Valige jaotisest **Kopeeri koosluseread viitest** suvand **Käsitsi**.</span><span class="sxs-lookup"><span data-stu-id="8ee20-109">Under **Copy BOM lines from reference**, select the **Manual** option.</span></span>

4.  <span data-ttu-id="8ee20-110">Sisestage väljale **Kaubakood** kaup tüübist **Kooslus** .</span><span class="sxs-lookup"><span data-stu-id="8ee20-110">In the **Item number** field, enter an item of the type **BOM**.</span></span>

5.  <span data-ttu-id="8ee20-111">Sisestage malli nimi väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="8ee20-111">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="8ee20-112">Sisestage väljadele **Kuupäevast** ja **Kuupäevani** kuupäevade vahemik, millal mallkooslus on aktiveeritud.</span><span class="sxs-lookup"><span data-stu-id="8ee20-112">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="8ee20-113">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="8ee20-113">Click **OK**.</span></span>

<span data-ttu-id="8ee20-114">Luuakse uus tühi mallkooslus.</span><span class="sxs-lookup"><span data-stu-id="8ee20-114">A new, blank template BOM is created.</span></span>

## <a name="create-a-template-bom-based-on-another-template-bom"></a><span data-ttu-id="8ee20-115">Mallkoosluse loomine teise mallkoosluse baasil</span><span class="sxs-lookup"><span data-stu-id="8ee20-115">Create a template BOM based on another template BOM</span></span>

1.  <span data-ttu-id="8ee20-116">Klõpsake valikut **Teenuste halduse** \> **Seadistus** \> **Teenuse objektid** \> **Mallkooslused**.</span><span class="sxs-lookup"><span data-stu-id="8ee20-116">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="8ee20-117">Vormi **Mallkoosluse loomine** avamiseks vajutage klahvikombinatsiooni CTRL + N.</span><span class="sxs-lookup"><span data-stu-id="8ee20-117">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="8ee20-118">Valige jaotisest **Kopeeri koosluseread viitest** suvand **Mallkooslus**.</span><span class="sxs-lookup"><span data-stu-id="8ee20-118">Under **Copy BOM lines from reference**, select the **Template BOM** option.</span></span>

4.  <span data-ttu-id="8ee20-119">Valige väljal **Viitenumber** olemasolev mallkooslus, mida soovite uude mallkooslusesse kopeerida.</span><span class="sxs-lookup"><span data-stu-id="8ee20-119">In the **Reference number** field, select an existing template BOM to copy to your new template BOM.</span></span>

5.  <span data-ttu-id="8ee20-120">Sisestage malli nimi väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="8ee20-120">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="8ee20-121">Sisestage väljadele **Kuupäevast** ja **Kuupäevani** kuupäevade vahemik, millal mallkooslus on aktiveeritud.</span><span class="sxs-lookup"><span data-stu-id="8ee20-121">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="8ee20-122">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="8ee20-122">Click **OK**.</span></span>

<span data-ttu-id="8ee20-123">Luuakse uus mallkooslus, kasutades ridu, mis vastavad algse mallkoosluse ridadele.</span><span class="sxs-lookup"><span data-stu-id="8ee20-123">A new template BOM is created by using lines that correspond to the lines in the original template BOM.</span></span>

## <a name="create-a-template-bom-based-on-an-item-bom"></a><span data-ttu-id="8ee20-124">Mallkoosluse loomine teise mallkoosluse baasil</span><span class="sxs-lookup"><span data-stu-id="8ee20-124">Create a template BOM based on an item BOM</span></span>

1.  <span data-ttu-id="8ee20-125">Klõpsake valikut **Teenuste halduse** \> **Seadistus** \> **Teenuse objektid** \> **Mallkooslused**.</span><span class="sxs-lookup"><span data-stu-id="8ee20-125">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="8ee20-126">Vormi **Mallkoosluse loomine** avamiseks vajutage klahvikombinatsiooni CTRL + N.</span><span class="sxs-lookup"><span data-stu-id="8ee20-126">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="8ee20-127">Valige jaotisest **Kopeeri koosluseread viitest** suvand **Kooslus**.</span><span class="sxs-lookup"><span data-stu-id="8ee20-127">Under **Copy BOM lines from reference**, select **BOM**.</span></span>

4.  <span data-ttu-id="8ee20-128">Valige koosluse versioon väljal **Viitenumber**.</span><span class="sxs-lookup"><span data-stu-id="8ee20-128">In the **Reference number** field, select a BOM version.</span></span> <span data-ttu-id="8ee20-129">Kaup tüübist kooslus kopeeritakse väljale **Kaubakood**.</span><span class="sxs-lookup"><span data-stu-id="8ee20-129">An item of the type BOM is copied to the **Item number**.</span></span>

5.  <span data-ttu-id="8ee20-130">Sisestage malli nimi väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="8ee20-130">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="8ee20-131">Sisestage väljadele **Kuupäevast** ja **Kuupäevani** kuupäevade vahemik, millal mallkooslus on aktiveeritud.</span><span class="sxs-lookup"><span data-stu-id="8ee20-131">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="8ee20-132">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="8ee20-132">Click **OK**.</span></span>

<span data-ttu-id="8ee20-133">Uus mallkooslus on loodud kasutades ridu, mis vastavad tabelis **Kooslused** loendatud koosluse ridadele.</span><span class="sxs-lookup"><span data-stu-id="8ee20-133">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **Bills of materials**.</span></span>

## <a name="create-a-template-bom-based-on-a-production-bom"></a><span data-ttu-id="8ee20-134">Mallkoosluse loomine tootmiskoosluse baasil</span><span class="sxs-lookup"><span data-stu-id="8ee20-134">Create a template BOM based on a production BOM</span></span>

1.  <span data-ttu-id="8ee20-135">Klõpsake valikut **Teenuste halduse** \> **Seadistus** \> **Teenuse objektid** \> **Mallkooslused**.</span><span class="sxs-lookup"><span data-stu-id="8ee20-135">Click **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="8ee20-136">Vormi **Mallkoosluse loomine** avamiseks vajutage klahvikombinatsiooni CTRL + N.</span><span class="sxs-lookup"><span data-stu-id="8ee20-136">Press CTRL+N to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="8ee20-137">Valige jaotisest **Kopeeri koosluseread viitest** suvand **Tootmine**.</span><span class="sxs-lookup"><span data-stu-id="8ee20-137">Under **Copy BOM lines from reference**, select **Production**.</span></span>

4.  <span data-ttu-id="8ee20-138">Valige tootmiskooslus väljal **Viitenumber**.</span><span class="sxs-lookup"><span data-stu-id="8ee20-138">In the **Reference number** field, select a production BOM.</span></span>

5.  <span data-ttu-id="8ee20-139">Sisestage malli nimi väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="8ee20-139">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="8ee20-140">Sisestage väljadele **Kuupäevast** ja **Kuupäevani** kuupäevade vahemik, millal mallkooslus on aktiveeritud.</span><span class="sxs-lookup"><span data-stu-id="8ee20-140">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="8ee20-141">Klõpsake nupul **OK**.</span><span class="sxs-lookup"><span data-stu-id="8ee20-141">Click **OK**.</span></span>

<span data-ttu-id="8ee20-142">Uus mallkooslus on loodud kasutades ridu, mis vastavad tabelis **Kooslus** loendatud koosluse ridadele.</span><span class="sxs-lookup"><span data-stu-id="8ee20-142">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **BOM**.</span></span>

## <a name="see-also"></a><span data-ttu-id="8ee20-143">Vt ka</span><span class="sxs-lookup"><span data-stu-id="8ee20-143">See also</span></span>

[<span data-ttu-id="8ee20-144">Mallkooslused</span><span class="sxs-lookup"><span data-stu-id="8ee20-144">Template BOMs</span></span>](template-boms.md)

  



