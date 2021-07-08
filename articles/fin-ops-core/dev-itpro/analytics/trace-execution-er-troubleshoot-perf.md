---
title: Elektroonilise aruandluse vormingute täitmise jälitamine jõudlusprobleemide tõrkeotsingu tegemiseks
description: Selles teemas kirjeldatakse, kuidas kasutada elektroonilises aruandluses (ER) jõudluse jälituse funktsiooni jõudluse probleemide tõrkeotsingu tegemiseks.
author: NickSelin
ms.date: 06/22/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 7fbec962fea374afdbabaad48a42dad380708678
ms.sourcegitcommit: dbffde1944b9d037124415c28053036c9ef1ecb7
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/23/2021
ms.locfileid: "6295569"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a><span data-ttu-id="d481b-103">ER-vormingute täitmise jälitus jõudluse probleemide tõrkeotsinguks</span><span class="sxs-lookup"><span data-stu-id="d481b-103">Trace the execution of ER formats to troubleshoot performance issues</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d481b-104">Üks osa elektroonilise aruandluse (ER) konfiguratsioonide kujundamisest elektrooniliste dokumentide loomise jaoks on määratleda meetod, mida kasutatakse andmete saamiseks rakendusest, ja sisestada see loodud väljundisse.</span><span class="sxs-lookup"><span data-stu-id="d481b-104">As part of the process of designing Electronic reporting (ER) configurations to generate electronic documents, you define the method that is used to get data out of the application and enter it in the output that is generated.</span></span> <span data-ttu-id="d481b-105">ER-i jõudluse jälituse funktsioon aitab märkimisväärselt vähendada aja- ja rahakulu, mis tekib ER-vormingu täitmise üksikasjade kogumisel ja nende kasutamisel jõudluse probleemide tõrkeotsinguks.</span><span class="sxs-lookup"><span data-stu-id="d481b-105">The ER performance trace feature helps significantly reduce the time and cost that are involved in collecting the details of ER format execution and using them to troubleshoot performance issues.</span></span> <span data-ttu-id="d481b-106">Selles õppetükis esitatakse juhised, kuidas jälitada täidetud ER-vormingute jõudlust ja kuidas kasutada jälitusest saadud teavet jõudluse täiustamiseks.</span><span class="sxs-lookup"><span data-stu-id="d481b-106">This tutorial provides guidelines about how to take performance traces for executed ER formats, and how to use the information from these traces to help improve performance.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d481b-107">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="d481b-107">Prerequisites</span></span>

<span data-ttu-id="d481b-108">Selle õppetüki näidete läbimiseks peavad teil olema järgmised juurdepääsuõigused.</span><span class="sxs-lookup"><span data-stu-id="d481b-108">To complete the examples in this tutorial, you must have the following access:</span></span>

- <span data-ttu-id="d481b-109">Juurdepääs ühele järgmistest rollidest.</span><span class="sxs-lookup"><span data-stu-id="d481b-109">Access to one of the following roles:</span></span>

    - <span data-ttu-id="d481b-110">Elektroonilise aruandluse arendaja</span><span class="sxs-lookup"><span data-stu-id="d481b-110">Electronic reporting developer</span></span>
    - <span data-ttu-id="d481b-111">Elektroonilise aruandluse funktsionaalne konsultant</span><span class="sxs-lookup"><span data-stu-id="d481b-111">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="d481b-112">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="d481b-112">System administrator</span></span>

- <span data-ttu-id="d481b-113">Juurdepääs teenuse Regulatory Configuration Services (RCS) eksemplarile, mis on ette valmistatud sama rentniku jaoks, nagu rakendus, ühe järgmise rolli jaoks:</span><span class="sxs-lookup"><span data-stu-id="d481b-113">Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as the application, for one of the following roles:</span></span>

    - <span data-ttu-id="d481b-114">Elektroonilise aruandluse arendaja</span><span class="sxs-lookup"><span data-stu-id="d481b-114">Electronic reporting developer</span></span>
    - <span data-ttu-id="d481b-115">Elektroonilise aruandluse funktsionaalne konsultant</span><span class="sxs-lookup"><span data-stu-id="d481b-115">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="d481b-116">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="d481b-116">System administrator</span></span>

