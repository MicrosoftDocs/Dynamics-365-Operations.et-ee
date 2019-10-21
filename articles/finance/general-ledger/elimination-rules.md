---
title: Eemaldamisreeglid
description: See teema annab teavet eemaldamisreeglite ja eemaldamistest teatamise erinevate võimaluste kohta.
author: aprilolson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerEliminationRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fdcfebad5329b8ac6f3507f2bc59f26cf70aae33
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2186666"
---
# <a name="elimination-rules"></a><span data-ttu-id="01322-103">Eemaldamisreeglid</span><span class="sxs-lookup"><span data-stu-id="01322-103">Elimination rules</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="01322-104">See teema annab teavet eemaldamisreeglite ja eemaldamistest teatamise erinevate võimaluste kohta.</span><span class="sxs-lookup"><span data-stu-id="01322-104">This topic provides information about elimination rules and the various options for reporting about eliminations.</span></span>

<span data-ttu-id="01322-105">Eemaldamiskanded on nõutavad juhul, kui emaettevõttest juriidilisel isikul on ärisuhted ühe või mitme tütarettevõttest juriidilise isikuga ning ta kasutab konsolideeritud finantsaruandlust.</span><span class="sxs-lookup"><span data-stu-id="01322-105">Elimination transactions are required when a parent legal entity does business with one or more subsidiary legal entities and uses consolidated financial reporting.</span></span> <span data-ttu-id="01322-106">Konsolideeritud finantsaruanded peavad sisaldama ainult konsolideeritud organisatsiooni ja teiste sellest organisatsioonist väljaspool asuvate üksuste vahelisi kandeid.</span><span class="sxs-lookup"><span data-stu-id="01322-106">Consolidated financial statements must include only transactions that occur between the consolidated organization and other entities outside that organizations.</span></span> <span data-ttu-id="01322-107">Seetõttu tuleb samasse organisatsiooni kuuluvate juriidiliste isikute vahelised kanded pearaamatust eemaldada, nii et neid finantsaruannetes ei kuvata.</span><span class="sxs-lookup"><span data-stu-id="01322-107">Therefore, transactions between legal entities that are part of the same organization must be removed, or eliminated, from the general ledger, so they don't appear on financial reports.</span></span> <span data-ttu-id="01322-108">Eemaldamistest saab teatada mitmesugusel moel.</span><span class="sxs-lookup"><span data-stu-id="01322-108">There are multiple ways to report about eliminations:</span></span>

-   <span data-ttu-id="01322-109">Eemaldamisreeglit saab luua ja töödelda konsolideerimis- või eemaldamisettevõttes.</span><span class="sxs-lookup"><span data-stu-id="01322-109">An elimination rule can be created and processed in a consolidation or elimination company.</span></span>
-   <span data-ttu-id="01322-110">Finantsaruandlust saab kasutada eemaldamiskontode ja dimensioonide kuvamiseks konkreetses reas või veerus.</span><span class="sxs-lookup"><span data-stu-id="01322-110">Financial reporting can be used to show the eliminations accounts and dimensions on a specific row or column.</span></span>
-   <span data-ttu-id="01322-111">Eemaldamiste jälgimiseks võib käsitsi kandekirjete sisestamiseks kasutada eraldi juriidilist isikut.</span><span class="sxs-lookup"><span data-stu-id="01322-111">A separate legal entity can be used to post manual transaction entries to track eliminations.</span></span>

<span data-ttu-id="01322-112">Selles teemas käsitletakse eemaldamisreegleid, mida töödeldakse eemaldamis- või konsolideerimisettevõttes.</span><span class="sxs-lookup"><span data-stu-id="01322-112">This topic focuses on elimination rules that are processed in a consolidation or elimination company.</span></span> <span data-ttu-id="01322-113">Saate seadistada eemaldamisreeglid, et luua eemaldamiskanded juriidilises isikus, mis on määratud sihtettevõttest juriidilise isikuna eemaldamiste jaoks.</span><span class="sxs-lookup"><span data-stu-id="01322-113">You can set up elimination rules to create elimination transactions in a legal entity that is specified as the destination legal entity for eliminations.</span></span> <span data-ttu-id="01322-114">Seda sihtettevõttest juriidilist isikut nimetatakse eemaldamise juriidiliseks isikuks.</span><span class="sxs-lookup"><span data-stu-id="01322-114">This destination legal entity is known as the elimination legal entity.</span></span> <span data-ttu-id="01322-115">Eemaldamistöölehti saab luua konsolideerimisprotsessis või eemaldamistöölehe soovituse abil.</span><span class="sxs-lookup"><span data-stu-id="01322-115">Elimination journals can be generated either during the consolidation process or by using an elimination journal proposal.</span></span> <span data-ttu-id="01322-116">Enne eemaldamisreeglite seadistamist tuleb tutvuda järgmiste terminitega.</span><span class="sxs-lookup"><span data-stu-id="01322-116">Before you set up elimination rules, you should become familiar with the following terms:</span></span>

