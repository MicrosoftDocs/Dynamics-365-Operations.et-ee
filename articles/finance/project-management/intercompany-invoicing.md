---
title: Kontsernisisene arveldamine
description: Selles artiklis on teave ja näited projektide kontsernisisese arveldamise kohta.
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerInterCompany
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 94153
ms.assetid: 33e98da7-01c1-4369-923d-aa1c8326cb80
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d0385c796ca1ac02d6b8f66c04dad21bafe15ef8
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2174826"
---
# <a name="intercompany-invoicing"></a><span data-ttu-id="84b62-103">Kontsernisisene arveldamine</span><span class="sxs-lookup"><span data-stu-id="84b62-103">Intercompany invoicing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="84b62-104">Selles artiklis on teave ja näited projektide kontsernisisese arveldamise kohta.</span><span class="sxs-lookup"><span data-stu-id="84b62-104">This article provides information and examples about intercompany invoicing for projects.</span></span>

<span data-ttu-id="84b62-105">Teie organisatsioonil võib olla mitu allüksust, tütarettevõtet ja muud juriidilist isikut, mis edastavad üksteisele projektide tarbeks tooteid ja teenuseid.</span><span class="sxs-lookup"><span data-stu-id="84b62-105">Your organization might have multiple divisions, subsidiaries, and other legal entities that transfer products and services to each other for projects.</span></span> <span data-ttu-id="84b62-106">Juriidilist isikut, kes teenust või toodet pakub *, nimetatakse laenu väljastavaks juriidiliseks isikuks* ja teenust või toodet vastuvõtvat juriidilist isikut *laenavaks juriidiliseks isikuks*.</span><span class="sxs-lookup"><span data-stu-id="84b62-106">The legal entity that provides the service or product is called the *lending legal entity*, and the legal entity that receives the service or product is called the *borrowing legal entity*.</span></span> 

<span data-ttu-id="84b62-107">Järgmisel joonisel on kujutatud tüüpilist stsenaariumi, kus kaks juriidilist isikut SI FR (laenav juriidiline isik) ja SI USA (laenu väljastav juriidiline isik) jagavad ressursse projekti läbiviimiseks kliendile A. Selle stsenaariumi puhul on peatöövõtja SI FR, kes peab töö kliendile A üle andma.</span><span class="sxs-lookup"><span data-stu-id="84b62-107">The following illustration shows a typical scenario where two legal entities, SI FR (the borrowing legal entity) and SI USA (the lending legal entity) share resources to deliver a project for customer A. For this scenario, SI FR is contracted to deliver the work to customer A.</span></span> 

