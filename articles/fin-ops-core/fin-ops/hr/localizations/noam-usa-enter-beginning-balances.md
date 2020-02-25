---
title: Palga algsaldode sisestamine
description: Selles teemas kirjeldatakse tulukoodide, mahaarvamiste, soodustuste ja maksude algsaldode sisestamist. See teave on partneritele väärtuslik andmete migreerimiseks või üleviimiseks uue palgajuurutuse korral teisest süsteemist.
author: kherr75
manager: AnnBe
ms.date: 04/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e4bb8f565f5bf5630a7c5f8602b96e569692bc7c
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3005674"
---
# <a name="enter-payroll-beginning-balances"></a><span data-ttu-id="479e9-104">Palga algsaldode sisestamine</span><span class="sxs-lookup"><span data-stu-id="479e9-104">Enter payroll beginning balances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="479e9-105">Selles teemas kirjeldatakse tulukoodide, mahaarvamiste, soodustuste ja maksude algsaldode sisestamist.</span><span class="sxs-lookup"><span data-stu-id="479e9-105">The topic describes the steps for entering beginning balances for earning codes, deductions, benefits, and taxes.</span></span> <span data-ttu-id="479e9-106">See teave väärtuslik partneritele, kes viivad uue palgajuurutuse jaoks teisest süsteemist andmeid üle.</span><span class="sxs-lookup"><span data-stu-id="479e9-106">This information is valuable for partners who transfer data for a new Payroll implementation from another system.</span></span> <span data-ttu-id="479e9-107">Palgasaldode sisestamiseks valmistumisel kontrollime järgmisi andmeid.</span><span class="sxs-lookup"><span data-stu-id="479e9-107">To prepare to enter beginning payroll balances, we verify the following information:</span></span>

- <span data-ttu-id="479e9-108">Töötajakirjed on sisestatud ja süsteemis saadaval</span><span class="sxs-lookup"><span data-stu-id="479e9-108">Employee records are entered and available in the system</span></span>
- <span data-ttu-id="479e9-109">Järgmised andmed on seadistatud ja töötajatele määratud.</span><span class="sxs-lookup"><span data-stu-id="479e9-109">The following data is set up and assigned to employees:</span></span>

    - <span data-ttu-id="479e9-110">Palgatsüklid ja makseperioodid</span><span class="sxs-lookup"><span data-stu-id="479e9-110">Pay cycles and pay periods</span></span>
    - <span data-ttu-id="479e9-111">Tulukoodid</span><span class="sxs-lookup"><span data-stu-id="479e9-111">Earning codes</span></span>
    - <span data-ttu-id="479e9-112">Maksud</span><span class="sxs-lookup"><span data-stu-id="479e9-112">Taxes</span></span>
    - <span data-ttu-id="479e9-113">Soodustused ja mahaarvamised</span><span class="sxs-lookup"><span data-stu-id="479e9-113">Benefits and deductions</span></span>

- <span data-ttu-id="479e9-114">Ettevõte oleks pidanud valima kuupäeva, millele saab määrata palga algsaldosid.</span><span class="sxs-lookup"><span data-stu-id="479e9-114">The company should have chosen a date where payroll beginning balances can be set.</span></span>
- <span data-ttu-id="479e9-115">Andmeid koguti kõigi tulude, soodustuste/mahaarvamiste, soodustuse panuste, töötaja maksude ja tööandja maksude ning nende summad pärandsüsteemist jooksva aasta kohta.</span><span class="sxs-lookup"><span data-stu-id="479e9-115">Information were gathered on all earnings, benefits/deductions, benefit contributions, employee taxes, and employer taxes and their YTD amounts from the legacy system.</span></span>

