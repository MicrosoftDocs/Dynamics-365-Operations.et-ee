---
title: Proovibilansi finantsaruanded
description: See artikkel kirjeldab proovibilansi vaikearuandeid. See kirjeldab ka nende aruannetega seotud alustalasid ja kuidas saate muuta aruandeid, et sobituda teie ärivajadustega.
author: jcart1106
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerTrialBalanceListPage
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 12314
ms.assetid: 3b77d6f3-fd07-41a7-9ddb-1b22d1ae33fc
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 842eecf68f5a658be6cdc7a05c365a18fe7d91dc
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846095"
---
# <a name="trial-balance-financial-reports"></a><span data-ttu-id="e2a66-104">Proovibilansi finantsaruanded</span><span class="sxs-lookup"><span data-stu-id="e2a66-104">Trial balance financial reports</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e2a66-105">See artikkel kirjeldab proovibilansi vaikearuandeid.</span><span class="sxs-lookup"><span data-stu-id="e2a66-105">This article describes the default reports for trial balances.</span></span> <span data-ttu-id="e2a66-106">See kirjeldab ka nende aruannetega seotud alustalasid ja kuidas saate muuta aruandeid, et sobituda teie ärivajadustega.</span><span class="sxs-lookup"><span data-stu-id="e2a66-106">It also describes the building blocks that are associated with these reports and how you can modify the reports to fit your business requirements.</span></span> 

<a name="default-trial-balance-reports"></a><span data-ttu-id="e2a66-107">Proovibilansi vaikearuanded</span><span class="sxs-lookup"><span data-stu-id="e2a66-107">Default trial balance reports</span></span>
-----------------------------

<span data-ttu-id="e2a66-108">Microsoft Dynamics 365 for Finance and Operationsi finantsaruandluses on saadaval kolm proovibilansi aruannet.</span><span class="sxs-lookup"><span data-stu-id="e2a66-108">Three trial balance reports are available in Financial reporting in Microsoft Dynamics 365 for Finance and Operations.</span></span>

| <span data-ttu-id="e2a66-109">Vaikearuanne</span><span class="sxs-lookup"><span data-stu-id="e2a66-109">Default report</span></span>                                 | <span data-ttu-id="e2a66-110">Selle funktsioon</span><span class="sxs-lookup"><span data-stu-id="e2a66-110">What it does</span></span>                                                                                                                                                                                        |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2a66-111">Üksikasjalik proovibilanss – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="e2a66-111">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="e2a66-112">Pakub saldoteavet kõigi kontode puhul, hõlmates deebet- ja kreeditsaldosid ja nende saldode netoväärtust koos kande kuupäeva, kande ja töölehe kirjeldusega.</span><span class="sxs-lookup"><span data-stu-id="e2a66-112">Provides balance information for all accounts, and includes debit and credit balances, and the net of these, together with the transaction date, voucher, and journal description.</span></span>                  |
| <span data-ttu-id="e2a66-113">Proovibilansi kokkuvõte – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="e2a66-113">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="e2a66-114">Pakub saldoteavet kõigi kontode puhul, hõlmates avamis- ja sulgemissaldosid ning deebet- ja kreeditsaldosid koos nende netoerinevusega.</span><span class="sxs-lookup"><span data-stu-id="e2a66-114">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference.</span></span>                                        |
| <span data-ttu-id="e2a66-115">Proovibilansi kokkuvõte aasta-aastalt – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="e2a66-115">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="e2a66-116">Pakub saldoteavet kõigi kontode puhul, hõlmates avamis- ja sulgemissaldosid ning deebet- ja kreeditsaldosid koos nende netoerinevusega praeguse aasta ja möödunud aasta kohta.</span><span class="sxs-lookup"><span data-stu-id="e2a66-116">Provides balance information for all accounts, and includes opening and closing balances, and debit and credit balances, together with their net difference for the current year and the past year.</span></span> |

## <a name="building-blocks"></a><span data-ttu-id="e2a66-117">Koosteüksused</span><span class="sxs-lookup"><span data-stu-id="e2a66-117">Building blocks</span></span>
<span data-ttu-id="e2a66-118">Proovibilansi finantsaruanded kasutavad järgmisi koosteüksusi.</span><span class="sxs-lookup"><span data-stu-id="e2a66-118">The trial balance financial reports use the following building blocks.</span></span>

