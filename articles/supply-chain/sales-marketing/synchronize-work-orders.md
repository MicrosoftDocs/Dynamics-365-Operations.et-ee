---
title: Töötellimuste sünkroonimine koos projektiga rakendusest Field Service rakendusse Finance and Operations
description: Selles teemas käsitletakse malle ja aluseks olevat ülesannet, mida kasutatakse projekti numbriga töökäskude sünkroonimiseks rakendusest Microsoft Dynamics 365 for Field Service rakendusse Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
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
ms.openlocfilehash: 5ca01b085315d916a18c512af28fc7534ce76ee8
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1536729"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a><span data-ttu-id="da456-103">Töötellimuste sünkroonimine koos projektiga rakendusest Field Service rakendusse Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="da456-103">Synchronize work orders with project from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="da456-104">Selles teemas käsitletakse malle ja aluseks olevat ülesannet, mida kasutatakse projekti numbriga töökäskude sünkroonimiseks rakendusest Microsoft Dynamics 365 for Field Service rakendusse Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="da456-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="da456-105">[![Äriprotsesside sünkroonimine rakenduste Finance and Operations ja Field Service vahel](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="da456-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="da456-106">Kasutatud mall **Töötellimused koos projektiga (rakendusest Field Service rakendusse Finance and Operations)** põhineb lahenduse mallil **Töötellimused (rakendusest Field Service rakendusse Finance and Operations)**.</span><span class="sxs-lookup"><span data-stu-id="da456-106">The used **Work Orders with Project (Field Service to Fin and Ops)** template is based on the **Work Orders (Field Service to Fin and Ops)** template.</span></span> <span data-ttu-id="da456-107">Lisateavet vt jaotisest [Rakenduse Field Service töötellimuste sünkroonimine rakenduse Finance and Operations müügitellimustega](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="da456-107">For more information, see [Synchronize work orders in Field Service to sales orders in Finance and Operations](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

<span data-ttu-id="da456-108">Selles teemas kirjeldatakse ainult kahe malli vahelisi erinevusi:</span><span class="sxs-lookup"><span data-stu-id="da456-108">This topic only describes the differences between the two templates:</span></span>
- <span data-ttu-id="da456-109">**Töötellimused koos projektiga (rakendusest Field Service rakendusse Finance and Operations)**</span><span class="sxs-lookup"><span data-stu-id="da456-109">**Work Orders with Project (Field Service to Fin and Ops)**</span></span>
- <span data-ttu-id="da456-110">**Töötellimused (rakendusest Field Service rakendusse Finance and Operations)**</span><span class="sxs-lookup"><span data-stu-id="da456-110">**Work Orders (Field Service to Fin and Ops)**</span></span>

<span data-ttu-id="da456-111">Peamine erinevus seisneb selles, et see mall sisaldab töötellimusele rakenduses Field Service määratud projektinumbri vastendust, mis tagab, et rakenduses Finance and Operations loodud müügitellimus sisaldab projekti numbrit ja saab toimuda seotud projekti arveldus.</span><span class="sxs-lookup"><span data-stu-id="da456-111">The main difference is that this template includes mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Finance and Operations include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="da456-112">Peale selle kasutab mall suvandit Täpsem päring ja filtreerimine.</span><span class="sxs-lookup"><span data-stu-id="da456-112">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="da456-113">Mallid ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="da456-113">Templates and tasks</span></span>

<span data-ttu-id="da456-114">**Malli nimi andmete integratsioonis:**</span><span class="sxs-lookup"><span data-stu-id="da456-114">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="da456-115">Töötellimused koos projektiga (rakendusest Field Service rakendusse Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="da456-115">Work Orders with Project (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="da456-116">**Ülesande nimi andmete integratsiooni projektis:**</span><span class="sxs-lookup"><span data-stu-id="da456-116">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="da456-117">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="da456-117">WorkOrderHeader</span></span>
- <span data-ttu-id="da456-118">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="da456-118">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="da456-119">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="da456-119">WorkOrderProduct</span></span>
- <span data-ttu-id="da456-120">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="da456-120">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="da456-121">Rakenduse Field Service CRM lahendus</span><span class="sxs-lookup"><span data-stu-id="da456-121">Field Service CRM solution</span></span>
<span data-ttu-id="da456-122">**Välise projekti** väli on lisatud üksusele Töökäsk.</span><span class="sxs-lookup"><span data-stu-id="da456-122">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="da456-123">See väli otsimine, mis märgistades teie Töökäsu Müügitellimuse projektiga ühendatakse seejärel Projektiga rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="da456-123">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Finance and Operations.</span></span> <span data-ttu-id="da456-124">Kui **Süsteemi olek** muutub Avatud – Pooleli(690,970,000) pealt kõrgema oleku peale, lukustatakse väli  **Väline projekt** ja te ei saa selle väärtusele lisada, seda eemaldada ega muuta.</span><span class="sxs-lookup"><span data-stu-id="da456-124">Ones the **System Status** changes from Open – In Progress(690,970,000) to a higher status the **External Project** field will be locked and you can't add, remove or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="da456-125">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="da456-125">Template mapping in Data integration</span></span>

<span data-ttu-id="da456-126">Järgmistel joonistel on näidatud malli vastendamine andmete integratsioonis.</span><span class="sxs-lookup"><span data-stu-id="da456-126">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheader"></a><span data-ttu-id="da456-127">Töötellimused koos projektiga (rakendusest Field Service rakendusse Finance and Operations): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="da456-127">Work Orders with Project (Field Service to Fin and Ops): WorkOrderHeader</span></span>

<span data-ttu-id="da456-128">[![Malli vastendamine andmete integratsioonis](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="da456-128">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheaderproject"></a><span data-ttu-id="da456-129">Töötellimused koos projektiga (rakendusest Field Service rakendusse Finance and Operations): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="da456-129">Work Orders with Project (Field Service to Fin and Ops): WorkOrderHeaderProject</span></span>

<span data-ttu-id="da456-130">[![Malli vastendamine andmete integratsioonis](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="da456-130">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderproduct"></a><span data-ttu-id="da456-131">Töötellimused koos projektiga (rakendusest Field Service rakendusse Finance and Operations): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="da456-131">Work Orders with Project (Field Service to Fin and Ops): WorkOrderProduct</span></span>

<span data-ttu-id="da456-132">[![Malli vastendamine andmete integratsioonis](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="da456-132">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderservice"></a><span data-ttu-id="da456-133">Töötellimused koos projektiga (rakendusest Field Service rakendusse Finance and Operations): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="da456-133">Work Orders with Project (Field Service to Fin and Ops): WorkOrderService</span></span>

<span data-ttu-id="da456-134">[![Malli vastendamine andmete integratsioonis](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="da456-134">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
