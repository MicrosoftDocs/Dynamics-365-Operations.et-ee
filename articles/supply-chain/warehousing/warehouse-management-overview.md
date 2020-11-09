---
title: Laohalduse ülevaade
description: Laohalduse abil laotoimingute jälgimine ja automatiseerimine.
author: ShylaThompson
manager: tfehr
ms.date: 04/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSParameters, WHSWorkPool
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ad0659a86e75dc4a5a204ebc05405f62abf2ca1e
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017456"
---
# <a name="warehouse-management-overview"></a><span data-ttu-id="ccd47-103">Laohalduse ülevaade</span><span class="sxs-lookup"><span data-stu-id="ccd47-103">Warehouse management overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ccd47-104">Laohalduse moodul võimaldab hallata laotoiminguid tootmis-, hulgimüügi- ja jaemüügiettevõtetes.</span><span class="sxs-lookup"><span data-stu-id="ccd47-104">The Warehouse management module lets you manage warehouse processes in manufacturing, distribution, and retail companies.</span></span> <span data-ttu-id="ccd47-105">Sellel moodulil on väga mitmesuguseid funktsioone, mis toetavad ladu alati optimaalsel tasemel.</span><span class="sxs-lookup"><span data-stu-id="ccd47-105">This module has a wide range of features to support the warehouse facility at an optimal level, at any time.</span></span> <span data-ttu-id="ccd47-106">Laohaldus on integreeritud täielikult teiste äriprotsessidega, nt transporti, tootmise, kvaliteedikontrolli, ostmise, üleviimise, müügi ja tagastustega.</span><span class="sxs-lookup"><span data-stu-id="ccd47-106">Warehouse management is fully integrated with other business processes such as transportation, manufacturing, quality control, purchase, transfer, sales, and returns.</span></span>

## <a name="get-started"></a><span data-ttu-id="ccd47-107">Alustamine</span><span class="sxs-lookup"><span data-stu-id="ccd47-107">Get started</span></span>
<span data-ttu-id="ccd47-108">Laohaldusega töö alustamiseks tuleb viia lõpule üldiste laoparameetrite seadistamine, et toetada oma ettevõtte äriprotsesse.</span><span class="sxs-lookup"><span data-stu-id="ccd47-108">To start working with Warehouse management, you need to complete the setup of the general warehouse parameters to support the business processes of your company.</span></span>

- <span data-ttu-id="ccd47-109">Minge lehele **Laohalduse parameetrid** jaotises **Laohaldus** > **Seadistus** , et seadistada üldised laoparameetrid.</span><span class="sxs-lookup"><span data-stu-id="ccd47-109">Go to the **Warehouse management parameters** page under **Warehouse management** > **Setup** to set up general warehouse parameters.</span></span>

<span data-ttu-id="ccd47-110">Peate konfigureerima sissetulevate ja väljaminevate laoprotsesside töövoogude komponendid vastavalt ärivajadustele.</span><span class="sxs-lookup"><span data-stu-id="ccd47-110">You must configure components for inbound and outbound warehouse process workflows according to business requirements.</span></span> <span data-ttu-id="ccd47-111">Kõige olulisemad komponendid, mis tuleb seadistada, on voomallid, töömallid, töökaustad ja asukohakorraldused.</span><span class="sxs-lookup"><span data-stu-id="ccd47-111">The most important components that you must configure are wave templates, work templates, work pools, and location directives.</span></span>

- [<span data-ttu-id="ccd47-112">Lao konfiguratsiooni ülevaade</span><span class="sxs-lookup"><span data-stu-id="ccd47-112">Warehouse configuration overview</span></span>](warehouse-configuration.md)
- [<span data-ttu-id="ccd47-113">Laotöö juhtimine töömallide ja asukohadirektiividega</span><span class="sxs-lookup"><span data-stu-id="ccd47-113">Control warehouse work by using work templates and location directives</span></span>](control-warehouse-location-directives.md)
- [<span data-ttu-id="ccd47-114">Mobiilsete seadmete seadistamine laotöö jaoks</span><span class="sxs-lookup"><span data-stu-id="ccd47-114">Set up mobile devices for warehouse work</span></span>](configure-mobile-devices-warehouse.md)
- [<span data-ttu-id="ccd47-115">Asukohakorralduse seadistamine ostutellimuse kõrvalepaneku jaoks</span><span class="sxs-lookup"><span data-stu-id="ccd47-115">Set up a location directive for purchase order put-away</span></span>](../transportation/tasks/set-up-location-directive-purchase-order-put-away.md)
- [<span data-ttu-id="ccd47-116">Ostutellimuste jaoks töömalli seadistamine</span><span class="sxs-lookup"><span data-stu-id="ccd47-116">Set up a work template for purchase orders</span></span>](./tasks/set-up-work-template-purchase-orders.md)

