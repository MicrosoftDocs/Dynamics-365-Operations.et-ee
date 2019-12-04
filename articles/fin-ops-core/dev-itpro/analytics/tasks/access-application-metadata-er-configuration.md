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
ms.openlocfilehash: aa8444b081650e3d375e6f28f47866c8d4853721
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772459"
---
# <a name="access-application-metadata-by-using-er-configuration"></a><span data-ttu-id="ab495-103">Juurdepääs rakenduse metaandmetele ER-konfiguratsiooni abil</span><span class="sxs-lookup"><span data-stu-id="ab495-103">Access application metadata by using ER configuration</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ab495-104">Järgmised etapid selgitavad, kuidas süsteemi administraatori või elektroonilise aruandluse arendaja rolliga lahenduse Regulatory Configuration Service (RCS) kasutaja saab kavandada uue elektroonilise aruandluse (ER) mudelivastenduse kasutades rakenduse metaandmeid.</span><span class="sxs-lookup"><span data-stu-id="ab495-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using the application metadata.</span></span> <span data-ttu-id="ab495-105">Rakenduse metaandmetele pääseb juurde elektroonilise aruandluse metaandmete konfiguratsiooni abil, mis sisaldab metaandmete nädiskomplekti juurdepääsuks väliskaubanduse kannetele.</span><span class="sxs-lookup"><span data-stu-id="ab495-105">Application metadata will be accessed by using an ER metadata configuration that contains a sample set of metadata to access foreign trade transactions.</span></span> <span data-ttu-id="ab495-106">Etappide lõpuleviimiseks, peate esmalt läbima ECS-is etapid teemas [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="ab495-106">To complete these steps, in RCS you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> <span data-ttu-id="ab495-107">Seejärel viige lõpule etapid teemas [Rakenduse metaandmete ettevalmistamine RCS-is kasutamiseks](prepare-application-metadata-rcs.md).</span><span class="sxs-lookup"><span data-stu-id="ab495-107">Then complete the steps in the topic, [Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ab495-108">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="ab495-108">Prerequisites</span></span>
1. <span data-ttu-id="ab495-109">Avage **Kõik tööruumid** > **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="ab495-109">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="ab495-110">Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja märgitud kui **Aktiivne**.</span><span class="sxs-lookup"><span data-stu-id="ab495-110">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="ab495-111">Kui te ei näe seda konfiguratsioonipakkujat, peate esmalt läbima protseduuris [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](er-configuration-provider-mark-it-active-2016-11.md) toodud juhised.</span><span class="sxs-lookup"><span data-stu-id="ab495-111">If you don’t see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="import-metadata-configuration"></a><span data-ttu-id="ab495-112">Importige metaandmete konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="ab495-112">Import metadata configuration</span></span> 
1. <span data-ttu-id="ab495-113">Klõpsake valikut **Metaandmete konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="ab495-113">Click **Metadata configurations**.</span></span> 
2. <span data-ttu-id="ab495-114">Importige ER metaandmete konfiguratsioon, mis sisaldab metaandmeid, mis on konfigureeritud looma elektroonilisi dokumente väliskaubanduse äritegevuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="ab495-114">Import the ER metadata configuration that contains metadata that has been configured to generate electronic documents for foreign trade business.</span></span> <span data-ttu-id="ab495-115">See ER-i metaandmete konfiguratsioon on eksporditud XML-failina, samal ajal kui etapid protseduuris [Rakenduse metaandmete ettevalmistamine RCS-is kasutamiseks](prepare-application-metadata-rcs.md) on lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="ab495-115">This ER metadata configuration has been exported as XML file while the steps in the [Prepare application metadata to be used in RCS](prepare-application-metadata-rcs.md) procedure have been completed.</span></span> 
3. <span data-ttu-id="ab495-116">Klõpsake valikut **Vahetus**.</span><span class="sxs-lookup"><span data-stu-id="ab495-116">Click **Exchange**.</span></span> 
4. <span data-ttu-id="ab495-117">Klõpsake valikut **Laadi XML-failist**.</span><span class="sxs-lookup"><span data-stu-id="ab495-117">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="ab495-118">Klõpsake **Sirvi** ja valige fail "Väliskaubanduse metaandmed.xml".</span><span class="sxs-lookup"><span data-stu-id="ab495-118">Click **Browse** and select the ‘Foreign trade metadata.xml’ file.</span></span> 
6. <span data-ttu-id="ab495-119">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="ab495-119">Click **OK**.</span></span> 
7. <span data-ttu-id="ab495-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ab495-120">Close the page.</span></span> 

