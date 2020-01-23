---
title: Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent Core HR (10. september 2018)
description: Selles teemas kirjeldatakse funktsioone, mis on kas uued või muutunud rakenduses Microsoft Dynamics 365 Talent - Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 09/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-09-06
ms.dyn365.ops.version: Talent September 10, 2018 update
ms.openlocfilehash: ff5d21a8a71b068a276bedaf6e4b9964adcb4027
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896746"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent---core-hr-september-10-2018"></a><span data-ttu-id="0bba4-103">Mis on uut või mida on muudetud rakenduses Dynamics 365 Talent Core HR (10. september 2018)</span><span class="sxs-lookup"><span data-stu-id="0bba4-103">What's new or changed in Dynamics 365 Talent - Core HR (September 10, 2018)</span></span>

<span data-ttu-id="0bba4-104">**Järk 8.1.138.0**</span><span class="sxs-lookup"><span data-stu-id="0bba4-104">**Build 8.1.138.0**</span></span>

<span data-ttu-id="0bba4-105">Selles teemas kirjeldatakse Microsoft Dynamics 365 Talent: Core HRi uusi või muutunud funktsioone.</span><span class="sxs-lookup"><span data-stu-id="0bba4-105">This topic describes features that are either new or changed in Microsoft Dynamics 365 Talent: Core HR.</span></span>

## <a name="allow-specific-time-of-day-on-time-off-requests-half-days"></a><span data-ttu-id="0bba4-106">Puhkeajataotlustele teatud aja päevast lubamine (poolikud päevad)</span><span class="sxs-lookup"><span data-stu-id="0bba4-106">Allow specific time of day on time-off requests (half days)</span></span>

<span data-ttu-id="0bba4-107">Kui puhkused ja puudumised on seadistatud nii, et puhkeaeg esitatakse päevades, saate nüüd lubada ka pooliku päeva määratluse.</span><span class="sxs-lookup"><span data-stu-id="0bba4-107">If leave and absence is set up so that time off is submitted in days, you can now also enable a half-day definition.</span></span> <span data-ttu-id="0bba4-108">Seejärel, kui kasutajad esitavad puhkeajataotlusi, saavad nad määrata, kas soovivad vabaks saada päeva esimese või teise poole.</span><span class="sxs-lookup"><span data-stu-id="0bba4-108">Then, when users submit time-off requests, they can specify whether they are requesting the first half or the second half of the day off.</span></span>

<span data-ttu-id="0bba4-109">Vaikimisi on see suvand välja lülitatud.</span><span class="sxs-lookup"><span data-stu-id="0bba4-109">By default, this option is turned off.</span></span> <span data-ttu-id="0bba4-110">Selleks et töövõtjad saaksid taotleda päeva esimese või teise poole vabaks, peate selle suvandi sisse lülitama akna Personali parameetrid alas **Puhkused ja puudumised**.</span><span class="sxs-lookup"><span data-stu-id="0bba4-110">For employees to request the first half or second half of the day off, you must turn on this option in the **Leave and absence** area of Human resources parameters.</span></span>

<span data-ttu-id="0bba4-111">Selle funktsiooni turbeprivileeg on Personaliparameetrite haldamine.</span><span class="sxs-lookup"><span data-stu-id="0bba4-111">The security privilege for this feature is Maintain Human Resources Parameters.</span></span>

## <a name="validation-of-leave-and-absence-entries"></a><span data-ttu-id="0bba4-112">Puhkuste ja puudumiste kannete kinnitamine</span><span class="sxs-lookup"><span data-stu-id="0bba4-112">Validation of leave and absence entries</span></span>

<span data-ttu-id="0bba4-113">Olenevalt sellest, kuidas puhkus on konfigureeritud, saavad töövõtjad, kes esitavad oma tööpäevas pikema puhkeajataotluse, hoiatusteate.</span><span class="sxs-lookup"><span data-stu-id="0bba4-113">Depending on how leave is configured, employees who try to submit a time-off request that is longer than their work day receive a warning message.</span></span> <span data-ttu-id="0bba4-114">Teisisõnu hoiatatakse neid, kui nad püüavad võtta mis tahes kuupäeval vabaks rohkem kui täistööpäeva.</span><span class="sxs-lookup"><span data-stu-id="0bba4-114">In other words, they are warned if they try to take more than a full day off on any given date.</span></span>

