---
title: Plaani ajaloo ja plaanimise logide vaatamine
description: Selles teemas selgitatakse, kuidas vaadata planeerimistööde ajalugu, mille on käivitanud planeerimise optimeerimise funktsioon.
author: ChristianRytt
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MPSPlanRegenerationJobList, MPSPlanRegenerationJobLogs
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: d7bba084b03f8698c8bf31d171d5e4e486ed06ad
ms.sourcegitcommit: a7649b361ec54b49c0e9ee1c1c63a8815f320225
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187243"
---
# <a name="view-plan-history-and-planning-logs"></a><span data-ttu-id="a98bc-103">Plaani ajaloo ja plaanimise logide vaatamine</span><span class="sxs-lookup"><span data-stu-id="a98bc-103">View plan history and planning logs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a98bc-104">Selles teemas selgitatakse, kuidas vaadata planeerimistööde ajalugu, mille on käivitanud planeerimise optimeerimise funktsioon rakenduses Microsoft Dynamics 365 Supply Chain Management-.</span><span class="sxs-lookup"><span data-stu-id="a98bc-104">This topic explains how to view the history of planning jobs that are triggered by the Planning Optimization functionality in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="a98bc-105">Plaani ajaloo vaatamiseks avage plaan, avades **Koonplaneerimine** \> **Seadistus** \> **Plaanid** \> **Koondplaanid** ja valides suvandi **Ajalugu**.</span><span class="sxs-lookup"><span data-stu-id="a98bc-105">To view the history for a plan, open the plan by going to **Master planning** \> **Setup** \> **Plans** \> **Master plans** and selecting **History**.</span></span> <span data-ttu-id="a98bc-106">Ajaloos loetletakse kõik valitud plaani tööd.</span><span class="sxs-lookup"><span data-stu-id="a98bc-106">The history lists all the jobs for the selected plan.</span></span> <span data-ttu-id="a98bc-107">Loend sisaldab lõpetatud ja aktiivseid töid.</span><span class="sxs-lookup"><span data-stu-id="a98bc-107">The list includes completed and active jobs.</span></span>

<span data-ttu-id="a98bc-108">Plaanimise optimeerimise koondplaneerimise tööde ajalugu töötab ainult kuni 60 kirjet koondplaani kohta.</span><span class="sxs-lookup"><span data-stu-id="a98bc-108">The history of jobs for Planning Optimization master planning runs keeps only up to 60 records per master plan.</span></span> <span data-ttu-id="a98bc-109">Kui käivitate uue koondplaneerimise arvutuse, kustutatakse selle plaani varaseim ajalookirje.</span><span class="sxs-lookup"><span data-stu-id="a98bc-109">Whenever you run a new master planning calculation, that plan's earliest history record is deleted.</span></span>

<span data-ttu-id="a98bc-110">Lisaks tööde algusaja ja oleku nägemisele saate vaadata konkreetse töö logi.</span><span class="sxs-lookup"><span data-stu-id="a98bc-110">In addition to seeing the start time and status of jobs, you can view the log for a specific job.</span></span> <span data-ttu-id="a98bc-111">Logi sisaldab täiendavat teavet ja hoiatusi.</span><span class="sxs-lookup"><span data-stu-id="a98bc-111">The log includes additional information and warnings.</span></span> <span data-ttu-id="a98bc-112">Kõikidel töödel ei ole logi.</span><span class="sxs-lookup"><span data-stu-id="a98bc-112">Not all jobs have a log.</span></span> <span data-ttu-id="a98bc-113">Töö logi vaatamiseks valige **Logi**.</span><span class="sxs-lookup"><span data-stu-id="a98bc-113">To view the log for a job, select **Log**.</span></span> <span data-ttu-id="a98bc-114">Logikirjeid säilitatakse ainult 30 päeva jooksul pärast töö lõpetamiskuupäeva, pärast mida need automaatselt kustutatakse.</span><span class="sxs-lookup"><span data-stu-id="a98bc-114">Log entries are only stored for 30 days after the date the job finished, after that they are automatically deleted.</span></span>

## <a name="related-resources"></a><span data-ttu-id="a98bc-115">Seotud ressursid</span><span class="sxs-lookup"><span data-stu-id="a98bc-115">Related resources</span></span>

- [<span data-ttu-id="a98bc-116">Planeerimise optimeerimise ülevaade</span><span class="sxs-lookup"><span data-stu-id="a98bc-116">Planning Optimization overview</span></span>](planning-optimization-overview.md)
- [<span data-ttu-id="a98bc-117">Planeerimise optimeerimise kasutamise alustamine</span><span class="sxs-lookup"><span data-stu-id="a98bc-117">Get started with Planning Optimization</span></span>](get-started.md)
- [<span data-ttu-id="a98bc-118">Planeerimise optimeerimise sobivuse analüüs</span><span class="sxs-lookup"><span data-stu-id="a98bc-118">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)
- [<span data-ttu-id="a98bc-119">Plaanile filtrite rakendamine</span><span class="sxs-lookup"><span data-stu-id="a98bc-119">Apply filters to a plan</span></span>](plan-filters.md)
- [<span data-ttu-id="a98bc-120">Planeerimistöö tühistamine</span><span class="sxs-lookup"><span data-stu-id="a98bc-120">Cancel a planning job</span></span>](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]