--- 
title: Elektroonilise aruandluse (ER) vormingu muutmine Microsoft Exceli malli uuesti rakendades
description: "Nende etappide lõpuleviimiseks peate esmalt läbima protseduuri „ER-i konfiguratsiooni loomine aruannete loomiseks vormingus OPENXML”."
author: NickSelin
manager: AnnBe
ms.date: 06/19/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: ae1de653354d891e99fb41fa4b10e6910f458cf4
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="modify-a-format-by-reapplying-a-microsoft-excel-template-for-electronic-reporting-er"></a><span data-ttu-id="d788b-103">Elektroonilise aruandluse (ER) vormingu muutmine Microsoft Exceli malli uuesti rakendades</span><span class="sxs-lookup"><span data-stu-id="d788b-103">Modify a format by reapplying a Microsoft Excel template for electronic reporting (ER)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d788b-104">Nende etappide lõpuleviimiseks peate esmalt läbima protseduuri „ER-i konfiguratsiooni loomine aruannete loomiseks vormingus OPENXML”.</span><span class="sxs-lookup"><span data-stu-id="d788b-104">To complete the steps in this procedure, you must first complete the procedure, ER - Design a configuration for generating reports in OPENXML format.</span></span>

<span data-ttu-id="d788b-105">See protseduur selgitab, kuidas muuta elektroonilise aruandluse (ER) vormingu konfiguratsiooni muudetud Microsoft Exceli malli uuesti rakendades.</span><span class="sxs-lookup"><span data-stu-id="d788b-105">This procedure explains how to modify an Electronic reporting (ER) format configuration by reapplying a Microsoft Excel template that has been modified.</span></span> <span data-ttu-id="d788b-106">Selles protseduuris selgitatakse, kuidas importida näidisettevõtte Litware, Inc. jaoks loodud elektroonilise aruandluse (ER) konfiguratsioonidesse muudetud Exceli mall ja seejärel luua elektrooniline dokument.</span><span class="sxs-lookup"><span data-stu-id="d788b-106">In this procedure, you will import a modified Excel template into ER format configurations that have been created for the sample company, Litware, Inc., and then generate electronic documents.</span></span> <span data-ttu-id="d788b-107">Protseduur on loodud kasutajatele, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll.</span><span class="sxs-lookup"><span data-stu-id="d788b-107">This procedure is intended for users who have the system administrator or electronic reporting developer role.</span></span> <span data-ttu-id="d788b-108">Need toimingud saab lõpule viia GBSI-i andmekomplekti abil.</span><span class="sxs-lookup"><span data-stu-id="d788b-108">These steps can be completed by using the GBSI dataset.</span></span> <span data-ttu-id="d788b-109">Enne alustamist laadige alla ja salvestage fail SampleVendPaymWsReport2.xlsx, mis on toodud spikriteemas „Elektroonilise aruandluse vormingu muutmine Exceli malli uuesti kasutades“ (https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template/).</span><span class="sxs-lookup"><span data-stu-id="d788b-109">Before you begin, download and save the file, SampleVendPaymWsReport2.xlsx, which is listed in the Help topic, Modify Electronic reporting format by reapplying an Excel template (https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template/).</span></span>

1. <span data-ttu-id="d788b-110">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="d788b-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="d788b-111">Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja tähistatud aktiivsena.</span><span class="sxs-lookup"><span data-stu-id="d788b-111">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="d788b-112">Kui te ei näe seda konfiguratsioonipakkujat, peate esmalt läbima protseduuris „Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks” toodud juhised.</span><span class="sxs-lookup"><span data-stu-id="d788b-112">If you don’t see this configuration provider, complete the steps in the procedure, Create a configuration provider and mark it as active.</span></span>  

