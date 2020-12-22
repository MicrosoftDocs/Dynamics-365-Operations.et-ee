---
title: Hajutatud tellimuste haldamise (DOM) kulukonfiguratsioon
description: Selles teemas kirjeldatakse Dynamics 365 Commercei hajutatud tellimuste haldamise (DOM) funktsiooni kulukonfiguratsiooni.
author: josaw1
manager: AnnBe
ms.date: 12/05/2018
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-12-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: 7644cb9800a418fd123b32a0257b787277fcb19f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4458814"
---
# <a name="cost-configuration-for-distributed-order-management-dom"></a><span data-ttu-id="9f46a-103">Hajutatud tellimuste haldamise (DOM) kulukonfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="9f46a-103">Cost configuration for distributed order management (DOM)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9f46a-104">Organisatsioonid kasutavad tellimuse täitmise alusena kasutatava optimaalse asukoha määratlemiseks mitut kulukomponenti.</span><span class="sxs-lookup"><span data-stu-id="9f46a-104">Organizations consider multiple cost components to determine the optimal location to fulfill an order from.</span></span> <span data-ttu-id="9f46a-105">Mõned neist kulukomponentidest on lähetuskulu, käsitluskulu ja pakenduskulu.</span><span class="sxs-lookup"><span data-stu-id="9f46a-105">Some of these cost components are shipping cost, handling cost, and packaging cost.</span></span> <span data-ttu-id="9f46a-106">Täitmisasukoha määratlemiseks arvutatakse nende kulude kombinatsioon.</span><span class="sxs-lookup"><span data-stu-id="9f46a-106">A combination of these costs is calculated to determine the fulfillment location.</span></span>

<span data-ttu-id="9f46a-107">Kui Dynamics 365 Commercei hajutatud tellimuste haldamise (DOM) esimene iteratsioon optimeeris tellimuste määramist täitmisasukohtadele, võttis see arvesse ainult vahemaad.</span><span class="sxs-lookup"><span data-stu-id="9f46a-107">When the first iteration of distributed order management (DOM) in Dynamics 365 Commerce optimized the assignment of orders to fulfillment locations, it factored in distance only.</span></span> <span data-ttu-id="9f46a-108">Kuigi vahemaa saab olla kuluga vastastikuses seoses, pole see siiski sama mis kulu.</span><span class="sxs-lookup"><span data-stu-id="9f46a-108">Although distance can be correlated with cost, it isn't the same as cost.</span></span> <span data-ttu-id="9f46a-109">Näiteks maksab öine saatmisviis rohkem kui sama vahemaaga kolmepäevane või seitsmepäevane tarne.</span><span class="sxs-lookup"><span data-stu-id="9f46a-109">For example, an overnight shipping method costs more than three-day shipping or seven-day shipping over the same distance.</span></span>

<span data-ttu-id="9f46a-110">Kulukonfiguratsiooni funktsioon võimaldab jaemüüjatel määratleda ja konfigureerida täiendavad kulukomponendid, mis arvutatakse ja mida võetakse arvesse selleks, et määratled tellimuseridade täitmiseks alusena kasutatav optimaalne asukoht.</span><span class="sxs-lookup"><span data-stu-id="9f46a-110">The cost configuration feature lets retailers define and configure additional cost components that will be calculated and factored in to determine the optimal location to fulfill order lines from.</span></span>

<span data-ttu-id="9f46a-111">Kui kulukomponendi on konfigureeritud, kasutab DOM-i solver tellimuse täitmise jaoks optimaalse asukoha määratlemiseks ainult neid kulumääratlusi.</span><span class="sxs-lookup"><span data-stu-id="9f46a-111">When cost components are configured, the DOM solver uses only those cost definitions to determine the optimal location for order fulfillment.</span></span> <span data-ttu-id="9f46a-112">See ei võta kuluna arvesse vahemaakomponenti.</span><span class="sxs-lookup"><span data-stu-id="9f46a-112">It doesn't consider the distance component as a cost.</span></span> <span data-ttu-id="9f46a-113">Kui kulukomponente pole aga konfigureeritud, kasutab DOM-i solver tellimuse täitmise jaoks optimaalse asukoha määratlemiseks kuluna vahemaakomponenti.</span><span class="sxs-lookup"><span data-stu-id="9f46a-113">However, if no cost components are configured, the DOM solver does use the distance component as a cost to determine the optimal location for order fulfillment.</span></span>

