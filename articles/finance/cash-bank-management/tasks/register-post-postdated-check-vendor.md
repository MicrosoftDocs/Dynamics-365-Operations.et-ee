---
title: Hankija hilisema kuupäevaga tšeki registreerimine ja sisestamine
description: Saate registreerida hilisema kuupäevaga dateeritud tšeki üksikasjad enne tšeki väljastamist hankijale, kasutades töölehe kannet.
author: kweekley
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransVendPaym
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3d26879ab54b5d87252287ab64fa3c7ae4ae4a90
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4985208"
---
# <a name="register-and-post-a-postdated-check-for-a-vendor"></a><span data-ttu-id="b2e6b-103">Hankija hilisema kuupäevaga tšeki registreerimine ja sisestamine</span><span class="sxs-lookup"><span data-stu-id="b2e6b-103">Register and post a postdated check for a vendor</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b2e6b-104">Saate registreerida hilisema kuupäevaga dateeritud tšeki üksikasjad enne tšeki väljastamist hankijale, kasutades töölehe kannet.</span><span class="sxs-lookup"><span data-stu-id="b2e6b-104">You can register the details of a postdated check before you issue the check to a vendor by using the journal voucher.</span></span> <span data-ttu-id="b2e6b-105">Saate ka sisestada hilisema kuupäevaga dateeritud tšeki ja luua finantskanded.</span><span class="sxs-lookup"><span data-stu-id="b2e6b-105">You can also post the postdated check and generate financial transactions.</span></span> <span data-ttu-id="b2e6b-106">Enne kui saate registreerida ja sisestada kliendilt saadud hilisema kuupäevaga dateeritud tšeki, peate täitma järgmise ülesande.</span><span class="sxs-lookup"><span data-stu-id="b2e6b-106">Before you register and post a postdated check from a vendor, complete the following task:</span></span> 

<span data-ttu-id="b2e6b-107">Hilisema kuupäevaga dateeritud tšekkide seadistamine lehel Sularaha- ja pangahaldus.</span><span class="sxs-lookup"><span data-stu-id="b2e6b-107">Set up postdated checks in the Cash and bank management page.</span></span> 



<span data-ttu-id="b2e6b-108">Selle ülesandejuhendi roll on Kassiir.</span><span class="sxs-lookup"><span data-stu-id="b2e6b-108">The role of this task guides is Treasurer.</span></span> <span data-ttu-id="b2e6b-109">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="b2e6b-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="b2e6b-110">Avage Ostureskonto > Maksed > Makse tööleht</span><span class="sxs-lookup"><span data-stu-id="b2e6b-110">Go to Acounts payable > Payments > Payment journal</span></span>
2. <span data-ttu-id="b2e6b-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="b2e6b-111">Click New.</span></span>
3. <span data-ttu-id="b2e6b-112">Sisestage väljale Nimi tekst „VendPay”.</span><span class="sxs-lookup"><span data-stu-id="b2e6b-112">In the Name field, type 'VendPay'.</span></span>
4. <span data-ttu-id="b2e6b-113">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="b2e6b-113">Click Lines.</span></span>
5. <span data-ttu-id="b2e6b-114">Täpsustage soovitud väärtusi väljal Konto.</span><span class="sxs-lookup"><span data-stu-id="b2e6b-114">In the Account field, specify the desired values.</span></span>
6. <span data-ttu-id="b2e6b-115">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="b2e6b-115">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="b2e6b-116">Sisestage arv väljale Deebet.</span><span class="sxs-lookup"><span data-stu-id="b2e6b-116">In the Debit field, enter a number.</span></span>
8. <span data-ttu-id="b2e6b-117">Klõpsake väljal Makseviis otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="b2e6b-117">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="b2e6b-118">Valige makseviis hilisema kuupäevaga dateeritud tšekile.</span><span class="sxs-lookup"><span data-stu-id="b2e6b-118">Select the method of payment for the postdated check</span></span>  
9. <span data-ttu-id="b2e6b-119">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="b2e6b-119">In the list, find and select the desired record.</span></span>
10. <span data-ttu-id="b2e6b-120">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="b2e6b-120">In the list, click the link in the selected row.</span></span>
11. <span data-ttu-id="b2e6b-121">Klõpsake vahekaarti Hilisema kuupäevaga dateeritud tšekid.</span><span class="sxs-lookup"><span data-stu-id="b2e6b-121">Click the Postdated checks tab.</span></span>
12. <span data-ttu-id="b2e6b-122">Sisestage väärtus väljale Tšeki number.</span><span class="sxs-lookup"><span data-stu-id="b2e6b-122">In the Check number field, type a value.</span></span>
    * <span data-ttu-id="b2e6b-123">Saate sisestada hilisema kuupäevaga dateeritud tšeki numbri või seda muuta.</span><span class="sxs-lookup"><span data-stu-id="b2e6b-123">Enter or modify the number of the postdated check.</span></span>  
13. <span data-ttu-id="b2e6b-124">Sisestage väärtus väljale Väljaandva panga nimi.</span><span class="sxs-lookup"><span data-stu-id="b2e6b-124">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="b2e6b-125">Saate sisestada väljaandva panga üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="b2e6b-125">enter the bank details for the issuing bank.</span></span>  
14. <span data-ttu-id="b2e6b-126">Klõpsake vahekaarti Loend.</span><span class="sxs-lookup"><span data-stu-id="b2e6b-126">Click the List tab.</span></span>
15. <span data-ttu-id="b2e6b-127">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="b2e6b-127">Click Post.</span></span>
16. <span data-ttu-id="b2e6b-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="b2e6b-128">Close the page.</span></span>
17. <span data-ttu-id="b2e6b-129">Klõpsake vahekaarti Hilisema kuupäevaga dateeritud tšekid.</span><span class="sxs-lookup"><span data-stu-id="b2e6b-129">Click the Postdated checks tab.</span></span>