## <a name="create-data-model-configuration"></a><span data-ttu-id="ab495-121">Looge andmemudeli konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="ab495-121">Create data model configuration</span></span>
1. <span data-ttu-id="ab495-122">Klõpsake valikut **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="ab495-122">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="ab495-123">Klõpsake valikut **Loo konfiguratsioon**, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="ab495-123">Click **Create configuration** to open the drop dialog.</span></span> 
3. <span data-ttu-id="ab495-124">Sisestage väljale **Nimi** "Väliskaubanduse mudel".</span><span class="sxs-lookup"><span data-stu-id="ab495-124">In the **Name** field, type 'Foreign trade model'.</span></span> 
4. <span data-ttu-id="ab495-125">Klõpsake **Loo konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="ab495-125">Click **Create configuration**.</span></span> 
5. <span data-ttu-id="ab495-126">Klõpsake valikut **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="ab495-126">Click **Designer**.</span></span> 
6. <span data-ttu-id="ab495-127">Rippdialoogi avamiseks klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="ab495-127">Click **New** to open the drop dialog.</span></span> 
7. <span data-ttu-id="ab495-128">Sisestage väljale **Nimi** "Juur".</span><span class="sxs-lookup"><span data-stu-id="ab495-128">In the **Name** field, type 'Root'.</span></span> 
8. <span data-ttu-id="ab495-129">Klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="ab495-129">Click **Add**.</span></span> 
9. <span data-ttu-id="ab495-130">Rippdialoogi avamiseks klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="ab495-130">Click **New** to open the drop dialog.</span></span> 
10. <span data-ttu-id="ab495-131">Trükkive "Kanne" väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="ab495-131">In the **Name** field, type 'Transaction'.</span></span> 
11. <span data-ttu-id="ab495-132">Valige väljalt **Üksuse tüüp** suvand **Kirjete loend**.</span><span class="sxs-lookup"><span data-stu-id="ab495-132">In the **Item type** field, select **Record list**.</span></span> 
12. <span data-ttu-id="ab495-133">Klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="ab495-133">Click **Add**.</span></span> 
13. <span data-ttu-id="ab495-134">Rippdialoogi avamiseks klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="ab495-134">Click **New** to open the drop dialog.</span></span> 
14. <span data-ttu-id="ab495-135">Trükkige "Kaubakood" väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="ab495-135">In the **Name** field, type 'Commodity code'.</span></span> 
15. <span data-ttu-id="ab495-136">Valige väljalt **Üksuse tüüp** suvand **String**.</span><span class="sxs-lookup"><span data-stu-id="ab495-136">In the **Item type** field, select **String**.</span></span> 
16. <span data-ttu-id="ab495-137">Klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="ab495-137">Click **Add**.</span></span> 
17. <span data-ttu-id="ab495-138">Rippdialoogi avamiseks klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="ab495-138">Click **New** to open the drop dialog.</span></span> 
18. <span data-ttu-id="ab495-139">Trükkige "Arveldatud summa" väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="ab495-139">In the **Name** field, type 'Invoiced amount'.</span></span> 
19. <span data-ttu-id="ab495-140">Väljal **Üksuse tüüp** valige **Tegelik**.</span><span class="sxs-lookup"><span data-stu-id="ab495-140">In the **Item type** field, select **Real**.</span></span> 
20. <span data-ttu-id="ab495-141">Klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="ab495-141">Click **Add**.</span></span> 
21. <span data-ttu-id="ab495-142">Rippdialoogi avamiseks klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="ab495-142">Click **New** to open the drop dialog.</span></span> 
22. <span data-ttu-id="ab495-143">Trükkige "Kuupäev" väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="ab495-143">In the **Name** field, type 'Date'.</span></span> 
23. <span data-ttu-id="ab495-144">Väljalt **Üksuse tüüp** valige **Kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="ab495-144">In the **Item type** field, select **Date**.</span></span> 
24. <span data-ttu-id="ab495-145">Klõpsake käsku **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="ab495-145">Click **Add**.</span></span> 
25. <span data-ttu-id="ab495-146">Klõpsake nupul **Juure viide**.</span><span class="sxs-lookup"><span data-stu-id="ab495-146">Click **Root reference**.</span></span> 
26. <span data-ttu-id="ab495-147">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="ab495-147">Click **OK**.</span></span> 
27. <span data-ttu-id="ab495-148">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ab495-148">Click **Save**.</span></span> 
28. <span data-ttu-id="ab495-149">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ab495-149">Close the page.</span></span> 
29. <span data-ttu-id="ab495-150">Klõpsake valikut **Muuda olekut**.</span><span class="sxs-lookup"><span data-stu-id="ab495-150">Click **Change status**.</span></span> 
30. <span data-ttu-id="ab495-151">Klõpsake valikut **Vii lõpule**.</span><span class="sxs-lookup"><span data-stu-id="ab495-151">Click **Complete**.</span></span> 
31. <span data-ttu-id="ab495-152">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="ab495-152">Click **OK**.</span></span> 

