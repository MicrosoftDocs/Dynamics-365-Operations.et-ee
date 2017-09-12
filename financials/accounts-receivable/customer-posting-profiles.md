---
title: Kliendi sisestusreeglid
description: Kliendi sisestusreeglid kontrollivad kliendikannete sisestamist pearaamatusse.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustPosting
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: da750645612c2a0a7650edfd933d707618d9f9ce
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---

# <a name="customer-posting-profiles"></a><span data-ttu-id="097f3-103">Kliendi sisestusreeglid</span><span class="sxs-lookup"><span data-stu-id="097f3-103">Customer posting profiles</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="097f3-104">Kliendi sisestusreeglid kontrollivad kliendikannete sisestamist pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="097f3-104">Customer posting profiles control the posting of customer transactions to the general ledger.</span></span>

<a name="customer-posting-profiles"></a><span data-ttu-id="097f3-105">Kliendi sisestusreeglid</span><span class="sxs-lookup"><span data-stu-id="097f3-105">Customer posting profiles</span></span>
-------------------------

<span data-ttu-id="097f3-106">Kliendi sisestusreeglid võimaldavad määrata pearaamatukontosid ja dokumendisätteid kõigile klientidele, kliendigrupile või üksikule kliendile.</span><span class="sxs-lookup"><span data-stu-id="097f3-106">Customer posting profiles enable you to assign general ledger accounts and document settings to all customers, a group of customers or a single customer.</span></span> <span data-ttu-id="097f3-107">Neid sätteid kasutatakse müügitellimuste, vabas vormis arvete, sularahamaksete, märgukirjade ja viivisearvete loomisel.</span><span class="sxs-lookup"><span data-stu-id="097f3-107">These settings will be used when you create sales orders, free text invoices, cash payments, collection letters, and interest notes.</span></span> <span data-ttu-id="097f3-108">Mõne kande puhul saate valida sisestusreegli, mis erineb ja on olulisem sellel lehel kannete jaoks seadistatud sisestusreeglitest.</span><span class="sxs-lookup"><span data-stu-id="097f3-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions in this page.</span></span> 

<span data-ttu-id="097f3-109">Vaike-sisestusreeglid määratletakse kiirkaardil Pearaamat ja käibemaks lehel Müügireskontro parameetrid.</span><span class="sxs-lookup"><span data-stu-id="097f3-109">The default posting profile is defined in the Ledger and Sales Tax fasttab on the Accounts receivable parameters page.</span></span> <span data-ttu-id="097f3-110">Vaike-sisestusreeglid lisatakse siis automaatselt uute dokumentide päisesse, kus saate vahetada need vajaduse korral teistsuguste sisestusreeglite vastu.</span><span class="sxs-lookup"><span data-stu-id="097f3-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile if needed.</span></span>

<span data-ttu-id="097f3-111">Saate seostada sisestamisdefinitsioonid kande sisestamistüüpidega lehel Kande sisestamisdefinitsioonid.</span><span class="sxs-lookup"><span data-stu-id="097f3-111">You can also associate posting definitions with transaction posting types in the Transaction posting definitions page.</span></span> <span data-ttu-id="097f3-112">Sisestamisdefinitsioonid juhivad kliendikannete sisestamist sisestusreeglite asemel pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="097f3-112">Posting definitions control the posting of customer transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="097f3-113">Sisestusreeglite loomine</span><span class="sxs-lookup"><span data-stu-id="097f3-113">Creating a posting profile</span></span>
<span data-ttu-id="097f3-114">Määrake kannete sisestamisel kasutatavad pearaamatukontod, mis kasutavad valitud sisestusreegleid.</span><span class="sxs-lookup"><span data-stu-id="097f3-114">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="097f3-115">Valige konto kood ja kui võimalik, siis ka konto või grupi number valitud sisestusreegli jaoks.</span><span class="sxs-lookup"><span data-stu-id="097f3-115">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="097f3-116">Sisestusprotsessis leitakse iga kande jaoks sobiv sisestusreegel, otsides kõige sobivamat kontokoodi, kontonumbri või grupi ja numbri kombinatsiooni järgmise prioriteediga.</span><span class="sxs-lookup"><span data-stu-id="097f3-116">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority:</span></span>

