---
title: ER-vormingute konfigureerimine juriidilise isiku kohta määratud parameetrite kasutamiseks
description: Selles teemas selgitatakse, kuidas saab konfigureerida elektroonilise aruandluse (ER) vorminguid juriidilise isiku kohta määratud parameetrite kasutamiseks.
author: NickSelin
manager: AnnBe
ms.date: 10/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: d32da76ee46ff5293ae8fefb16d251564b6be21a
ms.sourcegitcommit: d6196d83c7b9166ddb4fe43a91e6bd0ad9da2099
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/31/2019
ms.locfileid: "2694242"
---
# <a name="configure-er-formats-to-use-parameters-that-are-specified-per-legal-entity"></a><span data-ttu-id="ef787-103">ER-vormingute konfigureerimine juriidilise isiku kohta määratud parameetrite kasutamiseks</span><span class="sxs-lookup"><span data-stu-id="ef787-103">Configure ER formats to use parameters that are specified per legal entity</span></span>

[!include[banner](../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="ef787-104">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="ef787-104">Overview</span></span>

<span data-ttu-id="ef787-105">Paljudes elektroonilise aruandluse (ER) vormingutes, mida loote, peate andmeid filtreerima, kasutades väärtuste kogumit, mis on omane igale teie eksemplari juriidilisele isikule (nt maksukoodide kogum maksukannete filtreerimiseks).</span><span class="sxs-lookup"><span data-stu-id="ef787-105">In many of the Electronic reporting (ER) formats that you will design, you must filter data by using a set of values that are specific to each legal entity of your instance (for example, a set of tax codes to filter tax transactions).</span></span> <span data-ttu-id="ef787-106">Kui praegu on filtreerimine konfigureeritud ER-vormingus, kasutatakse andmete filtreerimisreeglite määratlemiseks ER-vormingu avaldistes väärtusi, mis sõltuvad juriidilisest isikust (nt maksukoode).</span><span class="sxs-lookup"><span data-stu-id="ef787-106">Currently, when filtering of this type is configured in an ER format, values that are dependent on the legal entity (for example, tax codes) are used in expressions of the ER format to specify data filtering rules.</span></span> <span data-ttu-id="ef787-107">Seetõttu on ER-vorming muudetud juriidilisele isikule omaseks, ja vajalike aruannete loomist peate looma tuletatud koopiad algsest ER-vormingust iga juriidilise isiku kohta, kus tuleb ER-vormingut käitada.</span><span class="sxs-lookup"><span data-stu-id="ef787-107">Therefore, the ER format is made legal entity–specific, and to generate the required reports, you must create derived copies of the original ER format for each legal entity where you have to run the ER format.</span></span> <span data-ttu-id="ef787-108">Iga tuletatud ER-vormingut tuleb redigeerida, et tuua sellesse juriidilise isiku põhised väärtused, muuta alust iga kord, kui algversiooni (alust) värskendatakse, eksportida katsekeskkonnast ja importida tootmiskeskkonda, kui see tuleb juurutada kasutamiseks tootmises, jne.</span><span class="sxs-lookup"><span data-stu-id="ef787-108">Each derived ER format must be edited to bring legal entity–specific values into it, rebased whenever the original (base) version has been updated, exported from a test environment and imported into a production environment when it must be deployed for production use, and so on.</span></span> <span data-ttu-id="ef787-109">Seetõttu on seda tüüpi konfigureeritud ER-lahenduse hooldus üsna keeruline ja aeganõudev mitmel põhjusel.</span><span class="sxs-lookup"><span data-stu-id="ef787-109">Therefore, maintenance of this type of configured ER solution is quite complex and time-consuming for several reasons:</span></span>

-   <span data-ttu-id="ef787-110">Mida rohkem on juriidilisi isikuid, seda rohkem ER-vormingu konfiguratsioone tuleb hooldada.</span><span class="sxs-lookup"><span data-stu-id="ef787-110">The more legal entities there are, the more ER format configurations must be maintained.</span></span>
-   <span data-ttu-id="ef787-111">ER-konfiguratsioonide hoolduseks peavad ärikasutajatel olema ER-alased teadmised.</span><span class="sxs-lookup"><span data-stu-id="ef787-111">Maintenance of ER configurations requires that business users have ER knowledge.</span></span>

<span data-ttu-id="ef787-112">ER-i rakendusepõhiste parameetrite funktsiooniga saavad lauskasutajad konfigureerida andmete filtreerimist ER-vormingus, nii et see põhineb abstraktsete reeglite kogumil.</span><span class="sxs-lookup"><span data-stu-id="ef787-112">The ER application-specific parameters feature lets power users configure data filtering in an ER format so that it's based on a set of abstract rules.</span></span> <span data-ttu-id="ef787-113">Seda reeglite kogumit saab konfigureerida ER-vormingus saadaolevate andmeallikate kasutamiseks.</span><span class="sxs-lookup"><span data-stu-id="ef787-113">This set of rules can be configured to use the data sources that are available in an ER format.</span></span> <span data-ttu-id="ef787-114">Ärikasutajad saavad määrata reaalseid reegleid väljaspool ER-raamistikku, kasutades kasutajaliidest (UI), mis luuakse automaatselt vastava ER-vormingu ja praeguse juriidilise isiku andmete põhjal, millele pääseb ligi ER-vorgmingu andmeallikatega.</span><span class="sxs-lookup"><span data-stu-id="ef787-114">Business users can then specify real rules beyond the ER framework by using the user interface (UI) that is automatically generated based on the settings of the corresponding ER format and the current legal entity data that will be accessed by the ER format's data sources.</span></span> <span data-ttu-id="ef787-115">ER-vormingu jaoks määratletud reeglite kogumit saab eksportida Dynamics 365 Finance’i (Finance) eksemplari praegusest juriidilisest isikust.</span><span class="sxs-lookup"><span data-stu-id="ef787-115">The set of rules that is specified for an ER format can be exported from the current legal entity of the Dynamics 365 Finance (Finance) instance.</span></span> <span data-ttu-id="ef787-116">Seda saab seejärel importida teise juriidilisse isikusse samas või mõnes teises Finance’i eksemplaris sama ER-vormingu reeglite kogumina.</span><span class="sxs-lookup"><span data-stu-id="ef787-116">It can then be imported into another legal entity of either the same Finance instance or a different instance as a set of rules for the same ER format.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ef787-117">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="ef787-117">Prerequisites</span></span>

<span data-ttu-id="ef787-118">Selle teema näidete läbimiseks peab teil ole juurdepääs teenuse Regulatory Configuration Services (RCS) eksemplarile, mis on eraldatud samale rentnikule kui rakendus Finance ühe järgmise rolli jaoks:</span><span class="sxs-lookup"><span data-stu-id="ef787-118">To complete the examples in this topic, you must have access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance for one of the following roles:</span></span>

- <span data-ttu-id="ef787-119">Elektroonilise aruandluse arendaja</span><span class="sxs-lookup"><span data-stu-id="ef787-119">Electronic reporting developer</span></span>
- <span data-ttu-id="ef787-120">Elektroonilise aruandluse funktsionaalne konsultant</span><span class="sxs-lookup"><span data-stu-id="ef787-120">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="ef787-121">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="ef787-121">System administrator</span></span>

<span data-ttu-id="ef787-122">Soovitame läbida etapid teemas [ARVUTATUD VÄLJATÜÜBI ER-andmeallikate parameetritega kõned](er-calculated-field-type.md).</span><span class="sxs-lookup"><span data-stu-id="ef787-122">We recommend that you complete the steps in the [Support parameterized calls of ER data sources of CALCULATED FIELD type](er-calculated-field-type.md) topic.</span></span> <span data-ttu-id="ef787-123">Kui olete need etapid juba läbinud, võite vahele jätta etapid järgmises jaotises **ER-konfiguratsioonide importimine RCS-i**.</span><span class="sxs-lookup"><span data-stu-id="ef787-123">If you've already completed those steps, you can skip the steps in the **Import ER configurations into RCS** section that follows.</span></span>

## <a name="import-er-configurations-into-rcs"></a><span data-ttu-id="ef787-124">ER-konfiguratsioonide importimine RCS-i</span><span class="sxs-lookup"><span data-stu-id="ef787-124">Import ER configurations into RCS</span></span>

<span data-ttu-id="ef787-125">Laadige [Microsofti allalaadimiskeskusest](https://go.microsoft.com/fwlink/?linkid=851448) alla tihendatud fail **ARVUTATUD VÄLJATÜÜBI ER-andmeallikate parameetritega kõned**.</span><span class="sxs-lookup"><span data-stu-id="ef787-125">From [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=851448), download the **Support parameterized calls of ER data sources of CALCULATED FIELD type** zip file.</span></span> <span data-ttu-id="ef787-126">See tihendatud fail sisaldab järgmisi ER-konfiguratsioone, mida tuleb kohapeal ekstraktida ja säilitada.</span><span class="sxs-lookup"><span data-stu-id="ef787-126">This zip file contains the following ER configurations that must be extracted and stored locally.</span></span>

| <span data-ttu-id="ef787-127">**Sisu kirjeldus**</span><span class="sxs-lookup"><span data-stu-id="ef787-127">**Content description**</span></span>                        | <span data-ttu-id="ef787-128">**Faili nimi**</span><span class="sxs-lookup"><span data-stu-id="ef787-128">**File name**</span></span>                                        |
|------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ef787-129">**ER-i andmemudeli** konfiguratsioonifaili näidis</span><span class="sxs-lookup"><span data-stu-id="ef787-129">Sample **ER data model** configuration file</span></span>    | <span data-ttu-id="ef787-130">Mudel parameetritega calls.version.1.xml õppimiseks</span><span class="sxs-lookup"><span data-stu-id="ef787-130">Model to learn parameterized calls.version.1.xml</span></span>     |
| <span data-ttu-id="ef787-131">**ER-i metaandmete** konfiguratsioonifaili näidis</span><span class="sxs-lookup"><span data-stu-id="ef787-131">Sample **ER metadata** configuration file</span></span>      | <span data-ttu-id="ef787-132">Metaandmed parameetritega calls.version.1.xml õppimiseks</span><span class="sxs-lookup"><span data-stu-id="ef787-132">Metadata to learn parameterized calls.version.1.xml</span></span>  |
| <span data-ttu-id="ef787-133">**ER-i mudelivastenduse** konfiguratsioonifaili näidis</span><span class="sxs-lookup"><span data-stu-id="ef787-133">Sample **ER model mapping** configuration file</span></span> | <span data-ttu-id="ef787-134">Vastendamine parameetritega calls.version.1.xml õppimiseks</span><span class="sxs-lookup"><span data-stu-id="ef787-134">Mapping to learn parameterized calls.version.1.1.xml</span></span> |
| <span data-ttu-id="ef787-135">**ER-vormingu** konfiguratsiooni näidis</span><span class="sxs-lookup"><span data-stu-id="ef787-135">Sample **ER format** configuration</span></span>             | <span data-ttu-id="ef787-136">Vorming parameetritega calls.version.1.xml õppimiseks</span><span class="sxs-lookup"><span data-stu-id="ef787-136">Format to learn parameterized calls.version.1.1.xml</span></span>  |

<span data-ttu-id="ef787-137">Järgmiseks logige sisse oma RCS-eksemplari.</span><span class="sxs-lookup"><span data-stu-id="ef787-137">Next, sign in to your RCS instance.</span></span>

<span data-ttu-id="ef787-138">Selles näites loote konfiguratsiooni näidisettevõttele Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="ef787-138">In this example, you will create a configuration for the Litware, Inc sample company.</span></span> <span data-ttu-id="ef787-139">Enne selle protseduuri läbimist peate läbima etapid RCS-i teemas [Konfiguratsioonipakkuja loomine ja selle märkimine aktiivseks](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="ef787-139">Before you can complete this procedure, you must complete the steps in the [Create a configuration provider and mark it as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) topic in RCS.</span></span>

1.  <span data-ttu-id="ef787-140">Valige vaikimisi armatuurlaual **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="ef787-140">On the default dashboard, select **Electronic reporting**.</span></span>
2.  <span data-ttu-id="ef787-141">Valige **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="ef787-141">Select **Reporting configurations**.</span></span>
3.  <span data-ttu-id="ef787-142">Importige varem allalaaditud ER-i konfiguratsioonid RCS-i järgmises järjekorras: andmemudel, metaandmed, mudeli vastendamine ja vorming.</span><span class="sxs-lookup"><span data-stu-id="ef787-142">Import the ER configurations that you downloaded earlier into RCS, in the following order: data model, metadata, model mapping, and format.</span></span> <span data-ttu-id="ef787-143">Tehke iga ER-i konfiguratsiooniga järgmist.</span><span class="sxs-lookup"><span data-stu-id="ef787-143">For each ER configuration, follow these steps:</span></span>

    1.  <span data-ttu-id="ef787-144">Valige **Exchange**.</span><span class="sxs-lookup"><span data-stu-id="ef787-144">Select **Exchange**.</span></span>
    2.  <span data-ttu-id="ef787-145">Valige **Laadi XML-failist**.</span><span class="sxs-lookup"><span data-stu-id="ef787-145">Select **Load from XML file**.</span></span>
    3.  <span data-ttu-id="ef787-146">Valige käsk **Sirvi**, et valida nõutava ER-i konfiguratsiooni jaoks XML-vormingus fail.</span><span class="sxs-lookup"><span data-stu-id="ef787-146">Select **Browse** to select the file for the required ER configuration in XML format.</span></span>
    4.  <span data-ttu-id="ef787-147">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef787-147">Select **OK**.</span></span>

## <a name="review-the-er-solution-that-is-provided"></a><span data-ttu-id="ef787-148">Vaadake läbi esitatud ER-lahendus</span><span class="sxs-lookup"><span data-stu-id="ef787-148">Review the ER solution that is provided</span></span>

1.  <span data-ttu-id="ef787-149">Laiendage konfiguratsioonipuus üksuse **Parameetritega kõnede õppimiseks kasutatava mudeli** sisu.</span><span class="sxs-lookup"><span data-stu-id="ef787-149">In the configuration tree, expand the contents of the **Model to learn parameterized calls** item.</span></span>
2.  <span data-ttu-id="ef787-150">Valige üksus **Vorming parameetritega kõnede õppimiseks**.</span><span class="sxs-lookup"><span data-stu-id="ef787-150">Select the **Format to learn parameterized calls** item.</span></span>
3.  <span data-ttu-id="ef787-151">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="ef787-151">Select **Designer**.</span></span>
4.  <span data-ttu-id="ef787-152">Valige **Laienda/ahenda**.</span><span class="sxs-lookup"><span data-stu-id="ef787-152">Select **Expand/Collapse**.</span></span>

    <span data-ttu-id="ef787-153">ER-vorming **Vorming parameetritega kõnede õppimiseks** on mõeldud XML-vormingus maksudeklaratsiooni loomiseks, millel kujutatakse mitut maksustamistaset (tavaline, vähendatud ja puudub).</span><span class="sxs-lookup"><span data-stu-id="ef787-153">The **Format to learn parameterized calls** ER format is designed to generate a tax statement in XML format that presents several levels of taxation (regular, reduced, and none).</span></span> <span data-ttu-id="ef787-154">Igal tasemel on erinev arv üksikasju.</span><span class="sxs-lookup"><span data-stu-id="ef787-154">Each level has a different number of details.</span></span>

    ![ER-i toimingu koostaja leht](./media/RCS-AppSpecParms-ReviewFormat.PNG)

5.  <span data-ttu-id="ef787-156">Laiendage vahekaardil **Vastendamine** üksusi **Mudel**, **Andmed** ja **Kokkuvõte**.</span><span class="sxs-lookup"><span data-stu-id="ef787-156">On the **Mapping** tab, expand the **Model**, **Data**, and **Summary** items.</span></span>

    <span data-ttu-id="ef787-157">Andmeallikas **Model.Data.Summary** tagastab maksukannete loendi.</span><span class="sxs-lookup"><span data-stu-id="ef787-157">The **Model.Data.Summary** data source returns the list of tax transactions.</span></span> <span data-ttu-id="ef787-158">Need kanded on kokku võetud maksukoodi järgi.</span><span class="sxs-lookup"><span data-stu-id="ef787-158">These transactions are summarized by tax code.</span></span> <span data-ttu-id="ef787-159">Selle andmeallika jaoks on arvutatud väli **Model.Data.Summary.Level** konfigureeritud tagastama iga kokku võetud kirje maksustamistaseme koodi.</span><span class="sxs-lookup"><span data-stu-id="ef787-159">For this data source, the **Model.Data.Summary.Level** calculated field has been configured to return the code for the taxation level of each summarized record.</span></span> <span data-ttu-id="ef787-160">Iga maksukoodi kohta, mida saab käitusajal tuua andmeallikast **Model.Data.Summary**, tagastab arvutatud väli maksustamistaseme koodi (**Tavaline**, **Vähendatud**, **Puudub** või **Muu**) tekstväärtusena.</span><span class="sxs-lookup"><span data-stu-id="ef787-160">For any tax code that can be retrieved from the **Model.Data.Summary** data source at runtime, the calculated field returns the taxation level code (**Regular**, **Reduced**, **None**, or **Other**) as a text value.</span></span> <span data-ttu-id="ef787-161">Arvutatud välja **Model.Data.Summary.Level** kasutatakse andmeallika **Model.Data.Summary** kirjete filtreerimiseks ja filtreeritud andmete sisestamiseks igasse XML-elementi, mis kujutavad maksustamistaset, kasutades välju **Model.Data2.Level1**, **Model.Data2.Level2** ja **Model.Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="ef787-161">The **Model.Data.Summary.Level** calculated field is used to filter records of the **Model.Data.Summary** data source and enter the filtered data in each XML element that represents a taxation level by using the **Model.Data2.Level1**, **Model.Data2.Level2**, and **Model.Data2.Level3** fields.</span></span>

    ![ER-i toimingu koostaja leht](./media/RCS-AppSpecParms-ReviewFormat-Data2Fld.PNG)

    <span data-ttu-id="ef787-163">Arvutatud väli **Model.Data.Summary.Level** on konfigureeritud nii, et see sisaldab ER-i avaldist.</span><span class="sxs-lookup"><span data-stu-id="ef787-163">The **Model.Data.Summary.Level** calculated field has been configured so that it contains an ER expression.</span></span> <span data-ttu-id="ef787-164">Pange tähele, et maksukoodid (**VAT19**, **InVAT19**, **VAT7**, **InVAT7**, **THIRD** ja **InVAT0**) on sellesse konfiguratsiooni püsiprogrammeeritud.</span><span class="sxs-lookup"><span data-stu-id="ef787-164">Note that tax codes (**VAT19**, **InVAT19**, **VAT7**, **InVAT7**, **THIRD**, and **InVAT0**) are hardcoded into this configuration.</span></span> <span data-ttu-id="ef787-165">Seetõttu oleneb see ER-vorming juriidilisest isikust, kus maksukoodid konfigureeriti.</span><span class="sxs-lookup"><span data-stu-id="ef787-165">Therefore, this ER format is dependent on the legal entity where these tax codes were configured.</span></span>

    ![ER-i toimingu koostaja leht](./media/RCS-AppSpecParms-ReviewFormat-LevelFld.PNG)

    <span data-ttu-id="ef787-167">Muu maksukoodide kogumi toetamiseks iga juriidilise isiku jaoks peate järgima järgmisi etappe.</span><span class="sxs-lookup"><span data-stu-id="ef787-167">To support a different set of tax codes for each legal entity, you must follow these steps:</span></span>

    - <span data-ttu-id="ef787-168">Looge ER-vormingust iga juriidilise isiku jaoks tuletatud versioon.</span><span class="sxs-lookup"><span data-stu-id="ef787-168">Create a derived version of the ER format for each legal entity.</span></span>
    - <span data-ttu-id="ef787-169">Värskendage maksukoode arvutatud väljas **Model.Data.Summary.Level**, lähtudes juriidilise isiku sättest.</span><span class="sxs-lookup"><span data-stu-id="ef787-169">Update the tax codes in the **Model.Data.Summary.Level** calculated field, based on the legal entity setting.</span></span>

6.  <span data-ttu-id="ef787-170">Sulgege **Vormingu koostaja** leht.</span><span class="sxs-lookup"><span data-stu-id="ef787-170">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="ef787-171">Tuletatud vormingu loomine</span><span class="sxs-lookup"><span data-stu-id="ef787-171">Create a derived format</span></span>

<span data-ttu-id="ef787-172">Järgmiseks kasutage ER-i rakendusepõhiste parameetrite funktsiooni, et toetada erinevaid maksukoodide kogumeid iga juriidilise isiku jaoks ühes ER-vormingus.</span><span class="sxs-lookup"><span data-stu-id="ef787-172">Next, you will use the ER application-specific parameters feature to support a different set of tax codes for each legal entity in a single ER format.</span></span>

1.  <span data-ttu-id="ef787-173">Laiendage konfiguratsioonipuus üksuse **Parameetritega kõnede õppimiseks kasutatava mudeli** sisu.</span><span class="sxs-lookup"><span data-stu-id="ef787-173">In the configuration tree, expand the contents of the **Model to learn parameterized calls** item.</span></span>
2.  <span data-ttu-id="ef787-174">Valige üksus **Vorming parameetritega kõnede õppimiseks**.</span><span class="sxs-lookup"><span data-stu-id="ef787-174">Select the **Format to learn parameterized calls** item.</span></span>
3.  <span data-ttu-id="ef787-175">Valige **Konfiguratsiooni loomine**.</span><span class="sxs-lookup"><span data-stu-id="ef787-175">Select **Create configuration**.</span></span>
4.  <span data-ttu-id="ef787-176">Valige suvand **Tuleta nimest: vorming parameetritega kõnede õppimiseks, Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="ef787-176">Select the **Derive from Name: Format to learn parameterized calls, Microsoft** option.</span></span>
5.  <span data-ttu-id="ef787-177">Sisestage väljale **Nimi** suvand **Vorming LE-andmete otsingu õppimiseks**.</span><span class="sxs-lookup"><span data-stu-id="ef787-177">In the **Name** field, enter **Format to learn how to lookup LE data**.</span></span>
6.  <span data-ttu-id="ef787-178">Valige **Konfiguratsiooni loomine**.</span><span class="sxs-lookup"><span data-stu-id="ef787-178">Select **Create configuration**.</span></span>

## <a name="configure-a-derived-format"></a><span data-ttu-id="ef787-179">Tuletatud vormingu konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="ef787-179">Configure a derived format</span></span>

### <a name="add-a-format-enumeration"></a><span data-ttu-id="ef787-180">Vormingu loetelu lisamine</span><span class="sxs-lookup"><span data-stu-id="ef787-180">Add a format enumeration</span></span>

<span data-ttu-id="ef787-181">Järgmiseks lisage uus ER-vormingu loetelu.</span><span class="sxs-lookup"><span data-stu-id="ef787-181">Next, you will add a new ER format enumeration.</span></span> <span data-ttu-id="ef787-182">Selle vormingu loetelu väärtused esitatakse ärikasutajatele, kes määravad juriidilise isikust sõltuvad maksukoodide kogumid mitmesuguste maksustamistasemete jaoks, mida ER-vormingus kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="ef787-182">The values of this format enumeration will be presented to business users, who will specify legal entity–dependent sets of tax codes for the various taxation levels that are used in the ER format.</span></span>

1.  <span data-ttu-id="ef787-183">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="ef787-183">Select **Designer**.</span></span>
2.  <span data-ttu-id="ef787-184">Valige suvand **Vormingu loetelud**.</span><span class="sxs-lookup"><span data-stu-id="ef787-184">Select **Format enumerations**.</span></span>
3.  <span data-ttu-id="ef787-185">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="ef787-185">Select **Add**.</span></span>
4.  <span data-ttu-id="ef787-186">Väljale **Nimi** sisestage väärtus **Maksustamistasemete loend**.</span><span class="sxs-lookup"><span data-stu-id="ef787-186">In the **Name** field, enter **List of taxation levels**.</span></span>
5.  <span data-ttu-id="ef787-187">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ef787-187">Select **Save**.</span></span>
6.  <span data-ttu-id="ef787-188">Vahekaardil **Vormingu loetelu väärtused** valige käsk **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="ef787-188">On the **Format enumeration values** tab, select **Add**.</span></span>
7.  <span data-ttu-id="ef787-189">Väljale **Nimi** sisestage väärtus **Tavaline maksustamine**.</span><span class="sxs-lookup"><span data-stu-id="ef787-189">In the **Name** field, enter **Regular taxation**.</span></span>
8.  <span data-ttu-id="ef787-190">Valige uuesti käsk **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="ef787-190">Select **Add** again.</span></span>
9.  <span data-ttu-id="ef787-191">Väljale **Nimi** sisestage väärtus **Vähendatud maksustamine**.</span><span class="sxs-lookup"><span data-stu-id="ef787-191">In the **Name** field, enter **Reduced taxation**.</span></span>
10. <span data-ttu-id="ef787-192">Valige uuesti käsk **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="ef787-192">Select **Add** again.</span></span>
11. <span data-ttu-id="ef787-193">Väljale **Nimi** sisestage väärtus **Maksustamine puudub**.</span><span class="sxs-lookup"><span data-stu-id="ef787-193">In the **Name** field, enter **No taxation**.</span></span>
12. <span data-ttu-id="ef787-194">Valige uuesti käsk **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="ef787-194">Select **Add** again.</span></span>
13. <span data-ttu-id="ef787-195">Väljale **Nimi** sisestage **Muu**.</span><span class="sxs-lookup"><span data-stu-id="ef787-195">In the **Name** field, enter **Other**.</span></span>

    ![ER-i toimingu koostaja leht](./media/RCS-AppSpecParms-ConfigureFormat-Enum.PNG)

    <span data-ttu-id="ef787-197">Kuna ärikasutajad võivad kasutada erinevaid keeli juriidilisest isikust sõltuvate maksukoodide kogumite määramiseks, soovitame teil tõlkida selle loetelu väärtused keeltesse, mis on konfigureeritud eelistatud keeltena nende kasutajate jaoks Finance’is.</span><span class="sxs-lookup"><span data-stu-id="ef787-197">Because the business users might use different languages to specify legal entity–dependent sets of tax codes, we recommend that you translate the values of this enumeration into the languages that are configured as the preferred languages for those users in Finance.</span></span>

14. <span data-ttu-id="ef787-198">Valige kirje **Maksustamine puudub**.</span><span class="sxs-lookup"><span data-stu-id="ef787-198">Select the **No taxation** record.</span></span>
15. <span data-ttu-id="ef787-199">Klõpsake välja **Silt**.</span><span class="sxs-lookup"><span data-stu-id="ef787-199">Click in the **Label** field.</span></span>
16. <span data-ttu-id="ef787-200">Valige käsk **Tõlgi**.</span><span class="sxs-lookup"><span data-stu-id="ef787-200">Select **Translate**.</span></span>
17. <span data-ttu-id="ef787-201">Sisestage paanil **Teksti tõlge** väljale **Sildi ID** väärtus **LBL_LEVELENUM_NO**.</span><span class="sxs-lookup"><span data-stu-id="ef787-201">In the **Text translation** pane, in the **Label Id** field, enter **LBL_LEVELENUM_NO**.</span></span>
18. <span data-ttu-id="ef787-202">Sisestage väljale **Tekst vaikekeeles** väärtus **Maksustamine puudub**.</span><span class="sxs-lookup"><span data-stu-id="ef787-202">In the **Text in default language** field, enter **No taxation**.</span></span>
19. <span data-ttu-id="ef787-203">Sisestage väljale **Keel** väärtus **DE**.</span><span class="sxs-lookup"><span data-stu-id="ef787-203">In the **Language** field, select **DE**.</span></span>
20. <span data-ttu-id="ef787-204">Sisestage väljale **Tõlgitud tekst** väärtus **keine Besteuerung**.</span><span class="sxs-lookup"><span data-stu-id="ef787-204">In the **Translated text** field, enter **keine Besteuerung**.</span></span>
21. <span data-ttu-id="ef787-205">Valige käsk **Tõlgi**.</span><span class="sxs-lookup"><span data-stu-id="ef787-205">Select **Translate**.</span></span>

    ![ER-i toimingu koostaja leht](./media/RCS-AppSpecParms-ConfigureFormat-EnumTranslate.PNG)

22. <span data-ttu-id="ef787-207">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ef787-207">Select **Save**.</span></span>
23. <span data-ttu-id="ef787-208">Sulgege leht **Vormingu loetelud**.</span><span class="sxs-lookup"><span data-stu-id="ef787-208">Close the **Format enumerations** page.</span></span>

### <a name="add-a-new-lookup-data-source"></a><span data-ttu-id="ef787-209">Uue andmeallika otsimise lisamine</span><span class="sxs-lookup"><span data-stu-id="ef787-209">Add a new lookup data source</span></span>

<span data-ttu-id="ef787-210">Järgmiseks lisage uus andmeallikas määramaks, kuidas ärikasutajad määravad juriidilisest isikust sõltuvaid reegleid õige maksustamistaseme tuvastamiseks iga kokkuvõtliku kande kirje jaoks.</span><span class="sxs-lookup"><span data-stu-id="ef787-210">Next, you will add a new data source to specify how business users will specify legal entity–dependent rules to recognize the correct taxation level for each summarized transaction record.</span></span>

1.  <span data-ttu-id="ef787-211">Valige vahekaardil **Vastendamine** käsk **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="ef787-211">On the **Mapping** tab, select **Add**.</span></span>
2.  <span data-ttu-id="ef787-212">Valige suvand **Vormingu loetelu\otsing**.</span><span class="sxs-lookup"><span data-stu-id="ef787-212">Select **Format enumeration\Lookup**.</span></span>

    <span data-ttu-id="ef787-213">Tuvastasite äsja, et iga reegel, mille ärikasutajad määravad maksustamistaseme tuvastamiseks, tagastavad ER-vormingu loetelu väärtuse.</span><span class="sxs-lookup"><span data-stu-id="ef787-213">You just identified that each rule that business users specify for taxation level recognition will return a value of an ER format enumeration.</span></span> <span data-ttu-id="ef787-214">Pange tähele, et andmeallika tüübile **Otsing** pääseb ligi jaotisest **Andmemudel** ja **Dynamics 365 for Operations**i plokkidest lisaks plokile **Vormingu loetelu**.</span><span class="sxs-lookup"><span data-stu-id="ef787-214">Notice that the **Lookup** data source type can be accessed under the **Data model** and **Dynamics 365 for Operations** blocks in addition to the **Format enumeration** block.</span></span> <span data-ttu-id="ef787-215">Seetõttu saab ER-i andmemudeli loetelusid ja rakenduse loetelusid kasutada väärtuste määramiseks, mis tagastatakse seda tüüpi andmeallikate kohta.</span><span class="sxs-lookup"><span data-stu-id="ef787-215">Therefore, ER data model enumerations and application enumerations can be used to specify the type of values that is are returned for data sources of that type.</span></span>
    
3.  <span data-ttu-id="ef787-216">Väljale **Nimi** sisestage suvand **Valija**.</span><span class="sxs-lookup"><span data-stu-id="ef787-216">In the **Name** field, enter **Selector**.</span></span>
4.  <span data-ttu-id="ef787-217">Väljalt **Vormingu loetelu** valige väärtus **Maksustamistasemete loend**.</span><span class="sxs-lookup"><span data-stu-id="ef787-217">In the **Format enumeration** field, select **List of taxation levels**.</span></span>

    <span data-ttu-id="ef787-218">Määrasite äsja, et iga selles andmeallikas määratud reegli kohta peab ärikasutaja valima ühe vormingu loetelu **Maksustamistasemete loend** väärtuse tagastatud väärtusena.</span><span class="sxs-lookup"><span data-stu-id="ef787-218">You just specified that, for each rule that is specified in this data source, a business user must select one of the values of the **List of taxation levels** format enumeration as a returned value.</span></span>
    
5.  <span data-ttu-id="ef787-219">Valige suvand **Otsingu redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="ef787-219">Select **Edit lookup**.</span></span>
6.  <span data-ttu-id="ef787-220">Valige suvand **Veerud**.</span><span class="sxs-lookup"><span data-stu-id="ef787-220">Select **Columns**.</span></span>
7.  <span data-ttu-id="ef787-221">Laiendage üksust **Mudel**.</span><span class="sxs-lookup"><span data-stu-id="ef787-221">Expand the **Model** item.</span></span>
8.  <span data-ttu-id="ef787-222">Laiendage üksust **Andmed**.</span><span class="sxs-lookup"><span data-stu-id="ef787-222">Expand the **Data** item.</span></span>
9.  <span data-ttu-id="ef787-223">Laiendage üksust **Maks**.</span><span class="sxs-lookup"><span data-stu-id="ef787-223">Expand the **Tax** item.</span></span>
10. <span data-ttu-id="ef787-224">Valige üksus **Model.Data.Tax.Code**.</span><span class="sxs-lookup"><span data-stu-id="ef787-224">Select the **Model.Data.Tax.Code** item.</span></span>
11. <span data-ttu-id="ef787-225">Valige nupp **Lisa** (paremnool).</span><span class="sxs-lookup"><span data-stu-id="ef787-225">Select the **Add** button (the right arrow).</span></span>

    ![ER-i toimingu koostaja leht](./media/RCS-AppSpecParms-ConfigureFormat-Lookup1.PNG)

    <span data-ttu-id="ef787-227">Määrasite äsja, et iga maksustamistaseme tuvastamise selles andmeallikas määratud reegli kohta peab ärikasutaja valima tingimuseks ühe maksukoodi.</span><span class="sxs-lookup"><span data-stu-id="ef787-227">You just specified that, for each rule that is specified in this data source for taxation level recognition, a business user must select one of the tax codes as a condition.</span></span> <span data-ttu-id="ef787-228">Maksukoodide loend, mida ärikasutaja saab valida, tagastatakse andmeallikaga **Model.Data.Tax**.</span><span class="sxs-lookup"><span data-stu-id="ef787-228">The list of tax codes that the business user can select will be returned by the **Model.Data.Tax** data source.</span></span> <span data-ttu-id="ef787-229">Kuna see andmeallikas sisaldab välja **Nimi**, kuvatakse maksukoodi nimi iga maksukoodi väärtuse kohta otsingus, mis esitatakse ärikasutajale.</span><span class="sxs-lookup"><span data-stu-id="ef787-229">Because this data source contains the **Name** field, the name of the tax code will be shown for each tax code value in the lookup that is presented to the business user.</span></span>
    
12. <span data-ttu-id="ef787-230">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef787-230">Select **OK**.</span></span>

    ![ER-i toimingu koostaja leht](./media/RCS-AppSpecParms-ConfigureFormat-Lookup2.PNG)

    <span data-ttu-id="ef787-232">Ärikasutajad saavad lisada selle andmeallika kirjetena mitu reeglit.</span><span class="sxs-lookup"><span data-stu-id="ef787-232">Business users can add multiple rules as records of this data source.</span></span> <span data-ttu-id="ef787-233">Iga kirje nummerdatakse rea koodi järgi.</span><span class="sxs-lookup"><span data-stu-id="ef787-233">Each record will be numbered by a line code.</span></span> <span data-ttu-id="ef787-234">Reegleid hinnatakse rea numbrite kasvavas järjekorras.</span><span class="sxs-lookup"><span data-stu-id="ef787-234">Rules will be evaluated in order of increasing line number.</span></span>

    <span data-ttu-id="ef787-235">Kuna valisite välja **Maksukood** reeglite tingimusena selles otsingu andmeallikas, ja kuna **Maksukood** on seadistatud andmetüübi **String** väljana, hinnatakse iga reeglit käitusajal, võrreldes maksukoodi, mis edastatakse andmeallikale, maksukoodiga, mis määratletakse andmeallika selles kirjes.</span><span class="sxs-lookup"><span data-stu-id="ef787-235">Because you selected the **Tax code** field as a condition for rules in this lookup data source, and because **Tax code** is set up as a field of the **String** data type, each rule will be evaluated at runtime by comparing the tax code that is passed to the data source with the tax code that is defined in this record of the data source.</span></span>

    <span data-ttu-id="ef787-236">Kui leitakse konfigureeritud tingimusele vastav reegel, tagastab see andmeallikas reegli otsinguväärtuse kohta, mis on määratletud väljas **Otsingu tulemus**.</span><span class="sxs-lookup"><span data-stu-id="ef787-236">When a rule that satisfies the configured condition is found, this data source returns the lookup value of the rule that is defined in the **Lookup result** field.</span></span> <span data-ttu-id="ef787-237">Kui ühtegi reeglit ei leita, esitatakse kasutajale erand, et andmeallikas ei saa õiget väärtust tagastada.</span><span class="sxs-lookup"><span data-stu-id="ef787-237">If no rule is found, an exception is thrown to notify the user that the current data source can't return a correct value.</span></span>

13. <span data-ttu-id="ef787-238">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ef787-238">Select **Save**.</span></span>
14. <span data-ttu-id="ef787-239">Sulgege leht **Otsingu koostaja**.</span><span class="sxs-lookup"><span data-stu-id="ef787-239">Close the **Lookup designer** page.</span></span>
15. <span data-ttu-id="ef787-240">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef787-240">Select **OK**.</span></span>

    <span data-ttu-id="ef787-241">Pange tähele, et kui lisasite uue andmeallika, tagastab see maksustamistaseme vormingu loetelu **Maksustamistasemete loend** väärtuse mis tahes maksukoodi kohta, mis edastatakse andmeallikale andmetüübi **String** parameetri **Kood** argumendina.</span><span class="sxs-lookup"><span data-stu-id="ef787-241">Notice that you added a new data source that will return the taxation level as the value of the **List of taxation levels** format enumeration for any tax code that is passed to the data source as the argument of the **Code** parameter of the **String** data type.</span></span>
    
    ![ER-i toimingu koostaja leht](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld.PNG)

    <span data-ttu-id="ef787-243">Pange tähele, et konfigureeritud reeglite hindamine oleneb väljade andmetüübist, mis on valitud määratlema nende reeglite tingimusi.</span><span class="sxs-lookup"><span data-stu-id="ef787-243">Note that the evaluation of configured rules depends on the data type of the fields that have been selected to define conditions of those rules.</span></span> <span data-ttu-id="ef787-244">Kui valite välja, mis on konfigureeritud väljaks andmetüübile **Numbriline** või **Kuupäev**, erinevad kriteeriumid kriteeriumitest, mida kirjeldati varem andmetüübi **String** kohta.</span><span class="sxs-lookup"><span data-stu-id="ef787-244">When you select a field that is configured as a field of either the **Numeric** or **Date** data type, the criteria will differ from the criteria that were described earlier for the **String** data type.</span></span> <span data-ttu-id="ef787-245">Väljade **Numbriline** ja **Kuupäev** korral tuleb reegel määrata väärtuste vahemikuna.</span><span class="sxs-lookup"><span data-stu-id="ef787-245">For **Numeric** and **Date** fields, the rule must be specified as a range of values.</span></span> <span data-ttu-id="ef787-246">Reegli tingimust peetakse täidetuks, kui andmeallikale edastatud väärtus jääb konfigureeritud vahemikku.</span><span class="sxs-lookup"><span data-stu-id="ef787-246">The condition of the rule will then be considered satisfied when a value that is passed to the data source is in the configured range.</span></span>
    
    <span data-ttu-id="ef787-247">Järgmisel joonisel on näide seda tüüpi seadistuse kohta.</span><span class="sxs-lookup"><span data-stu-id="ef787-247">The following illustration shows an example of this type of setup.</span></span> <span data-ttu-id="ef787-248">Peale välja **Model.Data.Tax.Code** andmetüübi **String** korral kasutatakse otsingu andmeallika tingimuste määramiseks välja **Model.Tax.Summary.Base** andmetüübi **Tegelik** korral.</span><span class="sxs-lookup"><span data-stu-id="ef787-248">In addition to the **Model.Data.Tax.Code** field of the **String** data type, the **Model.Tax.Summary.Base** field of the **Real** data type is used to specify conditions for a lookup data source.</span></span>
    
    ![ER-i toimingu koostaja leht](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld2.PNG)

    <span data-ttu-id="ef787-250">Kuna selle otsingu andmeallika jaoks valitakse väljad **Model.Data.Tax.Code** ja **Model.Tax.Summary.Base**, konfigureeritakse selle andmeallika iga reeglit järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="ef787-250">Because the **Model.Data.Tax.Code** and **Model.Tax.Summary.Base** fields are selected for this lookup data source, each rule of this data source will be configured in the following way:</span></span>
    
    -   <span data-ttu-id="ef787-251">Esitatud loendist tuleb tagastatud väärtuseks valida vormingu loetelu **Maksustamistasemete loend** väärtus.</span><span class="sxs-lookup"><span data-stu-id="ef787-251">In the list that is presented, the value of the **List of taxation levels** format enumeration must be selected as a returned value.</span></span>
    -   <span data-ttu-id="ef787-252">Selle reegli tingimuseks tuleb määrata maksukood.</span><span class="sxs-lookup"><span data-stu-id="ef787-252">The tax code must be entered as a condition of this rule.</span></span> <span data-ttu-id="ef787-253">Kehtivad ainult andmeallika **Model.Data.Tax** esitatud maksukoodid.</span><span class="sxs-lookup"><span data-stu-id="ef787-253">Only tax codes that are provided by the **Model.Data.Tax** data source are applicable.</span></span>
    -   <span data-ttu-id="ef787-254">Reegli tingimuseks tuleb sisestada maksu baassumma miinimum- ja maksimumväärtused.</span><span class="sxs-lookup"><span data-stu-id="ef787-254">Minimum and maximum values of the tax base amount must be entered as conditions of this rule.</span></span>

    <span data-ttu-id="ef787-255">Käitusajal hinnatakse selle andmeallika iga reeglit järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="ef787-255">Here is how each rule of this data source will be evaluated at runtime:</span></span>
    -   <span data-ttu-id="ef787-256">Kas andmetüübi **String** kood, mis edastatakse sellele andmeallikale, on võrdne reegli maksukoodiga?</span><span class="sxs-lookup"><span data-stu-id="ef787-256">Does the code of the **String** data type that was passed to this data source equal the tax code of a rule?</span></span>
    -   <span data-ttu-id="ef787-257">Kas andmetüübi **Tegelik** väärtus, mis edastatakse sellele andmeallikale, jääb miinimum- ja maksimumväärtuse vahele?</span><span class="sxs-lookup"><span data-stu-id="ef787-257">Does the value of the **Real** data type that was passed to this data source fall between specific minimum and maximum values?</span></span>

    <span data-ttu-id="ef787-258">Reeglit peetakse kehtivaks, kui mõlemad tingimused on täidetud.</span><span class="sxs-lookup"><span data-stu-id="ef787-258">A rule will be considered applicable when both conditions are satisfied.</span></span>

### <a name="translate-the-label-of-the-lookup-data-source-that-was-added"></a><span data-ttu-id="ef787-259">Lisatud otsingu andmeallika sildi tõlkimine</span><span class="sxs-lookup"><span data-stu-id="ef787-259">Translate the label of the lookup data source that was added</span></span>

<span data-ttu-id="ef787-260">Kuna ärikasutajad võivad kasutada erinevaid keeli juriidilisest isikust sõltuvate maksukoodide kogumite määramiseks, soovitame teil tõlkida iga lisatud otsingu andmeallika sildi, et see kuvataks vastaval lehel iga kasutaja valitud keeles.</span><span class="sxs-lookup"><span data-stu-id="ef787-260">Because business users might use different languages to specify legal entity–dependent sets of tax codes, we recommend that you translate the label of any lookup data source that you add, so that it's presented in each user's preferred language on the corresponding page.</span></span>

1.  <span data-ttu-id="ef787-261">Valige andmeallikas **Model.Data.Selector**.</span><span class="sxs-lookup"><span data-stu-id="ef787-261">Select the **Model.Data.Selector** data source.</span></span>
2.  <span data-ttu-id="ef787-262">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="ef787-262">Select **Edit**.</span></span>
3.  <span data-ttu-id="ef787-263">Klõpsake välja **Silt**.</span><span class="sxs-lookup"><span data-stu-id="ef787-263">Click in the **Label** field.</span></span>
4.  <span data-ttu-id="ef787-264">Valige käsk **Tõlgi**.</span><span class="sxs-lookup"><span data-stu-id="ef787-264">Select **Translate**.</span></span>
5.  <span data-ttu-id="ef787-265">Sisestage paanil **Teksti tõlge** väljale **Sildi ID** väärtus **LBL_SELECTOR_DS**.</span><span class="sxs-lookup"><span data-stu-id="ef787-265">In the **Text translation** pane, in the **Label Id** field, enter **LBL_SELECTOR_DS**.</span></span>
6.  <span data-ttu-id="ef787-266">Sisestage väljale **Tekst vaikekeeles** väärtus **Vali maksutase maksukoodi järgi**.</span><span class="sxs-lookup"><span data-stu-id="ef787-266">In the **Text in default language** field, enter **Select tax level by tax code**.</span></span>
7.  <span data-ttu-id="ef787-267">Sisestage väljale **Keel** väärtus **DE**.</span><span class="sxs-lookup"><span data-stu-id="ef787-267">In the **Language** field, select **DE**.</span></span>
8.  <span data-ttu-id="ef787-268">Sisestage väljale **Tõlgitud tekst** väärtus **Steuerebene für Steuerkennzeichen auswählen**.</span><span class="sxs-lookup"><span data-stu-id="ef787-268">In the **Translated text** field, enter **Steuerebene für Steuerkennzeichen auswählen**.</span></span>
9.  <span data-ttu-id="ef787-269">Valige käsk **Tõlgi**.</span><span class="sxs-lookup"><span data-stu-id="ef787-269">Select **Translate**.</span></span>
10. <span data-ttu-id="ef787-270">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef787-270">Select **OK**.</span></span>

    ![ER-i toimingu koostaja leht](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFldTranslate.PNG)

### <a name="add-a-new-field-to-consume-the-configured-lookup"></a><span data-ttu-id="ef787-272">Konfigureeritud otsingu kasutamiseks uue välja lisamine</span><span class="sxs-lookup"><span data-stu-id="ef787-272">Add a new field to consume the configured lookup</span></span>

1.  <span data-ttu-id="ef787-273">Laiendage üksust **Model.Data**.</span><span class="sxs-lookup"><span data-stu-id="ef787-273">Expand the **Model.Data** item.</span></span>
2.  <span data-ttu-id="ef787-274">Valige üksus **Model.Data.Summary**.</span><span class="sxs-lookup"><span data-stu-id="ef787-274">Select the **Model.Data.Summary** item.</span></span>
3.  <span data-ttu-id="ef787-275">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="ef787-275">Select **Add**.</span></span>
4.  <span data-ttu-id="ef787-276">Valige üksus **Funktsioonid / Arvutatud väli**.</span><span class="sxs-lookup"><span data-stu-id="ef787-276">Select **Functions/Calculated field**.</span></span>
5.  <span data-ttu-id="ef787-277">Väljale **Nimi** sisestage väärtus **LevelByLookup**.</span><span class="sxs-lookup"><span data-stu-id="ef787-277">In the **Name** field, enter **LevelByLookup**.</span></span>
6.  <span data-ttu-id="ef787-278">Valige **Valemi redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="ef787-278">Select **Edit formula**.</span></span>
7.  <span data-ttu-id="ef787-279">Sisestage väljale **Valem** väärtus **Model.Selector(Model.Data.Summary.Code)**.</span><span class="sxs-lookup"><span data-stu-id="ef787-279">In the **Formula field**, enter **Model.Selector(Model.Data.Summary.Code)**.</span></span>
8.  <span data-ttu-id="ef787-280">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ef787-280">Select **Save**.</span></span>

    ![ER-i toimingu koostaja leht](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld.PNG)

9.  <span data-ttu-id="ef787-282">Sulgege leht **Valemiredaktor**.</span><span class="sxs-lookup"><span data-stu-id="ef787-282">Close the **Formula editor** page.</span></span>
10. <span data-ttu-id="ef787-283">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef787-283">Select **OK**.</span></span>

    ![ER-i toimingu koostaja leht](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld2.PNG)

    <span data-ttu-id="ef787-285">Pange tähele, et lisatud arvutatud väli **LevelByLookup** tagastab iga kokkuvõtliku maksukande kirje kohta vormingu loetelu **Maksustamistasemete loend** väärtusena maksustamistaseme.</span><span class="sxs-lookup"><span data-stu-id="ef787-285">Notice that the **LevelByLookup** calculated field that you added will return the taxation level as the value of the **List of taxation levels** format enumeration for each summarized tax transactions record.</span></span> <span data-ttu-id="ef787-286">Kirje maksukood edastatakse otsingu andmeallikale **Model.Selector** ja selle andmeallika reeglite kogumit kasutatakse õige maksustamistaseme valimiseks.</span><span class="sxs-lookup"><span data-stu-id="ef787-286">The tax code of the record will be passed to the **Model.Selector** lookup data source, and the set of rules for this data source will be used to select the correct taxation level.</span></span>

### <a name="add-a-new-format-enumeration-based-data-source"></a><span data-ttu-id="ef787-287">Uue vormingu loetelul põhineva andmeallika lisamine</span><span class="sxs-lookup"><span data-stu-id="ef787-287">Add a new format enumeration-based data source</span></span>

<span data-ttu-id="ef787-288">Järgmiseks lisage uus andmeallikas, mis viitab varem lisatud vormingu loetelule.</span><span class="sxs-lookup"><span data-stu-id="ef787-288">Next, you will add a new data source that refers to the format enumeration that you added earlier.</span></span> <span data-ttu-id="ef787-289">Selle andmeallika väärtusi kasutatakse hiljem ER-vormingu avaldises.</span><span class="sxs-lookup"><span data-stu-id="ef787-289">Values of this data source will be used in an ER format expression later.</span></span>

1.  <span data-ttu-id="ef787-290">Valige **Lisa juur**.</span><span class="sxs-lookup"><span data-stu-id="ef787-290">Select **Add root**.</span></span>
2.  <span data-ttu-id="ef787-291">Valige suvand **Vormingu loetelud \ Loetelu**.</span><span class="sxs-lookup"><span data-stu-id="ef787-291">Select **Format enumerations\Enumeration**.</span></span>
3.  <span data-ttu-id="ef787-292">Väljale **Nimi** sisestage väärtus **Maksustamise tase**.</span><span class="sxs-lookup"><span data-stu-id="ef787-292">In the **Name** field, enter **TaxationLevel**.</span></span>
4.  <span data-ttu-id="ef787-293">Väljalt **Vormingu loetelu** valige väärtus **Maksustamistasemete loend**.</span><span class="sxs-lookup"><span data-stu-id="ef787-293">In the **Format enumeration** field, select **List of taxation levels**.</span></span>
5.  <span data-ttu-id="ef787-294">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ef787-294">Select **Save**.</span></span>

### <a name="modify-an-existing-field-to-start-to-use-the-lookup"></a><span data-ttu-id="ef787-295">Olemasoleva välja muutmine otsingu kasutamise alustamiseks</span><span class="sxs-lookup"><span data-stu-id="ef787-295">Modify an existing field to start to use the lookup</span></span>

<span data-ttu-id="ef787-296">Järgmiseks muutke olemasolevat arvutatud välja nii, et see kasutaks konfigureeritud otsingu andmeallikat õige maksustamistaseme väärtuse tagastamiseks olenevalt maksukoodist.</span><span class="sxs-lookup"><span data-stu-id="ef787-296">Next, you will modify the existing calculated field so that it uses the configured lookup data source to return the correct taxation level value, depending on the tax code.</span></span>

1.  <span data-ttu-id="ef787-297">Valige üksus **Model.Data.Summary.Level**.</span><span class="sxs-lookup"><span data-stu-id="ef787-297">Select the **Model.Data.Summary.Level** item.</span></span>
2.  <span data-ttu-id="ef787-298">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="ef787-298">Select **Edit**.</span></span>
3.  <span data-ttu-id="ef787-299">Valige **Valemi redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="ef787-299">Select **Edit formula**.</span></span>

    <span data-ttu-id="ef787-300">Pange tähele, et välja **Model.Data.Summary.Level** praegune avaldis sisaldab järgmisi püsiprogrammeeritud maksukoode:</span><span class="sxs-lookup"><span data-stu-id="ef787-300">Notice that the current expression of the **Model.Data.Summary.Level** field includes the following hard-coded tax codes:</span></span>
    
    <span data-ttu-id="ef787-301">CASE (@.Code, "VAT19", "Regular", "InVAT19", "Regular", "VAT7", "Reduced", "InVAT7", "Reduced", "THIRD", "None", "InVAT0", "None", "Other")</span><span class="sxs-lookup"><span data-stu-id="ef787-301">CASE (@.Code, "VAT19", "Regular", "InVAT19", "Regular", "VAT7", "Reduced", "InVAT7", "Reduced", "THIRD", "None", "InVAT0", "None", "Other")</span></span>

4.  <span data-ttu-id="ef787-302">Sisestage väljale **Valem** väärtus **CASE(@.LevelByLookup, TaxationLevel.'Regular taxation', "Regular", TaxationLevel.'Reduced taxation', "Reduced", TaxationLevel.'No taxation', "None", "Other")**.</span><span class="sxs-lookup"><span data-stu-id="ef787-302">In the **Formula** field, enter **CASE(@.LevelByLookup, TaxationLevel.'Regular taxation', "Regular", TaxationLevel.'Reduced taxation', "Reduced", TaxationLevel.'No taxation', "None", "Other")**.</span></span>

    ![ER-i toimingu koostaja leht](./media/RCS-AppSpecParms-ConfigureFormat-ChangeLookupFld.PNG)
    
    <span data-ttu-id="ef787-304">Pange tähele, et välja **Model.Data.Summary.Level** avaldis tagastab nüüd maksustamistaseme, lähtudes praeguse kirje maksukoodist ja reeglite kogumist, mille ärikasutaja konfigureerib otsingu andmeallikas **Model.Data.Selector**.</span><span class="sxs-lookup"><span data-stu-id="ef787-304">Notice that the expression of the **Model.Data.Summary.Level** field will now return the taxation level, based on the tax code of the current record and the set of rules that that a business user configures in the **Model.Data.Selector** lookup data source.</span></span>
    
5.  <span data-ttu-id="ef787-305">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ef787-305">Select **Save**.</span></span>
6.  <span data-ttu-id="ef787-306">Sulgege leht **Valemikoostaja**.</span><span class="sxs-lookup"><span data-stu-id="ef787-306">Close **Formula designer** page.</span></span>
7.  <span data-ttu-id="ef787-307">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef787-307">Select **OK**.</span></span>
8.  <span data-ttu-id="ef787-308">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="ef787-308">Select **Save**.</span></span>
9.  <span data-ttu-id="ef787-309">Sulgege **Vormingu koostaja** leht.</span><span class="sxs-lookup"><span data-stu-id="ef787-309">Close **Format designer** page.</span></span>

## <a name="complete-the-draft-version-of-a-derived-format"></a><span data-ttu-id="ef787-310">Tuletatud vormingu mustandversiooni lõpetamine</span><span class="sxs-lookup"><span data-stu-id="ef787-310">Complete the draft version of a derived format</span></span>

1.  <span data-ttu-id="ef787-311">Valige kiirkaardil **Versioonid** käsk **Muuda olekut**.</span><span class="sxs-lookup"><span data-stu-id="ef787-311">On the **Versions** fast tab, select **Change status**.</span></span>
2.  <span data-ttu-id="ef787-312">Valige **Lõpeta**.</span><span class="sxs-lookup"><span data-stu-id="ef787-312">Select **Complete**.</span></span>
3.  <span data-ttu-id="ef787-313">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef787-313">Select **OK**.</span></span>

## <a name="export-completed-version-of-modified-format"></a><span data-ttu-id="ef787-314">Muudetud vormingu lõpuleviidud versiooni eksportimine</span><span class="sxs-lookup"><span data-stu-id="ef787-314">Export completed version of modified format</span></span>

1.  <span data-ttu-id="ef787-315">Valige konfiguratsioonipuust üksus **Vorming LE-andmete otsingu õppimiseks**.</span><span class="sxs-lookup"><span data-stu-id="ef787-315">In the configuration tree, select the **Format to learn how to lookup LE data** item.</span></span>
2.  <span data-ttu-id="ef787-316">Valige kiirkaardil **Versioonid** kirje, mille olek on **Lõpule viidud**.</span><span class="sxs-lookup"><span data-stu-id="ef787-316">On the **Versions** fast tab, select the record that has a status of **Completed**.</span></span>
3.  <span data-ttu-id="ef787-317">Valige **Exchange**.</span><span class="sxs-lookup"><span data-stu-id="ef787-317">Select **Exchange**.</span></span>
4.  <span data-ttu-id="ef787-318">Valige **Ekspordi XML-failina**.</span><span class="sxs-lookup"><span data-stu-id="ef787-318">Select **Export as XML file**.</span></span>
5.  <span data-ttu-id="ef787-319">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef787-319">Select **OK**.</span></span>
6.  <span data-ttu-id="ef787-320">Veebibrauser laadib alla faili **Format to learn how to lookup LE data.xml**.</span><span class="sxs-lookup"><span data-stu-id="ef787-320">The web browser downloads a **Format to learn how to lookup LE data.xml** file.</span></span> <span data-ttu-id="ef787-321">Salvestage see fail lokaalselt.</span><span class="sxs-lookup"><span data-stu-id="ef787-321">Store this file locally.</span></span>

<span data-ttu-id="ef787-322">Korrake selle jaotise etappe vormingu **Vorming LE-andmete otsingu õppimiseks** ülemüksuste jaoks ja salvestage lokaalselt järgmised failid:</span><span class="sxs-lookup"><span data-stu-id="ef787-322">Repeat steps in this section for parent items of the **Format to learn how to lookup LE data** format, and store the following files locally:</span></span>

-   <span data-ttu-id="ef787-323">Format to learn parameterized calls.xml</span><span class="sxs-lookup"><span data-stu-id="ef787-323">Format to learn parameterized calls.xml</span></span>
-   <span data-ttu-id="ef787-324">Mapping to learn parameterized calls.xml</span><span class="sxs-lookup"><span data-stu-id="ef787-324">Mapping to learn parameterized calls.xml</span></span>
-   <span data-ttu-id="ef787-325">Model to learn parameterized calls.xml</span><span class="sxs-lookup"><span data-stu-id="ef787-325">Model to learn parameterized calls.xml</span></span>

<span data-ttu-id="ef787-326">Selleks et õppida konfigureeritud ER-vormingut **Vorming LE-andmete otsingu õppimiseks** kasutama juriidilisest isikust sõltuvate maksukoodide kogumite seadistamiseks, et filtreerida maksukandeid eri maksustamistasemete järgi, läbige etapid teemas [ER-vormingu parameetrite seadistamine juriidilise isiku kohta](er-app-specific-parameters-set-up.md).</span><span class="sxs-lookup"><span data-stu-id="ef787-326">To learn how to use the configured **Format to learn how to lookup LE data** ER format to set up legal entity–dependent sets of tax codes to filter tax transactions by different taxation levels, complete the steps in the [Set up the parameters of an ER format per legal entity](er-app-specific-parameters-set-up.md) topic.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ef787-327">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="ef787-327">Additional resources</span></span>

[<span data-ttu-id="ef787-328">Valemikoostaja elektroonilises aruandluses</span><span class="sxs-lookup"><span data-stu-id="ef787-328">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="ef787-329">ER-vormingu parameetrite seadistamine juriidilise isiku kohta</span><span class="sxs-lookup"><span data-stu-id="ef787-329">Set up the parameters of an ER format per legal entity</span></span>](er-app-specific-parameters-set-up.md)
