---
title: Projektimeeskonna koostamine
description: See teema sisaldab teavet projektimeeskondade loomise ja haldamise kohta.
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
ms.openlocfilehash: 834a6c0a4fcc32a955c1feddf0a6cbbb1f16b869
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760524"
---
# <a name="create-a-project-team"></a><span data-ttu-id="d2bfb-103">Projektimeeskonna koostamine</span><span class="sxs-lookup"><span data-stu-id="d2bfb-103">Create a project team</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d2bfb-104">Projektis eelnevalt seadistatud rollide kasutamiseks peab projektijuht need rollid projektiga seostama.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-104">To use the roles that were previously set up in a project, a project manager must associate the roles with the project.</span></span> <span data-ttu-id="d2bfb-105">Projektile saab määrata mitu rolli.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-105">Multiple roles can be assigned for a project.</span></span> <span data-ttu-id="d2bfb-106">Segaduse vältimiseks märgistatakse need rollid reserveerimise käigus automaatselt.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-106">To prevent confusion, these roles are automatically labeled during reservation.</span></span> <span data-ttu-id="d2bfb-107">Näiteks kui projektijuht vajab kolme tarkvarainseneri, luuakse automaatselt kolm tarkvarainseneri rolli, mille sildid on **tarkvarainsener 1**, **tarkvarainsener 2** ja **tarkvarainsener 3**.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-107">For example, if the project manager requires three software engineers, three Software engineer roles that have **software engineer 1**, **software engineer 2**, and **software engineer 3** as their labels are automatically generated.</span></span> <span data-ttu-id="d2bfb-108">Kui rollile olid eelnevalt määratud rolli omadused, rakendatakse need ressursi otsingute käigus filtrina.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-108">If role characteristics were previously set for the role, they are applied as a filter during searches for a resource.</span></span> <span data-ttu-id="d2bfb-109">Otsingu täiendavaks täpsustamiseks saab omadusi lisada.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-109">Additional characteristics can be added as required to further refine the search.</span></span>

<span data-ttu-id="d2bfb-110">Kuvasätteid saab samuti kohandada, et anda parem vaade ressursi saadavuse kohta.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-110">View settings can also be customized to give a better view of resource availability.</span></span> <span data-ttu-id="d2bfb-111">On olemas valikud saadavuse kuvamiseks tunnis, päevas, nädalas, kuus, kvartalis ja aastas.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-111">There are options to show hourly, daily, weekly, monthly, quarterly, and annual availability.</span></span> <span data-ttu-id="d2bfb-112">On olemas ka valik näidata ressursside olemasolevat ja järelejäänud mahtu.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-112">There is also an option to show available and remaining capacity on resources.</span></span> <span data-ttu-id="d2bfb-113">Sellest valikust on kasu aja juhtimisel, kui hindate tegevuste jaoks saadaolevat aega või ressursi kättesaadavust.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-113">This option is useful for time management, when you're estimating available time for activities or resource availability.</span></span>

<span data-ttu-id="d2bfb-114">Projektijuht võib valida lehelt rolli ja siis, kui on olemas vajadusele vastav kättesaadav ressurss, valida ressursi reserveerimise rolli täitmiseks.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-114">The project manager can select a role on the page and then, if there is an available resource that fits the requirement, select to reserve a resource to fill the role.</span></span> <span data-ttu-id="d2bfb-115">Pange tähele, et ressursse pole plaanimise etapi selles osas vaja reserveerida.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-115">Note that the resources don't have to be reserved at this point in the planning stage.</span></span> <span data-ttu-id="d2bfb-116">WBS-i loomisel saate asendada rollid projekti komplekteeritud ressurssidega.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-116">When you create a WBS, you can replace roles with staffed resources for the project.</span></span> <span data-ttu-id="d2bfb-117">Kui rollid asendatakse WBS-is komplekteeritud ressurssidega, värskendab ressursi seadistus automaatselt projektimeeskonna loendit ja plaanimist.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-117">If roles are replaced with staffed resources in the WBS, the resource setup automatically updates the project team listing and scheduling.</span></span>

