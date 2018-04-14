--- 
title: "Põhivara kulumi arvutamine juriidiliste isikute lõikes"
description: "See protseduur näitab, kuidas seadistada ja käivitada mitme juriidilise isiku kulumiprotsessi."
author: saraschi2
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 662554b1b6bed63e5017aad3a292dad7a2f0bcea
ms.contentlocale: et-ee
ms.lasthandoff: 04/13/2018

---
# <a name="calculate-fixed-asset-depreciation-across-legal-entities"></a><span data-ttu-id="c16a1-103">Põhivara kulumi arvutamine juriidiliste isikute lõikes</span><span class="sxs-lookup"><span data-stu-id="c16a1-103">Calculate fixed asset depreciation across legal entities</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c16a1-104">Mitme juriidilise isiku põhivara kulumit saab käitada ühe etapina.</span><span class="sxs-lookup"><span data-stu-id="c16a1-104">Fixed asset depreciation can be run across legal entities in a single step.</span></span> <span data-ttu-id="c16a1-105">See protseduur näitab, kuidas seadistada ja käitada protsessi mitme juriidilise isiku jaoks.</span><span class="sxs-lookup"><span data-stu-id="c16a1-105">This procedure shows you to how set up and run the process for multiple legal entities.</span></span> <span data-ttu-id="c16a1-106">Selleks kasutatakse raamatupidaja rolli.</span><span class="sxs-lookup"><span data-stu-id="c16a1-106">It uses the accountant role.</span></span>  

<span data-ttu-id="c16a1-107">Salvestamisel kasutatakse demoettevõtte USMF-i.</span><span class="sxs-lookup"><span data-stu-id="c16a1-107">This recording uses the USMF demo company.</span></span>


<span data-ttu-id="c16a1-108">Toimingud (16) Alamtoiming: seadistage kontsernisiseste kulumikäituste töölehed.</span><span class="sxs-lookup"><span data-stu-id="c16a1-108">Steps (16) Sub-task: Set up cross company depreciation run journals.</span></span> 

1. <span data-ttu-id="c16a1-109">Esmalt peate seadistama töölehed, mida kasutatakse iga juriidilise isiku kontsernisiseses kulumikäituses.</span><span class="sxs-lookup"><span data-stu-id="c16a1-109">First, you must set up the journals to be used in the cross company depreciation run in each legal entity.</span></span> <span data-ttu-id="c16a1-110">Avage Põhivarad > Seadistus > Põhivarade parameetrid.</span><span class="sxs-lookup"><span data-stu-id="c16a1-110">Go to Fixed assets > Setup > Fixed assets parameters.</span></span> 
2. <span data-ttu-id="c16a1-111">Laiendage jaotist Põhivara ettepanekud.</span><span class="sxs-lookup"><span data-stu-id="c16a1-111">Expand the Fixed asset proposals section.</span></span> 
3. <span data-ttu-id="c16a1-112">Looge töölehe nimega kirje, mida kasutatakse juriidilises isikus iga sisestamiskihi jaoks.</span><span class="sxs-lookup"><span data-stu-id="c16a1-112">Create a record with the journal name to be used for each posting layer in the legal entity.</span></span> <span data-ttu-id="c16a1-113">Kui raamatuid ei sisestata pearaamatusse, tuleb valida sisestamiskiht Puudub ja sellega seotud tööleht.</span><span class="sxs-lookup"><span data-stu-id="c16a1-113">If books do not post to the general ledger, then the None posting layer should be selected with the associated journal.</span></span> <span data-ttu-id="c16a1-114">Klõpsake vahekaarti Lisa.</span><span class="sxs-lookup"><span data-stu-id="c16a1-114">Click Add.</span></span> 
4. <span data-ttu-id="c16a1-115">Valige või sisestage väärtus väljal Sisestamiskiht.</span><span class="sxs-lookup"><span data-stu-id="c16a1-115">In the Posting layer field, enter or select a value.</span></span> 
5. <span data-ttu-id="c16a1-116">Valige või sisestage väärtus väljal Töölehe nimi.</span><span class="sxs-lookup"><span data-stu-id="c16a1-116">In the Journal name field, enter or select a value.</span></span> 
6. <span data-ttu-id="c16a1-117">Korrake töölehe seadistust iga juriidilise isiku lehel Põhivara parameetrid.</span><span class="sxs-lookup"><span data-stu-id="c16a1-117">Repeat the journal setup on the Fixed asset parameters page in each legal entity.</span></span> 

<span data-ttu-id="c16a1-118">Alamülesanne: kulumi arvutamine</span><span class="sxs-lookup"><span data-stu-id="c16a1-118">Sub-task: Calculate depreciation</span></span>

