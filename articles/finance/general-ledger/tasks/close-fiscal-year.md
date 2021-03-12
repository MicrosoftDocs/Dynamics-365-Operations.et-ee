---
title: Finantsaasta sulgemine
description: See protseduur kirjeldab rahandusaasta sulgemise protsessi etappe, millega kantakse saldod uude finantsaastasse üle.
author: aprilolson
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, LedgerFiscalCloseGroup, LedgerFiscalCloseAddLedger, SysLookupMultiSelectGrid, LedgerFiscalCloseRunGroup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b82cc7e4077a1bd50eab30f234c2f63c79e81d84
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994686"
---
# <a name="close-the-fiscal-year"></a><span data-ttu-id="91a61-103">Finantsaasta sulgemine</span><span class="sxs-lookup"><span data-stu-id="91a61-103">Close the fiscal year</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="91a61-104">See protseduur kirjeldab rahandusaasta sulgemise protsessi etappe, millega kantakse saldod uude finantsaastasse üle.</span><span class="sxs-lookup"><span data-stu-id="91a61-104">This procedure steps through the year end close process that transfers balances to a new fiscal year.</span></span>


## <a name="validate-year-end-close-parameters"></a><span data-ttu-id="91a61-105">Aastalõpu sulgemise parameetrite kontrollimine</span><span class="sxs-lookup"><span data-stu-id="91a61-105">Validate year-end close parameters</span></span>
1. <span data-ttu-id="91a61-106">Avage **Navigeerimispaan > Moodulid > Pearaamat > Pearaamatu häälestus > Pearaamatu parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="91a61-106">Go to **Navigation pane > Modules > General ledger > Ledger setup > General ledger parameters**.</span></span>
2. <span data-ttu-id="91a61-107">Laiendage jaotist **Rahandusaasta** sulgemine.</span><span class="sxs-lookup"><span data-stu-id="91a61-107">Expand the **Fiscal year close** section.</span></span>
3. <span data-ttu-id="91a61-108">Valige suvandi **Kustuta aasta lõpetamise kanded ülekandmisel** väärtuseks „Jah“ või „Ei“.</span><span class="sxs-lookup"><span data-stu-id="91a61-108">Select 'Yes' or 'No' for the **Delete close-of-year transactions during transfer** option.</span></span>
    
    <span data-ttu-id="91a61-109">Kui rahandusaasta on juba suletud ja aastalõpu sulgemine käivitatakse uuesti, on see säte oluline.</span><span class="sxs-lookup"><span data-stu-id="91a61-109">If the fiscal year has already been closed and the year-end close is being run again, this setting is important.</span></span> <span data-ttu-id="91a61-110">Kui väärtuseks on määratud Jah, kustutatakse eelmise aastalõpu sulgemise kanne ja luuakse uus kanne kõigile kontode algsaldodele.</span><span class="sxs-lookup"><span data-stu-id="91a61-110">If set to Yes, the voucher for the previous year-end close will be deleted, and a new voucher will be created for all accounts beginning balances.</span></span> <span data-ttu-id="91a61-111">Kui väärtuseks on määratud Ei, jääb eelmine kanne alles ja uus kanne luuakse ainult korrigeerimiskannetele, mis sisestati pärast viimast aastalõpu sulgemist.</span><span class="sxs-lookup"><span data-stu-id="91a61-111">If set to No, the previous voucher will remain and a new voucher will only be created for adjusting entries that were posted after the last year-end close.</span></span>

