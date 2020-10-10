---
title: Tõrke haldamine
description: Selles teemas kirjeldatakse varahalduse tõrke haldust.
author: josaw1
manager: tfehr
ms.date: 08/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetFaultArea, EntAssetFaultDesigner, EntAssetFaultCopyFromObjectType, EntAssetFaultRemedy, EntAssetObjectFaultRelationRequestInfoPart, EntAssetObjectFaultRelationWorkOrderInfoPart, EntAssetFaultCreateCombinations, EntAssetObjectFaultSymptom, EntAssetObjectFaultSymptomListPage, EntAssetFaultType, EntAssetFaultSymptom, EntAssetFaultCause
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 72d6c8d750a5a0903017b4c77b3ce5d9521cf99b
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889357"
---
# <a name="fault-management"></a><span data-ttu-id="428ad-103">Tõrke haldamine</span><span class="sxs-lookup"><span data-stu-id="428ad-103">Fault management</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="428ad-104">Varahalduses saate vara tüüpides seadistada tõrke sümptomeid, tõrke valdkondi ja tõrke tüüpe tõrke kujundajaga.</span><span class="sxs-lookup"><span data-stu-id="428ad-104">In Asset Management, you can use the fault designer to set up fault symptoms, fault areas, and fault types on asset types.</span></span> <span data-ttu-id="428ad-105">Nii saate hallata varades tuvastatavaid tõrkeid.</span><span class="sxs-lookup"><span data-stu-id="428ad-105">In this way, you can manage faults that are detected on assets.</span></span> <span data-ttu-id="428ad-106">Lisaks saab tõrgete põhjuseid ja nende lahendamissoovitusi registreerida töökäsus.</span><span class="sxs-lookup"><span data-stu-id="428ad-106">Additionally, fault causes and suggestions for fixing faults can be registered on a work order.</span></span>

<span data-ttu-id="428ad-107">Tõrke registreerimine ja haldamine sisaldab neid etappe.</span><span class="sxs-lookup"><span data-stu-id="428ad-107">The process for fault registration and management consists of these steps.</span></span>

1. <span data-ttu-id="428ad-108">Looge loend vara tüüpides esineda võivatest tõrke sümptomitest, tõrke valdkondadest ja tõrke tüüpidest.</span><span class="sxs-lookup"><span data-stu-id="428ad-108">Create a list of fault symptoms, fault areas, and fault types that might occur on your asset types.</span></span>
2. <span data-ttu-id="428ad-109">Tõrke kujundajas seadistage tõrke sümptomeid, tõrke valdkondi ja tõrke tüüpe.</span><span class="sxs-lookup"><span data-stu-id="428ad-109">In the fault designer, set up symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="428ad-110">Siin on paar näidet, mis aitavad eristada tõrke sümptomeid, tõrke valdkondi ja tõrke tüüpe.</span><span class="sxs-lookup"><span data-stu-id="428ad-110">Here are some examples to help you understand the difference between fault symptoms, fault areas, and fault types.</span></span>

<span data-ttu-id="428ad-111">**Tõrke sümptomid:**</span><span class="sxs-lookup"><span data-stu-id="428ad-111">**Fault symptoms:**</span></span>

- <span data-ttu-id="428ad-112">tasakaalustamata pinged;</span><span class="sxs-lookup"><span data-stu-id="428ad-112">Unbalanced voltages</span></span>
- <span data-ttu-id="428ad-113">lühis;</span><span class="sxs-lookup"><span data-stu-id="428ad-113">Short circuit</span></span>
- <span data-ttu-id="428ad-114">Müra</span><span class="sxs-lookup"><span data-stu-id="428ad-114">Noise</span></span>
- <span data-ttu-id="428ad-115">leke;</span><span class="sxs-lookup"><span data-stu-id="428ad-115">Leak</span></span>
- <span data-ttu-id="428ad-116">vibratsioonid.</span><span class="sxs-lookup"><span data-stu-id="428ad-116">Vibrations</span></span>

<span data-ttu-id="428ad-117">**Tõrke valdkonnad:**</span><span class="sxs-lookup"><span data-stu-id="428ad-117">**Fault areas:**</span></span>

