---
title: Juurdepääs rakenduse metaandmetele ER-konfiguratsiooni abil
description: Selle teema sammud selgitavad, kuidas Regulatory configuration service (RCS) kasutaja saab kujundada uut elektroonilise aruandluse (ER) mudeli kaardistamise, kasutades metaandmeid Finance and Operations.
author: NickSelin
manager: AnnBe
ms.date: 06/28/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-06-28
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b95b41b27cecd4c71ed7646f329cf5736a01b561
ms.sourcegitcommit: 287d78e6afdaf40c499e5db6c4531f2b26dbaca0
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/04/2019
ms.locfileid: "1727025"
---
# <a name="access-application-metadata-by-using-er-configuration"></a><span data-ttu-id="8be22-103">Juurdepääs rakenduse metaandmetele ER-konfiguratsiooni abil</span><span class="sxs-lookup"><span data-stu-id="8be22-103">Access application metadata by using ER configuration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8be22-104">Järgmised etapid selgitavad, kuidas süsteemi administraatori või elektroonilise aruandluse arendaja rolliga lahenduse Regulatory Configuration Service (RCS) kasutaja saab kavandada uue elektroonilise aruandluse (ER) mudelivastenduse kasutades rakenduse Dynamics 365 for Finance and Operations metaandmeid.</span><span class="sxs-lookup"><span data-stu-id="8be22-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using the metadata of the Dynamics 365 for Finance and Operations application.</span></span> <span data-ttu-id="8be22-105">Rakenduse metaandmetele pääseb juurde elektroonilise aruandluse metaandmete konfiguratsiooni abil, mis sisaldab metaandmete nädiskomplekti juurdepääsuks väliskaubanduse kannetele.</span><span class="sxs-lookup"><span data-stu-id="8be22-105">Application metadata will be accessed by using an ER metadata configuration that contains a sample set of metadata to access foreign trade transactions.</span></span> <span data-ttu-id="8be22-106">Etappide lõpuleviimiseks, peate esmalt läbima ECS-is etapid teemas [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="8be22-106">To complete these steps, in RCS you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> <span data-ttu-id="8be22-107">Seejärel viige lõpuni rakenduses Finance and Operations etapid teemas [(ER) RCS-i jaoks kasutatavate rakenduse metaandmete ettevalmistamine](prepare-application-metadata-rcs.md).</span><span class="sxs-lookup"><span data-stu-id="8be22-107">Then, in Finance and Operations, complete the steps in the topic, [(ER) Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8be22-108">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="8be22-108">Prerequisites</span></span>
1. <span data-ttu-id="8be22-109">Avage **Kõik tööruumid** > **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="8be22-109">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="8be22-110">Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja märgitud kui **Aktiivne**.</span><span class="sxs-lookup"><span data-stu-id="8be22-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="8be22-111">Kui te ei näe seda konfiguratsioonipakkujat, peate esmalt läbima protseduuris [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](er-configuration-provider-mark-it-active-2016-11.md) toodud juhised.</span><span class="sxs-lookup"><span data-stu-id="8be22-111">If you don’t see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="import-metadata-configuration"></a><span data-ttu-id="8be22-112">Importige metaandmete konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="8be22-112">Import metadata configuration</span></span> 
1. <span data-ttu-id="8be22-113">Klõpsake valikut **Metaandmete konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="8be22-113">Click **Metadata configurations**.</span></span> 
2. <span data-ttu-id="8be22-114">Importige ER metaandmete konfiguratsioon, mis sisaldab metaandmeid Finance and Operations rakendusest, mis on konfigureeritud looma elektroonilisi dokumente väliskaubanduse äritegevuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="8be22-114">Import the ER metadata configuration that contains metadata from the Finance and Operations application that is configured to generate electronic documents for foreign trade business.</span></span> <span data-ttu-id="8be22-115">See ER metaandmete konfiguratsioon on eksporditud XML-failina, samal ajal kui viiakse läbi protseduurion [(ER) RCS-i jaoks kasutatavate rakenduse metaandmete ettevalmistamine](prepare-application-metadata-rcs.md) etappe.</span><span class="sxs-lookup"><span data-stu-id="8be22-115">This ER metadata configuration has been exported as XML file while the steps in the [(ER) Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md) procedure have been completed.</span></span> 
3. <span data-ttu-id="8be22-116">Klõpsake valikut **Vahetus**.</span><span class="sxs-lookup"><span data-stu-id="8be22-116">Click **Exchange**.</span></span> 
4. <span data-ttu-id="8be22-117">Klõpsake valikut **Laadi XML-failist**.</span><span class="sxs-lookup"><span data-stu-id="8be22-117">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="8be22-118">Klõpsake **Sirvi** ja valige fail "Väliskaubanduse metaandmed.xml".</span><span class="sxs-lookup"><span data-stu-id="8be22-118">Click **Browse** and select the ‘Foreign trade metadata.xml’ file.</span></span> 
6. <span data-ttu-id="8be22-119">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="8be22-119">Click **OK**.</span></span> 
7. <span data-ttu-id="8be22-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="8be22-120">Close the page.</span></span> 