-   <span data-ttu-id="01322-117">**Lähteettevõttest juriidiline isik** – juriidiline isik, kus sisestatakse eemaldatavad summad.</span><span class="sxs-lookup"><span data-stu-id="01322-117">**Source legal entity** – The legal entity where the amounts that are being eliminated were posted.</span></span>
-   <span data-ttu-id="01322-118">**Sihtettevõttest juriidiline isik** – juriidiline isik, kus sisestatakse eemaldamisreeglid.</span><span class="sxs-lookup"><span data-stu-id="01322-118">**Destination legal entity** – The legal entity where elimination rules are posted.</span></span>
-   <span data-ttu-id="01322-119">**Eemaldamisettevõttest juriidiline isik** – juriidiline isik, mis on määratud eemaldamiste sihtettevõttest juriidiliseks isikuks.</span><span class="sxs-lookup"><span data-stu-id="01322-119">**Elimination legal entity** – The legal entity that is specified as the destination legal entity for eliminations.</span></span>
-   <span data-ttu-id="01322-120">**Konsolideeritud juriidiline isik** – juriidiline isik, mis on loodud finantstulemustest juriidiliste isikute grupile aruandmiseks.</span><span class="sxs-lookup"><span data-stu-id="01322-120">**Consolidated legal entity** – The legal entity that is created to report financial results for a group of legal entities.</span></span> <span data-ttu-id="01322-121">Juriidiliste isikute finantsandmed konsolideeritakse sellesse juriidilisse isikusse ja seejärel luuakse kombineeritud andmete põhjal finantsaruanne.</span><span class="sxs-lookup"><span data-stu-id="01322-121">The financial data from the legal entities is consolidated into this legal entity, and then a financial report is created by using the combined data.</span></span>

