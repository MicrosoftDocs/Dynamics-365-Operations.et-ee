---
title: Rakendusekohaste metaandmete ettevalmistamine RCS-i ja ER-i jaoks
description: Selles teemas selgitatakse, kuidas valmistada ette rakendusespetsiifilisi metaandmeid Regulatiivse konfiguratsiooniteenuse (RCS) ja elektroonilise aruandluse (ER) jaoks.
author: NickSelin
manager: AnnBe
ms.date: 04/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: f15b78d3ed5b4df47540f9f89cc69c0b535a7241
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680190"
---
# <a name="prepare-application-specific-metadata-for-rcs-and-er"></a><span data-ttu-id="e7da1-103">Rakendusekohaste metaandmete ettevalmistamine RCS-i ja ER-i jaoks</span><span class="sxs-lookup"><span data-stu-id="e7da1-103">Prepare application-specific metadata for RCS and ER</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e7da1-104">See teema selgitab järgmiste ülesannete näiteid.</span><span class="sxs-lookup"><span data-stu-id="e7da1-104">This topic walks you through examples of the following tasks:</span></span>

- [<span data-ttu-id="e7da1-105">RCS-i jaoks kasutatavate rakenduse metaandmete ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="e7da1-105">Prepare application metadata that can be used in RCS</span></span>](#prepare-application-metadata-that-can-be-used-in-rcs)
- [<span data-ttu-id="e7da1-106">Juurdepääs rakenduse metaandmetele ER-konfiguratsiooni abil</span><span class="sxs-lookup"><span data-stu-id="e7da1-106">Access application metadata by using an ER configuration</span></span>](#access-application-metadata-by-using-an-er-configuration)
- [<span data-ttu-id="e7da1-107">Juurdepääs rakenduse metaandmetele ühendatud rakenduste abil</span><span class="sxs-lookup"><span data-stu-id="e7da1-107">Access application metadata by using connected applications</span></span>](#access-application-metadata-by-using-connected-applications)

## <a name="prepare-application-metadata-that-can-be-used-in-rcs"></a><span data-ttu-id="e7da1-108">RCS-i jaoks kasutatavate rakenduse metaandmete ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="e7da1-108">Prepare application metadata that can be used in RCS</span></span>

<span data-ttu-id="e7da1-109">Järgnev protseduur näitab, kuidas kasutaja, kelle rolliks on kas **Süsteemiadministraator** või **Elektroonilise aruandluse arendaja**, saab luua elektroonilise aruandluse (ER) konfiguratsiooni, mis sisaldab metaandmeid rakendusele ja mida kasutatakse elektroonilises aruandluses mudelivastenduse konfiguratsioonides Regulatory configuration service (RCS).</span><span class="sxs-lookup"><span data-stu-id="e7da1-109">The following procedure shows how a user who has the **System Administrator** or **Electronic Reporting Developer** role can create an Electronic reporting (ER) configuration that contains metadata for the application, and that is used to design ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="e7da1-110">Selles näites loodud elektroonilise aruandluse mudelivastenduse konfiguratsiooni näidist kasutatakse juurdepääsuks väliskaubanduse kannetele.</span><span class="sxs-lookup"><span data-stu-id="e7da1-110">The sample ER model mapping configuration that is created in this example will be used to access foreign trade transactions.</span></span>

<span data-ttu-id="e7da1-111">Selles näites soovite kasutada RCS-i sellise elektroonilise aruandluse lahenduse kavandamiseks rakendusele, mida kasutatakse väliskaubanduse äritegevuse domeeni teavet sisaldavate elektrooniliste dokumentide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="e7da1-111">For this example, you want to use RCS to design an ER solution for the application that will be used to generate electronic documents that contain information from the foreign trade business domain.</span></span> <span data-ttu-id="e7da1-112">ER-i andmemudeli ja nõutavate andmete allikate vahelise vastendamise määramiseks peab teil RCS-is olema ligipääs rakenduse metaandmetele.</span><span class="sxs-lookup"><span data-stu-id="e7da1-112">To specify the mapping between the ER data model and the sources of required data, you must have access to application metadata in RCS.</span></span> <span data-ttu-id="e7da1-113">Seega peate ER-lahenduse projekteerimise protsessi osana konfigureerima uue ER-i metaandmete konfiguratsiooni, mis sisaldab kõiki metaandmeid, mis on valitud äridomeeni ER-aruannete genereerimiseks praegu nõutavad.</span><span class="sxs-lookup"><span data-stu-id="e7da1-113">Therefore, as part of the process of designing the ER solution, you must configure a new ER metadata configuration that contains all the metadata that is currently required in order to generate ER reports for the selected business domain.</span></span>

> [!NOTE]
> <span data-ttu-id="e7da1-114">Selles näites loote konfiguratsiooni näidisettevõttele Litware, Inc. Neid etappe saab teha mis tahes ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="e7da1-114">In this example, you will create a configuration for the sample company, Litware, Inc. These steps can be performed in any company.</span></span>

1. <span data-ttu-id="e7da1-115">Avage **Organisatsiooni haldamine \> Tööruumid \> Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-115">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="e7da1-116">Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja märgitud kui **Aktiivne**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-116">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="e7da1-117">Kui te ei näe seda konfiguratsioonipakkujat, viige lõpuni toiming [Konfiguratsiooni pakkujate loomine ja nende aktiivseks märkimine](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="e7da1-117">If you don't see this configuration provider, complete the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> 
3. <span data-ttu-id="e7da1-118">Valige **Metaandmete konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-118">Select **Metadata configurations**.</span></span>
4. <span data-ttu-id="e7da1-119">Valige **Konfiguratsiooni loomine**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-119">Select **Create configuration**.</span></span>
5. <span data-ttu-id="e7da1-120">Dialoogiakna ripploendis sisestage nimi väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-120">In the drop-down dialog box, in the **Name** field, enter a name.</span></span> <span data-ttu-id="e7da1-121">Selle näite puhul sisestage **Väliskaubanduse metaandmed**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-121">For this example, enter **Foreign trade metadata**.</span></span>
6. <span data-ttu-id="e7da1-122">Valige **Konfiguratsiooni loomine**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-122">Select **Create configuration**.</span></span>
7. <span data-ttu-id="e7da1-123">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-123">Select **Designer**.</span></span>
8. <span data-ttu-id="e7da1-124">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-124">Select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e7da1-125">Saate valida kas kogu rakenduse või valitud mudelite või moodulite metaandmed.</span><span class="sxs-lookup"><span data-stu-id="e7da1-125">You can select all metadata either for the whole application, or for selected models or modules.</span></span> <span data-ttu-id="e7da1-126">Mõlemal juhul arvestage, et lisatakse automaatselt järgmised metaandmed: kirjete tabelid, loetelud ja laiendatud andmetüübid (EDT-d).</span><span class="sxs-lookup"><span data-stu-id="e7da1-126">In both cases, be aware that the following metadata will be automatically added: tables of records, enumerations, and extended data types (EDTs).</span></span> <span data-ttu-id="e7da1-127">Kui on vaja täiendavaid metaandmete tüüpe, tuleb need lisada käsitsi.</span><span class="sxs-lookup"><span data-stu-id="e7da1-127">When additional types of metadata are required, they must be manually added.</span></span>

    <span data-ttu-id="e7da1-128">Peate lisama metaandmeid, mis on seotud välikaubanduse kannetega ja valima käsitsi metaandmete üksused.</span><span class="sxs-lookup"><span data-stu-id="e7da1-128">You must add some metadata that is related to foreign trade transactions and manually select metadata items.</span></span>

9. <span data-ttu-id="e7da1-129">Valige **Andmeallika lisamine \> Tabeli kirjed**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-129">Select **Add data source \> Table records**.</span></span>
10. <span data-ttu-id="e7da1-130">Filter väärtusel **Intrastat** väljal **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-130">Filter on a value of **Intrastat** in the **Name** field.</span></span>
11. <span data-ttu-id="e7da1-131">Valige tabeli kirje **Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-131">Select the **Intrastat** table record.</span></span>
12. <span data-ttu-id="e7da1-132">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-132">Select **OK**.</span></span>

    <span data-ttu-id="e7da1-133">Peate lisama Intrastati kirjetabeli metaandmete teabe.</span><span class="sxs-lookup"><span data-stu-id="e7da1-133">You must add metadata information about the Intrastat table of records.</span></span>

13. <span data-ttu-id="e7da1-134">Tehke puul valik **Tabeli kirjete intrastat \> \>Seosed \> Intrastati kaubaartikkel (Tabeli kirjete EcoResCategory)**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-134">In the tree, select **Table records Intrastat \> \>Relations \> IntrastatCommodity (Table records EcoResCategory)**.</span></span>
14. <span data-ttu-id="e7da1-135">Valige **Lisa metaandmed**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-135">Select **Add metadata**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e7da1-136">Valitud kirjetabeli nõutavate seoste metaandmed tuleb lisada käsitsi.</span><span class="sxs-lookup"><span data-stu-id="e7da1-136">Metadata about required relations for the selected table of records must be added manually.</span></span>

15. <span data-ttu-id="e7da1-137">Valige **Andmeallika lisamine**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-137">Select **Add data source**.</span></span>
16. <span data-ttu-id="e7da1-138">Valige **Loetelu**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-138">Select **Enumeration**.</span></span>
17. <span data-ttu-id="e7da1-139">Filter väärtusel **IntrastatDirection** väljal **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-139">Filter on a value of **IntrastatDirection** in the **Name** field.</span></span>
18. <span data-ttu-id="e7da1-140">Valige loetelu kirje **IntrastatDirection**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-140">Select the **IntrastatDirection** enumeration record.</span></span>
19. <span data-ttu-id="e7da1-141">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-141">Select **OK**.</span></span>
20. <span data-ttu-id="e7da1-142">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-142">Select **Save**.</span></span>
21. <span data-ttu-id="e7da1-143">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e7da1-143">Close the page.</span></span>
22. <span data-ttu-id="e7da1-144">Täitke metaandmete konfiguratsiooni mustandversioon.</span><span class="sxs-lookup"><span data-stu-id="e7da1-144">Complete the draft version of the metadata configuration:</span></span>

    1. <span data-ttu-id="e7da1-145">Valige **Muuda olekut \> Lõpule viidud**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-145">Select **Change status \> Complete**.</span></span>
    2. <span data-ttu-id="e7da1-146">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-146">Select **OK**.</span></span>
    3. <span data-ttu-id="e7da1-147">Valige lõpule viidud versioon 1.</span><span class="sxs-lookup"><span data-stu-id="e7da1-147">Select the completed version 1.</span></span>

23. <span data-ttu-id="e7da1-148">Eksportige metaandmete konfiguratsiooni lõpule viidud versioon rakendusest XML-failina.</span><span class="sxs-lookup"><span data-stu-id="e7da1-148">Export the completed version of the metadata configuration from the application as an XML file:</span></span>

    1. <span data-ttu-id="e7da1-149">Valige **Exchange \> Eksporti XML-failina**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-149">Select **Exchange \> Export as XML file**.</span></span>
    2. <span data-ttu-id="e7da1-150">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-150">Select **OK**.</span></span>

<span data-ttu-id="e7da1-151">Teie loodud ER-i metaandmete konfiguratsioon salvestatakse failina **Väliskaubanduse metaandmed.xml**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-151">The ER metadata configuration that you created is saved as the **Foreign trade metadata.xml** file.</span></span> <span data-ttu-id="e7da1-152">Nüüd saate selle importida RCS-i, nii et seda saab kasutada väliskaubanduse äritegevuse äridomeeni metaandmete allikana.</span><span class="sxs-lookup"><span data-stu-id="e7da1-152">You can now import it into RCS, so that it can be used as the source of metadata for the foreign trade business domain.</span></span> <span data-ttu-id="e7da1-153">Selle teabe põhjal saate määratleda vastendamise rakenduse metaandmete ja ER-i andmemudeli vahel.</span><span class="sxs-lookup"><span data-stu-id="e7da1-153">Based on this information, you can specify the mapping between application metadata and the ER data model.</span></span>

## <a name="access-application-metadata-by-using-an-er-configuration"></a><span data-ttu-id="e7da1-154">Juurdepääs rakenduse metaandmetele ER-konfiguratsiooni abil</span><span class="sxs-lookup"><span data-stu-id="e7da1-154">Access application metadata by using an ER configuration</span></span>

<span data-ttu-id="e7da1-155">Järgmine protseduur näitab, kuidas RCS-i kasutaja, kelle roll on kas **Süsteemiadministraator** või **Elektroonilise aruandluse arendaja**, saab kavandada uue elektroonilise aruandluse mudeli vastenduse, kasutades rakenduse metaandmeid.</span><span class="sxs-lookup"><span data-stu-id="e7da1-155">The following procedure shows how an RCS user who has the **System Administrator** or **Electronic Reporting Developer** role can design a new ER model mapping by using metadata from the application.</span></span> <span data-ttu-id="e7da1-156">Rakenduse metaandmetele pääseb juurde elektroonilise aruandluse metaandmete konfiguratsiooni abil, mis sisaldab metaandmete nädiskomplekti juurdepääsuks väliskaubanduse kannetele.</span><span class="sxs-lookup"><span data-stu-id="e7da1-156">Application metadata will be accessed by using an ER metadata configuration that contains a sample set of metadata to access foreign trade transactions.</span></span>

<span data-ttu-id="e7da1-157">Enne selle protseduuri lõpule viimist peate esmalt viima lõpuni järgmised protseduurid.</span><span class="sxs-lookup"><span data-stu-id="e7da1-157">Before you can complete this procedure, you must first complete the following procedures:</span></span>

- [<span data-ttu-id="e7da1-158">Konfiguratsiooni pakkujate loomine ja nende märkimine aktiivseks</span><span class="sxs-lookup"><span data-stu-id="e7da1-158">Create configuration providers and mark them as active</span></span>](tasks/er-configuration-provider-mark-it-active-2016-11.md)
- [<span data-ttu-id="e7da1-159">RCS-i jaoks kasutatavate rakenduse metaandmete ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="e7da1-159">Prepare application metadata that can be used in RCS</span></span>](#prepare-application-metadata-that-can-be-used-in-rcs)

1. <span data-ttu-id="e7da1-160">Avage **Kõik tööruumid \> Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-160">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="e7da1-161">Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja märgitud kui **Aktiivne**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-161">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="e7da1-162">Kui te ei näe seda konfiguratsioonipakkujat, viige lõpuni toiming [Konfiguratsiooni pakkujate loomine ja nende aktiivseks märkimine](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="e7da1-162">If you don't see this configuration provider, complete the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> 
3. <span data-ttu-id="e7da1-163">Importige ER metaandmete konfiguratsioon, mis sisaldab metaandmeid rakendusele ja mis on konfigureeritud looma elektroonilisi dokumente väliskaubanduse äritegevuse domeenile.</span><span class="sxs-lookup"><span data-stu-id="e7da1-163">Import the ER metadata configuration that contains metadata for the application, and that is configured to generate electronic documents for the foreign trade business domain.</span></span> <span data-ttu-id="e7da1-164">Lõite selle elektroonilise aruandluse metaandmete konfiguratsiooni ja eksportisite selle XML-failina varem siin teemas olnud protseduuris [RCS-i jaoks kasutatavate rakenduse metaandmete ettevalmistamine](#prepare-application-metadata-that-can-be-used-in-rcs).</span><span class="sxs-lookup"><span data-stu-id="e7da1-164">You created this ER metadata configuration and exported it as an XML file in the [Prepare application metadata that can be used in RCS](#prepare-application-metadata-that-can-be-used-in-rcs) procedure earlier in this topic.</span></span>

    1. <span data-ttu-id="e7da1-165">Valige **Metaandmete konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-165">Select **Metadata configurations**.</span></span>
    2. <span data-ttu-id="e7da1-166">Valige **Exchange**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-166">Select **Exchange**.</span></span>
    3. <span data-ttu-id="e7da1-167">Valige **Laadi XML-failist**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-167">Select **Load from XML file**.</span></span>
    4. <span data-ttu-id="e7da1-168">Sirvige ja valige fail **Väliskaubanduse metaandmed.xml**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-168">Browse to select the **Foreign trade metadata.xml** file.</span></span>
    5. <span data-ttu-id="e7da1-169">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-169">Select **OK**.</span></span>
    6. <span data-ttu-id="e7da1-170">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e7da1-170">Close the page.</span></span>

4. <span data-ttu-id="e7da1-171">Looge andmemudeli konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="e7da1-171">Create a data model configuration:</span></span>

    1. <span data-ttu-id="e7da1-172">Valige **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-172">Select **Reporting configurations**.</span></span>
    2. <span data-ttu-id="e7da1-173">Valige **Konfiguratsiooni loomine**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-173">Select **Create configuration**.</span></span>
    3. <span data-ttu-id="e7da1-174">Sisestage ripploendi dialoogiaknasse väljale **Nimi** suvand **Väliskaubanduse mudel**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-174">In the drop-down dialog box, in the **Name** field, enter **Foreign trade model**.</span></span>
    4. <span data-ttu-id="e7da1-175">Valige **Konfiguratsiooni loomine**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-175">Select **Create configuration**.</span></span>
    5. <span data-ttu-id="e7da1-176">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-176">Select **Designer**.</span></span>
    6. <span data-ttu-id="e7da1-177">Rippdialoogi avamiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-177">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="e7da1-178">Väljale **Nimi** trükkige **Juur**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-178">In the **Name** field, type **Root**.</span></span>
        2. <span data-ttu-id="e7da1-179">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-179">Select **Add**.</span></span>
    
    7. <span data-ttu-id="e7da1-180">Rippdialoogi avamiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-180">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="e7da1-181">Väljale **Nimi** trükkige **Kanne**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-181">In the **Name** field, type **Transaction**.</span></span>
        2. <span data-ttu-id="e7da1-182">Valige väljalt **Üksuse tüüp** suvand **Kirjete loend**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-182">In the **Item type** field, select **Record list**.</span></span>
        3. <span data-ttu-id="e7da1-183">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-183">Select **Add**.</span></span>
 
    8. <span data-ttu-id="e7da1-184">Rippdialoogi avamiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-184">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="e7da1-185">Väljale **Nimi** trükkige **Kaubakood**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-185">In the **Name** field, type **Commodity code**.</span></span>
        2. <span data-ttu-id="e7da1-186">Valige väljalt **Üksuse tüüp** suvand **String**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-186">In the **Item type** field, select **String**.</span></span>
        3. <span data-ttu-id="e7da1-187">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-187">Select **Add**.</span></span>

    9. <span data-ttu-id="e7da1-188">Rippdialoogi avamiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-188">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="e7da1-189">Trükkige nimeväljale **Arveldatud summa**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-189">In the Name field, type **Invoiced amount**.</span></span>
        2. <span data-ttu-id="e7da1-190">Väljal **Üksuse tüüp** valige **Tegelik**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-190">In the **Item type** field, select **Real**.</span></span>
        3. <span data-ttu-id="e7da1-191">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-191">Select **Add**.</span></span>

    10. <span data-ttu-id="e7da1-192">Rippdialoogi avamiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-192">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="e7da1-193">Väljale **Nimi** trükkige **Kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-193">In the **Name** field, type **Date**.</span></span>
        2. <span data-ttu-id="e7da1-194">Väljalt **Üksuse tüüp** valige **Kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-194">In the **Item type** field, select **Date**.</span></span>
        3. <span data-ttu-id="e7da1-195">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-195">Select **Add**.</span></span>
 
    11. <span data-ttu-id="e7da1-196">Valige **Lisa \> Juure viide**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-196">Select **Add \> Root reference**.</span></span>
    12. <span data-ttu-id="e7da1-197">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-197">Select **OK**.</span></span>
    13. <span data-ttu-id="e7da1-198">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-198">Select **Save**.</span></span>
    14. <span data-ttu-id="e7da1-199">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e7da1-199">Close the page.</span></span>
    15. <span data-ttu-id="e7da1-200">Valige **Muuda olekut \> Lõpule viidud**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-200">Select **Change status \> Complete**.</span></span>
    16. <span data-ttu-id="e7da1-201">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-201">Select **OK**.</span></span>

5. <span data-ttu-id="e7da1-202">Looge mudelivastenduse konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="e7da1-202">Create a model mapping configuration:</span></span>

    1. <span data-ttu-id="e7da1-203">Valige **Konfiguratsiooni loomine**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-203">Select **Create configuration**.</span></span>
    2. <span data-ttu-id="e7da1-204">Sisestage ripploendi dialoogiaknasse väljale **Uus** suvand **Mudeli vastendamine väliskaubanduse mudeli andmemudeli põhjal**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-204">In the drop-down dialog box, in the **New** field, enter **Model Mapping based on data model Foreign trade model**.</span></span>
    3. <span data-ttu-id="e7da1-205">Sisestage väljale **Nimi** suvand **Väliskaubanduse vastendamine**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-205">In the **Name** field, enter **Foreign trade mapping**.</span></span>
    4. <span data-ttu-id="e7da1-206">Valige **Konfiguratsiooni loomine**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-206">Select **Create configuration**.</span></span>
    5. <span data-ttu-id="e7da1-207">Valige kiirkaardilt **Eeltingimused** suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-207">On the **Prerequisites** FastTab, select **Edit**.</span></span>
    6. <span data-ttu-id="e7da1-208">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-208">Select **New**.</span></span>
    7. <span data-ttu-id="e7da1-209">Valige väljalt **Eeltingimuse komponendi tüüp** suvand **Konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-209">In the **Prerequisite component type** field, select **Configuration**.</span></span>
    8. <span data-ttu-id="e7da1-210">Valige konfiguratsioon **Väliskaubanduse metaandmed**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-210">Select the **Foreign trade metadata** configuration.</span></span>
    9. <span data-ttu-id="e7da1-211">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-211">Select **Save**.</span></span> <span data-ttu-id="e7da1-212">Pange tähele et viide lisatakse konfiguratsiooni **Väliskaubanduse metaandmed** versioonile 1.</span><span class="sxs-lookup"><span data-stu-id="e7da1-212">Notice that the reference is added to version 1 of the **Foreign trade metadata** configuration.</span></span> <span data-ttu-id="e7da1-213">Mudeli vastenduse kavandamise ajal pakutakse rakenduse selle konfiguratsiooni metaandmeid.</span><span class="sxs-lookup"><span data-stu-id="e7da1-213">Application metadata from this configuration will be offered while the model mapping is designed.</span></span>
    10. <span data-ttu-id="e7da1-214">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e7da1-214">Close the page.</span></span>
    11. <span data-ttu-id="e7da1-215">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-215">Select **Designer**.</span></span>
    12. <span data-ttu-id="e7da1-216">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-216">Select **Designer**.</span></span>
    13. <span data-ttu-id="e7da1-217">Valige puul väärtus **Dynamics 365 for Operations \> Tabeli kirjed**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-217">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
    14. <span data-ttu-id="e7da1-218">Valige **Lisa juur**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-218">Select **Add root**.</span></span>
    15. <span data-ttu-id="e7da1-219">Sisestage väljale **Nimi** suvand **Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-219">In the **Name** field, enter **Intrastat**.</span></span>
    16. <span data-ttu-id="e7da1-220">Valige tabeli kirjed **Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-220">Select **Intrastat** table records.</span></span>
    17. <span data-ttu-id="e7da1-221">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-221">Select **OK**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="e7da1-222">Pakutakse ainult kahte tabelit, sest praegu kasutatavale metaandmete komplektile lisati ainult kaks tabelit.</span><span class="sxs-lookup"><span data-stu-id="e7da1-222">Only two tables are offered, because only two tables were added to the set of metadata that is currently used.</span></span>

    18. <span data-ttu-id="e7da1-223">Valige **Seo**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-223">Select **Bind**.</span></span>
    19. <span data-ttu-id="e7da1-224">Tehke puul valik **Intrastat \> AmountMST**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-224">In the tree, select **Intrastat \> AmountMST**.</span></span>
    20. <span data-ttu-id="e7da1-225">Tehke puul valik **Kanne = Intrastat \> Arveldatud summa**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-225">In the tree, select **Transaction = Intrastat \> Invoiced amount**.</span></span>
    21. <span data-ttu-id="e7da1-226">Valige **Seo**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-226">Select **Bind**.</span></span>
    22. <span data-ttu-id="e7da1-227">Tehke puul valik **Intrastat \> TransDate**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-227">In the tree, select **Intrastat \> TransDate**.</span></span>
    23. <span data-ttu-id="e7da1-228">Tehke puul valik **Kanne = Intrastat \> Kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-228">In the tree, select **Transaction = Intrastat \> Date**.</span></span>
    24. <span data-ttu-id="e7da1-229">Valige **Seo**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-229">Select **Bind**.</span></span>
    25. <span data-ttu-id="e7da1-230">Tehke puul valik **Intrastat \> \>Seosed \> IntrastatCommodity \> Kood**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-230">In the tree, select **Intrastat \> \>Relations \> IntrastatCommodity \> Code**.</span></span>
    26. <span data-ttu-id="e7da1-231">Tehke puul valik **Kanne = Intrastat \> Kaubakood**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-231">In the tree, select **Transaction = Intrastat \> Commodity code**.</span></span>
    27. <span data-ttu-id="e7da1-232">Valige **Seo**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-232">Select **Bind**.</span></span>
    28. <span data-ttu-id="e7da1-233">Valige **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-233">Select **Validate**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="e7da1-234">Pärast kinnitamise lõpuleviimist olete andmemudeli elemendid edukalt sidunud nende andmeallikate üksustega, mida on viidatud elektroonilise aruandluse metaandmete konfiguratsiooni rakenduse metaandmetega kirjeldatud.</span><span class="sxs-lookup"><span data-stu-id="e7da1-234">After validation is completed, you've successfully bound elements of the data model to items of the data sources that are described by using details of the application metadata from the referenced ER metadata configuration.</span></span>

    29. <span data-ttu-id="e7da1-235">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-235">Select **Save**.</span></span>

<span data-ttu-id="e7da1-236">Vajadusel saate laiendada rakenduses olemas olevat metaandmete komplekti.</span><span class="sxs-lookup"><span data-stu-id="e7da1-236">As you require, you can extend the existing set of metadata in the application.</span></span> <span data-ttu-id="e7da1-237">Seejärel saate uue lõpule viidud ER metaandmete konfiguratsiooni versiooni eksportida, importida selle RCS-sse ja värskendada konfigureeritud mudeli vastenduse konfiguratsiooni eeltingimusi viitama uuele imporditud metaandmete konfiguratsiooni versioonile.</span><span class="sxs-lookup"><span data-stu-id="e7da1-237">You can then export the new completed version of the ER metadata configuration, import it into RCS, and update the prerequisites of the configured model mapping configuration to refer to a new version of the imported metadata configuration.</span></span>

> [!NOTE]
> <span data-ttu-id="e7da1-238">See meetod rakenduse metaandmete kohta info saamiseks on ainuke saadaolev meetod rakendustele, mis arendatakse kohapeal (see tähendab, siis kui rakenduse jaoks kasutatakse kohalikke äriandmeid \[LBD\] või asutusesisese juurutuse mudelit.)</span><span class="sxs-lookup"><span data-stu-id="e7da1-238">This method for getting information about application metadata is the only available method for applications that are locally deployed (that is, when a local business data \[LBD\], or on-premises, deployment model is used for the application).</span></span>

## <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="e7da1-239">Juurdepääs rakenduse metaandmetele ühendatud rakenduste abil</span><span class="sxs-lookup"><span data-stu-id="e7da1-239">Access application metadata by using connected applications</span></span>

<span data-ttu-id="e7da1-240">Järgmine protseduur näitab, kuidas RCS-i kasutaja, kelle roll on kas **Süsteemiadministraator** või **Elektroonilise aruandluse arendaja**, saab kavandada uue elektroonilise aruandluse mudeli vastenduse, kasutades rakenduse metaandmeid.</span><span class="sxs-lookup"><span data-stu-id="e7da1-240">The following procedure shows how an RCS user who has the **System Administrator** or **Electronic Reporting Developer** role can design a new ER model mapping by using metadata of the application.</span></span> <span data-ttu-id="e7da1-241">Rakenduse metaandmete saab online-juurdepääsu RCS-ga ühendatud rakenduse abil.</span><span class="sxs-lookup"><span data-stu-id="e7da1-241">Application metadata will be accessed online by using RCS connected application.</span></span> <span data-ttu-id="e7da1-242">Väliskaubanduse kannetele juurdepääsuks konfigureeritakse elektroonilise aruandluse mudeli vastenduse näidis.</span><span class="sxs-lookup"><span data-stu-id="e7da1-242">A sample ER model mapping will be configured to access foreign trade transactions.</span></span>

<span data-ttu-id="e7da1-243">Selle protseduuri lõpuleviimiseks peate esmalt läbima RCS-is protseduuri [Konfiguratsiooni pakkujate loomine ja nende aktiivseks märkimine](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="e7da1-243">To complete this procedure, you must first complete the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure in RCS.</span></span> <span data-ttu-id="e7da1-244">Kui te ei ole protseduuri [Juurdepääs rakenduse metaandmetele ER-konfiguratsiooni abil](#access-application-metadata-by-using-an-er-configuration) selles teemas varem lõpule viinud, avage leht [Elektroonilise aruandluse tegevusjuhised rakendusele Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739), et laadida eelnevalt alla järgmised elektroonilise aruandluse konfiguratsioonifailid ja salvestada need kohapeal: **Väliskaubanduse metaandmed.xml**, **Väliskaubanduse mudel.xml** ja **Väliskaubanduse vastendamine.xml**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-244">If you haven't yet completed the [Access application metadata by using an ER configuration](#access-application-metadata-by-using-an-er-configuration) procedure earlier in this topic, go to [Electronic Reporting Task Guides for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) page to download the following ER configuration files in advance and save them locally: **Foreign trade metadata.xml**, **Foreign trade model.xml**, and **Foreign trade mapping.xml**.</span></span>


### <a name="get-required-er-configurations"></a><span data-ttu-id="e7da1-245">Vajalike elektroonilise aruandluse konfiguratsioonide hankimine</span><span class="sxs-lookup"><span data-stu-id="e7da1-245">Get required ER configurations</span></span>

<span data-ttu-id="e7da1-246">Kui olete varem selles teemas protseduuri [Juurdepääs rakenduse metaandmetele ER-konfiguratsiooni abil](#access-application-metadata-by-using-an-er-configuration) lõpule viinud, on teil praeguses RCS-i eksemplaris juba kõik vajalikud elektroonilise aruandluse konfiguratsioonid (väliskaubanduse metaandmete, mudeli ja vastenduse konfiguratsioonid).</span><span class="sxs-lookup"><span data-stu-id="e7da1-246">If you've already completed the [Access application metadata by using an ER configuration](#access-application-metadata-by-using-an-er-configuration) procedure earlier in this topic, you already have all the required ER configurations (the foreign trade metadata, model, and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="e7da1-247">Sellisel juhul võite selle protseduuri vahele jätta.</span><span class="sxs-lookup"><span data-stu-id="e7da1-247">In that case, you can skip this procedure.</span></span>

1. <span data-ttu-id="e7da1-248">Avage **Kõik tööruumid \> Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-248">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="e7da1-249">Valige **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-249">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="e7da1-250">Laadige konfiguratsioonifailid **Väliskaubanduse metaandmed.xml**, **Väliskaubanduse mudel.xml** ja **Väliskaubanduse vastendamine.xml** korrates neist igaühe korral järgmist etappide jada.</span><span class="sxs-lookup"><span data-stu-id="e7da1-250">Load the **Foreign trade metadata.xml**, **Foreign trade model.xml**, and **Foreign trade mapping.xml** configuration files repeating the following chain of steps for each of them:</span></span>

    1. <span data-ttu-id="e7da1-251">Valige **Exchange**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-251">Select **Exchange**.</span></span>
    2. <span data-ttu-id="e7da1-252">Valige **Laadi XML-failist**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-252">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="e7da1-253">Valige **Sirvi** ja valige fail.</span><span class="sxs-lookup"><span data-stu-id="e7da1-253">Select **Browse**, and select a file.</span></span>
    4. <span data-ttu-id="e7da1-254">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-254">Select **OK**.</span></span>

### <a name="register-the-connection-with-the-application"></a><span data-ttu-id="e7da1-255">Registreerige ühendus rakendusega</span><span class="sxs-lookup"><span data-stu-id="e7da1-255">Register the connection with the application</span></span>

1. <span data-ttu-id="e7da1-256">Avage **Kõik tööruumid \> Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-256">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="e7da1-257">Valige **Ühendatud rakendused**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-257">Select **Connected applications**.</span></span>
3. <span data-ttu-id="e7da1-258">Veenduge, et konfigureeritud rakendus on Microsoft Azure põhine ja et see on RCS-i kasutajatele üldiselt juurdepääsetav.</span><span class="sxs-lookup"><span data-stu-id="e7da1-258">Make sure that the configured application is based on Microsoft Azure, and that it is accessible in general to RCS users.</span></span> <span data-ttu-id="e7da1-259">Praegusel RCS-i kasutajal peab olema juurdepääs konfigureeritud rakendusele, mis registreeritakse selle rakenduse kasutajana rollis, mis annab talle õigused rakenduse mataandmetele juurdepääsuks.</span><span class="sxs-lookup"><span data-stu-id="e7da1-259">The current RCS user must have access to the configured application being registered as a user of this application in a role that gives them privileges to access the application's metadata.</span></span>
4. <span data-ttu-id="e7da1-260">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-260">Select **New**.</span></span>
5. <span data-ttu-id="e7da1-261">Sisestage väljale **Nimi** ühendatud rakenduse nimena suvand **MyConnectedApp**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-261">In the **Name** field, enter **MyConnectedApp** as the name of the connected application.</span></span>
6. <span data-ttu-id="e7da1-262">Määratlege väljal **Rakendus** rakenduse URL.</span><span class="sxs-lookup"><span data-stu-id="e7da1-262">In the **Application** field, specify the URL of the application.</span></span>
7. <span data-ttu-id="e7da1-263">Määratlege väljal **Rentnik** rakenduse pakkuja.</span><span class="sxs-lookup"><span data-stu-id="e7da1-263">In the **Tenant** field, specify the provider of the application.</span></span>
8. <span data-ttu-id="e7da1-264">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-264">Select **Save**.</span></span> 
9. <span data-ttu-id="e7da1-265">Kui kontrollite konfigureeritud rakenduse ühendust, valige lehel **Ühenda kaugrakendusega** link **Valige see valitud kaugrakendusega ühendamiseks**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-265">When you check the connection to the configured application, on the **Connect to remote application** page, select the **Select here to connect to selected remote application** link.</span></span> 
10. <span data-ttu-id="e7da1-266">Valige **Kontrolli ühendust**, et kontrollida juurdepääsu konfigureeritud rakendusele.</span><span class="sxs-lookup"><span data-stu-id="e7da1-266">Select **Check connection** to validate access to the configured application.</span></span>
11. <span data-ttu-id="e7da1-267">Valige suvand **Sule**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-267">Select **Close**.</span></span>

<span data-ttu-id="e7da1-268">Pärast seda, kui olete selle protseduuri lõpule viinud ja ühenduse kontrollimine on edukas, uuendatakse praeguses ruudustikus konfigureeritud rakenduse versioon ja rentniku andmed.</span><span class="sxs-lookup"><span data-stu-id="e7da1-268">After you complete this procedure and validation of the connection succeeds, the version and tenant details for the configured application will be updated in the current grid.</span></span>

### <a name="review-the-existing-model-mapping-configuration"></a><span data-ttu-id="e7da1-269">Olemasoleva mudelivastenduse üle vaatamine</span><span class="sxs-lookup"><span data-stu-id="e7da1-269">Review the existing model mapping configuration</span></span>

1. <span data-ttu-id="e7da1-270">Avage **Kõik tööruumid \> Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-270">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="e7da1-271">Valige **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-271">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="e7da1-272">valige puul väärtus **Väliskaubanduse mudel \> Väliskaubanduse vastendamine**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-272">In the tree, select **Foreign trade model \> Foreign trade mapping**.</span></span>
4. <span data-ttu-id="e7da1-273">Valige kiirkaart **Eeltingimused**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-273">Select the **Prerequisites** FasTab.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e7da1-274">Praegu viitab see vastendamine metaandmete konfiguratsioonile.</span><span class="sxs-lookup"><span data-stu-id="e7da1-274">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="e7da1-275">Selle konfiguratsiooni rakenduse metaandmeid pakutakse selle mudeli vastendamise kavandamise ajal.</span><span class="sxs-lookup"><span data-stu-id="e7da1-275">Application metadata from this configuration will be offered while this model mapping is designed.</span></span>

4. <span data-ttu-id="e7da1-276">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-276">Select **Designer**.</span></span>
5. <span data-ttu-id="e7da1-277">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-277">Select **Designer**.</span></span>
6. <span data-ttu-id="e7da1-278">Valige puul väärtus **Dynamics 365 for Operations \> Tabeli kirjed**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-278">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
7. <span data-ttu-id="e7da1-279">Valige **Lisa juur**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-279">Select **Add root**.</span></span>
8. <span data-ttu-id="e7da1-280">Sisestage või valige väärtus väljalt **Tabel**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-280">In the **Table** field, enter or select a value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e7da1-281">Praegu viitab see vastendamine metaandmete konfiguratsioonile.</span><span class="sxs-lookup"><span data-stu-id="e7da1-281">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="e7da1-282">Selle konfiguratsiooni rakenduse metaandmeid pakutakse selle mudeli vastendamise kavandamise ajal.</span><span class="sxs-lookup"><span data-stu-id="e7da1-282">Application metadata from this configuration will be offered while this model mapping is designed.</span></span>

9. <span data-ttu-id="e7da1-283">Valige **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-283">Select **Cancel**.</span></span>

### <a name="assign-the-connected-application-to-a-model-mapping"></a><span data-ttu-id="e7da1-284">Määrake ühendatud rakendus mudelivastendusele</span><span class="sxs-lookup"><span data-stu-id="e7da1-284">Assign the connected application to a model mapping</span></span>

1. <span data-ttu-id="e7da1-285">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-285">Select **Edit**.</span></span>
2. <span data-ttu-id="e7da1-286">Valige väljal **Ühendatud rakenduse väli** rakendus **MyConnectedApp**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-286">In the **Connected application field**, select the **MyConnectedApp** application.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e7da1-287">See vastendamine viitab valitud ühendatud rakenduse metaandmetele.</span><span class="sxs-lookup"><span data-stu-id="e7da1-287">This mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="e7da1-288">Kui vastendamine viitab metaandmete konfiguratsioonile ja ühendatud rakendusele samaaegselt, kasutatakse ühendatud rakenduse metaandmeid.</span><span class="sxs-lookup"><span data-stu-id="e7da1-288">If a mapping refers to the metadata configuration and the connected application at the same time, the metadata of the connected application will be used.</span></span>

3. <span data-ttu-id="e7da1-289">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-289">Select **Designer**.</span></span>
4. <span data-ttu-id="e7da1-290">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-290">Select **Designer**.</span></span>
5. <span data-ttu-id="e7da1-291">Valige puul väärtus **Dynamics 365 for Operations \> Tabeli kirjed**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-291">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
6. <span data-ttu-id="e7da1-292">Valige **Lisa juur**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-292">Select **Add root**.</span></span>
7. <span data-ttu-id="e7da1-293">Sisestage või valige väärtus väljalt **Tabel**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-293">In the **Table** field, enter or select a value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e7da1-294">Sel hetkel pakutakse rohkem kui kahte rakenduse tabelit, sest see vastendamine kasutab kõiki sellele määratud ühendatud rakenduse metaandmeid.</span><span class="sxs-lookup"><span data-stu-id="e7da1-294">At this point, more than two application tables are offered, because this mapping uses all the metadata of the connected application that has been assigned to it.</span></span>

8. <span data-ttu-id="e7da1-295">Valige **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-295">Select **Cancel**.</span></span>
9. <span data-ttu-id="e7da1-296">Valige **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-296">Select **Validate**.</span></span>

<span data-ttu-id="e7da1-297">Olete nüüd andmemudeli elemendid edukalt sidunud nende andmeallikate üksustega, mida on kirjeldatud kasutades sellele vastendusele määratud ühendatud rakenduse metaandmete üksikasju.</span><span class="sxs-lookup"><span data-stu-id="e7da1-297">You've now bound elements of the data model to items of the data sources that are described by using details of the metadata of the connected application that has been assigned to this mapping.</span></span>

<span data-ttu-id="e7da1-298">Kui peate hindama seda mudeli vastendust, kasutades rakenduse teise versiooni metaandmeid, registreerige teine ühendatud rakendus, määrake see mudeli vastendamiseks ja kinnitage see uute metaandmetega.</span><span class="sxs-lookup"><span data-stu-id="e7da1-298">When you must evaluate this model mapping by using the metadata of a different version of the application, register another connected application, assign it to this model mapping, and validate it against the new metadata.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e7da1-299">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="e7da1-299">Additional resources</span></span>

<span data-ttu-id="e7da1-300">Teise võimalusena saate esitada rakenduse ülesande juhise **RCS-i jaoks kasutatavate rakenduse metaandmete ettevalmistamine** ja ka RCS-i ülesande juhised **Juurdepääs rakenduse metaandmetele ER-konfiguratsiooni abil** ja **Juurdepääs rakenduse metaandmetele ühendatud rakenduste abil**.</span><span class="sxs-lookup"><span data-stu-id="e7da1-300">Alternatively, you can play the **Prepare application metadata that can be used in RCS** task guide in the application as as well as the **Access application metadata by using an ER configuration** and **Access application metadata by using connected applications** task guides in RCS.</span></span> <span data-ttu-id="e7da1-301">Need ülesande juhised saab alla laadida lehelt [Elektroonilise aruandluse ülesande juhised rakendusele Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739).</span><span class="sxs-lookup"><span data-stu-id="e7da1-301">These task guides can be downloaded from the [Electronic Reporting Task Guides for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) page.</span></span>
