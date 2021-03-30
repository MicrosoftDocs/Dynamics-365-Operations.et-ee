---
title: Igakuiste töölehe kannete loomine partiis
description: See teema selgitab, kuidas luua töölehe kandeid partiina, et aidata suurendada igakuiste rendikulude kirjendamisel tõhusust.
author: moaamer
manager: Ann Beebe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 6fd1815620095909e290fd03c404d964baa04a94
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/15/2021
ms.locfileid: "5241558"
---
# <a name="create-monthly-journal-entries-in-a-batch"></a><span data-ttu-id="60468-103">Igakuiste töölehe kannete loomine partiis</span><span class="sxs-lookup"><span data-stu-id="60468-103">Create monthly journal entries in a batch</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="60468-104">See teema selgitab, kuidas luua töölehe kandeid partiina, et aidata suurendada igakuiste rendikulude kirjendamisel tõhusust.</span><span class="sxs-lookup"><span data-stu-id="60468-104">This topic explains how to create journal entries in a batch to help increase efficiency when monthly lease expenses are recorded.</span></span> <span data-ttu-id="60468-105">Mitmest ajakavast pärinevate töölehtede kirjete loomiseks saab kasutada partiina töötlemist.</span><span class="sxs-lookup"><span data-stu-id="60468-105">Batch processing can be used to create journal entries from multiple schedules.</span></span> <span data-ttu-id="60468-106">Need töölehe kanded võivad sisaldada rendimakseid, kohustise amortiseerumist, kasutamisõiguse esemeks oleva vara amortiseerumist ja täitekulude kulusid.</span><span class="sxs-lookup"><span data-stu-id="60468-106">These journal entries can include lease payments, liability amortization, right-of-use (ROU) asset amortization, and executory cost expenses.</span></span> <span data-ttu-id="60468-107">Samuti saate kasutada partiina töötlemist, et teha samal ajal mitme rendikirje esialgne tuvastus või teha mitmele rendikirjele sama ajal ülemineku korrigeerimisi.</span><span class="sxs-lookup"><span data-stu-id="60468-107">You can also use batch processing to do the initial recognition of multiple leases at the same time, or to create transition adjustments for multiple leases at the same time.</span></span>

<span data-ttu-id="60468-108">Pakett-töö häälestamiseks või mitme rendikirje maksuarvete, kulumi või intressi töötlemiseks avage **Vara rentimine \> Perioodiline \> Töölehe partiina loomine**.</span><span class="sxs-lookup"><span data-stu-id="60468-108">To set up a batch job, or to process payment invoices, depreciation, or interest for multiple leases, go to **Asset leasing \> Periodic \> Batch journal creation**.</span></span> <span data-ttu-id="60468-109">Kuvatavas dialoogiboksis saate valida ajakava, mille põhjal töölehe kirjed luua.</span><span class="sxs-lookup"><span data-stu-id="60468-109">In the dialog box that appears, you can select the schedule that the journal entries should be created from.</span></span> <span data-ttu-id="60468-110">Samuti saate määrata, kas konkreetsete olemite, rendigruppide või rendi raamatute jaoks tuleks käitada protsessi partiina.</span><span class="sxs-lookup"><span data-stu-id="60468-110">You can also specify whether the batch process should be run for specific entities, lease groups, or lease books.</span></span>

> [!NOTE]
> <span data-ttu-id="60468-111">Järgmised kanded (nt kohustise amortiseerimise graafikud, maksed, kulum ja kulud) sisestatakse alles pärast seda, kui sisestatakse vastava rendikirje esialgne tuvastamine.</span><span class="sxs-lookup"><span data-stu-id="60468-111">Subsequent transactions, such as liability amortization schedules, payments, depreciation, and expenses, will be posted only after the initial recognition for corresponding leases is posted.</span></span>
>
> <span data-ttu-id="60468-112">Töölehe kirjed luuakse, kuid neid ei sisestata enne, kui valite käsu **Käivita**.</span><span class="sxs-lookup"><span data-stu-id="60468-112">The journal entries are created, but they won't be posted until you select the **Run** command.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]