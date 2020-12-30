---
title: Toote kinnitamine kogumi komplekteerimise jaoks
description: Selles teemas kirjeldatakse kauba kontrollimise seadistamist koos kogumi komplekteerimisega.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 272c3a13b68e2b862faf20cc269ca790322b61de
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4426297"
---
# <a name="product-confirmation-for-cluster-picking"></a><span data-ttu-id="27012-103">Toote kinnitamine kogumi komplekteerimise jaoks</span><span class="sxs-lookup"><span data-stu-id="27012-103">Product confirmation for cluster picking</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="27012-104">Kogumi komplekteerimisel saate komplekteerida kaupu korraga mitme tellimuse jaoks.</span><span class="sxs-lookup"><span data-stu-id="27012-104">Cluster picking allows you to pick items for several orders at the same time.</span></span> <span data-ttu-id="27012-105">Kogumi komplekteerimise rakendamiseks on kinnitamine väga oluline, et kontrollida kogumitesse lisatud kaupu.</span><span class="sxs-lookup"><span data-stu-id="27012-105">When cluster picking is applied, item confirmation is crucial to verify the items that are added to clusters.</span></span> <span data-ttu-id="27012-106">Kogumi komplekteerimisprotsessi ajal saab kaupu kogumi komplekteerimisel kontrollida.</span><span class="sxs-lookup"><span data-stu-id="27012-106">You can verify items in cluster picking during the cluster picking process.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="27012-107">Kus see kehtib</span><span class="sxs-lookup"><span data-stu-id="27012-107">Where it applies</span></span>

<span data-ttu-id="27012-108">Kauba kontrollimine kogumi komplekteerimiseks toimib samamoodi, nagu kaupade kontrollimine mitte-kogumi komplekteerimisprotsesside korral.</span><span class="sxs-lookup"><span data-stu-id="27012-108">Item verification for cluster picking works the same way as when you verify items in a non-cluster picking processes.</span></span> <span data-ttu-id="27012-109">Seadistus põhineb toote vöötkoodi seadistusel.</span><span class="sxs-lookup"><span data-stu-id="27012-109">The setup is based on the product bar code setup.</span></span>

## <a name="set-up-item-verification-with-cluster-picking"></a><span data-ttu-id="27012-110">Kauba kontrollimise seadistamine kogumi komplekteerimisega</span><span class="sxs-lookup"><span data-stu-id="27012-110">Set up item verification with cluster picking</span></span>

1. <span data-ttu-id="27012-111">Avage mobiilse seadme menüüelemendis seadistusvorm töö kinnitamiseks: **Laohaldus** > **Laohaldus** > **Seadistus** > **Mobiilne seade** > **Mobiilse seadme menüüelemendid**.</span><span class="sxs-lookup"><span data-stu-id="27012-111">On a mobile device menu item, open the setup form for work confirmation: **Warehouse management** > **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**.</span></span>
1. <span data-ttu-id="27012-112">Avage mobiilse seadme menüüelemendist jaotis **Töö kinnituse häälestus**.</span><span class="sxs-lookup"><span data-stu-id="27012-112">From the mobile device menu item, open **Work confirmation setup**.</span></span>

|        <span data-ttu-id="27012-113">Suvand</span><span class="sxs-lookup"><span data-stu-id="27012-113">Option</span></span>        |                                    <span data-ttu-id="27012-114">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="27012-114">Description</span></span>                                    |
|----------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="27012-115">Toote kinnitus</span><span class="sxs-lookup"><span data-stu-id="27012-115">Product confirmation</span></span> | <span data-ttu-id="27012-116">Võimaldab iga varude üksust mobiilsel seadmel skannides kontrollida.</span><span class="sxs-lookup"><span data-stu-id="27012-116">Allows you to verify each piece of inventory from the mobile device when scanned.</span></span> |
