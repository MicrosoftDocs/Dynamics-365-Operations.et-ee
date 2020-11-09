---
title: Kiirelt komplekteeritava kauba ümberjaotamise häälestus
description: Selles teemas kirjeldatakse, kuidas lubada laotöötajatel kiiresti alternatiivseid asukohti leida, kui selles asukohas, kuhu nad suunati, pole piisavalt varusid.
author: ShylaThompson
manager: tfehr
ms.date: 06/29/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSWorkException, WHSWorker, WHSLocationWithWorkException
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: mirzaab
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e8f5c23f82e96145f411ec993f766a90137b5b8
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4015960"
---
# <a name="set-up-short-picking-item-reallocation"></a><span data-ttu-id="7d7f5-103">Kiirelt komplekteeritava kauba ümberjaotamise häälestus</span><span class="sxs-lookup"><span data-stu-id="7d7f5-103">Set up short picking item reallocation</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7d7f5-104">See protseduur näitab, kuidas lubada laotöötajatel kiiresti alternatiivseid asukohti leida, kui selles asukohas, kuhu nad suunati, pole piisavalt varusid.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-104">This procedure shows how to enable warehouse workers to quickly find alternative locations if there isn’t sufficient inventory at the location they’ve been directed to.</span></span> 

<span data-ttu-id="7d7f5-105">Ümberjaotamisprotsessi juhib **Tööerand** ja seda kasutab lao **töötaja.**</span><span class="sxs-lookup"><span data-stu-id="7d7f5-105">The reallocation process is controlled by a **Work exception** and used by the warehouse **worker.**</span></span>

<span data-ttu-id="7d7f5-106">Kasutada on võimalik automaatset, käsitsi või mõlemat ümberjaotamisprotsessi.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-106">It is possible to use Automatic, Manual, or both reallocation processes:</span></span>

- <span data-ttu-id="7d7f5-107">Automaatne ümberjaotamine – asukohadirektiive kasutatakse selleks, et määrata, kas kaubad on saadaval teises asukohas.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-107">Automatic reallocation - Location directives are used to determine if the goods are available at another location.</span></span> <span data-ttu-id="7d7f5-108">Võimaluse korral uuendatakse tööd ja lao kasutaja suunatakse alternatiivsesse asukohta.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-108">If possible, the work will be updated and the warehouse user will be directed to the alternative location.</span></span>
- <span data-ttu-id="7d7f5-109">Käsitsi ümberjaotamine – võimaldab lao kasutajal valida ühe või mitme asukoha vahel, millel on reserveerimata kaubakoguseid.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-109">Manual reallocation - Allows the warehouse user to select from one or more locations with unreserved quantities of goods.</span></span> 
- <span data-ttu-id="7d7f5-110">Automaatne ja käsitsi – kui süsteem ei saa automaatset ümberjaotamist teha ja reserveerimata kogustega asukohti on saadaval, palutakse kasutajal valida asukoht.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-110">Automatic and manual - If the system is unable to perform an automatic reallocation, and locations are available with unreserved quantities, the user will be prompted to select a location.</span></span>

## <a name="set-up-work-exceptions"></a><span data-ttu-id="7d7f5-111">Tööerandite häälestamine</span><span class="sxs-lookup"><span data-stu-id="7d7f5-111">Set up work exceptions</span></span>
<span data-ttu-id="7d7f5-112">Määratleda saab mitu tööerandit erinevate kauba ümberjaotamise poliitikatega, et laotöötaja saaks valida neist ühe töödeldava saadetise vajaduste põhjal.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-112">It's possible to define several work exceptions with different item reallocation policies to enable the warehouse worker to choose one based on the needs of the shipment that they are processing.</span></span>

<span data-ttu-id="7d7f5-113">Selle protseduuri loomiseks kasutati demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-113">The USMF demo data company was used to create this procedure.</span></span>

