---
title: Projektiloendi sünkroonimine rakendusest Finance and Operations rakendusse Field Service
description: Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse projektide sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 535094821ca7efa33bf40f2057fac8ffc17bb822
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843549"
---
# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a><span data-ttu-id="5b874-103">Projektiloendi sünkroonimine rakendusest Finance and Operations rakendusse Field Service</span><span class="sxs-lookup"><span data-stu-id="5b874-103">Synchronize project list from Finance and Operations to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="5b874-104">Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse projektide sünkroonimiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service.</span><span class="sxs-lookup"><span data-stu-id="5b874-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="5b874-105">[![Äriprotsesside sünkroonimine rakenduste Finance and Operations ja Field Service vahel](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="5b874-105">[![Synchronization of business processes between Finance and Operations and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="5b874-106">Mallid ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="5b874-106">Templates and tasks</span></span>
<span data-ttu-id="5b874-107">Projektide sünkroonimise käitamiseks rakendusest Microsoft Dynamics 365 for Finance and Operations rakendusse Microsoft Dynamics 365 for Field Service kasutatakse järgmisi malle ja aluseks olevaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="5b874-107">The following template and underlying tasks are used to run synchronization of projects from Microsoft Dynamics 365 for Finance and Operations to Microsoft Dynamics 365 for Field Service.</span></span>

<span data-ttu-id="5b874-108">**Mall andmeintegratsioonis**</span><span class="sxs-lookup"><span data-stu-id="5b874-108">**Template in Data integration**</span></span>
- <span data-ttu-id="5b874-109">Projektid (rakendusest Fin and Ops rakendusse Field Service)</span><span class="sxs-lookup"><span data-stu-id="5b874-109">Projects (Fin and Ops to Field Service)</span></span>

<span data-ttu-id="5b874-110">**Ülesanne andmeintegratsiooni projektis**</span><span class="sxs-lookup"><span data-stu-id="5b874-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="5b874-111">Projektid</span><span class="sxs-lookup"><span data-stu-id="5b874-111">Projects</span></span>

<span data-ttu-id="5b874-112">Enne projektide loendi sünkroonimist on nõutavad järgmised sünkroonimisülesanded.</span><span class="sxs-lookup"><span data-stu-id="5b874-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="5b874-113">Kontod (Salesist Fin and Opsi)</span><span class="sxs-lookup"><span data-stu-id="5b874-113">Accounts (Sales to Fin and Ops)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="5b874-114">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="5b874-114">Entity set</span></span>
| <span data-ttu-id="5b874-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="5b874-115">Field Service</span></span>           | <span data-ttu-id="5b874-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5b874-116">Finance and Operations</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="5b874-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="5b874-117">msdynce_externalprojects</span></span> | <span data-ttu-id="5b874-118">Projektid</span><span class="sxs-lookup"><span data-stu-id="5b874-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="5b874-119">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="5b874-119">Entity flow</span></span>
<span data-ttu-id="5b874-120">Projektid luuakse rakenduses Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5b874-120">Projects are created in Finance and Operations.</span></span> <span data-ttu-id="5b874-121">Projektid, mille **Projekti tüüp** on **Aeg ja materjal** ja **Projekti etapp** on **Pooleli**, sünkroonitakse rakenduses Field Service üksusse **Väline projekt**, sealhulgas projekti number, projekti nimi, projekti etapp ja kliendikonto andmed.</span><span class="sxs-lookup"><span data-stu-id="5b874-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="5b874-122">Loendit **Väline projekt** kasutatakse teenuse Field Service töökäskude sidumiseks rakenduse Finance and Operations projektidega.</span><span class="sxs-lookup"><span data-stu-id="5b874-122">The **External Project** list is used to pair Field service work orders with Finance and Operations projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="5b874-123">Rakenduse Field Service CRM lahendus</span><span class="sxs-lookup"><span data-stu-id="5b874-123">Field Service CRM solution</span></span>
<span data-ttu-id="5b874-124">Üksus **Väline projekt** toob kõik projektid rakendusest Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5b874-124">The **External Project** entity gets all the projects from Finance and Operations.</span></span> <span data-ttu-id="5b874-125">Üksusele **Töökäsk** on lisatud väli **Väline projekt**.</span><span class="sxs-lookup"><span data-stu-id="5b874-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="5b874-126">See on otsinguväli, nii et kui sildistate oma töökäsu projektiga, ühendatakse müügitellimus rakenduses Finance and Operations projektiga.</span><span class="sxs-lookup"><span data-stu-id="5b874-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Finance and Operations.</span></span> <span data-ttu-id="5b874-127">Kui **Süsteemi olek** muutub olekust **Avatud – pooleli (690,970,000)** kõrgemasse olekusse, lukustatakse väli **Väline projekt** ja te ei saa väärtust enam lisada, eemaldada ega muuta.</span><span class="sxs-lookup"><span data-stu-id="5b874-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="5b874-128">Eeltingimused ja vastendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="5b874-128">Prerequisites and mapping setup</span></span>
### <a name="finance-and-operations"></a><span data-ttu-id="5b874-129">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5b874-129">Finance and Operations</span></span>
<span data-ttu-id="5b874-130">Muudatuste jälgimise lubamine andmeüksuse projektide jaoks.</span><span class="sxs-lookup"><span data-stu-id="5b874-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="5b874-131">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="5b874-131">Template mapping in Data integration</span></span>


### <a name="projects-fin-and-ops-to-field-service-projects"></a><span data-ttu-id="5b874-132">Projektid (rakendusest Fin and Ops rakendusse Field Service): projektid</span><span class="sxs-lookup"><span data-stu-id="5b874-132">Projects (Fin and Ops to Field Service): Projects</span></span>

<span data-ttu-id="5b874-133">[![Malli vastendamine andmete integratsioonis](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="5b874-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>
