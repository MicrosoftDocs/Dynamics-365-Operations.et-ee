---
title: Palga algsaldode sisestamine
description: Selles teemas kirjeldatakse tulukoodide, mahaarvamiste, soodustuste ja maksude algsaldode sisestamist.
author: andreabichsel
ms.date: 11/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: 20931
ms.assetid: b48b1cb2-6e66-467e-9c0e-09b6a4aeb9fe
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2017-07-01
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9272828fe5d6e0bf131ea66353a0d5c3c7b1c4bd
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5752146"
---
# <a name="enter-payroll-beginning-balances"></a><span data-ttu-id="5c064-103">Palga algsaldode sisestamine</span><span class="sxs-lookup"><span data-stu-id="5c064-103">Enter payroll beginning balances</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="5c064-104">Selles teemas kirjeldatakse tulukoodide, mahaarvamiste, soodustuste ja maksude algsaldode sisestamist.</span><span class="sxs-lookup"><span data-stu-id="5c064-104">The topic describes the steps for entering beginning balances for earning codes, deductions, benefits, and taxes.</span></span> <span data-ttu-id="5c064-105">See teave väärtuslik partneritele, kes viivad uue palgajuurutuse jaoks teisest süsteemist andmeid üle.</span><span class="sxs-lookup"><span data-stu-id="5c064-105">This information is valuable for partners who transfer data for a new Payroll implementation from another system.</span></span> <span data-ttu-id="5c064-106">Palgasaldode sisestamiseks valmistumisel kontrollime järgmisi andmeid.</span><span class="sxs-lookup"><span data-stu-id="5c064-106">To prepare to enter beginning payroll balances, we verify the following information:</span></span>

- <span data-ttu-id="5c064-107">Töötajakirjed on sisestatud ja süsteemis saadaval</span><span class="sxs-lookup"><span data-stu-id="5c064-107">Employee records are entered and available in the system</span></span>
- <span data-ttu-id="5c064-108">Järgmised andmed on seadistatud ja töötajatele määratud.</span><span class="sxs-lookup"><span data-stu-id="5c064-108">The following data is set up and assigned to employees:</span></span>

    - <span data-ttu-id="5c064-109">Palgatsüklid ja makseperioodid</span><span class="sxs-lookup"><span data-stu-id="5c064-109">Pay cycles and pay periods</span></span>
    - <span data-ttu-id="5c064-110">Tulukoodid</span><span class="sxs-lookup"><span data-stu-id="5c064-110">Earning codes</span></span>
    - <span data-ttu-id="5c064-111">Maksud</span><span class="sxs-lookup"><span data-stu-id="5c064-111">Taxes</span></span>
    - <span data-ttu-id="5c064-112">Soodustused ja mahaarvamised</span><span class="sxs-lookup"><span data-stu-id="5c064-112">Benefits and deductions</span></span>

- <span data-ttu-id="5c064-113">Ettevõte oleks pidanud valima kuupäeva, millele saab määrata palga algsaldosid.</span><span class="sxs-lookup"><span data-stu-id="5c064-113">The company should have chosen a date where payroll beginning balances can be set.</span></span>
- <span data-ttu-id="5c064-114">Andmeid koguti kõigi tulude, soodustuste/mahaarvamiste, soodustuse panuste, töötaja maksude ja tööandja maksude ning nende summad pärandsüsteemist jooksva aasta kohta.</span><span class="sxs-lookup"><span data-stu-id="5c064-114">Information was gathered on all earnings, benefits/deductions, benefit contributions, employee taxes, and employer taxes and their YTD amounts from the legacy system.</span></span>

