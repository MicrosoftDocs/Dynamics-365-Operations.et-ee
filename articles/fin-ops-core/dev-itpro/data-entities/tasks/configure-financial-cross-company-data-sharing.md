---
title: Kontsernisisese finantsandmete ühiskasutuse konfigureerimine
description: Selles protseduuris selgitatakse, kuidas konfigureerida, lubada, kinnitada ja lahendada konflikte ettevõtete vahel andmeid ühiskasutades.
author: aprilolson
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportRnr, DMFExecutionHistoryWorkspace, DMFExecutionHistorySummary, DMFExecutionHistoryEntities,  SysDataSharingConfiguration, SysDataSharingDiscrepencies
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 35ec8fc809841c0830224646fb57b0e4e4d40ef4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752288"
---
# <a name="configure-financial-cross-company-data-sharing"></a><span data-ttu-id="9581d-103">Kontsernisisese finantsandmete ühiskasutuse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="9581d-103">Configure financial cross-company data sharing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9581d-104">Selles protseduuris selgitatakse, kuidas konfigureerida, lubada, kinnitada ja lahendada konflikte ettevõtete vahel andmeid ühiskasutades.</span><span class="sxs-lookup"><span data-stu-id="9581d-104">This procedure shows how to configure, enable, validate, and resolve conflicts when sharing data between companies.</span></span> <span data-ttu-id="9581d-105">See kasutab USMF-ettevõtet ja finantsandmete ühiskasutuse malli.</span><span class="sxs-lookup"><span data-stu-id="9581d-105">It uses the USMF company and the Financial data sharing template.</span></span>

<span data-ttu-id="9581d-106">Selle tegevusjuhise jaoks on nõutav Dynamics AX-i platvorm 7.1 või uuem.</span><span class="sxs-lookup"><span data-stu-id="9581d-106">This task guide requires Dynamics AX platform 7.1 or later.</span></span>

1. <span data-ttu-id="9581d-107">Avage **Navigatsioonipaan > Moodulid > Süsteemihaldus > Tööruumid > Andmehaldus**.</span><span class="sxs-lookup"><span data-stu-id="9581d-107">Go to **Navigation pane > Modules > System administration > Workspaces > Data management**.</span></span>
2. <span data-ttu-id="9581d-108">Klõpsake nuppu **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="9581d-108">Click **Import**.</span></span>
3. <span data-ttu-id="9581d-109">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="9581d-109">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="9581d-110">Valige pakendi tüüp väljal **Lähteandmete vorming**.</span><span class="sxs-lookup"><span data-stu-id="9581d-110">In the **Source data format** field, select the 'Package' type.</span></span> <span data-ttu-id="9581d-111">Klõpsake **Üleslaadimine**.</span><span class="sxs-lookup"><span data-stu-id="9581d-111">Click **Upload**.</span></span> <span data-ttu-id="9581d-112">Liikuge finantsandmete ühiskasutuse malli paketifaili asukohta ja valige see fail.</span><span class="sxs-lookup"><span data-stu-id="9581d-112">Navigate to the location of the Financial data sharing template package file and select that file.</span></span>
5. <span data-ttu-id="9581d-113">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="9581d-113">Click **Save**.</span></span>
6. <span data-ttu-id="9581d-114">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="9581d-114">In the list, mark the selected row.</span></span> <span data-ttu-id="9581d-115">Valige andmete ühiskasutuspoliitika, mis äsja loodi.</span><span class="sxs-lookup"><span data-stu-id="9581d-115">Select the data sharing policy that was just created.</span></span>  
7. <span data-ttu-id="9581d-116">Klõpsake nuppu **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="9581d-116">Click **Import**.</span></span>
8. <span data-ttu-id="9581d-117">Klõpsake valikut **Sule**.</span><span class="sxs-lookup"><span data-stu-id="9581d-117">Click **Close**.</span></span>
9. <span data-ttu-id="9581d-118">Värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="9581d-118">Refresh the page.</span></span>
10. <span data-ttu-id="9581d-119">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9581d-119">Close the page.</span></span>
11. <span data-ttu-id="9581d-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9581d-120">Close the page.</span></span>
12. <span data-ttu-id="9581d-121">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9581d-121">Close the page.</span></span>
13. <span data-ttu-id="9581d-122">Minge asukohta **Navigeerimispaan > Süsteemihaldus > Seadistus > Kontsernisisese andmete ühiskasutuse konfigureerimine**.</span><span class="sxs-lookup"><span data-stu-id="9581d-122">Go to **Navigation pane > Modules > System administration > Setup > Configure cross-company data sharing**.</span></span>
14. <span data-ttu-id="9581d-123">Otsige loendist ja valige **Maksepäevad**.</span><span class="sxs-lookup"><span data-stu-id="9581d-123">In the list, find and select **Payment days**.</span></span>
15. <span data-ttu-id="9581d-124">Klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="9581d-124">Click **Add**.</span></span>
16. <span data-ttu-id="9581d-125">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="9581d-125">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="9581d-126">Tippige USSI väljale **Ettevõte**.</span><span class="sxs-lookup"><span data-stu-id="9581d-126">In the **Company** field, type 'USSI'.</span></span>
18. <span data-ttu-id="9581d-127">Klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="9581d-127">Click **Add**.</span></span>
19. <span data-ttu-id="9581d-128">Tippige USMF väljale **Ettevõte**.</span><span class="sxs-lookup"><span data-stu-id="9581d-128">In the **Company** field, type 'USMF'.</span></span>
20. <span data-ttu-id="9581d-129">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="9581d-129">Click **Save**.</span></span>
21. <span data-ttu-id="9581d-130">Klõpsake käsku **Luba**.</span><span class="sxs-lookup"><span data-stu-id="9581d-130">Click **Enable**.</span></span>
22. <span data-ttu-id="9581d-131">Klõpsake nuppu **Jah**.</span><span class="sxs-lookup"><span data-stu-id="9581d-131">Click **Yes**.</span></span>
23. <span data-ttu-id="9581d-132">Klõpsake käsku **Otsi ühiskasutusprobleeme**.</span><span class="sxs-lookup"><span data-stu-id="9581d-132">Click **Find sharing issues**.</span></span>
24. <span data-ttu-id="9581d-133">Klõpsake nuppu **Jah**.</span><span class="sxs-lookup"><span data-stu-id="9581d-133">Click **Yes**.</span></span>
25. <span data-ttu-id="9581d-134">Klõpsake käsku **Värskenda välja väärtust**.</span><span class="sxs-lookup"><span data-stu-id="9581d-134">Click **Update field value**.</span></span>
26. <span data-ttu-id="9581d-135">Klõpsake käsku **Kasuta väärtust ettevõttest 1**.</span><span class="sxs-lookup"><span data-stu-id="9581d-135">Click **Use value from company 1**.</span></span>
27. <span data-ttu-id="9581d-136">Värskendage lehte.</span><span class="sxs-lookup"><span data-stu-id="9581d-136">Refresh the page.</span></span>
28. <span data-ttu-id="9581d-137">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="9581d-137">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]