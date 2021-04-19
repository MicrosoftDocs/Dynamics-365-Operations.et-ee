---
title: Tarne alternatiivid
description: Müügitellimuse vastuvõtjad saavad alternatiivsete tellimuse täitmise valikute uurimiseks kasutada lehte Tarnealternatiivid.
author: ChristianRytt
ms.date: 04/10/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SalesLineDeliveryDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: 271623
ms.assetid: 527f6084-44fe-41bb-924f-4386e926358a
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: crytt
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: bf7211d3e922fb7ad6b66f6ec70ffc2fe7b5db81
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840649"
---
# <a name="delivery-alternatives"></a><span data-ttu-id="983cf-103">Tarne alternatiivid</span><span class="sxs-lookup"><span data-stu-id="983cf-103">Delivery alternatives</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="983cf-104">Müügitellimuse vastuvõtjad saavad alternatiivsete tellimuse täitmise valikute uurimiseks kasutada lehte **Tarne alternatiivid**.</span><span class="sxs-lookup"><span data-stu-id="983cf-104">Sales order takers can use the **Delivery alternatives** page to discover alternative order fulfillment options.</span></span>

<span data-ttu-id="983cf-105">Lehepaigutus **Tarne alternatiivid** annab ülevaate alternatiivsetest valikutest.</span><span class="sxs-lookup"><span data-stu-id="983cf-105">The **Delivery alternatives** page layout gives an overview of all alternative options.</span></span> <span data-ttu-id="983cf-106">See võimaldab tellimuse vastuvõtjatel vaadata täitmise võimalusi ka praegusest ettevõttest väljaspool.</span><span class="sxs-lookup"><span data-stu-id="983cf-106">It also lets order takers look beyond the current company for fulfillment opportunities.</span></span> <span data-ttu-id="983cf-107">Nüüd saavad nad vaadata nii kontsernisiseseid kui ka väliste hankijate pakutavaid võimalusi.</span><span class="sxs-lookup"><span data-stu-id="983cf-107">They can now view both intercompany opportunities and opportunities from external vendors.</span></span> <span data-ttu-id="983cf-108">Valikute sortimiseks tarnekuupäeva järgi saavad müügitellimuste vastuvõtjad vaadata tarnealternatiivide arukat loendit.</span><span class="sxs-lookup"><span data-stu-id="983cf-108">By sorting the options by delivery date, sales order takers can view an intelligent list of delivery alternatives.</span></span> <span data-ttu-id="983cf-109">Peale selle aitavad parameetrid neil soovitatud tarneid paremini hallata.</span><span class="sxs-lookup"><span data-stu-id="983cf-109">In addition, parameters help them better manage the suggested deliveries.</span></span> <span data-ttu-id="983cf-110">Kuna transpordiaeg võib mõjutada tarnekuupäevi, saavad müügitellimuse vastuvõtjad uurida vedajate pakutavaid erinevaid transpordivalikuid.</span><span class="sxs-lookup"><span data-stu-id="983cf-110">Because transport time can affect delivery dates, sales order takers can explore the various transportation choices that carriers offer.</span></span> <span data-ttu-id="983cf-111">Kuna iga soovituse kohta kuvatakse üksikasjalikku teavet, saavad tellimuste vastuvõtjad teha teadlikke otsuseid otse lehel **Tarnealternatiivid**.</span><span class="sxs-lookup"><span data-stu-id="983cf-111">Because detailed information is shown for each suggestion, order takers can make informed decisions directly from the **Delivery alternatives** page.</span></span>

## <a name="open-the-delivery-alternatives-page"></a><span data-ttu-id="983cf-112">Lehe Tarnealternatiivid avamine</span><span class="sxs-lookup"><span data-stu-id="983cf-112">Open the Delivery alternatives page</span></span>

<span data-ttu-id="983cf-113">Lehe **Tarne alternatiivid** saate avada müügitellimuse realt.</span><span class="sxs-lookup"><span data-stu-id="983cf-113">You can open the **Delivery alternatives** page from the sales order line.</span></span>

