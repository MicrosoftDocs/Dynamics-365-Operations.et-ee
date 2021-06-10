---
title: Warehouse Management mobiilirakendusele astmeikoonide ja pealkirjade määramine
description: See teema kirjeldab, kuidas määrata Warehouse Management mobiilirakenduses uute või kohandatud ülesandevoogude etapiikoonid ja pealkirjad.
author: MarkusFogelberg
ms.date: 05/17/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2021-05-17
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 9523492d766669e6c38579fba7b5ddd6b3d282fc
ms.sourcegitcommit: c53de2c09b9296b41653e739178edf29f79e0679
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/17/2021
ms.locfileid: "6049360"
---
# <a name="assign-step-icons-and-titles-for-the-warehouse-management-mobile-app"></a><span data-ttu-id="3ed42-103">Warehouse Management mobiilirakendusele astmeikoonide ja pealkirjade määramine</span><span class="sxs-lookup"><span data-stu-id="3ed42-103">Assign step icons and titles for the Warehouse Management mobile app</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3ed42-104">See teema kirjeldab, kuidas määrata Warehouse Management mobiilirakenduses uute või kohandatud ülesandevoogude etapiikoonid ja pealkirjad.</span><span class="sxs-lookup"><span data-stu-id="3ed42-104">This topic describes how to assign step icons and step titles for new or customized task flows for the Warehouse Management mobile app.</span></span>

<span data-ttu-id="3ed42-105">Järgmised illustratsioonid näitavad, kuidas etapiikoonid ja pealkirjad kuvatakse Warehouse Management mobiilirakenduses.</span><span class="sxs-lookup"><span data-stu-id="3ed42-105">The following illustrations shows how step icons and titles appear in the Warehouse Management mobile app.</span></span>

<span data-ttu-id="3ed42-106">![Warehouse Management mobiilirakenduse astmeikooni ja etapi pealkirja näide](media/step-icon-example.png "Warehouse Management mobiilirakenduse astmeikooni ja etapi pealkirja näide")</span><span class="sxs-lookup"><span data-stu-id="3ed42-106">![Example of a step icon and a step title in the Warehouse Management mobile app](media/step-icon-example.png "Example of a step icon and a step title in the Warehouse Management mobile app")</span></span>

## <a name="turn-on-this-feature-in-your-system"></a><span data-ttu-id="3ed42-107">Funktsiooni sisselülitamine teie süsteemis</span><span class="sxs-lookup"><span data-stu-id="3ed42-107">Turn on this feature in your system</span></span>

<span data-ttu-id="3ed42-108">Enne selle funktsiooni kasutamist peate selle oma süsteemis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="3ed42-108">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="3ed42-109">Administraatorid saavad kasutada [funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) sätteid, et kontrollida funktsiooni olekut ja selle sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="3ed42-109">Admins can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="3ed42-110">Tööruumis **Funktsioonihaldus** loetletakse funktsiooni järgneval viisil.</span><span class="sxs-lookup"><span data-stu-id="3ed42-110">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="3ed42-111">**Moodul:** *laohaldus*</span><span class="sxs-lookup"><span data-stu-id="3ed42-111">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="3ed42-112">**Funktsiooni nimi:** *uue laorakenduse kasutajasätted, ikoonid ja etapi pealkirjad*</span><span class="sxs-lookup"><span data-stu-id="3ed42-112">**Feature name:** *User settings, icons, and step titles for the new warehouse app*</span></span>

## <a name="standard-step-ids-classes-and-icons"></a><span data-ttu-id="3ed42-113">Standardsammude ID-d, klassid ja ikoonid</span><span class="sxs-lookup"><span data-stu-id="3ed42-113">Standard step IDs, classes, and icons</span></span>

<span data-ttu-id="3ed42-114">Iga samm ülesande voos tuvastatakse etapi ID järgi ja igal sammu ID-l on vastav astmeklass.</span><span class="sxs-lookup"><span data-stu-id="3ed42-114">Each step in a task flow is identified by a step ID, and each step ID has a corresponding step class.</span></span> <span data-ttu-id="3ed42-115">Sammu ikoon ja pealkiri määratakse igas astmeklassis.</span><span class="sxs-lookup"><span data-stu-id="3ed42-115">The step icon and title are specified in each step class.</span></span>

### <a name="step-ids-and-step-classes"></a><a name="step-ids-classes"></a><span data-ttu-id="3ed42-116">Sammu ID-d ja etapiklassid</span><span class="sxs-lookup"><span data-stu-id="3ed42-116">Step IDs and step classes</span></span>

<span data-ttu-id="3ed42-117">Järgmises tabelis loetletakse kõik praegu saadaolevad etapi ID-d ja see on vastav astmeklass.</span><span class="sxs-lookup"><span data-stu-id="3ed42-117">The following table lists every step ID that is currently available, and its corresponding step class.</span></span> <span data-ttu-id="3ed42-118">Peamise sisendvälja juhtelemendi nime kasutatakse astme ID-s.</span><span class="sxs-lookup"><span data-stu-id="3ed42-118">The control name of the primary input field is used as the step ID.</span></span>

