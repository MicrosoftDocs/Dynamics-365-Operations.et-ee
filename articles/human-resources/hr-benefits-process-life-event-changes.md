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
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a3cddc6205660b48abd9067bfdcaa04c9d2ba541
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790904"
---
# <a name="process-life-event-changes"></a><span data-ttu-id="b69b4-103">Elusündmuste muutuste töötlemine</span><span class="sxs-lookup"><span data-stu-id="b69b4-103">Process life event changes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b69b4-104">Elusündmuste muutuste töötlemine rakenduses Microsoft Dynamics 365 Human Resources kahe elusündmuse muutuse korral.</span><span class="sxs-lookup"><span data-stu-id="b69b4-104">Process life event changes in Microsoft Dynamics 365 Human Resources for two life event changes:</span></span>

- <span data-ttu-id="b69b4-105">Sünnipäev muutub</span><span class="sxs-lookup"><span data-stu-id="b69b4-105">Birthday changes</span></span>
- <span data-ttu-id="b69b4-106">Sobivusreegli tühistamise aegumine muutub</span><span class="sxs-lookup"><span data-stu-id="b69b4-106">Eligibility rule override expiration changes</span></span> 

1. <span data-ttu-id="b69b4-107">Tööruumis **Soodustuste haldus** jaotises **Töötlemine** valige suvand **Elusündmuse muutuse töötlemine**.</span><span class="sxs-lookup"><span data-stu-id="b69b4-107">In the **Benefits management** workspace, under **Processing**, select **Life event change processing**.</span></span>

2. <span data-ttu-id="b69b4-108">Dialoogiaknas **Elusündmuse muutuse protsessi käitamine** määrake järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="b69b4-108">In the **Run life event change process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="b69b4-109">Väli</span><span class="sxs-lookup"><span data-stu-id="b69b4-109">Field</span></span> | <span data-ttu-id="b69b4-110">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="b69b4-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="b69b4-111">Registreerimisperiood</span><span class="sxs-lookup"><span data-stu-id="b69b4-111">Enrollment period</span></span> | <span data-ttu-id="b69b4-112">Registreerimisperiood, mille jaoks elusündmuse muudatusi töödelda.</span><span class="sxs-lookup"><span data-stu-id="b69b4-112">The enrollment period to process life event changes for.</span></span> |
   | <span data-ttu-id="b69b4-113">Juriidiline isik</span><span class="sxs-lookup"><span data-stu-id="b69b4-113">Legal entity</span></span> | <span data-ttu-id="b69b4-114">Juriidiline isik, mille jaoks elusündmuse muudatusi töödelda.</span><span class="sxs-lookup"><span data-stu-id="b69b4-114">The legal entity to process life event changes for.</span></span> |

3. <span data-ttu-id="b69b4-115">Kui soovite protsessi käitada taustal, valige suvand **Käivita taustal** ja tehke järgmised ülesanded.</span><span class="sxs-lookup"><span data-stu-id="b69b4-115">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="b69b4-116">Sisestage teavet protsessi kohta.</span><span class="sxs-lookup"><span data-stu-id="b69b4-116">Enter information for the process.</span></span>

   2. <span data-ttu-id="b69b4-117">Korduva töö seadistamiseks valige suvand **Kordumine**, sisestage kordumise teave ja valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="b69b4-117">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="b69b4-118">Töö teatise seadistamiseks valige suvand **teatised**, valige milliseid teatisi saada ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="b69b4-118">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="b69b4-119">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="b69b4-119">Select **OK**.</span></span> <span data-ttu-id="b69b4-120">Protsess töötab teie määratud parameetritega.</span><span class="sxs-lookup"><span data-stu-id="b69b4-120">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="b69b4-121">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="b69b4-121">Select **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]