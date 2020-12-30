---
title: Päisekulude proportsionaalselt jaotamine vastavatele müügiridadele
description: See teema kirjeldab täiendavaid võimalusi automaatsete kulude arvutamise ja kaubanduskanali tellimustele rakendamise kohta, kasutades täpsemate automaatsete kulude funktsiooni.
author: hhaines
manager: annbe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: hhaines
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 048885cac7a316e144b2df072da405d74096203f
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411548"
---
# <a name="prorate-header-charges-to-matching-sales-lines"></a><span data-ttu-id="0c861-103">Päisekulude proportsionaalselt jaotamine vastavatele müügiridadele</span><span class="sxs-lookup"><span data-stu-id="0c861-103">Prorate header charges to matching sales lines</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="0c861-104">Selles teemas kirjeldatakse päisetasemel automaatsete kulude rühmitamise ja nende kaubanduse müügiridadele proportsionaalselt jaotamise funktsionaalsust.</span><span class="sxs-lookup"><span data-stu-id="0c861-104">This topic describes the functionality for grouping header-level auto-charges and prorating them to commerce sales lines.</span></span> <span data-ttu-id="0c861-105">See funktsioon on saadaval kannetele, mis on loodud kassas (POS) rakenduse Retail versioonis 10.0.1 ja müükides, mis on loodud rakenduse Retail 10.0.2 versiooni kõnekeskuses.</span><span class="sxs-lookup"><span data-stu-id="0c861-105">This functionality is available for transactions that are created at the point of sale (POS) in Retail version 10.0.1 and sales that are created in a call center in Retail version 10.0.2.</span></span>

<span data-ttu-id="0c861-106">See funktsioon on saadaval ainult siis, kui funktsioon [täpsemad automaatsed kulud](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges) on lehel **Kaubanduse parameetrid** olevat suvandit kasutades sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="0c861-106">This functionality is available only if the [advanced auto-charges](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges) feature is turned on by using the option on the **Commerce parameters** page.</span></span> <span data-ttu-id="0c861-107">Samuti saab automaatsete kulude täiustatud arvutusviisi rakendada ainult müügitellimustele, mis on loodud kaubanduskanalite kaudu (kassa, kõnekeskus ja Dynamicsi e-Commerce’i platvorm).</span><span class="sxs-lookup"><span data-stu-id="0c861-107">Additionally, the enhanced calculation method for auto-charges can be applied only to sales orders that are created through commerce channels (the POS, a call center, and the Dynamics e-Commerce platform).</span></span>

<span data-ttu-id="0c861-108">See uus funktsioon pakub organisatsioonidele päisetasemel automaatsete kulude arvutamisel ja nende müügikannetele rakendamisel suuremat paindlikkust.</span><span class="sxs-lookup"><span data-stu-id="0c861-108">This new functionality gives organizations more flexibility in the way that header-level auto-charges are calculated and applied to sales transactions.</span></span>

<span data-ttu-id="0c861-109">Rakenduse versioonides, mis on varasemad kui 10.0.1, arvutatakse päisetasemel automaatsed kulud, millel on kindel tarneviisi seos, ainult siis, kui tarneviisis esineb vastavus, mis on määratletud müügitellimuse päises.</span><span class="sxs-lookup"><span data-stu-id="0c861-109">In versions of the app earlier than version 10.0.1, header-level auto-charges that have a specific mode of delivery relation are calculated only when there is a match with the mode of delivery that is defined on the sales order header.</span></span>

<span data-ttu-id="0c861-110">Näiteks on päisetasemel automaatsed kulud määratletud tarneviisi **99** ja **11** puhul.</span><span class="sxs-lookup"><span data-stu-id="0c861-110">For example, header-level auto-charges are defined for mode of delivery **99** and mode of delivery **11**.</span></span> <span data-ttu-id="0c861-111">Luuakse müügitellimus ja tarneviis **99** määratletakse tellimuse päises.</span><span class="sxs-lookup"><span data-stu-id="0c861-111">A sales order is created, and mode of delivery **99** is defined on the order header.</span></span> <span data-ttu-id="0c861-112">Siiski on osa müügiridu seadistatud viisil, et nad saadetakse tarneviisiga **11**.</span><span class="sxs-lookup"><span data-stu-id="0c861-112">However, some of the sale lines are set up so that they're shipped by using mode of delivery **11**.</span></span> <span data-ttu-id="0c861-113">Sellisel juhul arvestatakse ja rakendatakse müügitellimusele ainult päisetasemel kulud, mis on seotud tarneviisiga **99**.</span><span class="sxs-lookup"><span data-stu-id="0c861-113">In this case, only the header-level charges that are linked to mode of delivery **99** are considered and applied to the sales order.</span></span>