<span data-ttu-id="479e9-116">Kui plaanite algsaldode sisestamist, siis mõelge, kui üksikasjalikud andmed olema peavad.</span><span class="sxs-lookup"><span data-stu-id="479e9-116">As you plan to enter beginning balances, consider how detailed the data needs to be.</span></span> <span data-ttu-id="479e9-117">Enamik ettevõtteid sisestab jooksva aasta kohta ühe konsolideeritud summa.</span><span class="sxs-lookup"><span data-stu-id="479e9-117">Most businesses enter a single, consolidated year-to-date amount.</span></span> <span data-ttu-id="479e9-118">Kuid kui on vaja täpsemaid andmeid, saab saldod sisestada kvartalivahemikena.</span><span class="sxs-lookup"><span data-stu-id="479e9-118">However if more detailed information is needed, balances can be entered in quarterly increments.</span></span> <span data-ttu-id="479e9-119">Vajaliku üksikasjataseme põhjal määratakse, mitu käsitsi palgaväljavõtet tuleb igale töötajale luua.</span><span class="sxs-lookup"><span data-stu-id="479e9-119">Deciding the level of detail that's needed determines how many manual pay statements must be created for each worker.</span></span> <span data-ttu-id="479e9-120">Ühe jooksva aasta summa puhul on iga töötaja jaoks vaja ainult ühte käsitsi väljavõtet.</span><span class="sxs-lookup"><span data-stu-id="479e9-120">For a single year-to-date amount, only one manual statement is needed for each employee.</span></span> <span data-ttu-id="479e9-121">Selleks kasutage jooksva aasta summasid eelmise süsteemi lõplikust palgaväljavõttest uude palgasüsteemi sisestatava summana.</span><span class="sxs-lookup"><span data-stu-id="479e9-121">To do this use year-to-date amounts from the final pay statement from the previous system as the amount entered in the new payroll system.</span></span>

<span data-ttu-id="479e9-122">Järgmises näites näidatakse, kuidas sisestada töötaja palga algsaldosid, sh tulukoode, soodustusi/mahaarvamisi ja makse.</span><span class="sxs-lookup"><span data-stu-id="479e9-122">The following example shows how you can enter employee payroll beginning balances, including earning codes, benefits/deductions, and taxes.</span></span> <span data-ttu-id="479e9-123">Tõsielulise näite puhul oleks teil iga tulukoodi jaoks reaüksus, soodustuse mahaarvamine, soodustuse panus, töötaja maks ja tööandja maks ja sisestatav summa oleks jooksva aasta summa.</span><span class="sxs-lookup"><span data-stu-id="479e9-123">In a real-world example you would have a line item for each earning code, benefit deduction, benefit contribution, employee tax and employer tax with the amount entered being the year-to-date amount.</span></span> <span data-ttu-id="479e9-124">Kasutades seda koodide ja summade loendit, järgige juhiseid käsitsi tulu- ja palgaväljavõtte loomiseks, nii et arvestus oleks keelatud, et tuua algsaldod palga jaoks üle.</span><span class="sxs-lookup"><span data-stu-id="479e9-124">Using that list of codes and amounts, follow the steps for creating a manual earning and pay statement with accounting disabled to bring over beginning balances for payroll purposes.</span></span> <span data-ttu-id="479e9-125">Arvestus tuleb keelata, kuna seda algsaldo palgaväljavõtet ei ole vaja pearaamatusse sisestada.</span><span class="sxs-lookup"><span data-stu-id="479e9-125">You disable accounting because you won't want to post this beginning balance pay statement to your general ledger.</span></span> <span data-ttu-id="479e9-126">See tehti pärandsüsteemis ja see tuleb uude süsteemi üle, kui määrate pearaamatus algsaldod.</span><span class="sxs-lookup"><span data-stu-id="479e9-126">That was done in the legacy system and will come over to the new system when you set beginning balances in General ledger.</span></span>

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a><span data-ttu-id="479e9-127">A.</span><span class="sxs-lookup"><span data-stu-id="479e9-127">A.</span></span> <span data-ttu-id="479e9-128">Palga algsaldodes kasutatavate tulukoodide seadistamine</span><span class="sxs-lookup"><span data-stu-id="479e9-128">How to set up earnings codes to be used on payroll beginning balances</span></span>

<span data-ttu-id="479e9-129">Palga algsaldode sisestamisel veenduge, et kasutatavad tulukoodide konfigureerimisel oleks valik Luba tuluväljavõtte määrade muutmine lubatud.</span><span class="sxs-lookup"><span data-stu-id="479e9-129">When you enter payroll beginning balances, be sure the earning codes that you will be using are configured with the "Allow editing of earning statement rates" option enabled.</span></span> <span data-ttu-id="479e9-130">See võimaldab summat pärandsüsteemist käsitsi sisestada.</span><span class="sxs-lookup"><span data-stu-id="479e9-130">This will allow you to manually key the amount from the legacy system.</span></span> 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a><span data-ttu-id="479e9-131">B.</span><span class="sxs-lookup"><span data-stu-id="479e9-131">B.</span></span> <span data-ttu-id="479e9-132">Töötajale tuluväljavõtte koostamine algsaldo jaoks</span><span class="sxs-lookup"><span data-stu-id="479e9-132">Create earnings statement for an employee to have a beginning balance</span></span>

