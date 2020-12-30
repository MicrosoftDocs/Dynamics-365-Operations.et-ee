---
title: Jõudluse optimeerimine pakett-tööde ajastamisel töövälisele ajale
description: Selles teemas selgitatakse, kuidas lahendada Microsoft Dynamics 365 Human Resourcesi jõudluse probleeme, ajastades pakett-tööd töövälisele ajale.
author: andreabichsel
manager: AnnBe
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 452a87cf5ba6c1ac73636584d75b2ec2ac555e02
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 11/17/2020
ms.locfileid: "4527761"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a><span data-ttu-id="76ebd-103">Jõudluse optimeerimine pakett-tööde ajastamisel töövälisele ajale</span><span class="sxs-lookup"><span data-stu-id="76ebd-103">Optimize performance by scheduling batch jobs after hours</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a><span data-ttu-id="76ebd-104">Väljastus</span><span class="sxs-lookup"><span data-stu-id="76ebd-104">Issue</span></span>

<span data-ttu-id="76ebd-105">Microsoft Dynamics 365 Human Resourcesis võib esineda jõudluse probleeme, kui pikaajalisi pakett-töid käitatakse tavapärasel tööajal.</span><span class="sxs-lookup"><span data-stu-id="76ebd-105">Microsoft Dynamics 365 Human Resources can experience performance issues if long-running batch jobs run during typical business hours.</span></span>

## <a name="resolution"></a><span data-ttu-id="76ebd-106">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="76ebd-106">Resolution</span></span>

<span data-ttu-id="76ebd-107">Ajastage järgmised pakett-tööd töövälisele ajale.</span><span class="sxs-lookup"><span data-stu-id="76ebd-107">Schedule the following batch jobs during off hours.</span></span> <span data-ttu-id="76ebd-108">Samuti soovitame vaadata üle regulaarselt töötavate pakett-tööde sageduse.</span><span class="sxs-lookup"><span data-stu-id="76ebd-108">We also recommend reviewing the frequency of batch jobs that run frequently.</span></span> <span data-ttu-id="76ebd-109">Võimalusel vähendage pakett-töö sagedust.</span><span class="sxs-lookup"><span data-stu-id="76ebd-109">If possible, reduce the recurrence of the batch job.</span></span> <span data-ttu-id="76ebd-110">Paljudel juhtudel piisab vaikimisi sagedusest.</span><span class="sxs-lookup"><span data-stu-id="76ebd-110">In many cases, the default frequency is sufficient.</span></span>

<span data-ttu-id="76ebd-111">Järgmised pakett-tööd peaksid töötama öösiti või töövälisel ajal.</span><span class="sxs-lookup"><span data-stu-id="76ebd-111">The following batch jobs should run at night or after hours.</span></span> <span data-ttu-id="76ebd-112">Kontrollige kindlasti nende korduvate pakett-tööde ajavööndit.</span><span class="sxs-lookup"><span data-stu-id="76ebd-112">Be sure to check the time zone for these recurring batch jobs.</span></span> <span data-ttu-id="76ebd-113">Osad pakett-tööd võivad kasutada Lääneranniku aega (PST).</span><span class="sxs-lookup"><span data-stu-id="76ebd-113">Some batch jobs might use Pacific Standard Time (PST).</span></span>

| <span data-ttu-id="76ebd-114">Pakett-töö</span><span class="sxs-lookup"><span data-stu-id="76ebd-114">Batch job</span></span> | <span data-ttu-id="76ebd-115">Vaikesagedus</span><span class="sxs-lookup"><span data-stu-id="76ebd-115">Default occurrence</span></span> |
| --- | --- |
| <span data-ttu-id="76ebd-116">Pakett-töö ajaloo puhastamine</span><span class="sxs-lookup"><span data-stu-id="76ebd-116">Batch job history cleanup</span></span> | <span data-ttu-id="76ebd-117">1 kord kuus</span><span class="sxs-lookup"><span data-stu-id="76ebd-117">1 time per month</span></span> |
| <span data-ttu-id="76ebd-118">Ekspordi ajastamise puhastamine</span><span class="sxs-lookup"><span data-stu-id="76ebd-118">Export staging cleanup</span></span> | <span data-ttu-id="76ebd-119">1 kord päevas</span><span class="sxs-lookup"><span data-stu-id="76ebd-119">1 time per day</span></span> |
| <span data-ttu-id="76ebd-120">Common Data Service’i integreerimise vastamata päringu sünkroonimine</span><span class="sxs-lookup"><span data-stu-id="76ebd-120">Common Data Service integration missed request sync</span></span> | <span data-ttu-id="76ebd-121">1 kord päevas</span><span class="sxs-lookup"><span data-stu-id="76ebd-121">1 time per day</span></span> |
| <span data-ttu-id="76ebd-122">Andmebaasi tihendamise süsteemi töö, mida tuleb käitada regulaarselt töövälisel ajal</span><span class="sxs-lookup"><span data-stu-id="76ebd-122">Database compression system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="76ebd-123">1 kord päevas</span><span class="sxs-lookup"><span data-stu-id="76ebd-123">1 time per day</span></span> |
| <span data-ttu-id="76ebd-124">Andmebaasi indeksi uuesti loomise süsteemi töö, mida tuleb käitada regulaarselt töövälisel ajal</span><span class="sxs-lookup"><span data-stu-id="76ebd-124">Database index rebuild system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="76ebd-125">1 kord päevas</span><span class="sxs-lookup"><span data-stu-id="76ebd-125">1 time per day</span></span> |

1. <span data-ttu-id="76ebd-126">Valige rakenduses Human Resources suvand **Süsteemihaldus**.</span><span class="sxs-lookup"><span data-stu-id="76ebd-126">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="76ebd-127">Otsige ribal **Otsing** ühte ülaltoodud pakett-töödest.</span><span class="sxs-lookup"><span data-stu-id="76ebd-127">In the **Search** bar, search for one of the above batch jobs.</span></span>

3. <span data-ttu-id="76ebd-128">Valige suvand **Käivita taustal** ja seejärel valige **Kordumine**.</span><span class="sxs-lookup"><span data-stu-id="76ebd-128">Select **Run in the background**, and then select **Recurrence**.</span></span>

   ![Seadistage kordumine](media/talent-batch-history-cleanup-recurrence.png)

4. <span data-ttu-id="76ebd-130">Valikus **Määratle kordumine** seadistage **Alguskuupäev** ja **Algusaeg** töövälisele ajale või nädalavahetusele.</span><span class="sxs-lookup"><span data-stu-id="76ebd-130">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off hours or the weekend.</span></span> <span data-ttu-id="76ebd-131">Valige **Lõppkuupäev puudub**.</span><span class="sxs-lookup"><span data-stu-id="76ebd-131">Select **No end date**.</span></span> 

   ![Määratlege korduse alguskuupäev ja -kellaaeg](media/talent-batch-history-cleanup-define-recurrence.png)

5. <span data-ttu-id="76ebd-133">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="76ebd-133">Select **OK**.</span></span>

6. <span data-ttu-id="76ebd-134">Muutke vajadusel mistahes teisi parameetreid jaotises **Käivita taustal** ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="76ebd-134">If needed, change any other parameters under **Run in the background**, and then select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="76ebd-135">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="76ebd-135">Additional resources</span></span>

[<span data-ttu-id="76ebd-136">Jõudluse optimeerimine automaatsete puhastamisülesannetega</span><span class="sxs-lookup"><span data-stu-id="76ebd-136">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)
