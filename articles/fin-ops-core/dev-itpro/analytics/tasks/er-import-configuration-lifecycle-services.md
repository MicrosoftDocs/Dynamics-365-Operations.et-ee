---
title: Konfiguratsiooni importimine teenusest Lifecycle Services
description: Selles teemas selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad importida elektroonilise aruandluse (ER) konfiguratsiooni uue versiooni teenusest Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 59dbbf820f7a3de1e5fb31f781943320b8b1a60a
ms.sourcegitcommit: 9857d5cbdc0ab2fc9db049ac5ad118fc2b29bedc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/14/2020
ms.locfileid: "3810639"
---
# <a name="import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="0897c-103">Konfiguratsiooni importimine teenusest Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="0897c-103">Import a configuration from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0897c-104">Selles teemas selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad importida [elektroonilise aruandluse (ER) konfiguratsiooni](../general-electronic-reporting.md#Configuration) uue versiooni teenuse Microsoft Dynamics Lifecycle Services (LCS) [projekti tasandi varade teegist](../../lifecycle-services/asset-library.md).</span><span class="sxs-lookup"><span data-stu-id="0897c-104">This topic explains how a user in the System administrator or Electronic reporting developer role can import a new version of an [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) from the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="0897c-105">Selles näites valite soovitud ER-i konfiguratsiooni ja impordite selle näidisettevõttele Litware, Inc. Neid etappe saab läbida mis tahes ettevõttes, kuna ER-konfiguratsioonid on ettevõtete seas ühiskasutuses.</span><span class="sxs-lookup"><span data-stu-id="0897c-105">In this example, you will select the desired version of the ER configuration and import it for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="0897c-106">Etappide lõpule viimiseks, peate esmalt läbima protseduuri [Konfiguratsiooni üleslaadimine teenusesse Lifecycle Services](er-upload-configuration-into-lifecycle-services.md) etapid.</span><span class="sxs-lookup"><span data-stu-id="0897c-106">To complete these steps, you must first complete the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="0897c-107">Samuti on nõutav juurdepääs LCS-ile.</span><span class="sxs-lookup"><span data-stu-id="0897c-107">Access to LCS is also required.</span></span>

1. <span data-ttu-id="0897c-108">Logige rakendusse sisse, kasutades üht järgmistest rollidest.</span><span class="sxs-lookup"><span data-stu-id="0897c-108">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="0897c-109">Elektroonilise aruandluse arendaja</span><span class="sxs-lookup"><span data-stu-id="0897c-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="0897c-110">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="0897c-110">System administrator</span></span>

2. <span data-ttu-id="0897c-111">Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="0897c-111">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="0897c-112">Valige **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="0897c-112">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="0897c-113">Veenduge, et antud Dynamics 365 Finance'i kasutaja on selle LCS-i projekti liige, mis sisaldab varade teeki, millele kasutaja soovib [juurde pääseda](../../lifecycle-services/asset-library.md#asset-library-support) ER-konfiguratsioonide importimiseks.</span><span class="sxs-lookup"><span data-stu-id="0897c-113">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the Asset library that the user wants to [access](../../lifecycle-services/asset-library.md#asset-library-support) to import ER configurations.</span></span>
>
> <span data-ttu-id="0897c-114">Te ei pääse LCS-i projektile juurde ER-hoidlast, mis esindab rakenduses Finance kasutatavast domeenist erinevat domeeni.</span><span class="sxs-lookup"><span data-stu-id="0897c-114">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="0897c-115">Kui proovite, kuvatakse LCS-i projektide tühi loend ja te ei saa importida ER-konfiguratsioone LCS-i projekti tasandi varade teegist.</span><span class="sxs-lookup"><span data-stu-id="0897c-115">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="0897c-116">Projekti tasandi varade teekidele juurde pääsemiseks ER-konfiguratsioonide importimiseks kasutatavast ER-hoidlast logige rakendusse Finance sisse selle kasutaja mandaadi abil, kes kuulub rentnikku (domeeni), kelle jaoks praegune rakenduse Finance eksemplar on ette valmistatud.</span><span class="sxs-lookup"><span data-stu-id="0897c-116">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a><span data-ttu-id="0897c-117">Andmemudeli konfiguratsiooni ühiskasutuses versiooni kustutamine</span><span class="sxs-lookup"><span data-stu-id="0897c-117">Delete a shared version of a data model configuration</span></span>

