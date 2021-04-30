---
title: Human Resourcesi parameetrite konfigureerimine
description: See artikkel selgitab ettevõttepõhiste parameetrite häälestamist rakenduses Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HRMParameters, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 51941
ms.assetid: 2cfb061a-a616-4bf9-9d98-9cde00039eec
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: cd66cb4f5ac02407250e15ae134b36f5ccd4d290
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889928"
---
# <a name="configure-human-resources-parameters"></a><span data-ttu-id="114ad-103">Human Resourcesi parameetrite konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="114ad-103">Configure Human resources parameters</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="114ad-104">Osa inimressursside parameetrite sätteid on ettevõtteülesed, samas kui teiste parameetrite sätted on ettevõttekohased.</span><span class="sxs-lookup"><span data-stu-id="114ad-104">The settings of some Human resources parameters are shared across companies, while the settings of other parameters are company-specific.</span></span> <span data-ttu-id="114ad-105">See artikkel selgitab ettevõttekohaste inimressursside parameetrite häälestamist.</span><span class="sxs-lookup"><span data-stu-id="114ad-105">This topic explains how to set up company-specific Human resources parameters.</span></span>

<span data-ttu-id="114ad-106">Personali ehk inimressursside parameetrite määramiseks kasutatakse kahte lehte.</span><span class="sxs-lookup"><span data-stu-id="114ad-106">Two pages are used to set Human resources parameters.</span></span> <span data-ttu-id="114ad-107">Ettevõtetes ühiskasutatavate parameetrite puhul kasutate lehte **Inimressursside ühiskasutusega parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="114ad-107">For parameters that are shared across companies, you use the **Human resources shared parameters** page.</span></span> <span data-ttu-id="114ad-108">Ettevõttekohaste parameetrite (teisisõnu sätted, mis rakenduvad ühele ettevõttele) puhul kasutate lehte **Inimressursside parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="114ad-108">For parameters that are company-specific (in other words, the settings apply to a single company), you use the **Human resource parameters** page.</span></span>

![Avage Inimressursside parameetrid](./media/hr-employee-self-service-human-resources-parameters.png)

<span data-ttu-id="114ad-110">Lehel **Inimressursside parameetrid** jaotatakse sätted kuue vahekaardi vahel.</span><span class="sxs-lookup"><span data-stu-id="114ad-110">On the **Human resources parameters** page, the settings are divided among six tabs:</span></span>

