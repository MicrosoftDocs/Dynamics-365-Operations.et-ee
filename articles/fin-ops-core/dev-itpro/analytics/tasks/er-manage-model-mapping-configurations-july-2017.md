---
title: Elektroonilise aruandluse (ER) mudelivastenduse haldamine eraldi ER-i konfiguratsioonides
description: Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad hallata elektroonilise aruandluse (ER) mudelivastendusi eraldi ER-i konfiguratsioonides.
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b8ff3b419caafec626497c65ea18ca24ca95cb5d
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143049"
---
# <a name="manage-er-model-mapping-in-separate-er-configurations"></a><span data-ttu-id="6c326-103">Elektroonilise aruandluse (ER) mudelivastenduse haldamine eraldi ER-i konfiguratsioonides</span><span class="sxs-lookup"><span data-stu-id="6c326-103">Manage ER model mapping in separate ER configurations</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6c326-104">Järgmistes etappides selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad hallata elektroonilise aruandluse (ER) mudelivastendusi eraldi ER-i konfiguratsioonides.</span><span class="sxs-lookup"><span data-stu-id="6c326-104">The following steps explain how a user assigned to the System administrator or Electronic reporting developer role can manage Electronic reporting (ER) model mappings in separate ER configurations.</span></span> <span data-ttu-id="6c326-105">Juhendit järgides loote näidisettevõtte Litware, Inc. jaoks vajalikud ER-i konfiguratsioonid. Juhendis ülesannete lõpetamiseks peab esmalt täitma juhises „ER konfiguratsioonipakkuja loomine” toodud toimingud ja märkida see aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="6c326-105">In this task guide, you will create required ER configurations for the sample company, Litware, Inc. To complete this task guide, you must first complete the steps in the task guide, "ER Create a configuration provider" and mark it as active.</span></span> 

<span data-ttu-id="6c326-106">Kuna ER-i konfiguratsioonid on ettevõtete vahel ühisjagamises, võite läbida juhendi toimingud ükskõik, millise ettevõtte andmekogumiga.</span><span class="sxs-lookup"><span data-stu-id="6c326-106">Because ER configurations are shared among companies, you can complete this task guide using the company data set of your choice.</span></span> <span data-ttu-id="6c326-107">Selle tegevusjuhise funktsioonid on saadaval, kui olete installinud ühe järgmistest kiirparandustest: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 rakenduse Dynamics AX 7.0 versiooni jaoks või https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 rakenduse Dynamics 365 for Operations versiooni jaoks.</span><span class="sxs-lookup"><span data-stu-id="6c326-107">The functionality for this task guide is available if you have installed one of the following hotfixes: https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012872 for the Dynamics AX 7.0 version or https://fix.lcs.dynamics.com/Issue/Resolved?kb=4012871 for the Dynamics 365 for Operations version.</span></span>

1. <span data-ttu-id="6c326-108">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="6c326-108">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="6c326-109">Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja tähistatud aktiivsena.</span><span class="sxs-lookup"><span data-stu-id="6c326-109">Verify that the configuration provider for the sample company Litware, Inc. is available and marked as active.</span></span> <span data-ttu-id="6c326-110">Kui te ei näe seda konfiguratsioonipakkujat, peate esmalt läbima tegevuse juhises „Konfiguratsioonipakkuja loomine ja selle märkimine aktiivseks” esitatud toimingud.</span><span class="sxs-lookup"><span data-stu-id="6c326-110">If you don't see this configuration provider, you must first complete the steps in the task guide, Create a configuration provider and mark it as active.</span></span>   

## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="6c326-111">Uue elektroonilise aruandluse mudeli konfiguratsiooni lisamine</span><span class="sxs-lookup"><span data-stu-id="6c326-111">Add a new ER model configuration</span></span>
1. <span data-ttu-id="6c326-112">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="6c326-112">Click Reporting configurations.</span></span>
    * <span data-ttu-id="6c326-113">Lisage uus elektroonilise aruandluse mudeli konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="6c326-113">Add a new model configuration.</span></span> <span data-ttu-id="6c326-114">Nimi peab konfiguratsioonide puus olema kordumatu.</span><span class="sxs-lookup"><span data-stu-id="6c326-114">The name must be unique in the configurations tree.</span></span>  
