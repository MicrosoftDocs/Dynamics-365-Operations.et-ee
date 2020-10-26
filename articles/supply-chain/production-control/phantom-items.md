---
title: Fiktiivsed kaubad
description: Selles teemas kirjeldatakse üksikasjalikult, kuidas saab fiktiivset reatüüpi kasutada koosluse- ja valemiridade puhul rakenduses Dynamics 365 Supply Chain Management.
author: ShylaThompson
manager: tfehr
ms.date: 06/15/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysOperationTemplateForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 1705903
ms.search.region: Global
ms.author: kamaybac
ms.search.validfrom: ''
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: b14bebadd7088c9bbcfb6b1c5df1fe1a3c98694d
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/10/2020
ms.locfileid: "3980738"
---
# <a name="phantom-items"></a><span data-ttu-id="ba99d-103">Fiktiivsed kaubad</span><span class="sxs-lookup"><span data-stu-id="ba99d-103">Phantom items</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ba99d-104">Selles teemas kirjeldatakse üksikasjalikult, kuidas saab fiktiivset reatüüpi kasutada koosluse- (BOM) ja valemiridade puhul.</span><span class="sxs-lookup"><span data-stu-id="ba99d-104">This topic describes, in detail, how the Phantom line type can be used for the lines of a bill of materials (BOM) and a formula.</span></span> <span data-ttu-id="ba99d-105">Järgmisel joonisel tähistab (a) toote H ning osade F ja G kooslust ning (b) toodete H ja osa F protsessilehte.</span><span class="sxs-lookup"><span data-stu-id="ba99d-105">In the following illustration, (a) is the BOM for product H and parts F and G, and (b) is the route sheet for products H and part F.</span></span>

![Toode H ja osa F](media/product-H-part-F.png)


<span data-ttu-id="ba99d-107">Sellel joonisel on toodud näide koosluse struktuurist kahel tasemel.</span><span class="sxs-lookup"><span data-stu-id="ba99d-107">This illustration shows an example of a BOM structure in two levels.</span></span> <span data-ttu-id="ba99d-108">Lõpetatud toode H tähistab masinakoostu toodet.</span><span class="sxs-lookup"><span data-stu-id="ba99d-108">Finished product H represents a product for a machine assembly.</span></span> <span data-ttu-id="ba99d-109">Masinakoost koosneb kahest osast: elektriseadmest (F), millel on kaks materjali (A ja B), ning pakkematerjalide rühmast, millel on samuti kaks materjali (C ja D).</span><span class="sxs-lookup"><span data-stu-id="ba99d-109">The machine assembly consists of two parts, an electrical unit (F) that has two materials (A and B) and a group of packaging materials (G) that also has two materials (C and D).</span></span> <span data-ttu-id="ba99d-110">Veel üht materjali (E) kasutatakse masina üldise kokkupaneku ajal.</span><span class="sxs-lookup"><span data-stu-id="ba99d-110">Another material (E) is used during the general assembly of the machine.</span></span>

![Toode H ja osa F](media/product-H-part-B.png)

<span data-ttu-id="ba99d-112">Eeltoodud joonis kujutab toote H tehnilist joonist. See struktuur annab hea ülevaate masina üldkoostu osadest ja komponentidest.</span><span class="sxs-lookup"><span data-stu-id="ba99d-112">The preceding illustration represents the Engineering BOM for product H. This structure provides a good overview of the parts and components of the overall machine assembly.</span></span> <span data-ttu-id="ba99d-113">Ehkki tootekujundajad eelistaksid koosluse kujutamist sellisel viisil, ei pruugi see struktuur õigesti esitada viisi, kuidas masinat töökohas koostatakse.</span><span class="sxs-lookup"><span data-stu-id="ba99d-113">However, although product designers might prefer to see the BOM represented in this way, this structure might not correctly represent the way that the machine is built on the shop floor.</span></span> 

<span data-ttu-id="ba99d-114">Näiteks tehniline kooslus eeltoodud joonisel näitab, et elektriseade F pannakse kokku eraldi osana eraldi töökäsul.</span><span class="sxs-lookup"><span data-stu-id="ba99d-114">For example, the Engineering BOM in the preceding illustration indicates that electrical unit F is assembled as a separate part on a separate work order.</span></span> <span data-ttu-id="ba99d-115">Siiski võidakse töökojas hinnata optimaalsemaks panna elektriseade kokku masina üldkoostu osana, mitte eraldi töökäsuna.</span><span class="sxs-lookup"><span data-stu-id="ba99d-115">However, on the shop floor, it might be judged more optimal to assemble the electrical unit as part of the overall machine assembly, not as a separate work order.</span></span>

