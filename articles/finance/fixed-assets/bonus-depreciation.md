---
title: Lisakulum
description: Selles artiklis antakse ülevaade lisakulumi funktsioonist.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBonus
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 3621
ms.assetid: 835ec594-744e-461c-a676-1b9abc094173
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 687ba57042ad65d3a1ff4ad92f0da774c6751eac
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2187379"
---
# <a name="bonus-depreciation"></a><span data-ttu-id="aee7d-103">Lisakulum</span><span class="sxs-lookup"><span data-stu-id="aee7d-103">Bonus depreciation</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="aee7d-104">Selles artiklis antakse ülevaade lisakulumi funktsioonist.</span><span class="sxs-lookup"><span data-stu-id="aee7d-104">This article provides an overview of the bonus depreciation functionality.</span></span>

<span data-ttu-id="aee7d-105">Lisakulumi rakendamine võimaldab teil põhivarale selle esimesel kasulikul töö- ja amortisatsiooniaastal lisakulumit arvestada.</span><span class="sxs-lookup"><span data-stu-id="aee7d-105">For bonus depreciation, you can take extra or bonus depreciation amounts during the first year that the asset is put in service and depreciated.</span></span> <span data-ttu-id="aee7d-106">Lisakulum tuleb võtta enne mis tahes kulumiarvutusi.</span><span class="sxs-lookup"><span data-stu-id="aee7d-106">Bonus depreciation must be taken before any other depreciation calculations.</span></span> <span data-ttu-id="aee7d-107">Seetõttu on kõige parem kasutada lisakulumit raamatutega, kus funktsioon Pearaamatusse sisestamine on keelatud.</span><span class="sxs-lookup"><span data-stu-id="aee7d-107">Therefore, it's best to use bonus depreciation with books where the Post to general ledger functionality is disabled.</span></span> <span data-ttu-id="aee7d-108">Saate kasutada suvandit **Pearaamatusse sisestamata kannete kustutamine**, et kustutada selliste raamatute kannete ajalugu, mis ei sisestada pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="aee7d-108">You can use the **Delete transactions not posted to general ledger** option to delete historical transactions for books that don't post to the general ledger.</span></span> <span data-ttu-id="aee7d-109">Seejärel saate mahutada lisakulumi hiljem vara elutsüklisse, kustutades eelnevalt sisestatud kulumikanded.</span><span class="sxs-lookup"><span data-stu-id="aee7d-109">You can then accommodate bonus depreciation later in the asset life cycle by deleting depreciation transactions that were previously posted.</span></span> 

<span data-ttu-id="aee7d-110">Lisakulumit saate arvutada soovitusprotsessi abil või luua lisakulumikanded käsitsi.</span><span class="sxs-lookup"><span data-stu-id="aee7d-110">You can calculate bonus depreciation by using the proposal process, or you can create manual bonus depreciation transactions.</span></span> <span data-ttu-id="aee7d-111">Lisakulumikandeid ei ole võimalik luua, kui selles põhivara kulumiraamatus on kulumikandeid või kulumi korrigeerimiskandeid.</span><span class="sxs-lookup"><span data-stu-id="aee7d-111">You can't create bonus depreciation transactions if depreciation transactions or depreciation adjustment transactions exist for that asset book.</span></span>

<span data-ttu-id="aee7d-112">Kui kasutate lisakulumi arvutamisel soovitusprotsessi, kaasatakse aluse arvutamisse kõik olemasolevad lisakulumikanded.</span><span class="sxs-lookup"><span data-stu-id="aee7d-112">When you use the proposal process to calculate bonus depreciation, all existing bonus transactions are included in the calculation of the basis.</span></span> <span data-ttu-id="aee7d-113">Arvutus hõlmab ka mis tahes varasemaid lisakulumeid, mille sisestasite vara jaoks käsitsi.</span><span class="sxs-lookup"><span data-stu-id="aee7d-113">The calculation also includes any previous bonus depreciations that you manually entered for the asset.</span></span> 

<span data-ttu-id="aee7d-114">Kui põhivarale määratakse rohkem kui üks lisakulum, tuleb teil määrata prioriteedid.</span><span class="sxs-lookup"><span data-stu-id="aee7d-114">If more than one bonus depreciation will be taken for an asset, the priority is considered.</span></span> <span data-ttu-id="aee7d-115">Iga lisakulum vähendab põhivara järgmise lisakulumi alust.</span><span class="sxs-lookup"><span data-stu-id="aee7d-115">Each bonus reduces the asset basis for the next bonus.</span></span> <span data-ttu-id="aee7d-116">Jääkväärtust põhivara lisakulumi aluse arvutustesse ei kaasata ning kulumi arvestusreeglid lisakulumile ei kehti.</span><span class="sxs-lookup"><span data-stu-id="aee7d-116">Salvage value isn't considered in the asset basis for bonus depreciation calculations, and the depreciation convention doesn't apply for bonus depreciation.</span></span> 

