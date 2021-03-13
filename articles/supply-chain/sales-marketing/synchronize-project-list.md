---
title: Projektiloendi sünkroonimine rakendusest Supply Chain Management rakendusse Field Service
description: Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse projektide sünkroonimiseks rakendusest Dynamics 365 Supply Chain Management rakendusse Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
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
ms.openlocfilehash: 12708b35be87baf1ad13296b56507f3246f96394
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "5010868"
---
# <a name="synchronize-project-list-from-supply-chain-management-to-field-service"></a><span data-ttu-id="43ac2-103">Projektiloendi sünkroonimine rakendusest Supply Chain Management rakendusse Field Service</span><span class="sxs-lookup"><span data-stu-id="43ac2-103">Synchronize project list from Supply Chain Management to Field Service</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="43ac2-104">Selles teemas käsitletakse malle ja aluseks olevaid ülesandeid, mida kasutatakse projektide sünkroonimiseks rakendusest Dynamics 365 Supply Chain Management rakendusse Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="43ac2-104">This topic discusses the templates and underlying tasks that are used to synchronize projects from Dynamics 365 Supply Chain Management to Dynamics 365 Field Service.</span></span>

<span data-ttu-id="43ac2-105">[![Äriprotsesside sünkroonimine rakenduste Supply Chain Management ja Field Service vahel](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span><span class="sxs-lookup"><span data-stu-id="43ac2-105">[![Synchronization of business processes between Supply Chain Management and Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="43ac2-106">Mallid ja ülesanded</span><span class="sxs-lookup"><span data-stu-id="43ac2-106">Templates and tasks</span></span>
<span data-ttu-id="43ac2-107">Järgmist malli ja aluseks olevaid ülesandeid kasutatakse rakendusest Supply Chain Management rakendusse Field Service projektide sünkroonimise kävitamiseks.</span><span class="sxs-lookup"><span data-stu-id="43ac2-107">The following template and underlying tasks are used to run synchronization of projects from Supply Chain Management to Field Service.</span></span>

<span data-ttu-id="43ac2-108">**Mall andmeintegratsioonis**</span><span class="sxs-lookup"><span data-stu-id="43ac2-108">**Template in Data integration**</span></span>
- <span data-ttu-id="43ac2-109">Projektid (rakendusest Supply Chain Management rakendusse Field Service)</span><span class="sxs-lookup"><span data-stu-id="43ac2-109">Projects (Supply Chain Management to Field Service)</span></span>

<span data-ttu-id="43ac2-110">**Ülesanne andmeintegratsiooni projektis**</span><span class="sxs-lookup"><span data-stu-id="43ac2-110">**Task in the Data integration project**</span></span>
- <span data-ttu-id="43ac2-111">Projektid</span><span class="sxs-lookup"><span data-stu-id="43ac2-111">Projects</span></span>

<span data-ttu-id="43ac2-112">Enne projektide loendi sünkroonimist on nõutavad järgmised sünkroonimisülesanded.</span><span class="sxs-lookup"><span data-stu-id="43ac2-112">The following synchronization tasks are required before synchronization of project list can occur:</span></span>
- <span data-ttu-id="43ac2-113">Kontod (rakendusest Müük rakendusse Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="43ac2-113">Accounts (Sales to Supply Chain Management)</span></span> 

## <a name="entity-set"></a><span data-ttu-id="43ac2-114">Üksuste komplekt</span><span class="sxs-lookup"><span data-stu-id="43ac2-114">Entity set</span></span>
| <span data-ttu-id="43ac2-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="43ac2-115">Field Service</span></span>           | <span data-ttu-id="43ac2-116">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="43ac2-116">Supply Chain Management</span></span>  |
|-------------------------|-------------------------|
|<span data-ttu-id="43ac2-117">msdynce_externalprojects</span><span class="sxs-lookup"><span data-stu-id="43ac2-117">msdynce_externalprojects</span></span> | <span data-ttu-id="43ac2-118">Projektid</span><span class="sxs-lookup"><span data-stu-id="43ac2-118">Projects</span></span>                |

## <a name="entity-flow"></a><span data-ttu-id="43ac2-119">Üksuse voog</span><span class="sxs-lookup"><span data-stu-id="43ac2-119">Entity flow</span></span>
<span data-ttu-id="43ac2-120">Projektid luuakse rakenduses Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="43ac2-120">Projects are created in Supply Chain Management.</span></span> <span data-ttu-id="43ac2-121">Projektid, mille **Projekti tüüp** on **Aeg ja materjal** ja **Projekti etapp** on **Pooleli**, sünkroonitakse rakenduses Field Service üksusse **Väline projekt**, sealhulgas projekti number, projekti nimi, projekti etapp ja kliendikonto andmed.</span><span class="sxs-lookup"><span data-stu-id="43ac2-121">Projects with **Project type** set to **Time and material** and **Project stage** set to **In process** will synchronize to the **External Project** entity in Field Service, including Project number, Project name, Project stage, and Customer account information.</span></span> <span data-ttu-id="43ac2-122">Loendit **Väline projekt** kasutatakse teenuse Field Service töökäskude sidumiseks rakenduse Supply Chain Management projektidega.</span><span class="sxs-lookup"><span data-stu-id="43ac2-122">The **External Project** list is used to pair Field service work orders with Supply Chain Management projects.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="43ac2-123">Rakenduse Field Service CRM lahendus</span><span class="sxs-lookup"><span data-stu-id="43ac2-123">Field Service CRM solution</span></span>
<span data-ttu-id="43ac2-124">Üksus **Väline projekt** toob kõik projektid rakendusest Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="43ac2-124">The **External Project** entity gets all the projects from Supply Chain Management.</span></span> <span data-ttu-id="43ac2-125">Üksusele **Töökäsk** on lisatud väli **Väline projekt**.</span><span class="sxs-lookup"><span data-stu-id="43ac2-125">The **External Project** field has been added to the **Work Order** entity.</span></span> <span data-ttu-id="43ac2-126">See on otsinguväli, nii et kui sildistate oma töökäsu projektiga, ühendatakse müügitellimus rakenduses Supply Chain Management projektiga.</span><span class="sxs-lookup"><span data-stu-id="43ac2-126">This is a lookup field, so by tagging your work order with a project, the sales order will be connected to a project within Supply Chain Management.</span></span> <span data-ttu-id="43ac2-127">Kui **Süsteemi olek** muutub olekust **Avatud – pooleli (690,970,000)** kõrgemasse olekusse, lukustatakse väli **Väline projekt** ja te ei saa väärtust enam lisada, eemaldada ega muuta.</span><span class="sxs-lookup"><span data-stu-id="43ac2-127">After the **System Status** changes **Open – In Progress(690,970,000)** to a higher status, the **External Project** field will be locked and you can no longer add, remove, or change the value.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="43ac2-128">Eeltingimused ja vastendamise seadistamine</span><span class="sxs-lookup"><span data-stu-id="43ac2-128">Prerequisites and mapping setup</span></span>
### <a name="supply-chain-management"></a><span data-ttu-id="43ac2-129">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="43ac2-129">Supply Chain Management</span></span>
<span data-ttu-id="43ac2-130">Muudatuste jälgimise lubamine andmeüksuse projektide jaoks.</span><span class="sxs-lookup"><span data-stu-id="43ac2-130">Enable change tracking for Data entity projects.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="43ac2-131">Malli vastendamine andmete integratsioonis</span><span class="sxs-lookup"><span data-stu-id="43ac2-131">Template mapping in Data integration</span></span>


### <a name="projects-supply-chain-management-to-field-service-projects"></a><span data-ttu-id="43ac2-132">Projektid (rakendusest Supply Chain Management rakendusse Field Service): projektid</span><span class="sxs-lookup"><span data-stu-id="43ac2-132">Projects (Supply Chain Management to Field Service): Projects</span></span>

<span data-ttu-id="43ac2-133">[![Malli vastendamine andmete integratsioonis](./media/FSProject1.png)](./media/FSProject1.png)</span><span class="sxs-lookup"><span data-stu-id="43ac2-133">[![Template mapping in Data integration](./media/FSProject1.png)](./media/FSProject1.png)</span></span>
