---
title: Elektroonilise aruandluse (ER) konfiguratsiooni elutsükli haldamine
description: Selles teemas kirjeldatakse, kuidas hallata Microsoft Dynamics 365 Finance'i lahenduse elektroonilise aruandluse (ER) konfiguratsioonide elutsüklit.
author: NickSelin
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERMappedFormatDesigner, ERModelMappingDesigner, ERModelMappingTable, ERSolutionImport, ERSolutionTable, ERVendorTable, ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 58801
ms.assetid: 35ad19ea-185d-4fce-b9cb-f94584b14f75
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3b1b5ac8e256835332a4c53ed2872ee609253ad9
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5568721"
---
# <a name="manage-the-electronic-reporting-er-configuration-lifecycle"></a><span data-ttu-id="08298-103">Elektroonilise aruandluse (ER) konfiguratsiooni elutsükli haldamine</span><span class="sxs-lookup"><span data-stu-id="08298-103">Manage the Electronic reporting (ER) configuration lifecycle</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="08298-104">Selles teemas kirjeldatakse, kuidas hallata Microsoft Dynamics 365 Finance'i lahenduse elektroonilise aruandluse (ER) konfiguratsioonide elutsüklit.</span><span class="sxs-lookup"><span data-stu-id="08298-104">This topic describes how to manage the lifecycle of Electronic reporting (ER) configurations for Microsoft Dynamics 365 Finance.</span></span>

## <a name="overview"></a><span data-ttu-id="08298-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="08298-105">Overview</span></span>

