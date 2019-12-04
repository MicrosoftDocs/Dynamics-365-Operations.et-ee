---
title: Arvutatud väljatüübi ER-andmeallikate parameetritega kõned
description: See teema annab teavet selle kohta, kuidas kasutada arvutatud väljatüüpi ER-andmeallikate puhul.
author: NickSelin
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3f331401f8d191243f72961333e4f1dbe84d0be5
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2771325"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a><span data-ttu-id="4384a-103">Arvutatud väljatüübi ER-andmeallikate parameetritega kõned</span><span class="sxs-lookup"><span data-stu-id="4384a-103">Support parameterized calls of ER data sources of the Calculated field type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4384a-104">See teema selgitab, kuidas saate kujundada elektroonilise aruandluse (ER) andmeallikat, kasutades tüüpi **Arvutatud väli**.</span><span class="sxs-lookup"><span data-stu-id="4384a-104">This topic explains how you can design an Electronic reporting (ER) data source by using the **Calculated field** type.</span></span> <span data-ttu-id="4384a-105">See andmeallikas võib sisaldada ER-avaldist, mida käivitamisel saab juhtida seda andmeallikat nimetavas sidumises konfigureeritud parameetriargumentide väärtustega.</span><span class="sxs-lookup"><span data-stu-id="4384a-105">This data source may contain an ER expression that, when executed, can be controlled by the values of the parameter arguments that are configured in a binding that calls this data source.</span></span> <span data-ttu-id="4384a-106">Sellise andmeallika parameeteriseeritud kõnede konfigureerimisega saate ühte andmeallikat mitmes sidumises uuesti kasutada, mis vähendab ER-mudeli vastendustes või ER-vormingutes konfigureeritavate andmeallikate koguarvu.</span><span class="sxs-lookup"><span data-stu-id="4384a-106">By configuring parameterized calls of such a data source, you can reuse a single data source in many bindings, which reduces the total number of data sources that must be configured in ER model mappings or ER formats.</span></span> <span data-ttu-id="4384a-107">See lihtsustab ka konfigureeritud ER-komponenti, mis vähendab hoolduskulusid ja teiste tarbijate kasutuskulusid.</span><span class="sxs-lookup"><span data-stu-id="4384a-107">It also simplifies the configured ER component, which reduces the maintenance costs and the cost of use by other consumers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="4384a-108">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="4384a-108">Prerequisites</span></span>
<span data-ttu-id="4384a-109">Selles teemas näidete lõpuleviimiseks peavad teil olema järgmised juurdepääsuõigused.</span><span class="sxs-lookup"><span data-stu-id="4384a-109">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="4384a-110">Juurdepääs ühele neist rollidest:</span><span class="sxs-lookup"><span data-stu-id="4384a-110">Access to one of these roles:</span></span>

    - <span data-ttu-id="4384a-111">Elektroonilise aruandluse arendaja</span><span class="sxs-lookup"><span data-stu-id="4384a-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="4384a-112">Elektroonilise aruandluse funktsionaalne konsultant</span><span class="sxs-lookup"><span data-stu-id="4384a-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="4384a-113">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="4384a-113">System administrator</span></span>

- <span data-ttu-id="4384a-114">Juurdepääs teenuse Regulatory Configuration Services (RCS) eksemplarile, mis on ette valmistatud sama rentniku jaoks, nagu rakendus Finance and Operations, ühe järgmise rolli jaoks:</span><span class="sxs-lookup"><span data-stu-id="4384a-114">Access to Regulatory Configuration Services (RCS) that have been provisioned for the same tenant as Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="4384a-115">Elektroonilise aruandluse arendaja</span><span class="sxs-lookup"><span data-stu-id="4384a-115">Electronic reporting developer</span></span>
    - <span data-ttu-id="4384a-116">Elektroonilise aruandluse funktsionaalne konsultant</span><span class="sxs-lookup"><span data-stu-id="4384a-116">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="4384a-117">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="4384a-117">System administrator</span></span>

