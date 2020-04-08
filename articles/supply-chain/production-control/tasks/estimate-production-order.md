---
title: Tootmistellimuse hindamine
description: Saate seda protseduuri käitada demoettevõtte USMF või oma andmeid kasutades.
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
ms.openlocfilehash: f1e99d7c84171e4affe59fb896a7e93c2a328740
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3146763"
---
# <a name="estimate-a-production-order"></a><span data-ttu-id="e40fa-103">Tootmistellimuse hindamine</span><span class="sxs-lookup"><span data-stu-id="e40fa-103">Estimate a production order</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e40fa-104">Saate seda protseduuri käitada demoettevõtte USMF või oma andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="e40fa-104">You can run this procedure by using the USMF demo data company or your own data set.</span></span> <span data-ttu-id="e40fa-105">Mõlemal juhul peab teil olema avatud tootmistellimus, mis on olekus Loodud.</span><span class="sxs-lookup"><span data-stu-id="e40fa-105">In both cases, you need to have an open production order that has the Created status.</span></span> <span data-ttu-id="e40fa-106">See on teine protseduur seitsmest, mis selgitab tootmistellimuse elutsüklit.</span><span class="sxs-lookup"><span data-stu-id="e40fa-106">This is the second procedure out of seven which explains the production order lifecycle.</span></span>


## <a name="estimate-a-production-order"></a><span data-ttu-id="e40fa-107">Tootmistellimuse hindamine</span><span class="sxs-lookup"><span data-stu-id="e40fa-107">Estimate a production order</span></span>
1. <span data-ttu-id="e40fa-108">Avage Tootmise juhtimine > Tootmistellimused > Kõik tootmistellimused.</span><span class="sxs-lookup"><span data-stu-id="e40fa-108">Go to Production control > Production orders > All production orders.</span></span>
2. <span data-ttu-id="e40fa-109">Valige ruudustikus tellimus, mille olek on Loodud.</span><span class="sxs-lookup"><span data-stu-id="e40fa-109">Select an order that has the Created status in the grid.</span></span>
3. <span data-ttu-id="e40fa-110">Klõpsake toimingupaanil valikut Tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="e40fa-110">On the Action Pane, click Production order.</span></span>
4. <span data-ttu-id="e40fa-111">Klõpsake suvandit Hinnang.</span><span class="sxs-lookup"><span data-stu-id="e40fa-111">Click Estimate.</span></span>
    * <span data-ttu-id="e40fa-112">Selles etapis arvutatakse ühe tootmistellimuse eeldatavad kulud.</span><span class="sxs-lookup"><span data-stu-id="e40fa-112">In this step, the estimated costs of a single production order is calculated.</span></span>   
5. <span data-ttu-id="e40fa-113">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e40fa-113">Click OK.</span></span>

## <a name="view-the-calculation-details"></a><span data-ttu-id="e40fa-114">Kuva arvutamise üksikasjad</span><span class="sxs-lookup"><span data-stu-id="e40fa-114">View the calculation details</span></span>
1. <span data-ttu-id="e40fa-115">Klõpsake toimingupaanil valikut Kulude haldamine.</span><span class="sxs-lookup"><span data-stu-id="e40fa-115">On the Action Pane, click Manage costs.</span></span>
2. <span data-ttu-id="e40fa-116">Klõpsake suvandit Kuva arvutamise üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="e40fa-116">Click View calculation details.</span></span>
    * <span data-ttu-id="e40fa-117">Sellel lehel kuvatakse kulude jaotus.</span><span class="sxs-lookup"><span data-stu-id="e40fa-117">This page displays the cost breakdown.</span></span> <span data-ttu-id="e40fa-118">Näiteks saate vaadata esimese rea valmistoote kogu omahinda ühiku kohta.</span><span class="sxs-lookup"><span data-stu-id="e40fa-118">For example, you can view the total cost price per unit for the finished product in the first row.</span></span> <span data-ttu-id="e40fa-119">Järgnevad read sisaldavad vastavalt kooslusel, tootmisprotsessi ja kaudsete kulude kulusid.</span><span class="sxs-lookup"><span data-stu-id="e40fa-119">The subsequent rows contain costs according to the bill of materials, production route, and indirect costs.</span></span>  