1. <span data-ttu-id="0897c-118">Valige lehe **Konfiguratsioonid** konfiguratsioonide puult suvand **Mudeli konfiguratsiooni näide**.</span><span class="sxs-lookup"><span data-stu-id="0897c-118">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="0897c-119">Lõite andmemudeli konfiguratsiooni esimese versiooni ja avaldasite selle LCS-is, kui täitsite protsessi [Konfiguratsiooni üleslaadimine teenusesse Lifecycle Services](er-upload-configuration-into-lifecycle-services.md) etappe.</span><span class="sxs-lookup"><span data-stu-id="0897c-119">You created the first version of a sample data model configuration and published it to LCS when you completed the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="0897c-120">Selle protseduuri käigus kustutate selle ER-i konfiguratsiooni versiooni.</span><span class="sxs-lookup"><span data-stu-id="0897c-120">In this procedure, you will delete that version of the ER configuration.</span></span> <span data-ttu-id="0897c-121">Hiljem selles teemas impordite selle versiooni LCS-ist.</span><span class="sxs-lookup"><span data-stu-id="0897c-121">You will then import that version from LCS later in this topic.</span></span>

2. <span data-ttu-id="0897c-122">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="0897c-122">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="0897c-123">Valige selles näites selle konfiguratsiooni versioon, mille olek on **Ühiskasutuses**.</span><span class="sxs-lookup"><span data-stu-id="0897c-123">For this example, select the version of the configuration that has a status of **Shared**.</span></span> <span data-ttu-id="0897c-124">See olek näitab, et konfiguratsioon on avaldatud LCS-is.</span><span class="sxs-lookup"><span data-stu-id="0897c-124">This status indicates that the configuration has been published to LCS.</span></span>

3. <span data-ttu-id="0897c-125">Valige käsk **Muuda olekut**.</span><span class="sxs-lookup"><span data-stu-id="0897c-125">Select **Change status**.</span></span>
4. <span data-ttu-id="0897c-126">Valige nupp **Katkesta**.</span><span class="sxs-lookup"><span data-stu-id="0897c-126">Select **Discontinue**.</span></span>

    <span data-ttu-id="0897c-127">Muutes valitud versiooni oleku **Ühiskasutuses** olekuks **Katkestatud** muudetakse see kustutamiseks kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="0897c-127">By changing the status of the selected version from **Shared** to **Discontinued**, you make the version available for deletion.</span></span>

5. <span data-ttu-id="0897c-128">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="0897c-128">Select **OK**.</span></span>
6. <span data-ttu-id="0897c-129">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="0897c-129">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="0897c-130">Valige selles näites selle konfiguratsiooni versioon, mille olek on **Katkestatud**.</span><span class="sxs-lookup"><span data-stu-id="0897c-130">For this example, select the version of the configuration that has a status of **Discontinued**.</span></span>

7. <span data-ttu-id="0897c-131">Valige **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="0897c-131">Select **Delete**.</span></span>
8. <span data-ttu-id="0897c-132">Valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="0897c-132">Select **Yes**.</span></span>

    <span data-ttu-id="0897c-133">Pange tähele, et nüüd on saadaval ainult valitud andmemudeli konfiguratsiooni mustandversioon 2.</span><span class="sxs-lookup"><span data-stu-id="0897c-133">Notice that the only draft version 2 of the selected data model configuration is now available.</span></span>

