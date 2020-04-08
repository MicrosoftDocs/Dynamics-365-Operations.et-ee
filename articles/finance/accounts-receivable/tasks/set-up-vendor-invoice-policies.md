---
title: Hankija arve poliitikate seadistamine
description: Selles teemas selgitatakse, kuidas seadistada tarnijate arvete poliitikat.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 58518f5291b70c63506c20717034daff0268901b
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143357"
---
# <a name="set-up-vendor-invoice-policies"></a><span data-ttu-id="58ee9-103">Hankija arve poliitikate seadistamine</span><span class="sxs-lookup"><span data-stu-id="58ee9-103">Set up vendor invoice policies</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="58ee9-104">Selles teemas selgitatakse, kuidas seadistada tarnijate arvete poliitikat.</span><span class="sxs-lookup"><span data-stu-id="58ee9-104">This topic explains how to set up vendor invoice policies.</span></span> <span data-ttu-id="58ee9-105">Hankija arvepoliitikad käivitatakse, kui sisestate hankija arve leheküljel Hankija arve ja avate lehekülje Hankija arve poliitika rikkumised.</span><span class="sxs-lookup"><span data-stu-id="58ee9-105">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="58ee9-106">Hankija arve töövoogu saate konfigureerida ka selliselt, et hankija arve poliitikad käivitatakse iga kord, kui sisestate arve töövoogu.</span><span class="sxs-lookup"><span data-stu-id="58ee9-106">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

