---
title: "Tükeldatud perioodid perioodilistes töölehtedes"
description: "Perioodilisi töölehti nimetatakse mõnikord korduvtöölehtedeks, kuna suurus, tekst ja muu teave kordub iga kord, kui tööleht sisestatakse. Töölehe loomisel saate määrata perioodi kordumise intervalli, näiteks päeva või kuu. Saate määrata ka perioodide arvu, millal tööleht postitatakse."
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 261354
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: v-elgolu
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 73ccfc906e8d7a91e7bae5ae21d9ddad9d58f109
ms.contentlocale: et-ee
ms.lasthandoff: 11/03/2017

---

# <a name="split-periods-in-periodic-journals"></a><span data-ttu-id="b8a9e-105">Tükeldatud perioodid perioodilistes töölehtedes</span><span class="sxs-lookup"><span data-stu-id="b8a9e-105">Split periods in periodic journals</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="b8a9e-106">Perioodilisi töölehti nimetatakse mõnikord korduvtöölehtedeks, kuna suurus, tekst ja muu teave kordub iga kord, kui tööleht sisestatakse.</span><span class="sxs-lookup"><span data-stu-id="b8a9e-106">Periodic journals are sometimes called recurring journals because the amount, text, and other information are repeated each time that the journal is posted.</span></span> <span data-ttu-id="b8a9e-107">Töölehe loomisel saate määrata perioodi kordumise intervalli, näiteks päeva või kuu.</span><span class="sxs-lookup"><span data-stu-id="b8a9e-107">When you create the journal, you specify the period interval for the recurrence, such as days or months.</span></span> <span data-ttu-id="b8a9e-108">Saate määrata ka perioodide arvu, millal tööleht postitatakse.</span><span class="sxs-lookup"><span data-stu-id="b8a9e-108">You also specify the number of periods for which the journal will be posted.</span></span>

<span data-ttu-id="b8a9e-109">Kanderidade korduvaks toomiseks ja sisestamiseks saate kasutada lehte **Perioodilised töölehed**.</span><span class="sxs-lookup"><span data-stu-id="b8a9e-109">To repeatedly retrieve and post transaction lines, you can use the **Periodic journals** page.</span></span> <span data-ttu-id="b8a9e-110">Juriidiliste isikute puhul Tšehhi Vabariigis, Eestis, Ungaris, Lätis, Leedus, Poolas ja Venemaal on lehte **Perioodilised töölehed** laiendatud perioodide tükeldamise funktsiooniga.</span><span class="sxs-lookup"><span data-stu-id="b8a9e-110">For legal entities in Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, and Russia, the **Periodic journals** page is extended by the split for periods functionality.</span></span> <span data-ttu-id="b8a9e-111">Lisateavet vaadake jaotisest [Perioodilise töölehe sisestamine](../general-ledger/tasks/post-periodic-journals.md)</span><span class="sxs-lookup"><span data-stu-id="b8a9e-111">For more information, see [Post a periodic journal](../general-ledger/tasks/post-periodic-journals.md)</span></span>

### <a name="example-split-for-periods-in-periodic-journals"></a><span data-ttu-id="b8a9e-112">Näide: perioodide tükeldamine perioodilistes töölehtedes</span><span class="sxs-lookup"><span data-stu-id="b8a9e-112">Example: Split for periods in periodic journals</span></span>

<span data-ttu-id="b8a9e-113">Kindlustusfirma pakub teie organisatsioonile allahindlust terve aasta kindlustuspoliisi ettemaksule.</span><span class="sxs-lookup"><span data-stu-id="b8a9e-113">An insurance company offers your organization a discount for prepaying the insurance policy for an entire year.</span></span> <span data-ttu-id="b8a9e-114">Makse postitatakse põhivara kontole, näiteks ettemakstud kindlustuse kontole.</span><span class="sxs-lookup"><span data-stu-id="b8a9e-114">The payment is posted to an asset account such as prepaid insurance.</span></span> <span data-ttu-id="b8a9e-115">Seejärel amortiseerite kindlustuse aastase kuumaksu, luues perioodilise töölehe, mis sisaldab ettemakstud kindlustuse konto krediiti ja kindlustuse kulukonto deebetit.</span><span class="sxs-lookup"><span data-stu-id="b8a9e-115">You then amortize your monthly insurance expense throughout the year by creating a periodic journal that contains a credit to the prepaid insurance account and a debit to an insurance expense account.</span></span> <span data-ttu-id="b8a9e-116">Sellisel juhul saate kasutada perioodideks tükeldamise funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="b8a9e-116">In this case, you can use the split for periods functionality.</span></span> <span data-ttu-id="b8a9e-117">Klõpsake toimingupaani lehel **Perioodilise töölehe** **read** nuppu **Tükelda perioodideks** ja täitke järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="b8a9e-117">Click the **Split for periods** button on the Action Pane on the **Periodic journal** **lines** page, and then specify the following fields.</span></span>

