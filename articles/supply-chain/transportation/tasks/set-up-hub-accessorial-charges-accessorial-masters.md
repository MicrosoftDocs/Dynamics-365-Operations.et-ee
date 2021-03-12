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
ms.search.form: TMSCarrierAccessorial,TMSAccessorialMaster, TMSHubAccessorial
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e012850a390f373088e758418b68c7eaae7ad53e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4973981"
---
# <a name="set-up-hub-accessorial-charges-and-accessorial-masters"></a><span data-ttu-id="c1834-103">Keskuse lisatasude ja lisade koondandmete seadistamine</span><span class="sxs-lookup"><span data-stu-id="c1834-103">Set up hub accessorial charges and accessorial masters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c1834-104">See protseduur kirjeldab keskuse lisade koondandmete loomist ja nende koondandmete kasutamist keskuse lisade tasu loomiseks.</span><span class="sxs-lookup"><span data-stu-id="c1834-104">This procedure shows how to create an accessorial master for a hub and use that master to create a hub accessorial charge.</span></span> <span data-ttu-id="c1834-105">Protseduur kasutab USMF-i andmekomplekti.</span><span class="sxs-lookup"><span data-stu-id="c1834-105">The procedure uses the USMF dataset.</span></span> <span data-ttu-id="c1834-106">Seda seadistust teeb üldjuhul transpordikoordinaator.</span><span class="sxs-lookup"><span data-stu-id="c1834-106">This set up will typically be done by a transportation coordinator.</span></span>


## <a name="set-up-a-hub-master"></a><span data-ttu-id="c1834-107">Keskuse koondandmete seadistamine</span><span class="sxs-lookup"><span data-stu-id="c1834-107">Set up a hub master</span></span>
1. <span data-ttu-id="c1834-108">Avage Transpordihaldus > Seadistus > Hinnang > Lisade koondandmed.</span><span class="sxs-lookup"><span data-stu-id="c1834-108">Go to Transportation management > Setup > Rating > Accessorial masters.</span></span>
2. <span data-ttu-id="c1834-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="c1834-109">Click New.</span></span>
3. <span data-ttu-id="c1834-110">Sisestage väärtus väljale Lisade koondandmed.</span><span class="sxs-lookup"><span data-stu-id="c1834-110">In the Accessorial master field, type a value.</span></span>
4. <span data-ttu-id="c1834-111">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="c1834-111">In the Name field, type a value.</span></span>
5. <span data-ttu-id="c1834-112">Valige väljal Lisatasu tüüp suvand Keskus.</span><span class="sxs-lookup"><span data-stu-id="c1834-112">In the Accessorial type field, select 'Hub'.</span></span>
6. <span data-ttu-id="c1834-113">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="c1834-113">Click Save.</span></span>
7. <span data-ttu-id="c1834-114">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c1834-114">Close the page.</span></span>

## <a name="set-up-a-hub-accessorial-charge"></a><span data-ttu-id="c1834-115">Keskuse lisatasu seadistamine</span><span class="sxs-lookup"><span data-stu-id="c1834-115">Set up a hub accessorial charge</span></span>
1. <span data-ttu-id="c1834-116">Avage Transpordihaldus > Seadistus > Hinnang > Keskuse lisatasud.</span><span class="sxs-lookup"><span data-stu-id="c1834-116">Go to Transportation management > Setup > Rating > Hub accessorial charges.</span></span>
2. <span data-ttu-id="c1834-117">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="c1834-117">Click New.</span></span>
3. <span data-ttu-id="c1834-118">Sisestage väärtus väljale Keskuse lisade ID.</span><span class="sxs-lookup"><span data-stu-id="c1834-118">In the Hub accessorial ID field, type a value.</span></span>
4. <span data-ttu-id="c1834-119">Klõpsake väljal Keskus otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="c1834-119">In the Hub field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="c1834-120">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="c1834-120">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="c1834-121">Valige suvand väljalt Keskuse asend.</span><span class="sxs-lookup"><span data-stu-id="c1834-121">In the Hub position field, select an option.</span></span>
    * <span data-ttu-id="c1834-122">Saate luua tasu kui vastuvõtu või kohaleviimisena.</span><span class="sxs-lookup"><span data-stu-id="c1834-122">You can either create the charge as a pickup or drop-off.</span></span> <span data-ttu-id="c1834-123">Teie valikust olenevalt rakendatakse tasu teie marsruudi asjakohasele transpordisegmendile.</span><span class="sxs-lookup"><span data-stu-id="c1834-123">Depending on your selection the charge will be applied to the corresponding transportation segment on your route.</span></span>  
7. <span data-ttu-id="c1834-124">Klõpsake väljal Lisade koondandmed otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="c1834-124">In the Accessorial master field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="c1834-125">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="c1834-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="c1834-126">Valige äsja loodud koondandmed.</span><span class="sxs-lookup"><span data-stu-id="c1834-126">Select the master you just created.</span></span>  
9. <span data-ttu-id="c1834-127">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="c1834-127">Click Save.</span></span>
10. <span data-ttu-id="c1834-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="c1834-128">Close the page.</span></span>

