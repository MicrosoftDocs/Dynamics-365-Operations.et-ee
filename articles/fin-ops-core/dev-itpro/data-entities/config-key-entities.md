---
title: Konfiguratsioonivõtmed ja andmeüksused
description: Selles teemas kirjeldatakse konfiguratsioonivõtmete ja andmeüksuste vahelist seost.
author: Sunil-Garg
manager: AnnBe
ms.date: 05/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application user
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 25341
ms.assetid: 8e214c95-616b-4ee1-b5a4-fa5ce5147f2c
ms.search.region: Global
ms.author: sunilg
ms.search.validFrom: 2018-01-01
ms.dyn365.ops.version: Platform update 13
ms.openlocfilehash: b951c1da298689ea82f8c0abb868bea7c8c22487
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182067"
---
# <a name="configuration-keys-and-data-entities"></a><span data-ttu-id="edb5e-103">Konfiguratsioonivõtmed ja andmeüksused</span><span class="sxs-lookup"><span data-stu-id="edb5e-103">Configuration keys and data entities</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="edb5e-104">Enne andmete importimiseks või eksportimiseks andmeüksuste kasutamist soovitame teil määratleda konfiguratsioonivõtmete mõju andmeteüksustele, mida plaanite kasutada.</span><span class="sxs-lookup"><span data-stu-id="edb5e-104">Before you use data entities to import or export data, we recommended that you first determine the impact of configuration keys on the data entities that you are planning to use.</span></span>

<span data-ttu-id="edb5e-105">Lisateabe saamiseks konfiguratsioonivõtmete kohta lugege teemat [Litsentsikoodide ja konfiguratsioonivõtmete aruanne](../sysadmin/license-codes-configuration-keys-report.md).</span><span class="sxs-lookup"><span data-stu-id="edb5e-105">To learn more about configuration keys, see the [License codes and configuration keys report](../sysadmin/license-codes-configuration-keys-report.md).</span></span>

### <a name="configuration-key-assignments"></a><span data-ttu-id="edb5e-106">Konfiguratsioonivõtmete määramine</span><span class="sxs-lookup"><span data-stu-id="edb5e-106">Configuration key assignments</span></span>
<span data-ttu-id="edb5e-107">Konfiguratsioonivõtmeid saab määrata ühele või kõigile järgmistele artefaktidele.</span><span class="sxs-lookup"><span data-stu-id="edb5e-107">Configuration keys can be assigned to one or all of the following artifacts.</span></span>

- <span data-ttu-id="edb5e-108">Andmeüksused</span><span class="sxs-lookup"><span data-stu-id="edb5e-108">Data entities</span></span>
- <span data-ttu-id="edb5e-109">Andmeallikatena kasutatavad tabelid</span><span class="sxs-lookup"><span data-stu-id="edb5e-109">Tables used as data sources</span></span>
- <span data-ttu-id="edb5e-110">Tabeli väljad</span><span class="sxs-lookup"><span data-stu-id="edb5e-110">Table fields</span></span>
- <span data-ttu-id="edb5e-111">Andmeüksuse väljad</span><span class="sxs-lookup"><span data-stu-id="edb5e-111">Data entity fields</span></span>

<span data-ttu-id="edb5e-112">Järgmises tabelis antakse ülevaade, kuidas objektile aluseks olevate eri artefaktide konfiguratsioonivõtme väärtused muudavad objekti eeldatavat käitumist.</span><span class="sxs-lookup"><span data-stu-id="edb5e-112">The following table summarizes how configuration key values on the different artifacts that underlie an object change the expected behavior of the object.</span></span>

