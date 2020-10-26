---
title: Väikesed summad Ida-Euroopa ja Venemaa puhul
description: Selles teemas antakse teavet väikeste summade funktsiooni kohta, mis võimaldab Eestis, Leedus, Tšehhi Vabariigis, Ungaris, Lätis, Poolas ja Venemaal asuvatel kasutajatel kajastada süsteemis sularahatehinguid.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RCashBalance, RCashCountStatementForm, RCashPosting, RCashRemainLimit, RCashReportJour_PL, RCashTable, RCashTableBalance, RCashTableCredLimit, RCashTableLastRevaluation, RCashTableTransactions, RCashTrans
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 268504
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia
ms.author: kfend
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 890300d1251b2befce47f62535f44771378f3cb7
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3984674"
---
# <a name="petty-cash-for-eastern-europe-and-russia"></a><span data-ttu-id="66bbe-103">Väikesed summad Ida-Euroopa ja Venemaa puhul</span><span class="sxs-lookup"><span data-stu-id="66bbe-103">Petty cash for Eastern Europe and Russia</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="66bbe-104">Selles teemas antakse teavet väikeste summade funktsiooni kohta, mis võimaldab Eestis, Leedus, Tšehhi Vabariigis, Ungaris, Lätis, Poolas ja Venemaal asuvatel kasutajatel kajastada süsteemis sularahatehinguid.</span><span class="sxs-lookup"><span data-stu-id="66bbe-104">This topic provides information about the petty cash functionality that lets users in Estonia, Lithuania, Czech Republic, Hungary, Latvia, Poland, and Russia reflect cash operations in the system.</span></span>

<span data-ttu-id="66bbe-105">Väikeset summade funktsioon võimaldab automatiseerida sularahasissetulekute ja -kulude toiminguid, põhidokumentide loomist ja seotud aruannete printimist.</span><span class="sxs-lookup"><span data-stu-id="66bbe-105">You can use the petty cash functionality to automate operations for receipts and expenditures of cash, the creation of primary documents, and the printing of related reports.</span></span> <span data-ttu-id="66bbe-106">Väikeste summade funktsioon võimaldab teha järgmist.</span><span class="sxs-lookup"><span data-stu-id="66bbe-106">The petty cash functionality lets you perform the following operations:</span></span>

-   <span data-ttu-id="66bbe-107">Arvestada saadaoleva sularaha sissetulekuid ja kulusid.</span><span class="sxs-lookup"><span data-stu-id="66bbe-107">Account the receipt and expenditure of available cash assets.</span></span>
-   <span data-ttu-id="66bbe-108">Luua tüüpilisi sularahavorme: sularaha korvamisorderid, sularaha väljaminekuorderid ja sularahaorderite registreerimiste tööleht.</span><span class="sxs-lookup"><span data-stu-id="66bbe-108">Generate typical cash forms: Cash reimbursement slips, Cash disbursement slips, and a Journal of registration for cash slips.</span></span>
-   <span data-ttu-id="66bbe-109">Juhtida maksimaalset sularahasummat, mis on klientide, hankijatega jne tehtavate toimingute puhul lubatud.</span><span class="sxs-lookup"><span data-stu-id="66bbe-109">Control the maximum cash amount that is allowed for operations with customers, vendors, and so on.</span></span>
-   <span data-ttu-id="66bbe-110">Kajastada süsteemis sularahatoiminguid erinevates valuutades.</span><span class="sxs-lookup"><span data-stu-id="66bbe-110">Reflect cash operations in various currencies in the system.</span></span>
-   <span data-ttu-id="66bbe-111">Teisendada sularahatoimingute välisvaluutas summasid vaikevaluutasse ja esitada raamatupidamise aruandeid.</span><span class="sxs-lookup"><span data-stu-id="66bbe-111">Convert the amounts of cash operations in foreign currency to the default currency to provide accounting reporting.</span></span>
-   <span data-ttu-id="66bbe-112">Luua **kassaraamatu** ja kassapidaja aruandeid.</span><span class="sxs-lookup"><span data-stu-id="66bbe-112">Generate a **Cash book** report and a cashier’s report.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="66bbe-113">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="66bbe-113">Prerequisites</span></span>
<span data-ttu-id="66bbe-114">Väikeste summade funktsiooni kasutamiseks peate täitma järgmised eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="66bbe-114">Before you can use the petty cash functionality, you must complete the following prerequisites:</span></span>

-   <span data-ttu-id="66bbe-115">Seadistama sularahakontod.</span><span class="sxs-lookup"><span data-stu-id="66bbe-115">Set up cash accounts.</span></span>
-   <span data-ttu-id="66bbe-116">Seadistama sularahakonto sisestusreeglid.</span><span class="sxs-lookup"><span data-stu-id="66bbe-116">Set up cash posting profiles.</span></span>
-   <span data-ttu-id="66bbe-117">Seadistama kassadokumentide numbriseeriad.</span><span class="sxs-lookup"><span data-stu-id="66bbe-117">Set up number sequences for cash document numbering.</span></span>
-   <span data-ttu-id="66bbe-118">Seadistama sularaha- ja pangahalduse parameetrite vaikeväärtused.</span><span class="sxs-lookup"><span data-stu-id="66bbe-118">Set up default values for Cash and bank management parameters.</span></span>
-   <span data-ttu-id="66bbe-119">Seadistama pearaamatus sularahatöölehtede nimed.</span><span class="sxs-lookup"><span data-stu-id="66bbe-119">Set up cash journal names in General ledger.</span></span>

### <a name="set-up-cash-accounts"></a><span data-ttu-id="66bbe-120">Sularahakontode seadistamine</span><span class="sxs-lookup"><span data-stu-id="66bbe-120">Set up cash accounts</span></span>

<span data-ttu-id="66bbe-121">Sularahakonto seadistamiseks avage **Sularaha- ja pangahaldus** &gt; **Pangakontod** &gt; **Sularahakontod** ja sisestage järgmine teave.</span><span class="sxs-lookup"><span data-stu-id="66bbe-121">To set up a Cash, open **Cash and bank management** &gt; **Bank accounts** &gt; **Cash accounts**, and enter the following information.</span></span>

| <span data-ttu-id="66bbe-122">Väli</span><span class="sxs-lookup"><span data-stu-id="66bbe-122">Field</span></span>                 | <span data-ttu-id="66bbe-123">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="66bbe-123">Description</span></span>                                                                                                          |
|-----------------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66bbe-124">Sularaha</span><span class="sxs-lookup"><span data-stu-id="66bbe-124">Cash</span></span>                  | <span data-ttu-id="66bbe-125">Sisestage kood sularahakonto (kassa) tuvastamiseks.</span><span class="sxs-lookup"><span data-stu-id="66bbe-125">Enter a code to identify the cash account (cash).</span></span>                                                                    |
| <span data-ttu-id="66bbe-126">Nimi</span><span class="sxs-lookup"><span data-stu-id="66bbe-126">Name</span></span>                  | <span data-ttu-id="66bbe-127">Sisesta sularahakonto kirjeldus</span><span class="sxs-lookup"><span data-stu-id="66bbe-127">Enter a description of the cash account.</span></span>                                                                             |
| <span data-ttu-id="66bbe-128">Valuuta</span><span class="sxs-lookup"><span data-stu-id="66bbe-128">Currency</span></span>              | <span data-ttu-id="66bbe-129">Valige sularahatehingute vaikevaluutakood.</span><span class="sxs-lookup"><span data-stu-id="66bbe-129">Select the default currency code for cash transactions.</span></span>                                                              |
| <span data-ttu-id="66bbe-130">Numbriseeria grupp</span><span class="sxs-lookup"><span data-stu-id="66bbe-130">Number sequence group</span></span> | <span data-ttu-id="66bbe-131">Kui kassadokumentide numeratsioon peab erinema parameetrites määratud numeratsioonist, sisestage kood.</span><span class="sxs-lookup"><span data-stu-id="66bbe-131">If the numbering of cash documents must differ from the numbering that is specified in the parameters, enter a code.</span></span> |
| <span data-ttu-id="66bbe-132">Veel valuutasid</span><span class="sxs-lookup"><span data-stu-id="66bbe-132">More currencies</span></span>       | <span data-ttu-id="66bbe-133">Märkige see ruut, et võimaldada arvestusvaluutast erinevate valuutade sisestamist.</span><span class="sxs-lookup"><span data-stu-id="66bbe-133">Select this check box to allow currencies that differ from the accounting currency to be posted.</span></span>                     |
| <span data-ttu-id="66bbe-134">Negatiivne kassa</span><span class="sxs-lookup"><span data-stu-id="66bbe-134">Negative cash</span></span>         | <span data-ttu-id="66bbe-135">Märkige see ruut, et võimaldada mis tahes valuutas negatiivseid sularahasaldosid.</span><span class="sxs-lookup"><span data-stu-id="66bbe-135">Select this check box to allow negative cash balances in any currency.</span></span>                                               |

