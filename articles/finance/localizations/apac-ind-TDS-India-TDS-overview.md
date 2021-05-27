---
title: India maksu mahaarvamise allikast (TDS) ülevaade
description: Selles teemas antakse üksikasjalikku teavet mahaarvatava India maksu (TDS) kohta. TDS-dokumentatsioon hõlmab selle võimaluse funktsioone.
author: kailiang
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 28ee843036e11bd37b97a065ce53d2eb860c79d9
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023191"
---
# <a name="indian-tax-deducted-at-source-tds-overview"></a><span data-ttu-id="dbfa8-104">India maksu mahaarvamise allikast (TDS) ülevaade</span><span class="sxs-lookup"><span data-stu-id="dbfa8-104">Indian Tax Deducted at Source (TDS) overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dbfa8-105">Selles teemas antakse üksikasjalikku teavet mahaarvatava India maksu (TDS) kohta.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-105">This topic provides detailed information about Indian Tax Deducted at Source (TDS).</span></span>

<span data-ttu-id="dbfa8-106">TDS-dokumentatsioon hõlmab selle võimaluse funktsioone.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-106">The TDS documentation covers the functionality of this capability.</span></span> <span data-ttu-id="dbfa8-107">See selgitab ka TDS-i põhiseadistuse sooritamist, TDS-i arvutamist kannetel, TDS-i tasakaalustusprotsessi lõpule viimist, TDS-i serdinumbrite kirjendamist ja TDS-päringute, TDS-lausete ja TDS-i sertide genereerimist.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-107">It also explains how to do the basic setup for TDS, calculate TDS on transactions, complete the TDS settlement process, record TDS certificate numbers, and generate TDS inquiries, TDS statements, and TDS certificates.</span></span> <span data-ttu-id="dbfa8-108">See jaotis hõlmab järgmisi teemasid:</span><span class="sxs-lookup"><span data-stu-id="dbfa8-108">The documentation includes the following topics:</span></span>

- [<span data-ttu-id="dbfa8-109">TDS-i põhihäälestus</span><span class="sxs-lookup"><span data-stu-id="dbfa8-109">Basic setup for TDS</span></span>](apac-ind-TDS-TDS-ledger-accounts-setup.md)
- [<span data-ttu-id="dbfa8-110">TDS-i arvutuse valemikoostaja ja lävelimiit</span><span class="sxs-lookup"><span data-stu-id="dbfa8-110">Formula designer and threshold limit functionality used for TDS calculation</span></span>](apac-ind-TDS-Formula-designer.md)
- [<span data-ttu-id="dbfa8-111">Arvete, maksete, võlatähtede ja kontsernisiseste kannete TDS-i arvutamine</span><span class="sxs-lookup"><span data-stu-id="dbfa8-111">Calculation of TDS on invoices, payments, promissory notes, and intercompany transactions</span></span>](apac-ind-TDS-Calculate-TDS-on-invoices-using-journals.md)
- [<span data-ttu-id="dbfa8-112">TDS-i perioodiline tasakaalustusprotsess ja TDS-i summade tasakaalustus TDS-i asutusele hankijatele</span><span class="sxs-lookup"><span data-stu-id="dbfa8-112">Periodic TDS settlement process and settlement of TDS amounts to TDS authority vendors</span></span>](apac-ind-TDS-Run-the-periodic-TDS-settlement-process.md)
- [<span data-ttu-id="dbfa8-113">TDS-i sertifikaadinumbrite ja kuupäevade kirjendamine ja uuendamine</span><span class="sxs-lookup"><span data-stu-id="dbfa8-113">Recording and updating TDS certificate numbers and dates</span></span>](apac-ind-TDS-Record-TDS-concession-certificate-numbers.md)

## <a name="introduction-to-tds"></a><span data-ttu-id="dbfa8-114">Sissejuhatus TDS-i</span><span class="sxs-lookup"><span data-stu-id="dbfa8-114">Introduction to TDS</span></span>

