---
title: Maksekviitungi vormingu seadistamine projektiarvete jaoks
description: Ettevõtted kinnitavad sageli arvetele prinditud maksekviitungeid, et aidata kliente ja pakkuda sisestamise ja tasakaalustamise jaoks makseviidet.
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMLegalEntity, CustFormletterParameters
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4671e1df3bc86361736b5882d67e6b160b4c5644
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174833"
---
# <a name="set-up-payment-slip-format-for-project-invoices"></a><span data-ttu-id="503c5-103">Maksekviitungi vormingu seadistamine projektiarvete jaoks</span><span class="sxs-lookup"><span data-stu-id="503c5-103">Set up payment slip format for project invoices</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="503c5-104">Ettevõtted kinnitavad sageli arvetele prinditud maksekviitungeid, et aidata kliente ja pakkuda sisestamise ja tasakaalustamise jaoks makseviidet.</span><span class="sxs-lookup"><span data-stu-id="503c5-104">Businesses commonly attach printed payment slips to invoices to assist customers and provide a payment reference for posting and settlement.</span></span> <span data-ttu-id="503c5-105">Maksekviitungit saab lisaks müügiarvetele ja vabas vormis arvetele kasutada projekti ja teenuse arvete, märgukirjade, viivisearvete, kontoväljavõtete jaoks.</span><span class="sxs-lookup"><span data-stu-id="503c5-105">The payment slip can be used for project or service invoices, collection letters, interest notes, and account statements, in addition to sales invoices and free text invoices.</span></span> <span data-ttu-id="503c5-106">Maksekviitungite töötlemiseks seadistage esmalt oma kreeditori ID-number ja maksekviitungi manuste vormingud.</span><span class="sxs-lookup"><span data-stu-id="503c5-106">To process payment slips, first set up your creditor identification number and payment slip attachment formats.</span></span>

<span data-ttu-id="503c5-107">See protsess kasutab demoettevõtte DEMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="503c5-107">This procedure uses the DEMF demo company.</span></span> 

<span data-ttu-id="503c5-108">See funktsionaalsus on saadaval ainult juriidilistele isikutele, kelle esmane aadress on Taanis.</span><span class="sxs-lookup"><span data-stu-id="503c5-108">This functionality is available for legal entities whose primary address is in Denmark.</span></span>


## <a name="set-up-a-creditor-id-number"></a><span data-ttu-id="503c5-109">Kreeditori ID-numbri seadistamine</span><span class="sxs-lookup"><span data-stu-id="503c5-109">Set up a creditor ID number</span></span>
1. <span data-ttu-id="503c5-110">Avage Organisatsiooni haldus > Organisatsioonid > Juriidilised isikud.</span><span class="sxs-lookup"><span data-stu-id="503c5-110">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="503c5-111">Laiendage või ahendage jaotist Pangakonto teave.</span><span class="sxs-lookup"><span data-stu-id="503c5-111">Expand or collapse the Bank account information section.</span></span>
3. <span data-ttu-id="503c5-112">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="503c5-112">Click Edit.</span></span>
4. <span data-ttu-id="503c5-113">Sisestage väärtus väljale FI-kreeditor.</span><span class="sxs-lookup"><span data-stu-id="503c5-113">In the FI-Creditor ID field, type a value.</span></span>
5. <span data-ttu-id="503c5-114">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="503c5-114">Click Save.</span></span>
6. <span data-ttu-id="503c5-115">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="503c5-115">Close the page.</span></span>