<span data-ttu-id="01322-122">Järgmises tabelis on kirjeldatud kannete tüüpe, mis võivad olla eemaldatavad.</span><span class="sxs-lookup"><span data-stu-id="01322-122">The following table shows the types of transactions that might have to be eliminated.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="01322-123">Kande tüüp</span><span class="sxs-lookup"><span data-stu-id="01322-123">Transaction type</span></span></th>
<th><span data-ttu-id="01322-124">Näide</span><span class="sxs-lookup"><span data-stu-id="01322-124">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="01322-125">Müügitellimus kanne ja arve (tsentraliseeritud töötlemine)</span><span class="sxs-lookup"><span data-stu-id="01322-125">Sales order entry and invoicing (centralized processing)</span></span></td>
<td><span data-ttu-id="01322-126">Müüte toote kliendile oma organisatsiooni teise juriidilise isiku nimel.</span><span class="sxs-lookup"><span data-stu-id="01322-126">You sell a product to a customer on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01322-127">Müügitellimuse kanne (kontsernisisene) ja arve</span><span class="sxs-lookup"><span data-stu-id="01322-127">Sales order entry (intercompany/intracompany) and invoicing</span></span></td>
<td><span data-ttu-id="01322-128">Müüte tooteid oma organisatsiooni juriidiliste isikute vahel.</span><span class="sxs-lookup"><span data-stu-id="01322-128">You sell products between legal entities in your organization.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01322-129">Ostutellimused (tsentraliseeritud töötlemine)</span><span class="sxs-lookup"><span data-stu-id="01322-129">Purchase orders (centralized processing)</span></span></td>
<td><span data-ttu-id="01322-130">Ostate varusid, tarneid, teenuseid, põhivarasid ja muid tooteid hankijalt oma organisatsiooni teise juriidilise isiku nimel.</span><span class="sxs-lookup"><span data-stu-id="01322-130">You purchase inventory, supplies, services, fixed assets, and other products from a vendor on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01322-131">Laohaldus (kontsernisisene)</span><span class="sxs-lookup"><span data-stu-id="01322-131">Inventory management (intercompany/intracompany)</span></span></td>
<td><ul>
<li><span data-ttu-id="01322-132">Kannate oma organisatsiooni ühe juriidilise isiku varud üle teise juriidilise isiku põhivaradesse.</span><span class="sxs-lookup"><span data-stu-id="01322-132">You transfer one legal entity’s inventory to the fixed assets of another legal entity in your organization.</span></span></li>
<li><span data-ttu-id="01322-133">Kannate oma organisatsiooni ühe juriidilise isiku varud üle teise juriidilise isiku varudesse.</span><span class="sxs-lookup"><span data-stu-id="01322-133">You transfer one legal entity’s inventory to the inventory of another legal entity in your organization.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01322-134">Teel olevate varude jälgimine</span><span class="sxs-lookup"><span data-stu-id="01322-134">In-transit inventory tracking</span></span></td>
<td><span data-ttu-id="01322-135">Kannate kaupu üle samas juriidilises isikus, kuid erinevates geograafilistes paikades asuvate ladude vahel.</span><span class="sxs-lookup"><span data-stu-id="01322-135">You transfer items between warehouses in the same legal entity, but across different geographical sites.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01322-136">Ostureskontro tsentraliseeritud arvetöötlus</span><span class="sxs-lookup"><span data-stu-id="01322-136">Accounts payable centralized invoice processing</span></span></td>
<td><span data-ttu-id="01322-137">Kirjendate arve oma organisatsiooni teise juriidilise isiku nimel.</span><span class="sxs-lookup"><span data-stu-id="01322-137">You record an invoice on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01322-138">Ostureskontro tsentraliseeritud maksetöötlus</span><span class="sxs-lookup"><span data-stu-id="01322-138">Accounts payable centralized payment processing</span></span></td>
<td><span data-ttu-id="01322-139">Tasute arve oma organisatsiooni teise juriidilise isiku nimel.</span><span class="sxs-lookup"><span data-stu-id="01322-139">You pay an invoice on behalf of another legal entity in your organization.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01322-140">Kassahaldus ja kassa (tsentraliseeritud töötlemine)</span><span class="sxs-lookup"><span data-stu-id="01322-140">Cash management and treasury (centralized processing)</span></span></td>
<td><ul>
<li><span data-ttu-id="01322-141">Saate töödelda maksumakseid, maksu tagasimakseid, viivisetasusid, laene, ettemakse, makstud dividende ja ettemakstud autoritasusid või komisjonitasusid.</span><span class="sxs-lookup"><span data-stu-id="01322-141">You process tax payments, tax refunds, interest charges, loans, advances, dividend payments, and prepaid royalties or commissions.</span></span></li>
<li><span data-ttu-id="01322-142">Tasute kulu oma organisatsiooni teise juriidilise isiku nimel.</span><span class="sxs-lookup"><span data-stu-id="01322-142">You pay an expense on behalf of another legal entity in your organization.</span></span> <span data-ttu-id="01322-143">Arve on sisestatud sihtettevõttest juriidilise isiku raamatutesse ja te peate tegema ettevõtetevahelise tasakaalustuse.</span><span class="sxs-lookup"><span data-stu-id="01322-143">The invoice is entered in the destination legal entity’s books, and you must cross-settle between legal entities.</span></span> <span data-ttu-id="01322-144">Näiteks tasub üks juriidiline isik teise juriidilise isiku töötaja kuluaruande.</span><span class="sxs-lookup"><span data-stu-id="01322-144">For example, one legal entity pays the expense report of an employee in another legal entity.</span></span> <span data-ttu-id="01322-145">Sellisel juhul on töötaja kuluaruandes kulud, mis on seotud teise juriidilise isikuga.</span><span class="sxs-lookup"><span data-stu-id="01322-145">In this case, the employee’s expense report has expenses that are related to another legal entity.</span></span></li>
<li><span data-ttu-id="01322-146">Kannate sularaha oma organisatsiooni ühest juriidilisest isikust teise.</span><span class="sxs-lookup"><span data-stu-id="01322-146">You transfer cash from one legal entity to another in your organization.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01322-147">Müügireskontro (tsentraliseeritud töötlemine)</span><span class="sxs-lookup"><span data-stu-id="01322-147">Accounts receivable (centralized processing)</span></span></td>
<td><span data-ttu-id="01322-148">Võtate sularaha vastu teise juriidilise isiku kliendiarve jaoks ja deponeerite tšeki selle juriidilise isiku pangakontole.</span><span class="sxs-lookup"><span data-stu-id="01322-148">You receive cash for another legal entity’s customer invoice, and you deposit the check into that legal entity’s bank account.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01322-149">Palk (tsentraliseeritud töötlemine, kontsernisisene)</span><span class="sxs-lookup"><span data-stu-id="01322-149">Payroll (centralized processing, intercompany/intracompany)</span></span></td>
<td><ul>
<li><span data-ttu-id="01322-150">Maksate teise juriidilise isiku palgad.</span><span class="sxs-lookup"><span data-stu-id="01322-150">You pay another legal entity’s payroll.</span></span> <span data-ttu-id="01322-151">Näiteks võib juriidiline isik maksta oma töötajale palka, kuid arvestab maha tasu töö eest, mille töötaja tegi selle palgaarvestusperioodi jooksul teisele juriidilisele isikule.</span><span class="sxs-lookup"><span data-stu-id="01322-151">For example, a legal entity pays its own payroll for its employees but charges back work that an employee did for another legal entity during that pay run.</span></span> <span data-ttu-id="01322-152">Või kui töötaja töötas pool aega juriidilisele isikule A ja pool aega juriidilisele isikule B ning soodustused katavad kogu tasu.</span><span class="sxs-lookup"><span data-stu-id="01322-152">Or, an employee worked half-time for legal entity A and half-time for legal entity B, and the benefits are across all pay.</span></span> <span data-ttu-id="01322-153">Neil juhtudel sisaldab töötaja palk tasu mõlemalt juriidiliselt isikult.</span><span class="sxs-lookup"><span data-stu-id="01322-153">In these cases, the employee’s pay includes pay from both legal entities.</span></span> <span data-ttu-id="01322-154">Sisestatakse mitte ainult töötasud, vaid ka maksud, soodustused, mahaarvamised ja viitvõlad töötasudele.</span><span class="sxs-lookup"><span data-stu-id="01322-154">Not only are the salaries posted, but taxes, benefits, deductions, and accruals for salaries are also posted.</span></span></li>
<li><span data-ttu-id="01322-155">Kannate töö üle ühest osakonnast või üksusest teise.</span><span class="sxs-lookup"><span data-stu-id="01322-155">You transfer labor from one department or division to another.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="01322-156">Põhivarad (kontsernisisene)</span><span class="sxs-lookup"><span data-stu-id="01322-156">Fixed assets (intercompany/intracompany)</span></span></td>
<td><span data-ttu-id="01322-157">Kannate põhivarad üle teise juriidilise isiku põhivaradesse või varudesse.</span><span class="sxs-lookup"><span data-stu-id="01322-157">You transfer fixed assets to another legal entity’s fixed assets or inventory.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="01322-158">Eraldamised (kontsernisisene)</span><span class="sxs-lookup"><span data-stu-id="01322-158">Allocations (intercompany/intracompany)</span></span></td>
<td><span data-ttu-id="01322-159">Töötlete ettevõtte eraldusi.</span><span class="sxs-lookup"><span data-stu-id="01322-159">You process corporate allocations.</span></span> <span data-ttu-id="01322-160">Eraldused on tegevused kõigi eraldatud kontodega, olenemata moodulist, kust see pärit on.</span><span class="sxs-lookup"><span data-stu-id="01322-160">Allocations are activities to any account that is allocated, regardless of the originating module.</span></span></td>
</tr>
</tbody>
</table>