4. <span data-ttu-id="91a61-112">Valige suvandi **Loo ülekande ajal sulgemiskanded** väärtuseks „Jah“ või „Ei“.</span><span class="sxs-lookup"><span data-stu-id="91a61-112">Select 'Yes' or 'No' for the **Create closing transactions during transfer** option.</span></span>

    <span data-ttu-id="91a61-113">Kui väärtuseks on määratud Jah, luuakse kaks kannet.</span><span class="sxs-lookup"><span data-stu-id="91a61-113">If set to Yes, two transactions are created.</span></span> <span data-ttu-id="91a61-114">Üks kanne luuakse suletavas rahandusaastas, et viia tulu- ja kulukontode saldod nulli, ja teine kanne luuakse järgmises rahandusaastas algsaldode jaoks.</span><span class="sxs-lookup"><span data-stu-id="91a61-114">One voucher is created in the fiscal year being closed to bring the balances of the P&L ledger accounts down to zero and a second voucher is created in the next fiscal year for the beginning balances.</span></span> <span data-ttu-id="91a61-115">Kui väärtuseks on määratud Ei, luuakse järgmises rahandusaastas algsaldode jaoks üks kanne.</span><span class="sxs-lookup"><span data-stu-id="91a61-115">If set to No, a single voucher is created in the next fiscal year for the beginning balances.</span></span>  

5. <span data-ttu-id="91a61-116">Valige suvandi **Määra rahandusaasta olek püsivalt suletuks** väärtuseks „Jah“ või „Ei“.</span><span class="sxs-lookup"><span data-stu-id="91a61-116">Select 'Yes' or 'No' for the **Set fiscal year status to permanently closed** option.</span></span>

    <span data-ttu-id="91a61-117">Kui väärtuseks on määratud Jah, määratakse rahandusaasta olekuks Jäädavalt suletud.</span><span class="sxs-lookup"><span data-stu-id="91a61-117">If set to Yes, the fiscal year status will be set to Permanently closed.</span></span>  <span data-ttu-id="91a61-118">Kuna jäädavalt suletud aastat ei saa uuesti avada, tasub määrata selle valiku väärtuseks Ei.</span><span class="sxs-lookup"><span data-stu-id="91a61-118">Because a permanently closed year cannot be reopened, it would be a best practice to set this option to No.</span></span>  

6. <span data-ttu-id="91a61-119">Valige suvandi **Kande number tuleb aastalõpu sulgemise käigus täita** väärtuseks „Jah“ või „Ei“.</span><span class="sxs-lookup"><span data-stu-id="91a61-119">Select 'Yes' or 'No' for the **Voucher number must be filled in during the year end close** option.</span></span>

    <span data-ttu-id="91a61-120">Kui väärtuseks on määratud Jah, tuleb aastalõpu sulgemisprotsessi käigus kande number käsitsi sisestada.</span><span class="sxs-lookup"><span data-stu-id="91a61-120">If set to Yes, a voucher number must be manually entered during the year end close process.</span></span> <span data-ttu-id="91a61-121">Selle kande numbri loomiseks ei kasutata numbriseeriat.</span><span class="sxs-lookup"><span data-stu-id="91a61-121">A number sequence is not used to generate this voucher number.</span></span> <span data-ttu-id="91a61-122">Selle väärtuse olekuks tasub määrata Jah.</span><span class="sxs-lookup"><span data-stu-id="91a61-122">It's a best practice to set this to Yes.</span></span>  

7. <span data-ttu-id="91a61-123">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="91a61-123">Close the page.</span></span>
8. <span data-ttu-id="91a61-124">Minge jaotisse **Pearaamat > Perioodi sulgemine > Rahandusaasta sulgemine**.</span><span class="sxs-lookup"><span data-stu-id="91a61-124">Go to **General ledger > Period close > Year end close**.</span></span>
9. <span data-ttu-id="91a61-125">Klõpsake aastalõpu sulgemise malli loomiseks nuppu **Uus**.</span><span class="sxs-lookup"><span data-stu-id="91a61-125">Click **New** to create a year-end close template.</span></span>

    <span data-ttu-id="91a61-126">Juriidiliste isikute grupile, mille puhul aastalõpu sulgemine käivitada, saab luua malli.</span><span class="sxs-lookup"><span data-stu-id="91a61-126">A template can be created for a group of legal entities for which to run the year-end close.</span></span> <span data-ttu-id="91a61-127">Seda malli saab igal aastal uuesti kasutada.</span><span class="sxs-lookup"><span data-stu-id="91a61-127">This template can be reused year after year.</span></span>  

