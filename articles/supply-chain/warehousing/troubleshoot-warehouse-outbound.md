---
title: Väljuvate kaupade laotoimingute tõrkeotsing
description: Selles teemas kirjeldatakse, kuidas lahendada väljuvate kaupade laotoimingutega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 1344a1c16bf72b31f7aaf18aaeb6e08c7bc9d87e
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5223262"
---
# <a name="troubleshoot-outbound-warehouse-operations"></a><span data-ttu-id="42bdf-103">Väljuvate kaupade laotoimingute tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="42bdf-103">Troubleshoot outbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="42bdf-104">Selles teemas kirjeldatakse, kuidas lahendada väljuvate kaupade laotoimingutega töötamisel tekkivaid probleeme Microsoft Dynamics 365 Supply Chain Management rakenduses.</span><span class="sxs-lookup"><span data-stu-id="42bdf-104">This topic describes how to fix common issues that you might encounter while you work with outbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-sales-order-could-not-be-released"></a><span data-ttu-id="42bdf-105">Kuvatakse järgmine tõrketeade: "Müügitellimust ei saanud väljastada."</span><span class="sxs-lookup"><span data-stu-id="42bdf-105">I receive the following error message: "Sales order could not be released."</span></span>

### <a name="issue-description"></a><span data-ttu-id="42bdf-106">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="42bdf-106">Issue description</span></span>

<span data-ttu-id="42bdf-107">See probleem võib ilmneda mitmel põhjusel.</span><span class="sxs-lookup"><span data-stu-id="42bdf-107">This issue can occur for several reasons.</span></span> <span data-ttu-id="42bdf-108">Näiteks on tellimus krediidihalduses ja ühtegi saadetist ei saa luua enne, kui kõigi müügitellimusega seotud müügiridade jaoks on sisestatud kehtiv postiaadress.</span><span class="sxs-lookup"><span data-stu-id="42bdf-108">For example, the order is on credit management hold, and no shipments can be created until a valid postal address is entered for all sales lines that are associated with a sales order.</span></span> <span data-ttu-id="42bdf-109">Teise võimalusena võib olla ootel tellimus, millega tuleb tegeleda enne, kui tellimuse saab lattu väljastada.</span><span class="sxs-lookup"><span data-stu-id="42bdf-109">Alternatively, there is an order hold that must be addressed before the order can be released to the warehouse.</span></span> <span data-ttu-id="42bdf-110">See ootele panemine võib olla seotud tellimusega või see võib olla tingitud kliendi kontost.</span><span class="sxs-lookup"><span data-stu-id="42bdf-110">This hold might be order-specific, or it might be on the customer account.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="42bdf-111">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="42bdf-111">Issue resolution</span></span>

<span data-ttu-id="42bdf-112">Lisage või värskendage aadressi müügitellimuse ja tellimuse ridadel ning seejärel väljastage tellimus lattu.</span><span class="sxs-lookup"><span data-stu-id="42bdf-112">Add or update the address on the sales order and order lines, and then release the order to the warehouse.</span></span> <span data-ttu-id="42bdf-113">Tellimusi saab lattu väljastada ainult siis, kui neil on kehtiv tarneaadress (iga **Organisatsiooni halduse** moodulis oleva aadressi vormingu seadistuse kohta).</span><span class="sxs-lookup"><span data-stu-id="42bdf-113">Orders can be released to the warehouse only if they have a valid delivery address (per the address format setup in the **Organization administration** module).</span></span>

<span data-ttu-id="42bdf-114">Uurige tellimuse ootel olekut ja lahendage probleemid.</span><span class="sxs-lookup"><span data-stu-id="42bdf-114">Investigate the order hold, and address the issues.</span></span> <span data-ttu-id="42bdf-115">Seejärel eemaldage ootele panemine tellimuselt või kliendilt ja väljastage tellimus lattu.</span><span class="sxs-lookup"><span data-stu-id="42bdf-115">Then remove the hold from the order or customer, and release the order to the warehouse.</span></span>

