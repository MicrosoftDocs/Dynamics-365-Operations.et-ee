---
title: Hankija osalises summas maksed
description: "Mõnikord võite teha hankijale makse, mis on arve summast väiksem. See artikkel kirjeldab mitmesuguseid valikuid selle olukorra käsitlemiseks. Teile saadaolevad valikud sõltuvad teie ärivajadustest ja konfiguratsioonist."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 14321
ms.assetid: 9a17075e-5325-4d55-a1e5-1791b8c460a0
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 7acf791d9a04c618b9a238e5d16e676849792b65
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="vendor-payments-for-a-partial-amount"></a><span data-ttu-id="51e7e-105">Hankija osalises summas maksed</span><span class="sxs-lookup"><span data-stu-id="51e7e-105">Vendor payments for a partial amount</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="51e7e-106">Mõnikord võite teha hankijale makse, mis on arve summast väiksem.</span><span class="sxs-lookup"><span data-stu-id="51e7e-106">Sometimes, you might make a payment to a vendor that is less than the amount of an invoice.</span></span> <span data-ttu-id="51e7e-107">See artikkel kirjeldab mitmesuguseid valikuid selle olukorra käsitlemiseks.</span><span class="sxs-lookup"><span data-stu-id="51e7e-107">This article describes the various options for handling this situation.</span></span> <span data-ttu-id="51e7e-108">Teile saadaolevad valikud sõltuvad teie ärivajadustest ja konfiguratsioonist.</span><span class="sxs-lookup"><span data-stu-id="51e7e-108">The options that are available to you depend on your business requirements and configuration.</span></span> 

<a name="cash-discount-amounts"></a><span data-ttu-id="51e7e-109">Skonto summad</span><span class="sxs-lookup"><span data-stu-id="51e7e-109">Cash discount amounts</span></span>
---------------------

<span data-ttu-id="51e7e-110">Hankija võib pakkuda enne tähtaega tasutud arve puhul skontot.</span><span class="sxs-lookup"><span data-stu-id="51e7e-110">A vendor can offer you a cash discount for paying an invoice before the due date.</span></span> <span data-ttu-id="51e7e-111">Näiteks sisestate arve summas 100,00 ja sellele on määratud skonto 2%, kui arve tasutakse kümne päeva jooksul.</span><span class="sxs-lookup"><span data-stu-id="51e7e-111">For example, you enter an invoice for 100.00 that specifies a 2-percent cash discount if the invoice is paid within 10 days.</span></span> <span data-ttu-id="51e7e-112">Tähtaeg on 30 päeva.</span><span class="sxs-lookup"><span data-stu-id="51e7e-112">The due date terms are 30 days.</span></span> <span data-ttu-id="51e7e-113">Kui maksesoovitus kasutab arve valimise kriteeriumina sularaha allahindlust ja kui soovitus käivitatakse skonto kuupäeval või enne seda, valitakse arve maksmiseks ja makse luuakse summas 98,00.</span><span class="sxs-lookup"><span data-stu-id="51e7e-113">If a payment proposal uses the cash discount as a criterion for selecting an invoice, and if the proposal is run on or before the cash discount date, the invoice is selected for payment, and the payment is created for 98.00.</span></span> <span data-ttu-id="51e7e-114">Skonto saab võtta ka ühekordse käsitsi loodud makse jaoks.</span><span class="sxs-lookup"><span data-stu-id="51e7e-114">A cash discount can also be taken for a one-off payment that was created manually.</span></span>

## <a name="partial-payments-with-cash-discounts"></a><span data-ttu-id="51e7e-115">Osalised maksed skontodega</span><span class="sxs-lookup"><span data-stu-id="51e7e-115">Partial payments with cash discounts</span></span>
<span data-ttu-id="51e7e-116">Osalise makse tegemisel kavatsete ilmselt teha täiendava osamakse arve täielikuks tasakaalustamiseks.</span><span class="sxs-lookup"><span data-stu-id="51e7e-116">When you make a partial payment, you might plan to make an additional partial payment to fully settle the invoice.</span></span> <span data-ttu-id="51e7e-117">Osalise maksega skonto kasutamiseks valige leheküljel **Ostureskontro parameetrid** suvandi **Arvuta skontod osaliste maksete jaoks** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="51e7e-117">To take a cash discount for a partial payment, you must set the **Calculate cash discounts for partial payments **option to **Yes** on the **Account payable parameters** page.</span></span> 

<span data-ttu-id="51e7e-118">Näiteks saate 2% skontot, kui arve tasutakse kümne päeva jooksul pärast selle väljastamist.</span><span class="sxs-lookup"><span data-stu-id="51e7e-118">For example, you receive a 2-percent cash discount if the invoice is paid within 10 days after it's issued.</span></span> <span data-ttu-id="51e7e-119">Arve summas 100,00 on sisestatud.</span><span class="sxs-lookup"><span data-stu-id="51e7e-119">An invoice is posted for 100.00.</span></span> <span data-ttu-id="51e7e-120">Kui teete 10 päeva jooksul makse 49,00, sisestate maksetöölehele deebeti 49,00.</span><span class="sxs-lookup"><span data-stu-id="51e7e-120">If you make a payment of 49.00 within 10 days, you enter a debit of 49.00 in a payment journal.</span></span> <span data-ttu-id="51e7e-121">Lehel **Avatud kannete tasakaalustamine** osalise makse tasakaalustamisel ilmub väljale **Skonto summa võtmiseks** väärtus **1,00**.</span><span class="sxs-lookup"><span data-stu-id="51e7e-121">When you settle the partial payment on the **Settle open transactions** page, **1.00** appears in the **Cash discount amount to take** field.</span></span> 

