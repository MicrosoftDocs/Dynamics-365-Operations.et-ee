---
title: "Projektiloendi sünkroonimine rakendusest Finance and Operations rakendusse Field Service"
description: "See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse projektide sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service."
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
ms.openlocfilehash: adcb1c1b241ce2b073cd26cf2a8a8d64931c8b0f
ms.contentlocale: et-ee
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a><span data-ttu-id="68aab-103">Projektiloendi sünkroonimine rakendusest Finance and Operations rakendusse Field Service</span><span class="sxs-lookup"><span data-stu-id="68aab-103">Synchronize project list from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="68aab-104">See teema käsitleb malle ja aluseks olevaid ülesandeid, mida kasutatakse projektide sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="68aab-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="68aab-105">[![Äriprotsesside sünkroonimine rakenduste Finance and Operations ja Field Service vahel](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="68aab-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="68aab-106">Mallid ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="68aab-106">Templates and tasks</span></span>
<span data-ttu-id="68aab-107">Järgmist malli ja aluseks olevaid ülesandeid kasutatakse projektide sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="68aab-107">The following template and underlying tasks are used to run synchronization of projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="68aab-108">**Malli nimi andmete integratsioonis:**</span><span class="sxs-lookup"><span data-stu-id="68aab-108">**Name of the template in Data integration:**</span></span>
- <span data-ttu-id="68aab-109">Projektid (rakendusest Finance and Operations rakendusse Field Service)</span><span class="sxs-lookup"><span data-stu-id="68aab-109">Projects (Finance and Operations to Field Service)</span></span>

<span data-ttu-id="68aab-110">**Ülesannete nimed andmete integratsiooni projektis.**</span><span class="sxs-lookup"><span data-stu-id="68aab-110">**Names of the tasks in the Data integration project:**</span></span>
- <span data-ttu-id="68aab-111">Projektid</span><span class="sxs-lookup"><span data-stu-id="68aab-111">Projects</span></span>

<span data-ttu-id="68aab-112">Enne projektide loendi sünkroonimist on nõutavad järgmised sünkroonimisülesanded.</span><span class="sxs-lookup"><span data-stu-id="68aab-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="68aab-113">Kontod (Müügi integratsioon Finance and Operationsiks)</span><span class="sxs-lookup"><span data-stu-id="68aab-113">Accounts (Sales to Finance and Operations)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="68aab-114">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="68aab-114">Entity set</span></span>
<span data-ttu-id="68aab-115">Field Service   Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="68aab-115">Field Service   Finance and Operations</span></span>

| <span data-ttu-id="68aab-116">Field Service</span><span class="sxs-lookup"><span data-stu-id="68aab-116">Field Service</span></span>           | <span data-ttu-id="68aab-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="68aab-117">Finance and Operations</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="68aab-118">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="68aab-118">msdynce_externalprojects</span></span> | <span data-ttu-id="68aab-119">Projektid</span><span class="sxs-lookup"><span data-stu-id="68aab-119">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="68aab-120">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="68aab-120">Entity flow</span></span>
<span data-ttu-id="68aab-121">Projektid luuakse rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="68aab-121">Projects are created in Finance and Operations.</span></span> <span data-ttu-id="68aab-122">Projektid, mille **Projekti tüüp** on Aeg ja materjal ja **Projekti etapp** on Pooleli sünkroonitakse rakenduse Field Service **Väline projekt** alla, sealhulgas projekti number, projekti nimi, projekti etapp ja kliendikonto andmed.</span><span class="sxs-lookup"><span data-stu-id="68aab-122">Projects with **Project type** Time and material and **Project stage** In process will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage and Customer account information.</span></span> <span data-ttu-id="68aab-123">**Välise projekti** loendit kasutatakse Field Service'i töökäskude sidumiseks rakenduse Finance and Operations projektidega.</span><span class="sxs-lookup"><span data-stu-id="68aab-123">The list of **External Project** is used to pair Field service Work orders with Finance and Operations projects.</span></span>
<span data-ttu-id="68aab-124">Rakenduse Field Service CRM-lahenduse Väline Projekt on uus üksus, mis saab kõik projektid Operationsist.</span><span class="sxs-lookup"><span data-stu-id="68aab-124">Field Service CRM solution The External Project is a new entity that gets all the Projects from Operations.</span></span>
<span data-ttu-id="68aab-125">Välise projekti väli on lisatud üksusele Töökäsk.</span><span class="sxs-lookup"><span data-stu-id="68aab-125">The External Project field has been added to the Work Order entity.</span></span> <span data-ttu-id="68aab-126">See väli otsimine, mis märgistades teie Töökäsu Müügitellimuse projektiga ühendatakse seejärel Projektiga Operationsis.</span><span class="sxs-lookup"><span data-stu-id="68aab-126">This field is a lookup and buy tagging your Work Order with a project the Sales Order will then be connected to a Project within Operations.</span></span> <span data-ttu-id="68aab-127">Kui süsteemi olek muudab Avatud – Pooleli(690,970,000) pealt kõrgema oleku peale, lukustatakse väli Väline projekt ja te ei saa selle väärtusele lisada, seda eemaldada ega muuta.</span><span class="sxs-lookup"><span data-stu-id="68aab-127">Ones the System Status changes Open – In Progress(690,970,000) to a higher status the External Project field will be locked and you can't add, remove or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="68aab-128">Eeltingimused ja vastendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="68aab-128">Prerequisites and mapping setup</span></span>
### <a name="in-finance-and-operations"></a><span data-ttu-id="68aab-129">Rakenduses Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="68aab-129">In Finance and Operations</span></span>
<span data-ttu-id="68aab-130">Lubage muudatuste jälgimine Andmeüksuse projektide jaoks</span><span class="sxs-lookup"><span data-stu-id="68aab-130">Enable change tracking for Data entity Projects</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="68aab-131">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="68aab-131">Template mapping in Data integration</span></span>


### <a name="projects-finance-and-operations-to-field-service-projects"></a><span data-ttu-id="68aab-132">Projektid (rakendusest Finance and Operations rakendusse Field Service): Projektid</span><span class="sxs-lookup"><span data-stu-id="68aab-132">Projects (Finance and Operations to Field Service): Projects</span></span>

<span data-ttu-id="68aab-133">[![Malli vastendamine andmete integratsioonis](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="68aab-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>

