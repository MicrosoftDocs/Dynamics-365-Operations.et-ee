---
title: Laohaldus
description: "Laohalduse abil laotoimingute jälgimine ja automatiseerimine."
author: BibiSp
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSParameters
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: a569d9264097d7a0b742bc7bf47c2504c58cdb4e
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---
# <a name="warehouse-management"></a><span data-ttu-id="ce931-103">Laohaldus</span><span class="sxs-lookup"><span data-stu-id="ce931-103">Warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce931-104">Laohalduse moodul rakendusele Dynamics 365 for Finance and Operations võimaldab hallata laoprotsesse tootmis-, hulgi- ja jaemüügiettevõtetes.</span><span class="sxs-lookup"><span data-stu-id="ce931-104">The Warehouse management module for Dynamics 365 for Finance and Operations lets you manage warehouse processes in manufacturing, distribution, and retail companies.</span></span> <span data-ttu-id="ce931-105">Sellel moodulil on väga mitmesuguseid funktsioone, mis toetavad ladu alati optimaalsel tasemel.</span><span class="sxs-lookup"><span data-stu-id="ce931-105">This module has a wide range of features to support the warehouse facility at an optimal level, at any time.</span></span> <span data-ttu-id="ce931-106">Laohaldus on integreeritud täielikult teiste Finance and Operationsi äriprotsessidega, nt transporti, tootmise, kvaliteedikontrolli, ostmise, üleviimise, müügi ja tagastustega.</span><span class="sxs-lookup"><span data-stu-id="ce931-106">Warehouse management is fully integrated with other business processes in Finance and Operations such as transportation, manufacturing, quality control, purchase, transfer, sales, and returns.</span></span>

## <a name="get-started"></a><span data-ttu-id="ce931-107">Alustamine</span><span class="sxs-lookup"><span data-stu-id="ce931-107">Get started</span></span>
<span data-ttu-id="ce931-108">Laohaldusega töö alustamiseks tuleb viia lõpule üldiste laoparameetrite seadistamine, et toetada oma ettevõtte äriprotsesse.</span><span class="sxs-lookup"><span data-stu-id="ce931-108">To start working with Warehouse management, you need to complete the setup of the general warehouse parameters to support the business processes of you company.</span></span>

- <span data-ttu-id="ce931-109">Minge lehele **Laohalduse parameetrid** jaotises **Laohaldus** > **Seadistus**, et seadistada üldised laoparameetrid.</span><span class="sxs-lookup"><span data-stu-id="ce931-109">Go to the **Warehouse management parameters** page under **Warehouse management** > **Setup** to set up general warehouse parameters.</span></span>

<span data-ttu-id="ce931-110">Peate konfigureerima sissetulevate ja väljaminevate laoprotsesside töövoogude komponendid vastavalt ärivajadustele.</span><span class="sxs-lookup"><span data-stu-id="ce931-110">You must configure components for inbound and outbound warehouse process workflows according to business requirements.</span></span> <span data-ttu-id="ce931-111">Kõige olulisemad komponendid, mis tuleb seadistada, on voomallid, töömallid, töökaustad ja asukohakorraldused.</span><span class="sxs-lookup"><span data-stu-id="ce931-111">The most important components that you must configure are wave templates, work templates, work pools, and location directives.</span></span>

- [<span data-ttu-id="ce931-112">Lao konfiguratsioon</span><span class="sxs-lookup"><span data-stu-id="ce931-112">Warehouse configuration</span></span>](warehouse-configuration.md)
- [<span data-ttu-id="ce931-113">Laotöö juhtimine töömallide ja asukohadirektiividega</span><span class="sxs-lookup"><span data-stu-id="ce931-113">Control warehouse work by using work templates and location directives</span></span>](control-warehouse-location-directives.md)
- [<span data-ttu-id="ce931-114">Mobiilsete seadmete seadistamine laotöö jaoks</span><span class="sxs-lookup"><span data-stu-id="ce931-114">Set up mobile devices for warehouse work</span></span>](configure-mobile-devices-warehouse.md)
- [<span data-ttu-id="ce931-115">Asukohakorralduse seadistamine ostutellimuse kõrvalepaneku jaoks</span><span class="sxs-lookup"><span data-stu-id="ce931-115">Set up a location directive for purchase order put-away</span></span>](../transportation/tasks/set-up-location-directive-purchase-order-put-away.md)
- [<span data-ttu-id="ce931-116">Ostutellimuste jaoks töömalli seadistamine</span><span class="sxs-lookup"><span data-stu-id="ce931-116">Set up a work template for purchase orders</span></span>](./tasks/set-up-work-template-purchase-orders.md)

