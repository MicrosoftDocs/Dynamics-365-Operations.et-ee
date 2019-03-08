---
title: Töötellimuste sünkroonimine koos projektiga rakendusest Field Service rakendusse Finance and Operations
description: Selles teemas käsitletakse malle ja aluseks olevat ülesannet, mida kasutatakse projekti numbriga töökäskude sünkroonimiseks rakendusest Microsoft Dynamics 365 for Field Service rakendusse Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
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
ms.openlocfilehash: 6b61411a5a235e2d0aad8bb25ae4a3bfcf1248d1
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "329846"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a><span data-ttu-id="ce0b0-103">Töötellimuste sünkroonimine koos projektiga rakendusest Field Service rakendusse Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ce0b0-103">Synchronize work orders with project from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ce0b0-104">Selles teemas käsitletakse malle ja aluseks olevat ülesannet, mida kasutatakse projekti numbriga töökäskude sünkroonimiseks rakendusest Microsoft Dynamics 365 for Field Service rakendusse Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ce0b0-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="ce0b0-105">[![Äriprotsesside sünkroonimine rakenduste Finance and Operations ja Field Service vahel](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="ce0b0-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="ce0b0-106">Kasutatud mall **Field Service’i tooted (Finance and Operationsist Field Service’isse)** põhineb lahenduse Potentsiaalne klient sularahaks mallil **Tooted (Finance and Operationsist Salesi) – otse**.</span><span class="sxs-lookup"><span data-stu-id="ce0b0-106">The used **Field Service Products (Finance and Operations to Field Service)** template is based on the **Products (Finance and Operations to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="ce0b0-107">Lisateabe saamiseks vt [Tooted (Finance and Operationsist Salesi) – otse](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="ce0b0-107">For more information, see [Products (Finance and Operations to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="ce0b0-108">Selles teemas kirjeldatakse ainult mallide **Field Service’i tooted (Finance and Operationsist Field Service’isse)** ja **Field Service'i tooted (Finance and Operationsist Salesi)** erinevusi.</span><span class="sxs-lookup"><span data-stu-id="ce0b0-108">This topic only describes the differences between the **Field Service Products (Finance and Operations to Field Service)** and **Field Service Products (Finance and Operations to Field Service)** templates.</span></span>

<span data-ttu-id="ce0b0-109">Peamine erinevus seisneb selles, et see mall sisaldab töötellimusele rakenduses Field Service määratud projektinumbri vastendust, mis tagab, et rakenduses Finance and Operations loodud müügitellimus sisaldab projekti numbrit ja saab toimuda seotud projekti arveldus.</span><span class="sxs-lookup"><span data-stu-id="ce0b0-109">The main difference is that this template includes mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Finance and Operations include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="ce0b0-110">Peale selle kasutab mall suvandit Täpsem päring ja filtreerimine.</span><span class="sxs-lookup"><span data-stu-id="ce0b0-110">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="ce0b0-111">Mallid ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="ce0b0-111">Templates and tasks</span></span>

<span data-ttu-id="ce0b0-112">**Malli nimi andmete integratsioonis:**</span><span class="sxs-lookup"><span data-stu-id="ce0b0-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="ce0b0-113">Töötellimused koos projektiga (rakendusest Field Service rakendusse Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="ce0b0-113">Work Orders with Project (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="ce0b0-114">**Ülesande nimi andmete integratsiooni projektis:**</span><span class="sxs-lookup"><span data-stu-id="ce0b0-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="ce0b0-115">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="ce0b0-115">WorkOrderHeader</span></span>
- <span data-ttu-id="ce0b0-116">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="ce0b0-116">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="ce0b0-117">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="ce0b0-117">WorkOrderProduct</span></span>
- <span data-ttu-id="ce0b0-118">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="ce0b0-118">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="ce0b0-119">Rakenduse Field Service CRM lahendus</span><span class="sxs-lookup"><span data-stu-id="ce0b0-119">Field Service CRM solution</span></span>
<span data-ttu-id="ce0b0-120">**Välise projekti** väli on lisatud üksusele Töökäsk.</span><span class="sxs-lookup"><span data-stu-id="ce0b0-120">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="ce0b0-121">See väli otsimine, mis märgistades teie Töökäsu Müügitellimuse projektiga ühendatakse seejärel Projektiga rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ce0b0-121">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Finance and Operations.</span></span> <span data-ttu-id="ce0b0-122">Kui **Süsteemi olek** muutub Avatud – Pooleli(690,970,000) pealt kõrgema oleku peale, lukustatakse väli  **Väline projekt** ja te ei saa selle väärtusele lisada, seda eemaldada ega muuta.</span><span class="sxs-lookup"><span data-stu-id="ce0b0-122">Ones the **System Status** changes from Open – In Progress(690,970,000) to a higher status the **External Project** field will be locked and you can't add, remove or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="ce0b0-123">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="ce0b0-123">Template mapping in Data integration</span></span>

<span data-ttu-id="ce0b0-124">Järgmistel joonistel on näidatud malli vastendamine andmete integratsioonis.</span><span class="sxs-lookup"><span data-stu-id="ce0b0-124">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheader"></a><span data-ttu-id="ce0b0-125">Töötellimused koos projektiga (rakendusest Field Service rakendusse Finance and Operations): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="ce0b0-125">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeader</span></span>

<span data-ttu-id="ce0b0-126">[![Malli vastendamine andmete integratsioonis](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="ce0b0-126">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheaderproject"></a><span data-ttu-id="ce0b0-127">Töötellimused koos projektiga (rakendusest Field Service rakendusse Finance and Operations): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="ce0b0-127">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeaderProject</span></span>

<span data-ttu-id="ce0b0-128">[![Malli vastendamine andmete integratsioonis](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="ce0b0-128">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderproduct"></a><span data-ttu-id="ce0b0-129">Töötellimused koos projektiga (rakendusest Field Service rakendusse Finance and Operations): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="ce0b0-129">Work Orders with Project (Field Service to Finance and Operations): WorkOrderProduct</span></span>

<span data-ttu-id="ce0b0-130">[![Malli vastendamine andmete integratsioonis](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="ce0b0-130">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderservice"></a><span data-ttu-id="ce0b0-131">Töötellimused koos projektiga (rakendusest Field Service rakendusse Finance and Operations): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="ce0b0-131">Work Orders with Project (Field Service to Finance and Operations): WorkOrderService</span></span>

<span data-ttu-id="ce0b0-132">[![Malli vastendamine andmete integratsioonis](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="ce0b0-132">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>
