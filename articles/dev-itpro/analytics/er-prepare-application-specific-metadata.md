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
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 289f901501a68319c9d85e993d8dfbfc3838a8eb
ms.sourcegitcommit: d940c7892b6caa6141b3bda8abf1c56e9df4687a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/03/2019
ms.locfileid: "1726428"
---
# <a name="prepare-application-specific-metadata-for-rcs"></a><span data-ttu-id="13d38-103">Rakendusekohaste metaandmete ettevalmistamine RCS-i jaoks</span><span class="sxs-lookup"><span data-stu-id="13d38-103">Prepare application-specific metadata for RCS</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="13d38-104">See teema selgitab järgmiste ülesannete näiteid.</span><span class="sxs-lookup"><span data-stu-id="13d38-104">This topic walks you through examples of the following tasks:</span></span>

- [<span data-ttu-id="13d38-105">RCS-i jaoks kasutatavate rakenduse metaandmete ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="13d38-105">Prepare application metadata that can be used in RCS</span></span>](#prepare-application-metadata-that-can-be-used-in-rcs)
- [<span data-ttu-id="13d38-106">Juurdepääs rakenduse metaandmetele ER-konfiguratsiooni abil</span><span class="sxs-lookup"><span data-stu-id="13d38-106">Access application metadata by using an ER configuration</span></span>](#access-application-metadata-by-using-an-er-configuration)
- [<span data-ttu-id="13d38-107">Juurdepääs rakenduse metaandmetele ühendatud rakenduste abil</span><span class="sxs-lookup"><span data-stu-id="13d38-107">Access application metadata by using connected applications</span></span>](#access-application-metadata-by-using-connected-applications)

## <a name="prepare-application-metadata-that-can-be-used-in-rcs"></a><span data-ttu-id="13d38-108">RCS-i jaoks kasutatavate rakenduse metaandmete ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="13d38-108">Prepare application metadata that can be used in RCS</span></span>

<span data-ttu-id="13d38-109">Järgneb protseduur näitab, kudas Finance and Operationsi kasutaja, kelle rolliks on kas **Süsteemi administraator** või **Elektroonilise aruandluse arendaja**, saab luua elektroonilise aruandluse (ER) konfiguratsiooni, mis sisaldab metaandmeid rakendusele Microsoft Dynamics 365 for Finance and Operations ja mida kasutatakse elektroonilise aruandlues mudelivastenduse konfiguratsioonides teenuses Regulatory configuration service (RCS).</span><span class="sxs-lookup"><span data-stu-id="13d38-109">The following procedure shows how a user of Finance and Operations who has the **System Administrator** or **Electronic Reporting Developer** role can create an Electronic reporting (ER) configuration that contains metadata for the Microsoft Dynamics 365 for Finance and Operations application, and that is used to design ER model mapping configurations in Regulatory configuration service (RCS).</span></span> <span data-ttu-id="13d38-110">Selles näites loodud elektroonilise aruandluse mudelivastenduse konfiguratsiooni näidist kasutatakse juurdepääsuks väliskaubanduse kannetele.</span><span class="sxs-lookup"><span data-stu-id="13d38-110">The sample ER model mapping configuration that is created in this example will be used to access foreign trade transactions.</span></span>

<span data-ttu-id="13d38-111">Selles näites soovite kasutada RCS-i rakendusele Finance and Operations sellise elektroonilise aurandluse lahenduse kavandamiseks, mida kasutatakse väliskaubanduse äritegevuse domeeni teavet sisaldavate elektrooniliste dokumentide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="13d38-111">For this example, you want to use RCS to design an ER solution for Finance and Operations that will be used to generate electronic documents that contain information from the foreign trade business domain.</span></span> <span data-ttu-id="13d38-112">ER-i andmemudeli ja nõutavate andmete allikate vahelise vastendamise määramiseks peab teil RCS-is olema ligipääs rakenduse Finance and Operations metaandmetele.</span><span class="sxs-lookup"><span data-stu-id="13d38-112">To specify the mapping between the ER data model and the sources of required data, you must have access to application metadata for Finance and Operations in RCS.</span></span> <span data-ttu-id="13d38-113">Seega peate ER-lahenduse projekteerimise protsessi osana konfigureerima uue ER-i metaandmete konfiguratsiooni, mis sisaldab kõiki metaandmeid, mis on valitud äridomeeni ER-aruannete genereerimiseks praegu nõutavad.</span><span class="sxs-lookup"><span data-stu-id="13d38-113">Therefore, as part of the process of designing the ER solution, you must configure a new ER metadata configuration that contains all the metadata that is currently required in order to generate ER reports for the selected business domain.</span></span>

> [!NOTE]
> <span data-ttu-id="13d38-114">Selles näites loote konfiguratsiooni näidisettevõttele Litware, Inc. Neid etappe saab teha mis tahes ettevõttes.</span><span class="sxs-lookup"><span data-stu-id="13d38-114">In this example, you will create a configuration for the sample company, Litware, Inc. These steps can be performed in any company.</span></span>

1. <span data-ttu-id="13d38-115">Avage **Organisatsiooni haldamine \> Tööruumid \> Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="13d38-115">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="13d38-116">Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja märgitud kui **Aktiivne**.</span><span class="sxs-lookup"><span data-stu-id="13d38-116">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="13d38-117">Kui te ei näe seda konfiguratsioonipakkujat, viige lõpuni toiming [Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="13d38-117">If you don't see this configuration provider, complete the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> 
3. <span data-ttu-id="13d38-118">Valige **Metaandmete konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="13d38-118">Select **Metadata configurations**.</span></span>
4. <span data-ttu-id="13d38-119">Valige **Konfiguratsiooni loomine**.</span><span class="sxs-lookup"><span data-stu-id="13d38-119">Select **Create configuration**.</span></span>
5. <span data-ttu-id="13d38-120">Dialoogiakna ripploendis sisestage nimi väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="13d38-120">In the drop-down dialog box, in the **Name** field, enter a name.</span></span> <span data-ttu-id="13d38-121">Selle näite puhul sisestage **Väliskaubanduse metaandmed**.</span><span class="sxs-lookup"><span data-stu-id="13d38-121">For this example, enter **Foreign trade metadata**.</span></span>
6. <span data-ttu-id="13d38-122">Valige **Konfiguratsiooni loomine**.</span><span class="sxs-lookup"><span data-stu-id="13d38-122">Select **Create configuration**.</span></span>
7. <span data-ttu-id="13d38-123">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="13d38-123">Select **Designer**.</span></span>
8. <span data-ttu-id="13d38-124">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="13d38-124">Select **Add**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="13d38-125">Saate valida kas kogu rakenduse või valitud mudelite või moodulite metaandmed.</span><span class="sxs-lookup"><span data-stu-id="13d38-125">You can select all metadata either for the whole application, or for selected models or modules.</span></span> <span data-ttu-id="13d38-126">Mõlemal juhul arvestage, et lisatakse automaatselt järgmised metaandmed: kirjete tabelid, loetelud ja laiendatud andmetüübid (EDT-d).</span><span class="sxs-lookup"><span data-stu-id="13d38-126">In both cases, be aware that the following metadata will be automatically added: tables of records, enumerations, and extended data types (EDTs).</span></span> <span data-ttu-id="13d38-127">Kui on vaja täiendavaid metaandmete tüüpe, tuleb need lisada käsitsi.</span><span class="sxs-lookup"><span data-stu-id="13d38-127">When additional types of metadata are required, they must be manually added.</span></span>

<span data-ttu-id="13d38-128">Peate lisama metaandmeid, mis on seotud välikaubanduse kannetega ja valima käsitsi metaandmete üksused.</span><span class="sxs-lookup"><span data-stu-id="13d38-128">You must add some metadata that is related to foreign trade transactions and manually select metadata items.</span></span>

9. <span data-ttu-id="13d38-129">Valige **Andmeallika lisamine \> Tabeli kirjed**.</span><span class="sxs-lookup"><span data-stu-id="13d38-129">Select **Add data source \> Table records**.</span></span>
10. <span data-ttu-id="13d38-130">Filter väärtusel **Intrastat** väljal **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="13d38-130">Filter on a value of **Intrastat** in the **Name** field.</span></span>
11. <span data-ttu-id="13d38-131">Valige tabeli kirje **Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="13d38-131">Select the **Intrastat** table record.</span></span>
12. <span data-ttu-id="13d38-132">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="13d38-132">Select **OK**.</span></span>

<span data-ttu-id="13d38-133">Peate lisama Intrastati kirjetabeli metaandmete teabe.</span><span class="sxs-lookup"><span data-stu-id="13d38-133">You must add metadata information about the Intrastat table of records.</span></span>

13. <span data-ttu-id="13d38-134">Tehke puul valik **Tabeli kirjete intrastat \> \>Seosed \> Intrastati kaubaartikkel (Tabeli kirjete EcoResCategory)**.</span><span class="sxs-lookup"><span data-stu-id="13d38-134">In the tree, select **Table records Intrastat \> \>Relations \> IntrastatCommodity (Table records EcoResCategory)**.</span></span>
14. <span data-ttu-id="13d38-135">Valige **Lisa metaandmed**.</span><span class="sxs-lookup"><span data-stu-id="13d38-135">Select **Add metadata**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="13d38-136">Valitud kirjetabeli nõutavate seoste metaandmed tuleb lisada käsitsi.</span><span class="sxs-lookup"><span data-stu-id="13d38-136">Metadata about required relations for the selected table of records must be added manually.</span></span>

15. <span data-ttu-id="13d38-137">Valige **Andmeallika lisamine**.</span><span class="sxs-lookup"><span data-stu-id="13d38-137">Select **Add data source**.</span></span>
16. <span data-ttu-id="13d38-138">Valige **Loetelu**.</span><span class="sxs-lookup"><span data-stu-id="13d38-138">Select **Enumeration**.</span></span>
17. <span data-ttu-id="13d38-139">Filter väärtusel **IntrastatDirection** väljal **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="13d38-139">Filter on a value of **IntrastatDirection** in the **Name** field.</span></span>
18. <span data-ttu-id="13d38-140">Valige loetelu kirje **IntrastatDirection**.</span><span class="sxs-lookup"><span data-stu-id="13d38-140">Select the **IntrastatDirection** enumeration record.</span></span>
19. <span data-ttu-id="13d38-141">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="13d38-141">Select **OK**.</span></span>
20. <span data-ttu-id="13d38-142">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="13d38-142">Select **Save**.</span></span>
21. <span data-ttu-id="13d38-143">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="13d38-143">Close the page.</span></span>
22. <span data-ttu-id="13d38-144">Täitke metaandmete konfiguratsiooni mustandversioon.</span><span class="sxs-lookup"><span data-stu-id="13d38-144">Complete the draft version of the metadata configuration:</span></span>

    1. <span data-ttu-id="13d38-145">Valige **Muuda olekut \> Lõpule viidud**.</span><span class="sxs-lookup"><span data-stu-id="13d38-145">Select **Change status \> Complete**.</span></span>
    2. <span data-ttu-id="13d38-146">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="13d38-146">Select **OK**.</span></span>
    3. <span data-ttu-id="13d38-147">Valige lõpule viidud versioon 1.</span><span class="sxs-lookup"><span data-stu-id="13d38-147">Select the completed version 1.</span></span>

23. <span data-ttu-id="13d38-148">Eksportige metaandmete konfiguratsiooni lõpule viidud versioon rakendusest XML-failina.</span><span class="sxs-lookup"><span data-stu-id="13d38-148">Export the completed version of the metadata configuration from the application as an XML file:</span></span>

    1. <span data-ttu-id="13d38-149">Valige **Exchange \> Eksporti XML-failina**.</span><span class="sxs-lookup"><span data-stu-id="13d38-149">Select **Exchange \> Export as XML file**.</span></span>
    2. <span data-ttu-id="13d38-150">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="13d38-150">Select **OK**.</span></span>

<span data-ttu-id="13d38-151">Teie loodud ER-i metaandmete konfiguratsioon salvestatakse failina **Väliskaubanduse metaandmed.xml**.</span><span class="sxs-lookup"><span data-stu-id="13d38-151">The ER metadata configuration that you created is saved as the **Foreign trade metadata.xml** file.</span></span> <span data-ttu-id="13d38-152">Nüüd saate selle importida RCS-i, nii et seda saab kasutada väliskaubanduse äritegevuse äridomeeni metaandmete allikana rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="13d38-152">You can now import it into RCS, so that it can be used as the source of metadata for the foreign trade business domain in Finance and Operations.</span></span> <span data-ttu-id="13d38-153">Selle teabe põhjal saate määratleda vastendamise rakenduse metaandmete ja ER-i andmemudeli vahel.</span><span class="sxs-lookup"><span data-stu-id="13d38-153">Based on this information, you can specify the mapping between application metadata and the ER data model.</span></span>

## <a name="access-application-metadata-by-using-an-er-configuration"></a><span data-ttu-id="13d38-154">Juurdepääs rakenduse metaandmetele ER-konfiguratsiooni abil</span><span class="sxs-lookup"><span data-stu-id="13d38-154">Access application metadata by using an ER configuration</span></span>

<span data-ttu-id="13d38-155">Järgmine protseduur näitab, kuidas RCS-i kasutaja, kelle roll on kas **Süsteemi administraator** või **Eelktroonilise aruandluse arendaja**, saab kavandada uue elektroonilise aruandluse mudeli vastenduse, kasutades rakenduse Finance and Operations metaandmeid.</span><span class="sxs-lookup"><span data-stu-id="13d38-155">The following procedure shows how an RCS user who has the **System Administrator** or **Electronic Reporting Developer** role can design a new ER model mapping by using metadata from the Finance and Operations application.</span></span> <span data-ttu-id="13d38-156">Rakenduse metaandmetele pääseb juurde elektroonilise aruandluse metaandmete konfiguratsiooni abil, mis sisaldab metaandmete nädiskomplekti juurdepääsuks väliskaubanduse kannetele.</span><span class="sxs-lookup"><span data-stu-id="13d38-156">Application metadata will be accessed by using an ER metadata configuration that contains a sample set of metadata to access foreign trade transactions.</span></span>

<span data-ttu-id="13d38-157">Enne selle protseduuri lõpule viimist peate esmalt viima lõpuni järgmised protseduurid.</span><span class="sxs-lookup"><span data-stu-id="13d38-157">Before you can complete this procedure, you must first complete the following procedures:</span></span>

- [<span data-ttu-id="13d38-158">Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks</span><span class="sxs-lookup"><span data-stu-id="13d38-158">Create a configuration provider and mark it as active</span></span>](tasks/er-configuration-provider-mark-it-active-2016-11.md)
- [<span data-ttu-id="13d38-159">RCS-i jaoks kasutatavate rakenduse metaandmete ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="13d38-159">Prepare application metadata that can be used in RCS</span></span>](#prepare-application-metadata-that-can-be-used-in-rcs)

1. <span data-ttu-id="13d38-160">Avage **Kõik tööruumid \> Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="13d38-160">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="13d38-161">Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja märgitud kui **Aktiivne**.</span><span class="sxs-lookup"><span data-stu-id="13d38-161">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as **Active**.</span></span> <span data-ttu-id="13d38-162">Kui te ei näe seda konfiguratsioonipakkujat, viige lõpuni toiming [Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="13d38-162">If you don't see this configuration provider, complete the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span> 
3. <span data-ttu-id="13d38-163">Importige ER metaandmete konfiguratsioon, mis sisaldab metaandmeid rakendusele Finance and Operations, ja mis on konfigureeritud looma elektroonilisi dokumente väliskaubanduse äritegevuse domeenile.</span><span class="sxs-lookup"><span data-stu-id="13d38-163">Import the ER metadata configuration that contains metadata for the Finance and Operations application, and that is configured to generate electronic documents for the foreign trade business domain.</span></span> <span data-ttu-id="13d38-164">Lõite selle elektroonilise aruandluse metaandmete konfiguratsiooni ja eksportisite selle XML-failina varem siin teemas olnud protseduuris [RCS-i jaoks kasutatavate rakenduse metaandmete ettevalmistamine](#prepare-application-metadata-that-can-be-used-in-rcs).</span><span class="sxs-lookup"><span data-stu-id="13d38-164">You created this ER metadata configuration and exported it as an XML file in the [Prepare application metadata that can be used in RCS](#prepare-application-metadata-that-can-be-used-in-rcs) procedure earlier in this topic.</span></span>

    1. <span data-ttu-id="13d38-165">Valige **Metaandmete konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="13d38-165">Select **Metadata configurations**.</span></span>
    2. <span data-ttu-id="13d38-166">Valige **Exchange**.</span><span class="sxs-lookup"><span data-stu-id="13d38-166">Select **Exchange**.</span></span>
    3. <span data-ttu-id="13d38-167">Valige **Laadi XML-failist**.</span><span class="sxs-lookup"><span data-stu-id="13d38-167">Select **Load from XML file**.</span></span>
    4. <span data-ttu-id="13d38-168">Sirvige ja valige fail **Väliskaubanduse metaandmed.xml**.</span><span class="sxs-lookup"><span data-stu-id="13d38-168">Browse to select the **Foreign trade metadata.xml** file.</span></span>
    5. <span data-ttu-id="13d38-169">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="13d38-169">Select **OK**.</span></span>
    6. <span data-ttu-id="13d38-170">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="13d38-170">Close the page.</span></span>

4. <span data-ttu-id="13d38-171">Looge andmemudeli konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="13d38-171">Create a data model configuration:</span></span>

    1. <span data-ttu-id="13d38-172">Valige **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="13d38-172">Select **Reporting configurations**.</span></span>
    2. <span data-ttu-id="13d38-173">Valige **Konfiguratsiooni loomine**.</span><span class="sxs-lookup"><span data-stu-id="13d38-173">Select **Create configuration**.</span></span>
    3. <span data-ttu-id="13d38-174">Sisestage ripploendi dialoogiaknasse väljale **Nimi** suvand **Väliskaubanduse mudel**.</span><span class="sxs-lookup"><span data-stu-id="13d38-174">In the drop-down dialog box, in the **Name** field, enter **Foreign trade model**.</span></span>
    4. <span data-ttu-id="13d38-175">Valige **Konfiguratsiooni loomine**.</span><span class="sxs-lookup"><span data-stu-id="13d38-175">Select **Create configuration**.</span></span>
    5. <span data-ttu-id="13d38-176">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="13d38-176">Select **Designer**.</span></span>
    6. <span data-ttu-id="13d38-177">Rippdialoogi avamiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="13d38-177">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="13d38-178">Väljale **Nimi** trükkige **Juur**.</span><span class="sxs-lookup"><span data-stu-id="13d38-178">In the **Name** field, type **Root**.</span></span>
        2. <span data-ttu-id="13d38-179">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="13d38-179">Select **Add**.</span></span>
    
    7. <span data-ttu-id="13d38-180">Rippdialoogi avamiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="13d38-180">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="13d38-181">Väljale **Nimi** trükkige **Kanne**.</span><span class="sxs-lookup"><span data-stu-id="13d38-181">In the **Name** field, type **Transaction**.</span></span>
        2. <span data-ttu-id="13d38-182">Valige väljalt **Üksuse tüüp** suvand **Kirjete loend**.</span><span class="sxs-lookup"><span data-stu-id="13d38-182">In the **Item type** field, select **Record list**.</span></span>
        3. <span data-ttu-id="13d38-183">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="13d38-183">Select **Add**.</span></span>
 
    8. <span data-ttu-id="13d38-184">Rippdialoogi avamiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="13d38-184">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="13d38-185">Väljale **Nimi** trükkige **Kaubakood**.</span><span class="sxs-lookup"><span data-stu-id="13d38-185">In the **Name** field, type **Commodity code**.</span></span>
        2. <span data-ttu-id="13d38-186">Valige väljalt **Üksuse tüüp** suvand **String**.</span><span class="sxs-lookup"><span data-stu-id="13d38-186">In the **Item type** field, select **String**.</span></span>
        3. <span data-ttu-id="13d38-187">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="13d38-187">Select **Add**.</span></span>

    9. <span data-ttu-id="13d38-188">Rippdialoogi avamiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="13d38-188">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="13d38-189">Trükkige nimeväljale **Arveldatud summa**.</span><span class="sxs-lookup"><span data-stu-id="13d38-189">In the Name field, type **Invoiced amount**.</span></span>
        2. <span data-ttu-id="13d38-190">Väljal **Üksuse tüüp** valige **Tegelik**.</span><span class="sxs-lookup"><span data-stu-id="13d38-190">In the **Item type** field, select **Real**.</span></span>
        3. <span data-ttu-id="13d38-191">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="13d38-191">Select **Add**.</span></span>

    10. <span data-ttu-id="13d38-192">Rippdialoogi avamiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="13d38-192">Select **New** to open the drop dialog.</span></span>

        1. <span data-ttu-id="13d38-193">Väljale **Nimi** trükkige **Kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="13d38-193">In the **Name** field, type **Date**.</span></span>
        2. <span data-ttu-id="13d38-194">Väljalt **Üksuse tüüp** valige **Kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="13d38-194">In the **Item type** field, select **Date**.</span></span>
        3. <span data-ttu-id="13d38-195">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="13d38-195">Select **Add**.</span></span>
 
    11. <span data-ttu-id="13d38-196">Valige **Lisa \> Juure viide**.</span><span class="sxs-lookup"><span data-stu-id="13d38-196">Select **Add \> Root reference**.</span></span>
    12. <span data-ttu-id="13d38-197">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="13d38-197">Select **OK**.</span></span>
    13. <span data-ttu-id="13d38-198">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="13d38-198">Select **Save**.</span></span>
    14. <span data-ttu-id="13d38-199">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="13d38-199">Close the page.</span></span>
    15. <span data-ttu-id="13d38-200">Valige **Muuda olekut \> Lõpule viidud**.</span><span class="sxs-lookup"><span data-stu-id="13d38-200">Select **Change status \> Complete**.</span></span>
    16. <span data-ttu-id="13d38-201">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="13d38-201">Select **OK**.</span></span>

5. <span data-ttu-id="13d38-202">Looge mudelivastenduse konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="13d38-202">Create a model mapping configuration:</span></span>

    1. <span data-ttu-id="13d38-203">Valige **Konfiguratsiooni loomine**.</span><span class="sxs-lookup"><span data-stu-id="13d38-203">Select **Create configuration**.</span></span>
    2. <span data-ttu-id="13d38-204">Sisestage ripploendi dialoogiaknasse väljale **Uus** suvand **Mudeli vastendamine väliskaubanduse mudeli andmemudeli põhjal**.</span><span class="sxs-lookup"><span data-stu-id="13d38-204">In the drop-down dialog box, in the **New** field, enter **Model Mapping based on data model Foreign trade model**.</span></span>
    3. <span data-ttu-id="13d38-205">Sisestage väljale **Nimi** suvand **Väliskaubanduse vastendamine**.</span><span class="sxs-lookup"><span data-stu-id="13d38-205">In the **Name** field, enter **Foreign trade mapping**.</span></span>
    4. <span data-ttu-id="13d38-206">Valige **Konfiguratsiooni loomine**.</span><span class="sxs-lookup"><span data-stu-id="13d38-206">Select **Create configuration**.</span></span>
    5. <span data-ttu-id="13d38-207">Valige kiirkaardilt **Eeltingimused** suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="13d38-207">On the **Prerequisites** FastTab, select **Edit**.</span></span>
    6. <span data-ttu-id="13d38-208">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="13d38-208">Select **New**.</span></span>
    7. <span data-ttu-id="13d38-209">Valige väljalt **Eeltingimuse komponendi tüüp** suvand **Konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="13d38-209">In the **Prerequisite component type** field, select **Configuration**.</span></span>
    8. <span data-ttu-id="13d38-210">Valige konfiguratsioon **Väliskaubanduse metaandmed**.</span><span class="sxs-lookup"><span data-stu-id="13d38-210">Select the **Foreign trade metadata** configuration.</span></span>
    9. <span data-ttu-id="13d38-211">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="13d38-211">Select **Save**.</span></span> <span data-ttu-id="13d38-212">Pange tähele et viide lisatakse konfiguratsiooni **Väliskaubanduse metaandmed** versioonile 1.</span><span class="sxs-lookup"><span data-stu-id="13d38-212">Notice that the reference is added to version 1 of the **Foreign trade metadata** configuration.</span></span> <span data-ttu-id="13d38-213">Mudeli vastenduse kavandamise ajal pakutakse rakenduse selle konfiguratsiooni metaandmeid.</span><span class="sxs-lookup"><span data-stu-id="13d38-213">Application metadata from this configuration will be offered while the model mapping is designed.</span></span>
    10. <span data-ttu-id="13d38-214">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="13d38-214">Close the page.</span></span>
    11. <span data-ttu-id="13d38-215">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="13d38-215">Select **Designer**.</span></span>
    12. <span data-ttu-id="13d38-216">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="13d38-216">Select **Designer**.</span></span>
    13. <span data-ttu-id="13d38-217">Valige puul väärtus **Dynamics 365 for Operations \> Tabeli kirjed**.</span><span class="sxs-lookup"><span data-stu-id="13d38-217">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
    14. <span data-ttu-id="13d38-218">Valige **Lisa juur**.</span><span class="sxs-lookup"><span data-stu-id="13d38-218">Select **Add root**.</span></span>
    15. <span data-ttu-id="13d38-219">Sisestage väljale **Nimi** suvand **Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="13d38-219">In the **Name** field, enter **Intrastat**.</span></span>
    16. <span data-ttu-id="13d38-220">Valige tabeli kirjed **Intrastat**.</span><span class="sxs-lookup"><span data-stu-id="13d38-220">Select **Intrastat** table records.</span></span>
    17. <span data-ttu-id="13d38-221">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="13d38-221">Select **OK**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="13d38-222">Pakutakse ainult kahte tabelit, sest praegu kasutatavale metaandmete komplektile lisati ainult kaks tabelit.</span><span class="sxs-lookup"><span data-stu-id="13d38-222">Only two tables are offered, because only two tables were added to the set of metadata that is currently used.</span></span>

    18. <span data-ttu-id="13d38-223">Valige **Seo**.</span><span class="sxs-lookup"><span data-stu-id="13d38-223">Select **Bind**.</span></span>
    19. <span data-ttu-id="13d38-224">Tehke puul valik **Intrastat \> AmountMST**.</span><span class="sxs-lookup"><span data-stu-id="13d38-224">In the tree, select **Intrastat \> AmountMST**.</span></span>
    20. <span data-ttu-id="13d38-225">Tehke puul valik **Kanne = Intrastat \> Arveldatud summa**.</span><span class="sxs-lookup"><span data-stu-id="13d38-225">In the tree, select **Transaction = Intrastat \> Invoiced amount**.</span></span>
    21. <span data-ttu-id="13d38-226">Valige **Seo**.</span><span class="sxs-lookup"><span data-stu-id="13d38-226">Select **Bind**.</span></span>
    22. <span data-ttu-id="13d38-227">Tehke puul valik **Intrastat \> TransDate**.</span><span class="sxs-lookup"><span data-stu-id="13d38-227">In the tree, select **Intrastat \> TransDate**.</span></span>
    23. <span data-ttu-id="13d38-228">Tehke puul valik **Kanne = Intrastat \> Kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="13d38-228">In the tree, select **Transaction = Intrastat \> Date**.</span></span>
    24. <span data-ttu-id="13d38-229">Valige **Seo**.</span><span class="sxs-lookup"><span data-stu-id="13d38-229">Select **Bind**.</span></span>
    25. <span data-ttu-id="13d38-230">Tehke puul valik **Intrastat \> \>Seosed \> IntrastatCommodity \> Kood**.</span><span class="sxs-lookup"><span data-stu-id="13d38-230">In the tree, select **Intrastat \> \>Relations \> IntrastatCommodity \> Code**.</span></span>
    26. <span data-ttu-id="13d38-231">Tehke puul valik **Kanne = Intrastat \> Kaubakood**.</span><span class="sxs-lookup"><span data-stu-id="13d38-231">In the tree, select **Transaction = Intrastat \> Commodity code**.</span></span>
    27. <span data-ttu-id="13d38-232">Valige **Seo**.</span><span class="sxs-lookup"><span data-stu-id="13d38-232">Select **Bind**.</span></span>
    28. <span data-ttu-id="13d38-233">Valige **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="13d38-233">Select **Validate**.</span></span>

        > [!NOTE]
        > <span data-ttu-id="13d38-234">Pärast kinnitamise lõpuleviimist olete andmemudeli elemendid edukalt sidunud nende andmeallikate üksustega, mida on viidatud elektroonilise aruandluse metaandmete konfiguratsiooni rakenduse metaandmetega kirjeldatud.</span><span class="sxs-lookup"><span data-stu-id="13d38-234">After validation is completed, you've successfully bound elements of the data model to items of the data sources that are described by using details of the application metadata from the referenced ER metadata configuration.</span></span>

    29. <span data-ttu-id="13d38-235">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="13d38-235">Select **Save**.</span></span>

<span data-ttu-id="13d38-236">Vajadusel saate laiendada rakenduses Finance and Operations olemas olevat metaandmete komplekti.</span><span class="sxs-lookup"><span data-stu-id="13d38-236">As you require, you can extend the existing set of metadata in Finance and Operations.</span></span> <span data-ttu-id="13d38-237">Seejärel saate uue lõpule viidud ER metaandmete konfiguratsiooni versiooni rakendusest Finance and Operations eksportida, importida selle RCS-sse ja värskendada konfigureeritud mudeli vastenduse konfiguratsiooni eeltingimusi viitama uuele imporditud metaandmete konfiguratsiooni versioonile.</span><span class="sxs-lookup"><span data-stu-id="13d38-237">You can then export the new completed version of the ER metadata configuration from Finance and Operations, import it into RCS, and update the prerequisites of the configured model mapping configuration to refer to a new version of the imported metadata configuration.</span></span>

> [!NOTE]
> <span data-ttu-id="13d38-238">See meetod rakenduse metaandmete kohta info saamiseks on ainuke saadaolev meetod rakendustele, mis arendatakse kohapeal (see tähendab, siis kui rakenduse Finance and Operations jaoks kasutatakse kohalikke äriandmeid \[LBD\] või asutusesisese juurutuse mudelit.)</span><span class="sxs-lookup"><span data-stu-id="13d38-238">This method for getting information about application metadata is the only available method for applications that are locally deployed (that is, when a local business data \[LBD\], or on-premises, deployment model is used for Finance and Operations).</span></span>

## <a name="access-application-metadata-by-using-connected-applications"></a><span data-ttu-id="13d38-239">Juurdepääs rakenduse metaandmetele ühendatud rakenduste abil</span><span class="sxs-lookup"><span data-stu-id="13d38-239">Access application metadata by using connected applications</span></span>

<span data-ttu-id="13d38-240">Järgmine protseduur näitab, kuidas RCS-i kasutaja, kelle roll on kas **Süsteemi administraator** või **Eelktroonilise aruandluse arendaja**, saab kavandada uue elektroonilise aruandluse mudeli vastenduse, kasutades rakenduse Finance and Operations metaandmeid.</span><span class="sxs-lookup"><span data-stu-id="13d38-240">The following procedure shows how an RCS user who has the **System Administrator** or **Electronic Reporting Developer** role can design a new ER model mapping by using metadata of the Finance and Operations application.</span></span> <span data-ttu-id="13d38-241">Rakenduse metaandmete saab online-juurdepääsu RCS-ga ühendatud rakenduse abil.</span><span class="sxs-lookup"><span data-stu-id="13d38-241">Application metadata will be accessed online by using RCS connected application.</span></span> <span data-ttu-id="13d38-242">Väliskaubanduse kannetele juurdepääsuks konfigureeritakse elektroonilise aruandluse mudeli vastenduse näidis.</span><span class="sxs-lookup"><span data-stu-id="13d38-242">A sample ER model mapping will be configured to access foreign trade transactions.</span></span>

<span data-ttu-id="13d38-243">Selle protseduuri lõpuleviimiseks peate esmalt läbima RCS-is protseduuri [Konfiguratsioonipakkuja loomine ja selle märkimine aktiivseks](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="13d38-243">To complete this procedure, you must first complete the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure in RCS.</span></span> <span data-ttu-id="13d38-244">Kui te ei ole protseduuri [Juurdepääs rakenduse metaandmetele ER-konfiguratsiooni abil](#access-application-metadata-by-using-an-er-configuration) selles teemas varem lõpule viinud, avage leht [Elektroonilise aruandluse tegevusjuhised rakendusele Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739), et laadida eelnevalt alla järgmised elektroonilise aruandluse konfiguratsioonifailid ja salvestada need kohapeal: **Väliskaubanduse metaandmed.xml**, **Väliskaubanduse mudel.xml** ja **Väliskaubanduse vastendamine.xml**.</span><span class="sxs-lookup"><span data-stu-id="13d38-244">If you haven't yet completed the [Access application metadata by using an ER configuration](#access-application-metadata-by-using-an-er-configuration) procedure earlier in this topic, go to [Electronic Reporting Task Guides for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) page to download the following ER configuration files in advance and save them locally: **Foreign trade metadata.xml**, **Foreign trade model.xml**, and **Foreign trade mapping.xml**.</span></span>


### <a name="get-required-er-configurations"></a><span data-ttu-id="13d38-245">Vajalike elektroonilise aruandluse konfiguratsioonide hankimine</span><span class="sxs-lookup"><span data-stu-id="13d38-245">Get required ER configurations</span></span>

<span data-ttu-id="13d38-246">Kui olete varem selles teemas protseduuri [Juurdepääs rakenduse metaandmetele ER-konfiguratsiooni abil](#access-application-metadata-by-using-an-er-configuration) lõpule viinud, on teil praeguses RCS-i eksemplaris juba kõik vajalikud elektroonilise aruandluse konfiguratsioonid (väliskaubanduse metaandmete, mudeli ja vastenduse konfiguratsioonid).</span><span class="sxs-lookup"><span data-stu-id="13d38-246">If you've already completed the [Access application metadata by using an ER configuration](#access-application-metadata-by-using-an-er-configuration) procedure earlier in this topic, you already have all the required ER configurations (the foreign trade metadata, model, and mapping configurations) in the current RCS instance.</span></span> <span data-ttu-id="13d38-247">Sellisel juhul võite selle protseduuri vahele jätta.</span><span class="sxs-lookup"><span data-stu-id="13d38-247">In that case, you can skip this procedure.</span></span>

1. <span data-ttu-id="13d38-248">Avage **Kõik tööruumid \> Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="13d38-248">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="13d38-249">Valige **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="13d38-249">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="13d38-250">Laadige konfiguratsioonifailid **Väliskaubanduse metaandmed.xml**, **Väliskaubanduse mudel.xml** ja **Väliskaubanduse vastendamine.xml** korrates neist igaühe korral järgmist etappide jada.</span><span class="sxs-lookup"><span data-stu-id="13d38-250">Load the **Foreign trade metadata.xml**, **Foreign trade model.xml**, and **Foreign trade mapping.xml** configuration files repeating the following chain of steps for each of them:</span></span>

    1. <span data-ttu-id="13d38-251">Valige **Exchange**.</span><span class="sxs-lookup"><span data-stu-id="13d38-251">Select **Exchange**.</span></span>
    2. <span data-ttu-id="13d38-252">Valige **Laadi XML-failist**.</span><span class="sxs-lookup"><span data-stu-id="13d38-252">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="13d38-253">Valige **Sirvi** ja valige fail.</span><span class="sxs-lookup"><span data-stu-id="13d38-253">Select **Browse**, and select a file.</span></span>
    4. <span data-ttu-id="13d38-254">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="13d38-254">Select **OK**.</span></span>

### <a name="register-the-connection-with-finance-and-operations"></a><span data-ttu-id="13d38-255">Registreerige ühendus rakendusega Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="13d38-255">Register the connection with Finance and Operations</span></span>

1. <span data-ttu-id="13d38-256">Avage **Kõik tööruumid \> Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="13d38-256">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="13d38-257">Valige **Ühendatud rakendused**.</span><span class="sxs-lookup"><span data-stu-id="13d38-257">Select **Connected applications**.</span></span>
3. <span data-ttu-id="13d38-258">Veenduge, et konfigureeritud rakendus on Microsoft Azure põhine ja et see on RCS-i kasutajatele üldiselt juurdepääsetav.</span><span class="sxs-lookup"><span data-stu-id="13d38-258">Make sure that the configured application is based on Microsoft Azure, and that it is accessible in general to RCS users.</span></span> <span data-ttu-id="13d38-259">Praegusel RCSi kasutajal peab olema juurdepääs konfigureeritud rakendusele, mis registreeritakse selle rakenduse kasutajana rollis, mis annab talle õigused rakenduse mataandmetele juurdepääsuks.</span><span class="sxs-lookup"><span data-stu-id="13d38-259">The current RCS user must have access to the configured application being registered as a user of this application in a role that gives him or her privileges to access the application's metadata.</span></span>
4. <span data-ttu-id="13d38-260">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="13d38-260">Select **New**.</span></span>
5. <span data-ttu-id="13d38-261">Sisestage väljale **Nimi** ühendatud rakenduse nimena suvand **MyConnectedApp**.</span><span class="sxs-lookup"><span data-stu-id="13d38-261">In the **Name** field, enter **MyConnectedApp** as the name of the connected application.</span></span>
6. <span data-ttu-id="13d38-262">Määratlege väljal **Rakendus** rakenduse URL.</span><span class="sxs-lookup"><span data-stu-id="13d38-262">In the **Application** field, specify the URL of the application.</span></span>
7. <span data-ttu-id="13d38-263">Määratlege väljal **Rentnik** rakenduse pakkuja.</span><span class="sxs-lookup"><span data-stu-id="13d38-263">In the **Tenant** field, specify the provider of the application.</span></span>
8. <span data-ttu-id="13d38-264">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="13d38-264">Select **Save**.</span></span> 
9. <span data-ttu-id="13d38-265">Kui kontrollite konfigureeritud rakenduse ühendust, valige lehel **Ühenda kaugrakendusega** link **Valige see valitud kaugrakendusega ühendamiseks**.</span><span class="sxs-lookup"><span data-stu-id="13d38-265">When you check the connection to the configured application, on the **Connect to remote application** page, select the **Select here to connect to selected remote application** link.</span></span> 
10. <span data-ttu-id="13d38-266">Valige **Kontrolli ühendust**, et kontrollida juurdepääsu konfigureeritud rakendusele.</span><span class="sxs-lookup"><span data-stu-id="13d38-266">Select **Check connection** to validate access to the configured application.</span></span>
11. <span data-ttu-id="13d38-267">Valige suvand **Sule**.</span><span class="sxs-lookup"><span data-stu-id="13d38-267">Select **Close**.</span></span>

<span data-ttu-id="13d38-268">Pärast seda, kui olete selle protseduuri lõpule viinud ja ühenduse kontrollimine on edukas, uuendatakse praeguses ruudustikus konfigureeritud rakenduse versioon ja rentniku andmed.</span><span class="sxs-lookup"><span data-stu-id="13d38-268">After you complete this procedure and validation of the connection succeeds, the version and tenant details for the configured application will be updated in the current grid.</span></span>

### <a name="review-the-existing-model-mapping-configuration"></a><span data-ttu-id="13d38-269">Olemasoleva mudelivastenduse üle vaatamine</span><span class="sxs-lookup"><span data-stu-id="13d38-269">Review the existing model mapping configuration</span></span>

1. <span data-ttu-id="13d38-270">Avage **Kõik tööruumid \> Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="13d38-270">Go to **All workspaces \> Electronic reporting**.</span></span>
2. <span data-ttu-id="13d38-271">Valige **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="13d38-271">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="13d38-272">valige puul väärtus **Väliskaubanduse mudel \> Väliskaubanduse vastendamine**.</span><span class="sxs-lookup"><span data-stu-id="13d38-272">In the tree, select **Foreign trade model \> Foreign trade mapping**.</span></span>
4. <span data-ttu-id="13d38-273">Valige kiirkaart **Eeltingimused**.</span><span class="sxs-lookup"><span data-stu-id="13d38-273">Select the **Prerequisites** FasTab.</span></span>

    > [!NOTE]
    > <span data-ttu-id="13d38-274">Praegu viitab see vastendamine metaandmete konfiguratsioonile.</span><span class="sxs-lookup"><span data-stu-id="13d38-274">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="13d38-275">Selle konfiguratsiooni rakenduse metaandmeid pakutakse selle mudeli vastendamise kavandamise ajal.</span><span class="sxs-lookup"><span data-stu-id="13d38-275">Application metadata from this configuration will be offered while this model mapping is designed.</span></span>

4. <span data-ttu-id="13d38-276">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="13d38-276">Select **Designer**.</span></span>
5. <span data-ttu-id="13d38-277">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="13d38-277">Select **Designer**.</span></span>
6. <span data-ttu-id="13d38-278">Valige puul väärtus **Dynamics 365 for Operations \> Tabeli kirjed**.</span><span class="sxs-lookup"><span data-stu-id="13d38-278">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
7. <span data-ttu-id="13d38-279">Valige **Lisa juur**.</span><span class="sxs-lookup"><span data-stu-id="13d38-279">Select **Add root**.</span></span>
8. <span data-ttu-id="13d38-280">Sisestage või valige väärtus väljalt **Tabel**.</span><span class="sxs-lookup"><span data-stu-id="13d38-280">In the **Table** field, enter or select a value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="13d38-281">Praegu viitab see vastendamine metaandmete konfiguratsioonile.</span><span class="sxs-lookup"><span data-stu-id="13d38-281">Currently, this mapping refers to the metadata configuration.</span></span> <span data-ttu-id="13d38-282">Selle konfiguratsiooni rakenduse metaandmeid pakutakse selle mudeli vastendamise kavandamise ajal.</span><span class="sxs-lookup"><span data-stu-id="13d38-282">Application metadata from this configuration will be offered while this model mapping is designed.</span></span>

9. <span data-ttu-id="13d38-283">Valige **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="13d38-283">Select **Cancel**.</span></span>

### <a name="assign-the-connected-application-to-a-model-mapping"></a><span data-ttu-id="13d38-284">Määrake ühendatud rakendus mudelivastendusele</span><span class="sxs-lookup"><span data-stu-id="13d38-284">Assign the connected application to a model mapping</span></span>

1. <span data-ttu-id="13d38-285">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="13d38-285">Select **Edit**.</span></span>
2. <span data-ttu-id="13d38-286">Valige väljal **Ühendatud rakenduse väli** rakendus **MyConnectedApp**.</span><span class="sxs-lookup"><span data-stu-id="13d38-286">In the **Connected application field**, select the **MyConnectedApp** application.</span></span>

    > [!NOTE]
    > <span data-ttu-id="13d38-287">See vastendamine viitab valitud ühendatud rakenduse metaandmetele.</span><span class="sxs-lookup"><span data-stu-id="13d38-287">This mapping refers to the metadata of the selected connected application.</span></span> <span data-ttu-id="13d38-288">Kui vastendamine viitab metaandmete konfiguratsioonile ja ühendatud rakendusele samaaegselt, kasutatakse ühendatud rakenduse metaandmeid.</span><span class="sxs-lookup"><span data-stu-id="13d38-288">If a mapping refers to the metadata configuration and the connected application at the same time, the metadata of the connected application will be used.</span></span>

3. <span data-ttu-id="13d38-289">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="13d38-289">Select **Designer**.</span></span>
4. <span data-ttu-id="13d38-290">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="13d38-290">Select **Designer**.</span></span>
5. <span data-ttu-id="13d38-291">Valige puul väärtus **Dynamics 365 for Operations \> Tabeli kirjed**.</span><span class="sxs-lookup"><span data-stu-id="13d38-291">In the tree, select **Dynamics 365 for Operations \> Table records**.</span></span>
6. <span data-ttu-id="13d38-292">Valige **Lisa juur**.</span><span class="sxs-lookup"><span data-stu-id="13d38-292">Select **Add root**.</span></span>
7. <span data-ttu-id="13d38-293">Sisestage või valige väärtus väljalt **Tabel**.</span><span class="sxs-lookup"><span data-stu-id="13d38-293">In the **Table** field, enter or select a value.</span></span>

    > [!NOTE]
    > <span data-ttu-id="13d38-294">Sel hetkel pakutakse rohkem kui kahte rakenduse tabelit, sest see vastendamine kasutab kõiki sellele määratud ühendatud rakenduse metaandmeid.</span><span class="sxs-lookup"><span data-stu-id="13d38-294">At this point, more than two application tables are offered, because this mapping uses all the metadata of the connected application that has been assigned to it.</span></span>

8. <span data-ttu-id="13d38-295">Valige **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="13d38-295">Select **Cancel**.</span></span>
9. <span data-ttu-id="13d38-296">Valige **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="13d38-296">Select **Validate**.</span></span>

<span data-ttu-id="13d38-297">Olete nüüd andmemudeli elemendid edukalt sidunud nende andmeallikate üksustega, mida on kirjeldatud kasutades sellele vastendusele määratud ühendatud rakenduse metaandmete üksikasju.</span><span class="sxs-lookup"><span data-stu-id="13d38-297">You've now bound elements of the data model to items of the data sources that are described by using details of the metadata of the connected application that has been assigned to this mapping.</span></span>

<span data-ttu-id="13d38-298">Kui peate hindama seda mudeli vastendust, kasutades rakenduse teise versiooni metaandmeid, registreerige teine ühendatud rakendus, määrake see mudeli vastendamiseks ja kinnitage see uute metaandmetega.</span><span class="sxs-lookup"><span data-stu-id="13d38-298">When you must evaluate this model mapping by using the metadata of a different version of the application, register another connected application, assign it to this model mapping, and validate it against the new metadata.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="13d38-299">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="13d38-299">Additional resources</span></span>

<span data-ttu-id="13d38-300">Teise võimalusena saate esitada Finance and Operationsi ülesande juhise **RCS-i jaoks kasutatavate rakenduse metaandmete ettevalmistamine** ja ka RCS-i ülesande juhised **Juurdepääs rakenduse metaandmetele ER-konfiguratsiooni abil** ja **Juurdepääs rakenduse metaandmetele ühendatud rakenduste abil**.</span><span class="sxs-lookup"><span data-stu-id="13d38-300">Alternatively, you can play the **Prepare application metadata that can be used in RCS** task guide in Finance and Operationsas as well as the **Access application metadata by using an ER configuration** and **Access application metadata by using connected applications** task guides in RCS.</span></span> <span data-ttu-id="13d38-301">Need ülesande juhised saab alla laadida lehelt [Elektroonilise aruandluse ülesande juhised rakendusele Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739).</span><span class="sxs-lookup"><span data-stu-id="13d38-301">These task guides can be downloaded from the [Electronic Reporting Task Guides for Dynamics 365 for Finance and Operations 8.1](https://go.microsoft.com/fwlink/?linkid=2082739) page.</span></span>
