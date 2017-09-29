---
title: "Hilisema kuupäevaga dateeritud tšekid"
description: "Selles artiklis antakse teavet hilisema kuupäevaga tšekkide toe kohta Microsoft Dynamics 365 for Finance and Operations, Enterprise editionis. Hilisema kuupäevaga dateeritud tšekid on tšekid, mis väljastatakse tulevasel kuupäeval maksete tegemise ja vastuvõtmise eesmärgil. Seetõttu ei saa tšekki enne määratud kuupäeva sularahaks vahetada."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 45d28110ca93875eb534c69886ac2074ea4fe737
ms.openlocfilehash: 6a535b5f1192b7c27383cb8ece53f76a9c76f047
ms.contentlocale: et-ee
ms.lasthandoff: 08/09/2017

---

# <a name="postdated-checks"></a><span data-ttu-id="efc39-105">Hilisema kuupäevaga dateeritud tšekid</span><span class="sxs-lookup"><span data-stu-id="efc39-105">Postdated checks</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="efc39-106">Selles artiklis antakse teavet hilisema kuupäevaga tšekkide toe kohta Microsoft Dynamics 365 for Finance and Operations, Enterprise editionis.</span><span class="sxs-lookup"><span data-stu-id="efc39-106">This article provides information about support for postdated checks in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> <span data-ttu-id="efc39-107">Hilisema kuupäevaga dateeritud tšekid on tšekid, mis väljastatakse tulevasel kuupäeval maksete tegemise ja vastuvõtmise eesmärgil.</span><span class="sxs-lookup"><span data-stu-id="efc39-107">Postdated checks are checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="efc39-108">Seetõttu ei saa tšekki enne määratud kuupäeva sularahaks vahetada.</span><span class="sxs-lookup"><span data-stu-id="efc39-108">Therefore, the check can't be cashed until the specified date.</span></span>

