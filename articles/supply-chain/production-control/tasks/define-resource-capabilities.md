---
title: Ressursivõimaluste määratlemine
description: Ressursi võimalused kirjeldavad, milliseid operatsioone ressursid teha saavad.
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrCapability
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1ee6bfd06d7a38418812c2663695ab31701ef1ab
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843669"
---
# <a name="define-resource-capabilities"></a><span data-ttu-id="a3e29-103">Ressursivõimaluste määratlemine</span><span class="sxs-lookup"><span data-stu-id="a3e29-103">Define resource capabilities</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a3e29-104">Ressursi võimalused kirjeldavad, milliseid operatsioone ressursid teha saavad.</span><span class="sxs-lookup"><span data-stu-id="a3e29-104">Resource capabilities describe what operations resources can do.</span></span> <span data-ttu-id="a3e29-105">Planeerimisel vastendatakse iga töö ja operatsiooni nõuded saadaolevate ressursside võimalustega.</span><span class="sxs-lookup"><span data-stu-id="a3e29-105">During scheduling, the requirements of each job and operation are matched against the capabilities of the available resources.</span></span> <span data-ttu-id="a3e29-106">Selles tegevuse juhises aidatakse teil ressursi võimalust luua ja seda ressursile määrata.</span><span class="sxs-lookup"><span data-stu-id="a3e29-106">This task guide will help you create a resource capability and assign it to a resource.</span></span> <span data-ttu-id="a3e29-107">Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="a3e29-107">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-resource-capability"></a><span data-ttu-id="a3e29-108">Ressursi võimaluse loomine</span><span class="sxs-lookup"><span data-stu-id="a3e29-108">Create a resource capability</span></span>
1. <span data-ttu-id="a3e29-109">Avage Ressursi võimalused.</span><span class="sxs-lookup"><span data-stu-id="a3e29-109">Go to Resource capabilities.</span></span>
2. <span data-ttu-id="a3e29-110">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="a3e29-110">Click New.</span></span>
3. <span data-ttu-id="a3e29-111">Sisestage ressursi võimaluse ID väljale Võimalus.</span><span class="sxs-lookup"><span data-stu-id="a3e29-111">In the Capability field, type the ID of the resource capability.</span></span>
    * <span data-ttu-id="a3e29-112">Selle operatsiooni puhul kasutage võimaluse ID-d, et määrata võimalus, mis ressurssidel selle operatsiooni teostamiseks peab olema.</span><span class="sxs-lookup"><span data-stu-id="a3e29-112">For a given operation, you use the capability ID to specify that resources must have this capability to perform the operation.</span></span>  
4. <span data-ttu-id="a3e29-113">Sisestage võimaluse kirjeldus väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="a3e29-113">In the Description field, enter a description of the capability.</span></span>

## <a name="assign-capability-to-a-resource"></a><span data-ttu-id="a3e29-114">Ressursile võimaluse määramine</span><span class="sxs-lookup"><span data-stu-id="a3e29-114">Assign capability to a resource</span></span>
1. <span data-ttu-id="a3e29-115">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="a3e29-115">Click Add.</span></span>
2. <span data-ttu-id="a3e29-116">Sisestage ressursi ID väljale Ressurss.</span><span class="sxs-lookup"><span data-stu-id="a3e29-116">In the Resource field, type the ID of the resource.</span></span>
    * <span data-ttu-id="a3e29-117">Ressursi võimaluse saab määrata ühele või mitmele ressursile.</span><span class="sxs-lookup"><span data-stu-id="a3e29-117">A resource capability can be assigned to one or more resources.</span></span>  
3. <span data-ttu-id="a3e29-118">Sisestage kuupäev väljale Aegumine.</span><span class="sxs-lookup"><span data-stu-id="a3e29-118">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="a3e29-119">Saate seda välja kasutades ressursile ainult piiratud ajaks võimaluse määrata.</span><span class="sxs-lookup"><span data-stu-id="a3e29-119">You can use this field to specify that a resource has the capability for only a limited time.</span></span>  
4. <span data-ttu-id="a3e29-120">Sisestage arv väljale Prioriteet.</span><span class="sxs-lookup"><span data-stu-id="a3e29-120">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="a3e29-121">Tööde ja operatsioonide planeerimisel saate määrata, kas ressursse valitakse prioriteedi järgi.</span><span class="sxs-lookup"><span data-stu-id="a3e29-121">When you schedule jobs and operations, you can specify whether to select resources by priority.</span></span> <span data-ttu-id="a3e29-122">Kui otsustate selle valiku kasuks, kuid töö või operatsiooni saab soovitud kuupäevaks sooritatud rohkem kui üks ressurss, valitakse nõutava võimaluses suhtes madalaima prioriteediga ressurss.</span><span class="sxs-lookup"><span data-stu-id="a3e29-122">If you choose to do this, and more than one resource can perform the job or operation by the requested date, the resource that has the lowest priority with respect to the required capability is selected.</span></span>  
5. <span data-ttu-id="a3e29-123">Sisestage arv väljale Tase.</span><span class="sxs-lookup"><span data-stu-id="a3e29-123">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="a3e29-124">Kui määrate tööle või operatsioonile kindla nõutava võimaluse, saate määrata ka minimaalse nõutava taseme.</span><span class="sxs-lookup"><span data-stu-id="a3e29-124">When you specify that a job or operation requires a particular capability, you can also specify the minimum level that is required.</span></span> <span data-ttu-id="a3e29-125">Sama tööd erineval kiirusel, tugevusel, suurusel jms tegevate ressursside eristamiseks saate kasutada võimaluse taset.</span><span class="sxs-lookup"><span data-stu-id="a3e29-125">Use the capability level to differentiate resources that can perform the same job, but at different speeds, strengths, sizes, and so on.</span></span>  

