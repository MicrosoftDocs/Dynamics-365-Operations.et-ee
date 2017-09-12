--- 
title: " Kassa visuaalse profiili loomine "
description: See protseduur selgitab uue kassa visuaalse profiili loomist.
author: jashanno
manager: AnnBe
ms.date: 12/05/2015
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2b70bc95f56839da76612df2be3b35362925b977
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-pos-visual-profile"></a><span data-ttu-id="e5b09-103"> Kassa visuaalse profiili loomine </span><span class="sxs-lookup"><span data-stu-id="e5b09-103">Create a POS visual profile</span></span> 

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="e5b09-104">See protseduur selgitab uue kassa visuaalse profiili loomist.</span><span class="sxs-lookup"><span data-stu-id="e5b09-104">This procedure walks through creating a new point of sale (POS) visual profile.</span></span> <span data-ttu-id="e5b09-105">Visuaalne profiil sisaldab põhiteavet, mis määratleb kassaregistrite välimuse.</span><span class="sxs-lookup"><span data-stu-id="e5b09-105">A visual profile contains basic information that determines the appearance of POS registers.</span></span> <span data-ttu-id="e5b09-106">Saate luua mitu visuaalset profiili ja määrata kindlates registrites käitatavad konkreetsed profiilid.</span><span class="sxs-lookup"><span data-stu-id="e5b09-106">You can create several visual profiles and assign specific profiles to run on specific registers.</span></span> <span data-ttu-id="e5b09-107">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="e5b09-107">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="e5b09-108">Avage Jaemüük ja kaubandus > Kanali seadistus > Kassa seadistus > Kassaprofiilid > Visuaalsed profiilid.</span><span class="sxs-lookup"><span data-stu-id="e5b09-108">Go to Retail and commerce > Channel setup > POS setup > POS profiles > Visual profiles.</span></span>
2. <span data-ttu-id="e5b09-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e5b09-109">Click New.</span></span>
3. <span data-ttu-id="e5b09-110">Sisestage väärtus väljale Profiili number.</span><span class="sxs-lookup"><span data-stu-id="e5b09-110">In the Profile number field, type a value.</span></span>
4. <span data-ttu-id="e5b09-111">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="e5b09-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="e5b09-112">Klõpsake väljal Rakenduse tüüp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e5b09-112">In the Application type field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="e5b09-113">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e5b09-113">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="e5b09-114">Klõpsake väljal Kujundus otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e5b09-114">In the Theme field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="e5b09-115">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e5b09-115">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="e5b09-116">Otsingu avamiseks klõpsake väljal Rõhuvärv ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="e5b09-116">In the Accent colour field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="e5b09-117">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="e5b09-117">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="e5b09-118">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e5b09-118">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="e5b09-119">Laiendage jaotist Sisselogimise taust.</span><span class="sxs-lookup"><span data-stu-id="e5b09-119">Toggle the expansion of the Login background section.</span></span>
13. <span data-ttu-id="e5b09-120">Valige või sisestage pildi ID väljale Horisontaalpildi ID.</span><span class="sxs-lookup"><span data-stu-id="e5b09-120">In the Landscape image ID field, select or enter an image ID.</span></span>
14. <span data-ttu-id="e5b09-121">Valige või sisestage pildi ID väljale Vertikaalpildi ID.</span><span class="sxs-lookup"><span data-stu-id="e5b09-121">In the Portait image ID field, select or enter an image ID.</span></span>
15. <span data-ttu-id="e5b09-122">Laiendage jaotist Taust.</span><span class="sxs-lookup"><span data-stu-id="e5b09-122">Toggle the expansion of the Background section.</span></span>
16. <span data-ttu-id="e5b09-123">Tehke pildi ID toiming RequestPopup.</span><span class="sxs-lookup"><span data-stu-id="e5b09-123">RequestPopup the Image ID.</span></span>
17. <span data-ttu-id="e5b09-124">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="e5b09-124">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="e5b09-125">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e5b09-125">Click Save.</span></span>


