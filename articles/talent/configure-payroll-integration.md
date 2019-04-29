---
title: Rakenduste Talent ja Dayforce vahelise palgaarvestuse integratsiooni konfigureerimine
description: Selles teemas selgitatakse, kuidas konfigureerida rakenduste Microsoft Dynamics 365 for Talent ja Ceridian Dayforce vahelist integratsiooni nii, et saaksite teha palgatöötlust.
author: andreabichsel
manager: AnnBe
ms.date: 03/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 9a88bf61dbb12520b555ceb7363b1c646d95386e
ms.sourcegitcommit: 204e4554e409c39fbbf7b273ad138ce2809931a8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/26/2019
ms.locfileid: "898440"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="77de4-103">Palgaarvestuse integratsiooni konfigureerimine Talenti ja Dayforce’i vahel</span><span class="sxs-lookup"><span data-stu-id="77de4-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="77de4-104">Rakenduste Microsoft Dynamics 365 for Talent ja Ceridian Dayforce vaheline integratsioon sõltub mitmest konfiguratsioonietapist, mida kirjeldatakse selles teemas.</span><span class="sxs-lookup"><span data-stu-id="77de4-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="77de4-105">Enne palgatöötluse tegemist peate konfigureerima integratsiooni nii rakenduses Talent kui ka Dayforce.</span><span class="sxs-lookup"><span data-stu-id="77de4-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="77de4-106">Kui te kasutate palgatöötluste tegemiseks teenust nagu Dayforce, siis peate rakenduses Talent integratsiooni lubama.</span><span class="sxs-lookup"><span data-stu-id="77de4-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="77de4-107">Integratsiooni jaoks on rakendusest Talent vaja teatud andmeid.</span><span class="sxs-lookup"><span data-stu-id="77de4-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="77de4-108">Seega peate kinnitama, et Dayforce’iga vastendatud andmed on rakenduses Talent konfigureeritud viisil, mis lubab integratsiooni.</span><span class="sxs-lookup"><span data-stu-id="77de4-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="77de4-109">Integratsioon kasutab järgmisi üldisi andmekategooriaid.</span><span class="sxs-lookup"><span data-stu-id="77de4-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="77de4-110">Inimressursside andmed</span><span class="sxs-lookup"><span data-stu-id="77de4-110">Human resources data</span></span>
- <span data-ttu-id="77de4-111">Hüvituse andmed</span><span class="sxs-lookup"><span data-stu-id="77de4-111">Compensation data</span></span>
- <span data-ttu-id="77de4-112">Palgaandmed, näiteks palgatsüklid, makseperioodid ja tulukoodid</span><span class="sxs-lookup"><span data-stu-id="77de4-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="77de4-113">Töötaja andmed</span><span class="sxs-lookup"><span data-stu-id="77de4-113">Worker data</span></span>

<span data-ttu-id="77de4-114">Teemas kirjeldatakse etappe, mida peate integratsiooni lubamiseks läbima.</span><span class="sxs-lookup"><span data-stu-id="77de4-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="77de4-115">Samuti selgitatakse integratsiooni jaoks vajalikke andmetüüpe ja konfigureerimise üksikasju.</span><span class="sxs-lookup"><span data-stu-id="77de4-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="77de4-116">Integratsiooni lubamine</span><span class="sxs-lookup"><span data-stu-id="77de4-116">Enable the integration</span></span>

<span data-ttu-id="77de4-117">Dayforce’iga ühendamiseks peate rakenduses Talent sisse lülitama integratsiooni ja sisestama konfigureerimisteabe.</span><span class="sxs-lookup"><span data-stu-id="77de4-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="77de4-118">Kui soovite, et loodav pearaamatu kanne imporditaks rakendusse Microsoft Dynamics 365 for Finance and Operations, siis peate seadistama Microsoft Azure’i salvestuskonto ja sisestama Azure’i salvestusruumi ühendusstringi rakendusse Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="77de4-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="77de4-119">Rakenduses Talent integratsiooni sisselülitamiseks järgige järgmisi juhiseid.</span><span class="sxs-lookup"><span data-stu-id="77de4-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="77de4-120">Valige lehelt **Süsteemihaldus** suvand **Integratsiooni konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="77de4-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="77de4-121">Sisestage turvalise failiedastusprotokolli File Transfer Protocol (FTP) lõpp-punkt ja turvalise FTP kausta tee.</span><span class="sxs-lookup"><span data-stu-id="77de4-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="77de4-122">Sisestage selle kasutaja kasutajanimi ja parool, kellel on vaja juurdepääsu turvalise FTP lõpp-punktile ja kausta teele.</span><span class="sxs-lookup"><span data-stu-id="77de4-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="77de4-123">Testige ühendust vajaduse järgi ja määrake suvand **Palgaarvestuse integratsiooni lubamine** olekule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="77de4-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="77de4-124">Kui integratsioon on sisse lülitatud, luuakse andmete ekspordipakett ja -failid ning määratakse sagedus.</span><span class="sxs-lookup"><span data-stu-id="77de4-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="77de4-125">Vajaduse korral saate seda sagedust muuta.</span><span class="sxs-lookup"><span data-stu-id="77de4-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="77de4-126">Lisateavet Azure’i talletamiskontode ja Azure’i salvestusruumi ühendusstringide kohta leiate järgmistest Azure’i teemadest.</span><span class="sxs-lookup"><span data-stu-id="77de4-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="77de4-127">Azure’i salvestuskontod</span><span class="sxs-lookup"><span data-stu-id="77de4-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="77de4-128">Azure’i salvestusruumi ühendusstringide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="77de4-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a><span data-ttu-id="77de4-129">Andmete konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="77de4-129">Configure your data</span></span> 

<span data-ttu-id="77de4-130">Palgaarvestuse töötlemiseks peate konfigureerima rakenduses Talent personaliandmeid.</span><span class="sxs-lookup"><span data-stu-id="77de4-130">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="77de4-131">Peate määratlema organisatsiooni andmeid nagu tööd ja ametikohad, samuti teavet soodustuste ning kompensatsioonide kohta.</span><span class="sxs-lookup"><span data-stu-id="77de4-131">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="77de4-132">Selle teabe hulka kuulub töövõtja palgaandmete loomiseks vajalik teave töösuhte, palga ja mahaarvamiste kohta.</span><span class="sxs-lookup"><span data-stu-id="77de4-132">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="77de4-133">Personaliandmed</span><span class="sxs-lookup"><span data-stu-id="77de4-133">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="77de4-134">Soodustused</span><span class="sxs-lookup"><span data-stu-id="77de4-134">Benefits</span></span> 

<span data-ttu-id="77de4-135">Inimressursid pakuvad tööriistu, mis aitavad seadistada ja hallata soodustusi, mahaarvamisi ning töötajate hüvitusplaane, mida organisatsioon oma töötajatele pakub või nende puhul töötleb.</span><span class="sxs-lookup"><span data-stu-id="77de4-135">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="77de4-136">Soodustuste loomisel pidage meeles järgmisi Dayforce’is kasutatavaid andmeid ja konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="77de4-136">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="77de4-137">Soodustusplaanid</span><span class="sxs-lookup"><span data-stu-id="77de4-137">Benefit plans</span></span>

