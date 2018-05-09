--- 
title: "Viitvõlaskeemide loomine"
description: "See ülesandejuhend kirjeldab viitvõlaskeemi loomise etappe."
author: aprilolson
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: d1d7d531f547f517d1f39a6b181d9a7a782771e6
ms.contentlocale: et-ee
ms.lasthandoff: 05/08/2018

---
# <a name="create-accrual-schemes"></a><span data-ttu-id="e30de-103">Viitvõlaskeemide loomine</span><span class="sxs-lookup"><span data-stu-id="e30de-103">Create accrual schemes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e30de-104">See ülesandejuhend kirjeldab viitvõlaskeemi loomise etappe.</span><span class="sxs-lookup"><span data-stu-id="e30de-104">This task guide steps through creating an accrual scheme.</span></span> <span data-ttu-id="e30de-105">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="e30de-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="e30de-106">Minge jaotisse Pearaamat > Töölehe seadistus > Viitvõlaskeemid.</span><span class="sxs-lookup"><span data-stu-id="e30de-106">Go to General ledger > Journal setup > Accrual schemes.</span></span>
2. <span data-ttu-id="e30de-107">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="e30de-107">Click New.</span></span>
3. <span data-ttu-id="e30de-108">Sisestage väärtus väljale Viitvõla ID.</span><span class="sxs-lookup"><span data-stu-id="e30de-108">In the Accrual identification field, type a value.</span></span>
4. <span data-ttu-id="e30de-109">Sisestage väärtus väljale Viitvõlaskeemi kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="e30de-109">In the Description of accrual scheme field, type a value.</span></span>
5. <span data-ttu-id="e30de-110">Määrake väljal Deebet soovitud väärtused.</span><span class="sxs-lookup"><span data-stu-id="e30de-110">In the Debit field, specify the desired values.</span></span>
    * <span data-ttu-id="e30de-111">Määratletud põhikonto asendab deebeti põhikonto töölehe kandereal ja seda kasutatakse ka viitvõla tühistamiseks pearaamatu tekkepõhiste kannete põhjal.</span><span class="sxs-lookup"><span data-stu-id="e30de-111">The main account defined will replace the debit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
6. <span data-ttu-id="e30de-112">Määrake väljal Kreedit soovitud väärtused.</span><span class="sxs-lookup"><span data-stu-id="e30de-112">In the Credit field, specify the desired values.</span></span>
    * <span data-ttu-id="e30de-113">Määratletud põhikonto asendab kreediti põhikonto töölehe kandereal ja seda kasutatakse ka viitvõla tühistamiseks pearaamatu tekkepõhiste kannete põhjal.</span><span class="sxs-lookup"><span data-stu-id="e30de-113">The main account defined will replace the credit main account on the journal voucher line and it will also be used for the reversal of the deferral based on the ledger accrual transactions.</span></span>  
7. <span data-ttu-id="e30de-114">Valige väljal Kanne kannete sisestamisel kande määratlemise viis.</span><span class="sxs-lookup"><span data-stu-id="e30de-114">In the Voucher field, select how you want the voucher determined when the transactions are posted.</span></span>
8. <span data-ttu-id="e30de-115">Sisestage väljale Kirjeldus sisestatavaid kandeid kirjeldav väärtus.</span><span class="sxs-lookup"><span data-stu-id="e30de-115">In the Description field, type a value to describe the transactions that will be posted.</span></span>
9. <span data-ttu-id="e30de-116">Valige väljal Perioodi sagedus kannete soovitud toimumissagedus.</span><span class="sxs-lookup"><span data-stu-id="e30de-116">In the Period frequency field, select how often the transactions should occur.</span></span>
10. <span data-ttu-id="e30de-117">Sisestage arv väljale Juhtumite arv perioodide kaupa.</span><span class="sxs-lookup"><span data-stu-id="e30de-117">In the Number of occurrences by period field, enter a number.</span></span>
11. <span data-ttu-id="e30de-118">Valige väljal Kannete sisestamine kannete sisestamise aeg, näiteks Kord kuus.</span><span class="sxs-lookup"><span data-stu-id="e30de-118">In the Post transactions field, select when the transactions should be posted, such as Monthly.</span></span>


