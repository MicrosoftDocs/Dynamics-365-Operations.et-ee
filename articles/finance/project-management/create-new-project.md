---
title: Loo uus projekt
description: See teema sisaldab teavet uue projekti loomise kohta.
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
ms.openlocfilehash: c8c52b8c1c86ea2f6e03cf439ba5930f1006ab4f
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760523"
---
# <a name="create-a-new-project"></a><span data-ttu-id="b6d49-103">Loo uus projekt</span><span class="sxs-lookup"><span data-stu-id="b6d49-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b6d49-104">Uue projekti loomiseks läbige järgmised etapid.</span><span class="sxs-lookup"><span data-stu-id="b6d49-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="b6d49-105">Tehke lehel **Projektihaldus** valik **Uus projekt** ja sisestage järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="b6d49-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="b6d49-106">**Projekti tüüp:** aeg ja materjal</span><span class="sxs-lookup"><span data-stu-id="b6d49-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="b6d49-107">**Projekti nimi:** XYZ täiendusfaas 2</span><span class="sxs-lookup"><span data-stu-id="b6d49-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="b6d49-108">**Projektigrupp:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="b6d49-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="b6d49-109">**Projektilepingu ID:** 00000002</span><span class="sxs-lookup"><span data-stu-id="b6d49-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="b6d49-110">Valige **Loo projekt**.</span><span class="sxs-lookup"><span data-stu-id="b6d49-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="b6d49-111">Ressursi määramine projektile</span><span class="sxs-lookup"><span data-stu-id="b6d49-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="b6d49-112">Valige lehel **Töötajad** loendist **Töötajad** selle töötaja kirje, kelle jaoks eelnevalt kompetentsid seadistasite, ja avage töötaja kirje.</span><span class="sxs-lookup"><span data-stu-id="b6d49-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="b6d49-113">Tehke tegumiriba vahekaardil **Projekt** grupis **Seadistus** valik **Projektide määramine**.</span><span class="sxs-lookup"><span data-stu-id="b6d49-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="b6d49-114">Filtreerige lehe **Ressursi kinnitamise projekti määrangud** vahekaardi **Projektid** väljal **Lisa projekt valitud projektidele** projekti **XYZ täiendusfaas 2**.</span><span class="sxs-lookup"><span data-stu-id="b6d49-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="b6d49-115">Valige paanilt **Järelejäänud projektid** projekt ja valige siis noolenupp selle lisamiseks paanile **Valitud projektid**.</span><span class="sxs-lookup"><span data-stu-id="b6d49-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="b6d49-116">Vajaduse korral saate ka ressursile kategooriaid määrata.</span><span class="sxs-lookup"><span data-stu-id="b6d49-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="b6d49-117">Kategooria tüüp on **Kulu** või **Tulu**.</span><span class="sxs-lookup"><span data-stu-id="b6d49-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="b6d49-118">Kategooria tüübi määrab teie organisatsioon.</span><span class="sxs-lookup"><span data-stu-id="b6d49-118">The category type is determined by your organization.</span></span> <span data-ttu-id="b6d49-119">Kui ressursile pole määratud ühtegi kategooriat, otsib Finance üles kulu ja tulu tunnihindade vaikekategooria.</span><span class="sxs-lookup"><span data-stu-id="b6d49-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="b6d49-120">Projekti ressursi ja rolli omaduste seadistamine</span><span class="sxs-lookup"><span data-stu-id="b6d49-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="b6d49-121">Projektijuht saab kasutada projekti ressursieralduse funktsiooni projekti jaoks vajalike rollide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="b6d49-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="b6d49-122">Rolle saab kasutada juhul, kui kinnitatud ressursid on ressursside reserveerimise ajal veel teadmata.</span><span class="sxs-lookup"><span data-stu-id="b6d49-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="b6d49-123">Rolle saab reserveerida ajutiselt plaanitud ressurssidena, et saaksite projekti plaanimise etappe jätkata.</span><span class="sxs-lookup"><span data-stu-id="b6d49-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="b6d49-124">[![Rolli näide](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="b6d49-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="b6d49-125">**Stsenaarium:** Contoso palgati täitma aja ja materjali projekti, millel on kinnitatud projekti põhikiri.</span><span class="sxs-lookup"><span data-stu-id="b6d49-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="b6d49-126">Noorem-projektijuht täidab veel projekti ulatust.</span><span class="sxs-lookup"><span data-stu-id="b6d49-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="b6d49-127">Ressursihaldur tuvastab praegu konkreetseid ressursse, mis uue projektiga töötamiseks reserveeritakse.</span><span class="sxs-lookup"><span data-stu-id="b6d49-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="b6d49-128">Projekti kriitilise iseloomu tõttu soovis projekti sponsor ühena rollidest vanem-projektijuhti.</span><span class="sxs-lookup"><span data-stu-id="b6d49-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="b6d49-129">Ressursihaldur peab uue ressursi hankima ja määratlema rolli süsteemis, juhul kui noorem-projektijuht vajab projekti plaanimise käigus teavet ressursi kohta.</span><span class="sxs-lookup"><span data-stu-id="b6d49-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="b6d49-130">Järgmised juhised näitavad, kuidas ressursihaldur saab vanem-projektijuhi rolli seadistada ja seostada sellega ressursi omadused.</span><span class="sxs-lookup"><span data-stu-id="b6d49-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="b6d49-131">Hiljem saab rolli kasutada vajalikele ressursi kompetentsidele vastavate olemasolevate ressursside otsimiseks.</span><span class="sxs-lookup"><span data-stu-id="b6d49-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="b6d49-132">Tehke lehel **Rollide seadistus** valik **Uus** ja sisestage järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="b6d49-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="b6d49-133">**Rolli ID:** vanem-projektijuht</span><span class="sxs-lookup"><span data-stu-id="b6d49-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="b6d49-134">**Kirjeldus:** vanem-projektijuht</span><span class="sxs-lookup"><span data-stu-id="b6d49-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="b6d49-135">Valige **Loo**.</span><span class="sxs-lookup"><span data-stu-id="b6d49-135">Select **Create**.</span></span>
3. <span data-ttu-id="b6d49-136">Valige roll **Vanem-projektijuht** ja siis valige **Omaduste konfigureerimine**.</span><span class="sxs-lookup"><span data-stu-id="b6d49-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="b6d49-137">Valige väljalt **Omaduse tüüp** väärtus **Oskus**.</span><span class="sxs-lookup"><span data-stu-id="b6d49-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="b6d49-138">Sisestage väljale **Olemasolev omadus** oskus, mida otsida.</span><span class="sxs-lookup"><span data-stu-id="b6d49-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="b6d49-139">Valige väljalt **Omaduse tüüp** väärtus **Tunnistus**.</span><span class="sxs-lookup"><span data-stu-id="b6d49-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="b6d49-140">Sisestage väljale **Olemasolev omadus** tunnistuse tüüp, mida otsida.</span><span class="sxs-lookup"><span data-stu-id="b6d49-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="b6d49-141">Projekti ressursi määramine projektile</span><span class="sxs-lookup"><span data-stu-id="b6d49-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="b6d49-142">Valige lehelt **Kõik projektid** projekt **XYZ täiendusfaas 2**.</span><span class="sxs-lookup"><span data-stu-id="b6d49-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="b6d49-143">Tehke vahekaardil **Projektimeeskond ja plaanimine** valik **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="b6d49-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="b6d49-144">Valige väljalt **Roll** väärtus **Meeskonnaliige**.</span><span class="sxs-lookup"><span data-stu-id="b6d49-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="b6d49-145">Valige **Kalendrist reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="b6d49-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="b6d49-146">Tehke lehel **Ressursi saadavus** valik **Kuva sätted**.</span><span class="sxs-lookup"><span data-stu-id="b6d49-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="b6d49-147">Sisestage lehele **Kuvasätete kohandamine** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="b6d49-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="b6d49-148">**Kuupäevavahemiku kuva jaoks vormindamine:** päev</span><span class="sxs-lookup"><span data-stu-id="b6d49-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="b6d49-149">**Kuva saadavuse kirjeldused:** jah</span><span class="sxs-lookup"><span data-stu-id="b6d49-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="b6d49-150">**Kuva järelejääv võimsus:** jah</span><span class="sxs-lookup"><span data-stu-id="b6d49-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="b6d49-151">Valige ressursiloendist ressurss.</span><span class="sxs-lookup"><span data-stu-id="b6d49-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="b6d49-152">Valige **Fikseeritud reserveerimine** ja **Kogujõudlus**.</span><span class="sxs-lookup"><span data-stu-id="b6d49-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="b6d49-153">Vaikerollile ressursi määramine</span><span class="sxs-lookup"><span data-stu-id="b6d49-153">Assign a resource to a default role</span></span>

