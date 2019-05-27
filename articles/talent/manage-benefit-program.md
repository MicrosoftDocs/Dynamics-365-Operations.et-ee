---
title: Soodustusprogrammi määratlemine ja haldamine
description: Inimressursid pakuvad tööriistu, mida saab kasutada soodustuste, mahaarvamiste ja töötajate hüvitusplaanide seadistamiseks ja haldamiseks, mida organisatsioon oma töötajatele pakub või nende puhul töötleb. See artikkel sisaldab teavet soodustuste seadistamise ja haldamise kohta.
author: andreabichsel
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmBenefitEligibilityDetail, HcmBenefitSelection, SysPolicyListPage, SysPolicySourceDocumentRuleType
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 15681
ms.assetid: 6aee97ac-29f7-4b3c-8aa1-c65810de3090
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: 033377f7d45bfa2b798c098be2dde0c21739bb51
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517851"
---
# <a name="define-and-manage-a-benefits-program"></a><span data-ttu-id="cc214-104">Soodustusprogrammi määratlemine ja haldamine</span><span class="sxs-lookup"><span data-stu-id="cc214-104">Define and manage a benefits program</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cc214-105">Inimressursid pakuvad tööriistu, mida saab kasutada soodustuste, mahaarvamiste ja töötajate hüvitusplaanide seadistamiseks ja haldamiseks, mida organisatsioon oma töötajatele pakub või nende puhul töötleb.</span><span class="sxs-lookup"><span data-stu-id="cc214-105">Human resources provides a set of tools that can be used to set up and maintain benefits, deductions, and workers' compensation plans that an organization offers or processes for its workers.</span></span> <span data-ttu-id="cc214-106">See teema sisaldab teavet soodustuste seadistamise ja haldamise kohta.</span><span class="sxs-lookup"><span data-stu-id="cc214-106">This topic provides information about how to set up and manage benefits.</span></span>

<a name="benefit-setup"></a><span data-ttu-id="cc214-107">Soodustuse seadistamine</span><span class="sxs-lookup"><span data-stu-id="cc214-107">Benefit setup</span></span>
-------------

<span data-ttu-id="cc214-108">Enne kui töötajad saavad soodustuste saamiseks registreeruda, tuleb luua iga soodustuse elemendid.</span><span class="sxs-lookup"><span data-stu-id="cc214-108">Before workers can be enrolled in benefits, you must create the elements of each benefit.</span></span> <span data-ttu-id="cc214-109">Need elemendid ühendavad sarnased soodustusplaanid ja määratlevad vaikesätted, nagu mahaarvamise määrad ja raamatupidamise üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="cc214-109">These elements combine similar benefit plans and define default settings, such as deduction rates and accounting details.</span></span> <span data-ttu-id="cc214-110">Paljusid neid sätteid saab kohandada, kui töötajad soodustuse saamiseks hiljem registreeruvad.</span><span class="sxs-lookup"><span data-stu-id="cc214-110">Many of these settings can be adjusted when workers are later enrolled in the benefit.</span></span> <span data-ttu-id="cc214-111">Iga soodustusplaani puhul saab organisatsioon pakkuda mitut registreerimise võimalust või töötaja saab plaanis registreerumisest loobuda.</span><span class="sxs-lookup"><span data-stu-id="cc214-111">For each benefit plan, an organization can offer several enrollment options, or a worker can waive enrollment in the plan.</span></span> 

