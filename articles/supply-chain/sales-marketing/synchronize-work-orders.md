---
title: Töökäskude sünkroonimine projektiga rakendusest Field Service rakendusse Supply Chain Management
description: Selles teemas käsitletakse malle ja aluseks olevat ülesannet, mida kasutatakse projekti numbriga töökäskude sünkroonimiseks rakendusest Dynamics 365 Field Service rakendusse Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 03/12/2019
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
ms.openlocfilehash: 3ee512c2814b45a0bf35d1bee718b1ce37867bbb
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010800"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-supply-chain-management"></a><span data-ttu-id="cea41-103">Töökäskude sünkroonimine projektiga rakendusest Field Service rakendusse Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="cea41-103">Synchronize work orders with project from Field Service to Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="cea41-104">Selles teemas käsitletakse malle ja aluseks olevat ülesannet, mida kasutatakse projekti numbriga töökäskude sünkroonimiseks rakendusest Dynamics 365 Field Service rakendusse Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="cea41-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Dynamics 365 Field Service to Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="cea41-105">[![Äriprotsesside sünkroonimine rakenduste Supply Chain Management ja Field Service vahel](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="cea41-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="cea41-106">Kasutatud mall **Töötellimused koos projektiga (rakendusest Field Service rakendusse Supply Chain Management)** põhineb mallil **Töötellimused (rakendusest Field Service rakendusse Supply Chain Management)**.</span><span class="sxs-lookup"><span data-stu-id="cea41-106">The used **Work Orders with Project (Field Service to Supply Chain Management)** template is based on the **Work Orders (Field Service to Supply Chain Management)** template.</span></span> <span data-ttu-id="cea41-107">Lisateavet vt jaotisest [Rakenduse Field Service töötellimuste sünkroonimine rakenduse Supply Chain Management müügitellimustega](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span><span class="sxs-lookup"><span data-stu-id="cea41-107">For more information, see [Synchronize work orders in Field Service to sales orders in Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).</span></span>

<span data-ttu-id="cea41-108">Selles teemas kirjeldatakse ainult kahe malli vahelisi erinevusi:</span><span class="sxs-lookup"><span data-stu-id="cea41-108">This topic only describes the differences between the two templates:</span></span>
- <span data-ttu-id="cea41-109">**Projektiga töökäsud (rakendusest Field Service rakendusse Supply Chain Management)**</span><span class="sxs-lookup"><span data-stu-id="cea41-109">**Work Orders with Project (Field Service to Supply Chain Management)**</span></span>
- <span data-ttu-id="cea41-110">**Töötellimused (rakendusest Field Service rakendusse Supply Chain Management)**</span><span class="sxs-lookup"><span data-stu-id="cea41-110">**Work Orders (Field Service to Supply Chain Management)**</span></span>

<span data-ttu-id="cea41-111">Peamine erinevus seisneb selles, et see mall sisaldab töötellimusele rakenduses Field Service määratud projektinumbri vastendust, mis tagab, et rakenduses Supply Chain Management loodud müügitellimus sisaldab projekti numbrit ja saab toimuda seotud projekti arveldus.</span><span class="sxs-lookup"><span data-stu-id="cea41-111">The main difference is that this template includes mapping of the project number assigned to the Work order in Field Service, ensuring that the Sales order created in Supply Chain Management include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="cea41-112">Peale selle kasutab mall suvandit Täpsem päring ja filtreerimine.</span><span class="sxs-lookup"><span data-stu-id="cea41-112">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="cea41-113">Mallid ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="cea41-113">Templates and tasks</span></span>

<span data-ttu-id="cea41-114">**Malli nimi andmete integratsioonis:**</span><span class="sxs-lookup"><span data-stu-id="cea41-114">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="cea41-115">Projektiga töökäsud (rakendusest Field Service rakendusse Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="cea41-115">Work Orders with Project (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="cea41-116">**Ülesande nimi andmete integratsiooni projektis:**</span><span class="sxs-lookup"><span data-stu-id="cea41-116">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="cea41-117">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="cea41-117">WorkOrderHeader</span></span>
- <span data-ttu-id="cea41-118">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="cea41-118">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="cea41-119">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="cea41-119">WorkOrderProduct</span></span>
- <span data-ttu-id="cea41-120">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="cea41-120">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="cea41-121">Rakenduse Field Service CRM lahendus</span><span class="sxs-lookup"><span data-stu-id="cea41-121">Field Service CRM solution</span></span>
<span data-ttu-id="cea41-122">**Välise projekti** väli on lisatud üksusele Töökäsk.</span><span class="sxs-lookup"><span data-stu-id="cea41-122">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="cea41-123">See on otsinguväli, nii et kui sildistate oma töökäsu projektiga, ühendatakse müügitellimus rakenduses Supply Chain Management projektiga.</span><span class="sxs-lookup"><span data-stu-id="cea41-123">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Supply Chain Management.</span></span> <span data-ttu-id="cea41-124">Kui **Süsteemi olek** muutub Avatud – Pooleli(690,970,000) pealt kõrgema oleku peale, lukustatakse väli **Väline projekt** ja te ei saa selle väärtusele lisada, seda eemaldada ega muuta.</span><span class="sxs-lookup"><span data-stu-id="cea41-124">When the **System Status** changes from Open – In Progress(690,970,000) to a higher status, the **External Project** field will be locked and you can't add, remove, or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="cea41-125">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="cea41-125">Template mapping in Data integration</span></span>

<span data-ttu-id="cea41-126">Järgmistel joonistel on näidatud malli vastendamine andmete integratsioonis.</span><span class="sxs-lookup"><span data-stu-id="cea41-126">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheader"></a><span data-ttu-id="cea41-127">Projektiga töökäsud (rakendusest Field Service rakendusse Supply Chain Management): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="cea41-127">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderHeader</span></span>

<span data-ttu-id="cea41-128">[![Malli vastendamine andmete integratsioonis](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="cea41-128">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheaderproject"></a><span data-ttu-id="cea41-129">Projektiga töökäsud (rakendusest Field Service rakendusse Supply Chain Management): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="cea41-129">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderHeaderProject</span></span>

<span data-ttu-id="cea41-130">[![Malli vastendamine andmete integratsioonis](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="cea41-130">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderproduct"></a><span data-ttu-id="cea41-131">Projektiga töökäsud (rakendusest Field Service rakendusse Supply Chain Management): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="cea41-131">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderProduct</span></span>

<span data-ttu-id="cea41-132">[![Malli vastendamine andmete integratsioonis](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="cea41-132">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderservice"></a><span data-ttu-id="cea41-133">Projektiga töökäsud (rakendusest Field Service rakendusse Supply Chain Management): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="cea41-133">Work Orders with Project (Field Service to Supply Chain Management): WorkOrderService</span></span>

<span data-ttu-id="cea41-134">[![Malli vastendamine andmete integratsioonis](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="cea41-134">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