<span data-ttu-id="5c064-115">Kui plaanite algsaldode sisestamist, siis mõelge, kui üksikasjalikud andmed olema peavad.</span><span class="sxs-lookup"><span data-stu-id="5c064-115">As you plan to enter beginning balances, consider how detailed the data needs to be.</span></span> <span data-ttu-id="5c064-116">Enamik ettevõtteid sisestab jooksva aasta kohta ühe konsolideeritud summa.</span><span class="sxs-lookup"><span data-stu-id="5c064-116">Most businesses enter a single, consolidated year-to-date amount.</span></span> <span data-ttu-id="5c064-117">Kuid kui on vaja täpsemaid andmeid, saab saldod sisestada kvartalivahemikena.</span><span class="sxs-lookup"><span data-stu-id="5c064-117">However if more detailed information is needed, balances can be entered in quarterly increments.</span></span> <span data-ttu-id="5c064-118">Vajaliku üksikasjataseme põhjal määratakse, mitu käsitsi palgaväljavõtet tuleb igale töötajale luua.</span><span class="sxs-lookup"><span data-stu-id="5c064-118">Deciding the level of detail that's needed determines how many manual pay statements must be created for each worker.</span></span> <span data-ttu-id="5c064-119">Ühe jooksva aasta summa puhul on iga töötaja jaoks vaja ainult ühte käsitsi väljavõtet.</span><span class="sxs-lookup"><span data-stu-id="5c064-119">For a single year-to-date amount, only one manual statement is needed for each employee.</span></span> <span data-ttu-id="5c064-120">Selleks kasutage jooksva aasta summasid eelmise süsteemi lõplikust palgaväljavõttest uude palgasüsteemi sisestatava summana.</span><span class="sxs-lookup"><span data-stu-id="5c064-120">To do this, use year-to-date amounts from the final pay statement from the previous system as the amount entered in the new payroll system.</span></span>

<span data-ttu-id="5c064-121">Järgmises näites näidatakse, kuidas sisestada töötaja palga algsaldosid, sh tulukoode, soodustusi/mahaarvamisi ja makse.</span><span class="sxs-lookup"><span data-stu-id="5c064-121">The following example shows how you can enter employee payroll beginning balances, including earning codes, benefits/deductions, and taxes.</span></span> <span data-ttu-id="5c064-122">Tõsielulise näite puhul oleks teil iga tulukoodi jaoks reaüksus, soodustuse mahaarvamine, soodustuse panus, töötaja maks ja tööandja maks ja sisestatav summa oleks jooksva aasta summa.</span><span class="sxs-lookup"><span data-stu-id="5c064-122">In a real-world example you would have a line item for each earning code, benefit deduction, benefit contribution, employee tax and employer tax with the amount entered being the year-to-date amount.</span></span> <span data-ttu-id="5c064-123">Kasutades seda koodide ja summade loendit, järgige juhiseid käsitsi tulu- ja palgaväljavõtte loomiseks, nii et arvestus oleks keelatud, et tuua algsaldod palga jaoks üle.</span><span class="sxs-lookup"><span data-stu-id="5c064-123">Using that list of codes and amounts, follow the steps for creating a manual earning and pay statement with accounting disabled to bring over beginning balances for payroll purposes.</span></span> <span data-ttu-id="5c064-124">Arvestus tuleb keelata, kuna seda algsaldo palgaväljavõtet ei ole vaja pearaamatusse sisestada.</span><span class="sxs-lookup"><span data-stu-id="5c064-124">You disable accounting because you won't want to post this beginning balance pay statement to your general ledger.</span></span> <span data-ttu-id="5c064-125">See tehti pärandsüsteemis ja see tuleb uude süsteemi üle, kui määrate pearaamatus algsaldod.</span><span class="sxs-lookup"><span data-stu-id="5c064-125">That was done in the legacy system and will come over to the new system when you set beginning balances in General ledger.</span></span>

### <a name="a-how-to-set-up-earnings-codes-to-be-used-on-payroll-beginning-balances"></a><span data-ttu-id="5c064-126">A.</span><span class="sxs-lookup"><span data-stu-id="5c064-126">A.</span></span> <span data-ttu-id="5c064-127">Palga algsaldodes kasutatavate tulukoodide seadistamine</span><span class="sxs-lookup"><span data-stu-id="5c064-127">How to set up earnings codes to be used on payroll beginning balances</span></span>

<span data-ttu-id="5c064-128">Palga algsaldode sisestamisel veenduge, et kasutatavad tulukoodide konfigureerimisel oleks valik Luba tuluväljavõtte määrade muutmine lubatud.</span><span class="sxs-lookup"><span data-stu-id="5c064-128">When you enter payroll beginning balances, be sure the earning codes that you will be using are configured with the "Allow editing of earning statement rates" option enabled.</span></span> <span data-ttu-id="5c064-129">See võimaldab summat pärandsüsteemist käsitsi sisestada.</span><span class="sxs-lookup"><span data-stu-id="5c064-129">This will allow you to manually key the amount from the legacy system.</span></span> 

### <a name="b-create-earnings-statement-for-an-employee-to-have-a-beginning-balance"></a><span data-ttu-id="5c064-130">B.</span><span class="sxs-lookup"><span data-stu-id="5c064-130">B.</span></span> <span data-ttu-id="5c064-131">Töötajale tuluväljavõtte koostamine algsaldo jaoks</span><span class="sxs-lookup"><span data-stu-id="5c064-131">Create earnings statement for an employee to have a beginning balance</span></span>

