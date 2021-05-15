---
title: Tehniliste muudatuste halduse ülevaade
description: See teema annab ülevaate tehniliste muudatuste haldusest, mis aitab teil planeerida ja hallata toote versioonimist ning hallata toote töötsüklit ja tehnilisi muudatusi.
author: t-benebo
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: d7c0839ffbea80904ca12d1cba7ba9880f721cdd
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947516"
---
# <a name="engineering-change-management-overview"></a><span data-ttu-id="da12f-103">Tehniliste muudatuste halduse ülevaade</span><span class="sxs-lookup"><span data-stu-id="da12f-103">Engineering change management overview</span></span>

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a><span data-ttu-id="da12f-104">Funktsiooni kokkuvõte</span><span class="sxs-lookup"><span data-stu-id="da12f-104">Feature summary</span></span>

<span data-ttu-id="da12f-105">Tootjad nõuavad ranget tooteandmete haldamist, sest versioonihaldus ja tehniliste muudatuste haldus on, et saavutada edu tänapäeval, kus toote töötsüklid pidevalt lühenevad, kvaliteedi- ja töökindlusnõudeid karmistatakse ning tooteohutusele keskendutakse üha enam.</span><span class="sxs-lookup"><span data-stu-id="da12f-105">Today's manufacturers require strong product data management, version control, and engineering change management to succeed in a world of constantly shrinking product lifecycles, increased quality and reliability requirements, and an increased focus on product safety.</span></span>

<span data-ttu-id="da12f-106">Tehniliste muudatuste haldus loob tooteandmete haldamise ümber struktuuri ja korra ning võimaldab toodete määratlemist, välja andmist ja läbivaatamist kontrollitud viisil, mida töövood toetavad.</span><span class="sxs-lookup"><span data-stu-id="da12f-106">Engineering change management brings structure and discipline to the product data management process, and enables products to be defined, released, and revised in a controlled manner that is supported by workflows.</span></span><span data-ttu-id="da12f-107"> Toote versioonide ja tehniliste muudatuste haldamise kaudu saate dokumenteerida, hinnata ja rakendada tehnilisi muudatusi toote kogu töötsükli jooksul.</span><span class="sxs-lookup"><span data-stu-id="da12f-107"> Through product versions and engineering change management, you can document, assess the impact of, and apply engineering changes throughout the whole lifecycle of a product.</span></span>

<span data-ttu-id="da12f-108">Tehniliste muudatuste haldus aitab teil planeerida ja hallata toote versioonimist ning hallata toote töötsüklit ja tehnilisi muudatusi.</span><span class="sxs-lookup"><span data-stu-id="da12f-108">Engineering change management helps you plan and manage product versioning, and manage product lifecycles and engineering changes.</span></span> <span data-ttu-id="da12f-109">Siin on selle pakutavad põhifunktsioonid.</span><span class="sxs-lookup"><span data-stu-id="da12f-109">Here is a list of its main features:</span></span>

- <span data-ttu-id="da12f-110">Toodete versioonimine</span><span class="sxs-lookup"><span data-stu-id="da12f-110">Product versioning</span></span>
- <span data-ttu-id="da12f-111">Täiustatud toote väljalaskefunktsioon, mis võimaldab teil säilitada toote koondandmed ühe juriidilise isiku juures (tehnikaettevõttes) ja avaldada teistele juriidilistele isikutele täielikult konfigureeritud välja antud toote</span><span class="sxs-lookup"><span data-stu-id="da12f-111">Enhanced product release functionality that lets you maintain product master data in one legal entity (the engineering company) and publish the fully configured released product to other legal entities</span></span>
- <span data-ttu-id="da12f-112">Selle nõutava teabe kinnitamise reeglid sisestatakse enne toote versiooni aktiveerimist (valmisolekukontrollid)</span><span class="sxs-lookup"><span data-stu-id="da12f-112">Rules for validating that required information is entered before a product version is activated (readiness checks)</span></span>
- <span data-ttu-id="da12f-113">Põhjalik kontroll selle üle, millal välja antud toodet saab konkreetses äriprotsessis kasutada, täiustab toote töötsükli haldamist</span><span class="sxs-lookup"><span data-stu-id="da12f-113">Improved product lifecycle management through fine-grained control over when a released product can be used in specific business processes</span></span>
- <span data-ttu-id="da12f-114">Tehniliste muudatuste taotlusi toetavad töövood</span><span class="sxs-lookup"><span data-stu-id="da12f-114">Engineering change requests that are supported by workflows</span></span>
- <span data-ttu-id="da12f-115">Tehniliste muudatuste tellimusi toetavad töövood</span><span class="sxs-lookup"><span data-stu-id="da12f-115">Engineering change orders that are supported by workflows</span></span>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4HE6B]

