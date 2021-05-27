---
title: Kliendi ettemaksed
description: See teema kirjeldab, kuidas seadistada ja töödelda kliendi ettemakseid (nimetatakse ka kliendi deposiitideks).
author: roschlom
ms.date: 04/30/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustPosting, LedgerJournalTransCustPaym, CustParameters
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: ''
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c3314803b994aed40e5b04d8546a45bd305d48b6
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019416"
---
# <a name="customer-prepayments"></a><span data-ttu-id="cefdf-103">Kliendi ettemaksed</span><span class="sxs-lookup"><span data-stu-id="cefdf-103">Customer prepayments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cefdf-104">Kliendi ettemakseid kasutatakse kliendilt makse saamiseks, kuid pole ühtegi arvet, mille suhtes makset tasakaalustada saab.</span><span class="sxs-lookup"><span data-stu-id="cefdf-104">Customer prepayments are used when you receive a payment from a customer, but there is no invoice that the payment can be settled against.</span></span> <span data-ttu-id="cefdf-105">Seda tüüpi makseid nimetatakse ka kliendi deposiitideks.</span><span class="sxs-lookup"><span data-stu-id="cefdf-105">These types of payments are also referred to as customer deposits.</span></span>

<span data-ttu-id="cefdf-106">Kliendi ettemaksete seadistamise ja sellega töötamise protsess koosneb järgmistest põhietappidest.</span><span class="sxs-lookup"><span data-stu-id="cefdf-106">The process of setting up and working with customer prepayments consists of the following basic steps.</span></span>

1. <span data-ttu-id="cefdf-107">Looge ettemaksetele kliendi sisestusreeglid.</span><span class="sxs-lookup"><span data-stu-id="cefdf-107">Create a customer posting profile for prepayments.</span></span>
2. <span data-ttu-id="cefdf-108">Seadistage **Sisestamise profiil ettemaksu töölehekandega** parameeter.</span><span class="sxs-lookup"><span data-stu-id="cefdf-108">Set the **Posting profile with prepayment journal voucher** parameter.</span></span>
3. <span data-ttu-id="cefdf-109">Looge kliendimakse tööleht ja märkige iga rea puhul **Ettemaksu töölehe kanne** märkeruut.</span><span class="sxs-lookup"><span data-stu-id="cefdf-109">Create a customer payment journal, and select the **Prepayment journal voucher** check box on each line.</span></span>
4. <span data-ttu-id="cefdf-110">Kliendi makse töölehe sisestamine</span><span class="sxs-lookup"><span data-stu-id="cefdf-110">Post the customer payment journal.</span></span>
5. <span data-ttu-id="cefdf-111">Pärast arve loomist tasakaalustage ettemaks kasutades **Seadista avatud kannete tasakaalustamine** lehte.</span><span class="sxs-lookup"><span data-stu-id="cefdf-111">After an invoice is generated, settle the prepayment with it by using the **Settle open transactions** page.</span></span>

## <a name="create-a-customer-posting-profile-for-prepayments"></a><span data-ttu-id="cefdf-112">Looge ettemaksetele kliendi sisestamisprofiil</span><span class="sxs-lookup"><span data-stu-id="cefdf-112">Create a customer posting profile for prepayments</span></span>

<span data-ttu-id="cefdf-113">Tavaliselt, kui aktsepteerite klientide ettemakseid või deposiite enne kaupade või teenuste tarnimist või enne arve olemasolu süsteemis, soovite sularaha kirjendada kontoplaanil vara asemel kohustusena.</span><span class="sxs-lookup"><span data-stu-id="cefdf-113">Typically, when you accept prepayments or deposits from your customers before goods or services are delivered, or before an invoice exists in your system, you will want to record the cash as a liability instead of an asset in your chart of accounts.</span></span> <span data-ttu-id="cefdf-114">Nende summade pearaamatusse kirjendamise nõuded võivad sõltuvalt teie riigist või regioonist erineda.</span><span class="sxs-lookup"><span data-stu-id="cefdf-114">However, the requirements for recording these amounts in your general ledger might differ, depending on your country or region.</span></span> <span data-ttu-id="cefdf-115">Seetõttu konsulteerige kindlasti oma raamatupidajatega kehtivate kohalike määruste suhtes.</span><span class="sxs-lookup"><span data-stu-id="cefdf-115">Therefore, be sure to consult your accountants about any local regulations that apply.</span></span>

