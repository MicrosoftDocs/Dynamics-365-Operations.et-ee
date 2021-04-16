---
title: ER-vormingu korrigeerimine kohandatud elektroonilise dokumendi loomiseks
description: Selles teemas selgitatakse, kuidas korrigeerida Microsofti elektroonilise aruandluse (ER) vormingut nii, et see looks kohandatud elektroonilise dokumendi.
author: NickSelin
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7355fbb3321a6b5707ab561e88aed2d22cc967cd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5743649"
---
# <a name="adjust-an-er-format-to-generate-a-custom-electronic-document"></a><span data-ttu-id="485ff-103">ER-vormingu korrigeerimine kohandatud elektroonilise dokumendi loomiseks</span><span class="sxs-lookup"><span data-stu-id="485ff-103">Adjust an ER format to generate a custom electronic document</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="485ff-104">Selle teema protseduurid selgitavad, kuidas süsteemiadministraatori või elektroonilise aruandluse funktsionaalse konsultanti rolli kasutajad saavad neid ülesandeid täita.</span><span class="sxs-lookup"><span data-stu-id="485ff-104">The procedures in this topic explain how a user in the System Administrator or Electronic Reporting Functional Consultant role can perform these tasks:</span></span>

- <span data-ttu-id="485ff-105">Parameetrite konfigureerimine [Elektroonilise aruandluse (ER) raamistiku jaoks](general-electronic-reporting.md).</span><span class="sxs-lookup"><span data-stu-id="485ff-105">Configure parameters for the [Electronic reporting (ER) framework](general-electronic-reporting.md).</span></span>
- <span data-ttu-id="485ff-106">Importige ER-konfiguratsioonid, mida pakub Microsoft ja kasutatakse maksefaili loomiseks [hankija makse](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) töötlemise ajal.</span><span class="sxs-lookup"><span data-stu-id="485ff-106">Import ER configurations that are provided by Microsoft and used to generate a payment file while a [vendor payment](../../../finance/cash-bank-management/tasks/vendor-payment-overview.md) is being processed.</span></span>
- <span data-ttu-id="485ff-107">Looge standardse ER-vormingu konfiguratsiooni kohandatud versioon, mida pakub Microsoft.</span><span class="sxs-lookup"><span data-stu-id="485ff-107">Create a custom version of a standard ER format configuration that is provided by Microsoft.</span></span>
- <span data-ttu-id="485ff-108">Muutke kohandatud ER-vormingu konfiguratsiooni nii, et see looks kindla panga nõuetele vastavad maksefailid.</span><span class="sxs-lookup"><span data-stu-id="485ff-108">Modify the custom ER format configuration so that it generates payment files that meets the requirements of a specific bank.</span></span>
- <span data-ttu-id="485ff-109">Võtke kasutusele muudatused, mis on tehtud standardsele ER-vormingu konfiguratsioonile kohandatud ER-vormingu konfiguratsioonis.</span><span class="sxs-lookup"><span data-stu-id="485ff-109">Adopt changes that are made to the standard ER format configuration in the custom ER format configuration.</span></span>

<span data-ttu-id="485ff-110">Kõiki järgmisi protseduure saab teha ettevõttes **GBSI**.</span><span class="sxs-lookup"><span data-stu-id="485ff-110">All the following procedures can be done in the **GBSI** company.</span></span> <span data-ttu-id="485ff-111">Koodi pole vaja kirjutada.</span><span class="sxs-lookup"><span data-stu-id="485ff-111">No coding is required.</span></span>

