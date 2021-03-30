---
title: Perioodide tükeldamine perioodilistes töölehtedes
description: Selles teemas antakse Tšehhi Vabariigi, Eesti, Ungari, Läti, Leedu, Poola ja Venemaa juriidilistele isikutele teavet perioodide tükeldamise kohta perioodilistes töölehtedes või korduvates töölehtedes.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable
audience: Application User
ms.reviewer: kfend
ms.custom: 261354
ms.search.region: Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland
ms.author: kfend
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 976175671ec5ee36f80ba2b2c787a67c18a9b769
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5236302"
---
# <a name="split-periods-in-periodic-journals"></a><span data-ttu-id="791ac-103">Perioodide tükeldamine perioodilistes töölehtedes</span><span class="sxs-lookup"><span data-stu-id="791ac-103">Split periods in periodic journals</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="791ac-104">Perioodilisi töölehti nimetatakse mõnikord korduvtöölehtedeks, kuna suurus, tekst ja muu teave kordub iga kord, kui tööleht sisestatakse.</span><span class="sxs-lookup"><span data-stu-id="791ac-104">Periodic journals are sometimes called recurring journals because the amount, text, and other information are repeated each time that the journal is posted.</span></span> <span data-ttu-id="791ac-105">Töölehe loomisel saate määrata perioodi kordumise intervalli, näiteks päeva või kuu.</span><span class="sxs-lookup"><span data-stu-id="791ac-105">When you create the journal, you specify the period interval for the recurrence, such as days or months.</span></span> <span data-ttu-id="791ac-106">Saate määrata ka perioodide arvu, millal tööleht postitatakse.</span><span class="sxs-lookup"><span data-stu-id="791ac-106">You also specify the number of periods for which the journal will be posted.</span></span>

<span data-ttu-id="791ac-107">Kanderidade korduvaks toomiseks ja sisestamiseks saate kasutada lehte **Perioodilised töölehed**.</span><span class="sxs-lookup"><span data-stu-id="791ac-107">To repeatedly retrieve and post transaction lines, you can use the **Periodic journals** page.</span></span> <span data-ttu-id="791ac-108">Juriidiliste isikute puhul Tšehhi Vabariigis, Eestis, Ungaris, Lätis, Leedus, Poolas ja Venemaal on lehte **Perioodilised töölehed** laiendatud perioodide tükeldamise funktsiooniga.</span><span class="sxs-lookup"><span data-stu-id="791ac-108">For legal entities in Czech Republic, Estonia, Hungary, Latvia, Lithuania, Poland, and Russia, the **Periodic journals** page is extended by the split for periods functionality.</span></span> <span data-ttu-id="791ac-109">Lisateabe saamiseks vt [perioodijärgseid aruandeid](../general-ledger/tasks/post-periodic-journals.md)</span><span class="sxs-lookup"><span data-stu-id="791ac-109">For more information, see [Post periodic journals](../general-ledger/tasks/post-periodic-journals.md)</span></span>

### <a name="example-split-for-periods-in-periodic-journals"></a><span data-ttu-id="791ac-110">Näide: perioodide tükeldamine perioodilistes töölehtedes</span><span class="sxs-lookup"><span data-stu-id="791ac-110">Example: Split for periods in periodic journals</span></span>

<span data-ttu-id="791ac-111">Kindlustusfirma pakub teie organisatsioonile allahindlust terve aasta kindlustuspoliisi ettemaksule.</span><span class="sxs-lookup"><span data-stu-id="791ac-111">An insurance company offers your organization a discount for prepaying the insurance policy for an entire year.</span></span> <span data-ttu-id="791ac-112">Makse postitatakse põhivara kontole, näiteks ettemakstud kindlustuse kontole.</span><span class="sxs-lookup"><span data-stu-id="791ac-112">The payment is posted to an asset account such as prepaid insurance.</span></span> <span data-ttu-id="791ac-113">Seejärel amortiseerite kindlustuse aastase kuumaksu, luues perioodilise töölehe, mis sisaldab ettemakstud kindlustuse konto krediiti ja kindlustuse kulukonto deebetit.</span><span class="sxs-lookup"><span data-stu-id="791ac-113">You then amortize your monthly insurance expense throughout the year by creating a periodic journal that contains a credit to the prepaid insurance account and a debit to an insurance expense account.</span></span> <span data-ttu-id="791ac-114">Sellisel juhul saate kasutada perioodideks tükeldamise funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="791ac-114">In this case, you can use the split for periods functionality.</span></span> <span data-ttu-id="791ac-115">Klõpsake toimingupaani lehel **Perioodilise töölehe** **read** nuppu **Tükelda perioodideks** ja täitke järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="791ac-115">Click the **Split for periods** button on the Action Pane on the **Periodic journal** **lines** page, and then specify the following fields.</span></span>


