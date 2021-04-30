---
title: Elektroonilise arvelduse lisandmooduli kasutamise alustamine Itaalias
description: Sellest teemast leiate teabe, mis aitab teil alustada elektroonilise arveldusega Itaalias.
author: gionoder
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 140977a6eac145f35870d3516a4b0d0c794afe4b
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5894773"
---
# <a name="get-started-with-electronic-invoicing-for-italy"></a><span data-ttu-id="e16a0-103">Elektroonilise arvelduse lisandmooduli kasutamise alustamine Itaalias</span><span class="sxs-lookup"><span data-stu-id="e16a0-103">Get started with Electronic invoicing for Italy</span></span>

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> <span data-ttu-id="e16a0-104">Itaalia elektroonilise arvelduse lisandmoodul ei pruugi praegu toetada kõiki elektrooniliste arvete jaoks saadaolevaid funktsioone rakendustes Microsoft Dynamics 365 Finance ja Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e16a0-104">Electronic invoicing for Italy might not currently support all the functions that are available for electronic invoices in Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> 

<span data-ttu-id="e16a0-105">Sellest teemast leiate teabe, mis aitab teil alustada elektroonilise arveldusega Itaalias.</span><span class="sxs-lookup"><span data-stu-id="e16a0-105">This topic provides information that will help you get started with Electronic invoicing for Italy.</span></span> <span data-ttu-id="e16a0-106">Selles antakse juhiseid konfiguratsioonisammude kohta, mis on teenustes Regulatory Configuration Services (RCS) ja rakenduses Finance riigipõhised.</span><span class="sxs-lookup"><span data-stu-id="e16a0-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and Finance.</span></span> <span data-ttu-id="e16a0-107">Samuti antakse juhiseid selle kohta, kuidas edastada teenuse kaudu elektroonilisi arveid, mis on loodud Itaalia-põhises vormingus **FatturaPA**, ja selgitatakse, kuidas töötlemise tulemusi üle vaadata.</span><span class="sxs-lookup"><span data-stu-id="e16a0-107">It also guides you through the process for submitting electronic invoices that are generated in the Italy-specific **FatturaPA** format through the service, and it explains how to review the results of processing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e16a0-108">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="e16a0-108">Prerequisites</span></span>

