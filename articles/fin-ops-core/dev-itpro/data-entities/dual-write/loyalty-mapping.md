---
title: Kliendikaardid ja preemiapunktid
description: Selles teemas kirjeldatakse kliendikaartide ja preemiapunktide andmete integreerimist Finance and Operationsi rakenduste ja Common Data Service'i vahel.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-10
ms.openlocfilehash: 24ce08bb6cba9c74075151bafe0b07509fbdf73d
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "3998010"
---
# <a name="customer-loyalty-cards-and-reward-points"></a><span data-ttu-id="16b0f-103">Kliendikaardid ja preemiapunktid</span><span class="sxs-lookup"><span data-stu-id="16b0f-103">Customer loyalty cards and reward points</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="16b0f-104">Ettevõtted liigitavad kliente ja pakuvad keerukaid teenuseid klientide ostu- ja kulutamisharjumuste põhjal.</span><span class="sxs-lookup"><span data-stu-id="16b0f-104">Businesses classify customers and provide sophisticated services, based on customer shopping and spending patterns.</span></span> <span data-ttu-id="16b0f-105">Microsoft Dynamics 365 rakenduste komplektis on Dynamics 365 Commerce'il kliendikaartide, preemiapunktide, püsikliendipõhine hinnakujunduse ja preemiapõhise ostukogemusi hõlbustamiseks ja käsitlemiseks vajalik infrastruktuur ja funktsioonid.</span><span class="sxs-lookup"><span data-stu-id="16b0f-105">In the Microsoft Dynamics 365 suite of applications, Dynamics 365 Commerce has the infrastructure and functions to facilitate and handle customer loyalty cards, reward points, loyalty-based pricing, and rewards-based shopping experiences.</span></span> <span data-ttu-id="16b0f-106">Kui Commerce'i kliendikaartide ja preemiapunktide andmed sünkroonitakse Common Data Service'isse, saavad Dynamics 365 mudeljuhitud rakendused neid kasutada.</span><span class="sxs-lookup"><span data-stu-id="16b0f-106">When data about customer loyalty cards and reward points in Commerce is synced to Common Data service, model-driven apps in Dynamics 365 can use that data.</span></span> <span data-ttu-id="16b0f-107">Näiteks Dynamics 365 Customer Service'i kasutajad saavad kasutada neid andmeid samade keerukate teenuste saamiseks tehnoabi kaudu.</span><span class="sxs-lookup"><span data-stu-id="16b0f-107">For example, Dynamics 365 Customer Service users can use the data to provide the same sophisticated services through the help desk.</span></span>

## <a name="templates"></a><span data-ttu-id="16b0f-108">Mallid</span><span class="sxs-lookup"><span data-stu-id="16b0f-108">Templates</span></span>

| <span data-ttu-id="16b0f-109">Finance and Operations rakendused</span><span class="sxs-lookup"><span data-stu-id="16b0f-109">Finance and Operations apps</span></span> | <span data-ttu-id="16b0f-110">Mudeljuhitud Dynamics 365 rakendused</span><span class="sxs-lookup"><span data-stu-id="16b0f-110">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="16b0f-111">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="16b0f-111">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="16b0f-112">Kliendikaart</span><span class="sxs-lookup"><span data-stu-id="16b0f-112">Loyalty card</span></span>                | <span data-ttu-id="16b0f-113">msdyn\_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="16b0f-113">msdyn\_loyaltycards</span></span>               | <span data-ttu-id="16b0f-114">See mall sünkroonib kliendikaartide kohta käivat teavet.</span><span class="sxs-lookup"><span data-stu-id="16b0f-114">This template syncs information about customer loyalty cards.</span></span> |
| <span data-ttu-id="16b0f-115">Püsikliendi preemiapunktid</span><span class="sxs-lookup"><span data-stu-id="16b0f-115">Loyalty reward points</span></span>       | <span data-ttu-id="16b0f-116">msdyn\_loyaltyrewardpoints</span><span class="sxs-lookup"><span data-stu-id="16b0f-116">msdyn\_loyaltyrewardpoints</span></span>        | <span data-ttu-id="16b0f-117">See mall sünkroonib kliendi preemiapunktide kohta käivat teavet.</span><span class="sxs-lookup"><span data-stu-id="16b0f-117">This template syncs information about customer reward points.</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]