|                       |                                                                                                                                                                                                             |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8a9e-118">**Väli**</span><span class="sxs-lookup"><span data-stu-id="b8a9e-118">**Field**</span></span>             | <span data-ttu-id="b8a9e-119">**Kirjeldus**</span><span class="sxs-lookup"><span data-stu-id="b8a9e-119">**Description**</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="b8a9e-120">**Alguskuupäev**</span><span class="sxs-lookup"><span data-stu-id="b8a9e-120">**Start date**</span></span>        | <span data-ttu-id="b8a9e-121">Valige esimese perioodilise töölehe rea kuupäev.</span><span class="sxs-lookup"><span data-stu-id="b8a9e-121">Select the date for the first periodic journal line.</span></span>                                                                                                                                                        |
| <span data-ttu-id="b8a9e-122">**Perioodide arv**</span><span class="sxs-lookup"><span data-stu-id="b8a9e-122">**Number of periods**</span></span> | <span data-ttu-id="b8a9e-123">Sisestage perioodide arv, millega töölehe ridade arv jagada.</span><span class="sxs-lookup"><span data-stu-id="b8a9e-123">Enter the number of periods across which to split the journal line.</span></span> <span data-ttu-id="b8a9e-124">See väärtus määratleb, mitu uut kannet luuakse.</span><span class="sxs-lookup"><span data-stu-id="b8a9e-124">This value determines how many new transactions are generated.</span></span> <span data-ttu-id="b8a9e-125">Kande summa jagatakse ühtlaselt uute kannetega.</span><span class="sxs-lookup"><span data-stu-id="b8a9e-125">The transaction amount is distributed evenly among the new transactions.</span></span> |
| <span data-ttu-id="b8a9e-126">**Ühik**</span><span class="sxs-lookup"><span data-stu-id="b8a9e-126">**Unit**</span></span>              | <span data-ttu-id="b8a9e-127">Valige perioodile mõõtühik.</span><span class="sxs-lookup"><span data-stu-id="b8a9e-127">Select the unit of measure for the period.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="b8a9e-128">**Perioodi intervall**</span><span class="sxs-lookup"><span data-stu-id="b8a9e-128">**Period interval**</span></span>   | <span data-ttu-id="b8a9e-129">Määrake sisestusperioodide vaheline intervall.</span><span class="sxs-lookup"><span data-stu-id="b8a9e-129">Determine an interval between posting periods.</span></span>                                                                                                                                                              |

<span data-ttu-id="b8a9e-130">Näiteks kvartalipõhiste sisestuste loomiseks sisestage väljale **Perioodide arv** väärtus **4**, valige väljal **Ühik** säte **Kuud** ja sisestage väljale **Perioodi intervall** väärtus **3**.</span><span class="sxs-lookup"><span data-stu-id="b8a9e-130">For example, to generate quarterly postings, enter **4** in the **Number of periods** field, select **Months** in the **Unit** field, and enter **3** in the **Period interval** field.</span></span> <span data-ttu-id="b8a9e-131">Süsteem loob neli töölehe rida, iga rida on üks neljandik sisestatud töölehe rea summast iga 3 kuu järel.</span><span class="sxs-lookup"><span data-stu-id="b8a9e-131">The system generates four journal lines, each for one fourth of the journal line amount that you entered, at 3-month intervals.</span></span> <span data-ttu-id="b8a9e-132">Sarnane funktsioon on saadaval ka päevaraamatu kohta.</span><span class="sxs-lookup"><span data-stu-id="b8a9e-132">Similar functionality is also available for the general journal.</span></span> <span data-ttu-id="b8a9e-133">Päevaraamatu ridade vaatamisel valige **Perioodi tööraamat** &gt; **Salvesta tööraamat**.</span><span class="sxs-lookup"><span data-stu-id="b8a9e-133">When viewing general journal lines, select **Period journal** &gt; **Save journal**.</span></span>




