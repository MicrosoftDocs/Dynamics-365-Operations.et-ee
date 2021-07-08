---
title: Konfiguratsiooni importimine teenusest Lifecycle Services
description: Selles teemas kirjeldatakse, kuidas importida elektroonilise aruandluse (ER) konfiguratsiooni uus versioon teenusest Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
ms.date: 06/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionRepositoryTable, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b58ecb8a7d6f52631dbca7642a4acbcf6ff895a3
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270833"
---
# <a name="import-a-configuration-from-lifecycle-services"></a><span data-ttu-id="a5140-103">Konfiguratsiooni importimine teenusest Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="a5140-103">Import a configuration from Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a5140-104">Selles teemas selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad importida [elektroonilise aruandluse (ER) konfiguratsiooni](../general-electronic-reporting.md#Configuration) uue versiooni teenuse Microsoft Dynamics Lifecycle Services (LCS) [projekti tasandi varade teegist](../../lifecycle-services/asset-library.md).</span><span class="sxs-lookup"><span data-stu-id="a5140-104">This topic explains how a user in the System administrator or Electronic reporting developer role can import a new version of an [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) from the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a5140-105">LCS kasutamine elektroonilise aruandluse (ER) konfiguratsiooni talletushoidlana on [aegunud](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span><span class="sxs-lookup"><span data-stu-id="a5140-105">The use of LCS as a storage repository for ER configurations is being [deprecated](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span></span> <span data-ttu-id="a5140-106">Lisateavet vt jaotisest [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) ladustamise amortiseerimine](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span><span class="sxs-lookup"><span data-stu-id="a5140-106">For more information, see [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span></span>

<span data-ttu-id="a5140-107">Selles näites valite soovitud ER-i konfiguratsiooni ja impordite selle näidisettevõttele Litware, Inc. Neid etappe saab läbida mis tahes ettevõttes, kuna ER-konfiguratsioonid on ettevõtete seas ühiskasutuses.</span><span class="sxs-lookup"><span data-stu-id="a5140-107">In this example, you will select the desired version of the ER configuration and import it for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="a5140-108">Etappide lõpule viimiseks, peate esmalt läbima protseduuri [Konfiguratsiooni üleslaadimine teenusesse Lifecycle Services](er-upload-configuration-into-lifecycle-services.md) etapid.</span><span class="sxs-lookup"><span data-stu-id="a5140-108">To complete these steps, you must first complete the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="a5140-109">Samuti on nõutav juurdepääs LCS-ile.</span><span class="sxs-lookup"><span data-stu-id="a5140-109">Access to LCS is also required.</span></span>

1. <span data-ttu-id="a5140-110">Logige rakendusse sisse, kasutades üht järgmistest rollidest.</span><span class="sxs-lookup"><span data-stu-id="a5140-110">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="a5140-111">Elektroonilise aruandluse arendaja</span><span class="sxs-lookup"><span data-stu-id="a5140-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="a5140-112">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="a5140-112">System administrator</span></span>

2. <span data-ttu-id="a5140-113">Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="a5140-113">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="a5140-114">Valige **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="a5140-114">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="a5140-115">Veenduge, et antud Dynamics 365 Finance'i kasutaja on selle LCS-i projekti liige, mis sisaldab varade teeki, millele kasutaja soovib [juurde pääseda](../../lifecycle-services/asset-library.md#asset-library-support) ER-konfiguratsioonide importimiseks.</span><span class="sxs-lookup"><span data-stu-id="a5140-115">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the Asset library that the user wants to [access](../../lifecycle-services/asset-library.md#asset-library-support) to import ER configurations.</span></span>
>
> <span data-ttu-id="a5140-116">Te ei pääse LCS-i projektile juurde ER-hoidlast, mis esindab rakenduses Finance kasutatavast domeenist erinevat domeeni.</span><span class="sxs-lookup"><span data-stu-id="a5140-116">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="a5140-117">Kui proovite, kuvatakse LCS-i projektide tühi loend ja te ei saa importida ER-konfiguratsioone LCS-i projekti tasandi varade teegist.</span><span class="sxs-lookup"><span data-stu-id="a5140-117">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="a5140-118">Projekti tasandi varade teekidele juurde pääsemiseks ER-konfiguratsioonide importimiseks kasutatavast ER-hoidlast logige rakendusse Finance sisse selle kasutaja mandaadi abil, kes kuulub rentnikku (domeeni), kelle jaoks praegune rakenduse Finance eksemplar on ette valmistatud.</span><span class="sxs-lookup"><span data-stu-id="a5140-118">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="delete-a-shared-version-of-a-data-model-configuration"></a><span data-ttu-id="a5140-119">Andmemudeli konfiguratsiooni ühiskasutuses versiooni kustutamine</span><span class="sxs-lookup"><span data-stu-id="a5140-119">Delete a shared version of a data model configuration</span></span>