<span data-ttu-id="d481b-117">Samuti peate alla laadima ja kohalikult talletama järgmised failid.</span><span class="sxs-lookup"><span data-stu-id="d481b-117">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="d481b-118">Fail</span><span class="sxs-lookup"><span data-stu-id="d481b-118">File</span></span>                                  | <span data-ttu-id="d481b-119">Sisu</span><span class="sxs-lookup"><span data-stu-id="d481b-119">Content</span></span>                               |
|---------------------------------------|---------------------------------------|
| <span data-ttu-id="d481b-120">Performance trace model.version.1 (Jõudluse jälituse mudel, versioon 1)</span><span class="sxs-lookup"><span data-stu-id="d481b-120">Performance trace model.version.1</span></span>     | [<span data-ttu-id="d481b-121">ER-i andmemudeli konfiguratsiooni näide</span><span class="sxs-lookup"><span data-stu-id="d481b-121">Sample ER data model configuration</span></span>](https://download.microsoft.com/download/0/a/a/0aa84e48-8040-4c46-b542-e3bf15c9b2ad/Performancetracemodelversion.1.xml)    |
| <span data-ttu-id="d481b-122">Performance trace metadata.version.1 (Jõudluse jälituse metaandmed, versioon 1)</span><span class="sxs-lookup"><span data-stu-id="d481b-122">Performance trace metadata.version.1</span></span>  | [<span data-ttu-id="d481b-123">ER-i metaandmete konfiguratsiooni näide</span><span class="sxs-lookup"><span data-stu-id="d481b-123">Sample ER metadata configuration</span></span>](https://download.microsoft.com/download/a/9/3/a937e8c4-1f8a-43e4-83ee-7d599cf7d983/Performancetracemetadataversion.1.xml)      |
| <span data-ttu-id="d481b-124">Performance trace mapping.version.1.1 (Jõudluse jälituse vastendus, versioon 1.1)</span><span class="sxs-lookup"><span data-stu-id="d481b-124">Performance trace mapping.version.1.1</span></span> | [<span data-ttu-id="d481b-125">ER-i mudelivastenduse konfiguratsiooni näide</span><span class="sxs-lookup"><span data-stu-id="d481b-125">Sample ER model mapping configuration</span></span>](https://download.microsoft.com/download/7/7/3/77379bdc-7b22-4cfc-9b64-a9147599f931/Performancetracemappingversion1.1.xml) |
| <span data-ttu-id="d481b-126">Performance trace format.version.1.1 (Jõudluse jälituse vorming, versioon 1.1)</span><span class="sxs-lookup"><span data-stu-id="d481b-126">Performance trace format.version.1.1</span></span>  | [<span data-ttu-id="d481b-127">ER-vormingu konfiguratsiooni näide</span><span class="sxs-lookup"><span data-stu-id="d481b-127">Sample ER format configuration</span></span>](https://download.microsoft.com/download/8/6/8/868ba581-5a06-459e-b173-fb00f038b37f/Performancetraceformatversion1.1.xml)       |

### <a name="configure-er-parameters"></a><span data-ttu-id="d481b-128">Elektroonilise aruandluse parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="d481b-128">Configure ER parameters</span></span>

<span data-ttu-id="d481b-129">Iga ER-i jõudluse jälg, mis luuakse rakenduses, salvestatakse käivituslogi kirje manusena.</span><span class="sxs-lookup"><span data-stu-id="d481b-129">Each ER performance trace that is generated in the application is stored as an attachment of the execution log record.</span></span> <span data-ttu-id="d481b-130">Nende manuste haldamiseks kasutatakse dokumendihalduse raamistikku.</span><span class="sxs-lookup"><span data-stu-id="d481b-130">The Document management (DM) framework is used to manage these attachments.</span></span> <span data-ttu-id="d481b-131">Peate konfigureerima ER-i parameetreid varem, et määrata dokumendihalduse dokumendi tüüp, mida tuleks kasutada jõudluse jälgede manustamiseks.</span><span class="sxs-lookup"><span data-stu-id="d481b-131">You must configure ER parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="d481b-132">Tööruumis **Elektrooniline aruandlus** valige **Elektroonilise aruandluse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="d481b-132">In the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="d481b-133">Seejärel valige lehe **Elektroonilise aruandluse parameetrid** vahekaardi **Manused** väljal **Muud** dokumendihalduse dokumendi tüüp, mida tuleks kasutada jõudluse jälitusteks.</span><span class="sxs-lookup"><span data-stu-id="d481b-133">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![Elektroonilise aruandluse parameetrite leht](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

<span data-ttu-id="d481b-135">Selleks, et dokumendihalduse dokumenditüüp oleks otsinguväljal **Muud** saadaval, peab dokumendihalduse dokumenditüüp olema lehel **Dokumenditüübid** konfigureeritud järgmisel viisil (**Organisatsiooni haldus \> Dokumendihaldus \> Dokumenditüübid**).</span><span class="sxs-lookup"><span data-stu-id="d481b-135">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="d481b-136">**Klass:** manusfail</span><span class="sxs-lookup"><span data-stu-id="d481b-136">**Class:** Attach file</span></span>
- <span data-ttu-id="d481b-137">**Grupp:** fail</span><span class="sxs-lookup"><span data-stu-id="d481b-137">**Group:** File</span></span>

![Dokumenditüüpide leht](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> <span data-ttu-id="d481b-139">Valitud dokumenditüüp peab olema eksemplari igas ettevõttes saadaval, kuna dokumendihalduse manused on ettevõttekohased.</span><span class="sxs-lookup"><span data-stu-id="d481b-139">The selected document type must be available in every company of the current instance, because DM attachments are company-specific.</span></span>

### <a name="configure-rcs-parameters"></a><span data-ttu-id="d481b-140">RCS-i parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="d481b-140">Configure RCS parameters</span></span>

<span data-ttu-id="d481b-141">Loodud ER-i jõudluse jäled imporditakse analüüsimiseks RCS-i, kasutades ER-vormingu kujundajat ja ER-i mudelivastenduse kujundajat.</span><span class="sxs-lookup"><span data-stu-id="d481b-141">ER performance traces that are generated will be imported into RCS for analysis by using the ER format designer and the ER mapping designer.</span></span> <span data-ttu-id="d481b-142">Kuna ER-i jõudluse jäljed salvestatakse ER-vorminguga seotud käivituslogi kirje manustena, peate konfigureerima RCS-i parameetreid ette, et määrata dokumendihalduse dokumenditüüp, mida tuleks kasutada jõudluse jälje manustamiseks.</span><span class="sxs-lookup"><span data-stu-id="d481b-142">Because ER performance traces are stored as attachments of the execution log record that is related to the ER format, you must configure RCS parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="d481b-143">Valige RCS-i eksemplari, mis on teie ettevõtte jaoks ette valmistatud, tööruumis **Elektrooniline aruandlus** suvand **Elektroonilise aruandluse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="d481b-143">In the instance of RCS that has been provisioned for your company, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="d481b-144">Seejärel valige lehe **Elektroonilise aruandluse parameetrid** vahekaardi **Manused** väljal **Muud** dokumendihalduse dokumendi tüüp, mida tuleks kasutada jõudluse jälitusteks.</span><span class="sxs-lookup"><span data-stu-id="d481b-144">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![Elektroonilise aruandluse parameetrite leht RCS-is](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

<span data-ttu-id="d481b-146">Selleks, et dokumendihalduse dokumenditüüp oleks otsinguväljal **Muud** saadaval, peab dokumendihalduse dokumenditüüp olema lehel **Dokumenditüübid** konfigureeritud järgmisel viisil (**Organisatsiooni haldus \> Dokumendihaldus \> Dokumenditüübid**).</span><span class="sxs-lookup"><span data-stu-id="d481b-146">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="d481b-147">**Klass:** manusfail</span><span class="sxs-lookup"><span data-stu-id="d481b-147">**Class:** Attach file</span></span>
- <span data-ttu-id="d481b-148">**Grupp:** fail</span><span class="sxs-lookup"><span data-stu-id="d481b-148">**Group:** File</span></span>

## <a name="design-an-er-solution"></a><span data-ttu-id="d481b-149">ER-i lahenduse kujundamine</span><span class="sxs-lookup"><span data-stu-id="d481b-149">Design an ER solution</span></span>

<span data-ttu-id="d481b-150">Oletame, et olete alustanud uue ER-i lahenduse kujundamist, et luua uus hankija kandeid esitav aruanne.</span><span class="sxs-lookup"><span data-stu-id="d481b-150">Assume that you've started to design a new ER solution to generate a new report that presents vendor transactions.</span></span> <span data-ttu-id="d481b-151">Praegu leiate valitud hankija kanded lehel **Hankija kanded** (avage **Ostureskontro \> Hankijad \> Kõik hankijad**, valige hankija ja seejärel valige toimingupaanil vahekaardi **Hankija** grupis **Kanded** suvand **Kanded**).</span><span class="sxs-lookup"><span data-stu-id="d481b-151">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable \> Vendors \> All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="d481b-152">Kuid teil on vaja, et kõik hankija kanded oleksid samal ajal ühes elektroonilises dokumendis XML-vormingus.</span><span class="sxs-lookup"><span data-stu-id="d481b-152">However, you want to have all vendor transaction at the same time in one electronic document in XML format.</span></span> <span data-ttu-id="d481b-153">See lahendus koosneb mitmest ER-i konfiguratsioonist, mis sisaldavad nõutud andmemudelit, metaandmeid, mudelivastendust ja vormingu komponente.</span><span class="sxs-lookup"><span data-stu-id="d481b-153">This solution will consist of several ER configurations that contain the required data model, metadata, model mapping, and format components.</span></span>

1. <span data-ttu-id="d481b-154">Logige sisse RCS-i eksemplari, mis on teie ettevõtte jaoks ette valmistatud.</span><span class="sxs-lookup"><span data-stu-id="d481b-154">Sign in to the instance of RCS that has been provisioned for your company.</span></span>
2. <span data-ttu-id="d481b-155">Selles õppetükis loote näidisettevõtte **Litware, Inc** jaoks konfiguratsioonid ja muudate neid.</span><span class="sxs-lookup"><span data-stu-id="d481b-155">In this tutorial, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="d481b-156">Seetõttu veenduge, et see konfiguratsiooni pakkuja oleks RCS-i lisatud ja aktiivsena valitud.</span><span class="sxs-lookup"><span data-stu-id="d481b-156">Therefore, make sure that this configuration provider has been added to RCS and selected as active.</span></span> <span data-ttu-id="d481b-157">Juhiste saamiseks vaadake teemat [Konfiguratsiooni pakkujate loomine ja nende aktiivseks märkimine](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="d481b-157">For instructions, see the [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md) procedure.</span></span>
3. <span data-ttu-id="d481b-158">Tööruumis **Elektrooniline aruandlus** valige paan **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="d481b-158">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="d481b-159">Importige lehel **Konfiguratsioonid** ER-i konfiguratsioonid, mille eeltingimusena RCS-i alla laadisite, järgmises järjestuses: andmemudel, metaandmed, mudelivastendus, vorming.</span><span class="sxs-lookup"><span data-stu-id="d481b-159">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into RCS, in the following order: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="d481b-160">Toimige iga konfiguratsiooni puhul järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="d481b-160">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="d481b-161">Valige toimingupaanil suvand **Rahavahetus \> Laadi XML-failist**.</span><span class="sxs-lookup"><span data-stu-id="d481b-161">On the Action Pane, select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="d481b-162">Valige käsk **Sirvi**, et valida nõutava ER-i konfiguratsiooni jaoks sobiv fail XML-vormingus.</span><span class="sxs-lookup"><span data-stu-id="d481b-162">Select **Browse** to select the appropriate file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="d481b-163">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="d481b-163">Select **OK**.</span></span>

    ![Konfiguratsioonide leht RCS-is](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a><span data-ttu-id="d481b-165">ER-i lahenduse kasutamine täitmise jälituseks</span><span class="sxs-lookup"><span data-stu-id="d481b-165">Run the ER solution to trace execution</span></span>

<span data-ttu-id="d481b-166">Oletame, et olete lõpetanud ER-i lahenduse esimese versiooni kujundamise.</span><span class="sxs-lookup"><span data-stu-id="d481b-166">Assume that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="d481b-167">Nüüd soovite seda testida oma eksemplaris ja analüüsida täitmise jõudlust.</span><span class="sxs-lookup"><span data-stu-id="d481b-167">You now want to test it in your instance and analyze execution performance.</span></span>

### <a name="import-an-er-configuration-from-rcs-into-finance-and-operations"></a><a id='import-configuration'></a><span data-ttu-id="d481b-168">ER-konfiguratsiooni importimine RCS-ist rakendusse Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d481b-168">Import an ER configuration from RCS into Finance and Operations</span></span>

1. <span data-ttu-id="d481b-169">Logige sisse oma rakenduse eksemplari.</span><span class="sxs-lookup"><span data-stu-id="d481b-169">Sign in to your application instance.</span></span>
2. <span data-ttu-id="d481b-170">Selles õppetükis impordite konfiguratsioonid RCS-i eksemplarist (kus kujundate ER-i komponente) oma eksemplari (kus testite ja lõpuks neid kasutate).</span><span class="sxs-lookup"><span data-stu-id="d481b-170">For this tutorial, you will import configurations from your RCS instance (where you design your ER components) into your instance (where you test and finally use them).</span></span> <span data-ttu-id="d481b-171">Seega peate veenduma, et kõik nõutud artefaktid oleksid ette valmistatud.</span><span class="sxs-lookup"><span data-stu-id="d481b-171">Therefore, you must make sure that all the required artifacts have been prepared.</span></span> <span data-ttu-id="d481b-172">Juhised leiate teemast [Elektroonilise aruandluse (ER) konfiguratsioonide importimine teenusest Regulatory Configuration Services (RCS)](rcs-download-configurations.md).</span><span class="sxs-lookup"><span data-stu-id="d481b-172">For instructions, see the [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](rcs-download-configurations.md) procedure.</span></span>
3. <span data-ttu-id="d481b-173">Järgige neid samme, et importida konfiguratsioonid RCS-ist rakendusse.</span><span class="sxs-lookup"><span data-stu-id="d481b-173">Follow these steps to import the configurations from RCS into the application:</span></span>

    1. <span data-ttu-id="d481b-174">Valige tööruumi **Elektrooniline aruandlus** konfiguratsiooni pakkuja **Litware, Inc.** paanilt valik **Hoidlad**.</span><span class="sxs-lookup"><span data-stu-id="d481b-174">In the **Electronic reporting** workspace, on the tile for the **Litware, Inc.** configuration provider, select **Repositories**.</span></span>
    2. <span data-ttu-id="d481b-175">Valige lehel **Konfiguratsioonihoidla** hoidla tüübiga **RCS** ja seejärel valige käsk **Ava**.</span><span class="sxs-lookup"><span data-stu-id="d481b-175">On the **Configuration repository** page, select the repository of the **RCS** type, and then select **Open**.</span></span>
    3. <span data-ttu-id="d481b-176">Valige kiirkaardil **Konfiguratsioonid** konfiguratsioon **Jõudluse jälituse vorming**.</span><span class="sxs-lookup"><span data-stu-id="d481b-176">On the **Configurations** FastTab, select the **Performance trace format** configuration.</span></span>
    4. <span data-ttu-id="d481b-177">Valige kiirkaardil **Versioonid** valitud konfiguratsiooni versioon **1.1** ja seejärel käsk **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="d481b-177">On the **Versions** FastTab, select version **1.1** of the selected configuration, and then select **Import**.</span></span>

    ![Konfiguratsioonide hoidla leht](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

<span data-ttu-id="d481b-179">Andmemudeli ja mudelivastenduse vastavate versioonide konfiguratsioonid imporditakse eeltingimustena automaatselt imporditud ER-vormingu konfiguratsioonile.</span><span class="sxs-lookup"><span data-stu-id="d481b-179">The corresponding versions of the data model and model mapping configurations are automatically imported as prerequisites for the imported ER format configuration.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="d481b-180">ER-i jõudluse jälituse sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="d481b-180">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="d481b-181">Minge jaotisse **Organisatsiooni haldamine \> Elektrooniline aruandlus \> Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="d481b-181">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="d481b-182">Valige lehe **Konfiguratsioonid** toimingupaani vahekaardi **Konfiguratsioonid** grupist **Täpsemad sätted** valik **Kasutaja parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="d481b-182">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="d481b-183">Toimige dialoogiboksi **Kasutaja parameetrid** jaotises **Täitmise jälitus** järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="d481b-183">In the **User parameters** dialog box, in the **Execution tracing** section, follow these steps:</span></span>

    1. <span data-ttu-id="d481b-184">Määrake väljal **Täitmise jälituse vorming** loodud jõudluse jäljele vorming, milles talletatakse täitmise üksikasjad ER-vormingu ja vastendamise elementide jaoks.</span><span class="sxs-lookup"><span data-stu-id="d481b-184">In the **Execution trace format** field, specify the format of the generated performance trace that the execution details should be stored in for ER format and mapping elements:</span></span>

        - <span data-ttu-id="d481b-185">**Silumise jälgimisvorming** – valige see väärtus, kui plaanite interaktiivselt käitada lühikese täitmisajaga ER-vormingu.</span><span class="sxs-lookup"><span data-stu-id="d481b-185">**Debug trace format** – Select this value if you plan to interactively run an ER format that has a short execution time.</span></span> <span data-ttu-id="d481b-186">Siis käivitatakse ER-vormingu käivitamise üksikasjade kogum.</span><span class="sxs-lookup"><span data-stu-id="d481b-186">The collection of details about ER format execution is then started.</span></span> <span data-ttu-id="d481b-187">Kui see väärtus on valitud, kogub jõudluse jälitus teavet järgmistele toimingutele kulutatud aja kohta.</span><span class="sxs-lookup"><span data-stu-id="d481b-187">When this value is selected, the performance trace collects information about the time that is spent on the following actions:</span></span>

            - <span data-ttu-id="d481b-188">Iga andmeallika käitamine mudelivastendusel, mida kutsutakse andmeid tooma</span><span class="sxs-lookup"><span data-stu-id="d481b-188">Running each data source in the model mapping that is called to get data</span></span>
            - <span data-ttu-id="d481b-189">Iga vormingu üksuse töötlemine andmete sisestamiseks loodavasse väljundisse</span><span class="sxs-lookup"><span data-stu-id="d481b-189">Processing each format item to enter data in the output that is generated</span></span>

            <span data-ttu-id="d481b-190">Kui valite **silumisjälje vormingu** väärtuse, saate analüüsida jälje sisu ER-toimingu kujundajas.</span><span class="sxs-lookup"><span data-stu-id="d481b-190">If you select the **Debug trace format** value, you can analyze the content of the trace in the ER Operation designer.</span></span> <span data-ttu-id="d481b-191">Seal saate vaadata jäljes mainitud ER-vormingut või vastendamise elemente.</span><span class="sxs-lookup"><span data-stu-id="d481b-191">There, you can view the ER format or mapping elements that are mentioned in the trace.</span></span>

        - <span data-ttu-id="d481b-192">**Kokkuvõtlik jälgimisvorming** – valige see väärtus, kui plaanite käitada pika täitmisajaga ER-vormingu partiirežiimis.</span><span class="sxs-lookup"><span data-stu-id="d481b-192">**Aggregated trace format** – Select this value if you plan to run an ER format that has a long execution time in batch mode.</span></span> <span data-ttu-id="d481b-193">Siis käivitatakse ER-vormingu käivitamise kokkuvõtlik üksikasjade kogum.</span><span class="sxs-lookup"><span data-stu-id="d481b-193">The collection of the aggregated details about ER format execution is then started.</span></span> <span data-ttu-id="d481b-194">Kui see väärtus on valitud, kogub jõudluse jälitus teavet järgmistele toimingutele kulutatud aja kohta.</span><span class="sxs-lookup"><span data-stu-id="d481b-194">When this value is selected, the performance trace collects information about the time that is spent on the following actions:</span></span>

            - <span data-ttu-id="d481b-195">Iga andmeallika käitamine mudelivastendusel, mida kutsutakse andmeid tooma</span><span class="sxs-lookup"><span data-stu-id="d481b-195">Running each data source in the model mapping that is called to get data</span></span>
            - <span data-ttu-id="d481b-196">Iga andmeallika käitamine vormingu vastendusel, mida kutsutakse andmeid tooma</span><span class="sxs-lookup"><span data-stu-id="d481b-196">Running each data source in the format mapping that is called to get data</span></span>
            - <span data-ttu-id="d481b-197">Iga vormingu üksuse töötlemine andmete sisestamiseks loodavasse väljundisse</span><span class="sxs-lookup"><span data-stu-id="d481b-197">Processing each format item to enter data in the output that is generated</span></span>

            <span data-ttu-id="d481b-198">**Agregaeeritud jälitusvormingu** väärtus on saadaval Microsoft Dynamics 365 Finance versioonis 10.0.20 või uuemas.</span><span class="sxs-lookup"><span data-stu-id="d481b-198">The **Aggregated trace format** value is available in Microsoft Dynamics 365 Finance version 10.0.20 and later.</span></span>

            <span data-ttu-id="d481b-199">ER-vormingu kujundajas ja ER-mudeli vastendamise kujundajas saate vaadata üksiku komponendi kogu täitmisaega.</span><span class="sxs-lookup"><span data-stu-id="d481b-199">In the ER format designer and ER model mapping designer, you can view the total execution time for a single component.</span></span> <span data-ttu-id="d481b-200">Lisaks sisaldab jälg käivitamise üksikasju, nt teostamiste arvu ning üksiku käivitamise minimaalset ja maksimaalset aega.</span><span class="sxs-lookup"><span data-stu-id="d481b-200">Additionally, the trace contains details about the execution, such as the number of executions, and the minimum and maximum time of a single execution.</span></span>

            > [!NOTE]
            > <span data-ttu-id="d481b-201">See jälg kogutakse jälgitud komponentide tee põhjal.</span><span class="sxs-lookup"><span data-stu-id="d481b-201">This trace is collected based on the traced components path.</span></span> <span data-ttu-id="d481b-202">Seetõttu võib statistika olla vale, kui üksik vanemkomponent sisaldab mitut nimetamata alamkomponenti või kui mitme alamkomponendi nimi on sama.</span><span class="sxs-lookup"><span data-stu-id="d481b-202">Therefore, the statistics might be incorrect when a single parent component contains several unnamed child components, or when several child components have the same name.</span></span>

    2. <span data-ttu-id="d481b-203">Määrake järgmiste suvandite olekuks **Jah**, et koguda kindlaid üksikasju ER-i mudelivastenduse ja ER-vormingu komponentide täitmise kohta.</span><span class="sxs-lookup"><span data-stu-id="d481b-203">Set the following options to **Yes** to collect specific details of the execution of the ER model mapping and ER format components:</span></span>

        - <span data-ttu-id="d481b-204">**Päringustatistika sissenõudmine** – kui see valik on sisse lülitatud, kogub jõudluse jälitus järgmist teavet.</span><span class="sxs-lookup"><span data-stu-id="d481b-204">**Collect query statistics** – When this option is turned on, the performance trace will collect the following information:</span></span>

            - <span data-ttu-id="d481b-205">Andmeallikate tehtud andmebaasi kutsete arv</span><span class="sxs-lookup"><span data-stu-id="d481b-205">The number of database calls that were made by data sources</span></span>
            - <span data-ttu-id="d481b-206">Korduvate kutsete arv andmebaasi</span><span class="sxs-lookup"><span data-stu-id="d481b-206">The number of duplicate calls to the database</span></span>
            - <span data-ttu-id="d481b-207">Andmebaasi kutsete tegemiseks kasutatud SQL-i lausete üksikasjad</span><span class="sxs-lookup"><span data-stu-id="d481b-207">Details of the SQL statements that were used to make database calls</span></span>

        - <span data-ttu-id="d481b-208">**Jälita vahemälule juurdepääsu** – kui see valik on sisse lülitatud, kogub jõudluse jälitus teavet ER-i mudelivastenduse vahemälu kasutuse kohta.</span><span class="sxs-lookup"><span data-stu-id="d481b-208">**Trace access of caching** – When this option is turned on, the performance trace will collect information about the ER model mapping's cache usage.</span></span>
        - <span data-ttu-id="d481b-209">**Jälita andmete juurdepääsu** – kui see valik on sisse lülitatud, kogub jõudluse jälitus teavet andmebaasi kutsete arvu kohta, mis on tehtud kirjeloendi tüüpi täidetud andmeallikate jaoks.</span><span class="sxs-lookup"><span data-stu-id="d481b-209">**Trace data access** – When this option is turned on, the performance trace will collect information about the number of calls to the database for executed data sources of the record list type.</span></span>
        - <span data-ttu-id="d481b-210">**Jälita loendi loetelu** – kui see valik on sisse lülitatud, kogub jõudluse jälitus teavet kirjete arvu kohta, mis on taotletud kirjeloendi tüüpi andmeallikatest.</span><span class="sxs-lookup"><span data-stu-id="d481b-210">**Trace list enumeration** – When this option is turned on, the performance trace will collect information about the number of records that are requested from data sources of the record list type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d481b-211">Dialoogiboksi **Kasutaja parameetrid** parameetrid kehtivad konkreetsele kasutajale ja praegusele ettevõttele.</span><span class="sxs-lookup"><span data-stu-id="d481b-211">The parameters in the **User parameters** dialog box are specific to the user and the current company.</span></span>

    ![Kasutaja parameetrite dialoogiaken](./media/GER-PerfTrace-GER-UserParameters.png)

### <a name="run-the-er-format"></a><a id='run-format'></a><span data-ttu-id="d481b-213">ER-vormingu käivitamine</span><span class="sxs-lookup"><span data-stu-id="d481b-213">Run the ER format</span></span>

1. <span data-ttu-id="d481b-214">Valige ettevõte **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="d481b-214">Select the **DEMF** company.</span></span>
2. <span data-ttu-id="d481b-215">Minge jaotisse **Organisatsiooni haldamine \> Elektrooniline aruandlus \> Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="d481b-215">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3. <span data-ttu-id="d481b-216">Valige lehe **Konfiguratsioonid** konfiguratsioonipuult üksus **Jõudluse jälituse vorming**.</span><span class="sxs-lookup"><span data-stu-id="d481b-216">On the **Configurations** page, in the configuration tree, select the **Performance trace format** item.</span></span>
4. <span data-ttu-id="d481b-217">Valige toimingupaanil käsk **Käivita**.</span><span class="sxs-lookup"><span data-stu-id="d481b-217">On the Action Pane, select **Run**.</span></span>

<span data-ttu-id="d481b-218">Pange tähele, et loodud fail esitab teavet kuue hankija 265 kande kohta.</span><span class="sxs-lookup"><span data-stu-id="d481b-218">Notice that the file that is generated presents information about 265 transactions for six vendors.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="d481b-219">Täitmise jälje läbivaatus</span><span class="sxs-lookup"><span data-stu-id="d481b-219">Review the execution trace</span></span>

### <a name="export-the-generated-trace-from-the-application"></a><a id='export-trace'></a><span data-ttu-id="d481b-220">Eksportige loodud jälg rakendusest</span><span class="sxs-lookup"><span data-stu-id="d481b-220">Export the generated trace from the application</span></span>

<span data-ttu-id="d481b-221">Jõudluse jäljed lahutatakse ER-vormingu allikast ja neid saab järjestada välisele ZIP-failile.</span><span class="sxs-lookup"><span data-stu-id="d481b-221">Performance traces are decoupled from the source ER format and can be serialized to an external zip file.</span></span>

1. <span data-ttu-id="d481b-222">Minge jaotisse **Organisatsiooni haldamine\>  Elektrooniline aruandlus \>Konfiguratsiooni silumislogid**.</span><span class="sxs-lookup"><span data-stu-id="d481b-222">Go to **Organization administration \> Electronic reporting \> Configuration debug logs**.</span></span>
2. <span data-ttu-id="d481b-223">Valige lehe **Elektroonilise aruandluse käivituslogid** vasakpoolsel paanil **Konfiguratsiooni nimi** valik **Jõudluse jälituse vorming**, et leida logi kirjed, mis on loodud konfiguratsiooni **Jõudluse jälituse vorming** täitmisega.</span><span class="sxs-lookup"><span data-stu-id="d481b-223">On the **Electronic reporting run logs** page, in the left pane, in the **Configuration name** field, select **Performance trace format** to find the log records that have been generated by the execution of the **Performance trace format** configuration.</span></span>
3. <span data-ttu-id="d481b-224">Valige lehe paremas ülanurgas nupp **Manused** (kirjaklambrisümbol) või vajutage klahve **Ctrl + Shift + A**.</span><span class="sxs-lookup"><span data-stu-id="d481b-224">Select the **Attachments** button (the paper clip symbol) in the upper-right corner of the page, or press **Ctrl+Shift+A**.</span></span>

    ![Lehe Elektroonilise aruandluse käitamise logid nupp Manused](./media/GER-PerfTrace-GER-DebugLog.png)

4. <span data-ttu-id="d481b-226">Valige lehe **Elektroonilise aruandluse käitamise logide manused** toimingupaanil käsk **Ava**, et saada jõudluse jälg ZIP-failina ja seda kohalikult talletada.</span><span class="sxs-lookup"><span data-stu-id="d481b-226">On the **Attachments for Electronic reporting run logs** page, on the Action Pane, select **Open** to get the performance trace as a zip file and store it locally.</span></span>

    ![Elektroonilise aruandluse logide manused](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> <span data-ttu-id="d481b-228">Loodud jäljel on viide allika ER-i aruandele kordumatu aruande identifikaatori kaudu ainult **GUID**-vormingus.</span><span class="sxs-lookup"><span data-stu-id="d481b-228">The trace that is generated has a reference to the source ER report via a unique report identifier in **GUID** format only.</span></span> <span data-ttu-id="d481b-229">Vormingu versiooni nummerdamist ei arvestata.</span><span class="sxs-lookup"><span data-stu-id="d481b-229">The version numbering of the format isn't considered.</span></span>

<span data-ttu-id="d481b-230">Pange tähele, et täidetud ER-vormingu jaoks loodud jõudluse jälje ja ER-i mudelivastenduse vaheline seos põhineb kasutatud juurdeskriptoril ning üldisel andmemudelil.</span><span class="sxs-lookup"><span data-stu-id="d481b-230">Notice that the association between the performance trace that has been generated for the executed ER format and the ER model mapping is based on the root descriptor that was used and the common data model.</span></span> <span data-ttu-id="d481b-231">Vormingu ja mudelivastenduse versiooni nummerdamist ei arvestata.</span><span class="sxs-lookup"><span data-stu-id="d481b-231">The version numbering of the format and model mapping isn't considered.</span></span> <span data-ttu-id="d481b-232">Samuti ei arvestata mudelivastenduse lipu **Mudelivastenduse vaikeväärtus** sätet.</span><span class="sxs-lookup"><span data-stu-id="d481b-232">The setting of the **Default for model mapping** flag for the model mapping also isn't considered.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><a id='import-trace'></a><span data-ttu-id="d481b-233">Loodud jälje importimine RCS-i</span><span class="sxs-lookup"><span data-stu-id="d481b-233">Import the generated trace into RCS</span></span>

1. <span data-ttu-id="d481b-234">Valige RCS-i tööruumis **Elektrooniline aruandlus** paan **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="d481b-234">In RCS, in the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
2. <span data-ttu-id="d481b-235">Laiendage lehe **Konfiguratsioonid** konfiguratsioonipuul üksust **Jõudluse jälituse mudel** ja valige üksus **Jõudluse jälituse vorming**.</span><span class="sxs-lookup"><span data-stu-id="d481b-235">On the **Configurations** page, in the configuration tree, expand the **Performance trace model** item, and select the **Performance trace format** item.</span></span>
3. <span data-ttu-id="d481b-236">Valige toimingupaanil valik **Koostaja**.</span><span class="sxs-lookup"><span data-stu-id="d481b-236">On the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="d481b-237">Valige lehe **Vormingu koostaja** toimingupaanil **Jõudluse jälitus**.</span><span class="sxs-lookup"><span data-stu-id="d481b-237">On the **Format designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="d481b-238">Valige dialoogiaknas **Jõudluse jälituse tulemuste sätted** valik **Impordi jõudluse jälg**.</span><span class="sxs-lookup"><span data-stu-id="d481b-238">In the **Performance trace result settings** dialog box, select **Import performance trace**.</span></span>
6. <span data-ttu-id="d481b-239">Valige nupp **Sirvi**, et valida varem eksporditud zip fail.</span><span class="sxs-lookup"><span data-stu-id="d481b-239">Select **Browse** to select the zip file that you exported earlier.</span></span>
7. <span data-ttu-id="d481b-240">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="d481b-240">Select **OK**.</span></span>

    ![Jõudluse jälituse tulemuse sätete dialoogiboks RCS-is](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a><span data-ttu-id="d481b-242">Jõudluse jälituse kasutamine analüüsiks RCS-is – vormingu täitmine</span><span class="sxs-lookup"><span data-stu-id="d481b-242">Use the performance trace for analysis in RCS – Format execution</span></span>

1. <span data-ttu-id="d481b-243">Valige RCS-is lehel **Vormingu koostaja** käsk **Laienda/ahenda**, et laiendada kõigi vormingu üksuste sisu.</span><span class="sxs-lookup"><span data-stu-id="d481b-243">In RCS, on the **Format designer** page, select **Expand/collapse** to expand the content of all format items.</span></span>

    <span data-ttu-id="d481b-244">Pange tähele, et praeguse vormingu mõne üksuse kohta kuvatakse lisateavet.</span><span class="sxs-lookup"><span data-stu-id="d481b-244">Notice that additional information is shown for some items of the current format:</span></span>

    - <span data-ttu-id="d481b-245">Tegelik aeg, mis kulus andmete sisestamiseks loodud väljundisse kasutades vormingu üksust</span><span class="sxs-lookup"><span data-stu-id="d481b-245">The actual time that was spent entering data in the generated output by using the format item</span></span>
    - <span data-ttu-id="d481b-246">Sama aeg väljendatuna protsendina koguajast, mis kulutati kogu väljundi loomiseks</span><span class="sxs-lookup"><span data-stu-id="d481b-246">The same time expressed as a percentage of the total time that was spent generating the whole output</span></span>

    ![Vormingu koostaja leht RCS-is](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. <span data-ttu-id="d481b-248">Sulgege **Vormingu koostaja** leht.</span><span class="sxs-lookup"><span data-stu-id="d481b-248">Close **Format designer** page.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><a id='use-trace'></a><span data-ttu-id="d481b-249">Jõudluse jälituse kasutamine analüüsiks RCS-is – mudelivastendus</span><span class="sxs-lookup"><span data-stu-id="d481b-249">Use the performance trace for analysis in RCS – Model mapping</span></span>

1. <span data-ttu-id="d481b-250">Valige RCS-is lehe **Konfiguratsioonid** konfiguratsioonipuult üksus **Jõudluse jälituse vastendus**.</span><span class="sxs-lookup"><span data-stu-id="d481b-250">In RCS, on the **Configurations** page, in the configuration tree, select the **Performance trace mapping** item.</span></span>
2. <span data-ttu-id="d481b-251">Valige toimingupaanil valik **Koostaja**.</span><span class="sxs-lookup"><span data-stu-id="d481b-251">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="d481b-252">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="d481b-252">Select **Designer**.</span></span>
4. <span data-ttu-id="d481b-253">Valige lehe **Mudelivastenduse koostaja** toimingupaanil **Jõudluse jälitus**.</span><span class="sxs-lookup"><span data-stu-id="d481b-253">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="d481b-254">Valige jälg, mille varem importisite.</span><span class="sxs-lookup"><span data-stu-id="d481b-254">Select the trace that you imported earlier.</span></span>
6. <span data-ttu-id="d481b-255">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="d481b-255">Select **OK**.</span></span>

<span data-ttu-id="d481b-256">Pange tähele, et praeguse mudelivastenduse mõne andmeallika üksuse kohta muutub kättesaadavaks uus teave.</span><span class="sxs-lookup"><span data-stu-id="d481b-256">Notice that new information becomes available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="d481b-257">Tegelik aeg, mis kulus andmeallika abil andmete toomisele</span><span class="sxs-lookup"><span data-stu-id="d481b-257">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="d481b-258">Sama aeg väljendatuna protsendina koguajast, mis kulutati kogu mudelivastenduse käitamise peale</span><span class="sxs-lookup"><span data-stu-id="d481b-258">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

<span data-ttu-id="d481b-259">Pange tähele, et ER annab teile teate, et praegune mudelivastendus dubleerib andmebaasi taotlusi ajal, mil andmeallikat VendTable/\<Relations/VendTrans.VendTable\_AccountNum käitatakse.</span><span class="sxs-lookup"><span data-stu-id="d481b-259">Notice that ER informs you that the current model mapping duplicates database requests while the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source is run.</span></span> <span data-ttu-id="d481b-260">Dubleerimine toimub seetõttu, et hankija kannete loendit kutsutakse iga itereeritud hankija kirje puhul kaks korda.</span><span class="sxs-lookup"><span data-stu-id="d481b-260">This duplication occurs because the list of vendor transactions is called two times for each iterated vendor record:</span></span>

- <span data-ttu-id="d481b-261">Üks kutse tehakse, et sisestada andmemudelis iga kande üksikasjad konfigureeritud sidumiste alusel.</span><span class="sxs-lookup"><span data-stu-id="d481b-261">One call is made to enter details of each transaction in the data model, based on configured bindings.</span></span>
- <span data-ttu-id="d481b-262">Teine kutse tehakse, et sisestada andmemudelis iga hankija kohta arvutatud kannete arv.</span><span class="sxs-lookup"><span data-stu-id="d481b-262">One call is made to enter the calculated number of transactions per vendor in the data model.</span></span>

![Teade dubleeritud andmebaasi taotluste kohta mudelivastenduse koostaja lehel RCS-is](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

<span data-ttu-id="d481b-264">Väärtus **\[Q:530\]** näitab, et tabelit VendTrans kutsuti 530 korda, et tagastada sellest tabelist kirje andmeallikasse VendTable/\<Relations/VendTrans.VendTable\_AccountNum.</span><span class="sxs-lookup"><span data-stu-id="d481b-264">The value **\[Q:530\]** indicates that the VendTrans table was called 530 times to return a record from that table to the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source.</span></span> <span data-ttu-id="d481b-265">Väärtus **\[530\]** näitab, et andmeallikat VendTable/\<Relations/VendTrans.VendTable\_AccountNum kutsuti 530 korda, et tagastada kirje sellest andmeallikast ja sisestada selle üksikasjad andmemudelisse.</span><span class="sxs-lookup"><span data-stu-id="d481b-265">The value **\[530\]** indicates that the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source was called 530 times to return a record from that data source and enter the details from it in the data model.</span></span>

<span data-ttu-id="d481b-266">Soovitame kasutada andmeallika VendTable/\<Relations/VendTrans.VendTable\_AccountNum jaoks vahemällusalvestust, et vähendada kutsete arvu, mida tehakse 265 kande üksikasjade saamiseks, ja aidata parandada mudelivastenduse jõudlust.</span><span class="sxs-lookup"><span data-stu-id="d481b-266">We recommend that you use caching for the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source, to reduce the number of calls that are made to get the details for 265 transactions and help improve the performance of the model mapping.</span></span>

<span data-ttu-id="d481b-267">Samuti võib see olla kasulik. et vähendada andmeallikale LedgerTransTypeList tehtud kutsumiste arvu.</span><span class="sxs-lookup"><span data-stu-id="d481b-267">It can also be useful to reduce the number of calls that are made to the LedgerTransTypeList data source.</span></span> <span data-ttu-id="d481b-268">Seda andmeallikat kasutatakse **LedgerTransType**-i nummerdamise iga väärtuse seostamiseks oma sildiga.</span><span class="sxs-lookup"><span data-stu-id="d481b-268">This data source is used to associate each value of the **LedgerTransType** enumeration with its label.</span></span> <span data-ttu-id="d481b-269">Seda andmeallikat kasutades saate leida sobiva sildi ja seda andmeallikasse iga hankija kande jaoks sisestada.</span><span class="sxs-lookup"><span data-stu-id="d481b-269">By using this data source, you can find an appropriate label and enter it in the data model for each vendor transaction.</span></span> <span data-ttu-id="d481b-270">Praegune kutsete arv sellele andmeallikale (9027) on 265 kande kohta üsna kõrge.</span><span class="sxs-lookup"><span data-stu-id="d481b-270">The current number of calls to this data source (9,027) is quite high for 265 transactions.</span></span>

![Mudelivastenduse koostaja leht RCS-is, mis näitab 9027 kutset andmeallikale](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="d481b-272">Mudelivastenduse parandamine täitmise jälitusest saadud teabe põhjal</span><span class="sxs-lookup"><span data-stu-id="d481b-272">Improve the model mapping based on information from the execution trace</span></span>

### <a name="modify-the-logic-of-the-model-mapping"></a><span data-ttu-id="d481b-273">Mudelivastenduse loogika muutmine</span><span class="sxs-lookup"><span data-stu-id="d481b-273">Modify the logic of the model mapping</span></span>

1. <span data-ttu-id="d481b-274">Järgige vahemälu kasutamiseks järgmisi samme, et vältida andmebaasi dubleeritud kutseid.</span><span class="sxs-lookup"><span data-stu-id="d481b-274">Follow these steps to use caching, to help prevent duplicate calls to the database:</span></span>

    1. <span data-ttu-id="d481b-275">Valige RCS-is lehe **Mudelivastenduse koostaja** paanil **Andmeallikad** üksus **VendTable**.</span><span class="sxs-lookup"><span data-stu-id="d481b-275">In RCS, on the **Model mapping designer** page, in the **Data sources** pane, select the **VendTable** item.</span></span>
    2. <span data-ttu-id="d481b-276">Valige suvand **Vahemälu**.</span><span class="sxs-lookup"><span data-stu-id="d481b-276">Select **Cache**.</span></span>
    3. <span data-ttu-id="d481b-277">Laiendage üksust **VendTable**, laiendage andmeallika VendTable üks-mitmele seoste loendit (üksus **\<Seosed**) ja valige üksus **VendTrans.VendTable\_AccountNum**.</span><span class="sxs-lookup"><span data-stu-id="d481b-277">Expand the **VendTable** item, expand the list of one-to-many relations for the VendTable data source (the **\<Relations** item), and select the **VendTrans.VendTable\_AccountNum** item.</span></span>
    4. <span data-ttu-id="d481b-278">Valige suvand **Vahemälu**.</span><span class="sxs-lookup"><span data-stu-id="d481b-278">Select **Cache**.</span></span>

    ![Vahemälu häälestus, mis aitab vältida dubleeritud kutseid](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. <span data-ttu-id="d481b-280">Järgige neid samme, et tuua andmeallikas LedgerTransTypeList andmeallika VendTable ulatusse.</span><span class="sxs-lookup"><span data-stu-id="d481b-280">Follow these steps to bring the LedgerTransTypeList data source into the scope of the VendTable data source:</span></span>

    1. <span data-ttu-id="d481b-281">Laiendage paanil **Andmeallika tüübid** üksust **Funktsioonid** ja valige üksus **Arvutatud väli**.</span><span class="sxs-lookup"><span data-stu-id="d481b-281">In the **Data source types** pane, expand the **Functions** item, and select the **Calculated field** item.</span></span>
    2. <span data-ttu-id="d481b-282">Valige paanil **Andmeallikad** üksus **VendTable**.</span><span class="sxs-lookup"><span data-stu-id="d481b-282">In the **Data sources** pane, select the **VendTable** item.</span></span>
    3. <span data-ttu-id="d481b-283">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="d481b-283">Select **Add**.</span></span>
    4. <span data-ttu-id="d481b-284">Sisestage väljale **Nimi** tekst **\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="d481b-284">In the **Name** field, enter **\$TransType**.</span></span>
    5. <span data-ttu-id="d481b-285">Valige **Valemi redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="d481b-285">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="d481b-286">Sisestage väljale **Valem** tekst **LedgerTransTypeList**.</span><span class="sxs-lookup"><span data-stu-id="d481b-286">In the **Formula** field, enter **LedgerTransTypeList**.</span></span>
    7. <span data-ttu-id="d481b-287">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d481b-287">Select **Save**.</span></span>
    8. <span data-ttu-id="d481b-288">Sulgege leht **Valemiredaktor**.</span><span class="sxs-lookup"><span data-stu-id="d481b-288">Close the **Formula editor** page.</span></span>
    9. <span data-ttu-id="d481b-289">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="d481b-289">Click **OK**.</span></span>

3. <span data-ttu-id="d481b-290">Järgige neid samme, et kasutada vahemällusalvestust välja **\$TransType** jaoks.</span><span class="sxs-lookup"><span data-stu-id="d481b-290">Follow these steps to do caching of the **\$TransType** field:</span></span>

    1. <span data-ttu-id="d481b-291">Valige üksus **LedgerTransTypeList**.</span><span class="sxs-lookup"><span data-stu-id="d481b-291">Select the **LedgerTransTypeList** item.</span></span>
    2. <span data-ttu-id="d481b-292">Valige suvand **Vahemälu**.</span><span class="sxs-lookup"><span data-stu-id="d481b-292">Select **Cache**.</span></span>
    3. <span data-ttu-id="d481b-293">Valige üksus **VendTable.\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="d481b-293">Select the **VendTable.\$TransType** item.</span></span>
    4. <span data-ttu-id="d481b-294">Valige suvand **Vahemälu**.</span><span class="sxs-lookup"><span data-stu-id="d481b-294">Select **Cache**.</span></span>

    ![Vahemällusalvestuse seadistamine välja $TransType jaoks](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. <span data-ttu-id="d481b-296">Järgige neid samme, et muuta välja **\$TransTypeRecord** nii, et see hakkaks kasutama vahemällu salvestatud välja **\$TransType.**</span><span class="sxs-lookup"><span data-stu-id="d481b-296">Follow these steps to change the **\$TransTypeRecord** field so that it starts to use the cached **\$TransType** field:</span></span>

    1. <span data-ttu-id="d481b-297">Laiendage paanil **Andmeallikad** üksust **VendTable**, üksust **\<Seosed**, üksust **VendTrans.VendTable\_AccountNum** ja valige üksus **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord**.</span><span class="sxs-lookup"><span data-stu-id="d481b-297">In the **Data sources** pane, expand the **VendTable** item, expand the **\<Relations** item, expand the **VendTrans.VendTable\_AccountNum** item, and select the **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** item.</span></span>
    2. <span data-ttu-id="d481b-298">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="d481b-298">Select **Edit**.</span></span>
    3. <span data-ttu-id="d481b-299">Valige **Valemi redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="d481b-299">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="d481b-300">Leidke väljal **Valem** järgmine avaldis.</span><span class="sxs-lookup"><span data-stu-id="d481b-300">In the **Formula** field, find the following expression:</span></span>

        <span data-ttu-id="d481b-301">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span><span class="sxs-lookup"><span data-stu-id="d481b-301">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span></span>

    5. <span data-ttu-id="d481b-302">Sisestage väljale **Valem** järgmine avaldis.</span><span class="sxs-lookup"><span data-stu-id="d481b-302">In the **Formula** field, enter the following expression:</span></span>

        <span data-ttu-id="d481b-303">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span><span class="sxs-lookup"><span data-stu-id="d481b-303">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span></span>

    6. <span data-ttu-id="d481b-304">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d481b-304">Select **Save**.</span></span>
    7. <span data-ttu-id="d481b-305">Sulgege leht **Valemiredaktor**.</span><span class="sxs-lookup"><span data-stu-id="d481b-305">Close the **Formula editor** page.</span></span>
    8. <span data-ttu-id="d481b-306">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="d481b-306">Select **OK**.</span></span>

5. <span data-ttu-id="d481b-307">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d481b-307">Select **Save**.</span></span>
6. <span data-ttu-id="d481b-308">Sulgege leht **Mudelivastenduse koostaja**.</span><span class="sxs-lookup"><span data-stu-id="d481b-308">Close the **Model mapping designer** page.</span></span>
7. <span data-ttu-id="d481b-309">Sulgege leht **Mudelivastendused**.</span><span class="sxs-lookup"><span data-stu-id="d481b-309">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="d481b-310">ER-i mudelivastenduse muudetud versiooni lõpetamine</span><span class="sxs-lookup"><span data-stu-id="d481b-310">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="d481b-311">Valige RCS-is lehe **Konfiguratsioonid** kiirkaardil **Versioonid** konfiguratsiooni **Jõudluse jälituse vastendus** versioon **1.2**.</span><span class="sxs-lookup"><span data-stu-id="d481b-311">In RCS, on the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance trace mapping** configuration.</span></span>
2. <span data-ttu-id="d481b-312">Valige käsk **Muuda olekut**.</span><span class="sxs-lookup"><span data-stu-id="d481b-312">Select **Change status**.</span></span>
3. <span data-ttu-id="d481b-313">Valige **Lõpeta**.</span><span class="sxs-lookup"><span data-stu-id="d481b-313">Select **Complete**.</span></span>

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-the-application"></a><span data-ttu-id="d481b-314">Muudetud ER-i mudelivastenduse konfiguratsiooni importimine RCS-ist rakendusse</span><span class="sxs-lookup"><span data-stu-id="d481b-314">Import the modified ER model mapping configuration from RCS into the application</span></span>

<span data-ttu-id="d481b-315">Korrake samme selle teema jaotises [ER-i konfiguratsiooni importimine RCS-ist rakendusse Finance and Operations](#import-configuration), et importida konfiguratsiooni **Jõudluse jälituse vastendus** versioon 1.2.</span><span class="sxs-lookup"><span data-stu-id="d481b-315">Repeat the steps in the [Import an ER configuration from RCS into Finance and Operations](#import-configuration) section earlier in this topic to import version 1.2 of the **Performance trace mapping** configuration.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="d481b-316">Muudetud ER-i lahenduse kasutamine täitmise jälituseks</span><span class="sxs-lookup"><span data-stu-id="d481b-316">Run the modified ER solution to trace execution</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="d481b-317">ER-vormingu käivitamine</span><span class="sxs-lookup"><span data-stu-id="d481b-317">Run the ER format</span></span>

<span data-ttu-id="d481b-318">Korrake samme selle teema jaotises [ER-vormingu käivitamine](#run-format), et luua uus jõudluse jälg.</span><span class="sxs-lookup"><span data-stu-id="d481b-318">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="work-with-the-execution-trace"></a><span data-ttu-id="d481b-319">Töö käivitamise jäljega</span><span class="sxs-lookup"><span data-stu-id="d481b-319">Work with the execution trace</span></span>

### <a name="export-the-generated-trace-from-the-application"></a><span data-ttu-id="d481b-320">Eksportige loodud jälg rakendusest</span><span class="sxs-lookup"><span data-stu-id="d481b-320">Export the generated trace from the application</span></span>

<span data-ttu-id="d481b-321">Korrake samme selle teema jaotises [Loodud jälje eksportimine rakendusest](#export-trace), et salvestada uus jõudluse jälg kohalikult.</span><span class="sxs-lookup"><span data-stu-id="d481b-321">Repeat the steps in the [Export the generated trace from the application](#export-trace) section earlier in this topic to save a new performance trace locally.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><span data-ttu-id="d481b-322">Loodud jälje importimine RCS-i</span><span class="sxs-lookup"><span data-stu-id="d481b-322">Import the generated trace into RCS</span></span>

<span data-ttu-id="d481b-323">Korrake samme selle teema jaotises [Loodud jälje importimine RCS-i](#import-trace), et importida uus jõudluse jälg RCS-i.</span><span class="sxs-lookup"><span data-stu-id="d481b-323">Repeat the steps in the [Import the generated trace into RCS](#import-trace) section earlier in this topic to import the new performance trace into RCS.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><span data-ttu-id="d481b-324">Jõudluse jälituse kasutamine analüüsiks RCS-is – mudelivastendus</span><span class="sxs-lookup"><span data-stu-id="d481b-324">Use the performance trace for analysis in RCS – Model mapping</span></span>

<span data-ttu-id="d481b-325">Korrake samme selle teema jaotises [Jõudluse jälituse kasutamine analüüsiks RCS-is – mudelivastendus](#use-trace), et analüüsida viimast jõudluse jälge.</span><span class="sxs-lookup"><span data-stu-id="d481b-325">Repeat the steps in the [Use the performance trace for analysis in RCS – Model mapping](#use-trace) section earlier in this topic to analyze the latest performance trace.</span></span>

<span data-ttu-id="d481b-326">Pange tähele, et kohandused, mida tegite mudelivastendusele, on eemaldanud dubleeritud päringud andmebaasile.</span><span class="sxs-lookup"><span data-stu-id="d481b-326">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="d481b-327">Vähendatud on ka selle mudelivastenduse kutsete arvu andmebaasi tabelitele ja andmeallikatele.</span><span class="sxs-lookup"><span data-stu-id="d481b-327">The number of calls to database tables and data sources for this model mapping has been also reduced.</span></span> <span data-ttu-id="d481b-328">See on paranenud kogu ER-i lahenduse jõudlus.</span><span class="sxs-lookup"><span data-stu-id="d481b-328">Therefore, the performance of the whole ER solution has improved.</span></span>

![Jälje teave andmeallika VendTable kohta RCS-i lehel Mudelivastenduse koostaja](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

<span data-ttu-id="d481b-330">Jälje teabes näitab andmeallika VendTable väärtus **\[12\]**, et seda andmeallikat kutsuti 12 korda.</span><span class="sxs-lookup"><span data-stu-id="d481b-330">In the trace information, the value **\[12\]** for the VendTable data source indicates that this data source was called 12 times.</span></span> <span data-ttu-id="d481b-331">Väärtus **\[Q:6\]** näitab, et kuus kutset teisendati andmebaasi kutseteks andmeallika VendTable tabelile.</span><span class="sxs-lookup"><span data-stu-id="d481b-331">The value **\[Q:6\]** indicates that six calls were translated to database calls to the VendTable table.</span></span> <span data-ttu-id="d481b-332">Väärtus **\[C:6\]** näitab, et andmebaasist toodud kirjed salvestati vahemällu ja kuus muud kõnet töödeldi vahemälu abil.</span><span class="sxs-lookup"><span data-stu-id="d481b-332">The value **\[C:6\]** indicates that the records that were fetched from the database were cached, and six other calls were processed by using the cache.</span></span>

<span data-ttu-id="d481b-333">Pange tähele, et kutsete arv andmeallikale LedgerTransTypeList on vähendatud 9027-lt 240-le.</span><span class="sxs-lookup"><span data-stu-id="d481b-333">Notice that the number of calls to the LedgerTransTypeList data source has been reduced from 9,027 to 240.</span></span>

![Jälje teave andmeallika LedgerTransTypeList kohta RCS-i lehel Mudelivastenduse koostaja](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-the-application"></a><span data-ttu-id="d481b-335">Kontrollige käivitamise jälge rakenduses</span><span class="sxs-lookup"><span data-stu-id="d481b-335">Review the execution trace in the application</span></span>

<span data-ttu-id="d481b-336">Peale RCS-i võivad mõned versioonid pakkuda võimalusi ER-i raamistiku koostaja kogemuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="d481b-336">In addition to RCS, some versions might offer capabilities for an ER framework designer experience.</span></span> <span data-ttu-id="d481b-337">Nendel versioonidel on olemas suvand **Luba kujundusrežiim**, mida saab sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="d481b-337">These versions have an **Enable design mode** option that can be turned on.</span></span> <span data-ttu-id="d481b-338">Selle suvandi leiate lehe **Elektroonilise aruandluse parameetrid** vahekaardilt **Üldine**, mille saate avada tööruumist **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="d481b-338">You can find this option on the **General** tab of the **Electronic reporting parameters** page, which you can open from the **Electronic reporting** workspace.</span></span>

![Disainimise režiimi suvandi lubamine elektroonilise aruandluse parameetrite lehel](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

<span data-ttu-id="d481b-340">Kui kasutate ühte neist versioonidest, saate analüüsida loodud jõudluse jälje üksikasju otse rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d481b-340">If you use one of these versions, you can analyze the details of generated performance traces directly in the application.</span></span> <span data-ttu-id="d481b-341">Te ei pea neid eksportima rakendusest ning importima RCS-i.</span><span class="sxs-lookup"><span data-stu-id="d481b-341">You don't have to export them from the application and import them into RCS.</span></span>

## <a name="review-the-execution-trace-by-using-external-tools"></a><span data-ttu-id="d481b-342">Täitmise jälje läbivaatus väliste tööriistade abil</span><span class="sxs-lookup"><span data-stu-id="d481b-342">Review the execution trace by using external tools</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="d481b-343">Kasutaja parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="d481b-343">Configure user parameters</span></span>

1. <span data-ttu-id="d481b-344">Minge jaotisse **Organisatsiooni haldamine \> Elektrooniline aruandlus \> Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="d481b-344">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="d481b-345">Valige lehe **Konfiguratsioonid** toimingupaani vahekaardi **Konfiguratsioonid** grupist **Täpsemad sätted** valik **Kasutaja parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="d481b-345">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="d481b-346">Valige dialoogiboksi **Kasutaja parameetrid** jaotises **Täitmise jälitus** väljal **Täitmise jälje vorming** valik **PerfView XML.**</span><span class="sxs-lookup"><span data-stu-id="d481b-346">In the **User parameters** dialog box, in the **Execution tracing** section, in the **Execution trace format** field, select **PerfView XML**.</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="d481b-347">ER-vormingu käivitamine</span><span class="sxs-lookup"><span data-stu-id="d481b-347">Run the ER format</span></span>

<span data-ttu-id="d481b-348">Korrake samme selle teema jaotises [ER-vormingu käivitamine](#run-format), et luua uus jõudluse jälg.</span><span class="sxs-lookup"><span data-stu-id="d481b-348">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="d481b-349">Pange tähele, et veebibrauser pakub allalaadimiseks ZIP-faili.</span><span class="sxs-lookup"><span data-stu-id="d481b-349">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="d481b-350">See fail sisaldab jõudluse jälge PerfView-vormingus.</span><span class="sxs-lookup"><span data-stu-id="d481b-350">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="d481b-351">Seejärel saate kasutada PerfView jõudluse analüüsi tööriista, et analüüsida ER-vormingu täitmise üksikasju.</span><span class="sxs-lookup"><span data-stu-id="d481b-351">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span>

![Jõudluse jälje teave PerfView-vormingus](./media/GER-PerfTrace2-PerfViewTrace1.PNG)

## <a name="use-external-tools-to-review-an-execution-trace-that-includes-database-queries"></a><span data-ttu-id="d481b-353">Väliste tööriistade kasutamine täitmise jälje läbivaatamiseks, mis hõlmab andmebaasi päringuid</span><span class="sxs-lookup"><span data-stu-id="d481b-353">Use external tools to review an execution trace that includes database queries</span></span>

<span data-ttu-id="d481b-354">Tänu ER-raamistiku täiustustele pakub PerfView'is loodud jõudluse jälitus nüüd üksikasjalikumat teavet ER-i vormingu käivitamise kohta.</span><span class="sxs-lookup"><span data-stu-id="d481b-354">Because of improvements that have been made to the ER framework, the performance trace that is generated in PerfView format now offers more details about ER format execution.</span></span> <span data-ttu-id="d481b-355">Microsoft Dynamics 365 for Finance and Operations versioonis 10.0.4 (juuli, 2019) võib see jälg sisaldada ka rakenduse andmebaasile tehtud SQL-i päringute üksikasju.</span><span class="sxs-lookup"><span data-stu-id="d481b-355">In Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019), this trace can also include details of executed SQL queries to the application database.</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="d481b-356">Kasutaja parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="d481b-356">Configure user parameters</span></span>

1. <span data-ttu-id="d481b-357">Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="d481b-357">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="d481b-358">Valige lehe **Konfiguratsioonid** toimingupaani vahekaardi **Konfiguratsioonid** grupist **Täpsemad sätted** valik **Kasutaja parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="d481b-358">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="d481b-359">Seadke dialoogiboksi **Kasutaja parameetrid** jaotises **Täitmise jälitus** järgmised parameetrid.</span><span class="sxs-lookup"><span data-stu-id="d481b-359">In the **User parameters** dialog box, in the **Execution tracing** section, set the following parameters:</span></span>

    - <span data-ttu-id="d481b-360">Valige väljal **Täitmise jälituse vorming** suvand **PerfView XML**.</span><span class="sxs-lookup"><span data-stu-id="d481b-360">In the **Execution trace format** field, select **PerfView XML**.</span></span>
    - <span data-ttu-id="d481b-361">Seadistage **Päringustatistika sissenõudmise** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="d481b-361">Set the **Collect query statistics** option to **Yes**.</span></span>
    - <span data-ttu-id="d481b-362">Määrake suvand **Jälituse päring** olekule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="d481b-362">Set the **Trace query** option to **Yes**.</span></span>

    ![Jaotis Täitmise jälitus, dialoogiboks Kasutaja parameetrid](./media/GER-PerfTrace2-GER-UserParameters.PNG)

### <a name="run-the-er-format"></a><span data-ttu-id="d481b-364">ER-vormingu käivitamine</span><span class="sxs-lookup"><span data-stu-id="d481b-364">Run the ER format</span></span>

<span data-ttu-id="d481b-365">Korrake samme selle teema jaotises [ER-vormingu käivitamine](#run-format), et luua uus jõudluse jälg.</span><span class="sxs-lookup"><span data-stu-id="d481b-365">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="d481b-366">Pange tähele, et veebibrauser pakub allalaadimiseks ZIP-faili.</span><span class="sxs-lookup"><span data-stu-id="d481b-366">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="d481b-367">See fail sisaldab jõudluse jälge PerfView-vormingus.</span><span class="sxs-lookup"><span data-stu-id="d481b-367">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="d481b-368">Seejärel saate kasutada PerfView jõudluse analüüsi tööriista, et analüüsida ER-vormingu täitmise üksikasju.</span><span class="sxs-lookup"><span data-stu-id="d481b-368">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span> <span data-ttu-id="d481b-369">See jälg sisaldab nüüd SQL-i andmebaasi juurdepääsu üksikasju ER-vormingu käivitamise ajal.</span><span class="sxs-lookup"><span data-stu-id="d481b-369">This trace now includes the details of SQL database access during the execution of the ER format.</span></span>

![Käivitatud ER-vormingu jälitusteave PerfView'is](./media/GER-PerfTrace2-PerfViewTrace2.PNG)

## <a name="additional-resources"></a><span data-ttu-id="d481b-371">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="d481b-371">Additional resources</span></span>

- [<span data-ttu-id="d481b-372">Elektroonilise aruandluse ülevaade</span><span class="sxs-lookup"><span data-stu-id="d481b-372">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="d481b-373">Saate parandada ER-lahenduste jõudlust, lisades parameeteriseeritud ARVUTATUD VÄLJA andmeallikad</span><span class="sxs-lookup"><span data-stu-id="d481b-373">Improve performance of ER solutions by adding parameterized CALCULATED FIELD data sources</span></span>](er-calculated-field-ds-performance.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
