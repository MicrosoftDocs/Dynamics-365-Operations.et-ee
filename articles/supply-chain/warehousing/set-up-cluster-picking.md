---
title: Kogumi komplekteerimise seadistamine
description: Selles teemas kirjeldatakse, kuidas seadistada klastri komplekteerimist ja kuidas rakendada klastri komplekteerimisega kauba kinnitamist.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSClusterProfile, WHSRFAutoConfirm, WHSWorkCluster
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 009345e608c26887fedbe4a9c268367080593da2
ms.sourcegitcommit: a36a4f9915ae3eb36bf8220111cf1486387713d9
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/16/2020
ms.locfileid: "4017571"
---
# <a name="set-up-cluster-picking"></a><span data-ttu-id="9353f-103">Kogumi komplekteerimise seadistamine</span><span class="sxs-lookup"><span data-stu-id="9353f-103">Set up cluster picking</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9353f-104">Selles teemas kirjeldatakse, kuidas võimaldada töötajatel kasutada oma mobiilseid seameid komplekteerimistöö grupeerimiseks kogumitesse, et nad saaksid mitme töötellimuse puhul komplekteerida kaupu samal ajal ühest kohast.</span><span class="sxs-lookup"><span data-stu-id="9353f-104">This topic describes how to enable workers to use their mobile devices to group picking work into clusters, so that they can pick items from a single location for multiple work orders at the same time.</span></span> <span data-ttu-id="9353f-105">Seda nimetatakse *kogumi komplekteerimiseks*.</span><span class="sxs-lookup"><span data-stu-id="9353f-105">This is called *cluster picking*.</span></span>

## <a name="about-cluster-picking"></a><span data-ttu-id="9353f-106">Teave kogumi komplekteerimise kohta</span><span class="sxs-lookup"><span data-stu-id="9353f-106">About cluster picking</span></span>

<span data-ttu-id="9353f-107">Kui töötellimused on lattu vabastatud, saab töötaja määrata tellimused mobiilse seadme abil kogumisse.</span><span class="sxs-lookup"><span data-stu-id="9353f-107">After work orders are released to the warehouse, the worker can use a mobile device to assign the orders to a cluster.</span></span> <span data-ttu-id="9353f-108">Kogum korraldab töötaja jaoks komplekteerimistöö.</span><span class="sxs-lookup"><span data-stu-id="9353f-108">The cluster will organize the picking work for the worker.</span></span> <span data-ttu-id="9353f-109">Kui töötellimus on määratud kogumisse, peab töötaja tellimuse komplekteerimistöö tegemiseks kasutama kogumi komplekteerimist.</span><span class="sxs-lookup"><span data-stu-id="9353f-109">When a work order is assigned to a cluster, the worker must use cluster picking to perform the picking work for the order.</span></span> <span data-ttu-id="9353f-110">Töötaja ei saa kasutada muid komplekteerimisviise.</span><span class="sxs-lookup"><span data-stu-id="9353f-110">The worker cannot use other picking methods.</span></span> <span data-ttu-id="9353f-111">Kui töötellimus on kogumisse ekslikult määratud, peab töötaja kogumi lõhkuma ja selle uuesti looma.</span><span class="sxs-lookup"><span data-stu-id="9353f-111">If a work order is assigned to a cluster by mistake, the worker must break the cluster and then re-create it.</span></span>

<span data-ttu-id="9353f-112">Vajaduse korral saab töötaja edastada kogumi edasi teisele töötajale.</span><span class="sxs-lookup"><span data-stu-id="9353f-112">If needed, a worker can pass a cluster to another worker.</span></span> <span data-ttu-id="9353f-113">Sel juhul muutub kogumi olekuks Edastatud.</span><span class="sxs-lookup"><span data-stu-id="9353f-113">This changes the cluster status to Passed.</span></span> <span data-ttu-id="9353f-114">Kui töötaja kasutab komplekteerimis- ja mahapanekutöö lõpuleviimise näitamiseks mobiilset seadet, tuleb saadetis või koorem kinnitada kliendis.</span><span class="sxs-lookup"><span data-stu-id="9353f-114">When the worker uses a mobile device to indicate that the picking and put away work is completed, the shipment or load must be confirmed in the client.</span></span>

## <a name="enable-cluster-picking"></a><span data-ttu-id="9353f-115">Kogumi komplekteerimise lubamine</span><span class="sxs-lookup"><span data-stu-id="9353f-115">Enable cluster picking</span></span>

<span data-ttu-id="9353f-116">Kogumi komplekteerimise lubamiseks peate tegema järgmised seadistused.</span><span class="sxs-lookup"><span data-stu-id="9353f-116">To enable cluster picking, you must set up the following:</span></span>

