---
title: Kuluelemendi dimensiooniliikmete vastendamine dimensiooniliikmete ühtse mudeliga
description: Erinevate kuluelemendi dimensiooni liikmete vastendamisega kuluelemendi dimensiooni liikmete ühisele kogumile ühendate andmed analüüsi otstarbel ühisesse vormingusse.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMDimensionMember, CAMDimensionMapping
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 223234
ms.assetid: 4c66a231-aed2-48b5-9727-b3eb4fe6e6aa
ms.search.region: global
ms.author: roschlom
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: c6a9618a762d3af840beb05d86518b3588118e80
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4442282"
---
# <a name="map-cost-element-dimension-members-to-a-common-set-of-dimension-members"></a><span data-ttu-id="6ffbb-103">Kuluelemendi dimensiooniliikmete vastendamine dimensiooniliikmete ühtse mudeliga</span><span class="sxs-lookup"><span data-stu-id="6ffbb-103">Map cost element dimension members to a common set of dimension members</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6ffbb-104">Erinevate kuluelemendi dimensiooni liikmete vastendamisega kuluelemendi dimensiooni liikmete ühisele kogumile ühendate andmed analüüsi otstarbel ühisesse vormingusse.</span><span class="sxs-lookup"><span data-stu-id="6ffbb-104">By mapping different cost element dimension members to a common set of cost element dimension members, you merge data into a common format for analysis purposes.</span></span>

<span data-ttu-id="6ffbb-105">Kui olete globaalne ettevõtte ja järgite seadusjärgseid raamatupidamisnõudeid, võite kasutada mitut kontoplaani.</span><span class="sxs-lookup"><span data-stu-id="6ffbb-105">If you're a global company and comply with statutory accounting requirements, you might use multiple charts of accounts.</span></span> <span data-ttu-id="6ffbb-106">Kuluelemendi dimensiooni liikmete importimisel erinevatest kontoplaanidest saate lõpuks kontode segu.</span><span class="sxs-lookup"><span data-stu-id="6ffbb-106">When you import cost element dimension members from different charts of accounts, you can end up with a mix of accounts.</span></span> <span data-ttu-id="6ffbb-107">Siiski võib nendel kontodel tegelikult olla sama struktuur ja võite soovi korral analüüsida ja eraldada kulud neile, kasutades ühist vormingut.</span><span class="sxs-lookup"><span data-stu-id="6ffbb-107">However, these accounts might actually have the same nature, and you might want to analyze and allocate costs for them by using a common format.</span></span>

## <a name="map-cost-element-dimension-members-to-a-common-format"></a><span data-ttu-id="6ffbb-108">Kuluelemendi dimensiooni liikmete vastendamine ühisele vormingule</span><span class="sxs-lookup"><span data-stu-id="6ffbb-108">Map cost element dimension members to a common format</span></span>
<span data-ttu-id="6ffbb-109">Järgmine näide näitab teile, kuidas teie kulukontrollerina saate luua kuluarvestuses uue kuluelemendi dimensiooni, mis vastendab kuluelemendi dimensiooni liikmed USA ja Prantsuse kontoplaani struktuurist kuluelemendi dimensiooni liikmete ühisele kogumile.</span><span class="sxs-lookup"><span data-stu-id="6ffbb-109">The following example shows how you, as a cost controller, can create a new cost element dimension in Cost accounting that maps cost element dimension members from the US chart of accounts structure and the French chart of accounts structure to a common set of cost element dimension members.</span></span> <span data-ttu-id="6ffbb-110">Seejärel saate kasutada kuluelemendi dimensiooni liikmete ühist kogumit, et analüüsida kahe juriidilise isiku kuluandmeid kuluarvestuse pearaamatus.</span><span class="sxs-lookup"><span data-stu-id="6ffbb-110">You can then use the common set of cost element dimension members to analyze cost data from the two legal entities in a cost accounting ledger.</span></span>