## <a name="create-model-mapping-configuration"></a><span data-ttu-id="ab495-153">Looge mudelivastenduse konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="ab495-153">Create model mapping configuration</span></span> 
1. <span data-ttu-id="ab495-154">Klõpsake valikut **Loo konfiguratsioon**, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="ab495-154">Click **Create configuration** to open the drop dialog.</span></span> 
2. <span data-ttu-id="ab495-155">Sisestage väljale **Uus** suvand „Mudelivastendus, mis põhineb väliskaubanduse mudeli andmemudelil".</span><span class="sxs-lookup"><span data-stu-id="ab495-155">In the **New** field, enter 'Model Mapping based on data model Foreign trade model'.</span></span> 
3. <span data-ttu-id="ab495-156">Trükkige "Väliskaubanduse vastendamine" väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="ab495-156">In the **Name** field, type 'Foreign trade mapping'.</span></span> 
4. <span data-ttu-id="ab495-157">Klõpsake **Loo konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="ab495-157">Click **Create configuration**.</span></span> 
5. <span data-ttu-id="ab495-158">Laiendage jaotist **Eeltingimused**.</span><span class="sxs-lookup"><span data-stu-id="ab495-158">Expand the **Prerequisites** section.</span></span> 
6. <span data-ttu-id="ab495-159">Klõpsake valikut **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="ab495-159">Click **Edit**.</span></span> 
7. <span data-ttu-id="ab495-160">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="ab495-160">Click **New**.</span></span> 
8. <span data-ttu-id="ab495-161">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="ab495-161">In the list, mark the selected row.</span></span> 
9. <span data-ttu-id="ab495-162">Valige väljalt **Eeltingimuse komponendi tüüp** suvand **Konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="ab495-162">In the **Prerequisite component type** field, select **Configuration**.</span></span> 
10. <span data-ttu-id="ab495-163">Valige konfiguratsioon **Väliskaubanduse metaandmed**.</span><span class="sxs-lookup"><span data-stu-id="ab495-163">Select **Foreign trade metadata** configuration.</span></span> 
11. <span data-ttu-id="ab495-164">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ab495-164">Click **Save**.</span></span> 
12. <span data-ttu-id="ab495-165">Lisasime viite konfiguratsiooni "Väliskaubanduse metaandmed" versioonile 1.</span><span class="sxs-lookup"><span data-stu-id="ab495-165">We added the reference to the version 1 of the ‘Foreign trade metadata’ configuration.</span></span> <span data-ttu-id="ab495-166">Selle konfiguratsiooni rakenduse metaandmeid pakutakse selle mudeli vastendamise kavandamise ajal.</span><span class="sxs-lookup"><span data-stu-id="ab495-166">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 
13. <span data-ttu-id="ab495-167">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ab495-167">Close the page.</span></span> 
14. <span data-ttu-id="ab495-168">Klõpsake valikut **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="ab495-168">Click **Designer**.</span></span> 
15. <span data-ttu-id="ab495-169">Klõpsake valikut **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="ab495-169">Click **Designer**.</span></span> 
16. <span data-ttu-id="ab495-170">Valige puul väärtus **Dynamics 365 for Operations\Tabeli kirjed**.</span><span class="sxs-lookup"><span data-stu-id="ab495-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
17. <span data-ttu-id="ab495-171">Klõpsake suvandil **Juure lisamine**.</span><span class="sxs-lookup"><span data-stu-id="ab495-171">Click **Add root**.</span></span> 
18. <span data-ttu-id="ab495-172">Trükkige "Intrastat" väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="ab495-172">In the **Name** field, type 'Intrastat'.</span></span> 
19. <span data-ttu-id="ab495-173">Valige tabeli kirjed **Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="ab495-173">Select **Intrastat** table records.</span></span> 
20. <span data-ttu-id="ab495-174">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="ab495-174">Click **OK**.</span></span> 