<span data-ttu-id="cefdf-116">Üldiselt on sisestusreeglite loomise protsess, mida saab kasutada ettemaksete puhul, sama, mis teiste sisestusreeglite loomise protsessis.</span><span class="sxs-lookup"><span data-stu-id="cefdf-116">In general, the process for creating a posting profile that can be used for prepayments is the same as the process for creating other posting profiles.</span></span> <span data-ttu-id="cefdf-117">Peamine erinevus on põhikonto, mille valite **Summakonto** väljal.</span><span class="sxs-lookup"><span data-stu-id="cefdf-117">The primary difference is the main account that you select in the **Summary account** field.</span></span> <span data-ttu-id="cefdf-118">Lisateavet leiate teemast [Kliendi sisetamise profiil](customer-posting-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="cefdf-118">For more information, see [Customer posting profiles](customer-posting-profiles.md).</span></span>

## <a name="define-parameters-for-customer-prepayments"></a><span data-ttu-id="cefdf-119">Määratlege kliendi ettemaksete parameetrid</span><span class="sxs-lookup"><span data-stu-id="cefdf-119">Define parameters for customer prepayments</span></span>

<span data-ttu-id="cefdf-120">Müügireskontros on kaks põhiparameetrit, mida peate kliendi ettemaksete süsteemi konfigureerimisel arvesse võtma.</span><span class="sxs-lookup"><span data-stu-id="cefdf-120">There are two main Accounts receivable parameters that you must consider when you configure the system for customer prepayments.</span></span> <span data-ttu-id="cefdf-121">Parameetrite konfigureerimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="cefdf-121">Follow these steps to configure the parameters.</span></span>

1. <span data-ttu-id="cefdf-122">Minge jaotisse **Müügireskontro \> Seadistus \> Müügireskontro parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="cefdf-122">Go to **Accounts receivable \> Setup \> Accounts receivable parameters**.</span></span>
2. <span data-ttu-id="cefdf-123">Valikuline: Vahekaardil **Pearaamat ja käibemaks** kiirkaardil **Makse** määrake suvandile **Käibemaks ettemaksu töölehel** valik **Jah**.</span><span class="sxs-lookup"><span data-stu-id="cefdf-123">Optional: On the **Ledger and sales tax** tab, on the **Payment** FastTab, set the **Sales tax on prepayment journal voucher** option to **Yes**.</span></span>
3. <span data-ttu-id="cefdf-124">Väljal **Sisestusreeglid ettemaksu töölehekandega** valige kliendi ettemaksete sisestamisel kasutamiseks kliendi sisestusreeglid.</span><span class="sxs-lookup"><span data-stu-id="cefdf-124">In the **Posting profile with prepayment journal voucher** field, select the customer posting profile to use when customer prepayments are posted.</span></span>
4. <span data-ttu-id="cefdf-125">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="cefdf-125">Close the page.</span></span>

## <a name="create-customer-prepayment-vouchers"></a><span data-ttu-id="cefdf-126">Kliendi ettemakse kannete loomine</span><span class="sxs-lookup"><span data-stu-id="cefdf-126">Create customer prepayment vouchers</span></span>

<span data-ttu-id="cefdf-127">Kui loote kliendimakse töölehe iga ettemakse kohta, peate **Ettemaksu töölehe kande** valiku väärtuseks seaadistama **Jah** **Kliendi makse töölehe** lehel.</span><span class="sxs-lookup"><span data-stu-id="cefdf-127">When you create the customer payment journal, for every prepayment, you must set the **Prepayment journal voucher** option to **Yes** on the **Customer payment journal** page.</span></span> <span data-ttu-id="cefdf-128">Kliendi ettemakse loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="cefdf-128">Follow these steps to create a customer prepayment.</span></span>

1. <span data-ttu-id="cefdf-129">Avage **Müügireskontro \> Maksed \> Kliendi makse tööleht**.</span><span class="sxs-lookup"><span data-stu-id="cefdf-129">Go to **Accounts receivable \> Payments \> Customer payment journal**.</span></span>
2. <span data-ttu-id="cefdf-130">Valige **Uus**, et luua uus tööleht.</span><span class="sxs-lookup"><span data-stu-id="cefdf-130">Select **New** to create a journal.</span></span>
3. <span data-ttu-id="cefdf-131">Valige väljal **Nimi** töölehe nimi, mida kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="cefdf-131">In the **Name** field, select the journal name to use.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="cefdf-132">Kui määrate eelmises protseduuris valiku **Ettemakse töölehekande käibemaksu** väärtuseks **Jah**, peate valima töölehe nime, kus on valitud parameeter **Summa sisaldab käibemaksu**.</span><span class="sxs-lookup"><span data-stu-id="cefdf-132">If you set the **Sales tax on prepayment journal voucher** option to **Yes** in the previous procedure, you must select a journal name where the **Amount includes sales tax** parameter is selected.</span></span> 

4. <span data-ttu-id="cefdf-133">Valikuline: Sisestage väljale **Kirjeldus** detailne kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="cefdf-133">Optional: In the **Description** field, enter a detailed description.</span></span>
5. <span data-ttu-id="cefdf-134">Valige **Read**.</span><span class="sxs-lookup"><span data-stu-id="cefdf-134">Select **Lines**.</span></span>
6. <span data-ttu-id="cefdf-135">Kui tühja rida pole olemas, valige **Uus** rea loomiseks.</span><span class="sxs-lookup"><span data-stu-id="cefdf-135">If a blank line doesn't exist, select **New** to create a line.</span></span>
7. <span data-ttu-id="cefdf-136">Väljale **Kuupäev** sisestage kuupäev, millal ettemaks tuleks sisestada.</span><span class="sxs-lookup"><span data-stu-id="cefdf-136">In the **Date** field, enter the date when the prepayment should be posted.</span></span>
8. <span data-ttu-id="cefdf-137">Väljal **Konto** valige klient järgmise makse jaoks.</span><span class="sxs-lookup"><span data-stu-id="cefdf-137">In the **Account** field, select the customer for the prepayment.</span></span>
9. <span data-ttu-id="cefdf-138">Valikuline: Sisestage väljale **Kirjeldus** detailne kande kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="cefdf-138">Optional: In the **Description** field, enter a detailed description of the transaction.</span></span>
10. <span data-ttu-id="cefdf-139">Väljale **Kreedit** sisestage ettemaksu summa.</span><span class="sxs-lookup"><span data-stu-id="cefdf-139">In the **Credit** field, enter the amount of the prepayment.</span></span>
11. <span data-ttu-id="cefdf-140">Väljal **Vastaskonto** valige konto millele makse tasaarvestada.</span><span class="sxs-lookup"><span data-stu-id="cefdf-140">In the **Offset account** field, select the account to offset the payment to.</span></span> <span data-ttu-id="cefdf-141">Näiteks valige pank või põhikonto, mille jaoks makse sisestate.</span><span class="sxs-lookup"><span data-stu-id="cefdf-141">For example, select the bank or main account to post the payment to.</span></span>
12. <span data-ttu-id="cefdf-142">Väljale **Makseviis** sisestage kliendi makse viis.</span><span class="sxs-lookup"><span data-stu-id="cefdf-142">In the **Method of payment** field, select the customer's method of payment.</span></span>
13. <span data-ttu-id="cefdf-143">Seadke **Makse** vahekaardil **Ettemakse töölehekande** valiku väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="cefdf-143">On the **Payment** tab, set the **Prepayment journal voucher** option to **Yes**.</span></span>
14. <span data-ttu-id="cefdf-144">Korrake samme 7 kuni 13 iga täiendava ettemakse puhul, mida tuleb sisestada.</span><span class="sxs-lookup"><span data-stu-id="cefdf-144">Repeat steps 7 through 13 for each additional prepayment that must be posted.</span></span>
15. <span data-ttu-id="cefdf-145">Valige **Postita** töölehtede ridade sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="cefdf-145">Select **Post** to finalize the journal.</span></span>

## <a name="settle-prepayments-with-invoices"></a><span data-ttu-id="cefdf-146">Ettemaksete tasakaalustamine arvetega</span><span class="sxs-lookup"><span data-stu-id="cefdf-146">Settle prepayments with invoices</span></span>

<span data-ttu-id="cefdf-147">Saate kasutada **Kliendimaksete** tööruumi, et lihtsalt leida ja tasakaalustada makseid, mis pole täielikult tasakaalustatud.</span><span class="sxs-lookup"><span data-stu-id="cefdf-147">You can use the **Customer payments** workspace to easily find and settle payments that haven't been fully settled.</span></span>

1. <span data-ttu-id="cefdf-148">Valige **Avakuva** juhtpaneelil **Kliendimaksete** paneel.</span><span class="sxs-lookup"><span data-stu-id="cefdf-148">On the **Home** dashboard, select the **Customer payments** tile.</span></span>
2. <span data-ttu-id="cefdf-149">Tasakaalustamiseks otsige ja valige makse jaotises vahekaardil **Kliendi kanded** **Tasakaalustamata maksed**.</span><span class="sxs-lookup"><span data-stu-id="cefdf-149">In the **Customer transactions** section, on the **Payments not settled** tab, search for and select the payment to settle.</span></span>
3. <span data-ttu-id="cefdf-150">Valige **Kannete tasakaalustamine**.</span><span class="sxs-lookup"><span data-stu-id="cefdf-150">Select **Settle transactions**.</span></span>
4. <span data-ttu-id="cefdf-151">Valige **Märke** ruut arve jaoks ja makse jaoks, mida tasakaalustatakse.</span><span class="sxs-lookup"><span data-stu-id="cefdf-151">Select the **Mark** check box for the invoice and the payment that will be settled.</span></span>
5. <span data-ttu-id="cefdf-152">Valige **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="cefdf-152">Select **Post**.</span></span>

<span data-ttu-id="cefdf-153">Lisateavet avatud kannete tasakaalustamise kohta vt [tasakaalustamise ülevaade](/cash-bank-management/settlement-overview.md).</span><span class="sxs-lookup"><span data-stu-id="cefdf-153">For more information about how to settle open transactions, see [Settlement overview](/cash-bank-management/settlement-overview.md).</span></span>
