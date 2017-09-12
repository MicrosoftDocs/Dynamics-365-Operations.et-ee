--- 
title: "Pakkumiskutsete jaoks kutsetüüpide ja hindamiskriteeriumide loomine"
description: "See juhend näitab, kuidas kutse tüüpi luua ja seda hindamismeetodiga seostada."
author: mkirknel
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 095855d552d228375635bdbaa9fca37c47a3b952
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="create-solicitation-types-and-scoring-criteria-for-rfqs"></a><span data-ttu-id="6c0bc-103">Pakkumiskutsete jaoks kutsetüüpide ja hindamiskriteeriumide loomine</span><span class="sxs-lookup"><span data-stu-id="6c0bc-103">Create solicitation types and scoring criteria for RFQs</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6c0bc-104">See juhend näitab, kuidas kutse tüüpi luua ja seda hindamismeetodiga seostada.</span><span class="sxs-lookup"><span data-stu-id="6c0bc-104">This guide shows you how to create a solicitation type and associate this with a scoring method.</span></span> <span data-ttu-id="6c0bc-105">Samuti näitav see, kuidas kasutada kutse tüüpi pakkumiskutsel, mis siis vaike-hindamismeetodi määrab.</span><span class="sxs-lookup"><span data-stu-id="6c0bc-105">It also shows how to use the solicitation type on a request for quotation (RFQ) which then sets the default scoring method.</span></span> <span data-ttu-id="6c0bc-106">Neid ülesandeid täidab üldjuhul ostujuht.</span><span class="sxs-lookup"><span data-stu-id="6c0bc-106">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="6c0bc-107">Saate selle protseduuriga tutvuda demoettevõtte USMF või oma andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="6c0bc-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="6c0bc-108">Enne alustamist peab teil olema hindamismeetod kättesaadav.</span><span class="sxs-lookup"><span data-stu-id="6c0bc-108">You need to have a scoring method available before you start.</span></span>


## <a name="create-a-solicitation-type"></a><span data-ttu-id="6c0bc-109">Kutsetüübi loomine</span><span class="sxs-lookup"><span data-stu-id="6c0bc-109">Create a solicitation type</span></span>
1. <span data-ttu-id="6c0bc-110">Valige Hanked > Seadistus > Pakkumiskutse > Kutse tüüp.</span><span class="sxs-lookup"><span data-stu-id="6c0bc-110">Go to Procurement and sourcing > Setup > Request for quotation > Solicitation type.</span></span>
2. <span data-ttu-id="6c0bc-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6c0bc-111">Click New.</span></span>
3. <span data-ttu-id="6c0bc-112">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="6c0bc-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="6c0bc-113">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="6c0bc-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="6c0bc-114">Valige väljalt Hindamismeetod hindamismeetod, mida soovite selle kutse tüübi puhul kasutada.</span><span class="sxs-lookup"><span data-stu-id="6c0bc-114">In the Scoring method field, select the scoring method that you want to use for this solicitation type.</span></span>
6. <span data-ttu-id="6c0bc-115">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="6c0bc-115">Click Save.</span></span>
7. <span data-ttu-id="6c0bc-116">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6c0bc-116">Close the page.</span></span>

## <a name="use-the-solicitation-type"></a><span data-ttu-id="6c0bc-117">Kutse tüübi kasutamine</span><span class="sxs-lookup"><span data-stu-id="6c0bc-117">Use the solicitation type</span></span>
1. <span data-ttu-id="6c0bc-118">Avage Hanked > Pakkumiskutsed > Kõik pakkumiskutsed.</span><span class="sxs-lookup"><span data-stu-id="6c0bc-118">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="6c0bc-119">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="6c0bc-119">Click New.</span></span>
3. <span data-ttu-id="6c0bc-120">Valige väljalt Kutse tüüp äsja loodud kutse tüüp.</span><span class="sxs-lookup"><span data-stu-id="6c0bc-120">In the Solicitation type field, select the solicitation type that you have just created.</span></span> 
4. <span data-ttu-id="6c0bc-121">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="6c0bc-121">Click OK.</span></span>
5. <span data-ttu-id="6c0bc-122">Klõpsake valikut Hindamiskriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="6c0bc-122">Click Scoring criteria.</span></span>
    * <span data-ttu-id="6c0bc-123">Kuvatud hindamiskriteeriumid on kutse tüübiga seotud hindamismeetodi omad.</span><span class="sxs-lookup"><span data-stu-id="6c0bc-123">The scoring criteria that are shown are the ones from the scoring method that you associated with the solicitation type.</span></span> <span data-ttu-id="6c0bc-124">Saate sellele lehele kriteeriume lisada või kustutada.</span><span class="sxs-lookup"><span data-stu-id="6c0bc-124">You can choose to add or delete criteria on this page.</span></span> <span data-ttu-id="6c0bc-125">Võimalik on ka uute kriteeriumide lisamine, kopeerides need muudest hindamismeetoditest.</span><span class="sxs-lookup"><span data-stu-id="6c0bc-125">It's also possible to add new criteria by copying them from other scoring methods.</span></span>  
6. <span data-ttu-id="6c0bc-126">Klõpsake valikut Kopeeri kriteerium.</span><span class="sxs-lookup"><span data-stu-id="6c0bc-126">Click Copy criteria.</span></span>
7. <span data-ttu-id="6c0bc-127">Valige või sisestage väärtus väljal Hindamismeetod.</span><span class="sxs-lookup"><span data-stu-id="6c0bc-127">In the Scoring method field, enter or select a value.</span></span>
8. <span data-ttu-id="6c0bc-128">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="6c0bc-128">Click OK.</span></span>
9. <span data-ttu-id="6c0bc-129">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="6c0bc-129">Close the page.</span></span>


