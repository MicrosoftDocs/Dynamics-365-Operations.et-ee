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
ms.openlocfilehash: f67b4b4c20345297f186c792fe2766c686e2ddbf
ms.sourcegitcommit: bdfc84aa7f607511981c0b2f20f03fabcb773510
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/23/2020
ms.locfileid: "3500501"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a><span data-ttu-id="3c8e3-103">Jõudluse optimeerimine pakett-tööde ajastamisel töövälisele ajale</span><span class="sxs-lookup"><span data-stu-id="3c8e3-103">Optimize performance by scheduling batch jobs after hours</span></span>

## <a name="issue"></a><span data-ttu-id="3c8e3-104">Väljastus</span><span class="sxs-lookup"><span data-stu-id="3c8e3-104">Issue</span></span>

<span data-ttu-id="3c8e3-105">Microsoft Dynamics 365 Human Resourcesis võib esineda jõudluse probleeme, kui pikaajalisi pakett-töid käitatakse tavapärasel tööajal.</span><span class="sxs-lookup"><span data-stu-id="3c8e3-105">Microsoft Dynamics 365 Human Resources can experience performance issues if long-running batch jobs run during typical business hours.</span></span>

## <a name="resolution"></a><span data-ttu-id="3c8e3-106">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="3c8e3-106">Resolution</span></span>

<span data-ttu-id="3c8e3-107">Ajastage järgmised pakett-tööd töövälisele ajale.</span><span class="sxs-lookup"><span data-stu-id="3c8e3-107">Schedule the following batch jobs during off hours.</span></span> <span data-ttu-id="3c8e3-108">Samuti soovitame vaadata üle regulaarselt töötavate pakett-tööde sageduse.</span><span class="sxs-lookup"><span data-stu-id="3c8e3-108">We also recommend reviewing the frequency of batch jobs that run frequently.</span></span> <span data-ttu-id="3c8e3-109">Võimalusel vähendage pakett-töö sagedust.</span><span class="sxs-lookup"><span data-stu-id="3c8e3-109">If possible, reduce the recurrence of the batch job.</span></span> <span data-ttu-id="3c8e3-110">Paljudel juhtudel piisab vaikimisi sagedusest.</span><span class="sxs-lookup"><span data-stu-id="3c8e3-110">In many cases, the default frequency is sufficient.</span></span>

<span data-ttu-id="3c8e3-111">Järgmised pakett-tööd peaksid töötama öösiti või töövälisel ajal.</span><span class="sxs-lookup"><span data-stu-id="3c8e3-111">The following batch jobs should run at night or after hours.</span></span> <span data-ttu-id="3c8e3-112">Kontrollige kindlasti nende korduvate pakett-tööde ajavööndit.</span><span class="sxs-lookup"><span data-stu-id="3c8e3-112">Be sure to check the time zone for these recurring batch jobs.</span></span> <span data-ttu-id="3c8e3-113">Osad pakett-tööd võivad kasutada Lääneranniku aega (PST).</span><span class="sxs-lookup"><span data-stu-id="3c8e3-113">Some batch jobs might use Pacific Standard Time (PST).</span></span>

| <span data-ttu-id="3c8e3-114">Pakett-töö</span><span class="sxs-lookup"><span data-stu-id="3c8e3-114">Batch job</span></span> | <span data-ttu-id="3c8e3-115">Vaikesagedus</span><span class="sxs-lookup"><span data-stu-id="3c8e3-115">Default occurrence</span></span> |
| --- | --- |
| <span data-ttu-id="3c8e3-116">Pakett-töö ajaloo puhastamine</span><span class="sxs-lookup"><span data-stu-id="3c8e3-116">Batch job history cleanup</span></span> | <span data-ttu-id="3c8e3-117">1 kord kuus</span><span class="sxs-lookup"><span data-stu-id="3c8e3-117">1 time per month</span></span> |
| <span data-ttu-id="3c8e3-118">Ekspordi ajastamise puhastamine</span><span class="sxs-lookup"><span data-stu-id="3c8e3-118">Export staging cleanup</span></span> | <span data-ttu-id="3c8e3-119">1 kord päevas</span><span class="sxs-lookup"><span data-stu-id="3c8e3-119">1 time per day</span></span> |
| <span data-ttu-id="3c8e3-120">Common Data Service’i integreerimise vastamata päringu sünkroonimine</span><span class="sxs-lookup"><span data-stu-id="3c8e3-120">Common Data Service integration missed request sync</span></span> | <span data-ttu-id="3c8e3-121">1 kord päevas</span><span class="sxs-lookup"><span data-stu-id="3c8e3-121">1 time per day</span></span> |
| <span data-ttu-id="3c8e3-122">Andmebaasi tihendamise süsteemi töö, mida tuleb käitada regulaarselt töövälisel ajal</span><span class="sxs-lookup"><span data-stu-id="3c8e3-122">Database compression system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="3c8e3-123">1 kord päevas</span><span class="sxs-lookup"><span data-stu-id="3c8e3-123">1 time per day</span></span> |
| <span data-ttu-id="3c8e3-124">Andmebaasi indeksi uuesti loomise süsteemi töö, mida tuleb käitada regulaarselt töövälisel ajal</span><span class="sxs-lookup"><span data-stu-id="3c8e3-124">Database index rebuild system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="3c8e3-125">1 kord päevas</span><span class="sxs-lookup"><span data-stu-id="3c8e3-125">1 time per day</span></span> |

1. <span data-ttu-id="3c8e3-126">Valige rakenduses Human Resources suvand **Süsteemihaldus**.</span><span class="sxs-lookup"><span data-stu-id="3c8e3-126">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="3c8e3-127">Otsige ribal **Otsing** ühte ülaltoodud pakett-töödest.</span><span class="sxs-lookup"><span data-stu-id="3c8e3-127">In the **Search** bar, search for one of the above batch jobs.</span></span>

3. <span data-ttu-id="3c8e3-128">Valige suvand **Käivita taustal** ja seejärel valige **Kordumine**.</span><span class="sxs-lookup"><span data-stu-id="3c8e3-128">Select **Run in the background**, and then select **Recurrence**.</span></span>

   ![Seadistage kordumine](media/talent-batch-history-cleanup-recurrence.png)

4. <span data-ttu-id="3c8e3-130">Valikus **Määratle kordumine** seadistage **Alguskuupäev** ja **Algusaeg** töövälisele ajale või nädalavahetusele.</span><span class="sxs-lookup"><span data-stu-id="3c8e3-130">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off hours or the weekend.</span></span> <span data-ttu-id="3c8e3-131">Valige **Lõppkuupäev puudub**.</span><span class="sxs-lookup"><span data-stu-id="3c8e3-131">Select **No end date**.</span></span> 

   ![Määratlege korduse alguskuupäev ja -kellaaeg](media/talent-batch-history-cleanup-define-recurrence.png)

5. <span data-ttu-id="3c8e3-133">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="3c8e3-133">Select **OK**.</span></span>

6. <span data-ttu-id="3c8e3-134">Muutke vajadusel mistahes teisi parameetreid jaotises **Käivita taustal** ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="3c8e3-134">If needed, change any other parameters under **Run in the background**, and then select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3c8e3-135">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="3c8e3-135">Additional resources</span></span>

[<span data-ttu-id="3c8e3-136">Jõudluse optimeerimine automaatsete puhastamisülesannetega</span><span class="sxs-lookup"><span data-stu-id="3c8e3-136">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)
