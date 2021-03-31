---
title: Akreditiivi jaoks panga süsteemiteenuse lepingu loomine
description: Selles ülesandes näitlikustatakse, kuidas luua akreditiivi töötlemiseks panga süsteemiteenuse lepet.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankDocumentFacilityAgreement, BankAccountTableLookUp, BankDocumentFacilityAgreementExtension, DefaultDashboard
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 40d13e996b08efecb19be961c592230567656a4d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225485"
---
# <a name="create-a-bank-facility-agreement-for-a-letter-of-credit"></a><span data-ttu-id="aa9c5-103">Akreditiivi jaoks panga süsteemiteenuse lepingu loomine</span><span class="sxs-lookup"><span data-stu-id="aa9c5-103">Create a bank facility agreement for a letter of credit</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aa9c5-104">Selles ülesandes näitlikustatakse, kuidas luua akreditiivi töötlemiseks panga süsteemiteenuse lepet.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-104">This task walks through the creating a Bank facility agreement to process a Letter of credit.</span></span> <span data-ttu-id="aa9c5-105">Enne ülesande juurde asumist on soovitatav seadistada panga süsteemiteenused ja sisestusreeglid.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-105">You will want to set up bank facilities and posting profiles before this task.</span></span>  <span data-ttu-id="aa9c5-106">Selles ülesandes kasutatakse demoettevõtet USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-106">This task uses the demo company 'USMF'.</span></span>  


## <a name="create-bank-facility-agreement"></a><span data-ttu-id="aa9c5-107">Panga süsteemiteenuse leppe loomine</span><span class="sxs-lookup"><span data-stu-id="aa9c5-107">Create Bank facility agreement</span></span>
1. <span data-ttu-id="aa9c5-108">Avage Sularaha- ja pangahaldus > Akreditiivid > Panga süsteemiteenuse lepped.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-108">Go to Cash and bank management > Letters of credit > Bank facility agreements.</span></span>
2. <span data-ttu-id="aa9c5-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-109">Click New.</span></span>
3. <span data-ttu-id="aa9c5-110">Sisestage väljale Lepingu number lepingu number vastavalt pangaga sõlmitud lepingule.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-110">In the Agreement number field, enter the agreement number according to the agreement with the bank.</span></span>
4. <span data-ttu-id="aa9c5-111">Sisestage väljale Pangakonto kontonumber väljastavas pangas.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-111">In the Bank account field, enter the account number at the issuing bank.</span></span>
5. <span data-ttu-id="aa9c5-112">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="aa9c5-113">Sisestage väljale Alguskuupäev kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-113">In the Start date field, enter a date and time.</span></span>
7. <span data-ttu-id="aa9c5-114">Sisestage väljale Lõppkuupäev kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-114">In the End date field, enter a date and time.</span></span>
8. <span data-ttu-id="aa9c5-115">Laiendage või ahendage jaotist Üldine.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-115">Expand or collapse the General section.</span></span>
9. <span data-ttu-id="aa9c5-116">Klõpsake käsku Lisa rida.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-116">Click Add line.</span></span>
10. <span data-ttu-id="aa9c5-117">Klõpsake väljal Süsteemiteenuse tüüp otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-117">In the Facility type field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="aa9c5-118">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-118">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="aa9c5-119">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-119">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="aa9c5-120">Sisestage väljale Limiit pangaga kokku lepitud süsteemiteenuse summa.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-120">In the Limit field, enter the facility amount that was negotiated with the bank.</span></span>
14. <span data-ttu-id="aa9c5-121">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-121">Click Save.</span></span>
15. <span data-ttu-id="aa9c5-122">Rippdialoogi avamiseks klõpsake Laienda.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-122">Click Extend to open the drop dialog.</span></span>
16. <span data-ttu-id="aa9c5-123">Sisestage väärtus väljale Uus leppe number.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-123">In the New agreement number field, type a value.</span></span>
17. <span data-ttu-id="aa9c5-124">Sisestage väljale Lõppkuupäev kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-124">In the End date field, enter a date and time.</span></span>
18. <span data-ttu-id="aa9c5-125">Klõpsake Laienda.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-125">Click Extend.</span></span>
19. <span data-ttu-id="aa9c5-126">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="aa9c5-126">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]