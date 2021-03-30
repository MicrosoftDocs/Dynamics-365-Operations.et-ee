---
title: Kulumiraamatu täiendamise ülevaade
description: Varasemates väljalasetes on põhivarade jaoks kaks hindamiskontseptsiooni, väärtusmudelid ja kulumiraamatud.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer
ms.reviewer: roschlom
ms.custom: 221624
ms.assetid: cf434099-36f9-4b0f-a7c8-bed091e34f39
ms.search.region: global
ms.author: saraschi
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 016787fa0636b0a3c0d17d2e4fd890cf56d8f519
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241230"
---
# <a name="depreciation-book-upgrade-overview"></a><span data-ttu-id="3f76e-103">Kulumiraamatu uuendamise ülevaade</span><span class="sxs-lookup"><span data-stu-id="3f76e-103">Depreciation book upgrade overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3f76e-104">Varasemates väljalasetes on põhivarade jaoks kaks hindamiskontseptsiooni: väärtusmudelid ja kulumiraamatud.</span><span class="sxs-lookup"><span data-stu-id="3f76e-104">In previous releases, there were two valuation concepts for fixed assets -  value models and depreciation books.</span></span> <span data-ttu-id="3f76e-105">Rakenduses Microsoft Dynamics 365 for Operations (1611) on väärtusmudeli ja kulumiraamatu funktsioonid ühendatud üheks kontseptsiooniks, mis on tuntud kui raamat.</span><span class="sxs-lookup"><span data-stu-id="3f76e-105">In Microsoft Dynamics 365 for Operations (1611), the value model functionality and depreciation book functionality have been merged into a single concept that is known as a book.</span></span> <span data-ttu-id="3f76e-106">Selles teemas antakse mõned asjad, mida täiendamisel arvestada.</span><span class="sxs-lookup"><span data-stu-id="3f76e-106">This topic provides some things to consider for the upgrade.</span></span> 

<span data-ttu-id="3f76e-107">Täiendusprotsess liigutab teie olemasoleva seadistuse ja kõik olemasolevad kanded uude raamatu struktuuri.</span><span class="sxs-lookup"><span data-stu-id="3f76e-107">The upgrade process will move your existing setup and all existing transactions to the new book structure.</span></span> <span data-ttu-id="3f76e-108">Väärtusmudelid jäävad selliseks, nagu need praegu on ehk raamatuks, mis sisestab pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="3f76e-108">Value models will remain as they currently are, as a book that posts to the general ledger.</span></span> <span data-ttu-id="3f76e-109">Kulumiraamatud liigutatakse raamatusse, millel on valik **Pearaamatusse sisestamine** määratud sättele **Ei**.</span><span class="sxs-lookup"><span data-stu-id="3f76e-109">Depreciation books will be moved to a book that has the **Post to general ledger** option set to **No**.</span></span> <span data-ttu-id="3f76e-110">Kulumiraamatu töölehe nimed liigutatakse pearaamatu töölehele, mille nimel on sisestamiskiht määratud sättele **Pole**.</span><span class="sxs-lookup"><span data-stu-id="3f76e-110">Depreciation book journal names will be moved to a general ledger journal name with the posting layer set to **None**.</span></span> <span data-ttu-id="3f76e-111">Kulumiraamatu kanded teisaldatakse jaotisse Põhivara kanded.</span><span class="sxs-lookup"><span data-stu-id="3f76e-111">Depreciation book transactions will be moved to Fixed asset transactions.</span></span> 

<span data-ttu-id="3f76e-112">Enne andmete täiendamise käivitamist peate mõistma kahte suvandit, mis on saadaval kulumiraamatu tööleheridade täiendamiseks kanneteks, ja numbriseeriat, mida kasutatakse kande seeria jaoks.</span><span class="sxs-lookup"><span data-stu-id="3f76e-112">Before running the data upgrade, you should understand the two options available for upgrading depreciation book journal lines to transaction vouchers, and the number sequence that will be used for the voucher series.</span></span> 

