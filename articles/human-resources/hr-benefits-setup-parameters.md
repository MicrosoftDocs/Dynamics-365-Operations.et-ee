---
title: Soodustuste halduse parameetrite määramine
description: Konfigureerige soodustuste halduse parameetreid rakenduses Microsoft Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: ab9b1fc78ce42479d9265b80337adf899cec3866
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008759"
---
# <a name="set-benefits-management-parameters"></a><span data-ttu-id="bc4ce-103">Soodustuste halduse parameetrite määramine</span><span class="sxs-lookup"><span data-stu-id="bc4ce-103">Set Benefits management parameters</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="bc4ce-104">Enne rakenduses Microsoft Dynamics 365 Human Resources puhkuseplaanid seadistamist peate konfigureerima soodustuste halduse parameetrid.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-104">Before you can set up leave plans in Microsoft Dynamics 365 Human Resources, you need to configure Benefits management parameters.</span></span> <span data-ttu-id="bc4ce-105">Need parameetrid määravad vaikeväärtused, põhjuse koodid ja muud valikud.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-105">These parameters set default values, reason codes, and other options.</span></span>

## <a name="configure-general-parameters"></a><span data-ttu-id="bc4ce-106">Üldiste parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="bc4ce-106">Configure general parameters</span></span>

1. <span data-ttu-id="bc4ce-107">Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-107">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="bc4ce-108">Määrake vahekaardil **Üldine** järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-108">In the **General** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="bc4ce-109">Väli</span><span class="sxs-lookup"><span data-stu-id="bc4ce-109">Field</span></span> | <span data-ttu-id="bc4ce-110">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="bc4ce-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="bc4ce-111">**Riik/regioon**</span><span class="sxs-lookup"><span data-stu-id="bc4ce-111">**Country/region**</span></span> | <span data-ttu-id="bc4ce-112">Väli **Riik/regioon** määratleb sihtnumbrite/osariikide kuvamisjärjestuse.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-112">The **Country/region** field determines the display order of ZIP codes/states.</span></span> <span data-ttu-id="bc4ce-113">Valitud riik kuvatakse ripploendis esimesena.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-113">The selected country displays first in the dropdown list.</span></span> |
   | <span data-ttu-id="bc4ce-114">**Registreerimise põhjusekood**</span><span class="sxs-lookup"><span data-stu-id="bc4ce-114">**Enrollment reason code**</span></span> | <span data-ttu-id="bc4ce-115">Valige vaikimisi põhjuse kood, mida kasutada, kui töötaja plaanid avaliku registreerimise töötlemise käigus luuakse.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-115">Select a default reason code to use when employee plans are created during open enrollment processing.</span></span> |
   | <span data-ttu-id="bc4ce-116">**Tühistamise põhjusekood**</span><span class="sxs-lookup"><span data-stu-id="bc4ce-116">**Cancellation reason code**</span></span> | <span data-ttu-id="bc4ce-117">Töötaja soodustuse plaani tühistamisel kasutatav põhjuse kood.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-117">The reason code to use when an employee benefit plan is canceled.</span></span> <span data-ttu-id="bc4ce-118">See kuvatakse tühistamise protsessi käigus dialoogiaknas.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-118">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="bc4ce-119">Kasutajad saavad vajadusel suvandit **Tühistamise põhjuse kood** muuta.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-119">Users can change it the **Cancellation reason code** if necessary.</span></span> |
   | <span data-ttu-id="bc4ce-120">**Põhjusekoodi taasavamine**</span><span class="sxs-lookup"><span data-stu-id="bc4ce-120">**Reopen reason code**</span></span> | <span data-ttu-id="bc4ce-121">Töötaja soodustuse plaani taasavamisel kasutatav põhjuse kood.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-121">The reason code to use when an employee benefit plan is reopened.</span></span> <span data-ttu-id="bc4ce-122">See kuvatakse tühistamise protsessi käigus dialoogiaknas.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-122">It displays in a dialog during the cancellation process.</span></span> <span data-ttu-id="bc4ce-123">Kasutajad saavad vajadusel suvandit **Taasavamise põhjuse kood** muuta.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-123">Users can change the **Reopen reason code** if necessary.</span></span> | 
   | <span data-ttu-id="bc4ce-124">**Elusündmuse põhjusekood**</span><span class="sxs-lookup"><span data-stu-id="bc4ce-124">**Life event reason code**</span></span> | <span data-ttu-id="bc4ce-125">Põhjuse kood, mida kasutatakse elusündmuse toimumisel.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-125">The reason code to use when a life event occurs.</span></span> |
   | <span data-ttu-id="bc4ce-126">**Määra muutuse põhjusekood**</span><span class="sxs-lookup"><span data-stu-id="bc4ce-126">**Rate change reason code**</span></span> | <span data-ttu-id="bc4ce-127">Põhjuse kood, mida kasutada töötaja soodustuse plaani tühistamisel ja uuesti avamisel määra muutmise värskendamisprotsessi käigus.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-127">The reason code to use when canceling and reopening an employee benefit plan during the rate change update process.</span></span> <span data-ttu-id="bc4ce-128">See näitab, milliseid kirjeid määra muutmise värskendusprotsessiga muudeti.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-128">It indicates which records were changed by the rate change update process.</span></span> |
   | <span data-ttu-id="bc4ce-129">**Uus palkamine sobilik**</span><span class="sxs-lookup"><span data-stu-id="bc4ce-129">**New hire eligible**</span></span> | <span data-ttu-id="bc4ce-130">Määrab, kas uued töötajad on sobivad.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-130">Specifies whether new hires are eligible.</span></span> |
   | <span data-ttu-id="bc4ce-131">**Uue palkamise registreerimisperiood**</span><span class="sxs-lookup"><span data-stu-id="bc4ce-131">**New hire enrollment period**</span></span> | <span data-ttu-id="bc4ce-132">Ajaperiood, mil uue töötaja registreerimine on lubatud.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-132">The period of time the new hire enrollment is allowed.</span></span></br></br><span data-ttu-id="bc4ce-133">**Määrkus**: see säte alistab kõik uue töötaja registreerimisperioodid, mille plaani sobivusreeglis määrasite.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-133">**Note**: This setting overrides any new hire enrollment period you set on the plan eligibility rule.</span></span> | 
   | <span data-ttu-id="bc4ce-134">**Iga-aastane palgatõus**</span><span class="sxs-lookup"><span data-stu-id="bc4ce-134">**Annual salary enhancement**</span></span> | <span data-ttu-id="bc4ce-135">Määrab, kas arvutada summa **Aastane soodustuse palk** suvandis **Töövõtja soodustuse üksikasjad** automaatselt.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-135">Specifies whether to automatically calculate the **Annual benefit salary** amount in **Employment Benefit Details**.</span></span> <span data-ttu-id="bc4ce-136">See põhineb töövõtja suvanditel **Põhipalga palgamäär**, **Keskmised tunnid** ja **Maksesagedus**.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-136">It's based on the employee’s **Fixed compensation pay rate**, **Average hours**, and **Payment frequency**.</span></span></br></br><span data-ttu-id="bc4ce-137">**Keskmised tunnid** × **Põhipalga määr** × **Maksesagedus** (maksmisperioodide arv) = **Aastane soodustuse palk**</span><span class="sxs-lookup"><span data-stu-id="bc4ce-137">**Average hours** x **Fixed pay rate** x **Payment frequency** (# of pay periods) = **Annual benefit salary**</span></span> </br></br><span data-ttu-id="bc4ce-138">Kui mõni väärtus väljadel **Keskmised tunnid**, **Põhipalga maksemäär** või **Maksesagedus** muutub, arvutab süsteem muudetud väärtuse põhjal uue töövõtja summa **Aastane soodustuse palk**.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-138">If any of the values in the **Average hours**, **Fixed compensation pay rate**, or **Payment frequency** fields change, the system automatically recalculates the employee’s **Annual benefit salary** amount based on the changed values.</span></span> <span data-ttu-id="bc4ce-139">Süsteem loob kirje **Kehtivuskuupäev**, et tuvastada muutuse täpne kuupäev ja kellaaeg.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-139">The system creates a **Date effective** record to identify the exact date and time the change occurred.</span></span> <span data-ttu-id="bc4ce-140">Vajadusel saate summat **Aastane soodustuse palga** käsitsi muuta.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-140">You can manually edit the **Annual benefit salary** amount if necessary.</span></span> |
   | <span data-ttu-id="bc4ce-141">**Elusündmused on lubatud**</span><span class="sxs-lookup"><span data-stu-id="bc4ce-141">**Life events enabled**</span></span> | <span data-ttu-id="bc4ce-142">Lubab elusündmused.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-142">Enables life events.</span></span> |
   | <span data-ttu-id="bc4ce-143">**Peida pärandsoodustuse vormid**</span><span class="sxs-lookup"><span data-stu-id="bc4ce-143">**Hide legacy benefit forms**</span></span> | <span data-ttu-id="bc4ce-144">Võimaldab teil peita pärandsoodustuse vorme.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-144">Allows you to hide legacy benefit forms.</span></span> |

