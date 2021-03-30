---
title: Lao seadistamine lao konfiguratsioonimalli abil
description: Selles teemas selgitatakse, kuidas seadistada ladu lao konfiguratsioonimalli abil.
author: perlynne
manager: tfehr
ms.date: 11/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DataManagementWorkspace, DMFQuickImportExportEnhanced, DMFDefinitionGroupTemplate, DMFEntityTemplateDefinitionLoadDialog
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 7bf69ccec59f2c540d71d44347bd99dc2378dc4c
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5224974"
---
# <a name="set-up-a-warehouse-by-using-a-warehouse-configuration-template"></a><span data-ttu-id="0b363-103">Lao seadistamine lao konfiguratsioonimalli abil</span><span class="sxs-lookup"><span data-stu-id="0b363-103">Set up a warehouse by using a warehouse configuration template</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0b363-104">Selles teemas selgitatakse, kuidas seadistada ladu lao konfiguratsioonimalli abil.</span><span class="sxs-lookup"><span data-stu-id="0b363-104">This topic explains how to set up a warehouse by using a warehouse configuration template.</span></span> <span data-ttu-id="0b363-105">Saate kasutada mitut eelmääratud konfiguratsioonimalli.</span><span class="sxs-lookup"><span data-stu-id="0b363-105">There are several predefined configuration templates that you can use.</span></span> <span data-ttu-id="0b363-106">Teavet nende mallide kasutamise kohta leiate teemast [„Konfigureerimisandmete mallid”](../../dev-itpro/data-entities/configuration-data-templates.md).</span><span class="sxs-lookup"><span data-stu-id="0b363-106">For information about how to use these templates, see [Configuration data templates](../../dev-itpro/data-entities/configuration-data-templates.md).</span></span>

## <a name="scenarios-where-configuration-templates-can-be-helpful"></a><span data-ttu-id="0b363-107">Stsenaariumid, mille puhul konfiguratsioonimallid võivad kasulikud olla</span><span class="sxs-lookup"><span data-stu-id="0b363-107">Scenarios where configuration templates can be helpful</span></span>

<span data-ttu-id="0b363-108">Konfiguratsioonimallid võivad kasulikud olla mitme stsenaariumi puhul.</span><span class="sxs-lookup"><span data-stu-id="0b363-108">Configuration templates can be helpful in many scenarios.</span></span> <span data-ttu-id="0b363-109">Järgmisena on toodud mõned näited.</span><span class="sxs-lookup"><span data-stu-id="0b363-109">Here are some examples:</span></span>

- <span data-ttu-id="0b363-110">Olete konfiguratsiooni seadistamise lõpetanud ja seda testimiskeskkonnas testinud ning soovite nüüd seadistuse tootmiskeskkonda kopeerida.</span><span class="sxs-lookup"><span data-stu-id="0b363-110">You've completed and tested a configuration setup in a test environment, and you now want to copy the setup to a production environment.</span></span>
- <span data-ttu-id="0b363-111">Soovite lao seadistuse mitmele juriidilisele isikule üle kanda või luua samale juriidilisele isikule uue lao.</span><span class="sxs-lookup"><span data-stu-id="0b363-111">You want to roll the warehouse setup out to several legal entities or create a new warehouse in the same legal entity.</span></span>
- <span data-ttu-id="0b363-112">Soovite kiiresti ette valmistada lao funktsioonide demo.</span><span class="sxs-lookup"><span data-stu-id="0b363-112">You want to quickly prepare for a demo of the warehouse functionality.</span></span>
- <span data-ttu-id="0b363-113">Soovite olemasolevate kaupade ja ladude puhul varude halduse funktsionaalsuse asemel kasutada laohalduse funktsionaalsust.</span><span class="sxs-lookup"><span data-stu-id="0b363-113">You want existing items and warehouses to use the functionality in Warehouse management instead of the functionality in Inventory management.</span></span>

