---
title: Mittevastavuste loomine ja töötlemine
description: Selles teemas tutvustatakse, kuidas teha mittevastavuse haldust olemasoleva kvaliteettellimuse põhjal.
author: perlynne
ms.date: 03/23/2021
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 06a56a694f7a80d65cb46d08744e78d8361cee3b
ms.sourcegitcommit: 8362f3bd32ce8b9a5af93c8e57daef732a93b19e
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/28/2021
ms.locfileid: "5956202"
---
# <a name="create-and-process-nonconformances"></a><span data-ttu-id="14d31-103">Mittevastavuste loomine ja töötlemine</span><span class="sxs-lookup"><span data-stu-id="14d31-103">Create and process nonconformances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="14d31-104">Selles teemas tutvustatakse, kuidas teha mittevastavuse haldust olemasoleva kvaliteettellimuse põhjal.</span><span class="sxs-lookup"><span data-stu-id="14d31-104">This topic describes how to perform nonconformance management based on an existing quality order.</span></span> <span data-ttu-id="14d31-105">Mittevastavuse haldust viib tavaliselt läbi kvaliteediametnik.</span><span class="sxs-lookup"><span data-stu-id="14d31-105">Typically, nonconformance management is done by a quality clerk.</span></span> <span data-ttu-id="14d31-106">Eeltingimusena peab teil olema saadaval kvaliteettellimus.</span><span class="sxs-lookup"><span data-stu-id="14d31-106">As a prerequisite, you must have a quality order available.</span></span> <span data-ttu-id="14d31-107">(Lisateavet kvaliteettellimuse loomise kohta vt teemast [Kaupade kvaliteedi kontrollimine ](inspect-quality-goods.md).)</span><span class="sxs-lookup"><span data-stu-id="14d31-107">(For information about how to create a quality order, see [Inspect the quality of goods](inspect-quality-goods.md).)</span></span>

<span data-ttu-id="14d31-108">Enne, kui kasutaja saab mittevastavuse kinnitamist töödelda, peab töötaja olema määratud talle lehel **Kasutajad** oleval väljal **Isik**.</span><span class="sxs-lookup"><span data-stu-id="14d31-108">Before a user can process the approval of a nonconformance, a worker must be assigned to them in the **Person** field on the **Users** page.</span></span> <span data-ttu-id="14d31-109">Lisaks tuleb enne kasutajal dokumendi märkuste kasutamist kasutajavalikutes seada valik **Luba dokumendi käsitlemine** väärtusele *Jah*.</span><span class="sxs-lookup"><span data-stu-id="14d31-109">Additionally, before the user can use the document notes, the **Enable document handling** option must be set to *Yes* in their user options.</span></span>

## <a name="create-a-nonconformance"></a><span data-ttu-id="14d31-110">Mittevastavuse loomine</span><span class="sxs-lookup"><span data-stu-id="14d31-110">Create a nonconformance</span></span>

<span data-ttu-id="14d31-111">Mittevastavuse loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="14d31-111">To create a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="14d31-112">Avage **Varude haldus \> Perioodilised ülesanded \> Kvaliteedijuhtimine \> Mittevastavused**.</span><span class="sxs-lookup"><span data-stu-id="14d31-112">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="14d31-113">Valige toimingupaanil nupp **Uus**.</span><span class="sxs-lookup"><span data-stu-id="14d31-113">On the Action pane, select **New**.</span></span>
1. <span data-ttu-id="14d31-114">Dialoogiakna **Mittevastavuse loomine** väljal **Probleemi tüüp** valige probleemi tüüp, mis kontrollprotsessi käigus leiti.</span><span class="sxs-lookup"><span data-stu-id="14d31-114">In the **Create non conformance** dialog box, in **Problem type** field, select the type of problem that was found during the inspection process.</span></span>
1. <span data-ttu-id="14d31-115">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="14d31-115">Select **OK**.</span></span>

## <a name="approve-or-reject-a-nonconformance"></a><span data-ttu-id="14d31-116">Mittevastavuse kinnitamine või tagasilükkamine</span><span class="sxs-lookup"><span data-stu-id="14d31-116">Approve or reject a nonconformance</span></span>

