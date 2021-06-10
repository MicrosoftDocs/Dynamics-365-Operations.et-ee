---
title: Proovibilansi finantsaruanded
description: See artikkel kirjeldab proovibilansi vaikearuandeid. See kirjeldab ka nende aruannetega seotud alustalasid ja kuidas saate muuta aruandeid, et sobituda teie ärivajadustega.
author: jinniew
ms.date: 05/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 26ec03422315a280f7e779f992cf694eb5f845ea
ms.sourcegitcommit: 365092f735310990e82516110141d42aaf04e654
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/27/2021
ms.locfileid: "6103654"
---
# <a name="trial-balance-financial-reports"></a><span data-ttu-id="115de-104">Proovibilansi finantsaruanded</span><span class="sxs-lookup"><span data-stu-id="115de-104">Trial balance financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="115de-105">See artikkel kirjeldab proovibilansi vaikearuandeid.</span><span class="sxs-lookup"><span data-stu-id="115de-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="115de-106">See kirjeldab ka nende aruannetega seotud alustalasid ja kuidas saate muuta aruandeid, et sobituda teie ärivajadustega.</span><span class="sxs-lookup"><span data-stu-id="115de-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

## <a name="default-trial-balance-reports"></a><span data-ttu-id="115de-107">Proovibilansi vaikearuanded</span><span class="sxs-lookup"><span data-stu-id="115de-107">Default trial balance reports</span></span>

<span data-ttu-id="115de-108">Finantsaruandluses on saadaval kolm proovibilansi aruannet.</span><span class="sxs-lookup"><span data-stu-id="115de-108">Three trial balance reports are available in Financial reporting.</span></span>

| <span data-ttu-id="115de-109">Vaikearuanne</span><span class="sxs-lookup"><span data-stu-id="115de-109">Default report</span></span>                                 | <span data-ttu-id="115de-110">Selle funktsioon</span><span class="sxs-lookup"><span data-stu-id="115de-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="115de-111">Üksikasjalik proovibilanss – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="115de-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="115de-112">Pakub saldoteavet kõigi kontode puhul, hõlmates deebet- ja kreeditsaldosid ja nende saldode netoväärtust koos kande kuupäeva, kande ja töölehe kirjeldusega.</span><span class="sxs-lookup"><span data-stu-id="115de-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="115de-113">Proovibilansi kokkuvõte – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="115de-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="115de-114">Pakub saldoteavet kõigi kontode puhul, hõlmates avamis- ja sulgemissaldosid ning deebet- ja kreeditsaldosid koos nende netoerinevusega.</span><span class="sxs-lookup"><span data-stu-id="115de-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="115de-115">Proovibilansi kokkuvõte aasta-aastalt – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="115de-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="115de-116">Pakub saldoteavet kõigi kontode puhul, hõlmates avamis- ja sulgemissaldosid ning deebet- ja kreeditsaldosid koos nende netoerinevusega praeguse aasta ja möödunud aasta kohta.</span><span class="sxs-lookup"><span data-stu-id="115de-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="115de-117">Koosteüksused</span><span class="sxs-lookup"><span data-stu-id="115de-117">Building blocks</span></span>
<span data-ttu-id="115de-118">Proovibilansi finantsaruanded kasutavad järgmisi koosteüksusi.</span><span class="sxs-lookup"><span data-stu-id="115de-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="115de-119">Vaikearuanne</span><span class="sxs-lookup"><span data-stu-id="115de-119">Default report</span></span>                                 | <span data-ttu-id="115de-120">Rea definitsioon</span><span class="sxs-lookup"><span data-stu-id="115de-120">Row definition</span></span>          | <span data-ttu-id="115de-121">Veeru määratlus</span><span class="sxs-lookup"><span data-stu-id="115de-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="115de-122">Üksikasjalik proovibilanss – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="115de-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="115de-123">Proovibilanss – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="115de-123">Trial Balance - Default</span></span> | <span data-ttu-id="115de-124">Üksikasjalik proovibilanss – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="115de-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="115de-125">Proovibilansi kokkuvõte – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="115de-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="115de-126">Proovibilanss – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="115de-126">Trial Balance - Default</span></span> | <span data-ttu-id="115de-127">Proovibilansi kokkuvõte – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="115de-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="115de-128">Proovibilansi kokkuvõte aasta-aastalt – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="115de-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="115de-129">Proovibilanss – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="115de-129">Trial Balance - Default</span></span> | <span data-ttu-id="115de-130">Proovibilansi kokkuvõte aasta-aastalt – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="115de-130">Summary Trial Balance Year Over Year - Default</span></span> |

