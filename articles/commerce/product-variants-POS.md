---
title: Otsing varudest kassas
description: Selles teemas kirjeldatakse võimalusi, mis on saadaval varude teabe vaatamiseks kassas.
author: ashishmsft
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.openlocfilehash: 26bbbeee7ed6c228b3c84dc07576bccb8e1aebd8
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5231004"
---
# <a name="inventory-lookup-in-the-point-of-sale-pos"></a><span data-ttu-id="64512-103">Otsing varudest kassas</span><span class="sxs-lookup"><span data-stu-id="64512-103">Inventory lookup in the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="64512-104">Otsing varudest kassas aitab jaemüüjatel reaalajas saavutada kõrget töökvaliteeti ning saada ülevaateid kaupluste, kassa ja varukontori ühendamise teel.</span><span class="sxs-lookup"><span data-stu-id="64512-104">Inventory lookup in the point of sale (POS) helps retailers achieve real-time operational excellence and gain insights by connecting stores, the POS, and the back office.</span></span> <span data-ttu-id="64512-105">See funktsiooni annab täpse reaalajas vaate toote varudest kauplustes ja turustuskeskustes.</span><span class="sxs-lookup"><span data-stu-id="64512-105">This functionality provides an accurate real-time view of product inventory across stores and distribution centers.</span></span> <span data-ttu-id="64512-106">Samuti aitab see jaemüüjatel suurendada tõhusust ja säästlikkust, tõhustades varude planeerimist reaalajas.</span><span class="sxs-lookup"><span data-stu-id="64512-106">It also helps retailers drive additional efficiencies and cost savings by improving inventory planning in real time.</span></span>

<span data-ttu-id="64512-107">Täpne reaalajas ülevaade varudest kogu organisatsioonis aitab kaupluste töötajatel pakkuda kiiret ja tõhusat klienditeenindust.</span><span class="sxs-lookup"><span data-stu-id="64512-107">An accurate real-time view of inventory across an organization helps store associates provide timely, superior customer service.</span></span> <span data-ttu-id="64512-108">Kõige tähtsam hetk on see, mil klient on valmis tegema ostuotsust.</span><span class="sxs-lookup"><span data-stu-id="64512-108">The moment that matters most is the moment when the customer is ready to make a purchase decision.</span></span> <span data-ttu-id="64512-109">On tähtis, et kaupluse kassapidajatel oleks varude reaalajas teave käeulatuses, et nad saaksid pakkuda täpseid toote tarne ja komplekteerimise aegu.</span><span class="sxs-lookup"><span data-stu-id="64512-109">It's important that cashiers in the store have real-time inventory information at their fingertips, so that they can accurately promise product delivery and pickup.</span></span>

<span data-ttu-id="64512-110">Saate avada lehe **Otsing varudest** tööruumist **Retail Modern POS** või tööruumist **Jaemüügi pilvekassa**.</span><span class="sxs-lookup"><span data-stu-id="64512-110">You can open the **Inventory lookup** page from the **Retail Modern POS** workspace or the **Retail Cloud POS** workspace.</span></span>

![Varude otsingupaan kassa avalehel](media/POSHomepage.png)

<span data-ttu-id="64512-112">Lehel **Otsing varudest** saate kasutada numbriklaviatuuri tootenumbri sisestamiseks.</span><span class="sxs-lookup"><span data-stu-id="64512-112">On the **Inventory lookup** page, you can use the numeric keyboard to enter a product number.</span></span> <span data-ttu-id="64512-113">Saate vaadata laos olevat kogust mitme kaupluse ja lao kohta.</span><span class="sxs-lookup"><span data-stu-id="64512-113">You can then view the on-hand quantity for multiple stores and warehouses.</span></span>

![Standardne varude otsingu leht](media/InventoryLookUp.png)

<span data-ttu-id="64512-115">Iga asukoha kohta kuvatakse ka **reserveeritud** ja **tellitud** kogused.</span><span class="sxs-lookup"><span data-stu-id="64512-115">**Reserved** and **Ordered** quantities are also shown for each location.</span></span>

