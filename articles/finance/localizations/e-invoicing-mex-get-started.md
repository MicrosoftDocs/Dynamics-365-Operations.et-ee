---
title: Mehhiko elektroonilise arvelduse lisandmooduli kasutamise alustamine
description: Sellest teemast leiate teabe, mis aitab teil rakendustes Microsoft Dynamics 365 Finance ja Dynamics 365 Supply Chain Management Mehhiko elektroonilise arvelduse lisandmoodulit kasutama hakata.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: a30f5a9b585c826222108563ea10ac4194ee441c
ms.sourcegitcommit: d6250ee5ced43be39e789324a895fd1c07178935
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/19/2020
ms.locfileid: "4039818"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-mexico"></a><span data-ttu-id="c277e-103">Mehhiko elektroonilise arvelduse lisandmooduli kasutamise alustamine</span><span class="sxs-lookup"><span data-stu-id="c277e-103">Get started with the Electronic invoicing add-on for Mexico</span></span>

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="c277e-104">Elektroonilise arvelduse lisandmoodul Mehhiko jaoks ei pruugi praegu toetada kõiki funktsioone, mis on saadaval dokumendis Comprobante Fiscal Digital por Internet (CFDI) ja seotud integratsioonis, mis on sisse ehitatud rakendusse Microsoft Dynamics 365 Finance või Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="c277e-104">The Electronic invoicing add-on for Mexico might not currently support all the functions that are available in the Comprobante Fiscal Digital por Internet (CFDI) document, and in the related integration that is built into Microsoft Dynamics 365 Finance or Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="c277e-105">Sellest teemast leiate teabe, mis aitab teil Mehhiko elektroonilise arvelduse lisandmoodulit kasutama hakata.</span><span class="sxs-lookup"><span data-stu-id="c277e-105">This topic provides information that will help you get started with the Electronic invoicing add-on for Mexico.</span></span> <span data-ttu-id="c277e-106">Selles antakse juhiseid konfiguratsioonisammude kohta, mis on teenustes Regulatory Configuration Services (RCS) ja rakenduses Finance riigipõhised.</span><span class="sxs-lookup"><span data-stu-id="c277e-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and Finance.</span></span> <span data-ttu-id="c277e-107">Samuti antakse teile juhised, mida peate rakenduses Finance järgima, et edastada teenuse kaudu CFDI arveid, ning selgitatakse, kuidas vaadata üle töötlemise tulemusi ja CFDI arvete olekut.</span><span class="sxs-lookup"><span data-stu-id="c277e-107">It also guides you through the steps that you must follow in Finance to submit CFDI invoices through the service, and it explains how to review the processing results and the status of CFDI invoices.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c277e-108">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="c277e-108">Prerequisites</span></span>

