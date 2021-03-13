---
title: Konfiguratsiooni importimine teenusest Lifecycle Services
description: Selles teemas kirjeldatakse, kuidas importida elektroonilise aruandluse (ER) konfiguratsiooni uus versioon teenusest Microsoft Dynamics Lifecycle Services (LCS).
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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 602886b0dd729b8ec52940f42bd1c393dac8acda
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/30/2021
ms.locfileid: "5093691"
---
# <a name="import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="db9bd-103">Konfiguratsiooni importimine teenusest Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="db9bd-103">Import a configuration from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="db9bd-104">Selles teemas selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad importida [elektroonilise aruandluse (ER) konfiguratsiooni](../general-electronic-reporting.md#Configuration) uue versiooni teenuse Microsoft Dynamics Lifecycle Services (LCS) [projekti tasandi varade teegist](../../lifecycle-services/asset-library.md).</span><span class="sxs-lookup"><span data-stu-id="db9bd-104">This topic explains how a user in the System administrator or Electronic reporting developer role can import a new version of an [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) from the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="db9bd-105">Selles näites valite soovitud ER-i konfiguratsiooni ja impordite selle näidisettevõttele Litware, Inc. Neid etappe saab läbida mis tahes ettevõttes, kuna ER-konfiguratsioonid on ettevõtete seas ühiskasutuses.</span><span class="sxs-lookup"><span data-stu-id="db9bd-105">In this example, you will select the desired version of the ER configuration and import it for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="db9bd-106">Etappide lõpule viimiseks, peate esmalt läbima protseduuri [Konfiguratsiooni üleslaadimine teenusesse Lifecycle Services](er-upload-configuration-into-lifecycle-services.md) etapid.</span><span class="sxs-lookup"><span data-stu-id="db9bd-106">To complete these steps, you must first complete the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="db9bd-107">Samuti on nõutav juurdepääs LCS-ile.</span><span class="sxs-lookup"><span data-stu-id="db9bd-107">Access to LCS is also required.</span></span>

1. <span data-ttu-id="db9bd-108">Logige rakendusse sisse, kasutades üht järgmistest rollidest.</span><span class="sxs-lookup"><span data-stu-id="db9bd-108">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="db9bd-109">Elektroonilise aruandluse arendaja</span><span class="sxs-lookup"><span data-stu-id="db9bd-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="db9bd-110">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="db9bd-110">System administrator</span></span>

2. <span data-ttu-id="db9bd-111">Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="db9bd-111">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="db9bd-112">Valige **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="db9bd-112">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="db9bd-113">Veenduge, et antud Dynamics 365 Finance'i kasutaja on selle LCS-i projekti liige, mis sisaldab varade teeki, millele kasutaja soovib [juurde pääseda](../../lifecycle-services/asset-library.md#asset-library-support) ER-konfiguratsioonide importimiseks.</span><span class="sxs-lookup"><span data-stu-id="db9bd-113">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the Asset library that the user wants to [access](../../lifecycle-services/asset-library.md#asset-library-support) to import ER configurations.</span></span>
>
> <span data-ttu-id="db9bd-114">Te ei pääse LCS-i projektile juurde ER-hoidlast, mis esindab rakenduses Finance kasutatavast domeenist erinevat domeeni.</span><span class="sxs-lookup"><span data-stu-id="db9bd-114">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="db9bd-115">Kui proovite, kuvatakse LCS-i projektide tühi loend ja te ei saa importida ER-konfiguratsioone LCS-i projekti tasandi varade teegist.</span><span class="sxs-lookup"><span data-stu-id="db9bd-115">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="db9bd-116">Projekti tasandi varade teekidele juurde pääsemiseks ER-konfiguratsioonide importimiseks kasutatavast ER-hoidlast logige rakendusse Finance sisse selle kasutaja mandaadi abil, kes kuulub rentnikku (domeeni), kelle jaoks praegune rakenduse Finance eksemplar on ette valmistatud.</span><span class="sxs-lookup"><span data-stu-id="db9bd-116">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a><span data-ttu-id="db9bd-117">Andmemudeli konfiguratsiooni ühiskasutuses versiooni kustutamine</span><span class="sxs-lookup"><span data-stu-id="db9bd-117">Delete a shared version of a data model configuration</span></span>

