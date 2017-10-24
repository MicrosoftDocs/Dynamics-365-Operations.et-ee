---
title: "Kuluelemendi dimensiooniliikmete vastendamine dimensiooniliikmete ühtse mudeliga"
description: "Erinevate kuluelemendi dimensiooni liikmete vastendamisega kuluelemendi dimensiooni liikmete ühisele kogumile ühendate andmed analüüsi otstarbel ühisesse vormingusse."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension, CAMDimensionMember
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: yuyus
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: b15e251410937ff4f85ecdfaa55ca1a998d1d1ac
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="map-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a><span data-ttu-id="ed86d-103">Kuluelemendi dimensiooniliikmete vastendamine dimensiooniliikmete ühtse mudeliga</span><span class="sxs-lookup"><span data-stu-id="ed86d-103">Map cost element dimension members to a common set of dimension members</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="ed86d-104">Erinevate kuluelemendi dimensiooni liikmete vastendamisega kuluelemendi dimensiooni liikmete ühisele kogumile ühendate andmed analüüsi otstarbel ühisesse vormingusse.</span><span class="sxs-lookup"><span data-stu-id="ed86d-104">By mapping different cost element dimension members to a common set of cost element dimension members, you merge data into a common format for analysis purposes.</span></span>

<span data-ttu-id="ed86d-105">Kui olete globaalne ettevõtte ja järgite seadusjärgseid raamatupidamisnõudeid, võite kasutada mitut kontoplaani.</span><span class="sxs-lookup"><span data-stu-id="ed86d-105">If you're a global company and comply with statutory accounting requirements, you might use multiple charts of accounts.</span></span> <span data-ttu-id="ed86d-106">Kuluelemendi dimensiooni liikmete importimisel erinevatest kontoplaanidest saate lõpuks kontode segu.</span><span class="sxs-lookup"><span data-stu-id="ed86d-106">When you import cost element dimension members from different charts of accounts, you can end up with a mix of accounts.</span></span> <span data-ttu-id="ed86d-107">Siiski võib nendel kontodel tegelikult olla sama struktuur ja võite soovi korral analüüsida ja eraldada kulud neile, kasutades ühist vormingut.</span><span class="sxs-lookup"><span data-stu-id="ed86d-107">However, these accounts might actually have the same nature, and you might want to analyze and allocate costs for them by using a common format.</span></span>

## <a name="map-cost-element-dimension-members-to-a-common-format"></a><span data-ttu-id="ed86d-108">Kuluelemendi dimensiooni liikmete vastendamine ühisele vormingule</span><span class="sxs-lookup"><span data-stu-id="ed86d-108">Map cost element dimension members to a common format</span></span>
<span data-ttu-id="ed86d-109">Järgmine näide näitab teile, kuidas teie kulukontrollerina saate luua kuluarvestuses uue kuluelemendi dimensiooni, mis vastendab kuluelemendi dimensiooni liikmed USA ja Prantsuse kontoplaani struktuurist kuluelemendi dimensiooni liikmete ühisele kogumile.</span><span class="sxs-lookup"><span data-stu-id="ed86d-109">The following example shows how you, as a cost controller, can create a new cost element dimension in Cost accounting that maps cost element dimension members from the US chart of accounts structure and the French chart of accounts structure to a common set of cost element dimension members.</span></span> <span data-ttu-id="ed86d-110">Seejärel saate kasutada kuluelemendi dimensiooni liikmete ühist kogumit, et analüüsida kahe juriidilise isiku kuluandmeid kuluarvestuse pearaamatus.</span><span class="sxs-lookup"><span data-stu-id="ed86d-110">You can then use the common set of cost element dimension members to analyze cost data from the two legal entities in a cost accounting ledger.</span></span>