## <a name="set-up-cost-components"></a><span data-ttu-id="9f46a-114">Kulukomponentide seadistamine</span><span class="sxs-lookup"><span data-stu-id="9f46a-114">Set up cost components</span></span>

<span data-ttu-id="9f46a-115">Süsteemis saab määratleda kaks olulist kulukomponenti: **Lähetamine** ja **Muud**.</span><span class="sxs-lookup"><span data-stu-id="9f46a-115">Two major cost component types can be defined in the system: **Shipping** and **Other**.</span></span>

<span data-ttu-id="9f46a-116">Mõlemad kulukomponenditüübid toetavad mitut arvutusbaasi, nagu on näha järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="9f46a-116">Both cost component types support multiple calculation bases, as shown in the following table.</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="9f46a-117">Kulukomponendi tüüp</span><span class="sxs-lookup"><span data-stu-id="9f46a-117">Cost component type</span></span></th>
<th><span data-ttu-id="9f46a-118">Arvutuse alus</span><span class="sxs-lookup"><span data-stu-id="9f46a-118">Calculation basis</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="9f46a-119">Lähetamine</span><span class="sxs-lookup"><span data-stu-id="9f46a-119">Shipping</span></span></td>
<td>
<ul>
<li><span data-ttu-id="9f46a-120">Lihtne</span><span class="sxs-lookup"><span data-stu-id="9f46a-120">Simple</span></span></li>
<li><span data-ttu-id="9f46a-121">Astmeline</span><span class="sxs-lookup"><span data-stu-id="9f46a-121">Tiered</span></span></li>
</ul>
</td>
</tr>
<tr>
<td><span data-ttu-id="9f46a-122">Muud</span><span class="sxs-lookup"><span data-stu-id="9f46a-122">Other</span></span></td>
<td>
<ul>
<li><span data-ttu-id="9f46a-123">Müügitellimus</span><span class="sxs-lookup"><span data-stu-id="9f46a-123">Sales order</span></span></li>
<li><span data-ttu-id="9f46a-124">Müügirida</span><span class="sxs-lookup"><span data-stu-id="9f46a-124">Sales line</span></span></li>
<li><span data-ttu-id="9f46a-125">Koht</span><span class="sxs-lookup"><span data-stu-id="9f46a-125">Location</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

### <a name="shipping-cost-component-type"></a><span data-ttu-id="9f46a-126">Kulukomponendi tüüp Lähetamine</span><span class="sxs-lookup"><span data-stu-id="9f46a-126">Shipping cost component type</span></span>

<span data-ttu-id="9f46a-127">Selles jaotises selgitatakse, seadistada kulukomponendi tüübi **Lähetamine** ja lähetuskulude arvutuse aluse kombinatsioone.</span><span class="sxs-lookup"><span data-stu-id="9f46a-127">This section explains how to set up each combination of the **Shipping** cost component type and a calculation basis for shipping costs.</span></span> <span data-ttu-id="9f46a-128">Lisaks selgitatakse, kuidas kasutab DOM-i solver iga kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="9f46a-128">It also explains how the DOM solver uses each combination.</span></span>

#### <a name="cost-component-type--shipping-and-calculation-basis--simple"></a><span data-ttu-id="9f46a-129">Kulukomponendi tüüp = lähetamine; arvutuse alus = lihtne</span><span class="sxs-lookup"><span data-stu-id="9f46a-129">Cost component type = Shipping and Calculation basis = Simple</span></span>

<span data-ttu-id="9f46a-130">Kulukomponendi tüübi **Lähetamine** ja arvutuse aluse **Lihtne** kombinatsiooni kasutades põhineb tarneviisi lähetuskulu kas fikseeritud kulul või vahemaal.</span><span class="sxs-lookup"><span data-stu-id="9f46a-130">If a combination of the **Shipping** cost component type and the **Simple** calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</span></span>