## <a name="create-data-model-configuration"></a><span data-ttu-id="8be22-121">Looge andmemudeli konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="8be22-121">Create data model configuration</span></span>
1. <span data-ttu-id="8be22-122">Klõpsake valikut **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="8be22-122">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="8be22-123">Klõpsake valikut **Loo konfiguratsioon**, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="8be22-123">Click **Create configuration** to open the drop dialog.</span></span> 
3. <span data-ttu-id="8be22-124">Sisestage väljale **Nimi** "Väliskaubanduse mudel".</span><span class="sxs-lookup"><span data-stu-id="8be22-124">In the **Name** field, type 'Foreign trade model'.</span></span> 
4. <span data-ttu-id="8be22-125">Klõpsake **Loo konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="8be22-125">Click **Create configuration**.</span></span> 
5. <span data-ttu-id="8be22-126">Klõpsake valikut **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="8be22-126">Click **Designer**.</span></span> 
6. <span data-ttu-id="8be22-127">Rippdialoogi avamiseks klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="8be22-127">Click **New** to open the drop dialog.</span></span> 
7. <span data-ttu-id="8be22-128">Sisestage väljale **Nimi** "Juur".</span><span class="sxs-lookup"><span data-stu-id="8be22-128">In the **Name** field, type 'Root'.</span></span> 
8. <span data-ttu-id="8be22-129">Klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="8be22-129">Click **Add**.</span></span> 
9. <span data-ttu-id="8be22-130">Rippdialoogi avamiseks klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="8be22-130">Click **New** to open the drop dialog.</span></span> 
10. <span data-ttu-id="8be22-131">Trükkive "Kanne" väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="8be22-131">In the **Name** field, type 'Transaction'.</span></span> 
11. <span data-ttu-id="8be22-132">Valige väljalt **Üksuse tüüp** suvand **Kirjete loend**.</span><span class="sxs-lookup"><span data-stu-id="8be22-132">In the **Item type** field, select **Record list**.</span></span> 
12. <span data-ttu-id="8be22-133">Klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="8be22-133">Click **Add**.</span></span> 
13. <span data-ttu-id="8be22-134">Rippdialoogi avamiseks klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="8be22-134">Click **New** to open the drop dialog.</span></span> 
14. <span data-ttu-id="8be22-135">Trükkige "Kaubakood" väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="8be22-135">In the **Name** field, type 'Commodity code'.</span></span> 
15. <span data-ttu-id="8be22-136">Valige väljalt **Üksuse tüüp** suvand **String**.</span><span class="sxs-lookup"><span data-stu-id="8be22-136">In the **Item type** field, select **String**.</span></span> 
16. <span data-ttu-id="8be22-137">Klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="8be22-137">Click **Add**.</span></span> 
17. <span data-ttu-id="8be22-138">Rippdialoogi avamiseks klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="8be22-138">Click **New** to open the drop dialog.</span></span> 
18. <span data-ttu-id="8be22-139">Trükkige "Arveldatud summa" väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="8be22-139">In the **Name** field, type 'Invoiced amount'.</span></span> 
19. <span data-ttu-id="8be22-140">Väljal **Üksuse tüüp** valige **Tegelik**.</span><span class="sxs-lookup"><span data-stu-id="8be22-140">In the **Item type** field, select **Real**.</span></span> 
20. <span data-ttu-id="8be22-141">Klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="8be22-141">Click **Add**.</span></span> 
21. <span data-ttu-id="8be22-142">Rippdialoogi avamiseks klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="8be22-142">Click **New** to open the drop dialog.</span></span> 
22. <span data-ttu-id="8be22-143">Trükkige "Kuupäev" väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="8be22-143">In the **Name** field, type 'Date'.</span></span> 
23. <span data-ttu-id="8be22-144">Väljalt **Üksuse tüüp** valige **Kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="8be22-144">In the **Item type** field, select **Date**.</span></span> 
24. <span data-ttu-id="8be22-145">Klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="8be22-145">Click **Add**.</span></span> 
25. <span data-ttu-id="8be22-146">Klõpsake nupul **Juure viide**.</span><span class="sxs-lookup"><span data-stu-id="8be22-146">Click **Root reference**.</span></span> 
26. <span data-ttu-id="8be22-147">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="8be22-147">Click **OK**.</span></span> 
27. <span data-ttu-id="8be22-148">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="8be22-148">Click **Save**.</span></span> 
28. <span data-ttu-id="8be22-149">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="8be22-149">Close the page.</span></span> 
29. <span data-ttu-id="8be22-150">Klõpsake valikut **Muuda olekut**.</span><span class="sxs-lookup"><span data-stu-id="8be22-150">Click **Change status**.</span></span> 
30. <span data-ttu-id="8be22-151">Klõpsake valikut **Vii lõpule**.</span><span class="sxs-lookup"><span data-stu-id="8be22-151">Click **Complete**.</span></span> 
31. <span data-ttu-id="8be22-152">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="8be22-152">Click **OK**.</span></span> 

