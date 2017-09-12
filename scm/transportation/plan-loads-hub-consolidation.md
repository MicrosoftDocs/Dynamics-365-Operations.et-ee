---
title: Koormate plaanimine keskuse konsolideerimisega
description: "See artikkel kirjeldab saadetiste keskusse konsolideerimise funktsiooni, kui tarnite kaupu erinevatest ladudest samale kliendile või võtate kaupu vastu mitmelt hankijalt samasse lattu."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSLoadPlanningWorkbench
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 92273
ms.assetid: d27b0926-a534-4caf-a2a3-acbc7c440bca
ms.search.region: Global
ms.search.industry: Distribution
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 3145febe40108e50b263514de1ca541dd914b7c5
ms.contentlocale: et-ee
ms.lasthandoff: 07/18/2017

---

# <a name="plan-loads-using-hub-consolidation"></a><span data-ttu-id="19f74-103">Koormate plaanimine keskuse konsolideerimisega</span><span class="sxs-lookup"><span data-stu-id="19f74-103">Plan loads using hub consolidation</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="19f74-104">See artikkel kirjeldab saadetiste keskusse konsolideerimise funktsiooni, kui tarnite kaupu erinevatest ladudest samale kliendile või võtate kaupu vastu mitmelt hankijalt samasse lattu.</span><span class="sxs-lookup"><span data-stu-id="19f74-104">This article describes the feature for consolidating shipments in a hub when you deliver goods from different warehouses to the same customer, or when you receive goods from multiple vendors in the same warehouse.</span></span>

<span data-ttu-id="19f74-105">Saadetisi võib olla mõistlik keskusse konsolideerida, kui tarnite kaupu erinevatest ladudest samale kliendile või kui kaupu tarnitakse mitmelt hankijalt samasse lattu.</span><span class="sxs-lookup"><span data-stu-id="19f74-105">It can be useful to consolidate shipments in a hub when you deliver goods from different warehouses to the same customer, or when goods are delivered from multiple vendors to the same warehouse.</span></span>

