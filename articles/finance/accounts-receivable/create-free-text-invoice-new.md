---
title: Vabas vormis arve loomine
description: Selles teemas kirjeldatakse vabas vormis arvete loomist.
author: mikefalkner
manager: AnnBe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 909dd5bcaf1fa3b82adb44d265e312f9acc607d2
ms.sourcegitcommit: 9168621ca9b5061c65f3e05dbc5918b6a11d53d5
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/31/2020
ms.locfileid: "3000066"
---
# <a name="create-a-free-text-invoice"></a><span data-ttu-id="ae804-103">Vabas vormis arve loomine</span><span class="sxs-lookup"><span data-stu-id="ae804-103">Create a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ae804-104">Selles teemas kirjeldatakse vabas vormis arvete loomist.</span><span class="sxs-lookup"><span data-stu-id="ae804-104">This topic explains how to create free text invoices.</span></span> <span data-ttu-id="ae804-105">Selle protseduuri jaoks kasutage demoettevõtte **USMF** andmeid.</span><span class="sxs-lookup"><span data-stu-id="ae804-105">For the procedure, use the **USMF** demo company.</span></span>

## <a name="create-a-free-text-invoice"></a><span data-ttu-id="ae804-106">Vabas vormis arve loomine</span><span class="sxs-lookup"><span data-stu-id="ae804-106">Create a free text invoice</span></span>

1. <span data-ttu-id="ae804-107">Avage **Müügireskontro \> Arved \> Kõik vabas vormis arved**.</span><span class="sxs-lookup"><span data-stu-id="ae804-107">Go to **Accounts receivable \> Invoices \> All free text invoices**.</span></span>
2. <span data-ttu-id="ae804-108">Valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="ae804-108">Select **New**.</span></span>
3. <span data-ttu-id="ae804-109">Valige väärtus väljal **Kliendi konto**.</span><span class="sxs-lookup"><span data-stu-id="ae804-109">In the **Customer account** field, select a value.</span></span>

    * <span data-ttu-id="ae804-110">Vaikimisi kasutatakse arvekontona sama kontot, mis on valitud kliendikontoks.</span><span class="sxs-lookup"><span data-stu-id="ae804-110">By default, the account that is selected as the customer account is used as the invoice account.</span></span>
    * <span data-ttu-id="ae804-111">Kui arve pole sisestatud, algab raamatupidamisolek sõnaga **Pooleli**.</span><span class="sxs-lookup"><span data-stu-id="ae804-111">If the invoice isn't posted, the accounting status starts with **In process**.</span></span>
    * <span data-ttu-id="ae804-112">Pärast arve sisestamist määratakse arve number.</span><span class="sxs-lookup"><span data-stu-id="ae804-112">The invoice number will be assigned when the invoice is posted.</span></span>
    * <span data-ttu-id="ae804-113">Kui kasutate ühtse euromaksete piirkonna (SEPA) lubasid, sisestatakse kliendikonto valimisel otsekorralduse luba automaatselt.</span><span class="sxs-lookup"><span data-stu-id="ae804-113">If you're using Single Euro Payments Area (SEPA) mandates, the direct debit mandate is automatically entered when you select the customer account.</span></span>

4. <span data-ttu-id="ae804-114">Sisestage väärtus väljal **Kirjeldus**.</span><span class="sxs-lookup"><span data-stu-id="ae804-114">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="ae804-115">Määrake dimensioonideta kontonumber väljal **Põhikonto**.</span><span class="sxs-lookup"><span data-stu-id="ae804-115">In the **Main account** field, specify an account number that doesn't have dimensions.</span></span> <span data-ttu-id="ae804-116">Selles teemas saate hiljem sisestada ka dimensioonid.</span><span class="sxs-lookup"><span data-stu-id="ae804-116">You will enter dimensions later in this topic.</span></span>

    <span data-ttu-id="ae804-117">Samuti saate konto leidmiseks kasutada otsingut, sisestades põhikonto kohta ühe või mitu märki.</span><span class="sxs-lookup"><span data-stu-id="ae804-117">You can also enter one or more characters for the main account, and use the lookup to find the account.</span></span>

