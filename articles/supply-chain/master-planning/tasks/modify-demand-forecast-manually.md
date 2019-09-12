---
title: Nõudluse prognoosi käsitsi muutmine
description: See protseduur näitab, kuidas kauba prognoosi muuta.
author: ShylaThompson
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1ec1edb861619bae2ae3c211720b55e170b83ec9
ms.sourcegitcommit: cbcf344b3b552acca56c3e27606eac7f2f124afe
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/22/2019
ms.locfileid: "1916618"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="979c4-103">Nõudluse prognoosi käsitsi muutmine</span><span class="sxs-lookup"><span data-stu-id="979c4-103">Modify a demand forecast manually</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="979c4-104">See protseduur näitab, kuidas kauba prognoosi muuta.</span><span class="sxs-lookup"><span data-stu-id="979c4-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="979c4-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="979c4-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="979c4-106">Registreerimine on mõeldud tootmise planeerijale.</span><span class="sxs-lookup"><span data-stu-id="979c4-106">This recording is intended for the production planner.</span></span> 


## <a name="modify-the-forecast-for-an-item"></a><span data-ttu-id="979c4-107">Kauba prognoosi muutmine</span><span class="sxs-lookup"><span data-stu-id="979c4-107">Modify the forecast for an item</span></span>
1. <span data-ttu-id="979c4-108">**Navigeerimispaanil** avage **Moodulid > Toote teabe haldus > Tooted > Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="979c4-108">In the **Navigation pane**, go to **Modules > Product information management > Products > Released products**.</span></span>
2. <span data-ttu-id="979c4-109">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="979c4-109">In the list, find and select the desired record.</span></span> <span data-ttu-id="979c4-110">Valige kaup, mille puhul soovite prognoosi muuta.</span><span class="sxs-lookup"><span data-stu-id="979c4-110">Select the item for which you want to modify the forecast.</span></span> <span data-ttu-id="979c4-111">Näiteks saate valida kauba D0001.</span><span class="sxs-lookup"><span data-stu-id="979c4-111">For example, you can select item D0001.</span></span>  
3. <span data-ttu-id="979c4-112">Klõpsake **Toimingupaanil** valikut **Plaan**.</span><span class="sxs-lookup"><span data-stu-id="979c4-112">On the **Action Pane**, click **Plan**.</span></span>
4. <span data-ttu-id="979c4-113">Klõpsake **Nõudluse prognoos**.</span><span class="sxs-lookup"><span data-stu-id="979c4-113">Click **Demand forecast**.</span></span>
5. <span data-ttu-id="979c4-114">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="979c4-114">In the list, mark the selected row.</span></span> <span data-ttu-id="979c4-115">Kui prognoosi read puuduvad, looge uus rida klõpsates rakendusribal nuppu Uus.</span><span class="sxs-lookup"><span data-stu-id="979c4-115">If there are no forecast lines, create a new line by clicking New on the app bar.</span></span>  
6. <span data-ttu-id="979c4-116">Väljale **Müügi kogus** sisestage arv.</span><span class="sxs-lookup"><span data-stu-id="979c4-116">In the **Sales quantity** field, enter a number.</span></span> <span data-ttu-id="979c4-117">See number näitab kauba hinnangulist kogust.</span><span class="sxs-lookup"><span data-stu-id="979c4-117">This number represents the forecasted quantity for the item.</span></span>  
7. <span data-ttu-id="979c4-118">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="979c4-118">Click Save.</span></span>

## <a name="modify-the-forecast-in-excel"></a><span data-ttu-id="979c4-119">Prognoosi muutmine Excelis</span><span class="sxs-lookup"><span data-stu-id="979c4-119">Modify the forecast in Excel</span></span>
1. <span data-ttu-id="979c4-120">Klõpsake **Ava** lahenduses Microsoft Office.</span><span class="sxs-lookup"><span data-stu-id="979c4-120">Click **Open** in Microsoft Office.</span></span>
2. <span data-ttu-id="979c4-121">Klõpsake Excelis **Nõudluse prognoosi redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="979c4-121">Click **Edit Demand forecast** in Excel.</span></span> <span data-ttu-id="979c4-122">Excelis saate nõudluse prognoosi ridu lisada, kustutada ja muuta.</span><span class="sxs-lookup"><span data-stu-id="979c4-122">In Excel, you can add, delete and edit demand forecast lines.</span></span> <span data-ttu-id="979c4-123">Kui te andmeid Excelis ei näe, peate sisse logima rakendusse Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, nii et suvand Hoia mind sisselogituna on lubatud ja peate andmeühenduse rakendust usaldama.</span><span class="sxs-lookup"><span data-stu-id="979c4-123">If you are not able to see the data in Excel, you need to sign in to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition with the "Keep me signed in" option enabled and you need to trust the data connection app.</span></span>  