<span data-ttu-id="0bba4-115">See kinnitamine on alati sisse lülitatud.</span><span class="sxs-lookup"><span data-stu-id="0bba4-115">This validation is always turned on.</span></span> <span data-ttu-id="0bba4-116">Alati, kui töövõtja ületab päeva määratletud piirväärtuse, saab ta oma puhkeajataotluses hoiatuse.</span><span class="sxs-lookup"><span data-stu-id="0bba4-116">Any time that employees exceed the day threshold that is defined, they receive a warning in their time-off request.</span></span>

## <a name="additional-fields-for-conditional-statements-in-workflows"></a><span data-ttu-id="0bba4-117">Tingimuslike väljavõtete lisaväljad töövoogudes</span><span class="sxs-lookup"><span data-stu-id="0bba4-117">Additional fields for conditional statements in workflows</span></span>

<span data-ttu-id="0bba4-118">Core HR-is on mitme töövoo jaoks lisatud tingimuslikele väljavõtetele ja kohatäidetele lisaväljad.</span><span class="sxs-lookup"><span data-stu-id="0bba4-118">Additional fields have been added to conditional statements and placeholders for several workflows in Core HR.</span></span>

<span data-ttu-id="0bba4-119">Kompensatsiooni, lõpetamise ja ülekande töövoogudele on lisatud järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="0bba4-119">The following fields have been added to the compensation, termination, and transfer workflows:</span></span>

- <span data-ttu-id="0bba4-120">EmploymentType</span><span class="sxs-lookup"><span data-stu-id="0bba4-120">EmploymentType</span></span>
- <span data-ttu-id="0bba4-121">LegalEntity</span><span class="sxs-lookup"><span data-stu-id="0bba4-121">LegalEntity</span></span>
- <span data-ttu-id="0bba4-122">AdjustedWorkerStartDate</span><span class="sxs-lookup"><span data-stu-id="0bba4-122">AdjustedWorkerStartDate</span></span>
- <span data-ttu-id="0bba4-123">EmployerNoticeAmount</span><span class="sxs-lookup"><span data-stu-id="0bba4-123">EmployerNoticeAmount</span></span>
- <span data-ttu-id="0bba4-124">EmployerUnitOfNotice</span><span class="sxs-lookup"><span data-stu-id="0bba4-124">EmployerUnitOfNotice</span></span>
- <span data-ttu-id="0bba4-125">TransitionDate</span><span class="sxs-lookup"><span data-stu-id="0bba4-125">TransitionDate</span></span>
- <span data-ttu-id="0bba4-126">WorkerNoticeAmount</span><span class="sxs-lookup"><span data-stu-id="0bba4-126">WorkerNoticeAmount</span></span>
- <span data-ttu-id="0bba4-127">WorkerStartDate</span><span class="sxs-lookup"><span data-stu-id="0bba4-127">WorkerStartDate</span></span>
- <span data-ttu-id="0bba4-128">WorkerUnitOfNotice</span><span class="sxs-lookup"><span data-stu-id="0bba4-128">WorkerUnitOfNotice</span></span>
- <span data-ttu-id="0bba4-129">ProbationEndDate</span><span class="sxs-lookup"><span data-stu-id="0bba4-129">ProbationEndDate</span></span>
- <span data-ttu-id="0bba4-130">Ametikoht</span><span class="sxs-lookup"><span data-stu-id="0bba4-130">Position</span></span>
- <span data-ttu-id="0bba4-131">Ühendus</span><span class="sxs-lookup"><span data-stu-id="0bba4-131">Union</span></span>
- <span data-ttu-id="0bba4-132">Osakond</span><span class="sxs-lookup"><span data-stu-id="0bba4-132">Department</span></span>
- <span data-ttu-id="0bba4-133">PositionType</span><span class="sxs-lookup"><span data-stu-id="0bba4-133">PositionType</span></span>
- <span data-ttu-id="0bba4-134">CompLocation</span><span class="sxs-lookup"><span data-stu-id="0bba4-134">CompLocation</span></span>
- <span data-ttu-id="0bba4-135">Ametinimetus</span><span class="sxs-lookup"><span data-stu-id="0bba4-135">Title</span></span>
- <span data-ttu-id="0bba4-136">Töö</span><span class="sxs-lookup"><span data-stu-id="0bba4-136">Job</span></span>
- <span data-ttu-id="0bba4-137">JobType</span><span class="sxs-lookup"><span data-stu-id="0bba4-137">JobType</span></span>
- <span data-ttu-id="0bba4-138">JobFamily</span><span class="sxs-lookup"><span data-stu-id="0bba4-138">JobFamily</span></span>
- <span data-ttu-id="0bba4-139">JobFunction</span><span class="sxs-lookup"><span data-stu-id="0bba4-139">JobFunction</span></span>

