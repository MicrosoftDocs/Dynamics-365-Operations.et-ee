---
title: Jõudluse optimeerimine pakett-tööde ajastamisel töövälisele ajale
description: Selles teemas selgitatakse, kuidas lahendada Microsoft Dynamics 365 Human Resourcesi jõudluse probleeme, ajastades pakett-tööd töövälisele ajale.
author: andreabichsel
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: a5aeaeb7311d87a154882b7058b6da430900bd56
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053463"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a><span data-ttu-id="9545c-103">Jõudluse optimeerimine pakett-tööde ajastamisel töövälisele ajale</span><span class="sxs-lookup"><span data-stu-id="9545c-103">Optimize performance by scheduling batch jobs after hours</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a><span data-ttu-id="9545c-104">Väljastus</span><span class="sxs-lookup"><span data-stu-id="9545c-104">Issue</span></span>

<span data-ttu-id="9545c-105">Microsoft Dynamics 365 Human Resourcesis võib esineda jõudluse probleeme, kui pikaajalisi pakett-töid käitatakse tavapärasel tööajal.</span><span class="sxs-lookup"><span data-stu-id="9545c-105">Microsoft Dynamics 365 Human Resources can experience performance issues if long-running batch jobs run during typical business hours.</span></span>

## <a name="resolution"></a><span data-ttu-id="9545c-106">Eraldusvõime</span><span class="sxs-lookup"><span data-stu-id="9545c-106">Resolution</span></span>

<span data-ttu-id="9545c-107">Ajastage järgmised pakett-tööd töövälisele ajale.</span><span class="sxs-lookup"><span data-stu-id="9545c-107">Schedule the following batch jobs during off hours.</span></span> <span data-ttu-id="9545c-108">Samuti soovitame vaadata üle regulaarselt töötavate pakett-tööde sageduse.</span><span class="sxs-lookup"><span data-stu-id="9545c-108">We also recommend reviewing the frequency of batch jobs that run frequently.</span></span> <span data-ttu-id="9545c-109">Võimalusel vähendage pakett-töö sagedust.</span><span class="sxs-lookup"><span data-stu-id="9545c-109">If possible, reduce the recurrence of the batch job.</span></span> <span data-ttu-id="9545c-110">Paljudel juhtudel piisab vaikimisi sagedusest.</span><span class="sxs-lookup"><span data-stu-id="9545c-110">In many cases, the default frequency is sufficient.</span></span>

<span data-ttu-id="9545c-111">Järgmised pakett-tööd peaksid töötama öösiti või töövälisel ajal.</span><span class="sxs-lookup"><span data-stu-id="9545c-111">The following batch jobs should run at night or after hours.</span></span> <span data-ttu-id="9545c-112">Kontrollige kindlasti nende korduvate pakett-tööde ajavööndit.</span><span class="sxs-lookup"><span data-stu-id="9545c-112">Be sure to check the time zone for these recurring batch jobs.</span></span> <span data-ttu-id="9545c-113">Osad pakett-tööd võivad kasutada Lääneranniku aega (PST).</span><span class="sxs-lookup"><span data-stu-id="9545c-113">Some batch jobs might use Pacific Standard Time (PST).</span></span>

| <span data-ttu-id="9545c-114">Pakett-töö</span><span class="sxs-lookup"><span data-stu-id="9545c-114">Batch job</span></span> | <span data-ttu-id="9545c-115">Vaikesagedus</span><span class="sxs-lookup"><span data-stu-id="9545c-115">Default occurrence</span></span> |
| --- | --- |
| <span data-ttu-id="9545c-116">Pakett-töö ajaloo puhastamine</span><span class="sxs-lookup"><span data-stu-id="9545c-116">Batch job history cleanup</span></span> | <span data-ttu-id="9545c-117">1 kord kuus</span><span class="sxs-lookup"><span data-stu-id="9545c-117">1 time per month</span></span> |
| <span data-ttu-id="9545c-118">Ekspordi ajastamise puhastamine</span><span class="sxs-lookup"><span data-stu-id="9545c-118">Export staging cleanup</span></span> | <span data-ttu-id="9545c-119">1 kord päevas</span><span class="sxs-lookup"><span data-stu-id="9545c-119">1 time per day</span></span> |
| <span data-ttu-id="9545c-120">Common Data Service’i integreerimise vastamata päringu sünkroonimine</span><span class="sxs-lookup"><span data-stu-id="9545c-120">Common Data Service integration missed request sync</span></span> | <span data-ttu-id="9545c-121">1 kord päevas</span><span class="sxs-lookup"><span data-stu-id="9545c-121">1 time per day</span></span> |
| <span data-ttu-id="9545c-122">Andmebaasi tihendamise süsteemi töö, mida tuleb käitada regulaarselt töövälisel ajal</span><span class="sxs-lookup"><span data-stu-id="9545c-122">Database compression system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="9545c-123">1 kord päevas</span><span class="sxs-lookup"><span data-stu-id="9545c-123">1 time per day</span></span> |
| <span data-ttu-id="9545c-124">Andmebaasi indeksi uuesti loomise süsteemi töö, mida tuleb käitada regulaarselt töövälisel ajal</span><span class="sxs-lookup"><span data-stu-id="9545c-124">Database index rebuild system job that needs to run regularly during off hours</span></span> | <span data-ttu-id="9545c-125">1 kord päevas</span><span class="sxs-lookup"><span data-stu-id="9545c-125">1 time per day</span></span> |

1. <span data-ttu-id="9545c-126">Valige rakenduses Human Resources suvand **Süsteemihaldus**.</span><span class="sxs-lookup"><span data-stu-id="9545c-126">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="9545c-127">Otsige ribal **Otsing** ühte ülaltoodud pakett-töödest.</span><span class="sxs-lookup"><span data-stu-id="9545c-127">In the **Search** bar, search for one of the above batch jobs.</span></span>

3. <span data-ttu-id="9545c-128">Valige suvand **Käivita taustal** ja seejärel valige **Kordumine**.</span><span class="sxs-lookup"><span data-stu-id="9545c-128">Select **Run in the background**, and then select **Recurrence**.</span></span>

   ![Seadistage kordumine](media/talent-batch-history-cleanup-recurrence.png)

4. <span data-ttu-id="9545c-130">Valikus **Määratle kordumine** seadistage **Alguskuupäev** ja **Algusaeg** töövälisele ajale või nädalavahetusele.</span><span class="sxs-lookup"><span data-stu-id="9545c-130">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off hours or the weekend.</span></span> <span data-ttu-id="9545c-131">Valige **Lõppkuupäev puudub**.</span><span class="sxs-lookup"><span data-stu-id="9545c-131">Select **No end date**.</span></span> 

   ![Määratlege korduse alguskuupäev ja -kellaaeg](media/talent-batch-history-cleanup-define-recurrence.png)

5. <span data-ttu-id="9545c-133">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="9545c-133">Select **OK**.</span></span>

6. <span data-ttu-id="9545c-134">Muutke vajadusel mistahes teisi parameetreid jaotises **Käivita taustal** ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="9545c-134">If needed, change any other parameters under **Run in the background**, and then select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9545c-135">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="9545c-135">Additional resources</span></span>

[<span data-ttu-id="9545c-136">Jõudluse optimeerimine automaatsete puhastamisülesannetega</span><span class="sxs-lookup"><span data-stu-id="9545c-136">Optimize performance with auto cleanup tasks</span></span>](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]