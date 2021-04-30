---
title: Hindade, allahindluste, lepete ja tagasimaksete tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada hindadega, allahindlustega, lepetega ja tagasimaksetega töötamisel tekkivaid probleeme.
author: SmithaNataraj
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-9-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 2ccc1d52b83f9319af1c6336c1876c795c70028a
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908515"
---
# <a name="troubleshoot-prices-discounts-agreements-and-rebates"></a><span data-ttu-id="8fbdf-103">Hindade, allahindluste, lepete ja tagasimaksete tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="8fbdf-103">Troubleshoot prices, discounts, agreements, and rebates</span></span>

<span data-ttu-id="8fbdf-104">Selles teemas kirjeldatakse, kuidas lahendada hindadega, allahindlustega, lepetega ja tagasimaksetega töötamisel tekkivaid probleeme.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-104">This topic describes how to fix issues that you might encounter while you work with prices, discounts, agreements, and rebates.</span></span>

## <a name="i-cant-link-a-purchase-agreement-to-a-purchase-order-line-after-the-purchase-order-is-created"></a><span data-ttu-id="8fbdf-105">Pärast ostutellimuse loomist ei saa ma ostulepingut ostutellimuse reaga siduda.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-105">I can't link a purchase agreement to a purchase order line after the purchase order is created.</span></span>

<span data-ttu-id="8fbdf-106">Ostutellimuse loomisel tuleb ostuleping ostutellimusega seostada.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-106">A purchase agreement must be associated with a purchase order when the purchase order is created.</span></span> <span data-ttu-id="8fbdf-107">Vastasel juhul ei saa ostutellimuse ridu seostada ostulepingu ridadega.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-107">Otherwise, purchase order lines can't be associated with purchase agreement lines.</span></span>

## <a name="what-check-triggers-the-update-prices-and-discounts-entered-manually-or-external-document-message"></a><span data-ttu-id="8fbdf-108">Mis põhjustab teate „Värskendatud hinnad ja allahindlused sisestati käsitsi või tegemist on välise dokumendiga”?</span><span class="sxs-lookup"><span data-stu-id="8fbdf-108">What check triggers the "Update prices and discounts entered manually or external document" message?</span></span>

<span data-ttu-id="8fbdf-109">Kui muudate tarnekuupäeva, võidakse kuvada teade „Värskendatud hinnad ja allahindlused sisestati käsitsi või tegemist on välise dokumendiga”.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-109">When you change the shipping date, you might receive a message that states, "Update prices and discounts entered manually or external document."</span></span> <span data-ttu-id="8fbdf-110">Te saate selle teate, kuna lähetuskuupäeva muutmisel võidakse aktiveerida muu kaubanduslepe või müügileping, mis võib hindu muuta.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-110">You receive this message because, if the shipping date is changed, a different trade or sales agreement might be triggered and cause a price change.</span></span> <span data-ttu-id="8fbdf-111">Lähetuskuupäeva muutmine võib mõjutada ka laograafikuid ja muud seotud teavet.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-111">A change to the shipping date can also affect warehouse schedules and other related information.</span></span>

<span data-ttu-id="8fbdf-112">Teade kuvatakse, kui muudetakse mõnda kuupäeva või muud parameetrit.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-112">The message is triggered whenever any of the dates or some other parameters are changed.</span></span> <span data-ttu-id="8fbdf-113">Teate eesmärk on teha kindlaks, et te olete teadlik hinnamuutustest, mis võivad tekkida nende muudatuste tõttu.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-113">The purpose of the message is to make sure that you're aware of price changes that can occur because of those changes.</span></span>

<span data-ttu-id="8fbdf-114">See teade on kaubandusleppe hindamise (TAE) viip.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-114">The message is the trade agreement evaluation (TAE) prompt.</span></span> <span data-ttu-id="8fbdf-115">Täieliku kirjelduse leiate teemast [Kaubandusleppe hindamise poliitika](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).</span><span class="sxs-lookup"><span data-stu-id="8fbdf-115">For a full description, see [Trade agreement evaluation policies](/dynamicsax-2012/appuser-itpro/trade-agreement-evaluation-policies-white-paper).</span></span>

## <a name="a-purchase-order-receipt-doesnt-include-all-charges"></a><span data-ttu-id="8fbdf-116">Ostutellimuse sissetulek ei sisalda kõiki kulusid.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-116">A purchase order receipt doesn't include all charges.</span></span>

### <a name="reproduce-the-issue"></a><span data-ttu-id="8fbdf-117">Probleemi taastekitamine</span><span class="sxs-lookup"><span data-stu-id="8fbdf-117">Reproduce the issue</span></span>

<span data-ttu-id="8fbdf-118">Järgmine protsess näitab üht viisi probleemi taastekitamiseks.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-118">The following procedure shows one way to reproduce the issue.</span></span>

