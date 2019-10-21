---
title: Varude üleviimiste ja korrigeerimiste sünkroonimine rakendusest Field Service rakendusse Supply Chain Management
description: Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse varude korrigeerimiste ja üleviimiste sünkroonimiseks rakendusest Dynamics 365 Supply Chain Management rakendusse Dynamics 365 Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: c989e6efff88768f0b370fc81eea971c5c11bcef
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251626"
---
# <a name="synchronize-inventory-adjustments-from-field-service-to-supply-chain-management"></a><span data-ttu-id="461d1-103">Varude korrigeerimiste sünkroonimine rakendusest Field Service rakendusse Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="461d1-103">Synchronize inventory adjustments from Field Service to Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="461d1-104">Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse varude korrigeerimiste ja üleviimiste sünkroonimiseks rakendusest Dynamics 365 Supply Chain Management rakendusse Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="461d1-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="461d1-105">[![Äriprotsesside sünkroonimine rakenduste Supply Chain Management ja Field Service vahel](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="461d1-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="461d1-106">Mallid ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="461d1-106">Templates and tasks</span></span>
<span data-ttu-id="461d1-107">Varude korrigeerimiste ja üleviimiste sünkroonimiseks rakendusest Field Service rakendusse Supply Chain Management kasutatakse järgmist malli ja aluseks olevaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="461d1-107">The following template and underlying tasks are used to synchronize inventory adjustments and transfers from Field Service to Supply Chain Management.</span></span>

