---
title: Lao asukohad
description: Lao asukohti kasutatakse üldise ladustamisega (WMS I) määramiseks, kus kaubad on WMS I laos ladustatud ja kust need seal komplekteeritakse.
author: perlynne
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WMSLocation, WMSBlockingCause, WHSLocation
audience: Application User
ms.reviewer: kamaybac
ms.custom: 2134
ms.assetid: 69bf6922-4151-447f-b678-4ba95637f54c
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 31096aa9c97f0307c7004d1af1e424dde1dc65cd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5264062"
---
# <a name="inventory-locations"></a><span data-ttu-id="5b5ac-103">Lao asukohad</span><span class="sxs-lookup"><span data-stu-id="5b5ac-103">Inventory locations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5b5ac-104">Lao asukohti kasutatakse üldise ladustamisega (WMS I) määramiseks, kus kaubad on WMS I laos ladustatud ja kust need seal komplekteeritakse.</span><span class="sxs-lookup"><span data-stu-id="5b5ac-104">Inventory locations are used with basic warehousing (WMS I) to determine where items are stored and where items are picked from in a WMS I warehouse.</span></span>

<span data-ttu-id="5b5ac-105">See teema kehtib mooduli Varude haldus funktsioonide puhul.</span><span class="sxs-lookup"><span data-stu-id="5b5ac-105">This topic applies to features in the Inventory management module.</span></span> <span data-ttu-id="5b5ac-106">See ei kehti mooduli Laohaldus funktsioonidele.</span><span class="sxs-lookup"><span data-stu-id="5b5ac-106">It does not apply to features in the Warehouse management module.</span></span>

<span data-ttu-id="5b5ac-107">Mõiste asukoht viitab kohale, kus kaupu hoiundatakse ja kust võetakse.</span><span class="sxs-lookup"><span data-stu-id="5b5ac-107">The term location refers to the place that items are stored and drawn from.</span></span>

<span data-ttu-id="5b5ac-108">Iga asukoha puhul tuleb määrata ka koht, kuhu kaup paigutatakse.</span><span class="sxs-lookup"><span data-stu-id="5b5ac-108">For each location, the place where the item is inserted can also be specified.</span></span> <span data-ttu-id="5b5ac-109">Vaikimisi on need samad.</span><span class="sxs-lookup"><span data-stu-id="5b5ac-109">By default, they are the same.</span></span> <span data-ttu-id="5b5ac-110">Tavaliselt paigutatakse ja luuakse kaubad asukoha samalt küljelt, kuid see pole alati nii.</span><span class="sxs-lookup"><span data-stu-id="5b5ac-110">Items are usually inserted and drawn from the same side of a location, but not always.</span></span> <span data-ttu-id="5b5ac-111">Näiteks need kaubad, mis on ladustatud aktiivses laoriiulis, sisestatakse ühele riiulireale, kuid tuuakse teiselt.</span><span class="sxs-lookup"><span data-stu-id="5b5ac-111">For example, items that are stored in live storage racks are inserted from one aisle and drawn from another.</span></span> <span data-ttu-id="5b5ac-112">Põhisisend antakse asukoha nime järgi, mis määratletakse tavaliselt selle koordinaatidega: laud, riiulirida, sektsioon, riiul ja koht.</span><span class="sxs-lookup"><span data-stu-id="5b5ac-112">The main input is given by a location name, which is usually determined by its coordinates: warehouse, aisle, rack, shelf, and bin.</span></span> <span data-ttu-id="5b5ac-113">Selle nime või ID saab lehel Lao asukoht sisestada käsitsi või luua asukoha koordinaatide põhjal: näiteks 01-02-03-4, kui riiulirida on 1, sektsioon 2, riiul 3, koht 4.</span><span class="sxs-lookup"><span data-stu-id="5b5ac-113">This name or ID can be entered manually or generated from the location coordinates—for example, 01-02-03-4 for aisle 1, rack 2, shelf 3, bin 4 in the Inventory locations page.</span></span>
<span data-ttu-id="5b5ac-114">Asukoha atribuudid</span><span class="sxs-lookup"><span data-stu-id="5b5ac-114">Location properties</span></span>

<span data-ttu-id="5b5ac-115">Asukohal on järgmised tunnused:</span><span class="sxs-lookup"><span data-stu-id="5b5ac-115">A location has the following characteristics:</span></span>
-   <span data-ttu-id="5b5ac-116">Suurus (kõrgus, laius ja sügavus ja sellest tulenevalt maht)</span><span class="sxs-lookup"><span data-stu-id="5b5ac-116">Size (height, width, depth, and thereby volume)</span></span>
-   <span data-ttu-id="5b5ac-117">Ladu, riiulirida, sektsioon, riiul ja koht.</span><span class="sxs-lookup"><span data-stu-id="5b5ac-117">Warehouse, aisle, rack, shelf, and bin position</span></span>
-   <span data-ttu-id="5b5ac-118">Asukoha tüüp (hulgiasukoht, komplekteerimise asukoht, saabumisala, väljastusala, tootmissisendi asukoht, kontrolliasukoht või kanbani lõppladu)</span><span class="sxs-lookup"><span data-stu-id="5b5ac-118">Location type (bulk location, picking location, inbound dock, outbound dock, production input location, inspection location, or kanban supermarket)</span></span>

