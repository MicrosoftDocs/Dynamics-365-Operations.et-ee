---
title: Rakenduste Talent ja Dayforce vahelise palgaarvestuse integratsiooni konfigureerimine
description: "Teemas selgitatakse, kuidas konfigureerida rakenduste Microsoft Dynamics 365 for Talent ja Ceridian Dayforce vahelist integratsiooni nii, et saaksite teha palgatöötlust."
author: jcart1106
manager: AnnBe
ms.date: 07/10/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 
ms.dyn365.ops.version: 
ms.translationtype: HT
ms.sourcegitcommit: 82f039b305503c604d64610f39838fa86a8eb08a
ms.openlocfilehash: fcddf82cffb9f0ba94b83eb21809b810585ebc9e
ms.contentlocale: et-ee
ms.lasthandoff: 08/08/2018

---

# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="16f6d-103">Rakenduste Talent ja Dayforce vahelise palgaarvestuse integratsiooni konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="16f6d-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="16f6d-104">Rakenduste Microsoft Dynamics 365 for Talent ja Ceridian Dayforce vaheline integratsioon sõltub mitmest konfiguratsioonietapist, mida kirjeldatakse selles teemas.</span><span class="sxs-lookup"><span data-stu-id="16f6d-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="16f6d-105">Enne palgatöötluse tegemist peate konfigureerima integratsiooni nii rakenduses Talent kui ka Dayforce.</span><span class="sxs-lookup"><span data-stu-id="16f6d-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="16f6d-106">Kui te kasutate palgatöötluste tegemiseks teenust nagu Dayforce, siis peate rakenduses Talent integratsiooni lubama.</span><span class="sxs-lookup"><span data-stu-id="16f6d-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="16f6d-107">Integratsiooni jaoks on rakendusest Talent vaja teatud andmeid.</span><span class="sxs-lookup"><span data-stu-id="16f6d-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="16f6d-108">Seega peate kinnitama, et Dayforce’iga vastendatud andmed on rakenduses Talent konfigureeritud viisil, mis lubab integratsiooni.</span><span class="sxs-lookup"><span data-stu-id="16f6d-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="16f6d-109">Integratsioon kasutab järgmisi üldisi andmekategooriaid.</span><span class="sxs-lookup"><span data-stu-id="16f6d-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="16f6d-110">Inimressursside andmed</span><span class="sxs-lookup"><span data-stu-id="16f6d-110">Human resources data</span></span>
- <span data-ttu-id="16f6d-111">Hüvituse andmed</span><span class="sxs-lookup"><span data-stu-id="16f6d-111">Compensation data</span></span>
- <span data-ttu-id="16f6d-112">Palgaandmed, näiteks palgatsüklid, makseperioodid ja tulukoodid</span><span class="sxs-lookup"><span data-stu-id="16f6d-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="16f6d-113">Töötaja andmed</span><span class="sxs-lookup"><span data-stu-id="16f6d-113">Worker data</span></span>

<span data-ttu-id="16f6d-114">Teemas kirjeldatakse etappe, mida peate integratsiooni lubamiseks läbima.</span><span class="sxs-lookup"><span data-stu-id="16f6d-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="16f6d-115">Samuti selgitatakse integratsiooni jaoks vajalikke andmetüüpe ja konfigureerimise üksikasju.</span><span class="sxs-lookup"><span data-stu-id="16f6d-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="16f6d-116">Integratsiooni lubamine</span><span class="sxs-lookup"><span data-stu-id="16f6d-116">Enable the integration</span></span>

<span data-ttu-id="16f6d-117">Dayforce’iga ühendamiseks peate rakenduses Talent sisse lülitama integratsiooni ja sisestama konfigureerimisteabe.</span><span class="sxs-lookup"><span data-stu-id="16f6d-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="16f6d-118">Kui soovite, et loodav pearaamatu kanne imporditaks rakendusse Microsoft Dynamics 365 for Finance and Operations, siis peate üles seadma rakenduse Microsoft Azure salvestuskonto ja sisestama Azure’i salvestusruumi ühendusstringi rakendusse Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="16f6d-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="16f6d-119">Rakenduses Talent integratsiooni sisselülitamiseks järgige järgmisi juhiseid.</span><span class="sxs-lookup"><span data-stu-id="16f6d-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="16f6d-120">Valige lehelt **Süsteemihaldus** suvand **Integratsiooni konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="16f6d-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="16f6d-121">Sisestage turvalise failiedastusprotokolli File Transfer Protocol (FTP) lõpp-punkt ja turvalise FTP kausta tee.</span><span class="sxs-lookup"><span data-stu-id="16f6d-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="16f6d-122">Sisestage selle kasutaja kasutajanimi ja parool, kellel on vaja juurdepääsu turvalise FTP lõpp-punktile ja kausta teele.</span><span class="sxs-lookup"><span data-stu-id="16f6d-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="16f6d-123">Testige ühendust vajaduse järgi ja määrake suvand **Palgaarvestuse integratsiooni lubamine** olekule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="16f6d-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="16f6d-124">Kui integratsioon on sisse lülitatud, luuakse andmete ekspordipakett ja -failid ning määratakse sagedus.</span><span class="sxs-lookup"><span data-stu-id="16f6d-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="16f6d-125">Vajaduse korral saate seda sagedust muuta.</span><span class="sxs-lookup"><span data-stu-id="16f6d-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="16f6d-126">Lisateavet Azure’i talletamiskontode ja Azure’i salvestusruumi ühendusstringide kohta leiate järgmistest Azure’i teemadest.</span><span class="sxs-lookup"><span data-stu-id="16f6d-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="16f6d-127">Azure’i salvestuskontod</span><span class="sxs-lookup"><span data-stu-id="16f6d-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="16f6d-128">Azure’i salvestusruumi ühendusstringide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="16f6d-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a><span data-ttu-id="16f6d-129">Andmete konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="16f6d-129">Configure your data</span></span> 

<span data-ttu-id="16f6d-130">Palgaarvestuse töötlemiseks peate konfigureerima rakenduses Talent personaliandmeid.</span><span class="sxs-lookup"><span data-stu-id="16f6d-130">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="16f6d-131">Peate määratlema organisatsiooni andmeid nagu tööd ja ametikohad, samuti teavet soodustuste ning kompensatsioonide kohta.</span><span class="sxs-lookup"><span data-stu-id="16f6d-131">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="16f6d-132">Selle teabe hulka kuulub töövõtja palgaandmete loomiseks vajalik teave töösuhte, palga ja mahaarvamiste kohta.</span><span class="sxs-lookup"><span data-stu-id="16f6d-132">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="16f6d-133">Personaliandmed</span><span class="sxs-lookup"><span data-stu-id="16f6d-133">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="16f6d-134">Soodustused</span><span class="sxs-lookup"><span data-stu-id="16f6d-134">Benefits</span></span> 

<span data-ttu-id="16f6d-135">Inimressursid pakuvad tööriistu, mis aitavad seadistada ja hallata soodustusi, mahaarvamisi ning töötajate hüvitusplaane, mida organisatsioon oma töötajatele pakub või nende puhul töötleb.</span><span class="sxs-lookup"><span data-stu-id="16f6d-135">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="16f6d-136">Soodustuste loomisel pidage meeles järgmisi Dayforce’is kasutatavaid andmeid ja konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="16f6d-136">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="16f6d-137">Soodustusplaanid</span><span class="sxs-lookup"><span data-stu-id="16f6d-137">Benefit plans</span></span>

