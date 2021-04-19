---
title: Broneeringute tõrkeotsing laohalduses
description: Selles teemas kirjeldatakse, kuidas lahendada lao broneerimistega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d0d73396772ed9e8397797d6685fb550d911303b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828102"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a><span data-ttu-id="f2c1f-103">Broneeringute tõrkeotsing laohalduses</span><span class="sxs-lookup"><span data-stu-id="f2c1f-103">Troubleshoot reservations in warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f2c1f-104">Selles teemas kirjeldatakse, kuidas lahendada lao broneerimistega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.</span><span class="sxs-lookup"><span data-stu-id="f2c1f-104">This topic describes how to fix common issues that you might encounter while you work with warehouse reservations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="f2c1f-105">Teemade kohta, mis on seotud partii- ja seerianumbri registreerimistega, vt [Lao partii ja seeria reserveerimise hierarhiate tõrkeotsing](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md).</span><span class="sxs-lookup"><span data-stu-id="f2c1f-105">For topics that are related to batch and serial number registrations, see [Troubleshoot warehouse batch and serial reservation hierarchies](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md).</span></span>

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a><span data-ttu-id="f2c1f-106">Kuvatakse järgnev tõrge „Broneeringuid ei saa eemaldada, kuna loodud on töö, mis sõltub nendest broneeringutest”.</span><span class="sxs-lookup"><span data-stu-id="f2c1f-106">I receive the following error message: "Reservations cannot be removed because there is work created which relies on the reservations."</span></span>

### <a name="issue-description"></a><span data-ttu-id="f2c1f-107">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="f2c1f-107">Issue description</span></span>

<span data-ttu-id="f2c1f-108">Te ei saa varude broneerimist müügirealt maha võtta, kuna rea suhtes on avatud töö.</span><span class="sxs-lookup"><span data-stu-id="f2c1f-108">You can't unreserve inventory on a sales line, because there is open work against the line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f2c1f-109">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="f2c1f-109">Issue resolution</span></span>

<span data-ttu-id="f2c1f-110">Uurige, kas avatud pakkimisgrupi töö on olemas, et tuua kaup pakkimisühiku teise asukohta (nt *Uks*).</span><span class="sxs-lookup"><span data-stu-id="f2c1f-110">Investigate whether open packing group work exists to bring the item from a packing station to another location (such as *Baydoor*).</span></span> <span data-ttu-id="f2c1f-111">Vaadake üle kirjed **Töö loomise ajaloo logi** ja **Töö üksikasjade** lehtedel, et teha kindlaks, mis kaupa füüsiliselt broneerib, ja seejärel lõpetage või kustutage töö, et broneeringut vabastada.</span><span class="sxs-lookup"><span data-stu-id="f2c1f-111">Review the records on the **Work creation history log** and **Work details** pages to determine what is physically reserving the inventory, and then complete or delete the work to free up the reservation.</span></span>

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a><span data-ttu-id="f2c1f-112">Kuvatakse järgmine tõrketeade: "Varude kogust -%1 ei saanud uuendada kauba %2 ebapiisavate kaubavaru kannete tõttu."</span><span class="sxs-lookup"><span data-stu-id="f2c1f-112">I receive the following error message: "Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2...."</span></span>

### <a name="issue-description"></a><span data-ttu-id="f2c1f-113">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="f2c1f-113">Issue description</span></span>

<span data-ttu-id="f2c1f-114">See probleem võib ilmneda juhul, kui süsteem ei saa varude kogust värskendada, kuna pole piisavalt laokandeid, millel on määratud dimensioone.</span><span class="sxs-lookup"><span data-stu-id="f2c1f-114">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="f2c1f-115">Siin on täieliku tõrketeate täistekst:</span><span class="sxs-lookup"><span data-stu-id="f2c1f-115">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="f2c1f-116">Varude kogust -%1 ei saanud värskendada, kuna pole piisavalt laokandeid kaubaga %2, mille dimensioonid on suurus =%3, värvus =%4, täiendused =%5, sait =%6, ladu =%7, asukoht =%8, varude olek = saadaval, identifitseerimisnumber =%9, partii number =%10 ID-kood %11 saatepartii ID %12.</span><span class="sxs-lookup"><span data-stu-id="f2c1f-116">Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2 with dimensions Size=%3, Color=%4, Additions=%5, Site=%6, Warehouse=%7, Location=%8, Inventory status=Available, License plate=%9, Batch number=%10 for reference ID %11 on Lot ID %12.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f2c1f-117">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="f2c1f-117">Issue resolution</span></span>

<span data-ttu-id="f2c1f-118">Veenduge, et varude kanded ei broneeriks kauba kogust füüsiliselt.</span><span class="sxs-lookup"><span data-stu-id="f2c1f-118">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="f2c1f-119">Näiteks võivad need kanded avada kvaliteetseid tellimusi, lao blokeerimise kirjeid või väljaminekuordereid.</span><span class="sxs-lookup"><span data-stu-id="f2c1f-119">For example, these transactions might open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a><span data-ttu-id="f2c1f-120">Kuvatakse järgmine tõrketeade: "Füüsilist laoseisu... ei saa broneerida, kuna laos on saadaval ainult 0,00."</span><span class="sxs-lookup"><span data-stu-id="f2c1f-120">I receive the following error message: "Physical on-hand...cannot be reserved because only 0.00 are available in the inventory."</span></span>

### <a name="issue-description"></a><span data-ttu-id="f2c1f-121">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="f2c1f-121">Issue description</span></span>

<span data-ttu-id="f2c1f-122">See probleem võib ilmneda juhul, kui süsteem ei saa varude kogust värskendada, kuna pole piisavalt laokandeid, millel on määratud dimensioone.</span><span class="sxs-lookup"><span data-stu-id="f2c1f-122">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="f2c1f-123">Siin on täieliku tõrketeate täistekst:</span><span class="sxs-lookup"><span data-stu-id="f2c1f-123">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="f2c1f-124">Füüsiline vaba kaubavaru sait=%1, ladu=%2, varude olek=saadaval, partii number=%3, omanik=%4: %5 ei saa broneerida, kuna laos on saadaval ainult 0,00.</span><span class="sxs-lookup"><span data-stu-id="f2c1f-124">Physical on-hand Site=%1, Warehouse=%2, Inventory status=Available, Batch number=%3, Owner=%4: %5 cannot be reserved because only 0.00 are available in the inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="f2c1f-125">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="f2c1f-125">Issue resolution</span></span>

<span data-ttu-id="f2c1f-126">See probleem on tõenäoliselt põhjustatud avatud tööst.</span><span class="sxs-lookup"><span data-stu-id="f2c1f-126">This issue is probably caused by open work.</span></span> <span data-ttu-id="f2c1f-127">Lõpetage töö või võtke vastu ilma töö loomiseta.</span><span class="sxs-lookup"><span data-stu-id="f2c1f-127">Either complete the work or receive without work creation.</span></span> <span data-ttu-id="f2c1f-128">Veenduge, et varude kanded ei broneeriks kauba kogust füüsiliselt.</span><span class="sxs-lookup"><span data-stu-id="f2c1f-128">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="f2c1f-129">Näiteks võivad need kanded olla avatud kvaliteetsed tellimused, lao blokeerimise kirjed või väljamineku tellimused.</span><span class="sxs-lookup"><span data-stu-id="f2c1f-129">For example, these transactions might be open quality orders, inventory blocking records, or output orders.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
