---
title: Aastalõpu sulgemisel puuduvad algsaldod
description: Selles teemas selgitatakse, miks algsaldod võivad aasta sulgemisel puududa ja kuidas neid saldosid taastada, kui need puuduvad.
author: kweekley
ms.date: 05/12/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-12-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 045d0bf11b11c9a353858ce3ca82c698dbceea7c
ms.sourcegitcommit: 817716c2e96f24af0ef1d7d5323afdeccdc602f3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/13/2021
ms.locfileid: "6028559"
---
# <a name="year-end-close-missing-opening-balances"></a><span data-ttu-id="4a6ff-103">Aastalõpu sulgemisel puuduvad algsaldod</span><span class="sxs-lookup"><span data-stu-id="4a6ff-103">Year-end close missing opening balances</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4a6ff-104">Selles teemas selgitatakse, miks algsaldod võivad aasta sulgemisel puududa ja kuidas neid saldosid taastada, kui need puuduvad.</span><span class="sxs-lookup"><span data-stu-id="4a6ff-104">This topic explains why opening balances might be missing when you close a year, and how to rebuild those balances if they are missing.</span></span>

### <a name="symptom"></a><span data-ttu-id="4a6ff-105">Sümptom</span><span class="sxs-lookup"><span data-stu-id="4a6ff-105">Symptom</span></span>

<span data-ttu-id="4a6ff-106">Miks pärast pearaamatu aastalõpu sulgemist pole algsaldosid?</span><span class="sxs-lookup"><span data-stu-id="4a6ff-106">Why are there no beginning balances after running the General ledger year-end close?</span></span> 

### <a name="resolution"></a><span data-ttu-id="4a6ff-107">Lahendus</span><span class="sxs-lookup"><span data-stu-id="4a6ff-107">Resolution</span></span>

<span data-ttu-id="4a6ff-108">Kui olete pearaamatus aasta sulgenud ja seejärel loonud proovibilansi, mis ei näita järgmise finantsaasta algsaldosid, tuleks kontrollida järgmist.</span><span class="sxs-lookup"><span data-stu-id="4a6ff-108">Here are things to check if you've closed a year in General ledger, and then generated a trial balance that doesn't display opening balances for the next fiscal year.</span></span>

<span data-ttu-id="4a6ff-109">Kui välja **Eelmise sulgemise tagasivõtmine** väärtuseks on määratud **Jah**, siis eelmine sama finantsaasta aastalõpu sulgemine tühistatakse.</span><span class="sxs-lookup"><span data-stu-id="4a6ff-109">If the **Undo previous close** field is set to **Yes**, the previous year-end close for the same fiscal year is being reversed.</span></span> <span data-ttu-id="4a6ff-110">Aastalõpu sulgemise tühistamisprotsessi käigus kustutatakse kõik sulgemissaldo ja algsaldo kirjed, justkui aastat ei oleks kunagi suletud.</span><span class="sxs-lookup"><span data-stu-id="4a6ff-110">When running a process to reverse the year-end close, all entries for both closing and opening balances will be deleted, as if the year had never been closed.</span></span> <span data-ttu-id="4a6ff-111">Kanded kustutatakse samuti.</span><span class="sxs-lookup"><span data-stu-id="4a6ff-111">The vouchers are also deleted.</span></span> <span data-ttu-id="4a6ff-112">Aastalõpu sulgemise protsessi ei käivitata automaatselt uuesti.</span><span class="sxs-lookup"><span data-stu-id="4a6ff-112">The year-end close process will not run again automatically.</span></span> <span data-ttu-id="4a6ff-113">Peate ise protsessi uuesti käivitama, seades valiku **Eelmise sulgemise tagasivõtmine** olekuks nüüd **Ei**.</span><span class="sxs-lookup"><span data-stu-id="4a6ff-113">You must start the process again, this time updating the **Undo previous close** option to **No**.</span></span>

<span data-ttu-id="4a6ff-114">Seda stsenaariumit käsitletakse aastalõpu sulgemise KKK teemas.</span><span class="sxs-lookup"><span data-stu-id="4a6ff-114">This scenario is covered in the year-end close FAQ topic.</span></span> <span data-ttu-id="4a6ff-115">Lisateavet leiate artiklist [Aastalõpu tegevuste KKK](faq-year-end-activities.md).</span><span class="sxs-lookup"><span data-stu-id="4a6ff-115">For more information, see [Year-end activities FAQ](faq-year-end-activities.md).</span></span>

