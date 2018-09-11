--- 
title: Pakkumiskutsetele hindamismeetodi loomine
description: "Selles protseduuris näidatakse, kuidas hindamismeetodit luua."
author: mkirknel
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchRFQScoringMethod
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 0235723e0e5668c53ca6f6ac79732502aeae551a
ms.contentlocale: et-ee
ms.lasthandoff: 09/11/2018

---
# <a name="create-a-scoring-method-for-rfqs"></a><span data-ttu-id="cf3c9-103">Pakkumiskutsetele hindamismeetodi loomine</span><span class="sxs-lookup"><span data-stu-id="cf3c9-103">Create a scoring method for RFQs</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cf3c9-104">Selles protseduuris näidatakse, kuidas hindamismeetodit luua.</span><span class="sxs-lookup"><span data-stu-id="cf3c9-104">This procedure shows you how to create a scoring method.</span></span> <span data-ttu-id="cf3c9-105">Hindamismeetod on kriteeriumide kogum, mida saab kasutada pakkumiskutsele vastuseks saadetud pakkumiste võrdlemiseks.</span><span class="sxs-lookup"><span data-stu-id="cf3c9-105">A scoring method is a set of criteria that can be used to compare bids that are sent in reply to a request for quotation (RFQ).</span></span> <span data-ttu-id="cf3c9-106">Näiteks võib olla vaja hinnata hankijat varasema soorituse põhjal või hinnata, kas ettevõte on keskkonnasõbralik või hea koostööpartner, või võrrelda pakkumisi hinna alusel.</span><span class="sxs-lookup"><span data-stu-id="cf3c9-106">For example, you might want to rate a vendor on past performance, or rate whether the company is environmentally friendly or a good collaborator, or you might want to compare bids based on price.</span></span> <span data-ttu-id="cf3c9-107">Hindamismeetodi saab seostada kutse tüübiga seda tüüpi pakkumiskutsete vaike-hindamismeetodina.</span><span class="sxs-lookup"><span data-stu-id="cf3c9-107">The scoring method can be associated with a solicitation type as the default scoring method for RFQs of that type.</span></span> <span data-ttu-id="cf3c9-108">Neid ülesandeid täidab üldjuhul ostujuht.</span><span class="sxs-lookup"><span data-stu-id="cf3c9-108">These tasks would typically be carried out by a purchasing manager.</span></span> <span data-ttu-id="cf3c9-109">Saate selle protseduuriga tutvuda demoettevõtte USMF või oma andmeid kasutades.</span><span class="sxs-lookup"><span data-stu-id="cf3c9-109">You can use this procedure in demo data company USMF or on your own data.</span></span>

1. <span data-ttu-id="cf3c9-110">Valige Hanked > Seadistus > Pakkumiskutse > Hindamismeetod.</span><span class="sxs-lookup"><span data-stu-id="cf3c9-110">Go to Procurement and sourcing > Setup > Request for quotation > Scoring method.</span></span>
2. <span data-ttu-id="cf3c9-111">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="cf3c9-111">Click New.</span></span>
3. <span data-ttu-id="cf3c9-112">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="cf3c9-112">In the Name field, type a value.</span></span>
4. <span data-ttu-id="cf3c9-113">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="cf3c9-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="cf3c9-114">Klõpsake nuppu Salvesta.</span><span class="sxs-lookup"><span data-stu-id="cf3c9-114">Click Save.</span></span>
6. <span data-ttu-id="cf3c9-115">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="cf3c9-115">Click New.</span></span>
7. <span data-ttu-id="cf3c9-116">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="cf3c9-116">In the Name field, type a value.</span></span>
8. <span data-ttu-id="cf3c9-117">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="cf3c9-117">In the Description field, type a value.</span></span>
    * <span data-ttu-id="cf3c9-118">Kirjeldus kuvatakse koos hindamismeetodi nimega, kui hindamismeetod pakkumiskutse puhul valitakse.</span><span class="sxs-lookup"><span data-stu-id="cf3c9-118">This description is shown along with the scoring method name when a scoring method is selected for an RFQ.</span></span>  
9. <span data-ttu-id="cf3c9-119">Sisestage number väljale Vahemik alates.</span><span class="sxs-lookup"><span data-stu-id="cf3c9-119">In the Range from field, enter a number.</span></span>
    * <span data-ttu-id="cf3c9-120">Vahemiku piirid, mille hankespetsialist saab skoorina sisestada.</span><span class="sxs-lookup"><span data-stu-id="cf3c9-120">The range limits what the procurement professional can enter as a score.</span></span> <span data-ttu-id="cf3c9-121">Kui pakkumiskutsel on mitu hindamiskriteeriumi, liidetakse sisestatud skoorid üksteisele ja summa tehakse kättesaadavaks, et pakkumisi saaks võrrelda.</span><span class="sxs-lookup"><span data-stu-id="cf3c9-121">When there are multiple scoring criteria on an RFQ, the scores that have been entered are added to each other and the sum is made available to allow the bids to be compared.</span></span>  
10. <span data-ttu-id="cf3c9-122">Sisestage number väljale Vahemik kuni.</span><span class="sxs-lookup"><span data-stu-id="cf3c9-122">In the Range to field, enter a number.</span></span>
11. <span data-ttu-id="cf3c9-123">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="cf3c9-123">Click New.</span></span>
12. <span data-ttu-id="cf3c9-124">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="cf3c9-124">In the Name field, type a value.</span></span>
13. <span data-ttu-id="cf3c9-125">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="cf3c9-125">In the Description field, type a value.</span></span>
14. <span data-ttu-id="cf3c9-126">Sisestage number väljale Vahemik alates.</span><span class="sxs-lookup"><span data-stu-id="cf3c9-126">In the Range from field, enter a number.</span></span>
15. <span data-ttu-id="cf3c9-127">Sisestage number väljale Vahemik kuni.</span><span class="sxs-lookup"><span data-stu-id="cf3c9-127">In the Range to field, enter a number.</span></span>


