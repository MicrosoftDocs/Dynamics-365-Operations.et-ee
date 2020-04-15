---
title: Teise isiku nimel toodete tellimise õiguste seadistamine
description: See teema selgitab, kuidas anda töötajatele õigus teiste töötajate nimel ostutaotlusi koostada.
author: mkirknel
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchReqAuthorization, HcmWorkerLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: fe8ad0540febcc703554e2451f7f644338e4d57b
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149454"
---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a><span data-ttu-id="bd72e-103">Teise isiku nimel toodete tellimise õiguste seadistamine</span><span class="sxs-lookup"><span data-stu-id="bd72e-103">Set up permissions for ordering products on behalf of someone else</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bd72e-104">See teema selgitab, kuidas anda töötajatele õigus teiste töötajate nimel ostutaotlusi koostada.</span><span class="sxs-lookup"><span data-stu-id="bd72e-104">This topic explains how to grant workers permission to prepare purchase requisitions on behalf of other workers.</span></span> <span data-ttu-id="bd72e-105">Teisisõnu saab ostutaotluse „ettevalmistaja” luua nõude teisele „nõude esitajale”.</span><span class="sxs-lookup"><span data-stu-id="bd72e-105">In other words, a purchase requisition "preparer" can create a requisition for another "requester."</span></span> <span data-ttu-id="bd72e-106">See protseduur demonstreerib ka seda, kuidas anda töötajale õigus tellida kaupu ja teenuseid erinevate juriidiliste isikute või tootmisüksuste kaudu.</span><span class="sxs-lookup"><span data-stu-id="bd72e-106">The procedure also shows how to grant a worker permission to order items and services in different legal entities or operating units.</span></span> <span data-ttu-id="bd72e-107">Tavaliselt teeb need toimingud ostujuht.</span><span class="sxs-lookup"><span data-stu-id="bd72e-107">Typically, these tasks are performed by a purchasing manager.</span></span> <span data-ttu-id="bd72e-108">Saate seda protseduuri kasutada demoettevõtte USMF või oma andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="bd72e-108">You can use this procedure either on data for the USMF demo company or on your own data.</span></span>


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a><span data-ttu-id="bd72e-109">Õiguse andmine ostutaotluste sisestamiseks teise töötaja nimel</span><span class="sxs-lookup"><span data-stu-id="bd72e-109">Grant permission to enter purchase requisitions on behalf of another worker</span></span>
1. <span data-ttu-id="bd72e-110">Avage navigeerimispaneelil **Moodulid > Hange ja allikad > Seadistus > Poliitikad > Ostutaotluse load**.</span><span class="sxs-lookup"><span data-stu-id="bd72e-110">In the navigation pane, go to **Modules > Procurement and sourcing > Setup > Policies > Purchase requisition permissions**.</span></span> <span data-ttu-id="bd72e-111">Veenduge, et väljal **Praegune vaade** oleks määratud väärtus **Ettevalmistajalt**.</span><span class="sxs-lookup"><span data-stu-id="bd72e-111">Make sure that the **Current view** field is set to **By preparer**.</span></span> <span data-ttu-id="bd72e-112">Vasakul paanil olevas loendis on näidatud inimesed, kellele saab anda loa koostada teiste inimeste nimel ostutaotlusi.</span><span class="sxs-lookup"><span data-stu-id="bd72e-112">The list in the left pane shows the people who can be granted permission to prepare requisitions on behalf of other people.</span></span>  
2. <span data-ttu-id="bd72e-113">Valige isik, kellele õigus anda (ettevalmistaja).</span><span class="sxs-lookup"><span data-stu-id="bd72e-113">Select the person to grant permission to (the preparer).</span></span>
3. <span data-ttu-id="bd72e-114">Valige **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="bd72e-114">Select **Add**.</span></span>
4. <span data-ttu-id="bd72e-115">Otsige üles ja valige inimene, kes nõude esitajana lisada.</span><span class="sxs-lookup"><span data-stu-id="bd72e-115">Find and select the person to add as a requester.</span></span>
    - <span data-ttu-id="bd72e-116">Nõude esitaja on isik, kelle nimel ettevalmistaja saab taotlusi koostada.</span><span class="sxs-lookup"><span data-stu-id="bd72e-116">The requester is the person that the preparer can create requisitions on behalf of.</span></span>  
    - <span data-ttu-id="bd72e-117">Tehke väljal **Autoriseerimine** valik **Konkreetne**, kui ettevalmistaja peaks saama valitud töötaja nimel ostutaotlusi koostada.</span><span class="sxs-lookup"><span data-stu-id="bd72e-117">In the **Authorization** field, select **Specific** if the preparer should be able to create purchase requisitions on behalf of the selected worker.</span></span> <span data-ttu-id="bd72e-118">Valige **Aruandlus**, kui koostaja peaks saama koostada ostutaotlusi ka kõikide nende töötajate nimel, kes sellele töötajale alluvad.</span><span class="sxs-lookup"><span data-stu-id="bd72e-118">Select **Reporting** if the preparer should also be able to create purchase requisitions on behalf of all workers who report to that worker.</span></span>  
