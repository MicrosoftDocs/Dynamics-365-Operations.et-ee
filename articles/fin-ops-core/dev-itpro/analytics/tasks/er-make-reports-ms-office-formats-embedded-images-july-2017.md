---
title: Konfiguratsioonide kujundamine aruannete loomiseks Office’i vormingus koos manuspiltidega
description: Selles teemas kirjeldatakse, kuidas kujundada konfiguratsioone, mis loovad Exceli ja Wordi vormingus elektroonilisi dokumente, mis sisaldavad manuspilte.
author: NickSelin
ms.date: 01/23/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e1bafc919d73c9e603935398563bb26e8fb277d3
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5751054"
---
# <a name="design-configurations-to-generate-reports-in-office-format-that-have-embedded-images"></a><span data-ttu-id="a3277-103">Konfiguratsioonide kujundamine aruannete loomiseks Office’i vormingus koos manuspiltidega</span><span class="sxs-lookup"><span data-stu-id="a3277-103">Design configurations to generate reports in Office format that have embedded images</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a3277-104">Selle protseduuri toimingute lõpule viimiseks peate esmalt läbima protseduuri „ER Konfiguratsioonipakkuja loomine ja selle märkimine aktiivseks“.</span><span class="sxs-lookup"><span data-stu-id="a3277-104">To complete the steps in this procedure, first complete the procedure, "ER Create a configuration provider and mark it as active."</span></span> <span data-ttu-id="a3277-105">See toiming kirjeldab Microsoft Excelis või Wordis manuspilte sisaldavate elektrooniliste dokumentide loomiseks elektroonilise aruandluse (ER) konfiguratsioonide kujundamist.</span><span class="sxs-lookup"><span data-stu-id="a3277-105">This procedure explains how to design Electronic reporting (ER) configurations to generate a Microsoft Excel or Word document that contains embedded images.</span></span> <span data-ttu-id="a3277-106">Selles protseduuris loote näidisettevõtte Litware, Inc jaoks vajalikud elektroonilise aruandluse konfiguratsioonid. Need toimingud saab lõpule viia USMF-i andmekomplekti abil.</span><span class="sxs-lookup"><span data-stu-id="a3277-106">In this procedure, you will create the required ER configurations for the sample company, Litware, Inc. These steps can be completed using the USMF dataset.</span></span> <span data-ttu-id="a3277-107">Protseduur on loodud kasutajatele, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll.</span><span class="sxs-lookup"><span data-stu-id="a3277-107">This procedure is created for users with the assigned role of system administrator or electronic reporting developer.</span></span> <span data-ttu-id="a3277-108">Enne alustamist laadige alla ja salvestage spikriteemas loetletud failid [Piltide ja vormide manustamine ER-i abil loodavatesse dokumentidesse](../electronic-reporting-embed-images-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="a3277-108">Before you begin, download and save the files listed in the Help topic, [Embed images and shapes in documents that you generate by using ER](../electronic-reporting-embed-images-shapes.md).</span></span> <span data-ttu-id="a3277-109">Failid on järgmised: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png, and Cheque template Word.docx.</span><span class="sxs-lookup"><span data-stu-id="a3277-109">The files are: Model for cheques.xml, Cheques printing format.xml, Company logo.png, Signature image.png, Signature image 2.png, and Cheque template Word.docx.</span></span>

## <a name="verify-prerequisites"></a><span data-ttu-id="a3277-110">Eeltingimuste kontrollimine</span><span class="sxs-lookup"><span data-stu-id="a3277-110">Verify prerequisites</span></span>  
 1. <span data-ttu-id="a3277-111">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="a3277-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>  
 2. <span data-ttu-id="a3277-112">Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja tähistatud aktiivsena.</span><span class="sxs-lookup"><span data-stu-id="a3277-112">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="a3277-113">Kui te ei näe seda konfiguratsioonipakkujat, peate esmalt läbima protseduuris „Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks” toodud juhised.</span><span class="sxs-lookup"><span data-stu-id="a3277-113">If you don't see this configuration provider, complete the steps in the procedure, "Create a configuration provider and mark it as active."</span></span>   
 3. <span data-ttu-id="a3277-114">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="a3277-114">Click Reporting configurations.</span></span>  
 
