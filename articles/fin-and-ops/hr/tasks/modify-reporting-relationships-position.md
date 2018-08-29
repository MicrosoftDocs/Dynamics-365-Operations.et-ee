--- 
title: Ametikohtade aruandlusseoste muutmine
description: "Protseduur näitab, kuidas muuta töötaja aruandluse seost."
author: ShielaSogge
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 2e52552ec5bce957ac43c2e34ac9a0e42829accd
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---
# <a name="modify-the-reporting-relationships-for-positions"></a><span data-ttu-id="2ccec-103">Ametikohtade aruandlusseoste muutmine</span><span class="sxs-lookup"><span data-stu-id="2ccec-103">Modify the reporting relationships for positions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2ccec-104">Protseduur näitab, kuidas muuta töötaja aruandluse seost.</span><span class="sxs-lookup"><span data-stu-id="2ccec-104">This procedure shows how to change the reporting relationship for an employee.</span></span> <span data-ttu-id="2ccec-105">Aruandluse seost saab kasutada töövoos dokumentide marsruudi valikul.</span><span class="sxs-lookup"><span data-stu-id="2ccec-105">The reporting relationship can be used for routing documents through workflow.</span></span> <span data-ttu-id="2ccec-106">Protseduur näitab ka seda, kuidas määrata töötaja täiendavatesse hierarhiatesse.</span><span class="sxs-lookup"><span data-stu-id="2ccec-106">The procedure also shows how to assign the employee to additional hierarchies.</span></span> <span data-ttu-id="2ccec-107">Näiteks võib töötaja kuuluda projekti töörühma, mis hõlmab mitteametlikku aruandluse seost projektijuhiga.</span><span class="sxs-lookup"><span data-stu-id="2ccec-107">For example, an employee might be a part of a project team with an informal reporting relationship to a project supervisor.</span></span> <span data-ttu-id="2ccec-108">Ametikoha jaoks saab määratleda täiendavad aruandluse seosed, et võimaldada mitmesuguseid projekti- või maatriksistsenaariume.</span><span class="sxs-lookup"><span data-stu-id="2ccec-108">Additional reporting relationships can be defined on the position to accommodate various project or matrix scenarios.</span></span> <span data-ttu-id="2ccec-109">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="2ccec-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="2ccec-110">Avage jaotis Personaliarvestus > Ametikohad > Ametikohad.</span><span class="sxs-lookup"><span data-stu-id="2ccec-110">Go to Human resources > Positions > Positions.</span></span>
2. <span data-ttu-id="2ccec-111">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="2ccec-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="2ccec-112">Näiteks saate filtrida välja Ametikoht alusel väärtusega „000091”.</span><span class="sxs-lookup"><span data-stu-id="2ccec-112">For example, filter on the Position field with a value of '000091'.</span></span>
3. <span data-ttu-id="2ccec-113">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="2ccec-113">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="2ccec-114">Laiendage jaotist Millisele ametikohale annab aru.</span><span class="sxs-lookup"><span data-stu-id="2ccec-114">Expand the Reports to position section.</span></span>
5. <span data-ttu-id="2ccec-115">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="2ccec-115">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="2ccec-116">Sisestage või valige väärtus väljal Aruannete sihtkoht.</span><span class="sxs-lookup"><span data-stu-id="2ccec-116">In the Reports to field, enter or select a value.</span></span>
7. <span data-ttu-id="2ccec-117">Klõpsake käsku Loo.</span><span class="sxs-lookup"><span data-stu-id="2ccec-117">Click Create.</span></span>
8. <span data-ttu-id="2ccec-118">Laiendage jaotist Seosed.</span><span class="sxs-lookup"><span data-stu-id="2ccec-118">Expand the Relationships section.</span></span>
9. <span data-ttu-id="2ccec-119">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="2ccec-119">Click Add.</span></span>
10. <span data-ttu-id="2ccec-120">Märkige ruudustikust vasakul olev ruut.</span><span class="sxs-lookup"><span data-stu-id="2ccec-120">Select the check box on the left of the grid.</span></span>
11. <span data-ttu-id="2ccec-121">Sisestage või valige väärtus väljal Hierarhia nimi.</span><span class="sxs-lookup"><span data-stu-id="2ccec-121">In the Hierarchy name field, enter or select a value.</span></span>
    * <span data-ttu-id="2ccec-122">Näide: projekt</span><span class="sxs-lookup"><span data-stu-id="2ccec-122">Example: Project</span></span>  
12. <span data-ttu-id="2ccec-123">Sisestage või valige väärtus väljal Millisele ametikohale annab aru.</span><span class="sxs-lookup"><span data-stu-id="2ccec-123">In the Reports to position field, enter or select a value.</span></span>  <span data-ttu-id="2ccec-124">Näide: 000437</span><span class="sxs-lookup"><span data-stu-id="2ccec-124">Example:  000437</span></span>
13. <span data-ttu-id="2ccec-125">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="2ccec-125">Click Save.</span></span>


