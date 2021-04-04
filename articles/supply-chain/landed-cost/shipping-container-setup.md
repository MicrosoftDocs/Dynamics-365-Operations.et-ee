---
title: Saatmiskonteinerid
description: See teema kirjeldab, kuidas seadistada saatmiskonteinereid moodulis Väljalaadimiskulu.
author: sherry-zheng
manager: tfehr
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMContainerTypeTable, ITMContainerTable, ITMContainerUnitTypeTable, ITMRefrigerationTypeTable, ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: ca712aa7f07792861d5ba36afd8d7b63cc9ce8fb
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500954"
---
# <a name="shipping-container-setup"></a><span data-ttu-id="129af-103">Saatmiskonteineri seadistamine</span><span class="sxs-lookup"><span data-stu-id="129af-103">Shipping container setup</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="129af-104">See teema kirjeldab, kuidas seadistada saatmiskonteinereid moodulis **Väljalaadimiskulu**.</span><span class="sxs-lookup"><span data-stu-id="129af-104">This topic describes how to set up shipping containers for the **Landed cost** module.</span></span>

## <a name="set-up-shipping-container-types"></a><a id="shipping-container-types"></a><span data-ttu-id="129af-105">Saatmiskonteineritüüpide seadistamine</span><span class="sxs-lookup"><span data-stu-id="129af-105">Set up shipping container types</span></span>

<span data-ttu-id="129af-106">Saatmiskonteineritüübid määravad mis tüüpi konteinerid on saadaval tarnimisel ja teekondades kasutamiseks.</span><span class="sxs-lookup"><span data-stu-id="129af-106">Shipping container types define the types of shipping containers that are available for use during shipping and voyages.</span></span>

<span data-ttu-id="129af-107">Saatmiskonteineritüüpidega töötamiseks avage **Väljalaadimiskulu \> Konteinerite seadistus \> Saatmiskonteineritüübid**.</span><span class="sxs-lookup"><span data-stu-id="129af-107">To work with the shipping container types, go to **Landed cost \> Containers setup \> Shipping container types**.</span></span> <span data-ttu-id="129af-108">Seal saate konteineritüüpide kirjeid vaadata, lisada ja eemaldada.</span><span class="sxs-lookup"><span data-stu-id="129af-108">There, you can view, add, and remove records for your container types.</span></span> <span data-ttu-id="129af-109">Järgmises tabelis kirjeldatakse iga kirje jaoks saadaolevaid välju.</span><span class="sxs-lookup"><span data-stu-id="129af-109">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="129af-110">Field</span><span class="sxs-lookup"><span data-stu-id="129af-110">Field</span></span> | <span data-ttu-id="129af-111">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="129af-111">Description</span></span> |
|---|---|
| <span data-ttu-id="129af-112">Saatmiskonteineri tüüp</span><span class="sxs-lookup"><span data-stu-id="129af-112">Shipping container type</span></span> | <span data-ttu-id="129af-113">Sisestage saatmiskonteineritüübi ainu-ID nimi/number.</span><span class="sxs-lookup"><span data-stu-id="129af-113">Enter a unique identification name/number for the shipping container type.</span></span> |
| <span data-ttu-id="129af-114">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="129af-114">Description</span></span> | <span data-ttu-id="129af-115">Sisestage saatmiskonteineritüübi kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="129af-115">Enter a description of the shipping container type.</span></span> |
| <span data-ttu-id="129af-116">Maht</span><span class="sxs-lookup"><span data-stu-id="129af-116">Volume</span></span> | <span data-ttu-id="129af-117">Sisestage seda tüüpi saatmiskonteinerite lubatud maksimummaht.</span><span class="sxs-lookup"><span data-stu-id="129af-117">Enter the maximum volume that is allowed in shipping containers of this type.</span></span> |
| <span data-ttu-id="129af-118">Kaal</span><span class="sxs-lookup"><span data-stu-id="129af-118">Weight</span></span> | <span data-ttu-id="129af-119">Sisestage seda tüüpi saatmiskonteinerite lubatud maksimumkaal.</span><span class="sxs-lookup"><span data-stu-id="129af-119">Enter the maximum weight that is allowed in shipping containers of this type.</span></span> |
| <span data-ttu-id="129af-120">Tagastatav</span><span class="sxs-lookup"><span data-stu-id="129af-120">Returnable</span></span> | <span data-ttu-id="129af-121">Määrake, kas seda tüüpi saatmiskonteinerid saab pärast teekonnal kasutamist tagastada hankijale.</span><span class="sxs-lookup"><span data-stu-id="129af-121">Specify whether shipping containers of this type can be returned to the vendor after they are used during a voyage.</span></span> <span data-ttu-id="129af-122">Kui suvandi väärtuseks on seatud *Jah*, võivad seda tüüpi saatmiskonteinerite lähtesadamasse tagastamisele rakenduda lisakulud.</span><span class="sxs-lookup"><span data-stu-id="129af-122">If this option is set to *Yes*, additional costs might apply for the return of shipping containers of this type to the port of origin.</span></span> |