2. <span data-ttu-id="6c326-115">Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="6c326-115">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="6c326-116">Tippige nimeväljale tekst „Sample data model".</span><span class="sxs-lookup"><span data-stu-id="6c326-116">In the Name field, type 'Sample data model'.</span></span>
    * <span data-ttu-id="6c326-117">Näidisandmemudel</span><span class="sxs-lookup"><span data-stu-id="6c326-117">Sample data model</span></span>  
4. <span data-ttu-id="6c326-118">Klõpsake Loo konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="6c326-118">Click Create configuration.</span></span>
5. <span data-ttu-id="6c326-119">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="6c326-119">Click Designer.</span></span>
6. <span data-ttu-id="6c326-120">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6c326-120">Click New to open the drop dialog.</span></span>
7. <span data-ttu-id="6c326-121">Tippige Juur väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="6c326-121">In the Name field, type 'Root'.</span></span>
    * <span data-ttu-id="6c326-122">Juur</span><span class="sxs-lookup"><span data-stu-id="6c326-122">Root</span></span>  
8. <span data-ttu-id="6c326-123">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="6c326-123">Click Add.</span></span>
9. <span data-ttu-id="6c326-124">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6c326-124">Click New to open the drop dialog.</span></span>
10. <span data-ttu-id="6c326-125">Sisestage väljale Nimi suvand Ettevõte.</span><span class="sxs-lookup"><span data-stu-id="6c326-125">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="6c326-126">Ettevõte</span><span class="sxs-lookup"><span data-stu-id="6c326-126">Company</span></span>  
11. <span data-ttu-id="6c326-127">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="6c326-127">Click Add.</span></span>
12. <span data-ttu-id="6c326-128">Sisestage väljale Kirjeldus tekst, juriidilise isiku või ettevõtte kirjeldus, millesse kasutaja logis sisse käitusajal.</span><span class="sxs-lookup"><span data-stu-id="6c326-128">In the Description field, enter the text, Description of the legal entity or company in which a user logged at run-time.</span></span> 
    * <span data-ttu-id="6c326-129">Juriidiline isiku või ettevõtte kirjeldus kuhu kasutaja logis sisse käitusajal.</span><span class="sxs-lookup"><span data-stu-id="6c326-129">Description of the legal entity or company in which a user logged at run-time.</span></span>  
13. <span data-ttu-id="6c326-130">Valige "Juure viide".</span><span class="sxs-lookup"><span data-stu-id="6c326-130">Click Root reference.</span></span>
14. <span data-ttu-id="6c326-131">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="6c326-131">Click OK.</span></span>
15. <span data-ttu-id="6c326-132">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6c326-132">Click Save.</span></span>
16. <span data-ttu-id="6c326-133">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6c326-133">Close the page.</span></span>
17. <span data-ttu-id="6c326-134">Klõpsake valikut Muuda olekut.</span><span class="sxs-lookup"><span data-stu-id="6c326-134">Click Change status.</span></span>
18. <span data-ttu-id="6c326-135">Klõpsake valikut Valmis.</span><span class="sxs-lookup"><span data-stu-id="6c326-135">Click Complete.</span></span>
19. <span data-ttu-id="6c326-136">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="6c326-136">Click OK.</span></span>

