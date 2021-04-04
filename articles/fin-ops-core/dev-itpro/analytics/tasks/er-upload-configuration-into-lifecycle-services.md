---
title: Konfiguratsiooni üleslaadimine teenusesse Lifecycle Services
description: Selles teemas selgitatakse, kuidas luua uus elektroonilise aruandluse (ER) konfiguratsioon ja laadida see üles teenusesse Microsoft Dynamics Lifecycle Services (LCS).
author: NickSelin
manager: AnnBe
ms.date: 09/14/2020
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
ms.openlocfilehash: 6f17763236594092d04dfe2d2f9912e764b4f8d4
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562633"
---
# <a name="upload-a-configuration-into-lifecycle-services"></a><span data-ttu-id="da7ce-103">Konfiguratsiooni üleslaadimine teenusesse Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="da7ce-103">Upload a configuration into Lifecycle Services</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="da7ce-104">Selles teemas selgitatakse, kuidas süsteemiadministraatori või elektroonilise aruandluse arendaja rolli määratud kasutajad saavad luua uue [elektroonilise aruandluse (ER) konfiguratsiooni](../general-electronic-reporting.md#Configuration) ja laadida selle teenuse Microsoft Dynamics Lifecycle Services (LCS) [projekti tasandi varade teeki](../../lifecycle-services/asset-library.md).</span><span class="sxs-lookup"><span data-stu-id="da7ce-104">This topic explains how a user in the System administrator or Electronic reporting developer role can create a new [Electronic reporting (ER) configuration](../general-electronic-reporting.md#Configuration) and upload it into the [project-level Asset library](../../lifecycle-services/asset-library.md) in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="da7ce-105">Selles näites loote konfiguratsiooni näidisettevõttele Litware, Inc. ja laadite selle üles LCS-i. Neid etappe saab teha mis tahes ettevõttes, kuna ER-konfiguratsioonid on ettevõtetel ühised.</span><span class="sxs-lookup"><span data-stu-id="da7ce-105">In this example, you will create a configuration and upload it into LCS for a sample company that is named Litware, Inc. These steps can be completed in any company, because ER configurations are shared among companies.</span></span> <span data-ttu-id="da7ce-106">Etappide lõpuleviimiseks, peate esmalt läbima etapid teemas [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="da7ce-106">To complete these steps, you must first complete the steps in [Create configuration providers and mark them as active](er-configuration-provider-mark-it-active-2016-11.md).</span></span> <span data-ttu-id="da7ce-107">Samuti on nõutav juurdepääs LCS-ile.</span><span class="sxs-lookup"><span data-stu-id="da7ce-107">Access to LCS is also required.</span></span>

1. <span data-ttu-id="da7ce-108">Logige rakendusse sisse, kasutades üht järgmistest rollidest.</span><span class="sxs-lookup"><span data-stu-id="da7ce-108">Sign in to the application by using one of the following roles:</span></span>

    - <span data-ttu-id="da7ce-109">Elektroonilise aruandluse arendaja</span><span class="sxs-lookup"><span data-stu-id="da7ce-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="da7ce-110">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="da7ce-110">System administrator</span></span>

2. <span data-ttu-id="da7ce-111">Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="da7ce-111">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="da7ce-112">Valige **Litware, Inc.** ja sejärel valige **Aktiivne**.</span><span class="sxs-lookup"><span data-stu-id="da7ce-112">Select **Litware, Inc.**, and mark it as **Active**.</span></span>
4. <span data-ttu-id="da7ce-113">Valige **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="da7ce-113">Select **Configurations**.</span></span>