1. <span data-ttu-id="a5140-120">Valige lehe **Konfiguratsioonid** konfiguratsioonide puult suvand **Mudeli konfiguratsiooni näide**.</span><span class="sxs-lookup"><span data-stu-id="a5140-120">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="a5140-121">Lõite andmemudeli konfiguratsiooni esimese versiooni ja avaldasite selle LCS-is, kui täitsite protsessi [Konfiguratsiooni üleslaadimine teenusesse Lifecycle Services](er-upload-configuration-into-lifecycle-services.md) etappe.</span><span class="sxs-lookup"><span data-stu-id="a5140-121">You created the first version of a sample data model configuration and published it to LCS when you completed the steps in [Upload a configuration into Lifecycle Services](er-upload-configuration-into-lifecycle-services.md).</span></span> <span data-ttu-id="a5140-122">Selle protseduuri käigus kustutate selle ER-i konfiguratsiooni versiooni.</span><span class="sxs-lookup"><span data-stu-id="a5140-122">In this procedure, you will delete that version of the ER configuration.</span></span> <span data-ttu-id="a5140-123">Hiljem selles teemas impordite selle versiooni LCS-ist.</span><span class="sxs-lookup"><span data-stu-id="a5140-123">You will then import that version from LCS later in this topic.</span></span>

2. <span data-ttu-id="a5140-124">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="a5140-124">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="a5140-125">Valige selles näites selle konfiguratsiooni versioon, mille olek on **Ühiskasutuses**.</span><span class="sxs-lookup"><span data-stu-id="a5140-125">For this example, select the version of the configuration that has a status of **Shared**.</span></span> <span data-ttu-id="a5140-126">See olek näitab, et konfiguratsioon on avaldatud LCS-is.</span><span class="sxs-lookup"><span data-stu-id="a5140-126">This status indicates that the configuration has been published to LCS.</span></span>

3. <span data-ttu-id="a5140-127">Valige käsk **Muuda olekut**.</span><span class="sxs-lookup"><span data-stu-id="a5140-127">Select **Change status**.</span></span>
4. <span data-ttu-id="a5140-128">Valige nupp **Katkesta**.</span><span class="sxs-lookup"><span data-stu-id="a5140-128">Select **Discontinue**.</span></span>

    <span data-ttu-id="a5140-129">Muutes valitud versiooni oleku **Ühiskasutuses** olekuks **Katkestatud** muudetakse see kustutamiseks kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="a5140-129">By changing the status of the selected version from **Shared** to **Discontinued**, you make the version available for deletion.</span></span>

5. <span data-ttu-id="a5140-130">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="a5140-130">Select **OK**.</span></span>
6. <span data-ttu-id="a5140-131">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="a5140-131">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="a5140-132">Valige selles näites selle konfiguratsiooni versioon, mille olek on **Katkestatud**.</span><span class="sxs-lookup"><span data-stu-id="a5140-132">For this example, select the version of the configuration that has a status of **Discontinued**.</span></span>

7. <span data-ttu-id="a5140-133">Valige **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="a5140-133">Select **Delete**.</span></span>
8. <span data-ttu-id="a5140-134">Valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="a5140-134">Select **Yes**.</span></span>

    <span data-ttu-id="a5140-135">Pange tähele, et nüüd on saadaval ainult valitud andmemudeli konfiguratsiooni mustandversioon 2.</span><span class="sxs-lookup"><span data-stu-id="a5140-135">Notice that the only draft version 2 of the selected data model configuration is now available.</span></span>

