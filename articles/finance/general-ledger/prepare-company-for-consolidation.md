---
title: Juriidilise isiku ettevalmistamine konsolideerimisprotsessiks
description: Konsolideerimise ajal kogute kanded mitmetelt juriidiliste isikute kontokomplektidelt ühte juriidilise isiku kontokomplekti. Selles teemas kirjeldatakse, kuidas juriidilist isikut konsolideerimiseks ette valmistada.
author: jinniew
manager: AnnBe
ms.date: 10/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: jiwo
ms.search.validFrom: 2018-10-30
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: 07988e71276c6439e392bce2087f3a8923f5f40b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5230198"
---
# <a name="prepare-a-legal-entity-for-the-consolidation-process"></a><span data-ttu-id="4a515-104">Juriidilise isiku ettevalmistamine konsolideerimisprotsessiks</span><span class="sxs-lookup"><span data-stu-id="4a515-104">Prepare a legal entity for the consolidation process</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4a515-105">Konsolideerimise ajal kogute kanded mitmetelt juriidiliste isikute kontokomplektidelt ühte juriidilise isiku kontokomplekti.</span><span class="sxs-lookup"><span data-stu-id="4a515-105">During a consolidation, you gather transactions from several sets of legal entity accounts into a single set of legal entity accounts.</span></span> <span data-ttu-id="4a515-106">Selles teemas kirjeldatakse, kuidas juriidilist isikut konsolideerimiseks ette valmistada.</span><span class="sxs-lookup"><span data-stu-id="4a515-106">This topic explains how to prepare a legal entity for a consolidation.</span></span>

> [!NOTE]
> <span data-ttu-id="4a515-107">Soovitame teil kasutada rakenduse Microsoft Dynamics 365 Finance Management Reporterit, et kombineerida finantstulemused mitme juriidilise isiku jaoks konsolideeritud vormingus.</span><span class="sxs-lookup"><span data-stu-id="4a515-107">We recommend that you use Management Reporter for Microsoft Dynamics 365 Finance to combine the financial results for multiple legal entities in a consolidated format.</span></span> <span data-ttu-id="4a515-108">Management Reporter võimaldab luua konsolideeritud finantsaruandeid juriidiliste isikute lõikes, kasutada Excelit konsolideerimise andmete importimiseks teistest allikatest ja teisendada summad mis tahes arvuks aruandlusvaluutadeks ilma, et konsolideerimisprotsessi oleks vaja rakenduses Dynamics 365 Finance käivitada.</span><span class="sxs-lookup"><span data-stu-id="4a515-108">Management Reporter lets you create consolidated financial reports across legal entities, use Excel to import consolidation data from other sources, and translate amounts into any number of reporting currencies without having to run the consolidation process in Dynamics 365 Finance.</span></span>

<span data-ttu-id="4a515-109">Saate konsolideeritud juriidiliselt isikult aruandeid (nt finantsaruandeid) printida.</span><span class="sxs-lookup"><span data-stu-id="4a515-109">You can print reports, such as financial statements, from the consolidated legal entity.</span></span> <span data-ttu-id="4a515-110">Kuid te ei saa igapäevasteks kanneteks kasutada konsolideeritud juriidilist isikut.</span><span class="sxs-lookup"><span data-stu-id="4a515-110">However, you can't use the consolidated legal entity for daily transactions.</span></span>

<span data-ttu-id="4a515-111">Saate konsolideerida andmeid juriidilistelt isikutelt, mis kasutavad konsolideeritud juriidilise isiku andmebaasist erinevaid andmebaase.</span><span class="sxs-lookup"><span data-stu-id="4a515-111">You can consolidate data from legal entities that use different databases than the consolidated legal entity.</span></span> <span data-ttu-id="4a515-112">Sellele konsolideerimisprotsessile viidatakse kui *impordi konsolideerimisele*.</span><span class="sxs-lookup"><span data-stu-id="4a515-112">This consolidation process is referred to as an *import consolidation*.</span></span> <span data-ttu-id="4a515-113">Teise võimalusena saavad juriidilised isikud kasutada konsolideeritud juriidilise isikuga sama andmebaasi.</span><span class="sxs-lookup"><span data-stu-id="4a515-113">Alternatively, the legal entities can use the same database as the consolidated legal entity.</span></span> <span data-ttu-id="4a515-114">Sellele konsolideerimisprotsessile viidatakse kui *võrgus konsolideerimisele*.</span><span class="sxs-lookup"><span data-stu-id="4a515-114">This consolidation process is referred to as an *online consolidation*.</span></span>