<span data-ttu-id="66bbe-136">Sularahakonto puhul sularahasaldo juhtimise reeglite seadistamiseks valige sularahasaldo ja seejärel klõpsake toimingupaanil vahekaardi **Sularahakonto** rühmas **Saldolimiit** valikut **Saldolimiit**.</span><span class="sxs-lookup"><span data-stu-id="66bbe-136">To set up cash balance control rules for a cash account, select the cash account, and then, on the Action Pane, on the **Cash account** tab, in the **Balance limit** group, click **Balance limit**.</span></span> <span data-ttu-id="66bbe-137">Sisestage järgmine teave.</span><span class="sxs-lookup"><span data-stu-id="66bbe-137">Enter the following information.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="66bbe-138">Väli</span><span class="sxs-lookup"><span data-stu-id="66bbe-138">Field</span></span></th>
<th><span data-ttu-id="66bbe-139">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="66bbe-139">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="66bbe-140">Valuuta tüüp</span><span class="sxs-lookup"><span data-stu-id="66bbe-140">Currency type</span></span></td>
<td><span data-ttu-id="66bbe-141">Valige valuuta tüüp.</span><span class="sxs-lookup"><span data-stu-id="66bbe-141">Select the type of currency:</span></span>
<ul>
<li><span data-ttu-id="66bbe-142"><strong>Arvestusvaluuta</strong> – saate kasutada ettevõtte põhivaluutakoodi.</span><span class="sxs-lookup"><span data-stu-id="66bbe-142"><strong>Accounting currency</strong> – Use the basic company currency code.</span></span></li>
<li><span data-ttu-id="66bbe-143"><strong>Näidatud valuuta</strong> – saate kasutada ettevõtte põhivaluutakoodist erinevat valuutakoodi.</span><span class="sxs-lookup"><span data-stu-id="66bbe-143"><strong>Indicated currency</strong> – Use a currency code that differs from the basic company currency code.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66bbe-144">Valuuta</span><span class="sxs-lookup"><span data-stu-id="66bbe-144">Currency</span></span></td>
<td><span data-ttu-id="66bbe-145">Kui tegite väljal <strong>Valuuta tüüp</strong> valiku <strong>Näidatud valuuta</strong>, valige valuutakood.</span><span class="sxs-lookup"><span data-stu-id="66bbe-145">If you selected <strong>Indicated currency</strong> in the <strong>Currency type</strong> field, select a currency code.</span></span> <span data-ttu-id="66bbe-146">See väli pole saadaval, kui tegite väljal <strong>Valuuta tüüp</strong> valiku <strong>Arvestusvaluuta</strong>.</span><span class="sxs-lookup"><span data-stu-id="66bbe-146">This field is unavailable if you selected <strong>Accounting currency</strong> in the <strong>Currency type</strong> field.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66bbe-147">Saldolimiidi tüüp</span><span class="sxs-lookup"><span data-stu-id="66bbe-147">Balance limit type</span></span></td>
<td><span data-ttu-id="66bbe-148">Valige üks saadaolevatest väärtustest.</span><span class="sxs-lookup"><span data-stu-id="66bbe-148">Select one of the available values:</span></span>
<ul>
<li><span data-ttu-id="66bbe-149"><strong>Maksimaalne</strong> – sularahasaldo ei tohi ületada sularahakonto summat <strong>Saldolimiit</strong> (ülapiir).</span><span class="sxs-lookup"><span data-stu-id="66bbe-149"><strong>Maximum</strong> – The cash balance should not be allowed to exceed the <strong>Balance limit</strong> amount for the cash account (upper bound).</span></span></li>
<li><span data-ttu-id="66bbe-150"><strong>Minimaalne</strong> – sularahasaldo ei tohi langeda alla sularahakonto summat <strong>Saldolimiit</strong> (alapiir).</span><span class="sxs-lookup"><span data-stu-id="66bbe-150"><strong>Minimum</strong> – The cash balance should not be allowed to go below the <strong>Balance limit</strong> amount for the cash account (bottom bound).</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66bbe-151">Kontrolli saldolimiiti</span><span class="sxs-lookup"><span data-stu-id="66bbe-151">Check balance limit</span></span></td>
<td><span data-ttu-id="66bbe-152">Valige, mis juhtub kassadokumentide heakskiiduprotsessi ajal, kui sularahakonto puhul ületatakse summa <strong>Saldolimiit</strong>.</span><span class="sxs-lookup"><span data-stu-id="66bbe-152">Select what occurs during the approval process for cash documents if the <strong>Balance limit</strong> amount for the cash account is exceeded:</span></span>
<ul>
<li><span data-ttu-id="66bbe-153"><strong>Aktsepteeri</strong> – limiidi saab ületada.</span><span class="sxs-lookup"><span data-stu-id="66bbe-153"><strong>Accept</strong> – The limit can be exceeded.</span></span></li>
<li><span data-ttu-id="66bbe-154"><strong>Hoiatus</strong> – limiidi saab ületada, kuid kasutaja saab hoiatusteate.</span><span class="sxs-lookup"><span data-stu-id="66bbe-154"><strong>Warning</strong> – The limit can be exceeded, but the user receives a warning message.</span></span> <span data-ttu-id="66bbe-155">Kassadokument kinnitatakse või kiidetakse heaks.</span><span class="sxs-lookup"><span data-stu-id="66bbe-155">The cash document is confirmed or approved.</span></span></li>
<li><span data-ttu-id="66bbe-156"><strong>Tõrge</strong> – limiiti ei saa ületada.</span><span class="sxs-lookup"><span data-stu-id="66bbe-156"><strong>Error</strong> – The limit can&#39;t be exceeded.</span></span> <span data-ttu-id="66bbe-157">Kasutaja saab tõrketeate ja kassadokumenti ei kinnitata või ei kiideta heaks.</span><span class="sxs-lookup"><span data-stu-id="66bbe-157">The user receives an error message, and the cash document isn&#39;t confirmed or approved.</span></span></li>
</ul>
<span data-ttu-id="66bbe-158">Lisateavet kassadokumentide heakskiiduprotsessi kohta vt selle teema allpool olevast teemast &quot;Sularahakande kinnitamine ja sisestamine&quot;.</span><span class="sxs-lookup"><span data-stu-id="66bbe-158">For more information about the approval process for cash documents, see the &quot;Cash transaction approval and posting&quot; section, later in this topic.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66bbe-159">Saldolimiit</span><span class="sxs-lookup"><span data-stu-id="66bbe-159">Balance limit</span></span></td>
<td><span data-ttu-id="66bbe-160">Sisestage sularahakonto saldolimiit.</span><span class="sxs-lookup"><span data-stu-id="66bbe-160">Enter a limit for the cash account balance.</span></span> <span data-ttu-id="66bbe-161">Summa tuleb sisestada teie määratud valuutas.</span><span class="sxs-lookup"><span data-stu-id="66bbe-161">The amount should be in the currency that you specified.</span></span></td>
</tr>
</tbody>
</table>

### <a name="set-up-cash-posting-profiles"></a><span data-ttu-id="66bbe-162">Sularahakonto sisestusreeglite seadistamine</span><span class="sxs-lookup"><span data-stu-id="66bbe-162">Set up cash posting profiles</span></span>

<span data-ttu-id="66bbe-163">Sularahakonto sisestusreeglid määratlevad sisestused pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="66bbe-163">Cash posting profiles define postings to the general ledger.</span></span> <span data-ttu-id="66bbe-164">Sularahakonto sisestusreeglite seadistamiseks avage **Sularaha-** **ja pangahaldus** &gt; **Seadistus** &gt; **Sularahakonto sisestusreeglid** ning valige või looge sisestusreeglid.</span><span class="sxs-lookup"><span data-stu-id="66bbe-164">To set up a cash posting profile, go to **Cash** **and bank management** &gt; **Setup** &gt; **Cash posting profiles**, and select or create a posting profile.</span></span> <span data-ttu-id="66bbe-165">Sisestage järgmine teave.</span><span class="sxs-lookup"><span data-stu-id="66bbe-165">Enter the following information.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="66bbe-166">Väli</span><span class="sxs-lookup"><span data-stu-id="66bbe-166">Field</span></span></th>
<th><span data-ttu-id="66bbe-167">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="66bbe-167">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="66bbe-168">Kehtib</span><span class="sxs-lookup"><span data-stu-id="66bbe-168">Valid for</span></span></td>
<td><span data-ttu-id="66bbe-169">Valige, kas sisestusreegleid rakendatakse kindlale sularahakontole või kõigile sularahakontodele.</span><span class="sxs-lookup"><span data-stu-id="66bbe-169">Select whether the posting profile applies to a specific cash account or all cash accounts:</span></span>
<ul>
<li><span data-ttu-id="66bbe-170"><strong>Tabel</strong> – kui sularahakonto jaoks on sisestusreeglite rida olemas, kasutatakse seda rida sularahakannete sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="66bbe-170"><strong>Table</strong> – If there is a posting profile line for the cash account, that line is used for cash transaction posting.</span></span></li>
<li><span data-ttu-id="66bbe-171"><strong>Kõik</strong> – sularahakonto jaoks sisestusreeglite rida puudub.</span><span class="sxs-lookup"><span data-stu-id="66bbe-171"><strong>All</strong> – There is no posting profile line for the cash account.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66bbe-172">Sularaha</span><span class="sxs-lookup"><span data-stu-id="66bbe-172">Cash</span></span></td>
<td><span data-ttu-id="66bbe-173">Kui tegite väljal <strong>Kehtib</strong> valiku <strong>Tabel</strong>, määrake sularahakonto.</span><span class="sxs-lookup"><span data-stu-id="66bbe-173">If you selected <strong>Table</strong> in the <strong>Valid for</strong> field, specify the cash account.</span></span> <span data-ttu-id="66bbe-174">See väli jääb tühjaks, kui tegite väljal <strong>Kehtib</strong> valiku <strong>Kõik</strong>.</span><span class="sxs-lookup"><span data-stu-id="66bbe-174">This field remains blank if you selected <strong>All</strong> in the <strong>Valid for</strong> field.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66bbe-175">Pearaamatukonto</span><span class="sxs-lookup"><span data-stu-id="66bbe-175">Ledger account</span></span></td>
<td><span data-ttu-id="66bbe-176">Sisestage selle pearaamatukonto number, mida kasutatakse sularahakonto puhul kliendi koondkontona.</span><span class="sxs-lookup"><span data-stu-id="66bbe-176">Enter the number of the ledger account to use as the summary account for the cash account.</span></span></td>
</tr>
</tbody>
</table>

### <a name="set-up-number-sequences-for-cash-documents"></a><span data-ttu-id="66bbe-177">Kassadokumentide numbriseeriate seadistamine</span><span class="sxs-lookup"><span data-stu-id="66bbe-177">Set up number sequences for cash documents</span></span>

<span data-ttu-id="66bbe-178">Kassadokumentide numbriseeriate seadistamiseks avage **Sularaha- ja pangahaldus** &gt; **Seadistus** &gt; **Sularaha- ja pangahalduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="66bbe-178">To set up number sequences for cash documents, go to **Cash and bank management** &gt; **Setup** &gt; **Cash and bank management parameters**.</span></span> <span data-ttu-id="66bbe-179">Vahekaardil **Numbriseeria** määrake numbriseeria koodid dokumentidele **Kassa korvamisorderid**, **Kassa väljaminekuorderid**, **Kassa paranduskanne** ja **Valuutakursi korrigeerimine** ning väljale **Sularahaaruande number**.</span><span class="sxs-lookup"><span data-stu-id="66bbe-179">On the **Number sequence** tab, specify number sequence codes for the **Cash reimbursement slips**, **Cash disbursement slips**, **Cash correction voucher**, and **Exchange adjustment** documents, and for **Cash report number**.</span></span>

### <a name="set-up-default-values-for-cash-and-bank-management-parameters"></a><span data-ttu-id="66bbe-180">Sularaha- ja pangahalduse parameetrite vaikeväärtuste seadistamine.</span><span class="sxs-lookup"><span data-stu-id="66bbe-180">Set up default values for Cash and bank management parameters</span></span>