## <a name="example"></a><span data-ttu-id="01322-161">Näide</span><span class="sxs-lookup"><span data-stu-id="01322-161">Example</span></span>
<span data-ttu-id="01322-162">Teie juriidiline isik (A) müüb vidinad teisele teie ettevõtte juriidilisele isikule (B). Järgmises näites kirjeldatakse, kuidas kahe juriidilise isiku vahelised kannete eemaldamine võib vajalikuks osutuda.</span><span class="sxs-lookup"><span data-stu-id="01322-162">Your legal entity, legal entity A, sells widgets to another legal entity in your organization, legal entity B. The following example shows how transactions that occur between the two legal entities might have to be eliminated:</span></span>

-   <span data-ttu-id="01322-163">Juriidiline ettevõte A müüb 10,00 eurot maksva vidina juriidilisele isikule B hinnaga 10,00 eurot.</span><span class="sxs-lookup"><span data-stu-id="01322-163">Legal entity A sells a widget that costs 10.00 to legal entity B for 10.00.</span></span>
-   <span data-ttu-id="01322-164">Juriidiline isik A müüb 10,00 eurot maksva vidina juriidilisele isikule B hinnaga 10,00 eurot pluss 2,00 eurot tegelikku postikulu.</span><span class="sxs-lookup"><span data-stu-id="01322-164">Legal entity A sells a widget that costs 10.00 to legal entity B for 10.00, plus 2.00 in actual shipping costs.</span></span>
-   <span data-ttu-id="01322-165">Juriidiline isik A müüb 10,00 eurot maksva vidina juriidilisele isikule B hinnaga 15,00 eurot ja saab selle müügi pealt brutotulu.</span><span class="sxs-lookup"><span data-stu-id="01322-165">Legal entity A sells a widget that costs 10.00 to legal entity B for 15.00 and recognizes a margin on the sale.</span></span>
-   <span data-ttu-id="01322-166">Juriidiline isik A müüb 10.00 eurot maksva vidina juriidilisele isikule B hinnaga 15.00 eurot ja saab selle müügi pealt poole brutotulust.</span><span class="sxs-lookup"><span data-stu-id="01322-166">Legal entity A sells a widget that costs 10.00 to legal entity B for 15.00 and recognizes half the margin on the sale.</span></span> <span data-ttu-id="01322-167">Juriidiline isik B saab teise poole brutotulust.</span><span class="sxs-lookup"><span data-stu-id="01322-167">Legal entity B recognizes the other half of the margin on the sale.</span></span> <span data-ttu-id="01322-168">Seetõttu on tulu jagatud.</span><span class="sxs-lookup"><span data-stu-id="01322-168">Therefore, the revenue is split.</span></span> <span data-ttu-id="01322-169">Jagatud tulu pakub soodustust välisest organisatsioonist tellimise asemel oma organisatsiooni teisest ettevõttest tellimise korral.</span><span class="sxs-lookup"><span data-stu-id="01322-169">Split revenue provides an incentive to order from another legal entity in the organization instead of an external organization.</span></span>