## <a name="add-a-new-er-model-configuration"></a><span data-ttu-id="a3277-115">Uue elektroonilise aruandluse mudeli konfiguratsiooni lisamine</span><span class="sxs-lookup"><span data-stu-id="a3277-115">Add a new ER model configuration</span></span>  
 1. <span data-ttu-id="a3277-116">Uue mudeli loomise asemel saate laadida ER-i mudeli konfiguratsioonifaili (Model for cheques.xml), mille varem salvestasite.</span><span class="sxs-lookup"><span data-stu-id="a3277-116">Instead of creating a new model, you can load the ER model configuration file (Model for cheques.xml) that you saved earlier.</span></span> <span data-ttu-id="a3277-117">Fail sisaldab maksetšekkide näidisandmemudelit ning andmemudeli ja rakenduse Dynamics 365 for Operations andmekomponentide vastendust.</span><span class="sxs-lookup"><span data-stu-id="a3277-117">This file contains the sample data model for payment cheques and the mapping of the data model to the data components of the Dynamics 365 for Operations application.</span></span>   
 2. <span data-ttu-id="a3277-118">Klõpsake versioonide kiirkaardil nuppu Vahetus.</span><span class="sxs-lookup"><span data-stu-id="a3277-118">On the Versions FastTab, click Exchange.</span></span>   
 3. <span data-ttu-id="a3277-119">Klõpsake nuppu Laadi XML-failist.</span><span class="sxs-lookup"><span data-stu-id="a3277-119">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="a3277-120">Klõpsake käsku Sirvi ja seejärel valige fail Model for cheques.xml.</span><span class="sxs-lookup"><span data-stu-id="a3277-120">Click Browse, and then select Model for cheques.xml.</span></span>   
 5. <span data-ttu-id="a3277-121">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="a3277-121">Click OK.</span></span>  
 6. <span data-ttu-id="a3277-122">Laaditud mudelit kasutatakse Wordis ja Excelis andmeallikana pilte sisaldavate dokumentide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="a3277-122">The loaded model will be used as a data source of information to generate documents that contain images in Excel and Word.</span></span>  

## <a name="add-a-new-er-format-configuration"></a><span data-ttu-id="a3277-123">Uue elektroonilise aruandluse vormingu konfiguratsiooni lisamine</span><span class="sxs-lookup"><span data-stu-id="a3277-123">Add a new ER format configuration</span></span>  
 1. <span data-ttu-id="a3277-124">Uue vormingu loomise asemel saate laadida ER-i vormingu konfiguratsioonifaili (Cheques printing format.xml), mille varem salvestasite.</span><span class="sxs-lookup"><span data-stu-id="a3277-124">Instead of creating a new format, you can load the ER format configuration file (Cheques printing format.xml) that you saved earlier.</span></span> <span data-ttu-id="a3277-125">See fail sisaldab eelprinditud vormi abil tšekkide printimise vormingu näidispaigutust ning vormingu ja andmemudeli „Tšekkide mudel” vastendust.</span><span class="sxs-lookup"><span data-stu-id="a3277-125">This file contains the sample layout of the format to print cheques using the pre-printed form and the mapping of this format to the 'Model for cheques' data model.</span></span>   
 2. <span data-ttu-id="a3277-126">Klõpsake nuppu Vahetus.</span><span class="sxs-lookup"><span data-stu-id="a3277-126">Click Exchange.</span></span>  
 3. <span data-ttu-id="a3277-127">Klõpsake nuppu Laadi XML-failist.</span><span class="sxs-lookup"><span data-stu-id="a3277-127">Click Load from XML file.</span></span>  
 4. <span data-ttu-id="a3277-128">Klõpsake valikut Sirvi ja valige tšekkide printimise fail format.xml.</span><span class="sxs-lookup"><span data-stu-id="a3277-128">Click Browse and select the Cheques printing format.xml file.</span></span>   
 5. <span data-ttu-id="a3277-129">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="a3277-129">Click OK.</span></span>  
 6. <span data-ttu-id="a3277-130">Laiendage puus valik Tšekkide mudel.</span><span class="sxs-lookup"><span data-stu-id="a3277-130">In the tree, expand 'Model for cheques'.</span></span>  
 7. <span data-ttu-id="a3277-131">Valige puus „Model for cheques\Cheques printing format“.</span><span class="sxs-lookup"><span data-stu-id="a3277-131">In the tree, select 'Model for cheques\Cheques printing format'.</span></span>  
 8. <span data-ttu-id="a3277-132">Laaditud vormingut kasutatakse Wordis ja Excelis pilte sisaldavate dokumentide loomiseks.</span><span class="sxs-lookup"><span data-stu-id="a3277-132">The loaded format will be used to generate documents that contain images in Excel and Word.</span></span>   