### <a name="symptom"></a><span data-ttu-id="4a6ff-116">Sümptom</span><span class="sxs-lookup"><span data-stu-id="4a6ff-116">Symptom</span></span>

<span data-ttu-id="4a6ff-117">Käitasin aastalõpu sulgemise ja valiku **Eelmise sulgemise tagasivõtmine** olekuks oli seatud **Ei**, kuid mul ei ole ikka veel oma finantsaasta algsaldosid.</span><span class="sxs-lookup"><span data-stu-id="4a6ff-117">I ran year-end close with the **Undo previous close** option set to **No**, and I still do not have opening balances for my fiscal year.</span></span>

### <a name="resolution"></a><span data-ttu-id="4a6ff-118">Lahendus</span><span class="sxs-lookup"><span data-stu-id="4a6ff-118">Resolution</span></span>

<span data-ttu-id="4a6ff-119">Esmalt kontrollige pakett-töö olekut.</span><span class="sxs-lookup"><span data-stu-id="4a6ff-119">First check the status of the batch job.</span></span> <span data-ttu-id="4a6ff-120">Aasta sulgemine hõlmab mitmeid eraldi ülesandeid, kuid kõige kriitilisem samm on pakettülesanne kirjeldusega **Etapp 5.0.0**.</span><span class="sxs-lookup"><span data-stu-id="4a6ff-120">Closing a year includes a number of separate tasks, but the most critical step is the batch task with the task description **Step 5.0.0**.</span></span> <span data-ttu-id="4a6ff-121">Selle etapi käigus toimub avamiskannete (ja valikuliselt sulgemiskannete) sisestamine pearaamatusse.</span><span class="sxs-lookup"><span data-stu-id="4a6ff-121">Posting the opening transactions, and optionally the closing transactions, to General ledger takes place during this step.</span></span> 

