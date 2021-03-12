---
title: Kõigi ettevõtete soodustuste haldamise ja töövõtjate iseteeninduse parameetrite määramine
description: Soodustuste haldamise ja töövõtja iseteeninduse parameetrite konfigureerimine rakenduses Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: tfehr
ms.date: 12/07/2020
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
ms.openlocfilehash: b50c4f71789c34f08ce810312f3c3198303b031e
ms.sourcegitcommit: d02fae79d5c02a4bc4f4b16a410c2f5ce026c204
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/05/2021
ms.locfileid: "4962436"
---
# <a name="set-benefits-management-and-employee-self-service-parameters-for-all-companies"></a><span data-ttu-id="5d923-103">Kõigi ettevõtete soodustuste haldamise ja töövõtjate iseteeninduse parameetrite määramine</span><span class="sxs-lookup"><span data-stu-id="5d923-103">Set Benefits management and Employee self-service parameters for all companies</span></span>

<span data-ttu-id="5d923-104">Enne rakenduses Microsoft Dynamics 365 Human Resources soodustusplaanide häälestamist peate konfigureerima soodustuste halduse parameetrid.</span><span class="sxs-lookup"><span data-stu-id="5d923-104">Before you can set up benefit plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="5d923-105">Need parameetrid määravad vaikeväärtused, põhjuse koodid ja muud valikud.</span><span class="sxs-lookup"><span data-stu-id="5d923-105">These parameters set default values, reason codes, and other options.</span></span> 

## <a name="configure-general-parameters"></a><span data-ttu-id="5d923-106">Üldiste parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="5d923-106">Configure general parameters</span></span>

1. <span data-ttu-id="5d923-107">Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Human Resourcesi ühiskasutusega parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="5d923-107">In the **Benefits management** workspace, under **Setup**, select **Human Resources Shared Parameters**.</span></span>