<span data-ttu-id="0c861-114">Rakenduses Commerce on päisetasemel kuludel täiendav funktsioon, mis võimaldab teil määratleda [mitmetasemelise tasu konfiguratsiooni](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery), mis põhineb tellimuse väärtusel.</span><span class="sxs-lookup"><span data-stu-id="0c861-114">In Commerce, the header-level charges have an additional feature that lets you define a [tiered charge configuration](https://docs.microsoft.com/dynamics365/unified-operations/retail/configure-call-center-delivery) that is based on the order value.</span></span> <span data-ttu-id="0c861-115">Näiteks kui tellimuse väärtus on vahemikus $50,00 ja $200,00, võib ettevõte võtta veokulude eest tasu $5,00.</span><span class="sxs-lookup"><span data-stu-id="0c861-115">For example, if the order value is between $50.00 and $200.00, an organization might want to charge a freight charge of $5.00.</span></span> <span data-ttu-id="0c861-116">Kui tellimuse väärtus jääb vahemikku $200,01 ja $500,00, võiks veokulu olla $4,00.</span><span class="sxs-lookup"><span data-stu-id="0c861-116">However, if the order value is between $200.01 and $500.00, the freight charge might be $4.00.</span></span>

<span data-ttu-id="0c861-117">Mõned ettevõtted soovivad mitmetasandilise tasu arvutamisega kaasnevaid eeliseid, mida pakuvad päisetasemel kulud.</span><span class="sxs-lookup"><span data-stu-id="0c861-117">Some organizations want the benefits of the tiered charge calculation that is provided with header-level charges.</span></span> <span data-ttu-id="0c861-118">Siiski, stsenaariumites, kus on lubatud segatarneviisid, soovivad ettevõtted veenduda, et arvutatud kulud põhinevad tarneviisi vastavusel, mis on määratletud igal müügitellimuse real.</span><span class="sxs-lookup"><span data-stu-id="0c861-118">However, in scenarios that involve mixed modes of delivery, they also want to make sure that the charges that are calculated are based on a match with the mode of delivery that is defined on each sales line.</span></span>

<span data-ttu-id="0c861-119">Nüüd saate konfigureerida päisetasemel automaatseid kulusid nii, et kulude arvutamisel arvestatakse kõiki tarneviise.</span><span class="sxs-lookup"><span data-stu-id="0c861-119">You can now configure header-level auto-charges so that all modes of delivery on the order are considered when charges are calculated.</span></span> <span data-ttu-id="0c861-120">See funktsioon nõuab päisetasemel kulude arvutamiseks keerukamat arvutusloogikat.</span><span class="sxs-lookup"><span data-stu-id="0c861-120">This functionality requires a more complex calculation logic to calculate the header-level charges.</span></span> <span data-ttu-id="0c861-121">Loogika rühmitab kokku kõik sama tarneviisi kasutavad saadetavad kaubad ja käsitleb seda gruppi kaupade jaoks päisetaseme automaatsete kulude arvutamisel kalkulatsioonigrupina.</span><span class="sxs-lookup"><span data-stu-id="0c861-121">The logic groups together all the items that are shipped using the same mode of delivery, and it treats that group as the calculation group for the items when it calculates the header-level auto-charges.</span></span> <span data-ttu-id="0c861-122">Sama tarneviisiga kaupade puhul arvutatakse automaatsed kulud kaupade kombineeritud müügiväärtuse alusel.</span><span class="sxs-lookup"><span data-stu-id="0c861-122">For items that have the same mode of delivery, auto-charges are calculated based on the combined sales value of the items.</span></span> <span data-ttu-id="0c861-123">Sel viisil määratakse sobiv automaatse kulu järk.</span><span class="sxs-lookup"><span data-stu-id="0c861-123">In this way, the appropriate auto-charge tier is determined.</span></span>

<span data-ttu-id="0c861-124">Pärast seda, kui sobivad päisetasemel kulud on sama tarneviisiga saadetavate müügiridade jaoks toodud, jaotatakse arvutatud kulud proportsionaalselt müügirea tasemele.</span><span class="sxs-lookup"><span data-stu-id="0c861-124">After the appropriate header-level charges are obtained for the sales lines that are shipped using the same mode of delivery, the calculated charges are prorated down to the sales line level.</span></span> <span data-ttu-id="0c861-125">Kuna need kulud on reatasemel ja neid ei hoita päisetasemel, moodustatakse kauba ja selle jaoks arvutatud kulu väärtuse vahel spetsiifilisem link.</span><span class="sxs-lookup"><span data-stu-id="0c861-125">Because these charges are at the line level and not kept at the header level, a more specific link is made between the item and the charge value that calculated for it.</span></span> <span data-ttu-id="0c861-126">Selline käitumine võib olla kasulik osaliste tagastuste stsenaariumite korral, kus ettevõte soovib tagastada terve tasu asemel ainult osa tasust, kui tagastatakse ainult mõned kaubad.</span><span class="sxs-lookup"><span data-stu-id="0c861-126">This behavior can be useful in partial return scenarios, where an organization wants to refund only part of the charge instead of the whole charge when only some items are returned.</span></span>

## <a name="scenarios"></a><span data-ttu-id="0c861-127">Stsenaariumid</span><span class="sxs-lookup"><span data-stu-id="0c861-127">Scenarios</span></span>

<span data-ttu-id="0c861-128">Järgmised kaks näidisstsenaariumit annavad ülevaate nende kulude arvutamisest nii uue funktsiooni kasutamisel kui ka mittekasutamisel.</span><span class="sxs-lookup"><span data-stu-id="0c861-128">The following two sample scenarios outline how these charges are calculated both when the new functionality is used and when it isn't used.</span></span>

### <a name="scenario-1"></a><span data-ttu-id="0c861-129">1. stsenaarium</span><span class="sxs-lookup"><span data-stu-id="0c861-129">Scenario 1</span></span>

<span data-ttu-id="0c861-130">See stsenaarium kirjeldab käitumist, kui suvand **Proportsionaalselt vastavatele müügiridadele jaotamine** on automaatse kulu seadistuses määratud väärtusele **Ei**.</span><span class="sxs-lookup"><span data-stu-id="0c861-130">This scenario outlines the behavior when the **Pro-rate to matching sales lines** option is set to **No** in the auto-charge setup.</span></span> <span data-ttu-id="0c861-131">(Käitumine on võrdne päisetasemel kuludega rakenduse versioonides, mis on varasemad kui versioon 10.0.1)</span><span class="sxs-lookup"><span data-stu-id="0c861-131">(The behavior is equivalent to the behavior of header-level charges in app versions that are earlier than version 10.0.1.)</span></span>

<span data-ttu-id="0c861-132">Selles stsenaariumis on ettevõte määratlenud päisetasemel kulud tarneviisi seostele **99** ja **11**.</span><span class="sxs-lookup"><span data-stu-id="0c861-132">In this scenario, the organization has defined header-level charges for mode of delivery relation **99** and mode of delivery relation **11**.</span></span> <span data-ttu-id="0c861-133">Tarneviisile **21** pole konfigureeritud ühtegi automaatset kulu.</span><span class="sxs-lookup"><span data-stu-id="0c861-133">No auto-charges are configured for mode of delivery **21**.</span></span>

![Tarneviisi 99 automaatsed kulud, kui vastenduv rea proportsionaalne arvestus on välja lülitatud](media/99_disabled.png)

![Tarneviisi 11 automaatsed kulud, kui vastenduv rea proportsionaalne arvestus on välja lülitatud](media/11_disabled.png)

<span data-ttu-id="0c861-136">Kõnekeskuses luuakse müügitellimus ja tarneviisiks määratakse **99**.</span><span class="sxs-lookup"><span data-stu-id="0c861-136">A sales order is created in the call center, and the mode of delivery is set to **99**.</span></span> <span data-ttu-id="0c861-137">See tellimus sisaldab viit kaupa.</span><span class="sxs-lookup"><span data-stu-id="0c861-137">This order contains five items.</span></span> <span data-ttu-id="0c861-138">Kaks tellimuserida on konfigureeritud kasutama tarneviisi **99**, kaks rida on konfigureeritud kasutama tarneviisi **11** ja üks rida on konfigureeritud kasutama tarneviisi **21**, nagu on näidatud järgmises tabelis.</span><span class="sxs-lookup"><span data-stu-id="0c861-138">Two order lines have been configured to use mode of delivery **99**, two lines have been configured to use mode of delivery **11**, and one line has been configured to use mode of delivery **21**, as shown in the following table.</span></span>

| <span data-ttu-id="0c861-139">Kaup</span><span class="sxs-lookup"><span data-stu-id="0c861-139">Item</span></span>  | <span data-ttu-id="0c861-140">Rea kogus</span><span class="sxs-lookup"><span data-stu-id="0c861-140">Line quantity</span></span> | <span data-ttu-id="0c861-141">Tarneviis</span><span class="sxs-lookup"><span data-stu-id="0c861-141">Delivery mode</span></span> | <span data-ttu-id="0c861-142">Hind ühiku kohta</span><span class="sxs-lookup"><span data-stu-id="0c861-142">Price per unit</span></span> |
|-------|---------------|---------------|----------------|
| <span data-ttu-id="0c861-143">81331</span><span class="sxs-lookup"><span data-stu-id="0c861-143">81331</span></span> | <span data-ttu-id="0c861-144">1</span><span class="sxs-lookup"><span data-stu-id="0c861-144">1</span></span>             | <span data-ttu-id="0c861-145">11</span><span class="sxs-lookup"><span data-stu-id="0c861-145">11</span></span>            | <span data-ttu-id="0c861-146">$10</span><span class="sxs-lookup"><span data-stu-id="0c861-146">$10</span></span>            |
| <span data-ttu-id="0c861-147">81332</span><span class="sxs-lookup"><span data-stu-id="0c861-147">81332</span></span> | <span data-ttu-id="0c861-148">1</span><span class="sxs-lookup"><span data-stu-id="0c861-148">1</span></span>             | <span data-ttu-id="0c861-149">99</span><span class="sxs-lookup"><span data-stu-id="0c861-149">99</span></span>            | <span data-ttu-id="0c861-150">50 dollarit</span><span class="sxs-lookup"><span data-stu-id="0c861-150">$50</span></span>            |
| <span data-ttu-id="0c861-151">81333</span><span class="sxs-lookup"><span data-stu-id="0c861-151">81333</span></span> | <span data-ttu-id="0c861-152">2</span><span class="sxs-lookup"><span data-stu-id="0c861-152">2</span></span>             | <span data-ttu-id="0c861-153">11</span><span class="sxs-lookup"><span data-stu-id="0c861-153">11</span></span>            | <span data-ttu-id="0c861-154">$30</span><span class="sxs-lookup"><span data-stu-id="0c861-154">$30</span></span>            |
| <span data-ttu-id="0c861-155">81334</span><span class="sxs-lookup"><span data-stu-id="0c861-155">81334</span></span> | <span data-ttu-id="0c861-156">3</span><span class="sxs-lookup"><span data-stu-id="0c861-156">3</span></span>             | <span data-ttu-id="0c861-157">99</span><span class="sxs-lookup"><span data-stu-id="0c861-157">99</span></span>            | <span data-ttu-id="0c861-158">$10</span><span class="sxs-lookup"><span data-stu-id="0c861-158">$10</span></span>            |
| <span data-ttu-id="0c861-159">81334</span><span class="sxs-lookup"><span data-stu-id="0c861-159">81334</span></span> | <span data-ttu-id="0c861-160">3</span><span class="sxs-lookup"><span data-stu-id="0c861-160">3</span></span>             | <span data-ttu-id="0c861-161">21</span><span class="sxs-lookup"><span data-stu-id="0c861-161">21</span></span>            | <span data-ttu-id="0c861-162">$5</span><span class="sxs-lookup"><span data-stu-id="0c861-162">$5</span></span>             |

<span data-ttu-id="0c861-163">Selles stsenaariumis hinnatakse kogu tellimust tarneviisi **99** automaatse kulu tabeli suhtes.</span><span class="sxs-lookup"><span data-stu-id="0c861-163">In this scenario, the whole order is evaluated against the auto-charge table for mode of delivery **99**.</span></span> <span data-ttu-id="0c861-164">Kõigi müügiridade kogusummat kasutatakse automaatse kulu konfiguratsioonis vastava järgu määramiseks ja see tasu rakendatakse tellimuse päisetasemel.</span><span class="sxs-lookup"><span data-stu-id="0c861-164">The full total of all sales lines is used to determine a matching tier in the auto-charge configuration, and this charge is applied at the order header level.</span></span> <span data-ttu-id="0c861-165">Selles näites on tellimuse kogusumma $165,00 ja tellimuse päisele rakendatakse veokulu $15,00.</span><span class="sxs-lookup"><span data-stu-id="0c861-165">In this example, the order total is $165.00, and the $15.00 freight charge is applied to the order header.</span></span> <span data-ttu-id="0c861-166">Automaatsetele kuludele, mis konfigureeritakse tarneviisile **11**, ei viidata ja neid ei rakendata kunagi.</span><span class="sxs-lookup"><span data-stu-id="0c861-166">Auto-charges that are configured for mode of delivery **11** are never referenced or applied.</span></span>

<span data-ttu-id="0c861-167">Selles stsenaariumis, kui klient tagastab mõned tellimuse kaubad ja kui [tasukood on konfigureeritud nii, et see makstakse tagasi](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges#setup-and-configuration-2), rakendatakse tagasimaksele süstemaatiliselt päisetaseme kulude kogusumma, isegi kui tagastatakse ainult mõned kaubad.</span><span class="sxs-lookup"><span data-stu-id="0c861-167">In this scenario, if a customer returns some of the items on the order, and if the [charge code has been configured so that it will be refunded](https://docs.microsoft.com/dynamics365/unified-operations/retail/omni-auto-charges#setup-and-configuration-2), the total header-level charge is systematically applied to the refund, even if only some of the items are returned.</span></span>

### <a name="scenario-2"></a><span data-ttu-id="0c861-168">2. stsenaarium</span><span class="sxs-lookup"><span data-stu-id="0c861-168">Scenario 2</span></span>

<span data-ttu-id="0c861-169">Selles stsenaariumis määratletakse päisetasemel kulud tarneviisi seostele **99** ja **11**.</span><span class="sxs-lookup"><span data-stu-id="0c861-169">In this scenario, header-level charges are defined for mode of delivery relation **99** and mode of delivery relation **11**.</span></span> <span data-ttu-id="0c861-170">Kuid nende automaatse kulu tabelite puhul on suvand **Proportsionaalselt vastavatele müügiridadele jaotamine** määratud väärtusele **Jah**.</span><span class="sxs-lookup"><span data-stu-id="0c861-170">However, the **Pro-rate to matching sales lines** option is set to **Yes** for these auto-charge tables.</span></span>

![Tarneviisi 99 automaatsed kulud, kui vastenduv rea proportsionaalne arvestus on sisse lülitatud](media/99_enabled.png)

![Tarneviisi 11 automaatsed kulud, kui vastenduv rea proportsionaalne arvestus on sisse lülitatud](media/11_enabled.png)

<span data-ttu-id="0c861-173">Stsenaarium kasutab sama müügitellimust, mis sisaldab viit rida.</span><span class="sxs-lookup"><span data-stu-id="0c861-173">This scenario uses the same sales order that contains five lines.</span></span> <span data-ttu-id="0c861-174">Tellimuse päises on tarneviisi väärtuseks **99**, kuid müügitellimuses on iga kauba tarneviis konfigureeritud järgmises tabelis näidatud viisil.</span><span class="sxs-lookup"><span data-stu-id="0c861-174">The mode of delivery on the order header is set to **99**, but the mode of delivery for each item on the sales order is configured as shown in the following table.</span></span>

| <span data-ttu-id="0c861-175">Kaup</span><span class="sxs-lookup"><span data-stu-id="0c861-175">Item</span></span>  | <span data-ttu-id="0c861-176">Rea kogus</span><span class="sxs-lookup"><span data-stu-id="0c861-176">Line quantity</span></span> | <span data-ttu-id="0c861-177">Tarneviis</span><span class="sxs-lookup"><span data-stu-id="0c861-177">Delivery mode</span></span> | <span data-ttu-id="0c861-178">Hind ühiku kohta</span><span class="sxs-lookup"><span data-stu-id="0c861-178">Price per unit</span></span> |
|-------|---------------|---------------|----------------|
| <span data-ttu-id="0c861-179">81331</span><span class="sxs-lookup"><span data-stu-id="0c861-179">81331</span></span> | <span data-ttu-id="0c861-180">1</span><span class="sxs-lookup"><span data-stu-id="0c861-180">1</span></span>             | <span data-ttu-id="0c861-181">11</span><span class="sxs-lookup"><span data-stu-id="0c861-181">11</span></span>            | <span data-ttu-id="0c861-182">$10</span><span class="sxs-lookup"><span data-stu-id="0c861-182">$10</span></span>            |
| <span data-ttu-id="0c861-183">81332</span><span class="sxs-lookup"><span data-stu-id="0c861-183">81332</span></span> | <span data-ttu-id="0c861-184">1</span><span class="sxs-lookup"><span data-stu-id="0c861-184">1</span></span>             | <span data-ttu-id="0c861-185">99</span><span class="sxs-lookup"><span data-stu-id="0c861-185">99</span></span>            | <span data-ttu-id="0c861-186">50 dollarit</span><span class="sxs-lookup"><span data-stu-id="0c861-186">$50</span></span>            |
| <span data-ttu-id="0c861-187">81333</span><span class="sxs-lookup"><span data-stu-id="0c861-187">81333</span></span> | <span data-ttu-id="0c861-188">2</span><span class="sxs-lookup"><span data-stu-id="0c861-188">2</span></span>             | <span data-ttu-id="0c861-189">11</span><span class="sxs-lookup"><span data-stu-id="0c861-189">11</span></span>            | <span data-ttu-id="0c861-190">$30</span><span class="sxs-lookup"><span data-stu-id="0c861-190">$30</span></span>            |
| <span data-ttu-id="0c861-191">81334</span><span class="sxs-lookup"><span data-stu-id="0c861-191">81334</span></span> | <span data-ttu-id="0c861-192">3</span><span class="sxs-lookup"><span data-stu-id="0c861-192">3</span></span>             | <span data-ttu-id="0c861-193">99</span><span class="sxs-lookup"><span data-stu-id="0c861-193">99</span></span>            | <span data-ttu-id="0c861-194">$10</span><span class="sxs-lookup"><span data-stu-id="0c861-194">$10</span></span>            |
| <span data-ttu-id="0c861-195">81334</span><span class="sxs-lookup"><span data-stu-id="0c861-195">81334</span></span> | <span data-ttu-id="0c861-196">3</span><span class="sxs-lookup"><span data-stu-id="0c861-196">3</span></span>             | <span data-ttu-id="0c861-197">21</span><span class="sxs-lookup"><span data-stu-id="0c861-197">21</span></span>            | <span data-ttu-id="0c861-198">$5</span><span class="sxs-lookup"><span data-stu-id="0c861-198">$5</span></span>             |

<span data-ttu-id="0c861-199">Kuna automaatse kulu konfiguratsioon on määratud proportsionaalsele jaotamisele vastavate müügiridade vahel, teeb süsteem järgmised arvutusetapid.</span><span class="sxs-lookup"><span data-stu-id="0c861-199">Because the auto-charge configuration is set to prorate to matching sales lines, the system performs the following calculation steps.</span></span>

1. <span data-ttu-id="0c861-200">Kõik kaubad, millel on sama tarneviis, rühmitatakse kokku ja süsteem arvutab rühmas olevate toodete jaoks toodete koguväärtuse.</span><span class="sxs-lookup"><span data-stu-id="0c861-200">All items that have the same mode of delivery are grouped together, and the system calculates the total product value of the items in the group.</span></span>

    <span data-ttu-id="0c861-201">**Tarneviis 11**</span><span class="sxs-lookup"><span data-stu-id="0c861-201">**Delivery mode 11**</span></span>

    - <span data-ttu-id="0c861-202">Kaup 81331, kogus 1 = $10</span><span class="sxs-lookup"><span data-stu-id="0c861-202">Item 81331, quantity 1 = $10</span></span>
    - <span data-ttu-id="0c861-203">Kaup 81333, kogus 2 = $60 neto ($30 ühiku kohta)</span><span class="sxs-lookup"><span data-stu-id="0c861-203">Item 81333, quantity 2 = $60 net ($30 per unit)</span></span>
    - <span data-ttu-id="0c861-204">**Tarneviisi 11 toodete koguväärtus = $70**</span><span class="sxs-lookup"><span data-stu-id="0c861-204">**Total product value for delivery mode 11 = $70**</span></span>

    <span data-ttu-id="0c861-205">**Tarneviis 99**</span><span class="sxs-lookup"><span data-stu-id="0c861-205">**Delivery mode 99**</span></span>

    - <span data-ttu-id="0c861-206">Kaup 81332, kogus 1 = $50</span><span class="sxs-lookup"><span data-stu-id="0c861-206">Item 81332, quantity 1 = $50</span></span>
    - <span data-ttu-id="0c861-207">Kaup 81334, kogus 3 = $30 neto</span><span class="sxs-lookup"><span data-stu-id="0c861-207">Item 81334, quantity 3 = $30 net</span></span>
    - <span data-ttu-id="0c861-208">**Tarneviisi 99 toodete koguväärtus = $80**</span><span class="sxs-lookup"><span data-stu-id="0c861-208">**Total product value for delivery mode 99 = $80**</span></span>

    <span data-ttu-id="0c861-209">**Tarneviis 21**</span><span class="sxs-lookup"><span data-stu-id="0c861-209">**Delivery mode 21**</span></span>

    - <span data-ttu-id="0c861-210">Kaup 81334, kogus 3 = $15 neto</span><span class="sxs-lookup"><span data-stu-id="0c861-210">Item 81334, quantity 3 = $15 net</span></span>
    - <span data-ttu-id="0c861-211">**Tarneviisi 21 toodete koguväärtus = $15**</span><span class="sxs-lookup"><span data-stu-id="0c861-211">**Total product value for delivery mode 21 = $15**</span></span>

2. <span data-ttu-id="0c861-212">Süsteem otsib päisetasemel automaatsete kulude konfiguratsiooni, mis vastab iga kaubarühma puhul kliendi ja tarneviisi sätetele.</span><span class="sxs-lookup"><span data-stu-id="0c861-212">The system looks for the configuration for header-level auto-charges that matches the customer and mode of delivery settings for each group of items.</span></span> <span data-ttu-id="0c861-213">Kui konfiguratsioon leitakse, otsib süsteem mitmetasandilisest konfiguratsioonist tasu, mis tuleks rakendada, seda tarneviisi grupis olevate kaupade koguväärtuse põhjal.</span><span class="sxs-lookup"><span data-stu-id="0c861-213">If the configuration is found, the system looks in the tiered configuration to find the charge that should be applied, based on the total product value of items in the mode of delivery group.</span></span>

    <span data-ttu-id="0c861-214">**Tarneviis 11**</span><span class="sxs-lookup"><span data-stu-id="0c861-214">**Delivery mode 11**</span></span>

    - <span data-ttu-id="0c861-215">Toodete koguväärtus = $70</span><span class="sxs-lookup"><span data-stu-id="0c861-215">Total product value = $70</span></span>
    - <span data-ttu-id="0c861-216">**Tasu väärtus = $7**</span><span class="sxs-lookup"><span data-stu-id="0c861-216">**Charge value = $7**</span></span>

    <span data-ttu-id="0c861-217">**Tarneviis 99**</span><span class="sxs-lookup"><span data-stu-id="0c861-217">**Delivery mode 99**</span></span>

    - <span data-ttu-id="0c861-218">Toodete koguväärtus = $80</span><span class="sxs-lookup"><span data-stu-id="0c861-218">Total product value = $80</span></span>
    - <span data-ttu-id="0c861-219">**Tasu väärtus = $15**</span><span class="sxs-lookup"><span data-stu-id="0c861-219">**Charge value = $15**</span></span>

    <span data-ttu-id="0c861-220">**Tarneviis 21**</span><span class="sxs-lookup"><span data-stu-id="0c861-220">**Delivery mode 21**</span></span>

    - <span data-ttu-id="0c861-221">Toodete koguväärtus = $15</span><span class="sxs-lookup"><span data-stu-id="0c861-221">Total product value = $15</span></span>
    - <span data-ttu-id="0c861-222">**Tasu väärtus = $0** (Sellise kliendi ja tarneviisi kombinatsiooni jaoks pole automaatseid kulusid konfigureeritud.)</span><span class="sxs-lookup"><span data-stu-id="0c861-222">**Charge value = $0** (No auto-charges have been configured for this combination of a customer and a mode of delivery.)</span></span>

    ![Tarneviisi 11 tasud kuuluvad esiletõstetud järku](media/step2mode11.png)

    ![Tarneviisi 99 tasud kuuluvad esiletõstetud järku](media/step2mode99.png)

3. <span data-ttu-id="0c861-225">Süsteem arvutab kulu väärtuse, mis tuleb rakendada igale reale, võttes aluseks proportsionaalse arvestuse loogika, mis arvestab rea proportsionaalset väärtust grupi toodete koguväärtusega seoses.</span><span class="sxs-lookup"><span data-stu-id="0c861-225">The system calculates the charge value that should be applied to each line, based on proration logic that considers the proportional value of the line in relation to the group's total product value.</span></span>

    <span data-ttu-id="0c861-226">**Tarneviis 11**</span><span class="sxs-lookup"><span data-stu-id="0c861-226">**Delivery mode 11**</span></span>

    - <span data-ttu-id="0c861-227">Tasu väärtus = $7</span><span class="sxs-lookup"><span data-stu-id="0c861-227">Charge value = $7</span></span>
    - <span data-ttu-id="0c861-228">Grupi tooteväärtus = $70</span><span class="sxs-lookup"><span data-stu-id="0c861-228">Group product value = $70</span></span>
    - <span data-ttu-id="0c861-229">Rea 1 väärtus = $10 (= 14,2857 protsenti grupi väärtusest)</span><span class="sxs-lookup"><span data-stu-id="0c861-229">Line 1 value = $10 (= 14.2857 percent of the group value)</span></span>
    - <span data-ttu-id="0c861-230">Rea 3 väärtus = $60 (= 85,7143 protsenti grupi väärtusest)</span><span class="sxs-lookup"><span data-stu-id="0c861-230">Line 3 value = $60 (= 85.7143 percent of the group value)</span></span>
    - <span data-ttu-id="0c861-231">**Rea 1 reatasu = $1**</span><span class="sxs-lookup"><span data-stu-id="0c861-231">**Line charge for line 1 = $1**</span></span>
    - <span data-ttu-id="0c861-232">**Rea 3 reatasu = $6**</span><span class="sxs-lookup"><span data-stu-id="0c861-232">**Line charge for line 3 = $6**</span></span>

    <span data-ttu-id="0c861-233">**Tarneviis 99**</span><span class="sxs-lookup"><span data-stu-id="0c861-233">**Delivery mode 99**</span></span>

    - <span data-ttu-id="0c861-234">Tasu väärtus = $15</span><span class="sxs-lookup"><span data-stu-id="0c861-234">Charge value = $15</span></span>
    - <span data-ttu-id="0c861-235">Grupi tooteväärtus = $80</span><span class="sxs-lookup"><span data-stu-id="0c861-235">Group product value = $80</span></span>
    - <span data-ttu-id="0c861-236">Rea 2 väärtus = $50 (= 62,5 protsenti grupi väärtusest)</span><span class="sxs-lookup"><span data-stu-id="0c861-236">Line 2 value = $50 (= 62.5 percent of the group value)</span></span>
    - <span data-ttu-id="0c861-237">Rea 4 väärtus = $30 (= 37,5 protsenti grupi väärtusest)</span><span class="sxs-lookup"><span data-stu-id="0c861-237">Line 4 value = $30 (= 37.5 percent of the group value)</span></span>
    - <span data-ttu-id="0c861-238">**Rea 2 reatasu = $9,38**</span><span class="sxs-lookup"><span data-stu-id="0c861-238">**Line charge for line 2 = $9.38**</span></span>
    - <span data-ttu-id="0c861-239">**Rea 4 reatasu = $5,62**</span><span class="sxs-lookup"><span data-stu-id="0c861-239">**Line charge for line 4 = $5.62**</span></span>

    <span data-ttu-id="0c861-240">**Tarneviis 21**</span><span class="sxs-lookup"><span data-stu-id="0c861-240">**Delivery mode 21**</span></span>

    - <span data-ttu-id="0c861-241">Tasu väärtus = $0</span><span class="sxs-lookup"><span data-stu-id="0c861-241">Charge value = $0</span></span>
    - <span data-ttu-id="0c861-242">Grupi tooteväärtus = $15</span><span class="sxs-lookup"><span data-stu-id="0c861-242">Group product value = $15</span></span>
    - <span data-ttu-id="0c861-243">Rea 5 väärtus = $15 (= 100 protsenti grupi väärtusest)</span><span class="sxs-lookup"><span data-stu-id="0c861-243">Line 5 value = $15 (= 100 percent of the group value)</span></span>
    - <span data-ttu-id="0c861-244">**Rea 5 reatasu = $0**</span><span class="sxs-lookup"><span data-stu-id="0c861-244">**Line charge for line 5 = $0**</span></span>

<span data-ttu-id="0c861-245">Seetõttu määratakse selles näites kaubale 81334 veokulu summas $5,62.</span><span class="sxs-lookup"><span data-stu-id="0c861-245">Therefore, for this example, item 81334 will be assigned a freight charge of $5.62.</span></span> <span data-ttu-id="0c861-246">Neid tasusid saate vaadata müügitellimuse rea lehel **Tasude haldamine**.</span><span class="sxs-lookup"><span data-stu-id="0c861-246">You can view these charges on the **Maintain charges** page for the sales line.</span></span> <span data-ttu-id="0c861-247">Järgmisel joonisel on näidatud, kuidas see leht kauba 81334 jaoks välja näeb.</span><span class="sxs-lookup"><span data-stu-id="0c861-247">The following illustration shows what this page looks like for item 81334.</span></span>

![Müügirea proportsionaalselt jaotatud tasud kauba 81334 puhul](media/proratedlinecharge.png)

<span data-ttu-id="0c861-249">Kui seda arvutamismeetodit kasutatakse osalise tagastuse stsenaariumi korral, kui tasukood on tagasimakstav, makstakse kauba tagastamisel tagasi ainult see tasu osa, mis on eraldatud sellele reale.</span><span class="sxs-lookup"><span data-stu-id="0c861-249">When this method of calculation is used in a partial return scenario, if the charge code is refundable, only the part of the charge that is allocated to that line will be refunded when the item is returned.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0c861-250">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="0c861-250">Additional resources</span></span>

[<span data-ttu-id="0c861-251">Omnikanali täpsemad automaatsed kulud</span><span class="sxs-lookup"><span data-stu-id="0c861-251">Omni-channel advanced auto charges</span></span>](omni-auto-charges.md)

[<span data-ttu-id="0c861-252">Automaatsete tasude lubamine ja konfigureerimine kanali kaupa</span><span class="sxs-lookup"><span data-stu-id="0c861-252">Enable and configure auto charges by channel</span></span>](auto-charges-by-channel.md)