10. <span data-ttu-id="91a61-128">Sisestage väljale **Grupi nimi** aastalõpu sulgemise malli nimi.</span><span class="sxs-lookup"><span data-stu-id="91a61-128">In the **Group name** field, enter a year-end close template name..</span></span>
11. <span data-ttu-id="91a61-129">Valige väljal **Rahanduskalender** finantsaasta, mille jaoks mall luuakse.</span><span class="sxs-lookup"><span data-stu-id="91a61-129">In the **Fiscal calendar** field, select the fiscal year for which the template will be created.</span></span>

    <span data-ttu-id="91a61-130">Aastalõpu sulgemise malli saab kokku panna ainult sama rahandusaastat kasutavad juriidilised isikud.</span><span class="sxs-lookup"><span data-stu-id="91a61-130">Only legal entities which use the same fiscal year can be grouped together in the year-end close template.</span></span> <span data-ttu-id="91a61-131">Seda seetõttu, et aastalõpu sulgemine toimub rahandusaasta, mitte kuupäeva valimisega.</span><span class="sxs-lookup"><span data-stu-id="91a61-131">This is because the year end close is done by selecting a fiscal year, not a date.</span></span>  

12. <span data-ttu-id="91a61-132">Klõpsake **Toimingupaanil** valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="91a61-132">On the **Action pane**, click **Save**.</span></span>
13. <span data-ttu-id="91a61-133">Klõpsake jaotises **Juriidilised isikud** nuppu **Lisa**, et valida selle malli juriidilised isikud.</span><span class="sxs-lookup"><span data-stu-id="91a61-133">In the **Legal entities** section, click **Add** to select the legal entities for this template.</span></span>
    
    <span data-ttu-id="91a61-134">Juriidilisi isikuid saab lisada, valides juriidilised isikud või organisatsiooni hierarhia.</span><span class="sxs-lookup"><span data-stu-id="91a61-134">Legal entities can be added by either selecting the legal entities or by selecting an organizational hierarchy.</span></span>  <span data-ttu-id="91a61-135">Lisatakse ainult need organisatsiooni hierarhiad, millel on valitud sama rahanduskalender.</span><span class="sxs-lookup"><span data-stu-id="91a61-135">Only legal entities with the organizational hierarchy with the same fiscal calendar selected will be added.</span></span>  

14. <span data-ttu-id="91a61-136">Valige juriidilised isikud või organisatsiooni hierarhia.</span><span class="sxs-lookup"><span data-stu-id="91a61-136">Select either the legal entities or the organizational hierarchy.</span></span>
15. <span data-ttu-id="91a61-137">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="91a61-137">Click **OK**.</span></span>
16. <span data-ttu-id="91a61-138">Valige „Jah“ või „Ei“ **Edasta bilansidimensioon**.</span><span class="sxs-lookup"><span data-stu-id="91a61-138">Select 'Yes' or 'No' in the **Transfer balance sheet dimension**.</span></span>

    <span data-ttu-id="91a61-139">Selle valiku väärtuseks tasub bilansikontode puhul määrata Jah.</span><span class="sxs-lookup"><span data-stu-id="91a61-139">It's best practice to set this option to Yes for Balance sheet accounts.</span></span> <span data-ttu-id="91a61-140">See säilitab bilansikontode algsaldode loomisel sisestatud kannete finantsdimensioonid.</span><span class="sxs-lookup"><span data-stu-id="91a61-140">This will maintain the financial dimensions on posted transactions when creating the beginning balances for the balance sheet accounts.</span></span> <span data-ttu-id="91a61-141">Tulu- ja kulukontode puhul võite valida finantsdimensioonide säilitamise (Sule kõik), kui saldod viiakse jaotisse Jaotamata kasum, või lasta finantsdimensioonid asendada teise dimensiooniväärtusega (Sule üksik).</span><span class="sxs-lookup"><span data-stu-id="91a61-141">For profit and loss accounts, you can select to maintain the financial dimensions (Close all) when the balances are moved to Retained earnings or you can select to have the financial dimensions replaced with a different dimension value (Close single).</span></span> <span data-ttu-id="91a61-142">Kui teete valiku Sule üksik, saate määratleda igale dimensioonile konkreetse dimensiooniväärtuse või isegi selle tühjaks jätta.</span><span class="sxs-lookup"><span data-stu-id="91a61-142">If you choose Close single, you can define a specific dimension value for each dimension or even choose to leave it blank.</span></span>  

