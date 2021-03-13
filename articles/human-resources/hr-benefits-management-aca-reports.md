---
title: Taskukohase ravikindlustuse eelnõu (ACA) aruannete koostamine soodustuste halduses
description: Käesolevas teemas kirjeldatakse, kuidas Soodustuste haldus aitab jälgida teavet, mis on esitatud Taskukohase ravikindlustuse eelnõu (ACA) tööandja kohustuse vormidega 1095-B ja 1095-C.
author: andreabichsel
manager: tfehr
ms.date: 12/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-12-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 2e4b250f4a059719067a9e19bbf3ce4aecc9bb1f
ms.sourcegitcommit: ea2d652867b9b83ce6e5e8d6a97d2f9460a84c52
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/03/2021
ms.locfileid: "5112268"
---
# <a name="generate-aca-reports-in-benefits-management"></a><span data-ttu-id="6e315-103">ACA-aruannete loomine soodustuste halduses</span><span class="sxs-lookup"><span data-stu-id="6e315-103">Generate ACA reports in Benefits management</span></span>

<span data-ttu-id="6e315-104">Soodustuste haldus aitab jälgida teavet, mis on esitatud Taskukohase ravikindlustuse eelnõu (ACA) tööandja kohustuse vormidega 1095-B ja 1095-C.</span><span class="sxs-lookup"><span data-stu-id="6e315-104">Benefits management helps you track information that is reported on Form 1095-B and Form 1095-C for the Affordable Care Act (ACA) employer mandate.</span></span> <span data-ttu-id="6e315-105">Nagu ka ACA aruandluse võimalused vanas tööruumis **Soodustused**, kehtib see funktsioon ainult USA juriidilistele isikutele.</span><span class="sxs-lookup"><span data-stu-id="6e315-105">Like the ACA reporting capability in the old **Benefits** workspace, this functionality applies only to legal entities in the United States.</span></span>