## <a name="create-model-mapping-configuration"></a><span data-ttu-id="8be22-153">Looge mudelivastenduse konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="8be22-153">Create model mapping configuration</span></span> 
1. <span data-ttu-id="8be22-154">Klõpsake valikut **Loo konfiguratsioon**, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="8be22-154">Click **Create configuration** to open the drop dialog.</span></span> 
2. <span data-ttu-id="8be22-155">Sisestage väljale **Uus** suvand „Mudelivastendus, mis põhineb väliskaubanduse mudeli andmemudelil".</span><span class="sxs-lookup"><span data-stu-id="8be22-155">In the **New** field, enter 'Model Mapping based on data model Foreign trade model'.</span></span> 
3. <span data-ttu-id="8be22-156">Trükkige "Väliskaubanduse vastendamine" väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="8be22-156">In the **Name** field, type 'Foreign trade mapping'.</span></span> 
4. <span data-ttu-id="8be22-157">Klõpsake **Loo konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="8be22-157">Click **Create configuration**.</span></span> 
5. <span data-ttu-id="8be22-158">Laiendage jaotist **Eeltingimused**.</span><span class="sxs-lookup"><span data-stu-id="8be22-158">Expand the **Prerequisites** section.</span></span> 
6. <span data-ttu-id="8be22-159">Klõpsake valikut **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="8be22-159">Click **Edit**.</span></span> 
7. <span data-ttu-id="8be22-160">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="8be22-160">Click **New**.</span></span> 
8. <span data-ttu-id="8be22-161">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="8be22-161">In the list, mark the selected row.</span></span> 
9. <span data-ttu-id="8be22-162">Valige väljalt **Eeltingimuse komponendi tüüp** suvand **Konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="8be22-162">In the **Prerequisite component type** field, select **Configuration**.</span></span> 
10. <span data-ttu-id="8be22-163">Valige konfiguratsioon **Väliskaubanduse metaandmed**.</span><span class="sxs-lookup"><span data-stu-id="8be22-163">Select **Foreign trade metadata** configuration.</span></span> 
11. <span data-ttu-id="8be22-164">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="8be22-164">Click **Save**.</span></span> 
12. <span data-ttu-id="8be22-165">Lisasime viite konfiguratsiooni "Väliskaubanduse metaandmed" versioonile 1.</span><span class="sxs-lookup"><span data-stu-id="8be22-165">We added the reference to the version 1 of the ‘Foreign trade metadata’ configuration.</span></span> <span data-ttu-id="8be22-166">Selle konfiguratsiooni rakenduse metaandmeid pakutakse selle mudeli vastendamise kavandamise ajal.</span><span class="sxs-lookup"><span data-stu-id="8be22-166">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 
13. <span data-ttu-id="8be22-167">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="8be22-167">Close the page.</span></span> 
14. <span data-ttu-id="8be22-168">Klõpsake valikut **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="8be22-168">Click **Designer**.</span></span> 
15. <span data-ttu-id="8be22-169">Klõpsake valikut **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="8be22-169">Click **Designer**.</span></span> 
16. <span data-ttu-id="8be22-170">Valige puul väärtus **Dynamics 365 for Operations\Tabeli kirjed**.</span><span class="sxs-lookup"><span data-stu-id="8be22-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
17. <span data-ttu-id="8be22-171">Klõpsake suvandil **Juure lisamine**.</span><span class="sxs-lookup"><span data-stu-id="8be22-171">Click **Add root**.</span></span> 
18. <span data-ttu-id="8be22-172">Trükkige "Intrastat" väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="8be22-172">In the **Name** field, type 'Intrastat'.</span></span> 
19. <span data-ttu-id="8be22-173">Valige tabeli kirjed **Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="8be22-173">Select **Intrastat** table records.</span></span> 
20. <span data-ttu-id="8be22-174">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="8be22-174">Click **OK**.</span></span> 

