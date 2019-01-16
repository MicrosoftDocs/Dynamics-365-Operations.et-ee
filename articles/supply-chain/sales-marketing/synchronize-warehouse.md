---
title: "Ladude sünkroonimine rakendusest Finance and Operations rakendusse Field Service"
description: "See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse ladude sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 10/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: eb8ba6051777e27bd44504a8160118e8096b1435
ms.contentlocale: et-ee
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-warehouses-from-finance-and-operations-to-field-service"></a><span data-ttu-id="58e48-103">Ladude sünkroonimine rakendusest Finance and Operations rakendusse Field Service</span><span class="sxs-lookup"><span data-stu-id="58e48-103">Synchronize warehouses from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="58e48-104">See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse ladude sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="58e48-104">This topic discusses the templates and underlying tasks that are used to synchronize warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="58e48-105">[![Äriprotsesside sünkroonimine rakenduste Finance and Operations ja Field Service vahel](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span><span class="sxs-lookup"><span data-stu-id="58e48-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSWarehouseOW.png)](./media/FSWarehouseOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="58e48-106">Mallid ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="58e48-106">Templates and tasks</span></span>
<span data-ttu-id="58e48-107">Järgmist malli ja aluseks olevaid ülesandeid kasutatakse ladude sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="58e48-107">The following template and underlying tasks are used to run synchronization of warehouses from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="58e48-108">**Malli nimi andmete integratsioonis:**</span><span class="sxs-lookup"><span data-stu-id="58e48-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="58e48-109">Laod (rakendusest Finance and Operations rakendusse Field Service)</span><span class="sxs-lookup"><span data-stu-id="58e48-109">Warehouses (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="58e48-110">**Ülesannete nimed andmete integratsiooni projektis.**</span><span class="sxs-lookup"><span data-stu-id="58e48-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="58e48-111">Ladu</span><span class="sxs-lookup"><span data-stu-id="58e48-111">Warehouse</span></span>

## <a name="entity-set"></a><span data-ttu-id="58e48-112">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="58e48-112">Entity set</span></span>
| <span data-ttu-id="58e48-113">Field Service</span><span class="sxs-lookup"><span data-stu-id="58e48-113">Field Service</span></span>    | <span data-ttu-id="58e48-114">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="58e48-114">Finance and Operations</span></span>                 |
|------------------|----------------------------------------|
| <span data-ttu-id="58e48-115">msdyn_warehouses</span><span class="sxs-lookup"><span data-stu-id="58e48-115">msdyn_warehouses</span></span> | <span data-ttu-id="58e48-116">Laod</span><span class="sxs-lookup"><span data-stu-id="58e48-116">Warehouses</span></span>                             |

## <a name="entity-flow"></a><span data-ttu-id="58e48-117">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="58e48-117">Entity flow</span></span>
<span data-ttu-id="58e48-118">Rakenduses Finance and Operations loodud ja säilitatud ladusid saab Common Data Service’i (CDS) andmeintegratsiooni projekti kaudu sünkroonida rakendusega Field Service.</span><span class="sxs-lookup"><span data-stu-id="58e48-118">Warehouses that are created and maintained in Finance and Operations can be synchronized to Field Service via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="58e48-119">Soovitud ladusid, mis sünkroonivad rakendusse Field Service, saab juhtida suvandist Täpsem projekti päring ja filtreerimine.</span><span class="sxs-lookup"><span data-stu-id="58e48-119">The desired warehouses that synchronize to Field Service can be controlled with the Advanced query and filtering on the project.</span></span> <span data-ttu-id="58e48-120">Laod, mis sünkroonivad rakendusest Finance and Operations, luuakse rakenduses Field Service, nii et väli On väliselt hallatud on seadistatud jah peale ja kirje on kirjutuskaitstud.</span><span class="sxs-lookup"><span data-stu-id="58e48-120">Warehouses that synchronize from Finance and Operations are created in Field Service with the field Is maintained externally set to Yes and the record is made read only.</span></span>
<span data-ttu-id="58e48-121">Rakenduse Field Service CRM-lahendus Rakenduste Field Service ja Finance and Operations vahelise integratsiooni toetamiseks on vajalikud rakenduse Field Service CRM lahenduse lisafunktsioonid.</span><span class="sxs-lookup"><span data-stu-id="58e48-121">Field Service CRM solution To support the integration between Field Service and Finance and Operations, additional functionality from the Field Service CRM solution is required.</span></span> <span data-ttu-id="58e48-122">Lahendus sisaldab järgmisi muudatusi.</span><span class="sxs-lookup"><span data-stu-id="58e48-122">The solution includes the following changes.</span></span>
<span data-ttu-id="58e48-123">Väli **On väliselt hallatud** on lisatud **Lao (msdyn_warehouses)** üksusele.</span><span class="sxs-lookup"><span data-stu-id="58e48-123">The field **Is Maintained Externally** has been added to the **Warehouse (msdyn_warehouses)** entity.</span></span> <span data-ttu-id="58e48-124">See väli aitab tuvastada, kas Ladu käsitletakse Operationsi alt või on see olemas ainult rakenduses Field Service.</span><span class="sxs-lookup"><span data-stu-id="58e48-124">This field helps to identify If the Warehouse is handled from Operations or if It only exists in Field Service.</span></span>
- <span data-ttu-id="58e48-125">Jah – ladu pärineb rakendusest Finance and Operations ja seda ei saa rakenduses Sales muuta.</span><span class="sxs-lookup"><span data-stu-id="58e48-125">Yes – The warehouse originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="58e48-126">Ei – ladu sisestati otse rakendusse Field Service ja seda hallatakse seal.</span><span class="sxs-lookup"><span data-stu-id="58e48-126">No – The warehouse was entered directly in Field Service and is maintained here.</span></span>

<span data-ttu-id="58e48-127">Väli **On väliselt hallatud** aitab juhtida kaubavarude taseme, korrigeerimiste, üleviimiste ja töökäskude kasutuse sünkroonimist.</span><span class="sxs-lookup"><span data-stu-id="58e48-127">The **Is Externally Maintained** field helps control the synchronization of inventory levels, adjustments, transfers and usage on work orders.</span></span> <span data-ttu-id="58e48-128">Ainult ladusid kus **On väliselt hallatud** = Jah, saab kasutada otse teise süsteemi samasse lattu sünkroonimiseks.</span><span class="sxs-lookup"><span data-stu-id="58e48-128">Only warehouses with **Is Externally Maintained** = Yes can be used to synchronize directly to the same warehouse in the other system.</span></span> 

<span data-ttu-id="58e48-129">Märkus: Rakenduses Field Services on võimalik luua mitmeid ladusid (seadistusega **Is Externally Maintained** = ei) ja seejärel vastendada need ühe laoga rakenduses Finance and Operations, koos täpsema pärinug- ja filtreerimise funktsionaalsusega.</span><span class="sxs-lookup"><span data-stu-id="58e48-129">Note: It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained** = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="58e48-130">Seda kasutakse olukordades, kus soovite, et rakendus Field Service koondab üksikasjaliku kaubavaru taseme ja lihtsalt saadab värskendused rakendusse Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="58e48-130">This is used in situations where you want Field service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="58e48-131">Sllisel juhul ei saa rakendus Field Service kaubavarude taseme värskendusi rakendusest Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="58e48-131">In this case Field service will not receive inventory level updates from Finance and Operations.</span></span> <span data-ttu-id="58e48-132">Vaadake lisainfot varude korrigeerimise rakendusest Field Service rakendusse Finance and Operations sünkroonimise alt ja sünkroonige töökäsud rakendusest Field Service projektiga seotud töökäskudesse rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="58e48-132">See additional information in Synchronize inventory adjustments from Field Service to Finance and Operations and Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="58e48-133">Eeltingimused ja vastendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="58e48-133">Prerequisites and mapping setup</span></span>
### <a name="in-the-data-integration-project"></a><span data-ttu-id="58e48-134">Andmeintegratsiooni projektis</span><span class="sxs-lookup"><span data-stu-id="58e48-134">In the Data Integration project</span></span>
<span data-ttu-id="58e48-135">Enne ladude sünkroonimist veenduge, et uuendate suvandit Täpsem projekti päring ja filtreerimine, et see sisaldaks ainult ladusid, mida tahate tuua rakendusest Finance and Operations rakendusse Field Service.</span><span class="sxs-lookup"><span data-stu-id="58e48-135">Before synchronization of the warehouses make sure to update the Advanced query and filtering on the project to only include the warehouses that you want to bring from Finance and Operations to Field Service.</span></span> <span data-ttu-id="58e48-136">ÜPange tähele, et vajate ladu rakenduses Field Service, et rakendada seda töökäskudele, korrigeerimistele ja üleviimistele.</span><span class="sxs-lookup"><span data-stu-id="58e48-136">Note that you will need the warehouse in Field Service to apply it on work orders, adjustments and transfers.</span></span>  

<span data-ttu-id="58e48-137">Veenduge, et üksuse **msdyn_workorders** jaoks oleks olemas **msdyn_warehouses**.</span><span class="sxs-lookup"><span data-stu-id="58e48-137">Ensure the **Integration key** exist for **msdyn_warehouses**</span></span>
1. <span data-ttu-id="58e48-138">Avage andmete integratsioon</span><span class="sxs-lookup"><span data-stu-id="58e48-138">Go to Data Integration</span></span>
2. <span data-ttu-id="58e48-139">Valige vahekaart **Ühenduskomplekt**</span><span class="sxs-lookup"><span data-stu-id="58e48-139">Select **Connection Set** tab</span></span>
3. <span data-ttu-id="58e48-140">Valige töökäsu sünkroonimiseks kasutatud ühenduskomplekt</span><span class="sxs-lookup"><span data-stu-id="58e48-140">Select the Connection set used for Work order synchronization</span></span>
4. <span data-ttu-id="58e48-141">Valige vahekaart **Integreerimisvõti**</span><span class="sxs-lookup"><span data-stu-id="58e48-141">Select **Integration key** tab</span></span>
5. <span data-ttu-id="58e48-142">Leidke msdyn_warehouses ja kontrollige, kas võti **msdyn_name (nimi)** on lisatud.</span><span class="sxs-lookup"><span data-stu-id="58e48-142">Find msdyn_warehouses and check that the key **msdyn_name (name)** is added.</span></span> <span data-ttu-id="58e48-143">Kui seda ei kuvata, klõpsake selle lisamiseks lehe ülaosas valikut **Lisa võti** ja **Salvesta**</span><span class="sxs-lookup"><span data-stu-id="58e48-143">If it is not shown, add it by click **Add key** and click **Save** in the top of the page</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="58e48-144">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="58e48-144">Template mapping in Data integration</span></span>

<span data-ttu-id="58e48-145">Järgmistel joonistel on näidatud malli vastendamine andmete integratsioonis.</span><span class="sxs-lookup"><span data-stu-id="58e48-145">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="warehouses-finance-and-operations-to-field-service-warehouse"></a><span data-ttu-id="58e48-146">Laod (rakendusest Finance and Operations rakendusse Field Service): Ladu</span><span class="sxs-lookup"><span data-stu-id="58e48-146">Warehouses (Finance and Operations to Field Service): Warehouse</span></span>

<span data-ttu-id="58e48-147">[![Malli vastendamine andmete integratsioonis](./media/Warehouse1.png)](./media/Warehouse1.png)</span><span class="sxs-lookup"><span data-stu-id="58e48-147">[![Template mapping in Data integration](./media/Warehouse1.png)](./media/Warehouse1.png)</span></span>

