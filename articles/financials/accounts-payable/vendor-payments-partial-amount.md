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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: aeef806980665c523f10b373f7662ecf509a8172
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---

# <a name="vendor-payments-for-a-partial-amount"></a><span data-ttu-id="a3ec7-105">Hankija osalises summas maksed</span><span class="sxs-lookup"><span data-stu-id="a3ec7-105">Vendor payments for a partial amount</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="a3ec7-106">Mõnikord võite teha hankijale makse, mis on arve summast väiksem.</span><span class="sxs-lookup"><span data-stu-id="a3ec7-106">Sometimes, you might make a payment to a vendor that is less than the amount of an invoice.</span></span> <span data-ttu-id="a3ec7-107">See artikkel kirjeldab mitmesuguseid valikuid selle olukorra käsitlemiseks.</span><span class="sxs-lookup"><span data-stu-id="a3ec7-107">This article describes the various options for handling this situation.</span></span> <span data-ttu-id="a3ec7-108">Teile saadaolevad valikud sõltuvad teie ärivajadustest ja konfiguratsioonist.</span><span class="sxs-lookup"><span data-stu-id="a3ec7-108">The options that are available to you depend on your business requirements and configuration.</span></span> 

<a name="cash-discount-amounts"></a><span data-ttu-id="a3ec7-109">Skonto summad</span><span class="sxs-lookup"><span data-stu-id="a3ec7-109">Cash discount amounts</span></span>
---------------------

<span data-ttu-id="a3ec7-110">Hankija võib pakkuda enne tähtaega tasutud arve puhul skontot.</span><span class="sxs-lookup"><span data-stu-id="a3ec7-110">A vendor can offer you a cash discount for paying an invoice before the due date.</span></span> <span data-ttu-id="a3ec7-111">Näiteks sisestate arve summas 100,00 ja sellele on määratud skonto 2%, kui arve tasutakse kümne päeva jooksul.</span><span class="sxs-lookup"><span data-stu-id="a3ec7-111">For example, you enter an invoice for 100.00 that specifies a 2-percent cash discount if the invoice is paid within 10 days.</span></span> <span data-ttu-id="a3ec7-112">Tähtaeg on 30 päeva.</span><span class="sxs-lookup"><span data-stu-id="a3ec7-112">The due date terms are 30 days.</span></span> <span data-ttu-id="a3ec7-113">Kui maksesoovitus kasutab arve valimise kriteeriumina sularaha allahindlust ja kui soovitus käivitatakse skonto kuupäeval või enne seda, valitakse arve maksmiseks ja makse luuakse summas 98,00.</span><span class="sxs-lookup"><span data-stu-id="a3ec7-113">If a payment proposal uses the cash discount as a criterion for selecting an invoice, and if the proposal is run on or before the cash discount date, the invoice is selected for payment, and the payment is created for 98.00.</span></span> <span data-ttu-id="a3ec7-114">Skonto saab võtta ka ühekordse käsitsi loodud makse jaoks.</span><span class="sxs-lookup"><span data-stu-id="a3ec7-114">A cash discount can also be taken for a one-off payment that was created manually.</span></span>

## <a name="partial-payments-with-cash-discounts"></a><span data-ttu-id="a3ec7-115">Osalised maksed skontodega</span><span class="sxs-lookup"><span data-stu-id="a3ec7-115">Partial payments with cash discounts</span></span>
<span data-ttu-id="a3ec7-116">Osalise makse tegemisel kavatsete ilmselt teha täiendava osamakse arve täielikuks tasakaalustamiseks.</span><span class="sxs-lookup"><span data-stu-id="a3ec7-116">When you make a partial payment, you might plan to make an additional partial payment to fully settle the invoice.</span></span> <span data-ttu-id="a3ec7-117">Osalise maksega skonto kasutamiseks valige leheküljel <strong>Ostureskontro parameetrid</strong> jaotise <strong>Arvuta skontod osaliste maksete jaoks **suvand **Jah</strong>.</span><span class="sxs-lookup"><span data-stu-id="a3ec7-117">To take a cash discount for a partial payment, you must set the <strong>Calculate cash discounts for partial payments **option to **Yes</strong> on the <strong>Account payable parameters</strong> page.</span></span> 

<span data-ttu-id="a3ec7-118">Näiteks saate 2% skontot, kui arve tasutakse kümne päeva jooksul pärast selle väljastamist.</span><span class="sxs-lookup"><span data-stu-id="a3ec7-118">For example, you receive a 2-percent cash discount if the invoice is paid within 10 days after it's issued.</span></span> <span data-ttu-id="a3ec7-119">Arve summas 100,00 on sisestatud.</span><span class="sxs-lookup"><span data-stu-id="a3ec7-119">An invoice is posted for 100.00.</span></span> <span data-ttu-id="a3ec7-120">Kui teete 10 päeva jooksul makse 49,00, sisestate maksetöölehele deebeti 49,00.</span><span class="sxs-lookup"><span data-stu-id="a3ec7-120">If you make a payment of 49.00 within 10 days, you enter a debit of 49.00 in a payment journal.</span></span> <span data-ttu-id="a3ec7-121">Lehel **Avatud kannete tasakaalustamine** osalise makse tasakaalustamisel ilmub väljale **Skonto summa võtmiseks** väärtus **1,00**.</span><span class="sxs-lookup"><span data-stu-id="a3ec7-121">When you settle the partial payment on the **Settle open transactions** page, **1.00** appears in the **Cash discount amount to take** field.</span></span> 

