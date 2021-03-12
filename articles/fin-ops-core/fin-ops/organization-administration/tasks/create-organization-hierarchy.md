---
title: Organisatsiooni hierarhia loomine
description: Kasutage järgmist protseduuri, et luua organisatsiooni hierarhia.
author: sericks007
manager: AnnBe
ms.date: 12/15/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMHierarchyManager, OMHierarchyPurposeAssociation, OMHierarchySelection, HierarchyDesigner
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8627c1aa0ce9ec011b568224040b1143f0f54c31
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/19/2020
ms.locfileid: "4796918"
---
# <a name="create-an-organization-hierarchy"></a><span data-ttu-id="b904b-103">Organisatsiooni hierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="b904b-103">Create an organization hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b904b-104">Kasutage järgmist protseduuri, et luua organisatsiooni hierarhia.</span><span class="sxs-lookup"><span data-stu-id="b904b-104">Use the following procedure to create an organizational hierarchy.</span></span> <span data-ttu-id="b904b-105">Saate kasutada organisatsiooni hierarhiaid oma äri vaatamiseks ja selle aruandluse tegemiseks erinevatest aspektidest.</span><span class="sxs-lookup"><span data-stu-id="b904b-105">You can use organizational hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="b904b-106">Näiteks saate seadistada ühe hierarhia maksu-, õigus- või seadusliku aruandluse jaoks.</span><span class="sxs-lookup"><span data-stu-id="b904b-106">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="b904b-107">Seejärel saate seadistada teise hierarhia finantsteabe aruandluseks, mis ei ole õiguslikult vajalik, kuid mida kasutatakse sisemises aruandluses.</span><span class="sxs-lookup"><span data-stu-id="b904b-107">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span> 

<span data-ttu-id="b904b-108">Enne organisatsiooni hierarhia loomist tuleb luua organisatsioonid.</span><span class="sxs-lookup"><span data-stu-id="b904b-108">Before you create an organizational hierarchy, you must create organizations.</span></span> <span data-ttu-id="b904b-109">Lisateabe saamiseks vaadake ülesandeid „Juriidilise isiku loomine” või „Tootmisüksuse loomine”.</span><span class="sxs-lookup"><span data-stu-id="b904b-109">For more information, see the "Create a legal entity" or "Create an operating unit" tasks.</span></span> <span data-ttu-id="b904b-110">Saate luua ka osakondi ja meeskondi.</span><span class="sxs-lookup"><span data-stu-id="b904b-110">You can also create departments and teams.</span></span> 

<span data-ttu-id="b904b-111">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="b904b-111">The demo data company used to create this procedure is USMF.</span></span>

## <a name="create-a-hierarchy"></a><span data-ttu-id="b904b-112">Hierarhia loomine</span><span class="sxs-lookup"><span data-stu-id="b904b-112">Create a hierarchy</span></span>
1. <span data-ttu-id="b904b-113">Avage **Navigeerimispaan > Moodulid > Organisatsiooni haldus > Organisatsioonid > Organisatsiooni hierarhiad**.</span><span class="sxs-lookup"><span data-stu-id="b904b-113">Go to **Navigation pane > Modules > Organization administration > Organizations > Organization hierarchies**.</span></span>
2. <span data-ttu-id="b904b-114">Paanil **Toimingupaan** klõpsake valikut **Uus**.</span><span class="sxs-lookup"><span data-stu-id="b904b-114">On the **Action pane**, click **New**.</span></span>
3. <span data-ttu-id="b904b-115">Sisestage väärtus väljale **Nimi**.</span><span class="sxs-lookup"><span data-stu-id="b904b-115">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="b904b-116">Jaotises **Eesmärk** klõpsake **Määra eesmärk**.</span><span class="sxs-lookup"><span data-stu-id="b904b-116">In the **Purpose** section, click **Assign purpose**.</span></span>
5. <span data-ttu-id="b904b-117">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="b904b-117">In the list, find and select the desired record.</span></span> <span data-ttu-id="b904b-118">Valige organisatsiooni hierarhiale määratav eesmärk.</span><span class="sxs-lookup"><span data-stu-id="b904b-118">Select a purpose to assign to your organization hierarchy.</span></span>  
6. <span data-ttu-id="b904b-119">Jaotises **Määratud hierarhiad** klõpsake suvandit **Lisa**.</span><span class="sxs-lookup"><span data-stu-id="b904b-119">In the **Assigned hierarchies** section, click **Add**.</span></span>
7. <span data-ttu-id="b904b-120">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="b904b-120">In the list, mark the selected row.</span></span> <span data-ttu-id="b904b-121">Otsige äsja loodud hierarhia üles.</span><span class="sxs-lookup"><span data-stu-id="b904b-121">Find the hierarchy you just created.</span></span>  
8. <span data-ttu-id="b904b-122">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="b904b-122">Click **OK**.</span></span>

## <a name="add-organizations-to-the-hierarchy"></a><span data-ttu-id="b904b-123">Organisatsioonide lisamine hierarhiasse</span><span class="sxs-lookup"><span data-stu-id="b904b-123">Add organizations to the hierarchy</span></span>
1. <span data-ttu-id="b904b-124">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="b904b-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="b904b-125">Valige hierarhia.</span><span class="sxs-lookup"><span data-stu-id="b904b-125">Select your hierarchy.</span></span>  
2. <span data-ttu-id="b904b-126">Jaotises **Määratud hierarhiad** klõpsake **Kuva hierarhia**.</span><span class="sxs-lookup"><span data-stu-id="b904b-126">In the **Assigned hierarchies** section, click **View hierarchy**.</span></span>
    - <span data-ttu-id="b904b-127">Vajaduse korral lisage organisatsioone.</span><span class="sxs-lookup"><span data-stu-id="b904b-127">Add organizations, as necessary.</span></span>  
    - <span data-ttu-id="b904b-128">Organisatsiooni lisamiseks klõpsake **Redigeeri** ja seejärel **Sisesta**, et lisada organisatsioon.</span><span class="sxs-lookup"><span data-stu-id="b904b-128">To add an organization, click **Edit** and then **Insert** to add the organization.</span></span> <span data-ttu-id="b904b-129">Kui olete muudatuste tegemise lõpetanud, saate mustandi **salvestada** ja/või muudatused **avaldada**.</span><span class="sxs-lookup"><span data-stu-id="b904b-129">When you are done making changes you can **Save** a draft and/or **Publish** the changes.</span></span>  