<span data-ttu-id="3f76e-113">Suvand 1:  **Süsteemi määratletud numbriseeria** – see on vaikesuvand täiendamise jõudluse optimeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="3f76e-113">Option 1:  **System-defined number sequence** - This is the default option to optimize upgrade performance.</span></span> <span data-ttu-id="3f76e-114">Täiendamine ei kasutada numbriseeriate raamistikku, vaid eraldab selleasemel kanded kogumipõhise lähenemisega.</span><span class="sxs-lookup"><span data-stu-id="3f76e-114">The upgrade will not use the number sequences framework, but instead will allocate vouchers with a set-based approach.</span></span> <span data-ttu-id="3f76e-115">Pärast täiendamist luuakse uus numbriseeria, mille parameeter **Järgmine numbrikomplekt** põhineb asjakohaselt täiendatud kandel.</span><span class="sxs-lookup"><span data-stu-id="3f76e-115">After the upgrade, the new number sequence will be created with the **Next number set** appropriately based on the upgraded transactions.</span></span> <span data-ttu-id="3f76e-116">Vaikimisi on kasutatava numbriseeria vorming FADBUpgr\#\#\#\#\#\#\#\#\#.</span><span class="sxs-lookup"><span data-stu-id="3f76e-116">By default, the number sequence used will be in the FADBUpgr\#\#\#\#\#\#\#\#\# format.</span></span> <span data-ttu-id="3f76e-117">Seda lähenemist kasutades saate vormingut korrigeerida järgmiste parameetrite abil.</span><span class="sxs-lookup"><span data-stu-id="3f76e-117">There are a few parameters available to you to adjust the format when using this approach:</span></span>

-   <span data-ttu-id="3f76e-118">**Numbriseeria kood** – kood numbriseeria tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="3f76e-118">**Number sequence code** – The code to identify the number sequence.</span></span> <span data-ttu-id="3f76e-119">Seda numbriseeria koodi ei saa eksisteerida, kuna see luuakse täiendamisega.</span><span class="sxs-lookup"><span data-stu-id="3f76e-119">This number sequence code cannot exist since it will be created by the upgrade.</span></span>
    -   <span data-ttu-id="3f76e-120">Püsinimi: **NumberSequenceDefaultCode**</span><span class="sxs-lookup"><span data-stu-id="3f76e-120">Constant name: **NumberSequenceDefaultCode**</span></span>
    -   <span data-ttu-id="3f76e-121">Vaikeväärtus: "FADBUpgr"</span><span class="sxs-lookup"><span data-stu-id="3f76e-121">Default value: "FADBUpgr"</span></span>
-   <span data-ttu-id="3f76e-122">**Eesliide** – püsistringi väärtus, mida kasutatakse kande numbrite jaoks eesliitena.</span><span class="sxs-lookup"><span data-stu-id="3f76e-122">**Prefix** – The constant string value that will be used as a prefix for the voucher numbers.</span></span>
    -   <span data-ttu-id="3f76e-123">Püsinimi: **NumberSequenceDefaultParameterPrefix**</span><span class="sxs-lookup"><span data-stu-id="3f76e-123">Constant name: **NumberSequenceDefaultParameterPrefix**</span></span>
    -   <span data-ttu-id="3f76e-124">Vaikeväärtus: "FADBUpgr"</span><span class="sxs-lookup"><span data-stu-id="3f76e-124">Default value: "FADBUpgr"</span></span>
-   <span data-ttu-id="3f76e-125">**Tähtnumbriline pikkus** – numbriseeria tähtnumbrilise segmendi pikkus.</span><span class="sxs-lookup"><span data-stu-id="3f76e-125">**Alphanumeric length** – The length of the alphanumeric segment of the number sequence.</span></span>
    -   <span data-ttu-id="3f76e-126">Püsinimi: \*\*NumberSequenceDefaultParameterAlpanumericLength \*\*</span><span class="sxs-lookup"><span data-stu-id="3f76e-126">Constant name: \*\*NumberSequenceDefaultParameterAlpanumericLength \*\*</span></span>
    -   <span data-ttu-id="3f76e-127">Vaikeväärtus: 9</span><span class="sxs-lookup"><span data-stu-id="3f76e-127">Default value: 9</span></span>
-   <span data-ttu-id="3f76e-128">**Algusnumber** – esimene numbriseerias kasutatav number.</span><span class="sxs-lookup"><span data-stu-id="3f76e-128">**Start number** - The first number to be used in the number sequence.</span></span>
    -   <span data-ttu-id="3f76e-129">Püsinimi: \*\*NumberSequenceDefaultParameterStartNumber \*\*</span><span class="sxs-lookup"><span data-stu-id="3f76e-129">Constant name: \*\*NumberSequenceDefaultParameterStartNumber  \*\*</span></span>
    -   <span data-ttu-id="3f76e-130">Vaikeväärtus: 1</span><span class="sxs-lookup"><span data-stu-id="3f76e-130">Default value: 1</span></span>

<span data-ttu-id="3f76e-131">2. valik: **Olemasolev kasutaja määratletud numbriseeria** – see valik võimaldab määratleda täiendamiseks kasutatava numbriseeria.</span><span class="sxs-lookup"><span data-stu-id="3f76e-131">Option 2: **Existing user-defined number sequence** - This option will allow you to define the number sequence to be used for the upgrade.</span></span> <span data-ttu-id="3f76e-132">Kaaluge selle valiku kasutamist, kui vajate täpsemat numbriseeria konfigureerimist.</span><span class="sxs-lookup"><span data-stu-id="3f76e-132">Consider using this option if you need advanced number sequence configuration.</span></span> <span data-ttu-id="3f76e-133">Numbriseeria kasutamiseks peate muutma täiendusklassi ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans järgmise teabega.</span><span class="sxs-lookup"><span data-stu-id="3f76e-133">To use a number sequence, you must modify the upgrade class ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans with the following information:</span></span>