- <span data-ttu-id="64512-116">**Reserveeritud** – see kogus viitab **füüsiliselt reserveeritud** väärtusele varukontorist määratud tootenumbri kohta asukohas.</span><span class="sxs-lookup"><span data-stu-id="64512-116">**Reserved** – This quantity refers to the **Physical reserved** value from the back office for the specified product number at the location.</span></span>
- <span data-ttu-id="64512-117">**Tellitud** – see kogus viitab **kokku tellitud** väärtusele varukontorist määratud tootenumbri kohta asukohas.</span><span class="sxs-lookup"><span data-stu-id="64512-117">**Ordered** – This quantity refers to the **Ordered in total** value from the back office for the specified product number at the location.</span></span>

## <a name="locations-that-inventory-availability-information-is-shown-for"></a><span data-ttu-id="64512-118">Asukohad, mille kohta kuvatakse varude saadavuse teave</span><span class="sxs-lookup"><span data-stu-id="64512-118">Locations that inventory availability information is shown for</span></span>

<span data-ttu-id="64512-119">Asukohtade loend sisaldab kahte järgmist tüüpi üksuseid.</span><span class="sxs-lookup"><span data-stu-id="64512-119">The list of locations includes two types of entities:</span></span>

- <span data-ttu-id="64512-120">**Kauplused** – selles loendis kuvatakse kauplused, mille konfigureerimiseks on kasutatud kaupluselokaatori gruppi praeguse kaupluse jaoks komponendis Headquarters.</span><span class="sxs-lookup"><span data-stu-id="64512-120">**Stores** – The list shows stores that are configured by using the store locator group for the current store in the Headquarters.</span></span>
- <span data-ttu-id="64512-121">**Jaotuskeskused** – rakenduses Commerce saab konfigureerida erinevaid jaotuskeskuseid (nt ladusid).</span><span class="sxs-lookup"><span data-stu-id="64512-121">**Distribution centers** – Various types of distribution centers (such as warehouses) can be configured in Commerce.</span></span> <span data-ttu-id="64512-122">Kuid loendis kuvatakse varude saadavuse teave ainult jaotuskeskuste kohta, mille vaiketüüp on **Standardne**.</span><span class="sxs-lookup"><span data-stu-id="64512-122">However, the list shows inventory availability information only for distribution centers of the **Standard** default type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="64512-123">Varude saadavuse teavet ei kuvata ladude kohta, mille kassatüüp on **Transiit**, **Vaheladu** ja **Kaubad töötemisel**.</span><span class="sxs-lookup"><span data-stu-id="64512-123">Inventory availability information isn't shown for warehouses of the **Transit**, **Quarantine**, and **Goods in Route** types for the POS.</span></span>

<span data-ttu-id="64512-124">Lehel **Otsing varudest** saate iga kaupluse kohta lisaks praeguse vaba kaubavaru, reserveeritud koguste ja tellitud koguste teabele vaadata ka lubamiseks saadaval (ATP) koguseid.</span><span class="sxs-lookup"><span data-stu-id="64512-124">On the **Inventory lookup** page, you can view available to promise (ATP) quantities for each store, in addition to the current on-hand quantities, reserved quantities, and ordered quantities.</span></span> <span data-ttu-id="64512-125">Valige kauplus, mille ATP teavet soovite vaadata, ja seejärel valige **Kaupluse saadavuse kuvamine**.</span><span class="sxs-lookup"><span data-stu-id="64512-125">Select the store to view the ATP information for, and then select **Show store availability**.</span></span>

![ATP-i kogused](media/ATP.png)

## <a name="opening-the-dimension-based-matrix-view-to-show-all-variants"></a><span data-ttu-id="64512-127">Dimensioonipõhise maatriksvaate avamine kõigi variantide kuvamiseks</span><span class="sxs-lookup"><span data-stu-id="64512-127">Opening the Dimension based matrix view to show all variants</span></span>

<span data-ttu-id="64512-128">Tooteetaloni lehel **Toote üksikasjad** või lehel **Otsing varudest** valige lehe allosas rakenduste realt suvand **Kõigi variantide kuvamine**.</span><span class="sxs-lookup"><span data-stu-id="64512-128">On the **Product details** page of a product master, or on the **Inventory lookup** page, select **View all variants** from the app-bar at bottom of the page.</span></span> <span data-ttu-id="64512-129">Nende lehtede esmasel avamisel avanev vaade **Dimensioonipõhine maatriks** kuvab varude saadavuse teabe toote kõigi variantide kohta praeguses kaupluses.</span><span class="sxs-lookup"><span data-stu-id="64512-129">The **Dimension based matrix** view for the initial launch from these pages shows the inventory availability information for all variants of a product for the current store.</span></span>

