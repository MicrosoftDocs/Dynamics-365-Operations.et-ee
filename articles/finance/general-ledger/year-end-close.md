---
title: Aastalõpu sulgemine
description: See teema kirjeldab nõutavat seadistust ja juhiseid pearaamatu aastalõpu sulgemise protsessi käivitamiseks.
author: kweekley
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3071365640eb6c012cb9af5461e885bb3f135143
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175376"
---
# <a name="year-end-close"></a><span data-ttu-id="e358e-103">Aastalõpu sulgemine</span><span class="sxs-lookup"><span data-stu-id="e358e-103">Year-end close</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e358e-104">See teema kirjeldab nõutavat seadistust ja juhiseid pearaamatu aastalõpu sulgemise protsessi käivitamiseks.</span><span class="sxs-lookup"><span data-stu-id="e358e-104">This topic describes the required setup and steps for running the general ledger year-end close process.</span></span> 

<span data-ttu-id="e358e-105">Rahandusaasta lõpus peate käivitama aastalõpu sulgemisprotsessi algsaldode ülekandmiseks uude aastasse.</span><span class="sxs-lookup"><span data-stu-id="e358e-105">At the end of a fiscal year, you must run the year-end close process to transfer opening balances to the new year.</span></span> <span data-ttu-id="e358e-106">Enamik organisatsioone käivitavad aastalõpu sulgemise protsessi mitu korda.</span><span class="sxs-lookup"><span data-stu-id="e358e-106">Most organizations will run the year-end close process multiple times.</span></span> <span data-ttu-id="e358e-107">Esimene kord tuleks saldod uude finantsaastasse teisaldada.</span><span class="sxs-lookup"><span data-stu-id="e358e-107">The first time would be to get the balances moved into the new fiscal year.</span></span> <span data-ttu-id="e358e-108">Aastalõpu sulgemise saab seejärel uuesti käivitada nii palju kordi, kui on vaja, et teisaldada saldod kirjete reguleerimisest uude finantsaastasse.</span><span class="sxs-lookup"><span data-stu-id="e358e-108">The year-end close can then be run again, as many times are required, to move the balances from adjusting entries into the new fiscal year.</span></span> 

<span data-ttu-id="e358e-109">Aastalõpu sulgemise protsessi käigus on loodud kaks võimalikku kannete tüüpi.</span><span class="sxs-lookup"><span data-stu-id="e358e-109">During the year-end close process, there are two types of possible transactions created.</span></span> <span data-ttu-id="e358e-110">Avamiskanne luuakse alati ja seda kasutatakse uues finantsaastas algsaldode loomiseks.</span><span class="sxs-lookup"><span data-stu-id="e358e-110">An Opening transaction is always generated and is used to create the opening balances in the new fiscal year.</span></span> <span data-ttu-id="e358e-111">Avamiskanne näitab uue finantsaasta bilansi pearaamatukonto saldosid ja jaotamata kasumi pearaamatukontol olevate kasumi ja kahjumi pearaamatukonto saldodest pärinevaid saldosid.</span><span class="sxs-lookup"><span data-stu-id="e358e-111">The Opening transaction shows the balance sheet ledger account balances in the new fiscal year and balances from the profit and loss ledger account balances in the retained earnings ledger account in the new fiscal year.</span></span> <span data-ttu-id="e358e-112">Sulgemiskanne luuakse valikuliselt, et tuua kasumi- ja kahjumikontode saldod suletavas finantsaastas alla nullini.</span><span class="sxs-lookup"><span data-stu-id="e358e-112">The Closing transaction is optionally created to bring the balances of the profit and loss accounts down to zero in the fiscal year being closed.</span></span>

## <a name="prepare-to-run-the-year-end-close"></a><span data-ttu-id="e358e-113">Aastalõpu sulgemise käitamiseks ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="e358e-113">Prepare to run the year-end close</span></span>
<span data-ttu-id="e358e-114">Enne aastalõpu sulgemisprotsessi käitamist kinnitage sätted järgmisesse kohta.</span><span class="sxs-lookup"><span data-stu-id="e358e-114">Before you run the year-end close process, validate the settings for the following:</span></span> 