<span data-ttu-id="479e9-133">See etapp loob käsitsi tuluväljavõtte iga töötaja jaoks pärandsüsteemi viimase palgaperioodi kohta, mis loob tuluväljavõtte read uues palgasüsteemis.</span><span class="sxs-lookup"><span data-stu-id="479e9-133">This step manually creates an earnings statement for each worker for the last pay period of the legacy system, which creates the earning statement lines in the new payroll system.</span></span> <span data-ttu-id="479e9-134">Sisestage üks rida tulukoodi kohta ning jooksva aasta summa ja tunnid.</span><span class="sxs-lookup"><span data-stu-id="479e9-134">Enter one line per earning code and the YTD amount and hours.</span></span> <span data-ttu-id="479e9-135">Näidisetapid on järgmised.</span><span class="sxs-lookup"><span data-stu-id="479e9-135">The sample steps are as follows:</span></span>

1. <span data-ttu-id="479e9-136">Avage leht **Kõik tuluväljavõtted** ja klõpsake nuppu **Uus**.</span><span class="sxs-lookup"><span data-stu-id="479e9-136">Open the **All earnings statements** page and click **New**.</span></span>

    <span data-ttu-id="479e9-137">Sisestage järgnev.</span><span class="sxs-lookup"><span data-stu-id="479e9-137">Enter the following:</span></span> 

    | <span data-ttu-id="479e9-138">Väli</span><span class="sxs-lookup"><span data-stu-id="479e9-138">Field</span></span>      | <span data-ttu-id="479e9-139">Väärtus</span><span class="sxs-lookup"><span data-stu-id="479e9-139">Value</span></span>                 |
    |------------|-----------------------|
    | <span data-ttu-id="479e9-140">Töötaja</span><span class="sxs-lookup"><span data-stu-id="479e9-140">Worker</span></span>     | <span data-ttu-id="479e9-141">Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="479e9-141">Michael Redmond</span></span>       |
    | <span data-ttu-id="479e9-142">Palgatsükkel</span><span class="sxs-lookup"><span data-stu-id="479e9-142">Pay cycle</span></span>  | <span data-ttu-id="479e9-143">sm</span><span class="sxs-lookup"><span data-stu-id="479e9-143">sm</span></span>                    |
    | <span data-ttu-id="479e9-144">Makseperiood</span><span class="sxs-lookup"><span data-stu-id="479e9-144">Pay period</span></span> | <span data-ttu-id="479e9-145">6/16/2017 - 6/30/2017</span><span class="sxs-lookup"><span data-stu-id="479e9-145">6/16/2017 - 6/30/2017</span></span> |