> [!NOTE]
> <span data-ttu-id="64512-130">Nupp **Kõigi variantide kuvamine** on saadaval ainult kauba tooteetalonide korral, millel on tootevariandid.</span><span class="sxs-lookup"><span data-stu-id="64512-130">The **View all variants** button is available only for item product masters that have product variants.</span></span> <span data-ttu-id="64512-131">See pole saadaval eraldiseisvate toodete või komplektide korral.</span><span class="sxs-lookup"><span data-stu-id="64512-131">It isn't available for standalone products or kits.</span></span>

![Kõigi variantide kuvamise nupp lehel Otsing varudest](media/StandardToMatrix.png)

<span data-ttu-id="64512-133">Valige suvand **Kõigi variantide kuvamine** tooteetaloni lehel **Toote üksikasjad** või lehel **Otsing varudest** ilma asukohta valimata, et avada vaade **Dimensioonipõhine maatriks**, et vaadata varude saadavuse teavet toote kõigi variantide kohta praeguses kaupluses.</span><span class="sxs-lookup"><span data-stu-id="64512-133">Select **View all variants** on the **Product details** page of a product master, or on the **Inventory lookup** page, without selecting a location, to go to the **Dimension based matrix** view to view the inventory availability information for all variants of a product for the current store.</span></span>

![Dimensioonipõhise maatriksi vaade lehel Otsing varudest](media/Matrix.png)

> [!NOTE]
> <span data-ttu-id="64512-135">Eelmises näites on dimensioonide kuvamisjärjestus alfabeetiline, sest dimensioonide kuvamisjärjestust ei konfigureeritud valitud toote jaoks.</span><span class="sxs-lookup"><span data-stu-id="64512-135">In the preceding illustration, the display order of the dimensions is alphabetic, because the display order of dimensions wasn't configured for the selected product.</span></span>

<span data-ttu-id="64512-136">Vaates **Dimensioonipõhine maatriks** sisaldavad tootevariantide lahtrid parempoolses allnurgas vaba laoseisu väärtust.</span><span class="sxs-lookup"><span data-stu-id="64512-136">In the **Dimension based matrix** view, the cells for the product variants include an on-hand value in the lower-right corner.</span></span> <span data-ttu-id="64512-137">Järgmises tabelis selgitatakse erinevate väärtuste tähendust.</span><span class="sxs-lookup"><span data-stu-id="64512-137">The following table explains the meaning of the various values.</span></span>

| <span data-ttu-id="64512-138">Laoseisu väärtus</span><span class="sxs-lookup"><span data-stu-id="64512-138">On-hand value</span></span>                            | <span data-ttu-id="64512-139">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="64512-139">Description</span></span> |
|------------------------------------------|-------------|
| <span data-ttu-id="64512-140">Numbriline väärtus, mis on suurem kui 0 (null)</span><span class="sxs-lookup"><span data-stu-id="64512-140">Numeric value that is more than 0 (zero)</span></span> | <span data-ttu-id="64512-141">Variant on väljastatud valitud asukoha jaoks ja te saate lahtris teha täiendavaid toiminguid.</span><span class="sxs-lookup"><span data-stu-id="64512-141">A variant has been released to the selected location, and you can perform additional actions in the cell.</span></span> <span data-ttu-id="64512-142">(Neid toiminguid kirjeldatakse üksikasjalikumalt selles teemas allpool.)</span><span class="sxs-lookup"><span data-stu-id="64512-142">(These actions are described in more detail later in this topic.)</span></span> |
| <span data-ttu-id="64512-143">**0** (null)</span><span class="sxs-lookup"><span data-stu-id="64512-143">**0** (zero)</span></span>                             | <span data-ttu-id="64512-144">Variant on väljastatud valitud asukoha jaoks, kuid kaup pole valitud asukohas saadaval.</span><span class="sxs-lookup"><span data-stu-id="64512-144">A variant has been released to the selected location, but the item isn't available in selected location.</span></span> <span data-ttu-id="64512-145">Saate siiski teha lahtris täiendavaid toiminguid.</span><span class="sxs-lookup"><span data-stu-id="64512-145">However, you can perform additional actions in the cell.</span></span> <span data-ttu-id="64512-146">(Neid toiminguid kirjeldatakse üksikasjalikumalt selles teemas allpool.)</span><span class="sxs-lookup"><span data-stu-id="64512-146">(These actions are described in more detail later in this topic.)</span></span> |
| <span data-ttu-id="64512-147">**p/s** või passiivne lahter</span><span class="sxs-lookup"><span data-stu-id="64512-147">**n/a** or an inactive cell</span></span>              | <span data-ttu-id="64512-148">Varianti pole valitud asukoha jaoks väljastatud ja te ei saa lahtris täiendavaid toiminguid teha.</span><span class="sxs-lookup"><span data-stu-id="64512-148">A variant hasn't been released to the selected location, and you can't perform additional actions in the cell.</span></span> |