<span data-ttu-id="14d31-117">Mittevastavuse kinnitamiseks või tagasilükkamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="14d31-117">To approve or reject a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="14d31-118">Avage **Varude haldus \> Perioodilised ülesanded \> Kvaliteedijuhtimine \> Mittevastavused**.</span><span class="sxs-lookup"><span data-stu-id="14d31-118">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="14d31-119">Leidke ja valige loendist mittevastavus, mille soovite uuendada.</span><span class="sxs-lookup"><span data-stu-id="14d31-119">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="14d31-120">Saate lisada paranduse ainult kinnitatud mittevastavustele.</span><span class="sxs-lookup"><span data-stu-id="14d31-120">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="14d31-121">Tegevuspaanil valige, et mittevastavus kinnitada või **Funktsioonid \> Kinnita mittevastavus**, et mittevastavus kinnitada, või **Funktsioonid \> Keeldu mittevastavusest**, et see tagasi lükata.</span><span class="sxs-lookup"><span data-stu-id="14d31-121">On the Action Pane, select **Functions \> Approve non conformance** to approve the nonconformance or **Functions \> Refuse non conformance** to reject it.</span></span> <span data-ttu-id="14d31-122">Kinnitatud mittevastavused saate seostada [seotud toimingutega](../quality-operations.md).</span><span class="sxs-lookup"><span data-stu-id="14d31-122">You can associate approved nonconformances with [related operations](../quality-operations.md).</span></span> <span data-ttu-id="14d31-123">Sel viisil saate salvestada töö, mis tehakse mittevastavuse käsitlemise ja paranduste töötlemise osana.</span><span class="sxs-lookup"><span data-stu-id="14d31-123">In this way, you can record work that is done as part of the nonconformance handling and the processing of correction handling.</span></span>
1. <span data-ttu-id="14d31-124">Kui teil palutakse tegevus kinnitada, kinnitage oma valik.</span><span class="sxs-lookup"><span data-stu-id="14d31-124">You're prompted to confirm your selection.</span></span> <span data-ttu-id="14d31-125">Jätkamiseks valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="14d31-125">Select **Yes** to continue.</span></span>

## <a name="add-operations-and-other-details-to-nonconformances"></a><span data-ttu-id="14d31-126">Mittevastavustele toimingute ja muude üksikasjade lisamine</span><span class="sxs-lookup"><span data-stu-id="14d31-126">Add operations and other details to nonconformances</span></span>

<span data-ttu-id="14d31-127">Kui olete mittevastavuse loonud, saate alustada seotud operatsioonide lisamist ja määrata nende operatsioonide kohta lisateavet.</span><span class="sxs-lookup"><span data-stu-id="14d31-127">After you've created a nonconformance, you can start to add related operations and specify additional information about those operations.</span></span> <span data-ttu-id="14d31-128">Saate lisada seotud tegevusi ainult kinnitatud mittevastavustele.</span><span class="sxs-lookup"><span data-stu-id="14d31-128">You can add related operations only to nonconformances that are approved.</span></span>

<span data-ttu-id="14d31-129">Lisaks põhiteabele saate operatsioonile lisada ka järgmised üksikasjad:</span><span class="sxs-lookup"><span data-stu-id="14d31-129">Besides the basic information, you can add the following details to an operation:</span></span>

- <span data-ttu-id="14d31-130">**Kaubad** – saate luua nende kaupade loendi, mis tarbitakse paranduse katteks.</span><span class="sxs-lookup"><span data-stu-id="14d31-130">**Items** – You can create a list of items that are consumed to perform the correction.</span></span> <span data-ttu-id="14d31-131">Näiteks võivad kaubad olla tooted, mis on vajalikud valmistoodangu taastöötlemiseks vajalike seadmete või koostisainete remondiks.</span><span class="sxs-lookup"><span data-stu-id="14d31-131">For example, the items might be products that are required to repair equipment or ingredients that are required to rework a finished product.</span></span>
- <span data-ttu-id="14d31-132">**Kvaliteedikulud** – saate luua kulude loendi, mis on tekkinud või väljaarvestatud välisallikatele.</span><span class="sxs-lookup"><span data-stu-id="14d31-132">**Quality charges** – You can create a list of charges that are incurred or billed out to external sources.</span></span>
- <span data-ttu-id="14d31-133">**Ajatabel** – saate luua logi ajast, mil iga töötaja operatsioonile kulutab.</span><span class="sxs-lookup"><span data-stu-id="14d31-133">**Timesheet** – You can create a log of the time that each worker spends on the operation.</span></span>

<span data-ttu-id="14d31-134">Ülejäänud seaded on valikulised.</span><span class="sxs-lookup"><span data-stu-id="14d31-134">The remaining settings are optional.</span></span> <span data-ttu-id="14d31-135">Iga kauba kulu, kvaliteedikulud ja ajatabel on summeeritud ja operatsioonis näidatud.</span><span class="sxs-lookup"><span data-stu-id="14d31-135">The cost for each item, quality charges, and the timesheet are summed and shown on the operation.</span></span> <span data-ttu-id="14d31-136">Te ei saa otse redigeerida operatsiooni välja **Kulu**.</span><span class="sxs-lookup"><span data-stu-id="14d31-136">You can't directly edit the **Cost** field on the operation.</span></span>

### <a name="create-an-operation-for-a-nonconformance"></a><span data-ttu-id="14d31-137">Operatsiooni loomine mittevastavusele</span><span class="sxs-lookup"><span data-stu-id="14d31-137">Create an operation for a nonconformance</span></span>