2. <span data-ttu-id="479e9-146">Sisestage vahekaardile **Tuluväljavõtte rida** järgmised andmed.</span><span class="sxs-lookup"><span data-stu-id="479e9-146">In the **Earnings statement line** tab, enter the following:</span></span>

    <span data-ttu-id="479e9-147">Rida 1: vahekaart **Tuluväljavõtte rida**</span><span class="sxs-lookup"><span data-stu-id="479e9-147">Line 1: **Earning statement line** tab</span></span>

    | <span data-ttu-id="479e9-148">Väli</span><span class="sxs-lookup"><span data-stu-id="479e9-148">Field</span></span>            | <span data-ttu-id="479e9-149">Väärtus</span><span class="sxs-lookup"><span data-stu-id="479e9-149">Value</span></span>       |
    |------------------|-------------|
    | <span data-ttu-id="479e9-150">Tulukood</span><span class="sxs-lookup"><span data-stu-id="479e9-150">Earnings code</span></span>    | <span data-ttu-id="479e9-151">Regulaarne palk</span><span class="sxs-lookup"><span data-stu-id="479e9-151">Regular pay</span></span> |
    | <span data-ttu-id="479e9-152">Kogus</span><span class="sxs-lookup"><span data-stu-id="479e9-152">Quantity</span></span>         | <span data-ttu-id="479e9-153">1.00</span><span class="sxs-lookup"><span data-stu-id="479e9-153">1.00</span></span>        |
    | <span data-ttu-id="479e9-154">Kurss</span><span class="sxs-lookup"><span data-stu-id="479e9-154">Rate</span></span>             | <span data-ttu-id="479e9-155">30,000</span><span class="sxs-lookup"><span data-stu-id="479e9-155">30,000</span></span>      |
    | <span data-ttu-id="479e9-156">Rea üksikasjade vahekaart</span><span class="sxs-lookup"><span data-stu-id="479e9-156">Line details tab</span></span> |             |
    | <span data-ttu-id="479e9-157">Käsitsi</span><span class="sxs-lookup"><span data-stu-id="479e9-157">Manual</span></span>           | <span data-ttu-id="479e9-158">(märgitud)</span><span class="sxs-lookup"><span data-stu-id="479e9-158">(marked)</span></span>    |

    <span data-ttu-id="479e9-159">Rida 2: vahekaart **Tuluväljavõtte rida**</span><span class="sxs-lookup"><span data-stu-id="479e9-159">Line 2: **Earning statement line** tab</span></span>

    | <span data-ttu-id="479e9-160">Väli</span><span class="sxs-lookup"><span data-stu-id="479e9-160">Field</span></span>            | <span data-ttu-id="479e9-161">Väärtus</span><span class="sxs-lookup"><span data-stu-id="479e9-161">Value</span></span>    |
    |------------------|----------|
    | <span data-ttu-id="479e9-162">Tulukood</span><span class="sxs-lookup"><span data-stu-id="479e9-162">Earnings code</span></span>    | <span data-ttu-id="479e9-163">Preemia</span><span class="sxs-lookup"><span data-stu-id="479e9-163">Bonus</span></span>    |
    | <span data-ttu-id="479e9-164">Kogus</span><span class="sxs-lookup"><span data-stu-id="479e9-164">Quantity</span></span>         | <span data-ttu-id="479e9-165">1.0000</span><span class="sxs-lookup"><span data-stu-id="479e9-165">1.0000</span></span>   |
    | <span data-ttu-id="479e9-166">Kurss</span><span class="sxs-lookup"><span data-stu-id="479e9-166">Rate</span></span>             | <span data-ttu-id="479e9-167">4250.00</span><span class="sxs-lookup"><span data-stu-id="479e9-167">4250.00</span></span>  |
    | <span data-ttu-id="479e9-168">Rea üksikasjade vahekaart</span><span class="sxs-lookup"><span data-stu-id="479e9-168">Line details tab</span></span> |          |
    | <span data-ttu-id="479e9-169">Käsitsi</span><span class="sxs-lookup"><span data-stu-id="479e9-169">Manual</span></span>           | <span data-ttu-id="479e9-170">(märgitud)</span><span class="sxs-lookup"><span data-stu-id="479e9-170">(marked)</span></span> |

    <span data-ttu-id="479e9-171">Rida 3: vahekaart **Tuluväljavõtte rida**</span><span class="sxs-lookup"><span data-stu-id="479e9-171">Line 3: **Earning statement line** tab</span></span>

    | <span data-ttu-id="479e9-172">Väli</span><span class="sxs-lookup"><span data-stu-id="479e9-172">Field</span></span>           | <span data-ttu-id="479e9-173">Väärtus</span><span class="sxs-lookup"><span data-stu-id="479e9-173">Value</span></span>      |
    |-----------------|------------|
    | <span data-ttu-id="479e9-174">Tulukood</span><span class="sxs-lookup"><span data-stu-id="479e9-174">Earnings code</span></span>   | <span data-ttu-id="479e9-175">Komisjonitasu</span><span class="sxs-lookup"><span data-stu-id="479e9-175">Commission</span></span> |
    | <span data-ttu-id="479e9-176">Kogus</span><span class="sxs-lookup"><span data-stu-id="479e9-176">Quantity</span></span>        | <span data-ttu-id="479e9-177">1.0000</span><span class="sxs-lookup"><span data-stu-id="479e9-177">1.0000</span></span>     |
    | <span data-ttu-id="479e9-178">Kurss</span><span class="sxs-lookup"><span data-stu-id="479e9-178">Rate</span></span>            | <span data-ttu-id="479e9-179">!,299.00</span><span class="sxs-lookup"><span data-stu-id="479e9-179">!,299.00</span></span>   |
    | <span data-ttu-id="479e9-180">Kurss</span><span class="sxs-lookup"><span data-stu-id="479e9-180">Rate</span></span>            | <span data-ttu-id="479e9-181">1,299.00</span><span class="sxs-lookup"><span data-stu-id="479e9-181">1,299.00</span></span>   |
    | <span data-ttu-id="479e9-182">Rea üksikasjade vahekaart</span><span class="sxs-lookup"><span data-stu-id="479e9-182">Line detail tab</span></span> |            |
    | <span data-ttu-id="479e9-183">Käsitsi</span><span class="sxs-lookup"><span data-stu-id="479e9-183">Manual</span></span>          | <span data-ttu-id="479e9-184">(märgitud)</span><span class="sxs-lookup"><span data-stu-id="479e9-184">(Marked)</span></span>   |

    > [!NOTE]
    > <span data-ttu-id="479e9-185">Iga tuluväljavõtte rea puhul vahekaardil **Rea üksikasjad** liuguri **Käsitsi** lükkamine valikule **Jah** on iga töötaja puhul palga algsaldode sisestamiseks oluline.</span><span class="sxs-lookup"><span data-stu-id="479e9-185">Setting the **Manual** slider to **Yes** in the **Line Details** tab for each earnings statement line is key to have payroll beginning balances entered for each worker.</span></span>