<span data-ttu-id="66bbe-181">Sularaha- ja pangahalduse parameetrite vaikeväärtuste seadistamiseks väikeste summade funktsiooni jaoks avage **Sularaha- ja pangahaldus** &gt; **Seadistus** &gt; **Sularaha- ja pangahalduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="66bbe-181">To set up default values for Cash and bank management parameters for the petty cash functionality, go to **Cash and bank management** &gt; **Setup** &gt; **Cash and bank management parameters**.</span></span> <span data-ttu-id="66bbe-182">Vahekaardil **Sularaha** sisestage järgmine teave.</span><span class="sxs-lookup"><span data-stu-id="66bbe-182">On the **Cash** tab, enter the following information.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="66bbe-183">Väli</span><span class="sxs-lookup"><span data-stu-id="66bbe-183">Field</span></span></th>
<th><span data-ttu-id="66bbe-184">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="66bbe-184">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="66bbe-185">Sularaha</span><span class="sxs-lookup"><span data-stu-id="66bbe-185">Cash</span></span></td>
<td><span data-ttu-id="66bbe-186">Valige töölehtedel kasutatav vaikesularahakonto.</span><span class="sxs-lookup"><span data-stu-id="66bbe-186">Select the default cash account in journals.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66bbe-187">Kassaseisu sisestamine</span><span class="sxs-lookup"><span data-stu-id="66bbe-187">Cash posting</span></span></td>
<td><span data-ttu-id="66bbe-188">Sisestage sularahakonto vaikesisestusreeglid, mida kasutatakse, kui muid sisestusreegleid pole määratud.</span><span class="sxs-lookup"><span data-stu-id="66bbe-188">Enter the default cash posting profile that is used if no other posting profile is specified.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66bbe-189">Kontrolli kasutatud kannet</span><span class="sxs-lookup"><span data-stu-id="66bbe-189">Check for voucher used</span></span></td>
<td><span data-ttu-id="66bbe-190">Valige, mis juhtub, kui kassadokumendi numbri kontrollimisel leitakse topeltnumbrid.</span><span class="sxs-lookup"><span data-stu-id="66bbe-190">Select what occurs if duplicate numbers are found during the check of the cash document number:</span></span>
<ul>
<li><span data-ttu-id="66bbe-191">Lükka duplikaat tagasi</span><span class="sxs-lookup"><span data-stu-id="66bbe-191">Reject duplicate</span></span></li>
<li><span data-ttu-id="66bbe-192">Ära luba koopiaid samal rahandusaastal</span><span class="sxs-lookup"><span data-stu-id="66bbe-192">Reject copies within fiscal year</span></span></li>
<li><span data-ttu-id="66bbe-193">Luba duplikaate</span><span class="sxs-lookup"><span data-stu-id="66bbe-193">Accept duplicates</span></span></li>
<li><span data-ttu-id="66bbe-194">Hoiata duplikaatide korral</span><span class="sxs-lookup"><span data-stu-id="66bbe-194">Warn in case of duplicates</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66bbe-195">Kontrolli toimingute limiiti</span><span class="sxs-lookup"><span data-stu-id="66bbe-195">Check operations limit</span></span></td>
<td><span data-ttu-id="66bbe-196">Määrake, mis juhtub, kui vastaspooltega tehtavate toimingute piirmäär on ületatud.</span><span class="sxs-lookup"><span data-stu-id="66bbe-196">Specify what occurs if the limit for operations with counteragents is exceeded:</span></span>
<ul>
<li><span data-ttu-id="66bbe-197"><strong>Aktsepteeri</strong> – limiidi saab ületada.</span><span class="sxs-lookup"><span data-stu-id="66bbe-197"><strong>Accept</strong> – The limit can be exceeded.</span></span></li>
<li><span data-ttu-id="66bbe-198"><strong>Hoiatus</strong> – limiidi saab ületada, kuid kasutaja saab hoiatusteate.</span><span class="sxs-lookup"><span data-stu-id="66bbe-198"><strong>Warning</strong> – The limit can be exceeded, but the user receives a warning message.</span></span> <span data-ttu-id="66bbe-199">Toiming sisestatakse.</span><span class="sxs-lookup"><span data-stu-id="66bbe-199">The operation is posted.</span></span></li>
<li><span data-ttu-id="66bbe-200"><strong>Tõrge</strong> – limiiti ei saa ületada.</span><span class="sxs-lookup"><span data-stu-id="66bbe-200"><strong>Error</strong> – The limit can&#39;t be exceeded.</span></span> <span data-ttu-id="66bbe-201">Kasutaja saab tõrketeate ja toimingut ei sisestata.</span><span class="sxs-lookup"><span data-stu-id="66bbe-201">The user receives an error message, and the operation isn&#39;t posted.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66bbe-202">Kontrollimeetod</span><span class="sxs-lookup"><span data-stu-id="66bbe-202">Validation method</span></span></td>
<td><span data-ttu-id="66bbe-203">Valige kontrollimismeetod, mida kasutatakse toimingute piirsummade ületamise juhtimiseks.</span><span class="sxs-lookup"><span data-stu-id="66bbe-203">Select the validation method that is used to control exceeded limit amounts for operations:</span></span>
<ul>
<li><span data-ttu-id="66bbe-204"><strong>Toiming</strong> – kontrollitakse iga kannet.</span><span class="sxs-lookup"><span data-stu-id="66bbe-204"><strong>Operation</strong> – Validation is done per transaction</span></span></li>
<li><span data-ttu-id="66bbe-205"><strong>Leping</strong> – kontrollitakse iga tehingut, millel on vastaspoolega määratud leping.</span><span class="sxs-lookup"><span data-stu-id="66bbe-205"><strong>Agreement</strong> – Validation is done per transaction that has a specified contract with a counteragent.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66bbe-206">Toimingute limiit</span><span class="sxs-lookup"><span data-stu-id="66bbe-206">Operations limit</span></span></td>
<td><span data-ttu-id="66bbe-207">Sisestage maksimaalne summa, mis on vastaspooltega tehtavate sularahatoimingute puhul lubatud.</span><span class="sxs-lookup"><span data-stu-id="66bbe-207">Enter the maximum amount that is allowed for operations with counteragents in cash.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66bbe-208">Sisestus varasemal kuupäeval</span><span class="sxs-lookup"><span data-stu-id="66bbe-208">Posting on earlier date</span></span></td>
<td><span data-ttu-id="66bbe-209">Märkige see ruut, et lubada sularahakannete sisestamine enne viimast sularahakande kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="66bbe-209">Select this check box to enable cash transactions to be posted before the last date of the cash transaction.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66bbe-210">Dimensioonid</span><span class="sxs-lookup"><span data-stu-id="66bbe-210">Dimensions</span></span></td>
<td><span data-ttu-id="66bbe-211">Sisestage dimensioonid väljadele <strong>Osakonna kood</strong>, <strong>Analüütiline kood</strong> ja <strong>Eesmärgi kood</strong>.</span><span class="sxs-lookup"><span data-stu-id="66bbe-211">Enter dimensions in the <strong>Department code</strong>, <strong>Analytical code</strong>, and <strong>Purpose code</strong> fields.</span></span> <span data-ttu-id="66bbe-212">See teave kajastub kassadokumentide prindivormil.</span><span class="sxs-lookup"><span data-stu-id="66bbe-212">The printing form for cash documents will reflect this information.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66bbe-213">Kasuta kinnitatud olekut</span><span class="sxs-lookup"><span data-stu-id="66bbe-213">Use confirm status</span></span></td>
<td><span data-ttu-id="66bbe-214">Märkige see ruut, et kasutada kassadokumentide kinnitusprotsessi käigus lisaolekut <strong>Kinnitatud</strong>.</span><span class="sxs-lookup"><span data-stu-id="66bbe-214">Select this check box to use an additional status, <strong>Confirmed</strong>, during the approval process for cash documents.</span></span> <span data-ttu-id="66bbe-215">(Lisateavet vt teemast &quot;Sularahakannete kinnitamine ja sisestamine&quot;.)</span><span class="sxs-lookup"><span data-stu-id="66bbe-215">(For more information, see the &quot;Cash transaction approval and posting&quot; section.)</span></span></td>
</tr>
</tbody>
</table>

### <a name="set-up-cash-journal-names-in-general-ledger"></a><span data-ttu-id="66bbe-216">Pearaamatus sularahatöölehtede nimede seadistamine</span><span class="sxs-lookup"><span data-stu-id="66bbe-216">Set up cash journal names in General ledger</span></span>

<span data-ttu-id="66bbe-217">Sularahakannete sisestamiseks töölehe loomiseks avage **Pearaamat** &gt; **Töölehe seadistamine** &gt; **Töölehtede nimed** ja looge uus kirje.</span><span class="sxs-lookup"><span data-stu-id="66bbe-217">To create a journal for cash transaction posting, go to **General ledger** &gt; **Journal setup** &gt; **Journal names**, and create a new record.</span></span> <span data-ttu-id="66bbe-218">Valige väljal **Töölehe tüüp** suvand **Sularaha**.</span><span class="sxs-lookup"><span data-stu-id="66bbe-218">In the **Journal type** field, specify **Cash**.</span></span> <span data-ttu-id="66bbe-219">Määratlege muud vajalikud töölehe vaikeparameetrid.</span><span class="sxs-lookup"><span data-stu-id="66bbe-219">Define other default journal parameters as you require.</span></span>