1. <span data-ttu-id="983cf-114">Valige **Tooted ja tarne \> Tarnealternatiivid**.</span><span class="sxs-lookup"><span data-stu-id="983cf-114">Select **Products and supply \> Delivery alternatives**.</span></span>
1. <span data-ttu-id="983cf-115">Valige **Rea üksikasjad \> Tarne \> Tarne alternatiivid.**</span><span class="sxs-lookup"><span data-stu-id="983cf-115">Select **Line details \> Delivery \> Delivery alternatives.**</span></span>

<span data-ttu-id="983cf-116">Saate lehe **Tarnealternatiivid** avada ka tööruumist **Müügitellimuse töötlemine ja päring**, valides suvandi **Tellimused ja lemmikud \> Hilinenud tellimuse read \> Tarnealternatiivid**. **Märkus.** Saate avada lehe **Tarnealternatiivid** ainult siis, kui mõlemad järgmised tingimused on täidetud.</span><span class="sxs-lookup"><span data-stu-id="983cf-116">You can also open the **Delivery alternatives** page by opening the **Sales order processing and inquiry** workspace, and then selecting **Orders and favorites \> Delayed order lines \> Delivery alternatives** **Note:** You can open the **Delivery alternatives** page only if both the following conditions are met:</span></span>

- <span data-ttu-id="983cf-117">Kogu kohustuslik müügireateave on sisestatud.</span><span class="sxs-lookup"><span data-stu-id="983cf-117">All mandatory sales line information is filled in.</span></span>
- <span data-ttu-id="983cf-118">Välja **Tarnekuupäeva kontroll** väärtuseks on valitud muu väärtus kui **Pole**.</span><span class="sxs-lookup"><span data-stu-id="983cf-118">The **Delivery date control** field is set to a value other than **None**.</span></span>

## <a name="delivery-date-control-methods"></a><span data-ttu-id="983cf-119">Tarnekuupäeva kontrollimeetodid</span><span class="sxs-lookup"><span data-stu-id="983cf-119">Delivery date control methods</span></span>