6. <span data-ttu-id="ae804-118">Põhikontole dimensioonide lisamiseks valige kiirkaart **Rea üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="ae804-118">Select the **Line details** FastTab to add dimensions to the main account.</span></span>
7. <span data-ttu-id="ae804-119">Valige vahekaart **Finantsdimensiooni rida**.</span><span class="sxs-lookup"><span data-stu-id="ae804-119">Select the **Financial dimensions line** tab.</span></span>

    * <span data-ttu-id="ae804-120">Dimensioonid on ette nähtud ainult valitud reale.</span><span class="sxs-lookup"><span data-stu-id="ae804-120">The dimensions are for the selected line only.</span></span>
    * <span data-ttu-id="ae804-121">Käibemaksugrupp täidetakse kliendi põhjal.</span><span class="sxs-lookup"><span data-stu-id="ae804-121">The sales tax group is filled in from the customer.</span></span> <span data-ttu-id="ae804-122">Kui kliendil pole käibemaksugruppi, kasutatakse põhikonto käibemaksugruppi.</span><span class="sxs-lookup"><span data-stu-id="ae804-122">If the customer doesn't have a sales tax group, the sales tax group from the main account is used.</span></span>
    * <span data-ttu-id="ae804-123">Kauba käibemaksugrupp täidetakse põhikontolt.</span><span class="sxs-lookup"><span data-stu-id="ae804-123">The items sales tax group is filled in from the main account.</span></span> <span data-ttu-id="ae804-124">Kui põhikontol pole kauba käibemaksugruppi, kasutatakse pearaamatu käibemaksuparameetrite lehel määratud kauba käibemaksugruppi.</span><span class="sxs-lookup"><span data-stu-id="ae804-124">If the main account doesn't have an item sales tax group, the item sales tax group that is specified in the sales tax parameters in General ledger is used.</span></span>

8. <span data-ttu-id="ae804-125">Valikuline: sisestage arv väljale **Kogus**.</span><span class="sxs-lookup"><span data-stu-id="ae804-125">Optional: In the **Quantity** field, enter a number.</span></span>
9. <span data-ttu-id="ae804-126">Valikuline: sisestage arv väljale **Ühiku hind**.</span><span class="sxs-lookup"><span data-stu-id="ae804-126">Optional: In the **Unit price** field, enter a number.</span></span>

    <span data-ttu-id="ae804-127">Summa arvutamiseks korrutatakse kogus ühikuhinnaga.</span><span class="sxs-lookup"><span data-stu-id="ae804-127">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="ae804-128">Teil on ka võimalus see arvutus tühistada, sisestades summa.</span><span class="sxs-lookup"><span data-stu-id="ae804-128">However, you can override that calculation by entering an amount.</span></span>

10. <span data-ttu-id="ae804-129">Arve jaoks arvutatud käibemaksu kuvamiseks valige suvand **Käibemaks**.</span><span class="sxs-lookup"><span data-stu-id="ae804-129">Select **Sales tax** to view the sales tax that is calculated for the invoice.</span></span>

    <span data-ttu-id="ae804-130">Käibemaksusummasid saate vaadata sellel lehel või tühistada summad vahekaardil **Korrigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="ae804-130">You can view the sales tax amounts on this page, or you can override the amounts on the **Adjustment** tab.</span></span>

11. <span data-ttu-id="ae804-131">Valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="ae804-131">Select **OK**.</span></span>
12. <span data-ttu-id="ae804-132">Arvele tasu lisamiseks klõpsake valikut **Tasud**.</span><span class="sxs-lookup"><span data-stu-id="ae804-132">Select **Charges** to add a charge to the invoice.</span></span>
13. <span data-ttu-id="ae804-133">Sisestage väärtus väljale **Tasukood**.</span><span class="sxs-lookup"><span data-stu-id="ae804-133">In the **Charges code** field, enter a value.</span></span>
14. <span data-ttu-id="ae804-134">Sisestage arv väljale **Tasude väärtus**.</span><span class="sxs-lookup"><span data-stu-id="ae804-134">In the **Charges value** field, enter a number.</span></span>
15. <span data-ttu-id="ae804-135">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="ae804-135">Close the page.</span></span>
16. <span data-ttu-id="ae804-136">Lõpparve üksikasjade ja kogusummade kuvamiseks valige suvand **Kogusummad**.</span><span class="sxs-lookup"><span data-stu-id="ae804-136">Select **Totals** to view a summary of the invoice details and totals.</span></span>
17. <span data-ttu-id="ae804-137">Valige suvand **Sule**.</span><span class="sxs-lookup"><span data-stu-id="ae804-137">Select **Close**.</span></span>
18. <span data-ttu-id="ae804-138">Arve sisestamiseks valige suvand **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="ae804-138">Select **Post** to post the invoice.</span></span> <span data-ttu-id="ae804-139">Enne tegelikult sisestamist on teil veel võimalus tühistada.</span><span class="sxs-lookup"><span data-stu-id="ae804-139">You will still have an opportunity to cancel before you actually post.</span></span>

    * <span data-ttu-id="ae804-140">Saate muuta arve printimise aega.</span><span class="sxs-lookup"><span data-stu-id="ae804-140">You can change the timing of invoice printing.</span></span> <span data-ttu-id="ae804-141">Valige **Praegune**, et printida arve pärast värskendamist.</span><span class="sxs-lookup"><span data-stu-id="ae804-141">Select **Current** to print each invoice as it's updated.</span></span> <span data-ttu-id="ae804-142">Valige **Pärast**, et printida pärast kõikide arvete uuendamist.</span><span class="sxs-lookup"><span data-stu-id="ae804-142">Select **After** to print after all invoices have been updated.</span></span>
    * <span data-ttu-id="ae804-143">Muutke väärtust väljas **Krediidilimiidi tüüp**, et muuta seda, kuidas kliendi krediidilimiiti enne arve sisestamist kontrollitakse.</span><span class="sxs-lookup"><span data-stu-id="ae804-143">To change how the customer's credit limit is verified before the invoice is posted, change the value in the **Credit limit type** field.</span></span>
    * <span data-ttu-id="ae804-144">Arve printimiseks määrake suvand valikule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="ae804-144">To print the invoice, set the option to **Yes**.</span></span>
    * <span data-ttu-id="ae804-145">Arve sisestamiseks määrake suvand valikule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="ae804-145">To post the invoice, set the option to **Yes**.</span></span> <span data-ttu-id="ae804-146">Saate arve ilma sisestamata printida.</span><span class="sxs-lookup"><span data-stu-id="ae804-146">You can print the invoice without posting it.</span></span>