-   <span data-ttu-id="3f76e-134">**Numbriseeria kood** – numbriseeria kood.</span><span class="sxs-lookup"><span data-stu-id="3f76e-134">**Number sequence code** – The code of the number sequence.</span></span>
    -   <span data-ttu-id="3f76e-135">Püsinimi: \*\*NumberSequenceExistingCode \*\*</span><span class="sxs-lookup"><span data-stu-id="3f76e-135">Constant name: \*\*NumberSequenceExistingCode \*\*</span></span>
    -   <span data-ttu-id="3f76e-136">Vaikeväärtus: vaikesäte puudub, seda tuleb värskendada numbriseeria koodi järgi.</span><span class="sxs-lookup"><span data-stu-id="3f76e-136">Default value: No default, this must be updated to the number sequence code.</span></span>
-   <span data-ttu-id="3f76e-137">**Ühiskasutuses numbriseeria** – kahendmuutuja väärtus, et tuvastada numbriseeria ulatus.</span><span class="sxs-lookup"><span data-stu-id="3f76e-137">**Shared number sequence** – A boolean value to identify the scope of the number sequence.</span></span> <span data-ttu-id="3f76e-138">Kasutage kõigis ettevõtetes ühiskasutuses numbriseeriate jaoks „tõene” ja ettevõttespetsiifilise ulatuse jaoks „väär”.</span><span class="sxs-lookup"><span data-stu-id="3f76e-138">Use "true" for shared number sequences across all companies, and "false" for a company-specific scope.</span></span> <span data-ttu-id="3f76e-139">Väärtuse „väär” kasutamisel peab määratud nimega numbriseeria eksisteerima igas ettevõttes, mis sisaldab kulumiraamatu kandeid.</span><span class="sxs-lookup"><span data-stu-id="3f76e-139">When using "false", the number sequence with the specified name must exist in every company that contains depreciation book transactions.</span></span> <span data-ttu-id="3f76e-140">Ühiskasutatud numbriseeriad eksisteerivad igas sektsioonis, mis sisaldab kulumiraamatu kandeid.</span><span class="sxs-lookup"><span data-stu-id="3f76e-140">Shared number sequences exist in every partition that contains depreciation book transactions.</span></span>
    -   <span data-ttu-id="3f76e-141">Püsinimi: \*\*NumberSequenceExistingIsShared \*\*</span><span class="sxs-lookup"><span data-stu-id="3f76e-141">Constant name: \*\*NumberSequenceExistingIsShared \*\*</span></span>
    -   <span data-ttu-id="3f76e-142">Vaikeväärtus: tõene</span><span class="sxs-lookup"><span data-stu-id="3f76e-142">Default value: true</span></span>

<span data-ttu-id="3f76e-143">Parameetrid asuvad klassi ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans alguses.</span><span class="sxs-lookup"><span data-stu-id="3f76e-143">The parameters are located at the beginning of the ReleaseUpdateDB70\_FixedAssetJournalDepBookRemovalDepBookJournalTrans class.</span></span> 

<span data-ttu-id="3f76e-144">*// Määrake kannete eraldamise eelistatav lähenemisviis* 
 *// tõene, kui soovite kasutada olemasoleva numbriseeria koodi* 
 *// väär, kui soovite kasutada süsteemi määratletud numbriseeriat (vaikimisi)* const boolean NumberSequenceUseExistingCode = väär;</span><span class="sxs-lookup"><span data-stu-id="3f76e-144">*// Specify a preferable approach of vouchers allocation* 
 *// true, if you want to use an existing number sequence code* 
 *// false, if you intend to use the system-defined number sequence (default)* const boolean NumberSequenceUseExistingCode = false;</span></span>  

<span data-ttu-id="3f76e-145">*// Süsteemi määratletud numbriseeria lähenemisviisi kasutamisel määrake numbriseeria parameetrid.*
 *// Nende parameetritega luuakse uus numbriseeria.*</span><span class="sxs-lookup"><span data-stu-id="3f76e-145">*// If using the system-defined number sequence approach, specify the parameters for the number sequence.*
 *// A new number sequence will be created with these parameters.*</span></span> <span data-ttu-id="3f76e-146">const str NumberSequenceDefaultCode = 'FADBUpgr'; const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;</span><span class="sxs-lookup"><span data-stu-id="3f76e-146">const str NumberSequenceDefaultCode = 'FADBUpgr'; const str NumberSequenceDefaultParameterPrefix = 'FADBUpgr'; const int NumberSequenceDefaultParameterAlpanumericLength = 9; const int NumberSequenceDefaultParameterStartNumber = 1;</span></span>   