<span data-ttu-id="0b363-114">Selles teemas käsitletakse esimest neist stsenaariumidest.</span><span class="sxs-lookup"><span data-stu-id="0b363-114">This topic focuses on the first of these scenarios.</span></span> <span data-ttu-id="0b363-115">See näitab, kuidas konfiguratsioonimalli abil konfiguratsiooni seadistust testimiskeskkonnast tootmiskeskkonda kopeerida.</span><span class="sxs-lookup"><span data-stu-id="0b363-115">It shows how you can use a configuration template to copy a configuration setup from a test environment to a production environment.</span></span>

## <a name="copy-a-configuration-setup-from-a-test-environment-to-a-production-environment"></a><span data-ttu-id="0b363-116">Konfiguratsiooni seadistuse kopeerimine testimiskeskkonnast tootmiskeskkonda</span><span class="sxs-lookup"><span data-stu-id="0b363-116">Copy a configuration setup from a test environment to a production environment</span></span>

<span data-ttu-id="0b363-117">Selle stsenaariumi puhul on testimiskeskkonnas juba olemas lao ja mõne kande protsessi konfiguratsiooni seadistus.</span><span class="sxs-lookup"><span data-stu-id="0b363-117">For this scenario, the configuration setup for a warehouse and some transaction processes already exist in a test environment.</span></span> <span data-ttu-id="0b363-118">Nüüd soovite laohoone konfiguratsiooni seadistuse testimiskeskkonnast tootmiskeskkonda kopeerida.</span><span class="sxs-lookup"><span data-stu-id="0b363-118">You now want to copy the configuration setup for the warehouse from the test environment to a production environment.</span></span>

> [!NOTE]
> <span data-ttu-id="0b363-119">Konfiguratsiooni seadistuse kopeerimisel on oluline kaasata muud seotud seadistuse andmed.</span><span class="sxs-lookup"><span data-stu-id="0b363-119">It's important that you include other related setup data when you copy a configuration setup.</span></span> <span data-ttu-id="0b363-120">Näiteks soovite testimiskeskkonnast seadistust kopeerides tooted seadistada.</span><span class="sxs-lookup"><span data-stu-id="0b363-120">For example, you want to set up products by copying the setup from a test environment.</span></span> <span data-ttu-id="0b363-121">Siiski ei saa toote fikseeritud komplekteerimiskohta enne toote loomist seadistada.</span><span class="sxs-lookup"><span data-stu-id="0b363-121">However, you can't set up a fixed picking location for a product before that product is created.</span></span> <span data-ttu-id="0b363-122">Kuigi üksikud konfiguratsioonimallid ei toeta seda tüüpi sõltuvust, on olemas seda toetavaid vaikeandmemalle.</span><span class="sxs-lookup"><span data-stu-id="0b363-122">Although individual configuration templates don't support this type of dependency, there are default data templates that support it.</span></span> <span data-ttu-id="0b363-123">Saate need vaikeandmemallid hõlpsalt konfiguratsiooni protsessi kaasata.</span><span class="sxs-lookup"><span data-stu-id="0b363-123">You can easily include these default data templates in a configuration process.</span></span>

### <a name="export-a-default-warehouse-template"></a><span data-ttu-id="0b363-124">Lao vaikemalli eksportimine</span><span class="sxs-lookup"><span data-stu-id="0b363-124">Export a default warehouse template</span></span> 

1. <span data-ttu-id="0b363-125">Avage tööruum **Andmehaldus**.</span><span class="sxs-lookup"><span data-stu-id="0b363-125">Open the **Data management** workspace.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0b363-126">Kui kasutate seda tööruumi esimest korda, tuleb teil jätkamiseks kõik andmeüksused laadida.</span><span class="sxs-lookup"><span data-stu-id="0b363-126">If you're using this workspace for the first time, you must load all the data entities before you continue.</span></span>