## <a name="daily-cash-operations-via-a-slip-journal"></a><span data-ttu-id="66bbe-220">Igapäevased sularahatoimingud saatelehe töölehe kaudu</span><span class="sxs-lookup"><span data-stu-id="66bbe-220">Daily cash operations via a Slip journal</span></span>
<span data-ttu-id="66bbe-221">Kassadokumendi loomiseks saatelehe töölehe kaudu avage **Sularaha- ja pangahaldus** &gt; **Sularahakanded** &gt; **Saatelehe tööleht** ning looge uus tööleht.</span><span class="sxs-lookup"><span data-stu-id="66bbe-221">To create a cash document via a Slip journal, go to **Cash and bank management** &gt; **Cash transactions** &gt; **Slip journal**, and create a new journal.</span></span> <span data-ttu-id="66bbe-222">Klõpsake toimingupaanil valikut **Read**.</span><span class="sxs-lookup"><span data-stu-id="66bbe-222">On the Action Pane, click **Lines**.</span></span> <span data-ttu-id="66bbe-223">Lisage uus rida ja sisestage järgmine teave.</span><span class="sxs-lookup"><span data-stu-id="66bbe-223">Add a new line, and enter the following information.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="66bbe-224">Väli</span><span class="sxs-lookup"><span data-stu-id="66bbe-224">Field</span></span></th>
<th><span data-ttu-id="66bbe-225">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="66bbe-225">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="66bbe-226">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="66bbe-226">Date</span></span></td>
<td><span data-ttu-id="66bbe-227">Sisestage kande kuupäev.</span><span class="sxs-lookup"><span data-stu-id="66bbe-227">Enter the date of the transaction.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66bbe-228">Konto</span><span class="sxs-lookup"><span data-stu-id="66bbe-228">Account</span></span></td>
<td><span data-ttu-id="66bbe-229">Valige sularahakonto.</span><span class="sxs-lookup"><span data-stu-id="66bbe-229">Select the cash account.</span></span> <span data-ttu-id="66bbe-230">Vaikimisi määratakse sularahakonto sularaha- ja pangahalduse parameetrites.</span><span class="sxs-lookup"><span data-stu-id="66bbe-230">By default, a cash account is specified in the Cash and bank management parameters.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66bbe-231">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="66bbe-231">Description</span></span></td>
<td><span data-ttu-id="66bbe-232">Sisestage kande jaoks selgitav tekst.</span><span class="sxs-lookup"><span data-stu-id="66bbe-232">Enter explanatory text for the transaction.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66bbe-233">Deebet, kreedit</span><span class="sxs-lookup"><span data-stu-id="66bbe-233">Debit Credit</span></span></td>
<td><span data-ttu-id="66bbe-234">Sisestage kassadokumendi summa ühele järgmistest väljadest.</span><span class="sxs-lookup"><span data-stu-id="66bbe-234">Enter cash document amount in one of these fields:</span></span>
<ul>
<li><span data-ttu-id="66bbe-235"><strong>Deebet</strong> – kasutage seda välja kassa sissetuleku- ja väljaminekuorderite registreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="66bbe-235"><strong>Debit</strong> – Use this field to register cash receipts and a Cash reimbursement slip.</span></span></li>
<li><span data-ttu-id="66bbe-236"><strong>Kreedit</strong> – kasutage seda välja kassa kulu- ja väljaminekuorderite registreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="66bbe-236"><strong>Credit</strong> – Use this field to register cash expenditures and a Cash disbursement slip.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66bbe-237">Vastaskonto tüüp, vastaskonto</span><span class="sxs-lookup"><span data-stu-id="66bbe-237">Offset account type Offset account</span></span></td>
<td><span data-ttu-id="66bbe-238">Valige vastaskonto tüüp ja vastaskonto number.</span><span class="sxs-lookup"><span data-stu-id="66bbe-238">Select an offset account type and offset account number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66bbe-239">Valuuta</span><span class="sxs-lookup"><span data-stu-id="66bbe-239">Currency</span></span></td>
<td><span data-ttu-id="66bbe-240">Valige kande valuutakood.</span><span class="sxs-lookup"><span data-stu-id="66bbe-240">Select the code for the transaction currency.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66bbe-241">Kanne</span><span class="sxs-lookup"><span data-stu-id="66bbe-241">Voucher</span></span></td>
<td><span data-ttu-id="66bbe-242">See väli täidetakse automaatselt töölehe seadistuse põhjal.</span><span class="sxs-lookup"><span data-stu-id="66bbe-242">This field is filled in automatically, based on the journal setup.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66bbe-243">Tellimuse kood</span><span class="sxs-lookup"><span data-stu-id="66bbe-243">Order number</span></span></td>
<td><span data-ttu-id="66bbe-244">Kui sularahakonto jaoks pole muid numbriseeriaid seadistatud, täidetakse see väli automaatselt parameetrites määratud numbriseeria põhjal.</span><span class="sxs-lookup"><span data-stu-id="66bbe-244">If no other number sequence is set up for the cash account, this field is filled in automatically, based on the number sequence that is specified in the parameters.</span></span> <span data-ttu-id="66bbe-245">Saate sellele väljale sisestada soovi korral tellimuse numbri käsitsi.</span><span class="sxs-lookup"><span data-stu-id="66bbe-245">You can manually enter an order number in this field as you require.</span></span> <span data-ttu-id="66bbe-246">Kassadokumentide numeratsiooni ebajärjekindluse vältimiseks rakendatakse järgmist reeglit: varasema toimingukuupäevaga kassadokumendi number ei saa olla suurem kui hilisema toimingukuupäevaga kassadokumendi number.</span><span class="sxs-lookup"><span data-stu-id="66bbe-246">To prevent inconsistence in cash document numbering, the following control is applied: the number of a cash document that has an earlier date of operation can&#39;t be higher than number of a cash document that has a later date of operation.</span></span> <span data-ttu-id="66bbe-247">Kui te ei soovi seda reeglit rakendada, märkige sularaha- ja pangahalduse parameetrites ruut <strong>Sisestamine varasemal kuupäeval</strong>.</span><span class="sxs-lookup"><span data-stu-id="66bbe-247">If you don&#39;t require this control, select the <strong>Posting on earlier date</strong> check box in the Cash and bank management parameters.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66bbe-248">Kinnitamise olek</span><span class="sxs-lookup"><span data-stu-id="66bbe-248">Approval status</span></span></td>
<td><span data-ttu-id="66bbe-249">Esimese kande olek on <strong>Pole</strong>.</span><span class="sxs-lookup"><span data-stu-id="66bbe-249">The first transaction status is <strong>None</strong>.</span></span> <span data-ttu-id="66bbe-250">Teavet kande oleku määramise kohta vt teemast &quot;Sularahakannete kinnitamine ja sisestamine&quot;.</span><span class="sxs-lookup"><span data-stu-id="66bbe-250">For information about how to set the transaction status, See the &quot;Cash transaction approval and posting&quot; section.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66bbe-251">Dokumendi tüüp </span><span class="sxs-lookup"><span data-stu-id="66bbe-251">Document type</span></span></td>
<td><span data-ttu-id="66bbe-252">See väli vahekaardil <strong>Kassaorder</strong> täidetakse automaatselt kassadokumenti sisestatud summa põhjal.</span><span class="sxs-lookup"><span data-stu-id="66bbe-252">This field on the <strong>Cash order</strong> tab is filled in automatically, based on the amount that you entered for the cash document:</span></span>
<ul>
<li><span data-ttu-id="66bbe-253"><strong>Kassa korvamisorder</strong> – seda väärtust kasutatakse, kui sisestasite summa sularahakonto väljale <strong>Deebet</strong>.</span><span class="sxs-lookup"><span data-stu-id="66bbe-253"><strong>Cash reimbursement slip</strong> – This value is used if you entered an amount in the <strong>Debit</strong> field for the cash account.</span></span></li>
<li><span data-ttu-id="66bbe-254"><strong>Kassa väljaminekuorder</strong> – seda väärtust kasutatakse, kui sisestasite summa sularahakonto väljale <strong>Kreedit</strong>.</span><span class="sxs-lookup"><span data-stu-id="66bbe-254"><strong>Cash disbursement slip</strong> – This value is used if you entered an amount in the <strong>Credit</strong> field for the cash account</span></span></li>
<li><span data-ttu-id="66bbe-255"><strong>Parandus</strong> – olete sisestanud sularahakonto väljale <strong>Deebet</strong> või <strong>Kreedit</strong> negatiivse summa.</span><span class="sxs-lookup"><span data-stu-id="66bbe-255"><strong>Correction</strong> – You entered a negative amount in either the <strong>Debit</strong> field or the <strong>Credit</strong> field for the cash account.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66bbe-256">Käibemaksugrupp</span><span class="sxs-lookup"><span data-stu-id="66bbe-256">Sales tax group</span></span></td>
<td><span data-ttu-id="66bbe-257">Määrake käibemaksugrupp toimingu maksude arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="66bbe-257">Specify a sales tax group to calculate taxes on the operation.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66bbe-258">Kauba käibemaksugrupp</span><span class="sxs-lookup"><span data-stu-id="66bbe-258">Item sales tax group</span></span></td>
<td><span data-ttu-id="66bbe-259">Määrake kauba käibemaksugrupp toimingu maksude arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="66bbe-259">Specify an item sales tax group to calculate taxes on the operation.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66bbe-260">Põhjus</span><span class="sxs-lookup"><span data-stu-id="66bbe-260">Reason</span></span></td>
<td><span data-ttu-id="66bbe-261">Sisestage vahekaardil <strong>Kassaorder</strong> kande teemat kirjeldav tekst.</span><span class="sxs-lookup"><span data-stu-id="66bbe-261">On the <strong>Cash order</strong> tab, enter text that describes the transaction subject.</span></span> <span data-ttu-id="66bbe-262">See tekst prinditakse kassaorderi aruandlusvormile.</span><span class="sxs-lookup"><span data-stu-id="66bbe-262">This text will be printed on the cash slip reporting form.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66bbe-263">Dokumendi kuupäev</span><span class="sxs-lookup"><span data-stu-id="66bbe-263">Document Date</span></span></td>
<td><span data-ttu-id="66bbe-264">Sisestage kande põhjuseks oleva põhidokumendi (nt ettemaksuaruanded, arve või tellimus) kirjeldus, number ja kuupäev.</span><span class="sxs-lookup"><span data-stu-id="66bbe-264">Enter the description, number, and date of the primary document that is the reason for the transaction (for example, advance reports, invoice, or order).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66bbe-265">Esindaja tüüp</span><span class="sxs-lookup"><span data-stu-id="66bbe-265">Representative type</span></span></td>
<td><span data-ttu-id="66bbe-266">See väli võib sisaldada üht järgmistest väärtustest.</span><span class="sxs-lookup"><span data-stu-id="66bbe-266">This field can have the following values:</span></span>
<ul>
<li><span data-ttu-id="66bbe-267"><strong>Töötaja</strong> – otsing <strong>Esindaja</strong> sisaldab töötajate loendit, kui väljal <strong>Vastaskonto</strong> on valitud <strong>Pearaamat</strong> või <strong>Pank</strong>, või vastaspoole kontaktisikute loendit, kui väljal <strong>Vastaskonto</strong> on valitud <strong>Klient</strong> või <strong>Hankija</strong>.</span><span class="sxs-lookup"><span data-stu-id="66bbe-267"><strong>Worker</strong> – The <strong>Representative</strong> lookup contains a list of employees if the <strong>Offset account</strong> field is set to <strong>Ledger</strong> or <strong>Bank</strong>, or a list of the counteragent&#39;s contact persons if the <strong>Offset account</strong> field is set to <strong>Customer</strong> or <strong>Vendor</strong>.</span></span> <span data-ttu-id="66bbe-268">Esindajate seadistamiseks avage <strong>Põhiline</strong> &gt; <strong>Seadistus</strong> &gt; <strong>Kontaktid</strong> &gt; <strong>Kontaktisik</strong>.</span><span class="sxs-lookup"><span data-stu-id="66bbe-268">To set up representatives, go to <strong>Basic</strong> &gt; <strong>Setup</strong> &gt; <strong>Contacts</strong> &gt; <strong>Contact person</strong>.</span></span></li>
<li><span data-ttu-id="66bbe-269"><strong>Muu</strong> – otsing <strong>Esindaja</strong> sisaldab muude klientide loendit.</span><span class="sxs-lookup"><span data-stu-id="66bbe-269"><strong>Other</strong> – The <strong>Representative</strong> lookup contains a list of other clients.</span></span> <span data-ttu-id="66bbe-270">Saajate, keda tabelis <strong>Kliendid</strong> või <strong>Hankijad</strong> ei kuvata, seadistamiseks avage <strong>Pearaamat</strong> &gt; <strong>Saajad</strong>.</span><span class="sxs-lookup"><span data-stu-id="66bbe-270">To set up receivers who don&#39;t appear in the <strong>Customers</strong> or <strong>Vendors</strong> table, go to <strong>General ledger</strong> &gt; <strong>Receivers</strong>.</span></span> <span data-ttu-id="66bbe-271">See tüüp on saadaval ainult Läti puhul.</span><span class="sxs-lookup"><span data-stu-id="66bbe-271">This type is available only for Latvia.</span></span> <span data-ttu-id="66bbe-272">(Konfiguratsioonivõti <strong>CSELatvia</strong> peab olema lubatud.)</span><span class="sxs-lookup"><span data-stu-id="66bbe-272">(The <strong>CSELatvia</strong> configuration key should be enabled.)</span></span></li>
<li><span data-ttu-id="66bbe-273"><strong>Hankija</strong> – otsing <strong>Esindaja</strong> sisaldab hankijate loendit.</span><span class="sxs-lookup"><span data-stu-id="66bbe-273"><strong>Vendor</strong> – The <strong>Representative</strong> lookup contains a list of vendors.</span></span> <span data-ttu-id="66bbe-274">Hankijate seadistamiseks avage <strong>Ostureskontro</strong> &gt; <strong>Hankijad</strong>.</span><span class="sxs-lookup"><span data-stu-id="66bbe-274">To set up vendors, go to <strong>Accounts payable</strong> &gt; <strong>Vendors</strong>.</span></span></li>
<li><span data-ttu-id="66bbe-275"><strong>Klient</strong> – otsing <strong>Esindaja</strong> sisaldab klientide loendit.</span><span class="sxs-lookup"><span data-stu-id="66bbe-275"><strong>Customer</strong> – The <strong>Representative</strong> lookup contains a list of customers.</span></span> <span data-ttu-id="66bbe-276">Klientide seadistamiseks avage <strong>Müügireskontro</strong> &gt; <strong>Kliendid</strong>.</span><span class="sxs-lookup"><span data-stu-id="66bbe-276">To set up customers, go to <strong>Accounts receivable</strong> &gt; <strong>Customers</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66bbe-277">Esindaja</span><span class="sxs-lookup"><span data-stu-id="66bbe-277">Representative</span></span></td>
<td><span data-ttu-id="66bbe-278">Valige esindaja, kelle tüübi määrasite väljal <strong>Esindaja tüüp</strong>.</span><span class="sxs-lookup"><span data-stu-id="66bbe-278">Select a representative of the type that you specified in the <strong>Representative type</strong> field.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66bbe-279">Inimese nimi</span><span class="sxs-lookup"><span data-stu-id="66bbe-279">Name of person</span></span></td>
<td><span data-ttu-id="66bbe-280">See väli täidetakse automaatselt väljade <strong>Vastaskonto</strong> ja <strong>Esindaja</strong> põhjal.</span><span class="sxs-lookup"><span data-stu-id="66bbe-280">This field is filled in automatically, based on the <strong>Offset account</strong> and <strong>Representative</strong> fields.</span></span> <span data-ttu-id="66bbe-281">See teave kajastub kassaorderite prindivormil.</span><span class="sxs-lookup"><span data-stu-id="66bbe-281">The printing form for cash slips will reflect this information.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66bbe-282">ID-kaart</span><span class="sxs-lookup"><span data-stu-id="66bbe-282">Identity card</span></span></td>
<td><span data-ttu-id="66bbe-283">See väli täidetakse automaatselt kontaktisiku (esindaja) ID-kaardi andmete põhjal.</span><span class="sxs-lookup"><span data-stu-id="66bbe-283">This field is filled in automatically, based on the identity card data for the contact person (representative).</span></span> <span data-ttu-id="66bbe-284">Kui väljal <strong>Vastaskonto tüüp</strong> on valitud <strong>Avansisaaja</strong> ja väli <strong>Vastaskonto</strong> on määratud töövõtja koodile, saab kassaordereid või kulusid teha töövõtjalt või töövõtjale.</span><span class="sxs-lookup"><span data-stu-id="66bbe-284">If the <strong>Offset account type</strong> field is set to <strong>Advance holder</strong>, and the <strong>Offset account</strong> field is set to an employee number, cash receipts or expenditures can be done from or to the employee.</span></span> <span data-ttu-id="66bbe-285">Sellisel juhul täidetakse väli <strong>ID-kaart</strong> automaatselt, kasutades ID-kaardi andmeid tabelist <strong>Töövõtja</strong> (<strong>Personaliarvestus</strong> &gt; <strong>Töövõtjate tabel</strong>).</span><span class="sxs-lookup"><span data-stu-id="66bbe-285">In this case the <strong>Identity card</strong> field is filled in automatically by using data for the identity card from the <strong>Employee</strong> table (<strong>Staff accounting</strong> &gt; <strong>Employee table</strong>).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66bbe-286">Eesmärk</span><span class="sxs-lookup"><span data-stu-id="66bbe-286">Purpose</span></span></td>
<td><span data-ttu-id="66bbe-287">Tabelis <strong>Eesmärk</strong> saate määratleda kande summa ühe või mitu sihtkoodi.</span><span class="sxs-lookup"><span data-stu-id="66bbe-287">In the <strong>Purpose</strong> table, define one or more destination codes for the transaction amount.</span></span> <span data-ttu-id="66bbe-288">Valige sihtkood väljal <strong>Eesmärk</strong> ja sisestage selgitus väljale <strong>Kande tekst</strong>.</span><span class="sxs-lookup"><span data-stu-id="66bbe-288">Select a destination code in the <strong>Purpose</strong> field, and enter an explanation in the <strong>Transaction text</strong> field.</span></span> <span data-ttu-id="66bbe-289">Sisestage väljale <strong>Summa</strong> summa kandevaluutas.</span><span class="sxs-lookup"><span data-stu-id="66bbe-289">In the <strong>Amount</strong> field, enter an amount in the transaction currency.</span></span> <span data-ttu-id="66bbe-290">Väljal <strong>Protsent</strong> kuvatakse sihtsumma ja kande kogusumma suhe protsentides.</span><span class="sxs-lookup"><span data-stu-id="66bbe-290">The <strong>Percent</strong> field shows, as a percentage, the ratio of the destination amount to the total transaction amount.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66bbe-291">Jääk</span><span class="sxs-lookup"><span data-stu-id="66bbe-291">Remainder</span></span></td>
<td><span data-ttu-id="66bbe-292">Arvutatud järelejäänud summa.</span><span class="sxs-lookup"><span data-stu-id="66bbe-292">The remaining amount that is calculated.</span></span> <span data-ttu-id="66bbe-293">Pange tähele, et kande kogusumma tuleb määrata sihtkoodidele.</span><span class="sxs-lookup"><span data-stu-id="66bbe-293">Note that the whole transaction amount must be assigned to destination codes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66bbe-294">Ametiisikud</span><span class="sxs-lookup"><span data-stu-id="66bbe-294">Officials</span></span></td>
<td><span data-ttu-id="66bbe-295">Vahekaardil <strong>Ametiisikud</strong> saate määrata vastutavate isikute (direktor, pearaamatupidaja ja kassiir) nimed ja ametinimetused.</span><span class="sxs-lookup"><span data-stu-id="66bbe-295">On the <strong>Officials</strong> tab, specify the names and titles for responsible persons: Director, Chief accountant, and Cashier.</span></span> <span data-ttu-id="66bbe-296">Välja <strong>Ametikoht</strong> väärtused määratletakse ametiisikute seadistusega lehe <strong>Ametiisikud</strong> vahekaartidel <strong>Üldine</strong> ja <strong>Pearaamat</strong> (<strong>Põhiline</strong> &gt; <strong>Seadistus</strong> &gt; <strong>Kontaktid</strong> &gt; <strong>Ametiisikud</strong>).</span><span class="sxs-lookup"><span data-stu-id="66bbe-296">The <strong>Position</strong> values are determined by the setup of officials on the <strong>General</strong> and <strong>Ledger</strong> tabs of the <strong>Officials</strong> page (<strong>Basic</strong> &gt; <strong>Setup</strong> &gt; <strong>Contacts</strong> &gt; <strong>Officials</strong>).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66bbe-297">Ettemaks</span><span class="sxs-lookup"><span data-stu-id="66bbe-297">Prepayment</span></span></td>
<td><span data-ttu-id="66bbe-298">Märkige see ruut, kui kanne on ettemakse.</span><span class="sxs-lookup"><span data-stu-id="66bbe-298">Select this check box if the transaction is a prepayment.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66bbe-299">Sisestusreeglid</span><span class="sxs-lookup"><span data-stu-id="66bbe-299">Posting profile</span></span></td>
<td><span data-ttu-id="66bbe-300">Saate sisestada sularahakonto sisestusreeglid.</span><span class="sxs-lookup"><span data-stu-id="66bbe-300">Enter the posting profile for the cash account.</span></span> <span data-ttu-id="66bbe-301">Vaikimisi kasutatakse sularaha- ja pangahalduse parameetrites määratud sisestusreegleid.</span><span class="sxs-lookup"><span data-stu-id="66bbe-301">By default, the posting profile that is specified in the Cash and bank management parameters is used.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66bbe-302">Vastaskontoga sisestamise reeglid</span><span class="sxs-lookup"><span data-stu-id="66bbe-302">Offset posting profile</span></span></td>
<td><span data-ttu-id="66bbe-303">Saate sisestada valitud vastaskonto sisestusreeglid.</span><span class="sxs-lookup"><span data-stu-id="66bbe-303">Enter the posting profile for the selected offset account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66bbe-304">Kogusumma</span><span class="sxs-lookup"><span data-stu-id="66bbe-304">Total amount</span></span></td>
<td><span data-ttu-id="66bbe-305">Lehe alaosas asuvas väljagrupis <strong>Kogusumma</strong> oleval väljal <strong>Korv.</strong> kuvatakse kogusumma, mis arvutatakse kõigi praegusele töölehele sisestatud kassa korvamisorderite kohta, ning väljal <strong>Väljam.</strong> kuvatakse kõigi kassa väljaminekuorderite kogusumma.</span><span class="sxs-lookup"><span data-stu-id="66bbe-305">In the <strong>Total amount</strong> field group at the bottom of the page, the <strong>Reimb</strong> field shows the total that is calculated for all Cash reimbursement slips that are entered in the current journal, and the <strong>Disb</strong> field shows the total for all Cash disbursement slips.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="66bbe-306">Töölehekannete vaatamiseks klõpsake toimingupaanil nuppu **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="66bbe-306">To check journal entries, on the Action Pane, click **Validate**.</span></span>