5. <span data-ttu-id="bd72e-119">Sisestage kuupäev väljale **Jõustunud**.</span><span class="sxs-lookup"><span data-stu-id="bd72e-119">In the **Effective** field, enter a date.</span></span>
6. <span data-ttu-id="bd72e-120">Sisestage kuupäev väljale **Aegumine**.</span><span class="sxs-lookup"><span data-stu-id="bd72e-120">In the **Expiration** field, enter a date.</span></span>

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a><span data-ttu-id="bd72e-121">Ettevalmistajate vaatamine, kellel on õigus koostada valitud töötaja eest ostutaotlusi</span><span class="sxs-lookup"><span data-stu-id="bd72e-121">View preparers who have permission to create purchase requisitions for a selected worker</span></span>
1. <span data-ttu-id="bd72e-122">Tehke väljal **Praegune vaade** valik **Nõude esitajalt**.</span><span class="sxs-lookup"><span data-stu-id="bd72e-122">In the **Current view** field, select **By requester**.</span></span> <span data-ttu-id="bd72e-123">Selles vaates on loend ettevalmistajatest, kellele on antud õigus valitud töötaja nimel ostutaotlusi koostada.</span><span class="sxs-lookup"><span data-stu-id="bd72e-123">This view shows a list of preparers who have been granted permission to create purchase requisitions on behalf of a selected worker.</span></span>  
2. <span data-ttu-id="bd72e-124">Otsige kiirfiltri abil üles töötaja, kelle just nõude esitajana lisasite.</span><span class="sxs-lookup"><span data-stu-id="bd72e-124">Use the Quick Filter to find the worker that you just added as the requester.</span></span>
3. <span data-ttu-id="bd72e-125">Valige nõude esitaja.</span><span class="sxs-lookup"><span data-stu-id="bd72e-125">Select the requester.</span></span> <span data-ttu-id="bd72e-126">Loendis Ettevalmistaja on inimesed, kellel on õigus tellida kaupu vasakul paanil valitud nõude esitaja nimel.</span><span class="sxs-lookup"><span data-stu-id="bd72e-126">The Preparer list shows the people who have permission to order items on behalf of the requester who is selected in the left pane.</span></span>  <span data-ttu-id="bd72e-127">Siin saate lisada veel ettevalmistajaid.</span><span class="sxs-lookup"><span data-stu-id="bd72e-127">You can add additional preparers here.</span></span> <span data-ttu-id="bd72e-128">Selles vaates saate anda nõude esitajale ka õiguse koostada taotlusi juriidilistes isikutes ja tootmisüksustes, mis ei ole selle inimese peamised juriidilised isikud või tootmisüksused.</span><span class="sxs-lookup"><span data-stu-id="bd72e-128">This view also lets you grant the requester permission to create requisitions in legal entities and operating units that aren't that person's primary legal entity or operating unit.</span></span>  