<span data-ttu-id="efc39-109">Microsoft Dynamics 365 for Finance and Operations toetab hilisema kuupäevaga dateeritud tšekkide täielikku haldustsüklit nii müügireskontros kui ka ostureskontros, nagu on näidatud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="efc39-109">Microsoft Dynamics 365 for Finance and Operations supports the full management cycle for postdated checks in both Accounts receivable and Accounts payable, as shown in the following table.</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="efc39-110">Stsenaarium</span><span class="sxs-lookup"><span data-stu-id="efc39-110">Scenario</span></span></th>
<th><span data-ttu-id="efc39-111">Üksikasjad</span><span class="sxs-lookup"><span data-stu-id="efc39-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="efc39-112">Hilisema kuupäevaga tšekkide seadistamine</span><span class="sxs-lookup"><span data-stu-id="efc39-112">Set up postdated checks</span></span></td>
<td><span data-ttu-id="efc39-113">Peate seadistama uue makseviisi ja määrama makserutiini väljastatud tšekkide, vastuvõetud tšekkide ja kinnipeetava maksu kliiringukontodele.</span><span class="sxs-lookup"><span data-stu-id="efc39-113">You must set up a new payment method, and specify the payment routine for clearing accounts for issued checks, received checks, and withholding tax.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efc39-114">Registreeri ja postita hankija hilisema kuupäevaga tšekk</span><span class="sxs-lookup"><span data-stu-id="efc39-114">Register and post a postdated check for a vendor</span></span></td>
<td><span data-ttu-id="efc39-115">Registreerige hankijale väljastatava hilisema kuupäevaga tšeki üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="efc39-115">Register the details of a postdated check that you issue to a vendor.</span></span> <span data-ttu-id="efc39-116">Kui makse on sisestatud, siis tuvastatakse hankija kohustus, kuid pangakonto ei ole veel krediteeritud.</span><span class="sxs-lookup"><span data-stu-id="efc39-116">When the payment is posted, the vendor liability is recognized, but the bank account isn’t yet credit.</span></span> <span data-ttu-id="efc39-117">Selle asemel kasutatakse selleks kliiringukontot.</span><span class="sxs-lookup"><span data-stu-id="efc39-117">Instead, a clearing account is used for this purpose.</span></span> </td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efc39-118">Kliendi hilisema kuupäevaga tšeki registreerimine ja postitamine</span><span class="sxs-lookup"><span data-stu-id="efc39-118">Register and post a postdated check for a customer</span></span></td>
<td><span data-ttu-id="efc39-119">Regitreerige kliendilt saadud hilisema kuupäevaga tšeki üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="efc39-119">Register the details of a postdated check that you receive from a customer.</span></span> <span data-ttu-id="efc39-120">Kui makse on sisestatud, siis on kliendi nõue krediteeritud, kuid pangakontot ei ole veel debiteeritud.</span><span class="sxs-lookup"><span data-stu-id="efc39-120">When the payment is posted, the customer receivable is credit, but the bank account isn’t yet debit.</span></span> <span data-ttu-id="efc39-121">Selle asemel kasutatakse selleks kliiringukontot.</span><span class="sxs-lookup"><span data-stu-id="efc39-121">Instead, a clearing account is used for this purpose.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efc39-122">Registreerige ja postitage kliendi või hankija hilisema kuupäevaga asendustšekk.</span><span class="sxs-lookup"><span data-stu-id="efc39-122">Register and post a replacement postdated check for a customer or a vendor</span></span></td>
<td>
<span data-ttu-id="efc39-123">Kui teie algne tšekk hankijale või kliendilt on kadunud või kahjustatud, siis saate hankijale väljastada hilise kuupäevaga dateeritud asendustšeki.</span><span class="sxs-lookup"><span data-stu-id="efc39-123">If your original check to a vendor or from a customer is lost or damaged, you can issue a replacement postdated check.</span></span> <span data-ttu-id="efc39-124">Tšeki üksikasjade registreerimisel lisage viide esialgsele tšekile ja näidake, et uus tšekk on originaali asendaja.</span><span class="sxs-lookup"><span data-stu-id="efc39-124">When you register the check details, provide a reference to the original check, and indicate that the new check is a replacement for the original.</span></span> <span data-ttu-id="efc39-125">Asendustšeki saate ka sisestada.</span><span class="sxs-lookup"><span data-stu-id="efc39-125">You can also post the replacement check.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efc39-126">Kliendi hilisema kuupäevaga tšeki ülekandmine hankijale</span><span class="sxs-lookup"><span data-stu-id="efc39-126">Transfer a customer postdated check to a vendor</span></span></td>
<td><span data-ttu-id="efc39-127">Kui saate kliendilt hilisema kuupäevaga dateeritud tšeki, saate tšeki hankijale maksena üle kanda.</span><span class="sxs-lookup"><span data-stu-id="efc39-127">When you receive a postdated check from a customer, you can transfer that check to a vendor as a payment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="efc39-128">Kliendi või hankija hilisema kuupäevaga tšeki tasakaalustamine</span><span class="sxs-lookup"><span data-stu-id="efc39-128">Settle a postdated check for a customer or a vendor</span></span></td>
<td><span data-ttu-id="efc39-129">Tasakaalustage hilise kuupäevaga tšekk, mis sisestatakse kliendi või hankija vahekontole, kui tšekk lõpuks valmis on.</span><span class="sxs-lookup"><span data-stu-id="efc39-129">Settle a postdated check that is posted to a bridging account for a customer or a vendor when the check finally matures.</span></span> <span data-ttu-id="efc39-130">Tšeki tasakaalustamisel pank lõpuks debiteerib või krediteerib varem kasutatud kliiringukonto.</span><span class="sxs-lookup"><span data-stu-id="efc39-130">When the check is settled, the bank is finally debit or credit against the clearing account that was used earlier.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="efc39-131">Hankija hilisema kuupäevaga tšeki tühistamine</span><span class="sxs-lookup"><span data-stu-id="efc39-131">Cancel a postdated check for a vendor</span></span></td>
<td><span data-ttu-id="efc39-132">Sisestatud hilisema kuupäevaga tšeki saate tühistada järgmistes olukordades. - Pank tagastab tšeki.</span><span class="sxs-lookup"><span data-stu-id="efc39-132">You can cancel a posted postdated check in these situations: - The check is returned by the bank.</span></span>
<span data-ttu-id="efc39-133">- Tšekk on rakendatud valele arvele.</span><span class="sxs-lookup"><span data-stu-id="efc39-133">- The check is applied to an incorrect invoice.</span></span>
<span data-ttu-id="efc39-134">- Tšeki põhjal tehakse sularahamakse.</span><span class="sxs-lookup"><span data-stu-id="efc39-134">- A cash payment is made against the check.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="efc39-135">Hilisema kuupäevaga tšeki makse peatamine</span><span class="sxs-lookup"><span data-stu-id="efc39-135">Stop payment for a postdated check</span></span></td>
<td><span data-ttu-id="efc39-136">Saate peatada hankijale väljastatud hilisema kuupäevaga dateeritud tšeki põhjustel, nagu ebapiisavad vahendid, muudatused hankijaga sõlmitud lepingu tingimustes, hankija tarnitud defektsed kaubad või kaupade tagastamine hankijale.</span><span class="sxs-lookup"><span data-stu-id="efc39-136">You can stop payment on a postdated check that was issued to a vendor, for reasons such as not sufficient funds, changes in the terms of the agreement with the vendor, supply of defective goods by the vendor, or return of goods to the vendor.</span></span> <span data-ttu-id="efc39-137">Makse saate peatada ainult tasaarvestamata tšekkide puhul.</span><span class="sxs-lookup"><span data-stu-id="efc39-137">You can stop payment only on checks that haven’t cleared.</span></span></td>
</tr>
</tbody>
</table>



<span data-ttu-id="efc39-138">Lisateavet vt järgmistest teemadest:</span><span class="sxs-lookup"><span data-stu-id="efc39-138">For more information, see the following topics:</span></span>

[<span data-ttu-id="efc39-139">Hilisema kuupäevaga tšekkide seadistamine</span><span class="sxs-lookup"><span data-stu-id="efc39-139">Set up postdated checks</span></span>](tasks/set-up-postdated-checks.md)

[<span data-ttu-id="efc39-140">Kliendi hilisema kuupäevaga tšeki registreerimine ja sisestamine</span><span class="sxs-lookup"><span data-stu-id="efc39-140">Register and post a postdated check for a customer</span></span>](tasks/register-post-postdated-check-customer.md)

[<span data-ttu-id="efc39-141">Kliendi hilisema kuupäevaga tšeki tasakaalustamine</span><span class="sxs-lookup"><span data-stu-id="efc39-141">Settle a postdated check from a customer</span></span>](tasks/settle-postdated-check-customer.md)

[<span data-ttu-id="efc39-142">Hankija hilisema kuupäevaga tšeki registreerimine ja sisestamine</span><span class="sxs-lookup"><span data-stu-id="efc39-142">Register and post a postdated check for a vendor</span></span>](tasks/register-post-postdated-check-vendor.md) 

[<span data-ttu-id="efc39-143">Hankija hilisema kuupäevaga tšeki tasakaalustamine</span><span class="sxs-lookup"><span data-stu-id="efc39-143">Settle a postdated check for a vendor</span></span>](tasks/settle-postdated-check-vendor.md)




