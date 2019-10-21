---
title: Peatage ja jätkake kannet müügikohas (POS)
description: Selles teemas selgitatakse, kuidas kasutajad saavad pooleliolevad kanded peatada ja neid hiljem või teises registris jätkata, kasutades rakendust Dynamics 365 Retail.
author: jblucher
manager: AnnBe
ms.date: 11/27/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 261234
ms.assetid: 7cd68ecc-cc09-48ab-8cb8-48d5c304effa
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: efab3b793eb15e7feffb569492b5c36a2e9d6ec0
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/24/2019
ms.locfileid: "2025269"
---
# <a name="suspend-and-resume-transactions-in-the-point-of-sale-pos"></a><span data-ttu-id="fc078-103">Peatage ja jätkake kandeid müügikohas (POS)</span><span class="sxs-lookup"><span data-stu-id="fc078-103">Suspend and resume transactions in the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="fc078-104">Kassa (POS) kasutajad saavad peatada pooleliolevad kanded ja jätkata neid hiljem või teises registris.</span><span class="sxs-lookup"><span data-stu-id="fc078-104">Point of sale (POS) users can suspend in-progress transactions, and then resume them later or on a different register.</span></span> <span data-ttu-id="fc078-105">Kanded peatatakse sageli registri kiireks vabastamiseks teise ülesande jaoks praeguse kande olekut kaotamata.</span><span class="sxs-lookup"><span data-stu-id="fc078-105">Transactions are often suspended to quickly free up a register for a different task without losing any progress on the current transaction.</span></span> <span data-ttu-id="fc078-106">Näiteks alustab klienditeenindaja kliendi kande töötlemist mobiilses seadmes, kuid peab selle lõpule viima sularahasahtliga kassaaparaadis.</span><span class="sxs-lookup"><span data-stu-id="fc078-106">For example, a store associate starts to process a customer's transaction on a mobile device but must complete it on a register that has a cash drawer.</span></span> <span data-ttu-id="fc078-107">Sel juhul saab klienditeenindaja mobiilses seadmes kande peatada ja seejärel kande tagasi kutsuda ja jätkata kassaaparaadis.</span><span class="sxs-lookup"><span data-stu-id="fc078-107">In this case, the store associate can suspend the transaction on the mobile device, and then recall and resume it on a register.</span></span>

## <a name="configure-suspend-and-resume-functionality"></a><span data-ttu-id="fc078-108">Peatamise ja jätkamise funktsiooni konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="fc078-108">Configure suspend and resume functionality</span></span>

### <a name="pos-operations"></a><span data-ttu-id="fc078-109">Kassatoimingud</span><span class="sxs-lookup"><span data-stu-id="fc078-109">POS operations</span></span>

<span data-ttu-id="fc078-110">Kaks [kassatoimingut](pos-operations.md) lasevad kassatoes peatada ja jätkata stsenaariume.</span><span class="sxs-lookup"><span data-stu-id="fc078-110">Two [POS operations](pos-operations.md) let the POS support suspend and resume scenarios.</span></span> <span data-ttu-id="fc078-111">Saate määrata neid toiminguid kandelehel [nupupaneel](pos-screen-layouts.md) või tervituslehel.</span><span class="sxs-lookup"><span data-stu-id="fc078-111">You can assign these operations to [button grids](pos-screen-layouts.md) on the transaction page or the welcome page.</span></span>

- <span data-ttu-id="fc078-112">503: Peata kanne</span><span class="sxs-lookup"><span data-stu-id="fc078-112">503: Suspend transaction</span></span>
- <span data-ttu-id="fc078-113">504: Kutsu kanne tagasi</span><span class="sxs-lookup"><span data-stu-id="fc078-113">504: Recall transaction</span></span>

### <a name="receipt-template"></a><span data-ttu-id="fc078-114">Kviitungimall</span><span class="sxs-lookup"><span data-stu-id="fc078-114">Receipt template</span></span>

<span data-ttu-id="fc078-115">Kassat saab konfigureerida prinditud saatelehe loomiseks, kui kanne on peatatud.</span><span class="sxs-lookup"><span data-stu-id="fc078-115">The POS can be configured to generate a printed slip when a transaction is suspended.</span></span> <span data-ttu-id="fc078-116">Seejärel saab selle saatelehe abil kande kiiresti tuvastada ja hiljem tagasi kutsuda.</span><span class="sxs-lookup"><span data-stu-id="fc078-116">That slip can then be used to quickly identify and recall the transaction later.</span></span>