- <span data-ttu-id="428ad-118">elektriline;</span><span class="sxs-lookup"><span data-stu-id="428ad-118">Electrical</span></span>
- <span data-ttu-id="428ad-119">mehhaaniline;</span><span class="sxs-lookup"><span data-stu-id="428ad-119">Mechanical</span></span>
- <span data-ttu-id="428ad-120">hüdrauliline;</span><span class="sxs-lookup"><span data-stu-id="428ad-120">Hydraulic</span></span>
- <span data-ttu-id="428ad-121">pneumaatiline.</span><span class="sxs-lookup"><span data-stu-id="428ad-121">Pneumatic</span></span>

<span data-ttu-id="428ad-122">**Tõrke tüübid:**</span><span class="sxs-lookup"><span data-stu-id="428ad-122">**Fault types:**</span></span>

- <span data-ttu-id="428ad-123">vigane üldstaatori mähis;</span><span class="sxs-lookup"><span data-stu-id="428ad-123">Faulty main stator winding</span></span>
- <span data-ttu-id="428ad-124">vigane diood;</span><span class="sxs-lookup"><span data-stu-id="428ad-124">Faulty diode</span></span>
- <span data-ttu-id="428ad-125">mustad mähised;</span><span class="sxs-lookup"><span data-stu-id="428ad-125">Dirty windings</span></span>
- <span data-ttu-id="428ad-126">vigane generaator;</span><span class="sxs-lookup"><span data-stu-id="428ad-126">Defective generator</span></span>
- <span data-ttu-id="428ad-127">vigane andur.</span><span class="sxs-lookup"><span data-stu-id="428ad-127">Defective sensor</span></span>

## <a name="create-fault-symptoms"></a><span data-ttu-id="428ad-128">Looge rikkesümptomid</span><span class="sxs-lookup"><span data-stu-id="428ad-128">Create fault symptoms</span></span>

<span data-ttu-id="428ad-129">Järgige neid etappe, et luua loend tõrke kujundajas kasutatavatest sümptomitest.</span><span class="sxs-lookup"><span data-stu-id="428ad-129">Follow these steps to create a list of symptoms that can be used in the fault designer.</span></span>

1. <span data-ttu-id="428ad-130">Valige **Varahaldus** \> **Seadistus** \> **Tõrge** \> **Tõrke sümptomid**.</span><span class="sxs-lookup"><span data-stu-id="428ad-130">Select **Asset management** \> **Setup** \> **Fault** \> **Fault symptoms**.</span></span>
2. <span data-ttu-id="428ad-131">Valige **Uus**, et luua uus kirje.</span><span class="sxs-lookup"><span data-stu-id="428ad-131">Select **New** to create a record.</span></span>
3. <span data-ttu-id="428ad-132">Sisestage välja **Tõrke sümptom** tõrke sümptomi nimi.</span><span class="sxs-lookup"><span data-stu-id="428ad-132">In the **Fault symptom** field, enter a name for the fault symptom.</span></span>
4. <span data-ttu-id="428ad-133">Väljale **Kirjeldus** sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="428ad-133">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="428ad-134">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="428ad-134">Select **Save**.</span></span>

## <a name="create-fault-areas"></a><span data-ttu-id="428ad-135">Looge rikkevaldkonnad</span><span class="sxs-lookup"><span data-stu-id="428ad-135">Create fault areas</span></span>

<span data-ttu-id="428ad-136">Järgige neid etappe, et luua loend tõrke kujundajas kasutatavatest valdkondadest või asukohtadest.</span><span class="sxs-lookup"><span data-stu-id="428ad-136">Follow these steps to create a list of areas or locations that can be used in the fault designer.</span></span>

1. <span data-ttu-id="428ad-137">Valige **Varahaldus** \> **Seadistus** \> **Tõrge** \> **Tõrke valdkonnad**.</span><span class="sxs-lookup"><span data-stu-id="428ad-137">Select **Asset management** \> **Setup** \> **Fault** \> **Fault areas**.</span></span>
2. <span data-ttu-id="428ad-138">Valige **Uus**, et luua uus kirje.</span><span class="sxs-lookup"><span data-stu-id="428ad-138">Select **New** to create a record.</span></span>
3. <span data-ttu-id="428ad-139">Sisestage välja **Tõrke valdkond** tõrke valdkonna nimi.</span><span class="sxs-lookup"><span data-stu-id="428ad-139">In the **Fault area** field, enter a name for the fault area.</span></span>
4. <span data-ttu-id="428ad-140">Väljale **Kirjeldus** sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="428ad-140">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="428ad-141">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="428ad-141">Select **Save**.</span></span>

## <a name="create-fault-types"></a><span data-ttu-id="428ad-142">Looge tõrke tüübid</span><span class="sxs-lookup"><span data-stu-id="428ad-142">Create fault types</span></span>

