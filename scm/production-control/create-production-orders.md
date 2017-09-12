---
title: Tootmistellimuste loomine
description: "Kui tootmistellimus on loodud, siis käivitatakse taotlus kauba tootmise alustamiseks. Tootmistellimus sisaldab teavet selle kohta, mida toodetakse, tootmise koguse kohta ja kavandatavat valmimiskuupäeva. See sisaldab ka teavet tarbitavate materjalide ja selle kohta, millise protsessi abil kaupa toota."
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 58213d4d6e8c29ab6605eb7aa5c6cb9ca6ba4a10
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---

# <a name="create-production-orders"></a><span data-ttu-id="28295-105">Tootmistellimuste loomine</span><span class="sxs-lookup"><span data-stu-id="28295-105">Create production orders</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="28295-106">Kui tootmistellimus on loodud, siis käivitatakse taotlus kauba tootmise alustamiseks.</span><span class="sxs-lookup"><span data-stu-id="28295-106">When a production order is created, a request is initiated to start producing an item.</span></span> <span data-ttu-id="28295-107">Tootmistellimus sisaldab teavet selle kohta, mida toodetakse, tootmise koguse kohta ja kavandatavat valmimiskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="28295-107">The production order contains information about what will be produced, the quantity to produce, and the planned finish date.</span></span> <span data-ttu-id="28295-108">See sisaldab ka teavet tarbitavate materjalide ja selle kohta, millise protsessi abil kaupa toota.</span><span class="sxs-lookup"><span data-stu-id="28295-108">It also contains information about which materials to consume and which process to follow to produce the item.</span></span>

<span data-ttu-id="28295-109">Tootmistellimus läbib tootmise töötsükli etapid.</span><span class="sxs-lookup"><span data-stu-id="28295-109">A production order passes through stages of the production life cycle.</span></span> <span data-ttu-id="28295-110">Kui tellimus luuakse, antakse sellele olek **Loodud**.</span><span class="sxs-lookup"><span data-stu-id="28295-110">When an order is created, it is assigned the status **Created**.</span></span> <span data-ttu-id="28295-111">Kui tellimus lõpetatakse, antakse sellele olek **Lõpetatud**.</span><span class="sxs-lookup"><span data-stu-id="28295-111">When an order is finished, it is assigned the status **Ended**.</span></span> <span data-ttu-id="28295-112">Parameetri säte võimaldab kasutajal igas staadiumis iga etappi konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="28295-112">A parameter setting in each stage allows a user to configure each step.</span></span> <span data-ttu-id="28295-113">Sätte saab seadistada üksikkasutajale või kõigi kasutajate jaoks.</span><span class="sxs-lookup"><span data-stu-id="28295-113">The setting can be set up for a single user or for all users.</span></span>

<span data-ttu-id="28295-114">Tootmistellimuse põhiüksused on tootmise kooslus ja tootmisprotsess.</span><span class="sxs-lookup"><span data-stu-id="28295-114">The production bill of material and the production route are the main entities of the production order.</span></span> <span data-ttu-id="28295-115">Need kopeeritakse tootmistellimusele valitud kauba ja toodetava koguse põhjal.</span><span class="sxs-lookup"><span data-stu-id="28295-115">They are copied to the production order based on the selected item and quantity that are going to be produced.</span></span> <span data-ttu-id="28295-116">Enne tootmistellimuse alustamist saab tootmise kooslust ja protsessi redigeerida.</span><span class="sxs-lookup"><span data-stu-id="28295-116">Before the production order is started, the production bill of material and route can be edited.</span></span>

<span data-ttu-id="28295-117">Tootmistellimust saab luua järgmiste stsenaariumide korral.</span><span class="sxs-lookup"><span data-stu-id="28295-117">A production order can be created in the following scenarios:</span></span>

-   <span data-ttu-id="28295-118">Materjalinõudlusel põhineva koondplaanimise läbiviimise põhjal.</span><span class="sxs-lookup"><span data-stu-id="28295-118">Created by master planning execution based on material demand.</span></span>
-   <span data-ttu-id="28295-119">Otse müügitellimuse realt või kõrgema taseme tootmistellimuse loomisel ja hindamisel (seotud tarne).</span><span class="sxs-lookup"><span data-stu-id="28295-119">Created directly from a sales order line or when a higher-level production order is created and estimated (pegged supply).</span></span>
-   <span data-ttu-id="28295-120">Käsitsi loodud.</span><span class="sxs-lookup"><span data-stu-id="28295-120">Created manually.</span></span>





