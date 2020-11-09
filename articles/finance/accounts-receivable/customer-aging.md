---
title: Kliendi ajalise jaotuse aruanne
description: Kliendi ajalise jaotuse aruandes kuvatakse deebetsaldod, mis on sorditud kuupäevavahemiku või aegumisperioodi alusel.
author: JodiChristiansen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: jchrist
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f3a1bba4596c7b645c20a790a6cbe8725ab665d
ms.sourcegitcommit: e43aef72b7d65db1dcb014dfada5233ac051ba7c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/15/2020
ms.locfileid: "4013049"
---
# <a name="customer-aging-report"></a><span data-ttu-id="3b829-103">Kliendi ajalise jaotuse aruanne</span><span class="sxs-lookup"><span data-stu-id="3b829-103">Customer aging report</span></span> 

<span data-ttu-id="3b829-104">**Kliendi ajalise jaotuse** aruandes kuvatakse deebetsaldod, mis on sorditud kuupäevavahemiku või aegumisperioodi alusel.</span><span class="sxs-lookup"><span data-stu-id="3b829-104">The **Customer aging** report displays the balances that are due from customers, sorted by date interval, or aging period.</span></span>

<span data-ttu-id="3b829-105">Selle aruande loomisel kuvatakse järgmised vaikeparameetrid.</span><span class="sxs-lookup"><span data-stu-id="3b829-105">When you generate this report, the following default parameters are displayed.</span></span> <span data-ttu-id="3b829-106">Neid parameetreid saate kasutada aruandes kuvatud andmete filtreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="3b829-106">You can use these parameters to filter the data that will be displayed on the report.</span></span> <span data-ttu-id="3b829-107">Lisateavet leiate teemast [Sissenõuete seadistamine](set-up-collections.md).</span><span class="sxs-lookup"><span data-stu-id="3b829-107">For more information, see [Set up collections](set-up-collections.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="3b829-108">Väli</span><span class="sxs-lookup"><span data-stu-id="3b829-108">Field</span></span></p></th>
<th><p><span data-ttu-id="3b829-109">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="3b829-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b829-110"><strong>Arveldusklassifikatsioon</strong></span><span class="sxs-lookup"><span data-stu-id="3b829-110"><strong>Billing classification</strong></span></span></p></td>
<td><p><span data-ttu-id="3b829-111">Valige aruandesse lisamiseks vähemalt üks arveldusklassifikatsioon.</span><span class="sxs-lookup"><span data-stu-id="3b829-111">Select one or more billing classifications to include on the report.</span></span></p>
<div class="alert">

<span data-ttu-id="3b829-112">**Märkus.** See juhtelement on saadaval ainult juhul, kui on valitud konfiguratsioonivõti <STRONG>Avalik sektor</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="3b829-112">**Note:** This control is available only if the <STRONG>Public Sector</STRONG> configuration key is selected.</span></span></P>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b829-113"><strong>Ilma arveldusklassifikatsioonita kannete kaasamine</strong></span><span class="sxs-lookup"><span data-stu-id="3b829-113"><strong>Include transactions without a billing classification</strong></span></span></p></td>
<td><p><span data-ttu-id="3b829-114">Kui see märkeruut on märgitud, siis kuvatakse aruandes kõik kanded, millele pole määratud arveldusklassifikatsiooni.</span><span class="sxs-lookup"><span data-stu-id="3b829-114">If this check box is selected, all transactions that do not have a billing classification assigned to them will be displayed on the report.</span></span></p>
<div class="alert">

<span data-ttu-id="3b829-115">**Märkus.** See juhtelement on saadaval ainult juhul, kui on valitud konfiguratsioonivõti <STRONG>Avalik sektor</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="3b829-115">**Note:** This control is available only if the <STRONG>Public sector</STRONG> configuration key is selected.</span></span></P>

</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b829-116"><strong>Ajaline jaotus seisuga</strong></span><span class="sxs-lookup"><span data-stu-id="3b829-116"><strong>Aging as of</strong></span></span></p></td>
<td><p><span data-ttu-id="3b829-117">Sisestage praeguses ajalise jaotuse vahemikus kasutatud kuupäev.</span><span class="sxs-lookup"><span data-stu-id="3b829-117">Enter the date used on the current aging bucket.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b829-118"><strong>Saldo seisuga</strong></span><span class="sxs-lookup"><span data-stu-id="3b829-118"><strong>Balance as of</strong></span></span></p></td>
<td><p><span data-ttu-id="3b829-119">Sisestage kuupäev, et vaadata kliendi saldosid.</span><span class="sxs-lookup"><span data-stu-id="3b829-119">Enter the date to view the customer balances for.</span></span> <span data-ttu-id="3b829-120">Seda nimetatakse ka kannete piirkuupäevaks.</span><span class="sxs-lookup"><span data-stu-id="3b829-120">This is also known as a cutoff date for transactions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b829-121"><strong>Alguskuupäev</strong></span><span class="sxs-lookup"><span data-stu-id="3b829-121"><strong>Start date</strong></span></span></p></td>
<td><p><span data-ttu-id="3b829-122">Sisestage kuupäev, mis jääb esimese perioodiintervalli või aegumisperioodi piiridesse, et see aruandesse kaasata.</span><span class="sxs-lookup"><span data-stu-id="3b829-122">Enter a date that is in the first period interval or aging period to include on the report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b829-123"><strong>Kriteerium</strong></span><span class="sxs-lookup"><span data-stu-id="3b829-123"><strong>Criteria</strong></span></span></p></td>
<td><p><span data-ttu-id="3b829-124">Valige kuupäeva tüüp, millel aruanne põhineb.</span><span class="sxs-lookup"><span data-stu-id="3b829-124">Select the type of date to base the report on.</span></span></p>
<ul>
<li><p><span data-ttu-id="3b829-125"><strong>Kande kuupäev</strong> – kannete sisestuskuupäev.</span><span class="sxs-lookup"><span data-stu-id="3b829-125"><strong>Transaction date</strong> – The posting date of the transactions.</span></span> <span data-ttu-id="3b829-126">Näiteks võib see olla arve kuupäev, mis on tähtaja arvutamise aluseks.</span><span class="sxs-lookup"><span data-stu-id="3b829-126">For example, this might be an invoice date that is the basis for the calculation of the due date.</span></span></p></li>
<li><p><span data-ttu-id="3b829-127"><strong>Tähtaeg</strong> – kannete tähtaeg maksetingimuste järgi.</span><span class="sxs-lookup"><span data-stu-id="3b829-127"><strong>Due date</strong> – The due date of the transactions, based on the terms of payment.</span></span></p></li>
<li><p><span data-ttu-id="3b829-128"><strong>Dokumendi kuupäev</strong> – kasutaja määratud dokumendikuupäev, mille alusel arvutatakse tähtaeg.</span><span class="sxs-lookup"><span data-stu-id="3b829-128"><strong>Document date</strong> – A user-defined document date that is the basis for the calculation of the due date.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b829-129"><strong>Aegumisperioodi definitsioon</strong></span><span class="sxs-lookup"><span data-stu-id="3b829-129"><strong>Aging period definition</strong></span></span></p></td>
<td><p><span data-ttu-id="3b829-130">Valige aegumisperioodi definitsioon.</span><span class="sxs-lookup"><span data-stu-id="3b829-130">Select an aging period definition.</span></span> <span data-ttu-id="3b829-131">Välja <strong>Intervall</strong> ei kasutata, kui valite aegumisperioodi definitsiooni.</span><span class="sxs-lookup"><span data-stu-id="3b829-131">The <strong>Interval</strong> field is not used if you select an aging period definition.</span></span></p>
<p><span data-ttu-id="3b829-132">Prinditaval aruandel ei saa kasutada aegumisperioodi definitsioone, millel on rohkem kui kuus aegumisperioodi.</span><span class="sxs-lookup"><span data-stu-id="3b829-132">Aging period definitions that have more than six aging periods cannot be used on the printed report.</span></span></p>
<div class="alert">

<span data-ttu-id="3b829-133">**Märkus.** Aegumisperioode saate seadistada lehel <STRONG>Aegumisperioodi definitsioonid</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="3b829-133">**Note:** You can set up aging periods on the <STRONG>Aging period definitions</STRONG> page.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b829-134"><strong>Aegumisperioodi kirjelduse printimine</strong></span><span class="sxs-lookup"><span data-stu-id="3b829-134"><strong>Print aging period description</strong></span></span></p></td>
<td><p><span data-ttu-id="3b829-135">Valige <strong>Jah</strong> aegumisperioodide kirjelduste kaasamiseks aruandes iga aegumisperioodi veeru ülaosas.</span><span class="sxs-lookup"><span data-stu-id="3b829-135">Select <strong>Yes</strong> to include aging period descriptions at the top of each aging period column on the report.</span></span> <span data-ttu-id="3b829-136">Valige <strong>Ei</strong>, et printida aruanne ilma veerupäisteta.</span><span class="sxs-lookup"><span data-stu-id="3b829-136">Select <strong>No</strong> to print the report without column headers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b829-137"><strong>Intervall</strong></span><span class="sxs-lookup"><span data-stu-id="3b829-137"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="3b829-138">Määrake kasutatav periood, sisestades igas perioodis päeva- või kuuühikute arvu.</span><span class="sxs-lookup"><span data-stu-id="3b829-138">Define the period to use by entering the number of the day or month units in each period.</span></span> <span data-ttu-id="3b829-139">Näiteks nädalapõhise aegumisteabe vaatamiseks sisestage sellele väljale 7 ja valige väljal <strong>Päev/kuu</strong> suvand <strong>Päev</strong>.</span><span class="sxs-lookup"><span data-stu-id="3b829-139">For example, to view aging information by week, enter 7 in this field and select <strong>Day</strong> in the <strong>Day/Mth</strong> field.</span></span></p>
<div class="alert">

<span data-ttu-id="3b829-140">**Märkus.** Sellele väljale sisestatavat teavet kasutatakse üksnes juhul, kui te pole aegumisperioodi definitsiooni valinud.</span><span class="sxs-lookup"><span data-stu-id="3b829-140">**Note:** The information that you enter in this field is used only if you have not selected an aging period definition.</span></span> <span data-ttu-id="3b829-141">Vastasel juhul määratletakse printimissuund aegumisperioodi definitsioonis.</span><span class="sxs-lookup"><span data-stu-id="3b829-141">Otherwise, the printing direction is defined on the aging period definition.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b829-142"><strong>Päev/kuu</strong></span><span class="sxs-lookup"><span data-stu-id="3b829-142"><strong>Day/Mth</strong></span></span></p></td>
<td><p><span data-ttu-id="3b829-143">Valige ühik, kas <strong>Päev</strong> või <strong>Kuu</strong>, mida kasutatakse perioodi määratlemiseks väljal <strong>Intervall</strong>.</span><span class="sxs-lookup"><span data-stu-id="3b829-143">Select the unit, either <strong>Day</strong> or <strong>Month</strong>, that is used to define the period in the <strong>Interval</strong> field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b829-144"><strong>Printimissuund</strong></span><span class="sxs-lookup"><span data-stu-id="3b829-144"><strong>Printing direction</strong></span></span></p></td>
<td><p><span data-ttu-id="3b829-145">Valige, kas arvutada saldosid ja printida möödunud või tulevaste perioodide ajalise jaotuse aruanne.</span><span class="sxs-lookup"><span data-stu-id="3b829-145">Select whether to calculate balances and print the aging report for past or future periods.</span></span> <span data-ttu-id="3b829-146">Kuupäevi hinnatakse väljal <strong>Saldo seisuga</strong> valitud kuupäeva arvestades.</span><span class="sxs-lookup"><span data-stu-id="3b829-146">The dates are evaluated relative to the date that is selected in the <strong>Balance as on</strong> field.</span></span> <span data-ttu-id="3b829-147">Valige <strong>Tagasiulatuv</strong>, et näidata eelmiste perioodide teavet.</span><span class="sxs-lookup"><span data-stu-id="3b829-147">Select <strong>Backward</strong> to show information for past periods.</span></span> <span data-ttu-id="3b829-148">Valige <strong>Edasiulatuv</strong>, et näidata tulevaste perioodide teavet.</span><span class="sxs-lookup"><span data-stu-id="3b829-148">Select <strong>Forward</strong> to show information for future periods.</span></span></p>
<div class="alert"><span data-ttu-id="3b829-149">
  
<STRONG>Märkus.</STRONG> Sellele väljale sisestatavat teavet kasutatakse üksnes juhul, kui te pole aegumisperioodi definitsiooni valinud.</span><span class="sxs-lookup"><span data-stu-id="3b829-149">
  
<STRONG>Note:</STRONG> The information that you enter in this field is used only if you have not selected an aging period definition.</span></span></P>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b829-150"><strong>Üksikasjad</strong></span><span class="sxs-lookup"><span data-stu-id="3b829-150"><strong>Details</strong></span></span></p></td>
<td><p><span data-ttu-id="3b829-151">Valige, et loetleda kanded, mis on aruandel näidatud saldodesse kaasatud.</span><span class="sxs-lookup"><span data-stu-id="3b829-151">Select to list the transactions that are included in the balances that are shown on the report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b829-152"><strong>Kandevaluutas summade kaasamine</strong></span><span class="sxs-lookup"><span data-stu-id="3b829-152"><strong>Include amounts in transaction currency</strong></span></span></p></td>
<td><p><span data-ttu-id="3b829-153">Valige, et kaasata summad nii kandevaluutas kui ka arvestusvaluutas.</span><span class="sxs-lookup"><span data-stu-id="3b829-153">Select to include amounts in the transaction currency in addition to amounts in the accounting currency.</span></span> <span data-ttu-id="3b829-154">Kui see märkeruut ei ole märgitud, kuvatakse aruandes olevad summad ainult arvestusvaluutas.</span><span class="sxs-lookup"><span data-stu-id="3b829-154">If this check box is not selected, the amounts on the report are displayed only in the accounting currency.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b829-155"><strong>Negatiivne saldo</strong></span><span class="sxs-lookup"><span data-stu-id="3b829-155"><strong>Negative balance</strong></span></span></p></td>
<td><p><span data-ttu-id="3b829-156">Valige, et kaasata kliendikontod, millel on negatiivne saldo.</span><span class="sxs-lookup"><span data-stu-id="3b829-156">Select to include customer accounts that have negative balances.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b829-157"><strong>Nullsaldo kontode välistamine</strong></span><span class="sxs-lookup"><span data-stu-id="3b829-157"><strong>Exclude zero balance accounts</strong></span></span></p></td>
<td><p><span data-ttu-id="3b829-158">Valige, et välistada kliendikontod, mille saldo on null.</span><span class="sxs-lookup"><span data-stu-id="3b829-158">Select to exclude customer accounts that have a zero balance.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b829-159"><strong>Maksete paigutamine</strong></span><span class="sxs-lookup"><span data-stu-id="3b829-159"><strong>Payment positioning</strong></span></span></p></td>
<td><p><span data-ttu-id="3b829-160">Valige, et kuvada maksed, mida pole arveldatud.</span><span class="sxs-lookup"><span data-stu-id="3b829-160">Select to display payments that have not been settled.</span></span> <span data-ttu-id="3b829-161">Need kuvatakse aruande esimeses veerus.</span><span class="sxs-lookup"><span data-stu-id="3b829-161">These are displayed in the first column of the report.</span></span></p></td>
</tr>
</tbody>
</table>

