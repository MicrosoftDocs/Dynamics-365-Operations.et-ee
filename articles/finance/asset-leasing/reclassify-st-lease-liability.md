---
title: Rendikohustise lühiajalise osa ümberklassifitseerimine
description: Selles teemas selgitatakse, kuidas luua igakuise töölehe kirjet, rendikohustise osa lühiajaliseks ümberklassifitseerimiseks.
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
ms.openlocfilehash: 08ca824bb4c4a02a80f2187fb5f8fe4e8b7327c9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4992910"
---
# <a name="reclassify-the-short-term-portion-of-lease-liability"></a><span data-ttu-id="51bf7-103">Rendikohustise lühiajalise osa ümberklassifitseerimine</span><span class="sxs-lookup"><span data-stu-id="51bf7-103">Reclassify the short-term portion of lease liability</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="51bf7-104">Selles teemas selgitatakse, kuidas luua igakuise töölehe kirjet, rendikohustise osa lühiajaliseks ümberklassifitseerimiseks.</span><span class="sxs-lookup"><span data-stu-id="51bf7-104">This topic explains how to create a monthly journal entry to reclassify a portion of the lease liability as short-term.</span></span> <span data-ttu-id="51bf7-105">Kui pakktöötluses valitud graafik on **Lühiajalise rendikohustise ümberklassifitseerimine**, luuakse töölehe kanne.</span><span class="sxs-lookup"><span data-stu-id="51bf7-105">When the schedule that is selected in the batch process is **Short-term lease liability reclass**, a journal entry is created.</span></span> <span data-ttu-id="51bf7-106">Seda kirjet kasutatakse rendikohustise praeguse osa sisestamiseks kuu viimasel päeval.</span><span class="sxs-lookup"><span data-stu-id="51bf7-106">This entry is used to post the current portion of the lease liability on the last day of the month.</span></span> <span data-ttu-id="51bf7-107">Samal ajal sisestatakse tühistamise kirje järgmise kuu esimesel päeval.</span><span class="sxs-lookup"><span data-stu-id="51bf7-107">At the same time, a reversal entry is posted as of the first day of the next month.</span></span>

<span data-ttu-id="51bf7-108">Rendikohustise lühiajaline osa kuvatakse kohustuse amortisatsioonigraafikus.</span><span class="sxs-lookup"><span data-stu-id="51bf7-108">The short-term portion of the lease liability is shown on the liability amortization schedule.</span></span> <span data-ttu-id="51bf7-109">Kui töölehe kanne on sisestatud, siis on veerg **Kohustuse ümberklassifitseerimise tööleht loodud** saadaval ja töölehe ID on sisestatud ka graafikusse.</span><span class="sxs-lookup"><span data-stu-id="51bf7-109">When the journal entry is posted, the **Liability reclass journal created** column becomes available, and the journal ID is also filled in on the schedule.</span></span>

<span data-ttu-id="51bf7-110">Lühiajalise kohustise ümberklassifitseerimise töölehe kirje loomiseks ja sisestamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="51bf7-110">To create and post the short-term liability reclassification journal entry, follow these steps.</span></span>

1. <span data-ttu-id="51bf7-111">Avage **Vara rentimine \> Perioodiline \> Töölehe partiina loomine**.</span><span class="sxs-lookup"><span data-stu-id="51bf7-111">Go to **Asset leasing \> Periodic \> Batch journal creation**.</span></span>
2. <span data-ttu-id="51bf7-112">Valige dialoogikasti **Töölehe partiina loomine** väljal **Vali graafik** suvand **Lühiajalise rendikohustise ümberklassifitseerimine**.</span><span class="sxs-lookup"><span data-stu-id="51bf7-112">In the **Batch journal creation** dialog box, in the **Select schedule** field, select **Short-term lease liability reclass**.</span></span>
3. <span data-ttu-id="51bf7-113">Valige rendigrupp väljal **Rendigrupp**.</span><span class="sxs-lookup"><span data-stu-id="51bf7-113">In the **Lease group** field, select a lease group.</span></span> <span data-ttu-id="51bf7-114">Teise võimalusena valige raamatu ID väljal **Raamatu ID**.</span><span class="sxs-lookup"><span data-stu-id="51bf7-114">Alternatively, in the **Book ID** field, select the book ID.</span></span>
4. <span data-ttu-id="51bf7-115">Lülitage sisse parameeter **Sisestamine**.</span><span class="sxs-lookup"><span data-stu-id="51bf7-115">Turn on the **Post** parameter.</span></span> <span data-ttu-id="51bf7-116">Teise võimalusena, kui kanne tuleb luua, kuid mitte sisestada, jätke see parameeter välja.</span><span class="sxs-lookup"><span data-stu-id="51bf7-116">Alternatively, if the entry should be created but not posted, leave this parameter turned off.</span></span>
5. <span data-ttu-id="51bf7-117">Enne kirje sisestamist selle vaatamiseks lülitage sisse parameeter **Eelvaatle enne sisestamist**.</span><span class="sxs-lookup"><span data-stu-id="51bf7-117">Turn on the **Preview before posting** parameter to view the entry before it's posted.</span></span>
6. <span data-ttu-id="51bf7-118">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="51bf7-118">Select **OK**.</span></span>
