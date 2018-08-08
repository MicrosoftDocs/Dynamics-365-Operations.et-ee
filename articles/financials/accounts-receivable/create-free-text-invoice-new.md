--- 
title: Vabas vormis arve loomine
description: See artikkel kirjeldab, kuidas luua vabas vormis arveid.
author: mikefalkner
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: e6f89a6d77ff8e1cd88632df0d9a72915086ee1e
ms.contentlocale: et-ee
ms.lasthandoff: 08/07/2018

---

# <a name="create-a-free-text-invoice"></a><span data-ttu-id="ce1c3-103">Vabas vormis arve loomine</span><span class="sxs-lookup"><span data-stu-id="ce1c3-103">Create a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce1c3-104">See artikkel kirjeldab, kuidas luua vabas vormis arveid.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-104">This article demonstrates how to create a free text invoice.</span></span> <span data-ttu-id="ce1c3-105">Selle protseduuri jaoks kasutage demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-105">For this procedure, use the USMF demo company.</span></span>

## <a name="create-a-free-text-invoice"></a><span data-ttu-id="ce1c3-106">Vabas vormis arve loomine</span><span class="sxs-lookup"><span data-stu-id="ce1c3-106">Create a free text invoice</span></span>

1. <span data-ttu-id="ce1c3-107">Avage Müügireskontro > Arved > Kõik vabas vormis arved.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-107">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="ce1c3-108">Klõpsake valikut Uus.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-108">Click New.</span></span>
3. <span data-ttu-id="ce1c3-109">Valige väärtus väljal Kliendi konto.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-109">In the Customer account field, select a value.</span></span>
    * <span data-ttu-id="ce1c3-110">Arvekonto on vaikimisi sama konto, mida kasutatakse kliendikontona.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-110">The invoice account will default to the same account used for the customer account.</span></span>   
    * <span data-ttu-id="ce1c3-111">Kui arve pole sisestatud, algab raamatupidamisolek sõnaga „Pooleli”.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-111">The accounting status starts with In process if the invoice is not posted.</span></span>   
    * <span data-ttu-id="ce1c3-112">Pärast arve sisestamist määratakse arve number.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-112">The invoice number will be assigned when the invoice is posted.</span></span>  
    * <span data-ttu-id="ce1c3-113">Kui kasutate SEPA lubasid, täidetakse kliendikonto valimisel otsekorralduse luba loaga automaatselt.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-113">If you are using SEPA mandates, the direct debit mandate will be automatically populated with a mandate when you select the customer account.</span></span>  
4. <span data-ttu-id="ce1c3-114">Sisestage väljale Kirjeldus soovitud väärtus.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-114">In the Description field, type a value.</span></span>
5. <span data-ttu-id="ce1c3-115">Määrake valik kontonumber ilma dimensioonideta väljal Põhikonto.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-115">In the Main account field, specify an account number without dimensions.</span></span>
    * <span data-ttu-id="ce1c3-116">Samuti saate konto leidmiseks kasutada otsingut, sisestades põhikonto kohta ühe või mitu märki.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-116">You can also enter one or more characters for the main account and use the lookup to find your account.</span></span> <span data-ttu-id="ce1c3-117">Selles juhises saate hiljem ka dimensioonid sisestada.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-117">You will enter dimensions later on in this guide.</span></span>  
6. <span data-ttu-id="ce1c3-118">Põhikontole dimensioonide lisamiseks laiendage kiirkaart Rea üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-118">Expand the Line details fasttab so you can add dimensions to your main account.</span></span>
7. <span data-ttu-id="ce1c3-119">Klõpsake vahekaarti Finantsdimensiooni rida.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-119">Click the Financial dimensions line tab.</span></span>
    * <span data-ttu-id="ce1c3-120">Dimensioonid on ette nähtud ainult valitud reale.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-120">The dimensions are for the selected line only.</span></span>    
    * <span data-ttu-id="ce1c3-121">Käibemaksugrupp täidetakse kliendilt.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-121">The sales tax group is populated from the customer.</span></span> <span data-ttu-id="ce1c3-122">Kui kliendil ei ole käibemaksugruppi, kasutatakse põhikonto käibemaksugruppi.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-122">If the customer does not have a sales tax group, the sales tax group from the main account is used.</span></span>  
    * <span data-ttu-id="ce1c3-123">Kauba käibemaksugrupp täidetakse põhikontolt.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-123">The items sales tax group is populated from the main account.</span></span> <span data-ttu-id="ce1c3-124">Kui põhikontol pole kauba käibemaksugruppi, kasutatakse pearaamatu käibemaksuparameetrite lehel olevat kauba käibemaksugruppi.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-124">If the main account does not have an item sales tax group, then the item sales tax group in the General ledger sales tax parameters is used.</span></span>    
8. <span data-ttu-id="ce1c3-125">Sisestage arv väljale Kogus.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="ce1c3-126">Kogus on valikuline.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-126">The quantity is optional.</span></span>  
9. <span data-ttu-id="ce1c3-127">Sisestage arv väljale Ühiku hind.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-127">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="ce1c3-128">Ühiku hind on valikuline.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-128">The unit price is optional.</span></span>  
    * <span data-ttu-id="ce1c3-129">Summa arvutamiseks korrutatakse kogus ühikuhinnaga.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-129">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="ce1c3-130">Teil on ka võimalus see arvutus tühistada ja sisestada summa.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-130">However, you can override that calculation and enter an amount.</span></span>  
