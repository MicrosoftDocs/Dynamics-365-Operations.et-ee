---
title: "Töövoogude kasutamine töötajateabe haldamiseks"
description: "See teema selgitab, kuidas saate töötaja teabe haldamiseks kasutada inimressursside töövoo võimalust. Näiteks saate seostada töövoo positsiooniga ja konfigureerida kinnitamise töövoo, mis käivitatakse, kui töötajad muudavad oma kirjet."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 269074
ms.assetid: 426c6127-42ee-4163-8dd0-b2867f95581d
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: abc52192848649672cbcb8c770d74ba2aef139be
ms.openlocfilehash: cf2200057053f5a6d4754d37111ebe34849bb99d
ms.contentlocale: et-ee
ms.lasthandoff: 02/14/2018

---

# <a name="use-workflows-to-manage-employee-information"></a><span data-ttu-id="43930-104">Töövoogude kasutamine töötajateabe haldamiseks</span><span class="sxs-lookup"><span data-stu-id="43930-104">Use workflows to manage employee information</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="43930-105">See teema selgitab, kuidas saate töötaja teabe haldamiseks kasutada inimressursside töövoo võimalust.</span><span class="sxs-lookup"><span data-stu-id="43930-105">This topic explains how you can use the workflow capability for Human resources to manage employee information.</span></span> <span data-ttu-id="43930-106">Näiteks saate seostada töövoo positsiooniga ja konfigureerida kinnitamise töövoo, mis käivitatakse, kui töötajad muudavad oma kirjet.</span><span class="sxs-lookup"><span data-stu-id="43930-106">For example, you can associate a workflow with a position and configure an approval workflow that is started when employees change their record.</span></span>

<span data-ttu-id="43930-107">Inimressursside töövoo võimalus annab hulgaliselt töövoogusid inimressursside tegevuste haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="43930-107">The workflow capability for Human resources provides numerous workflows for managing human resources activities.</span></span> <span data-ttu-id="43930-108">Lisaks on saadaval mitmed valikud, et saaksite muuta spetsiifilisi töövoogusid ja seostada neid aruandlushierarhiaga.</span><span class="sxs-lookup"><span data-stu-id="43930-108">Additionally, numerous options are available so that you can modify specific workflows and associate them with a reporting hierarchy.</span></span> <span data-ttu-id="43930-109">Töövood on saadaval, et hallata muudatusi mitmele töötajateabe standardsele tüübile.</span><span class="sxs-lookup"><span data-stu-id="43930-109">Workflows are available to help manage changes to several standard types of employee information.</span></span> <span data-ttu-id="43930-110">Saate seostada töövoo positsiooniga.</span><span class="sxs-lookup"><span data-stu-id="43930-110">You can associate a workflow with a position.</span></span> <span data-ttu-id="43930-111">Kui töötajad muudavad seejärel oma töötaja kirjet, käivitatakse töövoog, mis nõuab enne uue teabe salvestamist kinnitust.</span><span class="sxs-lookup"><span data-stu-id="43930-111">Then, if employees change their employee record, a workflow is started that requires approval before the new information is saved.</span></span> <span data-ttu-id="43930-112">Töövood määratletakse eelnevalt järgmiste teabetüüpide puhul, et aidata teil tõhusalt muudatusi hallata ja töötajate andmete täpsust säilitada.</span><span class="sxs-lookup"><span data-stu-id="43930-112">Workflows are predefined for the following types of information to help you efficiently manage changes and keep your employees’ data accurate:</span></span>

-   <span data-ttu-id="43930-113">ID-numbrid</span><span class="sxs-lookup"><span data-stu-id="43930-113">Identification numbers</span></span>
-   <span data-ttu-id="43930-114">Kursused</span><span class="sxs-lookup"><span data-stu-id="43930-114">Courses</span></span>
-   <span data-ttu-id="43930-115">Haridus</span><span class="sxs-lookup"><span data-stu-id="43930-115">Education</span></span>
-   <span data-ttu-id="43930-116">Pilt</span><span class="sxs-lookup"><span data-stu-id="43930-116">Image</span></span>
-   <span data-ttu-id="43930-117">Laenatud üksused</span><span class="sxs-lookup"><span data-stu-id="43930-117">Loaned items</span></span>
-   <span data-ttu-id="43930-118">Töökogemus</span><span class="sxs-lookup"><span data-stu-id="43930-118">Professional experience</span></span>
-   <span data-ttu-id="43930-119">Projektikogemus</span><span class="sxs-lookup"><span data-stu-id="43930-119">Project experience</span></span>
-   <span data-ttu-id="43930-120">Oskused</span><span class="sxs-lookup"><span data-stu-id="43930-120">Skills</span></span>
-   <span data-ttu-id="43930-121">Vastutavad positsioonid</span><span class="sxs-lookup"><span data-stu-id="43930-121">Positions of trust</span></span>
-   <span data-ttu-id="43930-122">Inimressursside tegevused</span><span class="sxs-lookup"><span data-stu-id="43930-122">Human resources actions</span></span>
-   <span data-ttu-id="43930-123">Kursusele registreerimine</span><span class="sxs-lookup"><span data-stu-id="43930-123">Course registration</span></span>