| <span data-ttu-id="edb5e-113">Andmeüksuse konfiguratsioonivõtme säte</span><span class="sxs-lookup"><span data-stu-id="edb5e-113">Configuration key setting on data entity</span></span> | <span data-ttu-id="edb5e-114">Tabeli konfiguratsioonivõtme säte</span><span class="sxs-lookup"><span data-stu-id="edb5e-114">Configuration key setting on table</span></span> | <span data-ttu-id="edb5e-115">Tabeli välja konfiguratsioonivõtme säte</span><span class="sxs-lookup"><span data-stu-id="edb5e-115">Configuration key setting on table field</span></span> | <span data-ttu-id="edb5e-116">Andmeüksuse välja konfiguratsioonivõtme säte</span><span class="sxs-lookup"><span data-stu-id="edb5e-116">Configuration key on data entity field</span></span> | <span data-ttu-id="edb5e-117">Eeldatav käitumine</span><span class="sxs-lookup"><span data-stu-id="edb5e-117">Expected behavior</span></span> |
|-----------------------------------------|------------------------------------|------------------------------------------|----------------------------------------|------------------|
| <span data-ttu-id="edb5e-118">Keelatud</span><span class="sxs-lookup"><span data-stu-id="edb5e-118">Disabled</span></span>                                | <span data-ttu-id="edb5e-119">Pole hinnatud</span><span class="sxs-lookup"><span data-stu-id="edb5e-119">Not evaluated</span></span>                      | <span data-ttu-id="edb5e-120">Pole hinnatud</span><span class="sxs-lookup"><span data-stu-id="edb5e-120">Not evaluated</span></span>                            | <span data-ttu-id="edb5e-121">Pole hinnatud</span><span class="sxs-lookup"><span data-stu-id="edb5e-121">Not evaluated</span></span>                          | <span data-ttu-id="edb5e-122">Kui andmeüksuse konfiguratsioonivõti on keelatud, siis andmeüksus ei toimi.</span><span class="sxs-lookup"><span data-stu-id="edb5e-122">If the configuration key for the data entity is disabled, the data entity will not be functional.</span></span> <span data-ttu-id="edb5e-123">Pole vahet, kas aluseks olevate tabelite ja väljade konfiguratsioonivõtmed on lubatud või keelatud.</span><span class="sxs-lookup"><span data-stu-id="edb5e-123">It does not matter whether the configuration keys in the underlying tables and fields are enabled or disabled.</span></span> |
| <span data-ttu-id="edb5e-124">Lubatud</span><span class="sxs-lookup"><span data-stu-id="edb5e-124">Enabled</span></span>                                 | <span data-ttu-id="edb5e-125">Keelatud</span><span class="sxs-lookup"><span data-stu-id="edb5e-125">Disabled</span></span>                           | <span data-ttu-id="edb5e-126">Pole hinnatud</span><span class="sxs-lookup"><span data-stu-id="edb5e-126">Not evaluated</span></span>                            | <span data-ttu-id="edb5e-127">Pole hinnatud</span><span class="sxs-lookup"><span data-stu-id="edb5e-127">Not evaluated</span></span>                          | <span data-ttu-id="edb5e-128">Kui andmeüksuse konfiguratsioonivõti on lubatud, kontrollib andmehaldusraamistik iga aluseks oleva tabeli konfiguratsioonivõtit.</span><span class="sxs-lookup"><span data-stu-id="edb5e-128">If the configuration key for a data entity is enabled, the data management framework checks the configuration key on each of the underlying tables.</span></span> <span data-ttu-id="edb5e-129">Kui tabeli konfiguratsioonivõti on keelatud, ei saa seda tabelit andmeüksuses kasutada.</span><span class="sxs-lookup"><span data-stu-id="edb5e-129">If the configuration key for a table is disabled, that table will not be available in the data entity for functional use.</span></span> <span data-ttu-id="edb5e-130">Kui tabeli konfiguratsioonivõti on keelatud, ei hinnata tabeli ja andmeüksuse konfiguratsioonivõtme sätteid.</span><span class="sxs-lookup"><span data-stu-id="edb5e-130">If a table's configuration key is disabled, the table and data entity configuration key settings are not evaluated.</span></span> <span data-ttu-id="edb5e-131">Kui üksuse esmase tabeli konfiguratsioonivõti on keelatud, toimib süsteem nii, nagu üksuse konfiguratsioonivõti oleks keelatud.</span><span class="sxs-lookup"><span data-stu-id="edb5e-131">If the primary table in the entity has its configuration key disabled, then the system will act as though the entity's configuration key were disabled.</span></span> |
| <span data-ttu-id="edb5e-132">Lubatud</span><span class="sxs-lookup"><span data-stu-id="edb5e-132">Enabled</span></span>                                 | <span data-ttu-id="edb5e-133">Lubatud</span><span class="sxs-lookup"><span data-stu-id="edb5e-133">Enabled</span></span>                            | <span data-ttu-id="edb5e-134">Keelatud</span><span class="sxs-lookup"><span data-stu-id="edb5e-134">Disabled</span></span>                                 | <span data-ttu-id="edb5e-135">Pole hinnatud</span><span class="sxs-lookup"><span data-stu-id="edb5e-135">Not evaluated</span></span>                          | <span data-ttu-id="edb5e-136">Kui andmeüksuse konfiguratsioonivõti ja aluseks olevate tabelite konfiguratsioonivõtmed on lubatud, kontrollib andmehaldusraamistik tabelite väljade konfiguratsioonivõtit.</span><span class="sxs-lookup"><span data-stu-id="edb5e-136">If the configuration key for a data entity is enabled, and the underlying tables configuration keys are enabled, the data management framework will check the configuration key on of the fields in the tables.</span></span> <span data-ttu-id="edb5e-137">Kui välja konfiguratsioonivõti on keelatud, ei ole see väli andmeüksuses kasutamiseks saadaval isegi juhul, kui vastava andmeüksuse välja konfiguratsioonivõti on lubatud.</span><span class="sxs-lookup"><span data-stu-id="edb5e-137">If the configuration key for a field is disabled, that field will not be available in the data entity for functional use even if the corresponding data entity field has the configuration key enabled.</span></span> |
| <span data-ttu-id="edb5e-138">Lubatud</span><span class="sxs-lookup"><span data-stu-id="edb5e-138">Enabled</span></span>                                 | <span data-ttu-id="edb5e-139">Lubatud</span><span class="sxs-lookup"><span data-stu-id="edb5e-139">Enabled</span></span>                            | <span data-ttu-id="edb5e-140">Lubatud</span><span class="sxs-lookup"><span data-stu-id="edb5e-140">Enabled</span></span>                                  | <span data-ttu-id="edb5e-141">Keelatud</span><span class="sxs-lookup"><span data-stu-id="edb5e-141">Disabled</span></span>                               | <span data-ttu-id="edb5e-142">Kui konfiguratsioonivõti on lubatud kõigil muudel tasanditel, aga üksuse välja konfiguratsioonivõti ei ole lubatud, ei saa välja andmeüksuses kasutada.</span><span class="sxs-lookup"><span data-stu-id="edb5e-142">If the configuration key is enabled at all other levels, but the entity field configuration key is not enabled, then the field will not be available for use in the data entity.</span></span> |