<span data-ttu-id="fc078-117">Kassa saatelehe printida lubamiseks peate lisama jaotise **Peatatud kanne** kviitungi vormingu kaupluse kviitungi profiili.</span><span class="sxs-lookup"><span data-stu-id="fc078-117">To enable the POS to print a slip, you must add the **Suspended transaction** receipt format to the store's receipt profile.</span></span> <span data-ttu-id="fc078-118">Kviitungi vormingu saate kujundada nii, et see hõlmab või välistab kande üksikasju.</span><span class="sxs-lookup"><span data-stu-id="fc078-118">You can design the receipt format so that it includes or excludes specific details about the transaction.</span></span> <span data-ttu-id="fc078-119">Näiteks võib vorming sisaldada vöötkoodi skannimise toetamiseks.</span><span class="sxs-lookup"><span data-stu-id="fc078-119">For example, the format can include a barcode to support scanning.</span></span>

### <a name="receipt-numbering"></a><span data-ttu-id="fc078-120">Kviitungi nummerdamine</span><span class="sxs-lookup"><span data-stu-id="fc078-120">Receipt numbering</span></span>

<span data-ttu-id="fc078-121">Muude kassa kandetüüpide osas, mis loovad prinditud kviitungi, saate määratleda peatatud kannete numbriseeria jaotises **Kviitungi nummerdamine** kaupluse funktsiooniprofiili osas.</span><span class="sxs-lookup"><span data-stu-id="fc078-121">As for other POS transaction types that generate a printed receipt, you can define a number sequence for suspended transactions in the **Receipt numbering** section of the store's functionality profile.</span></span>

### <a name="void-when-closing-shift"></a><span data-ttu-id="fc078-122">Tühista vahetuse sulgemisel</span><span class="sxs-lookup"><span data-stu-id="fc078-122">Void when closing shift</span></span>

<span data-ttu-id="fc078-123">Saate kasutada suvandit **Tühistada vahetuse sulgemisel**, mis nõuab, et kasutajad kas lõpetavad või tühistavad mis tahes peatatud kanded enne nende vahetuse sulgemist.</span><span class="sxs-lookup"><span data-stu-id="fc078-123">You can use the **Void when closing shift** option to require that users either complete or void any suspended transactions before they close their shift.</span></span> <span data-ttu-id="fc078-124">Tegevuse **Sule vahetus** ajal palub kassa kasutajatel vaadata või tühistada kõik laekumata peatatud kanded.</span><span class="sxs-lookup"><span data-stu-id="fc078-124">During the **Close shift** operation, the POS will prompt users to either view or void any outstanding suspended transactions.</span></span>

## <a name="suspend-and-resume-a-transaction"></a><span data-ttu-id="fc078-125">Kande peatamine ja jätkamine</span><span class="sxs-lookup"><span data-stu-id="fc078-125">Suspend and resume a transaction</span></span>

### <a name="suspend-a-transaction"></a><span data-ttu-id="fc078-126">Kande peatamine</span><span class="sxs-lookup"><span data-stu-id="fc078-126">Suspend a transaction</span></span>

<span data-ttu-id="fc078-127">Kasutajad, kellel on piisavalt õigusi ja selline ekraanipaigutus, mis sisaldab toimingut **Kande peatamine**, saavad kande peatada nii, et seda saab tagasi kutsuda hiljem või teises registris.</span><span class="sxs-lookup"><span data-stu-id="fc078-127">Users who have sufficient privileges, and who have a screen layout that includes the **Suspend transaction** operation, can suspend a transaction so that it can be recalled later or on a different register.</span></span>

<span data-ttu-id="fc078-128">Kandeid saab peatada ainult siis, kui nad **ei** sisalda järgmisi ridu:</span><span class="sxs-lookup"><span data-stu-id="fc078-128">Transactions can be suspended only if they do **not** contain the following types of lines:</span></span>

- <span data-ttu-id="fc078-129">Aktiivsed makseread</span><span class="sxs-lookup"><span data-stu-id="fc078-129">Active payment lines</span></span>
- <span data-ttu-id="fc078-130">Kinkekaardi read (kas kinkekaardi väljastamine või kinkekaardi saldo lisamine)</span><span class="sxs-lookup"><span data-stu-id="fc078-130">Gift card lines (either to issue a gift card or to add to the gift card balance)</span></span>

<span data-ttu-id="fc078-131">Peatatud kanne ei mõjuta müügiteavet või kaupluse saadavalolevate varude teavet.</span><span class="sxs-lookup"><span data-stu-id="fc078-131">A suspended transaction doesn't affect sales information or inventory availability information for the store.</span></span>

