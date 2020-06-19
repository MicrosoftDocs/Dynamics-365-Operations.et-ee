---
title: Soodustuste halduse parameetrite määramine
description: Konfigureerige soodustuste halduse parameetreid rakenduses Microsoft Dynamics 365 Human Resources.
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
ms.openlocfilehash: 3e001c08751ea9c8bcab0e11a04b6cf639e51d1d
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2020
ms.locfileid: "3429979"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="37a98-103">Soodustuste halduse parameetrite määramine</span><span class="sxs-lookup"><span data-stu-id="37a98-103">Set Benefits management parameters</span></span>

<span data-ttu-id="37a98-104">Enne rakenduses Microsoft Dynamics 365 Human Resources puhkuseplaanid seadistamist peate konfigureerima soodustuste halduse parameetrid.</span><span class="sxs-lookup"><span data-stu-id="37a98-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you must configure Benefits management parameters.</span></span> <span data-ttu-id="37a98-105">Need parameetrid määravad vaikeväärtused, põhjuse koodid ja muud valikud.</span><span class="sxs-lookup"><span data-stu-id="37a98-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="37a98-106">Üldiste parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="37a98-106">Configure general parameters</span></span>

1. <span data-ttu-id="37a98-107">Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="37a98-107">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="37a98-108">Määrake vahekaardil **Üldine** järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="37a98-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="37a98-109">Väli</span><span class="sxs-lookup"><span data-stu-id="37a98-109">Field</span></span> | <span data-ttu-id="37a98-110">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="37a98-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="37a98-111">**Riik/regioon**</span><span class="sxs-lookup"><span data-stu-id="37a98-111">**Country/region**</span></span> | <span data-ttu-id="37a98-112">Väli **Riik/regioon** määratleb sihtnumbrite/osariikide kuvamisjärjestuse.</span><span class="sxs-lookup"><span data-stu-id="37a98-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="37a98-113">Valitud riik kuvatakse ripploendis esimesena.</span><span class="sxs-lookup"><span data-stu-id="37a98-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="37a98-114">**Registreerimise põhjusekood**</span><span class="sxs-lookup"><span data-stu-id="37a98-114">**Enrollment reason code**</span></span> | <span data-ttu-id="37a98-115">Valige vaikimisi põhjuse kood, mida kasutada, kui töötaja plaanid avaliku registreerimise töötlemise käigus luuakse.</span><span class="sxs-lookup"><span data-stu-id="37a98-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="37a98-116">**Tühistamise põhjusekood**</span><span class="sxs-lookup"><span data-stu-id="37a98-116">**Cancellation reason code**</span></span> | <span data-ttu-id="37a98-117">Töötaja soodustuse plaani tühistamisel kasutatav põhjuse kood.</span><span class="sxs-lookup"><span data-stu-id="37a98-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="37a98-118">See kuvatakse tühistamise protsessi käigus dialoogiaknas.</span><span class="sxs-lookup"><span data-stu-id="37a98-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="37a98-119">Kasutajad saavad vajadusel suvandit **Tühistamise põhjuse kood** muuta.</span><span class="sxs-lookup"><span data-stu-id="37a98-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="37a98-120">**Põhjusekoodi taasavamine**</span><span class="sxs-lookup"><span data-stu-id="37a98-120">**Reopen reason code**</span></span> | <span data-ttu-id="37a98-121">Töötaja soodustuse plaani taasavamisel kasutatav põhjuse kood.</span><span class="sxs-lookup"><span data-stu-id="37a98-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="37a98-122">See kuvatakse tühistamise protsessi käigus dialoogiaknas.</span><span class="sxs-lookup"><span data-stu-id="37a98-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="37a98-123">Kasutajad saavad vajadusel suvandit **Taasavamise põhjuse kood** muuta.</span><span class="sxs-lookup"><span data-stu-id="37a98-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="37a98-124">**Elusündmuse põhjusekood**</span><span class="sxs-lookup"><span data-stu-id="37a98-124">**Life event reason code**</span></span> | <span data-ttu-id="37a98-125">Põhjuse kood, mida kasutatakse elusündmuse toimumisel.</span><span class="sxs-lookup"><span data-stu-id="37a98-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="37a98-126">**Määra muutuse põhjusekood**</span><span class="sxs-lookup"><span data-stu-id="37a98-126">**Rate change reason code**</span></span> | <span data-ttu-id="37a98-127">Põhjuse kood, mida kasutada töötaja soodustuse plaani tühistamisel ja uuesti avamisel määra muutmise värskendamisprotsessi käigus.</span><span class="sxs-lookup"><span data-stu-id="37a98-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="37a98-128">See näitab, milliseid kirjeid määra muutmise värskendusprotsessiga muudeti.</span><span class="sxs-lookup"><span data-stu-id="37a98-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="37a98-129">**Uus palkamine sobilik**</span><span class="sxs-lookup"><span data-stu-id="37a98-129">**New hire eligible**</span></span> | <span data-ttu-id="37a98-130">Määrab, kas uued töötajad on sobivad.</span><span class="sxs-lookup"><span data-stu-id="37a98-130">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="37a98-131">**Uue palkamise registreerimisperiood**</span><span class="sxs-lookup"><span data-stu-id="37a98-131">**New hire enrollment period**</span></span> | <span data-ttu-id="37a98-132">Ajaperiood, mil uue töötaja registreerimine on lubatud.</span><span class="sxs-lookup"><span data-stu-id="37a98-132">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="37a98-133">**Määrkus**: see säte alistab kõik uue töötaja registreerimisperioodid, mille plaani sobivusreeglis määrasite.</span><span class="sxs-lookup"><span data-stu-id="37a98-133">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> | 
   | <span data-ttu-id="37a98-134">**Elusündmused on lubatud**</span><span class="sxs-lookup"><span data-stu-id="37a98-134">**Life events enabled**</span></span> | <span data-ttu-id="37a98-135">Lubab elusündmused.</span><span class="sxs-lookup"><span data-stu-id="37a98-135">Enables life events.</span></span> |
   | <span data-ttu-id="37a98-136">**Peida pärandsoodustuse vormid**</span><span class="sxs-lookup"><span data-stu-id="37a98-136">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="37a98-137">Võimaldab teil peita pärandsoodustuse vorme.</span><span class="sxs-lookup"><span data-stu-id="37a98-137">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="37a98-138">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="37a98-138">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="37a98-139">Töövõtja iseteeninduse parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="37a98-139">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="37a98-140">Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="37a98-140">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="37a98-141">Määrake vahekaardil **Töövõtja iseteenindus** järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="37a98-141">In the **Employee self service** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="37a98-142">Väli</span><span class="sxs-lookup"><span data-stu-id="37a98-142">Field</span></span> | <span data-ttu-id="37a98-143">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="37a98-143">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="37a98-144">**Soodustuse kinnitamine**</span><span class="sxs-lookup"><span data-stu-id="37a98-144">**Benefit verification**</span></span> | <span data-ttu-id="37a98-145">Soodustuste iseteenindusest väljaregistreerimisel kasutatav kinnitustekst.</span><span class="sxs-lookup"><span data-stu-id="37a98-145">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="37a98-146">**Volitatud isikute automaatne valimine**</span><span class="sxs-lookup"><span data-stu-id="37a98-146">**Auto select designees**</span></span> | <span data-ttu-id="37a98-147">Määrab, kas valida sõltuvad ja kasusaajad vastavalt nende plaanisuvandite sobivusele automaatselt.</span><span class="sxs-lookup"><span data-stu-id="37a98-147">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="37a98-148">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="37a98-148">Select **Save**.</span></span>
