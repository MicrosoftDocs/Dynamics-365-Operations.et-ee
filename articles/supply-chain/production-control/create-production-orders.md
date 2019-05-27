---
title: Tootmistellimuste loomine
description: Kui tootmistellimus on loodud, siis käivitatakse taotlus kauba tootmise alustamiseks. Tootmistellimus sisaldab teavet selle kohta, mida toodetakse, tootmise koguse kohta ja kavandatavat valmimiskuupäeva. See sisaldab ka teavet tarbitavate materjalide ja selle kohta, millise protsessi abil kaupa toota.
author: johanhoffmann
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProdTable, ProdTableCreate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19741
ms.assetid: bbb6e69d-479c-45fc-a0a8-66da5df16c7f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2957b387aac9e0218f88572fa605cde1a30c52e5
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1572623"
---
# <a name="create-production-orders"></a><span data-ttu-id="b4f56-105">Tootmistellimuste loomine</span><span class="sxs-lookup"><span data-stu-id="b4f56-105">Create production orders</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b4f56-106">Kui tootmistellimus on loodud, siis käivitatakse taotlus kauba tootmise alustamiseks.</span><span class="sxs-lookup"><span data-stu-id="b4f56-106">When a production order is created, a request is initiated to start producing an item.</span></span> <span data-ttu-id="b4f56-107">Tootmistellimus sisaldab teavet selle kohta, mida toodetakse, tootmise koguse kohta ja kavandatavat valmimiskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="b4f56-107">The production order contains information about what will be produced, the quantity to produce, and the planned finish date.</span></span> <span data-ttu-id="b4f56-108">See sisaldab ka teavet tarbitavate materjalide ja selle kohta, millise protsessi abil kaupa toota.</span><span class="sxs-lookup"><span data-stu-id="b4f56-108">It also contains information about which materials to consume and which process to follow to produce the item.</span></span>

<span data-ttu-id="b4f56-109">Tootmistellimus läbib tootmise töötsükli etapid.</span><span class="sxs-lookup"><span data-stu-id="b4f56-109">A production order passes through stages of the production life cycle.</span></span> <span data-ttu-id="b4f56-110">Kui tellimus luuakse, antakse sellele olek **Loodud**.</span><span class="sxs-lookup"><span data-stu-id="b4f56-110">When an order is created, it is assigned the status **Created**.</span></span> <span data-ttu-id="b4f56-111">Kui tellimus lõpetatakse, antakse sellele olek **Lõpetatud**.</span><span class="sxs-lookup"><span data-stu-id="b4f56-111">When an order is finished, it is assigned the status **Ended**.</span></span> <span data-ttu-id="b4f56-112">Parameetri säte võimaldab kasutajal igas staadiumis iga etappi konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="b4f56-112">A parameter setting in each stage allows a user to configure each step.</span></span> <span data-ttu-id="b4f56-113">Sätte saab seadistada üksikkasutajale või kõigi kasutajate jaoks.</span><span class="sxs-lookup"><span data-stu-id="b4f56-113">The setting can be set up for a single user or for all users.</span></span>

<span data-ttu-id="b4f56-114">Tootmistellimuse põhiüksused on tootmise kooslus ja tootmisprotsess.</span><span class="sxs-lookup"><span data-stu-id="b4f56-114">The production bill of material and the production route are the main entities of the production order.</span></span> <span data-ttu-id="b4f56-115">Need kopeeritakse tootmistellimusele valitud kauba ja toodetava koguse põhjal.</span><span class="sxs-lookup"><span data-stu-id="b4f56-115">They are copied to the production order based on the selected item and quantity that are going to be produced.</span></span> <span data-ttu-id="b4f56-116">Enne tootmistellimuse alustamist saab tootmise kooslust ja protsessi redigeerida.</span><span class="sxs-lookup"><span data-stu-id="b4f56-116">Before the production order is started, the production bill of material and route can be edited.</span></span>

<span data-ttu-id="b4f56-117">Tootmistellimust saab luua järgmiste stsenaariumide korral.</span><span class="sxs-lookup"><span data-stu-id="b4f56-117">A production order can be created in the following scenarios:</span></span>

-   <span data-ttu-id="b4f56-118">Materjalinõudlusel põhineva koondplaanimise läbiviimise põhjal.</span><span class="sxs-lookup"><span data-stu-id="b4f56-118">Created by master planning execution based on material demand.</span></span>
-   <span data-ttu-id="b4f56-119">Otse müügitellimuse realt või kõrgema taseme tootmistellimuse loomisel ja hindamisel (seotud tarne).</span><span class="sxs-lookup"><span data-stu-id="b4f56-119">Created directly from a sales order line or when a higher-level production order is created and estimated (pegged supply).</span></span>
-   <span data-ttu-id="b4f56-120">Käsitsi loodud.</span><span class="sxs-lookup"><span data-stu-id="b4f56-120">Created manually.</span></span>




