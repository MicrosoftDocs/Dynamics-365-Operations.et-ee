---
title: Nõudluse prognoosi käsitsi muutmine
description: See teema kirjeldab, kuidas kauba prognoosi muuta
author: ChristianRytt
ms.date: 08/12/2019
ms.topic: business-process
ms.search.form: EcoResProductDetailsExtended, ForecastSales
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5da1d5b1fbd91964e695a704681b1c9ee513a2f1
ms.sourcegitcommit: 4016c223a985c46e33f9941bf91ba5e1583e1cfd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889020"
---
# <a name="modify-a-demand-forecast-manually"></a><span data-ttu-id="5122e-103">Nõudluse prognoosi käsitsi muutmine</span><span class="sxs-lookup"><span data-stu-id="5122e-103">Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5122e-104">See protseduur näitab, kuidas kauba prognoosi muuta.</span><span class="sxs-lookup"><span data-stu-id="5122e-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="5122e-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="5122e-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="5122e-106">See protseduur on mõeldud tootmisplaanijale.</span><span class="sxs-lookup"><span data-stu-id="5122e-106">This procedure is intended for the production planner.</span></span>

## <a name="modify-the-forecast-for-a-selected-item"></a><span data-ttu-id="5122e-107">Valitud kauba prognoosi muutmine</span><span class="sxs-lookup"><span data-stu-id="5122e-107">Modify the forecast for a selected item</span></span>

<span data-ttu-id="5122e-108">Valitud kauba prognoosi muutmiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="5122e-108">To modify the forecast for a selected item:</span></span>

1. <span data-ttu-id="5122e-109">Avage **Moodulid \> Tooteteabe haldus \> Tooted \> Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="5122e-109">Go to **Modules \> Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="5122e-110">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="5122e-110">In the list, find and select the desired record.</span></span> <span data-ttu-id="5122e-111">Valige kaup, mille puhul soovite prognoosi muuta.</span><span class="sxs-lookup"><span data-stu-id="5122e-111">Select the item for which you want to modify the forecast.</span></span>
1. <span data-ttu-id="5122e-112">Avage toimingupaanil vahekaart **Plaan** ja valige **Nõudlusprognoos**.</span><span class="sxs-lookup"><span data-stu-id="5122e-112">On the Action Pane, open the **Plan** tab and select **Demand forecast**.</span></span>
1. <span data-ttu-id="5122e-113">Valige loendist rida.</span><span class="sxs-lookup"><span data-stu-id="5122e-113">In the list, select a row.</span></span> <span data-ttu-id="5122e-114">Kui prognoosi read puuduvad, looge uus rida valides toiminguribal nuppu **Uus**.</span><span class="sxs-lookup"><span data-stu-id="5122e-114">If there are no forecast lines, create a new line by selecting **New** on the Action Pane.</span></span>  
1. <span data-ttu-id="5122e-115">Väljale **Müügi kogus** sisestage positiivne arv.</span><span class="sxs-lookup"><span data-stu-id="5122e-115">In the **Sales quantity** field, enter a positive number.</span></span> <span data-ttu-id="5122e-116">See number näitab kauba hinnangulist kogust.</span><span class="sxs-lookup"><span data-stu-id="5122e-116">This number represents the forecasted quantity for the item.</span></span> <span data-ttu-id="5122e-117">Negatiivse arvu sisestamisel kuvatakse tõrge.</span><span class="sxs-lookup"><span data-stu-id="5122e-117">An error will be shown if you enter a negative number.</span></span>
1. <span data-ttu-id="5122e-118">Täitke teised väljad, nagu vaja.</span><span class="sxs-lookup"><span data-stu-id="5122e-118">Fill out the other fields as needed.</span></span>
1. <span data-ttu-id="5122e-119">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="5122e-119">Select **Save** on the Action Pane.</span></span>

## <a name="modify-the-forecast-for-one-or-more-items-microsoft-excel"></a><span data-ttu-id="5122e-120">Ühe või mitme kauba eelarve muutmine rakenduses Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="5122e-120">Modify the forecast for one or more items Microsoft Excel</span></span>

<span data-ttu-id="5122e-121">Ühe või mitme kauba eelarve muutmiseks rakenduses Microsoft Excel toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="5122e-121">To modify the forecast for one or more items Microsoft Excel:</span></span>

1. <span data-ttu-id="5122e-122">Tehke üht järgmistest valikutest.</span><span class="sxs-lookup"><span data-stu-id="5122e-122">Do one of the following:</span></span>
    - <span data-ttu-id="5122e-123">Avage leht **Nõudluse prognoosimine** mis tahes kauba jaoks (pole oluline, milline neist), nagu on kirjeldatud eelmises jaotises.</span><span class="sxs-lookup"><span data-stu-id="5122e-123">Open the **Demand forecast** page for any item (it doesn't matter which one) as described in the previous section.</span></span>
    - <span data-ttu-id="5122e-124">Avage K **oondplaneerimine \> Prognoosimine \>Käsitsi proggnoosisisend \> Nõudluse prognoosiread**.</span><span class="sxs-lookup"><span data-stu-id="5122e-124">Go to **Master planning \> Forecasting \> Manual forecast entry \> Demand forecast lines**.</span></span>
1. <span data-ttu-id="5122e-125">Avage toimingupaanil **Ava Microsoft Office \> Nõudlusprognoosi sissekanded**.</span><span class="sxs-lookup"><span data-stu-id="5122e-125">On the Action Pane, select **Open in Microsoft Office \> Demand forecast entries**.</span></span>
1. <span data-ttu-id="5122e-126">Valige allalaadimiskoht, salvestage ja avage allalaaditud fail Excelis.</span><span class="sxs-lookup"><span data-stu-id="5122e-126">Select a download location, save, and then open the downloaded file in Excel.</span></span>
1. <span data-ttu-id="5122e-127">Kui näete hoiatust, valige **Luba redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="5122e-127">If you see a warning, choose to **Enable editing**.</span></span>
1. <span data-ttu-id="5122e-128">Logige Excelis Microsoft Dynamics tööpaani abil rakendusse Supply Chain Management sisse.</span><span class="sxs-lookup"><span data-stu-id="5122e-128">In Excel, sign in to Supply Chain Management using the Microsoft Dynamics task pane.</span></span> <span data-ttu-id="5122e-129">Peate sisse logima suvandiga **Hoia mind sisse logitud** ja usaldama andmeühendusrakendust.</span><span class="sxs-lookup"><span data-stu-id="5122e-129">You must sign in with the **Keep me signed in** option enabled and you must trust the data connection app.</span></span>
1. <span data-ttu-id="5122e-130">Exceli arvutustabelis kuvatakse nüüd kõik teie ettevõtte praegused nõudluse prognoosiread.</span><span class="sxs-lookup"><span data-stu-id="5122e-130">The Excel spreadsheet now shows all the current demand forecast lines for your company.</span></span>  <span data-ttu-id="5122e-131">Vajadusel lisage, kustutage ja muutke nõudluse prognoosi ridu.</span><span class="sxs-lookup"><span data-stu-id="5122e-131">Add, delete, and edit demand forecast lines as needed.</span></span>
1. <span data-ttu-id="5122e-132">Muudatuste tagasilaadimiseks rakendusse Supply Chain Management valige Microsoft Dynamics tööpaanil **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="5122e-132">Select **Publish** on the Microsoft Dynamics task pane to upload your changes back to Supply Chain Management.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
