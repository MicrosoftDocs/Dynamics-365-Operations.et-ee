---
title: 'Juhend: Nõudluse prognoosi käsitsi muutmine'
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
ms.openlocfilehash: 1e12ccf90b9971379e8931bd48d6243a855bb795
ms.sourcegitcommit: 15aacd0e109b05c7281407b5bba4e6cd99116c28
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/10/2021
ms.locfileid: "6224006"
---
# <a name="guide-modify-a-demand-forecast-manually"></a><span data-ttu-id="70d5e-103">Juhend: Nõudluse prognoosi käsitsi muutmine</span><span class="sxs-lookup"><span data-stu-id="70d5e-103">Guide: Modify a demand forecast manually</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="70d5e-104">See protseduur näitab, kuidas kauba prognoosi muuta.</span><span class="sxs-lookup"><span data-stu-id="70d5e-104">This procedure shows how to modify the forecast for an item.</span></span> <span data-ttu-id="70d5e-105">See protseduur on mõeldud tootmisplaanijale.</span><span class="sxs-lookup"><span data-stu-id="70d5e-105">This procedure is intended for the production planner.</span></span>

## <a name="modify-the-forecast-for-a-selected-item"></a><span data-ttu-id="70d5e-106">Valitud kauba prognoosi muutmine</span><span class="sxs-lookup"><span data-stu-id="70d5e-106">Modify the forecast for a selected item</span></span>

<span data-ttu-id="70d5e-107">Valitud kauba prognoosi muutmiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="70d5e-107">To modify the forecast for a selected item:</span></span>

1. <span data-ttu-id="70d5e-108">Avage **Moodulid \> Tooteteabe haldus \> Tooted \> Väljastatud tooted**.</span><span class="sxs-lookup"><span data-stu-id="70d5e-108">Go to **Modules \> Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="70d5e-109">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="70d5e-109">In the list, find and select the desired record.</span></span> <span data-ttu-id="70d5e-110">Valige kaup, mille puhul soovite prognoosi muuta.</span><span class="sxs-lookup"><span data-stu-id="70d5e-110">Select the item for which you want to modify the forecast.</span></span>
1. <span data-ttu-id="70d5e-111">Avage toimingupaanil vahekaart **Plaan** ja valige **Nõudlusprognoos**.</span><span class="sxs-lookup"><span data-stu-id="70d5e-111">On the Action Pane, open the **Plan** tab and select **Demand forecast**.</span></span>
1. <span data-ttu-id="70d5e-112">Valige loendist rida.</span><span class="sxs-lookup"><span data-stu-id="70d5e-112">In the list, select a row.</span></span> <span data-ttu-id="70d5e-113">Kui prognoosi read puuduvad, looge uus rida valides toiminguribal nuppu **Uus**.</span><span class="sxs-lookup"><span data-stu-id="70d5e-113">If there are no forecast lines, create a new line by selecting **New** on the Action Pane.</span></span>  
1. <span data-ttu-id="70d5e-114">Väljale **Müügi kogus** sisestage positiivne arv.</span><span class="sxs-lookup"><span data-stu-id="70d5e-114">In the **Sales quantity** field, enter a positive number.</span></span> <span data-ttu-id="70d5e-115">See number näitab kauba hinnangulist kogust.</span><span class="sxs-lookup"><span data-stu-id="70d5e-115">This number represents the forecasted quantity for the item.</span></span> <span data-ttu-id="70d5e-116">Negatiivse arvu sisestamisel kuvatakse tõrge.</span><span class="sxs-lookup"><span data-stu-id="70d5e-116">An error will be shown if you enter a negative number.</span></span>
1. <span data-ttu-id="70d5e-117">Täitke teised väljad, nagu vaja.</span><span class="sxs-lookup"><span data-stu-id="70d5e-117">Fill out the other fields as needed.</span></span>
1. <span data-ttu-id="70d5e-118">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="70d5e-118">Select **Save** on the Action Pane.</span></span>

