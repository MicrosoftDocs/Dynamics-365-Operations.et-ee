---
title: Rakenduste Talent ja Dayforce vahelise palgaarvestuse integratsiooni konfigureerimine
description: Selles teemas selgitatakse, kuidas konfigureerida rakenduste Microsoft Dynamics 365 for Talent ja Ceridian Dayforce vahelist integratsiooni nii, et saaksite teha palgatöötlust.
author: jcart1106
manager: AnnBe
ms.date: 07/10/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, Talent
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fcddf82cffb9f0ba94b83eb21809b810585ebc9e
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/29/2019
ms.locfileid: "304025"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="8c7ec-103">Palgaarvestuse integratsiooni konfigureerimine Talenti ja Dayforce’i vahel</span><span class="sxs-lookup"><span data-stu-id="8c7ec-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8c7ec-104">Rakenduste Microsoft Dynamics 365 for Talent ja Ceridian Dayforce vaheline integratsioon sõltub mitmest konfiguratsioonietapist, mida kirjeldatakse selles teemas.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-104">The integration between Microsoft Dynamics 365 for Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="8c7ec-105">Enne palgatöötluse tegemist peate konfigureerima integratsiooni nii rakenduses Talent kui ka Dayforce.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="8c7ec-106">Kui te kasutate palgatöötluste tegemiseks teenust nagu Dayforce, siis peate rakenduses Talent integratsiooni lubama.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="8c7ec-107">Integratsiooni jaoks on rakendusest Talent vaja teatud andmeid.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="8c7ec-108">Seega peate kinnitama, et Dayforce’iga vastendatud andmed on rakenduses Talent konfigureeritud viisil, mis lubab integratsiooni.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="8c7ec-109">Integratsioon kasutab järgmisi üldisi andmekategooriaid.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="8c7ec-110">Inimressursside andmed</span><span class="sxs-lookup"><span data-stu-id="8c7ec-110">Human resources data</span></span>
- <span data-ttu-id="8c7ec-111">Hüvituse andmed</span><span class="sxs-lookup"><span data-stu-id="8c7ec-111">Compensation data</span></span>
- <span data-ttu-id="8c7ec-112">Palgaandmed, näiteks palgatsüklid, makseperioodid ja tulukoodid</span><span class="sxs-lookup"><span data-stu-id="8c7ec-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="8c7ec-113">Töötaja andmed</span><span class="sxs-lookup"><span data-stu-id="8c7ec-113">Worker data</span></span>

<span data-ttu-id="8c7ec-114">Teemas kirjeldatakse etappe, mida peate integratsiooni lubamiseks läbima.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="8c7ec-115">Samuti selgitatakse integratsiooni jaoks vajalikke andmetüüpe ja konfigureerimise üksikasju.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="8c7ec-116">Integratsiooni lubamine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-116">Enable the integration</span></span>

<span data-ttu-id="8c7ec-117">Dayforce’iga ühendamiseks peate rakenduses Talent sisse lülitama integratsiooni ja sisestama konfigureerimisteabe.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="8c7ec-118">Kui soovite, et loodav pearaamatu kanne imporditaks rakendusse Microsoft Dynamics 365 for Finance and Operations, siis peate seadistama Microsoft Azure’i salvestuskonto ja sisestama Azure’i salvestusruumi ühendusstringi rakendusse Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 for Finance and Operations, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance and Operations.</span></span>

<span data-ttu-id="8c7ec-119">Rakenduses Talent integratsiooni sisselülitamiseks järgige järgmisi juhiseid.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="8c7ec-120">Valige lehelt **Süsteemihaldus** suvand **Integratsiooni konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="8c7ec-121">Sisestage turvalise failiedastusprotokolli File Transfer Protocol (FTP) lõpp-punkt ja turvalise FTP kausta tee.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="8c7ec-122">Sisestage selle kasutaja kasutajanimi ja parool, kellel on vaja juurdepääsu turvalise FTP lõpp-punktile ja kausta teele.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="8c7ec-123">Testige ühendust vajaduse järgi ja määrake suvand **Palgaarvestuse integratsiooni lubamine** olekule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="8c7ec-124">Kui integratsioon on sisse lülitatud, luuakse andmete ekspordipakett ja -failid ning määratakse sagedus.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="8c7ec-125">Vajaduse korral saate seda sagedust muuta.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="8c7ec-126">Lisateavet Azure’i talletamiskontode ja Azure’i salvestusruumi ühendusstringide kohta leiate järgmistest Azure’i teemadest.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="8c7ec-127">Azure’i salvestuskontod</span><span class="sxs-lookup"><span data-stu-id="8c7ec-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="8c7ec-128">Azure’i salvestusruumi ühendusstringide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/en-us/azure/storage/common/storage-configure-connection-string)

## <a name="configure-your-data"></a><span data-ttu-id="8c7ec-129">Andmete konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-129">Configure your data</span></span> 

<span data-ttu-id="8c7ec-130">Palgaarvestuse töötlemiseks peate konfigureerima rakenduses Talent personaliandmeid.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-130">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="8c7ec-131">Peate määratlema organisatsiooni andmeid nagu tööd ja ametikohad, samuti teavet soodustuste ning kompensatsioonide kohta.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-131">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="8c7ec-132">Selle teabe hulka kuulub töövõtja palgaandmete loomiseks vajalik teave töösuhte, palga ja mahaarvamiste kohta.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-132">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="8c7ec-133">Personaliandmed</span><span class="sxs-lookup"><span data-stu-id="8c7ec-133">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="8c7ec-134">Soodustused</span><span class="sxs-lookup"><span data-stu-id="8c7ec-134">Benefits</span></span> 

<span data-ttu-id="8c7ec-135">Inimressursid pakuvad tööriistu, mis aitavad seadistada ja hallata soodustusi, mahaarvamisi ning töötajate hüvitusplaane, mida organisatsioon oma töötajatele pakub või nende puhul töötleb.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-135">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="8c7ec-136">Soodustuste loomisel pidage meeles järgmisi Dayforce’is kasutatavaid andmeid ja konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-136">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="8c7ec-137">Soodustusplaanid</span><span class="sxs-lookup"><span data-stu-id="8c7ec-137">Benefit plans</span></span>

