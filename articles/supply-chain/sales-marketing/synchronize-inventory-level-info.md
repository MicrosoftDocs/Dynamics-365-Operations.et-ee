---
title: "Varude taseme teabe sünkroonimine rakendusest Finance and Operations rakendusse Field Service"
description: "See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse varude taseme andmete sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service."
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
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
ms.openlocfilehash: 3ccc4d406fa4f9800dcdf8697a91892408783196
ms.contentlocale: et-ee
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a><span data-ttu-id="add3f-103">Varude taseme teabe sünkroonimine rakendusest Finance and Operations rakendusse Field Service</span><span class="sxs-lookup"><span data-stu-id="add3f-103">Synchronize inventory level information from Finance and Operations to Field Service</span></span> 

[!include[banner](../includes/banner.md)]

<span data-ttu-id="add3f-104">See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse varude taseme andmete sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="add3f-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory level information from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="add3f-105">[![Äriprotsesside sünkroonimine rakenduste Finance and Operations ja Field Service vahel](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span><span class="sxs-lookup"><span data-stu-id="add3f-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="add3f-106">Mallid ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="add3f-106">Templates and tasks</span></span>
<span data-ttu-id="add3f-107">Järgmist malli ja aluseks olevaid ülesandeid kasutatakse vabade varude taseme sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="add3f-107">The following template and underlying tasks are used to run synchronization of inventory on-hand levels from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="add3f-108">**Malli nimi andmete integratsioonis:**</span><span class="sxs-lookup"><span data-stu-id="add3f-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="add3f-109">Tootevarud (rakendusest Finance and Operations rakendusse Field Service)</span><span class="sxs-lookup"><span data-stu-id="add3f-109">Product Inventory (Finance and Operations to Field Service)</span></span>
  
<span data-ttu-id="add3f-110">**Ülesannete nimed andmete integratsiooni projektis.**</span><span class="sxs-lookup"><span data-stu-id="add3f-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="add3f-111">Tootevarud</span><span class="sxs-lookup"><span data-stu-id="add3f-111">Product inventory</span></span>

<span data-ttu-id="add3f-112">Enne kaubavarude taseme sünkroonimist on nõutavad järgmised sünkroonimisülesanded.</span><span class="sxs-lookup"><span data-stu-id="add3f-112">The following synchronization tasks are required before synchronization of inventory levels can occur:</span></span>
- <span data-ttu-id="add3f-113">Laod (rakendusest Finance and Operations rakendusse Field Service)</span><span class="sxs-lookup"><span data-stu-id="add3f-113">Warehouses (Finance and Operations to Field Service)</span></span> 
- <span data-ttu-id="add3f-114">Field Service'i tooted laoühikuga (rakendusest Finance and Operations rakendusse Müük)</span><span class="sxs-lookup"><span data-stu-id="add3f-114">Field Service Products with Inventory unit (Finance and Operations to Sales)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="add3f-115">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="add3f-115">Entity set</span></span>

| <span data-ttu-id="add3f-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="add3f-116">Field Service</span></span>                      | <span data-ttu-id="add3f-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="add3f-117">Finance and Operations</span></span>                 |
|------------------------------------|----------------------------------------|
| <span data-ttu-id="add3f-118">msdynce_externalproductinventories</span><span class="sxs-lookup"><span data-stu-id="add3f-118">msdynce_externalproductinventories</span></span> | <span data-ttu-id="add3f-119">Vabad CDS-i varud lao järgi</span><span class="sxs-lookup"><span data-stu-id="add3f-119">CDS inventory on-hand by warehouse</span></span>     |

## <a name="entity-flow"></a><span data-ttu-id="add3f-120">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="add3f-120">Entity flow</span></span>
<span data-ttu-id="add3f-121">Valitud toodete varude taseme teave rakendusest Finance and Operations saadetakse rakendusse Field Service.</span><span class="sxs-lookup"><span data-stu-id="add3f-121">Inventory level information from Finance and Operation is send to Field Service for selected products.</span></span> <span data-ttu-id="add3f-122">Kaubavarude taseme info sisaldab järgmist.</span><span class="sxs-lookup"><span data-stu-id="add3f-122">The inventory level information include:</span></span> 
- <span data-ttu-id="add3f-123">Laos olev kogus (praegune laos asuv registreeritud füüsiline kogus)</span><span class="sxs-lookup"><span data-stu-id="add3f-123">On hand quantity (current recorded physically quantity located in the warehouse)</span></span>
- <span data-ttu-id="add3f-124">Tellimusel kogus (kogu registreeritud tellimisel kogus - st müügitellimuste kogusumma)</span><span class="sxs-lookup"><span data-stu-id="add3f-124">On order quantity (total recorded quantity on order - i.e. sales orders)</span></span>
- <span data-ttu-id="add3f-125">Tellitud kogus (kogu registreeritud tellitud kogus - st ostutellimuste kogusumma)</span><span class="sxs-lookup"><span data-stu-id="add3f-125">Ordered quantity (total recorded ordered quantity - i.e. purchase orders)</span></span>

<span data-ttu-id="add3f-126">See teave hõivatakse iga lao iga väljastatud toote kohta ja sünkroonitakse muutuse jälgimise põhjal, kui kaubavaru tase muutub.</span><span class="sxs-lookup"><span data-stu-id="add3f-126">This information is captured per released product for each warehouse and synchronized based on change tracking, when the inventory level changes.</span></span>

