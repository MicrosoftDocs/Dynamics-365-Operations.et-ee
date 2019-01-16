---
title: "Töötellimuste sünkroonimine rakendusest Finance and Operations rakendusse Field Service"
description: "See teema käsitleb malle ja aluseks olevat ülesannet, mida kasutatakse projektinumbriga töötellimuste sünkroonimiseks rakendusest Microsoft Dynamics 365 for Field Service rakendusse Microsoft Dynamics 365 for Finance and Operations."
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
ms.openlocfilehash: f5bd6b8c554688d0d1b2bfd93a34a60a95412bf3
ms.contentlocale: et-ee
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a><span data-ttu-id="7b2b8-103">Töötellimuste sünkroonimine koos projektiga rakendusest Field Service rakendusse Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7b2b8-103">Synchronize work orders with project from Field Service to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7b2b8-104">See teema käsitleb malle ja aluseks olevat ülesannet, mida kasutatakse projektinumbriga töötellimuste sünkroonimiseks rakendusest Microsoft Dynamics 365 for Field Service rakendusse Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7b2b8-104">This topic discusses the templates and underlying task that are used to synchronize work orders with a project number from Microsoft Dynamics 365 for Field Service to Microsoft Dynamics 365 for Finance and Operations.</span></span>

<span data-ttu-id="7b2b8-105">[![Äriprotsesside sünkroonimine rakenduste Finance and Operations ja Field Service vahel](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span><span class="sxs-lookup"><span data-stu-id="7b2b8-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)</span></span>

<span data-ttu-id="7b2b8-106">Kasutatud mall **Field Service’i tooted (Finance and Operationsist Field Service’isse)** põhineb lahenduse Potentsiaalne klient sularahaks mallil **Tooted (Finance and Operationsist Salesi) – otse**.</span><span class="sxs-lookup"><span data-stu-id="7b2b8-106">The used **Field Service Products (Finance and Operations to Field Service)** template is based on the **Products (Finance and Operations to Sales) – Direct** template from Prospect to Cash.</span></span> <span data-ttu-id="7b2b8-107">Lisateabe saamiseks vt [Tooted (Finance and Operationsist Salesi) – otse](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span><span class="sxs-lookup"><span data-stu-id="7b2b8-107">For more information, see [Products (Finance and Operations to Sales) – Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).</span></span>

<span data-ttu-id="7b2b8-108">Selles teemas kirjeldatakse ainult mallide **Field Service’i tooted (Finance and Operationsist Field Service’isse)** ja **Field Service'i tooted (Finance and Operationsist Salesi)** erinevusi.</span><span class="sxs-lookup"><span data-stu-id="7b2b8-108">This topic only describes the differences between the **Field Service Products (Finance and Operations to Field Service)** and **Field Service Products (Finance and Operations to Field Service)** templates.</span></span>

<span data-ttu-id="7b2b8-109">Peamine erinevus seisneb selles, et see mall sisaldab töötellimusele rakenduses Field Service määratud projektinumbri vastendust, mis kindlustab, et rakenduses Finance and Operations loodud müügitellimus sisaldab projekti numbrit ja et saab toimuda seotud projekti arveldus.</span><span class="sxs-lookup"><span data-stu-id="7b2b8-109">The main difference is that this template include mapping of the project number asigned to the Work order in Field Service, ensuring that the Sales order created in Finance and Operations include the project number and that invoicing can happen on the related project.</span></span> <span data-ttu-id="7b2b8-110">Peale selle kasutab mall suvandit Täpsem päring ja filtreerimine.</span><span class="sxs-lookup"><span data-stu-id="7b2b8-110">Besides this the template use Advanced Query and Filtering.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="7b2b8-111">Mallid ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="7b2b8-111">Templates and tasks</span></span>

<span data-ttu-id="7b2b8-112">**Malli nimi andmete integratsioonis:**</span><span class="sxs-lookup"><span data-stu-id="7b2b8-112">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="7b2b8-113">Töötellimused koos projektiga (rakendusest Field Service rakendusse Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="7b2b8-113">Work Orders with Project (Field Service to Finance and Operations)</span></span>

<span data-ttu-id="7b2b8-114">**Ülesande nimi andmete integratsiooni projektis:**</span><span class="sxs-lookup"><span data-stu-id="7b2b8-114">**Name of the task in the Data integration project:**</span></span>

- <span data-ttu-id="7b2b8-115">WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="7b2b8-115">WorkOrderHeader</span></span>
- <span data-ttu-id="7b2b8-116">WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="7b2b8-116">WorkOrderHeaderProject</span></span>
- <span data-ttu-id="7b2b8-117">WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="7b2b8-117">WorkOrderProduct</span></span>
- <span data-ttu-id="7b2b8-118">WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="7b2b8-118">WorkOrderService</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="7b2b8-119">Rakenduse Field Service CRM lahendus</span><span class="sxs-lookup"><span data-stu-id="7b2b8-119">Field Service CRM solution</span></span>
<span data-ttu-id="7b2b8-120">**Välise projekti** väli on lisatud üksusele Töökäsk.</span><span class="sxs-lookup"><span data-stu-id="7b2b8-120">The **External Project** field has been added to the Work Order entity.</span></span> <span data-ttu-id="7b2b8-121">See väli otsimine, mis märgistades teie Töökäsu Müügitellimuse projektiga ühendatakse seejärel Projektiga rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7b2b8-121">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Finance and Operations.</span></span> <span data-ttu-id="7b2b8-122">Kui **Süsteemi olek** muutub Avatud – Pooleli(690,970,000) pealt kõrgema oleku peale, lukustatakse väli  **Väline projekt** ja te ei saa selle väärtusele lisada, seda eemaldada ega muuta.</span><span class="sxs-lookup"><span data-stu-id="7b2b8-122">Ones the **System Status** changes from Open – In Progress(690,970,000) to a higher status the **External Project** field will be locked and you can't add, remove or change the value.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="7b2b8-123">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="7b2b8-123">Template mapping in Data integration</span></span>

<span data-ttu-id="7b2b8-124">Järgmistel joonistel on näidatud malli vastendamine andmete integratsioonis.</span><span class="sxs-lookup"><span data-stu-id="7b2b8-124">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheader"></a><span data-ttu-id="7b2b8-125">Töötellimused koos projektiga (rakendusest Field Service rakendusse Finance and Operations): WorkOrderHeader</span><span class="sxs-lookup"><span data-stu-id="7b2b8-125">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeader</span></span>

<span data-ttu-id="7b2b8-126">[![Malli vastendamine andmete integratsioonis](./media/FSWOP1.png)](./media/FSWOP1.png)</span><span class="sxs-lookup"><span data-stu-id="7b2b8-126">[![Template mapping in Data integration](./media/FSWOP1.png)](./media/FSWOP1.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderheaderproject"></a><span data-ttu-id="7b2b8-127">Töötellimused koos projektiga (rakendusest Field Service rakendusse Finance and Operations): WorkOrderHeaderProject</span><span class="sxs-lookup"><span data-stu-id="7b2b8-127">Work Orders with Project (Field Service to Finance and Operations): WorkOrderHeaderProject</span></span>

<span data-ttu-id="7b2b8-128">[![Malli vastendamine andmete integratsioonis](./media/FSWOP2.png)](./media/FSWOP2.png)</span><span class="sxs-lookup"><span data-stu-id="7b2b8-128">[![Template mapping in Data integration](./media/FSWOP2.png)](./media/FSWOP2.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderproduct"></a><span data-ttu-id="7b2b8-129">Töötellimused koos projektiga (rakendusest Field Service rakendusse Finance and Operations): WorkOrderProduct</span><span class="sxs-lookup"><span data-stu-id="7b2b8-129">Work Orders with Project (Field Service to Finance and Operations): WorkOrderProduct</span></span>

<span data-ttu-id="7b2b8-130">[![Malli vastendamine andmete integratsioonis](./media/FSWOP3.png)](./media/FSWOP3.png)</span><span class="sxs-lookup"><span data-stu-id="7b2b8-130">[![Template mapping in Data integration](./media/FSWOP3.png)](./media/FSWOP3.png)</span></span>

### <a name="work-orders-with-project-field-service-to-finance-and-operations-workorderservice"></a><span data-ttu-id="7b2b8-131">Töötellimused koos projektiga (rakendusest Field Service rakendusse Finance and Operations): WorkOrderService</span><span class="sxs-lookup"><span data-stu-id="7b2b8-131">Work Orders with Project (Field Service to Finance and Operations): WorkOrderService</span></span>

<span data-ttu-id="7b2b8-132">[![Malli vastendamine andmete integratsioonis](./media/FSWOP4.png)](./media/FSWOP4.png)</span><span class="sxs-lookup"><span data-stu-id="7b2b8-132">[![Template mapping in Data integration](./media/FSWOP4.png)](./media/FSWOP4.png)</span></span>