> [!NOTE]
> <span data-ttu-id="edb5e-143">Kui üksusel andmeallikana teine üksus, rakendatakse ülal olevat semantikat rekursiivselt.</span><span class="sxs-lookup"><span data-stu-id="edb5e-143">If an entity has another entity as a data source then, the above semantics are applied in a recursive manner.</span></span>

### <a name="entity-list-refresh"></a><span data-ttu-id="edb5e-144">Üksuste loendi värskendamine</span><span class="sxs-lookup"><span data-stu-id="edb5e-144">Entity list refresh</span></span>
<span data-ttu-id="edb5e-145">Üksuse loendi värskendamisel loob andmehaldusraamistik konfiguratsioonivõtme metaandmed käitusajal kasutamiseks.</span><span class="sxs-lookup"><span data-stu-id="edb5e-145">When the entity list is refreshed, the data management framework builds the configuration key metadata for runtime use.</span></span> <span data-ttu-id="edb5e-146">Metaandmed luuakse ülalkirjeldatud loogikat kasutades.</span><span class="sxs-lookup"><span data-stu-id="edb5e-146">This metadata is built using the logic described above.</span></span> <span data-ttu-id="edb5e-147">Soovitame enne andmehaldusraamistikus tööde ja üksuste kasutamist tungivalt oodata üksuste loendi värskendamise lõpetamiseni.</span><span class="sxs-lookup"><span data-stu-id="edb5e-147">We strongly recommend that you wait for the entity list refresh to complete before using jobs and entities in the data management framework.</span></span> <span data-ttu-id="edb5e-148">Kui te ei oota, ei pruugi konfiguratsioonivõtme metaandmed olla ajakohastatud, mis võib põhjustada ootamatuid tulemusi.</span><span class="sxs-lookup"><span data-stu-id="edb5e-148">If you don't wait, the configuration key metadata may not be up to date and could result in unexpected outcomes.</span></span> <span data-ttu-id="edb5e-149">Üksuste loendi värskendamisel kuvatakse üksuste loendi lehel järgmine teade.</span><span class="sxs-lookup"><span data-stu-id="edb5e-149">When the entity list is being refreshed, the following message is shown in the entity list page.</span></span>

