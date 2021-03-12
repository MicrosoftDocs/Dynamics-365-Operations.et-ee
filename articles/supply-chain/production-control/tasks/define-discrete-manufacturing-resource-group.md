---
title: Diskreetse tootmise ressursigrupi määratlemine
description: Ressursigrupp on operatsiooniressursside kogum, mis tavaliselt vastab tootmistöödes kollaste joontega määratletud töörakkude füüsilisele organiseerimisele.
author: sorenva
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WrkCtrResourceGroup
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1930999604fb2605a88bad9a5972afd3579976a
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4975106"
---
# <a name="define-discrete-manufacturing-resource-group"></a><span data-ttu-id="248a1-103">Diskreetse tootmise ressursigrupi määratlemine</span><span class="sxs-lookup"><span data-stu-id="248a1-103">Define discrete manufacturing resource group</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="248a1-104">Ressursigrupp on operatsiooniressursside kogum, mis tavaliselt vastab tootmistöödes kollaste joontega määratletud töörakkude füüsilisele organiseerimisele.</span><span class="sxs-lookup"><span data-stu-id="248a1-104">A resource group is a set of operations resources that typically correspond to the physical organization of work cells, defined by yellow lines on the production shop floor.</span></span> <span data-ttu-id="248a1-105">Selles protseduuris näitlikustatakse, kuidas määratleda diskreetses tootmises kasutatavat ressursigruppi.</span><span class="sxs-lookup"><span data-stu-id="248a1-105">This procedure shows you how to define a ressource group for use in discrete production.</span></span> <span data-ttu-id="248a1-106">Saate selle toiminguga tutvuda demoettevõtte USMF-i või omaenda andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="248a1-106">You can walk through this procedure in demo data company USMF, or use your own data.</span></span>

1. <span data-ttu-id="248a1-107">Avage Ressursigrupid.</span><span class="sxs-lookup"><span data-stu-id="248a1-107">Go to Resource groups.</span></span>
2. <span data-ttu-id="248a1-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="248a1-108">Click New.</span></span>
3. <span data-ttu-id="248a1-109">Sisestage väärtus väljale Ressursigrupp.</span><span class="sxs-lookup"><span data-stu-id="248a1-109">In the Resource group field, type a value.</span></span>
4. <span data-ttu-id="248a1-110">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="248a1-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="248a1-111">Sisestage või valige väärtus väljal Koht.</span><span class="sxs-lookup"><span data-stu-id="248a1-111">In the Site field, enter or select a value.</span></span>
6. <span data-ttu-id="248a1-112">Sisestage või valige väärtus väljal Tootmisüksus.</span><span class="sxs-lookup"><span data-stu-id="248a1-112">In the Production unit field, enter or select a value.</span></span>

## <a name="define-default-operational-parameters"></a><span data-ttu-id="248a1-113">Toimingu vaikeparameetrite määratlemine</span><span class="sxs-lookup"><span data-stu-id="248a1-113">Define default operational parameters</span></span>
1. <span data-ttu-id="248a1-114">Laiendage jaotist Toiming.</span><span class="sxs-lookup"><span data-stu-id="248a1-114">Expand the Operation section.</span></span>
2. <span data-ttu-id="248a1-115">Sisestage arv väljale Praagi protsent.</span><span class="sxs-lookup"><span data-stu-id="248a1-115">In the Scrap percentage field, enter a number.</span></span>
3. <span data-ttu-id="248a1-116">Sisestage või valige väärtus väljal Seadistuse kategooria.</span><span class="sxs-lookup"><span data-stu-id="248a1-116">In the Setup category field, enter or select a value.</span></span>
4. <span data-ttu-id="248a1-117">Sisestage või valige väärtus väljal Käitusaja kategooria.</span><span class="sxs-lookup"><span data-stu-id="248a1-117">In the Run time category field, enter or select a value.</span></span>
5. <span data-ttu-id="248a1-118">Sisestage arv väljale Operatsioonide planeerimise protsent.</span><span class="sxs-lookup"><span data-stu-id="248a1-118">In the Operations scheduling percentage field, enter a number.</span></span>

## <a name="define-operating-hours"></a><span data-ttu-id="248a1-119">Tööaja määratlemine</span><span class="sxs-lookup"><span data-stu-id="248a1-119">Define operating hours</span></span>
1. <span data-ttu-id="248a1-120">Laiendage jaotist Kalendrid.</span><span class="sxs-lookup"><span data-stu-id="248a1-120">Expand the Calendars section.</span></span>
2. <span data-ttu-id="248a1-121">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="248a1-121">Click Add.</span></span>
3. <span data-ttu-id="248a1-122">Sisestage või valige väärtus väljal Kalender.</span><span class="sxs-lookup"><span data-stu-id="248a1-122">In the Calendar field, enter or select a value.</span></span>

## <a name="add-operations-resources"></a><span data-ttu-id="248a1-123">Operatsiooniressursside lisamine</span><span class="sxs-lookup"><span data-stu-id="248a1-123">Add operations resources</span></span>
1. <span data-ttu-id="248a1-124">Laiendage jaotist Ressursid.</span><span class="sxs-lookup"><span data-stu-id="248a1-124">Expand the Resources section.</span></span>
2. <span data-ttu-id="248a1-125">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="248a1-125">Click Add.</span></span>
3. <span data-ttu-id="248a1-126">Sisestage või valige väärtus väljal Ressurss.</span><span class="sxs-lookup"><span data-stu-id="248a1-126">In the Resource field, enter or select a value.</span></span>
4. <span data-ttu-id="248a1-127">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="248a1-127">Click Add.</span></span>
5. <span data-ttu-id="248a1-128">Sisestage või valige väärtus väljal Ressurss.</span><span class="sxs-lookup"><span data-stu-id="248a1-128">In the Resource field, enter or select a value.</span></span>
6. <span data-ttu-id="248a1-129">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="248a1-129">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="248a1-130">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="248a1-130">In the list, click the link in the selected row.</span></span>