| <span data-ttu-id="097f3-117">Välja **Konto kood** väärtus</span><span class="sxs-lookup"><span data-stu-id="097f3-117">**Account code** field value</span></span> | <span data-ttu-id="097f3-118">Välja **Konto/grupi number** väärtus</span><span class="sxs-lookup"><span data-stu-id="097f3-118">**Account/Group number** field value</span></span>            | <span data-ttu-id="097f3-119">Otsingu prioriteet</span><span class="sxs-lookup"><span data-stu-id="097f3-119">Search priority</span></span> |
|------------------------------|-------------------------------------------------|-----------------|
| <span data-ttu-id="097f3-120">**Tabel**</span><span class="sxs-lookup"><span data-stu-id="097f3-120">**Table**</span></span>                    | <span data-ttu-id="097f3-121">Spetsiaalne kliendi konto</span><span class="sxs-lookup"><span data-stu-id="097f3-121">Specific customer account</span></span>                       | <span data-ttu-id="097f3-122">1</span><span class="sxs-lookup"><span data-stu-id="097f3-122">1</span></span>               |
| <span data-ttu-id="097f3-123">**Grupp**</span><span class="sxs-lookup"><span data-stu-id="097f3-123">**Group**</span></span>                    | <span data-ttu-id="097f3-124">Kliendigrupp, mis on kliendile määratud</span><span class="sxs-lookup"><span data-stu-id="097f3-124">Customer group that is assigned to the customer</span></span> | <span data-ttu-id="097f3-125">2</span><span class="sxs-lookup"><span data-stu-id="097f3-125">2</span></span>               |
| <span data-ttu-id="097f3-126">**Kõik**</span><span class="sxs-lookup"><span data-stu-id="097f3-126">**All**</span></span>                      | <span data-ttu-id="097f3-127">Tühi</span><span class="sxs-lookup"><span data-stu-id="097f3-127">Blank</span></span>                                           | <span data-ttu-id="097f3-128">3</span><span class="sxs-lookup"><span data-stu-id="097f3-128">3</span></span>               |