![Üksuste loendi värskendamine](./media/Entity_refresh_list.png)

### <a name="data-entity-list-page"></a><span data-ttu-id="edb5e-151">Andmeüksuste loendi leht</span><span class="sxs-lookup"><span data-stu-id="edb5e-151">Data entity list page</span></span>
<span data-ttu-id="edb5e-152">Andmeüksuste loendi leht tööruumis Andmehaldus näitab üksuste konfiguratsioonivõtme sätteid.</span><span class="sxs-lookup"><span data-stu-id="edb5e-152">The data entity list page in the Data management workspace shows the configuration key settings for the entities.</span></span> <span data-ttu-id="edb5e-153">Konfiguratsioonivõtmete mõju mõistmiseks andmeüksustele alustage sellelt lehelt.</span><span class="sxs-lookup"><span data-stu-id="edb5e-153">Start from this page to understand the impact from configuration keys on the data entity.</span></span>

<span data-ttu-id="edb5e-154">See teave kuvatakse üksuse värskendamise ajal loodud metaandmete abil.</span><span class="sxs-lookup"><span data-stu-id="edb5e-154">This information is shown using the metadata that is built during entity refresh.</span></span> <span data-ttu-id="edb5e-155">Konfiguratsioonivõtme veerus kuvatakse andmeüksusega seostatud konfiguratsioonivõtme nimi.</span><span class="sxs-lookup"><span data-stu-id="edb5e-155">The configuration key column shows the name of the configuration key that is associated with the data entity.</span></span> <span data-ttu-id="edb5e-156">Kui see veerg on tühi, tähendab see, on andmeüksusega pole konfiguratsioonivõtit seostatud.</span><span class="sxs-lookup"><span data-stu-id="edb5e-156">If this column is blank it means that there is no configuration key associated with the data entity.</span></span> <span data-ttu-id="edb5e-157">Konfiguratsioonivõtme oleku veerus kuvatakse konfiguratsioonivõtme olek.</span><span class="sxs-lookup"><span data-stu-id="edb5e-157">The configuration key status column shows the state of the configuration key.</span></span> <span data-ttu-id="edb5e-158">Kui see on märgitud, tähendab see, et võti on lubatud.</span><span class="sxs-lookup"><span data-stu-id="edb5e-158">If it has a checkmark, it means the key is enabled.</span></span> <span data-ttu-id="edb5e-159">Kui see on tühi, tähendab see, et võti on keelatud või võtit ei ole seostatud.</span><span class="sxs-lookup"><span data-stu-id="edb5e-159">If it is blank, it means either the key is disabled or there is no key associated.</span></span>

![Üksuste loendi leht](./media/Data_entity_list_page.png)