<span data-ttu-id="add3f-127">Rakenduses Field Service loob integreeritud lahendus deltale laotöölehti, et saada rakenduse Field Service tasemed vastama rakenduse Finance and Operations tasemetele.</span><span class="sxs-lookup"><span data-stu-id="add3f-127">In Field Service the integration solution create inventory journals for the delta, to get the levels in Field Service to match the levels in Finance and Operations.</span></span>

<span data-ttu-id="add3f-128">Rakendus Finance and Operations toimib kaubavarude tasemete koondina.</span><span class="sxs-lookup"><span data-stu-id="add3f-128">Finance and Operations will act as the master for inventory levels.</span></span> <span data-ttu-id="add3f-129">Seega on oluline seadistada töökäskude, üleviimiste ja korrigeerimiste integreerimine rakendusest Field Service rakendusse Finance and Operations, kui funktsionaalsust kasutatakse rakenduses Field Service koos kaubavarude taseme sünkroonimisega rakendusest Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="add3f-129">So it is important to setup integration for workorders, transfers and adjustments from Field Service to Finance and Operations if the this functionality is used in Field Service, together with synchronization of inventory levels from Finance and Operations.</span></span>

<span data-ttu-id="add3f-130">Tooteid ja ladusid, kus varude tase koondatakse rakendusest Finance and Operations, saab juhtida jaotisest Täpsem päring ja filtreerimine (Power Query).</span><span class="sxs-lookup"><span data-stu-id="add3f-130">The products and warehouses where inventory levels are mastered from Finance and Operations can be controlled with the Advanced Query and Filtering (Power Query).</span></span>

<span data-ttu-id="add3f-131">Märkus: Rakenduses Field Services on võimalik luua mitmeid ladusid (seadistusega On väliselt hallatav = ei) ja seejärel vastendada need ühe laoga rakenduses Finance and Operations, koos täpsema pärinug- ja filtreerimise funktsionaalsusega.</span><span class="sxs-lookup"><span data-stu-id="add3f-131">Note: It is possible to create multiple warehouses in Field Services (with Is Externally Maintained = No) and then map them to a single warehouse in Finance and Operations, with the Advanced query and filtering functionality.</span></span> <span data-ttu-id="add3f-132">Seda kasutakse olukordades, kus soovite, et rakendus Field Service koondab üksikasjaliku kaubavaru taseme ja lihtsalt saadab värskendused rakendusse Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="add3f-132">This is used in situations where you want Field service to master the detailed inventory level and just send updates to Finance and Operations.</span></span> <span data-ttu-id="add3f-133">Sllisel juhul ei saa rakendus Field Service kaubavarude taseme värskendusi rakendusest Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="add3f-133">In this case Field service will not receive inventory level updates from Finance and Operations.</span></span> <span data-ttu-id="add3f-134">Vaadake lisainfot varude korrigeerimise rakendusest Field Service rakendusse Finance and Operations sünkroonimise alt ja sünkroonige töökäsud rakendusest Field Service projektiga seotud töökäskudesse rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="add3f-134">See additional information in Synchronize inventory adjustments from Field Service to Finance and Operations and Synchronize work orders in Field Service to sales orders linked to project in Finance and Operations.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="add3f-135">Rakenduse Field Service CRM lahendus</span><span class="sxs-lookup"><span data-stu-id="add3f-135">Field Service CRM solution</span></span>
<span data-ttu-id="add3f-136">Väliste tootevarude üksus on uus üksus, mida kasutatakse ainult integratsiooni tagaserveris.</span><span class="sxs-lookup"><span data-stu-id="add3f-136">The External Product Inventory entity is a new entity that’s only used for backend in the integration.</span></span> <span data-ttu-id="add3f-137">See saab kaubavarude taseme väärtused rakendusest Finance and Operations integratsioonist ja seejärel muudab need väärtused käsitsi laotöölehtedekks, mis seejärel muudetakse lao tootevarudeks.</span><span class="sxs-lookup"><span data-stu-id="add3f-137">It receives the inventory level values from Finance and Operations in the integration and then transforms those values to Manuel Inventory journals, that then changes the Inventory Products on the Warehouse.</span></span> 

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="add3f-138">Eeltingimused ja vastendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="add3f-138">Prerequisites and mapping setup</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="add3f-139">Andmeintegratsiooni projektis</span><span class="sxs-lookup"><span data-stu-id="add3f-139">In the Data Integration project</span></span>
<span data-ttu-id="add3f-140">Rakendage filtrid suvandi Täpsem päring ja filtreerimine abil juhtimaks, et ainult soovitud tooted ja laod saadavad kaubavarude taseme andmeid rakendusest Finance and Operations rakendusse Field Service.</span><span class="sxs-lookup"><span data-stu-id="add3f-140">Apply filters with the Advanced  Query and Filtering to control that only desired products and warehouses send inventory level information from Finance and Operations to Field Service.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="add3f-141">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="add3f-141">Template mapping in Data integration</span></span>

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a><span data-ttu-id="add3f-142">Tootevarud (rakendusest Finance and Operations rakendusse Field Service): varude üleviimine</span><span class="sxs-lookup"><span data-stu-id="add3f-142">Product Inventory (Finance and Operations to Field Service): Product inventory</span></span>

<span data-ttu-id="add3f-143">[![Malli vastendamine andmete integratsioonis](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span><span class="sxs-lookup"><span data-stu-id="add3f-143">[![Template mapping in Data integration](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)</span></span>