<span data-ttu-id="5b5ac-119">Selleks et kontrollida, kas operaator on valinud konkreetse kauba jaoks õige asukoha, saab võrgusüsteemides kasutada kontrollteksti.</span><span class="sxs-lookup"><span data-stu-id="5b5ac-119">Check text can be used in online systems to verify that the operator has selected the correct location for a specific item.</span></span> <span data-ttu-id="5b5ac-120">Kontrollteksti võib luua kas käsitsi või valida vaikimisi.</span><span class="sxs-lookup"><span data-stu-id="5b5ac-120">This check text can be created manually or by default.</span></span>

## <a name="sort-codes"></a><span data-ttu-id="5b5ac-121">Sortimiskoodid</span><span class="sxs-lookup"><span data-stu-id="5b5ac-121">Sort codes</span></span>
<span data-ttu-id="5b5ac-122">Sortimiskoode kasutatakse varudest kaupade komplekteerimiseks vajalikku teavet (sh komplekteerimisjärjekord) kirjeldavate komplekteerimisridade töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="5b5ac-122">Use sort codes to optimize the handling of picking lines, which describe the information that is required for picking items from inventory, including the picking order.</span></span> <span data-ttu-id="5b5ac-123">Sortimiskoode saab määrata riiuliridade ja muude koordinaatide aluse või määrata asukohale käsitsi.</span><span class="sxs-lookup"><span data-stu-id="5b5ac-123">Sort codes can be specified by the aisle and other coordinates, or assigned manually for the location.</span></span>

## <a name="blocked-locations"></a><span data-ttu-id="5b5ac-124">Blokeeritud asukohad</span><span class="sxs-lookup"><span data-stu-id="5b5ac-124">Blocked locations</span></span>
<span data-ttu-id="5b5ac-125">Mõnikord on vaja näidata, et asukoht on teatud ajaks blokeeritud, näiteks paranduste võimaldamiseks.</span><span class="sxs-lookup"><span data-stu-id="5b5ac-125">Occasionally, you might want to indicate that a location is blocked for a period of time, for example, to allow for repairs.</span></span> <span data-ttu-id="5b5ac-126">Mõnikord aga on vaja näidata ainult sissetuleku või väljamineku blokeerimist.</span><span class="sxs-lookup"><span data-stu-id="5b5ac-126">At other times, you may want to indicate blocking of only the input or only output.</span></span>

## <a name="tree-structure"></a><span data-ttu-id="5b5ac-127">Puu struktuur</span><span class="sxs-lookup"><span data-stu-id="5b5ac-127">Tree structure</span></span>

<span data-ttu-id="5b5ac-128">Lehel Lao asukohad saate vaadata lao paigutust puustruktuuril, tuginedes lao asukohtade koordinaatidele määratud kuvavormingus.</span><span class="sxs-lookup"><span data-stu-id="5b5ac-128">In the Inventory locations page, you can view the warehouse layout in a tree structure based on the coordinates of inventory locations, in a defined display format.</span></span>

## <a name="maintain-inventory-locations-via-the-warehouse-form"></a><span data-ttu-id="5b5ac-129">Lao asukohtade haldamine lao vormi kaudu</span><span class="sxs-lookup"><span data-stu-id="5b5ac-129">Maintain inventory locations via the warehouse form</span></span>

<span data-ttu-id="5b5ac-130">Asukohad saab kopeerida ühest laost teise ja asukohti luua viisardi abil.</span><span class="sxs-lookup"><span data-stu-id="5b5ac-130">It is possible to copy locations from one warehouse to another and to create locations via a wizard.</span></span> <span data-ttu-id="5b5ac-131">Enne viisardi käivitamist veenduge, et oleksite määratlenud lehel Ladu vaikeasukohtade nimed.</span><span class="sxs-lookup"><span data-stu-id="5b5ac-131">Before you run the wizard you should make sure that you have defined the default location names on the Warehouse page.</span></span>



<a name="additional-resources"></a><span data-ttu-id="5b5ac-132">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="5b5ac-132">Additional resources</span></span>
--------

[<span data-ttu-id="5b5ac-133">Uue laopaigutuse loomine</span><span class="sxs-lookup"><span data-stu-id="5b5ac-133">Create a new warehouse layout</span></span>](tasks/create-new-warehouse-layout.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]