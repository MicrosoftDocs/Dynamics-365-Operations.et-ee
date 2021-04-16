---
title: Kulumimääramise tava muutmine mitme põhivara puhul
description: See ülesanne värskendab konkreetse põhivara grupi kulumiarvestusreegli.
author: saraschi2
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SysQueryForm, SrsReportViewerForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a71b24b0c2ea072aeff8c994cfdac10bc57b64c6
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823976"
---
# <a name="change-depreciation-conventions-for-multiple-fixed-assets"></a><span data-ttu-id="d0449-103">Kulumimääramise tava muutmine mitme põhivara puhul</span><span class="sxs-lookup"><span data-stu-id="d0449-103">Change depreciation conventions for multiple fixed assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d0449-104">See ülesanne värskendab konkreetse põhivara grupi kulumiarvestusreegli.</span><span class="sxs-lookup"><span data-stu-id="d0449-104">This task updates the depreciation convention for a specified fixed asset group.</span></span> <span data-ttu-id="d0449-105">See ülesande juhend kasutab demoettevõtet USMF.</span><span class="sxs-lookup"><span data-stu-id="d0449-105">This task guide uses the USMF demo company.</span></span>

1. <span data-ttu-id="d0449-106">Avage Põhivarad > Perioodilised ülesanded > Hulgivärskendamine</span><span class="sxs-lookup"><span data-stu-id="d0449-106">Go to Fixed assets > Periodic tasks > Mass update</span></span>
2. <span data-ttu-id="d0449-107">Klõpsake väljal Kulumiraamat otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="d0449-107">In the Depreciation book field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="d0449-108">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="d0449-108">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="d0449-109">Sisestage kuupäev väljale Teenusesse saatmise algus.</span><span class="sxs-lookup"><span data-stu-id="d0449-109">In the Placed in service start field, enter a date.</span></span>
5. <span data-ttu-id="d0449-110">Sisestage kuupäev väljale Teenusesse saatmise lõpp.</span><span class="sxs-lookup"><span data-stu-id="d0449-110">In the Placed in service end field, enter a date.</span></span>
    * <span data-ttu-id="d0449-111">Värskendatakse ainult varasid, mis kuuluvad valitud kulumiraamatusse ja mis on teenusesse saadetud nende kuupäevade vahel.</span><span class="sxs-lookup"><span data-stu-id="d0449-111">Only assets that are a part of the select depreciation book and that have been placed in service between these dates will be updated.</span></span>  
6. <span data-ttu-id="d0449-112">Valige suvand väljalt Praegune kulumiarvestusreegel.</span><span class="sxs-lookup"><span data-stu-id="d0449-112">In the Current depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="d0449-113">Värskendatakse ainult praeguse kulumiarvestusreegli varasid.</span><span class="sxs-lookup"><span data-stu-id="d0449-113">Only assets that have the current depreciation convention will be updated.</span></span>  
7. <span data-ttu-id="d0449-114">Valige suvand väljalt Uus kulumiarvestusreegel.</span><span class="sxs-lookup"><span data-stu-id="d0449-114">In the New depreciation convention field, select an option.</span></span>
    * <span data-ttu-id="d0449-115">Kontrollige aruande printimist soovitud sihtkohta.</span><span class="sxs-lookup"><span data-stu-id="d0449-115">Verify the report will print to the desired destination.</span></span>  
8. <span data-ttu-id="d0449-116">Jaotise kaasamiseks laiendage kirjeid.</span><span class="sxs-lookup"><span data-stu-id="d0449-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="d0449-117">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="d0449-117">Click Filter.</span></span>
10. <span data-ttu-id="d0449-118">Valige loendist Põhivaragrupp.</span><span class="sxs-lookup"><span data-stu-id="d0449-118">In the list, select the Fixed asset group.</span></span>
11. <span data-ttu-id="d0449-119">Klõpsake väljal Kriteeriumid otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="d0449-119">In the Criteria field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="d0449-120">Valige soovitud Põhivaragrupp.</span><span class="sxs-lookup"><span data-stu-id="d0449-120">Select the desired Fixed asset group.</span></span>
13. <span data-ttu-id="d0449-121">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="d0449-121">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="d0449-122">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d0449-122">Click OK.</span></span>
15. <span data-ttu-id="d0449-123">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="d0449-123">Click OK.</span></span>
    *  <span data-ttu-id="d0449-124">Protsessi tulemused kuvatakse aruandel Hulgivärskendamine.</span><span class="sxs-lookup"><span data-stu-id="d0449-124">Results of the process are shown on the Mass update report.</span></span>     



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]