---
title: Saate parandada ER-lahenduste jõudlust, lisades parameeteriseeritud ARVUTATUD VÄLJA andmeallikad
description: Selles teemas selgitatakse, kuidas saate elektroonilise aruandluse (ER) lahenduste jõudlust parendada, lisades parameeteriseeritud ARVUTATUD VÄLJA andmeallikad.
author: NickSelin
ms.date: 04/23/2021
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
ms.openlocfilehash: 4ee5a074c5c6d2e2144181e39917b1cc42dfc015
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944829"
---
# <a name="improve-the-performance-of-er-solutions-by-adding-parameterized-calculated-field-data-sources"></a><span data-ttu-id="e05e5-103">Saate parandada ER-lahenduste jõudlust, lisades parameeteriseeritud ARVUTATUD VÄLJA andmeallikad</span><span class="sxs-lookup"><span data-stu-id="e05e5-103">Improve the performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e05e5-104">Selles teemas selgitatakse, kuidas saate jälgida käitatud [elektroonilise aruandluse (ER)](general-electronic-reporting.md) vormingute [jõudluse jälgi](trace-execution-er-troubleshoot-perf.md) ja seejärel kasutada nende jälgede teavet, et parandada jõudlust, konfigureerides parameetri **Arvutatud välja** andmeallikat.</span><span class="sxs-lookup"><span data-stu-id="e05e5-104">This topic explains how you can take [performance traces](trace-execution-er-troubleshoot-perf.md) of [Electronic reporting (ER)](general-electronic-reporting.md) formats that are run, and then use the information from those traces to help improve performance by configuring a parameterized **Calculated field** data source.</span></span>

<span data-ttu-id="e05e5-105">Üks osa ER-i konfiguratsioonide kujundamisest äridokumentide loomise jaoks on määratleda meetod, mida kasutatakse andmete saamiseks avaldusest, ja sisestada see loodud väljundisse.</span><span class="sxs-lookup"><span data-stu-id="e05e5-105">As part of the process of designing ER configurations to generate business documents, you define the method that is used to retrieve data from the application and enter it in the generated output.</span></span> <span data-ttu-id="e05e5-106">**Arvutatud välja** tüübi parameeteriseeritud ER-i andmeallika kujundamisega saate vähendada andmebaasi kutsete arvu ning vähendada oluliselt aega ja kulu, mis on seotud ER-i vormingu täitmise üksikasjade kogumisega.</span><span class="sxs-lookup"><span data-stu-id="e05e5-106">By designing a parametrized ER data source of the **Calculated field** type, you can reduce the number of database calls, and significantly reduce the time and cost that are involved in collecting the details of ER format execution.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e05e5-107">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="e05e5-107">Prerequisites</span></span>

- <span data-ttu-id="e05e5-108">Selles teemas toodud näidete läbimiseks peab teil olema juurdepääs ühele järgmistest [rollidest](../sysadmin/tasks/assign-users-security-roles.md).</span><span class="sxs-lookup"><span data-stu-id="e05e5-108">To complete the examples in this topic, you must have the access to one of the following [roles](../sysadmin/tasks/assign-users-security-roles.md):</span></span>

    - <span data-ttu-id="e05e5-109">Elektroonilise aruandluse arendaja</span><span class="sxs-lookup"><span data-stu-id="e05e5-109">Electronic reporting developer</span></span>
    - <span data-ttu-id="e05e5-110">Elektroonilise aruandluse funktsionaalne konsultant</span><span class="sxs-lookup"><span data-stu-id="e05e5-110">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="e05e5-111">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="e05e5-111">System administrator</span></span>