> [!NOTE]
> <span data-ttu-id="ab495-175">Pakutakse ainult kahte tabelit, sest praegu kasutatavale metaandmete komplektile lisati ainult kaks tabelit.</span><span class="sxs-lookup"><span data-stu-id="ab495-175">The only 2 tables were offered as the only 2 tables were added into the set of metadata which is currently in use.</span></span> 

21. <span data-ttu-id="ab495-176">Klõpsake valikult **Seo**.</span><span class="sxs-lookup"><span data-stu-id="ab495-176">Click **Bind**.</span></span> 
22. <span data-ttu-id="ab495-177">Laiendage puul valikut **Intrastat** .</span><span class="sxs-lookup"><span data-stu-id="ab495-177">In the tree, expand **Intrastat**.</span></span> 
23. <span data-ttu-id="ab495-178">Tehke puul valik **Intrastat\AmountMST**.</span><span class="sxs-lookup"><span data-stu-id="ab495-178">In the tree, select **Intrastat\AmountMST**.</span></span> 
24. <span data-ttu-id="ab495-179">Laiendage puul valikut **Kanne = Intrastat** .</span><span class="sxs-lookup"><span data-stu-id="ab495-179">In the tree, expand **Transaction = Intrastat**.</span></span> 
25. <span data-ttu-id="ab495-180">Tehke puul valik **Kanne = Intrastat\Arveldatud summa**.</span><span class="sxs-lookup"><span data-stu-id="ab495-180">In the tree, select **Transaction = Intrastat\Invoiced amount**.</span></span> 
26. <span data-ttu-id="ab495-181">Klõpsake valikult **Seo**.</span><span class="sxs-lookup"><span data-stu-id="ab495-181">Click **Bind**.</span></span> 
27. <span data-ttu-id="ab495-182">Tehke puul valik **Intrastat\TransDate**.</span><span class="sxs-lookup"><span data-stu-id="ab495-182">In the tree, select **Intrastat\TransDate**.</span></span> 
28. <span data-ttu-id="ab495-183">Tehke puul valik **Kanne = Intrastat\Kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="ab495-183">In the tree, select **Transaction = Intrastat\Date**.</span></span> 
29. <span data-ttu-id="ab495-184">Klõpsake valikult **Seo**.</span><span class="sxs-lookup"><span data-stu-id="ab495-184">Click **Bind**.</span></span> 
30. <span data-ttu-id="ab495-185">Laiendage puul valikut **Intrastat\>Seosed**.</span><span class="sxs-lookup"><span data-stu-id="ab495-185">In the tree, expand **Intrastat\>Relations**.</span></span> 
31. <span data-ttu-id="ab495-186">Laiendage puul valikut **Intrastat\>Seosed\IntrastatCommodity**.</span><span class="sxs-lookup"><span data-stu-id="ab495-186">In the tree, expand **Intrastat\>Relations\IntrastatCommodity**.</span></span> 
32. <span data-ttu-id="ab495-187">Tehke puul valik **Intrastat\>Seosed\IntrastatCommodity\Kood**.</span><span class="sxs-lookup"><span data-stu-id="ab495-187">In the tree, select **Intrastat\>Relations\IntrastatCommodity\Code**.</span></span> 
33. <span data-ttu-id="ab495-188">Tehke puul valik **Kanne = Intrastat\Kaubakood**.</span><span class="sxs-lookup"><span data-stu-id="ab495-188">In the tree, select **Transaction = Intrastat\Commodity code**.</span></span> 
34. <span data-ttu-id="ab495-189">Klõpsake valikult **Seo**.</span><span class="sxs-lookup"><span data-stu-id="ab495-189">Click **Bind**.</span></span> 
35. <span data-ttu-id="ab495-190">Klõpsake valikut **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="ab495-190">Click **Validate**.</span></span> 