<span data-ttu-id="64512-149">Saate muuta ka dimensioonide liigendust, valides kasutamiseks uue dimensiooni.</span><span class="sxs-lookup"><span data-stu-id="64512-149">You can also change the pivot for dimensions by selecting the new dimension to use.</span></span>

![Liigenduse muutmine](media/ChangePivot.png)

![Liigendus on muudetud](media/PivotChanged.png)

> [!NOTE]
> <span data-ttu-id="64512-152">Eelmisel illustratsioonidel on valitud toote dimensioonide kuvamisjärjestuse kohandatud (mittealfabeetiline).</span><span class="sxs-lookup"><span data-stu-id="64512-152">In the preceding illustrations, the display order of the dimensions for the selected product is custom (non-alphabetic).</span></span> <span data-ttu-id="64512-153">See põhineb varukontoris määratud dimensioonide kuvamisjärjestusel.</span><span class="sxs-lookup"><span data-stu-id="64512-153">It's based on the dimension display order that is set in the back office.</span></span>

<span data-ttu-id="64512-154">Peale selle saab vaates **Dimensioonipõhine maatriks** teha rohkem toiminguid, et suurendada kaupluse töötaja tööviljakust.</span><span class="sxs-lookup"><span data-stu-id="64512-154">Additionally, in the **Dimension based matrix** view, more actions can be performed to help boost a store associate's productivity.</span></span> <span data-ttu-id="64512-155">Järgmisena on toodud mõned näited.</span><span class="sxs-lookup"><span data-stu-id="64512-155">Here are some examples:</span></span>

- <span data-ttu-id="64512-156">Muutke kaupluse asukohta, et vaadata varude saadavust kõigi tootevariantide korral muudes asukohtades.</span><span class="sxs-lookup"><span data-stu-id="64512-156">Change the store location to look up the inventory availability of all product variants at other locations.</span></span> <span data-ttu-id="64512-157">Need asukohad hõlmavad teisi kauplusi kaupluselokaatori grupis ja jaotuskeskuseid vaiketüübiga **Standardne**.</span><span class="sxs-lookup"><span data-stu-id="64512-157">These locations include other stores in the store locator group and distribution centers of the **Standard** default type.</span></span>
- <span data-ttu-id="64512-158">Müüge üksik tootevariant kliendile, kasutades sularaha, kauplusesse järeletulemist või saatmist aadressile.</span><span class="sxs-lookup"><span data-stu-id="64512-158">Sell an individual product variant to a customer by using cash and carry, in-store pickup, or shipment to an address.</span></span>
- <span data-ttu-id="64512-159">Andke kliendile ATP teave üksiku tootevariandi kohta kindlas asukohas.</span><span class="sxs-lookup"><span data-stu-id="64512-159">Provide the customer with ATP information for an individual product variant at a specific location.</span></span>

![Täiendavad toimingud variandi paanidega](media/VariantActions.png)

> [!NOTE]
> <span data-ttu-id="64512-161">Eelmises näites on dimensioonide kuvamisjärjestus alfabeetiline, sest dimensioonide kuvamisjärjestust ei konfigureeritud valitud toote jaoks.</span><span class="sxs-lookup"><span data-stu-id="64512-161">In the preceding illustration, the display order of the dimensions is alphabetic, because the display order of dimensions wasn't configured for the selected product.</span></span>