<span data-ttu-id="dbfa8-115">1961. aasta tulumaksuseaduse alusel on teenuse saaja allikalt maha arvatud tulumaks ettemakse või krediidiarvestuse ajal, olenevalt sellest, kumb toimub esimesena.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-115">Per the Income tax Act, 1961, income tax is deducted at the source by the receiver of the service at the time of advance payment or accounting of credit, whichever occurs first.</span></span> <span data-ttu-id="dbfa8-116">Makse sooritanud isik peab maksusumma maha arvama ja maksma teenuse pakkujale ainult netosaldo.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-116">The person who makes the payment must deduct the tax amount and pay only the net balance to the provider of the service.</span></span> <span data-ttu-id="dbfa8-117">TDS-i rakendatakse valitsuse täpsustatud teenustele ja maks arvatakse maha valitsuse poolt perioodi jaoks määratud määrade alusel.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-117">TDS is applied on services that the government specifies, and the tax is deducted by using the rates that the government specifies for a period.</span></span> <span data-ttu-id="dbfa8-118">Mahaarvamise määr põhineb üksuse olekul, mis võtab makse vastu või pakub teenust.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-118">The rate of deduction is based on the status of the entity that receives the payment or provides the service.</span></span> <span data-ttu-id="dbfa8-119">Olekud hõlmavad **Isikut**, **Hindu jagamata peret** (**HUF**) **Ettevõtet**, **Firmat**, **isikute seost** (**AOP**), **Üksiisikute kehasid** (**BOI**), ja **Kohalikku isikut**.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-119">Statuses include **Individual**, **Hindu Undivided Family** (**HUF**), **Company**, **Firm**, **Association of Persons** (**AOP**), **Body of Individuals** (**BOI**), and **Local authority**.</span></span>

<span data-ttu-id="dbfa8-120">Järgmistes jaotistes loetletakse teenused, mille puhul TDS-i rakendatakse, nagu on määranud India valitsus.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-120">The following sections list the services that TDS is applied on, as specified by the Government of India.</span></span>

<span data-ttu-id="dbfa8-121">**Elanikud**</span><span class="sxs-lookup"><span data-stu-id="dbfa8-121">**Residents**</span></span>

- <span data-ttu-id="dbfa8-122">Tulu palgast (jaotis 192 all)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-122">Income from salaries (Under section 192)</span></span>
- <span data-ttu-id="dbfa8-123">Tulu väärtpaberide intressilt (jaotis 193)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-123">Income from interest on securities (Under section 193)</span></span>
- <span data-ttu-id="dbfa8-124">Tulu dividendidelt (jaotis 194 all)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-124">Income from dividend (Under section 194)</span></span>
- <span data-ttu-id="dbfa8-125">Tulu intressidelt (jaotis 194 all)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-125">Income from interest (Under section 194A)</span></span>
- <span data-ttu-id="dbfa8-126">Tulu loteriidest või mõistatustest (jaotis 194B all)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-126">Income from lotteries or puzzles (Under section 194B)</span></span>
- <span data-ttu-id="dbfa8-127">Võidud võiduajamistelt jne (jaotis 194BB all)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-127">Winning from horse races etc. (Under section 194BB)</span></span>
- <span data-ttu-id="dbfa8-128">Peatöövõtjad ja alamtöövõtjad (jaotis 194C all)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-128">Contractors and sub-contractors (Under section 194C)</span></span>
- <span data-ttu-id="dbfa8-129">Kindlustuse komisjonitasu (jaotis 194D all)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-129">Insurance commission (Under section 194D)</span></span>
- <span data-ttu-id="dbfa8-130">Sissetulek deposiidilt riikliku salvestamisskeemi alusel (jaotis 194EE all)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-130">Income from deposit under national saving scheme (Under section 194EE)</span></span>
- <span data-ttu-id="dbfa8-131">Tulu investeerimisfondist või UTI-st (jaotis 194F all)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-131">Income from mutual fund or UTI (Under section 194F)</span></span>
- <span data-ttu-id="dbfa8-132">Komisjonitasu, vahendustasu, auhind jne, müügil või loteriil (jaotis 194G all)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-132">Commission, Remuneration, Prize etc., on sale or lottery (Under section 194G)</span></span>
- <span data-ttu-id="dbfa8-133">Komisjonitasu või maakleritasu (jaotis 194H all)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-133">Payment of Commission or brokerage (Under section 194H)</span></span>
- <span data-ttu-id="dbfa8-134">Renditasu (jaotis 194I all)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-134">Rent (Under section 194I)</span></span>
- <span data-ttu-id="dbfa8-135">Professionaalne teenus (jaotis 194J all)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-135">Professional service (Under section 194J)</span></span>
- <span data-ttu-id="dbfa8-136">Tulu intressidelt (jaotis 194K all)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-136">Income from Units (Under section 194K)</span></span>
- <span data-ttu-id="dbfa8-137">Teatud kinnisvara omandamisel hüvitise maksmine (jaotis 194LA all)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-137">Payment of compensation on acquisition of certain immovable property (Under section 194LA)</span></span>