3. <span data-ttu-id="bc4ce-145">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-145">Select **Save**.</span></span>

## <a name="configure-employee-self-service-parameters"></a><span data-ttu-id="bc4ce-146">Töövõtja iseteeninduse parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="bc4ce-146">Configure Employee self service parameters</span></span>

1. <span data-ttu-id="bc4ce-147">Tööruumis **Soodustuste haldus** jaotises **Seadistus** valige suvand **Parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-147">In the **Benefits management** workspace, under **Setup**, select **Parameters**.</span></span>

2. <span data-ttu-id="bc4ce-148">Määrake vahekaardil **Töövõtja iseteenindus** järgmiste väljade väärtused.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-148">In the **Employee self service** tab, specify values for the following fields:</span></span>

   | <span data-ttu-id="bc4ce-149">Väli</span><span class="sxs-lookup"><span data-stu-id="bc4ce-149">Field</span></span> | <span data-ttu-id="bc4ce-150">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="bc4ce-150">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="bc4ce-151">**Soodustuse kinnitamine**</span><span class="sxs-lookup"><span data-stu-id="bc4ce-151">**Benefit verification**</span></span> | <span data-ttu-id="bc4ce-152">Soodustuste iseteenindusest väljaregistreerimisel kasutatav kinnitustekst.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-152">The verification text to use during self-service benefits checkout.</span></span> |
   | <span data-ttu-id="bc4ce-153">**Volitatud isikute automaatne valimine**</span><span class="sxs-lookup"><span data-stu-id="bc4ce-153">**Auto select designees**</span></span> | <span data-ttu-id="bc4ce-154">Määrab, kas valida sõltuvad ja kasusaajad vastavalt nende plaanisuvandite sobivusele automaatselt.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-154">Specifies whether to automatically select dependents and beneficiaries based on their eligibility for plan options.</span></span> |

3. <span data-ttu-id="bc4ce-155">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="bc4ce-155">Select **Save**.</span></span>