1. <span data-ttu-id="8fbdf-119">Veenduge, et lehe **Hankeparameetrid** vahekaardil **Tarne** oleks suvandi **Loo toote sissetuleku kulud** väärtuseks seatud *Jah*.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-119">On the **Procurement and sourcing parameters** page, on the **Delivery** tab, make sure that the **Generate charges on product receipt** option is set to *Yes*.</span></span>
1. <span data-ttu-id="8fbdf-120">Looge ostutellimus, mis sisaldab kulusid.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-120">Create a purchase order that includes charges.</span></span>
1. <span data-ttu-id="8fbdf-121">Kinnitage ostutellimus.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-121">Confirm the purchase order.</span></span>
1. <span data-ttu-id="8fbdf-122">Võtke ostutellimus vastu.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-122">Receive the purchase order.</span></span>
1. <span data-ttu-id="8fbdf-123">Vaadake sissetuleku kogusummat ja võrrelge seda oodatud kogusummaga.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-123">Look at the receipt total, and compare it to the expected total.</span></span>
1. <span data-ttu-id="8fbdf-124">Pange tähele, et ostutellimuse sissetulek ei sisalda kõiki kulusid.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-124">Notice that not all the charges are included on the purchase order receipt.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8fbdf-125">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="8fbdf-125">Issue resolution</span></span>

<span data-ttu-id="8fbdf-126">Lahendus sõltub sellest, kuidas lisakulud on seadistatud.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-126">The resolution depends on the way that the miscellaneous charges have been set up.</span></span> <span data-ttu-id="8fbdf-127">Teavet lisakulude seadistamise kohta oma vajaduste järgi leiate ajaveebipostitusest [Lisakulude sisestamine toote sissetuleku ajal](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span><span class="sxs-lookup"><span data-stu-id="8fbdf-127">For information about how to set up miscellaneous charges to meet your requirements, see the following blog post: [Post misc. charges at time of product receipt](https://cloudblogs.microsoft.com/dynamics365/no-audience/2014/11/11/post-misc-charges-at-time-of-product-receipt/).</span></span>

## <a name="trade-agreement-prices-and-discounts-arent-applied-on-sales-or-purchase-order-lines-that-are-imported-through-data-management"></a><span data-ttu-id="8fbdf-128">Kaubandusleppe hindu ja allahindlusi ei rakendata müügi- või ostutellimuse ridadel, mis imporditakse andmehalduse kaudu.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-128">Trade agreement prices and discounts aren't applied on sales or purchase order lines that are imported through data management.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8fbdf-129">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="8fbdf-129">Issue description</span></span>

<span data-ttu-id="8fbdf-130">Müügi- või ostutellimuse ridade puhul kohalduvaid kaubandusleppeid ei rakendata ridadel, mis imporditakse andmehalduse kaudu.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-130">Trade agreements that are applicable to sales or purchase order lines aren't applied on lines that are imported through data management.</span></span> <span data-ttu-id="8fbdf-131">Samas rakendatakse samu kaubandusleppeid käsitsi loodud müügi- või ostutellimuse ridadel.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-131">However, the same trade agreements are applied on sales or purchase order lines that are manually created.</span></span>

### <a name="reason-for-the-issue"></a><span data-ttu-id="8fbdf-132">Probleemi põhjus</span><span class="sxs-lookup"><span data-stu-id="8fbdf-132">Reason for the issue</span></span>

<span data-ttu-id="8fbdf-133">Kui andmehalduse kaudu imporditud ostutellimuse read sisaldavad juba hinnateavet, ei hinnata kaubanduslepet nende ridade puhul ümber.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-133">If purchase order lines that are imported via data management already include price information, the trade agreement won't be reevaluated for those lines.</span></span> <span data-ttu-id="8fbdf-134">Näiteks kui rea puhul on seadistatud **Rea allahindluse protsent** või mis tahes hinna ja allahindluse väärtus, siis ei otsita selle rea puhul kaubandusleppeid.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-134">For example, if **Line discount percentage** or any of the price and discount values is set for a line, then trade agreements will not be looked up for that line.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="8fbdf-135">Probleemi lahendus</span><span class="sxs-lookup"><span data-stu-id="8fbdf-135">Issue workaround</span></span>

<span data-ttu-id="8fbdf-136">Selline käitumine on oodatud ja on sarnane nii müügi- kui ka ostutellimuste puhul.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-136">This behavior is expected, and is similar for both sales orders and purchase orders.</span></span>

<span data-ttu-id="8fbdf-137">Lahendusega importige ostutellimuse read ilma hinnateavet määramata.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-137">As a workaround, import the purchase order lines without setting any price information.</span></span> <span data-ttu-id="8fbdf-138">Seejärel rakendatakse kaubandusleppeid ja ostutellimuse read värskendatakse määratletud kaubanduslepete alusel.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-138">The trade agreements will then be applied, and the purchase order lines will be updated based on the defined trade agreements.</span></span>

