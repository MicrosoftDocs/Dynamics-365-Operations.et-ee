---
title: Eeltingimuste seadistamine mittevastavuse halduseks
description: Kasutage seda protseduuri, et lubada mittevastavuse haldamise protsessid.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, SysUserManagement, SysUserSetup, InventTestDiagnosticType, InventTestMiscCharges, InventTestOperation, InventProblemType, InventProblemTypeSetup, InventQuarantineZone
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9094be37e44b978db224b16c255d04a36c5cefff
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845313"
---
# <a name="set-up-prerequisites-for-nonconformance-management"></a><span data-ttu-id="0c636-103">Eeltingimuste seadistamine mittevastavuse halduseks</span><span class="sxs-lookup"><span data-stu-id="0c636-103">Set up prerequisites for nonconformance management</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0c636-104">Kasutage seda protseduuri, et lubada mittevastavuse haldamise protsessid.</span><span class="sxs-lookup"><span data-stu-id="0c636-104">Use this procedure to enable nonconformance management processes.</span></span> <span data-ttu-id="0c636-105">Mittevastavus kirjeldab protseduuri või kaupa, millel on kvaliteediprobleem, kus kirjeldav teave sisaldab probleemi allikat ja tüüpi.</span><span class="sxs-lookup"><span data-stu-id="0c636-105">A nonconformance describes a procedure or item that has a quality problem, where the descriptive information includes the source and type of problem.</span></span> <span data-ttu-id="0c636-106">Protseduur kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="0c636-106">This procedure uses the USMF demo data company.</span></span> <span data-ttu-id="0c636-107">Tavaliselt teostab selle protseduuri kvaliteedijuht.</span><span class="sxs-lookup"><span data-stu-id="0c636-107">This procedure is typically performed by a quality manager.</span></span>


## <a name="enable-quality-management-processes-within-the-company"></a><span data-ttu-id="0c636-108">Ettevõttes kvaliteedijuhtimise protsesside lubamine</span><span class="sxs-lookup"><span data-stu-id="0c636-108">Enable quality management processes within the company</span></span>
1. <span data-ttu-id="0c636-109">Avage Varude haldus > Seadistus > Varude ja lao halduse parameetrid.</span><span class="sxs-lookup"><span data-stu-id="0c636-109">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="0c636-110">Klõpsake vahekaarti Kvaliteedijuhtimine.</span><span class="sxs-lookup"><span data-stu-id="0c636-110">Click the Quality management tab.</span></span>
3. <span data-ttu-id="0c636-111">Tehke väljal Kasuta kvaliteedijuhtimist valik Jah.</span><span class="sxs-lookup"><span data-stu-id="0c636-111">Select Yes in the Use quality management field.</span></span>
    * <span data-ttu-id="0c636-112">Valige see parameeter ettevõtte jaoks kvaliteedi haldamise protsesside lubamiseks.</span><span class="sxs-lookup"><span data-stu-id="0c636-112">Select this parameter to enable quality management processes for the company.</span></span>  
4. <span data-ttu-id="0c636-113">Sisestage väljale Tunnimäär number.</span><span class="sxs-lookup"><span data-stu-id="0c636-113">In the Hourly rate field, enter a number.</span></span>
    * <span data-ttu-id="0c636-114">Kasutage välja Tunnimäär, et sisestada tunnitasu kohalikus valuutas.</span><span class="sxs-lookup"><span data-stu-id="0c636-114">Use the Hourly rate field to enter an hourly labor rate in the local currency.</span></span> <span data-ttu-id="0c636-115">Tunnimäära kasutatakse mittevastavusega seotud toimingute kulude arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="0c636-115">The hourly rate is used for calculating costs for operations that are related to a nonconformance.</span></span> <span data-ttu-id="0c636-116">Tunnimäär ja arvutatud kulud annavad viiteteavet mittevastavuse kohta ega mõjuta teisi funktsioone.</span><span class="sxs-lookup"><span data-stu-id="0c636-116">The hourly rate and calculated costs provide reference information for a nonconformance, and they do not interact with other functionality.</span></span>  
5. <span data-ttu-id="0c636-117">Klõpsake suvandit Aruande seadistus.</span><span class="sxs-lookup"><span data-stu-id="0c636-117">Click Report setup.</span></span>
    * <span data-ttu-id="0c636-118">See leht võimaldab määratleda kvaliteediaruande märkuse tüübid, mida kasutatakse erinevatel kvaliteedijuhtimise aruannetel.</span><span class="sxs-lookup"><span data-stu-id="0c636-118">This page allows you define the quality report note types that will be used on different kinds of quality management reports.</span></span>  
