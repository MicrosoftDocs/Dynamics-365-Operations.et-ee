---
title: Varude saadavus topeltkirjutuses
description: Selles teemas saate teada, kuidas kontrollida varude saadavust topeltkirjutuses.
author: yijialuan
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: riluan
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-05-26
ms.openlocfilehash: a7bfe998d2d787203a507a831c171fc43b03fedc
ms.sourcegitcommit: cc9921295f26804259cc9ec5137788ec9f2a4c6f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/08/2021
ms.locfileid: "4839545"
---
# <a name="inventory-availability-in-dual-write"></a><span data-ttu-id="a52c5-103">Varude saadavus topeltkirjutuses</span><span class="sxs-lookup"><span data-stu-id="a52c5-103">Inventory availability in dual-write</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a52c5-104">Varude saadavuse abil saate kontrollida oma varusid enne, kui lisate toote rakenduses Microsoft Dynamics 365 Sales lehtedele **Pakkumised**, **Tellimused** või **Arved**.</span><span class="sxs-lookup"><span data-stu-id="a52c5-104">By using inventory availability, you can check your inventory before you add a product to the **Quotations**, **Orders**, or **Invoices** page in Microsoft Dynamics 365 Sales.</span></span> <span data-ttu-id="a52c5-105">Näiteks kontrollite te protsessi [potentsiaalne klient sularahaks](dual-write-prospect-to-cash.md) käigus ühe olulise ülesandena varusid ja määrate täitmiskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="a52c5-105">For example, you check inventory and determine a fulfillment date as one key task in the [prospect-to-cash](dual-write-prospect-to-cash.md) process.</span></span>

<span data-ttu-id="a52c5-106">Kui teil puuduvad piisavad varud, siis saate eeldatava varude vastuvõtu ja väljastamise alusel tarneaega prognoosida.</span><span class="sxs-lookup"><span data-stu-id="a52c5-106">If you don't have enough inventory, you can estimate a delivery date, based on projected inventory receipts and issues.</span></span> <span data-ttu-id="a52c5-107">Samuti saate kontrollida lubamiseks saadaval (ATP) toote teavet, kust leiate lubamiseks saadaval koguse eelmääratletud ajavahemiku raames.</span><span class="sxs-lookup"><span data-stu-id="a52c5-107">You can also check the product's available-to-promise (ATP) information, where you can find the ATP quantity in the predefined time fence.</span></span>

## <a name="on-hand-inventory"></a><span data-ttu-id="a52c5-108">Vaba kaubavaru</span><span class="sxs-lookup"><span data-stu-id="a52c5-108">On-hand inventory</span></span>

<span data-ttu-id="a52c5-109">Rakenduses Dynamics 365 Sales on lehtede **Pakkumised**, **Tellimused** ja **Arved** päisesse lisatud uus nupp **Vaba kaubavaru**.</span><span class="sxs-lookup"><span data-stu-id="a52c5-109">In Dynamics 365 Sales, a new **On-hand Inventory** button has been added to the header of the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="a52c5-110">Nupule klõpsates ilmub dialoogiboks, kus saate määratleda ettevõtte ja toote, mille puhul soovite kontrollida vaba kaubavaru.</span><span class="sxs-lookup"><span data-stu-id="a52c5-110">When you select this button, a dialog box appears, where you can specify the company and the product that you want to check the on-hand inventory for.</span></span> <span data-ttu-id="a52c5-111">Selles dialoogiboksis kuvatav teave ühtib teemas [Vaba kaubavaru](../../../../supply-chain/inventory/tasks/check-availability-stock.md) kirjeldatud teabega.</span><span class="sxs-lookup"><span data-stu-id="a52c5-111">This dialog box shows the same information as [On-hand inventory](../../../../supply-chain/inventory/tasks/check-availability-stock.md).</span></span>

<span data-ttu-id="a52c5-112">Dialoogiboksis kuvatakse Dynamics 365 Supply Chain Managementist pärit teavet varude kohta.</span><span class="sxs-lookup"><span data-stu-id="a52c5-112">The dialog box returns the inventory information from Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="a52c5-113">See teave sisaldab järgmiseid koguseid.</span><span class="sxs-lookup"><span data-stu-id="a52c5-113">This information includes the following quantities:</span></span>