1. <span data-ttu-id="db9bd-118">Valige lehe **Konfiguratsioonid** konfiguratsioonide puult suvand **Mudeli konfiguratsiooni näide**.</span><span class="sxs-lookup"><span data-stu-id="db9bd-118">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="db9bd-119">Lõite andmemudeli konfiguratsiooni esimese versiooni ja avaldasite selle LCS-is, kui täitsite protsessi [Konfiguratsiooni üleslaadimine teenusesse Lifecycle Services](er-upload-configuration-into-lifecycle-services.md) etappe.</span><span class="sxs-lookup"><span data-stu-id="db9bd-119">You created the first version of a sample data model configuration and published it to LCS when you completed the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="db9bd-120">Selle protseduuri käigus kustutate selle ER-i konfiguratsiooni versiooni.</span><span class="sxs-lookup"><span data-stu-id="db9bd-120">In this procedure, you will delete that version of the ER configuration.</span></span> <span data-ttu-id="db9bd-121">Hiljem selles teemas impordite selle versiooni LCS-ist.</span><span class="sxs-lookup"><span data-stu-id="db9bd-121">You will then import that version from LCS later in this topic.</span></span>

2. <span data-ttu-id="db9bd-122">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="db9bd-122">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="db9bd-123">Valige selles näites selle konfiguratsiooni versioon, mille olek on **Ühiskasutuses**.</span><span class="sxs-lookup"><span data-stu-id="db9bd-123">For this example, select the version of the configuration that has a status of **Shared**.</span></span> <span data-ttu-id="db9bd-124">See olek näitab, et konfiguratsioon on avaldatud LCS-is.</span><span class="sxs-lookup"><span data-stu-id="db9bd-124">This status indicates that the configuration has been published to LCS.</span></span>

3. <span data-ttu-id="db9bd-125">Valige käsk **Muuda olekut**.</span><span class="sxs-lookup"><span data-stu-id="db9bd-125">Select **Change status**.</span></span>
4. <span data-ttu-id="db9bd-126">Valige nupp **Katkesta**.</span><span class="sxs-lookup"><span data-stu-id="db9bd-126">Select **Discontinue**.</span></span>

    <span data-ttu-id="db9bd-127">Muutes valitud versiooni oleku **Ühiskasutuses** olekuks **Katkestatud** muudetakse see kustutamiseks kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="db9bd-127">By changing the status of the selected version from **Shared** to **Discontinued**, you make the version available for deletion.</span></span>

5. <span data-ttu-id="db9bd-128">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="db9bd-128">Select **OK**.</span></span>
6. <span data-ttu-id="db9bd-129">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="db9bd-129">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="db9bd-130">Valige selles näites selle konfiguratsiooni versioon, mille olek on **Katkestatud**.</span><span class="sxs-lookup"><span data-stu-id="db9bd-130">For this example, select the version of the configuration that has a status of **Discontinued**.</span></span>

7. <span data-ttu-id="db9bd-131">Valige **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="db9bd-131">Select **Delete**.</span></span>
8. <span data-ttu-id="db9bd-132">Valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="db9bd-132">Select **Yes**.</span></span>

    <span data-ttu-id="db9bd-133">Pange tähele, et nüüd on saadaval ainult valitud andmemudeli konfiguratsiooni mustandversioon 2.</span><span class="sxs-lookup"><span data-stu-id="db9bd-133">Notice that the only draft version 2 of the selected data model configuration is now available.</span></span>

