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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8740846a6c6ba9e61c73ebce532d3bec525c2cc7
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148028"
---
# <a name="view-outbound-planned-intercompany-demand"></a><span data-ttu-id="0c220-103">Väljamineva plaanitud kontsernisisese nõudluse kuvamine</span><span class="sxs-lookup"><span data-stu-id="0c220-103">View outbound planned intercompany demand</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0c220-104">See protseduur näitab, kuidas vaadata kõiki plaanitud tellimusi, mida kontsernisisene hankija täidab.</span><span class="sxs-lookup"><span data-stu-id="0c220-104">This procedure shows how to view all the planned orders that will be fulfilled by an intercompany vendor.</span></span> <span data-ttu-id="0c220-105">Selle protseduuri loomiseks kasutatav demoandmete ettevõte on DEMF.</span><span class="sxs-lookup"><span data-stu-id="0c220-105">The demo data company used to create this procedure is DEMF.</span></span>

1. <span data-ttu-id="0c220-106">Klõpsake valikul Koondplaneerimine.</span><span class="sxs-lookup"><span data-stu-id="0c220-106">Click Master planning.</span></span>
2. <span data-ttu-id="0c220-107">Valige või sisestage väärtus väljal Plaan.</span><span class="sxs-lookup"><span data-stu-id="0c220-107">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="0c220-108">Valige plaan 10 väljalt Plaan.</span><span class="sxs-lookup"><span data-stu-id="0c220-108">In the Plan field, select plan 10.</span></span>  
3. <span data-ttu-id="0c220-109">Klõpsake nuppu Käivita.</span><span class="sxs-lookup"><span data-stu-id="0c220-109">Click Run.</span></span>
4. <span data-ttu-id="0c220-110">Sisestage number väljale Lõimede arv.</span><span class="sxs-lookup"><span data-stu-id="0c220-110">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="0c220-111">See tähistab koondplaneerimises kasutatavate paralleelsete lõimede arvu.</span><span class="sxs-lookup"><span data-stu-id="0c220-111">This represents the number of parallel threads to be used for master planning.</span></span>  
5. <span data-ttu-id="0c220-112">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="0c220-112">Click OK.</span></span>
    * <span data-ttu-id="0c220-113">See võib veidi aega võtta.</span><span class="sxs-lookup"><span data-stu-id="0c220-113">This may take a while.</span></span>  
6. <span data-ttu-id="0c220-114">Klõpsake valikut Plaanitud kontsernisisene nõudlus.</span><span class="sxs-lookup"><span data-stu-id="0c220-114">Click Planned intercompany demand.</span></span>
7. <span data-ttu-id="0c220-115">Klõpsake valikut Väljaminev plaanitud kontsernisisene nõudlus.</span><span class="sxs-lookup"><span data-stu-id="0c220-115">Click Outbound planned intercompany demand.</span></span>
    * <span data-ttu-id="0c220-116">Sellel lehel antakse ülevaade kogu plaanitud nõudlusest, mille sisemise tarneahela hankija täidab.</span><span class="sxs-lookup"><span data-stu-id="0c220-116">This page provides an overview of all the planned demand that will be fulfilled by an internal supply chain vendor.</span></span>  
8. <span data-ttu-id="0c220-117">Laiendage jaotist Ülesvoolu nõudluse üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="0c220-117">Expand the Upstream demand details section.</span></span>
    * <span data-ttu-id="0c220-118">Selles jaotises saate vaadata teavet selle kohta, kuidas nõudlust täidetakse.</span><span class="sxs-lookup"><span data-stu-id="0c220-118">In this section, you can see the details about how the demand will be fulfilled.</span></span> <span data-ttu-id="0c220-119">Enne kui siin lisateavet näete, peate ootama koondplaneerimise käitamist tarneettevõttes.</span><span class="sxs-lookup"><span data-stu-id="0c220-119">You may need to wait for master planning to be run in the supply company before you can see additional information here.</span></span>  

