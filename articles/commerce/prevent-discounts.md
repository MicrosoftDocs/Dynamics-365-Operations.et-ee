---
title: Jaetoodete allahindluste vältimise suvandid
description: On erinevaid põhjuseid, miks jaemüüjad soovivad vältida mõne toote allahindlust kampaania ajal või kassas.
author: jblucher
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailPeriodicDiscount
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 85183
ms.assetid: e8c5a24f-7edd-4fd6-af80-5e0ac9f03127
ms.search.region: Global
ms.search.industry: Retail
ms.author: jeffbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.openlocfilehash: 822bd39bca3a95f073bacea90a8ee58eada50ae2
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/01/2020
ms.locfileid: "3022309"
---
# <a name="options-for-preventing-discounts-for-retail-products"></a><span data-ttu-id="46574-103">Jaetoodete allahindluste vältimise suvandid</span><span class="sxs-lookup"><span data-stu-id="46574-103">Options for preventing discounts for retail products</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="46574-104">On erinevaid põhjuseid, miks jaemüüjad soovivad vältida mõne toote allahindlust kampaania ajal või kassas.</span><span class="sxs-lookup"><span data-stu-id="46574-104">There are various reasons why retailers may want to prevent some products from being discounted, either from a promotion or during the sale at the POS.</span></span>

<span data-ttu-id="46574-105">Avaldatud toodete vahekaardil **Commerce** leitavaid suvandeid saab kasutada toote konfigureerimiseks, et välistada kõiki või käsitsi lisatud allahindluseid.</span><span class="sxs-lookup"><span data-stu-id="46574-105">The following options, which can be found on the **Commerce** tab of released products, will allow the product to be configured to prevent all or manual discounts.</span></span> <span data-ttu-id="46574-106">Sätteid saab määrata ka kategooria kaupa jaemüügi kategooriahierarhiast.</span><span class="sxs-lookup"><span data-stu-id="46574-106">The settings can also be specified at the category level from the retail category hierarchy.</span></span>

- <span data-ttu-id="46574-107">**Kõikide allahindluste vältimine**: valige see suvand, et vältida tootele ükskõik mis tüüpi allahindluse rakendamist.</span><span class="sxs-lookup"><span data-stu-id="46574-107">**Prevent all discounts** – Select this option to prevent all types of discounts from being applied to this product.</span></span> <span data-ttu-id="46574-108">Siia kuuluvad erinevad pakkumised (nt toodete kombineerimine, koguse- ja läveallahindlused) ja käsitsi lisatud toote- või tehinguallahindlused, mis lisatakse kassas müügihetkel.</span><span class="sxs-lookup"><span data-stu-id="46574-108">This includes promotions such as mix and match, quantity and threshold discounts, as well as manual line and transaction discounts that are applied during a sale by a POS user.</span></span>
- <span data-ttu-id="46574-109">**Käsitsi lisatud allahindluste vältimine**: valige see suvand, et vältida käsitsi tootele või kogu tehingule rakendatavaid allahindlusi kassas müügihetkel.</span><span class="sxs-lookup"><span data-stu-id="46574-109">**Prevent manual discounts** – Select this option to only prevent the manual line or transaction discounts that are applied during a sale by a POS user.</span></span> <span data-ttu-id="46574-110">Selle suvandiga märgitud toodetele võib rakendada kampaaniaid (nt toodete kombineerimine, koguse- ja läveallahindlused).</span><span class="sxs-lookup"><span data-stu-id="46574-110">Products with this option selected are still eligible for promotions, such as mix and match and quantity and threshold discounts.</span></span>

> [!NOTE]
> <span data-ttu-id="46574-111">Need sätted ei piira hinna alistamise toimingut, sest see on baashinda määrav toiming, mida ei käsitleta allahindlusena.</span><span class="sxs-lookup"><span data-stu-id="46574-111">These settings do not restrict the price override operation, because that sets the base price and is not treated as a discount.</span></span>

<span data-ttu-id="46574-112">[![Väli väldi allahindluseid](./media/prevent-discounts.png)](./media/prevent-discounts.png)</span><span class="sxs-lookup"><span data-stu-id="46574-112">[![Prevent discounts field](./media/prevent-discounts.png)](./media/prevent-discounts.png)</span></span>