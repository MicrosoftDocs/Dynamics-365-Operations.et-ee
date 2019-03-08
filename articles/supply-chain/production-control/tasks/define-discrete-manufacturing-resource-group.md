---
title: Diskreetse tootmise ressursigrupi määratlemine
description: Ressursigrupp on operatsiooniressursside kogum, mis tavaliselt vastab tootmistöödes kollaste joontega määratletud töörakkude füüsilisele organiseerimisele.
author: sorenva
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 50733e34bbf14ae2cade6822105da4d8c2120d7d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "353237"
---
# <a name="define-discrete-manufacturing-resource-group"></a><span data-ttu-id="6ed72-103">Diskreetse tootmise ressursigrupi määratlemine</span><span class="sxs-lookup"><span data-stu-id="6ed72-103">Define discrete manufacturing resource group</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6ed72-104">Ressursigrupp on operatsiooniressursside kogum, mis tavaliselt vastab tootmistöödes kollaste joontega määratletud töörakkude füüsilisele organiseerimisele.</span><span class="sxs-lookup"><span data-stu-id="6ed72-104">A resource group is a set of operations resources that typically correspond to the physical organization of work cells, defined by yellow lines on the production shop floor.</span></span> <span data-ttu-id="6ed72-105">Selles protseduuris näitlikustatakse, kuidas määratleda diskreetses tootmises kasutatavat ressursigruppi.</span><span class="sxs-lookup"><span data-stu-id="6ed72-105">This procedure shows you how to define a ressource group for use in discrete production.</span></span> <span data-ttu-id="6ed72-106">Saate selle toiminguga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="6ed72-106">You can walk through this procedure in demo data company USMF, or use your own data.</span></span>

1. <span data-ttu-id="6ed72-107">Avage Ressursigrupid.</span><span class="sxs-lookup"><span data-stu-id="6ed72-107">Go to Resource groups.</span></span>
2. <span data-ttu-id="6ed72-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6ed72-108">Click New.</span></span>
3. <span data-ttu-id="6ed72-109">Sisestage väärtus väljale Ressursigrupp.</span><span class="sxs-lookup"><span data-stu-id="6ed72-109">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="6ed72-110">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="6ed72-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6ed72-111">Sisestage või valige väärtus väljal Koht.</span><span class="sxs-lookup"><span data-stu-id="6ed72-111">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="6ed72-112">Sisestage või valige väärtus väljal Tootmisüksus.</span><span class="sxs-lookup"><span data-stu-id="6ed72-112">In the Production unit field, enter or select a value.</span></span>

## <a name="define-default-operational-parameters"></a><span data-ttu-id="6ed72-113">Toimingu vaikeparameetrite määratlemine</span><span class="sxs-lookup"><span data-stu-id="6ed72-113">Define default operational parameters</span></span>
1. <span data-ttu-id="6ed72-114">Laiendage jaotist Toiming.</span><span class="sxs-lookup"><span data-stu-id="6ed72-114">Expand the Operation section.</span></span>
2. <span data-ttu-id="6ed72-115">Sisestage arv väljale Praagi protsent.</span><span class="sxs-lookup"><span data-stu-id="6ed72-115">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="6ed72-116">Sisestage või valige väärtus väljal Seadistuse kategooria.</span><span class="sxs-lookup"><span data-stu-id="6ed72-116">In the Setup category field, enter or select a value.</span></span>
4. <span data-ttu-id="6ed72-117">Sisestage või valige väärtus väljal Käitusaja kategooria.</span><span class="sxs-lookup"><span data-stu-id="6ed72-117">In the Run time category field, enter or select a value.</span></span>
5. <span data-ttu-id="6ed72-118">Sisestage arv väljale Operatsioonide planeerimise protsent.</span><span class="sxs-lookup"><span data-stu-id="6ed72-118">In the Operations scheduling percentage field, enter a number.</span></span>

## <a name="define-operating-hours"></a><span data-ttu-id="6ed72-119">Tööaja määratlemine</span><span class="sxs-lookup"><span data-stu-id="6ed72-119">Define operating hours</span></span>
1. <span data-ttu-id="6ed72-120">Laiendage jaotist Kalendrid.</span><span class="sxs-lookup"><span data-stu-id="6ed72-120">Expand the Calendars section.</span></span>
2. <span data-ttu-id="6ed72-121">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="6ed72-121">Click Add.</span></span>
3. <span data-ttu-id="6ed72-122">Sisestage või valige väärtus väljal Kalender.</span><span class="sxs-lookup"><span data-stu-id="6ed72-122">In the Calendar field, enter or select a value.</span></span>

## <a name="add-operations-resources"></a><span data-ttu-id="6ed72-123">Operatsiooniressursside lisamine</span><span class="sxs-lookup"><span data-stu-id="6ed72-123">Add operations resources</span></span>
1. <span data-ttu-id="6ed72-124">Laiendage jaotist Ressursid.</span><span class="sxs-lookup"><span data-stu-id="6ed72-124">Expand the Resources section.</span></span>
2. <span data-ttu-id="6ed72-125">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="6ed72-125">Click Add.</span></span>
3. <span data-ttu-id="6ed72-126">Sisestage või valige väärtus väljal Ressurss.</span><span class="sxs-lookup"><span data-stu-id="6ed72-126">In the Resource field, enter or select a value.</span></span>
4. <span data-ttu-id="6ed72-127">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="6ed72-127">Click Add.</span></span>
5. <span data-ttu-id="6ed72-128">Sisestage või valige väärtus väljal Ressurss.</span><span class="sxs-lookup"><span data-stu-id="6ed72-128">In the Resource field, enter or select a value.</span></span>
6. <span data-ttu-id="6ed72-129">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="6ed72-129">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="6ed72-130">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="6ed72-130">In the list, click the link in the selected row.</span></span>

