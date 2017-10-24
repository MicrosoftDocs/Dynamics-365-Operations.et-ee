--- 
title: "Müügilepingute sisestamine"
description: "See protseduur näitab teile, kuidas koostada müügilepingut, mis kohustab ühe teie klientidest ostma teatud aja jooksul toodet kokkulepitud summas, saades vastutasuks erisoodustusi."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 8c11164f7edb8e05b93f3c58b9707c0bf2482228
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---
# <a name="enter-sales-agreements"></a><span data-ttu-id="a9f1f-103">Müügilepingute sisestamine</span><span class="sxs-lookup"><span data-stu-id="a9f1f-103">Enter sales agreements</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a9f1f-104">See protseduur näitab, kuidas luua müügilepingut, mis kohustab ühte teie klient ostma toode</span><span class="sxs-lookup"><span data-stu-id="a9f1f-104">This procedure shows you how to create a sales agreement that commits one of your customers to buy a product for an</span></span>

<span data-ttu-id="a9f1f-105">kokkulepitud summa eest teatud aja möödudes, saades vastutasuks eriallahindlusi.</span><span class="sxs-lookup"><span data-stu-id="a9f1f-105">agreed amount over time in exchange for special discounts.</span></span> <span data-ttu-id="a9f1f-106">Saate seda protseduuri käitada demoettevõtte USMF-i andmetega või oma andmetega.</span><span class="sxs-lookup"><span data-stu-id="a9f1f-106">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-sales-agreement-header"></a><span data-ttu-id="a9f1f-107">Müügilepingu päise seadistus</span><span class="sxs-lookup"><span data-stu-id="a9f1f-107">Set up sales agreement header</span></span>
1. <span data-ttu-id="a9f1f-108">Avage Müük ja turundus > Müügilepingud > Müügilepingud.</span><span class="sxs-lookup"><span data-stu-id="a9f1f-108">Go to Sales and marketing > Sales agreements > Sales agreements.</span></span>
2. <span data-ttu-id="a9f1f-109">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="a9f1f-109">Click New.</span></span>
3. <span data-ttu-id="a9f1f-110">Klõpsake väljal Kliendi konto otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="a9f1f-110">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="a9f1f-111">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="a9f1f-111">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="a9f1f-112">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="a9f1f-112">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="a9f1f-113">Klõpsake väljal Sales agreement classification (Müügilepingu klassifikatsioon) otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="a9f1f-113">In the Sales agreement classification field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="a9f1f-114">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="a9f1f-114">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="a9f1f-115">Laiendage jaotist Üldine.</span><span class="sxs-lookup"><span data-stu-id="a9f1f-115">Expand the General section.</span></span>
9. <span data-ttu-id="a9f1f-116">Tehke väljal Default commitment (Vaikimisi kohustus) valik Product value commitment (Toote väärtuse kohustus).</span><span class="sxs-lookup"><span data-stu-id="a9f1f-116">In the Default commitment field, select 'Product value commitment'.</span></span>
    * <span data-ttu-id="a9f1f-117">Kohustuse tüüp on kohustuslik kriteerium, mis tuleb leppele määrata, et määrata kindlaks, kuidas lepingut täidetakse.</span><span class="sxs-lookup"><span data-stu-id="a9f1f-117">A commitment type is a mandatory criterion that you must assign to the agreement to define how the agreement contract will be fulfilled.</span></span> <span data-ttu-id="a9f1f-118">Neli eelmääratud tüüpi võimaldavad teil määrata kliendi kohustuse eesmärgi koguse või väärtuse kujul.</span><span class="sxs-lookup"><span data-stu-id="a9f1f-118">The four predefined types let you set up the customer's commitment target, expressed as a quantity or a value.</span></span> <span data-ttu-id="a9f1f-119">Koguse kohustusetüüpi saab rakendada ainult kindlale tootele, kuid väärtusel põhinevad tüübid rakenduvad nii kindlate kui määramata toodete müügile.</span><span class="sxs-lookup"><span data-stu-id="a9f1f-119">The quantity commitment type can only be applied to a specific product, but the value-based types are applicable to sales of both specific and non-specific products.</span></span>  
