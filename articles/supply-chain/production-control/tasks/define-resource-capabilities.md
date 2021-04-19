---
title: Ressursivõimaluste määratlemine
description: Ressursi võimalused kirjeldavad, milliseid operatsioone ressursid teha saavad.
author: sorenva
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: WrkCtrCapability
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 072991e7b3844ad3583b7d0c575d426299f74e9f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828702"
---
# <a name="define-resource-capabilities"></a><span data-ttu-id="f490e-103">Ressursivõimaluste määratlemine</span><span class="sxs-lookup"><span data-stu-id="f490e-103">Define resource capabilities</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f490e-104">Ressursi võimalused kirjeldavad, milliseid operatsioone ressursid teha saavad.</span><span class="sxs-lookup"><span data-stu-id="f490e-104">Resource capabilities describe what operations resources can do.</span></span> <span data-ttu-id="f490e-105">Planeerimisel vastendatakse iga töö ja operatsiooni nõuded saadaolevate ressursside võimalustega.</span><span class="sxs-lookup"><span data-stu-id="f490e-105">During scheduling, the requirements of each job and operation are matched against the capabilities of the available resources.</span></span> <span data-ttu-id="f490e-106">Selles tegevuse juhises aidatakse teil ressursi võimalust luua ja seda ressursile määrata.</span><span class="sxs-lookup"><span data-stu-id="f490e-106">This task guide will help you create a resource capability and assign it to a resource.</span></span> <span data-ttu-id="f490e-107">Selle tegevuse loomisel kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="f490e-107">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-resource-capability"></a><span data-ttu-id="f490e-108">Ressursi võimaluse loomine</span><span class="sxs-lookup"><span data-stu-id="f490e-108">Create a resource capability</span></span>
1. <span data-ttu-id="f490e-109">Avage Ressursi võimalused.</span><span class="sxs-lookup"><span data-stu-id="f490e-109">Go to Resource capabilities.</span></span>
2. <span data-ttu-id="f490e-110">Klõpsake Uus.</span><span class="sxs-lookup"><span data-stu-id="f490e-110">Click New.</span></span>
3. <span data-ttu-id="f490e-111">Sisestage ressursi võimaluse ID väljale Võimalus.</span><span class="sxs-lookup"><span data-stu-id="f490e-111">In the Capability field, type the ID of the resource capability.</span></span>
    * <span data-ttu-id="f490e-112">Selle operatsiooni puhul kasutage võimaluse ID-d, et määrata võimalus, mis ressurssidel selle operatsiooni teostamiseks peab olema.</span><span class="sxs-lookup"><span data-stu-id="f490e-112">For a given operation, you use the capability ID to specify that resources must have this capability to perform the operation.</span></span>  
4. <span data-ttu-id="f490e-113">Sisestage võimaluse kirjeldus väljale Kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="f490e-113">In the Description field, enter a description of the capability.</span></span>

## <a name="assign-capability-to-a-resource"></a><span data-ttu-id="f490e-114">Ressursile võimaluse määramine</span><span class="sxs-lookup"><span data-stu-id="f490e-114">Assign capability to a resource</span></span>
1. <span data-ttu-id="f490e-115">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="f490e-115">Click Add.</span></span>
2. <span data-ttu-id="f490e-116">Sisestage ressursi ID väljale Ressurss.</span><span class="sxs-lookup"><span data-stu-id="f490e-116">In the Resource field, type the ID of the resource.</span></span>
    * <span data-ttu-id="f490e-117">Ressursi võimaluse saab määrata ühele või mitmele ressursile.</span><span class="sxs-lookup"><span data-stu-id="f490e-117">A resource capability can be assigned to one or more resources.</span></span>  
3. <span data-ttu-id="f490e-118">Sisestage kuupäev väljale Aegumine.</span><span class="sxs-lookup"><span data-stu-id="f490e-118">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="f490e-119">Saate seda välja kasutades ressursile ainult piiratud ajaks võimaluse määrata.</span><span class="sxs-lookup"><span data-stu-id="f490e-119">You can use this field to specify that a resource has the capability for only a limited time.</span></span>  
4. <span data-ttu-id="f490e-120">Sisestage arv väljale Prioriteet.</span><span class="sxs-lookup"><span data-stu-id="f490e-120">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="f490e-121">Tööde ja operatsioonide planeerimisel saate määrata, kas ressursse valitakse prioriteedi järgi.</span><span class="sxs-lookup"><span data-stu-id="f490e-121">When you schedule jobs and operations, you can specify whether to select resources by priority.</span></span> <span data-ttu-id="f490e-122">Kui otsustate selle valiku kasuks, kuid töö või operatsiooni saab soovitud kuupäevaks sooritatud rohkem kui üks ressurss, valitakse nõutava võimaluses suhtes madalaima prioriteediga ressurss.</span><span class="sxs-lookup"><span data-stu-id="f490e-122">If you choose to do this, and more than one resource can perform the job or operation by the requested date, the resource that has the lowest priority with respect to the required capability is selected.</span></span>  
5. <span data-ttu-id="f490e-123">Sisestage arv väljale Tase.</span><span class="sxs-lookup"><span data-stu-id="f490e-123">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="f490e-124">Kui määrate tööle või operatsioonile kindla nõutava võimaluse, saate määrata ka minimaalse nõutava taseme.</span><span class="sxs-lookup"><span data-stu-id="f490e-124">When you specify that a job or operation requires a particular capability, you can also specify the minimum level that is required.</span></span> <span data-ttu-id="f490e-125">Sama tööd erineval kiirusel, tugevusel, suurusel jms tegevate ressursside eristamiseks saate kasutada võimaluse taset.</span><span class="sxs-lookup"><span data-stu-id="f490e-125">Use the capability level to differentiate resources that can perform the same job, but at different speeds, strengths, sizes, and so on.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]