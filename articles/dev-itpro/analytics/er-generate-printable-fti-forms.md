---
title: Prinditavate FTI-vormide loomine
description: "Teemas selgitatakse, kuidas kasutada elektroonilise aruandluse (ER) raamistikku, et luua prinditavaid vabas vormis arvete (FTI) vorme Microsoft Office’i dokumentidena."
author: NickSelin
manager: AnnBe
ms.date: 07/24/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: d27a11a0d925b0f1164578f9c04e6abd4736b2b2
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---

# <a name="generate-printable-fti-forms"></a><span data-ttu-id="6def6-103">Prinditavate FTI-vormide loomine</span><span class="sxs-lookup"><span data-stu-id="6def6-103">Generate printable FTI forms</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6def6-104">Elektroonilise aruandluse (ER) raamistik võimaldab teil luua prinditavaid vabas vormis arvete (FTI) vorme Microsoft Office’i dokumentidena.</span><span class="sxs-lookup"><span data-stu-id="6def6-104">The Electronic reporting (ER) framework lets you generate printable free text invoice (FTI) forms as Microsoft Office documents.</span></span> <span data-ttu-id="6def6-105">Teema annab teavet selle kohta, kuidas luua oma konfiguratsioone, ja üksikasjaliku ülevaate saadavaolevate konfiguratsioonimallide kohta.</span><span class="sxs-lookup"><span data-stu-id="6def6-105">This topic provides information about how to build your own configurations as well as details of available configuration templates.</span></span>

## <a name="overview"></a><span data-ttu-id="6def6-106">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="6def6-106">Overview</span></span>

<span data-ttu-id="6def6-107">Peale olemasoleva võimaluse luua Microsofti SQL Serveri aruandlusteenustega (SSRS) prinditavaid FTI-vorme, saate nüüd selleks kasutada ka ER-i raamistikku.</span><span class="sxs-lookup"><span data-stu-id="6def6-107">In addition to the existing capability of generating printable FTI forms by using Microsoft SQL Server Reporting Services (SSRS), you can now use the ER framework.</span></span> <span data-ttu-id="6def6-108">Saate hallata prinditavaid FTI-vorme Microsoft Office Excelis ja Wordis.</span><span class="sxs-lookup"><span data-stu-id="6def6-108">You can manage printable FTI forms in Microsoft Office Excel and Word.</span></span> <span data-ttu-id="6def6-109">Samuti saate konkreetsete nõuete täitmiseks muuta paigutust, andmevoogu ja vormingut ilma, et peaks tegema muudatusi koodis.</span><span class="sxs-lookup"><span data-stu-id="6def6-109">You can also modify the layout, data flow, and formatting to meet specific requirements without making code changes.</span></span>

> [!NOTE]
> <span data-ttu-id="6def6-110">Kui soovite alustuseks näha ülevaadet olemasolevatest ER-i konfiguratsioonidest selle prinditavate FTI-vormide lahenduse näite jaoks, võite kohe liikuda selle teema jaotisesse **ER-i näidiskonfiguratsioonide allalaadimine, et luua prinditavaid FTI-vorme**.</span><span class="sxs-lookup"><span data-stu-id="6def6-110">If you want to start with an overview of existing ER configurations for this sample of the printable FTI forms solution, you can go directly to section **Download sample ER configurations to generate printable FTI forms** later in this topic.</span></span>

## <a name="create-customized-configurations-for-fti-printable-forms"></a><span data-ttu-id="6def6-111">Prinditavate FTI-vormide jaoks kohandatud konfiguratsioonide loomine</span><span class="sxs-lookup"><span data-stu-id="6def6-111">Create customized configurations for FTI printable forms</span></span>
<span data-ttu-id="6def6-112">Prinditavate FTI-vormide kohandatud lahenduse osana peate looma ER-i konfiguratsioonide kogumi.</span><span class="sxs-lookup"><span data-stu-id="6def6-112">As part of your customized solution for printable FTI forms, you must create a set of ER configurations.</span></span>

### <a name="configure-the-er-data-model"></a><span data-ttu-id="6def6-113">Elektroonilise aruandluse andmemudeli konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="6def6-113">Configure the ER data model</span></span>
<span data-ttu-id="6def6-114">Teie rakenduses peab olema ER-i andmemudeli konfiguratsioon, mis sisaldab andmemudelit, mis kirjeldab kliendi arveldamise ettevõttedomeeni.</span><span class="sxs-lookup"><span data-stu-id="6def6-114">Your application must include the ER data model configuration that contains a data model that describes the customer invoicing business domain.</span></span> <span data-ttu-id="6def6-115">Selle andmemudeli nimi peab olema **CustomersInvoicing**.</span><span class="sxs-lookup"><span data-stu-id="6def6-115">As a requirement, the name of the data model must be **CustomersInvoicing**.</span></span> <span data-ttu-id="6def6-116">Teavet ER-i andmemudelite kujundamise kohta leiate teemast [Elektroonilise aruandluse (ER) domeenikohase andmemudeli koostamine](tasks/er-design-domain-specific-data-model-2016-11.md)</span><span class="sxs-lookup"><span data-stu-id="6def6-116">For information about how to design ER data models, see [Design a domain-specific data model for electronic reporting (ER)](tasks/er-design-domain-specific-data-model-2016-11.md).</span></span>

