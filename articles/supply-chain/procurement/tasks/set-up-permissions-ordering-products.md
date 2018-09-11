--- 
title: "Teise isiku nimel toodete tellimise õiguste seadistamine"
description: "See protseduur näitab, kuidas anda töötajatele õigus teiste töötajate nimel ostutaotlusi koostada."
author: mkirknel
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchReqAuthorization, HcmWorkerLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: adcbf09cebc539a19ad3603a77dca1de77ce7d11
ms.contentlocale: et-ee
ms.lasthandoff: 09/11/2018

---
# <a name="set-up-permissions-for-ordering-products-on-behalf-of-someone-else"></a><span data-ttu-id="588b8-103">Teise isiku nimel toodete tellimise õiguste seadistamine</span><span class="sxs-lookup"><span data-stu-id="588b8-103">Set up permissions for ordering products on behalf of someone else</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="588b8-104">See protseduur näitab, kuidas anda töötajatele õigus teiste töötajate nimel ostutaotlusi koostada.</span><span class="sxs-lookup"><span data-stu-id="588b8-104">This procedure shows how to grant workers permission to prepare purchase requisitions on behalf of other workers.</span></span> <span data-ttu-id="588b8-105">Teisisõnu saab ostutaotluse "ettevalmistaja" luua nõude teisele "nõude esitajale".</span><span class="sxs-lookup"><span data-stu-id="588b8-105">In other words, a purchase requisition “preparer” can create a requisition for another “requester.”</span></span> <span data-ttu-id="588b8-106">See protseduur demonstreerib ka seda, kuidas anda töötajale õigus tellida kaupu ja teenuseid erinevate juriidiliste isikute või tootmisüksuste kaudu.</span><span class="sxs-lookup"><span data-stu-id="588b8-106">The procedure also shows how to grant a worker permission to order items and services in different legal entities or operating units.</span></span> <span data-ttu-id="588b8-107">Tavaliselt teeb need toimingud ostujuht.</span><span class="sxs-lookup"><span data-stu-id="588b8-107">Typically, these tasks are performed by a purchasing manager.</span></span> <span data-ttu-id="588b8-108">Saate seda protseduuri kasutada demoettevõtte USMF või oma andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="588b8-108">You can use this procedure either on data for the USMF demo company or on your own data.</span></span>


## <a name="grant-permission-to-enter-purchase-requisitions-on-behalf-of-another-worker"></a><span data-ttu-id="588b8-109">Õiguse andmine ostutaotluste sisestamiseks teise töötaja nimel</span><span class="sxs-lookup"><span data-stu-id="588b8-109">Grant permission to enter purchase requisitions on behalf of another worker</span></span>
1. <span data-ttu-id="588b8-110">Valige Hanked > Seadistus > Poliitikad > Ostutaotluse õigused.</span><span class="sxs-lookup"><span data-stu-id="588b8-110">Go to Procurement and sourcing > Setup > Policies > Purchase requisition permissions.</span></span>
    * <span data-ttu-id="588b8-111">Veenduge, et väljal Praegune vaade oleks määratud väärtus Ettevalmistajalt.</span><span class="sxs-lookup"><span data-stu-id="588b8-111">Make sure that the Current view field is set to By preparer.</span></span>  <span data-ttu-id="588b8-112">Vasakul paanil olevas loendis on näidatud inimesed, kellele saab anda loa koostada teiste inimeste nimel ostutaotlusi.</span><span class="sxs-lookup"><span data-stu-id="588b8-112">The list in the left pane shows the people who can be granted permission to prepare requisitions on behalf of other people.</span></span>  