<span data-ttu-id="983cf-120">Tarnekuupäeva kontrollimeetod määrab, kuidas süsteem loob tarnekuupäevi, kuidas tarnekuupäevi arvutatakse ja millist teavet kuvatakse.</span><span class="sxs-lookup"><span data-stu-id="983cf-120">The delivery date control method determines how the system establishes delivery dates, how delivery alternatives are calculated, and what information is shown.</span></span> <span data-ttu-id="983cf-121">Pange tähele, et tarne kuupäeva kontroll võtab arvesse kalendreid.</span><span class="sxs-lookup"><span data-stu-id="983cf-121">Note that delivery date control takes calendars into consideration.</span></span> <span data-ttu-id="983cf-122">Seetõttu võivad soovitatud vastuvõtukuupäeva mõjutada järgmised kalendrid: laokalender, transpordikalender, hankija kalender ja kliendi kalender.</span><span class="sxs-lookup"><span data-stu-id="983cf-122">Therefore, the following calendars can affect the suggested receipt date: Warehouse calendar, Transport calendar, Vendor calendar, and Customer calendar.</span></span> <span data-ttu-id="983cf-123">Järgmises tabelis kirjeldatakse iga tarnekuupäeva kontrollimeetodit.</span><span class="sxs-lookup"><span data-stu-id="983cf-123">The following table describes each method for delivery date control.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="983cf-124"><strong>Meetod</strong></span><span class="sxs-lookup"><span data-stu-id="983cf-124"><strong>Method</strong></span></span></td>
<td><span data-ttu-id="983cf-125"><strong>Kirjeldus</strong></span><span class="sxs-lookup"><span data-stu-id="983cf-125"><strong>Description</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="983cf-126"><strong>None</strong></span><span class="sxs-lookup"><span data-stu-id="983cf-126"><strong>None</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="983cf-127">Tarnealternatiive müügiridade puhul ei toetata.</span><span class="sxs-lookup"><span data-stu-id="983cf-127">Delivery alternatives for sales lines aren't supported.</span></span> <span data-ttu-id="983cf-128">See suvand lülitab tarne kuupäeva kontrolli välja.</span><span class="sxs-lookup"><span data-stu-id="983cf-128">This option turns off delivery date control.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="983cf-129"><strong>Müügi täitmisaeg</strong></span><span class="sxs-lookup"><span data-stu-id="983cf-129"><strong>Sales lead time</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="983cf-130">Tarnealternatiivid arvutatakse eelmääratletud müügi täitmisaja põhjal.</span><span class="sxs-lookup"><span data-stu-id="983cf-130">Delivery alternatives are calculated based on the predefined sales lead time.</span></span> <span data-ttu-id="983cf-131">Transpordipäevad arvutatakse tarneviisi põhjal.</span><span class="sxs-lookup"><span data-stu-id="983cf-131">The transport days are calculated based on the mode of delivery.</span></span></li>
<li><span data-ttu-id="983cf-132">Tarnealternatiivid hõlmavad ladusid, millel on vaba kaubavaru, ja tarne-/nõudlustellimusi.</span><span class="sxs-lookup"><span data-stu-id="983cf-132">Delivery alternatives include warehouses that have on-hand inventory, and supply/demand orders.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="983cf-133"><strong>ATP</strong></span><span class="sxs-lookup"><span data-stu-id="983cf-133"><strong>ATP</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="983cf-134">Tarnealternatiivid arvutatakse loogika „saadaval lubamiseks” (ATP) põhjal.</span><span class="sxs-lookup"><span data-stu-id="983cf-134">Delivery alternatives are calculated based on available to promise (ATP) logic.</span></span> <span data-ttu-id="983cf-135">Arvesse võetakse praegust saadavust ja eeldatavat tulevast saadavust.</span><span class="sxs-lookup"><span data-stu-id="983cf-135">The current availability and expected future availability are considered.</span></span> <span data-ttu-id="983cf-136">Transpordipäevad arvutatakse tarneviisi põhjal.</span><span class="sxs-lookup"><span data-stu-id="983cf-136">The transport days are calculated based on the mode of delivery.</span></span></li>
<li><span data-ttu-id="983cf-137">Tarnealternatiivid hõlmavad ladusid, millel on vaba kaubavaru, ja tarne-/nõudlustellimusi.</span><span class="sxs-lookup"><span data-stu-id="983cf-137">Delivery alternatives include warehouses that have on-hand inventory, and supply/demand orders.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="983cf-138"><strong>ATP + väljamineku ohutusvaru</strong></span><span class="sxs-lookup"><span data-stu-id="983cf-138"><strong>ATP + Issue margin</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="983cf-139">Tarnealternatiivid arvutatakse nagu ATP-meetodi puhul, kuid arvutusse kaasatakse väljamineku ohutusvaru.</span><span class="sxs-lookup"><span data-stu-id="983cf-139">Delivery alternatives are calculated as for the ATP method, but the issue margin is included in the calculation.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="983cf-140"><strong>CTP</strong></span><span class="sxs-lookup"><span data-stu-id="983cf-140"><strong>CTP</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="983cf-141">Tarnealternatiivid arvutatakse loogika „võimeline lubama” (CTP) põhjal.</span><span class="sxs-lookup"><span data-stu-id="983cf-141">Delivery alternatives are calculated based on the capable to promise (CTP) logic.</span></span> <span data-ttu-id="983cf-142">Saadavuse määramiseks kasutatakse MRP koosnevusarvutust.</span><span class="sxs-lookup"><span data-stu-id="983cf-142">MRP explosion is used to determine availability.</span></span> <span data-ttu-id="983cf-143">Pange tähele, et CTP nihutab tarnekuupäevad minimaalselt müügi täitmisajale.</span><span class="sxs-lookup"><span data-stu-id="983cf-143">Note that, at a minimum, CTP offsets delivery dates to the sales lead time.</span></span> <span data-ttu-id="983cf-144">Transpordipäevad arvutatakse tarneviisi põhjal.</span><span class="sxs-lookup"><span data-stu-id="983cf-144">The transport days are calculated based on the mode of delivery.</span></span></li>
<li><span data-ttu-id="983cf-145">Tarnealternatiivid hõlmavad soovitusi järgmiste ladude kohta:</span><span class="sxs-lookup"><span data-stu-id="983cf-145">Delivery alternatives include suggestions for the following warehouses:</span></span>
<ul>
<li><span data-ttu-id="983cf-146">Praegune ladu</span><span class="sxs-lookup"><span data-stu-id="983cf-146">Current warehouse</span></span></li>
<li><span data-ttu-id="983cf-147">Vaikeladu</span><span class="sxs-lookup"><span data-stu-id="983cf-147">Default warehouse</span></span></li>
<li><span data-ttu-id="983cf-148">Kõik laod, millel on olemas vaba kaubavaru</span><span class="sxs-lookup"><span data-stu-id="983cf-148">All warehouses that have available on-hand inventory</span></span></li>
<li><span data-ttu-id="983cf-149">Kõik laod, millel on hanketellimusi</span><span class="sxs-lookup"><span data-stu-id="983cf-149">All warehouses that have supply orders</span></span></li>
<li><span data-ttu-id="983cf-150">Kõik laod, millel on aktiivseid koosluse versioone</span><span class="sxs-lookup"><span data-stu-id="983cf-150">All warehouses that have active bill of materials (BOM) versions</span></span></li>
</ul></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="view-information-about-delivery-alternatives"></a><span data-ttu-id="983cf-151">Tarnealternatiivide teabe kuvamine</span><span class="sxs-lookup"><span data-stu-id="983cf-151">View information about delivery alternatives</span></span>

