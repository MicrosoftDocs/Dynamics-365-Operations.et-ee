---
title: Kliendi hilisema kuupäevaga tšeki registreerimine ja sisestamine
description: Saate registreerida kliendilt saadud hilisema kuupäevaga tšeki üksikasjad.
author: kweekley
manager: AnnBe
ms.date: 10/26/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a7b7899e11849175976b4c7ee44be4355e733d1d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5225341"
---
# <a name="register-and-post-a-postdated-check-for-a-customer"></a><span data-ttu-id="23279-103">Kliendi hilisema kuupäevaga tšeki registreerimine ja sisestamine</span><span class="sxs-lookup"><span data-stu-id="23279-103">Register and post a postdated check for a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="23279-104">Saate registreerida kliendilt saadud hilisema kuupäevaga tšeki üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="23279-104">You can register details of a postdated check received from a customer.</span></span> <span data-ttu-id="23279-105">Saate ka sisestada hilisema kuupäevaga dateeritud tšeki ja luua finantskanded.</span><span class="sxs-lookup"><span data-stu-id="23279-105">You can also post the postdated check and generate financial transactions.</span></span>   <span data-ttu-id="23279-106">Viige lõpule enne kliendilt saadud hilisema kuupäevaga tšeki registreerimist ja sisestamist järgmised ülesanded.   \* Seadistage lehel Sularaha ja panga haldus hilisema kuupäevaga tšekid \* Määrake hilisema kuupäevaga tšekkide jaoks maksemeetod   Seda toimingut tehakse rollis Laekur.</span><span class="sxs-lookup"><span data-stu-id="23279-106">Complete the following tasks before you register and post a postdated check received from a customer:   \* Set up postdated check in the Cash and bank management page \* Set up a method of payment for postdated checks   The role for this procedure is Treasurer.</span></span> <span data-ttu-id="23279-107">See protsess kasutab demoettevõtte USMF-i andmeid.</span><span class="sxs-lookup"><span data-stu-id="23279-107">This procedure uses the USMF demo company.</span></span>

1. <span data-ttu-id="23279-108">Avage Müügireskontro > Maksed > Makse tööleht.</span><span class="sxs-lookup"><span data-stu-id="23279-108">Go to Accounts receivable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="23279-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="23279-109">Click New.</span></span>
3. <span data-ttu-id="23279-110">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="23279-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="23279-111">Klõpsake valikut Read.</span><span class="sxs-lookup"><span data-stu-id="23279-111">Click Lines.</span></span>
5. <span data-ttu-id="23279-112">Märkige loendis valitud rida.</span><span class="sxs-lookup"><span data-stu-id="23279-112">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="23279-113">Täpsustage soovitud väärtusi väljal Konto.</span><span class="sxs-lookup"><span data-stu-id="23279-113">In the Account field, specify the desired values.</span></span>
7. <span data-ttu-id="23279-114">Sisestage arv väljale Kreedit.</span><span class="sxs-lookup"><span data-stu-id="23279-114">In the Credit field, enter a number.</span></span>
    * <span data-ttu-id="23279-115">Sisestage hilisema kuupäevaga dateeritud tšekis määratud summa.</span><span class="sxs-lookup"><span data-stu-id="23279-115">Enter the amount specified in the postdated check.</span></span>  
8. <span data-ttu-id="23279-116">Klõpsake vahekaarti Makse.</span><span class="sxs-lookup"><span data-stu-id="23279-116">Click the Payment tab.</span></span>
9. <span data-ttu-id="23279-117">Sisestage väärtus väljale Makseviis.</span><span class="sxs-lookup"><span data-stu-id="23279-117">In the Method of payment field, type a value.</span></span>
    * <span data-ttu-id="23279-118">Valige makseviis hilisema kuupäevaga dateeritud tšekile.</span><span class="sxs-lookup"><span data-stu-id="23279-118">Select the method of payment for the postdated check.</span></span>  
10. <span data-ttu-id="23279-119">Klõpsake vahekaarti Hilisema kuupäevaga dateeritud tšekid.</span><span class="sxs-lookup"><span data-stu-id="23279-119">Click the Postdated checks tab.</span></span>
11. <span data-ttu-id="23279-120">Sisestage kuupäev väljale Tähtaja kuupäev.</span><span class="sxs-lookup"><span data-stu-id="23279-120">In the Maturity date field, enter a date.</span></span>
    * <span data-ttu-id="23279-121">Sisestage kuupäev, millal hilisema kuupäevaga dateeritud tšekk kuulub maksmisele.</span><span class="sxs-lookup"><span data-stu-id="23279-121">Enter the date when the postdated check is due for payment.</span></span>  
12. <span data-ttu-id="23279-122">Sisestage väärtus väljale Väljaandva panga filiaal.</span><span class="sxs-lookup"><span data-stu-id="23279-122">In the Issuing bank branch field, type a value.</span></span>
    * <span data-ttu-id="23279-123">Sisestage hilisema kuupäevaga dateeritud tšeki panga üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="23279-123">Enter the bank details of the postdated check.</span></span>  
13. <span data-ttu-id="23279-124">Sisestage väärtus väljale Tšeki number.</span><span class="sxs-lookup"><span data-stu-id="23279-124">In the check number field, type a value.</span></span>
14. <span data-ttu-id="23279-125">Sisestage väärtus väljale Väljaandva panga nimi.</span><span class="sxs-lookup"><span data-stu-id="23279-125">In the Issuing bank name field, type a value.</span></span>
    * <span data-ttu-id="23279-126">Sisestage hilisema kuupäevaga dateeritud tšeki panga üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="23279-126">Enter the bank details of the postdated check.</span></span>  
15. <span data-ttu-id="23279-127">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="23279-127">Click Post.</span></span>
16. <span data-ttu-id="23279-128">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="23279-128">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]