- <span data-ttu-id="16f6d-138">Plaan (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-138">Plan (required)</span></span>
- <span data-ttu-id="16f6d-139">Tüüp (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-139">Type (required)</span></span>
- <span data-ttu-id="16f6d-140">Palga mõju (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-140">Payroll impact (required)</span></span>
- <span data-ttu-id="16f6d-141">Võlgnevuste sissenõudmine</span><span class="sxs-lookup"><span data-stu-id="16f6d-141">Recover arrears</span></span>
- <span data-ttu-id="16f6d-142">Mahaarvamismeetod</span><span class="sxs-lookup"><span data-stu-id="16f6d-142">Deduction method</span></span>
- <span data-ttu-id="16f6d-143">Mahaarvamise prioriteet</span><span class="sxs-lookup"><span data-stu-id="16f6d-143">Deduction priority</span></span>
- <span data-ttu-id="16f6d-144">Perioodi piiramine</span><span class="sxs-lookup"><span data-stu-id="16f6d-144">Limit period</span></span>
- <span data-ttu-id="16f6d-145">Piirsumma</span><span class="sxs-lookup"><span data-stu-id="16f6d-145">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="16f6d-146">Soodustused</span><span class="sxs-lookup"><span data-stu-id="16f6d-146">Benefits</span></span>

- <span data-ttu-id="16f6d-147">Plaan (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-147">Plan (required)</span></span>
- <span data-ttu-id="16f6d-148">Tüüp (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-148">Type (required)</span></span>
- <span data-ttu-id="16f6d-149">Suvand (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-149">Option (required)</span></span>
- <span data-ttu-id="16f6d-150">Soodustuse ID (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-150">Benefit ID (required)</span></span>
- <span data-ttu-id="16f6d-151">Sagedus</span><span class="sxs-lookup"><span data-stu-id="16f6d-151">Frequency</span></span>
- <span data-ttu-id="16f6d-152">Alus</span><span class="sxs-lookup"><span data-stu-id="16f6d-152">Basis</span></span>
- <span data-ttu-id="16f6d-153">Summa või määr</span><span class="sxs-lookup"><span data-stu-id="16f6d-153">Amount or rate</span></span>
- <span data-ttu-id="16f6d-154">Tulukood</span><span class="sxs-lookup"><span data-stu-id="16f6d-154">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="16f6d-155">Toetatud sagedused</span><span class="sxs-lookup"><span data-stu-id="16f6d-155">Supported frequencies</span></span> 

- <span data-ttu-id="16f6d-156">Iga nädal</span><span class="sxs-lookup"><span data-stu-id="16f6d-156">Weekly</span></span>
- <span data-ttu-id="16f6d-157">Kahe nädala tagant</span><span class="sxs-lookup"><span data-stu-id="16f6d-157">Bi-weekly</span></span>
- <span data-ttu-id="16f6d-158">Iga poole kuu tagant</span><span class="sxs-lookup"><span data-stu-id="16f6d-158">Semi-monthly</span></span>
- <span data-ttu-id="16f6d-159">Kord kuus</span><span class="sxs-lookup"><span data-stu-id="16f6d-159">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="16f6d-160">Toetatud alused</span><span class="sxs-lookup"><span data-stu-id="16f6d-160">Supported bases</span></span> 

- <span data-ttu-id="16f6d-161">Fikseeritud summa</span><span class="sxs-lookup"><span data-stu-id="16f6d-161">Fixed amount</span></span>
- <span data-ttu-id="16f6d-162">Tulu protsent</span><span class="sxs-lookup"><span data-stu-id="16f6d-162">Percent of earnings</span></span>
- <span data-ttu-id="16f6d-163">Produktiivsed tunnid</span><span class="sxs-lookup"><span data-stu-id="16f6d-163">Productive hours</span></span>

<span data-ttu-id="16f6d-164">Dayforce loob järgmised mahaarvamised palga mõju alusel, mis on määratletud soodustusplaanis.</span><span class="sxs-lookup"><span data-stu-id="16f6d-164">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="16f6d-165">Valik rakenduses Talent</span><span class="sxs-lookup"><span data-stu-id="16f6d-165">Selection in Talent</span></span>        | <span data-ttu-id="16f6d-166">Tulemus rakenduses Dayforce</span><span class="sxs-lookup"><span data-stu-id="16f6d-166">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="16f6d-167">Pole</span><span class="sxs-lookup"><span data-stu-id="16f6d-167">None</span></span>                       | <span data-ttu-id="16f6d-168">Mahaarvamist ei looda.</span><span class="sxs-lookup"><span data-stu-id="16f6d-168">No deduction is created.</span></span>                      |
| <span data-ttu-id="16f6d-169">Ainult mahaarvamine</span><span class="sxs-lookup"><span data-stu-id="16f6d-169">Deduction only</span></span>             | <span data-ttu-id="16f6d-170">Luuakse töövõtja mahaarvamine.</span><span class="sxs-lookup"><span data-stu-id="16f6d-170">An employee deduction is created.</span></span>             |
| <span data-ttu-id="16f6d-171">Ainult lisamine</span><span class="sxs-lookup"><span data-stu-id="16f6d-171">Contribution only</span></span>          | <span data-ttu-id="16f6d-172">Luuakse tööandja mahaarvamine.</span><span class="sxs-lookup"><span data-stu-id="16f6d-172">An employer deduction is created.</span></span>             |
| <span data-ttu-id="16f6d-173">Mahaarvamine ja lisamine</span><span class="sxs-lookup"><span data-stu-id="16f6d-173">Deduction and contribution</span></span> | <span data-ttu-id="16f6d-174">Luuakse töövõtja ja tööandja mahaarvamised.</span><span class="sxs-lookup"><span data-stu-id="16f6d-174">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="16f6d-175">Lisateavet soodustusprogrammi määratlemise ja haldamise kohta vaadake järgmistest teemadest.</span><span class="sxs-lookup"><span data-stu-id="16f6d-175">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="16f6d-176">Töötaja soodustuste programmi pakkumine</span><span class="sxs-lookup"><span data-stu-id="16f6d-176">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="16f6d-177">Uue soodustuse loomine</span><span class="sxs-lookup"><span data-stu-id="16f6d-177">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="16f6d-178">Soodustuskõlblikkuse reeglite ja poliitikate määratlemine</span><span class="sxs-lookup"><span data-stu-id="16f6d-178">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="16f6d-179">Töötajate soodustuste registreerimine ja eemaldamine</span><span class="sxs-lookup"><span data-stu-id="16f6d-179">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="16f6d-180">Hüvitus</span><span class="sxs-lookup"><span data-stu-id="16f6d-180">Compensation</span></span> 

<span data-ttu-id="16f6d-181">Hüvituste haldust kasutatakse põhitasu ja preemiate jagamise juhtimiseks.</span><span class="sxs-lookup"><span data-stu-id="16f6d-181">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="16f6d-182">Töötaja fikseeritud põhipalga ja preemia tõusu juhitakse põhipalga plaanide kaudu.</span><span class="sxs-lookup"><span data-stu-id="16f6d-182">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="16f6d-183">Lisatasude (nt preemiate, tulemustasude aktsiate eelismüügi ja toetuste ning ühekordsete preemiate) maksmist juhitakse ergutussüsteemi plaanide kaudu.</span><span class="sxs-lookup"><span data-stu-id="16f6d-183">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="16f6d-184">Dayforce kasutab hüvituse teavet töövõtja tunni- või aastamäära arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="16f6d-184">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="16f6d-185">Nõutavad on põhipalgaplaanid ja palgamäära teisendamised.</span><span class="sxs-lookup"><span data-stu-id="16f6d-185">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="16f6d-186">Töövõtjad peavad olema seotud põhipalgaplaaniga.</span><span class="sxs-lookup"><span data-stu-id="16f6d-186">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="16f6d-187">Lisateavet hüvitusplaanide kohta vaadake järgmistest teemadest.</span><span class="sxs-lookup"><span data-stu-id="16f6d-187">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="16f6d-188">Põhipalga plaanide loomine</span><span class="sxs-lookup"><span data-stu-id="16f6d-188">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="16f6d-189">Ergutussüsteemi plaanide loomine</span><span class="sxs-lookup"><span data-stu-id="16f6d-189">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="16f6d-190">Palga/hüvituse struktuuri ja plaanide arendamine</span><span class="sxs-lookup"><span data-stu-id="16f6d-190">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="16f6d-191">Hüvitusprotsess</span><span class="sxs-lookup"><span data-stu-id="16f6d-191">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="16f6d-192">Hüvitusprotsessi määratlemine ja tulemuste arvutamine</span><span class="sxs-lookup"><span data-stu-id="16f6d-192">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="16f6d-193">Töötaja liitmine põhipalga plaaniga</span><span class="sxs-lookup"><span data-stu-id="16f6d-193">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="16f6d-194">Töötaja liitmine tulemustasu plaaniga</span><span class="sxs-lookup"><span data-stu-id="16f6d-194">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="16f6d-195">Tööd</span><span class="sxs-lookup"><span data-stu-id="16f6d-195">Jobs</span></span> 

<span data-ttu-id="16f6d-196">Töö on tööd tegeva isiku jaoks nõutavate ülesannete ja vastutuste kogum.</span><span class="sxs-lookup"><span data-stu-id="16f6d-196">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="16f6d-197">Lisateavet vt järgmistest teemadest:</span><span class="sxs-lookup"><span data-stu-id="16f6d-197">For more information, see the following topics:</span></span>

- [<span data-ttu-id="16f6d-198">Töö komponentide seadistamine</span><span class="sxs-lookup"><span data-stu-id="16f6d-198">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="16f6d-199">Uute tööde määratlemine</span><span class="sxs-lookup"><span data-stu-id="16f6d-199">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="16f6d-200">Ametikohad</span><span class="sxs-lookup"><span data-stu-id="16f6d-200">Positions</span></span>

<span data-ttu-id="16f6d-201">Ametikoht on töökoha üksik eksemplar.</span><span class="sxs-lookup"><span data-stu-id="16f6d-201">A position is an individual instance of a job.</span></span> <span data-ttu-id="16f6d-202">Näiteks on ametikoht „müügijuht (Ida)” vaid üks tööga „müügijuht” seostatud ametikohti.</span><span class="sxs-lookup"><span data-stu-id="16f6d-202">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="16f6d-203">Ametikoht kuulub osakonna alla.</span><span class="sxs-lookup"><span data-stu-id="16f6d-203">A position exists in a department.</span></span> <span data-ttu-id="16f6d-204">Iga ametikohaga saab seostada vaid ühte töötajat.</span><span class="sxs-lookup"><span data-stu-id="16f6d-204">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="16f6d-205">Ametikohtade seadistamisel pidage meeles järgmisi andmeid ja konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="16f6d-205">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="16f6d-206">Ametikoht (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-206">Position (required)</span></span>
- <span data-ttu-id="16f6d-207">Kirjeldus (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-207">Description (required)</span></span>
- <span data-ttu-id="16f6d-208">Töö (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-208">Job (required)</span></span>
- <span data-ttu-id="16f6d-209">Osakond (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-209">Department (required)</span></span>
- <span data-ttu-id="16f6d-210">Ametikoha tüüp (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-210">Position type (required)</span></span>
- <span data-ttu-id="16f6d-211">Täistööaja vaste</span><span class="sxs-lookup"><span data-stu-id="16f6d-211">Full-time equivalent</span></span>
- <span data-ttu-id="16f6d-212">Iga-aastased regulaarsed tunnid (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-212">Annual regular hours (required)</span></span>
- <span data-ttu-id="16f6d-213">Maksja juriidiline isik (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-213">Paid by legal entity (required)</span></span>
- <span data-ttu-id="16f6d-214">Palgatsükkel (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-214">Pay cycle (required)</span></span>
- <span data-ttu-id="16f6d-215">Vaike-finantsdimensioonid – kulukeskus (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-215">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="16f6d-216">Töötaja määramine – töötaja, määramise algus, määramise lõpp, põhjuse kood</span><span class="sxs-lookup"><span data-stu-id="16f6d-216">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="16f6d-217">Kui ühes osakonnas on sama tööga seotud mitu ametikohta, siis konsolideeritakse need rakenduses Dayforce üheks ametikohaks.</span><span class="sxs-lookup"><span data-stu-id="16f6d-217">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="16f6d-218">Lisateavet vt järgmistest teemadest:</span><span class="sxs-lookup"><span data-stu-id="16f6d-218">For more information, see the following topics:</span></span>

- [<span data-ttu-id="16f6d-219">Tööjõu korraldamine osakondade, tööde ja ametikohtade abil</span><span class="sxs-lookup"><span data-stu-id="16f6d-219">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="16f6d-220">Ametikohtade seadistamine</span><span class="sxs-lookup"><span data-stu-id="16f6d-220">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="16f6d-221">Osakonnad</span><span class="sxs-lookup"><span data-stu-id="16f6d-221">Departments</span></span>

<span data-ttu-id="16f6d-222">Osakond on tootmisüksus, mis esindab organisatsiooni kategooriat või funktsionaalset ala.</span><span class="sxs-lookup"><span data-stu-id="16f6d-222">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="16f6d-223">Osakond vastutab organisatsiooni kindla valdkonna eest, nagu müük, raamatupidamine või inimressursid.</span><span class="sxs-lookup"><span data-stu-id="16f6d-223">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="16f6d-224">Saate osakondi kasutada funktsionaalsete alade aruannete koostamiseks.</span><span class="sxs-lookup"><span data-stu-id="16f6d-224">You can use departments to report on functional areas.</span></span> <span data-ttu-id="16f6d-225">Osakonnad võivad vastutada kasumi ja kahjumi eest.</span><span class="sxs-lookup"><span data-stu-id="16f6d-225">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="16f6d-226">Lisateavet vt järgmistest teemadest:</span><span class="sxs-lookup"><span data-stu-id="16f6d-226">For more information, see the following topics:</span></span>

- [<span data-ttu-id="16f6d-227">Osakonna loomine ja selle seostamine osakonnahierarhiaga</span><span class="sxs-lookup"><span data-stu-id="16f6d-227">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="16f6d-228">Uute osakondade määratlemine</span><span class="sxs-lookup"><span data-stu-id="16f6d-228">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="16f6d-229">Palgatsüklid ja makseperioodid</span><span class="sxs-lookup"><span data-stu-id="16f6d-229">Pay cycles and pay periods</span></span>

<span data-ttu-id="16f6d-230">Palgatsükkel määrab, kui tihti palgamaksmine toimub ja konkreetsed päevad, millal töötajatele palka makstakse.</span><span class="sxs-lookup"><span data-stu-id="16f6d-230">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="16f6d-231">Näiteks võib palgatsükli sageduseks olla üks kuu ja töövõtjatele makstakse seega kuu viimasel päeval.</span><span class="sxs-lookup"><span data-stu-id="16f6d-231">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="16f6d-232">Või kui palgatsükli sageduseks on üks nädal, siis makstakse töövõtjatele näiteks teisipäeviti pärast makseperioodi lõppu.</span><span class="sxs-lookup"><span data-stu-id="16f6d-232">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="16f6d-233">Palgatsükleid määratakse ametikohtadele selleks, et määrata, millal nendel ametikohtadel töötavatele töötajatele palka makstakse.</span><span class="sxs-lookup"><span data-stu-id="16f6d-233">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="16f6d-234">Pärast palgatsüklite loomist saate iga tsükli jaoks luua makseperioodid.</span><span class="sxs-lookup"><span data-stu-id="16f6d-234">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="16f6d-235">Igal makseperioodil on makse vaikekuupäev, mis põhineb teie sisestatud teabel.</span><span class="sxs-lookup"><span data-stu-id="16f6d-235">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="16f6d-236">Siiski saate erandite käsitlemiseks makseperioodi makse vaikekuupäeva muuta, näiteks kui maksekuupäev satub riigipühale.</span><span class="sxs-lookup"><span data-stu-id="16f6d-236">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="16f6d-237">Dayforce kasutab järgmist teavet.</span><span class="sxs-lookup"><span data-stu-id="16f6d-237">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="16f6d-238">Palgatsükkel (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-238">Pay cycle (required)</span></span>
- <span data-ttu-id="16f6d-239">Palgatsükli sagedus (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-239">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="16f6d-240">Perioodi alguskuupäev (esimene makseperiood on kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-240">Period start date (first pay period required)</span></span>
- <span data-ttu-id="16f6d-241">Makse vaikekuupäev (esimene makseperiood on kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-241">Default payment date (first pay period required)</span></span>

<span data-ttu-id="16f6d-242">See teave on integreeritud rakendusse Dayforce palgagruppidena ja on iga palgatsükli puhul eraldatud riigi või regiooniga.</span><span class="sxs-lookup"><span data-stu-id="16f6d-242">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="16f6d-243">Enne integreerimist peab olema loodud vähemalt üks makseperiood.</span><span class="sxs-lookup"><span data-stu-id="16f6d-243">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="16f6d-244">Dayforce loob palgagrupi kalendrid ja maksekuupäevad rakenduses Talent määratletud esimese makseperioodi alguskuupäeva ja makse vaikekuupäeva põhjal.</span><span class="sxs-lookup"><span data-stu-id="16f6d-244">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="16f6d-245">Tulukoodid</span><span class="sxs-lookup"><span data-stu-id="16f6d-245">Earning codes</span></span>

<span data-ttu-id="16f6d-246">Tulukoodid määratlevad kordumatult igat tüüpi tulud, mida töötajad saavad.</span><span class="sxs-lookup"><span data-stu-id="16f6d-246">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="16f6d-247">Koodidel on mitmeid tuludega seotud parameetreid, näiteks raamatupidamisreeglid, maksuseadused, aruandluse nõuded ja brutosumma võime.</span><span class="sxs-lookup"><span data-stu-id="16f6d-247">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="16f6d-248">Dayforce kasutab järgmist teavet.</span><span class="sxs-lookup"><span data-stu-id="16f6d-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="16f6d-249">Tulukood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-249">Earning Code (required)</span></span>
- <span data-ttu-id="16f6d-250">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="16f6d-250">Description</span></span>
- <span data-ttu-id="16f6d-251">Mõõtühik</span><span class="sxs-lookup"><span data-stu-id="16f6d-251">Unit of measure</span></span>
- <span data-ttu-id="16f6d-252">Produktiivne</span><span class="sxs-lookup"><span data-stu-id="16f6d-252">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="16f6d-253">Töötaja andmed</span><span class="sxs-lookup"><span data-stu-id="16f6d-253">Worker data</span></span>

<span data-ttu-id="16f6d-254">Töötajate kirjed on tähtsad teie personali- ja palgasüsteemide jaoks.</span><span class="sxs-lookup"><span data-stu-id="16f6d-254">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="16f6d-255">Teie sisestatud teavet saab kasutada töötajate ja nende isikliku teabe jälgimiseks.</span><span class="sxs-lookup"><span data-stu-id="16f6d-255">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="16f6d-256">Töötajate kohta saate hallata järgmist teavet.</span><span class="sxs-lookup"><span data-stu-id="16f6d-256">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="16f6d-257">**Üldine** – töötaja põhiteave, näiteks kontaktteave, demograafiline teave, tuvastamisteave, perekonna teave, sõjaväeteenistuse olek, välislähetuse teave ja isiklikud ning lähedase isiku kontaktandmed.</span><span class="sxs-lookup"><span data-stu-id="16f6d-257">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="16f6d-258">**Töösuhe** – töötaja töösuhte teave, näiteks töötaja palganud ettevõte või organisatsioon, määratud ametikoht, algus- ja lõppkuupäevad, töökõlblikkus, töölevõtutingimused, pension, puhkus ja ümberpaigutuse teave.</span><span class="sxs-lookup"><span data-stu-id="16f6d-258">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="16f6d-259">**Puhkused ja puudumised** – teave töötaja puudumiste kohta, näiteks töögraafikud, puudumiskanded ja puudumise seadistamine.</span><span class="sxs-lookup"><span data-stu-id="16f6d-259">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="16f6d-260">**Hüvitus ja palk** – teave töötaja hüvitusplaanide ja palgaarvestuse kohta, näiteks liitutud plaanid, preemiad, tööviljakus, komisjonitasu, maksuteave, pensionileminek ning palgast mahaarvamised.</span><span class="sxs-lookup"><span data-stu-id="16f6d-260">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="16f6d-261">Töötaja teabe sisestamisel pidage meeles järgmisi Dayforce’is kasutatavaid andmeid ja konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="16f6d-261">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="16f6d-262">Üldteave</span><span class="sxs-lookup"><span data-stu-id="16f6d-262">General information</span></span>

- <span data-ttu-id="16f6d-263">Töötaja number (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-263">Personnel number (required)</span></span>
- <span data-ttu-id="16f6d-264">Eesnimi (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-264">First name (required)</span></span>
- <span data-ttu-id="16f6d-265">Perekonnanimi (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-265">Last name (required)</span></span>
- <span data-ttu-id="16f6d-266">Teine eesnimi</span><span class="sxs-lookup"><span data-stu-id="16f6d-266">Middle name</span></span>
- <span data-ttu-id="16f6d-267">Staaž kuupäeval</span><span class="sxs-lookup"><span data-stu-id="16f6d-267">Seniority date</span></span>
- <span data-ttu-id="16f6d-268">Tuntud kui</span><span class="sxs-lookup"><span data-stu-id="16f6d-268">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="16f6d-269">Isikuandmed</span><span class="sxs-lookup"><span data-stu-id="16f6d-269">Personal information</span></span>

- <span data-ttu-id="16f6d-270">Perekonnaseis (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-270">Marital status (required)</span></span>
- <span data-ttu-id="16f6d-271">Sünnikuupäev (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-271">Birth date (required)</span></span>
- <span data-ttu-id="16f6d-272">Sugu (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-272">Gender (required)</span></span>
- <span data-ttu-id="16f6d-273">Puudega isik</span><span class="sxs-lookup"><span data-stu-id="16f6d-273">Person with disabilities</span></span>
- <span data-ttu-id="16f6d-274">Kodakondsusjärgse riigi regioon (ainult Mehhiko puhul)</span><span class="sxs-lookup"><span data-stu-id="16f6d-274">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="16f6d-275">Aadressiteave</span><span class="sxs-lookup"><span data-stu-id="16f6d-275">Address information</span></span>

- <span data-ttu-id="16f6d-276">Tänava nimi ja hoone number (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-276">Primary (required)</span></span>
- <span data-ttu-id="16f6d-277">Riik/regioon (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-277">Country/region (required)</span></span>
- <span data-ttu-id="16f6d-278">Sihtnumber (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-278">Postal code (required)</span></span>
- <span data-ttu-id="16f6d-279">Tänava number (kohustuslik) (ainult Mehhiko puhul)</span><span class="sxs-lookup"><span data-stu-id="16f6d-279">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="16f6d-280">Hoone tähis (ainult Mehhiko puhul)</span><span class="sxs-lookup"><span data-stu-id="16f6d-280">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="16f6d-281">Linn (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-281">City (required)</span></span>
- <span data-ttu-id="16f6d-282">Osariik (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-282">State (required)</span></span>
- <span data-ttu-id="16f6d-283">Maakond (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-283">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="16f6d-284">Kontaktteave</span><span class="sxs-lookup"><span data-stu-id="16f6d-284">Contact information</span></span> 

- <span data-ttu-id="16f6d-285">Tänava nimi ja hoone number (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-285">Primary (required)</span></span>
- <span data-ttu-id="16f6d-286">Kontaktnumber (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-286">Contact number (required)</span></span>
- <span data-ttu-id="16f6d-287">Sisetelefon</span><span class="sxs-lookup"><span data-stu-id="16f6d-287">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="16f6d-288">Palgateave ja tulukoodid</span><span class="sxs-lookup"><span data-stu-id="16f6d-288">Payroll information and earning codes</span></span>

<span data-ttu-id="16f6d-289">Töövõtjatele võidakse määrata teatud maksesagedusega konkreetsed tulud ja neil võivad olla eelistatud makseviisid.</span><span class="sxs-lookup"><span data-stu-id="16f6d-289">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="16f6d-290">Nende eelistuste ja sätete kasutamise tagamiseks kasutatakse Dayforce’is järgmisi välju.</span><span class="sxs-lookup"><span data-stu-id="16f6d-290">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="16f6d-291">Tulukoodid</span><span class="sxs-lookup"><span data-stu-id="16f6d-291">Earning codes</span></span>

- <span data-ttu-id="16f6d-292">Ametikoht (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-292">Position (required)</span></span>
- <span data-ttu-id="16f6d-293">Tulukood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-293">Earning Code (required)</span></span>
- <span data-ttu-id="16f6d-294">Maksesagedus (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-294">Frequency (required)</span></span>
- <span data-ttu-id="16f6d-295">Summa (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-295">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="16f6d-296">Palgateave</span><span class="sxs-lookup"><span data-stu-id="16f6d-296">Payroll information</span></span>

- <span data-ttu-id="16f6d-297">Makseviis</span><span class="sxs-lookup"><span data-stu-id="16f6d-297">Payment Method</span></span>
- <span data-ttu-id="16f6d-298">Majanduspiirkond (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-298">Economic Region (required)</span></span>
- <span data-ttu-id="16f6d-299">Töövõtja soodustuste ID</span><span class="sxs-lookup"><span data-stu-id="16f6d-299">Employee Benefits ID</span></span>
- <span data-ttu-id="16f6d-300">Riiklik isikukood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-300">National ID Number (required)</span></span>
- <span data-ttu-id="16f6d-301">Sõjaväeteenistuse number</span><span class="sxs-lookup"><span data-stu-id="16f6d-301">Military Service Number</span></span>
- <span data-ttu-id="16f6d-302">Vahetuse ID (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-302">Shift ID (required)</span></span>
- <span data-ttu-id="16f6d-303">Maksukood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-303">Tax Number (required)</span></span>
- <span data-ttu-id="16f6d-304">Ühingu ID (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-304">Union ID (required)</span></span>
- <span data-ttu-id="16f6d-305">Tööpäeva ID (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-305">Work Day ID (required)</span></span>
- <span data-ttu-id="16f6d-306">Tööloa number</span><span class="sxs-lookup"><span data-stu-id="16f6d-306">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="16f6d-307">Mehhiko toetab järgmisi makseviise: **sularaha**, **tšekk** (ettevõtte füüsiline tšekk) ja **elektrooniline makse**.</span><span class="sxs-lookup"><span data-stu-id="16f6d-307">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="16f6d-308">Kui makseviisi pole määratud, kasutatakse vaikevalikut **tšekk**.</span><span class="sxs-lookup"><span data-stu-id="16f6d-308">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="16f6d-309">Töösuhte üksikasjad</span><span class="sxs-lookup"><span data-stu-id="16f6d-309">Employment details</span></span>

<span data-ttu-id="16f6d-310">Töösuhte üksikasjade ajalugu on põhiline teave, millest tuletatakse rakenduses Dayforce töövõtja palkamise, töösuhte lõpetamise ja uuesti palkamise olekud.</span><span class="sxs-lookup"><span data-stu-id="16f6d-310">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="16f6d-311">Dayforce toetab korraga ainult ühte aktiivset töösuhte kirjet.</span><span class="sxs-lookup"><span data-stu-id="16f6d-311">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="16f6d-312">Töösuhte alguskuupäev (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-312">Employment start date (required)</span></span>
- <span data-ttu-id="16f6d-313">Töösuhte lõppkuupäev</span><span class="sxs-lookup"><span data-stu-id="16f6d-313">Employment end date</span></span>
- <span data-ttu-id="16f6d-314">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="16f6d-314">Start date</span></span>
- <span data-ttu-id="16f6d-315">Korrigeeritud alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="16f6d-315">Adjusted start date</span></span>
- <span data-ttu-id="16f6d-316">Töösuhte lõpetamise kuupäev (kohustuslik lõpetamisel)</span><span class="sxs-lookup"><span data-stu-id="16f6d-316">Termination date (required upon termination)</span></span>
- <span data-ttu-id="16f6d-317">Töösuhte lõpetamise põhjus (kohustuslik lõpetamisel)</span><span class="sxs-lookup"><span data-stu-id="16f6d-317">Termination reason (required upon termination)</span></span>

<span data-ttu-id="16f6d-318">Töövõtja tähtsaimad kuupäevad tuletatakse järgmisest teabest.</span><span class="sxs-lookup"><span data-stu-id="16f6d-318">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="16f6d-319">Talent</span><span class="sxs-lookup"><span data-stu-id="16f6d-319">Talent</span></span>                | <span data-ttu-id="16f6d-320">Dayforce</span><span class="sxs-lookup"><span data-stu-id="16f6d-320">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16f6d-321">Kõige värskem palkamise kuupäev</span><span class="sxs-lookup"><span data-stu-id="16f6d-321">Most recent hire date</span></span> | <span data-ttu-id="16f6d-322">Praeguse lõpetamata töösuhte ajalookirje alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="16f6d-322">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="16f6d-323">Lõpetamiskuupäev</span><span class="sxs-lookup"><span data-stu-id="16f6d-323">Termination date</span></span>      | <span data-ttu-id="16f6d-324">Praeguse lõpetamata töösuhte ajalookirje lõpetamise kuupäev</span><span class="sxs-lookup"><span data-stu-id="16f6d-324">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="16f6d-325">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="16f6d-325">Start date</span></span>            | <span data-ttu-id="16f6d-326">Korrigeeritud alguskuupäev, alguskuupäev või praeguse passiivse töösuhte ajalookirje alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="16f6d-326">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="16f6d-327">Palkamise algne kuupäev</span><span class="sxs-lookup"><span data-stu-id="16f6d-327">Original hire date</span></span>    | <span data-ttu-id="16f6d-328">Varaseima töösuhte ajalookirje alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="16f6d-328">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="16f6d-329">Hüvitus</span><span class="sxs-lookup"><span data-stu-id="16f6d-329">Compensation</span></span>

<span data-ttu-id="16f6d-330">Tööhõiveperioodi jooksul peab iga töövõtja peamise ametikohaga olema seotud põhipalgaplaan.</span><span class="sxs-lookup"><span data-stu-id="16f6d-330">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="16f6d-331">See periood algab kuupäeval, mil töövõtja palgati (või töösuhte alguskuupäeval), ja jätkub kuni töösuhte lõpetamiseni.</span><span class="sxs-lookup"><span data-stu-id="16f6d-331">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="16f6d-332">Kehtivuse algus (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-332">Effective Date (required)</span></span>
- <span data-ttu-id="16f6d-333">Aegumiskuupäev</span><span class="sxs-lookup"><span data-stu-id="16f6d-333">Expiration date</span></span>
- <span data-ttu-id="16f6d-334">Palgamäär (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-334">Pay Rate (required)</span></span>
- <span data-ttu-id="16f6d-335">Palgamäära teisendamised (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-335">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="16f6d-336">Aastane vaste (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-336">Annual equivalent (required)</span></span>
- <span data-ttu-id="16f6d-337">Tunnine vaste (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-337">Hourly equivalent (required)</span></span>

<span data-ttu-id="16f6d-338">Kui tunnimääraga töövõtjal on mitu ametikohta, siis imporditakse peamise ametikoha põhipalk rakendusse Dayforce töövõtja taseme põhimäärana/-palgana.</span><span class="sxs-lookup"><span data-stu-id="16f6d-338">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="16f6d-339">Teiseste ametikohtade puhul salvestatakse Dayforce’is tunnimäär vastava ametikoha jaoks.</span><span class="sxs-lookup"><span data-stu-id="16f6d-339">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="16f6d-340">Kui kuupalgaga töötajal on mitu ametikohta, siis kasutatakse töövõtja taseme põhimäärana/-palgana kõikide aktiivsete ametikohtade tuletatud kumulatiivset tunnimäära ja aastapalka.</span><span class="sxs-lookup"><span data-stu-id="16f6d-340">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="16f6d-341">ID-numbrid</span><span class="sxs-lookup"><span data-stu-id="16f6d-341">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="16f6d-342">Isiku identifikaator</span><span class="sxs-lookup"><span data-stu-id="16f6d-342">Social Security identifier</span></span> 

<span data-ttu-id="16f6d-343">Igal töövõtjal peab olema üks peamine identifikaator.</span><span class="sxs-lookup"><span data-stu-id="16f6d-343">Every employee must have one primary identifier.</span></span> <span data-ttu-id="16f6d-344">Identifikaator peab olema isikukoodi- ehk **SSN**-tüüpi.</span><span class="sxs-lookup"><span data-stu-id="16f6d-344">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="16f6d-345">Rakenduses Dayforce tuletatakse see automaatselt töövõtja isiku identifikaatorina, mis on palkamiseks vajalik.</span><span class="sxs-lookup"><span data-stu-id="16f6d-345">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="16f6d-346">Peamine isikukood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-346">Primary (required)</span></span>
- <span data-ttu-id="16f6d-347">ID tüüp = SSN</span><span class="sxs-lookup"><span data-stu-id="16f6d-347">Identification Type = "SSN"</span></span>
- <span data-ttu-id="16f6d-348">Väljastamise kuupäev</span><span class="sxs-lookup"><span data-stu-id="16f6d-348">Issued Date</span></span>
- <span data-ttu-id="16f6d-349">Aegumiskuupäev</span><span class="sxs-lookup"><span data-stu-id="16f6d-349">Expiration Date</span></span>

<span data-ttu-id="16f6d-350">Töövõtjad saavad deklareerida mitu **SSN**-identifitseerimistüüpi ID-numbrit.</span><span class="sxs-lookup"><span data-stu-id="16f6d-350">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="16f6d-351">Dayforce’i integreeritakse vaid tähistusega **Peamine** kirje, olenemata sellest, kas number on aktiivne või aegunud.</span><span class="sxs-lookup"><span data-stu-id="16f6d-351">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="16f6d-352">Pangakontod ja väljamaksed</span><span class="sxs-lookup"><span data-stu-id="16f6d-352">Bank accounts and disbursements</span></span>

<span data-ttu-id="16f6d-353">Iga töötaja jaoks, kes soovib oma palka pangakonto ülekandena kätte saada, tuleb sisestada kehtiv pangakonto teave.</span><span class="sxs-lookup"><span data-stu-id="16f6d-353">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="16f6d-354">Talent</span><span class="sxs-lookup"><span data-stu-id="16f6d-354">Talent</span></span>                         | <span data-ttu-id="16f6d-355">Dayforce</span><span class="sxs-lookup"><span data-stu-id="16f6d-355">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16f6d-356">Pangakonto number (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-356">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="16f6d-357">SWIFT-kood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-357">SWIFT code (required)</span></span>          | <span data-ttu-id="16f6d-358">Välja **Panga ID** kasutatakse palgaarvestuse töötlemiseks Mehhikos.</span><span class="sxs-lookup"><span data-stu-id="16f6d-358">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="16f6d-359">Filiaali kood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-359">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="16f6d-360">Pangakonto tüüp (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-360">Bank account type (required)</span></span>   | <span data-ttu-id="16f6d-361">Välja **Konto tüüp** kasutatakse palgaarvestuse töötlemiseks Mehhikos.</span><span class="sxs-lookup"><span data-stu-id="16f6d-361">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="16f6d-362">Toetatud väärtused on **Jooksevkonto** ja **Palgakonto**</span><span class="sxs-lookup"><span data-stu-id="16f6d-362">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="16f6d-363">Töövõtjad, kes soovivad oma palka pangakonto ülekannetena kätte saada, peavad esitama lingi jäägikontole, mis on juriidilise isiku alluvuses, kelle peamine aadress on Mehhikos ja kes on seotud Mehhiko panga kehtiva pangakontoga.</span><span class="sxs-lookup"><span data-stu-id="16f6d-363">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="16f6d-364">Kõiki ülejäänuid kontosid, mis pole jäägikontod, eiratakse.</span><span class="sxs-lookup"><span data-stu-id="16f6d-364">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="16f6d-365">Aadressiteave</span><span class="sxs-lookup"><span data-stu-id="16f6d-365">Address information</span></span>

<span data-ttu-id="16f6d-366">Igal töövõtjal peab olema üks peamine asukoht.</span><span class="sxs-lookup"><span data-stu-id="16f6d-366">Every employee must have one primary location.</span></span> <span data-ttu-id="16f6d-367">Dayforce’is kasutatakse seda asukohta, et määratleda töövõtja peamine elukoht maksustamise tarbeks.</span><span class="sxs-lookup"><span data-stu-id="16f6d-367">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="16f6d-368">Peamine elukoht (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-368">Primary (required)</span></span>
- <span data-ttu-id="16f6d-369">Riik/regioon (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-369">Country/region (required)</span></span>
- <span data-ttu-id="16f6d-370">Sihtnumber (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-370">Zip/postal code (required)</span></span>
- <span data-ttu-id="16f6d-371">Tänava nimi (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-371">Street (required)</span></span>
- <span data-ttu-id="16f6d-372">Tänava number (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-372">Street Number (required)</span></span>
- <span data-ttu-id="16f6d-373">Hoone tähis</span><span class="sxs-lookup"><span data-stu-id="16f6d-373">Building Complement</span></span>
- <span data-ttu-id="16f6d-374">Linn (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-374">City (required)</span></span>
- <span data-ttu-id="16f6d-375">Osariik (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-375">State (required)</span></span>
- <span data-ttu-id="16f6d-376">Maakond (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-376">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="16f6d-377">Andmete konfigureerimine palgaandmete loomiseks Ameerika Ühendriikides ja Kanadas</span><span class="sxs-lookup"><span data-stu-id="16f6d-377">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="16f6d-378">Kui loote palgaandmeid Ameerika Ühendriikide või Kanada töövõtjatele, siis peate konfigureerima järgmisi elemente.</span><span class="sxs-lookup"><span data-stu-id="16f6d-378">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="16f6d-379">Ametikohtadele tuleb määrata osakonnad.</span><span class="sxs-lookup"><span data-stu-id="16f6d-379">Departments are required on positions.</span></span>
- <span data-ttu-id="16f6d-380">Kulukeskused tuleb määratleda finantsdimensioonideks ja peavad olema vaike-finantsdimensiooni stringi esimene element.</span><span class="sxs-lookup"><span data-stu-id="16f6d-380">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="16f6d-381">Töötüübid</span><span class="sxs-lookup"><span data-stu-id="16f6d-381">Job types</span></span>

<span data-ttu-id="16f6d-382">Töötüüpe kasutatakse sarnaste tööde kategooriatesse grupeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="16f6d-382">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="16f6d-383">Töötüübid on vajalikud palgaarvestuse töötlemiseks Ameerika Ühendriikides ja Kanadas.</span><span class="sxs-lookup"><span data-stu-id="16f6d-383">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="16f6d-384">Töötüübid on näiteks täistööaeg ja osaline tööaeg või kuupalk ning tunnipalk.</span><span class="sxs-lookup"><span data-stu-id="16f6d-384">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="16f6d-385">Töötüübid vastendatakse Dayforce’i tasutüüpidena, mis näitavad, kas töövõtja on tunni- või palgatöötaja.</span><span class="sxs-lookup"><span data-stu-id="16f6d-385">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="16f6d-386">Järgmised töötüübid ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="16f6d-386">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="16f6d-387">Töö tüüp</span><span class="sxs-lookup"><span data-stu-id="16f6d-387">Job type</span></span>   | <span data-ttu-id="16f6d-388">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="16f6d-388">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="16f6d-389">Tunnimäär</span><span class="sxs-lookup"><span data-stu-id="16f6d-389">Hourly</span></span>     | <span data-ttu-id="16f6d-390">Tunnimäär</span><span class="sxs-lookup"><span data-stu-id="16f6d-390">Hourly</span></span>      |
| <span data-ttu-id="16f6d-391">Põhipalk</span><span class="sxs-lookup"><span data-stu-id="16f6d-391">Salaried</span></span>   | <span data-ttu-id="16f6d-392">Põhipalk</span><span class="sxs-lookup"><span data-stu-id="16f6d-392">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="16f6d-393">Ametikoha tüübid</span><span class="sxs-lookup"><span data-stu-id="16f6d-393">Position types</span></span> 

<span data-ttu-id="16f6d-394">Ametikoha tüüpe kasutatakse selleks, et kirjeldada, kas ametikoht on täiskohaga, osalise tööajaga või midagi muud.</span><span class="sxs-lookup"><span data-stu-id="16f6d-394">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="16f6d-395">Ametikoha tüübid vastendatakse Dayforce’i tasuklassidena, mis näitavad, kas töövõtja on täis- või osalise tööajaga töötaja.</span><span class="sxs-lookup"><span data-stu-id="16f6d-395">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="16f6d-396">Järgmised ametikoha tüübid ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="16f6d-396">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="16f6d-397">Ametikoha tüüp</span><span class="sxs-lookup"><span data-stu-id="16f6d-397">Position type</span></span>   | <span data-ttu-id="16f6d-398">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="16f6d-398">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="16f6d-399">Täistööaeg</span><span class="sxs-lookup"><span data-stu-id="16f6d-399">Full-time</span></span>       | <span data-ttu-id="16f6d-400">Täistööajaga töövõtja</span><span class="sxs-lookup"><span data-stu-id="16f6d-400">Full time employee</span></span> |
| <span data-ttu-id="16f6d-401">Osaline tööaeg</span><span class="sxs-lookup"><span data-stu-id="16f6d-401">Part-time</span></span>       | <span data-ttu-id="16f6d-402">Osalise tööajaga töövõtja</span><span class="sxs-lookup"><span data-stu-id="16f6d-402">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="16f6d-403">Põhjusekoodid</span><span class="sxs-lookup"><span data-stu-id="16f6d-403">Reason codes</span></span>

<span data-ttu-id="16f6d-404">Põhjusekoodid annavad teavet töövõtja oleku kohta.</span><span class="sxs-lookup"><span data-stu-id="16f6d-404">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="16f6d-405">Põhjusekoodid vastendatakse Dayforce’i olekupõhjustena, mis näitavad töövõtja ametikoha või töösuhte oleku muutuse põhjust.</span><span class="sxs-lookup"><span data-stu-id="16f6d-405">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="16f6d-406">Järgmised põhjusekoodid ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="16f6d-406">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="16f6d-407">Põhjusekood</span><span class="sxs-lookup"><span data-stu-id="16f6d-407">Reason code</span></span>    | <span data-ttu-id="16f6d-408">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="16f6d-408">Description</span></span>      | <span data-ttu-id="16f6d-409">Rakendatavad stsenaariumid</span><span class="sxs-lookup"><span data-stu-id="16f6d-409">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="16f6d-410">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="16f6d-410">RESIGNATION</span></span>    | <span data-ttu-id="16f6d-411">Lahkumine</span><span class="sxs-lookup"><span data-stu-id="16f6d-411">Resignation</span></span>      | <span data-ttu-id="16f6d-412">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="16f6d-412">Terminate worker</span></span>     |
| <span data-ttu-id="16f6d-413">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="16f6d-413">TERMINATION</span></span>    | <span data-ttu-id="16f6d-414">Lõpetamine</span><span class="sxs-lookup"><span data-stu-id="16f6d-414">Termination</span></span>      | <span data-ttu-id="16f6d-415">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="16f6d-415">Terminate worker</span></span>     |
| <span data-ttu-id="16f6d-416">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="16f6d-416">RETIREMENT</span></span>     | <span data-ttu-id="16f6d-417">Pensionile jäämine</span><span class="sxs-lookup"><span data-stu-id="16f6d-417">Retirement</span></span>       | <span data-ttu-id="16f6d-418">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="16f6d-418">Terminate worker</span></span>     |
| <span data-ttu-id="16f6d-419">OTHER</span><span class="sxs-lookup"><span data-stu-id="16f6d-419">OTHER</span></span>          | <span data-ttu-id="16f6d-420">Muud põhjused</span><span class="sxs-lookup"><span data-stu-id="16f6d-420">Other Reasons</span></span>    | <span data-ttu-id="16f6d-421">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="16f6d-421">Terminate worker</span></span>     |
| <span data-ttu-id="16f6d-422">DEATH</span><span class="sxs-lookup"><span data-stu-id="16f6d-422">DEATH</span></span>          | <span data-ttu-id="16f6d-423">Surm</span><span class="sxs-lookup"><span data-stu-id="16f6d-423">Death</span></span>            | <span data-ttu-id="16f6d-424">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="16f6d-424">Terminate worker</span></span>     |
| <span data-ttu-id="16f6d-425">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="16f6d-425">LEAVEOFABSENCE</span></span> | <span data-ttu-id="16f6d-426">Puhkus</span><span class="sxs-lookup"><span data-stu-id="16f6d-426">Leave of Absence</span></span> | <span data-ttu-id="16f6d-427">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="16f6d-427">Terminate worker</span></span>     |
| <span data-ttu-id="16f6d-428">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="16f6d-428">CONTRACTEND</span></span>    | <span data-ttu-id="16f6d-429">Lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="16f6d-429">End of Contract</span></span>  | <span data-ttu-id="16f6d-430">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="16f6d-430">Terminate worker</span></span>     |
| <span data-ttu-id="16f6d-431">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="16f6d-431">SALARYCHANGE</span></span>   | <span data-ttu-id="16f6d-432">Palga muutus</span><span class="sxs-lookup"><span data-stu-id="16f6d-432">Change of Salary</span></span> | <span data-ttu-id="16f6d-433">Hüvitus</span><span class="sxs-lookup"><span data-stu-id="16f6d-433">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="16f6d-434">Perekonnaseis</span><span class="sxs-lookup"><span data-stu-id="16f6d-434">Marital status</span></span>

<span data-ttu-id="16f6d-435">Perekonnaseisu väärtused vastendatakse Dayforce’i ja tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.</span><span class="sxs-lookup"><span data-stu-id="16f6d-435">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="16f6d-436">Järgmine tabel näitab, kuidas perekonnaseisu väärtusi Dayforce’i vastendatakse.</span><span class="sxs-lookup"><span data-stu-id="16f6d-436">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="16f6d-437">Talent</span><span class="sxs-lookup"><span data-stu-id="16f6d-437">Talent</span></span>                 | <span data-ttu-id="16f6d-438">Dayforce</span><span class="sxs-lookup"><span data-stu-id="16f6d-438">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="16f6d-439">Abielus</span><span class="sxs-lookup"><span data-stu-id="16f6d-439">Married</span></span>                | <span data-ttu-id="16f6d-440">Abielus</span><span class="sxs-lookup"><span data-stu-id="16f6d-440">Married</span></span>              |
| <span data-ttu-id="16f6d-441">Üksik</span><span class="sxs-lookup"><span data-stu-id="16f6d-441">Single</span></span>                 | <span data-ttu-id="16f6d-442">Üksik</span><span class="sxs-lookup"><span data-stu-id="16f6d-442">Single</span></span>               |
| <span data-ttu-id="16f6d-443">Lesk</span><span class="sxs-lookup"><span data-stu-id="16f6d-443">Widowed</span></span>                | <span data-ttu-id="16f6d-444">Lesk</span><span class="sxs-lookup"><span data-stu-id="16f6d-444">Widowed</span></span>              |
| <span data-ttu-id="16f6d-445">Lahutatud</span><span class="sxs-lookup"><span data-stu-id="16f6d-445">Divorced</span></span>               | <span data-ttu-id="16f6d-446">Lahutatud</span><span class="sxs-lookup"><span data-stu-id="16f6d-446">Divorced</span></span>             |
| <span data-ttu-id="16f6d-447">Registreeritud partnerlus</span><span class="sxs-lookup"><span data-stu-id="16f6d-447">Registered Partnership</span></span> | <span data-ttu-id="16f6d-448">Mitteabieluline kooselu</span><span class="sxs-lookup"><span data-stu-id="16f6d-448">Domestic Partnership</span></span> |
| <span data-ttu-id="16f6d-449">None</span><span class="sxs-lookup"><span data-stu-id="16f6d-449">None</span></span>                   | <span data-ttu-id="16f6d-450">None</span><span class="sxs-lookup"><span data-stu-id="16f6d-450">None</span></span>                 |
| <span data-ttu-id="16f6d-451">Kooselu</span><span class="sxs-lookup"><span data-stu-id="16f6d-451">Cohabiting</span></span>             | <span data-ttu-id="16f6d-452">Kooselu</span><span class="sxs-lookup"><span data-stu-id="16f6d-452">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="16f6d-453">Sugu</span><span class="sxs-lookup"><span data-stu-id="16f6d-453">Gender</span></span>

<span data-ttu-id="16f6d-454">Soo määratlused vastendatakse Dayforce’i ja tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.</span><span class="sxs-lookup"><span data-stu-id="16f6d-454">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="16f6d-455">Järgmine tabel näitab, kuidas soo määratlusi Dayforce’i vastendatakse.</span><span class="sxs-lookup"><span data-stu-id="16f6d-455">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="16f6d-456">Talent</span><span class="sxs-lookup"><span data-stu-id="16f6d-456">Talent</span></span>       | <span data-ttu-id="16f6d-457">Dayforce</span><span class="sxs-lookup"><span data-stu-id="16f6d-457">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="16f6d-458">Mees</span><span class="sxs-lookup"><span data-stu-id="16f6d-458">Male</span></span>         | <span data-ttu-id="16f6d-459">Mees</span><span class="sxs-lookup"><span data-stu-id="16f6d-459">Male</span></span>            |
| <span data-ttu-id="16f6d-460">Naine</span><span class="sxs-lookup"><span data-stu-id="16f6d-460">Female</span></span>       | <span data-ttu-id="16f6d-461">Naine</span><span class="sxs-lookup"><span data-stu-id="16f6d-461">Female</span></span>          |
| <span data-ttu-id="16f6d-462">Mittespetsiifiline</span><span class="sxs-lookup"><span data-stu-id="16f6d-462">Non-specific</span></span> | <span data-ttu-id="16f6d-463">*Ei toetata*</span><span class="sxs-lookup"><span data-stu-id="16f6d-463">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="16f6d-464">Tulukoodid</span><span class="sxs-lookup"><span data-stu-id="16f6d-464">Earning codes</span></span>

<span data-ttu-id="16f6d-465">Tulukoodid määratlevad kordumatult igat tüüpi tulud, mida töötajad saavad.</span><span class="sxs-lookup"><span data-stu-id="16f6d-465">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="16f6d-466">Koodid hõlmavad mitmeid tuludega seotud parameetreid, näiteks raamatupidamisreeglid, maksuseadused, aruandluse nõuded ja brutosumma võime.</span><span class="sxs-lookup"><span data-stu-id="16f6d-466">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="16f6d-467">Kui kasutatakse toetuseta sagedust, siis kasutatakse arvutamise jaoks vaikimisi sagedust **Iga makse**.</span><span class="sxs-lookup"><span data-stu-id="16f6d-467">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="16f6d-468">Toetatud sagedused</span><span class="sxs-lookup"><span data-stu-id="16f6d-468">Supported frequencies</span></span>

- <span data-ttu-id="16f6d-469">Kõik</span><span class="sxs-lookup"><span data-stu-id="16f6d-469">All</span></span>
- <span data-ttu-id="16f6d-470">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="16f6d-470">EVERYPAY</span></span>
- <span data-ttu-id="16f6d-471">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="16f6d-471">EACHPAYPERIOD</span></span>
- <span data-ttu-id="16f6d-472">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="16f6d-472">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="16f6d-473">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="16f6d-473">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="16f6d-474">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="16f6d-474">1OFMTH</span></span>
- <span data-ttu-id="16f6d-475">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="16f6d-475">LASTOFMTH</span></span>
- <span data-ttu-id="16f6d-476">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="16f6d-476">2OFMTH</span></span>
- <span data-ttu-id="16f6d-477">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="16f6d-477">3OFMTH</span></span>
- <span data-ttu-id="16f6d-478">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="16f6d-478">4OFMTH</span></span>
- <span data-ttu-id="16f6d-479">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="16f6d-479">5OFMTH</span></span>
- <span data-ttu-id="16f6d-480">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="16f6d-480">1N2OFMTH</span></span>
- <span data-ttu-id="16f6d-481">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="16f6d-481">3N4OFMTH</span></span>
- <span data-ttu-id="16f6d-482">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="16f6d-482">1N3OFMTH</span></span>
- <span data-ttu-id="16f6d-483">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="16f6d-483">1N4OFMTH</span></span>
- <span data-ttu-id="16f6d-484">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="16f6d-484">2N3OFMTH</span></span>
- <span data-ttu-id="16f6d-485">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="16f6d-485">2N4OFMTH</span></span>
- <span data-ttu-id="16f6d-486">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="16f6d-486">1N2N3OFMTH</span></span>
- <span data-ttu-id="16f6d-487">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="16f6d-487">1N2N4OFMTH</span></span>
- <span data-ttu-id="16f6d-488">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="16f6d-488">1N3N4OFMTH</span></span>
- <span data-ttu-id="16f6d-489">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="16f6d-489">2N3N4OFMTH</span></span>
- <span data-ttu-id="16f6d-490">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="16f6d-490">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="16f6d-491">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="16f6d-491">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="16f6d-492">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="16f6d-492">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="16f6d-493">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="16f6d-493">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="16f6d-494">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="16f6d-494">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="16f6d-495">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="16f6d-495">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="16f6d-496">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="16f6d-496">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="16f6d-497">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="16f6d-497">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="16f6d-498">Aadressid</span><span class="sxs-lookup"><span data-stu-id="16f6d-498">Addresses</span></span>

<span data-ttu-id="16f6d-499">Teatud riigi või regiooni, osariigi ja maakonna (haldusüksuse) koodide tuvastamise jaoks on vaja kindlaid vorminguid, mida Dayforce ning riigi-/regioonisisesed pakkujad ära tunnevad.</span><span class="sxs-lookup"><span data-stu-id="16f6d-499">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="16f6d-500">Kuigi linnade vorming on paindlik, peab iga linn olema seotud osariigiga.</span><span class="sxs-lookup"><span data-stu-id="16f6d-500">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="16f6d-501">Talent</span><span class="sxs-lookup"><span data-stu-id="16f6d-501">Talent</span></span>          | <span data-ttu-id="16f6d-502">Dayforce</span><span class="sxs-lookup"><span data-stu-id="16f6d-502">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="16f6d-503">Riik/regioon</span><span class="sxs-lookup"><span data-stu-id="16f6d-503">Country/Region</span></span>  | <span data-ttu-id="16f6d-504">Riigi kood</span><span class="sxs-lookup"><span data-stu-id="16f6d-504">Country Code</span></span>          |
| <span data-ttu-id="16f6d-505">Sihtnumber</span><span class="sxs-lookup"><span data-stu-id="16f6d-505">Zip/Postal Code</span></span> | <span data-ttu-id="16f6d-506">Sihtnumber</span><span class="sxs-lookup"><span data-stu-id="16f6d-506">Postal Code</span></span>           |
| <span data-ttu-id="16f6d-507">Osariik</span><span class="sxs-lookup"><span data-stu-id="16f6d-507">State</span></span>           | <span data-ttu-id="16f6d-508">Osariigi kood</span><span class="sxs-lookup"><span data-stu-id="16f6d-508">State Code</span></span>            |
| <span data-ttu-id="16f6d-509">Linn</span><span class="sxs-lookup"><span data-stu-id="16f6d-509">City</span></span>            | <span data-ttu-id="16f6d-510">Linn</span><span class="sxs-lookup"><span data-stu-id="16f6d-510">City</span></span>                  |
| <span data-ttu-id="16f6d-511">Maakond</span><span class="sxs-lookup"><span data-stu-id="16f6d-511">County</span></span>          | <span data-ttu-id="16f6d-512">Maakond (haldusüksus)</span><span class="sxs-lookup"><span data-stu-id="16f6d-512">County (Municipality)</span></span> |
| <span data-ttu-id="16f6d-513">Tänav</span><span class="sxs-lookup"><span data-stu-id="16f6d-513">Street</span></span>          | <span data-ttu-id="16f6d-514">Aadressirida 1</span><span class="sxs-lookup"><span data-stu-id="16f6d-514">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="16f6d-515">Maksuregioonid</span><span class="sxs-lookup"><span data-stu-id="16f6d-515">Tax regions</span></span>

<span data-ttu-id="16f6d-516">Maksuregioone kasutatakse palga loomisel sobiva maksu määramiseks.</span><span class="sxs-lookup"><span data-stu-id="16f6d-516">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="16f6d-517">Maksuregioonid vastendatakse Dayforce’i asukoha-aadressidena.</span><span class="sxs-lookup"><span data-stu-id="16f6d-517">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="16f6d-518">Maksuregiooni vaikevariant peab olema seotud töötaja aktiivse ametikohaga.</span><span class="sxs-lookup"><span data-stu-id="16f6d-518">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="16f6d-519">Maksuregioon (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-519">Tax region (required)</span></span>
- <span data-ttu-id="16f6d-520">Riik/regioon (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-520">Country/Region (required)</span></span>
- <span data-ttu-id="16f6d-521">Osariik (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-521">State (required)</span></span>
- <span data-ttu-id="16f6d-522">Maakond</span><span class="sxs-lookup"><span data-stu-id="16f6d-522">County</span></span> 
- <span data-ttu-id="16f6d-523">Linn (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="16f6d-523">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="16f6d-524">Andmete konfigureerimine palgaandmete loomiseks Mehhikos</span><span class="sxs-lookup"><span data-stu-id="16f6d-524">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="16f6d-525">Kui loote palgaandmeid Mehhiko töövõtjatele, siis peate konfigureerima järgmisi elemente.</span><span class="sxs-lookup"><span data-stu-id="16f6d-525">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="16f6d-526">Ametikohtadele tuleb määrata osakonnad.</span><span class="sxs-lookup"><span data-stu-id="16f6d-526">Departments are required on positions.</span></span>
- <span data-ttu-id="16f6d-527">Kulukeskused tuleb määratleda finantsdimensioonideks ja peavad olema vaike-finantsdimensiooni stringi esimene element.</span><span class="sxs-lookup"><span data-stu-id="16f6d-527">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="16f6d-528">Töötüübid</span><span class="sxs-lookup"><span data-stu-id="16f6d-528">Job types</span></span>

<span data-ttu-id="16f6d-529">Töötüüpe kasutatakse sarnaste tööde kategooriatesse grupeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="16f6d-529">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="16f6d-530">Mehhikos palgaarvestuse töötlemiseks on vajalikud töötüübid.</span><span class="sxs-lookup"><span data-stu-id="16f6d-530">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="16f6d-531">Töötüübid on näiteks täistööaeg ja osaline tööaeg või kuupalk ning tunnipalk.</span><span class="sxs-lookup"><span data-stu-id="16f6d-531">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="16f6d-532">Töötüübid vastendatakse Dayforce’i tasutüüpidena, mis näitavad, kas töövõtja on tunni- või palgatöötaja.</span><span class="sxs-lookup"><span data-stu-id="16f6d-532">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="16f6d-533">Järgmised töötüübid ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="16f6d-533">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="16f6d-534">Töö tüüp</span><span class="sxs-lookup"><span data-stu-id="16f6d-534">Job type</span></span>   | <span data-ttu-id="16f6d-535">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="16f6d-535">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="16f6d-536">Tunnimäär</span><span class="sxs-lookup"><span data-stu-id="16f6d-536">Hourly</span></span>     | <span data-ttu-id="16f6d-537">MX tunnimäär</span><span class="sxs-lookup"><span data-stu-id="16f6d-537">MX Hourly</span></span>   |
| <span data-ttu-id="16f6d-538">Põhipalk</span><span class="sxs-lookup"><span data-stu-id="16f6d-538">Salaried</span></span>   | <span data-ttu-id="16f6d-539">MX põhipalk</span><span class="sxs-lookup"><span data-stu-id="16f6d-539">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="16f6d-540">Positsioonitüübid</span><span class="sxs-lookup"><span data-stu-id="16f6d-540">Position types</span></span> 

<span data-ttu-id="16f6d-541">Ametikoha tüüpe kasutatakse selleks, et kirjeldada, kas ametikoht on täiskohaga, osalise tööajaga või midagi muud.</span><span class="sxs-lookup"><span data-stu-id="16f6d-541">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="16f6d-542">Ametikoha tüübid vastendatakse Dayforce’i tasuklassidena, mis näitavad, kas töövõtja on täis- või osalise tööajaga töötaja.</span><span class="sxs-lookup"><span data-stu-id="16f6d-542">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="16f6d-543">Järgmised ametikoha tüübid ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="16f6d-543">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="16f6d-544">Ametikoha tüüp</span><span class="sxs-lookup"><span data-stu-id="16f6d-544">Position type</span></span>   | <span data-ttu-id="16f6d-545">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="16f6d-545">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="16f6d-546">Täistööaeg</span><span class="sxs-lookup"><span data-stu-id="16f6d-546">Full-time</span></span>       | <span data-ttu-id="16f6d-547">Täistööajaga töövõtja</span><span class="sxs-lookup"><span data-stu-id="16f6d-547">Full time employee</span></span> |
| <span data-ttu-id="16f6d-548">Osaline tööaeg</span><span class="sxs-lookup"><span data-stu-id="16f6d-548">Part-time</span></span>       | <span data-ttu-id="16f6d-549">Osalise tööajaga töövõtja</span><span class="sxs-lookup"><span data-stu-id="16f6d-549">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="16f6d-550">Põhjuse koodid</span><span class="sxs-lookup"><span data-stu-id="16f6d-550">Reason codes</span></span>

<span data-ttu-id="16f6d-551">Põhjusekoodid annavad teavet töövõtja oleku kohta.</span><span class="sxs-lookup"><span data-stu-id="16f6d-551">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="16f6d-552">Põhjusekoodid vastendatakse Dayforce’i olekupõhjustena, mis näitavad töövõtja ametikoha või töösuhte oleku muutuse põhjust.</span><span class="sxs-lookup"><span data-stu-id="16f6d-552">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="16f6d-553">Järgmised põhjusekoodid ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="16f6d-553">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="16f6d-554">Põhjusekood</span><span class="sxs-lookup"><span data-stu-id="16f6d-554">Reason code</span></span>            | <span data-ttu-id="16f6d-555">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="16f6d-555">Description</span></span>                    | <span data-ttu-id="16f6d-556">Rakendatavad stsenaariumid</span><span class="sxs-lookup"><span data-stu-id="16f6d-556">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="16f6d-557">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="16f6d-557">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="16f6d-558">Lahkumine enne esimest palgamakset</span><span class="sxs-lookup"><span data-stu-id="16f6d-558">Departure before first payroll</span></span> | <span data-ttu-id="16f6d-559">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="16f6d-559">Terminate worker</span></span>     |
| <span data-ttu-id="16f6d-560">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="16f6d-560">RESIGNATION</span></span>            | <span data-ttu-id="16f6d-561">Lahkumine</span><span class="sxs-lookup"><span data-stu-id="16f6d-561">Resignation</span></span>                    | <span data-ttu-id="16f6d-562">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="16f6d-562">Terminate worker</span></span>     |
| <span data-ttu-id="16f6d-563">PENSION</span><span class="sxs-lookup"><span data-stu-id="16f6d-563">PENSION</span></span>                | <span data-ttu-id="16f6d-564">Pension</span><span class="sxs-lookup"><span data-stu-id="16f6d-564">Pension</span></span>                        | <span data-ttu-id="16f6d-565">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="16f6d-565">Terminate worker</span></span>     |
| <span data-ttu-id="16f6d-566">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="16f6d-566">TERMINATION</span></span>            | <span data-ttu-id="16f6d-567">Lõpetamine</span><span class="sxs-lookup"><span data-stu-id="16f6d-567">Termination</span></span>                    | <span data-ttu-id="16f6d-568">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="16f6d-568">Terminate worker</span></span>     |
| <span data-ttu-id="16f6d-569">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="16f6d-569">RETIREMENT</span></span>             | <span data-ttu-id="16f6d-570">Pensionile jäämine</span><span class="sxs-lookup"><span data-stu-id="16f6d-570">Retirement</span></span>                     | <span data-ttu-id="16f6d-571">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="16f6d-571">Terminate worker</span></span>     |
| <span data-ttu-id="16f6d-572">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="16f6d-572">ABSENTEE</span></span>               | <span data-ttu-id="16f6d-573">Puuduja</span><span class="sxs-lookup"><span data-stu-id="16f6d-573">Absentee</span></span>                       | <span data-ttu-id="16f6d-574">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="16f6d-574">Terminate worker</span></span>     |
| <span data-ttu-id="16f6d-575">OTHER</span><span class="sxs-lookup"><span data-stu-id="16f6d-575">OTHER</span></span>                  | <span data-ttu-id="16f6d-576">Muud põhjused</span><span class="sxs-lookup"><span data-stu-id="16f6d-576">Other Reasons</span></span>                  | <span data-ttu-id="16f6d-577">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="16f6d-577">Terminate worker</span></span>     |
| <span data-ttu-id="16f6d-578">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="16f6d-578">CLOSURE</span></span>                | <span data-ttu-id="16f6d-579">Ettevõte suletud</span><span class="sxs-lookup"><span data-stu-id="16f6d-579">Business Closure</span></span>               | <span data-ttu-id="16f6d-580">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="16f6d-580">Terminate worker</span></span>     |
| <span data-ttu-id="16f6d-581">DEATH</span><span class="sxs-lookup"><span data-stu-id="16f6d-581">DEATH</span></span>                  | <span data-ttu-id="16f6d-582">Surm</span><span class="sxs-lookup"><span data-stu-id="16f6d-582">Death</span></span>                          | <span data-ttu-id="16f6d-583">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="16f6d-583">Terminate worker</span></span>     |
| <span data-ttu-id="16f6d-584">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="16f6d-584">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="16f6d-585">Puhkus</span><span class="sxs-lookup"><span data-stu-id="16f6d-585">Leave of Absence</span></span>               | <span data-ttu-id="16f6d-586">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="16f6d-586">Terminate worker</span></span>     |
| <span data-ttu-id="16f6d-587">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="16f6d-587">CONTRACTEND</span></span>            | <span data-ttu-id="16f6d-588">Lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="16f6d-588">End of Contract</span></span>                | <span data-ttu-id="16f6d-589">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="16f6d-589">Terminate worker</span></span>     |
| <span data-ttu-id="16f6d-590">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="16f6d-590">SALARYCHANGE</span></span>           | <span data-ttu-id="16f6d-591">Palga muutus</span><span class="sxs-lookup"><span data-stu-id="16f6d-591">Change of Salary</span></span>               | <span data-ttu-id="16f6d-592">Hüvitus</span><span class="sxs-lookup"><span data-stu-id="16f6d-592">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="16f6d-593">Töösuhte tingimused</span><span class="sxs-lookup"><span data-stu-id="16f6d-593">Terms of employment</span></span>

<span data-ttu-id="16f6d-594">Töösuhte tingimusi kasutatakse töösuhte tingimuste kategooriate loomiseks.</span><span class="sxs-lookup"><span data-stu-id="16f6d-594">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="16f6d-595">Tingimused vastendatakse Dayforce’i töösuhte indikaatorväärtustena.</span><span class="sxs-lookup"><span data-stu-id="16f6d-595">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="16f6d-596">Järgmised töösuhte tingimused ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="16f6d-596">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="16f6d-597">Töösuhte tingimused</span><span class="sxs-lookup"><span data-stu-id="16f6d-597">Terms of employment</span></span>   | <span data-ttu-id="16f6d-598">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="16f6d-598">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="16f6d-599">Tavaline</span><span class="sxs-lookup"><span data-stu-id="16f6d-599">Regular</span></span>               | <span data-ttu-id="16f6d-600">Tavaline</span><span class="sxs-lookup"><span data-stu-id="16f6d-600">Regular</span></span>     |
| <span data-ttu-id="16f6d-601">Otse</span><span class="sxs-lookup"><span data-stu-id="16f6d-601">Direct</span></span>                | <span data-ttu-id="16f6d-602">Otse</span><span class="sxs-lookup"><span data-stu-id="16f6d-602">Direct</span></span>      |
| <span data-ttu-id="16f6d-603">Praktika</span><span class="sxs-lookup"><span data-stu-id="16f6d-603">Internship</span></span>            | <span data-ttu-id="16f6d-604">Praktika</span><span class="sxs-lookup"><span data-stu-id="16f6d-604">Internship</span></span>  |
| <span data-ttu-id="16f6d-605">Alaline</span><span class="sxs-lookup"><span data-stu-id="16f6d-605">Permanent</span></span>             | <span data-ttu-id="16f6d-606">Alaline</span><span class="sxs-lookup"><span data-stu-id="16f6d-606">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="16f6d-607">Perekonnaseis</span><span class="sxs-lookup"><span data-stu-id="16f6d-607">Marital status</span></span>

<span data-ttu-id="16f6d-608">Perekonnaseisu väärtused vastendatakse Dayforce’i ja tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.</span><span class="sxs-lookup"><span data-stu-id="16f6d-608">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="16f6d-609">Järgmine tabel näitab, kuidas perekonnaseisu väärtusi Dayforce’i vastendatakse.</span><span class="sxs-lookup"><span data-stu-id="16f6d-609">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="16f6d-610">Talent</span><span class="sxs-lookup"><span data-stu-id="16f6d-610">Talent</span></span>                 | <span data-ttu-id="16f6d-611">Dayforce</span><span class="sxs-lookup"><span data-stu-id="16f6d-611">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="16f6d-612">Abielus</span><span class="sxs-lookup"><span data-stu-id="16f6d-612">Married</span></span>                | <span data-ttu-id="16f6d-613">Abielus</span><span class="sxs-lookup"><span data-stu-id="16f6d-613">Married</span></span>                   |
| <span data-ttu-id="16f6d-614">Üksik</span><span class="sxs-lookup"><span data-stu-id="16f6d-614">Single</span></span>                 | <span data-ttu-id="16f6d-615">Üksik</span><span class="sxs-lookup"><span data-stu-id="16f6d-615">Single</span></span>                    |
| <span data-ttu-id="16f6d-616">Lesk</span><span class="sxs-lookup"><span data-stu-id="16f6d-616">Widowed</span></span>                | <span data-ttu-id="16f6d-617">Lesk</span><span class="sxs-lookup"><span data-stu-id="16f6d-617">Widowed</span></span>                   |
| <span data-ttu-id="16f6d-618">Lahutatud</span><span class="sxs-lookup"><span data-stu-id="16f6d-618">Divorced</span></span>               | <span data-ttu-id="16f6d-619">Lahutatud</span><span class="sxs-lookup"><span data-stu-id="16f6d-619">Divorced</span></span>                  |
| <span data-ttu-id="16f6d-620">Registreeritud partnerlus</span><span class="sxs-lookup"><span data-stu-id="16f6d-620">Registered Partnership</span></span> | <span data-ttu-id="16f6d-621">Mitteabieluline kooselu</span><span class="sxs-lookup"><span data-stu-id="16f6d-621">Domestic Partnership</span></span>      |
| <span data-ttu-id="16f6d-622">None</span><span class="sxs-lookup"><span data-stu-id="16f6d-622">None</span></span>                   | <span data-ttu-id="16f6d-623">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="16f6d-623">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="16f6d-624">Kooselu</span><span class="sxs-lookup"><span data-stu-id="16f6d-624">Cohabiting</span></span>             | <span data-ttu-id="16f6d-625">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="16f6d-625">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="16f6d-626">Sugu</span><span class="sxs-lookup"><span data-stu-id="16f6d-626">Gender</span></span>

<span data-ttu-id="16f6d-627">Soo määratlused vastendatakse Dayforce’i ja tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.</span><span class="sxs-lookup"><span data-stu-id="16f6d-627">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="16f6d-628">Järgmine tabel näitab, kuidas soo määratlusi Dayforce’i vastendatakse.</span><span class="sxs-lookup"><span data-stu-id="16f6d-628">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="16f6d-629">Talent</span><span class="sxs-lookup"><span data-stu-id="16f6d-629">Talent</span></span>       | <span data-ttu-id="16f6d-630">Dayforce</span><span class="sxs-lookup"><span data-stu-id="16f6d-630">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="16f6d-631">Mees</span><span class="sxs-lookup"><span data-stu-id="16f6d-631">Male</span></span>         | <span data-ttu-id="16f6d-632">Mees</span><span class="sxs-lookup"><span data-stu-id="16f6d-632">Male</span></span>                      |
| <span data-ttu-id="16f6d-633">Naine</span><span class="sxs-lookup"><span data-stu-id="16f6d-633">Female</span></span>       | <span data-ttu-id="16f6d-634">Naine</span><span class="sxs-lookup"><span data-stu-id="16f6d-634">Female</span></span>                    |
| <span data-ttu-id="16f6d-635">Mittespetsiifiline</span><span class="sxs-lookup"><span data-stu-id="16f6d-635">Non-specific</span></span> | <span data-ttu-id="16f6d-636">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="16f6d-636">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="16f6d-637">Makseviis</span><span class="sxs-lookup"><span data-stu-id="16f6d-637">Payment method</span></span>

<span data-ttu-id="16f6d-638">Makseviisid võimaldavad töövõtjal ja ettevõttel kirjeldada, kuidas töövõtjatele makstakse.</span><span class="sxs-lookup"><span data-stu-id="16f6d-638">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="16f6d-639">Makseviisid vastendatakse Dayforce’i ja tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.</span><span class="sxs-lookup"><span data-stu-id="16f6d-639">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="16f6d-640">Järgmine tabel näitab, kuidas makseviise Dayforce’i vastendatakse.</span><span class="sxs-lookup"><span data-stu-id="16f6d-640">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="16f6d-641">Talent</span><span class="sxs-lookup"><span data-stu-id="16f6d-641">Talent</span></span>             | <span data-ttu-id="16f6d-642">Dayforce</span><span class="sxs-lookup"><span data-stu-id="16f6d-642">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="16f6d-643">Sularaha</span><span class="sxs-lookup"><span data-stu-id="16f6d-643">Cash</span></span>               | <span data-ttu-id="16f6d-644">Sularaha</span><span class="sxs-lookup"><span data-stu-id="16f6d-644">Cash</span></span>                      |
| <span data-ttu-id="16f6d-645">Elektrooniline makse</span><span class="sxs-lookup"><span data-stu-id="16f6d-645">Electronic Payment</span></span> | <span data-ttu-id="16f6d-646">Ülekanne</span><span class="sxs-lookup"><span data-stu-id="16f6d-646">Transfer</span></span>                  |
| <span data-ttu-id="16f6d-647">Kontrolli</span><span class="sxs-lookup"><span data-stu-id="16f6d-647">Check</span></span>              | <span data-ttu-id="16f6d-648">Tšekk</span><span class="sxs-lookup"><span data-stu-id="16f6d-648">Cheque</span></span>                    |
| <span data-ttu-id="16f6d-649">Pangaveksel</span><span class="sxs-lookup"><span data-stu-id="16f6d-649">Bank Draft</span></span>         | <span data-ttu-id="16f6d-650">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="16f6d-650">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="16f6d-651">Muud</span><span class="sxs-lookup"><span data-stu-id="16f6d-651">Other</span></span>              | <span data-ttu-id="16f6d-652">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="16f6d-652">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="16f6d-653">Pangakonto tüüp</span><span class="sxs-lookup"><span data-stu-id="16f6d-653">Bank account type</span></span>

<span data-ttu-id="16f6d-654">Pangakonto tüüpe kasutatakse elektrooniliste maksete tegemiseks töötajatele.</span><span class="sxs-lookup"><span data-stu-id="16f6d-654">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="16f6d-655">Pangakonto tüübid vastendatakse Dayforce’i ülekandekonto teabena.</span><span class="sxs-lookup"><span data-stu-id="16f6d-655">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="16f6d-656">Pangakonto tüübid tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.</span><span class="sxs-lookup"><span data-stu-id="16f6d-656">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="16f6d-657">Talent</span><span class="sxs-lookup"><span data-stu-id="16f6d-657">Talent</span></span>            | <span data-ttu-id="16f6d-658">Dayforce</span><span class="sxs-lookup"><span data-stu-id="16f6d-658">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="16f6d-659">Jooksevkonto</span><span class="sxs-lookup"><span data-stu-id="16f6d-659">Checking Account</span></span>  | <span data-ttu-id="16f6d-660">Jooksevkonto</span><span class="sxs-lookup"><span data-stu-id="16f6d-660">CheckingAccount</span></span>           |
| <span data-ttu-id="16f6d-661">Palgakonto</span><span class="sxs-lookup"><span data-stu-id="16f6d-661">Payroll Account</span></span>   | <span data-ttu-id="16f6d-662">Palgakonto</span><span class="sxs-lookup"><span data-stu-id="16f6d-662">PayrollAccount</span></span>            |
| <span data-ttu-id="16f6d-663">Hoiukonto</span><span class="sxs-lookup"><span data-stu-id="16f6d-663">Savings Account</span></span>   | <span data-ttu-id="16f6d-664">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="16f6d-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="16f6d-665">BankGiroti konto</span><span class="sxs-lookup"><span data-stu-id="16f6d-665">BankGirot account</span></span> | <span data-ttu-id="16f6d-666">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="16f6d-666">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="16f6d-667">PlusGiroti konto</span><span class="sxs-lookup"><span data-stu-id="16f6d-667">PlusGirot account</span></span> | <span data-ttu-id="16f6d-668">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="16f6d-668">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="16f6d-669">Tulukoodid</span><span class="sxs-lookup"><span data-stu-id="16f6d-669">Earning codes</span></span>

<span data-ttu-id="16f6d-670">Tulukoodid määratlevad kordumatult igat tüüpi tulud, mida töötajad saavad.</span><span class="sxs-lookup"><span data-stu-id="16f6d-670">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="16f6d-671">Koodid hõlmavad mitmeid tuludega seotud parameetreid, näiteks raamatupidamisreeglid, maksuseadused, aruandluse nõuded ja brutosumma võime.</span><span class="sxs-lookup"><span data-stu-id="16f6d-671">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="16f6d-672">Kui kasutatakse toetuseta sagedust, siis kasutatakse arvutamise jaoks vaikimisi sagedust **Iga makse**.</span><span class="sxs-lookup"><span data-stu-id="16f6d-672">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="16f6d-673">Toetatud sagedused</span><span class="sxs-lookup"><span data-stu-id="16f6d-673">Supported frequencies</span></span>

- <span data-ttu-id="16f6d-674">Kõik</span><span class="sxs-lookup"><span data-stu-id="16f6d-674">All</span></span>
- <span data-ttu-id="16f6d-675">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="16f6d-675">EVERYPAY</span></span>
- <span data-ttu-id="16f6d-676">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="16f6d-676">EACHPAYPERIOD</span></span>
- <span data-ttu-id="16f6d-677">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="16f6d-677">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="16f6d-678">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="16f6d-678">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="16f6d-679">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="16f6d-679">1OFMTH</span></span>
- <span data-ttu-id="16f6d-680">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="16f6d-680">LASTOFMTH</span></span>
- <span data-ttu-id="16f6d-681">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="16f6d-681">2OFMTH</span></span>
- <span data-ttu-id="16f6d-682">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="16f6d-682">3OFMTH</span></span>
- <span data-ttu-id="16f6d-683">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="16f6d-683">4OFMTH</span></span>
- <span data-ttu-id="16f6d-684">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="16f6d-684">5OFMTH</span></span>
- <span data-ttu-id="16f6d-685">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="16f6d-685">1N2OFMTH</span></span>
- <span data-ttu-id="16f6d-686">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="16f6d-686">3N4OFMTH</span></span>
- <span data-ttu-id="16f6d-687">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="16f6d-687">1N3OFMTH</span></span>
- <span data-ttu-id="16f6d-688">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="16f6d-688">1N4OFMTH</span></span>
- <span data-ttu-id="16f6d-689">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="16f6d-689">2N3OFMTH</span></span>
- <span data-ttu-id="16f6d-690">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="16f6d-690">2N4OFMTH</span></span>
- <span data-ttu-id="16f6d-691">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="16f6d-691">1N2N3OFMTH</span></span>
- <span data-ttu-id="16f6d-692">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="16f6d-692">1N2N4OFMTH</span></span>
- <span data-ttu-id="16f6d-693">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="16f6d-693">1N3N4OFMTH</span></span>
- <span data-ttu-id="16f6d-694">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="16f6d-694">2N3N4OFMTH</span></span>
- <span data-ttu-id="16f6d-695">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="16f6d-695">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="16f6d-696">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="16f6d-696">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="16f6d-697">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="16f6d-697">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="16f6d-698">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="16f6d-698">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="16f6d-699">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="16f6d-699">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="16f6d-700">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="16f6d-700">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="16f6d-701">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="16f6d-701">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="16f6d-702">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="16f6d-702">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="16f6d-703">Aadressid</span><span class="sxs-lookup"><span data-stu-id="16f6d-703">Addresses</span></span>

<span data-ttu-id="16f6d-704">Teatud riigi või regiooni, osariigi ja maakonna (haldusüksuse) koodide tuvastamise jaoks on vaja kindlaid vorminguid, mida Dayforce ning riigi-/regioonisisesed pakkujad ära tunnevad.</span><span class="sxs-lookup"><span data-stu-id="16f6d-704">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="16f6d-705">Kuigi linnade vorming on paindlik, peab iga linn olema seotud osariigiga.</span><span class="sxs-lookup"><span data-stu-id="16f6d-705">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="16f6d-706">Talent</span><span class="sxs-lookup"><span data-stu-id="16f6d-706">Talent</span></span>              | <span data-ttu-id="16f6d-707">Dayforce</span><span class="sxs-lookup"><span data-stu-id="16f6d-707">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="16f6d-708">Riik/regioon</span><span class="sxs-lookup"><span data-stu-id="16f6d-708">Country/Region</span></span>      | <span data-ttu-id="16f6d-709">Riigi kood</span><span class="sxs-lookup"><span data-stu-id="16f6d-709">Country Code</span></span>          |
| <span data-ttu-id="16f6d-710">Sihtnumber</span><span class="sxs-lookup"><span data-stu-id="16f6d-710">Zip/Postal Code</span></span>     | <span data-ttu-id="16f6d-711">Sihtnumber</span><span class="sxs-lookup"><span data-stu-id="16f6d-711">Postal Code</span></span>           |
| <span data-ttu-id="16f6d-712">Osariik</span><span class="sxs-lookup"><span data-stu-id="16f6d-712">State</span></span>               | <span data-ttu-id="16f6d-713">Osariigi kood</span><span class="sxs-lookup"><span data-stu-id="16f6d-713">State Code</span></span>            |
| <span data-ttu-id="16f6d-714">Linn</span><span class="sxs-lookup"><span data-stu-id="16f6d-714">City</span></span>                | <span data-ttu-id="16f6d-715">Linn</span><span class="sxs-lookup"><span data-stu-id="16f6d-715">City</span></span>                  |
| <span data-ttu-id="16f6d-716">Maakond</span><span class="sxs-lookup"><span data-stu-id="16f6d-716">County</span></span>              | <span data-ttu-id="16f6d-717">Maakond (haldusüksus)</span><span class="sxs-lookup"><span data-stu-id="16f6d-717">County (Municipality)</span></span> |
| <span data-ttu-id="16f6d-718">Tänav</span><span class="sxs-lookup"><span data-stu-id="16f6d-718">Street</span></span>              | <span data-ttu-id="16f6d-719">Aadressirida 1</span><span class="sxs-lookup"><span data-stu-id="16f6d-719">Address Line 1</span></span>        |
| <span data-ttu-id="16f6d-720">Majanumber</span><span class="sxs-lookup"><span data-stu-id="16f6d-720">Street Number</span></span>       | <span data-ttu-id="16f6d-721">Aadressirida 2</span><span class="sxs-lookup"><span data-stu-id="16f6d-721">Address Line 2</span></span>        |
| <span data-ttu-id="16f6d-722">Hoone tähis</span><span class="sxs-lookup"><span data-stu-id="16f6d-722">Building Complement</span></span> | <span data-ttu-id="16f6d-723">Aadressirida 5</span><span class="sxs-lookup"><span data-stu-id="16f6d-723">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="16f6d-724">Passi number</span><span class="sxs-lookup"><span data-stu-id="16f6d-724">Passport number</span></span>

<span data-ttu-id="16f6d-725">Töötajad saavad deklareerida passi teavet.</span><span class="sxs-lookup"><span data-stu-id="16f6d-725">Employees can declare passport information.</span></span> <span data-ttu-id="16f6d-726">See teave on identifitseerimistüüpi **Pass** ja integreeritakse Dayforce’i töövõtja Mehhiko-teabe osana.</span><span class="sxs-lookup"><span data-stu-id="16f6d-726">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="16f6d-727">Identifitseerimistüüp = pass</span><span class="sxs-lookup"><span data-stu-id="16f6d-727">Identification Type = "Passport"</span></span>
- <span data-ttu-id="16f6d-728">Väljastamise kuupäev</span><span class="sxs-lookup"><span data-stu-id="16f6d-728">Issued Date</span></span>
- <span data-ttu-id="16f6d-729">Aegumiskuupäev</span><span class="sxs-lookup"><span data-stu-id="16f6d-729">Expiration Date</span></span>

<span data-ttu-id="16f6d-730">Töövõtjad saavad deklareerida mitu **Pass**-identifitseerimistüüpi ID-numbrit.</span><span class="sxs-lookup"><span data-stu-id="16f6d-730">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="16f6d-731">Dayforce’i integreeritakse siiski ainult praegune aktiivne passikirje.</span><span class="sxs-lookup"><span data-stu-id="16f6d-731">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="16f6d-732">Kui kõik passikirjed on aegunud, siis integreeritakse Dayforce’i pass, mis väljastati viimasena.</span><span class="sxs-lookup"><span data-stu-id="16f6d-732">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>