### <a name="target-fields"></a><span data-ttu-id="edb5e-161">Sihtväljad</span><span class="sxs-lookup"><span data-stu-id="edb5e-161">Target fields</span></span>
<span data-ttu-id="edb5e-162">Järgmiseks sammuks andmeteüksusesse süvitsiminek konfiguratsioonivõtmete mõju vaatamiseks tabelitele ja väljadele.</span><span class="sxs-lookup"><span data-stu-id="edb5e-162">The next step is to drill into the data entity to view the impact of configuration keys on tables and fields.</span></span> <span data-ttu-id="edb5e-163">Andmeüksuse sihtväljade vorm näitab andmeüksuses seotud tabelite ja väljade konfiguratsioonivõtme ja võtme oleku teavet.</span><span class="sxs-lookup"><span data-stu-id="edb5e-163">The target fields form for a data entity shows configuration key and the key status information for the related tables and fields in the data entity.</span></span> <span data-ttu-id="edb5e-164">Kui andmeüksus ise on oma konfiguratsioonivõtme keelanud, kuvatakse hoiatusteade, et selle üksuse sihtväljade vormi tabelid ja väljad ei ole sõltumata nende konfiguratsioonivõtme olekust üldse saadaval.</span><span class="sxs-lookup"><span data-stu-id="edb5e-164">If the data entity itself has its configuration key disabled, a warning message is shown informing that the tables and fields in the target fields form for this entity will not be available at all regardless of their configuration key status.</span></span>

![Sihtväljad](./media/Target_fields_1.png)

### <a name="child-entities"></a><span data-ttu-id="edb5e-166">Tütarüksused</span><span class="sxs-lookup"><span data-stu-id="edb5e-166">Child entities</span></span> 
<span data-ttu-id="edb5e-167">Teatud üksustel on andmeallikatena teisi üksuseid või need on liit-andmeüksused; nende üksuste konfiguratsioonivõtme teave kuvatakse alamüksuse vormil.</span><span class="sxs-lookup"><span data-stu-id="edb5e-167">Certain entities have other entities as data sources, or are composite data entities: configuration key information for these entities is shown in the Child entities form.</span></span> <span data-ttu-id="edb5e-168">Seda vormi saate kasutada samal viisil nagu ülal kirjeldatud üksusteloendi lehte.</span><span class="sxs-lookup"><span data-stu-id="edb5e-168">Use this form in the similar way to the entities list page described above.</span></span> <span data-ttu-id="edb5e-169">Alamüksuse sihtväljad käituvad samuti ülal kirjeldatud viisil.</span><span class="sxs-lookup"><span data-stu-id="edb5e-169">The target fields form for the child entity also behaves like what is described above.</span></span>

![Sihtväljad](./media/Target_fields_2.png)

### <a name="using-data-entities"></a><span data-ttu-id="edb5e-171">Andmeüksuste kasutamine</span><span class="sxs-lookup"><span data-stu-id="edb5e-171">Using data entities</span></span>
<span data-ttu-id="edb5e-172">Pärast konfiguratsioonivõtmete täieliku mõju mõistmist andmeüksustele, mida soovite kasutada, saate jätkata andmeüksuste kasutamist, lisades neid andmeprojektidele.</span><span class="sxs-lookup"><span data-stu-id="edb5e-172">After understanding the full impact, if any, of configuration keys on the data entities that you would like to use, you can now proceed to using the data entities by adding them to data projects.</span></span> 

### <a name="run-time-validations-for-configuration-keys"></a><span data-ttu-id="edb5e-173">Konfiguratsioonivõtmete käitusaja kontrollid</span><span class="sxs-lookup"><span data-stu-id="edb5e-173">Run time validations for configuration keys</span></span>
<span data-ttu-id="edb5e-174">Üksuste loendi värskendamise ajal loodud konfiguratsioonivõtme metaandmete kasutamisel tehakse käitusaja kontrolle järgmistel kasutusjuhtudel.</span><span class="sxs-lookup"><span data-stu-id="edb5e-174">Using the configuration key metadata built during entity refresh list, run time validations are performed in the following use cases.</span></span>

