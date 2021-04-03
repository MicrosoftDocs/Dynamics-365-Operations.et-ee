---
title: Arvutatud väljatüübi ER-andmeallikate parameetritega kõned
description: See teema annab teavet selle kohta, kuidas kasutada arvutatud väljatüüpi ER-andmeallikate puhul.
author: NickSelin
manager: AnnBe
ms.date: 08/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 1c2c13cd3f165826e0d5b5ac901ffa61895301e7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569197"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a><span data-ttu-id="09c37-103">Arvutatud väljatüübi ER-andmeallikate parameetritega kõned</span><span class="sxs-lookup"><span data-stu-id="09c37-103">Support parameterized calls of ER data sources of the Calculated field type</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="09c37-104">See teema selgitab, kuidas saate kujundada elektroonilise aruandluse (ER) andmeallikat, kasutades tüüpi **Arvutatud väli**.</span><span class="sxs-lookup"><span data-stu-id="09c37-104">This topic explains how you can design an Electronic reporting (ER) data source by using the **Calculated field** type.</span></span> <span data-ttu-id="09c37-105">See andmeallikas võib sisaldada ER-avaldist, mida käivitamisel saab juhtida seda andmeallikat nimetavas sidumises konfigureeritud parameetriargumentide väärtustega.</span><span class="sxs-lookup"><span data-stu-id="09c37-105">This data source may contain an ER expression that, when executed, can be controlled by the values of the parameter arguments that are configured in a binding that calls this data source.</span></span> <span data-ttu-id="09c37-106">Sellise andmeallika parameeteriseeritud kõnede konfigureerimisega saate ühte andmeallikat mitmes sidumises uuesti kasutada, mis vähendab ER-mudeli vastendustes või ER-vormingutes konfigureeritavate andmeallikate koguarvu.</span><span class="sxs-lookup"><span data-stu-id="09c37-106">By configuring parameterized calls of such a data source, you can reuse a single data source in many bindings, which reduces the total number of data sources that must be configured in ER model mappings or ER formats.</span></span> <span data-ttu-id="09c37-107">See lihtsustab ka konfigureeritud ER-komponenti, mis vähendab hoolduskulusid ja teiste tarbijate kasutuskulusid.</span><span class="sxs-lookup"><span data-stu-id="09c37-107">It also simplifies the configured ER component, which reduces the maintenance costs and the cost of use by other consumers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="09c37-108">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="09c37-108">Prerequisites</span></span>
<span data-ttu-id="09c37-109">Selles teemas näidete lõpuleviimiseks peavad teil olema järgmised juurdepääsuõigused.</span><span class="sxs-lookup"><span data-stu-id="09c37-109">To complete the examples in this topic, you must have the following access:</span></span>

- <span data-ttu-id="09c37-110">Juurdepääs ühele neist rollidest:</span><span class="sxs-lookup"><span data-stu-id="09c37-110">Access to one of these roles:</span></span>

    - <span data-ttu-id="09c37-111">Elektroonilise aruandluse arendaja</span><span class="sxs-lookup"><span data-stu-id="09c37-111">Electronic reporting developer</span></span>
    - <span data-ttu-id="09c37-112">Elektroonilise aruandluse funktsionaalne konsultant</span><span class="sxs-lookup"><span data-stu-id="09c37-112">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="09c37-113">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="09c37-113">System administrator</span></span>

- <span data-ttu-id="09c37-114">Juurdepääs teenustele Regulatory Configuration Services (RCS), mis on ette valmistatud sama rentniku jaoks, nagu rakendus Finance and Operations, ühe järgmise rolli jaoks.</span><span class="sxs-lookup"><span data-stu-id="09c37-114">Access to Regulatory Configuration Services (RCS) that have been provisioned for the same tenant as Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="09c37-115">Elektroonilise aruandluse arendaja</span><span class="sxs-lookup"><span data-stu-id="09c37-115">Electronic reporting developer</span></span>
    - <span data-ttu-id="09c37-116">Elektroonilise aruandluse funktsionaalne konsultant</span><span class="sxs-lookup"><span data-stu-id="09c37-116">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="09c37-117">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="09c37-117">System administrator</span></span>