| <span data-ttu-id="e2a66-119">Vaikearuanne</span><span class="sxs-lookup"><span data-stu-id="e2a66-119">Default report</span></span>                                 | <span data-ttu-id="e2a66-120">Rea definitsioon</span><span class="sxs-lookup"><span data-stu-id="e2a66-120">Row definition</span></span>          | <span data-ttu-id="e2a66-121">Veeru määratlus</span><span class="sxs-lookup"><span data-stu-id="e2a66-121">Column definition</span></span>                              |
|------------------------------------------------|-------------------------|------------------------------------------------|
| <span data-ttu-id="e2a66-122">Üksikasjalik proovibilanss – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="e2a66-122">Detailed Trial Balance - Default</span></span>               | <span data-ttu-id="e2a66-123">Proovibilanss – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="e2a66-123">Trial Balance - Default</span></span> | <span data-ttu-id="e2a66-124">Üksikasjalik proovibilanss – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="e2a66-124">Detailed Trial Balance - Default</span></span>               |
| <span data-ttu-id="e2a66-125">Proovibilansi kokkuvõte – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="e2a66-125">Summary Trial Balance – Default</span></span>                | <span data-ttu-id="e2a66-126">Proovibilanss – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="e2a66-126">Trial Balance - Default</span></span> | <span data-ttu-id="e2a66-127">Proovibilansi kokkuvõte – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="e2a66-127">Summary Trial Balance - Default</span></span>                |
| <span data-ttu-id="e2a66-128">Proovibilansi kokkuvõte aasta-aastalt – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="e2a66-128">Summary Trial Balance Year Over Year – Default</span></span> | <span data-ttu-id="e2a66-129">Proovibilanss – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="e2a66-129">Trial Balance - Default</span></span> | <span data-ttu-id="e2a66-130">Proovibilansi kokkuvõte aasta-aastalt – vaikimisi</span><span class="sxs-lookup"><span data-stu-id="e2a66-130">Summary Trial Balance Year Over Year - Default</span></span> |

### <a name="row-definition"></a><span data-ttu-id="e2a66-131">Rea definitsioon</span><span class="sxs-lookup"><span data-stu-id="e2a66-131">Row definition</span></span>

<span data-ttu-id="e2a66-132">Rea määratlus Proovibilanss – vaikimisi sisaldab ühte rida, mis koondab kõiki põhikontosid.</span><span class="sxs-lookup"><span data-stu-id="e2a66-132">The row definition, Trial Balance – Default, contains a single row that pulls in all main accounts.</span></span> <span data-ttu-id="e2a66-133">Seega saab igaüks luua aruande ilma muudatusi tegemata.</span><span class="sxs-lookup"><span data-stu-id="e2a66-133">Therefore, anyone can generate the report without having to make any modifications.</span></span> <span data-ttu-id="e2a66-134">Aruande vaatamisel saate iga konto üksikasjade kuvamiseks minna ühes reas süvitsi.</span><span class="sxs-lookup"><span data-stu-id="e2a66-134">When you view the report, you drill into the single row to see details about each account.</span></span> <span data-ttu-id="e2a66-135">Saate muuta readefinitsiooni nii, et see hõlmaks rohkem üksikasju.</span><span class="sxs-lookup"><span data-stu-id="e2a66-135">You can modify the row definition so that it includes more detail.</span></span> <span data-ttu-id="e2a66-136">Suvandi Proovibilanss – vaikimisi readefinitsiooni muutmiseks nii, et see hõlmaks kõikide kontode ridu, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="e2a66-136">To modify the Trial Balance – Default row definition so that it includes rows for all accounts, follow these steps.</span></span>

1.  <span data-ttu-id="e2a66-137">Klõpsake nuppu **Redigeeri** ja seejärel klõpsake suvandit **Sisesta read dimensioonidest**.</span><span class="sxs-lookup"><span data-stu-id="e2a66-137">Click **Edit**, and then click **Insert Rows from Dimensions**.</span></span> <span data-ttu-id="e2a66-138">Käsk **Sisesta read dimensioonidest** võimaldab teil valida dimensioonid, mida soovite readefinitsiooni kaasata.</span><span class="sxs-lookup"><span data-stu-id="e2a66-138">The **Insert Rows from Dimensions** command lets you choose the dimensions that you want to have in your row definition.</span></span> <span data-ttu-id="e2a66-139">Selle readefinitsiooni puhul kasutate **Põhikontot**.</span><span class="sxs-lookup"><span data-stu-id="e2a66-139">For this row definition, you're going to use **Main Account**.</span></span>
2.  <span data-ttu-id="e2a66-140">Veenduge, et **Põhikonto** sisaldab kõiki ampersande (&) ja seejärel klõpsake nuppu **OK**.</span><span class="sxs-lookup"><span data-stu-id="e2a66-140">Make sure that **Main Account** contains all ampersands (&), and then click **OK**.</span></span>

