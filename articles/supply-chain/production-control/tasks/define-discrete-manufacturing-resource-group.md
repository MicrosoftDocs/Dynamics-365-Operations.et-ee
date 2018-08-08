--- 
title: "Diskreetse tootmise ressursigrupi määratlemine"
description: "Ressursigrupp on operatsiooniressursside kogum, mis tavaliselt vastab tootmistöödes kollaste joontega määratletud töörakkude füüsilisele organiseerimisele."
author: sorenva
manager: AnnBe
ms.date: 11/03/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: e1be950a7d1d7548aced041a189222b472d767cf
ms.contentlocale: et-ee
ms.lasthandoff: 08/07/2018

---
# <a name="define-discrete-manufacturing-resource-group"></a><span data-ttu-id="ebc8f-103">Diskreetse tootmise ressursigrupi määratlemine</span><span class="sxs-lookup"><span data-stu-id="ebc8f-103">Define discrete manufacturing resource group</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ebc8f-104">Ressursigrupp on operatsiooniressursside kogum, mis tavaliselt vastab tootmistöödes kollaste joontega määratletud töörakkude füüsilisele organiseerimisele.</span><span class="sxs-lookup"><span data-stu-id="ebc8f-104">A resource group is a set of operations resources that typically correspond to the physical organization of work cells, defined by yellow lines on the production shop floor.</span></span> <span data-ttu-id="ebc8f-105">Selles protseduuris näitlikustatakse, kuidas määratleda diskreetses tootmises kasutatavat ressursigruppi.</span><span class="sxs-lookup"><span data-stu-id="ebc8f-105">This procedure shows you how to define a resource group for use in discrete production.</span></span> <span data-ttu-id="ebc8f-106">Saate selle toiminguga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="ebc8f-106">You can walk through this procedure in demo data company USMF, or use your own data.</span></span>

1. <span data-ttu-id="ebc8f-107">Avage Ressursigrupid.</span><span class="sxs-lookup"><span data-stu-id="ebc8f-107">Go to Resource groups.</span></span>
2. <span data-ttu-id="ebc8f-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ebc8f-108">Click New.</span></span>
3. <span data-ttu-id="ebc8f-109">Sisestage väärtus väljale Ressursigrupp.</span><span class="sxs-lookup"><span data-stu-id="ebc8f-109">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="ebc8f-110">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="ebc8f-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ebc8f-111">Sisestage või valige väärtus väljal Koht.</span><span class="sxs-lookup"><span data-stu-id="ebc8f-111">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="ebc8f-112">Sisestage või valige väärtus väljal Tootmisüksus.</span><span class="sxs-lookup"><span data-stu-id="ebc8f-112">In the Production unit field, enter or select a value.</span></span>

## <a name="define-default-operational-parameters"></a><span data-ttu-id="ebc8f-113">Toimingu vaikeparameetrite määratlemine</span><span class="sxs-lookup"><span data-stu-id="ebc8f-113">Define default operational parameters</span></span>
1. <span data-ttu-id="ebc8f-114">Laiendage jaotist Toiming.</span><span class="sxs-lookup"><span data-stu-id="ebc8f-114">Expand the Operation section.</span></span>
2. <span data-ttu-id="ebc8f-115">Sisestage arv väljale Praagi protsent.</span><span class="sxs-lookup"><span data-stu-id="ebc8f-115">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="ebc8f-116">Sisestage või valige väärtus väljal Seadistuse kategooria.</span><span class="sxs-lookup"><span data-stu-id="ebc8f-116">In the Setup category field, enter or select a value.</span></span>
4. <span data-ttu-id="ebc8f-117">Sisestage või valige väärtus väljal Käitusaja kategooria.</span><span class="sxs-lookup"><span data-stu-id="ebc8f-117">In the Run time category field, enter or select a value.</span></span>
5. <span data-ttu-id="ebc8f-118">Sisestage arv väljale Operatsioonide planeerimise protsent.</span><span class="sxs-lookup"><span data-stu-id="ebc8f-118">In the Operations scheduling percentage field, enter a number.</span></span>

## <a name="define-operating-hours"></a><span data-ttu-id="ebc8f-119">Tööaja määratlemine</span><span class="sxs-lookup"><span data-stu-id="ebc8f-119">Define operating hours</span></span>
1. <span data-ttu-id="ebc8f-120">Laiendage jaotist Kalendrid.</span><span class="sxs-lookup"><span data-stu-id="ebc8f-120">Expand the Calendars section.</span></span>
2. <span data-ttu-id="ebc8f-121">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="ebc8f-121">Click Add.</span></span>
3. <span data-ttu-id="ebc8f-122">Sisestage või valige väärtus väljal Kalender.</span><span class="sxs-lookup"><span data-stu-id="ebc8f-122">In the Calendar field, enter or select a value.</span></span>

## <a name="add-operations-resources"></a><span data-ttu-id="ebc8f-123">Operatsiooniressursside lisamine</span><span class="sxs-lookup"><span data-stu-id="ebc8f-123">Add operations resources</span></span>
1. <span data-ttu-id="ebc8f-124">Laiendage jaotist Ressursid.</span><span class="sxs-lookup"><span data-stu-id="ebc8f-124">Expand the Resources section.</span></span>
2. <span data-ttu-id="ebc8f-125">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="ebc8f-125">Click Add.</span></span>
3. <span data-ttu-id="ebc8f-126">Sisestage või valige väärtus väljal Ressurss.</span><span class="sxs-lookup"><span data-stu-id="ebc8f-126">In the Resource field, enter or select a value.</span></span>
4. <span data-ttu-id="ebc8f-127">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="ebc8f-127">Click Add.</span></span>
5. <span data-ttu-id="ebc8f-128">Sisestage või valige väärtus väljal Ressurss.</span><span class="sxs-lookup"><span data-stu-id="ebc8f-128">In the Resource field, enter or select a value.</span></span>
6. <span data-ttu-id="ebc8f-129">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="ebc8f-129">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="ebc8f-130">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="ebc8f-130">In the list, click the link in the selected row.</span></span>