## <a name="daily-cash-operations-via-a-general-journal"></a><span data-ttu-id="66bbe-307">Igapäevased sularahatoimingud päevaraamatu töölehe kaudu</span><span class="sxs-lookup"><span data-stu-id="66bbe-307">Daily cash operations via a General journal</span></span>
<span data-ttu-id="66bbe-308">Sularahakannete loomiseks pearaamatu töölehe kaudu avage **Pearaamat** &gt; **Töölehe sisestused** &gt; **Päevaraamatud** ja looge uus tööleht.</span><span class="sxs-lookup"><span data-stu-id="66bbe-308">To create a cash transaction via a General journal, go to **General ledger** &gt; **Journal entries** &gt; **General journals**, and create a new journal.</span></span> <span data-ttu-id="66bbe-309">Klõpsake toimingupaanil valikut **Read**.</span><span class="sxs-lookup"><span data-stu-id="66bbe-309">On the Action Pane, click **Lines**.</span></span> <span data-ttu-id="66bbe-310">Lisage uus rida ja sisestage järgmine teave.</span><span class="sxs-lookup"><span data-stu-id="66bbe-310">Add a new line, and enter the following information.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="66bbe-311">Väli</span><span class="sxs-lookup"><span data-stu-id="66bbe-311">Field</span></span></th>
<th><span data-ttu-id="66bbe-312">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="66bbe-312">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="66bbe-313">Kuupäev</span><span class="sxs-lookup"><span data-stu-id="66bbe-313">Date</span></span></td>
<td><span data-ttu-id="66bbe-314">Sisestage kande kuupäev.</span><span class="sxs-lookup"><span data-stu-id="66bbe-314">Enter the date of the transaction.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66bbe-315">Konto tüüp</span><span class="sxs-lookup"><span data-stu-id="66bbe-315">Account type</span></span></td>
<td><span data-ttu-id="66bbe-316">Valige <strong>Väikesed summad</strong>.</span><span class="sxs-lookup"><span data-stu-id="66bbe-316">Select <strong>Petty cash</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66bbe-317">Konto</span><span class="sxs-lookup"><span data-stu-id="66bbe-317">Account</span></span></td>
<td><span data-ttu-id="66bbe-318">Valige sularahakonto number.</span><span class="sxs-lookup"><span data-stu-id="66bbe-318">Select the cash account number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66bbe-319">Kande tekst</span><span class="sxs-lookup"><span data-stu-id="66bbe-319">Transaction text</span></span></td>
<td><span data-ttu-id="66bbe-320">Sisestage kande jaoks selgitav tekst.</span><span class="sxs-lookup"><span data-stu-id="66bbe-320">Enter explanatory text for the transaction.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66bbe-321">Deebet, kreedit</span><span class="sxs-lookup"><span data-stu-id="66bbe-321">Debit Credit</span></span></td>
<td><span data-ttu-id="66bbe-322">Sisestage kassadokumendi summa ühele järgmistest väljadest.</span><span class="sxs-lookup"><span data-stu-id="66bbe-322">Enter cash document amount in one of these fields:</span></span>
<ul>
<li><span data-ttu-id="66bbe-323"><strong>Deebet</strong> – kasutage seda välja kassa sissetuleku- ja väljaminekuorderite registreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="66bbe-323"><strong>Debit</strong> – Use this field to register cash receipts and a Cash reimbursement slip.</span></span></li>
<li><span data-ttu-id="66bbe-324"><strong>Kreedit</strong> – kasutage seda välja kassa kulu- ja väljaminekuorderite registreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="66bbe-324"><strong>Credit</strong> – Use this field to register cash expenditures and a Cash disbursement slip.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66bbe-325">Vastaskonto tüüp, vastaskonto</span><span class="sxs-lookup"><span data-stu-id="66bbe-325">Offset account type Offset account</span></span></td>
<td><span data-ttu-id="66bbe-326">Valige vastaskonto tüüp ja vastaskonto number.</span><span class="sxs-lookup"><span data-stu-id="66bbe-326">Select an offset account type and offset account number.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66bbe-327">Valuuta</span><span class="sxs-lookup"><span data-stu-id="66bbe-327">Currency</span></span></td>
<td><span data-ttu-id="66bbe-328">Valige kande valuutakood.</span><span class="sxs-lookup"><span data-stu-id="66bbe-328">Select the code for the transaction currency.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="66bbe-329">Vahekaardil **Arve** saate määrata valitud konto ja vastaskonto sisestusreeglid.</span><span class="sxs-lookup"><span data-stu-id="66bbe-329">On the **Invoice** tab, you can specify posting profiles for the selected account and offset account.</span></span> <span data-ttu-id="66bbe-330">Kui registreeritud kanne on ettemakse, märkige ruut **Ettemakse** vahekaardil **Makse**. Täitke väljagrupis **Esindaja** väljad, nagu saatelehe töölehtede puhul, et printida välja aruanne **Sularaha**.</span><span class="sxs-lookup"><span data-stu-id="66bbe-330">If the registered transaction is a prepayment, select the **Prepayment** check box on the **Payment** tab. In the **Representative** field group, fill in the fields as you did for the Slip journal lines to print on the **Cash** report.</span></span> <span data-ttu-id="66bbe-331">Töölehekannete vaatamiseks klõpsake toimingupaanil nuppu **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="66bbe-331">To check journal entries, on the Action Pane, click **Validate**.</span></span>

