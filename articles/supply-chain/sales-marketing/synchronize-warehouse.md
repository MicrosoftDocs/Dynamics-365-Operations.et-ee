---
title: Ladude sünkroonimine rakendusest Supply Chain Management rakendusse Field Service
description: Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse ladude sünkroonimiseks rakendusest Dynamics 365 Supply Chain Management rakendusse Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 6617b258a85a8f45b89a38f86919b44edc2100da
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/02/2020
ms.locfileid: "3215880"
---
# <a name="synchronize-warehouses-from-supply-chain-management-to-field-service"></a><span data-ttu-id="d9be0-103">Ladude sünkroonimine rakendusest Supply Chain Management rakendusse Field Service</span><span class="sxs-lookup"><span data-stu-id="d9be0-103">Synchronize warehouses from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d9be0-104">Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse ladude sünkroonimiseks rakendusest Dynamics 365 Supply Chain Management rakendusse Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="d9be0-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="d9be0-105">[![Äriprotsesside sünkroonimine rakenduste Supply Chain Management ja Field Service vahel](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="d9be0-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="d9be0-106">Mallid ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="d9be0-106">Templates and tasks</span></span>
<span data-ttu-id="d9be0-107">Järgmist malli ja aluseks olevaid ülesandeid kasutatakse rakendusest Supply Chain Management rakendusse Field Service ladude sünkroonimise kävitamiseks.</span><span class="sxs-lookup"><span data-stu-id="d9be0-107">The following template and underlying tasks are used to run synchronization of warehouses from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="d9be0-108">**Mall andmeintegratsioonis**</span><span class="sxs-lookup"><span data-stu-id="d9be0-108">**Template in Data integration**</span></span>
- <span data-ttu-id="d9be0-109">Laod (rakendusest Supply Chain Management rakendusse Field Service)</span><span class="sxs-lookup"><span data-stu-id="d9be0-109">Warehouses (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="d9be0-110">**Ülesanne andmeintegratsiooni projektis**</span><span class="sxs-lookup"><span data-stu-id="d9be0-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="d9be0-111">Ladu</span><span class="sxs-lookup"><span data-stu-id="d9be0-111">Warehouse</span></span>

## <a name="entity-set"></a><span data-ttu-id="d9be0-112">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="d9be0-112">Entity set</span></span>
| <span data-ttu-id="d9be0-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="d9be0-113">Field Service</span></span>    | <span data-ttu-id="d9be0-114">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="d9be0-114">Supply Chain Management</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="d9be0-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="d9be0-115">msdyn_warehouses</span></span> | <span data-ttu-id="d9be0-116">Laod</span><span class="sxs-lookup"><span data-stu-id="d9be0-116">Warehouses</span></span>                             |

## <a name="entity-flow"></a><span data-ttu-id="d9be0-117">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="d9be0-117">Entity flow</span></span>
<span data-ttu-id="d9be0-118">Rakenduses Supply Chain Management loodud ja säilitatud ladusid saab Common Data Service’i (CDS) andmeintegratsiooni projekti kaudu sünkroonida rakendusega Field Service.</span><span class="sxs-lookup"><span data-stu-id="d9be0-118">Warehouses that are created and maintained in Supply Chain Management can be synchronized to Field Service via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="d9be0-119">Ladusid, mille soovite sünkroonida rakendusega Field Service, saab juhtida suvandist Täpsem projekti päring ja filtreerimine.</span><span class="sxs-lookup"><span data-stu-id="d9be0-119">The warehouses that you want to synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="d9be0-120">Laod, mis sünkroonivad rakendusest Supply Chain Management, luuakse rakenduses Field Service, nii et välja **On väliselt hallatud** väärtuseks on valitud **Jah** ja kirje on kirjutuskaitstud.</span><span class="sxs-lookup"><span data-stu-id="d9be0-120">Warehouses that synchronize from Supply Chain Management are created in Field Service with the **Is maintained externally** field set to **Yes** and the record is read only.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="d9be0-121">Rakenduse Field Service CRM lahendus</span><span class="sxs-lookup"><span data-stu-id="d9be0-121">Field Service CRM solution</span></span>
<span data-ttu-id="d9be0-122">Rakenduste Field Service ja Supply Chain Management vahelise integratsiooni toetamiseks on vajalikud rakenduse Field Service CRM lahenduse lisafunktsioonid.</span><span class="sxs-lookup"><span data-stu-id="d9be0-122">To support the integration between Field Service and Supply Chain Management, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="d9be0-123">Lahenduses on väli **On väliselt hallatud** lisatud üksusele **Lao (msdyn_warehouses)**.</span><span class="sxs-lookup"><span data-stu-id="d9be0-123">In the solution, the **Is Maintained Externally** field has been added to the **Warehouse (msdyn_warehouses)** entity.</span></span> <span data-ttu-id="d9be0-124">See väli aitab tuvastada, kas ladu käsitletakse Supply Chain Managementist või on see olemas ainult rakenduses Field Service.</span><span class="sxs-lookup"><span data-stu-id="d9be0-124">This field helps to identify if the warehouse is handled from Supply Chain Management or if it only exists in Field Service.</span></span> <span data-ttu-id="d9be0-125">Selle välja sätted on järgmised.</span><span class="sxs-lookup"><span data-stu-id="d9be0-125">The settings for this field include:</span></span>
- <span data-ttu-id="d9be0-126">**Jah**: ladu pärineb rakendusest Supply Chain Management ja seda ei saa rakenduses Sales muuta.</span><span class="sxs-lookup"><span data-stu-id="d9be0-126">**Yes** – The warehouse originated from Supply Chain Management and won't be editable in Sales.</span></span>
- <span data-ttu-id="d9be0-127">**Ei** – ladu sisestati otse rakendusse Field Service ja seda hallatakse seal.</span><span class="sxs-lookup"><span data-stu-id="d9be0-127">**No** – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="d9be0-128">Väli **On väliselt hallatud** aitab juhtida varude tasemete, korrigeerimiste, üleviimiste ja töökäskude kasutuse sünkroonimist.</span><span class="sxs-lookup"><span data-stu-id="d9be0-128">The **Is Externally Maintained** field helps control the synchronization of inventory levels, adjustments, transfers, and usage on work orders.</span></span> <span data-ttu-id="d9be0-129">Ainult ladusid, kus suvandi **On väliselt hallatud** sätteks on valitud **Jah**, saab kasutada otse teise süsteemi sama laoga sünkroonimiseks.</span><span class="sxs-lookup"><span data-stu-id="d9be0-129">Only warehouses with **Is Externally Maintained** set to **Yes** can be used to synchronize directly to the same warehouse in the other system.</span></span> 

> [!NOTE]
> <span data-ttu-id="d9be0-130">Rakenduses Field Service on võimalik luua mitmeid ladusid (seadistusega **On väliselt hallatud** = Ei) ja seejärel vastendada need ühe laoga, kasutades täpsema päringu ja filtreerimise funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="d9be0-130">It is possible to create multiple warehouses in Field Service (with **Is Externally Maintained** = No) and then map them to a single warehouse, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="d9be0-131">Seda kasutakse olukordades, kus soovite, et rakendus Field Service koondaks üksikasjaliku varude taseme ja saadaks rakendusse Supply Chain Management ainult värskendused.</span><span class="sxs-lookup"><span data-stu-id="d9be0-131">This is used in situations where you want Field Service to master the detailed inventory level and just send updates to Supply Chain Management.</span></span> <span data-ttu-id="d9be0-132">Sellisel juhul ei saa Field Service varude taseme värskendusi rakendusest Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d9be0-132">In this case, Field Service will not receive inventory-level updates from Supply Chain Management.</span></span> <span data-ttu-id="d9be0-133">Lisateavet vt teemadest [Varude korrigeerimiste sünkroonimine rakendusest Field Service rakendusse Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) ja [Töökäskude sünkroonimine rakenduses Field Service rakenduses Finance and Operations projektiga seotud müügitellimustega](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="d9be0-133">For additional information, see [Synchronize inventory adjustments from Field Service to Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="d9be0-134">Eeltingimused ja vastendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="d9be0-134">Prerequisites and mapping setup</span></span>
### <a name="data-integration-project"></a><span data-ttu-id="d9be0-135">Andmeintegratsiooni projekt</span><span class="sxs-lookup"><span data-stu-id="d9be0-135">Data Integration project</span></span>
<span data-ttu-id="d9be0-136">Enne ladude sünkroonimist värskendage kindlasti suvandit Täpsem projekti päring ja filtreerimine, et see sisaldaks ainult ladusid, mille soovite tuua rakendusest Supply Chain Management rakendusse Field Service.</span><span class="sxs-lookup"><span data-stu-id="d9be0-136">Before synchronizing the warehouses, make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Supply Chain Management to Field Service.</span></span> <span data-ttu-id="d9be0-137">Pange tähele, et vajate ladu rakenduses Field Service, et rakendada seda töökäskudele, korrigeerimistele ja üleviimistele.</span><span class="sxs-lookup"><span data-stu-id="d9be0-137">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments, and transfers.</span></span>  

<span data-ttu-id="d9be0-138">Veenduge, et üksuse **msdyn_workorders** jaoks oleks olemas **integreerimisvõti**.</span><span class="sxs-lookup"><span data-stu-id="d9be0-138">To ensure that the **Integration key** exists for **msdyn_warehouses**:</span></span>
1. <span data-ttu-id="d9be0-139">Avage andmeintegratsioon.</span><span class="sxs-lookup"><span data-stu-id="d9be0-139">Go to Data Integration.</span></span>
2. <span data-ttu-id="d9be0-140">Valige vahekaart **Ühendusekogum**.</span><span class="sxs-lookup"><span data-stu-id="d9be0-140">Select the **Connection Set** tab.</span></span>
3. <span data-ttu-id="d9be0-141">Valige töökäsu sünkroonimiseks kasutatav ühendusekogum.</span><span class="sxs-lookup"><span data-stu-id="d9be0-141">Select the connection set used for work order synchronization.</span></span>
4. <span data-ttu-id="d9be0-142">Valige vahekaart **Integreerimisvõti**.</span><span class="sxs-lookup"><span data-stu-id="d9be0-142">Select the **Integration key** tab.</span></span>
5. <span data-ttu-id="d9be0-143">Leidke msdyn_warehouses ja kontrollige, kas võti **msdyn_name (nimi)** on lisatud.</span><span class="sxs-lookup"><span data-stu-id="d9be0-143">Find msdyn_warehouses and confirm that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="d9be0-144">Kui seda ei kuvata, klõpsake selle lisamiseks käsku **Lisa võti** ja seejärel lehe ülaosas käsku **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="d9be0-144">If it is not shown, add it by clicking **Add key** and then click **Save** at the top of the page.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="d9be0-145">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="d9be0-145">Template mapping in Data integration</span></span>

<span data-ttu-id="d9be0-146">Järgmistel joonistel on näidatud malli vastendamine andmeintegratsioonis.</span><span class="sxs-lookup"><span data-stu-id="d9be0-146">The following illustration shows the template mapping in Data integration.</span></span>

### <a name="warehouses-supply-chain-management-to-field-service-warehouse"></a><span data-ttu-id="d9be0-147">Laod (rakendusest Supply Chain Management rakendusse Field Service): ladu</span><span class="sxs-lookup"><span data-stu-id="d9be0-147">Warehouses (Supply Chain Management to Field Service): Warehouse</span></span>

<span data-ttu-id="d9be0-148">[![Malli vastendamine andmete integratsioonis](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="d9be0-148">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>
