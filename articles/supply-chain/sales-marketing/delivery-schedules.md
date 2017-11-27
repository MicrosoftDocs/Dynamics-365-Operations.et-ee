---
title: Tarnegraafikud
description: "Tarnegraafikute abil saate jälgida tellimuse rea kogust, kui kasutate ühe müügitellimuse, müügipakkumise või ostutellimuse puhul mitut tarnet."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchDeliverySchedule, SalesDeliverySchedule, SalesQuotationDeliverySchedule
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 213984
ms.assetid: 44cac104-c36c-4371-a992-9178b3fd65e9
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ceb568cc223a631f704caf2417f1a3bd56b56288
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="delivery-schedules"></a><span data-ttu-id="e0472-103">Tarnegraafikud</span><span class="sxs-lookup"><span data-stu-id="e0472-103">Delivery schedules</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="e0472-104">Tarnegraafikute abil saate jälgida tellimuse rea kogust, kui kasutate ühe müügitellimuse, müügipakkumise või ostutellimuse puhul mitut tarnet.</span><span class="sxs-lookup"><span data-stu-id="e0472-104">Delivery schedules allow you to track order line quantity when you are using multiple deliveries for a single sales order, sales quotation, or purchase order.</span></span>

<span data-ttu-id="e0472-105">Kasutage tarnegraafikuid, kui tellimuse- või pakkumiserea täielik kogus tuleb tarnida mitme saadetisena.</span><span class="sxs-lookup"><span data-stu-id="e0472-105">Use a delivery schedule when the total quantity on an order or quotation line must be delivered in multiple shipments.</span></span> <span data-ttu-id="e0472-106">Üksikud saadetised esitatakse tarneridadena.</span><span class="sxs-lookup"><span data-stu-id="e0472-106">Individual shipments are represented by delivery lines.</span></span> <span data-ttu-id="e0472-107">Kaks või enam tarnerida moodustavad ühe tarnegraafiku.</span><span class="sxs-lookup"><span data-stu-id="e0472-107">Two or more delivery lines make up one delivery schedule.</span></span> <span data-ttu-id="e0472-108">Tarneridadel võivad olla erinevad tarnekuupäevad, kogused, tarneviisid ja laoala dimensioonid, nagu tegevuskoht ja ladu.</span><span class="sxs-lookup"><span data-stu-id="e0472-108">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span>  

<span data-ttu-id="e0472-109">**Tarnegraafiku rea näide**</span><span class="sxs-lookup"><span data-stu-id="e0472-109">**Example of a delivery schedule**</span></span>

|                                   |                                          |
|-----------------------------------|------------------------------------------|
| <span data-ttu-id="e0472-110">Kogutellimus (algne tellimuserida)</span><span class="sxs-lookup"><span data-stu-id="e0472-110">Total order (original order line)</span></span> | <span data-ttu-id="e0472-111">600 tooli</span><span class="sxs-lookup"><span data-stu-id="e0472-111">600 chairs</span></span>                               |
| <span data-ttu-id="e0472-112">Nõutav tarnegraafik</span><span class="sxs-lookup"><span data-stu-id="e0472-112">Requested delivery schedule</span></span>       | <span data-ttu-id="e0472-113">100 tooli kuus</span><span class="sxs-lookup"><span data-stu-id="e0472-113">100 chairs per month</span></span>                     |
| <span data-ttu-id="e0472-114">Nõutav tarne ajavahemik</span><span class="sxs-lookup"><span data-stu-id="e0472-114">Requested time frame for delivery</span></span> | <span data-ttu-id="e0472-115">6 kuud, iga kuu esimesel päeval</span><span class="sxs-lookup"><span data-stu-id="e0472-115">6 months, on the first day of each month</span></span> |

<span data-ttu-id="e0472-116">Selle stsenaariumi korral taotleb klient 600 tooli tarnet 100-tooliste partiidena kuue kuu jooksul.</span><span class="sxs-lookup"><span data-stu-id="e0472-116">In this scenario, the customer requests delivery of 600 chairs in batches of 100 chairs over a period of six months.</span></span> <span data-ttu-id="e0472-117">Tarnenõuete jälgimiseks loote te tarnegraafiku.</span><span class="sxs-lookup"><span data-stu-id="e0472-117">To keep track of the delivery requirements, you create a delivery schedule.</span></span> <span data-ttu-id="e0472-118">Tarnegraafiku lehel loote kuus eraldi tarnerida.</span><span class="sxs-lookup"><span data-stu-id="e0472-118">On the delivery schedule page, you create six separate delivery lines.</span></span> <span data-ttu-id="e0472-119">Iga tarnerida sisaldab 100 tooli ja näitab nende 100 tooli tarnekuupäeva.</span><span class="sxs-lookup"><span data-stu-id="e0472-119">Each delivery line contains 100 chairs and indicates the delivery date for those 100 chairs.</span></span> <span data-ttu-id="e0472-120">Sellisel juhul tasakaalustatakse iga rida kuue järjestikuse kuu esimesel kuupäeval.</span><span class="sxs-lookup"><span data-stu-id="e0472-120">In this case, each line is offset on the first of the month for six consecutive months.</span></span>  

