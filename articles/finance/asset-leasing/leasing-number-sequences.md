---
title: Numbriseeriate määramine
description: See teema selgitab, kuidas luua rendi ID-de jaoks numbriseeriaid. Lisaks selgitab see, kuidas luua ainulaadseid ID-sid, mida kasutatakse indeksi ümberhindamise protsessis.
author: moaamer
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: a0b5d622df1e5dcdf7f1322328bce7e185f8edb8
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819814"
---
# <a name="assign-number-sequences"></a><span data-ttu-id="72fe7-104">Numbriseeriate määramine</span><span class="sxs-lookup"><span data-stu-id="72fe7-104">Assign number sequences</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="72fe7-105">See teema selgitab, kuidas luua rendi ID-de jaoks numbriseeriaid.</span><span class="sxs-lookup"><span data-stu-id="72fe7-105">This topic explains how to create number sequences for lease IDs.</span></span> <span data-ttu-id="72fe7-106">Lisaks selgitab see, kuidas luua ainulaadseid ID-sid, mida kasutatakse indeksi ümberhindamise protsessis.</span><span class="sxs-lookup"><span data-stu-id="72fe7-106">It also explains how to create unique IDs that are used in the index revaluation process.</span></span>

1. <span data-ttu-id="72fe7-107">Avage **Vara rentimine \> Seadistus \> Vara rentimise parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="72fe7-107">Go to **Asset leasing \> Setup \> Asset leasing parameters**.</span></span>
2. <span data-ttu-id="72fe7-108">Valige külgmine vahekaart **Numbriseeriad**.</span><span class="sxs-lookup"><span data-stu-id="72fe7-108">Select the **Number sequences** side tab.</span></span>
3. <span data-ttu-id="72fe7-109">Valige külgmisel ribal **Numbriseeriad**.</span><span class="sxs-lookup"><span data-stu-id="72fe7-109">Select **Number sequences** in the side bar.</span></span>
4. <span data-ttu-id="72fe7-110">Valige viite **Rendi ID** jaoks numbriseeria.</span><span class="sxs-lookup"><span data-stu-id="72fe7-110">Select the number sequence for the **Lease ID** reference.</span></span> <span data-ttu-id="72fe7-111">Seda numbriseeriat kasutatakse iga rendi jaoks kordumatu ID loomiseks.</span><span class="sxs-lookup"><span data-stu-id="72fe7-111">This number sequence will be used to generate the unique identifier for each lease.</span></span>
5. <span data-ttu-id="72fe7-112">Valige viite **Protsessi ID** jaoks numbriseeria.</span><span class="sxs-lookup"><span data-stu-id="72fe7-112">Select the number sequence for the **Process ID** reference.</span></span> <span data-ttu-id="72fe7-113">Seda numbriseeriat kasutatakse iga indeksi uuesti hindamise protsessi jaoks kordumatu ID loomiseks.</span><span class="sxs-lookup"><span data-stu-id="72fe7-113">This number sequence will be used to generate the unique identifier for each index revaluation process.</span></span>
6. <span data-ttu-id="72fe7-114">Valige viite **Lõpetamispakkumise** jaoks numbriseeria.</span><span class="sxs-lookup"><span data-stu-id="72fe7-114">Select the number sequence for the **Termination Proposal ID** reference.</span></span> <span data-ttu-id="72fe7-115">Seda numbriseeriat kasutatakse iga lõpetamispakkumise jaoks kordumatu ID loomiseks.</span><span class="sxs-lookup"><span data-stu-id="72fe7-115">This number sequence will be used to generate the unique identifier for each termination proposal.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]