<span data-ttu-id="e16a0-109">Enne selle teema juhiste täitmist peate järgima teemas [Elektroonilise arvelduse lisandmooduli kasutamise alustamine](e-invoicing-get-started.md) olevaid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="e16a0-109">Before you complete the steps in this topic, you must complete the steps in [Get started with Electronic invoicing](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="e16a0-110">RCS häälestus</span><span class="sxs-lookup"><span data-stu-id="e16a0-110">RCS setup</span></span>

<span data-ttu-id="e16a0-111">RCS-i seadistuse käigus teete järgmist.</span><span class="sxs-lookup"><span data-stu-id="e16a0-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="e16a0-112">E-arvelduse funktsiooni importimine kliendi elektrooniliste arvete eksportimiseks vormingus **FatturaPA**.</span><span class="sxs-lookup"><span data-stu-id="e16a0-112">Import the e-Invoicing feature for the export of customer electronic invoices in the **FatturaPA** format.</span></span>
2. <span data-ttu-id="e16a0-113">Elektrooniliste arvete loomiseks, edastamiseks ja nende vastuste vastu võtmiseks vajalike vormingukonfiguratsioonide ülevaatamine.</span><span class="sxs-lookup"><span data-stu-id="e16a0-113">Review the format configurations that are required to generate, submit, and receive responses about electronic invoices.</span></span>
3. <span data-ttu-id="e16a0-114">Elektroonilise arve edastamise stsenaariume toetavate sündmuste konfigureerimine.</span><span class="sxs-lookup"><span data-stu-id="e16a0-114">Configure the events that support the electronic invoice submission scenarios.</span></span>
4. <span data-ttu-id="e16a0-115">E-arvelduse funktsiooni avaldamine.</span><span class="sxs-lookup"><span data-stu-id="e16a0-115">Publish the e-Invoicing feature.</span></span>

> [!NOTE]
> <span data-ttu-id="e16a0-116">„E-arvelduse funktsioon” on kindla ressursi üldnimi, mis on konfigureeritud ja avaldatud kasutama elektroonilise arvelduse lisandmooduli serverit.</span><span class="sxs-lookup"><span data-stu-id="e16a0-116">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing server.</span></span> <span data-ttu-id="e16a0-117">Praegusel juhul on seadistatavaks e-arvelduse funktsiooniks klientide elektrooniliste arvete eksportimine.</span><span class="sxs-lookup"><span data-stu-id="e16a0-117">In this case, the export of customer electronic invoices is the e-Invoicing feature that you will set up.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="e16a0-118">E-arvelduse funktsiooni importimine</span><span class="sxs-lookup"><span data-stu-id="e16a0-118">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="e16a0-119">Logige oma RCS-i kontole sisse.</span><span class="sxs-lookup"><span data-stu-id="e16a0-119">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="e16a0-120">Valige tööruumis **Globaliseerimisfunktsioonid** jaotises **Funktsioonid** paan **E-arveldus**.</span><span class="sxs-lookup"><span data-stu-id="e16a0-120">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="e16a0-121">Valige lehel **E-arvelduse funktsioonid** suvand **Impordi**, et importida globaalsest hoidlast e-arvelduse funktsioon.</span><span class="sxs-lookup"><span data-stu-id="e16a0-121">On the **e-Invoicing Features** page, select **Import** to import the e-Invoicing feature from the Global repository.</span></span>

    > [!NOTE]
    > <span data-ttu-id="e16a0-122">Kui te ei näe saadaolevate funktsioonide loendit, valige **Sünkrooni**.</span><span class="sxs-lookup"><span data-stu-id="e16a0-122">If you don't see the list of available features, select **Synchronize**.</span></span> 

4. <span data-ttu-id="e16a0-123">Valige funktsioon **E-arvete eksportimine (IT)** ja seejärel valige **Impordi**.</span><span class="sxs-lookup"><span data-stu-id="e16a0-123">Select the **e-Invoices Export (IT)** feature, and then select **Import**.</span></span>

![E-arvete eksportimise (IT) funktsiooni importimine](media/e-Invoicing-services-get-started-ITA-Select-Import-e-Invoicing-feature.png)

<span data-ttu-id="e16a0-125">Funktsiooni **E-arvete eksportimine (IT)** importimisel globaalsest hoidlast, imporditakse ka kõik järgmistes jaotistes kirjeldatud sätted.</span><span class="sxs-lookup"><span data-stu-id="e16a0-125">When you import the **e-Invoices Export (IT)** feature from the Global repository, all the settings that are described in the next sections are also imported.</span></span>

## <a name="create-a-new-version-of-the-e-invoices-export-it-feature"></a><span data-ttu-id="e16a0-126">E-arvete eksportimise (IT) funktsiooni uue versiooni loomine</span><span class="sxs-lookup"><span data-stu-id="e16a0-126">Create a new version of the e-Invoices Export (IT) feature</span></span>

1. <span data-ttu-id="e16a0-127">Valige lehel **E-arvelduse funktsioonid** vahekaardil **Versioonid** suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e16a0-127">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span> 

    ![E-arvelduse funktsiooni uue versiooni lisamine](media/e-Invoicing-services-get-started-ITA-Select-New-e-Invoicing-feature-version.png)

    <span data-ttu-id="e16a0-129">Järgmisena konfigureerite elektroonilise aruandluse (ER) vormingud, mis on e-arvelduse funktsiooniga seotud.</span><span class="sxs-lookup"><span data-stu-id="e16a0-129">Next, you will configure the Electronic reporting (ER) formats that are associated with the e-Invoicing feature.</span></span>

2. <span data-ttu-id="e16a0-130">Valige vahekaardil **Konfiguratsioonid** suvand **Lisa**, et hallata konfiguratsiooni versioone.</span><span class="sxs-lookup"><span data-stu-id="e16a0-130">On the **Configurations** tab, select **Add** to manage the configuration versions.</span></span>

    ![E-arvelduse funktsiooni konfiguratsiooni versioonide haldamine](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-configurations.png)

    <span data-ttu-id="e16a0-132">Selles sammus lisate ja konfigureerite ER-i vormingud eri failide jaoks, mida kasutatakse Itaalia e-arvete eksportimiseks.</span><span class="sxs-lookup"><span data-stu-id="e16a0-132">In this step, you're adding and configuring the ER formats of different files that are used to export Italian e-invoices.</span></span> <span data-ttu-id="e16a0-133">Itaalia FatturaPA e-arvete puhul kasutage järgmisi standardseid konfiguratsioone või tegelikke e-arvelduse jaoks kasutatavaid kohandatud konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="e16a0-133">For Italian FatturaPA e-invoices, use either the following standard configurations or the actual customized configurations that you use for e-invoicing:</span></span>

    - <span data-ttu-id="e16a0-134">Müügiarve (IT)</span><span class="sxs-lookup"><span data-stu-id="e16a0-134">Sales invoice (IT)</span></span>
    - <span data-ttu-id="e16a0-135">Projektiarve (IT)</span><span class="sxs-lookup"><span data-stu-id="e16a0-135">Project invoice (IT)</span></span>

    <span data-ttu-id="e16a0-136">Kui loote e-arvelduse funktsiooni, mis on tuletatud mõnest muust e-arvelduse funktsioonist, päritakse kõik ER-i vormingud algsest funktsioonist.</span><span class="sxs-lookup"><span data-stu-id="e16a0-136">When you create an e-Invoicing feature that is derived from another e-Invoicing feature, all ER formats are inherited from the original feature.</span></span>

3. <span data-ttu-id="e16a0-137">Valige konkreetne ER-i vormingu failikonfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="e16a0-137">Select a specific ER format file configuration.</span></span>
4. <span data-ttu-id="e16a0-138">Valige **Redigeeri** või **Kuva**, et avada leht **Vormingukujundaja**.</span><span class="sxs-lookup"><span data-stu-id="e16a0-138">Select **Edit** or **View** to open the **Format designer** page.</span></span>

    ![Vormingukujundaja lehe avamine](media/e-Invoicing-services-get-started-ITA-Configuration-ER-format-designer.png)

5. <span data-ttu-id="e16a0-140">Kasutage ER-i vormingu failikonfiguratsioonide redigeerimiseks ja kuvamiseks lehte **Vormingukujundaja**.</span><span class="sxs-lookup"><span data-stu-id="e16a0-140">Use the **Format designer** page to edit and view the ER format file configurations.</span></span>

    ![Vormingukujundaja leht](media/e-Invoicing-services-get-started-ITA-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="e16a0-142">E-arvelduse funktsiooni seadistuste haldamine</span><span class="sxs-lookup"><span data-stu-id="e16a0-142">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="e16a0-143">Valige lehel **E-arvelduse funktsioonid** vahekaardil **Seadistused** suvand **Lisa**, **Kustuta** või **Redigeeri**, et hallata e-arvelduse funktsiooni seadistusi.</span><span class="sxs-lookup"><span data-stu-id="e16a0-143">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add**, **Delete**, or **Edit** to manage the e-Invoicing feature setups.</span></span>

![E-arvelduse funktsiooni seadistuste haldamine](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-setup.png)

<span data-ttu-id="e16a0-145">Selles sammus konfigureerite sündmused, mida rakendatakse elektrooniliste arvete puhul, sh XML-väljundfailide loomine vormingus **FatturaPA** ja digitaalne allkirjastamine (kui see on vajalik).</span><span class="sxs-lookup"><span data-stu-id="e16a0-145">In this step, you configure the events that are applicable to electronic invoices, including generation of the XML output files in **FatturaPA** format and digital signing (if required).</span></span>

### <a name="configure-the-sales-invoice-feature-setup"></a><span data-ttu-id="e16a0-146">Müügiarve funktsiooni seadistuse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="e16a0-146">Configure the Sales invoice feature setup</span></span>

1. <span data-ttu-id="e16a0-147">Valige lehe **E-arvelduse funktsioonid** vahekaardi **Seadistused** veerus **Funktsiooni seadistus** suvand **Müügiarve**.</span><span class="sxs-lookup"><span data-stu-id="e16a0-147">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Sales invoice**.</span></span>
2. <span data-ttu-id="e16a0-148">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="e16a0-148">Select **Edit**.</span></span>
3. <span data-ttu-id="e16a0-149">Valige lehel **Funktsiooni versiooni seadistus** vahekaart **Tegevused**, et hallata tegevuste loendit.</span><span class="sxs-lookup"><span data-stu-id="e16a0-149">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span> <span data-ttu-id="e16a0-150">Tegevused määratlevad selliste toimingute loendi, mis tuleb käitada sündmuse täielikuks lõpetamiseks järjestikku.</span><span class="sxs-lookup"><span data-stu-id="e16a0-150">Actions define a list of operations that must be run in sequential order to accomplish full execution of the event.</span></span>

    ![Tegevuste vahekaart](media/e-Invoicing-services-get-started-ITA-Select-Actions.png)

    | <span data-ttu-id="e16a0-152">Tegevuse ID</span><span class="sxs-lookup"><span data-stu-id="e16a0-152">Action ID</span></span> | <span data-ttu-id="e16a0-153">Tegevuse nimi</span><span class="sxs-lookup"><span data-stu-id="e16a0-153">Action name</span></span>        | <span data-ttu-id="e16a0-154">Tegevuse kirjeldus</span><span class="sxs-lookup"><span data-stu-id="e16a0-154">Action description</span></span>                                     |
    |-----------|--------------------|--------------------------------------------------------|
    | <span data-ttu-id="e16a0-155">1</span><span class="sxs-lookup"><span data-stu-id="e16a0-155">1</span></span>         | <span data-ttu-id="e16a0-156">Teisenda dokument</span><span class="sxs-lookup"><span data-stu-id="e16a0-156">Transform document</span></span> | <span data-ttu-id="e16a0-157">E-arve XML-faili loomine vormingus **FatturaPA**.</span><span class="sxs-lookup"><span data-stu-id="e16a0-157">Create the e-invoice XML file in **FatturaPA** format.</span></span> |
    | <span data-ttu-id="e16a0-158">2</span><span class="sxs-lookup"><span data-stu-id="e16a0-158">2</span></span>         | <span data-ttu-id="e16a0-159">Allkirjasta dokument</span><span class="sxs-lookup"><span data-stu-id="e16a0-159">Sign document</span></span>      | <span data-ttu-id="e16a0-160">Digitaalallkirja lisamine XML-failile.</span><span class="sxs-lookup"><span data-stu-id="e16a0-160">Apply a digital signature to the XML file.</span></span>             |

4. <span data-ttu-id="e16a0-161">Valige vahekaart **Rakendatavuse reeglid**, et vaadata ja hallata rakendatavuse reegleid.</span><span class="sxs-lookup"><span data-stu-id="e16a0-161">Select the **Applicability rules** tab to view and maintain the applicability rules.</span></span> <span data-ttu-id="e16a0-162">Rakendatavuse reeglid määratlevad konteksti, mille puhul tegevus käivitatakse.</span><span class="sxs-lookup"><span data-stu-id="e16a0-162">Applicability rules define the context where the action will be run.</span></span>

    ![Rakendatavuse reeglite vahekaart](media/e-Invoicing-services-get-started-ITA-Select-Applicability-rules.png)

5. <span data-ttu-id="e16a0-164">Valige vahekaart **Muutujad**, et vaadata ja hallata muutujaid.</span><span class="sxs-lookup"><span data-stu-id="e16a0-164">Select the **Variables** tab to view and maintain the variables.</span></span>

    ![Muutujate vahekaart](media/e-Invoicing-services-get-started-ITA-Select-Variables.png)

6. <span data-ttu-id="e16a0-166">Määratlege avalikud muutujad, mis on vajalikud tegevuste käivitamiseks.</span><span class="sxs-lookup"><span data-stu-id="e16a0-166">Define the public variables that are required to run the actions.</span></span>

### <a name="configure-the-project-invoice-feature-setup"></a><span data-ttu-id="e16a0-167">Projektiarve funktsiooni seadistuse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="e16a0-167">Configure the Project invoice feature setup</span></span> 

<span data-ttu-id="e16a0-168">Funktsiooni **Projektiarve** seadistuse konfigureerimiseks vajalikud juhised ja sätted on väga sarnased funktsiooni **Müügiarve** seadistuse juhiste ning sätetega.</span><span class="sxs-lookup"><span data-stu-id="e16a0-168">The steps and settings that are required to configure the **Project invoice** feature setup are very similar to the steps and settings for the **Sales invoice** feature setup.</span></span> <span data-ttu-id="e16a0-169">Projektiarvetega töötamise korral vaadake juhiseid müügiarvete kohta.</span><span class="sxs-lookup"><span data-stu-id="e16a0-169">When you work with project invoices, see the procedures for sales invoices.</span></span>

## <a name="assign-the-e-invoicing-feature-to-the-environment"></a><span data-ttu-id="e16a0-170">E-arvelduse funktsiooni määramine keskkonnale</span><span class="sxs-lookup"><span data-stu-id="e16a0-170">Assign the e-Invoicing feature to the environment</span></span>

1. <span data-ttu-id="e16a0-171">Valige lehel **E-arvelduse funktsioonid** vahekaardil **Keskkonnad** suvand **Luba**.</span><span class="sxs-lookup"><span data-stu-id="e16a0-171">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="e16a0-172">Valige keskkond väljal **Keskkond**.</span><span class="sxs-lookup"><span data-stu-id="e16a0-172">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="e16a0-173">Valige väljal **Kehtiv alates** kuupäev, mil uus keskkond peaks kehtima hakkama.</span><span class="sxs-lookup"><span data-stu-id="e16a0-173">In the **Effective from** field, select the date when the environment should become effective.</span></span>
4. <span data-ttu-id="e16a0-174">Valige **Luba**.</span><span class="sxs-lookup"><span data-stu-id="e16a0-174">Select **Enable**.</span></span> 

![E-arvelduse keskkonna lubamine](media/e-Invoicing-services-get-started-ITA-Enable-e-Invoicing-environment.png)

## <a name="publish-the-e-invoicing-feature"></a><span data-ttu-id="e16a0-176">E-arvelduse funktsiooni avaldamine</span><span class="sxs-lookup"><span data-stu-id="e16a0-176">Publish the e-invoicing feature</span></span>

<span data-ttu-id="e16a0-177">Saate avaldada e-arvelduse funktsiooni, muutes versiooni olekuks väärtuse **Lõpetatud** või **Avaldatud**.</span><span class="sxs-lookup"><span data-stu-id="e16a0-177">You can publish the e-Invoicing feature by changing the version status to **Completed** or **Published**.</span></span>

### <a name="change-the-version-status-to-completed"></a><span data-ttu-id="e16a0-178">Versiooni oleku muutmine lõpetatuks</span><span class="sxs-lookup"><span data-stu-id="e16a0-178">Change the version status to Completed</span></span>

1. <span data-ttu-id="e16a0-179">Valige lehel **E-arvelduse funktsioonid** vahekaardil **Versioonid** e-arvelduse funktsiooni versioon, mille olek on **Mustand**.</span><span class="sxs-lookup"><span data-stu-id="e16a0-179">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="e16a0-180">Valige **Muuda olekut \> Lõpule viidud**.</span><span class="sxs-lookup"><span data-stu-id="e16a0-180">Select **Change status \> Complete**.</span></span> 

### <a name="change-the-version-status-to-published"></a><span data-ttu-id="e16a0-181">Versiooni oleku muutmine avaldatuks</span><span class="sxs-lookup"><span data-stu-id="e16a0-181">Change the version status to Published</span></span> 

1. <span data-ttu-id="e16a0-182">Valige lehel **E-arvelduse funktsioonid** vahekaardil **Versioonid** e-arvelduse funktsiooni versioon, mille olek on **Lõpetatud**.</span><span class="sxs-lookup"><span data-stu-id="e16a0-182">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Completed**.</span></span>
2. <span data-ttu-id="e16a0-183">Valige **Muuda olekut \> Avalda**.</span><span class="sxs-lookup"><span data-stu-id="e16a0-183">Select **Change status \> Publish**.</span></span>

![E-arvelduse funktsiooni oleku muutmine](media/e-Invoicing-services-get-started-ITA-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-electronic-invoicing-integration-in-finance"></a><span data-ttu-id="e16a0-185">Seadista Elektroonilise arveldamise integratsioon Finantsis</span><span class="sxs-lookup"><span data-stu-id="e16a0-185">Set up Electronic invoicing integration in Finance</span></span>

<span data-ttu-id="e16a0-186">Rakenduse Finance seadistuse käigus teete järgmist.</span><span class="sxs-lookup"><span data-stu-id="e16a0-186">During the setup of Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="e16a0-187">ER-i andmemudeli, ER-i andmemudeli vastenduse ja FatturaPA e-arvete kontekstikonfiguratsioonide importimine.</span><span class="sxs-lookup"><span data-stu-id="e16a0-187">Import the ER data model, the ER data model mapping, and the context configurations for FatturaPA e-invoices.</span></span>
2. <span data-ttu-id="e16a0-188">Serdi konfigureerimine, mis on vajalik Itaalia e-arvete digitaalseks allkirjastamiseks.</span><span class="sxs-lookup"><span data-stu-id="e16a0-188">Configure the certificate that is required to digitally sign Italian e-invoices.</span></span>

### <a name="import-the-er-data-model-data-model-mapping-and-formats"></a><span data-ttu-id="e16a0-189">ER-i andmemudeli, andmemudeli vastenduse ja vormingute importimine</span><span class="sxs-lookup"><span data-stu-id="e16a0-189">Import the ER data model, data model mapping, and formats</span></span>

1. <span data-ttu-id="e16a0-190">Veenduge, et tööruumis **Elektrooniline aruandlus** oleks konfiguratsioonipakkuja **Äridokumendi teenus** väärtuseks määratud **Aktiivne**.</span><span class="sxs-lookup"><span data-stu-id="e16a0-190">In the **Electronic reporting** workspace, verify that the **Business Document Service** configuration provider is set to **Active**.</span></span>
2. <span data-ttu-id="e16a0-191">Valige **Hoidlad**.</span><span class="sxs-lookup"><span data-stu-id="e16a0-191">Select **Repositories**.</span></span>
3. <span data-ttu-id="e16a0-192">Valige **Globaalne ressurss \> Ava**.</span><span class="sxs-lookup"><span data-stu-id="e16a0-192">Select **Global resource \> Open**.</span></span>
4. <span data-ttu-id="e16a0-193">Importige **Arvemudel**, **Arvemudeli vastendus** ja **Kliendiarve kontekstimudel**.</span><span class="sxs-lookup"><span data-stu-id="e16a0-193">Import **Invoice model**, **Invoice model mapping**, and **Customer invoice context model**.</span></span>

#### <a name="turn-on-the-feature-for-exporting-customer-electronic-invoices-for-italy"></a><span data-ttu-id="e16a0-194">Itaalia elektrooniliste arvete eksportimise funktsiooni sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="e16a0-194">Turn on the feature for exporting customer electronic invoices for Italy</span></span>

1. <span data-ttu-id="e16a0-195">Avage **Organisatsiooni haldus \> Seadistus \> Elektroonilise dokumendi parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="e16a0-195">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="e16a0-196">Märkige vahekaardil **Funktsioonid** märkeruut **Lubatud** funktsiooniviite **IT00036** rea puhul.</span><span class="sxs-lookup"><span data-stu-id="e16a0-196">On the **Features** tab, select the **Enabled** check box in the row for feature reference **IT00036**.</span></span>

![FatturaPA funktsiooni sisselülitamine](media/e-Invoicing-services-get-started-ITA-Enable-FatturaPA-feature.png)

#### <a name="configure-electronic-documents"></a><span data-ttu-id="e16a0-198">Elektrooniliste dokumentide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="e16a0-198">Configure electronic documents</span></span>

1. <span data-ttu-id="e16a0-199">Avage **Organisatsiooni haldus \> Seadistus \> Elektroonilise dokumendi parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="e16a0-199">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="e16a0-200">Valige vahekaardil **Elektrooniline dokument** suvand **Lisa** ja sisestage tabelid, mis on vajalikud Itaalia e-arvete loomiseks.</span><span class="sxs-lookup"><span data-stu-id="e16a0-200">On the **Electronic document** tab, select **Add**, and enter the tables that are required to generate Italian e-invoices:</span></span>

    - <span data-ttu-id="e16a0-201">**Tabeli nimi:** kliendiarve tööleht</span><span class="sxs-lookup"><span data-stu-id="e16a0-201">**Table name:** Customer invoice journal</span></span>
    - <span data-ttu-id="e16a0-202">**Tabeli nimi:** projektiarve</span><span class="sxs-lookup"><span data-stu-id="e16a0-202">**Table name:** Project invoice</span></span>

3. <span data-ttu-id="e16a0-203">Määratlege iga tabeli puhul seotud dokumendi kontekst.</span><span class="sxs-lookup"><span data-stu-id="e16a0-203">For each table, define a related document context:</span></span>

    - <span data-ttu-id="e16a0-204">Valige suvandi **Kliendiarve tööleht** puhul **Kliendiarve kontekst**.</span><span class="sxs-lookup"><span data-stu-id="e16a0-204">For **Customer invoice journal**, select **Customer invoice context**.</span></span>
    - <span data-ttu-id="e16a0-205">Valige suvandi **Projektiarve** puhul **Projektiarve kontekst**.</span><span class="sxs-lookup"><span data-stu-id="e16a0-205">For **Project invoice**, select **Project invoice context**.</span></span>

![Vastusetüüpide seadistamine](media/e-Invoicing-services-get-started-ITA-Set-up-response-types.png)

## <a name="electronic-invoice-processing"></a><span data-ttu-id="e16a0-207">Elektroonilise arve töötlemine</span><span class="sxs-lookup"><span data-stu-id="e16a0-207">Electronic invoice processing</span></span>

<span data-ttu-id="e16a0-208">Rakenduses Finance teete töötlemise käigus järgmist.</span><span class="sxs-lookup"><span data-stu-id="e16a0-208">During processing in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="e16a0-209">Itaalia e-arvete loomine elektroonilise arvelduse lisandmooduli kaudu</span><span class="sxs-lookup"><span data-stu-id="e16a0-209">Generate Italian e-invoices through Electronic invoicing</span></span>
2. <span data-ttu-id="e16a0-210">Käivituslogide vaatamine ja töötlemise tulemuste ülevaatamine</span><span class="sxs-lookup"><span data-stu-id="e16a0-210">View the execution logs and review the results of processing</span></span>

### <a name="generate-electronic-invoices"></a><span data-ttu-id="e16a0-211">Elektrooniliste arvete loomine</span><span class="sxs-lookup"><span data-stu-id="e16a0-211">Generate electronic invoices</span></span>

<span data-ttu-id="e16a0-212">Pärast funktsiooni **Konfigureeritav elektroonilise arvelduse lisandmooduli integratsioon** sisse lülitamist ja funktsiooni **IT00036** aktiveerimist ei saa enam Itaalia e-arvete loomiseks kasutada rakenduse Finance vana protsessi.</span><span class="sxs-lookup"><span data-stu-id="e16a0-212">After you turn on the **Configurable Electronic invoicing integration** feature and activate the **IT00036** feature, the old Finance process for generating Italian e-invoices can no longer be used.</span></span> <span data-ttu-id="e16a0-213">See asendatakse uue protsessiga **Edasta elektroonilised dokumendid**.</span><span class="sxs-lookup"><span data-stu-id="e16a0-213">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

<span data-ttu-id="e16a0-214">Dokumente saate edastada käsitsi sõltuvalt nõudlusest e-arve dokumentide järele.</span><span class="sxs-lookup"><span data-stu-id="e16a0-214">You can submit the documents manually, based on your demand for e-invoice documents.</span></span>

> [!NOTE]
> <span data-ttu-id="e16a0-215">Enne jätkamist veenduge, et Itaalia e-arvete jaoks vajalik seadistus oleks lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="e16a0-215">Before you continue, verify that the setup that is required for Italian e-invoices was completed.</span></span> <span data-ttu-id="e16a0-216">Lisateavet leiate teemast [Kliendi elektroonilised arved](./emea-ita-e-invoices.md).</span><span class="sxs-lookup"><span data-stu-id="e16a0-216">For more information, see [Customer electronic invoices](./emea-ita-e-invoices.md).</span></span> <span data-ttu-id="e16a0-217">Pange tähele, et mõni selles teemas kirjeldatud seadistusetapp ei pruugi olla elektroonilise arvelduse lisandmooduli aktiveerimise tõttu saadaval.</span><span class="sxs-lookup"><span data-stu-id="e16a0-217">Be aware that some of the setup steps that are described in that topic might be unavailable because of Electronic invoicing activation.</span></span>

1. <span data-ttu-id="e16a0-218">Avage **Organisatsiooni haldus \> Perioodiline \> Elektroonilised dokumendid \> Edasta elektroonilised dokumendid**.</span><span class="sxs-lookup"><span data-stu-id="e16a0-218">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="e16a0-219">Mis tahes dokumendi esimese edastamise korral seadke suvandi **Dokumentide taasedastamine** väärtuseks **Ei**.</span><span class="sxs-lookup"><span data-stu-id="e16a0-219">For the first submission of any document, set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="e16a0-220">Kui peate dokumendi teenuse kaudu uuesti edastama, seadke selle suvandi väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="e16a0-220">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="e16a0-221">Valige kiirkaardil **Kaasatavad kirjed** suvand **Filter**, et avada dialoogiboks **Päring**, kus saate luua päringu edastatavate dokumentide valimiseks.</span><span class="sxs-lookup"><span data-stu-id="e16a0-221">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>

![Elektrooniliste dokumentide edastamise dialoogiboks](media/e-Invoicing-services-get-started-ITA-Submission-form.png)

#### <a name="filter-query"></a><span data-ttu-id="e16a0-223">Filtri päring</span><span class="sxs-lookup"><span data-stu-id="e16a0-223">Filter query</span></span>

1. <span data-ttu-id="e16a0-224">Konfigureerige dialoogiboksis **Päring** filtreerimistingimused nii müügi- kui ka projektiarvete jaoks või jätke tingimused tühjaks, et kaasata kõik edastamata arved.</span><span class="sxs-lookup"><span data-stu-id="e16a0-224">In the **Inquiry** dialog box, configure the filtering conditions for both sales invoices and project invoices, or leave the conditions blank to include all unsubmitted invoices.</span></span>

    ![Edastamise filtreerimiskriteeriumide seadistamine](media/e-Invoicing-services-get-started-ITA-Set-up-Submission-filter-criteria.png)

2. <span data-ttu-id="e16a0-226">Valige dialoogiboksi **Päring** sulgemiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="e16a0-226">Select **OK** to close the **Inquiry** dialog box.</span></span>
3. <span data-ttu-id="e16a0-227">Valige **OK**, et edastada valitud dokumendid.</span><span class="sxs-lookup"><span data-stu-id="e16a0-227">Select **OK** submit the selected documents.</span></span>

> <span data-ttu-id="e16a0-228">![MÄRKUS] Esimesel dokumendi edastamise katsel teenuse kaudu palutakse teil kinnitada ühendus elektroonilise arvelduse lisandmooduliga.</span><span class="sxs-lookup"><span data-stu-id="e16a0-228">![NOTE] During your first attempt to submit a document through the service, you will be prompted to confirm the connection with Electronic invoicing.</span></span> <span data-ttu-id="e16a0-229">Valige **Elektroonilise dokumendi edastusteenusega ühendumiseks klõpsake siin**.</span><span class="sxs-lookup"><span data-stu-id="e16a0-229">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

#### <a name="view-submission-logs"></a><span data-ttu-id="e16a0-230">Edastuslogide kuvamine</span><span class="sxs-lookup"><span data-stu-id="e16a0-230">View submission logs</span></span>

<span data-ttu-id="e16a0-231">Saate vaadata kõigi edastatud dokumentide edastuslogisid.</span><span class="sxs-lookup"><span data-stu-id="e16a0-231">You can view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="e16a0-232">Avage **Organisatsiooni haldus \> Perioodiline \> Elektroonilised dokumendid \> Elektroonilise dokumendi edastuslogi**.</span><span class="sxs-lookup"><span data-stu-id="e16a0-232">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="e16a0-233">Valige väljal **Dokumenditüüp** suvand **Kliendiarve tööleht** või **Projektiarve**, et kuvada vajalikud elektroonilised dokumendid.</span><span class="sxs-lookup"><span data-stu-id="e16a0-233">In the **Document type** field, select **Customer invoice journal** or **Project invoice** to filter for the required electronic documents.</span></span>

    ![Dokumendi tüübi valimine edastuslogide kuvamiseks](media/e-Invoicing-services-get-started-ITA-Select-Document-type-for-viewing-submission-log.png)

    <span data-ttu-id="e16a0-235">Veerus **Edastuse olek** toodud väärtus tähistab edastusprotsessi olekut.</span><span class="sxs-lookup"><span data-stu-id="e16a0-235">The value that is shown in the **Submission status** column represents the status of the submission process.</span></span> <span data-ttu-id="e16a0-236">See näitab, kas protsess käitati nagu konfigureeritud ja kas vajalik on täiendav tegevus.</span><span class="sxs-lookup"><span data-stu-id="e16a0-236">It indicates whether the process ran as configured and whether additional action is required.</span></span>

3. <span data-ttu-id="e16a0-237">Valige toimingupaanil **Päringud \> Edastuse üksikasjad**, et vaadata edastuse käivituslogide üksikasju.</span><span class="sxs-lookup"><span data-stu-id="e16a0-237">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Edastuslogi üksikasjade vaatamine](media/e-Invoicing-services-get-started-ITA-View-Submission-log-details.png)

4. <span data-ttu-id="e16a0-239">Kiirkaardil **Töötlemistegevused** saate vaadata RCS-is seadistatud funktsiooni versioonis konfigureeritud tegevuste käivituslogi.</span><span class="sxs-lookup"><span data-stu-id="e16a0-239">On the **Processing actions** FastTab, you can view the execution log for the actions that are configured in the feature version that was set up in RCS.</span></span> <span data-ttu-id="e16a0-240">Veerus **Olek** on näha, kas tegevuse käivitamine õnnestus.</span><span class="sxs-lookup"><span data-stu-id="e16a0-240">The **Status** column shows whether the action was successfully run.</span></span>
5. <span data-ttu-id="e16a0-241">Kiirkaardil **Tegevusfailid** saate vaadata vahefaile, mis loodi tegevuste käivitamise ajal.</span><span class="sxs-lookup"><span data-stu-id="e16a0-241">On the **Action files** FastTab, you can view the intermediate files that were generated during execution of the actions.</span></span> <span data-ttu-id="e16a0-242">Saate valida **Kuva**, et laadida alla XML-väljundfail vormingus **FatturaPA** ja vaadata selle sisu.</span><span class="sxs-lookup"><span data-stu-id="e16a0-242">You can select **View** to download the output XML file in **FatturaPA** format and view its content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e16a0-243">Seotud dokumendid</span><span class="sxs-lookup"><span data-stu-id="e16a0-243">Related topics</span></span>

- [<span data-ttu-id="e16a0-244">Elektroonilise arvelduse ülevaade</span><span class="sxs-lookup"><span data-stu-id="e16a0-244">Electronic invoicing overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="e16a0-245">Elektroonilise arveldusega alustamine</span><span class="sxs-lookup"><span data-stu-id="e16a0-245">Get started with Electronic invoicing</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="e16a0-246">Seadista elektrooniline häälestus</span><span class="sxs-lookup"><span data-stu-id="e16a0-246">Set up Electronic invoicing</span></span>](e-invoicing-setup.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]