---
title: Brasiilia elektroonilise arvelduse lisandmooduli kasutamise alustamine
description: Sellest teemast leiate teabe, mis aitab teil rakendustes Microsoft Dynamics 365 Finance ja Dynamics 365 Supply Chain Management Brasiilia elektroonilise arvelduse lisandmoodulit kasutama hakata.
author: gionoder
manager: AnnBe
ms.date: 09/04/2020
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
ms.openlocfilehash: fb3ec2d60875d7a0747d64b397aafaa0a3d26348
ms.sourcegitcommit: d6250ee5ced43be39e789324a895fd1c07178935
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/19/2020
ms.locfileid: "4039865"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-brazil"></a><span data-ttu-id="65d31-103">Brasiilia elektroonilise arvelduse lisandmooduli kasutamise alustamine</span><span class="sxs-lookup"><span data-stu-id="65d31-103">Get started with the Electronic invoicing add-on for Brazil</span></span> 

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> <span data-ttu-id="65d31-104">Brasiilia elektroonilise arvelduse lisandmoodul ei toeta praegu kõiki funktsioone, mis on saadaval finantsdokumendi integratsioonis, mis on sisse ehitatud rakendustesse Microsoft Dynamics 365 Finance ja Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="65d31-104">The Electronic invoicing add-on for Brazil doesn't currently support all the functions that are available in the fiscal document integration that is built into Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="65d31-105">Sellest teemast leiate teabe, mis aitab teil Brasiilia elektroonilise arvelduse lisandmoodulit kasutama hakata.</span><span class="sxs-lookup"><span data-stu-id="65d31-105">This topic provides information that will help you get started with the Electronic invoicing add-on for Brazil.</span></span> <span data-ttu-id="65d31-106">Selles antakse juhiseid konfiguratsioonisammude kohta, mis on riigipõhised teenustes Regulatory Configuration Services (RCS) ning rakendustes Finance ja Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="65d31-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and in Finance and Supply Chain Management.</span></span> <span data-ttu-id="65d31-107">Samuti on selles juhised teenuse kaudu NF-e finantsdokumendi (elektroonilise finantsdokumendi mudel 55) esitamiseks ning selles selgitatakse, kuidas vaadata üle töötlemise tulemused ja finantsdokumentide olek.</span><span class="sxs-lookup"><span data-stu-id="65d31-107">It also guides you through the process of submitting an NF-e fiscal document (Electronic fiscal document model 55) through the service, and it explains how review the processing results and the status of the fiscal documents.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="65d31-108">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="65d31-108">Prerequisites</span></span>

