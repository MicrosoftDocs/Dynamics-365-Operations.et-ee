---
title: "Pearaamatu sulgemine perioodi lõpus"
description: "Selles teemas kirjeldatakse ülesandeid, mida tehakse tavaliselt pearaamatu puhul perioodi sulgemisel."
author: aprilolson
manager: AnnBe
ms.date: 08/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14111
ms.assetid: cec9e039-c1a2-482c-bea6-e11d896eea9d
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 16acadf0b814ff5863873280cd8d6e6ddbdcffc8
ms.contentlocale: et-ee
ms.lasthandoff: 08/29/2017

---

# <a name="close-the-general-ledger-at-period-end"></a><span data-ttu-id="eeab9-103">Pearaamatu sulgemine perioodi lõpus</span><span class="sxs-lookup"><span data-stu-id="eeab9-103">Close the general ledger at period end</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="eeab9-104">Selles teemas kirjeldatakse ülesandeid, mida tehakse tavaliselt pearaamatu puhul perioodi sulgemisel.</span><span class="sxs-lookup"><span data-stu-id="eeab9-104">This topic describes the tasks that are typically completed when performing a period closing for General ledger.</span></span> 

<span data-ttu-id="eeab9-105">Pearaamatus võite sulgemistoiminguid teha perioodi või aasta puhul.</span><span class="sxs-lookup"><span data-stu-id="eeab9-105">In General ledger, you can complete closing procedures for a period or a year.</span></span> <span data-ttu-id="eeab9-106">Sulgemisprotsessid valmistavad süsteemi uueks perioodiks ette.</span><span class="sxs-lookup"><span data-stu-id="eeab9-106">Closing processes prepare the system for a new period.</span></span> <span data-ttu-id="eeab9-107">Süsteemi uueks aastaks ettevalmistamiseks tuleb käivitada aastalõpu sulgemise protsess.</span><span class="sxs-lookup"><span data-stu-id="eeab9-107">To prepare the system for a new year, you must run the year end close process.</span></span> <span data-ttu-id="eeab9-108">Igal organisatsioonil on eri protsessid ja etapid, mida perioodi lõpus tehakse.</span><span class="sxs-lookup"><span data-stu-id="eeab9-108">Each organization has different processes and steps that it performs for the end of a period.</span></span> <span data-ttu-id="eeab9-109">Järgmiselt on toodud mõni valikuline etapp perioodi lõppude puhul.</span><span class="sxs-lookup"><span data-stu-id="eeab9-109">Here are some optional steps for period ends:</span></span>

-   <span data-ttu-id="eeab9-110">Lõpetage kõik ülesanded kõigis teistes moodulites, nagu Müügireskontro, Ostureskontro ja Varud.</span><span class="sxs-lookup"><span data-stu-id="eeab9-110">Complete all the tasks for all other modules, such as Accounts receivable, Accounts payable, and Inventory.</span></span>
-   <span data-ttu-id="eeab9-111">Veenduge, et kõik töölehed on sisestatud.</span><span class="sxs-lookup"><span data-stu-id="eeab9-111">Verify that all journals are posted.</span></span>
-   <span data-ttu-id="eeab9-112">Käivitage välisvaluuta ümberarvutamine realiseerimata kasumi või kahjumi summa loomiseks.</span><span class="sxs-lookup"><span data-stu-id="eeab9-112">Run foreign currency revaluation to generate any unrealized gain or loss amounts.</span></span>
-   <span data-ttu-id="eeab9-113">Tasakaalustage kõigi pearaamatukontode kanded.</span><span class="sxs-lookup"><span data-stu-id="eeab9-113">Settle transactions for each ledger account.</span></span>
-   <span data-ttu-id="eeab9-114">Töödelge nõutavaid eraldamisi.</span><span class="sxs-lookup"><span data-stu-id="eeab9-114">Process any required allocations.</span></span>
-   <span data-ttu-id="eeab9-115">Sisestage perioodi lõpu korrigeerimised käsitsi.</span><span class="sxs-lookup"><span data-stu-id="eeab9-115">Manually post period-end adjustments.</span></span>
-   <span data-ttu-id="eeab9-116">Paigutage kanded töölehele ja vaadake aruannet **Pearaamatu tööleht**.</span><span class="sxs-lookup"><span data-stu-id="eeab9-116">Journalize transactions, and review the **Ledger journal** report.</span></span>
-   <span data-ttu-id="eeab9-117">Konsolideerige, kasutades konsolideeritud ettevõtet või finantsaruandlust.</span><span class="sxs-lookup"><span data-stu-id="eeab9-117">Perform a consolidation by using a consolidation company or Financial reporting.</span></span>
-   <span data-ttu-id="eeab9-118">Looge finantsaruandlust kasutades perioodi lõpu finantsaruanded.</span><span class="sxs-lookup"><span data-stu-id="eeab9-118">Generate period-end financial statements by using Financial reporting.</span></span>
-   <span data-ttu-id="eeab9-119">Seadke pearaamatu perioodid suvandile **Ootel**, nii et sisestamist enam ei toimu.</span><span class="sxs-lookup"><span data-stu-id="eeab9-119">Set ledger periods to **On hold**, so that no further posting occurs.</span></span> <span data-ttu-id="eeab9-120">Saate paremaks kontrolliks piirata perioodi ka konkreetsele kasutajagrupile, kuni perioodi lõpu tegevused toimuvad.</span><span class="sxs-lookup"><span data-stu-id="eeab9-120">You can also restrict a period to a specific user group while period-end activities are occurring, for better control.</span></span> <span data-ttu-id="eeab9-121">Perioode pole soovitatav seada olekusse **Jäädavalt suletud**, kuna suletud perioodi ei saa uuesti avada.</span><span class="sxs-lookup"><span data-stu-id="eeab9-121">It's not a good idea to set periods to **Permanently closed**, because you can't reopen a period that has been closed.</span></span>

<span data-ttu-id="eeab9-122">Finantsperioodi sulgemise tööruumi abil saab korraldada ja jälgida erinevate perioodi lõpu protsesside puhul nõutavaid ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="eeab9-122">The Financial period close workspace can be used to organize and track the tasks required for various period end processes.</span></span> 


<span data-ttu-id="eeab9-123">Lisateavet saate lugeda järgmistest teemadest.</span><span class="sxs-lookup"><span data-stu-id="eeab9-123">For more information, see the following topics for more information:</span></span>
- [<span data-ttu-id="eeab9-124">Finantsperioodi sulgemise tööruum</span><span class="sxs-lookup"><span data-stu-id="eeab9-124">Financial period close workspace</span></span>](financial-period-close-workspace.md) 
- [<span data-ttu-id="eeab9-125">Aastalõpu sulgemine</span><span class="sxs-lookup"><span data-stu-id="eeab9-125">Year end close</span></span>](Year-end-close.md)  
- [<span data-ttu-id="eeab9-126">Finantsperioodi hulgisulgemine</span><span class="sxs-lookup"><span data-stu-id="eeab9-126">Mass financial period close</span></span>](tasks/mass-financial-period-close.md)