<span data-ttu-id="097f3-129">Kui soovite, et kõigil kliendi kannetel oleksid samad sisestusreeglid, seadistage ainult üks sisestusreegel, valides väljal Konto kood väärtuse Kõik.</span><span class="sxs-lookup"><span data-stu-id="097f3-129">If you want all customer transactions to have the same posting profile, set up only one posting profile with All in the Account code field.</span></span> <span data-ttu-id="097f3-130">Määrake sisestusreeglite seadistamiseks järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="097f3-130">Specify the following values to set up your posting profile:</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="097f3-131">Väli</span><span class="sxs-lookup"><span data-stu-id="097f3-131">Field</span></span></th>
<th><span data-ttu-id="097f3-132">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="097f3-132">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="097f3-133"><strong>Sisestusreeglid</strong></span><span class="sxs-lookup"><span data-stu-id="097f3-133"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="097f3-134">Tippige sisestusreegli kood.</span><span class="sxs-lookup"><span data-stu-id="097f3-134">Enter a code for the posting profile.</span></span> <span data-ttu-id="097f3-135">Näiteks saate luua kaks sisestusreeglit, et saada üks kliendi saldode konto riigi valuutas ja teine kliendi saldode konto välisvaluutas.</span><span class="sxs-lookup"><span data-stu-id="097f3-135">For example, you could create two posting profiles to obtain one account for customer balances in the national currency and another for customer balances in a foreign currency.</span></span> <span data-ttu-id="097f3-136">Ühe konto nimeks võite panna Riiklik ja teise konto nimeks Välismaine.</span><span class="sxs-lookup"><span data-stu-id="097f3-136">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="097f3-137"><strong>Kirjeldus</strong></span><span class="sxs-lookup"><span data-stu-id="097f3-137"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="097f3-138">Sisestage sisestusreeglite kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="097f3-138">Enter a description of the posting profile.</span></span> <span data-ttu-id="097f3-139">Seda kasutatakse üksnes sisestusreeglite paremaks tuvastamiseks nende vaatamisel selle lehel.</span><span class="sxs-lookup"><span data-stu-id="097f3-139">This is only used to better identify the posting profile when you view it in this page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="097f3-140"><strong>Konto kood</strong></span><span class="sxs-lookup"><span data-stu-id="097f3-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="097f3-141">Määrake, kas sisestusreegleid rakendatakse üksikule kliendile, kliendigrupile või kõikidele klientidele.</span><span class="sxs-lookup"><span data-stu-id="097f3-141">Specify whether the posting profile applies to a single customer, a group of customers, or all customers:</span></span>
<ul>
<li><span data-ttu-id="097f3-142"><strong>Tabel</strong> – sisestusreeglid rakenduvad ühele kliendile.</span><span class="sxs-lookup"><span data-stu-id="097f3-142"><strong>Table</strong> – The posting profile applies to a single customer.</span></span> <span data-ttu-id="097f3-143">Valige kliendikonto väljal Konto/grupi number.</span><span class="sxs-lookup"><span data-stu-id="097f3-143">Select the customer account in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="097f3-144"><strong>Grupp</strong> – sisestusreeglid rakenduvad kliendigrupile.</span><span class="sxs-lookup"><span data-stu-id="097f3-144"><strong>Group</strong> – The posting profile applies to a customer group.</span></span> <span data-ttu-id="097f3-145">Valige kliendigrupp väljal Konto/grupi number.</span><span class="sxs-lookup"><span data-stu-id="097f3-145">Select the customer group in the Account/Group number field.</span></span></li>
<li><span data-ttu-id="097f3-146"><strong>Kõik</strong> – sisestusreeglid rakenduvad kõigile klientidele.</span><span class="sxs-lookup"><span data-stu-id="097f3-146"><strong>All</strong> – The posting profile applies to all customers.</span></span> <span data-ttu-id="097f3-147">Jätke väli Konto/grupi number tühjaks.</span><span class="sxs-lookup"><span data-stu-id="097f3-147">Leave the Account/Group number field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="097f3-148"><strong>Konto/grupi number</strong></span><span class="sxs-lookup"><span data-stu-id="097f3-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="097f3-149">Kui väljal Konto kood on valitud väärtus Tabel, valige sisestusreegliga seotud kliendi konto number.</span><span class="sxs-lookup"><span data-stu-id="097f3-149">If Table is selected in the Account code field, select the account number of the customer who is associated with the posting profile.</span></span> <span data-ttu-id="097f3-150">Valiku Grupp korral valige kliendigrupp.</span><span class="sxs-lookup"><span data-stu-id="097f3-150">If Group is selected, select the customer group.</span></span> <span data-ttu-id="097f3-151">Kui on valitud väärtus Kõik, jätke see väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="097f3-151">If All is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="097f3-152"><strong>Summakonto</strong></span><span class="sxs-lookup"><span data-stu-id="097f3-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="097f3-153">Valige selle pearaamatukonto number, mida kasutatakse antud sisestusreeglitega seotud klientide puhul kliendi summakontona.</span><span class="sxs-lookup"><span data-stu-id="097f3-153">Select the ledger account that will be used as the customer summary account for the customers who are associated with the posting profile.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="097f3-154"><strong>Tasakaalusta konto</strong></span><span class="sxs-lookup"><span data-stu-id="097f3-154"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="097f3-155">Valige likviidsuse planeerimisel kasutatud pearaamatu likviidsuskonto.</span><span class="sxs-lookup"><span data-stu-id="097f3-155">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="097f3-156">See väli kuvatakse ainult juhul, kui likviidsuse planeerimine on lubatud.</span><span class="sxs-lookup"><span data-stu-id="097f3-156">This field will only appear if cash flow forecasts are enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="097f3-157"><strong>Käibemaksu ettemaksed</strong></span><span class="sxs-lookup"><span data-stu-id="097f3-157"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="097f3-158">Valige ettemaksuna saadud maksete käibemaksu jaoks kasutatav konto.</span><span class="sxs-lookup"><span data-stu-id="097f3-158">Select the account for sales tax for payments that are received in advance.</span></span>
<div class="alert">
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="097f3-159"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Märkus</span><span class="sxs-lookup"><span data-stu-id="097f3-159"><img src="https://i-technet.sec.s-msft.com/areas/global/content/clear.gif" title="Note</span></span>" alt="Note" id="alert_note" class="cl_IC101471" /><span data-ttu-id="097f3-160"><strong>Märkus</strong></span><span class="sxs-lookup"><span data-stu-id="097f3-160"><strong>Note</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="097f3-161">Lehe Müügireskontro parameetrid abil saate määrata sisestusreeglid, mida kasutada, kui makse on märgitud ettemakseks.</span><span class="sxs-lookup"><span data-stu-id="097f3-161">Use the Accounts receivable parameters page to specify the posting profile to use when a payment is marked as a prepayment.</span></span></td>
</tr>
</tbody>
</table>
</div></td>
</tr>
<tr class="even">
<td><span data-ttu-id="097f3-162"><strong>Allahindluse konto kohustused</strong></span><span class="sxs-lookup"><span data-stu-id="097f3-162"><strong>Liabilities for discount account</strong></span></span></td>
<td><span data-ttu-id="097f3-163">Valige allahindluse passiva pearaamatukonto.</span><span class="sxs-lookup"><span data-stu-id="097f3-163">Select the ledger account for liabilities of discount.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="097f3-164"><strong>Märgukirja seeria</strong></span><span class="sxs-lookup"><span data-stu-id="097f3-164"><strong>Collection letter sequence</strong></span></span></td>
<td><span data-ttu-id="097f3-165">Valige märgukirjaseeria identifikaator, mida kasutatakse klientide puhul, kellele on määratud sisestusreeglid.</span><span class="sxs-lookup"><span data-stu-id="097f3-165">Select the identifier of the collection letter sequence to use for customers to whom the posting profile is assigned.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="097f3-166"><strong>Viivise kood</strong></span><span class="sxs-lookup"><span data-stu-id="097f3-166"><strong>Interest code</strong></span></span></td>
<td><span data-ttu-id="097f3-167">Valige intressi kood, mida kasutatakse intressi arvutamiseks klientide puhul, kellele on määratud sisestusreeglid.</span><span class="sxs-lookup"><span data-stu-id="097f3-167">Select the interest code to use for the calculation of interest for customers to whom the posting profile is assigned.</span></span></td>
</tr>
</tbody>
</table>

