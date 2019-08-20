---
title: Hankija maksetingimuste määratlemine
description: Selles teemas selgitatakse, kuidas sätestada maksetingimusi tarnija arvete jaoks.
author: abruer
manager: AnnBe
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PaymTerm, CashDisc
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6432d04aa821e76d67e2c430e514f4b9056d8228
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1843189"
---
# <a name="define-vendor-payment-terms"></a><span data-ttu-id="031e8-103">Hankija maksetingimuste määratlemine</span><span class="sxs-lookup"><span data-stu-id="031e8-103">Define vendor payment terms</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="031e8-104">Selles teemas selgitatakse, kuidas sätestada maksetingimusi tarnija arvete jaoks.</span><span class="sxs-lookup"><span data-stu-id="031e8-104">This topic explains how to set up payment terms for vendor invoices.</span></span> <span data-ttu-id="031e8-105">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="031e8-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="031e8-106">Avage **Navigeerimispaan > Moodulid > Ostureskontro > Makse häälestus > Maksetingimused**.</span><span class="sxs-lookup"><span data-stu-id="031e8-106">Go to **Navigation pane > Modules > Accounts payable > Payment setup > Terms of payment**.</span></span>
2. <span data-ttu-id="031e8-107">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="031e8-107">Select **New**.</span></span> <span data-ttu-id="031e8-108">Lehte Maksetingimused kasutatakse määratlemaks, kuidas tähtaega arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="031e8-108">The Terms of payment page is used to define how the due date will be calculated.</span></span> <span data-ttu-id="031e8-109">Seda ei kasutata määratlemaks, kuidas skonto kuupäeva arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="031e8-109">It is not used to define how the cash discount date will be calculated.</span></span>  
3. <span data-ttu-id="031e8-110">Sisestage väärtus väljale **Maksetingimused**.</span><span class="sxs-lookup"><span data-stu-id="031e8-110">In the **Terms of payment** field, type a value.</span></span>
4. <span data-ttu-id="031e8-111">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="031e8-111">In the **Description field**, type a value.</span></span>
5. <span data-ttu-id="031e8-112">Sisestage number väljale **Päevad**.</span><span class="sxs-lookup"><span data-stu-id="031e8-112">In the **Days** field, enter a number.</span></span> <span data-ttu-id="031e8-113">Siin sisestatud numbrit kasutatakse tähtajale või makseviisis määratletud perioodi lõppu lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="031e8-113">The number entered here will be used to add to the due date, or to the end of the period identified in the Payment method.</span></span> <span data-ttu-id="031e8-114">Näiteks kui valite **Neto**, lisatakse number tähtajale.</span><span class="sxs-lookup"><span data-stu-id="031e8-114">For example, if you select **Net**, the number will be added to the due date.</span></span> <span data-ttu-id="031e8-115">**Praeguse kuu** valimisel lisatakse tähtaja arvutamiseks number praeguse kuu viimasele päevale.</span><span class="sxs-lookup"><span data-stu-id="031e8-115">If you select **Current month**, it will add the number to the last day of the current month to calculate the due date.</span></span>  
6. <span data-ttu-id="031e8-116">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="031e8-116">Select **Save**.</span></span>
7. <span data-ttu-id="031e8-117">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="031e8-117">Close the page.</span></span>
8. <span data-ttu-id="031e8-118">Avage **Ostureskontro > Makse seadistus > Skontod**.</span><span class="sxs-lookup"><span data-stu-id="031e8-118">Go to **Accounts payable > Payment setup > Cash discounts**.</span></span>
9. <span data-ttu-id="031e8-119">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="031e8-119">Select **New**.</span></span>
10. <span data-ttu-id="031e8-120">Sisestage ID väljale **Skonto**.</span><span class="sxs-lookup"><span data-stu-id="031e8-120">In the **Cash discount** field, enter an ID.</span></span>
11. <span data-ttu-id="031e8-121">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="031e8-121">In the **Description** field, type a value.</span></span>
12. <span data-ttu-id="031e8-122">Kui hankija pakub mitmetasandilist allahindlust, valige järgmine skonto pärast praeguse aegumist.</span><span class="sxs-lookup"><span data-stu-id="031e8-122">If the vendor offers a tiered discount, select the next cash discount after the current one is expired.</span></span>
13. <span data-ttu-id="031e8-123">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="031e8-123">Close the page.</span></span>
14. <span data-ttu-id="031e8-124">Sisestage number väljale **Päevad**.</span><span class="sxs-lookup"><span data-stu-id="031e8-124">In the **Days** field, enter a number.</span></span> <span data-ttu-id="031e8-125">Väljale **Päevad** sisestatud kogust kasutatakse skonto kuupäeva arvutamiseks selle põhjal, milline suvand väljal **Neto/praegune** valiti.</span><span class="sxs-lookup"><span data-stu-id="031e8-125">The quantity entered in the **Days** field will be used to calculate the Cash discount date, based on what option was selected in the **Net/Current** field.</span></span> <span data-ttu-id="031e8-126">**Neto** valimisel lisatakse skonto kuupäeva määramiseks kogus arve kuupäevale.</span><span class="sxs-lookup"><span data-stu-id="031e8-126">If **Net** was selected, the quantity will be added to the invoice date to determine the cash discount date.</span></span> <span data-ttu-id="031e8-127">**Praeguse kuu** valimisel lisatakse skonto kuupäeva määramiseks kogus arve kuupäevale.</span><span class="sxs-lookup"><span data-stu-id="031e8-127">If **Current month** was selected, the quantity will be added to the end of the currency month to determine the cash discount date.</span></span>  
15. <span data-ttu-id="031e8-128">Sisestage skonto protsent väljale **Allahindlus**.</span><span class="sxs-lookup"><span data-stu-id="031e8-128">Enter the percentage of the cash discount in the **Discount** field.</span></span> 
16. <span data-ttu-id="031e8-129">Sisestage põhikonto, kuhu skonto sisestatakse kliendiarvete puhul, seejärel sisestage põhikonto, kuhu skonto sisestatakse hankija arvete puhul.</span><span class="sxs-lookup"><span data-stu-id="031e8-129">Enter the main account to which the cash discount will be posted for customer invoices, then enter the main account to which the cash discount will be posted for vendor invoices.</span></span> <span data-ttu-id="031e8-130">Kui suvand **Allahindluse vastaskontod** on seatud valikule **Kasuta hankija allahindluse jaoks põhikontot**, siis kasutatakse põhikontot.</span><span class="sxs-lookup"><span data-stu-id="031e8-130">If **Discount offset accounts** is set to **Use main account for vendor discount**, then the Main account will be used.</span></span> <span data-ttu-id="031e8-131">Kui suvand on seatud valikule **Kontod arve real**, sisestatakse skonto arve ridadel vara/kulu kontodele.</span><span class="sxs-lookup"><span data-stu-id="031e8-131">If the option is set to **Accounts on the invoice lines**, the cash discount will be posted to the asset/expense accounts on the invoice's lines.</span></span>  
17. <span data-ttu-id="031e8-132">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="031e8-132">Select **Save**.</span></span>