> [!NOTE]
> <span data-ttu-id="8be22-175">Pakutakse ainult kahte tabelit, sest praegu kasutatavale metaandmete komplektile lisati ainult kaks tabelit.</span><span class="sxs-lookup"><span data-stu-id="8be22-175">The only 2 tables were offered as the only 2 tables were added into the set of metadata which is currently in use.</span></span> 

21. <span data-ttu-id="8be22-176">Klõpsake valikult **Seo**.</span><span class="sxs-lookup"><span data-stu-id="8be22-176">Click **Bind**.</span></span> 
22. <span data-ttu-id="8be22-177">Laiendage puul valikut **Intrastat** .</span><span class="sxs-lookup"><span data-stu-id="8be22-177">In the tree, expand **Intrastat**.</span></span> 
23. <span data-ttu-id="8be22-178">Tehke puul valik **Intrastat\AmountMST**.</span><span class="sxs-lookup"><span data-stu-id="8be22-178">In the tree, select **Intrastat\AmountMST**.</span></span> 
24. <span data-ttu-id="8be22-179">Laiendage puul valikut **Kanne = Intrastat** .</span><span class="sxs-lookup"><span data-stu-id="8be22-179">In the tree, expand **Transaction = Intrastat**.</span></span> 
25. <span data-ttu-id="8be22-180">Tehke puul valik **Kanne = Intrastat\Arveldatud summa**.</span><span class="sxs-lookup"><span data-stu-id="8be22-180">In the tree, select **Transaction = Intrastat\Invoiced amount**.</span></span> 
26. <span data-ttu-id="8be22-181">Klõpsake valikult **Seo**.</span><span class="sxs-lookup"><span data-stu-id="8be22-181">Click **Bind**.</span></span> 
27. <span data-ttu-id="8be22-182">Tehke puul valik **Intrastat\TransDate**.</span><span class="sxs-lookup"><span data-stu-id="8be22-182">In the tree, select **Intrastat\TransDate**.</span></span> 
28. <span data-ttu-id="8be22-183">Tehke puul valik **Kanne = Intrastat\Kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="8be22-183">In the tree, select **Transaction = Intrastat\Date**.</span></span> 
29. <span data-ttu-id="8be22-184">Klõpsake valikult **Seo**.</span><span class="sxs-lookup"><span data-stu-id="8be22-184">Click **Bind**.</span></span> 
30. <span data-ttu-id="8be22-185">Laiendage puul valikut **Intrastat\>Seosed**.</span><span class="sxs-lookup"><span data-stu-id="8be22-185">In the tree, expand **Intrastat\>Relations**.</span></span> 
31. <span data-ttu-id="8be22-186">Laiendage puul valikut **Intrastat\>Seosed\IntrastatCommodity**.</span><span class="sxs-lookup"><span data-stu-id="8be22-186">In the tree, expand **Intrastat\>Relations\IntrastatCommodity**.</span></span> 
32. <span data-ttu-id="8be22-187">Tehke puul valik **Intrastat\>Seosed\IntrastatCommodity\Kood**.</span><span class="sxs-lookup"><span data-stu-id="8be22-187">In the tree, select **Intrastat\>Relations\IntrastatCommodity\Code**.</span></span> 
33. <span data-ttu-id="8be22-188">Tehke puul valik **Kanne = Intrastat\Kaubakood**.</span><span class="sxs-lookup"><span data-stu-id="8be22-188">In the tree, select **Transaction = Intrastat\Commodity code**.</span></span> 
34. <span data-ttu-id="8be22-189">Klõpsake valikult **Seo**.</span><span class="sxs-lookup"><span data-stu-id="8be22-189">Click **Bind**.</span></span> 
35. <span data-ttu-id="8be22-190">Klõpsake valikut **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="8be22-190">Click **Validate**.</span></span> 