6. <span data-ttu-id="0c636-119">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="0c636-119">Close the page.</span></span>
7. <span data-ttu-id="0c636-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="0c636-120">Close the page.</span></span>

## <a name="enable-user-for-nonconformance-processing"></a><span data-ttu-id="0c636-121">Mittevastavuse töötlemise lubamine kasutaja jaoks</span><span class="sxs-lookup"><span data-stu-id="0c636-121">Enable user for nonconformance processing</span></span>
1. <span data-ttu-id="0c636-122">Minge jaotisse Süsteemihaldus > Kasutajad > Kasutajad.</span><span class="sxs-lookup"><span data-stu-id="0c636-122">Go to System administration > Users > Users.</span></span>
    * <span data-ttu-id="0c636-123">Mittevastavuse kinnitamise töötlemiseks peab mittevastavusi kinnitavale või tagasilükkavale kasutajale olema lehel Kasutajad määratud väärtus Nimi.</span><span class="sxs-lookup"><span data-stu-id="0c636-123">To process the approval of a nonconformance the user who  approves or rejects nonconformances must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="0c636-124">Dokumendi märkuste kasutamiseks peab kasutajal olema kasutajasuvandites aktiveeritud ka suvand Dokumenditöötlus.</span><span class="sxs-lookup"><span data-stu-id="0c636-124">To use the document notes, the user must also have Document handling activated in the user options.</span></span>  
2. <span data-ttu-id="0c636-125">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="0c636-125">Use the Quick Filter to find records.</span></span> <span data-ttu-id="0c636-126">Näiteks saate filtreerida välja Nimi väärtuse „Ricardo” järgi.</span><span class="sxs-lookup"><span data-stu-id="0c636-126">For example, filter on the Name field with a value of 'Ricardo'.</span></span>
    * <span data-ttu-id="0c636-127">Kasutage filtrit, et otsida kasutajat, kes mittevastavuse kirjeid kinnitab või tagasi lükkab.</span><span class="sxs-lookup"><span data-stu-id="0c636-127">Use the filter to find the user who will be approving or rejecting the nonconformance records.</span></span>  
3. <span data-ttu-id="0c636-128">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="0c636-128">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="0c636-129">Mittevastavuse kinnitamise töötlemiseks peab mittevastavusi kinnitavale või tagasilükkavale kasutajale olema lehel Kasutajad määratud väärtus Nimi.</span><span class="sxs-lookup"><span data-stu-id="0c636-129">To process the approval of a nonconformance, make sure the user who approves or rejects nonconformances has a “Name” value assigned on the Users page.</span></span>  
4. <span data-ttu-id="0c636-130">Klõpsake suvandit Kasutaja suvandid.</span><span class="sxs-lookup"><span data-stu-id="0c636-130">Click User options.</span></span>
5. <span data-ttu-id="0c636-131">Klõpsake vahekaarti Eelistused.</span><span class="sxs-lookup"><span data-stu-id="0c636-131">Click the Preferences tab.</span></span>
6. <span data-ttu-id="0c636-132">Tehke väljal Luba dokumenditöötlus valik Jah.</span><span class="sxs-lookup"><span data-stu-id="0c636-132">Select Yes in the Enable document handling field.</span></span>
    * <span data-ttu-id="0c636-133">Dokumendi märkuste kasutamiseks peab kasutajal olema kasutajasuvandites aktiveeritud ka suvand Dokumenditöötlus.</span><span class="sxs-lookup"><span data-stu-id="0c636-133">To use the document notes, the user must also have Document handling activated in the user options.</span></span>  
7. <span data-ttu-id="0c636-134">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="0c636-134">Close the page.</span></span>
8. <span data-ttu-id="0c636-135">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="0c636-135">Close the page.</span></span>
9. <span data-ttu-id="0c636-136">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="0c636-136">Close the page.</span></span>

## <a name="define-diagnostic-types-for-nonconformance-processing"></a><span data-ttu-id="0c636-137">Mittevastavuse töötlemise jaoks diagnostikatüüpide määratlemine</span><span class="sxs-lookup"><span data-stu-id="0c636-137">Define diagnostic types for nonconformance processing</span></span>
1. <span data-ttu-id="0c636-138">Avage Laohaldus > Seadistus > Kvaliteedijuhtimine > Diagnostika tüübid.</span><span class="sxs-lookup"><span data-stu-id="0c636-138">Go to Inventory management > Setup > Quality management > Diagnostic types.</span></span>
    * <span data-ttu-id="0c636-139">Kasutage lehte Diagnostika tüübid diagnostiliste toimingute klassifikatsiooni määratlemiseks.</span><span class="sxs-lookup"><span data-stu-id="0c636-139">Use the Diagnostic types page to define a classification of diagnostic actions.</span></span> <span data-ttu-id="0c636-140">Parandus tuvastab, mis tüüpi diagnostilist tegevust tuleks kinnitatud mittevastavuse korral kasutada, kes peaks seda tegema ja soovitud ja planeeritud lõpetamiskuupäev.</span><span class="sxs-lookup"><span data-stu-id="0c636-140">A correction identifies what type of diagnostic action should be taken on an approved nonconformance, who should perform it, and the requested and planned completion date.</span></span>  
