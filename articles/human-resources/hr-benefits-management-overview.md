---
title: Soodustuste halduse ülevaade
description: Rakenduse Dynamics 365 Human Resources soodustuste haldamise funktsiooni eelvaade. Pakkuge oma töötajatele hõlpsasti kasutatava võrgukasutuskogemusega laiendatud soodustuste võimalusi.
author: andreabichsel
manager: AnnBe
ms.date: 09/17/2020
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
ms.openlocfilehash: e2e8fcdd0b6124b459c4dc073e2929418d18bcc5
ms.sourcegitcommit: 084eda1d5503be83e97e2e428e67ef5393535fab
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/17/2020
ms.locfileid: "3819761"
---
# <a name="benefits-management-overview"></a><span data-ttu-id="ca654-104">Soodustuste haldamise ülevaade</span><span class="sxs-lookup"><span data-stu-id="ca654-104">Benefits management overview</span></span>

<span data-ttu-id="ca654-105">Konkurentsivõime säilitamiseks peate pakkuma parimate töövõtjate meelitamiseks ja säilitamiseks rikkalikku soodustuste komplekti.</span><span class="sxs-lookup"><span data-stu-id="ca654-105">To remain competitive, you must offer a rich set of benefits to attract and retain your best employees.</span></span> <span data-ttu-id="ca654-106">Lisaks tavapärastele soodustustele, nagu ravi- ja hambaravikindlustus, võite tahta pakkuda ka laiendatud teenuseid, nagu abi adopteerimisel, vabaajaprogrammid ja toetus töörõivaste jaoks.</span><span class="sxs-lookup"><span data-stu-id="ca654-106">In addition to standard benefits like medical and dental coverage, you might also want to offer expanded services like adoption assistance, recreation programs, and clothing allowances.</span></span> <span data-ttu-id="ca654-107">Rakenduse Microsoft Dynamics 365 Human Resources soodustuste haldus pakub paindlikku lahendust, mis toetab mitmesuguseid soodustuste võimalusi.</span><span class="sxs-lookup"><span data-stu-id="ca654-107">Benefits management in Microsoft Dynamics 365 Human Resources provides you with a flexible solution that supports a wide variety of benefit options.</span></span> <span data-ttu-id="ca654-108">Human Resources sisaldab ka hõlpsasti kasutatavat töövõtja kogemust, mis teie pakutavat tutvustab.</span><span class="sxs-lookup"><span data-stu-id="ca654-108">Human Resources also includes an easy-to-use employee experience that showcases your offerings.</span></span>

- <span data-ttu-id="ca654-109">Täiustatud soodustuse plaanid võimaldavad teil luua ja hallata ainulaadseid soodustuse plaane ning toetada keerukaid soodustuse tabeleid ja pesastatud tasemeid.</span><span class="sxs-lookup"><span data-stu-id="ca654-109">Enhanced benefits plans let you create and manage unique benefit plans and support complex benefit rate tables and nested tiers.</span></span> <span data-ttu-id="ca654-110">Saate lihtsama töövõtja kogemuse jaoks hõlpsalt luua soodustusprogramme, kogumeid ja automaatse registreerimise reegleid.</span><span class="sxs-lookup"><span data-stu-id="ca654-110">You can easily create benefit programs, bundles, and auto-enrollment rules for an easier employee experience.</span></span>

- <span data-ttu-id="ca654-111">Paindliku krediidiga programmid võimaldavad proportsionaalselt jaotada pensioni- ja teiste elusündmuste toetusi.</span><span class="sxs-lookup"><span data-stu-id="ca654-111">Flex credit programs let you prorate to support retirement and other life events.</span></span>

- <span data-ttu-id="ca654-112">Ulatuslikud sobivusreeglid tagavad, et muudate õigeid soodustused kättesaadavaks õigetele töötajatele.</span><span class="sxs-lookup"><span data-stu-id="ca654-112">Extensive eligibility rules ensure you make the right benefits available to the right employees.</span></span>

- <span data-ttu-id="ca654-113">Veebipõhine soodustuste registreerimine tagab teie töövõtjatele lihtsa kogemuse.</span><span class="sxs-lookup"><span data-stu-id="ca654-113">Online benefits enrollment provides an easy experience for your employees.</span></span>