> [!NOTE]
> <span data-ttu-id="8be22-191">Oleme andmemudeli elemendid edukalt sidunud nende andmeallikate üksustega, mida on viidatud elektroonilise aruandluse metaandmete konfiguratsiooni rakenduse metaandmetega kirjeldatud.</span><span class="sxs-lookup"><span data-stu-id="8be22-191">We have successfully bound elements of data model with items of data sources that are described by using details of application metadata from the referred ER metadata configuration.</span></span> 
36. <span data-ttu-id="8be22-192">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="8be22-192">Click **Save**.</span></span> 
37. <span data-ttu-id="8be22-193">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="8be22-193">Close the page.</span></span> 
38. <span data-ttu-id="8be22-194">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="8be22-194">Close the page.</span></span> 
39. <span data-ttu-id="8be22-195">Kui teil on vaja laiendada olemasolevat metaandmete komplekti, saate seda teha rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8be22-195">When you need to extend the existing set of metadata, you can do it in Finance and Operations.</span></span> <span data-ttu-id="8be22-196">Seejärel saate uue lõpule viidud ER metaandmete konfiguratsiooni versiooni rakendusest Finance and Operations eksportida, importida selle RCS-sse ja värskendada konfigureeritud mudeli vastenduse konfiguratsiooni eeltingimusi viitama uuele imporditud metaandmete konfiguratsiooni versioonile.</span><span class="sxs-lookup"><span data-stu-id="8be22-196">Then you can export the new completed version of ER metadata configuration from Finance and Operation,s import it to RCS, and update the prerequisites of the configured model mapping configuration referring to a new version of imported metadata configuration.</span></span> 

> [!NOTE]
> <span data-ttu-id="8be22-197">Selline rakenduste metaandmete info hankimine on ainuke saadaolev meetod kohapeal juurutatud rakendustele (kui rakenduse Dynamics 365 for Finance and Operations jaoks kasutatakse kohalikke äriandmeid (LBD) või asutusesisese juurutuse mudelit).</span><span class="sxs-lookup"><span data-stu-id="8be22-197">This way of getting information about application metadata is the only one available for locally deployed applications (when local business data (LBD), or on-premises, deployment model is used for Dynamics 365 for Finance and Operations).</span></span>
        
