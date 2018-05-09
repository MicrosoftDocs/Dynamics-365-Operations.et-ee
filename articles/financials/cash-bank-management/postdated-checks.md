---
title: "Hilisema kuupäevaga dateeritud tšekid"
description: "Selles artiklis antakse teavet hilisema kuupäevaga tšekkide toe kohta rakenduses Microsoft Dynamics 365 for Finance and Operations. Hilisema kuupäevaga dateeritud tšekid on tšekid, mis väljastatakse tulevasel kuupäeval maksete tegemise ja vastuvõtmise eesmärgil. Seetõttu ei saa tšekki enne määratud kuupäeva sularahaks vahetada."
author: twheeloc
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: VendPostDatedChecks, CustPostDatedChecks
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 21741
ms.assetid: 4eb7c7da-1e6b-4d35-9f41-373b66103229
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 28b972720bcc566cf0cd52dc8cb645562c61c2ae
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---

# <a name="postdated-checks"></a><span data-ttu-id="74c6a-105">Hilisema kuupäevaga dateeritud tšekid</span><span class="sxs-lookup"><span data-stu-id="74c6a-105">Postdated checks</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="74c6a-106">Selles artiklis antakse teavet hilisema kuupäevaga tšekkide toe kohta rakenduses Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="74c6a-106">This article provides information about support for postdated checks in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="74c6a-107">Hilisema kuupäevaga dateeritud tšekid on tšekid, mis väljastatakse tulevasel kuupäeval maksete tegemise ja vastuvõtmise eesmärgil.</span><span class="sxs-lookup"><span data-stu-id="74c6a-107">Postdated checks are checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="74c6a-108">Seetõttu ei saa tšekki enne määratud kuupäeva sularahaks vahetada.</span><span class="sxs-lookup"><span data-stu-id="74c6a-108">Therefore, the check can't be cashed until the specified date.</span></span>