<span data-ttu-id="983cf-152">Selles jaotises kirjeldatakse teavet saadaolevate tarnealternatiivide kohta igal lehe **Tarnealternatiivid** kiirkaardil.</span><span class="sxs-lookup"><span data-stu-id="983cf-152">This section describes the information about delivery alternatives that is available on each FastTab of the **Delivery alternatives** page.</span></span>

### <a name="the-product-fasttab"></a><span data-ttu-id="983cf-153">Toote kiirkaart</span><span class="sxs-lookup"><span data-stu-id="983cf-153">The Product FastTab</span></span>

<span data-ttu-id="983cf-154">Sellel kiirkaardil kuvatakse toote kokkuvõte ja praeguse müügirea üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="983cf-154">This FastTab shows a summary of the product and details of the current sales line.</span></span>

### <a name="the-delivery-alternatives-fasttab"></a><span data-ttu-id="983cf-155">Kiirkaart Tarnealternatiivid</span><span class="sxs-lookup"><span data-stu-id="983cf-155">The Delivery alternatives FastTab</span></span>

<span data-ttu-id="983cf-156">Sellel kiirkaardil kuvatakse tarnealternatiivide loend, mis on sorditud vastuvõtu kuupäeva järgi.</span><span class="sxs-lookup"><span data-stu-id="983cf-156">This FastTab shows a list of delivery alternatives that is sorted by receipt date.</span></span> <span data-ttu-id="983cf-157">Loendi kohal saate valida, millistel valikutel peaksid soovitused põhinema.</span><span class="sxs-lookup"><span data-stu-id="983cf-157">Above the list, you can select which options to base the suggestions on.</span></span> <span data-ttu-id="983cf-158">Saate valida ka tarneviisi, mis määrab ära transpordipäevad.</span><span class="sxs-lookup"><span data-stu-id="983cf-158">You can also select the mode of delivery, which determines the transport days.</span></span> <span data-ttu-id="983cf-159">Valikud on järgmised:</span><span class="sxs-lookup"><span data-stu-id="983cf-159">The following options are available:</span></span>

