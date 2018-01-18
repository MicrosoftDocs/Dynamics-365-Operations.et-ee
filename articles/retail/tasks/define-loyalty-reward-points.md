--- 
title: " Püsikliendi preemiapunktide määratlemine"
description: "See protseduur juhendab püsikliendi preemiapunktide määratlemisel."
author: scott-tucker
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: scotttuc
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: b143675e5de12cfe2ca4b0fa949e68d56f920c9c
ms.contentlocale: et-ee
ms.lasthandoff: 01/17/2018

---
# <a name="define-loyalty-reward-points"></a><span data-ttu-id="c6a5b-103"> Püsikliendi preemiapunktide määratlemine</span><span class="sxs-lookup"><span data-stu-id="c6a5b-103">Define loyalty reward points</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="c6a5b-104">See protseduur juhendab püsikliendi preemiapunktide määratlemisel.</span><span class="sxs-lookup"><span data-stu-id="c6a5b-104">This procedure walks through defining loyalty reward points.</span></span> <span data-ttu-id="c6a5b-105">Püsikliendi preemiapunktid tuleks seadistada enne püsikliendi programmi alustamist.</span><span class="sxs-lookup"><span data-stu-id="c6a5b-105">You should set up loyalty reward points before you set up a loyalty program.</span></span> <span data-ttu-id="c6a5b-106">Protseduur kasutab demoettevõtte USRT andmeid.</span><span class="sxs-lookup"><span data-stu-id="c6a5b-106">This procedure uses the USRT demo data company.</span></span>

1. <span data-ttu-id="c6a5b-107">Avage Jaemüük ja kaubandus > Kliendid > Püsiklient > Püsikliendi preemiapunktid.</span><span class="sxs-lookup"><span data-stu-id="c6a5b-107">Go to Retail and commerce > Customers > Loyalty > Loyalty reward points.</span></span>
2. <span data-ttu-id="c6a5b-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="c6a5b-108">Click New.</span></span>
3. <span data-ttu-id="c6a5b-109">Sisestage väärtus väljale Reward point ID (Preemiapunkti ID).</span><span class="sxs-lookup"><span data-stu-id="c6a5b-109">In the Reward point ID field, type a value.</span></span>
4. <span data-ttu-id="c6a5b-110">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="c6a5b-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="c6a5b-111">Valige suvand väljal Reward point type (Preemiapunkti tüüp).</span><span class="sxs-lookup"><span data-stu-id="c6a5b-111">In the Reward point type field, select an option.</span></span>
    * <span data-ttu-id="c6a5b-112">Valige Kogus, kui soovite, et preemiapunktid ümardataks lähima täisarvuni.</span><span class="sxs-lookup"><span data-stu-id="c6a5b-112">Select Quantity if you want the reward points to be rounded to the nearest integer.</span></span> <span data-ttu-id="c6a5b-113">Kui soovite, et preemiapunktid ümardataks valuuta ümardamisreeglite järgi, valige Summa.</span><span class="sxs-lookup"><span data-stu-id="c6a5b-113">Select Amount if you want the reward points to be rounded according to currency rounding rules.</span></span> <span data-ttu-id="c6a5b-114">Kui teete valiku Kogus, jätke selle protseduuri järgmine etapp vahele.</span><span class="sxs-lookup"><span data-stu-id="c6a5b-114">If you select Quantity, skip the next step of this procedure..</span></span>  
6. <span data-ttu-id="c6a5b-115">Sisestage väärtus väljale Valuuta.</span><span class="sxs-lookup"><span data-stu-id="c6a5b-115">In the Currency field, type a value.</span></span>
    * <span data-ttu-id="c6a5b-116">Summa tüüpi preemiapunktide kasutamisel on kõik väljastatavad punktid valitud valuutas.</span><span class="sxs-lookup"><span data-stu-id="c6a5b-116">For Amount type reward points, all points issued will have the selected currency.</span></span> <span data-ttu-id="c6a5b-117">Koguse tüüpi preemiapunktide korral see väli ei kehti. Jätke see etapp vahele.</span><span class="sxs-lookup"><span data-stu-id="c6a5b-117">For Quantity type reward points, this field doesn't apply—skip this step.</span></span>  
7. <span data-ttu-id="c6a5b-118">Märkige ruut Redeemable (Lunastatav) või eemaldage sellest märge.</span><span class="sxs-lookup"><span data-stu-id="c6a5b-118">Check or uncheck the Redeemable checkbox.</span></span>
8. <span data-ttu-id="c6a5b-119">Sisestage number väljale Redeem ranking (Lunastusjärk).</span><span class="sxs-lookup"><span data-stu-id="c6a5b-119">In the Redeem ranking field, enter a number.</span></span>
    * <span data-ttu-id="c6a5b-120">Lunastusjärke kasutatakse, kui toodete eest maksmiseks saab kasutada kahte või enamat sobivat preemiapunkti.</span><span class="sxs-lookup"><span data-stu-id="c6a5b-120">Redeem ranking is used when two or more redeemable reward points can be used to pay for products.</span></span> <span data-ttu-id="c6a5b-121">Kui kahel preemiapunktil on sama lunastusjärk, siis kasutatakse seda, mille punktide arv vajab langetamist.</span><span class="sxs-lookup"><span data-stu-id="c6a5b-121">If the two reward points have the same redeem ranking, then the one that needs to lower number of points will be used.</span></span>  
9. <span data-ttu-id="c6a5b-122">Sisestage väljale Expiration time value (Realiseerimisaja väärtus) number.</span><span class="sxs-lookup"><span data-stu-id="c6a5b-122">In the Expiration time value field, enter a number.</span></span>
    * <span data-ttu-id="c6a5b-123">Preemiapunktid aeguvad nende väljastamise järel teatud arvu päevade, kuude või aastate pärast.</span><span class="sxs-lookup"><span data-stu-id="c6a5b-123">The reward points will expire the specified number of days, months, or years after when the points are issued.</span></span> <span data-ttu-id="c6a5b-124">Väärtus "0" tähendab, et püsikliendi preemiapunktid ei aegu kunagi.</span><span class="sxs-lookup"><span data-stu-id="c6a5b-124">A value of ‘0’ means the loyalty reward points will never expire.</span></span>  
10. <span data-ttu-id="c6a5b-125">Valige suvand väljal Expiration time unit (Realiseerimisaja ühik).</span><span class="sxs-lookup"><span data-stu-id="c6a5b-125">In the Expiration time unit field, select an option.</span></span>
11. <span data-ttu-id="c6a5b-126">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="c6a5b-126">Click Save.</span></span>