10. <span data-ttu-id="a9f1f-120">Väljal Expiration date (Aegumiskuupäev) määrake kuupäev tulevikus, mil soovite, et lepe aeguks.</span><span class="sxs-lookup"><span data-stu-id="a9f1f-120">In the Expiration date field, set the date to a future date when you want the agreement to expire.</span></span>
11. <span data-ttu-id="a9f1f-121">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="a9f1f-121">Click OK.</span></span>

## <a name="set-up-product-value-commitment-lines"></a><span data-ttu-id="a9f1f-122">Toote väärtuse kohustuse ridade seadistus</span><span class="sxs-lookup"><span data-stu-id="a9f1f-122">Set up product value commitment lines</span></span>
1. <span data-ttu-id="a9f1f-123">Klõpsake käsku Lisa rida.</span><span class="sxs-lookup"><span data-stu-id="a9f1f-123">Click Add line.</span></span>
2. <span data-ttu-id="a9f1f-124">Klõpsake väljal Kaubakood otsingu avamiseks ripploendi nuppu.</span><span class="sxs-lookup"><span data-stu-id="a9f1f-124">In the Item number field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="a9f1f-125">Otsige loendist ja valige soovitud kirje.</span><span class="sxs-lookup"><span data-stu-id="a9f1f-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="a9f1f-126">Klõpsake loendis valitud real olevat linki.</span><span class="sxs-lookup"><span data-stu-id="a9f1f-126">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="a9f1f-127">Kohustuse tüüp, mille olete lepingu jaoks valinud, mõjutab teavet, mida saate lepingu ridadele sisestada.</span><span class="sxs-lookup"><span data-stu-id="a9f1f-127">The type of commitment that you have chosen for the agreement affects the kind of information you can enter for the agreement lines.</span></span> <span data-ttu-id="a9f1f-128">Näiteks tuleb teil väärtusel põhineva lepingu korral täpsustada kogu netosummat (kokkulepitud valuutas), mille väärtuses klient kohustub teilt kaupa ostma.</span><span class="sxs-lookup"><span data-stu-id="a9f1f-128">For example, for a value-based agreement you must specify the total net amount (in the agreed currency) for which the customer commits to buys goods from you.</span></span> <span data-ttu-id="a9f1f-129">Selles näites ei ole koguse ja ühiku väljad real kättesaadavad, kuna koostate lepingu, millele vastavalt tuleb kliendil osta toodet kindlas väärtuses.</span><span class="sxs-lookup"><span data-stu-id="a9f1f-129">In this example the Quantity and Unit fields on the line are unavailable because you’re creating an agreement for the customer to buy a specific value of a product.</span></span>   
5. <span data-ttu-id="a9f1f-130">Sisestage väljale Net amount (Netosumma) rahasumma, mille väärtuses klient on kohustunud ostma.</span><span class="sxs-lookup"><span data-stu-id="a9f1f-130">In the Net amount field, enter the monetary amount that the customer has committed to buying.</span></span>
6. <span data-ttu-id="a9f1f-131">Väljale Discount percent (Allahindluse protsent) sisestage protsentuaalne väärtus, mis rakendub kliendi selle leppega seotud müügitellimuse ridadele.</span><span class="sxs-lookup"><span data-stu-id="a9f1f-131">In the Discount percent field, enter a percentage value that will apply to the customer's sales order lines that are linked to this agreement.</span></span>
7. <span data-ttu-id="a9f1f-132">Laiendage jaotis Rea üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="a9f1f-132">Expand the Line details section.</span></span>
8. <span data-ttu-id="a9f1f-133">Valige Yes (Jah) väljal Max is enforced (Maksimum rakendatud).</span><span class="sxs-lookup"><span data-stu-id="a9f1f-133">Select Yes in the Max is enforced field.</span></span>
    * <span data-ttu-id="a9f1f-134">Valik Max is enforced (Rakendatakse maksimum) tähendab, et müügitellimuse kõigi ridade, mis kasutavad kohustuse erihindu, allahindlusi ja/või maksetingimusi, kogusumma ei tohi ületada kohustuses täpsustatud summat.</span><span class="sxs-lookup"><span data-stu-id="a9f1f-134">Selecting Max is enforced means that the total amount of all the sales order lines that use the commitment's special prices, discounts and/or payment terms must not exceed the amount specified on the commitment.</span></span>  
    * <span data-ttu-id="a9f1f-135">Väljastussummade miinimum ja maksimum määravad väärtuste vahemiku, mis tuleb iga müügitellimusega, mis valitud lepingut kasutab, müüa.</span><span class="sxs-lookup"><span data-stu-id="a9f1f-135">The minimum and maximum release amounts specify a range of values that must be sold on each sales order that uses the selected agreement.</span></span>   