<span data-ttu-id="ba99d-116">See tehniline kooslus näitab ka, et osa G on eraldi osa.</span><span class="sxs-lookup"><span data-stu-id="ba99d-116">This Engineering BOM also indicates that part G is a separate part.</span></span> <span data-ttu-id="ba99d-117">Selles struktuuris ei tähista aga G füüsilist osa, vaid pakkematerjalide kogumit.</span><span class="sxs-lookup"><span data-stu-id="ba99d-117">However, in this structure, part G doesn’t represent a physical part but a collection of packaging materials.</span></span> 

<span data-ttu-id="ba99d-118">Seetõttu, kuigi tehniline kooslus annab toote kujundusele ja selle haldusele olulise väärtuse, ei pruugi see olla kõige loogilisem viis toote tootmise käivitamisprotsessi toetamiseks.</span><span class="sxs-lookup"><span data-stu-id="ba99d-118">Therefore, although an Engineering BOM provides great value for the design of a product and maintenance of that design, it might not be the most logical way to support the manufacturing execution process of the product.</span></span> <span data-ttu-id="ba99d-119">Seevastu kujutab tootmise kooslus parimat viisi toote koostamiseks.</span><span class="sxs-lookup"><span data-stu-id="ba99d-119">By contrast, a Manufacturing BOM represents the best way to build a product.</span></span>

<span data-ttu-id="ba99d-120">Järgmisel joonisel on näidatud, kuidas eelnev tehniline kooslus viiakse üle tootmise koosluseks.</span><span class="sxs-lookup"><span data-stu-id="ba99d-120">The following illustration shows how the preceding Engineering BOM is transitioned into a Manufacturing BOM.</span></span> <span data-ttu-id="ba99d-121">Sellel joonisel tähistab (a) toote H kooslust ja (b) toote H protsessilehte.</span><span class="sxs-lookup"><span data-stu-id="ba99d-121">In this illustration, (a) is the BOM for product H, and b is the route sheet for product H.</span></span>

<span data-ttu-id="ba99d-122">Sellises struktuuris näete, et osasid F ja G ei ole näidatud ning materjalid, millest need osad koosnevad, on tõstetud järgmisele kooslusetasandile.</span><span class="sxs-lookup"><span data-stu-id="ba99d-122">In this structure, you can see that there is no notion of parts F and G, and the materials that these parts consist of have been elevated to the next BOM level.</span></span> 

<span data-ttu-id="ba99d-123">Vastupidiselt tehnilisele kooslusele, millel oli kaks toimingulehte, on tootmise kooslusel ainult üks toiminguleht.</span><span class="sxs-lookup"><span data-stu-id="ba99d-123">Unlike the Engineering BOM, which had two operations sheets, the Manufacturing BOM has only one operations sheet.</span></span> <span data-ttu-id="ba99d-124">Osaga G seotud pakkimistoiming on samuti tõstetud ja on nüüd osa toote H toimingulehest. Elektriseadme kokkupanek on esimene toiming.</span><span class="sxs-lookup"><span data-stu-id="ba99d-124">The packaging operation that was linked to part G has also been elevated and is now part of the operations sheet for product H. The assembly of the electrical unit is the first operation.</span></span> <span data-ttu-id="ba99d-125">See järjekord on mõistlik, kuna seda seadet kasutatakse järgmises toimingus, milleks on masina kokkupanek.</span><span class="sxs-lookup"><span data-stu-id="ba99d-125">This order makes good sense, because this unit is used in the next operation, which is the machine assembly.</span></span> <span data-ttu-id="ba99d-126">Viimane toiming on pakkimistoiming, mis tarbib kaht pakkematerjali (C ja D).</span><span class="sxs-lookup"><span data-stu-id="ba99d-126">The last operation is the packaging operation, which consumes two packing materials (C and D).</span></span>

<span data-ttu-id="ba99d-127">Üleminek tehnilise koosluse ja tootmise koosluse vahel on lubatud fiktiivse koosluse reatüübi kaudu.</span><span class="sxs-lookup"><span data-stu-id="ba99d-127">The transition between the Engineering BOM and the Manufacturing BOM is enabled through the Phantom BOM line type.</span></span> <span data-ttu-id="ba99d-128">Mõiste „fiktiivne” näitab, et F ja G on kahe koosluse tüübi vahelisel üleminekul kadunud.</span><span class="sxs-lookup"><span data-stu-id="ba99d-128">As the term “phantom” indicates, parts F and G have disappeared during the transition between the two BOM types.</span></span> <span data-ttu-id="ba99d-129">Selles näites on fiktiivne reatüüp rakendatud tehnilises koosluses osade F ja G koosluseridadele.</span><span class="sxs-lookup"><span data-stu-id="ba99d-129">In this example, the Phantom line type is applied to the BOM lines for parts F and G in the Engineering BOM.</span></span> <span data-ttu-id="ba99d-130">Tootmis- või partiitellimuse loomisel kopeeritakse tehniline kooslus tootmis- või partiitellimusele.</span><span class="sxs-lookup"><span data-stu-id="ba99d-130">When a production or batch order is created, the Engineering BOM is copied to the production or batch order.</span></span> <span data-ttu-id="ba99d-131">Kui tellimus on hinnatud, toimub üleminek tehniliselt koosluselt tootmise kooslusele, nagu on näidatud eeltoodud joonistel.</span><span class="sxs-lookup"><span data-stu-id="ba99d-131">Then, when the order is estimated, the transition from the Engineering BOM to the Manufacturing BOM occurs, as shown in the preceding illustrations.</span></span> <span data-ttu-id="ba99d-132">Teisel joonisel näidatud toimingulehelt sisestatakse toimingu jaoks pakkematerjalid C ja D.</span><span class="sxs-lookup"><span data-stu-id="ba99d-132">From the operations sheet in the second illustration, packaging materials C and D are input for the operation.</span></span> 