2. <span data-ttu-id="588b8-113">Valige isik, kellele õigus anda (ettevalmistaja).</span><span class="sxs-lookup"><span data-stu-id="588b8-113">Select the person to grant permission to (the preparer).</span></span>
3. <span data-ttu-id="588b8-114">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="588b8-114">Click Add.</span></span>
4. <span data-ttu-id="588b8-115">Otsige üles ja valige inimene, kes nõude esitajana lisada.</span><span class="sxs-lookup"><span data-stu-id="588b8-115">Find and select the person to add as a requester.</span></span>
    * <span data-ttu-id="588b8-116">Nõude esitaja on isik, kelle nimel ettevalmistaja saab taotlusi koostada.</span><span class="sxs-lookup"><span data-stu-id="588b8-116">The requester is the person that the preparer can create requisitions on behalf of.</span></span>  
    * <span data-ttu-id="588b8-117">Tehke väljal Autoriseerimine valik Konkreetne, kui ettevalmistaja peaks saama valitud töötaja nimel ostutaotlusi koostada.</span><span class="sxs-lookup"><span data-stu-id="588b8-117">In the Authorization field, select Specific if the preparer should be able to create purchase requisitions on behalf of the selected worker.</span></span> <span data-ttu-id="588b8-118">Valige Aruandlus, kui koostaja peaks saama koostada ostutaotlusi ka kõikide nende töötajate nimel, kes sellele töötajale alluvad.</span><span class="sxs-lookup"><span data-stu-id="588b8-118">Select Reporting if the preparer should also be able to create purchase requisitions on behalf of all workers who report to that worker.</span></span>  
5. <span data-ttu-id="588b8-119">Sisestage kuupäev väljale Jõustunud.</span><span class="sxs-lookup"><span data-stu-id="588b8-119">In the Effective field, enter a date.</span></span>
6. <span data-ttu-id="588b8-120">Sisestage kuupäev väljale Aegumine.</span><span class="sxs-lookup"><span data-stu-id="588b8-120">In the Expiration field, enter a date.</span></span>

## <a name="view-preparers-who-have-permission-to-create-purchase-requisitions-for-a-selected-worker"></a><span data-ttu-id="588b8-121">Ettevalmistajate vaatamine, kellel on õigus koostada valitud töötaja eest ostutaotlusi</span><span class="sxs-lookup"><span data-stu-id="588b8-121">View preparers who have permission to create purchase requisitions for a selected worker</span></span>
1. <span data-ttu-id="588b8-122">Tehke väljal Praegune vaade valik Nõude esitajalt.</span><span class="sxs-lookup"><span data-stu-id="588b8-122">In the Current view field, select 'By requester'.</span></span>
    * <span data-ttu-id="588b8-123">Selles vaates on loend ettevalmistajatest, kellele on antud õigus valitud töötaja nimel ostutaotlusi koostada.</span><span class="sxs-lookup"><span data-stu-id="588b8-123">This view shows a list of preparers who have been granted permission to create purchase requisitions on behalf of a selected worker.</span></span>  
2. <span data-ttu-id="588b8-124">Otsige kiirfiltri abil üles töötaja, kelle just nõude esitajana lisasite.</span><span class="sxs-lookup"><span data-stu-id="588b8-124">Use the Quick Filter to find the worker that you just added as the requester.</span></span>
3. <span data-ttu-id="588b8-125">Valige nõude esitaja.</span><span class="sxs-lookup"><span data-stu-id="588b8-125">Select the requester.</span></span>
    * <span data-ttu-id="588b8-126">Loendis Ettevalmistaja on inimesed, kellel on õigus tellida kaupu vasakul paanil valitud nõude esitaja nimel.</span><span class="sxs-lookup"><span data-stu-id="588b8-126">The Preparer list shows the people who have permission to order items on behalf of the requester who is selected in the left pane.</span></span>   <span data-ttu-id="588b8-127">Siin saate lisada veel ettevalmistajaid.</span><span class="sxs-lookup"><span data-stu-id="588b8-127">You can add additional preparers here.</span></span>   <span data-ttu-id="588b8-128">Selles vaates saate anda nõude esitajale ka õiguse koostada taotlusi juriidilistes isikutes ja tootmisüksustes, mis ei ole selle inimese peamised juriidilised isikud või tootmisüksused.</span><span class="sxs-lookup"><span data-stu-id="588b8-128">This view also lets you grant the requester permission to create requisitions in legal entities and operating units that aren't that person's primary legal entity or operating unit.</span></span>  