<span data-ttu-id="9f46a-131">Selle kombinatsiooni jaoks peate seadistama järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="9f46a-131">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="9f46a-132">**Kulutegur** – sisestage kuluteguri kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="9f46a-132">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="9f46a-133">**Kirjeldus** – sisestage kuluteguri nimi ja kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="9f46a-133">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="9f46a-134">**Alguskuupäev** ja **Lõppkuupäev** – saate neid välju kasutada kuluteguri piiramiseks konkreetse kuupäevavahemikuga.</span><span class="sxs-lookup"><span data-stu-id="9f46a-134">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="9f46a-135">Kui jätate need väljad tühjaks, kehtib kulutegur määramata perioodi jooksul.</span><span class="sxs-lookup"><span data-stu-id="9f46a-135">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="9f46a-136">**Aktiivne** – näidake, kas kulutegur on aktiivne.</span><span class="sxs-lookup"><span data-stu-id="9f46a-136">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="9f46a-137">DOM võtab arvesse ainult aktiivseid täitmisprofiiliga seostatud kulutegureid.</span><span class="sxs-lookup"><span data-stu-id="9f46a-137">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="9f46a-138">**Ettevõte** – määrake juriidiline isik, mille jaoks kulutegur konfigureeritakse.</span><span class="sxs-lookup"><span data-stu-id="9f46a-138">**Company** – Specify the legal entity that the cost factor is configured for.</span></span> <span data-ttu-id="9f46a-139">Kõik arvutuskriteeriumite read peavad olema ette nähtud sama juriidilise isiku jaoks.</span><span class="sxs-lookup"><span data-stu-id="9f46a-139">All lines of the calculation criteria must be for the same legal entity.</span></span>
- <span data-ttu-id="9f46a-140">**Tarneviisid** – määrake tarneviisid, mille jaoks kulu konfigureeritakse.</span><span class="sxs-lookup"><span data-stu-id="9f46a-140">**Modes of delivery** – Specify the modes of delivery that the cost is configured for.</span></span>
- <span data-ttu-id="9f46a-141">**Arvutustüüp** – määrake, kuidas tuleb kulu konkreetse tarneviisi jaoks arvutada.</span><span class="sxs-lookup"><span data-stu-id="9f46a-141">**Calculation type** – Specify how the cost should be calculated for a specific mode of delivery.</span></span> <span data-ttu-id="9f46a-142">Toetatakse kaht arvutustüüpi.</span><span class="sxs-lookup"><span data-stu-id="9f46a-142">Two calculation types are supported:</span></span>

    - <span data-ttu-id="9f46a-143">**Fikseeritud** – tarneviisi jaoks kasutataks fikseeritud kulu.</span><span class="sxs-lookup"><span data-stu-id="9f46a-143">**Fixed** – A flat cost is used for the mode of delivery.</span></span> <span data-ttu-id="9f46a-144">Kui valite selle arvutustüübi, määratleb väli **Kulu** fikseeritud kulu.</span><span class="sxs-lookup"><span data-stu-id="9f46a-144">If you select this calculation type, the **Cost** field defines the flat cost.</span></span>
    - <span data-ttu-id="9f46a-145">**Vahemaaühiku kohta** – tarneviisi kulu arvutamiseks korrutatakse väljal **Kulu** määratud kuluväärtus tarneaadressi ja asukohtade vahelise vahemaaga.</span><span class="sxs-lookup"><span data-stu-id="9f46a-145">**Per-distance unit** – The cost for the mode of delivery is calculated as the cost value that is specified in the **Cost** field times the distance between the delivery address and the locations.</span></span>

- <span data-ttu-id="9f46a-146">**Kulu** – määrake kuluväärtus, mida kasutatakse koos väljaga **Arvutuse tüüp** tarneviisi kulu arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="9f46a-146">**Cost** – Specify the cost value that is used in conjunction with the **Calculation type** field to compute the cost for a mode of delivery.</span></span>

#### <a name="cost-component-type--shipping-and-calculation-basis--tiered"></a><span data-ttu-id="9f46a-147">Kulukomponendi tüüp = lähetamine; arvutuse alus = astmeline</span><span class="sxs-lookup"><span data-stu-id="9f46a-147">Cost component type = Shipping and Calculation basis = Tiered</span></span>

