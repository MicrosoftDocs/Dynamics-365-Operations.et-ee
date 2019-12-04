---
title: Elektroonilise aruandluse konfiguratsioonide kujundamine sissetulevate dokumentide sõelumiseks
description: Protseduur näitab, kuidas kujundada elektroonilise aruandluse (ER) konfiguratsioone sissetuleva elektroonilise dokumendi sõelumiseks.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 26a3dee8b73ae710def7e526ceefa7194171d716
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182665"
---
# <a name="design-er-configurations-to-parse-incoming-documents"></a><span data-ttu-id="415da-103">Elektroonilise aruandluse konfiguratsioonide kujundamine sissetulevate dokumentide sõelumiseks</span><span class="sxs-lookup"><span data-stu-id="415da-103">Design ER configurations to parse incoming documents</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="415da-104">Protseduur näitab, kuidas kujundada elektroonilise aruandluse (ER) konfiguratsioone sissetuleva elektroonilise dokumendi sõelumiseks.</span><span class="sxs-lookup"><span data-stu-id="415da-104">This procedure shows how to design Electronic reporting (ER) configurations to parse an incoming electronic document.</span></span> <span data-ttu-id="415da-105">Selles protseduuris selgitatakse, kuidas importida näidisettevõtte Litware, Inc. jaoks loodud elektroonilise aruandluse (ER) konfiguratsioone ja neid kasutada sissetulevate elektrooniliste dokumentide sõelumiseks.</span><span class="sxs-lookup"><span data-stu-id="415da-105">In this procedure, you will import the required ER configurations that have been created for the sample company, Litware, Inc. and use them for parsing incoming electronic documents.</span></span> <span data-ttu-id="415da-106">Selle protseduuri toimingute lõpuleviimiseks peate esmalt läbima protseduuri „ER Konfiguratsioonipakkuja loomine ja selle märkimine aktiivseks“.</span><span class="sxs-lookup"><span data-stu-id="415da-106">To complete the steps in this procedure, you must first complete the procedure, “ER Create a configuration provider and mark it as active.”</span></span>

<span data-ttu-id="415da-107">Protseduur on loodud kasutajatele, kellele on määratud süsteemiadministraatori või elektroonilise aruandluse arendaja roll.</span><span class="sxs-lookup"><span data-stu-id="415da-107">This procedure is created for users with the assigned role of System administrator or Electronic reporting developer.</span></span> 

<span data-ttu-id="415da-108">Need etapid saab lõpule viia ükskõik millise andmekomplekti abil.</span><span class="sxs-lookup"><span data-stu-id="415da-108">These steps can be completed using any dataset.</span></span> <span data-ttu-id="415da-109">Enne alustamist laadige alla ja salvestage teemas „Sissetulevate dokumentide sõelumine avalduse andmete värskendamiseks” loetletud failid (https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/parse-incoming-electronic-documents)).</span><span class="sxs-lookup"><span data-stu-id="415da-109">Before you begin, download and save the files listed in the topic, “Parse incoming documents to update application data” (https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/parse-incoming-electronic-documents).</span></span> <span data-ttu-id="415da-110">Failid on järgmised: EFSTA model.xml EFSTA format.xml Response1.xml Response2.xml Response3.xml, Response4.xml.</span><span class="sxs-lookup"><span data-stu-id="415da-110">The files are: EFSTA model.xml, EFSTA format.xml, Response1.xml, Response2.xml, Response3.xml, Response4.xml.</span></span>

1. <span data-ttu-id="415da-111">Avage Organisatsiooni haldamine > Tööruumid > Elektrooniline aruandlus.</span><span class="sxs-lookup"><span data-stu-id="415da-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
    * <span data-ttu-id="415da-112">Veenduge, et näidisettevõtte Litware, Inc. konfiguratsioonipakkuja on saadaval ja tähistatud aktiivsena.</span><span class="sxs-lookup"><span data-stu-id="415da-112">Make sure that the configuration provider for the sample company, Litware, Inc., is available and marked as Active.</span></span> <span data-ttu-id="415da-113">Kui te ei näe seda konfiguratsioonipakkujat, peate esmalt läbima protseduuris „Konfiguratsiooni pakkuja loomine ja selle märkimine aktiivseks” toodud juhised.</span><span class="sxs-lookup"><span data-stu-id="415da-113">If you don’t see this configuration provider, complete the steps in the procedure, “Create a configuration provider and mark it as active”.</span></span>  
