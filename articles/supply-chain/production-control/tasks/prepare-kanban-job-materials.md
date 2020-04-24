---
title: Protsessi kanban-töö ettevalmistamine, kui materjalid on tööraku jaoks saadaval
description: See ülesanne keskendub protsessi kanban-töö ettevalmistamisele, kui kõik materjalid on tööraku puhul saadaval.
author: johanhoffmann
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: cd6d5add4d11c917a705e88d10b589e2c43fab89
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3206929"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-available-for-the-work-cell"></a><span data-ttu-id="f2ddf-103">Protsessi kanban-töö ettevalmistamine, kui materjalid on tööraku jaoks saadaval</span><span class="sxs-lookup"><span data-stu-id="f2ddf-103">Prepare a process kanban job when materials are available for the work cell</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f2ddf-104">See ülesanne keskendub protsessi kanban-töö ettevalmistamisele, kui kõik materjalid on tööraku puhul saadaval.</span><span class="sxs-lookup"><span data-stu-id="f2ddf-104">This task focuses on preparing a process kanban job when all materials are available for the work cell.</span></span> <span data-ttu-id="f2ddf-105">Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="f2ddf-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="f2ddf-106">See ülesanne on mõeldud masinaoperaatorile.</span><span class="sxs-lookup"><span data-stu-id="f2ddf-106">This task is intended for the machine operator.</span></span>

1. <span data-ttu-id="f2ddf-107">Avage Protsessitööde kanban-tahvel.</span><span class="sxs-lookup"><span data-stu-id="f2ddf-107">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="f2ddf-108">Klõpsake väljal Töörakk otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="f2ddf-108">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="f2ddf-109">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="f2ddf-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f2ddf-110">Valige töörakk 1250 ja klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="f2ddf-110">Select work cell 1250 and click OK.</span></span>  
4. <span data-ttu-id="f2ddf-111">Valige loendist rida 4.</span><span class="sxs-lookup"><span data-stu-id="f2ddf-111">In the list, select row 4.</span></span>
    * <span data-ttu-id="f2ddf-112">Puhtas demoettevõttes on Kanban 000329 real 4 esimene töö, mis pole veel lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="f2ddf-112">In the clean demo company, Kanban 000329 in row 4 is the first job that is not completed yet.</span></span>  
5. <span data-ttu-id="f2ddf-113">Laiendage jaotist Komplekteerimisleht.</span><span class="sxs-lookup"><span data-stu-id="f2ddf-113">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="f2ddf-114">Kontrollige, kas tarneolek on saadaval kõigi komplekteerimiselehe kaupade puhul.</span><span class="sxs-lookup"><span data-stu-id="f2ddf-114">Verify that the supply status is available for all items in the picking list.</span></span>  
    * <span data-ttu-id="f2ddf-115">Mitme töö valimisel kuvab komplekteerimisleht kõikide valitud tööde puhul vajalike kaupade summa.</span><span class="sxs-lookup"><span data-stu-id="f2ddf-115">If multiple jobs are selected, the picking list will show the sum of all items needed for the selected jobs.</span></span>  
6. <span data-ttu-id="f2ddf-116">Klõpsake suvandit Valmista ette.</span><span class="sxs-lookup"><span data-stu-id="f2ddf-116">Click Prepare.</span></span>
    * <span data-ttu-id="f2ddf-117">Ettevalmistamise protsess on nüüd lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="f2ddf-117">The preparation process is now completed.</span></span> <span data-ttu-id="f2ddf-118">Kõigi komplekteerimislehe ridade puhul valitud märkeruut näitab, et tarneolek on komplekteeritud.</span><span class="sxs-lookup"><span data-stu-id="f2ddf-118">The selected check box for all rows in the picking list indicates that the supply status is picked.</span></span>  

