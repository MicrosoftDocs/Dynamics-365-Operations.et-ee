---
title: ER-vormingu parameetrite seadistamine juriidilise isiku kohta
description: Selles teemas selgitatakse, kuidas seadistada elektroonilise aruandluse (ER) vormingu parameetreid juriidilise isiku kohta.
author: NickSelin
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: b51a7ae8587a3cbb65efc4af574929efcbc8fbf8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681468"
---
# <a name="set-up-the-parameters-of-an-er-format-per-legal-entity"></a><span data-ttu-id="54902-103">ER-vormingu parameetrite seadistamine juriidilise isiku kohta</span><span class="sxs-lookup"><span data-stu-id="54902-103">Set up the parameters of an ER format per legal entity</span></span>

[!include[banner](../includes/banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="54902-104">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="54902-104">Prerequisites</span></span>

<span data-ttu-id="54902-105">Nende etappide läbimiseks peate kõigepealt läbima etapid teemas [ER-vormingute konfigureerimine juriidilise isiku kohta määratud parameetrite kasutamiseks](er-app-specific-parameters-configure-format.md).</span><span class="sxs-lookup"><span data-stu-id="54902-105">To complete these steps, you must first complete the steps in the [Configure ER formats to use parameters that are specified per legal entity](er-app-specific-parameters-configure-format.md) topic.</span></span>

<span data-ttu-id="54902-106">Selles teemas toodud näidete läbimiseks peab teil olema juurdepääs rakendusele Microsoft Dynamics 365 Finance (Finance) ühega järgmistest rollidest.</span><span class="sxs-lookup"><span data-stu-id="54902-106">To complete the examples in this topic, you must have access to Microsoft Dynamics 365 Finance (Finance) for one of the following roles:</span></span>

- <span data-ttu-id="54902-107">Elektroonilise aruandluse arendaja</span><span class="sxs-lookup"><span data-stu-id="54902-107">Electronic reporting developer</span></span>
- <span data-ttu-id="54902-108">Elektroonilise aruandluse funktsionaalne konsultant</span><span class="sxs-lookup"><span data-stu-id="54902-108">Electronic reporting functional consultant</span></span>
- <span data-ttu-id="54902-109">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="54902-109">System administrator</span></span>

## <a name="import-er-configurations"></a><span data-ttu-id="54902-110">Elektroonilise aruandluse konfiguratsioonide importimine</span><span class="sxs-lookup"><span data-stu-id="54902-110">Import ER configurations</span></span>

1.  <span data-ttu-id="54902-111">Logige oma keskkonda sisse.</span><span class="sxs-lookup"><span data-stu-id="54902-111">Sign in to your environment.</span></span>
2.  <span data-ttu-id="54902-112">Valige vaikimisi armatuurlaual **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="54902-112">On the default dashboard, select **Electronic reporting**.</span></span>
3.  <span data-ttu-id="54902-113">Valige **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="54902-113">Select **Reporting configurations**.</span></span>
4.  <span data-ttu-id="54902-114">Importige Finance’i praegusesse eksemplari konfiguratsioonid, mille eksportisite teenusest Regulatory Configuration Services (RCS), läbides etappe teemas [ER-vormingute konfigureerimine juriidilise isiku kohta määratud parameetrite kasutamiseks](er-app-specific-parameters-configure-format.md).</span><span class="sxs-lookup"><span data-stu-id="54902-114">Import, into the current instance of Finance, the configurations that you exported from Regulatory Configuration Services (RCS) while you were completing the steps in the [Configure ER formats to use parameters that are specified per legal entity](er-app-specific-parameters-configure-format.md) topic.</span></span> <span data-ttu-id="54902-115">Järgige neid etappe iga elektroonilise aruandluse (ER) konfiguratsiooni jaoks järgmises järjekorras: andmemudel, mudeli vastendamine ja vormingud.</span><span class="sxs-lookup"><span data-stu-id="54902-115">Follow these steps for each Electronic reporting (ER) configuration, in the following order: data model, model mapping, and formats.</span></span>

    1. <span data-ttu-id="54902-116">Valige suvandid **Vahetus \> Laadi XML-failist**.</span><span class="sxs-lookup"><span data-stu-id="54902-116">Select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="54902-117">Valige käsk **Sirvi**, et valida nõutava ER-i konfiguratsiooni jaoks XML-vormingus fail.</span><span class="sxs-lookup"><span data-stu-id="54902-117">Select **Browse** to select the file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="54902-118">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="54902-118">Select **OK**.</span></span>
    
    <span data-ttu-id="54902-119">Järgmisel joonisel on näha konfiguratsioonid, mis teil lõpetades olema peavad.</span><span class="sxs-lookup"><span data-stu-id="54902-119">The following illustration shows the configurations that you must have when you've finished.</span></span>

    ![ER-seadete leht](./media/GER-AppSpecParms-ImportedConfigurations.PNG)

## <a name="set-up-parameters-for-the-demf-company"></a><span data-ttu-id="54902-121">DEMF-i ettevõtte parameetrite seadistamine</span><span class="sxs-lookup"><span data-stu-id="54902-121">Set up parameters for the DEMF company</span></span>

<span data-ttu-id="54902-122">Saate kasutada ER-raamistikku rakendusekohaste parameetrite seadistamiseks ER-vormingu jaoks.</span><span class="sxs-lookup"><span data-stu-id="54902-122">You can use the ER framework to set up application-specific parameters for an ER format.</span></span>

1.  <span data-ttu-id="54902-123">Valige juriidiline isik **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="54902-123">Select the **DEMF** legal entity.</span></span>
2.  <span data-ttu-id="54902-124">Valige konfiguratsioonipuust vorming **Vorming LE-andmete otsingu õppimiseks**.</span><span class="sxs-lookup"><span data-stu-id="54902-124">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
3.  <span data-ttu-id="54902-125">Tehke tegumiriba vahekaardil **Konfiguratsioonid** grupis **Rakendusekohased parameetrid** valik **Seadistus**.</span><span class="sxs-lookup"><span data-stu-id="54902-125">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>

    ![ER-rakendusekohaste parameetrite leht](./media/GER-AppSpecParms-LookupForm.PNG)
    
    <span data-ttu-id="54902-127">Lehel **Rakendusekohased parameetrid** saate konfigureerida vormingu **Vorming LE-andmete otsingu õppimiseks** andmeallika **Valija** reeglid.</span><span class="sxs-lookup"><span data-stu-id="54902-127">On the **Application specific parameters** page, you can configure the rules for the **Selector** data source of the **Format to learn how to lookup LE data** format.</span></span>
    
    <span data-ttu-id="54902-128">Kui ER-vormingu alus sisaldab mitut tüübi **Otsing** andmeallikat, peate valima sobiva andmeallika kiirkaardilt **Otsingud**, enne kui saate alustada andmeallika reeglite konfigureerimist.</span><span class="sxs-lookup"><span data-stu-id="54902-128">If the base ER format will contain several data sources of the **Lookup** type, you must select the desired data source on the **Lookups** FastTab before you can start to configure the set of rules for the data source.</span></span>
    
    <span data-ttu-id="54902-129">Iga andmeallika jaoks saate konfigureerida eraldi reeglid valitud ER-vormingu iga versiooni kohta.</span><span class="sxs-lookup"><span data-stu-id="54902-129">For each data source, you can configure separate rules for each version of the selected ER format.</span></span>
    
    <span data-ttu-id="54902-130">ER-vormingu valitud versioonis saadaolevate kõikide otsingu andmeallikate kogu reeglite kogum moodustab ER-vormingu rakendusekohased parameetrid.</span><span class="sxs-lookup"><span data-stu-id="54902-130">The whole set of rules for all lookup data sources that are available in the selected version of the base ER format makes up the application-specific parameters for the ER format.</span></span>

4.  <span data-ttu-id="54902-131">Valige ER-vormingu versioon **1.1.1**.</span><span class="sxs-lookup"><span data-stu-id="54902-131">Select version **1.1.1** of the ER format.</span></span>
5.  <span data-ttu-id="54902-132">Valige kiirkaardil **Tingimused** käsk **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="54902-132">On the **Conditions** FastTab, select **Add**.</span></span>
6.  <span data-ttu-id="54902-133">Uue kirje väljal **Kood** otsingu avamiseks valige ripploendi nool.</span><span class="sxs-lookup"><span data-stu-id="54902-133">In the **Code** field of the new record, select the drop-down arrow to open the lookup.</span></span>

    <span data-ttu-id="54902-134">Otsing kujutab valimiseks saadaolevate maksukoodide loendit.</span><span class="sxs-lookup"><span data-stu-id="54902-134">The lookup presents the list of tax codes for selection.</span></span> <span data-ttu-id="54902-135">See loend tagastatakse andmeallikaga **Model.Data.Tax**, mis on konfigureeritud ER-vormingu aluses.</span><span class="sxs-lookup"><span data-stu-id="54902-135">This list is returned by the **Model.Data.Tax** data source that has been configured in the base ER format.</span></span> <span data-ttu-id="54902-136">Kuna see andmeallikas sisaldab välja **Nimi**, kuvatakse otsingus iga maksukoodi nimi.</span><span class="sxs-lookup"><span data-stu-id="54902-136">Because this data source contains the **Name** field, the name of each tax code appears in the lookup.</span></span>

    ![ER-rakendusekohaste parameetrite leht](./media/GER-AppSpecParms-LookupForm-CodeFldPicker.PNG)
    
7.  <span data-ttu-id="54902-138">Valige maksukood **VAT19**.</span><span class="sxs-lookup"><span data-stu-id="54902-138">Select the **VAT19** tax code.</span></span>
8.  <span data-ttu-id="54902-139">Uue kirje väljal **Otsingu tulemus** otsingu avamiseks valige ripploendi nool.</span><span class="sxs-lookup"><span data-stu-id="54902-139">In the **Lookup result** field of the new record, select the drop-down arrow to open the lookup.</span></span> <span data-ttu-id="54902-140">Otsing kujutab vormingu loetelu TaxationLevel valimiseks saadaolevate väärtuste loendit.</span><span class="sxs-lookup"><span data-stu-id="54902-140">The lookup presents the list of values for the TaxationLevel format enumeration for selection.</span></span>

    <span data-ttu-id="54902-141">Pange tähele, et kui sisse logitud kasutaja eelistatud keeleks on valitud saksa keel, kuvatakse otsingu väärtuste sildid saksa keeles, eeldusel, et need on ER-vormingu aluses tõlgitud.</span><span class="sxs-lookup"><span data-stu-id="54902-141">Note that, if German is selected as the preferred language of the user that you're signed in as, the labels of the values in the lookup will be in German, provided that they have been translated in the base ER format.</span></span> <span data-ttu-id="54902-142">Kui otsingu andmeallika silt on tõlgitud, kuvatakse see silt kasutaja eelistatud keeles vahekaardil **Otsingud**.</span><span class="sxs-lookup"><span data-stu-id="54902-142">Additionally, if the label of a lookup data source has been translated, that label will appear in the user's preferred language on the **Lookups** tab.</span></span>

    ![ER-rakendusekohaste parameetrite leht](./media/GER-AppSpecParms-LookupForm-LookupFldPicker.PNG)

9.  <span data-ttu-id="54902-144">Valige väärtus **Tavaline maksustamine**.</span><span class="sxs-lookup"><span data-stu-id="54902-144">Select the **Regular taxation** value.</span></span>

    <span data-ttu-id="54902-145">Selle kirje lisades saate määratleda järgmise reegli: alati kui vajalik on otsingu andmeallikas **Valija** ja maksukood **VAT19** edastatakse argumendina, tagastatakse nõutud maksustamistasemena tase **Tavaline maksustamine**.</span><span class="sxs-lookup"><span data-stu-id="54902-145">By adding this record, you define the following rule: Whenever the **Selector** lookup data source is requested, and the **VAT19** tax code is passed as an argument, **Regular taxation** will be returned as the requested taxation level.</span></span>

10. <span data-ttu-id="54902-146">Valige käsk **Lisa** ja tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="54902-146">Select **Add**, and then follow these steps:</span></span>

    1. <span data-ttu-id="54902-147">Valige väljalt **Kood** maksukood **InVAT19**.</span><span class="sxs-lookup"><span data-stu-id="54902-147">In the **Code** field, select the **InVAT19** tax code.</span></span>
    2. <span data-ttu-id="54902-148">Valige väljalt **Otsingu tulemus** väärtus **Tavaline maksustamine**.</span><span class="sxs-lookup"><span data-stu-id="54902-148">In the **Lookup result** field, select the **Regular taxation** value.</span></span>
    
11. <span data-ttu-id="54902-149">Valige uuesti käsk **Lisa** ja tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="54902-149">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="54902-150">Valige väljalt **Kood** maksukood **VAT7**.</span><span class="sxs-lookup"><span data-stu-id="54902-150">In the **Code** field, select the **VAT7** tax code.</span></span>
    2. <span data-ttu-id="54902-151">Valige väljalt **Otsingu tulemus** väärtus **Vähendatud maksustamine**.</span><span class="sxs-lookup"><span data-stu-id="54902-151">In the **Lookup result** field, select the **Reduced taxation** value.</span></span>
    
12. <span data-ttu-id="54902-152">Valige uuesti käsk **Lisa** ja tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="54902-152">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="54902-153">Valige väljalt **Kood** maksukood **InVAT7**.</span><span class="sxs-lookup"><span data-stu-id="54902-153">In the **Code** field, select the **InVAT7** tax code.</span></span>
    2. <span data-ttu-id="54902-154">Valige väljalt **Otsingu tulemus** väärtus **Vähendatud maksustamine**.</span><span class="sxs-lookup"><span data-stu-id="54902-154">In the **Lookup result** field, select the **Reduced taxation** value.</span></span>
    
13. <span data-ttu-id="54902-155">Valige uuesti käsk **Lisa** ja tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="54902-155">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="54902-156">Valige väljalt **Kood** maksukood **THIRD**.</span><span class="sxs-lookup"><span data-stu-id="54902-156">In the **Code** field, select the **THIRD** tax code.</span></span>
    2. <span data-ttu-id="54902-157">Valige väljalt **Otsingu tulemus** väärtus **Maksustamine puudub**.</span><span class="sxs-lookup"><span data-stu-id="54902-157">In the **Lookup result** field, select the **No taxation** value.</span></span>
    
14. <span data-ttu-id="54902-158">Valige uuesti käsk **Lisa** ja tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="54902-158">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="54902-159">Valige väljalt **Kood** maksukood **InVAT0**.</span><span class="sxs-lookup"><span data-stu-id="54902-159">In the **Code** field, select the **InVAT0** tax code.</span></span>
    2. <span data-ttu-id="54902-160">Valige väljalt **Otsingu tulemus** väärtus **Maksustamine puudub**.</span><span class="sxs-lookup"><span data-stu-id="54902-160">In the **Lookup result** field, select the **No taxation** value.</span></span>
    
15. <span data-ttu-id="54902-161">Valige uuesti käsk **Lisa** ja tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="54902-161">Select **Add** again, and then follow these steps:</span></span>

    1. <span data-ttu-id="54902-162">Valige väljalt **Kood** suvand **\*Mitte tühi\***.</span><span class="sxs-lookup"><span data-stu-id="54902-162">In the **Code** field, select the **\*Not blank\*** option.</span></span>
    2. <span data-ttu-id="54902-163">Valige väljalt **Otsingu tulemus** väärtus **Muu**.</span><span class="sxs-lookup"><span data-stu-id="54902-163">In the **Lookup result** field, select the **Other** value.</span></span>
    
    <span data-ttu-id="54902-164">Selle viimase kirje lisades saate määratleda järgmise reegli: alati kui argumendina edastatud maksukood ei täida mõnda eeltoodud tingimustest, tagastab otsingu andmeallikas nõutud maksustamistasemena taseme **Muu**.</span><span class="sxs-lookup"><span data-stu-id="54902-164">By adding this last record, you define the following rule: Whenever the tax code that is passed as an argument doesn't satisfy any of the previous rules, the lookup data source will return **Other** as the requested taxation level.</span></span>

    ![ER-rakendusekohaste parameetrite leht](./media/GER-AppSpecParms-LookupForm-RulesSet.PNG)
    
16. <span data-ttu-id="54902-166">Valige väljalt **Olek** suvand **Lõpule viidud**.</span><span class="sxs-lookup"><span data-stu-id="54902-166">In the **State** field, select **Completed**.</span></span>

    <span data-ttu-id="54902-167">Kui käitate ER-vormingu versiooni, mille olek on **Lõpule viidud** või **Jagatud**, peab see reeglite kogum olema olekus **Lõpule viidud**.</span><span class="sxs-lookup"><span data-stu-id="54902-167">When you run an ER format version that has a status of either **Completed** or **Shared**, this set of rules must be in the **Completed** state.</span></span> <span data-ttu-id="54902-168">Muidu katkestatakse ER-vormingu aluse käivitamine, kui vorming üritab laadida andmeid sellest reeglite kogumist, kui käitatakse otsingu andmeallikat **Valija**.</span><span class="sxs-lookup"><span data-stu-id="54902-168">Otherwise, execution of the base ER format will be interrupted when the format tries to load data from this set of rules while the **Selector** lookup data source is being run.</span></span>
    
    <span data-ttu-id="54902-169">Kui käitate ER-vormingu versiooni, mille olek on **Mustand**, pääseb ER-vormingu alus sellele reeglite kogumile ligi, olenemata selle olekust.</span><span class="sxs-lookup"><span data-stu-id="54902-169">When you run an ER format version that has a status of **Draft**, the base ER format can access this set of rules, regardless of its state.</span></span>
    
17. <span data-ttu-id="54902-170">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="54902-170">Select **Save**.</span></span>
18. <span data-ttu-id="54902-171">Sulgege leht **Rakendusekohased parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="54902-171">Close the **Application specific parameters** page.</span></span>

## <a name="run-the-er-format-in-the-demf-company"></a><span data-ttu-id="54902-172">ER-vormingu käitamine DEMF-i ettevõttes</span><span class="sxs-lookup"><span data-stu-id="54902-172">Run the ER format in the DEMF company</span></span>

1.  <span data-ttu-id="54902-173">Valige konfiguratsioonipuust vorming **Vorming LE-andmete otsingu õppimiseks**.</span><span class="sxs-lookup"><span data-stu-id="54902-173">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
2.  <span data-ttu-id="54902-174">Valige toimingupaanil käsk **Käivita**.</span><span class="sxs-lookup"><span data-stu-id="54902-174">On the Action Pane, select **Run**.</span></span>
3.  <span data-ttu-id="54902-175">Kuvatavas dialoogiboksis tehke valik **OK**.</span><span class="sxs-lookup"><span data-stu-id="54902-175">In the dialog box that appears, select **OK**.</span></span>
4.  <span data-ttu-id="54902-176">Laadige alla loodud aruanne ja salvestage see lokaalselt.</span><span class="sxs-lookup"><span data-stu-id="54902-176">Download the statement that is generated and store it locally.</span></span>

    <span data-ttu-id="54902-177">Pange tähele, et loodud aruandes on maksukoodi **InVAT7** kokkuvõte pandud tasemele **Vähendatud** ning maksukoodide **VAT19** ja **InVA19** kokkuvõtted on pandud tasemele **Tavaline**.</span><span class="sxs-lookup"><span data-stu-id="54902-177">In the generated statement, notice that the summary of the **InVAT7** tax code has been put on the **Reduced** level, and the summaries of the **VAT19** and **InVA19** tax codes have been put on the **Regular** level.</span></span> <span data-ttu-id="54902-178">Selle käitumise määrab juriidilisest isikust oleneva reeglite kogumi konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="54902-178">This behavior is determined by the configuration in the legal entity–dependent set of rules.</span></span>
    
5.  <span data-ttu-id="54902-179">Valige suvandid **Maks \> Kaudsed maksud \> Käibemaks \> Käibemaksukoodid**.</span><span class="sxs-lookup"><span data-stu-id="54902-179">Go to **Tax \> Indirect taxes \> Sales tax \> Sales tax codes**.</span></span>
6.  <span data-ttu-id="54902-180">Valige maksukood **InVAT17**.</span><span class="sxs-lookup"><span data-stu-id="54902-180">Select the **InVAT7** tax code.</span></span>
7.  <span data-ttu-id="54902-181">Valige toimingupaani vahekaardilt **Käibemaksu kood** grupis **Päringud** suvand **Sisestatud käibemaks**, et vaadata maksuväärtuse ja kohaldatava maksumäära teavet maksukoodi kohta.</span><span class="sxs-lookup"><span data-stu-id="54902-181">On the Action Pane, on the **Sales tax code** tab, in the **Inquiries** group, select **Posted sales tax** to view information about the tax value and applied tax rate per tax code.</span></span>

    ![Sisestatud käibemaksu leht](./media/GER-AppSpecParms-Statement.PNG)

8.  <span data-ttu-id="54902-183">Sulgege sisestatud käibemaksu leht.</span><span class="sxs-lookup"><span data-stu-id="54902-183">Close the Posted sales tax page.</span></span>

## <a name="set-up-parameters-for-the-usmf-company"></a><span data-ttu-id="54902-184">USMF-i ettevõtte parameetrite seadistamine</span><span class="sxs-lookup"><span data-stu-id="54902-184">Set up parameters for the USMF company</span></span>

1.  <span data-ttu-id="54902-185">Valige juriidiline isik **USMF**.</span><span class="sxs-lookup"><span data-stu-id="54902-185">Select the **USMF** legal entity.</span></span>
2.  <span data-ttu-id="54902-186">Minge jaotisse **Organisatsiooni haldamine \> Elektrooniline aruandlus \> Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="54902-186">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3.  <span data-ttu-id="54902-187">Laiendage konfiguratsioonipuus üksust **Mudel parameetritega kõnede õppimiseks**, laiendage üksust **Vorming parameetritega kõnede õppimiseks** ja valige vorming **Vorming LE-andmete otsingu õppimiseks**.</span><span class="sxs-lookup"><span data-stu-id="54902-187">In the configurations tree, expand the **Model to learn parameterized calls** item, expand the **Format to learn parameterized calls** item, and select the **Format to learn how to lookup LE data** format.</span></span>
4.  <span data-ttu-id="54902-188">Tehke tegumiriba vahekaardil **Konfiguratsioonid** grupis **Rakendusekohased parameetrid** valik **Seadistus**.</span><span class="sxs-lookup"><span data-stu-id="54902-188">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>
5.  <span data-ttu-id="54902-189">Valige valitud ER-vormingu versioon **1.1.1**.</span><span class="sxs-lookup"><span data-stu-id="54902-189">Select version **1.1.1** of the selected ER format.</span></span>
6.  <span data-ttu-id="54902-190">Valige kiirkaardil **Tingimused** käsk **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="54902-190">On the **Conditions** FastTab, select **Add**.</span></span>
7.  <span data-ttu-id="54902-191">Uue kirje väljal **Kood** otsingu avamiseks valige ripploendi nool.</span><span class="sxs-lookup"><span data-stu-id="54902-191">In the **Code** field of the new record, select the drop-down arrow to open the lookup.</span></span>

    <span data-ttu-id="54902-192">Otsing kujutab nüüd maksukoodide loendit ettevõtte **USMF** valitava maksu kohta.</span><span class="sxs-lookup"><span data-stu-id="54902-192">The lookup now presents the list of tax codes for the **USMF** company tax for selection.</span></span>

    ![ER-rakendusekohaste parameetrite leht](./media/GER-AppSpecParms-LookupForm-CodeFldPicker2.PNG)
    
8.  <span data-ttu-id="54902-194">Valige maksukood **EXEMPT**.</span><span class="sxs-lookup"><span data-stu-id="54902-194">Select the **EXEMPT** tax code.</span></span>
9.  <span data-ttu-id="54902-195">Valige uue kirje väljalt **Otsingu tulemus** väärtus **Maksustamine puudub**.</span><span class="sxs-lookup"><span data-stu-id="54902-195">In the **Lookup resul** t field of the new record, select the **No taxation** value.</span></span>
10. <span data-ttu-id="54902-196">Valige uuesti käsk **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="54902-196">Select **Add** again.</span></span>
11. <span data-ttu-id="54902-197">Valige uue kirje väljalt **Kood** suvand **\*Mitte tühi\***.</span><span class="sxs-lookup"><span data-stu-id="54902-197">In the **Code** field of the new record, select the **\*Not blank\*** option.</span></span>
12. <span data-ttu-id="54902-198">Valige uue kirje väljalt **Otsingu tulemus** väärtus **Tavaline maksustamine**.</span><span class="sxs-lookup"><span data-stu-id="54902-198">In the **Lookup result** field of the new record, select the **Regular taxation** value.</span></span>
13. <span data-ttu-id="54902-199">Valige väljalt **Olek** suvand **Lõpule viidud**.</span><span class="sxs-lookup"><span data-stu-id="54902-199">In the **State** field, select **Completed**.</span></span>
14. <span data-ttu-id="54902-200">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="54902-200">Select **Save**.</span></span>

    ![ER-rakendusekohaste parameetrite leht](./media/GER-AppSpecParms-LookupForm-RulesSet2.PNG)
    
15. <span data-ttu-id="54902-202">Sulgege leht **Rakendusekohased parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="54902-202">Close the **Application specific parameters** page.</span></span>

## <a name="run-the-er-format-in-the-usmf-company"></a><span data-ttu-id="54902-203">ER-vormingu käitamine USMF-i ettevõttes</span><span class="sxs-lookup"><span data-stu-id="54902-203">Run the ER format in the USMF company</span></span>

1.  <span data-ttu-id="54902-204">Valige konfiguratsioonipuust vorming **Vorming LE-andmete otsingu õppimiseks**.</span><span class="sxs-lookup"><span data-stu-id="54902-204">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
2.  <span data-ttu-id="54902-205">Valige toimingupaanil käsk **Käivita**.</span><span class="sxs-lookup"><span data-stu-id="54902-205">On the Action Pane, select **Run**.</span></span>
3.  <span data-ttu-id="54902-206">Kuvatavas dialoogiboksis tehke valik **OK**.</span><span class="sxs-lookup"><span data-stu-id="54902-206">In the dialog box that appears, select **OK**.</span></span>
4.  <span data-ttu-id="54902-207">Laadige alla loodud aruanne ja salvestage see lokaalselt.</span><span class="sxs-lookup"><span data-stu-id="54902-207">Download the statement that is generated and store it locally.</span></span>

    <span data-ttu-id="54902-208">Pange tähele, et loodud aruandes olete nüüd uuesti kasutanud sama ER-vormingut teise juriidilise isiku jaoks, aga ER-vormingut korrigeerimata.</span><span class="sxs-lookup"><span data-stu-id="54902-208">In the generated statement, notice that you've now reused the same ER format for a different legal entity, but without making any adjustments to the ER format.</span></span>

## <a name="reuse-legal-entitydependent-parameters"></a><span data-ttu-id="54902-209">Juriidilisest isikust sõltuvate parameetrite uuesti kasutamine</span><span class="sxs-lookup"><span data-stu-id="54902-209">Reuse legal entity–dependent parameters</span></span>

### <a name="export-parameters"></a><span data-ttu-id="54902-210">Ekspordiparameetrid</span><span class="sxs-lookup"><span data-stu-id="54902-210">Export parameters</span></span>

1.  <span data-ttu-id="54902-211">Avage **Organisatsiooni haldamine \> Tööruumid \> Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="54902-211">Go to **Organization administration \> Workspaces \> Electronic reporting**.</span></span>
2.  <span data-ttu-id="54902-212">Valige **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="54902-212">Select **Reporting configurations**.</span></span>
3.  <span data-ttu-id="54902-213">Valige konfiguratsioonipuust vorming **Vorming LE-andmete otsingu õppimiseks**.</span><span class="sxs-lookup"><span data-stu-id="54902-213">In the configurations tree, select the **Format to learn how to lookup LE data** format.</span></span>
4.  <span data-ttu-id="54902-214">Tehke tegumiriba vahekaardil **Konfiguratsioonid** grupis **Rakendusekohased parameetrid** valik **Seadistus**.</span><span class="sxs-lookup"><span data-stu-id="54902-214">On the Action Pane, on the **Configurations** tab, in the **Application specific parameters** group, select **Setup**.</span></span>
5.  <span data-ttu-id="54902-215">Valige ER-vormingu versioon **1.1.1**.</span><span class="sxs-lookup"><span data-stu-id="54902-215">Select version **1.1.1** of the ER format.</span></span>
6.  <span data-ttu-id="54902-216">Valige toimingupaanil käsk **Ekspordi**.</span><span class="sxs-lookup"><span data-stu-id="54902-216">On the Action Pane, select **Export**.</span></span>
7.  <span data-ttu-id="54902-217">Laadige alla loodud fail ja salvestage see lokaalselt.</span><span class="sxs-lookup"><span data-stu-id="54902-217">Download the file that is generated and store it locally.</span></span>

    <span data-ttu-id="54902-218">Konfigureeritud rakendusekohaste parameetrite kogum on nüüd eksporditud XML-failina.</span><span class="sxs-lookup"><span data-stu-id="54902-218">The configured set of application-specific parameters has now been exported as an XML file.</span></span>

### <a name="import-parameters"></a><span data-ttu-id="54902-219">Parameetrite importimine</span><span class="sxs-lookup"><span data-stu-id="54902-219">Import parameters</span></span>

1.  <span data-ttu-id="54902-220">Valige ER-vormingu versioon **1.1.2**.</span><span class="sxs-lookup"><span data-stu-id="54902-220">Select version **1.1.2** of the ER format.</span></span>
2.  <span data-ttu-id="54902-221">Toimingupaanil valige **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="54902-221">On the Action Pane, select **Import**.</span></span>
3.  <span data-ttu-id="54902-222">Valige suvand **Jah** kinnitamaks, et soovite vormingu selle versiooni jaoks üle kirjutada olemasolevad rakendusekohased parameetrid.</span><span class="sxs-lookup"><span data-stu-id="54902-222">Select **Yes** to confirm that you want to override the existing application-specific parameters for this format version.</span></span>
4.  <span data-ttu-id="54902-223">Valige suvand **Sirvi**, et leida versiooni **1.1.1** jaoks eksporditud rakendusekohaseid parameetreid sisaldav fail.</span><span class="sxs-lookup"><span data-stu-id="54902-223">Select **Browse** to find the file that contains the exported application-specific parameters for version **1.1.1**.</span></span>
5.  <span data-ttu-id="54902-224">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="54902-224">Select **OK**.</span></span>

    <span data-ttu-id="54902-225">ER-vormingu versioonil **1.1.2** on nüüd samad rakendusekohased parameetrid kui algselt versiooni **1.1.1** jaoks konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="54902-225">Version **1.1.2** of the ER format now has the same application-specific parameters that you originally configured for version **1.1.1**.</span></span>
    
    <span data-ttu-id="54902-226">Pange tähele, et ER-vormingu rakendusekohased parameetrid sõltuvad juriidilisest isikust.</span><span class="sxs-lookup"><span data-stu-id="54902-226">Note that the application-specific parameters of an ER format are legal entity–dependent.</span></span> <span data-ttu-id="54902-227">Ühe juriidilise isiku jaoks konfigureeritud rakendusekohaste parameetrite uuesti kasutamiseks teises juriidilises isikus peate need eksportima, kui olete sisse logitud esimesse juriidilisse isikusse, ja seejärel importima pärast sisselogimist teise juriidilisse isikusse.</span><span class="sxs-lookup"><span data-stu-id="54902-227">To reuse the application-specific parameters that were configured for one legal entity in a different legal entity, you must export them while you're signed in to the first legal entity and then import them after you sign in to the other legal entity.</span></span>

    <span data-ttu-id="54902-228">Võite seda lähenemist kasutada ka algselt ühes Finance’i eksemplaris konfigureeritud ER-vorminguga seotud rakendusekohaste parameetrite edastamiseks teise Finance’i eksemplari.</span><span class="sxs-lookup"><span data-stu-id="54902-228">You can also use this approach to transfer an ER format related application-specific parameters that were originally configured in one instance of Finance to another instance of Finance.</span></span>

    <span data-ttu-id="54902-229">Pange tähele, et kui konfigureerite rakendusekohaseid parameetreid ühe ER-vormingu versiooni jaoks ja impordite sama vormingu uuema versiooni praegusesse Finance’i eksemplari, ei rakendata olemasolevaid rakendusekohaseid parameetreid imporditud versioonile.</span><span class="sxs-lookup"><span data-stu-id="54902-229">Be aware that if you configure application-specific parameters for one version of an ER format and import a higher version of the same format into the current Finance instance, the existing application-specific parameters won't be applied for the imported version.</span></span>
    
    <span data-ttu-id="54902-230">Pidage ka meeles, et kui valite importimiseks faili, võrreldakse selle faili rakendusekohaseid parameetreid importimiseks valitud ER-vormingu tüübi **Otsing** vastava andmeallika struktuuriga.</span><span class="sxs-lookup"><span data-stu-id="54902-230">Also be aware that, when you select a file for import, the structure of the application-specific parameters in that file is compared with the structure of the corresponding data source of the **Lookup** type in the ER format that is selected for import.</span></span> <span data-ttu-id="54902-231">Importimine toimub siis, kui iga rakendusekohase parameetri struktuur vastab importimiseks valitud ER-vormingu vastava andmeallika struktuurile.</span><span class="sxs-lookup"><span data-stu-id="54902-231">The import is done when the structure of each application-specific parameter matches the structure of the corresponding data source in the ER format that is selected for import.</span></span> <span data-ttu-id="54902-232">Kui struktuurid ei kattu, kuvatakse hoiatusteade, et importimist ei toimu.</span><span class="sxs-lookup"><span data-stu-id="54902-232">If the structures don't match, you receive a warning message that states that the import can't be done.</span></span> <span data-ttu-id="54902-233">Kui sunnite importimise, tühistatakse valitud ER-vormingu olemasolevad rakendusekohased parameetrid ja peate need uuesti algusest peale seadistama.</span><span class="sxs-lookup"><span data-stu-id="54902-233">If you force the import to be done, the existing application-specific parameters for the selected ER format will be cleaned up, and you must set them up from the beginning.</span></span>

## <a name="relationship-between-application-specific-parameters-and-an-er-format"></a><span data-ttu-id="54902-234">Rakendusekohaste parameetrite ja ER-vormingu vaheline seos</span><span class="sxs-lookup"><span data-stu-id="54902-234">Relationship between application-specific parameters and an ER format</span></span>

<span data-ttu-id="54902-235">ER-vormingu ja selle rakendusekohaste parameetrite seos saavutatakse ER-vormingu eksemplarist sõltuva kordumatu identimiskoodiga.</span><span class="sxs-lookup"><span data-stu-id="54902-235">The relationship between an ER format and its application-specific parameters is established by the ER format's instance-independent unique identification code.</span></span> <span data-ttu-id="54902-236">Seega kui eemaldate ER-vormingu Finance’ist, säilitatakse ER-vormingu jaoks konfigureeritud rakendusekohaseid parameetreid praeguses Finance’i eksemplaris.</span><span class="sxs-lookup"><span data-stu-id="54902-236">Therefore, when you remove an ER format from Finance, the application-specific parameters that are configured for the ER format are kept in the current instance of Finance.</span></span> <span data-ttu-id="54902-237">Neile pääseb ligi alati, kui ER-vormingu alus sellesse Finance’i eksemplari uuesti imporditakse.</span><span class="sxs-lookup"><span data-stu-id="54902-237">They can be accessed whenever the base ER format is reimported into this instance of Finance.</span></span>

## <a name="access-application-specific-parameters-by-using-the-er-framework"></a><span data-ttu-id="54902-238">Ligipääs rakendusekohastele parameetritele ER-raamistikku kasutades</span><span class="sxs-lookup"><span data-stu-id="54902-238">Access application-specific parameters by using the ER framework</span></span>

<span data-ttu-id="54902-239">Eelnevas näites pääsesite ER-vormingu rakendusekohastele parameetritele ligi ER-raamistikku kasutades.</span><span class="sxs-lookup"><span data-stu-id="54902-239">In the preceding example, you have accessed application-specific parameters of an ER format by using the ER framework.</span></span> <span data-ttu-id="54902-240">See lähenemine ei lase teil piirata juurdepääsu konkreetse ER-vormingu rakendusekohastele parameetritele.</span><span class="sxs-lookup"><span data-stu-id="54902-240">This approach doesn't let you restrict access to the application-specific parameters of a specific ER format.</span></span> <span data-ttu-id="54902-241">Kui peate niisugused piirangut määrama, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="54902-241">If you must apply such restrictions, follow these steps.</span></span> 

1.  <span data-ttu-id="54902-242">Kasutage uuesti olemasolevat menüü-üksust **ERSolutionAppSpecificParametersDesigner** või juurutage oma menüü-üksus **ERSolutionAppSpecificParametersDesigner**.</span><span class="sxs-lookup"><span data-stu-id="54902-242">Either reuse an existing **ERSolutionAppSpecificParametersDesigner** menu item, or implement your own **ERSolutionAppSpecificParametersDesigner** menu item.</span></span>

    ![Visual Studio leht](./media/GER-AppSpecParms-LookupForm-Access1.PNG)
    
2.  <span data-ttu-id="54902-244">Järgige üht neist sammudest.</span><span class="sxs-lookup"><span data-stu-id="54902-244">Follow one of these steps:</span></span>

    1.  <span data-ttu-id="54902-245">Looge uus menüü-üksus nupp ja linkige see vastava kirjega tabelist **ERSolutionTable**, seadistades selle atribuudi **Andmeallikas** väärtusele **ERSolutionTable**.</span><span class="sxs-lookup"><span data-stu-id="54902-245">Create a new menu item button, and link it to the corresponding record from the **ERSolutionTable** table by setting its **Data Source** property to **ERSolutionTable**.</span></span>
    
        ![Visual Studio leht](./media/GER-AppSpecParms-LookupForm-Access2.PNG)
        
    2.  <span data-ttu-id="54902-247">Looge lihtne nupp ja kirjutage üle meetod **Klõpsatud**, nagu on näidatud järgmises näites.</span><span class="sxs-lookup"><span data-stu-id="54902-247">Create a simple button, and override the **Clicked** method as shown in the following example.</span></span>
    
        <span data-ttu-id="54902-248">Seda lähenemist kasutades saate määrata kordumatu lahenduse ID (määratakse väärtuse **GUID** kaudu), et anda ligipääs ainult konkreetse ER-vormingu rakendusekohastele parameetritele ja sellest tuletatud koopiatele.</span><span class="sxs-lookup"><span data-stu-id="54902-248">By using this approach, you can specify a unique solution ID (defined via the **GUID** value) to allow access to the application-specific parameters of only a specific ER format and descendant copies that have been derived from it.</span></span>
        
        ```xpp
        public void clicked()
            {
                super();

                ERSolutionTable solutionTableRecord = ERSolutionTable::findByGUID(str2Guid('ADACCB2F-EFD1-4C90-877D-7E1E5D1AEE92'));

                Args args = new Args();
                args.record(solutionTableRecord);
                args.caller(this);

                new MenuFunction(menuItemDisplayStr(ERSolutionAppSpecificParametersDesigner), MenuItemType::Display)
                    .run(args);
            }
        ```

## <a name="additional-resources"></a><span data-ttu-id="54902-249">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="54902-249">Additional resources</span></span>

[<span data-ttu-id="54902-250">Valemikoostaja elektroonilises aruandluses</span><span class="sxs-lookup"><span data-stu-id="54902-250">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="54902-251">ER-vormingute konfigureerimine juriidilise isiku kohta määratud parameetrite kasutamiseks</span><span class="sxs-lookup"><span data-stu-id="54902-251">Configure ER formats to use parameters that are specified per legal entity</span></span>](er-app-specific-parameters-configure-format.md)