## <a name="cash-transaction-approval-and-posting"></a><span data-ttu-id="66bbe-332">Sularahakande kinnitamine ja sisestamine</span><span class="sxs-lookup"><span data-stu-id="66bbe-332">Cash transaction approval and posting</span></span>
<span data-ttu-id="66bbe-333">Sularahakannete puhul saab rakendada järgmisi olekuid: **Pole**, **Kinnitatud**, **Heaks kiidetud**, **Tagasi lükatud**.</span><span class="sxs-lookup"><span data-stu-id="66bbe-333">For cash transactions, the following statuses can be applied: **None**, **Confirmed**, **Approved**, and **Rejected**.</span></span> <span data-ttu-id="66bbe-334">Parameeter **Kasuta kinnituse olekut** vahekaardi **Sularaha** kiirkaardil **Kinnitamine** (**Sularaha- ja pangahaldus** &gt; **Seadistus** &gt; **Sularaha- ja pangahalduse parameetrid**) võimaldab aktiveerida kaks lisaolekut: **Kinnitatud** ja **Tagasi lükatud**.</span><span class="sxs-lookup"><span data-stu-id="66bbe-334">A **Use confirm status** parameter on the **Approval** FastTab of the **Cash** tab at **Cash and bank management** &gt; **Setup** &gt; **Cash and bank management parameters** lets you activate two additional statuses: **Confirmed** and **Rejected**.</span></span> <span data-ttu-id="66bbe-335">Kinnitus on asjakohane, kui kassadokumendid on väljastatud ning kaks töövõtjat – raamatupidaja ja kassiir – kasutavad ühiselt kassaordereid või kulusid.</span><span class="sxs-lookup"><span data-stu-id="66bbe-335">Confirmation is appropriate when cash documents are issued, and cash receipts or expenditures are shared between two employees: accountant and cashier.</span></span> <span data-ttu-id="66bbe-336">Funktsioon **Lähtesta olek** muudab kande praegust olekut.</span><span class="sxs-lookup"><span data-stu-id="66bbe-336">The **Reset status** function changes the current transaction status.</span></span> <span data-ttu-id="66bbe-337">Olek **Heaks kiidetud** muutub olekuks **Kinnitatud** ja olek **Kinnitatud** muutub olekuks **Pole**.</span><span class="sxs-lookup"><span data-stu-id="66bbe-337">**Approved** becomes **Confirmed**, and **Confirmed** becomes **None**.</span></span> <span data-ttu-id="66bbe-338">Sularahatöölehe sisestusi saab redigeerida ainult siis, kui olek on **Pole**.</span><span class="sxs-lookup"><span data-stu-id="66bbe-338">Cash journal entries can be edited only when the status is **None**.</span></span> <span data-ttu-id="66bbe-339">Sularahakandeid saab tagasi lükata ainult siis, kui kande olek on **Kinnitatud**.</span><span class="sxs-lookup"><span data-stu-id="66bbe-339">Cash transactions can be rejected only if the transaction status is **Confirmed**.</span></span> <span data-ttu-id="66bbe-340">Tagasi lüktatud kassadokumendid kaasatakse aruandesse **Kassadokumentide registreerimise tööleht**, kuid need ei kajastu aruandes **Kassaraamat**.</span><span class="sxs-lookup"><span data-stu-id="66bbe-340">Rejected cash documents are included on the **Journal of registration of cash documents** report, but they aren't reflected on the **Cash book** report.</span></span> <span data-ttu-id="66bbe-341">Kande kinnitamiseks valige vastav saatelehe töölehe rida ja klõpsake valikuid **Dokumentide heakskiitmine** &gt; **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="66bbe-341">To confirm a transaction, select the corresponding Slip journal line, and then click **Documents approval** &gt; **Confirm**.</span></span> <span data-ttu-id="66bbe-342">Luuakse tellimuse number, võttes aluseks määratud numbriseeria.</span><span class="sxs-lookup"><span data-stu-id="66bbe-342">An order number is generated, based on the specified number sequence.</span></span> <span data-ttu-id="66bbe-343">Kande olekuks muutub **Kinnitatud** ja töölehe rida ei saa enam redigeerida.</span><span class="sxs-lookup"><span data-stu-id="66bbe-343">The transaction status is changed to **Confirmed**, and you can no longer edit the journal line.</span></span> <span data-ttu-id="66bbe-344">Sularahakonto saldo jääb muutumatuks.</span><span class="sxs-lookup"><span data-stu-id="66bbe-344">The cash account balance remains unchanged.</span></span> <span data-ttu-id="66bbe-345">Kassadokumendi tagasilükkamiseks klõpsake valikuid **Dokumentide heakskiitmine** &gt; **Lükka tagasi**.</span><span class="sxs-lookup"><span data-stu-id="66bbe-345">To reject a cash document, click **Documents approval** &gt; **Reject**.</span></span> <span data-ttu-id="66bbe-346">See suvand on saadaval ainult dokumentide puhul, mille olek on **Kinnitatud**.</span><span class="sxs-lookup"><span data-stu-id="66bbe-346">This option is available only for documents that have **Confirmed** status.</span></span> <span data-ttu-id="66bbe-347">Kande heakskiitmiseks valige vastav saatelehe töölehe rida ja klõpsake valikuid **Dokumentide heakskiitmine** &gt; **Kiida heaks**.</span><span class="sxs-lookup"><span data-stu-id="66bbe-347">To approve a transaction, select the corresponding Slip journal line, and then click **Documents approval** &gt; **Approve**.</span></span> <span data-ttu-id="66bbe-348">Olek **Heaks kiidetud** näitab, et sularaha on vastu võetud või kulutatud.</span><span class="sxs-lookup"><span data-stu-id="66bbe-348">The **Approved** status indicates that cash funds are received or expended.</span></span> <span data-ttu-id="66bbe-349">Kassasaldo on muutunud.</span><span class="sxs-lookup"><span data-stu-id="66bbe-349">The cash balance is changed.</span></span> <span data-ttu-id="66bbe-350">Sularahakannet saab sisestada.</span><span class="sxs-lookup"><span data-stu-id="66bbe-350">The cash transaction can be posted.</span></span> <span data-ttu-id="66bbe-351">Oleku **Heaks kiidetud** tühistamiseks ja ennistamiseks väärtusele **Pole** klõpsake valikuid **Dokumentide heakskiitmine** &gt; **Lähtesta olek**.</span><span class="sxs-lookup"><span data-stu-id="66bbe-351">To cancel an **Approved** status and reset the status to **None**, click **Documents approval** &gt; **Reset status**.</span></span> <span data-ttu-id="66bbe-352">Sisestada saab ainult heakskiidetud sularahakandeid.</span><span class="sxs-lookup"><span data-stu-id="66bbe-352">Only approved cash transactions can be posted.</span></span> <span data-ttu-id="66bbe-353">Töölehe sisestamiseks klõpsake valikuid **Sisesta** &gt; **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="66bbe-353">To post a journal, click **Post** &gt; **Post**.</span></span>

