---
title: Lisandunud kordustellimused
description: teenustellimuste puhul kogute tulud käsitsi perioodidesse, mis järgnevad kuupäevale, millal kande eest arve esitasite.
author: ShylaThompson
ms.date: 04/30/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMASubscriptionGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3d6f2f69b7093e5408b016f4a69792b28c70f57f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824674"
---
# <a name="accruing-subscriptions"></a><span data-ttu-id="96df1-103">Lisandunud kordustellimused</span><span class="sxs-lookup"><span data-stu-id="96df1-103">Accruing subscriptions</span></span> 

[!include [banner](../includes/banner.md)]


<span data-ttu-id="96df1-104">teenustellimuste puhul kogute tulud käsitsi perioodidesse, mis järgnevad kuupäevale, millal kande eest arve esitasite.</span><span class="sxs-lookup"><span data-stu-id="96df1-104">With service subscriptions, you manually accrue revenue in the periods following the date when you invoiced a fee transaction.</span></span>

<span data-ttu-id="96df1-105">Lisandumisperioodid luuakse arve perioodi kohta, mille kordustellimuse tasule määrate, ning lisandumisperioodid põhinevad tellimuse perioodikoodil.</span><span class="sxs-lookup"><span data-stu-id="96df1-105">Accrual periods are created for the invoice period that you set up for the subscription fee, and the accrual periods are based on the period code of the subscription.</span></span>

<span data-ttu-id="96df1-106">Saate viittulu koguda ja tühistada.</span><span class="sxs-lookup"><span data-stu-id="96df1-106">You can accrue and reverse accrued revenue.</span></span>

## <a name="reverse-accruals-of-credit-amounts"></a><span data-ttu-id="96df1-107">Kreeditsummade viitvõlad</span><span class="sxs-lookup"><span data-stu-id="96df1-107">Reverse accruals of credit amounts</span></span>

<span data-ttu-id="96df1-108">Kui krediteerite kordustellimuse tasu, mille eest on arve esitatud, siis saate tasu tühistamiseks kasutada kahte meetodit.</span><span class="sxs-lookup"><span data-stu-id="96df1-108">If you credit invoiced subscription amounts, you can use two methods to reverse the accrual amounts:</span></span>

  - <span data-ttu-id="96df1-109">Saate ükshaaval tagasi pöörata kõik viittulukanded enne, kui loote kandele kreeditarve ettepaneku.</span><span class="sxs-lookup"><span data-stu-id="96df1-109">You can reverse each accrued revenue transaction individually before you create the credit note proposal for the transaction.</span></span> <span data-ttu-id="96df1-110">See on käsitsimeetod.</span><span class="sxs-lookup"><span data-stu-id="96df1-110">This is the manual method.</span></span> <span data-ttu-id="96df1-111">(käsitsi)</span><span class="sxs-lookup"><span data-stu-id="96df1-111">(manual)</span></span>

  - <span data-ttu-id="96df1-112">Saate viittulu tühistada kuupäeval, millal kreeditarve sisestatakse, või juurdekasvu esialgse sisestamise kuupäeval.</span><span class="sxs-lookup"><span data-stu-id="96df1-112">You can have the accrued amounts reversed on the date where the credit note is posted or on the original posting date of the accrual.</span></span>