<span data-ttu-id="e358e-115">**Põhikonto** lehel</span><span class="sxs-lookup"><span data-stu-id="e358e-115">On the **Main account** page:</span></span>

-   <span data-ttu-id="e358e-116">Kinnitage, et **Põhikonto tüüp** on iga põhikonto jaoks õigesti määratletud.</span><span class="sxs-lookup"><span data-stu-id="e358e-116">Validate the **Main account type** is defined properly for each main account.</span></span> <span data-ttu-id="e358e-117">Põhikonto tüüpi kasutatakse määramaks, kas põhikonto saldo tuuakse edasi algsaldona või suletakse avamiskandes jaotamata kasumisse.</span><span class="sxs-lookup"><span data-stu-id="e358e-117">The Main account type is used to determine whether the balance of the main account will be brought forward as an opening balance or closed into retained earnings in the Opening transaction.</span></span>
-   <span data-ttu-id="e358e-118">Välja **Avamiskonto** saab kasutada aastalõpu sulgemise käigus põhikonto saldo üleviimiseks uuele põhikontole.</span><span class="sxs-lookup"><span data-stu-id="e358e-118">The **Opening account** field can be used to transfer the balance of the main account to a new main account during the year-end close.</span></span> <span data-ttu-id="e358e-119">Uus põhikonto sisestatakse väljale **Avamiskonto**.</span><span class="sxs-lookup"><span data-stu-id="e358e-119">The new main account is entered in the **Opening account** field.</span></span> <span data-ttu-id="e358e-120">Tavaliselt kasutatakse seda bilansi põhikontode jaoks, kui põhikonto on inaktiveeritud ja uut põhikontot kasutatakse uue finantsaasta jaoks.</span><span class="sxs-lookup"><span data-stu-id="e358e-120">Typically this will be used for balance sheet main accounts when the main account is inactivated and a new main account is used for the new fiscal year.</span></span>

<span data-ttu-id="e358e-121">Lehel **Pearaamatu parameetrid** valikus **Finantsaasta sulgemine** toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="e358e-121">On the **General ledger parameters** page under **Fiscal year close**:</span></span>