<span data-ttu-id="e0472-121">Tarnegraafiku loomisel muutub algse tellimusrea tüübiks automaatselt **Mitme tarnega tellimuserida**.</span><span class="sxs-lookup"><span data-stu-id="e0472-121">When you create a delivery schedule, the type of the original order line is automatically changed to **Order line with multiple deliveries**.</span></span> <span data-ttu-id="e0472-122">Seda tüüpi rida nimetatakse äriandmete reaks ja see on tähistatud ikooniga.</span><span class="sxs-lookup"><span data-stu-id="e0472-122">A line of this type is referred to as a commercial line and is marked by an icon.</span></span> <span data-ttu-id="e0472-123">Tarnerida on tähistatud teistsuguse ikooniga.</span><span class="sxs-lookup"><span data-stu-id="e0472-123">The delivery line is marked by a different icon.</span></span> <span data-ttu-id="e0472-124">Tarnerea koguse muutmisel värskendatakse äriandmete rida tarnegraafiku lõplikule kogusele.</span><span class="sxs-lookup"><span data-stu-id="e0472-124">If you change a quantity on a delivery line, the commercial line is updated to the total quantity of the delivery schedule.</span></span> <span data-ttu-id="e0472-125">Kui kaubandusleppes on määratletud tellimuse lõplik allahindlus, tagab tarnegraafik, et teie tellimus on sobilik tellimuse lõplikule allahindlusele, isegi kui tellimus on jaotatud eraldi tarneteks.</span><span class="sxs-lookup"><span data-stu-id="e0472-125">If a trade agreement has defined a total discount for the order, the delivery schedule ensures that your order is eligible for the total order discount, even when the order is split into separate deliveries.</span></span>  

<span data-ttu-id="e0472-126">Tarnegraafikuga tellimusi töödeldakse tarneridade järgi.</span><span class="sxs-lookup"><span data-stu-id="e0472-126">Orders that have a delivery schedule are processed against the delivery lines.</span></span> <span data-ttu-id="e0472-127">Töötlemine hõlmab saatelehtede sisestamist, toote sissetulekuid ja arveldamist.</span><span class="sxs-lookup"><span data-stu-id="e0472-127">Processing includes the posting of packing slips, product receipts, and invoicing.</span></span>  

<span data-ttu-id="e0472-128">Tarnegraafikuga tellimuste ja pakkumiste trükitud dokumentidel kuvatakse ainult tarneread.</span><span class="sxs-lookup"><span data-stu-id="e0472-128">Document printouts of orders and quotations that have a delivery schedule show only the delivery lines.</span></span> <span data-ttu-id="e0472-129">Algseid ridu (äriandmete ridu) neil ei kuvata.</span><span class="sxs-lookup"><span data-stu-id="e0472-129">They don't show the original lines (commercial lines).</span></span> <span data-ttu-id="e0472-130">**Märkus.** Peale selle kuvatakse järgmiste tegevuste korral ainult tarneread.</span><span class="sxs-lookup"><span data-stu-id="e0472-130">**Note:** In addition, only the delivery lines are shown when you perform these actions:</span></span>

-   <span data-ttu-id="e0472-131">Postita</span><span class="sxs-lookup"><span data-stu-id="e0472-131">Post</span></span>
-   <span data-ttu-id="e0472-132">Lehtede kopeerimine</span><span class="sxs-lookup"><span data-stu-id="e0472-132">Copy pages</span></span>
-   <span data-ttu-id="e0472-133">Loendi lehekülgede ja aruannete sirvimine</span><span class="sxs-lookup"><span data-stu-id="e0472-133">Browse list pages and reports</span></span>

<span data-ttu-id="e0472-134">Müügipakkumiste kinnitamisel kuvatakse tulemuseks saadavatel müügitellimustel kogu tarnegraafik, sh ka mitme tarnega tellimuseread.</span><span class="sxs-lookup"><span data-stu-id="e0472-134">When you confirm sales quotations, the resulting sales orders show the whole delivery schedule, even the order lines that have multiple deliveries.</span></span> <span data-ttu-id="e0472-135">Samuti kuvatakse kogu tarnegraafik kõigil põhilehtedel, nagu müügitellimused, müügipakkumised ja ostutellimused.</span><span class="sxs-lookup"><span data-stu-id="e0472-135">In addition, the whole delivery schedule is shown on all the major pages, such as sales orders, sales quotations, and purchase orders.</span></span>