<span data-ttu-id="dbfa8-138">**Mitteresidendid**</span><span class="sxs-lookup"><span data-stu-id="dbfa8-138">**Non-residents**</span></span>

- <span data-ttu-id="dbfa8-139">Maksed mitteresidendist sportlastele või spordiliitudele (jaotise 194E all)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-139">Payments to Non-resident sportsmen or sports association (Under section 194E)</span></span>
- <span data-ttu-id="dbfa8-140">Muud summad (jaotise 195 all)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-140">Other sums (Under section 195)</span></span>
- <span data-ttu-id="dbfa8-141">Mitte-residentide ühikute tulu (jaotise 196A all)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-141">Income in respect of units of non-residents (Under section 196A)</span></span>

    - <span data-ttu-id="dbfa8-142">Tulu välisvaluuta obligjonidelt või India ettevõtte aktsiatelt (jaotise 196C all)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-142">Income from foreign currency bonds or shares of Indian Company (Under section 196C)</span></span>
    - <span data-ttu-id="dbfa8-143">Välismaised investeerijad väärtpaberidest (jaotise 196D all)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-143">Incomes of foreign institutional investors from securities (Under section 196D)</span></span>
    - <span data-ttu-id="dbfa8-144">Palk ja kõik muud positiivsed sissetulekud mis tahes sissetulekul (jaotis 192)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-144">Salary and all other positive incomes under any head on income (Section 192)</span></span>
    - <span data-ttu-id="dbfa8-145">Viivis väärtpaberilt (jaotis 193)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-145">Interest on securities (Section 193)</span></span>
    - <span data-ttu-id="dbfa8-146">Viivis, mis pole viivis väärtpaberidelt (jaotis 194A)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-146">Interest other than interest on securities (Section 194A)</span></span>
    - <span data-ttu-id="dbfa8-147">Maksed peatöövõtjatele ja alamtöövõtjatele (jaotis 194C)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-147">Payments to contractors and sub-contractors (Section 194C)</span></span>
    - <span data-ttu-id="dbfa8-148">Võidud loteriidelt või ristsõna mõistatustelt (jaotis 194B)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-148">Winnings from Lottery or crossword puzzles (Section 194B)</span></span>
    - <span data-ttu-id="dbfa8-149">Võidud võiduajamistelt (jaotis 194BB)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-149">Winnings from horse races (Section 194BB)</span></span>
    - <span data-ttu-id="dbfa8-150">Kindlustus komisjonitasu, mis hõlmab kõiki kindlustuse hankimisega seotud makseid (jaotis 194D)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-150">Insurance Commission covering all payments for procuring Insurance business (Section 194D)</span></span>
    - <span data-ttu-id="dbfa8-151">Mitteresidentidele või välisettevõttele makstavad intressid (sektsioon 195)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-151">Any interest other than interest on securities payable to non-residents not being a company or to a foreign company (Section 195)</span></span>
    - <span data-ttu-id="dbfa8-152">Makse mitteresidendist sportlasele, sealhulgas sportlasele, spordiliidule või asutusele.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-152">Payment to non-resident sportsman including athlete or sports association or institution.</span></span> <span data-ttu-id="dbfa8-153">Mitteresidendist spordimehe puhul makstakse välja reklaamide ning artiklite kohta mis tahes Indias mängude/spordialade kohta ajalehtedes, ajakirjades jne.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-153">In case of non-resident sportsman, payments in respect of advertisements as well as articles on any game/sports in India in newspapers, magazines, and so.</span></span> <span data-ttu-id="dbfa8-154">On kaasatud (jaotis 194E)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-154">is included (Section 194E)</span></span>
    - <span data-ttu-id="dbfa8-155">Deposiitide eest makstav maks NSS \[riikliku hoiuste skeemi\] alusel (jaotis 194EE)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-155">Payment in respect of deposits under NSS \[National Savings Scheme\] (Section 194EE)</span></span>
    - <span data-ttu-id="dbfa8-156">Makse ühikute tagasiostuks ühisfondi või UTI alusel (jaotis 194F)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-156">Payment on account of repurchase of Units by Mutual Fund or UTI (Section 194F)</span></span>
    - <span data-ttu-id="dbfa8-157">Komisjonitasu või maakleritasu (jaotis 194H)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-157">Payment for Commission or brokerage (Section 194H)</span></span>
    - <span data-ttu-id="dbfa8-158">Rendimakse (jaotis 194I)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-158">Payment of rent (Section 194I)</span></span>
    - <span data-ttu-id="dbfa8-159">Professionaalsete või tehniliste teenuste tasude maksmine (jaotis 194J)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-159">Payment of fees for professional or technical services (Section 194J)</span></span>
    - <span data-ttu-id="dbfa8-160">Komisjonitasu aktsionäridele, levitajatele, ostjatele ja müüjatele, sh selliste piletite tasu või auhind (jaotis 194G)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-160">Commission to Stockiest, distributors, buyers and sellers of Lottery tickets including remuneration or prize on such tickets (Section 194G)</span></span>
    - <span data-ttu-id="dbfa8-161">Välisvaluutas ostetud ühikute tulu või pikaajaline kapitalikasum, mis tuleneb välisvaluutas ostetud ühikute ülekandmisest (jaotis 196B)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-161">Income from Units purchased in foreign currency or long-term capital gain arising from the transfer of such Units purchased in foreign currency (Section 196B)</span></span>
    - <span data-ttu-id="dbfa8-162">Mis tahes tulu maksmine mitteresidentidele seoses obligeeritud ja aktsiate intresside või dividendidega (sektsioon 196C)</span><span class="sxs-lookup"><span data-stu-id="dbfa8-162">Payment of any income to non-residents in respect of interest or dividend on bonds and shares (Section 196C)</span></span>