2. <span data-ttu-id="0c636-141">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0c636-141">Click New.</span></span>
3. <span data-ttu-id="0c636-142">Tippige väärtus väljale Diagnostika.</span><span class="sxs-lookup"><span data-stu-id="0c636-142">In the Diagnostic field, type a value.</span></span>
4. <span data-ttu-id="0c636-143">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="0c636-143">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0c636-144">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="0c636-144">Close the page.</span></span>

## <a name="define-quality-charges-for-nonconformance-processing"></a><span data-ttu-id="0c636-145">Mittevastavuse töötlemise jaoks kvaliteedikulude määratlemine</span><span class="sxs-lookup"><span data-stu-id="0c636-145">Define quality charges for nonconformance processing</span></span>
1. <span data-ttu-id="0c636-146">Avage Laohaldus > Seadistus > Kvaliteedijuhtimine > Kvaliteedikulud.</span><span class="sxs-lookup"><span data-stu-id="0c636-146">Go to Inventory management > Setup > Quality management > Quality charges.</span></span>
    * <span data-ttu-id="0c636-147">Kasutage lehte Kvaliteedikulud, et määratleda kulude klassifikatsioon, mida kasutatakse mittevastavustega seotud toimingutes.</span><span class="sxs-lookup"><span data-stu-id="0c636-147">Use the Quality charges page to define a classification of charges that will used in operations related to nonconformances.</span></span>  
2. <span data-ttu-id="0c636-148">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0c636-148">Click New.</span></span>
3. <span data-ttu-id="0c636-149">Sisestage väärtus väljale Tasukood.</span><span class="sxs-lookup"><span data-stu-id="0c636-149">In the Charges code field, type a value.</span></span>
4. <span data-ttu-id="0c636-150">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="0c636-150">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0c636-151">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="0c636-151">Close the page.</span></span>

## <a name="define-the-operations-for-nonconformance-processing"></a><span data-ttu-id="0c636-152">Mittevastavuste töötlemise jaoks toimingute määratlemine</span><span class="sxs-lookup"><span data-stu-id="0c636-152">Define the operations for nonconformance processing</span></span>
1. <span data-ttu-id="0c636-153">Avage Laohaldus > Seadistus > Kvaliteedijuhtimine > Toimingud.</span><span class="sxs-lookup"><span data-stu-id="0c636-153">Go to Inventory management > Setup > Quality management > Operations.</span></span>
    * <span data-ttu-id="0c636-154">Kasutage lehte Toimingud, et määratleda klassifikatsioon tööle, mida saab teha kinnitatud mittevastavuse puhul.</span><span class="sxs-lookup"><span data-stu-id="0c636-154">Use the Operations page to define a classification of the work that may be performed for an approved nonconformance.</span></span> <span data-ttu-id="0c636-155">Kui seote toimingu mittevastavusega, saate määrata toimingu tegemiseks nõutava teabe seotud materjali, töötundide ja lisakulude kohta.</span><span class="sxs-lookup"><span data-stu-id="0c636-155">When you relate an operation to a nonconformance, you can define information about the associated material, labor hours, and miscellaneous charges that are required to perform the operation.</span></span> <span data-ttu-id="0c636-156">Selle teabe alusel arvutatakse toimingu tegemise hinnanguline kulu.</span><span class="sxs-lookup"><span data-stu-id="0c636-156">This information provides the basis for calculating an estimated cost for performing the operation.</span></span>  
2. <span data-ttu-id="0c636-157">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0c636-157">Click New.</span></span>
3. <span data-ttu-id="0c636-158">Tippige väärtus väljale Toimingud.</span><span class="sxs-lookup"><span data-stu-id="0c636-158">In the Operation field, type a value.</span></span>
4. <span data-ttu-id="0c636-159">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="0c636-159">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0c636-160">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="0c636-160">Close the page.</span></span>

