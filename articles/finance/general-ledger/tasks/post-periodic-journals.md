---
title: Perioodiliste töölehtede sisestamine
description: Perioodilisi töölehti nimetatakse mõnikord korduvtöölehtedeks, kuna suurus, tekst ja muu teave kordub iga kord, kui tööleht sisestatakse.
author: aprilolson
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransPeriodic, LedgerJournalTransDaily
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4fdf630e9d292d0e016b6624a82b047d32bab898
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175384"
---
# <a name="post-periodic-journals"></a><span data-ttu-id="0038a-103">Perioodiliste töölehtede sisestamine</span><span class="sxs-lookup"><span data-stu-id="0038a-103">Post periodic journals</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0038a-104">Perioodilisi töölehti nimetatakse mõnikord korduvtöölehtedeks, kuna suurus, tekst ja muu teave kordub iga kord, kui tööleht sisestatakse.</span><span class="sxs-lookup"><span data-stu-id="0038a-104">Periodic journals are sometimes called recurring journals because the amount, text, and other information are repeated each time that the periodic journal is retrieved.</span></span> <span data-ttu-id="0038a-105">Perioodilise töölehe loomisel saate määrata perioodi kordumise intervalli, näiteks päeva või kuu.</span><span class="sxs-lookup"><span data-stu-id="0038a-105">When you create the periodic journal, you specify the period interval for the recurrence, such as days or months.</span></span> <span data-ttu-id="0038a-106">Selles tegevuse juhises luuakse igakuise kordumismustriga perioodiline tööleht.</span><span class="sxs-lookup"><span data-stu-id="0038a-106">This task guide will create a periodic journal with a monthly recurrence.</span></span>