<span data-ttu-id="09c37-118">Samuti peate alla laadima ja kohalikult talletama järgmised failid.</span><span class="sxs-lookup"><span data-stu-id="09c37-118">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="09c37-119">**Sisu**</span><span class="sxs-lookup"><span data-stu-id="09c37-119">**Content**</span></span>                           | <span data-ttu-id="09c37-120">**Faili nimi**</span><span class="sxs-lookup"><span data-stu-id="09c37-120">**File name**</span></span>                                        |
|---------------------------------------|------------------------------------------------------|
| <span data-ttu-id="09c37-121">ER-i andmemudeli konfiguratsiooni näide</span><span class="sxs-lookup"><span data-stu-id="09c37-121">Sample ER data model configuration</span></span>    | [<span data-ttu-id="09c37-122">Mudel parameetritega calls.version.1.xml õppimiseks</span><span class="sxs-lookup"><span data-stu-id="09c37-122">Model to learn parameterized calls.version.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)     |
| <span data-ttu-id="09c37-123">ER-i metaandmete konfiguratsiooni näide</span><span class="sxs-lookup"><span data-stu-id="09c37-123">Sample ER metadata configuration</span></span>      | [<span data-ttu-id="09c37-124">Metaandmed parameetritega calls.version.1.xml õppimiseks</span><span class="sxs-lookup"><span data-stu-id="09c37-124">Metadata to learn parameterized calls.version.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |
| <span data-ttu-id="09c37-125">ER-i mudelivastenduse konfiguratsiooni näide</span><span class="sxs-lookup"><span data-stu-id="09c37-125">Sample ER model mapping configuration</span></span> | [<span data-ttu-id="09c37-126">Vastendamine parameetritega calls.version.1.xml õppimiseks</span><span class="sxs-lookup"><span data-stu-id="09c37-126">Mapping to learn parameterized calls.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="09c37-127">ER-vormingu konfiguratsiooni näide</span><span class="sxs-lookup"><span data-stu-id="09c37-127">Sample ER format configuration</span></span>        | [<span data-ttu-id="09c37-128">Vorming parameetritega calls.version.1.xml õppimiseks</span><span class="sxs-lookup"><span data-stu-id="09c37-128">Format to learn parameterized calls.version.1.1.xml</span></span>](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |

## <a name="sign-in-to-your-rcs-instance"></a><span data-ttu-id="09c37-129">Logige sisse oma RCS-eksemplari.</span><span class="sxs-lookup"><span data-stu-id="09c37-129">Sign in to your RCS instance</span></span>
<span data-ttu-id="09c37-130">Selles näites loote konfiguratsiooni näidisettevõtte Litware, Inc. jaoks. Esmalt peate RCS-is täitma teemas [Konfiguratsiooni pakkujate loomine ja nende aktiivseks märkimine](tasks/er-configuration-provider-mark-it-active-2016-11.md) toodud juhised.</span><span class="sxs-lookup"><span data-stu-id="09c37-130">In this example, you will create a configuration for the sample company, Litware, Inc. First, in RCS, you must complete the steps in the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure:</span></span>

1. <span data-ttu-id="09c37-131">Valige vaikimisi armatuurlaual **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="09c37-131">On the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="09c37-132">Valige **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="09c37-132">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="09c37-133">Importige allalaaditud konfiguratsioonid RCS-i järgmises järjestuses: andmemudel, metaandmed, mudeli vastendamine, vorming.</span><span class="sxs-lookup"><span data-stu-id="09c37-133">Import the downloaded configurations to RCS in the following sequence: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="09c37-134">Täitke järgmised sammud iga ER-konfiguratsiooni puhul:</span><span class="sxs-lookup"><span data-stu-id="09c37-134">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="09c37-135">Valige **Vaheta**.</span><span class="sxs-lookup"><span data-stu-id="09c37-135">Select **Exchange.**</span></span>
    2. <span data-ttu-id="09c37-136">Valige **Laadi XML-failist**.</span><span class="sxs-lookup"><span data-stu-id="09c37-136">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="09c37-137">Valige käsk **Sirvi** ja valige nõutav ER-i konfiguratsioon XML-vormingus.</span><span class="sxs-lookup"><span data-stu-id="09c37-137">Select **Browse**, and then select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="09c37-138">Valige nupp **OK.**</span><span class="sxs-lookup"><span data-stu-id="09c37-138">Select **OK.**</span></span>

## <a name="review-the-provided-er-solution"></a><span data-ttu-id="09c37-139">Vaadake läbi esitatud ER-lahendus</span><span class="sxs-lookup"><span data-stu-id="09c37-139">Review the provided ER solution</span></span>

### <a name="review-model-mapping"></a><span data-ttu-id="09c37-140">Mudeli vastendamise läbivaatamine</span><span class="sxs-lookup"><span data-stu-id="09c37-140">Review model mapping</span></span>

1. <span data-ttu-id="09c37-141">Laiendage konfiguratsioonipuus üksuse **Parameetritega kõnede õppimiseks kasutatava mudeli** sisu.</span><span class="sxs-lookup"><span data-stu-id="09c37-141">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="09c37-142">Valige **Vastendamine parameetritega kõnede õppimiseks**.</span><span class="sxs-lookup"><span data-stu-id="09c37-142">Select **Mapping to learn parameterized calls**.</span></span>
3. <span data-ttu-id="09c37-143">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="09c37-143">Select **Designer**.</span></span>
4. <span data-ttu-id="09c37-144">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="09c37-144">Select **Designer**.</span></span>  
   
    <span data-ttu-id="09c37-145">See ER-mudeli vastendus on ette nähtud selleks, et teha järgmist:</span><span class="sxs-lookup"><span data-stu-id="09c37-145">This ER model mapping is designed to do the following:</span></span>

    - <span data-ttu-id="09c37-146">Tooge sisse maksukoodide loetelu (**Maksu** andmeallikas), mis asub tabelis **TaxTable**.</span><span class="sxs-lookup"><span data-stu-id="09c37-146">Fetch the list of tax codes (**Tax** data source) residing in the **TaxTable** table.</span></span>
    - <span data-ttu-id="09c37-147">Tooge esile maksukannete loetelu (**Kannete** andmeallikas), mis asub tabelis **TaxTranse**.</span><span class="sxs-lookup"><span data-stu-id="09c37-147">Fetch the list of tax transactions (**Trans** data source) residing in the **TaxTrans** table:</span></span>
    
        - <span data-ttu-id="09c37-148">Grupeerida sissetoodud kannete loend (**GR** andmeallikas) maksukoodi alusel.</span><span class="sxs-lookup"><span data-stu-id="09c37-148">Group the list of fetched transactions (**Gr** data source) by tax code.</span></span>
        - <span data-ttu-id="09c37-149">Arvutage grupeeritud kanded koondväärtuste järgi maksukoodi kohta järgnevalt.</span><span class="sxs-lookup"><span data-stu-id="09c37-149">Calculate for grouped transactions following aggregated values per tax code:</span></span>

            - <span data-ttu-id="09c37-150">Maksubaasi väärtuste summa.</span><span class="sxs-lookup"><span data-stu-id="09c37-150">Sum of tax base values.</span></span>
            - <span data-ttu-id="09c37-151">Maksuväärtuste summa.</span><span class="sxs-lookup"><span data-stu-id="09c37-151">Sum of tax values.</span></span>
            - <span data-ttu-id="09c37-152">Kohaldatava maksumäära miinimumväärtus.</span><span class="sxs-lookup"><span data-stu-id="09c37-152">Minimum value of applied tax rate.</span></span>

    <span data-ttu-id="09c37-153">Selle konfiguratsiooni mudeli vastendamine rakendab põhiandmete mudelit selle mudeli jaoks loodud ER-vormingute puhul, mida kasutatakse rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="09c37-153">The model mapping in this configuration implements the base data model for any of the ER formats created for this model and executed in Finance and Operations.</span></span> <span data-ttu-id="09c37-154">Selle tulemusena on **Maksu-** ja **Gr-** andmeallikate sisu avatud ER-vormingute, näiteks abstraktsete andmeallikate puhul.</span><span class="sxs-lookup"><span data-stu-id="09c37-154">As a result, the content of the **Tax** and **Gr** data sources is exposed for ER formats such as abstract data sources.</span></span>

    ![Mudeli vastendamise kujundaja lehekülg, kus kuvatakse maksu-ja Gr-andmeallikad](media/er-calculated-field-type-01.png)

5.  <span data-ttu-id="09c37-156">Sulgege leht **Mudelivastenduse koostaja**.</span><span class="sxs-lookup"><span data-stu-id="09c37-156">Close the **Model mapping designer** page.</span></span>
6.  <span data-ttu-id="09c37-157">Sulgege leht **Mudelivastendus**.</span><span class="sxs-lookup"><span data-stu-id="09c37-157">Close the **Model mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="09c37-158">Läbivaatuse vorming</span><span class="sxs-lookup"><span data-stu-id="09c37-158">Review format</span></span>

1. <span data-ttu-id="09c37-159">Laiendage konfiguratsioonipuus üksuse **Parameetritega kõnede õppimiseks kasutatava mudeli** sisu.</span><span class="sxs-lookup"><span data-stu-id="09c37-159">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="09c37-160">Valige **Vorming parameetritega kõnede õppimiseks**.</span><span class="sxs-lookup"><span data-stu-id="09c37-160">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="09c37-161">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="09c37-161">Select **Designer**.</span></span> <span data-ttu-id="09c37-162">See ER-vormingu vastendus on ette nähtud selleks, et teha järgmist.</span><span class="sxs-lookup"><span data-stu-id="09c37-162">This ER format is designed to do the following:</span></span>

    - <span data-ttu-id="09c37-163">Vastavusseviimiseks väljavõtte loomine.</span><span class="sxs-lookup"><span data-stu-id="09c37-163">Generate a tax statement in XML format.</span></span>
    - <span data-ttu-id="09c37-164">Esitada maksuaruandes järgmised maksustamistasemed: regulaarne, vähendatud ja pole.</span><span class="sxs-lookup"><span data-stu-id="09c37-164">Present the following levels of taxation in the tax statement: regular, reduced, and none.</span></span>
    - <span data-ttu-id="09c37-165">Esitada igal maksustamistasandil mitu üksikasja, millel on igal tasandil erinev arv üksikasju.</span><span class="sxs-lookup"><span data-stu-id="09c37-165">Present multiple details at each taxation level, having a different number of details in each level.</span></span>

    ![Vormingu koostaja leht](media/er-calculated-field-type-02.png)

4. <span data-ttu-id="09c37-167">Valige **Vastendamine**.</span><span class="sxs-lookup"><span data-stu-id="09c37-167">Select **Mapping**.</span></span>
5. <span data-ttu-id="09c37-168">Laiendage üksusi **Mudel**, **Andmed** ja **Kokkuvõte**.</span><span class="sxs-lookup"><span data-stu-id="09c37-168">Expand the **Model**, **Data,** and **Summary** items.</span></span> 

    <span data-ttu-id="09c37-169">Arvutatud väli **Model.Data.Summary.Level** sisaldab avaldist, mis tagastab maksutaseme koodi (**Regulaarne**, **Vähendatud**, **Pole** või **Muu**) tekstiväärtusena mis tahes maksukoodi jaoks, mida saab **Model.Data.Summary** mudelist tuua andmeallika käitusajal.</span><span class="sxs-lookup"><span data-stu-id="09c37-169">The calculated field **Model.Data.Summary.Level** contains the expression that returns the code of the taxation level (**Regular**, **Reduced**, **None,** or **Other**) as a text value for any tax code that can be retrieved from the **Model.Data.Summary** data source at run time.</span></span>

    ![Vormingu kujundaja leht, kus kuvatakse andmemudeli Mudeli üksikasjad parameetriliste kõnede õppimiseks](media/er-calculated-field-type-03.png)

6. <span data-ttu-id="09c37-171">Laiendage üksust **Model**.**Data2**.</span><span class="sxs-lookup"><span data-stu-id="09c37-171">Expand the **Model**.**Data2** item.</span></span>
7. <span data-ttu-id="09c37-172">Laiendage üksust **Model**.**Data2.Summary2**.</span><span class="sxs-lookup"><span data-stu-id="09c37-172">Expand the **Model**.**Data2.Summary2** item.</span></span>
   
    <span data-ttu-id="09c37-173">**Model**.**Data2. Summary2** andmeallikas on konfigureeritud grupeerima **Model.Data.Summary** andmeallika kande üksikasjad maksustamise taseme alusel (tagastab **Model.Data.Summary.Level** arvutatud väli) ja arvutama kokkuvõtted.</span><span class="sxs-lookup"><span data-stu-id="09c37-173">The **Model**.**Data2.Summary2** data source is configured to group the **Model.Data.Summary** data source transaction details by taxation level (returned by the **Model.Data.Summary.Level** calculated field) and compute the aggregations.</span></span>

    ![Vormingu kujundaja leht, kus kuvatakse andmeallika Model.Data2.Summary üksikasjad](media/er-calculated-field-type-04.png)

8. <span data-ttu-id="09c37-175">Vaadake üle arvutatud väljad **Model**.**Data2. Level1**, **Model**.**Data2. Level2** ja **Model**.**Data2. level3.**</span><span class="sxs-lookup"><span data-stu-id="09c37-175">Review the calculated fields **Model**.**Data2.Level1**, **Model**.**Data2.Level2**, and **Model**.**Data2.Level3.**</span></span> <span data-ttu-id="09c37-176">Neid arvutatud välju kasutatakse **Model**.**Data2. Summary2** kirjeteloendi filtreerimiseks ja ainult konkreetse maksustamistaset kajastavate kirjete tagastamiseks.</span><span class="sxs-lookup"><span data-stu-id="09c37-176">These calculated fields are used to filter the **Model**.**Data2.Summary2** records list and return only records that represent a particular taxation level.</span></span>
9. <span data-ttu-id="09c37-177">Sulgege **Vormingu koostaja** leht.</span><span class="sxs-lookup"><span data-stu-id="09c37-177">Close the **Format designer** page.</span></span>

## <a name="create-a-derived-format"></a><span data-ttu-id="09c37-178">Tuletatud vormingu loomine</span><span class="sxs-lookup"><span data-stu-id="09c37-178">Create a derived format</span></span>
<span data-ttu-id="09c37-179">Esitatud vormingut saate parandada, kui lisate ühe arvutatud välja, et filtreerida nõutavat maksustamistaset, mitte kasutada olemasolevaid kolme välja: **Model**.**Data2.Level1**, **Model**.**Data2.Level2** ja **Mudel**.**Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="09c37-179">You can improve the provided format by adding one calculated field to filter the required taxation level instead of using the existing three fields: **Model**.**Data2.Level1**, **Model**.**Data2.Level2,** and **Model**.**Data2.Level3**.</span></span> <span data-ttu-id="09c37-180">Nõutavat maksustamistaset saab määrata asukohas, kus seda uut arvutatud välja nimetatakse.</span><span class="sxs-lookup"><span data-stu-id="09c37-180">The required taxation level can be specified in the location where this new calculated field will be called.</span></span>

1. <span data-ttu-id="09c37-181">Laiendage konfiguratsioonipuus üksuse **Parameetritega kõnede õppimiseks kasutatava mudeli** sisu.</span><span class="sxs-lookup"><span data-stu-id="09c37-181">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="09c37-182">Valige **Vorming parameetritega kõnede õppimiseks**.</span><span class="sxs-lookup"><span data-stu-id="09c37-182">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="09c37-183">Valige **Konfiguratsiooni loomine**.</span><span class="sxs-lookup"><span data-stu-id="09c37-183">Select **Create configuration**.</span></span>
4. <span data-ttu-id="09c37-184">Valige **Tuletage nimest: vormindage parameetritega kõnede õppimiseks, Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="09c37-184">Select **Derive from Name: Format to learn parameterized calls, Microsoft**.</span></span>
5. <span data-ttu-id="09c37-185">Sisestage väljale **Nimi** suvand **Vorming parameetriga (kohandatud) kõnede õppimiseks**.</span><span class="sxs-lookup"><span data-stu-id="09c37-185">In the **Name** field, enter **Format to learn parameterized calls (custom)**.</span></span>
6. <span data-ttu-id="09c37-186">Valige **Konfiguratsiooni loomine.**</span><span class="sxs-lookup"><span data-stu-id="09c37-186">Select **Create configuration.**</span></span>

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a><span data-ttu-id="09c37-187">Parameetrite arvutatud välja konfigureerimine, mis tagastab kirjete loendi</span><span class="sxs-lookup"><span data-stu-id="09c37-187">Configure a parameterized calculated field that returns a list of records</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="09c37-188">Uue arvutatud välja lisamise alustamine</span><span class="sxs-lookup"><span data-stu-id="09c37-188">Start adding a new calculated field</span></span>

1. <span data-ttu-id="09c37-189">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="09c37-189">Select **Designer**.</span></span>
2. <span data-ttu-id="09c37-190">Kõigi vorminguüksuste laiendamiseks valige **Laienda/ahenda**.</span><span class="sxs-lookup"><span data-stu-id="09c37-190">Select **Expand/collapse** to expand all format items.</span></span>
3. <span data-ttu-id="09c37-191">Valige **Vastendamine**.</span><span class="sxs-lookup"><span data-stu-id="09c37-191">Select **Mapping**.</span></span>
4. <span data-ttu-id="09c37-192">Laiendage üksust **Mudel**.</span><span class="sxs-lookup"><span data-stu-id="09c37-192">Expand the **Model** item.</span></span>
5. <span data-ttu-id="09c37-193">Valige üksus **Model.Data2**.</span><span class="sxs-lookup"><span data-stu-id="09c37-193">Select the **Model.Data2** item.</span></span>
6. <span data-ttu-id="09c37-194">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="09c37-194">Select **Add**.</span></span>
7. <span data-ttu-id="09c37-195">Valige **Funktsioonid\\Arvutatud väli**.</span><span class="sxs-lookup"><span data-stu-id="09c37-195">Select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="09c37-196">Väljale **Nimi** sisestage **Tasemed**.</span><span class="sxs-lookup"><span data-stu-id="09c37-196">In the **Name** field, enter **Levels**.</span></span>
9. <span data-ttu-id="09c37-197">Valige **Valemi redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="09c37-197">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="09c37-198">Arvutatud välja lisamise parameetri määratlemine</span><span class="sxs-lookup"><span data-stu-id="09c37-198">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="09c37-199">Valige **Parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="09c37-199">Select **Parameters**.</span></span>
2. <span data-ttu-id="09c37-200">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="09c37-200">Select **New**.</span></span>
3. <span data-ttu-id="09c37-201">Väljale **Nimi** sisestage väärtus **Maksustamise tase**.</span><span class="sxs-lookup"><span data-stu-id="09c37-201">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="09c37-202">Valige väljalt **Tüüp** suvand **String**.</span><span class="sxs-lookup"><span data-stu-id="09c37-202">In the **Type** field, select **String**.</span></span>

    <span data-ttu-id="09c37-203">Parameetri argumendi tüübi määramiseks saab kasutada ainult primitiivseid andmetüüpe.</span><span class="sxs-lookup"><span data-stu-id="09c37-203">Only primitive data types can be used to specify the type of the parameter’s argument.</span></span> <span data-ttu-id="09c37-204">Seetõttu ei saa tüüpe **Kirjeloend**, **Kirje** ja **Loetelu** sel eesmärgil kasutada.</span><span class="sxs-lookup"><span data-stu-id="09c37-204">Therefore, **Record list**, **Record**, and **Enum** types cannot be used for this purpose.</span></span>

    <span data-ttu-id="09c37-205">Ühe arvutatud välja jaoks määratud maksimaalne parameetrite arv on 8.</span><span class="sxs-lookup"><span data-stu-id="09c37-205">The maximum number of parameters that can be specified for a single calculated field is 8.</span></span>

    ![Parameetrite andmeallika loend](media/er-calculated-field-type-05.png)

5. <span data-ttu-id="09c37-207">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="09c37-207">Select **OK**.</span></span>

<span data-ttu-id="09c37-208">Selle parameetri lisamisega määratlete tingimuse, mis peab olema kasutusel selle arvutatud välja nimetamiseks.</span><span class="sxs-lookup"><span data-stu-id="09c37-208">By adding this parameter, you specify the condition that must be in place to call this calculated field.</span></span> <span data-ttu-id="09c37-209">Kui nimetate seda arvutatud välja, peate määrama parameetri **Maksustamistase** argumendi väärtusena vorminguga **String**.</span><span class="sxs-lookup"><span data-stu-id="09c37-209">When you call this calculated field, you need to specify the argument of the **Taxation Level** parameter as a value with **String** format.</span></span>

   <span data-ttu-id="09c37-210">Veenduge, et määratlete parameetrid ainult nende arvutatud väljade jaoks, mis asuvad konteineris ( **kas kirje loend**, **kirje** või **konteiner**).</span><span class="sxs-lookup"><span data-stu-id="09c37-210">Make sure that you define parameters only for those calculated fields that reside in a container (either **Record list**, **Record**, or **Container**).</span></span>

   <span data-ttu-id="09c37-211">Konfigureeritud parameeter on saadaval selle arvutatud välja andmeallikate loendis.</span><span class="sxs-lookup"><span data-stu-id="09c37-211">The configured parameter is available in the list of data sources for this calculated field.</span></span> <span data-ttu-id="09c37-212">Parameetri lisamiseks konfigureeritud avaldisse Saate klõpsata käsku **lisa andmeallikas.**</span><span class="sxs-lookup"><span data-stu-id="09c37-212">You can add the parameter to the configured expression by selecting **Add data source**.</span></span>

   ![Andmeallika väljad](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="09c37-214">Arvutatud välja lisamise väljendi määratlemine</span><span class="sxs-lookup"><span data-stu-id="09c37-214">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="09c37-215">Sisestage väljale **Valem**:</span><span class="sxs-lookup"><span data-stu-id="09c37-215">In the **Formula** field, enter:</span></span> 

    <span data-ttu-id="09c37-216">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span><span class="sxs-lookup"><span data-stu-id="09c37-216">**WHERE(\@.Summary2, \@.Summary2.grouped.Level =**</span></span>
    
2. <span data-ttu-id="09c37-217">Valige andmeallikate loendis **Maksustamistaseme** parameeter.</span><span class="sxs-lookup"><span data-stu-id="09c37-217">Select the **Taxation Level** parameter in the list of data sources.</span></span>
3. <span data-ttu-id="09c37-218">Valige **Andmeallika lisamine**.</span><span class="sxs-lookup"><span data-stu-id="09c37-218">Select **Add data source**.</span></span>
4. <span data-ttu-id="09c37-219">Väljal **Valem** viimistlege avaldis järgmiselt:</span><span class="sxs-lookup"><span data-stu-id="09c37-219">In the **Formula** field, finalize the expression as:</span></span>  

    <span data-ttu-id="09c37-220">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span><span class="sxs-lookup"><span data-stu-id="09c37-220">**WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Taxation Level')**</span></span>

5. <span data-ttu-id="09c37-221">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="09c37-221">Select **Save**.</span></span>

    ![Andmeallika välja teave](media/er-calculated-field-type-07.png)

6. <span data-ttu-id="09c37-223">Sulgege **Valemikoostaja** leht.</span><span class="sxs-lookup"><span data-stu-id="09c37-223">Close the **Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="09c37-224">Uue arvutatud välja lisamise alustamine</span><span class="sxs-lookup"><span data-stu-id="09c37-224">Finish adding a new calculated field</span></span>

- <span data-ttu-id="09c37-225">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="09c37-225">Select **OK**.</span></span>

<span data-ttu-id="09c37-226">Lehel **Vormingu koostaja** nõuab konfigureeritud parameetritega arvutatud väli **Tasemed** argumenti **String**.</span><span class="sxs-lookup"><span data-stu-id="09c37-226">On the **Format designer** page, the configured parameterized calculated field **Levels** requires a **String** argument.</span></span>

![Arvutatud välja tasemete laiendatud loend](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements"></a><span data-ttu-id="09c37-228">Kasutage siduva vormingu elementide jaoks konfigureeritud arvutatud välja.</span><span class="sxs-lookup"><span data-stu-id="09c37-228">Use the configured calculated field for binding format elements</span></span>

1. <span data-ttu-id="09c37-229">Valige **Model.Data2.Levels**, et valida konfigureeritud arvutatud väli.</span><span class="sxs-lookup"><span data-stu-id="09c37-229">Select **Model.Data2.Levels** to select the configured calculated field.</span></span>
2. <span data-ttu-id="09c37-230">Valige **Statement.Taxation.Regular** vormingu element.</span><span class="sxs-lookup"><span data-stu-id="09c37-230">Select the **Statement.Taxation.Regular** format element.</span></span>
3. <span data-ttu-id="09c37-231">Valige **Seo**.</span><span class="sxs-lookup"><span data-stu-id="09c37-231">Select **Bind**.</span></span>
4. <span data-ttu-id="09c37-232">Valige **Jah**, et kinnitada praegu kasutatava andmeallika **Tase1** asendamist uue andmeallikaga **Tasemed** kõigis valitud vorminguelemendi pesastatud vorminguelementides.</span><span class="sxs-lookup"><span data-stu-id="09c37-232">Select **Yes** to confirm the replacement of the currently used data source, **Level1**, by the new data source, **Levels**, in all nested format elements of the selected format element.</span></span>

    <span data-ttu-id="09c37-233">Rakendatud sidumine on loodud parameetrina arvutatud välja kutsena.</span><span class="sxs-lookup"><span data-stu-id="09c37-233">Applied binding has been built as a call of the parameterized calculated field.</span></span> <span data-ttu-id="09c37-234">Vaikimisi kasutatakse seotud vormingu elemendi nime parameetrina arvutatud välja argumendina järgmistel tingimustel:</span><span class="sxs-lookup"><span data-stu-id="09c37-234">By default, the name of the bound format element is used as an argument for parameterized calculated field under the following conditions:</span></span>

      - <span data-ttu-id="09c37-235">Arvutatud väli on konfigureeritud kasutama ühte parameetrit.</span><span class="sxs-lookup"><span data-stu-id="09c37-235">The calculated field is configured to use a single parameter.</span></span>
      - <span data-ttu-id="09c37-236">Selle parameetri andmetüüp määratletakse **Stringina**.</span><span class="sxs-lookup"><span data-stu-id="09c37-236">The data type of this parameter is defined as **String**.</span></span>

    <span data-ttu-id="09c37-237">Kui seotud vormingu elemendi nimi on tühi, kasutatakse selle elemendi andmeallika nime rakendatud sidumises.</span><span class="sxs-lookup"><span data-stu-id="09c37-237">When the name of the bound format element is blank, the data source name of this element is used in applied binding.</span></span>

5. <span data-ttu-id="09c37-238">Valige **Statement.Taxation.Reduced** vormingu element.</span><span class="sxs-lookup"><span data-stu-id="09c37-238">Select the **Statement.Taxation.Reduced** format element.</span></span>
6. <span data-ttu-id="09c37-239">Valige **Seo**.</span><span class="sxs-lookup"><span data-stu-id="09c37-239">Select **Bind**.</span></span>
7. <span data-ttu-id="09c37-240">Valige **Jah**, et kinnitada praegu kasutatava andmeallika **Tase2** asendamist uue andmeallikaga **Tasemed** kõigis valitud vorminguelemendi pesastatud vorminguelementides.</span><span class="sxs-lookup"><span data-stu-id="09c37-240">Select **Yes** to confirm the replacement of the currently used data source, **Level2**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>
8. <span data-ttu-id="09c37-241">Valige **Statement.Taxation.None** vormingu element.</span><span class="sxs-lookup"><span data-stu-id="09c37-241">Select the **Statement.Taxation.None** format element.</span></span>
9. <span data-ttu-id="09c37-242">Valige **Seo**.</span><span class="sxs-lookup"><span data-stu-id="09c37-242">Select **Bind**.</span></span>
10. <span data-ttu-id="09c37-243">Valige **Jah**, et kinnitada praegu kasutatava andmeallika **Tase3** asendamist uue andmeallikaga **Tasemed** kõigis valitud vorminguelemendi pesastatud vorminguelementides.</span><span class="sxs-lookup"><span data-stu-id="09c37-243">Select **Yes** to confirm the replacement of the currently used data source, **Level3**, by the new data source, **Levels**, in all nested format elements under the selected format element.</span></span>

   <span data-ttu-id="09c37-244">Kui määrate argumendi parameetri arvutatud välja kohta XML-elemendi jaoks, mis tähistab maksustamistaset (nt **Model.Data2.Levels („Vähendatud”)** teksti väärtusena), ei pea te sama tegema pesastatud XML-atribuutide puhul – nende sidumised pärivad automaatselt ematasemel (**Model.Data2.Levels.aggregated.Base**, mitte **Model.Data2.Levels („Vähendatud”).aggregated.Base**).</span><span class="sxs-lookup"><span data-stu-id="09c37-244">When you specify the argument of the parameterized calculated field for the XML element representing taxation level (for example, **Model.Data2.Levels("Reduced")** as a text value), you don’t need to do the same for nested XML attributes—their bindings will automatically inherit the value of the argument defined on the parent level (**Model.Data2.Levels.aggregated.Base**, not **Model.Data2.Levels("Reduced").aggregated.Base**).</span></span>

<span data-ttu-id="09c37-245">Parameetritega arvutatud välja korduvaid kõnesid ei toetata.</span><span class="sxs-lookup"><span data-stu-id="09c37-245">Recurrent calls of any parameterized calculated field are not supported.</span></span>

<span data-ttu-id="09c37-246">Saate valida **Redigeeri valemit** ja muuta valitud sidumise parameetritega arvutatud välja vaikimisi rakendatud argumenti.</span><span class="sxs-lookup"><span data-stu-id="09c37-246">You can select **Edit formula**, and change the applied-by-default argument of the parameterized calculated field in the selected binding.</span></span> <span data-ttu-id="09c37-247">Kui see argument on puudu, võib see põhjustada tõrkeid käitusajal — kasutajat teavitatakse sellisest olukorrast, kui on kehtiv vorming on kontrollitud.</span><span class="sxs-lookup"><span data-stu-id="09c37-247">If this argument is missing, it can cause errors at run time — users are informed about such a situation when the current format is validated.</span></span>

![Kinnitamise hoiatuse teatis](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a><span data-ttu-id="09c37-249">Parameetritega arvutatud välja konfigureerimine kirje tagastamiseks</span><span class="sxs-lookup"><span data-stu-id="09c37-249">Configure a parameterized calculated field to return a record</span></span>
<span data-ttu-id="09c37-250">Kui parameetritega arvutatud väli tagastab kirje, peate elementide vormindamiseks toetama selle kirje üksikute väljade sidumist.</span><span class="sxs-lookup"><span data-stu-id="09c37-250">When a parameterized calculated field returns a record, you need to support binding of individual fields of this record to format elements.</span></span> <span data-ttu-id="09c37-251">Sellisel juhul puudub ülataseme sidumine, mis sisaldab parameetritega arvutatud välja kutsumise argumendi väärtust – see väärtus tuleb määratleda ühe kirje välja sidumisel.</span><span class="sxs-lookup"><span data-stu-id="09c37-251">In such cases there will be no parent binding that contains the value of an argument to call a parameterized calculated field — this value must be defined in the binding of a single record’s field.</span></span>

### <a name="start-adding-a-new-calculated-field"></a><span data-ttu-id="09c37-252">Uue arvutatud välja lisamise alustamine</span><span class="sxs-lookup"><span data-stu-id="09c37-252">Start adding a new calculated field</span></span>

1. <span data-ttu-id="09c37-253">Valige üksus **Model.Data2**.</span><span class="sxs-lookup"><span data-stu-id="09c37-253">Select the **Model.Data2** item.</span></span>
2. <span data-ttu-id="09c37-254">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="09c37-254">Select **Add**.</span></span>
3. <span data-ttu-id="09c37-255">Valige **Funktsioonid\\Arvutatud väli**.</span><span class="sxs-lookup"><span data-stu-id="09c37-255">Select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="09c37-256">Sisestage väljale **Nimi** suvand **LevelRecord**.</span><span class="sxs-lookup"><span data-stu-id="09c37-256">In the **Name** field, enter **LevelRecord**.</span></span>
5. <span data-ttu-id="09c37-257">Valige **Valemi redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="09c37-257">Select **Edit formula**.</span></span>

### <a name="define-a-parameter-for-adding-a-calculated-field"></a><span data-ttu-id="09c37-258">Arvutatud välja lisamise parameetri määratlemine</span><span class="sxs-lookup"><span data-stu-id="09c37-258">Define a parameter for adding a calculated field</span></span>

1. <span data-ttu-id="09c37-259">Valige **Parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="09c37-259">Select **Parameters**.</span></span>
2. <span data-ttu-id="09c37-260">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="09c37-260">Select **New**.</span></span>
3. <span data-ttu-id="09c37-261">Väljale **Nimi** sisestage väärtus **Maksustamise tase**.</span><span class="sxs-lookup"><span data-stu-id="09c37-261">In the **Name** field, enter **Taxation Level**.</span></span>
4. <span data-ttu-id="09c37-262">Valige väljalt **Tüüp** suvand **String**.</span><span class="sxs-lookup"><span data-stu-id="09c37-262">In the **Type** field, select **String**.</span></span>
5. <span data-ttu-id="09c37-263">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="09c37-263">Select **OK**.</span></span>

### <a name="define-an-expression-for-adding-a-calculated-field"></a><span data-ttu-id="09c37-264">Arvutatud välja lisamise väljendi määratlemine</span><span class="sxs-lookup"><span data-stu-id="09c37-264">Define an expression for adding a calculated field</span></span>

1. <span data-ttu-id="09c37-265">Sisestage väljale **Valem** järgmine tekst.</span><span class="sxs-lookup"><span data-stu-id="09c37-265">In the **Formula** field, enter the following:</span></span>  
    
    <span data-ttu-id="09c37-266">**FIRSTORNULL(\@.Levels(**</span><span class="sxs-lookup"><span data-stu-id="09c37-266">**FIRSTORNULL(\@.Levels(**</span></span>

2. <span data-ttu-id="09c37-267">Valige **Maksustamistaseme** parameeter.</span><span class="sxs-lookup"><span data-stu-id="09c37-267">Select the **Taxation Level** parameter.</span></span>
3. <span data-ttu-id="09c37-268">Valige **Andmeallika lisamine**.</span><span class="sxs-lookup"><span data-stu-id="09c37-268">Select **Add data source**.</span></span>
4. <span data-ttu-id="09c37-269">Väljale **Valem** lisage **„Maksustamistase”))**, mis on sisestatud juhises 1, et lõpetada avaldis:</span><span class="sxs-lookup"><span data-stu-id="09c37-269">In the **Formula** field, append **'Taxation Level'))** to what you entered in Step 1 to finalize the expression to:</span></span>  
    
    <span data-ttu-id="09c37-270">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span><span class="sxs-lookup"><span data-stu-id="09c37-270">**FIRSTORNULL(\@.Levels('Taxation Level'))**</span></span>

5. <span data-ttu-id="09c37-271">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="09c37-271">Select **Save**.</span></span>
6. <span data-ttu-id="09c37-272">Sulgege **Valemikoostaja** leht.</span><span class="sxs-lookup"><span data-stu-id="09c37-272">Close **the Formula designer** page.</span></span>

### <a name="finish-adding-a-new-calculated-field"></a><span data-ttu-id="09c37-273">Uue arvutatud välja lisamise alustamine</span><span class="sxs-lookup"><span data-stu-id="09c37-273">Finish adding a new calculated field</span></span>

-   <span data-ttu-id="09c37-274">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="09c37-274">Select **OK**.</span></span>

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a><span data-ttu-id="09c37-275">Kasutage siduva vormingu elementide jaoks konfigureeritud arvutatud välja.</span><span class="sxs-lookup"><span data-stu-id="09c37-275">Use the configured calculated field to bind format elements</span></span>

1. <span data-ttu-id="09c37-276">Laiendage välja **Model.Data2.LevelRecord**, et valida konfigureeritud arvutatud väli.</span><span class="sxs-lookup"><span data-stu-id="09c37-276">Expand **Model.Data2.LevelRecord** to select the configured calculated field.</span></span>
2. <span data-ttu-id="09c37-277">Laiendage välja **Model.Data2.aggregated**, et valida konfigureeritud arvutatud välja ümbris.</span><span class="sxs-lookup"><span data-stu-id="09c37-277">Expand the **Model.Data2.LevelRecord.aggregated** container of the configured calculated field.</span></span>
3. <span data-ttu-id="09c37-278">Valige **Model. Data2. LevelRecord.aggregated.Base** väli.</span><span class="sxs-lookup"><span data-stu-id="09c37-278">Select the **Model.Data2.LevelRecord.aggregated.Base** field.</span></span>
4. <span data-ttu-id="09c37-279">Valige **Statement.Taxation.None** vormingu element.</span><span class="sxs-lookup"><span data-stu-id="09c37-279">Select the **Statement.Taxation.None** format element.</span></span>
5. <span data-ttu-id="09c37-280">Valige **Tühista sidumine**.</span><span class="sxs-lookup"><span data-stu-id="09c37-280">Select **Unbind**.</span></span>
6. <span data-ttu-id="09c37-281">Valige **Statement.Taxation.None.Base** vormingu element.</span><span class="sxs-lookup"><span data-stu-id="09c37-281">Select the **Statement.Taxation.None.Base** format element.</span></span>
7. <span data-ttu-id="09c37-282">Valige **Seo**.</span><span class="sxs-lookup"><span data-stu-id="09c37-282">Select **Bind**.</span></span>
8. <span data-ttu-id="09c37-283">Valige **Valemi redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="09c37-283">Select **Edit formula**.</span></span>
9. <span data-ttu-id="09c37-284">Muutke avaldiseks **Model.Data2.LevelRecord („Pole”).aggregated.Base**.</span><span class="sxs-lookup"><span data-stu-id="09c37-284">Change the expression to **Model.Data2.LevelRecord("None").aggregated.Base**.</span></span>

![Värskendatud avaldis](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a><span data-ttu-id="09c37-286">Eemaldage arvutatud väljad, mida ei kasutata</span><span class="sxs-lookup"><span data-stu-id="09c37-286">Remove calculated fields that are not used</span></span>

1. <span data-ttu-id="09c37-287">Valige **Model.Data2.Level1**.</span><span class="sxs-lookup"><span data-stu-id="09c37-287">Select **Model.Data2.Level1**.</span></span>
2. <span data-ttu-id="09c37-288">Valige **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="09c37-288">Select **Delete**.</span></span>
3. <span data-ttu-id="09c37-289">Valige **Model.Data2.Level2**.</span><span class="sxs-lookup"><span data-stu-id="09c37-289">Select **Model.Data2.Level2**.</span></span>
4. <span data-ttu-id="09c37-290">Valige **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="09c37-290">Select **Delete**.</span></span>
5. <span data-ttu-id="09c37-291">Valige **Model.Data2.Level3**.</span><span class="sxs-lookup"><span data-stu-id="09c37-291">Select **Model.Data2.Level3**.</span></span>
6. <span data-ttu-id="09c37-292">Valige **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="09c37-292">Select **Delete**.</span></span>
7. <span data-ttu-id="09c37-293">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="09c37-293">Select **Save**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="09c37-294">Kasutasite uuesti sama arvutatud välja **Model.Data2.Levels** mitu korda vormingu sidumistes.</span><span class="sxs-lookup"><span data-stu-id="09c37-294">You reused the same calculated field **Model.Data2.Levels** several times in format bindings.</span></span> <span data-ttu-id="09c37-295">Mitme sarnase välja asemel on palju lihtsam kasutada ja hallata üksikut arvutatud välja.</span><span class="sxs-lookup"><span data-stu-id="09c37-295">It is much easier to use and maintain a single calculated field instead of doing this for multiple similar fields.</span></span>

8. <span data-ttu-id="09c37-296">Sulgege **Vormingu koostaja** leht.</span><span class="sxs-lookup"><span data-stu-id="09c37-296">Close the **Format designer** page.</span></span>

## <a name="complete-adjusted-version-of-a-derived-format"></a><span data-ttu-id="09c37-297">Tuletatud vormingu kohandatud versiooni lõpetamine</span><span class="sxs-lookup"><span data-stu-id="09c37-297">Complete adjusted version of a derived format</span></span>

1. <span data-ttu-id="09c37-298">Vahekaardil **Versioonid** valige **Muuda olekut**.</span><span class="sxs-lookup"><span data-stu-id="09c37-298">In the **Versions** FastTab, select **Change status**.</span></span>
2. <span data-ttu-id="09c37-299">Valige **Lõpeta**.</span><span class="sxs-lookup"><span data-stu-id="09c37-299">Select **Complete**.</span></span>

## <a name="export-completed-version-of-a-derived-format"></a><span data-ttu-id="09c37-300">Tuletatud vormingu lõpuleviidud versiooni eksportimine</span><span class="sxs-lookup"><span data-stu-id="09c37-300">Export completed version of a derived format</span></span>

1. <span data-ttu-id="09c37-301">Valige konfiguratsioonipuus  **Vorminda parameetritega kõnede õppimiseks (kohandatud)**.</span><span class="sxs-lookup"><span data-stu-id="09c37-301">Select **Format to learn parameterized calls (custom)** format in the configurations tree.</span></span>
2. <span data-ttu-id="09c37-302">Vahekaardil **Versioonid** valige lõpule viidud versioon 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="09c37-302">In the **Versions** FastTab, select the completed version 1.1.1.</span></span>
3. <span data-ttu-id="09c37-303">Valige **Exchange**.</span><span class="sxs-lookup"><span data-stu-id="09c37-303">Select **Exchange**.</span></span>
4. <span data-ttu-id="09c37-304">Valige **Ekspordi XML-failina**.</span><span class="sxs-lookup"><span data-stu-id="09c37-304">Select **Export as XML file**.</span></span>
5. <span data-ttu-id="09c37-305">Salvestage allalaaditud konfiguratsioon kohapeal, XML-vormingus.</span><span class="sxs-lookup"><span data-stu-id="09c37-305">Store the downloaded configuration locally, in XML format.</span></span>

## <a name="test-er-formats"></a><span data-ttu-id="09c37-306">Katsetage ER-vorminguid</span><span class="sxs-lookup"><span data-stu-id="09c37-306">Test ER formats</span></span> 
<span data-ttu-id="09c37-307">Saate käivitada algsed ja täiustatud ER-vormingud veendumaks, et konfigureeritud parameetritega arvutatud väljad töötavad õigesti.</span><span class="sxs-lookup"><span data-stu-id="09c37-307">You can run the initial and improved ER formats to make sure that configured parameterized calculated fields work properly.</span></span>

### <a name="import-er-configurations"></a><span data-ttu-id="09c37-308">Elektroonilise aruandluse konfiguratsioonide importimine</span><span class="sxs-lookup"><span data-stu-id="09c37-308">Import ER configurations</span></span>
<span data-ttu-id="09c37-309">Läbivaadatud konfiguratsioone saate RCS-ist importida tüübi **RCS** ER-hoidla abil.</span><span class="sxs-lookup"><span data-stu-id="09c37-309">You can import reviewed configurations from RCS by using the ER repository of the **RCS** type.</span></span> <span data-ttu-id="09c37-310">Kui te juba läbisite teemas toodud juhised [Elektroonilise aruandluse (ER) konfiguratsioonide importimine teenusest Regulatory Configuration Services (RCS)](rcs-download-configurations.md), kasutage konfigureeritud ER-hoidlat, et importida selles teemas varem arutatud konfiguratsioonid oma keskkonda.</span><span class="sxs-lookup"><span data-stu-id="09c37-310">If you already went through the steps in the topic, [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](rcs-download-configurations.md), use the configured ER repository to import configurations discussed earlier in this topic to your environment.</span></span> <span data-ttu-id="09c37-311">Muul juhul toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="09c37-311">Otherwise, follow these steps:</span></span>

1. <span data-ttu-id="09c37-312">Valige ettevõte **DEMF** ja valige vaikearmatuurlaual **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="09c37-312">Select the **DEMF** company and on the default dashboard, select **Electronic reporting**.</span></span>
2. <span data-ttu-id="09c37-313">Valige **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="09c37-313">Select **Reporting configurations**.</span></span>
3. <span data-ttu-id="09c37-314">Importige konfiguratsioonid Microsofti allalaadimiskeskusest järgmises järjestuses: andmemudel, mudelivastendus, vorming.</span><span class="sxs-lookup"><span data-stu-id="09c37-314">Import the configurations from Microsoft Download Center in the following sequence: data model, model mapping, format.</span></span> <span data-ttu-id="09c37-315">Täitke järgmised sammud iga ER-konfiguratsiooni puhul:</span><span class="sxs-lookup"><span data-stu-id="09c37-315">Complete the following steps for each ER configuration:</span></span>

    1. <span data-ttu-id="09c37-316">Valige **Vaheta**.</span><span class="sxs-lookup"><span data-stu-id="09c37-316">Select **Exchange.**</span></span>
    2. <span data-ttu-id="09c37-317">Valige **Laadi XML-failist**.</span><span class="sxs-lookup"><span data-stu-id="09c37-317">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="09c37-318">Valige käsk **Sirvi**, et valida nõutav ER-i konfiguratsioon XML-vormingus.</span><span class="sxs-lookup"><span data-stu-id="09c37-318">Select **Browse** to select the required ER configuration in XML format.</span></span>
    4. <span data-ttu-id="09c37-319">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="09c37-319">Select **OK**.</span></span>

4. <span data-ttu-id="09c37-320">Importige eksporditud RCS-i lõpule viidud versioon 1.1.1 vormingust **Vorminda parameetritega kõnede õppimiseks (kohandatud)**:</span><span class="sxs-lookup"><span data-stu-id="09c37-320">Import the exported from RCS completed version 1.1.1 of the **Format to learn parameterized calls (custom)** format:</span></span>

    1. <span data-ttu-id="09c37-321">Valige **Vaheta**.</span><span class="sxs-lookup"><span data-stu-id="09c37-321">Select **Exchange.**</span></span>
    2. <span data-ttu-id="09c37-322">Valige **Laadi XML-failist**.</span><span class="sxs-lookup"><span data-stu-id="09c37-322">Select **Load from XML file**.</span></span>
    3. <span data-ttu-id="09c37-323">Valige **Sirvi**, et valida kohalikult salvestatud **Vorminda parameetritega kõnede õppimiseks (kohandatud)** fail XML-vormingus.</span><span class="sxs-lookup"><span data-stu-id="09c37-323">Select **Browse** to select the locally stored **Format to learn parameterized calls (custom)** file in XML format.</span></span>
    4. <span data-ttu-id="09c37-324">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="09c37-324">Select **OK**.</span></span>

### <a name="run-er-formats"></a><span data-ttu-id="09c37-325">ER-vormingute käivitamine</span><span class="sxs-lookup"><span data-stu-id="09c37-325">Run ER formats</span></span>

1. <span data-ttu-id="09c37-326">Laiendage konfiguratsioonipuus üksuse **Parameetritega kõnede õppimiseks kasutatava mudeli** sisu.</span><span class="sxs-lookup"><span data-stu-id="09c37-326">In the configuration tree, expand the content of the **Model to learn parameterized calls** item.</span></span>
2. <span data-ttu-id="09c37-327">Valige **Vorming parameetritega kõnede õppimiseks**.</span><span class="sxs-lookup"><span data-stu-id="09c37-327">Select **Format to learn parameterized calls**.</span></span>
3. <span data-ttu-id="09c37-328">Valige kõige ülemisel ribal **Käivita**.</span><span class="sxs-lookup"><span data-stu-id="09c37-328">Select **Run** on the top-most ribbon.</span></span>
4. <span data-ttu-id="09c37-329">Salvestage kohapeal loodud väljund.</span><span class="sxs-lookup"><span data-stu-id="09c37-329">Save the locally generated output.</span></span>
5. <span data-ttu-id="09c37-330">Valige üksus **Vorminda parameetritega kõnede õppimiseks (kohandatud)**.</span><span class="sxs-lookup"><span data-stu-id="09c37-330">Select the **Format to learn parameterized calls (custom)** item.</span></span>
6. <span data-ttu-id="09c37-331">Valige kõige ülemisel ribal **Käivita**.</span><span class="sxs-lookup"><span data-stu-id="09c37-331">Select **Run** on the top-most ribbon.</span></span>
7. <span data-ttu-id="09c37-332">Salvestage loodud väljund kohapeal.</span><span class="sxs-lookup"><span data-stu-id="09c37-332">Save the generated output locally.</span></span> 
8. <span data-ttu-id="09c37-333">Võrrelge loodud väljundite sisu.</span><span class="sxs-lookup"><span data-stu-id="09c37-333">Compare the contents of the generated outputs.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="09c37-334">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="09c37-334">Additional resources</span></span>

- [<span data-ttu-id="09c37-335">Valemikoostaja elektroonilises aruandluses (ER)</span><span class="sxs-lookup"><span data-stu-id="09c37-335">Formula designer in Electronic reporting (ER)</span></span>](general-electronic-reporting-formula-designer.md)
- [<span data-ttu-id="09c37-336">Saate parandada ER-lahenduste jõudlust, lisades parameeteriseeritud ARVUTATUD VÄLJA andmeallikad</span><span class="sxs-lookup"><span data-stu-id="09c37-336">Improve performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>](er-calculated-field-ds-performance.md)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]