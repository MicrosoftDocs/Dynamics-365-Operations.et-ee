---
title: Varude üleviimiste ja korrigeerimiste sünkroonimine rakendusest Field Service rakendusse Supply Chain Management
description: Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse varude korrigeerimiste ja üleviimiste sünkroonimiseks rakendusest Dynamics 365 Supply Chain Management rakendusse Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: fce407a66c339f2ece4bbc37b30243a2ed172d0a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5251885"
---
# <a name="synchronize-inventory-transfers-and-adjustments-from-field-service-to-supply-chain-management"></a><span data-ttu-id="09f84-103">Varude üleviimiste ja korrigeerimiste sünkroonimine rakendusest Field Service rakendusse Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="09f84-103">Synchronize inventory transfers and adjustments from Field Service to Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="09f84-104">Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse varude korrigeerimiste ja üleviimiste sünkroonimiseks rakendusest Dynamics 365 Supply Chain Management rakendusse Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="09f84-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="09f84-105">[![Äriprotsesside sünkroonimine rakenduste Supply Chain Management ja Field Service vahel](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="09f84-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="09f84-106">Mallid ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="09f84-106">Templates and tasks</span></span>
<span data-ttu-id="09f84-107">Varude korrigeerimiste ja üleviimiste sünkroonimiseks rakendusest Field Service rakendusse Supply Chain Management kasutatakse järgmist malli ja aluseks olevaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="09f84-107">The following template and underlying tasks are used to synchronize inventory adjustments and transfers from Field Service to Supply Chain Management.</span></span>