2. <span data-ttu-id="5d923-108">Määrake vahekaardil **Soodustuste haldus** järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="5d923-108">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="5d923-109">Field</span><span class="sxs-lookup"><span data-stu-id="5d923-109">Field</span></span> | <span data-ttu-id="5d923-110">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="5d923-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="5d923-111">**Riik/regioon**</span><span class="sxs-lookup"><span data-stu-id="5d923-111">**Country/region**</span></span> | <span data-ttu-id="5d923-112">Väli **Riik/regioon** määratleb sihtnumbrite/osariikide kuvamisjärjestuse.</span><span class="sxs-lookup"><span data-stu-id="5d923-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="5d923-113">Valitud riik kuvatakse ripploendis esimesena.</span><span class="sxs-lookup"><span data-stu-id="5d923-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="5d923-114">**Registreerimise põhjusekood**</span><span class="sxs-lookup"><span data-stu-id="5d923-114">**Enrollment reason code**</span></span> | <span data-ttu-id="5d923-115">Valige vaikimisi põhjuse kood, mida kasutada, kui töötaja plaanid avaliku registreerimise töötlemise käigus luuakse.</span><span class="sxs-lookup"><span data-stu-id="5d923-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="5d923-116">**Tühistamise põhjusekood**</span><span class="sxs-lookup"><span data-stu-id="5d923-116">**Cancellation reason code**</span></span> | <span data-ttu-id="5d923-117">Töötaja soodustuse plaani tühistamisel kasutatav põhjuse kood.</span><span class="sxs-lookup"><span data-stu-id="5d923-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="5d923-118">See kuvatakse tühistamise protsessi käigus dialoogiaknas.</span><span class="sxs-lookup"><span data-stu-id="5d923-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="5d923-119">Kasutajad saavad vajadusel suvandit **Tühistamise põhjuse kood** muuta.</span><span class="sxs-lookup"><span data-stu-id="5d923-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="5d923-120">**Põhjusekoodi taasavamine**</span><span class="sxs-lookup"><span data-stu-id="5d923-120">**Reopen reason code**</span></span> | <span data-ttu-id="5d923-121">Töötaja soodustuse plaani taasavamisel kasutatav põhjuse kood.</span><span class="sxs-lookup"><span data-stu-id="5d923-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="5d923-122">See kuvatakse tühistamise protsessi käigus dialoogiaknas.</span><span class="sxs-lookup"><span data-stu-id="5d923-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="5d923-123">Kasutajad saavad vajadusel suvandit **Taasavamise põhjuse kood** muuta.</span><span class="sxs-lookup"><span data-stu-id="5d923-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="5d923-124">**Elusündmuse põhjusekood**</span><span class="sxs-lookup"><span data-stu-id="5d923-124">**Life event reason code**</span></span> | <span data-ttu-id="5d923-125">Põhjuse kood, mida kasutatakse elusündmuse toimumisel.</span><span class="sxs-lookup"><span data-stu-id="5d923-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="5d923-126">**Määra muutuse põhjusekood**</span><span class="sxs-lookup"><span data-stu-id="5d923-126">**Rate change reason code**</span></span> | <span data-ttu-id="5d923-127">Põhjuse kood, mida kasutada töötaja soodustuse plaani tühistamisel ja uuesti avamisel määra muutmise värskendamisprotsessi käigus.</span><span class="sxs-lookup"><span data-stu-id="5d923-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="5d923-128">See näitab, milliseid kirjeid määra muutmise värskendusprotsessiga muudeti.</span><span class="sxs-lookup"><span data-stu-id="5d923-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="5d923-129">**Soodustuste aastane palk**</span><span class="sxs-lookup"><span data-stu-id="5d923-129">**Benefits annual salary**</span></span> | <span data-ttu-id="5d923-130">Lubab teil määrata summa **Soodustuste aastane palgasumma** töövõtja jaoks.</span><span class="sxs-lookup"><span data-stu-id="5d923-130">Enables you to set a **Benefits annual salary** amount for an employee.</span></span> <span data-ttu-id="5d923-131">Human Resources kasutab summat **Soodustuse aastane palgasumma** kindlustussummade määramiseks aastase põhipalga summa asemel.</span><span class="sxs-lookup"><span data-stu-id="5d923-131">Human Resources will use the **Benefits annual salary** amount when determining coverage amounts, instead of the fixed compensation annual amount.</span></span> |
   | <span data-ttu-id="5d923-132">**Uus palkamine sobilik**</span><span class="sxs-lookup"><span data-stu-id="5d923-132">**New hire eligible**</span></span> | <span data-ttu-id="5d923-133">Määrab, kas uued töötajad on sobivad.</span><span class="sxs-lookup"><span data-stu-id="5d923-133">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="5d923-134">**Uue palkamise registreerimisperiood**</span><span class="sxs-lookup"><span data-stu-id="5d923-134">**New hire enrollment period**</span></span> | <span data-ttu-id="5d923-135">Ajaperiood, mil uue töötaja registreerimine on lubatud.</span><span class="sxs-lookup"><span data-stu-id="5d923-135">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="5d923-136">**Määrkus**: see säte alistab kõik uue töötaja registreerimisperioodid, mille plaani sobivusreeglis määrasite.</span><span class="sxs-lookup"><span data-stu-id="5d923-136">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> |
   | <span data-ttu-id="5d923-137">**Maksete vaikesagedus**</span><span class="sxs-lookup"><span data-stu-id="5d923-137">**Default pay frequency**</span></span> | <span data-ttu-id="5d923-138">Vaikimisi kasutatav maksesagedus uute töötajate lisamisel.</span><span class="sxs-lookup"><span data-stu-id="5d923-138">The default pay frequency to use when new workers are added.</span></span> |
   | <span data-ttu-id="5d923-139">**Elusündmused on lubatud**</span><span class="sxs-lookup"><span data-stu-id="5d923-139">**Life events enabled**</span></span> | <span data-ttu-id="5d923-140">Lubab elusündmused.</span><span class="sxs-lookup"><span data-stu-id="5d923-140">Enables life events.</span></span> |
   | <span data-ttu-id="5d923-141">**Peida pärandsoodustuse vormid**</span><span class="sxs-lookup"><span data-stu-id="5d923-141">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="5d923-142">Võimaldab teil peita pärandsoodustuse vorme.</span><span class="sxs-lookup"><span data-stu-id="5d923-142">Allows you to hide legacy benefit forms.</span></span> |
   | <span data-ttu-id="5d923-143">**Soodustuse kinnitamine**</span><span class="sxs-lookup"><span data-stu-id="5d923-143">**Benefit verification**</span></span> | <span data-ttu-id="5d923-144">Soodustuste iseteenindusest väljaregistreerimisel kasutatav kinnitustekst.</span><span class="sxs-lookup"><span data-stu-id="5d923-144">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="5d923-145">**Volitatud isikute automaatne valimine**</span><span class="sxs-lookup"><span data-stu-id="5d923-145">**Auto select designees**</span></span> | <span data-ttu-id="5d923-146">Määrab, kas valida sõltuvad ja kasusaajad vastavalt nende plaanisuvandite sobivusele automaatselt.</span><span class="sxs-lookup"><span data-stu-id="5d923-146">Specifies whether to automatically select dependents and beneficiaries, based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="5d923-147">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="5d923-147">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="5d923-148">Töövõtja iseteeninduse parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="5d923-148">Configure Employee self-service parameters</span></span>

1. <span data-ttu-id="5d923-149">Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Human Resourcesi parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="5d923-149">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="5d923-150">Määrake vahekaardil **Soodustuste haldus** järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="5d923-150">In the **Benefits management** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="5d923-151">Field</span><span class="sxs-lookup"><span data-stu-id="5d923-151">Field</span></span> | <span data-ttu-id="5d923-152">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="5d923-152">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="5d923-153">**Soodustuse kinnitamine**</span><span class="sxs-lookup"><span data-stu-id="5d923-153">**Benefit verification**</span></span> | <span data-ttu-id="5d923-154">Soodustuste iseteenindusest väljaregistreerimisel kasutatav kinnitustekst.</span><span class="sxs-lookup"><span data-stu-id="5d923-154">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="5d923-155">**Volitatud isikute automaatne valimine**</span><span class="sxs-lookup"><span data-stu-id="5d923-155">**Auto select designees**</span></span> | <span data-ttu-id="5d923-156">Määrab, kas valida sõltuvad ja kasusaajad vastavalt nende plaanisuvandite sobivusele automaatselt.</span><span class="sxs-lookup"><span data-stu-id="5d923-156">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="5d923-157">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="5d923-157">Select **Save**.</span></span>