## <a name="add-a-new-er-model-mapping-configuration"></a><span data-ttu-id="6c326-137">Uue elektroonilise aruandluse mudelivastenduse konfiguratsiooni lisamine</span><span class="sxs-lookup"><span data-stu-id="6c326-137">Add a new ER model mapping configuration</span></span>
1. <span data-ttu-id="6c326-138">Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="6c326-138">Click Create configuration to open the drop dialog.</span></span>
2. <span data-ttu-id="6c326-139">Sisestage väljale Uus suvand "Andmemudelil Näidisandmemudel põhinev mudelivastendus".</span><span class="sxs-lookup"><span data-stu-id="6c326-139">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
3. <span data-ttu-id="6c326-140">Sisestage nimeväljale tekst „Sample mapping".</span><span class="sxs-lookup"><span data-stu-id="6c326-140">In the Name field, type 'Sample mapping'.</span></span>
    * <span data-ttu-id="6c326-141">Näidisvastendamine</span><span class="sxs-lookup"><span data-stu-id="6c326-141">Sample mapping</span></span>  
4. <span data-ttu-id="6c326-142">Klõpsake Loo konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="6c326-142">Click Create configuration.</span></span>
5. <span data-ttu-id="6c326-143">Laiendage jaotist Eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="6c326-143">Expand the Prerequisites section.</span></span>
    * <span data-ttu-id="6c326-144">Pange tähele, et juurutuste eeltingimuste grupp on lisatud automaatselt.</span><span class="sxs-lookup"><span data-stu-id="6c326-144">Note that the Implementations prerequisites group has been added automatically.</span></span> <span data-ttu-id="6c326-145">Grupi sisaldab eeltingimuse komponenti, mis viitab ülataseme andmemudeli konfiguratsioonile ning see on märgitud juurutuseks.</span><span class="sxs-lookup"><span data-stu-id="6c326-145">The group contains the prerequisite component that refers to the parent data model configuration and is marked as Implementation.</span></span> <span data-ttu-id="6c326-146">See tähendab, et seda näidisvastendusmudeli vastenduskonfiguratsiooni peetakse andmemudeli, näidisandmemudeli, juurutamiseks.</span><span class="sxs-lookup"><span data-stu-id="6c326-146">This means that this Sample mapping model mapping configuration is considered the implementation of the data model, Sample data model.</span></span> <span data-ttu-id="6c326-147">Seetõttu sunnib see komponent elektroonilist aruandlust alla laadima mudelivastenduse konfiguratsiooni, näidisvastendust elektroonilise aruandluse hoidlast, kui mudeli konfiguratsioon, näidisandmemudel, on alla laaditud.</span><span class="sxs-lookup"><span data-stu-id="6c326-147">Therefore, this component will force ER to download the model mapping configuration, Sample mapping from an ER repository when the model configuration, Sample data model, is downloaded.</span></span>   
6. <span data-ttu-id="6c326-148">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="6c326-148">Click Designer.</span></span>
    * <span data-ttu-id="6c326-149">Pange tähele, et loodud mudelivastenduse konfiguratsiooni sisaldab uut tühja vastendamist, millel on loodud konfiguratsiooniga sama nimi.</span><span class="sxs-lookup"><span data-stu-id="6c326-149">Note that the created model mapping configuration contains a new blank mapping with the same name as the created configuration.</span></span> <span data-ttu-id="6c326-150">Võtke arvesse, et kui valitud ülataseme mudeli konfiguratsioon sisaldab mudelivastendusi, kopeeritakse need uude mudelivastenduse konfiguratsiooni.</span><span class="sxs-lookup"><span data-stu-id="6c326-150">Be aware that when a selected parent model configuration contains model mappings, they will be copied to a new model mapping configuration.</span></span>   
