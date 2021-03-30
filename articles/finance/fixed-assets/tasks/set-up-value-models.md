---
title: Väärtusmudelite seadistamine
description: See protseduur näitab, kuidas luua uut põhivara raamatut ja seostada seda põhivaragrupiga.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetBookTable, AssetGroupBookSetup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 88c6ee10fa0a208f0946cf0f4e6bb73cb61203a4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213528"
---
# <a name="set-up-value-models"></a><span data-ttu-id="0a51b-103">Väärtusmudelite seadistamine</span><span class="sxs-lookup"><span data-stu-id="0a51b-103">Set up value models</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0a51b-104">See protseduur näitab, kuidas luua uut põhivara raamatut ja seostada seda põhivaragrupiga.</span><span class="sxs-lookup"><span data-stu-id="0a51b-104">This procedure shows you to how create a new fixed asset book and associate it with a fixed asset group.</span></span> <span data-ttu-id="0a51b-105">See kasutab USMF-i juriidilise isiku puhul raamatupidaja rolli ja demoandmeid.</span><span class="sxs-lookup"><span data-stu-id="0a51b-105">It uses the accountant role and demo data for the USMF legal entity.</span></span>


## <a name="create-a-book"></a><span data-ttu-id="0a51b-106">Raamatu loomine</span><span class="sxs-lookup"><span data-stu-id="0a51b-106">Create a book</span></span>
1. <span data-ttu-id="0a51b-107">Avage Põhivarad > Seadistus > Raamatud.</span><span class="sxs-lookup"><span data-stu-id="0a51b-107">Go to Fixed assets > Setup > Books.</span></span>
2. <span data-ttu-id="0a51b-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="0a51b-108">Click New.</span></span>
3. <span data-ttu-id="0a51b-109">Tippige väärtus väljale Raamat.</span><span class="sxs-lookup"><span data-stu-id="0a51b-109">In the Book field, type a value.</span></span>
4. <span data-ttu-id="0a51b-110">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="0a51b-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="0a51b-111">Kui Kulumiarvestus on valitud, kaasatakse seostatud vara raamat kulumisoovitustesse.</span><span class="sxs-lookup"><span data-stu-id="0a51b-111">If Calculate depreciation is selected, the associated asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="0a51b-112">Kui see pole valitud, ei amortiseerita vara raamatut automaatselt.</span><span class="sxs-lookup"><span data-stu-id="0a51b-112">If it is not selected, the asset book will not be automatically depreciated.</span></span>  
5. <span data-ttu-id="0a51b-113">Tehke väljal Kulumiarvestus valik Jah.</span><span class="sxs-lookup"><span data-stu-id="0a51b-113">Select Yes in the Calculate depreciation field.</span></span>
6. <span data-ttu-id="0a51b-114">Valige või sisestage väärtus väljal Kulumireeglid.</span><span class="sxs-lookup"><span data-stu-id="0a51b-114">In the Depreciation profile field, enter or select a value.</span></span>
    * <span data-ttu-id="0a51b-115">Alternatiivne kulumireegel on tuntud ka kui kulumi ümberlülitusmeetod.</span><span class="sxs-lookup"><span data-stu-id="0a51b-115">An alternative depreciation profile is also known as a switchover method of depreciation.</span></span> <span data-ttu-id="0a51b-116">Kulumisoovitus lülitub sellele reeglile, kui alternatiivne reegel arvutab kulumi summa, mis on vaikimisi kulumireegliga võrdne või sellest suurem.</span><span class="sxs-lookup"><span data-stu-id="0a51b-116">The depreciation proposal will switch to this profile when the alternative profile calculates a depreciation amount that is equal to or greater than the default depreciation profile.</span></span>  
    * <span data-ttu-id="0a51b-117">Plaaniväliseid kulumireegleid kasutatakse vara täiendava kulumi arvestamiseks ebatavalistes olukordades.</span><span class="sxs-lookup"><span data-stu-id="0a51b-117">The Extraordinary depreciation profile is used for additional depreciation of an asset in unusual circumstances.</span></span> <span data-ttu-id="0a51b-118">Näiteks võite seda kasutada loodusõnnetusest tuleneva kulumi registreerimiseks.</span><span class="sxs-lookup"><span data-stu-id="0a51b-118">For example, you might use this to record depreciation that results from a natural disaster.</span></span>  
    * <span data-ttu-id="0a51b-119">Kui valitud on suvand Loo kulumi korrigeerimised koos aluse korrigeerimistega, luuakse kulumi korrigeerimised automaatselt, kui vara väärtust värskendatakse.</span><span class="sxs-lookup"><span data-stu-id="0a51b-119">If Create depreciation adjustments with basis adjustments is selected, depreciation adjustments will be automatically created when the value of the asset is updated.</span></span> <span data-ttu-id="0a51b-120">Kui see valitud pole, mõjutab värskendatud vara väärtus ainult kulumi arvutusi alates tänasest.</span><span class="sxs-lookup"><span data-stu-id="0a51b-120">If it is not selected, the updated asset value will only affect depreciation calculations going forward.</span></span>  
