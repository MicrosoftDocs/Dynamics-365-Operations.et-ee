---
title: Hilinemised
description: Selles teemas antakse teavet hilinenud kuupäevade kohta koondplaneerimises. Hilinenud kuupäev on realistlik kande vastuvõtmise tähtaeg, kui varaseim koondplaneerimise arvutatud täitmise kuupäev on nõutavast kuupäevast hilisem.
author: roxanadiaconu
manager: AnnBe
ms.date: 03/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqTransFuturesListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19311
ms.assetid: 5ffb1486-2e08-4cdc-bd34-b47ae795ef0f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: roxanad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c26fedf15118a304469604527c33a25871356be
ms.sourcegitcommit: 8eac5eee94bb32143df44c82a2dfdbe903967af8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/20/2019
ms.locfileid: "878306"
---
# <a name="delays"></a><span data-ttu-id="0f9b3-104">Hilinemised</span><span class="sxs-lookup"><span data-stu-id="0f9b3-104">Delays</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f9b3-105">Selles teemas antakse teavet hilinenud kuupäevade kohta koondplaneerimises.</span><span class="sxs-lookup"><span data-stu-id="0f9b3-105">This topic provides information about delayed dates in master planning.</span></span> <span data-ttu-id="0f9b3-106">Hilinenud kuupäev on realistlik kande vastuvõtmise tähtaeg, kui varaseim koondplaneerimise arvutatud täitmise kuupäev on nõutavast kuupäevast hilisem.</span><span class="sxs-lookup"><span data-stu-id="0f9b3-106">A delayed date is a realistic due date that a transaction receives if the earliest fulfillment date that master planning calculates is later than the requested date.</span></span>

<span data-ttu-id="0f9b3-107">Koondplaneerimine saab arvutada varaseima kande täitmise kuupäeva täitmisaegade, materjali saadavuse, võimsuse saadavuse ja erinevate plaanimisparameetrite põhjal.</span><span class="sxs-lookup"><span data-stu-id="0f9b3-107">Master planning can calculate the earliest fulfillment date for a transaction, based on lead times, material availability, capacity availability, and various planning parameters.</span></span> 

<span data-ttu-id="0f9b3-108">Kui koondplaneerimine arvutab praegusest kuupäevast varasema tellimuse kuupäeva, ei saa tellimust täita õigel ajal.</span><span class="sxs-lookup"><span data-stu-id="0f9b3-108">If master planning calculates an order date that precedes the current date, the order can't be fulfilled on time.</span></span> <span data-ttu-id="0f9b3-109">Seetõttu lükatakse tellimus edasi.</span><span class="sxs-lookup"><span data-stu-id="0f9b3-109">Therefore, the order is delayed.</span></span> <span data-ttu-id="0f9b3-110">Sellisel juhul plaanib koondplaneerimine tellimust praegusest kuupäevast edasi ja hõlmab täitmisaegu.</span><span class="sxs-lookup"><span data-stu-id="0f9b3-110">In this case, master planning forward-plans the order from the current date and includes lead times.</span></span> <span data-ttu-id="0f9b3-111">Need täitmisajad algavad mis tahes madalama taseme kaubakomponentidega.</span><span class="sxs-lookup"><span data-stu-id="0f9b3-111">These lead times start with any lower-level component items.</span></span> <span data-ttu-id="0f9b3-112">Tellimus saab seejärel edasilükatud kuupäeva.</span><span class="sxs-lookup"><span data-stu-id="0f9b3-112">The order then receives a delayed date.</span></span> <span data-ttu-id="0f9b3-113">Edasilükatud kuupäev on praegustel andmetel põhinev realistlik tähtaeg.</span><span class="sxs-lookup"><span data-stu-id="0f9b3-113">A delayed date is a realistic due date, based on the current data.</span></span> <span data-ttu-id="0f9b3-114">Koondplaneerimine arvutab ka hilinemispäevade arvu.</span><span class="sxs-lookup"><span data-stu-id="0f9b3-114">Master planning also calculates the number of delay days.</span></span> 