<span data-ttu-id="5c064-132">See etapp loob käsitsi tuluväljavõtte iga töötaja jaoks pärandsüsteemi viimase palgaperioodi kohta, mis loob tuluväljavõtte read uues palgasüsteemis.</span><span class="sxs-lookup"><span data-stu-id="5c064-132">This step manually creates an earnings statement for each worker for the last pay period of the legacy system, which creates the earning statement lines in the new payroll system.</span></span> <span data-ttu-id="5c064-133">Sisestage üks rida tulukoodi kohta ning jooksva aasta summa ja tunnid.</span><span class="sxs-lookup"><span data-stu-id="5c064-133">Enter one line per earning code and the YTD amount and hours.</span></span> <span data-ttu-id="5c064-134">Näidisetapid on järgmised.</span><span class="sxs-lookup"><span data-stu-id="5c064-134">The sample steps are as follows:</span></span>

1. <span data-ttu-id="5c064-135">Avage leht **Kõik tuluväljavõtted** ja klõpsake nuppu **Uus**.</span><span class="sxs-lookup"><span data-stu-id="5c064-135">Open the **All earnings statements** page and click **New**.</span></span>

    <span data-ttu-id="5c064-136">Sisestage järgnev.</span><span class="sxs-lookup"><span data-stu-id="5c064-136">Enter the following:</span></span> 

    | <span data-ttu-id="5c064-137">Väli</span><span class="sxs-lookup"><span data-stu-id="5c064-137">Field</span></span>      | <span data-ttu-id="5c064-138">Väärtus</span><span class="sxs-lookup"><span data-stu-id="5c064-138">Value</span></span>                 |
    |------------|-----------------------|
    | <span data-ttu-id="5c064-139">Töötaja</span><span class="sxs-lookup"><span data-stu-id="5c064-139">Worker</span></span>     | <span data-ttu-id="5c064-140">Michael Redmond</span><span class="sxs-lookup"><span data-stu-id="5c064-140">Michael Redmond</span></span>       |
    | <span data-ttu-id="5c064-141">Palgatsükkel</span><span class="sxs-lookup"><span data-stu-id="5c064-141">Pay cycle</span></span>  | <span data-ttu-id="5c064-142">sm</span><span class="sxs-lookup"><span data-stu-id="5c064-142">sm</span></span>                    |
    | <span data-ttu-id="5c064-143">Makseperiood</span><span class="sxs-lookup"><span data-stu-id="5c064-143">Pay period</span></span> | <span data-ttu-id="5c064-144">6/16/2017 - 6/30/2017</span><span class="sxs-lookup"><span data-stu-id="5c064-144">6/16/2017 - 6/30/2017</span></span> |