7. <span data-ttu-id="0a51b-121">Tehke väljal Loo kulumi korrigeerimised koos aluse korrigeerimistega valik Jah.</span><span class="sxs-lookup"><span data-stu-id="0a51b-121">Select Yes in the Create depreciation adjustments with basis adjustments field.</span></span>
    * <span data-ttu-id="0a51b-122">Vaikimisi sisestatakse põhivara raamatu kanded pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="0a51b-122">By default, fixed asset book transactions will post to the general ledger.</span></span> <span data-ttu-id="0a51b-123">Raamatu sisestamise pearaamatusse saab keelata, määrates valiku Sisesta pearaamatusse väärtuseks Ei.</span><span class="sxs-lookup"><span data-stu-id="0a51b-123">You can disable posting to the general ledger for the book by setting the Post to general ledger field to No.</span></span> <span data-ttu-id="0a51b-124">Raamatuid, mida pearaamatusse ei sisestata, kasutatakse tavaliselt maksuaruandluse jaoks.</span><span class="sxs-lookup"><span data-stu-id="0a51b-124">Books that do not post to the general ledger are typically used for tax reporting purposes.</span></span> <span data-ttu-id="0a51b-125">See lisab paindlikkust vararegistri varasemate kannete kustutamisel, kuna neid pole pearaamatuga kooskõlastatud.</span><span class="sxs-lookup"><span data-stu-id="0a51b-125">This gives you additional flexibility to delete historical transactions for the asset book because they have not been committed to the general ledger.</span></span>  
    * <span data-ttu-id="0a51b-126">Sisestamiskihiks on vaikimisi Praegune kiht, kui raamat sisestatakse pearaamatusse, ja Pole, kui seda pearaamatusse ei sisestata.</span><span class="sxs-lookup"><span data-stu-id="0a51b-126">The Posting layer defaults to the Current layer if the book posts to general ledger, and None if it does not post to general ledger.</span></span> <span data-ttu-id="0a51b-127">Värskendage sisestamiskihti, kui vajate selle raamatu kannete sisestamist teise kihti.</span><span class="sxs-lookup"><span data-stu-id="0a51b-127">Update Posting layer if you need transactions for this book to be posted to a different layer.</span></span>  
8. <span data-ttu-id="0a51b-128">Sisestage või valige väärtus väljal Kalender.</span><span class="sxs-lookup"><span data-stu-id="0a51b-128">In the Calendar field, enter or select a value.</span></span>
    * <span data-ttu-id="0a51b-129">Tuletatud raamatud sisestavad kandeid korraga erinevatesse raamatutesse.</span><span class="sxs-lookup"><span data-stu-id="0a51b-129">Derived books will post transactions to different books at the same time.</span></span> <span data-ttu-id="0a51b-130">Loote kanded peamises raamatus ja sisestamise ajal sisestatakse kande täpne koopia tuletatud raamatusse.</span><span class="sxs-lookup"><span data-stu-id="0a51b-130">You create the transactions with the primary book and during posting, an exact copy of the transaction is posted to the derived book.</span></span> <span data-ttu-id="0a51b-131">Tuletatud raamatu kandeid ei arvutata ümber, seega ei tohiks seda kulumikannete jaoks kasutada.</span><span class="sxs-lookup"><span data-stu-id="0a51b-131">There is no recalculation with derived book transactions, so it should not be used for depreciation transactions.</span></span>  

## <a name="associate-the-book-with-a-fixed-asset-group"></a><span data-ttu-id="0a51b-132">Raamatu seostamine põhivaragrupiga</span><span class="sxs-lookup"><span data-stu-id="0a51b-132">Associate the book with a fixed asset group</span></span>
1. <span data-ttu-id="0a51b-133">Klõpsake suvandit Põhivaragrupid.</span><span class="sxs-lookup"><span data-stu-id="0a51b-133">Click Fixed asset groups.</span></span>
2. <span data-ttu-id="0a51b-134">Sisestage väärtus väljale Põhivara grupp või valige sellelt väljalt.</span><span class="sxs-lookup"><span data-stu-id="0a51b-134">In the Fixed asset group field, enter or select a value.</span></span>
3. <span data-ttu-id="0a51b-135">Sisestage number väljale Kasutusiga.</span><span class="sxs-lookup"><span data-stu-id="0a51b-135">In the Service life field, enter a number.</span></span>
    * <span data-ttu-id="0a51b-136">Pange tähele, et väärtus Kulumiperioodid arvutatakse pärast kasutusea seadistamist.</span><span class="sxs-lookup"><span data-stu-id="0a51b-136">Note that Depreciation periods is calculated after setting the Service life.</span></span>  
    * <span data-ttu-id="0a51b-137">Kulumiarvestusreeglit saab maksuarvestuse jaoks vajalikul viisil seadistada.</span><span class="sxs-lookup"><span data-stu-id="0a51b-137">You are able to set the depreciation convention as required for tax purposes.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]