<span data-ttu-id="14d31-138">Mittevastavuse operatsiooni loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="14d31-138">To create an operation for a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="14d31-139">Avage **Varude haldus \> Perioodilised ülesanded \> Kvaliteedijuhtimine \> Mittevastavused**.</span><span class="sxs-lookup"><span data-stu-id="14d31-139">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="14d31-140">Leidke ja valige loendist mittevastavus, mille soovite uuendada.</span><span class="sxs-lookup"><span data-stu-id="14d31-140">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="14d31-141">Saate lisada või uuendada seotud tegevusi ainult kinnitatud mittevastavustele.</span><span class="sxs-lookup"><span data-stu-id="14d31-141">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="14d31-142">Valige toimingupaanil suvand **Seotud operatsioonid**.</span><span class="sxs-lookup"><span data-stu-id="14d31-142">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="14d31-143">Ruudustiku rea lisamiseks valige **seotud toimingute** lehekülje tegevuspaanil suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="14d31-143">On the **Related operations** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="14d31-144">Seejärel määrake uuel real järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="14d31-144">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="14d31-145">**Toiming** – valige mittevastavuse jaoks sooritatav toimingu kood.</span><span class="sxs-lookup"><span data-stu-id="14d31-145">**Operation** – Select the code of the operation that will be performed for the nonconformance.</span></span>
    - <span data-ttu-id="14d31-146">**Põhjus** – sisestage üksikasjalik kirjeldus, mis selgitab operatsiooni vajalikkust.</span><span class="sxs-lookup"><span data-stu-id="14d31-146">**Reason** – Enter a detailed description that explains why the operation is required.</span></span>
    - <span data-ttu-id="14d31-147">**Müügitellimus** – kui valitud toimingukood on seotud müügitellimuse tüübiga, valige müügitellimus, millega te operatsiooni seote.</span><span class="sxs-lookup"><span data-stu-id="14d31-147">**Sales order** – If the selected operation code is related to the sales order type, select the sales order that you're linking the operation to.</span></span>
    - <span data-ttu-id="14d31-148">**Ostutellimus** – kui valitud toimingukood on seotud ostuellimuse tüübiga, valige ostutellimus, millega te operatsiooni seote.</span><span class="sxs-lookup"><span data-stu-id="14d31-148">**Purchase order** – If the selected operation code is related to the purchase order type, select the purchase order that you're linking the operation to.</span></span>

1. <span data-ttu-id="14d31-149">Sulgege lehed.</span><span class="sxs-lookup"><span data-stu-id="14d31-149">Close the pages.</span></span>

### <a name="add-items-to-an-operation"></a><span data-ttu-id="14d31-150">Kaupade lisamine operatsioonile</span><span class="sxs-lookup"><span data-stu-id="14d31-150">Add items to an operation</span></span>

<span data-ttu-id="14d31-151">Kaupade lisamiseks operatsioonile järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="14d31-151">To add items to an operation, follow these steps.</span></span>

1. <span data-ttu-id="14d31-152">Avage **Varude haldus \> Perioodilised ülesanded \> Kvaliteedijuhtimine \> Mittevastavused**.</span><span class="sxs-lookup"><span data-stu-id="14d31-152">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="14d31-153">Leidke ja valige loendist mittevastavus, mille soovite uuendada.</span><span class="sxs-lookup"><span data-stu-id="14d31-153">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="14d31-154">Saate lisada või uuendada seotud tegevusi ainult kinnitatud mittevastavustele.</span><span class="sxs-lookup"><span data-stu-id="14d31-154">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="14d31-155">Valige toimingupaanil suvand **Seotud operatsioonid**.</span><span class="sxs-lookup"><span data-stu-id="14d31-155">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="14d31-156">Valige leheküljel **Seotud operatsioonid** operatsioon, millele soovite kaupu lisada.</span><span class="sxs-lookup"><span data-stu-id="14d31-156">On the **Related operations** page, select the operation that you want to add items to.</span></span>
1. <span data-ttu-id="14d31-157">Toimingupaanil valige käsk **Kaubad**.</span><span class="sxs-lookup"><span data-stu-id="14d31-157">On the Action Pane, select **Items**.</span></span>
1. <span data-ttu-id="14d31-158">Ruudustiku rea lisamiseks valige **seotud toimingute** lehekülje tegevuspaanil suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="14d31-158">On the **Related operations** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="14d31-159">Seejärel määrake uuel real järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="14d31-159">Then set the following fields for new row:</span></span>

    - <span data-ttu-id="14d31-160">**Kaubakood** – valige toode, mida tarbitakse valitud operatsiooni osana.</span><span class="sxs-lookup"><span data-stu-id="14d31-160">**Item number** – Select the product that will be consumed as part of the selected operation.</span></span>
    - <span data-ttu-id="14d31-161">**Kogus** – sisestage tarbitavate kaupade arv.</span><span class="sxs-lookup"><span data-stu-id="14d31-161">**Quantity** – Enter the number of items that will be consumed.</span></span>

    > [!NOTE]
    > <span data-ttu-id="14d31-162">Kauba kulu saate vaadata vahekaardi **Üldine** väljal **Kulu**. Näidatud kulu tuleb leheküljel **Väljastatud toode** seadistatud kulust.</span><span class="sxs-lookup"><span data-stu-id="14d31-162">You can view the cost for the item in the **Cost** field on the **General** tab. The cost that is shown there comes from the cost that is set up on the **Released product** page.</span></span> <span data-ttu-id="14d31-163">Kulu ei saa otse **seotud toimingu kauba lehel** uuendada.</span><span class="sxs-lookup"><span data-stu-id="14d31-163">The cost can't be updated directly on the **Related operation item** page.</span></span> <span data-ttu-id="14d31-164">Kõigi kaupade kulu, mis on lisatud **seotud toimingu kaupade** lehele, lisatakse automaatselt **seotud toimingute** lehe väljale **Kulu**.</span><span class="sxs-lookup"><span data-stu-id="14d31-164">The cost of all items that are added on the **Related operation items** page is automatically added to the **Cost** field on the **Related operations** page.</span></span>