> [!NOTE] 
> <span data-ttu-id="115de-131">**Proovibilansi** finantsaruandluses koostades märkige kindlasti **Kuva summadeta read** ja **Kuva aktiivsete ridadeta** read **Sätted** vahekaardil.</span><span class="sxs-lookup"><span data-stu-id="115de-131">When running the **Trial Balance** report in Financial reporting, be sure to select the check boxes for **Display rows with no amounts** and **Display reports with no active rows** on the **Settings** tab.</span></span>

### <a name="row-definition"></a><span data-ttu-id="115de-132">Rea definitsioon</span><span class="sxs-lookup"><span data-stu-id="115de-132">Row definition</span></span>

<span data-ttu-id="115de-133">Rea määratlus Proovibilanss – vaikimisi sisaldab ühte rida, mis koondab kõiki põhikontosid.</span><span class="sxs-lookup"><span data-stu-id="115de-133">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="115de-134">Seega saab igaüks luua aruande ilma muudatusi tegemata.</span><span class="sxs-lookup"><span data-stu-id="115de-134">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="115de-135">Aruande vaatamisel saate iga konto üksikasjade kuvamiseks minna ühes reas süvitsi.</span><span class="sxs-lookup"><span data-stu-id="115de-135">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="115de-136">Saate muuta readefinitsiooni nii, et see hõlmaks rohkem üksikasju.</span><span class="sxs-lookup"><span data-stu-id="115de-136">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="115de-137">Suvandi Proovibilanss – vaikimisi readefinitsiooni muutmiseks nii, et see hõlmaks kõikide kontode ridu, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="115de-137">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="115de-138">Klõpsake nuppu **Redigeeri** ja seejärel klõpsake suvandit **Sisesta read dimensioonidest**.</span><span class="sxs-lookup"><span data-stu-id="115de-138">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="115de-139">Käsk **Sisesta read dimensioonidest** võimaldab teil valida dimensioonid, mida soovite readefinitsiooni kaasata.</span><span class="sxs-lookup"><span data-stu-id="115de-139">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="115de-140">Selle readefinitsiooni puhul kasutate **Põhikontot**.</span><span class="sxs-lookup"><span data-stu-id="115de-140">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="115de-141">Veenduge, et **Põhikonto** sisaldab kõiki ampersande (&) ja seejärel klõpsake nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="115de-141">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="115de-142">Readefinitsioon sisaldab nüüd kõiki teie vaikimisi juriidilise isiku põhikontosid.</span><span class="sxs-lookup"><span data-stu-id="115de-142">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="115de-143">Veeru määratlus</span><span class="sxs-lookup"><span data-stu-id="115de-143">Column definition</span></span>

<span data-ttu-id="115de-144">Iga proovibilansi aruanne kasutab erinevat veeru definitsiooni.</span><span class="sxs-lookup"><span data-stu-id="115de-144">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="115de-145">Need veeru definitsioonid sisaldavad eri tüüpi veerge üksikasjade ja finantsandmete eri tasemete pakkumiseks.</span><span class="sxs-lookup"><span data-stu-id="115de-145">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="115de-146">**Üksikasjalik proovibilanss – vaikimisi veerutüübid:**</span><span class="sxs-lookup"><span data-stu-id="115de-146">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="115de-147">**DESC** – kirjeldus readefinitsioonist</span><span class="sxs-lookup"><span data-stu-id="115de-147">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="115de-148">**ACCT** – kontokoodid</span><span class="sxs-lookup"><span data-stu-id="115de-148">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="115de-149">**ATTR (3)** – atribuudid:</span><span class="sxs-lookup"><span data-stu-id="115de-149">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="115de-150">Kande kuupäev</span><span class="sxs-lookup"><span data-stu-id="115de-150">Transaction Date</span></span>
        -   <span data-ttu-id="115de-151">Kanne</span><span class="sxs-lookup"><span data-stu-id="115de-151">Voucher</span></span>
        -   <span data-ttu-id="115de-152">Töölehe kirjeldus</span><span class="sxs-lookup"><span data-stu-id="115de-152">Journal Description</span></span>
    -   <span data-ttu-id="115de-153">**FD** – finantsandmed, mis sisaldavad ainult deebeteid</span><span class="sxs-lookup"><span data-stu-id="115de-153">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="115de-154">**FD** – finantsandmed, mis sisaldavad ainult kreediteid</span><span class="sxs-lookup"><span data-stu-id="115de-154">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="115de-155">**CALC** – netoerinevus</span><span class="sxs-lookup"><span data-stu-id="115de-155">**CALC** – The net difference</span></span>
