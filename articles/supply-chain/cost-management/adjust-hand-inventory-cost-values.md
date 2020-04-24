---
title: Vaba kaubavaru kuluväärtuste korrigeerimine
description: Lehel Vaba kaubavaru korrigeerimine saab korrigeerida vaba kaubavaru omahinda pärast lao sulgemisprotsessi käitamist.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAdjInventOnHand
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 53231
ms.assetid: bc1fde9f-5ad9-4339-8ae8-e2839b792eb2
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1fc97db0f0b637e27ece904fe24e91a92044bc17
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208796"
---
# <a name="adjust-on-hand-inventory-cost-values"></a><span data-ttu-id="dc55f-103">Vaba kaubavaru kuluväärtuste korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="dc55f-103">Adjust on-hand inventory cost values</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc55f-104">Lehel Vaba kaubavaru korrigeerimine saab korrigeerida vaba kaubavaru omahinda pärast lao sulgemisprotsessi käitamist.</span><span class="sxs-lookup"><span data-stu-id="dc55f-104">Use the Adjustment of on-hand inventory page to adjust the cost value of the on-hand inventory quantities after an inventory close process is run.</span></span>

<span data-ttu-id="dc55f-105">Lehel **Vaba kaubavaru korrigeerimine** saab korrigeerida vaba kaubavaru omahinda pärast lao sulgemisprotsessi käitamist.</span><span class="sxs-lookup"><span data-stu-id="dc55f-105">You can use the **Adjustment of on-hand inventory** page to adjust the cost value of on-hand inventory quantities after an inventory close process is run.</span></span> <span data-ttu-id="dc55f-106">**Märkus.** Lehe **Vaba kaubavaru korrigeerimine** avamiseks valige lehel **Sulgemine ja korrigeerimine** lõpetatud lao sulgemisprotsessi kirje ja klõpsake siis valikuid **Korrigeerimine** &gt; **Laoseis**.</span><span class="sxs-lookup"><span data-stu-id="dc55f-106">**Note:** To open the **Adjustment of on-hand inventory** page, on the **Closing and adjustment** page, select the record of a completed inventory close process, and then click **Adjustment** &gt; **On-hand**.</span></span> <span data-ttu-id="dc55f-107">**Näide.** Veebruaris on teil järgmised kanded.</span><span class="sxs-lookup"><span data-stu-id="dc55f-107">**Example:** You have the following transactions in February:</span></span>

-   <span data-ttu-id="dc55f-108">1. veebruar: kaubavaru finantssissetulek, kogus 2, hind 10.00 USD</span><span class="sxs-lookup"><span data-stu-id="dc55f-108">February 1: An inventory financial receipt for a quantity of 2 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="dc55f-109">5. veebruar: kaubavaru finantssissetulek, kogus 1, hind 13.00 USD</span><span class="sxs-lookup"><span data-stu-id="dc55f-109">February 5: An inventory financial receipt for a quantity of 1 at a cost of USD 13.00</span></span>
-   <span data-ttu-id="dc55f-110">19. veebruar: kaubavaru finantssissetulek, kogus 1, keskmine hind 11.00 USD</span><span class="sxs-lookup"><span data-stu-id="dc55f-110">February 19: An inventory financial issue for a quantity of 1 at a running average cost of USD 11.00</span></span>

<span data-ttu-id="dc55f-111">See kaup seadistati FIFO-laomudeliga (esimesena sisse, esimesena välja) ning lao sulgemine toimus 28. veebruaril.</span><span class="sxs-lookup"><span data-stu-id="dc55f-111">This item was set up with the first in, first out (FIFO) inventory model, and inventory close was performed as of February 28.</span></span> <span data-ttu-id="dc55f-112">Finantsväliskanne summas 11,00 USD tasakaalustatakse finantssissetuleku suhtes 1. veebruaril ja tehakse parandus 1,00 USD ulatuses.</span><span class="sxs-lookup"><span data-stu-id="dc55f-112">The financial issue transaction of USD 11.00 will be settled against the financial receipt that is dated February 1, and an adjustment of USD 1.00 will be made.</span></span> <span data-ttu-id="dc55f-113">Järgmistes lao sissetulekutes sisaldub avatud lao koguseid:</span><span class="sxs-lookup"><span data-stu-id="dc55f-113">The following inventory receipts will then contain open inventory quantities:</span></span>

-   <span data-ttu-id="dc55f-114">1. veebruar: kogus 1, hind 10.00 USD</span><span class="sxs-lookup"><span data-stu-id="dc55f-114">February 1: A quantity of 1 at a cost of USD 10.00</span></span>
-   <span data-ttu-id="dc55f-115">5. veebruar: kogus 1, hind 13.00 USD</span><span class="sxs-lookup"><span data-stu-id="dc55f-115">February 5: A quantity of 1 at a cost of USD 13.00</span></span>

<span data-ttu-id="dc55f-116">Et seadistada nende kahe kauba kulu 15,00 USD-le, kasutage vaba kaubavaru korrigeerimise valikut, et korrigeerida vabu kaubakoguseid alates viimasest lao sulgemise perioodist.</span><span class="sxs-lookup"><span data-stu-id="dc55f-116">To set the cost of these two items to USD 15.00, use the on-hand adjustment option to adjust the open on-hand quantities as of the last inventory close period.</span></span> <span data-ttu-id="dc55f-117">**Märkus.** Vaba kaubavaru korrigeerimise kande kuupäeva sisestus on ka viimase lao sulgemise kuupäev.</span><span class="sxs-lookup"><span data-stu-id="dc55f-117">**Note:** The posting date of the on-hand adjustment transaction will be the date of the last inventory close.</span></span> <span data-ttu-id="dc55f-118">Seda kuupäeva ei saa muuta.</span><span class="sxs-lookup"><span data-stu-id="dc55f-118">This date can't be modified.</span></span>