1. <span data-ttu-id="14d31-165">Korrake eelmist sammu iga lisakauba puhul, mille peate lisama.</span><span class="sxs-lookup"><span data-stu-id="14d31-165">Repeat the previous step for each additional item that you must add.</span></span>
1. <span data-ttu-id="14d31-166">Sulgege lehed.</span><span class="sxs-lookup"><span data-stu-id="14d31-166">Close the pages.</span></span>

### <a name="add-quality-charges-to-an-operation"></a><span data-ttu-id="14d31-167">Operatsioonile kvaliteedikulude lisamine</span><span class="sxs-lookup"><span data-stu-id="14d31-167">Add quality charges to an operation</span></span>

<span data-ttu-id="14d31-168">Kvaliteedikulude lisamiseks operatsioonile järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="14d31-168">To add quality charges to an operation, follow these steps.</span></span>

1. <span data-ttu-id="14d31-169">Avage **Varude haldus \> Perioodilised ülesanded \> Kvaliteedijuhtimine \> Mittevastavused**.</span><span class="sxs-lookup"><span data-stu-id="14d31-169">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="14d31-170">Leidke ja valige loendist mittevastavus, mille soovite uuendada.</span><span class="sxs-lookup"><span data-stu-id="14d31-170">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="14d31-171">Saate lisada või uuendada seotud tegevusi ainult kinnitatud mittevastavustele.</span><span class="sxs-lookup"><span data-stu-id="14d31-171">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="14d31-172">Valige toimingupaanil suvand **Seotud operatsioonid**.</span><span class="sxs-lookup"><span data-stu-id="14d31-172">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="14d31-173">Valige leheküljel **Seotud operatsioonid** operatsioon, millele soovite kvaliteedikulusid lisada.</span><span class="sxs-lookup"><span data-stu-id="14d31-173">On the **Related operations** page, select the operation that you want to add quality charges to.</span></span>
1. <span data-ttu-id="14d31-174">Valige toimingupaanil suvand **Kvaliteedikulud**.</span><span class="sxs-lookup"><span data-stu-id="14d31-174">On the Action Pane, select **Quality charges**.</span></span>
1. <span data-ttu-id="14d31-175">Ruudustiku rea lisamiseks valige **seotud toimingute kulud** lehekülje tegevuspaanil suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="14d31-175">On the **Related operation charges** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="14d31-176">Seejärel määrake uuel real järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="14d31-176">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="14d31-177">**Kulude kood** – valige kvaliteedikulu, mida soovite lisada.</span><span class="sxs-lookup"><span data-stu-id="14d31-177">**Charges code** – Select the quality charge that you want to add.</span></span>
    - <span data-ttu-id="14d31-178">**Kirjeldus** – sisestage kulu detailne kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="14d31-178">**Description** – Enter a detailed description of the charge.</span></span>
    - <span data-ttu-id="14d31-179">**Kulude summa** – sisestage kulude summa.</span><span class="sxs-lookup"><span data-stu-id="14d31-179">**Charges value** – Enter the amount of the charge.</span></span>

1. <span data-ttu-id="14d31-180">Korrake eelmist sammu iga kulu puhul, mille peate lisama.</span><span class="sxs-lookup"><span data-stu-id="14d31-180">Repeat the previous step for each additional charge that you must add.</span></span>
1. <span data-ttu-id="14d31-181">Sulgege lehed.</span><span class="sxs-lookup"><span data-stu-id="14d31-181">Close the pages.</span></span>

