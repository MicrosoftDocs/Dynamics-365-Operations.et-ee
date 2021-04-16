---
title: Lähtedokumentide jaoks auditipoliitikate määratlemine
description: Selles teemas selgitatakse, kuidas seadistada ja käivitada auditipoliitika reegleid.
author: panolte
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 62ebe3d6ba1208bd5f9a2082969b1960c413c152
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5836957"
---
# <a name="define-audit-policies-for-source-documents"></a><span data-ttu-id="2c75e-103">Lähtedokumentide jaoks auditipoliitikate määratlemine</span><span class="sxs-lookup"><span data-stu-id="2c75e-103">Define audit policies for source documents</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2c75e-104">Selles teemas selgitatakse, kuidas seadistada ja käivitada auditipoliitika reegleid.</span><span class="sxs-lookup"><span data-stu-id="2c75e-104">This topic explains how to set up and run audit policy rules.</span></span> <span data-ttu-id="2c75e-105">Näites kasutatakse hotelli kulu tüübiga kuluaruandeid.</span><span class="sxs-lookup"><span data-stu-id="2c75e-105">The example uses expense reports with the hotel expense type.</span></span> <span data-ttu-id="2c75e-106">See protsess kasutab demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="2c75e-106">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="2c75e-107">Audiitori roll sisaldab nende ülesannete teostamiseks vajalikke õigusi.</span><span class="sxs-lookup"><span data-stu-id="2c75e-107">The auditor role contains the correct permissions in order to perform these tasks.</span></span>

