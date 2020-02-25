---
title: Registreerimise sobivuse töötlemine
description: Selles artiklis selgitatakse, kuidas käivitada registreerimise sobivuse töötlemist.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: 0344c48460a7d1540481e09ba106526e119de72b
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008697"
---
# <a name="process-enrollment-eligibility"></a><span data-ttu-id="0ff77-103">Registreerimise sobivuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="0ff77-103">Process enrollment eligibility</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="0ff77-104">Selles artiklis selgitatakse, kuidas käivitada registreerimise sobivuse töötlemist.</span><span class="sxs-lookup"><span data-stu-id="0ff77-104">This article explains how to run the enrollment eligibility process.</span></span>

1. <span data-ttu-id="0ff77-105">Tööruumis **Soodustuste haldus** jaotises **Töötlemine** valige suvand **Registreerimise sobivuse töötlemine**.</span><span class="sxs-lookup"><span data-stu-id="0ff77-105">In the **Benefits management** workspace, under **Processing**, select **Enrollment eligibility processing**.</span></span>

2. <span data-ttu-id="0ff77-106">Dialoogiaknas **Soodustuse registreerimise sobivuse protsessi käitamine** määrake järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="0ff77-106">In the **Run benefit enrollment eligibility process** dialog box, specify values for the following fields:</span></span>

   | <span data-ttu-id="0ff77-107">Väli</span><span class="sxs-lookup"><span data-stu-id="0ff77-107">Field</span></span> | <span data-ttu-id="0ff77-108">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="0ff77-108">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="0ff77-109">Registreerimisperiood</span><span class="sxs-lookup"><span data-stu-id="0ff77-109">Enrollment period</span></span> | <span data-ttu-id="0ff77-110">Registreerimisperiood, mille jaoks registreerimise sobilikkust töödelda.</span><span class="sxs-lookup"><span data-stu-id="0ff77-110">The enrollment period to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="0ff77-111">Juriidiline isik</span><span class="sxs-lookup"><span data-stu-id="0ff77-111">Legal entity</span></span> | <span data-ttu-id="0ff77-112">Juriidiline isik, mille jaoks registreerimise sobilikkust töödelda.</span><span class="sxs-lookup"><span data-stu-id="0ff77-112">The legal entity to process enrollment eligibility for.</span></span> |
   | <span data-ttu-id="0ff77-113">Töötaja</span><span class="sxs-lookup"><span data-stu-id="0ff77-113">Worker</span></span> | <span data-ttu-id="0ff77-114">Töötaja, kelle jaoks registreerimise sobilikkust töödelda.</span><span class="sxs-lookup"><span data-stu-id="0ff77-114">The worker to process enrollment eligibility for.</span></span> <span data-ttu-id="0ff77-115">Kui jätate selle välja tühjaks, töödeldakse registreerimise sobilikkust kõigi töötajate puhul.</span><span class="sxs-lookup"><span data-stu-id="0ff77-115">If you leave this field blank, enrollment eligibility will be processed for all workers.</span></span> |
   | <span data-ttu-id="0ff77-116">Soodustusplaan</span><span class="sxs-lookup"><span data-stu-id="0ff77-116">Benefit plan</span></span> | <span data-ttu-id="0ff77-117">Soodustuse plaan, mille jaoks registreerimise sobilikkust töödelda.</span><span class="sxs-lookup"><span data-stu-id="0ff77-117">The benefit plan to process enrollment eligibility for.</span></span>

3. <span data-ttu-id="0ff77-118">Kui soovite protsessi käitada taustal, valige suvand **Käivita taustal** ja tehke järgmised ülesanded.</span><span class="sxs-lookup"><span data-stu-id="0ff77-118">If you want to run the process in the background, select **Run in the background** and do the following tasks:</span></span>

   1. <span data-ttu-id="0ff77-119">Sisestage teavet protsessi kohta.</span><span class="sxs-lookup"><span data-stu-id="0ff77-119">Enter information for the process.</span></span>

   2. <span data-ttu-id="0ff77-120">Korduva töö seadistamiseks valige suvand **Kordumine**, sisestage kordumise teave ja valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="0ff77-120">To set up a recurring job, select **Recurrence**, enter the recurrence information, and the select **OK**.</span></span>

   3. <span data-ttu-id="0ff77-121">Töö teatise seadistamiseks valige suvand **teatised**, valige milliseid teatisi saada ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="0ff77-121">To set up a job alert, select **Alerts**, select the alerts to receive, and then select **OK**.</span></span>

   4. <span data-ttu-id="0ff77-122">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="0ff77-122">Select **OK**.</span></span> <span data-ttu-id="0ff77-123">Protsess töötab teie määratud parameetritega.</span><span class="sxs-lookup"><span data-stu-id="0ff77-123">The process will run with the parameters you set.</span></span>

4. <span data-ttu-id="0ff77-124">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="0ff77-124">Select **OK**.</span></span>