> [!NOTE]
> <span data-ttu-id="14d31-182">**Kulude väärtuse** väljal olevad summad summeeritakse automaatselt kõigi kvaliteedikulude osas ja lisatakse mis tahes muudele summadele väljal **Kulu** **seotud toimingute** lehel.</span><span class="sxs-lookup"><span data-stu-id="14d31-182">The amount in the **Charges value** field is automatically summed for all quality charges and added to any other amounts in the **Cost** field on the **Related operations** page.</span></span>

### <a name="create-a-timesheet-on-an-operation"></a><span data-ttu-id="14d31-183">Toimingu kohta ajatabeli loomine</span><span class="sxs-lookup"><span data-stu-id="14d31-183">Create a timesheet on an operation</span></span>

<span data-ttu-id="14d31-184">Ajatabeli lisamiseks operatsioonile järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="14d31-184">To add a timesheet to an operation, follow these steps.</span></span>

1. <span data-ttu-id="14d31-185">Avage **Varude haldus \> Perioodilised ülesanded \> Kvaliteedijuhtimine \> Mittevastavused**.</span><span class="sxs-lookup"><span data-stu-id="14d31-185">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="14d31-186">Leidke ja valige loendist mittevastavus, mille soovite uuendada.</span><span class="sxs-lookup"><span data-stu-id="14d31-186">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="14d31-187">Saate lisada või uuendada seotud tegevusi ainult kinnitatud mittevastavustele.</span><span class="sxs-lookup"><span data-stu-id="14d31-187">You can add or update operations only for nonconformances that are approved.</span></span>

1. <span data-ttu-id="14d31-188">Valige toimingupaanil suvand **Seotud operatsioonid**.</span><span class="sxs-lookup"><span data-stu-id="14d31-188">On the Action Pane, select **Related operations**.</span></span>
1. <span data-ttu-id="14d31-189">Valige leheküljel **Seotud operatsioonid** operatsioon, millele soovite ajatabelit lisada.</span><span class="sxs-lookup"><span data-stu-id="14d31-189">On the **Related operations** page, select the operation that you want to add a timesheet to.</span></span>
1. <span data-ttu-id="14d31-190">Valige tegevuste paanil käsk **Ajatabel**.</span><span class="sxs-lookup"><span data-stu-id="14d31-190">On the Action Pane, select **Timesheet**.</span></span>
1. <span data-ttu-id="14d31-191">Ruudustiku rea lisamiseks valige **seotud toimingute ajatabelid** lehekülje tegevuspaanil suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="14d31-191">On the **Related operation time sheets** page, on the Action pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="14d31-192">Seejärel määrake uuel real järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="14d31-192">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="14d31-193">**Kuupäev** – määrake töö tehtud töö kuupäev.</span><span class="sxs-lookup"><span data-stu-id="14d31-193">**Date** – Specify the date when work was done.</span></span> <span data-ttu-id="14d31-194">Vaikimisi on see väli seadistatud praegusele kuupäevale.</span><span class="sxs-lookup"><span data-stu-id="14d31-194">By default, this field is set to the current date.</span></span>
    - <span data-ttu-id="14d31-195">**Töötaja** – valige töötaja, kes tööd tegi.</span><span class="sxs-lookup"><span data-stu-id="14d31-195">**Worker** – Select the worker who did the work.</span></span> <span data-ttu-id="14d31-196">Vaikimisi on selle välja väärtuseks määratud praegusele kasutajale määratud töötaja.</span><span class="sxs-lookup"><span data-stu-id="14d31-196">By default, this field is set to the worker that is assigned to the current user.</span></span>
    - <span data-ttu-id="14d31-197">**Operatsiooni tunnid** – sisestage valitud operatsiooni ajal töötatud tundide arv.</span><span class="sxs-lookup"><span data-stu-id="14d31-197">**Operation hours** – Enter the number of hours that were worked on the selected operation.</span></span>
    - <span data-ttu-id="14d31-198">**Arveldatud** – märkige see ruut, kui arvel on kliendile või hankijale arve tasu küsimise aeg.</span><span class="sxs-lookup"><span data-stu-id="14d31-198">**Invoiced** – Select this check box if the time has been charged to a customer or vendor on an invoice.</span></span>

    > [!NOTE]
    > <span data-ttu-id="14d31-199">Kulu saate vaadata vahekaardi **Üldine** väljal **Kulu**. Kulu arvutatakse leheküljel **Varude halduse parameetrid** määratud määra alusel.</span><span class="sxs-lookup"><span data-stu-id="14d31-199">You can view the cost in the **Cost** field on the **General** tab. The cost is calculated by using the rate that you define on the **Inventory management parameters** page.</span></span>