3. <span data-ttu-id="479e9-186">Klõpsake paanil **Tegevus** valikut **Tuluväljavõtte väljastamine** USA-FED-ER-FICA.</span><span class="sxs-lookup"><span data-stu-id="479e9-186">On the **Action** pane, click **Release earnings statement** USA-FED-ER-FICA.</span></span>
4. <span data-ttu-id="479e9-187">Klõpsake paanil **Tegevus** valikut **Palgaväljavõte** lehe **Palgaväljavõtete loomine** avamiseks ja seadistage järgmised valikud.</span><span class="sxs-lookup"><span data-stu-id="479e9-187">On the **Action** pane click **Pay statement** to open the **Generate pay statements** page and set the following:</span></span>

    | <span data-ttu-id="479e9-188">Väli</span><span class="sxs-lookup"><span data-stu-id="479e9-188">Field</span></span>              | <span data-ttu-id="479e9-189">Väärtus</span><span class="sxs-lookup"><span data-stu-id="479e9-189">Value</span></span>     |
    |--------------------|-----------|
    | <span data-ttu-id="479e9-190">Maksekuupäev</span><span class="sxs-lookup"><span data-stu-id="479e9-190">Payment date</span></span>       | <span data-ttu-id="479e9-191">6/30/2017</span><span class="sxs-lookup"><span data-stu-id="479e9-191">6/30/2017</span></span> |
    | <span data-ttu-id="479e9-192">Maksetsükli tüüp</span><span class="sxs-lookup"><span data-stu-id="479e9-192">Payment run type</span></span>   | <span data-ttu-id="479e9-193">Käsitsi</span><span class="sxs-lookup"><span data-stu-id="479e9-193">Manual</span></span>    |
    | <span data-ttu-id="479e9-194">Keela raamatupidamine</span><span class="sxs-lookup"><span data-stu-id="479e9-194">Disable accounting</span></span> |   <span data-ttu-id="479e9-195">Jah</span><span class="sxs-lookup"><span data-stu-id="479e9-195">Yes</span></span>     |

    > [!NOTE] 
    > <span data-ttu-id="479e9-196">See on saadaval ainult siis, kui makse käitamise tüüp on käsitsi ja kui kasutaja soovib maksetsükli arvestuse keelata.</span><span class="sxs-lookup"><span data-stu-id="479e9-196">This is only available when the payment run type is manual and wherein the user want to disable accounting on the pay run.</span></span>

    <span data-ttu-id="479e9-197">Klõpsake nuppu **OK** ja sulgege **teabelogi**.</span><span class="sxs-lookup"><span data-stu-id="479e9-197">Click **OK** and close the **Infolog**.</span></span>

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a><span data-ttu-id="479e9-198">Miks peab liugur Keela arvestus olema makseväljavõtete loomisel seatud valikule Jah?</span><span class="sxs-lookup"><span data-stu-id="479e9-198">Why the Disable Accounting slider needs to set to Yes when generating pay statements?</span></span>