-   <span data-ttu-id="e358e-122">Valikut **Kustuta aasta lõpetamise kanded ülekandmisel** kasutatakse määramiseks, kas süsteemi loodud avamiskanne eelmisest aastalõpu sulgemisest tuleks kustutada, kui aastalõpu sulgemine käivitatakse uuesti.</span><span class="sxs-lookup"><span data-stu-id="e358e-122">The **Delete close of year transactions** option is used to specify whether the system-generated Opening transaction from a previous year-end close should be deleted when the year-end close is run again.</span></span> <span data-ttu-id="e358e-123">Kui see valik on seatud olekusse **Jah**, kustutatakse eelmine avamiskanne ja uus avamiskanne luuakse praeguste saldode põhjal.</span><span class="sxs-lookup"><span data-stu-id="e358e-123">If this option is set to **Yes**, the previous Opening transaction is deleted and a new Opening transaction is created based on the current balances.</span></span> <span data-ttu-id="e358e-124">Kui see valik on seatud olekusse **Ei**, püsib eelmine avamiskanne ja luuakse täiendav avamiskanne, et teisaldada saldod edasi pärast eelmist aastalõpu sulgemist sisestatud kannete reguleerimist.</span><span class="sxs-lookup"><span data-stu-id="e358e-124">If this option is set to **No**, the previous Opening transaction remains and an additional Opening transaction is created to move the balances forward from adjusting transactions posted after the previous year-end close.</span></span>
-   <span data-ttu-id="e358e-125">Valikut **Loo ülekande ajal sulgemiskanded** kasutatakse sulgemiskannete loomiseks suletaval finantsaastal, et viia kasumi- ja kahjumikontode saldod nulli.</span><span class="sxs-lookup"><span data-stu-id="e358e-125">The **Create closing transactions during transfer** option is used to create Closing transactions in the fiscal year being closed in order to bring the balances of the profit and loss accounts to zero.</span></span> <span data-ttu-id="e358e-126">Kui see valik on seatud olekusse **Jah**, luuakse nii avamis- kui ka sulgemiskanne.</span><span class="sxs-lookup"><span data-stu-id="e358e-126">If this option is set to **Yes**, both the Opening transaction and Closing transaction is created.</span></span> <span data-ttu-id="e358e-127">Kui see valik on seatud olekusse **Ei**, luuakse järgmisel finantsaastal saldode üleviimiseks ainult avamiskanne.</span><span class="sxs-lookup"><span data-stu-id="e358e-127">If this option is set to **No**, only the Opening transaction is created in the next fiscal year to transfer the balances.</span></span> <span data-ttu-id="e358e-128">Kasumi- ja kahjumikonto saldod püsivad finantsaasta lõpus.</span><span class="sxs-lookup"><span data-stu-id="e358e-128">The profit and loss account balances remain at the end of the fiscal year.</span></span>
-   <span data-ttu-id="e358e-129">Valik **Rahandusaasta oleku määramine püsivalt suletuks** kasutatakse finantsaasta seadmiseks püsivalt suletud olekusse.</span><span class="sxs-lookup"><span data-stu-id="e358e-129">The **Set fiscal year status to permanently closed** option is used to set the fiscal year to a permanently closed status.</span></span> <span data-ttu-id="e358e-130">Kasutage seda sätet ettevaatlikult, kuna kõiki püsivalt suletud olekuga perioode ei saa uuesti avada, ennetades korrigeerimiste sisestamist finantsaastasse.</span><span class="sxs-lookup"><span data-stu-id="e358e-130">Use this setting with caution, because all periods with a permanently closed status cannot be reopened, preventing adjustments from being posted to the fiscal year.</span></span> <span data-ttu-id="e358e-131">Selle valiku olekuks tasub määrata **Ei**.</span><span class="sxs-lookup"><span data-stu-id="e358e-131">It's a best practice to set this to **No**.</span></span>
-   <span data-ttu-id="e358e-132">Valikut **Kande number peab olema täidetud** kasutatakse määratlemiseks, kas kande number on aastalõpu sulgemisprotsessi käitamisel kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="e358e-132">The **Voucher number must be filled in** option is used to define whether a voucher number is required when running the year-end close process.</span></span> <span data-ttu-id="e358e-133">On hea tava nõuda kande numbrit, et avamiskannet hõlpsasti tuvastada.</span><span class="sxs-lookup"><span data-stu-id="e358e-133">It’s a best practice to require a voucher number in order to easily identify the Opening transaction.</span></span>

<span data-ttu-id="e358e-134">Lehel **Rahanduskalender** toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="e358e-134">On the **Fiscal calendar** page:</span></span>

-   <span data-ttu-id="e358e-135">Järgmine finantsaasta peab eksisteerima enne aastalõpu sulgemise käitamist.</span><span class="sxs-lookup"><span data-stu-id="e358e-135">The next fiscal year must exist before running the year-end close.</span></span> <span data-ttu-id="e358e-136">Järgmine finantsaasta on kohustuslik, et luua avamisperioodil algsaldod.</span><span class="sxs-lookup"><span data-stu-id="e358e-136">The next fiscal year is required in order to create the beginning balances in the opening period.</span></span>

<span data-ttu-id="e358e-137">Lehel **Pearaamatu kalender** toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="e358e-137">On the **Ledger calendar** page:</span></span>