<a name="accessconditions"></a>
> [!NOTE]
> <span data-ttu-id="da7ce-114">Veenduge, et antud Dynamics 365 Finance'i kasutaja on selle LCS-i projekti liige, mis sisaldab [varade teeki](../../lifecycle-services/asset-library.md#asset-library-support), mida kasutatakse ER-konfiguratsioonide importimiseks.</span><span class="sxs-lookup"><span data-stu-id="da7ce-114">Make sure that the current Dynamics 365 Finance user is a member of the LCS project that contains the [Asset library](../../lifecycle-services/asset-library.md#asset-library-support) that is used to import ER configurations.</span></span>
>
> <span data-ttu-id="da7ce-115">Te ei pääse LCS-i projektile juurde ER-hoidlast, mis esindab rakenduses Finance kasutatavast domeenist erinevat domeeni.</span><span class="sxs-lookup"><span data-stu-id="da7ce-115">You can't access an LCS project from an ER repository that represents a different domain than the domain that is used in Finance.</span></span> <span data-ttu-id="da7ce-116">Kui proovite, kuvatakse LCS-i projektide tühi loend ja te ei saa importida ER-konfiguratsioone LCS-i projekti tasandi varade teegist.</span><span class="sxs-lookup"><span data-stu-id="da7ce-116">If you try, an empty list of LCS projects will be shown, and you won't be able to import ER configurations from the project-level Asset library in LCS.</span></span> <span data-ttu-id="da7ce-117">Projekti tasandi varade teekidele juurde pääsemiseks ER-konfiguratsioonide importimiseks kasutatavast ER-hoidlast logige rakendusse Finance sisse selle kasutaja mandaadi abil, kes kuulub rentnikku (domeeni), kelle jaoks praegune rakenduse Finance eksemplar on ette valmistatud.</span><span class="sxs-lookup"><span data-stu-id="da7ce-117">To access project-level Asset libraries from an ER repository that is used to import ER configurations, sign in to Finance by using the credentials of a user who belongs to the tenant (domain) that the current Finance instance has been provisioned for.</span></span>

## <a name="create-a-new-data-model-configuration"></a><span data-ttu-id="da7ce-118">Uue andmemudeli konfiguratsiooni loomine</span><span class="sxs-lookup"><span data-stu-id="da7ce-118">Create a new data model configuration</span></span>

1. <span data-ttu-id="da7ce-119">Minge jaotisse **Organisatsiooni haldamine \> Elektrooniline aruandlus \> Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="da7ce-119">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="da7ce-120">Rippmenüü dialoogiboksi avamiseks valige lehel **Konfiguratsioonid** käsk **Loo konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="da7ce-120">On the **Configurations** page, select **Create configuration** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="da7ce-121">Selles näites loote konfiguratsiooni, mis sisaldab elektrooniliste dokumentide andmemudeli näidist.</span><span class="sxs-lookup"><span data-stu-id="da7ce-121">In this example, you will create a configuration that contains a sample data model for electronic documents.</span></span> <span data-ttu-id="da7ce-122">Selle andmemudeli konfiguratsioon laaditakse hiljem LCS-i.</span><span class="sxs-lookup"><span data-stu-id="da7ce-122">This data model configuration will be uploaded into LCS later.</span></span>

