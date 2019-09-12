---
title: Üksus, kus on kasutatud
description: Selles teemas kirjeldatakse, kuidas saada ülevaadet, kuidas üksust kasutatakse varahalduses.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 84ab803aedf5b803b6c5f39ff1907726335cb45d
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918322"
---
# <a name="item-where-used"></a><span data-ttu-id="89d3e-103">Üksus, kus on kasutatud</span><span class="sxs-lookup"><span data-stu-id="89d3e-103">Item where used</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="89d3e-104">Saate arvutada kindlat üksust, et saada ülevaade, kus vara halduses seda üksust on kasutatud.</span><span class="sxs-lookup"><span data-stu-id="89d3e-104">You can make a calculation for a specific item to get an overview of where in Asset Management the item has been used.</span></span> <span data-ttu-id="89d3e-105">Tulemused näitavad konteksti, milles üksust on kasutatud selle kasutusea jooksul.</span><span class="sxs-lookup"><span data-stu-id="89d3e-105">The results show the context in which the item has been used during its lifetime.</span></span> <span data-ttu-id="89d3e-106">Lehte **Üksus, kus kasutatud** saab avada vara halduse põhimenüüst ja sellele pääseb juurde ka järgmistelt lehtedelt:</span><span class="sxs-lookup"><span data-stu-id="89d3e-106">The **Item where used** page can be opened from the main Asset management menu, and it can also be accessed from the following pages:</span></span>

[<span data-ttu-id="89d3e-107">Vara kooslus</span><span class="sxs-lookup"><span data-stu-id="89d3e-107">Asset BOM</span></span>](../objects/object-BOM.md)

[<span data-ttu-id="89d3e-108">Vara tavatüübi varuosad</span><span class="sxs-lookup"><span data-stu-id="89d3e-108">Spare parts on asset type defaults</span></span>](../setup-for-objects/object-types.md)

[<span data-ttu-id="89d3e-109">Üksuse ennustamine hooldustöö tüübi tavaennustamisel</span><span class="sxs-lookup"><span data-stu-id="89d3e-109">Item forecast on Maintenance job type defaults forecast</span></span>](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

[<span data-ttu-id="89d3e-110">Töökäsu hooldusprognoos</span><span class="sxs-lookup"><span data-stu-id="89d3e-110">Work order maintenance forecast</span></span>](../work-orders/maintenance-forecasts.md)

[<span data-ttu-id="89d3e-111">Töökäsu ostutaotlus</span><span class="sxs-lookup"><span data-stu-id="89d3e-111">Work order purchase requisition</span></span>](../work-orders/procurement.md)

[<span data-ttu-id="89d3e-112">Töökäsu ost</span><span class="sxs-lookup"><span data-stu-id="89d3e-112">Work order purchase</span></span>](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a><span data-ttu-id="89d3e-113">Looge „Üksus, kus kasutatud“ arvutus</span><span class="sxs-lookup"><span data-stu-id="89d3e-113">Make an item-where-used calculation</span></span>

1. <span data-ttu-id="89d3e-114">Klõpsake **Vara haldus** > **Päringud** > **Üksus, kus kasutatud** või valige ühes ülal mainitud lehel nupp **Üksus, kus kasutatud**.</span><span class="sxs-lookup"><span data-stu-id="89d3e-114">Click **Asset management** > **Inquiries** > **Item where used**, or select the **Item where used** button on one of the pages mentioned above.</span></span>

2. <span data-ttu-id="89d3e-115">Dialoogis **Üksus, kus kasutatud** valige üksus, mida tahate arvutada väljas **Üksuse number**.</span><span class="sxs-lookup"><span data-stu-id="89d3e-115">In the **Item where used** dialog, select the item for which you want to make the calculation in the **Item number** field.</span></span>

3. <span data-ttu-id="89d3e-116">Väljaga **Tase** saate määrata, kui täpsed töö asukohtade üksuse read on.</span><span class="sxs-lookup"><span data-stu-id="89d3e-116">You can use the **Level** field to indicate how detailed you want the item lines to be regarding functional locations.</span></span> <span data-ttu-id="89d3e-117">Näiteks, kui sisestate välja numbri „1“ ja teil on mitmetasemeline töö asukoha ülesehitus, näidatakse ülemisel tasemel töö asukoha kõiki üksuse ridu.</span><span class="sxs-lookup"><span data-stu-id="89d3e-117">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all item lines for a functional location will be shown on the top level.</span></span> <span data-ttu-id="89d3e-118">Seega suhe/kogus rea kohta võidakse lisada madalama taseme töö asukohtadest.</span><span class="sxs-lookup"><span data-stu-id="89d3e-118">Therefore, relation/quantity on a line may be added up from functional locations located at a lower level.</span></span> <span data-ttu-id="89d3e-119">Kui sisestate välja **Tase** numbri „0“, näete põhjalikku tulemust, kus on näidatud asjakohaste kõikide töö asukoha tasemete kõik üksuse read.</span><span class="sxs-lookup"><span data-stu-id="89d3e-119">If you insert the number "0" in the **Level** field, you will see a detailed result showing all item lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="89d3e-120">Jaotises **Kaasamine** valige arvutusse lisatavate vahetamisnuppude seast „Jah“.</span><span class="sxs-lookup"><span data-stu-id="89d3e-120">In the **Include** section, select "Yes" on the toggle buttons that you want to include in the calculation.</span></span>

5. <span data-ttu-id="89d3e-121">Arvutuse alustamiseks klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="89d3e-121">Click **OK** to start the calculation.</span></span>

6. <span data-ttu-id="89d3e-122">Valige vahekaardi **Üksus, kus kasutatud** > toimingupaani rühmas **Rühmita alusel...** asjakohaseid nuppe, et näidata arvutuse nõutavate andmete taset.</span><span class="sxs-lookup"><span data-stu-id="89d3e-122">On the **Item where used** tab > **Group by...** action pane groups, select the relevant buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="89d3e-123">Valitud toimingupaani nupud on esile tõstetud.</span><span class="sxs-lookup"><span data-stu-id="89d3e-123">The selected action pane buttons are highlighted.</span></span> <span data-ttu-id="89d3e-124">Nupu aktiveerimiseks või inaktiveerimiseks klõpsake sellel.</span><span class="sxs-lookup"><span data-stu-id="89d3e-124">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="89d3e-125">Kui tahate näidata üksusega seotud dimensioone, klõpsake **Näita dimensioone** ja valige näidatavad dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="89d3e-125">If you want to show dimensions related to the item, click **Display dimensions**, and select the dimensions to be shown.</span></span>

<span data-ttu-id="89d3e-126">Alloleval joonisel on näide üksuse numbri „1000“ „Üksus, kus kasutatud“ arvutusest.</span><span class="sxs-lookup"><span data-stu-id="89d3e-126">In the figure below, you see an example of an item-where-used calculation for item number "1000".</span></span>

![Joonis 1](media/12-controlling-and-reporting.png)

