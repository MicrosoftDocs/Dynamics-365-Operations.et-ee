---
title: Garantiikirja jaoks panga süsteemiteenuse lepingu loomine
description: See ülesanne loob panga süsteemiteenuse leppe garantiikirja töötlemiseks.
author: ShylaThompson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 106ce3e9e6263802f9b28e0b0c95ac554e38f67d
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141691"
---
# <a name="create-a-bank-facility-agreement-for-the-letter-of-guarantee"></a><span data-ttu-id="33a9b-103">Garantiikirja jaoks panga süsteemiteenuse lepingu loomine</span><span class="sxs-lookup"><span data-stu-id="33a9b-103">Create a bank facility agreement for the letter of guarantee</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="33a9b-104">See ülesanne loob panga süsteemiteenuse leppe garantiikirja töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="33a9b-104">This task creates a bank facility agreement to process a letter of guarantee.</span></span> <span data-ttu-id="33a9b-105">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="33a9b-105">This task uses the USMF demo company.</span></span> 


## <a name="create-bank-facility-agreement"></a><span data-ttu-id="33a9b-106">Panga süsteemiteenuse leppe loomine</span><span class="sxs-lookup"><span data-stu-id="33a9b-106">Create Bank facility agreement</span></span>
1. <span data-ttu-id="33a9b-107">Minge jaotisse Sularaha- ja pangahaldus > Garantiikirjad > Panga süsteemiteenuse lepped.</span><span class="sxs-lookup"><span data-stu-id="33a9b-107">Go to Cash and bank management > Letters of guarantee > Bank facility agreements.</span></span>
2. <span data-ttu-id="33a9b-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="33a9b-108">Click New.</span></span>
3. <span data-ttu-id="33a9b-109">Sisestage väljale Leppe number kande pangaleppe number.</span><span class="sxs-lookup"><span data-stu-id="33a9b-109">In the Agreement number field, enter the bank agreement number for the transaction.</span></span>
4. <span data-ttu-id="33a9b-110">Valige väljal Pangakonto selle pangakonto number, mille jaoks garantiikiri on avatud.</span><span class="sxs-lookup"><span data-stu-id="33a9b-110">In the Bank account field, select the bank account number for which the letter of guarantee is open.</span></span> 
5. <span data-ttu-id="33a9b-111">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="33a9b-111">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="33a9b-112">Sisestage väljale Alguskuupäev kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="33a9b-112">In the Start date field, enter a date and time.</span></span>
7. <span data-ttu-id="33a9b-113">Sisestage väljale Lõppkuupäev kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="33a9b-113">In the End date field, enter a date and time.</span></span>
8. <span data-ttu-id="33a9b-114">Lülitage jaotise Üldine laiendamist.</span><span class="sxs-lookup"><span data-stu-id="33a9b-114">Toggle the expansion of the General section.</span></span>
9. <span data-ttu-id="33a9b-115">Klõpsake käsku Lisa rida.</span><span class="sxs-lookup"><span data-stu-id="33a9b-115">Click Add line.</span></span>
10. <span data-ttu-id="33a9b-116">Klõpsake väljal Süsteemiteenuse tüüp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="33a9b-116">In the Facility type field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="33a9b-117">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="33a9b-117">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="33a9b-118">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="33a9b-118">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="33a9b-119">Sisestage väljale Piirang pangaga kokkulepitud summa.</span><span class="sxs-lookup"><span data-stu-id="33a9b-119">In the Limit field, enter the amount negotiated with the bank.</span></span>
14. <span data-ttu-id="33a9b-120">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="33a9b-120">Click Save.</span></span>
15. <span data-ttu-id="33a9b-121">Laiendage jaotist Garantiikiri.</span><span class="sxs-lookup"><span data-stu-id="33a9b-121">Toggle the expansion of the Letter of guarantee section.</span></span>
16. <span data-ttu-id="33a9b-122">Valige suvand väljal Arvutusmeetod.</span><span class="sxs-lookup"><span data-stu-id="33a9b-122">In the Calculation method field, select an option.</span></span>
    * <span data-ttu-id="33a9b-123">Sisestage suvandi Sularaha marginaal, Väljaandmise komisjonitasu, Laiendi komisjonitasu, Väärtuse komisjonitasu suurendamine või Väärtuse komisjonitasu vähendamine puhul vastavalt arvutusmeetod ja protsendi üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="33a9b-123">Enter the calculation method and percentage details for the Cash margin, Issuance commission, Extension commission, Increase value commission, or Decrease value commission, as appropriate.</span></span>   
17. <span data-ttu-id="33a9b-124">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="33a9b-124">Click Save.</span></span>

## <a name="extend-bank-facility-agreement"></a><span data-ttu-id="33a9b-125">Laiendage panga süsteemiteenuse lepet</span><span class="sxs-lookup"><span data-stu-id="33a9b-125">Extend bank facility agreement</span></span>
1. <span data-ttu-id="33a9b-126">Rippdialoogi avamiseks klõpsake Laienda.</span><span class="sxs-lookup"><span data-stu-id="33a9b-126">Click Extend to open the drop dialog.</span></span>
2. <span data-ttu-id="33a9b-127">Sisestage väärtus väljale Uus leppe number.</span><span class="sxs-lookup"><span data-stu-id="33a9b-127">In the New agreement number field, type a value.</span></span>
3. <span data-ttu-id="33a9b-128">Sisestage väljale Lõppkuupäev kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="33a9b-128">In the End date field, enter a date and time.</span></span>
4. <span data-ttu-id="33a9b-129">Klõpsake Laienda.</span><span class="sxs-lookup"><span data-stu-id="33a9b-129">Click Extend.</span></span>
5. <span data-ttu-id="33a9b-130">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="33a9b-130">Click Save.</span></span>
6. <span data-ttu-id="33a9b-131">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="33a9b-131">Close the page.</span></span>