## <a name="warehouse-management-processes"></a><span data-ttu-id="ce931-117">Laohaldusprotsessid</span><span class="sxs-lookup"><span data-stu-id="ce931-117">Warehouse management processes</span></span>
- <span data-ttu-id="ce931-118">Integreeritud lähtedokumentide, müügitellimuste, tagastuste, üleviimistellimuste, tootmistellimuste ja kanbani tugi</span><span class="sxs-lookup"><span data-stu-id="ce931-118">Integrated support for source documents for sales orders, returns, transfer orders, production orders, and kanban</span></span>  
- <span data-ttu-id="ce931-119">Paindlik sissetuleva ja väljamineva materjali töövoo tugi päringute põhjal</span><span class="sxs-lookup"><span data-stu-id="ce931-119">Flexible, inbound and outbound material workflow support based on queries</span></span>
- <span data-ttu-id="ce931-120">Täielik integratsioon tootmise ja transpordi pakkumistega</span><span class="sxs-lookup"><span data-stu-id="ce931-120">Full integration with the Manufacturing and Transportation offerings</span></span>
- <span data-ttu-id="ce931-121">Ladustamispiiride ja asukoha mahu täielik kontroll</span><span class="sxs-lookup"><span data-stu-id="ce931-121">Full control of location stocking limits and location volumetrics</span></span>
- <span data-ttu-id="ce931-122">Varude oleku alusel juhitavad varude atribuudid</span><span class="sxs-lookup"><span data-stu-id="ce931-122">Inventory properties controlled by inventory status</span></span>
- <span data-ttu-id="ce931-123">Täielik partii- ja seeriakaupade tugi</span><span class="sxs-lookup"><span data-stu-id="ce931-123">Full batch and serial item support</span></span>
- <span data-ttu-id="ce931-124">Mitmesugused kauba vastuvõtu võimalused</span><span class="sxs-lookup"><span data-stu-id="ce931-124">Various item receiving capabilities</span></span>
- <span data-ttu-id="ce931-125">Mitu komplekteerimisstrateegiat</span><span class="sxs-lookup"><span data-stu-id="ce931-125">Multiple picking strategies</span></span>
- <span data-ttu-id="ce931-126">Järgmise põlvkonna vöötkoodiskannerite tugi valmislahendusena</span><span class="sxs-lookup"><span data-stu-id="ce931-126">Out-of-the-box support for the next generation of barcode scanners</span></span>
- <span data-ttu-id="ce931-127">Aluste/konteinerite tüübid laoprotsesside jaoks</span><span class="sxs-lookup"><span data-stu-id="ce931-127">Pallet/container types for warehouse processes</span></span>
- <span data-ttu-id="ce931-128">Heal tasemel inventuurivõimalused</span><span class="sxs-lookup"><span data-stu-id="ce931-128">Advanced counting capabilities</span></span>
- <span data-ttu-id="ce931-129">Siltide printimine ja siltide marsruutimine Zebra ZPL-i toega</span><span class="sxs-lookup"><span data-stu-id="ce931-129">Label printing and label routing with Zebra ZPL support</span></span>
- <span data-ttu-id="ce931-130">Äriteabe integreerimine Power BI-sse</span><span class="sxs-lookup"><span data-stu-id="ce931-130">Business intelligence integration into Power BI</span></span>
- <span data-ttu-id="ce931-131">Varude liikumine käsitsi ja automaatselt</span><span class="sxs-lookup"><span data-stu-id="ce931-131">Manual and automatic movement of inventory</span></span>
- <span data-ttu-id="ce931-132">Täielikult integreeritud kvaliteedikontroll (QMS)</span><span class="sxs-lookup"><span data-stu-id="ce931-132">Fully-integrated quality control (QMS)</span></span>
- <span data-ttu-id="ce931-133">Töötajate materjali töötlemise täielik jälgitavus</span><span class="sxs-lookup"><span data-stu-id="ce931-133">Full traceability of workers' material handling</span></span>
- <span data-ttu-id="ce931-134">Väljamineva voo töötlemine</span><span class="sxs-lookup"><span data-stu-id="ce931-134">Outbound wave processing</span></span>
- <span data-ttu-id="ce931-135">Käsitsi pakkimise ja automaatse konteineritesse paigutamise tugi</span><span class="sxs-lookup"><span data-stu-id="ce931-135">Manual packing and automatic containerization support</span></span>
- <span data-ttu-id="ce931-136">Kogumi komplekteerimine</span><span class="sxs-lookup"><span data-stu-id="ce931-136">Cluster picking</span></span>
- <span data-ttu-id="ce931-137">Lihtne ristlaadimine</span><span class="sxs-lookup"><span data-stu-id="ce931-137">Simple cross docking</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ce931-138">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="ce931-138">Additional resources</span></span>
### <a name="whats-new-and-in-development"></a><span data-ttu-id="ce931-139">Mis on uut ja mis on arendamisel</span><span class="sxs-lookup"><span data-stu-id="ce931-139">What's new and in development</span></span>
<span data-ttu-id="ce931-140">Avage [Microsoft Dynamics 365 sisukaart](https://roadmap.dynamics.com/), et näha, millised uued funktsioonid on välja antud ja millised uued funktsioonid on arendamisel.</span><span class="sxs-lookup"><span data-stu-id="ce931-140">Go to the [Microsoft Dynamics 365 Roadmap](https://roadmap.dynamics.com/) to see what new features have been released and what new features are in development.</span></span>

### <a name="blogs"></a><span data-ttu-id="ce931-141">Ajaveebid</span><span class="sxs-lookup"><span data-stu-id="ce931-141">Blogs</span></span>
<span data-ttu-id="ce931-142">Laohalduse ja muude lahendustega seotud arvamused, uudised ja muu teabe leiate [Microsoft Dynamics 365 ajaveebist](https://community.dynamics.com/b/msftdynamicsblog).</span><span class="sxs-lookup"><span data-stu-id="ce931-142">You can find opinions, news, and other information about Warehouse management and other solutions on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog).</span></span>


 


