---
title: Skontod
description: Skontod seadistatakse ning neid ühiskasutatakse ostu- ja müügireskontroga.  Saadaolevat skontot saab määratleda kliendi- või hankija arve puhul ja see võetakse, kui arve tasutakse skonto kuupäeval.
author: kweekley
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CashDisc
audience: Application User
ms.reviewer: roschlom
ms.custom: 3741
ms.assetid: c25f9d85-2702-46aa-8e61-0b4886e069b3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 06a9effdbe2aed6175273332654755b0ebc46659
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830469"
---
# <a name="cash-discounts"></a><span data-ttu-id="e62f0-104">Skontod</span><span class="sxs-lookup"><span data-stu-id="e62f0-104">Cash discounts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e62f0-105">Skontod seadistatakse ning neid ühiskasutatakse ostu- ja müügireskontroga.</span><span class="sxs-lookup"><span data-stu-id="e62f0-105">Cash discounts are setup and shared for Accounts payable and Accounts receivable.</span></span>  <span data-ttu-id="e62f0-106">Saadaolevat skontot saab määratleda kliendi- või hankija arve puhul ja see võetakse, kui arve tasutakse skonto kuupäeval.</span><span class="sxs-lookup"><span data-stu-id="e62f0-106">The cash discount available can be defined on the customer invoice or vendor invoice, and will be taken if the invoice is paid within the cash discount date.</span></span> 

## <a name="cash-discounts"></a><span data-ttu-id="e62f0-107">Skontod</span><span class="sxs-lookup"><span data-stu-id="e62f0-107">Cash discounts</span></span>

<span data-ttu-id="e62f0-108">Lehel Skontod saab luua skontosid nii klientidele kui ka hankijatele.</span><span class="sxs-lookup"><span data-stu-id="e62f0-108">Cash discounts for both customers or vendors can be created in the Cash discounts page.</span></span> <span data-ttu-id="e62f0-109">Saate määratleda välja Järgmine allahindluse kood abil ka eelnevate skontokuupäevade möödumisel üksteisele järgnevate skontode seeria.</span><span class="sxs-lookup"><span data-stu-id="e62f0-109">You can also define, by using the Next discount code field, a series of cash discounts that succeed each other as previous cash discount dates expire.</span></span> <span data-ttu-id="e62f0-110">Lisateavet leiate selle teema osast „Näide: skontoseeriad”.</span><span class="sxs-lookup"><span data-stu-id="e62f0-110">For more information, see “Example: Series of cash discounts” later in this topic.</span></span> <span data-ttu-id="e62f0-111">Kui arve, kreeditkanne (kas makse või kreeditarve) või mõlemad sisestatakse muus valuutas kui juriidilise isiku arvestusvaluuta, arvutatakse skonto kreeditarve maksekuupäeval kehtiva vahetuskursi alusel.</span><span class="sxs-lookup"><span data-stu-id="e62f0-111">If the invoice, credit transaction (either a payment or a credit note), or both are entered in a currency other than the accounting currency of the legal entity, the cash discount is calculated using the exchange rate based on the date of the payment or credit note.</span></span> <span data-ttu-id="e62f0-112">Kui arve ja kreeditarve sisestatakse erinevatele juriidilistele isikutele ja juriidiliste isikute arvestusvaluutad erinevad, võetakse vahetuskurss arve juriidiliselt isikult kreeditarve kuupäeva seisuga.</span><span class="sxs-lookup"><span data-stu-id="e62f0-112">If the invoice and credit document are entered in different legal entities, and if the accounting currencies for the legal entities differ, the exchange rate is taken from the legal entity of the invoice, as of the date of the credit document.</span></span> <span data-ttu-id="e62f0-113">Lisateavet leiate selle teema osast „Näide: skontode vahetuskursid”.</span><span class="sxs-lookup"><span data-stu-id="e62f0-113">For more information, see “Example: Exchange rates for cash discounts” later in this topic.</span></span>

## <a name="defaulting-order-of-cash-discount-main-account"></a><span data-ttu-id="e62f0-114">Skonto põhikonto vaiketegevuste järjestus</span><span class="sxs-lookup"><span data-stu-id="e62f0-114">Defaulting order of cash discount main account</span></span>