<span data-ttu-id="e2a66-141">Readefinitsioon sisaldab nüüd kõiki teie vaikimisi juriidilise isiku põhikontosid.</span><span class="sxs-lookup"><span data-stu-id="e2a66-141">The row definition now contains all the main accounts for your default legal entity.</span></span>

### <a name="column-definition"></a><span data-ttu-id="e2a66-142">Veeru määratlus</span><span class="sxs-lookup"><span data-stu-id="e2a66-142">Column definition</span></span>

<span data-ttu-id="e2a66-143">Iga proovibilansi aruanne kasutab erinevat veeru definitsiooni.</span><span class="sxs-lookup"><span data-stu-id="e2a66-143">Each trial balance report uses a different column definition.</span></span> <span data-ttu-id="e2a66-144">Need veeru definitsioonid sisaldavad eri tüüpi veerge üksikasjade ja finantsandmete eri tasemete pakkumiseks.</span><span class="sxs-lookup"><span data-stu-id="e2a66-144">These column definitions contain different types of columns to provide different levels of detail and financial data.</span></span>

-   <span data-ttu-id="e2a66-145">**Üksikasjalik proovibilanss – vaikimisi veerutüübid:**</span><span class="sxs-lookup"><span data-stu-id="e2a66-145">**Detailed Trial Balance – Default column types:**</span></span>
    -   <span data-ttu-id="e2a66-146">**DESC** – kirjeldus readefinitsioonist</span><span class="sxs-lookup"><span data-stu-id="e2a66-146">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="e2a66-147">**ACCT** – kontokoodid</span><span class="sxs-lookup"><span data-stu-id="e2a66-147">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="e2a66-148">**ATTR (3)** – atribuudid:</span><span class="sxs-lookup"><span data-stu-id="e2a66-148">**ATTR (3)** – Attributes:</span></span>
        -   <span data-ttu-id="e2a66-149">Kande kuupäev</span><span class="sxs-lookup"><span data-stu-id="e2a66-149">Transaction Date</span></span>
        -   <span data-ttu-id="e2a66-150">Kanne</span><span class="sxs-lookup"><span data-stu-id="e2a66-150">Voucher</span></span>
        -   <span data-ttu-id="e2a66-151">Töölehe kirjeldus</span><span class="sxs-lookup"><span data-stu-id="e2a66-151">Journal Description</span></span>
    -   <span data-ttu-id="e2a66-152">**FD** – finantsandmed, mis sisaldavad ainult deebeteid</span><span class="sxs-lookup"><span data-stu-id="e2a66-152">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="e2a66-153">**FD** – finantsandmed, mis sisaldavad ainult kreediteid</span><span class="sxs-lookup"><span data-stu-id="e2a66-153">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="e2a66-154">**CALC** – netoerinevus</span><span class="sxs-lookup"><span data-stu-id="e2a66-154">**CALC** – The net difference</span></span>
-   <span data-ttu-id="e2a66-155">**Proovibilansi kokkuvõte – vaikimisi veerutüübid:**</span><span class="sxs-lookup"><span data-stu-id="e2a66-155">**Summary Trial Balance – Default columns types:**</span></span>
    -   <span data-ttu-id="e2a66-156">**ACCT** – kontokoodid</span><span class="sxs-lookup"><span data-stu-id="e2a66-156">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="e2a66-157">**DESC** – kirjeldus readefinitsioonist</span><span class="sxs-lookup"><span data-stu-id="e2a66-157">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="e2a66-158">**ATTR** – atribuut:</span><span class="sxs-lookup"><span data-stu-id="e2a66-158">**ATTR** – An attribute:</span></span>
        -   <span data-ttu-id="e2a66-159">Kanne</span><span class="sxs-lookup"><span data-stu-id="e2a66-159">Voucher</span></span>
    -   <span data-ttu-id="e2a66-160">**FD** – algsaldo finantsandmed</span><span class="sxs-lookup"><span data-stu-id="e2a66-160">**FD** – The beginning balance financial data</span></span>
    -   <span data-ttu-id="e2a66-161">**FD** – finantsandmed, mis sisaldavad ainult deebeteid</span><span class="sxs-lookup"><span data-stu-id="e2a66-161">**FD** – Financial data that contains only debits</span></span>
    -   <span data-ttu-id="e2a66-162">**FD** – finantsandmed, mis sisaldavad ainult kreediteid</span><span class="sxs-lookup"><span data-stu-id="e2a66-162">**FD** – Financial data that contains only credits</span></span>
    -   <span data-ttu-id="e2a66-163">**CALC** – netoerinevus</span><span class="sxs-lookup"><span data-stu-id="e2a66-163">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="e2a66-164">**CALC** – sulgemissaldo</span><span class="sxs-lookup"><span data-stu-id="e2a66-164">**CALC** – The closing balance</span></span>