> [!NOTE]
> <span data-ttu-id="ab495-191">Oleme andmemudeli elemendid edukalt sidunud nende andmeallikate üksustega, mida on viidatud elektroonilise aruandluse metaandmete konfiguratsiooni rakenduse metaandmetega kirjeldatud.</span><span class="sxs-lookup"><span data-stu-id="ab495-191">We have successfully bound elements of data model with items of data sources that are described by using details of application metadata from the referred ER metadata configuration.</span></span> 
36. <span data-ttu-id="ab495-192">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ab495-192">Click **Save**.</span></span> 
37. <span data-ttu-id="ab495-193">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ab495-193">Close the page.</span></span> 
38. <span data-ttu-id="ab495-194">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ab495-194">Close the page.</span></span> 
39. <span data-ttu-id="ab495-195">Vajadusel saate olemasolevat metaandmete kogumit laiendada ja seejärel eksportida ER metaandmete konfiguratsiooni uue lõpule viidud versiooni.</span><span class="sxs-lookup"><span data-stu-id="ab495-195">When needed, you can extend the existing set of metadata and then export the new completed version of ER metadata configuration.</span></span> <span data-ttu-id="ab495-196">Seejärel saate importida selle RCS-i ja värskendada konfigureeritud mudeli vastendamise konfiguratsiooni eeltingimused, mis viitavad imporditud metaandmete konfiguratsiooni uuele versioonile.</span><span class="sxs-lookup"><span data-stu-id="ab495-196">You can then import it to RCS, and update the prerequisites of the configured model mapping configuration referring to a new version of imported metadata configuration.</span></span> 

> [!NOTE]
> <span data-ttu-id="ab495-197">Selline rakenduste metaandmete info hankimine on ainuke saadaolev meetod kohapeal juurutatud rakendustele (kui kasutatakse kohalikke äriandmeid (LBD) või asutusesisese juurutuse mudelit).</span><span class="sxs-lookup"><span data-stu-id="ab495-197">This way of getting information about application metadata is the only one available for locally deployed applications (when local business data (LBD), or on-premises, deployment model is used).</span></span>
        