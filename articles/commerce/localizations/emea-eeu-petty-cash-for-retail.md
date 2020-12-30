---
title: Kaubanduse pisikulude kassa haldus Ida-Euroopa puhul
description: See teema kirjeldab, kuidas seadistada ja kasutada kaubanduse kassahalduse funktsiooni Ida-Euroopas.
author: epopov
manager: annbe
ms.date: 10/03/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Retail, Operations
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.search.industry: Retail
ms.author: v-kikozl
ms.search.validFrom: 2018-10-31
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: b7c7c63083dceebe73bfa04169a0b2da3228c8b1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4407847"
---
# <a name="petty-cash-management-for-commerce-for-eastern-europe"></a><span data-ttu-id="9ed93-103">Kaubanduse pisikulude kassa haldus Ida-Euroopa puhul</span><span class="sxs-lookup"><span data-stu-id="9ed93-103">Petty cash management for Commerce for Eastern Europe</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9ed93-104">Selles artiklis kirjeldatakse Ida-Euroopa kaubandusega seotud lokaliseerimist.</span><span class="sxs-lookup"><span data-stu-id="9ed93-104">This article contains information about Eastern European localization specific for the commerce industry.</span></span>

<span data-ttu-id="9ed93-105">Ida-Euroopa raamatupidamise nõuete järgi saate seadistada sularahakontode operatsioonid, et automatiseerida sissetulekute, kassdokumentide ja sularahaaruannetega seotud protsesse.</span><span class="sxs-lookup"><span data-stu-id="9ed93-105">In accordance with the Eastern Europe accounting requirements, you can set up operations for cash accounts to automate the processes for receipts, cash documents and cash reports.</span></span> <span data-ttu-id="9ed93-106">Lisateabe saamiseks avage [(EEUR) Kassahalduse parameetrite seadistamine](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/eeur-set-up-parameters-for-cash-management).</span><span class="sxs-lookup"><span data-stu-id="9ed93-106">For more information, go to [(EEUR) Set up parameters for cash management](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/eeur-set-up-parameters-for-cash-management).</span></span>

<span data-ttu-id="9ed93-107">Jaemüüjad võivad võtta müüdavate toodete ja teenuste eest tasu erinevat tüüpi maksemeetoditega.</span><span class="sxs-lookup"><span data-stu-id="9ed93-107">Retailers can accept various types of payment in exchange for the products and services that they sell.</span></span> <span data-ttu-id="9ed93-108">Kuigi levinuim maksemeetod on sularaha, võivad jaemüüjad võtta tasu ka tšekkide, kaartide või kannetega.</span><span class="sxs-lookup"><span data-stu-id="9ed93-108">Although cash is the most common form of payment, retailers can also receive payment in the form of checks, cards, or vouchers.</span></span> <span data-ttu-id="9ed93-109">Kassas käideldakse sularaha, krediitkaardimakseid ja muid maksemeetodeid rahakäitlusüksuse kaudu.</span><span class="sxs-lookup"><span data-stu-id="9ed93-109">In Retail point of sale (POS), cash, credit card receipts, and other payments are processed through a cash office.</span></span>

<span data-ttu-id="9ed93-110">Kassahaldusega saate kaubanduses teha järgmist:</span><span class="sxs-lookup"><span data-stu-id="9ed93-110">You can do the following by using Cash management in Commerce:</span></span>

- <span data-ttu-id="9ed93-111">luua iga kaupluse jaoks valitud maksemeetodile sularahakonto,</span><span class="sxs-lookup"><span data-stu-id="9ed93-111">Create a cash account for the selected payment method for each store.</span></span>
- <span data-ttu-id="9ed93-112">kasutada jaemüügikassas tehtud sularahatehingute ja kliendimaksete sisestamiseks kassatöölehti,</span><span class="sxs-lookup"><span data-stu-id="9ed93-112">Use cash journals to post cash transactions and customer payments that are received at a retail POS.</span></span>
- <span data-ttu-id="9ed93-113">koondada väljavõtte sisestamisel kanded väljavõtte reale.</span><span class="sxs-lookup"><span data-stu-id="9ed93-113">Aggregate transactions in a statement line when you post a statement.</span></span> <span data-ttu-id="9ed93-114">Saate koondada seifi viidava raha, panka viidava raha, kandetehingud, eemaldada maksevahendi kandeid, sularaha kirje kandeid, tulu kandeid, kulu kandeid, kliendimakseid, müügitehinguid ja tagastuskandeid.</span><span class="sxs-lookup"><span data-stu-id="9ed93-114">You can aggregate safe drops, bank drops, voucher transactions, remove tender transactions, float entry transactions, income transactions, expense transactions, customer payments, sales transactions, and return transactions.</span></span>

