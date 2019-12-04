---
title: Kulumimääramise tava muutmine mitme põhivara puhul
description: See ülesanne värskendab konkreetse põhivara grupi kulumiarvestusreegli.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysQueryForm, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 21baf3692cbcb87f6ed37459848376a1fa87a438
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177325"
---
# <a name="change-depreciation-conventions-for-multiple-fixed-assets"></a><span data-ttu-id="efcd6-103">Kulumimääramise tava muutmine mitme põhivara puhul</span><span class="sxs-lookup"><span data-stu-id="efcd6-103">Change depreciation conventions for multiple fixed assets</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="efcd6-104">See ülesanne värskendab konkreetse põhivara grupi kulumiarvestusreegli.</span><span class="sxs-lookup"><span data-stu-id="efcd6-104">This task updates the depreciation convention for a specified fixed asset group.</span></span> <span data-ttu-id="efcd6-105">See ülesande juhend kasutab demoettevõtet USMF.</span><span class="sxs-lookup"><span data-stu-id="efcd6-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="efcd6-106">Avage Põhivarad > Perioodilised ülesanded > Hulgivärskendamine</span><span class="sxs-lookup"><span data-stu-id="efcd6-106">Go to Fixed assets > Periodic tasks > Mass update</span></span>
2. <span data-ttu-id="efcd6-107">Klõpsake väljal Kulumiraamat otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="efcd6-107">In the Depreciation book field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="efcd6-108">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="efcd6-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="efcd6-109">Sisestage kuupäev väljale Teenusesse saatmise algus.</span><span class="sxs-lookup"><span data-stu-id="efcd6-109">In the Placed in service start field, enter a date.</span></span>
5. <span data-ttu-id="efcd6-110">Sisestage kuupäev väljale Teenusesse saatmise lõpp.</span><span class="sxs-lookup"><span data-stu-id="efcd6-110">In the Placed in service end field, enter a date.</span></span>
    * <span data-ttu-id="efcd6-111">Värskendatakse ainult varasid, mis kuuluvad valitud kulumiraamatusse ja mis on teenusesse saadetud nende kuupäevade vahel.</span><span class="sxs-lookup"><span data-stu-id="efcd6-111">Only assets that are a part of the select depreciation book and that have been placed in service between these dates will be updated.</span></span>  
6. <span data-ttu-id="efcd6-112">Valige suvand väljalt Praegune kulumiarvestusreegel.</span><span class="sxs-lookup"><span data-stu-id="efcd6-112">In the Current depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="efcd6-113">Värskendatakse ainult praeguse kulumiarvestusreegli varasid.</span><span class="sxs-lookup"><span data-stu-id="efcd6-113">Only assets that have the current depreciation convention will be updated.</span></span>  
7. <span data-ttu-id="efcd6-114">Valige suvand väljalt Uus kulumiarvestusreegel.</span><span class="sxs-lookup"><span data-stu-id="efcd6-114">In the New depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="efcd6-115">Kontrollige aruande printimist soovitud sihtkohta.</span><span class="sxs-lookup"><span data-stu-id="efcd6-115">Verify the report will print to the desired destination.</span></span>  
8. <span data-ttu-id="efcd6-116">Jaotise kaasamiseks laiendage kirjeid.</span><span class="sxs-lookup"><span data-stu-id="efcd6-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="efcd6-117">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="efcd6-117">Click Filter.</span></span>
10. <span data-ttu-id="efcd6-118">Valige loendist Põhivaragrupp.</span><span class="sxs-lookup"><span data-stu-id="efcd6-118">In the list, select the Fixed asset group.</span></span>
11. <span data-ttu-id="efcd6-119">Klõpsake väljal Kriteeriumid otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="efcd6-119">In the Criteria field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="efcd6-120">Valige soovitud Põhivaragrupp.</span><span class="sxs-lookup"><span data-stu-id="efcd6-120">Select the desired Fixed asset group.</span></span>
13. <span data-ttu-id="efcd6-121">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="efcd6-121">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="efcd6-122">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="efcd6-122">Click OK.</span></span>
15. <span data-ttu-id="efcd6-123">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="efcd6-123">Click OK.</span></span>
    *  <span data-ttu-id="efcd6-124">Protsessi tulemused kuvatakse aruandel Hulgivärskendamine.</span><span class="sxs-lookup"><span data-stu-id="efcd6-124">Results of the process are shown on the Mass update report.</span></span>     