<span data-ttu-id="3ed42-119">Näide, mis näitab, kuidas nende sammude ID-sid ja klasse kasutatakse `WHSMobileAppStepInfoBuilder.stepId()` meetodi rakendamist [näites: määrake selles teemas hiljem etapiikoonid ja pealkirjad kohandatud voo](#example) selgitatakse selles teemas hiljem.</span><span class="sxs-lookup"><span data-stu-id="3ed42-119">For an example that shows how these step IDs and classes are used, see the implementation of the `WHSMobileAppStepInfoBuilder.stepId()` method in the [Example: Assign step icons and titles for a custom flow](#example) section later in this topic.</span></span>

| <span data-ttu-id="3ed42-120">Sammu ID</span><span class="sxs-lookup"><span data-stu-id="3ed42-120">Step ID</span></span> | <span data-ttu-id="3ed42-121">Samm klass</span><span class="sxs-lookup"><span data-stu-id="3ed42-121">Step Class</span></span> |
|-|-|
| <span data-ttu-id="3ed42-122">PartiiPositsioon</span><span class="sxs-lookup"><span data-stu-id="3ed42-122">BatchDisposition</span></span> | <span data-ttu-id="3ed42-123">WhSMobileAppStepBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="3ed42-123">WHSMobileAppStepBatchDisposition</span></span> |
| <span data-ttu-id="3ed42-124">Vedaja</span><span class="sxs-lookup"><span data-stu-id="3ed42-124">Carrier</span></span> | <span data-ttu-id="3ed42-125">WhSMobileAppStepCarrier</span><span class="sxs-lookup"><span data-stu-id="3ed42-125">WHSMobileAppStepCarrier</span></span> |
| <span data-ttu-id="3ed42-126">Tegelikkaal</span><span class="sxs-lookup"><span data-stu-id="3ed42-126">CatchWeight</span></span> | <span data-ttu-id="3ed42-127">WhSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="3ed42-127">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="3ed42-128">CatchWeightQtyOutboundWeight</span><span class="sxs-lookup"><span data-stu-id="3ed42-128">CatchWeightQtyOutboundWeight</span></span> | <span data-ttu-id="3ed42-129">WhSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="3ed42-129">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="3ed42-130">Tegelikukaalusilt</span><span class="sxs-lookup"><span data-stu-id="3ed42-130">CatchWeightTag</span></span> | <span data-ttu-id="3ed42-131">WhSMobileAppStepCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="3ed42-131">WHSMobileAppStepCatchWeightTag</span></span> |
| <span data-ttu-id="3ed42-132">CatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="3ed42-132">CatchWeightTagWeight</span></span> | <span data-ttu-id="3ed42-133">WhSMobileAppStepCatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="3ed42-133">WHSMobileAppStepCatchWeightTagWeight</span></span> |
| <span data-ttu-id="3ed42-134">ChangeWarekodaSuccess</span><span class="sxs-lookup"><span data-stu-id="3ed42-134">ChangeWarehouseSuccess</span></span> | <span data-ttu-id="3ed42-135">WHSMobileAppStepChangeWarekodaSuccess</span><span class="sxs-lookup"><span data-stu-id="3ed42-135">WHSMobileAppStepChangeWarehouseSuccess</span></span> |
| <span data-ttu-id="3ed42-136">Kontrollnumber</span><span class="sxs-lookup"><span data-stu-id="3ed42-136">CheckDigit</span></span> | <span data-ttu-id="3ed42-137">WhSMobileAppStepCheckDigit</span><span class="sxs-lookup"><span data-stu-id="3ed42-137">WHSMobileAppStepCheckDigit</span></span> |
| <span data-ttu-id="3ed42-138">KlastedId</span><span class="sxs-lookup"><span data-stu-id="3ed42-138">ClusterId</span></span> | <span data-ttu-id="3ed42-139">WhSMobileAppStepClusterId</span><span class="sxs-lookup"><span data-stu-id="3ed42-139">WHSMobileAppStepClusterId</span></span> |
| <span data-ttu-id="3ed42-140">ClusterPickQtyVerification</span><span class="sxs-lookup"><span data-stu-id="3ed42-140">ClusterPickQtyVerification</span></span> | <span data-ttu-id="3ed42-141">WhSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="3ed42-141">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="3ed42-142">Klastripositsioon</span><span class="sxs-lookup"><span data-stu-id="3ed42-142">ClusterPosition</span></span> | <span data-ttu-id="3ed42-143">WHSMobileAppStepClusterPosition</span><span class="sxs-lookup"><span data-stu-id="3ed42-143">WHSMobileAppStepClusterPosition</span></span> |
| <span data-ttu-id="3ed42-144">KonfiguratsiooniId</span><span class="sxs-lookup"><span data-stu-id="3ed42-144">ConfigId</span></span> | <span data-ttu-id="3ed42-145">WHSMobileAppStepConfigId</span><span class="sxs-lookup"><span data-stu-id="3ed42-145">WHSMobileAppStepConfigId</span></span> |
| <span data-ttu-id="3ed42-146">Kinnitus</span><span class="sxs-lookup"><span data-stu-id="3ed42-146">Confirmation</span></span> | <span data-ttu-id="3ed42-147">WHSMobileAppStepConfirmation</span><span class="sxs-lookup"><span data-stu-id="3ed42-147">WHSMobileAppStepConfirmation</span></span> |
| <span data-ttu-id="3ed42-148">KonsolideerimineLitsentseeritudPlaat</span><span class="sxs-lookup"><span data-stu-id="3ed42-148">ConsolidateFromLicensePlateId</span></span> | <span data-ttu-id="3ed42-149">WhSMobileAppStepConsolidateFromLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="3ed42-149">WHSMobileAppStepConsolidateFromLicensePlateId</span></span> |
| <span data-ttu-id="3ed42-150">KonsolideeritudLPCKinnitus</span><span class="sxs-lookup"><span data-stu-id="3ed42-150">ConsolidateLPConfirmation</span></span> | <span data-ttu-id="3ed42-151">WHSMobileAppStepConsolidateLPConfirmation</span><span class="sxs-lookup"><span data-stu-id="3ed42-151">WHSMobileAppStepConsolidateLPConfirmation</span></span> |
| <span data-ttu-id="3ed42-152">KonsolideerimineLitsentseeritudPlaat</span><span class="sxs-lookup"><span data-stu-id="3ed42-152">ConsolidateToLicensePlateId</span></span> | <span data-ttu-id="3ed42-153">WhSMobileAppStepConsolidateToLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="3ed42-153">WHSMobileAppStepConsolidateToLicensePlateId</span></span> |
| <span data-ttu-id="3ed42-154">Konteineritüüp</span><span class="sxs-lookup"><span data-stu-id="3ed42-154">ContainerType</span></span> | <span data-ttu-id="3ed42-155">WHSMobileAppStepContainerType</span><span class="sxs-lookup"><span data-stu-id="3ed42-155">WHSMobileAppStepContainerType</span></span> |
| <span data-ttu-id="3ed42-156">ArvestusePõhjusKood</span><span class="sxs-lookup"><span data-stu-id="3ed42-156">CountingReasonCode</span></span> | <span data-ttu-id="3ed42-157">WHSMobileAppStepCountingReasonCode</span><span class="sxs-lookup"><span data-stu-id="3ed42-157">WHSMobileAppStepCountingReasonCode</span></span> |
| <span data-ttu-id="3ed42-158">CycleCountingAddLPOrFinish</span><span class="sxs-lookup"><span data-stu-id="3ed42-158">CycleCountingAddLPOrFinish</span></span> | <span data-ttu-id="3ed42-159">WhSMobileAppStepCycleCountingAddLPOrFinish</span><span class="sxs-lookup"><span data-stu-id="3ed42-159">WHSMobileAppStepCycleCountingAddLPOrFinish</span></span> |
| <span data-ttu-id="3ed42-160">CycleCountQty1</span><span class="sxs-lookup"><span data-stu-id="3ed42-160">CycleCountQty1</span></span> | <span data-ttu-id="3ed42-161">WhSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="3ed42-161">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="3ed42-162">CycleCountQty2</span><span class="sxs-lookup"><span data-stu-id="3ed42-162">CycleCountQty2</span></span> | <span data-ttu-id="3ed42-163">WhSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="3ed42-163">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="3ed42-164">CycleCountQty3</span><span class="sxs-lookup"><span data-stu-id="3ed42-164">CycleCountQty3</span></span> | <span data-ttu-id="3ed42-165">WhSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="3ed42-165">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="3ed42-166">CycleCountQty4</span><span class="sxs-lookup"><span data-stu-id="3ed42-166">CycleCountQty4</span></span> | <span data-ttu-id="3ed42-167">WhSMobileAppStepCycleCountQty</span><span class="sxs-lookup"><span data-stu-id="3ed42-167">WHSMobileAppStepCycleCountQty</span></span> |
| <span data-ttu-id="3ed42-168">Likvideerimine</span><span class="sxs-lookup"><span data-stu-id="3ed42-168">Disposition</span></span> | <span data-ttu-id="3ed42-169">WHSMobileAppStepDisposition</span><span class="sxs-lookup"><span data-stu-id="3ed42-169">WHSMobileAppStepDisposition</span></span> |
| <span data-ttu-id="3ed42-170">DriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="3ed42-170">DriverCheckInConfirmation</span></span> | <span data-ttu-id="3ed42-171">WHSMobileAppStepDriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="3ed42-171">WHSMobileAppStepDriverCheckInConfirmation</span></span> |
| <span data-ttu-id="3ed42-172">DriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="3ed42-172">DriverCheckInId</span></span> | <span data-ttu-id="3ed42-173">WHSMobileAppStepDriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="3ed42-173">WHSMobileAppStepDriverCheckInId</span></span> |
| <span data-ttu-id="3ed42-174">DriverCheckOutConfirmation</span><span class="sxs-lookup"><span data-stu-id="3ed42-174">DriverCheckOutConfirmation</span></span> | <span data-ttu-id="3ed42-175">WHSMobileAppStepDriverCheckOutConfirmation</span><span class="sxs-lookup"><span data-stu-id="3ed42-175">WHSMobileAppStepDriverCheckOutConfirmation</span></span> |
| <span data-ttu-id="3ed42-176">SõitjaVäljaregamiseId</span><span class="sxs-lookup"><span data-stu-id="3ed42-176">DriverCheckOutId</span></span> | <span data-ttu-id="3ed42-177">WHSMobileAppStepDriverCheckOutId</span><span class="sxs-lookup"><span data-stu-id="3ed42-177">WHSMobileAppStepDriverCheckOutId</span></span> |
| <span data-ttu-id="3ed42-178">Aegumiskuupäev</span><span class="sxs-lookup"><span data-stu-id="3ed42-178">ExpDate</span></span> | <span data-ttu-id="3ed42-179">WhSMobileAppStepExpDate</span><span class="sxs-lookup"><span data-stu-id="3ed42-179">WHSMobileAppStepExpDate</span></span> |
| <span data-ttu-id="3ed42-180">PartiiLikvideerimine</span><span class="sxs-lookup"><span data-stu-id="3ed42-180">FromBatchDisposition</span></span> | <span data-ttu-id="3ed42-181">WHSMobileAppStepFromBatchDisposition</span><span class="sxs-lookup"><span data-stu-id="3ed42-181">WHSMobileAppStepFromBatchDisposition</span></span> |
| <span data-ttu-id="3ed42-182">VarudeOlek</span><span class="sxs-lookup"><span data-stu-id="3ed42-182">FromInventoryStatus</span></span> | <span data-ttu-id="3ed42-183">WhSMobileAppStepInventoryStatusFrom</span><span class="sxs-lookup"><span data-stu-id="3ed42-183">WHSMobileAppStepInventoryStatusFrom</span></span> |
| <span data-ttu-id="3ed42-184">TäisKogus</span><span class="sxs-lookup"><span data-stu-id="3ed42-184">FullQty</span></span> | <span data-ttu-id="3ed42-185">WhSMobileAppStepFullQty</span><span class="sxs-lookup"><span data-stu-id="3ed42-185">WHSMobileAppStepFullQty</span></span> |
| <span data-ttu-id="3ed42-186">SissetuleOsa</span><span class="sxs-lookup"><span data-stu-id="3ed42-186">InboundPut</span></span> | <span data-ttu-id="3ed42-187">WhSMobileAppStepInboundPut</span><span class="sxs-lookup"><span data-stu-id="3ed42-187">WHSMobileAppStepInboundPut</span></span> |
| <span data-ttu-id="3ed42-188">InventariPartiiId</span><span class="sxs-lookup"><span data-stu-id="3ed42-188">InventBatchId</span></span> | <span data-ttu-id="3ed42-189">WhSMobileAppStepBatch</span><span class="sxs-lookup"><span data-stu-id="3ed42-189">WHSMobileAppStepBatch</span></span> |
| <span data-ttu-id="3ed42-190">InventuuriVärviId</span><span class="sxs-lookup"><span data-stu-id="3ed42-190">InventColorId</span></span> | <span data-ttu-id="3ed42-191">WhSMobileAppStepInventColorId</span><span class="sxs-lookup"><span data-stu-id="3ed42-191">WHSMobileAppStepInventColorId</span></span> |
| <span data-ttu-id="3ed42-192">VarudeAsukoht</span><span class="sxs-lookup"><span data-stu-id="3ed42-192">InventLocation</span></span> | <span data-ttu-id="3ed42-193">WHSMobileAppStepInventLocation</span><span class="sxs-lookup"><span data-stu-id="3ed42-193">WHSMobileAppStepInventLocation</span></span> |
| <span data-ttu-id="3ed42-194">VarudeAsukohtId</span><span class="sxs-lookup"><span data-stu-id="3ed42-194">InventLocationId</span></span> | <span data-ttu-id="3ed42-195">WHSMobileAppStepWarehouse</span><span class="sxs-lookup"><span data-stu-id="3ed42-195">WHSMobileAppStepWarehouse</span></span> |
| <span data-ttu-id="3ed42-196">InventSeeriaId</span><span class="sxs-lookup"><span data-stu-id="3ed42-196">InventSerialId</span></span> | <span data-ttu-id="3ed42-197">WHSMobileAppStepInventSerialId</span><span class="sxs-lookup"><span data-stu-id="3ed42-197">WHSMobileAppStepInventSerialId</span></span> |
| <span data-ttu-id="3ed42-198">VaruSuuruseId</span><span class="sxs-lookup"><span data-stu-id="3ed42-198">InventSizeId</span></span> | <span data-ttu-id="3ed42-199">WHSMobileAppStepInventSizeId</span><span class="sxs-lookup"><span data-stu-id="3ed42-199">WHSMobileAppStepInventSizeId</span></span> |
| <span data-ttu-id="3ed42-200">VaruSeisId</span><span class="sxs-lookup"><span data-stu-id="3ed42-200">InventStatusId</span></span> | <span data-ttu-id="3ed42-201">WHSMobileAppStepInventStatus</span><span class="sxs-lookup"><span data-stu-id="3ed42-201">WHSMobileAppStepInventStatus</span></span> |
| <span data-ttu-id="3ed42-202">VaruStiilId</span><span class="sxs-lookup"><span data-stu-id="3ed42-202">InventStyleId</span></span> | <span data-ttu-id="3ed42-203">WHSMobileAppStepInventStyleId</span><span class="sxs-lookup"><span data-stu-id="3ed42-203">WHSMobileAppStepInventStyleId</span></span> |
| <span data-ttu-id="3ed42-204">VaruVersioonId</span><span class="sxs-lookup"><span data-stu-id="3ed42-204">InventVersionId</span></span> | <span data-ttu-id="3ed42-205">WHSMobileAppStepInventVersionId</span><span class="sxs-lookup"><span data-stu-id="3ed42-205">WHSMobileAppStepInventVersionId</span></span> |
| <span data-ttu-id="3ed42-206">ItemId</span><span class="sxs-lookup"><span data-stu-id="3ed42-206">ItemId</span></span> | <span data-ttu-id="3ed42-207">WHSMobileAppStepItem</span><span class="sxs-lookup"><span data-stu-id="3ed42-207">WHSMobileAppStepItem</span></span> |
| <span data-ttu-id="3ed42-208">ITMSisuID</span><span class="sxs-lookup"><span data-stu-id="3ed42-208">ITMContainerID</span></span> | <span data-ttu-id="3ed42-209">ITMMobileAppStepContainerId</span><span class="sxs-lookup"><span data-stu-id="3ed42-209">ITMMobileAppStepContainerId</span></span> |
| <span data-ttu-id="3ed42-210">ITMSaatmisID</span><span class="sxs-lookup"><span data-stu-id="3ed42-210">ITMShipmentID</span></span> | <span data-ttu-id="3ed42-211">ITMMobileAppStepShipmentId</span><span class="sxs-lookup"><span data-stu-id="3ed42-211">ITMMobileAppStepShipmentId</span></span> |
| <span data-ttu-id="3ed42-212">KanbanCardId</span><span class="sxs-lookup"><span data-stu-id="3ed42-212">KanbanCardId</span></span> | <span data-ttu-id="3ed42-213">WHSMobileAppStepKanbanCard</span><span class="sxs-lookup"><span data-stu-id="3ed42-213">WHSMobileAppStepKanbanCard</span></span> |
| <span data-ttu-id="3ed42-214">KanbanCardToEmpty</span><span class="sxs-lookup"><span data-stu-id="3ed42-214">KanbanCardToEmpty</span></span> | <span data-ttu-id="3ed42-215">WHSMobileAppStepKanbanCardToEmpty</span><span class="sxs-lookup"><span data-stu-id="3ed42-215">WHSMobileAppStepKanbanCardToEmpty</span></span> |
| <span data-ttu-id="3ed42-216">KanbanVõiKaardiId</span><span class="sxs-lookup"><span data-stu-id="3ed42-216">KanbanOrCardId</span></span> | <span data-ttu-id="3ed42-217">WHSMobileAppStepKanbanCard</span><span class="sxs-lookup"><span data-stu-id="3ed42-217">WHSMobileAppStepKanbanCard</span></span> |
| <span data-ttu-id="3ed42-218">LitsentsPlateId</span><span class="sxs-lookup"><span data-stu-id="3ed42-218">LicensePlateId</span></span> | <span data-ttu-id="3ed42-219">WhSMobileAppStepLicensePlate</span><span class="sxs-lookup"><span data-stu-id="3ed42-219">WHSMobileAppStepLicensePlate</span></span> |
| <span data-ttu-id="3ed42-220">KoormaId</span><span class="sxs-lookup"><span data-stu-id="3ed42-220">LoadId</span></span> | <span data-ttu-id="3ed42-221">WHSMobileAppStepLoadId</span><span class="sxs-lookup"><span data-stu-id="3ed42-221">WHSMobileAppStepLoadId</span></span> |
| <span data-ttu-id="3ed42-222">AsukohaLitsentsiPlaadiPaigutus</span><span class="sxs-lookup"><span data-stu-id="3ed42-222">LocationLicensePlatePosition</span></span> | <span data-ttu-id="3ed42-223">WHSMobileAppStepLocationLicensePlatePosition</span><span class="sxs-lookup"><span data-stu-id="3ed42-223">WHSMobileAppStepLocationLicensePlatePosition</span></span> |
| <span data-ttu-id="3ed42-224">LocOrLP</span><span class="sxs-lookup"><span data-stu-id="3ed42-224">LocOrLP</span></span> | <span data-ttu-id="3ed42-225">WHSMobileAppStepLocOrLP</span><span class="sxs-lookup"><span data-stu-id="3ed42-225">WHSMobileAppStepLocOrLP</span></span> |
| <span data-ttu-id="3ed42-226">LocOrLP_From</span><span class="sxs-lookup"><span data-stu-id="3ed42-226">LocOrLP_From</span></span> | <span data-ttu-id="3ed42-227">WHSMobileAppStepLocOrLPFrom</span><span class="sxs-lookup"><span data-stu-id="3ed42-227">WHSMobileAppStepLocOrLPFrom</span></span> |
| <span data-ttu-id="3ed42-228">LocOrLP_To</span><span class="sxs-lookup"><span data-stu-id="3ed42-228">LocOrLP_To</span></span> | <span data-ttu-id="3ed42-229">WHSMobileAppStepLocOrLPTo</span><span class="sxs-lookup"><span data-stu-id="3ed42-229">WHSMobileAppStepLocOrLPTo</span></span> |
| <span data-ttu-id="3ed42-230">LocOrLPcheck</span><span class="sxs-lookup"><span data-stu-id="3ed42-230">LocOrLPCheck</span></span> | <span data-ttu-id="3ed42-231">WHSMobileAppStepLocOrLPCheck</span><span class="sxs-lookup"><span data-stu-id="3ed42-231">WHSMobileAppStepLocOrLPCheck</span></span> |
| <span data-ttu-id="3ed42-232">KohalikKinnitus</span><span class="sxs-lookup"><span data-stu-id="3ed42-232">LocVerification</span></span> | <span data-ttu-id="3ed42-233">WHSMobileAppStepLocVerification</span><span class="sxs-lookup"><span data-stu-id="3ed42-233">WHSMobileAppStepLocVerification</span></span> |
| <span data-ttu-id="3ed42-234">LPAdjustIn</span><span class="sxs-lookup"><span data-stu-id="3ed42-234">LPAdjustIn</span></span> | <span data-ttu-id="3ed42-235">WhSMobileAppStepLPAdjustIn</span><span class="sxs-lookup"><span data-stu-id="3ed42-235">WHSMobileAppStepLPAdjustIn</span></span> |
| <span data-ttu-id="3ed42-236">LPLapseKindelLP</span><span class="sxs-lookup"><span data-stu-id="3ed42-236">LPBreakChildLP</span></span> | <span data-ttu-id="3ed42-237">WhSMobileAppStepLPBreakChildLP</span><span class="sxs-lookup"><span data-stu-id="3ed42-237">WHSMobileAppStepLPBreakChildLP</span></span> |
| <span data-ttu-id="3ed42-238">LPVanemaKindelLP</span><span class="sxs-lookup"><span data-stu-id="3ed42-238">LPBreakParentLP</span></span> | <span data-ttu-id="3ed42-239">WHSMobileAppStepLPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="3ed42-239">WHSMobileAppStepLPBreakParentLP</span></span> |
| <span data-ttu-id="3ed42-240">LPEhitaLapsLP</span><span class="sxs-lookup"><span data-stu-id="3ed42-240">LPBuildChildLP</span></span> | <span data-ttu-id="3ed42-241">WHSMobileAppStepLPBuildChildLP</span><span class="sxs-lookup"><span data-stu-id="3ed42-241">WHSMobileAppStepLPBuildChildLP</span></span> |
| <span data-ttu-id="3ed42-242">LPEhitaVanemLP</span><span class="sxs-lookup"><span data-stu-id="3ed42-242">LPBuildParentLP</span></span> | <span data-ttu-id="3ed42-243">WHSMobileAppStepLPBuildParentLP</span><span class="sxs-lookup"><span data-stu-id="3ed42-243">WHSMobileAppStepLPBuildParentLP</span></span> |
| <span data-ttu-id="3ed42-244">LPKinnitus</span><span class="sxs-lookup"><span data-stu-id="3ed42-244">LPVerification</span></span> | <span data-ttu-id="3ed42-245">WHSMobileAppStepLPVerification</span><span class="sxs-lookup"><span data-stu-id="3ed42-245">WHSMobileAppStepLPVerification</span></span> |
| <span data-ttu-id="3ed42-246">ÜhendatudKontainerId</span><span class="sxs-lookup"><span data-stu-id="3ed42-246">MergeContainerId</span></span> | <span data-ttu-id="3ed42-247">WHSMobileAppStepMergeContainerId</span><span class="sxs-lookup"><span data-stu-id="3ed42-247">WHSMobileAppStepMergeContainerId</span></span> |
| <span data-ttu-id="3ed42-248">SeagtudJoonNum</span><span class="sxs-lookup"><span data-stu-id="3ed42-248">MixedLPLineNum</span></span> | <span data-ttu-id="3ed42-249">WHSMobileAppStepMixedLPLineNum</span><span class="sxs-lookup"><span data-stu-id="3ed42-249">WHSMobileAppStepMixedLPLineNum</span></span> |
| <span data-ttu-id="3ed42-250">MobiiliSeadePäringSõnumKogumisIdentId</span><span class="sxs-lookup"><span data-stu-id="3ed42-250">MobileDeviceQueueMessageCollectionIdentifierId</span></span> | <span data-ttu-id="3ed42-251">WhSMobileAppStepSelectOrder</span><span class="sxs-lookup"><span data-stu-id="3ed42-251">WHSMobileAppStepSelectOrder</span></span> |
| <span data-ttu-id="3ed42-252">LiikumineKinnitusestLoobumine</span><span class="sxs-lookup"><span data-stu-id="3ed42-252">MovementConfirmCancel</span></span> | <span data-ttu-id="3ed42-253">WHSMobileAppStepMovementConfirmCancel</span><span class="sxs-lookup"><span data-stu-id="3ed42-253">WHSMobileAppStepMovementConfirmCancel</span></span> |
| <span data-ttu-id="3ed42-254">NewCaptureWeight</span><span class="sxs-lookup"><span data-stu-id="3ed42-254">NewCaptureWeight</span></span> | <span data-ttu-id="3ed42-255">WhSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="3ed42-255">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="3ed42-256">UusPäring</span><span class="sxs-lookup"><span data-stu-id="3ed42-256">NewQty</span></span> | <span data-ttu-id="3ed42-257">WHSMobileAppStepNewQty</span><span class="sxs-lookup"><span data-stu-id="3ed42-257">WHSMobileAppStepNewQty</span></span> |
| <span data-ttu-id="3ed42-258">VäljaminevKaaluKontrolliSilt</span><span class="sxs-lookup"><span data-stu-id="3ed42-258">OutboundCatchWeightTag</span></span> | <span data-ttu-id="3ed42-259">WhSMobileAppStepCatchWeightTag</span><span class="sxs-lookup"><span data-stu-id="3ed42-259">WHSMobileAppStepCatchWeightTag</span></span> |
| <span data-ttu-id="3ed42-260">VäljaminevVäljund</span><span class="sxs-lookup"><span data-stu-id="3ed42-260">OutboundPut</span></span> | <span data-ttu-id="3ed42-261">WHSMobileAppStepOutboundPut</span><span class="sxs-lookup"><span data-stu-id="3ed42-261">WHSMobileAppStepOutboundPut</span></span> |
| <span data-ttu-id="3ed42-262">VäljaminevKaal</span><span class="sxs-lookup"><span data-stu-id="3ed42-262">OutboundWeight</span></span> | <span data-ttu-id="3ed42-263">WhSMobileAppStepCatchWeight</span><span class="sxs-lookup"><span data-stu-id="3ed42-263">WHSMobileAppStepCatchWeight</span></span> |
| <span data-ttu-id="3ed42-264">KirjutaÜleUusAsukoht</span><span class="sxs-lookup"><span data-stu-id="3ed42-264">OverridePutNewLocation</span></span> | <span data-ttu-id="3ed42-265">WhSMobileAppStepOverridePutNewLocation</span><span class="sxs-lookup"><span data-stu-id="3ed42-265">WHSMobileAppStepOverridePutNewLocation</span></span> |
| <span data-ttu-id="3ed42-266">TükiPõhjalKinnitus</span><span class="sxs-lookup"><span data-stu-id="3ed42-266">PieceByPieceConfirmation</span></span> | <span data-ttu-id="3ed42-267">WhSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="3ed42-267">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="3ed42-268">PoReaNumber</span><span class="sxs-lookup"><span data-stu-id="3ed42-268">POLineNum</span></span> | <span data-ttu-id="3ed42-269">WHSMobileAppStepPOLineNum</span><span class="sxs-lookup"><span data-stu-id="3ed42-269">WHSMobileAppStepPOLineNum</span></span> |
| <span data-ttu-id="3ed42-270">PONum</span><span class="sxs-lookup"><span data-stu-id="3ed42-270">PONum</span></span> | <span data-ttu-id="3ed42-271">WHSMobileAppStepPONum</span><span class="sxs-lookup"><span data-stu-id="3ed42-271">WHSMobileAppStepPONum</span></span> |
| <span data-ttu-id="3ed42-272">AmetikohtTäis</span><span class="sxs-lookup"><span data-stu-id="3ed42-272">PositionFull</span></span> | <span data-ttu-id="3ed42-273">WHSMobileAppStepPositionFull</span><span class="sxs-lookup"><span data-stu-id="3ed42-273">WHSMobileAppStepPositionFull</span></span> |
| <span data-ttu-id="3ed42-274">AmetikohtTäisPäring</span><span class="sxs-lookup"><span data-stu-id="3ed42-274">PositionFullQty</span></span> | <span data-ttu-id="3ed42-275">WHSMobileAppStepPositionFullQty</span><span class="sxs-lookup"><span data-stu-id="3ed42-275">WHSMobileAppStepPositionFullQty</span></span> |
| <span data-ttu-id="3ed42-276">Sisaldus</span><span class="sxs-lookup"><span data-stu-id="3ed42-276">Potency</span></span> | <span data-ttu-id="3ed42-277">WHSMobileAppStepPotency</span><span class="sxs-lookup"><span data-stu-id="3ed42-277">WHSMobileAppStepPotency</span></span> |
| <span data-ttu-id="3ed42-278">PrinteriNimi</span><span class="sxs-lookup"><span data-stu-id="3ed42-278">PrinterName</span></span> | <span data-ttu-id="3ed42-279">WHSMobileAppStepPrinterName</span><span class="sxs-lookup"><span data-stu-id="3ed42-279">WHSMobileAppStepPrinterName</span></span> |
| <span data-ttu-id="3ed42-280">ProdId</span><span class="sxs-lookup"><span data-stu-id="3ed42-280">ProdId</span></span> | <span data-ttu-id="3ed42-281">WHSMobileAppStepProdId</span><span class="sxs-lookup"><span data-stu-id="3ed42-281">WHSMobileAppStepProdId</span></span> |
| <span data-ttu-id="3ed42-282">ProdViimanePlaatKinnitus</span><span class="sxs-lookup"><span data-stu-id="3ed42-282">ProdLastPalletConfirmation</span></span> | <span data-ttu-id="3ed42-283">WhSMobileAppStepProdLastPalletConfirmation</span><span class="sxs-lookup"><span data-stu-id="3ed42-283">WHSMobileAppStepProdLastPalletConfirmation</span></span> |
| <span data-ttu-id="3ed42-284">TooteKinnitus</span><span class="sxs-lookup"><span data-stu-id="3ed42-284">ProductConfirmation</span></span> | <span data-ttu-id="3ed42-285">WHSMobileAppStepProductConfirmation</span><span class="sxs-lookup"><span data-stu-id="3ed42-285">WHSMobileAppStepProductConfirmation</span></span> |
| <span data-ttu-id="3ed42-286">TootmisScrapKinnitus</span><span class="sxs-lookup"><span data-stu-id="3ed42-286">ProductionScrapConfirmation</span></span> | <span data-ttu-id="3ed42-287">WHSMobileAppStepProductionScrapConfirmation</span><span class="sxs-lookup"><span data-stu-id="3ed42-287">WHSMobileAppStepProductionScrapConfirmation</span></span> |
| <span data-ttu-id="3ed42-288">Pane</span><span class="sxs-lookup"><span data-stu-id="3ed42-288">Put</span></span> | <span data-ttu-id="3ed42-289">WHSMobileAppStepPut</span><span class="sxs-lookup"><span data-stu-id="3ed42-289">WHSMobileAppStepPut</span></span> |
| <span data-ttu-id="3ed42-290">KogumiteKlaster</span><span class="sxs-lookup"><span data-stu-id="3ed42-290">PutawayClusterId</span></span> | <span data-ttu-id="3ed42-291">WHSMobileAppStepPutawayClusterId</span><span class="sxs-lookup"><span data-stu-id="3ed42-291">WHSMobileAppStepPutawayClusterId</span></span> |
| <span data-ttu-id="3ed42-292">Kogus</span><span class="sxs-lookup"><span data-stu-id="3ed42-292">Qty</span></span> | <span data-ttu-id="3ed42-293">WHSMobileAppStepQty</span><span class="sxs-lookup"><span data-stu-id="3ed42-293">WHSMobileAppStepQty</span></span> |
| <span data-ttu-id="3ed42-294">KogusTäiendus</span><span class="sxs-lookup"><span data-stu-id="3ed42-294">QtyAdjust</span></span> | <span data-ttu-id="3ed42-295">WHSMobileAppStepQtyAdjust</span><span class="sxs-lookup"><span data-stu-id="3ed42-295">WHSMobileAppStepQtyAdjust</span></span> |
| <span data-ttu-id="3ed42-296">KogusLühike</span><span class="sxs-lookup"><span data-stu-id="3ed42-296">QtyShort</span></span> | <span data-ttu-id="3ed42-297">WHSMobileAppStepQtyShort</span><span class="sxs-lookup"><span data-stu-id="3ed42-297">WHSMobileAppStepQtyShort</span></span> |
| <span data-ttu-id="3ed42-298">KogusTarbima</span><span class="sxs-lookup"><span data-stu-id="3ed42-298">QtyToConsume</span></span> | <span data-ttu-id="3ed42-299">WhSMobileAppStepQtyToConsume</span><span class="sxs-lookup"><span data-stu-id="3ed42-299">WHSMobileAppStepQtyToConsume</span></span> |
| <span data-ttu-id="3ed42-300">KogusÜlesKorjama</span><span class="sxs-lookup"><span data-stu-id="3ed42-300">QtyToPick</span></span> | <span data-ttu-id="3ed42-301">WHSMobileAppStepQtyToPick</span><span class="sxs-lookup"><span data-stu-id="3ed42-301">WHSMobileAppStepQtyToPick</span></span> |
| <span data-ttu-id="3ed42-302">KogusVäljaMinev</span><span class="sxs-lookup"><span data-stu-id="3ed42-302">QtyToPut</span></span> | <span data-ttu-id="3ed42-303">WHSMobileAppStepQtyToPut</span><span class="sxs-lookup"><span data-stu-id="3ed42-303">WHSMobileAppStepQtyToPut</span></span> |
| <span data-ttu-id="3ed42-304">QtyToScrap</span><span class="sxs-lookup"><span data-stu-id="3ed42-304">QtyToScrap</span></span> | <span data-ttu-id="3ed42-305">WHSMobileAppStepQtyToScrap</span><span class="sxs-lookup"><span data-stu-id="3ed42-305">WHSMobileAppStepQtyToScrap</span></span> |
| <span data-ttu-id="3ed42-306">KogusKinnitus</span><span class="sxs-lookup"><span data-stu-id="3ed42-306">QtyVerification</span></span> | <span data-ttu-id="3ed42-307">WhSMobileAppStepQtyVerification</span><span class="sxs-lookup"><span data-stu-id="3ed42-307">WHSMobileAppStepQtyVerification</span></span> |
| <span data-ttu-id="3ed42-308">KogusValgeSkänningPiir</span><span class="sxs-lookup"><span data-stu-id="3ed42-308">QtyWithScanningLimit</span></span> | <span data-ttu-id="3ed42-309">WHSMobileAppStepQtyAdjust</span><span class="sxs-lookup"><span data-stu-id="3ed42-309">WHSMobileAppStepQtyAdjust</span></span> |
| <span data-ttu-id="3ed42-310">Põhjusestring</span><span class="sxs-lookup"><span data-stu-id="3ed42-310">ReasonString</span></span> | <span data-ttu-id="3ed42-311">WhSMobileAppStepReasonString</span><span class="sxs-lookup"><span data-stu-id="3ed42-311">WHSMobileAppStepReasonString</span></span> |
| <span data-ttu-id="3ed42-312">RecvAsukohaId</span><span class="sxs-lookup"><span data-stu-id="3ed42-312">RecvLocationId</span></span> | <span data-ttu-id="3ed42-313">WHSMobileAppStepRecvLocationId</span><span class="sxs-lookup"><span data-stu-id="3ed42-313">WHSMobileAppStepRecvLocationId</span></span> |
| <span data-ttu-id="3ed42-314">EemaldaContainerId</span><span class="sxs-lookup"><span data-stu-id="3ed42-314">RemoveContainerId</span></span> | <span data-ttu-id="3ed42-315">WHSMobileAppStepRemoveContainerId</span><span class="sxs-lookup"><span data-stu-id="3ed42-315">WHSMobileAppStepRemoveContainerId</span></span> |
| <span data-ttu-id="3ed42-316">UuestiprindiSildiKinnitus</span><span class="sxs-lookup"><span data-stu-id="3ed42-316">ReprintLabelConfirmation</span></span> | <span data-ttu-id="3ed42-317">WhSMobileAppStepReprintLabelConfirmation</span><span class="sxs-lookup"><span data-stu-id="3ed42-317">WHSMobileAppStepReprintLabelConfirmation</span></span> |
| <span data-ttu-id="3ed42-318">RMANum</span><span class="sxs-lookup"><span data-stu-id="3ed42-318">RMANum</span></span> | <span data-ttu-id="3ed42-319">WHSMobileAppStepRMANum</span><span class="sxs-lookup"><span data-stu-id="3ed42-319">WHSMobileAppStepRMANum</span></span> |
| <span data-ttu-id="3ed42-320">LühikeKorjePõhjus</span><span class="sxs-lookup"><span data-stu-id="3ed42-320">ShortPickReason</span></span> | <span data-ttu-id="3ed42-321">WhSMobileAppStepShortPickReason</span><span class="sxs-lookup"><span data-stu-id="3ed42-321">WHSMobileAppStepShortPickReason</span></span> |
| <span data-ttu-id="3ed42-322">LühikeKinnitusVõiLP</span><span class="sxs-lookup"><span data-stu-id="3ed42-322">SortConOrLP</span></span> | <span data-ttu-id="3ed42-323">WhSMobileAppStepSortConOrLP</span><span class="sxs-lookup"><span data-stu-id="3ed42-323">WHSMobileAppStepSortConOrLP</span></span> |
| <span data-ttu-id="3ed42-324">LühikeLitsentsPlateId</span><span class="sxs-lookup"><span data-stu-id="3ed42-324">SortLicensePlateId</span></span> | <span data-ttu-id="3ed42-325">WHSMobileAppStepSortLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="3ed42-325">WHSMobileAppStepSortLicensePlateId</span></span> |
| <span data-ttu-id="3ed42-326">LühikeAmetId</span><span class="sxs-lookup"><span data-stu-id="3ed42-326">SortPositionId</span></span> | <span data-ttu-id="3ed42-327">WHSMobileAppStepSortPositionId</span><span class="sxs-lookup"><span data-stu-id="3ed42-327">WHSMobileAppStepSortPositionId</span></span> |
| <span data-ttu-id="3ed42-328">SorteeriKinnitus</span><span class="sxs-lookup"><span data-stu-id="3ed42-328">SortVerification</span></span> | <span data-ttu-id="3ed42-329">WHSMobileAppStepSortVerification</span><span class="sxs-lookup"><span data-stu-id="3ed42-329">WHSMobileAppStepSortVerification</span></span> |
| <span data-ttu-id="3ed42-330">StartAsukohtId</span><span class="sxs-lookup"><span data-stu-id="3ed42-330">StartLocationId</span></span> | <span data-ttu-id="3ed42-331">WHSMobileAppStepStartLocationId</span><span class="sxs-lookup"><span data-stu-id="3ed42-331">WHSMobileAppStepStartLocationId</span></span> |
| <span data-ttu-id="3ed42-332">StartTooteTellimuseKinnitus</span><span class="sxs-lookup"><span data-stu-id="3ed42-332">StartProdOrderConfirmation</span></span> | <span data-ttu-id="3ed42-333">WhSMobileAppStepStartProdOrderConfirmation</span><span class="sxs-lookup"><span data-stu-id="3ed42-333">WHSMobileAppStepStartProdOrderConfirmation</span></span> |
| <span data-ttu-id="3ed42-334">EesmärkLitsentsPlateId</span><span class="sxs-lookup"><span data-stu-id="3ed42-334">TargetLicensePlateId</span></span> | <span data-ttu-id="3ed42-335">WHSMobileAppStepTargetLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="3ed42-335">WHSMobileAppStepTargetLicensePlateId</span></span> |
| <span data-ttu-id="3ed42-336">ReaNumber</span><span class="sxs-lookup"><span data-stu-id="3ed42-336">TOLineNum</span></span> | <span data-ttu-id="3ed42-337">WHSMobileAppStepTOLineNum</span><span class="sxs-lookup"><span data-stu-id="3ed42-337">WHSMobileAppStepTOLineNum</span></span> |
| <span data-ttu-id="3ed42-338">Asukohta</span><span class="sxs-lookup"><span data-stu-id="3ed42-338">ToLocation</span></span> | <span data-ttu-id="3ed42-339">WHSMobileAppStepToLocation</span><span class="sxs-lookup"><span data-stu-id="3ed42-339">WHSMobileAppStepToLocation</span></span> |
| <span data-ttu-id="3ed42-340">TONum</span><span class="sxs-lookup"><span data-stu-id="3ed42-340">TONum</span></span> | <span data-ttu-id="3ed42-341">WHSMobileAppStepTONum</span><span class="sxs-lookup"><span data-stu-id="3ed42-341">WHSMobileAppStepTONum</span></span> |
| <span data-ttu-id="3ed42-342">Lattu</span><span class="sxs-lookup"><span data-stu-id="3ed42-342">ToWarehouse</span></span> | <span data-ttu-id="3ed42-343">WHSMobileAppStepWarehouseTo</span><span class="sxs-lookup"><span data-stu-id="3ed42-343">WHSMobileAppStepWarehouseTo</span></span> |
| <span data-ttu-id="3ed42-344">TranspordiVaruId</span><span class="sxs-lookup"><span data-stu-id="3ed42-344">TransportLoadId</span></span> | <span data-ttu-id="3ed42-345">WhSMobileAppStepTransportLoadId</span><span class="sxs-lookup"><span data-stu-id="3ed42-345">WHSMobileAppStepTransportLoadId</span></span> |
| <span data-ttu-id="3ed42-346">VooSildiId</span><span class="sxs-lookup"><span data-stu-id="3ed42-346">WaveLabelId</span></span> | <span data-ttu-id="3ed42-347">WhSMobileAppStepWaveLabelId</span><span class="sxs-lookup"><span data-stu-id="3ed42-347">WHSMobileAppStepWaveLabelId</span></span> |
| <span data-ttu-id="3ed42-348">LaineLblQty</span><span class="sxs-lookup"><span data-stu-id="3ed42-348">WaveLblQty</span></span> | <span data-ttu-id="3ed42-349">WHSMobileAppStepWaveLblQty</span><span class="sxs-lookup"><span data-stu-id="3ed42-349">WHSMobileAppStepWaveLblQty</span></span> |
| <span data-ttu-id="3ed42-350">Kaal</span><span class="sxs-lookup"><span data-stu-id="3ed42-350">Weight</span></span> | <span data-ttu-id="3ed42-351">WHSMobileAppStepWeight</span><span class="sxs-lookup"><span data-stu-id="3ed42-351">WHSMobileAppStepWeight</span></span> |
| <span data-ttu-id="3ed42-352">KaalToConsume</span><span class="sxs-lookup"><span data-stu-id="3ed42-352">WeightToConsume</span></span> | <span data-ttu-id="3ed42-353">WHSMobileAppStepWeightToConsume</span><span class="sxs-lookup"><span data-stu-id="3ed42-353">WHSMobileAppStepWeightToConsume</span></span> |
| <span data-ttu-id="3ed42-354">WhSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="3ed42-354">WHSAdjustmentType</span></span> | <span data-ttu-id="3ed42-355">WhSMobileAppStepWHSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="3ed42-355">WHSMobileAppStepWHSAdjustmentType</span></span> |
| <span data-ttu-id="3ed42-356">WhSReceivingException</span><span class="sxs-lookup"><span data-stu-id="3ed42-356">WHSReceivingException</span></span> | <span data-ttu-id="3ed42-357">WhSMobileAppStepWHSReceivingException</span><span class="sxs-lookup"><span data-stu-id="3ed42-357">WHSMobileAppStepWHSReceivingException</span></span> |
| <span data-ttu-id="3ed42-358">WhSWorkException</span><span class="sxs-lookup"><span data-stu-id="3ed42-358">WHSWorkException</span></span> | <span data-ttu-id="3ed42-359">WHSMobileAppStepWHSWorkException</span><span class="sxs-lookup"><span data-stu-id="3ed42-359">WHSMobileAppStepWHSWorkException</span></span> |
| <span data-ttu-id="3ed42-360">WhSWorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="3ed42-360">WHSWorkLicensePlateId</span></span> | <span data-ttu-id="3ed42-361">WHSMobileAppStepWorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="3ed42-361">WHSMobileAppStepWorkLicensePlateId</span></span> |
| <span data-ttu-id="3ed42-362">WMSLocationId</span><span class="sxs-lookup"><span data-stu-id="3ed42-362">WMSLocationId</span></span> | <span data-ttu-id="3ed42-363">WHSMobiiliAppSammuAsukoht</span><span class="sxs-lookup"><span data-stu-id="3ed42-363">WHSMobileAppStepLocation</span></span> |
| <span data-ttu-id="3ed42-364">Töö ID</span><span class="sxs-lookup"><span data-stu-id="3ed42-364">WorkId</span></span> | <span data-ttu-id="3ed42-365">WHSMobileAppStepWorkId</span><span class="sxs-lookup"><span data-stu-id="3ed42-365">WHSMobileAppStepWorkId</span></span> |
| <span data-ttu-id="3ed42-366">TööstIdLoobumine</span><span class="sxs-lookup"><span data-stu-id="3ed42-366">WorkIdToCancel</span></span> | <span data-ttu-id="3ed42-367">WHSMobileAppStepWorkIdToCancel</span><span class="sxs-lookup"><span data-stu-id="3ed42-367">WHSMobileAppStepWorkIdToCancel</span></span> |
| <span data-ttu-id="3ed42-368">TööLPIdPaneäraKlaster</span><span class="sxs-lookup"><span data-stu-id="3ed42-368">WorkLPIdPutawayCluster</span></span> | <span data-ttu-id="3ed42-369">WHSMobileAppStepWorkLPIdPutawayCluster</span><span class="sxs-lookup"><span data-stu-id="3ed42-369">WHSMobileAppStepWorkLPIdPutawayCluster</span></span> |
| <span data-ttu-id="3ed42-370">TööpoolId</span><span class="sxs-lookup"><span data-stu-id="3ed42-370">WorkPoolId</span></span> | <span data-ttu-id="3ed42-371">WHSMobileAppStepWorkPoolId</span><span class="sxs-lookup"><span data-stu-id="3ed42-371">WHSMobileAppStepWorkPoolId</span></span> |
| <span data-ttu-id="3ed42-372">TsooniId</span><span class="sxs-lookup"><span data-stu-id="3ed42-372">ZoneId</span></span> | <span data-ttu-id="3ed42-373">WHSMobileAppStepZoneId</span><span class="sxs-lookup"><span data-stu-id="3ed42-373">WHSMobileAppStepZoneId</span></span> |

### <a name="available-step-icons"></a><a name="step-icons"></a><span data-ttu-id="3ed42-374">Saadaolevad astmeikoonid</span><span class="sxs-lookup"><span data-stu-id="3ed42-374">Available step icons</span></span>

<span data-ttu-id="3ed42-375">Süsteem hõlmab standardsete astmeikoonide kogumeid, mida saate kasutada ka kohandatud sammude puhul.</span><span class="sxs-lookup"><span data-stu-id="3ed42-375">The system includes a collection of standard step icons that you can also use for your custom steps.</span></span> <span data-ttu-id="3ed42-376">Kohandatud astme ikoone ei saa praegu üles laadida.</span><span class="sxs-lookup"><span data-stu-id="3ed42-376">You can't currently upload custom step icons.</span></span> <span data-ttu-id="3ed42-377">Seetõttu peate alati valima ühe standardsammikoonidest.</span><span class="sxs-lookup"><span data-stu-id="3ed42-377">Therefore, you must always select one of the standard step icons.</span></span>

<span data-ttu-id="3ed42-378">Järgmine tabel näitab kõiki praegu saadaolevaid standardseid astme ikoone ja selle nime.</span><span class="sxs-lookup"><span data-stu-id="3ed42-378">The following table shows every standard step icon that is currently available, and its name.</span></span>

<table>
<tbody>
<tr>
<td><img src="media/step-icons-about.png" alt="About step icon" title="Sammu ikoonist"><br><span data-ttu-id="3ed42-380">Teave</span><span class="sxs-lookup"><span data-stu-id="3ed42-380">About</span></span></td>
<td><img src="media/step-icons-add-lp.png" alt="Add license plate or item step icon" title="Litsentsiplaadi või kaubasammide ikooni lisamine"><br><span data-ttu-id="3ed42-382">AddLpOrItem</span><span class="sxs-lookup"><span data-stu-id="3ed42-382">AddLpOrItem</span></span></td>
<td><img src="media/step-icons-batch-disposition.png" alt="Batch disposition step icon" title="Partii likvideerimissamm"><br><span data-ttu-id="3ed42-384">PartiiPositsioon</span><span class="sxs-lookup"><span data-stu-id="3ed42-384">BatchDisposition</span></span></td>
<td><img src="media/step-icons-carrier.png" alt="Carrier step icon" title="Vedaja astme ikoon"><br><span data-ttu-id="3ed42-386">Vedaja</span><span class="sxs-lookup"><span data-stu-id="3ed42-386">Carrier</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-cw-tag.png" alt="Catch weight tag step icon" title="Tegeliku kaalu sildi etapi ikoon"><br><span data-ttu-id="3ed42-388">Tegelikukaalusilt</span><span class="sxs-lookup"><span data-stu-id="3ed42-388">CatchWeightTag</span></span></td>
<td><img src="media/step-icons-cw-tag-weight.png" alt="Catch weight tag weight step icon" title="Tegeliku kaalu sildi etapi ikoon"><br><span data-ttu-id="3ed42-390">CatchWeightTagWeight</span><span class="sxs-lookup"><span data-stu-id="3ed42-390">CatchWeightTagWeight</span></span></td>
<td><img src="media/step-icons-check-digit.png" alt="Check digit step icon" title="Kontrollnumbri astme ikoon"><br><span data-ttu-id="3ed42-392">Kontrollnumber</span><span class="sxs-lookup"><span data-stu-id="3ed42-392">CheckDigit</span></span></td>
<td><img src="media/step-icons-check-in-out.png" alt="Check in or out ID step icon" title="Sisse- või väljaregistreerimise ID-etapi ikoon"><br><span data-ttu-id="3ed42-394">Väljaregistreerimine (CheckInOutId)</span><span class="sxs-lookup"><span data-stu-id="3ed42-394">CheckInOutId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-child-lp.png" alt="Child license plate step icon" title="Alamlitsentsiplaadi etapi ikoon"><br><span data-ttu-id="3ed42-396">ChildLP</span><span class="sxs-lookup"><span data-stu-id="3ed42-396">ChildLP</span></span></td>
<td><img src="media/step-icons-cluster-id.png" alt="Cluster ID step icon" title="Klastri ID etapi ikoon"><br><span data-ttu-id="3ed42-398">KlastedId</span><span class="sxs-lookup"><span data-stu-id="3ed42-398">ClusterId</span></span></td>
<td><img src="media/step-icons-cluster-position.png" alt="Cluster position step icon" title="Klastri ID etapi ikoon"><br><span data-ttu-id="3ed42-400">Klastripositsioon</span><span class="sxs-lookup"><span data-stu-id="3ed42-400">ClusterPosition</span></span></td>
<td><img src="media/step-icons-config-id.png" alt="Config ID step icon" title="Konfigureeri ID etapi ikoon"><br><span data-ttu-id="3ed42-402">KonfiguratsiooniId</span><span class="sxs-lookup"><span data-stu-id="3ed42-402">ConfigId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-configured-field.png" alt="Configured field step icon" title="Konfigureeritud välja etapi ikoon"><br><span data-ttu-id="3ed42-404">Konfigureeritud väli</span><span class="sxs-lookup"><span data-stu-id="3ed42-404">ConfiguredField</span></span></td>
<td><img src="media/step-icons-con-lp.png" alt="Con or LP step icon" title="Con või LP etapi ikoon"><br><span data-ttu-id="3ed42-406">ConOrLP</span><span class="sxs-lookup"><span data-stu-id="3ed42-406">ConOrLP</span></span></td>
<td><img src="media/step-icons-consolidate-from-LP.png" alt="Consolidate from license plate ID step icon" title="Konsolideeri litsentsiplaadi ID etapi ikoonilt"><br><span data-ttu-id="3ed42-408">KonsolideerimineLitsentseeritudPlaatID</span><span class="sxs-lookup"><span data-stu-id="3ed42-408">ConsolidateFromLicensePlateID</span></span></td>
<td><img src="media/step-icons-consolidate-to-LP.png" alt="Consolidate to license plate ID step icon" title="Konsolideeri litsentsiplaadi ID etapi ikoon"><br><span data-ttu-id="3ed42-410">KonsolideerimineLitsentseeritudPlaatId</span><span class="sxs-lookup"><span data-stu-id="3ed42-410">ConsolidateToLicensePlateID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-container-type.png" alt="Container type step icon" title="Konteineri tüübi etapi ikoon"><br><span data-ttu-id="3ed42-412">Konteineritüüp</span><span class="sxs-lookup"><span data-stu-id="3ed42-412">ContainerType</span></span></td>
<td><img src="media/step-icons-counting.png" alt="Counting step icon" title="Arveldus etapi ikoon"><br><span data-ttu-id="3ed42-414">Inventuur</span><span class="sxs-lookup"><span data-stu-id="3ed42-414">Counting</span></span></td>
<td><img src="media/step-icons-counting-reason.png" alt="Counting reason code step icon" title="Inventuuri põhjusekoodi etapi ikoon"><br><span data-ttu-id="3ed42-416">ArvestusePõhjusKood</span><span class="sxs-lookup"><span data-stu-id="3ed42-416">CountingReasonCode</span></span></td>
<td><img src="media/step-icons-country-origin.png" alt="Country of origin code step icon" title="Päritoluriiki koodi juhise ikoon"><br><span data-ttu-id="3ed42-418">Päritoluriik</span><span class="sxs-lookup"><span data-stu-id="3ed42-418">CountryOfOrigin</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-disposition.png" alt="Disposition step icon" title="Partii likvideerimissammu ikoon"><br><span data-ttu-id="3ed42-420">Likvideerimine</span><span class="sxs-lookup"><span data-stu-id="3ed42-420">Disposition</span></span></td>
<td><img src="media/step-icons-done.png" alt="Done step icon" title="Valmisastme ikoon"><br><span data-ttu-id="3ed42-422">Valmis</span><span class="sxs-lookup"><span data-stu-id="3ed42-422">Done</span></span></td>
<td><img src="media/step-icons-driver-check-in-confirmation.png" alt="Driver check in confirmation step icon" title="Juhi sisseregistreerimise kinnitussamm"><br><span data-ttu-id="3ed42-424">DriverCheckInConfirmation</span><span class="sxs-lookup"><span data-stu-id="3ed42-424">DriverCheckInConfirmation</span></span></td>
<td><img src="media/step-icons-driver-check-in-id.png" alt="Driver check in ID step icon" title="Sisseregistreerimise ID-etapi ikoon"><br><span data-ttu-id="3ed42-426">DriverCheckInId</span><span class="sxs-lookup"><span data-stu-id="3ed42-426">DriverCheckInId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-driver-check-out-id.png" alt="Driver check out ID step icon" title="Väljaregistreerimise ID-etapi ikoon"><br><span data-ttu-id="3ed42-428">SõitjaVäljaregamiseId</span><span class="sxs-lookup"><span data-stu-id="3ed42-428">DriverCheckOutId</span></span></td>
<td><img src="media/step-icons-exp-date.png" alt="Expiration date step icon" title="Aegumiskuupäeva etapi ikoon"><br><span data-ttu-id="3ed42-430">Aegumiskuupäev</span><span class="sxs-lookup"><span data-stu-id="3ed42-430">ExpDate</span></span></td>
<td><img src="media/step-icons-field.png" alt="Field step icon" title="Välja sammu ikoon"><br><span data-ttu-id="3ed42-432">Field</span><span class="sxs-lookup"><span data-stu-id="3ed42-432">Field</span></span></td>
<td><img src="media/step-icons-from-batch.png" alt="From batch disposition step icon" title="Partii likvideerimissammu ikoon"><br><span data-ttu-id="3ed42-434">PartiiLikvideerimine</span><span class="sxs-lookup"><span data-stu-id="3ed42-434">FromBatchDisposition</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-from-inventory-status.png" alt="From inventory status step icon" title="Varude olekusammide ikoonilt"><br><span data-ttu-id="3ed42-436">VarudeOlekult</span><span class="sxs-lookup"><span data-stu-id="3ed42-436">FromInventoryStatus</span></span></td>
<td><img src="media/step-icons-id-attribute.png" alt="ID attribute step icon" title="Klastri ID etapi ikoon"><br><span data-ttu-id="3ed42-438">AtribuudiId</span><span class="sxs-lookup"><span data-stu-id="3ed42-438">IdAttribute</span></span></td>
<td><img src="media/step-icons-invent-batch-id.png" alt="Inventory batch ID step icon" title="Varude partii ID etapi ikoon"><br><span data-ttu-id="3ed42-440">InventariPartiiId</span><span class="sxs-lookup"><span data-stu-id="3ed42-440">InventBatchID</span></span></td>
<td><img src="media/step-icons-invent-color-id.png" alt="Inventory color ID step icon" title="Varude värvi ID etapi ikoon"><br><span data-ttu-id="3ed42-442">InventuuriVärviId</span><span class="sxs-lookup"><span data-stu-id="3ed42-442">InventColorID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-invent-location.png" alt="Inventory location step icon" title="Varude asukoha etapi ikoon"><br><span data-ttu-id="3ed42-444">VarudeAsukoht</span><span class="sxs-lookup"><span data-stu-id="3ed42-444">InventLocation</span></span></td>
<td><img src="media/step-icons-invent-serial-id.png" alt="Inventory serial ID step icon" title="Varude seeria ID etapi ikoon"><br><span data-ttu-id="3ed42-446">InventSeeriaId</span><span class="sxs-lookup"><span data-stu-id="3ed42-446">InventSerialID</span></span></td>
<td><img src="media/step-icons-invent-size-id.png" alt="Inventory size ID step icon" title="Varude suuruse ID etapi ikoon"><br><span data-ttu-id="3ed42-448">VaruSuuruseId</span><span class="sxs-lookup"><span data-stu-id="3ed42-448">InventSizeID</span></span></td>
<td><img src="media/step-icons-invent-status-id.png" alt="Inventory status ID step icon" title="Varude oleku ID sammu ikoon"><br><span data-ttu-id="3ed42-450">VaruSeisId</span><span class="sxs-lookup"><span data-stu-id="3ed42-450">InventStatusID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-invent-style-id.png" alt="Inventory style ID step icon" title="Varude stiili ID etapi ikoon"><br><span data-ttu-id="3ed42-452">VaruStiilId</span><span class="sxs-lookup"><span data-stu-id="3ed42-452">InventStyleID</span></span></td>
<td><img src="media/step-icons-invent-version-id.png" alt="Inventory version ID step icon" title="Varude versiooni ID sammu ikoon"><br><span data-ttu-id="3ed42-454">VaruVersioonId</span><span class="sxs-lookup"><span data-stu-id="3ed42-454">InventVersionID</span></span></td>
<td><img src="media/step-icons-item-id.png" alt="Item ID step icon" title="Ühiku ID etapi ikoon"><br><span data-ttu-id="3ed42-456">ÜhikuId</span><span class="sxs-lookup"><span data-stu-id="3ed42-456">ItemID</span></span></td>
<td><img src="media/step-icons-itm-contianer-id.png" alt="ITM container ID step icon" title="ITM konteineri ID etapi ikoon"><br><span data-ttu-id="3ed42-458">ITMKonteinerID</span><span class="sxs-lookup"><span data-stu-id="3ed42-458">ITMContainerID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-itm-shipment-id.png" alt="ITM shipment ID step icon" title="ITM-saadetise ID etapi ikoon"><br><span data-ttu-id="3ed42-460">ITMSaatmisID</span><span class="sxs-lookup"><span data-stu-id="3ed42-460">ITMShipmentID</span></span></td>
<td><img src="media/step-icons-kanban-card-id.png" alt="Kanban card ID step icon" title="Kanban-kaardi ID etapi ikoon"><br><span data-ttu-id="3ed42-462">KanbanKaardiId</span><span class="sxs-lookup"><span data-stu-id="3ed42-462">KanbanCardID</span></span></td>
<td><img src="media/step-icons-kanban-or-card-id.png" alt="Kanban or card ID step icon" title="Kanban või kaardi ID etapi ikoon"><br><span data-ttu-id="3ed42-464">KanbanVõiKaardiId</span><span class="sxs-lookup"><span data-stu-id="3ed42-464">KanbanOrCardID</span></span></td>
<td><img src="media/step-icons-license-plate-id.png" alt="License plate ID step icon" title="Alamlitsentsiplaadi ID etapi ikoon"><br><span data-ttu-id="3ed42-466">LitsentsPlateId</span><span class="sxs-lookup"><span data-stu-id="3ed42-466">LicensePlateID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-load-id.png" alt="Load ID step icon" title="Koorma ID etapi ikoon"><br><span data-ttu-id="3ed42-468">KoormaId</span><span class="sxs-lookup"><span data-stu-id="3ed42-468">LoadId</span></span></td>
<td><img src="media/step-icons-location-lp-pos.png" alt="Location license plate position step icon" title="Asukoha litsentsiplaadi paigutuse sammu ikoon"><br><span data-ttu-id="3ed42-470">AsukohaLitsentsiPlaadiPaigutus</span><span class="sxs-lookup"><span data-stu-id="3ed42-470">LocationLicensePlatePosition</span></span></td>
<td><img src="media/step-icons-location-or-lp.png" alt="Location or license plate step icon" title="Asukoha või litsentsiplaadi sammu ikoon"><br><span data-ttu-id="3ed42-472">LocOrLP</span><span class="sxs-lookup"><span data-stu-id="3ed42-472">LocOrLP</span></span></td>
<td><img src="media/step-icons-location-or-lp-check.png" alt="Location or license plate check step icon" title="Asukoha või litsentsiplaadi sammu ikoon"><br><span data-ttu-id="3ed42-474">LocOrLPcheck</span><span class="sxs-lookup"><span data-stu-id="3ed42-474">LocOrLPCheck</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-location-or-lp-from.png" alt="Location or license plate from step icon" title="Asukoha või litsentsiplaadi sammu ikoonilt"><br><span data-ttu-id="3ed42-476">LocOrLPFrom</span><span class="sxs-lookup"><span data-stu-id="3ed42-476">LocOrLPFrom</span></span></td>
<td><img src="media/step-icons-location-or-lp-to.png" alt="Location or license plate to step icon" title="Asukohalt või litsentsiplaadilt sammu ikoonile"><br><span data-ttu-id="3ed42-478">LocOrLPTo</span><span class="sxs-lookup"><span data-stu-id="3ed42-478">LocOrLPTo</span></span></td>
<td><img src="media/step-icons-long-process-complete.png" alt="Long process completed step icon" title="Pika protsessi lõpetatud etapi ikoon"><br><span data-ttu-id="3ed42-480">PikkprotsessLõpetatud</span><span class="sxs-lookup"><span data-stu-id="3ed42-480">LongProcessCompleted</span></span></td>
<td><img src="media/step-icons-lp-break-parent.png" alt="LP break parent LP step icon" title="LP-pausi ema LP etapi ikoon"><br><span data-ttu-id="3ed42-482">LPBreakParentLP</span><span class="sxs-lookup"><span data-stu-id="3ed42-482">LPBreakParentLP</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-merge-container.png" alt="Merge container ID step icon" title="Ühendatud konteineri ID etapi ikoon"><br><span data-ttu-id="3ed42-484">ÜhendatudKontainerId</span><span class="sxs-lookup"><span data-stu-id="3ed42-484">MergeContainerId</span></span></td>
<td><img src="media/step-icons-mixed-lp-line.png" alt="Mixed license plate line number step icon" title="Litsentsiplaadi rea numbri segaikoon"><br><span data-ttu-id="3ed42-486">SeagtudJoonNum</span><span class="sxs-lookup"><span data-stu-id="3ed42-486">MixedLPLineNum</span></span></td>
<td><img src="media/step-icons-outbound-weight.png" alt="Outbound weight step icon" title="Väljamineva kaalu astme ikoon"><br><span data-ttu-id="3ed42-488">VäljaminevKaal</span><span class="sxs-lookup"><span data-stu-id="3ed42-488">OutboundWeight</span></span></td>
<td><img src="media/step-icons-owner.png" alt="Owner step icon" title="Omaniku astme ikoon"><br><span data-ttu-id="3ed42-490">Omanik</span><span class="sxs-lookup"><span data-stu-id="3ed42-490">Owner</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-parent-lp.png" alt="Parent license plate step icon" title="Ülemlitsentsiplaadi etapi ikoon"><br><span data-ttu-id="3ed42-492">Ülem-LP</span><span class="sxs-lookup"><span data-stu-id="3ed42-492">ParentLP</span></span></td>
<td><img src="media/step-icons-please-confirm.png" alt="Please confirm step icon" title="Kinnitage sammu ikoon"><br><span data-ttu-id="3ed42-494">Palun kinnitage</span><span class="sxs-lookup"><span data-stu-id="3ed42-494">PleaseConfirm</span></span></td>
<td><img src="media/step-icons-po-line-num.png" alt="Purchase order line number step icon" title="Ostutellimuse rea numbri sammu ikoon"><br><span data-ttu-id="3ed42-496">PoReaNumber</span><span class="sxs-lookup"><span data-stu-id="3ed42-496">POLineNum</span></span></td>
<td><img src="media/step-icons-po-num.png" alt="Purchase order number step icon" title="Ostutellimuse rea numbri sammu ikoon"><br><span data-ttu-id="3ed42-498">PONum</span><span class="sxs-lookup"><span data-stu-id="3ed42-498">PONum</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-position-full.png" alt="Position full step icon" title="Ametikoha täis sammu ikoon"><br><span data-ttu-id="3ed42-500">AmetikohtTäis</span><span class="sxs-lookup"><span data-stu-id="3ed42-500">PositionFull</span></span></td>
<td><img src="media/step-icons-potency.png" alt="Potency step icon" title="Potentsiaalse sammu ikoon"><br><span data-ttu-id="3ed42-502">Sisaldus</span><span class="sxs-lookup"><span data-stu-id="3ed42-502">Potency</span></span></td>
<td><img src="media/step-icons-printer-name.png" alt="Printer name step icon" title="Printeri nimeastme ikoon"><br><span data-ttu-id="3ed42-504">PrinteriNimi</span><span class="sxs-lookup"><span data-stu-id="3ed42-504">PrinterName</span></span></td>
<td><img src="media/step-icons-prod-id.png" alt="Prod ID step icon" title="Koorma ID etapi ikoon"><br><span data-ttu-id="3ed42-506">ProdId</span><span class="sxs-lookup"><span data-stu-id="3ed42-506">ProdId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-product-confirm.png" alt="Product confirmation step icon" title="Toote kinnitussammu ikoon"><br><span data-ttu-id="3ed42-508">TooteKinnitus</span><span class="sxs-lookup"><span data-stu-id="3ed42-508">ProductConfirmation</span></span></td>
<td><img src="media/step-icons-put.png" alt="Put step icon" title="Pane sammu ikoon"><br><span data-ttu-id="3ed42-510">Pane</span><span class="sxs-lookup"><span data-stu-id="3ed42-510">Put</span></span></td>
<td><img src="media/step-icons-putaway-cluster-id.png" alt="Putaway cluster ID step icon" title="Pane klastri ID etapi ikoon"><br><span data-ttu-id="3ed42-512">PaneäraKlastriId</span><span class="sxs-lookup"><span data-stu-id="3ed42-512">PutawayClusterId</span></span></td>
<td><img src="media/step-icons-qty.png" alt="Quantity step icon" title="Koguse astme ikoon"><br><span data-ttu-id="3ed42-514">Kogus</span><span class="sxs-lookup"><span data-stu-id="3ed42-514">Qty</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-qty-adjust-in.png" alt="Quantity adjust in step icon" title="Koguse korrigeerimine astme ikoonil"><br><span data-ttu-id="3ed42-516">KogusTäiendusIn</span><span class="sxs-lookup"><span data-stu-id="3ed42-516">QtyAdjustIn</span></span></td>
<td><img src="media/step-icons-qty-short.png" alt="Quantity short step icon" title="Koguse lühike astme ikoon"><br><span data-ttu-id="3ed42-518">KogusLühike</span><span class="sxs-lookup"><span data-stu-id="3ed42-518">QtyShort</span></span></td>
<td><img src="media/step-icons-qty-to-consume.png" alt="Quantity to consume step icon" title="Astme ikooni tarbitav kogus"><br><span data-ttu-id="3ed42-520">KogusTarbima</span><span class="sxs-lookup"><span data-stu-id="3ed42-520">QtyToConsume</span></span></td>
<td><img src="media/step-icons-qty-to-put.png" alt="Quantity to put step icon" title="Astme ikooni tarbitav kogus"><br><span data-ttu-id="3ed42-522">KogusVäljaMinev</span><span class="sxs-lookup"><span data-stu-id="3ed42-522">QtyToPut</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-qty-to-scrap.png" alt="Quantity to scrap step icon" title="Koguse eemaldamise sammu ikoon"><br><span data-ttu-id="3ed42-524">QtyToScrap</span><span class="sxs-lookup"><span data-stu-id="3ed42-524">QtyToScrap</span></span></td>
<td><img src="media/step-icons-qty-confirmation.png" alt="Quantity confirmation step icon" title="Koguse kinnitussammu ikoon"><br><span data-ttu-id="3ed42-526">KogusKinnitus</span><span class="sxs-lookup"><span data-stu-id="3ed42-526">QuantityConfirmation</span></span></td>
<td><img src="media/step-icons-raf-end-job.png" alt="Report as finished end job step icon" title="Lõpetatuna kinnitatud tööastme ikoon"><br><span data-ttu-id="3ed42-528">RAFEndJob</span><span class="sxs-lookup"><span data-stu-id="3ed42-528">RAFEndJob</span></span></td>
<td><img src="media/step-icons-recv-loc-id.png" alt="Receive location ID step icon" title="Asukoha ID etapi ikooni vastu võtta"><br><span data-ttu-id="3ed42-530">RecvAsukohaId</span><span class="sxs-lookup"><span data-stu-id="3ed42-530">RecvLocationID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-remove-container-id.png" alt="Remove container ID step icon" title="Konteineri eemaldamise ID etapi ikoon"><br><span data-ttu-id="3ed42-532">EemaldaContainerId</span><span class="sxs-lookup"><span data-stu-id="3ed42-532">RemoveContainerID</span></span></td>
<td><img src="media/step-icons-rma-no.png" alt="RMA number step icon" title="RMA numbriastme ikoon"><br><span data-ttu-id="3ed42-534">RMANum</span><span class="sxs-lookup"><span data-stu-id="3ed42-534">RMANum</span></span></td>
<td><img src="media/step-icons-select-order.png" alt="Select order step icon" title="Valige tellimuse etapi ikoon"><br><span data-ttu-id="3ed42-536">ValiTellimus</span><span class="sxs-lookup"><span data-stu-id="3ed42-536">SelectOrder</span></span></td>
<td><img src="media/step-icons-short-pick-reason.png" alt="Short pick reason step icon" title="Lühike noppimise põhjuseastme ikoon"><br><span data-ttu-id="3ed42-538">LühikeKorjePõhjus</span><span class="sxs-lookup"><span data-stu-id="3ed42-538">ShortPickReason</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-sort-position-id.png" alt="Sort position ID step icon" title="Sordi positsiooni ID etapi ikoon"><br><span data-ttu-id="3ed42-540">LühikeAmetId</span><span class="sxs-lookup"><span data-stu-id="3ed42-540">SortPositionId</span></span></td>
<td><img src="media/step-icons-target-lp-id.png" alt="Target license plate ID step icon" title="Alamlitsentsiplaadi ID etapi ikoon"><br><span data-ttu-id="3ed42-542">EesmärkLitsentsPlateId</span><span class="sxs-lookup"><span data-stu-id="3ed42-542">TargetLicensePlateId</span></span></td>
<td><img src="media/step-icons-to-line-no.png" alt="To line number step icon" title="Reanumbri etapi ikooniks"><br><span data-ttu-id="3ed42-544">ReaNumbriks</span><span class="sxs-lookup"><span data-stu-id="3ed42-544">ToLineNum</span></span></td>
<td><img src="media/step-icons-to-location.png" alt="To location step icon" title="Varude asukoha etapi ikoonile"><br><span data-ttu-id="3ed42-546">Asukohta</span><span class="sxs-lookup"><span data-stu-id="3ed42-546">ToLocation</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-to-number.png" alt="To number step icon" title="Numbri astme ikoonile"><br><span data-ttu-id="3ed42-548">Numbrile</span><span class="sxs-lookup"><span data-stu-id="3ed42-548">ToNum</span></span></td>
<td><img src="media/step-icons-to-warehouse.png" alt="To warehouse step icon" title="Varude asukoha etapi ikoonile"><br><span data-ttu-id="3ed42-550">Lattu</span><span class="sxs-lookup"><span data-stu-id="3ed42-550">ToWarehouse</span></span></td>
<td><img src="media/step-icons-tranport-load-id.png" alt="Transport load ID step icon" title="Transpordikoorma ID etapi ikoon"><br><span data-ttu-id="3ed42-552">TranspordiVaruId</span><span class="sxs-lookup"><span data-stu-id="3ed42-552">TransportLoadId</span></span></td>
<td><img src="media/step-icons-vendor-batch-id.png" alt="Vendor batch ID step icon" title="Hankija partii ID etapi ikoon"><br><span data-ttu-id="3ed42-554">VendBatchId</span><span class="sxs-lookup"><span data-stu-id="3ed42-554">VendBatchId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-wave-label-id.png" alt="Wave label ID step icon" title="Voo sildi-ID etapi ikoon"><br><span data-ttu-id="3ed42-556">VooSildiId</span><span class="sxs-lookup"><span data-stu-id="3ed42-556">WaveLabelId</span></span></td>
<td><img src="media/step-icons-wave-label-qty.png" alt="Wave label quantity step icon" title="Voo sildi-ID kvaliteedi etapi ikoon"><br><span data-ttu-id="3ed42-558">LaineLblQty</span><span class="sxs-lookup"><span data-stu-id="3ed42-558">WaveLblQty</span></span></td>
<td><img src="media/step-icons-weight.png" alt="Weight step icon" title="Kaalu astme ikoon"><br><span data-ttu-id="3ed42-560">Kaal</span><span class="sxs-lookup"><span data-stu-id="3ed42-560">Weight</span></span></td>
<td><img src="media/step-icons-weight-to-consume.png" alt="Weight to consume step icon" title="Kaalu tarbitava sammu ikoon"><br><span data-ttu-id="3ed42-562">KaalToConsume</span><span class="sxs-lookup"><span data-stu-id="3ed42-562">WeightToConsume</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-whs-adjustment-type.png" alt="WHS adjustment type step icon" title="WHS kohandamistüübi etapi ikoon"><br><span data-ttu-id="3ed42-564">WhSAdjustmentType</span><span class="sxs-lookup"><span data-stu-id="3ed42-564">WHSAdjustmentType</span></span></td>
<td><img src="media/step-icons-whs-receiving-exception.png" alt="WHS receiving exception step icon" title="WHS-i vastuvõtmise erandisammu ikoon"><br><span data-ttu-id="3ed42-566">WhSReceivingException</span><span class="sxs-lookup"><span data-stu-id="3ed42-566">WHSReceivingException</span></span></td>
<td><img src="media/step-icons-wms-location-id.png" alt="WMS location ID step icon" title="WMS asukoha ID etapi ikoon"><br><span data-ttu-id="3ed42-568">WMSAsukohtId</span><span class="sxs-lookup"><span data-stu-id="3ed42-568">WMSLocationID</span></span></td>
<td><img src="media/step-icons-work-id.png" alt="Work ID step icon" title="Töö ID etapi ikoon"><br><span data-ttu-id="3ed42-570">Töö ID</span><span class="sxs-lookup"><span data-stu-id="3ed42-570">WorkId</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-work-id-to-cancel.png" alt="Work ID to cancel step icon" title="Töö ID etapi ikooni tühistamiseks"><br><span data-ttu-id="3ed42-572">TööstIdLoobumine</span><span class="sxs-lookup"><span data-stu-id="3ed42-572">WorkIdToCancel</span></span></td>
<td><img src="media/step-icons-work-lp-id.png" alt="Work license plate ID step icon" title="Töö litsentsiplaadi ID etapi ikoon"><br><span data-ttu-id="3ed42-574">WorkLicensePlateId</span><span class="sxs-lookup"><span data-stu-id="3ed42-574">WorkLicensePlateId</span></span></td>
<td><img src="media/step-icons-work-lp-putaway-cluster.png" alt="Work license plate ID putaway cluster step icon" title="Töö litsentsiplaadi ID ärapanemise klastri etapi ikoon"><br><span data-ttu-id="3ed42-576">TööLPIdPaneäraKlaster</span><span class="sxs-lookup"><span data-stu-id="3ed42-576">WorkLPIDPutawayCluster</span></span></td>
<td><img src="media/step-icons-work-pool-id.png" alt="Work pool ID step icon" title="Töö ID etapi ikoon"><br><span data-ttu-id="3ed42-578">WorkPoolID</span><span class="sxs-lookup"><span data-stu-id="3ed42-578">WorkPoolID</span></span></td>
</tr>
<tr>
<td><img src="media/step-icons-zone-pool-id.png" alt="Zone ID step icon" title="Tsooni ID etapi ikoon"><br><span data-ttu-id="3ed42-580">TsooniId</span><span class="sxs-lookup"><span data-stu-id="3ed42-580">ZoneID</span></span></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>

## <a name="example-assign-step-icons-and-titles-for-a-custom-flow"></a><a name="example"></a><span data-ttu-id="3ed42-581">Näide: kohandatud voo etapiikoonide ja pealkirjade määramine</span><span class="sxs-lookup"><span data-stu-id="3ed42-581">Example: Assign step icons and titles for a custom flow</span></span>

<span data-ttu-id="3ed42-582">See näide selgitab, kuidas seadistada kohandatud ülesandevoo astme ikoone ja pealkirjasid.</span><span class="sxs-lookup"><span data-stu-id="3ed42-582">This example explains how to set up step icons and titles for a custom task flow.</span></span> <span data-ttu-id="3ed42-583">Stsenaarium on üles ehitatud kohandatud ülesandevoo näitele, mida esitatakse ja analüüsitakse üksikasjalikumalt järgmises postituses": ladustamise [mobiilirakenduse kohandamine](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app).</span><span class="sxs-lookup"><span data-stu-id="3ed42-583">The scenario is built on an example of a custom task flow that is presented and explored in more detail in the following blog post: [Customizing the Warehousing Mobile App](https://cloudblogs.microsoft.com/dynamics365/it/2017/07/06/customizing-the-warehousing-mobile-app).</span></span> <span data-ttu-id="3ed42-584">Ülesande voog töötab järgmiselt:</span><span class="sxs-lookup"><span data-stu-id="3ed42-584">The task flow works in the following way:</span></span>

1. <span data-ttu-id="3ed42-585">Rakendus kuvab lehekülje, mis palub töötajal sisestada konteineri ID (nt vöötkoodi skannides).</span><span class="sxs-lookup"><span data-stu-id="3ed42-585">The app shows a page that prompts the worker to provide a container ID (for example, by scanning a bar code).</span></span>
1. <span data-ttu-id="3ed42-586">Kui konteineri ID on kehtiv, avab rakendus uue lehe, mis palub töötajal kaalu võtta.</span><span class="sxs-lookup"><span data-stu-id="3ed42-586">If the container ID is valid, the app opens a new page that prompts the worker for the weight.</span></span> <span data-ttu-id="3ed42-587">(Kui konteineri ID ei kehti, tagastatakse töötaja esimesele leheküljele.)</span><span class="sxs-lookup"><span data-stu-id="3ed42-587">(If the container ID isn't valid, the worker is returned to the first page.)</span></span>
1. <span data-ttu-id="3ed42-588">Kui töötaja sisestab kehtiva kaalu, talletab süsteem kaalu ja tagastab töötaja esimesele leheküljele.</span><span class="sxs-lookup"><span data-stu-id="3ed42-588">When the worker enters a valid weight, the system stores the weight and returns the worker to the first page.</span></span>

<span data-ttu-id="3ed42-589">Järgmisel illustratsioonil on toodud see töövoog.</span><span class="sxs-lookup"><span data-stu-id="3ed42-589">The following illustration shows this task flow.</span></span>

<span data-ttu-id="3ed42-590">![Ülesande voo diagramm](media/step-icons-example-task-flow.png "Ülesande voo diagramm")</span><span class="sxs-lookup"><span data-stu-id="3ed42-590">![Task flow diagram](media/step-icons-example-task-flow.png "Task flow diagram")</span></span>

### <a name="create-a-step-class-for-the-container-input-page"></a><span data-ttu-id="3ed42-591">Konteineri sisestuslehe etapiklassi loomine</span><span class="sxs-lookup"><span data-stu-id="3ed42-591">Create a step class for the container input page</span></span>

<span data-ttu-id="3ed42-592">Konteineri sisestusleht võimaldab töötajal skannida või sisestada konteineri ID.</span><span class="sxs-lookup"><span data-stu-id="3ed42-592">The container input page lets the worker scan or enter a container ID.</span></span>

<span data-ttu-id="3ed42-593">![Konteineri sisestusleht](media/step-icons-example-container-input.png "Konteineri sisestusleht")</span><span class="sxs-lookup"><span data-stu-id="3ed42-593">![Container input page](media/step-icons-example-container-input.png "Container input page")</span></span>

<span data-ttu-id="3ed42-594">Konteineri sisestuslehel on sisendvälja juhtelemendi nimi `ContainerId`.</span><span class="sxs-lookup"><span data-stu-id="3ed42-594">On the container input page, the control name of the input field is `ContainerId`.</span></span> <span data-ttu-id="3ed42-595">Kuna see juhtelemendi nimi ei ole [ID-de loendis](#step-ids-classes), te ei leia sellel põhinevat olemasolevat sammu.</span><span class="sxs-lookup"><span data-stu-id="3ed42-595">Because this control name isn't in the [list of step IDs](#step-ids-classes), you won't find an existing step that is based on it.</span></span> <span data-ttu-id="3ed42-596">Seetõttu peate looma astmeklassi, mis sammu esindab.</span><span class="sxs-lookup"><span data-stu-id="3ed42-596">Therefore, you must create a step class that represents the step.</span></span> <span data-ttu-id="3ed42-597">Siin on näide.</span><span class="sxs-lookup"><span data-stu-id="3ed42-597">Here is an example.</span></span>

```xpp
[WHSMobileAppStepId('ContainerId')]
final internal class WHSMobileAppStepContainerId extends WHSMobileAppStep
{
    private const WHSMobileAppStepIcon PopulationIcon = 'InventBatchID';
    private const WHSMobileAppStepTitle InputNotFilledTitle = "@WAX:WHSMobileAppStepContainerID_InputNotFilled"; //Scan a container
    protected void initValues()
    {
        defaultStepIcon = PopulationIcon;
        defaultStepTitle = InputNotFilledTitle;
    }
}
```

<span data-ttu-id="3ed42-598">Astme ikooni identifikaator salvestatakse klassi liikmele ja astme `defaultStepIcon` pealkiri talletatakse `defaultStepTitle` klassi liikmele.</span><span class="sxs-lookup"><span data-stu-id="3ed42-598">The identifier of the step icon is stored in the `defaultStepIcon` class member, and the step title is stored in the `defaultStepTitle` class member.</span></span>

<span data-ttu-id="3ed42-599">Astme ikooni määramiseks määrake üks ikooni ID-dest, mis on loetletud `defaultStepIcon` varasemas jaotises [Saadaolevad astme ikoonid](#step-icons) selles teemas.</span><span class="sxs-lookup"><span data-stu-id="3ed42-599">To assign a step icon, set `defaultStepIcon` to one of the icon IDs that are listed in the [Available step icons](#step-icons) section earlier in this topic.</span></span>

### <a name="use-a-standard-or-custom-step-icon-and-title-for-the-weight-input"></a><span data-ttu-id="3ed42-600">Kasuta kaalusisendi jaoks standardset või kohandatud etapi ikooni ja pealkirja</span><span class="sxs-lookup"><span data-stu-id="3ed42-600">Use a standard or custom step icon and title for the weight input</span></span>

<span data-ttu-id="3ed42-601">Kaalu sisestusleht võimaldab töötajal sisestada kaalu.</span><span class="sxs-lookup"><span data-stu-id="3ed42-601">The weight input page lets the worker enter a weight.</span></span>

<span data-ttu-id="3ed42-602">![Kaalu sisestusleht](media/step-icons-example-weight-input.png "Kaalu sisestusleht")</span><span class="sxs-lookup"><span data-stu-id="3ed42-602">![Weight input page](media/step-icons-example-weight-input.png "Weight input page")</span></span>

<span data-ttu-id="3ed42-603">Kaalu sisestuslehel on sisendvälja juhtelemendi nimi `Weight`, mis on [astmete ID-de loendis](#step-ids-classes).</span><span class="sxs-lookup"><span data-stu-id="3ed42-603">On the weight input page, the control name of the input field is `Weight`, which is in the [list of step IDs](#step-ids-classes).</span></span> <span data-ttu-id="3ed42-604">Seega, kui klassis määratletud astme ikoon ja pealkiri on teile vastuvõetavad, ei pea te selle `WHSMobileAppStepWeight` sammu jaoks midagi muutma.</span><span class="sxs-lookup"><span data-stu-id="3ed42-604">Therefore, if the step icon and title that are defined in the `WHSMobileAppStepWeight` class are acceptable to you, you don't have to change anything for this step.</span></span>

<span data-ttu-id="3ed42-605">Kuid kui eelistate selle sammu jaoks kasutada erinevat ikooni või pealkirja, saate alistada kas `stepId()` meetodi või `stepInfo()` meetodi koosteklassis.</span><span class="sxs-lookup"><span data-stu-id="3ed42-605">However, if you prefer to use a different icon or title for this step, you can override either the `stepId()` method or the `stepInfo()` method in the builder class.</span></span> <span data-ttu-id="3ed42-606">Igal ülesandevool on oma etapi teabekonstruktur.</span><span class="sxs-lookup"><span data-stu-id="3ed42-606">Each task flow has its own step info builder.</span></span>

#### <a name="override-the-stepid-method"></a><span data-ttu-id="3ed42-607">Meetodi stepId() alistamine</span><span class="sxs-lookup"><span data-stu-id="3ed42-607">Override the stepId() method</span></span>

<span data-ttu-id="3ed42-608">Järgmine näide näitab ühte viisi, kuidas saate muuta koostaja klassi, alistades `stepId()` meetodi.</span><span class="sxs-lookup"><span data-stu-id="3ed42-608">The following example shows one way that you can modify a builder class by overriding the `stepId()` method.</span></span>

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepId stepId()
    {
        WHSMobileAppStepId stepIdLocal = super();
        if (stepIdLocal == 'Weight')
        {
            return 'NewWeight';
        }
        return stepIdLocal;
    }
}
```

<span data-ttu-id="3ed42-609">Seejärel loote sammule `NewWeight` astmeklassi.</span><span class="sxs-lookup"><span data-stu-id="3ed42-609">You then create a step class for the `NewWeight` step.</span></span> <span data-ttu-id="3ed42-610">Kood peaks sarnanema koodiga, `ContainerId` mida selles teemas varem kuvati.</span><span class="sxs-lookup"><span data-stu-id="3ed42-610">The code should resemble the code for the `ContainerId` example that was shown earlier in this topic.</span></span>

#### <a name="override-the-stepinfo-method"></a><span data-ttu-id="3ed42-611">Meetodi stepId() ülekirjutamine</span><span class="sxs-lookup"><span data-stu-id="3ed42-611">Override the stepInfo() method</span></span>

<span data-ttu-id="3ed42-612">Järgmine näide näitab ühte viisi, kuidas saate muuta koostaja klassi, alistades `stepInfo()` meetodi.</span><span class="sxs-lookup"><span data-stu-id="3ed42-612">The following example shows one way that you can modify a builder class by overriding the `stepInfo()` method.</span></span>

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode:: WeighContainer)]
public class WHSMobileAppStepInfoBuilderWeighContainer extends WHSMobileAppStepInfoBuilder
{
    protected WHSMobileAppStepInfo stepInfo()
    {
        if (stepId != 'Weight')
        {
            return super();
        }
        WHSMobileAppStepInfo stepInfo = WHSMobileAppStepInfo::construct();
        stepInfo.parmStepIcon('NewIcon');
        stepInfo.parmStepTitle('NewTitle');
        return stepInfo;
    }
}
```

<span data-ttu-id="3ed42-613">Seejärel saate luua `WHSMobileAppStepInfo` objekti ja seadistada ikooni ja/või pealkirja otse.</span><span class="sxs-lookup"><span data-stu-id="3ed42-613">You then construct a `WHSMobileAppStepInfo` object, and set the icon and/or title directly.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3ed42-614">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="3ed42-614">Additional resources</span></span>

- [<span data-ttu-id="3ed42-615">Laohalduse mobiilirakenduse installimine ja ühendamine</span><span class="sxs-lookup"><span data-stu-id="3ed42-615">Install and connect the Warehouse Management mobile app</span></span>](install-configure-warehouse-management-app.md)
- [<span data-ttu-id="3ed42-616">Mobiilse seadme kasutaja sätted</span><span class="sxs-lookup"><span data-stu-id="3ed42-616">Mobile device user settings</span></span>](mobile-device-user-settings.md)