9. <span data-ttu-id="a5140-136">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a5140-136">Close the page.</span></span>

## <a name="import-a-shared-version-of-a-data-model-configuration-from-lcs"></a><span data-ttu-id="a5140-137">Andmemudeli konfiguratsiooni ühiskasutuses versiooni importimine LCS-ist</span><span class="sxs-lookup"><span data-stu-id="a5140-137">Import a shared version of a data model configuration from LCS</span></span>

1. <span data-ttu-id="a5140-138">Avage **Organisatsiooni haldamine \> Tööruumid \> Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="a5140-138">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="a5140-139">Valige jaotises **Konfiguratsiooni pakkujad** paan **Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="a5140-139">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="a5140-140">Valige paanil **Litware, Inc.** suvand **Hoidlad**.</span><span class="sxs-lookup"><span data-stu-id="a5140-140">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="a5140-141">See võimaldab avada ettevõtte Litware, Inc. konfiguratsioonipakkuja hoidlate loendi.</span><span class="sxs-lookup"><span data-stu-id="a5140-141">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="a5140-142">Valige **Avamine**.</span><span class="sxs-lookup"><span data-stu-id="a5140-142">Select **Open**.</span></span>

    <span data-ttu-id="a5140-143">Selle näite korral valige **LCS**-i hoidla ja avage see.</span><span class="sxs-lookup"><span data-stu-id="a5140-143">For this example, select the **LCS** repository, and open it.</span></span> <span data-ttu-id="a5140-144">Teil peab olema [juurdepääs](#accessconditions) LCS-i projektile ja varade teegile, millele valitud ER-hoidla juurde pääseb.</span><span class="sxs-lookup"><span data-stu-id="a5140-144">You must have [access](#accessconditions) to the LCS project and to the Asset library that is accessed by the selected ER repository.</span></span>

5. <span data-ttu-id="a5140-145">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="a5140-145">In the list, mark the selected row.</span></span>

    <span data-ttu-id="a5140-146">Valige selles näites versiooni loendist suvandi **Mudeli konfiguratsiooni näide** esimene versioon.</span><span class="sxs-lookup"><span data-stu-id="a5140-146">For this example, select the first version of **Sample model configuration** in the version list.</span></span>

6. <span data-ttu-id="a5140-147">Valige **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="a5140-147">Select **Import**.</span></span>
7. <span data-ttu-id="a5140-148">Valige **Jah**, et kinnitada valitud versiooni import LCS-ist.</span><span class="sxs-lookup"><span data-stu-id="a5140-148">Select **Yes** to confirm the import of the selected version from LCS.</span></span>

    <span data-ttu-id="a5140-149">Teade kinnitab, et valitud versioon on imporditud.</span><span class="sxs-lookup"><span data-stu-id="a5140-149">An informational message confirms that the selected version was successfully imported.</span></span>

8. <span data-ttu-id="a5140-150">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a5140-150">Close the page.</span></span>
9. <span data-ttu-id="a5140-151">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a5140-151">Close the page.</span></span>
10. <span data-ttu-id="a5140-152">Valige **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="a5140-152">Select **Configurations**.</span></span>
11. <span data-ttu-id="a5140-153">Valige puul väärtus **Mudeli konfiguratsiooni näide**.</span><span class="sxs-lookup"><span data-stu-id="a5140-153">In the tree, select **Sample model configuration**.</span></span>
12. <span data-ttu-id="a5140-154">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="a5140-154">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="a5140-155">Valige selles näites selle konfiguratsiooni versioon, mille olek on **Ühiskasutuses**.</span><span class="sxs-lookup"><span data-stu-id="a5140-155">For this example, select the version of the configuration that has a status of **Shared**.</span></span>

    <span data-ttu-id="a5140-156">Pange tähele, et nüüd on saadaval ka valitud andmemudeli konfiguratsiooni ühiskasutatav versioon 1.</span><span class="sxs-lookup"><span data-stu-id="a5140-156">Notice that shared version 1 of the selected data model configuration is also available now.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