## <a name="a-vendor-rebate-isnt-cumulated-based-on-invoices"></a><span data-ttu-id="8fbdf-139">Hankija tagasimakset ei kumuleerita arvete põhjal.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-139">A vendor rebate isn't cumulated based on invoices.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8fbdf-140">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="8fbdf-140">Issue description</span></span>

<span data-ttu-id="8fbdf-141">Kui sisestatud arvetel on eri tähtajad, ei kajastu need arved hankija tagasimaksetes, mis on nende põhjal loodud.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-141">If invoices that are posted have different due dates, those invoices aren't reflected in vendor rebates that are generated from them.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8fbdf-142">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="8fbdf-142">Issue resolution</span></span>

<span data-ttu-id="8fbdf-143">See on tahtlik, et hankija tagasimakse arvutamisel ei arvestata tähtaega.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-143">By design, the due date isn't considered when the vendor rebate is calculated.</span></span> <span data-ttu-id="8fbdf-144">Kaaluge süsteemi kohandamist nii, et tähtaeg ja suhe arvega avalduks tegeliku hankija tagasimakse puhul selgemalt.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-144">Consider customizing the system so that the due date and the relation to the invoice are more apparent with respect to the actual vendor rebate.</span></span>

## <a name="unit-prices-on-purchase-orders-arent-calculated-based-on-the-unit-conversion"></a><span data-ttu-id="8fbdf-145">Ostutellimuste ühiku hindasid ei arvutata ühikuteisenduse alusel.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-145">Unit prices on purchase orders aren't calculated based on the unit conversion.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8fbdf-146">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="8fbdf-146">Issue description</span></span>

<span data-ttu-id="8fbdf-147">Kui ostutellimusel muudetakse ühikut, ei arvutata kaubandusleppe hindu ühikuteisenduse määratluste alusel ümber.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-147">When a unit is changed on a purchase order, trade agreement prices aren't recalculated according to unit conversion definitions.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8fbdf-148">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="8fbdf-148">Issue resolution</span></span>

<span data-ttu-id="8fbdf-149">Hinnad võetakse alati kaubanduslepetest (või muudest süsteemis olevatest hinnasätetest, nt müügilepingutest või kauba hindadest) ja need määratakse ühikule.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-149">Prices are always obtained from trade agreements (or other price settings in the system, such as sales agreements or item prices), and they are set for a unit.</span></span>

<span data-ttu-id="8fbdf-150">Kui ühikut tellimuse real muudetakse, otsib süsteem uue ühiku jaoks üles hinna ja rakendab seda hinda.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-150">If the unit is changed on an order line, the system looks for a price for the new unit and applies that price.</span></span> <span data-ttu-id="8fbdf-151">Kui ühiku jaoks ei leita hinda, ei rakenda süsteem hinda.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-151">If no price is found for the unit, the system doesn't apply a price.</span></span> <span data-ttu-id="8fbdf-152">Ühikuteisendust ei saa kasutada hinna ümberarvutamiseks teiseks ühikuks.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-152">The unit conversion can't be used to recalculate the price into another unit.</span></span> <span data-ttu-id="8fbdf-153">Teoreetiliselt ei pruugi ühe kümmet kaupa sisaldava karbi hind võrduda kümne karbi hinnaga.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-153">Theoretically, the price for one box of ten might not equal ten times the price of one box.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="8fbdf-154">Probleemi lahendus</span><span class="sxs-lookup"><span data-stu-id="8fbdf-154">Issue workaround</span></span>

<span data-ttu-id="8fbdf-155">Üks viis selle probleemi lahendamiseks on veenduda, et ühikute jaoks, mida hakatakse kauba puhul tellimuse ridadel kasutama, oleks olemas kaubanduslepped.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-155">One way to work around this issue is to make sure that there are trade agreements for the units that you expect will be used on order lines for the item.</span></span>

## <a name="currency-conversion-issues-occur-with-trade-agreements"></a><span data-ttu-id="8fbdf-156">Kaubanduslepete puhul tekivad valuuta teisenduse probleemid.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-156">Currency conversion issues occur with trade agreements.</span></span>

<span data-ttu-id="8fbdf-157">Kaubandusleppe hindu ei arvutata valuuta põhjal ümber, kui valuuta on ostutellimusel erinev.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-157">Trade agreement prices aren't recalculated according to the currency when the currency differs on a purchase order.</span></span>