## <a name="define-problem-types-for-nonconformance-processing"></a><span data-ttu-id="0c636-161">Mittevastavuse töötlemise jaoks probleemitüüpide määatlemine</span><span class="sxs-lookup"><span data-stu-id="0c636-161">Define problem types for nonconformance processing</span></span>
1. <span data-ttu-id="0c636-162">Avage Laohaldus > Seadistus > Kvaliteedijuhtimine > Probleemi tüübid.</span><span class="sxs-lookup"><span data-stu-id="0c636-162">Go to Inventory management > Setup > Quality management > Problem types.</span></span>
    * <span data-ttu-id="0c636-163">Kasutage lehte Probleemi tüübid mitmesugustes mittevastavuse tüüpides ilmnevate kvaliteediprobleemide klassifikatsiooni määratlemiseks.</span><span class="sxs-lookup"><span data-stu-id="0c636-163">Use the Problem types page to define a classification of quality problems that are encountered in the various nonconformance types.</span></span> <span data-ttu-id="0c636-164">Mittevastavuse tüübid on Sisemine, Klient, Hankija, Teenuse päring, Tootmine ja Kaastoote tootmine.</span><span class="sxs-lookup"><span data-stu-id="0c636-164">The nonconformance types include Internal, Customer, Vendor, Service request, Production, and Co-product production.</span></span> <span data-ttu-id="0c636-165">Üks probleemi tüüp võib olla seotud mitme mittevastavuse tüübiga.</span><span class="sxs-lookup"><span data-stu-id="0c636-165">A single problem type can be associated with multiple nonconformance types.</span></span>  
2. <span data-ttu-id="0c636-166">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0c636-166">Click New.</span></span>
3. <span data-ttu-id="0c636-167">Tippige väärtus väljale Probleemi tüüp.</span><span class="sxs-lookup"><span data-stu-id="0c636-167">In the Problem type field, type a value.</span></span>
4. <span data-ttu-id="0c636-168">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="0c636-168">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0c636-169">Klõpsake suvandit Mittevastavuse tüübid.</span><span class="sxs-lookup"><span data-stu-id="0c636-169">Click Non conformance types.</span></span>
    * <span data-ttu-id="0c636-170">Kasutage lehte Mittevastavuse tüübid, et lubada probleemi tüübi kasutamine ühes või enamas mittevastavuse tüübis.</span><span class="sxs-lookup"><span data-stu-id="0c636-170">Use the Non conformance types page to authorize the use of a problem type for one or more of the nonconformance types.</span></span> <span data-ttu-id="0c636-171">Näiteks veakoodiga seotud probleemitüüpi saab rakendada kõigis mittevastavuse tüüpides, samas kui kliendikaebuste probleemitüüpi saab rakendada ainult kliendi ja teenuse taotluse mittevastavuse tüüpides.</span><span class="sxs-lookup"><span data-stu-id="0c636-171">For example, a problem type regarding a defect code could apply to all nonconformance types, whereas a problem type about customer complaints may only apply to the customer and service request nonconformance types.</span></span>  
6. <span data-ttu-id="0c636-172">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0c636-172">Click New.</span></span>
7. <span data-ttu-id="0c636-173">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="0c636-173">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="0c636-174">Valige suvand väljal Mittevastavuse tüüp.</span><span class="sxs-lookup"><span data-stu-id="0c636-174">In the Non conformance type field, select an option.</span></span>
9. <span data-ttu-id="0c636-175">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="0c636-175">Close the page.</span></span>
10. <span data-ttu-id="0c636-176">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="0c636-176">Close the page.</span></span>

## <a name="define-quarantine-zones-for-nonconformance-processing"></a><span data-ttu-id="0c636-177">Mittevastavuse töötlemise jaoks vahelao tsoonide määratlemine</span><span class="sxs-lookup"><span data-stu-id="0c636-177">Define quarantine zones for nonconformance processing</span></span>
1. <span data-ttu-id="0c636-178">Avage Laohaldus > Seadistus > Kvaliteedijuhtimine > Vahelao tsoonid.</span><span class="sxs-lookup"><span data-stu-id="0c636-178">Go to Inventory management > Setup > Quality management > Quarantine zones.</span></span>
2. <span data-ttu-id="0c636-179">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0c636-179">Click New.</span></span>
3. <span data-ttu-id="0c636-180">Tippige väärtus väljale Vahelao tsoon.</span><span class="sxs-lookup"><span data-stu-id="0c636-180">In the Quarantine zone field, type a value.</span></span>
4. <span data-ttu-id="0c636-181">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="0c636-181">In the Description field, type a value.</span></span>
5. <span data-ttu-id="0c636-182">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="0c636-182">Close the page.</span></span>