<span data-ttu-id="da12f-116">See video ([Muudatuste halduse funktsioonid Dynamics 365 Supply Chain Managementis](https://youtu.be/N313FqvRuBc)) on [ esitusloendis Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), mis on saadaval YouTube'is.</span><span class="sxs-lookup"><span data-stu-id="da12f-116">The preceding video ([Change management capabilities in Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="turn-on-the-engineering-change-management-and-version-dimension-features-for-your-system"></a><span data-ttu-id="da12f-117">Lülitage oma süsteemi jaoks sisse tehnilise muudatuse halduse ja versiooni dimensiooni funktsioonid</span><span class="sxs-lookup"><span data-stu-id="da12f-117">Turn on the engineering change management and version dimension features for your system</span></span>

<span data-ttu-id="da12f-118">Enne, kui saate kasutada tehnilise muudatuse haldust, peate lubama nii funktsiooni *Tehnilise muudatuse haldus* kui selle konfiguratsioonivõtme.</span><span class="sxs-lookup"><span data-stu-id="da12f-118">Before you can use engineering change management, you must enable both the *Engineering Change Management* feature and its configuration key.</span></span> <span data-ttu-id="da12f-119">Kui soovite ka jälgida kannetes toodete versiooni dimensiooni (valikuline), peate lisaks lubama funktsiooni *Tooteversiooni dimensioon* ja selle konfiguratsioonivõtme.</span><span class="sxs-lookup"><span data-stu-id="da12f-119">If you also want to track the version dimension of products in transactions (optional), then you must also enable the *Product version dimension* feature and its configuration key.</span></span>

<span data-ttu-id="da12f-120">Esmalt lülitage sisse funktsioonid, järgides järgmisi etappe.</span><span class="sxs-lookup"><span data-stu-id="da12f-120">First, turn on the features by following these steps.</span></span>

1. <span data-ttu-id="da12f-121">Avage [Funktsioonihaldus rakenduses](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruum.</span><span class="sxs-lookup"><span data-stu-id="da12f-121">Go to the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace.</span></span>
1. <span data-ttu-id="da12f-122">Otsige värskendusi.</span><span class="sxs-lookup"><span data-stu-id="da12f-122">Check for updates.</span></span>
1. <span data-ttu-id="da12f-123">Lülitage sisse funktsioon nimega **Tehniliste muudatuste haldus**.</span><span class="sxs-lookup"><span data-stu-id="da12f-123">Turn on the feature that is named **Engineering Change Management**.</span></span>
1. <span data-ttu-id="da12f-124">Kui soovite seda kasutada, lülitage sisse ka funktsioon nimega **Tootedimensiooni versioon**.</span><span class="sxs-lookup"><span data-stu-id="da12f-124">If you want to use it, then also turn on the feature that is named **Product dimension version**.</span></span>

<span data-ttu-id="da12f-125">Seejärel lülitage sisse konfiguratsioonivõtmed, järgides järgmisi etappe.</span><span class="sxs-lookup"><span data-stu-id="da12f-125">Next, turn on the configuration keys by following these steps.</span></span>

1. <span data-ttu-id="da12f-126">Pange oma süsteem hooldusrežiimi, nagu on kirjeldatud teemas [Hooldusrežiim](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="da12f-126">Put your system into maintenance mode, as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="da12f-127">Valige suvandid **Süsteemihaldus \> Häälestus \> Litsentsi konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="da12f-127">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="da12f-128">Laiendage **Äritegevuse** sõlmpunkti.</span><span class="sxs-lookup"><span data-stu-id="da12f-128">Expand the **Trade** node.</span></span>
1. <span data-ttu-id="da12f-129">Lubage põhifunktsiooni konfiguratsioonivõti, valides märkeruudu **Tehniliste muudatuste haldus**.</span><span class="sxs-lookup"><span data-stu-id="da12f-129">Enable the configuration key for the main feature by selecting the **Engineering Change Management** check box.</span></span> <span data-ttu-id="da12f-130">(Sõlmpunkti pole vaja laiendada, kui te ei soovi keelata ka üht või mõlemat selle alamfunktsiooni.)</span><span class="sxs-lookup"><span data-stu-id="da12f-130">(It isn't necessary to expand the node unless you also want to disable one or both of its sub-features.)</span></span>
1. <span data-ttu-id="da12f-131">Kui soovite kasutada ka versiooni dimensiooni, märkige ruut **Tootedimensioon – versioon**.</span><span class="sxs-lookup"><span data-stu-id="da12f-131">If you also want to use the version dimension, then select the **Product dimension - Version** check box.</span></span> <span data-ttu-id="da12f-132">(See märkeruut asub loendis allpool, mitte pesastatud **Tehniliste muudatuste halduse** sõlmpunkti alla.)</span><span class="sxs-lookup"><span data-stu-id="da12f-132">(This check box is further down the list, not nested under the **Engineering Change Management** node.)</span></span>
1. <span data-ttu-id="da12f-133">Lülitage hooldusrežiim välja, nagu on kirjeldatud teemas [Hooldusrežiim](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="da12f-133">Turn off maintenance mode, as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="da12f-134">Alates 2022. aasta aprillist lubatakse kõigi uute installide puhul vaikimisi nii **Tehniliste muudatuste haldus** kui ka **Toote dimensioon – versioon** litsentsivõtmed, kuid vajadusel saate need siiski keelata.</span><span class="sxs-lookup"><span data-stu-id="da12f-134">Starting in April 2022, the license keys for both **Engineering Change Management** and **Product dimension - Version** will be enabled by default for all new installations, but you will still be able to disable them if needed.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
