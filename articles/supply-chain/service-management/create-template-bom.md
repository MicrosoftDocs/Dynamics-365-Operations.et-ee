---
title: Käsitsi koostatava mallkoosluse loomine
description: Saate luua mallkoosluse, kasutades mitmesuguseid meetodeid.
author: ShylaThompson
manager: tfehr
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5afcb8171b674281faf8100d5c01fdff8d6ff764
ms.sourcegitcommit: 34b8f6f5c6134b7b97a9fb41d0b2e63215c67062
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/17/2021
ms.locfileid: "5470758"
---
# <a name="create-a-template-bom"></a><span data-ttu-id="68ea7-103">Käsitsi koostatava mallkoosluse loomine</span><span class="sxs-lookup"><span data-stu-id="68ea7-103">Create a template BOM</span></span>   

[!include [banner](../includes/banner.md)]


<span data-ttu-id="68ea7-104">Saate luua mallkoosluse, kasutades üht järgmistest meetoditest.</span><span class="sxs-lookup"><span data-stu-id="68ea7-104">You can create a template BOM by using any of the following methods.</span></span> <span data-ttu-id="68ea7-105">Kõikide meetodite puhul on väljad **Kuupäevast** ja **Kuupäevani** valikulised ja ainult informatiivsed.</span><span class="sxs-lookup"><span data-stu-id="68ea7-105">For all methods, the **From date** and **To date** fields are optional and for information only.</span></span>

## <a name="create-a-template-bom-manually"></a><span data-ttu-id="68ea7-106">Mallkoosluse loomine käsitsi</span><span class="sxs-lookup"><span data-stu-id="68ea7-106">Create a template BOM manually</span></span>

1.  <span data-ttu-id="68ea7-107">Valige **Teenuste haldus** \> **Seadistus** \> **Teenuse objektid** \> **Mallkooslused**.</span><span class="sxs-lookup"><span data-stu-id="68ea7-107">Go to **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="68ea7-108">Vormi **Mallkoosluse loomine** avamiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="68ea7-108">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="68ea7-109">Valige jaotisest **Kopeeri koosluseread viitest** suvand **Käsitsi**.</span><span class="sxs-lookup"><span data-stu-id="68ea7-109">Under **Copy BOM lines from reference**, select the **Manual** option.</span></span>

4.  <span data-ttu-id="68ea7-110">Sisestage väljale **Kaubakood** kaup tüübist **Kooslus** .</span><span class="sxs-lookup"><span data-stu-id="68ea7-110">In the **Item number** field, enter an item of the type **BOM**.</span></span>

5.  <span data-ttu-id="68ea7-111">Sisestage malli nimi väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="68ea7-111">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="68ea7-112">Sisestage väljadele **Kuupäevast** ja **Kuupäevani** kuupäevade vahemik, millal mallkooslus on aktiveeritud.</span><span class="sxs-lookup"><span data-stu-id="68ea7-112">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="68ea7-113">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="68ea7-113">Select **OK**.</span></span>

<span data-ttu-id="68ea7-114">Luuakse uus tühi mallkooslus.</span><span class="sxs-lookup"><span data-stu-id="68ea7-114">A new, blank template BOM is created.</span></span>

## <a name="create-a-template-bom-based-on-another-template-bom"></a><span data-ttu-id="68ea7-115">Mallkoosluse loomine teise mallkoosluse baasil</span><span class="sxs-lookup"><span data-stu-id="68ea7-115">Create a template BOM based on another template BOM</span></span>

1.  <span data-ttu-id="68ea7-116">Valige **Teenuste haldus** \> **Seadistus** \> **Teenuse objektid** \> **Mallkooslused**.</span><span class="sxs-lookup"><span data-stu-id="68ea7-116">Select **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="68ea7-117">Vormi **Mallkoosluse loomine** avamiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="68ea7-117">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="68ea7-118">Valige jaotisest **Kopeeri koosluseread viitest** suvand **Mallkooslus**.</span><span class="sxs-lookup"><span data-stu-id="68ea7-118">Under **Copy BOM lines from reference**, select the **Template BOM** option.</span></span>

4.  <span data-ttu-id="68ea7-119">Valige väljal **Viitenumber** olemasolev mallkooslus, mida soovite uude mallkooslusesse kopeerida.</span><span class="sxs-lookup"><span data-stu-id="68ea7-119">In the **Reference number** field, select an existing template BOM to copy to your new template BOM.</span></span>

5.  <span data-ttu-id="68ea7-120">Sisestage malli nimi väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="68ea7-120">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="68ea7-121">Sisestage väljadele **Kuupäevast** ja **Kuupäevani** kuupäevade vahemik, millal mallkooslus on aktiveeritud.</span><span class="sxs-lookup"><span data-stu-id="68ea7-121">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="68ea7-122">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="68ea7-122">Select **OK**.</span></span>