<span data-ttu-id="dbfa8-163">TDS arvutatakse ostude, müükide, müügi tagastuste, kreeditarvete, põhivarade soetamise, ettemaksete, käsirahade, võlatähtede, tööde maksu ja kontsernisiseste kannete alusel.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-163">TDS is calculated on purchases, sales, sales returns, credit notes, fixed asset acquisitions, prepayments, advance payments, promissory notes, works tax, and intercompany transactions.</span></span>

> [!NOTE]
> <span data-ttu-id="dbfa8-164">Praeguse India maksustsenaariumis ei arvutata TDS-i müügikannetele.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-164">In the current Indian tax scenario, TDS isn't calculated on sales transactions.</span></span> <span data-ttu-id="dbfa8-165">Süsteem sisaldab sätet müügitehingute, eriti ettevõtete vaheliste tehingute puhul kaetava TDS arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-165">However, the system includes a provision to calculate TDS recoverable on sales transactions, especially for intercompany transactions.</span></span>

<span data-ttu-id="dbfa8-166">TDS-i kalkulatsioon võtab alati arvesse lävendi ja erandi lävendi, mis on määratud TDS-i komponendile.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-166">The calculation of TDS always considers the threshold and the exception threshold that are defined for the TDS component.</span></span>

<span data-ttu-id="dbfa8-167">Peab käitama perioodilise TDS-i tasakaalustusprotsessi ja TDS-i maksed tuleb tasakaalustada TDS-i asutuse hankijatega.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-167">The periodic TDS settlement process must be run, and the TDS payments must be settled to TDS authority vendors.</span></span>