2. <span data-ttu-id="0b363-127">Vaikemallide laadimiseks valige paan **Mallid** ja seejärel **Vaikemallide laadimine**.</span><span class="sxs-lookup"><span data-stu-id="0b363-127">Select the **Templates** tile, and then select **Load default templates** to load the default templates.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0b363-128">Valik **Vaikemallide laadimine** on saadaval ainult **täiustatud** vaates.</span><span class="sxs-lookup"><span data-stu-id="0b363-128">**Load default templates** is available only in the **Enhanced** view.</span></span> <span data-ttu-id="0b363-129">Valige **Raamistiku parameetrid** ja seejärel väli **Vaikeväärtuste kuvamine** ning tehke seal valik **Täiustatud vaade**.</span><span class="sxs-lookup"><span data-stu-id="0b363-129">Select **Framework parameters**, and then, in the **View defaults** field, select **Enhanced view**.</span></span>

3. <span data-ttu-id="0b363-130">Vaikemallide laadimise järel saate neid oma äri vajaduste kohaselt muuta.</span><span class="sxs-lookup"><span data-stu-id="0b363-130">After the default templates are loaded, you can change them so that they meet your business requirements.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0b363-131">Vaikemallide laadimiseks ja mallide importimiseks peab teil olema süsteemiadministraatori juurdepääs.</span><span class="sxs-lookup"><span data-stu-id="0b363-131">To load default templates and import templates, you must have system administrator access.</span></span> <span data-ttu-id="0b363-132">See nõue aitab tagada kõikide üksuste korrektse malli laadimise.</span><span class="sxs-lookup"><span data-stu-id="0b363-132">This requirement helps guarantee that all entities are correctly loaded into the template.</span></span>

4. <span data-ttu-id="0b363-133">Veenduge, et oleksite selle juriidilise isiku kontol, millele soovite ettevõttekohaseid andmeid eksportida.</span><span class="sxs-lookup"><span data-stu-id="0b363-133">Make sure that you're in the legal entity that you want to export the company-specific data from.</span></span>
5. <span data-ttu-id="0b363-134">Valige tööruumis käsk **Ekspordi**.</span><span class="sxs-lookup"><span data-stu-id="0b363-134">In the workspace, select **Export**.</span></span>
6. <span data-ttu-id="0b363-135">Looge uus eksportimisprojekt.</span><span class="sxs-lookup"><span data-stu-id="0b363-135">Create a new export project.</span></span>
7. <span data-ttu-id="0b363-136">Valige **+ malli lisamine** ja leidke lao vaikemall **400 - WMS**.</span><span class="sxs-lookup"><span data-stu-id="0b363-136">Select **+ Add template**, and find the **400 - WMS** default warehouse template.</span></span> <span data-ttu-id="0b363-137">See mall lisab andmeüksused lao konfiguratsiooni.</span><span class="sxs-lookup"><span data-stu-id="0b363-137">This template adds data entities for warehouse configuration.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0b363-138">Kui eksporditavaid andmeid tuleb filtrida (nt soovite eksportida ainult kindla laoga seotud andmeid), peate igat andmeüksust hindama ja lisama filtrimise päringu kaudu.</span><span class="sxs-lookup"><span data-stu-id="0b363-138">If the data that you're exporting must be filtered (for example, you want to export only the data that is related to a specific warehouse), you must evaluate each data entity and add filtering via a query.</span></span> <span data-ttu-id="0b363-139">Teise võimalusena võite eksportida kõik andmed ja seejärel kustutada kirjed, mida pole sihtfailides vaja.</span><span class="sxs-lookup"><span data-stu-id="0b363-139">Alternatively, you can export all data and then delete the records that aren't required in the destination files.</span></span>

8. <span data-ttu-id="0b363-140">Valige **Ekspordi**.</span><span class="sxs-lookup"><span data-stu-id="0b363-140">Select **Export**.</span></span> <span data-ttu-id="0b363-141">Eksporditakse kõik projekti andmeüksustega seotud andmed.</span><span class="sxs-lookup"><span data-stu-id="0b363-141">Data that is related to all the data entities in the project is exported.</span></span>

