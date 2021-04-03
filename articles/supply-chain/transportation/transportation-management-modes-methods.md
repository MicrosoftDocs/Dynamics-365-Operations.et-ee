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
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2020-10-16
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 0d41d8665252a978962bf6a2e307dce3dad64a5b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5233435"
---
# <a name="transportation-management-modes-and-methods"></a><span data-ttu-id="e74d0-103">Transpordihalduse liigid ja meetodid</span><span class="sxs-lookup"><span data-stu-id="e74d0-103">Transportation management modes and methods</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e74d0-104">Transpordihalduse liik näitab transpordi tüüpi, mida vedaja kasutab veose tarnimiseks, näiteks Vähem kui koormatäis (LTL), Koormatäis (TL) või Pakk.</span><span class="sxs-lookup"><span data-stu-id="e74d0-104">The transportation management  mode represents the type of transport that the carrier uses for freight deliveries, such as less than load (LTL), truckload (TL), or parcel.</span></span> <span data-ttu-id="e74d0-105">Transpordi meetod on transpordivorm, mida vedaja kasutab veose tarnimiseks, näiteks õhk, maa, meri või raudtee.</span><span class="sxs-lookup"><span data-stu-id="e74d0-105">The transportation method represents the form of transport that the carrier uses for freight deliveries, such as air, ground, ocean, or rail.</span></span>

<span data-ttu-id="e74d0-106">Transpordiliike ja transpordimeetodeid kasutatakse mitmes kontekstis.</span><span class="sxs-lookup"><span data-stu-id="e74d0-106">Modes and transportation methods are used in several contexts.</span></span> <span data-ttu-id="e74d0-107">Protsessi plaanides kasutatakse ainult liike, samal ajal kui tarne vedajate ja vedaja teenuste seadistamisel kasutatakse nii transpordiliike kui ka transpordimeetodeid.</span><span class="sxs-lookup"><span data-stu-id="e74d0-107">Only modes are used in route plans, while both modes and transportation methods are used when setting up shipping carriers and carrier services.</span></span> <span data-ttu-id="e74d0-108">Transpordiliikide ja transpordimeetodite vahel pole otsest seost või hierarhiat.</span><span class="sxs-lookup"><span data-stu-id="e74d0-108">No explicit relationship or hierarchy exists between modes and transportation methods.</span></span>

## <a name="create-a-mode"></a><span data-ttu-id="e74d0-109">Liigi loomine</span><span class="sxs-lookup"><span data-stu-id="e74d0-109">Create a mode</span></span>

<span data-ttu-id="e74d0-110">Liigi loomiseks läbige järgmised sammud:</span><span class="sxs-lookup"><span data-stu-id="e74d0-110">To create a mode, follow these steps:</span></span>

1. <span data-ttu-id="e74d0-111">Tehke valik **Transpordi haldus \> Seadistus \> Vedajad \> Kättetoimetajad**.</span><span class="sxs-lookup"><span data-stu-id="e74d0-111">Go to **Transportation management \> Setup \> Carriers \> Mode**.</span></span>
1. <span data-ttu-id="e74d0-112">Valige uue liigi loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e74d0-112">Select **New** to create a new mode.</span></span>
1. <span data-ttu-id="e74d0-113">Sisestage liigile ainulaadne ID ja kirjeldav nimi.</span><span class="sxs-lookup"><span data-stu-id="e74d0-113">Enter a unique ID and a descriptive name for the mode.</span></span>
1. <span data-ttu-id="e74d0-114">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e74d0-114">Close the page.</span></span>

## <a name="create-a-transportation-method"></a><span data-ttu-id="e74d0-115">Transpordimeetodi loomine</span><span class="sxs-lookup"><span data-stu-id="e74d0-115">Create a transportation method</span></span>

<span data-ttu-id="e74d0-116">Uue transpordimeetodi loomiseks toimige järgmiselt:</span><span class="sxs-lookup"><span data-stu-id="e74d0-116">To create a transportation method, follow these steps:</span></span>

1. <span data-ttu-id="e74d0-117">Avage **Transpordihaldus \> Seadistus \> Vedajad \> Transpordimeetodid**.</span><span class="sxs-lookup"><span data-stu-id="e74d0-117">Go to **Transportation management \> Setup \> Carriers \> Transportation methods**.</span></span>
1. <span data-ttu-id="e74d0-118">Uue transpordimeetodi loomiseks klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="e74d0-118">Select **New** to create a new transportation method.</span></span>
1. <span data-ttu-id="e74d0-119">Sisestage transpordimeetodile ainulaadne ID ja kirjeldav nimi.</span><span class="sxs-lookup"><span data-stu-id="e74d0-119">Enter a unique ID and descriptive name for the transportation method.</span></span>
1. <span data-ttu-id="e74d0-120">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e74d0-120">Close the page.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]