<span data-ttu-id="dbfa8-168">Hankijatelt või klientidelt saadud TDS-tunnistuste serdi numbreid ja kuupäevi saab registreerida ja värskendada.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-168">The certificate numbers and dates for TDS certificates that are received from vendors or customers can be recorded and updated.</span></span> <span data-ttu-id="dbfa8-169">Lisaks saab rakenduses Finance luua Form 26Q ja Form 27Q kvartaliväljavõtteid ja Form 16A tunnistuse TDS-i.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-169">Additionally, Form 26Q and Form 27Q quarterly statements, and the Form 16A certificate for TDS, can be generated in Finance.</span></span>

## <a name="setting-up-and-working-with-tds"></a><span data-ttu-id="dbfa8-170">TDS-i seadistamine ja sellega töötamine</span><span class="sxs-lookup"><span data-stu-id="dbfa8-170">Setting up and working with TDS</span></span>

<span data-ttu-id="dbfa8-171">Siin on ülevaade TDS-i seadistamise ja sellega töötamise protsessist:</span><span class="sxs-lookup"><span data-stu-id="dbfa8-171">Here is an overview of the process for setting up and working with TDS:</span></span>

1. <span data-ttu-id="dbfa8-172">**TDS-i seadistus:**</span><span class="sxs-lookup"><span data-stu-id="dbfa8-172">**TDS setup:**</span></span>

    - <span data-ttu-id="dbfa8-173">Parameetrite seadistamine:</span><span class="sxs-lookup"><span data-stu-id="dbfa8-173">Parameter setup:</span></span>

        - <span data-ttu-id="dbfa8-174">Aktiveerige pearaamatu parameetrites TDS-iga seotud parameetrid.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-174">In General ledger parameters, activate parameters that are related to TDS.</span></span>
        - <span data-ttu-id="dbfa8-175">Pearaamatu parameetrites seadistage kinnipeetava maksu maksete numbriseeria.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-175">In General ledger parameters, set up the number sequence for withholding tax payments.</span></span>
        - <span data-ttu-id="dbfa8-176">TDS-i parameetrite määramine jaotises ostukontod ja müügikontod.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-176">Set up parameters in Accounts payable and Accounts receivable.</span></span>

    - <span data-ttu-id="dbfa8-177">Põhihäälestus:</span><span class="sxs-lookup"><span data-stu-id="dbfa8-177">Basic setup:</span></span>

        - <span data-ttu-id="dbfa8-178">Seadistage TDS-i registreerimisnumbrid ettevõttele, klientidele ja hankijatele.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-178">Set up TDS registration numbers for a company, customers, and vendors.</span></span>
        - <span data-ttu-id="dbfa8-179">Kordustellimuste gruppide häälestus.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-179">Set up TDS component groups.</span></span>
        - <span data-ttu-id="dbfa8-180">Seadistage TDS-i komponendid, lisage neile TDS-i komponendigrupid ning määratlege nende jaoks lävi ja erandi lävi.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-180">Set up TDS components, attach TDS component groups to them, and define the threshold and exception threshold for them.</span></span>
        - <span data-ttu-id="dbfa8-181">Seadistage TDS-i asutused.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-181">Set up TDS authorities.</span></span>
        - <span data-ttu-id="dbfa8-182">Käibemaksu tasakaalustusperioodide häälestamine.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-182">Set up TDS settlement periods.</span></span>
        - <span data-ttu-id="dbfa8-183">Seadistage TDS-i maksukoodid ja s seostage nendega TDS-i komponendid.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-183">Set up TDS tax codes, and attach TDS components to them.</span></span>
        - <span data-ttu-id="dbfa8-184">Seadistage TDS-i maksukoodid ja s seostage nendega TDS-i komponendid.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-184">Set up TDS tax groups, and attach TDS tax codes to them.</span></span>
        - <span data-ttu-id="dbfa8-185">TDS-grupi TDS-i arvutamiseks määratlege valemikoosturis.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-185">In the formula designer, define a formula to calculate TDS for a TDS group.</span></span>
        - <span data-ttu-id="dbfa8-186">TDS-i kontsessioonisertifikaatide numbrid.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-186">Record TDS concession certificate numbers.</span></span>

    - <span data-ttu-id="dbfa8-187">Pearaamatukontod ja ettevõtteseadistus:</span><span class="sxs-lookup"><span data-stu-id="dbfa8-187">Ledger accounts and company setup:</span></span>

        - <span data-ttu-id="dbfa8-188">Seadistage TDS-i maksmis- ja saadaoleva pearaamatu kontod.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-188">Set up TDS payable and receivable ledger accounts.</span></span>
        - <span data-ttu-id="dbfa8-189">Seadistage ettevõttele maksu mahaarvamise ja kogumise konto number (TAN) ja mahaarvaja tüübi kategooria.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-189">Set up a Tax Deduction and Collection Account Number (TAN) and a deductor type category for the company.</span></span>

    - <span data-ttu-id="dbfa8-190">Muu seadistus:</span><span class="sxs-lookup"><span data-stu-id="dbfa8-190">Other setup:</span></span>

        - <span data-ttu-id="dbfa8-191">Seadistage maksegraafik, mis sisaldab TDS-i eraldamist.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-191">Set up a payment schedule that includes TDS allocation.</span></span>
        - <span data-ttu-id="dbfa8-192">Seadistage TDS-asutusele tehtavate maksete jaoks maksetasu tüüp.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-192">Set up a payment fee type for payments to the TDS authority.</span></span>
        - <span data-ttu-id="dbfa8-193">Saate seadistada teabe hankijate ja klientide TDS-gruppide, püsikontonumbrite ja TAN-ide kohta.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-193">Set up information about TDS groups, permanent account numbers (PANs), and TANs for vendors and customers.</span></span>