9. <span data-ttu-id="a9f1f-136">Laiendage müügilepingu päiseosa.</span><span class="sxs-lookup"><span data-stu-id="a9f1f-136">Expand the Sales agreement header section.</span></span>
    * <span data-ttu-id="a9f1f-137">Kui leppe olekuks on määratud Effective (Kehtiv), ei saa müügitellimusi selle leppega seostada ja seetõttu ei osale need selle leppe täitmises.</span><span class="sxs-lookup"><span data-stu-id="a9f1f-137">Unless the status of the agreement is set to Effective, sales orders cannot be associated with the agreement and can therefore not contribute to the fulfilment of that agreement.</span></span> <span data-ttu-id="a9f1f-138">Selles etapis saate olekut käsitsi muuta.</span><span class="sxs-lookup"><span data-stu-id="a9f1f-138">You can change the status manually at this stage.</span></span> <span data-ttu-id="a9f1f-139">Siiski muudetaks olekut tavaliselt siis, kui leppe kliendi jaoks kinnitate.</span><span class="sxs-lookup"><span data-stu-id="a9f1f-139">However, the status would normally be changed when you confirm the agreement for the customer.</span></span>  
10. <span data-ttu-id="a9f1f-140">Klõpsake tegumiribal valikut Müügileping.</span><span class="sxs-lookup"><span data-stu-id="a9f1f-140">On the Action Pane, click Sales agreement.</span></span>
11. <span data-ttu-id="a9f1f-141">Klõpsake suvandit Kinnitus.</span><span class="sxs-lookup"><span data-stu-id="a9f1f-141">Click Confirmation.</span></span>
    * <span data-ttu-id="a9f1f-142">Veenduge, et valiku Mark agreement as effective (Märgi lepe kehtivaks) all oleks märgitud Yes (Jah).</span><span class="sxs-lookup"><span data-stu-id="a9f1f-142">Make sure that the Mark agreement as effective option is set to Yes.</span></span>  
12. <span data-ttu-id="a9f1f-143">Tehke väljal Print report (Aruande printimine) valik Yes (Jah).</span><span class="sxs-lookup"><span data-stu-id="a9f1f-143">Select Yes in the Print report field.</span></span>
13. <span data-ttu-id="a9f1f-144">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="a9f1f-144">Click OK.</span></span>
14. <span data-ttu-id="a9f1f-145">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="a9f1f-145">Close the page.</span></span>
    * <span data-ttu-id="a9f1f-146">See leping kehtib nüüd ja saate alustada kliendi tellimuste lepinguga seostamist kooskõlastatud sihtmärgiga tasakaalustamiseks.</span><span class="sxs-lookup"><span data-stu-id="a9f1f-146">The agreement is now effective and you can start linking the customer's orders to the agreement, to offset against the committed target.</span></span>  