-   <span data-ttu-id="e358e-138">Valikuline: iga suletavat finantsaasta rahandusaastat saab määrata olekusse **Ootel**, et takistada uute kannete sisestamist.</span><span class="sxs-lookup"><span data-stu-id="e358e-138">Optional: Each fiscal period for the fiscal year being closed can be set to **On hold** to prevent new transactions from being entered.</span></span> <span data-ttu-id="e358e-139">Korrigeerivate sisestuste tuvastamisel saab ooteloleku perioodid korrigeerivate sisestuste sisestamiseks taasavada isegi siis, kui aastalõpu sulgemisprotsess on juba käivitatud.</span><span class="sxs-lookup"><span data-stu-id="e358e-139">When adjusting entries are identified, the On hold periods can be reopened to post adjusting entries, even if the year-end close process has already been run.</span></span>

## <a name="define-year-end-close-templates"></a><span data-ttu-id="e358e-140">Aastalõpu sulgemismallide määratlemine</span><span class="sxs-lookup"><span data-stu-id="e358e-140">Define year-end close templates</span></span>
<span data-ttu-id="e358e-141">Pärast süsteemi konfigureerimist saab käivitada aastalõpu sulgemisprotsessi.</span><span class="sxs-lookup"><span data-stu-id="e358e-141">After the system is configured, the year-end close process can be run.</span></span> <span data-ttu-id="e358e-142">Lehel **Aastalõpu sulgemine** saab määratleda malli selliste juriidiliste isikute grupile, mille jaoks aastalõpu sulgemisprotsess käivitatakse.</span><span class="sxs-lookup"><span data-stu-id="e358e-142">On the **Year-end close** page, a template can be defined for the group of legal entities for which the year-end close process will be run.</span></span> <span data-ttu-id="e358e-143">Malli taaskasutatakse igal aastalõpu sulgemisel, kuid seda saab muuta, kui teie organisatsioon muutub.</span><span class="sxs-lookup"><span data-stu-id="e358e-143">The template will be reused at each year-end close, but can be modified if your organization changes.</span></span> 

<span data-ttu-id="e358e-144">Esmalt määratlege malli jaoks **Grupi nimi** ja valige rahanduskalender.</span><span class="sxs-lookup"><span data-stu-id="e358e-144">First, define the **Group name** for the template, and select the fiscal calendar.</span></span> <span data-ttu-id="e358e-145">Grupi nimi peaks identifitseerima lisatud juriidiliste isikute gruppi.</span><span class="sxs-lookup"><span data-stu-id="e358e-145">The group name should identify the group of legal entities included.</span></span>  <span data-ttu-id="e358e-146">Näiteks saab mallid seadistada geograafia põhjal nii, et Põhja-Ameerika, EMEA ja APAC juriidiliste isikute jaoks on loodud eraldi grupid.</span><span class="sxs-lookup"><span data-stu-id="e358e-146">For example, the templates may be set up based on geography, with separate groups created for North American legal entities, EMEA legal entities, and APAC legal entities.</span></span> 

<span data-ttu-id="e358e-147">Järgmisena saab mallile lisada juriidilised isikud.</span><span class="sxs-lookup"><span data-stu-id="e358e-147">Next, the legal entities can be added to the template.</span></span> <span data-ttu-id="e358e-148">Juriidilisi isikute lisamiseks saate valida organisatsioonihierarhia või valida juriidilised isikud.</span><span class="sxs-lookup"><span data-stu-id="e358e-148">Legal entities can be added by selecting an organizational hierarchy or by selecting the legal entities.</span></span> <span data-ttu-id="e358e-149">Organisatsioonihierarhia valimisel lisatakse malli ainult hierarhiasisesed juriidilised isikud, kes kasutavad valitud rahanduskalendrit.</span><span class="sxs-lookup"><span data-stu-id="e358e-149">If an organizational hierarchy is selected, only legal entities within the hierarchy that use the selected fiscal calendar will be added to the template.</span></span> <span data-ttu-id="e358e-150">Kui kasutate malli lisamiseks juriidilisi isikuid, saab lisada ainult sama rahanduskalendriga juriidilisi isikuid.</span><span class="sxs-lookup"><span data-stu-id="e358e-150">If you use legal entities to add to the template, only legal entities with the same fiscal calendar can be added.</span></span> <span data-ttu-id="e358e-151">Sama rahanduskalender on vajalik, kuna aastalõpu sulgemine käivitatakse finantsaasta valimisega, mis võib varieeruda olenevalt kalendrist.</span><span class="sxs-lookup"><span data-stu-id="e358e-151">The same fiscal calendar is required because the year-end close is run by selecting a fiscal year, which can vary from calendar to calendar.</span></span> 

