---
title: "Kliendi makse ülevaated (eelvaade)"
description: "Teema kirjeldab, kuidas funktsioon Kliendi makse ülevaated aitab ennustada, millal arve ära makstakse, ja luua optimeerimisstrateegiaid, mis täiustavad õigel ajal maksmise tõenäosust."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: 
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2018-04-02
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: 841ea53f754f61c2930e77fdafc85eac72f47d7a
ms.openlocfilehash: 9e722db6302d7ef51c01601cde245d4f4a333eba
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---

# <a name="customer-payment-insights-preview"></a><span data-ttu-id="3718e-103">Kliendi makse ülevaated (eelvaade)</span><span class="sxs-lookup"><span data-stu-id="3718e-103">Customer payment insights (preview)</span></span>

[!include[banner](../includes/banner.md)]

> [!IMPORTANT]
> <span data-ttu-id="3718e-104">See funktsioon on suunatud väljalaske osa ja see on saadaval ainult kasutajatele, kes on registreerinud privaatse eelvaate jaoks.</span><span class="sxs-lookup"><span data-stu-id="3718e-104">This feature is part of a targeted release and is only available to users who have opted into the Private Preview.</span></span> <span data-ttu-id="3718e-105">See funktsioon lisatakse tulevasse üldiselt kättesaadavasse väljalaskesse.</span><span class="sxs-lookup"><span data-stu-id="3718e-105">This feature will be included in an upcoming general availability release.</span></span>

# <a name="overview"></a><span data-ttu-id="3718e-106">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="3718e-106">Overview</span></span>

<span data-ttu-id="3718e-107">Organisatsioonidel on tihti raske ennustada, millal klient oma arved ära maksab.</span><span class="sxs-lookup"><span data-stu-id="3718e-107">Organizations often find it challenging to predict when a customer will pay their invoices.</span></span> <span data-ttu-id="3718e-108">Ülevaate puudumine võib põhjustada ebatäpset likviidsuse planeerimist, ebatõhusat kogumist ja võimalust, et tellimused väljastatakse klientidele, kes kujutavad endast krediidiriski.</span><span class="sxs-lookup"><span data-stu-id="3718e-108">This lack of insight can lead to inaccurate cash flow forecasts, inefficient collection processes, and the possibility of orders being released to customers who may pose a credit risk.</span></span> <span data-ttu-id="3718e-109">Funktsioon Kliendi makse ülevaated (eelvaade) kasutab arve maksmise ennustamiseks masinõpet.</span><span class="sxs-lookup"><span data-stu-id="3718e-109">Customer payment insights (preview) uses machine learning to predict when an invoice will be paid.</span></span> <span data-ttu-id="3718e-110">Samuti pakub see optimeerimise strateegiaid, mida saab kohandada, et maksimeerida klientide õigel ajal maksmise tõenäosust.</span><span class="sxs-lookup"><span data-stu-id="3718e-110">It also provides optimization strategies that can be tailored to maximize the probability of customers paying on time.</span></span>

## <a name="predictions"></a><span data-ttu-id="3718e-111">Ennustused</span><span class="sxs-lookup"><span data-stu-id="3718e-111">Predictions</span></span>

<span data-ttu-id="3718e-112">Maksete ennustused võimaldavad organisatsioonidel täiustada oma äritegevusi järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="3718e-112">Payment predictions allow organizations to improve their business processes by helping to:</span></span>

-   <span data-ttu-id="3718e-113">Aitab lihtsalt tuvastada arveid, millele ennustatakse makse hilinemist.</span><span class="sxs-lookup"><span data-stu-id="3718e-113">Easily identify the invoices that are predicted to be paid late.</span></span>
-   <span data-ttu-id="3718e-114">Rakendab asjakohaseid meetmeid, et suurendada õigel ajal maksmise tõenäosust.</span><span class="sxs-lookup"><span data-stu-id="3718e-114">Take appropriate measures to improve chances of getting paid on time.</span></span>

<span data-ttu-id="3718e-115">Funktsioon Kliendi makse ülevaated (eelvaade) kasutab arve maksmise ennustamiseks masinõpet.</span><span class="sxs-lookup"><span data-stu-id="3718e-115">Customer payment insights (preview) uses machine learning to predict when an invoice will be paid.</span></span> <span data-ttu-id="3718e-116">See kasutab ajaloolisi arvete, maksete ja klientide andmeid, et luua masinõppe mudel, mida kasutatakse arve äramaksmise ennustamiseks.</span><span class="sxs-lookup"><span data-stu-id="3718e-116">It uses historical invoice, payment, and customer data to create a machine learning model that is used to predict when an invoice will be paid.</span></span>

