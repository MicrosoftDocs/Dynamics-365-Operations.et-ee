---
title: Osa komplekteerimise kinnitus
description: Selles teemas kirjeldatakse, kuidas seadistada ja rakendada osa komplekteerimise kinnitust mobiilselt seadmelt.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm, WHSRFMenuItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b85414dd1385dc3d8c97632eaaeb252759590ff
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "349626"
---
# <a name="piece-picking-confirmation"></a><span data-ttu-id="42f93-103">Osa komplekteerimise kinnitus</span><span class="sxs-lookup"><span data-stu-id="42f93-103">Piece picking confirmation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="42f93-104">Osade komplekteerimine võimaldab kinnitada iga varude osa mobiilsel seadmel komplekteerimis- või inventuuritöö kaudu.</span><span class="sxs-lookup"><span data-stu-id="42f93-104">Piece picking allows you to confirm each piece of inventory through picking or counting work on a mobile device.</span></span> <span data-ttu-id="42f93-105">Komplekteerimiste puhul saate kinnitada töödeldava töö koguse kuni komplekteeritaval tööl määratud koguseni.</span><span class="sxs-lookup"><span data-stu-id="42f93-105">For picks, you can confirm the quantity of work to be processed up to the quantity that is specified on work to be picked.</span></span> <span data-ttu-id="42f93-106">Inventuuritöö puhul võite skannida loendatavad varud ja jälgida kogusummat.</span><span class="sxs-lookup"><span data-stu-id="42f93-106">For counting work, you can scan the inventory that you are counting and track the total amount.</span></span>

<span data-ttu-id="42f93-107">Kui lubate osade komplekteerimise, valitakse automaatselt toote kinnitamine.</span><span class="sxs-lookup"><span data-stu-id="42f93-107">When you enable piece picking, product confirmation is automatically selected.</span></span> <span data-ttu-id="42f93-108">Töö tüübi komplekteerimiste puhul on lubatud maksimaalne arv osi.</span><span class="sxs-lookup"><span data-stu-id="42f93-108">For work-type picks, a maximum number of pieces is enabled.</span></span> <span data-ttu-id="42f93-109">See võimaldab määrata maksimaalse ühikute arvu, mis tuleb tööprotsessi käigus kinnitada.</span><span class="sxs-lookup"><span data-stu-id="42f93-109">This allows you to set a maximum to the number of pieces that must be confirmed during the work process.</span></span> <span data-ttu-id="42f93-110">Maksimaalne kogus põhineb praegu töödeldaval töö ühikul.</span><span class="sxs-lookup"><span data-stu-id="42f93-110">The maximum quantity is based on the current work unit that is being processed.</span></span> <span data-ttu-id="42f93-111">Inventuuri töötüüp ei luba maksimumi.</span><span class="sxs-lookup"><span data-stu-id="42f93-111">The counting work type does not allow a maximum.</span></span>

<span data-ttu-id="42f93-112">Võite kasutada ka skannitud vöötkoodiga seostatud kogust ja mõõtühikut.</span><span class="sxs-lookup"><span data-stu-id="42f93-112">You can also use the quantity and unit of measure (UOM) that is associated with a scanned bar code.</span></span> <span data-ttu-id="42f93-113">See toimib sissetulevate voogude vastuvõtmisel, sh kombineeritud litsentsiplaadiga vastuvõtmine, ostutellimuse kaup, üleviimistellimuse kaup ja koormakaup.</span><span class="sxs-lookup"><span data-stu-id="42f93-113">This will work for receiving on inbound flows including mixed license plate receiving, purchase order item, transfer order item, and load item.</span></span> <span data-ttu-id="42f93-114">See toimib ka osa komplekteerimisel, kui vöötkoodi skannimine lisab koguse kinnitatud ühikute koguarvule, teisendades vöötkoodil olevat mõõtühikut ja tööühikut.</span><span class="sxs-lookup"><span data-stu-id="42f93-114">It also works for piece picking where scanning the bar code will add the quantity to the total number of confirmed pieces converting between the UOM on the bar code and the work unit.</span></span> <span data-ttu-id="42f93-115">Kui vöötkoodil oleva mõõtühiku loendamisel saab kinnitust, et kogus on lubatud seeriagrupis loendamiseks, lisatakse kogus koguarvule.</span><span class="sxs-lookup"><span data-stu-id="42f93-115">If, when counting the UOM on the bar code, it is confirmed that the quantity is allowed for counting on the sequence group, the quantity will be added to the total count.</span></span>