<span data-ttu-id="65d31-109">Enne selle teema juhiste täitmist peate järgima teemas [Elektroonilise arvelduse lisandmooduli kasutamise alustamine](e-invoicing-get-started.md) olevaid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="65d31-109">Before you complete the steps in this topic, you must complete the steps in [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="65d31-110">RCS-i seadistus</span><span class="sxs-lookup"><span data-stu-id="65d31-110">RCS setup</span></span>

<span data-ttu-id="65d31-111">RCS-i seadistuse käigus teete järgmist.</span><span class="sxs-lookup"><span data-stu-id="65d31-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="65d31-112">E-arvelduse funktsiooni importimine NF-e finantsdokumentide jaoks.</span><span class="sxs-lookup"><span data-stu-id="65d31-112">Import the e-Invoicing feature for NF-e fiscal documents.</span></span>
2. <span data-ttu-id="65d31-113">Failivormingute ülevaatamine, mis on vajalikud NF-e finantsdokumentide edastamiseks autoriseerimise eesmärgil.</span><span class="sxs-lookup"><span data-stu-id="65d31-113">Review the file formats that are required to submit NF-e fiscal documents for authorization.</span></span>
3. <span data-ttu-id="65d31-114">Failivormingute ülevaatamine, mis on vajalikud kinnitatud NF-e tühistamise taotlemiseks.</span><span class="sxs-lookup"><span data-stu-id="65d31-114">Review the file formats that are required to request the cancellation of an approved NF-e.</span></span>
4. <span data-ttu-id="65d31-115">Sündmuse konfigureerimine, mis on vajalik NF-e finantsdokumentide edastamiseks autoriseerimise eesmärgil.</span><span class="sxs-lookup"><span data-stu-id="65d31-115">Configure the event that is required to submit NF-e fiscal documents for authorization.</span></span>
5. <span data-ttu-id="65d31-116">Sündmuse konfigureerimine, mis on vajalik kinnitatud NF-e tühistamise taotlemiseks.</span><span class="sxs-lookup"><span data-stu-id="65d31-116">Configure the event that is required to request the cancellation of an approved NF-e.</span></span>
6. <span data-ttu-id="65d31-117">E-arvelduse funktsiooni määramine elektroonilise arvelduse lisandmooduli keskkonnale.</span><span class="sxs-lookup"><span data-stu-id="65d31-117">Assign the e-Invoicing feature to an Electronic invoicing add-on environment.</span></span>
7. <span data-ttu-id="65d31-118">E-arvelduse funktsiooni avaldamine.</span><span class="sxs-lookup"><span data-stu-id="65d31-118">Publish the e-Invoicing feature.</span></span>

> [!NOTE]
> <span data-ttu-id="65d31-119">„E-arvelduse funktsioon” on kindla ressursi üldnimi, mis on konfigureeritud ja avaldatud kasutama elektroonilise arvelduse lisandmooduli serverit.</span><span class="sxs-lookup"><span data-stu-id="65d31-119">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing add-on server.</span></span> <span data-ttu-id="65d31-120">E-arvelduse funktsiooni seadistus hõlmab muu hulgas elektroonilise aruandluse (ER) konfiguratsiooni vormingute kasutamist, et luua konfigureeritavaid ekspordi- ja impordifaile, ning tegevuste ja tegevusvoogude kasutamist, et luua konfigureeritavaid reegleid taotluste saatmiseks, vastuste importimiseks ning vastuste sisu sõelumiseks.</span><span class="sxs-lookup"><span data-stu-id="65d31-120">The setup of the e-Invoicing feature combines, among other things, the use of Electronic reporting (ER) configuration formats to create configurable export and import files, and the use of actions and actions flows to enable the creation of configurable rules to send requests, import responses, and parse the response contents.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="65d31-121">E-arvelduse funktsiooni importimine</span><span class="sxs-lookup"><span data-stu-id="65d31-121">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="65d31-122">Logige oma RCS-i kontole sisse</span><span class="sxs-lookup"><span data-stu-id="65d31-122">Sign in to your RCS account</span></span>
2. <span data-ttu-id="65d31-123">Valige tööruumis **Globaliseerimisfunktsioonid** jaotises **Funktsioonid** paan **E-arveldus**.</span><span class="sxs-lookup"><span data-stu-id="65d31-123">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="65d31-124">Valige lehel **E-arvelduse funktsioonid** suvand **Impordi** , et importida globaalsest hoidlast NF-e finantsdokumendi e-arvelduse funktsioon.</span><span class="sxs-lookup"><span data-stu-id="65d31-124">On the **e-Invoicing Features** page, select **Import** to import a NF-e fiscal document e-Invoicing feature from the Global repository.</span></span>

    ![Nupp „Impordi”](media/e-Invoicing-services-get-started-BRA-Select-Import-e-Invoicing-feature.png)

4. <span data-ttu-id="65d31-126">Valige NF-e finantsdokumendi funktsioon ja seejärel valige **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="65d31-126">Select the NF-e fiscal document feature, and then select **Import**.</span></span>

    ![NF-e funktsiooni importimine](media/e-Invoicing-services-get-started-BRA-Select-Import-NF-e-feature.png)

### <a name="create-a-new-version-of-the-nf-e-fiscal-document-feature"></a><span data-ttu-id="65d31-128">NF-e finantsdokumendi funktsiooni uue versiooni loomine</span><span class="sxs-lookup"><span data-stu-id="65d31-128">Create a new version of the NF-e fiscal document feature</span></span>

- <span data-ttu-id="65d31-129">Valige lehel **E-arvelduse funktsioonid** vahekaardil **Versioonid** suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="65d31-129">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span>

![E-arvelduse funktsiooni uue versiooni lisamine](media/e-Invoicing-services-get-started-BRA-Select-New-e-Invoicing-feature-version.png)

### <a name="update-the-configuration-version"></a><span data-ttu-id="65d31-131">Konfiguratsiooni versiooni uuendamine</span><span class="sxs-lookup"><span data-stu-id="65d31-131">Update the configuration version</span></span>

1. <span data-ttu-id="65d31-132">Valige lehel **E-arvelduse funktsioonid** vahekaardil **Konfiguratsioonid** suvand **Lisa** või **Kustuta** , et hallata konfiguratsiooni versioone (ER-i failivormingu konfiguratsioone).</span><span class="sxs-lookup"><span data-stu-id="65d31-132">On the **e-Invoicing Features** page, on the **Configurations** tab, select **Add** or **Delete** to manage the configuration versions (ER file format configurations).</span></span>

    ![E-arvelduse funktsiooni konfiguratsioonide haldamine](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-configurations.png)

    - <span data-ttu-id="65d31-134">NF-e finantsdokumendi funktsiooni uue versiooni loomisel päritakse kõik konfiguratsiooniversioonid (ER-i failivormingud) uusimast versioonist.</span><span class="sxs-lookup"><span data-stu-id="65d31-134">When you create a new version of the NF-e fiscal document feature, all configuration version (ER file formats) are inherited from the latest version.</span></span>
    - <span data-ttu-id="65d31-135">NF-e finantsdokumendi edastamiseks autoriseerimise eesmärgil on vajalikud järgmised konfiguratsiooniversioonid.</span><span class="sxs-lookup"><span data-stu-id="65d31-135">To submit the NF-e fiscal document for authorization, the following configuration versions are required:</span></span>

        - <span data-ttu-id="65d31-136">NFe edastuse ekspordivorming</span><span class="sxs-lookup"><span data-stu-id="65d31-136">NFe submit export format</span></span>
        - <span data-ttu-id="65d31-137">NFe vastuseteate importimine</span><span class="sxs-lookup"><span data-stu-id="65d31-137">NFe response message import</span></span>
        - <span data-ttu-id="65d31-138">NFe tõrkelogi importimine</span><span class="sxs-lookup"><span data-stu-id="65d31-138">NFe error log import</span></span>

    - <span data-ttu-id="65d31-139">NF-e tühistamise edastamiseks on vajalik järgmine konfiguratsiooniversioon.</span><span class="sxs-lookup"><span data-stu-id="65d31-139">To submit the NF-e cancellation, the following configuration version is required:</span></span>

        - <span data-ttu-id="65d31-140">NFe tühistamise ekspordivorming</span><span class="sxs-lookup"><span data-stu-id="65d31-140">NFe cancel export format</span></span>

2. <span data-ttu-id="65d31-141">Valige loendist konfiguratsiooni versioon ja seejärel suvand **Redigeeri** või **Kuva** , et avada leht **Vormingukujundaja** , kus saate konfiguratsiooni redigeerida või vaadata.</span><span class="sxs-lookup"><span data-stu-id="65d31-141">In the list, select a configuration version, and then select **Edit** or **View** to open the **Format designer** page, where you can edit or view the configuration.</span></span>

    ![Vormingukujundaja lehe avamine](media/e-Invoicing-services-get-started-BRA-Configuration-ER-fomat-designer.png)

3. <span data-ttu-id="65d31-143">Kasutage ER-i vormingu failikonfiguratsioonide redigeerimiseks või kuvamiseks lehte **Vormingukujundaja**.</span><span class="sxs-lookup"><span data-stu-id="65d31-143">Use the **Format designer** page to edit or view the ER format file configurations.</span></span> <span data-ttu-id="65d31-144">Lisateavet leiate jaotisest [Elektrooniliste dokumentide konfiguratsioonide loomine](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration).</span><span class="sxs-lookup"><span data-stu-id="65d31-144">For more information, see [Create electronic document configurations](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/electronic-reporting-configuration).</span></span>

    ![Vormingukujundaja leht](media/e-Invoicing-services-get-started-BRA-ER-Format-designer.png)

### <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="65d31-146">E-arvelduse funktsiooni seadistuste haldamine</span><span class="sxs-lookup"><span data-stu-id="65d31-146">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="65d31-147">Valige lehel **E-arvelduse funktsioonid** vahekaardil **Seadistused** suvand **Lisa** või **Kustuta** , et hallata e-arvelduse funktsiooni seadistusi (st NF-e sündmusi).</span><span class="sxs-lookup"><span data-stu-id="65d31-147">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add** or **Delete** to manage the e-Invoicing feature setups (that is, NF-e events).</span></span>

![E-arvelduse funktsiooni seadistuste haldamine](media/e-Invoicing-services-get-started-BRA-Manage-e-Invoicing-feature-setup.png)

<span data-ttu-id="65d31-149">Kui loote NF-e finantsdokumendi funktsiooni uue versiooni, mis on tuletatud mõnest teisest e-arvelduse funktsioonist, päritakse kõik funktsiooniseadistused (NF-e sündmused) uusimast versioonist.</span><span class="sxs-lookup"><span data-stu-id="65d31-149">When you create a new version of the NF-e fiscal document feature that is derived from another e-Invoicing feature, all feature setups (NF-e events) are inherited from the latest version.</span></span>

<span data-ttu-id="65d31-150">NF-e finantsdokumentide edastamiseks autoriseerimise eesmärgil on vajalik funktsiooniseadistus **Edastus**.</span><span class="sxs-lookup"><span data-stu-id="65d31-150">To submit NF-e fiscal documents for authorization, the **Submit** feature setup is required.</span></span>

<span data-ttu-id="65d31-151">NF-e tühistamise edastamiseks on vajalik funktsiooniseadistus **Tühistamine**.</span><span class="sxs-lookup"><span data-stu-id="65d31-151">To submit NF-e cancellation, the **Cancellation** feature setup is required.</span></span>

#### <a name="configure-the-submit-feature-setup"></a><span data-ttu-id="65d31-152">Edastusfunktsiooni seadistuse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="65d31-152">Configure the Submit feature setup</span></span>

1. <span data-ttu-id="65d31-153">Valige lehe **E-arvelduse funktsioonid** vahekaardi **Seadistused** veerus **Funktsiooni seadistus** suvand **Edastus**.</span><span class="sxs-lookup"><span data-stu-id="65d31-153">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Submit**.</span></span>
2. <span data-ttu-id="65d31-154">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="65d31-154">Select **Edit**.</span></span>

    ![E-arvelduse funktsiooni seadistuse redigeerimine](media/e-Invoicing-services-get-started-BRA-Edit-e-Invoicing-feature-setup.png)

3. <span data-ttu-id="65d31-156">Valige lehel **Funktsiooni versiooni seadistus** vahekaart **Tegevused** , et hallata tegevuste loendit.</span><span class="sxs-lookup"><span data-stu-id="65d31-156">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span>

    ![Tegevuste vahekaart](media/e-Invoicing-services-get-started-BRA-Select-Actions.png)

4. <span data-ttu-id="65d31-158">Tegevuste ülevaatamine, mis on vajalikud NF-e edastamiseks autoriseerimise eesmärgil.</span><span class="sxs-lookup"><span data-stu-id="65d31-158">Review the actions that are required to submit an NF-e for authorization.</span></span>

    | <span data-ttu-id="65d31-159">Tegevuse ID</span><span class="sxs-lookup"><span data-stu-id="65d31-159">Action ID</span></span> | <span data-ttu-id="65d31-160">Tegevuse nimi</span><span class="sxs-lookup"><span data-stu-id="65d31-160">Action name</span></span>                  | <span data-ttu-id="65d31-161">Tegevuse kirjeldus</span><span class="sxs-lookup"><span data-stu-id="65d31-161">Action description</span></span>                                                |
    |-----------|------------------------------|-------------------------------------------------------------------|
    | <span data-ttu-id="65d31-162">1</span><span class="sxs-lookup"><span data-stu-id="65d31-162">1</span></span>         | <span data-ttu-id="65d31-163">Teisenda dokument</span><span class="sxs-lookup"><span data-stu-id="65d31-163">Transform document</span></span>           | <span data-ttu-id="65d31-164">NF-e XML-faili loomine edastamiseks.</span><span class="sxs-lookup"><span data-stu-id="65d31-164">Create the NF-e XML file for submission.</span></span>                          |
    | <span data-ttu-id="65d31-165">2</span><span class="sxs-lookup"><span data-stu-id="65d31-165">2</span></span>         | <span data-ttu-id="65d31-166">Allkirjasta dokument</span><span class="sxs-lookup"><span data-stu-id="65d31-166">Sign document</span></span>                | <span data-ttu-id="65d31-167">Digitaalserdi lisamine XML-failile.</span><span class="sxs-lookup"><span data-stu-id="65d31-167">Apply the digital certificate to the XML file.</span></span>                    |
    | <span data-ttu-id="65d31-168">3</span><span class="sxs-lookup"><span data-stu-id="65d31-168">3</span></span>         | <span data-ttu-id="65d31-169">Kutsu Brasiilia SEFAZ teenust</span><span class="sxs-lookup"><span data-stu-id="65d31-169">Call Brazilian SEFAZ service</span></span> | <span data-ttu-id="65d31-170">Allkirjastatud XML-fail edastamine veebiteenustele autoriseerimise eesmärgil.</span><span class="sxs-lookup"><span data-stu-id="65d31-170">Submit the signed XML file to the web services for authorization.</span></span> |
    | <span data-ttu-id="65d31-171">4</span><span class="sxs-lookup"><span data-stu-id="65d31-171">4</span></span>         | <span data-ttu-id="65d31-172">Töötle vastust</span><span class="sxs-lookup"><span data-stu-id="65d31-172">Process response</span></span>             | <span data-ttu-id="65d31-173">Veebiteenuse vastuse hankimine.</span><span class="sxs-lookup"><span data-stu-id="65d31-173">Get the web service response.</span></span>                                     |
    | <span data-ttu-id="65d31-174">5</span><span class="sxs-lookup"><span data-stu-id="65d31-174">5</span></span>         | <span data-ttu-id="65d31-175">Teisenda dokument</span><span class="sxs-lookup"><span data-stu-id="65d31-175">Transform document</span></span>           | <span data-ttu-id="65d31-176">Vastusena saadud faili sisu sõelumine.</span><span class="sxs-lookup"><span data-stu-id="65d31-176">Parse the content of the file that is received as a response.</span></span>     |
    | <span data-ttu-id="65d31-177">6</span><span class="sxs-lookup"><span data-stu-id="65d31-177">6</span></span>         | <span data-ttu-id="65d31-178">Teisenda dokument</span><span class="sxs-lookup"><span data-stu-id="65d31-178">Transform document</span></span>           | <span data-ttu-id="65d31-179">XML-faili loomine edastuse oleku kohta teabe küsimiseks.</span><span class="sxs-lookup"><span data-stu-id="65d31-179">Create the XML file to inquire about status of the submission.</span></span>    |
    | <span data-ttu-id="65d31-180">7</span><span class="sxs-lookup"><span data-stu-id="65d31-180">7</span></span>         | <span data-ttu-id="65d31-181">Kutsu Brasiilia SEFAZ teenust</span><span class="sxs-lookup"><span data-stu-id="65d31-181">Call Brazilian SEFAZ service</span></span> | <span data-ttu-id="65d31-182">XML-faili edastamine, mis küsib edastuse olekut.</span><span class="sxs-lookup"><span data-stu-id="65d31-182">Submit the XML file that requests the submission status.</span></span>          |
    | <span data-ttu-id="65d31-183">8</span><span class="sxs-lookup"><span data-stu-id="65d31-183">8</span></span>         | <span data-ttu-id="65d31-184">Töötle vastust</span><span class="sxs-lookup"><span data-stu-id="65d31-184">Process response</span></span>             | <span data-ttu-id="65d31-185">Veebiteenuse vastuse hankimine.</span><span class="sxs-lookup"><span data-stu-id="65d31-185">Get the web service response.</span></span>                                     |

#### <a name="set-up-the-url-for-sefaz-web-services"></a><span data-ttu-id="65d31-186">SEFAZ veebiteenuste URL-i seadistamine</span><span class="sxs-lookup"><span data-stu-id="65d31-186">Set up the URL for SEFAZ web services</span></span> 

1. <span data-ttu-id="65d31-187">Valige lehel **Funktsiooni versiooni seadistus** vahekaardi **Tegevused** kiirkaardilt **Tegevused** suvand **Kutsu Brasiilia SEFAZ teenust** (tegevuse ID **3** ).</span><span class="sxs-lookup"><span data-stu-id="65d31-187">On the **Feature version setup** page, on the **Actions** tab, on the **Actions** FastTab, select **Call Brazilian SEFAZ service** (action ID **3** ).</span></span>
2. <span data-ttu-id="65d31-188">Sisestage kiirkaardil **Parameetrid** väljale **URL-aadressi parameeter** NF-e edastamiseks SEFAZ veebiteenuse URL.</span><span class="sxs-lookup"><span data-stu-id="65d31-188">On the **Parameters** FastTab, in the **URL address parameter** field, enter the URL of the SEFAZ web service for NF-e submission.</span></span>
3. <span data-ttu-id="65d31-189">Valige kiirkaardil **Tegevused** suvand **Kutsu Brasiilia SEFAZ teenust** (tegevuse ID **7** ).</span><span class="sxs-lookup"><span data-stu-id="65d31-189">On the **Actions** FastTab, select **Call Brazilian SEFAZ service** (action ID **7** ).</span></span>
4. <span data-ttu-id="65d31-190">Sisestage kiirkaardil **Parameetrid** väljale **URL-aadressi parameeter** NF-e edastamiseks SEFAZ veebiteenuse URL.</span><span class="sxs-lookup"><span data-stu-id="65d31-190">On the **Parameters** FastTab, in the **URL address parameter** field, enter the URL of the SEFAZ web service for NF-e submission.</span></span>

#### <a name="configure-the-cancellation-feature-setup"></a><span data-ttu-id="65d31-191">Tühistamisfunktsiooni seadistuse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="65d31-191">Configure the Cancellation feature setup</span></span>

1. <span data-ttu-id="65d31-192">Valige lehe **E-arvelduse funktsioonid** vahekaardi **Seadistused** veerus **Funktsiooni seadistus** suvand **Tühistamine**.</span><span class="sxs-lookup"><span data-stu-id="65d31-192">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Cancellation**.</span></span>
2. <span data-ttu-id="65d31-193">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="65d31-193">Select **Edit**.</span></span>
3. <span data-ttu-id="65d31-194">Valige lehel **Funktsiooni versiooni seadistus** vahekaart **Tegevused** , et hallata tegevuste loendit.</span><span class="sxs-lookup"><span data-stu-id="65d31-194">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span>
4. <span data-ttu-id="65d31-195">Vaadake üle tegevused, mis on vajalikud kinnitatud NF-e tühistamise taotlemiseks.</span><span class="sxs-lookup"><span data-stu-id="65d31-195">Review the actions that are required to request the cancellation of an approved NF-e.</span></span>

    | <span data-ttu-id="65d31-196">Tegevuse ID</span><span class="sxs-lookup"><span data-stu-id="65d31-196">Action ID</span></span> | <span data-ttu-id="65d31-197">Tegevuse nimi</span><span class="sxs-lookup"><span data-stu-id="65d31-197">Action name</span></span>                  | <span data-ttu-id="65d31-198">Tegevuse kirjeldus</span><span class="sxs-lookup"><span data-stu-id="65d31-198">Action description</span></span>                                               |
    |-----------|------------------------------|------------------------------------------------------------------|
    | <span data-ttu-id="65d31-199">1</span><span class="sxs-lookup"><span data-stu-id="65d31-199">1</span></span>         | <span data-ttu-id="65d31-200">Teisenda dokument</span><span class="sxs-lookup"><span data-stu-id="65d31-200">Transform document</span></span>           | <span data-ttu-id="65d31-201">NF-e tühistamise XML-faili loomine edastamiseks.</span><span class="sxs-lookup"><span data-stu-id="65d31-201">Create the NF-e cancellation XML file for submission.</span></span>            |
    | <span data-ttu-id="65d31-202">2</span><span class="sxs-lookup"><span data-stu-id="65d31-202">2</span></span>         | <span data-ttu-id="65d31-203">Allkirjasta dokument</span><span class="sxs-lookup"><span data-stu-id="65d31-203">Sign document</span></span>                | <span data-ttu-id="65d31-204">Digitaalserdi lisamine XML-failile.</span><span class="sxs-lookup"><span data-stu-id="65d31-204">Apply the digital certificate to the XML file.</span></span>                   |
    | <span data-ttu-id="65d31-205">3</span><span class="sxs-lookup"><span data-stu-id="65d31-205">3</span></span>         | <span data-ttu-id="65d31-206">Kutsu Brasiilia SEFAZ teenust</span><span class="sxs-lookup"><span data-stu-id="65d31-206">Call Brazilian SEFAZ service</span></span> | <span data-ttu-id="65d31-207">Allkirjastatud XML-fail edastamine veebiteenustele tühistamise eesmärgil.</span><span class="sxs-lookup"><span data-stu-id="65d31-207">Submit the signed XML file to the web services for cancellation.</span></span> |
    | <span data-ttu-id="65d31-208">4</span><span class="sxs-lookup"><span data-stu-id="65d31-208">4</span></span>         | <span data-ttu-id="65d31-209">Töötle vastust</span><span class="sxs-lookup"><span data-stu-id="65d31-209">Process response</span></span>             | <span data-ttu-id="65d31-210">Veebiteenuse vastuse hankimine.</span><span class="sxs-lookup"><span data-stu-id="65d31-210">Get the web service response.</span></span>                                    |

#### <a name="set-up-the-url-for-sefaz-web-services"></a><span data-ttu-id="65d31-211">SEFAZ veebiteenuste URL-i seadistamine</span><span class="sxs-lookup"><span data-stu-id="65d31-211">Set up the URL for SEFAZ web services</span></span>

1. <span data-ttu-id="65d31-212">Valige lehel **Funktsiooni versiooni seadistus** vahekaardi **Tegevused** kiirkaardilt **Tegevused** suvand **Kutsu Brasiilia SEFAZ teenust** (tegevuse ID **3** ).</span><span class="sxs-lookup"><span data-stu-id="65d31-212">On the **Feature version setup** page, on the **Actions** tab, on the **Actions** FastTab, select **Call Brazilian SEFAZ service** (action ID **3** ).</span></span>
2. <span data-ttu-id="65d31-213">Sisestage kiirkaardil **Parameetrid** väljale **URL-aadressi parameeter** kinnitatud NF-e tühistamiseks SEFAZ veebiteenuse URL.</span><span class="sxs-lookup"><span data-stu-id="65d31-213">On the **Parameters** FastTab, in the **URL address parameter** field, enter the URL of the SEFAZ web service for cancellation of an approved NF-e.</span></span>

### <a name="make-an-e-invoicing-environment-available-and-assign-a-draft-version"></a><span data-ttu-id="65d31-214">E-arvelduse keskkonna kättesaadavaks tegemine ja mustandversiooni määramine</span><span class="sxs-lookup"><span data-stu-id="65d31-214">Make an e-Invoicing environment available and assign a Draft version</span></span>

1. <span data-ttu-id="65d31-215">Valige lehel **E-arvelduse funktsioonid** vahekaardil **Keskkonnad** suvand **Luba**.</span><span class="sxs-lookup"><span data-stu-id="65d31-215">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="65d31-216">Valige keskkond väljal **Keskkond**.</span><span class="sxs-lookup"><span data-stu-id="65d31-216">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="65d31-217">Valige väljal **Kehtiv alates** kuupäev, mil uus keskkond peaks kehtima hakkama.</span><span class="sxs-lookup"><span data-stu-id="65d31-217">In the **Effective from** field, select the date when the environment should become effective.</span></span>
4. <span data-ttu-id="65d31-218">Valige **Luba**.</span><span class="sxs-lookup"><span data-stu-id="65d31-218">Select **Enable**.</span></span>

![E-arvelduse keskkonna lubamine](media/e-Invoicing-services-get-started-BRA-Enable-e-Invoicing-environment.png)

### <a name="change-the-status-to-completed"></a><span data-ttu-id="65d31-220">Oleku muutmine lõpetatuks</span><span class="sxs-lookup"><span data-stu-id="65d31-220">Change the status to Completed</span></span>

1. <span data-ttu-id="65d31-221">Valige lehel **E-arvelduse funktsioonid** vahekaardil **Versioonid** e-arvelduse funktsiooni versioon, mille olek on **Mustand**.</span><span class="sxs-lookup"><span data-stu-id="65d31-221">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="65d31-222">Valige **Muuda olekut \> Lõpule viidud**.</span><span class="sxs-lookup"><span data-stu-id="65d31-222">Select **Change status \> Complete**.</span></span>

### <a name="change-the-status-to-publish"></a><span data-ttu-id="65d31-223">Oleku muutmine avaldatuks</span><span class="sxs-lookup"><span data-stu-id="65d31-223">Change the status to Publish</span></span>

1. <span data-ttu-id="65d31-224">Valige lehel **E-arvelduse funktsioonid** vahekaardil **Versioonid** e-arvelduse funktsiooni versioon, mille olek on **Lõpetatud**.</span><span class="sxs-lookup"><span data-stu-id="65d31-224">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Completed**.</span></span>
2. <span data-ttu-id="65d31-225">Valige **Muuda olekut \> Avalda**.</span><span class="sxs-lookup"><span data-stu-id="65d31-225">Select **Change status \> Publish**.</span></span>

![E-arvelduse funktsiooni avaldamine](media/e-Invoicing-services-get-started-BRA-Publish-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-add-on-integration-in-finance-or-supply-chain-management"></a><span data-ttu-id="65d31-227">Elektroonilise arvelduse lisandmooduli integratsiooni seadistamine rakenduses Finance või Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="65d31-227">Set up Electronic invoicing add-on integration in Finance or Supply Chain Management</span></span>

<span data-ttu-id="65d31-228">Seadistuse käigus teete järgmist.</span><span class="sxs-lookup"><span data-stu-id="65d31-228">During setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="65d31-229">Brasiilia NF-e föderaalse funktsiooni sisselülitamine.</span><span class="sxs-lookup"><span data-stu-id="65d31-229">Turn on the NF-e Federal feature for Brazil.</span></span>
2. <span data-ttu-id="65d31-230">Kindla ER-i andmemudeli, ER-i andmemudeli vastenduse ja NF-e finantsdokumentide jaoks vajalike vormingute importimine.</span><span class="sxs-lookup"><span data-stu-id="65d31-230">Import the specific ER data model, the data model mapping, and the formats that are required for NF-e fiscal documents.</span></span>
3. <span data-ttu-id="65d31-231">ER-i konfiguratsiooni importimine ja vastusetüüpide seadistamine, mis on vajalikud finantsdokumendi oleku värskendamiseks pärast edastusprotsessi tagastamist.</span><span class="sxs-lookup"><span data-stu-id="65d31-231">Import the ER configuration, and set up the response types that are required to update the status of the fiscal document after the submission process is returned.</span></span>

### <a name="turn-on-the-nf-e-federal-feature-for-brazil"></a><span data-ttu-id="65d31-232">Brasiilia NF-e föderaalse funktsiooni sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="65d31-232">Turn on the NF-e Federal feature for Brazil</span></span>

1. <span data-ttu-id="65d31-233">Avage **Organisatsiooni haldus \> Seadistus \> Elektroonilise dokumendi parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="65d31-233">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="65d31-234">Märkige vahekaardil **Funktsioonid** märkeruut **Luba** funktsiooniviite **BR00053** rea puhul.</span><span class="sxs-lookup"><span data-stu-id="65d31-234">On the **Features** tab, select the **Enable** check box in the row for feature reference **BR00053**.</span></span>

### <a name="import-the-er-data-model-mapping-required-for-nf-e-fiscal-documents"></a><span data-ttu-id="65d31-235">NF-e finantsdokumentide jaoks vajaliku ER-i andmemudeli vastenduse importimine</span><span class="sxs-lookup"><span data-stu-id="65d31-235">Import the ER data model mapping required for NF-e fiscal documents</span></span>

1. <span data-ttu-id="65d31-236">Logige sisse rakendusse Finance.</span><span class="sxs-lookup"><span data-stu-id="65d31-236">Sign in to Finance.</span></span>
2. <span data-ttu-id="65d31-237">Valige tööruumi **Elektrooniline aruandlus** jaotisest **Konfiguratsioonipakkujad** paan **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="65d31-237">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** tile.</span></span> <span data-ttu-id="65d31-238">Veenduge, et konfiguratsioonipakkuja olekuks oleks seatud **Aktiivne**.</span><span class="sxs-lookup"><span data-stu-id="65d31-238">Make sure that this configuration provider is set to **Active**.</span></span> <span data-ttu-id="65d31-239">Lisateavet pakkuja **aktiivseks** märkimise kohta leiate teemast [Konfiguratsioonipakkujate loomine ja nende aktiivseks märkimine](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span><span class="sxs-lookup"><span data-stu-id="65d31-239">For information about how to set a provider to **Active** , see [Create configuration providers and mark them as active](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/analytics/tasks/er-configuration-provider-mark-it-active-2016-11).</span></span>
3. <span data-ttu-id="65d31-240">Valige **Osad**.</span><span class="sxs-lookup"><span data-stu-id="65d31-240">Select **Repositories**.</span></span>
4. <span data-ttu-id="65d31-241">Valige **Globaalne ressurss \> Ava**.</span><span class="sxs-lookup"><span data-stu-id="65d31-241">Select **Global resource \> Open**.</span></span>
5. <span data-ttu-id="65d31-242">Importige **Finantsdokumentide vastenduse** konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="65d31-242">Import **Fiscal documents mapping** configurations.</span></span>

### <a name="import-er-configurations-and-set-up-the-response-types-for-fiscal-documents"></a><span data-ttu-id="65d31-243">ER-i konfiguratsioonide importimine ja vastusetüüpide seadistamine finantsdokumentide jaoks</span><span class="sxs-lookup"><span data-stu-id="65d31-243">Import ER configurations and set up the response types for fiscal documents</span></span>

1. <span data-ttu-id="65d31-244">Valige tööruumi **Elektrooniline aruandlus** jaotisest **Konfiguratsioonipakkujad** paan **Microsoft**.</span><span class="sxs-lookup"><span data-stu-id="65d31-244">In the **Electronic reporting** workspace, in the **Configuration providers** section, select the **Microsoft** tile.</span></span>
2. <span data-ttu-id="65d31-245">Valige **Osad**.</span><span class="sxs-lookup"><span data-stu-id="65d31-245">Select **Repositories**.</span></span>
3. <span data-ttu-id="65d31-246">Valige **Globaalne ressurss \> Ava**.</span><span class="sxs-lookup"><span data-stu-id="65d31-246">Select **Global resource \> Open**.</span></span>
4. <span data-ttu-id="65d31-247">Importige **NF-e tõrkelogi importimine (BR)** , **NF-e vastuseandmete impordivorming (BR)** ja **NF-e vastuseteate importimine (BR)**.</span><span class="sxs-lookup"><span data-stu-id="65d31-247">Import **NF-e error log import (BR)** , **NF-e response data import format (BR)** , and **NF-e response message import (BR)**.</span></span>
5. <span data-ttu-id="65d31-248">Avage **Organisatsiooni haldus \> Seadistus \> Elektroonilise dokumendi parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="65d31-248">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
6. <span data-ttu-id="65d31-249">Valige lehel **Elektrooniline dokument** suvand **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="65d31-249">On the **Electronic document** tab, select **Add**.</span></span>
6. <span data-ttu-id="65d31-250">Sisestage väljale **Tabeli nimi** tekst **Finantsdokumendi päis**.</span><span class="sxs-lookup"><span data-stu-id="65d31-250">In the **Table name** field, enter **Fiscal document header**.</span></span>
7. <span data-ttu-id="65d31-251">Valige väljal **Dokumendi kontekst** suvand **Kliendiarve kontekstimudel – finantsdokumendi kontekst**.</span><span class="sxs-lookup"><span data-stu-id="65d31-251">In the **Document context** field, select **Customer invoice context model – Fiscal document context**.</span></span>
8. <span data-ttu-id="65d31-252">Valige **Vastusetüübid**.</span><span class="sxs-lookup"><span data-stu-id="65d31-252">Select **Response types**.</span></span>
9. <span data-ttu-id="65d31-253">Valige **Uus** ja valige siis väljal **Vastusetüüp** suvand **Vastus**.</span><span class="sxs-lookup"><span data-stu-id="65d31-253">Select **New** , and then, in the **Response type** field, select **Response**.</span></span>
10. <span data-ttu-id="65d31-254">Valige väljal **Edastuse olek** suvand **Ootel**.</span><span class="sxs-lookup"><span data-stu-id="65d31-254">In the **Submission status** field, select **Pending**.</span></span>
11. <span data-ttu-id="65d31-255">Valige väljal **Mudelivastendus** suvand **Vastuseteate impordivorming – mudelivastendus vastuseteatest**.</span><span class="sxs-lookup"><span data-stu-id="65d31-255">In the **Model mapping** field, select **Response message import format – Model mapping from response message**.</span></span>
12. <span data-ttu-id="65d31-256">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="65d31-256">Select **Save**.</span></span>
13. <span data-ttu-id="65d31-257">Valige **Uus** ja sisestage siis väljale **Vastusetüüp** väärtus **ResponseData**.</span><span class="sxs-lookup"><span data-stu-id="65d31-257">Select **New** , and then, in the **Response type** field, enter **ResponseData**.</span></span>
14. <span data-ttu-id="65d31-258">Valige väljal **Edastuse olek** suvand **Ootel**.</span><span class="sxs-lookup"><span data-stu-id="65d31-258">In the **Submission status** field, select **Pending**.</span></span>
15. <span data-ttu-id="65d31-259">Valige väljal **Mudelivastendus** suvand **NFe vastuseandmete impordivorming – vastuseandmete importimine**.</span><span class="sxs-lookup"><span data-stu-id="65d31-259">In the **Model mapping** field, select **NFe response data import format – Response data import**.</span></span>
16. <span data-ttu-id="65d31-260">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="65d31-260">Select **Save**.</span></span>

## <a name="electronic-invoice-processing"></a><span data-ttu-id="65d31-261">Elektroonilise arve töötlemine</span><span class="sxs-lookup"><span data-stu-id="65d31-261">Electronic invoice processing</span></span>

<span data-ttu-id="65d31-262">Rakenduses Finance teete töötlemise käigus järgmist.</span><span class="sxs-lookup"><span data-stu-id="65d31-262">During processing in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="65d31-263">Finantsdokumendi edastamine elektroonilise arvelduse lisandmooduli kaudu.</span><span class="sxs-lookup"><span data-stu-id="65d31-263">Submit a fiscal document through the Electronic invoicing add-on.</span></span>
2. <span data-ttu-id="65d31-264">Edastuse käivituslogide vaatamine ja töötlemise tulemuste ülevaatamine.</span><span class="sxs-lookup"><span data-stu-id="65d31-264">View the submission execution logs and review the results of processing.</span></span>
3. <span data-ttu-id="65d31-265">Finantsdokumendi tühistamise edastamine elektroonilise arvelduse lisandmooduli kaudu.</span><span class="sxs-lookup"><span data-stu-id="65d31-265">Submit the cancellation of a fiscal document through the Electronic invoicing add-on.</span></span>

### <a name="submit-nf-e-fiscal-documents-for-sefaz-authorization"></a><span data-ttu-id="65d31-266">NF-e finantsdokumentide edastamine SEFAZ-is autoriseerimiseks</span><span class="sxs-lookup"><span data-stu-id="65d31-266">Submit NF-e fiscal documents for SEFAZ authorization</span></span> 

<span data-ttu-id="65d31-267">Pärast funktsiooni **Konfigureeritav elektroonilise arvelduse lisandmooduli integratsioon** sisse lülitamist pole enam võimalik kasutada vana protsessi NF-e finantsdokumentide edastamiseks autoriseerimise eesmärgil ( **NF-e eksportimise/importimise protsess** ).</span><span class="sxs-lookup"><span data-stu-id="65d31-267">After you turn on the **Configurable Electronic invoicing add-on integration** feature, the old process for submitting NF-e fiscal documents for authorization ( **Export/Import NF-e process** ) can no longer be used.</span></span> <span data-ttu-id="65d31-268">See asendatakse uue protsessiga **Edasta elektroonilised dokumendid**.</span><span class="sxs-lookup"><span data-stu-id="65d31-268">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

> [!NOTE]
> <span data-ttu-id="65d31-269">Enne jätkamist veenduge, et teil on üks või mitu kliendi finantsdokumentide mudelit 55, mille väljastas kliendi finantsasutus.</span><span class="sxs-lookup"><span data-stu-id="65d31-269">Before you continue, make sure that you have one or more customer fiscal documents model 55 that were issued by the customer's fiscal establishment.</span></span> <span data-ttu-id="65d31-270">Nende finantsdokumentide suunaks peab olema määratud **Väljuv** ja olekuks **Loodud**.</span><span class="sxs-lookup"><span data-stu-id="65d31-270">The direction for these fiscal documents must be set to **Outgoing** , and the status must be **Created**.</span></span> <span data-ttu-id="65d31-271">Lisateavet leiate teemast [Kliendi finantsdokumendi väljastamine (Brasiilia)](https://docs.microsoft.com/dynamics365/finance/localizations/tasks/br-00038-issuing-customer-fiscal-document).</span><span class="sxs-lookup"><span data-stu-id="65d31-271">For more information, see [Issue customer fiscal document (Brazil)](https://docs.microsoft.com/dynamics365/finance/localizations/tasks/br-00038-issuing-customer-fiscal-document).</span></span>

1. <span data-ttu-id="65d31-272">Avage **Organisatsiooni haldus \> Perioodiline \> Elektroonilised dokumendid \> Edasta elektroonilised dokumendid**.</span><span class="sxs-lookup"><span data-stu-id="65d31-272">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="65d31-273">Mis tahes dokumendi esimese edastamise korral seadke suvandi **Dokumentide taasedastamine** väärtuseks alati **Ei**.</span><span class="sxs-lookup"><span data-stu-id="65d31-273">For the first submission of any document, always set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="65d31-274">Kui peate dokumendi teenuse kaudu uuesti edastama, seadke selle suvandi väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="65d31-274">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="65d31-275">Valige kiirkaardil **Kaasatavad kirjed** suvand **Filter** , et avada dialoogiboks **Päring** , kus saate luua päringu edastatavate dokumentide valimiseks.</span><span class="sxs-lookup"><span data-stu-id="65d31-275">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>
4. <span data-ttu-id="65d31-276">Valige vahekaardil **Vahemik** suvand **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="65d31-276">On the **Range** tab, select **Add**.</span></span>
5. <span data-ttu-id="65d31-277">Valige väljal **Tabel** suvand **Finantsdokumendi päis**.</span><span class="sxs-lookup"><span data-stu-id="65d31-277">In the **Table** field, select **Fiscal document header**.</span></span>
6. <span data-ttu-id="65d31-278">Valige väljal **Tuletatud tabel** suvand **Finantsdokumendi päis**.</span><span class="sxs-lookup"><span data-stu-id="65d31-278">In the **Derived table** field, select **Fiscal document header**.</span></span>
6. <span data-ttu-id="65d31-279">Valige väljal **Väli** suvand **Arv**.</span><span class="sxs-lookup"><span data-stu-id="65d31-279">In the **Field** field, select **Number**.</span></span>
7. <span data-ttu-id="65d31-280">Sisestage väljale **Kriteerium** edastatavate finantsdokumentide arv.</span><span class="sxs-lookup"><span data-stu-id="65d31-280">In the **Criteria** field, enter the number of the fiscal document that should be submitted.</span></span>
8. <span data-ttu-id="65d31-281">Valige dialoogiboksi **Päring** sulgemiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="65d31-281">Select **OK** to close the **Inquiry** dialog box.</span></span>
8. <span data-ttu-id="65d31-282">Valige **OK** , et valitud dokumendid edastada.</span><span class="sxs-lookup"><span data-stu-id="65d31-282">Select **OK** to submit the selected documents.</span></span>

> [!NOTE]
> <span data-ttu-id="65d31-283">Esimesel dokumendi edastamise katsel teenuse kaudu palutakse teil kinnitada ühendus elektroonilise arvelduse lisandmooduliga.</span><span class="sxs-lookup"><span data-stu-id="65d31-283">During your first attempt to submit a document through the service, you will be prompted to confirm the connection with the Electronic invoicing add-on.</span></span> <span data-ttu-id="65d31-284">Valige **Elektroonilise dokumendi edastusteenusega ühendumiseks klõpsake siin**.</span><span class="sxs-lookup"><span data-stu-id="65d31-284">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

### <a name="view-all-submission-logs"></a><span data-ttu-id="65d31-285">Kõigi edastuslogide kuvamine</span><span class="sxs-lookup"><span data-stu-id="65d31-285">View all submission logs</span></span>

<span data-ttu-id="65d31-286">Pärast funktsiooni **Konfigureeritav elektroonilise arvelduse lisandmooduli integratsioon** sisse lülitamist on saadaval uus leht, mis võimaldab teil jälgida dokumendi edastamise edenemist.</span><span class="sxs-lookup"><span data-stu-id="65d31-286">After you turn on the **Configurable Electronic invoicing add-on integration** feature, a new page is available that lets you follow up on the document submission process.</span></span> <span data-ttu-id="65d31-287">Selle lehe abil saate vaadata kõigi edastatud dokumentide edastuslogisid.</span><span class="sxs-lookup"><span data-stu-id="65d31-287">You can use this page to view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="65d31-288">Avage **Organisatsiooni haldus \> Perioodiline \> Elektroonilised dokumendid \> Elektroonilise dokumendi edastuslogi**.</span><span class="sxs-lookup"><span data-stu-id="65d31-288">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="65d31-289">Valige väljal **Dokumenditüüp** suvand **Finantsdokumendi päis** , et kuvada ainult finantsdokumendid.</span><span class="sxs-lookup"><span data-stu-id="65d31-289">In the **Document type** field, select **Fiscal document header** to filter for fiscal documents only.</span></span>
3. <span data-ttu-id="65d31-290">Valige toimingupaanil **Päringud \> Edastuse üksikasjad** , et vaadata edastuse käivituslogide üksikasju.</span><span class="sxs-lookup"><span data-stu-id="65d31-290">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

![Edastuslogi üksikasjade vaatamine](media/e-Invoicing-services-get-started-BRA-View-Submission-log-details.png)

> [!NOTE] 
> <span data-ttu-id="65d31-292">NF-e finantsdokumentide puhul on veerus **Tõrkekood** toodud tagastuskood, mille tagastasid SEFAZ veebiteenused.</span><span class="sxs-lookup"><span data-stu-id="65d31-292">For NF-e fiscal documents, the **Error code** column shows the return code that was returned by SEFAZ web services.</span></span>

### <a name="view-submission-logs-through-the-fiscal-document-page"></a><span data-ttu-id="65d31-293">Edastuslogide kuvamine finantsdokumendi lehe kaudu</span><span class="sxs-lookup"><span data-stu-id="65d31-293">View submission logs through the fiscal document page</span></span>

<span data-ttu-id="65d31-294">Pärast funktsiooni **Konfigureeritav elektroonilise arvelduse lisandmooduli integratsioon** sisse lülitamist saate vaadata edastuslogisid ka finantsdokumendi lehe kaudu.</span><span class="sxs-lookup"><span data-stu-id="65d31-294">After you turn on the **Configurable Electronic invoicing add-on integration** feature, you can also view the submission logs through the fiscal document page.</span></span>

1. <span data-ttu-id="65d31-295">Avage **Pearaamat \> Päringud ja aruanded \> Finantsdokumendid \> Kõik finantsdokumendid**.</span><span class="sxs-lookup"><span data-stu-id="65d31-295">Go to **General ledger \> Inquiries and reports \> Fiscal documents \> All fiscal documents**.</span></span>
2. <span data-ttu-id="65d31-296">Valige finantsdokument, mis esitati varem elektroonilise arvelduse lisandmooduli kaudu.</span><span class="sxs-lookup"><span data-stu-id="65d31-296">Select a fiscal document that was previously submitted through the Electronic invoicing add-on.</span></span>
3. <span data-ttu-id="65d31-297">Valige toimingupaanil vahekaardil **NF-e federal** suvand **Elektroonilise dokumendi logi**.</span><span class="sxs-lookup"><span data-stu-id="65d31-297">On the Action Pane, on the **NF-e federal** tab, select **Electronic document log**.</span></span>

![Edastuslogide kuvamine finantsdokumendi lehel](media/e-Invoicing-services-get-started-BRA-View-Submission-log-from-Fiscal-document-viewer.png)

### <a name="submit-approved-nf-e-fiscal-documents-for-sefaz-cancellation"></a><span data-ttu-id="65d31-299">Kinnitatud NF-e finantsdokumentide edastamine SEFAZ-is tühistamiseks</span><span class="sxs-lookup"><span data-stu-id="65d31-299">Submit approved NF-e fiscal documents for SEFAZ cancellation</span></span>

<span data-ttu-id="65d31-300">Pärast funktsiooni **Konfigureeritav elektroonilise arvelduse lisandmooduli integratsioon** sisse lülitamist ei saa enam vana NF-e finantsdokumentide tühistamise protsessi kasutada.</span><span class="sxs-lookup"><span data-stu-id="65d31-300">After you turn on the **Configurable Electronic invoicing add-on integration** feature, the old process for canceling NF-e fiscal documents can no longer be used.</span></span> <span data-ttu-id="65d31-301">See asendatakse uue tühistamisprotsessiga, mis on manustatud lehel **Elektroonilise dokumendi edastuslogi**.</span><span class="sxs-lookup"><span data-stu-id="65d31-301">It's replaced by a new cancellation process that is embedded on the **Electronic document submission log** page.</span></span>

> [!NOTE]
> <span data-ttu-id="65d31-302">Veenduge, et oleksite käivitanud kinnitatud NF-e finantsdokumendi puhul kliendi finantsdokumendi tühistamise.</span><span class="sxs-lookup"><span data-stu-id="65d31-302">Make sure that you've run the cancellation of the customer fiscal document for an approved NF-e fiscal document.</span></span> <span data-ttu-id="65d31-303">Lisateavet leiate teemast [Kliendi finantsdokumendi tühistamine (Brasiilia)](https://docs.microsoft.com/dynamics365/finance/localizations/latam-bra-cancel-customer-fiscal-documents).</span><span class="sxs-lookup"><span data-stu-id="65d31-303">For more information see, [Cancel customer fiscal document (Brazil)](https://docs.microsoft.com/dynamics365/finance/localizations/latam-bra-cancel-customer-fiscal-documents).</span></span>

1. <span data-ttu-id="65d31-304">Avage **Organisatsiooni haldus \> Perioodiline \> Elektroonilised dokumendid \> Elektroonilise dokumendi edastuslogi**.</span><span class="sxs-lookup"><span data-stu-id="65d31-304">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="65d31-305">Valige finantsdokument ja seejärel **Funktsioonid \> Saada seotud edastused**.</span><span class="sxs-lookup"><span data-stu-id="65d31-305">Select the fiscal document, and then select **Functions \> Send related submissions**.</span></span>
3. <span data-ttu-id="65d31-306">Sisestage seotud edastuse kirjeldus ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="65d31-306">Enter a description for the related submission, and then select **OK**.</span></span>

### <a name="view-cancellation-submission-logs"></a><span data-ttu-id="65d31-307">Tühistamise edastuslogide kuvamine</span><span class="sxs-lookup"><span data-stu-id="65d31-307">View cancellation submission logs</span></span>

1. <span data-ttu-id="65d31-308">Avage **Organisatsiooni haldus \> Perioodiline \> Elektroonilised dokumendid \> Elektroonilise dokumendi edastuslogi**.</span><span class="sxs-lookup"><span data-stu-id="65d31-308">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="65d31-309">Valige väljal **Dokumenditüüp** suvand **Finantsdokumendi päis** , et kuvada ainult finantsdokumendid.</span><span class="sxs-lookup"><span data-stu-id="65d31-309">In the **Document type** field, select **Fiscal document header** to filter for fiscal documents only.</span></span>
3. <span data-ttu-id="65d31-310">Valige finantsdokument ja seejärel valige toimingupaanil **Päringud \> Seotud edastus**.</span><span class="sxs-lookup"><span data-stu-id="65d31-310">Select the fiscal document, and then, on the Action Pane, select **Inquiries \> Related submission**.</span></span>

    <span data-ttu-id="65d31-311">Seotud edastused on edastused, mis on seotud esimesena tehtud põhiedastusega.</span><span class="sxs-lookup"><span data-stu-id="65d31-311">Related submissions are submissions that are related to a main submission that was made first.</span></span> <span data-ttu-id="65d31-312">Näiteks on põhiedastus see edastus, mis autoriseerib kindlat NF-e finantsdokumenti.</span><span class="sxs-lookup"><span data-stu-id="65d31-312">For example, the submission that authorizes a specific NF-e is the main submission.</span></span> <span data-ttu-id="65d31-313">Edastus, mis taotleb sama NF-e tühistamist SEFAZ-is, on seotud edastus.</span><span class="sxs-lookup"><span data-stu-id="65d31-313">The submission that requests the cancellation of the same NF-e in SEFAZ is a related submission.</span></span> <span data-ttu-id="65d31-314">See on olemas ainult seetõttu, et selle kaudu taotletakse teise edastuse kaudu tehtud töö tühistamist.</span><span class="sxs-lookup"><span data-stu-id="65d31-314">It exists only because it's requesting the cancellation of the job that was done through another submission.</span></span>

    <span data-ttu-id="65d31-315">Lehel **Seotud edastused** kuvatakse kõik asjaomase finantsdokumendiga seotud edastused ja nende edastamise olek.</span><span class="sxs-lookup"><span data-stu-id="65d31-315">The **Related submissions** page shows all related submissions, and their submission status, for a given fiscal document.</span></span> <span data-ttu-id="65d31-316">Järgmisel illustratsioonil tähistab esimene rida edastust, mis taotles finantsdokumendi kinnitust.</span><span class="sxs-lookup"><span data-stu-id="65d31-316">In the following illustration, the first line represents the submission that requested approval of the fiscal document.</span></span> <span data-ttu-id="65d31-317">Teine rida tähistab edastust, mis tühistas selle finantsdokumendi.</span><span class="sxs-lookup"><span data-stu-id="65d31-317">The second line represents the submission that canceled that fiscal document.</span></span>

    ![Tühistamise edastuslogide vaatamine](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log.png)

4. <span data-ttu-id="65d31-319">Valige toimingupaanil **Päringud \> Edastuse üksikasjad** , et vaadata edastuse käivituslogide üksikasju.</span><span class="sxs-lookup"><span data-stu-id="65d31-319">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Tühistamise edastuslogi üksikasjade vaatamine](media/e-Invoicing-services-get-started-BRA-View-Cancellation-Submission-log-details.png)

## <a name="privacy-notice"></a><span data-ttu-id="65d31-321">Privaatsusavaldus</span><span class="sxs-lookup"><span data-stu-id="65d31-321">Privacy notice</span></span>
<span data-ttu-id="65d31-322">Funktsiooni BR-00053 (NF-e Federal) lubamise korral on võimalik, et saata tuleb piiratud andmeid, sealhulgas organisatsiooni maksukohustuslasena registreerimise ID.</span><span class="sxs-lookup"><span data-stu-id="65d31-322">Enabling the BR-00053 (NF-e Federal) feature may require sending limited data, which includes the organization tax registration ID.</span></span> <span data-ttu-id="65d31-323">See edastatakse maksuameti volitatud kolmandatest isikutest asutustele, mille eesmärk on saata maksuametile elektroonilisi arveid eelmääratletud vormingus, mis on vajalik integratsiooniks valitsuse veebiteenusega.</span><span class="sxs-lookup"><span data-stu-id="65d31-323">This will be transmitted to third-party agencies authorized by the tax authority for purposes of sending electronic invoices to this tax authority in the predefined format required for integration with the government’s web service.</span></span> <span data-ttu-id="65d31-324">Administraator saab lubada ja keelata funktsiooni BR-00053 (NF-e Federal), avades **Organisatsiooni haldus \> Seadistus \> Elektroonilise dokumendi parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="65d31-324">An administrator can enable and disable the BR-00053 (NF-e Federal) feature by navigating to **Organization administration \> Setup \> Electronic document parameters**.</span></span> <span data-ttu-id="65d31-325">Valige vahekaart **Funktsioonid** , valige rida, mis sisaldab funktsiooni BR-00053, ning seejärel tehke sobiv valik.</span><span class="sxs-lookup"><span data-stu-id="65d31-325">Select the **Features** tab, select the row containing the BR-00053 feature, and then make the appropriate selection.</span></span> <span data-ttu-id="65d31-326">Nendest välissüsteemidest sellesse Dynamics 365 võrguteenusesse imporditud andmete puhul kehtib meie [privaatsusavaldus](https://go.microsoft.com/fwlink/?LinkId=512132).</span><span class="sxs-lookup"><span data-stu-id="65d31-326">Data imported from these external systems into this Dynamics 365 online service are subject to our [privacy statement](https://go.microsoft.com/fwlink/?LinkId=512132).</span></span> <span data-ttu-id="65d31-327">Lisateavet leiate riigipõhise funktsiooni dokumentatsioonis asuvatest privaatsusavalduse jaotistest.</span><span class="sxs-lookup"><span data-stu-id="65d31-327">Please consult the Privacy notice sections in country-specific feature documentation for more information.</span></span>


## <a name="additional-resources"></a><span data-ttu-id="65d31-328">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="65d31-328">Additional resources</span></span>

- [<span data-ttu-id="65d31-329">Elektroonilise arvelduse lisandmooduli ülevaade</span><span class="sxs-lookup"><span data-stu-id="65d31-329">Electronic invoicing add-on overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="65d31-330">Elektroonilise arvelduse lisandmooduli kasutamise alustamine</span><span class="sxs-lookup"><span data-stu-id="65d31-330">Get started with the Electronic invoicing add-on</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="65d31-331">Elektroonilise arvelduse lisandmooduli seadistamine</span><span class="sxs-lookup"><span data-stu-id="65d31-331">Set up the Electronic invoicing add-on</span></span>](e-invoicing-setup.md)
