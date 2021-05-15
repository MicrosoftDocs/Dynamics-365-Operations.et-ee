---
title: Konfiguratsioonide kujundamine aruannete loomiseks Office’i vormingus koos manuspiltidega
description: Selles teemas kirjeldatakse, kuidas kujundada konfiguratsioone, mis loovad Exceli ja Wordi vormingus elektroonilisi dokumente, mis sisaldavad manuspilte.
author: NickSelin
ms.date: 04/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5eea178a351716425706f481ae66c5b5183a52e5
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944553"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="10588-103">Konfiguratsioonide kujundamine aruannete loomiseks Office’i vormingus koos manuspiltidega</span><span class="sxs-lookup"><span data-stu-id="10588-103">Design configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="10588-104">Selle protseduuri toimingute lõpule viimiseks peate esmalt läbima protseduuri „ER Konfiguratsioonipakkuja loomine ja selle märkimine aktiivseks“.</span><span class="sxs-lookup"><span data-stu-id="10588-104">To complete the steps in this procedure, first complete the procedure, "ER Create a configuration provider and mark it as active."</span></span> <span data-ttu-id="10588-105">See toiming kirjeldab Microsoft Excelis või Wordis manuspilte sisaldavate elektrooniliste dokumentide loomiseks elektroonilise aruandluse (ER) konfiguratsioonide kujundamist.</span><span class="sxs-lookup"><span data-stu-id="10588-105">This procedure explains how to design Electronic reporting (ER) configurations to generate a Microsoft Excel or Word document that contains embedded images.</span></span> <span data-ttu-id="10588-106">Selles protseduuris loote näidisettevõtte Litware, Inc jaoks vajalikud elektroonilise aruandluse konfiguratsioonid. Need toimingud saab lõpule viia USMF-i andmekomplekti abil.</span><span class="sxs-lookup"><span data-stu-id="10588-106">In this procedure, you will create the required ER configurations for the sample company, Litware, Inc. These steps can be completed using the USMF dataset.</span></span> <span data-ttu-id="10588-107">Protseduur on loodud kasutajatele, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll.</span><span class="sxs-lookup"><span data-stu-id="10588-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="10588-108">Enne alustamist laadige alla ja talletage kohalikult järgmised failid.</span><span class="sxs-lookup"><span data-stu-id="10588-108">Before you begin, download and save the following files:</span></span> 

