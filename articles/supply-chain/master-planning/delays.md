---
title: Hilinemised
description: Selles teemas antakse teavet hilinenud kuupäevade kohta koondplaneerimises. Hilinenud kuupäev on realistlik kande vastuvõtmise tähtaeg, kui varaseim koondplaneerimise arvutatud täitmise kuupäev on nõutavast kuupäevast hilisem.
author: roxanadiaconu
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a8e863ae63466f68e763b133da9f0e9488c6cfa6
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6189342"
---
# <a name="delays"></a><span data-ttu-id="72b02-104">Hilinemised</span><span class="sxs-lookup"><span data-stu-id="72b02-104">Delays</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="72b02-105">Selles teemas antakse teavet hilinenud kuupäevade kohta koondplaneerimises.</span><span class="sxs-lookup"><span data-stu-id="72b02-105">This topic provides information about delayed dates in master planning.</span></span> <span data-ttu-id="72b02-106">Hilinenud kuupäev on realistlik kande vastuvõtmise tähtaeg, kui varaseim koondplaneerimise arvutatud täitmise kuupäev on nõutavast kuupäevast hilisem.</span><span class="sxs-lookup"><span data-stu-id="72b02-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="72b02-107">Koondplaneerimine saab arvutada varaseima kande täitmise kuupäeva täitmisaegade, materjali saadavuse, võimsuse saadavuse ja erinevate plaanimisparameetrite põhjal.</span><span class="sxs-lookup"><span data-stu-id="72b02-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="72b02-108">Kui koondplaneerimine arvutab praegusest kuupäevast varasema tellimuse kuupäeva, ei saa tellimust täita õigel ajal.</span><span class="sxs-lookup"><span data-stu-id="72b02-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="72b02-109">Seetõttu lükatakse tellimus edasi.</span><span class="sxs-lookup"><span data-stu-id="72b02-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="72b02-110">Sellisel juhul plaanib koondplaneerimine tellimust praegusest kuupäevast edasi ja hõlmab täitmisaegu.</span><span class="sxs-lookup"><span data-stu-id="72b02-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="72b02-111">Need täitmisajad algavad mis tahes madalama taseme kaubakomponentidega.</span><span class="sxs-lookup"><span data-stu-id="72b02-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="72b02-112">Tellimus saab seejärel edasilükatud kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="72b02-112">The order then receives a delayed date.</span></span> <span data-ttu-id="72b02-113">Edasilükatud kuupäev on praegustel andmetel põhinev realistlik tähtaeg.</span><span class="sxs-lookup"><span data-stu-id="72b02-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="72b02-114">Koondplaneerimine arvutab ka hilinemispäevade arvu.</span><span class="sxs-lookup"><span data-stu-id="72b02-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="72b02-115">Mõningatel juhtudel võite hilinemisi mitte arvutada, näiteks kui kasutajad teavad, et saavad täitmisaegu kiirendada, valides alternatiivsed tarneviisid.</span><span class="sxs-lookup"><span data-stu-id="72b02-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="72b02-116">Saate konfigureerida laovarude grupi viivituste arvutamise viisi.</span><span class="sxs-lookup"><span data-stu-id="72b02-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="72b02-117">Seejärel saate laovarude grupi hiljem kaubale lisada.</span><span class="sxs-lookup"><span data-stu-id="72b02-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="72b02-118">Lehel **Koondplaneerimise parameetrid** saate seadistada viivituste arvutamise algusaja.</span><span class="sxs-lookup"><span data-stu-id="72b02-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="72b02-119">Kui tellimus täidetakse pärast seda aega, lisatakse tellimuse viivituskuupäevale ühepäevane viivitus.</span><span class="sxs-lookup"><span data-stu-id="72b02-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

> [!NOTE]
> <span data-ttu-id="72b02-120">Varasemates versioonides nimetati arvutatud viivitusi *tähtajateadeteks*, hilinenud kuupäeva *tähtajakuupäevaks* ja hilinenud kannet *tulevaseks kandeks*.</span><span class="sxs-lookup"><span data-stu-id="72b02-120">In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