<span data-ttu-id="84b62-108">[![Kontsernisisese arveldamise näide](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg)</span><span class="sxs-lookup"><span data-stu-id="84b62-108">[![Intercompany invoicing example](./media/interco.invoicing-01.jpg)](./media/interco.invoicing-01.jpg)</span></span> 

<span data-ttu-id="84b62-109">Eesmärk on muuta kulude juhtimine, tulude kajastamine, maksud ja sisehind kontsernisiseste projektikannete puhul paindlikumaks ja võimsamaks.</span><span class="sxs-lookup"><span data-stu-id="84b62-109">The goal is to make cost control, revenue recognition, taxes, and transfer price for intercompany project transactions more flexible and powerful.</span></span> <span data-ttu-id="84b62-110">Lisaks pakutakse järgmisi võimalusi.</span><span class="sxs-lookup"><span data-stu-id="84b62-110">In addition, the following capabilities are provided:</span></span>

-   <span data-ttu-id="84b62-111">Kliendiarvete koostamine projekti suhtes laenavas juriidilises isikus, kasutades kontsernisiseseid ajatabelid, kulusid ja hankija arveid laenu väljastavas juriidilises isikus.</span><span class="sxs-lookup"><span data-stu-id="84b62-111">Create customer invoices against a project in a borrowing legal entity by using intercompany timesheets, expenses, and vendor invoices in a lending legal entity.</span></span>
-   <span data-ttu-id="84b62-112">Maksuarvutuste ja kaudsete kulude toetus.</span><span class="sxs-lookup"><span data-stu-id="84b62-112">Support tax calculations and indirect costs.</span></span>
-   <span data-ttu-id="84b62-113">Tulu näitamise edasilükkamine laenu väljastavas juriidilises isikus ja laenava juriidilise isiku poolsel tulu näitamisel.</span><span class="sxs-lookup"><span data-stu-id="84b62-113">Defer revenue recognition in a lending legal entity and when a borrowing legal entity should recognize the cost.</span></span>
-   <span data-ttu-id="84b62-114">Lõpetamata toodangu (WIP) tulu kogumine laenu väljastavasse juriidilisse isikusse.</span><span class="sxs-lookup"><span data-stu-id="84b62-114">Accrue work in process (WIP) revenue in the lending legal entity.</span></span>
-   <span data-ttu-id="84b62-115">Üleviimishindade määramine mitmesuguste hinnamudelite põhjal.</span><span class="sxs-lookup"><span data-stu-id="84b62-115">Set transfer prices that can be based on various pricing models.</span></span> <span data-ttu-id="84b62-116">Järgmisena on toodud mõned näited.</span><span class="sxs-lookup"><span data-stu-id="84b62-116">Here are some examples:</span></span>
    -   <span data-ttu-id="84b62-117">**Kogus** – summa, mis sisestatakse väljale **Hinnakujundus**, on tegelik kulu koguse või ühiku kohta.</span><span class="sxs-lookup"><span data-stu-id="84b62-117">**Quantity** – The amount that you enter in the **Pricing** field is the actual cost per quantity or unit.</span></span>
    -   <span data-ttu-id="84b62-118">**Kulude summa** – hind/kulu kande kohta pluss kulusumma, mille sisestate väljale **Hinnakujundus**.</span><span class="sxs-lookup"><span data-stu-id="84b62-118">**Charges amount** – The price/cost per transaction plus the charges amount that you enter in the **Pricing** field.</span></span>
    -   <span data-ttu-id="84b62-119">**Kulude protsent** – üleviimishind on hind/kulu kande kohta, mis on korrutatud väljale **Hinnakujundus** sisestatud tasuprotsendiga.</span><span class="sxs-lookup"><span data-stu-id="84b62-119">**Charges percentage** – The transfer price is the price/cost per transaction multiplied by the charges percentage that you enter in the **Pricing** field.</span></span>
    -   <span data-ttu-id="84b62-120">**Müügihinna protsent** – protsent müügihinnast, mis edastatakse laenu väljastavale juriidilisele isikule.</span><span class="sxs-lookup"><span data-stu-id="84b62-120">**Percentage of sales price** – The percentage of the sales price that is transferred to the lending legal entity.</span></span>
    -   <span data-ttu-id="84b62-121">**Summa alla müügihinna** – summa, mille laenav juriidiline isik peab müügihindadest kinni enne ülekannet laenu väljastavale juriidilisele isikule.</span><span class="sxs-lookup"><span data-stu-id="84b62-121">**Amount below sales price** – The amount that the borrowing legal entity holds back from the sales prices before transfer to the lending legal entity.</span></span>
    -   <span data-ttu-id="84b62-122">**Kasumimäär** – arv, mille sisestate väljale **Hinnakujundus**, on kasumimäär, mis on väljendatud protsendina müügihinnast.</span><span class="sxs-lookup"><span data-stu-id="84b62-122">**Contribution ratio** – The number that you enter in the **Pricing** field is the contribution ratio, which is expressed as a percentage of the sales price.</span></span>

## <a name="example-1-set-up-parameters-for-intercompany-invoicing"></a><span data-ttu-id="84b62-123">1. näide: kontsernisisese arveldamise parameetrite seadistamine</span><span class="sxs-lookup"><span data-stu-id="84b62-123">Example 1: Set up parameters for intercompany invoicing</span></span>
<span data-ttu-id="84b62-124">Selles näites on USSI laenu väljastav juriidiline isik ja tema ressursid registreerivad aega laenava juriidilise isiku FRSI suhtes, kellel on sõlmitud leping lõppkliendiga.</span><span class="sxs-lookup"><span data-stu-id="84b62-124">In this example, USSI is a lending legal entity, and its resources are reporting time against the borrowing legal entity, FRSI, which owns the contract with the end customer.</span></span> <span data-ttu-id="84b62-125">USSI töötajate registreeritavad tunnid ja kulud saab lisada FRSI koostatavale projektiarvele.</span><span class="sxs-lookup"><span data-stu-id="84b62-125">Hours and expenses that USSI employees report can be included in the project invoice that FRSI generates.</span></span> <span data-ttu-id="84b62-126">Lisaks on olemas kolmas kannete allikas, mis võib pärineda laenavast juriidilisest isikust (selles näites USSI), kui see osutab allüksustele (nt FRSI) jagatud hankijate teenuseid ja edastab need kulud siis projektidele nendes allüksustes.</span><span class="sxs-lookup"><span data-stu-id="84b62-126">In addition, there is a third source of transactions that can originate from the lending legal entity (USSI in this example) when it provides shared vendors services to subsidiaries (such as FRSI) and then passes on those costs to projects within those subsidiaries.</span></span> <span data-ttu-id="84b62-127">Kõik vastavad arvedokumendid ja maksuarvutused teeb Finance.</span><span class="sxs-lookup"><span data-stu-id="84b62-127">All matching invoice documents and tax calculations are completed by Finance.</span></span> 

<span data-ttu-id="84b62-128">Selles näites peab FRSI olema USSI juriidilises isikus klient ja USSI peab olema FRSI juriidilises isikus hankija.</span><span class="sxs-lookup"><span data-stu-id="84b62-128">For this example, FRSI must be a customer in the USSI legal entity, and USSI must be a vendor in the FRSI legal entity.</span></span> <span data-ttu-id="84b62-129">Seejärel saate seadistada kahe juriidilise isiku vahelise kontsernisisese seose.</span><span class="sxs-lookup"><span data-stu-id="84b62-129">You can then set up an intercompany relationship between the two legal entities.</span></span> <span data-ttu-id="84b62-130">Järgmine protseduur näitab, kuidas seadistada parameetreid, nii et mõlemad juriidilised isikud saaksid kontsernisiseses arvelduses osaleda.</span><span class="sxs-lookup"><span data-stu-id="84b62-130">The following procedure shows how to set up the parameters so that both legal entities can participate in intercompany invoicing.</span></span>

1. <span data-ttu-id="84b62-131">Seadistage FRSI kliendina USSI juriidilises isikus ja USSI hankijana FRSI juriidilises isikus.</span><span class="sxs-lookup"><span data-stu-id="84b62-131">Set up FRSI as a customer in the USSI legal entity, and set up USSI as a vendor in the FRSI legal entity.</span></span> <span data-ttu-id="84b62-132">Selle ülesande jaoks vajalike toimingute puhul on kolm sisestuspunkti.</span><span class="sxs-lookup"><span data-stu-id="84b62-132">There are three entry points for the steps that are required for this task.</span></span>

   | <span data-ttu-id="84b62-133">Etapp</span><span class="sxs-lookup"><span data-stu-id="84b62-133">Step</span></span> |                                                       <span data-ttu-id="84b62-134">Sisestuspunkt</span><span class="sxs-lookup"><span data-stu-id="84b62-134">Entry point</span></span>                                                        |                                                                                                                                                                                               <span data-ttu-id="84b62-135">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="84b62-135">Description</span></span>                                                                                                                                                                                               |
   |------|--------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
   |  <span data-ttu-id="84b62-136">A</span><span class="sxs-lookup"><span data-stu-id="84b62-136">A</span></span>   | <span data-ttu-id="84b62-137">Klõpsake USSI all valikuid <strong>Müügireskontro</strong> &gt; <strong>Kliendid</strong> &gt; <strong>Kõik kliendid</strong>.</span><span class="sxs-lookup"><span data-stu-id="84b62-137">In USSI, click <strong>Accounts receivable</strong> &gt; <strong>Customers</strong> &gt; <strong>All customers</strong>.</span></span> |                                                                                                                                                                  <span data-ttu-id="84b62-138">Looge FRSI-le uus kliendikirje ja valige kliendigrupp.</span><span class="sxs-lookup"><span data-stu-id="84b62-138">Create a new customer record for FRSI, and select the customer group.</span></span>                                                                                                                                                                  |
   |  <span data-ttu-id="84b62-139">B</span><span class="sxs-lookup"><span data-stu-id="84b62-139">B</span></span>   |    <span data-ttu-id="84b62-140">Klõpsake FRSI all valikuid <strong>Ostureskontro</strong> &gt; <strong>Hankijad</strong> &gt; <strong>Kõik hankijad</strong>.</span><span class="sxs-lookup"><span data-stu-id="84b62-140">In FRSI, click <strong>Accounts payable</strong> &gt; <strong>Vendors</strong> &gt; <strong>All vendors</strong>.</span></span>     |                                                                                                                                                                    <span data-ttu-id="84b62-141">Looge USSI-le uus hankija kirje ja valige hankijagrupp.</span><span class="sxs-lookup"><span data-stu-id="84b62-141">Create a new vendor record for USSI, and select the vendor group.</span></span>                                                                                                                                                                    |
   |  <span data-ttu-id="84b62-142">C</span><span class="sxs-lookup"><span data-stu-id="84b62-142">C</span></span>   |                                  <span data-ttu-id="84b62-143">Avage FRSI all äsja loodud hankija kirje.</span><span class="sxs-lookup"><span data-stu-id="84b62-143">In FRSI, open the vendor record that you just created.</span></span>                                  | <span data-ttu-id="84b62-144">Klõpsake tegumiriba vahekaardil <strong>Üldine</strong> grupis <strong>Seadistus</strong> valikut <strong>Kontsernisisene</strong>.</span><span class="sxs-lookup"><span data-stu-id="84b62-144">On the Action Pane, on the <strong>General</strong> tab, in the <strong>Set up</strong> group, click <strong>Intercompany</strong>.</span></span> <span data-ttu-id="84b62-145">Määrake lehe <strong>Kontsernisisene</strong> vahekaardil <strong>Kaubandussuhe</strong> liuguri <strong>Aktiivne</strong> väärtuseks <strong>Jah</strong>.</span><span class="sxs-lookup"><span data-stu-id="84b62-145">On the <strong>Intercompany</strong> page, on the <strong>Trading relationship</strong> tab, set the <strong>Active</strong> slider to <strong>Yes</strong>.</span></span> <span data-ttu-id="84b62-146">Valige väljalt <strong>Kliendi ettevõte</strong> kliendi kirje, mille lõite etapis A.</span><span class="sxs-lookup"><span data-stu-id="84b62-146">In the <strong>Customer company</strong> field, select the customer record that you created in step A.</span></span> |


2. <span data-ttu-id="84b62-147">Klõpsake valikuid **Projektihaldus ja raamatupidamine** &gt; **Seadistus** &gt; **Projektihalduse ja raamatupidamise parameetrid** ja seejärel vahekaarti **Kontsernisisene**. See, kuidas parameetrid seadistate, sõltub sellest, kas olete laenav või laenu väljastav juriidiline isik.</span><span class="sxs-lookup"><span data-stu-id="84b62-147">Click **Project management and accounting** &gt; **Setup** &gt; **Project management accounting parameters**, and then click the **Intercompany** tab. The way that you set up the parameters depends on whether you're the borrowing legal entity or the lending legal entity.</span></span>
   -   <span data-ttu-id="84b62-148">Kui olete laenav juriidiline isik, siis valige hankekategooria, mida tuleks kasutada automaatselt loodavate hankija arvete vastendamisel.</span><span class="sxs-lookup"><span data-stu-id="84b62-148">If you're the borrowing legal entity, select the procurement category that should be used to match the vendor invoices, which are automatically generated.</span></span>
   -   <span data-ttu-id="84b62-149">Kui olete laenu väljastav juriidiline isik, siis valige iga laenava üksuse puhul igale kandele projekti vaikekategooria.</span><span class="sxs-lookup"><span data-stu-id="84b62-149">If you're the lending legal entity, for each borrowing entity, select a default project category for each transaction type.</span></span> <span data-ttu-id="84b62-150">Projektikategooriaid kasutatakse maksude konfigureerimiseks, kui kontsernisiseste kannete arveldatud kategooria on olemas ainult laenavas juriidilises isikus.</span><span class="sxs-lookup"><span data-stu-id="84b62-150">Project categories are used for tax configuration when the invoiced category in intercompany transactions exists only in the borrowing legal entity.</span></span> <span data-ttu-id="84b62-151">Saate valida kontsernisiseste kannete puhul kulude juurdekasvu.</span><span class="sxs-lookup"><span data-stu-id="84b62-151">You can choose to accrue revenue for intercompany transactions.</span></span> <span data-ttu-id="84b62-152">See juurdekasv tekib kannete sisestamisel ja see tühistatakse kontsernisisese arve sisestamisel.</span><span class="sxs-lookup"><span data-stu-id="84b62-152">This accrual is done when the transactions are posted, and it's then reversed when the intercompany invoice is posted.</span></span>

3. <span data-ttu-id="84b62-153">Klõpsake valikuid **Projektihaldus ja raamatupidamine** &gt; **Seadistus** &gt; **Hinnad** &gt; **Ülekande hind**.</span><span class="sxs-lookup"><span data-stu-id="84b62-153">Click **Project management and accounting** &gt; **Setup** &gt; **Prices** &gt; **Transfer price**.</span></span>
4. <span data-ttu-id="84b62-154">Valige valuuta, kande tüüp ja ülekande hinnamudel.</span><span class="sxs-lookup"><span data-stu-id="84b62-154">Select a currency, transaction type, and transfer price model.</span></span> <span data-ttu-id="84b62-155">Arvel kasutatav valuuta on valuuta, mis on konfigureeritud laenu väljastava juriidilise isiku all laenava juriidilise isiku kliendikirjes.</span><span class="sxs-lookup"><span data-stu-id="84b62-155">The currency that is used on the invoice is the currency that is configured in the customer record for the borrowing legal entity in the lending legal entity.</span></span> <span data-ttu-id="84b62-156">Valuutat kasutatakse üleviimise hinnatabeli kirjete vastendamiseks.</span><span class="sxs-lookup"><span data-stu-id="84b62-156">The currency is used to match entries in the transfer price table.</span></span>
5. <span data-ttu-id="84b62-157">Klõpsake valikuid **Pearaamat** &gt; **Sisestamise seadistus** &gt; **Kontsernisisene raamatupidamine** ja seadistage USSI ja FRSI seos.</span><span class="sxs-lookup"><span data-stu-id="84b62-157">Click **General ledger** &gt; **Posting setup** &gt; **Intercompany accounting**, and set up a relationship for USSI and FRSI.</span></span>

## <a name="example-2-create-and-post-an-intercompany-timesheet"></a><span data-ttu-id="84b62-158">2. näide: kontsernisisese ajatabeli loomine ja sisestamine</span><span class="sxs-lookup"><span data-stu-id="84b62-158">Example 2: Create and post an intercompany timesheet</span></span>
<span data-ttu-id="84b62-159">USSI, laenu väljastav juriidiline isik, peab looma ja sisestama ajatabeli FRSI (laenava juriidilise isiku) projektile.</span><span class="sxs-lookup"><span data-stu-id="84b62-159">USSI, the lending legal entity, must create and post the timesheet for a project from FRSI, the borrowing legal entity.</span></span> <span data-ttu-id="84b62-160">Selle ülesande jaoks vajalike toimingute puhul on kaks sisestuspunkti.</span><span class="sxs-lookup"><span data-stu-id="84b62-160">There are two entry points for the steps that are required for this task.</span></span>

| <span data-ttu-id="84b62-161">Etapp</span><span class="sxs-lookup"><span data-stu-id="84b62-161">Step</span></span> | <span data-ttu-id="84b62-162">Sisestuspunkt</span><span class="sxs-lookup"><span data-stu-id="84b62-162">Entry point</span></span>                                                                       | <span data-ttu-id="84b62-163">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="84b62-163">Description</span></span>                                                                                                                                                                                       |
|------|-----------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84b62-164">A</span><span class="sxs-lookup"><span data-stu-id="84b62-164">A</span></span>    | <span data-ttu-id="84b62-165">**Projektihaldus ja raamatupidamine** &gt; **Ajatabelid** &gt; **Kõik ajatabelid**</span><span class="sxs-lookup"><span data-stu-id="84b62-165">**Project management and accounting** &gt; **Timesheets** &gt; **All timesheets**</span></span> | <span data-ttu-id="84b62-166">Looge uus ajatabel.</span><span class="sxs-lookup"><span data-stu-id="84b62-166">Create a new timesheet.</span></span> <span data-ttu-id="84b62-167">Tehke ajatabeli rea väljal **Juriidiline isik** valik **FRSI**.</span><span class="sxs-lookup"><span data-stu-id="84b62-167">On the timesheet line, in the **Legal entity** field, select **FRSI**.</span></span> <span data-ttu-id="84b62-168">Valige väljal **Projekti ID** FRSI alt projekt.</span><span class="sxs-lookup"><span data-stu-id="84b62-168">In the **Project ID** field, select the project in FRSI.</span></span> <span data-ttu-id="84b62-169">Sisestage iga nädalapäeva tundide arv.</span><span class="sxs-lookup"><span data-stu-id="84b62-169">Enter the hours for each day of the week.</span></span> |
| <span data-ttu-id="84b62-170">B</span><span class="sxs-lookup"><span data-stu-id="84b62-170">B</span></span>    | <span data-ttu-id="84b62-171">Leht **Ajatabel**</span><span class="sxs-lookup"><span data-stu-id="84b62-171">**Timesheet** page</span></span>                                                                | <span data-ttu-id="84b62-172">Pärast töövoo aktiveerimist postitage ajatabel ja märkige üles kandenumber.</span><span class="sxs-lookup"><span data-stu-id="84b62-172">After the workflow runs, post the timesheet, and make a note of the voucher number.</span></span>                                                                                                               |

## <a name="example-3-create-and-post-an-intercompany-vendor-invoice"></a><span data-ttu-id="84b62-173">3. näide: kontsernisisese hankija arve loomine ja sisestamine</span><span class="sxs-lookup"><span data-stu-id="84b62-173">Example 3: Create and post an intercompany vendor invoice</span></span>
<span data-ttu-id="84b62-174">USSI, laenu väljastav juriidiline isik, peab looma ja sisestama kontsernisisese hankija arve FRSI (laenava juriidilise isiku) projektile.</span><span class="sxs-lookup"><span data-stu-id="84b62-174">USSI, the lending legal entity, must create and post the intercompany vendor invoice for a project from FRSI, the borrowing legal entity.</span></span> <span data-ttu-id="84b62-175">See hankija arve kajastab sisse ostetud tööjõudu ja kulu, mis kaasnes USSI palgatud hankijate tööga.</span><span class="sxs-lookup"><span data-stu-id="84b62-175">This vendor invoice represents the outsourced labor and expense that were performed by vendors that are paid by USSI.</span></span> <span data-ttu-id="84b62-176">Selle ülesande jaoks vajalike toimingute puhul on kaks sisestuspunkti.</span><span class="sxs-lookup"><span data-stu-id="84b62-176">There are two entry points for the steps that are required for this task.</span></span>

| <span data-ttu-id="84b62-177">Etapp</span><span class="sxs-lookup"><span data-stu-id="84b62-177">Step</span></span> | <span data-ttu-id="84b62-178">Sisestuspunkt</span><span class="sxs-lookup"><span data-stu-id="84b62-178">Entry point</span></span>                                                                                      | <span data-ttu-id="84b62-179">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="84b62-179">Description</span></span>                                                                                                                                                                                                                                                                          |
|------|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84b62-180">A</span><span class="sxs-lookup"><span data-stu-id="84b62-180">A</span></span>    | <span data-ttu-id="84b62-181">**Ostureskontro** &gt; **Arved** &gt; **Ava hankija arved** &gt; **Uus hankija arve**</span><span class="sxs-lookup"><span data-stu-id="84b62-181">**Accounts payable** &gt; **Invoices** &gt; **Open vendor invoices** &gt; **New vendor invoice**</span></span> | <span data-ttu-id="84b62-182">Looge uus hankija arve ja sisestage teenused, mis FRSI projekti nimel hangiti.</span><span class="sxs-lookup"><span data-stu-id="84b62-182">Create a new vendor invoice, and enter the services that were procured on behalf of FRSI's project.</span></span>                                                                                                                                                                                  |
| <span data-ttu-id="84b62-183">B</span><span class="sxs-lookup"><span data-stu-id="84b62-183">B</span></span>    | <span data-ttu-id="84b62-184">Leht **Hankija arve**</span><span class="sxs-lookup"><span data-stu-id="84b62-184">The **Vendor invoice** page</span></span>                                                                      | <span data-ttu-id="84b62-185">Sisestage read, mis kajastavad FRSI nimel sisse ostetud teenuseid.</span><span class="sxs-lookup"><span data-stu-id="84b62-185">Enter lines that represent the outsourced services on behalf of FRSI.</span></span> <span data-ttu-id="84b62-186">Sisestage kiirkaardil **Rea üksikasjad** vahekaardil **Projekt** arve reale väljal **Projekti ettevõte** väärtus **FRSI**.</span><span class="sxs-lookup"><span data-stu-id="84b62-186">On the **Line details** FastTab, on the **Project** tab for the invoice line, in the **Project company** field, enter **FRSI**.</span></span> <span data-ttu-id="84b62-187">Sisestage projekt ja vastav teave.</span><span class="sxs-lookup"><span data-stu-id="84b62-187">Enter the project and corresponding information.</span></span> <span data-ttu-id="84b62-188">Seejärel sisestage hankija arve.</span><span class="sxs-lookup"><span data-stu-id="84b62-188">Then post the vendor invoice.</span></span> |

## <a name="example-4-create-and-post-the-intercompany-invoice"></a><span data-ttu-id="84b62-189">4. näide: kontsernisisese arve loomine ja sisestamine</span><span class="sxs-lookup"><span data-stu-id="84b62-189">Example 4: Create and post the intercompany invoice</span></span>
<span data-ttu-id="84b62-190">USSI, laenu väljastav juriidiline isik, peab koostama ja sisestama kontsernisisese arve.</span><span class="sxs-lookup"><span data-stu-id="84b62-190">USSI, the lending legal entity, must create and post the intercompany invoice.</span></span> <span data-ttu-id="84b62-191">Selle ülesande jaoks vajalike toimingute puhul on kaks sisestuspunkti.</span><span class="sxs-lookup"><span data-stu-id="84b62-191">There are two entry points for the steps that are required for this task.</span></span>

| <span data-ttu-id="84b62-192">Etapp</span><span class="sxs-lookup"><span data-stu-id="84b62-192">Step</span></span> | <span data-ttu-id="84b62-193">Sisestuspunkt</span><span class="sxs-lookup"><span data-stu-id="84b62-193">Entry point</span></span>                                                                                             | <span data-ttu-id="84b62-194">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="84b62-194">Description</span></span>                                                                                                                                      |
|------|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84b62-195">A</span><span class="sxs-lookup"><span data-stu-id="84b62-195">A</span></span>    | <span data-ttu-id="84b62-196">**Projektihaldus ja raamatupidamine** &gt; **Projektiarved** &gt; **Kontsernisisene kliendiarve**</span><span class="sxs-lookup"><span data-stu-id="84b62-196">**Project management and accounting** &gt; **Project invoices** &gt; **Intercompany customer invoice**</span></span>  | <span data-ttu-id="84b62-197">Klõpsake valikut **Uus** lehe **Kontsernisisese arve loomine** avamiseks.</span><span class="sxs-lookup"><span data-stu-id="84b62-197">Click **New** to open the **Create intercompany invoice** page.</span></span>                                                                                  |
| <span data-ttu-id="84b62-198">B</span><span class="sxs-lookup"><span data-stu-id="84b62-198">B</span></span>    | <span data-ttu-id="84b62-199">**Projektihaldus ja raamatupidamine** &gt; **Projektiarved** &gt; **Kontsernisisesed kliendiarved**</span><span class="sxs-lookup"><span data-stu-id="84b62-199">**Project management and accounting** &gt; **Project invoices** &gt; **Intercompany customer invoices**</span></span> | <span data-ttu-id="84b62-200">Sisestage lehele **Kontsernisisese arve loomine** juriidiline isik, määrake kanne, mis peaks olema lisatud, ja klõpsake siis käsku **Otsi**.</span><span class="sxs-lookup"><span data-stu-id="84b62-200">On the **Create intercompany invoice** page, enter the legal entity, specify the transaction that should be included, and then click **Search**.</span></span> |
| <span data-ttu-id="84b62-201">C</span><span class="sxs-lookup"><span data-stu-id="84b62-201">C</span></span>    | <span data-ttu-id="84b62-202">**Projektihaldus ja raamatupidamine** &gt; **Projektiarved** &gt; **Kontsernisisesed kliendiarved**</span><span class="sxs-lookup"><span data-stu-id="84b62-202">**Project management and accounting** &gt; **Project invoices** &gt; **Intercompany customer invoices**</span></span> | <span data-ttu-id="84b62-203">Valige arveldatavad kanded või klõpsake nuppu **Vali kõik** kõigi loendis olevate kannete arveldamiseks ja klõpsake siis nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="84b62-203">Select the transactions to invoice, or click **Select all** to invoice all the transactions in the list, and then click **OK**.</span></span>                  |
| <span data-ttu-id="84b62-204">D</span><span class="sxs-lookup"><span data-stu-id="84b62-204">D</span></span>    | <span data-ttu-id="84b62-205">Leht **Kontsernisisene arve**</span><span class="sxs-lookup"><span data-stu-id="84b62-205">The **Intercompany invoice** page</span></span>                                                                       | <span data-ttu-id="84b62-206">Kuvatakse kontsernisisene kliendiarve soovitus.</span><span class="sxs-lookup"><span data-stu-id="84b62-206">The intercompany customer invoice proposal is shown.</span></span>                                                                                             |
| <span data-ttu-id="84b62-207">E</span><span class="sxs-lookup"><span data-stu-id="84b62-207">E</span></span>    | <span data-ttu-id="84b62-208">Leht **Kontsernisisene arve**</span><span class="sxs-lookup"><span data-stu-id="84b62-208">The **Intercompany invoice** page</span></span>                                                                       | <span data-ttu-id="84b62-209">Klõpsake käsku **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="84b62-209">Click **Post**.</span></span>                                                                                                                                  |

## <a name="example-5-post-the-vendor-invoice-and-invoice-the-customer"></a><span data-ttu-id="84b62-210">5. näide: hankija arve sisestamine ja kliendile arve esitamine</span><span class="sxs-lookup"><span data-stu-id="84b62-210">Example 5: Post the vendor invoice and invoice the customer</span></span>
<span data-ttu-id="84b62-211">Kui laenu väljastav juriidiline isik USSI sisestab kontsernisisese kliendiarve, luuakse laenava juriidilise isiku FRSI all vastav ootel olev hankija arve.</span><span class="sxs-lookup"><span data-stu-id="84b62-211">When the lending legal entity, USSI, posts the intercompany customer invoice, a matching pending vendor invoice is created in the borrowing legal entity, FRSI.</span></span> <span data-ttu-id="84b62-212">Pärast selle hankija arve sisestamist esitab FRSI projekti kliendile ka arve USSI sisestatud tundide eest.</span><span class="sxs-lookup"><span data-stu-id="84b62-212">After this vendor invoice is posted, FRSI also invoices the project customer for the hours that USSI entered.</span></span> <span data-ttu-id="84b62-213">Selle ülesande jaoks vajalike toimingute puhul on kolm sisestuspunkti.</span><span class="sxs-lookup"><span data-stu-id="84b62-213">There are three entry points for the steps that are required for this task.</span></span>

| <span data-ttu-id="84b62-214">Etapp</span><span class="sxs-lookup"><span data-stu-id="84b62-214">Step</span></span> | <span data-ttu-id="84b62-215">Sisestuspunkt</span><span class="sxs-lookup"><span data-stu-id="84b62-215">Entry point</span></span>                                                                                        | <span data-ttu-id="84b62-216">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="84b62-216">Description</span></span>                                                                                                             |
|------|----------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="84b62-217">A</span><span class="sxs-lookup"><span data-stu-id="84b62-217">A</span></span>    | <span data-ttu-id="84b62-218">**Ostureskontro** &gt; **Arved** &gt; **Ootel hankija arved**</span><span class="sxs-lookup"><span data-stu-id="84b62-218">**Accounts payable** &gt; **Invoices** &gt; **Pending vendor invoices**</span></span>                            | <span data-ttu-id="84b62-219">Vaadake arve üle, veendumaks, et ajatabeli väärtused on lisatud, ja sisestage siis hankija arve.</span><span class="sxs-lookup"><span data-stu-id="84b62-219">Review the invoice to verify that the timesheet values are included, and then post the vendor invoice.</span></span>                  |
| <span data-ttu-id="84b62-220">B</span><span class="sxs-lookup"><span data-stu-id="84b62-220">B</span></span>    | <span data-ttu-id="84b62-221">**Projektihaldus ja raamatupidamine** &gt; **Projekti arved** &gt; **Projekti arvesoovitused**</span><span class="sxs-lookup"><span data-stu-id="84b62-221">**Project management and accounting** &gt; **Project invoices** &gt; **Project invoice proposals**</span></span> | <span data-ttu-id="84b62-222">Looge projektile uus projektiarve ja veenduge, et sisestatud tunnikanded kuvatakse.</span><span class="sxs-lookup"><span data-stu-id="84b62-222">Create a new project invoice for the project, and verify that the hour transactions that were posted appear.</span></span>            |
| <span data-ttu-id="84b62-223">C</span><span class="sxs-lookup"><span data-stu-id="84b62-223">C</span></span>    | <span data-ttu-id="84b62-224">Leht **Projekti arve**</span><span class="sxs-lookup"><span data-stu-id="84b62-224">The **Project invoice** page</span></span>                                                                       | <span data-ttu-id="84b62-225">Valige projekti arve ja klõpsake siis  **Kuva üksikasjad** kulude ja müügisumma ülevaatamiseks.</span><span class="sxs-lookup"><span data-stu-id="84b62-225">Select the project invoice, and then click **View details** to review the cost and sales amount.</span></span> <span data-ttu-id="84b62-226">Seejärel sisestage arve.</span><span class="sxs-lookup"><span data-stu-id="84b62-226">Then post the invoice.</span></span> |


<span data-ttu-id="84b62-227">Lisateabe saamiseks vt [Ettevõtetevahelise projekti arvete konfigureerimine](tasks/configure-intercompany-project-invoicing.md).</span><span class="sxs-lookup"><span data-stu-id="84b62-227">For more information, see [Configure intercompany project invoicing](tasks/configure-intercompany-project-invoicing.md).</span></span>

