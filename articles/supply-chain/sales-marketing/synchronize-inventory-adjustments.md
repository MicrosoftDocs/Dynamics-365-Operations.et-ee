---
title: Varude üleviimiste ja korrigeerimiste sünkroonimine rakendusest Field Service rakendusse Finance and Operations
description: Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse varude korrigeerimiste ja üleviimiste sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 01/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: aa54945cea5821da163e1f6ea1747ac29b31a3ce
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "308364"
---
# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a><span data-ttu-id="122f7-103">Varude korrigeerimiste sünkroonimine rakendusest Field Service rakendusse Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="122f7-103">Synchronize inventory adjustments from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="122f7-104">Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse varude korrigeerimiste ja üleviimiste sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="122f7-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="122f7-105">[![Äriprotsesside sünkroonimine rakenduste Finance and Operations ja Field Service vahel](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="122f7-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="122f7-106">Mallid ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="122f7-106">Templates and tasks</span></span>
<span data-ttu-id="122f7-107">Varude korrigeerimiste ja üleviimiste sünkroonimiseks rakendusest Microsoft Dynamics 365 for Field Service rakendusse Microsoft Dynamics 365 for Finance and Operations kasutatakse järgmist malli ja aluseks olevaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="122f7-107">The following template and underlying tasks are used to synchronize inventory adjustments and transfers from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="122f7-108">**Mallid andmeintegratsioonis**</span><span class="sxs-lookup"><span data-stu-id="122f7-108">**Templates in Data integration**</span></span>
- <span data-ttu-id="122f7-109">Varude korrigeerimine (rakendusest Field Service rakendusse Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="122f7-109">Inventory Adjustment (Field Service to Finance and Operations)</span></span>
- <span data-ttu-id="122f7-110">Varude üleviimine (rakendusest Field Service rakendusse Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="122f7-110">Inventory Transfers (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="122f7-111">**Ülesanded andmeintegratsiooni projektides**</span><span class="sxs-lookup"><span data-stu-id="122f7-111">**Tasks in the Data integration projects**</span></span>
- <span data-ttu-id="122f7-112">Varude korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="122f7-112">Inventory Adjustments</span></span>
- <span data-ttu-id="122f7-113">Varude üleviimine</span><span class="sxs-lookup"><span data-stu-id="122f7-113">Inventory Transfers</span></span>

## <a name="entity-set"></a><span data-ttu-id="122f7-114">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="122f7-114">Entity set</span></span>
| <span data-ttu-id="122f7-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="122f7-115">Field Service</span></span>                     | <span data-ttu-id="122f7-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="122f7-116">Finance and Operations</span></span>                             |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="122f7-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="122f7-117">msdyn_inventoryadjustmentproducts</span></span> |   <span data-ttu-id="122f7-118">CDS-i varude korrigeerimise töölehe päised ja read</span><span class="sxs-lookup"><span data-stu-id="122f7-118">CDS Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="122f7-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="122f7-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="122f7-120">CDS-i varude üleviimise töölehe päised ja read</span><span class="sxs-lookup"><span data-stu-id="122f7-120">CDS inventory transfer journal headers and lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="122f7-121">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="122f7-121">Entity flow</span></span>
<span data-ttu-id="122f7-122">Rakenduses Field Service tehtud varude korrigeerimised ja üleviimised sünkroonitakse rakendusse Finance and Operations siis, kui **Sisestuse olek** muudetakse olekust **Loodud** olekusse **Sisestatud**.</span><span class="sxs-lookup"><span data-stu-id="122f7-122">Inventory adjustments and transfers made in Field Service will synchronize to Finance and Operations after the **Post status** changes from **Created** to **Posted**.</span></span> <span data-ttu-id="122f7-123">Sellisel juhul lukustatakse korrigeerimis- või üleviimistellimus ja see muutub kirjutuskaitstuks.</span><span class="sxs-lookup"><span data-stu-id="122f7-123">When this occurs, the adjustment or the transfer order will be locked and become read only.</span></span> <span data-ttu-id="122f7-124">See tähendab, et korrigeerimised ja üleviimised saab rakendusse Finance and Operations sisestada, kuid neid ei saa muuta.</span><span class="sxs-lookup"><span data-stu-id="122f7-124">This means that adjustments and transfers can be posted in Finance and Operations, but cannot be modified.</span></span> <span data-ttu-id="122f7-125">Rakenduses Finance and Operations saate seadistada pakett-töö automaatselt korrigeerimisi sisestama ja integratsiooni ajal loodud varude töölehti üle viima.</span><span class="sxs-lookup"><span data-stu-id="122f7-125">In Finance and Operations, you can set up a batch job to automatically post the adjustments and transfer inventory journals that have been generated during the integration.</span></span> <span data-ttu-id="122f7-126">Vaadake allpoolt asuvatest eeltingimustest pakett-töö lubamise üksikasju.</span><span class="sxs-lookup"><span data-stu-id="122f7-126">See the following prerequisites for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="122f7-127">Rakenduse Field Service CRM lahendus</span><span class="sxs-lookup"><span data-stu-id="122f7-127">Field Service CRM solution</span></span> 
<span data-ttu-id="122f7-128">Üksusse **Toode** on lisatud väli **Laoühik**.</span><span class="sxs-lookup"><span data-stu-id="122f7-128">The **Inventory unit** field has been added to the **Product** entity.</span></span> <span data-ttu-id="122f7-129">See väli on vajalik, sest müügi- ja laoühik ei ole Finance and Operationsis alati sama ning Finance and Operationisis on laoühik laovarude jaoks vajalik.</span><span class="sxs-lookup"><span data-stu-id="122f7-129">This field is needed because the Sales and Inventory unit is not always the same in Finance and Operations, and the Inventory Unit is needed for the Warehouse Inventory in Finance and Operations.</span></span>
<span data-ttu-id="122f7-130">Kui määrate toote lehel Varude korrigeerimise toode nii suvandi Varude korrigeerimised kui ka Varude üleviimised puhul, tuuakse ühik varude toote väärtusest.</span><span class="sxs-lookup"><span data-stu-id="122f7-130">When you set the product on an Inventory adjustment product for both Inventory adjustments and Inventory transfers, the unit will be fetched from the inventory product value.</span></span> <span data-ttu-id="122f7-131">Kui väärtus leitakse, lukustatakse väli **Ühik** varude korrigeerimise tootele.</span><span class="sxs-lookup"><span data-stu-id="122f7-131">If a value is found, the **Unit** field will be locked on the Inventory adjustment product.</span></span>

<span data-ttu-id="122f7-132">Väli **Sisestuse olek** on lisatud nii üksusele **Varude korrigeerimine** kui ka üksusele **Varude üleviimine**.</span><span class="sxs-lookup"><span data-stu-id="122f7-132">The **Post status** field has been added to both the **Inventory adjustment** entity and the **Inventory transfer** entity.</span></span> <span data-ttu-id="122f7-133">Seda välja kasutatakse filtrina, kui korrigeerimine või üleviimine saadetakse Finance and Operationsi.</span><span class="sxs-lookup"><span data-stu-id="122f7-133">This field is used as a filter when an adjustment or transfer is sent to Finance and Operations.</span></span> <span data-ttu-id="122f7-134">Selle välja vaikeväärtus on Loodud (1), kuid seda ei saadeta Finance and Operationsisse.</span><span class="sxs-lookup"><span data-stu-id="122f7-134">The default for this field is Created (1), however it is not sent to Finance and Operations.</span></span> <span data-ttu-id="122f7-135">Kui värskendate väärtuse valikule Sisestatud (2), saadetakse see Finance and Operationsisse, kuid seejärel ei saa te korrigeerimist ega üleviimist enam muuta ega uusi ridu lisada.</span><span class="sxs-lookup"><span data-stu-id="122f7-135">When you update the value to Posted (2), it is sent to Finance and Operations, but after that you will no longer be able to change the adjustment or transfer or add new lines.</span></span>

<span data-ttu-id="122f7-136">Üksusele **Varude korrigeerimise toode** on lisatud väli **Numbriseeria**.</span><span class="sxs-lookup"><span data-stu-id="122f7-136">The **Number sequence** field has been added to the **Inventory adjustment product** entity.</span></span> <span data-ttu-id="122f7-137">See väli tagab, et integratsioonil on kordumatu number, nii et integratsioon saab korrigeerimisi luua ja värskendada.</span><span class="sxs-lookup"><span data-stu-id="122f7-137">This field ensures that the integration has a unique number, so the integration can create and update the adjustment.</span></span> <span data-ttu-id="122f7-138">Esimese varude korrigeerimise toote loomisel tekitab see üksusse **P2C Automaatnummerdus** uue kirje kasutatava numbriseeria ja prefiksi haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="122f7-138">When you create your first inventory adjustment product, it will create a new record in the **P2C AutoNumber** entity to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="122f7-139">Eeltingimused ja vastendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="122f7-139">Prerequisites and mapping setup</span></span>

### <a name="finance-and-operations"></a><span data-ttu-id="122f7-140">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="122f7-140">Finance and Operations</span></span>
<span data-ttu-id="122f7-141">Integratsiooniga loodud integratsiooni varude töölehed saab pakett-tööga automaatselt sisestada.</span><span class="sxs-lookup"><span data-stu-id="122f7-141">The integration inventory journals generated by the integration can automatically be posted using a batch job.</span></span> <span data-ttu-id="122f7-142">Selle lubamiseks valige suvandid **Varude haldus > Perioodilised ülesanded > CDS-integratsioon > Integratsiooni varude töölehtede sisestamine**.</span><span class="sxs-lookup"><span data-stu-id="122f7-142">This is enabled from **Inventory management > Periodic tasks > CDS integration > Post integration inventory journals**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="122f7-143">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="122f7-143">Template mapping in Data integration</span></span>

<span data-ttu-id="122f7-144">Järgmistel joonistel on näidatud malli vastendamine andmete integratsioonis.</span><span class="sxs-lookup"><span data-stu-id="122f7-144">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a><span data-ttu-id="122f7-145">Varude korrigeerimine (Field Service’ist Finance and Operationsisse): varude korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="122f7-145">Inventory adjustment (Field Service to Finance and Operations): Inventory adjustment</span></span>

<span data-ttu-id="122f7-146">[![Malli vastendamine andmete integratsioonis](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="122f7-146">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a><span data-ttu-id="122f7-147">Varude üleviimine (Field Service’ist Finance and Operationsisse): varude üleviimine</span><span class="sxs-lookup"><span data-stu-id="122f7-147">Inventory transfer (Field Service to Finance and Operations): Inventory transfer</span></span>

<span data-ttu-id="122f7-148">[![Malli vastendamine andmete integratsioonis](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="122f7-148">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>