<span data-ttu-id="64512-162">Järgnevast tabelist leiate lisateavet võimalike lisatoimingute kohta.</span><span class="sxs-lookup"><span data-stu-id="64512-162">The following table provides more information about the additional actions that are available.</span></span>

| <span data-ttu-id="64512-163">Tegevus</span><span class="sxs-lookup"><span data-stu-id="64512-163">Action</span></span>               | <span data-ttu-id="64512-164">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="64512-164">Description</span></span> |
|----------------------|-------------|
| <span data-ttu-id="64512-165">Müü kohe</span><span class="sxs-lookup"><span data-stu-id="64512-165">Sell now</span></span>             | <span data-ttu-id="64512-166">Lisage valitud kaubavariant kandele ja suunake kasutaja kandekuvale.</span><span class="sxs-lookup"><span data-stu-id="64512-166">Add the selected item variant to the transaction, and redirect the user to the transaction screen.</span></span> <span data-ttu-id="64512-167">(See toiming pole saadaval, kui valitud asukoht on jaotuskeskus.)</span><span class="sxs-lookup"><span data-stu-id="64512-167">(This action isn't available when the selected location is a distribution center.)</span></span> |
| <span data-ttu-id="64512-168">Kauplusesse järeletulemine</span><span class="sxs-lookup"><span data-stu-id="64512-168">Pick up in store</span></span>     | <span data-ttu-id="64512-169">Looge klienditellimus tootevariandi jaoks, millele tullakse valitud asukohta järele, ja suunakse kasutaja kandekuvale.</span><span class="sxs-lookup"><span data-stu-id="64512-169">Create a customer order for the product variant that will be picked up from the selected location, and redirect the user to the transaction screen.</span></span> <span data-ttu-id="64512-170">(See toiming pole saadaval, kui valitud asukoht on jaotuskeskus.)</span><span class="sxs-lookup"><span data-stu-id="64512-170">(This action isn't available when the selected location is a distribution center.)</span></span> |
| <span data-ttu-id="64512-171">Toote lähetus</span><span class="sxs-lookup"><span data-stu-id="64512-171">Ship product</span></span>         | <span data-ttu-id="64512-172">Looge klienditellimus tootevariandi jaoks, mis saadetakse valitud asukohast, ja suunakse kasutaja kandekuvale.</span><span class="sxs-lookup"><span data-stu-id="64512-172">Create a customer order for the product variant that will be shipped from the selected location, and redirect the user to the transaction screen.</span></span> |
| <span data-ttu-id="64512-173">Kättesaadavus</span><span class="sxs-lookup"><span data-stu-id="64512-173">Availability</span></span>         | <span data-ttu-id="64512-174">Näidake ATP teavet valitud variandi kombinatsiooni kohta valitud asukoha jaoks.</span><span class="sxs-lookup"><span data-stu-id="64512-174">Show the ATP information for the selected variant combination for the selected location.</span></span> |
| <span data-ttu-id="64512-175">Kõigi asukohtade kuvamine</span><span class="sxs-lookup"><span data-stu-id="64512-175">Show all locations</span></span>   | <span data-ttu-id="64512-176">Valige standardne varudest otsimise vaade ja tõstke esile varude saadavuse teave kaubavariandi kohta kõigis kauplustes kaupluselokaatori grupis ja ka jaotuskeskustes, mille tüüp on **Standardne/Vaikimisi**.</span><span class="sxs-lookup"><span data-stu-id="64512-176">Switch to the standard inventory lookup view, and highlight inventory availability information for the item variant across all stores in the store locator group, and also in distribution centers of the **Standard/Default** type.</span></span> |
| <span data-ttu-id="64512-177">Kuva toote üksikasjad</span><span class="sxs-lookup"><span data-stu-id="64512-177">View product details</span></span> | <span data-ttu-id="64512-178">Suunake kasutaja seostatud tooteetaloni lehele **Toote üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="64512-178">Redirect the user to the **Product details** page of the associated product master.</span></span> |


[!INCLUDE[footer-include](../includes/footer-banner.md)]