<span data-ttu-id="96df1-113">Lisateabe saamiseks vt teemat [Kordustellimuse parameetrid (vorm)](https://technet.microsoft.com/library/aa619615.aspx).</span><span class="sxs-lookup"><span data-stu-id="96df1-113">For more information, see [Subscription parameters (form)](https://technet.microsoft.com/library/aa619615.aspx).</span></span>

## <a name="setup-requirements"></a><span data-ttu-id="96df1-114">Nõuete seadistamine</span><span class="sxs-lookup"><span data-stu-id="96df1-114">Setup requirements</span></span>

<span data-ttu-id="96df1-115">Tulu lisamiseks veenduge, et järgmised andmenõuded on täidetud.</span><span class="sxs-lookup"><span data-stu-id="96df1-115">To accrue revenue, make sure that the following data requirements are met:</span></span>

## <a name="account-setup"></a><span data-ttu-id="96df1-116">Konto seadistus</span><span class="sxs-lookup"><span data-stu-id="96df1-116">Account setup</span></span>

<span data-ttu-id="96df1-117">Kontod **Lõpetamata toodang – kordustellimus** ja **Viittulu – kordustellimus** tuleb seadistada moodulis **Projekt**.</span><span class="sxs-lookup"><span data-stu-id="96df1-117">The **WIP - subscription** and the **Accrued revenue - subscription** accounts must be set up in the **Project** module.</span></span>

<span data-ttu-id="96df1-118">Kui sisestate viittulu, siis debiteeritakse viittulu kontolt **Lõpetamata toodang – kordustellimus** ja kontot **Viittulu – kordustellimus** krediteeritakse viittulu summa võrra.</span><span class="sxs-lookup"><span data-stu-id="96df1-118">When you post accrued revenue, the **WIP - subscription** account is debited with the accrual amount, and the **Accrued revenue - subscription** account is credited with the accrual amount.</span></span>

## <a name="set-up-accounts-for-accrual-of-subscription-revenue"></a><span data-ttu-id="96df1-119">Kontode seadistamine viittulu või kordustellimuse tulu jaoks</span><span class="sxs-lookup"><span data-stu-id="96df1-119">Set up accounts for accrual of subscription revenue</span></span>

1.  <span data-ttu-id="96df1-120">Klõpsake valikuid **Projektihaldus ja -arvestus** \> **Seadistus** \> **Sisestamine** \> **Pearaamatu sisestamise seadistus**.</span><span class="sxs-lookup"><span data-stu-id="96df1-120">Click **Project management and accounting** \> **Setup** \> **Posting** \> **Ledger posting setup**.</span></span>

2.  <span data-ttu-id="96df1-121">Kontode seadistamiseks klõpsake vahekaarti **Tulukontod** ja valige seejärel **Lõpetamata toodang – kordustellimus** või **Viittulu – kordustellimus**.</span><span class="sxs-lookup"><span data-stu-id="96df1-121">Click the **Revenue accounts** tab, and select **WIP - subscription** or **Accrued revenue - subscription** to set up the accounts.</span></span>

## <a name="subscription-group-setup"></a><span data-ttu-id="96df1-122">Kordustellimuste grupi seadistus</span><span class="sxs-lookup"><span data-stu-id="96df1-122">Subscription group setup</span></span>

<span data-ttu-id="96df1-123">Tulu lisamiseks kordustellimuste jaoks peab märkeruut **Tulu lisamine** olema märgitud.</span><span class="sxs-lookup"><span data-stu-id="96df1-123">To be able to accrue revenue for subscriptions, the **Accrue revenue** check box must be selected.</span></span> <span data-ttu-id="96df1-124">Leiate selle kordustellimusega seotud grupi vormilt **Kordustellimuste grupid**.</span><span class="sxs-lookup"><span data-stu-id="96df1-124">This is found on the **Subscription groups** form for the group that is attached to the subscription.</span></span> <span data-ttu-id="96df1-125">Klõpsake valikuid **Teenuste haldus** \> **Seadistus** \> **Teenuse kordustellimused** \> **Kordustellimuste grupid**.</span><span class="sxs-lookup"><span data-stu-id="96df1-125">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

## <a name="enable-revenue-accrual-on-a-subscription-group"></a><span data-ttu-id="96df1-126">Tulude lisamise võimaldamine kordustellimuste grupi kohta</span><span class="sxs-lookup"><span data-stu-id="96df1-126">Enable revenue accrual on a subscription group</span></span>

1.  <span data-ttu-id="96df1-127">Klõpsake valikuid **Teenuste haldus** \> **Seadistus** \> **Teenuse kordustellimused** \> **Kordustellimuste grupid**.</span><span class="sxs-lookup"><span data-stu-id="96df1-127">Click **Service management** \> **Setup** \> **Service subscriptions** \> **Subscription groups**.</span></span>

## <a name="periods"></a><span data-ttu-id="96df1-128">Perioodid</span><span class="sxs-lookup"><span data-stu-id="96df1-128">Periods</span></span>

<span data-ttu-id="96df1-129">Seadistada tuleb arveldusperioodi kood.</span><span class="sxs-lookup"><span data-stu-id="96df1-129">You must set up an invoicing period code.</span></span> <span data-ttu-id="96df1-130">Kui te ei soovi lisada tulu sama ajavahemiku jooksul, mida kasutate arve esitamise puhul, siis tuleb seadistada ka lisandumisperiood.</span><span class="sxs-lookup"><span data-stu-id="96df1-130">Unless you want to accrue revenue in the same time intervals as you use for invoicing, you must also set up an accrual period.</span></span>

<span data-ttu-id="96df1-131">Järgmine tabel annab ülevaate sellest, milliseid lisandumisperioode saate iga arveldusperioodi kohta seadistada.</span><span class="sxs-lookup"><span data-stu-id="96df1-131">The following table provides an overview of which accrual periods can be set up for each invoicing period:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="96df1-132">Arveldusperiood</span><span class="sxs-lookup"><span data-stu-id="96df1-132">Invoicing period</span></span></p></th>
<th><p><span data-ttu-id="96df1-133">Laekumisperiood</span><span class="sxs-lookup"><span data-stu-id="96df1-133">Accrual period</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="96df1-134"><strong>Aastad</strong></span><span class="sxs-lookup"><span data-stu-id="96df1-134"><strong>Years</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="96df1-135"><strong>Aastad</strong></span><span class="sxs-lookup"><span data-stu-id="96df1-135"><strong>Years</strong></span></span></p></li>
<li><p><span data-ttu-id="96df1-136"><strong>Kvartal</strong></span><span class="sxs-lookup"><span data-stu-id="96df1-136"><strong>Quarter</strong></span></span></p></li>
<li><p><span data-ttu-id="96df1-137"><strong>Kuu</strong></span><span class="sxs-lookup"><span data-stu-id="96df1-137"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="96df1-138"><strong>Päev</strong></span><span class="sxs-lookup"><span data-stu-id="96df1-138"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96df1-139"><strong>Kvartal</strong></span><span class="sxs-lookup"><span data-stu-id="96df1-139"><strong>Quarter</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="96df1-140"><strong>Kvartal</strong></span><span class="sxs-lookup"><span data-stu-id="96df1-140"><strong>Quarter</strong></span></span></p></li>
<li><p><span data-ttu-id="96df1-141"><strong>Kuu</strong></span><span class="sxs-lookup"><span data-stu-id="96df1-141"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="96df1-142"><strong>Päev</strong></span><span class="sxs-lookup"><span data-stu-id="96df1-142"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96df1-143"><strong>Kuu</strong></span><span class="sxs-lookup"><span data-stu-id="96df1-143"><strong>Month</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="96df1-144"><strong>Kuu</strong></span><span class="sxs-lookup"><span data-stu-id="96df1-144"><strong>Month</strong></span></span></p></li>
<li><p><span data-ttu-id="96df1-145"><strong>Päev</strong></span><span class="sxs-lookup"><span data-stu-id="96df1-145"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="96df1-146"><strong>Nädal</strong></span><span class="sxs-lookup"><span data-stu-id="96df1-146"><strong>Week</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="96df1-147"><strong>Päev</strong></span><span class="sxs-lookup"><span data-stu-id="96df1-147"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="96df1-148"><strong>Päev</strong></span><span class="sxs-lookup"><span data-stu-id="96df1-148"><strong>Day</strong></span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="96df1-149"><strong>Päev</strong></span><span class="sxs-lookup"><span data-stu-id="96df1-149"><strong>Day</strong></span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="96df1-150">Arveldusperioodi seadistamine on üldise kordustellimuse grupi seadistamise kohustuslik osa.</span><span class="sxs-lookup"><span data-stu-id="96df1-150">Setting up the invoicing period is a mandatory part of the overall subscription group setup.</span></span> <span data-ttu-id="96df1-151">Saate otsustada, kas soovite seadistada ka lisandumisperioodi kordustellimuse grupi jaoks.</span><span class="sxs-lookup"><span data-stu-id="96df1-151">You can decide whether to also set up an accrual period for the subscription group.</span></span> <span data-ttu-id="96df1-152">Kui seadistate kordustellimuste grupile lisandumisperioodi, siis soovitatakse seda perioodi väljal **Perioodi kood**.</span><span class="sxs-lookup"><span data-stu-id="96df1-152">If you set up an accrual period for the subscription group, this period is suggested in the **Period code** field.</span></span> <span data-ttu-id="96df1-153">See väli asub vormil **Kordustellimuse tulu lisamine** siis, kui lisate kordustellimuste tulu.</span><span class="sxs-lookup"><span data-stu-id="96df1-153">This field is found in the **Accrue subscription revenue** form, when you accrue subscription revenue.</span></span> <span data-ttu-id="96df1-154">Kuid laekumisperiood on kordustellimuste grupi puhul valikuline teave.</span><span class="sxs-lookup"><span data-stu-id="96df1-154">However, the accrual period is optional information about the subscription group.</span></span>


> [!NOTE]
> <P><span data-ttu-id="96df1-155">Kasutage järgmist teed, et avada vorm <STRONG>Kordustellimuse tulu lisamine</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="96df1-155">Use the following path to open the <STRONG>Accrue subscription revenue</STRONG> form.</span></span> <span data-ttu-id="96df1-156">Klõpsake valikuid <STRONG>Teenuste haldus</STRONG> &gt; <STRONG>Perioodiline</STRONG> &gt; <STRONG>Teenuse kordustellimused</STRONG> &gt; <STRONG>Kordustellimuse tulu lisamine</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="96df1-156">Click <STRONG>Service management</STRONG> &gt; <STRONG>Periodic</STRONG> &gt; <STRONG>Service subscriptions</STRONG> &gt; <STRONG>Accrue subscription revenue</STRONG>.</span></span></P>


## <a name="transactions"></a><span data-ttu-id="96df1-157">Kanded</span><span class="sxs-lookup"><span data-stu-id="96df1-157">Transactions</span></span>

<span data-ttu-id="96df1-158">Saate määrata pearaamatukannete arvu, mis luuakse viittulu sisestamisel.</span><span class="sxs-lookup"><span data-stu-id="96df1-158">You can control the number of ledger transactions that are created when you post accrued revenue.</span></span> <span data-ttu-id="96df1-159">Kordustellimuste puhul saate määrata, kas pearaamatukanded tuleks luua tervikule või iga rea kohta.</span><span class="sxs-lookup"><span data-stu-id="96df1-159">On subscriptions, define if the ledger transactions should be created as a total or per line.</span></span>

## <a name="specify-the-level-of-posting-details-to-display-for-accrued-transactions"></a><span data-ttu-id="96df1-160">Laekumiskannete kohta kuvatavate detailide sisestamise tasandi määramine</span><span class="sxs-lookup"><span data-stu-id="96df1-160">Specify the level of posting details to display for accrued transactions</span></span>

1.  <span data-ttu-id="96df1-161">Klõpsake valikuid **Projektihaldus ja raamatupidamine** \> **Seadistus** \> **Projektihalduse ja raamatupidamise parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="96df1-161">Click **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>

2.  <span data-ttu-id="96df1-162">Valige vahekaardi **Finants** väljal **Arve** suvand **Kokku** või **Rida**.</span><span class="sxs-lookup"><span data-stu-id="96df1-162">On the **Financial** tab, in the **Invoice** field, select **Total** or **Line**.</span></span>


## <a name="see-also"></a><span data-ttu-id="96df1-163">Vt ka</span><span class="sxs-lookup"><span data-stu-id="96df1-163">See also</span></span>

[<span data-ttu-id="96df1-164">Kordustellimuse tulu lisamine</span><span class="sxs-lookup"><span data-stu-id="96df1-164">Accrue subscription revenue</span></span>](accrue-subscription-revenue.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]