<span data-ttu-id="9ed93-115">Kõik kassas tehtavad kanded sisestatakse pearaamatu töölehte kasutades.</span><span class="sxs-lookup"><span data-stu-id="9ed93-115">All transactions that take place in POS are posted using a ledger journal.</span></span> <span data-ttu-id="9ed93-116">Kannete loomiseks ja sisestamiseks saate kasutada sularahamaksete töölehti, kliendimaksete töölehti ja üldtöölehti.</span><span class="sxs-lookup"><span data-stu-id="9ed93-116">You can use cash payment journals, customer payment journals, and general journals to create and post the statements.</span></span> <span data-ttu-id="9ed93-117">Lisateabe saamiseks avage [Kaupluse aruannete loomine, arvutamine ja sisestamine](https://docs.microsoft.com/dynamics365/unified-operations/retail/tasks/create-calculate-post-statement-retail-store).</span><span class="sxs-lookup"><span data-stu-id="9ed93-117">For more information, go to [Create, calculate, and post statements for a retail store](https://docs.microsoft.com/dynamics365/unified-operations/retail/tasks/create-calculate-post-statement-retail-store).</span></span>

<span data-ttu-id="9ed93-118">Tegumirea **Sisestatud väljavõtete** lehel saate teha järgmist.</span><span class="sxs-lookup"><span data-stu-id="9ed93-118">On the **Posted statements** page, on the Action Pane, you can do the following:</span></span>

- <span data-ttu-id="9ed93-119">Väljavõttega seotud sularahamaksete töölehtede avamiseks valige **Päringu \> Sularahamaksete tööleht**.</span><span class="sxs-lookup"><span data-stu-id="9ed93-119">Go to **Inquiries \> Cash payment journal** to access the cash payment journals that are related to the statement.</span></span>
- <span data-ttu-id="9ed93-120">Väljavõttega seotud pearaamatu töölehtede (v.a kliendimaksed ja sularahamaksed) avamiseks valige **Päringud \> Päevaraamat**.</span><span class="sxs-lookup"><span data-stu-id="9ed93-120">Go to **Inquiries \> General journal** to access the ledger journals that are related to the statement, other than customer payments and cash payments.</span></span>

## <a name="set-up-for-cash-management-for-pos"></a><span data-ttu-id="9ed93-121">Kassahalduse seadistamine</span><span class="sxs-lookup"><span data-stu-id="9ed93-121">Set up for cash management for POS</span></span>

<span data-ttu-id="9ed93-122">Enne sularahahalduse kasutamist peate lõpule viima järgmise seadistusprotseduuri.</span><span class="sxs-lookup"><span data-stu-id="9ed93-122">You must complete the following setup procedure before you use cash management:</span></span>

- <span data-ttu-id="9ed93-123">Seadistage **Makseviiside** lehel igale jaemüüja aktsepteeritavale maksetüübile makseviis.</span><span class="sxs-lookup"><span data-stu-id="9ed93-123">Set up a payment method for each payment type that the retailer accepts on the **Payment methods** page.</span></span> <span data-ttu-id="9ed93-124">Saate kassa kannete sisestamiseks kasutada erinevaid makseviise.</span><span class="sxs-lookup"><span data-stu-id="9ed93-124">You can use different payment methods for posting transactions in POS.</span></span> <span data-ttu-id="9ed93-125">Makseviiside kohta lisateabe saamiseks vt [Makseviise](https://docs.microsoft.com/dynamics365/unified-operations/retail/payment-methods).</span><span class="sxs-lookup"><span data-stu-id="9ed93-125">For more information about payment methods, see [Payment methods](https://docs.microsoft.com/dynamics365/unified-operations/retail/payment-methods).</span></span>
- <span data-ttu-id="9ed93-126">Parameetrite seadistamine kassatoimingute jaoks.</span><span class="sxs-lookup"><span data-stu-id="9ed93-126">Set up parameters for cash operations.</span></span>
- <span data-ttu-id="9ed93-127">Kaupluse sularahamaksete maksemeetodi seadistamine.</span><span class="sxs-lookup"><span data-stu-id="9ed93-127">Set up a payment method for cash payments in a store.</span></span>

### <a name="set-up-parameters-for-cash-operations"></a><span data-ttu-id="9ed93-128">Parameetrite seadistamine kassatoimingute jaoks</span><span class="sxs-lookup"><span data-stu-id="9ed93-128">Set up parameters for cash operations</span></span>

<span data-ttu-id="9ed93-129">Saate seadistada parameetreid kaubanduse funktsiooniga sularahakannete loomiseks ja sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="9ed93-129">You can set up parameters to create and post cash transactions in Commerce.</span></span> <span data-ttu-id="9ed93-130">Kassas saate müügikannete ja maksekannete sisestamiseks kasutada rakenduse sularahamaksete töölehti, kliendimaksete töölehti ja üldtöölehti.</span><span class="sxs-lookup"><span data-stu-id="9ed93-130">You can use cash payment journals, customer payment journals, or general journals to post sales transactions and payment transactions in the POS.</span></span> <span data-ttu-id="9ed93-131">Väljavõtte sisestamisel saate ühendada samade atribuutidega kanded.</span><span class="sxs-lookup"><span data-stu-id="9ed93-131">You can aggregate transactions that have the same properties when you post a statement.</span></span>

1. <span data-ttu-id="9ed93-132">Minge jaotisse **Jaemüük ja kaubandus \> Peakontori seadistamine \> Parameetrid \> Kaubanduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="9ed93-132">Go to **Retail and Commerce \> Headquarters setup \> Parameters \> Commerce parameters**.</span></span> <span data-ttu-id="9ed93-133">Klõpsake vasakul paanil nuppu **Sisestamine**.</span><span class="sxs-lookup"><span data-stu-id="9ed93-133">In the left pane, click **Posting**.</span></span>
2. <span data-ttu-id="9ed93-134">Määrake **Sisestamise** alal **Kogumi** kiirkaardil **Väljamakse-/vahetusraha** olekuks **Jah**, et koondada väljavõtte sisestamisel kokku väljavõtte reaga seotud väljamakse kanded ja vahetusraha kanded. </span><span class="sxs-lookup"><span data-stu-id="9ed93-134">In the **Posting** area, on the **Aggregation** FastTab, set **Tender remove/float** to **Yes** to aggregate the remove tender transactions or float entry transactions that are associated with a statement line when you post the statement.</span></span> <span data-ttu-id="9ed93-135">Maksevahendi eemaldamise kanne luuakse, kui võtate sularaha kassast välja.</span><span class="sxs-lookup"><span data-stu-id="9ed93-135">A remove tender transaction is created when you withdraw cash from the POS cash drawer.</span></span> <span data-ttu-id="9ed93-136">Vahetusraha kirje kanne luuakse, kui panete kassasse sularaha.</span><span class="sxs-lookup"><span data-stu-id="9ed93-136">A float entry transaction is created when you deposit cash in the POS cash drawer.</span></span>
3. <span data-ttu-id="9ed93-137">Aktiveerige alltoodud parameetrid, et koondada väljavõtte sisestamisel väljavõttereaga seotud kanded.</span><span class="sxs-lookup"><span data-stu-id="9ed93-137">Activate the individual parameters listed below to aggregate the transactions that are associated with a statement line when you post the statement:</span></span>

    - <span data-ttu-id="9ed93-138">**Raha hoiustamine panka** – pangakannete koondamine.</span><span class="sxs-lookup"><span data-stu-id="9ed93-138">**Bank drop** – Aggregate bank transactions.</span></span>
    - <span data-ttu-id="9ed93-139">**Seifi viidav raha** – seifikannete koondamine.</span><span class="sxs-lookup"><span data-stu-id="9ed93-139">**Safe drop** – Aggregate safe transactions.</span></span>
    - <span data-ttu-id="9ed93-140">**Tulu/kulu kanded** – tulu- või kulukannete koondamine.</span><span class="sxs-lookup"><span data-stu-id="9ed93-140">**Income/Expense transactions** – Aggregate income transactions or expense transactions.</span></span>
    - <span data-ttu-id="9ed93-141">**Kupongi kanded** – kupongi kannete koondamine.</span><span class="sxs-lookup"><span data-stu-id="9ed93-141">**Voucher transactions** – Aggregate voucher transactions.</span></span>
    - <span data-ttu-id="9ed93-142">**Kliendi maksed** – kliendimaksete koondamine.</span><span class="sxs-lookup"><span data-stu-id="9ed93-142">**Customer payments** – Aggregate customer payments.</span></span>
    - <span data-ttu-id="9ed93-143">**Müügid ja tagastusted** – müükide ja tagastuste kanded.</span><span class="sxs-lookup"><span data-stu-id="9ed93-143">**Sales and returns** – Aggregate sales and returns transactions.</span></span>

4. <span data-ttu-id="9ed93-144">Määrake **Maksete** kiirkaardil töölehe vaikenimi järgmistele valikutele.</span><span class="sxs-lookup"><span data-stu-id="9ed93-144">On the **Payments** FastTab, select a default journal name for the following options:</span></span>

    - <span data-ttu-id="9ed93-145">**Kliendimaksete tööleht** – seda töölehte kasutatakse kliendimaksete sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="9ed93-145">**Customer payment journal** – This journal is used to post customer payments.</span></span>
    - <span data-ttu-id="9ed93-146">**Sularahamaksete tööleht** – seda töölehte kasutatakse sularahamaksete sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="9ed93-146">**Cash payment journal** – This journal is used to post cash payments.</span></span>
    - <span data-ttu-id="9ed93-147">**Päevaraamat** – seda töölehte kasutatakse kannete (v.a kliendimaksete ja sularahamaksete) sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="9ed93-147">**General journal** – This journal is used to post transactions other than cash payments and customer payments.</span></span>

### <a name="set-up-a-payment-method-for-cash-payments-in-a-store"></a><span data-ttu-id="9ed93-148">Kaupluse sularahamaksete maksemeetodi seadistamine</span><span class="sxs-lookup"><span data-stu-id="9ed93-148">Set up a payment method for cash payments in a store</span></span>

<span data-ttu-id="9ed93-149">Kaupluses sularahamaksete kasutamiseks maksemeetodi häälestamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="9ed93-149">Use the following procedure to set up a payment method for cash payments in a store.</span></span>

1. <span data-ttu-id="9ed93-150">Minge jaotisse **Jaemüük ja kaubandus \> Kanalid \> Kauplused \> Kõik kauplused**.</span><span class="sxs-lookup"><span data-stu-id="9ed93-150">Go to **Retail and Commerce \> Channels \> Stores \> All stores**.</span></span>
2. <span data-ttu-id="9ed93-151">Valige **Kõigi kaupluste** loendi lehel kauplus, mille jaoks maksemeetodit seadistate.</span><span class="sxs-lookup"><span data-stu-id="9ed93-151">On the **All stores** list page, select the store to set up a payment method for.</span></span>
3. <span data-ttu-id="9ed93-152">Klõpsake tegumiriba vahekaardil **Seadista** grupis **Seadistus** valikut **Maksemeetodid**.</span><span class="sxs-lookup"><span data-stu-id="9ed93-152">On the Action Pane, on the **Set up** tab, in the **Set up** group, click **Payment methods**.</span></span>
4. <span data-ttu-id="9ed93-153">Looge või määrake **Maksemeetodi** lehel maksemeetod.</span><span class="sxs-lookup"><span data-stu-id="9ed93-153">On the **Payment method** page, create or select a payment method.</span></span>
5. <span data-ttu-id="9ed93-154">Valige **Sisestamise** kiirkaardil **Konto** väljagrupis **Kontotüübi** väljal **Sularahakonto**.</span><span class="sxs-lookup"><span data-stu-id="9ed93-154">On the **Posting** FastTab, in the **Account** field group, in the **Account type** field, select **Cash account**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9ed93-155">Saate **Konto tüübi** väljal **Sularahakonto** valida ainult siis, kui valite **Funktsiooni** väljal valiku **Tavaline** või **Väljamakse-/vahetusraha**.</span><span class="sxs-lookup"><span data-stu-id="9ed93-155">You can select **Cash account** in the **Account type** field only if you select **Normal** or **Tender remove/float** in the **Function** field.</span></span>

6. <span data-ttu-id="9ed93-156">Valige **Kontonumbri** väljal maksemeetodi sularahakonto number.</span><span class="sxs-lookup"><span data-stu-id="9ed93-156">In the **Account number** field, select a cash account number for the payment method.</span></span>
7. <span data-ttu-id="9ed93-157">Valige **Väljamakse-/vahetusraha** väljagrupis **Vastaskonto** väljal vastaskonto, millele sisestada maksemeetodi väljamakse või vahetusraha kanded.</span><span class="sxs-lookup"><span data-stu-id="9ed93-157">In the **Tender remove/float** field group, in the **Offset account** field, select the offset account to post remove tender or float entry transactions for the payment method.</span></span>

> [!NOTE]
> <span data-ttu-id="9ed93-158">Kauplusele tuleb seadistada vastaskontod nii sularaha maksemeetodi jaoks kui ka väljamakse või vahetusraha maksemeetodi jaoks.</span><span class="sxs-lookup"><span data-stu-id="9ed93-158">You must set up offset accounts for both the cash tender payment method and the remove tender or float entry payment method for a store.</span></span> <span data-ttu-id="9ed93-159">See loob tasakaalus pearaamatu sissekanded maksemeetodi väljamakse või vahetusraha kannetele.</span><span class="sxs-lookup"><span data-stu-id="9ed93-159">This creates balanced general ledger entries for remove tender or float entry transactions.</span></span>