<span data-ttu-id="68ea7-123">Luuakse uus mallkooslus, kasutades ridu, mis vastavad algse mallkoosluse ridadele.</span><span class="sxs-lookup"><span data-stu-id="68ea7-123">A new template BOM is created by using lines that correspond to the lines in the original template BOM.</span></span>

## <a name="create-a-template-bom-based-on-an-item-bom"></a><span data-ttu-id="68ea7-124">Mallkoosluse loomine teise mallkoosluse baasil</span><span class="sxs-lookup"><span data-stu-id="68ea7-124">Create a template BOM based on an item BOM</span></span>

1.  <span data-ttu-id="68ea7-125">Valige **Teenuste haldus** \> **Seadistus** \> **Teenuse objektid** \> **Mallkooslused**.</span><span class="sxs-lookup"><span data-stu-id="68ea7-125">Select **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="68ea7-126">Vormi **Mallkoosluse loomine** avamiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="68ea7-126">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="68ea7-127">Valige jaotisest **Kopeeri koosluseread viitest** suvand **Kooslus**.</span><span class="sxs-lookup"><span data-stu-id="68ea7-127">Under **Copy BOM lines from reference**, select **BOM**.</span></span>

4.  <span data-ttu-id="68ea7-128">Valige koosluse versioon väljal **Viitenumber**.</span><span class="sxs-lookup"><span data-stu-id="68ea7-128">In the **Reference number** field, select a BOM version.</span></span> <span data-ttu-id="68ea7-129">Kaup tüübist kooslus kopeeritakse väljale **Kaubakood**.</span><span class="sxs-lookup"><span data-stu-id="68ea7-129">An item of the type BOM is copied to the **Item number**.</span></span>

5.  <span data-ttu-id="68ea7-130">Sisestage malli nimi väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="68ea7-130">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="68ea7-131">Sisestage väljadele **Kuupäevast** ja **Kuupäevani** kuupäevade vahemik, millal mallkooslus on aktiveeritud.</span><span class="sxs-lookup"><span data-stu-id="68ea7-131">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="68ea7-132">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="68ea7-132">Select **OK**.</span></span>

<span data-ttu-id="68ea7-133">Uus mallkooslus on loodud kasutades ridu, mis vastavad tabelis **Kooslused** loendatud koosluse ridadele.</span><span class="sxs-lookup"><span data-stu-id="68ea7-133">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **Bills of materials**.</span></span>

## <a name="create-a-template-bom-based-on-a-production-bom"></a><span data-ttu-id="68ea7-134">Mallkoosluse loomine tootmiskoosluse baasil</span><span class="sxs-lookup"><span data-stu-id="68ea7-134">Create a template BOM based on a production BOM</span></span>

1.  <span data-ttu-id="68ea7-135">Valige **Teenuste haldus** \> **Seadistus** \> **Teenuse objektid** \> **Mallkooslused**.</span><span class="sxs-lookup"><span data-stu-id="68ea7-135">Select **Service management** \> **Setup** \> **Service objects** \> **Template BOMs**.</span></span>

2.  <span data-ttu-id="68ea7-136">Vormi **Mallkoosluse loomine** avamiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="68ea7-136">Select **New** to open the **Create template BOM** form.</span></span>

3.  <span data-ttu-id="68ea7-137">Valige jaotisest **Kopeeri koosluseread viitest** suvand **Tootmine**.</span><span class="sxs-lookup"><span data-stu-id="68ea7-137">Under **Copy BOM lines from reference**, select **Production**.</span></span>

4.  <span data-ttu-id="68ea7-138">Valige tootmiskooslus väljal **Viitenumber**.</span><span class="sxs-lookup"><span data-stu-id="68ea7-138">In the **Reference number** field, select a production BOM.</span></span>

5.  <span data-ttu-id="68ea7-139">Sisestage malli nimi väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="68ea7-139">In the **Name** field, enter a name for the template.</span></span>

6.  <span data-ttu-id="68ea7-140">Sisestage väljadele **Kuupäevast** ja **Kuupäevani** kuupäevade vahemik, millal mallkooslus on aktiveeritud.</span><span class="sxs-lookup"><span data-stu-id="68ea7-140">In the **From date** and **To date** fields, enter a date interval in which the template BOM is active.</span></span>

7.  <span data-ttu-id="68ea7-141">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="68ea7-141">Select **OK**.</span></span>

<span data-ttu-id="68ea7-142">Uus mallkooslus on loodud kasutades ridu, mis vastavad tabelis **Kooslus** loendatud koosluse ridadele.</span><span class="sxs-lookup"><span data-stu-id="68ea7-142">A new template BOM is created by using lines that correspond to the lines of the BOM listed in **BOM**.</span></span>

## <a name="see-also"></a><span data-ttu-id="68ea7-143">Vt ka</span><span class="sxs-lookup"><span data-stu-id="68ea7-143">See also</span></span>

[<span data-ttu-id="68ea7-144">Mallkooslused</span><span class="sxs-lookup"><span data-stu-id="68ea7-144">Template BOMs</span></span>](template-boms.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]