--- 
title: "Kaupade registreerimine üldiseks ladustamiseks lubatud kauba puhul saabuva kauba töölehe abil"
description: "Selle protseduuriga selgitatakse kaupade registreerimist, kasutades kauba saabumise töölehte mooduli Laohaldus üldise ladustamise kasutamisel."
author: BibiSp
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a5fa86bace459d694ab0a2ec289e11b0e4420932
ms.openlocfilehash: 184f38347e2525f3efef9b0d55003a94a75380d4
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-arrival-journal"></a><span data-ttu-id="7a10e-103">Kaupade registreerimine üldiseks ladustamiseks lubatud kauba puhul saabuva kauba töölehe abil</span><span class="sxs-lookup"><span data-stu-id="7a10e-103">Register items for a basic warehousing enabled item using an item arrival journal</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7a10e-104">Selle protseduuriga selgitatakse kaupade registreerimist, kasutades kauba saabumise töölehte mooduli Laohaldus üldise ladustamise kasutamisel.</span><span class="sxs-lookup"><span data-stu-id="7a10e-104">This procedure shows you how to register items using the item arrival journal when you are using “basic warehousing” in the Inventory management module.</span></span> <span data-ttu-id="7a10e-105">Seda teeb üldjuhul vastuvõtuametnik.</span><span class="sxs-lookup"><span data-stu-id="7a10e-105">This would usually be done by a receiving clerk.</span></span> <span data-ttu-id="7a10e-106">Saate käitada selle protseduuri demoandmete ettevõttes USMF näidatud näidisväärtusega.</span><span class="sxs-lookup"><span data-stu-id="7a10e-106">You can run this procedure in demo data company USMF with the example values that are shown.</span></span>  <span data-ttu-id="7a10e-107">Kui te USMF-i ei kasuta, peate enne selle juhendi käivitamist olema kinnitanud avatud ostutellimuse reaga ostutellimuse.</span><span class="sxs-lookup"><span data-stu-id="7a10e-107">If you are not using USMF, you need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="7a10e-108">Rea kaup peab olema ladustatav ja see ei tohi kasutada tootevariante ja sellel ei tohi olla jälgimisdimensioone.</span><span class="sxs-lookup"><span data-stu-id="7a10e-108">The item on the line must be stocked, and it must not use product variants, and must not have tracking dimensions.</span></span> <span data-ttu-id="7a10e-109">Samuti peavad kaubad olema seostatud laoala dimensioonigrupiga, kus sait ja ladu on aktiivsed.</span><span class="sxs-lookup"><span data-stu-id="7a10e-109">And the item needs to be associated with a storage dimension group, where site and warehouse are active.</span></span>


## <a name="create-item-arrival-journal-header"></a><span data-ttu-id="7a10e-110">Kauba saabumise töölehe päise loomine</span><span class="sxs-lookup"><span data-stu-id="7a10e-110">Create item arrival journal header</span></span>
1. <span data-ttu-id="7a10e-111">Avage Varude haldus > Töölehe sisestused > Kauba saabumine > Kauba saabumine.</span><span class="sxs-lookup"><span data-stu-id="7a10e-111">Go to Inventory management > Journal entries > Item arrival > Item arrival.</span></span>
2. <span data-ttu-id="7a10e-112">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="7a10e-112">Click New.</span></span>
3. <span data-ttu-id="7a10e-113">Sisestage väärtus väljale Nimi.</span><span class="sxs-lookup"><span data-stu-id="7a10e-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="7a10e-114">Kui kasutate USMF-i, saate sisestada WHS-i.</span><span class="sxs-lookup"><span data-stu-id="7a10e-114">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="7a10e-115">Kui kasutate muid andmeid, peavad töölehel, mille nime valite, olema järgmised atribuudid: Kontrolli komplekteerimiskohta peab olema seatud valikule Ei ja Vahelao haldus peab olema seatud valikule Ei.</span><span class="sxs-lookup"><span data-stu-id="7a10e-115">If you’re using other data, the journal whose name you choose has to have the following properties: cheque picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="7a10e-116">Sisestage väärtus väljale Saateleht.</span><span class="sxs-lookup"><span data-stu-id="7a10e-116">In the Packing slip field, type a value.</span></span>
    * <span data-ttu-id="7a10e-117">See on hankija väljastatud saatelehelt pärinev saatelehe ID.</span><span class="sxs-lookup"><span data-stu-id="7a10e-117">This is the packing slip ID from the packing slip issued by the vendor.</span></span> <span data-ttu-id="7a10e-118">Lisage kordumatu number.</span><span class="sxs-lookup"><span data-stu-id="7a10e-118">Add a unique number.</span></span>  