2. <span data-ttu-id="5c064-145">Sisestage vahekaardile **Tuluväljavõtte rida** järgmised andmed.</span><span class="sxs-lookup"><span data-stu-id="5c064-145">In the **Earnings statement line** tab, enter the following:</span></span>

    <span data-ttu-id="5c064-146">Rida 1: vahekaart **Tuluväljavõtte rida**</span><span class="sxs-lookup"><span data-stu-id="5c064-146">Line 1: **Earning statement line** tab</span></span>

    | <span data-ttu-id="5c064-147">Väli</span><span class="sxs-lookup"><span data-stu-id="5c064-147">Field</span></span>            | <span data-ttu-id="5c064-148">Väärtus</span><span class="sxs-lookup"><span data-stu-id="5c064-148">Value</span></span>       |
    |------------------|-------------|
    | <span data-ttu-id="5c064-149">Tulukood</span><span class="sxs-lookup"><span data-stu-id="5c064-149">Earnings code</span></span>    | <span data-ttu-id="5c064-150">Regulaarne palk</span><span class="sxs-lookup"><span data-stu-id="5c064-150">Regular pay</span></span> |
    | <span data-ttu-id="5c064-151">Kogus</span><span class="sxs-lookup"><span data-stu-id="5c064-151">Quantity</span></span>         | <span data-ttu-id="5c064-152">1.00</span><span class="sxs-lookup"><span data-stu-id="5c064-152">1.00</span></span>        |
    | <span data-ttu-id="5c064-153">Kurss</span><span class="sxs-lookup"><span data-stu-id="5c064-153">Rate</span></span>             | <span data-ttu-id="5c064-154">30,000</span><span class="sxs-lookup"><span data-stu-id="5c064-154">30,000</span></span>      |
    | <span data-ttu-id="5c064-155">Rea üksikasjade vahekaart</span><span class="sxs-lookup"><span data-stu-id="5c064-155">Line details tab</span></span> |             |
    | <span data-ttu-id="5c064-156">Käsitsi</span><span class="sxs-lookup"><span data-stu-id="5c064-156">Manual</span></span>           | <span data-ttu-id="5c064-157">(märgitud)</span><span class="sxs-lookup"><span data-stu-id="5c064-157">(marked)</span></span>    |

    <span data-ttu-id="5c064-158">Rida 2: vahekaart **Tuluväljavõtte rida**</span><span class="sxs-lookup"><span data-stu-id="5c064-158">Line 2: **Earning statement line** tab</span></span>

    | <span data-ttu-id="5c064-159">Väli</span><span class="sxs-lookup"><span data-stu-id="5c064-159">Field</span></span>            | <span data-ttu-id="5c064-160">Väärtus</span><span class="sxs-lookup"><span data-stu-id="5c064-160">Value</span></span>    |
    |------------------|----------|
    | <span data-ttu-id="5c064-161">Tulukood</span><span class="sxs-lookup"><span data-stu-id="5c064-161">Earnings code</span></span>    | <span data-ttu-id="5c064-162">Preemia</span><span class="sxs-lookup"><span data-stu-id="5c064-162">Bonus</span></span>    |
    | <span data-ttu-id="5c064-163">Kogus</span><span class="sxs-lookup"><span data-stu-id="5c064-163">Quantity</span></span>         | <span data-ttu-id="5c064-164">1.0000</span><span class="sxs-lookup"><span data-stu-id="5c064-164">1.0000</span></span>   |
    | <span data-ttu-id="5c064-165">Kurss</span><span class="sxs-lookup"><span data-stu-id="5c064-165">Rate</span></span>             | <span data-ttu-id="5c064-166">4250.00</span><span class="sxs-lookup"><span data-stu-id="5c064-166">4250.00</span></span>  |
    | <span data-ttu-id="5c064-167">Rea üksikasjade vahekaart</span><span class="sxs-lookup"><span data-stu-id="5c064-167">Line details tab</span></span> |          |
    | <span data-ttu-id="5c064-168">Käsitsi</span><span class="sxs-lookup"><span data-stu-id="5c064-168">Manual</span></span>           | <span data-ttu-id="5c064-169">(märgitud)</span><span class="sxs-lookup"><span data-stu-id="5c064-169">(marked)</span></span> |

    <span data-ttu-id="5c064-170">Rida 3: vahekaart **Tuluväljavõtte rida**</span><span class="sxs-lookup"><span data-stu-id="5c064-170">Line 3: **Earning statement line** tab</span></span>

    | <span data-ttu-id="5c064-171">Väli</span><span class="sxs-lookup"><span data-stu-id="5c064-171">Field</span></span>           | <span data-ttu-id="5c064-172">Väärtus</span><span class="sxs-lookup"><span data-stu-id="5c064-172">Value</span></span>      |
    |-----------------|------------|
    | <span data-ttu-id="5c064-173">Tulukood</span><span class="sxs-lookup"><span data-stu-id="5c064-173">Earnings code</span></span>   | <span data-ttu-id="5c064-174">Komisjonitasu</span><span class="sxs-lookup"><span data-stu-id="5c064-174">Commission</span></span> |
    | <span data-ttu-id="5c064-175">Kogus</span><span class="sxs-lookup"><span data-stu-id="5c064-175">Quantity</span></span>        | <span data-ttu-id="5c064-176">1.0000</span><span class="sxs-lookup"><span data-stu-id="5c064-176">1.0000</span></span>     |
    | <span data-ttu-id="5c064-177">Kurss</span><span class="sxs-lookup"><span data-stu-id="5c064-177">Rate</span></span>            | <span data-ttu-id="5c064-178">!,299.00</span><span class="sxs-lookup"><span data-stu-id="5c064-178">!,299.00</span></span>   |
    | <span data-ttu-id="5c064-179">Kurss</span><span class="sxs-lookup"><span data-stu-id="5c064-179">Rate</span></span>            | <span data-ttu-id="5c064-180">1,299.00</span><span class="sxs-lookup"><span data-stu-id="5c064-180">1,299.00</span></span>   |
    | <span data-ttu-id="5c064-181">Rea üksikasjade vahekaart</span><span class="sxs-lookup"><span data-stu-id="5c064-181">Line detail tab</span></span> |            |
    | <span data-ttu-id="5c064-182">Käsitsi</span><span class="sxs-lookup"><span data-stu-id="5c064-182">Manual</span></span>          | <span data-ttu-id="5c064-183">(märgitud)</span><span class="sxs-lookup"><span data-stu-id="5c064-183">(Marked)</span></span>   |

    > [!NOTE]
    > <span data-ttu-id="5c064-184">Iga tuluväljavõtte rea puhul vahekaardil **Rea üksikasjad** liuguri **Käsitsi** lükkamine valikule **Jah** on iga töötaja puhul palga algsaldode sisestamiseks oluline.</span><span class="sxs-lookup"><span data-stu-id="5c064-184">Setting the **Manual** slider to **Yes** in the **Line Details** tab for each earnings statement line is key to have payroll beginning balances entered for each worker.</span></span>

