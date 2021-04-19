---
title: Varude taseme teabe sünkroonimine rakendusest Supply Chain Management rakendusse Field Service
description: Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse varude tasemel teabe sünkroonimiseks rakendusest Dynamics 365 Supply Chain Management rakendusse Dynamics 365 Field Service.
author: ChristianRytt
ms.date: 05/07/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: c0db0c143abb8ce26a4a3007845050e4ddb02363
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840577"
---
# <a name="synchronize-inventory-level-information-from-supply-chain-management-to-field-service"></a><span data-ttu-id="3bc2a-103">Varude taseme teabe sünkroonimine rakendusest Supply Chain Management rakendusse Field Service</span><span class="sxs-lookup"><span data-stu-id="3bc2a-103">Synchronize inventory level information from Supply Chain Management to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="3bc2a-104">Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse varude tasemel teabe sünkroonimiseks rakendusest Dynamics 365 Supply Chain Management rakendusse Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="3bc2a-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory-level information from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="3bc2a-105">[![Äriprotsesside sünkroonimine rakenduste Supply Chain Management ja Field Service vahel](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="3bc2a-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="3bc2a-106">Mallid ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="3bc2a-106">Templates and tasks</span></span>
<span data-ttu-id="3bc2a-107">Olemasolevate varude taseme sünkroonimiseks rakendusest Supply Chain Management rakendusse Field Service kasutatakse järgmist malli ja aluseks olevaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="3bc2a-107">The following template and underlying tasks are used to synchronize inventory on-hand levels from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="3bc2a-108">**Mall andmeintegratsioonis**</span><span class="sxs-lookup"><span data-stu-id="3bc2a-108">**Template in Data integration**</span></span>
- <span data-ttu-id="3bc2a-109">Tootevarud (rakendusest Supply Chain Management rakendusse Field Service)</span><span class="sxs-lookup"><span data-stu-id="3bc2a-109">Product Inventory (Supply Chain Management to Field Service)</span></span>
  
<span data-ttu-id="3bc2a-110">**Ülesanne andmeintegratsiooni projektis**</span><span class="sxs-lookup"><span data-stu-id="3bc2a-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="3bc2a-111">Tootevarud</span><span class="sxs-lookup"><span data-stu-id="3bc2a-111">Product inventory</span></span>

