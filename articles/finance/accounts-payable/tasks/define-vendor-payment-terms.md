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
ms.openlocfilehash: 7e6778f61a9367399e4b71d5b2bb2459c09ba508
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3143888"
---
# <a name="define-vendor-payment-terms"></a><span data-ttu-id="92bd0-103">Hankija maksetingimuste määratlemine</span><span class="sxs-lookup"><span data-stu-id="92bd0-103">Define vendor payment terms</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="92bd0-104">Selles teemas selgitatakse, kuidas sätestada maksetingimusi tarnija arvete jaoks.</span><span class="sxs-lookup"><span data-stu-id="92bd0-104">This topic explains how to set up payment terms for vendor invoices.</span></span> <span data-ttu-id="92bd0-105">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="92bd0-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="92bd0-106">Avage **Navigeerimispaan > Moodulid > Ostureskontro > Makse häälestus > Maksetingimused**.</span><span class="sxs-lookup"><span data-stu-id="92bd0-106">Go to **Navigation pane > Modules > Accounts payable > Payment setup > Terms of payment**.</span></span>
2. <span data-ttu-id="92bd0-107">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="92bd0-107">Select **New**.</span></span> <span data-ttu-id="92bd0-108">Lehte Maksetingimused kasutatakse määratlemaks, kuidas tähtaega arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="92bd0-108">The Terms of payment page is used to define how the due date will be calculated.</span></span> <span data-ttu-id="92bd0-109">Seda ei kasutata määratlemaks, kuidas skonto kuupäeva arvutatakse.</span><span class="sxs-lookup"><span data-stu-id="92bd0-109">It is not used to define how the cash discount date will be calculated.</span></span>  
3. <span data-ttu-id="92bd0-110">Sisestage väärtus väljale **Maksetingimused**.</span><span class="sxs-lookup"><span data-stu-id="92bd0-110">In the **Terms of payment** field, type a value.</span></span>
4. <span data-ttu-id="92bd0-111">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="92bd0-111">In the **Description field**, type a value.</span></span>
5. <span data-ttu-id="92bd0-112">Sisestage number väljale **Päevad**.</span><span class="sxs-lookup"><span data-stu-id="92bd0-112">In the **Days** field, enter a number.</span></span> <span data-ttu-id="92bd0-113">Siin sisestatud numbrit kasutatakse tähtajale või makseviisis määratletud perioodi lõppu lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="92bd0-113">The number entered here will be used to add to the due date, or to the end of the period identified in the Payment method.</span></span> <span data-ttu-id="92bd0-114">Näiteks kui valite **Neto**, lisatakse number tähtajale.</span><span class="sxs-lookup"><span data-stu-id="92bd0-114">For example, if you select **Net**, the number will be added to the due date.</span></span> <span data-ttu-id="92bd0-115">**Praeguse kuu** valimisel lisatakse tähtaja arvutamiseks number praeguse kuu viimasele päevale.</span><span class="sxs-lookup"><span data-stu-id="92bd0-115">If you select **Current month**, it will add the number to the last day of the current month to calculate the due date.</span></span>  
6. <span data-ttu-id="92bd0-116">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="92bd0-116">Select **Save**.</span></span>
7. <span data-ttu-id="92bd0-117">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="92bd0-117">Close the page.</span></span>
8. <span data-ttu-id="92bd0-118">Avage **Ostureskontro > Makse seadistus > Skontod**.</span><span class="sxs-lookup"><span data-stu-id="92bd0-118">Go to **Accounts payable > Payment setup > Cash discounts**.</span></span>
9. <span data-ttu-id="92bd0-119">Valige suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="92bd0-119">Select **New**.</span></span>
10. <span data-ttu-id="92bd0-120">Sisestage ID väljale **Skonto**.</span><span class="sxs-lookup"><span data-stu-id="92bd0-120">In the **Cash discount** field, enter an ID.</span></span>
11. <span data-ttu-id="92bd0-121">Sisestage väärtus väljale **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="92bd0-121">In the **Description** field, type a value.</span></span>
12. <span data-ttu-id="92bd0-122">Kui hankija pakub mitmetasandilist allahindlust, valige järgmine skonto pärast praeguse aegumist.</span><span class="sxs-lookup"><span data-stu-id="92bd0-122">If the vendor offers a tiered discount, select the next cash discount after the current one is expired.</span></span>
13. <span data-ttu-id="92bd0-123">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="92bd0-123">Close the page.</span></span>
14. <span data-ttu-id="92bd0-124">Sisestage number väljale **Päevad**.</span><span class="sxs-lookup"><span data-stu-id="92bd0-124">In the **Days** field, enter a number.</span></span> <span data-ttu-id="92bd0-125">Väljale **Päevad** sisestatud kogust kasutatakse skonto kuupäeva arvutamiseks selle põhjal, milline suvand väljal **Neto/praegune** valiti.</span><span class="sxs-lookup"><span data-stu-id="92bd0-125">The quantity entered in the **Days** field will be used to calculate the Cash discount date, based on what option was selected in the **Net/Current** field.</span></span> <span data-ttu-id="92bd0-126">**Neto** valimisel lisatakse skonto kuupäeva määramiseks kogus arve kuupäevale.</span><span class="sxs-lookup"><span data-stu-id="92bd0-126">If **Net** was selected, the quantity will be added to the invoice date to determine the cash discount date.</span></span> <span data-ttu-id="92bd0-127">**Praeguse kuu** valimisel lisatakse skonto kuupäeva määramiseks kogus arve kuupäevale.</span><span class="sxs-lookup"><span data-stu-id="92bd0-127">If **Current month** was selected, the quantity will be added to the end of the currency month to determine the cash discount date.</span></span>  
15. <span data-ttu-id="92bd0-128">Sisestage skonto protsent väljale **Allahindlus**.</span><span class="sxs-lookup"><span data-stu-id="92bd0-128">Enter the percentage of the cash discount in the **Discount** field.</span></span> 
16. <span data-ttu-id="92bd0-129">Sisestage põhikonto, kuhu skonto sisestatakse kliendiarvete puhul, seejärel sisestage põhikonto, kuhu skonto sisestatakse hankija arvete puhul.</span><span class="sxs-lookup"><span data-stu-id="92bd0-129">Enter the main account to which the cash discount will be posted for customer invoices, then enter the main account to which the cash discount will be posted for vendor invoices.</span></span> <span data-ttu-id="92bd0-130">Kui suvand **Allahindluse vastaskontod** on seatud valikule **Kasuta hankija allahindluse jaoks põhikontot**, siis kasutatakse põhikontot.</span><span class="sxs-lookup"><span data-stu-id="92bd0-130">If **Discount offset accounts** is set to **Use main account for vendor discount**, then the Main account will be used.</span></span> <span data-ttu-id="92bd0-131">Kui suvand on seatud valikule **Kontod arve real**, sisestatakse skonto arve ridadel vara/kulu kontodele.</span><span class="sxs-lookup"><span data-stu-id="92bd0-131">If the option is set to **Accounts on the invoice lines**, the cash discount will be posted to the asset/expense accounts on the invoice's lines.</span></span>  
17. <span data-ttu-id="92bd0-132">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="92bd0-132">Select **Save**.</span></span>

