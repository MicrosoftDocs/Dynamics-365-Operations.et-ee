---
title: Juurdepääs rakenduse metaandmetele ühendatud rakenduste abil
description: Selle teema sammud selgitavad, kuidas Regulatory configuration service (RCS) kasutaja saab kujundada uut elektroonilise aruandluse (ER) mudeli kaardistamise, kasutades metaandmeid Finance and Operations.
author: NickSelin
manager: AnnBe
ms.date: 06/29/2019
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
ms.openlocfilehash: 5020b523ca5d76d36f7436a8f43e8629c029e3e8
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2769874"
---
# <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="4974f-103">Juurdepääs rakenduse metaandmetele ühendatud rakenduste abil</span><span class="sxs-lookup"><span data-stu-id="4974f-103">Access application metadata by using connected applications</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4974f-104">Järgmised etapid selgitavad, kuidas süsteemi administraatori või elektroonilise aruandluse arendaja rolliga lahenduse Regulatory Configuration Service (RCS) kasutaja saab kavandada uue elektroonilise aruandluse (ER) mudelivastenduse kasutades Finance and Operationsi metaandmeid.</span><span class="sxs-lookup"><span data-stu-id="4974f-104">The following steps explain how a Regulatory configuration service (RCS) user in the System Administrator or Electronic Reporting Developer role can design a new Electronic reporting (ER) model mapping by using metadata in Finance and Operations.</span></span> <span data-ttu-id="4974f-105">Rakenduse metaandmete saab online-juurdepääsu RCS-ga ühendatud rakenduse abil.</span><span class="sxs-lookup"><span data-stu-id="4974f-105">Application metadata will be accessed online by using the RCS connected application.</span></span> <span data-ttu-id="4974f-106">Väliskaubanduse kannetele juurdepääsuks konfigureeritakse elektroonilise aruandluse mudeli vastenduse näidis.</span><span class="sxs-lookup"><span data-stu-id="4974f-106">Sample ER model mapping will be configured to access foreign trade transactions.</span></span> <span data-ttu-id="4974f-107">Nende etappide lõpuleviimiseks peate esmalt RCSis viima lõpule etapid teemas [Konfiguratsiooniteenuse pakkujate loomine ja nende aktiivseks märkimine](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="4974f-107">To complete these steps, in RCS you must first complete the steps in the topic, [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="4974f-108">Kui te ei ole viinude lõpule etappe teemas [Juurdepääs rakenduse metaandmetele ER-konfiguratsiooni abil](access-application-metadata-er-configuration.md), avage [Elektroonilise aruandluse näidiste leht](https://go.microsoft.com/fwlink/?linkid=862266), et laadida alla ja salvestada järgmised elektroonilise aruandluse konfiguratsioonid: Väliskaubanduse metaandmed.xml; Väliskaubanduse mudel.xml; Väliskaubanduse vastendamine.xml, ja seejärel viige protseduuri etapid lõpuni.</span><span class="sxs-lookup"><span data-stu-id="4974f-108">If you have not completed the steps in the topic, [Access application metadata by using ER configuration](access-application-metadata-er-configuration.md), go to the [Electronic reporting examples page](https://go.microsoft.com/fwlink/?linkid=862266) to download and save the following ER configurations: Foreign trade metadata.xml; Foreign trade model.xml; Foreign trade mapping.xml, and then complete the steps in the procedure.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4974f-109">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="4974f-109">Prerequisites</span></span>
1. <span data-ttu-id="4974f-110">Avage **Kõik tööruumid** > **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="4974f-110">Go to **All workspaces** > **Electronic reporting**.</span></span> 
2. <span data-ttu-id="4974f-111">Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja märgitud kui **Aktiivne**.</span><span class="sxs-lookup"><span data-stu-id="4974f-111">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="4974f-112">Kui te ei näe seda konfiguratsioonipakkujat, peate esmalt läbima protseduuris [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](er-configuration-provider-mark-it-active-2016-11.md) toodud juhised.</span><span class="sxs-lookup"><span data-stu-id="4974f-112">If you don’t see this configuration provider, complete the steps in the procedure [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> 

## <a name="get-required-er-configurations"></a><span data-ttu-id="4974f-113">Vajalike elektroonilise aruandluse konfiguratsioonide hankimine</span><span class="sxs-lookup"><span data-stu-id="4974f-113">Get required ER configurations</span></span>
1. <span data-ttu-id="4974f-114">Klõpsake valikut **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="4974f-114">Click **Reporting configurations**.</span></span> 
2. <span data-ttu-id="4974f-115">Kui viisite need etapid juba protseduuris [Juurdepääs rakenduse metaandmetele ER-i konfiguratsiooni abil](access-application-metadata-er-configuration.md) lõpule, on teil juba kõik vajalikud ER-i konfiguratsioonid (väliskaubanduse metaandmed, mudel ja kaardistamise konfiguratsioonid) praeguses RCS-i eksemplaris olemas.</span><span class="sxs-lookup"><span data-stu-id="4974f-115">If you already completed the steps in the [Access application metadata by using ER configuration](access-application-metadata-er-configuration.md) procedure, you already have all necessary ER configurations (foreign trade metadata, model and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="4974f-116">Võite kõik selle alamülesande ülejäänud etapid vahele jätta.</span><span class="sxs-lookup"><span data-stu-id="4974f-116">You can skip all the remaining steps of this sub-task.</span></span> 
3. <span data-ttu-id="4974f-117">Klõpsake valikut **Vahetus**.</span><span class="sxs-lookup"><span data-stu-id="4974f-117">Click **Exchange**.</span></span> 
4. <span data-ttu-id="4974f-118">Klõpsake valikut **Laadi XML-failist**.</span><span class="sxs-lookup"><span data-stu-id="4974f-118">Click **Load from XML file**.</span></span> 
5. <span data-ttu-id="4974f-119">Klõpsake **Sirvi** ja valige fail **Väliskaubanduse metaandmed.xml**.</span><span class="sxs-lookup"><span data-stu-id="4974f-119">Click **Browse** and select the **Foreign trade metadata.xml** file.</span></span> 
6. <span data-ttu-id="4974f-120">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="4974f-120">Click **OK**.</span></span> 
7. <span data-ttu-id="4974f-121">Klõpsake valikut **Vahetus**.</span><span class="sxs-lookup"><span data-stu-id="4974f-121">Click **Exchange**.</span></span> 
8. <span data-ttu-id="4974f-122">Klõpsake valikut **Laadi XML-failist**.</span><span class="sxs-lookup"><span data-stu-id="4974f-122">Click **Load from XML file**.</span></span> 
9. <span data-ttu-id="4974f-123">Klõpsake **Sirvi** ja valige fail **Väliskaubanduse mudel.xml**.</span><span class="sxs-lookup"><span data-stu-id="4974f-123">Click **Browse** and select the **Foreign trade model.xml** file.</span></span> 
10. <span data-ttu-id="4974f-124">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="4974f-124">Click **OK**.</span></span> 
11. <span data-ttu-id="4974f-125">Klõpsake valikut **Vahetus**.</span><span class="sxs-lookup"><span data-stu-id="4974f-125">Click **Exchange**.</span></span> 
12. <span data-ttu-id="4974f-126">Klõpsake valikut **Laadi XML-failist**.</span><span class="sxs-lookup"><span data-stu-id="4974f-126">Click **Load from XML file**.</span></span> 
13. <span data-ttu-id="4974f-127">Klõpsake **Sirvi** ja valige fail **Väliskaubanduse vastendamine.xml**.</span><span class="sxs-lookup"><span data-stu-id="4974f-127">Click **Browse** and select the **Foreign trade mapping.xml** file.</span></span> 
14. <span data-ttu-id="4974f-128">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="4974f-128">Click **OK**.</span></span> 

## <a name="register-a-connected-application"></a><span data-ttu-id="4974f-129">Ühendatud rakenduse registreerimine</span><span class="sxs-lookup"><span data-stu-id="4974f-129">Register a connected application</span></span>
1. <span data-ttu-id="4974f-130">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="4974f-130">Close the page.</span></span> 
2. <span data-ttu-id="4974f-131">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="4974f-131">Close the page.</span></span> 
3. <span data-ttu-id="4974f-132">Avage **Kõik tööruumid** > **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="4974f-132">Go to **All workspaces** > **Electronic reporting**.</span></span> 
4. <span data-ttu-id="4974f-133">Klõpsake **Ühendatud rakendused**.</span><span class="sxs-lookup"><span data-stu-id="4974f-133">Click **Connected applications**.</span></span> 
5. <span data-ttu-id="4974f-134">Veenduge, et konfigureeritud rakendus on Azura põhine ja et see on praegusele RCS-i kasutajatele juurdepääsetav.</span><span class="sxs-lookup"><span data-stu-id="4974f-134">Make sure that the configured application is Azura based and accessible for the current RCS user.</span></span> <span data-ttu-id="4974f-135">Samuti on vajalik, et praegusel RCS-i kasutajal on juurdepääs valitud rakendusele ja ta on registreeritud selle rakenduse kasutajaks, kellel on roll, mis annab talle õigused rakenduse metaandmetele juurdepääsuks.</span><span class="sxs-lookup"><span data-stu-id="4974f-135">It is also required that the current RCS user has access to the selected application and has been registered as a user of this application playing a role giving him privileges to access application’s metadata.</span></span> 
6. <span data-ttu-id="4974f-136">Klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="4974f-136">Click **New**.</span></span> 
7. <span data-ttu-id="4974f-137">Trükkige "MyConnectedApp" väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="4974f-137">In the **Name** field, type 'MyConnectedApp'.</span></span> 
8. <span data-ttu-id="4974f-138">Trükkige väljale **Rakendus** suvand "https:// mycompany.operations.dynamics.com".</span><span class="sxs-lookup"><span data-stu-id="4974f-138">In the **Application** field, type 'https:// mycompany.operations.dynamics.com'.</span></span> 
9. <span data-ttu-id="4974f-139">Trükkige väljale **Rentnik** suvand "mycompany.onmicrosoft.com".</span><span class="sxs-lookup"><span data-stu-id="4974f-139">In the **Tenant** field, type ‘mycompany.onmicrosoft.com’.</span></span> 
10. <span data-ttu-id="4974f-140">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="4974f-140">Click **Save**.</span></span> 
11. <span data-ttu-id="4974f-141">Kui kontrollite konfigureeritud rakenduse ühendust, valige lehel **Ühenda kaugrakendusega** link **Klõpsake siin valitud kaugrakendusega ühendamiseks**.</span><span class="sxs-lookup"><span data-stu-id="4974f-141">When you check connection to configured application, on the **Connect to remote application** page click **Click here to connect to selected remote application** link.</span></span> 
12. <span data-ttu-id="4974f-142">Klõpsake nupul **Kontrolli ühendust**.</span><span class="sxs-lookup"><span data-stu-id="4974f-142">Click **Check connection**.</span></span> 
13. <span data-ttu-id="4974f-143">Klõpsake valikut **Sule**.</span><span class="sxs-lookup"><span data-stu-id="4974f-143">Click **Close**.</span></span> 
14. <span data-ttu-id="4974f-144">Pärast edukat ühenduse kontrollimist uuendatakse praeguses ruudustikus konfigureeritud rakenduse versioon ja rentniku andmed.</span><span class="sxs-lookup"><span data-stu-id="4974f-144">When the connection validation succeeded, version and tenant details will be updated for the configured application in the current grid.</span></span> 

## <a name="review-existing-model-mapping-configuration"></a><span data-ttu-id="4974f-145">Olemasoleva mudelivastenduse üle vaatamine</span><span class="sxs-lookup"><span data-stu-id="4974f-145">Review existing model mapping configuration</span></span>
1. <span data-ttu-id="4974f-146">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="4974f-146">Close the page.</span></span> 
2. <span data-ttu-id="4974f-147">Klõpsake valikut **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="4974f-147">Click **Reporting configurations**.</span></span> 
3. <span data-ttu-id="4974f-148">Laiendage puul valikut **Väliskaubanduse mudel**.</span><span class="sxs-lookup"><span data-stu-id="4974f-148">In the tree, expand **Foreign trade model**.</span></span> 
4. <span data-ttu-id="4974f-149">Valige puul väärtus **Väliskaubanduse mudel\Väliskaubanduse vastendamine**.</span><span class="sxs-lookup"><span data-stu-id="4974f-149">In the tree, select **Foreign trade model\Foreign trade mapping**.</span></span> 
5. <span data-ttu-id="4974f-150">Laiendage jaotist **Eeltingimused**.</span><span class="sxs-lookup"><span data-stu-id="4974f-150">Expand the **Prerequisites** section.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="4974f-151">Praegu viitab see vastendamine metaandmete konfiguratsioonile.</span><span class="sxs-lookup"><span data-stu-id="4974f-151">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="4974f-152">Selle konfiguratsiooni rakenduse metaandmeid pakutakse selle mudeli vastendamise kavandamise ajal.</span><span class="sxs-lookup"><span data-stu-id="4974f-152">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

6. <span data-ttu-id="4974f-153">Klõpsake valikut **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="4974f-153">Click **Designer**.</span></span> 
7. <span data-ttu-id="4974f-154">Klõpsake valikut **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="4974f-154">Click **Designer**.</span></span> 
8. <span data-ttu-id="4974f-155">Valige puul väärtus **Dynamics 365 for Operations\Tabeli kirjed**.</span><span class="sxs-lookup"><span data-stu-id="4974f-155">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
9. <span data-ttu-id="4974f-156">Klõpsake suvandil **Juure lisamine**.</span><span class="sxs-lookup"><span data-stu-id="4974f-156">Click **Add root**.</span></span> 
10. <span data-ttu-id="4974f-157">Sisestage või valige väärtus väljalt **Tabel**.</span><span class="sxs-lookup"><span data-stu-id="4974f-157">In the **Table** field, enter or select a value.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="4974f-158">Praegu viitab see vastendamine metaandmete konfiguratsioonile.</span><span class="sxs-lookup"><span data-stu-id="4974f-158">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="4974f-159">Selle konfiguratsiooni rakenduse metaandmeid pakutakse selle mudeli vastendamise kavandamise ajal.</span><span class="sxs-lookup"><span data-stu-id="4974f-159">Application metadata from this configuration will be offered while this model mapping will be designed.</span></span> 

11. <span data-ttu-id="4974f-160">Klõpsake **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="4974f-160">Click **Cancel**.</span></span> 
12. <span data-ttu-id="4974f-161">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="4974f-161">Close the page.</span></span> 
13. <span data-ttu-id="4974f-162">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="4974f-162">Close the page.</span></span> 

## <a name="assign-connected-application-to-model-mapping"></a><span data-ttu-id="4974f-163">Määrake ühendatud rakendus mudelivastendusele</span><span class="sxs-lookup"><span data-stu-id="4974f-163">Assign connected application to model mapping</span></span> 
1. <span data-ttu-id="4974f-164">Klõpsake valikut **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="4974f-164">Click **Edit**.</span></span> 
2. <span data-ttu-id="4974f-165">Valige rakendus **MyConnectedApp**.</span><span class="sxs-lookup"><span data-stu-id="4974f-165">Select **MyConnectedApp** application.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="4974f-166">Praegu viitab see vastendamine valitud ühendatud rakenduse metaandmetele.</span><span class="sxs-lookup"><span data-stu-id="4974f-166">Currently, this mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="4974f-167">Kui sama vastendamine viitab metaandmete konfiguratsioonile ja ühendatud rakendusele samaaegselt, kasutatakse ühendatud rakenduse metaandmeid.</span><span class="sxs-lookup"><span data-stu-id="4974f-167">When the same mapping refers to metadata configuration and connected application at the same time, metadata of the connected application will be used.</span></span> 

3. <span data-ttu-id="4974f-168">Klõpsake valikut **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="4974f-168">Click **Designer**.</span></span> 
4. <span data-ttu-id="4974f-169">Klõpsake valikut **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="4974f-169">Click **Designer**.</span></span> 
5. <span data-ttu-id="4974f-170">Valige puul väärtus **Dynamics 365 for Operations\Tabeli kirjed**.</span><span class="sxs-lookup"><span data-stu-id="4974f-170">In the tree, select **Dynamics 365 for Operations\Table records**.</span></span> 
6. <span data-ttu-id="4974f-171">Klõpsake suvandil **Juure lisamine**.</span><span class="sxs-lookup"><span data-stu-id="4974f-171">Click **Add root**.</span></span> 
7. <span data-ttu-id="4974f-172">Sisestage või valige väärtus väljalt **Tabel**.</span><span class="sxs-lookup"><span data-stu-id="4974f-172">In the **Table** field, enter or select a value.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="4974f-173">Praegu pakuti rohkem kui kahte rakenduse tabelit, sest see vastendamine kasutab kõiki sellele määratud ühendatud rakenduse metaandmeid.</span><span class="sxs-lookup"><span data-stu-id="4974f-173">More than two application tables were offered now as this mapping uses all the metadata of the connected application that has been assigned for it.</span></span> 

8. <span data-ttu-id="4974f-174">Klõpsake **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="4974f-174">Click **Cancel**.</span></span> 
9. <span data-ttu-id="4974f-175">Klõpsake valikut **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="4974f-175">Click **Validate**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="4974f-176">Oleme andmemudeli elemendid edukalt sidunud nende andmeallikate üksustega, mida on kirjeldatud kasutades sellele vastendusele määratud ühendatud rakenduse metaandmete üksikasju.</span><span class="sxs-lookup"><span data-stu-id="4974f-176">We successfully bound elements of data model with items of data sources that are described by using details of metadata of the connected application that has been assigned for this mapping.</span></span> 

10. <span data-ttu-id="4974f-177">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="4974f-177">Close the page.</span></span> 
11. <span data-ttu-id="4974f-178">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="4974f-178">Close the page.</span></span> 

<span data-ttu-id="4974f-179">Kui peate hindama seda mudeli vastendust, kasutades rakenduse teise versiooni metaandmeid, registreerige teine ühendatud rakendus, määrake see mudeli vastendamiseks ja kinnitage see uute metaandmetega.</span><span class="sxs-lookup"><span data-stu-id="4974f-179">When you need to evaluate this model mapping by using metadata of a different version application, register another connected application, assign it to this model mapping and validate it against new metadata.</span></span>