<span data-ttu-id="4a6ff-122">[![Pakett-tööde ajaloo loend](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)</span><span class="sxs-lookup"><span data-stu-id="4a6ff-122">[![Batch history list](./media/yec-mssng-open-blnces-01.png)](./media/yec-mssng-open-blnces-01.png)</span></span>

<span data-ttu-id="4a6ff-123">Kui see etapp jõudis edukalt lõpule, kuid te ei näe algsaldosid lehel **Proovibilansi päring** (**Pearaamat > Päringud ja aruanded > Proovibilanss**), vaadake läbi aastalõpu sulgemise pakett-töö tulemused, et näha, kas saldode taastamise etapp jõudis edukalt lõpule.</span><span class="sxs-lookup"><span data-stu-id="4a6ff-123">If this step ended successfully but you don’t see opening balances on the **Trial balance inquiry** page (**General ledger > Inquires and reports > Trial balance**), review the results of the year-end close batch job to see if the Rebuild balances step completed successfully.</span></span>

<span data-ttu-id="4a6ff-124">[![Aastalõpu sulgemise pakett-töö tulemused](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)</span><span class="sxs-lookup"><span data-stu-id="4a6ff-124">[![Results of year-end close batch job](./media/yec-mssng-open-blnces-02.png)](./media/yec-mssng-open-blnces-02.png)</span></span>

<span data-ttu-id="4a6ff-125">Kui see etapp mingil põhjusel nurjus, sisestati avamiskanded (ja valikuliselt sulgemiskanded) tõenäoliselt edukalt.</span><span class="sxs-lookup"><span data-stu-id="4a6ff-125">If this step has failed for any reason, the opening (and optionally closing) transactions were likely posted successfully.</span></span> <span data-ttu-id="4a6ff-126">Te saate kontrollida pearaamatu kannete sisestamise edukust lehe **Pearaamatu kannete päring** abil, sisestades suletud aasta aastalõpu sulgemise dialoogis esitatud pearaamatu kande numbri ja kuupäeva (**Pearaamat > Päringud ja aruanded > Pearaamatu kanded**).</span><span class="sxs-lookup"><span data-stu-id="4a6ff-126">You can verify that the General ledger transactions were posted successfully using the **Voucher transactions inquiry** page by specifying the voucher number and date provided on the year-end close dialog for the year that you closed, (**General Ledger > Inquiries and reports > Voucher transactions**).</span></span>

<span data-ttu-id="4a6ff-127">[![Pearaamatu kannete päring](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)</span><span class="sxs-lookup"><span data-stu-id="4a6ff-127">[![Voucher transactions inquiry](./media/yec-mssng-open-blnces-03.png)](./media/yec-mssng-open-blnces-03.png)</span></span>

<span data-ttu-id="4a6ff-128">Kui avamiskanded (ja valikuliselt sulgemiskanded) on olemas, pole teil vaja aastalõpu sulgemist uuesti käitada.</span><span class="sxs-lookup"><span data-stu-id="4a6ff-128">If the opening (and optionally closing) vouchers are present, you don’t need to run the year-end close again.</span></span> <span data-ttu-id="4a6ff-129">Selle asemel vaadake järgmisest jaotisest teavet selle kohta, kuidas edasi liikuda.</span><span class="sxs-lookup"><span data-stu-id="4a6ff-129">Instead refer to the next section for information about how to move forward.</span></span>

### <a name="symptom"></a><span data-ttu-id="4a6ff-130">Sümptom</span><span class="sxs-lookup"><span data-stu-id="4a6ff-130">Symptom</span></span>

<span data-ttu-id="4a6ff-131">Aastalõpu sulgemise etapp „Saldode taastamine” nurjus. Kas ma pean kogu aastalõpu sulgemise protsessi uuesti käitama?</span><span class="sxs-lookup"><span data-stu-id="4a6ff-131">The “Rebuild balances” step in the year-end close failed, do I need to re-run the entire year-end close process?</span></span>

### <a name="resolution"></a><span data-ttu-id="4a6ff-132">Lahendus</span><span class="sxs-lookup"><span data-stu-id="4a6ff-132">Resolution</span></span>

<span data-ttu-id="4a6ff-133">Saldode taastamise etapi käigus uuendatakse pearaamatu saldod, mida kasutatakse proovibilansi päringu loomisel.</span><span class="sxs-lookup"><span data-stu-id="4a6ff-133">The Rebuild balances step updates the General ledger balances that are used when the Trial balance inquiry is generated.</span></span>  <span data-ttu-id="4a6ff-134">See on aastalõpu sulgemise protsessi viimane etapp.</span><span class="sxs-lookup"><span data-stu-id="4a6ff-134">It is the final step in the year-end close process.</span></span>  <span data-ttu-id="4a6ff-135">Kui see etapp on ainus nurjunud etapp, on pearaamatu kanded edukalt sisestatud.</span><span class="sxs-lookup"><span data-stu-id="4a6ff-135">If this step is the only step that failed, the General ledger transactions have posted successfully.</span></span>  <span data-ttu-id="4a6ff-136">Aastalõpu sulgemist ei ole vaja uuesti käitada.</span><span class="sxs-lookup"><span data-stu-id="4a6ff-136">You do not need to run the year-end close again.</span></span> <span data-ttu-id="4a6ff-137">Saldode taastamise protsessi saate käsitsi käitada lehe **Finantsdimensioonikogumid** abil (**Pearaamat > Kontoplaan > Dimensioonid > Finantsdimensioonikogumid**).</span><span class="sxs-lookup"><span data-stu-id="4a6ff-137">You can run the process to rebuild the balances manually using the **Financial dimension sets** page (**General ledger > Chart of accounts > Dimensions > Financial dimension sets**).</span></span>

<span data-ttu-id="4a6ff-138">[![Nupp Taasta saldod lehel Finantsdimensioonikogumid](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)</span><span class="sxs-lookup"><span data-stu-id="4a6ff-138">[![Rebuild balances button on Financial dimension sets page](./media/yec-mssng-open-blnces-04.png)](./media/yec-mssng-open-blnces-04.png)</span></span>

<span data-ttu-id="4a6ff-139">Kui selle etapi töötlemiseks kulub liiga palju aega, soovitame üle vaadata finantsdimensioonikogumite parimad tavad, mida kirjeldatakse artiklis [Finantsdimensioonide uuendamise parimad tavad](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets).</span><span class="sxs-lookup"><span data-stu-id="4a6ff-139">If this step takes a long time to process, we recommend reviewing the best practices for financial dimension sets as described in [Best practices for updating Financial dimension sets](https://community.dynamics.com/365/financeandoperations/b/dynamics-365-finance-blog/posts/best-practices-for-updating-financial-dimension-set-dimension-sets).</span></span> 