<span data-ttu-id="e358e-152">Pärast juriidiliste isikute lisamist määratlege iga juriidilise isiku jaoks kinnipeetud tulude põhikontod.</span><span class="sxs-lookup"><span data-stu-id="e358e-152">After the legal entities are added, define the retained earnings main accounts for each legal entity.</span></span> <span data-ttu-id="e358e-153">Välja **Viimase rahandusaasta sulgemise kuupäev** värskendatakse iga kord, kui juriidilise isiku jaoks käivitatakse aastalõpu sulgemine.</span><span class="sxs-lookup"><span data-stu-id="e358e-153">The **Date of last year end close** field will be updated each time the year end close is run for the legal entity.</span></span> 

<span data-ttu-id="e358e-154">Vahekaarti **Finantsdimensioon** kasutatakse määratlemiseks, milliseid finantsdimensioone avamiskandel kasutatakse.</span><span class="sxs-lookup"><span data-stu-id="e358e-154">The **Financial dimension** tab is used to define which financial dimensions will be used on the Opening transaction.</span></span> <span data-ttu-id="e358e-155">Pange tähele, et määratletavad sätted on asjakohased ainult ruudustikus **Juriidilised isikud** valitud juriidilisele isikule.</span><span class="sxs-lookup"><span data-stu-id="e358e-155">Note that the settings you are defining are relevant to only the legal entity selected in the **Legal entities** grid.</span></span> <span data-ttu-id="e358e-156">Korrake seadistust iga ruudustikus oleva juriidilise isiku jaoks.</span><span class="sxs-lookup"><span data-stu-id="e358e-156">You will repeat the setup for each legal entity in the grid.</span></span> 

