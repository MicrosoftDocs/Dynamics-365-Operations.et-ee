---
title: Lao vanemate partiide mobiilses seadmes kuvamise konfigureerimine
description: Selles teemas kirjeldatakse mobiilse seadme seadistamist kuvama asukohtade loendit partiidega, mis on vanemad kui töörea praegune asukoht.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5b1c9452a811d662976a25993264be0617ac67fe
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426241"
---
# <a name="configure-display-older-batches-within-warehouse-on-a-mobile-device"></a><span data-ttu-id="124b4-103">Lao vanemate partiide mobiilses seadmes kuvamise konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="124b4-103">Configure Display older batches within warehouse on a mobile device</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="124b4-104">Konfiguratsioon **Kuva vanemad partiid laos** võimaldab kuvada loendi asukohtadest vanemate partiidega kui töörea praegune asukoht.</span><span class="sxs-lookup"><span data-stu-id="124b4-104">The **Display older batches within warehouse** configuration lets you display a list of locations with batches older than the current location of the work line.</span></span> <span data-ttu-id="124b4-105">Kuvatav asukohtade loend sisaldab teavet asukohas olevate vanemate partiide kohta koos iga partii aegumiskuupäeva ja füüsilise varuga.</span><span class="sxs-lookup"><span data-stu-id="124b4-105">The list of locations that are displayed includes information about the older batches in the location with the expiration date and the physical inventory of each batch.</span></span> <span data-ttu-id="124b4-106">Saate valida uuest asukohast komplekteerimise või jätkata komplekteerimist praegusest asukohast.</span><span class="sxs-lookup"><span data-stu-id="124b4-106">You can choose to pick from a new location or to continue picking from the current location.</span></span> 
- <span data-ttu-id="124b4-107">Komplekteerimine uuest asukohast – kui valite komplekteerimiseks uue asukoha, värskendatakse praegust töörida, et kasutada uut asukohta, ning töö jätkub tavapäraselt uue asukohaga.</span><span class="sxs-lookup"><span data-stu-id="124b4-107">Pick from a new location - If you select a new location to pick from, the  current work line will be updated to use the new location and work will continue as usual with the new location.</span></span> <span data-ttu-id="124b4-108">Selleks et uus asukoht kehtiks, peab sel olema kogu töörea ulatuses piisav saadaolev kogus.</span><span class="sxs-lookup"><span data-stu-id="124b4-108">For the new location to be valid, it must have enough available quantity for the whole work line.</span></span> <span data-ttu-id="124b4-109">Kui nõutud kogus pole saadaval, siis töörida ei värskendata ja kuvatakse loend.</span><span class="sxs-lookup"><span data-stu-id="124b4-109">If the required quantity is not available, the work line will not be updated, and the list will display.</span></span> 
- <span data-ttu-id="124b4-110">Komplekteerimise jätkamine praegusest asukohast – kui jätkate praeguse töörea asukohaga, komplekteeritakse töörea koguseid edasi algsest asukohast.</span><span class="sxs-lookup"><span data-stu-id="124b4-110">Continue picking from the current location - If you continue with the current work line location, the quantities for the work line will continue to be picked from the original location.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="124b4-111">Kus see kehtib</span><span class="sxs-lookup"><span data-stu-id="124b4-111">Where it applies</span></span>
<span data-ttu-id="124b4-112">Laos olevate vanemate partiide kuvamine on konfigureeritud mobiilse seadme menüüelementides ja see mõjutab allpool nimetatud partii komplekteerimist.</span><span class="sxs-lookup"><span data-stu-id="124b4-112">Display older batches within warehouse is configured on mobile device menu items and affects the pick for batch below items.</span></span>

## <a name="set-up-display-older-batches-within-warehouse"></a><span data-ttu-id="124b4-113">Laos olevate vanemate partiide kuvamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="124b4-113">Set up Display older batches within warehouse</span></span>
<span data-ttu-id="124b4-114">Konfiguratsioon **Laos olevate vanemate partiide kuvamine** on saadaval mobiilse seadme menüüelementides, kui suvandi **Komplekteeri vanim partii** sätteks on valitud **Hoiata**.</span><span class="sxs-lookup"><span data-stu-id="124b4-114">The **Display older batches within warehouse** configuration is available on mobile device menu items when the **Pick oldest batch** option is set to **Warn**.</span></span>

- <span data-ttu-id="124b4-115">Valige menüüs **Laohaldus** > **Seadistus** > **Mobiilne seade** > **Mobiilse seadme menüüelemendid** suvandi **Kasuta olemasolevat tööd** sätteks menüüelemendi puhul **Jah** ja valige väljal **Komplekteeri vanim partii** säte **Hoiata**.</span><span class="sxs-lookup"><span data-stu-id="124b4-115">Under **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**, set **Use existing work** to **Yes** for the menu item, and select **Warn** in the **Pick oldest batch** field.</span></span> 

