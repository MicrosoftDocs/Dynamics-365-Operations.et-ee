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
ms.openlocfilehash: cb2fe6bfebcc0cc302d623a34fd994a57cbea1c8
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177369"
---
# <a name="create-a-bank-facility-agreement-for-the-letter-of-guarantee"></a><span data-ttu-id="b1155-103">Garantiikirja jaoks panga süsteemiteenuse lepingu loomine</span><span class="sxs-lookup"><span data-stu-id="b1155-103">Create a bank facility agreement for the letter of guarantee</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b1155-104">See ülesanne loob panga süsteemiteenuse leppe garantiikirja töötlemiseks.</span><span class="sxs-lookup"><span data-stu-id="b1155-104">This task creates a bank facility agreement to process a letter of guarantee.</span></span> <span data-ttu-id="b1155-105">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="b1155-105">This task uses the USMF demo company.</span></span> 


## <a name="create-bank-facility-agreement"></a><span data-ttu-id="b1155-106">Panga süsteemiteenuse leppe loomine</span><span class="sxs-lookup"><span data-stu-id="b1155-106">Create Bank facility agreement</span></span>
1. <span data-ttu-id="b1155-107">Minge jaotisse Sularaha- ja pangahaldus > Garantiikirjad > Panga süsteemiteenuse lepped.</span><span class="sxs-lookup"><span data-stu-id="b1155-107">Go to Cash and bank management > Letters of guarantee > Bank facility agreements.</span></span>
2. <span data-ttu-id="b1155-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="b1155-108">Click New.</span></span>
3. <span data-ttu-id="b1155-109">Sisestage väljale Leppe number kande pangaleppe number.</span><span class="sxs-lookup"><span data-stu-id="b1155-109">In the Agreement number field, enter the bank agreement number for the transaction.</span></span>
4. <span data-ttu-id="b1155-110">Valige väljal Pangakonto selle pangakonto number, mille jaoks garantiikiri on avatud.</span><span class="sxs-lookup"><span data-stu-id="b1155-110">In the Bank account field, select the bank account number for which the letter of guarantee is open.</span></span> 
5. <span data-ttu-id="b1155-111">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="b1155-111">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="b1155-112">Sisestage väljale Alguskuupäev kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="b1155-112">In the Start date field, enter a date and time.</span></span>
7. <span data-ttu-id="b1155-113">Sisestage väljale Lõppkuupäev kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="b1155-113">In the End date field, enter a date and time.</span></span>
8. <span data-ttu-id="b1155-114">Lülitage jaotise Üldine laiendamist.</span><span class="sxs-lookup"><span data-stu-id="b1155-114">Toggle the expansion of the General section.</span></span>
9. <span data-ttu-id="b1155-115">Klõpsake käsku Lisa rida.</span><span class="sxs-lookup"><span data-stu-id="b1155-115">Click Add line.</span></span>
10. <span data-ttu-id="b1155-116">Klõpsake väljal Süsteemiteenuse tüüp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="b1155-116">In the Facility type field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="b1155-117">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="b1155-117">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="b1155-118">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="b1155-118">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="b1155-119">Sisestage väljale Piirang pangaga kokkulepitud summa.</span><span class="sxs-lookup"><span data-stu-id="b1155-119">In the Limit field, enter the amount negotiated with the bank.</span></span>
14. <span data-ttu-id="b1155-120">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="b1155-120">Click Save.</span></span>
15. <span data-ttu-id="b1155-121">Laiendage jaotist Garantiikiri.</span><span class="sxs-lookup"><span data-stu-id="b1155-121">Toggle the expansion of the Letter of guarantee section.</span></span>
16. <span data-ttu-id="b1155-122">Valige suvand väljal Arvutusmeetod.</span><span class="sxs-lookup"><span data-stu-id="b1155-122">In the Calculation method field, select an option.</span></span>
    * <span data-ttu-id="b1155-123">Sisestage suvandi Sularaha marginaal, Väljaandmise komisjonitasu, Laiendi komisjonitasu, Väärtuse komisjonitasu suurendamine või Väärtuse komisjonitasu vähendamine puhul vastavalt arvutusmeetod ja protsendi üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="b1155-123">Enter the calculation method and percentage details for the Cash margin, Issuance commission, Extension commission, Increase value commission, or Decrease value commission, as appropriate.</span></span>   
17. <span data-ttu-id="b1155-124">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="b1155-124">Click Save.</span></span>

## <a name="extend-bank-facility-agreement"></a><span data-ttu-id="b1155-125">Laiendage panga süsteemiteenuse lepet</span><span class="sxs-lookup"><span data-stu-id="b1155-125">Extend bank facility agreement</span></span>
1. <span data-ttu-id="b1155-126">Rippdialoogi avamiseks klõpsake Laienda.</span><span class="sxs-lookup"><span data-stu-id="b1155-126">Click Extend to open the drop dialog.</span></span>
2. <span data-ttu-id="b1155-127">Sisestage väärtus väljale Uus leppe number.</span><span class="sxs-lookup"><span data-stu-id="b1155-127">In the New agreement number field, type a value.</span></span>
3. <span data-ttu-id="b1155-128">Sisestage väljale Lõppkuupäev kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="b1155-128">In the End date field, enter a date and time.</span></span>
4. <span data-ttu-id="b1155-129">Klõpsake Laienda.</span><span class="sxs-lookup"><span data-stu-id="b1155-129">Click Extend.</span></span>
5. <span data-ttu-id="b1155-130">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="b1155-130">Click Save.</span></span>
6. <span data-ttu-id="b1155-131">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b1155-131">Close the page.</span></span>

