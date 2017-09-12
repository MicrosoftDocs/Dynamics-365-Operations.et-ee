--- 
title: "Hankija maksetingimuste määratlemine"
description: Seadistage hankija arvete maksetingimused.
author: abruer
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
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: a00ca73b1bc301960132a86846749d12c39ed3f7
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="define-vendor-payment-terms"></a><span data-ttu-id="95364-103">Hankija maksetingimuste määratlemine</span><span class="sxs-lookup"><span data-stu-id="95364-103">Define vendor payment terms</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="95364-104">Seadistage hankija arvete maksetingimused.</span><span class="sxs-lookup"><span data-stu-id="95364-104">Set up payment terms for vendor invoices.</span></span> <span data-ttu-id="95364-105">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="95364-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="95364-106">Avage Ostureskontro > Makse seadistus > Maksetingimused.</span><span class="sxs-lookup"><span data-stu-id="95364-106">Go to Accounts payable > Payment setup > Terms of payment.</span></span>
2. <span data-ttu-id="95364-107">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="95364-107">Click New.</span></span>
    * <span data-ttu-id="95364-108">Lehte Maksetingimused kasutatakse määratlemaks, kuidas tähtaega arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="95364-108">The Terms of payment page is used to define how the due date will be calculated.</span></span> <span data-ttu-id="95364-109">Seda ei kasutata määratlemaks, kuidas skonto kuupäeva arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="95364-109">It is not used to define how the cash discount date will be calculated.</span></span>  
3. <span data-ttu-id="95364-110">Sisestage väärtus väljale Maksetingimused.</span><span class="sxs-lookup"><span data-stu-id="95364-110">In the Terms of payment field, type a value.</span></span>
4. <span data-ttu-id="95364-111">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="95364-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="95364-112">Sisestage number väljale Päevad.</span><span class="sxs-lookup"><span data-stu-id="95364-112">In the Days field, enter a number.</span></span>
    * <span data-ttu-id="95364-113">Siin sisestatud numbrit kasutatakse tähtajale või makseviisis määratletud perioodi lõppu lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="95364-113">The number entered here will be used to add to the due date, or to the end of the period identified in the Payment method.</span></span> <span data-ttu-id="95364-114">Näiteks kui valite Neto, lisatakse number tähtajale.</span><span class="sxs-lookup"><span data-stu-id="95364-114">For example, if you select Net, the number will be added to the due date.</span></span> <span data-ttu-id="95364-115">Praeguse kuu valimisel lisatakse tähtaja arvutamiseks number praeguse kuu viimasele päevale.</span><span class="sxs-lookup"><span data-stu-id="95364-115">If you select Current month, it will add the number to the last day of the current month to calculate the due date.</span></span>  
6. <span data-ttu-id="95364-116">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="95364-116">Click Save.</span></span>
7. <span data-ttu-id="95364-117">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="95364-117">Close the page.</span></span>
8. <span data-ttu-id="95364-118">Avage Ostureskontro > Makse seadistus > Skontod.</span><span class="sxs-lookup"><span data-stu-id="95364-118">Go to Accounts payable > Payment setup > Cash discounts.</span></span>
9. <span data-ttu-id="95364-119">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="95364-119">Click New.</span></span>
10. <span data-ttu-id="95364-120">Sisestage ID väljale Skonto.</span><span class="sxs-lookup"><span data-stu-id="95364-120">In the Cash discount field, enter an ID.</span></span>
11. <span data-ttu-id="95364-121">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="95364-121">In the Description field, type a value.</span></span>
12. <span data-ttu-id="95364-122">Kui hankija pakub mitmetasandilist allahindlust, valige järgmine skonto pärast praeguse aegumist.</span><span class="sxs-lookup"><span data-stu-id="95364-122">If the vendor offers a tiered discount, select the next cash discount after the current one is expired.</span></span>
13. <span data-ttu-id="95364-123">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="95364-123">Close the page.</span></span>
14. <span data-ttu-id="95364-124">Sisestage number väljale Päevad.</span><span class="sxs-lookup"><span data-stu-id="95364-124">In the Days field, enter a number.</span></span>
    * <span data-ttu-id="95364-125">Väljale Päevad sisestatud kogust kasutatakse skonto kuupäeva arvutamiseks selle põhjal, milline suvand väljal Neto/praegune valiti.</span><span class="sxs-lookup"><span data-stu-id="95364-125">The quantity entered in the Days field will be used to calculate the Cash discount date, based on what option was selected in the Net/Current field.</span></span> <span data-ttu-id="95364-126">Neto valimisel lisatakse skonto kuupäeva määramiseks kogus arve kuupäevale.</span><span class="sxs-lookup"><span data-stu-id="95364-126">If Net was selected, the quantity will be added to the invoice date to determine the cash discount date.</span></span> <span data-ttu-id="95364-127">Praeguse kuu valimisel lisatakse skonto kuupäeva määramiseks kogus praeguse kuu lõppu.</span><span class="sxs-lookup"><span data-stu-id="95364-127">If Current month was selected, the quantity will be added to the end of the currency month to determine the cash discount date.</span></span>  
15. <span data-ttu-id="95364-128">Sisestage skonto protsent väljale Allahindlus.</span><span class="sxs-lookup"><span data-stu-id="95364-128">Enter the percentage of the cash discount in the Discount field.</span></span> 
16. <span data-ttu-id="95364-129">Sisestage põhikonto, millele skonto kliendiarvete puhul sisestatakse.</span><span class="sxs-lookup"><span data-stu-id="95364-129">Enter the main account to which the cash discount will be posted for customer invoices.</span></span>
17. <span data-ttu-id="95364-130">Sisestage põhikonto, millele skonto hankija arvete puhul sisestatakse.</span><span class="sxs-lookup"><span data-stu-id="95364-130">Enter the main account to which the cash discount will be posted for vendor invoices.</span></span>
    * <span data-ttu-id="95364-131">Kui suvand Allahindluse vastaskontod on seatud valikule Kasuta hankija allahindluse jaoks põhikontot, siis kasutatakse põhikontot.</span><span class="sxs-lookup"><span data-stu-id="95364-131">If 'Discount offset accounts' is set to Use main account for vendor discount, then the Main account will be used.</span></span>  <span data-ttu-id="95364-132">Kui suvand on seatud valikule Kontod arve real, sisestatakse skonto arve ridadel vara/kulu kontodele.</span><span class="sxs-lookup"><span data-stu-id="95364-132">If the option is set to Accounts on the invoice lines, the cash discount will be posted to the asset/expense accounts on the invoice's lines.</span></span>  
18. <span data-ttu-id="95364-133">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="95364-133">Click Save.</span></span>


