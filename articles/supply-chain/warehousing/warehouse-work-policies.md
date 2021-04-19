---
title: Tööpoliitikad
description: Selles teemas selgitatakse, kuidas seadistada tööpoliitikat.
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 39a9ba00763fac220eff16bdd42aa07cc8e35ba4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838126"
---
# <a name="work-policies"></a><span data-ttu-id="194d2-103">Tööpoliitikad</span><span class="sxs-lookup"><span data-stu-id="194d2-103">Work policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="194d2-104">See teema selgitab, kuidas häälestada süsteemi ja mobiilirakendust Warehouse Management, et nad toetaksid tööpoliitikaid.</span><span class="sxs-lookup"><span data-stu-id="194d2-104">This topic explains how to set up the system and the Warehouse Management mobile app so that they support work policies.</span></span> <span data-ttu-id="194d2-105">Seda funktsiooni saate kasutada lao kiireks registreerimiseks, loomata ladustamistööd, kui võtate vastu ostu-või üleviimistellimusi või kui lõpetate tootmisprotsesse.</span><span class="sxs-lookup"><span data-stu-id="194d2-105">You can use this functionality to quickly register inventory without creating putaway work when you receive purchase or transfer orders, or when you complete manufacturing processes.</span></span> <span data-ttu-id="194d2-106">See teema annab üldteavet.</span><span class="sxs-lookup"><span data-stu-id="194d2-106">This topic provides general information.</span></span> <span data-ttu-id="194d2-107">Üksikasjalikku teavet, mis on seotud litsentsiplaadi vastuvõtmisega, leiate teemast [Litsentsiplaadi vastuvõtmine mobiilirakenduse Warehouse Management kaudu](warehousing-mobile-device-app-license-plate-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="194d2-107">For detailed information that is related to license plate receiving, see [License plate receiving via the Warehouse Management mobile app](warehousing-mobile-device-app-license-plate-receiving.md).</span></span>

<span data-ttu-id="194d2-108">Tööpoliitika kontrollib, kas lao töö on loodud, kui toodetud kaup on lõpetatuks kinnitatud või kui kaubad võetakse vastu lao mobiilirakenduse Warehouse Management abil.</span><span class="sxs-lookup"><span data-stu-id="194d2-108">A work policy controls whether warehouse work is created when a manufactured item is reported as finished, or when goods are received by using the Warehouse Management mobile app.</span></span> <span data-ttu-id="194d2-109">Seadistage iga tööpoliitika, määratledes tingimused, mille puhul see kehtib: töötellimuse tüübid ja protsessid, lao asukoht ja (valikuliselt) tooted.</span><span class="sxs-lookup"><span data-stu-id="194d2-109">You set up each work policy by defining the conditions where it applies: the work order types and processes, the inventory location, and (optionally) the products.</span></span> <span data-ttu-id="194d2-110">Näiteks peab toote *A0001* ostutellimuse vastu võtma asukohas *RECV* laos *24*.</span><span class="sxs-lookup"><span data-stu-id="194d2-110">For example, a purchase order for product *A0001* must be received in location *RECV* in warehouse *24*.</span></span> <span data-ttu-id="194d2-111">Hiljem tarbitakse toodet teises protsessi asukohas *RECV*.</span><span class="sxs-lookup"><span data-stu-id="194d2-111">Later, the product is consumed in another process at location *RECV*.</span></span> <span data-ttu-id="194d2-112">Sellisel juhul saate seadistada tööpoliitika, et vältida ladustatud töö loomist, kui töötaja teatab tootest *A0001*, kui see saabus asukoha *RECV*.</span><span class="sxs-lookup"><span data-stu-id="194d2-112">In this case, you can set up a work policy to prevent putaway work from being created when a worker reports product *A0001* as received in location *RECV*.</span></span>

> [!NOTE]
> - <span data-ttu-id="194d2-113">Selleks, et tööpoliitika oleks aktiivne, peate selle määratlema vähemalt ühes asukohas lehe **Tööpoliitikad** FastTab valikus **Lao asukohad**.</span><span class="sxs-lookup"><span data-stu-id="194d2-113">For a work policy to be active, you must define at least one location for it on the **Inventory locations** FastTab of the **Work policies** page.</span></span> 
> - <span data-ttu-id="194d2-114">Sama asukohta ei saa määrata mitme tööpoliitika jaoks.</span><span class="sxs-lookup"><span data-stu-id="194d2-114">You can't specify the same location for multiple work policies.</span></span>
> - <span data-ttu-id="194d2-115">Mobiilse seadme menüükäskude suvand **Prindi silt** ei prindi tööd loomata litsentsiplaadi silti.</span><span class="sxs-lookup"><span data-stu-id="194d2-115">The **Print label** option for mobile device menu items won't print a license plate label unless work was created.</span></span>

## <a name="activate-the-features-in-your-system"></a><span data-ttu-id="194d2-116">Aktiveerige süsteemi funktsioonid</span><span class="sxs-lookup"><span data-stu-id="194d2-116">Activate the features in your system</span></span>

