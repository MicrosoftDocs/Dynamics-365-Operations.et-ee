--- 
title: "Lao tööpoliitikate seadistamine "
description: "Laotoimingud ei hõlma alati laotööd."
author: johanhoffmann
manager: AnnBe
ms.date: 06/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 22e359ee2ded2315c588c2dd5c3d62dee0440adf
ms.contentlocale: et-ee
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-warehouse-work-policies"></a><span data-ttu-id="0ce54-103">Lao tööpoliitikate seadistamine </span><span class="sxs-lookup"><span data-stu-id="0ce54-103">Set up warehouse work policies</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0ce54-104">Laotoimingud ei hõlma alati laotööd.</span><span class="sxs-lookup"><span data-stu-id="0ce54-104">Warehouse processes don’t always include warehouse work.</span></span> <span data-ttu-id="0ce54-105">Tööpoliitika määratlemisel saate vältida töö loomist toormaterjali komplekteerimise puhul ja lõpetatud kaupade ladustamist toodete kogumi puhul kindlates asukohtades.</span><span class="sxs-lookup"><span data-stu-id="0ce54-105">By defining a work policy, you can prevent the creation of work for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span> <span data-ttu-id="0ce54-106">Selle kirje loomisel kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="0ce54-106">The USMF demo data company was used to create this recording.</span></span> <span data-ttu-id="0ce54-107">Selle ülesande juhendi jaoks on nõutav rakenduse Dynamics AX-i versioon 7.0.1 või uuem versioon.</span><span class="sxs-lookup"><span data-stu-id="0ce54-107">This task guide requires Dynamics AX application 7.0.1 or later.</span></span>

1. <span data-ttu-id="0ce54-108">Avage Laohaldus > Seadistus > Töö > Tööpoliitikad.</span><span class="sxs-lookup"><span data-stu-id="0ce54-108">Go to Warehouse management > Setup > Work > Work policies.</span></span>
2. <span data-ttu-id="0ce54-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0ce54-109">Click New.</span></span>
3. <span data-ttu-id="0ce54-110">Tippige välja Tööpoliitika nimi väärtus Ladustamitööd ei ole.</span><span class="sxs-lookup"><span data-stu-id="0ce54-110">In the Work policy name field, type 'No put-away work'.</span></span>
4. <span data-ttu-id="0ce54-111">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="0ce54-111">Click Save.</span></span>
5. <span data-ttu-id="0ce54-112">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="0ce54-112">Click Add.</span></span>
6. <span data-ttu-id="0ce54-113">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="0ce54-113">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="0ce54-114">Tehke väljal Töötellimuse tüüp valik Lõpetatud kaupade kõrvalepanek.</span><span class="sxs-lookup"><span data-stu-id="0ce54-114">In the Work order type field, select 'Finished goods put away'.</span></span>
8. <span data-ttu-id="0ce54-115">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="0ce54-115">Click Add.</span></span>
9. <span data-ttu-id="0ce54-116">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="0ce54-116">In the list, mark the selected row.</span></span>
10. <span data-ttu-id="0ce54-117">Tehke välja Töötellimuse tüüp valik Kaastoodete ja kõrvalsaaduste kõrvalepanek.</span><span class="sxs-lookup"><span data-stu-id="0ce54-117">In the Work order type field, select 'Co-product and by-product put away'.</span></span>
11. <span data-ttu-id="0ce54-118">Laiendage jaotist Lao asukohad.</span><span class="sxs-lookup"><span data-stu-id="0ce54-118">Expand the Inventory locations section.</span></span>
12. <span data-ttu-id="0ce54-119">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="0ce54-119">Click Add.</span></span>
13. <span data-ttu-id="0ce54-120">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="0ce54-120">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="0ce54-121">Sisestage loendisse Ladu väärtus 51.</span><span class="sxs-lookup"><span data-stu-id="0ce54-121">In the Warehouse list, enter '51'.</span></span>
15. <span data-ttu-id="0ce54-122">Sisestage või valige väljal Asukoht väärtus 001.</span><span class="sxs-lookup"><span data-stu-id="0ce54-122">In the Location field, enter or select '001'.</span></span>
16. <span data-ttu-id="0ce54-123">Laiendage jaotist Tooted.</span><span class="sxs-lookup"><span data-stu-id="0ce54-123">Expand the Products section.</span></span>
17. <span data-ttu-id="0ce54-124">Tehk väljal Toote valimine valik Valitud.</span><span class="sxs-lookup"><span data-stu-id="0ce54-124">In the Product selection field, select 'Selected'.</span></span>
18. <span data-ttu-id="0ce54-125">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="0ce54-125">Click Add.</span></span>
19. <span data-ttu-id="0ce54-126">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="0ce54-126">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="0ce54-127">Sisestage või valige väljal Kaubakood väärtus L0101.</span><span class="sxs-lookup"><span data-stu-id="0ce54-127">In the Item number field, enter or select 'L0101'.</span></span>
21. <span data-ttu-id="0ce54-128">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="0ce54-128">Click Save.</span></span>