<span data-ttu-id="01322-170">Kõik need kanded loovad kontsernisisesed kanded, mis sisestatakse algus- ja lõpptähtaja kontodele.</span><span class="sxs-lookup"><span data-stu-id="01322-170">All these transactions create intercompany transactions that are posted to due-to and due-from accounts.</span></span> <span data-ttu-id="01322-171">Peale selle võivad need kanded hõlmata hinnalisandiga ja hinnavähendusega summasid, kui kontsernisisene müügisumma ja müüdud kaupade maksumus ei ole võrdsed.</span><span class="sxs-lookup"><span data-stu-id="01322-171">In addition, these transactions might include markup and markdown amounts when the amount of the intercompany sale doesn't equal the cost of the goods that were sold.</span></span>

## <a name="set-up-elimination-rules"></a><span data-ttu-id="01322-172">Eemaldamisreeglite seadistamine</span><span class="sxs-lookup"><span data-stu-id="01322-172">Set up elimination rules</span></span>
<span data-ttu-id="01322-173">Eemaldamisreeglite seadistamisel soovitame luua spetsiaalselt eemaldamiseks mõeldud finantsdimensiooni.</span><span class="sxs-lookup"><span data-stu-id="01322-173">When setting up elimination rules, we recommend that you create a financial dimension specifically for elimination purposes.</span></span> <span data-ttu-id="01322-174">Enamik kliente annab sellele nimeks Kaubanduspartner või muud sarnast.</span><span class="sxs-lookup"><span data-stu-id="01322-174">Most customers name it Trading Partner or something similar.</span></span> <span data-ttu-id="01322-175">Kui te ei soovi finantsdimensiooni kasutada, siis peavad teil kindlasti olema ainult ettevõtete vahelisteks kanneteks mõeldud põhikontod.</span><span class="sxs-lookup"><span data-stu-id="01322-175">If you decide not to use a financial dimension, then be sure to have main accounts that are specific for intercompany transactions only.</span></span> 

