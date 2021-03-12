---
title: Transpordihalduse numbriseeria
description: See teema kirjeldab, kuidas seadistada transpordi halduse numbriseeriaid.
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
ms.openlocfilehash: b7bb6c9338808828a41801a85a1b93b420e9c75b
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5004730"
---
# <a name="transportation-management-number-sequence"></a><span data-ttu-id="32b7f-103">Transpordihalduse numbriseeria</span><span class="sxs-lookup"><span data-stu-id="32b7f-103">Transportation management number sequence</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="32b7f-104">Kasutage Pro-numbrite seadistamiseks transpordi halduse moodulis lehekülge **Numbriseeriad**.</span><span class="sxs-lookup"><span data-stu-id="32b7f-104">Use the **Number sequences** page in the transportation management module to set up various pro numbers.</span></span> <span data-ttu-id="32b7f-105">Vedajad kasutavad Pro-numbreid iga saadetise edenemise korraldamiseks ja jälgimiseks.</span><span class="sxs-lookup"><span data-stu-id="32b7f-105">Pro numbers are used by carriers to organize and track the progress of each shipment.</span></span>

## <a name="create-a-number-sequence-for-a-pro-number"></a><span data-ttu-id="32b7f-106">Looge Pro-numbri jaoks numbriseeria.</span><span class="sxs-lookup"><span data-stu-id="32b7f-106">Create a number sequence for a pro number</span></span>

<span data-ttu-id="32b7f-107">Numbriseeria loomiseks Pro-numbri jaoks tehke järgmist:</span><span class="sxs-lookup"><span data-stu-id="32b7f-107">To create a number sequence for a pro number, do the following:</span></span>

1. <span data-ttu-id="32b7f-108">Avage jaotis **Transpordihaldus \> Seadistus \> Vedajad \> Numbriseeriad**.</span><span class="sxs-lookup"><span data-stu-id="32b7f-108">Go to **Transportation management \> Setup \> Carriers \> Number sequences**.</span></span>
1. <span data-ttu-id="32b7f-109">Valige uue numbriseeria loomiseks **Uus**.</span><span class="sxs-lookup"><span data-stu-id="32b7f-109">Select **New** to create a new number sequence.</span></span>
1. <span data-ttu-id="32b7f-110">Sisestage numbriseeria ainulaadne ID ja kirjeldav nimi.</span><span class="sxs-lookup"><span data-stu-id="32b7f-110">Enter a unique ID and descriptive name for the number sequence.</span></span>
1. <span data-ttu-id="32b7f-111">Väljal **Numbriseeria tüüp** on ainsaks valikuks *Pro-number*.</span><span class="sxs-lookup"><span data-stu-id="32b7f-111">In the **Number sequence type** field, *Pro number* is the only option.</span></span>
1. <span data-ttu-id="32b7f-112">**Kontrolli number** väljal on *Kontrolli number* ainus valik ja see seadistatakse üldise mootorina.</span><span class="sxs-lookup"><span data-stu-id="32b7f-112">In the **Check digit** field, *Check digit* is the only option and is set up as a generic engine.</span></span>
1. <span data-ttu-id="32b7f-113">Sisestage **Seeria** FastTab-is seeria teave.</span><span class="sxs-lookup"><span data-stu-id="32b7f-113">On the **Sequence** FastTab, provide information about the sequence.</span></span>
1. <span data-ttu-id="32b7f-114">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="32b7f-114">Close the page.</span></span>

## <a name="link-a-number-sequence-to-a-shipping-carrier"></a><span data-ttu-id="32b7f-115">Numbriseeria linkimine saadetise vedajaga</span><span class="sxs-lookup"><span data-stu-id="32b7f-115">Link a number sequence to a shipping carrier</span></span>

<span data-ttu-id="32b7f-116">Numbriseeria linkimiseks vedajaga tehke järgmist:</span><span class="sxs-lookup"><span data-stu-id="32b7f-116">To link a number sequence to a carrier, do the following:</span></span>

1. <span data-ttu-id="32b7f-117">Avage jaotis **Transpordihaldus \> Seadistus \> Vedajad \> Kättetoimetajad**.</span><span class="sxs-lookup"><span data-stu-id="32b7f-117">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="32b7f-118">Valige vedaja.</span><span class="sxs-lookup"><span data-stu-id="32b7f-118">Select a shipping carrier.</span></span>
1. <span data-ttu-id="32b7f-119">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="32b7f-119">Select **Edit**.</span></span>
1. <span data-ttu-id="32b7f-120">**Ülevaade** FastTab-is tehke valik **Pro-numbriseeria** väljal.</span><span class="sxs-lookup"><span data-stu-id="32b7f-120">On the **Overview** FastTab, select an option in the **Pro number sequence** field.</span></span>
1. <span data-ttu-id="32b7f-121">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="32b7f-121">Close the page.</span></span>
