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
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 01b797aa97e73cbe112c37a1efcd1e759730bc24
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149109"
---
# <a name="define-discrete-manufacturing-resource-group"></a><span data-ttu-id="24f4f-103">Diskreetse tootmise ressursigrupi määratlemine</span><span class="sxs-lookup"><span data-stu-id="24f4f-103">Define discrete manufacturing resource group</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="24f4f-104">Ressursigrupp on operatsiooniressursside kogum, mis tavaliselt vastab tootmistöödes kollaste joontega määratletud töörakkude füüsilisele organiseerimisele.</span><span class="sxs-lookup"><span data-stu-id="24f4f-104">A resource group is a set of operations resources that typically correspond to the physical organization of work cells, defined by yellow lines on the production shop floor.</span></span> <span data-ttu-id="24f4f-105">Selles protseduuris näitlikustatakse, kuidas määratleda diskreetses tootmises kasutatavat ressursigruppi.</span><span class="sxs-lookup"><span data-stu-id="24f4f-105">This procedure shows you how to define a ressource group for use in discrete production.</span></span> <span data-ttu-id="24f4f-106">Saate selle toiminguga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="24f4f-106">You can walk through this procedure in demo data company USMF, or use your own data.</span></span>

1. <span data-ttu-id="24f4f-107">Avage Ressursigrupid.</span><span class="sxs-lookup"><span data-stu-id="24f4f-107">Go to Resource groups.</span></span>
2. <span data-ttu-id="24f4f-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="24f4f-108">Click New.</span></span>
3. <span data-ttu-id="24f4f-109">Sisestage väärtus väljale Ressursigrupp.</span><span class="sxs-lookup"><span data-stu-id="24f4f-109">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="24f4f-110">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="24f4f-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="24f4f-111">Sisestage või valige väärtus väljal Koht.</span><span class="sxs-lookup"><span data-stu-id="24f4f-111">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="24f4f-112">Sisestage või valige väärtus väljal Tootmisüksus.</span><span class="sxs-lookup"><span data-stu-id="24f4f-112">In the Production unit field, enter or select a value.</span></span>

## <a name="define-default-operational-parameters"></a><span data-ttu-id="24f4f-113">Toimingu vaikeparameetrite määratlemine</span><span class="sxs-lookup"><span data-stu-id="24f4f-113">Define default operational parameters</span></span>
1. <span data-ttu-id="24f4f-114">Laiendage jaotist Toiming.</span><span class="sxs-lookup"><span data-stu-id="24f4f-114">Expand the Operation section.</span></span>
2. <span data-ttu-id="24f4f-115">Sisestage arv väljale Praagi protsent.</span><span class="sxs-lookup"><span data-stu-id="24f4f-115">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="24f4f-116">Sisestage või valige väärtus väljal Seadistuse kategooria.</span><span class="sxs-lookup"><span data-stu-id="24f4f-116">In the Setup category field, enter or select a value.</span></span>
4. <span data-ttu-id="24f4f-117">Sisestage või valige väärtus väljal Käitusaja kategooria.</span><span class="sxs-lookup"><span data-stu-id="24f4f-117">In the Run time category field, enter or select a value.</span></span>
5. <span data-ttu-id="24f4f-118">Sisestage arv väljale Operatsioonide planeerimise protsent.</span><span class="sxs-lookup"><span data-stu-id="24f4f-118">In the Operations scheduling percentage field, enter a number.</span></span>

## <a name="define-operating-hours"></a><span data-ttu-id="24f4f-119">Tööaja määratlemine</span><span class="sxs-lookup"><span data-stu-id="24f4f-119">Define operating hours</span></span>
1. <span data-ttu-id="24f4f-120">Laiendage jaotist Kalendrid.</span><span class="sxs-lookup"><span data-stu-id="24f4f-120">Expand the Calendars section.</span></span>
2. <span data-ttu-id="24f4f-121">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="24f4f-121">Click Add.</span></span>
3. <span data-ttu-id="24f4f-122">Sisestage või valige väärtus väljal Kalender.</span><span class="sxs-lookup"><span data-stu-id="24f4f-122">In the Calendar field, enter or select a value.</span></span>

## <a name="add-operations-resources"></a><span data-ttu-id="24f4f-123">Operatsiooniressursside lisamine</span><span class="sxs-lookup"><span data-stu-id="24f4f-123">Add operations resources</span></span>
1. <span data-ttu-id="24f4f-124">Laiendage jaotist Ressursid.</span><span class="sxs-lookup"><span data-stu-id="24f4f-124">Expand the Resources section.</span></span>
2. <span data-ttu-id="24f4f-125">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="24f4f-125">Click Add.</span></span>
3. <span data-ttu-id="24f4f-126">Sisestage või valige väärtus väljal Ressurss.</span><span class="sxs-lookup"><span data-stu-id="24f4f-126">In the Resource field, enter or select a value.</span></span>
4. <span data-ttu-id="24f4f-127">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="24f4f-127">Click Add.</span></span>
5. <span data-ttu-id="24f4f-128">Sisestage või valige väärtus väljal Ressurss.</span><span class="sxs-lookup"><span data-stu-id="24f4f-128">In the Resource field, enter or select a value.</span></span>
6. <span data-ttu-id="24f4f-129">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="24f4f-129">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="24f4f-130">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="24f4f-130">In the list, click the link in the selected row.</span></span>

