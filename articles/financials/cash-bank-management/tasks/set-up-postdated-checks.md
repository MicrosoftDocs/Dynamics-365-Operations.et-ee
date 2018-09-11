--- 
title: "Hilisema kuupäevaga tšekkide seadistamine"
description: "Selles teemas selgitatakse, kuidas määrata, kas sisestada hilisema kuupäevaga dateeritud tšekkidele töölehe sisestused ja milliseid sisestamise töölehti kliiringukirjete ja hankija maksete puhul kasutada."
author: kweekley
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankParameters, VendPaymMode, CustPaymMode
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 9cf1f6cc29f023977642380ee2583d4f07c53138
ms.contentlocale: et-ee
ms.lasthandoff: 09/11/2018

---
# <a name="set-up-postdated-checks"></a><span data-ttu-id="e4013-103">Hilisema kuupäevaga tšekkide seadistamine</span><span class="sxs-lookup"><span data-stu-id="e4013-103">Set up postdated checks</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e4013-104">Selles teemas selgitatakse, kuidas määrata, kas sisestada hilisema kuupäevaga dateeritud tšekkidele töölehe sisestused ja milliseid sisestamise töölehti kliiringukirjete ja hankija maksete puhul kasutada.</span><span class="sxs-lookup"><span data-stu-id="e4013-104">This topic explains how to specify whether to post journal entries for postdated checks and which posting journals to use for clearing entries and vendor payments.</span></span> <span data-ttu-id="e4013-105">Samuti saate määrata kliiringukontod väljastatud tšekkidele, vastuvõetud tšekkidele ja kinnipeetavatele maksudele.</span><span class="sxs-lookup"><span data-stu-id="e4013-105">You can also specify clearing accounts for issued checks, received checks, and withholding tax.</span></span> <span data-ttu-id="e4013-106">Hilisema kuupäevaga dateeritud tšekid, mis väljastatakse tulevasel kuupäeval maksete tegemiseks ja vastuvõtmiseks.</span><span class="sxs-lookup"><span data-stu-id="e4013-106">Postdated checks that are issued to make and receive payments on a future date.</span></span> <span data-ttu-id="e4013-107">Saate määrata, kas tšekk peab kajastuma raamatupidamises enne selle lõpptähtaega.</span><span class="sxs-lookup"><span data-stu-id="e4013-107">You can specify whether the check must be reflected in the accounting books before its maturity date.</span></span>



<span data-ttu-id="e4013-108">Selle protseduuri roll on Kassiir.</span><span class="sxs-lookup"><span data-stu-id="e4013-108">The role of this procedure is Treasurer.</span></span> <span data-ttu-id="e4013-109">See protsess kasutab demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="e4013-109">This procedure uses the USMF demo company.</span></span>