1. <span data-ttu-id="14d31-200">Korrake eelmist sammu iga ajatabeli rea puhul, mille peate lisama.</span><span class="sxs-lookup"><span data-stu-id="14d31-200">Repeat the previous step for each additional timesheet line that you must add.</span></span>
1. <span data-ttu-id="14d31-201">Sulgege lehed.</span><span class="sxs-lookup"><span data-stu-id="14d31-201">Close the pages.</span></span>

> [!NOTE]
> <span data-ttu-id="14d31-202">**Kulude väärtuse** väljal olevad summad summeeritakse automaatselt kõigi ajatabeli ridade osas ja lisatakse mis tahes muudele summadele väljal **Kulu** **seotud toimingute** lehel.</span><span class="sxs-lookup"><span data-stu-id="14d31-202">The amount in the **Cost** field is summed for all timesheet lines and added to any other amounts in the **Cost** field on the **Related operations** page.</span></span>

## <a name="add-a-correction-to-a-nonconformance"></a><span data-ttu-id="14d31-203">Mittevastavusele paranduste lisamine</span><span class="sxs-lookup"><span data-stu-id="14d31-203">Add a correction to a nonconformance</span></span>

<span data-ttu-id="14d31-204">Mittevastavusele paranduse lisamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="14d31-204">To add a correction to a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="14d31-205">Avage **Varude haldus \> Perioodilised ülesanded \> Kvaliteedijuhtimine \> Mittevastavused**.</span><span class="sxs-lookup"><span data-stu-id="14d31-205">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="14d31-206">Leidke ja valige loendist mittevastavus, mille soovite uuendada.</span><span class="sxs-lookup"><span data-stu-id="14d31-206">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="14d31-207">Saate lisada paranduse ainult kinnitatud mittevastavustele.</span><span class="sxs-lookup"><span data-stu-id="14d31-207">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="14d31-208">Valige toimingupaanil suvand **Parandused**.</span><span class="sxs-lookup"><span data-stu-id="14d31-208">On the Action Pane, select **Corrections**.</span></span>
1. <span data-ttu-id="14d31-209">Valige tegevuspaanil suvand **Uus**, et lisada rida jaotise **Parandused** tabelisse.</span><span class="sxs-lookup"><span data-stu-id="14d31-209">On the **Corrections** page, on the Action Pane, select **New** to add a row to the grid.</span></span> <span data-ttu-id="14d31-210">Seejärel määrake uuel real järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="14d31-210">Then set the following fields for the new row:</span></span>

    - <span data-ttu-id="14d31-211">**Diagnostika** – valige diagnostika tüüp, mis tuvastab parandustüübi, mida loote.</span><span class="sxs-lookup"><span data-stu-id="14d31-211">**Diagnostic** – Select the diagnostic type that identifies the type of correction that you're creating.</span></span>
    - <span data-ttu-id="14d31-212">**Töötaja** – valige paranduse eest vastutav isik.</span><span class="sxs-lookup"><span data-stu-id="14d31-212">**Worker** – Select the person who is responsible for the correction.</span></span>
    - <span data-ttu-id="14d31-213">**Paranduse prioriteet** – valige suvand, et näidata, kuidas parandust prioriteerida (*Madal*, *Tavaline* või *Kõrge*).</span><span class="sxs-lookup"><span data-stu-id="14d31-213">**Correction priority** – Select an option to indicate how the correction should be prioritized (*Low*, *Normal*, or *High*).</span></span>
    - <span data-ttu-id="14d31-214">**Nõutav kuupäev** – sisestage kuupäev, millal parandustegevust taotleti.</span><span class="sxs-lookup"><span data-stu-id="14d31-214">**Requested date** – Enter the date when the corrective action was requested.</span></span>
    - <span data-ttu-id="14d31-215">**Planeeritud kuupäev** – sisestage kuupäev, millal parandus eeldatavalt viiakse lõpule.</span><span class="sxs-lookup"><span data-stu-id="14d31-215">**Planned date** – Enter the date when the correction is expected to be completed.</span></span>
    - <span data-ttu-id="14d31-216">**Lühiajaline lahendus** – märkige see ruut, kui parandustegevus parandab mittevastavuse ainult lühikese aja jooksul.</span><span class="sxs-lookup"><span data-stu-id="14d31-216">**Short term solution** – Select this check box if the corrective action corrects the nonconformance only for a short time.</span></span>

1. <span data-ttu-id="14d31-217">Sulgege lehed.</span><span class="sxs-lookup"><span data-stu-id="14d31-217">Close the pages.</span></span>

## <a name="mark-a-correction-as-completed"></a><span data-ttu-id="14d31-218">Paranduse lõpetatuks märkimine</span><span class="sxs-lookup"><span data-stu-id="14d31-218">Mark a correction as completed</span></span>

