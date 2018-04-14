---
title: "Kassa riistvara välisseadmed"
description: "Tänapäevane jaemüügikassa (POS) ja pilve kassa saavad kasutada laial hulgal kassa riistvara lisaseadmeid, millel on mitu liidest juurutamissuvandit, et saavutada jaemüüja erinevad äristsenaariumid."
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 215234
ms.assetid: 1893d4b3-e1b7-4b66-be58-0102addd5b36
ms.search.region: global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6ecfb0d6d3884bd8c96444613afed68547e141f1
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---

# <a name="pos-hardware-peripherals"></a><span data-ttu-id="45fff-103">Kassa riistvara välisseadmed</span><span class="sxs-lookup"><span data-stu-id="45fff-103">POS hardware peripherals</span></span>

[!INCLUDE [banner](includes/banner.md)]

<span data-ttu-id="45fff-104">Tänapäevane jaemüügikassa (POS) ja pilve kassa saavad kasutada laial hulgal kassa riistvara lisaseadmeid, millel on mitu liidest juurutamissuvandit, et saavutada jaemüüja erinevad äristsenaariumid.</span><span class="sxs-lookup"><span data-stu-id="45fff-104">Retail Modern point of sale (POS) and Cloud POS can utilize a wide range of POS hardware peripherals, with multiple interfaces and deployment options to achieve a retailer’s various business scenarios.</span></span> 

<span data-ttu-id="45fff-105">Erinevate tootjate ja mudelite hulgas kõige laiemal valikul seadmete toetamiseks kasutab kassa standardseid liideseid, nagu OLE Retail POS-i jaoks (OPOS), Windowsi seadme draiverid ja Windowsi teenuse rakenduse programmiliideste (API-d) Windowsi punkt.</span><span class="sxs-lookup"><span data-stu-id="45fff-105">To support the widest selection of devices across manufactures and models, POS utilizes standard interfaces such as OLE for Retail POS (OPOS), Windows device drivers, and Windows point of service application program interfaces (APIs).</span></span> <span data-ttu-id="45fff-106">Üldiselt töötab kassa nendes seadmetes tingimusel, et on antud sobiv draiver.</span><span class="sxs-lookup"><span data-stu-id="45fff-106">Generally, POS will work on these devices provided that the appropriate driver is supplied.</span></span> <span data-ttu-id="45fff-107">Kuna siiski iga tootja ja tarkvara arendaja viis neid standardeid juurutada on erinev, on toetatud võimalustes ja käitumistes sageli erinevusi.</span><span class="sxs-lookup"><span data-stu-id="45fff-107">However, because each manufacturer and software developer’s implementation of these standards can vary, there are often differences in supported capabilities or behaviors.</span></span>

<span data-ttu-id="45fff-108">Järgmine loend hõlmab seadmemudeleid, igas klassis, mida Microsoft on sisemiselt testinud.</span><span class="sxs-lookup"><span data-stu-id="45fff-108">The following list includes device models, in each class, that have been tested internally by Microsoft.</span></span>

<span data-ttu-id="45fff-109">**OPOS-i seadmed**</span><span class="sxs-lookup"><span data-stu-id="45fff-109">**OPOS devices**</span></span>

-   <span data-ttu-id="45fff-110">Vöötkood – Motorola DS9208</span><span class="sxs-lookup"><span data-stu-id="45fff-110">Barcode – Motorola DS9208</span></span>
-   <span data-ttu-id="45fff-111">MSR – HP IDRA-334133, Magtek PN - 21073062</span><span class="sxs-lookup"><span data-stu-id="45fff-111">MSR – HP IDRA-334133, Magtek PN - 21073062</span></span>
-   <span data-ttu-id="45fff-112">LineDisplay – Epson M58DC</span><span class="sxs-lookup"><span data-stu-id="45fff-112">LineDisplay – Epson M58DC</span></span>
-   <span data-ttu-id="45fff-113">Pinpad – Verifone 1000SE</span><span class="sxs-lookup"><span data-stu-id="45fff-113">Pinpad – Verifone 1000SE</span></span>
-   <span data-ttu-id="45fff-114">Allkirja klahvistik – Scriptel ST1550</span><span class="sxs-lookup"><span data-stu-id="45fff-114">Signature pad – Scriptel ST1550</span></span>
-   <span data-ttu-id="45fff-115">Printer – EPSON TM-T88IV, TMT88V</span><span class="sxs-lookup"><span data-stu-id="45fff-115">Printer – EPSON TM-T88IV, TMT88V</span></span>
-   <span data-ttu-id="45fff-116">Sularahasahtel – Star SMD2-1317BK44</span><span class="sxs-lookup"><span data-stu-id="45fff-116">Cash drawer – Star SMD2-1317BK44</span></span>
-   <span data-ttu-id="45fff-117">Skaala – Datalogic Magellan 8400</span><span class="sxs-lookup"><span data-stu-id="45fff-117">Scale – Datalogic Magellan 8400</span></span>

<span data-ttu-id="45fff-118">**Klaviatuurikiil MSR**</span><span class="sxs-lookup"><span data-stu-id="45fff-118">**Keyboard wedge MSR**</span></span>

-   <span data-ttu-id="45fff-119">Magtek USB</span><span class="sxs-lookup"><span data-stu-id="45fff-119">Magtek USB</span></span>

<span data-ttu-id="45fff-120">**Makseterminal**</span><span class="sxs-lookup"><span data-stu-id="45fff-120">**Payment terminal**</span></span>

-   <span data-ttu-id="45fff-121">Equinox L3500</span><span class="sxs-lookup"><span data-stu-id="45fff-121">Equinox L3500</span></span>
-   <span data-ttu-id="45fff-122">Verifone MX925</span><span class="sxs-lookup"><span data-stu-id="45fff-122">Verifone MX925</span></span>

<span data-ttu-id="45fff-123">**Võrguseadmed**</span><span class="sxs-lookup"><span data-stu-id="45fff-123">**Network devices**</span></span>

-   <span data-ttu-id="45fff-124">Printer – Star TSP650II</span><span class="sxs-lookup"><span data-stu-id="45fff-124">Printer – Star TSP650II</span></span>
-   <span data-ttu-id="45fff-125">Sularahasahtel – APG Atwood</span><span class="sxs-lookup"><span data-stu-id="45fff-125">Cash drawer – APG Atwood</span></span>
-   <span data-ttu-id="45fff-126">Makseterminal – MX915, MX925</span><span class="sxs-lookup"><span data-stu-id="45fff-126">Payment terminal – MX915, MX925</span></span>

<span data-ttu-id="45fff-127">**Ainult MPOS-i otse IPC**</span><span class="sxs-lookup"><span data-stu-id="45fff-127">**MPOS direct IPC only**</span></span>

-   <span data-ttu-id="45fff-128">Vöötkood – Honeywell 1900, HP LS2208</span><span class="sxs-lookup"><span data-stu-id="45fff-128">Barcode – Honeywell 1900, HP LS2208</span></span>
-   <span data-ttu-id="45fff-129">MSR – Magtek PN - 21073075</span><span class="sxs-lookup"><span data-stu-id="45fff-129">MSR – Magtek PN - 21073075</span></span>