| <span data-ttu-id="ed86d-111">Allikas: USA kontoplaan</span><span class="sxs-lookup"><span data-stu-id="ed86d-111">Source: US chart of accounts</span></span>                                          | <span data-ttu-id="ed86d-112">Allikas: Prantsuse kontoplaan</span><span class="sxs-lookup"><span data-stu-id="ed86d-112">Source: French chart of accounts</span></span>                                          | <span data-ttu-id="ed86d-113">Uus kuluelemendi dimensiooni liikmete ühine kogum</span><span class="sxs-lookup"><span data-stu-id="ed86d-113">New common set of cost element dimension members</span></span>                        |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="ed86d-114">Imporditud kuluelemendi dimensiooni liikmed USA kontoplaanilt</span><span class="sxs-lookup"><span data-stu-id="ed86d-114">Imported cost element dimension members from the US chart of accounts</span></span> | <span data-ttu-id="ed86d-115">Imporditud kuluelemendi dimensiooni liikmed Prantsuse kontoplaanilt</span><span class="sxs-lookup"><span data-stu-id="ed86d-115">Imported cost element dimension members from the French chart of accounts</span></span> | <span data-ttu-id="ed86d-116">USA ja Prantsuse kuluelemendi dimensiooni liikmete vastendamine ühisele kogumile</span><span class="sxs-lookup"><span data-stu-id="ed86d-116">Mapping of US and French cost element dimension members to a common set</span></span> |
| <span data-ttu-id="ed86d-117">5001: Müük</span><span class="sxs-lookup"><span data-stu-id="ed86d-117">5001: Sales</span></span>                                                           | <span data-ttu-id="ed86d-118">5001: Müük ja turundus</span><span class="sxs-lookup"><span data-stu-id="ed86d-118">5001: Sales and advertising</span></span>                                               | <span data-ttu-id="ed86d-119">5000: Müük ja turundus</span><span class="sxs-lookup"><span data-stu-id="ed86d-119">5000: Sales and advertising</span></span>                                             |
| <span data-ttu-id="ed86d-120">5030: Reklaam</span><span class="sxs-lookup"><span data-stu-id="ed86d-120">5030: Advertising</span></span>                                                     | <span data-ttu-id="ed86d-121">6390: Lao ost\*</span><span class="sxs-lookup"><span data-stu-id="ed86d-121">6390: Stock purchase\*</span></span>                                                    | <span data-ttu-id="ed86d-122">7000: Puhastuskulud</span><span class="sxs-lookup"><span data-stu-id="ed86d-122">7000: Cleaning expenses</span></span>                                                 |
| <span data-ttu-id="ed86d-123">7001: Puhastuskulud</span><span class="sxs-lookup"><span data-stu-id="ed86d-123">7001: Cleaning expenses</span></span>                                               | <span data-ttu-id="ed86d-124">7001: Reisikulu</span><span class="sxs-lookup"><span data-stu-id="ed86d-124">7001: Travel expense</span></span>                                                      | <span data-ttu-id="ed86d-125">7001: Reisikulud</span><span class="sxs-lookup"><span data-stu-id="ed86d-125">7001: Travel expenses</span></span>                                                   |

<span data-ttu-id="ed86d-126">\*Lao ostu Prantsuse kuluelemendi dimensiooni liiget ei vastendata.</span><span class="sxs-lookup"><span data-stu-id="ed86d-126">\*The Stock purchase French cost element dimension member isn't mapped.</span></span>

## <a name="currency-conversion"></a><span data-ttu-id="ed86d-127">Valuutateisendus</span><span class="sxs-lookup"><span data-stu-id="ed86d-127">Currency conversion</span></span>
<span data-ttu-id="ed86d-128">Erinevaid kasutatavaid kontoplaane saab seadistada kasutama erinevaid valuutasid.</span><span class="sxs-lookup"><span data-stu-id="ed86d-128">The various charts of accounts that you use might be set up to use different currencies.</span></span> <span data-ttu-id="ed86d-129">Sellisel juhul määrake kindlasti valuutateisendus, et kuluandmeid töödeldaks õiget valuutat kasutades, nagu on määratletud kuluarvestuse pearaamatus, kus kasutatakse kuluelemendi dimensiooni liikmeid.</span><span class="sxs-lookup"><span data-stu-id="ed86d-129">In this case, be sure to specify a currency conversion, so that cost data is processed by using the correct currency, as defined in the cost accounting ledger where the cost element dimension members are used.</span></span> <span data-ttu-id="ed86d-130">Kui eeltoodud näites kasutatakse kuluarvestuse pearaamatus USA dollareid, peate looma valuutateisenduse USA dollarist eurodele (EUR), et töödelda kandeid vastendatud kuluelemendi dimensiooni liikmete jaoks.</span><span class="sxs-lookup"><span data-stu-id="ed86d-130">In the preceding example, if US dollars (USD) are used in the cost accounting ledger, you must create a currency conversion from USD to euros (EUR) to process transactions for the mapped cost element dimension members.</span></span>

## <a name="update-mappings-at-any-time"></a><span data-ttu-id="ed86d-131">Vastenduste värskendamine mis tahes ajal</span><span class="sxs-lookup"><span data-stu-id="ed86d-131">Update mappings at any time</span></span>
<span data-ttu-id="ed86d-132">Kuluelemendi dimensiooni vastendamise määratlusi saate igal ajal värskendada.</span><span class="sxs-lookup"><span data-stu-id="ed86d-132">You can update the mapping definitions for a cost element dimension at any time.</span></span> <span data-ttu-id="ed86d-133">Kuna vastendused ei ole kehtivuskuupäevaga, rakendatakse muudatused järgmine kord, kui töötlete kulukandeid või käitate kuluarvestusi.</span><span class="sxs-lookup"><span data-stu-id="ed86d-133">Because mappings aren't date-effective, changes are applied the next time that you process cost transactions or run cost calculations.</span></span>