- <span data-ttu-id="9353f-117">**Kogumiprofiilid** – saate määrata kogumi ID automaatse loomise, kasutatavate positsioonide arvu, kogumite lõhkumise ning komplekteerimistöö järjestamise ja kinnitamise viisi.</span><span class="sxs-lookup"><span data-stu-id="9353f-117">**Cluster profiles** – Specify whether to automatically generate cluster   IDs, the number of positions to use, when to break clusters, and how to   sequence and verify the picking work.</span></span>

- <span data-ttu-id="9353f-118">**Töömallid** – saate määrata, kuidas luua komplekteerimistöö kogumi komplekteerimiseks.</span><span class="sxs-lookup"><span data-stu-id="9353f-118">**Work templates** – Define how to create the picking work for cluster   picking.</span></span>

- <span data-ttu-id="9353f-119">**Asukoha korraldus** – saate määrata, kust kaubad komplekteerida ja kuhu need maha panna.</span><span class="sxs-lookup"><span data-stu-id="9353f-119">**Location directives** – Specify where to pick items from, and where to put   them.</span></span>

- <span data-ttu-id="9353f-120">**Mobiilse seadme menüü-üksused** – saate konfigureerida mobiilse seadme menüü-üksuse kasutama olemasolevat tööd, mida juhitakse kogumi komplekteerimisega.</span><span class="sxs-lookup"><span data-stu-id="9353f-120">**Mobile device menu items** – Configure a mobile device menu item to use existing work that is directed by cluster picking.</span></span> <span data-ttu-id="9353f-121">Seejärel peate menüü-üksuse lisama mobiilse seadme menüüsse, et see kuvataks mobiilses seadmes.</span><span class="sxs-lookup"><span data-stu-id="9353f-121">You must then add the menu item to a mobile device menu so that it is displayed on mobile devices.</span></span>

- <span data-ttu-id="9353f-122">**Laohalduse parameetrid** – saate määrata numbriseeria, mida kasutatakse, kui soovite kogumitele identifikaatorid luua.</span><span class="sxs-lookup"><span data-stu-id="9353f-122">**Warehouse management parameters** – Specify the number sequence to use if   you want to generate identifiers for clusters.</span></span>

## <a name="set-up-a-cluster-profile"></a><span data-ttu-id="9353f-123">Kogumi profiili seadistamine</span><span class="sxs-lookup"><span data-stu-id="9353f-123">Set up a cluster profile</span></span>

<span data-ttu-id="9353f-124">Kogumi profiili seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="9353f-124">To set up a cluster profile, follow these steps:</span></span>

1. <span data-ttu-id="9353f-125">Valige **Laohaldus** \> **Seadistamine** \> **Mobiilne seade** \> **Kogumiprofiilid**.</span><span class="sxs-lookup"><span data-stu-id="9353f-125">Click **Warehouse management** \> **Setup** \> **Mobile device** \>  **Cluster profiles**.</span></span>

1. <span data-ttu-id="9353f-126">Klõpsake uue profiili loomiseks suvandit **Uus**.</span><span class="sxs-lookup"><span data-stu-id="9353f-126">Click **New** to create a new profile.</span></span>

1. <span data-ttu-id="9353f-127">Klõpsake suvandit **Kogumi loomine** ja valikus **Kogumi sortimine** klõpsake suvandit **Uus** kogumi sortimiskriteeriumide seadistamiseks.</span><span class="sxs-lookup"><span data-stu-id="9353f-127">Click **Create cluster** and, under **Cluster sorting** , click **New** to set up the sorting criteria for the cluster.</span></span> <span data-ttu-id="9353f-128">Sortimiskriteeriumid määravad järjestuse, milles töötaja teeb komplekteerimistööd.</span><span class="sxs-lookup"><span data-stu-id="9353f-128">The sorting criteria control the order in which the worker will perform the picking work.</span></span> <span data-ttu-id="9353f-129">Saate lisada nii palju kriteeriume kui vaja.</span><span class="sxs-lookup"><span data-stu-id="9353f-129">You can add as many criteria as needed.</span></span>

1. <span data-ttu-id="9353f-130">Sisestage väljale **Järjekorranumber** number, mis määratleb järjestuse, milles sortimiskriteeriume töödeldakse.</span><span class="sxs-lookup"><span data-stu-id="9353f-130">In the **Sequence number** field, enter a number to define the order in  which the sorting criteria are processed.</span></span>

1. <span data-ttu-id="9353f-131">Valige väljal **Välja nimi** väli, mis määratleb sortimise.</span><span class="sxs-lookup"><span data-stu-id="9353f-131">In the **Field name** field, select the field that will determine the sorting.</span></span> <span data-ttu-id="9353f-132">Näiteks kui valite välja **WMSLocationId** , sorditakse töö asukoha järgi.</span><span class="sxs-lookup"><span data-stu-id="9353f-132">For example, if you select the **WMSLocationId** field, the work will be sorted by location.</span></span>

