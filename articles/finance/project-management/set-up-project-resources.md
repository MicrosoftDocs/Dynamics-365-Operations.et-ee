---
title: Projekti ressursside seadistamine
description: Selles teemas antakse teavet projekti ressursside seadistamise või taotlemise kohta.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c882e23794e3937f85b3e73774b36deaf28ac3ed
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760528"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="80f72-103">Projekti ressursside seadistamine</span><span class="sxs-lookup"><span data-stu-id="80f72-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="80f72-104">Peate seadistama kalendri ja seostama selle töötajaga.</span><span class="sxs-lookup"><span data-stu-id="80f72-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="80f72-105">Kalendrit kasutatakse projekti ja sellele reserveeritud ressursside tööaja plaanimiseks.</span><span class="sxs-lookup"><span data-stu-id="80f72-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="80f72-106">Kalendri seadistamisel saavad projektijuhid ressursside optimeerimise käigus ressursse ühtlustada.</span><span class="sxs-lookup"><span data-stu-id="80f72-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="80f72-107">Kalendrigraafiku alusel saab ressurssidele piiranguid seada.</span><span class="sxs-lookup"><span data-stu-id="80f72-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="80f72-108">Kalendri saab seadistada lehel **Kalendrid**.</span><span class="sxs-lookup"><span data-stu-id="80f72-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="80f72-109">Töötaja seadistamisel projekti ressursina saate valida töötajate hulgast, kes töötavad ettevõttes, millele ressursse seadistate.</span><span class="sxs-lookup"><span data-stu-id="80f72-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="80f72-110">Teine võimalus on valida töötajaid oma organisatsiooni teistest ettevõtetest.</span><span class="sxs-lookup"><span data-stu-id="80f72-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="80f72-111">Neid töötajaid nimetatakse kontsernisisesteks ressurssideks.</span><span class="sxs-lookup"><span data-stu-id="80f72-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="80f72-112">Järgmistes protseduurides selgitatakse, kuidas seadistada töötajat ettevõttes projektiressursina ja kuidas seadistada kontsernisisest projektiressurssi.</span><span class="sxs-lookup"><span data-stu-id="80f72-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="80f72-113">Töötaja seadistamine projekti ressursina</span><span class="sxs-lookup"><span data-stu-id="80f72-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="80f72-114">Valige lehel **Töötajad** loendist **Töötajad** töötaja, kelle projekti ressursina lisate, ja avage töötaja kirje..</span><span class="sxs-lookup"><span data-stu-id="80f72-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="80f72-115">Valige tegumiribalt **Projekt** &gt; **Seadistus** &gt; **Projekti seadistus**.</span><span class="sxs-lookup"><span data-stu-id="80f72-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="80f72-116">Valige kalender ja sulgege siis leht.</span><span class="sxs-lookup"><span data-stu-id="80f72-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="80f72-117">Saate määrata eelmäärangu tüübina ressursile ka vaikeprojekte.</span><span class="sxs-lookup"><span data-stu-id="80f72-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="80f72-118">Eelmääranguid saab kasutada, kui ressursihaldur või projektijuht teab ette, milliste projektidega ressurss töötama hakkab.</span><span class="sxs-lookup"><span data-stu-id="80f72-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="80f72-119">Eelmäärangud võivad põhineda ka projekti sponsori või kliendi soovil.</span><span class="sxs-lookup"><span data-stu-id="80f72-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="80f72-120">Projekti eelmääramiseks valige lehelt **Projektide määramine** vahekaardil **Projektid** loendis **Järelejäänud projektid** sobiv projekt.</span><span class="sxs-lookup"><span data-stu-id="80f72-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="80f72-121">Kontsernisisese ressursi seadistamine</span><span class="sxs-lookup"><span data-stu-id="80f72-121">Set up an intercompany resource</span></span>

<span data-ttu-id="80f72-122">Töötaja seadistamisel kontsernisisese ressursina peate tegema seadistuse nii välja laenavas ettevõttes kui ka laenuks võtvas ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="80f72-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="80f72-123">Välja laenavas ettevõttes tehke järgmist</span><span class="sxs-lookup"><span data-stu-id="80f72-123">In the lending company</span></span>