<span data-ttu-id="14d31-219">Mittevastavuse paranduse lõpetatuks märkimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="14d31-219">To mark a nonconformance correction as completed, follow these steps.</span></span>

1. <span data-ttu-id="14d31-220">Avage **Varude haldus \> Perioodilised ülesanded \> Kvaliteedijuhtimine \> Mittevastavused**.</span><span class="sxs-lookup"><span data-stu-id="14d31-220">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="14d31-221">Leidke ja valige loendist mittevastavus, mille soovite uuendada.</span><span class="sxs-lookup"><span data-stu-id="14d31-221">In the list, select the nonconformance that you want to update.</span></span>

    > [!NOTE]
    > <span data-ttu-id="14d31-222">Saate lisada paranduse ainult kinnitatud mittevastavustele.</span><span class="sxs-lookup"><span data-stu-id="14d31-222">You can add a correction only to nonconformances that are approved.</span></span>

1. <span data-ttu-id="14d31-223">Valige toimingupaanil suvand **Parandused**.</span><span class="sxs-lookup"><span data-stu-id="14d31-223">On the Action Pane, select **Corrections**.</span></span>
1. <span data-ttu-id="14d31-224">Lehel **Parandused**, ruudustikus, valige parandus, mida tahate märkida lõpetatuks.</span><span class="sxs-lookup"><span data-stu-id="14d31-224">On the **Corrections** page, in the grid, select the correction that you want to mark as completed.</span></span>
1. <span data-ttu-id="14d31-225">Toimingupaanil valige **Märgi lõpetatuks**.</span><span class="sxs-lookup"><span data-stu-id="14d31-225">On the Action Pane, select **Mark complete**.</span></span>
1. <span data-ttu-id="14d31-226">Kui teil palutakse tegevus kinnitada, kinnitage oma valik.</span><span class="sxs-lookup"><span data-stu-id="14d31-226">You're prompted to confirm your selection.</span></span> <span data-ttu-id="14d31-227">Jätkamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="14d31-227">Select **OK** to continue.</span></span> <span data-ttu-id="14d31-228">Väli **Lõpetamise kuupäev ja kellaaeg** seatakse praegusele kuupäevale ja kellaajale ning ruut **Lõpetatud** on märgitud.</span><span class="sxs-lookup"><span data-stu-id="14d31-228">The **Completion date and time** field is set to the current date and time, and the **Completed** check box is selected.</span></span>
1. <span data-ttu-id="14d31-229">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="14d31-229">Close the page.</span></span>

## <a name="reopen-a-completed-correction"></a><span data-ttu-id="14d31-230">Lõpetatuks märgitud paranduse uuesti avamine</span><span class="sxs-lookup"><span data-stu-id="14d31-230">Reopen a completed correction</span></span>

<span data-ttu-id="14d31-231">Lõpetatud paranduse uuesti avamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="14d31-231">To reopen a completed correction, follow these steps.</span></span>

1. <span data-ttu-id="14d31-232">Avage **Varude haldus \> Perioodilised ülesanded \> Kvaliteedijuhtimine \> Mittevastavused**.</span><span class="sxs-lookup"><span data-stu-id="14d31-232">Go to **Inventory management \> Periodic tasks \> Quality management \> Non conformances**.</span></span>
1. <span data-ttu-id="14d31-233">Leidke ja valige loendist mittevastavus, mille soovite uuendada.</span><span class="sxs-lookup"><span data-stu-id="14d31-233">In the list, select the nonconformance that you want to update.</span></span>
1. <span data-ttu-id="14d31-234">Valige toimingupaanil suvand **Parandused**.</span><span class="sxs-lookup"><span data-stu-id="14d31-234">On the Action pane, select **Corrections**.</span></span>
1. <span data-ttu-id="14d31-235">Valige **Parandus** ruudustikus leheküljel Parandused, mille soovite uuesti avada.</span><span class="sxs-lookup"><span data-stu-id="14d31-235">On the **Corrections** page, in the grid, select the correction that you want to reopen.</span></span>
1. <span data-ttu-id="14d31-236">Toimingupaanil valige käsk **Uuesti avamine**.</span><span class="sxs-lookup"><span data-stu-id="14d31-236">On the Action Pane, select **Reopen**.</span></span>
1. <span data-ttu-id="14d31-237">Kui teil palutakse tegevus kinnitada, kinnitage oma valik.</span><span class="sxs-lookup"><span data-stu-id="14d31-237">You're prompted to confirm your selection.</span></span> <span data-ttu-id="14d31-238">Jätkamiseks valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="14d31-238">Select **OK** to continue.</span></span> <span data-ttu-id="14d31-239">Väärtus tühjendatakse **väljalt Lõpetamise kuupäev** ja kellaaeg ning märkeruut **Lõpetatud** tühjendatakse.</span><span class="sxs-lookup"><span data-stu-id="14d31-239">The value is cleared from the **Completion date and time** field, and the **Completed** check box is cleared.</span></span>
1. <span data-ttu-id="14d31-240">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="14d31-240">Close the page.</span></span>