## <a name="select-the-er-format"></a><span data-ttu-id="d788b-113">Elektroonilise aruandluse vormingu valimine</span><span class="sxs-lookup"><span data-stu-id="d788b-113">Select the ER format</span></span>
1. <span data-ttu-id="d788b-114">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="d788b-114">Click Reporting configurations.</span></span>
2. <span data-ttu-id="d788b-115">Laiendage puus sõlme „Payment model”.</span><span class="sxs-lookup"><span data-stu-id="d788b-115">In the tree, expand 'Payment model'.</span></span>
3. <span data-ttu-id="d788b-116">Tehke puul valik Maksemudel \ töölehe aruande näide.</span><span class="sxs-lookup"><span data-stu-id="d788b-116">In the tree, select 'Payment model\Sample worksheet report'.</span></span>
4. <span data-ttu-id="d788b-117">Klõpsake suvandit Manused.</span><span class="sxs-lookup"><span data-stu-id="d788b-117">Click Attachments.</span></span>
    * <span data-ttu-id="d788b-118">Pange tähele, et Exceli fail SampleVendPaymWsReport.xlsx on praegu mallina kasutatav makse töölehe töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="d788b-118">Note that the SampleVendPaymWsReport.xlsx Excel file is currently used as a template for payment journal processing.</span></span>   
5. <span data-ttu-id="d788b-119">Klõpsake valikut Ava.</span><span class="sxs-lookup"><span data-stu-id="d788b-119">Click Open.</span></span>
    * <span data-ttu-id="d788b-120">Klõpsake käsku Ava Exceli malli paigutuse uurimiseks.</span><span class="sxs-lookup"><span data-stu-id="d788b-120">Click Open to explore the layout of the Excel template.</span></span>  
    * <span data-ttu-id="d788b-121">Vaadake mall üle.</span><span class="sxs-lookup"><span data-stu-id="d788b-121">Review the template.</span></span> <span data-ttu-id="d788b-122">Pange tähele, et see sisaldab praegu järgmisi üksikasju iga makserea jaoks: hankija kontonumber, hankija nimi, pank, protsessikood, kontonumber, deebet, kreedit ja valuuta.</span><span class="sxs-lookup"><span data-stu-id="d788b-122">Note that it currently includes the following details for each payment line: vendor account number, vendor name, bank, routing number, account number, debit, credit, and currency.</span></span> <span data-ttu-id="d788b-123">Näiteks soovime selle loendi laiendamiseks lisada üksikasju maksekuupäeva kohta.</span><span class="sxs-lookup"><span data-stu-id="d788b-123">For this example, we want to extend this list by adding details about the payment date.</span></span>   
6. <span data-ttu-id="d788b-124">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d788b-124">Close the page.</span></span>

## <a name="reapply-a-new-excel-template-to-er-format"></a><span data-ttu-id="d788b-125">Rakendage elektroonilise aruandluse vormingule uus Exceli mall</span><span class="sxs-lookup"><span data-stu-id="d788b-125">Reapply a new Excel template to ER format</span></span>
1. <span data-ttu-id="d788b-126">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="d788b-126">Click Designer.</span></span>
    * <span data-ttu-id="d788b-127">Avage mustandversioon valitud elektroonilise aruandluse vormigu redigeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="d788b-127">Open the draft version of the selected ER format for editing.</span></span>  
2. <span data-ttu-id="d788b-128">Klõpsake toimingupaanil nuppu Impordi.</span><span class="sxs-lookup"><span data-stu-id="d788b-128">On the Action Pane, click Import.</span></span>
3. <span data-ttu-id="d788b-129">Klõpsake käsku Uuenda Excelist.</span><span class="sxs-lookup"><span data-stu-id="d788b-129">Click Update from Excel.</span></span>
    * <span data-ttu-id="d788b-130">Klõpsake valikut Uuenda malli ja seejärel valige fail SampleVendPaymWsReport2.xlsx.</span><span class="sxs-lookup"><span data-stu-id="d788b-130">Click ‘Update template’, and then select the file, SampleVendPaymWsReport2.xlsx.</span></span>  
    * <span data-ttu-id="d788b-131">Klõpsake nuppu Värskenda malli ja sirvige, et saada varasem allalaaditud fail SampleVendPaymWsReport2.xlsx.</span><span class="sxs-lookup"><span data-stu-id="d788b-131">Click Update template and browse to get the downloaded earlier SampleVendPaymWsReport2.xlsx file.</span></span>  
