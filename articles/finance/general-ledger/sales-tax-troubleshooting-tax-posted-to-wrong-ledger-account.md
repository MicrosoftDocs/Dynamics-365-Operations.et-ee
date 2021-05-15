---
title: Maks sisestatakse kandes valele pearaamatukontole
description: See teema pakub tõrkeotsingu teavet, mis võib aidata, kui maks sisestatakse kandes valele pearaamatukontole.
author: qire
manager: beya
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 0404d71f0492e188ed5da62387bb90a336e69c5a
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947627"
---
# <a name="tax-is-posted-to-the-wrong-ledger-account-in-the-voucher"></a><span data-ttu-id="fd3e5-103">Maks sisestatakse kandes valele pearaamatukontole</span><span class="sxs-lookup"><span data-stu-id="fd3e5-103">Tax is posted to the wrong ledger account in the voucher</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd3e5-104">Sisestamise ajal võib juhtuda, et maks sisestatakse kandes valele pearaamatukontole.</span><span class="sxs-lookup"><span data-stu-id="fd3e5-104">During posting, tax might be posted to the wrong ledger account in the voucher.</span></span> <span data-ttu-id="fd3e5-105">Selle probleemi tõrkeotsinguks järgige vastavalt järgmistele jaotistele juhiseid.</span><span class="sxs-lookup"><span data-stu-id="fd3e5-105">To troubleshoot this issue, follow the steps in the following sections as required.</span></span> <span data-ttu-id="fd3e5-106">Selle teema näidetes kasutatakse äridokumendina müügitellimust.</span><span class="sxs-lookup"><span data-stu-id="fd3e5-106">The examples in this topic use a sales order as the business document.</span></span>

## <a name="find-the-tax-code-of-the-incorrectly-posted-tax-transaction"></a><span data-ttu-id="fd3e5-107">Leia valesti sisestatud maksukande maksukood</span><span class="sxs-lookup"><span data-stu-id="fd3e5-107">Find the tax code of the incorrectly posted tax transaction</span></span>