1. <span data-ttu-id="0038a-107">Avage **Navigeerimispaan > Moodulid > Pearaamat > Perioodilised ülesanded > Perioodilised töölehed**.</span><span class="sxs-lookup"><span data-stu-id="0038a-107">Go to **Navigation pane > Modules > General ledger > Periodic tasks > Periodic journals**.</span></span>
2. <span data-ttu-id="0038a-108">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="0038a-108">Click **New**.</span></span>
3. <span data-ttu-id="0038a-109">Sisestage või valige väärtus väljal **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="0038a-109">In the **Name** field, enter or select a value.</span></span>
4. <span data-ttu-id="0038a-110">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="0038a-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="0038a-111">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="0038a-111">In the **Description** field, type a value.</span></span> <span data-ttu-id="0038a-112">See kirjeldus on hiljem ka perioodilise töölehe nimi, seetõttu tasub sellele anda asjakohane nimi.</span><span class="sxs-lookup"><span data-stu-id="0038a-112">The description will be the name of the Periodic journal when retrieved later so make sure to give it a relevant name.</span></span>
6. <span data-ttu-id="0038a-113">Klõpsake paanil **Tegevuspaan** valikut **Read**.</span><span class="sxs-lookup"><span data-stu-id="0038a-113">On the **Action pane**, click **Lines**.</span></span> <span data-ttu-id="0038a-114">Perioodilisel töölehel on tavaliselt mitu töölehe rida.</span><span class="sxs-lookup"><span data-stu-id="0038a-114">A periodic journal will typically include several journal lines.</span></span> <span data-ttu-id="0038a-115">Selles ülesandes lisatakse sellele siiski vaid üks rida.</span><span class="sxs-lookup"><span data-stu-id="0038a-115">this task guide will however only add one line.</span></span>
7. <span data-ttu-id="0038a-116">Väljale **Kuupäev** sisestage kuupäev.</span><span class="sxs-lookup"><span data-stu-id="0038a-116">In the **Date** field, enter a date.</span></span> <span data-ttu-id="0038a-117">Väli **Kuupäev** sisaldab järgmise päevase töölehe kande sisestuskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="0038a-117">The **Date** field contains the posting date for the next transfer to the daily journal.</span></span> <span data-ttu-id="0038a-118">Igakuiste töölehtede puhul on soovitatav kasutada kuupäeva, mil see sisestatakse, tavaliselt kas esimene viimane kuupäev perioodis.</span><span class="sxs-lookup"><span data-stu-id="0038a-118">For journals that will be retrieved each month it is recommended to use the date in the month when it will be posted, typically the first or last date in the period.</span></span> <span data-ttu-id="0038a-119">Kasutades välja Tühi kuupäev võite jätta välja Kuupäev tühjaks ning lisada selle siis, kui tööleht on toodud.</span><span class="sxs-lookup"><span data-stu-id="0038a-119">It is possible to leave the Date field blank and to give a date when the journal is retrieved, using the Empty date field.</span></span> <span data-ttu-id="0038a-120">Välja värskendatakse automaatselt järgmise korduva kuupäevani, kui kandeid tuuakse.</span><span class="sxs-lookup"><span data-stu-id="0038a-120">The field is automatically updated to the next recurring date when transactions are retrieved.</span></span> 
8. <span data-ttu-id="0038a-121">Täpsustage soovitud väärtusi väljal **Konto**.</span><span class="sxs-lookup"><span data-stu-id="0038a-121">In the **Account** field, specify the desired values.</span></span>
9. <span data-ttu-id="0038a-122">Valige väärtus väljal **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="0038a-122">In the **Description** field, select a value.</span></span>
10. <span data-ttu-id="0038a-123">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="0038a-123">Close the page.</span></span>
11. <span data-ttu-id="0038a-124">Sisestage arv väljale **Deebet**.</span><span class="sxs-lookup"><span data-stu-id="0038a-124">In the **Debit** field, enter a number.</span></span>
12. <span data-ttu-id="0038a-125">Määratlega väljal **Vastaskonto** soovitud väärtused.</span><span class="sxs-lookup"><span data-stu-id="0038a-125">In the **Offset account** field, specify the desired values.</span></span>
13. <span data-ttu-id="0038a-126">Valige Kuud väljal **Ühik**.</span><span class="sxs-lookup"><span data-stu-id="0038a-126">In the **Unit** field, select 'Months'.</span></span>
14. <span data-ttu-id="0038a-127">Sisestage number 1 väljale **Ühikute arv**.</span><span class="sxs-lookup"><span data-stu-id="0038a-127">In the **Number of units** field, enter '1'.</span></span>
15. <span data-ttu-id="0038a-128">Sisestage kuupäev väljale **Lõpukuupäev**.</span><span class="sxs-lookup"><span data-stu-id="0038a-128">In the **Last date** field, enter a date.</span></span> <span data-ttu-id="0038a-129">Eelmise perioodi viimase kuupäeva sisestamine aitab vältida kogemata korduvtöölehe loomist valesse algusperioodi.</span><span class="sxs-lookup"><span data-stu-id="0038a-129">Entering last date in the preceding period will prevent that the recurring journal by mistake is created in the wrong starting period.</span></span> <span data-ttu-id="0038a-130">Viimast kuupäeva värskendatakse hiljem iga kord, kui perioodilist töölehte tuuakse.</span><span class="sxs-lookup"><span data-stu-id="0038a-130">Last date will later on be updated each time the periodic journal is retrieved.</span></span> 
16. <span data-ttu-id="0038a-131">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="0038a-131">Click **Save**.</span></span>
17. <span data-ttu-id="0038a-132">Avage **Navigeerimispaan > Moodulid > Pearaamat > Töölehe kanded > Päevaraamatud**.</span><span class="sxs-lookup"><span data-stu-id="0038a-132">Go to **Navigation pane > Modules > General ledger > Journal entries > General journals**.</span></span>
18. <span data-ttu-id="0038a-133">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="0038a-133">Click **New**.</span></span>
19. <span data-ttu-id="0038a-134">Sisestage või valige väärtus väljal **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="0038a-134">In the **Name** field, enter or select a value.</span></span>
20. <span data-ttu-id="0038a-135">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="0038a-135">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="0038a-136">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="0038a-136">In the list, click the link in the selected row.</span></span>
22. <span data-ttu-id="0038a-137">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="0038a-137">In the **Description** field, type a value.</span></span>
23. <span data-ttu-id="0038a-138">Klõpsake paanil **Tegevuspaan** valikut **Read**.</span><span class="sxs-lookup"><span data-stu-id="0038a-138">On the **Action pane**, click **Lines**.</span></span>
24. <span data-ttu-id="0038a-139">Paanil **Toimingupaan** klõpsake **Perioodiline tööleht**.</span><span class="sxs-lookup"><span data-stu-id="0038a-139">On the **Action pane**, click **Period journal**.</span></span>
25. <span data-ttu-id="0038a-140">Klõpsake käsku **Too tööleht**.</span><span class="sxs-lookup"><span data-stu-id="0038a-140">Click **Retrieve journal**.</span></span>
26. <span data-ttu-id="0038a-141">Sisestage kuupäev väljale **Lõppkuupäev**.</span><span class="sxs-lookup"><span data-stu-id="0038a-141">In the **To date** field, enter a date.</span></span> <span data-ttu-id="0038a-142">**Lõppkuupäev** toimib perioodiliste kannete ridadel nagu äralõikekuupäev.</span><span class="sxs-lookup"><span data-stu-id="0038a-142">The **To date** serves as the cutoff date for the periodic voucher lines.</span></span> <span data-ttu-id="0038a-143">Olenevalt kordussätetest võivad samal real paiknevad Viimane kuupäev ja Lõpukuupäev esineda tulemuseks oleval töölehel rohkem kui ühel korral.</span><span class="sxs-lookup"><span data-stu-id="0038a-143">Based on the recurrence setting, the Last date and To date the same line might be included more than once in the resulting journal.</span></span> <span data-ttu-id="0038a-144">Lõpukuupäeva värskendatakse automaatselt olenevalt perioodilise rea viimase töölehele ülekandmise seansi kuupäevast.</span><span class="sxs-lookup"><span data-stu-id="0038a-144">To date is automatically updated based on  session date of the last time the periodic line was transferred to a journal.</span></span> 
27. <span data-ttu-id="0038a-145">Sisestage või valige väärtus väljal **Perioodilise töölehe kood**.</span><span class="sxs-lookup"><span data-stu-id="0038a-145">In the **Periodic journal number** field, enter or select a value.</span></span>
28. <span data-ttu-id="0038a-146">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="0038a-146">In the list, click the link in the selected row.</span></span>
29. <span data-ttu-id="0038a-147">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="0038a-147">Click **OK**.</span></span> <span data-ttu-id="0038a-148">Sõltuvalt nõuetest ja seadistusest saab nüüd perioodi töölehte üle vaadata, kinnitada või sisestada.</span><span class="sxs-lookup"><span data-stu-id="0038a-148">The period journal can now be reviewed, approved or posted depending on requirement and setup.</span></span>   
