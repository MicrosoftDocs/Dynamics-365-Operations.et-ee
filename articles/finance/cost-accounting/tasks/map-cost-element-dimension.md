---
title: Kuluelemendi dimensiooni vastendamine
description: Kulu kontrollija saab selle protseduuri abil vastendada kuluelemendi dimensiooni MXMF-i juriidilise isiku kuluelemendi dimensiooniga.
author: ShylaThompson
manager: AnnBe
ms.date: 06/28/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 346c64ffb19e320d0babf886c15f1b46959b4f32
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177346"
---
# <a name="map-a-cost-element-dimension"></a><span data-ttu-id="95fa0-103">Kuluelemendi dimensiooni vastendamine</span><span class="sxs-lookup"><span data-stu-id="95fa0-103">Map a cost element dimension</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="95fa0-104">Kulu kontrollija saab selle protseduuri abil vastendada kuluelemendi dimensiooni MXMF-i juriidilise isiku kuluelemendi dimensiooniga.</span><span class="sxs-lookup"><span data-stu-id="95fa0-104">A cost controller can use this procedure to map a cost element dimension to a cost element dimension in the MXMF legal entity.</span></span> <span data-ttu-id="95fa0-105">See salvestis kasutab USP2 demoandmete ettevõtet.</span><span class="sxs-lookup"><span data-stu-id="95fa0-105">This recording uses the USP2 demo data company.</span></span>

1. <span data-ttu-id="95fa0-106">Avage Kuluarvestus > Dimensioonid > Kuluelemendi dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="95fa0-106">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="95fa0-107">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="95fa0-107">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="95fa0-108">Selles näites valige Kuluelemendid.</span><span class="sxs-lookup"><span data-stu-id="95fa0-108">For this example, select Cost elements.</span></span>  
3. <span data-ttu-id="95fa0-109">Klõpsake suvandit Dimensioonide vastendused.</span><span class="sxs-lookup"><span data-stu-id="95fa0-109">Click Dimension mappings.</span></span>
4. <span data-ttu-id="95fa0-110">Klõpsake suvandit Konfigureeri vastendused sellest dimensioonist.</span><span class="sxs-lookup"><span data-stu-id="95fa0-110">Click Configure mappings from this dimension.</span></span>
5. <span data-ttu-id="95fa0-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="95fa0-111">Click New.</span></span>
6. <span data-ttu-id="95fa0-112">Sisestage või valige väärtus väljal Sihtdimensioon.</span><span class="sxs-lookup"><span data-stu-id="95fa0-112">In the To dimension field, enter or select a value.</span></span>
    * <span data-ttu-id="95fa0-113">Selles näites valige MXMF-i kuluelemendid.</span><span class="sxs-lookup"><span data-stu-id="95fa0-113">For this example, select MXMF Cost elements.</span></span>  
7. <span data-ttu-id="95fa0-114">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="95fa0-114">Click New.</span></span>
8. <span data-ttu-id="95fa0-115">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="95fa0-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="95fa0-116">Sisestage või valige väärtus väljal Lähtedimensiooni liige.</span><span class="sxs-lookup"><span data-stu-id="95fa0-116">In the From dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="95fa0-117">Selle näite puhul valige dimensiooniliikme 606400 Telefoni ja faksi kulu.</span><span class="sxs-lookup"><span data-stu-id="95fa0-117">For this example, select dimension member 606400 Telephone & Fax Expense.</span></span>  
10. <span data-ttu-id="95fa0-118">Sisestage või valige väärtus väljal Sihtdimensiooni liige.</span><span class="sxs-lookup"><span data-stu-id="95fa0-118">In the To dimension member field, enter or select a value.</span></span>
    * <span data-ttu-id="95fa0-119">Näiteks saate valida dimensiooniliikme 6001004 Telefon.</span><span class="sxs-lookup"><span data-stu-id="95fa0-119">For this example, select dimension member 6001004 Telefono.</span></span>  
11. <span data-ttu-id="95fa0-120">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="95fa0-120">Click Save.</span></span>