1. <span data-ttu-id="2c75e-108">Navigeerimispaanil avage **Moodulid > Auditi töölaud > Seadistus > Poliitika reegli tüüp**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-108">In the navigation pane, go to **Modules > Audit workbench > Setup > Policy rule type**.</span></span>
2. <span data-ttu-id="2c75e-109">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-109">Select **New**.</span></span>
3. <span data-ttu-id="2c75e-110">Sisestage väärtus väljale **Reegli nimi**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-110">In the **Rule name** field, type a value.</span></span>
4. <span data-ttu-id="2c75e-111">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-111">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="2c75e-112">Väljal **Päringu nimi** valige **Kuluaruande rida**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-112">In the **Query name** field, select **Expense report line**</span></span>
6. <span data-ttu-id="2c75e-113">Väljal **Päringu tüüp** valige **Liitväärtus**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-113">In the **query type** field, select **Aggregate**</span></span>
7. <span data-ttu-id="2c75e-114">Väljal **Juriidiline isik** valige **Juriidiline isik**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-114">In the **Legal entity** field, select **Legal entity**</span></span>
8. <span data-ttu-id="2c75e-115">Väljal **Dokumendi kuupäeva viide** valige **Muutmise kuupäev ja kellaaeg**</span><span class="sxs-lookup"><span data-stu-id="2c75e-115">In the **Document date reference** field, select **Modified date and time**</span></span>
9. <span data-ttu-id="2c75e-116">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-116">Select **Save**.</span></span>
10. <span data-ttu-id="2c75e-117">Navigeerimispaanil avage **Moodulid > Auditi töölaud > Seadistus > Auditipoliitika**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-117">In the navigation pane, go to **Modules > Audit workbench > Setup > Audit policies**.</span></span>
11. <span data-ttu-id="2c75e-118">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-118">Select **New**.</span></span>
12. <span data-ttu-id="2c75e-119">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-119">In the **Name** field, type a value.</span></span>
13. <span data-ttu-id="2c75e-120">Laiendage jaotist **Poliitika organisatsioonid**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-120">Expand the **Policy organizations** section.</span></span>
14. <span data-ttu-id="2c75e-121">Puus valige **Contoso Meelelahutussüsteem USA**, seejärel valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-121">In the tree, select **Contoso Entertainment System USA**, then select **Add**.</span></span>
15. <span data-ttu-id="2c75e-122">Puus valige **Contoso Nõustamine USA**, seejärel valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-122">In the tree, select **Contoso Consulting USA**, then select **Add**.</span></span>
16. <span data-ttu-id="2c75e-123">Puus valige **Contoso Jaemüük USA**, seejärel valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-123">In the tree, select **Contoso Retail USA**, then select **Add**.</span></span>
17. <span data-ttu-id="2c75e-124">Ahendage jaotist **Poliitika organisatsioonid**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-124">Collapse the **Policy organizations** section.</span></span>
18. <span data-ttu-id="2c75e-125">Laiendage jaotist **Poliitika reeglid**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-125">Expand the **Policy rules** section.</span></span>
19. <span data-ttu-id="2c75e-126">Leidke ja valige loendist varem loodud poliitika reegel.</span><span class="sxs-lookup"><span data-stu-id="2c75e-126">In the list, find and select the Policy Rule that was created previously.</span></span>
20. <span data-ttu-id="2c75e-127">Valige **Poliitika reegli loomine**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-127">Select **Create policy rule**.</span></span>
21. <span data-ttu-id="2c75e-128">Sisestage kuupäev ja kellaaeg väljale **Jõustumiskuupäev**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-128">In the **Effective date** field, enter a date and time.</span></span>
22. <span data-ttu-id="2c75e-129">Valige **Filter**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-129">Select **Filter**.</span></span>
23. <span data-ttu-id="2c75e-130">Loendist valige rida **Kulukategooria** ja seadke üksikasjad valikule **Hotell**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-130">In the list, select the row for **Expense category**, and set the details to **Hotel**.</span></span>
24. <span data-ttu-id="2c75e-131">Sisestage või valige väärtus väljal **Kriteeriumid**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-131">In the **Criteria** field, enter or select a value.</span></span>
25. <span data-ttu-id="2c75e-132">Valige vahekaart **Liitväärtus**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-132">Select the **Aggregate** tab.</span></span>
26. <span data-ttu-id="2c75e-133">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-133">Select **Add**.</span></span>
27. <span data-ttu-id="2c75e-134">Loendist valige välja väärtus **Kandesumma**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-134">In the list, select a field value of **Transaction amount**.</span></span>
28. <span data-ttu-id="2c75e-135">Väljale **Väli** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="2c75e-135">In the **Field** field, enter or select a value.</span></span>
29. <span data-ttu-id="2c75e-136">Väljal **Liitväärtuse funktsioon** valige **Summa**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-136">In the **AggregateFunction** field, select **Sum**.</span></span>
30. <span data-ttu-id="2c75e-137">Valige vahekaart **Grupeerimisalus**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-137">Select the **Group by** tab.</span></span>
31. <span data-ttu-id="2c75e-138">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-138">Select **Add**.</span></span>
32. <span data-ttu-id="2c75e-139">Loendist valige välja väärtus **Töötaja**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-139">In the list, select a value of **Employee** .</span></span>
33. <span data-ttu-id="2c75e-140">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-140">Select **Add**.</span></span>
34. <span data-ttu-id="2c75e-141">Loendist valige välja väärtus **Kulukategooria**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-141">In the list, select a value of **Expense category**.</span></span>
35. <span data-ttu-id="2c75e-142">Väljale **Väli** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="2c75e-142">In the **Field** field, enter or select a value.</span></span>
36. <span data-ttu-id="2c75e-143">Valige vahekaart **Saamine**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-143">Select the **Having** tab.</span></span>
37. <span data-ttu-id="2c75e-144">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-144">Select **Add**.</span></span>
38. <span data-ttu-id="2c75e-145">Valige **Kandesumma**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-145">Select **Transaction amount**.</span></span>
39. <span data-ttu-id="2c75e-146">Väljale **Väli** sisestage või valige väärtus.</span><span class="sxs-lookup"><span data-stu-id="2c75e-146">In the **Field** field, enter or select a value.</span></span>
40. <span data-ttu-id="2c75e-147">Väljal **Liitväärtuse funktsioon** valige **Summa**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-147">In the **AggregateFunction** field, select **Sum**.</span></span>
41. <span data-ttu-id="2c75e-148">Väljale **Kriteerium** sisestage `>2000`.</span><span class="sxs-lookup"><span data-stu-id="2c75e-148">In the **Criteria** field, type `>2000`.</span></span>
42. <span data-ttu-id="2c75e-149">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-149">Select **OK**.</span></span>
43. <span data-ttu-id="2c75e-150">Valige **Test**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-150">Select **Test**.</span></span>
44. <span data-ttu-id="2c75e-151">Väljale **Dokumendi valimise alguskuupäev** sisestage kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="2c75e-151">In the **Document selection starting date** field, enter a date and time.</span></span>
45. <span data-ttu-id="2c75e-152">Väljale **Dokumendi valimise lõppkuupäev** sisestage kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="2c75e-152">In the **Document selection ending date** field, enter a date and time.</span></span>
46. <span data-ttu-id="2c75e-153">Valige **Käivita test**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-153">Select **Run test**.</span></span>
47. <span data-ttu-id="2c75e-154">Toimingupaanil valige **Auditipoliitika**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-154">On the Action Pane, select **Audit policy**.</span></span>
48. <span data-ttu-id="2c75e-155">Valige **Lisasuvandid**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-155">Select **Additional options**.</span></span>
49. <span data-ttu-id="2c75e-156">Väljale **Alguskuupäev** sisestage kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="2c75e-156">In the **Starting date** field, enter a date and time.</span></span>
50. <span data-ttu-id="2c75e-157">Väljale **Lõppkuupäev** sisestage kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="2c75e-157">In the **Ending date** field, enter a date and time.</span></span>
51. <span data-ttu-id="2c75e-158">Valige **Partii**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-158">Select **Batch**.</span></span>
52. <span data-ttu-id="2c75e-159">Laiendage jaotist **Käivita taustal**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-159">Expand the **Run in the background** section.</span></span>
53. <span data-ttu-id="2c75e-160">Valige väärtus **Jah** väljal **Pakett-töötlus**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-160">Select **Yes** in the **Batch processing** field.</span></span>
54. <span data-ttu-id="2c75e-161">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-161">Select **OK**.</span></span>
55. <span data-ttu-id="2c75e-162">Navigeerimispaanil avage **Moodulid > Auditi töölaud > Auditi juhtumid**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-162">In the navigation pane, go to **Modules > Audit workbench > Audit cases**.</span></span>
56. <span data-ttu-id="2c75e-163">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="2c75e-163">In the list, find and select the desired record.</span></span>
57. <span data-ttu-id="2c75e-164">Laiendage jaotist **Seosed**.</span><span class="sxs-lookup"><span data-stu-id="2c75e-164">Expand the **Associations** section.</span></span>
58. <span data-ttu-id="2c75e-165">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="2c75e-165">In the list, find and select the desired record.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]