- <span data-ttu-id="edb5e-175">Kui andmeüksus lisatakse tööle</span><span class="sxs-lookup"><span data-stu-id="edb5e-175">When a data entity is added to a job</span></span>
- <span data-ttu-id="edb5e-176">Kui kasutaja klõpsab üksuste loendil käsku Kontrolli</span><span class="sxs-lookup"><span data-stu-id="edb5e-176">When user clicks 'validate' on the entity list</span></span>
- <span data-ttu-id="edb5e-177">Kui kasutaja laadib andmepaketi andmeprojekti</span><span class="sxs-lookup"><span data-stu-id="edb5e-177">When the user loads a data package into a data project</span></span>
- <span data-ttu-id="edb5e-178">Kui kasutaja laadib malli andmeprojekti</span><span class="sxs-lookup"><span data-stu-id="edb5e-178">When the user loads a template into a data project</span></span>
- <span data-ttu-id="edb5e-179">Kui olemasolev andmeprojekt on laaditud</span><span class="sxs-lookup"><span data-stu-id="edb5e-179">When an existing data project is loaded</span></span>
- <span data-ttu-id="edb5e-180">Kui mall on laaditud andmeprojekti</span><span class="sxs-lookup"><span data-stu-id="edb5e-180">When a template is loaded into a data project</span></span>
- <span data-ttu-id="edb5e-181">Enne ekspordi/impordi töö käivitamist (partii, mitte-partii, korduv, OData)</span><span class="sxs-lookup"><span data-stu-id="edb5e-181">Before the export/import job is executed (batch, non-batch, recurring, OData)</span></span>
- <span data-ttu-id="edb5e-182">Kui kasutaja loob vastendamise</span><span class="sxs-lookup"><span data-stu-id="edb5e-182">When the user generates mapping</span></span>
- <span data-ttu-id="edb5e-183">Kui kasutaja vastendab välju vastendamise kasutajaliidesel</span><span class="sxs-lookup"><span data-stu-id="edb5e-183">When the user maps fields in the mapping UI</span></span>
- <span data-ttu-id="edb5e-184">Kui kasutaja lisab ainult imporditavaid välju</span><span class="sxs-lookup"><span data-stu-id="edb5e-184">When the user adds only 'importable fields'</span></span>

### <a name="managing-configuration-key-changes"></a><span data-ttu-id="edb5e-185">Konfiguratsioonivõtme muudatuste haldamine</span><span class="sxs-lookup"><span data-stu-id="edb5e-185">Managing configuration key changes</span></span>
<span data-ttu-id="edb5e-186">Konfiguratsioonivõtmete värskendamisel üksuse, tabeli või välja tasemel tuleb värskendada andmehaldusraamistiku üksuste loendit.</span><span class="sxs-lookup"><span data-stu-id="edb5e-186">Anytime that you update configuration keys at the entity, table or field level, the entity list in the data management framework must be refreshed.</span></span> <span data-ttu-id="edb5e-187">See tagab, et raamistik komplekteerib konfiguratsioonivõtme uusimad sätted.</span><span class="sxs-lookup"><span data-stu-id="edb5e-187">This process ensures that the framework picks up the latest configuration key settings.</span></span> <span data-ttu-id="edb5e-188">Kuni üksuste loendit värskendatakse, kuvatakse üksuste loendi lehel järgmine hoiatus.</span><span class="sxs-lookup"><span data-stu-id="edb5e-188">Until the entity list is refreshed, the following warning will be shown in the entity list page.</span></span> <span data-ttu-id="edb5e-189">Värskendatud konfiguratsioonivõtme muudatused jõustuvad kohe pärast üksuste loendi värskendamist.</span><span class="sxs-lookup"><span data-stu-id="edb5e-189">The updated configuration key changes will take effect immediately after the entity list is refreshed.</span></span> <span data-ttu-id="edb5e-190">Soovitame olemasoleva andmeprojektid ja tööd kinnitada, veendumaks et need toimiksid pärast konfiguratsioonivõtmete muudatuste rakendamist õigesti.</span><span class="sxs-lookup"><span data-stu-id="edb5e-190">We recommend that you validate existing data projects and jobs to make sure that they function as expected after the configuration keys changes are put in effect.</span></span>

![Sihtväljad](./media/Target_fields_3.png)