1. <span data-ttu-id="fd3e5-108">Leheküljel **Kviitungi kanne** valige kanne, mida soovite kasutada ja seejärel valige **Sisestatud käibemaks**.</span><span class="sxs-lookup"><span data-stu-id="fd3e5-108">On the **Voucher transactions** page, select the transaction that you want to work with, and then select **Posted sales tax**.</span></span>

    <span data-ttu-id="fd3e5-109">[![Sisestatud käibemaksu nupp lehel kviitungi kanded](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)</span><span class="sxs-lookup"><span data-stu-id="fd3e5-109">[![Posted sales tax button on the Voucher transactions page](./media/tax-posted-to-wrong-ledger-account-Picture1.png)](./media/tax-posted-to-wrong-ledger-account-Picture1.png)</span></span>

2. <span data-ttu-id="fd3e5-110">Kontrollige väärtust väljal **Käibemaksukood**.</span><span class="sxs-lookup"><span data-stu-id="fd3e5-110">Review the value in the **Sales tax code** field.</span></span> <span data-ttu-id="fd3e5-111">Selles näites on **km 19**.</span><span class="sxs-lookup"><span data-stu-id="fd3e5-111">In this example, it's **VAT 19**.</span></span>

    <span data-ttu-id="fd3e5-112">[![Käibemaksukoodi väli sisestatud käibemaksu lehel](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)</span><span class="sxs-lookup"><span data-stu-id="fd3e5-112">[![Sales tax code field on the Posted sales tax page](./media/tax-posted-to-wrong-ledger-account-Picture2.png)](./media/tax-posted-to-wrong-ledger-account-Picture2.png)</span></span>

## <a name="check-the-ledger-posting-group-of-the-tax-code"></a><span data-ttu-id="fd3e5-113">Kontrollige pearaamatu sisestamise rühma maksukoodi</span><span class="sxs-lookup"><span data-stu-id="fd3e5-113">Check the ledger posting group of the tax code</span></span>

1. <span data-ttu-id="fd3e5-114">Valige suvandid **Maks** \> **Kaudsed maksud** \> **Käibemaks** \> **Käibemaksukoodid**.</span><span class="sxs-lookup"><span data-stu-id="fd3e5-114">Go to **Tax** \> **Indirect taxes** \> **Sales tax** \> **Sales tax codes**.</span></span>
2. <span data-ttu-id="fd3e5-115">Otsige ja valige maksukood ning vaadake seejärel üle väärtus väljal **Pearaamatu sisestusgrupp**.</span><span class="sxs-lookup"><span data-stu-id="fd3e5-115">Find and select the tax code, and then review the value in the **Ledger posting group** field.</span></span> <span data-ttu-id="fd3e5-116">Selles näites on **km**.</span><span class="sxs-lookup"><span data-stu-id="fd3e5-116">In this example, it's **VAT**.</span></span>

    <span data-ttu-id="fd3e5-117">[![Pearaamatu sisestamisgrupi väli käibemaksukoodide lehel](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)</span><span class="sxs-lookup"><span data-stu-id="fd3e5-117">[![Ledger posting group field on the Sales tax codes page](./media/tax-posted-to-wrong-ledger-account-Picture3.png)](./media/tax-posted-to-wrong-ledger-account-Picture3.png)</span></span>

3. <span data-ttu-id="fd3e5-118">Väärtus väljal **Pearaamatu sisestusrühm** on link.</span><span class="sxs-lookup"><span data-stu-id="fd3e5-118">The value in the **Ledger posting group** field is a link.</span></span> <span data-ttu-id="fd3e5-119">Grupi konfiguratsiooni üksikasjade vaatamiseks valige link.</span><span class="sxs-lookup"><span data-stu-id="fd3e5-119">To view the details of the group's configuration, select the link.</span></span> <span data-ttu-id="fd3e5-120">Teise võimalusena valige ja hoidke all (või paremklõpsake) väljal ja valige käsk **Kuva üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="fd3e5-120">Alternatively, select and hold (or right-click) in the field, and then select **View details**.</span></span>

    <span data-ttu-id="fd3e5-121">[![Käsk Kuva üksikasjad](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)</span><span class="sxs-lookup"><span data-stu-id="fd3e5-121">[![View details command](./media/tax-posted-to-wrong-ledger-account-Picture4.png)](./media/tax-posted-to-wrong-ledger-account-Picture4.png)</span></span>

4. <span data-ttu-id="fd3e5-122">Väljal **Tasumisele kuuluv käibemaks** kontrollige, et kontonumber on kandetüübi alusel õige.</span><span class="sxs-lookup"><span data-stu-id="fd3e5-122">In the **Sales tax payable** field, verify that the account number is correct, according to the transaction type.</span></span> <span data-ttu-id="fd3e5-123">Kui ei ole, valige õige konto, mida sisestada.</span><span class="sxs-lookup"><span data-stu-id="fd3e5-123">If it isn't, select the correct account to post to.</span></span> <span data-ttu-id="fd3e5-124">Selles näites tuleks müügitellimuse käibemaks sisestada käibemaksu käibemaksu tasumisele kuuluvale kontole 222200.</span><span class="sxs-lookup"><span data-stu-id="fd3e5-124">In this example, the sales tax of the sales order should be posted to sales tax payable account 222200.</span></span>

    <span data-ttu-id="fd3e5-125">[![Tasumisele kuuluva käibemaksu väli lehel Pearaamatu sisestamisgrupid](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)</span><span class="sxs-lookup"><span data-stu-id="fd3e5-125">[![Sales tax payable field on the Ledger posting groups page](./media/tax-posted-to-wrong-ledger-account-Picture5.png)](./media/tax-posted-to-wrong-ledger-account-Picture5.png)</span></span>

    <span data-ttu-id="fd3e5-126">Järgmine tabel annab teavet iga välja kohta **Pearaamatu sisestamisgruppide** lehel.</span><span class="sxs-lookup"><span data-stu-id="fd3e5-126">The following table provides information about each field on the **Ledger posting groups** page.</span></span>

    | <span data-ttu-id="fd3e5-127">Field</span><span class="sxs-lookup"><span data-stu-id="fd3e5-127">Field</span></span>                  | <span data-ttu-id="fd3e5-128">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="fd3e5-128">Description</span></span> |
    |------------------------|-------------|
    | <span data-ttu-id="fd3e5-129">Tasumisele kuuluv käibemaks</span><span class="sxs-lookup"><span data-stu-id="fd3e5-129">Sales tax payable</span></span>      | <span data-ttu-id="fd3e5-130">Maksuhaldurile makstava tasumisele kuuluva käibemaksu põhikonto.</span><span class="sxs-lookup"><span data-stu-id="fd3e5-130">The main account for outgoing sales taxes that are payable to the tax authority.</span></span> |
    | <span data-ttu-id="fd3e5-131">Saadaolev käibemaks</span><span class="sxs-lookup"><span data-stu-id="fd3e5-131">Sales tax receivable</span></span>   | <span data-ttu-id="fd3e5-132">Maksuhaldurilt saadaolevate maksutagastuste põhikonto.</span><span class="sxs-lookup"><span data-stu-id="fd3e5-132">The main account for incoming taxes that are received from the tax authority.</span></span> |
    | <span data-ttu-id="fd3e5-133">Kasutusmaksu kulu</span><span class="sxs-lookup"><span data-stu-id="fd3e5-133">Use tax expense</span></span>        | <span data-ttu-id="fd3e5-134">Peamine konto, mida kasutatakse mahaarvatavate kasutusmaksude kirjendamiseks, mida hankijad ei nõua või aruandeks maksuhaldurile osana Euroopa Liidu (EL) kaupade ja teenuste maksu pöördmaksustamisest (GST) / ühtlustatud käibemaksust (HST).</span><span class="sxs-lookup"><span data-stu-id="fd3e5-134">The main account that is used to post deductible use taxes that vendors don't claim or report to the tax authority as part of European Union (EU) reverse charge Goods and Services Tax (GST)/Harmonized Sales Tax (HST).</span></span> <span data-ttu-id="fd3e5-135">Suvand **Kasuta maksu** peab olema valitud kandes kasutatavale käibemaksukoodile jaotises käibemaksugrupp.</span><span class="sxs-lookup"><span data-stu-id="fd3e5-135">**Use tax** must be selected for the sales tax code in the sales tax group that is used in the transaction.</span></span> <span data-ttu-id="fd3e5-136">See väli ei ole kohaldatav, kui lehel **Pearaamatu parameetrid** on valitud suvand **Rakenda käibemaksuga maksustamise reeglid**.</span><span class="sxs-lookup"><span data-stu-id="fd3e5-136">This field isn't available if **Apply sales tax taxation rules** is selected on the **General ledger parameters** page.</span></span> |
    | <span data-ttu-id="fd3e5-137">Kasutusmaksu kohustus</span><span class="sxs-lookup"><span data-stu-id="fd3e5-137">Use tax payable</span></span>        | <span data-ttu-id="fd3e5-138">Põhikonto, mida kasutatakse maksuametile makstavate sissetulevate kasutusmaksude sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="fd3e5-138">The main account that is used to post incoming use taxes that are payable to tax authorities.</span></span> |
    | <span data-ttu-id="fd3e5-139">Tasakaalustuskonto</span><span class="sxs-lookup"><span data-stu-id="fd3e5-139">Settlement account</span></span>     | <span data-ttu-id="fd3e5-140">Põhikonto, mida kasutatakse pearaamatu kontode netosaldo kirjendamiseks, mis on täpsustatud väljadel **Makstav kasutusmaks** ja **Saadaolev käibemaks**.</span><span class="sxs-lookup"><span data-stu-id="fd3e5-140">The main account that is used to post the net balance of the ledger accounts that are specified in the **Use tax payable** and **Sales tax receivable** fields.</span></span> |
    | <span data-ttu-id="fd3e5-141">Hankija skonto</span><span class="sxs-lookup"><span data-stu-id="fd3e5-141">Vendor cash discount</span></span>   | <span data-ttu-id="fd3e5-142">Põhikonto, mida kasutatakse selle pearaamatu sisestamisgrupiga seotud käibemaksukoodide varase makse soodustuse sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="fd3e5-142">The main account that is used to post a cash discount for sales tax codes that are associated with this ledger posting group.</span></span> |
    | <span data-ttu-id="fd3e5-143">Kliendijuhtumi allahindlus</span><span class="sxs-lookup"><span data-stu-id="fd3e5-143">Customer case discount</span></span> | <span data-ttu-id="fd3e5-144">Põhikonto, mida kasutatakse selle pearaamatu sisestamisgrupiga seotud käibemaksukoodide varase makse soodustuse sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="fd3e5-144">The main account that is used to post a cash discount for sales tax codes that are associated with this ledger posting group.</span></span> |

    <span data-ttu-id="fd3e5-145">Lisateavet leiate teemast [Käibemaksu jaoks pearaamatu sisestusgruppide seadistamine](tasks/set-up-ledger-posting-groups-sales-tax.md)</span><span class="sxs-lookup"><span data-stu-id="fd3e5-145">For more information, see, [Set up Ledger posting groups for sales tax](tasks/set-up-ledger-posting-groups-sales-tax.md)</span></span>

## <a name="debug-in-code-to-check-ledger-dimensions"></a><span data-ttu-id="fd3e5-146">Vigade parandamine koodis kontrollimaks pearaamatu dimensioone</span><span class="sxs-lookup"><span data-stu-id="fd3e5-146">Debug in code to check ledger dimensions</span></span>

<span data-ttu-id="fd3e5-147">Koodis määrab sisestuskonto pearaamatu dimensioon.</span><span class="sxs-lookup"><span data-stu-id="fd3e5-147">In the code, the posting account is determined by the ledger dimension.</span></span> <span data-ttu-id="fd3e5-148">Pearaamatu dimensioon salvestab andmebaasi konto kirje ID.</span><span class="sxs-lookup"><span data-stu-id="fd3e5-148">The ledger dimension saves the record ID of an account in the database.</span></span>

1. <span data-ttu-id="fd3e5-149">Müügitellimuse puhul lisage katkestuspunkt meetoditele **Tax::saveAndPost()** ja **Tax::post()**.</span><span class="sxs-lookup"><span data-stu-id="fd3e5-149">For a sales order, add a breakpoint at the **Tax::saveAndPost()** and **Tax::post()** methods.</span></span> <span data-ttu-id="fd3e5-150">Pööra tähelepanu parameetri **\_pearaamati dimensioon** väärtusele.</span><span class="sxs-lookup"><span data-stu-id="fd3e5-150">Pay attention to the value of **\_ledgerDimension**.</span></span>

    <span data-ttu-id="fd3e5-151">[![Müügitellimuse koodi näidis, millel on katkestuspunkt](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)</span><span class="sxs-lookup"><span data-stu-id="fd3e5-151">[![Sales order code sample that has a breakpoint](./media/tax-posted-to-wrong-ledger-account-Picture6.png)](./media/tax-posted-to-wrong-ledger-account-Picture6.png)</span></span>

    <span data-ttu-id="fd3e5-152">Ostutellimuse puhul lisage katkestuspunkt meetoditele **TaxPost::saveAndPost()** ja **TaxPost::postToTaxTrans()**.</span><span class="sxs-lookup"><span data-stu-id="fd3e5-152">For a purchase order, add a breakpoint at the **TaxPost::saveAndPost()** and **TaxPost::postToTaxTrans()** methods.</span></span> <span data-ttu-id="fd3e5-153">Pööra tähelepanu parameetri **\_pearaamati dimensioon** väärtusele.</span><span class="sxs-lookup"><span data-stu-id="fd3e5-153">Pay attention to the value of **\_ledgerDimension**.</span></span>

    <span data-ttu-id="fd3e5-154">[![Ostutellimuse koodi näidis, millel on katkestuspunkt](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)</span><span class="sxs-lookup"><span data-stu-id="fd3e5-154">[![Purchase order code sample that has a breakpoint](./media/tax-posted-to-wrong-ledger-account-Picture7.png)](./media/tax-posted-to-wrong-ledger-account-Picture7.png)</span></span>

2. <span data-ttu-id="fd3e5-155">Käivitage järgmine SQL-päring, et leida andmebaasis konto kuvamisväärtus, mis põhineb pearaamatu dimensiooni salvestatud kirje ID-l.</span><span class="sxs-lookup"><span data-stu-id="fd3e5-155">Run the following SQL query to find the display value of the account in the database, based on the record ID that is saved by the ledger dimension.</span></span>

    ```sql
    select * from DIMENSIONATTRIBUTEVALUECOMBINATION where recid={the value of _ledgerDimension}
    ```

    <span data-ttu-id="fd3e5-156">[![Kirje ID kuvatav väärtus](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)</span><span class="sxs-lookup"><span data-stu-id="fd3e5-156">[![Display value of the record ID](./media/tax-posted-to-wrong-ledger-account-Picture8.png)](./media/tax-posted-to-wrong-ledger-account-Picture8.png)</span></span>

3. <span data-ttu-id="fd3e5-157">Uurida väljakutse pinu, et leida kus **_pearaamatu dimensiooni** väärtus on määratud.</span><span class="sxs-lookup"><span data-stu-id="fd3e5-157">Examine the callstack to find where the **_ledgerDimension** value is assigned.</span></span> <span data-ttu-id="fd3e5-158">Tavaliselt on väärtus pärit **TmpTaxWorkTrans**.</span><span class="sxs-lookup"><span data-stu-id="fd3e5-158">Usually, the value is from **TmpTaxWorkTrans**.</span></span> <span data-ttu-id="fd3e5-159">Sel juhul peaksite lisama katkestuspunkti **TmpTaxWorkTrans::insert()** ja **TmpTaxWorkTrans::update()**, et leida kus väärtus määratud on.</span><span class="sxs-lookup"><span data-stu-id="fd3e5-159">In this case, you should add a breakpoint at **TmpTaxWorkTrans::insert()** and **TmpTaxWorkTrans::update()** to find where the value assigned.</span></span>

## <a name="determine-whether-customization-exists"></a><span data-ttu-id="fd3e5-160">Kohanduse olemasolu tuvastamine</span><span class="sxs-lookup"><span data-stu-id="fd3e5-160">Determine whether customization exists</span></span>

<span data-ttu-id="fd3e5-161">Kui olete eelmistes jaotistes kirjeldatud toimingud teinud, kuid pole probleemi lahendada õnnestunud, tehke kindlaks, kas kohandamine on võimalik.</span><span class="sxs-lookup"><span data-stu-id="fd3e5-161">If you've completed the steps in the previous sections but have found no issue, determine whether customization exists.</span></span> <span data-ttu-id="fd3e5-162">Kui kohandust ei ole, looge Microsofti teenusetaotlus edasise toe saamiseks.</span><span class="sxs-lookup"><span data-stu-id="fd3e5-162">If no customization exists, create a Microsoft service request for further support.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