### <a name="configure-the-er-model-mapping"></a><span data-ttu-id="6def6-117">Elektroonilise aruandluse mudelivastenduse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="6def6-117">Configure the ER model mapping</span></span>
<span data-ttu-id="6def6-118">Teie rakenduses peab olema andmemudeli CustomersInvoicing jaoks ER-i mudelivastendus.</span><span class="sxs-lookup"><span data-stu-id="6def6-118">Your application must include the ER model mapping for the CustomersInvoicing data model.</span></span> <span data-ttu-id="6def6-119">Mudelivastendus võib olla kas ER-i andmemudeli konfiguratsioonis või ER-i mudelivastenduse konfiguratsioonis.</span><span class="sxs-lookup"><span data-stu-id="6def6-119">The model mapping can be in either the ER data model configuration or the ER model mapping configuration.</span></span> <span data-ttu-id="6def6-120">Mudelivastenduse juurdeskriptori nimi peab aga olema **FreeTextInvoice**.</span><span class="sxs-lookup"><span data-stu-id="6def6-120">However, the name of the root descriptor of the model mapping must be **FreeTextInvoice**.</span></span>

<span data-ttu-id="6def6-121">Vastendamine peab sisaldama järgmisi andmeallikaid.</span><span class="sxs-lookup"><span data-stu-id="6def6-121">The mapping must contain the following data sources:</span></span>

- <span data-ttu-id="6def6-122">Andmeallika tüüp: **Tabeli kirjed**</span><span class="sxs-lookup"><span data-stu-id="6def6-122">Data source type: **Table records**</span></span>

    - <span data-ttu-id="6def6-123">Selle andmeallika nimi peab olema **CustInvoiceJour**.</span><span class="sxs-lookup"><span data-stu-id="6def6-123">This data source must be named **CustInvoiceJour**.</span></span>
    - <span data-ttu-id="6def6-124">See peab viitama rakendustabelile CustInvoiceJour.</span><span class="sxs-lookup"><span data-stu-id="6def6-124">It must refer to the CustInvoiceJour application table.</span></span>
    - <span data-ttu-id="6def6-125">Seda kasutatakse käitusajal, et edastada printimiseks valitud arvete loend rakendusest ER-i mudelivastendusele.</span><span class="sxs-lookup"><span data-stu-id="6def6-125">It's used at runtime to pass from the application to the ER model mapping the list of invoices that have been selected for printing.</span></span>

- <span data-ttu-id="6def6-126">Andmeallika tüüp: **Objekt**</span><span class="sxs-lookup"><span data-stu-id="6def6-126">Data source type: **Object**</span></span>

    - <span data-ttu-id="6def6-127">Selle andmeallika nimi peab olema **PrintMgmtPrintSettingDetail**.</span><span class="sxs-lookup"><span data-stu-id="6def6-127">This data source must be named **PrintMgmtPrintSettingDetail**.</span></span>
    - <span data-ttu-id="6def6-128">See peab viitama rakendusklassile **PrintMgmtPrintSettingDetail**.</span><span class="sxs-lookup"><span data-stu-id="6def6-128">It must refer to the **PrintMgmtPrintSettingDetail** application class.</span></span>
    - <span data-ttu-id="6def6-129">Seda kasutatakse käitusajal, et edastada töötava ER-vormingu prindihalduse sätete üksikasjad rakendusest ER-i mudelivastendusele.</span><span class="sxs-lookup"><span data-stu-id="6def6-129">It's used at runtime to pass from the application to the ER model mapping details of the print management settings for the ER format that is running.</span></span>

<span data-ttu-id="6def6-130">Rakenduse ER-i raamistikuga integreerimise üksikasjad leiate rakenduse lähtekoodi klassis **ERPrintMgmtReportFormatSubscriber** (ER-i rakenduste komplekti integreerimismudel).</span><span class="sxs-lookup"><span data-stu-id="6def6-130">The details of the application integration with the ER framework can be found in the **ERPrintMgmtReportFormatSubscriber** class (ER Application Suite integration model) in the source code of the application.</span></span>