<span data-ttu-id="461d1-108">**Mallid andmeintegratsioonis**</span><span class="sxs-lookup"><span data-stu-id="461d1-108">**Templates in Data integration**</span></span>
- <span data-ttu-id="461d1-109">Varude korrigeerimine (rakendusest Field Service rakendusse Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="461d1-109">Inventory Adjustment (Field Service to Supply Chain Management)</span></span>
- <span data-ttu-id="461d1-110">Varude üleviimised (rakendusest Field Service rakendusse Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="461d1-110">Inventory Transfers (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="461d1-111">**Ülesanded andmeintegratsiooni projektides**</span><span class="sxs-lookup"><span data-stu-id="461d1-111">**Tasks in the Data integration projects**</span></span>
- <span data-ttu-id="461d1-112">Varude korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="461d1-112">Inventory Adjustments</span></span>
- <span data-ttu-id="461d1-113">Varude üleviimine</span><span class="sxs-lookup"><span data-stu-id="461d1-113">Inventory Transfers</span></span>

## <a name="entity-set"></a><span data-ttu-id="461d1-114">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="461d1-114">Entity set</span></span>
| <span data-ttu-id="461d1-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="461d1-115">Field Service</span></span>                     | <span data-ttu-id="461d1-116">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="461d1-116">Supply Chain Management</span></span>                          |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="461d1-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="461d1-117">msdyn_inventoryadjustmentproducts</span></span> |   <span data-ttu-id="461d1-118">CDS-i varude korrigeerimise töölehe päised ja read</span><span class="sxs-lookup"><span data-stu-id="461d1-118">CDS Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="461d1-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="461d1-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="461d1-120">CDS-i varude üleviimise töölehe päised ja read</span><span class="sxs-lookup"><span data-stu-id="461d1-120">CDS inventory transfer journal headers and lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="461d1-121">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="461d1-121">Entity flow</span></span>
<span data-ttu-id="461d1-122">Rakenduses Field Service tehtud varude korrigeerimised ja üleviimised sünkroonitakse rakendusse Supply Chain Management siis, kui **Sisestuse olek** muudetakse olekust **Loodud** olekusse **Sisestatud**.</span><span class="sxs-lookup"><span data-stu-id="461d1-122">Inventory adjustments and transfers made in Field Service will synchronize to Supply Chain Management after the **Post status** changes from **Created** to **Posted**.</span></span> <span data-ttu-id="461d1-123">Sellisel juhul lukustatakse korrigeerimis- või üleviimistellimus ja see muutub kirjutuskaitstuks.</span><span class="sxs-lookup"><span data-stu-id="461d1-123">When this occurs, the adjustment or the transfer order will be locked and become read only.</span></span> <span data-ttu-id="461d1-124">See tähendab, et korrigeerimised ja üleviimised saab rakendusse Supply Chain Management sisestada, kuid neid ei saa muuta.</span><span class="sxs-lookup"><span data-stu-id="461d1-124">This means that adjustments and transfers can be posted in Supply Chain Management, but cannot be modified.</span></span> <span data-ttu-id="461d1-125">Rakenduses Supply Chain Management saate seadistada pakett-töö automaatselt korrigeerimisi sisestama ja integratsiooni ajal loodud varude töölehti üle viima.</span><span class="sxs-lookup"><span data-stu-id="461d1-125">In Supply Chain Management, you can set up a batch job to automatically post the adjustments and transfer inventory journals that have been generated during the integration.</span></span> <span data-ttu-id="461d1-126">Vaadake allpoolt asuvatest eeltingimustest pakett-töö lubamise üksikasju.</span><span class="sxs-lookup"><span data-stu-id="461d1-126">See the following prerequisites for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="461d1-127">Rakenduse Field Service CRM lahendus</span><span class="sxs-lookup"><span data-stu-id="461d1-127">Field Service CRM solution</span></span> 
<span data-ttu-id="461d1-128">Üksusse **Toode** on lisatud väli **Laoühik**.</span><span class="sxs-lookup"><span data-stu-id="461d1-128">The **Inventory unit** field has been added to the **Product** entity.</span></span> <span data-ttu-id="461d1-129">See väli on vajalik, sest müügi- ja laoühik ei ole Supply Chain Managementis alati sama ning Supply Chain Managementis on laoühik laovarude jaoks vajalik.</span><span class="sxs-lookup"><span data-stu-id="461d1-129">This field is needed because the Sales and Inventory unit is not always the same in Supply Chain Management, and the Inventory Unit is needed for the Warehouse Inventory in Supply Chain Management.</span></span>
<span data-ttu-id="461d1-130">Kui määrate toote lehel Varude korrigeerimise toode nii suvandi Varude korrigeerimised kui ka Varude üleviimised puhul, tuuakse ühik varude toote väärtusest.</span><span class="sxs-lookup"><span data-stu-id="461d1-130">When you set the product on an Inventory adjustment product for both Inventory adjustments and Inventory transfers, the unit will be fetched from the inventory product value.</span></span> <span data-ttu-id="461d1-131">Kui väärtus leitakse, lukustatakse väli **Ühik** varude korrigeerimise tootele.</span><span class="sxs-lookup"><span data-stu-id="461d1-131">If a value is found, the **Unit** field will be locked on the Inventory adjustment product.</span></span>

<span data-ttu-id="461d1-132">Väli **Sisestuse olek** on lisatud nii üksusele **Varude korrigeerimine** kui ka üksusele **Varude üleviimine**.</span><span class="sxs-lookup"><span data-stu-id="461d1-132">The **Post status** field has been added to both the **Inventory adjustment** entity and the **Inventory transfer** entity.</span></span> <span data-ttu-id="461d1-133">Seda välja kasutatakse filtrina, kui korrigeerimine või üleviimine saadetakse Supply Chain Managementi.</span><span class="sxs-lookup"><span data-stu-id="461d1-133">This field is used as a filter when an adjustment or transfer is sent to Supply Chain Management.</span></span> <span data-ttu-id="461d1-134">Selle välja vaikeväärtus on Loodud (1), kuid seda ei saadeta Supply Chain Managementi.</span><span class="sxs-lookup"><span data-stu-id="461d1-134">The default for this field is Created (1), however it is not sent to Supply Chain Management.</span></span> <span data-ttu-id="461d1-135">Kui värskendate väärtuse valikule Sisestatud (2), saadetakse see Supply Chain Managementi, kuid seejärel ei saa te korrigeerimist ega üleviimist enam muuta ega uusi ridu lisada.</span><span class="sxs-lookup"><span data-stu-id="461d1-135">When you update the value to Posted (2), it is sent to Supply Chain Management, but after that you will no longer be able to change the adjustment or transfer or add new lines.</span></span>

<span data-ttu-id="461d1-136">Üksusele **Varude korrigeerimise toode** on lisatud väli **Numbriseeria**.</span><span class="sxs-lookup"><span data-stu-id="461d1-136">The **Number sequence** field has been added to the **Inventory adjustment product** entity.</span></span> <span data-ttu-id="461d1-137">See väli tagab, et integratsioonil on kordumatu number, nii et integratsioon saab korrigeerimisi luua ja värskendada.</span><span class="sxs-lookup"><span data-stu-id="461d1-137">This field ensures that the integration has a unique number, so the integration can create and update the adjustment.</span></span> <span data-ttu-id="461d1-138">Esimese varude korrigeerimise toote loomisel tekitab see üksusse **P2C Automaatnummerdus** uue kirje kasutatava numbriseeria ja prefiksi haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="461d1-138">When you create your first inventory adjustment product, it will create a new record in the **P2C AutoNumber** entity to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="461d1-139">Eeltingimused ja vastendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="461d1-139">Prerequisites and mapping setup</span></span>

### <a name="supply-chain-management"></a><span data-ttu-id="461d1-140">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="461d1-140">Supply Chain Management</span></span>
<span data-ttu-id="461d1-141">Integratsiooniga loodud integratsiooni varude töölehed saab pakett-tööga automaatselt sisestada.</span><span class="sxs-lookup"><span data-stu-id="461d1-141">The integration inventory journals generated by the integration can automatically be posted using a batch job.</span></span> <span data-ttu-id="461d1-142">Selle lubamiseks valige suvandid **Varude haldus > Perioodilised ülesanded > CDS-integratsioon > Integratsiooni varude töölehtede sisestamine**.</span><span class="sxs-lookup"><span data-stu-id="461d1-142">This is enabled from **Inventory management > Periodic tasks > CDS integration > Post integration inventory journals**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="461d1-143">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="461d1-143">Template mapping in Data integration</span></span>

<span data-ttu-id="461d1-144">Järgmistel joonistel on näidatud malli vastendamine andmete integratsioonis.</span><span class="sxs-lookup"><span data-stu-id="461d1-144">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a><span data-ttu-id="461d1-145">Varude korrigeerimine (rakendusest Field Service rakendusse Supply Chain Management): varude korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="461d1-145">Inventory adjustment (Field Service to Supply Chain Management): Inventory adjustment</span></span>

<span data-ttu-id="461d1-146">[![Malli vastendamine andmete integratsioonis](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="461d1-146">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a><span data-ttu-id="461d1-147">Varude üleviimine (rakendusest Field Service rakendusse Supply Chain Management): Varude üleviimine</span><span class="sxs-lookup"><span data-stu-id="461d1-147">Inventory transfer (Field Service to Supply Chain Management): Inventory transfer</span></span>

<span data-ttu-id="461d1-148">[![Malli vastendamine andmete integratsioonis](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="461d1-148">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>