3. <span data-ttu-id="5c064-185">Klõpsake paanil **Tegevus** valikut **Tuluväljavõtte väljastamine** USA-FED-ER-FICA.</span><span class="sxs-lookup"><span data-stu-id="5c064-185">On the **Action** pane, click **Release earnings statement** USA-FED-ER-FICA.</span></span>
4. <span data-ttu-id="5c064-186">Klõpsake paanil **Tegevus** valikut **Palgaväljavõte** lehe **Palgaväljavõtete loomine** avamiseks ja seadistage järgmised valikud.</span><span class="sxs-lookup"><span data-stu-id="5c064-186">On the **Action** pane click **Pay statement** to open the **Generate pay statements** page and set the following:</span></span>

    | <span data-ttu-id="5c064-187">Väli</span><span class="sxs-lookup"><span data-stu-id="5c064-187">Field</span></span>              | <span data-ttu-id="5c064-188">Väärtus</span><span class="sxs-lookup"><span data-stu-id="5c064-188">Value</span></span>     |
    |--------------------|-----------|
    | <span data-ttu-id="5c064-189">Maksekuupäev</span><span class="sxs-lookup"><span data-stu-id="5c064-189">Payment date</span></span>       | <span data-ttu-id="5c064-190">6/30/2017</span><span class="sxs-lookup"><span data-stu-id="5c064-190">6/30/2017</span></span> |
    | <span data-ttu-id="5c064-191">Maksetsükli tüüp</span><span class="sxs-lookup"><span data-stu-id="5c064-191">Payment run type</span></span>   | <span data-ttu-id="5c064-192">Käsitsi</span><span class="sxs-lookup"><span data-stu-id="5c064-192">Manual</span></span>    |
    | <span data-ttu-id="5c064-193">Keela raamatupidamine</span><span class="sxs-lookup"><span data-stu-id="5c064-193">Disable accounting</span></span> |   <span data-ttu-id="5c064-194">Jah</span><span class="sxs-lookup"><span data-stu-id="5c064-194">Yes</span></span>     |

    > [!NOTE] 
    > <span data-ttu-id="5c064-195">See on saadaval ainult siis, kui makse käitamise tüüp on käsitsi ja kui kasutaja soovib maksetsükli arvestuse keelata.</span><span class="sxs-lookup"><span data-stu-id="5c064-195">This is only available when the payment run type is manual and wherein the user want to disable accounting on the pay run.</span></span>

    <span data-ttu-id="5c064-196">Klõpsake nuppu **OK** ja sulgege **teabelogi**.</span><span class="sxs-lookup"><span data-stu-id="5c064-196">Click **OK** and close the **Infolog**.</span></span>

#### <a name="why-the-disable-accounting-slider-needs-to-set-to-yes-when-generating-pay-statements"></a><span data-ttu-id="5c064-197">Miks peab liugur Keela arvestus olema makseväljavõtete loomisel seatud valikule Jah?</span><span class="sxs-lookup"><span data-stu-id="5c064-197">Why the Disable Accounting slider needs to set to Yes when generating pay statements?</span></span>