7. <span data-ttu-id="6c326-151">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="6c326-151">Click Designer.</span></span>
8. <span data-ttu-id="6c326-152">Valige puul väärtus Dynamics 365 for Operations \ Tabel.</span><span class="sxs-lookup"><span data-stu-id="6c326-152">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="6c326-153">Klõpsake suvandit Juure lisamine.</span><span class="sxs-lookup"><span data-stu-id="6c326-153">Click Add root.</span></span>
10. <span data-ttu-id="6c326-154">Sisestage väljale Nimi suvand Ettevõte.</span><span class="sxs-lookup"><span data-stu-id="6c326-154">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="6c326-155">Ettevõte</span><span class="sxs-lookup"><span data-stu-id="6c326-155">Company</span></span>  
11. <span data-ttu-id="6c326-156">Sisestage väljale Tabel suvand CompanyInfo.</span><span class="sxs-lookup"><span data-stu-id="6c326-156">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="6c326-157">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="6c326-157">CompanyInfo</span></span>  
12. <span data-ttu-id="6c326-158">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="6c326-158">Click OK.</span></span>
13. <span data-ttu-id="6c326-159">Laiendage puul väärtust "Company".</span><span class="sxs-lookup"><span data-stu-id="6c326-159">In the tree, expand 'Company'.</span></span>
14. <span data-ttu-id="6c326-160">Laiendage puul valikut „Company\find()“.</span><span class="sxs-lookup"><span data-stu-id="6c326-160">In the tree, expand 'Company\find()'.</span></span>
15. <span data-ttu-id="6c326-161">Tehke puul valik „Company\find()\Name".</span><span class="sxs-lookup"><span data-stu-id="6c326-161">In the tree, select 'Company\find()\Name'.</span></span>
16. <span data-ttu-id="6c326-162">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="6c326-162">Click Bind.</span></span>
17. <span data-ttu-id="6c326-163">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6c326-163">Click Save.</span></span>
18. <span data-ttu-id="6c326-164">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6c326-164">Close the page.</span></span>
19. <span data-ttu-id="6c326-165">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6c326-165">Close the page.</span></span>
20. <span data-ttu-id="6c326-166">Klõpsake tegumiribal valikut Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="6c326-166">On the Action Pane, click Configurations.</span></span>
21. <span data-ttu-id="6c326-167">Klõpsake valikut Kasutaja parameetrid.</span><span class="sxs-lookup"><span data-stu-id="6c326-167">Click User parameters.</span></span>
22. <span data-ttu-id="6c326-168">Tehke väljal Käivita sätted valik Jah.</span><span class="sxs-lookup"><span data-stu-id="6c326-168">Select Yes in the Run settings field.</span></span>
23. <span data-ttu-id="6c326-169">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="6c326-169">Click OK.</span></span>
24. <span data-ttu-id="6c326-170">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="6c326-170">Click Edit.</span></span>
25. <span data-ttu-id="6c326-171">Tehke väljal Käivita mustand valik Jah.</span><span class="sxs-lookup"><span data-stu-id="6c326-171">Select Yes in the Run Draft field.</span></span>

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="6c326-172">Uue elektroonilise aruandluse vormingu konfiguratsiooni lisamine</span><span class="sxs-lookup"><span data-stu-id="6c326-172">Add a new ER format configuration</span></span>
1. <span data-ttu-id="6c326-173">Tehke puul valik „Sample data model".</span><span class="sxs-lookup"><span data-stu-id="6c326-173">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="6c326-174">Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="6c326-174">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="6c326-175">Sisestage väljale Uus suvand „Format based on data model Sample data model".</span><span class="sxs-lookup"><span data-stu-id="6c326-175">In the New field, enter 'Format based on data model Sample data model'.</span></span>
4. <span data-ttu-id="6c326-176">Sisestage nimeväljale suvand „Sample format".</span><span class="sxs-lookup"><span data-stu-id="6c326-176">In the Name field, type 'Sample format'.</span></span>
    * <span data-ttu-id="6c326-177">Näidise vorming</span><span class="sxs-lookup"><span data-stu-id="6c326-177">Sample format</span></span>  
