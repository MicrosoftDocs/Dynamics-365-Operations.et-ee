---
title: Eelarve plaanimise põhjendusdokumendid
description: Põhjendusdokumendid pakuvad eelarvetaotlejatele teatud eelarve vajalikkust põhjendavaid selgitusi.
author: ryansandness
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanJustificationTemplate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 259594
ms.assetid: 52576fad-32b9-48f2-8197-c11ec313fc29
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 5c7db2c10572ad7b5fd18381d139259c08182586
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834315"
---
# <a name="budget-planning-justification-documents"></a><span data-ttu-id="f4c9b-103">Eelarve plaanimise põhjendusdokumendid</span><span class="sxs-lookup"><span data-stu-id="f4c9b-103">Budget planning justification documents</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f4c9b-104">Põhjendusdokumendid pakuvad eelarvetaotlejatele teatud eelarve vajalikkust põhjendavaid selgitusi.</span><span class="sxs-lookup"><span data-stu-id="f4c9b-104">Justification documents provide a narrative for those requesting a budget to explain why a specific budget is necessary.</span></span> 

<span data-ttu-id="f4c9b-105">Eelarvehaldur loob Microsoft Wordis eelarveplaani malli ja määrab selle praegusse eelarve plaanimise protsessi.</span><span class="sxs-lookup"><span data-stu-id="f4c9b-105">A budget plan template is created by the budget manager in Microsoft Word and assigned to the current budget planning process.</span></span> <span data-ttu-id="f4c9b-106">Seejärel saavad eelarve omanikud malli avada ja andmed Wordis automaatselt sisestada oma eelarvetaotluse põhjal.</span><span class="sxs-lookup"><span data-stu-id="f4c9b-106">Budget owners can then open the template and have data automatically populated in Word based on their budget request.</span></span> <span data-ttu-id="f4c9b-107">Pärast seda on võimalik lisada täiendavat teksti või andmeid ning seejärel isikupärastatud põhjendusdokument salvestada ja manustada eelarveplaanile.</span><span class="sxs-lookup"><span data-stu-id="f4c9b-107">They can then add additional text or data prior to saving and attaching their personalized justification document to their budget plan.</span></span>

##### <a name="set-up-microsoft-dynamics-office-add-in-for-microsoft-word"></a><span data-ttu-id="f4c9b-108">Microsoft Dynamics Office’i lisandmooduli seadistamine Microsoft Wordi jaoks</span><span class="sxs-lookup"><span data-stu-id="f4c9b-108">Set up Microsoft Dynamics Office Add-in for Microsoft Word</span></span>

1.  <span data-ttu-id="f4c9b-109">Avage uus Microsoft Wordi dokument.</span><span class="sxs-lookup"><span data-stu-id="f4c9b-109">Open a new Microsoft Word document.</span></span>
2.  <span data-ttu-id="f4c9b-110">Klõpsake lindil valikut **Sisesta** ja siis valikut **Pood**.</span><span class="sxs-lookup"><span data-stu-id="f4c9b-110">Click **Insert** on the ribbon, and click **Store**.</span></span>
3.  <span data-ttu-id="f4c9b-111">Otsige Microsoft Dynamics Office’i lisandmoodulit ja klõpsake nuppu **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="f4c9b-111">Search for Microsoft Dynamics Office Add-in and click **Add**.</span></span>
4.  <span data-ttu-id="f4c9b-112">Klõpsake Wordi paremal paanil valikut **Lisa serveriteave**.</span><span class="sxs-lookup"><span data-stu-id="f4c9b-112">In Word, in the right pane, click **Add server information**.</span></span>
5.  <span data-ttu-id="f4c9b-113">Tippige või kleepige serveri URL ja klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="f4c9b-113">Type or paste the server URL and click **OK**.</span></span>

##### <a name="define-the-justification-template-in-microsoft-word"></a><span data-ttu-id="f4c9b-114">Põhjenduse malli määratlemine Microsoft Wordis</span><span class="sxs-lookup"><span data-stu-id="f4c9b-114">Define the Justification template in Microsoft Word</span></span>

