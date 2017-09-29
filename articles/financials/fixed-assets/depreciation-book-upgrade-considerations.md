---
title: "Kulumiraamatu täiendamise ülevaade"
description: "Varasemates väljalasetes on põhivarade jaoks kaks hindamiskontseptsiooni: väärtusmudelid ja kulumiraamatud. Rakenduses Microsoft Dynamics 365 for Operations (1611) on väärtusmudeli ja kulumiraamatu funktsioonid ühendatud üheks kontseptsiooniks, mis on tuntud kui raamat. Selles teemas antakse mõned asjad, mida täiendamisel arvestada."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, Developer
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 221624
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: d6ce53d4d9335348d0203a524e62dbbdfd1580b6
ms.contentlocale: et-ee
ms.lasthandoff: 07/18/2017

---

# <a name="depreciation-book-upgrade-overview"></a><span data-ttu-id="6aa94-105">Kulumiraamatu täiendamise ülevaade</span><span class="sxs-lookup"><span data-stu-id="6aa94-105">Depreciation book upgrade overview</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="6aa94-106">Varasemates väljalasetes on põhivarade jaoks kaks hindamiskontseptsiooni: väärtusmudelid ja kulumiraamatud.</span><span class="sxs-lookup"><span data-stu-id="6aa94-106">In previous releases, there were two valuation concepts for fixed assets -  value models and depreciation books.</span></span> <span data-ttu-id="6aa94-107">Rakenduses Microsoft Dynamics 365 for Operations (1611) on väärtusmudeli ja kulumiraamatu funktsioonid ühendatud üheks kontseptsiooniks, mis on tuntud kui raamat.</span><span class="sxs-lookup"><span data-stu-id="6aa94-107">In Microsoft Dynamics 365 for Operations (1611), the value model functionality and depreciation book functionality have been merged into a single concept that is known as a book.</span></span> <span data-ttu-id="6aa94-108">Selles teemas antakse mõned asjad, mida täiendamisel arvestada.</span><span class="sxs-lookup"><span data-stu-id="6aa94-108">This topic provides some things to consider for the upgrade.</span></span> 

<span data-ttu-id="6aa94-109">Täiendusprotsess liigutab teie olemasoleva seadistuse ja kõik olemasolevad kanded uude raamatu struktuuri.</span><span class="sxs-lookup"><span data-stu-id="6aa94-109">The upgrade process will move your existing setup and all existing transactions to the new book structure.</span></span> <span data-ttu-id="6aa94-110">Väärtusmudelid jäävad selliseks, nagu need praegu on ehk raamatuks, mis sisestab pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="6aa94-110">Value models will remain as they currently are, as a book that posts to the general ledger.</span></span> <span data-ttu-id="6aa94-111">Kulumiraamatud liigutatakse raamatusse, millel on valik **Pearaamatusse sisestamine** määratud sättele **Ei**.</span><span class="sxs-lookup"><span data-stu-id="6aa94-111">Depreciation books will be moved to a book that has the **Post to general ledger** option set to **No**.</span></span> <span data-ttu-id="6aa94-112">Kulumiraamatu töölehe nimed liigutatakse pearaamatu töölehele, mille nimel on sisestamiskiht määratud sättele **Pole**.</span><span class="sxs-lookup"><span data-stu-id="6aa94-112">Depreciation book journal names will be moved to a general ledger journal name with the posting layer set to **None**.</span></span> <span data-ttu-id="6aa94-113">Kulumiraamatu kanded teisaldatakse jaotisse Põhivara kanded.</span><span class="sxs-lookup"><span data-stu-id="6aa94-113">Depreciation book transactions will be moved to Fixed asset transactions.</span></span> 

<span data-ttu-id="6aa94-114">Enne andmete täiendamise käivitamist peate mõistma kahte suvandit, mis on saadaval kulumiraamatu tööleheridade täiendamiseks kanneteks, ja numbriseeriat, mida kasutatakse kande seeria jaoks.</span><span class="sxs-lookup"><span data-stu-id="6aa94-114">Before running the data upgrade, you should understand the two options available for upgrading depreciation book journal lines to transaction vouchers, and the number sequence that will be used for the voucher series.</span></span> 