<span data-ttu-id="5c064-198">Liuguri seadmine valikule **Jah** takistab makseväljavõtte levitamist ja sisestamist pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="5c064-198">Setting the slider to **Yes** prevents lines in the pay statement from being distributed to General ledger.</span></span> <span data-ttu-id="5c064-199">Pearaamatu summasid värskendati varem, kui sisestati kontosaldod pärandsüsteemist.</span><span class="sxs-lookup"><span data-stu-id="5c064-199">General ledger amounts were updating earlier when account balances from the legacy system were entered.</span></span> <span data-ttu-id="5c064-200">Palgaarvestuse algsaldode sisestamine võimaldab luua aruanded, mis sisaldavad teavet varasematest aastatest, samuti tuvastada soodustuste piirangud ja maksuotstarbed.</span><span class="sxs-lookup"><span data-stu-id="5c064-200">Entering beginning balances for Payroll lets you generate reports that include information from prior years, as well as for identifying limits for benefit and tax purposes.</span></span>

### <a name="c-create-pay-statements-for-employees"></a><span data-ttu-id="5c064-201">C.</span><span class="sxs-lookup"><span data-stu-id="5c064-201">C.</span></span> <span data-ttu-id="5c064-202">Töötajatele palgaväljavõtete koostamine</span><span class="sxs-lookup"><span data-stu-id="5c064-202">Create pay statements for employees</span></span>

<span data-ttu-id="5c064-203">Pärast algsaldodega palgaväljavõtete koostamist tuleb kontrollida, et palgaväljavõtted kajastaksid täpselt palgaandmeid.</span><span class="sxs-lookup"><span data-stu-id="5c064-203">After you generate pay statements that have beginning balances, you must verify that the pay statements accurately reflect payroll data.</span></span> <span data-ttu-id="5c064-204">Soodustuste ja maksude teave tuleb samuti käsitsi uuendada, et see vastaks eelmises palgasüsteemis olevatele väärtustele.</span><span class="sxs-lookup"><span data-stu-id="5c064-204">You must also manually update the benefit and taxes information to match the values in the previous payroll system.</span></span> <span data-ttu-id="5c064-205">Pärast kontrollimist, et eelmise palgasüsteemi summad vastavad praeguste palgaväljavõtete summadele, tuleb palgaväljavõtted lõpetada.</span><span class="sxs-lookup"><span data-stu-id="5c064-205">After you verify that the amounts from the previous payroll system match the amounts on the current pay statements, you must finalize the pay statements.</span></span>

1. <span data-ttu-id="5c064-206">Avage leht **Kõik palgaväljavõtted**.</span><span class="sxs-lookup"><span data-stu-id="5c064-206">Open the **All pay statements** page.</span></span>
2. <span data-ttu-id="5c064-207">Tõstke esile viimati Michael Redmondile koostatud palgaväljavõte</span><span class="sxs-lookup"><span data-stu-id="5c064-207">Highlight the last generated pay statement for Michael Redmond</span></span>
3. <span data-ttu-id="5c064-208">Klõpsake nuppu **Redigeeri** lehe **Palgaväljavõte** avamiseks.</span><span class="sxs-lookup"><span data-stu-id="5c064-208">Click **Edit** to open the **Pay statement** page.</span></span>
4. <span data-ttu-id="5c064-209">Avage vahekaart **Soodustuse mahaarvamised** ja sisestage järgmine.</span><span class="sxs-lookup"><span data-stu-id="5c064-209">Open the **Benefit deductions** tab and enter the following:</span></span>

    | <span data-ttu-id="5c064-210">Väli</span><span class="sxs-lookup"><span data-stu-id="5c064-210">Field</span></span>             | <span data-ttu-id="5c064-211">Väärtus</span><span class="sxs-lookup"><span data-stu-id="5c064-211">Value</span></span>            |
    |-------------------|------------------|
    | <span data-ttu-id="5c064-212">Soodustus</span><span class="sxs-lookup"><span data-stu-id="5c064-212">Benefit</span></span>           | <span data-ttu-id="5c064-213">Mahaarvatav summa</span><span class="sxs-lookup"><span data-stu-id="5c064-213">Deduction amount</span></span> |
    | <span data-ttu-id="5c064-214">401K</span><span class="sxs-lookup"><span data-stu-id="5c064-214">401K</span></span>              | <span data-ttu-id="5c064-215">Osalus</span><span class="sxs-lookup"><span data-stu-id="5c064-215">Participate</span></span>      |
    | <span data-ttu-id="5c064-216">Hambaravikindlustus</span><span class="sxs-lookup"><span data-stu-id="5c064-216">Dental</span></span>            | <span data-ttu-id="5c064-217">SubSp</span><span class="sxs-lookup"><span data-stu-id="5c064-217">SubSp</span></span>            |
    | <span data-ttu-id="5c064-218">Osak. kulutused ravikindlustusele</span><span class="sxs-lookup"><span data-stu-id="5c064-218">Dep care spending</span></span> | <span data-ttu-id="5c064-219">Osalus</span><span class="sxs-lookup"><span data-stu-id="5c064-219">Participate</span></span>      |
    | <span data-ttu-id="5c064-220">Visioon</span><span class="sxs-lookup"><span data-stu-id="5c064-220">Vision</span></span>            | <span data-ttu-id="5c064-221">SupSp</span><span class="sxs-lookup"><span data-stu-id="5c064-221">SupSp</span></span>            |