<span data-ttu-id="9f46a-148">Kulukomponendi tüübi **Lähetamine** ja arvutuse aluse **Astmeline** kombinatsiooni kasutades põhineb tarneviisi lähetuskulu kas fikseeritud kulul või vahemaal.</span><span class="sxs-lookup"><span data-stu-id="9f46a-148">If a combination of the **Shipping** cost component type and the **Tiered** calculation basis is used, the shipping cost for a mode of delivery is based on either a flat cost or distance.</span></span> <span data-ttu-id="9f46a-149">Selles kombinatsioonis põhineb vahemaa vahemaade astmelisel vahemikul.</span><span class="sxs-lookup"><span data-stu-id="9f46a-149">However, in this combination, the distance is based on a tiered range of distances.</span></span>

<span data-ttu-id="9f46a-150">Selle kombinatsiooni jaoks peate seadistama järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="9f46a-150">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="9f46a-151">**Kulutegur** – sisestage kuluteguri kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="9f46a-151">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="9f46a-152">**Kirjeldus** – sisestage kuluteguri nimi ja kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="9f46a-152">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="9f46a-153">**Vaikekulu** – määrake kulu, mida tuleks kasutada tarneviisi puhul, kui vahemaa tarneaadressi ja asukoha vahel ei lange kokku tarneviisi ühegi astmelise vahemaaga.</span><span class="sxs-lookup"><span data-stu-id="9f46a-153">**Default cost** – Specify the cost that should be used for a mode of delivery if the distance between the delivery address and the location doesn't fall into any of the tiered distances for the mode of delivery.</span></span>
- <span data-ttu-id="9f46a-154">**Alguskuupäev** ja **Lõppkuupäev** – saate neid välju kasutada kuluteguri piiramiseks konkreetse kuupäevavahemikuga.</span><span class="sxs-lookup"><span data-stu-id="9f46a-154">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="9f46a-155">Kui jätate need väljad tühjaks, kehtib kulutegur määramata perioodi jooksul.</span><span class="sxs-lookup"><span data-stu-id="9f46a-155">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="9f46a-156">**Aktiivne** – näidake, kas kulutegur on aktiivne.</span><span class="sxs-lookup"><span data-stu-id="9f46a-156">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="9f46a-157">DOM võtab arvesse ainult aktiivseid täitmisprofiiliga seostatud kulutegureid.</span><span class="sxs-lookup"><span data-stu-id="9f46a-157">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="9f46a-158">**Ettevõte** – määrake juriidiline isik, mille jaoks kulutegur konfigureeritakse.</span><span class="sxs-lookup"><span data-stu-id="9f46a-158">**Company** – Specify the legal entity that the cost factor is configured for.</span></span> <span data-ttu-id="9f46a-159">Kõik arvutuskriteeriumite read peavad olema ette nähtud sama juriidilise isiku jaoks.</span><span class="sxs-lookup"><span data-stu-id="9f46a-159">All lines of the calculation criteria must be for the same legal entity.</span></span>
- <span data-ttu-id="9f46a-160">**Tarneviisid** – määrake tarneviisid, mille jaoks kulu konfigureeritakse.</span><span class="sxs-lookup"><span data-stu-id="9f46a-160">**Modes of delivery** – Specify the modes of delivery that the cost is configured for.</span></span>
- <span data-ttu-id="9f46a-161">**Vahemaa tüüp** – määrake, kas astmelise vahemaa määratlus on vahemaa linnulennul või mööda maad mõõdetav vahemaa.</span><span class="sxs-lookup"><span data-stu-id="9f46a-161">**Distance type** – Specify whether the tiered distance definition is an aerial distance or a road distance.</span></span>
- <span data-ttu-id="9f46a-162">**Vahemaaühikud** – määrake ühik, milles astmelist vahemaad mõõdetakse.</span><span class="sxs-lookup"><span data-stu-id="9f46a-162">**Distance units** – Specify the unit that the tiered distance is measured in.</span></span>
- <span data-ttu-id="9f46a-163">**Vahemaa lähtekoht** – määrake astmelise vahemaa algvahemik.</span><span class="sxs-lookup"><span data-stu-id="9f46a-163">**Distance from** – Specify the start range for the tiered distance.</span></span>
- <span data-ttu-id="9f46a-164">**Vahemaa sihtkoht** – määrake astmelise vahemaa lõppvahemik.</span><span class="sxs-lookup"><span data-stu-id="9f46a-164">**Distance to** – Specify the end range for the tiered distance.</span></span>
- <span data-ttu-id="9f46a-165">**Arvutustüüp** – määrake, kuidas tuleb kulu konkreetse tarneviisi ja astmelise vahemaa jaoks arvutada.</span><span class="sxs-lookup"><span data-stu-id="9f46a-165">**Calculation type** – Specify how the cost should be calculated for a specific mode of delivery and tiered distance.</span></span> <span data-ttu-id="9f46a-166">Toetatakse kaht arvutustüüpi.</span><span class="sxs-lookup"><span data-stu-id="9f46a-166">Two calculation types are supported:</span></span>

    - <span data-ttu-id="9f46a-167">**Fikseeritud** – tarneviisi jaoks kasutataks fikseeritud kulu.</span><span class="sxs-lookup"><span data-stu-id="9f46a-167">**Fixed** – A flat cost is used for the mode of delivery.</span></span> <span data-ttu-id="9f46a-168">Kui valite selle arvutustüübi, määratleb väli **Kulu** fikseeritud kulu.</span><span class="sxs-lookup"><span data-stu-id="9f46a-168">If you select this calculation type, the **Cost** field defines the flat cost.</span></span>
    - <span data-ttu-id="9f46a-169">**Vahemaaühiku kohta** – tarneviisi ja astmelise vahemaa kulu arvutamiseks korrutatakse väljal **Kulu** määratud kuluväärtus tarneaadressi ja asukohtade vahelise vahemaaga.</span><span class="sxs-lookup"><span data-stu-id="9f46a-169">**Per distance unit** – The cost for the mode of delivery and tiered distance is calculated as the cost value that is specified in the **Cost** field times the distance between the delivery address and the locations.</span></span>