<span data-ttu-id="6aa94-115">Suvand 1:  **Süsteemi määratletud numbriseeria** – see on vaikesuvand täiendamise jõudluse optimeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="6aa94-115">Option 1:  **System-defined number sequence** - This is the default option to optimize upgrade performance.</span></span> <span data-ttu-id="6aa94-116">Täiendamine ei kasutada numbriseeriate raamistikku, vaid eraldab selleasemel kanded kogumipõhise lähenemisega.</span><span class="sxs-lookup"><span data-stu-id="6aa94-116">The upgrade will not use the number sequences framework, but instead will allocate vouchers with a set-based approach.</span></span> <span data-ttu-id="6aa94-117">Pärast täiendamist luuakse uus numbriseeria, mille parameeter **Järgmine numbrikomplekt** põhineb asjakohaselt täiendatud kandel.</span><span class="sxs-lookup"><span data-stu-id="6aa94-117">After the upgrade, the new number sequence will be created with the **Next number set** appropriately based on the upgraded transactions.</span></span> <span data-ttu-id="6aa94-118">Vaikimisi on kasutatava numbriseeria vorming FADBUpgr\#\#\#\#\#\#\#\#\#.</span><span class="sxs-lookup"><span data-stu-id="6aa94-118">By default, the number sequence used will be in the FADBUpgr\#\#\#\#\#\#\#\#\# format.</span></span> <span data-ttu-id="6aa94-119">Seda lähenemist kasutades saate vormingut korrigeerida järgmiste parameetrite abil.</span><span class="sxs-lookup"><span data-stu-id="6aa94-119">There are a few parameters available to you to adjust the format when using this approach:</span></span>

-   <span data-ttu-id="6aa94-120">**Numbriseeria kood** – kood numbriseeria tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="6aa94-120">**Number sequence code** – The code to identify the number sequence.</span></span> <span data-ttu-id="6aa94-121">Seda numbriseeria koodi ei saa eksisteerida, kuna see luuakse täiendamisega.</span><span class="sxs-lookup"><span data-stu-id="6aa94-121">This number sequence code cannot exist since it will be created by the upgrade.</span></span>
    -   <span data-ttu-id="6aa94-122">Püsinimi: **NumberSequenceDefaultCode**</span><span class="sxs-lookup"><span data-stu-id="6aa94-122">Constant name: **NumberSequenceDefaultCode**</span></span>
    -   <span data-ttu-id="6aa94-123">Vaikeväärtus: "FADBUpgr"</span><span class="sxs-lookup"><span data-stu-id="6aa94-123">Default value: "FADBUpgr"</span></span>
-   <span data-ttu-id="6aa94-124">**Eesliide** – püsistringi väärtus, mida kasutatakse kande numbrite jaoks eesliitena.</span><span class="sxs-lookup"><span data-stu-id="6aa94-124">**Prefix** – The constant string value that will be used as a prefix for the voucher numbers.</span></span>
    -   <span data-ttu-id="6aa94-125">Püsinimi: **NumberSequenceDefaultParameterPrefix**</span><span class="sxs-lookup"><span data-stu-id="6aa94-125">Constant name: **NumberSequenceDefaultParameterPrefix**</span></span>
    -   <span data-ttu-id="6aa94-126">Vaikeväärtus: "FADBUpgr"</span><span class="sxs-lookup"><span data-stu-id="6aa94-126">Default value: "FADBUpgr"</span></span>
-   <span data-ttu-id="6aa94-127">**Tähtnumbriline pikkus** – numbriseeria tähtnumbrilise segmendi pikkus.</span><span class="sxs-lookup"><span data-stu-id="6aa94-127">**Alphanumeric length** – The length of the alphanumeric segment of the number sequence.</span></span>
    -   <span data-ttu-id="6aa94-128">Püsinimi: **NumberSequenceDefaultParameterAlpanumericLength **</span><span class="sxs-lookup"><span data-stu-id="6aa94-128">Constant name: **NumberSequenceDefaultParameterAlpanumericLength **</span></span>
    -   <span data-ttu-id="6aa94-129">Vaikeväärtus: 9</span><span class="sxs-lookup"><span data-stu-id="6aa94-129">Default value: 9</span></span>
-   <span data-ttu-id="6aa94-130">**Algusnumber** – esimene numbriseerias kasutatav number.</span><span class="sxs-lookup"><span data-stu-id="6aa94-130">**Start number** - The first number to be used in the number sequence.</span></span>
    -   <span data-ttu-id="6aa94-131">Püsinimi: **NumberSequenceDefaultParameterStartNumber  **</span><span class="sxs-lookup"><span data-stu-id="6aa94-131">Constant name: **NumberSequenceDefaultParameterStartNumber  **</span></span>
    -   <span data-ttu-id="6aa94-132">Vaikeväärtus: 1</span><span class="sxs-lookup"><span data-stu-id="6aa94-132">Default value: 1</span></span>

