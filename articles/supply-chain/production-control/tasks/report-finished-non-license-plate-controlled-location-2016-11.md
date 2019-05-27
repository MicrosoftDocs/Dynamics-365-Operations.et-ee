---
title: Lõpetatuna kinnitamine asukohta, mida ei juhi litsentsiplaat (avaldus, mai 2016)
description: Selles ülesande juhendis esitatakse näide lõpetatuks kuulutamisest mittelitsentsiplaadiga juhitava asukoha jaoks.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup, ProdTableListPage, ProdTableCreate, InventItemIdLookupPurchase, ProdParmCostEstimation, ProdParmStartUp, ProdParmReportFinished, WHSWorkTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4da6868a2184a76c435efe824f4670504e1134e7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1562923"
---
# <a name="report-as-finished-to-a-non-license-plate-controlled-location--application-may-2016"></a><span data-ttu-id="619eb-103">Lõpetatuna kinnitamine asukohta, mida ei juhi litsentsiplaat (avaldus, mai 2016)</span><span class="sxs-lookup"><span data-stu-id="619eb-103">Report as finished to a non-license plate controlled location  (Application, May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="619eb-104">Selles ülesande juhendis esitatakse näide lõpetatuks kuulutamisest mittelitsentsiplaadiga juhitava asukoha jaoks.</span><span class="sxs-lookup"><span data-stu-id="619eb-104">This task guide shows an example of reporting as finished to a location that isn't license plate–controlled.</span></span> <span data-ttu-id="619eb-105">Selle ülesande eeltingimus on kehtiv tööpoliitika.</span><span class="sxs-lookup"><span data-stu-id="619eb-105">An applicable work policy is the prerequisite for this task.</span></span> <span data-ttu-id="619eb-106">Eelmises ülesande juhendis selgitati tööpoliitika seadistamist.</span><span class="sxs-lookup"><span data-stu-id="619eb-106">A previous task guide showed the setup of the work policy.</span></span> <span data-ttu-id="619eb-107">Selle tegevusjuhise jaoks on nõutav rakenduse Dynamics AX-i versioon 7.0.1 või uuem.</span><span class="sxs-lookup"><span data-stu-id="619eb-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>




## <a name="set-up-an-output-location"></a><span data-ttu-id="619eb-108">Väljundi asukoha seadistamine</span><span class="sxs-lookup"><span data-stu-id="619eb-108">Set up an output location</span></span>
1. <span data-ttu-id="619eb-109">Avage Organisatsiooni haldus > Ressursid > Ressursigrupid.</span><span class="sxs-lookup"><span data-stu-id="619eb-109">Go to Organization administration > Resources > Resource groups.</span></span>
2. <span data-ttu-id="619eb-110">Valige loendist ressursigrupp 5102.</span><span class="sxs-lookup"><span data-stu-id="619eb-110">In the list, select resource group '5102'.</span></span>
3. <span data-ttu-id="619eb-111">Klõpsake nuppu Redigeeri.</span><span class="sxs-lookup"><span data-stu-id="619eb-111">Click Edit.</span></span>
4. <span data-ttu-id="619eb-112">Sisestage väljale Väljastusladu väärtus 51.</span><span class="sxs-lookup"><span data-stu-id="619eb-112">In the Output warehouse field, enter '51'.</span></span>
5. <span data-ttu-id="619eb-113">Sisestage väljale Väljundi asukoht väärtus 001.</span><span class="sxs-lookup"><span data-stu-id="619eb-113">In the Output location field, enter '001'.</span></span>
    * <span data-ttu-id="619eb-114">Asukoht 001 pole litsentsiplaadiga juhitav asukoht.</span><span class="sxs-lookup"><span data-stu-id="619eb-114">Location 001 isn't a license plate–controlled location.</span></span> <span data-ttu-id="619eb-115">Saate seadistada mittelitsentsiplaadi väljundi asukoha ainult siis, kui asukohale on olemas vastav tööpoliitika.</span><span class="sxs-lookup"><span data-stu-id="619eb-115">You can set up a non–license plate output location only if an applicable work policy exists for the location.</span></span>  