## <a name="set-up-a-payment-slip-format-for-invoices-notes-letters-and-statements"></a><span data-ttu-id="503c5-116">Maksekviitungi vormingu seadistamine arvete, märkmete, kirjade ja väljavõtete jaoks.</span><span class="sxs-lookup"><span data-stu-id="503c5-116">Set up a payment slip format for invoices, notes, letters, and statements</span></span>
1. <span data-ttu-id="503c5-117">Minge jaotisse Müügireskontro > Seadistus > Vormid > Vormi seadistus.</span><span class="sxs-lookup"><span data-stu-id="503c5-117">Go to Accounts receivable > Setup > Forms > Form setup.</span></span>
2. <span data-ttu-id="503c5-118">Klõpsake vahekaarti Arve.</span><span class="sxs-lookup"><span data-stu-id="503c5-118">Click the Invoice tab.</span></span>
3. <span data-ttu-id="503c5-119">Valige suvand väljal Seotud maksemanus kliendiarvel.</span><span class="sxs-lookup"><span data-stu-id="503c5-119">In the Associated payment attachment on customer invoice field, select an option.</span></span>
    * <span data-ttu-id="503c5-120">Puudub: maksekviitungit ei prindita.</span><span class="sxs-lookup"><span data-stu-id="503c5-120">None – Do not print a payment slip.</span></span> <span data-ttu-id="503c5-121">Valige see suvand, kui maksesumma on muus valuutas kui Taani kroon (DKK).</span><span class="sxs-lookup"><span data-stu-id="503c5-121">Choose this option if the payment amount is in a currency other than Danish kroner (DKK).</span></span>   <span data-ttu-id="503c5-122">FIK 751: saate printida FIK 751 maksekviitungi, kui kavatsete maksesumma ja tähtaja maksekviitungile käsitsi kirjutada.</span><span class="sxs-lookup"><span data-stu-id="503c5-122">FIK 751 – Print an FIK 751 payment slip if you intend to manually write the payment amount and due date on the payment slip.</span></span>   <span data-ttu-id="503c5-123">FIK 752: saate printida FIK 752 maksekviitungi, kui kavatsete kasutada arvuti genereeritud maksekviitungit, millel on eelprinditud maksesumma ja tähtaeg.</span><span class="sxs-lookup"><span data-stu-id="503c5-123">FIK 752 – Print an FIK 752 payment slip if you intend to use a computer-generated payment slip with a preprinted payment amount and due date.</span></span>  
4. <span data-ttu-id="503c5-124">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="503c5-124">Click Save.</span></span>
5. <span data-ttu-id="503c5-125">Klõpsake vahekaarti Vabas vormis arve.</span><span class="sxs-lookup"><span data-stu-id="503c5-125">Click the Free text invoice tab.</span></span>
6. <span data-ttu-id="503c5-126">Valige suvand väljal Seotud maksemanus vabas vormis arvel.</span><span class="sxs-lookup"><span data-stu-id="503c5-126">In the Associated payment attachment on free text invoice field, select an option.</span></span>
    * <span data-ttu-id="503c5-127">Puudub: maksekviitungit ei prindita.</span><span class="sxs-lookup"><span data-stu-id="503c5-127">None – Do not print a payment slip.</span></span> <span data-ttu-id="503c5-128">Valige see suvand, kui maksesumma on muus valuutas kui Taani kroon (DKK).</span><span class="sxs-lookup"><span data-stu-id="503c5-128">Choose this option if the payment amount is in a currency other than Danish kroner (DKK).</span></span>   <span data-ttu-id="503c5-129">FIK 751: saate printida FIK 751 maksekviitungi, kui kavatsete maksesumma ja tähtaja maksekviitungile käsitsi kirjutada.</span><span class="sxs-lookup"><span data-stu-id="503c5-129">FIK 751 – Print an FIK 751 payment slip if you intend to write the payment amount and due date on the payment slip manually.</span></span>   <span data-ttu-id="503c5-130">FIK 752: saate printida FIK 752 maksekviitungi, kui kavatsete kasutada arvuti genereeritud maksekviitungit, millel on eelprinditud maksesumma ja tähtaeg.</span><span class="sxs-lookup"><span data-stu-id="503c5-130">FIK 752 – Print an FIK 752 payment slip if you intend to use a computer-generated payment slip with a preprinted payment amount and due date.</span></span>  
7. <span data-ttu-id="503c5-131">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="503c5-131">Click Save.</span></span>
8. <span data-ttu-id="503c5-132">Klõpsake vahekaarti Viivisearve.</span><span class="sxs-lookup"><span data-stu-id="503c5-132">Click the Interest note tab.</span></span>
9. <span data-ttu-id="503c5-133">Valige suvand väljal Seotud maksemanus viivisearvel.</span><span class="sxs-lookup"><span data-stu-id="503c5-133">In the Associated payment attachment on interest note field, select an option.</span></span>
    * <span data-ttu-id="503c5-134">Puudub: maksekviitungit ei prindita.</span><span class="sxs-lookup"><span data-stu-id="503c5-134">None – Do not print a payment slip.</span></span> <span data-ttu-id="503c5-135">Valige see suvand, kui maksesumma on muus valuutas kui Taani kroon (DKK).</span><span class="sxs-lookup"><span data-stu-id="503c5-135">Choose this option if the payment amount is in a currency other than Danish kroner (DKK).</span></span>   <span data-ttu-id="503c5-136">FIK 751: saate printida FIK 751 maksekviitungi, kui kavatsete maksesumma ja tähtaja maksekviitungile käsitsi kirjutada.</span><span class="sxs-lookup"><span data-stu-id="503c5-136">FIK 751 – Print an FIK 751 payment slip if you intend to write the payment amount and due date on the payment slip manually.</span></span>   <span data-ttu-id="503c5-137">FIK 752: saate printida FIK 752 maksekviitungi, kui kavatsete kasutada arvuti genereeritud maksekviitungit, millel on eelprinditud maksesumma ja tähtaeg.</span><span class="sxs-lookup"><span data-stu-id="503c5-137">FIK 752 – Print an FIK 752 payment slip if you intend to use a computer-generated payment slip with a preprinted payment amount and due date.</span></span>  
