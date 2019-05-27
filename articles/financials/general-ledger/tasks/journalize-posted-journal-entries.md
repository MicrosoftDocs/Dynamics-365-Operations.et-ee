---
title: Sisestatud töölehekirjete töölehele paigutamine
description: See protseduur näitab, kuidas sisestatud töölehe kandeid töölehele paigutada.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b50809cf9eb59475856f91d9f1ddfe28ecfd8de6
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547906"
---
# <a name="journalize-posted-journal-entries"></a><span data-ttu-id="e4324-103">Sisestatud töölehekirjete töölehele paigutamine</span><span class="sxs-lookup"><span data-stu-id="e4324-103">Journalize posted journal entries</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e4324-104">See protseduur näitab, kuidas sisestatud töölehe kandeid töölehele paigutada.</span><span class="sxs-lookup"><span data-stu-id="e4324-104">This procedure shows how to journalize posted journal entries.</span></span> <span data-ttu-id="e4324-105">Protseduur kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="e4324-105">This procedure uses the USMF demo data company.</span></span>

1. <span data-ttu-id="e4324-106">Kontrollige töölehele paigutamise sätteid jaotises Pearaamat > Pearaamatu seadistamine > Pearaamatu parameetrid.</span><span class="sxs-lookup"><span data-stu-id="e4324-106">Validate the settings for journalizing under General ledger > Ledger setup > General ledger parameters.</span></span>
2. <span data-ttu-id="e4324-107">Välja Laiendatud pearaamatu tööleht sätteks võib määrata Jah või Ei.</span><span class="sxs-lookup"><span data-stu-id="e4324-107">The Extended ledger journal field can be set to Yes or No.</span></span> <span data-ttu-id="e4324-108">Kui see on Jah, on aruande väljund teistsugune.</span><span class="sxs-lookup"><span data-stu-id="e4324-108">If Yes, the report output will be different.</span></span>
3. <span data-ttu-id="e4324-109">Valige, kas perioodi saab sulgeda, kui töölehele paigutamise protsessi pole käivitatud.</span><span class="sxs-lookup"><span data-stu-id="e4324-109">Select whether the period can be closed if the journalizing process hasn't been run.</span></span>
    * <span data-ttu-id="e4324-110">Kui selle suvandi säte on Jah, ei saa perioodi sulgeda enne, kui selle perioodi puhul on töölehele paigutamise protsess lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="e4324-110">If this option is set to Yes, the period cannot be closed until the journalizing process has been completed for that period.</span></span>  
4. <span data-ttu-id="e4324-111">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="e4324-111">Close the page.</span></span>
5. <span data-ttu-id="e4324-112">Minge jaotisse Pearaamat > Perioodilised ülesanded > Töölehele paigutamine.</span><span class="sxs-lookup"><span data-stu-id="e4324-112">Go to General ledger > Periodic tasks > Journalizing.</span></span>
6. <span data-ttu-id="e4324-113">Klõpsake käsku Filtreeri.</span><span class="sxs-lookup"><span data-stu-id="e4324-113">Click Filter.</span></span>
7. <span data-ttu-id="e4324-114">Tõstke esile rida, mille filtri kriteeriume soovite määratleda.</span><span class="sxs-lookup"><span data-stu-id="e4324-114">Highlight the row with the filter criteria that you want to define.</span></span>
8. <span data-ttu-id="e4324-115">Sisestage või valige filtri kriteeriumid väljal Kriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="e4324-115">In the Criteria field, enter or select the filter criteria..</span></span>
9. <span data-ttu-id="e4324-116">Klõpsake filtri lehe sulgemiseks nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e4324-116">Click OK to close the filter page.</span></span>
10. <span data-ttu-id="e4324-117">Klõpsake töölehele paigutamise protsessi käivitamiseks nuppu OK.</span><span class="sxs-lookup"><span data-stu-id="e4324-117">Click OK to start the journalizing process.</span></span>
    * <span data-ttu-id="e4324-118">Pärast protsessi lõpetamist koostatakse aruanne.</span><span class="sxs-lookup"><span data-stu-id="e4324-118">A report will be generated after the process is complete.</span></span>  