<span data-ttu-id="0bba4-140">Ametikoha töövoole on lisatud järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="0bba4-140">The following fields have been added to the position workflow:</span></span>

- <span data-ttu-id="0bba4-141">Ametikoht</span><span class="sxs-lookup"><span data-stu-id="0bba4-141">Position</span></span>
- <span data-ttu-id="0bba4-142">Ühendus</span><span class="sxs-lookup"><span data-stu-id="0bba4-142">Union</span></span>
- <span data-ttu-id="0bba4-143">Osakond</span><span class="sxs-lookup"><span data-stu-id="0bba4-143">Department</span></span>
- <span data-ttu-id="0bba4-144">PositionType</span><span class="sxs-lookup"><span data-stu-id="0bba4-144">PositionType</span></span>
- <span data-ttu-id="0bba4-145">CompLocation</span><span class="sxs-lookup"><span data-stu-id="0bba4-145">CompLocation</span></span>
- <span data-ttu-id="0bba4-146">Ametinimetus</span><span class="sxs-lookup"><span data-stu-id="0bba4-146">Title</span></span>
- <span data-ttu-id="0bba4-147">Töö</span><span class="sxs-lookup"><span data-stu-id="0bba4-147">Job</span></span>
- <span data-ttu-id="0bba4-148">JobType</span><span class="sxs-lookup"><span data-stu-id="0bba4-148">JobType</span></span>
- <span data-ttu-id="0bba4-149">JobFamily</span><span class="sxs-lookup"><span data-stu-id="0bba4-149">JobFamily</span></span>
- <span data-ttu-id="0bba4-150">JobFunction</span><span class="sxs-lookup"><span data-stu-id="0bba4-150">JobFunction</span></span>

<span data-ttu-id="0bba4-151">Tingimuslike väljavõtete ja kohatäidete väljad on saadaval kõigile kasutajatele, kellel on juurdepääs eelnevalt mainitud töövoo konfigureerimisele.</span><span class="sxs-lookup"><span data-stu-id="0bba4-151">Fields in conditional statements and placeholders are available to all users who have access to configure the previously mentioned workflows.</span></span>

## <a name="navigation-to-attract-from-personnel-management"></a><span data-ttu-id="0bba4-152">Personalihaldusest Attracti navigeerimine</span><span class="sxs-lookup"><span data-stu-id="0bba4-152">Navigation to Attract from personnel management</span></span>

<span data-ttu-id="0bba4-153">Kui Attract pole personalihalduses seadistatud, suunab jaotis **Palgatavad kandidaadid** kasutajad alustama Attractiga, mitte ei kuva teadet „Me ei leidnud siin kuvamiseks midagi”.</span><span class="sxs-lookup"><span data-stu-id="0bba4-153">In personnel management, if Attract hasn't been set up, the **Candidates to hire** section directs users to get started with Attract instead of showing the message, "We didn't find anything to show here."</span></span>

## <a name="other-changes"></a><span data-ttu-id="0bba4-154">Muud muudatused</span><span class="sxs-lookup"><span data-stu-id="0bba4-154">Other changes</span></span>

<span data-ttu-id="0bba4-155">Selles versioonis sisaldub mitu täiendavat veaparandust.</span><span class="sxs-lookup"><span data-stu-id="0bba4-155">This release includes several additional bug fixes:</span></span>

- <span data-ttu-id="0bba4-156">Kui peatöövõtja on palgatud, pole vahekaart **Kompensatsioon** taotluse/toimingu lehel saadaval.</span><span class="sxs-lookup"><span data-stu-id="0bba4-156">When a contractor is hired, the **Compensation** tab should not be available on the request/action page.</span></span>
- <span data-ttu-id="0bba4-157">Taotluse lõpetamisprotsessi kestel ei saa te enne jätkata, kuni kõik nõutud väljad on täidetud.</span><span class="sxs-lookup"><span data-stu-id="0bba4-157">During the request termination process, you can't continue until all required fields contain data.</span></span>
- <span data-ttu-id="0bba4-158">Lahendatud on sortimisjärjestuse ja kuupäeva kuvamise probleemid personalijuhtimise analüüsis.</span><span class="sxs-lookup"><span data-stu-id="0bba4-158">Sort order and date display issues on the Personnel management analytics have been addressed.</span></span>