5. <span data-ttu-id="6c326-178">Klõpsake Loo konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="6c326-178">Click Create configuration.</span></span>
6. <span data-ttu-id="6c326-179">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="6c326-179">Click Designer.</span></span>
7. <span data-ttu-id="6c326-180">Klõpsake suvandit Lisa juur rippdialoogi avamiseks.</span><span class="sxs-lookup"><span data-stu-id="6c326-180">Click Add root to open the drop dialog.</span></span>
8. <span data-ttu-id="6c326-181">Valige puul suvand Tekst\String.</span><span class="sxs-lookup"><span data-stu-id="6c326-181">In the tree, select 'Text\String'.</span></span>
9. <span data-ttu-id="6c326-182">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="6c326-182">Click OK.</span></span>
10. <span data-ttu-id="6c326-183">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="6c326-183">Click the Mapping tab.</span></span>
11. <span data-ttu-id="6c326-184">Laiendage puus sõlme „model”.</span><span class="sxs-lookup"><span data-stu-id="6c326-184">In the tree, expand 'model'.</span></span>
12. <span data-ttu-id="6c326-185">Tehke puul valik „model\Company".</span><span class="sxs-lookup"><span data-stu-id="6c326-185">In the tree, select 'model\Company'.</span></span>
13. <span data-ttu-id="6c326-186">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="6c326-186">Click Bind.</span></span>
14. <span data-ttu-id="6c326-187">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6c326-187">Click Save.</span></span>
15. <span data-ttu-id="6c326-188">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6c326-188">Close the page.</span></span>
    * <span data-ttu-id="6c326-189">Käivitage loodud vormingu mustandiversioon testimise eesmärgil.</span><span class="sxs-lookup"><span data-stu-id="6c326-189">Run the draft version of the created format for testing purposes.</span></span>  
16. <span data-ttu-id="6c326-190">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="6c326-190">Click Run.</span></span>
    * <span data-ttu-id="6c326-191">Klõpsake Versioonide kiirkaardil nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="6c326-191">On the Versions FastTab, click Run.</span></span>  
17. <span data-ttu-id="6c326-192">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="6c326-192">Click OK.</span></span>
    * <span data-ttu-id="6c326-193">Vaadake toodangu, mis sisaldab kasutaja, kes töötab sellele vormingu konfiguratsioonile loginud ettevõtte nimi.</span><span class="sxs-lookup"><span data-stu-id="6c326-193">Review the output that contains the name of the company in which the user who is running this format configuration is logged into.</span></span> <span data-ttu-id="6c326-194">Pange tähele, et see vormingukonfiguratsioon kasutab loodud mudelivastenduskonfiguratsiooni, kuna see on ainus saadaolev konfiguratsioon, mis sisaldab nõutavaid mudelivastendusi.</span><span class="sxs-lookup"><span data-stu-id="6c326-194">Note that the created model mapping configuration is used by this format configuration because there is only one configuration available that contains required model mappings.</span></span>   

## <a name="add-alternative-er-model-mapping-configuration"></a><span data-ttu-id="6c326-195">Alternatiivse elektroonilise aruandluse mudelivastenduse konfiguratsiooni lisamine</span><span class="sxs-lookup"><span data-stu-id="6c326-195">Add alternative ER model mapping configuration</span></span>
1. <span data-ttu-id="6c326-196">Tehke puul valik „Sample data model".</span><span class="sxs-lookup"><span data-stu-id="6c326-196">In the tree, select 'Sample data model'.</span></span>
2. <span data-ttu-id="6c326-197">Klõpsake valikut Loo konfiguratsioon, et avada rippdialoog.</span><span class="sxs-lookup"><span data-stu-id="6c326-197">Click Create configuration to open the drop dialog.</span></span>
3. <span data-ttu-id="6c326-198">Sisestage väljale Uus suvand "Andmemudelil Näidisandmemudel põhinev mudelivastendus".</span><span class="sxs-lookup"><span data-stu-id="6c326-198">In the New field, enter 'Model Mapping based on data model Sample data model'.</span></span>
4. <span data-ttu-id="6c326-199">Sisestage nimeväljale tekst „Sample mapping (alternative)".</span><span class="sxs-lookup"><span data-stu-id="6c326-199">In the Name field, type 'Sample mapping (alternative)'.</span></span>
    * <span data-ttu-id="6c326-200">Näidise vastendamine (alternatiivne)</span><span class="sxs-lookup"><span data-stu-id="6c326-200">Sample mapping (alternative)</span></span>  