| <span data-ttu-id="6ffbb-111">Allikas: USA kontoplaan</span><span class="sxs-lookup"><span data-stu-id="6ffbb-111">Source: US chart of accounts</span></span>                                          | <span data-ttu-id="6ffbb-112">Allikas: Prantsuse kontoplaan</span><span class="sxs-lookup"><span data-stu-id="6ffbb-112">Source: French chart of accounts</span></span>                                          | <span data-ttu-id="6ffbb-113">Uus kuluelemendi dimensiooni liikmete ühine kogum</span><span class="sxs-lookup"><span data-stu-id="6ffbb-113">New common set of cost element dimension members</span></span>                        |
|-----------------------------------------------------------------------|---------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span data-ttu-id="6ffbb-114">Imporditud kuluelemendi dimensiooni liikmed USA kontoplaanilt</span><span class="sxs-lookup"><span data-stu-id="6ffbb-114">Imported cost element dimension members from the US chart of accounts</span></span> | <span data-ttu-id="6ffbb-115">Imporditud kuluelemendi dimensiooni liikmed Prantsuse kontoplaanilt</span><span class="sxs-lookup"><span data-stu-id="6ffbb-115">Imported cost element dimension members from the French chart of accounts</span></span> | <span data-ttu-id="6ffbb-116">USA ja Prantsuse kuluelemendi dimensiooni liikmete vastendamine ühisele kogumile</span><span class="sxs-lookup"><span data-stu-id="6ffbb-116">Mapping of US and French cost element dimension members to a common set</span></span> |
| <span data-ttu-id="6ffbb-117">5001: Müük</span><span class="sxs-lookup"><span data-stu-id="6ffbb-117">5001: Sales</span></span>                                                           | <span data-ttu-id="6ffbb-118">5001: Müük ja turundus</span><span class="sxs-lookup"><span data-stu-id="6ffbb-118">5001: Sales and advertising</span></span>                                               | <span data-ttu-id="6ffbb-119">5000: Müük ja turundus</span><span class="sxs-lookup"><span data-stu-id="6ffbb-119">5000: Sales and advertising</span></span>                                             |
| <span data-ttu-id="6ffbb-120">5030: Reklaam</span><span class="sxs-lookup"><span data-stu-id="6ffbb-120">5030: Advertising</span></span>                                                     | <span data-ttu-id="6ffbb-121">6390: Lao ost\*</span><span class="sxs-lookup"><span data-stu-id="6ffbb-121">6390: Stock purchase\*</span></span>                                                    | <span data-ttu-id="6ffbb-122">7000: Puhastuskulud</span><span class="sxs-lookup"><span data-stu-id="6ffbb-122">7000: Cleaning expenses</span></span>                                                 |
| <span data-ttu-id="6ffbb-123">7001: Puhastuskulud</span><span class="sxs-lookup"><span data-stu-id="6ffbb-123">7001: Cleaning expenses</span></span>                                               | <span data-ttu-id="6ffbb-124">7001: Reisikulu</span><span class="sxs-lookup"><span data-stu-id="6ffbb-124">7001: Travel expense</span></span>                                                      | <span data-ttu-id="6ffbb-125">7001: Reisikulud</span><span class="sxs-lookup"><span data-stu-id="6ffbb-125">7001: Travel expenses</span></span>                                                   |

<span data-ttu-id="6ffbb-126">\*Lao ostu Prantsuse kuluelemendi dimensiooni liiget ei vastendata.</span><span class="sxs-lookup"><span data-stu-id="6ffbb-126">\*The Stock purchase French cost element dimension member isn't mapped.</span></span>

## <a name="currency-conversion"></a><span data-ttu-id="6ffbb-127">Valuutateisendus</span><span class="sxs-lookup"><span data-stu-id="6ffbb-127">Currency conversion</span></span>
<span data-ttu-id="6ffbb-128">Erinevaid kasutatavaid kontoplaane saab seadistada kasutama erinevaid valuutasid.</span><span class="sxs-lookup"><span data-stu-id="6ffbb-128">The various charts of accounts that you use might be set up to use different currencies.</span></span> <span data-ttu-id="6ffbb-129">Sellisel juhul määrake kindlasti valuutateisendus, et kuluandmeid töödeldaks õiget valuutat kasutades, nagu on määratletud kuluarvestuse pearaamatus, kus kasutatakse kuluelemendi dimensiooni liikmeid.</span><span class="sxs-lookup"><span data-stu-id="6ffbb-129">In this case, be sure to specify a currency conversion, so that cost data is processed by using the correct currency, as defined in the cost accounting ledger where the cost element dimension members are used.</span></span> <span data-ttu-id="6ffbb-130">Kui eeltoodud näites kasutatakse kuluarvestuse pearaamatus USA dollareid, peate looma valuutateisenduse USA dollarist eurodele (EUR), et töödelda kandeid vastendatud kuluelemendi dimensiooni liikmete jaoks.</span><span class="sxs-lookup"><span data-stu-id="6ffbb-130">In the preceding example, if US dollars (USD) are used in the cost accounting ledger, you must create a currency conversion from USD to euros (EUR) to process transactions for the mapped cost element dimension members.</span></span>

## <a name="update-mappings-at-any-time"></a><span data-ttu-id="6ffbb-131">Vastenduste värskendamine mis tahes ajal</span><span class="sxs-lookup"><span data-stu-id="6ffbb-131">Update mappings at any time</span></span>
<span data-ttu-id="6ffbb-132">Kuluelemendi dimensiooni vastendamise määratlusi saate igal ajal värskendada.</span><span class="sxs-lookup"><span data-stu-id="6ffbb-132">You can update the mapping definitions for a cost element dimension at any time.</span></span> <span data-ttu-id="6ffbb-133">Kuna vastendused ei ole kehtivuskuupäevaga, rakendatakse muudatused järgmine kord, kui töötlete kulukandeid või käitate kuluarvestusi.</span><span class="sxs-lookup"><span data-stu-id="6ffbb-133">Because mappings aren't date-effective, changes are applied the next time that you process cost transactions or run cost calculations.</span></span>