5. <span data-ttu-id="5c064-222">Sisestage vahekaardile **Soodustuse panused** järgmine.</span><span class="sxs-lookup"><span data-stu-id="5c064-222">In the **Benefit contributions** tab and enter the following:</span></span>

    | <span data-ttu-id="5c064-223">Väli</span><span class="sxs-lookup"><span data-stu-id="5c064-223">Field</span></span>   | <span data-ttu-id="5c064-224">Väärtus</span><span class="sxs-lookup"><span data-stu-id="5c064-224">Value</span></span>               |
    |---------|---------------------|
    | <span data-ttu-id="5c064-225">Soodustus</span><span class="sxs-lookup"><span data-stu-id="5c064-225">Benefit</span></span> | <span data-ttu-id="5c064-226">Panuse summa</span><span class="sxs-lookup"><span data-stu-id="5c064-226">Contribution amount</span></span> |
    | <span data-ttu-id="5c064-227">401K</span><span class="sxs-lookup"><span data-stu-id="5c064-227">401K</span></span>    | <span data-ttu-id="5c064-228">Osalus</span><span class="sxs-lookup"><span data-stu-id="5c064-228">Participate</span></span>         |
    | <span data-ttu-id="5c064-229">Hambaravikindlustus</span><span class="sxs-lookup"><span data-stu-id="5c064-229">Dental</span></span>  | <span data-ttu-id="5c064-230">SubSp</span><span class="sxs-lookup"><span data-stu-id="5c064-230">SubSp</span></span>               |
    | <span data-ttu-id="5c064-231">Visioon</span><span class="sxs-lookup"><span data-stu-id="5c064-231">Vision</span></span>  | <span data-ttu-id="5c064-232">SubSp</span><span class="sxs-lookup"><span data-stu-id="5c064-232">SubSp</span></span>               |

6. <span data-ttu-id="5c064-233">Sisestage vahekaardile **Maksude mahaarvamised** järgmine.</span><span class="sxs-lookup"><span data-stu-id="5c064-233">In the **Tax deductions** tab, enter the following:</span></span>

    | <span data-ttu-id="5c064-234">Väli</span><span class="sxs-lookup"><span data-stu-id="5c064-234">Field</span></span>           | <span data-ttu-id="5c064-235">Väärtus</span><span class="sxs-lookup"><span data-stu-id="5c064-235">Value</span></span>            |
    |-----------------|------------------|
    | <span data-ttu-id="5c064-236">Maksukood</span><span class="sxs-lookup"><span data-stu-id="5c064-236">Tax code</span></span>        | <span data-ttu-id="5c064-237">Mahaarvatav summa</span><span class="sxs-lookup"><span data-stu-id="5c064-237">Deduction amount</span></span> |
    | <span data-ttu-id="5c064-238">USA-FED-ER-FICA</span><span class="sxs-lookup"><span data-stu-id="5c064-238">USA-FED-ER-FICA</span></span> | <span data-ttu-id="5c064-239">1600.00</span><span class="sxs-lookup"><span data-stu-id="5c064-239">1600.00</span></span>          |
    | <span data-ttu-id="5c064-240">USA-FED-ER-MEDI</span><span class="sxs-lookup"><span data-stu-id="5c064-240">USA-FED-ER-MEDI</span></span> | <span data-ttu-id="5c064-241">825.75</span><span class="sxs-lookup"><span data-stu-id="5c064-241">825.75</span></span>           |