## <a name="print-a-cash-order"></a><span data-ttu-id="66bbe-354">Kassaorderi printimine</span><span class="sxs-lookup"><span data-stu-id="66bbe-354">Print a cash order</span></span>
<span data-ttu-id="66bbe-355">Kassaorderi printimiseks valige saatelehe töölehe rida ja seejärel klõpsake toimingupaanil valikuid **Prindi** &gt; **Kassaorderi aruanne**.</span><span class="sxs-lookup"><span data-stu-id="66bbe-355">To print a cash order, select a Slip journal line, and then, on the Action Pane, click **Print** &gt; **Cash order report**.</span></span> <span data-ttu-id="66bbe-356">Süsteem loob prindivormi kas kassa korvamisorderi või kassa väljaminekuorderi kohta olenevalt sellest, kas summa on sisestatud valitud real väljale **Deebet** või **Kreedit**.</span><span class="sxs-lookup"><span data-stu-id="66bbe-356">The system generates a printing form for either a Cash reimbursement slip or a Cash disbursement slip, depending on whether an amount is entered in the **Debit** field the or **Credit** field for the selected line:</span></span>

-   <span data-ttu-id="66bbe-357">Kui summa on väljal **Deebet**: kassa korvamisorder</span><span class="sxs-lookup"><span data-stu-id="66bbe-357">If there is an amount in the **Debit** field: Cash reimbursement slip</span></span>
-   <span data-ttu-id="66bbe-358">Kui summa on väljal **Kreedit**: kassa väljaminekuorder</span><span class="sxs-lookup"><span data-stu-id="66bbe-358">If there is an amount in the **Credit** field: Cash disbursement slip</span></span>

<span data-ttu-id="66bbe-359">Printida saab saatelehe töölehe ridu, mille olek on **Kinnitatud**, **Heaks kiidetud** või **Tagasi lükatud**.</span><span class="sxs-lookup"><span data-stu-id="66bbe-359">Slip journal lines that have **Confirmed**, **Approved**, or **Rejected** status can be printed.</span></span> <span data-ttu-id="66bbe-360">Samuti saate printida kassaorderi dokumente jaotises **Sularaha- ja pangahaldus** &gt; **Päringud ja aruanded** &gt; **Kassaorder**.</span><span class="sxs-lookup"><span data-stu-id="66bbe-360">You can also print cash order documents at **Cash and bank management** &gt; **Inquires and reports** &gt; **Cash order**.</span></span>