## <a name="create-a-production-order-and-report-it-as-finished"></a><span data-ttu-id="619eb-116">Tootmistellimuse loomine ja selle lõpetatuna kinnitamine</span><span class="sxs-lookup"><span data-stu-id="619eb-116">Create a production order and report it as finished</span></span>
1. <span data-ttu-id="619eb-117">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="619eb-117">Close the page.</span></span>
2. <span data-ttu-id="619eb-118">Avage Tootmise juhtimine > Tootmistellimused > Kõik tootmistellimused.</span><span class="sxs-lookup"><span data-stu-id="619eb-118">Go to Production control > Production orders > All production orders.</span></span>
3. <span data-ttu-id="619eb-119">Klõpsake valikut Uus tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="619eb-119">Click New production order.</span></span>
4. <span data-ttu-id="619eb-120">Sisestage väljale Kauba kood väärtus L0101.</span><span class="sxs-lookup"><span data-stu-id="619eb-120">In the Item number field, enter 'L0101'.</span></span>
5. <span data-ttu-id="619eb-121">Klõpsake käsku Loo.</span><span class="sxs-lookup"><span data-stu-id="619eb-121">Click Create.</span></span>
6. <span data-ttu-id="619eb-122">Klõpsake toimingupaanil valikut Tootmistellimus.</span><span class="sxs-lookup"><span data-stu-id="619eb-122">On the Action Pane, click Production order.</span></span>
7. <span data-ttu-id="619eb-123">Klõpsake suvandit Hinnang.</span><span class="sxs-lookup"><span data-stu-id="619eb-123">Click Estimate.</span></span>
8. <span data-ttu-id="619eb-124">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="619eb-124">Click OK.</span></span>
9. <span data-ttu-id="619eb-125">Klõpsake käsku Käivita.</span><span class="sxs-lookup"><span data-stu-id="619eb-125">Click Start.</span></span>
10. <span data-ttu-id="619eb-126">Klõpsake vahekaarti Üldine.</span><span class="sxs-lookup"><span data-stu-id="619eb-126">Click the General tab.</span></span>
11. <span data-ttu-id="619eb-127">Tehke väljal Automaatne koosluse tarbimine valik Mitte kunagi.</span><span class="sxs-lookup"><span data-stu-id="619eb-127">In the Automatic BOM consumption field, select 'Never'.</span></span>
12. <span data-ttu-id="619eb-128">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="619eb-128">Click OK.</span></span>
13. <span data-ttu-id="619eb-129">Klõpsake valikut Kinnita lõpetamine.</span><span class="sxs-lookup"><span data-stu-id="619eb-129">Click Report as finished.</span></span>
14. <span data-ttu-id="619eb-130">Klõpsake vahekaarti Üldine.</span><span class="sxs-lookup"><span data-stu-id="619eb-130">Click the General tab.</span></span>
15. <span data-ttu-id="619eb-131">Tehke väljal Aktsepteeri viga valik Jah.</span><span class="sxs-lookup"><span data-stu-id="619eb-131">Select Yes in the Accept error field.</span></span>
16. <span data-ttu-id="619eb-132">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="619eb-132">Click OK.</span></span>
17. <span data-ttu-id="619eb-133">Klõpsake toimingupaanil valikut Ladu.</span><span class="sxs-lookup"><span data-stu-id="619eb-133">On the Action Pane, click Warehouse.</span></span>
18. <span data-ttu-id="619eb-134">Klõpsake suvandit Töö üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="619eb-134">Click Work details.</span></span>
    * <span data-ttu-id="619eb-135">Kui tootmistellimus on lõpetatuks kuulutatud, pole ladustamiseks tööd loodud.</span><span class="sxs-lookup"><span data-stu-id="619eb-135">When the production order was reported as finished, no work was generated for put-away.</span></span> <span data-ttu-id="619eb-136">See ilmneb, kuna määratletud on tööpoliitika, mis takistab töö loomist, kui toode L0101 kuulutatakse lõpetatuks asukohale 001.</span><span class="sxs-lookup"><span data-stu-id="619eb-136">This occurs because a work policy is defined that prevents work from being generated when product L0101 is reported as finished to location 001.</span></span>  