<span data-ttu-id="3718e-117">Funktsioon Kliendi makse ülevaated (eelvaade) ennustab iga avatud arve jaoks kolme maksetõenäosust.</span><span class="sxs-lookup"><span data-stu-id="3718e-117">For each open invoice, Customer payment insights (preview) predicts three payment probabilities:</span></span>

-  <span data-ttu-id="3718e-118">Tõenäosus, et makse tehakse õigel ajal (enne arve tähtaega).</span><span class="sxs-lookup"><span data-stu-id="3718e-118">Probability of payment being made on time (within the invoice due date).</span></span>
-  <span data-ttu-id="3718e-119">Tõenäosus, et makse tehakse 30 päeva jooksul pärast arve tähtaega.</span><span class="sxs-lookup"><span data-stu-id="3718e-119">Probability of payment being made within 30 days of the invoice due date.</span></span>
-  <span data-ttu-id="3718e-120">Tõenäosus, et makse tehakse hiljem kui 30 päeva pärast arve tähtaja möödumist.</span><span class="sxs-lookup"><span data-stu-id="3718e-120">Probability of payment being made beyond 30 days of the invoice due date.</span></span>

<span data-ttu-id="3718e-121">Maksete tõenäosusi saate vaadata ennustuste jaotises.</span><span class="sxs-lookup"><span data-stu-id="3718e-121">The probability of payments can be viewed in the prediction section.</span></span>

