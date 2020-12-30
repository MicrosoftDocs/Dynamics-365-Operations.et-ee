---
title: Kliendikaardid ja preemiapunktid
description: Selles teemas kirjeldatakse topeltkirjutuses kliendikaartide ja preemiapunktide andmete integreerimist.
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
ms.openlocfilehash: 28872e9510394cf3d5cee151798d4130b8b6fe27
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683494"
---
# <a name="customer-loyalty-cards-and-reward-points"></a><span data-ttu-id="ef78e-103">Kliendikaardid ja preemiapunkte</span><span class="sxs-lookup"><span data-stu-id="ef78e-103">Customer loyalty cards and reward points</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ef78e-104">Ettevõtted liigitavad kliente ja pakuvad keerukaid teenuseid klientide ostu- ja kulutamisharjumuste põhjal.</span><span class="sxs-lookup"><span data-stu-id="ef78e-104">Businesses classify customers and provide sophisticated services, based on customer shopping and spending patterns.</span></span> <span data-ttu-id="ef78e-105">Näiteks Dynamics 365 Commerce'il on kliendikaartide, preemiapunktide, püsikliendipõhine hinnakujunduse ja preemiapõhise ostukogemusi hõlbustamiseks ja käsitlemiseks vajalik infrastruktuur ja funktsioonid.</span><span class="sxs-lookup"><span data-stu-id="ef78e-105">For example, Dynamics 365 Commerce has the infrastructure and functions to facilitate and handle customer loyalty cards, reward points, loyalty-based pricing, and rewards-based shopping experiences.</span></span> <span data-ttu-id="ef78e-106">Kui Commerce'i kliendikaartide ja preemiapunktide andmed sünkroonitakse Dataverse'i, saavad klientide kaasamise rakendused neid kasutada.</span><span class="sxs-lookup"><span data-stu-id="ef78e-106">When data about customer loyalty cards and reward points in Commerce is synced to Dataverse, customer engagement apps can use that data.</span></span> <span data-ttu-id="ef78e-107">Näiteks Dynamics 365 Customer Service'i kasutajad saavad kasutada neid andmeid samade keerukate teenuste saamiseks tehnoabi kaudu.</span><span class="sxs-lookup"><span data-stu-id="ef78e-107">For example, Dynamics 365 Customer Service users can use the data to provide the same sophisticated services through the help desk.</span></span>

## <a name="templates"></a><span data-ttu-id="ef78e-108">Mallid</span><span class="sxs-lookup"><span data-stu-id="ef78e-108">Templates</span></span>

| <span data-ttu-id="ef78e-109">Finance and Operations rakendused</span><span class="sxs-lookup"><span data-stu-id="ef78e-109">Finance and Operations apps</span></span> | <span data-ttu-id="ef78e-110">Mudeljuhitud Dynamics 365 rakendused</span><span class="sxs-lookup"><span data-stu-id="ef78e-110">Model-driven apps in Dynamics 365</span></span> | <span data-ttu-id="ef78e-111">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="ef78e-111">Description</span></span> |
|-----------------------------|-----------------------------------|-------------|
| <span data-ttu-id="ef78e-112">Kliendikaart</span><span class="sxs-lookup"><span data-stu-id="ef78e-112">Loyalty card</span></span>                | <span data-ttu-id="ef78e-113">msdyn\_loyaltycards</span><span class="sxs-lookup"><span data-stu-id="ef78e-113">msdyn\_loyaltycards</span></span>               | <span data-ttu-id="ef78e-114">See mall sünkroonib kliendikaartide kohta käivat teavet.</span><span class="sxs-lookup"><span data-stu-id="ef78e-114">This template syncs information about customer loyalty cards.</span></span> |
| <span data-ttu-id="ef78e-115">Püsikliendi preemiapunktid</span><span class="sxs-lookup"><span data-stu-id="ef78e-115">Loyalty reward points</span></span>       | <span data-ttu-id="ef78e-116">msdyn\_loyaltyrewardpoints</span><span class="sxs-lookup"><span data-stu-id="ef78e-116">msdyn\_loyaltyrewardpoints</span></span>        | <span data-ttu-id="ef78e-117">See mall sünkroonib kliendi preemiapunktide kohta käivat teavet.</span><span class="sxs-lookup"><span data-stu-id="ef78e-117">This template syncs information about customer reward points.</span></span> |

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [mapping loyalty card](includes/LoyaltyCard-msdyn-loyaltycards.md)]

[!include [mapping reward points](includes/LoyaltyRewardPoints-msdyn-loyaltyrewardpoints.md)]