<span data-ttu-id="e358e-157">Valikut **Bilansi dimensioonide ülekandmine** kasutatakse määratlemiseks, kas bilansikontodele sisestatud kannetel olevaid finantsdimensioone tuleks säilitada avamiskandes.</span><span class="sxs-lookup"><span data-stu-id="e358e-157">The **Transfer balance sheet dimensions** is used to define whether the financial dimensions on transactions posted to balance sheet accounts should be maintained on the Opening transaction.</span></span> <span data-ttu-id="e358e-158">Selle valiku olekuks tasub seada **Jah**.</span><span class="sxs-lookup"><span data-stu-id="e358e-158">It’s a best practice to set this option to **Yes**.</span></span> <span data-ttu-id="e358e-159">Valikut **Kasumi ja kahjumi dimensioonide ülekandmine** kasutatakse määratlemiseks, millised kasumi- ja kahjumikontole sisestatud finantsdimensioonid viiakse üle jaotamata kasumi põhikontole.</span><span class="sxs-lookup"><span data-stu-id="e358e-159">The **Transfer profit and loss dimensions** is used to define which financial dimensions on transactions posted to profit and loss account will be transferred to the retained earnings main account.</span></span> <span data-ttu-id="e358e-160">Esmalt tuvastage valitud juriidilisele isikule asjakohased finantsdimensioonid.</span><span class="sxs-lookup"><span data-stu-id="e358e-160">First, identify the financial dimensions relevant to the selected legal entity.</span></span> <span data-ttu-id="e358e-161">See peaks hõlmama kõiki finantsdimensioone, mille suhtes on aasta jooksul sisestatud, isegi kui finantsdimensioon ei ole osa aktiivsest kontostruktuurist.</span><span class="sxs-lookup"><span data-stu-id="e358e-161">This would include any financial dimensions posted against during the year, even if the financial dimension is not part of an active account structure.</span></span> <span data-ttu-id="e358e-162">Järgmisena määratlege iga dimensioon kui **Sule üksik** või **Sule kõik**.</span><span class="sxs-lookup"><span data-stu-id="e358e-162">Next, define each dimension as either **Close single** or **Close all**.</span></span>  <span data-ttu-id="e358e-163">Vaikesäte on **Sule kõik**, mis säilitab algsed finantsdimensiooni väärtused sisestatud kannetest ja kasutab neid jaotamata kasumi konto jaoks avamissaldode loomiseks.</span><span class="sxs-lookup"><span data-stu-id="e358e-163">The default is **Close all**, which maintains the original financial dimension values from posted transactions and uses them for creating the opening balances for the retained earnings account.</span></span> <span data-ttu-id="e358e-164">Eraldi jaotamata kasumi algsaldod luuakse iga unikaalse finantsdimensiooni väärtuste unikaalse kombinatsiooni puhul.</span><span class="sxs-lookup"><span data-stu-id="e358e-164">Separate retained earnings beginning balances will be created for each unique combination of financial dimension values.</span></span> <span data-ttu-id="e358e-165">Valiku **Sule üksik** tegemisel võetakse kõik selle finantsdimensiooniga sisestatud kanded kokku jaotamata kasumi algsaldosse valiku **Sule üksik** väljale sisestatud dimensiooniväärtuse puhul.</span><span class="sxs-lookup"><span data-stu-id="e358e-165">If **Close single** is selected, all transactions posted with that financial dimension will be summarized into a retained earnings beginning balance for the dimension value entered in the field after **Close single**.</span></span> <span data-ttu-id="e358e-166">Näiteks eeldame, et kõik finantsaasta kanded sisestati põhikonto struktuuriga – osakond.</span><span class="sxs-lookup"><span data-stu-id="e358e-166">For example, assume that all transactions for the fiscal year were posted with the account structure of Main account - Department.</span></span> <span data-ttu-id="e358e-167">Malli osakonna finantsdimensioonis tehakse valik **Sule üksik** ja sisestatakse väärtus 100.</span><span class="sxs-lookup"><span data-stu-id="e358e-167">On the Department financial dimension on the template, **Close single** is selected and 100 is the value entered.</span></span> <span data-ttu-id="e358e-168">Kui kõik osakondadesse 200, 300 ja 400 sisestatud kanded on 100 000 dollarit, luuakse jaotamata kasumi jaoks üks algsaldo – 100.</span><span class="sxs-lookup"><span data-stu-id="e358e-168">If the total income of all transactions posted to departments 200, 300, and 400 is $100,000, one opening balance will be created for Retained earnings - 100.</span></span> <span data-ttu-id="e358e-169">Kui teete valiku **Sule üksik** ja jätate finantsdimensiooni väärtuse tühjaks, sisestatakse kõik kanded jaotamata kasumisse nii, et dimensiooni väärtus on tühi.</span><span class="sxs-lookup"><span data-stu-id="e358e-169">If you select **Close single** and leave the financial dimension value blank, all transactions will post to retained earnings with that dimension value being blank.</span></span> 