<span data-ttu-id="428ad-143">Järgige neid etappe, et luua loend tõrke kujundajas kasutatavatest tõrke tüüpidest.</span><span class="sxs-lookup"><span data-stu-id="428ad-143">Follow these steps to create a list of fault types that can be used in the fault designer.</span></span>

1. <span data-ttu-id="428ad-144">Valige **Varahaldus** \> **Seadistus** \> **Tõrge** \> **Tõrke tüüpidest**.</span><span class="sxs-lookup"><span data-stu-id="428ad-144">Select **Asset management** \> **Setup** \> **Fault** \> **Fault types**.</span></span>
2. <span data-ttu-id="428ad-145">Valige **Uus**, et luua uus kirje.</span><span class="sxs-lookup"><span data-stu-id="428ad-145">Select **New** to create a record.</span></span>
3. <span data-ttu-id="428ad-146">Sisestage välja **Tõrke tüüp** tõrke tüübi nimi.</span><span class="sxs-lookup"><span data-stu-id="428ad-146">In the **Fault type** field, enter a name for the fault type.</span></span>
4. <span data-ttu-id="428ad-147">Väljale **Kirjeldus** sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="428ad-147">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="428ad-148">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="428ad-148">Select **Save**.</span></span>

## <a name="set-up-the-fault-designer"></a><span data-ttu-id="428ad-149">Seadistage tõrke kujundaja</span><span class="sxs-lookup"><span data-stu-id="428ad-149">Set up the fault designer</span></span>

<span data-ttu-id="428ad-150">Tõrke kujundajas seadistate vara tüüpide tõrke andmed.</span><span class="sxs-lookup"><span data-stu-id="428ad-150">In the fault designer, you set up fault data on asset types.</span></span>

1. <span data-ttu-id="428ad-151">Valige **Varahaldus** \> **Seadistus** \> **Tõrge** \> **Tõrke kujundaja**.</span><span class="sxs-lookup"><span data-stu-id="428ad-151">Select **Asset management** \> **Setup** \> **Fault** \> **Fault designer**.</span></span>
2. <span data-ttu-id="428ad-152">Valige vasakus paanis vara tüüp, et seadistada selle tõrke kannet.</span><span class="sxs-lookup"><span data-stu-id="428ad-152">In the left pane, select the type of asset to set up a fault record for.</span></span>
3. <span data-ttu-id="428ad-153">Kiirkaardil **Tõrke sümptom** valige **Lisa rida** ja seejärel valige väljas **Tõrke sümptom** tõrke sümptom.</span><span class="sxs-lookup"><span data-stu-id="428ad-153">On the **Fault symptom** FastTab, select **Add line**, and then, in the **Fault symptom** field, select a fault symptom.</span></span>
4. <span data-ttu-id="428ad-154">Kiirkaardil **Tõrke valdkond** valige **Lisa rida** ja seejärel valige väljas **Tõrke valdkond** tõrke valdkond.</span><span class="sxs-lookup"><span data-stu-id="428ad-154">On the **Fault area** FastTab, select **Add line**, and then, in the **Fault area** field select a fault area.</span></span>
5. <span data-ttu-id="428ad-155">Kiirkaardil **Tõrke tüüp** valige **Lisa rida** ja seejärel valige väljas **Tõrke tüüp** tõrke tüüp.</span><span class="sxs-lookup"><span data-stu-id="428ad-155">On the **Fault type** FastTab, select **Add line**, and then, in the **Fault type** field, select a fault type.</span></span>
6. <span data-ttu-id="428ad-156">Valitud vara tüübi kõikide olemasolevate tõrke sümptomite, valdkondade ja tüüpide kombinatsioonide kiireks loomiseks valige **Looge tõrke kombinatsioonid**.</span><span class="sxs-lookup"><span data-stu-id="428ad-156">To quickly create combinations of all existing fault symptoms, areas, and types for the selected asset type, select **Create fault combinations**.</span></span> <span data-ttu-id="428ad-157">Sellest on kasu siis, kui olete lisanud palju tõrke sümptomeid, valdkondi ja tüüpe.</span><span class="sxs-lookup"><span data-stu-id="428ad-157">This function is useful if you've added many fault symptoms, areas, and types.</span></span> <span data-ttu-id="428ad-158">Lihtsam on kustutada vara tüübiga mitte seotud mistahes kombinatsioonide ridu kui luua ise uusi ridu.</span><span class="sxs-lookup"><span data-stu-id="428ad-158">It's easier to delete the lines for any combinations that aren't relevant to the asset type than to create new lines manually.</span></span>

    > [!NOTE]
    > <span data-ttu-id="428ad-159">Tõrke sümptomite, valdkondade ja tüüpide seadete kopeerimiseks ühest vara tüübist valitud vara tüüpi valige **Kopeeri vara tüübist**.</span><span class="sxs-lookup"><span data-stu-id="428ad-159">To copy the setup of fault symptoms, areas, and types from one asset type to the selected asset type, select **Copy from asset type**.</span></span>