- <span data-ttu-id="58ee9-107">Hankija arvepoliitikad ei kehti arvetele, mis on loodud arveregistris või arve töölehel.</span><span class="sxs-lookup"><span data-stu-id="58ee9-107">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span>  
- <span data-ttu-id="58ee9-108">Arvete võrdlemise kinnitamisel ei kasutata hankija arvepoliitikaid, vaid selle sätted määratakse leheküljel Ostureskontro parameetrid.</span><span class="sxs-lookup"><span data-stu-id="58ee9-108">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>  
- <span data-ttu-id="58ee9-109">Salvestamisel kasutatakse demoettevõtte USMF-i.</span><span class="sxs-lookup"><span data-stu-id="58ee9-109">This recording uses the USMF demo company.</span></span> <span data-ttu-id="58ee9-110">Järgmiste sammude tegemiseks on vaja ostureskontro juhi või pearaamatupidaja rolli.</span><span class="sxs-lookup"><span data-stu-id="58ee9-110">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="58ee9-111">Enne alustamist veenduge, et valitud on konfiguratsioonivõti Arvete vastendamine.</span><span class="sxs-lookup"><span data-stu-id="58ee9-111">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="58ee9-112">Hankija arve poliitikate loomise ettevalmistus</span><span class="sxs-lookup"><span data-stu-id="58ee9-112">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="58ee9-113">Avage **Navigeerimispaan > Moodulid > Ostureskontro > Häälestus > Ostureskontro parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="58ee9-113">Go to **Navigation pane > Modules > Accounts payable > Setup > Accounts payable parameters**.</span></span>
2. <span data-ttu-id="58ee9-114">Valige vahekaart **Arve kinnitamine**.</span><span class="sxs-lookup"><span data-stu-id="58ee9-114">Select the **Invoice validation** tab.</span></span>
3. <span data-ttu-id="58ee9-115">Valige või tühjendage oleku **Arve päise automaatne uuendamine** märkeruut.</span><span class="sxs-lookup"><span data-stu-id="58ee9-115">Select or clear the **Automatically update invoice header** status check box.</span></span>
4. <span data-ttu-id="58ee9-116">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="58ee9-116">Select **OK**.</span></span>
5. <span data-ttu-id="58ee9-117">Valige suvand väljal **Lahknevustega arve sisestamine**.</span><span class="sxs-lookup"><span data-stu-id="58ee9-117">In the **Post invoice with discrepancies** field, select an option.</span></span>
6. <span data-ttu-id="58ee9-118">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="58ee9-118">Close the page.</span></span>
7. <span data-ttu-id="58ee9-119">Avage **Navigeerimispaan > Moodulid > Ostureskontro > Poliitika häälestus > Hankija arve poliitika**.</span><span class="sxs-lookup"><span data-stu-id="58ee9-119">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
8. <span data-ttu-id="58ee9-120">Valige **Parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="58ee9-120">Select **Parameters**.</span></span>
9. <span data-ttu-id="58ee9-121">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="58ee9-121">Select **Add**.</span></span>
10. <span data-ttu-id="58ee9-122">Avalehele naasmiseks sulgege lehekülg.</span><span class="sxs-lookup"><span data-stu-id="58ee9-122">Close the page to return to the home page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="58ee9-123">Hankija arvete poliitika reegli tüüpide loomine</span><span class="sxs-lookup"><span data-stu-id="58ee9-123">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="58ee9-124">Avage **Navigeerimispaan > Moodulid > Ostureskontro > Poliitika häälestus > Hankija arve poliitika reegli tüübid**.</span><span class="sxs-lookup"><span data-stu-id="58ee9-124">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policy rule types**.</span></span>
2. <span data-ttu-id="58ee9-125">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="58ee9-125">Select **New**.</span></span>
3. <span data-ttu-id="58ee9-126">Sisestage väärtused väljadele **Reegli nimi** ja **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="58ee9-126">In the **Rule name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="58ee9-127">Valige väljal **Päringu nimi** otsingu avamiseks ripploendi nupp ja seejärel valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="58ee9-127">In the **Query name** field, select the drop-down button to open the lookup, then select the desired record.</span></span>
5. <span data-ttu-id="58ee9-128">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="58ee9-128">Select **Save**.</span></span>
6. <span data-ttu-id="58ee9-129">Avalehele naasmiseks sulgege lehekülg.</span><span class="sxs-lookup"><span data-stu-id="58ee9-129">Close the page to return to the home page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="58ee9-130">Hankija arvepoliitika määratlemine</span><span class="sxs-lookup"><span data-stu-id="58ee9-130">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="58ee9-131">Avage **Navigeerimispaan > Moodulid > Ostureskontro > Poliitika häälestus > Hankija arve poliitika**.</span><span class="sxs-lookup"><span data-stu-id="58ee9-131">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
2. <span data-ttu-id="58ee9-132">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="58ee9-132">Select **New**.</span></span>
3. <span data-ttu-id="58ee9-133">Sisestage väärtused väljadele **Nimi** ja **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="58ee9-133">In the **Name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="58ee9-134">Laiendage või ahendage jaotist **Poliitika organisatsioonid**.</span><span class="sxs-lookup"><span data-stu-id="58ee9-134">Expand or collapse the **Policy organizations** section.</span></span>
5. <span data-ttu-id="58ee9-135">Valige puust **Contoso Entertainment System USA**.</span><span class="sxs-lookup"><span data-stu-id="58ee9-135">In the tree, select **Contoso Entertainment System USA**.</span></span>
6. <span data-ttu-id="58ee9-136">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="58ee9-136">Select **Add**.</span></span>
7. <span data-ttu-id="58ee9-137">Laiendage või ahendage jaotist **Poliitika reeglid**.</span><span class="sxs-lookup"><span data-stu-id="58ee9-137">Expand or collapse the **Policy rules** section.</span></span>
8. <span data-ttu-id="58ee9-138">Valige **Poliitika reegli loomine**.</span><span class="sxs-lookup"><span data-stu-id="58ee9-138">Select **Create policy rule**.</span></span>
9. <span data-ttu-id="58ee9-139">Sisestage väärtus väljale **Poliitika reegli kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="58ee9-139">In the **Policy rule description** field, type a value.</span></span>
10. <span data-ttu-id="58ee9-140">Valige **Filter**.</span><span class="sxs-lookup"><span data-stu-id="58ee9-140">Select **Filter**.</span></span>
11. <span data-ttu-id="58ee9-141">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="58ee9-141">Select **Add**.</span></span> <span data-ttu-id="58ee9-142">Valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="58ee9-142">Select the desired record.</span></span>
12. <span data-ttu-id="58ee9-143">Väljadel **Tabel**, **Tuletatud tabel** ja **Väli**, valige või sisestage suvandid ripploendi menüüdest.</span><span class="sxs-lookup"><span data-stu-id="58ee9-143">In the **Table**, **Derived table**, and **Field** fields, select or enter options from the drop-down menus.</span></span>
13. <span data-ttu-id="58ee9-144">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="58ee9-144">Close the page.</span></span>
14. <span data-ttu-id="58ee9-145">Sisestage väärtus väljale **Kriteerium**.</span><span class="sxs-lookup"><span data-stu-id="58ee9-145">In the **Criteria** field, type a value.</span></span>
15. <span data-ttu-id="58ee9-146">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="58ee9-146">Select **OK**.</span></span>
16. <span data-ttu-id="58ee9-147">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="58ee9-147">Select **OK**.</span></span>
17. <span data-ttu-id="58ee9-148">Avalehele naasmiseks sulgege leheküljed.</span><span class="sxs-lookup"><span data-stu-id="58ee9-148">Close the pages to return to the home page.</span></span>

