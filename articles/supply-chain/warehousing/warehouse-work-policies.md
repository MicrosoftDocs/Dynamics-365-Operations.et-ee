---
title: Tööpoliitikad
description: Selles teemas selgitatakse, kuidas seadistada tööpoliitikat.
author: perlynne
manager: tfehr
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 3e7814790bce0aee648421e3a69d702fd0012404
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5248543"
---
# <a name="work-policies"></a><span data-ttu-id="71ff4-103">Tööpoliitikad</span><span class="sxs-lookup"><span data-stu-id="71ff4-103">Work policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="71ff4-104">See teema selgitab, kuidas häälestada süsteemi ja rakenduse ladu, et nad toetaksid tööpoliitikaid.</span><span class="sxs-lookup"><span data-stu-id="71ff4-104">This topic explains how to set up the system and the warehouse app so that they support work policies.</span></span> <span data-ttu-id="71ff4-105">Seda funktsiooni saate kasutada lao kiireks registreerimiseks, loomata ladustamistööd, kui võtate vastu ostu-või üleviimistellimusi või kui lõpetate tootmisprotsesse.</span><span class="sxs-lookup"><span data-stu-id="71ff4-105">You can use this functionality to quickly register inventory without creating putaway work when you receive purchase or transfer orders, or when you complete manufacturing processes.</span></span> <span data-ttu-id="71ff4-106">See teema annab üldteavet.</span><span class="sxs-lookup"><span data-stu-id="71ff4-106">This topic provides general information.</span></span> <span data-ttu-id="71ff4-107">Üksikasjalikku teavet, mis on seotud litsentsiplaadi vastuvõtmisega, leiate teemast [Litsentsiplaadi vastuvõtmine laorakenduse kaudu](warehousing-mobile-device-app-license-plate-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="71ff4-107">For detailed information that is related to license plate receiving, see [License plate receiving via the warehouse app](warehousing-mobile-device-app-license-plate-receiving.md).</span></span>

<span data-ttu-id="71ff4-108">Tööpoliitika kontrollib, kas lao töö on loodud, kui toodetud kaup on lõpetatuks kinnitatud või kui kaubad võetakse vastu lao rakenduse abil.</span><span class="sxs-lookup"><span data-stu-id="71ff4-108">A work policy controls whether warehouse work is created when a manufactured item is reported as finished, or when goods are received by using the warehouse app.</span></span> <span data-ttu-id="71ff4-109">Seadistage iga tööpoliitika, määratledes tingimused, mille puhul see kehtib: töötellimuse tüübid ja protsessid, lao asukoht ja (valikuliselt) tooted.</span><span class="sxs-lookup"><span data-stu-id="71ff4-109">You set up each work policy by defining the conditions where it applies: the work order types and processes, the inventory location, and (optionally) the products.</span></span> <span data-ttu-id="71ff4-110">Näiteks peab toote *A0001* ostutellimuse vastu võtma asukohas *RECV* laos *24*.</span><span class="sxs-lookup"><span data-stu-id="71ff4-110">For example, a purchase order for product *A0001* must be received in location *RECV* in warehouse *24*.</span></span> <span data-ttu-id="71ff4-111">Hiljem tarbitakse toodet teises protsessi asukohas *RECV*.</span><span class="sxs-lookup"><span data-stu-id="71ff4-111">Later, the product is consumed in another process at location *RECV*.</span></span> <span data-ttu-id="71ff4-112">Sellisel juhul saate seadistada tööpoliitika, et vältida ladustatud töö loomist, kui töötaja teatab tootest *A0001*, kui see saabus asukoha *RECV*.</span><span class="sxs-lookup"><span data-stu-id="71ff4-112">In this case, you can set up a work policy to prevent putaway work from being created when a worker reports product *A0001* as received in location *RECV*.</span></span>

> [!NOTE]
> - <span data-ttu-id="71ff4-113">Selleks, et tööpoliitika oleks aktiivne, peate selle määratlema vähemalt ühes asukohas lehe **Tööpoliitikad** FastTab valikus **Lao asukohad**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-113">For a work policy to be active, you must define at least one location for it on the **Inventory locations** FastTab of the **Work policies** page.</span></span> 
> - <span data-ttu-id="71ff4-114">Sama asukohta ei saa määrata mitme tööpoliitika jaoks.</span><span class="sxs-lookup"><span data-stu-id="71ff4-114">You can't specify the same location for multiple work policies.</span></span>
> - <span data-ttu-id="71ff4-115">Mobiilse seadme menüükäskude suvand **Prindi silt** ei prindi tööd loomata litsentsiplaadi silti.</span><span class="sxs-lookup"><span data-stu-id="71ff4-115">The **Print label** option for mobile device menu items won't print a license plate label unless work was created.</span></span>

## <a name="activate-the-features-in-your-system"></a><span data-ttu-id="71ff4-116">Aktiveerige süsteemi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="71ff4-116">Activate the features in your system</span></span>