3. <span data-ttu-id="da7ce-123">Tippige väljale **Nimi** tekst **Mudeli konfiguratsiooni näide**.</span><span class="sxs-lookup"><span data-stu-id="da7ce-123">In the **Name** field, enter **Sample model configuration**.</span></span>
4. <span data-ttu-id="da7ce-124">Tippige väljale **Kirjeldus** tekst **Mudeli konfiguratsiooni näide**.</span><span class="sxs-lookup"><span data-stu-id="da7ce-124">In the **Description** field, enter **Sample model configuration**.</span></span>
5. <span data-ttu-id="da7ce-125">Valige **Konfiguratsiooni loomine**.</span><span class="sxs-lookup"><span data-stu-id="da7ce-125">Select **Create configuration**.</span></span>
6. <span data-ttu-id="da7ce-126">Valige **Mudeli koostaja**.</span><span class="sxs-lookup"><span data-stu-id="da7ce-126">Select **Model designer**.</span></span>
7. <span data-ttu-id="da7ce-127">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="da7ce-127">Select **New**.</span></span>
8. <span data-ttu-id="da7ce-128">Väljale **Nimi** sisestage **Sisenemiskoht**.</span><span class="sxs-lookup"><span data-stu-id="da7ce-128">In the **Name** field, enter **Entry point**.</span></span>
9. <span data-ttu-id="da7ce-129">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="da7ce-129">Select **Add**.</span></span>
10. <span data-ttu-id="da7ce-130">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="da7ce-130">Select **Save**.</span></span>
11. <span data-ttu-id="da7ce-131">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="da7ce-131">Close the page.</span></span>
12. <span data-ttu-id="da7ce-132">Valige käsk **Muuda olekut**.</span><span class="sxs-lookup"><span data-stu-id="da7ce-132">Select **Change status**.</span></span>
13. <span data-ttu-id="da7ce-133">Valige **Lõpeta**.</span><span class="sxs-lookup"><span data-stu-id="da7ce-133">Select **Complete**.</span></span>
14. <span data-ttu-id="da7ce-134">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="da7ce-134">Select **OK**.</span></span>
15. <span data-ttu-id="da7ce-135">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="da7ce-135">Close the page.</span></span>

## <a name="register-a-new-repository"></a><span data-ttu-id="da7ce-136">Uue hoidla registreerimine</span><span class="sxs-lookup"><span data-stu-id="da7ce-136">Register a new repository</span></span>

1. <span data-ttu-id="da7ce-137">Avage **Organisatsiooni haldamine \> Tööruumid \> Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="da7ce-137">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>

2. <span data-ttu-id="da7ce-138">Valige jaotises **Konfiguratsiooni pakkujad** paan **Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="da7ce-138">In the **Configuration providers** section, select the **Litware, Inc.** tile.</span></span>

3. <span data-ttu-id="da7ce-139">Valige paanil **Litware, Inc.** suvand **Hoidlad**.</span><span class="sxs-lookup"><span data-stu-id="da7ce-139">On the **Litware, Inc.** tile, select **Repositories**.</span></span>

    <span data-ttu-id="da7ce-140">See võimaldab avada ettevõtte Litware, Inc. konfiguratsioonipakkuja hoidlate loendi.</span><span class="sxs-lookup"><span data-stu-id="da7ce-140">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

4. <span data-ttu-id="da7ce-141">Valige **Lisa**, et avada rippmenüü dialoogiaken.</span><span class="sxs-lookup"><span data-stu-id="da7ce-141">Select **Add** to open the drop-down dialog box.</span></span>

    <span data-ttu-id="da7ce-142">Nüüd saate lisada uue hoidla.</span><span class="sxs-lookup"><span data-stu-id="da7ce-142">You can now add a new repository.</span></span>