5. <span data-ttu-id="6c326-201">Klõpsake Loo konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="6c326-201">Click Create configuration.</span></span>
6. <span data-ttu-id="6c326-202">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="6c326-202">Click Designer.</span></span>
7. <span data-ttu-id="6c326-203">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="6c326-203">Click Designer.</span></span>
8. <span data-ttu-id="6c326-204">Valige puul väärtus Dynamics 365 for Operations \ Tabel.</span><span class="sxs-lookup"><span data-stu-id="6c326-204">In the tree, select 'Dynamics 365 for Operations\Table'.</span></span>
9. <span data-ttu-id="6c326-205">Klõpsake suvandit Juure lisamine.</span><span class="sxs-lookup"><span data-stu-id="6c326-205">Click Add root.</span></span>
10. <span data-ttu-id="6c326-206">Sisestage väljale Nimi suvand Ettevõte.</span><span class="sxs-lookup"><span data-stu-id="6c326-206">In the Name field, type 'Company'.</span></span>
    * <span data-ttu-id="6c326-207">Ettevõte</span><span class="sxs-lookup"><span data-stu-id="6c326-207">Company</span></span>  
11. <span data-ttu-id="6c326-208">Sisestage väljale Tabel suvand CompanyInfo.</span><span class="sxs-lookup"><span data-stu-id="6c326-208">In the Table field, type 'CompanyInfo'.</span></span>
    * <span data-ttu-id="6c326-209">CompanyInfo</span><span class="sxs-lookup"><span data-stu-id="6c326-209">CompanyInfo</span></span>  