<span data-ttu-id="6aa94-133">2. valik: **Olemasolev kasutaja määratletud numbriseeria** – see valik võimaldab määratleda täiendamiseks kasutatava numbriseeria.</span><span class="sxs-lookup"><span data-stu-id="6aa94-133">Option 2: **Existing user-defined number sequence** - This option will allow you to define the number sequence to be used for the upgrade.</span></span> <span data-ttu-id="6aa94-134">Kaaluge selle valiku kasutamist, kui vajate täpsemat numbriseeria konfigureerimist.</span><span class="sxs-lookup"><span data-stu-id="6aa94-134">Consider using this option if you need advanced number sequence configuration.</span></span> <span data-ttu-id="6aa94-135">Numbriseeria kasutamiseks peate muutma täiendusklassi ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans järgmise teabega.</span><span class="sxs-lookup"><span data-stu-id="6aa94-135">To use a number sequence, you must modify the upgrade class ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans with the following information:</span></span>

-   <span data-ttu-id="6aa94-136">**Numbriseeria kood** – numbriseeria kood.</span><span class="sxs-lookup"><span data-stu-id="6aa94-136">**Number sequence code** – The code of the number sequence.</span></span>
    -   <span data-ttu-id="6aa94-137">Püsinimi: **NumberSequenceExistingCode **</span><span class="sxs-lookup"><span data-stu-id="6aa94-137">Constant name: **NumberSequenceExistingCode **</span></span>
    -   <span data-ttu-id="6aa94-138">Vaikeväärtus: vaikesäte puudub, seda tuleb värskendada numbriseeria koodi järgi.</span><span class="sxs-lookup"><span data-stu-id="6aa94-138">Default value: No default, this must be updated to the number sequence code.</span></span>
-   <span data-ttu-id="6aa94-139">**Ühiskasutuses numbriseeria** – kahendmuutuja väärtus, et tuvastada numbriseeria ulatus.</span><span class="sxs-lookup"><span data-stu-id="6aa94-139">**Shared number sequence** – A boolean value to identify the scope of the number sequence.</span></span> <span data-ttu-id="6aa94-140">Kasutage kõigis ettevõtetes ühiskasutuses numbriseeriate jaoks „tõene” ja ettevõttespetsiifilise ulatuse jaoks „väär”.</span><span class="sxs-lookup"><span data-stu-id="6aa94-140">Use "true" for shared number sequences across all companies, and "false" for a company-specific scope.</span></span> <span data-ttu-id="6aa94-141">Väärtuse „väär” kasutamisel peab määratud nimega numbriseeria eksisteerima igas ettevõttes, mis sisaldab kulumiraamatu kandeid.</span><span class="sxs-lookup"><span data-stu-id="6aa94-141">When using "false", the number sequence with the specified name must exist in every company that contains depreciation book transactions.</span></span> <span data-ttu-id="6aa94-142">Ühiskasutatud numbriseeriad eksisteerivad igas sektsioonis, mis sisaldab kulumiraamatu kandeid.</span><span class="sxs-lookup"><span data-stu-id="6aa94-142">Shared number sequences exist in every partition that contains depreciation book transactions.</span></span>
    -   <span data-ttu-id="6aa94-143">Püsinimi: **NumberSequenceExistingIsShared **</span><span class="sxs-lookup"><span data-stu-id="6aa94-143">Constant name: **NumberSequenceExistingIsShared **</span></span>
    -   <span data-ttu-id="6aa94-144">Vaikeväärtus: tõene</span><span class="sxs-lookup"><span data-stu-id="6aa94-144">Default value: true</span></span>

<span data-ttu-id="6aa94-145">Parameetrid asuvad klassi ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans alguses.</span><span class="sxs-lookup"><span data-stu-id="6aa94-145">The parameters are located at the beginning of the ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans class.</span></span> 

<span data-ttu-id="6aa94-146">*// Määrake kannete eraldamise eelistatav lähenemisviis* 
*// tõene, kui soovite kasutada olemasoleva numbriseeria koodi* 
*// väär, kui soovite kasutada süsteemi määratletud numbriseeriat (vaikimisi)* const boolean NumberSequenceUseExistingCode = väär;</span><span class="sxs-lookup"><span data-stu-id="6aa94-146">*// Specify a preferable approach of vouchers allocation* 
*// true, if you want to use an existing number sequence code* 
*// false, if you intend to use the system-defined number sequence (default)* const boolean NumberSequenceUseExistingCode = false;</span></span>  

<span data-ttu-id="6aa94-147">*// Süsteemi määratletud numbriseeria lähenemisviisi kasutamisel määrake numbriseeria parameetrid.*
*// Nende parameetritega luuakse uus numbriseeria.*</span><span class="sxs-lookup"><span data-stu-id="6aa94-147">*// If using the system-defined number sequence approach, specify the parameters for the number sequence.*
*// A new number sequence will be created with these parameters.*</span></span> <span data-ttu-id="6aa94-148">const str NumberSequenceDefaultCode = 'FADBUpgr'; const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;</span><span class="sxs-lookup"><span data-stu-id="6aa94-148">const str NumberSequenceDefaultCode = 'FADBUpgr'; const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;</span></span>   