10. <span data-ttu-id="ce1c3-131">Arve jaoks arvutatud käibemaksu kuvamiseks klõpsake valikut Käibemaks.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-131">Click on Sales tax to view the sales tax calculated for your invoice.</span></span>
    * <span data-ttu-id="ce1c3-132">Käibemaksusummasid saate vaadata sellelt lehelt või tühistada summad vahekaardil Korrigeerimine.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-132">View the sales tax amounts in this page or you can override the amounts on the Adjustment tab.</span></span>  
11. <span data-ttu-id="ce1c3-133">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-133">Click OK.</span></span>
12. <span data-ttu-id="ce1c3-134">Arvele tasu lisamiseks klõpsake valikut Tasud.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-134">Click Charges to add a charge to your invoice.</span></span> 
13. <span data-ttu-id="ce1c3-135">Sisestage väärtus väljale Tasukood.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-135">In the Charges code field, type a value.</span></span>
14. <span data-ttu-id="ce1c3-136">Sisestage arv väljale Tasude väärtus.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-136">In the Charges value field, enter a number.</span></span>
15. <span data-ttu-id="ce1c3-137">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-137">Close the page.</span></span>
16. <span data-ttu-id="ce1c3-138">Lõpparve üksikasjade ja kogusummade kuvamiseks klõpsake valikut Kogusummad.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-138">Click Totals to view the summary invoice details and totals.</span></span>
17. <span data-ttu-id="ce1c3-139">Klõpsake valikut Sule.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-139">Click Close.</span></span>
18. <span data-ttu-id="ce1c3-140">Arve sisestamiseks klõpsake nuppu Sisesta.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-140">Click Post to post the invoice.</span></span> <span data-ttu-id="ce1c3-141">Enne sisestamist saate toimingu tühistada.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-141">You will be able to cancel before you post.</span></span>
    * <span data-ttu-id="ce1c3-142">Arve printimisaja muutmiseks klõpsake nuppu Praegu, kui soovite igat arvet pärast selle uuendamist printida, või nuppu Pärast, kui soovite printida pärast kõikide arvete uuendamist.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-142">To change the timing of your invoice printing:  Select Current to print each invoice as it is updated   or  Select After to print after all invoices have been updated.</span></span>  
    * <span data-ttu-id="ce1c3-143">Kui soovite muuta, kuidas kliendi krediidilimiiti enne sisestamist kontrollitakse, muutke suvandit Krediidilimiidi tüüp.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-143">If you want to change how the customer's credit limit is checked before posting, change the Credit limit type.</span></span>  
    * <span data-ttu-id="ce1c3-144">Kui soovite arve printida, valige Jah.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-144">If you want to print the invoice, select Yes.</span></span>  
    * <span data-ttu-id="ce1c3-145">Kui soovite arve sisestada, valige Jah.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-145">If you want to post the invoice, select Yes.</span></span> <span data-ttu-id="ce1c3-146">Saate arve ilma sisestamata printida.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-146">You can print the invoice without posting.</span></span>  
19. <span data-ttu-id="ce1c3-147">Klõpsake nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-147">Click OK.</span></span>

## <a name="copy-lines"></a><span data-ttu-id="ce1c3-148">Kopeeri read</span><span class="sxs-lookup"><span data-stu-id="ce1c3-148">Copy lines</span></span>
<span data-ttu-id="ce1c3-149">Vabas vormis arve ridade kopeerimiseks valige üks või mitu rida ja klõpsake nuppu Kopeeri valitud read.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-149">To copy lines on the free text invoice, select one or more lines and then click Copy selected lines.</span></span> <span data-ttu-id="ce1c3-150">Saate määrata soovitud koopiate arvu ning saate ka kopeerida märkusi ja manused.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-150">You can specify the number of copies that you want to make, and you can also copy notes and attachments.</span></span> <span data-ttu-id="ce1c3-151">Saate kopeerida jaotused või lubada sisestamisel nende uuesti loomise.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-151">You can copy the distributions or allow them to be recreated when you post.</span></span> <span data-ttu-id="ce1c3-152">Kui olete read kopeerinud, saate redigeerida teavet vastavalt vajadusele.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-152">Once you copy the lines, you can edit the information as needed.</span></span> 

## <a name="create-a-free-text-invoice-from-a-template"></a><span data-ttu-id="ce1c3-153">Vabas vormis arve loomine mallist</span><span class="sxs-lookup"><span data-stu-id="ce1c3-153">Create a free text invoice from a template</span></span>
<span data-ttu-id="ce1c3-154">Saate luua vabas vormis arve mallist.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-154">You can create a free text invoice from a template.</span></span> <span data-ttu-id="ce1c3-155">Kui valite vahekaardil Arve suvandi Uus mallist, saate uue vabas vormis malli jaoks valida malli nime ja kliendikonto.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-155">When you select New from template from the Invoice tab, you can select a template name and the customer account for the new free text invoice.</span></span> <span data-ttu-id="ce1c3-156">Saate valida ka vaikeväärtused, nt maksetingimused ja kliendi makseviisi jaoks, või kasutada malliga salvestatud väärtusi.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-156">You can also choose to default values such as the terms of payment and method of payment from the customer or use the values that were saved with the template.</span></span> <span data-ttu-id="ce1c3-157">Luuakse uus vabas vormis arve, mille väärtusi saate redigeerida.</span><span class="sxs-lookup"><span data-stu-id="ce1c3-157">A new free text invoice will be created and you can edit the values in that invoice.</span></span> 