- <span data-ttu-id="a52c5-114">Laos olev kogus</span><span class="sxs-lookup"><span data-stu-id="a52c5-114">On-hand quantity</span></span>
- <span data-ttu-id="a52c5-115">Reserveeritud laos olev kogus</span><span class="sxs-lookup"><span data-stu-id="a52c5-115">Reserved on-hand quantity</span></span>
- <span data-ttu-id="a52c5-116">Saadaolev laos olev kogus</span><span class="sxs-lookup"><span data-stu-id="a52c5-116">Available on-hand quantity</span></span>
- <span data-ttu-id="a52c5-117">Tellitud kogus</span><span class="sxs-lookup"><span data-stu-id="a52c5-117">Ordered quantity</span></span>
- <span data-ttu-id="a52c5-118">Tellimisel kogus</span><span class="sxs-lookup"><span data-stu-id="a52c5-118">On-order quantity</span></span>
- <span data-ttu-id="a52c5-119">Reserveeritud tellitud kogus</span><span class="sxs-lookup"><span data-stu-id="a52c5-119">Reserved ordered quantity</span></span>
- <span data-ttu-id="a52c5-120">Saadaolev kogus kokku</span><span class="sxs-lookup"><span data-stu-id="a52c5-120">Total available quantity</span></span>

## <a name="atp-information"></a><span data-ttu-id="a52c5-121">ATP teave</span><span class="sxs-lookup"><span data-stu-id="a52c5-121">ATP information</span></span>