1. <span data-ttu-id="7d7f5-114">Minge **Navigeerimispaanil** jaotisesse **Laohaldus> Seadistamine> Töö> Töö erandid**.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-114">In the **Navigation pane** , go to **Warehouse management > Setup > Work > Work exceptions**.</span></span>
2. <span data-ttu-id="7d7f5-115">Klõpsake valikut **Uus**</span><span class="sxs-lookup"><span data-stu-id="7d7f5-115">Click **New**</span></span> 
3. <span data-ttu-id="7d7f5-116">Tippige väärtus väljale **Tööerandi kood**.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-116">In the **Work exception code** field, type a value.</span></span> <span data-ttu-id="7d7f5-117">See on selle erandi pealkiri.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-117">This will be the title of this exception .</span></span> <span data-ttu-id="7d7f5-118">Näiteks Puuduva käsitsi valimine.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-118">For example, Short picking manual.</span></span>
4. <span data-ttu-id="7d7f5-119">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-119">In the **Description** field, type a value.</span></span> <span data-ttu-id="7d7f5-120">See on selle erandi kasutuse lühikirjeldus.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-120">This will be a short description of the usage of this exception.</span></span> <span data-ttu-id="7d7f5-121">Näiteks Puuduva valimine – kaup pole saadaval.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-121">For example, Short picking - item not available.</span></span>
5. <span data-ttu-id="7d7f5-122">Tehke väljal **Erandi** tüüp valik **Puuduva valimine**.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-122">In the **Exception** type field, select **Short pick**.</span></span>
6. <span data-ttu-id="7d7f5-123">Märkige ruut **Varude korrigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-123">Select the **Adjust inventory** check box.</span></span> <span data-ttu-id="7d7f5-124">Selle valimisel reguleeritakse varud puuduva valimise asukohas automaatselt väärtusele 0.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-124">If selected, inventory will automatically be adjusted to 0 at the short picked location.</span></span>
7. <span data-ttu-id="7d7f5-125">Valige või sisestage väärtus väljal **Vaikimisi korrigeerimistüübi kood**.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-125">In the **Default adjustment type code** field, enter or select a value.</span></span> <span data-ttu-id="7d7f5-126">Näiteks USMF-is saate valida **Remove Res Adj Out**. Iga korrigeerimise tüübi kood sisaldab nelja omadust: nimi, kirjeldus, lao töölehe nimi ja **Eemalda reserveeringud**.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-126">For example, in USMF you can select **Remove Res Adj Out**. Each Adjustment type code contains four characteristics: name, description, inventory journal name, and **Remove reservations**.</span></span> <span data-ttu-id="7d7f5-127">Valiku **Eemalda reserveeringud** lubamisel eemaldatakse ka puuduva valimise tellimuse rea reserveeringud.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-127">If **Remove reservations** is enabled, the short-picked order line's reservations will be removed.</span></span>  
8. <span data-ttu-id="7d7f5-128">Valige väljal **Kauba ümberjaotamine** väärtus, nt Käsitsi.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-128">In the **Item reallocation** field, select a value, such as Manual.</span></span> <span data-ttu-id="7d7f5-129">Kui teete valiku Käsitsi või Automaatne ja Käsitsi, peab laotöötajale olema antud võimalus kasutada käsitsi ümberjaotamist.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-129">If you select Manual, or Automatic and Manual, the warehouse worker needs to be enabled to use manual reallocation.</span></span>

## <a name="set-up-a-worker-to-use-manual-item-reallocation"></a><span data-ttu-id="7d7f5-130">Töötaja seadistamine käsitsi kauba ümberjaotamist kasutama</span><span class="sxs-lookup"><span data-stu-id="7d7f5-130">Set up a worker to use manual item reallocation</span></span>

<span data-ttu-id="7d7f5-131">Selle protseduuri loomiseks kasutati demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-131">The USMF demo data company was used to create this procedure.</span></span>

1. <span data-ttu-id="7d7f5-132">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-132">Close the page.</span></span>
2. <span data-ttu-id="7d7f5-133">Avage **Navigeerimispaneelil** Moodulid > **Laohaldus > Seaditus > Töö**.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-133">In the **Navigation pane** , go to **Warehouse management > Setup > Worker**.</span></span>
3. <span data-ttu-id="7d7f5-134">Klõpsake valikut **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-134">Click **Edit**.</span></span>
4. <span data-ttu-id="7d7f5-135">Valige loendist töötaja.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-135">In the list, select worker.</span></span> <span data-ttu-id="7d7f5-136">Näiteks Julia Funderburk.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-136">For example, Julia Funderburk.</span></span>
5. <span data-ttu-id="7d7f5-137">Laiendage kiirkaarti **Kasutajad**.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-137">Expand the **Users** FastTab.</span></span>
6. <span data-ttu-id="7d7f5-138">Valige loendist **Kasutaja ID**.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-138">In the list, select a **User ID**.</span></span> <span data-ttu-id="7d7f5-139">Näiteks 24.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-139">For example, 24.</span></span>
7. <span data-ttu-id="7d7f5-140">Laiendage kiirkaarti **Töö**.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-140">Expand the **Work** FastTab.</span></span>
8. <span data-ttu-id="7d7f5-141">Tehke väljal **Luba käsitsi kauba ümberjaotamine** valik **Jah**.</span><span class="sxs-lookup"><span data-stu-id="7d7f5-141">Select **Yes** in the **Allow manual item reallocation** field.</span></span>