<span data-ttu-id="3bc2a-112">Enne kaubavarude taseme sünkroonimist on nõutavad järgmised sünkroonimisülesanded.</span><span class="sxs-lookup"><span data-stu-id="3bc2a-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="3bc2a-113">Laod (rakendusest Supply Chain Management rakendusse Field Service)</span><span class="sxs-lookup"><span data-stu-id="3bc2a-113">Warehouses (Supply Chain Management to Field Service)</span></span> 
- <span data-ttu-id="3bc2a-114">Field Service’i tooted laoühikuga (rakendusest Supply Chain Management rakendusse Müük)</span><span class="sxs-lookup"><span data-stu-id="3bc2a-114">Field Service products with Inventory unit (Supply Chain Management to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="3bc2a-115">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="3bc2a-115">Entity set</span></span>

| <span data-ttu-id="3bc2a-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="3bc2a-116">Field Service</span></span>                      | <span data-ttu-id="3bc2a-117">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="3bc2a-117">Supply Chain Management</span></span>                |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="3bc2a-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="3bc2a-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="3bc2a-119">Dataverse’i vabad varud lao järgi</span><span class="sxs-lookup"><span data-stu-id="3bc2a-119">Dataverse inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="3bc2a-120">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="3bc2a-120">Entity flow</span></span>
<span data-ttu-id="3bc2a-121">Valitud toodete varude tasemel teave saadetakse rakendusest Finance and Operations rakendusse Field Service.</span><span class="sxs-lookup"><span data-stu-id="3bc2a-121">Inventory-level information from Finance and Operation is sent to Field Service for selected products.</span></span> <span data-ttu-id="3bc2a-122">Varude tasemel teave hõlmab järgmist.</span><span class="sxs-lookup"><span data-stu-id="3bc2a-122">The inventory-level information includes:</span></span> 
- <span data-ttu-id="3bc2a-123">Vaba kaubavaru (praegune laos asuv registreeritud füüsiline kogus)</span><span class="sxs-lookup"><span data-stu-id="3bc2a-123">On hand quantity (current recorded physical quantity located in the warehouse)</span></span>
- <span data-ttu-id="3bc2a-124">Tellimusel kogus (kogu registreeritud tellimisel kogus, nagu müügitellimused)</span><span class="sxs-lookup"><span data-stu-id="3bc2a-124">On order quantity (total recorded quantity on order, such as sales orders)</span></span>
- <span data-ttu-id="3bc2a-125">Tellitud kogus (kogu registreeritud tellitud kogus, nagu ostutellimused)</span><span class="sxs-lookup"><span data-stu-id="3bc2a-125">Ordered quantity (total recorded ordered quantity, such as purchase orders)</span></span>

<span data-ttu-id="3bc2a-126">See teave hõivatakse iga lao iga väljastatud toote kohta ja sünkroonitakse muutuse jälgimise põhjal, kui kaubavaru tase muutub.</span><span class="sxs-lookup"><span data-stu-id="3bc2a-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="3bc2a-127">Rakenduses Field Service loob integratsioonilahendus deltale varude töölehed, et rakenduse Field Service tasemed vastaksid rakenduse Supply Chain Management tasemetele.</span><span class="sxs-lookup"><span data-stu-id="3bc2a-127">In Field Service, the integration solution creates inventory journals for the delta, so that the levels in Field Service match the levels in Supply Chain Management.</span></span>

<span data-ttu-id="3bc2a-128">Rakendus Supply Chain Management toimib kaubavarude tasemete koondina.</span><span class="sxs-lookup"><span data-stu-id="3bc2a-128">Supply Chain Management will act as the master for inventory levels.</span></span> <span data-ttu-id="3bc2a-129">Seega on oluline seadistada töökäskude, üleviimiste ja korrigeerimiste integreerimine rakendusest Field Service rakendusse Supply Chain Management kui seda funktsiooni kasutatakse rakenduses Field Service koos varude tasemete sünkroonimisega rakendusest Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3bc2a-129">Therefore it is important to set up integration for work orders, transfers, and adjustments from Field Service to Supply Chain Management if this functionality is used in Field Service, together with synchronization of inventory levels from Supply Chain Management.</span></span>

<span data-ttu-id="3bc2a-130">Tooteid ja ladusid, kus varude tase koondatakse rakendusest Supply Chain Management, saab juhtida jaotisest Täpsem päring ja filtreerimine (Power Query).</span><span class="sxs-lookup"><span data-stu-id="3bc2a-130">The products and warehouses where inventory levels are mastered from Supply Chain Management can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

> [!NOTE]
> <span data-ttu-id="3bc2a-131">Rakenduses Field Service on võimalik luua mitmeid ladusid (seadistusega **On väliselt hallatav = Ei**) ja seejärel vastendada need ühe laoga rakenduses Supply Chain Management koos täpsema päringu ja filtreerimise funktsiooniga.</span><span class="sxs-lookup"><span data-stu-id="3bc2a-131">It is possible to create multiple warehouses in Field Services (with **Is Externally Maintained = No**) and then map them to a single warehouse in Supply Chain Management, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="3bc2a-132">Seda kasutakse olukordades, kus soovite, et rakendus Field Service koondab üksikasjaliku varude taseme ja saadab ainult värskendused rakendusse Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3bc2a-132">This is used in situations where you want Field Service to master the detailed inventory level and only send updates to Supply Chain Management.</span></span> <span data-ttu-id="3bc2a-133">Sellisel juhul ei saa Field Service varude taseme värskendusi rakendusest Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="3bc2a-133">In this case, Field Service will not receive inventory-level updates from Supply Chain Management.</span></span> <span data-ttu-id="3bc2a-134">Lisateavet vt teemadest [Varude korrigeerimiste sünkroonimine rakendusest Field Service rakendusse Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) ja [Töökäskude sünkroonimine rakenduses Field Service rakenduses Supply Chain Management projektiga seotud müügitellimustega](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="3bc2a-134">For additional information, see [Synchronize inventory adjustments from Field Service to Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) and [Synchronize work orders in Field Service to sales orders linked to project in Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="3bc2a-135">Rakenduse Field Service CRM lahendus</span><span class="sxs-lookup"><span data-stu-id="3bc2a-135">Field Service CRM solution</span></span>
<span data-ttu-id="3bc2a-136">**Välised tootevarud** on uus üksus, mida kasutatakse ainult integratsiooni tagaserveris.</span><span class="sxs-lookup"><span data-stu-id="3bc2a-136">The **External product inventory** entity is only used for back end in to the integration.</span></span> <span data-ttu-id="3bc2a-137">See üksus saab kaubavarude taseme väärtused rakendusest Supply Chain Management integratsioonis ja seejärel muudab need väärtused käsitsi varude töölehtedeks, mis seejärel muudab varude tooteid laos.</span><span class="sxs-lookup"><span data-stu-id="3bc2a-137">This entity receives the inventory level values from Supply Chain Management in the integration and then transforms those values to Manual inventory journals, which then changes the Inventory products in the Warehouse.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="3bc2a-138">Eeltingimused ja vastendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="3bc2a-138">Prerequisites and mapping setup</span></span>

### <a name="data-integration"></a><span data-ttu-id="3bc2a-139">Andmete integratsioon</span><span class="sxs-lookup"><span data-stu-id="3bc2a-139">Data integration</span></span>
<span data-ttu-id="3bc2a-140">Et projekt töötaks peate tagama, et uuendatakse integreerimisvõtit msdynce_externalproductinventories jaoks.</span><span class="sxs-lookup"><span data-stu-id="3bc2a-140">For the project to work, you need to ensure that the Integration key is updated for msdynce_externalproductinventories.</span></span>
1.  <span data-ttu-id="3bc2a-141">Avage **Andmete integreerimine > Ühenduskomplektid**.</span><span class="sxs-lookup"><span data-stu-id="3bc2a-141">Go to **Data integration > Connection sets**.</span></span>
2.  <span data-ttu-id="3bc2a-142">Valige kasutatav ühenduskomplekt.</span><span class="sxs-lookup"><span data-stu-id="3bc2a-142">Select the used Connection set.</span></span>
3.  <span data-ttu-id="3bc2a-143">Vahekaardil **Integreerimisvõti** veenduge, et lisatakse järgmised võtmed toodetele msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="3bc2a-143">On the **Integration key** tab, ensure that the following keys are added to msdynce_externalproductinventories:</span></span>
      - <span data-ttu-id="3bc2a-144">msdynce_productnumber (tootenumber)</span><span class="sxs-lookup"><span data-stu-id="3bc2a-144">msdynce_productnumber (Product Number)</span></span>
      - <span data-ttu-id="3bc2a-145">msdynce_warehouseid (lao ID)</span><span class="sxs-lookup"><span data-stu-id="3bc2a-145">msdynce_warehouseid (Warehouse ID)</span></span>
      
### <a name="data-integration-project"></a><span data-ttu-id="3bc2a-146">Andmeintegratsiooni projekt</span><span class="sxs-lookup"><span data-stu-id="3bc2a-146">Data integration project</span></span>
<span data-ttu-id="3bc2a-147">Saate rakendada filtreid täpsema päringu ja filtreerimise abil, nii et ainult teatud tooted ja laod saadavad varude tasemel teavet rakendusest Supply Chain Management rakendusse Field Service.</span><span class="sxs-lookup"><span data-stu-id="3bc2a-147">You can apply filters with Advanced Query and Filtering so that only certain products and warehouses send inventory-level information from Supply Chain Management to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="3bc2a-148">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="3bc2a-148">Template mapping in Data integration</span></span>

### <a name="product-inventory-supply-chain-management-to-field-service-product-inventory"></a><span data-ttu-id="3bc2a-149">Tootevarud (rakendusest Supply Chain Management rakendusse Field Service): tootevarud</span><span class="sxs-lookup"><span data-stu-id="3bc2a-149">Product inventory (Supply Chain Management to Field Service): Product inventory</span></span>

<span data-ttu-id="3bc2a-150">[![Malli vastendamine andmete integratsioonis](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="3bc2a-150">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]