<span data-ttu-id="479e9-199">Liuguri seadmine valikule **Jah** takistab makseväljavõtte levitamist ja sisestamist pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="479e9-199">Setting the slider to **Yes** prevents lines in the pay statement from being districuted to General ledger.</span></span> <span data-ttu-id="479e9-200">Pearaamatu summasid värskendati varem, kui sisestati kontosaldod pärandsüsteemist.</span><span class="sxs-lookup"><span data-stu-id="479e9-200">General ledger amounts were updating earlier when account balances from the legacy system were entered.</span></span> <span data-ttu-id="479e9-201">Palgaarvestuse algsaldode sisestamine võimaldab luua aruanded, mis sisaldavad teavet varasematest aastatest, samuti tuvastada soodustuste piirangud ja maksuotstarbed.</span><span class="sxs-lookup"><span data-stu-id="479e9-201">Entering beginning balances for Payroll lets you generate reports that include information from prior years, as well as for identifying limits for benefit and tax purposes.</span></span>

### <a name="c-create-pay-statements-for-employees"></a><span data-ttu-id="479e9-202">C.</span><span class="sxs-lookup"><span data-stu-id="479e9-202">C.</span></span> <span data-ttu-id="479e9-203">Töötajatele palgaväljavõtete koostamine</span><span class="sxs-lookup"><span data-stu-id="479e9-203">Create pay statements for employees</span></span>

<span data-ttu-id="479e9-204">Pärast algsaldodega palgaväljavõtete koostamist tuleb kontrollida, et palgaväljavõtted kajastaksid täpselt palgaandmeid.</span><span class="sxs-lookup"><span data-stu-id="479e9-204">After you generate pay statements that have beginning balances, you must verify that the pay statements accurately reflect payroll data.</span></span> <span data-ttu-id="479e9-205">Soodustuste ja maksude teave tuleb samuti käsitsi uuendada, et see vastaks eelmises palgasüsteemis olevatele väärtustele.</span><span class="sxs-lookup"><span data-stu-id="479e9-205">You must also manually update the benefit and taxes information to match the values in the previous payroll system.</span></span> <span data-ttu-id="479e9-206">Pärast kontrollimist, et eelmise palgasüsteemi summad vastavad praeguste palgaväljavõtete summadele, tuleb palgaväljavõtted lõpetada.</span><span class="sxs-lookup"><span data-stu-id="479e9-206">After you verify that the amounts from the previous payroll system match the amounts on the current pay statements, you must finalize the pay statements.</span></span>

1. <span data-ttu-id="479e9-207">Avage leht **Kõik palgaväljavõtted**.</span><span class="sxs-lookup"><span data-stu-id="479e9-207">Open the **All pay statements** page.</span></span>
2. <span data-ttu-id="479e9-208">Tõstke esile viimati Michael Redmondile koostatud palgaväljavõte</span><span class="sxs-lookup"><span data-stu-id="479e9-208">Highlight the last generated pay statement for Michael Redmond</span></span>
3. <span data-ttu-id="479e9-209">Klõpsake nuppu **Redigeeri** lehe **Palgaväljavõte** avamiseks.</span><span class="sxs-lookup"><span data-stu-id="479e9-209">Click **Edit** to open the **Pay statement** page.</span></span>
4. <span data-ttu-id="479e9-210">Avage vahekaart **Soodustuse mahaarvamised** ja sisestage järgmine.</span><span class="sxs-lookup"><span data-stu-id="479e9-210">Open the **Benefit deductions** tab and enter the following:</span></span>

    | <span data-ttu-id="479e9-211">Väli</span><span class="sxs-lookup"><span data-stu-id="479e9-211">Field</span></span>             | <span data-ttu-id="479e9-212">Väärtus</span><span class="sxs-lookup"><span data-stu-id="479e9-212">Value</span></span>            |
    |-------------------|------------------|
    | <span data-ttu-id="479e9-213">Soodustus</span><span class="sxs-lookup"><span data-stu-id="479e9-213">Benefit</span></span>           | <span data-ttu-id="479e9-214">Mahaarvatav summa</span><span class="sxs-lookup"><span data-stu-id="479e9-214">Deduction amount</span></span> |
    | <span data-ttu-id="479e9-215">401K</span><span class="sxs-lookup"><span data-stu-id="479e9-215">401K</span></span>              | <span data-ttu-id="479e9-216">Osalus</span><span class="sxs-lookup"><span data-stu-id="479e9-216">Participate</span></span>      |
    | <span data-ttu-id="479e9-217">Hambaravikindlustus</span><span class="sxs-lookup"><span data-stu-id="479e9-217">Dental</span></span>            | <span data-ttu-id="479e9-218">SubSp</span><span class="sxs-lookup"><span data-stu-id="479e9-218">SubSp</span></span>            |
    | <span data-ttu-id="479e9-219">Osak. kulutused ravikindlustusele</span><span class="sxs-lookup"><span data-stu-id="479e9-219">Dep care spending</span></span> | <span data-ttu-id="479e9-220">Osalus</span><span class="sxs-lookup"><span data-stu-id="479e9-220">Participate</span></span>      |
    | <span data-ttu-id="479e9-221">Visioon</span><span class="sxs-lookup"><span data-stu-id="479e9-221">Vision</span></span>            | <span data-ttu-id="479e9-222">SupSp</span><span class="sxs-lookup"><span data-stu-id="479e9-222">SupSp</span></span>            |