- <span data-ttu-id="8c7ec-138">Plaan (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-138">Plan (required)</span></span>
- <span data-ttu-id="8c7ec-139">Tüüp (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-139">Type (required)</span></span>
- <span data-ttu-id="8c7ec-140">Palga mõju (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-140">Payroll impact (required)</span></span>
- <span data-ttu-id="8c7ec-141">Võlgnevuste sissenõudmine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-141">Recover arrears</span></span>
- <span data-ttu-id="8c7ec-142">Mahaarvamismeetod</span><span class="sxs-lookup"><span data-stu-id="8c7ec-142">Deduction method</span></span>
- <span data-ttu-id="8c7ec-143">Mahaarvamise prioriteet</span><span class="sxs-lookup"><span data-stu-id="8c7ec-143">Deduction priority</span></span>
- <span data-ttu-id="8c7ec-144">Perioodi piiramine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-144">Limit period</span></span>
- <span data-ttu-id="8c7ec-145">Piirsumma</span><span class="sxs-lookup"><span data-stu-id="8c7ec-145">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="8c7ec-146">Soodustused</span><span class="sxs-lookup"><span data-stu-id="8c7ec-146">Benefits</span></span>

- <span data-ttu-id="8c7ec-147">Plaan (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-147">Plan (required)</span></span>
- <span data-ttu-id="8c7ec-148">Tüüp (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-148">Type (required)</span></span>
- <span data-ttu-id="8c7ec-149">Suvand (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-149">Option (required)</span></span>
- <span data-ttu-id="8c7ec-150">Soodustuse ID (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-150">Benefit ID (required)</span></span>
- <span data-ttu-id="8c7ec-151">Sagedus</span><span class="sxs-lookup"><span data-stu-id="8c7ec-151">Frequency</span></span>
- <span data-ttu-id="8c7ec-152">Alus</span><span class="sxs-lookup"><span data-stu-id="8c7ec-152">Basis</span></span>
- <span data-ttu-id="8c7ec-153">Summa või määr</span><span class="sxs-lookup"><span data-stu-id="8c7ec-153">Amount or rate</span></span>
- <span data-ttu-id="8c7ec-154">Tulukood</span><span class="sxs-lookup"><span data-stu-id="8c7ec-154">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="8c7ec-155">Toetatud sagedused</span><span class="sxs-lookup"><span data-stu-id="8c7ec-155">Supported frequencies</span></span> 

- <span data-ttu-id="8c7ec-156">Iga nädal</span><span class="sxs-lookup"><span data-stu-id="8c7ec-156">Weekly</span></span>
- <span data-ttu-id="8c7ec-157">Kahe nädala tagant</span><span class="sxs-lookup"><span data-stu-id="8c7ec-157">Bi-weekly</span></span>
- <span data-ttu-id="8c7ec-158">Iga poole kuu tagant</span><span class="sxs-lookup"><span data-stu-id="8c7ec-158">Semi-monthly</span></span>
- <span data-ttu-id="8c7ec-159">Kord kuus</span><span class="sxs-lookup"><span data-stu-id="8c7ec-159">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="8c7ec-160">Toetatud alused</span><span class="sxs-lookup"><span data-stu-id="8c7ec-160">Supported bases</span></span> 

- <span data-ttu-id="8c7ec-161">Fikseeritud summa</span><span class="sxs-lookup"><span data-stu-id="8c7ec-161">Fixed amount</span></span>
- <span data-ttu-id="8c7ec-162">Tulu protsent</span><span class="sxs-lookup"><span data-stu-id="8c7ec-162">Percent of earnings</span></span>
- <span data-ttu-id="8c7ec-163">Produktiivsed tunnid</span><span class="sxs-lookup"><span data-stu-id="8c7ec-163">Productive hours</span></span>

<span data-ttu-id="8c7ec-164">Dayforce loob järgmised mahaarvamised palga mõju alusel, mis on määratletud soodustusplaanis.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-164">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="8c7ec-165">Valik rakenduses Talent</span><span class="sxs-lookup"><span data-stu-id="8c7ec-165">Selection in Talent</span></span>        | <span data-ttu-id="8c7ec-166">Tulemus rakenduses Dayforce</span><span class="sxs-lookup"><span data-stu-id="8c7ec-166">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="8c7ec-167">Pole</span><span class="sxs-lookup"><span data-stu-id="8c7ec-167">None</span></span>                       | <span data-ttu-id="8c7ec-168">Mahaarvamist ei looda.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-168">No deduction is created.</span></span>                      |
| <span data-ttu-id="8c7ec-169">Ainult mahaarvamine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-169">Deduction only</span></span>             | <span data-ttu-id="8c7ec-170">Luuakse töövõtja mahaarvamine.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-170">An employee deduction is created.</span></span>             |
| <span data-ttu-id="8c7ec-171">Ainult lisamine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-171">Contribution only</span></span>          | <span data-ttu-id="8c7ec-172">Luuakse tööandja mahaarvamine.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-172">An employer deduction is created.</span></span>             |
| <span data-ttu-id="8c7ec-173">Mahaarvamine ja lisamine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-173">Deduction and contribution</span></span> | <span data-ttu-id="8c7ec-174">Luuakse töövõtja ja tööandja mahaarvamised.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-174">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="8c7ec-175">Lisateavet soodustusprogrammi määratlemise ja haldamise kohta vaadake järgmistest teemadest.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-175">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="8c7ec-176">Töötaja soodustuste programmi pakkumine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-176">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="8c7ec-177">Uue soodustuse loomine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-177">Create a new benefit</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="8c7ec-178">Soodustuskõlblikkuse reeglite ja poliitikate määratlemine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-178">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="8c7ec-179">Töötajate soodustuste registreerimine ja eemaldamine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-179">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="8c7ec-180">Hüvitus</span><span class="sxs-lookup"><span data-stu-id="8c7ec-180">Compensation</span></span> 

<span data-ttu-id="8c7ec-181">Hüvituste haldust kasutatakse põhitasu ja preemiate jagamise juhtimiseks.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-181">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="8c7ec-182">Töötaja fikseeritud põhipalga ja preemia tõusu juhitakse põhipalga plaanide kaudu.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-182">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="8c7ec-183">Lisatasude (nt preemiate, tulemustasude aktsiate eelismüügi ja toetuste ning ühekordsete preemiate) maksmist juhitakse ergutussüsteemi plaanide kaudu.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-183">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="8c7ec-184">Dayforce kasutab hüvituse teavet töövõtja tunni- või aastamäära arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-184">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="8c7ec-185">Nõutavad on põhipalgaplaanid ja palgamäära teisendamised.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-185">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="8c7ec-186">Töövõtjad peavad olema seotud põhipalgaplaaniga.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-186">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="8c7ec-187">Lisateavet hüvitusplaanide kohta vaadake järgmistest teemadest.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-187">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="8c7ec-188">Põhipalga plaanide loomine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-188">Create fixed compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="8c7ec-189">Ergutussüsteemi plaanide loomine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-189">Create variable compensation plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="8c7ec-190">Palga/hüvituse struktuuri ja plaanide arendamine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-190">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="8c7ec-191">Hüvitusprotsess</span><span class="sxs-lookup"><span data-stu-id="8c7ec-191">Process compensation</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="8c7ec-192">Hüvitusprotsessi määratlemine ja tulemuste arvutamine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-192">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="8c7ec-193">Töötaja liitmine põhipalga plaaniga</span><span class="sxs-lookup"><span data-stu-id="8c7ec-193">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="8c7ec-194">Töötaja liitmine tulemustasu plaaniga</span><span class="sxs-lookup"><span data-stu-id="8c7ec-194">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="8c7ec-195">Tööd</span><span class="sxs-lookup"><span data-stu-id="8c7ec-195">Jobs</span></span> 

<span data-ttu-id="8c7ec-196">Töö on tööd tegeva isiku jaoks nõutavate ülesannete ja vastutuste kogum.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-196">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="8c7ec-197">Lisateavet vt järgmistest teemadest:</span><span class="sxs-lookup"><span data-stu-id="8c7ec-197">For more information, see the following topics:</span></span>

- [<span data-ttu-id="8c7ec-198">Töö komponentide seadistamine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-198">Setting up the components of a job</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="8c7ec-199">Uute tööde määratlemine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-199">Define new jobs</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="8c7ec-200">Ametikohad</span><span class="sxs-lookup"><span data-stu-id="8c7ec-200">Positions</span></span>

<span data-ttu-id="8c7ec-201">Ametikoht on töökoha üksik eksemplar.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-201">A position is an individual instance of a job.</span></span> <span data-ttu-id="8c7ec-202">Näiteks on ametikoht „müügijuht (Ida)” vaid üks tööga „müügijuht” seostatud ametikohti.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-202">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="8c7ec-203">Ametikoht kuulub osakonna alla.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-203">A position exists in a department.</span></span> <span data-ttu-id="8c7ec-204">Iga ametikohaga saab seostada vaid ühte töötajat.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-204">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="8c7ec-205">Ametikohtade seadistamisel pidage meeles järgmisi andmeid ja konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-205">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="8c7ec-206">Ametikoht (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-206">Position (required)</span></span>
- <span data-ttu-id="8c7ec-207">Kirjeldus (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-207">Description (required)</span></span>
- <span data-ttu-id="8c7ec-208">Töö (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-208">Job (required)</span></span>
- <span data-ttu-id="8c7ec-209">Osakond (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-209">Department (required)</span></span>
- <span data-ttu-id="8c7ec-210">Ametikoha tüüp (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-210">Position type (required)</span></span>
- <span data-ttu-id="8c7ec-211">Täistööaja vaste</span><span class="sxs-lookup"><span data-stu-id="8c7ec-211">Full-time equivalent</span></span>
- <span data-ttu-id="8c7ec-212">Iga-aastased regulaarsed tunnid (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-212">Annual regular hours (required)</span></span>
- <span data-ttu-id="8c7ec-213">Maksja juriidiline isik (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-213">Paid by legal entity (required)</span></span>
- <span data-ttu-id="8c7ec-214">Palgatsükkel (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-214">Pay cycle (required)</span></span>
- <span data-ttu-id="8c7ec-215">Vaike-finantsdimensioonid – kulukeskus (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-215">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="8c7ec-216">Töötaja määramine – töötaja, määramise algus, määramise lõpp, põhjuse kood</span><span class="sxs-lookup"><span data-stu-id="8c7ec-216">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="8c7ec-217">Kui ühes osakonnas on sama tööga seotud mitu ametikohta, siis konsolideeritakse need rakenduses Dayforce üheks ametikohaks.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-217">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="8c7ec-218">Lisateavet vt järgmistest teemadest:</span><span class="sxs-lookup"><span data-stu-id="8c7ec-218">For more information, see the following topics:</span></span>

- [<span data-ttu-id="8c7ec-219">Tööjõu korraldamine osakondade, tööde ja ametikohtade abil</span><span class="sxs-lookup"><span data-stu-id="8c7ec-219">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="8c7ec-220">Ametikohtade seadistamine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-220">Set up positions</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="8c7ec-221">Osakonnad</span><span class="sxs-lookup"><span data-stu-id="8c7ec-221">Departments</span></span>

<span data-ttu-id="8c7ec-222">Osakond on tootmisüksus, mis esindab organisatsiooni kategooriat või funktsionaalset ala.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-222">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="8c7ec-223">Osakond vastutab organisatsiooni kindla valdkonna eest, nagu müük, raamatupidamine või inimressursid.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-223">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="8c7ec-224">Saate osakondi kasutada funktsionaalsete alade aruannete koostamiseks.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-224">You can use departments to report on functional areas.</span></span> <span data-ttu-id="8c7ec-225">Osakonnad võivad vastutada kasumi ja kahjumi eest.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-225">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="8c7ec-226">Lisateavet vt järgmistest teemadest:</span><span class="sxs-lookup"><span data-stu-id="8c7ec-226">For more information, see the following topics:</span></span>

- [<span data-ttu-id="8c7ec-227">Osakonna loomine ja selle seostamine osakonnahierarhiaga</span><span class="sxs-lookup"><span data-stu-id="8c7ec-227">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="8c7ec-228">Uute osakondade määratlemine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-228">Define new departments</span></span>](https://docs.microsoft.com/en-us/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="8c7ec-229">Palgatsüklid ja makseperioodid</span><span class="sxs-lookup"><span data-stu-id="8c7ec-229">Pay cycles and pay periods</span></span>

<span data-ttu-id="8c7ec-230">Palgatsükkel määrab, kui tihti palgamaksmine toimub ja konkreetsed päevad, millal töötajatele palka makstakse.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-230">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="8c7ec-231">Näiteks võib palgatsükli sageduseks olla üks kuu ja töövõtjatele makstakse seega kuu viimasel päeval.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-231">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="8c7ec-232">Või kui palgatsükli sageduseks on üks nädal, siis makstakse töövõtjatele näiteks teisipäeviti pärast makseperioodi lõppu.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-232">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="8c7ec-233">Palgatsükleid määratakse ametikohtadele selleks, et määrata, millal nendel ametikohtadel töötavatele töötajatele palka makstakse.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-233">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="8c7ec-234">Pärast palgatsüklite loomist saate iga tsükli jaoks luua makseperioodid.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-234">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="8c7ec-235">Igal makseperioodil on makse vaikekuupäev, mis põhineb teie sisestatud teabel.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-235">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="8c7ec-236">Siiski saate erandite käsitlemiseks makseperioodi makse vaikekuupäeva muuta, näiteks kui maksekuupäev satub riigipühale.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-236">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="8c7ec-237">Dayforce kasutab järgmist teavet.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-237">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="8c7ec-238">Palgatsükkel (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-238">Pay cycle (required)</span></span>
- <span data-ttu-id="8c7ec-239">Palgatsükli sagedus (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-239">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="8c7ec-240">Perioodi alguskuupäev (esimene makseperiood on kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-240">Period start date (first pay period required)</span></span>
- <span data-ttu-id="8c7ec-241">Makse vaikekuupäev (esimene makseperiood on kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-241">Default payment date (first pay period required)</span></span>

<span data-ttu-id="8c7ec-242">See teave on integreeritud rakendusse Dayforce palgagruppidena ja on iga palgatsükli puhul eraldatud riigi või regiooniga.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-242">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="8c7ec-243">Enne integreerimist peab olema loodud vähemalt üks makseperiood.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-243">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="8c7ec-244">Dayforce loob palgagrupi kalendrid ja maksekuupäevad rakenduses Talent määratletud esimese makseperioodi alguskuupäeva ja makse vaikekuupäeva põhjal.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-244">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="8c7ec-245">Tulukoodid</span><span class="sxs-lookup"><span data-stu-id="8c7ec-245">Earning codes</span></span>

<span data-ttu-id="8c7ec-246">Tulukoodid määratlevad kordumatult igat tüüpi tulud, mida töötajad saavad.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-246">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="8c7ec-247">Koodidel on mitmeid tuludega seotud parameetreid, näiteks raamatupidamisreeglid, maksuseadused, aruandluse nõuded ja brutosumma võime.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-247">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="8c7ec-248">Dayforce kasutab järgmist teavet.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="8c7ec-249">Tulukood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-249">Earning Code (required)</span></span>
- <span data-ttu-id="8c7ec-250">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="8c7ec-250">Description</span></span>
- <span data-ttu-id="8c7ec-251">Mõõtühik</span><span class="sxs-lookup"><span data-stu-id="8c7ec-251">Unit of measure</span></span>
- <span data-ttu-id="8c7ec-252">Produktiivne</span><span class="sxs-lookup"><span data-stu-id="8c7ec-252">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="8c7ec-253">Töötaja andmed</span><span class="sxs-lookup"><span data-stu-id="8c7ec-253">Worker data</span></span>

<span data-ttu-id="8c7ec-254">Töötajate kirjed on tähtsad teie personali- ja palgasüsteemide jaoks.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-254">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="8c7ec-255">Teie sisestatud teavet saab kasutada töötajate ja nende isikliku teabe jälgimiseks.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-255">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="8c7ec-256">Töötajate kohta saate hallata järgmist teavet.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-256">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="8c7ec-257">**Üldine** – töötaja põhiteave, näiteks kontaktteave, demograafiline teave, tuvastamisteave, perekonna teave, sõjaväeteenistuse olek, välislähetuse teave ja isiklikud ning lähedase isiku kontaktandmed.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-257">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="8c7ec-258">**Töösuhe** – töötaja töösuhte teave, näiteks töötaja palganud ettevõte või organisatsioon, määratud ametikoht, algus- ja lõppkuupäevad, töökõlblikkus, töölevõtutingimused, pension, puhkus ja ümberpaigutuse teave.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-258">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="8c7ec-259">**Puhkused ja puudumised** – teave töötaja puudumiste kohta, näiteks töögraafikud, puudumiskanded ja puudumise seadistamine.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-259">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="8c7ec-260">**Hüvitus ja palk** – teave töötaja hüvitusplaanide ja palgaarvestuse kohta, näiteks liitutud plaanid, preemiad, tööviljakus, komisjonitasu, maksuteave, pensionileminek ning palgast mahaarvamised.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-260">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="8c7ec-261">Töötaja teabe sisestamisel pidage meeles järgmisi Dayforce’is kasutatavaid andmeid ja konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-261">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="8c7ec-262">Üldteave</span><span class="sxs-lookup"><span data-stu-id="8c7ec-262">General information</span></span>

- <span data-ttu-id="8c7ec-263">Töötaja number (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-263">Personnel number (required)</span></span>
- <span data-ttu-id="8c7ec-264">Eesnimi (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-264">First name (required)</span></span>
- <span data-ttu-id="8c7ec-265">Perekonnanimi (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-265">Last name (required)</span></span>
- <span data-ttu-id="8c7ec-266">Teine eesnimi</span><span class="sxs-lookup"><span data-stu-id="8c7ec-266">Middle name</span></span>
- <span data-ttu-id="8c7ec-267">Staaž kuupäeval</span><span class="sxs-lookup"><span data-stu-id="8c7ec-267">Seniority date</span></span>
- <span data-ttu-id="8c7ec-268">Tuntud kui</span><span class="sxs-lookup"><span data-stu-id="8c7ec-268">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="8c7ec-269">Isikuandmed</span><span class="sxs-lookup"><span data-stu-id="8c7ec-269">Personal information</span></span>

- <span data-ttu-id="8c7ec-270">Perekonnaseis (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-270">Marital status (required)</span></span>
- <span data-ttu-id="8c7ec-271">Sünnikuupäev (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-271">Birth date (required)</span></span>
- <span data-ttu-id="8c7ec-272">Sugu (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-272">Gender (required)</span></span>
- <span data-ttu-id="8c7ec-273">Puudega isik</span><span class="sxs-lookup"><span data-stu-id="8c7ec-273">Person with disabilities</span></span>
- <span data-ttu-id="8c7ec-274">Kodakondsusjärgse riigi regioon (ainult Mehhiko puhul)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-274">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="8c7ec-275">Aadressiteave</span><span class="sxs-lookup"><span data-stu-id="8c7ec-275">Address information</span></span>

- <span data-ttu-id="8c7ec-276">Tänava nimi ja hoone number (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-276">Primary (required)</span></span>
- <span data-ttu-id="8c7ec-277">Riik/regioon (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-277">Country/region (required)</span></span>
- <span data-ttu-id="8c7ec-278">Sihtnumber (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-278">Postal code (required)</span></span>
- <span data-ttu-id="8c7ec-279">Tänava number (kohustuslik) (ainult Mehhiko puhul)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-279">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="8c7ec-280">Hoone tähis (ainult Mehhiko puhul)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-280">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="8c7ec-281">Linn (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-281">City (required)</span></span>
- <span data-ttu-id="8c7ec-282">Osariik (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-282">State (required)</span></span>
- <span data-ttu-id="8c7ec-283">Maakond (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-283">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="8c7ec-284">Kontaktteave</span><span class="sxs-lookup"><span data-stu-id="8c7ec-284">Contact information</span></span> 

- <span data-ttu-id="8c7ec-285">Tänava nimi ja hoone number (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-285">Primary (required)</span></span>
- <span data-ttu-id="8c7ec-286">Kontaktnumber (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-286">Contact number (required)</span></span>
- <span data-ttu-id="8c7ec-287">Sisetelefon</span><span class="sxs-lookup"><span data-stu-id="8c7ec-287">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="8c7ec-288">Palgateave ja tulukoodid</span><span class="sxs-lookup"><span data-stu-id="8c7ec-288">Payroll information and earning codes</span></span>

<span data-ttu-id="8c7ec-289">Töövõtjatele võidakse määrata teatud maksesagedusega konkreetsed tulud ja neil võivad olla eelistatud makseviisid.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-289">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="8c7ec-290">Nende eelistuste ja sätete kasutamise tagamiseks kasutatakse Dayforce’is järgmisi välju.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-290">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="8c7ec-291">Tulukoodid</span><span class="sxs-lookup"><span data-stu-id="8c7ec-291">Earning codes</span></span>

- <span data-ttu-id="8c7ec-292">Ametikoht (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-292">Position (required)</span></span>
- <span data-ttu-id="8c7ec-293">Tulukood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-293">Earning Code (required)</span></span>
- <span data-ttu-id="8c7ec-294">Maksesagedus (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-294">Frequency (required)</span></span>
- <span data-ttu-id="8c7ec-295">Summa (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-295">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="8c7ec-296">Palgateave</span><span class="sxs-lookup"><span data-stu-id="8c7ec-296">Payroll information</span></span>

- <span data-ttu-id="8c7ec-297">Makseviis</span><span class="sxs-lookup"><span data-stu-id="8c7ec-297">Payment Method</span></span>
- <span data-ttu-id="8c7ec-298">Majanduspiirkond (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-298">Economic Region (required)</span></span>
- <span data-ttu-id="8c7ec-299">Töövõtja soodustuste ID</span><span class="sxs-lookup"><span data-stu-id="8c7ec-299">Employee Benefits ID</span></span>
- <span data-ttu-id="8c7ec-300">Riiklik isikukood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-300">National ID Number (required)</span></span>
- <span data-ttu-id="8c7ec-301">Sõjaväeteenistuse number</span><span class="sxs-lookup"><span data-stu-id="8c7ec-301">Military Service Number</span></span>
- <span data-ttu-id="8c7ec-302">Vahetuse ID (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-302">Shift ID (required)</span></span>
- <span data-ttu-id="8c7ec-303">Maksukood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-303">Tax Number (required)</span></span>
- <span data-ttu-id="8c7ec-304">Ühingu ID (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-304">Union ID (required)</span></span>
- <span data-ttu-id="8c7ec-305">Tööpäeva ID (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-305">Work Day ID (required)</span></span>
- <span data-ttu-id="8c7ec-306">Tööloa number</span><span class="sxs-lookup"><span data-stu-id="8c7ec-306">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="8c7ec-307">Mehhiko toetab järgmisi makseviise: **sularaha**, **tšekk** (ettevõtte füüsiline tšekk) ja **elektrooniline makse**.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-307">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="8c7ec-308">Kui makseviisi pole määratud, kasutatakse vaikevalikut **tšekk**.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-308">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="8c7ec-309">Töösuhte üksikasjad</span><span class="sxs-lookup"><span data-stu-id="8c7ec-309">Employment details</span></span>

<span data-ttu-id="8c7ec-310">Töösuhte üksikasjade ajalugu on põhiline teave, millest tuletatakse rakenduses Dayforce töövõtja palkamise, töösuhte lõpetamise ja uuesti palkamise olekud.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-310">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="8c7ec-311">Dayforce toetab korraga ainult ühte aktiivset töösuhte kirjet.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-311">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="8c7ec-312">Töösuhte alguskuupäev (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-312">Employment start date (required)</span></span>
- <span data-ttu-id="8c7ec-313">Töösuhte lõppkuupäev</span><span class="sxs-lookup"><span data-stu-id="8c7ec-313">Employment end date</span></span>
- <span data-ttu-id="8c7ec-314">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="8c7ec-314">Start date</span></span>
- <span data-ttu-id="8c7ec-315">Korrigeeritud alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="8c7ec-315">Adjusted start date</span></span>
- <span data-ttu-id="8c7ec-316">Töösuhte lõpetamise kuupäev (kohustuslik lõpetamisel)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-316">Termination date (required upon termination)</span></span>
- <span data-ttu-id="8c7ec-317">Töösuhte lõpetamise põhjus (kohustuslik lõpetamisel)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-317">Termination reason (required upon termination)</span></span>

<span data-ttu-id="8c7ec-318">Töövõtja tähtsaimad kuupäevad tuletatakse järgmisest teabest.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-318">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="8c7ec-319">Talent</span><span class="sxs-lookup"><span data-stu-id="8c7ec-319">Talent</span></span>                | <span data-ttu-id="8c7ec-320">Dayforce</span><span class="sxs-lookup"><span data-stu-id="8c7ec-320">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c7ec-321">Kõige värskem palkamise kuupäev</span><span class="sxs-lookup"><span data-stu-id="8c7ec-321">Most recent hire date</span></span> | <span data-ttu-id="8c7ec-322">Praeguse lõpetamata töösuhte ajalookirje alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="8c7ec-322">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="8c7ec-323">Lõpetamiskuupäev</span><span class="sxs-lookup"><span data-stu-id="8c7ec-323">Termination date</span></span>      | <span data-ttu-id="8c7ec-324">Praeguse lõpetamata töösuhte ajalookirje lõpetamise kuupäev</span><span class="sxs-lookup"><span data-stu-id="8c7ec-324">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="8c7ec-325">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="8c7ec-325">Start date</span></span>            | <span data-ttu-id="8c7ec-326">Korrigeeritud alguskuupäev, alguskuupäev või praeguse passiivse töösuhte ajalookirje alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="8c7ec-326">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="8c7ec-327">Palkamise algne kuupäev</span><span class="sxs-lookup"><span data-stu-id="8c7ec-327">Original hire date</span></span>    | <span data-ttu-id="8c7ec-328">Varaseima töösuhte ajalookirje alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="8c7ec-328">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="8c7ec-329">Hüvitus</span><span class="sxs-lookup"><span data-stu-id="8c7ec-329">Compensation</span></span>

<span data-ttu-id="8c7ec-330">Tööhõiveperioodi jooksul peab iga töövõtja peamise ametikohaga olema seotud põhipalgaplaan.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-330">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="8c7ec-331">See periood algab kuupäeval, mil töövõtja palgati (või töösuhte alguskuupäeval), ja jätkub kuni töösuhte lõpetamiseni.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-331">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="8c7ec-332">Kehtivuse algus (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-332">Effective Date (required)</span></span>
- <span data-ttu-id="8c7ec-333">Aegumiskuupäev</span><span class="sxs-lookup"><span data-stu-id="8c7ec-333">Expiration date</span></span>
- <span data-ttu-id="8c7ec-334">Palgamäär (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-334">Pay Rate (required)</span></span>
- <span data-ttu-id="8c7ec-335">Palgamäära teisendamised (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-335">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="8c7ec-336">Aastane vaste (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-336">Annual equivalent (required)</span></span>
- <span data-ttu-id="8c7ec-337">Tunnine vaste (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-337">Hourly equivalent (required)</span></span>

<span data-ttu-id="8c7ec-338">Kui tunnimääraga töövõtjal on mitu ametikohta, siis imporditakse peamise ametikoha põhipalk rakendusse Dayforce töövõtja taseme põhimäärana/-palgana.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-338">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="8c7ec-339">Teiseste ametikohtade puhul salvestatakse Dayforce’is tunnimäär vastava ametikoha jaoks.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-339">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="8c7ec-340">Kui kuupalgaga töötajal on mitu ametikohta, siis kasutatakse töövõtja taseme põhimäärana/-palgana kõikide aktiivsete ametikohtade tuletatud kumulatiivset tunnimäära ja aastapalka.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-340">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="8c7ec-341">ID-numbrid</span><span class="sxs-lookup"><span data-stu-id="8c7ec-341">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="8c7ec-342">Isiku identifikaator</span><span class="sxs-lookup"><span data-stu-id="8c7ec-342">Social Security identifier</span></span> 

<span data-ttu-id="8c7ec-343">Igal töövõtjal peab olema üks peamine identifikaator.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-343">Every employee must have one primary identifier.</span></span> <span data-ttu-id="8c7ec-344">Identifikaator peab olema isikukoodi- ehk **SSN**-tüüpi.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-344">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="8c7ec-345">Rakenduses Dayforce tuletatakse see automaatselt töövõtja isiku identifikaatorina, mis on palkamiseks vajalik.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-345">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="8c7ec-346">Peamine isikukood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-346">Primary (required)</span></span>
- <span data-ttu-id="8c7ec-347">ID tüüp = SSN</span><span class="sxs-lookup"><span data-stu-id="8c7ec-347">Identification Type = "SSN"</span></span>
- <span data-ttu-id="8c7ec-348">Väljastamise kuupäev</span><span class="sxs-lookup"><span data-stu-id="8c7ec-348">Issued Date</span></span>
- <span data-ttu-id="8c7ec-349">Aegumiskuupäev</span><span class="sxs-lookup"><span data-stu-id="8c7ec-349">Expiration Date</span></span>

<span data-ttu-id="8c7ec-350">Töövõtjad saavad deklareerida mitu **SSN**-identifitseerimistüüpi ID-numbrit.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-350">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="8c7ec-351">Dayforce’i integreeritakse vaid tähistusega **Peamine** kirje, olenemata sellest, kas number on aktiivne või aegunud.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-351">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="8c7ec-352">Pangakontod ja väljamaksed</span><span class="sxs-lookup"><span data-stu-id="8c7ec-352">Bank accounts and disbursements</span></span>

<span data-ttu-id="8c7ec-353">Iga töötaja jaoks, kes soovib oma palka pangakonto ülekandena kätte saada, tuleb sisestada kehtiv pangakonto teave.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-353">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="8c7ec-354">Talent</span><span class="sxs-lookup"><span data-stu-id="8c7ec-354">Talent</span></span>                         | <span data-ttu-id="8c7ec-355">Dayforce</span><span class="sxs-lookup"><span data-stu-id="8c7ec-355">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8c7ec-356">Pangakonto number (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-356">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="8c7ec-357">SWIFT-kood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-357">SWIFT code (required)</span></span>          | <span data-ttu-id="8c7ec-358">Välja **Panga ID** kasutatakse palgaarvestuse töötlemiseks Mehhikos.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-358">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="8c7ec-359">Filiaali kood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-359">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="8c7ec-360">Pangakonto tüüp (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-360">Bank account type (required)</span></span>   | <span data-ttu-id="8c7ec-361">Välja **Konto tüüp** kasutatakse palgaarvestuse töötlemiseks Mehhikos.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-361">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="8c7ec-362">Toetatud väärtused on **Jooksevkonto** ja **Palgakonto**</span><span class="sxs-lookup"><span data-stu-id="8c7ec-362">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="8c7ec-363">Töövõtjad, kes soovivad oma palka pangakonto ülekannetena kätte saada, peavad esitama lingi jäägikontole, mis on juriidilise isiku alluvuses, kelle peamine aadress on Mehhikos ja kes on seotud Mehhiko panga kehtiva pangakontoga.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-363">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="8c7ec-364">Kõiki ülejäänuid kontosid, mis pole jäägikontod, eiratakse.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-364">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="8c7ec-365">Aadressiteave</span><span class="sxs-lookup"><span data-stu-id="8c7ec-365">Address information</span></span>

<span data-ttu-id="8c7ec-366">Igal töövõtjal peab olema üks peamine asukoht.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-366">Every employee must have one primary location.</span></span> <span data-ttu-id="8c7ec-367">Dayforce’is kasutatakse seda asukohta, et määratleda töövõtja peamine elukoht maksustamise tarbeks.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-367">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="8c7ec-368">Peamine elukoht (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-368">Primary (required)</span></span>
- <span data-ttu-id="8c7ec-369">Riik/regioon (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-369">Country/region (required)</span></span>
- <span data-ttu-id="8c7ec-370">Sihtnumber (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-370">Zip/postal code (required)</span></span>
- <span data-ttu-id="8c7ec-371">Tänava nimi (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-371">Street (required)</span></span>
- <span data-ttu-id="8c7ec-372">Tänava number (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-372">Street Number (required)</span></span>
- <span data-ttu-id="8c7ec-373">Hoone tähis</span><span class="sxs-lookup"><span data-stu-id="8c7ec-373">Building Complement</span></span>
- <span data-ttu-id="8c7ec-374">Linn (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-374">City (required)</span></span>
- <span data-ttu-id="8c7ec-375">Osariik (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-375">State (required)</span></span>
- <span data-ttu-id="8c7ec-376">Maakond (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-376">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="8c7ec-377">Andmete konfigureerimine palgaandmete loomiseks Ameerika Ühendriikides ja Kanadas</span><span class="sxs-lookup"><span data-stu-id="8c7ec-377">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="8c7ec-378">Kui loote palgaandmeid Ameerika Ühendriikide või Kanada töövõtjatele, siis peate konfigureerima järgmisi elemente.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-378">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="8c7ec-379">Ametikohtadele tuleb määrata osakonnad.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-379">Departments are required on positions.</span></span>
- <span data-ttu-id="8c7ec-380">Kulukeskused tuleb määratleda finantsdimensioonideks ja peavad olema vaike-finantsdimensiooni stringi esimene element.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-380">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="8c7ec-381">Töötüübid</span><span class="sxs-lookup"><span data-stu-id="8c7ec-381">Job types</span></span>

<span data-ttu-id="8c7ec-382">Töötüüpe kasutatakse sarnaste tööde kategooriatesse grupeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-382">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="8c7ec-383">Töötüübid on vajalikud palgaarvestuse töötlemiseks Ameerika Ühendriikides ja Kanadas.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-383">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="8c7ec-384">Töötüübid on näiteks täistööaeg ja osaline tööaeg või kuupalk ning tunnipalk.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-384">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="8c7ec-385">Töötüübid vastendatakse Dayforce’i tasutüüpidena, mis näitavad, kas töövõtja on tunni- või palgatöötaja.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-385">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="8c7ec-386">Järgmised töötüübid ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-386">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="8c7ec-387">Töö tüüp</span><span class="sxs-lookup"><span data-stu-id="8c7ec-387">Job type</span></span>   | <span data-ttu-id="8c7ec-388">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="8c7ec-388">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="8c7ec-389">Tunnimäär</span><span class="sxs-lookup"><span data-stu-id="8c7ec-389">Hourly</span></span>     | <span data-ttu-id="8c7ec-390">Tunnimäär</span><span class="sxs-lookup"><span data-stu-id="8c7ec-390">Hourly</span></span>      |
| <span data-ttu-id="8c7ec-391">Põhipalk</span><span class="sxs-lookup"><span data-stu-id="8c7ec-391">Salaried</span></span>   | <span data-ttu-id="8c7ec-392">Põhipalk</span><span class="sxs-lookup"><span data-stu-id="8c7ec-392">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="8c7ec-393">Ametikoha tüübid</span><span class="sxs-lookup"><span data-stu-id="8c7ec-393">Position types</span></span> 

<span data-ttu-id="8c7ec-394">Ametikoha tüüpe kasutatakse selleks, et kirjeldada, kas ametikoht on täiskohaga, osalise tööajaga või midagi muud.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-394">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="8c7ec-395">Ametikoha tüübid vastendatakse Dayforce’i tasuklassidena, mis näitavad, kas töövõtja on täis- või osalise tööajaga töötaja.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-395">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="8c7ec-396">Järgmised ametikoha tüübid ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-396">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="8c7ec-397">Ametikoha tüüp</span><span class="sxs-lookup"><span data-stu-id="8c7ec-397">Position type</span></span>   | <span data-ttu-id="8c7ec-398">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="8c7ec-398">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="8c7ec-399">Täistööaeg</span><span class="sxs-lookup"><span data-stu-id="8c7ec-399">Full-time</span></span>       | <span data-ttu-id="8c7ec-400">Täistööajaga töövõtja</span><span class="sxs-lookup"><span data-stu-id="8c7ec-400">Full time employee</span></span> |
| <span data-ttu-id="8c7ec-401">Osaline tööaeg</span><span class="sxs-lookup"><span data-stu-id="8c7ec-401">Part-time</span></span>       | <span data-ttu-id="8c7ec-402">Osalise tööajaga töövõtja</span><span class="sxs-lookup"><span data-stu-id="8c7ec-402">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="8c7ec-403">Põhjuse koodid</span><span class="sxs-lookup"><span data-stu-id="8c7ec-403">Reason codes</span></span>

<span data-ttu-id="8c7ec-404">Põhjusekoodid annavad teavet töövõtja oleku kohta.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-404">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="8c7ec-405">Põhjusekoodid vastendatakse Dayforce’i olekupõhjustena, mis näitavad töövõtja ametikoha või töösuhte oleku muutuse põhjust.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-405">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="8c7ec-406">Järgmised põhjusekoodid ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-406">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="8c7ec-407">Põhjusekood</span><span class="sxs-lookup"><span data-stu-id="8c7ec-407">Reason code</span></span>    | <span data-ttu-id="8c7ec-408">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="8c7ec-408">Description</span></span>      | <span data-ttu-id="8c7ec-409">Rakendatavad stsenaariumid</span><span class="sxs-lookup"><span data-stu-id="8c7ec-409">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="8c7ec-410">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="8c7ec-410">RESIGNATION</span></span>    | <span data-ttu-id="8c7ec-411">Lahkumine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-411">Resignation</span></span>      | <span data-ttu-id="8c7ec-412">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-412">Terminate worker</span></span>     |
| <span data-ttu-id="8c7ec-413">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="8c7ec-413">TERMINATION</span></span>    | <span data-ttu-id="8c7ec-414">Lõpetamine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-414">Termination</span></span>      | <span data-ttu-id="8c7ec-415">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-415">Terminate worker</span></span>     |
| <span data-ttu-id="8c7ec-416">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="8c7ec-416">RETIREMENT</span></span>     | <span data-ttu-id="8c7ec-417">Pensionile jäämine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-417">Retirement</span></span>       | <span data-ttu-id="8c7ec-418">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-418">Terminate worker</span></span>     |
| <span data-ttu-id="8c7ec-419">OTHER</span><span class="sxs-lookup"><span data-stu-id="8c7ec-419">OTHER</span></span>          | <span data-ttu-id="8c7ec-420">Muud põhjused</span><span class="sxs-lookup"><span data-stu-id="8c7ec-420">Other Reasons</span></span>    | <span data-ttu-id="8c7ec-421">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-421">Terminate worker</span></span>     |
| <span data-ttu-id="8c7ec-422">DEATH</span><span class="sxs-lookup"><span data-stu-id="8c7ec-422">DEATH</span></span>          | <span data-ttu-id="8c7ec-423">Surm</span><span class="sxs-lookup"><span data-stu-id="8c7ec-423">Death</span></span>            | <span data-ttu-id="8c7ec-424">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-424">Terminate worker</span></span>     |
| <span data-ttu-id="8c7ec-425">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="8c7ec-425">LEAVEOFABSENCE</span></span> | <span data-ttu-id="8c7ec-426">Puhkus</span><span class="sxs-lookup"><span data-stu-id="8c7ec-426">Leave of Absence</span></span> | <span data-ttu-id="8c7ec-427">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-427">Terminate worker</span></span>     |
| <span data-ttu-id="8c7ec-428">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="8c7ec-428">CONTRACTEND</span></span>    | <span data-ttu-id="8c7ec-429">Lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-429">End of Contract</span></span>  | <span data-ttu-id="8c7ec-430">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-430">Terminate worker</span></span>     |
| <span data-ttu-id="8c7ec-431">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="8c7ec-431">SALARYCHANGE</span></span>   | <span data-ttu-id="8c7ec-432">Palga muutus</span><span class="sxs-lookup"><span data-stu-id="8c7ec-432">Change of Salary</span></span> | <span data-ttu-id="8c7ec-433">Hüvitus</span><span class="sxs-lookup"><span data-stu-id="8c7ec-433">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="8c7ec-434">Perekonnaseis</span><span class="sxs-lookup"><span data-stu-id="8c7ec-434">Marital status</span></span>

<span data-ttu-id="8c7ec-435">Perekonnaseisu väärtused vastendatakse Dayforce’i ja tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-435">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="8c7ec-436">Järgmine tabel näitab, kuidas perekonnaseisu väärtusi Dayforce’i vastendatakse.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-436">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="8c7ec-437">Talent</span><span class="sxs-lookup"><span data-stu-id="8c7ec-437">Talent</span></span>                 | <span data-ttu-id="8c7ec-438">Dayforce</span><span class="sxs-lookup"><span data-stu-id="8c7ec-438">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="8c7ec-439">Abielus</span><span class="sxs-lookup"><span data-stu-id="8c7ec-439">Married</span></span>                | <span data-ttu-id="8c7ec-440">Abielus</span><span class="sxs-lookup"><span data-stu-id="8c7ec-440">Married</span></span>              |
| <span data-ttu-id="8c7ec-441">Üksik</span><span class="sxs-lookup"><span data-stu-id="8c7ec-441">Single</span></span>                 | <span data-ttu-id="8c7ec-442">Üksik</span><span class="sxs-lookup"><span data-stu-id="8c7ec-442">Single</span></span>               |
| <span data-ttu-id="8c7ec-443">Lesk</span><span class="sxs-lookup"><span data-stu-id="8c7ec-443">Widowed</span></span>                | <span data-ttu-id="8c7ec-444">Lesk</span><span class="sxs-lookup"><span data-stu-id="8c7ec-444">Widowed</span></span>              |
| <span data-ttu-id="8c7ec-445">Lahutatud</span><span class="sxs-lookup"><span data-stu-id="8c7ec-445">Divorced</span></span>               | <span data-ttu-id="8c7ec-446">Lahutatud</span><span class="sxs-lookup"><span data-stu-id="8c7ec-446">Divorced</span></span>             |
| <span data-ttu-id="8c7ec-447">Registreeritud partnerlus</span><span class="sxs-lookup"><span data-stu-id="8c7ec-447">Registered Partnership</span></span> | <span data-ttu-id="8c7ec-448">Mitteabieluline kooselu</span><span class="sxs-lookup"><span data-stu-id="8c7ec-448">Domestic Partnership</span></span> |
| <span data-ttu-id="8c7ec-449">None</span><span class="sxs-lookup"><span data-stu-id="8c7ec-449">None</span></span>                   | <span data-ttu-id="8c7ec-450">None</span><span class="sxs-lookup"><span data-stu-id="8c7ec-450">None</span></span>                 |
| <span data-ttu-id="8c7ec-451">Kooselu</span><span class="sxs-lookup"><span data-stu-id="8c7ec-451">Cohabiting</span></span>             | <span data-ttu-id="8c7ec-452">Kooselu</span><span class="sxs-lookup"><span data-stu-id="8c7ec-452">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="8c7ec-453">Sugu</span><span class="sxs-lookup"><span data-stu-id="8c7ec-453">Gender</span></span>

<span data-ttu-id="8c7ec-454">Soo määratlused vastendatakse Dayforce’i ja tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-454">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="8c7ec-455">Järgmine tabel näitab, kuidas soo määratlusi Dayforce’i vastendatakse.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-455">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="8c7ec-456">Talent</span><span class="sxs-lookup"><span data-stu-id="8c7ec-456">Talent</span></span>       | <span data-ttu-id="8c7ec-457">Dayforce</span><span class="sxs-lookup"><span data-stu-id="8c7ec-457">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="8c7ec-458">Mees</span><span class="sxs-lookup"><span data-stu-id="8c7ec-458">Male</span></span>         | <span data-ttu-id="8c7ec-459">Mees</span><span class="sxs-lookup"><span data-stu-id="8c7ec-459">Male</span></span>            |
| <span data-ttu-id="8c7ec-460">Naine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-460">Female</span></span>       | <span data-ttu-id="8c7ec-461">Naine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-461">Female</span></span>          |
| <span data-ttu-id="8c7ec-462">Mittespetsiifiline</span><span class="sxs-lookup"><span data-stu-id="8c7ec-462">Non-specific</span></span> | <span data-ttu-id="8c7ec-463">*Ei toetata*</span><span class="sxs-lookup"><span data-stu-id="8c7ec-463">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="8c7ec-464">Tulukoodid</span><span class="sxs-lookup"><span data-stu-id="8c7ec-464">Earning codes</span></span>

<span data-ttu-id="8c7ec-465">Tulukoodid määratlevad kordumatult igat tüüpi tulud, mida töötajad saavad.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-465">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="8c7ec-466">Koodid hõlmavad mitmeid tuludega seotud parameetreid, näiteks raamatupidamisreeglid, maksuseadused, aruandluse nõuded ja brutosumma võime.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-466">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="8c7ec-467">Kui kasutatakse toetuseta sagedust, siis kasutatakse arvutamise jaoks vaikimisi sagedust **Iga makse**.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-467">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="8c7ec-468">Toetatud sagedused</span><span class="sxs-lookup"><span data-stu-id="8c7ec-468">Supported frequencies</span></span>

- <span data-ttu-id="8c7ec-469">Kõik</span><span class="sxs-lookup"><span data-stu-id="8c7ec-469">All</span></span>
- <span data-ttu-id="8c7ec-470">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="8c7ec-470">EVERYPAY</span></span>
- <span data-ttu-id="8c7ec-471">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="8c7ec-471">EACHPAYPERIOD</span></span>
- <span data-ttu-id="8c7ec-472">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="8c7ec-472">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="8c7ec-473">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="8c7ec-473">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="8c7ec-474">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="8c7ec-474">1OFMTH</span></span>
- <span data-ttu-id="8c7ec-475">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="8c7ec-475">LASTOFMTH</span></span>
- <span data-ttu-id="8c7ec-476">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="8c7ec-476">2OFMTH</span></span>
- <span data-ttu-id="8c7ec-477">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="8c7ec-477">3OFMTH</span></span>
- <span data-ttu-id="8c7ec-478">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="8c7ec-478">4OFMTH</span></span>
- <span data-ttu-id="8c7ec-479">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="8c7ec-479">5OFMTH</span></span>
- <span data-ttu-id="8c7ec-480">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="8c7ec-480">1N2OFMTH</span></span>
- <span data-ttu-id="8c7ec-481">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="8c7ec-481">3N4OFMTH</span></span>
- <span data-ttu-id="8c7ec-482">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="8c7ec-482">1N3OFMTH</span></span>
- <span data-ttu-id="8c7ec-483">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="8c7ec-483">1N4OFMTH</span></span>
- <span data-ttu-id="8c7ec-484">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="8c7ec-484">2N3OFMTH</span></span>
- <span data-ttu-id="8c7ec-485">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="8c7ec-485">2N4OFMTH</span></span>
- <span data-ttu-id="8c7ec-486">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="8c7ec-486">1N2N3OFMTH</span></span>
- <span data-ttu-id="8c7ec-487">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="8c7ec-487">1N2N4OFMTH</span></span>
- <span data-ttu-id="8c7ec-488">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="8c7ec-488">1N3N4OFMTH</span></span>
- <span data-ttu-id="8c7ec-489">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="8c7ec-489">2N3N4OFMTH</span></span>
- <span data-ttu-id="8c7ec-490">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="8c7ec-490">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="8c7ec-491">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="8c7ec-491">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="8c7ec-492">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="8c7ec-492">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="8c7ec-493">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="8c7ec-493">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="8c7ec-494">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="8c7ec-494">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="8c7ec-495">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="8c7ec-495">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="8c7ec-496">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="8c7ec-496">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="8c7ec-497">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="8c7ec-497">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="8c7ec-498">Aadressid</span><span class="sxs-lookup"><span data-stu-id="8c7ec-498">Addresses</span></span>

<span data-ttu-id="8c7ec-499">Teatud riigi või regiooni, osariigi ja maakonna (haldusüksuse) koodide tuvastamise jaoks on vaja kindlaid vorminguid, mida Dayforce ning riigi-/regioonisisesed pakkujad ära tunnevad.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-499">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="8c7ec-500">Kuigi linnade vorming on paindlik, peab iga linn olema seotud osariigiga.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-500">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="8c7ec-501">Talent</span><span class="sxs-lookup"><span data-stu-id="8c7ec-501">Talent</span></span>          | <span data-ttu-id="8c7ec-502">Dayforce</span><span class="sxs-lookup"><span data-stu-id="8c7ec-502">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="8c7ec-503">Riik/regioon</span><span class="sxs-lookup"><span data-stu-id="8c7ec-503">Country/Region</span></span>  | <span data-ttu-id="8c7ec-504">Riigi kood</span><span class="sxs-lookup"><span data-stu-id="8c7ec-504">Country Code</span></span>          |
| <span data-ttu-id="8c7ec-505">Sihtnumber</span><span class="sxs-lookup"><span data-stu-id="8c7ec-505">Zip/Postal Code</span></span> | <span data-ttu-id="8c7ec-506">Sihtnumber</span><span class="sxs-lookup"><span data-stu-id="8c7ec-506">Postal Code</span></span>           |
| <span data-ttu-id="8c7ec-507">Osariik</span><span class="sxs-lookup"><span data-stu-id="8c7ec-507">State</span></span>           | <span data-ttu-id="8c7ec-508">Osariigi kood</span><span class="sxs-lookup"><span data-stu-id="8c7ec-508">State Code</span></span>            |
| <span data-ttu-id="8c7ec-509">Linn</span><span class="sxs-lookup"><span data-stu-id="8c7ec-509">City</span></span>            | <span data-ttu-id="8c7ec-510">Linn</span><span class="sxs-lookup"><span data-stu-id="8c7ec-510">City</span></span>                  |
| <span data-ttu-id="8c7ec-511">Maakond</span><span class="sxs-lookup"><span data-stu-id="8c7ec-511">County</span></span>          | <span data-ttu-id="8c7ec-512">Maakond (haldusüksus)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-512">County (Municipality)</span></span> |
| <span data-ttu-id="8c7ec-513">Tänav</span><span class="sxs-lookup"><span data-stu-id="8c7ec-513">Street</span></span>          | <span data-ttu-id="8c7ec-514">Aadressirida 1</span><span class="sxs-lookup"><span data-stu-id="8c7ec-514">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="8c7ec-515">Maksuregioonid</span><span class="sxs-lookup"><span data-stu-id="8c7ec-515">Tax regions</span></span>

<span data-ttu-id="8c7ec-516">Maksuregioone kasutatakse palga loomisel sobiva maksu määramiseks.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-516">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="8c7ec-517">Maksuregioonid vastendatakse Dayforce’i asukoha-aadressidena.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-517">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="8c7ec-518">Maksuregiooni vaikevariant peab olema seotud töötaja aktiivse ametikohaga.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-518">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="8c7ec-519">Maksuregioon (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-519">Tax region (required)</span></span>
- <span data-ttu-id="8c7ec-520">Riik/regioon (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-520">Country/Region (required)</span></span>
- <span data-ttu-id="8c7ec-521">Osariik (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-521">State (required)</span></span>
- <span data-ttu-id="8c7ec-522">Maakond</span><span class="sxs-lookup"><span data-stu-id="8c7ec-522">County</span></span> 
- <span data-ttu-id="8c7ec-523">Linn (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-523">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="8c7ec-524">Andmete konfigureerimine palgaandmete loomiseks Mehhikos</span><span class="sxs-lookup"><span data-stu-id="8c7ec-524">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="8c7ec-525">Kui loote palgaandmeid Mehhiko töövõtjatele, siis peate konfigureerima järgmisi elemente.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-525">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="8c7ec-526">Ametikohtadele tuleb määrata osakonnad.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-526">Departments are required on positions.</span></span>
- <span data-ttu-id="8c7ec-527">Kulukeskused tuleb määratleda finantsdimensioonideks ja peavad olema vaike-finantsdimensiooni stringi esimene element.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-527">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="8c7ec-528">Töötüübid</span><span class="sxs-lookup"><span data-stu-id="8c7ec-528">Job types</span></span>

<span data-ttu-id="8c7ec-529">Töötüüpe kasutatakse sarnaste tööde kategooriatesse grupeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-529">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="8c7ec-530">Mehhikos palgaarvestuse töötlemiseks on vajalikud töötüübid.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-530">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="8c7ec-531">Töötüübid on näiteks täistööaeg ja osaline tööaeg või kuupalk ning tunnipalk.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-531">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="8c7ec-532">Töötüübid vastendatakse Dayforce’i tasutüüpidena, mis näitavad, kas töövõtja on tunni- või palgatöötaja.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-532">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="8c7ec-533">Järgmised töötüübid ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-533">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="8c7ec-534">Töö tüüp</span><span class="sxs-lookup"><span data-stu-id="8c7ec-534">Job type</span></span>   | <span data-ttu-id="8c7ec-535">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="8c7ec-535">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="8c7ec-536">Tunnimäär</span><span class="sxs-lookup"><span data-stu-id="8c7ec-536">Hourly</span></span>     | <span data-ttu-id="8c7ec-537">MX tunnimäär</span><span class="sxs-lookup"><span data-stu-id="8c7ec-537">MX Hourly</span></span>   |
| <span data-ttu-id="8c7ec-538">Põhipalk</span><span class="sxs-lookup"><span data-stu-id="8c7ec-538">Salaried</span></span>   | <span data-ttu-id="8c7ec-539">MX põhipalk</span><span class="sxs-lookup"><span data-stu-id="8c7ec-539">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="8c7ec-540">Positsioonitüübid</span><span class="sxs-lookup"><span data-stu-id="8c7ec-540">Position types</span></span> 

<span data-ttu-id="8c7ec-541">Ametikoha tüüpe kasutatakse selleks, et kirjeldada, kas ametikoht on täiskohaga, osalise tööajaga või midagi muud.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-541">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="8c7ec-542">Ametikoha tüübid vastendatakse Dayforce’i tasuklassidena, mis näitavad, kas töövõtja on täis- või osalise tööajaga töötaja.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-542">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="8c7ec-543">Järgmised ametikoha tüübid ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-543">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="8c7ec-544">Ametikoha tüüp</span><span class="sxs-lookup"><span data-stu-id="8c7ec-544">Position type</span></span>   | <span data-ttu-id="8c7ec-545">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="8c7ec-545">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="8c7ec-546">Täistööaeg</span><span class="sxs-lookup"><span data-stu-id="8c7ec-546">Full-time</span></span>       | <span data-ttu-id="8c7ec-547">Täistööajaga töövõtja</span><span class="sxs-lookup"><span data-stu-id="8c7ec-547">Full time employee</span></span> |
| <span data-ttu-id="8c7ec-548">Osaline tööaeg</span><span class="sxs-lookup"><span data-stu-id="8c7ec-548">Part-time</span></span>       | <span data-ttu-id="8c7ec-549">Osalise tööajaga töövõtja</span><span class="sxs-lookup"><span data-stu-id="8c7ec-549">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="8c7ec-550">Põhjuse koodid</span><span class="sxs-lookup"><span data-stu-id="8c7ec-550">Reason codes</span></span>

<span data-ttu-id="8c7ec-551">Põhjusekoodid annavad teavet töövõtja oleku kohta.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-551">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="8c7ec-552">Põhjusekoodid vastendatakse Dayforce’i olekupõhjustena, mis näitavad töövõtja ametikoha või töösuhte oleku muutuse põhjust.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-552">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="8c7ec-553">Järgmised põhjusekoodid ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-553">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="8c7ec-554">Põhjusekood</span><span class="sxs-lookup"><span data-stu-id="8c7ec-554">Reason code</span></span>            | <span data-ttu-id="8c7ec-555">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="8c7ec-555">Description</span></span>                    | <span data-ttu-id="8c7ec-556">Rakendatavad stsenaariumid</span><span class="sxs-lookup"><span data-stu-id="8c7ec-556">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="8c7ec-557">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="8c7ec-557">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="8c7ec-558">Lahkumine enne esimest palgamakset</span><span class="sxs-lookup"><span data-stu-id="8c7ec-558">Departure before first payroll</span></span> | <span data-ttu-id="8c7ec-559">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-559">Terminate worker</span></span>     |
| <span data-ttu-id="8c7ec-560">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="8c7ec-560">RESIGNATION</span></span>            | <span data-ttu-id="8c7ec-561">Lahkumine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-561">Resignation</span></span>                    | <span data-ttu-id="8c7ec-562">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-562">Terminate worker</span></span>     |
| <span data-ttu-id="8c7ec-563">PENSION</span><span class="sxs-lookup"><span data-stu-id="8c7ec-563">PENSION</span></span>                | <span data-ttu-id="8c7ec-564">Pension</span><span class="sxs-lookup"><span data-stu-id="8c7ec-564">Pension</span></span>                        | <span data-ttu-id="8c7ec-565">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-565">Terminate worker</span></span>     |
| <span data-ttu-id="8c7ec-566">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="8c7ec-566">TERMINATION</span></span>            | <span data-ttu-id="8c7ec-567">Lõpetamine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-567">Termination</span></span>                    | <span data-ttu-id="8c7ec-568">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-568">Terminate worker</span></span>     |
| <span data-ttu-id="8c7ec-569">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="8c7ec-569">RETIREMENT</span></span>             | <span data-ttu-id="8c7ec-570">Pensionile jäämine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-570">Retirement</span></span>                     | <span data-ttu-id="8c7ec-571">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-571">Terminate worker</span></span>     |
| <span data-ttu-id="8c7ec-572">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="8c7ec-572">ABSENTEE</span></span>               | <span data-ttu-id="8c7ec-573">Puuduja</span><span class="sxs-lookup"><span data-stu-id="8c7ec-573">Absentee</span></span>                       | <span data-ttu-id="8c7ec-574">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-574">Terminate worker</span></span>     |
| <span data-ttu-id="8c7ec-575">OTHER</span><span class="sxs-lookup"><span data-stu-id="8c7ec-575">OTHER</span></span>                  | <span data-ttu-id="8c7ec-576">Muud põhjused</span><span class="sxs-lookup"><span data-stu-id="8c7ec-576">Other Reasons</span></span>                  | <span data-ttu-id="8c7ec-577">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-577">Terminate worker</span></span>     |
| <span data-ttu-id="8c7ec-578">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="8c7ec-578">CLOSURE</span></span>                | <span data-ttu-id="8c7ec-579">Ettevõte suletud</span><span class="sxs-lookup"><span data-stu-id="8c7ec-579">Business Closure</span></span>               | <span data-ttu-id="8c7ec-580">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-580">Terminate worker</span></span>     |
| <span data-ttu-id="8c7ec-581">DEATH</span><span class="sxs-lookup"><span data-stu-id="8c7ec-581">DEATH</span></span>                  | <span data-ttu-id="8c7ec-582">Surm</span><span class="sxs-lookup"><span data-stu-id="8c7ec-582">Death</span></span>                          | <span data-ttu-id="8c7ec-583">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-583">Terminate worker</span></span>     |
| <span data-ttu-id="8c7ec-584">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="8c7ec-584">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="8c7ec-585">Puhkus</span><span class="sxs-lookup"><span data-stu-id="8c7ec-585">Leave of Absence</span></span>               | <span data-ttu-id="8c7ec-586">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-586">Terminate worker</span></span>     |
| <span data-ttu-id="8c7ec-587">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="8c7ec-587">CONTRACTEND</span></span>            | <span data-ttu-id="8c7ec-588">Lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-588">End of Contract</span></span>                | <span data-ttu-id="8c7ec-589">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-589">Terminate worker</span></span>     |
| <span data-ttu-id="8c7ec-590">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="8c7ec-590">SALARYCHANGE</span></span>           | <span data-ttu-id="8c7ec-591">Palga muutus</span><span class="sxs-lookup"><span data-stu-id="8c7ec-591">Change of Salary</span></span>               | <span data-ttu-id="8c7ec-592">Hüvitus</span><span class="sxs-lookup"><span data-stu-id="8c7ec-592">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="8c7ec-593">Töösuhte tingimused</span><span class="sxs-lookup"><span data-stu-id="8c7ec-593">Terms of employment</span></span>

<span data-ttu-id="8c7ec-594">Töösuhte tingimusi kasutatakse töösuhte tingimuste kategooriate loomiseks.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-594">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="8c7ec-595">Tingimused vastendatakse Dayforce’i töösuhte indikaatorväärtustena.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-595">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="8c7ec-596">Järgmised töösuhte tingimused ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-596">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="8c7ec-597">Töösuhte tingimused</span><span class="sxs-lookup"><span data-stu-id="8c7ec-597">Terms of employment</span></span>   | <span data-ttu-id="8c7ec-598">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="8c7ec-598">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="8c7ec-599">Tavaline</span><span class="sxs-lookup"><span data-stu-id="8c7ec-599">Regular</span></span>               | <span data-ttu-id="8c7ec-600">Tavaline</span><span class="sxs-lookup"><span data-stu-id="8c7ec-600">Regular</span></span>     |
| <span data-ttu-id="8c7ec-601">Otse</span><span class="sxs-lookup"><span data-stu-id="8c7ec-601">Direct</span></span>                | <span data-ttu-id="8c7ec-602">Otse</span><span class="sxs-lookup"><span data-stu-id="8c7ec-602">Direct</span></span>      |
| <span data-ttu-id="8c7ec-603">Praktika</span><span class="sxs-lookup"><span data-stu-id="8c7ec-603">Internship</span></span>            | <span data-ttu-id="8c7ec-604">Praktika</span><span class="sxs-lookup"><span data-stu-id="8c7ec-604">Internship</span></span>  |
| <span data-ttu-id="8c7ec-605">Alaline</span><span class="sxs-lookup"><span data-stu-id="8c7ec-605">Permanent</span></span>             | <span data-ttu-id="8c7ec-606">Alaline</span><span class="sxs-lookup"><span data-stu-id="8c7ec-606">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="8c7ec-607">Perekonnaseis</span><span class="sxs-lookup"><span data-stu-id="8c7ec-607">Marital status</span></span>

<span data-ttu-id="8c7ec-608">Perekonnaseisu väärtused vastendatakse Dayforce’i ja tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-608">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="8c7ec-609">Järgmine tabel näitab, kuidas perekonnaseisu väärtusi Dayforce’i vastendatakse.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-609">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="8c7ec-610">Talent</span><span class="sxs-lookup"><span data-stu-id="8c7ec-610">Talent</span></span>                 | <span data-ttu-id="8c7ec-611">Dayforce</span><span class="sxs-lookup"><span data-stu-id="8c7ec-611">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="8c7ec-612">Abielus</span><span class="sxs-lookup"><span data-stu-id="8c7ec-612">Married</span></span>                | <span data-ttu-id="8c7ec-613">Abielus</span><span class="sxs-lookup"><span data-stu-id="8c7ec-613">Married</span></span>                   |
| <span data-ttu-id="8c7ec-614">Üksik</span><span class="sxs-lookup"><span data-stu-id="8c7ec-614">Single</span></span>                 | <span data-ttu-id="8c7ec-615">Üksik</span><span class="sxs-lookup"><span data-stu-id="8c7ec-615">Single</span></span>                    |
| <span data-ttu-id="8c7ec-616">Lesk</span><span class="sxs-lookup"><span data-stu-id="8c7ec-616">Widowed</span></span>                | <span data-ttu-id="8c7ec-617">Lesk</span><span class="sxs-lookup"><span data-stu-id="8c7ec-617">Widowed</span></span>                   |
| <span data-ttu-id="8c7ec-618">Lahutatud</span><span class="sxs-lookup"><span data-stu-id="8c7ec-618">Divorced</span></span>               | <span data-ttu-id="8c7ec-619">Lahutatud</span><span class="sxs-lookup"><span data-stu-id="8c7ec-619">Divorced</span></span>                  |
| <span data-ttu-id="8c7ec-620">Registreeritud partnerlus</span><span class="sxs-lookup"><span data-stu-id="8c7ec-620">Registered Partnership</span></span> | <span data-ttu-id="8c7ec-621">Mitteabieluline kooselu</span><span class="sxs-lookup"><span data-stu-id="8c7ec-621">Domestic Partnership</span></span>      |
| <span data-ttu-id="8c7ec-622">None</span><span class="sxs-lookup"><span data-stu-id="8c7ec-622">None</span></span>                   | <span data-ttu-id="8c7ec-623">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="8c7ec-623">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="8c7ec-624">Kooselu</span><span class="sxs-lookup"><span data-stu-id="8c7ec-624">Cohabiting</span></span>             | <span data-ttu-id="8c7ec-625">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="8c7ec-625">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="8c7ec-626">Sugu</span><span class="sxs-lookup"><span data-stu-id="8c7ec-626">Gender</span></span>

<span data-ttu-id="8c7ec-627">Soo määratlused vastendatakse Dayforce’i ja tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-627">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="8c7ec-628">Järgmine tabel näitab, kuidas soo määratlusi Dayforce’i vastendatakse.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-628">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="8c7ec-629">Talent</span><span class="sxs-lookup"><span data-stu-id="8c7ec-629">Talent</span></span>       | <span data-ttu-id="8c7ec-630">Dayforce</span><span class="sxs-lookup"><span data-stu-id="8c7ec-630">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="8c7ec-631">Mees</span><span class="sxs-lookup"><span data-stu-id="8c7ec-631">Male</span></span>         | <span data-ttu-id="8c7ec-632">Mees</span><span class="sxs-lookup"><span data-stu-id="8c7ec-632">Male</span></span>                      |
| <span data-ttu-id="8c7ec-633">Naine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-633">Female</span></span>       | <span data-ttu-id="8c7ec-634">Naine</span><span class="sxs-lookup"><span data-stu-id="8c7ec-634">Female</span></span>                    |
| <span data-ttu-id="8c7ec-635">Mittespetsiifiline</span><span class="sxs-lookup"><span data-stu-id="8c7ec-635">Non-specific</span></span> | <span data-ttu-id="8c7ec-636">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="8c7ec-636">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="8c7ec-637">Makseviis</span><span class="sxs-lookup"><span data-stu-id="8c7ec-637">Payment method</span></span>

<span data-ttu-id="8c7ec-638">Makseviisid võimaldavad töövõtjal ja ettevõttel kirjeldada, kuidas töövõtjatele makstakse.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-638">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="8c7ec-639">Makseviisid vastendatakse Dayforce’i ja tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-639">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="8c7ec-640">Järgmine tabel näitab, kuidas makseviise Dayforce’i vastendatakse.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-640">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="8c7ec-641">Talent</span><span class="sxs-lookup"><span data-stu-id="8c7ec-641">Talent</span></span>             | <span data-ttu-id="8c7ec-642">Dayforce</span><span class="sxs-lookup"><span data-stu-id="8c7ec-642">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="8c7ec-643">Sularaha</span><span class="sxs-lookup"><span data-stu-id="8c7ec-643">Cash</span></span>               | <span data-ttu-id="8c7ec-644">Sularaha</span><span class="sxs-lookup"><span data-stu-id="8c7ec-644">Cash</span></span>                      |
| <span data-ttu-id="8c7ec-645">Elektrooniline makse</span><span class="sxs-lookup"><span data-stu-id="8c7ec-645">Electronic Payment</span></span> | <span data-ttu-id="8c7ec-646">Ülekanne</span><span class="sxs-lookup"><span data-stu-id="8c7ec-646">Transfer</span></span>                  |
| <span data-ttu-id="8c7ec-647">Kontrolli</span><span class="sxs-lookup"><span data-stu-id="8c7ec-647">Check</span></span>              | <span data-ttu-id="8c7ec-648">Tšekk</span><span class="sxs-lookup"><span data-stu-id="8c7ec-648">Cheque</span></span>                    |
| <span data-ttu-id="8c7ec-649">Pangaveksel</span><span class="sxs-lookup"><span data-stu-id="8c7ec-649">Bank Draft</span></span>         | <span data-ttu-id="8c7ec-650">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="8c7ec-650">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="8c7ec-651">Muud</span><span class="sxs-lookup"><span data-stu-id="8c7ec-651">Other</span></span>              | <span data-ttu-id="8c7ec-652">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="8c7ec-652">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="8c7ec-653">Pangakonto tüüp</span><span class="sxs-lookup"><span data-stu-id="8c7ec-653">Bank account type</span></span>

<span data-ttu-id="8c7ec-654">Pangakonto tüüpe kasutatakse elektrooniliste maksete tegemiseks töötajatele.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-654">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="8c7ec-655">Pangakonto tüübid vastendatakse Dayforce’i ülekandekonto teabena.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-655">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="8c7ec-656">Pangakonto tüübid tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-656">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="8c7ec-657">Talent</span><span class="sxs-lookup"><span data-stu-id="8c7ec-657">Talent</span></span>            | <span data-ttu-id="8c7ec-658">Dayforce</span><span class="sxs-lookup"><span data-stu-id="8c7ec-658">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="8c7ec-659">Jooksevkonto</span><span class="sxs-lookup"><span data-stu-id="8c7ec-659">Checking Account</span></span>  | <span data-ttu-id="8c7ec-660">Jooksevkonto</span><span class="sxs-lookup"><span data-stu-id="8c7ec-660">CheckingAccount</span></span>           |
| <span data-ttu-id="8c7ec-661">Palgakonto</span><span class="sxs-lookup"><span data-stu-id="8c7ec-661">Payroll Account</span></span>   | <span data-ttu-id="8c7ec-662">Palgakonto</span><span class="sxs-lookup"><span data-stu-id="8c7ec-662">PayrollAccount</span></span>            |
| <span data-ttu-id="8c7ec-663">Hoiukonto</span><span class="sxs-lookup"><span data-stu-id="8c7ec-663">Savings Account</span></span>   | <span data-ttu-id="8c7ec-664">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="8c7ec-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="8c7ec-665">BankGiroti konto</span><span class="sxs-lookup"><span data-stu-id="8c7ec-665">BankGirot account</span></span> | <span data-ttu-id="8c7ec-666">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="8c7ec-666">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="8c7ec-667">PlusGiroti konto</span><span class="sxs-lookup"><span data-stu-id="8c7ec-667">PlusGirot account</span></span> | <span data-ttu-id="8c7ec-668">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="8c7ec-668">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="8c7ec-669">Tulukoodid</span><span class="sxs-lookup"><span data-stu-id="8c7ec-669">Earning codes</span></span>

<span data-ttu-id="8c7ec-670">Tulukoodid määratlevad kordumatult igat tüüpi tulud, mida töötajad saavad.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-670">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="8c7ec-671">Koodid hõlmavad mitmeid tuludega seotud parameetreid, näiteks raamatupidamisreeglid, maksuseadused, aruandluse nõuded ja brutosumma võime.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-671">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="8c7ec-672">Kui kasutatakse toetuseta sagedust, siis kasutatakse arvutamise jaoks vaikimisi sagedust **Iga makse**.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-672">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="8c7ec-673">Toetatud sagedused</span><span class="sxs-lookup"><span data-stu-id="8c7ec-673">Supported frequencies</span></span>

- <span data-ttu-id="8c7ec-674">Kõik</span><span class="sxs-lookup"><span data-stu-id="8c7ec-674">All</span></span>
- <span data-ttu-id="8c7ec-675">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="8c7ec-675">EVERYPAY</span></span>
- <span data-ttu-id="8c7ec-676">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="8c7ec-676">EACHPAYPERIOD</span></span>
- <span data-ttu-id="8c7ec-677">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="8c7ec-677">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="8c7ec-678">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="8c7ec-678">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="8c7ec-679">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="8c7ec-679">1OFMTH</span></span>
- <span data-ttu-id="8c7ec-680">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="8c7ec-680">LASTOFMTH</span></span>
- <span data-ttu-id="8c7ec-681">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="8c7ec-681">2OFMTH</span></span>
- <span data-ttu-id="8c7ec-682">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="8c7ec-682">3OFMTH</span></span>
- <span data-ttu-id="8c7ec-683">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="8c7ec-683">4OFMTH</span></span>
- <span data-ttu-id="8c7ec-684">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="8c7ec-684">5OFMTH</span></span>
- <span data-ttu-id="8c7ec-685">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="8c7ec-685">1N2OFMTH</span></span>
- <span data-ttu-id="8c7ec-686">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="8c7ec-686">3N4OFMTH</span></span>
- <span data-ttu-id="8c7ec-687">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="8c7ec-687">1N3OFMTH</span></span>
- <span data-ttu-id="8c7ec-688">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="8c7ec-688">1N4OFMTH</span></span>
- <span data-ttu-id="8c7ec-689">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="8c7ec-689">2N3OFMTH</span></span>
- <span data-ttu-id="8c7ec-690">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="8c7ec-690">2N4OFMTH</span></span>
- <span data-ttu-id="8c7ec-691">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="8c7ec-691">1N2N3OFMTH</span></span>
- <span data-ttu-id="8c7ec-692">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="8c7ec-692">1N2N4OFMTH</span></span>
- <span data-ttu-id="8c7ec-693">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="8c7ec-693">1N3N4OFMTH</span></span>
- <span data-ttu-id="8c7ec-694">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="8c7ec-694">2N3N4OFMTH</span></span>
- <span data-ttu-id="8c7ec-695">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="8c7ec-695">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="8c7ec-696">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="8c7ec-696">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="8c7ec-697">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="8c7ec-697">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="8c7ec-698">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="8c7ec-698">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="8c7ec-699">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="8c7ec-699">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="8c7ec-700">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="8c7ec-700">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="8c7ec-701">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="8c7ec-701">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="8c7ec-702">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="8c7ec-702">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="8c7ec-703">Aadressid</span><span class="sxs-lookup"><span data-stu-id="8c7ec-703">Addresses</span></span>

<span data-ttu-id="8c7ec-704">Teatud riigi või regiooni, osariigi ja maakonna (haldusüksuse) koodide tuvastamise jaoks on vaja kindlaid vorminguid, mida Dayforce ning riigi-/regioonisisesed pakkujad ära tunnevad.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-704">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="8c7ec-705">Kuigi linnade vorming on paindlik, peab iga linn olema seotud osariigiga.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-705">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="8c7ec-706">Talent</span><span class="sxs-lookup"><span data-stu-id="8c7ec-706">Talent</span></span>              | <span data-ttu-id="8c7ec-707">Dayforce</span><span class="sxs-lookup"><span data-stu-id="8c7ec-707">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="8c7ec-708">Riik/regioon</span><span class="sxs-lookup"><span data-stu-id="8c7ec-708">Country/Region</span></span>      | <span data-ttu-id="8c7ec-709">Riigi kood</span><span class="sxs-lookup"><span data-stu-id="8c7ec-709">Country Code</span></span>          |
| <span data-ttu-id="8c7ec-710">Sihtnumber</span><span class="sxs-lookup"><span data-stu-id="8c7ec-710">Zip/Postal Code</span></span>     | <span data-ttu-id="8c7ec-711">Sihtnumber</span><span class="sxs-lookup"><span data-stu-id="8c7ec-711">Postal Code</span></span>           |
| <span data-ttu-id="8c7ec-712">Osariik</span><span class="sxs-lookup"><span data-stu-id="8c7ec-712">State</span></span>               | <span data-ttu-id="8c7ec-713">Osariigi kood</span><span class="sxs-lookup"><span data-stu-id="8c7ec-713">State Code</span></span>            |
| <span data-ttu-id="8c7ec-714">Linn</span><span class="sxs-lookup"><span data-stu-id="8c7ec-714">City</span></span>                | <span data-ttu-id="8c7ec-715">Linn</span><span class="sxs-lookup"><span data-stu-id="8c7ec-715">City</span></span>                  |
| <span data-ttu-id="8c7ec-716">Maakond</span><span class="sxs-lookup"><span data-stu-id="8c7ec-716">County</span></span>              | <span data-ttu-id="8c7ec-717">Maakond (haldusüksus)</span><span class="sxs-lookup"><span data-stu-id="8c7ec-717">County (Municipality)</span></span> |
| <span data-ttu-id="8c7ec-718">Tänav</span><span class="sxs-lookup"><span data-stu-id="8c7ec-718">Street</span></span>              | <span data-ttu-id="8c7ec-719">Aadressirida 1</span><span class="sxs-lookup"><span data-stu-id="8c7ec-719">Address Line 1</span></span>        |
| <span data-ttu-id="8c7ec-720">Majanumber</span><span class="sxs-lookup"><span data-stu-id="8c7ec-720">Street Number</span></span>       | <span data-ttu-id="8c7ec-721">Aadressirida 2</span><span class="sxs-lookup"><span data-stu-id="8c7ec-721">Address Line 2</span></span>        |
| <span data-ttu-id="8c7ec-722">Hoone tähis</span><span class="sxs-lookup"><span data-stu-id="8c7ec-722">Building Complement</span></span> | <span data-ttu-id="8c7ec-723">Aadressirida 5</span><span class="sxs-lookup"><span data-stu-id="8c7ec-723">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="8c7ec-724">Passi number</span><span class="sxs-lookup"><span data-stu-id="8c7ec-724">Passport number</span></span>

<span data-ttu-id="8c7ec-725">Töötajad saavad deklareerida passi teavet.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-725">Employees can declare passport information.</span></span> <span data-ttu-id="8c7ec-726">See teave on identifitseerimistüüpi **Pass** ja integreeritakse Dayforce’i töövõtja Mehhiko-teabe osana.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-726">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="8c7ec-727">Identifitseerimistüüp = pass</span><span class="sxs-lookup"><span data-stu-id="8c7ec-727">Identification Type = "Passport"</span></span>
- <span data-ttu-id="8c7ec-728">Väljastamise kuupäev</span><span class="sxs-lookup"><span data-stu-id="8c7ec-728">Issued Date</span></span>
- <span data-ttu-id="8c7ec-729">Aegumiskuupäev</span><span class="sxs-lookup"><span data-stu-id="8c7ec-729">Expiration Date</span></span>

<span data-ttu-id="8c7ec-730">Töövõtjad saavad deklareerida mitu **Pass**-identifitseerimistüüpi ID-numbrit.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-730">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="8c7ec-731">Dayforce’i integreeritakse siiski ainult praegune aktiivne passikirje.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-731">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="8c7ec-732">Kui kõik passikirjed on aegunud, siis integreeritakse Dayforce’i pass, mis väljastati viimasena.</span><span class="sxs-lookup"><span data-stu-id="8c7ec-732">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
