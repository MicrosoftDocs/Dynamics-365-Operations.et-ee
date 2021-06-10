---
title: Elusündmuste muutuste töötlemine
description: Elusündmuste muutuste töötlemine rakenduses Microsoft Dynamics 365 Human Resources elusündmuste muutuste korral.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitLifeEventTypes, BenefitEligibilityProcessResultViewer
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1bfbd7347581e57edcab39a675b17ef66e262582
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059012"
---
# <a name="process-life-event-changes"></a><span data-ttu-id="b6da6-103">Elusündmuste muutuste töötlemine</span><span class="sxs-lookup"><span data-stu-id="b6da6-103">Process life event changes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b6da6-104">Elusündmuste muutuste töötlemine rakenduses Microsoft Dynamics 365 Human Resources kahe elusündmuse muutuse korral.</span><span class="sxs-lookup"><span data-stu-id="b6da6-104">Process life event changes in Microsoft Dynamics 365 Human Resources for two life event changes:</span></span>

- <span data-ttu-id="b6da6-105">Sünnipäev muutub</span><span class="sxs-lookup"><span data-stu-id="b6da6-105">Birthday changes</span></span>
- <span data-ttu-id="b6da6-106">Sobivusreegli tühistamise aegumine muutub</span><span class="sxs-lookup"><span data-stu-id="b6da6-106">Eligibility rule override expiration changes</span></span> 

1. <span data-ttu-id="b6da6-107">Tööruumis **Soodustuste haldus** jaotises **Töötlemine** valige suvand **Elusündmuse muutuse töötlemine**.</span><span class="sxs-lookup"><span data-stu-id="b6da6-107">In the **Benefits management** workspace, under **Processing**, select **Life event change processing**.</span></span>

2. <span data-ttu-id="b6da6-108">Dialoogiaknas **Elusündmuse muutuse protsessi käitamine** määrake järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="b6da6-108">In the **Run life event change process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="b6da6-109">Väli</span><span class="sxs-lookup"><span data-stu-id="b6da6-109">Field</span></span> | <span data-ttu-id="b6da6-110">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="b6da6-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="b6da6-111">Registreerimisperiood</span><span class="sxs-lookup"><span data-stu-id="b6da6-111">Enrollment period</span></span> | <span data-ttu-id="b6da6-112">Registreerimisperiood, mille jaoks elusündmuse muudatusi töödelda.</span><span class="sxs-lookup"><span data-stu-id="b6da6-112">The enrollment period to process life event changes for.</span></span> |
   | <span data-ttu-id="b6da6-113">Juriidiline isik</span><span class="sxs-lookup"><span data-stu-id="b6da6-113">Legal entity</span></span> | <span data-ttu-id="b6da6-114">Juriidiline isik, mille jaoks elusündmuse muudatusi töödelda.</span><span class="sxs-lookup"><span data-stu-id="b6da6-114">The legal entity to process life event changes for.</span></span> |

3. <span data-ttu-id="b6da6-115">Kui soovite protsessi käitada taustal, valige suvand **Käivita taustal** ja tehke järgmised ülesanded.</span><span class="sxs-lookup"><span data-stu-id="b6da6-115">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="b6da6-116">Sisestage teavet protsessi kohta.</span><span class="sxs-lookup"><span data-stu-id="b6da6-116">Enter information for the process.</span></span>

   2. <span data-ttu-id="b6da6-117">Korduva töö seadistamiseks valige suvand **Kordumine**, sisestage kordumise teave ja valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6da6-117">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="b6da6-118">Töö teatise seadistamiseks valige suvand **teatised**, valige milliseid teatisi saada ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6da6-118">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="b6da6-119">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6da6-119">Select **OK**.</span></span> <span data-ttu-id="b6da6-120">Protsess töötab teie määratud parameetritega.</span><span class="sxs-lookup"><span data-stu-id="b6da6-120">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="b6da6-121">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6da6-121">Select **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]