- <span data-ttu-id="e05e5-112">Ettevõtte sätteks peab olema seatud **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-112">The company must be set to **DEMF**.</span></span>
- <span data-ttu-id="e05e5-113">Järgige selle teema [1. lisas](#appendix1) toodud etappe, et laadida alla Microsofti ER-i näidislahenduse komponendid, mis on vajalikud selles teemas toodud näidete lõpuleviimiseks.</span><span class="sxs-lookup"><span data-stu-id="e05e5-113">Follow the steps in [Appendix 1](#appendix1) of this topic to download the components of the sample Microsoft ER solution that is required to complete the examples in this topic.</span></span>
- <span data-ttu-id="e05e5-114">Järgige selle teema [2. lisas](#appendix2) toodud etappe, et konfigureerida ER-i parameetrite minimaalne kogum, mis on vajalikud ER-i raamistiku kasutamiseks, et aidata parandada Microsofti ER-i näidislahenduse toimivust.</span><span class="sxs-lookup"><span data-stu-id="e05e5-114">Follow the steps in [Appendix 2](#appendix2) of this topic to configure the minimal set of ER parameters that is required to use the ER framework to help improve the performance of the sample Microsoft ER solution.</span></span>

## <a name="import-the-sample-er-solution"></a><span data-ttu-id="e05e5-115">ER-i näidislahenduse importimine</span><span class="sxs-lookup"><span data-stu-id="e05e5-115">Import the sample ER solution</span></span>

<span data-ttu-id="e05e5-116">Oletame, et peate kujundama uue ER-i lahenduse, et luua uus hankija kandeid esitav aruanne.</span><span class="sxs-lookup"><span data-stu-id="e05e5-116">Imagine that you must design an ER solution to generate a new report that shows vendor transactions.</span></span> <span data-ttu-id="e05e5-117">Praegu leiate valitud hankija kanded lehel **Hankija kanded** (avage **Ostureskontro** \> **Hankijad** \> **Kõik hankijad**, valige hankija ja seejärel valige toimingupaanil vahekaardi **Hankija** grupis **Kanded** suvand **Kanded**).</span><span class="sxs-lookup"><span data-stu-id="e05e5-117">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable** \> **Vendors** \> **All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="e05e5-118">Kuid teil on vaja, et kõik hankija kanded oleksid samal ajal ühes elektroonilises dokumendis XML-vormingus.</span><span class="sxs-lookup"><span data-stu-id="e05e5-118">However, you want to have all vendor transactions together in one electronic document in XML format.</span></span> <span data-ttu-id="e05e5-119">See lahendus koosneb mitmest ER-i konfiguratsioonist, mis sisaldavad nõutud andmemudelit, mudeli vastendust ja vormingu komponente.</span><span class="sxs-lookup"><span data-stu-id="e05e5-119">This solution will consist of several ER configurations that contain the required data model, model mapping, and format components.</span></span>

<span data-ttu-id="e05e5-120">Esimese etapina tuleb importida ER-i näidislahendus hankija kannete aruande loomiseks.</span><span class="sxs-lookup"><span data-stu-id="e05e5-120">The first step is to import the sample ER solution to generate a vendor transactions report.</span></span>

1. <span data-ttu-id="e05e5-121">Logige sisse Microsoft Dynamics 365 Finance'i eksemplari, mis on teie ettevõtte jaoks ette valmistatud.</span><span class="sxs-lookup"><span data-stu-id="e05e5-121">Sign in to the instance of Microsoft Dynamics 365 Finance that is provisioned for your company.</span></span>
2. <span data-ttu-id="e05e5-122">Selles teemas loote näidisettevõtte **Litware, Inc** jaoks konfiguratsioonid ja muudate neid.</span><span class="sxs-lookup"><span data-stu-id="e05e5-122">In this topic, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="e05e5-123">Veenduge, et see konfiguratsiooni pakkuja oleks teie Finance'i eksemplari lisatud ja on aktiivsena märgitud.</span><span class="sxs-lookup"><span data-stu-id="e05e5-123">Make sure that this configuration provider has been added to your Finance instance and is marked as active.</span></span> <span data-ttu-id="e05e5-124">Lisateabe saamiseks vaadake teemat [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="e05e5-124">For more information, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>
3. <span data-ttu-id="e05e5-125">Tööruumis **Elektrooniline aruandlus** valige paan **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-125">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="e05e5-126">Importige lehel **Konfiguratsioonid** ER-i konfiguratsioonid, mille eeltingimusena Finance'i alla laadisite, järgmises järjestuses: andmemudel, mudeli vastendus, vorming.</span><span class="sxs-lookup"><span data-stu-id="e05e5-126">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into Finance, in the following order: data model, model mapping, format.</span></span> <span data-ttu-id="e05e5-127">Toimige iga konfiguratsiooni puhul järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="e05e5-127">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="e05e5-128">Valige toimingupaanil suvand **Vahetus** \> **Laadi XML-failist**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-128">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
    2. <span data-ttu-id="e05e5-129">Valige käsk **Sirvi** ja valige ER-i konfiguratsiooni jaoks sobiv fail XML-vormingus.</span><span class="sxs-lookup"><span data-stu-id="e05e5-129">Select **Browse**, and select the appropriate file for the ER configuration in XML format.</span></span>
    3. <span data-ttu-id="e05e5-130">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-130">Select **OK**.</span></span>

![Imporditud konfiguratsioonid lehel Konfiguratsioonid](./media/er-calculated-field-ds-performance-imported-configurations.png)

## <a name="review-the-sample-er-solution"></a><span data-ttu-id="e05e5-132">ER-i näidislahenduse ülevaatamine</span><span class="sxs-lookup"><span data-stu-id="e05e5-132">Review the sample ER solution</span></span>

### <a name="review-the-model-mapping"></a><span data-ttu-id="e05e5-133">Mudeli vastendamise läbivaatamine</span><span class="sxs-lookup"><span data-stu-id="e05e5-133">Review the model mapping</span></span>

1. <span data-ttu-id="e05e5-134">Laiendage lehel **Konfiguratsioonid** vormingupuus suvand **Jõudlustäiustuse mudel** ja seejärel valige **Jõudlustäiustuse vastendamine**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-134">On the **Configurations** page, in the configuration tree, expand **Performance improvement model**, and select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="e05e5-135">Valige toimingupaanil valik **Koostaja**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-135">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="e05e5-136">Tehke lehe **Mudelist andmeallikasse vastendamine** tegevuse paanil valik **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-136">On the **Model to datasource mapping** page, on the Action Pane, select **Designer**.</span></span>

    <span data-ttu-id="e05e5-137">See ER-mudeli vastendus on ette nähtud selleks, et teha järgmist.</span><span class="sxs-lookup"><span data-stu-id="e05e5-137">This ER model mapping is designed to perform the following actions:</span></span>

    - <span data-ttu-id="e05e5-138">Saate tuua tabelis VendTrans (andmeallikas **Kanded**) talletatud hankija kannete loendi.</span><span class="sxs-lookup"><span data-stu-id="e05e5-138">Fetch the list of vendor transactions that are stored in the VendTrans table (**Trans** data source).</span></span>
    - <span data-ttu-id="e05e5-139">Iga kande korral tooge tabelist VendTable selle hankija kirje, kelle jaoks kanne on sisestatud (andmeallikas **\#Hankija**).</span><span class="sxs-lookup"><span data-stu-id="e05e5-139">For every transaction, fetch, from the VendTable table, the record of a vendor that the transaction has been posted for (**\#Vend** data source).</span></span>

    > [!NOTE]
    > <span data-ttu-id="e05e5-140">Andmeallikas **\#Hankija** on konfigureeritud tooma vastavat hankija kirjet, kasutades olemasolevat üks-ühele seost **\@.'\>Relations'.VendTable\_AccountNum**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-140">The **\#Vend** data source is configured to fetch the corresponding vendor record by using the existing many-to-one relation **\@.'\>Relations'.VendTable\_AccountNum**.</span></span>

    <span data-ttu-id="e05e5-141">Selle konfiguratsiooni mudeli vastendamine rakendab põhiandmete mudelit selle mudeli jaoks loodud ER-vormingute korral, mida kasutatakse rakenduses Finance.</span><span class="sxs-lookup"><span data-stu-id="e05e5-141">The model mapping in this configuration implements the base data model for any ER formats that are created for this model and run in Finance.</span></span> <span data-ttu-id="e05e5-142">Selle tulemusena on andmeallika **Kanded** sisu avatud ER-vormingute, näiteks abstraktsete **andmemudeli** allikate korral.</span><span class="sxs-lookup"><span data-stu-id="e05e5-142">Therefore, the content of the **Trans** data source is exposed for ER formats such as abstract **model** data sources.</span></span>

    ![Andmeallikas Kanded mudeli vastenduse koostaja lehel](media/er-calculated-field-ds-performance-mapping-1.png)

4. <span data-ttu-id="e05e5-144">Sulgege leht **Mudelivastenduse kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-144">Close the **Model mapping designer** page.</span></span>
5. <span data-ttu-id="e05e5-145">Sulgege leht **Mudelist andmeallikasse vastendamine**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-145">Close the **Model to datasource mapping** page.</span></span>

### <a name="review-format"></a><span data-ttu-id="e05e5-146">Läbivaatuse vorming</span><span class="sxs-lookup"><span data-stu-id="e05e5-146">Review format</span></span>

1. <span data-ttu-id="e05e5-147">Laiendage lehel **Konfiguratsioonid** vormingupuus suvand **Jõudlustäiustuse mudel** ja seejärel valige **Jõudlustäiustuse vorming**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-147">On the **Configurations** page, in the configuration tree, expand **Performance improvement model**, and select **Performance improvement format**.</span></span>
2. <span data-ttu-id="e05e5-148">Valige toimingupaanil valik **Koostaja**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-148">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="e05e5-149">Tehke lehe **Vormingu kujundaja** vahekaardil **Vastendamine** valik **Laienda/ahenda**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-149">On the **Format designer** page, on the **Mapping** tab, select **Expand/Collapse**.</span></span>
4. <span data-ttu-id="e05e5-150">Laiendage üksusi **Mudel**, **Andmed** ja **Kanne**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-150">Expand the **Model**, **Data,** and **Transaction** items.</span></span>

    <span data-ttu-id="e05e5-151">See ER-vorming on loodud hankija kannete aruande loomiseks XML-vormingus.</span><span class="sxs-lookup"><span data-stu-id="e05e5-151">This ER format is designed to generate a vendor transactions report in XML format.</span></span>

    ![Vorminguelementide andmeallikate ja konfigureeritud sidumiste vormindamine vormingu koostaja lehel](media/er-calculated-field-ds-performance-format.png)

5. <span data-ttu-id="e05e5-153">Sulgege **Vormingu kujundaja** leht.</span><span class="sxs-lookup"><span data-stu-id="e05e5-153">Close the **Format designer** page.</span></span>

## <a name="run-the-sample-er-solution-to-trace-execution"></a><span data-ttu-id="e05e5-154">Muudetud ER-i näidislahenduse kasutamine täitmise jälituseks</span><span class="sxs-lookup"><span data-stu-id="e05e5-154">Run the sample ER solution to trace execution</span></span>

<span data-ttu-id="e05e5-155">Oletame, et olete lõpetanud ER-i lahenduse esimese versiooni kujundamise.</span><span class="sxs-lookup"><span data-stu-id="e05e5-155">Imagine that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="e05e5-156">Nüüd soovite lahendust testida oma rakenduse Finance eksemplaris ja analüüsida täitmise jõudlust.</span><span class="sxs-lookup"><span data-stu-id="e05e5-156">You now want to test the solution in your Finance instance and analyze the execution performance.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="e05e5-157">ER-i jõudluse jälituse sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="e05e5-157">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="e05e5-158">Valige ettevõte **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-158">Select the **DEMF** company.</span></span>
2. <span data-ttu-id="e05e5-159">Järgige teemas [ER-i jõudluse jälituse sisselülitamine](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) toodud juhiseid, et luua jõudluse jälitus ER-vormingu käivitamisel.</span><span class="sxs-lookup"><span data-stu-id="e05e5-159">Follow the steps in [Turn on the ER performance trace](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) to generate a performance trace while an ER format is run.</span></span>

    ![Kasutaja parameetrite dialoogiaken](media/er-calculated-field-ds-performance-format-user-parameters.png)

### <a name="run-the-er-format"></a><a id="run-format"></a><span data-ttu-id="e05e5-161">ER-vormingu käivitamine</span><span class="sxs-lookup"><span data-stu-id="e05e5-161">Run the ER format</span></span>

1. <span data-ttu-id="e05e5-162">Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-162">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="e05e5-163">Tehke lehe **Konfiguratsioonid** konfiguratsioonipuul valik **Jõudlustäiustuse vorming**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-163">On the **Configurations** page, in the configuration tree, select **Performance improvement format**.</span></span>
3. <span data-ttu-id="e05e5-164">Valige toimingupaanil käsk **Käivita**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-164">On the Action Pane, select **Run**.</span></span>

## <a name="use-the-performance-trace-to-analyze-model-mapping-performance"></a><span data-ttu-id="e05e5-165">Jõudluse jälituse kasutamine mudeli vastenduse jõudluse analüüsimiseks</span><span class="sxs-lookup"><span data-stu-id="e05e5-165">Use the performance trace to analyze model mapping performance</span></span>

1. <span data-ttu-id="e05e5-166">Tehke lehe **Konfiguratsioonid** konfiguratsioonipuul valik **Jõudlustäiustuse vastendamine**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-166">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="e05e5-167">Valige toimingupaanil valik **Koostaja**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-167">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="e05e5-168">Tehke lehe **Mudeli vastendused** tegevuse paanil valik **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-168">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="e05e5-169">Valige lehe **Mudelivastenduse koostaja** toimingupaanil **Jõudluse jälitus**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-169">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="e05e5-170">Valige viimati loodud jälitus ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-170">Select the most recent trace that was generated, and then select **OK**.</span></span>

<span data-ttu-id="e05e5-171">Praeguse mudeli vastenduse mõne andmeallika üksuse kohta on kättesaadav uus teave.</span><span class="sxs-lookup"><span data-stu-id="e05e5-171">New information is now available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="e05e5-172">Tegelik aeg, mis kulus andmeallika abil andmete toomisele</span><span class="sxs-lookup"><span data-stu-id="e05e5-172">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="e05e5-173">Sama aeg väljendatuna protsendina koguajast, mis kulutati kogu mudelivastenduse käitamise peale</span><span class="sxs-lookup"><span data-stu-id="e05e5-173">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

![Käivitamise aja üksikasjad Mudeli vastenduse koostaja lehel](./media/er-calculated-field-ds-performance-mapping-2.png)

<span data-ttu-id="e05e5-175">Ruudustik **Jõudluse statistika** näitab, et andmeallikas **Kanded** kutsub tabeli VendTrans ühel korral.</span><span class="sxs-lookup"><span data-stu-id="e05e5-175">The **Performance statistics** grid shows that the **Trans** data source calls the VendTrans table one time.</span></span> <span data-ttu-id="e05e5-176">Andmeallika **Kanded** väärtus **\[265\]\[Q:265\]** näitab, et avalduse tabelist on toodud 265 hankija kannet ja need on tagastatud andmemudelisse.</span><span class="sxs-lookup"><span data-stu-id="e05e5-176">The value **\[265\]\[Q:265\]** of the **Trans** data source indicates that 265 vendor transactions have been fetched from the application table and returned to the data model.</span></span>

<span data-ttu-id="e05e5-177">Ruudustik **Jõudluse statistika** näitab ka, et praegune mudelivastendus dubleerib andmebaasi taotlusi, samal ajal kui käivitatakse andmeallikas **\#Hankija**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-177">The **Performance statistics** grid also shows that the current model mapping duplicates database requests while the **\#Vend** data source is run.</span></span> <span data-ttu-id="e05e5-178">Dubleerimine toimub järgmistel põhjustel.</span><span class="sxs-lookup"><span data-stu-id="e05e5-178">This duplication occurs for the following reasons:</span></span>

- <span data-ttu-id="e05e5-179">Hankija tabelit kutsutakse iga 265 itereeritud hankija kande korral kaks korda; kokku on 530 kutset.</span><span class="sxs-lookup"><span data-stu-id="e05e5-179">The vendor table is called two times for each of the 265 iterated vendor transactions, for a total of 530 calls:</span></span>

    - <span data-ttu-id="e05e5-180">Üks kutse tehakse hankija kontonumbri sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="e05e5-180">One call is made to enter the vendor account number.</span></span>
    - <span data-ttu-id="e05e5-181">Üks kutse tehakse hankija nime sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="e05e5-181">One call is made to enter the vendor name.</span></span>

- <span data-ttu-id="e05e5-182">Hankija tabelit kutsutakse iga itereeritud hankija kande korral, kuigi toodud kanded on sisestatud ainult viie hankija kohta.</span><span class="sxs-lookup"><span data-stu-id="e05e5-182">The vendor table is called for each iterated vendor transaction, even though the fetched transactions have been posted for only five vendors.</span></span> <span data-ttu-id="e05e5-183">530 kutsest 525 on duplikaadid.</span><span class="sxs-lookup"><span data-stu-id="e05e5-183">Of the 530 calls, 525 are duplicates.</span></span> <span data-ttu-id="e05e5-184">Järgmisel illustratsioonil on kujutatud teade, mis kuvatakse duplikaatkutsete (andmebaasitaotluste) kohta.</span><span class="sxs-lookup"><span data-stu-id="e05e5-184">The following illustration shows the message that you receive about duplicate calls (database requests).</span></span>

![Teade dubleeritud andmebaasi taotluste kohta mudelivastenduse koostaja lehel](./media/er-calculated-field-ds-performance-mapping-2a.png)

<span data-ttu-id="e05e5-186">Pange tähele, et mudelivastenduse käivitamise koguajast (ligikaudu kaheksa sekundit) on kulunud rohkem kui 80 protsenti (ligikaudu kuus sekundit) avalduse tabelist VendTable väärtuste toomisele.</span><span class="sxs-lookup"><span data-stu-id="e05e5-186">Of the total model mapping execution time (approximately eight seconds), notice that more than 80 percent (approximately six seconds) has been spent retrieving values from the VendTable application table.</span></span> <span data-ttu-id="e05e5-187">See protsent on viie hankija kahe atribuudi jaoks liiga suur, võrreldes avalduse tabelist VendTrans pärit andmete mahuga.</span><span class="sxs-lookup"><span data-stu-id="e05e5-187">That percentage is too large for two attributes of five vendors, compared with the volume of information from the VendTrans application table.</span></span>

<span data-ttu-id="e05e5-188">Hankija teabe saamiseks iga tehingu kohta tehtud kutsete arvu vähendamiseks ja mudelivastenduse jõudluse parandamiseks saate kasutada andmeallika **\#Hankija** vahemällu salvestamist.</span><span class="sxs-lookup"><span data-stu-id="e05e5-188">To reduce the number of calls that are made to get the vendor details for every transaction, and to improve the performance of the model mapping, you can use caching for the **\#Vend** data source.</span></span>

> [!NOTE]
> <span data-ttu-id="e05e5-189">Andmeallikas **Kanne\\\#Hankija** salvestatakse vahemällu käitusajal andmeallika **Kanne** praeguse kande ulatuses.</span><span class="sxs-lookup"><span data-stu-id="e05e5-189">The **Trans\\\#Vend** data source will be cached in the scope of the current transaction of the **Trans** data source at runtime.</span></span>

<span data-ttu-id="e05e5-190">Andmeallika **\#Hankija** vahemällu salvestades vähendate dubleeritud kutsete arvu 525-lt 260-le, kuid te ei kõrvalda dubleerimist täielikult.</span><span class="sxs-lookup"><span data-stu-id="e05e5-190">By caching the **\#Vend** data source, you reduce the number of duplicated calls from 525 to 260, but you don't completely eliminate the duplication.</span></span> <span data-ttu-id="e05e5-191">Dubleerimise täielikuks kõrvaldamiseks saate konfigureerida uue parameetritega andmeallika, mille tüüp on **Arvutatud väli**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-191">To completely eliminate duplication, you can configure a new parameterized data source of the **Calculated field** type.</span></span>

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="e05e5-192">Mudelivastenduse parandamine täitmise jälitusest saadud teabe põhjal</span><span class="sxs-lookup"><span data-stu-id="e05e5-192">Improve the model mapping based on information from the execution trace</span></span>

### <a name="change-the-logic-of-the-model-mapping"></a><span data-ttu-id="e05e5-193">Mudelivastenduse loogika muutmine</span><span class="sxs-lookup"><span data-stu-id="e05e5-193">Change the logic of the model mapping</span></span>

<span data-ttu-id="e05e5-194">Järgige järgmisi juhiseid vahemällu salvestamise ja tüübiga **Arvutatud väli** andmeallika kasutamiseks, et vältida andmebaasi duplikaatkutseid.</span><span class="sxs-lookup"><span data-stu-id="e05e5-194">Follow these steps to use caching and a data source of the **Calculated field** type, to help prevent duplicate calls to the database.</span></span>

1. <span data-ttu-id="e05e5-195">Tehke lehe **Konfiguratsioonid** konfiguratsioonipuul valik **Jõudlustäiustuse vastendamine**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-195">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="e05e5-196">Valige toimingupaanil valik **Koostaja**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-196">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="e05e5-197">Tehke lehe **Mudeli vastendused** tegevuse paanil valik **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-197">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="e05e5-198">Lehel **Mudelivastenduse koostaja** tehke järgmist, et lisada tüübiga andmeallikas **Tabeli kirjed** avalduse tabeli VendTable kirjetele juurdepääsemiseks.</span><span class="sxs-lookup"><span data-stu-id="e05e5-198">On the **Model mapping designer** page, follow these steps to add a data source of the **Table records** type to access records in the VendTable application table:</span></span>

    1. <span data-ttu-id="e05e5-199">Laiendage paanil **Andmeallika tüübid** teenust **Dynamics 365 for Operations** ja valige suvand **Tabeli kirjed**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-199">In the **Data source types** pane, expand **Dynamics 365 for Operations**, and select **Table records**.</span></span>
    2. <span data-ttu-id="e05e5-200">Valige **Lisa juur**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-200">Select **Add root**.</span></span>
    3. <span data-ttu-id="e05e5-201">Sisestage dialoogiboksis väljale **Nimi** väärtus **Hankija**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-201">In the dialog box, in the **Name** field, enter **Vend**.</span></span>
    4. <span data-ttu-id="e05e5-202">Sisestage väljale **Tabel** väärtus **VendTable**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-202">In the **Table** field, enter **VendTable**.</span></span>
    5. <span data-ttu-id="e05e5-203">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-203">Select **OK**.</span></span>

5. <span data-ttu-id="e05e5-204">Tüübiga **Arvutatud väljad** andmeallikate kutsed saate parametriseerida ainult juhul, kui need andmeallikad asuvad konteineris.</span><span class="sxs-lookup"><span data-stu-id="e05e5-204">You can parameterize calls to data sources of the **Calculated field** type only if those data sources reside in a container.</span></span> <span data-ttu-id="e05e5-205">Seetõttu tehke järgmist, et lisada tüübiga **Tühi konteiner** andmeallikas, et säilitada uus tüübiga **Arvutatud väli** parametriseeritud andmeallikas.</span><span class="sxs-lookup"><span data-stu-id="e05e5-205">Therefore, follow these steps to add a data source of the **Empty container** type to hold a new parameterized data source of the **Calculated field** type:</span></span>

    1. <span data-ttu-id="e05e5-206">Laiendage paanil **Andmeallika tüübid** suvandit **Üldine** ja valige **Tühi konteiner**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-206">In the **Data source types** pane, expand **General**, and select **Empty container**.</span></span>
    2. <span data-ttu-id="e05e5-207">Valige **Lisa juur**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-207">Select **Add root**.</span></span>
    3. <span data-ttu-id="e05e5-208">Sisestage dialoogiboksis väljale **Nimi** väärtus **Väli**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-208">In the dialog box, in the **Name** field, enter **Box**.</span></span>
    3. <span data-ttu-id="e05e5-209">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-209">Select **OK**.</span></span>

    ![Andmeallikas Väli mudeli vastenduse koostaja lehel](./media/er-calculated-field-ds-performance-mapping-3.png)

6. <span data-ttu-id="e05e5-211">Tüübiga **Arvutatud väli** parametriseeritud andmeallika lisamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="e05e5-211">Follow these steps to add a parameterized data source of the **Calculated field** type:</span></span>

    1. <span data-ttu-id="e05e5-212">Tehke paanil **Andmeallikad** valik **Väli**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-212">In the **Data sources** pane, select **Box**.</span></span>
    2. <span data-ttu-id="e05e5-213">Laiendage paanil **Andmeallika tüübid** üksust **Funktsioonid** ja valige üksus **Arvutatud väli**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-213">In the **Data source types** pane, expand **Functions**, and select **Calculated field**.</span></span>
    3. <span data-ttu-id="e05e5-214">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-214">Select **Add**.</span></span>
    4. <span data-ttu-id="e05e5-215">Sisestage dialoogiboksis väljale **Nimi** väärtus **Hankija**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-215">In the dialog box, in the **Name** field, enter **Vend**.</span></span>
    5. <span data-ttu-id="e05e5-216">Valige **Valemi redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-216">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="e05e5-217">Tehke lehel **Valemikoostaja** valik **Parameetrid**, et määrata parameetrid, mis tuleb selle andmeallika kutsumisel esitada.</span><span class="sxs-lookup"><span data-stu-id="e05e5-217">On the **Formula designer** page, select **Parameters** to specify the parameters that must be provided when this data source is called.</span></span>
    7. <span data-ttu-id="e05e5-218">Tehke dialoogiaknas **Parameetrid** valik **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-218">In the **Parameters** dialog box, select **New**.</span></span>
    8. <span data-ttu-id="e05e5-219">Sisestage väljale **Nimi** väärtus **parmVendAccNumber**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-219">In the **Name** field, enter **parmVendAccNumber**.</span></span>
    9. <span data-ttu-id="e05e5-220">Valige väljalt **Tüüp** suvand **String**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-220">In the **Type** field, select **String**.</span></span>
    10. <span data-ttu-id="e05e5-221">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-221">Select **OK**.</span></span>
    11. <span data-ttu-id="e05e5-222">Sisestage väljale **Valem** tekst **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-222">In the **Formula** field, enter **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**.</span></span>
    12. <span data-ttu-id="e05e5-223">Valige **Salvesta** ja sulgege leht **Valemikoostaja**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-223">Select **Save**, and close the **Formula designer** page.</span></span>
    13. <span data-ttu-id="e05e5-224">Uue andmeallika lisamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-224">Select **OK** to add the new data source.</span></span>

7. <span data-ttu-id="e05e5-225">Kui soovite, et lisatud andmeallikas oleks käivitamise ajal vahemällu salvestatud, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="e05e5-225">Follow these steps to mark the added data source as cached during the execution:</span></span>

    1. <span data-ttu-id="e05e5-226">Valige paanil **Andmeallikad** suvand **Väli\\Hankija**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-226">In the **Data sources** pane, select **Box\\Vend**.</span></span>
    2. <span data-ttu-id="e05e5-227">Valige suvand **Vahemälu**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-227">Select **Cache**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e05e5-228">Andmeallikas **Väli\\Hankija** salvestatakse vahemällu käitusajal andmeallika **Hankija** kõigi hankija kannete ulatuses.</span><span class="sxs-lookup"><span data-stu-id="e05e5-228">The **Box\\Vend** data source will be cached in the scope of all vendor transactions of the **Trans** data source at runtime.</span></span>

8. <span data-ttu-id="e05e5-229">Pesastatud andmeallika **Kanne\\\#Hankija** värskendamiseks nii, et see kasutaks andmeallikat **Väli\\Hankija**, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="e05e5-229">Follow these steps to update the nested **Trans\\\#Vend** data source so that it uses the **Box\\Vend** data source:</span></span>

    1. <span data-ttu-id="e05e5-230">Laiendage paanil **Andmeallikad** suvandit **Kanne**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-230">In the **Data sources** pane, expand **Trans**.</span></span>
    2. <span data-ttu-id="e05e5-231">Valige andmeallikas **Kanne\\\#Hankija** ja seejärel valige **Redigeerimine** \> **Redigeeri valemit**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-231">Select the **Trans\\\#Vend** data source, and then select **Edit** \> **Edit formula**.</span></span>
    3. <span data-ttu-id="e05e5-232">Sisestage lehe **Valemikoostaja** väljale **Valem** tekst **Box.Vend(\@.AccountNum)**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-232">On the **Formula designer** page, in the **Formula** field, enter **Box.Vend(\@.AccountNum)**.</span></span>
    4. <span data-ttu-id="e05e5-233">Valige käsk **Salvesta** ja sulgege leht **Valemikoostaja**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-233">Select **Save**, and then close the **Formula designer** page.</span></span>
    5. <span data-ttu-id="e05e5-234">Valitud andmeallika muudatuste lõpuleviimiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-234">Select **OK** to complete your changes to the selected data source.</span></span>

9. <span data-ttu-id="e05e5-235">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-235">Select **Save**.</span></span>

    ![Andmeallikas Hankija mudeli vastenduse koostaja lehel](./media/er-calculated-field-ds-performance-mapping-4.png)

10. <span data-ttu-id="e05e5-237">Sulgege leht **Mudelivastenduse kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-237">Close the **Model mapping designer** page.</span></span>
11. <span data-ttu-id="e05e5-238">Sulgege leht **Mudelivastendused**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-238">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="e05e5-239">ER-i mudelivastenduse muudetud versiooni lõpetamine</span><span class="sxs-lookup"><span data-stu-id="e05e5-239">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="e05e5-240">Valige lehe **Konfiguratsioonid** kiirkaardil **Versioonid** konfiguratsiooni **Jõudlustäiustuse vastendamine** versioon **1.2**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-240">On the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance improvement mapping** configuration.</span></span>
2. <span data-ttu-id="e05e5-241">Valige **Muuda olekut** \> **Valmis** ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-241">Select **Change status** \> **Complete**, and then select **OK**.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="e05e5-242">Muudetud ER-i lahenduse kasutamine täitmise jälituseks</span><span class="sxs-lookup"><span data-stu-id="e05e5-242">Run the modified ER solution to trace execution</span></span>

<span data-ttu-id="e05e5-243">Korrake samme selle teema jaotises [ER-vormingu käivitamine](#run-format), et luua uus jõudluse jälg.</span><span class="sxs-lookup"><span data-stu-id="e05e5-243">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="use-the-performance-trace-to-analyze-adjustments-to-the-model-mapping"></a><span data-ttu-id="e05e5-244">Jõudluse jälituse kasutamine mudeli vastenduse korrigeerimiste analüüsimiseks</span><span class="sxs-lookup"><span data-stu-id="e05e5-244">Use the performance trace to analyze adjustments to the model mapping</span></span> 

1. <span data-ttu-id="e05e5-245">Tehke lehe **Konfiguratsioonid** konfiguratsioonipuul valik **Jõudlustäiustuse vastendamine**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-245">On the **Configurations** page, in the configuration tree, select **Performance improvement mapping**.</span></span>
2. <span data-ttu-id="e05e5-246">Valige toimingupaanil valik **Koostaja**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-246">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="e05e5-247">Tehke lehe **Mudeli vastendused** tegevuse paanil valik **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-247">On the **Model mappings** page, on the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="e05e5-248">Valige lehe **Mudelivastenduse koostaja** toimingupaanil **Jõudluse jälitus**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-248">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="e05e5-249">Valige viimati loodud jälitus ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-249">Select the most recent trace that was generated, and then select **OK**.</span></span>

<span data-ttu-id="e05e5-250">Pange tähele, et kohandused, mida tegite mudelivastendusele, on eemaldanud dubleeritud päringud andmebaasile.</span><span class="sxs-lookup"><span data-stu-id="e05e5-250">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="e05e5-251">Vähendatud on ka selle mudelivastenduse kutsete arvu andmebaasi tabelitele ja andmeallikatele.</span><span class="sxs-lookup"><span data-stu-id="e05e5-251">The number of calls to database tables and data sources for this model mapping has also been reduced.</span></span>

![Jälitusteave mudeli vastenduse koostaja lehel 1](./media/er-calculated-field-ds-performance-mapping-5.png)

<span data-ttu-id="e05e5-253">Täitmisaega on vähendatud umbes 20 korda (umbes 8 sekundilt 400 millisekundini).</span><span class="sxs-lookup"><span data-stu-id="e05e5-253">The total execution time has been reduced about 20 times (from about 8 seconds to about 400 milliseconds).</span></span> <span data-ttu-id="e05e5-254">See on parandanud kogu ER-lahenduse jõudlus.</span><span class="sxs-lookup"><span data-stu-id="e05e5-254">Therefore, the performance of the whole ER solution has been improved.</span></span>

![Jälitusteave mudeli vastenduse koostaja lehel 2](./media/er-calculated-field-ds-performance-mapping-5a.png)

## <a name="appendix-1-download-the-components-of-the-sample-microsoft-er-solution"></a><a name="appendix1"></a><span data-ttu-id="e05e5-256">Lisa 1: laadige alla Microsofti ER-näidislahenduse komponendid</span><span class="sxs-lookup"><span data-stu-id="e05e5-256">Appendix 1: Download the components of the sample Microsoft ER solution</span></span>

<span data-ttu-id="e05e5-257">Peate alla laadima ja kohalikult talletama järgmised failid.</span><span class="sxs-lookup"><span data-stu-id="e05e5-257">You must download the following files and store them locally.</span></span>

| <span data-ttu-id="e05e5-258">Fail</span><span class="sxs-lookup"><span data-stu-id="e05e5-258">File</span></span>                                        | <span data-ttu-id="e05e5-259">Sisu</span><span class="sxs-lookup"><span data-stu-id="e05e5-259">Content</span></span> |
|---------------------------------------------|---------|
| <span data-ttu-id="e05e5-260">Jõudlustäiustuse mudel, versioon 1</span><span class="sxs-lookup"><span data-stu-id="e05e5-260">Performance improvement model.version.1</span></span>     | [<span data-ttu-id="e05e5-261">ER-i andmemudeli konfiguratsiooni näide</span><span class="sxs-lookup"><span data-stu-id="e05e5-261">Sample ER data model configuration</span></span>](https://download.microsoft.com/download/4/6/f/46f0f3fa-782b-414a-8f7b-b6c64a388661/Performance_improvement_model.version.1.xml) |
| <span data-ttu-id="e05e5-262">Jõudlustäiustuse vastendamine, versioon 1.1</span><span class="sxs-lookup"><span data-stu-id="e05e5-262">Performance improvement mapping.version.1.1</span></span> | [<span data-ttu-id="e05e5-263">ER-i mudelivastenduse konfiguratsiooni näide</span><span class="sxs-lookup"><span data-stu-id="e05e5-263">Sample ER model mapping configuration</span></span>](https://download.microsoft.com/download/8/9/1/8913a763-afb8-4bf4-aaf1-95ad793ffc5a/Performance_improvement_mapping.version.1.1.xml) |
| <span data-ttu-id="e05e5-264">Jõudlustäiustuse vorming, versioon 1.1</span><span class="sxs-lookup"><span data-stu-id="e05e5-264">Performance improvement format.version.1.1</span></span>  | [<span data-ttu-id="e05e5-265">ER-vormingu konfiguratsiooni näide</span><span class="sxs-lookup"><span data-stu-id="e05e5-265">Sample ER format configuration</span></span>](https://download.microsoft.com/download/9/0/c/90c75963-bc78-4edc-9096-556bbe281f10/Performance_improvement_format.version.1.1.xml) |

## <a name="appendix-2-configure-the-er-framework"></a><a name="appendix2"></a><span data-ttu-id="e05e5-266">Lisa 2: ER-raamistiku konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="e05e5-266">Appendix 2: Configure the ER framework</span></span>

<span data-ttu-id="e05e5-267">Enne kui saate hakata kasutama ER-raamistikku, et parandada Microsofti ER-näidislahenduse jõudlust, peate konfigureerima ER-i parameetrite minimaalse kogumi.</span><span class="sxs-lookup"><span data-stu-id="e05e5-267">Before you can start to use the ER framework to improve the performance of the sample Microsoft ER solution, you must configure the minimal set of ER parameters.</span></span>

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a><span data-ttu-id="e05e5-268">Elektroonilise aruandluse parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="e05e5-268">Configure ER parameters</span></span>

1. <span data-ttu-id="e05e5-269">Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-269">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="e05e5-270">Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Seostatud lingid** paan **Elektroonilise aruandluse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-270">On the **Localization configurations** page, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="e05e5-271">Valige lehel **Elektroonilise aruandluse parameetrid** vahekaardil **Üldine** suvandi **Luba kujundusrežiim** sätteks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-271">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="e05e5-272">Vahekaardil **Manused** määrake järgmised parameetrid.</span><span class="sxs-lookup"><span data-stu-id="e05e5-272">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="e05e5-273">Valige väljal **Konfiguratsioonid** tüüp **Fail** ettevõttele **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-273">In the **Configurations** field, select the **File** type for the **DEMF** company.</span></span>
    - <span data-ttu-id="e05e5-274">Valige väljadel **Töö arhiiv**, **Ajutine**, **Alus** ja **Muud** tüüp **Fail**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-274">In the **Job archive**, **Temporary**, **Baseline**, and **Others** fields, select the **File** type.</span></span>

<span data-ttu-id="e05e5-275">Lisateavet ER-parameetrite kohta vt jaotisest [ER-raamistiku konfigureerimine](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="e05e5-275">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="e05e5-276">ER-konfiguratsiooni pakkuja aktiveerimine</span><span class="sxs-lookup"><span data-stu-id="e05e5-276">Activate an ER configuration provider</span></span>

<span data-ttu-id="e05e5-277">Kõigile lisatud ER-konfiguratsioonidele on märgitud omanikuks ER-konfiguratsiooni pakkuja.</span><span class="sxs-lookup"><span data-stu-id="e05e5-277">Every ER configuration that is added is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="e05e5-278">Sel eesmärgil kasutatakse tööruumis **Elektrooniline aruandlus** aktiveeritud ER-konfiguratsiooni pakkujat.</span><span class="sxs-lookup"><span data-stu-id="e05e5-278">The ER configuration provider that is activated in the **Electronic reporting** workspace is used for this purpose.</span></span> <span data-ttu-id="e05e5-279">Seega enne ER-konfiguratsioonide lisamist või redigeerimist peate aktiveerima tööruumis **Elektrooniline aruandlus** ER-konfiguratsiooni pakkuja.</span><span class="sxs-lookup"><span data-stu-id="e05e5-279">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="e05e5-280">ER-konfiguratsiooni saab redigeerida ainult konfiguratsiooni omanik.</span><span class="sxs-lookup"><span data-stu-id="e05e5-280">Only the owner of an ER configuration can edit the configuration.</span></span> <span data-ttu-id="e05e5-281">Seega enne ER-konfiguratsiooni redigeerimist pea olema tööruumis **Elektrooniline aruandlus** aktiveeriud vastav ER-konfiguratsiooni pakkuja.</span><span class="sxs-lookup"><span data-stu-id="e05e5-281">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a><span data-ttu-id="e05e5-282">ER-konfiguratsiooni pakkujate loendi ülevaatamine</span><span class="sxs-lookup"><span data-stu-id="e05e5-282">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="e05e5-283">Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-283">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="e05e5-284">Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Seostatud lingid** paan **Konfiguratsioonipakkujad**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-284">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="e05e5-285">Lehel **Konfiguratsioonipakkuja tabel** on igal pakkuja kirjel kordumatu nimi ja URL.</span><span class="sxs-lookup"><span data-stu-id="e05e5-285">On the **Configuration provider table** page, each provider record has a unique name and URL.</span></span> <span data-ttu-id="e05e5-286">Vaadake üle selle lehe sisu.</span><span class="sxs-lookup"><span data-stu-id="e05e5-286">Review the contents of this page.</span></span> <span data-ttu-id="e05e5-287">Kui üksuse **Litware, Inc.** kirje on juba olemas, jätke järgmine protseduur vahele, vt [Uue ER-vormingu konfiguratsioonipakkuja lisamine](#ActivateProvider).</span><span class="sxs-lookup"><span data-stu-id="e05e5-287">If a record for **Litware, Inc.** already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="e05e5-288">Uue ER-konfiguratsiooni pakkuja lisamine</span><span class="sxs-lookup"><span data-stu-id="e05e5-288">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="e05e5-289">Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-289">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="e05e5-290">Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Seostatud lingid** paan **Konfiguratsioonipakkujad**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-290">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="e05e5-291">Lehel **Konfiguratsioonipakkujad** valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-291">On the **Configuration providers** page, select **New**.</span></span>
4. <span data-ttu-id="e05e5-292">Väljale **Nimi** sisestage väärtus **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="e05e5-292">In the **Name** field, enter **Litware, Inc.**</span></span>
5. <span data-ttu-id="e05e5-293">Sisestage väljale **Interneti-aadress** `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="e05e5-293">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
6. <span data-ttu-id="e05e5-294">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-294">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a><span data-ttu-id="e05e5-295">ER-konfiguratsiooni pakkuja aktiveerimine</span><span class="sxs-lookup"><span data-stu-id="e05e5-295">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="e05e5-296">Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-296">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="e05e5-297">Vailge lehe **Lokaliseerimise konfiguratsioonid** jaotises **Konfiguratsioonipakkujad** paan **Litware, Inc.** ja seejärel valige **Määra aktiivne**.</span><span class="sxs-lookup"><span data-stu-id="e05e5-297">On the **Localization configurations** page, in the **Configuration providers** section, select the **Litware, Inc.** tile, and then select **Set active**.</span></span>

<span data-ttu-id="e05e5-298">Lisateabe saamiseks ER-konfiguratsiooni pakkujate kohta vaadake teemat [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="e05e5-298">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e05e5-299">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="e05e5-299">Additional resources</span></span>

- [<span data-ttu-id="e05e5-300">Elektroonilise aruandluse ülevaade</span><span class="sxs-lookup"><span data-stu-id="e05e5-300">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="e05e5-301">Elektroonilise aruandluse vormingute täitmise jälitamine jõudlusprobleemide tõrkeotsingu tegemiseks</span><span class="sxs-lookup"><span data-stu-id="e05e5-301">Trace the execution of ER formats to troubleshoot performance issues</span></span>](trace-execution-er-troubleshoot-perf.md)
- [<span data-ttu-id="e05e5-302">Arvutatud väljatüübi ER-andmeallikate parameetritega kõned</span><span class="sxs-lookup"><span data-stu-id="e05e5-302">Support parameterized calls of ER data sources of the Calculated field type</span></span>](er-calculated-field-type.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
