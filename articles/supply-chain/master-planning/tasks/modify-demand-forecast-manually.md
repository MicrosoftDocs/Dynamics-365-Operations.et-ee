--- 
title: "Nõudluse prognoosi käsitsi muutmine"
description: "See protseduur näitab, kuidas kauba prognoosi muuta."
author: ShylaThompson
manager: AnnBe
ms.date: 11/15/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 72080dc7782320e82a3eabf7498c816495721b2d
ms.contentlocale: et-ee
ms.lasthandoff: 08/07/2018

---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="eae88-103">Nõudluse prognoosi käsitsi muutmine</span><span class="sxs-lookup"><span data-stu-id="eae88-103">Modify a demand forecast manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="eae88-104">See protseduur näitab, kuidas kauba prognoosi muuta.</span><span class="sxs-lookup"><span data-stu-id="eae88-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="eae88-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="eae88-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="eae88-106">Registreerimine on mõeldud tootmise planeerijale.</span><span class="sxs-lookup"><span data-stu-id="eae88-106">This recording is intended for the production planner.</span></span> 


## <a name="modify-the-forecast-for-an-item"></a><span data-ttu-id="eae88-107">Kauba prognoosi muutmine</span><span class="sxs-lookup"><span data-stu-id="eae88-107">Modify the forecast for an item</span></span>
1. <span data-ttu-id="eae88-108">Avage Tooteteabe haldus > Tooted > Väljastatud tooted.</span><span class="sxs-lookup"><span data-stu-id="eae88-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="eae88-109">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="eae88-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="eae88-110">Valige kaup, mille puhul soovite prognoosi muuta.</span><span class="sxs-lookup"><span data-stu-id="eae88-110">Select the item for which you want to modify the forecast.</span></span> <span data-ttu-id="eae88-111">Näiteks saate valida kauba D0001.</span><span class="sxs-lookup"><span data-stu-id="eae88-111">For example, you can select item D0001.</span></span>  
3. <span data-ttu-id="eae88-112">Klõpsake toimingupaanil valikut Plaan.</span><span class="sxs-lookup"><span data-stu-id="eae88-112">On the Action Pane, click Plan.</span></span>
4. <span data-ttu-id="eae88-113">Klõpsake valikut Nõudluse prognoos.</span><span class="sxs-lookup"><span data-stu-id="eae88-113">Click Demand forecast.</span></span>
5. <span data-ttu-id="eae88-114">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="eae88-114">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="eae88-115">Kui prognoosiridu ei ole, saab luua uue rea, </span><span class="sxs-lookup"><span data-stu-id="eae88-115">If there are no forecast lines, create a new line by  .</span></span> <span data-ttu-id="eae88-116">klõpsates rakenduse real nuppu Uus.</span><span class="sxs-lookup"><span data-stu-id="eae88-116">clicking New on the app bar.</span></span>  
6. <span data-ttu-id="eae88-117">Sisestage number väljale Müügikogus.</span><span class="sxs-lookup"><span data-stu-id="eae88-117">In the Sales quantity field, enter a number.</span></span>
    * <span data-ttu-id="eae88-118">See number näitab kauba hinnangulist kogust.</span><span class="sxs-lookup"><span data-stu-id="eae88-118">This number represents the forecasted quantity for the item.</span></span>  
7. <span data-ttu-id="eae88-119">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="eae88-119">Click Save.</span></span>

## <a name="modify-the-forecast-in-excel"></a><span data-ttu-id="eae88-120">Prognoosi muutmine Excelis</span><span class="sxs-lookup"><span data-stu-id="eae88-120">Modify the forecast in Excel</span></span>
1. <span data-ttu-id="eae88-121">Klõpsake suvandit Ava Microsoft Office’is.</span><span class="sxs-lookup"><span data-stu-id="eae88-121">Click Open in Microsoft Office.</span></span>
2. <span data-ttu-id="eae88-122">Klõpsake suvandit Nõudluse prognoosi korrigeerimine Excelis.</span><span class="sxs-lookup"><span data-stu-id="eae88-122">Click Edit Demand forecast in Excel.</span></span>
    * <span data-ttu-id="eae88-123">Excelis saate nõudluse prognoosi ridu lisada, kustutada ja muuta.</span><span class="sxs-lookup"><span data-stu-id="eae88-123">In Excel, you can add, delete and edit demand forecast lines.</span></span> <span data-ttu-id="eae88-124">Kui te andmeid Excelis ei näe, peate sisse logima rakendusse Microsoft Dynamics 365 for Finance and Operations, nii et suvand Hoia mind sisselogituna on lubatud ja peate andmeühenduse rakendust usaldama.</span><span class="sxs-lookup"><span data-stu-id="eae88-124">If you are not able to see the data in Excel, you need to sign in to Microsoft Dynamics 365 for Finance and Operations with the "Keep me signed in" option enabled and you need to trust the data connection app.</span></span>  