4. <span data-ttu-id="d788b-132">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d788b-132">Click OK.</span></span>
    * <span data-ttu-id="d788b-133">Mall SampleVendPaymWsReport2.xlsx on rakendatud.</span><span class="sxs-lookup"><span data-stu-id="d788b-133">The SampleVendPaymWsReport2.xlsx template is applied.</span></span> <span data-ttu-id="d788b-134">Elektroonilise aruandluse vormingu struktuur sünkroonitakse selle malli sisuga, mille elemendid lisatakse elektroonilise aruandluse vormingule.</span><span class="sxs-lookup"><span data-stu-id="d788b-134">The structure of the ER format is synchronized with the content of the template, whose elements are added to the ER format.</span></span> <span data-ttu-id="d788b-135">Kõik olemasolevad elektroonilise aruandluse vormingu elemendid, mis pole malli kaasatud, eemaldatakse vormingu definitsioonist.</span><span class="sxs-lookup"><span data-stu-id="d788b-135">Any existing elements in the ER format that aren’t included in the template are removed from the format definition.</span></span>  
5. <span data-ttu-id="d788b-136">Tehke puul valik „Excel".</span><span class="sxs-lookup"><span data-stu-id="d788b-136">In the tree, select 'Excel'.</span></span>
    * <span data-ttu-id="d788b-137">Pange tähele, et väli Mall sisaldab nüüd viidet uuele mallile.</span><span class="sxs-lookup"><span data-stu-id="d788b-137">Note that the Template field now contains a reference to the new template.</span></span>   
6. <span data-ttu-id="d788b-138">Klõpsake suvandit Manused.</span><span class="sxs-lookup"><span data-stu-id="d788b-138">Click Attachments.</span></span>
7. <span data-ttu-id="d788b-139">Klõpsake valikut Ava.</span><span class="sxs-lookup"><span data-stu-id="d788b-139">Click Open.</span></span>
    * <span data-ttu-id="d788b-140">Klõpsake käsku Ava muudetud Exceli malli paigutuse uurimiseks.</span><span class="sxs-lookup"><span data-stu-id="d788b-140">Click Open to explore the layout of the modified Excel template.</span></span>  
    * <span data-ttu-id="d788b-141">Vaadake mall üle.</span><span class="sxs-lookup"><span data-stu-id="d788b-141">Review the template.</span></span> <span data-ttu-id="d788b-142">Pange tähele, et see sisaldab nüüd maksekuupäeva rida.</span><span class="sxs-lookup"><span data-stu-id="d788b-142">Note that it now contains a line for the payment date.</span></span>   
8. <span data-ttu-id="d788b-143">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d788b-143">Close the page.</span></span>
9. <span data-ttu-id="d788b-144">Laiendage puul valikut „Excel".</span><span class="sxs-lookup"><span data-stu-id="d788b-144">In the tree, expand 'Excel'.</span></span>
10. <span data-ttu-id="d788b-145">Puuvaates laiendage „Excel\PaymLines”.</span><span class="sxs-lookup"><span data-stu-id="d788b-145">In the tree, expand 'Excel\PaymLines'.</span></span>
11. <span data-ttu-id="d788b-146">Tehke puul valik „Excel\PaymLines\PaymDate".</span><span class="sxs-lookup"><span data-stu-id="d788b-146">In the tree, select 'Excel\PaymLines\PaymDate'.</span></span>
    * <span data-ttu-id="d788b-147">Pange tähele, et elektroonilise aruandluse vorming sisaldab nüüd veel ühte üksust.</span><span class="sxs-lookup"><span data-stu-id="d788b-147">Note that the ER format now contains one more item.</span></span> <span data-ttu-id="d788b-148">Exceli malli on lisatud lahter PaymDate.</span><span class="sxs-lookup"><span data-stu-id="d788b-148">A cell, PaymDate, has been added to the Excel template.</span></span>  