## <a name="limited-delays-in-production-setup-with-multiple-bom-levels"></a><span data-ttu-id="72b02-121">Piiratud viivitused tootmise seadistamisel mitme kooslusetasemega</span><span class="sxs-lookup"><span data-stu-id="72b02-121">Limited delays in production setup with multiple BOM levels</span></span>
<span data-ttu-id="72b02-122">Kui töötate mitme kooslusetasemega tootmise seadistuse viivitustega, on oluline meeles pidada, et koondplaneerimise käitamise osana värskendatakse viivitusega ainult viivitust põhjustava üksuse kohal (koosluse struktuuris) olevad üksused.</span><span class="sxs-lookup"><span data-stu-id="72b02-122">When you work with delays in a production setup that has multiple BOM levels, it is important to note that only the items directly above the item (in the BOM structure) causing the delay, will be updated with a delay as part of the master planning run.</span></span> <span data-ttu-id="72b02-123">Muudele koosluse struktuuri üksustele ei saa viivitust rakendada enne esimese koondplaneerimise käitamist, kui ülataseme plaanitud tellimus on kinnitatud.</span><span class="sxs-lookup"><span data-stu-id="72b02-123">Other items in the BOM structure will not get the delay applied until the first master planning run, when the planned order for the top level is approved or firmed.</span></span> 

<span data-ttu-id="72b02-124">Selle teadaoleva piirangu lahendamiseks saab koosluse struktuuri ülaosa viivitustega tootmistellimused kinnitada enne järgmise koondplaneerimise käitamist.</span><span class="sxs-lookup"><span data-stu-id="72b02-124">To work around this known limitation, the production orders on the top of the BOM structure with delays can be approved (or firmed) prior to the next master planning run.</span></span> <span data-ttu-id="72b02-125">Nii säilitatakse viivitusega kinnitatud plaanitud tootmistellimuse viivitus ja kõik selle aluseks olevad komponendid ajakohastatakse vastavalt.</span><span class="sxs-lookup"><span data-stu-id="72b02-125">This way the delay from the delayed approved planned production order will be kept and all underlying components will be updated accordingly.</span></span>
<span data-ttu-id="72b02-126">Tegevusteateid saab kasutada ka plaanitud tellimuste tuvastamiseks, mida saab koosluse struktuuri muude viivituste tõttu hilisemale kuupäevale teisaldada.</span><span class="sxs-lookup"><span data-stu-id="72b02-126">Action messages can also be used to identify planned orders that can be moved to a later date, due to other delays in the BOM structure.</span></span>

## <a name="desired-date"></a><span data-ttu-id="72b02-127">Soovitud kuupäev</span><span class="sxs-lookup"><span data-stu-id="72b02-127">Desired date</span></span>

<span data-ttu-id="72b02-128">Lehe **Plaanitud tellimus** vahekaardil **Viivitused** on planeeritud kuupäeva parameeter **Soovitud kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="72b02-128">On the **Planned order** page, under the **Delays** tab is the **Desired date** for the planned order.</span></span> <span data-ttu-id="72b02-129">Plaanitud tellimuse soovitud kuupäev on viivituste aluskuupäev, mis on arvutatud kuupäev, mis võrdub parameetrist **Netonõue** arvutatud parameetriga **Nõutav kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="72b02-129">The desired date of a planned order is the base date for delays, which is a computed date that equals the **Requested date** calculated from the **Net Requirement**.</span></span> <span data-ttu-id="72b02-130">Kui plaanitud tellimus on koosluse rida, tootmisrida või kanban-rida, on soovitud kuupäeva aluseks **Vajaduse kuupäev** ja soovitud kuupäeva ei kuvata lehel **Plaanitud tellimus**.</span><span class="sxs-lookup"><span data-stu-id="72b02-130">If the planned order is a BOM line, production line or kanban line, the desired date is based on the **Requirement date** and the desired date will not be shown on the **Planned order** page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="72b02-131">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="72b02-131">Additional resources</span></span>

[<span data-ttu-id="72b02-132">Laovarude sätted</span><span class="sxs-lookup"><span data-stu-id="72b02-132">Coverage settings</span></span>](coverage-settings.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]