<span data-ttu-id="4384a-118">Laadige [Microsofti allalaadimiskeskusest](https://go.microsoft.com/fwlink/?linkid=874684) alla tihendatud fail **Arvutatud väljatüübi ER-andmeallikate parameetritega kõned**.</span><span class="sxs-lookup"><span data-stu-id="4384a-118">From the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684), download the zipped (compressed) file **Support parameterized calls of ER data sources of Calculated field type**.</span></span> <span data-ttu-id="4384a-119">See sisaldab järgmisi ER-konfiguratsioone, mida tuleb kohapeal ekstraheerida ja säilitada.</span><span class="sxs-lookup"><span data-stu-id="4384a-119">It contains the following ER configurations that must be extracted and stored locally.</span></span>

| <span data-ttu-id="4384a-120">**Sisu**</span><span class="sxs-lookup"><span data-stu-id="4384a-120">**Content**</span></span>                           | <span data-ttu-id="4384a-121">**Faili nimi**</span><span class="sxs-lookup"><span data-stu-id="4384a-121">**File name**</span></span>                                        |
|---------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4384a-122">ER-i andmemudeli konfiguratsiooni näide</span><span class="sxs-lookup"><span data-stu-id="4384a-122">Sample ER data model configuration</span></span>    | <span data-ttu-id="4384a-123">Mudel parameetritega calls.version.1.xml õppimiseks</span><span class="sxs-lookup"><span data-stu-id="4384a-123">Model to learn parameterized calls.version.1.xml</span></span>     |
| <span data-ttu-id="4384a-124">ER-i metaandmete konfiguratsiooni näide</span><span class="sxs-lookup"><span data-stu-id="4384a-124">Sample ER metadata configuration</span></span>      | <span data-ttu-id="4384a-125">Metaandmed parameetritega calls.version.1.xml õppimiseks</span><span class="sxs-lookup"><span data-stu-id="4384a-125">Metadata to learn parameterized calls.version.1.xml</span></span>  |
| <span data-ttu-id="4384a-126">ER-i mudelivastenduse konfiguratsiooni näide</span><span class="sxs-lookup"><span data-stu-id="4384a-126">Sample ER model mapping configuration</span></span> | <span data-ttu-id="4384a-127">Vastendamine parameetritega calls.version.1.xml õppimiseks</span><span class="sxs-lookup"><span data-stu-id="4384a-127">Mapping to learn parameterized calls.version.1.1.xml</span></span> |
| <span data-ttu-id="4384a-128">ER-vormingu konfiguratsiooni näide</span><span class="sxs-lookup"><span data-stu-id="4384a-128">Sample ER format configuration</span></span>        | <span data-ttu-id="4384a-129">Vorming parameetritega calls.version.1.xml õppimiseks</span><span class="sxs-lookup"><span data-stu-id="4384a-129">Format to learn parameterized calls.version.1.1.xml</span></span>  |

## <a name="sign-in-to-your-rcs-instance"></a><span data-ttu-id="4384a-130">Logige sisse oma RCS-eksemplari.</span><span class="sxs-lookup"><span data-stu-id="4384a-130">Sign in to your RCS instance</span></span>
<span data-ttu-id="4384a-131">Selles näites loote konfiguratsiooni näidisettevõtte Litware, Inc. jaoks. Esmalt peate RCS-is täitma teemas [Konfiguratsiooni pakkujate loomine ja nende aktiivseks märkimine](tasks/er-configuration-provider-mark-it-active-2016-11.md) toodud juhised.</span><span class="sxs-lookup"><span data-stu-id="4384a-131">In this example, you will create a configuration for the sample company, Litware, Inc. First, in RCS, you must complete the steps in the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure:</span></span>

1. <span data-ttu-id="4384a-132">Valige vaikimisi armatuurlaual **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="4384a-132">On the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="4384a-133">Valige **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="4384a-133">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="4384a-134">Importige allalaaditud konfiguratsioonid RCS-i järgmises järjestuses: andmemudel, metaandmed, mudeli vastendamine, vorming.</span><span class="sxs-lookup"><span data-stu-id="4384a-134">Import the downloaded configurations to RCS in the following sequence: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="4384a-135">Täitke järgmised sammud iga ER-konfiguratsiooni puhul:</span><span class="sxs-lookup"><span data-stu-id="4384a-135">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="4384a-136">Valige **Vaheta**.</span><span class="sxs-lookup"><span data-stu-id="4384a-136">Select **Exchange.**</span></span>
    2. <span data-ttu-id="4384a-137">Valige **Laadi XML-failist**.</span><span class="sxs-lookup"><span data-stu-id="4384a-137">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="4384a-138">Valige käsk **Sirvi** ja valige nõutav ER-i konfiguratsioon XML-vormingus.</span><span class="sxs-lookup"><span data-stu-id="4384a-138">Select **Browse**, and then select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="4384a-139">Valige nupp **OK.**</span><span class="sxs-lookup"><span data-stu-id="4384a-139">Select **OK.**</span></span>

## <a name="review-the-provided-er-solution"></a><span data-ttu-id="4384a-140">Vaadake läbi esitatud ER-lahendus</span><span class="sxs-lookup"><span data-stu-id="4384a-140">Review the provided ER solution</span></span>

### <a name="review-model-mapping"></a><span data-ttu-id="4384a-141">Mudeli vastendamise läbivaatamine</span><span class="sxs-lookup"><span data-stu-id="4384a-141">Review model mapping</span></span>

1. <span data-ttu-id="4384a-142">Laiendage konfiguratsioonipuus üksuse **Parameetritega kõnede õppimiseks kasutatava mudeli** sisu.</span><span class="sxs-lookup"><span data-stu-id="4384a-142">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="4384a-143">Valige **Vastendamine parameetritega kõnede õppimiseks**.</span><span class="sxs-lookup"><span data-stu-id="4384a-143">Select **Mapping to learn parameterized calls**.</span></span>
3. <span data-ttu-id="4384a-144">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="4384a-144">Select **Designer**.</span></span>
4. <span data-ttu-id="4384a-145">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="4384a-145">Select **Designer**.</span></span>  
   
    <span data-ttu-id="4384a-146">See ER-mudeli vastendus on ette nähtud selleks, et teha järgmist:</span><span class="sxs-lookup"><span data-stu-id="4384a-146">This ER model mapping is designed to do the following:</span></span>

    - <span data-ttu-id="4384a-147">Tooge sisse maksukoodide loetelu (**Maksu** andmeallikas), mis asub tabelis **TaxTable**.</span><span class="sxs-lookup"><span data-stu-id="4384a-147">Fetch the list of tax codes (**Tax** data source) residing in the **TaxTable** table.</span></span>
    - <span data-ttu-id="4384a-148">Tooge esile maksukannete loetelu (**Kannete** andmeallikas), mis asub tabelis **TaxTranse**.</span><span class="sxs-lookup"><span data-stu-id="4384a-148">Fetch the list of tax transactions (**Trans** data source) residing in the **TaxTrans** table:</span></span>
    
        - <span data-ttu-id="4384a-149">Grupeerida sissetoodud kannete loend (**GR** andmeallikas) maksukoodi alusel.</span><span class="sxs-lookup"><span data-stu-id="4384a-149">Group the list of fetched transactions (**Gr** data source) by tax code.</span></span>
        - <span data-ttu-id="4384a-150">Arvutage grupeeritud kanded koondväärtuste järgi maksukoodi kohta järgnevalt.</span><span class="sxs-lookup"><span data-stu-id="4384a-150">Calculate for grouped transactions following aggregated values per tax code:</span></span>

            - <span data-ttu-id="4384a-151">Maksubaasi väärtuste summa.</span><span class="sxs-lookup"><span data-stu-id="4384a-151">Sum of tax base values.</span></span>
            - <span data-ttu-id="4384a-152">Maksuväärtuste summa.</span><span class="sxs-lookup"><span data-stu-id="4384a-152">Sum of tax values.</span></span>
            - <span data-ttu-id="4384a-153">Kohaldatava maksumäära miinimumväärtus.</span><span class="sxs-lookup"><span data-stu-id="4384a-153">Minimum value of applied tax rate.</span></span>

    <span data-ttu-id="4384a-154">Selle konfiguratsiooni mudeli vastendamine rakendab põhiandmete mudelit selle mudeli jaoks loodud ning rakenduse Finance and Operations puhul.</span><span class="sxs-lookup"><span data-stu-id="4384a-154">The model mapping in this configuration implements the base data model for any of the ER formats created for this model and executed in Finance and Operations.</span></span> <span data-ttu-id="4384a-155">Selle tulemusena on **Maksu-** ja **Gr-** andmeallikate sisu avatud ER-vormingute, näiteks abstraktsete andmeallikate puhul.</span><span class="sxs-lookup"><span data-stu-id="4384a-155">As a result, the content of the **Tax** and **Gr** data sources is exposed for ER formats such as abstract data sources.</span></span>

    ![Mudeli vastendamise kujundaja lehekülg, kus kuvatakse maksu-ja Gr-andmeallikad](media/er-calculated-field-type-01.png)

5.  <span data-ttu-id="4384a-157">Sulgege leht **Mudelivastenduse koostaja**.</span><span class="sxs-lookup"><span data-stu-id="4384a-157">Close the **Model mapping designer** page.</span></span>
6.  <span data-ttu-id="4384a-158">Sulgege leht **Mudelivastendus**.</span><span class="sxs-lookup"><span data-stu-id="4384a-158">Close the **Model mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="4384a-159">Läbivaatuse vorming</span><span class="sxs-lookup"><span data-stu-id="4384a-159">Review format</span></span>

1. <span data-ttu-id="4384a-160">Laiendage konfiguratsioonipuus üksuse **Parameetritega kõnede õppimiseks kasutatava mudeli** sisu.</span><span class="sxs-lookup"><span data-stu-id="4384a-160">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="4384a-161">Valige **Vorming parameetritega kõnede õppimiseks**.</span><span class="sxs-lookup"><span data-stu-id="4384a-161">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="4384a-162">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="4384a-162">Select **Designer**.</span></span> <span data-ttu-id="4384a-163">See ER-vormingu vastendus on ette nähtud selleks, et teha järgmist.</span><span class="sxs-lookup"><span data-stu-id="4384a-163">This ER format is designed to do the following:</span></span>

    - <span data-ttu-id="4384a-164">Vastavusseviimiseks väljavõtte loomine.</span><span class="sxs-lookup"><span data-stu-id="4384a-164">Generate a tax statement in XML format.</span></span>
    - <span data-ttu-id="4384a-165">Esitada maksuaruandes järgmised maksustamistasemed: regulaarne, vähendatud ja pole.</span><span class="sxs-lookup"><span data-stu-id="4384a-165">Present the following levels of taxation in the tax statement: regular, reduced, and none.</span></span>
    - <span data-ttu-id="4384a-166">Esitada igal maksustamistasandil mitu üksikasja, millel on igal tasandil erinev arv üksikasju.</span><span class="sxs-lookup"><span data-stu-id="4384a-166">Present multiple details at each taxation level, having a different number of details in each level.</span></span>

    ![Vormingu koostaja leht](media/er-calculated-field-type-02.png)

4. <span data-ttu-id="4384a-168">Valige **Vastendamine**.</span><span class="sxs-lookup"><span data-stu-id="4384a-168">Select **Mapping**.</span></span>
5. <span data-ttu-id="4384a-169">Laiendage üksusi **Mudel**, **Andmed** ja **Kokkuvõte**.</span><span class="sxs-lookup"><span data-stu-id="4384a-169">Expand the **Model**, **Data,** and **Summary** items.</span></span> 

    <span data-ttu-id="4384a-170">Arvutatud väli **Model.Data.Summary.Level** sisaldab avaldist, mis tagastab maksutaseme koodi (**Regulaarne**, **Vähendatud**, **Pole** või **Muu**) tekstiväärtusena mis tahes maksukoodi jaoks, mida saab **Model.Data.Summary** mudelist tuua andmeallika käitusajal.</span><span class="sxs-lookup"><span data-stu-id="4384a-170">The calculated field **Model.Data.Summary.Level** contains the expression that returns the code of the taxation level (**Regular**, **Reduced**, **None,** or **Other**) as a text value for any tax code that can be retrieved from the **Model.Data.Summary** data source at run time.</span></span>

    ![Vormingu kujundaja leht, kus kuvatakse andmemudeli Mudeli üksikasjad parameetriliste kõnede õppimiseks](media/er-calculated-field-type-03.png)

6. <span data-ttu-id="4384a-172">Laiendage üksust **Model**.**Data2**.</span><span class="sxs-lookup"><span data-stu-id="4384a-172">Expand the **Model**.**Data2** item.</span></span>
7. <span data-ttu-id="4384a-173">Laiendage üksust **Model**.**Data2.Summary2**.</span><span class="sxs-lookup"><span data-stu-id="4384a-173">Expand the **Model**.**Data2.Summary2** item.</span></span>
   
    <span data-ttu-id="4384a-174">**Model**.**Data2. Summary2** andmeallikas on konfigureeritud grupeerima **Model.Data.Summary** andmeallika kande üksikasjad maksustamise taseme alusel (tagastab **Model.Data.Summary.Level** arvutatud väli) ja arvutama kokkuvõtted.</span><span class="sxs-lookup"><span data-stu-id="4384a-174">The **Model**.**Data2.Summary2** data source is configured to group the **Model.Data.Summary** data source transaction details by taxation level (returned by the **Model.Data.Summary.Level** calculated field) and compute the aggregations.</span></span>

    ![Vormingu kujundaja leht, kus kuvatakse andmeallika Model.Data2.Summary üksikasjad](media/er-calculated-field-type-04.png)

8. <span data-ttu-id="4384a-176">Vaadake üle arvutatud väljad **Model**.**Data2. Level1**, **Model**.**Data2. Level2** ja **Model**.**Data2. level3.**</span><span class="sxs-lookup"><span data-stu-id="4384a-176">Review the calculated fields **Model**.**Data2.Level1**, **Model**.**Data2.Level2**, and **Model**.**Data2.Level3.**</span></span> <span data-ttu-id="4384a-177">Neid arvutatud välju kasutatakse **Model**.**Data2. Summary2** kirjeteloendi filtreerimiseks ja ainult konkreetse maksustamistaset kajastavate kirjete tagastamiseks.</span><span class="sxs-lookup"><span data-stu-id="4384a-177">These calculated fields are used to filter the **Model**.**Data2.Summary2** records list and return only records that represent a particular taxation level.</span></span>
9. <span data-ttu-id="4384a-178">Sulgege **Vormingu koostaja** leht.</span><span class="sxs-lookup"><span data-stu-id="4384a-178">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="4384a-179">Tuletatud vormingu loomine</span><span class="sxs-lookup"><span data-stu-id="4384a-179">Create a derived format</span></span>
<span data-ttu-id="4384a-180">Esitatud vormingut saate parandada, kui lisate ühe arvutatud välja, et filtreerida nõutavat maksustamistaset, mitte kasutada olemasolevaid kolme välja: **Model**.**Data2.Level1**, **Model**.**Data2.Level2** ja **Mudel**.**Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="4384a-180">You can improve the provided format by adding one calculated field to filter the required taxation level instead of using the existing three fields: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** and **Model**.**Data2.Level3**.</span></span> <span data-ttu-id="4384a-181">Nõutavat maksustamistaset saab määrata asukohas, kus seda uut arvutatud välja nimetatakse.</span><span class="sxs-lookup"><span data-stu-id="4384a-181">The required taxation level can be specified in the location where this new calculated field will be called.</span></span>

1. <span data-ttu-id="4384a-182">Laiendage konfiguratsioonipuus üksuse **Parameetritega kõnede õppimiseks kasutatava mudeli** sisu.</span><span class="sxs-lookup"><span data-stu-id="4384a-182">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="4384a-183">Valige **Vorming parameetritega kõnede õppimiseks**.</span><span class="sxs-lookup"><span data-stu-id="4384a-183">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="4384a-184">Valige **Konfiguratsiooni loomine**.</span><span class="sxs-lookup"><span data-stu-id="4384a-184">Select **Create configuration**.</span></span>
4. <span data-ttu-id="4384a-185">Valige **Tuletage nimest: vormindage parameetritega kõnede õppimiseks, Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="4384a-185">Select **Derive from Name: Format to learn parameterized calls, Microsoft**.</span></span>
5. <span data-ttu-id="4384a-186">Sisestage väljale **Nimi** suvand **Vorming parameetriga (kohandatud) kõnede õppimiseks**.</span><span class="sxs-lookup"><span data-stu-id="4384a-186">In the **Name** field, enter **Format to learn parameterized calls (custom)**.</span></span>
6. <span data-ttu-id="4384a-187">Valige **Konfiguratsiooni loomine.**</span><span class="sxs-lookup"><span data-stu-id="4384a-187">Select **Create configuration.**</span></span>

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a><span data-ttu-id="4384a-188">Parameetrite arvutatud välja konfigureerimine, mis tagastab kirjete loendi</span><span class="sxs-lookup"><span data-stu-id="4384a-188">Configure a parameterized calculated field that returns a list of records</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="4384a-189">Uue arvutatud välja lisamise alustamine</span><span class="sxs-lookup"><span data-stu-id="4384a-189">Start adding a new calculated field</span></span>

1. <span data-ttu-id="4384a-190">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="4384a-190">Select **Designer**.</span></span>
2. <span data-ttu-id="4384a-191">Kõigi vorminguüksuste laiendamiseks valige **Laienda/ahenda**.</span><span class="sxs-lookup"><span data-stu-id="4384a-191">Select **Expand/collapse** to expand all format items.</span></span>
3. <span data-ttu-id="4384a-192">Valige **Vastendamine**.</span><span class="sxs-lookup"><span data-stu-id="4384a-192">Select **Mapping**.</span></span>
4. <span data-ttu-id="4384a-193">Laiendage üksust **Mudel**.</span><span class="sxs-lookup"><span data-stu-id="4384a-193">Expand the **Model** item.</span></span>
5. <span data-ttu-id="4384a-194">Valige üksus **Model.Data2**.</span><span class="sxs-lookup"><span data-stu-id="4384a-194">Select the **Model.Data2** item.</span></span>
6. <span data-ttu-id="4384a-195">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="4384a-195">Select **Add**.</span></span>
7. <span data-ttu-id="4384a-196">Valige **Funktsioonid\\Arvutatud väli**.</span><span class="sxs-lookup"><span data-stu-id="4384a-196">Select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="4384a-197">Väljale **Nimi** sisestage **Tasemed**.</span><span class="sxs-lookup"><span data-stu-id="4384a-197">In the **Name** field, enter **Levels**.</span></span>
9. <span data-ttu-id="4384a-198">Valige **Valemi redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="4384a-198">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="4384a-199">Arvutatud välja lisamise parameetri määratlemine</span><span class="sxs-lookup"><span data-stu-id="4384a-199">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="4384a-200">Valige **Parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="4384a-200">Select **Parameters**.</span></span>
2. <span data-ttu-id="4384a-201">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="4384a-201">Select **New**.</span></span>
3. <span data-ttu-id="4384a-202">Väljale **Nimi** sisestage väärtus **Maksustamise tase**.</span><span class="sxs-lookup"><span data-stu-id="4384a-202">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="4384a-203">Valige väljalt **Tüüp** suvand **String**.</span><span class="sxs-lookup"><span data-stu-id="4384a-203">In the **Type** field, select **String**.</span></span>

    <span data-ttu-id="4384a-204">Parameetri argumendi tüübi määramiseks saab kasutada ainult primitiivseid andmetüüpe.</span><span class="sxs-lookup"><span data-stu-id="4384a-204">Only primitive data types can be used to specify the type of the parameter’s argument.</span></span> <span data-ttu-id="4384a-205">Seetõttu ei saa tüüpe **Kirjeloend**, **Kirje** ja **Loetelu** sel eesmärgil kasutada.</span><span class="sxs-lookup"><span data-stu-id="4384a-205">Therefore, **Record list**, **Record**, and **Enum** types cannot be used for this purpose.</span></span>

    <span data-ttu-id="4384a-206">Ühe arvutatud välja jaoks määratud maksimaalne parameetrite arv on 8.</span><span class="sxs-lookup"><span data-stu-id="4384a-206">The maximum number of parameters that can be specified for a single calculated field is 8.</span></span>

    ![Parameetrite andmeallika loend](media/er-calculated-field-type-05.png)

5. <span data-ttu-id="4384a-208">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="4384a-208">Select **OK**.</span></span>

<span data-ttu-id="4384a-209">Selle parameetri lisamisega määratlete tingimuse, mis peab olema kasutusel selle arvutatud välja nimetamiseks.</span><span class="sxs-lookup"><span data-stu-id="4384a-209">By adding this parameter, you specify the condition that must be in place to call this calculated field.</span></span> <span data-ttu-id="4384a-210">Kui nimetate seda arvutatud välja, peate määrama parameetri **Maksustamistase** argumendi väärtusena vorminguga **String**.</span><span class="sxs-lookup"><span data-stu-id="4384a-210">When you call this calculated field, you need to specify the argument of the **Taxation Level** parameter as a value with **String** format.</span></span>

   <span data-ttu-id="4384a-211">Veenduge, et määratlete parameetrid ainult nende arvutatud väljade jaoks, mis asuvad konteineris ( **kas kirje loend**, **kirje**või **konteiner**).</span><span class="sxs-lookup"><span data-stu-id="4384a-211">Make sure that you define parameters only for those calculated fields that reside in a container (either **Record list**, **Record**, or **Container**).</span></span>

   <span data-ttu-id="4384a-212">Konfigureeritud parameeter on saadaval selle arvutatud välja andmeallikate loendis.</span><span class="sxs-lookup"><span data-stu-id="4384a-212">The configured parameter is available in the list of data sources for this calculated field.</span></span> <span data-ttu-id="4384a-213">Parameetri lisamiseks konfigureeritud avaldisse Saate klõpsata käsku **lisa andmeallikas.**</span><span class="sxs-lookup"><span data-stu-id="4384a-213">You can add the parameter to the configured expression by selecting **Add data source**.</span></span>

   ![Andmeallika väljad](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="4384a-215">Arvutatud välja lisamise väljendi määratlemine</span><span class="sxs-lookup"><span data-stu-id="4384a-215">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="4384a-216">Sisestage väljale **Valem**:</span><span class="sxs-lookup"><span data-stu-id="4384a-216">In the **Formula** field, enter:</span></span> 

    <span data-ttu-id="4384a-217">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span><span class="sxs-lookup"><span data-stu-id="4384a-217">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span></span>
    
2. <span data-ttu-id="4384a-218">Valige andmeallikate loendis **Maksustamistaseme** parameeter.</span><span class="sxs-lookup"><span data-stu-id="4384a-218">Select the **Taxation Level** parameter in the list of data sources.</span></span>
3. <span data-ttu-id="4384a-219">Valige **Andmeallika lisamine**.</span><span class="sxs-lookup"><span data-stu-id="4384a-219">Select **Add data source**.</span></span>
4. <span data-ttu-id="4384a-220">Väljal **Valem** viimistlege avaldis järgmiselt:</span><span class="sxs-lookup"><span data-stu-id="4384a-220">In the **Formula** field, finalize the expression as:</span></span>  

    <span data-ttu-id="4384a-221">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span><span class="sxs-lookup"><span data-stu-id="4384a-221">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span></span>

5. <span data-ttu-id="4384a-222">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="4384a-222">Select **Save**.</span></span>

    ![Andmeallika välja teave](media/er-calculated-field-type-07.png)

6. <span data-ttu-id="4384a-224">Sulgege **Valemikoostaja** leht.</span><span class="sxs-lookup"><span data-stu-id="4384a-224">Close the **Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="4384a-225">Uue arvutatud välja lisamise alustamine</span><span class="sxs-lookup"><span data-stu-id="4384a-225">Finish adding a new calculated field</span></span>

- <span data-ttu-id="4384a-226">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="4384a-226">Select **OK**.</span></span>

<span data-ttu-id="4384a-227">Lehel **Vormingu koostaja** nõuab konfigureeritud parameetritega arvutatud väli **Tasemed** argumenti **String**.</span><span class="sxs-lookup"><span data-stu-id="4384a-227">On the **Format designer** page, the configured parameterized calculated field **Levels** requires a **String** argument.</span></span>

![Arvutatud välja tasemete laiendatud loend](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements"></a><span data-ttu-id="4384a-229">Kasutage siduva vormingu elementide jaoks konfigureeritud arvutatud välja.</span><span class="sxs-lookup"><span data-stu-id="4384a-229">Use the configured calculated field for binding format elements</span></span>

1. <span data-ttu-id="4384a-230">Valige **Model.Data2.Levels**, et valida konfigureeritud arvutatud väli.</span><span class="sxs-lookup"><span data-stu-id="4384a-230">Select **Model.Data2.Levels** to select the configured calculated field.</span></span>
2. <span data-ttu-id="4384a-231">Valige **Statement.Taxation.Regular** vormingu element.</span><span class="sxs-lookup"><span data-stu-id="4384a-231">Select the **Statement.Taxation.Regular** format element.</span></span>
3. <span data-ttu-id="4384a-232">Valige **Seo**.</span><span class="sxs-lookup"><span data-stu-id="4384a-232">Select **Bind**.</span></span>
4. <span data-ttu-id="4384a-233">Valige **Jah**, et kinnitada praegu kasutatava andmeallika **Tase1** asendamist uue andmeallikaga **Tasemed** kõigis valitud vorminguelemendi pesastatud vorminguelementides.</span><span class="sxs-lookup"><span data-stu-id="4384a-233">Select **Yes** to confirm the replacement of the currently used data source, **Level1**, by the new data source, **Levels**, in all nested format elements of the selected format element.</span></span>

    <span data-ttu-id="4384a-234">Rakendatud sidumine on loodud parameetrina arvutatud välja kutsena.</span><span class="sxs-lookup"><span data-stu-id="4384a-234">Applied binding has been built as a call of the parameterized calculated field.</span></span> <span data-ttu-id="4384a-235">Vaikimisi kasutatakse seotud vormingu elemendi nime parameetrina arvutatud välja argumendina järgmistel tingimustel:</span><span class="sxs-lookup"><span data-stu-id="4384a-235">By default, the name of the bound format element is used as an argument for parameterized calculated field under the following conditions:</span></span>

      - <span data-ttu-id="4384a-236">Arvutatud väli on konfigureeritud kasutama ühte parameetrit.</span><span class="sxs-lookup"><span data-stu-id="4384a-236">The calculated field is configured to use a single parameter.</span></span>
      - <span data-ttu-id="4384a-237">Selle parameetri andmetüüp määratletakse **Stringina**.</span><span class="sxs-lookup"><span data-stu-id="4384a-237">The data type of this parameter is defined as **String**.</span></span>

    <span data-ttu-id="4384a-238">Kui seotud vormingu elemendi nimi on tühi, kasutatakse selle elemendi andmeallika nime rakendatud sidumises.</span><span class="sxs-lookup"><span data-stu-id="4384a-238">When the name of the bound format element is blank, the data source name of this element is used in applied binding.</span></span>

5. <span data-ttu-id="4384a-239">Valige **Statement.Taxation.Reduced** vormingu element.</span><span class="sxs-lookup"><span data-stu-id="4384a-239">Select the **Statement.Taxation.Reduced** format element.</span></span>
6. <span data-ttu-id="4384a-240">Valige **Seo**.</span><span class="sxs-lookup"><span data-stu-id="4384a-240">Select **Bind**.</span></span>
7. <span data-ttu-id="4384a-241">Valige **Jah**, et kinnitada praegu kasutatava andmeallika **Tase2** asendamist uue andmeallikaga **Tasemed** kõigis valitud vorminguelemendi pesastatud vorminguelementides.</span><span class="sxs-lookup"><span data-stu-id="4384a-241">Select **Yes** to confirm the replacement of the currently used data source, **Level2**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>
8. <span data-ttu-id="4384a-242">Valige **Statement.Taxation.None** vormingu element.</span><span class="sxs-lookup"><span data-stu-id="4384a-242">Select the **Statement.Taxation.None** format element.</span></span>
9. <span data-ttu-id="4384a-243">Valige **Seo**.</span><span class="sxs-lookup"><span data-stu-id="4384a-243">Select **Bind**.</span></span>
10. <span data-ttu-id="4384a-244">Valige **Jah**, et kinnitada praegu kasutatava andmeallika **Tase3** asendamist uue andmeallikaga **Tasemed** kõigis valitud vorminguelemendi pesastatud vorminguelementides.</span><span class="sxs-lookup"><span data-stu-id="4384a-244">Select **Yes** to confirm the replacement of the currently used data source, **Level3**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>

   <span data-ttu-id="4384a-245">Kui määrate argumendi parameetri arvutatud välja kohta XML-elemendi jaoks, mis tähistab maksustamistaset (nt **Model.Data2.Levels („Vähendatud”)** teksti väärtusena), ei pea te sama tegema pesastatud XML-atribuutide puhul – nende sidumised pärivad automaatselt ematasemel (**Model.Data2.Levels.aggregated.Base**, mitte **Model.Data2.Levels („Vähendatud”).aggregated.Base**).</span><span class="sxs-lookup"><span data-stu-id="4384a-245">When you specify the argument of the parameterized calculated field for the XML element representing taxation level (for example, **Model.Data2.Levels("Reduced")** as a text value), you don’t need to do the same for nested XML attributes—their bindings will automatically inherit the value of the argument defined on the parent level (**Model.Data2.Levels.aggregated.Base**, not **Model.Data2.Levels("Reduced").aggregated.Base**).</span></span>

<span data-ttu-id="4384a-246">Parameetritega arvutatud välja korduvaid kõnesid ei toetata.</span><span class="sxs-lookup"><span data-stu-id="4384a-246">Recurrent calls of any parameterized calculated field are not supported.</span></span>

<span data-ttu-id="4384a-247">Saate valida **Redigeeri valemit** ja muuta valitud sidumise parameetritega arvutatud välja vaikimisi rakendatud argumenti.</span><span class="sxs-lookup"><span data-stu-id="4384a-247">You can select **Edit formula**, and change the applied-by-default argument of the parameterized calculated field in the selected binding.</span></span> <span data-ttu-id="4384a-248">Kui see argument on puudu, võib see põhjustada tõrkeid käitusajal — kasutajat teavitatakse sellisest olukorrast, kui on kehtiv vorming on kontrollitud.</span><span class="sxs-lookup"><span data-stu-id="4384a-248">If this argument is missing, it can cause errors at run time — users are informed about such a situation when the current format is validated.</span></span>

![Kinnitamise hoiatuse teatis](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a><span data-ttu-id="4384a-250">Parameetritega arvutatud välja konfigureerimine kirje tagastamiseks</span><span class="sxs-lookup"><span data-stu-id="4384a-250">Configure a parameterized calculated field to return a record</span></span>
<span data-ttu-id="4384a-251">Kui parameetritega arvutatud väli tagastab kirje, peate elementide vormindamiseks toetama selle kirje üksikute väljade sidumist.</span><span class="sxs-lookup"><span data-stu-id="4384a-251">When a parameterized calculated field returns a record, you need to support binding of individual fields of this record to format elements.</span></span> <span data-ttu-id="4384a-252">Sellisel juhul puudub ülataseme sidumine, mis sisaldab parameetritega arvutatud välja kutsumise argumendi väärtust – see väärtus tuleb määratleda ühe kirje välja sidumisel.</span><span class="sxs-lookup"><span data-stu-id="4384a-252">In such cases there will be no parent binding that contains the value of an argument to call a parameterized calculated field — this value must be defined in the binding of a single record’s field.</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="4384a-253">Uue arvutatud välja lisamise alustamine</span><span class="sxs-lookup"><span data-stu-id="4384a-253">Start adding a new calculated field</span></span>

1. <span data-ttu-id="4384a-254">Valige üksus **Model.Data2**.</span><span class="sxs-lookup"><span data-stu-id="4384a-254">Select the **Model.Data2** item.</span></span>
2. <span data-ttu-id="4384a-255">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="4384a-255">Select **Add**.</span></span>
3. <span data-ttu-id="4384a-256">Valige **Funktsioonid\\Arvutatud väli**.</span><span class="sxs-lookup"><span data-stu-id="4384a-256">Select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="4384a-257">Sisestage väljale **Nimi** suvand **LevelRecord**.</span><span class="sxs-lookup"><span data-stu-id="4384a-257">In the **Name** field, enter **LevelRecord**.</span></span>
5. <span data-ttu-id="4384a-258">Valige **Valemi redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="4384a-258">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="4384a-259">Arvutatud välja lisamise parameetri määratlemine</span><span class="sxs-lookup"><span data-stu-id="4384a-259">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="4384a-260">Valige **Parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="4384a-260">Select **Parameters**.</span></span>
2. <span data-ttu-id="4384a-261">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="4384a-261">Select **New**.</span></span>
3. <span data-ttu-id="4384a-262">Väljale **Nimi** sisestage väärtus **Maksustamise tase**.</span><span class="sxs-lookup"><span data-stu-id="4384a-262">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="4384a-263">Valige väljalt **Tüüp** suvand **String**.</span><span class="sxs-lookup"><span data-stu-id="4384a-263">In the **Type** field, select **String**.</span></span>
5. <span data-ttu-id="4384a-264">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="4384a-264">Select **OK**.</span></span>

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="4384a-265">Arvutatud välja lisamise väljendi määratlemine</span><span class="sxs-lookup"><span data-stu-id="4384a-265">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="4384a-266">Sisestage väljale **Valem** järgmine tekst.</span><span class="sxs-lookup"><span data-stu-id="4384a-266">In the **Formula** field, enter the following:</span></span>  
    
    <span data-ttu-id="4384a-267">**FIRSTORNULL(\@.Levels(**</span><span class="sxs-lookup"><span data-stu-id="4384a-267">**FIRSTORNULL(\@.Levels(**</span></span>

2. <span data-ttu-id="4384a-268">Valige **Maksustamistaseme** parameeter.</span><span class="sxs-lookup"><span data-stu-id="4384a-268">Select the **Taxation Level** parameter.</span></span>
3. <span data-ttu-id="4384a-269">Valige **Andmeallika lisamine**.</span><span class="sxs-lookup"><span data-stu-id="4384a-269">Select **Add data source**.</span></span>
4. <span data-ttu-id="4384a-270">Väljale **Valem** lisage **„Maksustamistase”))**, mis on sisestatud juhises 1, et lõpetada avaldis:</span><span class="sxs-lookup"><span data-stu-id="4384a-270">In the **Formula** field, append **'Taxation Level'))** to what you entered in Step 1 to finalize the expression to:</span></span>  
    
    <span data-ttu-id="4384a-271">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span><span class="sxs-lookup"><span data-stu-id="4384a-271">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span></span>

5. <span data-ttu-id="4384a-272">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="4384a-272">Select **Save**.</span></span>
6. <span data-ttu-id="4384a-273">Sulgege **Valemikoostaja** leht.</span><span class="sxs-lookup"><span data-stu-id="4384a-273">Close **the Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="4384a-274">Uue arvutatud välja lisamise alustamine</span><span class="sxs-lookup"><span data-stu-id="4384a-274">Finish adding a new calculated field</span></span>

-   <span data-ttu-id="4384a-275">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="4384a-275">Select **OK**.</span></span>

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a><span data-ttu-id="4384a-276">Kasutage siduva vormingu elementide jaoks konfigureeritud arvutatud välja.</span><span class="sxs-lookup"><span data-stu-id="4384a-276">Use the configured calculated field to bind format elements</span></span>

1. <span data-ttu-id="4384a-277">Laiendage välja **Model.Data2.LevelRecord**, et valida konfigureeritud arvutatud väli.</span><span class="sxs-lookup"><span data-stu-id="4384a-277">Expand **Model.Data2.LevelRecord** to select the configured calculated field.</span></span>
2. <span data-ttu-id="4384a-278">Laiendage välja **Model.Data2.aggregated**, et valida konfigureeritud arvutatud välja ümbris.</span><span class="sxs-lookup"><span data-stu-id="4384a-278">Expand the **Model.Data2.LevelRecord.aggregated** container of the configured calculated field.</span></span>
3. <span data-ttu-id="4384a-279">Valige **Model. Data2. LevelRecord.aggregated.Base** väli.</span><span class="sxs-lookup"><span data-stu-id="4384a-279">Select the **Model.Data2.LevelRecord.aggregated.Base** field.</span></span>
4. <span data-ttu-id="4384a-280">Valige **Statement.Taxation.None** vormingu element.</span><span class="sxs-lookup"><span data-stu-id="4384a-280">Select the **Statement.Taxation.None** format element.</span></span>
5. <span data-ttu-id="4384a-281">Valige **Tühista sidumine**.</span><span class="sxs-lookup"><span data-stu-id="4384a-281">Select **Unbind**.</span></span>
6. <span data-ttu-id="4384a-282">Valige **Statement.Taxation.None.Base** vormingu element.</span><span class="sxs-lookup"><span data-stu-id="4384a-282">Select the **Statement.Taxation.None.Base** format element.</span></span>
7. <span data-ttu-id="4384a-283">Valige **Seo**.</span><span class="sxs-lookup"><span data-stu-id="4384a-283">Select **Bind**.</span></span>
8. <span data-ttu-id="4384a-284">Valige **Valemi redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="4384a-284">Select **Edit formula**.</span></span>
9. <span data-ttu-id="4384a-285">Muutke avaldiseks **Model.Data2.LevelRecord („Pole”).aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="4384a-285">Change the expression to **Model.Data2.LevelRecord("None").aggregated.Base**.</span></span>

![Värskendatud avaldis](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a><span data-ttu-id="4384a-287">Eemaldage arvutatud väljad, mida ei kasutata</span><span class="sxs-lookup"><span data-stu-id="4384a-287">Remove calculated fields that are not used</span></span>

1. <span data-ttu-id="4384a-288">Valige **Model.Data2.Level1**.</span><span class="sxs-lookup"><span data-stu-id="4384a-288">Select **Model.Data2.Level1**.</span></span>
2. <span data-ttu-id="4384a-289">Valige **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="4384a-289">Select **Delete**.</span></span>
3. <span data-ttu-id="4384a-290">Valige **Model.Data2.Level2**.</span><span class="sxs-lookup"><span data-stu-id="4384a-290">Select **Model.Data2.Level2**.</span></span>
4. <span data-ttu-id="4384a-291">Valige **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="4384a-291">Select **Delete**.</span></span>
5. <span data-ttu-id="4384a-292">Valige **Model.Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="4384a-292">Select **Model.Data2.Level3**.</span></span>
6. <span data-ttu-id="4384a-293">Valige **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="4384a-293">Select **Delete**.</span></span>
7. <span data-ttu-id="4384a-294">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="4384a-294">Select **Save**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="4384a-295">Kasutasite uuesti sama arvutatud välja **Model.Data2.Levels** mitu korda vormingu sidumistes.</span><span class="sxs-lookup"><span data-stu-id="4384a-295">You reused the same calculated field **Model.Data2.Levels** several times in format bindings.</span></span> <span data-ttu-id="4384a-296">Mitme sarnase välja asemel on palju lihtsam kasutada ja hallata üksikut arvutatud välja.</span><span class="sxs-lookup"><span data-stu-id="4384a-296">It is much easier to use and maintain a single calculated field instead of doing this for multiple similar fields.</span></span>

8. <span data-ttu-id="4384a-297">Sulgege **Vormingu koostaja** leht.</span><span class="sxs-lookup"><span data-stu-id="4384a-297">Close the **Format designer** page.</span></span>

## <a name="complete-adjusted-version-of-a-derived-format"></a><span data-ttu-id="4384a-298">Tuletatud vormingu kohandatud versiooni lõpetamine</span><span class="sxs-lookup"><span data-stu-id="4384a-298">Complete adjusted version of a derived format</span></span>

1. <span data-ttu-id="4384a-299">Vahekaardil **Versioonid** valige **Muuda olekut**.</span><span class="sxs-lookup"><span data-stu-id="4384a-299">In the **Versions** FastTab, select **Change status**.</span></span>
2. <span data-ttu-id="4384a-300">Valige **Lõpeta**.</span><span class="sxs-lookup"><span data-stu-id="4384a-300">Select **Complete**.</span></span>

## <a name="export-completed-version-of-a-derived-format"></a><span data-ttu-id="4384a-301">Tuletatud vormingu lõpuleviidud versiooni eksportimine</span><span class="sxs-lookup"><span data-stu-id="4384a-301">Export completed version of a derived format</span></span>

1. <span data-ttu-id="4384a-302">Valige konfiguratsioonipuus  **Vorminda parameetritega kõnede õppimiseks (kohandatud)**.</span><span class="sxs-lookup"><span data-stu-id="4384a-302">Select **Format to learn parameterized calls (custom)** format in the configurations tree.</span></span>
2. <span data-ttu-id="4384a-303">Vahekaardil **Versioonid** valige lõpule viidud versioon 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="4384a-303">In the **Versions** FastTab, select the completed version 1.1.1.</span></span>
3. <span data-ttu-id="4384a-304">Valige **Exchange**.</span><span class="sxs-lookup"><span data-stu-id="4384a-304">Select **Exchange**.</span></span>
4. <span data-ttu-id="4384a-305">Valige **Ekspordi XML-failina**.</span><span class="sxs-lookup"><span data-stu-id="4384a-305">Select **Export as XML file**.</span></span>
5. <span data-ttu-id="4384a-306">Salvestage allalaaditud konfiguratsioon kohapeal, XML-vormingus.</span><span class="sxs-lookup"><span data-stu-id="4384a-306">Store the downloaded configuration locally, in XML format.</span></span>

## <a name="test-er-formats"></a><span data-ttu-id="4384a-307">Katsetage ER-vorminguid</span><span class="sxs-lookup"><span data-stu-id="4384a-307">Test ER formats</span></span> 
<span data-ttu-id="4384a-308">Saate käivitada algsed ja täiustatud ER-vormingud veendumaks, et konfigureeritud parameetritega arvutatud väljad töötavad õigesti.</span><span class="sxs-lookup"><span data-stu-id="4384a-308">You can run the initial and improved ER formats to make sure that configured parameterized calculated fields work properly.</span></span>

### <a name="import-er-configurations"></a><span data-ttu-id="4384a-309">Elektroonilise aruandluse konfiguratsioonide importimine</span><span class="sxs-lookup"><span data-stu-id="4384a-309">Import ER configurations</span></span>
<span data-ttu-id="4384a-310">Läbivaadatud konfiguratsioone saate RCS-ist importida tüübi **RCS** ER-hoidla abil.</span><span class="sxs-lookup"><span data-stu-id="4384a-310">You can import reviewed configurations from RCS by using the ER repository of the **RCS** type.</span></span> <span data-ttu-id="4384a-311">Kui te juba läbisite teemas toodud juhised [Elektroonilise aruandluse (ER) konfiguratsioonide importimine teenusest Regulatory Configuration Services (RCS)](rcs-download-configurations.md), kasutage konfigureeritud ER-hoidlat, et importida selles teemas varem arutatud konfiguratsioonid oma keskkonda.</span><span class="sxs-lookup"><span data-stu-id="4384a-311">If you already went through the steps in the topic, [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](rcs-download-configurations.md), use the configured ER repository to import configurations discussed earlier in this topic to your environment.</span></span> <span data-ttu-id="4384a-312">Muul juhul toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="4384a-312">Otherwise, follow these steps:</span></span>

1. <span data-ttu-id="4384a-313">Valige ettevõte **DEMF** ja valige vaikearmatuurlaual **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="4384a-313">Select the **DEMF** company and on the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="4384a-314">Valige **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="4384a-314">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="4384a-315">Importige konfiguratsioonid Microsofti allalaadimiskeskusest järgmises järjestuses: andmemudel, mudelivastendus, vorming.</span><span class="sxs-lookup"><span data-stu-id="4384a-315">Import the configurations from Microsoft Download Center in the following sequence: data model, model mapping, format.</span></span> <span data-ttu-id="4384a-316">Täitke järgmised sammud iga ER-konfiguratsiooni puhul:</span><span class="sxs-lookup"><span data-stu-id="4384a-316">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="4384a-317">Valige **Vaheta**.</span><span class="sxs-lookup"><span data-stu-id="4384a-317">Select **Exchange.**</span></span>
    2. <span data-ttu-id="4384a-318">Valige **Laadi XML-failist**.</span><span class="sxs-lookup"><span data-stu-id="4384a-318">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="4384a-319">Valige käsk **Sirvi**, et valida nõutav ER-i konfiguratsioon XML-vormingus.</span><span class="sxs-lookup"><span data-stu-id="4384a-319">Select **Browse** to select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="4384a-320">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="4384a-320">Select **OK**.</span></span>

4. <span data-ttu-id="4384a-321">Importige eksporditud RCS-i lõpule viidud versioon 1.1.1 vormingust **Vorminda parameetritega kõnede õppimiseks (kohandatud)**:</span><span class="sxs-lookup"><span data-stu-id="4384a-321">Import the exported from RCS completed version 1.1.1 of the **Format to learn parameterized calls (custom)** format:</span></span>

    1. <span data-ttu-id="4384a-322">Valige **Vaheta**.</span><span class="sxs-lookup"><span data-stu-id="4384a-322">Select **Exchange.**</span></span>
    2. <span data-ttu-id="4384a-323">Valige **Laadi XML-failist**.</span><span class="sxs-lookup"><span data-stu-id="4384a-323">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="4384a-324">Valige **Sirvi**, et valida kohalikult salvestatud **Vorminda parameetritega kõnede õppimiseks (kohandatud)** fail XML-vormingus.</span><span class="sxs-lookup"><span data-stu-id="4384a-324">Select **Browse** to select the locally stored **Format to learn parameterized calls (custom)** file in XML format.</span></span>
    4. <span data-ttu-id="4384a-325">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="4384a-325">Select **OK**.</span></span>

### <a name="run-er-formats"></a><span data-ttu-id="4384a-326">ER-vormingute käivitamine</span><span class="sxs-lookup"><span data-stu-id="4384a-326">Run ER formats</span></span>

1. <span data-ttu-id="4384a-327">Laiendage konfiguratsioonipuus üksuse **Parameetritega kõnede õppimiseks kasutatava mudeli** sisu.</span><span class="sxs-lookup"><span data-stu-id="4384a-327">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="4384a-328">Valige **Vorming parameetritega kõnede õppimiseks**.</span><span class="sxs-lookup"><span data-stu-id="4384a-328">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="4384a-329">Valige kõige ülemisel ribal **Käivita**.</span><span class="sxs-lookup"><span data-stu-id="4384a-329">Select **Run** on the top-most ribbon.</span></span>
4. <span data-ttu-id="4384a-330">Salvestage kohapeal loodud väljund.</span><span class="sxs-lookup"><span data-stu-id="4384a-330">Save the locally generated output.</span></span>
5. <span data-ttu-id="4384a-331">Valige üksus **Vorminda parameetritega kõnede õppimiseks (kohandatud)**.</span><span class="sxs-lookup"><span data-stu-id="4384a-331">Select the **Format to learn parameterized calls (custom)** item.</span></span>
6. <span data-ttu-id="4384a-332">Valige kõige ülemisel ribal **Käivita**.</span><span class="sxs-lookup"><span data-stu-id="4384a-332">Select **Run** on the top-most ribbon.</span></span>
7. <span data-ttu-id="4384a-333">Salvestage loodud väljund kohapeal.</span><span class="sxs-lookup"><span data-stu-id="4384a-333">Save the generated output locally.</span></span> 
8. <span data-ttu-id="4384a-334">Võrrelge loodud väljundite sisu.</span><span class="sxs-lookup"><span data-stu-id="4384a-334">Compare the contents of the generated outputs.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4384a-335">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="4384a-335">Additional resources</span></span>
[<span data-ttu-id="4384a-336">Valemikoostaja elektroonilises aruandluses (ER)</span><span class="sxs-lookup"><span data-stu-id="4384a-336">Formula designer in Electronic reporting (ER)</span></span>](general-electronic-reporting-formula-designer.md)