- <span data-ttu-id="9f46a-170">**Kulu** – määrake kuluväärtus, mida kasutatakse koos väljaga **Arvutuse tüüp** tarneviisi kulu arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="9f46a-170">**Cost** – Specify the cost value that is used in conjunction with the **Calculation type** field to compute the cost for a mode of delivery.</span></span>

> [!NOTE]
> - <span data-ttu-id="9f46a-171">Astmeliste vahemaade määratlemise korral kontrollib süsteem, ega kuskil pole puuduvaid ega kattuvaid vahemaid.</span><span class="sxs-lookup"><span data-stu-id="9f46a-171">When you define tiered distances, the system validates that there are no missing or overlapping distances.</span></span>
> - <span data-ttu-id="9f46a-172">Tarneviisi jaoks kasutatav vahemaatüüp peab olema kõigil astmelistel vahemaadel sama.</span><span class="sxs-lookup"><span data-stu-id="9f46a-172">The distance type that is used for a mode of delivery must be the same across all the tiered distances.</span></span>

### <a name="other-cost-component-type"></a><span data-ttu-id="9f46a-173">Muu kulukomponendi tüüp</span><span class="sxs-lookup"><span data-stu-id="9f46a-173">Other cost component type</span></span>

<span data-ttu-id="9f46a-174">Selles jaotises selgitatakse, seadistada lähetuskulude jaoks kulukomponendi tüübi **Muud** ja lähetamisega mitteseotud kulude muu kulutüübi kombinatsioone.</span><span class="sxs-lookup"><span data-stu-id="9f46a-174">This section explains how to set up each combination of the **Other** cost component type and an other cost type for non-shipping costs.</span></span> <span data-ttu-id="9f46a-175">Lisaks selgitatakse, kuidas kasutab DOM-i solver iga kombinatsiooni.</span><span class="sxs-lookup"><span data-stu-id="9f46a-175">It also explains how the DOM solver uses each combination.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--sales-order"></a><span data-ttu-id="9f46a-176">Kulukomponendi tüüp = muud; muu kulutüüp = müügitellimus</span><span class="sxs-lookup"><span data-stu-id="9f46a-176">Cost component type = Other and Other cost type = Sales order</span></span>