5. <span data-ttu-id="7a10e-119">Valige ostutellimus väljalt Number.</span><span class="sxs-lookup"><span data-stu-id="7a10e-119">In the Number field, In the Number field, select the purchase order..</span></span>
6. <span data-ttu-id="7a10e-120">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="7a10e-120">Click OK.</span></span>

## <a name="add-lines-to-item-arrival-journal"></a><span data-ttu-id="7a10e-121">Kauba saabumistöölehtede ridade lisamine</span><span class="sxs-lookup"><span data-stu-id="7a10e-121">Add lines to item arrival journal</span></span>
1. <span data-ttu-id="7a10e-122">Klõpsake suvandit Funktsioonid.</span><span class="sxs-lookup"><span data-stu-id="7a10e-122">Click Functions.</span></span>
2. <span data-ttu-id="7a10e-123">Klõpsake suvandit Loo read.</span><span class="sxs-lookup"><span data-stu-id="7a10e-123">Click Create lines.</span></span>
    * <span data-ttu-id="7a10e-124">Ridu saab sellele töölehele sisestada käsitsi või luua automaatselt.</span><span class="sxs-lookup"><span data-stu-id="7a10e-124">The lines can be entered manually into this journal or created automatically.</span></span> <span data-ttu-id="7a10e-125">See näitab, kuidas seda automaatselt luua.</span><span class="sxs-lookup"><span data-stu-id="7a10e-125">This will show you how to create this automatically.</span></span>  
3. <span data-ttu-id="7a10e-126">Märkige või tühjendage ruut Lähtesta kogus.</span><span class="sxs-lookup"><span data-stu-id="7a10e-126">Check or uncheck the Initialize quantity checkbox.</span></span>
    * <span data-ttu-id="7a10e-127">See lähtestab töölehe ridadel oleva koguse registreerimata kogusega ostutellimuse realt.</span><span class="sxs-lookup"><span data-stu-id="7a10e-127">This will initialize the quantity on the journal lines with the quantity not registered from the purchase order line.</span></span>  
4. <span data-ttu-id="7a10e-128">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="7a10e-128">Click OK.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="7a10e-129">Töölehe sisestamine</span><span class="sxs-lookup"><span data-stu-id="7a10e-129">Post the journal</span></span>
1. <span data-ttu-id="7a10e-130">Klõpsake valikut Sisesta.</span><span class="sxs-lookup"><span data-stu-id="7a10e-130">Click Post.</span></span>
2. <span data-ttu-id="7a10e-131">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="7a10e-131">Click OK.</span></span>

## <a name="generate-the-product-receipt"></a><span data-ttu-id="7a10e-132">Toote sissetuleku loomine</span><span class="sxs-lookup"><span data-stu-id="7a10e-132">Generate the product receipt</span></span>
1. <span data-ttu-id="7a10e-133">Klõpsake suvandit Funktsioonid.</span><span class="sxs-lookup"><span data-stu-id="7a10e-133">Click Functions.</span></span>
2. <span data-ttu-id="7a10e-134">Klõpsake valikut Toote sissetulek.</span><span class="sxs-lookup"><span data-stu-id="7a10e-134">Click Product receipt.</span></span>
3. <span data-ttu-id="7a10e-135">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="7a10e-135">Click OK.</span></span>


