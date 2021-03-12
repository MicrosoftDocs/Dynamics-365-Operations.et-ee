---
title: Sisestatud töölehekirjete töölehele paigutamine
description: See protseduur näitab, kuidas sisestatud töölehe kandeid töölehele paigutada.
author: aprilolson
manager: AnnBe
ms.date: 08/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, SysQueryForm
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ad18063e0a66a4aac0ebef7f0ce45c73137abcc7
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4968525"
---
# <a name="journalize-posted-journal-entries"></a><span data-ttu-id="d8938-103">Sisestatud töölehekirjete töölehele paigutamine</span><span class="sxs-lookup"><span data-stu-id="d8938-103">Journalize posted journal entries</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d8938-104">See protseduur näitab, kuidas sisestatud töölehe kandeid töölehele paigutada.</span><span class="sxs-lookup"><span data-stu-id="d8938-104">This procedure shows how to journalize posted journal entries.</span></span> <span data-ttu-id="d8938-105">Protseduur kasutab demoettevõtte USMF andmeid.</span><span class="sxs-lookup"><span data-stu-id="d8938-105">This procedure uses the USMF demo data company.</span></span>

1. <span data-ttu-id="d8938-106">Minge **navigeerimispaanil** jaotisesse **Moodulid > Pearaamat > Pearaamatu seadistamine > Pearaamatu parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="d8938-106">In the **Navigation pane**, go to **Modules > General ledger > Ledger setup > General ledger parameters**.</span></span>
2. <span data-ttu-id="d8938-107">Välja **Laiendatud pearaamatu leht** väärtuseks saab seada Jah või Ei.</span><span class="sxs-lookup"><span data-stu-id="d8938-107">The **Extended ledger journal** field can be set to Yes or No.</span></span> <span data-ttu-id="d8938-108">Kui see on Jah, on aruande väljund teistsugune.</span><span class="sxs-lookup"><span data-stu-id="d8938-108">If Yes, the report output will be different.</span></span>
3. <span data-ttu-id="d8938-109">Valige, kas perioodi saab sulgeda, kui töölehele paigutamise protsessi pole käivitatud.</span><span class="sxs-lookup"><span data-stu-id="d8938-109">Select whether the period can be closed if the journalizing process hasn't been run.</span></span> <span data-ttu-id="d8938-110">Kui selle suvandi säte on Jah, ei saa perioodi sulgeda enne, kui selle perioodi puhul on töölehele paigutamise protsess lõpule viidud.</span><span class="sxs-lookup"><span data-stu-id="d8938-110">If this option is set to Yes, the period cannot be closed until the journalizing process has been completed for that period.</span></span>  
4. <span data-ttu-id="d8938-111">Sulgege leht.</span><span class="sxs-lookup"><span data-stu-id="d8938-111">Close the page.</span></span>
5. <span data-ttu-id="d8938-112">Paanil **Navigeerimispaan** avage **Moodulid > Pearaamat > Perioodilised ülesanded > Töölehele kandmine**.</span><span class="sxs-lookup"><span data-stu-id="d8938-112">In the **Navigation pane**, go to **Modules > General ledger > Periodic tasks > Journalizing**.</span></span>
6. <span data-ttu-id="d8938-113">Klõpsake käsku **Filtreeri**.</span><span class="sxs-lookup"><span data-stu-id="d8938-113">Click **Filter**.</span></span>
7. <span data-ttu-id="d8938-114">Tõstke esile rida, mille filtri kriteeriume soovite määratleda.</span><span class="sxs-lookup"><span data-stu-id="d8938-114">Highlight the row with the filter criteria that you want to define.</span></span>
8. <span data-ttu-id="d8938-115">Väljal **Kriteeriumid** sisestage või valige filtrikriteeriumid.</span><span class="sxs-lookup"><span data-stu-id="d8938-115">In the **Criteria** field, enter or select the filter criteria..</span></span>
9. <span data-ttu-id="d8938-116">Klõpsake **OK**, et sulgeda filtrileht.</span><span class="sxs-lookup"><span data-stu-id="d8938-116">Click **OK** to close the filter page.</span></span>
10. <span data-ttu-id="d8938-117">Klõpsake **OK**, et alustada töölehele kandmist.</span><span class="sxs-lookup"><span data-stu-id="d8938-117">Click **OK** to start the journalizing process.</span></span> <span data-ttu-id="d8938-118">Pärast protsessi lõpetamist koostatakse aruanne.</span><span class="sxs-lookup"><span data-stu-id="d8938-118">A report will be generated after the process is complete.</span></span>  