<span data-ttu-id="9f46a-177">Kulukomponendi tüübi **Muud** ja muu kulutüübi **Müügitellimus** kombinatsiooni kasutatakse lähetamisega mitteseotud kulude määratlemiseks müügitellimuse tasemel.</span><span class="sxs-lookup"><span data-stu-id="9f46a-177">A combination of the **Other** cost component type and the **Sales order** other cost type is used to define non-shipping costs at the sales order level.</span></span>

<span data-ttu-id="9f46a-178">Selle kombinatsiooni jaoks peate seadistama järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="9f46a-178">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="9f46a-179">**Kulutegur** – sisestage kuluteguri kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="9f46a-179">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="9f46a-180">**Kirjeldus** – sisestage kuluteguri nimi ja kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="9f46a-180">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="9f46a-181">**Alguskuupäev** ja **Lõppkuupäev** – saate neid välju kasutada kuluteguri piiramiseks konkreetse kuupäevavahemikuga.</span><span class="sxs-lookup"><span data-stu-id="9f46a-181">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="9f46a-182">Kui jätate need väljad tühjaks, kehtib kulutegur määramata perioodi jooksul.</span><span class="sxs-lookup"><span data-stu-id="9f46a-182">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="9f46a-183">**Aktiivne** – näidake, kas kulutegur on aktiivne.</span><span class="sxs-lookup"><span data-stu-id="9f46a-183">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="9f46a-184">DOM võtab arvesse ainult aktiivseid täitmisprofiiliga seostatud kulutegureid.</span><span class="sxs-lookup"><span data-stu-id="9f46a-184">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="9f46a-185">**Kulu** – määrake lähetamisega mitteseotud kulu kuluväärtus müügitellimuse tasemel.</span><span class="sxs-lookup"><span data-stu-id="9f46a-185">**Cost** – Specify the cost value for a non-shipping cost at the sales order level.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--sales-line"></a><span data-ttu-id="9f46a-186">Kulukomponendi tüüp = muud; muu kulutüüp = müügirida</span><span class="sxs-lookup"><span data-stu-id="9f46a-186">Cost component type = Other and Other cost type = Sales line</span></span>

<span data-ttu-id="9f46a-187">Kulukomponendi tüübi **Muud** ja muu kulutüübi **Müügirida** kombinatsiooni kasutatakse lähetamisega mitteseotud kulude määratlemiseks müügitellimuse rea tasemel.</span><span class="sxs-lookup"><span data-stu-id="9f46a-187">A combination of the **Other** cost component type and the **Sales line** other cost type is used to define non-shipping costs at the sales order line level.</span></span>

<span data-ttu-id="9f46a-188">Selle kombinatsiooni jaoks peate seadistama järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="9f46a-188">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="9f46a-189">**Kulutegur** – sisestage kuluteguri kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="9f46a-189">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="9f46a-190">**Kirjeldus** – sisestage kuluteguri nimi ja kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="9f46a-190">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="9f46a-191">**Alguskuupäev** ja **Lõppkuupäev** – saate neid välju kasutada kuluteguri piiramiseks konkreetse kuupäevavahemikuga.</span><span class="sxs-lookup"><span data-stu-id="9f46a-191">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="9f46a-192">Kui jätate need väljad tühjaks, kehtib kulutegur määramata perioodi jooksul.</span><span class="sxs-lookup"><span data-stu-id="9f46a-192">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="9f46a-193">**Aktiivne** – näidake, kas kulutegur on aktiivne.</span><span class="sxs-lookup"><span data-stu-id="9f46a-193">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="9f46a-194">DOM võtab arvesse ainult aktiivseid täitmisprofiiliga seostatud kulutegureid.</span><span class="sxs-lookup"><span data-stu-id="9f46a-194">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="9f46a-195">**Kulu** – määrake lähetamisega mitteseotud kulu kuluväärtus müügitellimuse rea tasemel.</span><span class="sxs-lookup"><span data-stu-id="9f46a-195">**Cost** – Specify the cost value for a non-shipping cost at the sales order line level.</span></span>

#### <a name="cost-component-type--other-and-other-cost-type--location"></a><span data-ttu-id="9f46a-196">Kulukomponendi tüüp = muud; muu kulutüüp = asukoht</span><span class="sxs-lookup"><span data-stu-id="9f46a-196">Cost component type = Other and Other cost type = Location</span></span>