<span data-ttu-id="6def6-131">Lisateavet ER-i mudelivastenduse kujunduse kohta leiate teemast [Elektroonilise aruandluse (ER) mudelivastenduse määratlemine ja andmeallikate valimine](tasks/er-define-model-mapping-select-data-sources-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="6def6-131">For more information about the design of ER model mappings, see [Define model mapping and select data sources for electronic reporting (ER)](tasks/er-define-model-mapping-select-data-sources-2016-11.md).</span></span>

### <a name="configure-the-er-format"></a><span data-ttu-id="6def6-132">ER-i vormingu konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="6def6-132">Configure the ER format</span></span>
<span data-ttu-id="6def6-133">Teie rakenduse eksemplaris peab olema FTI-vormide loomiseks kasutatav ER-i vormingu konfiguratsioon.</span><span class="sxs-lookup"><span data-stu-id="6def6-133">In your application instance, you must have the ER format configuration that will be used to generate FTI forms.</span></span> 

> [!NOTE]
> <span data-ttu-id="6def6-134">See vormingu konfiguratsioon tuleb luua andmemudeli CustomersInvoicing jaoks ja see vorming peab kasutama mudelivastendust, millel on juurdeskriptor **FreeTextInvoice**.</span><span class="sxs-lookup"><span data-stu-id="6def6-134">This format configuration must be created for the CustomersInvoicing data model, and it must use the model mapping that has the **FreeTextInvoice** root descriptor.</span></span>

<span data-ttu-id="6def6-135">Teavet ER-i vormingute konfigureerimise kohta leiate teemast [Elektroonilise aruandluse (ER) vormingukonfiguratsiooni loomine](tasks/er-format-configuration-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="6def6-135">For information about how to configure ER formats, see [Create a format configuration for electronic reporting (ER)](tasks/er-format-configuration-2016-11.md).</span></span> <span data-ttu-id="6def6-136">Teavet OpenXML-i vormingus aruannete loomiseks ER-i vormingute kujundamise kohta leiate teemast [Elektroonilise aruandluse (ER) konfiguratsiooni loomine OpenXML-i vormingus aruannete genereerimiseks](tasks/er-design-reports-openxml-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="6def6-136">For information about how to design ER formats to generate reports in OpenXML format, see [Design a configuration for generating reports in OpenXML format for electronic reporting (ER)](tasks/er-design-reports-openxml-2016-11.md).</span></span>

## <a name="configure-print-management"></a><span data-ttu-id="6def6-137">Prindihalduse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="6def6-137">Configure print management</span></span>
<span data-ttu-id="6def6-138">ER-raamistiku kaudu FTI-vormingute loomiseks saate määrata ER-i vorminguid samamoodi, nagu määrate SSRS-aruandeid.</span><span class="sxs-lookup"><span data-stu-id="6def6-138">To generate FTI forms by using the ER framework, you can assign ER formats in the same way that you assign SSRS reports.</span></span> <span data-ttu-id="6def6-139">Selleks, et seostada ER-i vorming kõikide müügireskontro FTI-dega, valige **Müügireskontro** \> **Seadistus** \> **Vormid** \> **Vormi seadistus** \> **Üldine** \> **Prindihaldus** \> **Vabas vormis arve** \> **Originaal**.</span><span class="sxs-lookup"><span data-stu-id="6def6-139">To associate the ER format with all Accounts receivable FTIs, go to **Accounts receivable** \> **Setup** \> **Forms** \> **Form setup** \> **General** \> **Print management** \> **Free text invoice** \> **Original**.</span></span> <span data-ttu-id="6def6-140">ER-i vormingu seostamiseks kindla kliendi või arvega järgige järgmisi juhiseid.</span><span class="sxs-lookup"><span data-stu-id="6def6-140">To associate the ER format with a specific customer or invoice, follow these steps.</span></span>

1. <span data-ttu-id="6def6-141">Avage **Müügireskontro** \> **Arved** \> **Kõik vabas vormis arved**.</span><span class="sxs-lookup"><span data-stu-id="6def6-141">Go to **Accounts receivable** \> **Invoices** \> **All free text invoices**.</span></span>
2. <span data-ttu-id="6def6-142">Valige FTI, millega ER-i vorming seostada, ja avage leht **Prindihalduse seadistus**.</span><span class="sxs-lookup"><span data-stu-id="6def6-142">Select the FTI to associate the ER format with, and open the **Print management setup** page.</span></span>
3. <span data-ttu-id="6def6-143">Valige dokumendi tase, et määrata töötlemisele minevate arvete ulatus.</span><span class="sxs-lookup"><span data-stu-id="6def6-143">Select the document level to specify the scope of invoices for processing.</span></span>
4. <span data-ttu-id="6def6-144">Valige määratletud dokumendi taseme jaoks ER-i vorming.</span><span class="sxs-lookup"><span data-stu-id="6def6-144">Select the ER format for the specified document level.</span></span>

![Prindihalduse seadistus](media/FTIbyGER-PMSetting.png)

> [!NOTE]
> <span data-ttu-id="6def6-146">Valitud vormingu väljal **Aruande vormingu otsing** ilmuvad vaid ER-i vormingud, mis kasutavad andmemudeli **CustomersInvoicing** juurdeskriptorit **FreeTextInvoice**.</span><span class="sxs-lookup"><span data-stu-id="6def6-146">Only ER formats that use the **FreeTextInvoice** root descriptor of the **CustomersInvoicing** data model appear in the **Report format lookup** field for the selected format.</span></span>

## <a name="generate-fti-forms"></a><span data-ttu-id="6def6-147">FTI-vormide loomine</span><span class="sxs-lookup"><span data-stu-id="6def6-147">Generate FTI forms</span></span>
<span data-ttu-id="6def6-148">FTI-vorme luuakse ER-i raamistikus samamoodi, nagu luuakse SSRS-aruandeid.</span><span class="sxs-lookup"><span data-stu-id="6def6-148">FTI forms are generated in the ER framework in the same way that SSRS reports are generated.</span></span>

<span data-ttu-id="6def6-149">FTI-vormide loomiseks saate valida arveid kas vahemiku järgi või valiku alusel.</span><span class="sxs-lookup"><span data-stu-id="6def6-149">To generate FTI forms, you can select invoices either by range or by selection.</span></span> 

![Arvete valimine](media/FTIbyGER-InvoiceSelection.png)

![Arve eelvaade](media/FTIbyGER-InvoiceExcelPreview.png)

<span data-ttu-id="6def6-152">Kui kasutate ER-i vorminguid, et sellel teel FTI-vorme printida, siis kasutatakse ER-i failide vaikesihtkohti.</span><span class="sxs-lookup"><span data-stu-id="6def6-152">When you use ER formats to print FTI forms in this way, the default ER file destinations are used.</span></span> <span data-ttu-id="6def6-153">Seda sihtkohta ei saa muuta.</span><span class="sxs-lookup"><span data-stu-id="6def6-153">You can't change the destination.</span></span> <span data-ttu-id="6def6-154">Lisateavet ER-i vormingute sihtkohtade konfigureerimise kohta leiate teemast [Elektroonilise aruandluse sihtkohad](electronic-reporting-destinations.md).</span><span class="sxs-lookup"><span data-stu-id="6def6-154">For more information about how to configure the ER destinations for ER formats, see [Electronic reporting destinations](electronic-reporting-destinations.md).</span></span>

<span data-ttu-id="6def6-155">FTI postitamisel saate ka luua FTI-vorme, kui lülitate sisse suvandi **Prindi arve** ja välja suvandi **Kasuta prindihalduse sihtkohti**.</span><span class="sxs-lookup"><span data-stu-id="6def6-155">You can also generate FTI forms when you post an FTI, by turning **Print invoice** on and turning **Use print management destinations** off.</span></span>

> [!NOTE]
> <span data-ttu-id="6def6-156">Kui kasutate ER-i vorminguid, et sellel teel FTI-vorme printida, siis kasutatakse ER-i failide vaikesihtkohti.</span><span class="sxs-lookup"><span data-stu-id="6def6-156">When you use ER formats to print FTI forms in this way, the default ER file destinations are used.</span></span> <span data-ttu-id="6def6-157">Kui sihtkoht on juba konfigureeritud, saate muuta vaikesihtkoha käitusajal.</span><span class="sxs-lookup"><span data-stu-id="6def6-157">You can change the default destination at runtime if the destination has already been configured.</span></span> <span data-ttu-id="6def6-158">Sihtkoha muutmiseks peab teil olema järgmine turbeprivileeg.</span><span class="sxs-lookup"><span data-stu-id="6def6-158">To change the destination, you must have the following security privilege:</span></span>
>
> - <span data-ttu-id="6def6-159">**Nimi:** ERFormatDestinationRuntimeMaintain</span><span class="sxs-lookup"><span data-stu-id="6def6-159">**Name:** ERFormatDestinationRuntimeMaintain</span></span>
> - <span data-ttu-id="6def6-160">**Silt:** elektroonilise aruandluse vormingu sihtkoha haldamine käitusaja jooksul</span><span class="sxs-lookup"><span data-stu-id="6def6-160">**Label:** Maintain electronic reporting format destination during runtime</span></span>

![Elektroonilise aruandluse sihtkoht](media/FTIbyGER-ERFileDestinationSetting.png)

![Elektroonilise aruandluse vormingu sihtkoht](media/FTIbyGER-ERFileDestinationUsage.png)

<span data-ttu-id="6def6-163">ER-i raamistik toetab praegu loodud dokumentide jaoks järgmisi sihtkohti.</span><span class="sxs-lookup"><span data-stu-id="6def6-163">The ER framework currently supports the following destinations for generated documents:</span></span>

- <span data-ttu-id="6def6-164">**Allalaaditud fail** – loodud vorme pakutakse allalaadimistena, mida saate brauseri kaudu salvestada.</span><span class="sxs-lookup"><span data-stu-id="6def6-164">**Downloaded file** – Generated forms are offered as downloads that you can save by using the browser.</span></span>
- <span data-ttu-id="6def6-165">**Ekraan** – kasutatakse rakendust Microsoft Office 365 Excel, et kuvada loodud FTI-vormide eelvaateid Exceli vormingus.</span><span class="sxs-lookup"><span data-stu-id="6def6-165">**Screen** – Microsoft Office 365 Excel is used to preview generated FTI forms in Excel format.</span></span>
- <span data-ttu-id="6def6-166">**SharePointi kaust** – loodud vorme hoiustatakse dokumendihalduse raamistiku sätete järgi.</span><span class="sxs-lookup"><span data-stu-id="6def6-166">**SharePoint folder** – Generated forms are stored based on the settings of the Document management framework.</span></span>
- <span data-ttu-id="6def6-167">**Rakenduse arhiiv** – loodud vorme hoiustatakse Microsoft Azure’i salvestusruumis käivituslogi kirjete manustena.</span><span class="sxs-lookup"><span data-stu-id="6def6-167">**Application archive** – Generated forms are stored as attachments of execution log records in the Microsoft Azure Storage.</span></span>
- <span data-ttu-id="6def6-168">**Meil** – loodud vormid saadetakse meilimanustena.</span><span class="sxs-lookup"><span data-stu-id="6def6-168">**Email** – Generated forms are sent as email attachments.</span></span>

> [!NOTE]
> <span data-ttu-id="6def6-169">Te ei saa loodud FTI-vorme otse printimisele saata, sest otseprintimine kasutab Dynamicsi printeri marsruudivaliku agenti, mis ei ole praegu toetatud.</span><span class="sxs-lookup"><span data-stu-id="6def6-169">You can't send the FTI forms that are generated directly to the printer, because direct printing that uses the Dynamics Printer Routing Agent isn't currently supported.</span></span>

## <a name="download-sample-er-configurations-to-generate-printable-fti-forms"></a><span data-ttu-id="6def6-170">ER-i näidiskonfiguratsioonide allalaadimine, et luua prinditavaid FTI-vorme</span><span class="sxs-lookup"><span data-stu-id="6def6-170">Download sample ER configurations to generate printable FTI forms</span></span>
<span data-ttu-id="6def6-171">Saate alla laadida ER-i näidiskonfiguratsioone, et kasutada neid oma FTI-lahenduses mallina.</span><span class="sxs-lookup"><span data-stu-id="6def6-171">You can download sample ER configurations to use as a template for your FTI solution.</span></span> <span data-ttu-id="6def6-172">Konfiguratsioone talletatakse Microsoft Dynamicsi teenuse Lifecycle Services (LCS) ühiste vahendite teegis.</span><span class="sxs-lookup"><span data-stu-id="6def6-172">The configurations are stored in the Shared asset library in Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="6def6-173">Konfiguratsioonid sisaldavad järgmist.</span><span class="sxs-lookup"><span data-stu-id="6def6-173">The configurations include:</span></span>

- <span data-ttu-id="6def6-174">Konfiguratsioon **Kliendiarvete mudel** sisaldab vajalikku andmemudelit ja mudelivastendust.</span><span class="sxs-lookup"><span data-stu-id="6def6-174">The **Customer invoicing model** configuration contains the required data model and model mapping.</span></span>
- <span data-ttu-id="6def6-175">Konfiguratsioon **Kliendi FTI-aruanne (GER)** sisaldab näidisvormingut.</span><span class="sxs-lookup"><span data-stu-id="6def6-175">The **Customer FTI report (GER)** configuration contains the sample format.</span></span>

> [!NOTE]
> <span data-ttu-id="6def6-176">Need konfiguratsioonid on loodud näidisteks, et selgitada võimalikke stsenaariumeid.</span><span class="sxs-lookup"><span data-stu-id="6def6-176">These configurations have been created as samples to help clarify possible scenarios.</span></span> <span data-ttu-id="6def6-177">Nende konfiguratsioonide tulevik sõltub selle hinnangu tulemustest ja saadud tagasisidest.</span><span class="sxs-lookup"><span data-stu-id="6def6-177">The future of these configurations depends on the results of this evaluation and any feedback that is received.</span></span>

### <a name="features-that-are-implemented-in-the-sample-er-format"></a><span data-ttu-id="6def6-178">ER-i näidisvormingus rakendatud funktsioonid</span><span class="sxs-lookup"><span data-stu-id="6def6-178">Features that are implemented in the sample ER format</span></span>
<span data-ttu-id="6def6-179">ER-i näidisvormingu konfiguratsioonis kasutatakse FTI-vormide loomisel mallina Exceli faili.</span><span class="sxs-lookup"><span data-stu-id="6def6-179">In the sample ER format configuration, an Excel file is used as a template to generate FTI forms.</span></span>

![Vormingu koostaja](media/FTIbyGER-ERFormat.png)

<span data-ttu-id="6def6-181">Praegu toetab see ER-i näidisvorming FTI-vormide loomiseks järgmisi funktsioone.</span><span class="sxs-lookup"><span data-stu-id="6def6-181">Currently, this sample ER format supports the following features to generate FTI forms:</span></span>

- <span data-ttu-id="6def6-182">FTI-vormid luuakse nii sisestatud kui ka sisetamata originaalarvete jaoks.</span><span class="sxs-lookup"><span data-stu-id="6def6-182">FTI forms are generated for both original invoices that have been posted and original invoices that haven't yet been posted.</span></span> <span data-ttu-id="6def6-183">Korrigeeritud arveid ja kreeditarveid ei toetata.</span><span class="sxs-lookup"><span data-stu-id="6def6-183">Corrected invoices and credit notes aren't supported.</span></span>
- <span data-ttu-id="6def6-184">FTI-vormid luuakse arve keeles.</span><span class="sxs-lookup"><span data-stu-id="6def6-184">FTI forms are generated in the invoice language.</span></span> <span data-ttu-id="6def6-185">Loodud vormide väärtuste ja kuupäevade vorming on kasutaja kliendi lokaadi sätete põhjal määratud.</span><span class="sxs-lookup"><span data-stu-id="6def6-185">The format of values and dates in the generated forms is based on the settings of the user's client locale.</span></span>
- <span data-ttu-id="6def6-186">Loodud arved näitavad andmete mittesaadavuse teatisi, kui arvetes pole töödeldud ridasid.</span><span class="sxs-lookup"><span data-stu-id="6def6-186">Generated invoices show data unavailability notifications if there are no lines in the invoices that are processed.</span></span>
- <span data-ttu-id="6def6-187">Loodud arvete päised põhinevad paberiformaadil, mis on lehel **Müügireskontro parameetrid** FTI-vormi jaoks valitud.</span><span class="sxs-lookup"><span data-stu-id="6def6-187">Generated invoice headers are based on the paper format that has been selected for the FTI form on the **Accounts receivable parameters** page.</span></span> <span data-ttu-id="6def6-188">Ettevõtte andmeid näidatakse loodud arve vormi päises vaid siis, kui paberiformaadi valik on tühi.</span><span class="sxs-lookup"><span data-stu-id="6def6-188">Company details appear in the header of the generated invoice form only if the paper format is blank.</span></span>
- <span data-ttu-id="6def6-189">Loodud arve vormid näitavad ettevõtte ja kliendi maksuvabastuskoode, kui FTI-vormi jaoks on lehel **Müügireskontro parameetrid** tehtud asjakohane valik.</span><span class="sxs-lookup"><span data-stu-id="6def6-189">Generated invoice forms show company and customer tax exempt numbers when the appropriate option has been selected for the FTI form on the **Accounts receivable parameters** page.</span></span>
- <span data-ttu-id="6def6-190">Loodud arve ridade ja arve kogusumma jaotised näitavad arve valuutaandmete vaikevarianti arve registreerimisvaluutas.</span><span class="sxs-lookup"><span data-stu-id="6def6-190">The generated invoice lines and invoice totals sections show the default invoice's monetary details in the invoice registration currency.</span></span>
- <span data-ttu-id="6def6-191">Loodud arve kogusummade jaotis võib näidata valuutaandmeid eurodes ja arve registreerimisvaluutas, kui suvand **Eurot tähistavas valuutas summa printimine** on lehel **Müügireskontro parameetrid** lubatud.</span><span class="sxs-lookup"><span data-stu-id="6def6-191">The generated invoice totals section can show monetary details in the euro currency and the invoice registration currency when the **Print amount in currency representing the euro** option is enabled on the **Accounts receivable parameters** page.</span></span>
- <span data-ttu-id="6def6-192">Loodud arve vormid näitavad iga protsessi saadavaolevaid arve märkuseid, nagu on määratud lehe **Müügireskontro parameetrid** sätetes.</span><span class="sxs-lookup"><span data-stu-id="6def6-192">Generated invoice forms show any process invoice notes that are available, based on settings on the **Accounts receivable parameters** page.</span></span> <span data-ttu-id="6def6-193">Märkused on olemas nii kogu arve kui ka iga arverea jaoks.</span><span class="sxs-lookup"><span data-stu-id="6def6-193">Notes are included for both the whole invoice and each invoice line.</span></span>
- <span data-ttu-id="6def6-194">Loodud arve vormidel on märkused kliendi FTI-vormi ja töötlemise arve keele jaoks, kui see on nii konfigureeritud ER-i vormi märkuse loendis.</span><span class="sxs-lookup"><span data-stu-id="6def6-194">Generated invoice forms include notes for the customer FTI form and the processing invoice language when they have been configured in the AR form notes list.</span></span>
- <span data-ttu-id="6def6-195">Olenevalt prindihalduse sätetest on loodud arvetel kohandatud tekstiga jalus, kui see on konfigureeritud arve keele, ER-i vormingu ja FTI-dokumendi ulatuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="6def6-195">Depending on the Print management settings, generated invoices include custom footer text when it has been configured for the invoice language, the ER format, and the FTI document scope.</span></span>
- <span data-ttu-id="6def6-196">Loodud arve vormide kogusummade jaotis hõlmab kõik saadavaloleva skonto teave.</span><span class="sxs-lookup"><span data-stu-id="6def6-196">The totals section of generated invoice forms includes any cash discount information that is available.</span></span>
- <span data-ttu-id="6def6-197">Loodud arve vormide maksegraafiku jaotis hõlmab kõik saadavalolevad maksegraafikud.</span><span class="sxs-lookup"><span data-stu-id="6def6-197">The payment schedule section of generated invoice forms includes any payment schedule details that are available.</span></span>
- <span data-ttu-id="6def6-198">Loodud arve vormide hinnalisandi jaotis hõlmab kõik saadavalolevad tasude kanded.</span><span class="sxs-lookup"><span data-stu-id="6def6-198">The markup section of generated invoice forms includes any charges transactions that are available.</span></span>
- <span data-ttu-id="6def6-199">Loodud arve vormid sisaldavad käibemaksu üksikasju, nagu on määratletud lehe **Müügireskontro parameetrid** sättes **Käibemaksu täpsustus**.</span><span class="sxs-lookup"><span data-stu-id="6def6-199">Generated invoice forms include sales tax details, based on the **Sales tax specification** setting on the **Accounts receivable parameters** page.</span></span> <span data-ttu-id="6def6-200">Selles jaotises võidakse näidata maksu üksikasju kas ainult arve registreerimisvaluutas või arve registreerimisvaluutas ja ettevõtte arvestusvaluutas samal ajal.</span><span class="sxs-lookup"><span data-stu-id="6def6-200">This section can show tax details either in the invoice registration currency only, or in the invoice registration currency and the company accounting currency at the same time.</span></span>
- <span data-ttu-id="6def6-201">Loodud arve vormid näitavad otsekorralduse teatise üksikasju.</span><span class="sxs-lookup"><span data-stu-id="6def6-201">Generated invoice forms show direct debit notification details.</span></span> <span data-ttu-id="6def6-202">Näiteks näitavad need, millal valiti arve jaoks kohustusliku otsekorralduse loa ID-ga makseviis, millal registreeriti töödeldav arve valuutas euro ja millal määratleti arve jaoks otsekorralduse loa ID.</span><span class="sxs-lookup"><span data-stu-id="6def6-202">For example, they show when the method of payment that has the mandatory direct debit mandate ID was selected for the invoice, when the processing invoice was registered in the euro currency, and when the direct debit mandate ID was defined for the invoice.</span></span>
- <span data-ttu-id="6def6-203">Loodud arved näitavad kõiki ettemakse üksikasju, mis on sisestatud arvete jaoks saadaval.</span><span class="sxs-lookup"><span data-stu-id="6def6-203">Generated invoices show any prepayment details that are available for posted invoices.</span></span>
- <span data-ttu-id="6def6-204">Loodud arve vorme saab saata arve kliendile meilimanusena.</span><span class="sxs-lookup"><span data-stu-id="6def6-204">Generated invoice forms can be sent to an invoice customer as an email attachment.</span></span> <span data-ttu-id="6def6-205">Kasutatava ER-i vormingu jaoks tuleks konfigureerida asjakohane ER-i faili sihtkoht.</span><span class="sxs-lookup"><span data-stu-id="6def6-205">The appropriate ER file destination should be configured for the ER format that is being used.</span></span>

### <a name="countryregion-specific-features"></a><span data-ttu-id="6def6-206">Riigi/regioonikohased funktsioonid</span><span class="sxs-lookup"><span data-stu-id="6def6-206">Country/region-specific features</span></span> 
<span data-ttu-id="6def6-207">ER-i näidisvormingusse on kaasatud järgmised riigi-/regioonipõhised funktsioonid, et näidata, kuidas konkreetseid nõudeid saab ER-i konfiguratsioonides käsitleda.</span><span class="sxs-lookup"><span data-stu-id="6def6-207">The following country/region-specific features are included in the sample ER format to show how specific requirements can be handled in ER configurations.</span></span>

#### <a name="norway"></a><span data-ttu-id="6def6-208">Norra</span><span class="sxs-lookup"><span data-stu-id="6def6-208">Norway</span></span>
<span data-ttu-id="6def6-209">Loodud arve päisesse lisatakse ettevõtte registri tingimus siis, kui arve töödeldakse juriidilisele isikule, mis on järgmiselt konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="6def6-209">The Enterprise register term is put on the header of the generated invoice form when the invoice is processed for a legal entity that is configured in the following manner:</span></span>

- <span data-ttu-id="6def6-210">Kasutatakse Norra riigi/regiooni konteksti.</span><span class="sxs-lookup"><span data-stu-id="6def6-210">The country/region context for Norway is used.</span></span>
- <span data-ttu-id="6def6-211">Müügidokumentidel on aktiivne parameeter **Prindi Foretaksregisteret**.</span><span class="sxs-lookup"><span data-stu-id="6def6-211">The **Print Foretaksregisteret** parameter is active on sales documents.</span></span>

#### <a name="spain"></a><span data-ttu-id="6def6-212">Hispaania</span><span class="sxs-lookup"><span data-stu-id="6def6-212">Spain</span></span>
<span data-ttu-id="6def6-213">Loodud arve päisesse lisatakse tingimus **Sularahaarvestuse meetodi erirežiim** siis, kui arve töödeldakse juriidilisele isikule, mis on järgmiselt konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="6def6-213">The **Special regime for cash accounting method** term is put on the header of the generated invoice form when the invoice is processed for a legal entity that is configured in the following manner:</span></span>

- <span data-ttu-id="6def6-214">Kasutatakse Hispaania riigi/regiooni konteksti.</span><span class="sxs-lookup"><span data-stu-id="6def6-214">The country/region context for Spain is used.</span></span>
- <span data-ttu-id="6def6-215">Sularahaarvestuse meetodi erirežiim on arve töötlemise kuupäeval lubatud.</span><span class="sxs-lookup"><span data-stu-id="6def6-215">The special regime for the cash accounting method is enabled on the invoice processing date.</span></span>

<span data-ttu-id="6def6-216">Kui saadaval on skonto üksikasjad, näiteks skonto summa ja arverea netosumma, siis näidatakse neid loodud arve kogusumma jaotises siis, kui arve töödeldakse juriidilisele isikule, mis on järgmiselt konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="6def6-216">When cash discount details, such as the cash discount amount and invoice line net amount, are available, they are presented in the invoice totals section of the generated invoice form when it has been processed for a legal entity that is configured in the following manner:</span></span>

- <span data-ttu-id="6def6-217">Kasutatakse Hispaania riigi/regiooni konteksti.</span><span class="sxs-lookup"><span data-stu-id="6def6-217">The country/region context for Spain is used.</span></span>
- <span data-ttu-id="6def6-218">Arve suvandis on valik **Arvele rakendatakse skontot** sisse lülitatud (**Üldised pearaamatu parameetrid** \> **Käibemaksu jaotis**).</span><span class="sxs-lookup"><span data-stu-id="6def6-218">**Cash discount is applied in the invoice** is turned on in the invoice option (**General ledger parameters** \> **Sales tax section**).</span></span>

#### <a name="italy"></a><span data-ttu-id="6def6-219">Itaalia</span><span class="sxs-lookup"><span data-stu-id="6def6-219">Italy</span></span>
<span data-ttu-id="6def6-220">Kaupade allahindluse märge on kaasatud loodud arve arveridadele siis, kui arve töödeldakse juriidilisele isikule, mis on konfigureeritud Itaalia riigi/piirkonna kontekstiga.</span><span class="sxs-lookup"><span data-stu-id="6def6-220">The goods discount mark is included on the invoice lines of the generated invoice when it's being processed for a legal entity that is configured using the country/region context for Italy.</span></span>

#### <a name="finland"></a><span data-ttu-id="6def6-221">Soome</span><span class="sxs-lookup"><span data-stu-id="6def6-221">Finland</span></span>
<span data-ttu-id="6def6-222">Peale loodud arve vormi saab luua maksekorraldusi järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="6def6-222">In addition to the generated invoice form, Giro money transfer slips can be generated as follows:</span></span>

- <span data-ttu-id="6def6-223">Juriidilise isiku jaoks, mis kasutab Soome riigi/regiooni konteksti ja millel on vähemalt üks pangakonto, mis on märgitud **Ülekandekontoks** ja kaasatud **Panga vöötkoodi**.</span><span class="sxs-lookup"><span data-stu-id="6def6-223">For the legal entity that uses the country/region context for Finland, and that has at least one bank account that is marked as **Giro account** and **Bank bar code**.</span></span> 
- <span data-ttu-id="6def6-224">Arve jaoks, mis on **Soome** seostatud maksemanuse jaoks vajalikuks märgitud.</span><span class="sxs-lookup"><span data-stu-id="6def6-224">For an invoice that is marked as required for the **Finnish** associated payment attachment.</span></span>

![Ülekandeleht](media/FTIbyGER-GiroSlip.PNG)

> [!NOTE]
> <span data-ttu-id="6def6-226">ER-i näidisvorming on konfigureeritud valikuliselt eraldi töölehel maksekorraldusi looma.</span><span class="sxs-lookup"><span data-stu-id="6def6-226">The sample ER format has been configured to optionally generate the Giro money transfer slips in the separate worksheet.</span></span>

> [!NOTE]
> <span data-ttu-id="6def6-227">Esmalt peate installima fondi, mida kasutatakse vöötkoodi loomiseks kohalikul masinal, kus vaadatakse Exceli vormingus loodud arve vormi eelvaadet.</span><span class="sxs-lookup"><span data-stu-id="6def6-227">You must first install the font that is used to generate the bar code on the local machine where the generated invoice form in Excel format will be previewed.</span></span>

### <a name="use-the-sample-er-format-to-configure-email-destinations"></a><span data-ttu-id="6def6-228">ER-i näidisvormingu kasutamine meilisihtkohtade konfigureerimiseks</span><span class="sxs-lookup"><span data-stu-id="6def6-228">Use the sample ER format to configure email destinations</span></span>
<span data-ttu-id="6def6-229">Kasutage ER-i näidisvormingu järgmisi elemente, et konfigureerida meilisihtkohti.</span><span class="sxs-lookup"><span data-stu-id="6def6-229">Use the following elements of the sample ER format to configure email destinations:</span></span>

- <span data-ttu-id="6def6-230">Kliendi kontakti meiliaadressile saab juurdepääsu järgmise ER-i avaldisega: **model.InvoiceBase.Contact.ElectronicMail**.</span><span class="sxs-lookup"><span data-stu-id="6def6-230">The email address of a customer contact can be accessed through the following ER expression: **model.InvoiceBase.Contact.ElectronicMail**.</span></span>
- <span data-ttu-id="6def6-231">Meili teema tekstile saab juurdepääsu järgmise ER-i avaldisega: **Emailing.TxtToUse.Subject**.</span><span class="sxs-lookup"><span data-stu-id="6def6-231">The email subject text can be accessed through the following ER expression: **Emailing.TxtToUse.Subject**.</span></span>
- <span data-ttu-id="6def6-232">Meili kehatekstile saab juurdepääsu järgmise ER-i avaldisega: **Emailing.TxtToUse.Body**.</span><span class="sxs-lookup"><span data-stu-id="6def6-232">The email body text can be accessed through the following ER expression: **Emailing.TxtToUse.Body**.</span></span>

![Sihtkoha sätted](media/FTIbyGER-ERFileDestinationSettingEmail.png)

<span data-ttu-id="6def6-234">Meili teema ja keha vaiketekst on ER-i näidisvormingus määratletud.</span><span class="sxs-lookup"><span data-stu-id="6def6-234">The default text of the email's subject and body is defined in the sample ER format.</span></span> <span data-ttu-id="6def6-235">Keelevalik sõltub vormingu siltidest.</span><span class="sxs-lookup"><span data-stu-id="6def6-235">The language depends on the format's labels.</span></span> <span data-ttu-id="6def6-236">Meilide jaoks kasutatakse vaiketeksti, kui lisatud on kohandatud organisatsiooni meilimall, millel on eelmääratletud ID **ERFTITMP**.</span><span class="sxs-lookup"><span data-stu-id="6def6-236">This default text will be used for emails if a custom organization email template that has the predefined **ERFTITMP** ID hasn't been added.</span></span>

> [!NOTE]
> <span data-ttu-id="6def6-237">Meilimalli ID **ERFTITMP** on ER-i näidisvormingus määratletud.</span><span class="sxs-lookup"><span data-stu-id="6def6-237">The **ERFTITMP** email template ID has been defined in the sample ER format.</span></span> <span data-ttu-id="6def6-238">Seda saab vajaduse korral muuta uues näidisvormingu põhjal loodud ER-i vormingus.</span><span class="sxs-lookup"><span data-stu-id="6def6-238">It can be changed as required in a new ER format that is created from this sample format.</span></span>

<span data-ttu-id="6def6-239">Kui eelmääratletud ID-ga **ERFTITMP** organisatsiooni meilimall on lisatud juriidilisele isikule, mille arvet te töötlete, siis kasutatakse meili loomiseks meilimalli teema ja kehateksti.</span><span class="sxs-lookup"><span data-stu-id="6def6-239">If the organization email template that has the predefined **ERFTITMP** ID has been added for the legal entity that you're processing the invoice for, the template for the email subject and body text will be used to generate the email.</span></span> 

![Organisatsiooni meilimallid](media/FTIbyGER-EmailTemplate.png)

![Meilimalli üleslaadimine](media/FTIbyGER-EmailTemplateBody.png)

<span data-ttu-id="6def6-242">ER-i näidisvormingu ER-avaldis **Emailing.TxtToUse.Subject** on konfigureeritud asendama kõiki kohatäite %1 esinemisi töödeldava arve ID-ga.</span><span class="sxs-lookup"><span data-stu-id="6def6-242">The **Emailing.TxtToUse.Subject** ER expression of the sample ER format is configured to replace any occurrences of the placeholder %1 by the processing invoice ID.</span></span>

<span data-ttu-id="6def6-243">ER-i näidisvormingu ER-avaldis **Emailing.TxtToUse.Body** on konfigureeritud kohatäiteid järgmiste andmetega asendama.</span><span class="sxs-lookup"><span data-stu-id="6def6-243">The **Emailing.TxtToUse.Body** expression of the sample format is configured for the following substitutions for placeholders:</span></span>

- <span data-ttu-id="6def6-244">„%1” asendatakse kliendi kontaktisiku nimega.</span><span class="sxs-lookup"><span data-stu-id="6def6-244">"%1" is replaced with the name of the customer's contact person.</span></span>
- <span data-ttu-id="6def6-245">„%2” asendatakse ettevõtte nimega.</span><span class="sxs-lookup"><span data-stu-id="6def6-245">"%2" is replaced with the company name.</span></span>
- <span data-ttu-id="6def6-246">„%3” asendatakse kliendi nimega.</span><span class="sxs-lookup"><span data-stu-id="6def6-246">"%3" is replaced with the customer name.</span></span>
- <span data-ttu-id="6def6-247">„%4” asendatakse ettevõtte kontaktisiku nimega.</span><span class="sxs-lookup"><span data-stu-id="6def6-247">"%4" is replaced with the name of the company's contact person.</span></span>
- <span data-ttu-id="6def6-248">„%5” asendatakse ettevõtte kontaktisiku ametinimetusega.</span><span class="sxs-lookup"><span data-stu-id="6def6-248">"%5" is replaced with the job title of the company's contact person.</span></span>
- <span data-ttu-id="6def6-249">„%6” asendatakse ettevõtte kontaktisiku meiliaadressiga.</span><span class="sxs-lookup"><span data-stu-id="6def6-249">"%6" is replaced with the email address of the company's contact person.</span></span>

![Meil](media/FTIbyGER-Email.PNG)

## <a name="additional-resources"></a><span data-ttu-id="6def6-251">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="6def6-251">Additional resources</span></span>
[<span data-ttu-id="6def6-252">Elektroonilise aruandluse ülevaade</span><span class="sxs-lookup"><span data-stu-id="6def6-252">Electronic reporting overview</span></span>](general-electronic-reporting.md)

