--- 
title: Vabas vormis arve loomine
description: "Selles tegevuse juhises näitlikustatakse, kuidas vabas vormis arvet luua."
author: mikefalkner
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 33324a9b95026600bcc6facb9c22a04fd2e323c8
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-free-text-invoice"></a><span data-ttu-id="cbf53-103">Vabas vormis arve loomine</span><span class="sxs-lookup"><span data-stu-id="cbf53-103">Create a free text invoice</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cbf53-104">Selles tegevuse juhises näitlikustatakse, kuidas vabas vormis arvet luua.</span><span class="sxs-lookup"><span data-stu-id="cbf53-104">This task guide demonstrates creating a free text invoice.</span></span> <span data-ttu-id="cbf53-105">See ülesanne kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="cbf53-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="cbf53-106">Avage Müügireskontro > Arved > Kõik vabas vormis arved.</span><span class="sxs-lookup"><span data-stu-id="cbf53-106">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="cbf53-107">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="cbf53-107">Click New.</span></span>
3. <span data-ttu-id="cbf53-108">Valige väärtus väljal Kliendi konto.</span><span class="sxs-lookup"><span data-stu-id="cbf53-108">In the Customer account field, select a value.</span></span>
    * <span data-ttu-id="cbf53-109">Arvekonto on vaikimisi sama konto, mida kasutatakse kliendikontona.</span><span class="sxs-lookup"><span data-stu-id="cbf53-109">The invoice account will default to the same account used for the customer account.</span></span>   
    * <span data-ttu-id="cbf53-110">Kui arve pole sisestatud, algab raamatupidamisolek sõnaga „Pooleli”.</span><span class="sxs-lookup"><span data-stu-id="cbf53-110">The accounting status starts with In process if the invoice is not posted.</span></span>   
    * <span data-ttu-id="cbf53-111">Pärast arve sisestamist määratakse arve number.</span><span class="sxs-lookup"><span data-stu-id="cbf53-111">The invoice number will be assigned when the invoice is posted.</span></span>  
    * <span data-ttu-id="cbf53-112">Kui kasutate SEPA lubasid, täidetakse kliendikonto valimisel otsekorralduse luba loaga automaatselt.</span><span class="sxs-lookup"><span data-stu-id="cbf53-112">If you are using SEPA mandates, the direct debit mandate will be automatically populated with a mandate when you select the customer account.</span></span>  
4. <span data-ttu-id="cbf53-113">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="cbf53-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="cbf53-114">Määrake valik kontonumber ilma dimensioonideta väljal Põhikonto.</span><span class="sxs-lookup"><span data-stu-id="cbf53-114">In the Main account field, specify an account number without dimensions.</span></span>
    * <span data-ttu-id="cbf53-115">Samuti saate konto leidmiseks kasutada otsingut, sisestades põhikonto kohta ühe või mitu märki.</span><span class="sxs-lookup"><span data-stu-id="cbf53-115">You can also enter one or more characters for the main account and use the lookup to find your account.</span></span> <span data-ttu-id="cbf53-116">Selles juhises saate hiljem ka dimensioonid sisestada.</span><span class="sxs-lookup"><span data-stu-id="cbf53-116">You will enter dimensions later on in this guide.</span></span>  
6. <span data-ttu-id="cbf53-117">Põhikontole dimensioonide lisamiseks laiendage kiirkaart Rea üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="cbf53-117">Expand the Line details fasttab so you can add dimensions to your main account.</span></span>
7. <span data-ttu-id="cbf53-118">Klõpsake vahekaarti Finantsdimensiooni rida.</span><span class="sxs-lookup"><span data-stu-id="cbf53-118">Click the Financial dimensions line tab.</span></span>
    * <span data-ttu-id="cbf53-119">Dimensioonid on ette nähtud ainult valitud reale.</span><span class="sxs-lookup"><span data-stu-id="cbf53-119">The dimensions are for the selected line only.</span></span>    
    * <span data-ttu-id="cbf53-120">Käibemaksugrupp täidetakse kliendilt.</span><span class="sxs-lookup"><span data-stu-id="cbf53-120">The sales tax group is populated from the customer.</span></span> <span data-ttu-id="cbf53-121">Kui kliendil ei ole käibemaksugruppi, kasutatakse põhikonto käibemaksugruppi.</span><span class="sxs-lookup"><span data-stu-id="cbf53-121">If the customer does not have a sales tax group, the sales tax group from the main account is used.</span></span>  
    * <span data-ttu-id="cbf53-122">Kauba käibemaksugrupp täidetakse põhikontolt.</span><span class="sxs-lookup"><span data-stu-id="cbf53-122">The items sales tax group is populated from the main account.</span></span> <span data-ttu-id="cbf53-123">Kui põhikontol pole kauba käibemaksugruppi, kasutatakse pearaamatu käibemaksuparameetrite lehel olevat kauba käibemaksugruppi.</span><span class="sxs-lookup"><span data-stu-id="cbf53-123">If the main account does not have a item sales tax group, then the item sales tax group in the General ledger sales tax parameters is used.</span></span>    