> [!NOTE] 
> <span data-ttu-id="51e7e-122">. Kui sisestate osalise makse ja jätate täieliku arve summa väljale **Tasakaalustatav summa**, arvutatakse väli **Skonto summa võtmiseks** automaatselt ümber, kui kanded sisestate.</span><span class="sxs-lookup"><span data-stu-id="51e7e-122">If you enter a partial payment and leave the full invoice amount in the **Amount to settle** field, the **Cash discount amount to take** field is automatically recalculated when you post the transactions.</span></span>

## <a name="credit-notes-with-cash-discounts"></a><span data-ttu-id="51e7e-123">Skontodega kreeditarved</span><span class="sxs-lookup"><span data-stu-id="51e7e-123">Credit notes with cash discounts</span></span>
<span data-ttu-id="51e7e-124">Võib-olla tagastate osa arvel olevatest kaupadest ja saate kreeditarve.</span><span class="sxs-lookup"><span data-stu-id="51e7e-124">You might return some of the items on an invoice and receive a credit note.</span></span> <span data-ttu-id="51e7e-125">Kui algse arve puhul arvestati skontot, lahutage skonto väärtus ja saate tagasimakse õiges summas.</span><span class="sxs-lookup"><span data-stu-id="51e7e-125">If a cash discount was taken on the original invoice, you can subtract the value of the discount and receive a refund for the correct amount.</span></span> <span data-ttu-id="51e7e-126">Kui suvand **Arvuta skontod kreeditarvete jaoks** on lehel **Ostureskontro parameetrid** seatud väärtusele **Jah**, arvutatakse allahindlus kreeditarve jaoks automaatselt.</span><span class="sxs-lookup"><span data-stu-id="51e7e-126">If the **Calculate cash discounts for credit notes **option is set to **Yes** on the **Accounts payable parameters** page, the discount is automatically calculated for the credit note.</span></span> 

<span data-ttu-id="51e7e-127">Näiteks saate 2% skontot, kui arve tasutakse kümne päeva jooksul pärast selle väljastamist.</span><span class="sxs-lookup"><span data-stu-id="51e7e-127">For example, you receive a 2-percent cash discount if the invoice is paid within 10 days after it's issued.</span></span> <span data-ttu-id="51e7e-128">Sisestatud on arve summas 100,00.</span><span class="sxs-lookup"><span data-stu-id="51e7e-128">An invoice for 100.00 is posted.</span></span> <span data-ttu-id="51e7e-129">Kui tagastate kaubad ja saate kreeditarve, saate algse arve täissumma jaoks sisestada kreeditarve, mis on 100,00, pluss 2-protsendine skonto, mis määratletakse samuti krediiditeatisel.</span><span class="sxs-lookup"><span data-stu-id="51e7e-129">If you return the goods and receive a credit note, you can enter the credit note for the full amount of the original invoice, 100.00, together with the 2-percent cash discount that is also defined on the credit memo.</span></span>  <span data-ttu-id="51e7e-130">Kui vaatate kreeditarvet lehel **Kannete tasakaalustamine**, ilmub **98,00** väljale **Tasakaalustatav summa** ja **–2,00** väljale **Skonto summa**.</span><span class="sxs-lookup"><span data-stu-id="51e7e-130">When you view the credit note on the **Settle transactions** page, **98.00** appears in the **Amount to settle** field, and **-2.00** appears in the **Cash discount amount** field.</span></span> <span data-ttu-id="51e7e-131">Allahindluse summa sisestatakse skontokontole.</span><span class="sxs-lookup"><span data-stu-id="51e7e-131">The discount amount is posted to a cash discount account.</span></span>

## <a name="overpaymentunderpayment-amounts"></a><span data-ttu-id="51e7e-132">Üle-/alamakse summad</span><span class="sxs-lookup"><span data-stu-id="51e7e-132">Overpayment/underpayment amounts</span></span>
<span data-ttu-id="51e7e-133">Võib‑olla teete osalise makse, mille puhul tasakaalustamist vajav osa on väga väike.</span><span class="sxs-lookup"><span data-stu-id="51e7e-133">You might make a partial payment where the amount that must still be settled is very small.</span></span> <span data-ttu-id="51e7e-134">Näiteks, kui hankija arve on summas 1000,00 ja maksate sellest 999,90.</span><span class="sxs-lookup"><span data-stu-id="51e7e-134">For example, the vendor invoice is for 1,000.00, and you pay 999.90.</span></span> <span data-ttu-id="51e7e-135">Kui järelejäänud summa on väiksem kui summa, mis on määratud üle- või alamaksete puhul leheküljel **Ostureskontro parameetrid**, sisestatakse erinevus automaatselt üle-/alamakse pearaamatukontole.</span><span class="sxs-lookup"><span data-stu-id="51e7e-135">If the remaining amount is less than the amount that is specified for overpayments or underpayments on the **Accounts payable parameters** page, the difference is automatically posted to an overpayment/underpayment ledger account.</span></span>


<span data-ttu-id="51e7e-136">Lisateabe saamiseks vt [Hankijamaksete ülevaade](../cash-bank-management/tasks/vendor-payment-overview.md).</span><span class="sxs-lookup"><span data-stu-id="51e7e-136">For more information, see [Vendor payment overview](../cash-bank-management/tasks/vendor-payment-overview.md).</span></span>

