---
title: Üksus, kus on kasutatud
description: Selles teemas kirjeldatakse, kuidas saada ülevaadet, kuidas üksust kasutatakse varahalduses.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetItemWhereUsed, EntAssetItemWhereUsedCalculate
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: bc78568e314c7cf83848ed2c39f9613d6ed638ba
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889621"
---
# <a name="item-where-used"></a><span data-ttu-id="2571e-103">Üksus, kus on kasutatud</span><span class="sxs-lookup"><span data-stu-id="2571e-103">Item where used</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="2571e-104">Saate arvutada kindlat üksust, et saada ülevaade, kus vara halduses seda üksust on kasutatud.</span><span class="sxs-lookup"><span data-stu-id="2571e-104">You can make a calculation for a specific item to get an overview of where in Asset Management the item has been used.</span></span> <span data-ttu-id="2571e-105">Tulemused näitavad konteksti, milles üksust on kasutatud selle kasutusea jooksul.</span><span class="sxs-lookup"><span data-stu-id="2571e-105">The results show the context in which the item has been used during its lifetime.</span></span> <span data-ttu-id="2571e-106">Lehte **Üksus, kus kasutatud** saab avada varahalduse põhimenüüst ja sellele pääseb juurde ka järgmistelt lehtedelt:</span><span class="sxs-lookup"><span data-stu-id="2571e-106">The **Item where used** page can be opened from the main Asset Management menu, and it can also be accessed from the following pages:</span></span>

- [<span data-ttu-id="2571e-107">Vara kooslused</span><span class="sxs-lookup"><span data-stu-id="2571e-107">Asset BOMs</span></span>](../objects/object-BOM.md)

- [<span data-ttu-id="2571e-108">Vara tavatüübi varuosad</span><span class="sxs-lookup"><span data-stu-id="2571e-108">Spare parts on asset type defaults</span></span>](../setup-for-objects/object-types.md#spare-parts-on-the-asset-type-setup)

- [<span data-ttu-id="2571e-109">Hooldustööde tüüpide kategooriad ja hooldustööde tüübid, hooldustööde tüüpide variandid, hooldustööde kaubandus ja hoolduse kontrollnimekirjad</span><span class="sxs-lookup"><span data-stu-id="2571e-109">Maintenance job type categories and maintenance job types, maintenance job type variants, maintenance job trades, and maintenance checklists</span></span>](../setup-for-work-orders/job-groups-and-job-types-variants-trades-and-checklists.md)

- [<span data-ttu-id="2571e-110">Hooldusprognoos</span><span class="sxs-lookup"><span data-stu-id="2571e-110">Maintenance forecast</span></span>](../work-orders/maintenance-forecasts.md)

- [<span data-ttu-id="2571e-111">Hange</span><span class="sxs-lookup"><span data-stu-id="2571e-111">Procurement</span></span>](../work-orders/procurement.md)

- [<span data-ttu-id="2571e-112">Töökäsu ost</span><span class="sxs-lookup"><span data-stu-id="2571e-112">Work order purchase</span></span>](../work-orders/procurement.md)

## <a name="make-an-item-where-used-calculation"></a><span data-ttu-id="2571e-113">Looge „Üksus, kus kasutatud“ arvutus</span><span class="sxs-lookup"><span data-stu-id="2571e-113">Make an item-where-used calculation</span></span>

1. <span data-ttu-id="2571e-114">Klõpsake **Vara haldus** > **Päringud** > **Üksus, kus kasutatud** või valige ühes ülal mainitud lehel nupp **Üksus, kus kasutatud**.</span><span class="sxs-lookup"><span data-stu-id="2571e-114">Click **Asset management** > **Inquiries** > **Item where used**, or select the **Item where used** button on one of the pages mentioned above.</span></span>

2. <span data-ttu-id="2571e-115">Dialoogis **Üksus, kus kasutatud** valige üksus, mida tahate arvutada väljas **Üksuse number**.</span><span class="sxs-lookup"><span data-stu-id="2571e-115">In the **Item where used** dialog, select the item for which you want to make the calculation in the **Item number** field.</span></span>

3. <span data-ttu-id="2571e-116">Väljaga **Tase** saate määrata, kui täpsed töö asukohtade üksuse read on.</span><span class="sxs-lookup"><span data-stu-id="2571e-116">You can use the **Level** field to indicate how detailed you want the item lines to be regarding functional locations.</span></span> 

    <span data-ttu-id="2571e-117">Näiteks, kui sisestate välja numbri „1“ ja teil on mitmetasemeline töö asukoha ülesehitus, näidatakse ülemisel tasemel töö asukoha kõiki üksuse ridu.</span><span class="sxs-lookup"><span data-stu-id="2571e-117">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all item lines for a functional location will be shown on the top level.</span></span> <span data-ttu-id="2571e-118">Seega suhe/kogus rea kohta võidakse lisada madalama taseme töö asukohtadest.</span><span class="sxs-lookup"><span data-stu-id="2571e-118">Therefore, relation/quantity on a line may be added up from functional locations located at a lower level.</span></span> 
    
    <span data-ttu-id="2571e-119">Kui sisestate välja **Tase** numbri „0“, näete põhjalikku tulemust, kus on näidatud asjakohaste kõikide töö asukoha tasemete kõik üksuse read.</span><span class="sxs-lookup"><span data-stu-id="2571e-119">If you insert the number "0" in the **Level** field, you will see a detailed result showing all item lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="2571e-120">Jaotises **Kaasamine** valige arvutusse lisatavate vahetamisnuppude seast „Jah“.</span><span class="sxs-lookup"><span data-stu-id="2571e-120">In the **Include** section, select "Yes" on the toggle buttons that you want to include in the calculation.</span></span>

5. <span data-ttu-id="2571e-121">Arvutuse alustamiseks klõpsake **OK**.</span><span class="sxs-lookup"><span data-stu-id="2571e-121">Click **OK** to start the calculation.</span></span>

6. <span data-ttu-id="2571e-122">Valige vahekaardi **Üksus, kus kasutatud** nupud  **Rühmitusalus**, et näidata arvutuse nõutavate andmete taset.</span><span class="sxs-lookup"><span data-stu-id="2571e-122">On the **Item where used** tab, select the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="2571e-123">Valitud nupud **Rühmitusalus** on esile tõstetud.</span><span class="sxs-lookup"><span data-stu-id="2571e-123">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="2571e-124">Nupu aktiveerimiseks või inaktiveerimiseks klõpsake sellel.</span><span class="sxs-lookup"><span data-stu-id="2571e-124">Click on a button to activate or deactivate it.</span></span>

7. <span data-ttu-id="2571e-125">Kui tahate näidata üksusega seotud dimensioone, klõpsake **Näita dimensioone** ja valige näidatavad dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="2571e-125">If you want to show dimensions related to the item, click **Display dimensions**, and select the dimensions to be shown.</span></span>

## <a name="example"></a><span data-ttu-id="2571e-126">Näide</span><span class="sxs-lookup"><span data-stu-id="2571e-126">Example</span></span>

<span data-ttu-id="2571e-127">Alloleval kuvatõmmisel on näide üksuse numbri „1000“ „Üksus, kus kasutatud“ arvutusest.</span><span class="sxs-lookup"><span data-stu-id="2571e-127">In the screenshot below, you see an example of an item-where-used calculation for item number "1000".</span></span>

![„Üksus, kus kasutatud“ arvutuse näide](media/12-controlling-and-reporting.png)