<span data-ttu-id="b6d49-154">Projekti- või ressursihaldurite abistamiseks võite minna veel rohkem süvitsi ressurssides, mida projektile reserveerida saab.</span><span class="sxs-lookup"><span data-stu-id="b6d49-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="b6d49-155">Saate seostada vaikerolli olemasoleva ressursiga või äsja omandatud ressursiga.</span><span class="sxs-lookup"><span data-stu-id="b6d49-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="b6d49-156">Näiteks kui Daniel palgati, olid tal kogemuse ja oskused ärianalüütiku rolli täitmiseks.</span><span class="sxs-lookup"><span data-stu-id="b6d49-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="b6d49-157">Ressursihaldur määras selle rolli Danieli vaikerolliks.</span><span class="sxs-lookup"><span data-stu-id="b6d49-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="b6d49-158">Seetõttu lisas ressursihaldur Danieli projektidega töötavate analüütikute kausta.</span><span class="sxs-lookup"><span data-stu-id="b6d49-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="b6d49-159">Ressursi reserveerimise ajal saavad projektijuhid filtreerida rolli ressursse, mis on projektidega töötamiseks saadaval.</span><span class="sxs-lookup"><span data-stu-id="b6d49-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="b6d49-160">Nad saavad kasutada neid andmeid ühe kriteeriumina, kui nad teevad ressursside täitmisel mitmel kriteeriumil põhinevaid analüüse.</span><span class="sxs-lookup"><span data-stu-id="b6d49-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="b6d49-161">Samuti saavad nad lisada filtrile muid ressursiomadusi, et otsida antud projekti jaoks konkreetsete oskuste, hariduse ja kogemustega ressursse.</span><span class="sxs-lookup"><span data-stu-id="b6d49-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="b6d49-162">**Stsenaarium:** kinnitatud projekt on alanud ja vanem-projektijuhi roll reserveeriti plaanitud ressursina projekti plaanimisetapi käigus.</span><span class="sxs-lookup"><span data-stu-id="b6d49-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="b6d49-163">Ressursihaldur on nüüd hankinud ressursi vanem-projektijuhi rolli täitmiseks.</span><span class="sxs-lookup"><span data-stu-id="b6d49-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="b6d49-164">Valige lehelt **Ressursside loend** väärtus **Daniel Goldschmidt**.</span><span class="sxs-lookup"><span data-stu-id="b6d49-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="b6d49-165">Tehke lehel **Ressursi roll** valik **Uus** ja sisestage järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="b6d49-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="b6d49-166">**Jõustub:** sisestage jooksev kuupäev.</span><span class="sxs-lookup"><span data-stu-id="b6d49-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="b6d49-167">**Aegumine:** sisestage **Mitte kunagi**.</span><span class="sxs-lookup"><span data-stu-id="b6d49-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="b6d49-168">**Roll:** sisestage **Vanem-projektijuht**.</span><span class="sxs-lookup"><span data-stu-id="b6d49-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="b6d49-169">Valige **Salvesta** ja sulgege seejärel leht.</span><span class="sxs-lookup"><span data-stu-id="b6d49-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="b6d49-170">Lisage vahekaardile **Kompetentsid** oskus **ProjectMgmt** ja tunnistus **PMP**.</span><span class="sxs-lookup"><span data-stu-id="b6d49-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>