<span data-ttu-id="6aa94-149">*// Olemasoleva numbriseeria lähenemisviisi kasutamisel määrake olemasoleva numbriseeria kood.* 
*// Kande eraldamine läheb olemasoleva numbriseeria puhul rea haaval.*</span><span class="sxs-lookup"><span data-stu-id="6aa94-149">*// If using the existing number sequence approach, specify the existing number sequence code.* 
*// Voucher allocation will go row-by-row for existing number sequences.*</span></span> <span data-ttu-id="6aa94-150">const str NumberSequenceExistingCode = ''; *// Määrake olemasoleva numbriseeria koodi ulatus* 
*// tõene, kui määratud numbriseeria on ühiskasutuses* 
*// väär, kui määratud numbriseeria on ettevõtte kohta* 
*// Vaikimisi süsteemi määratletud numbriseeriat kasutatakse, kui määratud ulatusega numbriseeria koodi ei leita.*</span><span class="sxs-lookup"><span data-stu-id="6aa94-150">const str NumberSequenceExistingCode = ''; *// Specify the scope of the existing number sequence code* 
*// true, if the specified number sequence is shared* 
*// false, if the specified number sequence is per-company* 
*// The default system-defined number sequence will be used if a number sequence code with the specified scope is not found.*</span></span> <span data-ttu-id="6aa94-151">const boolean NumberSequenceExistingIsShared = true;</span><span class="sxs-lookup"><span data-stu-id="6aa94-151">const boolean NumberSequenceExistingIsShared = true;</span></span> 

<span data-ttu-id="6aa94-152">Ehitage uuesti projekt, mis sialdab klassi, kui konstandid on modifitseeritud.</span><span class="sxs-lookup"><span data-stu-id="6aa94-152">Rebuild the project that contains the class after the constants have been modified.</span></span> 

<span data-ttu-id="6aa94-153">Süsteemi loodud numbriseeria lähenemise (1. valik) kasutamisel kasutab täiendamine kogumipõhist töötlemist, et eraldada kande numbrid, nagu on määratud täiendamisskripti parameetrites.</span><span class="sxs-lookup"><span data-stu-id="6aa94-153">When using the system-generated number sequence approach (option 1), the upgrade will use set-based processing to allocate the voucher numbers as specified in the upgrade script parameters.</span></span> <span data-ttu-id="6aa94-154">See loob pärast eraldamist ka määratud parameetritega uue numbriseeria.</span><span class="sxs-lookup"><span data-stu-id="6aa94-154">It will also create a new number sequence with specified parameters after the allocation.</span></span> 

<span data-ttu-id="6aa94-155">Kasutaja määratletud olemasoleva numbriseeria lähenemise (suvand 2) kasutamisel kontrollib täiendus, kas määratud ulatusega numbriseeria on andmebaasis olemas iga kulumiraamatu kannetega sektsiooni ja ettevõtte jaoks.</span><span class="sxs-lookup"><span data-stu-id="6aa94-155">When using the user-defined existing number sequence approach (option 2), the data upgrade checks whether the number sequence with the specified scope exists in the database for each partition and company with depreciation book transactions.</span></span> <span data-ttu-id="6aa94-156">See on olemas, kasutab täiendus rea haaval töötlemist, et eraldada kandenumbrid, nagu on määratud numbriseeriaga, mis kasutab numbriseeria raamistikku.</span><span class="sxs-lookup"><span data-stu-id="6aa94-156">If it does exist, the upgrade will use row-by-row processing to allocate the voucher numbers as specified by the number sequence using the number sequence framework.</span></span> <span data-ttu-id="6aa94-157">Kui määratud ulatusega numbriseeriat ei ole, kasutab täiendus kandenumbrite eraldamiseks süsteemi määratletud numbriseeria vaike-lähenemisviisi ja loob pärast eraldamist määratud vaikeparameetritega uue numbriseeria.</span><span class="sxs-lookup"><span data-stu-id="6aa94-157">If the number sequence does not exist with the specified scope, the upgrade will use the default system-defined number sequence approach to allocate the voucher numbers, and will create a new number sequence with specified default parameters after the allocation.</span></span>

<span data-ttu-id="6aa94-158">Mõlema lähenemisega kasutab andmete täiendamisskript ka numbriseeriat uue pearaamatu töölehe nimedel oleva välja **Voucher series** jaoks, mis on loodud endiste kulumiraamatu töölehenimede jaoks.</span><span class="sxs-lookup"><span data-stu-id="6aa94-158">With either approach, the data upgrade script will also use the number sequence for the **Voucher series** field on the new general ledger journal names created for the former depreciation book journal names.</span></span>