1. <span data-ttu-id="9353f-133">Väljal **Sortimine** tehke üks järgmistest valikutest.</span><span class="sxs-lookup"><span data-stu-id="9353f-133">In the **Sorting** field, select one of the following options.</span></span>

| <span data-ttu-id="9353f-134">**Suvand**</span><span class="sxs-lookup"><span data-stu-id="9353f-134">**Option**</span></span>     | <span data-ttu-id="9353f-135">**Kirjeldus**</span><span class="sxs-lookup"><span data-stu-id="9353f-135">**Description**</span></span>                                                                                                                                                                                                                    |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9353f-136">**Kasvavas järjestuses**</span><span class="sxs-lookup"><span data-stu-id="9353f-136">**Ascending**</span></span>  | <span data-ttu-id="9353f-137">Komplekteerimistööd järjestatakse sortimiskriteeriumite alusel kasvavalt.</span><span class="sxs-lookup"><span data-stu-id="9353f-137">Picking work is sequenced in ascending order based on the sorting criteria.</span></span> <span data-ttu-id="9353f-138">Näiteks kui kasutate sortimiskriteeriumina välja **WMSLocationId** ja teie asukoha ID-d on 1, 2, 3 ja 4, saate esmalt komplekteerida asukohast 4.</span><span class="sxs-lookup"><span data-stu-id="9353f-138">For example, if you use the **WMSLocationId** field as sorting criteria, and your location IDs are 1, 2, 3, and 4, you will pick from location 4 first.</span></span> |
| <span data-ttu-id="9353f-139">**Kahanevas järjestuses**</span><span class="sxs-lookup"><span data-stu-id="9353f-139">**Descending**</span></span> | <span data-ttu-id="9353f-140">Komplekteerimistööd järjestatakse sortimiskriteeriumite alusel kahanevalt.</span><span class="sxs-lookup"><span data-stu-id="9353f-140">Picking work is sequenced in descending order based on the sorting criteria.</span></span> <span data-ttu-id="9353f-141">Näiteks kui kasutate sortimiskriteeriumina välja **WMSLocationId** ja teie asukoha ID-d on 1, 2, 3 ja 4, saate esmalt komplekteerida asukohast 1.</span><span class="sxs-lookup"><span data-stu-id="9353f-141">For example, if you use the **WMSLocationId** field as sorting criteria, and your location IDs are 1, 2, 3, and 4, you will pick from location 1 first.</span></span> |

## <a name="item-confirmation"></a><span data-ttu-id="9353f-142">Kauba kinnitamine</span><span class="sxs-lookup"><span data-stu-id="9353f-142">Item confirmation</span></span>

<span data-ttu-id="9353f-143">Kogumi komplekteerimise rakendamiseks on kinnitamine väga oluline, et kontrollida kogumitesse lisatud kaupu.</span><span class="sxs-lookup"><span data-stu-id="9353f-143">When cluster picking is applied, item confirmation is crucial to verify the items that are added to clusters.</span></span> <span data-ttu-id="9353f-144">Kogumi komplekteerimisprotsessi ajal saab kaupu kogumi komplekteerimisel kontrollida.</span><span class="sxs-lookup"><span data-stu-id="9353f-144">You can verify items in cluster picking during the cluster picking process.</span></span> <span data-ttu-id="9353f-145">Seadistus põhineb toote vöötkoodi seadistusel.</span><span class="sxs-lookup"><span data-stu-id="9353f-145">The setup is based on the product bar code setup.</span></span>

### <a name="set-up-item-verification-with-cluster-picking"></a><span data-ttu-id="9353f-146">Kauba kontrollimise seadistamine kogumi komplekteerimisega</span><span class="sxs-lookup"><span data-stu-id="9353f-146">Set up item verification with cluster picking</span></span>

1. <span data-ttu-id="9353f-147">Avage mobiilse seadme menüü üksuses seadistusvorm töö kinnitamiseks: **Laohaldus** \> **Laohaldus** \> **Seadistus** \> **Mobiilne seade** \> **Mobiilse seadme menüü üksused**.</span><span class="sxs-lookup"><span data-stu-id="9353f-147">On a mobile device menu item, open the setup form for work confirmation:  **Warehouse management** \> **Warehouse management** \> **Setup** \>  **Mobile device** \> **Mobile device menu items**.</span></span>

1. <span data-ttu-id="9353f-148">Avage mobiilse seadme menüüelemendist jaotis **Töö kinnituse häälestus**.</span><span class="sxs-lookup"><span data-stu-id="9353f-148">From the mobile device menu item, open **Work confirmation setup**.</span></span> <span data-ttu-id="9353f-149">Suvand **Toote kinnitus** võimaldab iga varude üksust mobiilsel seadmel skannides kontrollida.</span><span class="sxs-lookup"><span data-stu-id="9353f-149">The **Product confirmation** option allows you to verify each piece of inventory from the mobile device when scanned.</span></span>