| <span data-ttu-id="791ac-116">Väli</span><span class="sxs-lookup"><span data-stu-id="791ac-116">Field</span></span>            | <span data-ttu-id="791ac-117">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="791ac-117">Description</span></span>                                                                                                                                                                                             |
|-----------------------|---------------------------------------------------------------|
| <span data-ttu-id="791ac-118">**Alguskuupäev**</span><span class="sxs-lookup"><span data-stu-id="791ac-118">**Start date**</span></span>        | <span data-ttu-id="791ac-119">Valige esimese perioodilise töölehe rea kuupäev.</span><span class="sxs-lookup"><span data-stu-id="791ac-119">Select the date for the first periodic journal line.</span></span>                                                                                                                                                        |
| <span data-ttu-id="791ac-120">**Perioodide arv**</span><span class="sxs-lookup"><span data-stu-id="791ac-120">**Number of periods**</span></span> | <span data-ttu-id="791ac-121">Sisestage perioodide arv, millega töölehe ridade arv jagada.</span><span class="sxs-lookup"><span data-stu-id="791ac-121">Enter the number of periods across which to split the journal line.</span></span> <span data-ttu-id="791ac-122">See väärtus määratleb, mitu uut kannet luuakse.</span><span class="sxs-lookup"><span data-stu-id="791ac-122">This value determines how many new transactions are generated.</span></span> <span data-ttu-id="791ac-123">Kande summa jagatakse ühtlaselt uute kannetega.</span><span class="sxs-lookup"><span data-stu-id="791ac-123">The transaction amount is distributed evenly among the new transactions.</span></span> |
| <span data-ttu-id="791ac-124">**Ühik**</span><span class="sxs-lookup"><span data-stu-id="791ac-124">**Unit**</span></span>              | <span data-ttu-id="791ac-125">Valige perioodile mõõtühik.</span><span class="sxs-lookup"><span data-stu-id="791ac-125">Select the unit of measure for the period.</span></span>                                                                                                                                                                  |
| <span data-ttu-id="791ac-126">**Perioodi intervall**</span><span class="sxs-lookup"><span data-stu-id="791ac-126">**Period interval**</span></span>   | <span data-ttu-id="791ac-127">Määrake sisestusperioodide vaheline intervall.</span><span class="sxs-lookup"><span data-stu-id="791ac-127">Determine an interval between posting periods.</span></span>                                                                                                                                                              |

<span data-ttu-id="791ac-128">Näiteks kvartalipõhiste sisestuste loomiseks sisestage väljale **Perioodide arv** väärtus **4**, valige väljal **Ühik** säte **Kuud** ja sisestage väljale **Perioodi intervall** väärtus **3**.</span><span class="sxs-lookup"><span data-stu-id="791ac-128">For example, to generate quarterly postings, enter **4** in the **Number of periods** field, select **Months** in the **Unit** field, and enter **3** in the **Period interval** field.</span></span> <span data-ttu-id="791ac-129">Süsteem loob neli töölehe rida, iga rida on üks neljandik sisestatud töölehe rea summast iga 3 kuu järel.</span><span class="sxs-lookup"><span data-stu-id="791ac-129">The system generates four journal lines, each for one fourth of the journal line amount that you entered, at 3-month intervals.</span></span> <span data-ttu-id="791ac-130">Sarnane funktsioon on saadaval ka päevaraamatu kohta.</span><span class="sxs-lookup"><span data-stu-id="791ac-130">Similar functionality is also available for the general journal.</span></span> <span data-ttu-id="791ac-131">Päevaraamatu ridade vaatamisel valige **Perioodi tööraamat** &gt; **Salvesta tööraamat**.</span><span class="sxs-lookup"><span data-stu-id="791ac-131">When viewing general journal lines, select **Period journal** &gt; **Save journal**.</span></span>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]