- <span data-ttu-id="983cf-160">**Kaasa muud tootevariandid** – see valik on saadaval tootevariantidega toodete puhul.</span><span class="sxs-lookup"><span data-stu-id="983cf-160">**Include other product variants** - This option is available for products that have product variants.</span></span> <span data-ttu-id="983cf-161">See hõlmab toote muude variantide tarnealternatiive.</span><span class="sxs-lookup"><span data-stu-id="983cf-161">It will include delivery alternatives for other variants of the product.</span></span> <span data-ttu-id="983cf-162">See valik pole CTP puhul saadaval.</span><span class="sxs-lookup"><span data-stu-id="983cf-162">This option isn't available for CTP.</span></span>
- <span data-ttu-id="983cf-163">**Kaasa osaline kogus** – vaikimisi kaasatakse ainult soovitused, mis täidavad müügirea täieliku koguse.</span><span class="sxs-lookup"><span data-stu-id="983cf-163">**Include partial quantity** - By default, only suggestions that fulfill the full quantity of the sales line are included.</span></span> <span data-ttu-id="983cf-164">Valige see suvand soovituste kaasamiseks, mis täidavad tellimuserea ainult osaliselt.</span><span class="sxs-lookup"><span data-stu-id="983cf-164">Select this option to include suggestions that only partially fulfill the order line.</span></span> <span data-ttu-id="983cf-165">See valik on kasulik, kui klient nõuab varasemat tarnekuupäeva ja nõustub osalise tarnega.</span><span class="sxs-lookup"><span data-stu-id="983cf-165">This option is useful when the customer requests an earlier delivery date and accepts partial delivery.</span></span>
- <span data-ttu-id="983cf-166">**Kaasa hilisemad kuupäevad** – vaikimisi kuvatakse ainult soovitused, mis on paremad (varasemad) kui praegused kuupäevad müügireal.</span><span class="sxs-lookup"><span data-stu-id="983cf-166">**Include later dates** - By default, only suggestions that are better (earlier) than the current dates on the sales line are shown.</span></span> <span data-ttu-id="983cf-167">Valige see suvand hilisemate kuupäevade kaasamiseks.</span><span class="sxs-lookup"><span data-stu-id="983cf-167">Select this option to include later dates.</span></span> <span data-ttu-id="983cf-168">See suvand võib olla kasulik olukordades, kus prioriteet on muudel parameetritel kui kuupäev.</span><span class="sxs-lookup"><span data-stu-id="983cf-168">This option can be useful in situations where parameters other than the date have priority.</span></span> <span data-ttu-id="983cf-169">Näiteks võib eelistatud olla kindel hankija või ladu.</span><span class="sxs-lookup"><span data-stu-id="983cf-169">For example, a specific vendor or warehouse might be preferred.</span></span>
- <span data-ttu-id="983cf-170">**Tarneviis** – saate valida transpordiaja ja -kulu optimeerimiseks eelistatud tarneviisi.</span><span class="sxs-lookup"><span data-stu-id="983cf-170">**Mode of delivery** - Select the preferred mode of delivery to optimize transport time and cost.</span></span> <span data-ttu-id="983cf-171">Näete mõju soovitatud tarnealternatiividele kohe.</span><span class="sxs-lookup"><span data-stu-id="983cf-171">You will immediately see the effect on the suggested delivery alternatives.</span></span> <span data-ttu-id="983cf-172">Seega on alternatiive lihtne võrrelda.</span><span class="sxs-lookup"><span data-stu-id="983cf-172">Therefore, it's easy to compare the alternatives.</span></span>
- <span data-ttu-id="983cf-173">**Kaasa hange** – hanke valimisel hõlmavad soovitatud tarnealternatiivid valikuid hankimiseks nii välistelt hankijatelt kui ka teistelt kontserni ettevõtetelt (kontsernisiseselt).</span><span class="sxs-lookup"><span data-stu-id="983cf-173">**Include procurement** - When procurement is selected, the suggested delivery alternatives include options to procure from both external vendors and other companies in the enterprise (intercompany).</span></span> <span data-ttu-id="983cf-174">Valikut **Kaasa hange** toetatakse ATP ja ATP + väljamineku ohutusvaru tarnekuupäeva kontrolli puhul.</span><span class="sxs-lookup"><span data-stu-id="983cf-174">The **Include procurement** option is supported for ATP and ATP + Issue margin delivery date control.</span></span> <span data-ttu-id="983cf-175">Kaasatakse kõik hankevalikud toote vaike-ostuhankijalt ja kõigilt toote kinnitatud hankijatelt.</span><span class="sxs-lookup"><span data-stu-id="983cf-175">Procurement options from the default purchase vendor for the product and all approved vendors for the product are included.</span></span>
- <span data-ttu-id="983cf-176">Väliste hankijate puhul põhineb arvutus ostu täitmisajal.</span><span class="sxs-lookup"><span data-stu-id="983cf-176">For external vendors, the calculation is based on the purchase lead time.</span></span>
- <span data-ttu-id="983cf-177">Kontsernisisese valiku puhul võtab arvutus arvesse, mis on hankeettevõttelt saadaval, arvestades hankeettevõtte tarnekuupäeva kontrolli.</span><span class="sxs-lookup"><span data-stu-id="983cf-177">For intercompany, the calculation considers what is available from the sourcing company, based on delivery date control in the sourcing company.</span></span>
- <span data-ttu-id="983cf-178">**Tarnetüüp** (hankimisel)</span><span class="sxs-lookup"><span data-stu-id="983cf-178">**Delivery type** (Relevant for procurement)</span></span>
  - <span data-ttu-id="983cf-179">**Varud** – tooted saadetakse hankelaost müügireal toodud tegevuskohta/lattu.</span><span class="sxs-lookup"><span data-stu-id="983cf-179">**Stock** - Products are shipped from the sourcing warehouse to the site/warehouse on the sales line.</span></span> <span data-ttu-id="983cf-180">Seejärel saadetakse need laost kliendile.</span><span class="sxs-lookup"><span data-stu-id="983cf-180">They are then shipped from that warehouse to the customer.</span></span>
  - <span data-ttu-id="983cf-181">**Otsetarne** – -tooted saadetakse hankelaost otse kliendile.</span><span class="sxs-lookup"><span data-stu-id="983cf-181">**Direct delivery** - Products are shipped directly from the sourcing warehouse to the customer.</span></span>