<span data-ttu-id="e62f0-115">Kui arve on allahindluse saamiseks õigel ajal tasutud, sisestatakse allahindlus automaatselt skonto jaoks määratud põhikontole järgmiste vaikeprioriteetide alusel.</span><span class="sxs-lookup"><span data-stu-id="e62f0-115">If an invoice is settled in time to obtain a cash discount, the cash discount is automatically posted to a cash discount main account according to the following defaulting priority:</span></span>
1.  <span data-ttu-id="e62f0-116">Põhikonto, mis on määratud kliendi lehe Avatud kannete tasakaalustamine või hankija lehe Avatud kannete tasakaalustamine väljal Alternatiivne skonto.</span><span class="sxs-lookup"><span data-stu-id="e62f0-116">The main account specified in the Alternative cash discount account field on the customer Settle open transactions page or the vendor Settle open transactions page.</span></span>
2.  <span data-ttu-id="e62f0-117">Põhikonto määratakse arve käibemaksukoodiga määratud pearaamatu sisestamisgrupi väljal Kliendi skonto või Hankija skonto.</span><span class="sxs-lookup"><span data-stu-id="e62f0-117">The main account specified in the Customer cash discount field or the Vendor cash discount field of the ledger posting group that is assigned to the sales tax code of the invoice.</span></span> <span data-ttu-id="e62f0-118">Saate seadistada lehel Pearaamatu sisestusgrupid pearaamatu sisestusgruppe ja määrata neid käibemaksukoodidele lehel Käibemaksukoodid.</span><span class="sxs-lookup"><span data-stu-id="e62f0-118">Set up ledger posting groups on the Ledger posting groups page and assign them to sales tax codes in the Sales tax codes page.</span></span>
3.  <span data-ttu-id="e62f0-119">Tasakaalustatud arvel oleva skonto koodi peamine sisestuskonto lehel Skontod väljal Kliendi allahindluste põhikonto või Hankija allahindluste põhikonto.</span><span class="sxs-lookup"><span data-stu-id="e62f0-119">The main posting account on the Cash discounts page in either the Main account for customer discounts field or the Main account for vendor discounts field for the cash discount code that is on the settled invoice.</span></span>
4.  <span data-ttu-id="e62f0-120">Lehel Automaatsete kannete kontod määratletud skontode põhikonto.</span><span class="sxs-lookup"><span data-stu-id="e62f0-120">The main account for cash discounts, as defined in the Accounts for automatic transactions page.</span></span>

## <a name="example-series-of-cash-discounts"></a><span data-ttu-id="e62f0-121"> Näide: skontode seeriad</span><span class="sxs-lookup"><span data-stu-id="e62f0-121">Example: Series of cash discounts</span></span>
<span data-ttu-id="e62f0-122">Seadistage kolm skontokoodi järgmiselt:</span><span class="sxs-lookup"><span data-stu-id="e62f0-122">Set up three cash discount codes as follows:</span></span>
-   <span data-ttu-id="e62f0-123">Kood 5D10% – allahindlus 10%, kui summa tasutakse 5 päeva jooksul.</span><span class="sxs-lookup"><span data-stu-id="e62f0-123">Code 5D10% – A cash discount of 10% when the amount is paid within 5 days.</span></span>
-   <span data-ttu-id="e62f0-124">Kood 10D5% – allahindlus 5%, kui summa tasutakse 10 päeva jooksul.</span><span class="sxs-lookup"><span data-stu-id="e62f0-124">Code 10D5% – A cash discount of 5% when the amount is paid within 10 days.</span></span>
-   <span data-ttu-id="e62f0-125">Kood 14D2% – allahindlus 2%, kui summa tasutakse 14 päeva jooksul.</span><span class="sxs-lookup"><span data-stu-id="e62f0-125">Code 14D2% – A cash discount of 2% when the amount is paid within 14 days.</span></span>

<span data-ttu-id="e62f0-126">Tehke väljal Järgmine allahindlus järgmist.</span><span class="sxs-lookup"><span data-stu-id="e62f0-126">In the Next discount code field:</span></span>
-   <span data-ttu-id="e62f0-127">Koodi 5D10% puhul valige 10D5%.</span><span class="sxs-lookup"><span data-stu-id="e62f0-127">For the 5D10% code, select 10D5%.</span></span>
-   <span data-ttu-id="e62f0-128">Koodi 10D5% puhul valige 14D2%.</span><span class="sxs-lookup"><span data-stu-id="e62f0-128">For the 10D5% code, select 14D2%.</span></span>
-   <span data-ttu-id="e62f0-129">Koodi 14D2% puhul jätke väli Järgmine allahindluse kood tühjaks.</span><span class="sxs-lookup"><span data-stu-id="e62f0-129">For the 14D2% code, leave the Next discount code field blank.</span></span>

