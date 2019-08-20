---
title: ER-vormingu täitmise jälitus jõudluse probleemide tõrkeotsinguks
description: Selles teemas kirjeldatakse, kuidas kasutada elektroonilises aruandluses (ER) jõudluse jälituse funktsiooni jõudluse probleemide tõrkeotsingu tegemiseks.
author: NickSelin
manager: AnnBe
ms.date: 06/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 7ec16bea1e4f7685f95178f848ba7348a06c31f3
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/12/2019
ms.locfileid: "1741499"
---
# <a name="trace-the-execution-of-er-formats-to-troubleshoot-performance-issues"></a><span data-ttu-id="f0c11-103">ER-vormingute täitmise jälitus jõudluse probleemide tõrkeotsinguks</span><span class="sxs-lookup"><span data-stu-id="f0c11-103">Trace the execution of ER formats to troubleshoot performance issues</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="f0c11-104">Üks osa elektroonilise aruandluse (ER) konfiguratsioonide kujundamisest elektrooniliste dokumentide loomise jaoks on määratleda meetod, mida kasutatakse andmete saamiseks rakendusest Microsoft Dynamics 365 for Finance and Operations, ja sisestada see loodud väljundisse.</span><span class="sxs-lookup"><span data-stu-id="f0c11-104">As part of the process of designing Electronic reporting (ER) configurations to generate electronic documents, you define the method that is used to get data out of Microsoft Dynamics 365 for Finance and Operations and enter it in the output that is generated.</span></span> <span data-ttu-id="f0c11-105">ER-i jõudluse jälituse funktsioon aitab märkimisväärselt vähendada aja- ja rahakulu, mis tekib ER-vormingu täitmise üksikasjade kogumisel ja nende kasutamisel jõudluse probleemide tõrkeotsinguks.</span><span class="sxs-lookup"><span data-stu-id="f0c11-105">The ER performance trace feature helps significantly reduce the time and cost that are involved in collecting the details of ER format execution and using them to troubleshoot performance issues.</span></span> <span data-ttu-id="f0c11-106">Selles õppetükis esitatakse juhised, kuidas jälitada täidetud ER-vormingute jõudlust rakenduses Finance and Operations ja kuidas kasutada jälitusest saadud teavet jõudluse täiustamiseks.</span><span class="sxs-lookup"><span data-stu-id="f0c11-106">This tutorial provides guidelines about how to take performance traces for executed ER formats in Finance and Operations, and how to use the information from these traces to help improve performance.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f0c11-107">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="f0c11-107">Prerequisites</span></span>

<span data-ttu-id="f0c11-108">Selle õppetüki näidete läbimiseks peavad teil olema järgmised juurdepääsuõigused.</span><span class="sxs-lookup"><span data-stu-id="f0c11-108">To complete the examples in this tutorial, you must have the following access:</span></span>

- <span data-ttu-id="f0c11-109">Juurdepääs Finance and Operationsile ühe järgmise rolli jaoks:</span><span class="sxs-lookup"><span data-stu-id="f0c11-109">Access to Finance and Operations for one of the following roles:</span></span>

    - <span data-ttu-id="f0c11-110">Elektroonilise aruandluse arendaja</span><span class="sxs-lookup"><span data-stu-id="f0c11-110">Electronic reporting developer</span></span>
    - <span data-ttu-id="f0c11-111">Elektroonilise aruandluse funktsionaalne konsultant</span><span class="sxs-lookup"><span data-stu-id="f0c11-111">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="f0c11-112">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="f0c11-112">System administrator</span></span>

- <span data-ttu-id="f0c11-113">Juurdepääs teenuse Regulatory Configuration Services (RCS) eksemplarile, mis on ette valmistatud sama rentniku jaoks, nagu rakendus Finance and Operations, ühe järgmise rolli jaoks:</span><span class="sxs-lookup"><span data-stu-id="f0c11-113">Access to the instance of Regulatory Configuration Services (RCS) that has been provisioned for the same tenant as Finance and Operations, for one of the following roles:</span></span>

    - <span data-ttu-id="f0c11-114">Elektroonilise aruandluse arendaja</span><span class="sxs-lookup"><span data-stu-id="f0c11-114">Electronic reporting developer</span></span>
    - <span data-ttu-id="f0c11-115">Elektroonilise aruandluse funktsionaalne konsultant</span><span class="sxs-lookup"><span data-stu-id="f0c11-115">Electronic reporting functional consultant</span></span>
    - <span data-ttu-id="f0c11-116">Süsteemiadministraator</span><span class="sxs-lookup"><span data-stu-id="f0c11-116">System administrator</span></span>

<span data-ttu-id="f0c11-117">Samuti peate alla laadima ja kohalikult talletama järgmised failid.</span><span class="sxs-lookup"><span data-stu-id="f0c11-117">You must also download and locally store the following files.</span></span>

