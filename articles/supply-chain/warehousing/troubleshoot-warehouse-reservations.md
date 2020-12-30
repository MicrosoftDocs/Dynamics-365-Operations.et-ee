---
title: Broneeringute tõrkeotsing laohalduses
description: Selles teemas kirjeldatakse, kuidas lahendada lao broneerimistega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 6151797001b1ccdb7e371c70b90c304a5ab422d8
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645115"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a><span data-ttu-id="b5b75-103">Broneeringute tõrkeotsing laohalduses</span><span class="sxs-lookup"><span data-stu-id="b5b75-103">Troubleshoot reservations in warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b5b75-104">Selles teemas kirjeldatakse, kuidas lahendada lao broneerimistega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.</span><span class="sxs-lookup"><span data-stu-id="b5b75-104">This topic describes how to fix common issues that you might encounter while you work with warehouse reservations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a><span data-ttu-id="b5b75-105">Kuvatakse järgnev tõrge „Broneeringuid ei saa eemaldada, kuna loodud on töö, mis sõltub nendest broneeringutest”.</span><span class="sxs-lookup"><span data-stu-id="b5b75-105">I receive the following error message: "Reservations cannot be removed because there is work created which relies on the reservations."</span></span>

### <a name="issue-description"></a><span data-ttu-id="b5b75-106">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="b5b75-106">Issue description</span></span>

<span data-ttu-id="b5b75-107">Te ei saa varude broneerimist müügirealt maha võtta, kuna rea suhtes on avatud töö.</span><span class="sxs-lookup"><span data-stu-id="b5b75-107">You can't unreserve inventory on a sales line, because there is open work against the line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b5b75-108">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="b5b75-108">Issue resolution</span></span>

<span data-ttu-id="b5b75-109">Uurige, kas avatud pakkimisgrupi töö on olemas, et tuua kaup pakkimisühiku teise asukohta (nt *Uks*).</span><span class="sxs-lookup"><span data-stu-id="b5b75-109">Investigate whether open packing group work exists to bring the item from a packing station to another location (such as *Baydoor*).</span></span> <span data-ttu-id="b5b75-110">Vaadake üle kirjed **Töö loomise ajaloo logi** ja **Töö üksikasjade** lehtedel, et teha kindlaks, mis kaupa füüsiliselt broneerib, ja seejärel lõpetage või kustutage töö, et broneeringut vabastada.</span><span class="sxs-lookup"><span data-stu-id="b5b75-110">Review the records on the **Work creation history log** and **Work details** pages to determine what is physically reserving the inventory, and then complete or delete the work to free up the reservation.</span></span>

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a><span data-ttu-id="b5b75-111">Kuvatakse järgmine tõrketeade: "Varude kogust -%1 ei saanud uuendada kauba %2 ebapiisavate kaubavaru kannete tõttu."</span><span class="sxs-lookup"><span data-stu-id="b5b75-111">I receive the following error message: "Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2...."</span></span>

### <a name="issue-description"></a><span data-ttu-id="b5b75-112">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="b5b75-112">Issue description</span></span>

<span data-ttu-id="b5b75-113">See probleem võib ilmneda juhul, kui süsteem ei saa varude kogust värskendada, kuna pole piisavalt laokandeid, millel on määratud dimensioone.</span><span class="sxs-lookup"><span data-stu-id="b5b75-113">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="b5b75-114">Siin on täieliku tõrketeate täistekst:</span><span class="sxs-lookup"><span data-stu-id="b5b75-114">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="b5b75-115">Varude kogust -%1 ei saanud värskendada, kuna pole piisavalt laokandeid kaubaga %2, mille dimensioonid on suurus =%3, värvus =%4, täiendused =%5, sait =%6, ladu =%7, asukoht =%8, varude olek = saadaval, identifitseerimisnumber =%9, partii number =%10 ID-kood %11 saatepartii ID %12.</span><span class="sxs-lookup"><span data-stu-id="b5b75-115">Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2 with dimensions Size=%3, Color=%4, Additions=%5, Site=%6, Warehouse=%7, Location=%8, Inventory status=Available, License plate=%9, Batch number=%10 for reference ID %11 on Lot ID %12.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b5b75-116">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="b5b75-116">Issue resolution</span></span>

<span data-ttu-id="b5b75-117">Veenduge, et varude kanded ei broneeriks kauba kogust füüsiliselt.</span><span class="sxs-lookup"><span data-stu-id="b5b75-117">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="b5b75-118">Näiteks võivad need kanded avada kvaliteetseid tellimusi, lao blokeerimise kirjeid või väljaminekuordereid.</span><span class="sxs-lookup"><span data-stu-id="b5b75-118">For example, these transactions might open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a><span data-ttu-id="b5b75-119">Kuvatakse järgmine tõrketeade: "Füüsilist laoseisu... ei saa broneerida, kuna laos on saadaval ainult 0,00."</span><span class="sxs-lookup"><span data-stu-id="b5b75-119">I receive the following error message: "Physical on-hand...cannot be reserved because only 0.00 are available in the inventory."</span></span>

### <a name="issue-description"></a><span data-ttu-id="b5b75-120">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="b5b75-120">Issue description</span></span>