### <a name="the-availability-information-fasttab"></a><span data-ttu-id="983cf-182">Kiirkaart Kättesaadavuse teave</span><span class="sxs-lookup"><span data-stu-id="983cf-182">The Availability information FastTab</span></span>

<span data-ttu-id="983cf-183">Selle kiirkaardi teave on seotud valitud tarnealternatiivi reaga.</span><span class="sxs-lookup"><span data-stu-id="983cf-183">Information on this FastTab is related to the delivery alternative line that is selected.</span></span> <span data-ttu-id="983cf-184">Olenevalt müügitellimuse tarnekuupäeva kontrollist kuvatakse järgmine teave.</span><span class="sxs-lookup"><span data-stu-id="983cf-184">The following information is shown, depending on the delivery date control for the sales line:</span></span>

- <span data-ttu-id="983cf-185">**Müügi täitmisaeg**</span><span class="sxs-lookup"><span data-stu-id="983cf-185">**Sales lead time**</span></span>
  - <span data-ttu-id="983cf-186">**Saadaval täna** – kuvatakse praegune füüsiliselt vaba kaubavaru, füüsiliselt reserveeritud ja füüsiliselt saadaolevad varud.</span><span class="sxs-lookup"><span data-stu-id="983cf-186">**Available today** - Show the current physical on-hand, physical reserved, and available physical inventory.</span></span>
  - <span data-ttu-id="983cf-187">**Parameetrid** – kuvatakse varude ühik ja müügi täitmisaeg.</span><span class="sxs-lookup"><span data-stu-id="983cf-187">**Parameters** - Show the inventory unit and sales lead time.</span></span>

- <span data-ttu-id="983cf-188">**ATP ja ATP + väljamineku ohutusvaru**</span><span class="sxs-lookup"><span data-stu-id="983cf-188">**ATP and ATP + Issue margin**</span></span>
  - <span data-ttu-id="983cf-189">**Saadaval täna** – kuvatakse praegune füüsiliselt vaba kaubavaru, füüsiliselt reserveeritud ja füüsiliselt saadaolevad varud.</span><span class="sxs-lookup"><span data-stu-id="983cf-189">**Available today** - Show the current physical on-hand, physical reserved, and available physical inventory.</span></span>
  - <span data-ttu-id="983cf-190">**Parameetrid** – kuvatakse varude ühik ja müügi täitmisaeg.</span><span class="sxs-lookup"><span data-stu-id="983cf-190">**Parameters** - Show the inventory unit and sales lead time.</span></span>
  - <span data-ttu-id="983cf-191">**Kättesaadavus tulevikus** – kuvatakse graafilisel kujul praegune ja tulevane kättesaadavus jaotises **Tarnealternatiivid** valitud tegevukoha ning lao kohta.</span><span class="sxs-lookup"><span data-stu-id="983cf-191">**Future availability** - Show a graphical representation of current and future availability for the selected site and warehouse under **Delivery alternatives**.</span></span> <span data-ttu-id="983cf-192">Toote tulevikus saadavuse kohta üksikasjalikuma teabe nägemiseks valige diagrammi veerud.</span><span class="sxs-lookup"><span data-stu-id="983cf-192">You can select the chart columns to see more detailed information about the future availability of the product.</span></span> <span data-ttu-id="983cf-193">Liugur näitab asjakohaste nõudlus- ja tarnetellimuste loendit ATP ajavahemikus.</span><span class="sxs-lookup"><span data-stu-id="983cf-193">The slider shows a list of relevant demand and supply orders within the ATP time fence.</span></span>