| <span data-ttu-id="f0c11-118">Fail</span><span class="sxs-lookup"><span data-stu-id="f0c11-118">File</span></span>                                  | <span data-ttu-id="f0c11-119">Sisu</span><span class="sxs-lookup"><span data-stu-id="f0c11-119">Content</span></span>                               |
|---------------------------------------|---------------------------------------|
| <span data-ttu-id="f0c11-120">Performance trace model.version.1 (Jõudluse jälituse mudel, versioon 1)</span><span class="sxs-lookup"><span data-stu-id="f0c11-120">Performance trace model.version.1</span></span>     | [<span data-ttu-id="f0c11-121">ER-i andmemudeli konfiguratsiooni näide</span><span class="sxs-lookup"><span data-stu-id="f0c11-121">Sample ER data model configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)    |
| <span data-ttu-id="f0c11-122">Performance trace metadata.version.1 (Jõudluse jälituse metaandmed, versioon 1)</span><span class="sxs-lookup"><span data-stu-id="f0c11-122">Performance trace metadata.version.1</span></span>  | [<span data-ttu-id="f0c11-123">ER-i metaandmete konfiguratsiooni näide</span><span class="sxs-lookup"><span data-stu-id="f0c11-123">Sample ER metadata configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)      |
| <span data-ttu-id="f0c11-124">Performance trace mapping.version.1.1 (Jõudluse jälituse vastendus, versioon 1.1)</span><span class="sxs-lookup"><span data-stu-id="f0c11-124">Performance trace mapping.version.1.1</span></span> | [<span data-ttu-id="f0c11-125">ER-i mudelivastenduse konfiguratsiooni näide</span><span class="sxs-lookup"><span data-stu-id="f0c11-125">Sample ER model mapping configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| <span data-ttu-id="f0c11-126">Performance trace format.version.1.1 (Jõudluse jälituse vorming, versioon 1.1)</span><span class="sxs-lookup"><span data-stu-id="f0c11-126">Performance trace format.version.1.1</span></span>  | [<span data-ttu-id="f0c11-127">ER-vormingu konfiguratsiooni näide</span><span class="sxs-lookup"><span data-stu-id="f0c11-127">Sample ER format configuration</span></span>](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg)       |

### <a name="configure-er-parameters"></a><span data-ttu-id="f0c11-128">Elektroonilise aruandluse parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="f0c11-128">Configure ER parameters</span></span>

<span data-ttu-id="f0c11-129">Iga ER-i jõudluse jälg, mis luuakse rakenduses Finance and Operations, salvestatakse käivituslogi kirje manusena.</span><span class="sxs-lookup"><span data-stu-id="f0c11-129">Each ER performance trace that is generated in Finance and Operations is stored as an attachment of the execution log record.</span></span> <span data-ttu-id="f0c11-130">Nende manuste haldamiseks kasutatakse rakenduse Finance and Operations dokumendihalduse raamistikku.</span><span class="sxs-lookup"><span data-stu-id="f0c11-130">The Document management (DM) framework of Finance and Operations is used to manage these attachments.</span></span> <span data-ttu-id="f0c11-131">Peate konfigureerima ER-i parameetreid varem, et määrata dokumendihalduse dokumendi tüüp, mida tuleks kasutada jõudluse jälgede manustamiseks.</span><span class="sxs-lookup"><span data-stu-id="f0c11-131">You must configure ER parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="f0c11-132">Valige rakenduse Finance and Operations tööruumis **Elektrooniline aruandlus** suvand **Elektroonilise aruandluse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-132">In Finance and Operation, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="f0c11-133">Seejärel valige lehe **Elektroonilise aruandluse parameetrid** vahekaardi **Manused** väljal **Muud** dokumendihalduse dokumendi tüüp, mida tuleks kasutada jõudluse jälitusteks.</span><span class="sxs-lookup"><span data-stu-id="f0c11-133">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![Elektroonilise aruandluse parameetrite leht rakenduses Finance and Operations](./media/GER-PerfTrace-GER-Parameters-DocumentType.png)

<span data-ttu-id="f0c11-135">Selleks, et dokumendihalduse dokumenditüüp oleks otsinguväljal **Muud** saadaval, peab dokumendihalduse dokumenditüüp olema lehel **Dokumenditüübid** konfigureeritud järgmisel viisil (**Organisatsiooni haldus \> Dokumendihaldus \> Dokumenditüübid**).</span><span class="sxs-lookup"><span data-stu-id="f0c11-135">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="f0c11-136">**Klass:** manusfail</span><span class="sxs-lookup"><span data-stu-id="f0c11-136">**Class:** Attach file</span></span>
- <span data-ttu-id="f0c11-137">**Grupp:** fail</span><span class="sxs-lookup"><span data-stu-id="f0c11-137">**Group:** File</span></span>

![Dokumenditüüpide leht rakenduses Finance and Operations](./media/GER-PerfTrace-DM-DocumentType.png)

> [!NOTE]
> <span data-ttu-id="f0c11-139">Valitud dokumenditüüp peab olema praeguse rakenduse Finance and Operations eksemplari igas ettevõttes saadaval, kuna dokumendihalduse manused on ettevõttekohased.</span><span class="sxs-lookup"><span data-stu-id="f0c11-139">The selected document type must be available in every company of the current Finance and Operations instance, because DM attachments are company-specific.</span></span>

### <a name="configure-rcs-parameters"></a><span data-ttu-id="f0c11-140">RCS-i parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="f0c11-140">Configure RCS parameters</span></span>

<span data-ttu-id="f0c11-141">ER-i jõudluse jäljed, mis on loodud rakenduses Finance and Operations, imporditakse analüüsimiseks RCS-i, kasutades ER-vormingu kujundajat ja ER-i mudelivastenduse kujundajat.</span><span class="sxs-lookup"><span data-stu-id="f0c11-141">ER performance traces that are generated in Finance and Operations will be imported into RCS for analysis by using the ER format designer and the ER mapping designer.</span></span> <span data-ttu-id="f0c11-142">Kuna ER-i jõudluse jäljed salvestatakse ER-vorminguga seotud käivituslogi kirje manustena, peate konfigureerima RCS-i parameetreid ette, et määrata dokumendihalduse dokumenditüüp, mida tuleks kasutada jõudluse jälje manustamiseks.</span><span class="sxs-lookup"><span data-stu-id="f0c11-142">Because ER performance traces are stored as attachments of the execution log record that is related to the ER format, you must configure RCS parameters in advance, to specify the DM document type that should be used to attach performance traces.</span></span> <span data-ttu-id="f0c11-143">Valige RCS-i eksemplari, mis on teie ettevõtte jaoks ette valmistatud, tööruumis **Elektrooniline aruandlus** suvand **Elektroonilise aruandluse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-143">In the instance of RCS that has been provisioned for your company, in the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span> <span data-ttu-id="f0c11-144">Seejärel valige lehe **Elektroonilise aruandluse parameetrid** vahekaardi **Manused** väljal **Muud** dokumendihalduse dokumendi tüüp, mida tuleks kasutada jõudluse jälitusteks.</span><span class="sxs-lookup"><span data-stu-id="f0c11-144">Then, on the **Electronic reporting parameters** page, on the **Attachments** tab, in the **Others** field, select the DM document type to use for performance traces.</span></span>

![Elektroonilise aruandluse parameetrite leht RCS-is](./media/GER-PerfTrace-RCS-Parameters-DocumentType.png)

<span data-ttu-id="f0c11-146">Selleks, et dokumendihalduse dokumenditüüp oleks otsinguväljal **Muud** saadaval, peab dokumendihalduse dokumenditüüp olema lehel **Dokumenditüübid** konfigureeritud järgmisel viisil (**Organisatsiooni haldus \> Dokumendihaldus \> Dokumenditüübid**).</span><span class="sxs-lookup"><span data-stu-id="f0c11-146">To be available in the **Others** lookup field, a DM document type must be configured in the following manner on the **Document types** page (**Organization administration \> Document management \> Document types**):</span></span>

- <span data-ttu-id="f0c11-147">**Klass:** manusfail</span><span class="sxs-lookup"><span data-stu-id="f0c11-147">**Class:** Attach file</span></span>
- <span data-ttu-id="f0c11-148">**Grupp:** fail</span><span class="sxs-lookup"><span data-stu-id="f0c11-148">**Group:** File</span></span>

## <a name="design-an-er-solution"></a><span data-ttu-id="f0c11-149">ER-i lahenduse kujundamine</span><span class="sxs-lookup"><span data-stu-id="f0c11-149">Design an ER solution</span></span>

<span data-ttu-id="f0c11-150">Oletame, et olete alustanud uue ER-i lahenduse kujundamist, et luua uus hankija kandeid esitav aruanne.</span><span class="sxs-lookup"><span data-stu-id="f0c11-150">Assume that you've started to design a new ER solution to generate a new report that presents vendor transactions.</span></span> <span data-ttu-id="f0c11-151">Praegu leiate valitud hankija kanded lehel **Hankija kanded** (avage **Ostureskontro \> Hankijad \> Kõik hankijad**, valige hankija ja seejärel valige toimingupaanil vahekaardi **Hankija** grupis **Kanded** suvand **Kanded**).</span><span class="sxs-lookup"><span data-stu-id="f0c11-151">Currently, you can find the transactions for a selected vendor on the **Vendor transactions** page (go to **Account payable \> Vendors \> All vendors**, select a vendor, and then, on the Action Pane, on the **Vendor** tab, in the **Transactions** group, select **Transactions**).</span></span> <span data-ttu-id="f0c11-152">Kuid teil on vaja, et kõik hankija kanded oleksid samal ajal ühes elektroonilises dokumendis XML-vormingus.</span><span class="sxs-lookup"><span data-stu-id="f0c11-152">However, you want to have all vendor transaction at the same time in one electronic document in XML format.</span></span> <span data-ttu-id="f0c11-153">See lahendus koosneb mitmest ER-i konfiguratsioonist, mis sisaldavad nõutud andmemudelit, metaandmeid, mudelivastendust ja vormingu komponente.</span><span class="sxs-lookup"><span data-stu-id="f0c11-153">This solution will consist of several ER configurations that contain the required data model, metadata, model mapping, and format components.</span></span>

1. <span data-ttu-id="f0c11-154">Logige sisse RCS-i eksemplari, mis on teie ettevõtte jaoks ette valmistatud.</span><span class="sxs-lookup"><span data-stu-id="f0c11-154">Sign in to the instance of RCS that has been provisioned for your company.</span></span>
2. <span data-ttu-id="f0c11-155">Selles õppetükis loote näidisettevõtte **Litware, Inc** jaoks konfiguratsioonid ja muudate neid.</span><span class="sxs-lookup"><span data-stu-id="f0c11-155">In this tutorial, you will create and modify configurations for the **Litware, Inc.** sample company.</span></span> <span data-ttu-id="f0c11-156">Seetõttu veenduge, et see konfiguratsiooni pakkuja oleks RCS-i lisatud ja aktiivsena valitud.</span><span class="sxs-lookup"><span data-stu-id="f0c11-156">Therefore, make sure that this configuration provider has been added to RCS and selected as active.</span></span> <span data-ttu-id="f0c11-157">Juhiste saamiseks vaadake teemat [Konfiguratsiooni pakkujate loomine ja nende aktiivseks märkimine](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span><span class="sxs-lookup"><span data-stu-id="f0c11-157">For instructions, see the [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11) procedure.</span></span>
3. <span data-ttu-id="f0c11-158">Tööruumis **Elektrooniline aruandlus** valige paan **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-158">In the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
4. <span data-ttu-id="f0c11-159">Importige lehel **Konfiguratsioonid** ER-i konfiguratsioonid, mille eeltingimusena RCS-i alla laadisite, järgmises järjestuses: andmemudel, metaandmed, mudelivastendus, vorming.</span><span class="sxs-lookup"><span data-stu-id="f0c11-159">On the **Configurations** page, import the ER configurations that you downloaded as a prerequisite into RCS, in the following order: data model, metadata, model mapping, format.</span></span> <span data-ttu-id="f0c11-160">Toimige iga konfiguratsiooni puhul järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="f0c11-160">For each configuration, follow these steps:</span></span>

    1. <span data-ttu-id="f0c11-161">Valige toimingupaanil suvand **Rahavahetus \> Laadi XML-failist**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-161">On the Action Pane, select **Exchange \> Load from XML file**.</span></span>
    2. <span data-ttu-id="f0c11-162">Valige käsk **Sirvi**, et valida nõutava ER-i konfiguratsiooni jaoks sobiv fail XML-vormingus.</span><span class="sxs-lookup"><span data-stu-id="f0c11-162">Select **Browse** to select the appropriate file for the required ER configuration in XML format.</span></span>
    3. <span data-ttu-id="f0c11-163">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-163">Select **OK**.</span></span>

    ![Konfiguratsioonide leht RCS-is](./media/GER-PerfTrace-RCS-ImportedConfigurations.png)

## <a name="run-the-er-solution-to-trace-execution"></a><span data-ttu-id="f0c11-165">ER-i lahenduse kasutamine täitmise jälituseks</span><span class="sxs-lookup"><span data-stu-id="f0c11-165">Run the ER solution to trace execution</span></span>

<span data-ttu-id="f0c11-166">Oletame, et olete lõpetanud ER-i lahenduse esimese versiooni kujundamise.</span><span class="sxs-lookup"><span data-stu-id="f0c11-166">Assume that you've finished designing the first version of the ER solution.</span></span> <span data-ttu-id="f0c11-167">Nüüd soovite seda testida oma rakenduse Finance and Operations eksemplaris ja analüüsida täitmise jõudlust.</span><span class="sxs-lookup"><span data-stu-id="f0c11-167">You now want to test it in your Finance and Operations instance and analyze execution performance.</span></span>

### <a id='import-configuration'></a><span data-ttu-id="f0c11-168">ER-i konfiguratsiooni importimine RCS-ist rakendusse Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f0c11-168">Import an ER configuration from RCS into Finance and Operations</span></span>

1. <span data-ttu-id="f0c11-169">Logige oma Finance and Operationsi eksemplari sisse.</span><span class="sxs-lookup"><span data-stu-id="f0c11-169">Sign in to your Finance and Operations instance.</span></span>
2. <span data-ttu-id="f0c11-170">Selles õppetükis impordite konfiguratsioonid RCS-i eksemplarist (kus kujundate ER-i komponente) rakenduse Finance and Operations eksemplari (kus testite ja lõpuks neid kasutate).</span><span class="sxs-lookup"><span data-stu-id="f0c11-170">For this tutorial, you will import configurations from your RCS instance (where you design your ER components) into your Finance and Operations instance (where you test and finally use them).</span></span> <span data-ttu-id="f0c11-171">Seega peate veenduma, et kõik nõutud artefaktid oleksid ette valmistatud.</span><span class="sxs-lookup"><span data-stu-id="f0c11-171">Therefore, you must make sure that all the required artifacts have been prepared.</span></span> <span data-ttu-id="f0c11-172">Juhised leiate teemast [Elektroonilise aruandluse (ER) konfiguratsioonide importimine teenusest Regulatory Configuration Services (RCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations).</span><span class="sxs-lookup"><span data-stu-id="f0c11-172">For instructions, see the [Import Electronic reporting (ER) configurations from Regulatory Configuration Services (RCS)](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/rcs-download-configurations) procedure.</span></span>
3. <span data-ttu-id="f0c11-173">Järgige neid samme, et importida konfiguratsioonid RCS-ist rakendusse Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f0c11-173">Follow these steps to import the configurations from RCS into Finance and Operations:</span></span>

    1. <span data-ttu-id="f0c11-174">Valige tööruumi **Elektrooniline aruandlus** konfiguratsiooni pakkuja **Litware, Inc.** paanilt valik **Hoidlad**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-174">In the **Electronic reporting** workspace, on the tile for the **Litware, Inc.** configuration provider, select **Repositories**.</span></span>
    2. <span data-ttu-id="f0c11-175">Valige lehel **Konfiguratsioonihoidla** hoidla tüübiga **RCS** ja seejärel valige käsk **Ava**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-175">On the **Configuration repository** page, select the repository of the **RCS** type, and then select **Open**.</span></span>
    3. <span data-ttu-id="f0c11-176">Valige kiirkaardil **Konfiguratsioonid** konfiguratsioon **Jõudluse jälituse vorming**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-176">On the **Configurations** FastTab, select the **Performance trace format** configuration.</span></span>
    4. <span data-ttu-id="f0c11-177">Valige kiirkaardil **Versioonid** valitud konfiguratsiooni versioon **1.1** ja seejärel käsk **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-177">On the **Versions** FastTab, select version **1.1** of the selected configuration, and then select **Import**.</span></span>

    ![Konfiguratsioonihoidla leht rakenduses Finance and Operations](./media/GER-PerfTrace-GER-ImportedConfigurations.png)

<span data-ttu-id="f0c11-179">Andmemudeli ja mudelivastenduse vastavate versioonide konfiguratsioonid imporditakse eeltingimustena automaatselt imporditud ER-vormingu konfiguratsioonile.</span><span class="sxs-lookup"><span data-stu-id="f0c11-179">The corresponding versions of the data model and model mapping configurations are automatically imported as prerequisites for the imported ER format configuration.</span></span>

### <a name="turn-on-the-er-performance-trace"></a><span data-ttu-id="f0c11-180">ER-i jõudluse jälituse sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="f0c11-180">Turn on the ER performance trace</span></span>

1. <span data-ttu-id="f0c11-181">Avage rakenduses Finance and Operations **Organisatsiooni haldus \> Elektrooniline aruandlus \> Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-181">In Finance and Operations, go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="f0c11-182">Valige lehe **Konfiguratsioonid** toimingupaani vahekaardi **Konfiguratsioonid** grupist **Täpsemad sätted** valik **Kasutaja parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-182">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="f0c11-183">Toimige dialoogiboksi **Kasutaja parameetrid** jaotises **Täitmise jälitus** järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="f0c11-183">In the **User parameters** dialog box, in the **Execution tracing** section, follow these steps:</span></span>

    1. <span data-ttu-id="f0c11-184">Valige väljal **Täitmise jälituse vorming** valik **Jälituse vormingu silumine**, et alustada ER-vormingu täitmise üksikasjade kogumist.</span><span class="sxs-lookup"><span data-stu-id="f0c11-184">In the **Execution trace format** field, select **Debug trace format** to start to collect the details of ER format execution.</span></span> <span data-ttu-id="f0c11-185">Kui see väärtus on valitud, kogub jõudluse jälitus teavet järgmistele toimingutele kulutatud aja kohta.</span><span class="sxs-lookup"><span data-stu-id="f0c11-185">When this value is selected, the performance trace will collect information about the time that is spent on the following actions:</span></span>

        - <span data-ttu-id="f0c11-186">Iga andmeallika käitamine mudelivastendusel, mida kutsutakse andmeid tooma</span><span class="sxs-lookup"><span data-stu-id="f0c11-186">Running each data source in the model mapping that is called to get data</span></span>
        - <span data-ttu-id="f0c11-187">Iga vormingu üksuse töötlemine andmete sisestamiseks loodavasse väljundisse</span><span class="sxs-lookup"><span data-stu-id="f0c11-187">Processing each format item to enter data in the output that is generated</span></span>

        <span data-ttu-id="f0c11-188">Välja **Täitmise jälituse vorming** kasutate selleks, et määrata loodud jõudluse jäljele vorming, milles talletatakse täitmise üksikasjad ER-vormingu ja vastendamise elementide jaoks.</span><span class="sxs-lookup"><span data-stu-id="f0c11-188">You use the **Execution trace format** field to specify the format of the generated performance trace that the execution details are stored in for ER format and mapping elements.</span></span> <span data-ttu-id="f0c11-189">Kui valite väärtuseks **Jälituse vormingu silumine**, saate analüüsida jälje sisu ER-i toimingukoostajas ja näha ER-vorminguid või vastendamise elemente, mis on jäljes mainitud.</span><span class="sxs-lookup"><span data-stu-id="f0c11-189">By selecting **Debug trace format** as the value, you will be able to analyze the content of the trace in ER Operation designer, and see the ER format or mapping elements that are mentioned in the trace.</span></span>

    2. <span data-ttu-id="f0c11-190">Määrake järgmiste suvandite olekuks **Jah**, et koguda kindlaid üksikasju ER-i mudelivastenduse ja ER-vormingu komponentide täitmise kohta.</span><span class="sxs-lookup"><span data-stu-id="f0c11-190">Set the following options to **Yes** to collect specific details of the execution of the ER model mapping and ER format components:</span></span>

        - <span data-ttu-id="f0c11-191">**Päringustatistika sissenõudmine** – kui see valik on sisse lülitatud, kogub jõudluse jälitus järgmist teavet.</span><span class="sxs-lookup"><span data-stu-id="f0c11-191">**Collect query statistics** – When this option is turned on, the performance trace will collect the following information:</span></span>

            - <span data-ttu-id="f0c11-192">Andmeallikate tehtud andmebaasi kutsete arv</span><span class="sxs-lookup"><span data-stu-id="f0c11-192">The number of database calls that were made by data sources</span></span>
            - <span data-ttu-id="f0c11-193">Korduvate kutsete arv andmebaasi</span><span class="sxs-lookup"><span data-stu-id="f0c11-193">The number of duplicate calls to the database</span></span>
            - <span data-ttu-id="f0c11-194">Andmebaasi kutsete tegemiseks kasutatud SQL-i lausete üksikasjad</span><span class="sxs-lookup"><span data-stu-id="f0c11-194">Details of the SQL statements that were used to make database calls</span></span>

        - <span data-ttu-id="f0c11-195">**Jälita vahemälule juurdepääsu** – kui see valik on sisse lülitatud, kogub jõudluse jälitus teavet ER-i mudelivastenduse vahemälu kasutuse kohta.</span><span class="sxs-lookup"><span data-stu-id="f0c11-195">**Trace access of caching** – When this option is turned on, the performance trace will collect information about the ER model mapping's cache usage.</span></span>
        - <span data-ttu-id="f0c11-196">**Jälita andmete juurdepääsu** – kui see valik on sisse lülitatud, kogub jõudluse jälitus teavet andmebaasi kutsete arvu kohta, mis on tehtud kirjeloendi tüüpi täidetud andmeallikate jaoks.</span><span class="sxs-lookup"><span data-stu-id="f0c11-196">**Trace data access** – When this option is turned on, the performance trace will collect information about the number of calls to the database for executed data sources of the record list type.</span></span>
        - <span data-ttu-id="f0c11-197">**Jälita loendi loetelu** – kui see valik on sisse lülitatud, kogub jõudluse jälitus teavet kirjete arvu kohta, mis on taotletud kirjeloendi tüüpi andmeallikatest.</span><span class="sxs-lookup"><span data-stu-id="f0c11-197">**Trace list enumeration** – When this option is turned on, the performance trace will collect information about the number of records that are requested from data sources of the record list type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="f0c11-198">Dialoogiboksi **Kasutaja parameetrid** parameetrid kehtivad konkreetsele kasutajale ja praegusele ettevõttele.</span><span class="sxs-lookup"><span data-stu-id="f0c11-198">The parameters in the **User parameters** dialog box are specific to the user and the current company.</span></span>

    ![Kasutaja parameetrite dialoogiboks rakenduses Finance and Operations](./media/GER-PerfTrace-GER-UserParameters.png)

### <a id='run-format'></a><span data-ttu-id="f0c11-200">ER-vormingu käivitamine</span><span class="sxs-lookup"><span data-stu-id="f0c11-200">Run the ER format</span></span>

1. <span data-ttu-id="f0c11-201">Valige rakenduses Finance and Operations ettevõte **DEMF**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-201">In Finance and Operations, select the **DEMF** company.</span></span>
2. <span data-ttu-id="f0c11-202">Minge jaotisse **Organisatsiooni haldamine \> Elektrooniline aruandlus \> Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-202">Go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
3. <span data-ttu-id="f0c11-203">Valige lehe **Konfiguratsioonid** konfiguratsioonipuult üksus **Jõudluse jälituse vorming**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-203">On the **Configurations** page, in the configuration tree, select the **Performance trace format** item.</span></span>
4. <span data-ttu-id="f0c11-204">Valige toimingupaanil käsk **Käivita**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-204">On the Action Pane, select **Run**.</span></span>

<span data-ttu-id="f0c11-205">Pange tähele, et loodud fail esitab teavet kuue hankija 265 kande kohta.</span><span class="sxs-lookup"><span data-stu-id="f0c11-205">Notice that the file that is generated presents information about 265 transactions for six vendors.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="f0c11-206">Täitmise jälje läbivaatus</span><span class="sxs-lookup"><span data-stu-id="f0c11-206">Review the execution trace</span></span>

### <a id='export-trace'></a><span data-ttu-id="f0c11-207">Loodud jälje eksportimine rakendusest Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f0c11-207">Export the generated trace from Finance and Operations</span></span>

<span data-ttu-id="f0c11-208">Jõudluse jäljed lahutatakse ER-vormingu allikast ja neid saab järjestada välisele ZIP-failile.</span><span class="sxs-lookup"><span data-stu-id="f0c11-208">Performance traces are decoupled from the source ER format and can be serialized to an external zip file.</span></span>

1. <span data-ttu-id="f0c11-209">Avage rakenduses Finance and Operations **Organisatsiooni haldus \> Elektrooniline aruandlus \> Konfiguratsiooni silumislogid**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-209">In Finance and Operations, go to **Organization administration \> Electronic reporting \> Configuration debug logs**.</span></span>
2. <span data-ttu-id="f0c11-210">Valige lehe **Elektroonilise aruandluse käivituslogid** vasakpoolsel paanil **Konfiguratsiooni nimi** valik **Jõudluse jälituse vorming**, et leida logi kirjed, mis on loodud konfiguratsiooni **Jõudluse jälituse vorming** täitmisega.</span><span class="sxs-lookup"><span data-stu-id="f0c11-210">On the **Electronic reporting run logs** page, in the left pane, in the **Configuration name** field, select **Performance trace format** to find the log records that have been generated by the execution of the **Performance trace format** configuration.</span></span>
3. <span data-ttu-id="f0c11-211">Valige lehe paremas ülanurgas nupp **Manused** (kirjaklambrisümbol) või vajutage klahve **Ctrl + Shift + A**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-211">Select the **Attachments** button (the paper clip symbol) in the upper-right corner of the page, or press **Ctrl+Shift+A**.</span></span>

    ![Rakenduse Finance and Operations lehe Elektroonilise aruandluse käitamise logid nupp Manused](./media/GER-PerfTrace-GER-DebugLog.png)

4. <span data-ttu-id="f0c11-213">Valige lehe **Elektroonilise aruandluse käitamise logide manused** toimingupaanil käsk **Ava**, et saada jõudluse jälg ZIP-failina ja seda kohalikult talletada.</span><span class="sxs-lookup"><span data-stu-id="f0c11-213">On the **Attachments for Electronic reporting run logs** page, on the Action Pane, select **Open** to get the performance trace as a zip file and store it locally.</span></span>

    ![Rakenduse Finance and Operations leht Elektroonilise aruandluse käitamise logide manused](./media/GER-PerfTrace-GER-DebugLog-AttachedTrace.png)

> [!NOTE]
> <span data-ttu-id="f0c11-215">Loodud jäljel on viide allika ER-i aruandele kordumatu aruande identifikaatori kaudu ainult **GUID**-vormingus.</span><span class="sxs-lookup"><span data-stu-id="f0c11-215">The trace that is generated has a reference to the source ER report via a unique report identifier in **GUID** format only.</span></span> <span data-ttu-id="f0c11-216">Vormingu versiooni nummerdamist ei arvestata.</span><span class="sxs-lookup"><span data-stu-id="f0c11-216">The version numbering of the format isn't considered.</span></span>

<span data-ttu-id="f0c11-217">Pange tähele, et täidetud ER-vormingu jaoks loodud jõudluse jälje ja ER-i mudelivastenduse vaheline seos põhineb kasutatud juurdeskriptoril ning üldisel andmemudelil.</span><span class="sxs-lookup"><span data-stu-id="f0c11-217">Notice that the association between the performance trace that has been generated for the executed ER format and the ER model mapping is based on the root descriptor that was used and the common data model.</span></span> <span data-ttu-id="f0c11-218">Vormingu ja mudelivastenduse versiooni nummerdamist ei arvestata.</span><span class="sxs-lookup"><span data-stu-id="f0c11-218">The version numbering of the format and model mapping isn't considered.</span></span> <span data-ttu-id="f0c11-219">Samuti ei arvestata mudelivastenduse lipu **Mudelivastenduse vaikeväärtus** sätet.</span><span class="sxs-lookup"><span data-stu-id="f0c11-219">The setting of the **Default for model mapping** flag for the model mapping also isn't considered.</span></span>

### <a id='import-trace'></a><span data-ttu-id="f0c11-220">Loodud jälje importimine RCS-i</span><span class="sxs-lookup"><span data-stu-id="f0c11-220">Import the generated trace into RCS</span></span>

1. <span data-ttu-id="f0c11-221">Valige RCS-i tööruumis **Elektrooniline aruandlus** paan **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-221">In RCS, in the **Electronic reporting** workspace, select the **Reporting configurations** tile.</span></span>
2. <span data-ttu-id="f0c11-222">Laiendage lehe **Konfiguratsioonid** konfiguratsioonipuul üksust **Jõudluse jälituse mudel** ja valige üksus **Jõudluse jälituse vorming**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-222">On the **Configurations** page, in the configuration tree, expand the **Performance trace model** item, and select the **Performance trace format** item.</span></span>
3. <span data-ttu-id="f0c11-223">Valige toimingupaanil valik **Koostaja**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-223">On the Action Pane, select **Designer**.</span></span>
4. <span data-ttu-id="f0c11-224">Valige lehe **Vormingu koostaja** toimingupaanil **Jõudluse jälitus**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-224">On the **Format designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="f0c11-225">Valige dialoogiaknas **Jõudluse jälituse tulemuste sätted** valik **Impordi jõudluse jälg**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-225">In the **Performance trace result settings** dialog box, select **Import performance trace**.</span></span>
6. <span data-ttu-id="f0c11-226">Valige käsk **Sirvi**, et valida ZIP-fail, mida eksportisite varem rakendusest Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f0c11-226">Select **Browse** to select the zip file that you exported from Finance and Operations earlier.</span></span>
7. <span data-ttu-id="f0c11-227">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-227">Select **OK**.</span></span>

    ![Jõudluse jälituse tulemuse sätete dialoogiboks RCS-is](./media/GER-PerfTrace-RCS-ImportedPerfTrace.png)

### <a name="use-the-performance-trace-for-analysis-in-rcs--format-execution"></a><span data-ttu-id="f0c11-229">Jõudluse jälituse kasutamine analüüsiks RCS-is – vormingu täitmine</span><span class="sxs-lookup"><span data-stu-id="f0c11-229">Use the performance trace for analysis in RCS – Format execution</span></span>

1. <span data-ttu-id="f0c11-230">Valige RCS-is lehel **Vormingu koostaja** käsk **Laienda/ahenda**, et laiendada kõigi vormingu üksuste sisu.</span><span class="sxs-lookup"><span data-stu-id="f0c11-230">In RCS, on the **Format designer** page, select **Expand/collapse** to expand the content of all format items.</span></span>

    <span data-ttu-id="f0c11-231">Pange tähele, et praeguse vormingu mõne üksuse kohta kuvatakse lisateavet.</span><span class="sxs-lookup"><span data-stu-id="f0c11-231">Notice that additional information is shown for some items of the current format:</span></span>

    - <span data-ttu-id="f0c11-232">Tegelik aeg, mis kulus andmete sisestamiseks loodud väljundisse kasutades vormingu üksust</span><span class="sxs-lookup"><span data-stu-id="f0c11-232">The actual time that was spent entering data in the generated output by using the format item</span></span>
    - <span data-ttu-id="f0c11-233">Sama aeg väljendatuna protsendina koguajast, mis kulutati kogu väljundi loomiseks</span><span class="sxs-lookup"><span data-stu-id="f0c11-233">The same time expressed as a percentage of the total time that was spent generating the whole output</span></span>

    ![Vormingu koostaja leht RCS-is](./media/GER-PerfTrace-RCS-TraceInfoInFormat.png)

2. <span data-ttu-id="f0c11-235">Sulgege **Vormingu koostaja** leht.</span><span class="sxs-lookup"><span data-stu-id="f0c11-235">Close **Format designer** page.</span></span>

### <a id='use-trace'></a><span data-ttu-id="f0c11-236">Jõudluse jälituse kasutamine analüüsiks RCS-is – mudelivastendus</span><span class="sxs-lookup"><span data-stu-id="f0c11-236">Use the performance trace for analysis in RCS – Model mapping</span></span>

1. <span data-ttu-id="f0c11-237">Valige RCS-is lehe **Konfiguratsioonid** konfiguratsioonipuult üksus **Jõudluse jälituse vastendus**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-237">In RCS, on the **Configurations** page, in the configuration tree, select the **Performance trace mapping** item.</span></span>
2. <span data-ttu-id="f0c11-238">Valige toimingupaanil valik **Koostaja**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-238">On the Action Pane, select **Designer**.</span></span>
3. <span data-ttu-id="f0c11-239">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-239">Select **Designer**.</span></span>
4. <span data-ttu-id="f0c11-240">Valige lehe **Mudelivastenduse koostaja** toimingupaanil **Jõudluse jälitus**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-240">On the **Model mapping designer** page, on the Action Pane, select **Performance trace**.</span></span>
5. <span data-ttu-id="f0c11-241">Valige jälg, mille varem importisite.</span><span class="sxs-lookup"><span data-stu-id="f0c11-241">Select the trace that you imported earlier.</span></span>
6. <span data-ttu-id="f0c11-242">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-242">Select **OK**.</span></span>

<span data-ttu-id="f0c11-243">Pange tähele, et praeguse mudelivastenduse mõne andmeallika üksuse kohta muutub kättesaadavaks uus teave.</span><span class="sxs-lookup"><span data-stu-id="f0c11-243">Notice that new information becomes available for some data source items of the current model mapping:</span></span>

- <span data-ttu-id="f0c11-244">Tegelik aeg, mis kulus andmeallika abil andmete toomisele</span><span class="sxs-lookup"><span data-stu-id="f0c11-244">The actual time that was spent getting data by using the data source</span></span>
- <span data-ttu-id="f0c11-245">Sama aeg väljendatuna protsendina koguajast, mis kulutati kogu mudelivastenduse käitamise peale</span><span class="sxs-lookup"><span data-stu-id="f0c11-245">The same time expressed as a percentage of the total time that was spent running the whole model mapping</span></span>

<span data-ttu-id="f0c11-246">Pange tähele, et ER annab teile teate, et praegune mudelivastendus dubleerib andmebaasi taotlusi ajal, mil andmeallikat VendTable/\<Relations/VendTrans.VendTable\_AccountNum käitatakse.</span><span class="sxs-lookup"><span data-stu-id="f0c11-246">Notice that ER informs you that the current model mapping duplicates database requests while the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source is run.</span></span> <span data-ttu-id="f0c11-247">Dubleerimine toimub seetõttu, et hankija kannete loendit kutsutakse iga itereeritud hankija kirje puhul kaks korda.</span><span class="sxs-lookup"><span data-stu-id="f0c11-247">This duplication occurs because the list of vendor transactions is called two times for each iterated vendor record:</span></span>

- <span data-ttu-id="f0c11-248">Üks kutse tehakse, et sisestada andmemudelis iga kande üksikasjad konfigureeritud sidumiste alusel.</span><span class="sxs-lookup"><span data-stu-id="f0c11-248">One call is made to enter details of each transaction in the data model, based on configured bindings.</span></span>
- <span data-ttu-id="f0c11-249">Teine kutse tehakse, et sisestada andmemudelis iga hankija kohta arvutatud kannete arv.</span><span class="sxs-lookup"><span data-stu-id="f0c11-249">One call is made to enter the calculated number of transactions per vendor in the data model.</span></span>

![Teade dubleeritud andmebaasi taotluste kohta mudelivastenduse koostaja lehel RCS-is](./media/GER-PerfTrace-RCS-TraceInfoInMapping1.png)

<span data-ttu-id="f0c11-251">Väärtus **\[Q:530\]** näitab, et tabelit VendTrans kutsuti 530 korda, et tagastada sellest tabelist kirje andmeallikasse VendTable/\<Relations/VendTrans.VendTable\_AccountNum.</span><span class="sxs-lookup"><span data-stu-id="f0c11-251">The value **\[Q:530\]** indicates that the VendTrans table was called 530 times to return a record from that table to the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source.</span></span> <span data-ttu-id="f0c11-252">Väärtus **\[530\]** näitab, et andmeallikat VendTable/\<Relations/VendTrans.VendTable\_AccountNum kutsuti 530 korda, et tagastada kirje sellest andmeallikast ja sisestada selle üksikasjad andmemudelisse.</span><span class="sxs-lookup"><span data-stu-id="f0c11-252">The value **\[530\]** indicates that the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source was called 530 times to return a record from that data source and enter the details from it in the data model.</span></span>

<span data-ttu-id="f0c11-253">Soovitame kasutada andmeallika VendTable/\<Relations/VendTrans.VendTable\_AccountNum jaoks vahemällusalvestust, et vähendada kutsete arvu, mida tehakse 265 kande üksikasjade saamiseks, ja aidata parandada mudelivastenduse jõudlust.</span><span class="sxs-lookup"><span data-stu-id="f0c11-253">We recommend that you use caching for the VendTable/\<Relations/VendTrans.VendTable\_AccountNum data source, to reduce the number of calls that are made to get the details for 265 transactions and help improve the performance of the model mapping.</span></span>

<span data-ttu-id="f0c11-254">Samuti võib see olla kasulik. et vähendada andmeallikale LedgerTransTypeList tehtud kutsumiste arvu.</span><span class="sxs-lookup"><span data-stu-id="f0c11-254">It can also be useful to reduce the number of calls that are made to the LedgerTransTypeList data source.</span></span> <span data-ttu-id="f0c11-255">Seda andmeallikat kasutatakse **LedgerTransType**-i nummerdamise iga väärtuse seostamiseks oma sildiga.</span><span class="sxs-lookup"><span data-stu-id="f0c11-255">This data source is used to associate each value of the **LedgerTransType** enumeration with its label.</span></span> <span data-ttu-id="f0c11-256">Seda andmeallikat kasutades saate leida sobiva sildi ja seda andmeallikasse iga hankija kande jaoks sisestada.</span><span class="sxs-lookup"><span data-stu-id="f0c11-256">By using this data source, you can find an appropriate label and enter it in the data model for each vendor transaction.</span></span> <span data-ttu-id="f0c11-257">Praegune kutsete arv sellele andmeallikale (9027) on 265 kande kohta üsna kõrge.</span><span class="sxs-lookup"><span data-stu-id="f0c11-257">The current number of calls to this data source (9,027) is quite high for 265 transactions.</span></span>

![Mudelivastenduse koostaja leht RCS-is, mis näitab 9027 kutset andmeallikale](./media/GER-PerfTrace-RCS-TraceInfoInMapping1a.png)

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a><span data-ttu-id="f0c11-259">Mudelivastenduse parandamine täitmise jälitusest saadud teabe põhjal</span><span class="sxs-lookup"><span data-stu-id="f0c11-259">Improve the model mapping based on information from the execution trace</span></span>

### <a name="modify-the-logic-of-the-model-mapping"></a><span data-ttu-id="f0c11-260">Mudelivastenduse loogika muutmine</span><span class="sxs-lookup"><span data-stu-id="f0c11-260">Modify the logic of the model mapping</span></span>

1. <span data-ttu-id="f0c11-261">Järgige vahemälu kasutamiseks järgmisi samme, et vältida andmebaasi dubleeritud kutseid.</span><span class="sxs-lookup"><span data-stu-id="f0c11-261">Follow these steps to use caching, to help prevent duplicate calls to the database:</span></span>

    1. <span data-ttu-id="f0c11-262">Valige RCS-is lehe **Mudelivastenduse koostaja** paanil **Andmeallikad** üksus **VendTable**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-262">In RCS, on the **Model mapping designer** page, in the **Data sources** pane, select the **VendTable** item.</span></span>
    2. <span data-ttu-id="f0c11-263">Valige suvand **Vahemälu**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-263">Select **Cache**.</span></span>
    3. <span data-ttu-id="f0c11-264">Laiendage üksust **VendTable**, laiendage andmeallika VendTable üks-mitmele seoste loendit (üksus **\<Seosed**) ja valige üksus **VendTrans.VendTable\_AccountNum**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-264">Expand the **VendTable** item, expand the list of one-to-many relations for the VendTable data source (the **\<Relations** item), and select the **VendTrans.VendTable\_AccountNum** item.</span></span>
    4. <span data-ttu-id="f0c11-265">Valige suvand **Vahemälu**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-265">Select **Cache**.</span></span>

    ![Vahemälu häälestus, mis aitab vältida dubleeritud kutseid](./media/GER-PerfTrace-RCS-ChangeMapping-Cache.png)

2. <span data-ttu-id="f0c11-267">Järgige neid samme, et tuua andmeallikas LedgerTransTypeList andmeallika VendTable ulatusse.</span><span class="sxs-lookup"><span data-stu-id="f0c11-267">Follow these steps to bring the LedgerTransTypeList data source into the scope of the VendTable data source:</span></span>

    1. <span data-ttu-id="f0c11-268">Laiendage paanil **Andmeallika tüübid** üksust **Funktsioonid** ja valige üksus **Arvutatud väli**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-268">In the **Data source types** pane, expand the **Functions** item, and select the **Calculated field** item.</span></span>
    2. <span data-ttu-id="f0c11-269">Valige paanil **Andmeallikad** üksus **VendTable**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-269">In the **Data sources** pane, select the **VendTable** item.</span></span>
    3. <span data-ttu-id="f0c11-270">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-270">Select **Add**.</span></span>
    4. <span data-ttu-id="f0c11-271">Sisestage väljale **Nimi** tekst **\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-271">In the **Name** field, enter **\$TransType**.</span></span>
    5. <span data-ttu-id="f0c11-272">Valige **Valemi redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-272">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="f0c11-273">Sisestage väljale **Valem** tekst **LedgerTransTypeList**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-273">In the **Formula** field, enter **LedgerTransTypeList**.</span></span>
    7. <span data-ttu-id="f0c11-274">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-274">Select **Save**.</span></span>
    8. <span data-ttu-id="f0c11-275">Sulgege leht **Valemiredaktor**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-275">Close the **Formula editor** page.</span></span>
    9. <span data-ttu-id="f0c11-276">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-276">Click **OK**.</span></span>

3. <span data-ttu-id="f0c11-277">Järgige neid samme, et kasutada vahemällusalvestust välja **\$TransType** jaoks.</span><span class="sxs-lookup"><span data-stu-id="f0c11-277">Follow these steps to do caching of the **\$TransType** field:</span></span>

    1. <span data-ttu-id="f0c11-278">Valige üksus **LedgerTransTypeList**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-278">Select the **LedgerTransTypeList** item.</span></span>
    2. <span data-ttu-id="f0c11-279">Valige suvand **Vahemälu**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-279">Select **Cache**.</span></span>
    3. <span data-ttu-id="f0c11-280">Valige üksus **VendTable.\$TransType**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-280">Select the **VendTable.\$TransType** item.</span></span>
    4. <span data-ttu-id="f0c11-281">Valige suvand **Vahemälu**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-281">Select **Cache**.</span></span>

    ![Vahemällusalvestuse seadistamine välja $TransType jaoks](./media/GER-PerfTrace-RCS-ChangeMapping-Cache2.png)

4. <span data-ttu-id="f0c11-283">Järgige neid samme, et muuta välja **\$TransTypeRecord** nii, et see hakkaks kasutama vahemällu salvestatud välja **\$TransType.**</span><span class="sxs-lookup"><span data-stu-id="f0c11-283">Follow these steps to change the **\$TransTypeRecord** field so that it starts to use the cached **\$TransType** field:</span></span>

    1. <span data-ttu-id="f0c11-284">Laiendage paanil **Andmeallikad** üksust **VendTable**, üksust**\<Seosed**, üksust **VendTrans.VendTable\_AccountNum** ja valige üksus **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-284">In the **Data sources** pane, expand the **VendTable** item, expand the **\<Relations** item, expand the **VendTrans.VendTable\_AccountNum** item, and select the **VendTable. VendTrans.VendTable\_AccountNum.\$TransTypeRecord** item.</span></span>
    2. <span data-ttu-id="f0c11-285">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-285">Select **Edit**.</span></span>
    3. <span data-ttu-id="f0c11-286">Valige **Valemi redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-286">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="f0c11-287">Leidke väljal **Valem** järgmine avaldis.</span><span class="sxs-lookup"><span data-stu-id="f0c11-287">In the **Formula** field, find the following expression:</span></span>

        <span data-ttu-id="f0c11-288">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span><span class="sxs-lookup"><span data-stu-id="f0c11-288">FIRSTORNULL (WHERE (LedgerTransTypeList, LedgerTransTypeList.Enum = \@.TransType))</span></span>

    5. <span data-ttu-id="f0c11-289">Sisestage väljale **Valem** järgmine avaldis.</span><span class="sxs-lookup"><span data-stu-id="f0c11-289">In the **Formula** field, enter the following expression:</span></span>

        <span data-ttu-id="f0c11-290">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span><span class="sxs-lookup"><span data-stu-id="f0c11-290">FIRSTORNULL (WHERE (VendTable.'\$TransType', VendTable.'\$TransType'.Enum = \@.TransType)).</span></span>

    6. <span data-ttu-id="f0c11-291">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-291">Select **Save**.</span></span>
    7. <span data-ttu-id="f0c11-292">Sulgege leht **Valemiredaktor**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-292">Close the **Formula editor** page.</span></span>
    8. <span data-ttu-id="f0c11-293">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-293">Select **OK**.</span></span>

5. <span data-ttu-id="f0c11-294">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-294">Select **Save**.</span></span>
6. <span data-ttu-id="f0c11-295">Sulgege leht **Mudelivastenduse koostaja**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-295">Close the **Model mapping designer** page.</span></span>
7. <span data-ttu-id="f0c11-296">Sulgege leht **Mudelivastendused**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-296">Close the **Model mappings** page.</span></span>

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a><span data-ttu-id="f0c11-297">ER-i mudelivastenduse muudetud versiooni lõpetamine</span><span class="sxs-lookup"><span data-stu-id="f0c11-297">Complete the modified version of the ER model mapping</span></span>

1. <span data-ttu-id="f0c11-298">Valige RCS-is lehe **Konfiguratsioonid** kiirkaardil **Versioonid** konfiguratsiooni **Jõudluse jälituse vastendus** versioon **1.2**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-298">In RCS, on the **Configurations** page, on the **Versions** FastTab, select version **1.2** of the **Performance trace mapping** configuration.</span></span>
2. <span data-ttu-id="f0c11-299">Valige käsk **Muuda olekut**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-299">Select **Change status**.</span></span>
3. <span data-ttu-id="f0c11-300">Valige **Lõpeta**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-300">Select **Complete**.</span></span>

### <a name="import-the-modified-er-model-mapping-configuration-from-rcs-into-finance-and-operations"></a><span data-ttu-id="f0c11-301">Muudetud ER-i mudelivastenduse konfiguratsiooni importimine RCS-ist rakendusse Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f0c11-301">Import the modified ER model mapping configuration from RCS into Finance and Operations</span></span>

<span data-ttu-id="f0c11-302">Korrake samme selle teema jaotises [ER-i konfiguratsiooni importimine RCS-ist rakendusse Finance and Operations](#import-configuration), et importida konfiguratsiooni **Jõudluse jälituse vastendus** versioon 1.2 rakendusse Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f0c11-302">Repeat the steps in the [Import an ER configuration from RCS into Finance and Operations](#import-configuration) section earlier in this topic to import version 1.2 of the **Performance trace mapping** configuration into Finance and Operations.</span></span>

## <a name="run-the-modified-er-solution-to-trace-execution"></a><span data-ttu-id="f0c11-303">Muudetud ER-i lahenduse kasutamine täitmise jälituseks</span><span class="sxs-lookup"><span data-stu-id="f0c11-303">Run the modified ER solution to trace execution</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="f0c11-304">ER-vormingu käivitamine</span><span class="sxs-lookup"><span data-stu-id="f0c11-304">Run the ER format</span></span>

<span data-ttu-id="f0c11-305">Korrake samme selle teema jaotises [ER-vormingu käivitamine](#run-format), et luua uus jõudluse jälg.</span><span class="sxs-lookup"><span data-stu-id="f0c11-305">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

## <a name="review-the-execution-trace"></a><span data-ttu-id="f0c11-306">Täitmise jälje läbivaatus</span><span class="sxs-lookup"><span data-stu-id="f0c11-306">Review the execution trace</span></span>

### <a name="export-the-generated-trace-from-finance-and-operations"></a><span data-ttu-id="f0c11-307">Loodud jälje eksportimine rakendusest Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f0c11-307">Export the generated trace from Finance and Operations</span></span>

<span data-ttu-id="f0c11-308">Korrake samme selle teema jaotises [Loodud jälje eksportimine rakendusest Finance and Operations](#export-trace), et salvestada uus jõudluse jälg kohalikult.</span><span class="sxs-lookup"><span data-stu-id="f0c11-308">Repeat the steps in the [Export the generated trace from Finance and Operations](#export-trace) section earlier in this topic to save a new performance trace locally.</span></span>

### <a name="import-the-generated-trace-into-rcs"></a><span data-ttu-id="f0c11-309">Loodud jälje importimine RCS-i</span><span class="sxs-lookup"><span data-stu-id="f0c11-309">Import the generated trace into RCS</span></span>

<span data-ttu-id="f0c11-310">Korrake samme selle teema jaotises [Loodud jälje importimine RCS-i](#import-trace), et importida uus jõudluse jälg RCS-i.</span><span class="sxs-lookup"><span data-stu-id="f0c11-310">Repeat the steps in the [Import the generated trace into RCS](#import-trace) section earlier in this topic to import the new performance trace into RCS.</span></span>

### <a name="use-the-performance-trace-for-analysis-in-rcs--model-mapping"></a><span data-ttu-id="f0c11-311">Jõudluse jälituse kasutamine analüüsiks RCS-is – mudelivastendus</span><span class="sxs-lookup"><span data-stu-id="f0c11-311">Use the performance trace for analysis in RCS – Model mapping</span></span>

<span data-ttu-id="f0c11-312">Korrake samme selle teema jaotises [Jõudluse jälituse kasutamine analüüsiks RCS-is – mudelivastendus](#use-trace), et analüüsida viimast jõudluse jälge.</span><span class="sxs-lookup"><span data-stu-id="f0c11-312">Repeat the steps in the [Use the performance trace for analysis in RCS – Model mapping](#use-trace) section earlier in this topic to analyze the latest performance trace.</span></span>

<span data-ttu-id="f0c11-313">Pange tähele, et kohandused, mida tegite mudelivastendusele, on eemaldanud dubleeritud päringud andmebaasile.</span><span class="sxs-lookup"><span data-stu-id="f0c11-313">Notice that the adjustments that you made to the model mapping have eliminated duplicate queries to database.</span></span> <span data-ttu-id="f0c11-314">Vähendatud on ka selle mudelivastenduse kutsete arvu andmebaasi tabelitele ja andmeallikatele.</span><span class="sxs-lookup"><span data-stu-id="f0c11-314">The number of calls to database tables and data sources for this model mapping has been also reduced.</span></span> <span data-ttu-id="f0c11-315">See on paranenud kogu ER-i lahenduse jõudlus.</span><span class="sxs-lookup"><span data-stu-id="f0c11-315">Therefore, the performance of the whole ER solution has improved.</span></span>

![Jälje teave andmeallika VendTable kohta RCS-i lehel Mudelivastenduse koostaja](./media/GER-PerfTrace-RCS-TraceInfoInMapping2.png)

<span data-ttu-id="f0c11-317">Jälje teabes näitab andmeallika VendTable väärtus **\[12\]**, et seda andmeallikat kutsuti 12 korda.</span><span class="sxs-lookup"><span data-stu-id="f0c11-317">In the trace information, the value **\[12\]** for the VendTable data source indicates that this data source was called 12 times.</span></span> <span data-ttu-id="f0c11-318">Väärtus **\[Q:6\]** näitab, et kuus kutset teisendati andmebaasi kutseteks andmeallika VendTable tabelile.</span><span class="sxs-lookup"><span data-stu-id="f0c11-318">The value **\[Q:6\]** indicates that six calls were translated to database calls to the VendTable table.</span></span> <span data-ttu-id="f0c11-319">Väärtus **\[C:6\]** näitab, et andmebaasist toodud kirjed salvestati vahemällu ja kuus muud kõnet töödeldi vahemälu abil.</span><span class="sxs-lookup"><span data-stu-id="f0c11-319">The value **\[C:6\]** indicates that the records that were fetched from the database were cached, and six other calls were processed by using the cache.</span></span>

<span data-ttu-id="f0c11-320">Pange tähele, et kutsete arv andmeallikale LedgerTransTypeList on vähendatud 9027-lt 240-le.</span><span class="sxs-lookup"><span data-stu-id="f0c11-320">Notice that the number of calls to the LedgerTransTypeList data source has been reduced from 9,027 to 240.</span></span>

![Jälje teave andmeallika LedgerTransTypeList kohta RCS-i lehel Mudelivastenduse koostaja](./media/GER-PerfTrace-RCS-TraceInfoInMapping2a.png)

## <a name="review-the-execution-trace-in-finance-and-operations"></a><span data-ttu-id="f0c11-322">Täitmise jälje läbivaatus rakenduses Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f0c11-322">Review the execution trace in Finance and Operations</span></span>

<span data-ttu-id="f0c11-323">Peale RCS-i võivad mõned rakenduse Finance and Operations versioonid pakkuda võimalusi ER-i raamistiku koostaja kogemuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="f0c11-323">In addition to RCS, some versions of Finance and Operations might offer capabilities for an ER framework designer experience.</span></span> <span data-ttu-id="f0c11-324">Nendel rakenduse Finance and Operations versioonidel on olemas suvand **Luba kujundusrežiim**, mida saab sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="f0c11-324">These versions of Finance and Operations have an **Enable design mode** option that can be turned on.</span></span> <span data-ttu-id="f0c11-325">Selle suvandi leiate lehe **Elektroonilise aruandluse parameetrid** vahekaardilt **Üldine**, mille saate avada tööruumist **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-325">You can find this option on the **General** tab of the **Electronic reporting parameters** page, which you can open from the **Electronic reporting** workspace.</span></span>

![Rakenduse Finance and Operations lehel Elektroonilise aruandluse parameetrid kujundusrežiimi suvandi lubamine](./media/GER-PerfTrace-GER-Parameters-DesignMode.png)

<span data-ttu-id="f0c11-327">Kui kasutate ühte neist rakenduse Finance and Operations versioonidest, saate analüüsida loodud jõudluse jälje üksikasju otse rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="f0c11-327">If you use one of these versions of Finance and Operations, you can analyze the details of generated performance traces directly in Finance and Operations.</span></span> <span data-ttu-id="f0c11-328">Te ei pea neid eksportima rakendusest Finance and Operations ning importima RCS-i.</span><span class="sxs-lookup"><span data-stu-id="f0c11-328">You don't have to export them from Finance and Operation and import them into RCS.</span></span>

## <a name="review-the-execution-trace-by-using-external-tools"></a><span data-ttu-id="f0c11-329">Täitmise jälje läbivaatus väliste tööriistade abil</span><span class="sxs-lookup"><span data-stu-id="f0c11-329">Review the execution trace by using external tools</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="f0c11-330">Kasutaja parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="f0c11-330">Configure user parameters</span></span>

1. <span data-ttu-id="f0c11-331">Avage rakenduses Finance and Operations **Organisatsiooni haldus \> Elektrooniline aruandlus \> Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-331">In Finance and Operations, go to **Organization administration \> Electronic reporting \> Configurations**.</span></span>
2. <span data-ttu-id="f0c11-332">Valige lehe **Konfiguratsioonid** toimingupaani vahekaardi **Konfiguratsioonid** grupist **Täpsemad sätted** valik **Kasutaja parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-332">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="f0c11-333">Valige dialoogiboksi **Kasutaja parameetrid** jaotises **Täitmise jälitus** väljal **Täitmise jälje vorming** valik **PerfView XML.**</span><span class="sxs-lookup"><span data-stu-id="f0c11-333">In the **User parameters** dialog box, in the **Execution tracing** section, in the **Execution trace format** field, select **PerfView XML**.</span></span>

### <a name="run-the-er-format"></a><span data-ttu-id="f0c11-334">ER-vormingu käivitamine</span><span class="sxs-lookup"><span data-stu-id="f0c11-334">Run the ER format</span></span>

<span data-ttu-id="f0c11-335">Korrake samme selle teema jaotises [ER-vormingu käivitamine](#run-format), et luua uus jõudluse jälg.</span><span class="sxs-lookup"><span data-stu-id="f0c11-335">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="f0c11-336">Pange tähele, et veebibrauser pakub allalaadimiseks ZIP-faili.</span><span class="sxs-lookup"><span data-stu-id="f0c11-336">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="f0c11-337">See fail sisaldab jõudluse jälge PerfView-vormingus.</span><span class="sxs-lookup"><span data-stu-id="f0c11-337">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="f0c11-338">Seejärel saate kasutada PerfView jõudluse analüüsi tööriista, et analüüsida ER-vormingu täitmise üksikasju.</span><span class="sxs-lookup"><span data-stu-id="f0c11-338">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span>

![Käivitatud ER-vormingu jälitusteave PerfView'is](./media/GER-PerfTrace2-PerfViewTrace1.PNG)

## <a name="use-external-tools-to-review-an-execution-trace-that-includes-database-queries"></a><span data-ttu-id="f0c11-340">Väliste tööriistade kasutamine täitmise jälje läbivaatamiseks, mis hõlmab andmebaasi päringuid</span><span class="sxs-lookup"><span data-stu-id="f0c11-340">Use external tools to review an execution trace that includes database queries</span></span>

<span data-ttu-id="f0c11-341">Tänu ER-raamistiku täiustustele pakub PerfView'is loodud jõudluse jälitus nüüd üksikasjalikumat teavet ER-i vormingu käivitamise kohta.</span><span class="sxs-lookup"><span data-stu-id="f0c11-341">Because of improvements that have been made to the ER framework, the performance trace that is generated in PerfView format now offers more details about ER format execution.</span></span> <span data-ttu-id="f0c11-342">Microsoft Dynamics 365 for Finance and Operations versioonis 10.0.4 (juuli, 2019) võib see jälg sisaldada ka rakenduse andmebaasile tehtud SQL-i päringute üksikasju.</span><span class="sxs-lookup"><span data-stu-id="f0c11-342">In Microsoft Dynamics 365 for Finance and Operations version 10.0.4 (July 2019), this trace can also include details of executed SQL queries to the application database.</span></span>

### <a name="configure-user-parameters"></a><span data-ttu-id="f0c11-343">Kasutaja parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="f0c11-343">Configure user parameters</span></span>

1. <span data-ttu-id="f0c11-344">Avage rakenduses Finance and Operations **Organisatsiooni haldus**\> **Elektrooniline aruandlus** \>**Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-344">In Finance and Operations, go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="f0c11-345">Valige lehe **Konfiguratsioonid** toimingupaani vahekaardi **Konfiguratsioonid** grupist **Täpsemad sätted** valik **Kasutaja parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-345">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="f0c11-346">Seadke dialoogiboksi **Kasutaja parameetrid** jaotises **Täitmise jälitus** järgmised parameetrid.</span><span class="sxs-lookup"><span data-stu-id="f0c11-346">In the **User parameters** dialog box, in the **Execution tracing** section, set the following parameters:</span></span>

    - <span data-ttu-id="f0c11-347">Valige väljal **Täitmise jälituse vorming** suvand **PerfView XML**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-347">In the **Execution trace format** field, select **PerfView XML**.</span></span>
    - <span data-ttu-id="f0c11-348">Seadistage **Päringustatistika sissenõudmise** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-348">Set the **Collect query statistics** option to **Yes**.</span></span>
    - <span data-ttu-id="f0c11-349">Määrake suvand **Jälituse päring** olekule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="f0c11-349">Set the **Trace query** option to **Yes**.</span></span>

    ![Kasutaja parameetrite dialoogiboks rakenduses Finance and Operations](./media/GER-PerfTrace2-GER-UserParameters.PNG)

### <a name="run-the-er-format"></a><span data-ttu-id="f0c11-351">ER-vormingu käivitamine</span><span class="sxs-lookup"><span data-stu-id="f0c11-351">Run the ER format</span></span>

<span data-ttu-id="f0c11-352">Korrake samme selle teema jaotises [ER-vormingu käivitamine](#run-format), et luua uus jõudluse jälg.</span><span class="sxs-lookup"><span data-stu-id="f0c11-352">Repeat the steps in the [Run the ER format](#run-format) section earlier in this topic to generate a new performance trace.</span></span>

<span data-ttu-id="f0c11-353">Pange tähele, et veebibrauser pakub allalaadimiseks ZIP-faili.</span><span class="sxs-lookup"><span data-stu-id="f0c11-353">Notice that the web browser offers a zip file for download.</span></span> <span data-ttu-id="f0c11-354">See fail sisaldab jõudluse jälge PerfView-vormingus.</span><span class="sxs-lookup"><span data-stu-id="f0c11-354">This file contains the performance trace in PerfView format.</span></span> <span data-ttu-id="f0c11-355">Seejärel saate kasutada PerfView jõudluse analüüsi tööriista, et analüüsida ER-vormingu täitmise üksikasju.</span><span class="sxs-lookup"><span data-stu-id="f0c11-355">You can then use the PerfView performance analysis tool to analyze the details of ER format execution.</span></span> <span data-ttu-id="f0c11-356">See jälg sisaldab nüüd SQL-i andmebaasi juurdepääsu üksikasju ER-vormingu käivitamise ajal.</span><span class="sxs-lookup"><span data-stu-id="f0c11-356">This trace now includes the details of SQL database access during the execution of the ER format.</span></span>

![Käivitatud ER-vormingu jälitusteave PerfView'is](./media/GER-PerfTrace2-PerfViewTrace2.PNG)