8. <span data-ttu-id="cbf53-124">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="cbf53-124">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="cbf53-125">Kogus on valikuline.</span><span class="sxs-lookup"><span data-stu-id="cbf53-125">The quantity is optional.</span></span>  
9. <span data-ttu-id="cbf53-126">Sisestage arv väljale Ühiku hind.</span><span class="sxs-lookup"><span data-stu-id="cbf53-126">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="cbf53-127">Ühiku hind on valikuline.</span><span class="sxs-lookup"><span data-stu-id="cbf53-127">The unit price is optional.</span></span>  
    * <span data-ttu-id="cbf53-128">Summa arvutamiseks korrutatakse kogus ühikuhinnaga.</span><span class="sxs-lookup"><span data-stu-id="cbf53-128">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="cbf53-129">Teil on ka võimalus see arvutus tühistada ja sisestada summa.</span><span class="sxs-lookup"><span data-stu-id="cbf53-129">However, you can override that calculation and enter an amount.</span></span>  
10. <span data-ttu-id="cbf53-130">Arve jaoks arvutatud käibemaksu kuvamiseks klõpsake valikut Käibemaks.</span><span class="sxs-lookup"><span data-stu-id="cbf53-130">Click on Sales tax to view the sales tax calculated for your invoice.</span></span>
    * <span data-ttu-id="cbf53-131">Käibemaksusummasid saate vaadata sellelt lehelt või tühistada summad vahekaardil Korrigeerimine.</span><span class="sxs-lookup"><span data-stu-id="cbf53-131">View the sales tax amounts in this page or you can override the amounts on the Adjustment tab.</span></span>  
11. <span data-ttu-id="cbf53-132">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="cbf53-132">Click OK.</span></span>
12. <span data-ttu-id="cbf53-133">Arvele tasu lisamiseks klõpsake valikut Tasud.</span><span class="sxs-lookup"><span data-stu-id="cbf53-133">Click Charges to add a charge to your invoice.</span></span> 
13. <span data-ttu-id="cbf53-134">Sisestage väärtus väljale Tasukood.</span><span class="sxs-lookup"><span data-stu-id="cbf53-134">In the Charges code field, type a value.</span></span>
14. <span data-ttu-id="cbf53-135">Sisestage arv väljale Tasude väärtus.</span><span class="sxs-lookup"><span data-stu-id="cbf53-135">In the Charges value field, enter a number.</span></span>
15. <span data-ttu-id="cbf53-136">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="cbf53-136">Close the page.</span></span>
16. <span data-ttu-id="cbf53-137">Lõpparve üksikasjade ja kogusummade kuvamiseks klõpsake valikut Kogusummad.</span><span class="sxs-lookup"><span data-stu-id="cbf53-137">Click Totals to view the summary invoice details and totals.</span></span>
17. <span data-ttu-id="cbf53-138">Klõpsake valikut Sule.</span><span class="sxs-lookup"><span data-stu-id="cbf53-138">Click Close.</span></span>
18. <span data-ttu-id="cbf53-139">Arve sisestamiseks klõpsake nuppu Sisesta.</span><span class="sxs-lookup"><span data-stu-id="cbf53-139">Click Post to post the invoice.</span></span> <span data-ttu-id="cbf53-140">Enne sisestamist saate toimingu tühistada.</span><span class="sxs-lookup"><span data-stu-id="cbf53-140">You will be able to cancel before you post.</span></span>
    * <span data-ttu-id="cbf53-141">Arve printimisaja muutmiseks klõpsake nuppu Praegu, kui soovite igat arvet pärast selle uuendamist printida, või nuppu Pärast, kui soovite printida pärast kõikide arvete uuendamist.</span><span class="sxs-lookup"><span data-stu-id="cbf53-141">To change the timing of your invoice printing:  Select Current to print each invoice as it is updated   or  Select After to print after all invoices have been updated.</span></span>  
    * <span data-ttu-id="cbf53-142">Kui soovite muuta, kuidas kliendi krediidilimiiti enne sisestamist kontrollitakse, muutke suvandit Krediidilimiidi tüüp.</span><span class="sxs-lookup"><span data-stu-id="cbf53-142">If you want to change how the customer's credit limit is checked before posting, change the Credit limit type.</span></span>  
    * <span data-ttu-id="cbf53-143">Kui soovite arve printida, valige Jah.</span><span class="sxs-lookup"><span data-stu-id="cbf53-143">If you want to print the invoice, select Yes.</span></span>  
    * <span data-ttu-id="cbf53-144">Kui soovite arve sisestada, valige Jah.</span><span class="sxs-lookup"><span data-stu-id="cbf53-144">If you want to post the invoice, select Yes.</span></span> <span data-ttu-id="cbf53-145">Saate arve ilma sisestamata printida.</span><span class="sxs-lookup"><span data-stu-id="cbf53-145">You can print the invoice without posting.</span></span>  
19. <span data-ttu-id="cbf53-146">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="cbf53-146">Click OK.</span></span>


