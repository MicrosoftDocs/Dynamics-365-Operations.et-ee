--- 
title: "Põhivara käibelt kõrvaldamine vabas vormis arve abil"
description: "See protseduur näitab, kuidas soetada põhivara, kasutades põhivara töölehe soetussoovitust."
author: saraschi2
manager: AnnBe
ms.date: 10/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 715b7057b48b14145f49d5f83e7d0008ce9146ca
ms.contentlocale: et-ee
ms.lasthandoff: 08/07/2018

---
# <a name="dispose-of-a-fixed-asset-using-a-free-text-invoice"></a><span data-ttu-id="25f9e-103">Põhivara käibelt kõrvaldamine vabas vormis arve abil</span><span class="sxs-lookup"><span data-stu-id="25f9e-103">Dispose of a fixed asset using a free text invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="25f9e-104">See protseduur näitab, kuidas soetada põhivara, kasutades põhivara töölehe soetussoovitust.</span><span class="sxs-lookup"><span data-stu-id="25f9e-104">This procedure shows how to acquire a fixed asset using the acquisition proposal in the Fixed assets journal.</span></span> <span data-ttu-id="25f9e-105">See kasutab USMF-i juriidilise isiku puhul raamatupidaja rolli ja demoandmeid.</span><span class="sxs-lookup"><span data-stu-id="25f9e-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="25f9e-106">Avage Põhivarad > Töölehe sisestused > Põhivarade tööleht.</span><span class="sxs-lookup"><span data-stu-id="25f9e-106">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>
2. <span data-ttu-id="25f9e-107">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="25f9e-107">Click New.</span></span>
3. <span data-ttu-id="25f9e-108">Sisestage või valige väärtus väljal Nimi.</span><span class="sxs-lookup"><span data-stu-id="25f9e-108">In the Name field, enter or select a value.</span></span>
4. <span data-ttu-id="25f9e-109">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="25f9e-109">Click Lines.</span></span>
5. <span data-ttu-id="25f9e-110">Klõpsake suvandit Soovitused.</span><span class="sxs-lookup"><span data-stu-id="25f9e-110">Click Proposals.</span></span>
6. <span data-ttu-id="25f9e-111">Klõpsake suvandit Soetussoovitus.</span><span class="sxs-lookup"><span data-stu-id="25f9e-111">Click Acquisition proposal.</span></span>
7. <span data-ttu-id="25f9e-112">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="25f9e-112">Click Filter.</span></span>
8. <span data-ttu-id="25f9e-113">Eelmiste väärtuste eemaldamiseks klõpsake nuppu Lähtesta.</span><span class="sxs-lookup"><span data-stu-id="25f9e-113">Click Reset to clear out previous values.</span></span>
9. <span data-ttu-id="25f9e-114">Valige rida Põhivara kood.</span><span class="sxs-lookup"><span data-stu-id="25f9e-114">Select the Fixed asset number row.</span></span>
10. <span data-ttu-id="25f9e-115">Sisestage või valige väärtus väljal Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="25f9e-115">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="25f9e-116">Seadistage ülejäänud kriteeriumid põhivarade puhul, mida soovite selle soovitusega soetada.</span><span class="sxs-lookup"><span data-stu-id="25f9e-116">Set the remaining criteria for the fixed assets that you want to acquire with this proposal.</span></span>  
11. <span data-ttu-id="25f9e-117">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="25f9e-117">Click OK.</span></span>
12. <span data-ttu-id="25f9e-118">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="25f9e-118">Click OK.</span></span>
    * <span data-ttu-id="25f9e-119">Kontrollige loodud kande ridu.</span><span class="sxs-lookup"><span data-stu-id="25f9e-119">Verify the transaction lines created.</span></span>  
    * <span data-ttu-id="25f9e-120">Soetussoovitusse kaasatakse ainult põhivarad, mille soetamiskuupäev ja soetusmaksumus on raamatus seadistatud.</span><span class="sxs-lookup"><span data-stu-id="25f9e-120">Only fixed assets with the acquisition date and acquisition price set on the book will be included in the acquisition proposal.</span></span>  
13. <span data-ttu-id="25f9e-121">Klõpsake vahekaarti Raamatud.</span><span class="sxs-lookup"><span data-stu-id="25f9e-121">Click the Books tab.</span></span>
14. <span data-ttu-id="25f9e-122">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="25f9e-122">Click Post.</span></span>


