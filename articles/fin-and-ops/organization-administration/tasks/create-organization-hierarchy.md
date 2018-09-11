--- 
title: Organisatsiooni hierarhia loomine
description: "Kasutage järgmist protseduuri, et luua organisatsiooni hierarhia."
author: sericks007
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: OMHierarchyManager, OMHierarchyPurposeAssociation, OMHierarchySelection, HierarchyDesigner
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 99819a2bff8d002721397c084babc07ebc070a37
ms.contentlocale: et-ee
ms.lasthandoff: 09/11/2018

---
# <a name="create-an-organization-hierarchy"></a><span data-ttu-id="6faff-103">Organisatsiooni hierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="6faff-103">Create an organization hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6faff-104">Kasutage järgmist protseduuri, et luua organisatsiooni hierarhia.</span><span class="sxs-lookup"><span data-stu-id="6faff-104">Use the following procedure to create an organizational hierarchy.</span></span> <span data-ttu-id="6faff-105">Saate kasutada organisatsiooni hierarhiaid oma äri vaatamiseks ja selle aruandluse tegemiseks erinevatest aspektidest.</span><span class="sxs-lookup"><span data-stu-id="6faff-105">You can use organizational hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="6faff-106">Näiteks saate seadistada ühe hierarhia maksu-, õigus- või seadusliku aruandluse jaoks.</span><span class="sxs-lookup"><span data-stu-id="6faff-106">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="6faff-107">Seejärel saate seadistada teise hierarhia finantsteabe aruandluseks, mis ei ole õiguslikult vajalik, kuid mida kasutatakse sisemises aruandluses.</span><span class="sxs-lookup"><span data-stu-id="6faff-107">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span> 



<span data-ttu-id="6faff-108">Enne organisatsiooni hierarhia loomist tuleb luua organisatsioonid.</span><span class="sxs-lookup"><span data-stu-id="6faff-108">Before you create an organizational hierarchy, you must create organizations.</span></span> <span data-ttu-id="6faff-109">Lisateabe saamiseks vaadake ülesandeid Juriidilise isiku loomine või Tootmisüksuse loomine.</span><span class="sxs-lookup"><span data-stu-id="6faff-109">For more information, see the “Create a legal entity” or “Create an operating unit” tasks.</span></span> <span data-ttu-id="6faff-110">Saate luua ka osakondi ja meeskondi.</span><span class="sxs-lookup"><span data-stu-id="6faff-110">You can also create departments and teams.</span></span> 



<span data-ttu-id="6faff-111">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="6faff-111">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-hierarchy"></a><span data-ttu-id="6faff-112">Hierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="6faff-112">Create a hierarchy</span></span>
1. <span data-ttu-id="6faff-113">Avage Organisatsiooni haldus > Organisatsioonid > Organisatsiooni hierarhiad.</span><span class="sxs-lookup"><span data-stu-id="6faff-113">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
2. <span data-ttu-id="6faff-114">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6faff-114">Click New.</span></span>
3. <span data-ttu-id="6faff-115">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="6faff-115">In the Name field, type a value.</span></span>
4. <span data-ttu-id="6faff-116">Klõpsake valikut Eesmärgi määramine.</span><span class="sxs-lookup"><span data-stu-id="6faff-116">Click Assign purpose.</span></span>
5. <span data-ttu-id="6faff-117">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="6faff-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6faff-118">Valige organisatsiooni hierarhiale määratav eesmärk.</span><span class="sxs-lookup"><span data-stu-id="6faff-118">Select a purpose to assign to your organization hierarchy.</span></span>  
6. <span data-ttu-id="6faff-119">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="6faff-119">Click Add.</span></span>
7. <span data-ttu-id="6faff-120">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="6faff-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="6faff-121">Otsige äsja loodud hierarhia üles.</span><span class="sxs-lookup"><span data-stu-id="6faff-121">Find the hierarchy you just created.</span></span>  
8. <span data-ttu-id="6faff-122">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="6faff-122">Click OK.</span></span>

## <a name="add-organizations-to-the-hierarchy"></a><span data-ttu-id="6faff-123">Organisatsioonide lisamine hierarhiasse</span><span class="sxs-lookup"><span data-stu-id="6faff-123">Add organizations to the hierarchy</span></span>
1. <span data-ttu-id="6faff-124">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="6faff-124">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="6faff-125">Valige hierarhia.</span><span class="sxs-lookup"><span data-stu-id="6faff-125">Select your hierarchy.</span></span>  
2. <span data-ttu-id="6faff-126">Klõpsake käsku Kuva hierarhia.</span><span class="sxs-lookup"><span data-stu-id="6faff-126">Click View hierarchy.</span></span>
    * <span data-ttu-id="6faff-127">Vajaduse korral lisage organisatsioone.</span><span class="sxs-lookup"><span data-stu-id="6faff-127">Add organizations, as necessary.</span></span>  
    * <span data-ttu-id="6faff-128">Organisatsiooni lisamiseks klõpsake nuppu Redigeeri ja seejärel organisatsiooni lisamiseks nuppu Sisesta.</span><span class="sxs-lookup"><span data-stu-id="6faff-128">To add an organization, click Edit and then Insert to add the organization.</span></span>     <span data-ttu-id="6faff-129">Kui olete muudatuste tegemise lõpetanud, saate salvestada mustandi ja/või muudatused avaldada.</span><span class="sxs-lookup"><span data-stu-id="6faff-129">When you are done making changes you can save a draft and/or publish the changes.</span></span>  