<span data-ttu-id="e358e-170">Aastalõpu sulgemise protsess ei järgi kontostruktuure.</span><span class="sxs-lookup"><span data-stu-id="e358e-170">The year-end close process doesn’t adhere to account structures.</span></span> <span data-ttu-id="e358e-171">Seda selle tõttu, et kontostruktuurid võivad muutuda finantsaasta jooksul ja nende muudatuste tõttu pole võimalik tuvastada asjakohast kontot.</span><span class="sxs-lookup"><span data-stu-id="e358e-171">This is because account structures can change throughout a fiscal year and it's not always possible to identify the relevant account structure due to those changes.</span></span>  <span data-ttu-id="e358e-172">Avamiskannete loomisel tuuakse saldod edasi finantsdimensioonidega, nagu on määratletud aastalõpu sulgemise mallis.</span><span class="sxs-lookup"><span data-stu-id="e358e-172">When opening transactions are created, the balances will be brought forward with financial dimensions as defined in the year end close template.</span></span> <span data-ttu-id="e358e-173">Algsaldo kirjed võivad hõlmata praeguses kontostruktuuris ja segmendikombinatsioonides mittesisalduvaid finantsdimensioone, mis ei kehti enam praeguses kontostruktuuris.</span><span class="sxs-lookup"><span data-stu-id="e358e-173">The beginning balances entries could include financial dimensions no longer in the current account structure and segment combinations that are no longer valid in the current account structure.</span></span> <span data-ttu-id="e358e-174">Kui teie organisatsioon soovib jaotamata kasumi algsaldo puhul finantsdimensiooni välja arvata, seadke finantsdimensioon valikule **Sule üksik** ja jätke dimensiooni väärtus tühjaks.</span><span class="sxs-lookup"><span data-stu-id="e358e-174">If your organization wants to exclude a financial dimension for the retained earning beginning balance, set the financial dimension to be **Close single** and leave the dimension value empty.</span></span>

## <a name="run-the-year-end-close-process"></a><span data-ttu-id="e358e-175">Aastalõpu sulgemisprotsessi käivitamine</span><span class="sxs-lookup"><span data-stu-id="e358e-175">Run the year-end close process</span></span>
<span data-ttu-id="e358e-176">Pärast aastalõpu sulgemismallide loomist käivitatakse aastalõpu sulgemisprotsess, valides tegumiribal suvandi **Käivita finantsaasta**.</span><span class="sxs-lookup"><span data-stu-id="e358e-176">After the year-end close templates are created, the year-end close process is initiated by choosing **Run fiscal year** on the Action Pane.</span></span> <span data-ttu-id="e358e-177">Valige mallilt kõik juriidilised isikud või nende alamkogum, mille puhul aastalõpu sulgemine käivitada.</span><span class="sxs-lookup"><span data-stu-id="e358e-177">Either select all or a subset of legal entities from the template for which to run the year-end close.</span></span> <span data-ttu-id="e358e-178">Finantsaastas esimest korda aastalõpu sulgemise käivitamisel valite tõenäoliselt kõik juriidilised isikud, et luua kõikide juriidiliste isikute jaoks algsaldod.</span><span class="sxs-lookup"><span data-stu-id="e358e-178">When running the year-end close for the first time in a fiscal year, you will likely choose all the legal entities to create beginning balances for all the legal entities.</span></span> <span data-ttu-id="e358e-179">Kui käivitate uuesti aastalõpu sulgemise, võite valida protsessi käivitamise ainult juriidilistele isikutele, kelle jaoks korrigeerivad kirjed sisestati.</span><span class="sxs-lookup"><span data-stu-id="e358e-179">If you're running the year-end close again, you may choose to run the process for only the legal entities for which adjusting entries were posted.</span></span> 

<span data-ttu-id="e358e-180">Valige finantsaasta, mille suhtes sooviksite käivitada aastalõpu sulgemisprotsessi.</span><span class="sxs-lookup"><span data-stu-id="e358e-180">Select the fiscal year that you would like to run the year end close process against.</span></span> <span data-ttu-id="e358e-181">Kui finantsdimensiooni viimase perioodi kohta on olemas rohkem kui üks sulgemisperiood, muutub väli **Perioodi nimi** kättesaadavaks, et saaksite valida, millisesse sulgemisperioodi sulgemiskanne sisestada, kui seadistus määratletakse sulgemiskande loomiseks.</span><span class="sxs-lookup"><span data-stu-id="e358e-181">If more than one closing period exists for the last period of the fiscal year, the **Period name** field will become available so you can select which closing period to post the Closing transaction, if setup is defined to create the Closing transaction.</span></span> 

