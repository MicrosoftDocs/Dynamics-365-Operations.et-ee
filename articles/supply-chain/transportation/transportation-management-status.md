---
title: Transpordihalduse olekud
description: See teema selgitab, kuidas luua transpordi olekut ja vastendada seda olekut vedaja olekuga.
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
ms.search.validFrom: 2020-09-08
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 9d3ed4b73f909b50e97c971a37c548c8c4a9e620
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5006462"
---
# <a name="transportation-management-statuses"></a><span data-ttu-id="5fe7d-103">Transpordihalduse olekud</span><span class="sxs-lookup"><span data-stu-id="5fe7d-103">Transportation management statuses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5fe7d-104">Seadistage transpordi olekute põhikoodid, et tõlgendada kättetoimetajate poolt tarnitud koode.</span><span class="sxs-lookup"><span data-stu-id="5fe7d-104">Set up master codes for transportation statuses to interpret codes that are provided by your shipping carriers.</span></span> <span data-ttu-id="5fe7d-105">See võimaldab teil oleku pakkumiseks ühendada saadetise vedajatega.</span><span class="sxs-lookup"><span data-stu-id="5fe7d-105">This lets you integrate with shipping carriers to provide a status.</span></span> <span data-ttu-id="5fe7d-106">Transpordi oleku põhikoodi jaoks esitatud transpordi olek võib aidata jälgida koorma, saadetise või konteineri olekut.</span><span class="sxs-lookup"><span data-stu-id="5fe7d-106">The transportation status that you provide for a transportation master status code can help you track the status of a load, shipment, or container.</span></span> <span data-ttu-id="5fe7d-107">Koorma, saadetise või konteineri kindlat transpordi olekut saab uuendada ainult läbi andmevahetuse ja mitte käsitsi kasutajaliidese kaudu.</span><span class="sxs-lookup"><span data-stu-id="5fe7d-107">The specific transportation status for a load, shipment, or container can only be updated through data integration and not manually through the user interface.</span></span>

## <a name="create-a-transportation-status"></a><span data-ttu-id="5fe7d-108">Transpordi oleku loomine</span><span class="sxs-lookup"><span data-stu-id="5fe7d-108">Create a transportation status</span></span>

<span data-ttu-id="5fe7d-109">Uue transpordi oleku loomiseks toimige järgmiselt:</span><span class="sxs-lookup"><span data-stu-id="5fe7d-109">To create a transportation status, follow these steps:</span></span>

1. <span data-ttu-id="5fe7d-110">Avage **Transpordihaldus \> Seadistus \> Transpordioleku koondüksused**.</span><span class="sxs-lookup"><span data-stu-id="5fe7d-110">Go to **Transportation management \> Setup \> Transportation status masters**.</span></span>
1. <span data-ttu-id="5fe7d-111">Transpordi oleku koondüksuse loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="5fe7d-111">Select **New** to create a transportation status master.</span></span>
1. <span data-ttu-id="5fe7d-112">Väljal **Transpordi oleku koondüksus** sisestage transpordi oleku kordumatu kood.</span><span class="sxs-lookup"><span data-stu-id="5fe7d-112">In the **Transportation status master** field, enter a unique code for the transportation status.</span></span>
1. <span data-ttu-id="5fe7d-113">Väljal **Transpordi tüüp** valige transpordi tüübiks *Saadetise vedaja* või *Keksus*.</span><span class="sxs-lookup"><span data-stu-id="5fe7d-113">In the **Transportation type** field, select either *Shipping carrier* or *Hub* as the type of transportation.</span></span>
1. <span data-ttu-id="5fe7d-114">Sisestage nimi ja transpordi olek.</span><span class="sxs-lookup"><span data-stu-id="5fe7d-114">Enter a name and transportation status.</span></span>
1. <span data-ttu-id="5fe7d-115">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5fe7d-115">Close the page.</span></span>

## <a name="map-a-transportation-status-to-a-carrier-status"></a><span data-ttu-id="5fe7d-116">Transpordi oleku vastendamine vedaja olekuga</span><span class="sxs-lookup"><span data-stu-id="5fe7d-116">Map a transportation status to a carrier status</span></span>

<span data-ttu-id="5fe7d-117">Transpordi oleku vastendamiseks vedaja olekuga järgige järgmisi samme:</span><span class="sxs-lookup"><span data-stu-id="5fe7d-117">To map a transportation status to a carrier status, follow these steps:</span></span>

1. <span data-ttu-id="5fe7d-118">Avage **Transpordihaldus \> Seadistus \> Vedajad \> Vedaja transpordi olek**.</span><span class="sxs-lookup"><span data-stu-id="5fe7d-118">Go to **Transportation management \> Setup \> Carriers \> Carrier transportation status**.</span></span>
1. <span data-ttu-id="5fe7d-119">Kättetoimetaja koodi vastendamiseks transpordi oleku põhikoodiga valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="5fe7d-119">Select **New** to map a code from a shipping carrier to a transportation status master code.</span></span>
1. <span data-ttu-id="5fe7d-120">Valige vedaja ja veoteenuse kordumatu ID.</span><span class="sxs-lookup"><span data-stu-id="5fe7d-120">Select the unique ID for the shipping carrier and the carrier service.</span></span>
1. <span data-ttu-id="5fe7d-121">Valige transpordi oleku kood, mida soovite vastendada valitud vedaja koodiga.</span><span class="sxs-lookup"><span data-stu-id="5fe7d-121">Select the transportation status code that you want to map to the selected shipping carrier's code.</span></span>
1. <span data-ttu-id="5fe7d-122">Sisestage kättetoimetaja kasutatav väliskood.</span><span class="sxs-lookup"><span data-stu-id="5fe7d-122">Enter the external code that is used by the shipping carrier.</span></span>
1. <span data-ttu-id="5fe7d-123">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="5fe7d-123">Close the page.</span></span>