<span data-ttu-id="4a515-115">Konsolideeritud juriidiline isik kogub tütarettevõtete tulemusi ja saldosid.</span><span class="sxs-lookup"><span data-stu-id="4a515-115">The consolidated legal entity collects the results and balances of the subsidiaries.</span></span> <span data-ttu-id="4a515-116">Konsolideeritud juriidilise isiku konsolideerimiseks ettevalmistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="4a515-116">To prepare a consolidated legal entity for a consolidation, follow these steps.</span></span>

1. <span data-ttu-id="4a515-117">Avage **Pearaamat \> Seadistus \> Organisatsioon \> Juriidilised isikud**.</span><span class="sxs-lookup"><span data-stu-id="4a515-117">Go to **General ledger \> Setup \> Organization \> Legal entities**.</span></span>
2. <span data-ttu-id="4a515-118">Valige **Uus**, et luua uus juriidiline isik, mis on konsolideeritud juriidiline isik.</span><span class="sxs-lookup"><span data-stu-id="4a515-118">Select **New** to create the legal entity that will be the consolidated legal entity.</span></span>
3. <span data-ttu-id="4a515-119">Valige märkeruut **Kasuta finantskonsolideeritmise protsessi** ja seejärel sisestage teave konsolideeritud juriidilise isiku kohta.</span><span class="sxs-lookup"><span data-stu-id="4a515-119">Select the **Use for financial consolidation process** check box, and then enter information about the consolidated legal entity.</span></span> <span data-ttu-id="4a515-120">Sisestage kindlasti see teave täpselt nii, nagu soovite seda konsolideeritud juriidilise isiku finantsaruandes näha.</span><span class="sxs-lookup"><span data-stu-id="4a515-120">Be sure to enter this information exactly as you want it to appear on financial statements for the consolidated legal entity.</span></span>
4. <span data-ttu-id="4a515-121">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="4a515-121">Close the page.</span></span>
5. <span data-ttu-id="4a515-122">Valige lehe ülemise parempoolse nurga väljal konsolideeritud juriidiline isik ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="4a515-122">Select the consolidated legal entity in the field in the upper-right corner of the page, and then select **OK**.</span></span>
6. <span data-ttu-id="4a515-123">Avage **Pearaamat \> Seadistus \> Pearaamat**.</span><span class="sxs-lookup"><span data-stu-id="4a515-123">Go to **General ledger \> Setup \> Ledger**.</span></span>
7. <span data-ttu-id="4a515-124">Valige konsolideeritud juriidilisele isikule kontoplaan, rahanduskalender, arvestusvaluuta, valikuline aruandlusvaluuta ja vahetuskursi vaiketüüp.</span><span class="sxs-lookup"><span data-stu-id="4a515-124">Select the chart of accounts, the fiscal calendar, the accounting currency, an optional reporting currency, and the default type of exchange rate for the consolidated legal entity.</span></span> 
8. <span data-ttu-id="4a515-125">Avage **Pearaamat \> Seadistus \> Valuuta \> Valuuta vahetuskursi määrad**.</span><span class="sxs-lookup"><span data-stu-id="4a515-125">Go to **General ledger \> Setup \> Currency \> Currency exchange rates**.</span></span>
9. <span data-ttu-id="4a515-126">Seadistage tütarettevõttena tegutsevate juriidiliste isikute valuutadele valuutavahetuskursid asjakohasteks perioodideks.</span><span class="sxs-lookup"><span data-stu-id="4a515-126">Set up currency exchange rates in relevant periods for the currencies of the subsidiary legal entities.</span></span>
10. <span data-ttu-id="4a515-127">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="4a515-127">Close the page.</span></span>
11. <span data-ttu-id="4a515-128">Kui konsolideeritud juriidilisel isikul on tütarettevõtteid, mis kasutavad välisvaluutat, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="4a515-128">If the consolidated legal entity has subsidiaries that use foreign currencies, follow these steps:</span></span>

    1. <span data-ttu-id="4a515-129">Avage **Pearaamat \> Seadistus \> Sisestamine \> Kontod automaatseteks kanneteks**.</span><span class="sxs-lookup"><span data-stu-id="4a515-129">Go to **General ledger \> Setup \> Posting \> Accounts for automatic transactions**.</span></span>
    2. <span data-ttu-id="4a515-130">Valige väljal **Sisestamise tüüp** sobiv konto.</span><span class="sxs-lookup"><span data-stu-id="4a515-130">In the **Posting type** field, select an appropriate account:</span></span>

        - <span data-ttu-id="4a515-131">Kui juriidilisel isikul on välismaiseid tütarettevõtteid, mis on finantsiliselt või tegevusliselt emaettevõtte juriidilise isikuga vastastikku sõltuvad, valige sobiv konto sisestustüübile **Kasum ja kahjum erinevuste sisestamiseks konsolideeritud**.</span><span class="sxs-lookup"><span data-stu-id="4a515-131">If the legal entity has foreign subsidiaries that are financially or operationally interdependent with the parent legal entity, select an appropriate account for the **Profit and loss account for consolidation differences** posting type.</span></span>
        - <span data-ttu-id="4a515-132">Kui konsolideerite tütarettevõtte, mis on rahaliselt ja juhtimiselt emaüksuse juriidilisest isikust sõltumatu, või juriidilise isiku, mis hõlmab tulemusi mitmelt tütarettevõttelt, mis on rahaliselt ja juhtimiselt peamisest juriidilisest isikust sõltumatu, ja kui kasutate andmete konsolideerimiseks teisendamismeetodeid, valige sisestamise tüübile **Konsolideerimiserinevuste saldo konto** sobiv konto.</span><span class="sxs-lookup"><span data-stu-id="4a515-132">If you're consolidating a subsidiary that is financially and operationally independent of the parent legal entity, or a legal entity that contains the results of several subsidiaries that are financially and operationally independent of the parent legal entity, and if you're using translation methods to consolidate the data, select an appropriate account for the **Balance account for consolidation differences** posting type.</span></span>

    3. <span data-ttu-id="4a515-133">Valige väljal **Põhikonto** need põhikontod mida kasutatakse välisvaluuta ümberarvutamise korrigeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="4a515-133">In the **Main account** field, select the main accounts that should be used for foreign currency revaluation adjustments.</span></span>
    4. <span data-ttu-id="4a515-134">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="4a515-134">Close the page.</span></span>

    <span data-ttu-id="4a515-135">Kui loote konsolideeritud juriidilise isiku perioodi alguses, saate välisvaluuta summad ümber arvutada vastavalt sellele, kuidas vahetuskursid konsolideerimisperioodi jooksul muutuvad.</span><span class="sxs-lookup"><span data-stu-id="4a515-135">If you create the consolidated legal entity early in a period, you can revalue foreign currency amounts as exchange rates change during the consolidation period.</span></span>