12. <span data-ttu-id="d788b-149">Klõpsake vahekaarti Vastendus.</span><span class="sxs-lookup"><span data-stu-id="d788b-149">Click the Mapping tab.</span></span>
13. <span data-ttu-id="d788b-150">Laiendage puus sõlme „model”.</span><span class="sxs-lookup"><span data-stu-id="d788b-150">In the tree, expand 'model'.</span></span>
14. <span data-ttu-id="d788b-151">Laiendage puus sõlme model\Payments.</span><span class="sxs-lookup"><span data-stu-id="d788b-151">In the tree, expand 'model\Payments'.</span></span>
15. <span data-ttu-id="d788b-152">Valige puul suvand model\Payments\Transaction date(TransactionDate).</span><span class="sxs-lookup"><span data-stu-id="d788b-152">In the tree, select 'model\Payments\Transaction date(TransactionDate)'.</span></span>
16. <span data-ttu-id="d788b-153">Klõpsake valikut Seo.</span><span class="sxs-lookup"><span data-stu-id="d788b-153">Click Bind.</span></span>
    * <span data-ttu-id="d788b-154">Täpsustage, millised andmed on uude lahtrisse lisatud käitusajal.</span><span class="sxs-lookup"><span data-stu-id="d788b-154">Specify what data is added to the new cell at runtime.</span></span>  
17. <span data-ttu-id="d788b-155">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="d788b-155">Click Save.</span></span>
18. <span data-ttu-id="d788b-156">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d788b-156">Close the page.</span></span>

## <a name="enable-the-modified-draft-version-of-the-er-format-for-use-in-payment-journal-processing"></a><span data-ttu-id="d788b-157">Luba elektroonilise aruandluse muudetud mustandversiooni kasutamiseks maksete töölehe töötlemisel</span><span class="sxs-lookup"><span data-stu-id="d788b-157">Enable the modified draft version of the ER format for use in payment journal processing</span></span>
1. <span data-ttu-id="d788b-158">Klõpsake tegumiribal valikut Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="d788b-158">On the Action Pane, click Configurations.</span></span>
2. <span data-ttu-id="d788b-159">Klõpsake valikut Kasutaja parameetrid.</span><span class="sxs-lookup"><span data-stu-id="d788b-159">Click User parameters.</span></span>
3. <span data-ttu-id="d788b-160">Tehke väljal Käivita sätted valik Jah.</span><span class="sxs-lookup"><span data-stu-id="d788b-160">Select Yes in the Run settings field.</span></span>
4. <span data-ttu-id="d788b-161">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d788b-161">Click OK.</span></span>
5. <span data-ttu-id="d788b-162">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="d788b-162">Click Edit.</span></span>
6. <span data-ttu-id="d788b-163">Tehke väljal Käivita mustand valik Jah.</span><span class="sxs-lookup"><span data-stu-id="d788b-163">Select Yes in the Run Draft field.</span></span>

## <a name="use-the-modified-draft-version-of-the-er-format-for-payment-journal-processing"></a><span data-ttu-id="d788b-164">Kasutage elektroonilise aruandluse muudetud mustandversiooni maksete töölehe töötlemiseks</span><span class="sxs-lookup"><span data-stu-id="d788b-164">Use the modified draft version of the ER format for payment journal processing</span></span>
    * <span data-ttu-id="d788b-165">Vaadake üle loodud tööleht (sh makseridade uus üksikasi – maksekuupäev).</span><span class="sxs-lookup"><span data-stu-id="d788b-165">Review the created worksheet, including new detail of payment lines – payment date.</span></span>  


