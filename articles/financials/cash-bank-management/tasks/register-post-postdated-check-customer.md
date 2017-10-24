--- 
title: "Kliendi hilisema kuupäevaga tšeki registreerimine ja sisestamine"
description: "Saate registreerida kliendilt saadud hilisema kuupäevaga tšeki üksikasjad."
author: kweekley
manager: AnnBe
ms.date: 11/14/2016
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1610036815349f625a67d5dd67260114d42fff97
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="register-and-post-a-postdated-check-for-a-customer"></a><span data-ttu-id="bd97d-103">Kliendi hilisema kuupäevaga tšeki registreerimine ja sisestamine</span><span class="sxs-lookup"><span data-stu-id="bd97d-103">Register and post a postdated check for a customer</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bd97d-104">Saate registreerida kliendilt saadud hilisema kuupäevaga tšeki üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="bd97d-104">You can register details of a postdated cheque received from a customer.</span></span> <span data-ttu-id="bd97d-105">Saate ka sisestada hilisema kuupäevaga dateeritud tšeki ja luua finantskanded.</span><span class="sxs-lookup"><span data-stu-id="bd97d-105">You can also post the postdated cheque and generate financial transactions.</span></span>   <span data-ttu-id="bd97d-106">Lõpetage enne kliendilt saadud hilisema kuupäevaga tšeki registreerimist ja sisestamist järgmised ülesanded: seadistage lehel Sularaha ja panga haldus hilisema kuupäevaga tšekid ja määrake hilisema kuupäevaga tšekkide jaoks maksemeetod. Seda toimingut tehakse rollis Laekur.</span><span class="sxs-lookup"><span data-stu-id="bd97d-106">Complete the following tasks before you register and post a postdated cheque received from a customer:   • Set up postdated Cheques in the Cash and bank management page • Set up a method of payment for postdated Cheques   The role for this procedure is Treasurer.</span></span> <span data-ttu-id="bd97d-107">See protsess kasutab demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="bd97d-107">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="bd97d-108">Avage Müügireskontro > Maksed > Makse tööleht.</span><span class="sxs-lookup"><span data-stu-id="bd97d-108">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="bd97d-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="bd97d-109">Click New.</span></span>
3. <span data-ttu-id="bd97d-110">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="bd97d-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="bd97d-111">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="bd97d-111">Click Lines.</span></span>
5. <span data-ttu-id="bd97d-112">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="bd97d-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="bd97d-113">Täpsustage soovitud väärtusi väljal Konto.</span><span class="sxs-lookup"><span data-stu-id="bd97d-113">In the Account field, specify the desired values.</span></span>
7. <span data-ttu-id="bd97d-114">Sisestage arv väljale Kreedit.</span><span class="sxs-lookup"><span data-stu-id="bd97d-114">In the Credit field, enter a number.</span></span>
    * <span data-ttu-id="bd97d-115">Sisestage hilisema kuupäevaga dateeritud tšekis määratud summa.</span><span class="sxs-lookup"><span data-stu-id="bd97d-115">Enter the amount specified in the postdated cheque.</span></span>  
8. <span data-ttu-id="bd97d-116">Klõpsake vahekaarti Makse.</span><span class="sxs-lookup"><span data-stu-id="bd97d-116">Click the Payment tab.</span></span>
9. <span data-ttu-id="bd97d-117">Sisestage väärtus väljale Makseviis.</span><span class="sxs-lookup"><span data-stu-id="bd97d-117">In the Method of payment field, type a value.</span></span>
    * <span data-ttu-id="bd97d-118">Valige makseviis hilisema kuupäevaga dateeritud tšekile.</span><span class="sxs-lookup"><span data-stu-id="bd97d-118">Select the method of payment for the postdated cheque</span></span>  
10. <span data-ttu-id="bd97d-119">Klõpsake vahekaarti Hilisema kuupäevaga dateeritud tšekid.</span><span class="sxs-lookup"><span data-stu-id="bd97d-119">Click the Postdated checks tab.</span></span>
11. <span data-ttu-id="bd97d-120">Sisestage kuupäev väljale Tähtaja kuupäev.</span><span class="sxs-lookup"><span data-stu-id="bd97d-120">In the Maturity date field, enter a date.</span></span>
    * <span data-ttu-id="bd97d-121">Sisestage kuupäev, millal hilisema kuupäevaga dateeritud tšekk kuulub maksmisele.</span><span class="sxs-lookup"><span data-stu-id="bd97d-121">Enter the date when the postdated cheque is due for payment.</span></span>  
12. <span data-ttu-id="bd97d-122">Sisestage väärtus väljale Väljaandva panga filiaal.</span><span class="sxs-lookup"><span data-stu-id="bd97d-122">In the Issuing bank branch field, type a value.</span></span>
    * <span data-ttu-id="bd97d-123">Sisestage hilisema kuupäevaga dateeritud tšeki panga üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="bd97d-123">Enter the bank details of the postdated cheque.</span></span>  
13. <span data-ttu-id="bd97d-124">Sisestage väärtus väljale Tšeki number.</span><span class="sxs-lookup"><span data-stu-id="bd97d-124">In the cheque number field, type a value.</span></span>
14. <span data-ttu-id="bd97d-125">Sisestage väärtus väljale Väljaandva panga nimi.</span><span class="sxs-lookup"><span data-stu-id="bd97d-125">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="bd97d-126">Sisestage hilisema kuupäevaga dateeritud tšeki panga üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="bd97d-126">Enter the bank details of the postdated check.</span></span>  
15. <span data-ttu-id="bd97d-127">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="bd97d-127">Click Post.</span></span>
16. <span data-ttu-id="bd97d-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="bd97d-128">Close the page.</span></span>