<span data-ttu-id="0b363-142">Teil on võimalik andmed ZIP-failina alla laadida.</span><span class="sxs-lookup"><span data-stu-id="0b363-142">You can download a zip file for the data package.</span></span> <span data-ttu-id="0b363-143">See fail sisaldab kõiki valitud vormingus andmeid (nt Exceli vormingus).</span><span class="sxs-lookup"><span data-stu-id="0b363-143">This file contains all the data in the selected format (for example, Excel format).</span></span> <span data-ttu-id="0b363-144">Nagu öeldud, tuleb võib-olla mõnda kirjet andmefailides enne tootmiskeskkonda importimist värskendada.</span><span class="sxs-lookup"><span data-stu-id="0b363-144">As has been mentioned, some records in the data package files might have to be updated before you can import them into the production environment.</span></span> <span data-ttu-id="0b363-145">Kirje värskendamisel veenduge, et te ei muudaks faili nime.</span><span class="sxs-lookup"><span data-stu-id="0b363-145">If you update a record, make sure that you don't change the file name.</span></span>

### <a name="import-a-warehouse-configuration-setup"></a><span data-ttu-id="0b363-146">Lao konfiguratsiooni seadistuse importimine</span><span class="sxs-lookup"><span data-stu-id="0b363-146">Import a warehouse configuration setup</span></span>

1. <span data-ttu-id="0b363-147">Veenduge sihtkeskkonnas, et oleksite selle ettevõtte kontol, kuhu soovite laoandmed importida.</span><span class="sxs-lookup"><span data-stu-id="0b363-147">In the destination environment, make sure that you're in the company that you want to import the warehouse data into.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0b363-148">Enne importimist peaksite tuvastama andmete vahelised sõltuvused.</span><span class="sxs-lookup"><span data-stu-id="0b363-148">Before you do the import, you should identify any data dependencies.</span></span> <span data-ttu-id="0b363-149">Näiteks sisaldab mall **Laohaldus** andmeüksust nimega **Lao likvideerimiskoodid**.</span><span class="sxs-lookup"><span data-stu-id="0b363-149">For example, the **Warehouse management** template includes a data entity that is named **Warehouse disposition codes**.</span></span> <span data-ttu-id="0b363-150">See üksus sisaldab andmeid, mis on seotud seadistuslehega **Likvideerimiskoodid** (**Laohaldus** > **Seadistamine** > **Mobiilne seade** > **Likvideerimiskoodid**).</span><span class="sxs-lookup"><span data-stu-id="0b363-150">This entity contains data that is related to the **Disposition codes** setup page (**Warehouse management** > **Setup** > **Mobile device** > **Disposition codes**).</span></span> <span data-ttu-id="0b363-151">Kui olemasolev seadistus tegeleb juba müügitellimuste tagastusprotsessiga, sisaldab väli **Tagastamise likvideerimiskood** väärtust.</span><span class="sxs-lookup"><span data-stu-id="0b363-151">If an existing setup already handles the return process for sales orders, the **Return disposition code** field contains a value.</span></span> <span data-ttu-id="0b363-152">Selle välja likvideerimiskood on seotud andmeüksusega **Likvideerimiskood**, mis kuulub malli **Müük ja turundus**.</span><span class="sxs-lookup"><span data-stu-id="0b363-152">The disposition code in this field is related to the **Disposition code** data entity, which is part of the **Sales and marketing** template.</span></span> <span data-ttu-id="0b363-153">Kui andmeüksuse **Likvideerimiskood** andmeid ei impordita enne väljalt **Lao likvideerimiskoodid** andmete importimist, siis importimine nurjub.</span><span class="sxs-lookup"><span data-stu-id="0b363-153">If the data from the **Disposition code** data entity isn't imported before the data from the **Warehouse disposition codes** field, the import will fail.</span></span>

