--- 
title: "Garantiikirja jaoks panga süsteemiteenuse lepingu loomine"
description: "See ülesanne loob panga süsteemiteenuse leppe garantiikirja töötlemiseks."
author: ShylaThompson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 954fb358a1733a4f386553a349e10c2236597096
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-bank-facility-agreement-for-the-letter-of-guarantee"></a><span data-ttu-id="51a01-103">Garantiikirja jaoks panga süsteemiteenuse lepingu loomine</span><span class="sxs-lookup"><span data-stu-id="51a01-103">Create a bank facility agreement for the letter of guarantee</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="51a01-104">See ülesanne loob panga süsteemiteenuse leppe garantiikirja töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="51a01-104">This task creates a bank facility agreement to process a letter of guarantee.</span></span> <span data-ttu-id="51a01-105">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="51a01-105">This task uses the USMF demo company.</span></span> 


## <a name="create-bank-facility-agreement"></a><span data-ttu-id="51a01-106">Panga süsteemiteenuse leppe loomine</span><span class="sxs-lookup"><span data-stu-id="51a01-106">Create Bank facility agreement</span></span>
1. <span data-ttu-id="51a01-107">Minge jaotisse Sularaha- ja pangahaldus > Garantiikirjad > Panga süsteemiteenuse lepped.</span><span class="sxs-lookup"><span data-stu-id="51a01-107">Go to Cash and bank management > Letters of guarantee > Bank facility agreements.</span></span>
2. <span data-ttu-id="51a01-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="51a01-108">Click New.</span></span>
3. <span data-ttu-id="51a01-109">Sisestage väljale Leppe number kande pangaleppe number.</span><span class="sxs-lookup"><span data-stu-id="51a01-109">In the Agreement number field, enter the bank agreement number for the transaction.</span></span>
4. <span data-ttu-id="51a01-110">Valige väljal Pangakonto selle pangakonto number, mille jaoks garantiikiri on avatud.</span><span class="sxs-lookup"><span data-stu-id="51a01-110">In the Bank account field, select the bank account number for which the letter of guarantee is open.</span></span> 
5. <span data-ttu-id="51a01-111">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="51a01-111">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="51a01-112">Sisestage väljale Alguskuupäev kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="51a01-112">In the Start date field, enter a date and time.</span></span>
7. <span data-ttu-id="51a01-113">Sisestage väljale Lõppkuupäev kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="51a01-113">In the End date field, enter a date and time.</span></span>
8. <span data-ttu-id="51a01-114">Lülitage jaotise Üldine laiendamist.</span><span class="sxs-lookup"><span data-stu-id="51a01-114">Toggle the expansion of the General section.</span></span>
9. <span data-ttu-id="51a01-115">Klõpsake käsku Lisa rida.</span><span class="sxs-lookup"><span data-stu-id="51a01-115">Click Add line.</span></span>
10. <span data-ttu-id="51a01-116">Klõpsake väljal Süsteemiteenuse tüüp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="51a01-116">In the Facility type field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="51a01-117">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="51a01-117">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="51a01-118">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="51a01-118">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="51a01-119">Sisestage väljale Piirang pangaga kokkulepitud summa.</span><span class="sxs-lookup"><span data-stu-id="51a01-119">In the Limit field, enter the amount negotiated with the bank.</span></span>
14. <span data-ttu-id="51a01-120">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="51a01-120">Click Save.</span></span>
15. <span data-ttu-id="51a01-121">Laiendage jaotist Garantiikiri.</span><span class="sxs-lookup"><span data-stu-id="51a01-121">Toggle the expansion of the Letter of guarantee section.</span></span>
16. <span data-ttu-id="51a01-122">Valige suvand väljal Arvutusmeetod.</span><span class="sxs-lookup"><span data-stu-id="51a01-122">In the Calculation method field, select an option.</span></span>
    * <span data-ttu-id="51a01-123">Sisestage suvandi Sularaha marginaal, Väljaandmise komisjonitasu, Laiendi komisjonitasu, Väärtuse komisjonitasu suurendamine või Väärtuse komisjonitasu vähendamine puhul vastavalt arvutusmeetod ja protsendi üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="51a01-123">Enter the calculation method and percentage details for the Cash margin, Issuance commission, Extension commission, Increase value commission, or Decrease value commission, as appropriate.</span></span>   
17. <span data-ttu-id="51a01-124">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="51a01-124">Click Save.</span></span>

## <a name="extend-bank-facility-agreement"></a><span data-ttu-id="51a01-125">Laiendage panga süsteemiteenuse lepet</span><span class="sxs-lookup"><span data-stu-id="51a01-125">Extend bank facility agreement</span></span>
1. <span data-ttu-id="51a01-126">Rippdialoogi avamiseks klõpsake Laienda.</span><span class="sxs-lookup"><span data-stu-id="51a01-126">Click Extend to open the drop dialog.</span></span>
2. <span data-ttu-id="51a01-127">Sisestage väärtus väljale Uus leppe number.</span><span class="sxs-lookup"><span data-stu-id="51a01-127">In the New agreement number field, type a value.</span></span>
3. <span data-ttu-id="51a01-128">Sisestage väljale Lõppkuupäev kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="51a01-128">In the End date field, enter a date and time.</span></span>
4. <span data-ttu-id="51a01-129">Klõpsake Laienda.</span><span class="sxs-lookup"><span data-stu-id="51a01-129">Click Extend.</span></span>
5. <span data-ttu-id="51a01-130">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="51a01-130">Click Save.</span></span>
6. <span data-ttu-id="51a01-131">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="51a01-131">Close the page.</span></span>