- <span data-ttu-id="114ad-111">**Üldine**</span><span class="sxs-lookup"><span data-stu-id="114ad-111">**General**</span></span>
- <span data-ttu-id="114ad-112">**Värbamine** (Dynamics 365 Human Resources ei sisalda seda vahekaarti)</span><span class="sxs-lookup"><span data-stu-id="114ad-112">**Recruitment** (this tab isn't included in Dynamics 365 Human Resources)</span></span>
- <span data-ttu-id="114ad-113">**Hüvitus**</span><span class="sxs-lookup"><span data-stu-id="114ad-113">**Compensation**</span></span>
- <span data-ttu-id="114ad-114">**Numbriseeriad**</span><span class="sxs-lookup"><span data-stu-id="114ad-114">**Number sequences**</span></span>
- <span data-ttu-id="114ad-115">**FMLA**</span><span class="sxs-lookup"><span data-stu-id="114ad-115">**FMLA**</span></span>
- <span data-ttu-id="114ad-116">**Töötaja iseteenindus**</span><span class="sxs-lookup"><span data-stu-id="114ad-116">**Employee self service**</span></span>
- <span data-ttu-id="114ad-117">**Juhi iseteenindus**</span><span class="sxs-lookup"><span data-stu-id="114ad-117">**Manager self service**</span></span>
- <span data-ttu-id="114ad-118">**Soodustuste haldus**</span><span class="sxs-lookup"><span data-stu-id="114ad-118">**Benefits management**</span></span>
- <span data-ttu-id="114ad-119">**Puhkused ja puudumine**</span><span class="sxs-lookup"><span data-stu-id="114ad-119">**Leave and absence**</span></span>
- <span data-ttu-id="114ad-120">**Makseviisid**</span><span class="sxs-lookup"><span data-stu-id="114ad-120">**Payment methods**</span></span>

<span data-ttu-id="114ad-121">Iga vahekaart sisaldab teavet, mis on seotud ühe ettevõttega.</span><span class="sxs-lookup"><span data-stu-id="114ad-121">Each tab contains information that pertains to a single company.</span></span>

## <a name="general"></a><span data-ttu-id="114ad-122">Üldine</span><span class="sxs-lookup"><span data-stu-id="114ad-122">General</span></span>

<span data-ttu-id="114ad-123">Sätted vahekaardil **Üldine** määratlevad puudumise, vigastuste ja haiguste ning uute värbamiste kohta käiva teabe ilmumise.</span><span class="sxs-lookup"><span data-stu-id="114ad-123">The settings on the **General** tab define the appearance of information about absence, injury and illness, and new hires.</span></span> <span data-ttu-id="114ad-124">Sellel vahekaardil olevad sätted määratlevad ka mõned vaikekirjed, mis ilmuvad töö tegemisel.</span><span class="sxs-lookup"><span data-stu-id="114ad-124">The settings on this tab also define some default entries that appear as you work.</span></span> <span data-ttu-id="114ad-125">Sellel vahekaardil saate:</span><span class="sxs-lookup"><span data-stu-id="114ad-125">Specifically, this tab lets you:</span></span>

- <span data-ttu-id="114ad-126">valida avatud puudumiskannetele rakendatava värvi;</span><span class="sxs-lookup"><span data-stu-id="114ad-126">Select a color to apply to open absence transactions</span></span>
- <span data-ttu-id="114ad-127">määrata aruannetes kasutatava laadilehe;</span><span class="sxs-lookup"><span data-stu-id="114ad-127">Specify the style sheet to use for reports</span></span>
- <span data-ttu-id="114ad-128">lubada koolituskursuste ja puudumiste registreerimise vahelise integratsiooni;</span><span class="sxs-lookup"><span data-stu-id="114ad-128">Enable the integration between training courses and absence registration</span></span>
- <span data-ttu-id="114ad-129">valida selle integratsiooni juhtimiseks kasutatava puudumise koodi;</span><span class="sxs-lookup"><span data-stu-id="114ad-129">Select the absence code that is used to control this integration.</span></span>
- <span data-ttu-id="114ad-130">näidata, kui kaua säilitada vigastus- ja haigusjuhtude juhtumeid;</span><span class="sxs-lookup"><span data-stu-id="114ad-130">Indicate how long to keep injury and illness case incidents.</span></span>
- <span data-ttu-id="114ad-131">määrata uue töötaja palkamisel vaikimisi kuvatava ID-numbri.</span><span class="sxs-lookup"><span data-stu-id="114ad-131">Specify the default identification number shown when a new worker is hired.</span></span>

![Vahekaart Üldine](./media/hr-setup-parameters-general.png)

## <a name="recruitment"></a><span data-ttu-id="114ad-133">Värbamine</span><span class="sxs-lookup"><span data-stu-id="114ad-133">Recruitment</span></span>

<span data-ttu-id="114ad-134">Vahekaardi **Värbamine** sätted määratlevad dokumenditüübid, mida kasutatakse kandidaatidele automaatselt saadetavas kirjavahetuses.</span><span class="sxs-lookup"><span data-stu-id="114ad-134">The settings on the **Recruitment** tab define the document types used for correspondence automatically sent to applicants.</span></span> <span data-ttu-id="114ad-135">Samuti saate osutada soovimatute avalduste jaoks kasutatavale värbamisprojektile.</span><span class="sxs-lookup"><span data-stu-id="114ad-135">You can also indicate the recruitment project used for unsolicited applications.</span></span>

<span data-ttu-id="114ad-136">Värbamisprojekti ajalise jaotuse jaoks määratletud periood määrab ära värbamisprojektid, mis on lisatud paanile **Projektide ajaline jaotus** tööruumis **Värbamise haldus**.</span><span class="sxs-lookup"><span data-stu-id="114ad-136">The period defined for recruitment project aging determines the recruitment projects included on the **Aging projects** tile in the **Recruitment management** workspace.</span></span> <span data-ttu-id="114ad-137">Avalduse tähtaja hoiatuse jaoks määratletud perioodi kasutatakse avalduse tähtajale lähenevate värbamisprojektide kuvamiseks paanil **Avalduse tähtaeg on lähenemas** tööruumis **Värbamine**.</span><span class="sxs-lookup"><span data-stu-id="114ad-137">The period defined for the application deadline warning is used to display recruitment projects that are approaching their application deadline on the **Application deadline approaching** tile in the **Recruitment** workspace.</span></span>

<span data-ttu-id="114ad-138">Värbamise kohta lisateabe saamiseks vt teemat [Kandidaatide värbamine](hr-personnel-recruit.md).</span><span class="sxs-lookup"><span data-stu-id="114ad-138">For more information about recruiting, see [Recruit job candidates](hr-personnel-recruit.md).</span></span>

## <a name="compensation"></a><span data-ttu-id="114ad-139">Hüvitus</span><span class="sxs-lookup"><span data-stu-id="114ad-139">Compensation</span></span>

<span data-ttu-id="114ad-140">Dynamics 365 Finance'is määratlevad vahekaardil **Hüvitus** olevad sätted, kas kasutajad peavad fikseeritud või ergutussüsteemi plaani jaoks teabe salvestamise kinnitama.</span><span class="sxs-lookup"><span data-stu-id="114ad-140">In Dynamics 365 Finance, the settings on the **Compensation** tab define whether users must confirm that they want to save information for a fixed or variable compensation plan.</span></span> <span data-ttu-id="114ad-141">Ruudu **Luba salvestamise kinnitamine** märkimise korral saavad kasutajad hüvitusega seotud lehe sulgemisel teate, mis küsib, kas nad soovivad kirje salvestada.</span><span class="sxs-lookup"><span data-stu-id="114ad-141">If you select **Enable save validation**, when users close a compensation-related page, they receive a message that asks whether they want to save the record.</span></span> <span data-ttu-id="114ad-142">Osa hüvituste halduse lehti ei luba kasutajatel teavet kustutada.</span><span class="sxs-lookup"><span data-stu-id="114ad-142">Some pages in Compensation management don't let users delete information.</span></span> <span data-ttu-id="114ad-143">Kui palute kasutajatel kinnitada, kas nad soovivad teabe salvestada, aitab see piirata sellise salvestatud teabe hulka, mida ei saa hiljem kustutada.</span><span class="sxs-lookup"><span data-stu-id="114ad-143">By prompting users to verify that they want to save information, you might be able to limit the amount of information that is saved but can't be deleted later.</span></span> <span data-ttu-id="114ad-144">Märkeruudu **Luba salvestamise kinnitamine** tühjendamisel salvestatakse kirjed alati kohe (võimalik, et enne seda, kui kasutaja on selleks valmis).</span><span class="sxs-lookup"><span data-stu-id="114ad-144">If you clear **Enable save validation**, records save immediately, possibly before the user is ready.</span></span> <span data-ttu-id="114ad-145">Jõudlushalduse kasutamisel võimaldab vahekaart **Hüvitus** teil valida ka hindamismudeli, mida tööviljakuse ehk jõudluse hindamisel kompensatsiooniplaanidele määratud mudeli asemel kasutada.</span><span class="sxs-lookup"><span data-stu-id="114ad-145">If you're using Performance management, the **Compensation** tab also lets you select a rating model to use instead of the model assigned to compensation plans when rating performance.</span></span>

<span data-ttu-id="114ad-146">Inimressursside moodulis saate vahekaardi **Hüvitus** kaudu soovi korral piirata juurdepääsu kompensatsiooniplaanidele ja häälestada vaikevaluuta.</span><span class="sxs-lookup"><span data-stu-id="114ad-146">In Human Resources, you can use the **Compensation** tab to choose to restrict access to compensation plans and to set a default currency.</span></span>

<span data-ttu-id="114ad-147">Lisateavet kompensatsiooni kohta leiate artiklist [Kompensatsiooniplaanide ülevaade](hr-compensation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="114ad-147">For more information about compensation, see [Compensation plans overview](hr-compensation-overview.md).</span></span>

![Kompensatsiooni vahekaart](./media/hr-setup-parameters-compensation.png)

## <a name="number-sequences"></a><span data-ttu-id="114ad-149">Numbriseeriad</span><span class="sxs-lookup"><span data-stu-id="114ad-149">Number sequences</span></span>

<span data-ttu-id="114ad-150">Vahekaardi **Numbriseeria** sätted määravad ära seeriad, mida kasutatakse inimressurssides üksustele ID-de automaatseks määramiseks, näiteks:</span><span class="sxs-lookup"><span data-stu-id="114ad-150">The settings on the **Number sequence** tab determine the sequences used to automatically assign IDs to items in Human Resources, such as:</span></span>

- <span data-ttu-id="114ad-151">Avaldused</span><span class="sxs-lookup"><span data-stu-id="114ad-151">Applications</span></span>
- <span data-ttu-id="114ad-152">Puudumiste registreerimised</span><span class="sxs-lookup"><span data-stu-id="114ad-152">Absence registrations</span></span>
- <span data-ttu-id="114ad-153">Kompensatsiooniprotsessi tulemused</span><span class="sxs-lookup"><span data-stu-id="114ad-153">Compensation process results</span></span>
- <span data-ttu-id="114ad-154">Juhtuminumbrid</span><span class="sxs-lookup"><span data-stu-id="114ad-154">Case numbers</span></span>
- <span data-ttu-id="114ad-155">Kursused</span><span class="sxs-lookup"><span data-stu-id="114ad-155">Courses</span></span>
- <span data-ttu-id="114ad-156">Kursuste päevakord</span><span class="sxs-lookup"><span data-stu-id="114ad-156">Course agendas</span></span>

<span data-ttu-id="114ad-157">Numbriseeriate viidete ja koodide säilitamiseks kasutage loendilehte **Numbriseeriad** (valige **Organisatsiooni haldus > Numbriseeriad > Numbriseeriad**).</span><span class="sxs-lookup"><span data-stu-id="114ad-157">To maintain number sequence references and codes, use the **Number sequences** list page (select **Organization administration > Number sequences > Number sequences**).</span></span>

<span data-ttu-id="114ad-158">Lisateabe saamiseks vt teemat [Numbriseeriate ülevaade](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="114ad-158">For more information, see [Number sequences overview](../fin-ops-core/fin-ops/organization-administration/number-sequence-overview.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

> [!NOTE]
> <span data-ttu-id="114ad-159">Töötundide arv ei tohi ületada 1250 tundi ja töösuhte pikkus ei saa olla pikem kui 12 kuud.</span><span class="sxs-lookup"><span data-stu-id="114ad-159">The number of hours that are worked can't exceed 1,250, and the length of employment can't exceed 12 months.</span></span> <span data-ttu-id="114ad-160">Need maksimumväärtused on kooskõlas USA föderaalseadustega.</span><span class="sxs-lookup"><span data-stu-id="114ad-160">These maximum values are in accordance with federal law in the United States.</span></span>

![Vahekaart Numbriseeriad](./media/hr-setup-parameters-number-sequences.png)

## <a name="fmla"></a><span data-ttu-id="114ad-162">FMLA</span><span class="sxs-lookup"><span data-stu-id="114ad-162">FMLA</span></span>

<span data-ttu-id="114ad-163">FMLA vahekaardil saate määrata FMLA sobivuse nõuded ja FMLA õigustatud tunnid.</span><span class="sxs-lookup"><span data-stu-id="114ad-163">On the FMLA tab, you set FMLA eligibility requirements and FMLA entitlement hours.</span></span> <span data-ttu-id="114ad-164">Lisateabe saamiseks vt jaotist [Puhkuse ja puudumise parameetrite konfigureerimine](hr-leave-and-absence-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="114ad-164">For more information, see [Configure leave and absence parameters](hr-leave-and-absence-parameters.md).</span></span>

![FMLA vahekaart](./media/hr-setup-parameters-fmla.png)

## <a name="employee-self-service"></a><span data-ttu-id="114ad-166">Töövõtja iseteenindus</span><span class="sxs-lookup"><span data-stu-id="114ad-166">Employee self service</span></span>

<span data-ttu-id="114ad-167">Vahekaardi **Töötaja iseteenindus** sätted mõjutavad töötaja iseteeninduse vaate kuvamist töötajatele.</span><span class="sxs-lookup"><span data-stu-id="114ad-167">The settings on the **Employee self service** tab affect how Employee self service appears to employees.</span></span> <span data-ttu-id="114ad-168">Sellel vahekaardil saate:</span><span class="sxs-lookup"><span data-stu-id="114ad-168">On this tab, you can:</span></span>

- <span data-ttu-id="114ad-169">sisestada töötaja iseteeninduse tööruumi nime;</span><span class="sxs-lookup"><span data-stu-id="114ad-169">Enter a name for the Employee self service workspace</span></span>
- <span data-ttu-id="114ad-170">valida, millist teavet saab ülemus töötajate kohta sisestada;</span><span class="sxs-lookup"><span data-stu-id="114ad-170">Select which information a manager can enter for employees</span></span>
- <span data-ttu-id="114ad-171">lisada töötajate jaoks kasulikke linke;</span><span class="sxs-lookup"><span data-stu-id="114ad-171">Add useful links for employees</span></span>
- <span data-ttu-id="114ad-172">piirata töötajatel ettevõtte kontaktteabe lisamist või redigeerimist.</span><span class="sxs-lookup"><span data-stu-id="114ad-172">Restrict employees from adding or editing business contact details.</span></span> <span data-ttu-id="114ad-173">Lisateavet vt teemast [Isikuandmete redigeerimise piiramine](hr-employee-self-service-restrict-editing.md).</span><span class="sxs-lookup"><span data-stu-id="114ad-173">For more information, see [Restrict editing of personal information](hr-employee-self-service-restrict-editing.md).</span></span>

<span data-ttu-id="114ad-174">Lisateavet töötaja iseteeninduse häälestamise kohta vt teemast [Töövõtja ja ülemuse iseteeninduse ülevaade](hr-employee-manager-self-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="114ad-174">For more information about setting up Employee self service, see [Employee and Manager self service overview](hr-employee-manager-self-service-overview.md).</span></span>

![Töötaja iseteeninduse vahekaart](./media/hr-setup-parameters-employee-self-service.png)

## <a name="manager-self-service"></a><span data-ttu-id="114ad-176">Juhi iseteenindus</span><span class="sxs-lookup"><span data-stu-id="114ad-176">Manager self service</span></span>

<span data-ttu-id="114ad-177">Vahekaardi **Juhi iseteenindus** sätted mõjutavad seda, millist teavet ülemused juhi iseteeninduse aknas näevad.</span><span class="sxs-lookup"><span data-stu-id="114ad-177">The settings on the **Manager self service** tab affect what managers see in Manager self service.</span></span> <span data-ttu-id="114ad-178">Sellel vahekaardil saate konfigureerida järgmisi valikuid:</span><span class="sxs-lookup"><span data-stu-id="114ad-178">On this tab, you can configure the following options:</span></span>

- <span data-ttu-id="114ad-179">Aeguvate kirjete vahemik</span><span class="sxs-lookup"><span data-stu-id="114ad-179">The range for expiring records</span></span>
- <span data-ttu-id="114ad-180">Teabehaldurid saavad aegumiskirjetes vaadata järgmist teavet</span><span class="sxs-lookup"><span data-stu-id="114ad-180">Information managers can view in expiring records</span></span>
- <span data-ttu-id="114ad-181">Kas ülemused saavad laiendatud aruannete jaoks vaadata vabu ametikohti?</span><span class="sxs-lookup"><span data-stu-id="114ad-181">Whether managers can view open positions for extended reports</span></span>
- <span data-ttu-id="114ad-182">Lahkuvate töötajate vaated</span><span class="sxs-lookup"><span data-stu-id="114ad-182">Views of exiting workers</span></span>
- <span data-ttu-id="114ad-183">Ülemustele kasulikud lingid</span><span class="sxs-lookup"><span data-stu-id="114ad-183">Useful links for managers</span></span>

<span data-ttu-id="114ad-184">Lisateavet juhi iseteeninduse häälestamise kohta vt teemast [Töövõtja ja ülemuse iseteeninduse ülevaade](hr-employee-manager-self-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="114ad-184">For more information about setting up Manager self service, see [Employee and Manager self service overview](hr-employee-manager-self-service-overview.md).</span></span>

![Juhi iseteeninduse vahekaart](./media/hr-setup-parameters-manager-self-service.png)

## <a name="benefits-management"></a><span data-ttu-id="114ad-186">Soodustuste haldus</span><span class="sxs-lookup"><span data-stu-id="114ad-186">Benefits management</span></span>

<span data-ttu-id="114ad-187">Soodustuste halduse vahekaardil saate konfigureerida soodustuste halduse meilivalikud.</span><span class="sxs-lookup"><span data-stu-id="114ad-187">On the Benefits management tab, you can configure email options for Benefits management.</span></span> <span data-ttu-id="114ad-188">Lisateavet soodustuste halduse häälestamise ja kasutamise kohta vt teemast [Soodustuste halduse ülevaade](hr-benefits-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="114ad-188">For information about setting up and using Benefits management, see [Benefits management overview](hr-benefits-management-overview.md).</span></span>

![Soodustuste halduse vahekaart](./media/hr-setup-parameters-benefits-management.png)

## <a name="leave-and-absence"></a><span data-ttu-id="114ad-190">Puhkused ja puudumine</span><span class="sxs-lookup"><span data-stu-id="114ad-190">Leave and absence</span></span>

<span data-ttu-id="114ad-191">Puhkuste ja puudumiste häälestamise ja kasutamise kohta teabe saamiseks vt teemat [Puhkuste ja puudumiste ülevaade](hr-leave-and-absence-overview.md).</span><span class="sxs-lookup"><span data-stu-id="114ad-191">For information about setting up and using Leave and absence, see [Leave and absence overview](hr-leave-and-absence-overview.md).</span></span>

## <a name="payment-methods"></a><span data-ttu-id="114ad-192">Makseviisid</span><span class="sxs-lookup"><span data-stu-id="114ad-192">Payment methods</span></span>

<span data-ttu-id="114ad-193">Vahekaardil **Makseviisid** saate valida makseviisid, mida teie organisatsioon toetab.</span><span class="sxs-lookup"><span data-stu-id="114ad-193">On the **Payment methods** tab, you can select the payment methods supported by your organization.</span></span> <span data-ttu-id="114ad-194">Lisateavet hüvituste konfigureerimise kohta leiate artiklist [Kompensatsiooniplaanide ülevaade](hr-compensation-overview.md).</span><span class="sxs-lookup"><span data-stu-id="114ad-194">For more information about configuring compensation, see [Compensation plans overview](hr-compensation-overview.md).</span></span>

![Makseviiside vahekaart](./media/hr-setup-parameters-payment-methods.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]