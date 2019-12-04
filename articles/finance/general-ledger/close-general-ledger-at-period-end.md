---
title: Pearaamatu sulgemine perioodi lõpus
description: Selles teemas kirjeldatakse ülesandeid, mida tehakse tavaliselt pearaamatu puhul perioodi sulgemisel.
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerPeriodCloseWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5cabdce5e23704fbf12e631a138235174ebc5772
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770777"
---
# <a name="close-the-general-ledger-at-period-end"></a><span data-ttu-id="6e13e-103">Pearaamatu sulgemine perioodi lõpus</span><span class="sxs-lookup"><span data-stu-id="6e13e-103">Close the general ledger at period end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6e13e-104">Selles teemas kirjeldatakse ülesandeid, mida tehakse tavaliselt pearaamatu puhul perioodi sulgemisel.</span><span class="sxs-lookup"><span data-stu-id="6e13e-104">This topic describes the tasks that are typically completed when performing a period closing for General ledger.</span></span> 

<span data-ttu-id="6e13e-105">Pearaamatus võite sulgemistoiminguid teha perioodi või aasta puhul.</span><span class="sxs-lookup"><span data-stu-id="6e13e-105">In General ledger, you can complete closing procedures for a period or a year.</span></span> <span data-ttu-id="6e13e-106">Sulgemisprotsessid valmistavad süsteemi uueks perioodiks ette.</span><span class="sxs-lookup"><span data-stu-id="6e13e-106">Closing processes prepare the system for a new period.</span></span> <span data-ttu-id="6e13e-107">Süsteemi uueks aastaks ettevalmistamiseks tuleb käivitada aastalõpu sulgemise protsess.</span><span class="sxs-lookup"><span data-stu-id="6e13e-107">To prepare the system for a new year, you must run the year end close process.</span></span> <span data-ttu-id="6e13e-108">Igal organisatsioonil on eri protsessid ja etapid, mida perioodi lõpus tehakse.</span><span class="sxs-lookup"><span data-stu-id="6e13e-108">Each organization has different processes and steps that it performs for the end of a period.</span></span> <span data-ttu-id="6e13e-109">Järgmiselt on toodud mõni valikuline etapp perioodi lõppude puhul.</span><span class="sxs-lookup"><span data-stu-id="6e13e-109">Here are some optional steps for period ends:</span></span>

-   <span data-ttu-id="6e13e-110">Lõpetage kõik ülesanded kõigis teistes moodulites, nagu Müügireskontro, Ostureskontro ja Varud.</span><span class="sxs-lookup"><span data-stu-id="6e13e-110">Complete all the tasks for all other modules, such as Accounts receivable, Accounts payable, and Inventory.</span></span>
-   <span data-ttu-id="6e13e-111">Veenduge, et kõik töölehed on sisestatud.</span><span class="sxs-lookup"><span data-stu-id="6e13e-111">Verify that all journals are posted.</span></span>
-   <span data-ttu-id="6e13e-112">Käivitage välisvaluuta ümberarvutamine realiseerimata kasumi või kahjumi summa loomiseks.</span><span class="sxs-lookup"><span data-stu-id="6e13e-112">Run foreign currency revaluation to generate any unrealized gain or loss amounts.</span></span>
-   <span data-ttu-id="6e13e-113">Tasakaalustage kõigi pearaamatukontode kanded.</span><span class="sxs-lookup"><span data-stu-id="6e13e-113">Settle transactions for each ledger account.</span></span>
-   <span data-ttu-id="6e13e-114">Töödelge nõutavaid eraldamisi.</span><span class="sxs-lookup"><span data-stu-id="6e13e-114">Process any required allocations.</span></span>
-   <span data-ttu-id="6e13e-115">Sisestage perioodi lõpu korrigeerimised käsitsi.</span><span class="sxs-lookup"><span data-stu-id="6e13e-115">Manually post period-end adjustments.</span></span>
-   <span data-ttu-id="6e13e-116">Paigutage kanded töölehele ja vaadake aruannet **Pearaamatu tööleht**.</span><span class="sxs-lookup"><span data-stu-id="6e13e-116">Journalize transactions, and review the **Ledger journal** report.</span></span>
-   <span data-ttu-id="6e13e-117">Konsolideerige, kasutades konsolideeritud ettevõtet või finantsaruandlust.</span><span class="sxs-lookup"><span data-stu-id="6e13e-117">Perform a consolidation by using a consolidation company or Financial reporting.</span></span>
-   <span data-ttu-id="6e13e-118">Looge finantsaruandlust kasutades perioodi lõpu finantsaruanded.</span><span class="sxs-lookup"><span data-stu-id="6e13e-118">Generate period-end financial statements by using Financial reporting.</span></span>
-   <span data-ttu-id="6e13e-119">Seadke pearaamatu perioodid suvandile **Ootel**, nii et sisestamist enam ei toimu.</span><span class="sxs-lookup"><span data-stu-id="6e13e-119">Set ledger periods to **On hold**, so that no further posting occurs.</span></span> <span data-ttu-id="6e13e-120">Saate paremaks kontrolliks piirata perioodi ka konkreetsele kasutajagrupile, kuni perioodi lõpu tegevused toimuvad.</span><span class="sxs-lookup"><span data-stu-id="6e13e-120">You can also restrict a period to a specific user group while period-end activities are occurring, for better control.</span></span> <span data-ttu-id="6e13e-121">Perioode pole soovitatav seada olekusse **Jäädavalt suletud**, kuna suletud perioodi ei saa uuesti avada.</span><span class="sxs-lookup"><span data-stu-id="6e13e-121">It's not a good idea to set periods to **Permanently closed**, because you can't reopen a period that has been closed.</span></span>

<span data-ttu-id="6e13e-122">Finantsperioodi sulgemise tööruumi abil saab korraldada ja jälgida erinevate perioodi lõpu protsesside puhul nõutavaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="6e13e-122">The Financial period close workspace can be used to organize and track the tasks required for various period end processes.</span></span> 


<span data-ttu-id="6e13e-123">Lisateavet saate lugeda järgmistest teemadest.</span><span class="sxs-lookup"><span data-stu-id="6e13e-123">For more information, see the following topics for more information:</span></span>
- [<span data-ttu-id="6e13e-124">Finantsperioodi sulgemise tööruum</span><span class="sxs-lookup"><span data-stu-id="6e13e-124">Financial period close workspace</span></span>](financial-period-close-workspace.md) 
- [<span data-ttu-id="6e13e-125">Aastalõpu sulgemine</span><span class="sxs-lookup"><span data-stu-id="6e13e-125">Year-end close</span></span>](Year-end-close.md)  
- [<span data-ttu-id="6e13e-126">Finantsperioodi hulgisulgemine</span><span class="sxs-lookup"><span data-stu-id="6e13e-126">Mass financial period close</span></span>](tasks/mass-financial-period-close.md)