12. <span data-ttu-id="6c326-210">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="6c326-210">Click OK.</span></span>
13. <span data-ttu-id="6c326-211">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="6c326-211">Click Edit.</span></span>
14. <span data-ttu-id="6c326-212">Valige puul suvand String\ÜHENDA.</span><span class="sxs-lookup"><span data-stu-id="6c326-212">In the tree, select 'String\CONCATENATE'.</span></span>
15. <span data-ttu-id="6c326-213">Klõpsake suvandit Funktsiooni lisamine.</span><span class="sxs-lookup"><span data-stu-id="6c326-213">Click Add function.</span></span>
16. <span data-ttu-id="6c326-214">Laiendage puul väärtust "Company".</span><span class="sxs-lookup"><span data-stu-id="6c326-214">In the tree, expand 'Company'.</span></span>
17. <span data-ttu-id="6c326-215">Laiendage puul valikut „Company\find()“.</span><span class="sxs-lookup"><span data-stu-id="6c326-215">In the tree, expand 'Company\find()'.</span></span>
18. <span data-ttu-id="6c326-216">Tehke puul valik „Company\find()\Name".</span><span class="sxs-lookup"><span data-stu-id="6c326-216">In the tree, select 'Company\find()\Name'.</span></span>
19. <span data-ttu-id="6c326-217">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="6c326-217">Click Add data source.</span></span>
20. <span data-ttu-id="6c326-218">Sisestage väärtus väljale Valem.</span><span class="sxs-lookup"><span data-stu-id="6c326-218">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="6c326-219">CONCATENATE(Company.'find()'.Name, ";",</span><span class="sxs-lookup"><span data-stu-id="6c326-219">CONCATENATE(Company.'find()'.Name, ";",</span></span>  
21. <span data-ttu-id="6c326-220">Tehke puul valik „Company\find()\Company(DataArea)".</span><span class="sxs-lookup"><span data-stu-id="6c326-220">In the tree, select 'Company\find()\Company(DataArea)'.</span></span>
22. <span data-ttu-id="6c326-221">Klõpsake suvandit Andmeallika lisamine.</span><span class="sxs-lookup"><span data-stu-id="6c326-221">Click Add data source.</span></span>
23. <span data-ttu-id="6c326-222">Sisestage väärtus väljale Valem.</span><span class="sxs-lookup"><span data-stu-id="6c326-222">In the Formula field, type a value.</span></span>
    * <span data-ttu-id="6c326-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span><span class="sxs-lookup"><span data-stu-id="6c326-223">CONCATENATE(Company.'find()'.Name, ";", Company.'find()'.DataArea)</span></span>  
24. <span data-ttu-id="6c326-224">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6c326-224">Click Save.</span></span>
25. <span data-ttu-id="6c326-225">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6c326-225">Close the page.</span></span>
26. <span data-ttu-id="6c326-226">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6c326-226">Click Save.</span></span>
27. <span data-ttu-id="6c326-227">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6c326-227">Close the page.</span></span>
28. <span data-ttu-id="6c326-228">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6c326-228">Close the page.</span></span>
29. <span data-ttu-id="6c326-229">Tehke väljal Käivita mustand valik Jah.</span><span class="sxs-lookup"><span data-stu-id="6c326-229">Select Yes in the Run Draft field.</span></span>

## <a name="use-an-existing-er-model-mapping-configuration"></a><span data-ttu-id="6c326-230">Olemasoleva elektroonilise aruandluse mudelivastenduse konfiguratsiooni kasutamine</span><span class="sxs-lookup"><span data-stu-id="6c326-230">Use an existing ER model mapping configuration</span></span>
1. <span data-ttu-id="6c326-231">Tehke puul valik „Näidisandmemudel\Näidisformaat".</span><span class="sxs-lookup"><span data-stu-id="6c326-231">In the tree, select 'Sample data model\Sample format'.</span></span>
2. <span data-ttu-id="6c326-232">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="6c326-232">Click Run.</span></span>
    * <span data-ttu-id="6c326-233">Pange tähele, et valitud ER-vormingu konfiguratsiooni mustandiversiooni ei saa käivitada, kuna määratlemata andmemudeli jaoks, mis on valitud käivitatud ER-vormingu andmeallikana, sisaldab mitut mudelivastenduse konfiguratsiooni.</span><span class="sxs-lookup"><span data-stu-id="6c326-233">Note that the selected draft version of the ER format configuration can't be executed because there is more than one model mapping configuration available for the undefined data model that has been selected as the data source of the running ER format.</span></span>   
    * <span data-ttu-id="6c326-234">Seejärel määratlege alternatiivne mudelivastenduskonfiguratsioon sellena, millest mudelivastendusi kasutatakse andmeallikana käivitatud ER-vormingu jaoks.</span><span class="sxs-lookup"><span data-stu-id="6c326-234">Next, you will define the alternative model mapping configuration as the one from which model mappings will be used as data sources for running ER format.</span></span>   
3. <span data-ttu-id="6c326-235">Tehke puul valik „Näidisandmemudel\Näidisvastendamine (alternatiivne)".</span><span class="sxs-lookup"><span data-stu-id="6c326-235">In the tree, select 'Sample data model\Sample mapping (alternative)'.</span></span>
4. <span data-ttu-id="6c326-236">Väljal Mudelivastenduse vaikeväärtus valige Jah.</span><span class="sxs-lookup"><span data-stu-id="6c326-236">Select Yes in the Default for model mapping field.</span></span>
5. <span data-ttu-id="6c326-237">Tehke puul valik „Näidisandmemudel\Näidisformaat".</span><span class="sxs-lookup"><span data-stu-id="6c326-237">In the tree, select 'Sample data model\Sample format'.</span></span>
6. <span data-ttu-id="6c326-238">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="6c326-238">Click Run.</span></span>
7. <span data-ttu-id="6c326-239">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="6c326-239">Click OK.</span></span>
    * <span data-ttu-id="6c326-240">Pange tähele, et mudelivastenduse vaikekonfiguratsiooni kasutab see vormingukonfiguratsioon elektroonilise dokumendi genereerimiseks (loodud väljund sisaldab ettevõtte koodi).</span><span class="sxs-lookup"><span data-stu-id="6c326-240">Note that the default model mapping configuration is used by this format configuration for generating the electronic document (the created output contains the company code).</span></span>  

