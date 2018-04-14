--- 
title: "Hankija hilisema kuupäevaga tšeki registreerimine ja sisestamine"
description: "Saate registreerida hilisema kuupäevaga dateeritud tšeki üksikasjad enne tšeki väljastamist hankijale, kasutades töölehe kannet."
author: kweekley
manager: AnnBe
ms.date: 10/31/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: cd00227ed6d288a4b2041630bc7a604ac94d3c70
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---
# <a name="register-and-post-a-postdated-check-for-a-vendor"></a><span data-ttu-id="1574e-103">Hankija hilisema kuupäevaga tšeki registreerimine ja sisestamine</span><span class="sxs-lookup"><span data-stu-id="1574e-103">Register and post a postdated check for a vendor</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1574e-104">Saate registreerida hilisema kuupäevaga dateeritud tšeki üksikasjad enne tšeki väljastamist hankijale, kasutades töölehe kannet.</span><span class="sxs-lookup"><span data-stu-id="1574e-104">You can register the details of a postdated check before you issue the check to a vendor by using the journal voucher.</span></span> <span data-ttu-id="1574e-105">Saate ka sisestada hilisema kuupäevaga dateeritud tšeki ja luua finantskanded.</span><span class="sxs-lookup"><span data-stu-id="1574e-105">You can also post the postdated check and generate financial transactions.</span></span> <span data-ttu-id="1574e-106">Enne kui saate registreerida ja sisestada kliendilt saadud hilisema kuupäevaga dateeritud tšeki, peate täitma järgmise ülesande.</span><span class="sxs-lookup"><span data-stu-id="1574e-106">Before you register and post a postdated check from a vendor, complete the following task:</span></span> 

<span data-ttu-id="1574e-107">Hilisema kuupäevaga dateeritud tšekkide seadistamine lehel Sularaha- ja pangahaldus.</span><span class="sxs-lookup"><span data-stu-id="1574e-107">Set up postdated checks in the Cash and bank management page.</span></span> 



<span data-ttu-id="1574e-108">Selle ülesandejuhendi roll on Kassiir.</span><span class="sxs-lookup"><span data-stu-id="1574e-108">The role of this task guides is Treasurer.</span></span> <span data-ttu-id="1574e-109">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="1574e-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="1574e-110">Avage Ostureskontro > Maksed > Makse tööleht.</span><span class="sxs-lookup"><span data-stu-id="1574e-110">Go to Accounts payable > Payments > Payment journal</span></span>
2. <span data-ttu-id="1574e-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="1574e-111">Click New.</span></span>
3. <span data-ttu-id="1574e-112">Sisestage väljale Nimi tekst „VendPay”.</span><span class="sxs-lookup"><span data-stu-id="1574e-112">In the Name field, type 'VendPay'.</span></span>
4. <span data-ttu-id="1574e-113">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="1574e-113">Click Lines.</span></span>
5. <span data-ttu-id="1574e-114">Täpsustage soovitud väärtusi väljal Konto.</span><span class="sxs-lookup"><span data-stu-id="1574e-114">In the Account field, specify the desired values.</span></span>
6. <span data-ttu-id="1574e-115">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="1574e-115">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="1574e-116">Sisestage arv väljale Deebet.</span><span class="sxs-lookup"><span data-stu-id="1574e-116">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="1574e-117">Klõpsake väljal Makseviis otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="1574e-117">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="1574e-118">Valige makseviis hilisema kuupäevaga dateeritud tšekile.</span><span class="sxs-lookup"><span data-stu-id="1574e-118">Select the method of payment for the postdated check</span></span>  
9. <span data-ttu-id="1574e-119">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="1574e-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="1574e-120">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="1574e-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="1574e-121">Klõpsake vahekaarti Hilisema kuupäevaga dateeritud tšekid.</span><span class="sxs-lookup"><span data-stu-id="1574e-121">Click the Postdated checks tab.</span></span>
12. <span data-ttu-id="1574e-122">Sisestage väärtus väljale Tšeki number.</span><span class="sxs-lookup"><span data-stu-id="1574e-122">In the Check number field, type a value.</span></span>
    * <span data-ttu-id="1574e-123">Saate sisestada hilisema kuupäevaga dateeritud tšeki numbri või seda muuta.</span><span class="sxs-lookup"><span data-stu-id="1574e-123">Enter or modify the number of the postdated check.</span></span>  
13. <span data-ttu-id="1574e-124">Sisestage väärtus väljale Väljaandva panga nimi.</span><span class="sxs-lookup"><span data-stu-id="1574e-124">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="1574e-125">Saate sisestada väljaandva panga üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="1574e-125">enter the bank details for the issuing bank.</span></span>  
14. <span data-ttu-id="1574e-126">Klõpsake vahekaarti Loend.</span><span class="sxs-lookup"><span data-stu-id="1574e-126">Click the List tab.</span></span>
15. <span data-ttu-id="1574e-127">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="1574e-127">Click Post.</span></span>
16. <span data-ttu-id="1574e-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="1574e-128">Close the page.</span></span>
17. <span data-ttu-id="1574e-129">Klõpsake vahekaarti Hilisema kuupäevaga dateeritud tšekid.</span><span class="sxs-lookup"><span data-stu-id="1574e-129">Click the Postdated checks tab.</span></span>