<span data-ttu-id="3f76e-147">*// Olemasoleva numbriseeria lähenemisviisi kasutamisel määrake olemasoleva numbriseeria kood.* 
 *// Kande eraldamine läheb olemasoleva numbriseeria puhul rea haaval.*</span><span class="sxs-lookup"><span data-stu-id="3f76e-147">*// If using the existing number sequence approach, specify the existing number sequence code.* 
 *// Voucher allocation will go row-by-row for existing number sequences.*</span></span> <span data-ttu-id="3f76e-148">const str NumberSequenceExistingCode = ''; *// Määrake olemasoleva numbriseeria koodi ulatus* 
 *// tõene, kui määratud numbriseeria on ühiskasutuses* 
 *// väär, kui määratud numbriseeria on ettevõtte kohta* 
 *// Vaikimisi süsteemi määratletud numbriseeriat kasutatakse, kui määratud ulatusega numbriseeria koodi ei leita.*</span><span class="sxs-lookup"><span data-stu-id="3f76e-148">const str NumberSequenceExistingCode = ''; *// Specify the scope of the existing number sequence code* 
 *// true, if the specified number sequence is shared* 
 *// false, if the specified number sequence is per-company* 
 *// The default system-defined number sequence will be used if a number sequence code with the specified scope is not found.*</span></span> <span data-ttu-id="3f76e-149">const boolean NumberSequenceExistingIsShared = true;</span><span class="sxs-lookup"><span data-stu-id="3f76e-149">const boolean NumberSequenceExistingIsShared = true;</span></span> 

<span data-ttu-id="3f76e-150">Ehitage uuesti projekt, mis sialdab klassi, kui konstandid on modifitseeritud.</span><span class="sxs-lookup"><span data-stu-id="3f76e-150">Rebuild the project that contains the class after the constants have been modified.</span></span> 

<span data-ttu-id="3f76e-151">Süsteemi loodud numbriseeria lähenemise (1. valik) kasutamisel kasutab täiendamine kogumipõhist töötlemist, et eraldada kande numbrid, nagu on määratud täiendamisskripti parameetrites.</span><span class="sxs-lookup"><span data-stu-id="3f76e-151">When using the system-generated number sequence approach (option 1), the upgrade will use set-based processing to allocate the voucher numbers as specified in the upgrade script parameters.</span></span> <span data-ttu-id="3f76e-152">See loob pärast eraldamist ka määratud parameetritega uue numbriseeria.</span><span class="sxs-lookup"><span data-stu-id="3f76e-152">It will also create a new number sequence with specified parameters after the allocation.</span></span> 

<span data-ttu-id="3f76e-153">Kasutaja määratletud olemasoleva numbriseeria lähenemise (suvand 2) kasutamisel kontrollib täiendus, kas määratud ulatusega numbriseeria on andmebaasis olemas iga kulumiraamatu kannetega sektsiooni ja ettevõtte jaoks.</span><span class="sxs-lookup"><span data-stu-id="3f76e-153">When using the user-defined existing number sequence approach (option 2), the data upgrade checks whether the number sequence with the specified scope exists in the database for each partition and company with depreciation book transactions.</span></span> <span data-ttu-id="3f76e-154">See on olemas, kasutab täiendus rea haaval töötlemist, et eraldada kandenumbrid, nagu on määratud numbriseeriaga, mis kasutab numbriseeria raamistikku.</span><span class="sxs-lookup"><span data-stu-id="3f76e-154">If it does exist, the upgrade will use row-by-row processing to allocate the voucher numbers as specified by the number sequence using the number sequence framework.</span></span> <span data-ttu-id="3f76e-155">Kui määratud ulatusega numbriseeriat ei ole, kasutab täiendus kandenumbrite eraldamiseks süsteemi määratletud numbriseeria vaike-lähenemisviisi ja loob pärast eraldamist määratud vaikeparameetritega uue numbriseeria.</span><span class="sxs-lookup"><span data-stu-id="3f76e-155">If the number sequence does not exist with the specified scope, the upgrade will use the default system-defined number sequence approach to allocate the voucher numbers, and will create a new number sequence with specified default parameters after the allocation.</span></span>

<span data-ttu-id="3f76e-156">Mõlema lähenemisega kasutab andmete täiendamisskript ka numbriseeriat uue pearaamatu töölehe nimedel oleva välja **Voucher series** jaoks, mis on loodud endiste kulumiraamatu töölehenimede jaoks.</span><span class="sxs-lookup"><span data-stu-id="3f76e-156">With either approach, the data upgrade script will also use the number sequence for the **Voucher series** field on the new general ledger journal names created for the former depreciation book journal names.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]