- <span data-ttu-id="ca654-114">Kvalifitseeritud elusündmuse töötlemine toetab tulevasi elusündmusi.</span><span class="sxs-lookup"><span data-stu-id="ca654-114">Qualified life event processing supports future life events.</span></span>

<span data-ttu-id="ca654-115">Kui soovite ligipääsu demoandmetelel, peate oma liivakastikeskkonna uuesti juurutama.</span><span class="sxs-lookup"><span data-stu-id="ca654-115">If you would like to access the demo data, you'll need to redeploy your sandbox environment.</span></span>

## <a name="enable-benefits-management"></a><span data-ttu-id="ca654-116">Soodustuste halduse lubamine</span><span class="sxs-lookup"><span data-stu-id="ca654-116">Enable Benefits management</span></span>

<span data-ttu-id="ca654-117">Selles teemas kirjeldatakse, kuidas funktsioone rakenduses Human Resources sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="ca654-117">This topic describes how to turn on features in Human Resources.</span></span> <span data-ttu-id="ca654-118">Lisaks annab see teada, millised rakenduse Human Resources olemasolevad funktsioonid soodustuste haldamine asendab või keelab, kui lülitate soodustuste haldamise sisse.</span><span class="sxs-lookup"><span data-stu-id="ca654-118">It also tells which existing features in Human Resources that Benefits management replaces or are disabled once you turn on Benefits management.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ca654-119">Keskkonnas **Tootmine** ei saa soodustuste haldust keelata, kui olete selle lubanud.</span><span class="sxs-lookup"><span data-stu-id="ca654-119">After you enable Benefits management in a **Production** environment, you can't disable it.</span></span> <span data-ttu-id="ca654-120">Enne soodustuste halduse keskkonnas **Tootmine** lubamist soovitame lubada ja testida soodustuste haldust keskkonnas **Liivakast**.</span><span class="sxs-lookup"><span data-stu-id="ca654-120">We recommend enabling and testing Benefits management in a **Sandbox** environment before enabling it in a **Production** environment.</span></span> <span data-ttu-id="ca654-121">Olemasolevate pärandsoodustuse funktsioonide ja uute pärandsoodustuse funktsioonide vahel on olulisi erinevusi, mis vajavad täiendavat seadistamist ja mida tuleks enne tootmise alustamist testida.</span><span class="sxs-lookup"><span data-stu-id="ca654-121">There are significant differences between the legacy Benefit functionality and new Benefits management functionality that require additional setup and should be tested prior to being placed into production.</span></span>

- [<span data-ttu-id="ca654-122">Funktsioonide haldamine</span><span class="sxs-lookup"><span data-stu-id="ca654-122">Manage features</span></span>](hr-admin-manage-features.md)

## <a name="configure-employee-information"></a><span data-ttu-id="ca654-123">Töötaja teabe konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="ca654-123">Configure employee information</span></span>

<span data-ttu-id="ca654-124">Enne eeliste andmist töötajatele peate sisestama nõutava teabe.</span><span class="sxs-lookup"><span data-stu-id="ca654-124">Before you can enroll employees in benefits, you must provide required information.</span></span> <span data-ttu-id="ca654-125">Peate töötaja lisama **põhipalgaplaanile** nende töötamise alguskuupäeval ning vormi **Töötaja** väljal **Tööhõive üksikasjad** peate valima **Soodustuse maksesagedus**.</span><span class="sxs-lookup"><span data-stu-id="ca654-125">You must enroll an employee in a **Fixed compensation plan** on their start date, and you must select a **Benefit pay frequency** in **Employment details** on the **Worker** form.</span></span>