<span data-ttu-id="01322-176">Eemaldamised saate seadistada mooduli Konsolideerimised alal Seadistus.</span><span class="sxs-lookup"><span data-stu-id="01322-176">The setup for eliminations is found in the Setup area of the Consolidations module.</span></span> <span data-ttu-id="01322-177">Kui olete reegli kohta kirjelduse sisestanud, peate valima ettevõtte, millesse eemaldamisreegel sisestab.</span><span class="sxs-lookup"><span data-stu-id="01322-177">After you enter a description for the rule, you must pick the company that the elimination journal will post to.</span></span> <span data-ttu-id="01322-178">See peab olema ettevõte, mille puhul on juriidilise isiku seadistuses valitud suvand **Kasuta finantsiliseks eemaldamisprotsessiks**.</span><span class="sxs-lookup"><span data-stu-id="01322-178">This should be a company that has **Use for financial elimination process** selected in the Legal entity setup.</span></span> 

<span data-ttu-id="01322-179">Saate määrata eemaldamisreegli jõustumiskuupäeva ja vajadusel ka aegumiskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="01322-179">You can set a date on which the elimination rule becomes effective and when it is expired, if needed.</span></span> <span data-ttu-id="01322-180">Kui soovite, et see oleks eemaldamispakkumise protsessis saadaval, valige suvandi **Aktiivne** sätteks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="01322-180">You must set **Active** to **Yes** if you want it to be available in the elimination proposal process.</span></span> <span data-ttu-id="01322-181">Valige selle töölehe nimi, mille tüüp on **Eemaldamine**.</span><span class="sxs-lookup"><span data-stu-id="01322-181">Select a journal name that has a type of **Elimination**.</span></span>

<span data-ttu-id="01322-182">Kui olete põhiparameetrid määratlenud, saate määratleda ka tegelikud töötlusreeglid, klõpsates valikut **Read**.</span><span class="sxs-lookup"><span data-stu-id="01322-182">After you have defined the basics, you can define the actual processing rules by clicking **Lines**.</span></span> <span data-ttu-id="01322-183">Eemaldamiseks on kaks võimalust: netomuutuse summa eemaldamine või fikseeritud summa määratlemine.</span><span class="sxs-lookup"><span data-stu-id="01322-183">There are two options for eliminations, eliminating the net change amount or defining a fixed amount.</span></span> 

<span data-ttu-id="01322-184">Valige lähtekonto.</span><span class="sxs-lookup"><span data-stu-id="01322-184">Select your source account.</span></span> <span data-ttu-id="01322-185">Saate kasutada metamärgina tärni (\*).</span><span class="sxs-lookup"><span data-stu-id="01322-185">You can use an asterisk (\*) as a wild card.</span></span> <span data-ttu-id="01322-186">Näiteks väärtuse 1\* korral valitakse eralduse andmeallikana kõik kontod, mis algavad numbriga 1.</span><span class="sxs-lookup"><span data-stu-id="01322-186">For example, 1\* would select all accounts that start with a 1 as a source of data for the allocation.</span></span> 

<span data-ttu-id="01322-187">Kui olete lähtekontod valinud, määrab valik **Konto täpsustus** kasutatava konto sihtettevõttes.</span><span class="sxs-lookup"><span data-stu-id="01322-187">After you have selected your source accounts, the **Account specification** determines the account from the destination company that is used.</span></span> <span data-ttu-id="01322-188">Valige suvand **Allikas**, kui soovite kasutada sama põhikontot, mis on määratletud jaotises **Lähtekonto**.</span><span class="sxs-lookup"><span data-stu-id="01322-188">Select **Source** if you want to use the same main account defined in the **Source** account.</span></span> <span data-ttu-id="01322-189">Kui valite suvandi **Kasutaja määratletud**, peate määrama sihtkonto.</span><span class="sxs-lookup"><span data-stu-id="01322-189">If you select **User defined**, then you must specify a destination account.</span></span> 

