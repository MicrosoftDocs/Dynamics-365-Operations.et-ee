---
title: Elusündmuste muutuste töötlemine
description: Elusündmuste muutuste töötlemine rakenduses Microsoft Dynamics 365 Human Resources elusündmuste muutuste korral.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ae1aa74c7e463cd0d8c8d740394b998030c8498f
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/06/2020
ms.locfileid: "3229989"
---
# <a name="process-life-event-changes"></a><span data-ttu-id="2a232-103">Elusündmuste muutuste töötlemine</span><span class="sxs-lookup"><span data-stu-id="2a232-103">Process life event changes</span></span>

<span data-ttu-id="2a232-104">Elusündmuste muutuste töötlemine rakenduses Microsoft Dynamics 365 Human Resources kahe elusündmuse muutuse korral.</span><span class="sxs-lookup"><span data-stu-id="2a232-104">Process life event changes in Microsoft Dynamics 365 Human Resources for two life event changes:</span></span>

- <span data-ttu-id="2a232-105">Sünnipäev muutub</span><span class="sxs-lookup"><span data-stu-id="2a232-105">Birthday changes</span></span>
- <span data-ttu-id="2a232-106">Sobivusreegli tühistamise aegumine muutub</span><span class="sxs-lookup"><span data-stu-id="2a232-106">Eligibility rule override expiration changes</span></span> 

1. <span data-ttu-id="2a232-107">Tööruumis **Soodustuste haldus** jaotises **Töötlemine** valige suvand **Elusündmuse muutuse töötlemine**.</span><span class="sxs-lookup"><span data-stu-id="2a232-107">In the **Benefits management** workspace, under **Processing**, select **Life event change processing**.</span></span>

2. <span data-ttu-id="2a232-108">Dialoogiaknas **Elusündmuse muutuse protsessi käitamine** määrake järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="2a232-108">In the **Run life event change process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="2a232-109">Väli</span><span class="sxs-lookup"><span data-stu-id="2a232-109">Field</span></span> | <span data-ttu-id="2a232-110">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="2a232-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="2a232-111">Registreerimisperiood</span><span class="sxs-lookup"><span data-stu-id="2a232-111">Enrollment period</span></span> | <span data-ttu-id="2a232-112">Registreerimisperiood, mille jaoks elusündmuse muudatusi töödelda.</span><span class="sxs-lookup"><span data-stu-id="2a232-112">The enrollment period to process life event changes for.</span></span> |
   | <span data-ttu-id="2a232-113">Juriidiline isik</span><span class="sxs-lookup"><span data-stu-id="2a232-113">Legal entity</span></span> | <span data-ttu-id="2a232-114">Juriidiline isik, mille jaoks elusündmuse muudatusi töödelda.</span><span class="sxs-lookup"><span data-stu-id="2a232-114">The legal entity to process life event changes for.</span></span> |

3. <span data-ttu-id="2a232-115">Kui soovite protsessi käitada taustal, valige suvand **Käivita taustal** ja tehke järgmised ülesanded.</span><span class="sxs-lookup"><span data-stu-id="2a232-115">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="2a232-116">Sisestage teavet protsessi kohta.</span><span class="sxs-lookup"><span data-stu-id="2a232-116">Enter information for the process.</span></span>

   2. <span data-ttu-id="2a232-117">Korduva töö seadistamiseks valige suvand **Kordumine**, sisestage kordumise teave ja valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a232-117">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="2a232-118">Töö teatise seadistamiseks valige suvand **teatised**, valige milliseid teatisi saada ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a232-118">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="2a232-119">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a232-119">Select **OK**.</span></span> <span data-ttu-id="2a232-120">Protsess töötab teie määratud parameetritega.</span><span class="sxs-lookup"><span data-stu-id="2a232-120">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="2a232-121">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a232-121">Select **OK**.</span></span>