-   <span data-ttu-id="e2a66-165">**Proovibilansi kokkuvõte aasta-aastalt – vaikimisi:**</span><span class="sxs-lookup"><span data-stu-id="e2a66-165">**Summary Trial Balance Year Over Year – Default:**</span></span>
    -   <span data-ttu-id="e2a66-166">**ACCT** – kontokoodid</span><span class="sxs-lookup"><span data-stu-id="e2a66-166">**ACCT** – Account codes</span></span>
    -   <span data-ttu-id="e2a66-167">**DESC** – kirjeldus readefinitsioonist</span><span class="sxs-lookup"><span data-stu-id="e2a66-167">**DESC** – The description from the row definition</span></span>
    -   <span data-ttu-id="e2a66-168">**ATTR** – atribuut</span><span class="sxs-lookup"><span data-stu-id="e2a66-168">**ATTR** – An attribute</span></span>
        -   <span data-ttu-id="e2a66-169">Kanne</span><span class="sxs-lookup"><span data-stu-id="e2a66-169">Voucher</span></span>
    -   <span data-ttu-id="e2a66-170">**FD** – algsaldo finantsandmed praeguse aasta puhul</span><span class="sxs-lookup"><span data-stu-id="e2a66-170">**FD** – The beginning balance financial data for the current year</span></span>
    -   <span data-ttu-id="e2a66-171">**FD** – finantsandmed, mis sisaldavad ainult jooksva aasta deebeteid</span><span class="sxs-lookup"><span data-stu-id="e2a66-171">**FD** – Financial data that contains only debits for the current year</span></span>
    -   <span data-ttu-id="e2a66-172">**FD** – finantsandmed, mis sisaldavad ainult jooksva aasta kreediteid</span><span class="sxs-lookup"><span data-stu-id="e2a66-172">**FD** – Financial data that contains only credits for the current year</span></span>
    -   <span data-ttu-id="e2a66-173">**CALC** – netoerinevus</span><span class="sxs-lookup"><span data-stu-id="e2a66-173">**CALC** – The net difference</span></span>
    -   <span data-ttu-id="e2a66-174">**CALC** – sulgemissaldo</span><span class="sxs-lookup"><span data-stu-id="e2a66-174">**CALC** – The closing balance</span></span>
    -   <span data-ttu-id="e2a66-175">**FD** – finantsandmed, mis sisaldavad ainult möödunud aasta deebeteid</span><span class="sxs-lookup"><span data-stu-id="e2a66-175">**FD** – Financial data that contains only debits for the last year</span></span>
    -   <span data-ttu-id="e2a66-176">**FD** – finantsandmed, mis sisaldavad ainult möödunud aasta kreediteid</span><span class="sxs-lookup"><span data-stu-id="e2a66-176">**FD** – Financial data that contains only credits for the last year</span></span>



<a name="additional-resources"></a><span data-ttu-id="e2a66-177">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="e2a66-177">Additional resources</span></span>
--------

[<span data-ttu-id="e2a66-178">Finantsaruandlus</span><span class="sxs-lookup"><span data-stu-id="e2a66-178">Financial reporting</span></span>](financial-reporting-getting-started.md)

[<span data-ttu-id="e2a66-179">Finantsaruannete vaatamine</span><span class="sxs-lookup"><span data-stu-id="e2a66-179">View financial reports</span></span>](view-financial-reports.md)

[<span data-ttu-id="e2a66-180">Dynamicsi finantsaruandluse ajaveeb</span><span class="sxs-lookup"><span data-stu-id="e2a66-180">Dynamics Financial Reporting Blog</span></span>](https://blogs.msdn.com/b/dynamics_financial_reporting/)