<span data-ttu-id="9f46a-197">Kulukomponendi tüübi **Muud** ja muu kulutüübi **Asukoht** kombinatsiooni kasutatakse lähetamisega mitteseotud kulude määratlemiseks asukohtade rühma või üksikasukoha jaoks.</span><span class="sxs-lookup"><span data-stu-id="9f46a-197">A combination of the **Other** cost component type and the **Location** other cost type is used to define non-shipping costs for a group of locations or an individual location.</span></span>

<span data-ttu-id="9f46a-198">Selle kombinatsiooni jaoks peate seadistama järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="9f46a-198">You must set up the following fields for this combination:</span></span>

- <span data-ttu-id="9f46a-199">**Kulutegur** – sisestage kuluteguri kordumatu identifikaator.</span><span class="sxs-lookup"><span data-stu-id="9f46a-199">**Cost factor** – Enter a unique identifier for the cost factor.</span></span>
- <span data-ttu-id="9f46a-200">**Kirjeldus** – sisestage kuluteguri nimi ja kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="9f46a-200">**Description** – Enter the name and description of the cost factor.</span></span>
- <span data-ttu-id="9f46a-201">**Alguskuupäev** ja **Lõppkuupäev** – saate neid välju kasutada kuluteguri piiramiseks konkreetse kuupäevavahemikuga.</span><span class="sxs-lookup"><span data-stu-id="9f46a-201">**Start date** and **End date** – You can use these fields to limit the cost factor for a specific date range.</span></span> <span data-ttu-id="9f46a-202">Kui jätate need väljad tühjaks, kehtib kulutegur määramata perioodi jooksul.</span><span class="sxs-lookup"><span data-stu-id="9f46a-202">If you leave these fields blank, the cost factor is valid for an indefinite period.</span></span>
- <span data-ttu-id="9f46a-203">**Aktiivne** – näidake, kas kulutegur on aktiivne.</span><span class="sxs-lookup"><span data-stu-id="9f46a-203">**Active** – Indicate whether the cost factor is active.</span></span> <span data-ttu-id="9f46a-204">DOM võtab arvesse ainult aktiivseid täitmisprofiiliga seostatud kulutegureid.</span><span class="sxs-lookup"><span data-stu-id="9f46a-204">The DOM considers only active cost factors that are associated with the fulfillment profile.</span></span>
- <span data-ttu-id="9f46a-205">**Täitmisgrupp** – määrake nende asukohtade grupp, mille jaoks lähetamisega mitteseotud kulu määratletakse.</span><span class="sxs-lookup"><span data-stu-id="9f46a-205">**Fulfillment group** – Specify the group of locations that the non-shipping cost is defined for.</span></span>
- <span data-ttu-id="9f46a-206">**Täitmisasukoht** – määrake asukoht, mille jaoks lähetamisega mitteseotud kulu määratletakse.</span><span class="sxs-lookup"><span data-stu-id="9f46a-206">**Fulfillment location** – Specify the location that the non-shipping cost is defined for.</span></span>

    > [!NOTE]
    > <span data-ttu-id="9f46a-207">Asukohapõhiste arvutuskriteeriumite jaoks ei saa ühel ja samal real määrata täitmisgruppi ja täitmisasukohta.</span><span class="sxs-lookup"><span data-stu-id="9f46a-207">You can't specify a fulfillment group and a fulfillment location on the same line for location-based calculation criteria.</span></span>

- <span data-ttu-id="9f46a-208">**Kulu** – määrake lähetamisega mitteseotud kulu kuluväärtus täitmisgrupi tasemel või täitmisasukoha tasemel.</span><span class="sxs-lookup"><span data-stu-id="9f46a-208">**Cost** – Specify the cost value for a non-shipping cost at the fulfillment group level or fulfillment location level.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9f46a-209">Et DOM võtaks neid kulusid käitamisel arvesse, peate lisama kuluteguri asjakohasele täitmisprofiilile.</span><span class="sxs-lookup"><span data-stu-id="9f46a-209">For DOM to consider these costs when it's run, you must add the cost factor to the relevant fulfillment profile.</span></span>