1.  <span data-ttu-id="f4c9b-115">Klõpsake Microsoft Dynamics Office’i lisandmoodulis pärast sisselogimist nuppu **Kujundus**.</span><span class="sxs-lookup"><span data-stu-id="f4c9b-115">Click **Design** in the Microsoft Dynamics Office Add-in after you’ve logged in.</span></span>
2.  <span data-ttu-id="f4c9b-116">Päiseteabe jaoks kasutage nuppu **Lisa välju**.</span><span class="sxs-lookup"><span data-stu-id="f4c9b-116">For header information, use the **Add fields** button.</span></span>
3.  <span data-ttu-id="f4c9b-117">Valige atribuudi BudgetPlanJustification üksuse andmeallikas ja klõpsake nuppu **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="f4c9b-117">Select the entity data source of BudgetPlanJustification, and click **Next**.</span></span> <span data-ttu-id="f4c9b-118">**Märkus.** See üksus on nõutav kõigi põhjendusdokumentide puhul.</span><span class="sxs-lookup"><span data-stu-id="f4c9b-118">**Note:** This entity is required for any justification document.</span></span> <span data-ttu-id="f4c9b-119">Muid üksusi võib kasutada, kuid uuesti üleslaadimine rakendusse Microsoft Dynamics 365 for Finance and Operations nurjub, kui see üksus pole kaasatud.</span><span class="sxs-lookup"><span data-stu-id="f4c9b-119">Other entities can be used but the upload back to Microsoft Dynamics 365 for Finance and Operations will fail if this entity isn’t included.</span></span>
4.  <span data-ttu-id="f4c9b-120">Lisage Wordi dokumenti atribuutide BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter ja DocumentNumber sildid ning väärtused.</span><span class="sxs-lookup"><span data-stu-id="f4c9b-120">Add the BudgetPlanName, BudgetPlanPreparer, ResponsibilityCenter, and DocumentNumber labels and values in the Word document.</span></span> <span data-ttu-id="f4c9b-121">**Märkus.** Vajaduse korral saate standardsiltide asemel kasutada oma kohandatud silte.</span><span class="sxs-lookup"><span data-stu-id="f4c9b-121">**Note:** You can use your own custom labels, rather than the standard labels, if needed.</span></span>
5.  <span data-ttu-id="f4c9b-122">Päisejaotisega lõpetamiseks klõpsake nuppu **Valmis**.</span><span class="sxs-lookup"><span data-stu-id="f4c9b-122">Click **Done** to complete the header section.</span></span>
6.  <span data-ttu-id="f4c9b-123">Eelarveplaani summade reatasemel üksikasjade saamiseks klõpsake valikut **Lisa tabel**.</span><span class="sxs-lookup"><span data-stu-id="f4c9b-123">For line level detail of budget plan amounts, click **Add table**.</span></span>
7.  <span data-ttu-id="f4c9b-124">Valige jälle atribuudi BudgetPlanJustification üksuse andmeallikas ja klõpsake nuppu **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="f4c9b-124">Again, select the entity data source of BudgetPlanJustification, and click **Next**.</span></span>
8.  <span data-ttu-id="f4c9b-125">Lisage väljad atribuutide EffectiveDate, ScenarioName, AccountDisplayValue ja AccountingCurrencyExpenseAmount jaoks.</span><span class="sxs-lookup"><span data-stu-id="f4c9b-125">Add fields for EffectiveDate, ScenarioName, AccountDisplayValue, and AccountingCurrencyExpenseAmount.</span></span> <span data-ttu-id="f4c9b-126">**Märkus.** Kui üksikutele eelarveplaani ridadele lisamiseks on kommentaarid saadaval, saab need siin tabelisse lisada.</span><span class="sxs-lookup"><span data-stu-id="f4c9b-126">**Note:** If comments are available to add within individual budget plan lines, those can be added to the table here.</span></span>
9.  <span data-ttu-id="f4c9b-127">Lisage muud lõppkasutajale pakutavad lisajuhised ning tehke dokumendile vajalikud vormindus- ja laadimuudatused.</span><span class="sxs-lookup"><span data-stu-id="f4c9b-127">Add any additional instructions to provide to the end user, and perform any necessary formatting or styling to the document.</span></span>
10. <span data-ttu-id="f4c9b-128">Enne jätkamist salvestage dokument kohalikku arvutisse ja sulgege fail.</span><span class="sxs-lookup"><span data-stu-id="f4c9b-128">Save the document to your local computer and close the file before continuing.</span></span>

