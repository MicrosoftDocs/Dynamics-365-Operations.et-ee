---
title: Väljamineva plaanitud kontsernisisese nõudluse kuvamine
description: See protseduur näitab, kuidas vaadata kõiki plaanitud tellimusi, mida kontsernisisene hankija täidab.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqOutboundIntercompanyDemand
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2e0e3a4613e5598e725c475c7dff7662bf4169a7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "333710"
---
# <a name="view-outbound-planned-intercompany-demand"></a><span data-ttu-id="44771-103">Väljamineva plaanitud kontsernisisese nõudluse kuvamine</span><span class="sxs-lookup"><span data-stu-id="44771-103">View outbound planned intercompany demand</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="44771-104">See protseduur näitab, kuidas vaadata kõiki plaanitud tellimusi, mida kontsernisisene hankija täidab.</span><span class="sxs-lookup"><span data-stu-id="44771-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="44771-105">Selle protseduuri loomiseks kasutatav demoandmete ettevõte on DEMF.</span><span class="sxs-lookup"><span data-stu-id="44771-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="44771-106">Klõpsake valikul Koondplaneerimine.</span><span class="sxs-lookup"><span data-stu-id="44771-106">Click Master planning.</span></span>
2. <span data-ttu-id="44771-107">Valige või sisestage väärtus väljal Plaan.</span><span class="sxs-lookup"><span data-stu-id="44771-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="44771-108">Valige plaan 10 väljalt Plaan.</span><span class="sxs-lookup"><span data-stu-id="44771-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="44771-109">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="44771-109">Click Run.</span></span>
4. <span data-ttu-id="44771-110">Sisestage number väljale Lõimede arv.</span><span class="sxs-lookup"><span data-stu-id="44771-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="44771-111">See tähistab koondplaneerimises kasutatavate paralleelsete lõimede arvu.</span><span class="sxs-lookup"><span data-stu-id="44771-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="44771-112">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="44771-112">Click OK.</span></span>
    * <span data-ttu-id="44771-113">See võib veidi aega võtta.</span><span class="sxs-lookup"><span data-stu-id="44771-113">This may take a while.</span></span>  
6. <span data-ttu-id="44771-114">Klõpsake valikut Plaanitud kontsernisisene nõudlus.</span><span class="sxs-lookup"><span data-stu-id="44771-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="44771-115">Klõpsake valikut Väljaminev plaanitud kontsernisisene nõudlus.</span><span class="sxs-lookup"><span data-stu-id="44771-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="44771-116">Sellel lehel antakse ülevaade kogu plaanitud nõudlusest, mille sisemise tarneahela hankija täidab.</span><span class="sxs-lookup"><span data-stu-id="44771-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="44771-117">Laiendage jaotist Ülesvoolu nõudluse üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="44771-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="44771-118">Selles jaotises saate vaadata teavet selle kohta, kuidas nõudlust täidetakse.</span><span class="sxs-lookup"><span data-stu-id="44771-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="44771-119">Enne kui siin lisateavet näete, peate ootama koondplaneerimise käitamist tarneettevõttes.</span><span class="sxs-lookup"><span data-stu-id="44771-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  

