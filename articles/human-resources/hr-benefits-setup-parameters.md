---
title: Soodustuste halduse parameetrite määramine
description: Konfigureerige soodustuste halduse parameetreid rakenduses Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 07/16/2020
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
ms.openlocfilehash: 85bbe5d3b422f2f29f1d1fe8ee269b407da691c2
ms.sourcegitcommit: 9dc5c7dd5877cc6e7cd0059d173bcd8052ba13bc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/16/2020
ms.locfileid: "3599352"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="dc9a9-103">Soodustuste halduse parameetrite määramine</span><span class="sxs-lookup"><span data-stu-id="dc9a9-103">Set Benefits management parameters</span></span>

<span data-ttu-id="dc9a9-104">Enne rakenduses Microsoft Dynamics 365 Human Resources puhkuseplaanid seadistamist peate konfigureerima soodustuste halduse parameetrid.</span><span class="sxs-lookup"><span data-stu-id="dc9a9-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="dc9a9-105">Need parameetrid määravad vaikeväärtused, põhjuse koodid ja muud valikud.</span><span class="sxs-lookup"><span data-stu-id="dc9a9-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="dc9a9-106">Üldiste parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="dc9a9-106">Configure general parameters</span></span>

1. <span data-ttu-id="dc9a9-107">Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Human Resourcesi ühiskasutusega parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="dc9a9-107">In the **Benefits management** workspace, under **Setup**, select **Human Resources Shared Parameters**.</span></span>

