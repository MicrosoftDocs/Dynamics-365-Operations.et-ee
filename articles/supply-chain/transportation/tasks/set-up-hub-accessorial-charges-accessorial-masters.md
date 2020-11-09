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
ms.search.form: TMSHubAccessorial, TMSAccessorialMaster, TMSCarrierAccessorial
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f728339ed9a0c6fffa8f6d8171976aafc41fc75e
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4016535"
---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a><span data-ttu-id="a1a50-103">Keskuse lisatasude ja lisade koondandmete seadistamine</span><span class="sxs-lookup"><span data-stu-id="a1a50-103">Set up hub accessorial charges and accessorial masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a1a50-104">See protseduur kirjeldab keskuse lisade koondandmete loomist ja nende koondandmete kasutamist keskuse lisade tasu loomiseks.</span><span class="sxs-lookup"><span data-stu-id="a1a50-104">This procedure shows how to create an accessorial master for a hub and use that master to create a hub accessorial charge.</span></span> <span data-ttu-id="a1a50-105">Protseduur kasutab USMF-i andmekomplekti.</span><span class="sxs-lookup"><span data-stu-id="a1a50-105">The procedure uses the USMF dataset.</span></span> <span data-ttu-id="a1a50-106">Seda seadistust teeb üldjuhul transpordikoordinaator.</span><span class="sxs-lookup"><span data-stu-id="a1a50-106">This set up will typically be done by a transportation coordinator.</span></span>


## <a name="set-up-a-hub-master"></a><span data-ttu-id="a1a50-107">Keskuse koondandmete seadistamine</span><span class="sxs-lookup"><span data-stu-id="a1a50-107">Set up a hub master</span></span>
1. <span data-ttu-id="a1a50-108">Avage Transpordihaldus > Seadistus > Hinnang > Lisade koondandmed.</span><span class="sxs-lookup"><span data-stu-id="a1a50-108">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="a1a50-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="a1a50-109">Click New.</span></span>
3. <span data-ttu-id="a1a50-110">Sisestage väärtus väljale Lisade koondandmed.</span><span class="sxs-lookup"><span data-stu-id="a1a50-110">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="a1a50-111">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="a1a50-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="a1a50-112">Valige väljal Lisatasu tüüp suvand Keskus.</span><span class="sxs-lookup"><span data-stu-id="a1a50-112">In the Accessorial type field, select 'Hub'.</span></span>
6. <span data-ttu-id="a1a50-113">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="a1a50-113">Click Save.</span></span>
7. <span data-ttu-id="a1a50-114">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a1a50-114">Close the page.</span></span>

## <a name="set-up-a-hub-accessorial-charge"></a><span data-ttu-id="a1a50-115">Keskuse lisatasu seadistamine</span><span class="sxs-lookup"><span data-stu-id="a1a50-115">Set up a hub accessorial charge</span></span>
1. <span data-ttu-id="a1a50-116">Avage Transpordihaldus > Seadistus > Hinnang > Keskuse lisatasud.</span><span class="sxs-lookup"><span data-stu-id="a1a50-116">Go to Transportation management > Setup > Rating > Hub accessorial charges.</span></span>
2. <span data-ttu-id="a1a50-117">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="a1a50-117">Click New.</span></span>
3. <span data-ttu-id="a1a50-118">Sisestage väärtus väljale Keskuse lisade ID.</span><span class="sxs-lookup"><span data-stu-id="a1a50-118">In the Hub accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="a1a50-119">Klõpsake väljal Keskus otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="a1a50-119">In the Hub field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="a1a50-120">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="a1a50-120">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="a1a50-121">Valige suvand väljalt Keskuse asend.</span><span class="sxs-lookup"><span data-stu-id="a1a50-121">In the Hub position field, select an option.</span></span>
    * <span data-ttu-id="a1a50-122">Saate luua tasu kui vastuvõtu või kohaleviimisena.</span><span class="sxs-lookup"><span data-stu-id="a1a50-122">You can either create the charge as a pickup or drop-off.</span></span> <span data-ttu-id="a1a50-123">Teie valikust olenevalt rakendatakse tasu teie marsruudi asjakohasele transpordisegmendile.</span><span class="sxs-lookup"><span data-stu-id="a1a50-123">Depending on your selection the charge will be applied to the corresponding transportation segment on your route.</span></span>  
7. <span data-ttu-id="a1a50-124">Klõpsake väljal Lisade koondandmed otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="a1a50-124">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="a1a50-125">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="a1a50-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a1a50-126">Valige äsja loodud koondandmed.</span><span class="sxs-lookup"><span data-stu-id="a1a50-126">Select the master you just created.</span></span>  
9. <span data-ttu-id="a1a50-127">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="a1a50-127">Click Save.</span></span>
10. <span data-ttu-id="a1a50-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a1a50-128">Close the page.</span></span>

