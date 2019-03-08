---
title: Tootmistellimuse lõpetamine
description: See protseduur näitab, kuidas tootmistellimust lõpetada.
author: johanhoffmann
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8f5cb4afdc0285a6ccf28dbd362df3799c0ecc74
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "357354"
---
# <a name="end-a-production-order"></a><span data-ttu-id="69a77-103">Tootmistellimuse lõpetamine</span><span class="sxs-lookup"><span data-stu-id="69a77-103">End a production order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="69a77-104">See protseduur näitab, kuidas tootmistellimust lõpetada.</span><span class="sxs-lookup"><span data-stu-id="69a77-104">This procedure shows how to end a production order.</span></span> <span data-ttu-id="69a77-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="69a77-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="69a77-106">See on viimane protseduur seitsmest, mis selgitab tootmistellimuse elutsüklit.</span><span class="sxs-lookup"><span data-stu-id="69a77-106">This is the final procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="end-a-production-order"></a><span data-ttu-id="69a77-107">Tootmistellimuse lõpetamine</span><span class="sxs-lookup"><span data-stu-id="69a77-107">End a production order</span></span>
1. <span data-ttu-id="69a77-108">Avage Tootmise juhtimine > Tootmistellimused > Kõik tootmistellimused.</span><span class="sxs-lookup"><span data-stu-id="69a77-108">Go to Production control > Production orders > All production orders.</span></span>
    * <span data-ttu-id="69a77-109">Valige tootmistellimus, mille olek on Lõpetatuna kinnitatud.</span><span class="sxs-lookup"><span data-stu-id="69a77-109">Select a production order that has the status Reported as finished.</span></span>  
2. <span data-ttu-id="69a77-110">Klõpsake toimingupaanil valikut Tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="69a77-110">On the Action Pane, click Production order.</span></span>
3. <span data-ttu-id="69a77-111">Klõpsake suvandit Lõpeta.</span><span class="sxs-lookup"><span data-stu-id="69a77-111">Click End.</span></span>
    * <span data-ttu-id="69a77-112">Sellel lehel saate kinnitada tootmistellimuse lõpetamise.</span><span class="sxs-lookup"><span data-stu-id="69a77-112">On this page, you can confirm that you want to end the production order.</span></span>  
4. <span data-ttu-id="69a77-113">Klõpsake vahekaarti Üldine.</span><span class="sxs-lookup"><span data-stu-id="69a77-113">Click the General tab.</span></span>
5. <span data-ttu-id="69a77-114">Sisestage kuupäev väljale Kuupäev.</span><span class="sxs-lookup"><span data-stu-id="69a77-114">In the Date field, enter a date.</span></span>
6. <span data-ttu-id="69a77-115">Valige väljal Praagimeetod suvand Eraldamine.</span><span class="sxs-lookup"><span data-stu-id="69a77-115">In the Scrap method field, select 'Allocation'.</span></span>
    * <span data-ttu-id="69a77-116">Kui valite suvandi Eraldamismeetod, lisatakse lõpetatud kaupadele kulud mahakantud materjalide kulud.</span><span class="sxs-lookup"><span data-stu-id="69a77-116">When you select the Allocation method, costs from the scrapped materials are added to the finished goods.</span></span>  
7. <span data-ttu-id="69a77-117">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="69a77-117">Click OK.</span></span>

## <a name="validate-calculation-results"></a><span data-ttu-id="69a77-118">arvutustulemuste kinnitamine</span><span class="sxs-lookup"><span data-stu-id="69a77-118">Validate calculation results</span></span>
1. <span data-ttu-id="69a77-119">Klõpsake toimingupaanil valikut Kulude haldamine.</span><span class="sxs-lookup"><span data-stu-id="69a77-119">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="69a77-120">Klõpsake käsku Kuva kulu võrdlus.</span><span class="sxs-lookup"><span data-stu-id="69a77-120">Click View cost comparison.</span></span>
    * <span data-ttu-id="69a77-121">Pärast seda, kui tootmistellimus on lõpetatud, saate võrrelda eeldatavat omahinda realiseeritud omahinnaga, et saada ülevaade tootmishälvetest.</span><span class="sxs-lookup"><span data-stu-id="69a77-121">After you have ended the production order, you can compare the estimated cost price against the realized cost price to get an overview of the production variances.</span></span>  