19. <span data-ttu-id="ae804-147">Valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="ae804-147">Select **OK**.</span></span>

## <a name="copy-lines"></a><span data-ttu-id="ae804-148">Kopeeri read</span><span class="sxs-lookup"><span data-stu-id="ae804-148">Copy lines</span></span>
<span data-ttu-id="ae804-149">Vabas vormis arve ridade kopeerimiseks valige üks või mitu rida ja valige suvand **Kopeeri valitud read**.</span><span class="sxs-lookup"><span data-stu-id="ae804-149">To copy lines on a free text invoice, select one or more lines, and then select **Copy selected lines**.</span></span> <span data-ttu-id="ae804-150">Saate määrata koopiate arvu ning kopeerida märkusi ja manuseid.</span><span class="sxs-lookup"><span data-stu-id="ae804-150">You can specify the number of copies to make, and you can also copy notes and attachments.</span></span> <span data-ttu-id="ae804-151">Saate kopeerida jaotused või lubada sisestamisel nende uuesti loomise.</span><span class="sxs-lookup"><span data-stu-id="ae804-151">You can either copy the distributions or let them be re-created when you post.</span></span>

<span data-ttu-id="ae804-152">Pärast ridade kopeerimist saate redigeerida teavet vajaduse järgi.</span><span class="sxs-lookup"><span data-stu-id="ae804-152">After you copy lines, you can edit the information as you require.</span></span>

## <a name="create-a-free-text-invoice-from-a-template"></a><span data-ttu-id="ae804-153">Vabas vormis arve loomine mallist</span><span class="sxs-lookup"><span data-stu-id="ae804-153">Create a free text invoice from a template</span></span>
<span data-ttu-id="ae804-154">Saate luua vabas vormis arve mallist.</span><span class="sxs-lookup"><span data-stu-id="ae804-154">You can create a free text invoice from a template.</span></span> <span data-ttu-id="ae804-155">Kui valite suvandi **Uus mallist** vahekaardil **Arve**, saate uue vabas vormis malli jaoks valida malli nime ja kliendikonto.</span><span class="sxs-lookup"><span data-stu-id="ae804-155">When you select **New from template** on the **Invoice** tab, you can select a template name and the customer account for the new free text invoice.</span></span> <span data-ttu-id="ae804-156">Vaikeväärtusi, nt maksetingimused ja makseviisi, saab automaatselt kliendi põhjal täita või võite kasutada malli salvestatud väärtusi.</span><span class="sxs-lookup"><span data-stu-id="ae804-156">Default values, such as the terms of payment and method of payment, can be automatically filled in from the customer, or you can use the values that were saved in the template.</span></span>

<span data-ttu-id="ae804-157">Luuakse uus vabas vormis arve, mille väärtusi saate vajaduse järgi redigeerida.</span><span class="sxs-lookup"><span data-stu-id="ae804-157">A new free text invoice is created, and you can edit the values as you require.</span></span>