<span data-ttu-id="a52c5-122">Rakenduses Sales on lisatud lehtede **Pakkumised**, **Tellimused** ja **Arved** reakaupadele uus nupp **ATP teave**.</span><span class="sxs-lookup"><span data-stu-id="a52c5-122">In Sales, a new **ATP Information** button has been added to line items on the **Quotes**, **Orders**, and **Invoices** pages.</span></span> <span data-ttu-id="a52c5-123">Nupule klõpsates ilmub dialoogiboks, kus saate määratleda ettevõtte, toote, varude saidi, varude lao ja tellimuse koguse.</span><span class="sxs-lookup"><span data-stu-id="a52c5-123">When you select this button, a dialog box appears, where you can specify the company, product, inventory site, inventory warehouse, and order quantity.</span></span> <span data-ttu-id="a52c5-124">Selle dialoogiboksi sätted ühtivad teemas [Tellimuse lubamine](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations) kirjeldatutega.</span><span class="sxs-lookup"><span data-stu-id="a52c5-124">This dialog box has the same settings that are described in [Order promising](../../../../supply-chain/sales-marketing/delivery-dates-available-promise-calculations.md#atp-calculations).</span></span>

<span data-ttu-id="a52c5-125">Dialoogiboksis kuvatakse Supply Chain Managementist pärit ATP teave.</span><span class="sxs-lookup"><span data-stu-id="a52c5-125">The dialog box returns the ATP information from Supply Chain Management.</span></span> <span data-ttu-id="a52c5-126">See teave sisaldab järgmiseid koguseid.</span><span class="sxs-lookup"><span data-stu-id="a52c5-126">This information includes the following quantities:</span></span>

- <span data-ttu-id="a52c5-127">ATP kogus</span><span class="sxs-lookup"><span data-stu-id="a52c5-127">ATP quantity</span></span>
- <span data-ttu-id="a52c5-128">Sissetuleku kogus</span><span class="sxs-lookup"><span data-stu-id="a52c5-128">Receipt quantity</span></span>
- <span data-ttu-id="a52c5-129">Väljamineku kogus</span><span class="sxs-lookup"><span data-stu-id="a52c5-129">Issue quantity</span></span>
- <span data-ttu-id="a52c5-130">Laos olev kogus</span><span class="sxs-lookup"><span data-stu-id="a52c5-130">On-hand quantity</span></span>

## <a name="how-it-works"></a><span data-ttu-id="a52c5-131">Toimimisviis</span><span class="sxs-lookup"><span data-stu-id="a52c5-131">How it works</span></span>

<span data-ttu-id="a52c5-132">Kui valite **Pakkumised**, **Tellimused** või **Arved** nupu **Vaba kaubavaru**, tehakse **vaba kaubavaru** API-le reaalajas topeltkirjutuse kutse.</span><span class="sxs-lookup"><span data-stu-id="a52c5-132">When you select the **On-hand Inventory** button on the **Quotes**, **Orders**, or **Invoices** page, a live dual-write call is made to the **Onhand inventory** API.</span></span> <span data-ttu-id="a52c5-133">API arvutab selle toote vaba kaubavaru.</span><span class="sxs-lookup"><span data-stu-id="a52c5-133">The API calculates the on-hand inventory for the given product.</span></span> <span data-ttu-id="a52c5-134">Tulemus talletatakse tabelites **InventCDSInventoryOnHandRequestEntity** ja **InventCDSInventoryOnHandEntryEntity** ning seejärel kirjutatakse see topeltkirjutuse abil Dataverse’i.</span><span class="sxs-lookup"><span data-stu-id="a52c5-134">The result is stored in the **InventCDSInventoryOnHandRequestEntity** and **InventCDSInventoryOnHandEntryEntity** tables, and then is written to Dataverse by dual-write.</span></span> <span data-ttu-id="a52c5-135">Selle funktsiooni kasutamiseks peate käivitama järgmised topeltkirjutuse kaardid.</span><span class="sxs-lookup"><span data-stu-id="a52c5-135">To use this functionality, you need to run the following dual-write maps.</span></span> <span data-ttu-id="a52c5-136">Jätke kaartide käivitamisel esialgne sünkroonimine vahele.</span><span class="sxs-lookup"><span data-stu-id="a52c5-136">Skip initial synchronization when you run the maps.</span></span>

- <span data-ttu-id="a52c5-137">CDS-i vaba kaubavaru kirjed (msdyn_inventoryonhandentries)</span><span class="sxs-lookup"><span data-stu-id="a52c5-137">CDS inventory on-hand entries (msdyn_inventoryonhandentries)</span></span>
- <span data-ttu-id="a52c5-138">CDS-i vaba kaubavaru taotlused (msdyn_inventoryonhandrequests)</span><span class="sxs-lookup"><span data-stu-id="a52c5-138">CDS inventory on-hand requests (msdyn_inventoryonhandrequests)</span></span>

## <a name="templates"></a><span data-ttu-id="a52c5-139">Mallid</span><span class="sxs-lookup"><span data-stu-id="a52c5-139">Templates</span></span>
<span data-ttu-id="a52c5-140">Vaba kaubavaru andmete näitamiseks on saadaval järgmised mallid.</span><span class="sxs-lookup"><span data-stu-id="a52c5-140">The following templates are available for the exposing the onhand inventory data.</span></span>

<span data-ttu-id="a52c5-141">Finance and Operations rakendused</span><span class="sxs-lookup"><span data-stu-id="a52c5-141">Finance and Operations apps</span></span> | <span data-ttu-id="a52c5-142">Klientide kaasamise rakendus</span><span class="sxs-lookup"><span data-stu-id="a52c5-142">Customer engagement app</span></span> | <span data-ttu-id="a52c5-143">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="a52c5-143">Description</span></span> 
---|---|---
[<span data-ttu-id="a52c5-144">CDS-i vaba kaubavaru kirjed</span><span class="sxs-lookup"><span data-stu-id="a52c5-144">CDS inventory on-hand entries</span></span>](#145) | <span data-ttu-id="a52c5-145">msdyn_inventoryonhandentries</span><span class="sxs-lookup"><span data-stu-id="a52c5-145">msdyn_inventoryonhandentries</span></span> |
[<span data-ttu-id="a52c5-146">CDS-i vaba kaubavaru kirjete taotlused</span><span class="sxs-lookup"><span data-stu-id="a52c5-146">CDS inventory on-hand requests</span></span>](#147) | <span data-ttu-id="a52c5-147">msdyn_inventoryonhandrequests</span><span class="sxs-lookup"><span data-stu-id="a52c5-147">msdyn_inventoryonhandrequests</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

###  <a name="cds-inventory-on-hand-entries-msdyn_inventoryonhandentries"></a><a name="145"></a><span data-ttu-id="a52c5-148">CDS-i vaba kaubavaru kirjed (msdyn_inventoryonhandentries)</span><span class="sxs-lookup"><span data-stu-id="a52c5-148">CDS inventory on-hand entries (msdyn_inventoryonhandentries)</span></span>

<span data-ttu-id="a52c5-149">See mall sünkroonib andmeid rakenduste Finance and Operations ja Dataverse'i vahel.</span><span class="sxs-lookup"><span data-stu-id="a52c5-149">This template synchronizes data between Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="a52c5-150">Finance and Operationsi väli</span><span class="sxs-lookup"><span data-stu-id="a52c5-150">Finance and Operations field</span></span> | <span data-ttu-id="a52c5-151">Kaardi tüüp</span><span class="sxs-lookup"><span data-stu-id="a52c5-151">Map type</span></span> | <span data-ttu-id="a52c5-152">Klientide kaasamise väli</span><span class="sxs-lookup"><span data-stu-id="a52c5-152">Customer engagement field</span></span> | <span data-ttu-id="a52c5-153">Vaikeväärtus</span><span class="sxs-lookup"><span data-stu-id="a52c5-153">Default value</span></span>
---|---|---|---
`REQUESTID` | = | `msdyn_request.msdyn_requestid` |
`INVENTORYSITEID` | = | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | = | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`AVAILABLEONHANDQUANTITY` | > | `msdyn_availableonhandquantity` |
`AVAILABLEORDEREDQUANTITY` | > | `msdyn_availableorderedquantity` |
`ONHANDQUANTITY` | > | `msdyn_onhandquantity` |
`ONORDERQUANTITY` | > | `msdyn_onorderquantity` |
`ORDEREDQUANTITY` | > | `msdyn_orderedquantity` |
`RESERVEDONHANDQUANTITY` | > | `msdyn_reservedonhandquantity` |
`RESERVEDORDEREDQUANTITY` | > | `msdyn_reservedorderedquantity` |
`TOTALAVAILABLEQUANTITY` | > | `msdyn_totalavailablequantity` |
`ATPDATE` | = | `msdyn_atpdate` |
`ATPQUANTITY` | > | `msdyn_atpquantity` |
`PROJECTEDISSUEQUANTITY` | > | `msdyn_projectedissuequantity` |
`PROJECTEDONHANDQUANTITY` | > | `msdyn_projectedonhandquantity` |
`PROJECTEDRECEIPTQUANTITY` | > | `msdyn_projectedreceiptquantity` |
`ORDERQUANTITY` | > | `msdyn_orderquantity` |
`UNAVAILABLEONHANDQUANTITY` | > | `msdyn_unavailableonhandquantity` |

###  <a name="cds-inventory-on-hand-requests-msdyn_inventoryonhandrequests"></a><a name="147"></a><span data-ttu-id="a52c5-154">CDS-i vaba kaubavaru taotlused (msdyn_inventoryonhandrequests)</span><span class="sxs-lookup"><span data-stu-id="a52c5-154">CDS inventory on-hand requests (msdyn_inventoryonhandrequests)</span></span>

<span data-ttu-id="a52c5-155">See mall sünkroonib andmeid rakenduste Finance and Operations ja Dataverse'i vahel.</span><span class="sxs-lookup"><span data-stu-id="a52c5-155">This template synchronizes data between Finance and Operations apps and Dataverse.</span></span>

<span data-ttu-id="a52c5-156">Finance and Operationsi väli</span><span class="sxs-lookup"><span data-stu-id="a52c5-156">Finance and Operations field</span></span> | <span data-ttu-id="a52c5-157">Kaardi tüüp</span><span class="sxs-lookup"><span data-stu-id="a52c5-157">Map type</span></span> | <span data-ttu-id="a52c5-158">Klientide kaasamise väli</span><span class="sxs-lookup"><span data-stu-id="a52c5-158">Customer engagement field</span></span> | <span data-ttu-id="a52c5-159">Vaikeväärtus</span><span class="sxs-lookup"><span data-stu-id="a52c5-159">Default value</span></span>
---|---|---|---
`REQUESTID` | = | `msdyn_requestid` |
`PRODUCTNUMBER` | < | `msdyn_product.msdyn_productnumber` |
`ISATPCALCULATION` | << | `msdyn_isatpcalculation` |
`ORDERQUANTITY` | < | `msdyn_orderquantity` |
`INVENTORYSITEID` | < | `msdyn_inventorysite.msdyn_siteid` |
`INVENTORYWAREHOUSEID` | < | `msdyn_inventorywarehouse.msdyn_warehouseidentifier` |
`REFERENCENUMBER` | < | `msdyn_referencenumber` |
`LINECREATIONSEQUENCENUMBER` | < | `msdyn_linecreationsequencenumber` |