##### <a name="set-up-the-budget-planning-process-to-use-the-justification-template"></a><span data-ttu-id="f4c9b-129">Eelarve plaanimise protsessi seadistamine põhjendusmalli kasutamiseks</span><span class="sxs-lookup"><span data-stu-id="f4c9b-129">Set up the Budget planning process to use the Justification template</span></span>

1.  <span data-ttu-id="f4c9b-130">Minge Finance and Operationsis jaotisse **Eelarvestus** &gt; **Seadistus** &gt; **Eelarve plaanimine** &gt; **Põhjendusdokumendi mallid**.</span><span class="sxs-lookup"><span data-stu-id="f4c9b-130">In Finance and Operations, go to **Budgeting** &gt; **Setup** &gt; **Budget planning** &gt; **Justification document templates**.</span></span>
2.  <span data-ttu-id="f4c9b-131">Klõpsake nuppu **Uus** ja sirvige vastloodud Microsoft Wordi dokumendini.</span><span class="sxs-lookup"><span data-stu-id="f4c9b-131">Click **New** and browse to your newly created Microsoft Word document.</span></span>
3.  <span data-ttu-id="f4c9b-132">Sisestage malli kuvatav nimi ja kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="f4c9b-132">Enter a template display name and description.</span></span> <span data-ttu-id="f4c9b-133">Klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="f4c9b-133">Click **OK**.</span></span>
4.  <span data-ttu-id="f4c9b-134">Minge jaotisse **Eelarvestus** &gt; **Seadistus** &gt; **Eelarve** **plaanimine** &gt; **Eelarve plaanimise protsess**.</span><span class="sxs-lookup"><span data-stu-id="f4c9b-134">Go to **Budgeting** &gt; **Setup** &gt; **Budget** **planning** &gt; **Budget planning process**.</span></span>
5.  <span data-ttu-id="f4c9b-135">Valige protsess, kus malli tuleb kasutada, ja klõpsake nuppu **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="f4c9b-135">Select the process where the justification template should be used, and click **Edit**.</span></span>
6.  <span data-ttu-id="f4c9b-136">Valige väljal **Põhjendusdokumendi mall** sobiv mall ja salvestage.</span><span class="sxs-lookup"><span data-stu-id="f4c9b-136">In the **Justification document template** field, select the appropriate template and save.</span></span>

##### <a name="edit-and-save-personalized-justification-documents"></a><span data-ttu-id="f4c9b-137">Isikupärastatud põhjendusdokumentide redigeerimine ja salvestamine</span><span class="sxs-lookup"><span data-stu-id="f4c9b-137">Edit and save personalized justification documents</span></span>

1.  <span data-ttu-id="f4c9b-138">Looge Finance and Operationsis uus eelarveplaan või avage olemasolev.</span><span class="sxs-lookup"><span data-stu-id="f4c9b-138">In Finance and Operations, create a new budget plan or open an existing budget plan.</span></span>
2.  <span data-ttu-id="f4c9b-139">Valige ripploendist **Põhjendus** suvand **Uue põhjenduse loomine**.</span><span class="sxs-lookup"><span data-stu-id="f4c9b-139">In the **Justification** drop-down menu, select **Create new justification**.</span></span>
3.  <span data-ttu-id="f4c9b-140">Pärast üksikasjade sisestamist valige rippmenüüst **Põhjendus** isikupärastatud dokumendi üleslaadimine.</span><span class="sxs-lookup"><span data-stu-id="f4c9b-140">After filling in the details, select to upload the personalized document from the **Justification** drop-down menu.</span></span>




