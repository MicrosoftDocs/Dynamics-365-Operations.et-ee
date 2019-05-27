---
title: Tootele vöötkoodi loomine
description: See protseduur selgitab, kuidas luua käsitsi vöötkoodi, kasutades näitena kaubakoodi M0001.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductMaintainWorkspace, EcoResProductOpenCasesFormPart, EcoResProductDetailsExtended, InventItemBarcode, InventItemBarcodeLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2ae2765a125045d60566267d01e380069d5d527c
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568600"
---
# <a name="create-a-bar-code-for-a-product"></a><span data-ttu-id="039b7-103">Tootele vöötkoodi loomine</span><span class="sxs-lookup"><span data-stu-id="039b7-103">Create a bar code for a product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="039b7-104">See protseduur selgitab, kuidas luua käsitsi vöötkoodi, kasutades näitena kaubakoodi M0001.</span><span class="sxs-lookup"><span data-stu-id="039b7-104">This procedure shows how to manually create a bar code using the item number M0001 as an example.</span></span> <span data-ttu-id="039b7-105">Selle protseduuri loomiseks kasutati demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="039b7-105">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="039b7-106">Klõpsake valikut Väljastatud toodete hooldus.</span><span class="sxs-lookup"><span data-stu-id="039b7-106">Click Released product maintenance.</span></span>
2. <span data-ttu-id="039b7-107">Klõpsake valikut Väljastatud tooted.</span><span class="sxs-lookup"><span data-stu-id="039b7-107">Click Released products.</span></span>
3. <span data-ttu-id="039b7-108">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="039b7-108">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="039b7-109">Klõpsake toimingupaanil suvandit Halda varusid.</span><span class="sxs-lookup"><span data-stu-id="039b7-109">On the Action Pane, click Manage inventory.</span></span>
5. <span data-ttu-id="039b7-110">Klõpsake valikut Vöötkoodid.</span><span class="sxs-lookup"><span data-stu-id="039b7-110">Click Bar codes.</span></span>
6. <span data-ttu-id="039b7-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="039b7-111">Click New.</span></span>
7. <span data-ttu-id="039b7-112">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="039b7-112">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="039b7-113">Valige või sisestage väärtus väljal Vöötkoodi häälestus.</span><span class="sxs-lookup"><span data-stu-id="039b7-113">In the Barcode setup field, enter or select a value.</span></span>
9. <span data-ttu-id="039b7-114">Sisestage või valige väärtus väljal Vöötkood.</span><span class="sxs-lookup"><span data-stu-id="039b7-114">In the Bar code field, enter or select a value.</span></span>
10. <span data-ttu-id="039b7-115">Tippige väärtus väljale Vöötkood.</span><span class="sxs-lookup"><span data-stu-id="039b7-115">In the Bar code field, type a value.</span></span>
    * <span data-ttu-id="039b7-116">Vajutage tabeldusklahvi.</span><span class="sxs-lookup"><span data-stu-id="039b7-116">Press the Tab key.</span></span>  
11. <span data-ttu-id="039b7-117">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="039b7-117">Close the page.</span></span>
12. <span data-ttu-id="039b7-118">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="039b7-118">In the Quantity field, enter a number.</span></span>
13. <span data-ttu-id="039b7-119">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="039b7-119">Click Save.</span></span>
    * <span data-ttu-id="039b7-120">Kui klõpsate käsku Salvesta, kontrollitakse vöötkoodi ja praegusel juhul kuvatakse tõrge, mis ütleb, et oodati kontrollnumbrit 8, aga leiti 3.</span><span class="sxs-lookup"><span data-stu-id="039b7-120">When you click Save, the barcode check is run, and in this case it will display an error stating that the expected check digit is 8, but that 3 was found.</span></span> <span data-ttu-id="039b7-121">Muutke vöötkoodi numbrit käsitsi, nii et lõpus oleks 8.</span><span class="sxs-lookup"><span data-stu-id="039b7-121">Manually update the barcode number so that 8 is at the end.</span></span>  
14. <span data-ttu-id="039b7-122">Sisestage või valige väärtus väljal Vöötkood.</span><span class="sxs-lookup"><span data-stu-id="039b7-122">In the Bar code field, enter or select a value.</span></span>
15. <span data-ttu-id="039b7-123">Tippige väärtus väljale Vöötkood.</span><span class="sxs-lookup"><span data-stu-id="039b7-123">In the Bar code field, type a value.</span></span>
    * <span data-ttu-id="039b7-124">Vajutage tabeldusklahvi.</span><span class="sxs-lookup"><span data-stu-id="039b7-124">Press the Tab key.</span></span>  
16. <span data-ttu-id="039b7-125">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="039b7-125">Close the page.</span></span>
17. <span data-ttu-id="039b7-126">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="039b7-126">Click Save.</span></span>
18. <span data-ttu-id="039b7-127">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="039b7-127">Close the page.</span></span>