2. <span data-ttu-id="415da-114">Klõpsake valikut Aruandluse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="415da-114">Click Reporting configurations.</span></span>
    * <span data-ttu-id="415da-115">Järgmise stsenaariumiga demonstreeritakse sissetulevate XML-vormingus elektrooniliste dokumentide sõelumisfunktsioone: ERP rakendus taotleb andmeid veebiteenusest (nt http://efsta.org/ EFSTA finantsteenus) ja sõelub sissetulevad vastused, et värskendada sobival moel avalduse andmeid.</span><span class="sxs-lookup"><span data-stu-id="415da-115">The following scenario will be used to show the capabilities of parsing incoming electronic documents in XML format: ERP application requests data from the web service (such as http://efsta.org/ EFSTA fiscal service) and parses the incoming responses to update application data accordingly.</span></span> <span data-ttu-id="415da-116">Kõige tõhusamaks sõelumiseks kasutatakse üht ER-i vormingut olenemata eeldatavate sissetulevate XML-vormingus dokumentide erinevast struktuurist.</span><span class="sxs-lookup"><span data-stu-id="415da-116">For the most efficient way to parse, a single ER format is used despite the different structure of expected incoming documents in XML format.</span></span>   

## <a name="import-and-review-er-configurations"></a><span data-ttu-id="415da-117">ER-i konfiguratsioonide importimine ja ülevaatamine</span><span class="sxs-lookup"><span data-stu-id="415da-117">Import and review ER configurations</span></span>
<span data-ttu-id="415da-118">Importige ER-i mudeli konfiguratsioon, mis sisaldab näidisandmemudelit, mis on mõeldud sissetuleva faili andmete talletamiseks.</span><span class="sxs-lookup"><span data-stu-id="415da-118">Import the ER model configuration that contains the sample data model designed to store the details of the incoming file.</span></span>  
1. <span data-ttu-id="415da-119">Klõpsake nuppu Vahetus.</span><span class="sxs-lookup"><span data-stu-id="415da-119">Click Exchange.</span></span>
2. <span data-ttu-id="415da-120">Klõpsake nuppu Laadi XML-failist.</span><span class="sxs-lookup"><span data-stu-id="415da-120">Click Load from XML file.</span></span>
    * <span data-ttu-id="415da-121">Klõpsake käsku Sirvi ja vali EFSTA fail model.xml.</span><span class="sxs-lookup"><span data-stu-id="415da-121">Click Browse and select the EFSTA model.xml file.</span></span>  
3. <span data-ttu-id="415da-122">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="415da-122">Click OK.</span></span>
4. <span data-ttu-id="415da-123">Valige puul väärtus „EFSTA mudel”.</span><span class="sxs-lookup"><span data-stu-id="415da-123">In the tree, select 'EFSTA model'.</span></span>
5. <span data-ttu-id="415da-124">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="415da-124">Click Designer.</span></span>
    * <span data-ttu-id="415da-125">Vaadake üle imporditud andmemudeli struktuur.</span><span class="sxs-lookup"><span data-stu-id="415da-125">Review the structure of the imported data model.</span></span> <span data-ttu-id="415da-126">Pange tähele, et loetelu enumType määratletakse järgmist tüüpi teenuse vastuste tuvastamiseks: kande esitamise kinnituse saamiseks, viimase esitatud kande kohta teabe saamiseks ja toetamata vastusetüüpide tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="415da-126">Note that the enumType enumeration is defined to recognize the following types of service responses: to get confirmation about transaction’s submission, to get info about last transaction submitted, and to recognize unsupported response types.</span></span>   
6. <span data-ttu-id="415da-127">Laiendage puul väärtust „Vastus”.</span><span class="sxs-lookup"><span data-stu-id="415da-127">In the tree, expand 'Response'.</span></span>
    * <span data-ttu-id="415da-128">Pange tähele, et juurüksus „Vastus” määratletakse selleks, et määrata, millist tüüpi andmeid tuleb toetatud teenuse vastusest hankida, et avalduse andmeid värskendada.</span><span class="sxs-lookup"><span data-stu-id="415da-128">Note that the root item ‘Response’ is defined to specify what kind of data must be taken from a supported service response to update application data accordingly.</span></span>   
7. <span data-ttu-id="415da-129">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="415da-129">Close the page.</span></span>
    * <span data-ttu-id="415da-130">Impordite ER-i vormingu konfiguratsiooni, mis määrab, kuidas  sissetulevaid dokumente sõelutakse ER-i andmemudelisse andmete talletamiseks.</span><span class="sxs-lookup"><span data-stu-id="415da-130">You will import the ER format configuration that specifies how the incoming documents will be parsed to store data in the ER data model.</span></span>   
8. <span data-ttu-id="415da-131">Klõpsake nuppu Vahetus.</span><span class="sxs-lookup"><span data-stu-id="415da-131">Click Exchange.</span></span>
9. <span data-ttu-id="415da-132">Klõpsake nuppu Laadi XML-failist.</span><span class="sxs-lookup"><span data-stu-id="415da-132">Click Load from XML file.</span></span>
    * <span data-ttu-id="415da-133">Klõpsake käsku Sirvi ja vali EFSTA fail format.xml.</span><span class="sxs-lookup"><span data-stu-id="415da-133">Click Browse and select the EFSTA format.xml file.</span></span>  
10. <span data-ttu-id="415da-134">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="415da-134">Click OK.</span></span>
11. <span data-ttu-id="415da-135">Laiendage puul väärtust „EFSTA mudel”.</span><span class="sxs-lookup"><span data-stu-id="415da-135">In the tree, expand 'EFSTA model'.</span></span>
12. <span data-ttu-id="415da-136">Valige puul väärtus „EFSTA mudel\EFSTA vorming”.</span><span class="sxs-lookup"><span data-stu-id="415da-136">In the tree, select 'EFSTA model\EFSTA format'.</span></span>
13. <span data-ttu-id="415da-137">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="415da-137">Click Designer.</span></span>
14. <span data-ttu-id="415da-138">Klõpsake nuppu Laienda/ahenda.</span><span class="sxs-lookup"><span data-stu-id="415da-138">Click Expand/collapse.</span></span>
    * <span data-ttu-id="415da-139">Pange tähele, et vormingus CASE elementi kasutatakse juurena ja see sisaldab kolme pesastatud elementi FILE, mis tähendab, et see vorming on loodud mitmes vormingus sissetulevate failide sõelumiseks.</span><span class="sxs-lookup"><span data-stu-id="415da-139">Note that the CASE format element is used as the root and contains three nested FILE elements, which means that this format has been designed to parse incoming files of several formats.</span></span>  
15. <span data-ttu-id="415da-140">Valige puul väärtus „Vastused\Kande lõpuleviimine\TraC”.</span><span class="sxs-lookup"><span data-stu-id="415da-140">In the tree, select 'Responses\Transaction completion\TraC'.</span></span>
    * <span data-ttu-id="415da-141">Pange tähele, et esitatud kande vastus algab juurelemendist „TraC”.</span><span class="sxs-lookup"><span data-stu-id="415da-141">Note that the response about the submitted transaction starts from the ‘TraC’ root element.</span></span>   
16. <span data-ttu-id="415da-142">Valige puul „Vastused\Viimane kande taotlus\Tra”.</span><span class="sxs-lookup"><span data-stu-id="415da-142">In the tree, select 'Responses\Last transaction request\Tra'.</span></span>
    * <span data-ttu-id="415da-143">Pange tähele, et viimasena esitatud kande vastus algab juurelemendist „Tra”.</span><span class="sxs-lookup"><span data-stu-id="415da-143">Note that the response about the last submitted transaction starts from the ‘Tra’ root element.</span></span>   
17. <span data-ttu-id="415da-144">Valige puul „Vastused\Ootamatu vastus\Tekst”.</span><span class="sxs-lookup"><span data-stu-id="415da-144">In the tree, select 'Responses\Unexpected response\Text'.</span></span>
    * <span data-ttu-id="415da-145">Lisati kolmas element FILE pesastatud elemendiga TEXT, et tuvastada muud tüüpi vastuseid, mis erinevad ülalmainitust.</span><span class="sxs-lookup"><span data-stu-id="415da-145">The third FILE element with nested TEXT element has been added to recognize any other types of responses that differ from mentioned above.</span></span>   
18. <span data-ttu-id="415da-146">Klõpsake nuppu Vormingu vastendamine mudeliga.</span><span class="sxs-lookup"><span data-stu-id="415da-146">Click Map format to model.</span></span>
    * <span data-ttu-id="415da-147">Mudeli vastendus sisaldab andmevoo definitsiooni, millega talletada sõelutud sissetuleva dokumendi üksikasju, kasutades andmemudeli üksusi.</span><span class="sxs-lookup"><span data-stu-id="415da-147">This model mapping contains the definition of data flow to store details of the parsed incoming document with using the data model’s items.</span></span>  
19. <span data-ttu-id="415da-148">Klõpsake valikut Kujundaja.</span><span class="sxs-lookup"><span data-stu-id="415da-148">Click Designer.</span></span>
20. <span data-ttu-id="415da-149">Laiendage puul valikut „format”.</span><span class="sxs-lookup"><span data-stu-id="415da-149">In the tree, expand 'format'.</span></span>
21. <span data-ttu-id="415da-150">Laiendage puul valikut „format\Responses: Case(Responses)”.</span><span class="sxs-lookup"><span data-stu-id="415da-150">In the tree, expand 'format\Responses: Case(Responses)'.</span></span>
    * <span data-ttu-id="415da-151">Vaadake üle andmeallika „Vorming” struktuur.</span><span class="sxs-lookup"><span data-stu-id="415da-151">Review the structure of the ‘format’ data source.</span></span> <span data-ttu-id="415da-152">Pange tähele, et kõiki kolme vastusetüüpi pakutakse eraldi.</span><span class="sxs-lookup"><span data-stu-id="415da-152">Note that all three response types are offered separately.</span></span>   
22. <span data-ttu-id="415da-153">Valige puul „format\Responses: Case(Responses)\aType”.</span><span class="sxs-lookup"><span data-stu-id="415da-153">In the tree, select 'format\Responses: Case(Responses)\aType'.</span></span>
    * <span data-ttu-id="415da-154">Lisati andmeallika üksus „aType”, et näidata vastuse tüüpi. See on seotud andmemudeli üksusega „Tüüp”.</span><span class="sxs-lookup"><span data-stu-id="415da-154">The data source item ‘aType’ has been added to indicate the response type and is bound to the data model item ‘Type’.</span></span>  
23. <span data-ttu-id="415da-155">Klõpsake vahekaarti Kinnitused.</span><span class="sxs-lookup"><span data-stu-id="415da-155">Click the Validations tab.</span></span>
24. <span data-ttu-id="415da-156">Valige puul „Type = format.Responses.aType”.</span><span class="sxs-lookup"><span data-stu-id="415da-156">In the tree, select 'Type = format.Responses.aType'.</span></span>
    * <span data-ttu-id="415da-157">Pange tähele, et ER-i kinnitamine on konfigureeritud selleks, et teavitada kasutajat olukorrast, kui vastuse struktuur ei ühti kande esitamise kinnitusega või viimati esitatud kande teabega (toetamata vastuse puhul).</span><span class="sxs-lookup"><span data-stu-id="415da-157">Note that the ER validation has been configured to inform the user about the situation when the response structure does not match the confirmation about transaction’s submission or the information about last transaction submitted (unsupported response case).</span></span>   
25. <span data-ttu-id="415da-158">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="415da-158">Close the page.</span></span>

## <a name="run-model-mapping-of-er-format-configured-for-parsing-incoming-files"></a><span data-ttu-id="415da-159">Sissetulevate failide sõelumiseks konfigureeritud ER-i vormingu mudelivastenduse käitamine</span><span class="sxs-lookup"><span data-stu-id="415da-159">Run model mapping of ER format configured for parsing incoming files</span></span>
<span data-ttu-id="415da-160">Käivitate loodud mudeli vastendamise testimise eesmärgil, et vaadata, kuidas konfigureeritud ER-i vorming sõelub sissetulevaid teenuse vastuseid.</span><span class="sxs-lookup"><span data-stu-id="415da-160">You will run the created model mapping for testing purposes to see how the configured ER format will parse incoming service responses.</span></span> <span data-ttu-id="415da-161">See etapp kasutab erinevaid XML-faile, et simuleerida veebiteenuste vastuste eri tüüpe.</span><span class="sxs-lookup"><span data-stu-id="415da-161">This step uses different XML files to simulate different type of web service responses.</span></span>   
1. <span data-ttu-id="415da-162">Avage fail Response1.xml XML-lugeris, nt veebibrauseris.</span><span class="sxs-lookup"><span data-stu-id="415da-162">Open the Response1.xml file in an xml reader, such as a web browser.</span></span> <span data-ttu-id="415da-163">Pange tähele, et fail sisaldab lõpuleviidud kande kinnituse üksikasju (juurelement on „TraC”).</span><span class="sxs-lookup"><span data-stu-id="415da-163">Note that this file contains confirmation details about the completed transaction (‘TraC’ is the root element).</span></span>   
2. <span data-ttu-id="415da-164">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="415da-164">Click Run.</span></span>
    * <span data-ttu-id="415da-165">Klõpsake käsku Sirvi ja vali fail Response1.xml.</span><span class="sxs-lookup"><span data-stu-id="415da-165">Click Browse and select the Response1.xml file.</span></span>  
3. <span data-ttu-id="415da-166">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="415da-166">Click OK.</span></span>
    * <span data-ttu-id="415da-167">Vaadake loodud väljundit.</span><span class="sxs-lookup"><span data-stu-id="415da-167">Review the generated output.</span></span> <span data-ttu-id="415da-168">Pange tähele, et vastusetüüp on õigesti tuvastatud ja sõelutud (ERModelEnumDataSourceHandler#EFSTA model#enumType#C tähendab kande lõpuleviimise juhtumit).</span><span class="sxs-lookup"><span data-stu-id="415da-168">Note that the response type has been correctly recognized and parsed (ERModelEnumDataSourceHandler#EFSTA model#enumType#C means transaction completion case).</span></span>   
    * <span data-ttu-id="415da-169">Avage fail Response2.xml XML-lugejas.</span><span class="sxs-lookup"><span data-stu-id="415da-169">Open the Response2.xml file in an XML reader.</span></span> <span data-ttu-id="415da-170">Pange tähele, et fail sisaldab viimase lõpuleviidud kande teavet (juurelement on „Tra”).</span><span class="sxs-lookup"><span data-stu-id="415da-170">Note that this file contains information about last transaction submitted (‘Tra’ is the root element).</span></span>   
4. <span data-ttu-id="415da-171">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="415da-171">Click Run.</span></span>
    * <span data-ttu-id="415da-172">Klõpsake käsku Sirvi ja vali fail Response2.xml.</span><span class="sxs-lookup"><span data-stu-id="415da-172">Click Browse and select the Response2.xml file.</span></span>  
5. <span data-ttu-id="415da-173">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="415da-173">Click OK.</span></span>
    * <span data-ttu-id="415da-174">Vaadake loodud väljundit.</span><span class="sxs-lookup"><span data-stu-id="415da-174">Review the generated output.</span></span> <span data-ttu-id="415da-175">Pange tähele, et vastusetüüp on õigesti tuvastatud ja sõelutud (ERModelEnumDataSourceHandler#EFSTA model#enumType#R tähendab süsteemi taaskäivitamise juhtumit).</span><span class="sxs-lookup"><span data-stu-id="415da-175">Note that the response type has been correctly recognized and parsed (ERModelEnumDataSourceHandler#EFSTA model#enumType#R means system restart case).</span></span>   
    * <span data-ttu-id="415da-176">Avage fail Response3.xml XML-lugejas.</span><span class="sxs-lookup"><span data-stu-id="415da-176">Open the Response3.xml file in an XML reader.</span></span> <span data-ttu-id="415da-177">Pange tähele, et faili algab juurüksusest TraZ ja seda struktuuri ei konfigureeritud ER-i vormingus.</span><span class="sxs-lookup"><span data-stu-id="415da-177">Note that this file starts from the TraZ root item and that this structure is not configured using ER format.</span></span>   
6. <span data-ttu-id="415da-178">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="415da-178">Click Run.</span></span>
    * <span data-ttu-id="415da-179">Klõpsake käsku Sirvi ja vali fail Response3.xml.</span><span class="sxs-lookup"><span data-stu-id="415da-179">Click Browse and select the Response3.xml file.</span></span>  
7. <span data-ttu-id="415da-180">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="415da-180">Click OK.</span></span>
    * <span data-ttu-id="415da-181">Vaadake loodud väljundit.</span><span class="sxs-lookup"><span data-stu-id="415da-181">Review the generated output.</span></span> <span data-ttu-id="415da-182">Pange tähele, et vastusetüüp on õigesti tuvastatud kui toetamata (ERModelEnumDataSourceHandler#EFSTA model#enumType#U).</span><span class="sxs-lookup"><span data-stu-id="415da-182">Note that the response type has been correctly recognized as not-supported (ERModelEnumDataSourceHandler#EFSTA model#enumType#U).</span></span> <span data-ttu-id="415da-183">Vastav teade lisati teabelogisse (ER-i kinnitamissätte kohaselt) ja enamik andmemudelist pole täidetud.</span><span class="sxs-lookup"><span data-stu-id="415da-183">The corresponding message has been placed in the Infolog (according to the ER validation setting), and most of the data model has not been filled in.</span></span>   
    * <span data-ttu-id="415da-184">Avage fail Response4.xml XML-lugejas.</span><span class="sxs-lookup"><span data-stu-id="415da-184">Open the Response4.xml file in an XML reader.</span></span> <span data-ttu-id="415da-185">Pange tähele, et selle faili struktuur on peaaegu sama mis sõelutud failil Response1.xml, v.a juurelemendi „TraC” pesastatud elementide seeria.</span><span class="sxs-lookup"><span data-stu-id="415da-185">Note that the structure of this file is almost the same as the successfully parsed Response1.xml, except the sequence of nested elements of the root element ‘TraC’.</span></span>   
8. <span data-ttu-id="415da-186">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="415da-186">Click Run.</span></span>
    * <span data-ttu-id="415da-187">Klõpsake käsku Sirvi ja valige fail Response4.xml.</span><span class="sxs-lookup"><span data-stu-id="415da-187">Click Browse and select the Response4.xml file.</span></span>  
9. <span data-ttu-id="415da-188">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="415da-188">Click OK.</span></span>
    * <span data-ttu-id="415da-189">Vaadake loodud väljundit.</span><span class="sxs-lookup"><span data-stu-id="415da-189">Review the generated output.</span></span> <span data-ttu-id="415da-190">Pange tähele, et vastusetüüp on õigesti tuvastatud kui toetamata (ERModelEnumDataSourceHandler#EFSTA model#enumType#U).</span><span class="sxs-lookup"><span data-stu-id="415da-190">Note that the response type has been correctly recognized as not-supported (ERModelEnumDataSourceHandler#EFSTA model#enumType#U)).</span></span> <span data-ttu-id="415da-191">Vastav teade lisati teabelogisse ja enamik andmemudelist pole täidetud.</span><span class="sxs-lookup"><span data-stu-id="415da-191">The corresponding message has been placed in the Infolog, and most of the data model has not been filled in.</span></span> <span data-ttu-id="415da-192">Selle põhjuseks ons ee, et ER-i vormingu praegune säte eeldab sissetuleva faili juurüksuse pesastatud elementide teatud jada.</span><span class="sxs-lookup"><span data-stu-id="415da-192">This is because the current setting of this ER format assumes a certain sequence of nested elements of the root item of the incoming file.</span></span>   
10. <span data-ttu-id="415da-193">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="415da-193">Close the page.</span></span>
11. <span data-ttu-id="415da-194">Valige puul väärtus „Vastused\Kande lõpuleviimine\TraC”.</span><span class="sxs-lookup"><span data-stu-id="415da-194">In the tree, select 'Responses\Transaction completion\TraC'.</span></span>
12. <span data-ttu-id="415da-195">Väljal Pesastatud elementide sõelumise järjekord valige „Kõik”.</span><span class="sxs-lookup"><span data-stu-id="415da-195">In the Parsing order of nested elements field, select 'Any'.</span></span>
    * <span data-ttu-id="415da-196">Väljal „Pesastatud elementide sõelumise järjestus” valige Mis tahes, et lubada XML-juurüksuse jaoks pesastatud elementide mis tahes seeria.</span><span class="sxs-lookup"><span data-stu-id="415da-196">Select Any in the ‘Parsing order of nested elements’ field to allow any sequence of nested elements for this root XML item.</span></span>  
13. <span data-ttu-id="415da-197">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="415da-197">Click Save.</span></span>
14. <span data-ttu-id="415da-198">Klõpsake nuppu Vormingu vastendamine mudeliga.</span><span class="sxs-lookup"><span data-stu-id="415da-198">Click Map format to model.</span></span>
15. <span data-ttu-id="415da-199">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="415da-199">Click Run.</span></span>
    * <span data-ttu-id="415da-200">Klõpsake käsku Sirvi ja valige fail Response4.xml.</span><span class="sxs-lookup"><span data-stu-id="415da-200">Click Browse and select the Response4.xml file.</span></span>  
16. <span data-ttu-id="415da-201">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="415da-201">Click OK.</span></span>
    * <span data-ttu-id="415da-202">Vaadake loodud väljundit.</span><span class="sxs-lookup"><span data-stu-id="415da-202">Review the generated output.</span></span> <span data-ttu-id="415da-203">Pange tähele, et vastusetüüpi on nüüd tuvastatud õigesti failiga Response1.xml võrdsena.</span><span class="sxs-lookup"><span data-stu-id="415da-203">Note that the response type has now been properly recognized as equal for Response1.xml file.</span></span>  