9. <span data-ttu-id="db9bd-134">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="db9bd-134">Close the page.</span></span>

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a><span data-ttu-id="db9bd-135">Andmemudeli konfiguratsiooni ühiskasutuses versiooni importimine LCS-ist</span><span class="sxs-lookup"><span data-stu-id="db9bd-135">Import a shared version of a data model configuration from LCS</span></span>

1. <span data-ttu-id="db9bd-136">Avage **Organisatsiooni haldamine \> Tööruumid \> Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="db9bd-136">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="db9bd-137">Valige jaotises **Konfiguratsiooni pakkujad** paan **Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="db9bd-137">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="db9bd-138">Valige paanil **Litware, Inc.** suvand **Hoidlad**.</span><span class="sxs-lookup"><span data-stu-id="db9bd-138">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="db9bd-139">See võimaldab avada ettevõtte Litware, Inc. konfiguratsioonipakkuja hoidlate loendi.</span><span class="sxs-lookup"><span data-stu-id="db9bd-139">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="db9bd-140">Valige **Avamine**.</span><span class="sxs-lookup"><span data-stu-id="db9bd-140">Select **Open**.</span></span>

    <span data-ttu-id="db9bd-141">Selle näite korral valige **LCS**-i hoidla ja avage see.</span><span class="sxs-lookup"><span data-stu-id="db9bd-141">For this example, select the **LCS** repository, and open it.</span></span> <span data-ttu-id="db9bd-142">Teil peab olema [juurdepääs](#accessconditions) LCS-i projektile ja varade teegile, millele valitud ER-hoidla juurde pääseb.</span><span class="sxs-lookup"><span data-stu-id="db9bd-142">You must have [access](#accessconditions) to the LCS project and to the Asset library that is accessed by the selected ER repository.</span></span>

5. <span data-ttu-id="db9bd-143">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="db9bd-143">In the list, mark the selected row.</span></span>

    <span data-ttu-id="db9bd-144">Valige selles näites versiooni loendist suvandi **Mudeli konfiguratsiooni näide** esimene versioon.</span><span class="sxs-lookup"><span data-stu-id="db9bd-144">For this example, select the first version of **Sample model configuration** in the version list.</span></span>

6. <span data-ttu-id="db9bd-145">Valige **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="db9bd-145">Select **Import**.</span></span>
7. <span data-ttu-id="db9bd-146">Valige **Jah**, et kinnitada valitud versiooni import LCS-ist.</span><span class="sxs-lookup"><span data-stu-id="db9bd-146">Select **Yes** to confirm the import of the selected version from LCS.</span></span>

    <span data-ttu-id="db9bd-147">Teade kinnitab, et valitud versioon on imporditud.</span><span class="sxs-lookup"><span data-stu-id="db9bd-147">An informational message confirms that the selected version was successfully imported.</span></span>

8. <span data-ttu-id="db9bd-148">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="db9bd-148">Close the page.</span></span>
9. <span data-ttu-id="db9bd-149">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="db9bd-149">Close the page.</span></span>
10. <span data-ttu-id="db9bd-150">Valige **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="db9bd-150">Select **Configurations**.</span></span>
11. <span data-ttu-id="db9bd-151">Valige puul väärtus **Mudeli konfiguratsiooni näide**.</span><span class="sxs-lookup"><span data-stu-id="db9bd-151">In the tree, select **Sample model configuration**.</span></span>
12. <span data-ttu-id="db9bd-152">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="db9bd-152">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="db9bd-153">Valige selles näites selle konfiguratsiooni versioon, mille olek on **Ühiskasutuses**.</span><span class="sxs-lookup"><span data-stu-id="db9bd-153">For this example, select the version of the configuration that has a status of **Shared**.</span></span>

    <span data-ttu-id="db9bd-154">Pange tähele, et nüüd on saadaval ka valitud andmemudeli konfiguratsiooni ühiskasutatav versioon 1.</span><span class="sxs-lookup"><span data-stu-id="db9bd-154">Notice that shared version 1 of the selected data model configuration is also available now.</span></span>