2. <span data-ttu-id="dc9a9-108">Määrake vahekaardil **Üldine** järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="dc9a9-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="dc9a9-109">Väli</span><span class="sxs-lookup"><span data-stu-id="dc9a9-109">Field</span></span> | <span data-ttu-id="dc9a9-110">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="dc9a9-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="dc9a9-111">**Riik/regioon**</span><span class="sxs-lookup"><span data-stu-id="dc9a9-111">**Country/region**</span></span> | <span data-ttu-id="dc9a9-112">Väli **Riik/regioon** määratleb sihtnumbrite/osariikide kuvamisjärjestuse.</span><span class="sxs-lookup"><span data-stu-id="dc9a9-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="dc9a9-113">Valitud riik kuvatakse ripploendis esimesena.</span><span class="sxs-lookup"><span data-stu-id="dc9a9-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="dc9a9-114">**Registreerimise põhjusekood**</span><span class="sxs-lookup"><span data-stu-id="dc9a9-114">**Enrollment reason code**</span></span> | <span data-ttu-id="dc9a9-115">Valige vaikimisi põhjuse kood, mida kasutada, kui töötaja plaanid avaliku registreerimise töötlemise käigus luuakse.</span><span class="sxs-lookup"><span data-stu-id="dc9a9-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="dc9a9-116">**Tühistamise põhjusekood**</span><span class="sxs-lookup"><span data-stu-id="dc9a9-116">**Cancellation reason code**</span></span> | <span data-ttu-id="dc9a9-117">Töötaja soodustuse plaani tühistamisel kasutatav põhjuse kood.</span><span class="sxs-lookup"><span data-stu-id="dc9a9-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="dc9a9-118">See kuvatakse tühistamise protsessi käigus dialoogiaknas.</span><span class="sxs-lookup"><span data-stu-id="dc9a9-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="dc9a9-119">Kasutajad saavad vajadusel suvandit **Tühistamise põhjuse kood** muuta.</span><span class="sxs-lookup"><span data-stu-id="dc9a9-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="dc9a9-120">**Põhjusekoodi taasavamine**</span><span class="sxs-lookup"><span data-stu-id="dc9a9-120">**Reopen reason code**</span></span> | <span data-ttu-id="dc9a9-121">Töötaja soodustuse plaani taasavamisel kasutatav põhjuse kood.</span><span class="sxs-lookup"><span data-stu-id="dc9a9-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="dc9a9-122">See kuvatakse tühistamise protsessi käigus dialoogiaknas.</span><span class="sxs-lookup"><span data-stu-id="dc9a9-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="dc9a9-123">Kasutajad saavad vajadusel suvandit **Taasavamise põhjuse kood** muuta.</span><span class="sxs-lookup"><span data-stu-id="dc9a9-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="dc9a9-124">**Elusündmuse põhjusekood**</span><span class="sxs-lookup"><span data-stu-id="dc9a9-124">**Life event reason code**</span></span> | <span data-ttu-id="dc9a9-125">Põhjuse kood, mida kasutatakse elusündmuse toimumisel.</span><span class="sxs-lookup"><span data-stu-id="dc9a9-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="dc9a9-126">**Määra muutuse põhjusekood**</span><span class="sxs-lookup"><span data-stu-id="dc9a9-126">**Rate change reason code**</span></span> | <span data-ttu-id="dc9a9-127">Põhjuse kood, mida kasutada töötaja soodustuse plaani tühistamisel ja uuesti avamisel määra muutmise värskendamisprotsessi käigus.</span><span class="sxs-lookup"><span data-stu-id="dc9a9-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="dc9a9-128">See näitab, milliseid kirjeid määra muutmise värskendusprotsessiga muudeti.</span><span class="sxs-lookup"><span data-stu-id="dc9a9-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="dc9a9-129">**Soodustuste aastane palk**</span><span class="sxs-lookup"><span data-stu-id="dc9a9-129">**Benefits annual salary**</span></span> | <span data-ttu-id="dc9a9-130">Lubab teil määrata summa **Soodustuste aastane palgasumma** töövõtja jaoks.</span><span class="sxs-lookup"><span data-stu-id="dc9a9-130">Enables you to set a **Benefits annual salary** amount for an employee.</span></span> <span data-ttu-id="dc9a9-131">Human Resources kasutab summat **Soodustuse aastane palgasumma** kindlustussummade määramiseks aastase põhipalga summa asemel.</span><span class="sxs-lookup"><span data-stu-id="dc9a9-131">Human Resources will use the **Benefits annual salary** amount when determing coverage amounts, instead of the fixed compensation annual amount.</span></span> |
   | <span data-ttu-id="dc9a9-132">**Uus palkamine sobilik**</span><span class="sxs-lookup"><span data-stu-id="dc9a9-132">**New hire eligible**</span></span> | <span data-ttu-id="dc9a9-133">Määrab, kas uued töötajad on sobivad.</span><span class="sxs-lookup"><span data-stu-id="dc9a9-133">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="dc9a9-134">**Uue palkamise registreerimisperiood**</span><span class="sxs-lookup"><span data-stu-id="dc9a9-134">**New hire enrollment period**</span></span> | <span data-ttu-id="dc9a9-135">Ajaperiood, mil uue töötaja registreerimine on lubatud.</span><span class="sxs-lookup"><span data-stu-id="dc9a9-135">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="dc9a9-136">**Määrkus**: see säte alistab kõik uue töötaja registreerimisperioodid, mille plaani sobivusreeglis määrasite.</span><span class="sxs-lookup"><span data-stu-id="dc9a9-136">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> |
   | <span data-ttu-id="dc9a9-137">**Maksete vaikesagedus**</span><span class="sxs-lookup"><span data-stu-id="dc9a9-137">**Default pay frequency**</span></span> | <span data-ttu-id="dc9a9-138">Vaikimisi kasutatav maksesagedus uute töötajate lisamisel.</span><span class="sxs-lookup"><span data-stu-id="dc9a9-138">The default pay frequency to use when new workers are added.</span></span> |
   | <span data-ttu-id="dc9a9-139">**Elusündmused on lubatud**</span><span class="sxs-lookup"><span data-stu-id="dc9a9-139">**Life events enabled**</span></span> | <span data-ttu-id="dc9a9-140">Lubab elusündmused.</span><span class="sxs-lookup"><span data-stu-id="dc9a9-140">Enables life events.</span></span> |
   | <span data-ttu-id="dc9a9-141">**Peida pärandsoodustuse vormid**</span><span class="sxs-lookup"><span data-stu-id="dc9a9-141">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="dc9a9-142">Võimaldab teil peita pärandsoodustuse vorme.</span><span class="sxs-lookup"><span data-stu-id="dc9a9-142">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="dc9a9-143">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="dc9a9-143">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="dc9a9-144">Töövõtja iseteeninduse parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="dc9a9-144">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="dc9a9-145">Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Human Resourcesi parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="dc9a9-145">In the **Benefits management** workspace, under **Setup**, select **Human Resources Parameters**.</span></span>

2. <span data-ttu-id="dc9a9-146">Määrake vahekaardil **Töövõtja iseteenindus** järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="dc9a9-146">In the **Employee self service** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="dc9a9-147">Väli</span><span class="sxs-lookup"><span data-stu-id="dc9a9-147">Field</span></span> | <span data-ttu-id="dc9a9-148">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="dc9a9-148">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="dc9a9-149">**Soodustuse kinnitamine**</span><span class="sxs-lookup"><span data-stu-id="dc9a9-149">**Benefit verification**</span></span> | <span data-ttu-id="dc9a9-150">Soodustuste iseteenindusest väljaregistreerimisel kasutatav kinnitustekst.</span><span class="sxs-lookup"><span data-stu-id="dc9a9-150">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="dc9a9-151">**Volitatud isikute automaatne valimine**</span><span class="sxs-lookup"><span data-stu-id="dc9a9-151">**Auto select designees**</span></span> | <span data-ttu-id="dc9a9-152">Määrab, kas valida sõltuvad ja kasusaajad vastavalt nende plaanisuvandite sobivusele automaatselt.</span><span class="sxs-lookup"><span data-stu-id="dc9a9-152">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="dc9a9-153">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="dc9a9-153">Select **Save**.</span></span>
