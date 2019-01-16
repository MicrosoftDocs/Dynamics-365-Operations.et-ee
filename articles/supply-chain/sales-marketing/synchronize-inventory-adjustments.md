---
title: "Varude üleviimiste ja korrigeerimiste sünkroonimine rakendusest Field Service rakendusse Finance and Operations"
description: "See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse varude korrigeerimise ja üleviimise sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service."
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
ms.openlocfilehash: 79a1cfac3fa94223cc9af73e758ce95fd47065c9
ms.contentlocale: et-ee
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a><span data-ttu-id="d456f-103">Varude korrigeerimiste sünkroonimine rakendusest Field Service rakendusse Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d456f-103">Synchronize inventory adjustments from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="d456f-104">See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse varude korrigeerimise ja üleviimise sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="d456f-104">This topic discusses the templates and underlying tasks that are used to synchronize inventory adjustments and transfers from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="d456f-105">[![Äriprotsesside sünkroonimine rakenduste Finance and Operations ja Field Service vahel](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span><span class="sxs-lookup"><span data-stu-id="d456f-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="d456f-106">Mallid ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="d456f-106">Templates and tasks</span></span>
<span data-ttu-id="d456f-107">Järgmist malli ja aluseks olevaid ülesandeid kasutatakse varude korrigeerimise ja üleviimise sünkroonimiseks rakendusest Microsoft Dynamics 365 for Field Service rakendusse Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="d456f-107">The following template and underlying tasks are used to run synchronization of inventory adjustments and transfers from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="d456f-108">**Mallide nimi andmete integratsioonis:**</span><span class="sxs-lookup"><span data-stu-id="d456f-108">**Name of the templates in Data integration:**</span></span>
- <span data-ttu-id="d456f-109">Varude korrigeerimine (rakendusest Field Service rakendusse Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="d456f-109">Inventory Adjustment (Field Service to Finance and Operations)</span></span>
- <span data-ttu-id="d456f-110">Varude üleviimine (rakendusest Field Service rakendusse Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="d456f-110">Inventory Transfers (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="d456f-111">**Ülesannete nimed andmete integratsiooni projektides.**</span><span class="sxs-lookup"><span data-stu-id="d456f-111">**Names of the tasks in the Data integration projects:**</span></span>
- <span data-ttu-id="d456f-112">Varude korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="d456f-112">Inventory Adjustments</span></span>
- <span data-ttu-id="d456f-113">Varude üleviimine</span><span class="sxs-lookup"><span data-stu-id="d456f-113">Inventory Transfers</span></span>

## <a name="entity-set"></a><span data-ttu-id="d456f-114">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="d456f-114">Entity set</span></span>
| <span data-ttu-id="d456f-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="d456f-115">Field Service</span></span>                     | <span data-ttu-id="d456f-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d456f-116">Finance and Operations</span></span>                             |
|-----------------------------------|----------------------------------------------------|
| <span data-ttu-id="d456f-117">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="d456f-117">msdyn_inventoryadjustmentproducts</span></span> |   <span data-ttu-id="d456f-118">CDS-i varude korrigeerimise töölehe päised ja read</span><span class="sxs-lookup"><span data-stu-id="d456f-118">CDS Inventory adjustment journal headers and lines</span></span> |
| <span data-ttu-id="d456f-119">msdyn_inventoryadjustmentproducts</span><span class="sxs-lookup"><span data-stu-id="d456f-119">msdyn_inventoryadjustmentproducts</span></span> | <span data-ttu-id="d456f-120">CDS-i varude üleviimise töölehe päised ja read</span><span class="sxs-lookup"><span data-stu-id="d456f-120">CDS inventory transfer journal headers and lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="d456f-121">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="d456f-121">Entity flow</span></span>
<span data-ttu-id="d456f-122">Rakenduses Field Service tehtud varude korrigeerimine ja üleviimine sünkroonitakse rakendusse Finance and Operations siis, kui **Sisestuse olek** muudetakse olekust Loodud olekusse Sisestatud.</span><span class="sxs-lookup"><span data-stu-id="d456f-122">Inventory adjustments and transfers made in Field Service will synchronize to Finance and Operations, once the **Post status** is changed from Created to Posted.</span></span> <span data-ttu-id="d456f-123">Kui see juhtub, lukustatakse korrigeerimise või üleviimise käsk ja see muutub kirjutuskaitstuks, sest korrigeerimisi ja üleviimisi võib sisestada rakenduses Finance and Operations ning seega neid ei saa muuta.</span><span class="sxs-lookup"><span data-stu-id="d456f-123">When this happen the adjustment or transfer order will be locked and become read-only, as adjustments and transfers might be posted in Finance and Operations and therefor can't be modified.</span></span>
<span data-ttu-id="d456f-124">Rakenduses Finance and Operations saate seadistada pakett-töö automaatselt korrektuure sisestama ja integratsiooniga loodud laotöölehti üle kandma.</span><span class="sxs-lookup"><span data-stu-id="d456f-124">In Finance and Operations you can setup a batch job to automatically post the adjustments and transfer inventory journals generated with the integration.</span></span> <span data-ttu-id="d456f-125">Vaadake allpoolt asuvatest eeltingimustest pakett-töö lubamise üksikasju.</span><span class="sxs-lookup"><span data-stu-id="d456f-125">See prerequisite below for details on how to enable the batch job.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="d456f-126">Rakenduse Field Service CRM lahendus</span><span class="sxs-lookup"><span data-stu-id="d456f-126">Field Service CRM solution</span></span> 
<span data-ttu-id="d456f-127">Toote üksuse alla on lisatud väli Laoüksus.</span><span class="sxs-lookup"><span data-stu-id="d456f-127">The Inventory Unit field has been added to the Product entity.</span></span> <span data-ttu-id="d456f-128">See väli on vajalik, sest Müügi- ja laoühik ei ole Operationsis alati sama ning meil on Operationsis Laoüksust Laovarude jaoks vaja.</span><span class="sxs-lookup"><span data-stu-id="d456f-128">This field is needed since the Sales and Inventory Unit is not always the same in Operations, and for the Warehouse Inventory in operations we need the Inventory Unit.</span></span>
<span data-ttu-id="d456f-129">Kui seadistate Toote Varude korrigeerimise Toote nii Varude korrigeerimise kui ka Varude üleviimise jaoks, võetakse Üksus Toote Laotoote väärtusest.</span><span class="sxs-lookup"><span data-stu-id="d456f-129">When you set the Product on an Inventory Adjustment Product for both Inventory Adjustments and Inventory Transfers the Unit will be fetched from the Products Inventory Product value.</span></span> <span data-ttu-id="d456f-130">Kui väärtus leitakse, lukustatakse väli Varude korrigeerimise tootele</span><span class="sxs-lookup"><span data-stu-id="d456f-130">If a value is found the Unit field will be locked on the Inventory Adjustment Product</span></span>

<span data-ttu-id="d456f-131">Väli Sisestuse olek on lisatud nii Varude korrigeerimise üksusele kui ka Varude üleviimise üksusele.</span><span class="sxs-lookup"><span data-stu-id="d456f-131">The Post Status field has been added to both the Inventory Adjustment entity and the Inventory Transfer entity.</span></span> <span data-ttu-id="d456f-132">Seda välja kasutatakse filtrina, kui korrigeerimine või üleviimine saadetakse Operationsi.</span><span class="sxs-lookup"><span data-stu-id="d456f-132">This field is used as a filter for when a adjustment or transfer is sent to Operations.</span></span> <span data-ttu-id="d456f-133">Välja vaikeväärtuseks on Loodud (1) ja seejärel ei saadeta seda edasi Operationsi.</span><span class="sxs-lookup"><span data-stu-id="d456f-133">The field is defaulted to Created (1) and its then not sent over to Operations.</span></span> <span data-ttu-id="d456f-134">Kui muudate selle väärtuseks Sisestatud (2), saadetakse see edasi Operationsi, kuid siis ei saa te enam midagi Korrigeerimise või Üleviimise all muuta ega sellele ridu lisada.</span><span class="sxs-lookup"><span data-stu-id="d456f-134">Ones you change is to Posted (2) It is sent over to operations, but you will then no longer be able to change anything in the Adjustment or Transfer or add any new lines to it.</span></span>
<span data-ttu-id="d456f-135">Varude korrigeerimise tooteüksusele on lisatud väli Numbrijada.</span><span class="sxs-lookup"><span data-stu-id="d456f-135">The Number Sequence field has been added to the Inventory Adjustment Product entity.</span></span> <span data-ttu-id="d456f-136">See väli aitab integratsioonil omada kordumatut koodi, et integratsioon teaks, millal teha loomisi ja millal värskendusi.</span><span class="sxs-lookup"><span data-stu-id="d456f-136">This field helps the integration to have a Unique number, so the integration knows when to do creates and when to do updates.</span></span> <span data-ttu-id="d456f-137">Esimese Varude korrigeerimise toote loomisel tekitab see uue kirje P2C Automaatnummerduse üksusesse kasutatava numbrijada ja prefiksi säilitamiseks.</span><span class="sxs-lookup"><span data-stu-id="d456f-137">When you create your first Inventory Adjustment Product it will create a new record in the P2C AutoNumber entity to maintain the number series and the prefix that is used.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="d456f-138">Eeltingimused ja vastendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="d456f-138">Prerequisites and mapping setup</span></span>

### <a name="in-finance-and-operations"></a><span data-ttu-id="d456f-139">Rakenduses Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="d456f-139">In Finance and Operations</span></span>
<span data-ttu-id="d456f-140">Integratsiooni loodud integratsiooni laotöölehed saab pakett-tööga automaatselt postitada.</span><span class="sxs-lookup"><span data-stu-id="d456f-140">The integration inventory journals generated by the integration can automatically be posted with a batch job.</span></span> <span data-ttu-id="d456f-141">Selle lubamiseks avage: Varude haldus > Perioodilised ülesanded > CDS-integratsioon > Integratsiooni laotöölehe sisestamine</span><span class="sxs-lookup"><span data-stu-id="d456f-141">This is enabled from: Inventory management > Periodic tasks > CDS integration > Post integration inventory journals</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="d456f-142">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="d456f-142">Template mapping in Data integration</span></span>

<span data-ttu-id="d456f-143">Järgmistel joonistel on näidatud malli vastendamine andmete integratsioonis.</span><span class="sxs-lookup"><span data-stu-id="d456f-143">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a><span data-ttu-id="d456f-144">Varude korrigeerimine (Field Service'ist Finance and Operationsisse): Varude korrigeerimine</span><span class="sxs-lookup"><span data-stu-id="d456f-144">Inventory Adjustment (Field Service to Finance and Operations): Inventory Adjustment</span></span>

<span data-ttu-id="d456f-145">[![Malli vastendamine andmete integratsioonis](./media/FSAdj1.png)](./media/FSAdj1.png)</span><span class="sxs-lookup"><span data-stu-id="d456f-145">[![Template mapping in Data integration](./media/FSAdj1.png)](./media/FSAdj1.png)</span></span>


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a><span data-ttu-id="d456f-146">Varude üleviimine (Field Service'ist Finance and Operationsisse): Varude üleviimine</span><span class="sxs-lookup"><span data-stu-id="d456f-146">Inventory Transfer (Field Service to Finance and Operations): Inventory Transfer</span></span>

<span data-ttu-id="d456f-147">[![Malli vastendamine andmete integratsioonis](./media/FSTrans1.png)](./media/FSTrans1.png)</span><span class="sxs-lookup"><span data-stu-id="d456f-147">[![Template mapping in Data integration](./media/FSTrans1.png)](./media/FSTrans1.png)</span></span>