<span data-ttu-id="14d31-241">Nüüd saate parandusse teha täiendavaid muudatusi või uuendusi.</span><span class="sxs-lookup"><span data-stu-id="14d31-241">You can now make additional edits or updates to the correction.</span></span> <span data-ttu-id="14d31-242">Kui olete parandusega lõpetanud, saate paranduse uuesti lõpetatuks märkida.</span><span class="sxs-lookup"><span data-stu-id="14d31-242">When you've finished, you can mark the correction as completed again.</span></span>

## <a name="close-a-nonconformance"></a><span data-ttu-id="14d31-243">Mittevastavuse sulgemine</span><span class="sxs-lookup"><span data-stu-id="14d31-243">Close a nonconformance</span></span>

<span data-ttu-id="14d31-244">Mittevastavuse sulgemiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="14d31-244">To close a nonconformance, follow these steps.</span></span>

1. <span data-ttu-id="14d31-245">Avage **Varude haldus \> Perioodilised ülesanded \> Kvaliteedijuhtimine \> Kvaliteettellimused**.</span><span class="sxs-lookup"><span data-stu-id="14d31-245">Go to **Inventory management \> Periodic tasks \> Quality management \> Quality orders**.</span></span>
1. <span data-ttu-id="14d31-246">Valige ruudustikust kvaliteettellimus.</span><span class="sxs-lookup"><span data-stu-id="14d31-246">Select a quality order in the grid.</span></span>
1. <span data-ttu-id="14d31-247">Valige toimingupaanilt **Päringud \> Mittevastavused**.</span><span class="sxs-lookup"><span data-stu-id="14d31-247">On the Action Pane, select **Inquiries \> Non conformances**.</span></span>
1. <span data-ttu-id="14d31-248">Valige lehel **Mittevastavused** ruudustikust sihtmärgi mittevastavus.</span><span class="sxs-lookup"><span data-stu-id="14d31-248">On the **Non conformances** page, select the target nonconformance in the grid.</span></span>
1. <span data-ttu-id="14d31-249">Valige tegevuspaanil suvand **Funktsioonid \> Sulge mittevastavus**.</span><span class="sxs-lookup"><span data-stu-id="14d31-249">On the Action Pane, select **Functions \> Close non conformance**.</span></span>
1. <span data-ttu-id="14d31-250">Kui teil palutakse tegevus kinnitada, kinnitage oma valik.</span><span class="sxs-lookup"><span data-stu-id="14d31-250">You're prompted to confirm your selection.</span></span> <span data-ttu-id="14d31-251">Jätkamiseks valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="14d31-251">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="14d31-252">Sulgege lehed.</span><span class="sxs-lookup"><span data-stu-id="14d31-252">Close the pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="14d31-253">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="14d31-253">Additional resources</span></span>

- [<span data-ttu-id="14d31-254">Kvaliteedijuhtimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="14d31-254">Quality management overview</span></span>](../quality-management-processes.md)
- [<span data-ttu-id="14d31-255">Kvaliteedi ja mittevastavuse haldamise lubamine</span><span class="sxs-lookup"><span data-stu-id="14d31-255">Enable quality and nonconformance management</span></span>](../enable-quality-management.md)
- [<span data-ttu-id="14d31-256">Mittevastavuste kinnitamise eest vastutavad töötajad</span><span class="sxs-lookup"><span data-stu-id="14d31-256">Workers responsible for approving nonconformances</span></span>](../quality-responsible-workers.md)
- [<span data-ttu-id="14d31-257">Mittevastavuste vahelao tsoonid</span><span class="sxs-lookup"><span data-stu-id="14d31-257">Quarantine zones for nonconformances</span></span>](../quality-quarantine-zones.md)
- [<span data-ttu-id="14d31-258">Mittevastavuste diagnostika tüübid</span><span class="sxs-lookup"><span data-stu-id="14d31-258">Diagnostic types for nonconformances</span></span>](../quality-diagnostic-types.md)
- [<span data-ttu-id="14d31-259">Kvaliteeditasud mittevastavustele</span><span class="sxs-lookup"><span data-stu-id="14d31-259">Quality charges for nonconformances</span></span>](../quality-charges.md)
- [<span data-ttu-id="14d31-260">Operatsioonid mittevastavusele</span><span class="sxs-lookup"><span data-stu-id="14d31-260">Operations for nonconformances</span></span>](../quality-operations.md)
- [<span data-ttu-id="14d31-261">Laoprotsesside kvaliteedijuhtimine</span><span class="sxs-lookup"><span data-stu-id="14d31-261">Quality management for warehouse processes</span></span>](../quality-management-for-warehouses-processes.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