<span data-ttu-id="43930-124">Töötajate palkamisel, üleviimisel või nendega töösuhte lõpetamisel võib töövoog hõlmata ülevaatamise protsessi.</span><span class="sxs-lookup"><span data-stu-id="43930-124">When employees are hired, transferred, or terminated, the workflow can include a review process.</span></span> <span data-ttu-id="43930-125">Sellisel viisil saab dokumenti parandada või tegevuse tingimusi määratleda osana töövoost.</span><span class="sxs-lookup"><span data-stu-id="43930-125">In this way, a document can be revised or the terms of an action can be defined as part of the workflow.</span></span> <span data-ttu-id="43930-126">Ülevaatamisprotsessi lõpuleviimisel viiakse dokument või tegevus lõpule ja töövoog liigub lõplikku kinnitamisetappi.</span><span class="sxs-lookup"><span data-stu-id="43930-126">When the review process is completed, the document or action is completed, and the workflow moves to a final approval step.</span></span>

## <a name="associate-a-workflow-with-a-position-hierarchy"></a><span data-ttu-id="43930-127">Töövoo seostamine positsioonihierarhiaga</span><span class="sxs-lookup"><span data-stu-id="43930-127">Associate a workflow with a position hierarchy</span></span>
<span data-ttu-id="43930-128">Saate seostada töövoo mis tahes konfigureeritava hierarhiaga.</span><span class="sxs-lookup"><span data-stu-id="43930-128">You can associate a workflow with any hierarchy that you configure.</span></span> <span data-ttu-id="43930-129">Näiteks kui positsioon on seotud maatriksi aruandluse hierarhiaga, võite konfigureerida töövoo, mis suunab spetsiifilise projekti kulud selle positsiooniga seotud töötaja juhataja asemel projekti müügivihjele.</span><span class="sxs-lookup"><span data-stu-id="43930-129">For example, if a position is associated with a matrix reporting hierarchy, you might configure a workflow that routes expenses for a specific project to the project lead instead of the manager of the employee who is associated with that position.</span></span> <span data-ttu-id="43930-130">Uue töövoo loomiseks või olemasoleva töövoo muutmiseks klõpsake lehel **Inimressursside töövood** nuppu **Uus**.</span><span class="sxs-lookup"><span data-stu-id="43930-130">To create a new workflow or modify an existing workflow, on the **Human resources workflow** page, click **New**.</span></span> <span data-ttu-id="43930-131">Töövoo kujundaja käivitamiseks valige loendis töövoog.</span><span class="sxs-lookup"><span data-stu-id="43930-131">Select a workflow in the list to start the Workflow designer.</span></span> <span data-ttu-id="43930-132">Saate kasutada kujundajat uue töövoo loomiseks või etappide muutmiseks olemasolevas töövoos.</span><span class="sxs-lookup"><span data-stu-id="43930-132">You can use the designer to create a new workflow or change the steps in an existing workflow.</span></span> <span data-ttu-id="43930-133">Olemasoleva töövoo muutmisel salvestatakse teie muudatused uude versiooni.</span><span class="sxs-lookup"><span data-stu-id="43930-133">When you change an existing workflow, your changes are saved as a new version.</span></span> <span data-ttu-id="43930-134">Lisaks saate vajaduse korral minna tagasi eelmisesse versiooni.</span><span class="sxs-lookup"><span data-stu-id="43930-134">Therefore, you can always go back to a previous version if you have to.</span></span>