2. <span data-ttu-id="0b363-154">Valige tööruumis **Andmehaldus** käsk **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="0b363-154">In the **Data management** workspace, select **Import**.</span></span>
3. <span data-ttu-id="0b363-155">Looge uus importimisprojekt.</span><span class="sxs-lookup"><span data-stu-id="0b363-155">Create a new import project.</span></span>
4. <span data-ttu-id="0b363-156">Valige **+ lisa fail** ja laadige andmed üles ZIP-failina.</span><span class="sxs-lookup"><span data-stu-id="0b363-156">Select **+ Add file**, and upload the zip file for the data package.</span></span>
5. <span data-ttu-id="0b363-157">Valige **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="0b363-157">Select **Import**.</span></span> <span data-ttu-id="0b363-158">**Täiustatud** vaates saate importimisel tekkida võivatest probleemidest kiiresti ülevaate, kui kasutate suvandit **Filtreeri**.</span><span class="sxs-lookup"><span data-stu-id="0b363-158">In the **Enhanced** view, you can use the **Filter** option to quickly get an overview of issues that might occur during the import.</span></span>

<span data-ttu-id="0b363-159">Käsk **Kuva käivituslogi** annab üksikasjaliku teabe iga imporditud andmeüksuse kohta.</span><span class="sxs-lookup"><span data-stu-id="0b363-159">The **View execution** log provides detailed information about each data entity that is imported.</span></span> <span data-ttu-id="0b363-160">Kiirelt sihtandmete juurde jõudmiseks saate kasutada andmete ajastamise vaadet.</span><span class="sxs-lookup"><span data-stu-id="0b363-160">You can use the staging data view to quickly get to the target data.</span></span> <span data-ttu-id="0b363-161">Sel viisil näete, kuidas imporditud andmed rakenduse seotud lehekülgedel välja näevad.</span><span class="sxs-lookup"><span data-stu-id="0b363-161">In this way, you can see what the imported data looks like on the related pages in the application.</span></span> <span data-ttu-id="0b363-162">Vaikeandmemallide kasutamisel töötab importimise järjestus iga andmeüksuse puhul eelmääratud viisil, tagamaks, et sõltuvad andmed imporditakse esimesena.</span><span class="sxs-lookup"><span data-stu-id="0b363-162">When you use the default data templates, the import sequence for each data entity works in the predefined manner, to help guarantee that all dependent data is imported first.</span></span> <span data-ttu-id="0b363-163">Kui projekti kuuluvad kohandatud andmeüksused, peate veenduma, et õige järjekord oleks määratud.</span><span class="sxs-lookup"><span data-stu-id="0b363-163">If custom data entities are part of the project, you must make sure that the correct sequence is defined.</span></span> <span data-ttu-id="0b363-164">Lisateavet vaadake teemast [„Konfigureerimisandmete mallid”](../../dev-itpro/data-entities/configuration-data-templates.md).</span><span class="sxs-lookup"><span data-stu-id="0b363-164">For more information, see [Configuration data templates](../../dev-itpro/data-entities/configuration-data-templates.md).</span></span>

<span data-ttu-id="0b363-165">Rohkem teavet selle kohta, kuidas kasutada laomalli, et kopeerida lao konfiguratsiooni ühest ettevõttest sama eksemplari uude ettevõttesse, leiate järgmisest 3-minutilisest YouTube’i videost: [Laomalli kasutamine konfiguratsiooni kopeerimiseks rakenduse Finance and Operations](https://www.youtube.com/watch?v=K2WIfFlqJYs) jaoks.</span><span class="sxs-lookup"><span data-stu-id="0b363-165">To learn more about how to use warehouse template to copy the configuration of a warehouse from one company to a new company within the same instance, see this 3-minute video on YouTube about [how to use warehouse template to copy the configuration for Finance and Operations](https://www.youtube.com/watch?v=K2WIfFlqJYs).</span></span>

## <a name="related-topic"></a><span data-ttu-id="0b363-166">Seotud teema</span><span class="sxs-lookup"><span data-stu-id="0b363-166">Related topic</span></span>

[<span data-ttu-id="0b363-167">Konfigureerimisandmete mallid</span><span class="sxs-lookup"><span data-stu-id="0b363-167">Configuration data templates</span></span>](../../dev-itpro/data-entities/configuration-data-templates.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]