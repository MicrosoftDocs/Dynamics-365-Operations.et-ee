---
title: Toote jaoks partiiatribuutide loomine
description: See protseduur näitab, kuidas luua partii atribuuti, määrata vaikeväärtuse vahemikke ja kaasata atribuudi gruppi.
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 65153dbcfa69046e4f38eb6ffa013bb6fb87ebd8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "330651"
---
# <a name="create-batch-attributes-for-a-product"></a><span data-ttu-id="e1834-103">Toote jaoks partiiatribuutide loomine</span><span class="sxs-lookup"><span data-stu-id="e1834-103">Create batch attributes for a product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e1834-104">See protseduur näitab, kuidas luua partii atribuuti, määrata vaikeväärtuse vahemikke ja kaasata atribuudi gruppi.</span><span class="sxs-lookup"><span data-stu-id="e1834-104">This procedure shows how to create a batch attribute, assign default value ranges, and include the attribute in a group.</span></span> <span data-ttu-id="e1834-105">Selle protseduuri loomiseks kasutati demoettevõtte USP2 andmeid.</span><span class="sxs-lookup"><span data-stu-id="e1834-105">The demo data company used to create this procedure is the USP2 Company.</span></span>

1. <span data-ttu-id="e1834-106">Avage Varude haldus > Seadistus > Partii > Partii atribuudid.</span><span class="sxs-lookup"><span data-stu-id="e1834-106">Go to Inventory management > Setup > Batch > Batch attributes.</span></span>
2. <span data-ttu-id="e1834-107">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e1834-107">Click New.</span></span>
3. <span data-ttu-id="e1834-108">Sisestage väärtus väljale Atribuut.</span><span class="sxs-lookup"><span data-stu-id="e1834-108">In the Attribute field, type a value.</span></span>
4. <span data-ttu-id="e1834-109">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="e1834-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="e1834-110">Valige väljalt Atribuudi tüüp suvand Murd.</span><span class="sxs-lookup"><span data-stu-id="e1834-110">In the Attribute type field, select 'Fraction'.</span></span>
    * <span data-ttu-id="e1834-111">See protseduur kasutab kümnendarvude võimaldamiseks tüüpi Murd.</span><span class="sxs-lookup"><span data-stu-id="e1834-111">This procedure uses the Fraction type to enable decimal values.</span></span> <span data-ttu-id="e1834-112">Saate valida muid atribuudi tüüpe.</span><span class="sxs-lookup"><span data-stu-id="e1834-112">You can select other attribute types.</span></span> <span data-ttu-id="e1834-113">Tüübi Loetelu valimisel peate sisestama väärtused loetelu loendisse enne, kui saate väärtuse väljale Siht sisestada.</span><span class="sxs-lookup"><span data-stu-id="e1834-113">If you select the Enumeration type, you must enter values in the enumeration list before you can enter a value in the Target field.</span></span>  
6. <span data-ttu-id="e1834-114">Sisestage number väljale Miinimum.</span><span class="sxs-lookup"><span data-stu-id="e1834-114">In the Minimum field, enter a number.</span></span>
7. <span data-ttu-id="e1834-115">Sisestage number väljale Maksimum.</span><span class="sxs-lookup"><span data-stu-id="e1834-115">In the Maximum field, enter a number.</span></span>
8. <span data-ttu-id="e1834-116">Sisestage number väljale Juurdekasv.</span><span class="sxs-lookup"><span data-stu-id="e1834-116">In the Increment field, enter a number.</span></span>
9. <span data-ttu-id="e1834-117">Sisestage väärtus väljale Siht.</span><span class="sxs-lookup"><span data-stu-id="e1834-117">In the Target field, type a value.</span></span>
10. <span data-ttu-id="e1834-118">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e1834-118">Click Save.</span></span>
11. <span data-ttu-id="e1834-119">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e1834-119">Close the page.</span></span>
12. <span data-ttu-id="e1834-120">Avage Varude haldus > Seadistus > Partii > Partii atribuudigrupid.</span><span class="sxs-lookup"><span data-stu-id="e1834-120">Go to Inventory management > Setup > Batch > Batch attribute groups.</span></span>
13. <span data-ttu-id="e1834-121">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e1834-121">Click New.</span></span>
14. <span data-ttu-id="e1834-122">Sisestage väärtus väljale Atribuudigrupp.</span><span class="sxs-lookup"><span data-stu-id="e1834-122">In the Attribute group field, type a value.</span></span>
15. <span data-ttu-id="e1834-123">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="e1834-123">In the Description field, type a value.</span></span>
16. <span data-ttu-id="e1834-124">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e1834-124">Click Save.</span></span>
17. <span data-ttu-id="e1834-125">Klõpsake käsku Grupeeri atribuudid.</span><span class="sxs-lookup"><span data-stu-id="e1834-125">Click Group attributes.</span></span>
18. <span data-ttu-id="e1834-126">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e1834-126">Click New.</span></span>
19. <span data-ttu-id="e1834-127">Klõpsake väljal Atribuut otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e1834-127">In the Attribute field, click the drop-down button to open the lookup.</span></span>
20. <span data-ttu-id="e1834-128">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e1834-128">In the list, find and select the desired record.</span></span>
21. <span data-ttu-id="e1834-129">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e1834-129">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e1834-130">Atribuut võib olla kaasatud mis tahes gruppi.</span><span class="sxs-lookup"><span data-stu-id="e1834-130">An attribute can be included in any of the groups.</span></span>  
22. <span data-ttu-id="e1834-131">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e1834-131">Click Save.</span></span>
23. <span data-ttu-id="e1834-132">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e1834-132">Close the page.</span></span>