<span data-ttu-id="6e315-106">Selle funktsiooni kasutamiseks peate esmalt lülitama sisse suvandi **Täpsem soodustuste haldus**.</span><span class="sxs-lookup"><span data-stu-id="6e315-106">To use this functionality, you must first turn on **Advanced Benefits Management**.</span></span> <span data-ttu-id="6e315-107">Lisateavet, sealhulgas olulisi hoiatusi soodustuste halduse kohta leiate jaotisest [Soodustuste halduse lubamine või keelamine](hr-admin-manage-features.md#enable-or-disable-benefits-management).</span><span class="sxs-lookup"><span data-stu-id="6e315-107">For more information, including important caveats about Benefits management, see [Enable or disable Benefits management](hr-admin-manage-features.md#enable-or-disable-benefits-management).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6e315-108">ACA-aruandlust saate kasutada ainult kas tööruumist **Soodustuste haldus** või vanast tööruumist **Eelised**, mitte mõlemast.</span><span class="sxs-lookup"><span data-stu-id="6e315-108">You can use ACA reporting only from either the **Benefits management** workspace or the old **Benefits** workspace, not from both.</span></span> <span data-ttu-id="6e315-109">Näiteks kui lülitasite Soodustuste haldusele, on ACA aruandlus saadaval ainult tööruumis **Soodustuste haldus**, mitte vanas tööruumis **Soodustused**.</span><span class="sxs-lookup"><span data-stu-id="6e315-109">For example, if you switched to Benefits management, ACA reporting is available only from the **Benefits management** workspace, not from the old **Benefits** workspace.</span></span>
>
> <span data-ttu-id="6e315-110">Kui lülitute Soodustuste haldusele registreerimisaasta keskel, peate töötajata andmed soodustuste halduses kogu aasta jaoks õigesti konfigureerima.</span><span class="sxs-lookup"><span data-stu-id="6e315-110">If you switch to Benefits management in the middle of an enrollment year, you must correctly configure employee data for the whole year in Benefits management.</span></span> <span data-ttu-id="6e315-111">Sedasi tagate, et saate kogu aasta kohta õige aruandeteabe.</span><span class="sxs-lookup"><span data-stu-id="6e315-111">In this way, you ensure that you will receive accurate reporting information for the whole year.</span></span>

## <a name="getting-started"></a><span data-ttu-id="6e315-112">Alustamine</span><span class="sxs-lookup"><span data-stu-id="6e315-112">Getting started</span></span>

<span data-ttu-id="6e315-113">1095-vormide jaoks andmete jälgimiseks looge kõigepealt üks või rohkem ravikindlustusega hõlmatud gruppi.</span><span class="sxs-lookup"><span data-stu-id="6e315-113">To track information for 1095 forms, first create one or more Affordable Care coverage groups.</span></span> <span data-ttu-id="6e315-114">Need grupid näitavad järgmist teavet.</span><span class="sxs-lookup"><span data-stu-id="6e315-114">These groups indicate the following information:</span></span>

- <span data-ttu-id="6e315-115">Töötajale antud kindlustuspakkumine</span><span class="sxs-lookup"><span data-stu-id="6e315-115">The offer of coverage that was provided to an employee</span></span>
- <span data-ttu-id="6e315-116">Töötaja osa madalaima maksumusega kuumaksest, kui kulu ületab föderaalset vaesuspiiri</span><span class="sxs-lookup"><span data-stu-id="6e315-116">The employee's share of the lowest-cost monthly premium, if the cost is above the federal poverty line</span></span>
- <span data-ttu-id="6e315-117">Tööandja kasutatav Safe Harbor, kui see on kohaldatav</span><span class="sxs-lookup"><span data-stu-id="6e315-117">The safe harbor that is used by the employer, if applicable</span></span>

<span data-ttu-id="6e315-118">Ravikindlustusega hõlmatud grupid aitavad teil hallata neid andmeid mitme töötaja kirjete kohta, millel on samad tingimused.</span><span class="sxs-lookup"><span data-stu-id="6e315-118">Affordable Care coverage groups help you manage this information for multiple employee records that have the same conditions.</span></span> <span data-ttu-id="6e315-119">Saate kerge vaevaba määrata gruppe ühele või rohkemale töötajale.</span><span class="sxs-lookup"><span data-stu-id="6e315-119">You can easily assign groups to one or more employees.</span></span>

### <a name="create-or-edit-an-affordable-care-coverage-group"></a><span data-ttu-id="6e315-120">Ravikindlustusega hõlmatud grupi loomine või redigeerimine</span><span class="sxs-lookup"><span data-stu-id="6e315-120">Create or edit an Affordable Care coverage group</span></span>

1. <span data-ttu-id="6e315-121">Valige tööruumis **Soodustuste haldus** valik **Ravikindlustusega hõlmatud grupp**.</span><span class="sxs-lookup"><span data-stu-id="6e315-121">In the **Benefits management** workspace, select **Affordable Care coverage group**.</span></span>

    ![Ravikindlustusega hõlmatud grupi valimine](./media/hr-benefits-management-aca-coverage-group.png)

2. <span data-ttu-id="6e315-123">Uue ravikindlustusega hõlmatud grupi loomiseks valige **Uus** või olemasoleva grupi redigeerimiseks valige **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="6e315-123">Select **New** to create a new Affordable Care coverage group or **Edit** to change an existing group.</span></span>

    ![Uue või Redigeerimise valik](./media/hr-benefits-management-aca-new.png)

3. <span data-ttu-id="6e315-125">Seadistage järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="6e315-125">Set the following fields.</span></span>

    | <span data-ttu-id="6e315-126">Field</span><span class="sxs-lookup"><span data-stu-id="6e315-126">Field</span></span> | <span data-ttu-id="6e315-127">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="6e315-127">Description</span></span> |
    |---|---|
    | <span data-ttu-id="6e315-128">Nimi</span><span class="sxs-lookup"><span data-stu-id="6e315-128">Name</span></span> | <span data-ttu-id="6e315-129">Sisestage grupile nimi.</span><span class="sxs-lookup"><span data-stu-id="6e315-129">Enter a name for the group.</span></span> |
    | <span data-ttu-id="6e315-130">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="6e315-130">Description</span></span> | <span data-ttu-id="6e315-131">Saate sisestada grupi kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="6e315-131">Enter a description of the group.</span></span> |
    | <span data-ttu-id="6e315-132">Katvuse pakkumine</span><span class="sxs-lookup"><span data-stu-id="6e315-132">Offer of coverage</span></span> | <span data-ttu-id="6e315-133">Töötajatele, nende abikaasale või partnerile ja nende ülalpeetavatele pakutav kindlustuskaitse.</span><span class="sxs-lookup"><span data-stu-id="6e315-133">The coverage that is offered to employees, their spouse or partner, and their dependents.</span></span> |
    | <span data-ttu-id="6e315-134">Töötaja kulu osa</span><span class="sxs-lookup"><span data-stu-id="6e315-134">Employee share of cost</span></span> | <span data-ttu-id="6e315-135">Summa, mille eest vastutab töötaja.</span><span class="sxs-lookup"><span data-stu-id="6e315-135">The amount that the employee is responsible for.</span></span> |
    | <span data-ttu-id="6e315-136">Kohaldatav jaotis 4980H Safe Harbor</span><span class="sxs-lookup"><span data-stu-id="6e315-136">Applicable section 4980H safe harbor</span></span> | <span data-ttu-id="6e315-137">4980H Safe Harbori või ülemineku leevenduse kood.</span><span class="sxs-lookup"><span data-stu-id="6e315-137">The 4980H safe harbor or transition relief code.</span></span> |
    | <span data-ttu-id="6e315-138">Plaani alguskuu</span><span class="sxs-lookup"><span data-stu-id="6e315-138">Plan start month</span></span> | <span data-ttu-id="6e315-139">Valige kalendrikuu, millal teie soodustusplaani aasta algab.</span><span class="sxs-lookup"><span data-stu-id="6e315-139">Select the calendar month when your benefit plan year begins.</span></span> |
    | <span data-ttu-id="6e315-140">Grupp kehtib alates</span><span class="sxs-lookup"><span data-stu-id="6e315-140">Group valid from</span></span> | <span data-ttu-id="6e315-141">Esimene kuupäev, millal see kirje kehtib.</span><span class="sxs-lookup"><span data-stu-id="6e315-141">The first date when this record is valid.</span></span> |
    | <span data-ttu-id="6e315-142">Grupp kehtib kuni</span><span class="sxs-lookup"><span data-stu-id="6e315-142">Group valid through</span></span> | <span data-ttu-id="6e315-143">Viimane kuupäev, millal see kirje kehtib.</span><span class="sxs-lookup"><span data-stu-id="6e315-143">The last date when this record is valid.</span></span> <span data-ttu-id="6e315-144">Kui aegumiskuupäev puudub, sisestage **Mitte kunagi**.</span><span class="sxs-lookup"><span data-stu-id="6e315-144">If there is no expiration date, enter **Never**.</span></span> |

    ![Kindlustuskaitse grupi loomine](./media/hr-benefits-management-aca-new-group.png)

4. <span data-ttu-id="6e315-146">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="6e315-146">Select **Save**.</span></span>

### <a name="assign-multiple-employees-to-an-affordable-care-coverage-group"></a><span data-ttu-id="6e315-147">Mitme töötaja määramine ravikindlustusega hõlmatud gruppi</span><span class="sxs-lookup"><span data-stu-id="6e315-147">Assign multiple employees to an Affordable Care coverage group</span></span>

1. <span data-ttu-id="6e315-148">Valige tööruumis **Soodustuste haldus** valik **Ravikindlustusega hõlmatud grupp**.</span><span class="sxs-lookup"><span data-stu-id="6e315-148">In the **Benefits management** workspace, select **Affordable Care coverage group**.</span></span>
2. <span data-ttu-id="6e315-149">Valige grupp, millele töötajaid määrata.</span><span class="sxs-lookup"><span data-stu-id="6e315-149">Select the group to assign employees to.</span></span>
3. <span data-ttu-id="6e315-150">Valige **Massiline määramine**.</span><span class="sxs-lookup"><span data-stu-id="6e315-150">Select **Mass assignment**.</span></span>

    ![Massilise määramise valimine](./media/hr-benefits-management-aca-mass-assignment.png)

4. <span data-ttu-id="6e315-152">Valige loendist töötajad ja seejärel valige käsk **Määra**.</span><span class="sxs-lookup"><span data-stu-id="6e315-152">Select employees in the list, and then select **Assign**.</span></span>

    ![Valitud töötajate määramine gruppi.](./media/hr-benefits-management-aca-assign-coverage-group.png)

## <a name="maintain-multiple-versions-of-coverage-options"></a><span data-ttu-id="6e315-154">Mitme kindlustuskaitse valiku säilitamine</span><span class="sxs-lookup"><span data-stu-id="6e315-154">Maintain multiple versions of coverage options</span></span>

<span data-ttu-id="6e315-155">Saate säilitada mistahes kindlustuskaitse grupist mitu versiooni.</span><span class="sxs-lookup"><span data-stu-id="6e315-155">You can maintain multiple versions of any coverage group.</span></span> <span data-ttu-id="6e315-156">Kui teie organisatsioonis või teie pakutavates soodustustes midagi muutub, saate hoida grupi andmed ajakohased ilma, et peaksite looma uue grupi ja määrama töötajad sinna ümber.</span><span class="sxs-lookup"><span data-stu-id="6e315-156">When something changes in your organization or the benefits that are offered, you can keep the group's information up to date without having to create a new group and reassign employees to it.</span></span>

<span data-ttu-id="6e315-157">Kui olete ravikindlustusega hõlmatud grupid loonud, saate neisse töötajaid hulgi määrata.</span><span class="sxs-lookup"><span data-stu-id="6e315-157">After you've created Affordable Care coverage groups, you can mass-assign employees to them.</span></span> <span data-ttu-id="6e315-158">Saate töötajaid gruppidesse ka ükshaaval määrata ning näidata, kas ACA teavet jälgitakse ja esitatakse.</span><span class="sxs-lookup"><span data-stu-id="6e315-158">You can also individually assign employees to groups, and indicate whether ACA information is tracked and reported.</span></span>

<span data-ttu-id="6e315-159">Kui te ei pea töötaja ACA-teavet jälgima ja esitama, saate määrata suvandi **Kindlustuskaitse aruandlus** väärtuseks **Ei**.</span><span class="sxs-lookup"><span data-stu-id="6e315-159">If you don't have to track and report ACA information for an employee, you can set the **Report coverage** option to **No**.</span></span> <span data-ttu-id="6e315-160">Näiteks võivad teil olla osalise tööajaga töötajad, kes ei vaja ACA-aruandlust.</span><span class="sxs-lookup"><span data-stu-id="6e315-160">For example, you might have part-time employees who don't require ACA reporting.</span></span>

### <a name="override-default-values-for-an-employee"></a><span data-ttu-id="6e315-161">Töötaja vaikeväärtuste alistamine</span><span class="sxs-lookup"><span data-stu-id="6e315-161">Override default values for an employee</span></span>

<span data-ttu-id="6e315-162">Töötajate puhul, kes on määratud ravikindlustusega hõlmatud gruppi, saate kõigi kuude jaoks, mis vajavad erinevaid väärtusi, muuta järgmisi suvandeid.</span><span class="sxs-lookup"><span data-stu-id="6e315-162">For employees who are assigned to an Affordable Care coverage group, you can change the following options for any months that require different values:</span></span>

- <span data-ttu-id="6e315-163">Katvuse pakkumine</span><span class="sxs-lookup"><span data-stu-id="6e315-163">Offer of coverage</span></span>
- <span data-ttu-id="6e315-164">Töötaja kulu osa</span><span class="sxs-lookup"><span data-stu-id="6e315-164">Employee share of cost</span></span>
- <span data-ttu-id="6e315-165">Kohaldatav jaotis 4980H Safe Harbor</span><span class="sxs-lookup"><span data-stu-id="6e315-165">Applicable section 4980H safe harbor</span></span>

> [!NOTE]
> <span data-ttu-id="6e315-166">2020 ACA-aruannete puhul tuleb vormil 1095-C esitada nii töö kui ka kodu sihtnumbrid.</span><span class="sxs-lookup"><span data-stu-id="6e315-166">For 2020 ACA reports, you must report both work and home ZIP Codes on Form 1095-C.</span></span> <span data-ttu-id="6e315-167">Väärtused täidetakse praeguste aktiivsete asukohtade alusel automaatselt.</span><span class="sxs-lookup"><span data-stu-id="6e315-167">Values are automatically filled in, based on current active locations.</span></span> <span data-ttu-id="6e315-168">Kui kumbki asukoht oli aasta mis tahes osal erinev, peate väärtuse alistama.</span><span class="sxs-lookup"><span data-stu-id="6e315-168">If either location was different during any part of the year, you must override the value.</span></span> <span data-ttu-id="6e315-169">1095-C aruande väli **Sihtnumber** (rida 17) täidetakse ainult siis, kui kood **Kindlustuspakkumine** sisaldab väärtusi **1L** kuni **1Q** järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="6e315-169">The **ZIP Code** field (line 17) of the 1095-C report is filled in only if the **Offer of coverage** code contains **1L** through **1Q**, as follows:</span></span>
>
> - <span data-ttu-id="6e315-170">**1L, 1M või 1N:** esmane elukoha sihtnumber</span><span class="sxs-lookup"><span data-stu-id="6e315-170">**1L, 1M, or 1N:** The primary residence ZIP Code</span></span>
> - <span data-ttu-id="6e315-171">**1O, 1P, 1Q:** esmane töökoha sihtnumber</span><span class="sxs-lookup"><span data-stu-id="6e315-171">**1O, 1P, 1Q:** The primary work ZIP Code</span></span>

<span data-ttu-id="6e315-172">Ravikindlustusega hõlmatud grupi mistahes väärtustele erandite sisestamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="6e315-172">To enter exceptions for any values of an Affordable Care coverage group, follow these steps.</span></span>

1. <span data-ttu-id="6e315-173">Valige tööruumis **Personalihaldus** suvand **Lingid** ja seejärel **Töötajad**.</span><span class="sxs-lookup"><span data-stu-id="6e315-173">In the **Personnel management** workspace, select **Links**, and then select **Workers**.</span></span>
2. <span data-ttu-id="6e315-174">Valige loendist töötaja.</span><span class="sxs-lookup"><span data-stu-id="6e315-174">Select the employee in the list.</span></span>
3. <span data-ttu-id="6e315-175">Valige vahekaardi **Tööhõive** jaotises **Lisateave** suvand **Ravikindlustuskaitse**.</span><span class="sxs-lookup"><span data-stu-id="6e315-175">On the **Employment** tab, in the **More information** section, select **Affordable Care coverage**.</span></span>

    ![Ühe töötaja valikute muutmine](./media/hr-benefits-management-aca-change-single-employee.png)

4. <span data-ttu-id="6e315-177">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="6e315-177">Select **Edit**.</span></span>
5. <span data-ttu-id="6e315-178">Iga kuu puhul, mis nõuab muudatusi, valige märkeruut **Vaikesätete alistamine** ja seejärel muutke vajadusel muid väärtusi.</span><span class="sxs-lookup"><span data-stu-id="6e315-178">For each month that requires changes, select the **Override default** check box, and then change the other values as required.</span></span>

    ![Vaikeväärtuste alistamine](./media/hr-benefits-management-aca-override-default.png)

6. <span data-ttu-id="6e315-180">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="6e315-180">Select **Save**.</span></span>

## <a name="report-health-care-coverage"></a><span data-ttu-id="6e315-181">Tervisekindlustuskaitse aruandlus</span><span class="sxs-lookup"><span data-stu-id="6e315-181">Report health care coverage</span></span>

<span data-ttu-id="6e315-182">Peate jälgima täiskohaga ja osalise tööajaga töötajate mistahes töötaja toetusega töötaja enda kindlustuskaitset.</span><span class="sxs-lookup"><span data-stu-id="6e315-182">You must track any employer-sponsored, self-insured health care coverage for full-time and part-time employees.</span></span> <span data-ttu-id="6e315-183">Lisage aruandele 1095-C kõik töötajad ja nende ülalpeetavad nende kuude kohta, millal neil kindlustuskaitse oli.</span><span class="sxs-lookup"><span data-stu-id="6e315-183">Include each employee, together with their dependents, on the 1095-C report for the months when they were covered.</span></span>

<span data-ttu-id="6e315-184">Et näidata, kas soodustusplaanist tuleb teatada, järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="6e315-184">To indicate whether a benefit plan must be reported, follow these steps.</span></span>

1. <span data-ttu-id="6e315-185">Valige tööruumis **Soodustuste haldus** suvand **Soodustusplaanid**.</span><span class="sxs-lookup"><span data-stu-id="6e315-185">In the **Benefits management** workspace, select **Benefit plans**.</span></span>
2. <span data-ttu-id="6e315-186">Valige aruande soodustusplaan.</span><span class="sxs-lookup"><span data-stu-id="6e315-186">Select the benefit plan to report.</span></span>
3. <span data-ttu-id="6e315-187">Valige suvand **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="6e315-187">Select **Edit**.</span></span>
4. <span data-ttu-id="6e315-188">Seadke suvandi **Taskukohase ravikindlustuse eelnõu aruanne** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="6e315-188">Set the **Reported under the Affordable Care Act** option to **Yes**.</span></span>

    ![Tervisekindlustuse registreerimine](./media/hr-benefits-management-aca-report-coverage.png)

5. <span data-ttu-id="6e315-190">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="6e315-190">Select **Save**.</span></span>

<span data-ttu-id="6e315-191">Kui töötaja valib ülalpeetavale tervisekindlustuskaitse, määratakse ülalpeetava tervisekindlustuse kaitse periood kuupäeva järgi, millal ülalpeetav liideti või eemaldati.</span><span class="sxs-lookup"><span data-stu-id="6e315-191">If an employee chooses health care coverage for a dependent, the dependent's coverage period is determined by the date when the dependent was enrolled or removed.</span></span> <span data-ttu-id="6e315-192">Kindlustuskaitse kuupäevad arvestatakse ülalpeetavatele vastavalt perioodile, millal ülalpeetav oli liitumisaastal plaani jaoks sobiv ja aktiivne.</span><span class="sxs-lookup"><span data-stu-id="6e315-192">Coverage dates for dependents are automatically calculated based on the period when the dependent was eligible and active in a plan during the enrollment year.</span></span>

## <a name="generate-1095-b-and-1095-c-forms"></a><span data-ttu-id="6e315-193">Vormide 1095-B ja 1095-C loomine</span><span class="sxs-lookup"><span data-stu-id="6e315-193">Generate 1095-B and 1095-C forms</span></span>

<span data-ttu-id="6e315-194">Saate luua ka vormid 1095-B ja 1095-C ning jaotada need igale töötajale.</span><span class="sxs-lookup"><span data-stu-id="6e315-194">You can generate ACA 1095-B and 1095-C forms, and then distribute them to each of your employees.</span></span> <span data-ttu-id="6e315-195">Võite vormi 1095-C ja vastavad 1094-C edastusfailid luua ka elektrooniliselt ning saate need IRS-ile.</span><span class="sxs-lookup"><span data-stu-id="6e315-195">You can also electronically generate Form 1095-C and the corresponding 1094-C transmittal files to send to the Internal Revenue Service (IRS).</span></span>

1. <span data-ttu-id="6e315-196">Valige tööruumis **Soodustuste haldus** kas **vorm ACA 1095-B** või **vorm ACA 1095-C**.</span><span class="sxs-lookup"><span data-stu-id="6e315-196">In the **Benefits management** workspace, select **ACA 1095-B form** or **ACA 1095-C form**.</span></span>
2. <span data-ttu-id="6e315-197">Muutke parameetreid vastavalt vajadusele ja valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="6e315-197">Change the parameters as required, and then select **OK**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6e315-198">Rohkem kui 500 töötaja 1095-C vormi printimisel saate rohkem kui ühe PDF-faili.</span><span class="sxs-lookup"><span data-stu-id="6e315-198">If you're printing 1095-C forms for more than 500 employees, you will receive more than one PDF file.</span></span> <span data-ttu-id="6e315-199">Soovitame suurendada välja **Maksimaalne failisuurus megabaitides** väärtust lehel **Dokumendihalduse parameetrid** väärtusele **150**.</span><span class="sxs-lookup"><span data-stu-id="6e315-199">We recommend that you increase the value of the **Maximum file size in megabytes** field on the **Document management parameters** page to **150**.</span></span> <span data-ttu-id="6e315-200">(Selle lehe kiireks avamiseks saate kasutada navigeerimisriba otsinguvälja.)</span><span class="sxs-lookup"><span data-stu-id="6e315-200">(To quickly open that page, you can use the search field on the navigation bar.)</span></span>
    >
    > ![Maksimaalse failisuuruse muutmine](./media/hr-benefits-management-aca-maximum-file-size.png)

3. <span data-ttu-id="6e315-202">Aruannete oleku kontrollimiseks ja nende vaatamiseks kasutage navigeerimisriba otsinguvälja, et avada leht **Elektroonilise aruandluse tööd**.</span><span class="sxs-lookup"><span data-stu-id="6e315-202">To check the status of your reports and view them, use the search field on the navigation bar to open the **Electronic reporting jobs** page.</span></span>

    ![Elektroonilise aruandluse tööde lehe otsing](./media/hr-benefits-management-aca-search-electronic-reporting-jobs.png)

4. <span data-ttu-id="6e315-204">Valige vaatamiseks aruanne ja seejärel klõpsake käsku **Kuva failid**.</span><span class="sxs-lookup"><span data-stu-id="6e315-204">Select the report to view, and then select **Show files**.</span></span>

    ![Failide kuvamine](./media/hr-benefits-management-aca-show-files.png)

5. <span data-ttu-id="6e315-206">Valige **Avamine**.</span><span class="sxs-lookup"><span data-stu-id="6e315-206">Select **Open**.</span></span>

    ![Faili avamine](./media/hr-benefits-management-aca-open-file.png)

6. <span data-ttu-id="6e315-208">Avage brauseriakna allosas kuvatav teavitusriba, avage zip-fail ja seejärel valige aruanne.</span><span class="sxs-lookup"><span data-stu-id="6e315-208">From the Notification bar that appears at the bottom of the browser window, open the zip file, and then select the report.</span></span> <span data-ttu-id="6e315-209">Saate PDF-faili vaadata või printida.</span><span class="sxs-lookup"><span data-stu-id="6e315-209">You can view or print the PDF file.</span></span>

    ![Vormi 1095-C näidis](./media/hr-benefits-management-aca-1095-c-form.png)

## <a name="view-aca-coverage-information"></a><span data-ttu-id="6e315-211">ACA kindlustuskaitse teabe vaatamine</span><span class="sxs-lookup"><span data-stu-id="6e315-211">View ACA coverage information</span></span>

<span data-ttu-id="6e315-212">Leht **Töötaja ravikindlustuskaitse** kuvab järgmist teavet.</span><span class="sxs-lookup"><span data-stu-id="6e315-212">The **Worker Affordable Care coverage** page shows the following information:</span></span>

- <span data-ttu-id="6e315-213">Igale kindlustuskaitse grupile määratud töötajad</span><span class="sxs-lookup"><span data-stu-id="6e315-213">Employees who are assigned to each coverage group</span></span>
- <span data-ttu-id="6e315-214">Töötajad, keda ei pea aruandesse kaasama</span><span class="sxs-lookup"><span data-stu-id="6e315-214">Employees who don't have to be included on a report</span></span>
- <span data-ttu-id="6e315-215">Määramata töötajad</span><span class="sxs-lookup"><span data-stu-id="6e315-215">Unassigned employees</span></span>

<span data-ttu-id="6e315-216">Selle teabe vaatamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="6e315-216">To view this information, follow these steps.</span></span>

1. <span data-ttu-id="6e315-217">Valige tööruumis **Soodustuste haldus** valik **Töötaja ravikindlustuskaitse**.</span><span class="sxs-lookup"><span data-stu-id="6e315-217">In the **Benefits management** workspace, select **Worker Affordable Care coverage**.</span></span>
2. <span data-ttu-id="6e315-218">Valige grupp väljal **Grupi nimi**.</span><span class="sxs-lookup"><span data-stu-id="6e315-218">In the **Group name** field, select a group.</span></span>

    ![ACA kindlustuskaitse vaatamine](./media/hr-benefits-management-aca-view-coverage.png)

<span data-ttu-id="6e315-220">Kui mõni väärtus taskukohase ravikindlustuse grupist on alistatud, kuvatakse muudetud väärtuse kõrval tärn.</span><span class="sxs-lookup"><span data-stu-id="6e315-220">If any default values from the Affordable Care coverage group have been overridden, an asterisk appears next to the value that was changed.</span></span> <span data-ttu-id="6e315-221">Kui kõigi 12 kuu väärtused on samad ja neid pole alistatud, kuvatakse väärtus veerus **Kõik 12 kuud**.</span><span class="sxs-lookup"><span data-stu-id="6e315-221">If the values for all 12 months are the same and haven't been overridden, the value appears in the **All 12 months** column.</span></span>

<span data-ttu-id="6e315-222">Saate vaadata töötajaid, kes on märgitud ACA-aruandele mitte lisatavaks ja kes ei vaja vormi 1095-C.</span><span class="sxs-lookup"><span data-stu-id="6e315-222">You can view employees who are marked as not ACA-reportable, and who won't require a Form 1095-C.</span></span> <span data-ttu-id="6e315-223">Valige väljal **Filtreerimise alus** suvand **Ei ole ACA-le esitatav**.</span><span class="sxs-lookup"><span data-stu-id="6e315-223">In the **Filter by** field, select **Not ACA reportable**.</span></span>

<span data-ttu-id="6e315-224">Saate vaadata töötajaid, kes pole gruppi määratud või kes on määratud aegunud gruppi.</span><span class="sxs-lookup"><span data-stu-id="6e315-224">You can view employees who aren't assigned to a group, or who are assigned to an expired group.</span></span> <span data-ttu-id="6e315-225">Valige väljal **Filtreerimisalus** valik **Määramata või aegunud grupp**.</span><span class="sxs-lookup"><span data-stu-id="6e315-225">In the **Filter by** field, select **Unassigned or expired group**.</span></span>

### <a name="export-to-excel"></a><span data-ttu-id="6e315-226">Excelisse eksportimine</span><span class="sxs-lookup"><span data-stu-id="6e315-226">Export to Excel</span></span>

<span data-ttu-id="6e315-227">Loendite eksportimiseks rakendusse Microsoft Excel järgi neid samme.</span><span class="sxs-lookup"><span data-stu-id="6e315-227">To export any of the lists to Microsoft Excel, follow these steps.</span></span>

1. <span data-ttu-id="6e315-228">Valige nupp **Ava Microsoft Office'is**.</span><span class="sxs-lookup"><span data-stu-id="6e315-228">Select the **Open in Microsoft Office** button.</span></span>
2. <span data-ttu-id="6e315-229">Valige **HCM-i inimressursside ajutine tabel sisemiseks kasutamiseks**.</span><span class="sxs-lookup"><span data-stu-id="6e315-229">Select **HCM Human Resources temporary table for internal use**.</span></span>
3. <span data-ttu-id="6e315-230">Valige **Laadi alla**.</span><span class="sxs-lookup"><span data-stu-id="6e315-230">Select **Download**.</span></span>

### <a name="view-aca-reportable-dependents"></a><span data-ttu-id="6e315-231">ACA-aruandele lisatavate ülalpeetavate vaatamine</span><span class="sxs-lookup"><span data-stu-id="6e315-231">View ACA-reportable dependents</span></span>

<span data-ttu-id="6e315-232">Kui peate kindlustuskaitsega inimestest teatama, sest pakute isekindlustuskaitset, saate vaadata ülalpeetavaid, kes on soodustusplaanidega kaitstud ja märgitud kui **ACA-aruandele lisatavad**.</span><span class="sxs-lookup"><span data-stu-id="6e315-232">If you must report covered individuals because you provide self-insured coverage, you can view dependents who are covered under benefit plans that are marked as **ACA reportable**.</span></span> <span data-ttu-id="6e315-233">Valige toimingupaanil nupp **Vaata ülalpeetavate kindlustuskaitset**.</span><span class="sxs-lookup"><span data-stu-id="6e315-233">On the Action Pane, select **View Dependent coverage**.</span></span>

![Ülalpeetavate kindlustuskaitse vaatamine](./media/hr-benefits-management-aca-view-dependent-coverage.png)

<span data-ttu-id="6e315-235">Kuvatakse töötaja ülalpeetavate kindlustuskaitse teave.</span><span class="sxs-lookup"><span data-stu-id="6e315-235">Coverage information for the employee's dependents is shown.</span></span>

![Sõltuv kindlustus](./media/hr-benefits-management-aca-dependents.png)

> [!NOTE]
> <span data-ttu-id="6e315-237">Lehel kuvatakse ainult soodustusplaanid, mis on märgitud kui **ACA-aruandele lisatavad**.</span><span class="sxs-lookup"><span data-stu-id="6e315-237">The page shows only benefits plans that are marked as **ACA reportable**.</span></span>