<span data-ttu-id="8fbdf-158">Funktsioon *Üldvaluuta* võimaldab teil määratleda hindu ja allahindlusi ainult ühes valuutas.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-158">The *Generic currency* feature lets you define prices and discounts in only one currency.</span></span> <span data-ttu-id="8fbdf-159">Seejärel saate neid vajaduse korral muusse valuutasse teisendada.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-159">You can then convert to other currencies as you require.</span></span> <span data-ttu-id="8fbdf-160">Lisaks saab funktsioon pärast teisenduse lõpetamist automaatselt rakendada nutikat ümardamist.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-160">Furthermore, after the conversion is done, the feature can automatically apply smart rounding.</span></span>

## <a name="when-i-open-the-purchase-agreement-page-in-a-line-view-mode-i-cant-personalize-the-page-by-adding-the-price-unit-field-in-the-overview-of-the-line"></a><span data-ttu-id="8fbdf-161">Kui ma avan lehe „Ostuleping” reavaaterežiimis, ei saa ma lehte isikupärastada välja „Hinnaühik” lisamise kaudu rea ülevaatesse.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-161">When I open the Purchase agreement page in a line view mode, I can't personalize the page by adding the Price unit field in the overview of the line.</span></span>

<span data-ttu-id="8fbdf-162">Mõnda lepperaamistiku jagatud välja ei saa isikupärastamistes kasutada.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-162">Some shared fields in the agreement framework can't be included in personalizations.</span></span> <span data-ttu-id="8fbdf-163">See piirang tuleneb juurutatud andmemudelist.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-163">This limitation occurs because of the data model that is implemented.</span></span> <span data-ttu-id="8fbdf-164">Seetõttu ei saa te välja **Hinnaühik** isikupärastada.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-164">Therefore, you can't personalize the **Price unit** field.</span></span>

## <a name="the-maximum-limit-from-a-purchase-agreement-isnt-effective-on-a-purchase-requisition"></a><span data-ttu-id="8fbdf-165">Ostulepingust pärit ülempiirlepe ei kehti ostutaotluses.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-165">The maximum limit from a purchase agreement isn't effective on a purchase requisition.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8fbdf-166">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="8fbdf-166">Issue description</span></span>

<span data-ttu-id="8fbdf-167">Kui ostutaotlus seotakse ostulepinguga, ei kehti ostutaotluse puhul ostulepingust pärit ülempiir.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-167">When a purchase requisition is linked to a purchase agreement, the maximum limit from the purchase agreement isn't effective on the purchase requisition.</span></span> <span data-ttu-id="8fbdf-168">Vaikehinnateave on õigesti sisestatud, kuid ostutaotluse kaudu saab tellida koguse, mis ületab ostulepingu ülempiiri.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-168">The default price information is correctly entered, but more than the maximum limit from the purchase agreement can be ordered in the purchase requisition.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8fbdf-169">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="8fbdf-169">Issue resolution</span></span>

<span data-ttu-id="8fbdf-170">Selline käitumine on oodatud.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-170">This behavior is expected.</span></span> <span data-ttu-id="8fbdf-171">Kuna taotlusi ei kinnitata alati, ei tohi ostulepingus kogust või summat reserveerida.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-171">Because requisitions aren't always approved, a quantity or amount should not be reserved on the purchase agreement.</span></span> <span data-ttu-id="8fbdf-172">Seetõttu ei saa te kasutada ostulepingu ülempiiri.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-172">Therefore, you won't meet the maximum limit from the purchase agreement.</span></span>

## <a name="trade-agreements-can-be-created-from-rejected-rfqs-therefore-the-system-doesnt-prevent-trade-agreement-journals-from-being-created-if-the-rfq-line-hasnt-been-accepted"></a><span data-ttu-id="8fbdf-173">Kaubandusleppeid saab luua tagasilükatud pakkumiskutsete põhjal.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-173">Trade agreements can be created from rejected RFQs.</span></span> <span data-ttu-id="8fbdf-174">Seetõttu ei takista süsteem kaubandusleppe töölehtede loomist juhul, kui pakkumiskutse rida pole aktsepteeritud.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-174">Therefore, the system doesn't prevent trade agreement journals from being created if the RFQ line hasn't been accepted.</span></span>

<span data-ttu-id="8fbdf-175">Saate luua kaubandusleppeid pakkumiskutsete (RFQ) kõigi vastuste puhul olenemata sellest, kas need on aktsepteeritud või tagasi lükatud.</span><span class="sxs-lookup"><span data-stu-id="8fbdf-175">You can create trade agreements for any replies for a request for quotation (RFQ), regardless of whether they were accepted or rejected.</span></span> <span data-ttu-id="8fbdf-176">Lisateavet leiate teemast [Pakkumiskutsete (RFQ-de) ülevaade](request-quotations.md).</span><span class="sxs-lookup"><span data-stu-id="8fbdf-176">For more information, see [Requests for quotation (RFQs) overview](request-quotations.md).</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]