--- 
title: "Saate häälestada käibemaksukoode."
description: "Käibemaksukoodid luuakse iga kaudse maksu või kohustuse puhul, mida juriidiline isik on kohustatud arvutama, koguma ja käibemaksuhalduritele maksma."
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 968f4bb9f7d54cdb4de4f7842ed1777c9a9acd64
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="set-up-sales-tax-codes"></a><span data-ttu-id="d5db0-103">Saate häälestada käibemaksukoode.</span><span class="sxs-lookup"><span data-stu-id="d5db0-103">Set up sales tax codes</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d5db0-104">Käibemaksukoodid luuakse iga kaudse maksu või kohustuse puhul, mida juriidiline isik on kohustatud arvutama, koguma ja käibemaksuhalduritele maksma.</span><span class="sxs-lookup"><span data-stu-id="d5db0-104">Sales tax codes are created for every indirect tax or duty that the legal entity is obligated to calculate, collect, and pay to sales tax authorities.</span></span>

<span data-ttu-id="d5db0-105">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="d5db0-105">This task uses the USMF demo company.</span></span>



1. <span data-ttu-id="d5db0-106">Avage Maks > Kaudsed maksud > Käibemaks > Käibemaksukoodid.</span><span class="sxs-lookup"><span data-stu-id="d5db0-106">Go to Tax > Indirect taxes > Sales tax > Sales tax codes.</span></span>
2. <span data-ttu-id="d5db0-107">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="d5db0-107">Click New.</span></span>
3. <span data-ttu-id="d5db0-108">Sisestage väärtus väljale Käibemaksukood.</span><span class="sxs-lookup"><span data-stu-id="d5db0-108">In the Sales tax code field, type a value.</span></span>
4. <span data-ttu-id="d5db0-109">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="d5db0-109">In the Name field, type a value.</span></span>
5. <span data-ttu-id="d5db0-110">Valige tasakaalustusperiood, määramaks, millisele maksuhaldurile ning mis vahemikega tuleb seda käibemaksu esitada ja maksta.</span><span class="sxs-lookup"><span data-stu-id="d5db0-110">Select a Settlement period to specify which Sales tax authority and in which intervals this sales tax needs to be reported and paid.</span></span>
6. <span data-ttu-id="d5db0-111">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="d5db0-111">In the list, click the link in the selected row.</span></span>
7. <span data-ttu-id="d5db0-112">Valige Pearaamatu sisestusgrupp, et määrata põhikontod käibemaksu sisestamiseks pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="d5db0-112">Select a Ledger posting group to specify the main accounts to post sales tax to the general ledger.</span></span>
8. <span data-ttu-id="d5db0-113">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="d5db0-113">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="d5db0-114">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="d5db0-114">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="d5db0-115">Laiendage kiirvahekaarti Arvutus.</span><span class="sxs-lookup"><span data-stu-id="d5db0-115">Expand the Calculation FastTab.</span></span>
    * <span data-ttu-id="d5db0-116">Kiirvahekaardil Arvutamine on mitu välja, mis määravad, kuidas käibemaksusummasid arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="d5db0-116">The Calculation FastTab has multiple fields that control how sales tax amounts will be calculated.</span></span>  
11. <span data-ttu-id="d5db0-117">Klõpsake toimingupaanil suvandit Käibemaksukood.</span><span class="sxs-lookup"><span data-stu-id="d5db0-117">On the Action Pane, click Sales tax code.</span></span>
12. <span data-ttu-id="d5db0-118">Klõpsake suvandit Väärtused.</span><span class="sxs-lookup"><span data-stu-id="d5db0-118">Click Values.</span></span>
13. <span data-ttu-id="d5db0-119">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="d5db0-119">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="d5db0-120">Sisestage selle maksukoodi väärtus.</span><span class="sxs-lookup"><span data-stu-id="d5db0-120">Enter the value for this tax code.</span></span>
    * <span data-ttu-id="d5db0-121">Kiirvahekaardi Arvutamine väljal Päritolu korrutatakse juhul, kui Summa ühiku kohta on valitud, käibemaksusumma arvutamiseks väärtus kande kogusega.</span><span class="sxs-lookup"><span data-stu-id="d5db0-121">On the Calculation FastTab, in the Origin field, if Amount per unit is selected, the value will be multiplied by the quantity on the transaction to calculate the sales tax amount.</span></span>  <span data-ttu-id="d5db0-122">Kui maksukood pole ühikupõhine maks, on väärtus protsent, mis rakendatakse selle maksukoodi päritolule käibemaksu summa arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="d5db0-122">If the tax code is not a unit based tax, the value is a percentage that is applied on the Origin for this tax code to calculate the sales tax amount.</span></span>     
15. <span data-ttu-id="d5db0-123">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="d5db0-123">Click Save.</span></span>
16. <span data-ttu-id="d5db0-124">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d5db0-124">Close the page.</span></span>
17. <span data-ttu-id="d5db0-125">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="d5db0-125">Click Save.</span></span>


