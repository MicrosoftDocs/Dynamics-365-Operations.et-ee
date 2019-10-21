---
title: Organisatsiooni hierarhia loomine
description: Kasutage järgmist protseduuri, et luua organisatsiooni hierarhia.
author: sericks007
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMHierarchyManager, OMHierarchyPurposeAssociation, OMHierarchySelection, HierarchyDesigner
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 48c8564694b22a5110341d853a79096fbe805c91
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177433"
---
# <a name="create-an-organization-hierarchy"></a><span data-ttu-id="f3ff1-103">Organisatsiooni hierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="f3ff1-103">Create an organization hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f3ff1-104">Kasutage järgmist protseduuri, et luua organisatsiooni hierarhia.</span><span class="sxs-lookup"><span data-stu-id="f3ff1-104">Use the following procedure to create an organizational hierarchy.</span></span> <span data-ttu-id="f3ff1-105">Saate kasutada organisatsiooni hierarhiaid oma äri vaatamiseks ja selle aruandluse tegemiseks erinevatest aspektidest.</span><span class="sxs-lookup"><span data-stu-id="f3ff1-105">You can use organizational hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="f3ff1-106">Näiteks saate seadistada ühe hierarhia maksu-, õigus- või seadusliku aruandluse jaoks.</span><span class="sxs-lookup"><span data-stu-id="f3ff1-106">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="f3ff1-107">Seejärel saate seadistada teise hierarhia finantsteabe aruandluseks, mis ei ole õiguslikult vajalik, kuid mida kasutatakse sisemises aruandluses.</span><span class="sxs-lookup"><span data-stu-id="f3ff1-107">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span> 

<span data-ttu-id="f3ff1-108">Enne organisatsiooni hierarhia loomist tuleb luua organisatsioonid.</span><span class="sxs-lookup"><span data-stu-id="f3ff1-108">Before you create an organizational hierarchy, you must create organizations.</span></span> <span data-ttu-id="f3ff1-109">Lisateabe saamiseks vaadake ülesandeid Juriidilise isiku loomine või Tootmisüksuse loomine.</span><span class="sxs-lookup"><span data-stu-id="f3ff1-109">For more information, see the “Create a legal entity” or “Create an operating unit” tasks.</span></span> <span data-ttu-id="f3ff1-110">Saate luua ka osakondi ja meeskondi.</span><span class="sxs-lookup"><span data-stu-id="f3ff1-110">You can also create departments and teams.</span></span> 

<span data-ttu-id="f3ff1-111">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="f3ff1-111">The demo data company used to create this procedure is USMF.</span></span>

## <a name="create-a-hierarchy"></a><span data-ttu-id="f3ff1-112">Hierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="f3ff1-112">Create a hierarchy</span></span>
1. <span data-ttu-id="f3ff1-113">Avage **Navigeerimispaan > Moodulid > Organisatsiooni haldus > Organisatsioonid > Organisatsiooni hierarhiad**.</span><span class="sxs-lookup"><span data-stu-id="f3ff1-113">Go to **Navigation pane > Modules > Organization administration > Organizations > Organization hierarchies**.</span></span>
2. <span data-ttu-id="f3ff1-114">Paanil **Toimingupaan** klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="f3ff1-114">On the **Action pane**, click **New**.</span></span>
3. <span data-ttu-id="f3ff1-115">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="f3ff1-115">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="f3ff1-116">Jaotises **Eesmärk** klõpsake **Määra eesmärk**.</span><span class="sxs-lookup"><span data-stu-id="f3ff1-116">In the **Purpose** section, click **Assign purpose**.</span></span>
5. <span data-ttu-id="f3ff1-117">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="f3ff1-117">In the list, find and select the desired record.</span></span> <span data-ttu-id="f3ff1-118">Valige organisatsiooni hierarhiale määratav eesmärk.</span><span class="sxs-lookup"><span data-stu-id="f3ff1-118">Select a purpose to assign to your organization hierarchy.</span></span>  
6. <span data-ttu-id="f3ff1-119">Jaotises **Määratud hierarhiad** klõpsake **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="f3ff1-119">In the **Assigned hierarchies** sectiom, click **Add**.</span></span>
7. <span data-ttu-id="f3ff1-120">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="f3ff1-120">In the list, mark the selected row.</span></span> <span data-ttu-id="f3ff1-121">Otsige äsja loodud hierarhia üles.</span><span class="sxs-lookup"><span data-stu-id="f3ff1-121">Find the hierarchy you just created.</span></span>  
8. <span data-ttu-id="f3ff1-122">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="f3ff1-122">Click **OK**.</span></span>

## <a name="add-organizations-to-the-hierarchy"></a><span data-ttu-id="f3ff1-123">Organisatsioonide lisamine hierarhiasse</span><span class="sxs-lookup"><span data-stu-id="f3ff1-123">Add organizations to the hierarchy</span></span>
1. <span data-ttu-id="f3ff1-124">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="f3ff1-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="f3ff1-125">Valige hierarhia.</span><span class="sxs-lookup"><span data-stu-id="f3ff1-125">Select your hierarchy.</span></span>  
2. <span data-ttu-id="f3ff1-126">Jaotises **Määratud hierarhiad** klõpsake **Kuva hierarhia**.</span><span class="sxs-lookup"><span data-stu-id="f3ff1-126">In the **Assigned hierarchies** section, click **View hierarchy**.</span></span>
    - <span data-ttu-id="f3ff1-127">Vajaduse korral lisage organisatsioone.</span><span class="sxs-lookup"><span data-stu-id="f3ff1-127">Add organizations, as necessary.</span></span>  
    - <span data-ttu-id="f3ff1-128">Organisatsiooni lisamiseks klõpsake **Redigeeri** ja seejärel **Sisesta**, et lisada organisatsioon.</span><span class="sxs-lookup"><span data-stu-id="f3ff1-128">To add an organization, click **Edit** and then **Insert** to add the organization.</span></span> <span data-ttu-id="f3ff1-129">Kui olete muudatuste tegemise lõpetanud, saate mustandi **salvestada** ja/või muudatused **avaldada**.</span><span class="sxs-lookup"><span data-stu-id="f3ff1-129">When you are done making changes you can **Save** a draft and/or **Publish** the changes.</span></span>  