9. <span data-ttu-id="0897c-134">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="0897c-134">Close the page.</span></span>

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a><span data-ttu-id="0897c-135">Andmemudeli konfiguratsiooni ühiskasutuses versiooni importimine LCS-ist</span><span class="sxs-lookup"><span data-stu-id="0897c-135">Import a shared version of a data model configuration from LCS</span></span>

1. <span data-ttu-id="0897c-136">Avage **Organisatsiooni haldamine \> Tööruumid \> Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="0897c-136">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="0897c-137">Valige jaotises **Konfiguratsiooni pakkujad** paan **Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="0897c-137">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="0897c-138">Valige paanil **Litware, Inc.** suvand **Hoidlad**.</span><span class="sxs-lookup"><span data-stu-id="0897c-138">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="0897c-139">See võimaldab avada ettevõtte Litware, Inc. konfiguratsioonipakkuja hoidlate loendi.</span><span class="sxs-lookup"><span data-stu-id="0897c-139">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="0897c-140">Valige **Avamine**.</span><span class="sxs-lookup"><span data-stu-id="0897c-140">Select **Open**.</span></span>

    <span data-ttu-id="0897c-141">Selle näite korral valige **LCS**-i hoidla ja avage see.</span><span class="sxs-lookup"><span data-stu-id="0897c-141">For this example, select the **LCS** repository, and open it.</span></span> <span data-ttu-id="0897c-142">Teil peab olema [juurdepääs](#accessconditions) LCS-i projektile ja varade teegile, millele valitud ER-hoidla juurde pääseb.</span><span class="sxs-lookup"><span data-stu-id="0897c-142">You must have [access](#accessconditions) to the LCS project and to the Asset library that is accessed by the selected ER repository.</span></span>

5. <span data-ttu-id="0897c-143">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="0897c-143">In the list, mark the selected row.</span></span>

    <span data-ttu-id="0897c-144">Valige selles näites versiooni loendist suvandi **Mudeli konfiguratsiooni näide** esimene versioon.</span><span class="sxs-lookup"><span data-stu-id="0897c-144">For this example, select the first version of **Sample model configuration** in the version list.</span></span>

6. <span data-ttu-id="0897c-145">Valige **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="0897c-145">Select **Import**.</span></span>
7. <span data-ttu-id="0897c-146">Valige **Jah**, et kinnitada valitud versiooni import LCS-ist.</span><span class="sxs-lookup"><span data-stu-id="0897c-146">Select **Yes** to confirm the import of the selected version from LCS.</span></span>

    <span data-ttu-id="0897c-147">Teade kinnitab, et valitud versioon on imporditud.</span><span class="sxs-lookup"><span data-stu-id="0897c-147">An informational message confirms that the selected version was successfully imported.</span></span>

8. <span data-ttu-id="0897c-148">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="0897c-148">Close the page.</span></span>
9. <span data-ttu-id="0897c-149">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="0897c-149">Close the page.</span></span>
10. <span data-ttu-id="0897c-150">Valige **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="0897c-150">Select **Configurations**.</span></span>
11. <span data-ttu-id="0897c-151">Valige puul väärtus **Mudeli konfiguratsiooni näide**.</span><span class="sxs-lookup"><span data-stu-id="0897c-151">In the tree, select **Sample model configuration**.</span></span>
12. <span data-ttu-id="0897c-152">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="0897c-152">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="0897c-153">Valige selles näites selle konfiguratsiooni versioon, mille olek on **Ühiskasutuses**.</span><span class="sxs-lookup"><span data-stu-id="0897c-153">For this example, select the version of the configuration that has a status of **Shared**.</span></span>

    <span data-ttu-id="0897c-154">Pange tähele, et nüüd on saadaval ka valitud andmemudeli konfiguratsiooni ühiskasutatav versioon 1.</span><span class="sxs-lookup"><span data-stu-id="0897c-154">Notice that shared version 1 of the selected data model configuration is also available now.</span></span>
