---
title: Ametikoha aruandlusseoste muutmine
description: Protseduur näitab, kuidas muuta töötaja aruandluse seost.
author: ShielaSogge
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HcmPosition, HcmPositionReportsToDialog, HcmPositionLookup
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e779a337ff8f8e0199a60e094f4bec9eba49e701
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "322693"
---
# <a name="modify-reporting-relationships-for-a-position"></a><span data-ttu-id="37bbe-103">Ametikoha aruandlusseoste muutmine</span><span class="sxs-lookup"><span data-stu-id="37bbe-103">Modify reporting relationships for a position</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="37bbe-104">Protseduur näitab, kuidas muuta töötaja aruandluse seost.</span><span class="sxs-lookup"><span data-stu-id="37bbe-104">This procedure shows how to change the reporting relationship for an employee.</span></span> <span data-ttu-id="37bbe-105">Aruandluse seost saab kasutada töövoos dokumentide marsruudi valikul.</span><span class="sxs-lookup"><span data-stu-id="37bbe-105">The reporting relationship can be used for routing documents through workflow.</span></span> <span data-ttu-id="37bbe-106">Protseduur näitab ka seda, kuidas määrata töötaja täiendavatesse hierarhiatesse.</span><span class="sxs-lookup"><span data-stu-id="37bbe-106">The procedure also shows how to assign the employee to additional hierarchies.</span></span> <span data-ttu-id="37bbe-107">Näiteks võib töötaja kuuluda projekti töörühma, mis hõlmab mitteametlikku aruandluse seost projektijuhiga.</span><span class="sxs-lookup"><span data-stu-id="37bbe-107">For example, an employee might be a part of a project team with an informal reporting relationship to a project supervisor.</span></span> <span data-ttu-id="37bbe-108">Ametikoha jaoks saab määratleda täiendavad aruandluse seosed, et võimaldada mitmesuguseid projekti- või maatriksistsenaariume.</span><span class="sxs-lookup"><span data-stu-id="37bbe-108">Additional reporting relationships can be defined on the position to accommodate various project or matrix scenarios.</span></span> <span data-ttu-id="37bbe-109">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="37bbe-109">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="37bbe-110">Avage jaotis Personaliarvestus > Ametikohad > Ametikohad.</span><span class="sxs-lookup"><span data-stu-id="37bbe-110">Go to Human resources > Positions > Positions.</span></span>
2. <span data-ttu-id="37bbe-111">Saate kirjete leidmiseks kasutada valikut Kiirfilter.</span><span class="sxs-lookup"><span data-stu-id="37bbe-111">Use the Quick Filter to find records.</span></span> <span data-ttu-id="37bbe-112">Näiteks saate filtrida välja Ametikoht alusel väärtusega „000091”.</span><span class="sxs-lookup"><span data-stu-id="37bbe-112">For example, filter on the Position field with a value of '000091'.</span></span>
3. <span data-ttu-id="37bbe-113">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="37bbe-113">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="37bbe-114">Laiendage jaotist Millisele ametikohale annab aru.</span><span class="sxs-lookup"><span data-stu-id="37bbe-114">Expand the Reports to position section.</span></span>
5. <span data-ttu-id="37bbe-115">Rippdialoogi avamiseks klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="37bbe-115">Click New to open the drop dialog.</span></span>
6. <span data-ttu-id="37bbe-116">Sisestage või valige väärtus väljal Aruannete sihtkoht.</span><span class="sxs-lookup"><span data-stu-id="37bbe-116">In the Reports to field, enter or select a value.</span></span>
7. <span data-ttu-id="37bbe-117">Klõpsake käsku Loo.</span><span class="sxs-lookup"><span data-stu-id="37bbe-117">Click Create.</span></span>
8. <span data-ttu-id="37bbe-118">Laiendage jaotist Seosed.</span><span class="sxs-lookup"><span data-stu-id="37bbe-118">Expand the Relationships section.</span></span>
9. <span data-ttu-id="37bbe-119">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="37bbe-119">Click Add.</span></span>
10. <span data-ttu-id="37bbe-120">Märkige ruudustikust vasakul olev ruut.</span><span class="sxs-lookup"><span data-stu-id="37bbe-120">Select the check box on the left of the grid.</span></span>
11. <span data-ttu-id="37bbe-121">Sisestage või valige väärtus väljal Hierarhia nimi.</span><span class="sxs-lookup"><span data-stu-id="37bbe-121">In the Hierarchy name field, enter or select a value.</span></span>
    * <span data-ttu-id="37bbe-122">Näide: projekt</span><span class="sxs-lookup"><span data-stu-id="37bbe-122">Example: Project</span></span>  
12. <span data-ttu-id="37bbe-123">Sisestage või valige väärtus väljal Millisele ametikohale annab aru.</span><span class="sxs-lookup"><span data-stu-id="37bbe-123">In the Reports to position field, enter or select a value.</span></span>  <span data-ttu-id="37bbe-124">Näide: 000437</span><span class="sxs-lookup"><span data-stu-id="37bbe-124">Example:  000437</span></span>
13. <span data-ttu-id="37bbe-125">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="37bbe-125">Click Save.</span></span>

