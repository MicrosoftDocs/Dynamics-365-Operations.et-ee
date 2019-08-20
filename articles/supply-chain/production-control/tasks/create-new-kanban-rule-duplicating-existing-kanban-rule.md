---
title: Uue kanban-reegli loomine olemasoleva kanban-reegli dubleerimise teel
description: See protseduur keskendub olemasoleva kanban-reegli duplikaadi loomisele.
author: ChristianRytt
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanRules, KanbanRuleDuplicate, InventItemIdLookupSimple
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3aef2725152d39e49070f33d0c56089200c94353
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1837802"
---
# <a name="create-a-new-kanban-rule-by-duplicating-an-existing-kanban-rule"></a><span data-ttu-id="39703-103">Uue kanban-reegli loomine olemasoleva kanban-reegli dubleerimise teel</span><span class="sxs-lookup"><span data-stu-id="39703-103">Create a new kanban rule by duplicating an existing kanban rule</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="39703-104">See protseduur keskendub olemasoleva kanban-reegli duplikaadi loomisele.</span><span class="sxs-lookup"><span data-stu-id="39703-104">This procedure focuses on creating a duplicate of an existing kanban rule.</span></span> <span data-ttu-id="39703-105">See on kasulik, kui soovite luua uued kanban-reeglid olemasolevate kanban-reeglite alusel.</span><span class="sxs-lookup"><span data-stu-id="39703-105">This is useful if you want to create new kanban rules based on existing kanban rules.</span></span> <span data-ttu-id="39703-106">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="39703-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="39703-107">Protseduur on mõeldud protsessiinsenerile või väärtuse voo haldurile, kuna nad valmistavad ette tootmist muudetud tootmisvoo või uue täiendusreegli puhul.</span><span class="sxs-lookup"><span data-stu-id="39703-107">This procedure is intended for the process engineer or the value stream manager as they prepare production for a changed production flow or a new replenishment rule.</span></span>


## <a name="select-a-kanban-rule"></a><span data-ttu-id="39703-108">Kanban-reegli valimine</span><span class="sxs-lookup"><span data-stu-id="39703-108">Select a kanban rule</span></span>
1. <span data-ttu-id="39703-109">Minge jaotisse Kanban-reeglid.</span><span class="sxs-lookup"><span data-stu-id="39703-109">Go to Kanban rules.</span></span>
2. <span data-ttu-id="39703-110">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="39703-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="39703-111">Valige kanban-reegel 000017 tootele M0006.</span><span class="sxs-lookup"><span data-stu-id="39703-111">Select kanban rule 000017 for Product M0006.</span></span>  

## <a name="duplicate-a-kanban-rule"></a><span data-ttu-id="39703-112">Kanban-reegli dubleerimine</span><span class="sxs-lookup"><span data-stu-id="39703-112">Duplicate a kanban rule</span></span>
1. <span data-ttu-id="39703-113">Klõpsake suvandit Kanban-reegli dubleerimine.</span><span class="sxs-lookup"><span data-stu-id="39703-113">Click Duplicate kanban rule.</span></span>
    * <span data-ttu-id="39703-114">Kanban-reegli dubleerimisel on võimalik muuta tüüpi, kuupäeva, tegevusi ja tootevalikut.</span><span class="sxs-lookup"><span data-stu-id="39703-114">When duplicating a kanban rule, it is possible to change type, dates, activities, and the product selection.</span></span> <span data-ttu-id="39703-115">Selle protseduuri puhul saate toodet muuta järgmises etapis.</span><span class="sxs-lookup"><span data-stu-id="39703-115">Change the product for this procedure in the next step.</span></span>  
2. <span data-ttu-id="39703-116">Sisestage või valige väärtus väljal Toode.</span><span class="sxs-lookup"><span data-stu-id="39703-116">In the Product field, enter or select a value.</span></span>
    * <span data-ttu-id="39703-117">Valige suvand M0007.</span><span class="sxs-lookup"><span data-stu-id="39703-117">Select M0007.</span></span>  
3. <span data-ttu-id="39703-118">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="39703-118">Click OK.</span></span>
    * <span data-ttu-id="39703-119">Pange tähele, et luuakse kanban-reegli 000017 duplikaat.</span><span class="sxs-lookup"><span data-stu-id="39703-119">Note that a duplicate of kanban rule 000017 is created.</span></span>    