## <a name="configure-a-human-resources-workflow"></a><span data-ttu-id="43930-135">Inimressursside töövoo konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="43930-135">Configure a Human resources workflow</span></span>
<span data-ttu-id="43930-136">Konfigureerimaks põhitöövoogu, mis käivitatakse siis, kui töötajad nõuavad nende isikukoodi muutmist, järgige neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="43930-136">To configure a basic workflow that is started when employees request changes to their personal identification, follow these steps.</span></span>

1.  <span data-ttu-id="43930-137">Lehel **Inimressursside töövood** klõpsake nuppu **Uus**.</span><span class="sxs-lookup"><span data-stu-id="43930-137">On the **Human resources workflows** page, click **New**.</span></span>
2.  <span data-ttu-id="43930-138">Saadaolevate töövoogude loendis valige **ID-koodid**.</span><span class="sxs-lookup"><span data-stu-id="43930-138">In the list of available workflows, select **Identification numbers**.</span></span>
3.  <span data-ttu-id="43930-139">Klõpsake nuppu **Käivita**, et käivitada töövoo kujundaja ja sisestada seejärel vastava viiba kuvamisel oma kasutajanime ja parooli.</span><span class="sxs-lookup"><span data-stu-id="43930-139">Click **Run** to start the Workflow designer, and then enter your user name and password when you're prompted.</span></span>
4.  <span data-ttu-id="43930-140">Lohistage element **Kinnituse ID-number** töövoo elementide loendist kujundaja lõuendile.</span><span class="sxs-lookup"><span data-stu-id="43930-140">Drag the **Approve identification number** element from the list of workflow elements to the designer canvas.</span></span>
5.  <span data-ttu-id="43930-141">Ühendage kinnituse element valikuga **Algus** ja **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="43930-141">Connect the approval element to **Start** and **Finish**.</span></span>
6.  <span data-ttu-id="43930-142">Topeltklõpsake nuppu **Kinnita element** ning seejärel paremklõpsake ja valige suvand **Atribuudid**.</span><span class="sxs-lookup"><span data-stu-id="43930-142">Double-click **Approve element**, and then right-click, and select **Properties**.</span></span>
7.  <span data-ttu-id="43930-143">Järgige tööüksuse juhiste lisamiseks neid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="43930-143">Follow these steps to add work item instructions:</span></span>
    1.  <span data-ttu-id="43930-144">Valige **Määramine** ja seejärel valige määramistüübi valikus **Hierarhia**.</span><span class="sxs-lookup"><span data-stu-id="43930-144">Select **Assignment**, and then select **Hierarchy** under the assignment type.</span></span>
    2.  <span data-ttu-id="43930-145">Valikus **Hierarhia** valige **Konfigureeritav hierarhia**.</span><span class="sxs-lookup"><span data-stu-id="43930-145">Under the **Hierarchy** selection, select **Configurable hierarchy**.</span></span>
    3.  <span data-ttu-id="43930-146">Lisage peatamistingimus ja sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="43930-146">Add a stop condition, and close the page.</span></span>

8.  <span data-ttu-id="43930-147">Täitke mis tahes täiendavad juhised (täiendavaid hoiatusi ei tohiks olla).</span><span class="sxs-lookup"><span data-stu-id="43930-147">Complete any additional instructions (no additional warnings should exist).</span></span>
9.  <span data-ttu-id="43930-148">Klõpsake käsku **Salvesta ja sule**.</span><span class="sxs-lookup"><span data-stu-id="43930-148">Click **Save and close**.</span></span> <span data-ttu-id="43930-149">Aktiveerige uus töövoog, kui dialoogiboks avaneb, ja valige **Muuda aktiivseks**.</span><span class="sxs-lookup"><span data-stu-id="43930-149">Activate the new workflow when the dialog box opens, and select **Make active**.</span></span>
10. <span data-ttu-id="43930-150">Valige **Inimressurssid** &gt; **Ametikohad** &gt; **Positsiooni hierarhiatüübid**.</span><span class="sxs-lookup"><span data-stu-id="43930-150">Go to **Human Resources** &gt; **Positions** &gt; **Position hierarchy types**.</span></span>
11. <span data-ttu-id="43930-151">Valige suvand **Maatriks**.</span><span class="sxs-lookup"><span data-stu-id="43930-151">Select **Matrix**.</span></span>
12. <span data-ttu-id="43930-152">Lisage loendisse töövoog **Töötaja ID-kood**.</span><span class="sxs-lookup"><span data-stu-id="43930-152">Add the **Worker identification number** workflow to the list.</span></span>