### <a name="resume-a-suspended-transaction"></a><span data-ttu-id="fc078-132">Peatatud kande jätkamine</span><span class="sxs-lookup"><span data-stu-id="fc078-132">Resume a suspended transaction</span></span>

<span data-ttu-id="fc078-133">Peatatud kandeid saab tagasi kutsuda ja jätkata sama poe iga kasutaja, kellel on piisavalt õigusi ja paigutus, mis sisaldab toimingut **Kande tagasikutsumine**.</span><span class="sxs-lookup"><span data-stu-id="fc078-133">Suspended transactions can be recalled and resumed in the same store by any user who has sufficient privileges, and who also has a layout that includes the **Recall transaction** operation.</span></span>

<span data-ttu-id="fc078-134">Peatatud kande kiiresti ja hõlpsasti tagasikutsumiseks skannige prinditud saatelehe vöötkood toimingust **Kande tagasikutsumine** kannete loendi vaatamise ajal.</span><span class="sxs-lookup"><span data-stu-id="fc078-134">To quickly and easily recall a suspended transaction, scan the barcode on the printed slip while you're viewing the list of transactions from the **Recall transaction** operation.</span></span>

### <a name="considerations-for-offline-mode"></a><span data-ttu-id="fc078-135">Millega arvestada võrguühenduseta režiimi puhul</span><span class="sxs-lookup"><span data-stu-id="fc078-135">Considerations for offline mode</span></span>

- <span data-ttu-id="fc078-136">Kandeid, mis on peatatud kassa ühendusrežiimis, ei saa jätkata ühenduseta režiimis, sest andmed ei sünkroonita võrguühenduseta andmebaasi.</span><span class="sxs-lookup"><span data-stu-id="fc078-136">Any transaction that is suspended while the POS is in online mode can't be resumed in offline mode, because the data isn't synced to the offline database.</span></span>
- <span data-ttu-id="fc078-137">Kui kanne peatada kassa võrguühenduseta režiimis, saab selle tagasi kutsuda võrguühenduseta režiimis juhul, kui kassat ei lülitatud sisse ühendusrežiimi sel ajal, kui kanne oli peatatud.</span><span class="sxs-lookup"><span data-stu-id="fc078-137">If you suspend a transaction while the POS is in offline mode, you can recall it in offline mode, provided that the POS wasn't switched back to online mode at any time since you suspended the transaction.</span></span> <span data-ttu-id="fc078-138">Kassa sisselülitamisel ühendusrežiimi teisaldatakse peatatud kannete andmed võrguühendusega andmebaasi ja eemaldatakse võrguühenduseta andmebaasist.</span><span class="sxs-lookup"><span data-stu-id="fc078-138">When the POS is switched back to online mode, data about suspended transactions is moved to the online database and removed from the offline database.</span></span> <span data-ttu-id="fc078-139">Seetõttu saab kandeid jätkata ainult võrguühendusega režiimis.</span><span class="sxs-lookup"><span data-stu-id="fc078-139">Therefore, the transactions can be resumed only in online mode.</span></span> <span data-ttu-id="fc078-140">Kui aktiveerite kassa võrguühenduseta režiimi, ei saa te jätkata peatatud kandeid, kuna need on juba eemaldatud võrguühenduseta andmebaasist.</span><span class="sxs-lookup"><span data-stu-id="fc078-140">If you switch the POS back to offline mode, you won't be able to resume those suspended transaction, because they have already been removed from the offline database.</span></span>

### <a name="void-a-suspended-transaction"></a><span data-ttu-id="fc078-141">Peatatud kande tühistamine</span><span class="sxs-lookup"><span data-stu-id="fc078-141">Void a suspended transaction</span></span>

<span data-ttu-id="fc078-142">Saate tühistada peatatud kande kas kande tagasikutsumisega ja seejärel toimingu **Kande tühistamine** teostamisega või valides kande loendist **Kande tagasikutsumine** ja valides suvandi **Tühistamine** rakenduste ribal.</span><span class="sxs-lookup"><span data-stu-id="fc078-142">You can void suspended transactions either by recalling the transaction and then performing the **Void transaction** operation, or by selecting the transaction in the **Recall transaction** list and selecting **Void** on the app bar.</span></span> <span data-ttu-id="fc078-143">Alternatiivina saab kauplus konfigureerida kasutajad valima peatatud kannete tühistamise vahetuse sulgemisel.</span><span class="sxs-lookup"><span data-stu-id="fc078-143">Alternatively, the store can be configured to prompt users to void suspended transactions when they close their shift.</span></span>