2. <span data-ttu-id="dbfa8-194">**TDS kalkulatsioonitehingud:**</span><span class="sxs-lookup"><span data-stu-id="dbfa8-194">**Calculation of TDS in transactions:**</span></span>

    - <span data-ttu-id="dbfa8-195">Arved ja maksed</span><span class="sxs-lookup"><span data-stu-id="dbfa8-195">Invoices and payments</span></span>
    - <span data-ttu-id="dbfa8-196">Võlatähed</span><span class="sxs-lookup"><span data-stu-id="dbfa8-196">Promissory notes</span></span>
    - <span data-ttu-id="dbfa8-197">Ettemaksed</span><span class="sxs-lookup"><span data-stu-id="dbfa8-197">Advance payments</span></span>
    - <span data-ttu-id="dbfa8-198">Ettemaksed</span><span class="sxs-lookup"><span data-stu-id="dbfa8-198">Prepayments</span></span>

3. <span data-ttu-id="dbfa8-199">**TDS tasumine:**</span><span class="sxs-lookup"><span data-stu-id="dbfa8-199">**TDS settlement:**</span></span>

    - <span data-ttu-id="dbfa8-200">Perioodilise TDS-i tasumise käitamine</span><span class="sxs-lookup"><span data-stu-id="dbfa8-200">Periodic TDS settlement process</span></span>
    - <span data-ttu-id="dbfa8-201">TDS-i maksete tasumine TDS-i halduri hankijatele ja TDS-i dokumendi loomine</span><span class="sxs-lookup"><span data-stu-id="dbfa8-201">Settlement of TDS payments to TDS authority vendors and generation of TDS challan</span></span>

4. <span data-ttu-id="dbfa8-202">**TDS-i päringud, väljavõtted ja sertifikaadid:**</span><span class="sxs-lookup"><span data-stu-id="dbfa8-202">**TDS inquiries, statements, and certificate:**</span></span>

    - <span data-ttu-id="dbfa8-203">TDS-i sertifikaadinumbrite ja kuupäevade kirjendamine ja uuendamine.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-203">Record and update TDS certificate numbers and dates.</span></span>
    - <span data-ttu-id="dbfa8-204">Looge TDS-i päring ja sisestatud TDS-i päring.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-204">Generate a TDS inquiry and a posted TDS inquiry.</span></span>
    - <span data-ttu-id="dbfa8-205">Looge Form 27A, Form 26Q ja Form 27Q TDS-i ja e-TDS-i kvartaliaruanded.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-205">Generate Form 27A, Form 26Q, and Form 27Q TDS and e-TDS quarterly statements.</span></span>
    - <span data-ttu-id="dbfa8-206">Form 16A serdi loomine.</span><span class="sxs-lookup"><span data-stu-id="dbfa8-206">Generate a Form 16A TDS certificate.</span></span>