<span data-ttu-id="08298-106">Elektrooniline aruandlus (ER) on mootor seadusega kehtestatud ja riigipõhiste elektrooniliste dokumentide toetamiseks.</span><span class="sxs-lookup"><span data-stu-id="08298-106">Electronic reporting (ER) is an engine that supports statutory required and country-specific electronic documents.</span></span> <span data-ttu-id="08298-107">Üldjuhul eeldab ER võimalust teha üksiku elektroonilise dokumendi puhul järgmisi toiminguid.</span><span class="sxs-lookup"><span data-stu-id="08298-107">In general, ER assumes an ability to perform the following tasks for a single electronic document.</span></span> <span data-ttu-id="08298-108">Lisateavet leiate jaotisest [Elektroonilise aruandluse (ER) ülevaade](general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="08298-108">For more details, see [Electronic reporting (ER) overview](general-electronic-reporting.md).</span></span>

- <span data-ttu-id="08298-109">Elektroonilise dokumendi malli kujundamine.</span><span class="sxs-lookup"><span data-stu-id="08298-109">Design a template for an electronic document:</span></span>

    - <span data-ttu-id="08298-110">Tuvastage nõutavad andmeallikad, mida saab dokumendis esitada:</span><span class="sxs-lookup"><span data-stu-id="08298-110">Identify the required sources of data that can be presented in the document:</span></span>

        - <span data-ttu-id="08298-111">Alusandmed, nt andmetabelid, andmeüksused ja klassid.</span><span class="sxs-lookup"><span data-stu-id="08298-111">Underlying data, such as data tables, data entities, and classes.</span></span>
        - <span data-ttu-id="08298-112">protsessipõhised atribuudid, nt käivitamise kuupäev ja kellaaeg ning ajatsoon;</span><span class="sxs-lookup"><span data-stu-id="08298-112">Process-specific properties, such as execution date and time, and time zone.</span></span>
        - <span data-ttu-id="08298-113">kasutaja sisendparameetrid, mille määrab lõppkasutaja käitamisel.</span><span class="sxs-lookup"><span data-stu-id="08298-113">User input parameters, specified by the end user at run time.</span></span>

    - <span data-ttu-id="08298-114">Määratlege vajalikud dokumendielemendid ja nende topoloogia lõppdokumendi vormingu määramiseks.</span><span class="sxs-lookup"><span data-stu-id="08298-114">Define the required document elements and their topology to specify a final document format.</span></span>
    - <span data-ttu-id="08298-115">Konfigureerige soovitud andmevoog valitud andmeallikatest määratletud dokumendielementidele (andmeallika sidumiste kaudu dokumendivormingu komponentidega) ja määrake protsessi juhtimisloogika.</span><span class="sxs-lookup"><span data-stu-id="08298-115">Configure the desired flow of data from selected data sources to defined document elements (via data source bindings to document format components), and specify process control logic.</span></span>

- <span data-ttu-id="08298-116">Tehke mall kättesaadavaks, et seda saaks teistes eksemplarides kasutada.</span><span class="sxs-lookup"><span data-stu-id="08298-116">Make a template available so that it can be used in other instances:</span></span>

    - <span data-ttu-id="08298-117">Teisendage dokumendimall ER-i konfiguratsiooniks ja eksportige konfiguratsioon praegusest rakenduse eksemplarist XML-paketina, mille saab salvestada kohalikult või LCS-i.</span><span class="sxs-lookup"><span data-stu-id="08298-117">Transform a document template that was created into an ER configuration, and export the configuration from the current application instance as an XML package that can be stored either locally or in LCS.</span></span>
    - <span data-ttu-id="08298-118">Teisendage ER-i konfiguratsioon rakenduse dokumendimalliks.</span><span class="sxs-lookup"><span data-stu-id="08298-118">Transform an ER configuration into an application document template.</span></span>
    - <span data-ttu-id="08298-119">Importige kohalikult või LCS-i salvestatud XML-pakett praegusesse eksemplari.</span><span class="sxs-lookup"><span data-stu-id="08298-119">Import an XML package that is stored either locally or in LCS into the current instance.</span></span>

- <span data-ttu-id="08298-120">Kohandage elektroonilise dokumendi malli.</span><span class="sxs-lookup"><span data-stu-id="08298-120">Customize the template of an electronic document:</span></span>

    - <span data-ttu-id="08298-121">Tooge mall LCS-ist praegusesse eksemplari ER-i konfiguratsioonina.</span><span class="sxs-lookup"><span data-stu-id="08298-121">Bring a template from LCS into the current instance as an ER configuration.</span></span>
    - <span data-ttu-id="08298-122">Kujundage ER-i konfiguratsioonist kohandatud versioon ja säilitage viide selle alusversioonile.</span><span class="sxs-lookup"><span data-stu-id="08298-122">Design a custom version of an ER configuration, and keep a reference to the base version.</span></span>

- <span data-ttu-id="08298-123">Integreerige mall konkreetse äriprotsessiga, nii et see oleks rakenduses saadaval.</span><span class="sxs-lookup"><span data-stu-id="08298-123">Integrate a template with a particular business process, so that it's available in the application:</span></span>

    - <span data-ttu-id="08298-124">Konfigureerige sätted nii, et rakendus hakkaks kasutama ER-i konfiguratsiooni, viidates sellele konfiguratsioonile protsessiga seotud parameetris.</span><span class="sxs-lookup"><span data-stu-id="08298-124">Configure settings so that the application starts to use an ER configuration, by referring to that configuration in a process-related parameter.</span></span> <span data-ttu-id="08298-125">Näiteks viidake ER-i konfiguratsioonile konkreetses ostureskontro makseviisis, et luua arvete töötlemiseks elektrooniline maksesõnum.</span><span class="sxs-lookup"><span data-stu-id="08298-125">For example, refer to the ER configuration in a specific Accounts payable payment method to generate an electronic payment message for processing invoices.</span></span>

- <span data-ttu-id="08298-126">Kasutage malli kindlas äriprotsessis.</span><span class="sxs-lookup"><span data-stu-id="08298-126">Use a template in a specific business process:</span></span>

    - <span data-ttu-id="08298-127">Käivitage ER-i konfiguratsioon konkreetses äriprotsessis.</span><span class="sxs-lookup"><span data-stu-id="08298-127">Run an ER configuration in a specific business process.</span></span> <span data-ttu-id="08298-128">Näiteks elektroonilise maksesõnumi loomiseks arvete töötlemiseks, kui on valitud ER-i konfiguratsioonile viitav makseviis.</span><span class="sxs-lookup"><span data-stu-id="08298-128">For example, to generate an electronic payment message for processing invoices when a payment method that references the ER configuration is selected.</span></span>

## <a name="concepts"></a><span data-ttu-id="08298-129">Mõisted</span><span class="sxs-lookup"><span data-stu-id="08298-129">Concepts</span></span>
<span data-ttu-id="08298-130">ER-i konfiguratsiooni elutsükliga on seotud järgmised rollid ja seotud tegevused.</span><span class="sxs-lookup"><span data-stu-id="08298-130">The following roles and related activities are associated with the ER configuration lifecycle.</span></span>

| <span data-ttu-id="08298-131">Roll</span><span class="sxs-lookup"><span data-stu-id="08298-131">Role</span></span>                                       | <span data-ttu-id="08298-132">Tegevused</span><span class="sxs-lookup"><span data-stu-id="08298-132">Activities</span></span>                                                      | <span data-ttu-id="08298-133">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="08298-133">Description</span></span> |
|--------------------------------------------|-----------------------------------------------------------------|-------------|
| <span data-ttu-id="08298-134">Elektroonilise aruandluse funktsionaalne konsultant</span><span class="sxs-lookup"><span data-stu-id="08298-134">Electronic reporting functional consultant</span></span> | <span data-ttu-id="08298-135">Looge ja hallake ER-i komponente (mudeleid ja vorminguid).</span><span class="sxs-lookup"><span data-stu-id="08298-135">Create and manage ER components (models and formats).</span></span>           | <span data-ttu-id="08298-136">Äriinimene, kes ER-i domeenipõhised andmemudelid kujundab, kujundab vajalikud elektrooniliste dokumentide mallid ja seob need vastavalt.</span><span class="sxs-lookup"><span data-stu-id="08298-136">A business person who designs ER domain–specific data models, designs the required templates for electronic documents, and binds them accordingly.</span></span> |
| <span data-ttu-id="08298-137">Elektroonilise aruandluse arendaja</span><span class="sxs-lookup"><span data-stu-id="08298-137">Electronic reporting developer</span></span>             | <span data-ttu-id="08298-138">Looge ja hallake andmemudeli vastendusi.</span><span class="sxs-lookup"><span data-stu-id="08298-138">Create and manage data model mappings.</span></span>                          | <span data-ttu-id="08298-139">Spetsialist, kes valib vajalikud Finance'i andmeallikad ja seob need ER-i domeenipõhiste andmemudelitega.</span><span class="sxs-lookup"><span data-stu-id="08298-139">A specialist who selects the required Finance data sources and binds them to ER domain–specific data models.</span></span> |
| <span data-ttu-id="08298-140">Raamatupidaja</span><span class="sxs-lookup"><span data-stu-id="08298-140">Accounting supervisor</span></span>                      | <span data-ttu-id="08298-141">Konfigureerige ER-i parasiitidele viitavaid protsessiga seotud sätteid.</span><span class="sxs-lookup"><span data-stu-id="08298-141">Configure process-related settings that reference ER artifacts.</span></span> | <span data-ttu-id="08298-142">Näiteks roll **Raamatupidaja**, mis võimaldab ER-i konfiguratsiooni sätete kasutamist konkreetses ostureskontro makseviisis arvete töötlemiseks vajaliku elektroonilise maksesõnumi koostamiseks.</span><span class="sxs-lookup"><span data-stu-id="08298-142">For example, an **Accounting supervisor** role that allows the settings of an ER configuration to be used in a particular Accounts payable payment method to generate an electronic payment message for processing invoices.</span></span> |
| <span data-ttu-id="08298-143">Ostureskontro maksuametnik</span><span class="sxs-lookup"><span data-stu-id="08298-143">Accounts payable payments clerk</span></span>            | <span data-ttu-id="08298-144">Kasutage ER-i parasiite kindlas äriprotsessis.</span><span class="sxs-lookup"><span data-stu-id="08298-144">Use ER artifacts in a specific business process.</span></span>                | <span data-ttu-id="08298-145">Näiteks roll **Ostureskontro maksuametnik**, mis võimaldab elektrooniliste maksesõnumite koostamist arvete töötlemiseks, tuginedes konkreetse makseviisi jaoks konfigureeritud ER-i vormingule.</span><span class="sxs-lookup"><span data-stu-id="08298-145">For example, an **Accounts payable payments clerk** role that allows electronic payment messages to be generated for processing invoices, based on the ER format that is configured for a specific payment method.</span></span> |

## <a name="er-configuration-development-lifecycle"></a><span data-ttu-id="08298-146">ER-i konfiguratsiooni arenduse elutsükkel</span><span class="sxs-lookup"><span data-stu-id="08298-146">ER configuration development lifecycle</span></span>
<span data-ttu-id="08298-147">Järgmistel ER-iga seotud põhjustel soovitame kujundada ER-i konfiguratsioonid arenduskeskkonnas eraldi Finance and Operationsi eksemplarina.</span><span class="sxs-lookup"><span data-stu-id="08298-147">For the following ER-related reasons, we recommend that you design ER configurations in the development environment, as a separate instance of Finance and Operations:</span></span>

- <span data-ttu-id="08298-148">Kasutajad rollis **Elektroonilise aruandluse arendaja** või rollis **Elektroonilise aruandluse funktsionaalne konsultant** saavad konfiguratsioone redigeerida ja neid testimise eesmärgil käitada.</span><span class="sxs-lookup"><span data-stu-id="08298-148">Users in either the **Electronic reporting developer** role or the **Electronic reporting functional consultant** role can edit configurations and run them for testing purposes.</span></span> <span data-ttu-id="08298-149">See stsenaarium võib põhjustada klasside ja tabelite meetodite kasutamise, mis võivad kahjustada äriandmeid ja eksemplari toimimist.</span><span class="sxs-lookup"><span data-stu-id="08298-149">This scenario can cause calls of methods of classes and tables that might harm business data and the performance of the instance.</span></span>
- <span data-ttu-id="08298-150">Klasside ja tabelite meetodite kasutamine ER-i konfiguratsioonide ER-i andmeallikatena ei ole piiratud sisestuspunktide ja logitud ettevõtte sisuga.</span><span class="sxs-lookup"><span data-stu-id="08298-150">Calls of methods of classes and tables as ER data sources of ER configurations aren't restricted by entry points and logged company content.</span></span> <span data-ttu-id="08298-151">Seega pääsevad äriliselt tundlike andmete juurde kasutajad rolliga **Elektroonilise aruandluse arendaja** või **Elektroonilise aruandluse funktsionaalne konsultant**.</span><span class="sxs-lookup"><span data-stu-id="08298-151">Therefore, users in either the **Electronic reporting developer** role or the **Electronic reporting functional consultant** role can access business-sensitive data.</span></span>

<span data-ttu-id="08298-152">Arenduskeskkonnas kujundatud ER-i konfiguratsioone saab üles laadida testkeskkonda, et hinnata konfiguratsiooni (õige protsessi integreerimine, tulemuste õigsus ja jõudlus) ja kvaliteedi tagamiseks, nt rolli juhitud juurdepääsuõiguste õigsus ja kohustuste jagamine.</span><span class="sxs-lookup"><span data-stu-id="08298-152">ER configurations that are designed in the development environment can be uploaded to the test environment for the configuration evaluation (proper process integration, correctness of results, and performance) and quality assurance, such as correctness of role-driven access rights and segregation of duties.</span></span> <span data-ttu-id="08298-153">Selleks saab kasutada funktsioone, mis lubavad ER-i konfiguratsiooni vahetamise.</span><span class="sxs-lookup"><span data-stu-id="08298-153">The features that enable ER configuration interchange can be used for this purpose.</span></span> <span data-ttu-id="08298-154">Lõpuks saab tõestatud ER-i konfiguratsioonid üles laadida kas LCS-i, kus neid saab teenuse tellijatega jagada, või tootmiskeskkonda ettevõttesiseseks kasutamiseks, nt nii, nagu on näidatud järgmisel joonisel.</span><span class="sxs-lookup"><span data-stu-id="08298-154">Finally, proven ER configurations can be uploaded either to LCS, where they can be shared with service subscribers, or to the production environment for internal use, such as shown in the following illustration.</span></span>

![ER-i konfiguratsiooni elutsükkel](./media/ger-configuration-lifecycle.png)

## <a name="additional-resources"></a><span data-ttu-id="08298-156">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="08298-156">Additional resources</span></span>

[<span data-ttu-id="08298-157">Elektroonilise aruandluse (ER) ülevaade</span><span class="sxs-lookup"><span data-stu-id="08298-157">Electronic reporting (ER) overview</span></span>](general-electronic-reporting.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]