<span data-ttu-id="ca654-126">Kui teil on töötaja, kes saab lisahüvitust (nt komisjonitasud), saate lisada summa **Soodustuste aastane palgasumma** töövõtja kirjesse.</span><span class="sxs-lookup"><span data-stu-id="ca654-126">If you have an employee who receives supplemental compensation like commissions, you can add a **Benefits annual salary** amount from the employee record.</span></span> <span data-ttu-id="ca654-127">Human Resources kasutab summat **Soodustuse aastane palgasumma** kindlustussummade määramiseks aastase põhipalga summa asemel.</span><span class="sxs-lookup"><span data-stu-id="ca654-127">Human Resources will use the **Benefits annual salary** amount when determining coverage amounts, instead of the fixed compensation annual amount.</span></span> <span data-ttu-id="ca654-128">**Soodustuste aastane palgasumma** peab kehtima alates töövõtja alustamise kuupäevast või soodustuse perioodi algusest, olenevalt sellest, kumb on hilisem.</span><span class="sxs-lookup"><span data-stu-id="ca654-128">The **Benefits annual salary** must be valid as of the employee’s start date or the beginning of the benefit period, whichever is latest.</span></span> <span data-ttu-id="ca654-129">Kui töövõtja kohta kirjendatakse nii põhipalk soodustuste aastane palgasumma, kasutatakse kindlustuse summade määramisel soodustuste aastast palgasummat.</span><span class="sxs-lookup"><span data-stu-id="ca654-129">If both a fixed compensation and benefits annual salary amount is recorded for an employee, the benefits annual salary will be used in determining coverage amounts.</span></span>

<span data-ttu-id="ca654-130">Kui loote soodustusplaani, mis kasutab sool või vanusel põhinevaid määrasid, peate soodustuse maksumuse arvutamiseks sisestama töötaja sünnikuupäeva ja soo.</span><span class="sxs-lookup"><span data-stu-id="ca654-130">When you create a benefit plan that uses rates that are based on gender or age, you must enter a birth date and gender for the employee to calculate the benefit cost.</span></span>

## <a name="configure-benefits-management"></a><span data-ttu-id="ca654-131">Soodustuste halduse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="ca654-131">Configure Benefits management</span></span>

<span data-ttu-id="ca654-132">Enne kui saate oma töötajate jaoks soodustuse plaane luua, tuleb teil plaanide valikud konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="ca654-132">Before you can create benefit plans for your employees, you need to configure options for the plans.</span></span>

- [<span data-ttu-id="ca654-133">Soodustuste halduse parameetrite määramine</span><span class="sxs-lookup"><span data-stu-id="ca654-133">Set Benefits management parameters</span></span>](hr-benefits-setup-parameters.md)
- [<span data-ttu-id="ca654-134">Sobivusreeglite ja suvandite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="ca654-134">Configure eligibility rules and options</span></span>](hr-benefits-setup-eligibility-rules.md)
- [<span data-ttu-id="ca654-135">Isiklike kontaktide sobivuse suvandite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="ca654-135">Configure personal contact eligibility options</span></span>](hr-benefits-setup-contact-eligibility-options.md)
- [<span data-ttu-id="ca654-136">Katvuse suvandite loomine</span><span class="sxs-lookup"><span data-stu-id="ca654-136">Create coverage options</span></span>](hr-benefits-setup-coverage-options.md)
- [<span data-ttu-id="ca654-137">Maksesageduste häälestamine</span><span class="sxs-lookup"><span data-stu-id="ca654-137">Set up payment frequencies</span></span>](hr-benefits-setup-payment-frequencies.md)
- [<span data-ttu-id="ca654-138">Elusündmuse tüüpide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="ca654-138">Configure life event types</span></span>](hr-benefits-setup-life-event-types.md)
- [<span data-ttu-id="ca654-139">Plaani tüüpide loomine</span><span class="sxs-lookup"><span data-stu-id="ca654-139">Create plan types</span></span>](hr-benefits-setup-plan-types.md)
- [<span data-ttu-id="ca654-140">Põhjusekoodide häälestamine</span><span class="sxs-lookup"><span data-stu-id="ca654-140">Set up reason codes</span></span>](hr-benefits-setup-reason-codes.md)
- [<span data-ttu-id="ca654-141">Järgukoodide häälestamine</span><span class="sxs-lookup"><span data-stu-id="ca654-141">Set up tier codes</span></span>](hr-benefits-setup-tier-codes.md)
- [<span data-ttu-id="ca654-142">Määrade konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="ca654-142">Configure rates</span></span>](hr-benefits-setup-rates.md)
- [<span data-ttu-id="ca654-143">Mahaarvamiste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="ca654-143">Configure deductions</span></span>](hr-benefits-setup-deductions.md)
- [<span data-ttu-id="ca654-144">Ootepäevade konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="ca654-144">Configure waiting days</span></span>](hr-benefits-setup-waiting-days.md)
- [<span data-ttu-id="ca654-145">Ooteperioodide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="ca654-145">Configure waiting periods</span></span>](hr-benefits-setup-waiting-periods.md)
- [<span data-ttu-id="ca654-146">Ümardamisreeglite häälestus</span><span class="sxs-lookup"><span data-stu-id="ca654-146">Set up rounding rules</span></span>](hr-benefits-setup-rounding-rules.md)
- [<span data-ttu-id="ca654-147">Töötajate kategooriate loomine</span><span class="sxs-lookup"><span data-stu-id="ca654-147">Create employment categories</span></span>](hr-benefits-setup-employment-categories.md)
- [<span data-ttu-id="ca654-148">Tööhõive tüüpide seadistamine</span><span class="sxs-lookup"><span data-stu-id="ca654-148">Set up employment types</span></span>](hr-benefits-setup-employment-types.md)
- [<span data-ttu-id="ca654-149">Töövõtja iseteeninduse konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="ca654-149">Configure employee self service</span></span>](hr-benefits-setup-employee-self-service.md)