17. <span data-ttu-id="91a61-143">Klõpsake valikut **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="91a61-143">Click **Save**.</span></span>
18. <span data-ttu-id="91a61-144">Käivitage aastalõpu sulgemine valides **Rahandusaasta sulgemise käivitamine** **Toimingupaanil**.</span><span class="sxs-lookup"><span data-stu-id="91a61-144">Start the year-end close by choosing **Run fiscal close** on the **Action Pane**.</span></span> <span data-ttu-id="91a61-145">Valitud mallil käivitatakse aastalõpu sulgemine.</span><span class="sxs-lookup"><span data-stu-id="91a61-145">The year-end close will be run for the selected template.</span></span>  
19. <span data-ttu-id="91a61-146">Valige mallilt kõik juriidilised isikud või nende alamkogum, mille puhul aastalõpu sulgemine käivitada.</span><span class="sxs-lookup"><span data-stu-id="91a61-146">Select all or a subset of legal entities from the template for which to run the year-end close.</span></span>

    <span data-ttu-id="91a61-147">Aastalõpu sulgemise esmakordsel käivitamisel võib enamik organisatsioone otsustada algsaldode saamiseks käivitada aastalõpu sulgemise kõigi malli juriidiliste isikute puhul.</span><span class="sxs-lookup"><span data-stu-id="91a61-147">When first running the year-end close, to get beginning balance,s most organizations may choose to run the year-end close for all legal entities within the template.</span></span> <span data-ttu-id="91a61-148">Kui pärast seda tehakse korrigeerimiskandeid, võite valida aastalõpu sulgemise käivitamise ainult nende juriidiliste isikute puhul, kellel on korrigeerimisi.</span><span class="sxs-lookup"><span data-stu-id="91a61-148">If adjusting entries are made after that, you may choose to run the year-end close for only the legal entities that have adjustments.</span></span>  

20. <span data-ttu-id="91a61-149">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="91a61-149">Click **OK**.</span></span>
21. <span data-ttu-id="91a61-150">Valige finantsaasta, mille puhul aastalõpu sulgemine käivitada.</span><span class="sxs-lookup"><span data-stu-id="91a61-150">Select the fiscal year for which to run the year-end close.</span></span>
22. <span data-ttu-id="91a61-151">Tippige väärtus väljale **Kanne**.</span><span class="sxs-lookup"><span data-stu-id="91a61-151">In the **Voucher field**, type a value.</span></span> <span data-ttu-id="91a61-152">On hea mõte lisada kande numbrisse rahandusaasta, et loodud aastalõpu sulgemise kannet oleks lihtsam leida.</span><span class="sxs-lookup"><span data-stu-id="91a61-152">It's best practice to include the fiscal year in the voucher number, to make it easier to find the year-end close voucher that is created.</span></span>  
23. <span data-ttu-id="91a61-153">Aastalõpu sulgemine käivitub vaikimisi partiina.</span><span class="sxs-lookup"><span data-stu-id="91a61-153">The year-end close defaults to run in batch.</span></span> <span data-ttu-id="91a61-154">Aeganõudvate protsesside puhul on mõistlik kasutada partiirežiimi.</span><span class="sxs-lookup"><span data-stu-id="91a61-154">It's best practice for long-running processes to run in batch mode.</span></span> <span data-ttu-id="91a61-155">See on tavaliselt üks neist protsessidest, seetõttu on vaikesäte partiirežiimi kasutamine.</span><span class="sxs-lookup"><span data-stu-id="91a61-155">This is typically one of those processes, which is why the default is to use batch mode.</span></span>  
24. <span data-ttu-id="91a61-156">Klõpsake valikut **OK**.</span><span class="sxs-lookup"><span data-stu-id="91a61-156">Click **OK**.</span></span>