10. <span data-ttu-id="503c5-138">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="503c5-138">Click Save.</span></span>
11. <span data-ttu-id="503c5-139">Klõpsake vahekaarti Märgukiri.</span><span class="sxs-lookup"><span data-stu-id="503c5-139">Click the Collection letter tab.</span></span>
12. <span data-ttu-id="503c5-140">Valige suvand väljal Seotud maksemanus märgukirjal.</span><span class="sxs-lookup"><span data-stu-id="503c5-140">In the Associated payment attachment on collection letter field, select an option.</span></span>
    * <span data-ttu-id="503c5-141">Puudub: maksekviitungit ei prindita.</span><span class="sxs-lookup"><span data-stu-id="503c5-141">None – Do not print a payment slip.</span></span> <span data-ttu-id="503c5-142">Valige see suvand, kui maksesumma on muus valuutas kui Taani kroon (DKK).</span><span class="sxs-lookup"><span data-stu-id="503c5-142">Choose this option if the payment amount is in a currency other than Danish kroner (DKK).</span></span>   <span data-ttu-id="503c5-143">FIK 751: saate printida FIK 751 maksekviitungi, kui kavatsete maksesumma ja tähtaja maksekviitungile käsitsi kirjutada.</span><span class="sxs-lookup"><span data-stu-id="503c5-143">FIK 751 – Print an FIK 751 payment slip if you intend to write the payment amount and due date on the payment slip manually.</span></span>   <span data-ttu-id="503c5-144">FIK 752: saate printida FIK 752 maksekviitungi, kui kavatsete kasutada arvuti genereeritud maksekviitungit, millel on eelprinditud maksesumma ja tähtaeg.</span><span class="sxs-lookup"><span data-stu-id="503c5-144">FIK 752 – Print an FIK 752 payment slip if you intend to use a computer-generated payment slip with a preprinted payment amount and due date.</span></span>  
13. <span data-ttu-id="503c5-145">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="503c5-145">Click Save.</span></span>
14. <span data-ttu-id="503c5-146">Klõpsake vahekaarti Kontoväljavõte.</span><span class="sxs-lookup"><span data-stu-id="503c5-146">Click the Account statement tab.</span></span>
15. <span data-ttu-id="503c5-147">Valige suvand väljal Seotud maksemanus kontoväljavõttel.</span><span class="sxs-lookup"><span data-stu-id="503c5-147">In the Associated payment attachment on account statement field, select an option.</span></span>
    * <span data-ttu-id="503c5-148">Puudub: maksekviitungit ei prindita.</span><span class="sxs-lookup"><span data-stu-id="503c5-148">None – Do not print a payment slip.</span></span> <span data-ttu-id="503c5-149">Valige see suvand, kui maksesumma on muus valuutas kui Taani kroon (DKK).</span><span class="sxs-lookup"><span data-stu-id="503c5-149">Choose this option if the payment amount is in a currency other than Danish kroner (DKK).</span></span>   <span data-ttu-id="503c5-150">FIK 751: saate printida FIK 751 maksekviitungi, kui kavatsete maksesumma ja tähtaja maksekviitungile käsitsi kirjutada.</span><span class="sxs-lookup"><span data-stu-id="503c5-150">FIK 751 – Print an FIK 751 payment slip if you intend to write the payment amount and due date on the payment slip manually.</span></span>   <span data-ttu-id="503c5-151">FIK 752: saate printida FIK 752 maksekviitungi, kui kavatsete kasutada arvuti genereeritud maksekviitungit, millel on eelprinditud maksesumma ja tähtaeg.</span><span class="sxs-lookup"><span data-stu-id="503c5-151">FIK 752 – Print an FIK 752 payment slip if you intend to use a computer-generated payment slip with a preprinted payment amount and due date.</span></span>  
16. <span data-ttu-id="503c5-152">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="503c5-152">Click Save.</span></span>
17. <span data-ttu-id="503c5-153">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="503c5-153">Close the page.</span></span>