## <a name="building-loads"></a><span data-ttu-id="19f74-106">Koormate koostamine</span><span class="sxs-lookup"><span data-stu-id="19f74-106">Building loads</span></span>
<span data-ttu-id="19f74-107">Enne keskusse konsolideerimise kasutamist peate lubama valiku **Transiidi plaanimine**lehel **Transpordihalduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="19f74-107">Before you can use hub consolidation, you must enable the **In transit planning** option on the **Transportation management parameters** page.</span></span> <span data-ttu-id="19f74-108">Peate looma ka keskused, kus konsolideerimine toimub.</span><span class="sxs-lookup"><span data-stu-id="19f74-108">You must also create the hubs where consolidation will occur.</span></span> <span data-ttu-id="19f74-109">Järgmisel diagrammil on keskusse konsolideerimise näide.</span><span class="sxs-lookup"><span data-stu-id="19f74-109">The following diagram shows an example of hub consolidation.</span></span> <span data-ttu-id="19f74-110">Praegusel juhul lähevad erinevatest ladudest pärinevad müügitellimused samale kliendile.</span><span class="sxs-lookup"><span data-stu-id="19f74-110">In this case, sales orders from different warehouses are going to the same customer.</span></span> <span data-ttu-id="19f74-111">Peamised koormad koostatakse müügitellimuste põhjal tavalisel viisil, kasutades lehte **Koorma planeerimise töölaud**.</span><span class="sxs-lookup"><span data-stu-id="19f74-111">The basic loads are created based on sales orders in the usual way, by using the **Load planning workbench** page.</span></span> <span data-ttu-id="19f74-112">Kahe koorma konsolideerimiseks keskusse enne nende kliendile tarnimist tehke lehe **Koorma planeerimise töölaud** väljal **Transport** valik **Keskusse konsolideerimine**.</span><span class="sxs-lookup"><span data-stu-id="19f74-112">To consolidate the two loads in a hub before they are delivered to the customer, on the **Load planning workbench** page, in the **Transportation** field, select **Hub consolidation**.</span></span> <span data-ttu-id="19f74-113">Kui valite igale koormale õige keskuse, on koormate kohaleviimise sihtkohaks keskus.</span><span class="sxs-lookup"><span data-stu-id="19f74-113">When you select the correct hub for each load, the loads will have the hub as the “drop off” destination.</span></span> <span data-ttu-id="19f74-114">Samuti on jaotises **Pakkumine ja nõudlus** lehel **Koorma planeerimise töölaud** kaks transporditaotluse rida.</span><span class="sxs-lookup"><span data-stu-id="19f74-114">You will also have two “transportation request lines” in the **Supply and Demand** section on the **Load planning workbench** page.</span></span> <span data-ttu-id="19f74-115">Seejärel saate lisada need kaks rida uuele koormale.</span><span class="sxs-lookup"><span data-stu-id="19f74-115">You can then add these two lines to a new load.</span></span> <span data-ttu-id="19f74-116">Sellel uuel koormal on mõlemad müügitellimuse read ja pealevõtmise aadressiks keskus ning kohaleviimise aadressiks klient A.</span><span class="sxs-lookup"><span data-stu-id="19f74-116">This new load will have both sales order lines, and will also have the hub as the “pick up” address and customer A as the “drop off” destination.</span></span> <span data-ttu-id="19f74-117">Seejärel on kolm koormat teiste koormate sarnaselt hindamiseks ja suunamiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="19f74-117">The three loads are then ready to be rated and routed like any other load.</span></span> <span data-ttu-id="19f74-118">Saate valida igale koormale sobiva süsteemi soovitatud vedaja.</span><span class="sxs-lookup"><span data-stu-id="19f74-118">You can select whatever shipping carrier the system suggests for each load.</span></span> <span data-ttu-id="19f74-119">[![Keskusse konsolideerimine](./media/hubconsol.jpg)](./media/hubconsol.jpg) Sama meetodit saab kasutada ka mitme üleviimistellimuse koormate konsolideerimiseks.</span><span class="sxs-lookup"><span data-stu-id="19f74-119">[![Hub consolidation](./media/hubconsol.jpg)](./media/hubconsol.jpg) You can also use the same method to consolidate loads for multiple transfer orders.</span></span> <span data-ttu-id="19f74-120">Sellisel juhul on eelmise diagrammi klient A ladu.</span><span class="sxs-lookup"><span data-stu-id="19f74-120">In this case, customer A in the preceding diagram is a warehouse.</span></span> <span data-ttu-id="19f74-121">Teine võimalus on konsolideerida mitme ostutellimuse koormad, kui koormad tarnitakse erinevatelt hankijatelt samasse lattu.</span><span class="sxs-lookup"><span data-stu-id="19f74-121">Alternatively, you can consolidate loads for multiple purchase orders, where the loads are delivered from different vendors to the same warehouse.</span></span> <span data-ttu-id="19f74-122">Teil võib olla rohkem kui üks konsolideerimiskeskus ja suurema arvu koormate puhul erinevatest ladudest saate konsolideerida mitmesse keskusse.</span><span class="sxs-lookup"><span data-stu-id="19f74-122">You can have more than one consolidation hub, and can consolidate in multiple hubs for more loads that come from different warehouses.</span></span> <span data-ttu-id="19f74-123">Pärast põhikoormate koostamist ja keskuse konsolideerimise valiku kasutamist koostatakse uued koormad, kasutades konsolideeritud transporditaotluse ridu.</span><span class="sxs-lookup"><span data-stu-id="19f74-123">After you build your basic loads and use the hub consolidation option, you build the new loads by using the consolidated transportation request lines.</span></span> <span data-ttu-id="19f74-124">Seejärel saab koormaid hinnata ja suunata.</span><span class="sxs-lookup"><span data-stu-id="19f74-124">You then rate and route your loads.</span></span>