## <a name="warehouse-management-processes"></a><span data-ttu-id="ccd47-117">Laohaldusprotsessid</span><span class="sxs-lookup"><span data-stu-id="ccd47-117">Warehouse management processes</span></span>
- <span data-ttu-id="ccd47-118">Integreeritud lähtedokumentide, müügitellimuste, tagastuste, üleviimistellimuste, tootmistellimuste ja kanbani tugi</span><span class="sxs-lookup"><span data-stu-id="ccd47-118">Integrated support for source documents for sales orders, returns, transfer orders, production orders, and kanban</span></span>  
- <span data-ttu-id="ccd47-119">Paindlik sissetuleva ja väljamineva materjali töövoo tugi päringute põhjal</span><span class="sxs-lookup"><span data-stu-id="ccd47-119">Flexible, inbound and outbound material workflow support based on queries</span></span>
- <span data-ttu-id="ccd47-120">Täielik integratsioon tootmise ja transpordi pakkumistega</span><span class="sxs-lookup"><span data-stu-id="ccd47-120">Full integration with the Manufacturing and Transportation offerings</span></span>
- <span data-ttu-id="ccd47-121">Ladustamispiiride ja asukoha mahu täielik kontroll</span><span class="sxs-lookup"><span data-stu-id="ccd47-121">Full control of location stocking limits and location volumetrics</span></span>
- <span data-ttu-id="ccd47-122">Varude oleku alusel juhitavad varude atribuudid</span><span class="sxs-lookup"><span data-stu-id="ccd47-122">Inventory properties controlled by inventory status</span></span>
- <span data-ttu-id="ccd47-123">Täielik partii- ja seeriakaupade tugi</span><span class="sxs-lookup"><span data-stu-id="ccd47-123">Full batch and serial item support</span></span>
- <span data-ttu-id="ccd47-124">Mitmesugused kauba vastuvõtu võimalused</span><span class="sxs-lookup"><span data-stu-id="ccd47-124">Various item receiving capabilities</span></span>
- <span data-ttu-id="ccd47-125">Mitu komplekteerimisstrateegiat</span><span class="sxs-lookup"><span data-stu-id="ccd47-125">Multiple picking strategies</span></span>
- <span data-ttu-id="ccd47-126">Järgmise põlvkonna vöötkoodiskannerite tugi valmislahendusena</span><span class="sxs-lookup"><span data-stu-id="ccd47-126">Out-of-the-box support for the next generation of barcode scanners</span></span>
- <span data-ttu-id="ccd47-127">Aluste/konteinerite tüübid laoprotsesside jaoks</span><span class="sxs-lookup"><span data-stu-id="ccd47-127">Pallet/container types for warehouse processes</span></span>
- <span data-ttu-id="ccd47-128">Heal tasemel inventuurivõimalused</span><span class="sxs-lookup"><span data-stu-id="ccd47-128">Advanced counting capabilities</span></span>
- <span data-ttu-id="ccd47-129">Siltide printimine ja siltide marsruutimine Zebra ZPL-i toega</span><span class="sxs-lookup"><span data-stu-id="ccd47-129">Label printing and label routing with Zebra ZPL support</span></span>
- <span data-ttu-id="ccd47-130">Äriteabe integreerimine Power BI-sse</span><span class="sxs-lookup"><span data-stu-id="ccd47-130">Business intelligence integration into Power BI</span></span>
- <span data-ttu-id="ccd47-131">Varude liikumine käsitsi ja automaatselt</span><span class="sxs-lookup"><span data-stu-id="ccd47-131">Manual and automatic movement of inventory</span></span>
- <span data-ttu-id="ccd47-132">Täielikult integreeritud kvaliteedikontroll (QMS)</span><span class="sxs-lookup"><span data-stu-id="ccd47-132">Fully-integrated quality control (QMS)</span></span>
- <span data-ttu-id="ccd47-133">Töötajate materjali töötlemise täielik jälgitavus</span><span class="sxs-lookup"><span data-stu-id="ccd47-133">Full traceability of workers' material handling</span></span>
- <span data-ttu-id="ccd47-134">Väljamineva voo töötlemine</span><span class="sxs-lookup"><span data-stu-id="ccd47-134">Outbound wave processing</span></span>
- <span data-ttu-id="ccd47-135">Käsitsi pakkimise ja automaatse konteineritesse paigutamise tugi</span><span class="sxs-lookup"><span data-stu-id="ccd47-135">Manual packing and automatic containerization support</span></span>
- <span data-ttu-id="ccd47-136">Kogumi komplekteerimine</span><span class="sxs-lookup"><span data-stu-id="ccd47-136">Cluster picking</span></span>
- <span data-ttu-id="ccd47-137">Lihtne ristlaadimine</span><span class="sxs-lookup"><span data-stu-id="ccd47-137">Simple cross docking</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ccd47-138">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="ccd47-138">Additional resources</span></span>
### <a name="whats-new-and-in-development"></a><span data-ttu-id="ccd47-139">Mis on uut ja mis on arendamisel?</span><span class="sxs-lookup"><span data-stu-id="ccd47-139">What's new and in development</span></span>
<span data-ttu-id="ccd47-140">Avage [Microsoft Dynamics 365 sisukaart](https://roadmap.dynamics.com/), et näha, millised uued funktsioonid on välja antud ja millised uued funktsioonid on arendamisel.</span><span class="sxs-lookup"><span data-stu-id="ccd47-140">Go to the [Microsoft Dynamics 365 Roadmap](https://roadmap.dynamics.com/) to see what new features have been released and what new features are in development.</span></span>

### <a name="blogs"></a><span data-ttu-id="ccd47-141">Ajaveebid</span><span class="sxs-lookup"><span data-stu-id="ccd47-141">Blogs</span></span>
<span data-ttu-id="ccd47-142">Laohalduse ja muude lahendustega seotud arvamused, uudised ja muu teabe leiate [Microsoft Dynamics 365 ajaveebist](https://community.dynamics.com/b/msftdynamicsblog).</span><span class="sxs-lookup"><span data-stu-id="ccd47-142">You can find opinions, news, and other information about Warehouse management and other solutions on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog).</span></span>


 