<span data-ttu-id="3718e-122">[![Maksete ennustused](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)</span><span class="sxs-lookup"><span data-stu-id="3718e-122">[![Payment predictions](./media/Predictions-sm2.png)](./media/Predictions-sm2.png)</span></span>

<span data-ttu-id="3718e-123">Iga arvele määratakse ka võitnud maksetõenäosus, kasutades ühte kolmest eespool määratletud ennustavat maksetõenäosuse stsenaariumit.</span><span class="sxs-lookup"><span data-stu-id="3718e-123">Each invoice is also assigned a winning probability of payment using one of the three predicted payment probabilities scenarios defined above.</span></span> <span data-ttu-id="3718e-124">Suurima maksetõenäosusega stsenaarium on võitnud stsenaarium.</span><span class="sxs-lookup"><span data-stu-id="3718e-124">The scenario with the highest probability of payment is the winning scenario.</span></span>


<span data-ttu-id="3718e-125">Oletame näiteks, et ennustuse järgi on arve õigel ajal maksmise tõenäosus 71 protsenti, arve 30 päeva jooksul maksmise tõenäosus 13 protsenti ja arve pärast tähtajast 30 päeva möödumist maksmise tõenäosus 16 protsenti.</span><span class="sxs-lookup"><span data-stu-id="3718e-125">For example, let’s assume for an invoice the prediction shows a 71 percent probability that the invoice will be paid on time, 13 percent probability that the invoice will be paid within 30 days of due date, and 16 percent probability that the invoice will be paid beyond 30 days of the due date.</span></span> <span data-ttu-id="3718e-126">Suurim tõenäosus näitab, et arve maksmise tõenäoliseim stsenaarium on õigel ajal maksmise stsenaarium, nii et arve märgistatakse õigel ajal maksmise tõenäosusega.</span><span class="sxs-lookup"><span data-stu-id="3718e-126">The highest probability shows that the invoice will be in the on-time scenario, so the invoice will be tagged with the probability of being paid on time.</span></span>

<span data-ttu-id="3718e-127">[![Maksete ennustused](./media/payment-predict.png)](./media/payment-predict.png)</span><span class="sxs-lookup"><span data-stu-id="3718e-127">[![Payment predictions](./media/payment-predict.png)](./media/payment-predict.png)</span></span>

## <a name="optimization-strategies"></a><span data-ttu-id="3718e-128">Optimeerimise strateegiad</span><span class="sxs-lookup"><span data-stu-id="3718e-128">Optimization strategies</span></span>

<span data-ttu-id="3718e-129">Peale maksete ennustuste saab funktsioon Kliendi makse ülevaated (eelvaade) kasutada ka optimeerimise strateegiaid, et täiustada õigel ajal maksmiste tõenäosust.</span><span class="sxs-lookup"><span data-stu-id="3718e-129">In addition to payment predictions, the Customer Payment Insights (preview) can use optimization strategies to improve the chances of getting paid on time.</span></span> <span data-ttu-id="3718e-130">See võimaldab organisatsioonidel teha tegurite mõju analüüsi, lastes kasutajatel kohandada arvete ja klientide parameetreid ja seejärel võrrelda muudatuste mõju arvete õigel ajal maksmise tõenäosusele.</span><span class="sxs-lookup"><span data-stu-id="3718e-130">This lets organizations do 'What if' analysis by allowing users to adjust invoice and customer parameters and then compare the corresponding effect on the probability of receiving payment on invoices on time.</span></span>

<span data-ttu-id="3718e-131">Näiteks võib organisatsioon soovida hinnata, kuidas mõjutab maksete õigeaegsust arvete skonto värskendamine.</span><span class="sxs-lookup"><span data-stu-id="3718e-131">For example, an organization may want to evaluate the effect of updating the cash discount on invoices on the probability of receiving the payment on time.</span></span> <span data-ttu-id="3718e-132">Kui arved on optimeeritud kasutama uut allahindlust, saavad kasutajad üle vaadata, kuidas allahindluse rakendamine mõjutab nende arvete õigeaegset maksmist.</span><span class="sxs-lookup"><span data-stu-id="3718e-132">When the invoices are optimized to use the new discount, the users can review the effect of applying the discount on the probability of receiving payments for those invoices on time.</span></span> <span data-ttu-id="3718e-133">Kui allahindluse rakendamise kulu on võrreldes õigeaegse makse eelisega minimaalne, siis võib organisatsioon valida selle allahindluse rakendamise kõikidele tulevastele avatud tellimustele.</span><span class="sxs-lookup"><span data-stu-id="3718e-133">If the cost of applying the discount is minimal when compared to the benefit of collecting the payment on time, the organization may choose to apply the selected discount to all future open orders.</span></span>

> [!NOTE] 
> <span data-ttu-id="3718e-134">Praegu on funktsiooni Kliendi makse ülevaated (eelvaade) ainuke saadavalolev optimeerimise strateegia allahindlus.</span><span class="sxs-lookup"><span data-stu-id="3718e-134">Currently, only discount is available as an optimization strategy for Customer payment insights (preview).</span></span>

<span data-ttu-id="3718e-135">[![Optimeeritud ennustused](./media/optimized-pay.png)](./media/optimized-pay.png)</span><span class="sxs-lookup"><span data-stu-id="3718e-135">[![Optimized predictions](./media/optimized-pay.png)](./media/optimized-pay.png)</span></span>

## <a name="how-to-get-customer-payment-insights-preview"></a><span data-ttu-id="3718e-136">Kuidas hankida funktsioon Kliendi makse ülevaated (eelvaade)</span><span class="sxs-lookup"><span data-stu-id="3718e-136">How to get Customer payment insights (preview)</span></span>

<span data-ttu-id="3718e-137">Kui olete huvitatud funktsiooni Kliendi makse ülevaated (eelvaade) proovimisest, saatke meil [finantsülevaadete eelvaate töörühmale](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="3718e-137">If you are interested in trying Customer payment insights (preview), please email [Finance Insights Preview team](mailto:fiap@microsoft.com).</span></span> 

## <a name="privacy-statement"></a><span data-ttu-id="3718e-138">Privaatsusavaldus</span><span class="sxs-lookup"><span data-stu-id="3718e-138">Privacy Statement</span></span>

<span data-ttu-id="3718e-139">Eelvaated hoiustavad kliendiandmeid Ameerika Ühendriikides.</span><span class="sxs-lookup"><span data-stu-id="3718e-139">Previews store customer data in the United States.</span></span> <span data-ttu-id="3718e-140">Peale selle, eelvaade 1) võib kasutada vähem privaatsus- ja turbemeetmeid kui rakenduse Dynamics 365 for Finance and Operations teenus, 2) ei ole hõlmatud selle teenuse teenusetaseme leppes, 3) ei tohi olla kasutusel isiklike andmete ega muude andmete töötlemiseks, mis on seaduste või määrustega kaitstud, ja 4) on piiratud toega.</span><span class="sxs-lookup"><span data-stu-id="3718e-140">In addition, previews (1) may utilize less privacy and security measures than the Dynamics 365 for Finance and Operations service, (2) are not included in the service level agreement for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) has limited support.</span></span>

