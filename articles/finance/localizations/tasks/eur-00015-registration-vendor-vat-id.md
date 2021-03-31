---
title: EUR-00015 Hankija KM ID registreerimine
description: See protseduur näitab, kuidas lisada hankija kontole KM registreerimise ID-sid ja maksuvabastuse numbrit.
author: v-oloski
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddress, RegNumTaxIdLookup
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: v-oloski
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cb72a5f187afe9ebe1081acd6fe0b039c370718e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5227902"
---
# <a name="eur-00015-registration-of-vendor-vat-id"></a><span data-ttu-id="e7efd-103">EUR-00015 Hankija KM ID registreerimine</span><span class="sxs-lookup"><span data-stu-id="e7efd-103">EUR-00015 Registration of vendor VAT ID</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e7efd-104">See protseduur näitab, kuidas lisada hankija kontole KM registreerimise ID-sid ja maksuvabastuse numbrit.</span><span class="sxs-lookup"><span data-stu-id="e7efd-104">This procedure shows how to add VAT registration IDs and a tax except number to a vendor account.</span></span> <span data-ttu-id="e7efd-105">See protsess on juriidiliste isikute ja klientide puhul sarnane.</span><span class="sxs-lookup"><span data-stu-id="e7efd-105">This process is similar for legal entities and customers.</span></span> 

<span data-ttu-id="e7efd-106">Enne seda protseduuri tuleb seadistada KM ID-d.</span><span class="sxs-lookup"><span data-stu-id="e7efd-106">Before you can complete this procedure you must set up VAT IDs.</span></span> <span data-ttu-id="e7efd-107">See protseduur kohaldub kõigile Euroopa riikidele/piirkondadele.</span><span class="sxs-lookup"><span data-stu-id="e7efd-107">This procedure applies to all European countries/regions.</span></span> <span data-ttu-id="e7efd-108">Protseduuri loomisel kasutati demoettevõtte DEMF, mille esmaseks aadressiks on Saksamaa, andmeid.</span><span class="sxs-lookup"><span data-stu-id="e7efd-108">The procedure was created using the demo data company DEMF with a primary address in Germany.</span></span> <span data-ttu-id="e7efd-109">See protseduur on mõeldud andmehalduse administraatoritele, ostureskontro juhile või müügireskontro juhile.</span><span class="sxs-lookup"><span data-stu-id="e7efd-109">This procedure is intended for a data management administrator, accounts payable manager, or accounts receivable manager.</span></span> <span data-ttu-id="e7efd-110">See protseduur on funktsiooni kohta, mis lisati rakenduse Dynamics 365 for Operations versioonis 1611.</span><span class="sxs-lookup"><span data-stu-id="e7efd-110">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>

1. <span data-ttu-id="e7efd-111">Minge jaotisse Ostureskontrod > Hankijad > Kõik hankijad.</span><span class="sxs-lookup"><span data-stu-id="e7efd-111">Go to Accounts payable > Vendors > All vendors.</span></span>
2. <span data-ttu-id="e7efd-112">Otsige ja valige loendist hankija DE-01001</span><span class="sxs-lookup"><span data-stu-id="e7efd-112">In the list find and select vendor DE-01001</span></span>
3. <span data-ttu-id="e7efd-113">Klõpsake valikut Registreerimise ID-d.</span><span class="sxs-lookup"><span data-stu-id="e7efd-113">Click Registration IDs.</span></span>
4. <span data-ttu-id="e7efd-114">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="e7efd-114">Click Add.</span></span>
5. <span data-ttu-id="e7efd-115">Valige KM ID.</span><span class="sxs-lookup"><span data-stu-id="e7efd-115">Select VAT ID.</span></span>
6. <span data-ttu-id="e7efd-116">Tippige väärtus väljale Registreerimisnumber.</span><span class="sxs-lookup"><span data-stu-id="e7efd-116">In the Registration number field, type a value.</span></span>
    * <span data-ttu-id="e7efd-117">Määrake valitud hankijale Saksamaa KM ID.</span><span class="sxs-lookup"><span data-stu-id="e7efd-117">Specify a VAT ID in Germany for the selected vendor.</span></span> <span data-ttu-id="e7efd-118">ID peab vastama registreerimistüübi määratud vormingule.</span><span class="sxs-lookup"><span data-stu-id="e7efd-118">The ID must match the specified format of the registration type.</span></span>  