> [!NOTE] 
> <span data-ttu-id="a3ec7-122">. Kui sisestate osalise makse ja jätate täieliku arve summa väljale **Tasakaalustatav summa**, arvutatakse väli **Skonto summa võtmiseks** automaatselt ümber, kui kanded sisestate.</span><span class="sxs-lookup"><span data-stu-id="a3ec7-122">If you enter a partial payment and leave the full invoice amount in the **Amount to settle** field, the **Cash discount amount to take** field is automatically recalculated when you post the transactions.</span></span>

## <a name="credit-notes-with-cash-discounts"></a><span data-ttu-id="a3ec7-123">Skontodega kreeditarved</span><span class="sxs-lookup"><span data-stu-id="a3ec7-123">Credit notes with cash discounts</span></span>
<span data-ttu-id="a3ec7-124">Võib-olla tagastate osa arvel olevatest kaupadest ja saate kreeditarve.</span><span class="sxs-lookup"><span data-stu-id="a3ec7-124">You might return some of the items on an invoice and receive a credit note.</span></span> <span data-ttu-id="a3ec7-125">Kui algse arve puhul arvestati skontot, lahutage skonto väärtus ja saate tagasimakse õiges summas.</span><span class="sxs-lookup"><span data-stu-id="a3ec7-125">If a cash discount was taken on the original invoice, you can subtract the value of the discount and receive a refund for the correct amount.</span></span> <span data-ttu-id="a3ec7-126">Kui lehekülje <strong>Ostureskontro parameetrid</strong> jaotise <strong>Arvuta skontod kreeditarvete jaoks **suvandi väärtuseks on seatud **Jah</strong>, arvutatakse skonto kreeditarve jaoks automaatselt.</span><span class="sxs-lookup"><span data-stu-id="a3ec7-126">If the <strong>Calculate cash discounts for credit notes **option is set to **Yes</strong> on the <strong>Accounts payable parameters</strong> page, the discount is automatically calculated for the credit note.</span></span> 

<span data-ttu-id="a3ec7-127">Näiteks saate 2% skontot, kui arve tasutakse kümne päeva jooksul pärast selle väljastamist.</span><span class="sxs-lookup"><span data-stu-id="a3ec7-127">For example, you receive a 2-percent cash discount if the invoice is paid within 10 days after it's issued.</span></span> <span data-ttu-id="a3ec7-128">Sisestatud on arve summas 100,00.</span><span class="sxs-lookup"><span data-stu-id="a3ec7-128">An invoice for 100.00 is posted.</span></span> <span data-ttu-id="a3ec7-129">Kui tagastate kaubad ja saate kreeditarve, saate algse arve täissumma jaoks sisestada kreeditarve, mis on 100,00, pluss 2-protsendine skonto, mis määratletakse samuti krediiditeatisel.</span><span class="sxs-lookup"><span data-stu-id="a3ec7-129">If you return the goods and receive a credit note, you can enter the credit note for the full amount of the original invoice, 100.00, together with the 2-percent cash discount that is also defined on the credit memo.</span></span>  <span data-ttu-id="a3ec7-130">Kui vaatate kreeditarvet lehel **Kannete tasakaalustamine**, ilmub **98,00** väljale **Tasakaalustatav summa** ja **–2,00** väljale **Skonto summa**.</span><span class="sxs-lookup"><span data-stu-id="a3ec7-130">When you view the credit note on the **Settle transactions** page, **98.00** appears in the **Amount to settle** field, and **-2.00** appears in the **Cash discount amount** field.</span></span> <span data-ttu-id="a3ec7-131">Allahindluse summa sisestatakse skontokontole.</span><span class="sxs-lookup"><span data-stu-id="a3ec7-131">The discount amount is posted to a cash discount account.</span></span>

## <a name="overpaymentunderpayment-amounts"></a><span data-ttu-id="a3ec7-132">Üle-/alamakse summad</span><span class="sxs-lookup"><span data-stu-id="a3ec7-132">Overpayment/underpayment amounts</span></span>
<span data-ttu-id="a3ec7-133">Võib‑olla teete osalise makse, mille puhul tasakaalustamist vajav osa on väga väike.</span><span class="sxs-lookup"><span data-stu-id="a3ec7-133">You might make a partial payment where the amount that must still be settled is very small.</span></span> <span data-ttu-id="a3ec7-134">Näiteks, kui hankija arve on summas 1000,00 ja maksate sellest 999,90.</span><span class="sxs-lookup"><span data-stu-id="a3ec7-134">For example, the vendor invoice is for 1,000.00, and you pay 999.90.</span></span> <span data-ttu-id="a3ec7-135">Kui järelejäänud summa on väiksem kui summa, mis on määratud üle- või alamaksete puhul leheküljel **Ostureskontro parameetrid**, sisestatakse erinevus automaatselt üle-/alamakse pearaamatukontole.</span><span class="sxs-lookup"><span data-stu-id="a3ec7-135">If the remaining amount is less than the amount that is specified for overpayments or underpayments on the **Accounts payable parameters** page, the difference is automatically posted to an overpayment/underpayment ledger account.</span></span>


<span data-ttu-id="a3ec7-136">Lisateabe saamiseks vt [Hankijamaksete ülevaade](../cash-bank-management/tasks/vendor-payment-overview.md).</span><span class="sxs-lookup"><span data-stu-id="a3ec7-136">For more information, see [Vendor payment overview](../cash-bank-management/tasks/vendor-payment-overview.md).</span></span>