## <a name="create-benefit-plans"></a><span data-ttu-id="ca654-150">Soodustuse plaanide loomine</span><span class="sxs-lookup"><span data-stu-id="ca654-150">Create benefit plans</span></span>

<span data-ttu-id="ca654-151">Need artiklid näitavad, kuidas luua soodustuse plaane, kaasa arvatud kogumid ja paindliku krediidiga programmid.</span><span class="sxs-lookup"><span data-stu-id="ca654-151">These articles show how to create benefit plans, including bundles and flex credit programs.</span></span>

- [<span data-ttu-id="ca654-152">Soodustusplaanide seadistamine</span><span class="sxs-lookup"><span data-stu-id="ca654-152">Set up benefit plans</span></span>](hr-benefits-plans-setup.md)
- [<span data-ttu-id="ca654-153">Paindkrediidi programmide seadistamine</span><span class="sxs-lookup"><span data-stu-id="ca654-153">Set up flex credit programs</span></span>](hr-benefits-plans-flex-credit-programs.md)

## <a name="process-benefit-plans"></a><span data-ttu-id="ca654-154">Soodustusplaanide töötlemine</span><span class="sxs-lookup"><span data-stu-id="ca654-154">Process benefit plans</span></span>

<span data-ttu-id="ca654-155">Nende aktiivseks muutmiseks peate osasid muudatusi töötlema.</span><span class="sxs-lookup"><span data-stu-id="ca654-155">You need to process some of your changes to make them active.</span></span>

- [<span data-ttu-id="ca654-156">Registreerimise sobivuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="ca654-156">Process enrollment eligibility</span></span>](hr-benefits-process-enrollment-eligibility.md)
- [<span data-ttu-id="ca654-157">Elusündmuste töötlemine</span><span class="sxs-lookup"><span data-stu-id="ca654-157">Process life events</span></span>](hr-benefits-process-life-events.md)
- [<span data-ttu-id="ca654-158">Elusündmuste muutuste töötlemine</span><span class="sxs-lookup"><span data-stu-id="ca654-158">Process life event changes</span></span>](hr-benefits-process-life-event-changes.md)
- [<span data-ttu-id="ca654-159">Elusündmuse sobivuse töötlemine</span><span class="sxs-lookup"><span data-stu-id="ca654-159">Process life event eligibility</span></span>](hr-benefits-process-life-event-eligibility.md)
- [<span data-ttu-id="ca654-160">Määrade muudatuste töötlemine</span><span class="sxs-lookup"><span data-stu-id="ca654-160">Process rate changes</span></span>](hr-benefits-process-rate-changes.md)