<span data-ttu-id="74c6a-109">Microsoft Dynamics 365 for Finance and Operations toetab hilisema kuupäevaga dateeritud tšekkide täielikku haldustsüklit nii müügireskontros kui ka ostureskontros, nagu on näidatud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="74c6a-109">Microsoft Dynamics 365 for Finance and Operations supports the full management cycle for postdated checks in both Accounts receivable and Accounts payable, as shown in the following table.</span></span>
<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="74c6a-110">Stsenaarium</span><span class="sxs-lookup"><span data-stu-id="74c6a-110">Scenario</span></span></th>
<th><span data-ttu-id="74c6a-111">Üksikasjad</span><span class="sxs-lookup"><span data-stu-id="74c6a-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="74c6a-112">Hilisema kuupäevaga tšekkide seadistamine</span><span class="sxs-lookup"><span data-stu-id="74c6a-112">Set up postdated checks</span></span></td>
<td><span data-ttu-id="74c6a-113">Peate seadistama uue makseviisi ja määrama makserutiini väljastatud tšekkide, vastuvõetud tšekkide ja kinnipeetava maksu kliiringukontodele.</span><span class="sxs-lookup"><span data-stu-id="74c6a-113">You must set up a new payment method, and specify the payment routine for clearing accounts for issued checks, received checks, and withholding tax.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74c6a-114">Registreeri ja postita hankija hilisema kuupäevaga tšekk</span><span class="sxs-lookup"><span data-stu-id="74c6a-114">Register and post a postdated check for a vendor</span></span></td>
<td><span data-ttu-id="74c6a-115">Registreerige hankijale väljastatava hilisema kuupäevaga tšeki üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="74c6a-115">Register the details of a postdated check that you issue to a vendor.</span></span> <span data-ttu-id="74c6a-116">Kui makse on sisestatud, siis tuvastatakse hankija kohustus, kuid pangakonto ei ole veel krediteeritud.</span><span class="sxs-lookup"><span data-stu-id="74c6a-116">When the payment is posted, the vendor liability is recognized, but the bank account isn’t yet credit.</span></span> <span data-ttu-id="74c6a-117">Selle asemel kasutatakse selleks kliiringukontot.</span><span class="sxs-lookup"><span data-stu-id="74c6a-117">Instead, a clearing account is used for this purpose.</span></span> </td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74c6a-118">Kliendi hilisema kuupäevaga tšeki registreerimine ja postitamine</span><span class="sxs-lookup"><span data-stu-id="74c6a-118">Register and post a postdated check for a customer</span></span></td>
<td><span data-ttu-id="74c6a-119">Regitreerige kliendilt saadud hilisema kuupäevaga tšeki üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="74c6a-119">Register the details of a postdated check that you receive from a customer.</span></span> <span data-ttu-id="74c6a-120">Kui makse on sisestatud, siis on kliendi nõue krediteeritud, kuid pangakontot ei ole veel debiteeritud.</span><span class="sxs-lookup"><span data-stu-id="74c6a-120">When the payment is posted, the customer receivable is credit, but the bank account isn’t yet debit.</span></span> <span data-ttu-id="74c6a-121">Selle asemel kasutatakse selleks kliiringukontot.</span><span class="sxs-lookup"><span data-stu-id="74c6a-121">Instead, a clearing account is used for this purpose.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74c6a-122">Registreerige ja postitage kliendi või hankija hilisema kuupäevaga asendustšekk.</span><span class="sxs-lookup"><span data-stu-id="74c6a-122">Register and post a replacement postdated check for a customer or a vendor</span></span></td>
<td>
<span data-ttu-id="74c6a-123">Kui teie algne tšekk hankijale või kliendilt on kadunud või kahjustatud, siis saate hankijale väljastada hilise kuupäevaga dateeritud asendustšeki.</span><span class="sxs-lookup"><span data-stu-id="74c6a-123">If your original check to a vendor or from a customer is lost or damaged, you can issue a replacement postdated check.</span></span> <span data-ttu-id="74c6a-124">Tšeki üksikasjade registreerimisel lisage viide esialgsele tšekile ja näidake, et uus tšekk on originaali asendaja.</span><span class="sxs-lookup"><span data-stu-id="74c6a-124">When you register the check details, provide a reference to the original check, and indicate that the new check is a replacement for the original.</span></span> <span data-ttu-id="74c6a-125">Asendustšeki saate ka sisestada.</span><span class="sxs-lookup"><span data-stu-id="74c6a-125">You can also post the replacement check.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74c6a-126">Kliendi hilisema kuupäevaga tšeki ülekandmine hankijale</span><span class="sxs-lookup"><span data-stu-id="74c6a-126">Transfer a customer postdated check to a vendor</span></span></td>
<td><span data-ttu-id="74c6a-127">Kui saate kliendilt hilisema kuupäevaga dateeritud tšeki, saate tšeki hankijale maksena üle kanda.</span><span class="sxs-lookup"><span data-stu-id="74c6a-127">When you receive a postdated check from a customer, you can transfer that check to a vendor as a payment.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="74c6a-128">Kliendi või hankija hilisema kuupäevaga tšeki tasakaalustamine</span><span class="sxs-lookup"><span data-stu-id="74c6a-128">Settle a postdated check for a customer or a vendor</span></span></td>
<td><span data-ttu-id="74c6a-129">Tasakaalustage hilise kuupäevaga tšekk, mis sisestatakse kliendi või hankija vahekontole, kui tšekk lõpuks valmis on.</span><span class="sxs-lookup"><span data-stu-id="74c6a-129">Settle a postdated check that is posted to a bridging account for a customer or a vendor when the check finally matures.</span></span> <span data-ttu-id="74c6a-130">Tšeki tasakaalustamisel pank lõpuks debiteerib või krediteerib varem kasutatud kliiringukonto.</span><span class="sxs-lookup"><span data-stu-id="74c6a-130">When the check is settled, the bank is finally debit or credit against the clearing account that was used earlier.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="74c6a-131">Hankija hilisema kuupäevaga tšeki tühistamine</span><span class="sxs-lookup"><span data-stu-id="74c6a-131">Cancel a postdated check for a vendor</span></span></td>
<td><span data-ttu-id="74c6a-132">Sisestatud hilisema kuupäevaga tšeki saate tühistada järgmistes olukordades. - Pank tagastab tšeki.</span><span class="sxs-lookup"><span data-stu-id="74c6a-132">You can cancel a posted postdated check in these situations: - The check is returned by the bank.</span></span>
<span data-ttu-id="74c6a-133">- Tšekk on rakendatud valele arvele.</span><span class="sxs-lookup"><span data-stu-id="74c6a-133">- The check is applied to an incorrect invoice.</span></span>
<span data-ttu-id="74c6a-134">- Tšeki põhjal tehakse sularahamakse.</span><span class="sxs-lookup"><span data-stu-id="74c6a-134">- A cash payment is made against the check.</span></span>
  </td>
  </tr>
  <tr class="even">
  <td><span data-ttu-id="74c6a-135">Hilisema kuupäevaga tšeki makse peatamine</span><span class="sxs-lookup"><span data-stu-id="74c6a-135">Stop payment for a postdated check</span></span></td>
  <td><span data-ttu-id="74c6a-136">Saate peatada hankijale väljastatud hilisema kuupäevaga dateeritud tšeki põhjustel, nagu ebapiisavad vahendid, muudatused hankijaga sõlmitud lepingu tingimustes, hankija tarnitud defektsed kaubad või kaupade tagastamine hankijale.</span><span class="sxs-lookup"><span data-stu-id="74c6a-136">You can stop payment on a postdated check that was issued to a vendor, for reasons such as not sufficient funds, changes in the terms of the agreement with the vendor, supply of defective goods by the vendor, or return of goods to the vendor.</span></span> <span data-ttu-id="74c6a-137">Makse saate peatada ainult tasaarvestamata tšekkide puhul.</span><span class="sxs-lookup"><span data-stu-id="74c6a-137">You can stop payment only on checks that haven’t cleared.</span></span></td>
  </tr>
  </tbody>
  </table>