## <a name="where-it-applies"></a><span data-ttu-id="42f93-116">Kus see kehtib</span><span class="sxs-lookup"><span data-stu-id="42f93-116">Where it applies</span></span>

<span data-ttu-id="42f93-117">Osa komplekteerimine toimib kogu inventuuritöö ja mis tahes tüüpi töö algse komplekteerimise puhul.</span><span class="sxs-lookup"><span data-stu-id="42f93-117">Piece picking works for all counting work and for the initial pick for any type of work.</span></span> <span data-ttu-id="42f93-118">Osa komplekteerimine ei rakendu, kui kaupa juhitakse seerianumbritega või kui tegemist on tootmise või kanbani komplekteerimisega litsentsiplaadi (LP) asukohast ja kaup on määratud kogumiseks.</span><span class="sxs-lookup"><span data-stu-id="42f93-118">Piece picking does not apply if the item is controlled by serial numbers or if it is a production or kanban pick from a license plate (LP) location and the item is set to staging.</span></span>

## <a name="set-up-piece-picking"></a><span data-ttu-id="42f93-119">Osa komplekteerimise seadistamine</span><span class="sxs-lookup"><span data-stu-id="42f93-119">Set up piece picking</span></span>

1.  <span data-ttu-id="42f93-120">Avage mobiilse seadme menüüelemendis seadistusvorm töö kinnitamiseks: Laohaldus > **Laohaldus** > **Seadistus** > **Mobiilne seade** > **Mobiilse seadme menüüelemendid**.</span><span class="sxs-lookup"><span data-stu-id="42f93-120">On a mobile device menu item, open the setup form for work confirmation: Warehouse management > **Warehouse management** > **Setup** > **Mobile device** > **Mobile device menu items**.</span></span> 
2. <span data-ttu-id="42f93-121">Avage mobiilse seadme menüüelemendist jaotis Töö kinnituse häälestus.</span><span class="sxs-lookup"><span data-stu-id="42f93-121">From the mobile device menu item, open Work confirmation setup.</span></span>

<span data-ttu-id="42f93-122">Kui töö tüüp on komplekteerimine või inventuur, saab teha järgmisi valikuid.</span><span class="sxs-lookup"><span data-stu-id="42f93-122">The following options become available for selection when the work type is pick or counting.</span></span>


|           <span data-ttu-id="42f93-123">Suvand</span><span class="sxs-lookup"><span data-stu-id="42f93-123">Option</span></span>           |                                                                            <span data-ttu-id="42f93-124">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="42f93-124">Description</span></span>                                                                            |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="42f93-125">Osa komplekteerimise kinnitus</span><span class="sxs-lookup"><span data-stu-id="42f93-125">Piece picking confirmation</span></span> | <span data-ttu-id="42f93-126">Saadaval komplekteerimise ja inventuuri töötüüpide jaoks.</span><span class="sxs-lookup"><span data-stu-id="42f93-126">Available for pick and counting work types.</span></span> <span data-ttu-id="42f93-127">Toote kinnitamine valitakse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="42f93-127">Product confirmation is automatically selected.</span></span> <span data-ttu-id="42f93-128">Võimaldab iga varude üksust mobiilsel seadmel skannides kinnitada.</span><span class="sxs-lookup"><span data-stu-id="42f93-128">Allows you to confirm each piece of inventory from the mobile device.</span></span> |
|  <span data-ttu-id="42f93-129">Osade maksimaalne arv</span><span class="sxs-lookup"><span data-stu-id="42f93-129">Maximum number of pieces</span></span>  |                   <span data-ttu-id="42f93-130">Komplekteerimistöö jaoks saadaval, kui osa komplekteerimise kinnitamine on lubatud.</span><span class="sxs-lookup"><span data-stu-id="42f93-130">Available for pick work if piece picking confirmation is enabled.</span></span> <span data-ttu-id="42f93-131">Määrab piirmäära ühikute arvule, mille peate kinnitama.</span><span class="sxs-lookup"><span data-stu-id="42f93-131">Sets a limit to the number of pieces that you must confirm.</span></span>                   |