- [<span data-ttu-id="485ff-112">ER-raamistiku konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="485ff-112">Configure the ER framework</span></span>](#ConfigureFramework)

    - [<span data-ttu-id="485ff-113">Elektroonilise aruandluse parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="485ff-113">Configure ER parameters</span></span>](#ConfigureParameters)
    - [<span data-ttu-id="485ff-114">ER-konfiguratsiooni pakkuja aktiveerimine</span><span class="sxs-lookup"><span data-stu-id="485ff-114">Activate an ER configuration provider</span></span>](#ActivateProvider)

        - [<span data-ttu-id="485ff-115">ER-konfiguratsiooni pakkujate loendi ülevaatamine</span><span class="sxs-lookup"><span data-stu-id="485ff-115">Review the list of ER configuration providers</span></span>](#ReviewProvidersList)
        - [<span data-ttu-id="485ff-116">Uue ER-vormingu konfiguratsioonipakkuja lisamine</span><span class="sxs-lookup"><span data-stu-id="485ff-116">Add a new ER configuration provider</span></span>](#ActivateProvider)
        - [<span data-ttu-id="485ff-117">ER-konfiguratsiooni pakkuja aktiveerimine</span><span class="sxs-lookup"><span data-stu-id="485ff-117">Activate an ER configuration provider</span></span>](#ActivateAddedProvider)

- [<span data-ttu-id="485ff-118">Standardse ER‑vormingu konfiguratsiooni importimine</span><span class="sxs-lookup"><span data-stu-id="485ff-118">Import the standard ER format configurations</span></span>](#ImportERSolution1)

    - [<span data-ttu-id="485ff-119">Standardse ER-konfiguratsiooni importimine</span><span class="sxs-lookup"><span data-stu-id="485ff-119">Import the standard ER configurations</span></span>](#ImportERFormat1)
    - [<span data-ttu-id="485ff-120">Imporditud ER-konfiguratsioonide ülevaatamine</span><span class="sxs-lookup"><span data-stu-id="485ff-120">Review the imported ER configurations</span></span>](#ReviewImportedERSolution)

- [<span data-ttu-id="485ff-121">Hankija makse ettevalmistamine töötlemiseks</span><span class="sxs-lookup"><span data-stu-id="485ff-121">Prepare a vendor payment for processing</span></span>](#PrepareVendorPayment)

    - [<span data-ttu-id="485ff-122">Hankija kontole panga teabe lisamine</span><span class="sxs-lookup"><span data-stu-id="485ff-122">Add bank information for a vendor account</span></span>](#AddBankAccount)
    - [<span data-ttu-id="485ff-123">Hankija makse sisestamine</span><span class="sxs-lookup"><span data-stu-id="485ff-123">Enter a vendor payment</span></span>](#EnterVendorPayment)

- [<span data-ttu-id="485ff-124">Hankija makse töötlemine standardse ER-vormingu abil</span><span class="sxs-lookup"><span data-stu-id="485ff-124">Process a vendor payment by using the standard ER format</span></span>](#ProcessVendorPayment1)

    - [<span data-ttu-id="485ff-125">Elektroonilise makseviisi seadistamine</span><span class="sxs-lookup"><span data-stu-id="485ff-125">Set up the electronic payment method</span></span>](#ConfigureMethodOfPayment1)
    - [<span data-ttu-id="485ff-126">Hankija makse töötlemine</span><span class="sxs-lookup"><span data-stu-id="485ff-126">Process a vendor payment</span></span>](#ProcessPayment1)

- [<span data-ttu-id="485ff-127">Standardse ER-vormingu kohandamine</span><span class="sxs-lookup"><span data-stu-id="485ff-127">Customize the standard ER format</span></span>](#CustomizeProvidedFormat)

    - [<span data-ttu-id="485ff-128">Kohandatud vormingu loomine</span><span class="sxs-lookup"><span data-stu-id="485ff-128">Create a custom format</span></span>](#DeriveProvidedFormat)
    - [<span data-ttu-id="485ff-129">Kohandatud vormingu redigeerimine</span><span class="sxs-lookup"><span data-stu-id="485ff-129">Edit a custom format</span></span>](#ConfigureDerivedFormat)
    - [<span data-ttu-id="485ff-130">Kohandatud vormingu märkimine käitatavaks</span><span class="sxs-lookup"><span data-stu-id="485ff-130">Mark a custom format as runnable</span></span>](#MarkFormatRunnable)

- [<span data-ttu-id="485ff-131">Hankija makse töötlemine kohandatud ER-vormingu abil</span><span class="sxs-lookup"><span data-stu-id="485ff-131">Process a vendor payment by using the custom ER format</span></span>](#ProcessVendorPayment2)

    - [<span data-ttu-id="485ff-132">Elektroonilise makseviisi seadistamine</span><span class="sxs-lookup"><span data-stu-id="485ff-132">Set up the electronic payment method</span></span>](#ConfigureMethodOfPayment2)
    - [<span data-ttu-id="485ff-133">Hankija makse töötlemine</span><span class="sxs-lookup"><span data-stu-id="485ff-133">Process a vendor payment</span></span>](#ProcessPayment2)

- [<span data-ttu-id="485ff-134">Standardse ER‑vormingu konfiguratsiooni uute versioonide importimine</span><span class="sxs-lookup"><span data-stu-id="485ff-134">Import new versions of the standard ER format configurations</span></span>](#ImportERSolution2)

    - [<span data-ttu-id="485ff-135">Standardse ER‑konfiguratsiooni uute versioonide importimine</span><span class="sxs-lookup"><span data-stu-id="485ff-135">Import new versions of the standard ER configurations</span></span>](#ImportERFormat2)
    - [<span data-ttu-id="485ff-136">Imporditud ER-vormingu konfiguratsioonide ülevaatamine</span><span class="sxs-lookup"><span data-stu-id="485ff-136">Review the imported ER format configurations</span></span>](#ReviewImportedERFormat)

- [<span data-ttu-id="485ff-137">Muudatuste kasutuselevõtmine kohandatud vormingu imporditud vormingu uues versioonis</span><span class="sxs-lookup"><span data-stu-id="485ff-137">Adopt the changes in the new version of an imported format in a custom format</span></span>](#AdoptNewBaseVersion)

    - [<span data-ttu-id="485ff-138">Kohandatud vormingu praeguse mustandversiooni lõpule viimine</span><span class="sxs-lookup"><span data-stu-id="485ff-138">Complete the current draft version of a custom format</span></span>](#CompleteDerivedFormat)
    - [<span data-ttu-id="485ff-139">Uuele alusversioonile kohandatud vormingu aluse muutmine</span><span class="sxs-lookup"><span data-stu-id="485ff-139">Rebase a custom format to a new base version</span></span>](#RebaseDerivedFormat)
    - [<span data-ttu-id="485ff-140">Hankija makse töötlemine muudetud alusega ER-vormingu abil</span><span class="sxs-lookup"><span data-stu-id="485ff-140">Process a vendor payment by using a rebased ER format</span></span>](#ProcessPayment3)

- [<span data-ttu-id="485ff-141">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="485ff-141">Additional resources</span></span>](#References)

## <a name="configure-the-er-framework"></a><a id="ConfigureFramework"></a><span data-ttu-id="485ff-142">ER-raamistiku konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="485ff-142">Configure the ER framework</span></span>

<span data-ttu-id="485ff-143">Elektroonilise aruandluse funktsionaalse konsultandi rolli kasutajana peate konfigureerima minimaalsete ER-parameetrite kogumi, enne kui saate hakata kasutama ER-raamistikku standardse ER-vormingu kohandatud versiooni kujundamiseks.</span><span class="sxs-lookup"><span data-stu-id="485ff-143">As a user in the Electronic Reporting Functional Consultant role, you must configure the minimal set of ER parameters before you can start to use the ER framework to design a custom version of a standard ER format.</span></span>

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a><span data-ttu-id="485ff-144">Elektroonilise aruandluse parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="485ff-144">Configure ER parameters</span></span>

1. <span data-ttu-id="485ff-145">Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="485ff-145">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="485ff-146">Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Seostatud lingid** paan **Elektroonilise aruandluse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="485ff-146">On the **Localization configurations** page, in the **Related links** section, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="485ff-147">Valige lehel **Elektroonilise aruandluse parameetrid** vahekaardil **Üldine** suvandi **Luba kujundusrežiim** sätteks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="485ff-147">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="485ff-148">Vahekaardil **Manused** määrake järgmised parameetrid.</span><span class="sxs-lookup"><span data-stu-id="485ff-148">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="485ff-149">Valige väljal **Konfiguratsioonid** tüüp **Fail** ettevõttele **USMF**.</span><span class="sxs-lookup"><span data-stu-id="485ff-149">In the **Configurations** field, select the **File** type for the **USMF** company.</span></span>
    - <span data-ttu-id="485ff-150">Valige väljadel **Töö arhiiv**, **Ajutine**, **Alus** ja **Muud** tüüp **Fail**.</span><span class="sxs-lookup"><span data-stu-id="485ff-150">In the **Job archive**, **Temporary**, **Baseline**, and **Others** fields, select the **File** type.</span></span>

<span data-ttu-id="485ff-151">Lisateavet ER-parameetrite kohta vt jaotisest [ER-raamistiku konfigureerimine](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="485ff-151">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="485ff-152">ER-konfiguratsiooni pakkuja aktiveerimine</span><span class="sxs-lookup"><span data-stu-id="485ff-152">Activate an ER configuration provider</span></span>

<span data-ttu-id="485ff-153">Kõigile lisatud ER-konfiguratsioonidele on märgitud omanikuks ER-konfiguratsiooni pakkuja.</span><span class="sxs-lookup"><span data-stu-id="485ff-153">Every ER configuration that is added is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="485ff-154">Sel eesmärgil kasutatakse tööruumis **Elektrooniline aruandlus** aktiveeritud ER-konfiguratsiooni pakkujat.</span><span class="sxs-lookup"><span data-stu-id="485ff-154">The ER configuration provider that is activated in the **Electronic reporting** workspace is used for this purpose.</span></span> <span data-ttu-id="485ff-155">Seega enne ER-konfiguratsioonide lisamist või redigeerimist peate aktiveerima tööruumis **Elektrooniline aruandlus** ER-konfiguratsiooni pakkuja.</span><span class="sxs-lookup"><span data-stu-id="485ff-155">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="485ff-156">ER-konfiguratsiooni saab redigeerida ainult selle omanik.</span><span class="sxs-lookup"><span data-stu-id="485ff-156">Only the owner of an ER configuration can edit it.</span></span> <span data-ttu-id="485ff-157">Seega enne ER-konfiguratsiooni redigeerimist pea olema tööruumis **Elektrooniline aruandlus** aktiveeriud vastav ER-konfiguratsiooni pakkuja.</span><span class="sxs-lookup"><span data-stu-id="485ff-157">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a><span data-ttu-id="485ff-158">ER-konfiguratsiooni pakkujate loendi ülevaatamine</span><span class="sxs-lookup"><span data-stu-id="485ff-158">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="485ff-159">Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="485ff-159">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="485ff-160">Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Seostatud lingid** paan **Konfiguratsioonipakkujad**.</span><span class="sxs-lookup"><span data-stu-id="485ff-160">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="485ff-161">Lehel **Konfiguratsioonipakkuja tabel** on igal pakkuja kirjel kordumatu nimi ja URL.</span><span class="sxs-lookup"><span data-stu-id="485ff-161">On the **Configuration provider table** page, each provider record has a unique name and URL.</span></span> <span data-ttu-id="485ff-162">Vaadake üle selle lehe sisu.</span><span class="sxs-lookup"><span data-stu-id="485ff-162">Review the contents of this page.</span></span> <span data-ttu-id="485ff-163">Kui üksuse **Litware, Inc.** (`https://www.litware.com`) kirje on juba olemas, jätke järgmine protseduur vahele [Uue ER-konfiguratsiooni pakkuja lisamine](#ActivateProvider).</span><span class="sxs-lookup"><span data-stu-id="485ff-163">If a record for **Litware, Inc.** (`https://www.litware.com`) already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a><span data-ttu-id="485ff-164">Uue ER-konfiguratsiooni pakkuja lisamine</span><span class="sxs-lookup"><span data-stu-id="485ff-164">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="485ff-165">Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="485ff-165">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="485ff-166">Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Seostatud lingid** paan **Konfiguratsioonipakkujad**.</span><span class="sxs-lookup"><span data-stu-id="485ff-166">On the **Localization configurations** page, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="485ff-167">Lehel **Konfiguratsioonipakkujad** valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="485ff-167">On the **Configuration providers** page, select **New**.</span></span>
4. <span data-ttu-id="485ff-168">Väljale **Nimi** sisestage väärtus **Litware, Inc.**</span><span class="sxs-lookup"><span data-stu-id="485ff-168">In the **Name** field, enter **Litware, Inc.**</span></span>
5. <span data-ttu-id="485ff-169">Sisestage väljale **Interneti-aadress** `https://www.litware.com`.</span><span class="sxs-lookup"><span data-stu-id="485ff-169">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
6. <span data-ttu-id="485ff-170">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="485ff-170">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a><span data-ttu-id="485ff-171">ER-konfiguratsiooni pakkuja aktiveerimine</span><span class="sxs-lookup"><span data-stu-id="485ff-171">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="485ff-172">Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="485ff-172">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="485ff-173">Vailge lehe **Lokaliseerimise konfiguratsioonid** jaotises **Konfiguratsioonipakkujad** paan **Litware, Inc.** ja seejärel valige **Määra aktiivne**.</span><span class="sxs-lookup"><span data-stu-id="485ff-173">On the **Localization configurations** page, in the **Configuration providers** section, select the **Litware, Inc.** tile, and then select **Set active**.</span></span>

<span data-ttu-id="485ff-174">Lisateabe saamiseks ER-konfiguratsiooni pakkujate kohta vaadake teemat [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="485ff-174">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="import-the-standard-er-format-configurations"></a><a id="ImportERSolution1"></a><span data-ttu-id="485ff-175">Standardse ER‑vormingu konfiguratsiooni importimine</span><span class="sxs-lookup"><span data-stu-id="485ff-175">Import the standard ER format configurations</span></span>

### <a name="import-the-standard-er-configurations"></a><a id="ImportERFormat1"></a><span data-ttu-id="485ff-176">Standardse ER-konfiguratsiooni importimine</span><span class="sxs-lookup"><span data-stu-id="485ff-176">Import the standard ER configurations</span></span>

<span data-ttu-id="485ff-177">Oma praegusesse Microsoft Dynamics 365 Finance'i eksemplari standardsete ER-konfiguratsioonide lisamiseks peate importima need selle eksemplari jaoks konfigureeritud ER-[hoidlast](general-electronic-reporting.md#Repository).</span><span class="sxs-lookup"><span data-stu-id="485ff-177">To add the standard ER configurations to your current instance of Microsoft Dynamics 365 Finance, you must import them from the ER [repository](general-electronic-reporting.md#Repository) that was configured for that instance.</span></span>

1. <span data-ttu-id="485ff-178">Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="485ff-178">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="485ff-179">Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Konfiguratsioonipakkujad** paan **Microsoft** ja seejärel valige pakkuja Microsoft hoidlate loendi kuvamiseks **Hoidlad**.</span><span class="sxs-lookup"><span data-stu-id="485ff-179">On the **Localization configurations** page, in the **Configuration providers** section, select the **Microsoft** tile, and then select **Repositories** to view the list of repositories for the Microsoft provider.</span></span>
3. <span data-ttu-id="485ff-180">Valige lehel **Konfiguratsioonihoidlad** hoidla tüübiga **Globaalne** ja seejärel valige käsk **Ava**.</span><span class="sxs-lookup"><span data-stu-id="485ff-180">On the **Configuration repositories** page, select the repository of the **Global** type, and then select **Open**.</span></span> <span data-ttu-id="485ff-181">Kui teilt küsitakse autoriseerimist ühenduse loomiseks Regulatory Configuration Service'iga, järgige autoriseerimise juhiseid.</span><span class="sxs-lookup"><span data-stu-id="485ff-181">If you're prompted for authorization to connect to Regulatory Configuration Service, follow the authorization instructions.</span></span>
4. <span data-ttu-id="485ff-182">Valige lehel **Konfiguratsioonihoidla** vasakpoolselt paanilt konfiguratsioonipuult vormingu **BACS (UK)** konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="485ff-182">On the **Configuration repository** page, in the configuration tree in the left pane, select the **BACS (UK)** format configuration.</span></span>
5. <span data-ttu-id="485ff-183">Kiirkaardil **Versioonid** valige valitud ER-vormingu konfiguratsiooni versioon **1.1**.</span><span class="sxs-lookup"><span data-stu-id="485ff-183">On the **Versions** FastTab, select version **1.1** of the selected ER format configuration.</span></span>
6. <span data-ttu-id="485ff-184">Valige käsk **Impordi**, et laadida valitud versioon globaalsest hoidlast alla Finance'i praegusesse eksemplari.</span><span class="sxs-lookup"><span data-stu-id="485ff-184">Select **Import** to download the selected version from the Global repository to the current Finance instance.</span></span>

![Konfiguratsioonihoidla leht](./media/er-quick-start2-import-solution1.png)

> [!TIP]
> <span data-ttu-id="485ff-186">Kui teil on probleeme [globaalsele hoidlale](er-download-configurations-global-repo.md) juurde pääsemisega, saate selle asemel [laadida konfiguratsioonid alla](download-electronic-reporting-configuration-lcs.md) Microsoft Dynamics Lifecycle Servicesist (LCS).</span><span class="sxs-lookup"><span data-stu-id="485ff-186">If you have trouble accessing the [Global repository](er-download-configurations-global-repo.md), you can [download configurations](download-electronic-reporting-configuration-lcs.md) from Microsoft Dynamics Lifecycle Services (LCS) instead.</span></span>

### <a name="review-the-imported-er-configurations"></a><a id="ReviewImportedERSolution"></a><span data-ttu-id="485ff-187">Imporditud ER-konfiguratsioonide ülevaatamine</span><span class="sxs-lookup"><span data-stu-id="485ff-187">Review the imported ER configurations</span></span>

1. <span data-ttu-id="485ff-188">Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="485ff-188">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="485ff-189">Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Konfiguratsioonid** paan **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="485ff-189">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="485ff-190">Laiendage lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvandit **Maksemudel**.</span><span class="sxs-lookup"><span data-stu-id="485ff-190">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**.</span></span>
4. <span data-ttu-id="485ff-191">Pange tähele, et lisaks valitud ER-vormingule **BACS (UK)** imporditi teised nõutavad ER-konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="485ff-191">Notice that, in addition to the selected **BACS (UK)** ER format, other required ER configurations were imported.</span></span> <span data-ttu-id="485ff-192">Veenduge, et konfiguratsioonipuus oleksid saadaval järgmised ER-konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="485ff-192">Make sure that the following ER configurations are available in the configuration tree:</span></span>

    - <span data-ttu-id="485ff-193">**Maksemudel** – see konfiguratsioon sisaldab [andmemudeli](general-electronic-reporting.md#data-model-and-model-mapping-components) ER-komponenti, mis tähistab makse äridomeeni andmete struktuuri.</span><span class="sxs-lookup"><span data-stu-id="485ff-193">**Payment model** – This configuration contains the [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) ER component that represents the data structure of the payment business domain.</span></span>
    - <span data-ttu-id="485ff-194">**Maksemudeli vastendamine 1611** – see konfiguratsioon sisaldab [mudeli vastendamise](general-electronic-reporting.md#data-model-and-model-mapping-components) ER-komponenti, mis kirjeldab, kuidas andmemudel täidetakse rakenduse andmetega käitusajal.</span><span class="sxs-lookup"><span data-stu-id="485ff-194">**Payment model mapping 1611** – This configuration contains the [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) ER component that describes how the data model is filled in with application data at runtime.</span></span>
    - <span data-ttu-id="485ff-195">**BACS (UK)** – see konfiguratsioon sisaldab [vormingu](general-electronic-reporting.md#FormatComponentOutbound) ja vormingu vastendamise ER-komponente.</span><span class="sxs-lookup"><span data-stu-id="485ff-195">**BACS (UK)** – This configuration contains the [format](general-electronic-reporting.md#FormatComponentOutbound) and format mapping ER components.</span></span> <span data-ttu-id="485ff-196">Vormingu komponent määratleb aruande paigutuse.</span><span class="sxs-lookup"><span data-stu-id="485ff-196">The format component specifies the report layout.</span></span> <span data-ttu-id="485ff-197">Vormingu vastendamise komponent sisaldab mudeli andmeallikat ja määratleb, kuidas täidetakse aruande paigutust andmeallika abil käitusajal.</span><span class="sxs-lookup"><span data-stu-id="485ff-197">The format mapping component contains the model data source and specifies how the report layout is filled in by using this data source at runtime.</span></span>

![Konfiguratsioonide leht](./media/er-quick-start2-imported-solution1.png)

## <a name="prepare-a-vendor-payment-for-processing"></a><a id="PrepareVendorPayment"></a><span data-ttu-id="485ff-199">Hankija makse ettevalmistamine töötlemiseks</span><span class="sxs-lookup"><span data-stu-id="485ff-199">Prepare a vendor payment for processing</span></span>

### <a name="add-bank-information-for-a-vendor-account"></a><a id="AddBankAccount"></a><span data-ttu-id="485ff-200">Hankija kontole panga teabe lisamine</span><span class="sxs-lookup"><span data-stu-id="485ff-200">Add bank information for a vendor account</span></span>

<span data-ttu-id="485ff-201">Peate lisama hankija kontole panga teabe, millele viidatakse hiljem registreeritud makses.</span><span class="sxs-lookup"><span data-stu-id="485ff-201">You must add bank information for a vendor account that will be referred to later in a registered payment.</span></span>

1. <span data-ttu-id="485ff-202">Avage **Ostureskontro** \> **Hankijad** \> **Kõik hankijad**.</span><span class="sxs-lookup"><span data-stu-id="485ff-202">Go to **Accounts payable** \> **Vendors** \> **All vendors**.</span></span>
2. <span data-ttu-id="485ff-203">Valige lehel **Kõik hankijad** hankija konto **GB_SI_000001** ja seejärel valige toimingupaani vahekaardil **Hankija** grupis **Seadistamine** suvand **Pangakontod**.</span><span class="sxs-lookup"><span data-stu-id="485ff-203">On the **All vendors** page, select the **GB_SI_000001** vendor account, and then, on the Action Pane, on the **Vendor** tab, in the **Set up** group, select **Bank accounts**.</span></span>
3. <span data-ttu-id="485ff-204">Valige lehel **Hankija pangakontod** suvand **Uus** ja seejärel sisestage järgmine teave.</span><span class="sxs-lookup"><span data-stu-id="485ff-204">On the **Vendor bank accounts** page, select **New**, and then enter the following information:</span></span>

    1. <span data-ttu-id="485ff-205">Sisestage väljal **Pangakonto** suvand **GBP OPER**.</span><span class="sxs-lookup"><span data-stu-id="485ff-205">In the **Bank account** field, enter **GBP OPER**.</span></span>
    2. <span data-ttu-id="485ff-206">Valige väljal **Pangagrupid** suvand **BankGBP**.</span><span class="sxs-lookup"><span data-stu-id="485ff-206">In the **Bank groups** field, select **BankGBP**.</span></span>
    3. <span data-ttu-id="485ff-207">Sisestage väljal **Pangakonto number** suvand **202015**.</span><span class="sxs-lookup"><span data-stu-id="485ff-207">In the **Bank account number** field, enter **202015**.</span></span>
    4. <span data-ttu-id="485ff-208">Sisestage väljale **SWIFT-kood** väärtus <a id="DefineSWIFTCode"></a>**CHASDEFXXXX**.</span><span class="sxs-lookup"><span data-stu-id="485ff-208">In the **SWIFT code** field, enter <a id="DefineSWIFTCode"></a>**CHASDEFXXXX**.</span></span>
    5. <span data-ttu-id="485ff-209">Sisestage väljale **IBAN** väärtus **GB33BUKB20201555555555**.</span><span class="sxs-lookup"><span data-stu-id="485ff-209">In the **IBAN** field, enter **GB33BUKB20201555555555**.</span></span>
    6. <span data-ttu-id="485ff-210">Jätke väljale **Registreerimisnumber** vaikeväärtus <a id="DefineRoutingNumber"></a>**123456**.</span><span class="sxs-lookup"><span data-stu-id="485ff-210">In the **Routing number** field, keep the default value, <a id="DefineRoutingNumber"></a>**123456**.</span></span>

    ![Hankija pangakontode leht](./media/er-quick-start2-bank-account.png)

4. <span data-ttu-id="485ff-212">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="485ff-212">Select **Save**.</span></span>
5. <span data-ttu-id="485ff-213">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="485ff-213">Close the page.</span></span>
6. <span data-ttu-id="485ff-214">Avage lehel **Kõik hankijad** hankija konto **GB_SI_000001**.</span><span class="sxs-lookup"><span data-stu-id="485ff-214">On the **All vendors** page, open the **GB_SI_000001** vendor account.</span></span>
7. <span data-ttu-id="485ff-215">Vajadusel valige hankija üksikasjade lehel **Redigeeri**, et muuta leht redigeeritavaks.</span><span class="sxs-lookup"><span data-stu-id="485ff-215">On the vendor details page, select **Edit** to make the page editable, if required.</span></span>
8. <span data-ttu-id="485ff-216">Valige kiirkaardi **Makse** väljal **Pangakonto** suvand **GBP OPER**.</span><span class="sxs-lookup"><span data-stu-id="485ff-216">On the **Payment** FastTab, in the **Bank account** field, select **GBP OPER**.</span></span>

    ![Hankija üksikasjade leht](./media/er-quick-start2-bank-account-reference.png)

9. <span data-ttu-id="485ff-218">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="485ff-218">Select **Save**.</span></span>
10. <span data-ttu-id="485ff-219">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="485ff-219">Close the page.</span></span>

### <a name="enter-a-vendor-payment"></a><a id="EnterVendorPayment"></a><span data-ttu-id="485ff-220">Hankija makse sisestamine</span><span class="sxs-lookup"><span data-stu-id="485ff-220">Enter a vendor payment</span></span>

<span data-ttu-id="485ff-221">Peate sisestama uue hankija makse [maksesoovituse](https://docs.microsoft.com/dynamics365/finance/accounts-payable/create-vendor-payments-payment-proposal) abil.</span><span class="sxs-lookup"><span data-stu-id="485ff-221">You must enter a new vendor payment by using a [payment proposal](https://docs.microsoft.com/dynamics365/finance/accounts-payable/create-vendor-payments-payment-proposal).</span></span>

1. <span data-ttu-id="485ff-222">Avage **Ostureskontro** \> **Maksed** \> **Hankija maksete tööleht**.</span><span class="sxs-lookup"><span data-stu-id="485ff-222">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="485ff-223">Lehel **Hankija maksete tööleht** valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="485ff-223">On the **Vendor payment journal** page, select **New**.</span></span>
3. <span data-ttu-id="485ff-224">Valige väljal **Nimi** suvand **VendPay**.</span><span class="sxs-lookup"><span data-stu-id="485ff-224">In the **Name** field, select **VendPay**.</span></span>
4. <span data-ttu-id="485ff-225">Valige **Read**.</span><span class="sxs-lookup"><span data-stu-id="485ff-225">Select **Lines**.</span></span>
5. <span data-ttu-id="485ff-226">Valige **Maksesoovitus** \> **Loo maksesoovitus**.</span><span class="sxs-lookup"><span data-stu-id="485ff-226">Select **Payment proposal** \> **Create payment proposal**.</span></span>
6. <span data-ttu-id="485ff-227">Konfigureerige dialoogiboksis **Hankija maksesoovitus** filtreerimistingimused ainult hankija konto **GB_SI_000001** kirjete jaoks ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="485ff-227">In the **Vendor payment proposal** dialog box, configure conditions to filter for records for the **GB_SI_000001** vendor account only, and then select **OK**.</span></span>
7. <span data-ttu-id="485ff-228">Valige arve **00000007_Inv** rida ja seejärel valige **Loo makse**.</span><span class="sxs-lookup"><span data-stu-id="485ff-228">Select the line for the **00000007_Inv** invoice, and then select **Create payment**.</span></span>

    ![Hankija maksesoovituse dialoogiboks](./media/er-quick-start2-payment-proposal.png)

8. <span data-ttu-id="485ff-230">Veenduge, et sisestatud makse oleks konfigureeritud kasutama makseviisi **Elektrooniline**.</span><span class="sxs-lookup"><span data-stu-id="485ff-230">Verify that the payment that is entered is configured to use the **Electronic** method of payment.</span></span>

    ![Hankija maksete leht](./media/er-quick-start2-payment-line.png)

## <a name="process-a-vendor-payment-by-using-the-standard-er-format"></a><a id="ProcessVendorPayment1"></a><span data-ttu-id="485ff-232">Hankija makse töötlemine standardse ER-vormingu abil</span><span class="sxs-lookup"><span data-stu-id="485ff-232">Process a vendor payment by using the standard ER format</span></span>

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment1"></a><span data-ttu-id="485ff-233">Elektroonilise makseviisi seadistamine</span><span class="sxs-lookup"><span data-stu-id="485ff-233">Set up the electronic payment method</span></span>

<span data-ttu-id="485ff-234">Peate konfigureerima elektroonilise makseviisi, et see kasutaks imporditud ER-vormingu konfiguratsiooni.</span><span class="sxs-lookup"><span data-stu-id="485ff-234">You must configure the electronic method of payment so that it uses the imported ER format configuration.</span></span>

1. <span data-ttu-id="485ff-235">Avage **Ostureskontro** \> **Maksmise seadistamine** \> **Makseviisid**.</span><span class="sxs-lookup"><span data-stu-id="485ff-235">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="485ff-236">Valige lehe **Makseviisid – hankijad** vasakpoolsel paanil makseviis **Elektrooniline**.</span><span class="sxs-lookup"><span data-stu-id="485ff-236">On the **Methods of payment - vendors** page, select the **Electronic** method of payment in the left pane.</span></span>
3. <span data-ttu-id="485ff-237">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="485ff-237">Select **Edit**.</span></span>
4. <span data-ttu-id="485ff-238">Seadistage kiirkaardil **Failivormingud** suvandi **Üldine elektrooniline ekspordivorming** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="485ff-238">On the **File formats** FastTab, set the **General electronic Export format** option to **Yes**.</span></span>
5. <span data-ttu-id="485ff-239">Valige väljal **Ekspordivormingu konfiguratsioon** vormingu konfiguratsioon **BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="485ff-239">In the **Export format configuration** field, select the **BACS (UK)** format configuration.</span></span>

    ![Makseviisid - hankijate leht](./media/er-quick-start2-method-of-payment1.png)

6. <span data-ttu-id="485ff-241">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="485ff-241">Select **Save**.</span></span>

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment1"></a><span data-ttu-id="485ff-242">Hankija makse töötlemine</span><span class="sxs-lookup"><span data-stu-id="485ff-242">Process a vendor payment</span></span>

1. <span data-ttu-id="485ff-243">Avage **Ostureskontro** \> **Maksed** \> **Hankija maksete tööleht**.</span><span class="sxs-lookup"><span data-stu-id="485ff-243">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="485ff-244">Valige lehel **Hankija maksete tööleht** eelnevalt lisatud maksete tööleht ja seejärel valige **Read**.</span><span class="sxs-lookup"><span data-stu-id="485ff-244">On the **Vendor payment journal** page, select the payment journal that you added earlier, and then select **Lines**.</span></span>
3. <span data-ttu-id="485ff-245">Valige lehel **Hankija maksed** suvand **Loo maksed**.</span><span class="sxs-lookup"><span data-stu-id="485ff-245">On the **Vendor payments** page, select **Generate payments**.</span></span>
4. <span data-ttu-id="485ff-246">Sisestage dialoogiboksi **Loo maksed** järgmine teave.</span><span class="sxs-lookup"><span data-stu-id="485ff-246">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="485ff-247">Valige väljal **Makseviis** **Elektrooniline**.</span><span class="sxs-lookup"><span data-stu-id="485ff-247">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="485ff-248">Valige väljal **Pangakonto** suvand **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="485ff-248">In the **Bank account** field, select **GBSI OPER**.</span></span>

5. <span data-ttu-id="485ff-249">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="485ff-249">Select **OK**.</span></span>
6. <span data-ttu-id="485ff-250">Määrake dialoogiboksis **Elektroonilise aruande parameetrid** suvandi **Prindi kontrollaruanne** väärtuseks **Jah** ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="485ff-250">In the **Electronic report parameters** dialog box, set the **Print control report** option to **Yes**, and then select **OK**.</span></span>

    ![Elektroonilise aruande parameetrite dialoogileht](./media/er-quick-start2-payment-dialog1.png)

    > [!NOTE]
    > <span data-ttu-id="485ff-252">Lisaks maksefailile saate nüüd luua ka kontrollaruande.</span><span class="sxs-lookup"><span data-stu-id="485ff-252">In addition to the payment file, you can now generate the control report.</span></span>

7. <span data-ttu-id="485ff-253">Laadige alla ZIP-fail ja seejärel ekstraktige sellest järgmised failid.</span><span class="sxs-lookup"><span data-stu-id="485ff-253">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="485ff-254">Kontrollaruanne Exceli vormingus</span><span class="sxs-lookup"><span data-stu-id="485ff-254">The control report in Excel format</span></span>
    - <span data-ttu-id="485ff-255">Maksefail TXT-vormingus</span><span class="sxs-lookup"><span data-stu-id="485ff-255">The payment file in TXT format</span></span>

        <span data-ttu-id="485ff-256">Pange tähele, et vastavalt antud ER-vormingu [struktuurile](#PositionRoutingNumber) algab loodud faili makserida registreerimisnumbriga, mis [määratleti](#DefineRoutingNumber) konfigureeritud pangakonto jaoks.</span><span class="sxs-lookup"><span data-stu-id="485ff-256">Notice that, in accordance with the [structure](#PositionRoutingNumber) of the provided ER format, the payment line in the generated file starts with the routing number that was [defined](#DefineRoutingNumber) for the configured bank account.</span></span>

        ![Maksefail TXT-vormingus](./media/er-quick-start2-payment-file1.png)

## <a name="customize-the-standard-er-format"></a><a id="CustomizeProvidedFormat"></a><span data-ttu-id="485ff-258">Standardse ER-vormingu kohandamine</span><span class="sxs-lookup"><span data-stu-id="485ff-258">Customize the standard ER format</span></span>

<span data-ttu-id="485ff-259">Selles jaotises kuvatud näite puhul peaksite kasutama BACS-vormingus hankija maksete failide loomiseks Microsofti pakutavaid ER-konfiguratsioone, kuid peate lisama kohanduse, et toetada konkreetse panga nõudeid.</span><span class="sxs-lookup"><span data-stu-id="485ff-259">For the example that is shown in this section, you want to use the ER configurations that are provided by Microsoft to generate vendor payment files in BACS format, but you must add a customization to support the requirements of a specific bank.</span></span> <span data-ttu-id="485ff-260">Lisaks peaksite saama täiendada oma kohandatud vormingut, kui uued ER-konfiguratsioonide versioonid on saadaval.</span><span class="sxs-lookup"><span data-stu-id="485ff-260">You also want to be able to upgrade your custom format when new versions of ER configurations become available.</span></span> <span data-ttu-id="485ff-261">Kuid täiendust peaks olema võimalik teha madalaima hinnaga.</span><span class="sxs-lookup"><span data-stu-id="485ff-261">However, you want to be able to do the upgrade at the lowest cost.</span></span>

<span data-ttu-id="485ff-262">Sellisel juhul peaksite Litware, Inc.-i esindajana looma (tuletama) uue ER-vormingu konfiguratsiooni, kasutades alusena Microsofti antud konfiguratsiooni **BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="485ff-262">In this case, as the representative of Litware, Inc., you must create (derive) a new ER format configuration by using the **BACS (UK)** Microsoft-provided configuration as a base.</span></span>

### <a name="create-a-custom-format"></a><a id="DeriveProvidedFormat"></a><span data-ttu-id="485ff-263">Kohandatud vormingu loomine</span><span class="sxs-lookup"><span data-stu-id="485ff-263">Create a custom format</span></span>

1. <span data-ttu-id="485ff-264">Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="485ff-264">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="485ff-265">Laiendage lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvandit **Maksemudel** ja seejärel valige **BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="485ff-265">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK)**.</span></span> <span data-ttu-id="485ff-266">Litware, Inc. kasutab kohandatud versiooni alusena selle ER-vormingu konfiguratsiooni versiooni 1.1.</span><span class="sxs-lookup"><span data-stu-id="485ff-266">Litware, Inc. will use version 1.1 of this ER format configuration as the base for the custom version.</span></span>
3. <span data-ttu-id="485ff-267">Rippmenüü dialoogiboksi avamiseks valige käsk **Loo konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="485ff-267">Select **Create configuration** to open the drop-down dialog box.</span></span> <span data-ttu-id="485ff-268">Selle dialoogiboksi abil saate luua uue konfiguratsiooni kohandatud maksevormingu jaoks.</span><span class="sxs-lookup"><span data-stu-id="485ff-268">You can use this dialog box to create a new configuration for a custom payment format.</span></span>
4. <span data-ttu-id="485ff-269">Valige väljagrupis **Uus** suvand **Tuleta nimest: BACS (UK), Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="485ff-269">In the **New** field group, select the **Derive from Name: BACS (UK), Microsoft** option.</span></span>
5. <span data-ttu-id="485ff-270">Välja **Nimi** sisestage väärtus **BACS (UK kohandatud)**.</span><span class="sxs-lookup"><span data-stu-id="485ff-270">In the **Name** field, enter **BACS (UK custom)**.</span></span>

    ![Konfiguratsiooni loomise rippmenüü dialoogiaken](./media/er-quick-start2-add-derived-format.png)

6. <span data-ttu-id="485ff-272">Valige **Konfiguratsiooni loomine**.</span><span class="sxs-lookup"><span data-stu-id="485ff-272">Select **Create configuration**.</span></span>

<span data-ttu-id="485ff-273">Luuakse ER-vormingu konfiguratsiooni **BACS (UK kohandatud)** versioon 1.1.1.</span><span class="sxs-lookup"><span data-stu-id="485ff-273">Version 1.1.1 of the **BACS (UK custom)** ER format configuration is created.</span></span> <span data-ttu-id="485ff-274">Selle versiooni [olek](general-electronic-reporting.md#component-versioning) on **Mustand** ja seda saab redigeerida.</span><span class="sxs-lookup"><span data-stu-id="485ff-274">This version has a [status](general-electronic-reporting.md#component-versioning) of **Draft** and can be edited.</span></span> <span data-ttu-id="485ff-275">Teie kohandatud ER-vormingu praegune sisu vastab Microsofti antud vormingu sisule.</span><span class="sxs-lookup"><span data-stu-id="485ff-275">The current content of your custom ER format matches the content of the format that is provided by Microsoft.</span></span>

![Konfiguratsioonide leht](./media/er-quick-start2-derived-format-configuration1.png)

### <a name="edit-a-custom-format"></a><a id="ConfigureDerivedFormat"></a><span data-ttu-id="485ff-277">Kohandatud vormingu redigeerimine</span><span class="sxs-lookup"><span data-stu-id="485ff-277">Edit a custom format</span></span>

<span data-ttu-id="485ff-278">Peate konfigureerima oma kohandatud vormingut nii, et see vastaks pangapõhistele nõuetele.</span><span class="sxs-lookup"><span data-stu-id="485ff-278">You must configure your custom format so that it meets bank-specific requirements.</span></span> <span data-ttu-id="485ff-279">Näiteks võib pank nõuda, et loodavad maksefailid sisaldaksid SWIFT-koodi (Society for Worldwide Interbank Financial Telecommunication), millele määratakse agendi roll töödeldud hankija makses.</span><span class="sxs-lookup"><span data-stu-id="485ff-279">For example, a bank might require that payment files that are generated include the Society for Worldwide Interbank Financial Telecommunication (SWIFT) code of a bank that is assigned the agent role in the processed vendor payment.</span></span> <span data-ttu-id="485ff-280">SWIFT-koodid on rahvusvahelised pangakoodid, mis tuvastavad kindlad pangad üle maailma.</span><span class="sxs-lookup"><span data-stu-id="485ff-280">SWIFT codes are international bank codes that identify specific banks worldwide.</span></span> <span data-ttu-id="485ff-281">Neid tuntakse ka panga identifikaatorkoodidena (BIC).</span><span class="sxs-lookup"><span data-stu-id="485ff-281">They are also known as Bank Identifier Codes (BICs).</span></span> <span data-ttu-id="485ff-282">SWIFT-kood peab sisaldama 11 märki ja see tuleb sisestada loodava maksefaili iga makserea algusesse.</span><span class="sxs-lookup"><span data-stu-id="485ff-282">The SWIFT code must be 11 characters long, and it must be entered at the beginning of every payment line in a generated payment file.</span></span>

1. <span data-ttu-id="485ff-283">Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="485ff-283">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="485ff-284">Laiendage lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvandit **Maksemudel** ja seejärel valige **BACS (UK kohandatud)**.</span><span class="sxs-lookup"><span data-stu-id="485ff-284">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK custom)**.</span></span>
3. <span data-ttu-id="485ff-285">Kiirkaardil **Versioonid** valige valitud konfiguratsiooni versioon **1.1.1**.</span><span class="sxs-lookup"><span data-stu-id="485ff-285">On the **Versions** FastTab, select version **1.1.1** of the selected configuration.</span></span>
4. <span data-ttu-id="485ff-286">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="485ff-286">Select **Designer**.</span></span>
5. <span data-ttu-id="485ff-287">Vorminguelementide kohta lisateabe saamiseks valige lehel **Vormingu koostaja** suvand **Kuva üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="485ff-287">On the **Format designer** page, select **Show details** to view more information about the format elements.</span></span>
6. <span data-ttu-id="485ff-288">Laiendage ja vaadake üle järgmised elemendid.</span><span class="sxs-lookup"><span data-stu-id="485ff-288">Expand and review the following elements:</span></span>

    - <span data-ttu-id="485ff-289">Tüübi **Kaust** element **BACSReportsFolder**.</span><span class="sxs-lookup"><span data-stu-id="485ff-289">The **BACSReportsFolder** element of the **Folder** type.</span></span> <span data-ttu-id="485ff-290">Seda elementi kasutatakse ZIP-vormingus väljundi loomiseks.</span><span class="sxs-lookup"><span data-stu-id="485ff-290">This element is used to generate output in ZIP format.</span></span>
    - <span data-ttu-id="485ff-291">Tüübi **Fail** element **fail**.</span><span class="sxs-lookup"><span data-stu-id="485ff-291">The **file** element of the **File** type.</span></span> <span data-ttu-id="485ff-292">Seda elementi kasutatakse TXT-vormingus maksefaili loomiseks.</span><span class="sxs-lookup"><span data-stu-id="485ff-292">This element is used to generate a payment file in TXT format.</span></span>
    - <span data-ttu-id="485ff-293">Tüübi **Järjestus** element **kanded**.</span><span class="sxs-lookup"><span data-stu-id="485ff-293">The **transactions** element of the **Sequence** type.</span></span> <span data-ttu-id="485ff-294">Seda elementi kasutatakse maksefailis üksiku makserea loomiseks.</span><span class="sxs-lookup"><span data-stu-id="485ff-294">This element is used to generate a single payment line in a payment file.</span></span>
    - <span data-ttu-id="485ff-295">Tüübi **Järjestus** element **kanne**.</span><span class="sxs-lookup"><span data-stu-id="485ff-295">The **transaction** element of the **Sequence** type.</span></span> <span data-ttu-id="485ff-296">Seda elementi kasutatakse üksiku makserea üksikute väljade loomiseks.</span><span class="sxs-lookup"><span data-stu-id="485ff-296">This element is used to generate individual fields of a single payment line.</span></span>

7. <span data-ttu-id="485ff-297">Valige element **kanne**.</span><span class="sxs-lookup"><span data-stu-id="485ff-297">Select the **transaction** element.</span></span>

    ![Kande element ER-toimingute koostajas](./media/er-quick-start2-derived-format0.png)

    > [!NOTE]
    > <span data-ttu-id="485ff-299">Antud aruanne on konfigureeritud nii, et <a id="PositionRoutingNumber"></a>iga makserida algaks panga registreerimisnumbriga.</span><span class="sxs-lookup"><span data-stu-id="485ff-299">The provided report is configured so that <a id="PositionRoutingNumber"></a>every payment line starts with the bank routing number.</span></span> <span data-ttu-id="485ff-300">Selleks otstarbeks kasutatakse vorminguelementi **VendBankRouteNum**.</span><span class="sxs-lookup"><span data-stu-id="485ff-300">The **vendBankRouteNum** format element is used for this purpose.</span></span> 

8. <span data-ttu-id="485ff-301">Valige **Lisa** ja seejärel valige lisatava vorminguelemendi tüüp **Tekst\\String**.</span><span class="sxs-lookup"><span data-stu-id="485ff-301">Select **Add**, and then select the **Text\\String** type of the format element that you're adding:</span></span>

    1. <span data-ttu-id="485ff-302">Väljale **Nimi** sisestage väärtus **vendBankSWIFT**.</span><span class="sxs-lookup"><span data-stu-id="485ff-302">In the **Name** field, enter **vendBankSWIFT**.</span></span>
    2. <span data-ttu-id="485ff-303">Sisestage väljale **Minimaalne pikkus** väärtus **11**.</span><span class="sxs-lookup"><span data-stu-id="485ff-303">In the **Minimum length** field, enter **11**.</span></span>
    3. <span data-ttu-id="485ff-304">Sisestage väljale **Maksimaalne pikkus** väärtus **11**.</span><span class="sxs-lookup"><span data-stu-id="485ff-304">In the **Maximum length** field, enter **11**.</span></span>
    4. <span data-ttu-id="485ff-305">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="485ff-305">Select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="485ff-306">Elementi **VendBankSWIFT** kasutatakse hankija panga SWIFT-koodi sisestamiseks loodud failides.</span><span class="sxs-lookup"><span data-stu-id="485ff-306">The **vendBankSWIFT** element will be used to enter the SWIFT code of a vendor bank in generated files.</span></span>

9. <span data-ttu-id="485ff-307">Valige vormingustruktuuri puus **vendBankSWIFT**.</span><span class="sxs-lookup"><span data-stu-id="485ff-307">In the format structure tree, select **vendBankSWIFT**.</span></span>
10. <span data-ttu-id="485ff-308">Valige **Nihuta üles**, et liigutada valitud vorminguelementi ühe taseme võrra ülespoole.</span><span class="sxs-lookup"><span data-stu-id="485ff-308">Select **Move up** to move the selected format element up one level.</span></span> <span data-ttu-id="485ff-309">Korrake seda etappi senikaua, kuni element **vendBankSWIFT** on <a id="PositionSWIFTCode"></a>esimene element peamise elemendi **kanne** all.</span><span class="sxs-lookup"><span data-stu-id="485ff-309">Repeat this step until the **vendBankSWIFT** element is the <a id="PositionSWIFTCode"></a>first element under the parent **transaction** element.</span></span>

    ![VendBankSWIFT on ER-toimingute koostaja kande esimene element](./media/er-quick-start2-derived-format1.png)

11. <span data-ttu-id="485ff-311">Kui suvand **vendBankSWIFT** on vormingustruktuuri puus valitud, valige vahekaart **Vastendamine** ja seejärel laiendage andmeallikat **mudel**.</span><span class="sxs-lookup"><span data-stu-id="485ff-311">While the **vendBankSWIFT** is still selected in the format structure tree, select the **Mapping** tab, and then expand the **model** data source.</span></span>
12. <span data-ttu-id="485ff-312">Laiendage suvandit **model.Payment** \> **model.Payment.CreditorAgent** ja valige andmeallika väli **model.Payment.CreditorAgent.BICFI**.</span><span class="sxs-lookup"><span data-stu-id="485ff-312">Expand **model.Payment** \> **model.Payment.CreditorAgent**, and select the **model.Payment.CreditorAgent.BICFI** data source field.</span></span> <span data-ttu-id="485ff-313">See andmeallika väli näitab hankija panga SWIFT-koodi, millele määratakse agendi roll töödeldud hankija makses.</span><span class="sxs-lookup"><span data-stu-id="485ff-313">This data source field exposes the SWIFT code of a vendor bank that is assigned the agent role in the processed vendor payment.</span></span>
13. <span data-ttu-id="485ff-314">Valige **Seo**.</span><span class="sxs-lookup"><span data-stu-id="485ff-314">Select **Bind**.</span></span> <span data-ttu-id="485ff-315">Vorminguelement **VendBankSWIFT** on nüüd seotud andmeallika väljaga **model.Payment.CreditorAgent.BICFI**, et SWIFT-koode sisestatakse loodud maksefailidesse.</span><span class="sxs-lookup"><span data-stu-id="485ff-315">The **vendBankSWIFT** format element is now bound with the **model.Payment.CreditorAgent.BICFI** data source field, so that SWIFT codes will be entered in generated payment files.</span></span>

    ![Andmeallika väljaga model.Payment.CreditorAgent.BICFI seotud vorminguelement vendBankSWIFT ER-toimingute koostajas](./media/er-quick-start2-derived-format2.png)

14. <span data-ttu-id="485ff-317">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="485ff-317">Select **Save**.</span></span>
15. <span data-ttu-id="485ff-318">Sulgege koostaja leht.</span><span class="sxs-lookup"><span data-stu-id="485ff-318">Close the designer page.</span></span>

### <a name="mark-a-custom-format-as-runnable"></a><a id="MarkFormatRunnable"></a><span data-ttu-id="485ff-319">Kohandatud vormingu märkimine käitatavaks</span><span class="sxs-lookup"><span data-stu-id="485ff-319">Mark a custom format as runnable</span></span>

<span data-ttu-id="485ff-320">Kui teie kohandatud vormingu esimene versioon on loodud ja selle olek on **Mustand**, saate selle käitada testimise eesmärgil.</span><span class="sxs-lookup"><span data-stu-id="485ff-320">Now that the first version of your custom format has been created and has a status of **Draft**, you can run it for testing purposes.</span></span> <span data-ttu-id="485ff-321">Aruande käitamiseks peate töötlema hankija makset makseviisi abil, mis viitab teie kohandatud ER-vormingule.</span><span class="sxs-lookup"><span data-stu-id="485ff-321">To run the report, you must process a vendor payment by using the payment method that refers to your custom ER format.</span></span> <span data-ttu-id="485ff-322">Kui toote rakendusest ER-vormingu võetakse vaikimisi [arvesse](general-electronic-reporting.md#component-versioning) ainult versioone, mille olek on **Lõpule viidud** või **Ühiskasutusse antud**.</span><span class="sxs-lookup"><span data-stu-id="485ff-322">By default, when you call an ER format from the application, only versions that have a status of **Completed** or **Shared** are [considered](general-electronic-reporting.md#component-versioning).</span></span> <span data-ttu-id="485ff-323">Selle käitumise abil saab vältida ER-vormingute kasutamist, mille koostamine on lõpetamata.</span><span class="sxs-lookup"><span data-stu-id="485ff-323">This behavior helps prevent ER formats that have unfinished designs from being used.</span></span> <span data-ttu-id="485ff-324">Kuid oma testikäivitustel saate sundida rakendust kasutama teie ER-vormingu versiooni, mille olekuks on **Mustand**.</span><span class="sxs-lookup"><span data-stu-id="485ff-324">However, for your test runs, you can force the application to use the version of your ER format that has a status of **Draft**.</span></span> <span data-ttu-id="485ff-325">Sedasi saate korrigeerida praeguse vormingu versiooni, kui muudatusi on vaja.</span><span class="sxs-lookup"><span data-stu-id="485ff-325">In this way, you can adjust the current format version if any modifications are required.</span></span> <span data-ttu-id="485ff-326">Lisateavet vt jaotisest [Kohaldatavus](electronic-reporting-destinations.md#applicability).</span><span class="sxs-lookup"><span data-stu-id="485ff-326">For more information, see [Applicability](electronic-reporting-destinations.md#applicability).</span></span>

<span data-ttu-id="485ff-327">ER-vormingu mustandversiooni kasutamiseks peate ER-vormingu selgelt märgistama.</span><span class="sxs-lookup"><span data-stu-id="485ff-327">To use the draft version of an ER format, you must explicitly mark the ER format.</span></span>

1. <span data-ttu-id="485ff-328">Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="485ff-328">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="485ff-329">Valige lehe **Konfiguratsioonid** toimingupaani vahekaardi **Konfiguratsioonid** grupist **Täpsemad sätted** valik **Kasutaja parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="485ff-329">On the **Configurations** page, on the Action Pane, on the **Configurations** tab, in the **Advanced settings** group, select **User parameters**.</span></span>
3. <span data-ttu-id="485ff-330">Seadke dialoogiboksis **Kasutaja parameetrid** suvandi **Käivitamissätted** väärtuseks **Jah** ja valige seejärel **OK**.</span><span class="sxs-lookup"><span data-stu-id="485ff-330">In the **User parameters** dialog box, set the **Run settings** option to **Yes**, and then select **OK**.</span></span>
4. <span data-ttu-id="485ff-331">Vastavalt vajadusele valige **Redigeeri**, et muuta praegune leht redigeeritavaks.</span><span class="sxs-lookup"><span data-stu-id="485ff-331">Select **Edit** to make the current page editable, as required.</span></span>
5. <span data-ttu-id="485ff-332">Valige vasakpoolse paani konfiguratsioonipuus **BACS (UK kohandatud)**.</span><span class="sxs-lookup"><span data-stu-id="485ff-332">In the configuration tree in the left pane, select **BACS (UK custom)**.</span></span>
6. <span data-ttu-id="485ff-333">Seadke suvandi **Käivita mustand** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="485ff-333">Set the **Run Draft** option to **Yes**.</span></span>

    ![Suvand Käivita mustand lehel Konfiguratsioonid](./media/er-quick-start2-derived-format-configuration2.png)

## <a name="process-a-vendor-payment-by-using-the-custom-er-format"></a><a id="ProcessVendorPayment2"></a><span data-ttu-id="485ff-335">Hankija makse töötlemine kohandatud ER-vormingu abil</span><span class="sxs-lookup"><span data-stu-id="485ff-335">Process a vendor payment by using the custom ER format</span></span>

### <a name="set-up-the-electronic-payment-method"></a><a id="ConfigureMethodOfPayment2"></a><span data-ttu-id="485ff-336">Elektroonilise makseviisi seadistamine</span><span class="sxs-lookup"><span data-stu-id="485ff-336">Set up the electronic payment method</span></span>

<span data-ttu-id="485ff-337">Peate konfigureerima elektroonilise makseviisi, et teie kohandatud ER-vormingut kasutataks hankija maksete töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="485ff-337">You must configure the electronic method of payment so that your custom ER format is used to process vendor payments.</span></span>

1. <span data-ttu-id="485ff-338">Avage **Ostureskontro** \> **Maksmise seadistamine** \> **Makseviisid**.</span><span class="sxs-lookup"><span data-stu-id="485ff-338">Go to **Accounts payable** \> **Payment setup** \> **Methods of payment**.</span></span>
2. <span data-ttu-id="485ff-339">Valige lehe **Makseviisid – hankijad** vasakpoolsel paanil makseviis **Elektrooniline**.</span><span class="sxs-lookup"><span data-stu-id="485ff-339">On the **Methods of payment - vendors** page, select the **Electronic** method of payment in the left pane.</span></span>
3. <span data-ttu-id="485ff-340">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="485ff-340">Select **Edit**.</span></span>
4. <span data-ttu-id="485ff-341">Seadistage kiirkaardil **Failivorming** suvandi **Üldine elektrooniline ekspordivorming** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="485ff-341">On the **File format** FastTab, set the **General electronic export format** option to **Yes**.</span></span>
5. <span data-ttu-id="485ff-342">Valige väljal **Ekspordivormingu konfiguratsioon** vormingu konfiguratsioon **BACS (UK kohandatud)**.</span><span class="sxs-lookup"><span data-stu-id="485ff-342">In the **Export format configuration** field, select the **BACS (UK custom)** format configuration.</span></span>

    ![Makseviisid - hankijate leht](./media/er-quick-start2-method-of-payment2.png)

6. <span data-ttu-id="485ff-344">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="485ff-344">Select **Save**.</span></span>

### <a name="process-a-vendor-payment"></a><a id="ProcessPayment2"></a><span data-ttu-id="485ff-345">Hankija makse töötlemine</span><span class="sxs-lookup"><span data-stu-id="485ff-345">Process a vendor payment</span></span>

1. <span data-ttu-id="485ff-346">Avage **Ostureskontro** \> **Maksed** \> **Hankija maksete tööleht**.</span><span class="sxs-lookup"><span data-stu-id="485ff-346">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="485ff-347">Valige lehel **Hankija maksete tööleht** eelnevalt loodud maksete tööleht.</span><span class="sxs-lookup"><span data-stu-id="485ff-347">On the **Vendor payment journal** page, select the payment journal that you created earlier.</span></span>
3. <span data-ttu-id="485ff-348">Valige **Read**.</span><span class="sxs-lookup"><span data-stu-id="485ff-348">Select **Lines**.</span></span>
4. <span data-ttu-id="485ff-349">Valige lehe **Hankija maksed** ruudustiku kohalt **Makse olek** \> **Puudub**.</span><span class="sxs-lookup"><span data-stu-id="485ff-349">On the **Vendor payments** page, above the grid, select **Payment status** \> **None**.</span></span>
5. <span data-ttu-id="485ff-350">Valige **Loo makse**.</span><span class="sxs-lookup"><span data-stu-id="485ff-350">Select **Generate payment**.</span></span>
6. <span data-ttu-id="485ff-351">Sisestage dialoogiboksi **Loo maksed** järgmine teave.</span><span class="sxs-lookup"><span data-stu-id="485ff-351">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="485ff-352">Valige väljal **Makseviis** **Elektrooniline**.</span><span class="sxs-lookup"><span data-stu-id="485ff-352">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="485ff-353">Valige väljal **Pangakonto** suvand **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="485ff-353">In the **Bank account** field, select **GBSI OPER**.</span></span>

7. <span data-ttu-id="485ff-354">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="485ff-354">Select **OK**.</span></span>
8. <span data-ttu-id="485ff-355">Määrake dialoogiboksis **Elektroonilise aruande parameetrid** suvandi **Prindi kontrollaruanne** väärtuseks **Jah** ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="485ff-355">In the **Electronic report parameters** dialog box, set the **Print control report** option to **Yes**, and then select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="485ff-356">Lisaks maksefailile saate luua ainult kontrollaruande.</span><span class="sxs-lookup"><span data-stu-id="485ff-356">In addition to the payment file, you can generate only the control report.</span></span>

9. <span data-ttu-id="485ff-357">Laadige alla ZIP-fail ja seejärel ekstraktige sellest järgmised failid.</span><span class="sxs-lookup"><span data-stu-id="485ff-357">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="485ff-358">Kontrollaruanne Exceli vormingus</span><span class="sxs-lookup"><span data-stu-id="485ff-358">The control report in Excel format</span></span>
    - <span data-ttu-id="485ff-359">Maksefail TXT-vormingus</span><span class="sxs-lookup"><span data-stu-id="485ff-359">The payment file in TXT format</span></span>

        <span data-ttu-id="485ff-360">Pange tähele, et vastavalt teie kohandatud ER-vormingu struktuurile [algab](#PositionSWIFTCode) loodud faili makserida nüüd SWIFT-koodiga, mis [sisestati](#DefineSWIFTCode) selle hankija pangakontole, kelle makse on töödeldud.</span><span class="sxs-lookup"><span data-stu-id="485ff-360">Notice that, in accordance with the structure of your custom ER format, the payment line in the generated file now [starts](#PositionSWIFTCode) with the SWIFT code that was [entered](#DefineSWIFTCode) for the bank account of the vendor whose payment has been processed.</span></span>

        ![Maksefail TXT-vormingus](./media/er-quick-start2-payment-file2.png)

## <a name="import-new-versions-of-the-standard-er-format-configurations"></a><a id="ImportERSolution2"></a><span data-ttu-id="485ff-362">Standardse ER‑vormingu konfiguratsiooni uute versioonide importimine</span><span class="sxs-lookup"><span data-stu-id="485ff-362">Import new versions of the standard ER format configurations</span></span>

<span data-ttu-id="485ff-363">Käesolevas jaotises kuvatud näite puhul kuvatakse teile teatis teabebaasi artikli [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046) kohta.</span><span class="sxs-lookup"><span data-stu-id="485ff-363">For the example that is shown in this section, you receive a notification about Knowledge Base article [KB3763330](https://fix.lcs.dynamics.com/Issue/Details?kb=3182046).</span></span> <span data-ttu-id="485ff-364">Selle teatisega teavitatakse teid Microsofti avaldatud uuest ER-vormingu **BACS (UK)** versioonist.</span><span class="sxs-lookup"><span data-stu-id="485ff-364">This notification informs you about the new version of the **BACS (UK)** ER format that has been published by Microsoft.</span></span> <span data-ttu-id="485ff-365">Lisaks kontrollaruandele võimaldab see uus versioon kasutajatel luua maksesoovituse aruannet ja osalemismärkuse aruannet hankija makse töötlemise ajal.</span><span class="sxs-lookup"><span data-stu-id="485ff-365">In addition to the control report, this new version lets users generate the payment advice report and the attending note report while a vendor payment is being processed.</span></span> <span data-ttu-id="485ff-366">Soovite hakata seda funktsiooni kasutama.</span><span class="sxs-lookup"><span data-stu-id="485ff-366">You want to start to use that functionality.</span></span>

### <a name="import-new-versions-of-the-standard-er-configurations"></a><a id="ImportERFormat2"></a><span data-ttu-id="485ff-367">Standardse ER‑konfiguratsiooni uute versioonide importimine</span><span class="sxs-lookup"><span data-stu-id="485ff-367">Import new versions of the standard ER configurations</span></span>

<span data-ttu-id="485ff-368">Oma praegusesse Finance'i eksemplari ER-konfiguratsioonide uute versioonide lisamiseks peate importima need enda konfigureeritud ER-[hoidlast](general-electronic-reporting.md#Repository).</span><span class="sxs-lookup"><span data-stu-id="485ff-368">To add new versions of the ER configurations to the current Finance instance, you must import them from the ER [repository](general-electronic-reporting.md#Repository) that you've configured.</span></span>

1. <span data-ttu-id="485ff-369">Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="485ff-369">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="485ff-370">Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Konfiguratsioonipakkujad** paan **Microsoft** ja seejärel valige pakkuja Microsoft hoidlate loendi kuvamiseks **Hoidlad**.</span><span class="sxs-lookup"><span data-stu-id="485ff-370">On the **Localization configurations** page, in the **Configuration providers** section, select the **Microsoft** tile, and then select **Repositories** to view the list of repositories for the Microsoft provider.</span></span>
3. <span data-ttu-id="485ff-371">Valige lehel **Konfiguratsioonihoidlad** hoidla tüübiga **Globaalne** ja seejärel valige käsk **Ava**.</span><span class="sxs-lookup"><span data-stu-id="485ff-371">On the **Configuration repositories** page, select the repository of the **Global** type, and then select **Open**.</span></span> <span data-ttu-id="485ff-372">Kui teilt küsitakse autoriseerimist ühenduse loomiseks Regulatory Configuration Service'iga, järgige autoriseerimise juhiseid.</span><span class="sxs-lookup"><span data-stu-id="485ff-372">If you're prompted for authorization to connect to Regulatory Configuration Service, follow the authorization instructions.</span></span>
4. <span data-ttu-id="485ff-373">Valige lehel **Konfiguratsioonihoidla** vasakpoolselt paanilt konfiguratsioonipuult vormingu **BACS (UK)** konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="485ff-373">On the **Configuration repository** page, in the configuration tree in the left pane, select the **BACS (UK)** format configuration.</span></span>
5. <span data-ttu-id="485ff-374">Kiirkaardil **Versioonid** valige valitud ER-vormingu konfiguratsiooni versioon **3.3**.</span><span class="sxs-lookup"><span data-stu-id="485ff-374">On the **Versions** FastTab, select version **3.3** of the selected ER format configuration.</span></span>
6. <span data-ttu-id="485ff-375">Valige käsk **Impordi**, et laadida valitud versioon globaalsest hoidlast alla Finance'i praegusesse eksemplari.</span><span class="sxs-lookup"><span data-stu-id="485ff-375">Select **Import** to download the selected version from the Global repository to the current Finance instance.</span></span>

![Konfiguratsioonihoidla leht](./media/er-quick-start2-import-solution2.png)

> [!TIP]
> <span data-ttu-id="485ff-377">Kui teil on probleeme [globaalsele hoidlale](er-download-configurations-global-repo.md) juurde pääsemisega, saate selle asemel [laadida konfiguratsioonid alla](download-electronic-reporting-configuration-lcs.md) LCS-ist.</span><span class="sxs-lookup"><span data-stu-id="485ff-377">If you have trouble accessing the [Global repository](er-download-configurations-global-repo.md), you can [download configurations](download-electronic-reporting-configuration-lcs.md) from LCS instead.</span></span>

### <a name="review-the-imported-er-format-configurations"></a><a id="ReviewImportedERFormat"></a><span data-ttu-id="485ff-378">Imporditud ER-vormingu konfiguratsioonide ülevaatamine</span><span class="sxs-lookup"><span data-stu-id="485ff-378">Review the imported ER format configurations</span></span>

1. <span data-ttu-id="485ff-379">Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="485ff-379">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="485ff-380">Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Konfiguratsioonid** paan **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="485ff-380">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="485ff-381">Laiendage lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvandit **Maksemudel** ja seejärel valige **BACS (UK)**.</span><span class="sxs-lookup"><span data-stu-id="485ff-381">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK)**.</span></span>
4. <span data-ttu-id="485ff-382">Kiirkaardil **Versioonid** valige versioon **3.3**.</span><span class="sxs-lookup"><span data-stu-id="485ff-382">On the **Versions** FastTab, select version **3.3**.</span></span>
5. <span data-ttu-id="485ff-383">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="485ff-383">Select **Designer**.</span></span>
6. <span data-ttu-id="485ff-384">Laiendage lehel **Vormingu koostaja** vorminguelementi **BACSReportsFolder**.</span><span class="sxs-lookup"><span data-stu-id="485ff-384">On the **Format designer** page, expand the **BACSReportsFolder** format element.</span></span>
7.  <span data-ttu-id="485ff-385">Pange tähele, et versioon 3.3 sisaldab vorminguelementi **PaymentAdviceReport**, mida kasutatakse maksesoovituse aruande loomiseks hankija makse töötlemisel.</span><span class="sxs-lookup"><span data-stu-id="485ff-385">Notice that version 3.3 contains the **PaymentAdviceReport** format element that is used to generate a payment advice report when a vendor payment is processed.</span></span>

    ![Vorminguelement PaymentAdviceReport ER-toimingute koostajas](./media/er-quick-start2-imported-solution2.png)

8. <span data-ttu-id="485ff-387">Sulgege koostaja leht.</span><span class="sxs-lookup"><span data-stu-id="485ff-387">Close the designer page.</span></span>

## <a name="adopt-the-changes-in-the-new-version-of-an-imported-format-in-a-custom-format"></a><a id="AdoptNewBaseVersion"></a><span data-ttu-id="485ff-388">Muudatuste kasutuselevõtmine kohandatud vormingu imporditud vormingu uues versioonis</span><span class="sxs-lookup"><span data-stu-id="485ff-388">Adopt the changes in the new version of an imported format in a custom format</span></span>

### <a name="complete-the-current-draft-version-of-a-custom-format"></a><a id="CompleteDerivedFormat"></a><span data-ttu-id="485ff-389">Kohandatud vormingu praeguse mustandversiooni lõpule viimine</span><span class="sxs-lookup"><span data-stu-id="485ff-389">Complete the current draft version of a custom format</span></span>

<span data-ttu-id="485ff-390">Kui soovite jätta alles oma kohandatud vormingu praeguse oleku, viige lõpule mustandi versioon 1.1.1, muutes selle olek **Mustand** olekuks **Lõpule viidud**.</span><span class="sxs-lookup"><span data-stu-id="485ff-390">If you want to keep the current state of your custom format, complete the draft version 1.1.1 by changing its status from **Draft** to **Completed**.</span></span>

1. <span data-ttu-id="485ff-391">Avage **Organisatsiooni haldamine** \> **Tööruumid** \> **Elektrooniline aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="485ff-391">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="485ff-392">Valige lehe **Lokaliseerimise konfiguratsioonid** jaotises **Konfiguratsioonid** paan **Aruandluse konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="485ff-392">On the **Localization configurations** page, in the **Configurations** section, select the **Reporting configurations** tile.</span></span>
3. <span data-ttu-id="485ff-393">Laiendage lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvandit **Maksemudel**, laiendage **BACS (UK)** ja seejärel valige **BACS (UK kohandatud)**.</span><span class="sxs-lookup"><span data-stu-id="485ff-393">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, expand **BACS (UK)**, and then select **BACS (UK custom)**.</span></span>
4. <span data-ttu-id="485ff-394">Valige kiirkaardil **Versioonid** **Muuda olekut** \> **Lõpuleviimine** ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="485ff-394">On the **Versions** FastTab, select **Change status** \> **Complete**, and then select **OK**.</span></span>

<span data-ttu-id="485ff-395">Versiooni 1.1.1 olek **Mustand** muudetakse olekuks **Lõpule viidud** ja versioon muudetakse kirjutuskaitstuks.</span><span class="sxs-lookup"><span data-stu-id="485ff-395">The status of version 1.1.1 is changed from **Draft** to **Completed**, and the version becomes read-only.</span></span> <span data-ttu-id="485ff-396">Lisatud on uus redigeeritav versioon, 1.1.2, ja selle olekuks on **Mustand**.</span><span class="sxs-lookup"><span data-stu-id="485ff-396">A new editable version, 1.1.2, has been added and has a status of **Draft**.</span></span> <span data-ttu-id="485ff-397">Seda versiooni saate kasutada oma kohandatud ER-vormingu täiendavate muudatuste tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="485ff-397">You can use this version to make further changes in your custom ER format.</span></span>

### <a name="rebase-a-custom-format-to-a-new-base-version"></a><a id="RebaseDerivedFormat"></a><span data-ttu-id="485ff-398">Uuele alusversioonile kohandatud vormingu aluse muutmine</span><span class="sxs-lookup"><span data-stu-id="485ff-398">Rebase a custom format to a new base version</span></span>

<span data-ttu-id="485ff-399">Oma kohanduses vormingu **BACS (UK)** versiooni 3.3 uue funktsiooni kasutamiseks, peate muutma kohandatud konfiguratsiooni **BACS (UK kohandatud)** aluskonfiguratsiooni versiooni.</span><span class="sxs-lookup"><span data-stu-id="485ff-399">To start to use the new functionality of version 3.3 of the **BACS (UK)** format in your customization, you must change the base configuration version for the custom configuration, **BACS (UK custom)**.</span></span> <span data-ttu-id="485ff-400">Seda protsessi nimetatakse [aluse muutmiseks](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase).</span><span class="sxs-lookup"><span data-stu-id="485ff-400">This process is known as [rebasing](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase).</span></span> <span data-ttu-id="485ff-401">**BACS (UK)** versiooni 1.1 asemel kasutage uut versiooni 3.3.</span><span class="sxs-lookup"><span data-stu-id="485ff-401">Instead of version 1.1 of **BACS (UK)**, use version 3.3.</span></span>

1. <span data-ttu-id="485ff-402">Minge jaotisse **Organisatsiooni haldamine** \> **Elektrooniline aruandlus** \> **Konfiguratsioonid**.</span><span class="sxs-lookup"><span data-stu-id="485ff-402">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="485ff-403">Laiendage lehe **Konfiguratsioonid** vasakpoolsel paanil konfiguratsioonipuus suvandit **Maksemudel** ja seejärel valige **BACS (UK kohandatud)**.</span><span class="sxs-lookup"><span data-stu-id="485ff-403">On the **Configurations** page, in the configuration tree in the left pane, expand **Payment model**, and then select **BACS (UK custom)**.</span></span>
3. <span data-ttu-id="485ff-404">Valige kiirkaardil **Versioonid** versioon **1.1.2** ja valige **Muuda alust**.</span><span class="sxs-lookup"><span data-stu-id="485ff-404">On the **Versions** FastTab, select version **1.1.2**, and then select **Rebase**.</span></span>
4. <span data-ttu-id="485ff-405">Valige dialoogiboksi **Muuda alust** väljal **Sihtversioon** aluskonfiguratsiooni versioon **3.3**, et rakendada see uue alusena ja kasutada seda konfiguratsiooni värskendamiseks.</span><span class="sxs-lookup"><span data-stu-id="485ff-405">In the **Rebase** dialog box, in the **Target version** field, select version **3.3** of the base configuration to apply it as the new base and use it to update the configuration.</span></span>

    ![Dialoogiakna aluse muutmine](./media/er-quick-start2-rebase1.png)

5. <span data-ttu-id="485ff-407">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="485ff-407">Select **OK**.</span></span>
6. <span data-ttu-id="485ff-408">Pange tähele, et mustandi versiooni number **1.1.2** on muudetud numbriks **3.3.2**, et kajastada alusversiooni muudatust.</span><span class="sxs-lookup"><span data-stu-id="485ff-408">Notice that the number of the draft version has been changed from **1.1.2** to **3.3.2** to reflect the change in the base version.</span></span>

    <span data-ttu-id="485ff-409">Kohandatud versiooni ja uue alusversiooni liitmisel võidakse avastada konflikte osade vormingumuudatuste tõttu, mida ei saa automaatselt ühendada.</span><span class="sxs-lookup"><span data-stu-id="485ff-409">When the custom version and a new base version are merged, some conflicts might be discovered because of format changes that can't be merged automatically.</span></span>

    ![Muudetud alusega konfiguratsioon, millel on konflikte lehel Konfiguratsioonid](./media/er-quick-start2-rebase2.png)

    <span data-ttu-id="485ff-411">Konfliktide avastamisel tuleb need käsitsi lahendada vormingu koostajas.</span><span class="sxs-lookup"><span data-stu-id="485ff-411">If conflicts are discovered, they must be manually resolved in the format designer.</span></span>

7. <span data-ttu-id="485ff-412">Kiirkaardil **Versioonid** valige versioon **3.3.2**.</span><span class="sxs-lookup"><span data-stu-id="485ff-412">On the **Versions** FastTab, select version **3.3.2**.</span></span>
8. <span data-ttu-id="485ff-413">Valige **Kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="485ff-413">Select **Designer**.</span></span>
9. <span data-ttu-id="485ff-414">Valige lehe **Vormingu koostaja** kiirkaardil **Üksikasjad** aluse muutmise konflikti kirje ja seejärel valige **Rakenda alusväärtus**.</span><span class="sxs-lookup"><span data-stu-id="485ff-414">On the **Format designer** page, on the **Details** FastTab, select a rebase conflict record, and then select **Apply base value**.</span></span>

    ![Aluse muutmise konflikti kirje ER-toimingute koostajas](./media/er-quick-start2-rebase3.png)

10. <span data-ttu-id="485ff-416">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="485ff-416">Select **Save**.</span></span>

    <span data-ttu-id="485ff-417">Aluse muutmise konflikti kirje ei tohiks olla enam kuvatud kiirkaardil **Üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="485ff-417">The rebase conflict record should no longer appear on the **Details** FastTab.</span></span>

    ![Konflikt lahendatud ER-toimingute koostajas](./media/er-quick-start2-rebase4.png)

    > [!NOTE]
    > <span data-ttu-id="485ff-419">Lahendasite konflikti kinnitades, et selles ER-vormingus tuleb kasutada alusmudeli versiooni 3.</span><span class="sxs-lookup"><span data-stu-id="485ff-419">You resolved the conflict by confirming that version 3 of the base model must be used in this ER format.</span></span>

11. <span data-ttu-id="485ff-420">Laiendage suvandit **BACSReportsFolder** \> **fail** \> **kanded** \> **kanne**.</span><span class="sxs-lookup"><span data-stu-id="485ff-420">Expand **BACSReportsFolder** \> **file** \> **transactions** \> **transaction**.</span></span>
12. <span data-ttu-id="485ff-421">Pange tähele, et vahekaardil **Vastendamine** sisaldab teie kohandatud ER-vormingu versioon 3.3.2 nii teie kohandust (vorminguelementi **vendBankSWIFT** ja selle sidumist) kui ka Microsofti antud ER-vormingu aluse versiooni 3.3 uut funktsiooni (vorminguelementi **PaymentAdviceReport** koos selle pesastatud elementide ja konfigureeritud sidumistega).</span><span class="sxs-lookup"><span data-stu-id="485ff-421">On the **Mapping** tab, notice that version 3.3.2 of your custom ER format contains both your customization (the **vendBankSWIFT** format element and its binding) and the new functionality of version 3.3 of the base ER format that was provided by Microsoft (the **PaymentAdviceReport** format element together with its nested elements and configured bindings).</span></span> <span data-ttu-id="485ff-422">Vaid mõne hiireklõpsuga võtsite vastu uue alusversiooni muudatused, ühendades need oma kohandusega.</span><span class="sxs-lookup"><span data-stu-id="485ff-422">In just a few mouse clicks, you adopted the modifications of a new base version by merging them with your customization.</span></span>

    ![Ühendatud vorming ER-toimingute koostajas](./media/er-quick-start2-rebase5.png)

13. <span data-ttu-id="485ff-424">Sulgege koostaja leht.</span><span class="sxs-lookup"><span data-stu-id="485ff-424">Close the designer page.</span></span>

> [!NOTE]
> <span data-ttu-id="485ff-425">Aluse muutmise tegevus on tühistatav.</span><span class="sxs-lookup"><span data-stu-id="485ff-425">The rebase action is reversible.</span></span> <span data-ttu-id="485ff-426">Selle aluse muutmise tühistamiseks valige vahekaardil **Versioonid** vormingu **BACS (UK kohandatud)** versioon **1.1.1** ja seejärel valige **Hangi see versioon**.</span><span class="sxs-lookup"><span data-stu-id="485ff-426">To cancel this rebase, select version **1.1.1** of the **BACS (UK custom)** format on the **Versions** FastTab, and then select **Get this version**.</span></span> <span data-ttu-id="485ff-427">Versiooni 3.3.2 numbriks pannakse seejärel 1.1.2 ja mustandi versiooni 1.1.2 sisu vastab versiooni 1.1.1 sisule.</span><span class="sxs-lookup"><span data-stu-id="485ff-427">Version 3.3.2 will then be renumbered 1.1.2, and the content of draft version 1.1.2 will match the content of version 1.1.1.</span></span>

### <a name="process-a-vendor-payment-by-using-a-rebased-er-format"></a><a id="ProcessPayment3"></a><span data-ttu-id="485ff-428">Hankija makse töötlemine muudetud alusega ER-vormingu abil</span><span class="sxs-lookup"><span data-stu-id="485ff-428">Process a vendor payment by using a rebased ER format</span></span>

1. <span data-ttu-id="485ff-429">Avage **Ostureskontro** \> **Maksed** \> **Hankija maksete tööleht**.</span><span class="sxs-lookup"><span data-stu-id="485ff-429">Go to **Accounts payable** \> **Payments** \> **Vendor payment journal**.</span></span>
2. <span data-ttu-id="485ff-430">Valige lehel **Hankija maksete tööleht** eelnevalt loodud maksete tööleht.</span><span class="sxs-lookup"><span data-stu-id="485ff-430">On the **Vendor payment journal** page, select the payment journal that you created earlier.</span></span>
3. <span data-ttu-id="485ff-431">Valige **Read**.</span><span class="sxs-lookup"><span data-stu-id="485ff-431">Select **Lines**.</span></span>
4. <span data-ttu-id="485ff-432">Valige lehe **Hankija maksed** ruudustiku kohalt **Makse olek** \> **Puudub**.</span><span class="sxs-lookup"><span data-stu-id="485ff-432">On the **Vendor payments** page, above the grid, select **Payment status** \> **None**.</span></span>
5. <span data-ttu-id="485ff-433">Valige **Loo makse**.</span><span class="sxs-lookup"><span data-stu-id="485ff-433">Select **Generate payment**.</span></span>
6. <span data-ttu-id="485ff-434">Sisestage dialoogiboksi **Loo maksed** järgmine teave.</span><span class="sxs-lookup"><span data-stu-id="485ff-434">In the **Generate payments** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="485ff-435">Valige väljal **Makseviis** **Elektrooniline**.</span><span class="sxs-lookup"><span data-stu-id="485ff-435">In the **Method of payment** field, select **Electronic**.</span></span>
    - <span data-ttu-id="485ff-436">Valige väljal **Pangakonto** suvand **GBSI OPER**.</span><span class="sxs-lookup"><span data-stu-id="485ff-436">In the **Bank account** field, select **GBSI OPER**.</span></span>

7. <span data-ttu-id="485ff-437">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="485ff-437">Select **OK**.</span></span>
8. <span data-ttu-id="485ff-438">Sisestage dialoogiboksi **Elektroonilise aruande parameetrid** järgmine teave.</span><span class="sxs-lookup"><span data-stu-id="485ff-438">In the **Electronic report parameters** dialog box, enter the following information:</span></span>

    - <span data-ttu-id="485ff-439">Seadistage valik **Kontrollaruande printimine** olekusse **Jah**.</span><span class="sxs-lookup"><span data-stu-id="485ff-439">Set the **Print control report** option to **Yes**.</span></span>
    - <span data-ttu-id="485ff-440">Seadistage valik **Maksesoovituse printimine** olekusse **Jah**.</span><span class="sxs-lookup"><span data-stu-id="485ff-440">Set the **Print payment advice** option to **Yes**.</span></span>

    ![Elektroonilise aruande parameetrite dialoogiaken](./media/er-quick-start2-payment-dialog2.png)

    > [!NOTE]
    > <span data-ttu-id="485ff-442">Lisaks maksefailile saate nüüd luua nii kontrollaruande kui ka maksesoovituse aruande.</span><span class="sxs-lookup"><span data-stu-id="485ff-442">In addition to the payment file, you can now generate both the control report and the payment advice report.</span></span>

9. <span data-ttu-id="485ff-443">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="485ff-443">Select **OK**.</span></span>
10. <span data-ttu-id="485ff-444">Laadige alla ZIP-fail ja seejärel ekstraktige sellest järgmised failid.</span><span class="sxs-lookup"><span data-stu-id="485ff-444">Download the zip file, and then extract the following files from it:</span></span>

    - <span data-ttu-id="485ff-445">Kontrollaruanne Exceli vormingus</span><span class="sxs-lookup"><span data-stu-id="485ff-445">The control report in Excel format</span></span>
    - <span data-ttu-id="485ff-446">Maksesoovituse aruanne Exceli vormingus</span><span class="sxs-lookup"><span data-stu-id="485ff-446">The payment advice report in Excel format</span></span>

        ![Maksesoovituse aruanne Exceli vormingus](./media/er-quick-start2-payment-advice-report.png)

    - <span data-ttu-id="485ff-448">Maksefail TXT-vormingus</span><span class="sxs-lookup"><span data-stu-id="485ff-448">The payment file in TXT format</span></span>

        <span data-ttu-id="485ff-449">Pange tähele, et loodud faili makserida algab SWIFT-koodiga, mis sisestati selle hankija pangakontole, kelle makse on töödeldud.</span><span class="sxs-lookup"><span data-stu-id="485ff-449">Notice that the payment line in the generated file starts  with the SWIFT code that was entered for the bank account of a vendor whose payment has been processed.</span></span>

        ![Maksefail TXT-vormingus](./media/er-quick-start2-payment-file3.png)

## <a name="additional-resources"></a><a id="References"></a><span data-ttu-id="485ff-451">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="485ff-451">Additional resources</span></span>

- [<span data-ttu-id="485ff-452">Elektroonilise aruandluse ülevaade</span><span class="sxs-lookup"><span data-stu-id="485ff-452">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="485ff-453">ER-konfiguratsioonide allalaadimine teenusest Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="485ff-453">Download ER configurations from Lifecycle Services</span></span>](download-electronic-reporting-configuration-lcs.md)
- [<span data-ttu-id="485ff-454">ER-konfiguratsioonide allalaadimine konfiguratsiooniteenuse globaalsest hoidlast</span><span class="sxs-lookup"><span data-stu-id="485ff-454">Download ER configurations from Global repository of Configuration service</span></span>](er-download-configurations-global-repo.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]