<span data-ttu-id="74c6a-138">Lisateavet vt järgmistest teemadest:</span><span class="sxs-lookup"><span data-stu-id="74c6a-138">For more information, see the following topics:</span></span>

[<span data-ttu-id="74c6a-139">Hilisema kuupäevaga tšekkide seadistamine</span><span class="sxs-lookup"><span data-stu-id="74c6a-139">Set up postdated checks</span></span>](tasks/set-up-postdated-checks.md)

[<span data-ttu-id="74c6a-140">Kliendi hilisema kuupäevaga tšeki registreerimine ja sisestamine</span><span class="sxs-lookup"><span data-stu-id="74c6a-140">Register and post a postdated check for a customer</span></span>](tasks/register-post-postdated-check-customer.md)

[<span data-ttu-id="74c6a-141">Kliendi hilisema kuupäevaga tšeki tasakaalustamine</span><span class="sxs-lookup"><span data-stu-id="74c6a-141">Settle a postdated check from a customer</span></span>](tasks/settle-postdated-check-customer.md)

[<span data-ttu-id="74c6a-142">Hankija hilisema kuupäevaga tšeki registreerimine ja sisestamine</span><span class="sxs-lookup"><span data-stu-id="74c6a-142">Register and post a postdated check for a vendor</span></span>](tasks/register-post-postdated-check-vendor.md) 

[<span data-ttu-id="74c6a-143">Hankija hilisema kuupäevaga tšeki tasakaalustamine</span><span class="sxs-lookup"><span data-stu-id="74c6a-143">Settle a postdated check for a vendor</span></span>](tasks/settle-postdated-check-vendor.md)