## <a name="i-receive-the-following-message-the-shipment-for-load-1-has-been-confirmed-however-no-lines-are-posted"></a><span data-ttu-id="42bdf-116">Kuvatakse järgmine teade: "Saadetis koormale 1% on kinnitatud."</span><span class="sxs-lookup"><span data-stu-id="42bdf-116">I receive the following message: "The shipment for load 1% has been confirmed."</span></span> <span data-ttu-id="42bdf-117">Kuid ridu ei sisestata.</span><span class="sxs-lookup"><span data-stu-id="42bdf-117">However, no lines are posted.</span></span>

### <a name="issue-description"></a><span data-ttu-id="42bdf-118">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="42bdf-118">Issue description</span></span>

<span data-ttu-id="42bdf-119">Koorma saadetis on kinnitatud, kuid ei ole edasist sisestamist.</span><span class="sxs-lookup"><span data-stu-id="42bdf-119">A shipment on a load was confirmed, but no further posting occurred.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="42bdf-120">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="42bdf-120">Issue resolution</span></span>

<span data-ttu-id="42bdf-121">Saatmise kinnitus ei mõjuta sisestamist.</span><span class="sxs-lookup"><span data-stu-id="42bdf-121">Shipment confirmation doesn't affect posting.</span></span> <span data-ttu-id="42bdf-122">See lihtsalt uuendab saadetise ja koorma olekut.</span><span class="sxs-lookup"><span data-stu-id="42bdf-122">It just updates the shipment and load status.</span></span> <span data-ttu-id="42bdf-123">Sisestamine peab toimuma eraldi protsessis.</span><span class="sxs-lookup"><span data-stu-id="42bdf-123">Posting must occur in a separate process.</span></span>

## <a name="i-receive-the-following-error-message-direct-delivery-is-not-able-to-process-for-warehouse-1-as-it-has-warehouse-management-enabled-please-specify-another-warehouse-that-is-not-enabled-for-warehouse-management"></a><span data-ttu-id="42bdf-124">Kuvatakse järgmine tõrketeade: "Otsetarne ei ole võimeline töötlema ladu 1%, kuna see on lubatud laohalduseks.</span><span class="sxs-lookup"><span data-stu-id="42bdf-124">I receive the following error message: "Direct delivery is not able to process for warehouse 1% as it has warehouse management enabled.</span></span> <span data-ttu-id="42bdf-125">Määrake mõni muu ladu, mis pole laohalduse jaoks lubatud."</span><span class="sxs-lookup"><span data-stu-id="42bdf-125">Please specify another warehouse that is not enabled for warehouse management."</span></span>

### <a name="issue-description"></a><span data-ttu-id="42bdf-126">Probleemi kirjeldus</span><span class="sxs-lookup"><span data-stu-id="42bdf-126">Issue description</span></span>

<span data-ttu-id="42bdf-127">Kaup lisatakse müügireal otsetarneks laost, mis on lubatud laohalduse jaoks (WMS).</span><span class="sxs-lookup"><span data-stu-id="42bdf-127">An item is added to a sales line for direct delivery from a warehouse that is enabled for warehouse management (WMS).</span></span> <span data-ttu-id="42bdf-128">See tõrketeade kuvatakse müügirea uuendamisel.</span><span class="sxs-lookup"><span data-stu-id="42bdf-128">You receive this error message when the sales line is updated.</span></span> 

### <a name="issue-resolution"></a><span data-ttu-id="42bdf-129">Probleemi lahendamine</span><span class="sxs-lookup"><span data-stu-id="42bdf-129">Issue resolution</span></span>

<span data-ttu-id="42bdf-130">Microsoft on seda probleemi hinnanud ja on määranud, et see on funktsiooni piirang.</span><span class="sxs-lookup"><span data-stu-id="42bdf-130">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="42bdf-131">Praegu ei toeta WMS otsetarnet.</span><span class="sxs-lookup"><span data-stu-id="42bdf-131">Currently, WMS doesn't support direct delivery.</span></span> <span data-ttu-id="42bdf-132">Seetõttu peate otsetarne kasutamiseks valima mitte-WMS kauba ja lao.</span><span class="sxs-lookup"><span data-stu-id="42bdf-132">Therefore, to use direct delivery, you must select a non-WMS item and warehouse.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]