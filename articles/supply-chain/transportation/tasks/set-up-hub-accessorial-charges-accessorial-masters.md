---
title: Keskuse lisatasude ja lisade koondandmete seadistamine
description: See protseduur kirjeldab keskuse lisade koondandmete loomist ja nende koondandmete kasutamist keskuse lisade tasu loomiseks.
author: ShylaThompson
manager: tfehr
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f385c8079216de0b5e5d16cbdfc9636dd5bc7725
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3214852"
---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a><span data-ttu-id="ca339-103">Keskuse lisatasude ja lisade koondandmete seadistamine</span><span class="sxs-lookup"><span data-stu-id="ca339-103">Set up hub accessorial charges and accessorial masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ca339-104">See protseduur kirjeldab keskuse lisade koondandmete loomist ja nende koondandmete kasutamist keskuse lisade tasu loomiseks.</span><span class="sxs-lookup"><span data-stu-id="ca339-104">This procedure shows how to create an accessorial master for a hub and use that master to create a hub accessorial charge.</span></span> <span data-ttu-id="ca339-105">Protseduur kasutab USMF-i andmekomplekti.</span><span class="sxs-lookup"><span data-stu-id="ca339-105">The procedure uses the USMF dataset.</span></span> <span data-ttu-id="ca339-106">Seda seadistust teeb üldjuhul transpordikoordinaator.</span><span class="sxs-lookup"><span data-stu-id="ca339-106">This set up will typically be done by a transportation coordinator.</span></span>


## <a name="set-up-a-hub-master"></a><span data-ttu-id="ca339-107">Keskuse koondandmete seadistamine</span><span class="sxs-lookup"><span data-stu-id="ca339-107">Set up a hub master</span></span>
1. <span data-ttu-id="ca339-108">Avage Transpordihaldus > Seadistus > Hinnang > Lisade koondandmed.</span><span class="sxs-lookup"><span data-stu-id="ca339-108">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="ca339-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ca339-109">Click New.</span></span>
3. <span data-ttu-id="ca339-110">Sisestage väärtus väljale Lisade koondandmed.</span><span class="sxs-lookup"><span data-stu-id="ca339-110">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="ca339-111">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="ca339-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="ca339-112">Valige väljal Lisatasu tüüp suvand Keskus.</span><span class="sxs-lookup"><span data-stu-id="ca339-112">In the Accessorial type field, select 'Hub'.</span></span>
6. <span data-ttu-id="ca339-113">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ca339-113">Click Save.</span></span>
7. <span data-ttu-id="ca339-114">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ca339-114">Close the page.</span></span>

## <a name="set-up-a-hub-accessorial-charge"></a><span data-ttu-id="ca339-115">Keskuse lisatasu seadistamine</span><span class="sxs-lookup"><span data-stu-id="ca339-115">Set up a hub accessorial charge</span></span>
1. <span data-ttu-id="ca339-116">Avage Transpordihaldus > Seadistus > Hinnang > Keskuse lisatasud.</span><span class="sxs-lookup"><span data-stu-id="ca339-116">Go to Transportation management > Setup > Rating > Hub accessorial charges.</span></span>
2. <span data-ttu-id="ca339-117">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ca339-117">Click New.</span></span>
3. <span data-ttu-id="ca339-118">Sisestage väärtus väljale Keskuse lisade ID.</span><span class="sxs-lookup"><span data-stu-id="ca339-118">In the Hub accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="ca339-119">Klõpsake väljal Keskus otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="ca339-119">In the Hub field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="ca339-120">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="ca339-120">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="ca339-121">Valige suvand väljalt Keskuse asend.</span><span class="sxs-lookup"><span data-stu-id="ca339-121">In the Hub position field, select an option.</span></span>
    * <span data-ttu-id="ca339-122">Saate luua tasu kui vastuvõtu või kohaleviimisena.</span><span class="sxs-lookup"><span data-stu-id="ca339-122">You can either create the charge as a pickup or drop-off.</span></span> <span data-ttu-id="ca339-123">Teie valikust olenevalt rakendatakse tasu teie marsruudi asjakohasele transpordisegmendile.</span><span class="sxs-lookup"><span data-stu-id="ca339-123">Depending on your selection the charge will be applied to the corresponding transportation segment on your route.</span></span>  
7. <span data-ttu-id="ca339-124">Klõpsake väljal Lisade koondandmed otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="ca339-124">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="ca339-125">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="ca339-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="ca339-126">Valige äsja loodud koondandmed.</span><span class="sxs-lookup"><span data-stu-id="ca339-126">Select the master you just created.</span></span>  
9. <span data-ttu-id="ca339-127">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="ca339-127">Click Save.</span></span>
10. <span data-ttu-id="ca339-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ca339-128">Close the page.</span></span>