### 

### <a name="table-restrictions"></a><span data-ttu-id="097f3-168">**Tabelipiirangud**</span><span class="sxs-lookup"><span data-stu-id="097f3-168">**Table restrictions**</span></span>

<span data-ttu-id="097f3-169">Valitud sisestusreeglitega kanded määravad, kas kanded tasakaalustatakse automaatselt, kas arvutatakse intress ja väljastatakse märgukirjad.</span><span class="sxs-lookup"><span data-stu-id="097f3-169">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="097f3-170">Saate valida ka konto, mida kasutatakse, kui valitud sisestusreeglitega kanded on suletud.</span><span class="sxs-lookup"><span data-stu-id="097f3-170">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="097f3-171">Määrake sisestusreeglite seadistamiseks järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="097f3-171">Specify the following values to set up your posting profile:</span></span>

| <span data-ttu-id="097f3-172">Väli</span><span class="sxs-lookup"><span data-stu-id="097f3-172">Field</span></span>                 | <span data-ttu-id="097f3-173">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="097f3-173">Description</span></span>                                                                                                                                                                                                                                        |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="097f3-174">**Tasakaalustus**</span><span class="sxs-lookup"><span data-stu-id="097f3-174">**Settlement**</span></span>        | <span data-ttu-id="097f3-175">Tehke see valik nende sisestusreeglitega kannete automaatse tasakaalustamise lubamiseks.</span><span class="sxs-lookup"><span data-stu-id="097f3-175">Select this toggle to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="097f3-176">Kui see valik eemaldada, tuleb kanded käsitsi tasakaalustada, kasutades lehte Avatud kannete tasakaalustamine või Kliendimaksete sisestamine.</span><span class="sxs-lookup"><span data-stu-id="097f3-176">If this toggle is cleared, you must manually settle transactions by using the Settle open transactions page or the Enter customer payments page.</span></span> |
| <span data-ttu-id="097f3-177">**Huvi**</span><span class="sxs-lookup"><span data-stu-id="097f3-177">**Interest**</span></span>          | <span data-ttu-id="097f3-178">Tehke see valik, kui neid sisestusreegleid kasutavate kliendikontode puhul tuleks arvestada intressi.</span><span class="sxs-lookup"><span data-stu-id="097f3-178">Select this toggle if interest should be calculated on outstanding balances for customer accounts that use this profile.</span></span> <span data-ttu-id="097f3-179">Kui see valik on eemaldatud, siis nende klientide puhul intressi ei arvutata.</span><span class="sxs-lookup"><span data-stu-id="097f3-179">If this toggle is cleared, interest will not be calculated for these customers.</span></span>                                           |
| <span data-ttu-id="097f3-180">**Märgukiri**</span><span class="sxs-lookup"><span data-stu-id="097f3-180">**Collection letter**</span></span> | <span data-ttu-id="097f3-181">Tehke see valik, kui neid sisestusreegleid kasutavate kliendikontode puhul tuleks koostada märgukirjad.</span><span class="sxs-lookup"><span data-stu-id="097f3-181">Select this toggle if collection letters should be generated for customer accounts that use this profile.</span></span> <span data-ttu-id="097f3-182">Kui see valik on eemaldatud, siis nende klientide puhul märgukirju ei koostata.</span><span class="sxs-lookup"><span data-stu-id="097f3-182">If this toggle is cleared, collection letters will not be generated for these customers.</span></span>                                                 |
| <span data-ttu-id="097f3-183">**Sulge**</span><span class="sxs-lookup"><span data-stu-id="097f3-183">**Close**</span></span>             | <span data-ttu-id="097f3-184">Valige sisestusreeglid, millele üle minna, kui nende sisestusreeglitega kanded suletakse.</span><span class="sxs-lookup"><span data-stu-id="097f3-184">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="097f3-185">Kanne loetakse suletuks, kui see on täielikult tasakaalustatud.</span><span class="sxs-lookup"><span data-stu-id="097f3-185">A transaction is regarded as closed when it has been settled in full.</span></span>                                                                           |



<span data-ttu-id="097f3-186">Lisateabe saamiseks vt [Kliendimaksete ülevaade](../cash-bank-management/tasks/customer-payment-overview.md).</span><span class="sxs-lookup"><span data-stu-id="097f3-186">For more information, see [Customer payment overview](../cash-bank-management/tasks/customer-payment-overview.md).</span></span>