<span data-ttu-id="0f9b3-115">Mõningatel juhtudel võite hilinemisi mitte arvutada, näiteks kui kasutajad teavad, et saavad täitmisaegu kiirendada, valides alternatiivsed tarneviisid.</span><span class="sxs-lookup"><span data-stu-id="0f9b3-115">In some situations, you might choose not to calculate delays, such as when users know that they can expedite lead times by selecting alternative modes of delivery.</span></span> 

<span data-ttu-id="0f9b3-116">Saate konfigureerida laovarude grupi viivituste arvutamise viisi.</span><span class="sxs-lookup"><span data-stu-id="0f9b3-116">You can configure how delays are calculated for a coverage group.</span></span> <span data-ttu-id="0f9b3-117">Seejärel saate laovarude grupi hiljem kaubale lisada.</span><span class="sxs-lookup"><span data-stu-id="0f9b3-117">You can then attach the coverage group to an item later.</span></span> 

<span data-ttu-id="0f9b3-118">Lehel **Koondplaneerimise parameetrid** saate seadistada viivituste arvutamise algusaja.</span><span class="sxs-lookup"><span data-stu-id="0f9b3-118">On the **Master planning parameters** page, you can set the start time for the calculation of delays.</span></span> <span data-ttu-id="0f9b3-119">Kui tellimus täidetakse pärast seda aega, lisatakse tellimuse viivituskuupäevale ühepäevane viivitus.</span><span class="sxs-lookup"><span data-stu-id="0f9b3-119">If an order is fulfilled after this time, a delay of one day is added to the delay date of the order.</span></span> 

> <span data-ttu-id="0f9b3-120">[!MÄRKUS} Varasemates versioonides nimetati arvutatud viivitusi *tähtajateadeteks*, hilinenud kuupäeva *tähtajakuupäevaks* ja hilinenud kannet *tulevaseks kandeks*.</span><span class="sxs-lookup"><span data-stu-id="0f9b3-120">[!NOTE} In earlier versions, calculated delays were known as *futures messages*, the delayed date was known as the *futures date*, and a delayed transaction was referred to as *a transaction that was future set*.</span></span>

## <a name="desired-date"></a><span data-ttu-id="0f9b3-121">Soovitud kuupäev</span><span class="sxs-lookup"><span data-stu-id="0f9b3-121">Desired date</span></span>

<span data-ttu-id="0f9b3-122">Lehe **Plaanitud tellimus** vahekaardil **Viivitused** on planeeritud kuupäeva parameeter **Soovitud kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="0f9b3-122">On the **Planned order** page, under the **Delays** tab is the **Desired date** for the planned order.</span></span> <span data-ttu-id="0f9b3-123">Plaanitud tellimuse soovitud kuupäev on viivituste aluskuupäev, mis on arvutatud kuupäev, mis võrdub parameetrist **Netonõue** arvutatud parameetriga **Nõutav kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="0f9b3-123">The desired date of a planned order is the base date for delays, which is a computed date that equals the **Requested date** calculated from the **Net Requirement**.</span></span> <span data-ttu-id="0f9b3-124">Kui plaanitud tellimus on koosluse rida, tootmisrida või kanban-rida, on soovitud kuupäeva aluseks **Vajaduse kuupäev** ja soovitud kuupäeva ei kuvata lehel **Plaanitud tellimus**.</span><span class="sxs-lookup"><span data-stu-id="0f9b3-124">If the planned order is a BOM line, production line or kanban line, the desired date is based on the **Requirement date** and the desired date will not be shown on the **Planned order** page.</span></span>

<a name="additional-resources"></a><span data-ttu-id="0f9b3-125">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="0f9b3-125">Additional resources</span></span>
--------

[<span data-ttu-id="0f9b3-126">Laovarude sätted</span><span class="sxs-lookup"><span data-stu-id="0f9b3-126">Coverage settings</span></span>](coverage-settings.md)