## <a name="set-up-shipping-containers"></a><span data-ttu-id="129af-123">Saatmiskonteinerite seadistamine</span><span class="sxs-lookup"><span data-stu-id="129af-123">Set up shipping containers</span></span>

<span data-ttu-id="129af-124">Kõigi teekondades kasutatud konteinerite tuvastamiseks kasutate saatmiskonteinerikirjeid.</span><span class="sxs-lookup"><span data-stu-id="129af-124">You use shipping container records to identify each container that you use during voyages.</span></span> <span data-ttu-id="129af-125">Teekonna loomisel saate selle jaoks valida kindla konteineri kõigi siin määratud saatmiskonteinerikirjete loendist.</span><span class="sxs-lookup"><span data-stu-id="129af-125">When you create a voyage, you can select a specific container for it in the list of all the shipping container records that you've defined here.</span></span> <span data-ttu-id="129af-126">See funktsioon on eriti kasulik juhul, kui ettevõttel on oma saatmiskonteinerid.</span><span class="sxs-lookup"><span data-stu-id="129af-126">This feature is especially useful if your company owns its own shipping containers.</span></span>

<span data-ttu-id="129af-127">Saatmiskonteinerinumbreid ei pea sisestada selliste saatmiskonteinerite jaoks, mida kasutatakse ainult üks kord.</span><span class="sxs-lookup"><span data-stu-id="129af-127">You don't have to enter shipping container numbers for shipping containers that will be used only one time.</span></span> <span data-ttu-id="129af-128">Selle asemel saate saatmiskonteineri numbri lisada teekonna loomisel.</span><span class="sxs-lookup"><span data-stu-id="129af-128">Instead, you can add the shipping container number when you create a voyage.</span></span>

<span data-ttu-id="129af-129">Saatmiskonteinerikirjeid kasutatakse ainult moodulis Väljalaadimiskulu.</span><span class="sxs-lookup"><span data-stu-id="129af-129">Shipping container records are used only in Landed cost.</span></span> <span data-ttu-id="129af-130">Need pole saadaval standardmoodulis **Transpordihaldus** (TMS).</span><span class="sxs-lookup"><span data-stu-id="129af-130">They aren't available in the standard **Transportation management** module (TMS).</span></span>