7. <span data-ttu-id="428ad-160">Oma muudatuste salvestamiseks valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="428ad-160">Select **Save** to save your changes.</span></span>

![Tõrke kujundaja leht](media/21-setup-for-work-orders.png)

## <a name="create-fault-causes"></a><span data-ttu-id="428ad-162">Looge tõrke põhjused</span><span class="sxs-lookup"><span data-stu-id="428ad-162">Create fault causes</span></span>

<span data-ttu-id="428ad-163">Järgige neid etappe, et luua loend teadaolevatest tõrke põhjustest, mida saab lisada töökäsku või hooldusnõudesse.</span><span class="sxs-lookup"><span data-stu-id="428ad-163">Follow these steps to create a list of known fault causes that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="428ad-164">Valige **Varahaldus** \> **Seadistus** \> **Tõrge** \> **Tõrke põhjused**.</span><span class="sxs-lookup"><span data-stu-id="428ad-164">Select **Asset management** \> **Setup** \> **Fault** \> **Fault causes**.</span></span>
2. <span data-ttu-id="428ad-165">Valige **Uus**, et luua uus kirje.</span><span class="sxs-lookup"><span data-stu-id="428ad-165">Select **New** to create a record.</span></span>
3. <span data-ttu-id="428ad-166">Sisestage välja **Tõrke põhjus** tõrke põhjuse nimi.</span><span class="sxs-lookup"><span data-stu-id="428ad-166">In the **Fault cause** field, enter a name for the fault cause.</span></span>
4. <span data-ttu-id="428ad-167">Väljale **Kirjeldus** sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="428ad-167">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="428ad-168">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="428ad-168">Select **Save**.</span></span>

## <a name="create-fault-remedies"></a><span data-ttu-id="428ad-169">Looge tõrkelahendusi</span><span class="sxs-lookup"><span data-stu-id="428ad-169">Create fault remedies</span></span>

<span data-ttu-id="428ad-170">Järgige neid etappe, et luua loend lahenduse ja paranduse soovitustest, mida saab lisada töökäsku või hooldusnõudesse.</span><span class="sxs-lookup"><span data-stu-id="428ad-170">Follow these steps to create a list of suggestions for remedy and repair that can be added to a work order or a maintenance request.</span></span>

1. <span data-ttu-id="428ad-171">Valige **Varahaldus** \> **Seadistus** \> **Tõrge** \> **Tõrke lahendused**.</span><span class="sxs-lookup"><span data-stu-id="428ad-171">Select **Asset management** \> **Setup** \> **Fault** \> **Fault remedies**.</span></span>
2. <span data-ttu-id="428ad-172">Valige **Uus**, et luua uus kirje.</span><span class="sxs-lookup"><span data-stu-id="428ad-172">Select **New** to create a record.</span></span>
3. <span data-ttu-id="428ad-173">Sisestage välja **Tõrke lahendus** tõrke lahenduse nimi.</span><span class="sxs-lookup"><span data-stu-id="428ad-173">In the **Fault remedy** field, enter a name for the fault remedy.</span></span>
4. <span data-ttu-id="428ad-174">Väljale **Kirjeldus** sisestage kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="428ad-174">In the **Description** field, enter a description.</span></span>
5. <span data-ttu-id="428ad-175">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="428ad-175">Select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="428ad-176">Saate vajadusel muuta tõrke sümptomite, valdkondade, tüüpide, põhjuste ja lahenduste nimesid.</span><span class="sxs-lookup"><span data-stu-id="428ad-176">You can change the names of your fault symptoms, areas, types, causes, and remedies as you require.</span></span> <span data-ttu-id="428ad-177">Nime muutused kajastuvad automaatselt vastavates tõrke registreerimistes.</span><span class="sxs-lookup"><span data-stu-id="428ad-177">The name changes are automatically reflected in the related fault registrations.</span></span>
