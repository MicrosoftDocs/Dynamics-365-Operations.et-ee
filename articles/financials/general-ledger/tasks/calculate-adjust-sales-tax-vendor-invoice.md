--- 
title: "Käibemaksu arvutamine ja korrigeerimine hankija arvel"
description: "Kui algne lähtedokument kuvab erinevad arvutatud maksusummade, saate neid summasid enne sisestamist korrigeerida."
author: twheeloc
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTable, LedgerJournalTransVendInvoice, VendTableLookup, TaxTmpWorkTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 2c120eeed18a1ae05bcdda1d1ae285232d68c6ed
ms.contentlocale: et-ee
ms.lasthandoff: 09/11/2018

---
# <a name="calculate-and-adjust-sales-tax-on-a-vendor-invoice"></a><span data-ttu-id="14870-103">Käibemaksu arvutamine ja korrigeerimine hankija arvel</span><span class="sxs-lookup"><span data-stu-id="14870-103">Calculate and adjust sales tax on a vendor invoice</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="14870-104">Kui algne lähtedokument kuvab erinevad arvutatud maksusummade, saate neid summasid enne sisestamist korrigeerida.</span><span class="sxs-lookup"><span data-stu-id="14870-104">If the original source document displays different tax amounts as calculated, you can adjust those amounts before posting.</span></span> <span data-ttu-id="14870-105">See ülesanne kasutab demoettevõtte DEMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="14870-105">This task uses the DEMF demo company.</span></span>

1. <span data-ttu-id="14870-106">Avage Ostureskontro > Arved > Arve tööleht.</span><span class="sxs-lookup"><span data-stu-id="14870-106">Go to Accounts payable > Invoices > Invoice journal.</span></span>
2. <span data-ttu-id="14870-107">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="14870-107">Click New.</span></span>
3. <span data-ttu-id="14870-108">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="14870-108">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="14870-109">Klõpsake väljal Nimi otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="14870-109">In the Name field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="14870-110">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="14870-110">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="14870-111">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="14870-111">Click Lines.</span></span>
7. <span data-ttu-id="14870-112">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="14870-112">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="14870-113">Täpsustage soovitud väärtusi väljal Konto.</span><span class="sxs-lookup"><span data-stu-id="14870-113">In the Account field, specify the desired values.</span></span>
9. <span data-ttu-id="14870-114">Sisestage väärtus väljale Arve.</span><span class="sxs-lookup"><span data-stu-id="14870-114">In the Invoice field, type a value.</span></span>
10. <span data-ttu-id="14870-115">Sisestage arv väljale Kreedit.</span><span class="sxs-lookup"><span data-stu-id="14870-115">In the Credit field, enter a number.</span></span>
11. <span data-ttu-id="14870-116">Täpsustage soovitud väärtusi väljal Vastaskonto.</span><span class="sxs-lookup"><span data-stu-id="14870-116">In the Offset account field, specify the desired values.</span></span>
12. <span data-ttu-id="14870-117">Klõpsake suvandit Käibemaks.</span><span class="sxs-lookup"><span data-stu-id="14870-117">Click Sales tax.</span></span>
13. <span data-ttu-id="14870-118">Sisestage number väljale Tegeliku käibemaksu kogusumma.</span><span class="sxs-lookup"><span data-stu-id="14870-118">In the Total actual sales tax amount field, enter a number.</span></span>
14. <span data-ttu-id="14870-119">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="14870-119">Click OK.</span></span>
15. <span data-ttu-id="14870-120">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="14870-120">Click Save.</span></span>
16. <span data-ttu-id="14870-121">Klõpsake suvandit Käibemaks.</span><span class="sxs-lookup"><span data-stu-id="14870-121">Click Sales tax.</span></span>
17. <span data-ttu-id="14870-122">Vahekaardil Korrigeerimine saab korrigeerida käibemaksusummat käibemaksukoodi kohta.</span><span class="sxs-lookup"><span data-stu-id="14870-122">On the Adjustment tab, the sales tax amounts can be adjusted per sales tax code.</span></span>
18. <span data-ttu-id="14870-123">Klõpsake suvandit Tegeliku väärtuse lähtestamine arvutatud summadest.</span><span class="sxs-lookup"><span data-stu-id="14870-123">Click Reset actual from calculated amounts.</span></span>
19. <span data-ttu-id="14870-124">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="14870-124">Click OK.</span></span>
20. <span data-ttu-id="14870-125">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="14870-125">Click Save.</span></span>