1. <span data-ttu-id="c16a1-119">Lehel Kulumiettepaneku loomine saate käivitada kulumikäituse mitmes juriidilises isikus.</span><span class="sxs-lookup"><span data-stu-id="c16a1-119">Use the Create depreciation proposal page to start your depreciation run across legal entities.</span></span> <span data-ttu-id="c16a1-120">Avage Põhivarad > Töölehe kirjed > Kulumisoovituse koostamine.</span><span class="sxs-lookup"><span data-stu-id="c16a1-120">Go to Fixed assets > Journal entries > Create depreciation proposal.</span></span> 
2. <span data-ttu-id="c16a1-121">Valige või sisestage väärtus väljal Sisestamiskiht.</span><span class="sxs-lookup"><span data-stu-id="c16a1-121">In the Posting layer field, enter or select a value.</span></span> 
3. <span data-ttu-id="c16a1-122">Töölehe nimi põhineb põhivara parameetrites määratud vaikesättel.</span><span class="sxs-lookup"><span data-stu-id="c16a1-122">The journal name will default from the Fixed asset parameters.</span></span> <span data-ttu-id="c16a1-123">Seda saab praeguse juriidilise isiku jaoks siin muuta.</span><span class="sxs-lookup"><span data-stu-id="c16a1-123">It can be changed here for the current legal entity.</span></span> 
4. <span data-ttu-id="c16a1-124">Sisestage kuupäev väljale Lõpukuupäev.</span><span class="sxs-lookup"><span data-stu-id="c16a1-124">In the To date field, enter a date.</span></span> 
5. <span data-ttu-id="c16a1-125">Valige kulumikäitusesse kaasatavad juriidilised isikud.</span><span class="sxs-lookup"><span data-stu-id="c16a1-125">Select the legal entities to be included in the depreciation run.</span></span> <span data-ttu-id="c16a1-126">Loendis kuvatakse ainult juriidilised isikud, kelle töölehed on põhivara parameetrite lehel põhivara ettepanekute jaoks häälestatud.</span><span class="sxs-lookup"><span data-stu-id="c16a1-126">Only legal entities with journals set up for Fixed asset proposals on the Fixed asset parameters page will be shown in the list.</span></span> 
6. <span data-ttu-id="c16a1-127">Kui suvand Sisesta töölehed on lubatud, sisestatakse kulumitöölehed loomisel automaatselt.</span><span class="sxs-lookup"><span data-stu-id="c16a1-127">When enabled, the Post journals option will automatically post the depreciation journals when they are created.</span></span> <span data-ttu-id="c16a1-128">Kui suvand ei ole valitud, siis loodud töölehti ei sisestata, et saaksite üksikasjad enne sisestamist üle vaadata.</span><span class="sxs-lookup"><span data-stu-id="c16a1-128">When not selected, the journals will be created, but not posted, so you can review the details before posting.</span></span> <span data-ttu-id="c16a1-129">Valige väljal Sisesta töölehed väärtus Jah.</span><span class="sxs-lookup"><span data-stu-id="c16a1-129">Select Yes in the Post journals field.</span></span> 
7. <span data-ttu-id="c16a1-130">Filtreerimisväljad hõlmavad kõiki selle kulumikäituse jaoks valitud juriidiliste isikute põhivarasid, gruppe ja raamatuid.</span><span class="sxs-lookup"><span data-stu-id="c16a1-130">Filtering fields include all fixed assets, groups, and books for the legal entities selected for this depreciation run.</span></span> 
8. <span data-ttu-id="c16a1-131">Suvand Pakktöötlus on vaikimisi lubatud.</span><span class="sxs-lookup"><span data-stu-id="c16a1-131">The Batch processing option is enabled by default.</span></span> <span data-ttu-id="c16a1-132">Kui suvand on lubatud, toimub kulumitöölehe loomine ja sisestamine taustal.</span><span class="sxs-lookup"><span data-stu-id="c16a1-132">When this option is enabled, the depreciation journal creation and posting will run in the background.</span></span> 
9. <span data-ttu-id="c16a1-133">Klõpsake suvandit Loo tööleht.</span><span class="sxs-lookup"><span data-stu-id="c16a1-133">Click Create journal.</span></span> 
10. <span data-ttu-id="c16a1-134">Peate vaatama vastavates juriidilistes isikutes loodud kulumitöölehti.</span><span class="sxs-lookup"><span data-stu-id="c16a1-134">You must view the depreciation journals created in the respective legal entities.</span></span> <span data-ttu-id="c16a1-135">Avage Põhivarad > Töölehe sisestused > Põhivarade tööleht.</span><span class="sxs-lookup"><span data-stu-id="c16a1-135">Go to Fixed assets > Journal entries > Fixed assets journal.</span></span>

