---
title: Kulumiraamatute seadistamine
description: See protseduur juhendab uue kulumiraamatu loomise protsessi ja selle seostamist põhivaragrupiga.
author: saraschi2
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepBookTable, AssetGroupDepBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b0ab7f9332e3224c3dadd62aae532ccffb05c82a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815592"
---
# <a name="set-up-depreciation-books"></a><span data-ttu-id="bb918-103">Kulumiraamatute seadistamine</span><span class="sxs-lookup"><span data-stu-id="bb918-103">Set up depreciation books</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bb918-104">See protseduur juhendab uue kulumiraamatu loomise protsessi ja selle seostamist põhivaragrupiga.</span><span class="sxs-lookup"><span data-stu-id="bb918-104">This procedure walks through the process of creating a new depreciation book and associate it with a fixed asset group.</span></span> 

## <a name="create-a-depreciation-book"></a><span data-ttu-id="bb918-105">Kulumiraamatu loomine</span><span class="sxs-lookup"><span data-stu-id="bb918-105">Create a depreciation book</span></span>
1. <span data-ttu-id="bb918-106">Avage Põhivarad > Seadistus > Kulumiraamatud.</span><span class="sxs-lookup"><span data-stu-id="bb918-106">Go to Fixed assets > Setup > Depreciation books.</span></span>
2. <span data-ttu-id="bb918-107">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="bb918-107">Click New.</span></span>
3. <span data-ttu-id="bb918-108">Sisestage väärtus väljale Kulumiraamat.</span><span class="sxs-lookup"><span data-stu-id="bb918-108">In the Depreciation book field, type a value.</span></span>
4. <span data-ttu-id="bb918-109">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="bb918-109">In the Description field, type a value.</span></span>
5. <span data-ttu-id="bb918-110">Märkige või tühjendage ruut Arvuta kulum.</span><span class="sxs-lookup"><span data-stu-id="bb918-110">Check or uncheck the Calculate depreciation checkbox.</span></span>
6. <span data-ttu-id="bb918-111">Klõpsake väljal Kulumireegel otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="bb918-111">In the Depreciation profile field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="bb918-112">Leidke ja valige loendist soovitud kulumireegel.</span><span class="sxs-lookup"><span data-stu-id="bb918-112">In the list, find and select the desired depreciation profile.</span></span>
8. <span data-ttu-id="bb918-113">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="bb918-113">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="bb918-114">Klõpsake väljal Alternatiivne kulumireegel otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="bb918-114">In the Alternative depreciation profile field, click the drop-down button to open the lookup.</span></span>
10. <span data-ttu-id="bb918-115">Valige loendist soovitud kulumireegel.</span><span class="sxs-lookup"><span data-stu-id="bb918-115">In the list, select the desired depreciation profile.</span></span>
11. <span data-ttu-id="bb918-116">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="bb918-116">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="bb918-117">Plaaniväliseid kulumireegleid kasutatakse vara täiendava kulumi arvestamiseks ebatavalistes olukordades.</span><span class="sxs-lookup"><span data-stu-id="bb918-117">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="bb918-118">Näiteks võite seda kasutada loodusõnnetusest tuleneva kulumi registreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="bb918-118">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
12. <span data-ttu-id="bb918-119">Märkige või tühjendage ruut Loo kulumi korrigeerimised koos aluse korrigeerimistega.</span><span class="sxs-lookup"><span data-stu-id="bb918-119">Check or uncheck the Create depreciation adjustments with basis adjustments checkbox.</span></span>
13. <span data-ttu-id="bb918-120">Klõpsake väljal Kalender otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="bb918-120">In the Calendar field, click the drop-down button to open the lookup.</span></span>
14. <span data-ttu-id="bb918-121">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="bb918-121">In the list, click the link in the selected row.</span></span>

## <a name="associate-the-depreciation-book-with-a-fixed-asset-group"></a><span data-ttu-id="bb918-122">Kulumiraamatu seostamine põhivaragrupiga</span><span class="sxs-lookup"><span data-stu-id="bb918-122">Associate the depreciation book with a fixed asset group</span></span>
1. <span data-ttu-id="bb918-123">Klõpsake suvandit Põhivaragrupid.</span><span class="sxs-lookup"><span data-stu-id="bb918-123">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="bb918-124">Klõpsake väljal Põhivara grupp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="bb918-124">In the Fixed asset group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="bb918-125">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="bb918-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="bb918-126">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="bb918-126">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="bb918-127">Valige suvand väljalt Kulumiarvestusreegel.</span><span class="sxs-lookup"><span data-stu-id="bb918-127">In the Depreciation convention field, select an option.</span></span>
6. <span data-ttu-id="bb918-128">Sisestage number väljale Kasutusiga.</span><span class="sxs-lookup"><span data-stu-id="bb918-128">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="bb918-129">Pange tähele, et välja Kulumiperioodid väärtus arvutatakse pärast kasutusea seadistamist.</span><span class="sxs-lookup"><span data-stu-id="bb918-129">Notice the Depreciation periods field value is calculated after setting the Service life.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]