<span data-ttu-id="09f84-108">**Mallid andmeintegratsioonis**</span><span class="sxs-lookup"><span data-stu-id="09f84-108">**Templates in Data integration**</span></span>
- <span data-ttu-id="09f84-109">Varude korrigeerimine (rakendusest Field Service rakendusse Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="09f84-109">Inventory Adjustment (Field Service to Supply Chain Management)</span></span>
- <span data-ttu-id="09f84-110">Varude üleviimised (rakendusest Field Service rakendusse Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="09f84-110">Inventory Transfers (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="09f84-111">**Ülesanded andmeintegratsiooni projektides**</span><span class="sxs-lookup"><span data-stu-id="09f84-111">**Tasks in the Data integration projects**</span></span>
- <span data-ttu-id="09f84-112">Varude korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="09f84-112">Inventory Adjustments</span></span>
- <span data-ttu-id="09f84-113">Varude üleviimine</span><span class="sxs-lookup"><span data-stu-id="09f84-113">Inventory Transfers</span></span>

## <a name="table-set"></a><span data-ttu-id="09f84-114">Tabelikomplekt</span><span class="sxs-lookup"><span data-stu-id="09f84-114">Table set</span></span>
| <span data-ttu-id="09f84-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="09f84-115">Field Service</span></span>                     | <span data-ttu-id="09f84-116">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="09f84-116">Supply Chain Management</span></span>                          |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="09f84-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="09f84-117">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="09f84-118">Dataverse’i varude korrigeerimise töölehe päised ja read</span><span class="sxs-lookup"><span data-stu-id="09f84-118">Dataverse Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="09f84-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="09f84-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="09f84-120">Dataverse’i varude üleviimise töölehe päised ja read</span><span class="sxs-lookup"><span data-stu-id="09f84-120">Dataverse inventory transfer journal headers and lines</span></span>   |

## <a name="table-flow"></a><span data-ttu-id="09f84-121">Tabelivoog</span><span class="sxs-lookup"><span data-stu-id="09f84-121">Table flow</span></span>
<span data-ttu-id="09f84-122">Rakenduses Field Service tehtud varude korrigeerimised ja üleviimised sünkroonitakse rakendusse Supply Chain Management siis, kui **Sisestuse olek** muudetakse olekust **Loodud** olekusse **Sisestatud**.</span><span class="sxs-lookup"><span data-stu-id="09f84-122">Inventory adjustments and transfers made in Field Service will synchronize to Supply Chain Management after the **Post status** changes from **Created** to **Posted**.</span></span> <span data-ttu-id="09f84-123">Sellisel juhul lukustatakse korrigeerimis- või üleviimistellimus ja see muutub kirjutuskaitstuks.</span><span class="sxs-lookup"><span data-stu-id="09f84-123">When this occurs, the adjustment or the transfer order will be locked and become read only.</span></span> <span data-ttu-id="09f84-124">See tähendab, et korrigeerimised ja üleviimised saab rakendusse Supply Chain Management sisestada, kuid neid ei saa muuta.</span><span class="sxs-lookup"><span data-stu-id="09f84-124">This means that adjustments and transfers can be posted in Supply Chain Management, but cannot be modified.</span></span> <span data-ttu-id="09f84-125">Rakenduses Supply Chain Management saate seadistada pakett-töö automaatselt korrigeerimisi sisestama ja integratsiooni ajal loodud varude töölehti üle viima.</span><span class="sxs-lookup"><span data-stu-id="09f84-125">In Supply Chain Management, you can set up a batch job to automatically post the adjustments and transfer inventory journals that have been generated during the integration.</span></span> <span data-ttu-id="09f84-126">Vaadake allpoolt asuvatest eeltingimustest pakett-töö lubamise üksikasju.</span><span class="sxs-lookup"><span data-stu-id="09f84-126">See the following prerequisites for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="09f84-127">Rakenduse Field Service CRM lahendus</span><span class="sxs-lookup"><span data-stu-id="09f84-127">Field Service CRM solution</span></span> 
<span data-ttu-id="09f84-128">Tabelisse **Toode** on lisatud veerg **Laoühik**.</span><span class="sxs-lookup"><span data-stu-id="09f84-128">The **Inventory unit** column has been added to the **Product** table.</span></span> <span data-ttu-id="09f84-129">See veerg on vajalik, sest müügi- ja laoühik ei ole Supply Chain Managementis alati sama ning Supply Chain Managementis on laoühik laovarude jaoks vajalik.</span><span class="sxs-lookup"><span data-stu-id="09f84-129">This column is needed because the Sales and Inventory unit is not always the same in Supply Chain Management, and the Inventory Unit is needed for the Warehouse Inventory in Supply Chain Management.</span></span>
<span data-ttu-id="09f84-130">Kui määrate toote lehel Varude korrigeerimise toode nii suvandi Varude korrigeerimised kui ka Varude üleviimised puhul, tuuakse ühik varude toote väärtusest.</span><span class="sxs-lookup"><span data-stu-id="09f84-130">When you set the product on an Inventory adjustment product for both Inventory adjustments and Inventory transfers, the unit will be fetched from the inventory product value.</span></span> <span data-ttu-id="09f84-131">Kui väärtus leitakse, lukustatakse veerg **Ühik** varude korrigeerimise tootele.</span><span class="sxs-lookup"><span data-stu-id="09f84-131">If a value is found, the **Unit** column will be locked on the Inventory adjustment product.</span></span>

<span data-ttu-id="09f84-132">Veerg **Sisestuse olek** on lisatud nii tabelile **Varude korrigeerimine** kui ka tabelile **Varude üleviimine**.</span><span class="sxs-lookup"><span data-stu-id="09f84-132">The **Post status** column has been added to both the **Inventory adjustment** table and the **Inventory transfer** table.</span></span> <span data-ttu-id="09f84-133">Seda veergu kasutatakse filtrina, kui korrigeerimine või üleviimine saadetakse Supply Chain Managementi.</span><span class="sxs-lookup"><span data-stu-id="09f84-133">This column is used as a filter when an adjustment or transfer is sent to Supply Chain Management.</span></span> <span data-ttu-id="09f84-134">Selle veeru vaikeväärtus on Loodud (1), kuid seda ei saadeta Supply Chain Managementi.</span><span class="sxs-lookup"><span data-stu-id="09f84-134">The default for this column is Created (1), however it is not sent to Supply Chain Management.</span></span> <span data-ttu-id="09f84-135">Kui värskendate väärtuse valikule Sisestatud (2), saadetakse see Supply Chain Managementi, kuid seejärel ei saa te korrigeerimist ega üleviimist enam muuta ega uusi ridu lisada.</span><span class="sxs-lookup"><span data-stu-id="09f84-135">When you update the value to Posted (2), it is sent to Supply Chain Management, but after that you will no longer be able to change the adjustment or transfer or add new lines.</span></span>

<span data-ttu-id="09f84-136">Tabelile **Varude korrigeerimise toode** on lisatud veerg **Numbriseeria**.</span><span class="sxs-lookup"><span data-stu-id="09f84-136">The **Number sequence** column has been added to the **Inventory adjustment product** table.</span></span> <span data-ttu-id="09f84-137">See veerg tagab, et integratsioonil on kordumatu number, nii et integratsioon saab korrigeerimisi luua ja värskendada.</span><span class="sxs-lookup"><span data-stu-id="09f84-137">This column ensures that the integration has a unique number, so the integration can create and update the adjustment.</span></span> <span data-ttu-id="09f84-138">Esimese varude korrigeerimise toote loomisel tekitab see tabelisse **P2C Automaatnummerdus** uue kirje kasutatava numbriseeria ja eesliite haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="09f84-138">When you create your first inventory adjustment product, it will create a new record in the **P2C AutoNumber** table to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="09f84-139">Eeltingimused ja vastendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="09f84-139">Prerequisites and mapping setup</span></span>

### <a name="supply-chain-management"></a><span data-ttu-id="09f84-140">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="09f84-140">Supply Chain Management</span></span>
<span data-ttu-id="09f84-141">Integratsiooniga loodud integratsiooni varude töölehed saab pakett-tööga automaatselt sisestada.</span><span class="sxs-lookup"><span data-stu-id="09f84-141">The integration inventory journals generated by the integration can automatically be posted using a batch job.</span></span> <span data-ttu-id="09f84-142">Selle lubamiseks valige suvandid **Varude haldus > Perioodilised ülesanded > Dataverse’i integratsioon > Integratsiooni varude töölehtede sisestamine**.</span><span class="sxs-lookup"><span data-stu-id="09f84-142">This is enabled from **Inventory management > Periodic tasks > Dataverse integration > Post integration inventory journals**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="09f84-143">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="09f84-143">Template mapping in Data integration</span></span>

<span data-ttu-id="09f84-144">Järgmistel joonistel on näidatud malli vastendamine andmete integratsioonis.</span><span class="sxs-lookup"><span data-stu-id="09f84-144">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a><span data-ttu-id="09f84-145">Varude korrigeerimine (rakendusest Field Service rakendusse Supply Chain Management): varude korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="09f84-145">Inventory adjustment (Field Service to Supply Chain Management): Inventory adjustment</span></span>

<span data-ttu-id="09f84-146">[![Malli vastendamine andmete integratsioonis](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="09f84-146">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a><span data-ttu-id="09f84-147">Varude üleviimine (rakendusest Field Service rakendusse Supply Chain Management): Varude üleviimine</span><span class="sxs-lookup"><span data-stu-id="09f84-147">Inventory transfer (Field Service to Supply Chain Management): Inventory transfer</span></span>

<span data-ttu-id="09f84-148">[![Malli vastendamine andmete integratsioonis](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="09f84-148">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]