<span data-ttu-id="b5b75-121">See probleem võib ilmneda juhul, kui süsteem ei saa varude kogust värskendada, kuna pole piisavalt laokandeid, millel on määratud dimensioone.</span><span class="sxs-lookup"><span data-stu-id="b5b75-121">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="b5b75-122">Siin on täieliku tõrketeate täistekst:</span><span class="sxs-lookup"><span data-stu-id="b5b75-122">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="b5b75-123">Füüsiline vaba kaubavaru sait=%1, ladu=%2, varude olek=saadaval, partii number=%3, omanik=%4: %5 ei saa broneerida, kuna laos on saadaval ainult 0,00.</span><span class="sxs-lookup"><span data-stu-id="b5b75-123">Physical on-hand Site=%1, Warehouse=%2, Inventory status=Available, Batch number=%3, Owner=%4: %5 cannot be reserved because only 0.00 are available in the inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b5b75-124">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="b5b75-124">Issue resolution</span></span>

<span data-ttu-id="b5b75-125">See probleem on tõenäoliselt põhjustatud avatud tööst.</span><span class="sxs-lookup"><span data-stu-id="b5b75-125">This issue is probably caused by open work.</span></span> <span data-ttu-id="b5b75-126">Lõpetage töö või võtke vastu ilma töö loomiseta.</span><span class="sxs-lookup"><span data-stu-id="b5b75-126">Either complete the work or receive without work creation.</span></span> <span data-ttu-id="b5b75-127">Veenduge, et varude kanded ei broneeriks kauba kogust füüsiliselt.</span><span class="sxs-lookup"><span data-stu-id="b5b75-127">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="b5b75-128">Näiteks võivad need kanded olla avatud kvaliteetsed tellimused, lao blokeerimise kirjed või väljamineku tellimused.</span><span class="sxs-lookup"><span data-stu-id="b5b75-128">For example, these transactions might be open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a><span data-ttu-id="b5b75-129">Kuvatakse järgmine tõrketeade: "Kui soovite määrata voo, peavad koorma read määrama dimensioonid asukoha kohal.</span><span class="sxs-lookup"><span data-stu-id="b5b75-129">I receive the following error message: "To be assigned to wave, load lines must specify the dimensions above the location.</span></span> <span data-ttu-id="b5b75-130">Nende dimensioonide määramiseks broneerige ja looge uuesti koorma rida."</span><span class="sxs-lookup"><span data-stu-id="b5b75-130">To assign these dimensions, reserve and recreate the load line."</span></span>

### <a name="issue-description"></a><span data-ttu-id="b5b75-131">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="b5b75-131">Issue description</span></span>

<span data-ttu-id="b5b75-132">Kui kasutate kaupa, millel on "partii eespool" broneerimise hierarhia (mille **partiinumbri** dimensioon on paigutatud *enne* **Asukoha** dimensiooni), ei tööta osalise koguse jaoks **Väljasta lattu** käsklus **Koorma plaanimise töölaua** lehel.</span><span class="sxs-lookup"><span data-stu-id="b5b75-132">When you use an item that has a "batch above" reservation hierarchy (with the **Batch number** dimension placed *above* the **Location** dimension), the **Release to warehouse** command on the **Load planning workbench** page for a partial quantity doesn't work.</span></span> <span data-ttu-id="b5b75-133">Te saate selle tõrketeate ja ükski töö ei ole loodud osalise koguse jaoks.</span><span class="sxs-lookup"><span data-stu-id="b5b75-133">You receive this error message, and no work is created for the partial quantity.</span></span>

<span data-ttu-id="b5b75-134">Kui aga kasutate kaupa, millel on "partii allpool" broneerimise hierarhia (mille **partiinumbri** dimensioon on paigutatud *allapoole* **Asukoha** dimensiooni), saate väljastada osalise koguse **Koorma plaanimise töölaua** lehel.</span><span class="sxs-lookup"><span data-stu-id="b5b75-134">However, if you use an item that has a "batch below" reservation hierarchy (with the **Batch number** dimension placed *below* the **Location** dimension), you can release a load from the **Load planning workbench** page for a partial quantity.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="b5b75-135">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="b5b75-135">Issue resolution</span></span>

<span data-ttu-id="b5b75-136">Selline käitumine on nii kavandatud.</span><span class="sxs-lookup"><span data-stu-id="b5b75-136">This behavior is by design.</span></span> <span data-ttu-id="b5b75-137">Kui asetate broneerimise hierarhias dimensiooni **Asukoha** dimensioonist ettepoole, peab see olema määratud enne lattu väljastamist.</span><span class="sxs-lookup"><span data-stu-id="b5b75-137">If you put a dimension above the **Location** dimension in the reservation hierarchy, it must be specified before the release to the warehouse.</span></span> <span data-ttu-id="b5b75-138">Microsoft on seda probleemi hinnanud ja on määranud, et see on funktsiooni piirang koorma planeerimise töölaualt lattu väljastamise ajal.</span><span class="sxs-lookup"><span data-stu-id="b5b75-138">Microsoft has evaluated this issue and has determined that it's a feature limitation during releases to the warehouse from the load planning workbench.</span></span> <span data-ttu-id="b5b75-139">Osalisi koguseid ei saa väljastada, kui ühe või mitme dimensiooni **Asukoht** on määramata.</span><span class="sxs-lookup"><span data-stu-id="b5b75-139">Partial quantities can't be released if one or more dimensions above **Location** aren't specified.</span></span>

<span data-ttu-id="b5b75-140">Lisateavet vt [Paindlik dimensiooni broneerimise poliitika laotasemel](flexible-warehouse-level-dimension-reservation.md).</span><span class="sxs-lookup"><span data-stu-id="b5b75-140">For more information, see [Flexible warehouse-level dimension reservation policy](flexible-warehouse-level-dimension-reservation.md).</span></span>
