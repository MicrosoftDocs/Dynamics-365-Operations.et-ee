---
title: Protsessi kanban-töö ettevalmistamine, kui materjalid on tööraku jaoks saadaval
description: See ülesanne keskendub protsessi kanban-töö ettevalmistamisele, kui kõik materjalid on tööraku puhul saadaval.
author: johanhoffmann
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardWorkCell
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 460d55a8c4b8a8401db7abc43721cf0d114c27c5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5807820"
---
# <a name="prepare-a-process-kanban-job-when-materials-are-available-for-the-work-cell"></a><span data-ttu-id="93a91-103">Protsessi kanban-töö ettevalmistamine, kui materjalid on tööraku jaoks saadaval</span><span class="sxs-lookup"><span data-stu-id="93a91-103">Prepare a process kanban job when materials are available for the work cell</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="93a91-104">See ülesanne keskendub protsessi kanban-töö ettevalmistamisele, kui kõik materjalid on tööraku puhul saadaval.</span><span class="sxs-lookup"><span data-stu-id="93a91-104">This task focuses on preparing a process kanban job when all materials are available for the work cell.</span></span> <span data-ttu-id="93a91-105">Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="93a91-105">The demo data company used to create this task is USMF.</span></span> <span data-ttu-id="93a91-106">See ülesanne on mõeldud masinaoperaatorile.</span><span class="sxs-lookup"><span data-stu-id="93a91-106">This task is intended for the machine operator.</span></span>

1. <span data-ttu-id="93a91-107">Avage Protsessitööde kanban-tahvel.</span><span class="sxs-lookup"><span data-stu-id="93a91-107">Go to Kanban board for process jobs.</span></span>
2. <span data-ttu-id="93a91-108">Klõpsake väljal Töörakk otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="93a91-108">In the Work cell field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="93a91-109">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="93a91-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="93a91-110">Valige töörakk 1250 ja klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="93a91-110">Select work cell 1250 and click OK.</span></span>  
4. <span data-ttu-id="93a91-111">Valige loendist rida 4.</span><span class="sxs-lookup"><span data-stu-id="93a91-111">In the list, select row 4.</span></span>
    * <span data-ttu-id="93a91-112">Puhtas demoettevõttes on Kanban 000329 real 4 esimene töö, mis pole veel lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="93a91-112">In the clean demo company, Kanban 000329 in row 4 is the first job that is not completed yet.</span></span>  
5. <span data-ttu-id="93a91-113">Laiendage jaotist Komplekteerimisleht.</span><span class="sxs-lookup"><span data-stu-id="93a91-113">Toggle the expansion of the Picking list section.</span></span>
    * <span data-ttu-id="93a91-114">Kontrollige, kas tarneolek on saadaval kõigi komplekteerimiselehe kaupade puhul.</span><span class="sxs-lookup"><span data-stu-id="93a91-114">Verify that the supply status is available for all items in the picking list.</span></span>  
    * <span data-ttu-id="93a91-115">Mitme töö valimisel kuvab komplekteerimisleht kõikide valitud tööde puhul vajalike kaupade summa.</span><span class="sxs-lookup"><span data-stu-id="93a91-115">If multiple jobs are selected, the picking list will show the sum of all items needed for the selected jobs.</span></span>  
6. <span data-ttu-id="93a91-116">Klõpsake suvandit Valmista ette.</span><span class="sxs-lookup"><span data-stu-id="93a91-116">Click Prepare.</span></span>
    * <span data-ttu-id="93a91-117">Ettevalmistamise protsess on nüüd lõpetatud.</span><span class="sxs-lookup"><span data-stu-id="93a91-117">The preparation process is now completed.</span></span> <span data-ttu-id="93a91-118">Kõigi komplekteerimislehe ridade puhul valitud märkeruut näitab, et tarneolek on komplekteeritud.</span><span class="sxs-lookup"><span data-stu-id="93a91-118">The selected check box for all rows in the picking list indicates that the supply status is picked.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]