5. <span data-ttu-id="479e9-223">Sisestage vahekaardile **Soodustuse panused** järgmine.</span><span class="sxs-lookup"><span data-stu-id="479e9-223">In the **Benefit contributions** tab and enter the following:</span></span>

    | <span data-ttu-id="479e9-224">Väli</span><span class="sxs-lookup"><span data-stu-id="479e9-224">Field</span></span>   | <span data-ttu-id="479e9-225">Väärtus</span><span class="sxs-lookup"><span data-stu-id="479e9-225">Value</span></span>               |
    |---------|---------------------|
    | <span data-ttu-id="479e9-226">Soodustus</span><span class="sxs-lookup"><span data-stu-id="479e9-226">Benefit</span></span> | <span data-ttu-id="479e9-227">Panuse summa</span><span class="sxs-lookup"><span data-stu-id="479e9-227">Contribution amount</span></span> |
    | <span data-ttu-id="479e9-228">401K</span><span class="sxs-lookup"><span data-stu-id="479e9-228">401K</span></span>    | <span data-ttu-id="479e9-229">Osalus</span><span class="sxs-lookup"><span data-stu-id="479e9-229">Participate</span></span>         |
    | <span data-ttu-id="479e9-230">Hambaravikindlustus</span><span class="sxs-lookup"><span data-stu-id="479e9-230">Dental</span></span>  | <span data-ttu-id="479e9-231">SubSp</span><span class="sxs-lookup"><span data-stu-id="479e9-231">SubSp</span></span>               |
    | <span data-ttu-id="479e9-232">Visioon</span><span class="sxs-lookup"><span data-stu-id="479e9-232">Vision</span></span>  | <span data-ttu-id="479e9-233">SubSp</span><span class="sxs-lookup"><span data-stu-id="479e9-233">SubSp</span></span>               |

6. <span data-ttu-id="479e9-234">Sisestage vahekaardile **Maksude mahaarvamised** järgmine.</span><span class="sxs-lookup"><span data-stu-id="479e9-234">In the **Tax deductions** tab, enter the following:</span></span>

    | <span data-ttu-id="479e9-235">Väli</span><span class="sxs-lookup"><span data-stu-id="479e9-235">Field</span></span>           | <span data-ttu-id="479e9-236">Väärtus</span><span class="sxs-lookup"><span data-stu-id="479e9-236">Value</span></span>            |
    |-----------------|------------------|
    | <span data-ttu-id="479e9-237">Maksukood</span><span class="sxs-lookup"><span data-stu-id="479e9-237">Tax code</span></span>        | <span data-ttu-id="479e9-238">Mahaarvatav summa</span><span class="sxs-lookup"><span data-stu-id="479e9-238">Deduction amount</span></span> |
    | <span data-ttu-id="479e9-239">USA-FED-ER-FICA</span><span class="sxs-lookup"><span data-stu-id="479e9-239">USA-FED-ER-FICA</span></span> | <span data-ttu-id="479e9-240">1600.00</span><span class="sxs-lookup"><span data-stu-id="479e9-240">1600.00</span></span>          |
    | <span data-ttu-id="479e9-241">USA-FED-ER-MEDI</span><span class="sxs-lookup"><span data-stu-id="479e9-241">USA-FED-ER-MEDI</span></span> | <span data-ttu-id="479e9-242">825.75</span><span class="sxs-lookup"><span data-stu-id="479e9-242">825.75</span></span>           |