<span data-ttu-id="01322-190">Dimensiooni täpsustus toimib samal moel.</span><span class="sxs-lookup"><span data-stu-id="01322-190">The dimension specification acts in the same way.</span></span> <span data-ttu-id="01322-191">Kui valite suvandi **Allikas**, kasutab see sihtettevõttes lähteettevõttega samu dimensioone.</span><span class="sxs-lookup"><span data-stu-id="01322-191">If you select **Source**, it will use the same dimensions in the destination company as the source company.</span></span> <span data-ttu-id="01322-192">Kui valite suvandi **Kasutaja määratletud**, peate määrama sihtettevõtes dimensioonid, klõpsates menüüelementi **Sihtdimensioonid**.</span><span class="sxs-lookup"><span data-stu-id="01322-192">If you select **User defined**, you will need to specify the dimensions in the destination company by clicking the **Destination dimensions** menu item.</span></span> 

<span data-ttu-id="01322-193">Valige lähtedimensioonid ja finantsdimensioonid ning väärtused, mida kasutatakse eemaldamisallikana.</span><span class="sxs-lookup"><span data-stu-id="01322-193">Select source dimensions and the financial dimensions and values that are used as a source of the elimination.</span></span>

## <a name="process-elimination-transactions"></a><span data-ttu-id="01322-194">Eemaldamiskannete töötlemine</span><span class="sxs-lookup"><span data-stu-id="01322-194">Process elimination transactions</span></span>
<span data-ttu-id="01322-195">Eemaldamiskannete töötlemiseks on kaks võimalust: ainult võrgu kaudu konsolideerimise ajal või luues eemaldamise tööraamatu ja käitades eemaldamispakkumise protsessi.</span><span class="sxs-lookup"><span data-stu-id="01322-195">There are two ways to process elimination transactions, during the consolidate online process or by creating an elimination journal and running the elimination proposal process.</span></span> <span data-ttu-id="01322-196">See jaotis keskendub töölehe loomisele ja eemaldamisprotsessi käitamisele.</span><span class="sxs-lookup"><span data-stu-id="01322-196">This section focuses on creating the journal and running the elimination process.</span></span> 

<span data-ttu-id="01322-197">Valige eemaldamisettevõttena määratletud ettevõttes moodulis Konsolideerimine suvand **Eemaldamisreegel**.</span><span class="sxs-lookup"><span data-stu-id="01322-197">In a company defined as an elimination company, select **Elimination journal** in the Consolidations module.</span></span> <span data-ttu-id="01322-198">Pärast töölehe nime valimist klõpsake valikut **Read**.</span><span class="sxs-lookup"><span data-stu-id="01322-198">After you have selected the journal name, click **Lines**.</span></span> <span data-ttu-id="01322-199">Pakkumise saate käivitada, valides menüü **Pakkumised** ja seejärel suvandi **Eemaldamisperiood.**</span><span class="sxs-lookup"><span data-stu-id="01322-199">You can run the proposal by selecting the **Proposals** menu and then selecting **Elimination proposal**.</span></span>

<span data-ttu-id="01322-200">Valige ettevõte, mis on konsolideeritud andmete allikas, ja seejärel valige reegel, mida soovite töödelda.</span><span class="sxs-lookup"><span data-stu-id="01322-200">Select the company that is the source of the consolidated data, and then choose the rule that you want to process.</span></span> <span data-ttu-id="01322-201">Sisestage eemaldamissummade otsimiseks algus- ja lõppkuupäev.</span><span class="sxs-lookup"><span data-stu-id="01322-201">Enter a start date to begin the search for elimination amounts, and an end date to end the search date for elimination amounts.</span></span> <span data-ttu-id="01322-202">Välja **Pearaamatu sisestamise kuupäev** kasutatakse töölehe pearaamatusse sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="01322-202">The **GL posting date** field is the date used for posting the journal to the general ledger.</span></span> <span data-ttu-id="01322-203">Pärast nupu **OK** klõpsamist saate summad üle vaadata ja töölehe sisestada.</span><span class="sxs-lookup"><span data-stu-id="01322-203">After you click **OK**, you can review the amounts and post the journal.</span></span>