## <a name="configure-er-user-parameters"></a><span data-ttu-id="a3277-133">Elektroonilise aruandluse kasutaja parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="a3277-133">Configure ER user parameters</span></span>  
 1. <span data-ttu-id="a3277-134">Klõpsake tegumiribal valikut Konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="a3277-134">On the Action Pane, click Configurations.</span></span>  
 2. <span data-ttu-id="a3277-135">Klõpsake valikut Kasutaja parameetrid.</span><span class="sxs-lookup"><span data-stu-id="a3277-135">Click User parameters.</span></span>  
 3. <span data-ttu-id="a3277-136">Tehke väljal Käivita sätted valik Jah.</span><span class="sxs-lookup"><span data-stu-id="a3277-136">Select Yes in the Run settings field.</span></span>  
  <span data-ttu-id="a3277-137">Lülitage sisse lipp „Käivita mustand”, et käivitada valitud vormingu mustandiversioon, mitte lõpule viidud versioon.</span><span class="sxs-lookup"><span data-stu-id="a3277-137">Turn on the 'Run draft' flag to start the draft version of the selected format instead of the completed one.</span></span>  
 4. <span data-ttu-id="a3277-138">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="a3277-138">Click OK.</span></span>  

## <a name="configure-cash--bank-management-parameters"></a><span data-ttu-id="a3277-139">Sularaha- ja pangahalduse parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="a3277-139">Configure Cash & bank management parameters</span></span>  
 1. <span data-ttu-id="a3277-140">Avage Sularaha- ja pangahaldus > Pangakontod > Pangakontod.</span><span class="sxs-lookup"><span data-stu-id="a3277-140">Go to Cash and bank management > Bank accounts > Bank accounts.</span></span>  
 2. <span data-ttu-id="a3277-141">Kasutage kiirfiltrit, et filtrida välja Pangakonto väärtusega USMF OPER.</span><span class="sxs-lookup"><span data-stu-id="a3277-141">Use the Quick Filter to filter on the Bank account field with a value of 'USMF OPER'.</span></span>  
 3. <span data-ttu-id="a3277-142">Klõpsake tegumiribal valikut Seadistus.</span><span class="sxs-lookup"><span data-stu-id="a3277-142">On the Action Pane, click Set up.</span></span>  
 4. <span data-ttu-id="a3277-143">Klõpsake nuppu Kontrolli.</span><span class="sxs-lookup"><span data-stu-id="a3277-143">Click Check.</span></span>  
 5. <span data-ttu-id="a3277-144">Laiendage jaotist Seadistus.</span><span class="sxs-lookup"><span data-stu-id="a3277-144">Expand the Setup section.</span></span>  
 6. <span data-ttu-id="a3277-145">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="a3277-145">Click Edit.</span></span>  
 7. <span data-ttu-id="a3277-146">Tehke väljal Ettevõtte logo valik Jah.</span><span class="sxs-lookup"><span data-stu-id="a3277-146">Select Yes in the Company logo field.</span></span>  
 8. <span data-ttu-id="a3277-147">Klõpsake ettevõtte logo.</span><span class="sxs-lookup"><span data-stu-id="a3277-147">Click Company logo.</span></span>  
 9. <span data-ttu-id="a3277-148">Klõpsake käsku Muuda.</span><span class="sxs-lookup"><span data-stu-id="a3277-148">Click Change.</span></span>  
 10. <span data-ttu-id="a3277-149">Klõpsake käsku Sirvi ja valige varem allalaaditud fail Company logo.png.</span><span class="sxs-lookup"><span data-stu-id="a3277-149">Click Browse and select the file that you downloaded earlier, Company logo.png.</span></span>   
 11. <span data-ttu-id="a3277-150">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="a3277-150">Click Save.</span></span>  
 12. <span data-ttu-id="a3277-151">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a3277-151">Close the page.</span></span>  
 13. <span data-ttu-id="a3277-152">Laiendage jaotist Allkiri.</span><span class="sxs-lookup"><span data-stu-id="a3277-152">Expand the Signature section.</span></span>  
 14. <span data-ttu-id="a3277-153">Valige väljal Esimese allkirja printimine suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="a3277-153">Select Yes in the Print first signature field.</span></span>  
 15. <span data-ttu-id="a3277-154">Klõpsake käsku Muuda.</span><span class="sxs-lookup"><span data-stu-id="a3277-154">Click Change.</span></span>  
 16. <span data-ttu-id="a3277-155">Klõpsake käsku Sirvi ja valige varem allalaaditud fail Signature image.png.</span><span class="sxs-lookup"><span data-stu-id="a3277-155">Click Browse and select the file that you downloaded earlier, Signature image.png.</span></span>   
 17. <span data-ttu-id="a3277-156">Laiendage jaotis Eksemplare.</span><span class="sxs-lookup"><span data-stu-id="a3277-156">Expand the Copies section.</span></span>  
 18. <span data-ttu-id="a3277-157">Tehke väljal Vesimärk valik.</span><span class="sxs-lookup"><span data-stu-id="a3277-157">In the Watermark field, select an option.</span></span>  
 19. <span data-ttu-id="a3277-158">Valige väljal Üldine elektrooniline ekspordivorming suvand Jah.</span><span class="sxs-lookup"><span data-stu-id="a3277-158">Select Yes in the Generic electronic Export format field.</span></span>  
 20. <span data-ttu-id="a3277-159">Saate valida konfiguratsiooni „Tšekkide printimise vorm”.</span><span class="sxs-lookup"><span data-stu-id="a3277-159">Select 'Cheques printing form' configuration.</span></span>  
 21. <span data-ttu-id="a3277-160">Nüüd kasutatakse valitud ER-i vormingut tšekkide printimiseks.</span><span class="sxs-lookup"><span data-stu-id="a3277-160">Now the selected ER format will be used for printing cheques.</span></span>  
 22. <span data-ttu-id="a3277-161">Klõpsake suvandit Manusta.</span><span class="sxs-lookup"><span data-stu-id="a3277-161">Click Attach.</span></span>  
 23. <span data-ttu-id="a3277-162">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="a3277-162">Click New.</span></span>  
 24. <span data-ttu-id="a3277-163">Klõpsake suvandit Fail.</span><span class="sxs-lookup"><span data-stu-id="a3277-163">Click File.</span></span>  
 25. <span data-ttu-id="a3277-164">Klõpsake käsku Sirvi ja valige varem allalaaditud fail Signature image 2.png.</span><span class="sxs-lookup"><span data-stu-id="a3277-164">Click Browse and select the file that you downloaded earlier, Signature image 2.png.</span></span>   
 26. <span data-ttu-id="a3277-165">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a3277-165">Close the page.</span></span>  
 27. <span data-ttu-id="a3277-166">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a3277-166">Close the page.</span></span>  
 28. <span data-ttu-id="a3277-167">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a3277-167">Close the page.</span></span>  
 29. <span data-ttu-id="a3277-168">Minge jaotisse Sularaha- ja pangahaldus > Seadistus > Sularaha- ja pangahalduse parameetrid.</span><span class="sxs-lookup"><span data-stu-id="a3277-168">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>  
 30. <span data-ttu-id="a3277-169">Väljal „Luba eelpäringu loomine passiivsetel pangakontodel:” valige Jah.</span><span class="sxs-lookup"><span data-stu-id="a3277-169">Select Yes in the Allow prenote creation on inactive bank accounts: field.</span></span>  
 31. <span data-ttu-id="a3277-170">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="a3277-170">Click Save.</span></span>  
 32. <span data-ttu-id="a3277-171">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a3277-171">Close the page.</span></span>  


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]