<span data-ttu-id="e62f0-130">Kolm skontot järgnevad üksteisele, kui maksekuupäev ületab arve eelmise skonto kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="e62f0-130">The three cash discounts succeed each other as the payment date exceeds the previous cash discount date on the invoice.</span></span> <span data-ttu-id="e62f0-131">Arve maksmisel antakse ainult üks skonto, olenevalt sellest, milline skonto kuupäev skontode seerias kehtib.</span><span class="sxs-lookup"><span data-stu-id="e62f0-131">Only one cash discount is granted when the invoice is paid, based on which cash discount date is meet in the sequence of cash discounts.</span></span>

## <a name="example-exchange-rates-for-cash-discounts"></a><span data-ttu-id="e62f0-132"> Näide: skontode vahetuskursid</span><span class="sxs-lookup"><span data-stu-id="e62f0-132">Example: Exchange rates for cash discounts</span></span>
<span data-ttu-id="e62f0-133">Teie juriidilise isiku arvestusvaluuta on euro ja USA dollarile on määratud järgmised vahetuskursid:</span><span class="sxs-lookup"><span data-stu-id="e62f0-133">Your legal entity’s accounting currency is EUR and the following exchange rates are specified for USD:</span></span>
-   <span data-ttu-id="e62f0-134">1. veebruar = 110</span><span class="sxs-lookup"><span data-stu-id="e62f0-134">February 1 = 110</span></span>
-   <span data-ttu-id="e62f0-135">1. märts = 80</span><span class="sxs-lookup"><span data-stu-id="e62f0-135">March 1 = 80</span></span>

<span data-ttu-id="e62f0-136">15. veebruaril sisestatakse arve 1000 USD skonto tingimustega 20D2%.</span><span class="sxs-lookup"><span data-stu-id="e62f0-136">An invoice for 1000 USD with cash discount terms of 20D2% is posted on February 15.</span></span> <span data-ttu-id="e62f0-137">Arve summa arvestusvaluutas on 1100 eurot.</span><span class="sxs-lookup"><span data-stu-id="e62f0-137">The accounting currency amount of the invoice is 1100 EUR.</span></span> <span data-ttu-id="e62f0-138">Makse summas 980 USA dollarit tasakaalustatakse arvega 1. märtsil.</span><span class="sxs-lookup"><span data-stu-id="e62f0-138">A payment for 980 USD is settled with the invoice on March 1.</span></span> <span data-ttu-id="e62f0-139">Skonto summa on 20 dollarit.</span><span class="sxs-lookup"><span data-stu-id="e62f0-139">The cash discount amount is 20 USD.</span></span> <span data-ttu-id="e62f0-140">Makse summa arvestusvaluutas on 784 eurot.</span><span class="sxs-lookup"><span data-stu-id="e62f0-140">The accounting currency amount of the payment is 784 EUR.</span></span> <span data-ttu-id="e62f0-141">Skonto summa arvestusvaluutas arvutatakse 1. märtsi vahetuskursiga: 20 \* 80 / 100 = 16 eurot.</span><span class="sxs-lookup"><span data-stu-id="e62f0-141">The accounting currency amount of the cash discount is calculated by using the exchange rate as of March 1: 20 \* 80 / 100 = 16 EUR.</span></span>

> [!NOTE]
> <span data-ttu-id="e62f0-142">Kui lehel Müügireskontro parameetrid või Ostureskontro parameetrid on tehtud valik Arvuta skontod osaliste maksete jaoks, kasutatakse iga osamakse kuupäeval kehtivat vahetuskurssi.</span><span class="sxs-lookup"><span data-stu-id="e62f0-142">If the Calculate cash discounts for partial payments option is selected in the Accounts receivable parameters or Accounts payable parameters pages, the exchange rate that is in effect on the date of each partial payment is used.</span></span> 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]