<span data-ttu-id="129af-131">Saatmiskonteineritega töötamiseks avage **Väljalaadimiskulu \> Konteinerite seadistus \> Saatmiskonteinerid**.</span><span class="sxs-lookup"><span data-stu-id="129af-131">To work with shipping containers, go to **Landed cost \> Containers setup \> Shipping containers**.</span></span> <span data-ttu-id="129af-132">Seal saate saatmiskonteinerite kirjeid vaadata, lisada ja eemaldada.</span><span class="sxs-lookup"><span data-stu-id="129af-132">There, you can view, add, and remove records your shipping containers.</span></span> <span data-ttu-id="129af-133">Järgmises tabelis kirjeldatakse iga kirje jaoks saadaolevaid välju.</span><span class="sxs-lookup"><span data-stu-id="129af-133">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="129af-134">Field</span><span class="sxs-lookup"><span data-stu-id="129af-134">Field</span></span> | <span data-ttu-id="129af-135">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="129af-135">Description</span></span> |
|---|---|
| <span data-ttu-id="129af-136">Saatmiskonteiner</span><span class="sxs-lookup"><span data-stu-id="129af-136">Shipping container</span></span> | <span data-ttu-id="129af-137">Sisestage saatmiskonteineri ainu-ID nimi/number.</span><span class="sxs-lookup"><span data-stu-id="129af-137">Enter a unique identification name/number for the shipping container.</span></span> |
| <span data-ttu-id="129af-138">Saatmiskonteineri tüüp</span><span class="sxs-lookup"><span data-stu-id="129af-138">Shipping container type</span></span> | <span data-ttu-id="129af-139">Valige saatmiskonteineri tüüp.</span><span class="sxs-lookup"><span data-stu-id="129af-139">Select the type of shipping container.</span></span> <span data-ttu-id="129af-140">Lisateavet leiate selle teema varasemast jaotisest [Saatmiskonteineritüüpide seadistamine](#shipping-container-types).</span><span class="sxs-lookup"><span data-stu-id="129af-140">For more information, see the [Set up shipping container types](#shipping-container-types) section earlier in this topic.</span></span> |

> [!NOTE]
> - <span data-ttu-id="129af-141">Saatmiskonteineri seadistamine on valikuline.</span><span class="sxs-lookup"><span data-stu-id="129af-141">The shipping container setup is optional.</span></span> <span data-ttu-id="129af-142">Tavaliselt kasutatakse seda ainult juhul, kui ettevõttel on oma saatmiskonteinerid või kui see kasutab sageli samu saatmiskonteinereid.</span><span class="sxs-lookup"><span data-stu-id="129af-142">Typically, you will use it only if your company owns its own shipping containers or often reuses the same shipping containers.</span></span>
> - <span data-ttu-id="129af-143">Saatmiskonteinerinumbrite jaoks ei arvutata kontrollnumbreid.</span><span class="sxs-lookup"><span data-stu-id="129af-143">No check digits are calculated for shipping container numbers.</span></span>

## <a name="set-up-unit-types"></a><a name="unit-types"></a><span data-ttu-id="129af-144">Ühikutüüpide seadistamine</span><span class="sxs-lookup"><span data-stu-id="129af-144">Set up unit types</span></span>

<span data-ttu-id="129af-145">Ühikutüübid määravad saatmiskonteinerite jaoks täiendavad rühmitus- ja tuvastusmeetodid.</span><span class="sxs-lookup"><span data-stu-id="129af-145">Unit types establish additional groupings and identification methods for shipping containers.</span></span> <span data-ttu-id="129af-146">Ühikutüüpi kasutatakse tavaliselt selleks, et tuvastada kaupu sisaldava konteineri tüüp, näiteks kaubaalused või vaadid.</span><span class="sxs-lookup"><span data-stu-id="129af-146">The unit type is typically used to identify the type of container that goods are packaged in, such as pallets or drums.</span></span> <span data-ttu-id="129af-147">Ühikutüübi saate valida, kui seadistate konteineri lehel **Kõik saatmiskonteinerid**.</span><span class="sxs-lookup"><span data-stu-id="129af-147">You can select a unit type when you set up a container on the **All shipping containers** page.</span></span>

<span data-ttu-id="129af-148">Ühikutüüpe kasutatakse ainult moodulis Väljalaadimiskulu.</span><span class="sxs-lookup"><span data-stu-id="129af-148">Unit types are used only in Landed cost.</span></span> <span data-ttu-id="129af-149">Need ei ole saadaval TMS-is.</span><span class="sxs-lookup"><span data-stu-id="129af-149">They aren't available in TMS.</span></span>

<span data-ttu-id="129af-150">Ühikutüüpidega töötamiseks avage **Väljalaadimiskulu \> Konteinerite seadistus \> Ühikutüübid**.</span><span class="sxs-lookup"><span data-stu-id="129af-150">To work with unit types, go to **Landed cost \> Containers setup \> Unit types**.</span></span> <span data-ttu-id="129af-151">Seal saate ühikutüüpide kirjeid vaadata, lisada ja eemaldada.</span><span class="sxs-lookup"><span data-stu-id="129af-151">There, you can view, add, and remove records for your unit types.</span></span> <span data-ttu-id="129af-152">Järgmises tabelis kirjeldatakse iga kirje jaoks saadaolevaid välju.</span><span class="sxs-lookup"><span data-stu-id="129af-152">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="129af-153">Field</span><span class="sxs-lookup"><span data-stu-id="129af-153">Field</span></span> | <span data-ttu-id="129af-154">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="129af-154">Description</span></span> |
|---|---|
| <span data-ttu-id="129af-155">Ühiku tüüp</span><span class="sxs-lookup"><span data-stu-id="129af-155">Unit type</span></span> | <span data-ttu-id="129af-156">Sisestage ühikutüübi ainu-ID nimi/number.</span><span class="sxs-lookup"><span data-stu-id="129af-156">Enter a unique identification name/number for the unit type.</span></span> |
| <span data-ttu-id="129af-157">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="129af-157">Description</span></span> | <span data-ttu-id="129af-158">Sisestage ühikutüübi kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="129af-158">Enter a description of the unit type.</span></span> |

## <a name="set-up-refrigeration-types"></a><a name="refrigeration-types"></a><span data-ttu-id="129af-159">Külmutuse tüüpide seadistamine</span><span class="sxs-lookup"><span data-stu-id="129af-159">Set up refrigeration types</span></span>

<span data-ttu-id="129af-160">Külmutuse tüübid määravad saatmiskonteinerite (tavaliselt külmkonteinerite) jaoks täiendavad rühmitus- ja tuvastusmeetodid.</span><span class="sxs-lookup"><span data-stu-id="129af-160">Refrigeration types establish additional groupings and identification methods for shipping containers (usually refrigerated containers).</span></span> <span data-ttu-id="129af-161">Külmutuse tüübi saate valida, kui seadistate konteineri lehel **Kõik saatmiskonteinerid**.</span><span class="sxs-lookup"><span data-stu-id="129af-161">You can select a refrigeration type when you set up a container on the **All shipping containers** page.</span></span>

<span data-ttu-id="129af-162">Külmutuse tüüpidega töötamiseks avage **Väljalaadimiskulu \> Konteinerite seadistus \> Külmutuse tüübid**.</span><span class="sxs-lookup"><span data-stu-id="129af-162">To work with refrigeration types, go to **Landed cost \> Containers setup \> Refrigeration types**.</span></span> <span data-ttu-id="129af-163">Seal saate külmutuse tüüpide kirjeid vaadata, lisada ja eemaldada.</span><span class="sxs-lookup"><span data-stu-id="129af-163">There, you can view, add, and remove records for your refrigeration types.</span></span> <span data-ttu-id="129af-164">Järgmises tabelis kirjeldatakse iga kirje jaoks saadaolevaid välju.</span><span class="sxs-lookup"><span data-stu-id="129af-164">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="129af-165">Field</span><span class="sxs-lookup"><span data-stu-id="129af-165">Field</span></span> | <span data-ttu-id="129af-166">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="129af-166">Description</span></span> |
|---|---|
| <span data-ttu-id="129af-167">Külmutuse tüüp</span><span class="sxs-lookup"><span data-stu-id="129af-167">Refrigeration type</span></span> | <span data-ttu-id="129af-168">Sisestage külmutuse tüübi ainu-ID nimi/number.</span><span class="sxs-lookup"><span data-stu-id="129af-168">Enter a unique identification name/number for the refrigeration type.</span></span> |
| <span data-ttu-id="129af-169">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="129af-169">Description</span></span> | <span data-ttu-id="129af-170">Sisestage külmutuse tüübi kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="129af-170">Enter a description of the refrigeration type.</span></span> |