- <span data-ttu-id="77de4-138">Plaan (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-138">Plan (required)</span></span>
- <span data-ttu-id="77de4-139">Tüüp (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-139">Type (required)</span></span>
- <span data-ttu-id="77de4-140">Palga mõju (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-140">Payroll impact (required)</span></span>
- <span data-ttu-id="77de4-141">Võlgnevuste sissenõudmine</span><span class="sxs-lookup"><span data-stu-id="77de4-141">Recover arrears</span></span>
- <span data-ttu-id="77de4-142">Mahaarvamismeetod</span><span class="sxs-lookup"><span data-stu-id="77de4-142">Deduction method</span></span>
- <span data-ttu-id="77de4-143">Mahaarvamise prioriteet</span><span class="sxs-lookup"><span data-stu-id="77de4-143">Deduction priority</span></span>
- <span data-ttu-id="77de4-144">Perioodi piiramine</span><span class="sxs-lookup"><span data-stu-id="77de4-144">Limit period</span></span>
- <span data-ttu-id="77de4-145">Piirsumma</span><span class="sxs-lookup"><span data-stu-id="77de4-145">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="77de4-146">Soodustused</span><span class="sxs-lookup"><span data-stu-id="77de4-146">Benefits</span></span>

- <span data-ttu-id="77de4-147">Plaan (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-147">Plan (required)</span></span>
- <span data-ttu-id="77de4-148">Tüüp (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-148">Type (required)</span></span>
- <span data-ttu-id="77de4-149">Suvand (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-149">Option (required)</span></span>
- <span data-ttu-id="77de4-150">Soodustuse ID (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-150">Benefit ID (required)</span></span>
- <span data-ttu-id="77de4-151">Sagedus</span><span class="sxs-lookup"><span data-stu-id="77de4-151">Frequency</span></span>
- <span data-ttu-id="77de4-152">Alus</span><span class="sxs-lookup"><span data-stu-id="77de4-152">Basis</span></span>
- <span data-ttu-id="77de4-153">Summa või määr</span><span class="sxs-lookup"><span data-stu-id="77de4-153">Amount or rate</span></span>
- <span data-ttu-id="77de4-154">Tulukood</span><span class="sxs-lookup"><span data-stu-id="77de4-154">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="77de4-155">Toetatud sagedused</span><span class="sxs-lookup"><span data-stu-id="77de4-155">Supported frequencies</span></span> 

- <span data-ttu-id="77de4-156">Iga nädal</span><span class="sxs-lookup"><span data-stu-id="77de4-156">Weekly</span></span>
- <span data-ttu-id="77de4-157">Kahe nädala tagant</span><span class="sxs-lookup"><span data-stu-id="77de4-157">Bi-weekly</span></span>
- <span data-ttu-id="77de4-158">Iga poole kuu tagant</span><span class="sxs-lookup"><span data-stu-id="77de4-158">Semi-monthly</span></span>
- <span data-ttu-id="77de4-159">Kord kuus</span><span class="sxs-lookup"><span data-stu-id="77de4-159">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="77de4-160">Toetatud alused</span><span class="sxs-lookup"><span data-stu-id="77de4-160">Supported bases</span></span> 

- <span data-ttu-id="77de4-161">Fikseeritud summa</span><span class="sxs-lookup"><span data-stu-id="77de4-161">Fixed amount</span></span>
- <span data-ttu-id="77de4-162">Tulu protsent</span><span class="sxs-lookup"><span data-stu-id="77de4-162">Percent of earnings</span></span>
- <span data-ttu-id="77de4-163">Produktiivsed tunnid</span><span class="sxs-lookup"><span data-stu-id="77de4-163">Productive hours</span></span>

<span data-ttu-id="77de4-164">Dayforce loob järgmised mahaarvamised palga mõju alusel, mis on määratletud soodustusplaanis.</span><span class="sxs-lookup"><span data-stu-id="77de4-164">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="77de4-165">Valik rakenduses Talent</span><span class="sxs-lookup"><span data-stu-id="77de4-165">Selection in Talent</span></span>        | <span data-ttu-id="77de4-166">Tulemus rakenduses Dayforce</span><span class="sxs-lookup"><span data-stu-id="77de4-166">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="77de4-167">Pole</span><span class="sxs-lookup"><span data-stu-id="77de4-167">None</span></span>                       | <span data-ttu-id="77de4-168">Mahaarvamist ei looda.</span><span class="sxs-lookup"><span data-stu-id="77de4-168">No deduction is created.</span></span>                      |
| <span data-ttu-id="77de4-169">Ainult mahaarvamine</span><span class="sxs-lookup"><span data-stu-id="77de4-169">Deduction only</span></span>             | <span data-ttu-id="77de4-170">Luuakse töövõtja mahaarvamine.</span><span class="sxs-lookup"><span data-stu-id="77de4-170">An employee deduction is created.</span></span>             |
| <span data-ttu-id="77de4-171">Ainult lisamine</span><span class="sxs-lookup"><span data-stu-id="77de4-171">Contribution only</span></span>          | <span data-ttu-id="77de4-172">Luuakse tööandja mahaarvamine.</span><span class="sxs-lookup"><span data-stu-id="77de4-172">An employer deduction is created.</span></span>             |
| <span data-ttu-id="77de4-173">Mahaarvamine ja lisamine</span><span class="sxs-lookup"><span data-stu-id="77de4-173">Deduction and contribution</span></span> | <span data-ttu-id="77de4-174">Luuakse töövõtja ja tööandja mahaarvamised.</span><span class="sxs-lookup"><span data-stu-id="77de4-174">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="77de4-175">Lisateavet soodustusprogrammi määratlemise ja haldamise kohta vaadake järgmistest teemadest.</span><span class="sxs-lookup"><span data-stu-id="77de4-175">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="77de4-176">Töötaja soodustuste programmi pakkumine</span><span class="sxs-lookup"><span data-stu-id="77de4-176">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="77de4-177">Uue soodustuse loomine</span><span class="sxs-lookup"><span data-stu-id="77de4-177">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="77de4-178">Soodustuskõlblikkuse reeglite ja poliitikate määratlemine</span><span class="sxs-lookup"><span data-stu-id="77de4-178">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="77de4-179">Töötajate soodustuste registreerimine ja eemaldamine</span><span class="sxs-lookup"><span data-stu-id="77de4-179">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="77de4-180">Hüvitus</span><span class="sxs-lookup"><span data-stu-id="77de4-180">Compensation</span></span> 

<span data-ttu-id="77de4-181">Hüvituste haldust kasutatakse põhitasu ja preemiate jagamise juhtimiseks.</span><span class="sxs-lookup"><span data-stu-id="77de4-181">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="77de4-182">Töötaja fikseeritud põhipalga ja preemia tõusu juhitakse põhipalga plaanide kaudu.</span><span class="sxs-lookup"><span data-stu-id="77de4-182">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="77de4-183">Lisatasude (nt preemiate, tulemustasude aktsiate eelismüügi ja toetuste ning ühekordsete preemiate) maksmist juhitakse ergutussüsteemi plaanide kaudu.</span><span class="sxs-lookup"><span data-stu-id="77de4-183">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="77de4-184">Dayforce kasutab hüvituse teavet töövõtja tunni- või aastamäära arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="77de4-184">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="77de4-185">Nõutavad on põhipalgaplaanid ja palgamäära teisendamised.</span><span class="sxs-lookup"><span data-stu-id="77de4-185">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="77de4-186">Töövõtjad peavad olema seotud põhipalgaplaaniga.</span><span class="sxs-lookup"><span data-stu-id="77de4-186">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="77de4-187">Lisateavet hüvitusplaanide kohta vaadake järgmistest teemadest.</span><span class="sxs-lookup"><span data-stu-id="77de4-187">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="77de4-188">Põhipalga plaanide loomine</span><span class="sxs-lookup"><span data-stu-id="77de4-188">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="77de4-189">Ergutussüsteemi plaanide loomine</span><span class="sxs-lookup"><span data-stu-id="77de4-189">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="77de4-190">Palga/hüvituse struktuuri ja plaanide arendamine</span><span class="sxs-lookup"><span data-stu-id="77de4-190">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="77de4-191">Hüvitusprotsess</span><span class="sxs-lookup"><span data-stu-id="77de4-191">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="77de4-192">Hüvitusprotsessi määratlemine ja tulemuste arvutamine</span><span class="sxs-lookup"><span data-stu-id="77de4-192">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="77de4-193">Töötaja liitmine põhipalga plaaniga</span><span class="sxs-lookup"><span data-stu-id="77de4-193">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="77de4-194">Töötaja liitmine tulemustasu plaaniga</span><span class="sxs-lookup"><span data-stu-id="77de4-194">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="77de4-195">Tööd</span><span class="sxs-lookup"><span data-stu-id="77de4-195">Jobs</span></span> 

<span data-ttu-id="77de4-196">Töö on tööd tegeva isiku jaoks nõutavate ülesannete ja vastutuste kogum.</span><span class="sxs-lookup"><span data-stu-id="77de4-196">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="77de4-197">Lisateavet vt järgmistest teemadest:</span><span class="sxs-lookup"><span data-stu-id="77de4-197">For more information, see the following topics:</span></span>

- [<span data-ttu-id="77de4-198">Töö komponentide seadistamine</span><span class="sxs-lookup"><span data-stu-id="77de4-198">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="77de4-199">Uute tööde määratlemine</span><span class="sxs-lookup"><span data-stu-id="77de4-199">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="77de4-200">Ametikohad</span><span class="sxs-lookup"><span data-stu-id="77de4-200">Positions</span></span>

<span data-ttu-id="77de4-201">Ametikoht on töökoha üksik eksemplar.</span><span class="sxs-lookup"><span data-stu-id="77de4-201">A position is an individual instance of a job.</span></span> <span data-ttu-id="77de4-202">Näiteks on ametikoht „müügijuht (Ida)” vaid üks tööga „müügijuht” seostatud ametikohti.</span><span class="sxs-lookup"><span data-stu-id="77de4-202">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="77de4-203">Ametikoht kuulub osakonna alla.</span><span class="sxs-lookup"><span data-stu-id="77de4-203">A position exists in a department.</span></span> <span data-ttu-id="77de4-204">Iga ametikohaga saab seostada vaid ühte töötajat.</span><span class="sxs-lookup"><span data-stu-id="77de4-204">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="77de4-205">Ametikohtade seadistamisel pidage meeles järgmisi andmeid ja konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="77de4-205">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="77de4-206">Ametikoht (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-206">Position (required)</span></span>
- <span data-ttu-id="77de4-207">Kirjeldus (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-207">Description (required)</span></span>
- <span data-ttu-id="77de4-208">Töö (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-208">Job (required)</span></span>
- <span data-ttu-id="77de4-209">Osakond (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-209">Department (required)</span></span>
- <span data-ttu-id="77de4-210">Ametikoha tüüp (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-210">Position type (required)</span></span>
- <span data-ttu-id="77de4-211">Täistööaja vaste</span><span class="sxs-lookup"><span data-stu-id="77de4-211">Full-time equivalent</span></span>
- <span data-ttu-id="77de4-212">Iga-aastased regulaarsed tunnid (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-212">Annual regular hours (required)</span></span>
- <span data-ttu-id="77de4-213">Maksja juriidiline isik (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-213">Paid by legal entity (required)</span></span>
- <span data-ttu-id="77de4-214">Palgatsükkel (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-214">Pay cycle (required)</span></span>
- <span data-ttu-id="77de4-215">Vaike-finantsdimensioonid – kulukeskus (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-215">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="77de4-216">Töötaja määramine – töötaja, määramise algus, määramise lõpp, põhjuse kood</span><span class="sxs-lookup"><span data-stu-id="77de4-216">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="77de4-217">Kui ühes osakonnas on sama tööga seotud mitu ametikohta, siis konsolideeritakse need rakenduses Dayforce üheks ametikohaks.</span><span class="sxs-lookup"><span data-stu-id="77de4-217">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="77de4-218">Lisateavet vt järgmistest teemadest:</span><span class="sxs-lookup"><span data-stu-id="77de4-218">For more information, see the following topics:</span></span>

- [<span data-ttu-id="77de4-219">Tööjõu korraldamine osakondade, tööde ja ametikohtade abil</span><span class="sxs-lookup"><span data-stu-id="77de4-219">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="77de4-220">Ametikohtade seadistamine</span><span class="sxs-lookup"><span data-stu-id="77de4-220">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="77de4-221">Osakonnad</span><span class="sxs-lookup"><span data-stu-id="77de4-221">Departments</span></span>

<span data-ttu-id="77de4-222">Osakond on tootmisüksus, mis esindab organisatsiooni kategooriat või funktsionaalset ala.</span><span class="sxs-lookup"><span data-stu-id="77de4-222">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="77de4-223">Osakond vastutab organisatsiooni kindla valdkonna eest, nagu müük, raamatupidamine või inimressursid.</span><span class="sxs-lookup"><span data-stu-id="77de4-223">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="77de4-224">Saate osakondi kasutada funktsionaalsete alade aruannete koostamiseks.</span><span class="sxs-lookup"><span data-stu-id="77de4-224">You can use departments to report on functional areas.</span></span> <span data-ttu-id="77de4-225">Osakonnad võivad vastutada kasumi ja kahjumi eest.</span><span class="sxs-lookup"><span data-stu-id="77de4-225">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="77de4-226">Lisateavet vt järgmistest teemadest:</span><span class="sxs-lookup"><span data-stu-id="77de4-226">For more information, see the following topics:</span></span>

- [<span data-ttu-id="77de4-227">Osakonna loomine ja selle seostamine osakonnahierarhiaga</span><span class="sxs-lookup"><span data-stu-id="77de4-227">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="77de4-228">Uute osakondade määratlemine</span><span class="sxs-lookup"><span data-stu-id="77de4-228">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="77de4-229">Palgatsüklid ja makseperioodid</span><span class="sxs-lookup"><span data-stu-id="77de4-229">Pay cycles and pay periods</span></span>

<span data-ttu-id="77de4-230">Palgatsükkel määrab, kui tihti palgamaksmine toimub ja konkreetsed päevad, millal töötajatele palka makstakse.</span><span class="sxs-lookup"><span data-stu-id="77de4-230">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="77de4-231">Näiteks võib palgatsükli sageduseks olla üks kuu ja töövõtjatele makstakse seega kuu viimasel päeval.</span><span class="sxs-lookup"><span data-stu-id="77de4-231">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="77de4-232">Või kui palgatsükli sageduseks on üks nädal, siis makstakse töövõtjatele näiteks teisipäeviti pärast makseperioodi lõppu.</span><span class="sxs-lookup"><span data-stu-id="77de4-232">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="77de4-233">Palgatsükleid määratakse ametikohtadele selleks, et määrata, millal nendel ametikohtadel töötavatele töötajatele palka makstakse.</span><span class="sxs-lookup"><span data-stu-id="77de4-233">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="77de4-234">Pärast palgatsüklite loomist saate iga tsükli jaoks luua makseperioodid.</span><span class="sxs-lookup"><span data-stu-id="77de4-234">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="77de4-235">Igal makseperioodil on makse vaikekuupäev, mis põhineb teie sisestatud teabel.</span><span class="sxs-lookup"><span data-stu-id="77de4-235">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="77de4-236">Siiski saate erandite käsitlemiseks makseperioodi makse vaikekuupäeva muuta, näiteks kui maksekuupäev satub riigipühale.</span><span class="sxs-lookup"><span data-stu-id="77de4-236">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="77de4-237">Dayforce kasutab järgmist teavet.</span><span class="sxs-lookup"><span data-stu-id="77de4-237">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="77de4-238">Palgatsükkel (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-238">Pay cycle (required)</span></span>
- <span data-ttu-id="77de4-239">Palgatsükli sagedus (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-239">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="77de4-240">Perioodi alguskuupäev (esimene makseperiood on kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-240">Period start date (first pay period required)</span></span>
- <span data-ttu-id="77de4-241">Makse vaikekuupäev (esimene makseperiood on kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-241">Default payment date (first pay period required)</span></span>

<span data-ttu-id="77de4-242">See teave on integreeritud rakendusse Dayforce palgagruppidena ja on iga palgatsükli puhul eraldatud riigi või regiooniga.</span><span class="sxs-lookup"><span data-stu-id="77de4-242">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="77de4-243">Enne integreerimist peab olema loodud vähemalt üks makseperiood.</span><span class="sxs-lookup"><span data-stu-id="77de4-243">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="77de4-244">Dayforce loob palgagrupi kalendrid ja maksekuupäevad rakenduses Talent määratletud esimese makseperioodi alguskuupäeva ja makse vaikekuupäeva põhjal.</span><span class="sxs-lookup"><span data-stu-id="77de4-244">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="77de4-245">Tulukoodid</span><span class="sxs-lookup"><span data-stu-id="77de4-245">Earning codes</span></span>

<span data-ttu-id="77de4-246">Tulukoodid määratlevad kordumatult igat tüüpi tulud, mida töötajad saavad.</span><span class="sxs-lookup"><span data-stu-id="77de4-246">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="77de4-247">Koodidel on mitmeid tuludega seotud parameetreid, näiteks raamatupidamisreeglid, maksuseadused, aruandluse nõuded ja brutosumma võime.</span><span class="sxs-lookup"><span data-stu-id="77de4-247">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="77de4-248">Dayforce kasutab järgmist teavet.</span><span class="sxs-lookup"><span data-stu-id="77de4-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="77de4-249">Tulukood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-249">Earning Code (required)</span></span>
- <span data-ttu-id="77de4-250">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="77de4-250">Description</span></span>
- <span data-ttu-id="77de4-251">Mõõtühik</span><span class="sxs-lookup"><span data-stu-id="77de4-251">Unit of measure</span></span>
- <span data-ttu-id="77de4-252">Produktiivne</span><span class="sxs-lookup"><span data-stu-id="77de4-252">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="77de4-253">Töötaja andmed</span><span class="sxs-lookup"><span data-stu-id="77de4-253">Worker data</span></span>

<span data-ttu-id="77de4-254">Töötajate kirjed on tähtsad teie personali- ja palgasüsteemide jaoks.</span><span class="sxs-lookup"><span data-stu-id="77de4-254">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="77de4-255">Teie sisestatud teavet saab kasutada töötajate ja nende isikliku teabe jälgimiseks.</span><span class="sxs-lookup"><span data-stu-id="77de4-255">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="77de4-256">Töötajate kohta saate hallata järgmist teavet.</span><span class="sxs-lookup"><span data-stu-id="77de4-256">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="77de4-257">**Üldine** – töötaja põhiteave, näiteks kontaktteave, demograafiline teave, tuvastamisteave, perekonna teave, sõjaväeteenistuse olek, välislähetuse teave ja isiklikud ning lähedase isiku kontaktandmed.</span><span class="sxs-lookup"><span data-stu-id="77de4-257">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="77de4-258">**Töösuhe** – töötaja töösuhte teave, näiteks töötaja palganud ettevõte või organisatsioon, määratud ametikoht, algus- ja lõppkuupäevad, töökõlblikkus, töölevõtutingimused, pension, puhkus ja ümberpaigutuse teave.</span><span class="sxs-lookup"><span data-stu-id="77de4-258">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="77de4-259">**Puhkused ja puudumised** – teave töötaja puudumiste kohta, näiteks töögraafikud, puudumiskanded ja puudumise seadistamine.</span><span class="sxs-lookup"><span data-stu-id="77de4-259">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="77de4-260">**Hüvitus ja palk** – teave töötaja hüvitusplaanide ja palgaarvestuse kohta, näiteks liitutud plaanid, preemiad, tööviljakus, komisjonitasu, maksuteave, pensionileminek ning palgast mahaarvamised.</span><span class="sxs-lookup"><span data-stu-id="77de4-260">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="77de4-261">Töötaja teabe sisestamisel pidage meeles järgmisi Dayforce’is kasutatavaid andmeid ja konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="77de4-261">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="77de4-262">Üldteave</span><span class="sxs-lookup"><span data-stu-id="77de4-262">General information</span></span>

- <span data-ttu-id="77de4-263">Töötaja number (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-263">Personnel number (required)</span></span>
- <span data-ttu-id="77de4-264">Eesnimi (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-264">First name (required)</span></span>
- <span data-ttu-id="77de4-265">Perekonnanimi (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-265">Last name (required)</span></span>
- <span data-ttu-id="77de4-266">Teine eesnimi</span><span class="sxs-lookup"><span data-stu-id="77de4-266">Middle name</span></span>
- <span data-ttu-id="77de4-267">Staaž kuupäeval</span><span class="sxs-lookup"><span data-stu-id="77de4-267">Seniority date</span></span>
- <span data-ttu-id="77de4-268">Tuntud kui</span><span class="sxs-lookup"><span data-stu-id="77de4-268">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="77de4-269">Isikuandmed</span><span class="sxs-lookup"><span data-stu-id="77de4-269">Personal information</span></span>

- <span data-ttu-id="77de4-270">Perekonnaseis (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-270">Marital status (required)</span></span>
- <span data-ttu-id="77de4-271">Sünnikuupäev (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-271">Birth date (required)</span></span>
- <span data-ttu-id="77de4-272">Sugu (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-272">Gender (required)</span></span>
- <span data-ttu-id="77de4-273">Puudega isik</span><span class="sxs-lookup"><span data-stu-id="77de4-273">Person with disabilities</span></span>
- <span data-ttu-id="77de4-274">Kodakondsusjärgse riigi regioon (ainult Mehhiko puhul)</span><span class="sxs-lookup"><span data-stu-id="77de4-274">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="77de4-275">Aadressiteave</span><span class="sxs-lookup"><span data-stu-id="77de4-275">Address information</span></span>

- <span data-ttu-id="77de4-276">Tänava nimi ja hoone number (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-276">Primary (required)</span></span>
- <span data-ttu-id="77de4-277">Riik/regioon (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-277">Country/region (required)</span></span>
- <span data-ttu-id="77de4-278">Sihtnumber (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-278">Postal code (required)</span></span>
- <span data-ttu-id="77de4-279">Tänava number (kohustuslik) (ainult Mehhiko puhul)</span><span class="sxs-lookup"><span data-stu-id="77de4-279">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="77de4-280">Hoone tähis (ainult Mehhiko puhul)</span><span class="sxs-lookup"><span data-stu-id="77de4-280">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="77de4-281">Linn (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-281">City (required)</span></span>
- <span data-ttu-id="77de4-282">Osariik (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-282">State (required)</span></span>
- <span data-ttu-id="77de4-283">Maakond (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-283">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="77de4-284">Kontaktteave</span><span class="sxs-lookup"><span data-stu-id="77de4-284">Contact information</span></span> 

- <span data-ttu-id="77de4-285">Tänava nimi ja hoone number (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-285">Primary (required)</span></span>
- <span data-ttu-id="77de4-286">Kontaktnumber (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-286">Contact number (required)</span></span>
- <span data-ttu-id="77de4-287">Sisetelefon</span><span class="sxs-lookup"><span data-stu-id="77de4-287">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="77de4-288">Palgateave ja tulukoodid</span><span class="sxs-lookup"><span data-stu-id="77de4-288">Payroll information and earning codes</span></span>

<span data-ttu-id="77de4-289">Töövõtjatele võidakse määrata teatud maksesagedusega konkreetsed tulud ja neil võivad olla eelistatud makseviisid.</span><span class="sxs-lookup"><span data-stu-id="77de4-289">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="77de4-290">Nende eelistuste ja sätete kasutamise tagamiseks kasutatakse Dayforce’is järgmisi välju.</span><span class="sxs-lookup"><span data-stu-id="77de4-290">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="77de4-291">Tulukoodid</span><span class="sxs-lookup"><span data-stu-id="77de4-291">Earning codes</span></span>

- <span data-ttu-id="77de4-292">Ametikoht (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-292">Position (required)</span></span>
- <span data-ttu-id="77de4-293">Tulukood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-293">Earning Code (required)</span></span>
- <span data-ttu-id="77de4-294">Maksesagedus (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-294">Frequency (required)</span></span>
- <span data-ttu-id="77de4-295">Summa (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-295">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="77de4-296">Palgateave</span><span class="sxs-lookup"><span data-stu-id="77de4-296">Payroll information</span></span>

- <span data-ttu-id="77de4-297">Makseviis</span><span class="sxs-lookup"><span data-stu-id="77de4-297">Payment Method</span></span>
- <span data-ttu-id="77de4-298">Majanduspiirkond (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-298">Economic Region (required)</span></span>
- <span data-ttu-id="77de4-299">Töövõtja soodustuste ID</span><span class="sxs-lookup"><span data-stu-id="77de4-299">Employee Benefits ID</span></span>
- <span data-ttu-id="77de4-300">Riiklik isikukood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-300">National ID Number (required)</span></span>
- <span data-ttu-id="77de4-301">Sõjaväeteenistuse number</span><span class="sxs-lookup"><span data-stu-id="77de4-301">Military Service Number</span></span>
- <span data-ttu-id="77de4-302">Vahetuse ID (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-302">Shift ID (required)</span></span>
- <span data-ttu-id="77de4-303">Maksukood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-303">Tax Number (required)</span></span>
- <span data-ttu-id="77de4-304">Ühingu ID (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-304">Union ID (required)</span></span>
- <span data-ttu-id="77de4-305">Tööpäeva ID (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-305">Work Day ID (required)</span></span>
- <span data-ttu-id="77de4-306">Tööloa number</span><span class="sxs-lookup"><span data-stu-id="77de4-306">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="77de4-307">Mehhiko toetab järgmisi makseviise: **sularaha**, **tšekk** (ettevõtte füüsiline tšekk) ja **elektrooniline makse**.</span><span class="sxs-lookup"><span data-stu-id="77de4-307">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="77de4-308">Kui makseviisi pole määratud, kasutatakse vaikevalikut **tšekk**.</span><span class="sxs-lookup"><span data-stu-id="77de4-308">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="77de4-309">Töösuhte üksikasjad</span><span class="sxs-lookup"><span data-stu-id="77de4-309">Employment details</span></span>

<span data-ttu-id="77de4-310">Töösuhte üksikasjade ajalugu on põhiline teave, millest tuletatakse rakenduses Dayforce töövõtja palkamise, töösuhte lõpetamise ja uuesti palkamise olekud.</span><span class="sxs-lookup"><span data-stu-id="77de4-310">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="77de4-311">Dayforce toetab korraga ainult ühte aktiivset töösuhte kirjet.</span><span class="sxs-lookup"><span data-stu-id="77de4-311">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="77de4-312">Töösuhte alguskuupäev (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-312">Employment start date (required)</span></span>
- <span data-ttu-id="77de4-313">Töösuhte lõppkuupäev</span><span class="sxs-lookup"><span data-stu-id="77de4-313">Employment end date</span></span>
- <span data-ttu-id="77de4-314">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="77de4-314">Start date</span></span>
- <span data-ttu-id="77de4-315">Korrigeeritud alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="77de4-315">Adjusted start date</span></span>
- <span data-ttu-id="77de4-316">Töösuhte lõpetamise kuupäev (kohustuslik lõpetamisel)</span><span class="sxs-lookup"><span data-stu-id="77de4-316">Termination date (required upon termination)</span></span>
- <span data-ttu-id="77de4-317">Töösuhte lõpetamise põhjus (kohustuslik lõpetamisel)</span><span class="sxs-lookup"><span data-stu-id="77de4-317">Termination reason (required upon termination)</span></span>

<span data-ttu-id="77de4-318">Töövõtja tähtsaimad kuupäevad tuletatakse järgmisest teabest.</span><span class="sxs-lookup"><span data-stu-id="77de4-318">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="77de4-319">Talent</span><span class="sxs-lookup"><span data-stu-id="77de4-319">Talent</span></span>                | <span data-ttu-id="77de4-320">Dayforce</span><span class="sxs-lookup"><span data-stu-id="77de4-320">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77de4-321">Kõige värskem palkamise kuupäev</span><span class="sxs-lookup"><span data-stu-id="77de4-321">Most recent hire date</span></span> | <span data-ttu-id="77de4-322">Praeguse lõpetamata töösuhte ajalookirje alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="77de4-322">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="77de4-323">Lõpetamiskuupäev</span><span class="sxs-lookup"><span data-stu-id="77de4-323">Termination date</span></span>      | <span data-ttu-id="77de4-324">Praeguse lõpetamata töösuhte ajalookirje lõpetamise kuupäev</span><span class="sxs-lookup"><span data-stu-id="77de4-324">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="77de4-325">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="77de4-325">Start date</span></span>            | <span data-ttu-id="77de4-326">Korrigeeritud alguskuupäev, alguskuupäev või praeguse passiivse töösuhte ajalookirje alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="77de4-326">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="77de4-327">Palkamise algne kuupäev</span><span class="sxs-lookup"><span data-stu-id="77de4-327">Original hire date</span></span>    | <span data-ttu-id="77de4-328">Varaseima töösuhte ajalookirje alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="77de4-328">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="77de4-329">Hüvitus</span><span class="sxs-lookup"><span data-stu-id="77de4-329">Compensation</span></span>

<span data-ttu-id="77de4-330">Tööhõiveperioodi jooksul peab iga töövõtja peamise ametikohaga olema seotud põhipalgaplaan.</span><span class="sxs-lookup"><span data-stu-id="77de4-330">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="77de4-331">See periood algab kuupäeval, mil töövõtja palgati (või töösuhte alguskuupäeval), ja jätkub kuni töösuhte lõpetamiseni.</span><span class="sxs-lookup"><span data-stu-id="77de4-331">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="77de4-332">Kehtivuse algus (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-332">Effective Date (required)</span></span>
- <span data-ttu-id="77de4-333">Aegumiskuupäev</span><span class="sxs-lookup"><span data-stu-id="77de4-333">Expiration date</span></span>
- <span data-ttu-id="77de4-334">Palgamäär (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-334">Pay Rate (required)</span></span>
- <span data-ttu-id="77de4-335">Palgamäära teisendamised (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-335">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="77de4-336">Aastane vaste (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-336">Annual equivalent (required)</span></span>
- <span data-ttu-id="77de4-337">Tunnine vaste (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-337">Hourly equivalent (required)</span></span>

<span data-ttu-id="77de4-338">Kui tunnimääraga töövõtjal on mitu ametikohta, siis imporditakse peamise ametikoha põhipalk rakendusse Dayforce töövõtja taseme põhimäärana/-palgana.</span><span class="sxs-lookup"><span data-stu-id="77de4-338">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="77de4-339">Teiseste ametikohtade puhul salvestatakse Dayforce’is tunnimäär vastava ametikoha jaoks.</span><span class="sxs-lookup"><span data-stu-id="77de4-339">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="77de4-340">Kui kuupalgaga töötajal on mitu ametikohta, siis kasutatakse töövõtja taseme põhimäärana/-palgana kõikide aktiivsete ametikohtade tuletatud kumulatiivset tunnimäära ja aastapalka.</span><span class="sxs-lookup"><span data-stu-id="77de4-340">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="77de4-341">ID-numbrid</span><span class="sxs-lookup"><span data-stu-id="77de4-341">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="77de4-342">Isiku identifikaator</span><span class="sxs-lookup"><span data-stu-id="77de4-342">Social Security identifier</span></span> 

<span data-ttu-id="77de4-343">Igal töövõtjal peab olema üks peamine identifikaator.</span><span class="sxs-lookup"><span data-stu-id="77de4-343">Every employee must have one primary identifier.</span></span> <span data-ttu-id="77de4-344">Identifikaator peab olema isikukoodi- ehk **SSN**-tüüpi.</span><span class="sxs-lookup"><span data-stu-id="77de4-344">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="77de4-345">Rakenduses Dayforce tuletatakse see automaatselt töövõtja isiku identifikaatorina, mis on palkamiseks vajalik.</span><span class="sxs-lookup"><span data-stu-id="77de4-345">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="77de4-346">Peamine isikukood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-346">Primary (required)</span></span>
- <span data-ttu-id="77de4-347">ID tüüp = SSN</span><span class="sxs-lookup"><span data-stu-id="77de4-347">Identification Type = "SSN"</span></span>
- <span data-ttu-id="77de4-348">Väljastamise kuupäev</span><span class="sxs-lookup"><span data-stu-id="77de4-348">Issued Date</span></span>
- <span data-ttu-id="77de4-349">Aegumiskuupäev</span><span class="sxs-lookup"><span data-stu-id="77de4-349">Expiration Date</span></span>

<span data-ttu-id="77de4-350">Töövõtjad saavad deklareerida mitu **SSN**-identifitseerimistüüpi ID-numbrit.</span><span class="sxs-lookup"><span data-stu-id="77de4-350">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="77de4-351">Dayforce’i integreeritakse vaid tähistusega **Peamine** kirje, olenemata sellest, kas number on aktiivne või aegunud.</span><span class="sxs-lookup"><span data-stu-id="77de4-351">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="77de4-352">Pangakontod ja väljamaksed</span><span class="sxs-lookup"><span data-stu-id="77de4-352">Bank accounts and disbursements</span></span>

<span data-ttu-id="77de4-353">Iga töötaja jaoks, kes soovib oma palka pangakonto ülekandena kätte saada, tuleb sisestada kehtiv pangakonto teave.</span><span class="sxs-lookup"><span data-stu-id="77de4-353">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="77de4-354">Talent</span><span class="sxs-lookup"><span data-stu-id="77de4-354">Talent</span></span>                         | <span data-ttu-id="77de4-355">Dayforce</span><span class="sxs-lookup"><span data-stu-id="77de4-355">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77de4-356">Pangakonto number (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-356">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="77de4-357">SWIFT-kood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-357">SWIFT code (required)</span></span>          | <span data-ttu-id="77de4-358">Välja **Panga ID** kasutatakse palgaarvestuse töötlemiseks Mehhikos.</span><span class="sxs-lookup"><span data-stu-id="77de4-358">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="77de4-359">Filiaali kood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-359">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="77de4-360">Pangakonto tüüp (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-360">Bank account type (required)</span></span>   | <span data-ttu-id="77de4-361">Välja **Konto tüüp** kasutatakse palgaarvestuse töötlemiseks Mehhikos.</span><span class="sxs-lookup"><span data-stu-id="77de4-361">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="77de4-362">Toetatud väärtused on **Jooksevkonto** ja **Palgakonto**</span><span class="sxs-lookup"><span data-stu-id="77de4-362">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="77de4-363">Töövõtjad, kes soovivad oma palka pangakonto ülekannetena kätte saada, peavad esitama lingi jäägikontole, mis on juriidilise isiku alluvuses, kelle peamine aadress on Mehhikos ja kes on seotud Mehhiko panga kehtiva pangakontoga.</span><span class="sxs-lookup"><span data-stu-id="77de4-363">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="77de4-364">Kõiki ülejäänuid kontosid, mis pole jäägikontod, eiratakse.</span><span class="sxs-lookup"><span data-stu-id="77de4-364">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="77de4-365">Aadressiteave</span><span class="sxs-lookup"><span data-stu-id="77de4-365">Address information</span></span>

<span data-ttu-id="77de4-366">Igal töövõtjal peab olema üks peamine asukoht.</span><span class="sxs-lookup"><span data-stu-id="77de4-366">Every employee must have one primary location.</span></span> <span data-ttu-id="77de4-367">Dayforce’is kasutatakse seda asukohta, et määratleda töövõtja peamine elukoht maksustamise tarbeks.</span><span class="sxs-lookup"><span data-stu-id="77de4-367">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="77de4-368">Peamine elukoht (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-368">Primary (required)</span></span>
- <span data-ttu-id="77de4-369">Riik/regioon (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-369">Country/region (required)</span></span>
- <span data-ttu-id="77de4-370">Sihtnumber (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-370">Zip/postal code (required)</span></span>
- <span data-ttu-id="77de4-371">Tänava nimi (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-371">Street (required)</span></span>
- <span data-ttu-id="77de4-372">Tänava number (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-372">Street Number (required)</span></span>
- <span data-ttu-id="77de4-373">Hoone tähis</span><span class="sxs-lookup"><span data-stu-id="77de4-373">Building Complement</span></span>
- <span data-ttu-id="77de4-374">Linn (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-374">City (required)</span></span>
- <span data-ttu-id="77de4-375">Osariik (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-375">State (required)</span></span>
- <span data-ttu-id="77de4-376">Maakond (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-376">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="77de4-377">Andmete konfigureerimine palgaandmete loomiseks Ameerika Ühendriikides ja Kanadas</span><span class="sxs-lookup"><span data-stu-id="77de4-377">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="77de4-378">Kui loote palgaandmeid Ameerika Ühendriikide või Kanada töövõtjatele, siis peate konfigureerima järgmisi elemente.</span><span class="sxs-lookup"><span data-stu-id="77de4-378">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="77de4-379">Ametikohtadele tuleb määrata osakonnad.</span><span class="sxs-lookup"><span data-stu-id="77de4-379">Departments are required on positions.</span></span>
- <span data-ttu-id="77de4-380">Kulukeskused tuleb määratleda finantsdimensioonideks ja peavad olema vaike-finantsdimensiooni stringi esimene element.</span><span class="sxs-lookup"><span data-stu-id="77de4-380">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="77de4-381">Saate konfigureerida rakenduse Talent nõudma, et ametikohad määraksid osakonna.</span><span class="sxs-lookup"><span data-stu-id="77de4-381">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="77de4-382">Selleks valige **Inimressursside ühised ametikohad > Ametikohad > Nõua ametikohtade puhul osakondi**.</span><span class="sxs-lookup"><span data-stu-id="77de4-382">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="77de4-383">Soovitame selle sätte integreerimiseks jõustada.</span><span class="sxs-lookup"><span data-stu-id="77de4-383">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="77de4-384">Töötüübid</span><span class="sxs-lookup"><span data-stu-id="77de4-384">Job types</span></span>

<span data-ttu-id="77de4-385">Töötüüpe kasutatakse sarnaste tööde kategooriatesse grupeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="77de4-385">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="77de4-386">Töötüübid on vajalikud palgaarvestuse töötlemiseks Ameerika Ühendriikides ja Kanadas.</span><span class="sxs-lookup"><span data-stu-id="77de4-386">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="77de4-387">Töötüübid on näiteks täistööaeg ja osaline tööaeg või kuupalk ning tunnipalk.</span><span class="sxs-lookup"><span data-stu-id="77de4-387">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="77de4-388">Töötüübid vastendatakse Dayforce’i tasutüüpidena, mis näitavad, kas töövõtja on tunni- või palgatöötaja.</span><span class="sxs-lookup"><span data-stu-id="77de4-388">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="77de4-389">Järgmised töötüübid ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="77de4-389">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="77de4-390">Töö tüüp</span><span class="sxs-lookup"><span data-stu-id="77de4-390">Job type</span></span>   | <span data-ttu-id="77de4-391">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="77de4-391">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="77de4-392">Tunnimäär</span><span class="sxs-lookup"><span data-stu-id="77de4-392">Hourly</span></span>     | <span data-ttu-id="77de4-393">Tunnimäär</span><span class="sxs-lookup"><span data-stu-id="77de4-393">Hourly</span></span>      |
| <span data-ttu-id="77de4-394">Põhipalk</span><span class="sxs-lookup"><span data-stu-id="77de4-394">Salaried</span></span>   | <span data-ttu-id="77de4-395">Põhipalk</span><span class="sxs-lookup"><span data-stu-id="77de4-395">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="77de4-396">Ametikoha tüübid</span><span class="sxs-lookup"><span data-stu-id="77de4-396">Position types</span></span> 

<span data-ttu-id="77de4-397">Ametikoha tüüpe kasutatakse selleks, et kirjeldada, kas ametikoht on täiskohaga, osalise tööajaga või midagi muud.</span><span class="sxs-lookup"><span data-stu-id="77de4-397">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="77de4-398">Ametikoha tüübid vastendatakse Dayforce’i tasuklassidena, mis näitavad, kas töövõtja on täis- või osalise tööajaga töötaja.</span><span class="sxs-lookup"><span data-stu-id="77de4-398">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="77de4-399">Järgmised ametikoha tüübid ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="77de4-399">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="77de4-400">Ametikoha tüüp</span><span class="sxs-lookup"><span data-stu-id="77de4-400">Position type</span></span>   | <span data-ttu-id="77de4-401">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="77de4-401">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="77de4-402">Täistööaeg</span><span class="sxs-lookup"><span data-stu-id="77de4-402">Full-time</span></span>       | <span data-ttu-id="77de4-403">Täistööajaga töövõtja</span><span class="sxs-lookup"><span data-stu-id="77de4-403">Full time employee</span></span> |
| <span data-ttu-id="77de4-404">Osaline tööaeg</span><span class="sxs-lookup"><span data-stu-id="77de4-404">Part-time</span></span>       | <span data-ttu-id="77de4-405">Osalise tööajaga töövõtja</span><span class="sxs-lookup"><span data-stu-id="77de4-405">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="77de4-406">Põhjuse koodid</span><span class="sxs-lookup"><span data-stu-id="77de4-406">Reason codes</span></span>

<span data-ttu-id="77de4-407">Põhjusekoodid annavad teavet töövõtja oleku kohta.</span><span class="sxs-lookup"><span data-stu-id="77de4-407">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="77de4-408">Põhjusekoodid vastendatakse Dayforce’i olekupõhjustena, mis näitavad töövõtja ametikoha või töösuhte oleku muutuse põhjust.</span><span class="sxs-lookup"><span data-stu-id="77de4-408">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="77de4-409">Järgmised põhjusekoodid ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="77de4-409">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="77de4-410">Põhjusekood</span><span class="sxs-lookup"><span data-stu-id="77de4-410">Reason code</span></span>    | <span data-ttu-id="77de4-411">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="77de4-411">Description</span></span>      | <span data-ttu-id="77de4-412">Rakendatavad stsenaariumid</span><span class="sxs-lookup"><span data-stu-id="77de4-412">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="77de4-413">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="77de4-413">RESIGNATION</span></span>    | <span data-ttu-id="77de4-414">Lahkumine</span><span class="sxs-lookup"><span data-stu-id="77de4-414">Resignation</span></span>      | <span data-ttu-id="77de4-415">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="77de4-415">Terminate worker</span></span>     |
| <span data-ttu-id="77de4-416">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="77de4-416">TERMINATION</span></span>    | <span data-ttu-id="77de4-417">Lõpetamine</span><span class="sxs-lookup"><span data-stu-id="77de4-417">Termination</span></span>      | <span data-ttu-id="77de4-418">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="77de4-418">Terminate worker</span></span>     |
| <span data-ttu-id="77de4-419">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="77de4-419">RETIREMENT</span></span>     | <span data-ttu-id="77de4-420">Pensionile jäämine</span><span class="sxs-lookup"><span data-stu-id="77de4-420">Retirement</span></span>       | <span data-ttu-id="77de4-421">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="77de4-421">Terminate worker</span></span>     |
| <span data-ttu-id="77de4-422">OTHER</span><span class="sxs-lookup"><span data-stu-id="77de4-422">OTHER</span></span>          | <span data-ttu-id="77de4-423">Muud põhjused</span><span class="sxs-lookup"><span data-stu-id="77de4-423">Other Reasons</span></span>    | <span data-ttu-id="77de4-424">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="77de4-424">Terminate worker</span></span>     |
| <span data-ttu-id="77de4-425">DEATH</span><span class="sxs-lookup"><span data-stu-id="77de4-425">DEATH</span></span>          | <span data-ttu-id="77de4-426">Surm</span><span class="sxs-lookup"><span data-stu-id="77de4-426">Death</span></span>            | <span data-ttu-id="77de4-427">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="77de4-427">Terminate worker</span></span>     |
| <span data-ttu-id="77de4-428">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="77de4-428">LEAVEOFABSENCE</span></span> | <span data-ttu-id="77de4-429">Puhkus</span><span class="sxs-lookup"><span data-stu-id="77de4-429">Leave of Absence</span></span> | <span data-ttu-id="77de4-430">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="77de4-430">Terminate worker</span></span>     |
| <span data-ttu-id="77de4-431">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="77de4-431">CONTRACTEND</span></span>    | <span data-ttu-id="77de4-432">Lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="77de4-432">End of Contract</span></span>  | <span data-ttu-id="77de4-433">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="77de4-433">Terminate worker</span></span>     |
| <span data-ttu-id="77de4-434">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="77de4-434">SALARYCHANGE</span></span>   | <span data-ttu-id="77de4-435">Palga muutus</span><span class="sxs-lookup"><span data-stu-id="77de4-435">Change of Salary</span></span> | <span data-ttu-id="77de4-436">Hüvitus</span><span class="sxs-lookup"><span data-stu-id="77de4-436">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="77de4-437">Perekonnaseis</span><span class="sxs-lookup"><span data-stu-id="77de4-437">Marital status</span></span>

<span data-ttu-id="77de4-438">Perekonnaseisu väärtused vastendatakse Dayforce’i ja tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.</span><span class="sxs-lookup"><span data-stu-id="77de4-438">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="77de4-439">Järgmine tabel näitab, kuidas perekonnaseisu väärtusi Dayforce’i vastendatakse.</span><span class="sxs-lookup"><span data-stu-id="77de4-439">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="77de4-440">Talent</span><span class="sxs-lookup"><span data-stu-id="77de4-440">Talent</span></span>                 | <span data-ttu-id="77de4-441">Dayforce</span><span class="sxs-lookup"><span data-stu-id="77de4-441">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="77de4-442">Abielus</span><span class="sxs-lookup"><span data-stu-id="77de4-442">Married</span></span>                | <span data-ttu-id="77de4-443">Abielus</span><span class="sxs-lookup"><span data-stu-id="77de4-443">Married</span></span>              |
| <span data-ttu-id="77de4-444">Üksik</span><span class="sxs-lookup"><span data-stu-id="77de4-444">Single</span></span>                 | <span data-ttu-id="77de4-445">Üksik</span><span class="sxs-lookup"><span data-stu-id="77de4-445">Single</span></span>               |
| <span data-ttu-id="77de4-446">Lesk</span><span class="sxs-lookup"><span data-stu-id="77de4-446">Widowed</span></span>                | <span data-ttu-id="77de4-447">Lesk</span><span class="sxs-lookup"><span data-stu-id="77de4-447">Widowed</span></span>              |
| <span data-ttu-id="77de4-448">Lahutatud</span><span class="sxs-lookup"><span data-stu-id="77de4-448">Divorced</span></span>               | <span data-ttu-id="77de4-449">Lahutatud</span><span class="sxs-lookup"><span data-stu-id="77de4-449">Divorced</span></span>             |
| <span data-ttu-id="77de4-450">Registreeritud partnerlus</span><span class="sxs-lookup"><span data-stu-id="77de4-450">Registered Partnership</span></span> | <span data-ttu-id="77de4-451">Mitteabieluline kooselu</span><span class="sxs-lookup"><span data-stu-id="77de4-451">Domestic Partnership</span></span> |
| <span data-ttu-id="77de4-452">None</span><span class="sxs-lookup"><span data-stu-id="77de4-452">None</span></span>                   | <span data-ttu-id="77de4-453">None</span><span class="sxs-lookup"><span data-stu-id="77de4-453">None</span></span>                 |
| <span data-ttu-id="77de4-454">Kooselu</span><span class="sxs-lookup"><span data-stu-id="77de4-454">Cohabiting</span></span>             | <span data-ttu-id="77de4-455">Kooselu</span><span class="sxs-lookup"><span data-stu-id="77de4-455">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="77de4-456">Sugu</span><span class="sxs-lookup"><span data-stu-id="77de4-456">Gender</span></span>

<span data-ttu-id="77de4-457">Soo määratlused vastendatakse Dayforce’i ja tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.</span><span class="sxs-lookup"><span data-stu-id="77de4-457">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="77de4-458">Järgmine tabel näitab, kuidas soo määratlusi Dayforce’i vastendatakse.</span><span class="sxs-lookup"><span data-stu-id="77de4-458">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="77de4-459">Talent</span><span class="sxs-lookup"><span data-stu-id="77de4-459">Talent</span></span>       | <span data-ttu-id="77de4-460">Dayforce</span><span class="sxs-lookup"><span data-stu-id="77de4-460">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="77de4-461">Mees</span><span class="sxs-lookup"><span data-stu-id="77de4-461">Male</span></span>         | <span data-ttu-id="77de4-462">Mees</span><span class="sxs-lookup"><span data-stu-id="77de4-462">Male</span></span>            |
| <span data-ttu-id="77de4-463">Naine</span><span class="sxs-lookup"><span data-stu-id="77de4-463">Female</span></span>       | <span data-ttu-id="77de4-464">Naine</span><span class="sxs-lookup"><span data-stu-id="77de4-464">Female</span></span>          |
| <span data-ttu-id="77de4-465">Mittespetsiifiline</span><span class="sxs-lookup"><span data-stu-id="77de4-465">Non-specific</span></span> | <span data-ttu-id="77de4-466">*Ei toetata*</span><span class="sxs-lookup"><span data-stu-id="77de4-466">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="77de4-467">Tulukoodid</span><span class="sxs-lookup"><span data-stu-id="77de4-467">Earning codes</span></span>

<span data-ttu-id="77de4-468">Tulukoodid määratlevad kordumatult igat tüüpi tulud, mida töötajad saavad.</span><span class="sxs-lookup"><span data-stu-id="77de4-468">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="77de4-469">Koodid hõlmavad mitmeid tuludega seotud parameetreid, näiteks raamatupidamisreeglid, maksuseadused, aruandluse nõuded ja brutosumma võime.</span><span class="sxs-lookup"><span data-stu-id="77de4-469">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="77de4-470">Kui kasutatakse toetuseta sagedust, siis kasutatakse arvutamise jaoks vaikimisi sagedust **Iga makse**.</span><span class="sxs-lookup"><span data-stu-id="77de4-470">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="77de4-471">Toetatud sagedused</span><span class="sxs-lookup"><span data-stu-id="77de4-471">Supported frequencies</span></span>

- <span data-ttu-id="77de4-472">Kõik</span><span class="sxs-lookup"><span data-stu-id="77de4-472">All</span></span>
- <span data-ttu-id="77de4-473">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="77de4-473">EVERYPAY</span></span>
- <span data-ttu-id="77de4-474">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="77de4-474">EACHPAYPERIOD</span></span>
- <span data-ttu-id="77de4-475">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="77de4-475">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="77de4-476">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="77de4-476">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="77de4-477">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="77de4-477">1OFMTH</span></span>
- <span data-ttu-id="77de4-478">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="77de4-478">LASTOFMTH</span></span>
- <span data-ttu-id="77de4-479">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="77de4-479">2OFMTH</span></span>
- <span data-ttu-id="77de4-480">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="77de4-480">3OFMTH</span></span>
- <span data-ttu-id="77de4-481">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="77de4-481">4OFMTH</span></span>
- <span data-ttu-id="77de4-482">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="77de4-482">5OFMTH</span></span>
- <span data-ttu-id="77de4-483">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="77de4-483">1N2OFMTH</span></span>
- <span data-ttu-id="77de4-484">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="77de4-484">3N4OFMTH</span></span>
- <span data-ttu-id="77de4-485">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="77de4-485">1N3OFMTH</span></span>
- <span data-ttu-id="77de4-486">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="77de4-486">1N4OFMTH</span></span>
- <span data-ttu-id="77de4-487">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="77de4-487">2N3OFMTH</span></span>
- <span data-ttu-id="77de4-488">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="77de4-488">2N4OFMTH</span></span>
- <span data-ttu-id="77de4-489">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="77de4-489">1N2N3OFMTH</span></span>
- <span data-ttu-id="77de4-490">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="77de4-490">1N2N4OFMTH</span></span>
- <span data-ttu-id="77de4-491">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="77de4-491">1N3N4OFMTH</span></span>
- <span data-ttu-id="77de4-492">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="77de4-492">2N3N4OFMTH</span></span>
- <span data-ttu-id="77de4-493">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="77de4-493">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="77de4-494">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="77de4-494">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="77de4-495">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="77de4-495">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="77de4-496">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="77de4-496">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="77de4-497">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="77de4-497">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="77de4-498">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="77de4-498">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="77de4-499">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="77de4-499">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="77de4-500">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="77de4-500">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="77de4-501">Aadressid</span><span class="sxs-lookup"><span data-stu-id="77de4-501">Addresses</span></span>

<span data-ttu-id="77de4-502">Teatud riigi või regiooni, osariigi ja maakonna (haldusüksuse) koodide tuvastamise jaoks on vaja kindlaid vorminguid, mida Dayforce ning riigi-/regioonisisesed pakkujad ära tunnevad.</span><span class="sxs-lookup"><span data-stu-id="77de4-502">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="77de4-503">Kuigi linnade vorming on paindlik, peab iga linn olema seotud osariigiga.</span><span class="sxs-lookup"><span data-stu-id="77de4-503">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="77de4-504">Talent</span><span class="sxs-lookup"><span data-stu-id="77de4-504">Talent</span></span>          | <span data-ttu-id="77de4-505">Dayforce</span><span class="sxs-lookup"><span data-stu-id="77de4-505">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="77de4-506">Riik/regioon</span><span class="sxs-lookup"><span data-stu-id="77de4-506">Country/Region</span></span>  | <span data-ttu-id="77de4-507">Riigi kood</span><span class="sxs-lookup"><span data-stu-id="77de4-507">Country Code</span></span>          |
| <span data-ttu-id="77de4-508">Sihtnumber</span><span class="sxs-lookup"><span data-stu-id="77de4-508">Zip/Postal Code</span></span> | <span data-ttu-id="77de4-509">Sihtnumber</span><span class="sxs-lookup"><span data-stu-id="77de4-509">Postal Code</span></span>           |
| <span data-ttu-id="77de4-510">Osariik</span><span class="sxs-lookup"><span data-stu-id="77de4-510">State</span></span>           | <span data-ttu-id="77de4-511">Osariigi kood</span><span class="sxs-lookup"><span data-stu-id="77de4-511">State Code</span></span>            |
| <span data-ttu-id="77de4-512">Linn</span><span class="sxs-lookup"><span data-stu-id="77de4-512">City</span></span>            | <span data-ttu-id="77de4-513">Linn</span><span class="sxs-lookup"><span data-stu-id="77de4-513">City</span></span>                  |
| <span data-ttu-id="77de4-514">Maakond</span><span class="sxs-lookup"><span data-stu-id="77de4-514">County</span></span>          | <span data-ttu-id="77de4-515">Maakond (haldusüksus)</span><span class="sxs-lookup"><span data-stu-id="77de4-515">County (Municipality)</span></span> |
| <span data-ttu-id="77de4-516">Tänav</span><span class="sxs-lookup"><span data-stu-id="77de4-516">Street</span></span>          | <span data-ttu-id="77de4-517">Aadressirida 1</span><span class="sxs-lookup"><span data-stu-id="77de4-517">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="77de4-518">Maksuregioonid</span><span class="sxs-lookup"><span data-stu-id="77de4-518">Tax regions</span></span>

<span data-ttu-id="77de4-519">Maksuregioone kasutatakse palga loomisel sobiva maksu määramiseks.</span><span class="sxs-lookup"><span data-stu-id="77de4-519">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="77de4-520">Maksuregioonid vastendatakse Dayforce’i asukoha-aadressidena.</span><span class="sxs-lookup"><span data-stu-id="77de4-520">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="77de4-521">Maksuregiooni vaikevariant peab olema seotud töötaja aktiivse ametikohaga.</span><span class="sxs-lookup"><span data-stu-id="77de4-521">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="77de4-522">Maksuregioon (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-522">Tax region (required)</span></span>
- <span data-ttu-id="77de4-523">Riik/regioon (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-523">Country/Region (required)</span></span>
- <span data-ttu-id="77de4-524">Osariik (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-524">State (required)</span></span>
- <span data-ttu-id="77de4-525">Maakond</span><span class="sxs-lookup"><span data-stu-id="77de4-525">County</span></span> 
- <span data-ttu-id="77de4-526">Linn (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="77de4-526">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="77de4-527">Andmete konfigureerimine palgaandmete loomiseks Mehhikos</span><span class="sxs-lookup"><span data-stu-id="77de4-527">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="77de4-528">Kui loote palgaandmeid Mehhiko töövõtjatele, siis peate konfigureerima järgmisi elemente.</span><span class="sxs-lookup"><span data-stu-id="77de4-528">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="77de4-529">Ametikohtadele tuleb määrata osakonnad.</span><span class="sxs-lookup"><span data-stu-id="77de4-529">Departments are required on positions.</span></span>
- <span data-ttu-id="77de4-530">Kulukeskused tuleb määratleda finantsdimensioonideks ja peavad olema vaike-finantsdimensiooni stringi esimene element.</span><span class="sxs-lookup"><span data-stu-id="77de4-530">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="77de4-531">Töötüübid</span><span class="sxs-lookup"><span data-stu-id="77de4-531">Job types</span></span>

<span data-ttu-id="77de4-532">Töötüüpe kasutatakse sarnaste tööde kategooriatesse grupeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="77de4-532">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="77de4-533">Mehhikos palgaarvestuse töötlemiseks on vajalikud töötüübid.</span><span class="sxs-lookup"><span data-stu-id="77de4-533">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="77de4-534">Töötüübid on näiteks täistööaeg ja osaline tööaeg või kuupalk ning tunnipalk.</span><span class="sxs-lookup"><span data-stu-id="77de4-534">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="77de4-535">Töötüübid vastendatakse Dayforce’i tasutüüpidena, mis näitavad, kas töövõtja on tunni- või palgatöötaja.</span><span class="sxs-lookup"><span data-stu-id="77de4-535">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="77de4-536">Järgmised töötüübid ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="77de4-536">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="77de4-537">Töö tüüp</span><span class="sxs-lookup"><span data-stu-id="77de4-537">Job type</span></span>   | <span data-ttu-id="77de4-538">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="77de4-538">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="77de4-539">Tunnimäär</span><span class="sxs-lookup"><span data-stu-id="77de4-539">Hourly</span></span>     | <span data-ttu-id="77de4-540">MX tunnimäär</span><span class="sxs-lookup"><span data-stu-id="77de4-540">MX Hourly</span></span>   |
| <span data-ttu-id="77de4-541">Põhipalk</span><span class="sxs-lookup"><span data-stu-id="77de4-541">Salaried</span></span>   | <span data-ttu-id="77de4-542">MX põhipalk</span><span class="sxs-lookup"><span data-stu-id="77de4-542">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="77de4-543">Positsioonitüübid</span><span class="sxs-lookup"><span data-stu-id="77de4-543">Position types</span></span> 

<span data-ttu-id="77de4-544">Ametikoha tüüpe kasutatakse selleks, et kirjeldada, kas ametikoht on täiskohaga, osalise tööajaga või midagi muud.</span><span class="sxs-lookup"><span data-stu-id="77de4-544">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="77de4-545">Ametikoha tüübid vastendatakse Dayforce’i tasuklassidena, mis näitavad, kas töövõtja on täis- või osalise tööajaga töötaja.</span><span class="sxs-lookup"><span data-stu-id="77de4-545">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="77de4-546">Järgmised ametikoha tüübid ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="77de4-546">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="77de4-547">Ametikoha tüüp</span><span class="sxs-lookup"><span data-stu-id="77de4-547">Position type</span></span>   | <span data-ttu-id="77de4-548">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="77de4-548">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="77de4-549">Täistööaeg</span><span class="sxs-lookup"><span data-stu-id="77de4-549">Full-time</span></span>       | <span data-ttu-id="77de4-550">Täistööajaga töövõtja</span><span class="sxs-lookup"><span data-stu-id="77de4-550">Full time employee</span></span> |
| <span data-ttu-id="77de4-551">Osaline tööaeg</span><span class="sxs-lookup"><span data-stu-id="77de4-551">Part-time</span></span>       | <span data-ttu-id="77de4-552">Osalise tööajaga töövõtja</span><span class="sxs-lookup"><span data-stu-id="77de4-552">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="77de4-553">Põhjuse koodid</span><span class="sxs-lookup"><span data-stu-id="77de4-553">Reason codes</span></span>

<span data-ttu-id="77de4-554">Põhjusekoodid annavad teavet töövõtja oleku kohta.</span><span class="sxs-lookup"><span data-stu-id="77de4-554">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="77de4-555">Põhjusekoodid vastendatakse Dayforce’i olekupõhjustena, mis näitavad töövõtja ametikoha või töösuhte oleku muutuse põhjust.</span><span class="sxs-lookup"><span data-stu-id="77de4-555">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="77de4-556">Järgmised põhjusekoodid ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="77de4-556">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="77de4-557">Põhjusekood</span><span class="sxs-lookup"><span data-stu-id="77de4-557">Reason code</span></span>            | <span data-ttu-id="77de4-558">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="77de4-558">Description</span></span>                    | <span data-ttu-id="77de4-559">Rakendatavad stsenaariumid</span><span class="sxs-lookup"><span data-stu-id="77de4-559">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="77de4-560">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="77de4-560">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="77de4-561">Lahkumine enne esimest palgamakset</span><span class="sxs-lookup"><span data-stu-id="77de4-561">Departure before first payroll</span></span> | <span data-ttu-id="77de4-562">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="77de4-562">Terminate worker</span></span>     |
| <span data-ttu-id="77de4-563">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="77de4-563">RESIGNATION</span></span>            | <span data-ttu-id="77de4-564">Lahkumine</span><span class="sxs-lookup"><span data-stu-id="77de4-564">Resignation</span></span>                    | <span data-ttu-id="77de4-565">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="77de4-565">Terminate worker</span></span>     |
| <span data-ttu-id="77de4-566">PENSION</span><span class="sxs-lookup"><span data-stu-id="77de4-566">PENSION</span></span>                | <span data-ttu-id="77de4-567">Pension</span><span class="sxs-lookup"><span data-stu-id="77de4-567">Pension</span></span>                        | <span data-ttu-id="77de4-568">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="77de4-568">Terminate worker</span></span>     |
| <span data-ttu-id="77de4-569">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="77de4-569">TERMINATION</span></span>            | <span data-ttu-id="77de4-570">Lõpetamine</span><span class="sxs-lookup"><span data-stu-id="77de4-570">Termination</span></span>                    | <span data-ttu-id="77de4-571">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="77de4-571">Terminate worker</span></span>     |
| <span data-ttu-id="77de4-572">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="77de4-572">RETIREMENT</span></span>             | <span data-ttu-id="77de4-573">Pensionile jäämine</span><span class="sxs-lookup"><span data-stu-id="77de4-573">Retirement</span></span>                     | <span data-ttu-id="77de4-574">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="77de4-574">Terminate worker</span></span>     |
| <span data-ttu-id="77de4-575">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="77de4-575">ABSENTEE</span></span>               | <span data-ttu-id="77de4-576">Puuduja</span><span class="sxs-lookup"><span data-stu-id="77de4-576">Absentee</span></span>                       | <span data-ttu-id="77de4-577">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="77de4-577">Terminate worker</span></span>     |
| <span data-ttu-id="77de4-578">OTHER</span><span class="sxs-lookup"><span data-stu-id="77de4-578">OTHER</span></span>                  | <span data-ttu-id="77de4-579">Muud põhjused</span><span class="sxs-lookup"><span data-stu-id="77de4-579">Other Reasons</span></span>                  | <span data-ttu-id="77de4-580">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="77de4-580">Terminate worker</span></span>     |
| <span data-ttu-id="77de4-581">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="77de4-581">CLOSURE</span></span>                | <span data-ttu-id="77de4-582">Ettevõte suletud</span><span class="sxs-lookup"><span data-stu-id="77de4-582">Business Closure</span></span>               | <span data-ttu-id="77de4-583">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="77de4-583">Terminate worker</span></span>     |
| <span data-ttu-id="77de4-584">DEATH</span><span class="sxs-lookup"><span data-stu-id="77de4-584">DEATH</span></span>                  | <span data-ttu-id="77de4-585">Surm</span><span class="sxs-lookup"><span data-stu-id="77de4-585">Death</span></span>                          | <span data-ttu-id="77de4-586">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="77de4-586">Terminate worker</span></span>     |
| <span data-ttu-id="77de4-587">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="77de4-587">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="77de4-588">Puhkus</span><span class="sxs-lookup"><span data-stu-id="77de4-588">Leave of Absence</span></span>               | <span data-ttu-id="77de4-589">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="77de4-589">Terminate worker</span></span>     |
| <span data-ttu-id="77de4-590">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="77de4-590">CONTRACTEND</span></span>            | <span data-ttu-id="77de4-591">Lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="77de4-591">End of Contract</span></span>                | <span data-ttu-id="77de4-592">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="77de4-592">Terminate worker</span></span>     |
| <span data-ttu-id="77de4-593">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="77de4-593">SALARYCHANGE</span></span>           | <span data-ttu-id="77de4-594">Palga muutus</span><span class="sxs-lookup"><span data-stu-id="77de4-594">Change of Salary</span></span>               | <span data-ttu-id="77de4-595">Hüvitus</span><span class="sxs-lookup"><span data-stu-id="77de4-595">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="77de4-596">Töösuhte tingimused</span><span class="sxs-lookup"><span data-stu-id="77de4-596">Terms of employment</span></span>

<span data-ttu-id="77de4-597">Töösuhte tingimusi kasutatakse töösuhte tingimuste kategooriate loomiseks.</span><span class="sxs-lookup"><span data-stu-id="77de4-597">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="77de4-598">Tingimused vastendatakse Dayforce’i töösuhte indikaatorväärtustena.</span><span class="sxs-lookup"><span data-stu-id="77de4-598">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="77de4-599">Järgmised töösuhte tingimused ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="77de4-599">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="77de4-600">Töösuhte tingimused</span><span class="sxs-lookup"><span data-stu-id="77de4-600">Terms of employment</span></span>   | <span data-ttu-id="77de4-601">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="77de4-601">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="77de4-602">Tavaline</span><span class="sxs-lookup"><span data-stu-id="77de4-602">Regular</span></span>               | <span data-ttu-id="77de4-603">Tavaline</span><span class="sxs-lookup"><span data-stu-id="77de4-603">Regular</span></span>     |
| <span data-ttu-id="77de4-604">Otse</span><span class="sxs-lookup"><span data-stu-id="77de4-604">Direct</span></span>                | <span data-ttu-id="77de4-605">Otse</span><span class="sxs-lookup"><span data-stu-id="77de4-605">Direct</span></span>      |
| <span data-ttu-id="77de4-606">Praktika</span><span class="sxs-lookup"><span data-stu-id="77de4-606">Internship</span></span>            | <span data-ttu-id="77de4-607">Praktika</span><span class="sxs-lookup"><span data-stu-id="77de4-607">Internship</span></span>  |
| <span data-ttu-id="77de4-608">Alaline</span><span class="sxs-lookup"><span data-stu-id="77de4-608">Permanent</span></span>             | <span data-ttu-id="77de4-609">Alaline</span><span class="sxs-lookup"><span data-stu-id="77de4-609">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="77de4-610">Perekonnaseis</span><span class="sxs-lookup"><span data-stu-id="77de4-610">Marital status</span></span>

<span data-ttu-id="77de4-611">Perekonnaseisu väärtused vastendatakse Dayforce’i ja tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.</span><span class="sxs-lookup"><span data-stu-id="77de4-611">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="77de4-612">Järgmine tabel näitab, kuidas perekonnaseisu väärtusi Dayforce’i vastendatakse.</span><span class="sxs-lookup"><span data-stu-id="77de4-612">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="77de4-613">Talent</span><span class="sxs-lookup"><span data-stu-id="77de4-613">Talent</span></span>                 | <span data-ttu-id="77de4-614">Dayforce</span><span class="sxs-lookup"><span data-stu-id="77de4-614">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="77de4-615">Abielus</span><span class="sxs-lookup"><span data-stu-id="77de4-615">Married</span></span>                | <span data-ttu-id="77de4-616">Abielus</span><span class="sxs-lookup"><span data-stu-id="77de4-616">Married</span></span>                   |
| <span data-ttu-id="77de4-617">Üksik</span><span class="sxs-lookup"><span data-stu-id="77de4-617">Single</span></span>                 | <span data-ttu-id="77de4-618">Üksik</span><span class="sxs-lookup"><span data-stu-id="77de4-618">Single</span></span>                    |
| <span data-ttu-id="77de4-619">Lesk</span><span class="sxs-lookup"><span data-stu-id="77de4-619">Widowed</span></span>                | <span data-ttu-id="77de4-620">Lesk</span><span class="sxs-lookup"><span data-stu-id="77de4-620">Widowed</span></span>                   |
| <span data-ttu-id="77de4-621">Lahutatud</span><span class="sxs-lookup"><span data-stu-id="77de4-621">Divorced</span></span>               | <span data-ttu-id="77de4-622">Lahutatud</span><span class="sxs-lookup"><span data-stu-id="77de4-622">Divorced</span></span>                  |
| <span data-ttu-id="77de4-623">Registreeritud partnerlus</span><span class="sxs-lookup"><span data-stu-id="77de4-623">Registered Partnership</span></span> | <span data-ttu-id="77de4-624">Mitteabieluline kooselu</span><span class="sxs-lookup"><span data-stu-id="77de4-624">Domestic Partnership</span></span>      |
| <span data-ttu-id="77de4-625">None</span><span class="sxs-lookup"><span data-stu-id="77de4-625">None</span></span>                   | <span data-ttu-id="77de4-626">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="77de4-626">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="77de4-627">Kooselu</span><span class="sxs-lookup"><span data-stu-id="77de4-627">Cohabiting</span></span>             | <span data-ttu-id="77de4-628">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="77de4-628">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="77de4-629">Sugu</span><span class="sxs-lookup"><span data-stu-id="77de4-629">Gender</span></span>

<span data-ttu-id="77de4-630">Soo määratlused vastendatakse Dayforce’i ja tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.</span><span class="sxs-lookup"><span data-stu-id="77de4-630">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="77de4-631">Järgmine tabel näitab, kuidas soo määratlusi Dayforce’i vastendatakse.</span><span class="sxs-lookup"><span data-stu-id="77de4-631">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="77de4-632">Talent</span><span class="sxs-lookup"><span data-stu-id="77de4-632">Talent</span></span>       | <span data-ttu-id="77de4-633">Dayforce</span><span class="sxs-lookup"><span data-stu-id="77de4-633">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="77de4-634">Mees</span><span class="sxs-lookup"><span data-stu-id="77de4-634">Male</span></span>         | <span data-ttu-id="77de4-635">Mees</span><span class="sxs-lookup"><span data-stu-id="77de4-635">Male</span></span>                      |
| <span data-ttu-id="77de4-636">Naine</span><span class="sxs-lookup"><span data-stu-id="77de4-636">Female</span></span>       | <span data-ttu-id="77de4-637">Naine</span><span class="sxs-lookup"><span data-stu-id="77de4-637">Female</span></span>                    |
| <span data-ttu-id="77de4-638">Mittespetsiifiline</span><span class="sxs-lookup"><span data-stu-id="77de4-638">Non-specific</span></span> | <span data-ttu-id="77de4-639">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="77de4-639">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="77de4-640">Makseviis</span><span class="sxs-lookup"><span data-stu-id="77de4-640">Payment method</span></span>

<span data-ttu-id="77de4-641">Makseviisid võimaldavad töövõtjal ja ettevõttel kirjeldada, kuidas töövõtjatele makstakse.</span><span class="sxs-lookup"><span data-stu-id="77de4-641">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="77de4-642">Makseviisid vastendatakse Dayforce’i ja tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.</span><span class="sxs-lookup"><span data-stu-id="77de4-642">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="77de4-643">Järgmine tabel näitab, kuidas makseviise Dayforce’i vastendatakse.</span><span class="sxs-lookup"><span data-stu-id="77de4-643">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="77de4-644">Talent</span><span class="sxs-lookup"><span data-stu-id="77de4-644">Talent</span></span>             | <span data-ttu-id="77de4-645">Dayforce</span><span class="sxs-lookup"><span data-stu-id="77de4-645">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="77de4-646">Sularaha</span><span class="sxs-lookup"><span data-stu-id="77de4-646">Cash</span></span>               | <span data-ttu-id="77de4-647">Sularaha</span><span class="sxs-lookup"><span data-stu-id="77de4-647">Cash</span></span>                      |
| <span data-ttu-id="77de4-648">Elektrooniline makse</span><span class="sxs-lookup"><span data-stu-id="77de4-648">Electronic Payment</span></span> | <span data-ttu-id="77de4-649">Ülekanne</span><span class="sxs-lookup"><span data-stu-id="77de4-649">Transfer</span></span>                  |
| <span data-ttu-id="77de4-650">Kontrolli</span><span class="sxs-lookup"><span data-stu-id="77de4-650">Check</span></span>              | <span data-ttu-id="77de4-651">Tšekk</span><span class="sxs-lookup"><span data-stu-id="77de4-651">Cheque</span></span>                    |
| <span data-ttu-id="77de4-652">Pangaveksel</span><span class="sxs-lookup"><span data-stu-id="77de4-652">Bank Draft</span></span>         | <span data-ttu-id="77de4-653">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="77de4-653">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="77de4-654">Muud</span><span class="sxs-lookup"><span data-stu-id="77de4-654">Other</span></span>              | <span data-ttu-id="77de4-655">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="77de4-655">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="77de4-656">Pangakonto tüüp</span><span class="sxs-lookup"><span data-stu-id="77de4-656">Bank account type</span></span>

<span data-ttu-id="77de4-657">Pangakonto tüüpe kasutatakse elektrooniliste maksete tegemiseks töötajatele.</span><span class="sxs-lookup"><span data-stu-id="77de4-657">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="77de4-658">Pangakonto tüübid vastendatakse Dayforce’i ülekandekonto teabena.</span><span class="sxs-lookup"><span data-stu-id="77de4-658">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="77de4-659">Pangakonto tüübid tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.</span><span class="sxs-lookup"><span data-stu-id="77de4-659">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="77de4-660">Talent</span><span class="sxs-lookup"><span data-stu-id="77de4-660">Talent</span></span>            | <span data-ttu-id="77de4-661">Dayforce</span><span class="sxs-lookup"><span data-stu-id="77de4-661">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="77de4-662">Jooksevkonto</span><span class="sxs-lookup"><span data-stu-id="77de4-662">Checking Account</span></span>  | <span data-ttu-id="77de4-663">Jooksevkonto</span><span class="sxs-lookup"><span data-stu-id="77de4-663">CheckingAccount</span></span>           |
| <span data-ttu-id="77de4-664">Palgakonto</span><span class="sxs-lookup"><span data-stu-id="77de4-664">Payroll Account</span></span>   | <span data-ttu-id="77de4-665">Palgakonto</span><span class="sxs-lookup"><span data-stu-id="77de4-665">PayrollAccount</span></span>            |
| <span data-ttu-id="77de4-666">Hoiukonto</span><span class="sxs-lookup"><span data-stu-id="77de4-666">Savings Account</span></span>   | <span data-ttu-id="77de4-667">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="77de4-667">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="77de4-668">BankGiroti konto</span><span class="sxs-lookup"><span data-stu-id="77de4-668">BankGirot account</span></span> | <span data-ttu-id="77de4-669">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="77de4-669">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="77de4-670">PlusGiroti konto</span><span class="sxs-lookup"><span data-stu-id="77de4-670">PlusGirot account</span></span> | <span data-ttu-id="77de4-671">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="77de4-671">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="77de4-672">Tulukoodid</span><span class="sxs-lookup"><span data-stu-id="77de4-672">Earning codes</span></span>

<span data-ttu-id="77de4-673">Tulukoodid määratlevad kordumatult igat tüüpi tulud, mida töötajad saavad.</span><span class="sxs-lookup"><span data-stu-id="77de4-673">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="77de4-674">Koodid hõlmavad mitmeid tuludega seotud parameetreid, näiteks raamatupidamisreeglid, maksuseadused, aruandluse nõuded ja brutosumma võime.</span><span class="sxs-lookup"><span data-stu-id="77de4-674">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="77de4-675">Kui kasutatakse toetuseta sagedust, siis kasutatakse arvutamise jaoks vaikimisi sagedust **Iga makse**.</span><span class="sxs-lookup"><span data-stu-id="77de4-675">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="77de4-676">Toetatud sagedused</span><span class="sxs-lookup"><span data-stu-id="77de4-676">Supported frequencies</span></span>

- <span data-ttu-id="77de4-677">Kõik</span><span class="sxs-lookup"><span data-stu-id="77de4-677">All</span></span>
- <span data-ttu-id="77de4-678">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="77de4-678">EVERYPAY</span></span>
- <span data-ttu-id="77de4-679">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="77de4-679">EACHPAYPERIOD</span></span>
- <span data-ttu-id="77de4-680">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="77de4-680">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="77de4-681">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="77de4-681">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="77de4-682">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="77de4-682">1OFMTH</span></span>
- <span data-ttu-id="77de4-683">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="77de4-683">LASTOFMTH</span></span>
- <span data-ttu-id="77de4-684">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="77de4-684">2OFMTH</span></span>
- <span data-ttu-id="77de4-685">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="77de4-685">3OFMTH</span></span>
- <span data-ttu-id="77de4-686">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="77de4-686">4OFMTH</span></span>
- <span data-ttu-id="77de4-687">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="77de4-687">5OFMTH</span></span>
- <span data-ttu-id="77de4-688">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="77de4-688">1N2OFMTH</span></span>
- <span data-ttu-id="77de4-689">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="77de4-689">3N4OFMTH</span></span>
- <span data-ttu-id="77de4-690">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="77de4-690">1N3OFMTH</span></span>
- <span data-ttu-id="77de4-691">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="77de4-691">1N4OFMTH</span></span>
- <span data-ttu-id="77de4-692">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="77de4-692">2N3OFMTH</span></span>
- <span data-ttu-id="77de4-693">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="77de4-693">2N4OFMTH</span></span>
- <span data-ttu-id="77de4-694">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="77de4-694">1N2N3OFMTH</span></span>
- <span data-ttu-id="77de4-695">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="77de4-695">1N2N4OFMTH</span></span>
- <span data-ttu-id="77de4-696">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="77de4-696">1N3N4OFMTH</span></span>
- <span data-ttu-id="77de4-697">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="77de4-697">2N3N4OFMTH</span></span>
- <span data-ttu-id="77de4-698">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="77de4-698">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="77de4-699">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="77de4-699">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="77de4-700">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="77de4-700">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="77de4-701">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="77de4-701">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="77de4-702">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="77de4-702">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="77de4-703">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="77de4-703">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="77de4-704">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="77de4-704">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="77de4-705">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="77de4-705">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="77de4-706">Aadressid</span><span class="sxs-lookup"><span data-stu-id="77de4-706">Addresses</span></span>

<span data-ttu-id="77de4-707">Teatud riigi või regiooni, osariigi ja maakonna (haldusüksuse) koodide tuvastamise jaoks on vaja kindlaid vorminguid, mida Dayforce ning riigi-/regioonisisesed pakkujad ära tunnevad.</span><span class="sxs-lookup"><span data-stu-id="77de4-707">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="77de4-708">Kuigi linnade vorming on paindlik, peab iga linn olema seotud osariigiga.</span><span class="sxs-lookup"><span data-stu-id="77de4-708">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="77de4-709">Talent</span><span class="sxs-lookup"><span data-stu-id="77de4-709">Talent</span></span>              | <span data-ttu-id="77de4-710">Dayforce</span><span class="sxs-lookup"><span data-stu-id="77de4-710">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="77de4-711">Riik/regioon</span><span class="sxs-lookup"><span data-stu-id="77de4-711">Country/Region</span></span>      | <span data-ttu-id="77de4-712">Riigi kood</span><span class="sxs-lookup"><span data-stu-id="77de4-712">Country Code</span></span>          |
| <span data-ttu-id="77de4-713">Sihtnumber</span><span class="sxs-lookup"><span data-stu-id="77de4-713">Zip/Postal Code</span></span>     | <span data-ttu-id="77de4-714">Sihtnumber</span><span class="sxs-lookup"><span data-stu-id="77de4-714">Postal Code</span></span>           |
| <span data-ttu-id="77de4-715">Osariik</span><span class="sxs-lookup"><span data-stu-id="77de4-715">State</span></span>               | <span data-ttu-id="77de4-716">Osariigi kood</span><span class="sxs-lookup"><span data-stu-id="77de4-716">State Code</span></span>            |
| <span data-ttu-id="77de4-717">Linn</span><span class="sxs-lookup"><span data-stu-id="77de4-717">City</span></span>                | <span data-ttu-id="77de4-718">Linn</span><span class="sxs-lookup"><span data-stu-id="77de4-718">City</span></span>                  |
| <span data-ttu-id="77de4-719">Maakond</span><span class="sxs-lookup"><span data-stu-id="77de4-719">County</span></span>              | <span data-ttu-id="77de4-720">Maakond (haldusüksus)</span><span class="sxs-lookup"><span data-stu-id="77de4-720">County (Municipality)</span></span> |
| <span data-ttu-id="77de4-721">Tänav</span><span class="sxs-lookup"><span data-stu-id="77de4-721">Street</span></span>              | <span data-ttu-id="77de4-722">Aadressirida 1</span><span class="sxs-lookup"><span data-stu-id="77de4-722">Address Line 1</span></span>        |
| <span data-ttu-id="77de4-723">Majanumber</span><span class="sxs-lookup"><span data-stu-id="77de4-723">Street Number</span></span>       | <span data-ttu-id="77de4-724">Aadressirida 2</span><span class="sxs-lookup"><span data-stu-id="77de4-724">Address Line 2</span></span>        |
| <span data-ttu-id="77de4-725">Hoone tähis</span><span class="sxs-lookup"><span data-stu-id="77de4-725">Building Complement</span></span> | <span data-ttu-id="77de4-726">Aadressirida 5</span><span class="sxs-lookup"><span data-stu-id="77de4-726">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="77de4-727">Passi number</span><span class="sxs-lookup"><span data-stu-id="77de4-727">Passport number</span></span>

<span data-ttu-id="77de4-728">Töötajad saavad deklareerida passi teavet.</span><span class="sxs-lookup"><span data-stu-id="77de4-728">Employees can declare passport information.</span></span> <span data-ttu-id="77de4-729">See teave on identifitseerimistüüpi **Pass** ja integreeritakse Dayforce’i töövõtja Mehhiko-teabe osana.</span><span class="sxs-lookup"><span data-stu-id="77de4-729">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="77de4-730">Identifitseerimistüüp = pass</span><span class="sxs-lookup"><span data-stu-id="77de4-730">Identification Type = "Passport"</span></span>
- <span data-ttu-id="77de4-731">Väljastamise kuupäev</span><span class="sxs-lookup"><span data-stu-id="77de4-731">Issued Date</span></span>
- <span data-ttu-id="77de4-732">Aegumiskuupäev</span><span class="sxs-lookup"><span data-stu-id="77de4-732">Expiration Date</span></span>

<span data-ttu-id="77de4-733">Töövõtjad saavad deklareerida mitu **Pass**-identifitseerimistüüpi ID-numbrit.</span><span class="sxs-lookup"><span data-stu-id="77de4-733">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="77de4-734">Dayforce’i integreeritakse siiski ainult praegune aktiivne passikirje.</span><span class="sxs-lookup"><span data-stu-id="77de4-734">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="77de4-735">Kui kõik passikirjed on aegunud, siis integreeritakse Dayforce’i pass, mis väljastati viimasena.</span><span class="sxs-lookup"><span data-stu-id="77de4-735">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