<span data-ttu-id="c277e-109">Enne selle teema juhiste täitmist peate järgima teemas [Elektroonilise arvelduse lisandmooduli kasutamise alustamine](e-invoicing-get-started.md) olevaid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="c277e-109">Before you complete the steps in this topic, you must complete the steps in [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="c277e-110">RCS-i seadistus</span><span class="sxs-lookup"><span data-stu-id="c277e-110">RCS setup</span></span>

<span data-ttu-id="c277e-111">RCS-i seadistuse käigus teete järgmist.</span><span class="sxs-lookup"><span data-stu-id="c277e-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="c277e-112">E-arvelduse funktsiooni importimine CFDI arvete töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="c277e-112">Import the e-Invoicing feature for processing CFDI invoices.</span></span>
2. <span data-ttu-id="c277e-113">Vormingu konfiguratsioonide ülevaatamine, mis on vajalikud CFDI arvete loomiseks, edastamiseks ja nende vastuste vastu võtmiseks ning tühistamisega seotud vastuste edastamiseks ja vastu võtmiseks.</span><span class="sxs-lookup"><span data-stu-id="c277e-113">Review the format configurations that are required to generate, submit, and receive responses about CFDI invoices, and to submit and receive responses about cancellation.</span></span>
3. <span data-ttu-id="c277e-114">CFDI arve edastamise stsenaariume toetavate sündmuste konfigureerimine.</span><span class="sxs-lookup"><span data-stu-id="c277e-114">Configure the events that support the CFDI invoice submission scenarios.</span></span>
4. <span data-ttu-id="c277e-115">E-arvelduse funktsiooni avaldamine CFDI arvete jaoks.</span><span class="sxs-lookup"><span data-stu-id="c277e-115">Publish the e-Invoicing feature for CFDI invoices.</span></span>

> [!NOTE]
> <span data-ttu-id="c277e-116">„E-arvelduse funktsioon” on kindla ressursi üldnimi, mis on konfigureeritud ja avaldatud kasutama elektroonilise arvelduse lisandmooduli serverit.</span><span class="sxs-lookup"><span data-stu-id="c277e-116">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing add-on server.</span></span> <span data-ttu-id="c277e-117">Praegusel juhul on seadistatavaks e-arvelduse funktsiooniks CFDI arved (MX).</span><span class="sxs-lookup"><span data-stu-id="c277e-117">In this case, CFDI invoices (MX) are the e-Invoicing feature that you will set up.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="c277e-118">E-arvelduse funktsiooni importimine</span><span class="sxs-lookup"><span data-stu-id="c277e-118">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="c277e-119">Logige oma RCS-i kontole sisse.</span><span class="sxs-lookup"><span data-stu-id="c277e-119">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="c277e-120">Valige tööruumis **Globaliseerimisfunktsioonid** jaotises **Funktsioonid** paan **E-arveldus**.</span><span class="sxs-lookup"><span data-stu-id="c277e-120">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="c277e-121">Valige lehel **E-arvelduse funktsioonid** suvand **Impordi** , et importida globaalsest hoidlast funktsioon **CFDI arved (MX)**.</span><span class="sxs-lookup"><span data-stu-id="c277e-121">On the **e-Invoicing Features** page, select **Import** to import the **CFDI invoices (MX)** feature from the Global repository.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c277e-122">Kui te funktsiooni loendis ei näe, valige **Sünkrooni** ja seejärel korrake kolmandat sammu.</span><span class="sxs-lookup"><span data-stu-id="c277e-122">If you don't see the feature in the list, select **Synchronize** , and then repeat step 3.</span></span>

![CFDI arvete (MX) funktsiooni importimine](media/e-Invoicing-services-get-started-MEX-Select-Import-CFDI-feature.png)

<span data-ttu-id="c277e-124">Funktsiooni **CFDI arved (MX)** importimisel globaalsest hoidlast imporditakse ka kõik funktsiooni sätted, sealhulgas konfiguratsioonid ja tegevused.</span><span class="sxs-lookup"><span data-stu-id="c277e-124">When you import the **CFDI invoices (MX)** feature from the Global repository, all the feature settings, including configurations and actions, are also imported.</span></span>

### <a name="create-a-new-version-of-the-cfdi-invoices-mx-feature"></a><span data-ttu-id="c277e-125">CFDI arvete (MX) funktsiooni uue versiooni loomine</span><span class="sxs-lookup"><span data-stu-id="c277e-125">Create a new version of the CFDI invoices (MX) feature</span></span>

<span data-ttu-id="c277e-126">Saate luua uue versiooni, kui URL-i on näiteks vaja värskendada.</span><span class="sxs-lookup"><span data-stu-id="c277e-126">You can create a new version if, for example, URLs must be updated.</span></span> <span data-ttu-id="c277e-127">Lisateavet leiate teemast [E-arvelduse CFDI](tasks/mx-00010-e-invoicing-cfdi.md).</span><span class="sxs-lookup"><span data-stu-id="c277e-127">For more information, see [E-invoicing CFDI](tasks/mx-00010-e-invoicing-cfdi.md).</span></span>

- <span data-ttu-id="c277e-128">Valige lehel **E-arvelduse funktsioonid** vahekaardil **Versioonid** suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="c277e-128">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span>

![E-arvelduse funktsiooni uue versiooni lisamine](media/e-Invoicing-services-get-started-MEX-Select-New-e-Invoicing-feature.png)

### <a name="update-the-configuration-version"></a><span data-ttu-id="c277e-130">Konfiguratsiooni versiooni uuendamine</span><span class="sxs-lookup"><span data-stu-id="c277e-130">Update the configuration version</span></span>

1. <span data-ttu-id="c277e-131">Valige lehel **E-arvelduse funktsioonid** vahekaardil **Konfiguratsioonid** suvand **Lisa** või **Kustuta** , et hallata konfiguratsiooni versioone (ER-i failivormingu konfiguratsioone).</span><span class="sxs-lookup"><span data-stu-id="c277e-131">On the **e-Invoicing Features** page, on the **Configurations** tab, select **Add** or **Delete** to manage the configuration versions (ER file format configurations).</span></span>

    ![E-arvelduse funktsiooni konfiguratsioonide haldamine](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Configurations.png)

    <span data-ttu-id="c277e-133">Uue versiooni loomisel päritakse kõik konfiguratsioonid viimasest avaldatud versioonist.</span><span class="sxs-lookup"><span data-stu-id="c277e-133">When you create a new version, all configurations are inherited from the last published version.</span></span> <span data-ttu-id="c277e-134">CFDI arvete töötlemiseks on vajalikud järgmised konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="c277e-134">To process CFDI invoices, the following configurations are required:</span></span>

    - <span data-ttu-id="c277e-135">CFDI arve (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="c277e-135">CFDI invoice (BusinessDocumentService)</span></span>
    - <span data-ttu-id="c277e-136">CFDI vastuseteate importimine</span><span class="sxs-lookup"><span data-stu-id="c277e-136">CFDI response message import</span></span>
    - <span data-ttu-id="c277e-137">CFDI tõrkelogi importimine</span><span class="sxs-lookup"><span data-stu-id="c277e-137">CFDI error log import</span></span>
    - <span data-ttu-id="c277e-138">CFDI tühistamistaotlus (MX) (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="c277e-138">CFDI cancelation request (MX) (BusinessDocumentService)</span></span>
    - <span data-ttu-id="c277e-139">CFDI arve (BusinessDocumentService)</span><span class="sxs-lookup"><span data-stu-id="c277e-139">CFDI invoice (BusinessDocumentService)</span></span>

2. <span data-ttu-id="c277e-140">Valige loendist konfiguratsiooni versioon ja seejärel suvand **Redigeeri** või **Kuva** , et avada leht **Vormingukujundaja** , kus saate konfiguratsiooni redigeerida või vaadata.</span><span class="sxs-lookup"><span data-stu-id="c277e-140">In the list, select a configuration version, and then select **Edit** or **View** to open the **Format designer** page, where you can edit or view the configuration.</span></span>

    ![Vormingukujundaja lehe avamine](media/e-Invoicing-services-get-started-MEX-Configuration-ER-format-designer.png)

3. <span data-ttu-id="c277e-142">Kasutage ER-i vormingu failikonfiguratsioonide redigeerimiseks ja kuvamiseks lehte **Vormingukujundaja**.</span><span class="sxs-lookup"><span data-stu-id="c277e-142">Use the **Format designer** page to edit and view the ER format file configurations.</span></span> <span data-ttu-id="c277e-143">Lisateavet leiate jaotisest [Elektrooniliste dokumentide konfiguratsioonide loomine](../../dev-itpro/analytics/electronic-reporting-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="c277e-143">For more information, see [Create electronic document configurations](../../dev-itpro/analytics/electronic-reporting-configuration.md).</span></span>

    ![Vormingukujundaja leht](media/e-Invoicing-services-get-started-MEX-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="c277e-145">E-arvelduse funktsiooni seadistuste haldamine</span><span class="sxs-lookup"><span data-stu-id="c277e-145">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="c277e-146">Valige lehel **E-arvelduse funktsioonid** vahekaardil **Seadistused** suvand **Lisa** , **Kustuta** või **Redigeeri** , et hallata e-arvelduse funktsiooni seadistusi.</span><span class="sxs-lookup"><span data-stu-id="c277e-146">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add** , **Delete** , or **Edit** to manage the e-Invoicing feature setups.</span></span>

![E-arvelduse funktsiooni seadistuste haldamine](media/e-Invoicing-services-get-started-MEX-Manage-e-Invoicing-feature-Setup.png)

<span data-ttu-id="c277e-148">CFDI arvete edastamiseks autoriseerimise eesmärgil (XML-faili loomiseks, XML-faili edastamiseks ja vastuse töötlemiseks) on vajalik funktsiooniseadistus **Müügiarve**.</span><span class="sxs-lookup"><span data-stu-id="c277e-148">To submit CFDI invoices for authorization (generate the XML file, submit the XML file, and process the response), the **Sales invoice** feature setup is required.</span></span>

<span data-ttu-id="c277e-149">CFDI arve tühistamise edastamiseks on vajalikud funktsiooniseadistused **Tühistamine** ja **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="c277e-149">To submit CFDI invoice cancellation, the **Cancellation** and **Cancel** feature setups are required.</span></span>

### <a name="configure-the-sales-invoice-feature-setup"></a><span data-ttu-id="c277e-150">Müügiarve funktsiooni seadistuse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="c277e-150">Configure the Sales invoice feature setup</span></span>

1. <span data-ttu-id="c277e-151">Valige lehe **E-arvelduse funktsioonid** vahekaardi **Seadistused** veerus **Funktsiooni seadistus** suvand **Müügiarve**.</span><span class="sxs-lookup"><span data-stu-id="c277e-151">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Sales invoice**.</span></span>
2. <span data-ttu-id="c277e-152">Valige **Redigeeri** , et konfigureerida tegevused, rakendatavuse reeglid ja muutujad.</span><span class="sxs-lookup"><span data-stu-id="c277e-152">Select **Edit** to configure the actions, applicability rules, and variables.</span></span>

    ![E-arvelduse funktsiooni seadistuse redigeerimine](media/e-Invoicing-services-get-started-MEX-Edit-e-Invoicing-feature-setup.png)

3. <span data-ttu-id="c277e-154">Valige lehel **Funktsiooni versiooni seadistus** vahekaart **Tegevused** , et hallata tegevuste loendit.</span><span class="sxs-lookup"><span data-stu-id="c277e-154">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span> <span data-ttu-id="c277e-155">Tegevused määratlevad selliste toimingute loendi, mis tuleb käitada sündmuse täielikuks lõpetamiseks järjestikku.</span><span class="sxs-lookup"><span data-stu-id="c277e-155">Actions define a list of operations that must be run in sequential order to accomplish full execution of the event.</span></span>

    ![Tegevuste vahekaart](media/e-Invoicing-services-get-started-MEX-Select-Actions.png)

    | <span data-ttu-id="c277e-157">Tegevuse ID</span><span class="sxs-lookup"><span data-stu-id="c277e-157">Action ID</span></span> | <span data-ttu-id="c277e-158">Tegevus</span><span class="sxs-lookup"><span data-stu-id="c277e-158">Action</span></span>                   | <span data-ttu-id="c277e-159">Tegevuse nimi</span><span class="sxs-lookup"><span data-stu-id="c277e-159">Action name</span></span>                                  | <span data-ttu-id="c277e-160">Tegevuse kirjeldus</span><span class="sxs-lookup"><span data-stu-id="c277e-160">Action description</span></span>                                          |
    |-----------|--------------------------|----------------------------------------------|-------------------------------------------------------------|
    | <span data-ttu-id="c277e-161">1</span><span class="sxs-lookup"><span data-stu-id="c277e-161">1</span></span>         | <span data-ttu-id="c277e-162">Teisenda dokument</span><span class="sxs-lookup"><span data-stu-id="c277e-162">Transform document</span></span>       | <span data-ttu-id="c277e-163">Loo CFDI e-arve digitaalallkirjata</span><span class="sxs-lookup"><span data-stu-id="c277e-163">Generate CFDI E-Invoice without digital sign</span></span> | <span data-ttu-id="c277e-164">CFDI e-arve loomine.</span><span class="sxs-lookup"><span data-stu-id="c277e-164">Generate the CFDI e-invoice.</span></span>                                |
    | <span data-ttu-id="c277e-165">2</span><span class="sxs-lookup"><span data-stu-id="c277e-165">2</span></span>         | <span data-ttu-id="c277e-166">Allkirjasta dokument</span><span class="sxs-lookup"><span data-stu-id="c277e-166">Sign document</span></span>            | <span data-ttu-id="c277e-167">Digitaalallkiri</span><span class="sxs-lookup"><span data-stu-id="c277e-167">Digital sign</span></span>                                 | <span data-ttu-id="c277e-168">E-arve digitaalne allkirjastamine edastamiseks.</span><span class="sxs-lookup"><span data-stu-id="c277e-168">Digitally sign the e-invoice for submission.</span></span>                |
    | <span data-ttu-id="c277e-169">3</span><span class="sxs-lookup"><span data-stu-id="c277e-169">3</span></span>         | <span data-ttu-id="c277e-170">Kutsu Mehhiko PAC teenust</span><span class="sxs-lookup"><span data-stu-id="c277e-170">Call Mexican PAC service</span></span> | <span data-ttu-id="c277e-171">Edasta CFDI e-arve</span><span class="sxs-lookup"><span data-stu-id="c277e-171">Submit CFDI E-Invoice</span></span>                        | <span data-ttu-id="c277e-172">Windows Communication Foundationi (WCF) klient edastab CFDI e-arve.</span><span class="sxs-lookup"><span data-stu-id="c277e-172">The Windows Communication Foundation (WCF) client submits the CFDI e-invoice.</span></span> |
    | <span data-ttu-id="c277e-173">4</span><span class="sxs-lookup"><span data-stu-id="c277e-173">4</span></span>         | <span data-ttu-id="c277e-174">Töötle vastust</span><span class="sxs-lookup"><span data-stu-id="c277e-174">Process response</span></span>         | <span data-ttu-id="c277e-175">Analüüsi veebiteenuse vastust</span><span class="sxs-lookup"><span data-stu-id="c277e-175">Analyze web service response</span></span>                 | <span data-ttu-id="c277e-176">Veebiteenuse vastuse analüüsimine ja tõrkelogi tagastamine.</span><span class="sxs-lookup"><span data-stu-id="c277e-176">Analyze the web service response, and return the error log.</span></span> |

### <a name="set-up-the-url-for-mexican-pac-web-services"></a><span data-ttu-id="c277e-177">Mehhiko PAC veebiteenuste URL-i seadistamine</span><span class="sxs-lookup"><span data-stu-id="c277e-177">Set up the URL for Mexican PAC web services</span></span> 

1. <span data-ttu-id="c277e-178">Valige lehel **Funktsiooni versiooni seadistus** vahekaardi **Tegevused** kiirkaardilt **Tegevused** suvand **Kutsu Mehhiko PAC teenust**.</span><span class="sxs-lookup"><span data-stu-id="c277e-178">On the **Feature version setup** page, on the **Actions** tab, on the **Actions** FastTab, select **Call Mexican PAC service**.</span></span>
2. <span data-ttu-id="c277e-179">Sisestage kiirkaardil **Parameetrid** väljale **URL-aadress** CFDI arve edastamiseks veebiteenuse URL.</span><span class="sxs-lookup"><span data-stu-id="c277e-179">On the **Parameters** FastTab, in the **URL address** field, enter the URL of the web service for CFDI invoice submission.</span></span>

> [!NOTE]
> <span data-ttu-id="c277e-180">Kasutage samu samme, et värskendada tegevuse **Kutsu Mehhiko PAC teenust** URL-i funktsiooniseadistuste **Tühista** ja **Tühistamistaotlus** jaoks.</span><span class="sxs-lookup"><span data-stu-id="c277e-180">Use the same steps to update the URL for **Call Mexican PAC service** action for the **Cancel** and **Cancelation request** feature setups.</span></span>

## <a name="assign-the-draft-version-to-an-e-invoicing-environment"></a><span data-ttu-id="c277e-181">Mustandversiooni määramine e-arvelduse keskkonnale</span><span class="sxs-lookup"><span data-stu-id="c277e-181">Assign the Draft version to an e-Invoicing environment</span></span>

1. <span data-ttu-id="c277e-182">Valige lehel **E-arvelduse funktsioonid** vahekaardil **Keskkonnad** suvand **Luba**.</span><span class="sxs-lookup"><span data-stu-id="c277e-182">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="c277e-183">Valige keskkond väljal **Keskkond**.</span><span class="sxs-lookup"><span data-stu-id="c277e-183">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="c277e-184">Valige väljal **Kehtiv alates** kuupäev, mil uus keskkond peaks kehtima hakkama.</span><span class="sxs-lookup"><span data-stu-id="c277e-184">In the **Effective from** field, select the date when the environment should become effective.</span></span>
3. <span data-ttu-id="c277e-185">Valige **Luba**.</span><span class="sxs-lookup"><span data-stu-id="c277e-185">Select **Enable**.</span></span>

![E-arvelduse keskkonna lubamine](media/e-Invoicing-services-get-started-MEX-Enable-e-Invoicing-Environment.png)

## <a name="change-the-version-status-to-completed"></a><span data-ttu-id="c277e-187">Versiooni oleku muutmine lõpetatuks</span><span class="sxs-lookup"><span data-stu-id="c277e-187">Change the version status to Completed</span></span>

1. <span data-ttu-id="c277e-188">Valige lehel **E-arvelduse funktsioonid** vahekaardil **Versioonid** e-arvelduse funktsiooni versioon, mille olek on **Mustand**.</span><span class="sxs-lookup"><span data-stu-id="c277e-188">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="c277e-189">Valige **Muuda olekut \> Lõpule viidud**.</span><span class="sxs-lookup"><span data-stu-id="c277e-189">Select **Change status \> Complete**.</span></span>

## <a name="change-the-version-status-to-published"></a><span data-ttu-id="c277e-190">Versiooni oleku muutmine avaldatuks</span><span class="sxs-lookup"><span data-stu-id="c277e-190">Change the version status to Published</span></span>

- <span data-ttu-id="c277e-191">Valige lehel **E-arvelduse funktsioonid** vahekaardil **Versioonid** suvand **Muuda olekut \> Avalda**.</span><span class="sxs-lookup"><span data-stu-id="c277e-191">On the **e-Invoicing Features** page, on the **Versions** tab, select **Change status \> Publish**.</span></span>

## <a name="publish-the-e-invoicing-feature"></a><span data-ttu-id="c277e-192">E-arvelduse funktsiooni avaldamine</span><span class="sxs-lookup"><span data-stu-id="c277e-192">Publish the e-Invoicing feature</span></span>

1. <span data-ttu-id="c277e-193">Valige lehel **E-arvelduse funktsioonid** vahekaart **Versioonid** , et hallata funktsiooni **CFDI arved (MX)** olekut.</span><span class="sxs-lookup"><span data-stu-id="c277e-193">On the **e-Invoicing Features** page, select the **Versions** tab to manage the status of the **CFDI invoices (MX)** feature.</span></span>
2. <span data-ttu-id="c277e-194">Valige **Muuda olekut** , et muuta funktsiooni olekut.</span><span class="sxs-lookup"><span data-stu-id="c277e-194">Select **Change status** to change the status of the feature.</span></span>

![E-arvelduse funktsiooni oleku muutmine](media/e-Invoicing-services-get-started-MEX-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance"></a><span data-ttu-id="c277e-196">Elektroonilise arvelduse lisandmooduli integratsiooni seadistamine rakenduses Finance</span><span class="sxs-lookup"><span data-stu-id="c277e-196">Set up Electronic invoicing add-on integration in Finance</span></span>

<span data-ttu-id="c277e-197">Elektroonilise arvelduse lisandmooduli seadistamise käigus rakenduses Finance teete järgmist.</span><span class="sxs-lookup"><span data-stu-id="c277e-197">To set up the Electronic invoicing add-on in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="c277e-198">ER-i andmemudeli, ER-i andmemudeli vastenduse ja CFDI arvete jaoks vajalike vormingute importimine.</span><span class="sxs-lookup"><span data-stu-id="c277e-198">Import the ER data model, the ER data model mapping, and the formats that are required for CFDI invoices.</span></span>
2. <span data-ttu-id="c277e-199">Vastusetüüpide konfigureerimine CFDI arvete värskendamiseks.</span><span class="sxs-lookup"><span data-stu-id="c277e-199">Configure response types for updating the CFDI invoices.</span></span> <span data-ttu-id="c277e-200">Vastusetüüpe kasutatakse autoriseeritud serdipakkuja (PAC) serveri vastuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="c277e-200">These response types are used for the response from the authorized certification provider (PAC) server.</span></span>

### <a name="import-the-er-data-model-er-data-model-mapping-and-context-configurations-for-cfdi-invoices"></a><span data-ttu-id="c277e-201">ER-i andmemudeli, ER-i andmemudeli vastenduse ja CFDI arvete kontekstikonfiguratsioonide importimine</span><span class="sxs-lookup"><span data-stu-id="c277e-201">Import the ER data model, ER data model mapping, and context configurations for CFDI invoices</span></span>

1. <span data-ttu-id="c277e-202">Logige sisse rakendusse Finance.</span><span class="sxs-lookup"><span data-stu-id="c277e-202">Sign in to Finance.</span></span>
2. <span data-ttu-id="c277e-203">Valige tööruumi **Elektrooniline aruandlus** jaotisest **Konfiguratsioonipakkujad** pealkiri **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="c277e-203">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** title.</span></span> <span data-ttu-id="c277e-204">Veenduge, et konfiguratsioonipakkuja olekuks oleks seatud **Aktiivne**.</span><span class="sxs-lookup"><span data-stu-id="c277e-204">Make sure that this configuration provider is set to **Active**.</span></span> <span data-ttu-id="c277e-205">Lisateavet pakkuja **aktiivseks** märkimise kohta leiate teemast [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span><span class="sxs-lookup"><span data-stu-id="c277e-205">For information about how to set a provider to **Active** , see [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span></span>
3. <span data-ttu-id="c277e-206">Valige **Osad**.</span><span class="sxs-lookup"><span data-stu-id="c277e-206">Select **Repositories**.</span></span>
4. <span data-ttu-id="c277e-207">Valige **Globaalne ressurss \> Ava**.</span><span class="sxs-lookup"><span data-stu-id="c277e-207">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="c277e-208">Importige **Arvemudel** , **Arvemudeli vastendus** , **CFDI arve vorming (MX)** , **CFDI arve tühistamistaotluse vorming (MX)** ja **CFDI arve tühistamisvorming (MX)**.</span><span class="sxs-lookup"><span data-stu-id="c277e-208">Import **Invoice model** , **Invoice model mapping** , **CFDI invoice format (MX)** , **CFDI invoice cancelation request format (MX)** , and **CFDI invoice cancel format (MX)**.</span></span>

### <a name="turn-on-the-feature-for-processing-cfdi-invoices"></a><span data-ttu-id="c277e-209">Funktsiooni sisselülitamine CFDI arvete töötlemiseks</span><span class="sxs-lookup"><span data-stu-id="c277e-209">Turn on the feature for processing CFDI invoices</span></span>

1. <span data-ttu-id="c277e-210">Avage **Organisatsiooni haldus \> Seadistus \> Elektroonilise dokumendi parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="c277e-210">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="c277e-211">Märkige vahekaardil **Funktsioonid** märkeruut **Luba** funktsiooniviidete **MX-00010** ja **MX-00016** ridade puhul.</span><span class="sxs-lookup"><span data-stu-id="c277e-211">On the **Features** tab, select the **Enable** check box in the rows for feature references **MX-00010** and **MX-00016**.</span></span>

![Funktsioonide sisselülitamine CFDI arvete töötlemiseks](media/e-Invoicing-services-get-started-MEX-Enable-CFDI-feature.png)

### <a name="import-er-configurations-and-set-up-the-response-types-for-updating-cfdi-invoices"></a><span data-ttu-id="c277e-213">ER-i konfiguratsioonide importimine ja vastusetüüpide seadistamine CFDI arvete värskendamiseks</span><span class="sxs-lookup"><span data-stu-id="c277e-213">Import ER configurations and set up the response types for updating CFDI invoices</span></span>

#### <a name="import-er-configurations"></a><span data-ttu-id="c277e-214">Elektroonilise aruandluse konfiguratsioonide importimine</span><span class="sxs-lookup"><span data-stu-id="c277e-214">Import ER configurations</span></span>

1. <span data-ttu-id="c277e-215">Valige tööruumi **Elektrooniline aruandlus** jaotisest **Konfiguratsioonipakkujad** pealkiri **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="c277e-215">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** title.</span></span>
3. <span data-ttu-id="c277e-216">Valige **Osad**.</span><span class="sxs-lookup"><span data-stu-id="c277e-216">Select **Repositories**.</span></span>
4. <span data-ttu-id="c277e-217">Valige **Globaalne ressurss \> Ava**.</span><span class="sxs-lookup"><span data-stu-id="c277e-217">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="c277e-218">Importige **Vastuseteate mudel** , **CFDI tõrkelogi importimine (MX)** , **CFDI tõrkelogi importimine (MX)** ja **CFDI vastuseteate importimine (MX)**.</span><span class="sxs-lookup"><span data-stu-id="c277e-218">Import **Response message model** , **CFDI error log import (MX)** , **CFDI error log import (MX)** , and **CFDI response message import (MX)**.</span></span>

#### <a name="set-up-the-response-types"></a><span data-ttu-id="c277e-219">Vastusetüüpide seadistamine</span><span class="sxs-lookup"><span data-stu-id="c277e-219">Set up the response types</span></span>

1. <span data-ttu-id="c277e-220">Avage **Organisatsiooni haldus \> Seadistus \> Elektroonilise dokumendi parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="c277e-220">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="c277e-221">Valige lehel **Elektrooniline dokument** suvand **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="c277e-221">On the **Electronic document** tab, select **Add**.</span></span>
3. <span data-ttu-id="c277e-222">Sisestage kliendiarve tööleht ja seejärel valige väljal **Tabeli nimi** projektiarve.</span><span class="sxs-lookup"><span data-stu-id="c277e-222">Enter the customer invoice journal, and then, in the **Table name** field, select the project invoice.</span></span>
4. <span data-ttu-id="c277e-223">Määratlege iga tabeli puhul seotud dokumendi kontekst.</span><span class="sxs-lookup"><span data-stu-id="c277e-223">For each table, define a related document context:</span></span>

    - <span data-ttu-id="c277e-224">Sisestage suvandi **Kliendiarve tööleht** puhul **Kliendiarve kontekst**.</span><span class="sxs-lookup"><span data-stu-id="c277e-224">For **Customer invoice journal** , enter **Customer invoice context**.</span></span>
    - <span data-ttu-id="c277e-225">Sisestage suvandi **Projektiarve** puhul **Projektiarve kontekst**.</span><span class="sxs-lookup"><span data-stu-id="c277e-225">For **Project invoice** , enter **Project invoice context**.</span></span>

4. <span data-ttu-id="c277e-226">Valige **Vastusetüübid** , et konfigureerida vastusetüübid, mida saab elektroonilise arvelduse lisandmoodulist tagastada ja lisada kliendiarve töölehele või projektiarvele.</span><span class="sxs-lookup"><span data-stu-id="c277e-226">Select **Response types** to configure the response types that can be returned from the Electronic invoicing add-on and included in a customer invoice journal or project invoice.</span></span>
5. <span data-ttu-id="c277e-227">Valige **Uus** ja valige siis väljal **Vastusetüüp** suvand **Vastus**.</span><span class="sxs-lookup"><span data-stu-id="c277e-227">Select **New** , and then, in the **Response type** field, select **Response**.</span></span>
6. <span data-ttu-id="c277e-228">Valige väljal **Edastuse olek** suvand **Ootel**.</span><span class="sxs-lookup"><span data-stu-id="c277e-228">In the **Submission status** field, select **Pending**.</span></span>
7. <span data-ttu-id="c277e-229">Valige väljal **Mudelivastendus** suvand **Vastuseteate impordivorming – mudelivastendus vastuseteatest**.</span><span class="sxs-lookup"><span data-stu-id="c277e-229">In the **Model mapping** field, select **Response message import format – Model mapping from response message**.</span></span>
8. <span data-ttu-id="c277e-230">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="c277e-230">Select **Save**.</span></span>
9. <span data-ttu-id="c277e-231">Valige **Uus** ja valige siis väljal **Vastusetüüp** suvand **ResponseData**.</span><span class="sxs-lookup"><span data-stu-id="c277e-231">Select **New** , and then, in the **Response type** field, select **ResponseData**.</span></span>
10. <span data-ttu-id="c277e-232">Valige väljal **Edastuse olek** suvand **Ootel**.</span><span class="sxs-lookup"><span data-stu-id="c277e-232">In the **Submission status** field, select **Pending**.</span></span>
11. <span data-ttu-id="c277e-233">Valige väljal **Mudelivastendus** suvand **CFDI vastuseandmete impordivorming (üksikasjad) – vastuseandmete importimine**.</span><span class="sxs-lookup"><span data-stu-id="c277e-233">In the **Model mapping** field, select **CFDI response data import format (details) – Response data import**.</span></span>
12. <span data-ttu-id="c277e-234">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="c277e-234">Select **Save**.</span></span>

## <a name="process-electronic-invoices-in-finance"></a><span data-ttu-id="c277e-235">Elektrooniliste arvete töötlemine rakenduses Finance</span><span class="sxs-lookup"><span data-stu-id="c277e-235">Process electronic invoices in Finance</span></span> 

<span data-ttu-id="c277e-236">CFDI arvete töötlemisel rakenduses Finance elektroonilise arvelduse lisandmooduli kaudu saate teha järgmisi toiminguid.</span><span class="sxs-lookup"><span data-stu-id="c277e-236">During the processing of CFDI invoices in Finance through the Electronic invoicing add-on, you can perform the following tasks:</span></span>

- <span data-ttu-id="c277e-237">CFDI arvete edastamine.</span><span class="sxs-lookup"><span data-stu-id="c277e-237">Submit CFDI invoices.</span></span>
- <span data-ttu-id="c277e-238">Edastuse käivituslogide kuvamine.</span><span class="sxs-lookup"><span data-stu-id="c277e-238">View the submission execution logs.</span></span>
- <span data-ttu-id="c277e-239">CFDI arve tühistamise edastamine.</span><span class="sxs-lookup"><span data-stu-id="c277e-239">Submit the cancellation of a CFDI invoice.</span></span>

### <a name="submit-cfdi-invoices"></a><span data-ttu-id="c277e-240">CFDI arvete edastamine</span><span class="sxs-lookup"><span data-stu-id="c277e-240">Submit CFDI invoices</span></span>

<span data-ttu-id="c277e-241">Pärast funktsiooni **Konfigureeritav elektroonilise arvelduse lisandmooduli integratsioon** sisse lülitamist pole CFDI arvete edastamiseks enam võimalik kasutada protsessi **Ekspordi/impordi elektrooniline arve** ( **Müügireskontro \> Arved \> E-arved** ).</span><span class="sxs-lookup"><span data-stu-id="c277e-241">After you turn on the **Configurable Electronic invoicing add-on integration** feature, the **Export/Import electronic invoice** process ( **Accounts receivable \> Invoices \> E-invoices** ) for submitting CFDI invoices can no longer be used.</span></span> <span data-ttu-id="c277e-242">See asendatakse uue protsessiga **Edasta elektroonilised dokumendid**.</span><span class="sxs-lookup"><span data-stu-id="c277e-242">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

> [!NOTE]
> <span data-ttu-id="c277e-243">Enne uue protsessi **Edasta elektroonilised dokumendid** kasutamist veenduge, et Mehhiko e-arvete jaoks vajalik seadistus oleks lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="c277e-243">Before you use the new **Submit electronic documents** process, verify that the setup that is required for Mexican e-invoices was completed.</span></span> <span data-ttu-id="c277e-244">Lisateavet leiate teemast [CFDI paigutuse versioon 3.3](https://docs.microsoft.com/dynamics365/finance/localizations/latam-mex-cfdi-3-3).</span><span class="sxs-lookup"><span data-stu-id="c277e-244">For more information, see [CFDI layout version 3.3](https://docs.microsoft.com/dynamics365/finance/localizations/latam-mex-cfdi-3-3).</span></span>

1. <span data-ttu-id="c277e-245">Avage **Organisatsiooni haldus \> Perioodiline \> Elektroonilised dokumendid \> Edasta elektroonilised dokumendid**.</span><span class="sxs-lookup"><span data-stu-id="c277e-245">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="c277e-246">Mis tahes dokumendi esimese edastamise korral seadke suvandi **Dokumentide taasedastamine** väärtuseks alati **Ei**.</span><span class="sxs-lookup"><span data-stu-id="c277e-246">For the first submission of any document, always set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="c277e-247">Kui peate dokumendi teenuse kaudu uuesti edastama, seadke selle suvandi väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="c277e-247">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="c277e-248">Valige kiirkaardil **Kaasatavad kirjed** suvand **Filter** , et avada dialoogiboks **Päring** , kus saate luua päringu edastatavate dokumentide valimiseks.</span><span class="sxs-lookup"><span data-stu-id="c277e-248">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>

![CFDI dokumendi edastamine](media/e-Invoicing-services-get-started-MEX-Submit-CFDI-document.png)

> [!NOTE]
> <span data-ttu-id="c277e-250">Esimesel dokumendi edastamise katsel teenuse kaudu palutakse teil kinnitada ühendus elektroonilise arvelduse lisandmooduliga.</span><span class="sxs-lookup"><span data-stu-id="c277e-250">During your first attempt to submit a document through the service, you will be prompted to confirm the connection with the Electronic invoicing add-on.</span></span> <span data-ttu-id="c277e-251">Valige **Elektroonilise dokumendi edastusteenusega ühendumiseks klõpsake siin**.</span><span class="sxs-lookup"><span data-stu-id="c277e-251">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

### <a name="view-submission-logs"></a><span data-ttu-id="c277e-252">Edastuslogide kuvamine</span><span class="sxs-lookup"><span data-stu-id="c277e-252">View submission logs</span></span>

<span data-ttu-id="c277e-253">Saate vaadata kõigi edastatud dokumentide või ainult ühe edastatud dokumendi edastuslogisid.</span><span class="sxs-lookup"><span data-stu-id="c277e-253">You can view the submission logs for all submitted documents or for just one submitted document.</span></span>

#### <a name="view-all-submission-logs"></a><span data-ttu-id="c277e-254">Kõigi edastuslogide kuvamine</span><span class="sxs-lookup"><span data-stu-id="c277e-254">View all submission logs</span></span>

<span data-ttu-id="c277e-255">Pärast funktsiooni **Konfigureeritav elektroonilise arvelduse lisandmooduli integratsioon** sisse lülitamist on saadaval uus leht, mis võimaldab teil jälgida dokumendi edastamise edenemist.</span><span class="sxs-lookup"><span data-stu-id="c277e-255">After you turn on the **Configurable Electronic invoicing add-on integration** feature, a new page is available that lets you follow up on the document submission process.</span></span> <span data-ttu-id="c277e-256">Selle lehe abil saate vaadata kõigi edastatud dokumentide edastuslogisid.</span><span class="sxs-lookup"><span data-stu-id="c277e-256">You can use this page to view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="c277e-257">Avage **Organisatsiooni haldus \> Perioodiline \> Elektroonilised dokumendid \> Elektroonilise dokumendi edastuslogi**.</span><span class="sxs-lookup"><span data-stu-id="c277e-257">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="c277e-258">Valige väljal **Dokumenditüüp** suvand **Kliendiarve tööleht** , et kuvada vajalikud elektroonilised dokumendid.</span><span class="sxs-lookup"><span data-stu-id="c277e-258">In the **Document type** field, select **Customer invoice journal** to filter for the required electronic documents.</span></span>

    ![Dokumendi tüübi valimine edastuslogide kuvamiseks](media/e-Invoicing-services-get-started-MEX-Select-document-type-for-viewing-submission-log.png)

3. <span data-ttu-id="c277e-260">Valige toimingupaanil **Päringud \> Edastuse üksikasjad** , et vaadata edastuse käivituslogide üksikasju.</span><span class="sxs-lookup"><span data-stu-id="c277e-260">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Edastuslogi üksikasjade vaatamine](media/e-Invoicing-services-get-started-MEX-View-submission-log-details.png)

<span data-ttu-id="c277e-262">Edastuslogide teave on jagatud kolme kiirkaardi vahel.</span><span class="sxs-lookup"><span data-stu-id="c277e-262">The information in the submission logs is divided among three FastTabs:</span></span>

- <span data-ttu-id="c277e-263">**Töötlemistegevused** – sellel kiirkaardil näidatakse RCS-is seadistatud funktsiooni versioonis konfigureeritud tegevuste käivituslogi.</span><span class="sxs-lookup"><span data-stu-id="c277e-263">**Processing actions** – This FastTab shows the execution log for the actions that are configured in the feature version that was set up in RCS.</span></span> <span data-ttu-id="c277e-264">Veerus **Olek** on näha, kas tegevuse käivitamine õnnestus.</span><span class="sxs-lookup"><span data-stu-id="c277e-264">The **Status** column shows whether the action was successfully run.</span></span>
- <span data-ttu-id="c277e-265">**Tegevusfailid** – sellel kiirkaadil on vahefailid, mis loodi tegevuste käivitamise ajal.</span><span class="sxs-lookup"><span data-stu-id="c277e-265">**Action files** – This FastTab shows the intermediate files that were generated during execution of the actions.</span></span> <span data-ttu-id="c277e-266">Saate valida **Kuva** , et fail alla laadida ja seda vaadata.</span><span class="sxs-lookup"><span data-stu-id="c277e-266">You can select **View** to download and view the file.</span></span>
- <span data-ttu-id="c277e-267">**Töötlemise tegevuslogi** – sellel kiirkaardil on kuvatud elektroonilise arvelduse lisandmooduli ja sihtveebiteenuse vahelise suhtluse tulemused.</span><span class="sxs-lookup"><span data-stu-id="c277e-267">**Processing action log** – This FastTab shows the results of the communication between the Electronic invoicing add-on and the target web service.</span></span> <span data-ttu-id="c277e-268">See näitab ka, mis tagastati veebiteenuse töötlemise käigus.</span><span class="sxs-lookup"><span data-stu-id="c277e-268">It also shows what was returned by the processing from the web service.</span></span> <span data-ttu-id="c277e-269">Veerus **Tõrkekood** on toodud tagastuskood, mis tagastati autoriseerivast veebiteenusest.</span><span class="sxs-lookup"><span data-stu-id="c277e-269">The **Error code** column shows the return code that was returned by the authorization web service.</span></span>

<span data-ttu-id="c277e-270">Kui edastatud CFDI arve on autoriseeritud, määratakse selle olekuks väärtus **Kinnitatud**.</span><span class="sxs-lookup"><span data-stu-id="c277e-270">When the submitted CFDI invoice is authorized, its status is updated to **Approved**.</span></span>

#### <a name="view-submission-logs-from-cfdi-invoices"></a><span data-ttu-id="c277e-271">Edastuslogide kuvamine CFDI arvetes</span><span class="sxs-lookup"><span data-stu-id="c277e-271">View submission logs from CFDI invoices</span></span>

<span data-ttu-id="c277e-272">Pärast funktsiooni **Konfigureeritav elektroonilise arvelduse lisandmooduli integratsioon** sisse lülitamist saate vaadata edastuslogisid ka CFDI arvetes.</span><span class="sxs-lookup"><span data-stu-id="c277e-272">After you turn on the **ConfigurableElectronic invoicing add-on integration** feature, you can also view the submission logs from CFDI invoices.</span></span>

1. <span data-ttu-id="c277e-273">Avage **Müügireskontro \> Päringud ja aruanded \> CFDI (elektroonilised arved)**.</span><span class="sxs-lookup"><span data-stu-id="c277e-273">Go to **Accounts receivable \> Inquiries and reports \> CFDI (electronic invoices)**.</span></span>
2. <span data-ttu-id="c277e-274">Valige CFDI arve, mis edastati pärast funktsiooni **Konfigureeritav elektroonilise arvelduse lisandmooduli integratsioon** sisse lülitamist.</span><span class="sxs-lookup"><span data-stu-id="c277e-274">Select a CFDI invoice that was submitted after the **Configurable Electronic invoicing add-on integration** feature was turned on.</span></span>
3. <span data-ttu-id="c277e-275">Valige toimingupaanil vahekaardil **Ajalugu** suvand **Elektroonilise dokumendi logi**.</span><span class="sxs-lookup"><span data-stu-id="c277e-275">On the Action Pane, on the **History** tab, select **Electronic document log**.</span></span>

![Edastuslogide vaatamine CFDI arvetes](media/e-Invoicing-services-get-started-MEX-View-submission-log-from-CFDI-invoice.png)

> [!NOTE]
> <span data-ttu-id="c277e-277">CFDI arvete puhul, mis edastati enne funktsiooni **Konfigureeritav elektroonilise arvelduse lisandmooduli integratsioon** sisse lülitamist, on saadaval nupp **Ajalugu**.</span><span class="sxs-lookup"><span data-stu-id="c277e-277">For CFDI invoices that were submitted before the **Configurable Electronic invoicing add-on integration** feature was turned on, the **History** button is available.</span></span> <span data-ttu-id="c277e-278">CFDI arvete puhul, mis edastati pärast funktsiooni **Konfigureeritav elektroonilise arvelduse lisandmooduli integratsioon** sisse lülitamist, pole nupp **Ajalugu** saadaval.</span><span class="sxs-lookup"><span data-stu-id="c277e-278">The **History** button isn't available for CFDI invoices that were submitted after the **Configurable Electronic invoicing add-on integration** feature was turned on.</span></span>

### <a name="submit-cancellation-of-cfdi-invoices"></a><span data-ttu-id="c277e-279">CFDI arvete tühistamise edastamine</span><span class="sxs-lookup"><span data-stu-id="c277e-279">Submit cancellation of CFDI invoices</span></span>

<span data-ttu-id="c277e-280">Pärast funktsiooni **Konfigureeritav elektroonilise arvelduse lisandmooduli integratsioon** sisse lülitamist ei saa enam vana CFDI arvete tühistamise protsessi kasutada.</span><span class="sxs-lookup"><span data-stu-id="c277e-280">After you turn on the **Configurable Electronic invoicing add-on integration** feature, the old process for canceling CFDI invoices can no longer be used.</span></span> <span data-ttu-id="c277e-281">See asendatakse uue tühistamisprotsessiga, mis on manustatud lehel **Elektroonilise dokumendi edastuslogi**.</span><span class="sxs-lookup"><span data-stu-id="c277e-281">It's replaced by a new cancellation process that is embedded on the **Electronic document submission log** page.</span></span>

1. <span data-ttu-id="c277e-282">Avage **Müügireskontro \> Päringud ja aruanded \> CFDI (elektroonilised arved)**.</span><span class="sxs-lookup"><span data-stu-id="c277e-282">Go to **Accounts receivable \> Inquiries and reports \> CFDI (electronic invoices)**.</span></span>
2. <span data-ttu-id="c277e-283">Kui CFDI arve olek on **Kinnitatud** , valige **Funktsioonid \> Tühista CFDI**.</span><span class="sxs-lookup"><span data-stu-id="c277e-283">If the CFDI invoice has a status of **Approved** , select **Functions \> Cancel CFDI**.</span></span>
3. <span data-ttu-id="c277e-284">Avage **Organisatsiooni haldus \> Perioodiline \> Elektroonilised dokumendid \> Elektroonilise dokumendi edastuslogi**.</span><span class="sxs-lookup"><span data-stu-id="c277e-284">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
4. <span data-ttu-id="c277e-285">Valige CFDI arve ja seejärel **Funktsioonid \> Saada seotud edastused**.</span><span class="sxs-lookup"><span data-stu-id="c277e-285">Select the CFDI invoice, and then select **Functions \> Send related submissions**.</span></span>
5. <span data-ttu-id="c277e-286">Sisestage seotud edastuse kirjeldus ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="c277e-286">Enter a description for the related submission, and then select **OK**.</span></span>

#### <a name="view-cancellation-submission-logs"></a><span data-ttu-id="c277e-287">Tühistamise edastuslogide kuvamine</span><span class="sxs-lookup"><span data-stu-id="c277e-287">View cancellation submission logs</span></span>

1. <span data-ttu-id="c277e-288">Avage **Organisatsiooni haldus \> Perioodiline \> Elektroonilised dokumendid \> Elektroonilise dokumendi edastuslogi**.</span><span class="sxs-lookup"><span data-stu-id="c277e-288">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="c277e-289">Valige väljal **Dokumenditüüp** suvand **Kliendiarve tööleht** , et kuvada ainult kliendiarve töölehe dokumendid.</span><span class="sxs-lookup"><span data-stu-id="c277e-289">In the **Document type** field, select **Customer invoice journal** to filter for customer invoice journal documents only.</span></span>
3. <span data-ttu-id="c277e-290">Valige CFDI arve ja seejärel valige toimingupaanil **Päringud \> Seotud edastus**.</span><span class="sxs-lookup"><span data-stu-id="c277e-290">Select the CFDI invoice, and then, on the Action Pane, select **Inquiries \> Related submission**.</span></span>

    <span data-ttu-id="c277e-291">Lehel **Seotud edastused** kuvatakse kõik asjaomase CFDI arvega seotud edastused ja nende edastamise olek.</span><span class="sxs-lookup"><span data-stu-id="c277e-291">The **Related submissions** page shows all related submissions, and their submission status, for a given CFDI invoice.</span></span> <span data-ttu-id="c277e-292">Järgmisel illustratsioonil tähistab esimene rida edastust, mis taotles CFDI arve kinnitust.</span><span class="sxs-lookup"><span data-stu-id="c277e-292">In the following illustration, the first line represents the submission that requested approval of the CFDI invoice.</span></span> <span data-ttu-id="c277e-293">Teine rida tähistab edastust, mis tühistas selle CFDI arve.</span><span class="sxs-lookup"><span data-stu-id="c277e-293">The second line represents the submission that canceled that CFDI invoice.</span></span>

    ![Tühistamise edastuslogide vaatamine](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log.png)

4. <span data-ttu-id="c277e-295">Valige toimingupaanil **Päringud \> Edastuse üksikasjad** , et vaadata edastuse käivituslogide üksikasju.</span><span class="sxs-lookup"><span data-stu-id="c277e-295">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Tühistamise edastuslogi üksikasjade vaatamine](media/e-Invoicing-services-get-started-MEX-View-cancellation-submission-log-details.png)

## <a name="privacy-notice"></a><span data-ttu-id="c277e-297">Privaatsusavaldus</span><span class="sxs-lookup"><span data-stu-id="c277e-297">Privacy notice</span></span>
<span data-ttu-id="c277e-298">Funktsioonide MX-00010 ja MX-00016 (CFDI arve ja CFDI tühistamine) lubamise korral on võimalik, et saata tuleb piiratud andmeid, sealhulgas organisatsiooni maksukohustuslasena registreerimise ID.</span><span class="sxs-lookup"><span data-stu-id="c277e-298">Enabling the MX-00010 and MX-00016 (CFDI Invoice and CFDI Cancellation) features may require sending limited data, which includes the organization tax registration ID.</span></span> <span data-ttu-id="c277e-299">See edastatakse maksuameti volitatud kolmandatest isikutest asutustele, mille eesmärk on saata maksuametile elektroonilisi arveid eelmääratletud vormingus, mis on vajalik integratsiooniks valitsuse veebiteenusega.</span><span class="sxs-lookup"><span data-stu-id="c277e-299">This will be transmitted to third-party agencies authorized by the tax authority for purposes of sending electronic invoices to this tax authority in the predefined format required for integration with the government’s web service.</span></span> <span data-ttu-id="c277e-300">Administraator saab lubada ja keelata funktsioonid MX-00010 ja MX-00016 (CFDI arve ja CFDI tühistamine), avades **Organisatsiooni haldus \> Seadistus \> Elektroonilise dokumendi parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="c277e-300">An administrator can enable and disable the MX-00010 and MX-00016 (CFDI Invoice and CFDI Cancellation) features by navigating to **Organization administration \> Setup \> Electronic document parameters**.</span></span> <span data-ttu-id="c277e-301">Valige vahekaart **Funktsioonid** , valige read, mis sisaldavad funktsioone MX-00010 ja MX-00016, ning seejärel tehke sobiv valik.</span><span class="sxs-lookup"><span data-stu-id="c277e-301">Select the **Features** tab, select the rows containing the MX-00010 and MX-00016 features, and then make the appropriate selection.</span></span> <span data-ttu-id="c277e-302">Nendest välissüsteemidest sellesse Dynamics 365 võrguteenusesse imporditud andmete puhul kehtib meie [privaatsusavaldus](https://go.microsoft.com/fwlink/?LinkId=512132).</span><span class="sxs-lookup"><span data-stu-id="c277e-302">Data imported from these external systems into this Dynamics 365 online service are subject to our [privacy statement](https://go.microsoft.com/fwlink/?LinkId=512132).</span></span> <span data-ttu-id="c277e-303">Lisateavet leiate riigipõhise funktsiooni dokumentatsioonis asuvatest privaatsusavalduse jaotistest.</span><span class="sxs-lookup"><span data-stu-id="c277e-303">Consult the Privacy notice sections in country-specific feature documentation for more information.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c277e-304">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="c277e-304">Additional resources</span></span>

- [<span data-ttu-id="c277e-305">Elektroonilise arvelduse lisandmooduli ülevaade</span><span class="sxs-lookup"><span data-stu-id="c277e-305">Electronic invoicing add-on overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="c277e-306">Elektroonilise arvelduse lisandmooduli kasutamise alustamine</span><span class="sxs-lookup"><span data-stu-id="c277e-306">Get started with the Electronic invoicing add-on</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="c277e-307">Elektroonilise arvelduse lisandmooduli seadistamine</span><span class="sxs-lookup"><span data-stu-id="c277e-307">Set up the Electronic invoicing add-on</span></span>](e-invoicing-setup.md)
