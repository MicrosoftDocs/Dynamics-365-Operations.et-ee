---
title: Hilinemised
description: "Selles artiklis antakse teavet hilinenud kuupäevade kohta koondplaneerimises. Hilinenud kuupäev on realistlik kande vastuvõtmise tähtaeg, kui varaseim koondplaneerimise arvutatud täitmise kuupäev on nõutavast kuupäevast hilisem."
author: roxanadiaconu
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ed0df1abbf4f70ea70046eff7b91a25fdd59016c
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="delays"></a><span data-ttu-id="84301-104">Hilinemised</span><span class="sxs-lookup"><span data-stu-id="84301-104">Delays</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="84301-105">Selles artiklis antakse teavet hilinenud kuupäevade kohta koondplaneerimises.</span><span class="sxs-lookup"><span data-stu-id="84301-105">This article provides information about delayed dates in master planning.</span></span> <span data-ttu-id="84301-106">Hilinenud kuupäev on realistlik kande vastuvõtmise tähtaeg, kui varaseim koondplaneerimise arvutatud täitmise kuupäev on nõutavast kuupäevast hilisem.</span><span class="sxs-lookup"><span data-stu-id="84301-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="84301-107">Koondplaneerimine saab arvutada varaseima kande täitmise kuupäeva täitmisaegade, materjali saadavuse, võimsuse saadavuse ja erinevate plaanimisparameetrite põhjal.</span><span class="sxs-lookup"><span data-stu-id="84301-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="84301-108">Kui koondplaneerimine arvutab praegusest kuupäevast varasema tellimuse kuupäeva, ei saa tellimust täita õigel ajal.</span><span class="sxs-lookup"><span data-stu-id="84301-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="84301-109">Seetõttu lükatakse tellimus edasi.</span><span class="sxs-lookup"><span data-stu-id="84301-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="84301-110">Sellisel juhul plaanib koondplaneerimine tellimust praegusest kuupäevast edasi ja hõlmab täitmisaegu.</span><span class="sxs-lookup"><span data-stu-id="84301-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="84301-111">Need täitmisajad algavad mis tahes madalama taseme kaubakomponentidega.</span><span class="sxs-lookup"><span data-stu-id="84301-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="84301-112">Tellimus saab seejärel edasilükatud kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="84301-112">The order then receives a delayed date.</span></span> <span data-ttu-id="84301-113">Edasilükatud kuupäev on praegustel andmetel põhinev realistlik tähtaeg.</span><span class="sxs-lookup"><span data-stu-id="84301-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="84301-114">Koondplaneerimine arvutab ka hilinemispäevade arvu.</span><span class="sxs-lookup"><span data-stu-id="84301-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="84301-115">Mõningatel juhtudel võite hilinemisi mitte arvutada, näiteks kui kasutajad teavad, et saavad täitmisaegu kiirendada, valides alternatiivsed tarneviisid.</span><span class="sxs-lookup"><span data-stu-id="84301-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="84301-116">Saate konfigureerida laovarude grupi viivituste arvutamise viisi.</span><span class="sxs-lookup"><span data-stu-id="84301-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="84301-117">Seejärel saate laovarude grupi hiljem kaubale lisada.</span><span class="sxs-lookup"><span data-stu-id="84301-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="84301-118">Lehel **Koondplaneerimise parameetrid** saate seadistada viivituste arvutamise algusaja.</span><span class="sxs-lookup"><span data-stu-id="84301-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="84301-119">Kui tellimus täidetakse pärast seda aega, lisatakse tellimuse viivituskuupäevale ühepäevane viivitus.</span><span class="sxs-lookup"><span data-stu-id="84301-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

<span data-ttu-id="84301-120">**Märkus.** Varasemates versioonides kutsuti arvutatud viivitusi nimetusega *tähtajateated*, hilinenud kuupäeva nimetusega *tähtajakuupäev* ja hilinenud kandele viidati nimetusega *tulevane kanne*.</span><span class="sxs-lookup"><span data-stu-id="84301-120">**Note:** In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

<a name="see-also"></a><span data-ttu-id="84301-121">Vt ka</span><span class="sxs-lookup"><span data-stu-id="84301-121">See also</span></span>
--------

[<span data-ttu-id="84301-122">Laovarude sätted</span><span class="sxs-lookup"><span data-stu-id="84301-122">Coverage settings</span></span>](coverage-settings.md)