- <span data-ttu-id="983cf-194">**CTP**</span><span class="sxs-lookup"><span data-stu-id="983cf-194">**CTP**</span></span>
  - <span data-ttu-id="983cf-195">**Saadaval täna** – kuvatakse praegune füüsiliselt vaba kaubavaru, füüsiliselt reserveeritud ja füüsiliselt saadaolevad varud.</span><span class="sxs-lookup"><span data-stu-id="983cf-195">**Available today** - Show the current physical on-hand, physical reserved, and available physical inventory.</span></span>
  - <span data-ttu-id="983cf-196">**Parameetrid** – kuvatakse varude ühik ja müügi täitmisaeg.</span><span class="sxs-lookup"><span data-stu-id="983cf-196">**Parameters** - Show the inventory unit and sales lead time.</span></span>
  - <span data-ttu-id="983cf-197">**Koosnevusarvutus** – kuvatakse koosnevusarvutus valitud tarnealternatiivi kohta.</span><span class="sxs-lookup"><span data-stu-id="983cf-197">**Explosion** - Show a supply explosion of the selected delivery alternative.</span></span> <span data-ttu-id="983cf-198">Koosnevusarvutuses kuvatavate väljade ja varude dimensioonide muutmiseks saate kasutada jaotist **Seadistus**.</span><span class="sxs-lookup"><span data-stu-id="983cf-198">You can use **Setup** to change the fields and inventory dimensions that are shown in the explosion.</span></span>

### <a name="the-impact-of-selected-alternative-fasttab"></a><span data-ttu-id="983cf-199">Kiirkaart Valitud alternatiivi mõju</span><span class="sxs-lookup"><span data-stu-id="983cf-199">The Impact of selected alternative FastTab</span></span>

<span data-ttu-id="983cf-200">Sellel kiirkaardil on toodud esile valitud tarnealternatiivi mõju.</span><span class="sxs-lookup"><span data-stu-id="983cf-200">This FastTab highlights the impact of the selected delivery alternative.</span></span> <span data-ttu-id="983cf-201">Kui valite **OK**, värskendatakse müügirida VALITUD veergudel esiletõstetud väärtustega.</span><span class="sxs-lookup"><span data-stu-id="983cf-201">If you select **OK**, the sales line is updated with the highlighted values in the SELECTED columns.</span></span> <span data-ttu-id="983cf-202">Pange tähele, et kui valitud tarnealternatiivi kogus on väiksem kui müügirea kogus, luuakse tarnegraafik ja tellimuserida tükeldatakse kaheks reaks: üks rida valitud koguse jaoks ja teine rida ülejäänud koguse jaoks.</span><span class="sxs-lookup"><span data-stu-id="983cf-202">Note that, if the quantity on the selected delivery alternative is less than quantity on the sales line, a delivery schedule is created, and the order line is split into two lines: one line for the selected quantity and one line for the remaining quantity.</span></span> <span data-ttu-id="983cf-203">Saate värskendada ka äriandmete rida, et see vastaks graafiku ridadele ja mõjutaks hinda.</span><span class="sxs-lookup"><span data-stu-id="983cf-203">You can also update the commercial line so that it matches the schedule lines and affects the pricing.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="983cf-204">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="983cf-204">Additional resources</span></span>

[<span data-ttu-id="983cf-205">Tellimuse lubamine</span><span class="sxs-lookup"><span data-stu-id="983cf-205">Order promising</span></span>](delivery-dates-available-promise-calculations.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]