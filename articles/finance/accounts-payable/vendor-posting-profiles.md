---
title: Hankija sisestusreeglid
description: Hankija sisestusreeglid kontrollivad hankijakannete sisestamist pearaamatusse.
author: abruer
ms.date: 06/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: VendPosting
audience: Application User
ms.reviewer: roschlom
ms.custom: 24691
ms.assetid: 18def866-7655-4f0b-b299-eec83098d23a
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e4b38fd137e6479493da79d4b62d0111b502a632
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189489"
---
# <a name="vendor-posting-profiles"></a><span data-ttu-id="4aa0b-103">Hankija sisestusreeglid</span><span class="sxs-lookup"><span data-stu-id="4aa0b-103">Vendor posting profiles</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4aa0b-104">Hankija sisestusreeglid kontrollivad hankijakannete sisestamist pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-104">Vendor posting profiles control the posting of vendor transactions to the general ledger.</span></span>

## <a name="vendor-posting-profiles"></a><span data-ttu-id="4aa0b-105">Hankija sisestusreeglid</span><span class="sxs-lookup"><span data-stu-id="4aa0b-105">Vendor posting profiles</span></span>

<span data-ttu-id="4aa0b-106">Hankija sisestusreeglid võimaldavad määrata pearaamatukontosid ja dokumendisätteid kõigile hankijatele, hankijagrupile või üksikule hankijale.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-106">Vendor posting profiles enable you to assign general ledger accounts and document settings to all vendors, a group of vendors, or a single vendor.</span></span> <span data-ttu-id="4aa0b-107">Neid sätteid kasutatakse ostutellimuste, hankija arvete ja sularahamaksete loomisel.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-107">These settings will be used when you create purchase orders, vendor invoices, and cash payments.</span></span> <span data-ttu-id="4aa0b-108">Mõne kande puhul saate valida sisestusreegli, mis erineb ja on olulisem sellel lehel kannete jaoks seadistatud sisestusreeglitest.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-108">For some transactions, you can select a posting profile that differs from and takes precedence over the posting profiles that are set up for transactions on this page.</span></span> <span data-ttu-id="4aa0b-109">Vaike-sisestusreeglid määratletakse kiirkaardil **Pearaamat ja käibemaks** lehel **Ostureskontro parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-109">The default posting profile is defined on the **Ledger and Sales Tax** FastTab on the **Accounts payable parameters** page.</span></span> <span data-ttu-id="4aa0b-110">Vaike-sisestusreeglid lisatakse siis automaatselt uute dokumentide päisesse, kus saate need vajaduse korral teistsuguste sisestusreeglite vastu vahetada.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-110">The default posting profile is then included automatically on the header of new documents where you can change it to a different posting profile, if needed.</span></span>

<span data-ttu-id="4aa0b-111">Saate seostada sisestamisdefinitsioonid kande sisestamistüüpidega lehel **Kande sisestamisdefinitsioonid**.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-111">You can also associate posting definitions with transaction posting types on the **Transaction posting definitions** page.</span></span> <span data-ttu-id="4aa0b-112">Sisestamisdefinitsioonid juhivad hankija kannete sisestamist sisestusreeglite asemel pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-112">Posting definitions control the posting of vendor transactions to the general ledger instead of posting profiles.</span></span>

## <a name="creating-a-posting-profile"></a><span data-ttu-id="4aa0b-113">Sisestusreeglite loomine</span><span class="sxs-lookup"><span data-stu-id="4aa0b-113">Creating a posting profile</span></span>
### <a name="setup"></a><span data-ttu-id="4aa0b-114">**Häälestus**</span><span class="sxs-lookup"><span data-stu-id="4aa0b-114">**Setup**</span></span>

