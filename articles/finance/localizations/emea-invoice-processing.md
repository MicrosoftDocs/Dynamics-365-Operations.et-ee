---
title: Arve töötlemine
description: See teema annab teavet arve töötlemise kohta Ida-Euroopa puhul.
author: EvgenyPopovMBS
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustParameters, VendParameters
audience: Application User
ms.reviewer: kfend
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, Russia, Italy
ms.author: epopov
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 9ec3cd6088f311c25d8c506fda7563064669b5ea
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814964"
---
# <a name="invoice-processing"></a><span data-ttu-id="528e2-103">Arve töötlemine</span><span class="sxs-lookup"><span data-stu-id="528e2-103">Invoice processing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="528e2-104">See teema käsitleb lühidalt mõningaid riigipõhiseid stsenaariume, nagu EL-i sisene käibemaks (KM) ja viitmaks.</span><span class="sxs-lookup"><span data-stu-id="528e2-104">This topic briefly describes some country-specific scenarios, such as intra-community value-added tax (VAT) and deferred tax.</span></span> <span data-ttu-id="528e2-105">Mõne Euroopa riigi seadusenõuded mõjutavad arveldusprotsessi.</span><span class="sxs-lookup"><span data-stu-id="528e2-105">Legal requirements for some European countries affect the invoicing process.</span></span> <span data-ttu-id="528e2-106">Selles teemas antakse teavet ka selle kohta, kuidas nende riikide puhul klientide ja hankijate arveid töödeldakse.</span><span class="sxs-lookup"><span data-stu-id="528e2-106">This topic also provides information about how customer and vendor invoices are processed for these countries.</span></span> 
<table>
<thead>
<tr>
<th><span data-ttu-id="528e2-107">Stsenaarium</span><span class="sxs-lookup"><span data-stu-id="528e2-107">Scenario</span></span></th>
<th><span data-ttu-id="528e2-108">Riigid</span><span class="sxs-lookup"><span data-stu-id="528e2-108">Countries</span></span></th>
<th><span data-ttu-id="528e2-109">Funktsioonimuudatuste kirjeldus</span><span class="sxs-lookup"><span data-stu-id="528e2-109">Description of the functionality changes</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="528e2-110"> Müügireskontro ja ostureskontro kuupäevad käibemaksu jaoks</span><span class="sxs-lookup"><span data-stu-id="528e2-110">Accounts receivable and Accounts payable dates for VAT</span></span></td>
<td><span data-ttu-id="528e2-111">Tšehhi Vabariik, Poola</span><span class="sxs-lookup"><span data-stu-id="528e2-111">Czech Republic, Poland</span></span></td>
<td>
<p><span data-ttu-id="528e2-112">Euroopa Liidu (EL) riikidest kaupade ostmisel on kohustuslik iseseisev KM arvestamine:</span><span class="sxs-lookup"><span data-stu-id="528e2-112">When goods are purchased from European Union (EU) countries, there is an obligation of self-assessment of VAT:</span></span></p>
<ul>
<li><span data-ttu-id="528e2-113">arvestatud KM tuleb maksta sellel KM-perioodil, millal arve väljastati (dokumendi kuupäev).</span><span class="sxs-lookup"><span data-stu-id="528e2-113">The output VAT must be paid in a VAT period where the invoice was issued (document date).</span></span></li>
<li><span data-ttu-id="528e2-114">Sisendkäibemaksu ei saa enne dokumendi kättesaamist (KM registreerimise kuupäeva) maha arvestada.</span><span class="sxs-lookup"><span data-stu-id="528e2-114">The input VAT can’t be deducted before the document receipt (VAT register date).</span></span></li>
</ul>
<p><span data-ttu-id="528e2-115">Selle stsenaariumi toetamiseks peaksid olema konfigureeritud järgmised sätted.</span><span class="sxs-lookup"><span data-stu-id="528e2-115">The following settings should be configured to support this scenario:</span></span></p>
<ul>
<li><span data-ttu-id="528e2-116">Aktiveerige lehel <strong>Ostureskontro parameetrid</strong> valik <strong>EL-i sisene KM</strong> ja <strong>Dokumendi kuupäev EL-i sisese käibemaksu puhul</strong>.</span><span class="sxs-lookup"><span data-stu-id="528e2-116">On the <strong>Accounts payable parameters</strong> page, enable the <strong>Intra-community VAT</strong> and <strong>Document date for intra-community VAT</strong> parameters.</span></span></li>
<li><span data-ttu-id="528e2-117">Seadistage kuni kaks käibemaksukoodi: üks, millel on positiivne käibemaksuprotsent ja teine, millel on negatiivne käibemaksuprotsent.</span><span class="sxs-lookup"><span data-stu-id="528e2-117">Set up two sales tax codes, one that has a positive sales tax percentage and one that has a negative sales tax percentage.</span></span></li>
<li><span data-ttu-id="528e2-118">Seadistage käibemaksugrupp, mis sisaldab nii positiivset kui ka negatiivset käibemaksukoodi.</span><span class="sxs-lookup"><span data-stu-id="528e2-118">Set up a sales tax group that includes both the positive and negative sales tax codes.</span></span> <span data-ttu-id="528e2-119">Negatiivse käibemaksukoodi puhul määrake parameetri <strong>EL-i sisene KM</strong> väärtuseks <strong>Jah</strong>.</span><span class="sxs-lookup"><span data-stu-id="528e2-119">For the negative sales tax code, set the <strong>Intracommunity VAT</strong> parameter to <strong>Yes</strong>.</span></span></li>
</ul>
<p><span data-ttu-id="528e2-120">Pärast edukat seadistust on ostudel kaks sisestatud käibemaksukannet:</span><span class="sxs-lookup"><span data-stu-id="528e2-120">After successful setup, purchases will have two posted sales tax transactions:</span></span></p>
<ul>
<li><span data-ttu-id="528e2-121">positiivne kanne, mille suund on <strong>saadaolev käibemaks</strong> ja millel on arve sisestuslehe kuupäevaga võrdne käibemaksu registreerimiskuupäev;</span><span class="sxs-lookup"><span data-stu-id="528e2-121">A positive transaction that has a direction of <strong>sales tax receivable</strong> and a VAT register date that equals the date from the invoice posting page.</span></span></li>
<li><span data-ttu-id="528e2-122">negatiivne kanne, mille suund on <strong>maksmisele kuuluv käibemaks</strong> ja mille käibemaksu registreerimiskuupäev on võrdne dokumendi kuupäevaga.</span><span class="sxs-lookup"><span data-stu-id="528e2-122">A negative transaction that has a direction of <strong>sales tax payable</strong> and a VAT register date that equals the document date.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="528e2-123">Müügidokumendi kuupäeva muutmine.</span><span class="sxs-lookup"><span data-stu-id="528e2-123">Modify a sales document date.</span></span></td>
<td><span data-ttu-id="528e2-124">Kõik Ida-Euroopa riigid</span><span class="sxs-lookup"><span data-stu-id="528e2-124">All Eastern European countries</span></span></td>
<td><p><span data-ttu-id="528e2-125">Saate muuta välja <strong>Dokumendi kuupäev</strong> projekti arvel.</span><span class="sxs-lookup"><span data-stu-id="528e2-125">You can modify the <strong>Document date</strong> field on a project invoice.</span></span> <span data-ttu-id="528e2-126">See kuupäev kuvatakse prinditud arvel.</span><span class="sxs-lookup"><span data-stu-id="528e2-126">This date appears on the printed invoice.</span></span></p>
<p><span data-ttu-id="528e2-127">Lehtedel <strong>Arve sisestamine</strong> ja <strong>Vabas vormis arve</strong> on ka väli <strong>Dokumendi kuupäev</strong>.</span><span class="sxs-lookup"><span data-stu-id="528e2-127">There is also a <strong>Document date</strong> field on the <strong>Posting invoice</strong> and <strong>Free text invoice</strong> pages.</span></span> <span data-ttu-id="528e2-128">Pärast arve sisestamist kuvatakse dokumendi kuupäev arve päises.</span><span class="sxs-lookup"><span data-stu-id="528e2-128">After you post an invoice, the document date appears on the invoice header.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="528e2-129">Dokumendi kuupäev vahetuskursside jaoks</span><span class="sxs-lookup"><span data-stu-id="528e2-129">Document date for exchange rates</span></span></td>
<td><span data-ttu-id="528e2-130">Poola, Ungari, Tšehhi Vabariik, Itaalia</span><span class="sxs-lookup"><span data-stu-id="528e2-130">Poland, Hungary, Czech Republic, Italy</span></span></td>
<td>
<p><span data-ttu-id="528e2-131">Seaduses on äritehingute jaoks kehtivate vahetuskursside valimiseks erinevad reeglid.</span><span class="sxs-lookup"><span data-stu-id="528e2-131">Legislation provides different rules for selecting valid exchange rates for business transactions.</span></span> <span data-ttu-id="528e2-132">Lehtede <strong>Müügireskontro parameetrid</strong> ja <strong>Ostureskontro parameetrid</strong> väljal <strong>Vahetuskursi kuupäev</strong> saab valida kuupäeva, mida tuleks kasutada ostu- ja müügidokumentidel arvestusvaluuta arvutuste jaoks.</span><span class="sxs-lookup"><span data-stu-id="528e2-132">In the <strong>Exchange rate date</strong> field on the <strong>Accounts receivable parameters</strong> and <strong>Accounts payable parameters</strong> pages, you can select the date that should be used for amounts in the accounting currency calculation on purchase and sales documents.</span></span> <span data-ttu-id="528e2-133">Andmete sisestamisel toob süsteem selle parameetri põhjal kande vahetuskursi.</span><span class="sxs-lookup"><span data-stu-id="528e2-133">During data entry, the system retrieves the exchange rate for the transaction, based on this parameter.</span></span></p>
<blockquote>[!NOTE]<br><span data-ttu-id="528e2-134">Itaalia puhul rakendub see funktsioon ainult ostureskontro moodulis.</span><span class="sxs-lookup"><span data-stu-id="528e2-134">For Italy, this functionality is only applicable in the Accounts payable module.</span></span> <span data-ttu-id="528e2-135">Ostureskontro parameetrites saab kasutaja valida <strong>Sisestamise kuupäeva</strong> või <strong>Dokumendi kuupäeva</strong> väljal <strong>Vahetuskursi kuupäev</strong>.</span><span class="sxs-lookup"><span data-stu-id="528e2-135">In the Accounts payable parameters, a user can select <strong>Posting date</strong> or <strong>Document date</strong> in the <strong>Exchange rate date</strong> field.</span></span>   </blockquote>
<blockquote>[!NOTE]<br><span data-ttu-id="528e2-136">Kui määrate välja <strong>Vahetuskursi kuupäev</strong> väärtuseks <strong>Dokumendi kuupäev (ainult EL-i kaubanduse puhul)</strong>, kasutab süsteem käibemaksugruppi.</span><span class="sxs-lookup"><span data-stu-id="528e2-136">When you set the <strong>Exchange rate date</strong> field to <strong>Document date (for EU trade only)</strong>, the system uses the sales tax group.</span></span> <span data-ttu-id="528e2-137">Käibemaksugrupi puhul on vahekaardil <strong>Üldine</strong> parameeter <strong>EL-i kaubandus</strong>. Kui käibemaksugrupil on valiku <strong>EL-i kaubandus</strong> väärtuseks määratud <strong>Jah</strong> ja kui see käibemaksugrupp on dokumendi päises olemas, toob süsteem vahetuskursi dokumendi kuupäeva põhjal.</span><span class="sxs-lookup"><span data-stu-id="528e2-137">For the sales tax group, there is a <strong>EU trade</strong> parameter on the <strong>General</strong> tab. If the <strong>EU trade</strong> option is set to <strong>Yes</strong> for the sales tax group, and if this sales tax group exists on the header of the document, the system retrieves the exchange rate based on the document date.</span></span> <span data-ttu-id="528e2-138">Kui selle käibemaksugrupi puhul on valiku <strong>EL-i kaubandus</strong> väärtuseks määratud <strong>Ei</strong>, toob süsteem vahetuskursi dokumendi sisestuskuupäeva põhjal.</span><span class="sxs-lookup"><span data-stu-id="528e2-138">If the <strong>EU trade</strong> option is set to <strong>No</strong> for this sales tax group, the system retrieves the exchange rate based on the posting date of the document.</span></span></blockquote>
</td>
</tr>
<tr>
<td><span data-ttu-id="528e2-139">Kaubavahetuse kuupäevad, käibemaksu registreerimise kuupäevad ja käibemaksu kuupäeva juhtimine</span><span class="sxs-lookup"><span data-stu-id="528e2-139">Trade dates, VAT register dates, and document and VAT date control</span></span></td>
<td><span data-ttu-id="528e2-140">Poola, Ungari, Tšehhi Vabariik</span><span class="sxs-lookup"><span data-stu-id="528e2-140">Poland, Hungary, Czech Republic</span></span></td>
<td>
<p><span data-ttu-id="528e2-141">Müügikuupäev ja dokumendi vastuvõtukuupäev on käibemaksuaruande jaoks kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="528e2-141">The sales date and the document receipt date are required for VAT reporting:</span></span></p>
<ul>
<li><span data-ttu-id="528e2-142">Müügikuupäev on kande täitmise kuupäev müügireskontrol.</span><span class="sxs-lookup"><span data-stu-id="528e2-142">The sales date is the fulfillment date of the transaction in Accounts receivable.</span></span></li>
<li><span data-ttu-id="528e2-143">Dokumendi vastuvõtukuupäev on kuupäev, mis näitab käibemaksu mahaarvamise nõudmise õigusi ostureskontrol.</span><span class="sxs-lookup"><span data-stu-id="528e2-143">The document receipt date is a date that demonstrates the rights to claim a VAT deduction in Accounts payable.</span></span> <span data-ttu-id="528e2-144">Igal vastuvõetaval dokumendil on auditeerimiseks kuupäev.</span><span class="sxs-lookup"><span data-stu-id="528e2-144">Each document that is received has a date for audit purposes.</span></span></li>
</ul>
<p><span data-ttu-id="528e2-145">Ungari kuupäeva tähtaegade funktsioon, Tšehhi Vabariigi kuupäevade täitmise funktsioon ja Poola KM registreerimise kuupäeva funktsioon hõlmavad maksuteabe aruandluse nõuet, mis põhineb sisestuskuupäevast erineval kuupäeval.</span><span class="sxs-lookup"><span data-stu-id="528e2-145">The Hungarian functionality for date deadlines, the Czech Republic functionality for fulfill dates, and the Polish functionality for the VAT register date include the requirement for tax information reporting that is based on a date that differs from the posting date.</span></span></p>
<p><span data-ttu-id="528e2-146">Väli <strong>KM-registri kuupäev</strong> toetab seda nõuet ja kuvatakse rohkem kui 20 lehel.</span><span class="sxs-lookup"><span data-stu-id="528e2-146">The <strong>Date of VAT register</strong> field supports this requirement and appears on more than 20 pages.</span></span> <span data-ttu-id="528e2-147">Nende lehtede hulka kuuluvad töölehed, müügitellimused, ostutellimused, vabas vormis arved, hankija arve töölehed ja projektiarved.</span><span class="sxs-lookup"><span data-stu-id="528e2-147">These pages include journals, sales orders, purchase orders, free-text invoices, vendor invoice journals, and project invoices.</span></span> <span data-ttu-id="528e2-148">Dokumentide värskendamisel või sisestamisel sisestatakse kõik maksud käibemaksuregistri asjakohase kuupäevaga ja kuupäev on lisatud lehtedele, nt kliendi ja hankija arve töölehtede lehtedele.</span><span class="sxs-lookup"><span data-stu-id="528e2-148">When you update or post the documents, all taxes are posted by using the corresponding date of the VAT register, and the date is included on pages such as the customer and vendor invoice journals pages.</span></span></p>
<p><span data-ttu-id="528e2-149">Konkreetselt Tšehhi Vabariigi puhul võib väli <strong>Käibemaksu registreerimiskuupäev</strong> sisestamise ajal tühi olla, kui KM-sisestus on edasi lükatud.</span><span class="sxs-lookup"><span data-stu-id="528e2-149">Specifically, for the Czech Republic, the <strong>VAT register date</strong> field can be blank during posting, in the event of postponed VAT posting.</span></span> <span data-ttu-id="528e2-150">Vastasel korral väli on kohustuslik ja tuleb täita.</span><span class="sxs-lookup"><span data-stu-id="528e2-150">Otherwise, the field is mandatory and must be filled in.</span></span></p>
<p><span data-ttu-id="528e2-151">Kuupäeva valideerimise parameetrid saab määrata lehel <strong>Käibemaksugrupid</strong>.</span><span class="sxs-lookup"><span data-stu-id="528e2-151">Date validation parameters can be set on the <strong>Sales tax groups</strong> page:</span></span></p>
<ul>
<li><span data-ttu-id="528e2-152">Parameetreid <strong>KM-registri kuupäeva täitmine</strong> ja <strong>Müügikuupäeva täitmine</strong> kasutatakse täitmise vaikemeetodina sobivatel kuupäevadel.</span><span class="sxs-lookup"><span data-stu-id="528e2-152">The <strong>Date of VAT register filling</strong> and <strong>Sales date filling</strong> parameters are used as a default filling method for appropriate dates.</span></span> <span data-ttu-id="528e2-153">Saadaval on ka käsitsi sisestus ja mitu automaatset sisestusmeetodit.</span><span class="sxs-lookup"><span data-stu-id="528e2-153">Manual input and several automated input methods are also available.</span></span></li>
<li><span data-ttu-id="528e2-154">Väljal <strong>Kohustuslik müügikuupäev</strong> on näidatud, kas müügikuupäev tuleb sisestada enne müügiarve sisestamist.</span><span class="sxs-lookup"><span data-stu-id="528e2-154">The <strong>Mandatory sales date</strong> field indicates whether the sales date must be entered before a sales invoice is posted.</span></span></li>
</ul>
<p><span data-ttu-id="528e2-155">Lehel <strong>Käibemaksuregistri kanded</strong> saate täita sisestatud maksukannete kohta käibemaksuregistri tühjad kuupäevad.</span><span class="sxs-lookup"><span data-stu-id="528e2-155">On the <strong>VAT Register transactions</strong> page, you can fill in blank dates for the VAT register for posted tax transactions.</span></span></p>
</td>
</tr>
<tr>
<td><span data-ttu-id="528e2-156">KM-registri kuupäevad, mis sisaldavad viitmaksu</span><span class="sxs-lookup"><span data-stu-id="528e2-156">VAT register dates that include deferred tax</span></span></td>
<td><span data-ttu-id="528e2-157">Ungari</span><span class="sxs-lookup"><span data-stu-id="528e2-157">Hungary</span></span></td>
<td>
<p><span data-ttu-id="528e2-158">Ungari maksuseadused nõuavad, et arved koostatakse kas täitmise ajal või hiljemalt 15 päeva pärast täitmist.</span><span class="sxs-lookup"><span data-stu-id="528e2-158">Hungary tax regulations require that invoices be created at either the time of fulfillment or no later than 15 days after fulfillment.</span></span></p>
<p><span data-ttu-id="528e2-159">Täitmise kuupäev on tellitud teenuste osutamise või tellitud kaupade kohaletoimetamise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="528e2-159">The fulfillment date is either the date when the ordered services were provided or the date when ordered items were delivered.</span></span> <span data-ttu-id="528e2-160">Dokumentide muutmisel või sisestamisel sisestatakse kõik maksud, kasutades vastavat käibemaksuregistri kuupäeva, ja kuupäev kuvatakse vastavatel lehtedel.</span><span class="sxs-lookup"><span data-stu-id="528e2-160">When you update or post the documents, all taxes are posted by using the corresponding date of the VAT register, and the date appears on relevant pages.</span></span> <span data-ttu-id="528e2-161">Lisaks nõuavad eeskirjad, et pidevalt osutatavate teenuste (nt rentimine, liisimine, konsultatsioonid ja küte) KM vastaks järgmistele kriteeriumidele.</span><span class="sxs-lookup"><span data-stu-id="528e2-161">Additionally, regulations require that VAT on continuous delivery of services, such as renting, leasing, consulting, and heating, meet the following criteria:</span></span></p>
<ul>
<li><span data-ttu-id="528e2-162">KM tuleb sisestada spetsiaalsele pearaamatukontole arve kuupäeval.</span><span class="sxs-lookup"><span data-stu-id="528e2-162">VAT must be posted to a dedicated general ledger account on the invoice date.</span></span></li>
<li><span data-ttu-id="528e2-163">KM tuleb kanda üle spetsiaalsetelt kontodelt saadaoleva või tasumisele kuuluva käibemaksu kontole ja see peab kajastuma ettenähtud kuupäeva KM-aruandes.</span><span class="sxs-lookup"><span data-stu-id="528e2-163">VAT must be transferred from the special accounts to a sales tax receivable account or a payable account, and must be included in the VAT report on the due date.</span></span></li>
</ul>
<p><span data-ttu-id="528e2-164">Nende nõuete täitmiseks võite kanda pearaamatu sisestused laekuva viitmaksu kontole ja väljamineva viitmaksu kontole.</span><span class="sxs-lookup"><span data-stu-id="528e2-164">To support these requirements, you can transfer General ledger postings to the Deferred incoming tax account and the Deferred outgoing tax account.</span></span> <span data-ttu-id="528e2-165">Kuid kõigepealt peavad olema täidetud järgmised eeltingimused.</span><span class="sxs-lookup"><span data-stu-id="528e2-165">However, you must first complete the following prerequisites:</span></span></p>
<ul>
<li><span data-ttu-id="528e2-166">Seadistage pearaamatu sisestamisgruppides maksmisele kuuluva viitkäibemaksu ja saadaoleva viitkäibemaksu pearaamatukontod.</span><span class="sxs-lookup"><span data-stu-id="528e2-166">Set up the Deferred VAT Payable and Deferred VAT Receivable ledger accounts in ledger posting groups.</span></span></li>
<li><span data-ttu-id="528e2-167">Lubage kauba käibemaksugruppide parameeter <strong>Viitkäibemaks</strong>.</span><span class="sxs-lookup"><span data-stu-id="528e2-167">Enable the <strong>Deferred VAT</strong> parameter for item sales tax groups.</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="528e2-168"> Kohustuslik käibemaksu kuupäev</span><span class="sxs-lookup"><span data-stu-id="528e2-168">Mandatory VAT date</span></span></td>
<td><span data-ttu-id="528e2-169">Poola</span><span class="sxs-lookup"><span data-stu-id="528e2-169">Poland</span></span></td>
<td>
<p><span data-ttu-id="528e2-170">Võite nõuda, et KM-registri kuupäev lisataks ostu- ja müügikande kirjetele.</span><span class="sxs-lookup"><span data-stu-id="528e2-170">You can require that the date of the VAT register be included in purchase and sales transaction records.</span></span> <span data-ttu-id="528e2-171">Seetõttu saab KM-registri kuupäeva hõivata enne kande sisestamist.</span><span class="sxs-lookup"><span data-stu-id="528e2-171">Therefore, the date of the VAT register can be captured before a transaction is posted.</span></span> <span data-ttu-id="528e2-172">Selle funktsiooni abil saate vältida mitme kande töötlemist perioodi lõpus.</span><span class="sxs-lookup"><span data-stu-id="528e2-172">This functionality helps you avoid having to handle multiple transactions at the end of the period.</span></span></p>
<p><span data-ttu-id="528e2-173">Saate muuta välja <strong>KM-registri kuupäev</strong> kliendi või hankija kannete sisestamisel kohustuslikuks.</span><span class="sxs-lookup"><span data-stu-id="528e2-173">You can make the <strong>Date of VAT register</strong> field mandatory when customer or vendor transactions are posted.</span></span> <span data-ttu-id="528e2-174">Välja kohustuslikuks muutmiseks lubage seotud kliendi või hankija kontol valik <strong>KM kuupäev on nõutav</strong>.</span><span class="sxs-lookup"><span data-stu-id="528e2-174">To make this field mandatory, enable the <strong>VAT date is required</strong> option for the related customer or vendor account.</span></span></p>
</td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]