-   <span data-ttu-id="115de-156">**Proovibilansi kokkuvõte – vaikimisi veerutüübid:**</span><span class="sxs-lookup"><span data-stu-id="115de-156">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="115de-157">**ACCT** – kontokoodid</span><span class="sxs-lookup"><span data-stu-id="115de-157">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="115de-158">**DESC** – kirjeldus readefinitsioonist</span><span class="sxs-lookup"><span data-stu-id="115de-158">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="115de-159">**ATTR** – atribuut:</span><span class="sxs-lookup"><span data-stu-id="115de-159">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="115de-160">Kanne</span><span class="sxs-lookup"><span data-stu-id="115de-160">Voucher</span></span>
    -   <span data-ttu-id="115de-161">**FD** – algsaldo finantsandmed</span><span class="sxs-lookup"><span data-stu-id="115de-161">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="115de-162">**FD** – finantsandmed, mis sisaldavad ainult deebeteid</span><span class="sxs-lookup"><span data-stu-id="115de-162">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="115de-163">**FD** – finantsandmed, mis sisaldavad ainult kreediteid</span><span class="sxs-lookup"><span data-stu-id="115de-163">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="115de-164">**CALC** – netoerinevus</span><span class="sxs-lookup"><span data-stu-id="115de-164">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="115de-165">**CALC** – sulgemissaldo</span><span class="sxs-lookup"><span data-stu-id="115de-165">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="115de-166">**Proovibilansi kokkuvõte aasta-aastalt – vaikimisi:**</span><span class="sxs-lookup"><span data-stu-id="115de-166">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="115de-167">**ACCT** – kontokoodid</span><span class="sxs-lookup"><span data-stu-id="115de-167">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="115de-168">**DESC** – kirjeldus readefinitsioonist</span><span class="sxs-lookup"><span data-stu-id="115de-168">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="115de-169">**ATTR** – atribuut</span><span class="sxs-lookup"><span data-stu-id="115de-169">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="115de-170">Kanne</span><span class="sxs-lookup"><span data-stu-id="115de-170">Voucher</span></span>
    -   <span data-ttu-id="115de-171">**FD** – algsaldo finantsandmed praeguse aasta puhul</span><span class="sxs-lookup"><span data-stu-id="115de-171">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="115de-172">**FD** – finantsandmed, mis sisaldavad ainult jooksva aasta deebeteid</span><span class="sxs-lookup"><span data-stu-id="115de-172">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="115de-173">**FD** – finantsandmed, mis sisaldavad ainult jooksva aasta kreediteid</span><span class="sxs-lookup"><span data-stu-id="115de-173">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="115de-174">**CALC** – netoerinevus</span><span class="sxs-lookup"><span data-stu-id="115de-174">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="115de-175">**CALC** – sulgemissaldo</span><span class="sxs-lookup"><span data-stu-id="115de-175">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="115de-176">**FD** – finantsandmed, mis sisaldavad ainult möödunud aasta deebeteid</span><span class="sxs-lookup"><span data-stu-id="115de-176">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="115de-177">**FD** – finantsandmed, mis sisaldavad ainult möödunud aasta kreediteid</span><span class="sxs-lookup"><span data-stu-id="115de-177">**FD** – Financial data that contains only credits for the last year</span></span>

## <a name="additional-resources"></a><span data-ttu-id="115de-178">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="115de-178">Additional resources</span></span>

[<span data-ttu-id="115de-179">Finantsaruandluse ülevaade</span><span class="sxs-lookup"><span data-stu-id="115de-179">Financial reporting overview</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="115de-180">Finantsaruannete vaatamine</span><span class="sxs-lookup"><span data-stu-id="115de-180">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="115de-181">Dynamicsi finantsaruandluse ajaveeb</span><span class="sxs-lookup"><span data-stu-id="115de-181">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