<span data-ttu-id="4aa0b-115">Määrake kannete sisestamisel kasutatavad pearaamatukontod, mis kasutavad valitud sisestusreegleid.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-115">Specify the ledger accounts that are used in the posting of transactions that use the selected posting profile.</span></span> <span data-ttu-id="4aa0b-116">Valige konto kood ja kui võimalik, siis ka konto või grupi number valitud sisestusreegli jaoks.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-116">Select an account code and, whenever possible, an account or group number for the selected posting profile.</span></span> <span data-ttu-id="4aa0b-117">Sisestusprotsessis leitakse iga kande jaoks sobiv sisestusreegel, otsides kõige sobivamat kontokoodi, kontonumbri või grupi ja numbri kombinatsiooni järgmise prioriteediga.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-117">In the posting process, the most appropriate posting profile for each transaction is located by searching for the most specific account code, account number, or group and number combination in the following priority.</span></span>

| <span data-ttu-id="4aa0b-118">Välja **Konto kood** väärtus</span><span class="sxs-lookup"><span data-stu-id="4aa0b-118">**Account code** field value</span></span> | <span data-ttu-id="4aa0b-119">Välja **Konto/grupi number** väärtus</span><span class="sxs-lookup"><span data-stu-id="4aa0b-119">**Account/Group number** field value</span></span>        | <span data-ttu-id="4aa0b-120">Otsingu prioriteet</span><span class="sxs-lookup"><span data-stu-id="4aa0b-120">Search priority</span></span> |
|------------------------------|---------------------------------------------|-----------------|
| <span data-ttu-id="4aa0b-121">**Tabel**</span><span class="sxs-lookup"><span data-stu-id="4aa0b-121">**Table**</span></span>                    | <span data-ttu-id="4aa0b-122">Konkreetse hankija konto</span><span class="sxs-lookup"><span data-stu-id="4aa0b-122">Specific vendor account</span></span>                     | <span data-ttu-id="4aa0b-123">1</span><span class="sxs-lookup"><span data-stu-id="4aa0b-123">1</span></span>               |
| <span data-ttu-id="4aa0b-124">**Grupeeri**</span><span class="sxs-lookup"><span data-stu-id="4aa0b-124">**Group**</span></span>                    | <span data-ttu-id="4aa0b-125">Hankijale määratud hankijagrupp</span><span class="sxs-lookup"><span data-stu-id="4aa0b-125">Vendor group that is assigned to the vendor</span></span> | <span data-ttu-id="4aa0b-126">2</span><span class="sxs-lookup"><span data-stu-id="4aa0b-126">2</span></span>               |
| <span data-ttu-id="4aa0b-127">**Kõik**</span><span class="sxs-lookup"><span data-stu-id="4aa0b-127">**All**</span></span>                      | <span data-ttu-id="4aa0b-128">Tühi</span><span class="sxs-lookup"><span data-stu-id="4aa0b-128">Blank</span></span>                                       | <span data-ttu-id="4aa0b-129">3</span><span class="sxs-lookup"><span data-stu-id="4aa0b-129">3</span></span>               |