## <a name="multilevel-phantom-bom-structures"></a><span data-ttu-id="ba99d-133">Mitmetasandilised fiktiivse koosluse struktuurid</span><span class="sxs-lookup"><span data-stu-id="ba99d-133">Multilevel phantom BOM structures</span></span>
<span data-ttu-id="ba99d-134">Fiktiivset reatüüpi saab kasutada mitmetasandilistes kooslusestruktuurides, nagu on näidatud järgmisel joonisel.</span><span class="sxs-lookup"><span data-stu-id="ba99d-134">The Phantom line type can be used in multilevel BOM structures, as shown in the following illustration.</span></span> <span data-ttu-id="ba99d-135">Sellel joonisel tähistab (a) toote G kooslust ning (b) osade E ja F ning toote G protsessilehte.</span><span class="sxs-lookup"><span data-stu-id="ba99d-135">In this illustration, (a) is the BOM for product G, and (b) is the route sheet for parts E and F and product G.</span></span> 

![Toode G ja osa F koos protsessilehtedega](media/product-G-route-sheet-G.png)


<span data-ttu-id="ba99d-137">Järgmisel joonisel on näidatud tulemuseks saadud tootmise kooslus ja protsessileht, kui osade E ning F koosluseread on konfigureeritud nii, et reatüüp on Fiktiivne.</span><span class="sxs-lookup"><span data-stu-id="ba99d-137">The following illustration shows the resulting Manufacturing BOM and route sheet if the BOM lines for parts E and F are configured so that the line type is Phantom.</span></span> <span data-ttu-id="ba99d-138">Sellel joonisel tähistab (a) toote G kooslust ja (b) toote G protsessilehte.</span><span class="sxs-lookup"><span data-stu-id="ba99d-138">In this illustration, (a) is the BOM for product G, and (b) is the route sheet for product G.</span></span>

![Toode G](media/product-G.png)


## <a name="phantom-and-route-network"></a><span data-ttu-id="ba99d-140">Fiktiivne ja protsessivõrk</span><span class="sxs-lookup"><span data-stu-id="ba99d-140">Phantom and route network</span></span>
<span data-ttu-id="ba99d-141">Fiktiivseid kooslusi saab kasutada ka protsessivõrguga koosluse puhul.</span><span class="sxs-lookup"><span data-stu-id="ba99d-141">Phantom BOMs can also be used for a BOM that has a route network.</span></span> <span data-ttu-id="ba99d-142">Protsessivõrgus tehakse paralleelselt üht või mitut toimingut.</span><span class="sxs-lookup"><span data-stu-id="ba99d-142">In a route network, one or more operations run in parallel.</span></span> <span data-ttu-id="ba99d-143">Järgmisel joonisel on näidatud mitmetasandilises koosluses kasutatava protsessivõrgu näide.</span><span class="sxs-lookup"><span data-stu-id="ba99d-143">The following illustration shows an example of a route network that is used in a multilevel BOM.</span></span> <span data-ttu-id="ba99d-144">Sellel joonisel tähistab (a) toote G ja osa F kooslust ning (b) toote G ja osa F protsessilehte, millel on protsessivõrk.</span><span class="sxs-lookup"><span data-stu-id="ba99d-144">In this illustration, (a) is the BOM for product G and part F, and (b) is the route sheet for product G and part F, which has a route network.</span></span>

![Toode G ja osa F](media/product-G-part-F.png)


<span data-ttu-id="ba99d-146">Järgmisel joonisel tähistab (a) toote G ning osa F kooslust ning (b) toote G ja osa F protsessilehte.</span><span class="sxs-lookup"><span data-stu-id="ba99d-146">In the following illustration, (a) is the BOM for product G and part F, and (b) is the route sheet for product G and part F.</span></span>

![Toode G ja osa F koos protsessilehtedega](media/product-G-part-F-with-route-sheet.png)