## <a name="periodic-tasks"></a><span data-ttu-id="66bbe-361">Perioodilised ülesanded</span><span class="sxs-lookup"><span data-stu-id="66bbe-361">Periodic tasks</span></span>
<span data-ttu-id="66bbe-362">Jaotises **Sularaha- ja pangahaldus** &gt; **Perioodilised ülesanded** saab teha järgmist.</span><span class="sxs-lookup"><span data-stu-id="66bbe-362">The following tasks can be performed at **Cash and bank management** &gt; **Periodic tasks**.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="66bbe-363">Perioodiline ülesanne</span><span class="sxs-lookup"><span data-stu-id="66bbe-363">Periodic task</span></span></th>
<th><span data-ttu-id="66bbe-364">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="66bbe-364">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="66bbe-365">Kontrolli saldolimiiti</span><span class="sxs-lookup"><span data-stu-id="66bbe-365">Check balance limit</span></span></td>
<td><span data-ttu-id="66bbe-366">Saate kontrollida valitud sularahakonto saldot määratud kuupäeval ja kuvada tulemuse teabesõnumis.</span><span class="sxs-lookup"><span data-stu-id="66bbe-366">Check the balance for the selected cash account on the specified date, and show the result in an information message.</span></span> <span data-ttu-id="66bbe-367">Saldoarvutusse saab kaasata ainult heakskiidetud kandeid.</span><span class="sxs-lookup"><span data-stu-id="66bbe-367">Only approved transactions can be counted in the balance calculation.</span></span> <span data-ttu-id="66bbe-368">Kandeid märkega <strong>Palgaarvestuseks</strong> arvesse ei võeta.</span><span class="sxs-lookup"><span data-stu-id="66bbe-368">Transactions that are marked as <strong>For payroll</strong> aren&#39;t considered.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66bbe-369">Kassasaldo ümberarvutamine</span><span class="sxs-lookup"><span data-stu-id="66bbe-369">Cash balance recalculation</span></span></td>
<td><span data-ttu-id="66bbe-370">Selle ülesandega saate kontrollida, kas sularahakontode pearaamatusaldod vastavad sularahasaldole.</span><span class="sxs-lookup"><span data-stu-id="66bbe-370">Use this task to make sure that the ledger balances for cash accounts fit the cash balance.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66bbe-371">Sularahaaruande loomine (ainult Poola puhul).</span><span class="sxs-lookup"><span data-stu-id="66bbe-371">Cash report creation (for Poland only)</span></span></td>
<td><span data-ttu-id="66bbe-372">Looge aruanne <strong>Sularaha</strong>.</span><span class="sxs-lookup"><span data-stu-id="66bbe-372">Create a <strong>Cash</strong> report.</span></span> <span data-ttu-id="66bbe-373">Aruande <strong>Sularaha</strong> number luuakse suvandi <strong>Aruande number</strong> jaoks seadistatud numbriseeria põhjal.</span><span class="sxs-lookup"><span data-stu-id="66bbe-373">The <strong>Cash</strong> report number is generated based on the number sequence that is set up for <strong>Report number</strong>.</span></span> <span data-ttu-id="66bbe-374">Määrake ülesande dialoogiboksis väljal <strong>Tähtaeg</strong> viimane kuupäev, mille sularahakandeid tuleb aruandes <strong>Sularaha</strong> arvesse võtta.</span><span class="sxs-lookup"><span data-stu-id="66bbe-374">In the dialog box for the task, in the <strong>To date</strong>, specify the last date for which cash transactions should be counted for the <strong>Cash</strong> report.</span></span> <span data-ttu-id="66bbe-375">Määrake vahekaardi <strong>Kaasatavad kirjed</strong> funktsiooniga <strong>Filtreeri</strong> lisakriteeriumid sularahakannete valiku piiramiseks.</span><span class="sxs-lookup"><span data-stu-id="66bbe-375">Use the <strong>Filter</strong> function on the <strong>Records to include</strong> tab to specify additional criteria to limit the selection of cash transactions.</span></span> <span data-ttu-id="66bbe-376">Need kriteeriumid võivad sisaldada sularahakontode numbreid ja valuutakoode.</span><span class="sxs-lookup"><span data-stu-id="66bbe-376">These criteria can include cash account numbers and currency codes.</span></span> <span data-ttu-id="66bbe-377">Valige väljal <strong>Looja</strong> aruande koostamise eest vastutav kasutaja.</span><span class="sxs-lookup"><span data-stu-id="66bbe-377">In the <strong>Create by</strong> field, select the user who is responsible for report creation.</span></span> <span data-ttu-id="66bbe-378">Loodud aruande <strong>Sularaha</strong> vaatamiseks kasutage lehel <strong>Sularahakontod</strong> olevat nuppu <strong>Sularahaaruanded</strong>.</span><span class="sxs-lookup"><span data-stu-id="66bbe-378">To view the <strong>Cash</strong> report that is created, use the <strong>Cash reports</strong> button on the <strong>Cash accounts</strong> page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="66bbe-379">Kassa – valuutakursi korrigeerimine, FIFO ja LIFO (ainult Poola puhul)</span><span class="sxs-lookup"><span data-stu-id="66bbe-379">Cash - Exchange adjustment FIFO and LIFO (for Poland only)</span></span></td>
<td><span data-ttu-id="66bbe-380">Arvutage valuutakursi korrigeerimine Poola standardite alusel.</span><span class="sxs-lookup"><span data-stu-id="66bbe-380">Calculate the exchange adjustment per Polish standards.</span></span> <span data-ttu-id="66bbe-381">Määrake vahekaardi <strong>Kaasatavad kirjed</strong> funktsiooniga <strong>Filtreeri</strong> sularahakonto, mille kohta ülesanne kävitada.</span><span class="sxs-lookup"><span data-stu-id="66bbe-381">Use the <strong>Filter</strong> function on the <strong>Records to include</strong> tab to specify the cash account to run the task for.</span></span> <span data-ttu-id="66bbe-382">Märkige ruut <strong>Ümberarvutus</strong> valuutakursi korrigeerimise erinevuse ümberarvutamiseks kõigi avatud perioodide puhul.</span><span class="sxs-lookup"><span data-stu-id="66bbe-382">Select the <strong>Recalculation</strong> check box to do a full recalculation of the exchange adjustment difference for all open periods.</span></span> <span data-ttu-id="66bbe-383">Kaubavarude hinna määramise FIFO-meetodi (esimesena sisse, esimesena välja) ja kaubavarude hinna määramise LIFO-meetodi (viimasena sisse, esimesena välja) kasutamisel arvutatakse valuutakursi korrigeerimine järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="66bbe-383">Here is how the exchange adjustment is calculated when the first in, first out (FIFO) and last in, first out (LIFO) methods are used:</span></span>
<ul>
<li><span data-ttu-id="66bbe-384"><strong>FIFO-meetod</strong>– süsteem otsib varasema kandekuupäevaga (väiksema tellimuse numbriga) kulukannet ja tasakaalustab selle varasema kandekuupäevaga (väiksema tellimuse numbriga) sissetulekukandega.</span><span class="sxs-lookup"><span data-stu-id="66bbe-384"><strong>FIFO method</strong> – The system searches for an expenditure transaction that has an earlier transaction date (smaller order number) and settles it with a receipt transaction that has an earlier transaction date (smaller order number).</span></span></li>
<li><span data-ttu-id="66bbe-385"><strong>LIFO-meetod</strong>– süsteem otsib hilisema kandekuupäevaga (suurema tellimuse numbriga) kulukannet ja tasakaalustab selle hilisema kandekuupäevaga (suurema tellimuse numbriga) sissetulekukandega.</span><span class="sxs-lookup"><span data-stu-id="66bbe-385"><strong>LIFO method</strong> – The system searches for an expenditure transaction that has a later transaction date (larger order number) and settles it with a receipt transaction that has a later transaction date (larger order number).</span></span></li>
</ul>
<span data-ttu-id="66bbe-386">Tasakaalustatud summa kajastub lehe <strong>Sularahakanne</strong> väljal <strong>Tasakaalustatud valuuta</strong>.</span><span class="sxs-lookup"><span data-stu-id="66bbe-386">The settled amount is reflected in the <strong>Settled currency</strong> field on the <strong>Cash transaction</strong> page.</span></span> <span data-ttu-id="66bbe-387">Valuutakursi korrigeerimise erinevuse korral kajastub summa väljal <strong>Valuutakursi korrigeerimise summa</strong> ja tabelis <strong>Sularahakanne</strong> luuakse kanne dokumenditüübita <strong>Valuutakursi erinevus</strong>.</span><span class="sxs-lookup"><span data-stu-id="66bbe-387">If there is an exchange adjustment difference, the amount is reflected in the <strong>Exchange adjustment amount</strong> field, and a transaction of the <strong>Exchange rate difference</strong> document type is generated in the <strong>Cash transaction</strong> table.</span></span> <span data-ttu-id="66bbe-388">Kasumi/kahjumi kannete pearaamatukontod määratakse tabelis <strong>Valuuta</strong> (<strong>Valuutakursi finantskasum</strong> ja <strong>Valuutakursi finantskahjum</strong>).</span><span class="sxs-lookup"><span data-stu-id="66bbe-388">Ledger accounts for profit/loss transactions are set in the <strong>Currency</strong> table (<strong>Exchange rate financial profit</strong> and <strong>Exchange rate financial loss</strong>).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="66bbe-389">Välisvaluuta ümberarvutamine – kassa</span><span class="sxs-lookup"><span data-stu-id="66bbe-389">Foreign currency revaluation - Cash</span></span></td>
<td><span data-ttu-id="66bbe-390">Saate selle ülesande abil tagada aruandluskuupäeval piisava saldo vaikevaluutas, kui toimingud on sisestatud välisvaluutades.</span><span class="sxs-lookup"><span data-stu-id="66bbe-390">Use this task to have an adequate balance in the default currency on the reporting date when the operations are entered in foreign currencies.</span></span> <span data-ttu-id="66bbe-391">Määrake vahekaardi <strong>Kaasatavad kirjed</strong> funktsiooniga <strong>Filtreeri</strong> sularahakonto, mille kohta ülesanne kävitada.</span><span class="sxs-lookup"><span data-stu-id="66bbe-391">Use the <strong>Filter</strong> function on the <strong>Records to include</strong> tab to specify the cash account to run the task for.</span></span> <span data-ttu-id="66bbe-392">Määrake ülesande dialoogiboksis väljade <strong>Lähtevaluuta</strong> ja <strong>Sihtvaluuta</strong> abil kande valuutad.</span><span class="sxs-lookup"><span data-stu-id="66bbe-392">In the dialog box for the task, use the <strong>From currency</strong> and <strong>To Currency</strong> fields to specify transaction currencies.</span></span> <span data-ttu-id="66bbe-393">Süsteem võrdleb valitud kuupäeva valuutakursi abil teisendatud valuuta summat vaikevaluuta summaga.</span><span class="sxs-lookup"><span data-stu-id="66bbe-393">The system compares the amount in the currency that was converted by using exchange rate on the selected date with the amount in the default currency.</span></span> <span data-ttu-id="66bbe-394">Kahe summa vaheline erinevus (v.a eelmine valuutakursi korrigeerimine) on arvutatud valuutakursi korrigeerimine.</span><span class="sxs-lookup"><span data-stu-id="66bbe-394">The difference between the two amounts (excluding the previous exchange adjustment) is the calculated exchange adjustment.</span></span> <span data-ttu-id="66bbe-395">See ülesanne loob heakskiidetud sularahakande tüübiga <strong>Valuutakursi korrigeerimine</strong>.</span><span class="sxs-lookup"><span data-stu-id="66bbe-395">This task creates an approved cash transaction of the <strong>Exchange adjustment</strong> type.</span></span> <span data-ttu-id="66bbe-396">Pearaamatu kanne koostamisel kasutatakse sularaha pearaamatukontot ja tabelis <strong>Valuuta</strong> väljal <strong>Realiseerimata kasum</strong> või <strong>Realiseerimata kahjum</strong> määratud pearaamatukontot.</span><span class="sxs-lookup"><span data-stu-id="66bbe-396">The ledger transaction is formed by using the ledger account for cash and the ledger account that is specified in <strong>Unrealized profit</strong> or <strong>Unrealized loss</strong> in the <strong>Currency</strong> table.</span></span></td>
</tr>
</tbody>
</table>

## <a name="inquiries-and-reports"></a><span data-ttu-id="66bbe-397">Päringud ja aruanded</span><span class="sxs-lookup"><span data-stu-id="66bbe-397">Inquiries and reports</span></span>

| <span data-ttu-id="66bbe-398">Päringud või aruandlus</span><span class="sxs-lookup"><span data-stu-id="66bbe-398">Inquiry or report</span></span>                             | <span data-ttu-id="66bbe-399">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="66bbe-399">Description</span></span>                                                                                                                                                                                                                     |
|-----------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66bbe-400">Sularahakannete kuvamine</span><span class="sxs-lookup"><span data-stu-id="66bbe-400">Cash transactions view</span></span>                        | <span data-ttu-id="66bbe-401">Saatelehe töölehe rea puhul kasutage pearaamatu kannete, sularahasaldo ja muu teabe kuvamiseks toimingupaani nuppu **Päringud**.</span><span class="sxs-lookup"><span data-stu-id="66bbe-401">For a Slip journal line, use the **Inquiries** button on the Action Pane to view ledger transactions, the cash balance, and other information.</span></span>                                                                                  |
| <span data-ttu-id="66bbe-402">Sularahakanne</span><span class="sxs-lookup"><span data-stu-id="66bbe-402">Cash transaction</span></span>                              | <span data-ttu-id="66bbe-403">Sularahakannete kuvamiseks avage **Sularaha- ja pangahaldus** &gt; **Päringud ja aruanded** &gt; **Sularahakanded**.</span><span class="sxs-lookup"><span data-stu-id="66bbe-403">Go to **Cash and bank management** &gt; **Inquiries and reports** &gt; **Cash transactions** to view cash transactions.</span></span> <span data-ttu-id="66bbe-404">Määrake funktsiooniga **Filtreeri** lisakriteeriumid sularahakannete valiku piiramiseks.</span><span class="sxs-lookup"><span data-stu-id="66bbe-404">Use the **Filter** function to specify additional criteria to limit the selection of cash transactions.</span></span> |
| <span data-ttu-id="66bbe-405">Registreerimise tööleht (Eesti ja Venemaa puhul)</span><span class="sxs-lookup"><span data-stu-id="66bbe-405">Journal of registration (for Estonia, Russia)</span></span> | <span data-ttu-id="66bbe-406">Aruanne jaotises **Sularaha- ja pangahaldus** &gt; **Päringud ja aruanded** &gt; **Registreerimise tööleht** kajastab kõiki väljastatud kassa korvamis- ja väljaminekuordereid.</span><span class="sxs-lookup"><span data-stu-id="66bbe-406">The report at **Cash and bank management** &gt; **Inquiries and reports** &gt; **Journal of registration** reflects all cash reimbursement and cash disbursement slips that have been issued.</span></span>                                   |
| <span data-ttu-id="66bbe-407">Kassaraamat (Läti, Leedu ja Venemaa puhul)</span><span class="sxs-lookup"><span data-stu-id="66bbe-407">Cash book (for Latvia, Lithuania, Russia)</span></span>     | <span data-ttu-id="66bbe-408">Aruanne jaotises **Sularaha- ja pangahaldus** &gt; **Päringud ja aruanded** &gt; **Kassaraamatu aruanne** kajastab tegelikke sularahaliikumisi (sissetulekud ja kulud).</span><span class="sxs-lookup"><span data-stu-id="66bbe-408">The report at **Cash and bank management** &gt; **Inquiries and reports** &gt; **Cash book report** reflects actual cash fund movements (receipts and expenditures).</span></span>                                                            |