<span data-ttu-id="4aa0b-130">Kui soovite, et kõigil hankija kannetel oleksid samad sisestusreeglid, seadistage ainult üks sisestusreegel, valides väljal **Konto kood** väärtuse **Kõik**.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-130">If you want all vendor transactions to have the same posting profile, set up only one posting profile with **All** in the **Account code** field.</span></span> <span data-ttu-id="4aa0b-131">Määrake sisestusreeglite seadistamiseks järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-131">Specify the following values to set up your posting profile.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="4aa0b-132">Väli</span><span class="sxs-lookup"><span data-stu-id="4aa0b-132">Field</span></span></th>
<th><span data-ttu-id="4aa0b-133">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="4aa0b-133">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4aa0b-134"><strong>Sisestusreeglid</strong></span><span class="sxs-lookup"><span data-stu-id="4aa0b-134"><strong>Posting profile</strong></span></span></td>
<td><span data-ttu-id="4aa0b-135">Tippige sisestusreegli kood.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-135">Enter a code for the posting profile.</span></span> <span data-ttu-id="4aa0b-136">Näiteks saate luua kaks sisestusreeglit, et saada üks hankijasaldode konto riigi valuutas ja teine hankijasaldode konto välisvaluutas.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-136">For example, you could create two posting profiles to obtain one account for vendor balances in the national currency and another for vendor balances in a foreign currency.</span></span> <span data-ttu-id="4aa0b-137">Ühe konto nimeks võite panna Riiklik ja teise konto nimeks Välismaine.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-137">You could call one account National and the other Foreign.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4aa0b-138"><strong>Kirjeldus</strong></span><span class="sxs-lookup"><span data-stu-id="4aa0b-138"><strong>Description</strong></span></span></td>
<td><span data-ttu-id="4aa0b-139">Sisestage sisestusreeglite kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-139">Enter a description of the posting profile.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4aa0b-140"><strong>Konto kood</strong></span><span class="sxs-lookup"><span data-stu-id="4aa0b-140"><strong>Account code</strong></span></span></td>
<td><span data-ttu-id="4aa0b-141">Määrake, kas sisestusreeglit rakendatakse kindlale hankijale, hankijagrupile või kõikidele hankijatele.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-141">Specify whether the posting profile applies to a specific vendor, a group of vendors, or all vendors:</span></span>
<ul>
<li><span data-ttu-id="4aa0b-142"><strong>Tabel</strong> – sisestusreeglid rakenduvad ühele hankijale.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-142"><strong>Table</strong> – The posting profile applies to a single vendor.</span></span> <span data-ttu-id="4aa0b-143">Valige hankija konto väljal <strong>Konto/grupi number</strong>.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-143">Select the vendor account in the <strong>Account/Group number</strong> field.</span></span></li>
<li><span data-ttu-id="4aa0b-144"><strong>Grupp</strong> – sisestusreeglid rakenduvad hankijagrupile.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-144"><strong>Group</strong> – The posting profile applies to a vendor group.</span></span> <span data-ttu-id="4aa0b-145">Valige hankijagrupp väljal <strong>Konto/grupi number</strong>.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-145">Select the vendor group in the <strong>Account/Group number</strong> field.</span></span></li>
<li><span data-ttu-id="4aa0b-146"><strong>Kõik</strong> – sisestusreeglid rakenduvad kõigile hankijatele.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-146"><strong>All</strong> – The posting profile applies to all vendors.</span></span> <span data-ttu-id="4aa0b-147">Jätke väli <strong>Konto/grupi number</strong> tühjaks.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-147">Leave the <strong>Account/Group number</strong> field blank.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4aa0b-148"><strong>Konto/grupi number</strong></span><span class="sxs-lookup"><span data-stu-id="4aa0b-148"><strong>Account/Group number</strong></span></span></td>
<td><span data-ttu-id="4aa0b-149">Kui väljal <strong>Konto kood</strong> on valitud väärtus <strong>Tabel</strong>, valige sisestusreegliga seotud hankija konto number.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-149">If <strong>Table</strong> is selected in the <strong>Account code</strong> field, select the account number of the vendor that is associated with the posting profile.</span></span> <span data-ttu-id="4aa0b-150">Kui on valitud väärtus <strong>Grupp</strong>, valige hankijagrupp.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-150">If <strong>Group</strong> is selected, select a vendor group.</span></span> <span data-ttu-id="4aa0b-151">Kui on valitud väärtus <strong>Kõik</strong>, jätke see väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-151">If <strong>All</strong> is selected, leave this field blank.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4aa0b-152"><strong>Summakonto</strong></span><span class="sxs-lookup"><span data-stu-id="4aa0b-152"><strong>Summary account</strong></span></span></td>
<td><span data-ttu-id="4aa0b-153">Valige selle pearaamatukonto number, mida kasutatakse antud sisestusreeglitega seotud hankijate puhul summakontona.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-153">Select the ledger account that will be used as the summary account for the vendors that the posting profile relates to.</span></span> <span data-ttu-id="4aa0b-154">Märgitakse parameeter <strong>Ära luba käsitsi sisestamist</strong>.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-154">The <strong>Do not allow manual entry</strong> parameter for this main account will be marked.</span></span> <span data-ttu-id="4aa0b-155">Kui eemaldate seejärel selle konto sisestusreeglitest, kinnitage seadistus <strong>Ära luba käsitsi sisestamist</strong> lehel <strong>Põhikontod</strong>.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-155">If you subsequently remove this account from the posting profile, validate the <strong>Do not allow manual entry</strong> setting on the <strong>Main accounts</strong> page.</span></span> 
<p><span data-ttu-id="4aa0b-156"><strong>Märkus</strong>Kui lehel <strong>Pearaamatu parameetrid</strong> on valitud nupp <strong>Kasuta sisestamisdefinitsioone</strong>, kasutatakse hankija arvete puhul summakonto asemel kande sisestamisdefinitsiooni.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-156"><strong>Note:</strong> If the <strong>Use posting definitions</strong> option is selected on the <strong>General ledger parameters</strong> page, the transaction posting definition for vendor invoices is used instead of the summary account.</span></span></p>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="4aa0b-157"><strong>Tasakaalusta konto</strong></span><span class="sxs-lookup"><span data-stu-id="4aa0b-157"><strong>Settle account</strong></span></span></td>
<td><span data-ttu-id="4aa0b-158">Valige likviidsuse planeerimisel kasutatud pearaamatu likviidsuskonto.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-158">Select the liquidity ledger account that is used for cash flow forecasts.</span></span> <span data-ttu-id="4aa0b-159">See väli on saadaval ainult siis, kui on lubatud likviidsuse planeerimine.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-159">This fields is only available when cash flow forecasting is enabled.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4aa0b-160"><strong>Käibemaksu ettemaksed</strong></span><span class="sxs-lookup"><span data-stu-id="4aa0b-160"><strong>Sales tax prepayments</strong></span></span></td>
<td><span data-ttu-id="4aa0b-161">Valige ettemaksuna saadud maksete käibemaksu jaoks kasutatav konto.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-161">Select the account for sales tax payments that are received in advance.</span></span>
<p><span data-ttu-id="4aa0b-162"><strong>Märkus.</strong>Sisestusreegel, mida kasutatakse, kui ettemakseks märgitud makse on valitud lehel <strong>Ostureskontro parameetrid</strong> ala <strong>Pearaamat ja käibemaks</strong> väljal <strong>Sisestusreeglid</strong> <strong>Ettemaksu töölehekandega</strong>.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-162"><strong>Note:</strong> The posting profile that is used when the payment is marked as a prepayment is selected in the <strong>Posting</strong> profile with <strong>Prepayment journal voucher</strong> field in the <strong>Ledger and sales tax</strong> area on the <strong>Accounts payable parameters</strong> page.</span></span></p>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="4aa0b-163"><strong>Saabumine</strong></span><span class="sxs-lookup"><span data-stu-id="4aa0b-163"><strong>Arrival</strong></span></span></td>
<td><span data-ttu-id="4aa0b-164">Valige pearaamatukonto, kuhu sisestatakse teave kinnitamata hankija arvete kohta.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-164">Select the ledger account that information about unapproved vendor invoices is posted to.</span></span> <span data-ttu-id="4aa0b-165">Teave sisestatakse arveregistri töölehele.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-165">The information is entered in the Invoice register journal.</span></span> <span data-ttu-id="4aa0b-166">Näiteks kasutaja sisestab kõige põhilisema teabe hankija arvete kohta, nii nagu need on vastu võetud arveregistrisse.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-166">For example, a user enters very basic information about vendor invoices when they are received in the invoice register.</span></span> <span data-ttu-id="4aa0b-167">Arveregistri sisestamisel sisestatakse kanded sellele väljale ja väljale <strong>Vastaskonto</strong> sisestatud kontole.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-167">When the invoice register is posted, the transactions are posted to the account that is entered here and in the <strong>Offset account</strong> field.</span></span> <span data-ttu-id="4aa0b-168">Kui arved kinnitatakse, kantakse võlg saabumiskontolt üle hankija summakontole.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-168">When the invoices are approved, the debt is transferred from the arrival account to the vendor summary account.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4aa0b-169"><strong>Vastaskonto</strong></span><span class="sxs-lookup"><span data-stu-id="4aa0b-169"><strong>Offset account</strong></span></span></td>
<td><span data-ttu-id="4aa0b-170">Valige pearaamatukonto, mida kasutatakse arveregistri kaudu uuendatavate kinnitamata hankijaarvete vastaskontona.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-170">Select the ledger account that is used for offsetting unapproved vendor invoices that are updated by using the invoice register.</span></span> <span data-ttu-id="4aa0b-171">Vastaskonto toimib saabumiskontodele sisestatud kannete vastaskontona.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-171">The offset account acts as the offset account for transactions that are posted to arrival accounts.</span></span> <span data-ttu-id="4aa0b-172">Konto sisaldab seetõttu veel kinnitamata hankija oste.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-172">Therefore, the account contains vendor purchases that have not yet been approved.</span></span></td>
</tr>
</tbody>
</table>


