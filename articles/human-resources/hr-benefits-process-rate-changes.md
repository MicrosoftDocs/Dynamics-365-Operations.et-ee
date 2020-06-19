---
title: Määrade muudatuste töötlemine
description: Töödelge rakenduses Microsoft Dynamics 365 Human Resources soodustuse määrade muudatus, kui uuel või olemasoleval soodustuse plaanil muudetake sobivusreegli sätteid.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b12c845b92b29063f3b0b2f6a9d98143b7f10eff
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429193"
---
# <a name="process-rate-changes"></a><span data-ttu-id="80cea-103">Määrade muudatuste töötlemine</span><span class="sxs-lookup"><span data-stu-id="80cea-103">Process rate changes</span></span>

<span data-ttu-id="80cea-104">Töödelge rakenduses Microsoft Dynamics 365 Human Resources soodustuse määrade muudatus, kui uuel või olemasoleval soodustuse plaanil muudetake sobivusreegli sätteid.</span><span class="sxs-lookup"><span data-stu-id="80cea-104">Process benefit rate changes in Microsoft Dynamics 365 Human Resources when a new or existing benefit plan has a change in eligibility rule settings.</span></span> <span data-ttu-id="80cea-105">Kui luuakse uus sobivusreegel ja määratakse plaanile, ajendab see süsteemi käitama uuesti töötajate sobivust, et kontrollida, kas töötajad võivad nüüd olla plaani jaoks sobivad uute sobivuse võimaluste alusel.</span><span class="sxs-lookup"><span data-stu-id="80cea-105">If a new eligibility rule is created and assigned to the plan, this prompts the system to rerun worker eligibility to check if workers may now be eligible for the plan based on new eligibility options.</span></span> 

1. <span data-ttu-id="80cea-106">Tööruumis **Soodustuste haldus** jaotises **Töötlemine** valige suvand **Määra muutuse uuendamise töötlemine**.</span><span class="sxs-lookup"><span data-stu-id="80cea-106">In the **Benefits management** workspace, under **Processing**, select **Rate change update processing**.</span></span>

2. <span data-ttu-id="80cea-107">Dialoogiaknas **Soodustuse määra uuendamise protsessi käitamine** määrake järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="80cea-107">In the **Run benefit rate update process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="80cea-108">Väli</span><span class="sxs-lookup"><span data-stu-id="80cea-108">Field</span></span> | <span data-ttu-id="80cea-109">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="80cea-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="80cea-110">**Registreerimisperiood**</span><span class="sxs-lookup"><span data-stu-id="80cea-110">**Enrollment period**</span></span> | <span data-ttu-id="80cea-111">Registreerimisperiood, mille jaoks määrade muutusi töödelda.</span><span class="sxs-lookup"><span data-stu-id="80cea-111">The enrollment period to process rate changes for.</span></span> |

3. <span data-ttu-id="80cea-112">Kui soovite protsessi käitada taustal, valige suvand **Käivita taustal** ja tehke järgmised ülesanded.</span><span class="sxs-lookup"><span data-stu-id="80cea-112">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="80cea-113">Sisestage teavet protsessi kohta.</span><span class="sxs-lookup"><span data-stu-id="80cea-113">Enter information for the process.</span></span>

   2. <span data-ttu-id="80cea-114">Korduva töö seadistamiseks valige suvand **Kordumine**, sisestage kordumise teave ja valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="80cea-114">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="80cea-115">Töö teatise seadistamiseks valige suvand **teatised**, valige milliseid teatisi saada ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="80cea-115">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="80cea-116">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="80cea-116">Select **OK**.</span></span> <span data-ttu-id="80cea-117">Protsess töötab teie määratud parameetritega.</span><span class="sxs-lookup"><span data-stu-id="80cea-117">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="80cea-118">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="80cea-118">Select **OK**.</span></span>