## <a name="set-up-postdated-checks"></a><span data-ttu-id="e4013-110">Hilisema kuupäevaga tšekkide seadistamine</span><span class="sxs-lookup"><span data-stu-id="e4013-110">Set up postdated checks</span></span>
1. <span data-ttu-id="e4013-111">Minge jaotisse Sularaha- ja pangahaldus > Seadistus > Sularaha- ja pangahalduse parameetrid.</span><span class="sxs-lookup"><span data-stu-id="e4013-111">Go to Cash and bank management > Setup > Cash and bank management parameters.</span></span>
2. <span data-ttu-id="e4013-112">Klõpsake vahekaarti Hilisema kuupäevaga dateeritud tšekid.</span><span class="sxs-lookup"><span data-stu-id="e4013-112">Click the Postdated checks tab.</span></span>
3. <span data-ttu-id="e4013-113">Märkige või tühjendage ruut Luba hilisema kuupäevaga dateeritud tšekid.</span><span class="sxs-lookup"><span data-stu-id="e4013-113">Select or clear the Enable postdated checks check box.</span></span>
4. <span data-ttu-id="e4013-114">Märkige või tühjendage ruut Sisesta töölehe kirjed hilisema kuupäevaga dateeritud tšekkide jaoks.</span><span class="sxs-lookup"><span data-stu-id="e4013-114">Select or clear the Post journal entries for postdated checks check box.</span></span>
5. <span data-ttu-id="e4013-115">Määrake väljal Kliiringukonto väljastatud tšekkide jaoks soovitud väärtused.</span><span class="sxs-lookup"><span data-stu-id="e4013-115">In the Clearing account for issued checks field, specify the desired values.</span></span>
6. <span data-ttu-id="e4013-116">Määrake väljal Kliiringukonto vastuvõetud tšekkide jaoks soovitud väärtused.</span><span class="sxs-lookup"><span data-stu-id="e4013-116">In the Clearing account for received checks field, specify the desired values.</span></span>
7. <span data-ttu-id="e4013-117">Sisestage väärtus väljale Pearaamat kliiringukirjete jaoks.</span><span class="sxs-lookup"><span data-stu-id="e4013-117">In the General journal for clearing entries field, type a value.</span></span>
8. <span data-ttu-id="e4013-118">Sisestage väärtus väljale Kanna hilisema kuupäevaga dateeritud tšekid üle selle hankija maksetöölehele.</span><span class="sxs-lookup"><span data-stu-id="e4013-118">In the Transfer postdated checks to this vendor payment journal field, type a value.</span></span>
9. <span data-ttu-id="e4013-119">Määrake väljal Kinnipeetava maksu kliiringukonto soovitud väärtused.</span><span class="sxs-lookup"><span data-stu-id="e4013-119">In the Withholding tax clearing account field, specify the desired values.</span></span>
10. <span data-ttu-id="e4013-120">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="e4013-120">Click Save.</span></span>
11. <span data-ttu-id="e4013-121">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e4013-121">Close the page.</span></span>
12. <span data-ttu-id="e4013-122">Avage Ostureskontro > Makse seadistus > Makseviisid.</span><span class="sxs-lookup"><span data-stu-id="e4013-122">Go to Accounts payable > Payment setup > Methods of payment.</span></span>
13. <span data-ttu-id="e4013-123">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e4013-123">Click New.</span></span>
14. <span data-ttu-id="e4013-124">Sisestage väärtus väljale Makseviis.</span><span class="sxs-lookup"><span data-stu-id="e4013-124">In the Method of payment field, type a value.</span></span>
15. <span data-ttu-id="e4013-125">Märkige ruut Hilisema kuupäevaga dateeritud tšekkide kliiringsisestus näitamaks, et tšeki summa sisestatakse kliiringukontole.</span><span class="sxs-lookup"><span data-stu-id="e4013-125">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
16. <span data-ttu-id="e4013-126">Valige väljalt Konto tüüp suvand Pank.</span><span class="sxs-lookup"><span data-stu-id="e4013-126">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="e4013-127">Maksemeetodi vastaskonto on pank.</span><span class="sxs-lookup"><span data-stu-id="e4013-127">The offset account of the payment method will be a bank.</span></span>  
17. <span data-ttu-id="e4013-128">Määrake väljal Maksekonto soovitud väärtused.</span><span class="sxs-lookup"><span data-stu-id="e4013-128">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="e4013-129">Valige pangakonto, mida kasutatakse arvesumma mahaarvamiseks.</span><span class="sxs-lookup"><span data-stu-id="e4013-129">Select the bank account that is used to deduct the invoice amount.</span></span>  
18. <span data-ttu-id="e4013-130">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e4013-130">Close the page.</span></span>
19. <span data-ttu-id="e4013-131">Minge jaotisse Müügireskontro > Maksete seadistus > Makseviisid.</span><span class="sxs-lookup"><span data-stu-id="e4013-131">Go to Accounts receivable > Payment setup > Methods of payment</span></span>
20. <span data-ttu-id="e4013-132">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e4013-132">Click New.</span></span>
21. <span data-ttu-id="e4013-133">Sisestage väärtus väljale Makseviis.</span><span class="sxs-lookup"><span data-stu-id="e4013-133">In the Method of payment field, type a value.</span></span>
22. <span data-ttu-id="e4013-134">Märkige ruut Hilisema kuupäevaga dateeritud tšekkide kliiringsisestus näitamaks, et tšeki summa sisestatakse kliiringukontole.</span><span class="sxs-lookup"><span data-stu-id="e4013-134">Select the Postdated check clearing posting option to indicate that the check amount is posted to a clearing account.</span></span>
23. <span data-ttu-id="e4013-135">Valige väljalt Konto tüüp suvand Pank.</span><span class="sxs-lookup"><span data-stu-id="e4013-135">In the Account type field, select 'Bank'.</span></span>
    * <span data-ttu-id="e4013-136">Maksemeetodi vastaskonto on pank.</span><span class="sxs-lookup"><span data-stu-id="e4013-136">The offset account of the payment method will be a bank.</span></span>  
24. <span data-ttu-id="e4013-137">Määrake väljal Maksekonto soovitud väärtused.</span><span class="sxs-lookup"><span data-stu-id="e4013-137">In the Payment account field, specify the desired values.</span></span>
    * <span data-ttu-id="e4013-138">Valige pangakonto, mida kasutatakse arvesumma mahaarvamiseks.</span><span class="sxs-lookup"><span data-stu-id="e4013-138">Select the bank account that is used to deduct the invoice amount.</span></span>  
25. <span data-ttu-id="e4013-139">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e4013-139">Close the page.</span></span>