7. <span data-ttu-id="479e9-243">Sisestage vahekaardile **Maksude panused** järgmine.</span><span class="sxs-lookup"><span data-stu-id="479e9-243">In the **Tax contributions** tab enter the following:</span></span>
8. <span data-ttu-id="479e9-244">Klõpsake valikut **Arvuta**.</span><span class="sxs-lookup"><span data-stu-id="479e9-244">Click **Calculate**.</span></span>

    > [!IMPORTANT] 
    > <span data-ttu-id="479e9-245">Kontrollige töötaja makseväljavõtete kogusummade vastavust pärandsüsteemi jooksva aasta summadele.</span><span class="sxs-lookup"><span data-stu-id="479e9-245">Validate the totals of the pay statement that they match the YTD of the legacy system for the worker.</span></span> <span data-ttu-id="479e9-246">Järgmises etapis võib olla vaja lõpetamisega oodata, et oleks võimalik kõiki palgaväljavõtteid üldiselt kontrollida.</span><span class="sxs-lookup"><span data-stu-id="479e9-246">You may want to hold off on finalizing in the next step to do some overall validating of all pay statements in aggregate.</span></span> <span data-ttu-id="479e9-247">Kui palgaväljavõtted on kontrollitud, vaadake need läbi ja lõpetage need.</span><span class="sxs-lookup"><span data-stu-id="479e9-247">Once validated run through all the pay statements and finalize them.</span></span>

<span data-ttu-id="479e9-248">Sama protsessi saab teha vajaduse korral kvartalite kaupa iga aasta kõigi eelmiste kvartalite kohta.</span><span class="sxs-lookup"><span data-stu-id="479e9-248">The same process can be done in quarter increments if necessary for all prior quarters in each year.</span></span> <span data-ttu-id="479e9-249">See on vajalik ainult juhul, kui kliendil on vaja andmeid kvartalite kaupa näha, pärandsüsteemi naasmata.</span><span class="sxs-lookup"><span data-stu-id="479e9-249">This is only needed if the customer needs to see the data by quarter without going back to the legacy system.</span></span>

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a><span data-ttu-id="479e9-250">Kui teete töötaja algsaldode sisestamisel vea,</span><span class="sxs-lookup"><span data-stu-id="479e9-250">If you make a mistake Entering Beginning Balances for an Employee</span></span>

<span data-ttu-id="479e9-251">on võimalik kandeid tühistada ja uuesti sisestada.</span><span class="sxs-lookup"><span data-stu-id="479e9-251">It is possible to reverse and reenter transactions.</span></span> <span data-ttu-id="479e9-252">Kande tühistamiseks peate tegema lehel **Kõik palgaväljavõtted** järgmised toimingud.</span><span class="sxs-lookup"><span data-stu-id="479e9-252">To reverse the transaction, all you have to do is to complete the follow steps on the **All pay statements** page.</span></span>

1. <span data-ttu-id="479e9-253">Klõpsake valikut **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="479e9-253">Click **Reverse**.</span></span>
2. <span data-ttu-id="479e9-254">Klõpsake **Jah**, kui kuvatakse teade „Selle palgaväljavõtte tühistamisel luuakse tühistav palgaväljavõte selle palgaväljavõtte tasakaalustamiseks.</span><span class="sxs-lookup"><span data-stu-id="479e9-254">Click **Yes** when the message "When you reverse this pay statement, a reversing pay statement will be created to offset this pay statement.</span></span> <span data-ttu-id="479e9-255">Kumbagi palgaväljavõtet ei saa muuta.</span><span class="sxs-lookup"><span data-stu-id="479e9-255">Neither pay statement can be edited.</span></span> <span data-ttu-id="479e9-256">Kas soovite selle palgaväljavõtte tühistada?”</span><span class="sxs-lookup"><span data-stu-id="479e9-256">Do you want to reverse this pay statement?"</span></span> <span data-ttu-id="479e9-257">.</span><span class="sxs-lookup"><span data-stu-id="479e9-257">displays.</span></span> 

<span data-ttu-id="479e9-258">Kui olete palgaväljavõtte tühistanud, saate luua uue palgaväljavõtte töötaja jaoks varem loodud tuluväljavõtte põhjal.</span><span class="sxs-lookup"><span data-stu-id="479e9-258">After you reverse the pay statement, you can generate a new pay statement for the worker from the earnings statement that you created previously.</span></span> <span data-ttu-id="479e9-259">Korrigeerige kindlasti kõik tuluväljavõtte valed read, enne kui loote uue palgaväljavõtte, ja seejärel looge uued palgaväljavõtted õigete summadega.</span><span class="sxs-lookup"><span data-stu-id="479e9-259">Be sure to fix any incorrect lines on the earnings statement before you generate the new pay statement, and then generate new pay statements with the correct amounts.</span></span> 