7. <span data-ttu-id="5c064-242">Sisestage vahekaardile **Maksude panused** järgmine.</span><span class="sxs-lookup"><span data-stu-id="5c064-242">In the **Tax contributions** tab enter the following:</span></span>
8. <span data-ttu-id="5c064-243">Klõpsake valikut **Arvuta**.</span><span class="sxs-lookup"><span data-stu-id="5c064-243">Click **Calculate**.</span></span>

    > [!IMPORTANT] 
    > <span data-ttu-id="5c064-244">Kontrollige töötaja makseväljavõtete kogusummade vastavust pärandsüsteemi jooksva aasta summadele.</span><span class="sxs-lookup"><span data-stu-id="5c064-244">Validate the totals of the pay statement that they match the YTD of the legacy system for the worker.</span></span> <span data-ttu-id="5c064-245">Järgmises etapis võib olla vaja lõpetamisega oodata, et oleks võimalik kõiki palgaväljavõtteid üldiselt kontrollida.</span><span class="sxs-lookup"><span data-stu-id="5c064-245">You may want to hold off on finalizing in the next step to do some overall validating of all pay statements in aggregate.</span></span> <span data-ttu-id="5c064-246">Kui palgaväljavõtted on kontrollitud, vaadake need läbi ja lõpetage need.</span><span class="sxs-lookup"><span data-stu-id="5c064-246">Once validated run through all the pay statements and finalize them.</span></span>

<span data-ttu-id="5c064-247">Sama protsessi saab teha vajaduse korral kvartalite kaupa iga aasta kõigi eelmiste kvartalite kohta.</span><span class="sxs-lookup"><span data-stu-id="5c064-247">The same process can be done in quarter increments if necessary for all prior quarters in each year.</span></span> <span data-ttu-id="5c064-248">See on vajalik ainult juhul, kui kliendil on vaja andmeid kvartalite kaupa näha, pärandsüsteemi naasmata.</span><span class="sxs-lookup"><span data-stu-id="5c064-248">This is only needed if the customer needs to see the data by quarter without going back to the legacy system.</span></span>

## <a name="if-you-make-a-mistake-entering-beginning-balances-for-an-employee"></a><span data-ttu-id="5c064-249">Kui teete töötaja algsaldode sisestamisel vea,</span><span class="sxs-lookup"><span data-stu-id="5c064-249">If you make a mistake Entering Beginning Balances for an Employee</span></span>

<span data-ttu-id="5c064-250">on võimalik kandeid tühistada ja uuesti sisestada.</span><span class="sxs-lookup"><span data-stu-id="5c064-250">It is possible to reverse and reenter transactions.</span></span> <span data-ttu-id="5c064-251">Kande tühistamiseks peate tegema lehel **Kõik palgaväljavõtted** järgmised toimingud.</span><span class="sxs-lookup"><span data-stu-id="5c064-251">To reverse the transaction, all you have to do is to complete the follow steps on the **All pay statements** page.</span></span>

1. <span data-ttu-id="5c064-252">Klõpsake valikut **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="5c064-252">Click **Reverse**.</span></span>
2. <span data-ttu-id="5c064-253">Klõpsake **Jah**, kui kuvatakse teade „Selle palgaväljavõtte tühistamisel luuakse tühistav palgaväljavõte selle palgaväljavõtte tasakaalustamiseks.</span><span class="sxs-lookup"><span data-stu-id="5c064-253">Click **Yes** when the message "When you reverse this pay statement, a reversing pay statement will be created to offset this pay statement.</span></span> <span data-ttu-id="5c064-254">Kumbagi palgaväljavõtet ei saa muuta.</span><span class="sxs-lookup"><span data-stu-id="5c064-254">Neither pay statement can be edited.</span></span> <span data-ttu-id="5c064-255">Kas soovite selle palgaväljavõtte tühistada?”</span><span class="sxs-lookup"><span data-stu-id="5c064-255">Do you want to reverse this pay statement?"</span></span> <span data-ttu-id="5c064-256">.</span><span class="sxs-lookup"><span data-stu-id="5c064-256">displays.</span></span> 

<span data-ttu-id="5c064-257">Kui olete palgaväljavõtte tühistanud, saate luua uue palgaväljavõtte töötaja jaoks varem loodud tuluväljavõtte põhjal.</span><span class="sxs-lookup"><span data-stu-id="5c064-257">After you reverse the pay statement, you can generate a new pay statement for the worker from the earnings statement that you created previously.</span></span> <span data-ttu-id="5c064-258">Korrigeerige kindlasti kõik tuluväljavõtte valed read, enne kui loote uue palgaväljavõtte, ja seejärel looge uued palgaväljavõtted õigete summadega.</span><span class="sxs-lookup"><span data-stu-id="5c064-258">Be sure to fix any incorrect lines on the earnings statement before you generate the new pay statement, and then generate new pay statements with the correct amounts.</span></span> 


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]