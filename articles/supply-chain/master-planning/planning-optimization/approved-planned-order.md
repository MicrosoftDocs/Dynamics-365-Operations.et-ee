---
title: Plaanitud tellimuste kinnitamine
description: Selles teemas kirjeldatakse plaaneerimise optimeerimise korral toetatud plaanitud tellimuste kinnitamist.
author: ChristianRytt
manager: tfehr
ms.date: 08/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-08-21
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: c29ede7ad8916a97b4a04b68f41961f79810e0c8
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983565"
---
# <a name="approve-planned-orders"></a><span data-ttu-id="198b7-103">Plaanitud tellimuste kinnitamine</span><span class="sxs-lookup"><span data-stu-id="198b7-103">Approve planned orders</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="198b7-104">See kirjeldab, kuidas planeerimise optimeerimise korral värskendada plaanitud tellimuste olekut.</span><span class="sxs-lookup"><span data-stu-id="198b7-104">This topic provides information about how to update the status of planned orders in Planning Optimization.</span></span>

<span data-ttu-id="198b7-105">Pidage meeles, et plaanitud tellimuste kinnitamine on valikuline etapp plaanitud tellimuse kinnitatud tellimuseks muutmisel.</span><span class="sxs-lookup"><span data-stu-id="198b7-105">Note that approval of planned orders is an optional step, on the way to create a firmed order from a planned order.</span></span> <span data-ttu-id="198b7-106">Soovitatav on kinnitada muudetud plaanitud tellimused, vastasel juhul ignoreeritakse muudatusi ja need kirjutatakse üle järgmise plaanimise käitamisel.</span><span class="sxs-lookup"><span data-stu-id="198b7-106">It is recommended to approve modified planned orders, otherwise the edits will be ignored and overwritten by the next planning run.</span></span>

![Plaanitud tellimuse voog](media/approved-planned-orders-1.png)

<span data-ttu-id="198b7-108">Väli **Olek** aitab teil jälgida edenemist järgmiste väärtuste abil.</span><span class="sxs-lookup"><span data-stu-id="198b7-108">The **Status** field helps you tack your progress using the following values:</span></span>

- <span data-ttu-id="198b7-109">**Töötlemata:** kui koondplaneerimine loob plaanitud tellimused, on nende olek *Töötlemata*.</span><span class="sxs-lookup"><span data-stu-id="198b7-109">**Unprocessed:** When master planning generates planned orders, the planned orders have a status of *Unprocessed*.</span></span> <span data-ttu-id="198b7-110">Selle olekuga plaanitud tellimused kustutatakse järgmise plaanimise käitamisel.</span><span class="sxs-lookup"><span data-stu-id="198b7-110">Planned orders with this status will be deleted during the next planning run.</span></span>
- <span data-ttu-id="198b7-111">**Lõpetatud:** kui otsustate plaanitud tellimust mitte kinnitada, saate muuta oleku *Lõpetatuks*, mis näitab, et olete selle plaanitud tellimuse hindamise lõpule viinud.</span><span class="sxs-lookup"><span data-stu-id="198b7-111">**Completed:** If you decide not to firm a planned order, you can change the status to *Completed* to indicate that you completed evaluating this planned order.</span></span> <span data-ttu-id="198b7-112">Pange tähele, et süsteem käsitleb olekut *Töötlemata* ja *Lõpetatud* sama moodi.</span><span class="sxs-lookup"><span data-stu-id="198b7-112">Note that a status of *Unprocessed* and *Completed* are treated the same by the system.</span></span>
- <span data-ttu-id="198b7-113">**Kinnitatud:** kui soovite muudatusi säilitada või plaanitud tellimuse kinnitada, muutke olekuks *Kinnitatud*.</span><span class="sxs-lookup"><span data-stu-id="198b7-113">**Approved:** If you want to keep edits or are planning to firm a planned order, change the status to *Approved*.</span></span> <span data-ttu-id="198b7-114">Olekuga *Kinnitatud* plaanitud tellimusi käsitletakse koondplaneerimisel fikseeritult ja eeldatavalt tarnitavatena, nii et neid ei muudeta ega kustutata hilisema koondplaneerimise käivitamiste ajal.</span><span class="sxs-lookup"><span data-stu-id="198b7-114">Planned orders with *Approved* status are considered as fixed and expected supply by master planning, so they are not modified or deleted during later master planning runs.</span></span> <span data-ttu-id="198b7-115">Selle saavutamiseks kopeerib planeerimisloogika koondplaneerimise ajal *kinnitatud* plaanitud tellimused vana plaani versioonist uude plaani versiooni.</span><span class="sxs-lookup"><span data-stu-id="198b7-115">To achieve this, the planning logic copies the *Approved* planned orders from the old plan version to the new plan version during master planning.</span></span> <span data-ttu-id="198b7-116">Pange tähele, et *Kinnitatud* plaanitud tellimusi loetakse tarnitavateks ainult konkreetse koondplaani korral.</span><span class="sxs-lookup"><span data-stu-id="198b7-116">Note that *Approved* planned orders are only considered supply within the specific master plan.</span></span>

<span data-ttu-id="198b7-117">Saate planeeritud tellimusi hallata tööruumis **Koondplaneerimine**, loendis **Plaanitud tellimus** või loendites **Plaanitud tootmistellimused**, **Plaanitud ostutellimused** ja **Plaanitud üleviimised**.</span><span class="sxs-lookup"><span data-stu-id="198b7-117">You can manage planned orders from the  **Master planning**  workspace, the  **Planned order**  list, or the  **Planned production orders**,  **Planned purchase orders**, and  **Planned transfer**  lists.</span></span>
