---
title: Transpordihalduse liigid ja meetodid
description: See teema näitab, kuidas seadistada transpordihalduse liike ja meetodeid.
author: Henrikan
manager: tfehr
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: ceb3930cdb7764f846e88edfff6906b902a7f5fa
ms.sourcegitcommit: fe7ac653efcb1ac6318083f482394b96ed82b4c7
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/29/2020
ms.locfileid: "4426723"
---
# <a name="transportation-management-modes-and-methods"></a><span data-ttu-id="e13e8-103">Transpordihalduse liigid ja meetodid</span><span class="sxs-lookup"><span data-stu-id="e13e8-103">Transportation management modes and methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e13e8-104">Transpordihalduse liik näitab transpordi tüüpi, mida vedaja kasutab veose tarnimiseks, näiteks Vähem kui koormatäis (LTL), Koormatäis (TL) või Pakk.</span><span class="sxs-lookup"><span data-stu-id="e13e8-104">The transportation management  mode represents the type of transport that the carrier uses for freight deliveries, such as less than load (LTL), truckload (TL), or parcel.</span></span> <span data-ttu-id="e13e8-105">Transpordi meetod on transpordivorm, mida vedaja kasutab veose tarnimiseks, näiteks õhk, maa, meri või raudtee.</span><span class="sxs-lookup"><span data-stu-id="e13e8-105">The transportation method represents the form of transport that the carrier uses for freight deliveries, such as air, ground, ocean, or rail.</span></span>

<span data-ttu-id="e13e8-106">Transpordiliike ja transpordimeetodeid kasutatakse mitmes kontekstis.</span><span class="sxs-lookup"><span data-stu-id="e13e8-106">Modes and transportation methods are used in several contexts.</span></span> <span data-ttu-id="e13e8-107">Protsessi plaanides kasutatakse ainult liike, samal ajal kui tarne vedajate ja vedaja teenuste seadistamisel kasutatakse nii transpordiliike kui ka transpordimeetodeid.</span><span class="sxs-lookup"><span data-stu-id="e13e8-107">Only modes are used in route plans, while both modes and transportation methods are used when setting up shipping carriers and carrier services.</span></span> <span data-ttu-id="e13e8-108">Transpordiliikide ja transpordimeetodite vahel pole otsest seost või hierarhiat.</span><span class="sxs-lookup"><span data-stu-id="e13e8-108">No explicit relationship or hierarchy exists between modes and transportation methods.</span></span>

## <a name="create-a-mode"></a><span data-ttu-id="e13e8-109">Liigi loomine</span><span class="sxs-lookup"><span data-stu-id="e13e8-109">Create a mode</span></span>

<span data-ttu-id="e13e8-110">Liigi loomiseks läbige järgmised sammud:</span><span class="sxs-lookup"><span data-stu-id="e13e8-110">To create a mode, follow these steps:</span></span>

1. <span data-ttu-id="e13e8-111">Tehke valik **Transpordi haldus \> Seadistus \> Vedajad \> Kättetoimetajad**.</span><span class="sxs-lookup"><span data-stu-id="e13e8-111">Go to **Transportation management \> Setup \> Carriers \> Mode**.</span></span>
1. <span data-ttu-id="e13e8-112">Valige uue liigi loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e13e8-112">Select **New** to create a new mode.</span></span>
1. <span data-ttu-id="e13e8-113">Sisestage liigile ainulaadne ID ja kirjeldav nimi.</span><span class="sxs-lookup"><span data-stu-id="e13e8-113">Enter a unique ID and a descriptive name for the mode.</span></span>
1. <span data-ttu-id="e13e8-114">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e13e8-114">Close the page.</span></span>

## <a name="create-a-transportation-method"></a><span data-ttu-id="e13e8-115">Transpordimeetodi loomine</span><span class="sxs-lookup"><span data-stu-id="e13e8-115">Create a transportation method</span></span>

<span data-ttu-id="e13e8-116">Uue transpordimeetodi loomiseks toimige järgmiselt:</span><span class="sxs-lookup"><span data-stu-id="e13e8-116">To create a transportation method, follow these steps:</span></span>

1. <span data-ttu-id="e13e8-117">Avage **Transpordihaldus \> Seadistus \> Vedajad \> Transpordimeetodid**.</span><span class="sxs-lookup"><span data-stu-id="e13e8-117">Go to **Transportation management \> Setup \> Carriers \> Transportation methods**.</span></span>
1. <span data-ttu-id="e13e8-118">Uue transpordimeetodi loomiseks klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e13e8-118">Select **New** to create a new transportation method.</span></span>
1. <span data-ttu-id="e13e8-119">Sisestage transpordimeetodile ainulaadne ID ja kirjeldav nimi.</span><span class="sxs-lookup"><span data-stu-id="e13e8-119">Enter a unique ID and descriptive name for the transportation method.</span></span>
1. <span data-ttu-id="e13e8-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e13e8-120">Close the page.</span></span>
