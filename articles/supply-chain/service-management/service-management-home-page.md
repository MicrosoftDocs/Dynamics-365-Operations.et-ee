---
title: Teeninduse halduse ülevaade
description: Teenuste haldusega saate luua teenuseleppeid ja hooldustellimusi, hallata hooldustellimusi ja kliendi päringuid ning hallata ja analüüsida teenuste pakkumist klientidele.
author: ShylaThompson
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6c58cd8002f6bb80ebcbd8c552e4e3509d7528ea
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215167"
---
# <a name="service-management-overview"></a><span data-ttu-id="1e68a-103">Teeninduse halduse ülevaade</span><span class="sxs-lookup"><span data-stu-id="1e68a-103">Service management overview</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="1e68a-104">**Teenuste haldusega** saate luua teenuseleppeid ja hooldustellimusi, hallata hooldustellimusi ja kliendi päringuid ning hallata ja analüüsida teenuste pakkumist klientidele.</span><span class="sxs-lookup"><span data-stu-id="1e68a-104">Use **Service management** to establish service agreements and service subscriptions, handle service orders and customer inquiries, and to manage and analyze the delivery of services to customers.</span></span> <span data-ttu-id="1e68a-105">Hoolduslepingutega saate määrata ressursid, mida kasutatakse tüüpilisel teenusekülastusel.</span><span class="sxs-lookup"><span data-stu-id="1e68a-105">You can use service agreements to define the resources that are used in a typical service visit.</span></span> <span data-ttu-id="1e68a-106">Hoolduslepingutega saate ka vaadata, kuidas neid ressursse kliendile arveldatakse.</span><span class="sxs-lookup"><span data-stu-id="1e68a-106">You can also use service agreements to view how those resources are invoiced to the customer.</span></span> <span data-ttu-id="1e68a-107">Hooldusleping võib sisaldada ka teenustaseme lepingut, millega määratakse reageerimisaeg ja pakutakse võimalusi tegelikult kulunud aega salvestada.</span><span class="sxs-lookup"><span data-stu-id="1e68a-107">A service agreement can also include a service level agreement that specifies standard response times, and offers tools to record the actual time.</span></span>

<span data-ttu-id="1e68a-108">Saate luua hooldustellimusi, et hallata teavet hooldustehniku plaanitud ja plaanimata külastuste kohta kliendi asukohta.</span><span class="sxs-lookup"><span data-stu-id="1e68a-108">You can create service orders to manage information about scheduled and unscheduled visits by a service technician to a customer site.</span></span> <span data-ttu-id="1e68a-109">Hooldustellimustes on näiteks järgmist teavet.</span><span class="sxs-lookup"><span data-stu-id="1e68a-109">Service orders include information such as:</span></span>

1.  <span data-ttu-id="1e68a-110">Hooldustehniku kulutatav töötundide arv</span><span class="sxs-lookup"><span data-stu-id="1e68a-110">The hours of work that the service technician will perform</span></span>

2.  <span data-ttu-id="1e68a-111">Teenuse või parandustöö tüüp</span><span class="sxs-lookup"><span data-stu-id="1e68a-111">The type of service or repair</span></span>

3.  <span data-ttu-id="1e68a-112">Parandatav kaup, sh sümptomite ja diagnoosi üksikasjad</span><span class="sxs-lookup"><span data-stu-id="1e68a-112">The item to repair, including details about the symptoms and diagnosis</span></span>

4.  <span data-ttu-id="1e68a-113">Hooldamise või parandamisega seotud kulud ja tasud</span><span class="sxs-lookup"><span data-stu-id="1e68a-113">Any expenses and fees related to the service or repair</span></span>

<span data-ttu-id="1e68a-114">Saate teenusetaotlusi vastu võtta, käidelda ja edasi saata.</span><span class="sxs-lookup"><span data-stu-id="1e68a-114">You can receive, process, and dispatch service requests.</span></span> <span data-ttu-id="1e68a-115">Pärast hooldustellimuse loomist saate kasutada edenemise jälgimiseks hoolduse etappe ning määrata reegleid igas etapis tehtavate toimingute kohta.</span><span class="sxs-lookup"><span data-stu-id="1e68a-115">After you have created a service order, you can use service stages to monitor progress and specify rules that control what actions are enabled in each stage.</span></span> <span data-ttu-id="1e68a-116">Kui hooldustellimus on lõpetatud, saate tellimuse lõpetatuks märkida ja seejärel arveldusprotsessi alustamiseks sisestada.</span><span class="sxs-lookup"><span data-stu-id="1e68a-116">When a service order is complete, you can sign off on the order to confirm that it is complete, and then post the order to start the invoice process.</span></span>