7. <span data-ttu-id="e7efd-119">Klõpsake vahekaarti Üldine.</span><span class="sxs-lookup"><span data-stu-id="e7efd-119">Click the General tab.</span></span>
8. <span data-ttu-id="e7efd-120">Sisestage kuupäev väljale Jõustunud.</span><span class="sxs-lookup"><span data-stu-id="e7efd-120">In the Effective field, enter a date.</span></span>
9. <span data-ttu-id="e7efd-121">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e7efd-121">Click Save.</span></span>
10. <span data-ttu-id="e7efd-122">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e7efd-122">Click New.</span></span>
11. <span data-ttu-id="e7efd-123">Sisestage väärtus väljale Nimi või kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="e7efd-123">In the Name or description field, type a value.</span></span>
    * <span data-ttu-id="e7efd-124">Sisestage näiteks ITA.</span><span class="sxs-lookup"><span data-stu-id="e7efd-124">For example, enter ITA.</span></span>  
12. <span data-ttu-id="e7efd-125">Sisestage või valige väärtus väljal Riik/piirkond.</span><span class="sxs-lookup"><span data-stu-id="e7efd-125">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="e7efd-126">Valige näiteks ITA.</span><span class="sxs-lookup"><span data-stu-id="e7efd-126">For example, select ITA.</span></span>  
13. <span data-ttu-id="e7efd-127">Valige Jah väljal Riigi puhul esmane.</span><span class="sxs-lookup"><span data-stu-id="e7efd-127">Select Yes in the Primary for country field.</span></span>
14. <span data-ttu-id="e7efd-128">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e7efd-128">Click Save.</span></span>
15. <span data-ttu-id="e7efd-129">Klõpsake vahekaarti Ülevaade.</span><span class="sxs-lookup"><span data-stu-id="e7efd-129">Click the Overview tab.</span></span>
16. <span data-ttu-id="e7efd-130">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="e7efd-130">Click Add.</span></span>
17. <span data-ttu-id="e7efd-131">Sisestage või valige väärtus väljal Registreerimise tüüp.</span><span class="sxs-lookup"><span data-stu-id="e7efd-131">In the Registration type field, enter or select a value.</span></span>
    * <span data-ttu-id="e7efd-132">Valige näiteks väärtus KM ID.</span><span class="sxs-lookup"><span data-stu-id="e7efd-132">For example, select VAT ID.</span></span>  
18. <span data-ttu-id="e7efd-133">Tippige väärtus väljale Registreerimisnumber.</span><span class="sxs-lookup"><span data-stu-id="e7efd-133">In the Registration number field, type a value.</span></span>
    * <span data-ttu-id="e7efd-134">Määrake näiteks KM ID Itaalias.</span><span class="sxs-lookup"><span data-stu-id="e7efd-134">For example, specify a VAT ID in Italy.</span></span>  <span data-ttu-id="e7efd-135">ID-l peab olema registreerimistüübiga sama vorming.</span><span class="sxs-lookup"><span data-stu-id="e7efd-135">The ID must have the same format as the registration type.</span></span>  
19. <span data-ttu-id="e7efd-136">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e7efd-136">Click Save.</span></span>
20. <span data-ttu-id="e7efd-137">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e7efd-137">Close the page.</span></span>
21. <span data-ttu-id="e7efd-138">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e7efd-138">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e7efd-139">Valige näiteks DE-01001.</span><span class="sxs-lookup"><span data-stu-id="e7efd-139">For example, select DE-01001.</span></span>  
22. <span data-ttu-id="e7efd-140">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e7efd-140">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="e7efd-141">Laiendage jaotist Arve ja tarne.</span><span class="sxs-lookup"><span data-stu-id="e7efd-141">Expand the Invoice and delivery section.</span></span>
24. <span data-ttu-id="e7efd-142">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="e7efd-142">Click Edit.</span></span>
25. <span data-ttu-id="e7efd-143">Sisestage või valige väärtus väljal Maksuvabastuse number.</span><span class="sxs-lookup"><span data-stu-id="e7efd-143">In the Tax exempt number field, enter or select a value.</span></span>
26. <span data-ttu-id="e7efd-144">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e7efd-144">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]