---
title: Määrade muudatuste töötlemine
description: Töödelge rakenduses Microsoft Dynamics 365 Human Resources soodustuse määrade muudatus, kui uuel või olemasoleval soodustuse plaanil muudetake sobivusreegli sätteid.
author: andreabichsel
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart, BenefitRate, BenefitEligibilityProcessResultViewer
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c841f5d5d409c7e73cdc38988f8233747a11f837
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803821"
---
# <a name="process-rate-changes"></a><span data-ttu-id="66eb2-103">Määrade muudatuste töötlemine</span><span class="sxs-lookup"><span data-stu-id="66eb2-103">Process rate changes</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="66eb2-104">Töödelge rakenduses Microsoft Dynamics 365 Human Resources soodustuse määrade muudatus, kui uuel või olemasoleval soodustuse plaanil muudetake sobivusreegli sätteid.</span><span class="sxs-lookup"><span data-stu-id="66eb2-104">Process benefit rate changes in Microsoft Dynamics 365 Human Resources when a new or existing benefit plan has a change in eligibility rule settings.</span></span> <span data-ttu-id="66eb2-105">Kui luuakse uus sobivusreegel ja määratakse plaanile, ajendab see süsteemi käitama uuesti töötajate sobivust, et kontrollida, kas töötajad võivad nüüd olla plaani jaoks sobivad uute sobivuse võimaluste alusel.</span><span class="sxs-lookup"><span data-stu-id="66eb2-105">If a new eligibility rule is created and assigned to the plan, this prompts the system to rerun worker eligibility to check if workers may now be eligible for the plan based on new eligibility options.</span></span> 

1. <span data-ttu-id="66eb2-106">Tööruumis **Soodustuste haldus** jaotises **Töötlemine** valige suvand **Määra muutuse uuendamise töötlemine**.</span><span class="sxs-lookup"><span data-stu-id="66eb2-106">In the **Benefits management** workspace, under **Processing**, select **Rate change update processing**.</span></span>

2. <span data-ttu-id="66eb2-107">Dialoogiaknas **Soodustuse määra uuendamise protsessi käitamine** määrake järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="66eb2-107">In the **Run benefit rate update process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="66eb2-108">Väli</span><span class="sxs-lookup"><span data-stu-id="66eb2-108">Field</span></span> | <span data-ttu-id="66eb2-109">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="66eb2-109">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="66eb2-110">**Registreerimisperiood**</span><span class="sxs-lookup"><span data-stu-id="66eb2-110">**Enrollment period**</span></span> | <span data-ttu-id="66eb2-111">Registreerimisperiood, mille jaoks määrade muutusi töödelda.</span><span class="sxs-lookup"><span data-stu-id="66eb2-111">The enrollment period to process rate changes for.</span></span> |

3. <span data-ttu-id="66eb2-112">Kui soovite protsessi käitada taustal, valige suvand **Käivita taustal** ja tehke järgmised ülesanded.</span><span class="sxs-lookup"><span data-stu-id="66eb2-112">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="66eb2-113">Sisestage teavet protsessi kohta.</span><span class="sxs-lookup"><span data-stu-id="66eb2-113">Enter information for the process.</span></span>

   2. <span data-ttu-id="66eb2-114">Korduva töö seadistamiseks valige suvand **Kordumine**, sisestage kordumise teave ja valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="66eb2-114">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="66eb2-115">Töö teatise seadistamiseks valige suvand **teatised**, valige milliseid teatisi saada ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="66eb2-115">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="66eb2-116">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="66eb2-116">Select **OK**.</span></span> <span data-ttu-id="66eb2-117">Protsess töötab teie määratud parameetritega.</span><span class="sxs-lookup"><span data-stu-id="66eb2-117">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="66eb2-118">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="66eb2-118">Select **OK**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]