<span data-ttu-id="71ff4-117">Selleks, et kõik selles teemas kirjeldatud funktsioonid oleksid teie süsteemis saadaval, lülitage sisse järgmised kaks funktsiooni asukohas [Funktsiooni haldus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="71ff4-117">To make all the functionality that is described in this topic available in your system, turn on the following two features in [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):</span></span>

- <span data-ttu-id="71ff4-118">Litsentsiplaadi vastuvõtu täiustused</span><span class="sxs-lookup"><span data-stu-id="71ff4-118">License plate receiving enhancements</span></span>
- <span data-ttu-id="71ff4-119">Sissetuleva töö tööpoliitika täiustused</span><span class="sxs-lookup"><span data-stu-id="71ff4-119">Work policy enhancements for inbound work</span></span>

## <a name="the-work-policies-page"></a><span data-ttu-id="71ff4-120">Tööpoliitikate leht</span><span class="sxs-lookup"><span data-stu-id="71ff4-120">The Work policies page</span></span>

<span data-ttu-id="71ff4-121">Tööpoliitikate seadistamiseks avage **Laohaldus \> Häälestamine \> Töö \> Tööpoliitikad**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-121">To set up work policies, go to **Warehouse management \> Setup \> Work \> Work policies**.</span></span> <span data-ttu-id="71ff4-122">Seejärel seadistage igal FastTab-il väljad, nagu on kirjeldatud järgmistes alamosades.</span><span class="sxs-lookup"><span data-stu-id="71ff4-122">Then, on each FastTab, set the fields as described in the following subsections.</span></span>

### <a name="the-work-order-types-fasttab"></a><span data-ttu-id="71ff4-123">Töötellimuse tüübid FastTab</span><span class="sxs-lookup"><span data-stu-id="71ff4-123">The Work order types FastTab</span></span>

<span data-ttu-id="71ff4-124">**Töötellimuse tüübid** FastTab-is saate lisada kõik töötellimuse tüübid ja sellega seotud tööprotsessid, millele tööpoliitika rakendub.</span><span class="sxs-lookup"><span data-stu-id="71ff4-124">On the **Work order types** FastTab, add all the work order types, and the related work processes, that the work policy applies to.</span></span> <span data-ttu-id="71ff4-125">Tööpoliitikate jaoks toetatakse järgmisi töötellimuse tüüpe ja seotud tööpoliitikaid.</span><span class="sxs-lookup"><span data-stu-id="71ff4-125">The following work order types and related work processes are supported for work policies.</span></span>

| <span data-ttu-id="71ff4-126">Töötellimuse tüüp</span><span class="sxs-lookup"><span data-stu-id="71ff4-126">Work order type</span></span> | <span data-ttu-id="71ff4-127">Tööprotsess</span><span class="sxs-lookup"><span data-stu-id="71ff4-127">Work process</span></span> |
|---|---|
| <span data-ttu-id="71ff4-128">Toormaterjalide komplekteerimine</span><span class="sxs-lookup"><span data-stu-id="71ff4-128">Raw material picking</span></span>| <span data-ttu-id="71ff4-129">Kõik seotud protsessid</span><span class="sxs-lookup"><span data-stu-id="71ff4-129">All related processes</span></span> |
| <span data-ttu-id="71ff4-130">Kaastoodete ja kõrvalsaaduste kõrvalepanek</span><span class="sxs-lookup"><span data-stu-id="71ff4-130">Co-product and by-product put away</span></span> | <span data-ttu-id="71ff4-131">Kõik seotud protsessid</span><span class="sxs-lookup"><span data-stu-id="71ff4-131">All related processes</span></span> |
| <span data-ttu-id="71ff4-132">Lõpetatud kaupade ladustamine</span><span class="sxs-lookup"><span data-stu-id="71ff4-132">Finished goods putaway</span></span> | <span data-ttu-id="71ff4-133">Kõik seotud protsessid</span><span class="sxs-lookup"><span data-stu-id="71ff4-133">All related processes</span></span> |
| <span data-ttu-id="71ff4-134">Üleviimistarne</span><span class="sxs-lookup"><span data-stu-id="71ff4-134">Transfer receipt</span></span> | <span data-ttu-id="71ff4-135">Litsentsiplaadi vastuvõtt (ja kõrvale panemine)</span><span class="sxs-lookup"><span data-stu-id="71ff4-135">License plate receiving (and putaway)</span></span> |
| <span data-ttu-id="71ff4-136">Ostutellimused</span><span class="sxs-lookup"><span data-stu-id="71ff4-136">Purchase orders</span></span> | <ul><li><span data-ttu-id="71ff4-137">Litsentsiplaadi vastuvõtt (ja kõrvale panemine)</span><span class="sxs-lookup"><span data-stu-id="71ff4-137">License plate receiving (and putaway)</span></span></li><li><span data-ttu-id="71ff4-138">Koormas oleva kauba vastuvõtmine (ja kõrvale panemine)</span><span class="sxs-lookup"><span data-stu-id="71ff4-138">Load item receiving (and putaway)</span></span></li><li><span data-ttu-id="71ff4-139">Vastuvõttev ostutellimuse rida (ja kõrvaleseadmine)</span><span class="sxs-lookup"><span data-stu-id="71ff4-139">Purchase order line receiving (and putaway)</span></span></li><li><span data-ttu-id="71ff4-140">Vastuvõttev ostutellimuse üksus (ja kõrvaleseadmine)</span><span class="sxs-lookup"><span data-stu-id="71ff4-140">Purchase order item receiving (and putaway)</span></span></li></ul> |

<span data-ttu-id="71ff4-141">Tööpoliitika seadistamiseks viisil,, et see rakendub mitmele sama töötellimuse tüübi tööprotsessile, lisage iga tööprotsessi jaoks tabelisse eraldi rida.</span><span class="sxs-lookup"><span data-stu-id="71ff4-141">To set up a work policy so that it applies to several work processes of the same work order type, add a separate line for each work process to the grid.</span></span>

<span data-ttu-id="71ff4-142">Määrake iga tabeli rea puhul väli **Töö loomise meetod** ühele järgmistest väärtustest.</span><span class="sxs-lookup"><span data-stu-id="71ff4-142">For each line in the grid, set the **Work creation method** field to one of the following values:</span></span>

- <span data-ttu-id="71ff4-143">**Mitte kunagi** – see väärtus näitab, et tööpoliitika takistab laotöö loomist valitud töötellimuse tüübi ja seotud tööprotsessi jaoks.</span><span class="sxs-lookup"><span data-stu-id="71ff4-143">**Never** – The work policy will prevent warehouse work from being created for the selected work order type and related work process.</span></span>
- <span data-ttu-id="71ff4-144">**Ristlaadimine** — tööpoliitika loob kaudse edasisaatmise töö, kasutades väljal **Ristlaadimise poliitika nimi** valitud poliitikat.</span><span class="sxs-lookup"><span data-stu-id="71ff4-144">**Cross docking** – The work policy will create cross-docking work by using the policy that you select in the **Cross docking policy name** field.</span></span>

### <a name="the-inventory-locations-fasttab"></a><span data-ttu-id="71ff4-145">Varude asukohad FastTab-is</span><span class="sxs-lookup"><span data-stu-id="71ff4-145">The Inventory locations FastTab</span></span>

<span data-ttu-id="71ff4-146">Lisage FastTab **Varude asukohtad** kõik asukohad, kus seda tööpoliitikat rakendada.</span><span class="sxs-lookup"><span data-stu-id="71ff4-146">On the **Inventory locations** FastTab, add all the locations where this work policy should be applied.</span></span> <span data-ttu-id="71ff4-147">Kui tööpoliitikaga ei seostu ühtki asukohta, siis ei rakendu tööpoliitika ühelegi protsessile.</span><span class="sxs-lookup"><span data-stu-id="71ff4-147">If no location is associated with a work policy, the work policy won't be applied to any process.</span></span>

<span data-ttu-id="71ff4-148">Sama asukohta ei saa määrata mitme tööpoliitika jaoks.</span><span class="sxs-lookup"><span data-stu-id="71ff4-148">You can't specify the same location for multiple work policies.</span></span>

<span data-ttu-id="71ff4-149">Asukoha profiilile määratud lao asukohta saate kasutada ka siis, kui funktsioon **Kasuta litsentsiplaadi jälgimist** ei ole sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="71ff4-149">You can use a warehouse location that is assigned to a location profile where the **Use license plate tracking** option is turned off.</span></span> <span data-ttu-id="71ff4-150">Sel juhul registreerivad töötajad otse vaba kaubavaru.</span><span class="sxs-lookup"><span data-stu-id="71ff4-150">In this case, workers will directly register the on-hand inventory.</span></span>

### <a name="the-products-fasttab"></a><span data-ttu-id="71ff4-151">Toodete FastTab</span><span class="sxs-lookup"><span data-stu-id="71ff4-151">The Products FastTab</span></span>

<span data-ttu-id="71ff4-152">Vahekaardil **Tooted** määrake väli **Toote valik** juhtelemendile, mis tooteid poliitika peaks rakendama:</span><span class="sxs-lookup"><span data-stu-id="71ff4-152">On the **Products** tab, set the **Product selection** field to control which products the policy should apply to:</span></span>

- <span data-ttu-id="71ff4-153">**Kõik** — poliitika peaks rakenduma kõikidele toodetele.</span><span class="sxs-lookup"><span data-stu-id="71ff4-153">**All** – The policy should apply to all products.</span></span>
- <span data-ttu-id="71ff4-154">**Valitud** — poliitika peaks rakenduma ainult tabelis loetletud toodetele.</span><span class="sxs-lookup"><span data-stu-id="71ff4-154">**Selected** – The policy should apply only to products that are listed in the grid.</span></span> <span data-ttu-id="71ff4-155">Kasutage **Toodete** FastTab tööriistariba toodete tabelisse lisamiseks või sealt eemaldamiseks.</span><span class="sxs-lookup"><span data-stu-id="71ff4-155">Use the toolbar on the **Products** FastTab to add products to the grid or remove them from the grid.</span></span>

## <a name="default-and-custom-to-locations"></a><span data-ttu-id="71ff4-156">Vaikimisi ja kohandatud "sinna" asukohad</span><span class="sxs-lookup"><span data-stu-id="71ff4-156">Default and custom "to" locations</span></span>

> [!NOTE]
> <span data-ttu-id="71ff4-157">Selles jaotises kirjeldatud funktsioonide kättesaadavaks tegemiseks süsteemis peate sisse lülitama funktsioonid *Litsentsiplaadi täiustuste saamine* ja *Tööpoliitika täiustused sissetuleva töö puhul* asukohas [Funktsioonihaldus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="71ff4-157">To make the functionality that is described in this section available in your system, you must turn on the *License plate receiving enhancements* and *Work policy enhancements for inbound work* features in [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

<span data-ttu-id="71ff4-158">Varem toetas süsteem vastuvõtmist ainult iga lao jaoks eraldi seatud vaikimisi asukohas.</span><span class="sxs-lookup"><span data-stu-id="71ff4-158">Previously, the system supported receiving only at the default location that is defined for each warehouse.</span></span> <span data-ttu-id="71ff4-159">Kuid mobiilse seadme menüüüksused, mis kasutavad järgmisi töö loomise protsesse, pakuvad nüüd suvandit **Vaikeandmete kasutamine**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-159">However, mobile device menu items that use the following work creation processes now provide the **Use default data** option.</span></span> <span data-ttu-id="71ff4-160">See valik võimaldab teil määrata kohandatud asukohta ühele või mitmele menüükäsule.</span><span class="sxs-lookup"><span data-stu-id="71ff4-160">This option lets you assign a custom "to" location to one or more menu items.</span></span> <span data-ttu-id="71ff4-161">(See suvand oli teatud menüükäsu tüüpide jaoks juba saadaval.)</span><span class="sxs-lookup"><span data-stu-id="71ff4-161">(This option was already available for some other types of menu items.)</span></span>

- <span data-ttu-id="71ff4-162">Litsentsiplaadi vastuvõtt (ja kõrvale panemine)</span><span class="sxs-lookup"><span data-stu-id="71ff4-162">License plate receiving (and putaway)</span></span>
- <span data-ttu-id="71ff4-163">Koormas oleva kauba vastuvõtmine (ja kõrvale panemine)</span><span class="sxs-lookup"><span data-stu-id="71ff4-163">Load item receiving (and putaway)</span></span>
- <span data-ttu-id="71ff4-164">Vastuvõttev ostutellimuse rida (ja kõrvaleseadmine)</span><span class="sxs-lookup"><span data-stu-id="71ff4-164">Purchase order line receiving (and putaway)</span></span>
- <span data-ttu-id="71ff4-165">Vastuvõttev ostutellimuse üksus (ja kõrvaleseadmine)</span><span class="sxs-lookup"><span data-stu-id="71ff4-165">Purchase order item receiving (and putaway)</span></span>

<span data-ttu-id="71ff4-166">**Asukoha** menüü-üksuse säte kirjutab üle lao vastuvõtmise vaikeasukohta kõigi tellimuste puhul, mida töödeldakse selle menüükäsu abil.</span><span class="sxs-lookup"><span data-stu-id="71ff4-166">The **To location** setting for a menu item overrides the default receiving location for the warehouse, for all orders that are processed by using that menu item.</span></span>

<span data-ttu-id="71ff4-167">Mobiilse seadme menüü-üksuse seadistamiseks, mis toetab vastuvõtmist kohandatud asukohas, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="71ff4-167">To set up a mobile device menu item to support receiving at a custom location, follow these steps.</span></span>

1. <span data-ttu-id="71ff4-168">Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü-üksused**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-168">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="71ff4-169">Valige või looge menüükäsk, mis kasutab ühte selles jaotises varem loetletud tööloomise protsessidest.</span><span class="sxs-lookup"><span data-stu-id="71ff4-169">Select or create a menu item that uses one of the work creation processes that are listed earlier in this section.</span></span>
1. <span data-ttu-id="71ff4-170">Määrake FastTab-il **Üldine** suvandil **Kasutage vaikeandmed** valikut **Jah**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-170">On the **General** FastTab, set the **Use default data** option to **Yes**.</span></span>
1. <span data-ttu-id="71ff4-171">Valige tegumiribal suvand **Vaikeandmed**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-171">On the Action Pane, select **Default data**.</span></span>
1. <span data-ttu-id="71ff4-172">Määrake lehel **Vaikeandmed** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="71ff4-172">On the **Default data** page, set the following values:</span></span>

    - <span data-ttu-id="71ff4-173">**Vaikimisi andmeväli:** määrake see väli *asukohta*.</span><span class="sxs-lookup"><span data-stu-id="71ff4-173">**Default data field:** Set this field to *To location*.</span></span>
    - <span data-ttu-id="71ff4-174">**Ladu:** valige sihtladu, mida selle menüükäsuga kasutada.</span><span class="sxs-lookup"><span data-stu-id="71ff4-174">**Warehouse:** Select the destination warehouse to use with this menu item.</span></span>
    - <span data-ttu-id="71ff4-175">**Asukoht:** see väli loendab kõik valitud lao jaoks saadaolevad asukoha ID-d.</span><span class="sxs-lookup"><span data-stu-id="71ff4-175">**Location:** This field lists all the location IDs that are available for the selected warehouse.</span></span> <span data-ttu-id="71ff4-176">Kuid selle välja sättel ei ole tegelikult mingit mõju.</span><span class="sxs-lookup"><span data-stu-id="71ff4-176">However, the setting of this field doesn't actually have any effect.</span></span> <span data-ttu-id="71ff4-177">Seetõttu saate selle tühjaks jätta.</span><span class="sxs-lookup"><span data-stu-id="71ff4-177">Therefore, you can leave it blank.</span></span> <span data-ttu-id="71ff4-178">Sellegipoolest saate kasutada loendit, et kinnitada ID, mille peate sisestama väljale **Kindlaksmääratud väärtus**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-178">Nevertheless, you can use the list to confirm the ID that you must enter in the **Hardcoded value** field.</span></span>
    - <span data-ttu-id="71ff4-179">**Kindlaksmääratud väärtus:** sisestage selle menüükäsuga seotud asukoha ID.</span><span class="sxs-lookup"><span data-stu-id="71ff4-179">**Hardcoded value:** Enter the location ID for the receiving location that applies to this menu item.</span></span>

> [!TIP]
> <span data-ttu-id="71ff4-180">Tööpoliitikat saab rakendada ainult siis, kui kõik vastuvõtvad asukohad on loetletud vastavas tööpoliitika sättes.</span><span class="sxs-lookup"><span data-stu-id="71ff4-180">A work policy can be applied only if all the receiving locations are listed in the relevant work policy setup.</span></span> <span data-ttu-id="71ff4-181">See nõue rakendub hoolimata sellest, kas kasutate lao vaikeasukohta või kohandatud asukohta.</span><span class="sxs-lookup"><span data-stu-id="71ff4-181">This requirement applies regardless of whether you're using the default warehouse receiving location or a custom "to" location.</span></span>

## <a name="example-scenario-warehouse-receiving"></a><span data-ttu-id="71ff4-182">Stsenaariumi näide: lao vastuvõtt</span><span class="sxs-lookup"><span data-stu-id="71ff4-182">Example scenario: Warehouse receiving</span></span>

<span data-ttu-id="71ff4-183">Kõik tooted, mis on vastu võetud *Ostutellimuse kauba vastuvõtmisel (ja ladustamisel)*, peavad olema registreeritud asukohas *FL-001* ja need peavad olema saadaval laos *24*.</span><span class="sxs-lookup"><span data-stu-id="71ff4-183">All products that are received by the *Purchase order item receiving (and putaway)* process must be registered in location *FL-001*, and they must be available in warehouse *24*.</span></span> <span data-ttu-id="71ff4-184">Siiski ei tohi tööd luua.</span><span class="sxs-lookup"><span data-stu-id="71ff4-184">However, work should not be created.</span></span> <span data-ttu-id="71ff4-185">Tooted, mis on saadud mis tahes muul viisil (s.h kasutades muid mobiilse seadme menüükäske) tuleks registreerida vaikimisi lao vastuvõtvas asukohas (*RECV*) ja töö tuleb luua nagu tavaliselt.</span><span class="sxs-lookup"><span data-stu-id="71ff4-185">Products that are received by any other process (that is, by using other mobile device menu items) should be registered at the default warehouse receiving location (*RECV*), and work should be created as usual.</span></span> <span data-ttu-id="71ff4-186">(See stsenaarium ei kuva vaikimisi vastuvõtmise häälestust.)</span><span class="sxs-lookup"><span data-stu-id="71ff4-186">(This scenario doesn't show the default receiving setup.)</span></span>

<span data-ttu-id="71ff4-187">See stsenaarium nõuab järgmisi elemente:</span><span class="sxs-lookup"><span data-stu-id="71ff4-187">This scenario requires the following elements:</span></span>

- <span data-ttu-id="71ff4-188">*Ostutellimuse kauba vastuvõtmine (ja kõrvalepanek)* tööpoliitika protsess asukohas *FL-001*, kõikidele toodetele</span><span class="sxs-lookup"><span data-stu-id="71ff4-188">A work policy for the *Purchase order item receiving (and putaway)* process in location *FL-001*, for all products</span></span>
- <span data-ttu-id="71ff4-189">Mobiilse seadme menüükäsk, millel on vaikeandmed ja mis määrab **Välja asukoha** väärtuseks *FL-001*</span><span class="sxs-lookup"><span data-stu-id="71ff4-189">A mobile device menu item that has default data, and that sets the **To location** field to *FL-001*</span></span>

### <a name="prerequisites"></a><span data-ttu-id="71ff4-190">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="71ff4-190">Prerequisites</span></span>

<span data-ttu-id="71ff4-191">Selles stsenaariumis kirjeldatud funktsioonide kättesaadavaks tegemiseks süsteemis peate sisse lülitama funktsioonid *Litsentsiplaadi täiustuste saamine* ja *Tööpoliitika täiustused sissetuleva töö puhul* asukohas [Funktsioonihaldus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="71ff4-191">To make the functionality that is described in this scenario available in your system, you must turn on the *License plate receiving enhancements* and *Work policy enhancements for inbound work* features in [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

<span data-ttu-id="71ff4-192">See stsenaarium kasutab standardseid demoandmeid.</span><span class="sxs-lookup"><span data-stu-id="71ff4-192">This scenario uses the standard demo data.</span></span> <span data-ttu-id="71ff4-193">Niisiis, kui soovite selle läbida siin toodud väärtuseid kasutades, peate kasutama süsteemi, kuhu demoandmed on installitud.</span><span class="sxs-lookup"><span data-stu-id="71ff4-193">Therefore, if you want to work through it by using the values that are provided here, you must work on a system where demo data is installed.</span></span> <span data-ttu-id="71ff4-194">Peate valima ka juriidilise isiku **USMF**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-194">Additionally, you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-work-policy"></a><span data-ttu-id="71ff4-195">Tööpoliitika häälestamine</span><span class="sxs-lookup"><span data-stu-id="71ff4-195">Set up a work policy</span></span>

1. <span data-ttu-id="71ff4-196">Minge asukohta **Laohaldus \> Häälestamine \> Töö \> Tööpoliitikad**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-196">Go to **Warehouse management \> Setup \> Work \> Work policies**.</span></span>
1. <span data-ttu-id="71ff4-197">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-197">Select **New**.</span></span>
1. <span data-ttu-id="71ff4-198">Minge väljal **Tööpoliitika nimi** asukohta *Ostukauba ladustamise töö puudub*.</span><span class="sxs-lookup"><span data-stu-id="71ff4-198">In the **Work policy name** field, enter *No purchase item putaway work*.</span></span>
1. <span data-ttu-id="71ff4-199">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-199">Select **Save**.</span></span>
1. <span data-ttu-id="71ff4-200">**Töötellimuse tüüpide** FastTab-l valige **Lisa**, et lisada tabelisse rida ja seejärel määrake uue rea jaoks järgmised väärtused:</span><span class="sxs-lookup"><span data-stu-id="71ff4-200">On the **Work order types** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="71ff4-201">**Töötellimuse tüüp:** *ostutellimused*</span><span class="sxs-lookup"><span data-stu-id="71ff4-201">**Work order type:** *Purchase orders*</span></span>
    - <span data-ttu-id="71ff4-202">**Tööprotsess:** *vastuvõttev ostutellimuse kaup (ja ladustamine)*</span><span class="sxs-lookup"><span data-stu-id="71ff4-202">**Work process:** *Purchase order item receiving (and putaway)*</span></span>
    - <span data-ttu-id="71ff4-203">**Töö loomise meetod:** *mitte kunagi*</span><span class="sxs-lookup"><span data-stu-id="71ff4-203">**Work creation method:** *Never*</span></span>
    - <span data-ttu-id="71ff4-204">**Ristlaadimise poliitika nimi:** jätke see väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="71ff4-204">**Cross docking policy name:** Leave this field blank.</span></span>

1. <span data-ttu-id="71ff4-205">**Varude asukohtade** FastTab-l valige **Lisa**, et lisada tabelisse rida ja seejärel määrake uue rea jaoks järgmised väärtused:</span><span class="sxs-lookup"><span data-stu-id="71ff4-205">On the **Inventory locations** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="71ff4-206">**Ladu:** *24*</span><span class="sxs-lookup"><span data-stu-id="71ff4-206">**Warehouse:** *24*</span></span>
    - <span data-ttu-id="71ff4-207">**Asukoht:** *FL-001*</span><span class="sxs-lookup"><span data-stu-id="71ff4-207">**Location:** *FL-001*</span></span>

1. <span data-ttu-id="71ff4-208">**Toodete** FastTab-il seadistage välja **Tootevalik** väärtuseks *Kõik*.</span><span class="sxs-lookup"><span data-stu-id="71ff4-208">On the **Products** FastTab, set the **Product selection** field to *All*.</span></span>
1. <span data-ttu-id="71ff4-209">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-209">Select **Save**.</span></span>

### <a name="set-up-a-mobile-device-menu-item-to-change-the-receiving-location"></a><span data-ttu-id="71ff4-210">Mobiilse seadme menüükäsu häälestus kättesaamise asukoha muutmiseks</span><span class="sxs-lookup"><span data-stu-id="71ff4-210">Set up a mobile device menu item to change the receiving location</span></span>

1. <span data-ttu-id="71ff4-211">Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü-üksused**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-211">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="71ff4-212">Vasakpoolsel paanil valige olemasolev **Ostu vastuvõtmise** menüükäsk.</span><span class="sxs-lookup"><span data-stu-id="71ff4-212">In the left pane, select the existing **Purchase receive** menu item.</span></span>
1. <span data-ttu-id="71ff4-213">Määrake FastTab-il **Üldine** suvandil **Kasutage vaikeandmed** valikut *Jah*.</span><span class="sxs-lookup"><span data-stu-id="71ff4-213">On the **General** FastTab, set the **Use default data** option to *Yes*.</span></span>
1. <span data-ttu-id="71ff4-214">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-214">Select **Save**.</span></span>
1. <span data-ttu-id="71ff4-215">Valige tegumiribal suvand **Vaikeandmed**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-215">On the Action Pane, select **Default data**.</span></span>
1. <span data-ttu-id="71ff4-216">**Vaikeandmete** lehel tegevuspaanil valige **Uus**, et lisada tabelisse rida ja seejärel määrake uue rea jaoks järgmised väärtused:</span><span class="sxs-lookup"><span data-stu-id="71ff4-216">On the **Default data** page, on the Action Pane, select **New** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="71ff4-217">**Vaikimisi andmeväli:** *Asukohta*</span><span class="sxs-lookup"><span data-stu-id="71ff4-217">**Default data field:** *To location*</span></span>
    - <span data-ttu-id="71ff4-218">**Ladu:** *24*</span><span class="sxs-lookup"><span data-stu-id="71ff4-218">**Warehouse:** *24*</span></span>
    - <span data-ttu-id="71ff4-219">**Asukoht:** jätke see väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="71ff4-219">**Location:** Leave this field blank.</span></span>
    - <span data-ttu-id="71ff4-220">**Kindlaks määratud väärtus:** *FL-001*</span><span class="sxs-lookup"><span data-stu-id="71ff4-220">**Hardcoded value:** *FL-001*</span></span>

1. <span data-ttu-id="71ff4-221">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-221">Select **Save**.</span></span>

### <a name="receive-a-purchase-order-without-creating-work"></a><span data-ttu-id="71ff4-222">Ostutellimuse vastuvõtmine tööd loomata</span><span class="sxs-lookup"><span data-stu-id="71ff4-222">Receive a purchase order without creating work</span></span>

<span data-ttu-id="71ff4-223">Selles jaotises toodud näites kirjeldatakse, kuidas saada ostutellimuse kaupa, kuid mitte tööd luues asukohas, mis erineb lao jaoks seadistatud vastuvõtmise vaikeasukohast.</span><span class="sxs-lookup"><span data-stu-id="71ff4-223">The example in this section shows how to receive a purchase order item, but without creating work, at a location that differs from the default receiving location that is set up for the warehouse.</span></span> <span data-ttu-id="71ff4-224">Selles näites kasutatakse tööpoliitikat ja mobiilse seadme üksust, mille lõite selle stsenaariumiga varem.</span><span class="sxs-lookup"><span data-stu-id="71ff4-224">This example uses the work policy and mobile device item that you created earlier in this scenario.</span></span>

#### <a name="create-a-purchase-order"></a><span data-ttu-id="71ff4-225">Ostutellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="71ff4-225">Create a purchase order</span></span>

1. <span data-ttu-id="71ff4-226">Avage **Hanked \> Ostutellimused \> Kõik ostutellimused**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-226">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="71ff4-227">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-227">Select **New**.</span></span>
1. <span data-ttu-id="71ff4-228">Dialoogiboksis **Ostutellimuse loomine** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="71ff4-228">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="71ff4-229">**Hankija konto:** *US-101*</span><span class="sxs-lookup"><span data-stu-id="71ff4-229">**Vendor account:** *US-101*</span></span>
    - <span data-ttu-id="71ff4-230">**Tegevuskoht:** *2*</span><span class="sxs-lookup"><span data-stu-id="71ff4-230">**Site:** *2*</span></span>
    - <span data-ttu-id="71ff4-231">**Ladu:** *24*</span><span class="sxs-lookup"><span data-stu-id="71ff4-231">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="71ff4-232">Dialoogiboksi sulgemiseks ja uue müügitellimuse loomiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-232">Select **OK** to close the dialog box and open the new purchase order.</span></span>
1. <span data-ttu-id="71ff4-233">FastTab **Ostutellimuse ridadel** määrake tühjale reale järgmised väärtused:</span><span class="sxs-lookup"><span data-stu-id="71ff4-233">On the **Purchase order lines** FastTab, set the following values for the empty row:</span></span>

    - <span data-ttu-id="71ff4-234">**Kauba kood:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="71ff4-234">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="71ff4-235">**Kogus:** *1*</span><span class="sxs-lookup"><span data-stu-id="71ff4-235">**Quantity:** *1*</span></span>

1. <span data-ttu-id="71ff4-236">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-236">Select **Save**.</span></span>
1. <span data-ttu-id="71ff4-237">Märkige üles ostutellimuse number.</span><span class="sxs-lookup"><span data-stu-id="71ff4-237">Make a note of the purchase order number.</span></span>

#### <a name="receive-a-purchase-order"></a><span data-ttu-id="71ff4-238">Ostutellimuse vastuvõtmine</span><span class="sxs-lookup"><span data-stu-id="71ff4-238">Receive a purchase order</span></span>

1. <span data-ttu-id="71ff4-239">Logige sisse mobiilses seadmes lattu *24* kasutades *24* kasutaja ID-na ja *1* paroolina.</span><span class="sxs-lookup"><span data-stu-id="71ff4-239">On the mobile device, sign in to warehouse *24* by using *24* as the user ID and *1* as the password.</span></span>
1. <span data-ttu-id="71ff4-240">Valige **Sissetulev**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-240">Select **Inbound**.</span></span>
1. <span data-ttu-id="71ff4-241">Valige **Ostu vastuvõtmine**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-241">Select **Purchase receive**.</span></span> <span data-ttu-id="71ff4-242">Välja **Asukoht** väärtuseks peab olema seatud *FL-001*.</span><span class="sxs-lookup"><span data-stu-id="71ff4-242">The **Location** field should be set to *FL-001*.</span></span>
1. <span data-ttu-id="71ff4-243">Sisestage eelmises protseduuris loodud ostutellimuse number.</span><span class="sxs-lookup"><span data-stu-id="71ff4-243">Enter the purchase order number for the purchase order that you created in the previous procedure.</span></span>
1. <span data-ttu-id="71ff4-244">Sisestage väljale **Kauba number** väärtus *A0001*.</span><span class="sxs-lookup"><span data-stu-id="71ff4-244">In the **Item number** field, enter *A0001*.</span></span>
1. <span data-ttu-id="71ff4-245">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-245">Select **OK**.</span></span>
1. <span data-ttu-id="71ff4-246">Sisestage väljale **Kogus** väärtus *1*.</span><span class="sxs-lookup"><span data-stu-id="71ff4-246">In the **Quantity** field, enter *1*.</span></span>
1. <span data-ttu-id="71ff4-247">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-247">Select **OK**.</span></span>

<span data-ttu-id="71ff4-248">Ostutellimus on nüüd vastu võetud, kuid sellega pole seotud ühtegi tööd.</span><span class="sxs-lookup"><span data-stu-id="71ff4-248">The purchase order is now received, but no work is associated with it.</span></span> <span data-ttu-id="71ff4-249">Vaba kaubavaru on värskendatud ja kauba *A0001* kogus *1* on nüüd saadaval asukohas *FL-001*.</span><span class="sxs-lookup"><span data-stu-id="71ff4-249">The on-hand inventory has been updated, and a quantity of *1* of item *A0001* is now available at location *FL-001*.</span></span>

## <a name="example-scenario-manufacturing"></a><span data-ttu-id="71ff4-250">Stsenaariumi näide: tootmine</span><span class="sxs-lookup"><span data-stu-id="71ff4-250">Example scenario: Manufacturing</span></span>

<span data-ttu-id="71ff4-251">Järgmises näites on kaks tootmistellimust: *PRD-001* ja *PRD-002*.</span><span class="sxs-lookup"><span data-stu-id="71ff4-251">In the following example, there are two production orders, *PRD-001* and *PRD-002*.</span></span> <span data-ttu-id="71ff4-252">Tootmistellimusel *PRD-001* on toiming nimega *Assembler*, kus toode *SC1* on teatatud lõpetatuks asukohale *001*.</span><span class="sxs-lookup"><span data-stu-id="71ff4-252">Production order *PRD-001* has an operation that is named *Assembly*, where product *SC1* is being reported as finished to location *001*.</span></span> <span data-ttu-id="71ff4-253">Tootmistellimusel *PRD-002* on toiming nimega *Värvimine* ja tarbib toodet *SC1* asukohast *001*.</span><span class="sxs-lookup"><span data-stu-id="71ff4-253">Production order *PRD-002* has an operation that is named *Painting* and consumes product *SC1* from location *001*.</span></span> <span data-ttu-id="71ff4-254">Tootmistellimus *PRD-002* tarbib ka toormaterjali *RM1* asukohast *001*.</span><span class="sxs-lookup"><span data-stu-id="71ff4-254">Production order *PRD-002* also consumes raw material *RM1* from location *001*.</span></span> <span data-ttu-id="71ff4-255">Toormaterjali *RM1* hoitakse laoasukohas *BULK-001* ja komplekteeritakse asukohale *001* laotööga toormaterjali komplekteerimiseks.</span><span class="sxs-lookup"><span data-stu-id="71ff4-255">Raw material *RM1* is stored in warehouse location *BULK-001* and will be picked to location *001* by warehouse work for raw material picking.</span></span> <span data-ttu-id="71ff4-256">Komplekteerimistöö luuakse tootmise *PRD-002* väljastamisel.</span><span class="sxs-lookup"><span data-stu-id="71ff4-256">The picking work is generated when production *PRD-002* is released.</span></span>

<span data-ttu-id="71ff4-257">[![Lao tööpoliitikad](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span><span class="sxs-lookup"><span data-stu-id="71ff4-257">[![Warehouse work policies](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span></span>

<span data-ttu-id="71ff4-258">Kui plaanite selle stsenaariumi jaoks konfigureerida lao tööpoliitika, peaksite arvestama järgmisi punkte.</span><span class="sxs-lookup"><span data-stu-id="71ff4-258">When you're planning to configure a warehouse work policy for this scenario, you should consider the following points:</span></span>

- <span data-ttu-id="71ff4-259">Laotöö pole lõpetatud kaupade ladustamiseks vajalik, kui teatate toote *SC1* lõpetatuks tootmistellimusest *PRD-001* asukohale *001*.</span><span class="sxs-lookup"><span data-stu-id="71ff4-259">Warehouse work for putaway of finished goods isn't required when you report product *SC1* as finished from production order *PRD-001* to location *001*.</span></span> <span data-ttu-id="71ff4-260">Seda põhjusel, et tootmistellimuse *PRD-002* toiming *Värvimine* tarbib samas asukohas toodet *SC1*.</span><span class="sxs-lookup"><span data-stu-id="71ff4-260">The reason is that the *Painting* operation for production order *PRD-002* consumes product *SC1* at the same location.</span></span>
- <span data-ttu-id="71ff4-261">Laotöö on toormaterjali komplekteerimiseks vajalik, et liigutada toormaterjali *RM1* laoasukohast *BULK-001* asukohta *001*.</span><span class="sxs-lookup"><span data-stu-id="71ff4-261">Warehouse work for raw material picking is required to move raw material *RM1* from warehouse location *BULK-001* to location *001*.</span></span>

<span data-ttu-id="71ff4-262">Siin on näide tööpoliitikast, mida saate nende kaalutluste põhjal seadistada:</span><span class="sxs-lookup"><span data-stu-id="71ff4-262">Here is an example of a work policy that you can set up, based on these considerations:</span></span>

- <span data-ttu-id="71ff4-263">**Tööpoliitika nimi:** *ladustamistööd ei ole*</span><span class="sxs-lookup"><span data-stu-id="71ff4-263">**Work policy name:** *No putaway work*</span></span>
- <span data-ttu-id="71ff4-264">**Töötellimuse tüübid:** *lõpetatud kaupade ladustamine* ja *Kaastoote ja kõrvalsaaduse ladustamine*</span><span class="sxs-lookup"><span data-stu-id="71ff4-264">**Work order types:** *Finished goods put away* and *Co-product and by-product put away*</span></span>
- <span data-ttu-id="71ff4-265">**Varude asukohad:** ladu *51* ja asukoht *001*</span><span class="sxs-lookup"><span data-stu-id="71ff4-265">**Inventory locations:** Warehouse *51* and location *001*</span></span>
- <span data-ttu-id="71ff4-266">**Tooted:** *SC1*</span><span class="sxs-lookup"><span data-stu-id="71ff4-266">**Products:** *SC1*</span></span>

<span data-ttu-id="71ff4-267">Järgmised näidisstsenaariumid annavad etapiviisilise juhise, kuidas seadistada selle stsenaarium jaoks laotöö poliitikat.</span><span class="sxs-lookup"><span data-stu-id="71ff4-267">The following example scenario provides step-by-step instructions for setting up the warehouse work policy for this scenario.</span></span>

## <a name="example-scenario-report-as-finished-to-a-location-that-isnt-license-platecontrolled"></a><span data-ttu-id="71ff4-268">Näidisstsenaarium: teatage tootmistellimus lõpetatuks asukohale, mis pole litsentsiplaadiga kontrollitud</span><span class="sxs-lookup"><span data-stu-id="71ff4-268">Example scenario: Report as finished to a location that isn't license plate–controlled</span></span>

<span data-ttu-id="71ff4-269">See stsenaarium näitab näidet, kus tootmistellimus teatatakse lõpetatuks asukohale, mis pole litsentsiplaadiga kontrollitav.</span><span class="sxs-lookup"><span data-stu-id="71ff4-269">This scenario shows an example where a production order is reported as finished to a location that isn't license plate–controlled.</span></span>

<span data-ttu-id="71ff4-270">See stsenaarium kasutab standardseid demoandmeid.</span><span class="sxs-lookup"><span data-stu-id="71ff4-270">This scenario uses the standard demo data.</span></span> <span data-ttu-id="71ff4-271">Niisiis, kui soovite selle läbida siin toodud väärtuseid kasutades, peate kasutama süsteemi, kuhu demoandmed on installitud.</span><span class="sxs-lookup"><span data-stu-id="71ff4-271">Therefore, if you want to work through it by using the values that are provided here, you must work on a system where demo data is installed.</span></span> <span data-ttu-id="71ff4-272">Peate valima ka juriidilise isiku **USMF**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-272">Additionally, you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-warehouse-work-policy"></a><span data-ttu-id="71ff4-273">Lao tööpoliitika seadistamine</span><span class="sxs-lookup"><span data-stu-id="71ff4-273">Set up a warehouse work policy</span></span>

<span data-ttu-id="71ff4-274">Laotoimingud ei hõlma alati laotööd.</span><span class="sxs-lookup"><span data-stu-id="71ff4-274">Warehouse processes don't always include warehouse work.</span></span> <span data-ttu-id="71ff4-275">Tööpoliitika määratlemisel saate vältida töö loomist toormaterjali komplekteerimise puhul ja lõpetatud kaupade ladustamist toodete kogumi puhul kindlates asukohtades.</span><span class="sxs-lookup"><span data-stu-id="71ff4-275">By defining a work policy, you can prevent the creation of work for raw material picking and putaway of finished goods for a set of products at specific locations.</span></span>

1. <span data-ttu-id="71ff4-276">Minge asukohta **Laohaldus \> Häälestamine \> Töö \> Tööpoliitikad**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-276">Go to **Warehouse management \> Setup \> Work \> Work policies**.</span></span>
1. <span data-ttu-id="71ff4-277">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-277">Select **New**.</span></span>
1. <span data-ttu-id="71ff4-278">Minge väljal **Tööpoliitika nimi** asukohta *Ladustamistöö puudub*.</span><span class="sxs-lookup"><span data-stu-id="71ff4-278">In the **Work policy name** field, enter *No putaway work*.</span></span>
1. <span data-ttu-id="71ff4-279">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-279">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="71ff4-280">**Töötellimuse tüüpide** FastTab-l valige **Lisa**, et lisada tabelisse rida ja seejärel määrake uue rea jaoks järgmised väärtused:</span><span class="sxs-lookup"><span data-stu-id="71ff4-280">On the **Work order types** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="71ff4-281">**Töötellimuse tüüp:** *lõpetatud kaupade ladustamine*</span><span class="sxs-lookup"><span data-stu-id="71ff4-281">**Work order type:** *Finished goods put away*</span></span>
    - <span data-ttu-id="71ff4-282">**Tööprotsess:** *kõik seotud tööprotsessid*</span><span class="sxs-lookup"><span data-stu-id="71ff4-282">**Work process:** *All related work processes*</span></span>
    - <span data-ttu-id="71ff4-283">**Töö loomise meetod:** *mitte kunagi*</span><span class="sxs-lookup"><span data-stu-id="71ff4-283">**Work creation method:** *Never*</span></span>
    - <span data-ttu-id="71ff4-284">**Ristlaadimise poliitika nimi:** jätke see väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="71ff4-284">**Cross docking policy name:** Leave this field blank.</span></span>

1. <span data-ttu-id="71ff4-285">Valige **Lisa** uuesti, et lisada tabelisse teine rida ja seejärel määrake uue rea jaoks järgmised väärtused:</span><span class="sxs-lookup"><span data-stu-id="71ff4-285">Select **Add** again to add a second row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="71ff4-286">**Töötellimuse tüüp:** *kaastoodete ja kõrvalsaaduste ladustamine*</span><span class="sxs-lookup"><span data-stu-id="71ff4-286">**Work order type:** *Co-product and by-product put away*</span></span>
    - <span data-ttu-id="71ff4-287">**Tööprotsess:** *kõik seotud tööprotsessid*</span><span class="sxs-lookup"><span data-stu-id="71ff4-287">**Work process:** *All related work processes*</span></span>
    - <span data-ttu-id="71ff4-288">**Töö loomise meetod:** *mitte kunagi*</span><span class="sxs-lookup"><span data-stu-id="71ff4-288">**Work creation method:** *Never*</span></span>
    - <span data-ttu-id="71ff4-289">**Ristlaadimise poliitika nimi:** jätke see väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="71ff4-289">**Cross docking policy name:** Leave this field blank.</span></span>

1. <span data-ttu-id="71ff4-290">**Varude asukohtade** FastTab-l valige **Lisa**, et lisada tabelisse rida ja seejärel määrake uue rea jaoks järgmised väärtused:</span><span class="sxs-lookup"><span data-stu-id="71ff4-290">On the **Inventory locations** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="71ff4-291">**Ladu:** *51*</span><span class="sxs-lookup"><span data-stu-id="71ff4-291">**Warehouse:** *51*</span></span>
    - <span data-ttu-id="71ff4-292">**Asukoht:** *001*</span><span class="sxs-lookup"><span data-stu-id="71ff4-292">**Location:** *001*</span></span>

1. <span data-ttu-id="71ff4-293">**Toodete** FastTab-il seadistage välja **Tootevalik** väärtuseks *Valitud*.</span><span class="sxs-lookup"><span data-stu-id="71ff4-293">On the **Products** FastTab, set the **Product selection** field to *Selected*.</span></span>
1. <span data-ttu-id="71ff4-294">FastTab-il **Tooted** valige käsk **Lisa**, et lisada uus rida tabelisse.</span><span class="sxs-lookup"><span data-stu-id="71ff4-294">On the **Products** FastTab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="71ff4-295">Uues reas määrake välja **Kauba number** väärtuseks *L0101*.</span><span class="sxs-lookup"><span data-stu-id="71ff4-295">In the new row, set the **Item number** field to *L0101*.</span></span>
1. <span data-ttu-id="71ff4-296">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-296">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-an-output-location"></a><span data-ttu-id="71ff4-297">Väljundi asukoha seadistamine</span><span class="sxs-lookup"><span data-stu-id="71ff4-297">Set up an output location</span></span>

1. <span data-ttu-id="71ff4-298">Avage **Organisatsiooni haldus \> Ressursid \> Ressursigrupid**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-298">Go to **Organization administration \> Resources \> Resource groups**.</span></span>
1. <span data-ttu-id="71ff4-299">Valige vasakult paneelist ressursigrupp **5102**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-299">In the left pane, select resource group **5102**.</span></span>
1. <span data-ttu-id="71ff4-300">Määrake kiirkaardil **Üldine** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="71ff4-300">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="71ff4-301">**Väljastusladu:** *51*</span><span class="sxs-lookup"><span data-stu-id="71ff4-301">**Output warehouse:** *51*</span></span>
    - <span data-ttu-id="71ff4-302">**Väljastuskoht:** *001*</span><span class="sxs-lookup"><span data-stu-id="71ff4-302">**Output location:** *001*</span></span>

1. <span data-ttu-id="71ff4-303">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-303">On the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="71ff4-304">Asukoht *001* pole litsentsiplaadiga juhitav asukoht.</span><span class="sxs-lookup"><span data-stu-id="71ff4-304">Location *001* isn't a license plate–controlled location.</span></span> <span data-ttu-id="71ff4-305">Saate seadistada väljundi, mis pole litsentsiplaadiga juhitav, asukoha ainult siis, kui asukohale on olemas vastav tööpoliitika.</span><span class="sxs-lookup"><span data-stu-id="71ff4-305">You can set up an output location that isn't license plate–controlled only if an applicable work policy exists for the location.</span></span>

### <a name="create-a-production-order-and-report-it-as-finished"></a><span data-ttu-id="71ff4-306">Tootmistellimuse loomine ja selle lõpetatuna kinnitamine</span><span class="sxs-lookup"><span data-stu-id="71ff4-306">Create a production order and report it as finished</span></span>

1. <span data-ttu-id="71ff4-307">Avage **Tootmise juhtimine \> Tootmistellimused \> Kõik tootmistellimused**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-307">Go to **Production control \> Production orders \> All production orders**.</span></span>
1. <span data-ttu-id="71ff4-308">Toimingupaanil valige **Uus tootmistellimus**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-308">On the Action Pane, select **New production order**.</span></span>
1. <span data-ttu-id="71ff4-309">Seadistage dialoogiaknas **Loo tootmistellimus** välja **Kauba number** väärtuseks *L0101*.</span><span class="sxs-lookup"><span data-stu-id="71ff4-309">In the **Create production order** dialog box, set the **Item number** field to *L0101*.</span></span>
1. <span data-ttu-id="71ff4-310">Valige tellimuse loomiseks ja dialoogiboksi sulgemiseks **Loo**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-310">Select **Create** to create the order and close the dialog box.</span></span>

    <span data-ttu-id="71ff4-311">**Kõik tootmistellimused** lehe tabelisse lisatakse uus tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="71ff4-311">A new production order is added to the grid on the **All production orders** page.</span></span>

    <span data-ttu-id="71ff4-312">Hoidke uus tootmistellimus valituna.</span><span class="sxs-lookup"><span data-stu-id="71ff4-312">Keep the new production order selected.</span></span>

1. <span data-ttu-id="71ff4-313">Tehke tegumiriba vahekaardil **Tootmistellimus** grupis **Protsess** valik **Hinda**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-313">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Estimate**.</span></span>
1. <span data-ttu-id="71ff4-314">Dialoogiaknas **Hinda** lugege hinnangut ja seejärel klõpsake nuppu **OK**, et sulgeda dialoogiaken.</span><span class="sxs-lookup"><span data-stu-id="71ff4-314">In the **Estimate** dialog box, read the estimate, and then select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="71ff4-315">Tehke tegumiriba vahekaardil **Tootmistellimus** grupis **Protsess** valik **Alusta**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-315">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Start**.</span></span>
1. <span data-ttu-id="71ff4-316">Seadke dialoogiaknas **Alusta** vahekaardil **Üldine** väli **Automaatne BOM-tarbimine** väärtuseks *Mitte kunagi*.</span><span class="sxs-lookup"><span data-stu-id="71ff4-316">In the **Start** dialog box, on the **General** tab, set the **Automatic BOM consumption** field to *Never*.</span></span>
1. <span data-ttu-id="71ff4-317">Valige **OK**, et salvestada oma säte ja sulgeda dialoogiaken.</span><span class="sxs-lookup"><span data-stu-id="71ff4-317">Select **OK** to save your setting and close the dialog box.</span></span>
1. <span data-ttu-id="71ff4-318">Tehke tegumiriba vahekaardil **Tootmistellimus** grupis **Protsess** valik **Kinnita lõpetatuks**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-318">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Report as finished**.</span></span>
1. <span data-ttu-id="71ff4-319">Dialoogiaknas **Lõpetatuks kinnitamine** vahekaardil **Üldine** määrake suvandi **Kinnita tõrge** väärtuseks *Jah*.</span><span class="sxs-lookup"><span data-stu-id="71ff4-319">In the **Report as finished** dialog box, on the **General** tab, set the **Accept error** option to *Yes*.</span></span>
1. <span data-ttu-id="71ff4-320">Valige **OK**, et salvestada oma säte ja sulgeda dialoogiaken.</span><span class="sxs-lookup"><span data-stu-id="71ff4-320">Select **OK** to save your setting and close the dialog box.</span></span>
1. <span data-ttu-id="71ff4-321">Valige toimingupaani vahekaardil **Ladu** grupis **Seotud teave** üksus **Töö üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="71ff4-321">On the Action Pane, on the **Warehouse** tab, in the **General** group, select **Work details**.</span></span>

<span data-ttu-id="71ff4-322">Kui tootmistellimus on lõpetatuks kuulutatud, pole ladustamiseks tööd loodud.</span><span class="sxs-lookup"><span data-stu-id="71ff4-322">When the production order is reported as finished, no work is generated for putaway.</span></span> <span data-ttu-id="71ff4-323">Seda käitumist ilmneb, kuna määratletud on tööpoliitika, mis takistab töö loomist, kui toode *L0101* kuulutatakse lõpetatuks asukohale *001*.</span><span class="sxs-lookup"><span data-stu-id="71ff4-323">This behavior occurs because a work policy is defined that prevents work from being generated when product *L0101* is reported as finished to location *001*.</span></span>

## <a name="more-information"></a><span data-ttu-id="71ff4-324">Lisateave</span><span class="sxs-lookup"><span data-stu-id="71ff4-324">More information</span></span>

<span data-ttu-id="71ff4-325">Lisateavet mobiilse seadme menüü üksuste kohta vt teemast [Mobiilsete seadmete seadistamine laotöö jaoks](configure-mobile-devices-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="71ff4-325">For more information about mobile device menu items, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>

<span data-ttu-id="71ff4-326">Lisateavet, mis on seotud litsentsiplaadi vastuvõtmisega ja tööpoliitikatega, leiate teemast [Litsentsiplaadi vastuvõtmine laorakenduse kaudu](warehousing-mobile-device-app-license-plate-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="71ff4-326">For more information about license plate receiving and work policies, see [License plate receiving via the warehouse app](warehousing-mobile-device-app-license-plate-receiving.md).</span></span>

<span data-ttu-id="71ff4-327">Lisateavet sissetuleva koormuse halduse kohta vt teemast [Ostutellimuste sissetulevate koormate laohaldus](inbound-load-handling.md).</span><span class="sxs-lookup"><span data-stu-id="71ff4-327">For more information about inbound load management, see [Warehouse handling of inbound loads for purchase orders](inbound-load-handling.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]