### <a name="table-restrictions"></a><span data-ttu-id="4aa0b-173">**Tabelipiirangud**</span><span class="sxs-lookup"><span data-stu-id="4aa0b-173">**Table restrictions**</span></span>

<span data-ttu-id="4aa0b-174">Valitud sisestusreeglitega kanded määravad, kas kanded tasakaalustatakse automaatselt, kas arvutatakse intress ja väljastatakse märgukirjad.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-174">For transactions that have the selected posting profile, specify whether transactions will be settled automatically, interest will be calculated, and collection letters will be issued.</span></span> <span data-ttu-id="4aa0b-175">Saate valida ka konto, mida kasutatakse, kui valitud sisestusreeglitega kanded on suletud.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-175">You can also select the account that is used when transactions that have the selected posting profile are closed.</span></span>

<span data-ttu-id="4aa0b-176">Määrake sisestusreeglite seadistamiseks järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-176">Specify the following values to set up your posting profile</span></span>

| <span data-ttu-id="4aa0b-177">Väli</span><span class="sxs-lookup"><span data-stu-id="4aa0b-177">Field</span></span>          | <span data-ttu-id="4aa0b-178">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="4aa0b-178">Description</span></span>                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4aa0b-179">**Tasakaalustus**</span><span class="sxs-lookup"><span data-stu-id="4aa0b-179">**Settlement**</span></span> | <span data-ttu-id="4aa0b-180">Tehke see valik nende sisestusreeglitega kannete automaatse tasakaalustamise lubamiseks.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-180">Select this option to enable automatic settlement of transactions that have this posting profile.</span></span> <span data-ttu-id="4aa0b-181">Kui see valik eemaldada, tuleb kanded käsitsi tasakaalustada, kasutades lehte **Avatud kannete tasakaalustamine**.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-181">If this option is cleared, you must manually settle transactions by using the **Settle open transactions** page.</span></span> |
| <span data-ttu-id="4aa0b-182">**Tühista**</span><span class="sxs-lookup"><span data-stu-id="4aa0b-182">**Cancel**</span></span>     | <span data-ttu-id="4aa0b-183">Tehke see valik, kui soovite, et saaksite nende sisestusreeglitega kandeid tühistada.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-183">Select this option if you want to be able to cancel transactions that have this posting profile.</span></span>                                                                                                               |
| <span data-ttu-id="4aa0b-184">**Sulge**</span><span class="sxs-lookup"><span data-stu-id="4aa0b-184">**Close**</span></span>      | <span data-ttu-id="4aa0b-185">Valige sisestusreeglid, millele üle minna, kui nende sisestusreeglitega kanded suletakse.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-185">Select a posting profile to change to when transactions that have this posting profile are closed.</span></span> <span data-ttu-id="4aa0b-186">Kanne loetakse suletuks, kui see on täielikult tasakaalustatud.</span><span class="sxs-lookup"><span data-stu-id="4aa0b-186">A transaction is regarded as closed when it has been settled in full.</span></span>                                       |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]