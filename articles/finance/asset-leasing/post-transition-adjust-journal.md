---
title: Ülemineku korrigeerimise töölehe kannete sisestamine jaotisse vara rentimine
description: Selles teemas kirjeldatakse funktsiooni, mis võimaldab teil rendiportfelli üle viia uutele rentimise raamatupidamisstandarditele, raamatupidamisstandardite kodeerimise teemale 842 (ASC 842) ja rahvusvahelise finantsaruandluse standardile 16 (IFRS 16).
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
ms.openlocfilehash: ea61a0d6e30695a2ef6b93529fcf3d21882c9cd2
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5819766"
---
# <a name="post-transition-adjustment-journal-entries-in-asset-leasing"></a><span data-ttu-id="ef6b8-103">Ülemineku korrigeerimise töölehe kannete sisestamine jaotisse vara rentimine</span><span class="sxs-lookup"><span data-stu-id="ef6b8-103">Post transition adjustment journal entries in Asset leasing</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ef6b8-104">Selles teemas kirjeldatakse funktsiooni, mis võimaldab teil rendiportfelli üle viia uutele rentimise raamatupidamisstandarditele: raamatupidamise standardite kodeerimise teema 842 (ASC 842), mis on üldtunnustatud raamatupidamispõhimõtete standard USA-s (USA RAAMATUPIDAMISTAVA) ja rahvusvahelise finantsaruandluse Standard 16 (IFRS 16).</span><span class="sxs-lookup"><span data-stu-id="ef6b8-104">This topic describes the functionality that lets you transition a lease portfolio to the new lease accounting standards: Accounting Standards Codification Topic 842 (ASC 842), which is the standard in Generally Accepted Accounting Principles in the US (US GAAP), and International Financial Reporting Standard 16 (IFRS 16).</span></span>

<span data-ttu-id="ef6b8-105">Lisateavet selle kohta, kuidas seadistada raamat uuele standardile üleminekuks, leiate teemast [Rendiraamatute seadistamine](set-up-lease-books.md).</span><span class="sxs-lookup"><span data-stu-id="ef6b8-105">For information about how to set up a book for the transition to the new standards, see [Set up lease books](set-up-lease-books.md).</span></span>

<span data-ttu-id="ef6b8-106">Ülemineku korrigeerimise töölehe kirje loomisel luuakse töölehe kirje.</span><span class="sxs-lookup"><span data-stu-id="ef6b8-106">When you create a transition adjustment journal entry, a journal entry is generated.</span></span> <span data-ttu-id="ef6b8-107">See kirje kajastab bilansi mõju sellel kuupäeval rendi uutele standarditele üleviimisele.</span><span class="sxs-lookup"><span data-stu-id="ef6b8-107">This entry reflects the balance sheet impact of recording the lease under the new standards on that date.</span></span> <span data-ttu-id="ef6b8-108">Vastav vara konto debiteeritakse sellel kuupäeval bilansilise väärtuse summas ja kohustise konto krediteeritakse.</span><span class="sxs-lookup"><span data-stu-id="ef6b8-108">The appropriate asset account is debited for the carrying amount on that date, and the liability account is credited.</span></span> <span data-ttu-id="ef6b8-109">Erinevused debiteeritakse või krediteeritakse jaotamata kasumile.</span><span class="sxs-lookup"><span data-stu-id="ef6b8-109">The difference is either debited or credited to retained earnings.</span></span>

<span data-ttu-id="ef6b8-110">Ülemineku korrigeerimise sisestamiseks uute raamatupidamisstandardite järgi toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="ef6b8-110">To post a transition adjustment in compliance with the new accounting standards, follow these steps.</span></span>

1. <span data-ttu-id="ef6b8-111">Valige lehel **Rendi kokkuvõte** rendikirje ja seejärel valige **Raamatud**.</span><span class="sxs-lookup"><span data-stu-id="ef6b8-111">On the **Lease summary** page, select the lease, and then select **Books**.</span></span>
2. <span data-ttu-id="ef6b8-112">Valige raamatust **Maksegraafik**.</span><span class="sxs-lookup"><span data-stu-id="ef6b8-112">In the book, select **Payment schedule**.</span></span>
3. <span data-ttu-id="ef6b8-113">Valige **Maksegraafiku** dialoogiaknast käsk **Kinnita**.</span><span class="sxs-lookup"><span data-stu-id="ef6b8-113">In the **Payment schedule** dialog box, select **Confirm**.</span></span> <span data-ttu-id="ef6b8-114">Seejärel sulgege dialoogiboks.</span><span class="sxs-lookup"><span data-stu-id="ef6b8-114">Then close the dialog box.</span></span>
4. <span data-ttu-id="ef6b8-115">Valige **Ülemineku korrigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="ef6b8-115">Select **Transition adjustment**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="ef6b8-116">Ülemineku korrigeerimise saab luua ainult nende rendiraamatute jaoks, mis on määratud raamatule, kus väli **Raamatu üleviimine** on saadaval.</span><span class="sxs-lookup"><span data-stu-id="ef6b8-116">A transition adjustment can be created only for lease books that are assigned to a book where the **Transition book** field is available.</span></span> <span data-ttu-id="ef6b8-117">Kui väärtus väljal **Rendi algus** on hilisem kui ülemineku kuupäev, uuendata väärtust väljal **Ülemineku korrigeerimine**.</span><span class="sxs-lookup"><span data-stu-id="ef6b8-117">If the value in the **Lease commencement** field is later than the transition date, the value in the **Transition adjustment** field won't be updated.</span></span>

5. <span data-ttu-id="ef6b8-118">Töölehe kirje vaatamiseks valige **Vara rentimise töölehed**.</span><span class="sxs-lookup"><span data-stu-id="ef6b8-118">To view the journal entry, select **Asset leasing journals**.</span></span>
6. <span data-ttu-id="ef6b8-119">Valige uus tööleht ja seejärel valige käsk **Sisesta**.</span><span class="sxs-lookup"><span data-stu-id="ef6b8-119">Select the new journal, and then select **Post**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]