<span data-ttu-id="4a515-136">Konsolideeritud juriidiline isik on nüüd perioodilise töö **Konsolideerimise** jaoks seadistatud.</span><span class="sxs-lookup"><span data-stu-id="4a515-136">The consolidated legal entity is now set up for the **Consolidate** periodic job.</span></span> <span data-ttu-id="4a515-137">Saate teha kas impordi konsolideerimist või võrgukonsolideerimisi.</span><span class="sxs-lookup"><span data-stu-id="4a515-137">You can do either an import consolidation or an online consolidation.</span></span>

- <span data-ttu-id="4a515-138">Konsolideerimise importimiseks avage **Pearaamat \> Perioodiline \> Konsolideeri \> Konsolideeri \[Impordi asukohast\]**.</span><span class="sxs-lookup"><span data-stu-id="4a515-138">To do an import consolidation, go to **General ledger \> Periodic \> Consolidate \> Consolidate \[Import from\]**.</span></span>
- <span data-ttu-id="4a515-139">Veebipõhise konsolideerimise importimiseks avage **Pearaamat \> Perioodiline \> Konsolideeri \> Konsolideeri \[Veebis\]**.</span><span class="sxs-lookup"><span data-stu-id="4a515-139">To do an online consolidation, go to **General ledger \> Periodic \> Consolidate \> Consolidate \[Online\]**.</span></span>

> [!NOTE]
> <span data-ttu-id="4a515-140">Enne konsolideerimist valmistage tütarettevõtte juriidilised isikud konsolideerimiseks ette.</span><span class="sxs-lookup"><span data-stu-id="4a515-140">Before you can process the consolidation, you must prepare the subsidiary legal entities for consolidation.</span></span> <span data-ttu-id="4a515-141">Lisateavet vt jaotisest [Allettevõte juriidilise isiku konsolideerimiseks seadistamine](set-up-subsidiary-company-for-consolidation.md).</span><span class="sxs-lookup"><span data-stu-id="4a515-141">For more information, see [Set up a subsidiary legal entity for consolidation](set-up-subsidiary-company-for-consolidation.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]