---
title: Jõudluse optimeerimine automaatsete puhastamisülesannetega
description: See artikkel selgitab, kuidas lahendada rakenduses Microsoft Dynamics 365 Human Resources jõudluse probleeme, puhastades pakett-töö ajaloo.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 97f6e310d3a69c870fe8ef03bd7a10cc7ab652e5
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112227"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a><span data-ttu-id="d9e8e-103">Optimeeri jõudlus automaatse puhastamise ülesannetega</span><span class="sxs-lookup"><span data-stu-id="d9e8e-103">Optimize performance with auto cleanup tasks</span></span>

<span data-ttu-id="d9e8e-104">**Väljastamine**</span><span class="sxs-lookup"><span data-stu-id="d9e8e-104">**Issue**</span></span>

<span data-ttu-id="d9e8e-105">Microsoft Dynamics 365 Human Resources võib kogeda jõudluse probleeme, kui pakett-töö ajalugu kasvab liiga suureks.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-105">Microsoft Dynamics 365 Human Resources can experience performance issues if the batch job history grows too large.</span></span>

<span data-ttu-id="d9e8e-106">**Põhjus**</span><span class="sxs-lookup"><span data-stu-id="d9e8e-106">**Cause**</span></span>

<span data-ttu-id="d9e8e-107">Sageli käivitatavad pakett-tööd võivad põhjustada pakett-töö ajaloo jätkusuutmatut kasvu.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-107">Batch jobs that run frequently can lead to unsustainable growth of the batch job history.</span></span> <span data-ttu-id="d9e8e-108">See võib põhjustada jõudluse probleeme.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-108">This can cause performance issues.</span></span> 

<span data-ttu-id="d9e8e-109">**Eraldusvõime**</span><span class="sxs-lookup"><span data-stu-id="d9e8e-109">**Resolution**</span></span>

<span data-ttu-id="d9e8e-110">Planeerige automaatne ülesanne oma pakett-töö ajaloo puhastamiseks.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-110">Schedule an automatic task to clean up your batch job history.</span></span> <span data-ttu-id="d9e8e-111">Soovitame ülesande seadistada iganädalaseks käivitamiseks, kuid sõltuvalt keskkonnast võib osutuda vajalikuks puhastamist sagedamini või harvemini käitada.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-111">We recommend setting up the task to run weekly, but you might need to run the cleanup more or less frequently, depending on your environment.</span></span> <span data-ttu-id="d9e8e-112">Järgmine protseduur sisaldab meie soovitatud sätteid, kuid te saate neid vastavalt vajadusele muuta.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-112">The following procedure contains our recommended settings, but you can change these according to your needs.</span></span>

1. <span data-ttu-id="d9e8e-113">Valige rakenduses Human Resources suvand **Süsteemihaldus**.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-113">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="d9e8e-114">Sisestage väljale **Otsing** käsk **Pakett-töö ajaloo puhastamine**.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-114">In the **Search** bar, enter **Batch job history clean-up**.</span></span>

   ![Otsige pakett-töö ajaloo puhastamist](media/talent-batch-history-cleanup-search-bar.png)

3. <span data-ttu-id="d9e8e-116">Sisestage jaotisse **Ajaloo limiit (päeva)** väärtus **30**.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-116">In **History limit (days)**, enter **30**.</span></span>

   ![Määrake ajaloo limiidiks 30](media/talent-batch-history-cleanup-history-limit.png)

4. <span data-ttu-id="d9e8e-118">Valige suvand **Käivita taustal** ja seejärel valige **Kordumine**.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-118">Select **Run in the background** and then select **Recurrence**.</span></span>

   ![Seadistage kordumine](media/talent-batch-history-cleanup-recurrence.png)

5. <span data-ttu-id="d9e8e-120">Valikus **Määratle kordumine** seadistage **Alguskuupäev** ja **Algusaeg** töövälisele ajale või nädalavahetusele ning seejärel valige **LÕPP-KUUPÄEV PUUDUB**.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-120">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off-hours or the weekend, and then select **NO END DATE**.</span></span> 

   ![Määratlege korduse alguskuupäev ja -kellaaeg](media/talent-batch-history-cleanup-define-recurrence.png)

6. <span data-ttu-id="d9e8e-122">Jaotises **KORDUMISMUSTER** valige **Päevad** ja määrake **KORDA MÄÄRATUD INTERVALLI JÄREL** kuni **7**.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-122">Under **RECURRENCE PATTERN**, select **Days** and set **REPEAT AFTER SPECIFIED INTERVAL** to **7**.</span></span>

   ![Määrake puhastamisele iganädalane kordus](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. <span data-ttu-id="d9e8e-124">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-124">Select **OK**.</span></span>

8. <span data-ttu-id="d9e8e-125">Muutke vajadusel mistahes teisi parameetreid jaotises **Käivita taustal** ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="d9e8e-125">Change any other parameters under **Run in the background** as necessary, and then select **OK**.</span></span>