<span data-ttu-id="1e68a-117">Aruandlustarvikutega saate jälgida hooldustellimuse veeriseid ja tellimuste kandeid ning printida töökirjeldusi ja sissetulekuid.</span><span class="sxs-lookup"><span data-stu-id="1e68a-117">Use the reporting tools to monitor service order margins and subscription transactions, and print work descriptions and work receipts.</span></span>

## <a name="business-processes"></a><span data-ttu-id="1e68a-118">Äriprotsessid</span><span class="sxs-lookup"><span data-stu-id="1e68a-118">Business processes</span></span>

<span data-ttu-id="1e68a-119">Järgmisel joonisel on funktsiooni **Teenuste haldus** kõrge taseme äriprotsesside kasutamise näide ja näidatakse ka, kus hooldusprotsessid muude moodulitega integreeruvad.</span><span class="sxs-lookup"><span data-stu-id="1e68a-119">The following diagram illustrates the high level business processes for **Service management**, and shows where service processes integrate with other modules.</span></span>

<span data-ttu-id="1e68a-120">[![Teenuste halduse äriprotsessi diagramm](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span><span class="sxs-lookup"><span data-stu-id="1e68a-120">[![Service management business process diagram](./media/sm_home_page.gif)](./media/sm_home_page.gif)</span></span>

## <a name="service-management-at-a-glance"></a><span data-ttu-id="1e68a-121">Hoolduse halduse ülevaade</span><span class="sxs-lookup"><span data-stu-id="1e68a-121">Service management at a glance</span></span>

|<span data-ttu-id="1e68a-122">Olulised ülesanded</span><span class="sxs-lookup"><span data-stu-id="1e68a-122">Important tasks</span></span>           | <span data-ttu-id="1e68a-123">Esmased lehed</span><span class="sxs-lookup"><span data-stu-id="1e68a-123">Primary pages</span></span>                         |<span data-ttu-id="1e68a-124">Levinud aruanded</span><span class="sxs-lookup"><span data-stu-id="1e68a-124">Popular reports</span></span>              |
|--------------------------|---------------------------------------|-----------------------------|
|<span data-ttu-id="1e68a-125">Hoolduslepete täitmine</span><span class="sxs-lookup"><span data-stu-id="1e68a-125">Fulfill service agreements</span></span>|<span data-ttu-id="1e68a-126">Hoolduslepped</span><span class="sxs-lookup"><span data-stu-id="1e68a-126">Service agreements</span></span>                     |<span data-ttu-id="1e68a-127">Teenuse tellimuse kasum</span><span class="sxs-lookup"><span data-stu-id="1e68a-127">Service order margin</span></span>         |
|<span data-ttu-id="1e68a-128">Kliendipäringute käsitlemine</span><span class="sxs-lookup"><span data-stu-id="1e68a-128">Handle customer inquiries</span></span> |<span data-ttu-id="1e68a-129">Teenuse tellimused</span><span class="sxs-lookup"><span data-stu-id="1e68a-129">Service orders</span></span>                         |<span data-ttu-id="1e68a-130">Töö kirjeldus</span><span class="sxs-lookup"><span data-stu-id="1e68a-130">Work description</span></span>             |
|                          |<span data-ttu-id="1e68a-131">Lähetustahvel</span><span class="sxs-lookup"><span data-stu-id="1e68a-131">Dispatch board</span></span>                         |<span data-ttu-id="1e68a-132">Kanne – kordustellimus</span><span class="sxs-lookup"><span data-stu-id="1e68a-132">Transaction - subscription</span></span>   |
|                          |                                       |<span data-ttu-id="1e68a-133">Kordustellimuse tasu kanded</span><span class="sxs-lookup"><span data-stu-id="1e68a-133">Subscription fee transactions</span></span>|


## <a name="integration-of-service-management"></a><span data-ttu-id="1e68a-134">Teenusehalduse ühendamine</span><span class="sxs-lookup"><span data-stu-id="1e68a-134">Integration of Service management</span></span>

<span data-ttu-id="1e68a-135">Teenusehalduse saab ühendada järgmiste moodulitega:</span><span class="sxs-lookup"><span data-stu-id="1e68a-135">Service management can be integrated with the following modules:</span></span>

  - [<span data-ttu-id="1e68a-136">Müügi ja turunduse ülevaade</span><span class="sxs-lookup"><span data-stu-id="1e68a-136">Sales and marketing overview</span></span>](../sales-marketing/overview-sales-marketing.md)
  - [<span data-ttu-id="1e68a-137">Inimressursid</span><span class="sxs-lookup"><span data-stu-id="1e68a-137">Human resources</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/index)

  