| <span data-ttu-id="10588-109">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="10588-109">Description</span></span>                                          | <span data-ttu-id="10588-110">Faili nimi</span><span class="sxs-lookup"><span data-stu-id="10588-110">File name</span></span>                   |
|------------------------------------------------------|-----------------------------|
| <span data-ttu-id="10588-111">ER-i andmemudeli konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="10588-111">ER data model configuration</span></span>                          | [<span data-ttu-id="10588-112">Model for cheques.xml</span><span class="sxs-lookup"><span data-stu-id="10588-112">Model for cheques.xml</span></span>](https://download.microsoft.com/download/6/e/a/6ea166fd-1382-4fdb-8dcb-0f13379f9c8e/Modelforcheques.xml)       |
| <span data-ttu-id="10588-113">Elektroonilise aruandluse vormingu konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="10588-113">ER format configuration</span></span>                              | [<span data-ttu-id="10588-114">Cheques printing format.xml</span><span class="sxs-lookup"><span data-stu-id="10588-114">Cheques printing format.xml</span></span>](https://download.microsoft.com/download/1/7/c/17c301e3-c4ee-4886-ae75-440fcc002c8c/Chequesprintingformat.xml) |
| <span data-ttu-id="10588-115">Ettevõtte logo pilt</span><span class="sxs-lookup"><span data-stu-id="10588-115">Company logo image</span></span>                                   | [<span data-ttu-id="10588-116">Ettevõtte logo.png</span><span class="sxs-lookup"><span data-stu-id="10588-116">Company logo.png</span></span>](https://download.microsoft.com/download/8/2/e/82e6bd81-caac-4e9a-bfce-1392ce7c8616/Companylogo.png)            |
| <span data-ttu-id="10588-117">Allkirja pilt</span><span class="sxs-lookup"><span data-stu-id="10588-117">Signature image</span></span>                                      | [<span data-ttu-id="10588-118">Allkirja pilt.png</span><span class="sxs-lookup"><span data-stu-id="10588-118">Signature image.png</span></span>](https://download.microsoft.com/download/5/0/9/509151b3-06fc-4870-9408-7c9a43b72771/Signatureimage.png)         |
| <span data-ttu-id="10588-119">Alternatiivne allkirjapilt</span><span class="sxs-lookup"><span data-stu-id="10588-119">Alternative signature image</span></span>                          | [<span data-ttu-id="10588-120">Allkirja pilt 2.png</span><span class="sxs-lookup"><span data-stu-id="10588-120">Signature image 2.png</span></span>](https://download.microsoft.com/download/3/0/0/30045bf1-0ff6-4215-9162-b77c2f5dcc7c/Signatureimage2.png)       |
| <span data-ttu-id="10588-121">Microsoft Word Maksekontrollide printimise mall</span><span class="sxs-lookup"><span data-stu-id="10588-121">Microsoft Word template for printing payment checks</span></span>  | [<span data-ttu-id="10588-122">Tšeki malli Word.docx</span><span class="sxs-lookup"><span data-stu-id="10588-122">Cheque template Word.docx</span></span>](https://download.microsoft.com/download/4/4/d/44d9d255-9ad1-42fe-87db-23f319fd8e89/ChequetemplateWord.docx)   |

## <a name="verify-prerequisites"></a><span data-ttu-id="10588-123">Eeltingimuste kontrollimine</span><span class="sxs-lookup"><span data-stu-id="10588-123">Verify prerequisites</span></span>  
 1. <span data-ttu-id="10588-124">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="10588-124">Go to Organization administration > Workspaces > Electronic reporting.</span></span>  
 2. <span data-ttu-id="10588-125">Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja tähistatud aktiivsena.</span><span class="sxs-lookup"><span data-stu-id="10588-125">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="10588-126">Kui te ei näe seda konfiguratsioonipakkujat, peate esmalt läbima protseduuris „Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks” toodud juhised.</span><span class="sxs-lookup"><span data-stu-id="10588-126">If you don't see this configuration provider, complete the steps in the procedure, "Create a configuration provider and mark it as active."</span></span>   
 3. <span data-ttu-id="10588-127">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="10588-127">Click Reporting configurations.</span></span>  
 
## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="10588-128">Uue elektroonilise aruandluse mudeli konfiguratsiooni lisamine</span><span class="sxs-lookup"><span data-stu-id="10588-128">Add a new ER model configuration</span></span>  
 1. <span data-ttu-id="10588-129">Uue mudeli loomise asemel saate laadida ER-i mudeli konfiguratsioonifaili (Model for cheques.xml), mille varem salvestasite.</span><span class="sxs-lookup"><span data-stu-id="10588-129">Instead of creating a new model, you can load the ER model configuration file (Model for cheques.xml) that you saved earlier.</span></span> <span data-ttu-id="10588-130">Fail sisaldab maksetšekkide näidisandmemudelit ning andmemudeli ja rakenduse Dynamics 365 for Operations andmekomponentide vastendust.</span><span class="sxs-lookup"><span data-stu-id="10588-130">This file contains the sample data model for payment cheques and the mapping of the data model to the data components of the Dynamics 365 for Operations application.</span></span>   
 2. <span data-ttu-id="10588-131">Klõpsake versioonide kiirkaardil nuppu Vahetus.</span><span class="sxs-lookup"><span data-stu-id="10588-131">On the Versions FastTab, click Exchange.</span></span>   
 3. <span data-ttu-id="10588-132">Klõpsake nuppu Laadi XML-failist.</span><span class="sxs-lookup"><span data-stu-id="10588-132">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="10588-133">Klõpsake käsku Sirvi ja seejärel valige fail Model for cheques.xml.</span><span class="sxs-lookup"><span data-stu-id="10588-133">Click Browse, and then select Model for cheques.xml.</span></span>   
 5. <span data-ttu-id="10588-134">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="10588-134">Click OK.</span></span>  
 6. <span data-ttu-id="10588-135">Laaditud mudelit kasutatakse Wordis ja Excelis andmeallikana pilte sisaldavate dokumentide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="10588-135">The loaded model will be used as a data source of information to generate documents that contain images in Excel and Word.</span></span>  

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="10588-136">Uue elektroonilise aruandluse vormingu konfiguratsiooni lisamine</span><span class="sxs-lookup"><span data-stu-id="10588-136">Add a new ER format configuration</span></span>  
 1. <span data-ttu-id="10588-137">Uue vormingu loomise asemel saate laadida ER-i vormingu konfiguratsioonifaili (Cheques printing format.xml), mille varem salvestasite.</span><span class="sxs-lookup"><span data-stu-id="10588-137">Instead of creating a new format, you can load the ER format configuration file (Cheques printing format.xml) that you saved earlier.</span></span> <span data-ttu-id="10588-138">See fail sisaldab eelprinditud vormi abil tšekkide printimise vormingu näidispaigutust ning vormingu ja andmemudeli „Tšekkide mudel” vastendust.</span><span class="sxs-lookup"><span data-stu-id="10588-138">This file contains the sample layout of the format to print cheques using the pre-printed form and the mapping of this format to the 'Model for cheques' data model.</span></span>   
 2. <span data-ttu-id="10588-139">Klõpsake nuppu Vahetus.</span><span class="sxs-lookup"><span data-stu-id="10588-139">Click Exchange.</span></span>  
 3. <span data-ttu-id="10588-140">Klõpsake nuppu Laadi XML-failist.</span><span class="sxs-lookup"><span data-stu-id="10588-140">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="10588-141">Klõpsake valikut Sirvi ja valige tšekkide printimise fail format.xml.</span><span class="sxs-lookup"><span data-stu-id="10588-141">Click Browse and select the Cheques printing format.xml file.</span></span>   
 5. <span data-ttu-id="10588-142">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="10588-142">Click OK.</span></span>  
 6. <span data-ttu-id="10588-143">Laiendage puus valik Tšekkide mudel.</span><span class="sxs-lookup"><span data-stu-id="10588-143">In the tree, expand 'Model for cheques'.</span></span>  
 7. <span data-ttu-id="10588-144">Valige puus „Model for cheques\Cheques printing format“.</span><span class="sxs-lookup"><span data-stu-id="10588-144">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>  
 8. <span data-ttu-id="10588-145">Laaditud vormingut kasutatakse Wordis ja Excelis pilte sisaldavate dokumentide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="10588-145">The loaded format will be used to generate documents that contain images in Excel and Word.</span></span>   

## <a name="configure-er-user-parameters"></a><span data-ttu-id="10588-146">Elektroonilise aruandluse kasutaja parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="10588-146">Configure ER user parameters</span></span>  
 1. <span data-ttu-id="10588-147">Klõpsake tegumiribal valikut Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="10588-147">On the Action Pane, click Configurations.</span></span>  
 2. <span data-ttu-id="10588-148">Klõpsake valikut Kasutaja parameetrid.</span><span class="sxs-lookup"><span data-stu-id="10588-148">Click User parameters.</span></span>  
 3. <span data-ttu-id="10588-149">Tehke väljal Käivita sätted valik Jah.</span><span class="sxs-lookup"><span data-stu-id="10588-149">Select Yes in the Run settings field.</span></span>  
  <span data-ttu-id="10588-150">Lülitage sisse lipp „Käivita mustand”, et käivitada valitud vormingu mustandiversioon, mitte lõpule viidud versioon.</span><span class="sxs-lookup"><span data-stu-id="10588-150">Turn on the 'Run draft' flag to start the draft version of the selected format instead of the completed one.</span></span>  
 4. <span data-ttu-id="10588-151">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="10588-151">Click OK.</span></span>  

## <a name="configure-cash--bank-management-parameters"></a><span data-ttu-id="10588-152">Sularaha- ja pangahalduse parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="10588-152">Configure Cash & bank management parameters</span></span>  
 1. <span data-ttu-id="10588-153">Avage Sularaha- ja pangahaldus > Pangakontod > Pangakontod.</span><span class="sxs-lookup"><span data-stu-id="10588-153">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>  
 2. <span data-ttu-id="10588-154">Kasutage kiirfiltrit, et filtrida välja Pangakonto väärtusega USMF OPER.</span><span class="sxs-lookup"><span data-stu-id="10588-154">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>  
 3. <span data-ttu-id="10588-155">Klõpsake tegumiribal valikut Seadistus.</span><span class="sxs-lookup"><span data-stu-id="10588-155">On the Action Pane, click Set up.</span></span>  
 4. <span data-ttu-id="10588-156">Klõpsake nuppu Kontrolli.</span><span class="sxs-lookup"><span data-stu-id="10588-156">Click Check.</span></span>  
 5. <span data-ttu-id="10588-157">Laiendage jaotist Seadistus.</span><span class="sxs-lookup"><span data-stu-id="10588-157">Expand the Setup section.</span></span>  
 6. <span data-ttu-id="10588-158">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="10588-158">Click Edit.</span></span>  
 7. <span data-ttu-id="10588-159">Tehke väljal Ettevõtte logo valik Jah.</span><span class="sxs-lookup"><span data-stu-id="10588-159">Select Yes in the Company logo field.</span></span>  
 8. <span data-ttu-id="10588-160">Klõpsake ettevõtte logo.</span><span class="sxs-lookup"><span data-stu-id="10588-160">Click Company logo.</span></span>  
 9. <span data-ttu-id="10588-161">Klõpsake käsku Muuda.</span><span class="sxs-lookup"><span data-stu-id="10588-161">Click Change.</span></span>  
 10. <span data-ttu-id="10588-162">Klõpsake käsku Sirvi ja valige varem allalaaditud fail Company logo.png.</span><span class="sxs-lookup"><span data-stu-id="10588-162">Click Browse and select the file that you downloaded earlier, Company logo.png.</span></span>   
 11. <span data-ttu-id="10588-163">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="10588-163">Click Save.</span></span>  
 12. <span data-ttu-id="10588-164">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="10588-164">Close the page.</span></span>  
 13. <span data-ttu-id="10588-165">Laiendage jaotist Allkiri.</span><span class="sxs-lookup"><span data-stu-id="10588-165">Expand the Signature section.</span></span>  
 14. <span data-ttu-id="10588-166">Valige väljal Esimese allkirja printimine suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="10588-166">Select Yes in the Print first signature field.</span></span>  
 15. <span data-ttu-id="10588-167">Klõpsake käsku Muuda.</span><span class="sxs-lookup"><span data-stu-id="10588-167">Click Change.</span></span>  
 16. <span data-ttu-id="10588-168">Klõpsake käsku Sirvi ja valige varem allalaaditud fail Signature image.png.</span><span class="sxs-lookup"><span data-stu-id="10588-168">Click Browse and select the file that you downloaded earlier, Signature image.png.</span></span>   
 17. <span data-ttu-id="10588-169">Laiendage jaotis Eksemplare.</span><span class="sxs-lookup"><span data-stu-id="10588-169">Expand the Copies section.</span></span>  
 18. <span data-ttu-id="10588-170">Tehke väljal Vesimärk valik.</span><span class="sxs-lookup"><span data-stu-id="10588-170">In the Watermark field, select an option.</span></span>  
 19. <span data-ttu-id="10588-171">Valige väljal Üldine elektrooniline ekspordivorming suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="10588-171">Select Yes in the Generic electronic Export format field.</span></span>  
 20. <span data-ttu-id="10588-172">Saate valida konfiguratsiooni „Tšekkide printimise vorm”.</span><span class="sxs-lookup"><span data-stu-id="10588-172">Select 'Cheques printing form' configuration.</span></span>  
 21. <span data-ttu-id="10588-173">Nüüd kasutatakse valitud ER-i vormingut tšekkide printimiseks.</span><span class="sxs-lookup"><span data-stu-id="10588-173">Now the selected ER format will be used for printing cheques.</span></span>  
 22. <span data-ttu-id="10588-174">Klõpsake suvandit Manusta.</span><span class="sxs-lookup"><span data-stu-id="10588-174">Click Attach.</span></span>  
 23. <span data-ttu-id="10588-175">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="10588-175">Click New.</span></span>  
 24. <span data-ttu-id="10588-176">Klõpsake suvandit Fail.</span><span class="sxs-lookup"><span data-stu-id="10588-176">Click File.</span></span>  
 25. <span data-ttu-id="10588-177">Klõpsake käsku Sirvi ja valige varem allalaaditud fail Signature image 2.png.</span><span class="sxs-lookup"><span data-stu-id="10588-177">Click Browse and select the file that you downloaded earlier, Signature image 2.png.</span></span>   
 26. <span data-ttu-id="10588-178">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="10588-178">Close the page.</span></span>  
 27. <span data-ttu-id="10588-179">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="10588-179">Close the page.</span></span>  
 28. <span data-ttu-id="10588-180">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="10588-180">Close the page.</span></span>  
 29. <span data-ttu-id="10588-181">Minge jaotisse Sularaha- ja pangahaldus > Seadistus > Sularaha- ja pangahalduse parameetrid.</span><span class="sxs-lookup"><span data-stu-id="10588-181">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>  
 30. <span data-ttu-id="10588-182">Väljal „Luba eelpäringu loomine passiivsetel pangakontodel:” valige Jah.</span><span class="sxs-lookup"><span data-stu-id="10588-182">Select Yes in the Allow prenote creation on inactive bank accounts: field.</span></span>  
 31. <span data-ttu-id="10588-183">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="10588-183">Click Save.</span></span>  
 32. <span data-ttu-id="10588-184">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="10588-184">Close the page.</span></span>  


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