<span data-ttu-id="aee7d-117">Praegu on Ameerika Ühendriikides määratletud teatud vara sektsiooni 179 varana.</span><span class="sxs-lookup"><span data-stu-id="aee7d-117">Currently, in the United States, some property qualifies as Section 179 property.</span></span> <span data-ttu-id="aee7d-118">Sektsiooni 179 mahaarvamise abil saate taastada kogu või osa mõne vara maksumusest teatud piirini.</span><span class="sxs-lookup"><span data-stu-id="aee7d-118">By using the Section 179 deduction, you can recover all or part of the cost of some property, up to a limit.</span></span> <span data-ttu-id="aee7d-119">Saate taastada kulu, arvates selle maha vara kasutuselevõtmise aastal.</span><span class="sxs-lookup"><span data-stu-id="aee7d-119">You can recover the cost by deducting it in the year when you put the property in service.</span></span>

## <a name="example"></a><span data-ttu-id="aee7d-120">Näide</span><span class="sxs-lookup"><span data-stu-id="aee7d-120">Example</span></span>
<span data-ttu-id="aee7d-121">Järgmised lisakulumid on seostatud vararaamatuga.</span><span class="sxs-lookup"><span data-stu-id="aee7d-121">The following bonus depreciations are associated with an asset book:</span></span>

-   <span data-ttu-id="aee7d-122">**Sektsioon 179:** 1000,00, prioriteet 1</span><span class="sxs-lookup"><span data-stu-id="aee7d-122">**Section 179:** 1,000.00, Priority 1</span></span>
-   <span data-ttu-id="aee7d-123">**Tsooniprivileeg:** 30 protsenti, prioriteet 2</span><span class="sxs-lookup"><span data-stu-id="aee7d-123">**Liberty Zone:** 30 percent, Priority 2</span></span>

<span data-ttu-id="aee7d-124">Vara soetusmaksumus on 5000,00.</span><span class="sxs-lookup"><span data-stu-id="aee7d-124">The asset acquisition cost is 5,000.00.</span></span> <span data-ttu-id="aee7d-125">Lisakulumi arvutamisel saadakse sektsiooni 179 esimeseks lisakulumisummaks 1000,00 dollarit.</span><span class="sxs-lookup"><span data-stu-id="aee7d-125">When bonus depreciation is calculated, the first bonus depreciation amount is 1,000.00 for the Section 179 depreciation.</span></span> 

<span data-ttu-id="aee7d-126">Järgmine lisakulumi summa, tsooniprivileegi kulumi puhul, arvutatakse järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="aee7d-126">The next bonus depreciation amount, for the Liberty Zone depreciation, is calculated as follows:</span></span> 

<span data-ttu-id="aee7d-127">Soetuskulu – 1000 (sektsiooni 179 kulum) x 30 protsenti = 1200</span><span class="sxs-lookup"><span data-stu-id="aee7d-127">Acquisition cost – 1,000 (Section 179 depreciation) × 30 percent = 1,200</span></span> 

<span data-ttu-id="aee7d-128">Kui lisakulumi summa on rohkem kui ülejäänud soetusmaksumus, on lisakulumi summa lisakulumi arvutuse tulemus või ülejäänud soetusmaksumus, misiganes summa on väiksem.</span><span class="sxs-lookup"><span data-stu-id="aee7d-128">If the bonus depreciation amount is more than the remaining acquisition cost, the bonus depreciation amount is either the result of the bonus depreciation calculation or the remaining acquisition cost, whichever amount is less.</span></span> 

<span data-ttu-id="aee7d-129">Kui soetusmaksumuse jääk on 0 (null) või sellest väiksem, siis lisakulumi kandeid ei looda.</span><span class="sxs-lookup"><span data-stu-id="aee7d-129">If the remaining acquisition cost is 0 (zero) or less, bonus depreciation transactions isn't generated.</span></span> 

<span data-ttu-id="aee7d-130">Lisakulumi arvutamisel soovitusprotsessi abil luuakse lisakulumikanne kõigi rakendatavate põhivara kulumiraamatuga seotud lisakulumikirjete kohta.</span><span class="sxs-lookup"><span data-stu-id="aee7d-130">When bonus depreciation is calculated by using the proposal process, a bonus depreciation transaction is created for all applicable bonus depreciation records that are associated with the asset book.</span></span> 

<span data-ttu-id="aee7d-131">Loodavate lisakulumikirjete arv on piiramatu.</span><span class="sxs-lookup"><span data-stu-id="aee7d-131">You can create an unlimited number of bonus depreciation records.</span></span> <span data-ttu-id="aee7d-132">Pärast nende kirjete põhivaragrupi raamatule rakendatakse need sellele kulumiraamatusse.</span><span class="sxs-lookup"><span data-stu-id="aee7d-132">After you assign those records to the asset group book, they are applied to the asset book.</span></span> 

<span data-ttu-id="aee7d-133">Lisakulum sisestatakse protsendina või kindla summana.</span><span class="sxs-lookup"><span data-stu-id="aee7d-133">Bonus depreciation is entered as either a percentage or a fixed amount.</span></span> <span data-ttu-id="aee7d-134">Kui sisestate kulumisoovitusi, sisestatakse lisakulumikanded raamatusse kulumikannetest eraldi kannetena.</span><span class="sxs-lookup"><span data-stu-id="aee7d-134">When you post depreciation proposals, bonus depreciation transactions are posted to the book as separate transactions from the depreciation transactions.</span></span>