<span data-ttu-id="d2bfb-118">[![Projekti töörühma loend, mis sisaldab nii rolle kui ka tegelikke ressursse](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span><span class="sxs-lookup"><span data-stu-id="d2bfb-118">[![Project team listing that includes both roles and actual resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span></span> 

<span data-ttu-id="d2bfb-119">Projektijuhil on mitmesuguseid võimalusi projektile ressursi reserveerimiseks, nt **Järelejäänud võimsus**, **Täisvõimsus**, **Võimsuse protsent** ja **Tundide määramine**.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-119">The project manager has various options for booking a resource for a project, such as **Remaining capacity**, **Full capacity**, **Capacity percentage**, and **Specify hours**.</span></span> <span data-ttu-id="d2bfb-120">Neid reserveerimisvalikuid saab ressursi määrangute muutumisel igal ajal tühistada.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-120">These booking options can be canceled at any time if resource assignments change.</span></span> <span data-ttu-id="d2bfb-121">Toetatakse kahte reserveerimise tüüpi:</span><span class="sxs-lookup"><span data-stu-id="d2bfb-121">Two types of booking are supported:</span></span>

- <span data-ttu-id="d2bfb-122">**Fikseeritud reserveerimine** – ressursi reserveerimine kinnitati töötamiseks tegevusega määratud perioodil.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-122">**Hard Book** – The resource reservation was approved and confirmed to work on the engagement for the specified duration.</span></span>
- <span data-ttu-id="d2bfb-123">**Esialgne reserveerimine** – ressurss reserveeriti esialgselt töötamiseks tegevusega määratud perioodil.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-123">**Soft book** – The resource reservations was tentatively set to work on the engagement for the specified duration.</span></span>

<span data-ttu-id="d2bfb-124">Järgmine protseduur selgitab, kuidas projektimeeskonda koostada.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-124">The following procedure explains how to create a project team.</span></span>

## <a name="create-a-project-team"></a><span data-ttu-id="d2bfb-125">Projektimeeskonna koostamine</span><span class="sxs-lookup"><span data-stu-id="d2bfb-125">Create a project team</span></span>

1. <span data-ttu-id="d2bfb-126">Valige loendilehelt **Kõik projektid** projekt ja valige siis **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-126">On the **All projects** list page, select a project, and then select **Edit**.</span></span>
2. <span data-ttu-id="d2bfb-127">Sisestage vahekaardile **Projektimeeskond ja plaanimine** väljal **Graafiku lõppkuupäev** graafiku alguskuupäev pluss üks kuu.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-127">On the **Project team and scheduling** tab, in the **Schedule end date** field, enter the schedule start date plus one month.</span></span> <span data-ttu-id="d2bfb-128">Näiteks kui graafiku alguskuupäev on 24. juuni 2017 (24/06/2017), sisestage **24/07/2017**.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-128">For example, if the schedule start date is June 24, 2017 (24/06/2017), enter **24/07/2017**.</span></span>
3. <span data-ttu-id="d2bfb-129">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-129">Select **Add**.</span></span>
4. <span data-ttu-id="d2bfb-130">Valige paanilt **Projektile rollide lisamine** väljal **Roll** väärtus **Vanem-projektijuht**.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-130">In the **Add roles to the project** pane, in the **Role** field, select **Senior Project Manager**.</span></span>
5. <span data-ttu-id="d2bfb-131">Valige **Nõutud pädevused**.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-131">Select **Required competencies**.</span></span>
6. <span data-ttu-id="d2bfb-132">Lehel **Omaduste valimine** on vaikimisi valitud omadused, mille eelnevalt vanem-projektijuhi rollile määrasite.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-132">On the **Choose characteristics** page, the characteristics that you previously set for the Senior project manager role are selected by default.</span></span> <span data-ttu-id="d2bfb-133">Valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-133">Select **OK**.</span></span>
7. <span data-ttu-id="d2bfb-134">Sisestage lehe **Rollide lisamine projektidele** väljale **Ressursside arv** väärtus **1**.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-134">On the **Add roles to project** page, in the **Number of resources** field, enter **1**.</span></span>
8. <span data-ttu-id="d2bfb-135">Väljal **Ressurss** näitab otsing kõiki ressursse, millel on vajalikud kompetentsid.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-135">In the **Resource** field, the lookup shows all resources that have the required competencies.</span></span> <span data-ttu-id="d2bfb-136">Valige **Daniel Goldschmidt** ja seejärel **Loo**.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-136">Select **Daniel Goldschmidt**, and then select **Create**.</span></span>
9. <span data-ttu-id="d2bfb-137">Tehke lehel **Projekt** valik **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-137">On the **Project** page, select **Add**.</span></span>
10. <span data-ttu-id="d2bfb-138">Valige paanilt **Projektile rollide lisamine** väljal **Roll** väärtus **Meeskonnaliige**.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-138">In the **Add roles to the project** pane, in the **Role** field, select **Team member**.</span></span> <span data-ttu-id="d2bfb-139">Sisestage väljale **Ressursside arv** väärtus **5**.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-139">In the **Number of resources** field, enter **5**.</span></span>
11. <span data-ttu-id="d2bfb-140">Valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-140">Select **Create**.</span></span>
12. <span data-ttu-id="d2bfb-141">Tehke lehel **Projektid** valik **Täida ressurss**.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-141">On the **Projects** page, select **Fulfill resource**.</span></span>

## <a name="monitor-project-teams"></a><span data-ttu-id="d2bfb-142">Jälgida projektimeeskondi</span><span class="sxs-lookup"><span data-stu-id="d2bfb-142">Monitor project teams</span></span>
1. <span data-ttu-id="d2bfb-143">Valige lehelt **Kõik projektid** projekti **XYZ täiendusfaas 2** link **Projekti ID**.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-143">On the **All projects** page, select the **Project ID** link for the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="d2bfb-144">Veenduge, et kiirkaardil **Projektimeeskond ja plaanimine** loetletud projektiressursid on õiged.</span><span class="sxs-lookup"><span data-stu-id="d2bfb-144">On the **Project team and scheduling** FastTab, verify that the project resources that are listed are correct.</span></span>