1. <span data-ttu-id="80f72-124">Kontrollige Finance’is, kas välja laenav ettevõte on valitud, ja läbige siis eelmises jaotises kirjeldatud protseduur „Töötaja seadistamine projekti ressursina“.</span><span class="sxs-lookup"><span data-stu-id="80f72-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="80f72-125">Tehke lehel **Kontserni raamatupidamine** valik **Uus**.</span><span class="sxs-lookup"><span data-stu-id="80f72-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="80f72-126">Valige väljalt **Juriidilise isiku ID** välja laenav ettevõte.</span><span class="sxs-lookup"><span data-stu-id="80f72-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="80f72-127">Täitke vajalikul viisil ülejäänud väljad ja valige siis **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="80f72-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="80f72-128">Tehke lehel **Ülekande hind** valik **Uus**.</span><span class="sxs-lookup"><span data-stu-id="80f72-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="80f72-129">Valige väljalt **Laenav juriidiline isik** sobiv ettevõte.</span><span class="sxs-lookup"><span data-stu-id="80f72-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="80f72-130">Selleks, et laenata laenuks võtvale ettevõttele ainult see ressurss, mille jaotise alguses väljal **Ressurss** lõite, valige loodud ressursi nimi.</span><span class="sxs-lookup"><span data-stu-id="80f72-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="80f72-131">Selleks, et teha välja laenavale ettevõttele kättesaadavaks kõik ettevõtte ressursid, jätke väli **Ressurss** tühjaks.</span><span class="sxs-lookup"><span data-stu-id="80f72-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="80f72-132">Määrake lehe **Projektihalduse ja raamatupidamise parameetrid** vahekaardil **Kontsernisisene** valiku **Luba kontsernisisene ressursside plaanimine ja ajatabelid** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="80f72-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="80f72-133">Laenuks võtvas ettevõttes tehke järgmist</span><span class="sxs-lookup"><span data-stu-id="80f72-133">In the borrowing company</span></span>

- <span data-ttu-id="80f72-134">Sisestage lehel **Ressursside loend** otsingufiltrisse välja laenava ettevõtte jaoks loodud ressursi nimi, et kontrollida, kas see nimi sisaldub laenuks võtva ettevõtte ressursiloendis.</span><span class="sxs-lookup"><span data-stu-id="80f72-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="80f72-135">Projekti ressursside taotlemine</span><span class="sxs-lookup"><span data-stu-id="80f72-135">Request project resources</span></span>
<span data-ttu-id="80f72-136">Projekti ressursi plaanimise funktsioon võimaldab ressursihalduritel ainult komplekteeritud ressursse tegevustele või projektidele jagada.</span><span class="sxs-lookup"><span data-stu-id="80f72-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="80f72-137">Selle funktsiooni lubamiseks tehke järgmised toimingud või veenduge, et need oleksid tehtud.</span><span class="sxs-lookup"><span data-stu-id="80f72-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="80f72-138">Häälestage numbriseeriad.</span><span class="sxs-lookup"><span data-stu-id="80f72-138">Set up number sequences.</span></span>
- <span data-ttu-id="80f72-139">Seadistage projektihalduse ja raamatupidamise töövood.</span><span class="sxs-lookup"><span data-stu-id="80f72-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="80f72-140">Luba ressursi taotluse töövood.</span><span class="sxs-lookup"><span data-stu-id="80f72-140">Enable resource request workflows.</span></span>

<span data-ttu-id="80f72-141">Pärast eelmiste toimingute tegemist võite teha vajaduse järgi järgmised toimingud.</span><span class="sxs-lookup"><span data-stu-id="80f72-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="80f72-142">Luua esialgselt reserveeritud komplekteeritud ressursist ressursitaotlust.</span><span class="sxs-lookup"><span data-stu-id="80f72-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="80f72-143">Jälgida ressursitaotlusi.</span><span class="sxs-lookup"><span data-stu-id="80f72-143">Monitor resource requests.</span></span>
- <span data-ttu-id="80f72-144">Täita ressursitaotlusi.</span><span class="sxs-lookup"><span data-stu-id="80f72-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="80f72-145">Taotleda WBS-ilt komplekteeritud ressurssi.</span><span class="sxs-lookup"><span data-stu-id="80f72-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="80f72-146">Reserveerida projektile ressursse ilma komplekteeritud ressursi taotluseta.</span><span class="sxs-lookup"><span data-stu-id="80f72-146">Book resources to a project without having a request for a staffed resource.</span></span>