5. <span data-ttu-id="da7ce-143">Sisestage väljale **Konfiguratsioonihoidla** valik **LCS**.</span><span class="sxs-lookup"><span data-stu-id="da7ce-143">In the **Configuration repository enter** field, select **LCS**.</span></span>
6. <span data-ttu-id="da7ce-144">Valige käsk **Loo hoidla**.</span><span class="sxs-lookup"><span data-stu-id="da7ce-144">Select **Create repository**.</span></span>
7. <span data-ttu-id="da7ce-145">Valige või sisestage väärtus väljal **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="da7ce-145">In the **Project** field, enter or select a value.</span></span>

    <span data-ttu-id="da7ce-146">Selle näite korral valige soovitud LCS-i projekt.</span><span class="sxs-lookup"><span data-stu-id="da7ce-146">For this example, select the desired LCS project.</span></span> <span data-ttu-id="da7ce-147">Teil peab olema [juurdepääs](#accessconditions) projektile.</span><span class="sxs-lookup"><span data-stu-id="da7ce-147">You must have [access](#accessconditions) to the project.</span></span>

8. <span data-ttu-id="da7ce-148">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="da7ce-148">Select **OK**.</span></span>

    <span data-ttu-id="da7ce-149">Täitke uus hoidla kirje.</span><span class="sxs-lookup"><span data-stu-id="da7ce-149">Complete a new repository entry.</span></span>

9. <span data-ttu-id="da7ce-150">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="da7ce-150">In the list, mark the selected row.</span></span>

    <span data-ttu-id="da7ce-151">Selle näite korral valige **LCS**-i hoidla kirje.</span><span class="sxs-lookup"><span data-stu-id="da7ce-151">For this example, select the **LCS** repository record.</span></span>

    <span data-ttu-id="da7ce-152">Pange tähele, et registreeritud hoidla on praeguse pakkuja poolt märgitud.</span><span class="sxs-lookup"><span data-stu-id="da7ce-152">Note that a registered repository is marked by the current provider.</span></span> <span data-ttu-id="da7ce-153">Teisisõnu saab sellesse hoidlasse panna ainult selle pakkuja omanduses olevaid konfiguratsioone ja seetõttu valitud LCS-i projekti üles laadida.</span><span class="sxs-lookup"><span data-stu-id="da7ce-153">In other words, only configurations that are owned by that provider can be put in this repository and therefore uploaded into the selected LCS project.</span></span>

10. <span data-ttu-id="da7ce-154">Valige **Avamine**.</span><span class="sxs-lookup"><span data-stu-id="da7ce-154">Select **Open**.</span></span>

    <span data-ttu-id="da7ce-155">Avage hoidla ER-i konfiguratsioonide loendi vaatamiseks.</span><span class="sxs-lookup"><span data-stu-id="da7ce-155">You open the repository to view the list of ER configurations.</span></span> <span data-ttu-id="da7ce-156">Loend on tühi, kui valitud projekti pole veel kasutatud ER-i konfiguratsioonide ühiskasutuseks.</span><span class="sxs-lookup"><span data-stu-id="da7ce-156">If the selected project hasn't yet been used for ER configurations sharing, the list will be empty.</span></span>

11. <span data-ttu-id="da7ce-157">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="da7ce-157">Close the page.</span></span>
12. <span data-ttu-id="da7ce-158">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="da7ce-158">Close the page.</span></span>

## <a name="upload-a-configuration-into-lcs"></a><span data-ttu-id="da7ce-159">Konfiguratsiooni üleslaadimine LCS-i</span><span class="sxs-lookup"><span data-stu-id="da7ce-159">Upload a configuration into LCS</span></span>

1. <span data-ttu-id="da7ce-160">Minge jaotisse **Organisatsiooni haldamine \> Elektrooniline aruandlus \> Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="da7ce-160">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="da7ce-161">Valige lehe **Konfiguratsioonid** konfiguratsioonide puult suvand **Mudeli konfiguratsiooni näide**.</span><span class="sxs-lookup"><span data-stu-id="da7ce-161">On the **Configurations** page, in the configurations tree, select **Sample model configuration**.</span></span>

    <span data-ttu-id="da7ce-162">Peate valima loodud konfiguratsiooni, mis on juba lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="da7ce-162">You must select a created configuration that has been already completed.</span></span>

3. <span data-ttu-id="da7ce-163">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="da7ce-163">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="da7ce-164">Valige selles näites valitud konfiguratsiooni versioon, mille olek on **Lõpule viidud**.</span><span class="sxs-lookup"><span data-stu-id="da7ce-164">For this example, select the version of the selected configuration that has a status of **Completed**.</span></span>

4. <span data-ttu-id="da7ce-165">Valige käsk **Muuda olekut**.</span><span class="sxs-lookup"><span data-stu-id="da7ce-165">Select **Change status**.</span></span>
5. <span data-ttu-id="da7ce-166">Valige **Anna ühiskasutusse**.</span><span class="sxs-lookup"><span data-stu-id="da7ce-166">Select **Share**.</span></span>

    <span data-ttu-id="da7ce-167">Kui konfiguratsioon avaldatakse LCS-is, muudetakse konfiguratsiooni olek **Lõpule viidud** olekuks **Ühiskasutuses**.</span><span class="sxs-lookup"><span data-stu-id="da7ce-167">The status of the configuration is changed from **Completed** to **Shared** when the configuration is published in LCS.</span></span>

6. <span data-ttu-id="da7ce-168">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="da7ce-168">Select **OK**.</span></span>
7. <span data-ttu-id="da7ce-169">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="da7ce-169">In the list, find and select the desired record.</span></span>

    <span data-ttu-id="da7ce-170">Valige selles näites selle konfiguratsiooni versioon, mille olek on **Ühiskasutuses**.</span><span class="sxs-lookup"><span data-stu-id="da7ce-170">For this example, select the configuration version that has a status of **Shared**.</span></span>

    <span data-ttu-id="da7ce-171">Pange tähele, et valitud versiooni olek **Lõpule viidud** muudeti olekuks **Ühiskasutuses**.</span><span class="sxs-lookup"><span data-stu-id="da7ce-171">Note that the status of the selected version was changed from **Completed** to **Shared**.</span></span>

8. <span data-ttu-id="da7ce-172">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="da7ce-172">Close the page.</span></span>
9. <span data-ttu-id="da7ce-173">Valige **Osad**.</span><span class="sxs-lookup"><span data-stu-id="da7ce-173">Select **Repositories**.</span></span>

    <span data-ttu-id="da7ce-174">See võimaldab avada ettevõtte Litware, Inc. konfiguratsioonipakkuja hoidlate loendi.</span><span class="sxs-lookup"><span data-stu-id="da7ce-174">You can now open the list of repositories for the Litware, Inc. configuration provider.</span></span>

10. <span data-ttu-id="da7ce-175">Valige **Avamine**.</span><span class="sxs-lookup"><span data-stu-id="da7ce-175">Select **Open**.</span></span>

    <span data-ttu-id="da7ce-176">Selle näite korral valige **LCS**-i hoidla ja avage see.</span><span class="sxs-lookup"><span data-stu-id="da7ce-176">For this example, select the **LCS** repository, and open it.</span></span>

    <span data-ttu-id="da7ce-177">Pange tähele, et valitud konfiguratsiooni näidatakse valitud LCS-i projekti varana.</span><span class="sxs-lookup"><span data-stu-id="da7ce-177">Notice that the selected configuration is shown as an asset of the selected LCS project.</span></span>

11. <span data-ttu-id="da7ce-178">Avage LCS, minnes saidile <https://lcs.dynamics.com>.</span><span class="sxs-lookup"><span data-stu-id="da7ce-178">Open LCS by going to <https://lcs.dynamics.com>.</span></span>
12. <span data-ttu-id="da7ce-179">Avage projekti, mida kasutati varem hoidla registreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="da7ce-179">Open a project that was used earlier for repository registration.</span></span>
13. <span data-ttu-id="da7ce-180">Avage projekti varade teek.</span><span class="sxs-lookup"><span data-stu-id="da7ce-180">Open the Asset library of the project.</span></span>
14. <span data-ttu-id="da7ce-181">Valige **GER-i konfiguratsiooni** vara tüüp.</span><span class="sxs-lookup"><span data-stu-id="da7ce-181">Select the **GER configuration** asset type.</span></span>

    <span data-ttu-id="da7ce-182">Teie üleslaaditud ER-konfiguratsioon peaks olema loetletud.</span><span class="sxs-lookup"><span data-stu-id="da7ce-182">The ER configuration that you uploaded should be listed.</span></span>

    <span data-ttu-id="da7ce-183">Pange tähele, et üleslaaditud LCS-i konfiguratsiooni saab importida teise eksemplari, kui teenuse pakkujatel on juurdepääs sellele LCS-i projektile.</span><span class="sxs-lookup"><span data-stu-id="da7ce-183">Note that the uploaded LCS configuration can be imported into another instance if providers have access to this LCS project.</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]