<span data-ttu-id="194d2-117">Selleks, et kõik selles teemas kirjeldatud funktsioonid oleksid teie süsteemis saadaval, lülitage sisse järgmised kaks funktsiooni asukohas [Funktsiooni haldus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="194d2-117">To make all the functionality that is described in this topic available in your system, turn on the following two features in [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):</span></span>

- <span data-ttu-id="194d2-118">Litsentsiplaadi vastuvõtu täiustused</span><span class="sxs-lookup"><span data-stu-id="194d2-118">License plate receiving enhancements</span></span>
- <span data-ttu-id="194d2-119">Sissetuleva töö tööpoliitika täiustused</span><span class="sxs-lookup"><span data-stu-id="194d2-119">Work policy enhancements for inbound work</span></span>

## <a name="the-work-policies-page"></a><span data-ttu-id="194d2-120">Tööpoliitikate leht</span><span class="sxs-lookup"><span data-stu-id="194d2-120">The Work policies page</span></span>

<span data-ttu-id="194d2-121">Tööpoliitikate seadistamiseks avage **Laohaldus \> Häälestamine \> Töö \> Tööpoliitikad**.</span><span class="sxs-lookup"><span data-stu-id="194d2-121">To set up work policies, go to **Warehouse management \> Setup \> Work \> Work policies**.</span></span> <span data-ttu-id="194d2-122">Seejärel seadistage igal FastTab-il väljad, nagu on kirjeldatud järgmistes alamosades.</span><span class="sxs-lookup"><span data-stu-id="194d2-122">Then, on each FastTab, set the fields as described in the following subsections.</span></span>

### <a name="the-work-order-types-fasttab"></a><span data-ttu-id="194d2-123">Töötellimuse tüübid FastTab</span><span class="sxs-lookup"><span data-stu-id="194d2-123">The Work order types FastTab</span></span>

<span data-ttu-id="194d2-124">**Töötellimuse tüübid** FastTab-is saate lisada kõik töötellimuse tüübid ja sellega seotud tööprotsessid, millele tööpoliitika rakendub.</span><span class="sxs-lookup"><span data-stu-id="194d2-124">On the **Work order types** FastTab, add all the work order types, and the related work processes, that the work policy applies to.</span></span> <span data-ttu-id="194d2-125">Tööpoliitikate jaoks toetatakse järgmisi töötellimuse tüüpe ja seotud tööpoliitikaid.</span><span class="sxs-lookup"><span data-stu-id="194d2-125">The following work order types and related work processes are supported for work policies.</span></span>

| <span data-ttu-id="194d2-126">Töötellimuse tüüp</span><span class="sxs-lookup"><span data-stu-id="194d2-126">Work order type</span></span> | <span data-ttu-id="194d2-127">Tööprotsess</span><span class="sxs-lookup"><span data-stu-id="194d2-127">Work process</span></span> |
|---|---|
| <span data-ttu-id="194d2-128">Toormaterjalide komplekteerimine</span><span class="sxs-lookup"><span data-stu-id="194d2-128">Raw material picking</span></span>| <span data-ttu-id="194d2-129">Kõik seotud protsessid</span><span class="sxs-lookup"><span data-stu-id="194d2-129">All related processes</span></span> |
| <span data-ttu-id="194d2-130">Kaastoodete ja kõrvalsaaduste kõrvalepanek</span><span class="sxs-lookup"><span data-stu-id="194d2-130">Co-product and by-product put away</span></span> | <span data-ttu-id="194d2-131">Kõik seotud protsessid</span><span class="sxs-lookup"><span data-stu-id="194d2-131">All related processes</span></span> |
| <span data-ttu-id="194d2-132">Lõpetatud kaupade ladustamine</span><span class="sxs-lookup"><span data-stu-id="194d2-132">Finished goods putaway</span></span> | <span data-ttu-id="194d2-133">Kõik seotud protsessid</span><span class="sxs-lookup"><span data-stu-id="194d2-133">All related processes</span></span> |
| <span data-ttu-id="194d2-134">Üleviimistarne</span><span class="sxs-lookup"><span data-stu-id="194d2-134">Transfer receipt</span></span> | <span data-ttu-id="194d2-135">Litsentsiplaadi vastuvõtt (ja kõrvale panemine)</span><span class="sxs-lookup"><span data-stu-id="194d2-135">License plate receiving (and putaway)</span></span> |
| <span data-ttu-id="194d2-136">Ostutellimused</span><span class="sxs-lookup"><span data-stu-id="194d2-136">Purchase orders</span></span> | <ul><li><span data-ttu-id="194d2-137">Litsentsiplaadi vastuvõtt (ja kõrvale panemine)</span><span class="sxs-lookup"><span data-stu-id="194d2-137">License plate receiving (and putaway)</span></span></li><li><span data-ttu-id="194d2-138">Koormas oleva kauba vastuvõtmine (ja kõrvale panemine)</span><span class="sxs-lookup"><span data-stu-id="194d2-138">Load item receiving (and putaway)</span></span></li><li><span data-ttu-id="194d2-139">Vastuvõttev ostutellimuse rida (ja kõrvaleseadmine)</span><span class="sxs-lookup"><span data-stu-id="194d2-139">Purchase order line receiving (and putaway)</span></span></li><li><span data-ttu-id="194d2-140">Vastuvõttev ostutellimuse üksus (ja kõrvaleseadmine)</span><span class="sxs-lookup"><span data-stu-id="194d2-140">Purchase order item receiving (and putaway)</span></span></li></ul> |

<span data-ttu-id="194d2-141">Tööpoliitika seadistamiseks viisil,, et see rakendub mitmele sama töötellimuse tüübi tööprotsessile, lisage iga tööprotsessi jaoks tabelisse eraldi rida.</span><span class="sxs-lookup"><span data-stu-id="194d2-141">To set up a work policy so that it applies to several work processes of the same work order type, add a separate line for each work process to the grid.</span></span>

<span data-ttu-id="194d2-142">Määrake iga tabeli rea puhul väli **Töö loomise meetod** ühele järgmistest väärtustest.</span><span class="sxs-lookup"><span data-stu-id="194d2-142">For each line in the grid, set the **Work creation method** field to one of the following values:</span></span>

- <span data-ttu-id="194d2-143">**Mitte kunagi** – see väärtus näitab, et tööpoliitika takistab laotöö loomist valitud töötellimuse tüübi ja seotud tööprotsessi jaoks.</span><span class="sxs-lookup"><span data-stu-id="194d2-143">**Never** – The work policy will prevent warehouse work from being created for the selected work order type and related work process.</span></span>
- <span data-ttu-id="194d2-144">**Ristlaadimine** — tööpoliitika loob kaudse edasisaatmise töö, kasutades väljal **Ristlaadimise poliitika nimi** valitud poliitikat.</span><span class="sxs-lookup"><span data-stu-id="194d2-144">**Cross docking** – The work policy will create cross-docking work by using the policy that you select in the **Cross docking policy name** field.</span></span>

### <a name="the-inventory-locations-fasttab"></a><span data-ttu-id="194d2-145">Varude asukohad FastTab-is</span><span class="sxs-lookup"><span data-stu-id="194d2-145">The Inventory locations FastTab</span></span>

<span data-ttu-id="194d2-146">Lisage FastTab **Varude asukohtad** kõik asukohad, kus seda tööpoliitikat rakendada.</span><span class="sxs-lookup"><span data-stu-id="194d2-146">On the **Inventory locations** FastTab, add all the locations where this work policy should be applied.</span></span> <span data-ttu-id="194d2-147">Kui tööpoliitikaga ei seostu ühtki asukohta, siis ei rakendu tööpoliitika ühelegi protsessile.</span><span class="sxs-lookup"><span data-stu-id="194d2-147">If no location is associated with a work policy, the work policy won't be applied to any process.</span></span>

<span data-ttu-id="194d2-148">Sama asukohta ei saa määrata mitme tööpoliitika jaoks.</span><span class="sxs-lookup"><span data-stu-id="194d2-148">You can't specify the same location for multiple work policies.</span></span>

<span data-ttu-id="194d2-149">Asukoha profiilile määratud lao asukohta saate kasutada ka siis, kui funktsioon **Kasuta litsentsiplaadi jälgimist** ei ole sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="194d2-149">You can use a warehouse location that is assigned to a location profile where the **Use license plate tracking** option is turned off.</span></span> <span data-ttu-id="194d2-150">Sel juhul registreerivad töötajad otse vaba kaubavaru.</span><span class="sxs-lookup"><span data-stu-id="194d2-150">In this case, workers will directly register the on-hand inventory.</span></span>

### <a name="the-products-fasttab"></a><span data-ttu-id="194d2-151">Toodete FastTab</span><span class="sxs-lookup"><span data-stu-id="194d2-151">The Products FastTab</span></span>

<span data-ttu-id="194d2-152">Vahekaardil **Tooted** määrake väli **Toote valik** juhtelemendile, mis tooteid poliitika peaks rakendama:</span><span class="sxs-lookup"><span data-stu-id="194d2-152">On the **Products** tab, set the **Product selection** field to control which products the policy should apply to:</span></span>

- <span data-ttu-id="194d2-153">**Kõik** — poliitika peaks rakenduma kõikidele toodetele.</span><span class="sxs-lookup"><span data-stu-id="194d2-153">**All** – The policy should apply to all products.</span></span>
- <span data-ttu-id="194d2-154">**Valitud** — poliitika peaks rakenduma ainult tabelis loetletud toodetele.</span><span class="sxs-lookup"><span data-stu-id="194d2-154">**Selected** – The policy should apply only to products that are listed in the grid.</span></span> <span data-ttu-id="194d2-155">Kasutage **Toodete** FastTab tööriistariba toodete tabelisse lisamiseks või sealt eemaldamiseks.</span><span class="sxs-lookup"><span data-stu-id="194d2-155">Use the toolbar on the **Products** FastTab to add products to the grid or remove them from the grid.</span></span>

## <a name="default-and-custom-to-locations"></a><span data-ttu-id="194d2-156">Vaikimisi ja kohandatud "sinna" asukohad</span><span class="sxs-lookup"><span data-stu-id="194d2-156">Default and custom "to" locations</span></span>

> [!NOTE]
> <span data-ttu-id="194d2-157">Selles jaotises kirjeldatud funktsioonide kättesaadavaks tegemiseks süsteemis peate sisse lülitama funktsioonid *Litsentsiplaadi täiustuste saamine* ja *Tööpoliitika täiustused sissetuleva töö puhul* asukohas [Funktsioonihaldus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="194d2-157">To make the functionality that is described in this section available in your system, you must turn on the *License plate receiving enhancements* and *Work policy enhancements for inbound work* features in [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

<span data-ttu-id="194d2-158">Varem toetas süsteem vastuvõtmist ainult iga lao jaoks eraldi seatud vaikimisi asukohas.</span><span class="sxs-lookup"><span data-stu-id="194d2-158">Previously, the system supported receiving only at the default location that is defined for each warehouse.</span></span> <span data-ttu-id="194d2-159">Kuid mobiilse seadme menüüüksused, mis kasutavad järgmisi töö loomise protsesse, pakuvad nüüd suvandit **Vaikeandmete kasutamine**.</span><span class="sxs-lookup"><span data-stu-id="194d2-159">However, mobile device menu items that use the following work creation processes now provide the **Use default data** option.</span></span> <span data-ttu-id="194d2-160">See valik võimaldab teil määrata kohandatud asukohta ühele või mitmele menüükäsule.</span><span class="sxs-lookup"><span data-stu-id="194d2-160">This option lets you assign a custom "to" location to one or more menu items.</span></span> <span data-ttu-id="194d2-161">(See suvand oli teatud menüükäsu tüüpide jaoks juba saadaval.)</span><span class="sxs-lookup"><span data-stu-id="194d2-161">(This option was already available for some other types of menu items.)</span></span>

- <span data-ttu-id="194d2-162">Litsentsiplaadi vastuvõtt (ja kõrvale panemine)</span><span class="sxs-lookup"><span data-stu-id="194d2-162">License plate receiving (and putaway)</span></span>
- <span data-ttu-id="194d2-163">Koormas oleva kauba vastuvõtmine (ja kõrvale panemine)</span><span class="sxs-lookup"><span data-stu-id="194d2-163">Load item receiving (and putaway)</span></span>
- <span data-ttu-id="194d2-164">Vastuvõttev ostutellimuse rida (ja kõrvaleseadmine)</span><span class="sxs-lookup"><span data-stu-id="194d2-164">Purchase order line receiving (and putaway)</span></span>
- <span data-ttu-id="194d2-165">Vastuvõttev ostutellimuse üksus (ja kõrvaleseadmine)</span><span class="sxs-lookup"><span data-stu-id="194d2-165">Purchase order item receiving (and putaway)</span></span>

<span data-ttu-id="194d2-166">**Asukoha** menüü-üksuse säte kirjutab üle lao vastuvõtmise vaikeasukohta kõigi tellimuste puhul, mida töödeldakse selle menüükäsu abil.</span><span class="sxs-lookup"><span data-stu-id="194d2-166">The **To location** setting for a menu item overrides the default receiving location for the warehouse, for all orders that are processed by using that menu item.</span></span>

<span data-ttu-id="194d2-167">Mobiilse seadme menüü-üksuse seadistamiseks, mis toetab vastuvõtmist kohandatud asukohas, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="194d2-167">To set up a mobile device menu item to support receiving at a custom location, follow these steps.</span></span>

1. <span data-ttu-id="194d2-168">Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü-üksused**.</span><span class="sxs-lookup"><span data-stu-id="194d2-168">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="194d2-169">Valige või looge menüükäsk, mis kasutab ühte selles jaotises varem loetletud tööloomise protsessidest.</span><span class="sxs-lookup"><span data-stu-id="194d2-169">Select or create a menu item that uses one of the work creation processes that are listed earlier in this section.</span></span>
1. <span data-ttu-id="194d2-170">Määrake FastTab-il **Üldine** suvandil **Kasutage vaikeandmed** valikut **Jah**.</span><span class="sxs-lookup"><span data-stu-id="194d2-170">On the **General** FastTab, set the **Use default data** option to **Yes**.</span></span>
1. <span data-ttu-id="194d2-171">Valige tegumiribal suvand **Vaikeandmed**.</span><span class="sxs-lookup"><span data-stu-id="194d2-171">On the Action Pane, select **Default data**.</span></span>
1. <span data-ttu-id="194d2-172">Määrake lehel **Vaikeandmed** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="194d2-172">On the **Default data** page, set the following values:</span></span>

    - <span data-ttu-id="194d2-173">**Vaikimisi andmeväli:** määrake see väli *asukohta*.</span><span class="sxs-lookup"><span data-stu-id="194d2-173">**Default data field:** Set this field to *To location*.</span></span>
    - <span data-ttu-id="194d2-174">**Ladu:** valige sihtladu, mida selle menüükäsuga kasutada.</span><span class="sxs-lookup"><span data-stu-id="194d2-174">**Warehouse:** Select the destination warehouse to use with this menu item.</span></span>
    - <span data-ttu-id="194d2-175">**Asukoht:** see väli loendab kõik valitud lao jaoks saadaolevad asukoha ID-d.</span><span class="sxs-lookup"><span data-stu-id="194d2-175">**Location:** This field lists all the location IDs that are available for the selected warehouse.</span></span> <span data-ttu-id="194d2-176">Kuid selle välja sättel ei ole tegelikult mingit mõju.</span><span class="sxs-lookup"><span data-stu-id="194d2-176">However, the setting of this field doesn't actually have any effect.</span></span> <span data-ttu-id="194d2-177">Seetõttu saate selle tühjaks jätta.</span><span class="sxs-lookup"><span data-stu-id="194d2-177">Therefore, you can leave it blank.</span></span> <span data-ttu-id="194d2-178">Sellegipoolest saate kasutada loendit, et kinnitada ID, mille peate sisestama väljale **Kindlaksmääratud väärtus**.</span><span class="sxs-lookup"><span data-stu-id="194d2-178">Nevertheless, you can use the list to confirm the ID that you must enter in the **Hardcoded value** field.</span></span>
    - <span data-ttu-id="194d2-179">**Kindlaksmääratud väärtus:** sisestage selle menüükäsuga seotud asukoha ID.</span><span class="sxs-lookup"><span data-stu-id="194d2-179">**Hardcoded value:** Enter the location ID for the receiving location that applies to this menu item.</span></span>

> [!TIP]
> <span data-ttu-id="194d2-180">Tööpoliitikat saab rakendada ainult siis, kui kõik vastuvõtvad asukohad on loetletud vastavas tööpoliitika sättes.</span><span class="sxs-lookup"><span data-stu-id="194d2-180">A work policy can be applied only if all the receiving locations are listed in the relevant work policy setup.</span></span> <span data-ttu-id="194d2-181">See nõue rakendub hoolimata sellest, kas kasutate lao vaikeasukohta või kohandatud asukohta.</span><span class="sxs-lookup"><span data-stu-id="194d2-181">This requirement applies regardless of whether you're using the default warehouse receiving location or a custom "to" location.</span></span>

## <a name="example-scenario-warehouse-receiving"></a><span data-ttu-id="194d2-182">Stsenaariumi näide: lao vastuvõtt</span><span class="sxs-lookup"><span data-stu-id="194d2-182">Example scenario: Warehouse receiving</span></span>

<span data-ttu-id="194d2-183">Kõik tooted, mis on vastu võetud *Ostutellimuse kauba vastuvõtmisel (ja ladustamisel)*, peavad olema registreeritud asukohas *FL-001* ja need peavad olema saadaval laos *24*.</span><span class="sxs-lookup"><span data-stu-id="194d2-183">All products that are received by the *Purchase order item receiving (and putaway)* process must be registered in location *FL-001*, and they must be available in warehouse *24*.</span></span> <span data-ttu-id="194d2-184">Siiski ei tohi tööd luua.</span><span class="sxs-lookup"><span data-stu-id="194d2-184">However, work should not be created.</span></span> <span data-ttu-id="194d2-185">Tooted, mis on saadud mis tahes muul viisil (s.h kasutades muid mobiilse seadme menüükäske) tuleks registreerida vaikimisi lao vastuvõtvas asukohas (*RECV*) ja töö tuleb luua nagu tavaliselt.</span><span class="sxs-lookup"><span data-stu-id="194d2-185">Products that are received by any other process (that is, by using other mobile device menu items) should be registered at the default warehouse receiving location (*RECV*), and work should be created as usual.</span></span> <span data-ttu-id="194d2-186">(See stsenaarium ei kuva vaikimisi vastuvõtmise häälestust.)</span><span class="sxs-lookup"><span data-stu-id="194d2-186">(This scenario doesn't show the default receiving setup.)</span></span>

<span data-ttu-id="194d2-187">See stsenaarium nõuab järgmisi elemente:</span><span class="sxs-lookup"><span data-stu-id="194d2-187">This scenario requires the following elements:</span></span>

- <span data-ttu-id="194d2-188">*Ostutellimuse kauba vastuvõtmine (ja kõrvalepanek)* tööpoliitika protsess asukohas *FL-001*, kõikidele toodetele</span><span class="sxs-lookup"><span data-stu-id="194d2-188">A work policy for the *Purchase order item receiving (and putaway)* process in location *FL-001*, for all products</span></span>
- <span data-ttu-id="194d2-189">Mobiilse seadme menüükäsk, millel on vaikeandmed ja mis määrab **Välja asukoha** väärtuseks *FL-001*</span><span class="sxs-lookup"><span data-stu-id="194d2-189">A mobile device menu item that has default data, and that sets the **To location** field to *FL-001*</span></span>

### <a name="prerequisites"></a><span data-ttu-id="194d2-190">Eeltingimused</span><span class="sxs-lookup"><span data-stu-id="194d2-190">Prerequisites</span></span>

<span data-ttu-id="194d2-191">Selles stsenaariumis kirjeldatud funktsioonide kättesaadavaks tegemiseks süsteemis peate sisse lülitama funktsioonid *Litsentsiplaadi täiustuste saamine* ja *Tööpoliitika täiustused sissetuleva töö puhul* asukohas [Funktsioonihaldus](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="194d2-191">To make the functionality that is described in this scenario available in your system, you must turn on the *License plate receiving enhancements* and *Work policy enhancements for inbound work* features in [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

<span data-ttu-id="194d2-192">See stsenaarium kasutab standardseid demoandmeid.</span><span class="sxs-lookup"><span data-stu-id="194d2-192">This scenario uses the standard demo data.</span></span> <span data-ttu-id="194d2-193">Niisiis, kui soovite selle läbida siin toodud väärtuseid kasutades, peate kasutama süsteemi, kuhu demoandmed on installitud.</span><span class="sxs-lookup"><span data-stu-id="194d2-193">Therefore, if you want to work through it by using the values that are provided here, you must work on a system where demo data is installed.</span></span> <span data-ttu-id="194d2-194">Peate valima ka juriidilise isiku **USMF**.</span><span class="sxs-lookup"><span data-stu-id="194d2-194">Additionally, you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-work-policy"></a><span data-ttu-id="194d2-195">Tööpoliitika häälestamine</span><span class="sxs-lookup"><span data-stu-id="194d2-195">Set up a work policy</span></span>

1. <span data-ttu-id="194d2-196">Minge asukohta **Laohaldus \> Häälestamine \> Töö \> Tööpoliitikad**.</span><span class="sxs-lookup"><span data-stu-id="194d2-196">Go to **Warehouse management \> Setup \> Work \> Work policies**.</span></span>
1. <span data-ttu-id="194d2-197">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="194d2-197">Select **New**.</span></span>
1. <span data-ttu-id="194d2-198">Minge väljal **Tööpoliitika nimi** asukohta *Ostukauba ladustamise töö puudub*.</span><span class="sxs-lookup"><span data-stu-id="194d2-198">In the **Work policy name** field, enter *No purchase item putaway work*.</span></span>
1. <span data-ttu-id="194d2-199">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="194d2-199">Select **Save**.</span></span>
1. <span data-ttu-id="194d2-200">**Töötellimuse tüüpide** FastTab-l valige **Lisa**, et lisada tabelisse rida ja seejärel määrake uue rea jaoks järgmised väärtused:</span><span class="sxs-lookup"><span data-stu-id="194d2-200">On the **Work order types** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="194d2-201">**Töötellimuse tüüp:** *ostutellimused*</span><span class="sxs-lookup"><span data-stu-id="194d2-201">**Work order type:** *Purchase orders*</span></span>
    - <span data-ttu-id="194d2-202">**Tööprotsess:** *vastuvõttev ostutellimuse kaup (ja ladustamine)*</span><span class="sxs-lookup"><span data-stu-id="194d2-202">**Work process:** *Purchase order item receiving (and putaway)*</span></span>
    - <span data-ttu-id="194d2-203">**Töö loomise meetod:** *mitte kunagi*</span><span class="sxs-lookup"><span data-stu-id="194d2-203">**Work creation method:** *Never*</span></span>
    - <span data-ttu-id="194d2-204">**Ristlaadimise poliitika nimi:** jätke see väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="194d2-204">**Cross docking policy name:** Leave this field blank.</span></span>

1. <span data-ttu-id="194d2-205">**Varude asukohtade** FastTab-l valige **Lisa**, et lisada tabelisse rida ja seejärel määrake uue rea jaoks järgmised väärtused:</span><span class="sxs-lookup"><span data-stu-id="194d2-205">On the **Inventory locations** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="194d2-206">**Ladu:** *24*</span><span class="sxs-lookup"><span data-stu-id="194d2-206">**Warehouse:** *24*</span></span>
    - <span data-ttu-id="194d2-207">**Asukoht:** *FL-001*</span><span class="sxs-lookup"><span data-stu-id="194d2-207">**Location:** *FL-001*</span></span>

1. <span data-ttu-id="194d2-208">**Toodete** FastTab-il seadistage välja **Tootevalik** väärtuseks *Kõik*.</span><span class="sxs-lookup"><span data-stu-id="194d2-208">On the **Products** FastTab, set the **Product selection** field to *All*.</span></span>
1. <span data-ttu-id="194d2-209">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="194d2-209">Select **Save**.</span></span>

### <a name="set-up-a-mobile-device-menu-item-to-change-the-receiving-location"></a><span data-ttu-id="194d2-210">Mobiilse seadme menüükäsu häälestus kättesaamise asukoha muutmiseks</span><span class="sxs-lookup"><span data-stu-id="194d2-210">Set up a mobile device menu item to change the receiving location</span></span>

1. <span data-ttu-id="194d2-211">Avage **Laohaldus \> Seadistus \> Mobiilne seade \> Mobiilse seadme menüü-üksused**.</span><span class="sxs-lookup"><span data-stu-id="194d2-211">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="194d2-212">Vasakpoolsel paanil valige olemasolev **Ostu vastuvõtmise** menüükäsk.</span><span class="sxs-lookup"><span data-stu-id="194d2-212">In the left pane, select the existing **Purchase receive** menu item.</span></span>
1. <span data-ttu-id="194d2-213">Määrake FastTab-il **Üldine** suvandil **Kasutage vaikeandmed** valikut *Jah*.</span><span class="sxs-lookup"><span data-stu-id="194d2-213">On the **General** FastTab, set the **Use default data** option to *Yes*.</span></span>
1. <span data-ttu-id="194d2-214">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="194d2-214">Select **Save**.</span></span>
1. <span data-ttu-id="194d2-215">Valige tegumiribal suvand **Vaikeandmed**.</span><span class="sxs-lookup"><span data-stu-id="194d2-215">On the Action Pane, select **Default data**.</span></span>
1. <span data-ttu-id="194d2-216">**Vaikeandmete** lehel tegevuspaanil valige **Uus**, et lisada tabelisse rida ja seejärel määrake uue rea jaoks järgmised väärtused:</span><span class="sxs-lookup"><span data-stu-id="194d2-216">On the **Default data** page, on the Action Pane, select **New** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="194d2-217">**Vaikimisi andmeväli:** *Asukohta*</span><span class="sxs-lookup"><span data-stu-id="194d2-217">**Default data field:** *To location*</span></span>
    - <span data-ttu-id="194d2-218">**Ladu:** *24*</span><span class="sxs-lookup"><span data-stu-id="194d2-218">**Warehouse:** *24*</span></span>
    - <span data-ttu-id="194d2-219">**Asukoht:** jätke see väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="194d2-219">**Location:** Leave this field blank.</span></span>
    - <span data-ttu-id="194d2-220">**Kindlaks määratud väärtus:** *FL-001*</span><span class="sxs-lookup"><span data-stu-id="194d2-220">**Hardcoded value:** *FL-001*</span></span>

1. <span data-ttu-id="194d2-221">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="194d2-221">Select **Save**.</span></span>

### <a name="receive-a-purchase-order-without-creating-work"></a><span data-ttu-id="194d2-222">Ostutellimuse vastuvõtmine tööd loomata</span><span class="sxs-lookup"><span data-stu-id="194d2-222">Receive a purchase order without creating work</span></span>

<span data-ttu-id="194d2-223">Selles jaotises toodud näites kirjeldatakse, kuidas saada ostutellimuse kaupa, kuid mitte tööd luues asukohas, mis erineb lao jaoks seadistatud vastuvõtmise vaikeasukohast.</span><span class="sxs-lookup"><span data-stu-id="194d2-223">The example in this section shows how to receive a purchase order item, but without creating work, at a location that differs from the default receiving location that is set up for the warehouse.</span></span> <span data-ttu-id="194d2-224">Selles näites kasutatakse tööpoliitikat ja mobiilse seadme üksust, mille lõite selle stsenaariumiga varem.</span><span class="sxs-lookup"><span data-stu-id="194d2-224">This example uses the work policy and mobile device item that you created earlier in this scenario.</span></span>

#### <a name="create-a-purchase-order"></a><span data-ttu-id="194d2-225">Ostutellimuse loomine</span><span class="sxs-lookup"><span data-stu-id="194d2-225">Create a purchase order</span></span>

1. <span data-ttu-id="194d2-226">Avage **Hanked \> Ostutellimused \> Kõik ostutellimused**.</span><span class="sxs-lookup"><span data-stu-id="194d2-226">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="194d2-227">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="194d2-227">Select **New**.</span></span>
1. <span data-ttu-id="194d2-228">Dialoogiboksis **Ostutellimuse loomine** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="194d2-228">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="194d2-229">**Hankija konto:** *US-101*</span><span class="sxs-lookup"><span data-stu-id="194d2-229">**Vendor account:** *US-101*</span></span>
    - <span data-ttu-id="194d2-230">**Tegevuskoht:** *2*</span><span class="sxs-lookup"><span data-stu-id="194d2-230">**Site:** *2*</span></span>
    - <span data-ttu-id="194d2-231">**Ladu:** *24*</span><span class="sxs-lookup"><span data-stu-id="194d2-231">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="194d2-232">Dialoogiboksi sulgemiseks ja uue müügitellimuse loomiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="194d2-232">Select **OK** to close the dialog box and open the new purchase order.</span></span>
1. <span data-ttu-id="194d2-233">FastTab **Ostutellimuse ridadel** määrake tühjale reale järgmised väärtused:</span><span class="sxs-lookup"><span data-stu-id="194d2-233">On the **Purchase order lines** FastTab, set the following values for the empty row:</span></span>

    - <span data-ttu-id="194d2-234">**Kauba kood:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="194d2-234">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="194d2-235">**Kogus:** *1*</span><span class="sxs-lookup"><span data-stu-id="194d2-235">**Quantity:** *1*</span></span>

1. <span data-ttu-id="194d2-236">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="194d2-236">Select **Save**.</span></span>
1. <span data-ttu-id="194d2-237">Märkige üles ostutellimuse number.</span><span class="sxs-lookup"><span data-stu-id="194d2-237">Make a note of the purchase order number.</span></span>

#### <a name="receive-a-purchase-order"></a><span data-ttu-id="194d2-238">Ostutellimuse vastuvõtmine</span><span class="sxs-lookup"><span data-stu-id="194d2-238">Receive a purchase order</span></span>

1. <span data-ttu-id="194d2-239">Logige sisse mobiilses seadmes lattu *24* kasutades *24* kasutaja ID-na ja *1* paroolina.</span><span class="sxs-lookup"><span data-stu-id="194d2-239">On the mobile device, sign in to warehouse *24* by using *24* as the user ID and *1* as the password.</span></span>
1. <span data-ttu-id="194d2-240">Valige **Sissetulev**.</span><span class="sxs-lookup"><span data-stu-id="194d2-240">Select **Inbound**.</span></span>
1. <span data-ttu-id="194d2-241">Valige **Ostu vastuvõtmine**.</span><span class="sxs-lookup"><span data-stu-id="194d2-241">Select **Purchase receive**.</span></span> <span data-ttu-id="194d2-242">Välja **Asukoht** väärtuseks peab olema seatud *FL-001*.</span><span class="sxs-lookup"><span data-stu-id="194d2-242">The **Location** field should be set to *FL-001*.</span></span>
1. <span data-ttu-id="194d2-243">Sisestage eelmises protseduuris loodud ostutellimuse number.</span><span class="sxs-lookup"><span data-stu-id="194d2-243">Enter the purchase order number for the purchase order that you created in the previous procedure.</span></span>
1. <span data-ttu-id="194d2-244">Sisestage väljale **Kauba number** väärtus *A0001*.</span><span class="sxs-lookup"><span data-stu-id="194d2-244">In the **Item number** field, enter *A0001*.</span></span>
1. <span data-ttu-id="194d2-245">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="194d2-245">Select **OK**.</span></span>
1. <span data-ttu-id="194d2-246">Sisestage väljale **Kogus** väärtus *1*.</span><span class="sxs-lookup"><span data-stu-id="194d2-246">In the **Quantity** field, enter *1*.</span></span>
1. <span data-ttu-id="194d2-247">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="194d2-247">Select **OK**.</span></span>

<span data-ttu-id="194d2-248">Ostutellimus on nüüd vastu võetud, kuid sellega pole seotud ühtegi tööd.</span><span class="sxs-lookup"><span data-stu-id="194d2-248">The purchase order is now received, but no work is associated with it.</span></span> <span data-ttu-id="194d2-249">Vaba kaubavaru on värskendatud ja kauba *A0001* kogus *1* on nüüd saadaval asukohas *FL-001*.</span><span class="sxs-lookup"><span data-stu-id="194d2-249">The on-hand inventory has been updated, and a quantity of *1* of item *A0001* is now available at location *FL-001*.</span></span>

## <a name="example-scenario-manufacturing"></a><span data-ttu-id="194d2-250">Stsenaariumi näide: tootmine</span><span class="sxs-lookup"><span data-stu-id="194d2-250">Example scenario: Manufacturing</span></span>

<span data-ttu-id="194d2-251">Järgmises näites on kaks tootmistellimust: *PRD-001* ja *PRD-002*.</span><span class="sxs-lookup"><span data-stu-id="194d2-251">In the following example, there are two production orders, *PRD-001* and *PRD-002*.</span></span> <span data-ttu-id="194d2-252">Tootmistellimusel *PRD-001* on toiming nimega *Assembler*, kus toode *SC1* on teatatud lõpetatuks asukohale *001*.</span><span class="sxs-lookup"><span data-stu-id="194d2-252">Production order *PRD-001* has an operation that is named *Assembly*, where product *SC1* is being reported as finished to location *001*.</span></span> <span data-ttu-id="194d2-253">Tootmistellimusel *PRD-002* on toiming nimega *Värvimine* ja tarbib toodet *SC1* asukohast *001*.</span><span class="sxs-lookup"><span data-stu-id="194d2-253">Production order *PRD-002* has an operation that is named *Painting* and consumes product *SC1* from location *001*.</span></span> <span data-ttu-id="194d2-254">Tootmistellimus *PRD-002* tarbib ka toormaterjali *RM1* asukohast *001*.</span><span class="sxs-lookup"><span data-stu-id="194d2-254">Production order *PRD-002* also consumes raw material *RM1* from location *001*.</span></span> <span data-ttu-id="194d2-255">Toormaterjali *RM1* hoitakse laoasukohas *BULK-001* ja komplekteeritakse asukohale *001* laotööga toormaterjali komplekteerimiseks.</span><span class="sxs-lookup"><span data-stu-id="194d2-255">Raw material *RM1* is stored in warehouse location *BULK-001* and will be picked to location *001* by warehouse work for raw material picking.</span></span> <span data-ttu-id="194d2-256">Komplekteerimistöö luuakse tootmise *PRD-002* väljastamisel.</span><span class="sxs-lookup"><span data-stu-id="194d2-256">The picking work is generated when production *PRD-002* is released.</span></span>

<span data-ttu-id="194d2-257">[![Lao tööpoliitikad](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span><span class="sxs-lookup"><span data-stu-id="194d2-257">[![Warehouse work policies](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span></span>

<span data-ttu-id="194d2-258">Kui plaanite selle stsenaariumi jaoks konfigureerida lao tööpoliitika, peaksite arvestama järgmisi punkte.</span><span class="sxs-lookup"><span data-stu-id="194d2-258">When you're planning to configure a warehouse work policy for this scenario, you should consider the following points:</span></span>

- <span data-ttu-id="194d2-259">Laotöö pole lõpetatud kaupade ladustamiseks vajalik, kui teatate toote *SC1* lõpetatuks tootmistellimusest *PRD-001* asukohale *001*.</span><span class="sxs-lookup"><span data-stu-id="194d2-259">Warehouse work for putaway of finished goods isn't required when you report product *SC1* as finished from production order *PRD-001* to location *001*.</span></span> <span data-ttu-id="194d2-260">Seda põhjusel, et tootmistellimuse *PRD-002* toiming *Värvimine* tarbib samas asukohas toodet *SC1*.</span><span class="sxs-lookup"><span data-stu-id="194d2-260">The reason is that the *Painting* operation for production order *PRD-002* consumes product *SC1* at the same location.</span></span>
- <span data-ttu-id="194d2-261">Laotöö on toormaterjali komplekteerimiseks vajalik, et liigutada toormaterjali *RM1* laoasukohast *BULK-001* asukohta *001*.</span><span class="sxs-lookup"><span data-stu-id="194d2-261">Warehouse work for raw material picking is required to move raw material *RM1* from warehouse location *BULK-001* to location *001*.</span></span>

<span data-ttu-id="194d2-262">Siin on näide tööpoliitikast, mida saate nende kaalutluste põhjal seadistada:</span><span class="sxs-lookup"><span data-stu-id="194d2-262">Here is an example of a work policy that you can set up, based on these considerations:</span></span>

- <span data-ttu-id="194d2-263">**Tööpoliitika nimi:** *ladustamistööd ei ole*</span><span class="sxs-lookup"><span data-stu-id="194d2-263">**Work policy name:** *No putaway work*</span></span>
- <span data-ttu-id="194d2-264">**Töötellimuse tüübid:** *lõpetatud kaupade ladustamine* ja *Kaastoote ja kõrvalsaaduse ladustamine*</span><span class="sxs-lookup"><span data-stu-id="194d2-264">**Work order types:** *Finished goods put away* and *Co-product and by-product put away*</span></span>
- <span data-ttu-id="194d2-265">**Varude asukohad:** ladu *51* ja asukoht *001*</span><span class="sxs-lookup"><span data-stu-id="194d2-265">**Inventory locations:** Warehouse *51* and location *001*</span></span>
- <span data-ttu-id="194d2-266">**Tooted:** *SC1*</span><span class="sxs-lookup"><span data-stu-id="194d2-266">**Products:** *SC1*</span></span>

<span data-ttu-id="194d2-267">Järgmised näidisstsenaariumid annavad etapiviisilise juhise, kuidas seadistada selle stsenaarium jaoks laotöö poliitikat.</span><span class="sxs-lookup"><span data-stu-id="194d2-267">The following example scenario provides step-by-step instructions for setting up the warehouse work policy for this scenario.</span></span>

## <a name="example-scenario-report-as-finished-to-a-location-that-isnt-license-platecontrolled"></a><span data-ttu-id="194d2-268">Näidisstsenaarium: teatage tootmistellimus lõpetatuks asukohale, mis pole litsentsiplaadiga kontrollitud</span><span class="sxs-lookup"><span data-stu-id="194d2-268">Example scenario: Report as finished to a location that isn't license plate–controlled</span></span>

<span data-ttu-id="194d2-269">See stsenaarium näitab näidet, kus tootmistellimus teatatakse lõpetatuks asukohale, mis pole litsentsiplaadiga kontrollitav.</span><span class="sxs-lookup"><span data-stu-id="194d2-269">This scenario shows an example where a production order is reported as finished to a location that isn't license plate–controlled.</span></span>

<span data-ttu-id="194d2-270">See stsenaarium kasutab standardseid demoandmeid.</span><span class="sxs-lookup"><span data-stu-id="194d2-270">This scenario uses the standard demo data.</span></span> <span data-ttu-id="194d2-271">Niisiis, kui soovite selle läbida siin toodud väärtuseid kasutades, peate kasutama süsteemi, kuhu demoandmed on installitud.</span><span class="sxs-lookup"><span data-stu-id="194d2-271">Therefore, if you want to work through it by using the values that are provided here, you must work on a system where demo data is installed.</span></span> <span data-ttu-id="194d2-272">Peate valima ka juriidilise isiku **USMF**.</span><span class="sxs-lookup"><span data-stu-id="194d2-272">Additionally, you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-warehouse-work-policy"></a><span data-ttu-id="194d2-273">Lao tööpoliitika seadistamine</span><span class="sxs-lookup"><span data-stu-id="194d2-273">Set up a warehouse work policy</span></span>

<span data-ttu-id="194d2-274">Laotoimingud ei hõlma alati laotööd.</span><span class="sxs-lookup"><span data-stu-id="194d2-274">Warehouse processes don't always include warehouse work.</span></span> <span data-ttu-id="194d2-275">Tööpoliitika määratlemisel saate vältida töö loomist toormaterjali komplekteerimise puhul ja lõpetatud kaupade ladustamist toodete kogumi puhul kindlates asukohtades.</span><span class="sxs-lookup"><span data-stu-id="194d2-275">By defining a work policy, you can prevent the creation of work for raw material picking and putaway of finished goods for a set of products at specific locations.</span></span>

1. <span data-ttu-id="194d2-276">Minge asukohta **Laohaldus \> Häälestamine \> Töö \> Tööpoliitikad**.</span><span class="sxs-lookup"><span data-stu-id="194d2-276">Go to **Warehouse management \> Setup \> Work \> Work policies**.</span></span>
1. <span data-ttu-id="194d2-277">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="194d2-277">Select **New**.</span></span>
1. <span data-ttu-id="194d2-278">Minge väljal **Tööpoliitika nimi** asukohta *Ladustamistöö puudub*.</span><span class="sxs-lookup"><span data-stu-id="194d2-278">In the **Work policy name** field, enter *No putaway work*.</span></span>
1. <span data-ttu-id="194d2-279">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="194d2-279">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="194d2-280">**Töötellimuse tüüpide** FastTab-l valige **Lisa**, et lisada tabelisse rida ja seejärel määrake uue rea jaoks järgmised väärtused:</span><span class="sxs-lookup"><span data-stu-id="194d2-280">On the **Work order types** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="194d2-281">**Töötellimuse tüüp:** *lõpetatud kaupade ladustamine*</span><span class="sxs-lookup"><span data-stu-id="194d2-281">**Work order type:** *Finished goods put away*</span></span>
    - <span data-ttu-id="194d2-282">**Tööprotsess:** *kõik seotud tööprotsessid*</span><span class="sxs-lookup"><span data-stu-id="194d2-282">**Work process:** *All related work processes*</span></span>
    - <span data-ttu-id="194d2-283">**Töö loomise meetod:** *mitte kunagi*</span><span class="sxs-lookup"><span data-stu-id="194d2-283">**Work creation method:** *Never*</span></span>
    - <span data-ttu-id="194d2-284">**Ristlaadimise poliitika nimi:** jätke see väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="194d2-284">**Cross docking policy name:** Leave this field blank.</span></span>

1. <span data-ttu-id="194d2-285">Valige **Lisa** uuesti, et lisada tabelisse teine rida ja seejärel määrake uue rea jaoks järgmised väärtused:</span><span class="sxs-lookup"><span data-stu-id="194d2-285">Select **Add** again to add a second row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="194d2-286">**Töötellimuse tüüp:** *kaastoodete ja kõrvalsaaduste ladustamine*</span><span class="sxs-lookup"><span data-stu-id="194d2-286">**Work order type:** *Co-product and by-product put away*</span></span>
    - <span data-ttu-id="194d2-287">**Tööprotsess:** *kõik seotud tööprotsessid*</span><span class="sxs-lookup"><span data-stu-id="194d2-287">**Work process:** *All related work processes*</span></span>
    - <span data-ttu-id="194d2-288">**Töö loomise meetod:** *mitte kunagi*</span><span class="sxs-lookup"><span data-stu-id="194d2-288">**Work creation method:** *Never*</span></span>
    - <span data-ttu-id="194d2-289">**Ristlaadimise poliitika nimi:** jätke see väli tühjaks.</span><span class="sxs-lookup"><span data-stu-id="194d2-289">**Cross docking policy name:** Leave this field blank.</span></span>

1. <span data-ttu-id="194d2-290">**Varude asukohtade** FastTab-l valige **Lisa**, et lisada tabelisse rida ja seejärel määrake uue rea jaoks järgmised väärtused:</span><span class="sxs-lookup"><span data-stu-id="194d2-290">On the **Inventory locations** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="194d2-291">**Ladu:** *51*</span><span class="sxs-lookup"><span data-stu-id="194d2-291">**Warehouse:** *51*</span></span>
    - <span data-ttu-id="194d2-292">**Asukoht:** *001*</span><span class="sxs-lookup"><span data-stu-id="194d2-292">**Location:** *001*</span></span>

1. <span data-ttu-id="194d2-293">**Toodete** FastTab-il seadistage välja **Tootevalik** väärtuseks *Valitud*.</span><span class="sxs-lookup"><span data-stu-id="194d2-293">On the **Products** FastTab, set the **Product selection** field to *Selected*.</span></span>
1. <span data-ttu-id="194d2-294">FastTab-il **Tooted** valige käsk **Lisa**, et lisada uus rida tabelisse.</span><span class="sxs-lookup"><span data-stu-id="194d2-294">On the **Products** FastTab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="194d2-295">Uues reas määrake välja **Kauba number** väärtuseks *L0101*.</span><span class="sxs-lookup"><span data-stu-id="194d2-295">In the new row, set the **Item number** field to *L0101*.</span></span>
1. <span data-ttu-id="194d2-296">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="194d2-296">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-an-output-location"></a><span data-ttu-id="194d2-297">Väljundi asukoha seadistamine</span><span class="sxs-lookup"><span data-stu-id="194d2-297">Set up an output location</span></span>

1. <span data-ttu-id="194d2-298">Avage **Organisatsiooni haldus \> Ressursid \> Ressursigrupid**.</span><span class="sxs-lookup"><span data-stu-id="194d2-298">Go to **Organization administration \> Resources \> Resource groups**.</span></span>
1. <span data-ttu-id="194d2-299">Valige vasakult paneelist ressursigrupp **5102**.</span><span class="sxs-lookup"><span data-stu-id="194d2-299">In the left pane, select resource group **5102**.</span></span>
1. <span data-ttu-id="194d2-300">Määrake kiirkaardil **Üldine** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="194d2-300">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="194d2-301">**Väljastusladu:** *51*</span><span class="sxs-lookup"><span data-stu-id="194d2-301">**Output warehouse:** *51*</span></span>
    - <span data-ttu-id="194d2-302">**Väljastuskoht:** *001*</span><span class="sxs-lookup"><span data-stu-id="194d2-302">**Output location:** *001*</span></span>

1. <span data-ttu-id="194d2-303">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="194d2-303">On the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="194d2-304">Asukoht *001* pole litsentsiplaadiga juhitav asukoht.</span><span class="sxs-lookup"><span data-stu-id="194d2-304">Location *001* isn't a license plate–controlled location.</span></span> <span data-ttu-id="194d2-305">Saate seadistada väljundi, mis pole litsentsiplaadiga juhitav, asukoha ainult siis, kui asukohale on olemas vastav tööpoliitika.</span><span class="sxs-lookup"><span data-stu-id="194d2-305">You can set up an output location that isn't license plate–controlled only if an applicable work policy exists for the location.</span></span>

### <a name="create-a-production-order-and-report-it-as-finished"></a><span data-ttu-id="194d2-306">Tootmistellimuse loomine ja selle lõpetatuna kinnitamine</span><span class="sxs-lookup"><span data-stu-id="194d2-306">Create a production order and report it as finished</span></span>

1. <span data-ttu-id="194d2-307">Avage **Tootmise juhtimine \> Tootmistellimused \> Kõik tootmistellimused**.</span><span class="sxs-lookup"><span data-stu-id="194d2-307">Go to **Production control \> Production orders \> All production orders**.</span></span>
1. <span data-ttu-id="194d2-308">Toimingupaanil valige **Uus tootmistellimus**.</span><span class="sxs-lookup"><span data-stu-id="194d2-308">On the Action Pane, select **New production order**.</span></span>
1. <span data-ttu-id="194d2-309">Seadistage dialoogiaknas **Loo tootmistellimus** välja **Kauba number** väärtuseks *L0101*.</span><span class="sxs-lookup"><span data-stu-id="194d2-309">In the **Create production order** dialog box, set the **Item number** field to *L0101*.</span></span>
1. <span data-ttu-id="194d2-310">Valige tellimuse loomiseks ja dialoogiboksi sulgemiseks **Loo**.</span><span class="sxs-lookup"><span data-stu-id="194d2-310">Select **Create** to create the order and close the dialog box.</span></span>

    <span data-ttu-id="194d2-311">**Kõik tootmistellimused** lehe tabelisse lisatakse uus tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="194d2-311">A new production order is added to the grid on the **All production orders** page.</span></span>

    <span data-ttu-id="194d2-312">Hoidke uus tootmistellimus valituna.</span><span class="sxs-lookup"><span data-stu-id="194d2-312">Keep the new production order selected.</span></span>

1. <span data-ttu-id="194d2-313">Tehke tegumiriba vahekaardil **Tootmistellimus** grupis **Protsess** valik **Hinda**.</span><span class="sxs-lookup"><span data-stu-id="194d2-313">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Estimate**.</span></span>
1. <span data-ttu-id="194d2-314">Dialoogiaknas **Hinda** lugege hinnangut ja seejärel klõpsake nuppu **OK**, et sulgeda dialoogiaken.</span><span class="sxs-lookup"><span data-stu-id="194d2-314">In the **Estimate** dialog box, read the estimate, and then select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="194d2-315">Tehke tegumiriba vahekaardil **Tootmistellimus** grupis **Protsess** valik **Alusta**.</span><span class="sxs-lookup"><span data-stu-id="194d2-315">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Start**.</span></span>
1. <span data-ttu-id="194d2-316">Seadke dialoogiaknas **Alusta** vahekaardil **Üldine** väli **Automaatne BOM-tarbimine** väärtuseks *Mitte kunagi*.</span><span class="sxs-lookup"><span data-stu-id="194d2-316">In the **Start** dialog box, on the **General** tab, set the **Automatic BOM consumption** field to *Never*.</span></span>
1. <span data-ttu-id="194d2-317">Valige **OK**, et salvestada oma säte ja sulgeda dialoogiaken.</span><span class="sxs-lookup"><span data-stu-id="194d2-317">Select **OK** to save your setting and close the dialog box.</span></span>
1. <span data-ttu-id="194d2-318">Tehke tegumiriba vahekaardil **Tootmistellimus** grupis **Protsess** valik **Kinnita lõpetatuks**.</span><span class="sxs-lookup"><span data-stu-id="194d2-318">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Report as finished**.</span></span>
1. <span data-ttu-id="194d2-319">Dialoogiaknas **Lõpetatuks kinnitamine** vahekaardil **Üldine** määrake suvandi **Kinnita tõrge** väärtuseks *Jah*.</span><span class="sxs-lookup"><span data-stu-id="194d2-319">In the **Report as finished** dialog box, on the **General** tab, set the **Accept error** option to *Yes*.</span></span>
1. <span data-ttu-id="194d2-320">Valige **OK**, et salvestada oma säte ja sulgeda dialoogiaken.</span><span class="sxs-lookup"><span data-stu-id="194d2-320">Select **OK** to save your setting and close the dialog box.</span></span>
1. <span data-ttu-id="194d2-321">Valige toimingupaani vahekaardil **Ladu** grupis **Seotud teave** üksus **Töö üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="194d2-321">On the Action Pane, on the **Warehouse** tab, in the **General** group, select **Work details**.</span></span>

<span data-ttu-id="194d2-322">Kui tootmistellimus on lõpetatuks kuulutatud, pole ladustamiseks tööd loodud.</span><span class="sxs-lookup"><span data-stu-id="194d2-322">When the production order is reported as finished, no work is generated for putaway.</span></span> <span data-ttu-id="194d2-323">Seda käitumist ilmneb, kuna määratletud on tööpoliitika, mis takistab töö loomist, kui toode *L0101* kuulutatakse lõpetatuks asukohale *001*.</span><span class="sxs-lookup"><span data-stu-id="194d2-323">This behavior occurs because a work policy is defined that prevents work from being generated when product *L0101* is reported as finished to location *001*.</span></span>

## <a name="more-information"></a><span data-ttu-id="194d2-324">Lisateave</span><span class="sxs-lookup"><span data-stu-id="194d2-324">More information</span></span>

<span data-ttu-id="194d2-325">Lisateavet mobiilse seadme menüü üksuste kohta vt teemast [Mobiilsete seadmete seadistamine laotöö jaoks](configure-mobile-devices-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="194d2-325">For more information about mobile device menu items, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>

<span data-ttu-id="194d2-326">Lisateavet, mis on seotud litsentsiplaadi vastuvõtmisega ja tööpoliitikatega, leiate teemast [Litsentsiplaadi vastuvõtmine mobiilirakenduse Warehouse Management kaudu](warehousing-mobile-device-app-license-plate-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="194d2-326">For more information about license plate receiving and work policies, see [License plate receiving via the Warehouse Management mobile app](warehousing-mobile-device-app-license-plate-receiving.md).</span></span>

<span data-ttu-id="194d2-327">Lisateavet sissetuleva koormuse halduse kohta vt teemast [Ostutellimuste sissetulevate koormate laohaldus](inbound-load-handling.md).</span><span class="sxs-lookup"><span data-stu-id="194d2-327">For more information about inbound load management, see [Warehouse handling of inbound loads for purchase orders](inbound-load-handling.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]