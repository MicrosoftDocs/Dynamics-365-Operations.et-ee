---
title: Põhivara kulumiraamatute seadistamine (mai 2016)
description: See ülesande juhend loob uue kulumiraamatu ja seostab selle põhivaragrupiga.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1fd53ea1dff9b116d19c525c5d6967ece0993b6f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566911"
---
# <a name="set-up-depreciation-books-may-2016"></a><span data-ttu-id="98db7-103">Põhivara kulumiraamatute seadistamine (mai 2016)</span><span class="sxs-lookup"><span data-stu-id="98db7-103">Set up depreciation books (May 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="98db7-104">See ülesande juhend loob uue kulumiraamatu ja seostab selle põhivaragrupiga.</span><span class="sxs-lookup"><span data-stu-id="98db7-104">This task guide will create a new depreciation book and associate it with a fixed asset group.</span></span>  <span data-ttu-id="98db7-105">See kasutab USMF-i juriidilise isiku puhul raamatupidaja rolli ja demoandmeid.</span><span class="sxs-lookup"><span data-stu-id="98db7-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-depreciation-book"></a><span data-ttu-id="98db7-106">Kulumiraamatu loomine</span><span class="sxs-lookup"><span data-stu-id="98db7-106">Create a depreciation book</span></span>
1. <span data-ttu-id="98db7-107">Avage Põhivarad > Seadistus > Kulumiraamatud.</span><span class="sxs-lookup"><span data-stu-id="98db7-107">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="98db7-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="98db7-108">Click New.</span></span>
3. <span data-ttu-id="98db7-109">Sisestage väärtus väljale Kulumiraamat.</span><span class="sxs-lookup"><span data-stu-id="98db7-109">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="98db7-110">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="98db7-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="98db7-111">Märkige või tühjendage ruut Arvuta kulum.</span><span class="sxs-lookup"><span data-stu-id="98db7-111">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="98db7-112">Klõpsake väljal Kulumireegel otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="98db7-112">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="98db7-113">Leidke ja valige loendist soovitud kulumireegel.</span><span class="sxs-lookup"><span data-stu-id="98db7-113">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="98db7-114">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="98db7-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="98db7-115">Klõpsake väljal Alternatiivne kulumireegel otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="98db7-115">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="98db7-116">Valige loendist soovitud kulumireegel.</span><span class="sxs-lookup"><span data-stu-id="98db7-116">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="98db7-117">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="98db7-117">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="98db7-118">Plaaniväliseid kulumireegleid kasutatakse vara täiendava kulumi arvestamiseks ebatavalistes olukordades.</span><span class="sxs-lookup"><span data-stu-id="98db7-118">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="98db7-119">Näiteks võite seda kasutada loodusõnnetusest tuleneva kulumi registreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="98db7-119">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="98db7-120">Märkige või tühjendage ruut Loo kulumi korrigeerimised koos aluse korrigeerimistega.</span><span class="sxs-lookup"><span data-stu-id="98db7-120">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="98db7-121">Klõpsake väljal Kalender otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="98db7-121">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="98db7-122">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="98db7-122">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="98db7-123">Kulumiraamatu seostamine põhivaragrupiga</span><span class="sxs-lookup"><span data-stu-id="98db7-123">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="98db7-124">Klõpsake suvandit Põhivaragrupid.</span><span class="sxs-lookup"><span data-stu-id="98db7-124">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="98db7-125">Klõpsake väljal Põhivara grupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="98db7-125">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="98db7-126">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="98db7-126">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="98db7-127">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="98db7-127">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="98db7-128">Valige suvand väljalt Kulumiarvestusreegel.</span><span class="sxs-lookup"><span data-stu-id="98db7-128">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="98db7-129">Sisestage number väljale Kasutusiga.</span><span class="sxs-lookup"><span data-stu-id="98db7-129">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="98db7-130">Pange tähele, et välja Kulumiperioodid väärtus arvutatakse pärast kasutusea seadistamist.</span><span class="sxs-lookup"><span data-stu-id="98db7-130">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  