<span data-ttu-id="e358e-182">Sisestage kandenumber, mis ei pruugi sõltuvalt pearaamatu parameetrite seadistusest olla vajalik.</span><span class="sxs-lookup"><span data-stu-id="e358e-182">Enter a voucher number, which or may not be required, depending on the setup in General ledger parameters.</span></span> <span data-ttu-id="e358e-183">Sama kandenumbrit kasutatakse kõikide aastalõpu sulgemisprotsessi jaoks valitud juriidiliste isikute puhul.</span><span class="sxs-lookup"><span data-stu-id="e358e-183">The same voucher number will be used for all the legal entities selected for the year end close process.</span></span> <span data-ttu-id="e358e-184">Kandenumbrit ei looda numbriseeriat kasutades.</span><span class="sxs-lookup"><span data-stu-id="e358e-184">The voucher number is not generated using a number sequence.</span></span> <span data-ttu-id="e358e-185">Kandenumber tuleks sisestada siis, kui see pole kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="e358e-185">It’s a best practice to enter a voucher number, even if it’s not required.</span></span> <span data-ttu-id="e358e-186">Kandenumbri sisestamine muudab lihtsaks avamiskande leidmise uuel finantsaastal.</span><span class="sxs-lookup"><span data-stu-id="e358e-186">Entering a voucher number makes it easier to find the Opening transaction in the new fiscal year.</span></span> <span data-ttu-id="e358e-187">Kui kandenumbrit ei sisestata, on kanne avamiskande puhul tühi.</span><span class="sxs-lookup"><span data-stu-id="e358e-187">If a voucher number isn’t entered, the voucher will be blank for the Opening transaction.</span></span> 

<span data-ttu-id="e358e-188">Kui sooviksite valitud finantsaasta puhul varasema aasta lõpu sulgemise ümber pöörata, seadke valik **Eelmise sulgemise tagasivõtmine** olekusse **Jah**.</span><span class="sxs-lookup"><span data-stu-id="e358e-188">If you would like to reverse a previous year end close for the selected fiscal year, set **Undo previous close** to **Yes**.</span></span> <span data-ttu-id="e358e-189">Aastalõpu sulgemine pööratakse ümber, kuid protsessi saab igal ajal uuesti käivitada.</span><span class="sxs-lookup"><span data-stu-id="e358e-189">The year-end close will be reversed, but the process can be rerun at any time.</span></span> <span data-ttu-id="e358e-190">Kui pöörate aastalõpu sulgemise ümber, siis pole valik **Viimase rahandusaasta sulgemise kuupäev** enam saadaval.</span><span class="sxs-lookup"><span data-stu-id="e358e-190">If you reverse a year-end close, the **Date of last year end close** will be unavailable.</span></span> 

<span data-ttu-id="e358e-191">Aastalõpu sulgemise protsess läheb vaikimisi pakktöötlusrežiimi.</span><span class="sxs-lookup"><span data-stu-id="e358e-191">The year-end close process defaults to run in batch mode.</span></span> <span data-ttu-id="e358e-192">Mõistlik on käivitada protsess pakktöötlusrežiimis, et lubada kasutajal naasta teiste tegevuste juurde.</span><span class="sxs-lookup"><span data-stu-id="e358e-192">It’s a best practice to run the process in batch mode, to allow the user to return to other activities.</span></span> <span data-ttu-id="e358e-193">Pärast aastalõpu sulgemisprotsessi lõpuleviimist värskendatakse valikut **Viimase rahandusaasta sulgemise kuupäev**.</span><span class="sxs-lookup"><span data-stu-id="e358e-193">After the year end close process is complete, the **Date of last year end close** will be updated with the session date.</span></span>

<span data-ttu-id="e358e-194">Lisateabe saamiseks vt [Pearaamatu sulgemine perioodi lõpus](close-general-ledger-at-period-end.md) ja [Rahandusaasta sulgemine](tasks/close-fiscal-year.md).</span><span class="sxs-lookup"><span data-stu-id="e358e-194">For more information, see [Close the general ledger at period end](close-general-ledger-at-period-end.md) and [Close the fiscal year](tasks/close-fiscal-year.md).</span></span>