## <a name="modify-the-forecast-for-one-or-more-items-with-microsoft-excel"></a><span data-ttu-id="70d5e-119">Ühe või mitme kauba eelarve muutmine rakendusega Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="70d5e-119">Modify the forecast for one or more items with Microsoft Excel</span></span>

<span data-ttu-id="70d5e-120">Ühe või mitme kauba eelarve muutmine rakendusega Microsoft Excel:</span><span class="sxs-lookup"><span data-stu-id="70d5e-120">To modify the forecast for one or more items with Microsoft Excel:</span></span>

1. <span data-ttu-id="70d5e-121">Tehke üht järgmistest valikutest.</span><span class="sxs-lookup"><span data-stu-id="70d5e-121">Do one of the following:</span></span>
    - <span data-ttu-id="70d5e-122">Avage leht **Nõudluse prognoosimine** mis tahes kauba jaoks (pole oluline, milline neist), nagu on kirjeldatud eelmises jaotises.</span><span class="sxs-lookup"><span data-stu-id="70d5e-122">Open the **Demand forecast** page for any item (it doesn't matter which one) as described in the previous section.</span></span>
    - <span data-ttu-id="70d5e-123">Avage K **oondplaneerimine \> Prognoosimine \>Käsitsi proggnoosisisend \> Nõudluse prognoosiread**.</span><span class="sxs-lookup"><span data-stu-id="70d5e-123">Go to **Master planning \> Forecasting \> Manual forecast entry \> Demand forecast lines**.</span></span>
1. <span data-ttu-id="70d5e-124">Avage toimingupaanil **Ava Microsoft Office \> Nõudlusprognoosi sissekanded**.</span><span class="sxs-lookup"><span data-stu-id="70d5e-124">On the Action Pane, select **Open in Microsoft Office \> Demand forecast entries**.</span></span>
1. <span data-ttu-id="70d5e-125">Valige allalaadimiskoht, salvestage ja avage allalaaditud fail Excelis.</span><span class="sxs-lookup"><span data-stu-id="70d5e-125">Select a download location, save, and then open the downloaded file in Excel.</span></span>
1. <span data-ttu-id="70d5e-126">Kui näete hoiatust, valige **Luba redigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="70d5e-126">If you see a warning, choose to **Enable editing**.</span></span>
1. <span data-ttu-id="70d5e-127">Logige Excelis Microsoft Dynamics tööpaani abil rakendusse Supply Chain Management sisse.</span><span class="sxs-lookup"><span data-stu-id="70d5e-127">In Excel, sign in to Supply Chain Management using the Microsoft Dynamics task pane.</span></span> <span data-ttu-id="70d5e-128">Peate sisse logima suvandiga **Hoia mind sisse logitud** ja usaldama andmeühendusrakendust.</span><span class="sxs-lookup"><span data-stu-id="70d5e-128">You must sign in with the **Keep me signed in** option enabled and you must trust the data connection app.</span></span>
1. <span data-ttu-id="70d5e-129">Exceli arvutustabelis kuvatakse nüüd kõik teie ettevõtte praegused nõudluse prognoosiread.</span><span class="sxs-lookup"><span data-stu-id="70d5e-129">The Excel spreadsheet now shows all the current demand forecast lines for your company.</span></span>  <span data-ttu-id="70d5e-130">Vajadusel lisage, kustutage ja muutke nõudluse prognoosi ridu.</span><span class="sxs-lookup"><span data-stu-id="70d5e-130">Add, delete, and edit demand forecast lines as needed.</span></span>
1. <span data-ttu-id="70d5e-131">Muudatuste tagasilaadimiseks rakendusse Supply Chain Management valige Microsoft Dynamics tööpaanil **Avalda**.</span><span class="sxs-lookup"><span data-stu-id="70d5e-131">Select **Publish** on the Microsoft Dynamics task pane to upload your changes back to Supply Chain Management.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