<span data-ttu-id="cc214-112">[![Soodustuse protsessivoog](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)</span><span class="sxs-lookup"><span data-stu-id="cc214-112">[![Benefit process flow](./media/benefit-process-flow1.png)](./media/benefit-process-flow1.png)</span></span>

## <a name="benefit-elements"></a><span data-ttu-id="cc214-113">Soodustuse elemendid</span><span class="sxs-lookup"><span data-stu-id="cc214-113">Benefit elements</span></span>
<span data-ttu-id="cc214-114">Enne soodustuste loomist ja töötajate registreerimist nende saamiseks peate määratlema elemendid, mis moodustavad soodustuse: tüüp, plaan ja valikud.</span><span class="sxs-lookup"><span data-stu-id="cc214-114">Before you begin to create to create benefits and enroll workers in them, you must define the elements that make up a benefit: the type, plan, and options.</span></span>

-   <span data-ttu-id="cc214-115">**Tüüp** – teatud soodustuse plaanide kogum, näiteks arstiabi või parkimine.</span><span class="sxs-lookup"><span data-stu-id="cc214-115">**Type** – A collection of plans for a specific benefit, such as medical or parking.</span></span>
-   <span data-ttu-id="cc214-116">**Plaan** – lepinguliselt pakkujalt saadav konkreetne soodustus.</span><span class="sxs-lookup"><span data-stu-id="cc214-116">**Plan** – A specific benefit that is contracted from a provider.</span></span>
-   <span data-ttu-id="cc214-117">**Valik** – katvuse tase, näiteks ainult töötaja või töötaja ja abikaasa/partner.</span><span class="sxs-lookup"><span data-stu-id="cc214-117">**Option** – The coverage level, such as employee only, or employee and spouse/partner.</span></span>

<span data-ttu-id="cc214-118">Iga soodustuse tüübi, nt visiooni või hambaravi puhul saab organisatsioon pakkuda oma töötajatele ühte või enamat plaani.</span><span class="sxs-lookup"><span data-stu-id="cc214-118">For each type of benefit, such as vision or dental, an organization can offer one or more plans to its workers.</span></span> <span data-ttu-id="cc214-119">Iga plaani puhul saab organisatsioon pakkuda erinevaid valikuid.</span><span class="sxs-lookup"><span data-stu-id="cc214-119">For each plan, the organization can offer different options.</span></span> <span data-ttu-id="cc214-120">Näiteks saavad töötajad täiendava tähtajaga elukindlustuse katvuse osta oma ühe, kahe või kolme aastapalga ulatuses.</span><span class="sxs-lookup"><span data-stu-id="cc214-120">For example, workers can buy additional term life insurance coverage at one, two, or three times their yearly salary.</span></span> <span data-ttu-id="cc214-121">Iga plaani ja valiku kombinatsioonist saab soodustus, mille saamiseks töötajad saavad registreeruda.</span><span class="sxs-lookup"><span data-stu-id="cc214-121">Each combination of a plan and options becomes a benefit that workers can enroll in.</span></span> 

<span data-ttu-id="cc214-122">[![soodustuse pilt](./media/benefit-pic.png)](./media/benefit-pic.png)</span><span class="sxs-lookup"><span data-stu-id="cc214-122">[![benefit pic](./media/benefit-pic.png)](./media/benefit-pic.png)</span></span>

## <a name="eligibility"></a><span data-ttu-id="cc214-123">Sobivus</span><span class="sxs-lookup"><span data-stu-id="cc214-123">Eligibility</span></span>
<span data-ttu-id="cc214-124">Töötaja soodustuse saamise õiguse tööandja pakutavatele eri tüüpi soodustustele määravad paljud tegurid.</span><span class="sxs-lookup"><span data-stu-id="cc214-124">Many factors determine worker eligibility for the various types of benefits that an employer offers.</span></span> <span data-ttu-id="cc214-125">Soodustuse loomisel Microsoft Dynamics Talentis saate seadistada selle soodustuse puhul rakenduva soodustuse saamise õiguse tüübi.</span><span class="sxs-lookup"><span data-stu-id="cc214-125">When you create a benefit in Microsoft Talent, you can set the type of eligibility that applies to that benefit.</span></span> 

<span data-ttu-id="cc214-126">Saate muuta soodustuse saadavaks kõigile töötajatele.</span><span class="sxs-lookup"><span data-stu-id="cc214-126">You can make a benefit available to all workers.</span></span> <span data-ttu-id="cc214-127">Mõned ettevõtted pakuvad näiteks parkimislube kõigile töötajatele erisoodustusena.</span><span class="sxs-lookup"><span data-stu-id="cc214-127">For example, some companies offer parking passes to all employees as a fringe benefit.</span></span> <span data-ttu-id="cc214-128">Selle soodustuse loomisel seate soodustuse saamise õiguse suvandile **Kõigil töötajatel on soodustuse saamiseks õigus**.</span><span class="sxs-lookup"><span data-stu-id="cc214-128">When you create this benefit, you set the eligibility to **All workers are eligible**.</span></span> 

<span data-ttu-id="cc214-129">Muude soodustuste, nagu sissenõudmiste ja maksude kehtestamise puhul soodustuse saamise õigus ei kehti.</span><span class="sxs-lookup"><span data-stu-id="cc214-129">For other benefits, such as garnishments and tax levies, eligibility doesn't apply.</span></span> <span data-ttu-id="cc214-130">Seda tüüpi soodustuste loomisel seate soodustuse saamise õiguse valikule **Jäta soodustuse saamise õiguse protsess vahele**.</span><span class="sxs-lookup"><span data-stu-id="cc214-130">Whey you create these types of benefits, you set the eligibility to **Bypass eligibility process**.</span></span> 

<span data-ttu-id="cc214-131">Lisaks võib soodustuse saamise õigus olla reeglipõhine.</span><span class="sxs-lookup"><span data-stu-id="cc214-131">Finally, benefit eligibility can be rule-based.</span></span> <span data-ttu-id="cc214-132">Näiteks ettevõte pakub töötajatele kahte tüüpi elukindlustust.</span><span class="sxs-lookup"><span data-stu-id="cc214-132">For example, a company offers two types of life insurance benefit to employees.</span></span> <span data-ttu-id="cc214-133">Juhtivtöötajatel on õigus kasutada ühte meie elukindlustusplaani, samas kui kõigil teistel täistööajaga töötajatel on õigus kasutada muud elukindlustusplaani.</span><span class="sxs-lookup"><span data-stu-id="cc214-133">Executive employees are eligible for one life insurance plan, whereas all other full-time employees are eligible for the other life insurance plan.</span></span> <span data-ttu-id="cc214-134">Talentis saate luua kõigi juhtivtöötajate leidmiseks soodustuse saamise õiguse reegli ja teise reegli kõigi täistööajaga töötajate leidmiseks ja seejärel saate need reeglid asjakohasele soodustusele rakendada.</span><span class="sxs-lookup"><span data-stu-id="cc214-134">In Talent, you can create a benefit eligibility rule to find all executive employees and another rule to find all other full-time employees, and then apply those rules to the appropriate benefit.</span></span>

## <a name="enrollment"></a><span data-ttu-id="cc214-135">Registreerimine</span><span class="sxs-lookup"><span data-stu-id="cc214-135">Enrollment</span></span>
<span data-ttu-id="cc214-136">Pärast teie organisatsiooni pakutavate soodustuste loomist ja soodustuse saamise õiguse määratlemist saate töötajaid soodustuse saamiseks registreerida.</span><span class="sxs-lookup"><span data-stu-id="cc214-136">After you've created the benefits that your organization offers and determined eligibility, you can enroll your workers in benefits.</span></span> <span data-ttu-id="cc214-137">Saate soodustuse saamiseks registreerida ühe töötaja või registreerida mitu töötajat ühe protsessi ühe või mitme soodustuse saamiseks.</span><span class="sxs-lookup"><span data-stu-id="cc214-137">You can enroll a single worker in benefits, or you can enroll many workers in one or more benefits during a single process.</span></span> 

<span data-ttu-id="cc214-138">Mõnikord lõpetab organisatsioon konkreetsete soodustuste pakkumise.</span><span class="sxs-lookup"><span data-stu-id="cc214-138">Sometimes, an organization stops offering certain benefits.</span></span> <span data-ttu-id="cc214-139">Sellisel juhul peate soodustust ja selle saamiseks registreerunud töötajaid värskendama.</span><span class="sxs-lookup"><span data-stu-id="cc214-139">In this case, you must update the benefit and the workers who are enrolled in.</span></span> <span data-ttu-id="cc214-140">Hulgisoodustuse aegumine võimaldab teil korraga muuta nii soodustuse kui ka selleks soodustuseks töötajate registreerumise aegumiskuupäeva.</span><span class="sxs-lookup"><span data-stu-id="cc214-140">Mass benefit expiration lets you change the expiration date of both a benefit and the worker enrollments for that benefit at the same time.</span></span> <span data-ttu-id="cc214-141">Samuti saate valida mitut soodustuse saamiseks registreerunud töötajat ja muuta nende soodusperioodi lõppkuupäeva.</span><span class="sxs-lookup"><span data-stu-id="cc214-141">You can also select multiple workers who are enrolled in a benefit and change the ending date of their coverage.</span></span> 

<span data-ttu-id="cc214-142">Samuti võimaldab hulgisoodustuse pikendamine teil pikendada nii soodustuse kui ka selle saamiseks töötajate registreerumise aegumiskuupäeva, kui otsustate soodustust pakkuda kauem kui algselt plaanitud.</span><span class="sxs-lookup"><span data-stu-id="cc214-142">Similarly, mass benefit extension lets you extend the expiration date of both a benefit and the worker enrollments for that benefit if you decide to offer a benefit longer than you originally planned.</span></span>

<a name="additional-resources"></a><span data-ttu-id="cc214-143">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="cc214-143">Additional resources</span></span>
--------

[<span data-ttu-id="cc214-144">Soodustuse saamise õiguse eeskirjad</span><span class="sxs-lookup"><span data-stu-id="cc214-144">Benefit eligibility policies</span></span>](benefit-eligibility-policies.md)



