---
title: Konfiguratsiooni üleslaadimine teenusesse Lifecycle Services
description: Selles teemas selgitatakse, kuidas luua uus elektroonilise aruandluse (ER) konfiguratsioon ja laadida see üles teenusesse Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
ms.date: 06/17/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, ERDataModelDesigner, ERDataModelContentsItemCreationDialog, ERSolutionRepositoryTable, ERSolutionRepositoryCreateDropDialog, ERSolutionImport
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 41a8fcf2592bde4901aba703e0cd124b1155dac6
ms.sourcegitcommit: dc4898aa32f381620c517bf89c7856e693563ace
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/17/2021
ms.locfileid: "6270555"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="be4d1-103">Konfiguratsiooni üleslaadimine teenusesse Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="be4d1-103">Upload a configuration into Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="be4d1-104">Selles teemas selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad luua uue [elektroonilise aruandluse (ER) konfiguratsiooni](../general-electronic-reporting.md#Configuration) ja laadida selle teenuse Microsoft Dynamics Lifecycle Services (LCS) [projekti tasandi varade teeki](../../lifecycle-services/asset-library.md).</span><span class="sxs-lookup"><span data-stu-id="be4d1-104">This topic explains how a user in the System administrator or Electronic reporting developer role can create a new [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) and upload it into the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="be4d1-105">LCS kasutamine elektroonilise aruandluse (ER) konfiguratsiooni talletushoidlana on [aegunud](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span><span class="sxs-lookup"><span data-stu-id="be4d1-105">The use of LCS as a storage repository for ER configurations is being [deprecated](../../../../finance/get-started/removed-deprecated-features-finance.md#features-removed-or-deprecated-in-the-finance-10017-release).</span></span> <span data-ttu-id="be4d1-106">Lisateavet vt jaotisest [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) ladustamise amortiseerimine](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span><span class="sxs-lookup"><span data-stu-id="be4d1-106">For more information, see [Regulatory Configuration Service (RCS) – Lifecycle Services (LCS) storage deprecation](../../../../finance/localizations/rcs-lcs-repo-dep-faq.md).</span></span>

<span data-ttu-id="be4d1-107">Selles näites loote konfiguratsiooni näidisettevõttele Litware, Inc. ja laadite selle üles LCS-i. Neid etappe saab teha mis tahes ettevõttes, kuna ER-konfiguratsioonid on ettevõtetel ühised.</span><span class="sxs-lookup"><span data-stu-id="be4d1-107">In this example, you will create a configuration and upload it into LCS for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="be4d1-108">Etappide lõpuleviimiseks, peate esmalt läbima etapid teemas [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="be4d1-108">To complete these steps, you must first complete the steps in [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="be4d1-109">Samuti on nõutav juurdepääs LCS-ile.</span><span class="sxs-lookup"><span data-stu-id="be4d1-109">Access to LCS is also required.</span></span>

1. <span data-ttu-id="be4d1-110">Logige rakendusse sisse, kasutades üht järgmistest rollidest.</span><span class="sxs-lookup"><span data-stu-id="be4d1-110">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="be4d1-111">Elektroonilise aruandluse arendaja</span><span class="sxs-lookup"><span data-stu-id="be4d1-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="be4d1-112">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="be4d1-112">System administrator</span></span>

2. <span data-ttu-id="be4d1-113">Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="be4d1-113">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="be4d1-114">Valige **Litware, Inc.** ja sejärel valige **Aktiivne**.</span><span class="sxs-lookup"><span data-stu-id="be4d1-114">Select **Litware, Inc.**, and mark it as **Active**.</span></span>
4. <span data-ttu-id="be4d1-115">Valige **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="be4d1-115">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="be4d1-116">Veenduge, et antud Dynamics 365 Finance'i kasutaja on selle LCS-i projekti liige, mis sisaldab [varade teeki](../../lifecycle-services/asset-library.md#asset-library-support), mida kasutatakse ER-konfiguratsioonide importimiseks.</span><span class="sxs-lookup"><span data-stu-id="be4d1-116">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the [Asset library](../../lifecycle-services/asset-library.md#asset-library-support) that is used to import ER configurations.</span></span>
>
> <span data-ttu-id="be4d1-117">Te ei pääse LCS-i projektile juurde ER-hoidlast, mis esindab rakenduses Finance kasutatavast domeenist erinevat domeeni.</span><span class="sxs-lookup"><span data-stu-id="be4d1-117">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="be4d1-118">Kui proovite, kuvatakse LCS-i projektide tühi loend ja te ei saa importida ER-konfiguratsioone LCS-i projekti tasandi varade teegist.</span><span class="sxs-lookup"><span data-stu-id="be4d1-118">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="be4d1-119">Projekti tasandi varade teekidele juurde pääsemiseks ER-konfiguratsioonide importimiseks kasutatavast ER-hoidlast logige rakendusse Finance sisse selle kasutaja mandaadi abil, kes kuulub rentnikku (domeeni), kelle jaoks praegune rakenduse Finance eksemplar on ette valmistatud.</span><span class="sxs-lookup"><span data-stu-id="be4d1-119">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="be4d1-120">Uue andmemudeli konfiguratsiooni loomine</span><span class="sxs-lookup"><span data-stu-id="be4d1-120">Create a new data model configuration</span></span>

1. <span data-ttu-id="be4d1-121">Minge jaotisse **Organisatsiooni haldamine \> Elektrooniline aruandlus \> Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="be4d1-121">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="be4d1-122">Rippmenüü dialoogiboksi avamiseks valige lehel **Konfiguratsioonid** käsk **Loo konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="be4d1-122">On the **Configurations** page, select **Create configuration** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="be4d1-123">Selles näites loote konfiguratsiooni, mis sisaldab elektrooniliste dokumentide andmemudeli näidist.</span><span class="sxs-lookup"><span data-stu-id="be4d1-123">In this example, you will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="be4d1-124">Selle andmemudeli konfiguratsioon laaditakse hiljem LCS-i.</span><span class="sxs-lookup"><span data-stu-id="be4d1-124">This data model configuration will be uploaded into LCS later.</span></span>

3. <span data-ttu-id="be4d1-125">Tippige väljale **Nimi** tekst **Mudeli konfiguratsiooni näide**.</span><span class="sxs-lookup"><span data-stu-id="be4d1-125">In the **Name** field, enter **Sample model configuration**.</span></span>
4. <span data-ttu-id="be4d1-126">Tippige väljale **Kirjeldus** tekst **Mudeli konfiguratsiooni näide**.</span><span class="sxs-lookup"><span data-stu-id="be4d1-126">In the **Description** field, enter **Sample model configuration**.</span></span>
5. <span data-ttu-id="be4d1-127">Valige **Konfiguratsiooni loomine**.</span><span class="sxs-lookup"><span data-stu-id="be4d1-127">Select **Create configuration**.</span></span>
6. <span data-ttu-id="be4d1-128">Valige **Mudeli koostaja**.</span><span class="sxs-lookup"><span data-stu-id="be4d1-128">Select **Model designer**.</span></span>
7. <span data-ttu-id="be4d1-129">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="be4d1-129">Select **New**.</span></span>
8. <span data-ttu-id="be4d1-130">Väljale **Nimi** sisestage **Sisenemiskoht**.</span><span class="sxs-lookup"><span data-stu-id="be4d1-130">In the **Name** field, enter **Entry point**.</span></span>
9. <span data-ttu-id="be4d1-131">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="be4d1-131">Select **Add**.</span></span>
10. <span data-ttu-id="be4d1-132">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="be4d1-132">Select **Save**.</span></span>
11. <span data-ttu-id="be4d1-133">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="be4d1-133">Close the page.</span></span>
12. <span data-ttu-id="be4d1-134">Valige käsk **Muuda olekut**.</span><span class="sxs-lookup"><span data-stu-id="be4d1-134">Select **Change status**.</span></span>
13. <span data-ttu-id="be4d1-135">Valige **Lõpeta**.</span><span class="sxs-lookup"><span data-stu-id="be4d1-135">Select **Complete**.</span></span>
14. <span data-ttu-id="be4d1-136">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="be4d1-136">Select **OK**.</span></span>
15. <span data-ttu-id="be4d1-137">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="be4d1-137">Close the page.</span></span>

## <a name="register-a-new-repository"></a><span data-ttu-id="be4d1-138">Uue hoidla registreerimine</span><span class="sxs-lookup"><span data-stu-id="be4d1-138">Register a new repository</span></span>

1. <span data-ttu-id="be4d1-139">Avage **Organisatsiooni haldamine \> Tööruumid \> Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="be4d1-139">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="be4d1-140">Valige jaotises **Konfiguratsiooni pakkujad** paan **Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="be4d1-140">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="be4d1-141">Valige paanil **Litware, Inc.** suvand **Hoidlad**.</span><span class="sxs-lookup"><span data-stu-id="be4d1-141">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="be4d1-142">See võimaldab avada ettevõtte Litware, Inc. konfiguratsioonipakkuja hoidlate loendi.</span><span class="sxs-lookup"><span data-stu-id="be4d1-142">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="be4d1-143">Valige **Lisa**, et avada rippmenüü dialoogiaken.</span><span class="sxs-lookup"><span data-stu-id="be4d1-143">Select **Add** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="be4d1-144">Nüüd saate lisada uue hoidla.</span><span class="sxs-lookup"><span data-stu-id="be4d1-144">You can now add a new repository.</span></span>

5. <span data-ttu-id="be4d1-145">Sisestage väljale **Konfiguratsioonihoidla** valik **LCS**.</span><span class="sxs-lookup"><span data-stu-id="be4d1-145">In the **Configuration repository enter** field, select **LCS**.</span></span>
6. <span data-ttu-id="be4d1-146">Valige käsk **Loo hoidla**.</span><span class="sxs-lookup"><span data-stu-id="be4d1-146">Select **Create repository**.</span></span>
7. <span data-ttu-id="be4d1-147">Valige või sisestage väärtus väljal **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="be4d1-147">In the **Project** field, enter or select a value.</span></span>

    <span data-ttu-id="be4d1-148">Selle näite korral valige soovitud LCS-i projekt.</span><span class="sxs-lookup"><span data-stu-id="be4d1-148">For this example, select the desired LCS project.</span></span> <span data-ttu-id="be4d1-149">Teil peab olema [juurdepääs](#accessconditions) projektile.</span><span class="sxs-lookup"><span data-stu-id="be4d1-149">You must have [access](#accessconditions) to the project.</span></span>

8. <span data-ttu-id="be4d1-150">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="be4d1-150">Select **OK**.</span></span>

    <span data-ttu-id="be4d1-151">Täitke uus hoidla kirje.</span><span class="sxs-lookup"><span data-stu-id="be4d1-151">Complete a new repository entry.</span></span>

9. <span data-ttu-id="be4d1-152">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="be4d1-152">In the list, mark the selected row.</span></span>

    <span data-ttu-id="be4d1-153">Selle näite korral valige **LCS**-i hoidla kirje.</span><span class="sxs-lookup"><span data-stu-id="be4d1-153">For this example, select the **LCS** repository record.</span></span>

    <span data-ttu-id="be4d1-154">Pange tähele, et registreeritud hoidla on praeguse pakkuja poolt märgitud.</span><span class="sxs-lookup"><span data-stu-id="be4d1-154">Note that a registered repository is marked by the current provider.</span></span> <span data-ttu-id="be4d1-155">Teisisõnu saab sellesse hoidlasse panna ainult selle pakkuja omanduses olevaid konfiguratsioone ja seetõttu valitud LCS-i projekti üles laadida.</span><span class="sxs-lookup"><span data-stu-id="be4d1-155">In other words, only configurations that are owned by that provider can be put in this repository and therefore uploaded into the selected LCS project.</span></span>

10. <span data-ttu-id="be4d1-156">Valige **Avamine**.</span><span class="sxs-lookup"><span data-stu-id="be4d1-156">Select **Open**.</span></span>

    <span data-ttu-id="be4d1-157">Avage hoidla ER-i konfiguratsioonide loendi vaatamiseks.</span><span class="sxs-lookup"><span data-stu-id="be4d1-157">You open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="be4d1-158">Loend on tühi, kui valitud projekti pole veel kasutatud ER-i konfiguratsioonide ühiskasutuseks.</span><span class="sxs-lookup"><span data-stu-id="be4d1-158">If the selected project hasn't yet been used for ER configurations sharing, the list will be empty.</span></span>

11. <span data-ttu-id="be4d1-159">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="be4d1-159">Close the page.</span></span>
12. <span data-ttu-id="be4d1-160">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="be4d1-160">Close the page.</span></span>

## <a name="upload-a-configuration-into-lcs"></a><span data-ttu-id="be4d1-161">Konfiguratsiooni üleslaadimine LCS-i</span><span class="sxs-lookup"><span data-stu-id="be4d1-161">Upload a configuration into LCS</span></span>

1. <span data-ttu-id="be4d1-162">Minge jaotisse **Organisatsiooni haldamine \> Elektrooniline aruandlus \> Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="be4d1-162">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="be4d1-163">Valige lehe **Konfiguratsioonid** konfiguratsioonide puult suvand **Mudeli konfiguratsiooni näide**.</span><span class="sxs-lookup"><span data-stu-id="be4d1-163">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="be4d1-164">Peate valima loodud konfiguratsiooni, mis on juba lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="be4d1-164">You must select a created configuration that has been already completed.</span></span>

3. <span data-ttu-id="be4d1-165">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="be4d1-165">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="be4d1-166">Valige selles näites valitud konfiguratsiooni versioon, mille olek on **Lõpule viidud**.</span><span class="sxs-lookup"><span data-stu-id="be4d1-166">For this example, select the version of the selected configuration that has a status of **Completed**.</span></span>

4. <span data-ttu-id="be4d1-167">Valige käsk **Muuda olekut**.</span><span class="sxs-lookup"><span data-stu-id="be4d1-167">Select **Change status**.</span></span>
5. <span data-ttu-id="be4d1-168">Valige **Anna ühiskasutusse**.</span><span class="sxs-lookup"><span data-stu-id="be4d1-168">Select **Share**.</span></span>

    <span data-ttu-id="be4d1-169">Kui konfiguratsioon avaldatakse LCS-is, muudetakse konfiguratsiooni olek **Lõpule viidud** olekuks **Ühiskasutuses**.</span><span class="sxs-lookup"><span data-stu-id="be4d1-169">The status of the configuration is changed from **Completed** to **Shared** when the configuration is published in LCS.</span></span>

6. <span data-ttu-id="be4d1-170">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="be4d1-170">Select **OK**.</span></span>
7. <span data-ttu-id="be4d1-171">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="be4d1-171">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="be4d1-172">Valige selles näites selle konfiguratsiooni versioon, mille olek on **Ühiskasutuses**.</span><span class="sxs-lookup"><span data-stu-id="be4d1-172">For this example, select the configuration version that has a status of **Shared**.</span></span>

    <span data-ttu-id="be4d1-173">Pange tähele, et valitud versiooni olek **Lõpule viidud** muudeti olekuks **Ühiskasutuses**.</span><span class="sxs-lookup"><span data-stu-id="be4d1-173">Note that the status of the selected version was changed from **Completed** to **Shared**.</span></span>

8. <span data-ttu-id="be4d1-174">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="be4d1-174">Close the page.</span></span>
9. <span data-ttu-id="be4d1-175">Valige **Osad**.</span><span class="sxs-lookup"><span data-stu-id="be4d1-175">Select **Repositories**.</span></span>

    <span data-ttu-id="be4d1-176">See võimaldab avada ettevõtte Litware, Inc. konfiguratsioonipakkuja hoidlate loendi.</span><span class="sxs-lookup"><span data-stu-id="be4d1-176">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

10. <span data-ttu-id="be4d1-177">Valige **Avamine**.</span><span class="sxs-lookup"><span data-stu-id="be4d1-177">Select **Open**.</span></span>

    <span data-ttu-id="be4d1-178">Selle näite korral valige **LCS**-i hoidla ja avage see.</span><span class="sxs-lookup"><span data-stu-id="be4d1-178">For this example, select the **LCS** repository, and open it.</span></span>

    <span data-ttu-id="be4d1-179">Pange tähele, et valitud konfiguratsiooni näidatakse valitud LCS-i projekti varana.</span><span class="sxs-lookup"><span data-stu-id="be4d1-179">Notice that the selected configuration is shown as an asset of the selected LCS project.</span></span>

11. <span data-ttu-id="be4d1-180">Avage LCS, minnes saidile <https://lcs.dynamics.com>.</span><span class="sxs-lookup"><span data-stu-id="be4d1-180">Open LCS by going to <https://lcs.dynamics.com>.</span></span>
12. <span data-ttu-id="be4d1-181">Avage projekti, mida kasutati varem hoidla registreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="be4d1-181">Open a project that was used earlier for repository registration.</span></span>
13. <span data-ttu-id="be4d1-182">Avage projekti varade teek.</span><span class="sxs-lookup"><span data-stu-id="be4d1-182">Open the Asset library of the project.</span></span>
14. <span data-ttu-id="be4d1-183">Valige **GER-i konfiguratsiooni** vara tüüp.</span><span class="sxs-lookup"><span data-stu-id="be4d1-183">Select the **GER configuration** asset type.</span></span>

    <span data-ttu-id="be4d1-184">Teie üleslaaditud ER-konfiguratsioon peaks olema loetletud.</span><span class="sxs-lookup"><span data-stu-id="be4d1-184">The ER configuration that you uploaded should be listed.</span></span>

    <span data-ttu-id="be4d1-185">Pange tähele, et üleslaaditud LCS-i konfiguratsiooni saab importida teise eksemplari, kui teenuse pakkujatel on juurdepääs sellele LCS-i projektile.</span><span class="sxs-lookup"><span data-stu-id="be4d1-185">Note that the uploaded LCS configuration can be imported into another instance if providers have access to this LCS project.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
