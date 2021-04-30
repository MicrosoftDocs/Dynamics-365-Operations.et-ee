---
title: Dayforce’iga integreerimise konfigureerimine
description: Rakenduste Microsoft Dynamics 365 Human Resources ja Ceridian Dayforce vaheline integratsioon oleneb mitmest selles teemas kirjeldatavast konfiguratsioonietapist. Enne palgatöötluse tegemist peate konfigureerima integratsiooni nii rakenduses Human Resources kui ka Dayforce.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PersonnelIntegrationConfiguration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1647b7fbf84a78051e745e918954df32a2e7e1dd
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890000"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="63ca9-104">Dayforce’iga integreerimise konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="63ca9-104">Configure integration with Dayforce</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="63ca9-105">Rakenduste Microsoft Dynamics 365 Human Resources ja Ceridian Dayforce vaheline integratsioon oleneb mitmest selles teemas kirjeldatavast konfiguratsioonietapist.</span><span class="sxs-lookup"><span data-stu-id="63ca9-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="63ca9-106">Enne palgatöötluse tegemist peate konfigureerima integratsiooni nii rakenduses Human Resources kui ka Dayforce.</span><span class="sxs-lookup"><span data-stu-id="63ca9-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="63ca9-107">Kui te kasutate palgatöötluste tegemiseks teenust, nagu Dayforce, siis peate rakenduses Human Resources integratsiooni lubama.</span><span class="sxs-lookup"><span data-stu-id="63ca9-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="63ca9-108">Integratsiooni jaoks on rakendusest Human Resources vaja teatud andmeid.</span><span class="sxs-lookup"><span data-stu-id="63ca9-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="63ca9-109">Seega peate kinnitama, et Dayforce’iga vastendatud andmed on rakenduses Human Resources konfigureeritud viisil, mis lubab integratsiooni.</span><span class="sxs-lookup"><span data-stu-id="63ca9-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="63ca9-110">Integratsioon kasutab järgmisi üldisi andmekategooriaid.</span><span class="sxs-lookup"><span data-stu-id="63ca9-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="63ca9-111">Inimressursside andmed</span><span class="sxs-lookup"><span data-stu-id="63ca9-111">Human resources data</span></span>
- <span data-ttu-id="63ca9-112">Hüvituse andmed</span><span class="sxs-lookup"><span data-stu-id="63ca9-112">Compensation data</span></span>
- <span data-ttu-id="63ca9-113">Palgaandmed, näiteks palgatsüklid, makseperioodid ja tulukoodid</span><span class="sxs-lookup"><span data-stu-id="63ca9-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="63ca9-114">Töötaja andmed</span><span class="sxs-lookup"><span data-stu-id="63ca9-114">Worker data</span></span>

<span data-ttu-id="63ca9-115">Teemas kirjeldatakse integratsiooni lubamiseks vajalikke etappe.</span><span class="sxs-lookup"><span data-stu-id="63ca9-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="63ca9-116">Samuti selgitatakse integratsiooni jaoks vajalikke andmetüüpe ja konfigureerimise üksikasju.</span><span class="sxs-lookup"><span data-stu-id="63ca9-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="63ca9-117">Integratsiooni lubamine</span><span class="sxs-lookup"><span data-stu-id="63ca9-117">Enable the integration</span></span>

<span data-ttu-id="63ca9-118">Dayforce’iga ühendamiseks peate rakenduses Human Resources sisse lülitama integratsiooni ja sisestama konfigureerimisteabe.</span><span class="sxs-lookup"><span data-stu-id="63ca9-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="63ca9-119">Kui soovite, et loodav pearaamatu kanne imporditaks rakendusse Microsoft Dynamics 365 Finance, siis peate seadistama Microsoft Azure’i salvestuskonto ja sisestama Azure’i salvestusruumi ühendusstringi rakendusse Finance.</span><span class="sxs-lookup"><span data-stu-id="63ca9-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="63ca9-120">Integratsiooni sisselülitamiseks rakenduses Human Resources järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="63ca9-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="63ca9-121">Valige lehelt **Süsteemihaldus** suvand **Integratsiooni konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="63ca9-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="63ca9-122">Sisestage turvalise failiedastusprotokolli File Transfer Protocol (FTP) lõpp-punkt ja turvalise FTP kausta tee.</span><span class="sxs-lookup"><span data-stu-id="63ca9-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="63ca9-123">Sisestage selle kasutaja kasutajanimi ja parool, kellel on vaja juurdepääsu turvalise FTP lõpp-punktile ja kausta teele.</span><span class="sxs-lookup"><span data-stu-id="63ca9-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="63ca9-124">Testige ühendust vajaduse järgi ja määrake suvand **Palgaarvestuse integratsiooni lubamine** olekule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="63ca9-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="63ca9-125">Kui integratsioon on sisse lülitatud, luuakse andmete ekspordipakett ja -failid ning määratakse sagedus.</span><span class="sxs-lookup"><span data-stu-id="63ca9-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="63ca9-126">Vajaduse korral saate seda sagedust muuta.</span><span class="sxs-lookup"><span data-stu-id="63ca9-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="63ca9-127">Lisateavet Azure’i talletamiskontode ja Azure’i salvestusruumi ühendusstringide kohta leiate järgmistest Azure’i teemadest.</span><span class="sxs-lookup"><span data-stu-id="63ca9-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="63ca9-128">Azure’i salvestuskontod</span><span class="sxs-lookup"><span data-stu-id="63ca9-128">About Azure storage accounts</span></span>](/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="63ca9-129">Azure’i salvestusruumi ühendusstringide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="63ca9-129">Configure Azure Storage connection strings</span></span>](/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="63ca9-130">Tehnilised üksikasjad, kui palga integratsioon on lubatud</span><span class="sxs-lookup"><span data-stu-id="63ca9-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="63ca9-131">Palga integreerimise sisselülitamisel on kaks peamist mõju.</span><span class="sxs-lookup"><span data-stu-id="63ca9-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="63ca9-132">Luuakse andmete ekspordi projekt nimega "Palga integreerimise eksport".</span><span class="sxs-lookup"><span data-stu-id="63ca9-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="63ca9-133">See projekt sisaldab palga integreerimise jaoks nõutavaid üksusi ja välju.</span><span class="sxs-lookup"><span data-stu-id="63ca9-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="63ca9-134">Projekti uurimiseks avage **Süsteemihaldus**, valige paan **Andmehaldus** ja avage projektiloendist andmete projekt.</span><span class="sxs-lookup"><span data-stu-id="63ca9-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="63ca9-135">See pakett-töö käivitab andmete eksportimise projekti, krüptib tulemuste andmete paketi ja edastab andmete paketi faili SFTP-lõpp-punktile, mis on konfigureeritud kuval **integratsiooni konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="63ca9-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="63ca9-136">SFTP-lõpp-punkti edastatud andmete pakett krüptitakse, kasutades võtit, mis on paketile kordumatu.</span><span class="sxs-lookup"><span data-stu-id="63ca9-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="63ca9-137">Võti on Azure võtmehoidlas, mis on kättesaadav ainult Ceridianile.</span><span class="sxs-lookup"><span data-stu-id="63ca9-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="63ca9-138">Andmebaasi sisu ei saa dekrüptida ja uurida.</span><span class="sxs-lookup"><span data-stu-id="63ca9-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="63ca9-139">Kui teil on vaja uurida andmepaketi sisu, peate eksportima projekti "Palga integreerimise eksport" käsitsi, selle alla laadima ja seejärel avama.</span><span class="sxs-lookup"><span data-stu-id="63ca9-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="63ca9-140">Käsitsi eksportimine ei rakenda krüptimist ega edasta paketti.</span><span class="sxs-lookup"><span data-stu-id="63ca9-140">Manual export will not apply encryption or transfer the package.</span></span>
> <span data-ttu-id="63ca9-141">Kui integratsioonifailid saadetakse Dynamics 365 Human Resources UAT- või liivakastikeskkonnast Ceridian Dayforce'i testkeskkonda, saate kasutada järgmist võtmehoidla URL-i: https://payrollintegrationprod.vault.azure.net.</span><span class="sxs-lookup"><span data-stu-id="63ca9-141">For instances where the integration files are sent from a Dynamics 365 Human Resources UAT or Sandbox environment to a Ceridian Dayforce Test environment, you can use the following key vault URL: https://payrollintegrationprod.vault.azure.net.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="63ca9-142">Andmete konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="63ca9-142">Configure your data</span></span> 

<span data-ttu-id="63ca9-143">Palgaarvestuse töötlemiseks peate konfigureerima personaliandmeid rakenduses Human Resources.</span><span class="sxs-lookup"><span data-stu-id="63ca9-143">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="63ca9-144">Peate määratlema organisatsiooni andmeid nagu tööd ja ametikohad, samuti teavet soodustuste ning kompensatsioonide kohta.</span><span class="sxs-lookup"><span data-stu-id="63ca9-144">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="63ca9-145">Selle teabe hulka kuulub töövõtja palgaandmete loomiseks vajalik teave töösuhte, palga ja mahaarvamiste kohta.</span><span class="sxs-lookup"><span data-stu-id="63ca9-145">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="63ca9-146">Personaliandmed</span><span class="sxs-lookup"><span data-stu-id="63ca9-146">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="63ca9-147">Soodustused</span><span class="sxs-lookup"><span data-stu-id="63ca9-147">Benefits</span></span> 

<span data-ttu-id="63ca9-148">Inimressursid pakuvad tööriistu, mis aitavad seadistada ja hallata soodustusi, mahaarvamisi ning töötajate hüvitusplaane, mida organisatsioon oma töötajatele pakub või nende puhul töötleb.</span><span class="sxs-lookup"><span data-stu-id="63ca9-148">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="63ca9-149">Soodustuste loomisel pidage meeles järgmisi Dayforce’is kasutatavaid andmeid ja konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="63ca9-149">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="63ca9-150">Soodustusplaanid</span><span class="sxs-lookup"><span data-stu-id="63ca9-150">Benefit plans</span></span>

- <span data-ttu-id="63ca9-151">Plaan (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-151">Plan (required)</span></span>
- <span data-ttu-id="63ca9-152">Tüüp (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-152">Type (required)</span></span>
- <span data-ttu-id="63ca9-153">Palga mõju (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-153">Payroll impact (required)</span></span>
- <span data-ttu-id="63ca9-154">Võlgnevuste sissenõudmine</span><span class="sxs-lookup"><span data-stu-id="63ca9-154">Recover arrears</span></span>
- <span data-ttu-id="63ca9-155">Mahaarvamismeetod</span><span class="sxs-lookup"><span data-stu-id="63ca9-155">Deduction method</span></span>
- <span data-ttu-id="63ca9-156">Mahaarvamise prioriteet</span><span class="sxs-lookup"><span data-stu-id="63ca9-156">Deduction priority</span></span>
- <span data-ttu-id="63ca9-157">Perioodi piiramine</span><span class="sxs-lookup"><span data-stu-id="63ca9-157">Limit period</span></span>
- <span data-ttu-id="63ca9-158">Piirsumma</span><span class="sxs-lookup"><span data-stu-id="63ca9-158">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="63ca9-159">Soodustused</span><span class="sxs-lookup"><span data-stu-id="63ca9-159">Benefits</span></span>

- <span data-ttu-id="63ca9-160">Plaan (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-160">Plan (required)</span></span>
- <span data-ttu-id="63ca9-161">Tüüp (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-161">Type (required)</span></span>
- <span data-ttu-id="63ca9-162">Suvand (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-162">Option (required)</span></span>
- <span data-ttu-id="63ca9-163">Soodustuse ID (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-163">Benefit ID (required)</span></span>
- <span data-ttu-id="63ca9-164">Sagedus</span><span class="sxs-lookup"><span data-stu-id="63ca9-164">Frequency</span></span>
- <span data-ttu-id="63ca9-165">Alus</span><span class="sxs-lookup"><span data-stu-id="63ca9-165">Basis</span></span>
- <span data-ttu-id="63ca9-166">Summa või määr</span><span class="sxs-lookup"><span data-stu-id="63ca9-166">Amount or rate</span></span>
- <span data-ttu-id="63ca9-167">Tulukood</span><span class="sxs-lookup"><span data-stu-id="63ca9-167">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="63ca9-168">Toetatud sagedused</span><span class="sxs-lookup"><span data-stu-id="63ca9-168">Supported frequencies</span></span> 

- <span data-ttu-id="63ca9-169">Iga nädal</span><span class="sxs-lookup"><span data-stu-id="63ca9-169">Weekly</span></span>
- <span data-ttu-id="63ca9-170">Kahe nädala tagant</span><span class="sxs-lookup"><span data-stu-id="63ca9-170">Bi-weekly</span></span>
- <span data-ttu-id="63ca9-171">Iga poole kuu tagant</span><span class="sxs-lookup"><span data-stu-id="63ca9-171">Semi-monthly</span></span>
- <span data-ttu-id="63ca9-172">Kord kuus</span><span class="sxs-lookup"><span data-stu-id="63ca9-172">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="63ca9-173">Toetatud alused</span><span class="sxs-lookup"><span data-stu-id="63ca9-173">Supported bases</span></span> 

- <span data-ttu-id="63ca9-174">Fikseeritud summa</span><span class="sxs-lookup"><span data-stu-id="63ca9-174">Fixed amount</span></span>
- <span data-ttu-id="63ca9-175">Tulu protsent</span><span class="sxs-lookup"><span data-stu-id="63ca9-175">Percent of earnings</span></span>
- <span data-ttu-id="63ca9-176">Produktiivsed tunnid</span><span class="sxs-lookup"><span data-stu-id="63ca9-176">Productive hours</span></span>

<span data-ttu-id="63ca9-177">Dayforce loob järgmised mahaarvamised palga mõju alusel, mis on määratletud soodustusplaanis.</span><span class="sxs-lookup"><span data-stu-id="63ca9-177">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="63ca9-178">Valik rakenduses Human Resources</span><span class="sxs-lookup"><span data-stu-id="63ca9-178">Selection in Human Resources</span></span>        | <span data-ttu-id="63ca9-179">Tulemus rakenduses Dayforce</span><span class="sxs-lookup"><span data-stu-id="63ca9-179">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="63ca9-180">Puudub</span><span class="sxs-lookup"><span data-stu-id="63ca9-180">None</span></span>                       | <span data-ttu-id="63ca9-181">Mahaarvamist ei looda.</span><span class="sxs-lookup"><span data-stu-id="63ca9-181">No deduction is created.</span></span>                      |
| <span data-ttu-id="63ca9-182">Ainult mahaarvamine</span><span class="sxs-lookup"><span data-stu-id="63ca9-182">Deduction only</span></span>             | <span data-ttu-id="63ca9-183">Luuakse töövõtja mahaarvamine.</span><span class="sxs-lookup"><span data-stu-id="63ca9-183">An employee deduction is created.</span></span>             |
| <span data-ttu-id="63ca9-184">Ainult lisamine</span><span class="sxs-lookup"><span data-stu-id="63ca9-184">Contribution only</span></span>          | <span data-ttu-id="63ca9-185">Luuakse tööandja mahaarvamine.</span><span class="sxs-lookup"><span data-stu-id="63ca9-185">An employer deduction is created.</span></span>             |
| <span data-ttu-id="63ca9-186">Mahaarvamine ja lisamine</span><span class="sxs-lookup"><span data-stu-id="63ca9-186">Deduction and contribution</span></span> | <span data-ttu-id="63ca9-187">Luuakse töövõtja ja tööandja mahaarvamised.</span><span class="sxs-lookup"><span data-stu-id="63ca9-187">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="63ca9-188">Lisateavet soodustusprogrammi määratlemise ja haldamise kohta vaadake järgmistest artiklitest.</span><span class="sxs-lookup"><span data-stu-id="63ca9-188">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="63ca9-189">Töötaja soodustuste programmi pakkumine</span><span class="sxs-lookup"><span data-stu-id="63ca9-189">Deliver an employee benefits program</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="63ca9-190">Uue soodustuse loomine</span><span class="sxs-lookup"><span data-stu-id="63ca9-190">Create a new benefit</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="63ca9-191">Soodustuskõlblikkuse reeglite ja poliitikate määratlemine</span><span class="sxs-lookup"><span data-stu-id="63ca9-191">Define benefit eligibility rules and policies</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="63ca9-192">Töötajate soodustuste registreerimine ja eemaldamine</span><span class="sxs-lookup"><span data-stu-id="63ca9-192">Enroll and remove benefits from workers</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="63ca9-193">Hüvitus</span><span class="sxs-lookup"><span data-stu-id="63ca9-193">Compensation</span></span> 

<span data-ttu-id="63ca9-194">Hüvituste haldust kasutatakse põhitasu ja preemiate jagamise juhtimiseks.</span><span class="sxs-lookup"><span data-stu-id="63ca9-194">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="63ca9-195">Töötaja fikseeritud põhipalga ja preemia tõusu juhitakse põhipalga plaanide kaudu.</span><span class="sxs-lookup"><span data-stu-id="63ca9-195">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="63ca9-196">Lisatasude (nt preemiate, tulemustasude aktsiate eelismüügi ja toetuste ning ühekordsete preemiate) maksmist juhitakse ergutussüsteemi plaanide kaudu.</span><span class="sxs-lookup"><span data-stu-id="63ca9-196">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="63ca9-197">Dayforce kasutab hüvituse teavet töövõtja tunni- või aastamäära arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="63ca9-197">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="63ca9-198">Nõutavad on põhipalgaplaanid ja palgamäära teisendamised.</span><span class="sxs-lookup"><span data-stu-id="63ca9-198">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="63ca9-199">Töövõtjad peavad olema seotud põhipalgaplaaniga.</span><span class="sxs-lookup"><span data-stu-id="63ca9-199">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="63ca9-200">Lisateavet hüvitusplaanide kohta vaadake järgmistest artiklitest.</span><span class="sxs-lookup"><span data-stu-id="63ca9-200">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="63ca9-201">Põhipalga plaanide loomine</span><span class="sxs-lookup"><span data-stu-id="63ca9-201">Create fixed compensation plans</span></span>](/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="63ca9-202">Ergutussüsteemi plaanide loomine</span><span class="sxs-lookup"><span data-stu-id="63ca9-202">Create variable compensation plans</span></span>](/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="63ca9-203">Palga/hüvituse struktuuri ja plaanide arendamine</span><span class="sxs-lookup"><span data-stu-id="63ca9-203">Develop salary/compensation structure and plans</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="63ca9-204">Hüvitusprotsess</span><span class="sxs-lookup"><span data-stu-id="63ca9-204">Process compensation</span></span>](/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="63ca9-205">Hüvitusprotsessi määratlemine ja tulemuste arvutamine</span><span class="sxs-lookup"><span data-stu-id="63ca9-205">Define compensation process and calculate results</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="63ca9-206">Töötaja liitmine põhipalga plaaniga</span><span class="sxs-lookup"><span data-stu-id="63ca9-206">Enroll an employee in a fixed compensation plan</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="63ca9-207">Töötaja liitmine tulemustasu plaaniga</span><span class="sxs-lookup"><span data-stu-id="63ca9-207">Enroll an employee in a variable compensation plan</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="63ca9-208">Tööd</span><span class="sxs-lookup"><span data-stu-id="63ca9-208">Jobs</span></span> 

<span data-ttu-id="63ca9-209">Töö on tööd tegeva isiku jaoks nõutavate ülesannete ja vastutuste kogum.</span><span class="sxs-lookup"><span data-stu-id="63ca9-209">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="63ca9-210">Lisateavet vt järgmistest artiklitest.</span><span class="sxs-lookup"><span data-stu-id="63ca9-210">For more information, see the following articles:</span></span>

- [<span data-ttu-id="63ca9-211">Töö komponentide seadistamine</span><span class="sxs-lookup"><span data-stu-id="63ca9-211">Setting up the components of a job</span></span>](/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="63ca9-212">Uute tööde määratlemine</span><span class="sxs-lookup"><span data-stu-id="63ca9-212">Define new jobs</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="63ca9-213">Ametikohad</span><span class="sxs-lookup"><span data-stu-id="63ca9-213">Positions</span></span>

<span data-ttu-id="63ca9-214">Ametikoht on töökoha üksik eksemplar.</span><span class="sxs-lookup"><span data-stu-id="63ca9-214">A position is an individual instance of a job.</span></span> <span data-ttu-id="63ca9-215">Näiteks on ametikoht „müügijuht (Ida)” vaid üks tööga „müügijuht” seostatud ametikohti.</span><span class="sxs-lookup"><span data-stu-id="63ca9-215">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="63ca9-216">Ametikoht kuulub osakonna alla.</span><span class="sxs-lookup"><span data-stu-id="63ca9-216">A position exists in a department.</span></span> <span data-ttu-id="63ca9-217">Iga ametikohaga saab seostada vaid ühte töötajat.</span><span class="sxs-lookup"><span data-stu-id="63ca9-217">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="63ca9-218">Ametikohtade seadistamisel pidage meeles järgmisi andmeid ja konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="63ca9-218">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="63ca9-219">Ametikoht (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-219">Position (required)</span></span>
- <span data-ttu-id="63ca9-220">Kirjeldus (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-220">Description (required)</span></span>
- <span data-ttu-id="63ca9-221">Töö (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-221">Job (required)</span></span>
- <span data-ttu-id="63ca9-222">Osakond (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-222">Department (required)</span></span>
- <span data-ttu-id="63ca9-223">Ametikoha tüüp (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-223">Position type (required)</span></span>
- <span data-ttu-id="63ca9-224">Täistööaja vaste</span><span class="sxs-lookup"><span data-stu-id="63ca9-224">Full-time equivalent</span></span>
- <span data-ttu-id="63ca9-225">Iga-aastased regulaarsed tunnid (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-225">Annual regular hours (required)</span></span>
- <span data-ttu-id="63ca9-226">Maksja juriidiline isik (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-226">Paid by legal entity (required)</span></span>
- <span data-ttu-id="63ca9-227">Palgatsükkel (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-227">Pay cycle (required)</span></span>
- <span data-ttu-id="63ca9-228">Vaike-finantsdimensioonid – kulukeskus (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-228">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="63ca9-229">Töötaja määramine – töötaja, määramise algus, määramise lõpp, põhjuse kood</span><span class="sxs-lookup"><span data-stu-id="63ca9-229">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="63ca9-230">Kui ühes osakonnas on sama tööga seotud mitu ametikohta, siis konsolideeritakse need rakenduses Dayforce üheks ametikohaks.</span><span class="sxs-lookup"><span data-stu-id="63ca9-230">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="63ca9-231">Lisateavet vt järgmistest artiklitest.</span><span class="sxs-lookup"><span data-stu-id="63ca9-231">For more information, see the following articles:</span></span>

- [<span data-ttu-id="63ca9-232">Tööjõu korraldamine osakondade, tööde ja ametikohtade abil</span><span class="sxs-lookup"><span data-stu-id="63ca9-232">Organize your workforce using departments, jobs, and positions</span></span>](/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="63ca9-233">Ametikohtade seadistamine</span><span class="sxs-lookup"><span data-stu-id="63ca9-233">Set up positions</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="63ca9-234">Osakonnad</span><span class="sxs-lookup"><span data-stu-id="63ca9-234">Departments</span></span>

<span data-ttu-id="63ca9-235">Osakond on tootmisüksus, mis esindab organisatsiooni kategooriat või funktsionaalset ala.</span><span class="sxs-lookup"><span data-stu-id="63ca9-235">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="63ca9-236">Osakond vastutab organisatsiooni kindla valdkonna eest, nagu müük, raamatupidamine või inimressursid.</span><span class="sxs-lookup"><span data-stu-id="63ca9-236">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="63ca9-237">Saate osakondi kasutada funktsionaalsete alade aruannete koostamiseks.</span><span class="sxs-lookup"><span data-stu-id="63ca9-237">You can use departments to report on functional areas.</span></span> <span data-ttu-id="63ca9-238">Osakonnad võivad vastutada kasumi ja kahjumi eest.</span><span class="sxs-lookup"><span data-stu-id="63ca9-238">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="63ca9-239">Lisateavet vt järgmistest artiklitest.</span><span class="sxs-lookup"><span data-stu-id="63ca9-239">For more information, see the following articles:</span></span>

- [<span data-ttu-id="63ca9-240">Osakonna loomine ja selle seostamine osakonnahierarhiaga</span><span class="sxs-lookup"><span data-stu-id="63ca9-240">Create a department and associate it with the department hierarchy</span></span>](/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="63ca9-241">Uute osakondade määratlemine</span><span class="sxs-lookup"><span data-stu-id="63ca9-241">Define new departments</span></span>](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="63ca9-242">Palgatsüklid ja makseperioodid</span><span class="sxs-lookup"><span data-stu-id="63ca9-242">Pay cycles and pay periods</span></span>

<span data-ttu-id="63ca9-243">Palgatsükkel määrab, kui tihti palgamaksmine toimub ja konkreetsed päevad, millal töötajatele palka makstakse.</span><span class="sxs-lookup"><span data-stu-id="63ca9-243">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="63ca9-244">Näiteks võib palgatsükli sageduseks olla üks kuu ja töövõtjatele makstakse seega kuu viimasel päeval.</span><span class="sxs-lookup"><span data-stu-id="63ca9-244">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="63ca9-245">Või kui palgatsükli sageduseks on üks nädal, siis makstakse töövõtjatele näiteks teisipäeviti pärast makseperioodi lõppu.</span><span class="sxs-lookup"><span data-stu-id="63ca9-245">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="63ca9-246">Palgatsükleid määratakse ametikohtadele selleks, et määrata, millal nendel ametikohtadel töötavatele töötajatele palka makstakse.</span><span class="sxs-lookup"><span data-stu-id="63ca9-246">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="63ca9-247">Pärast palgatsüklite loomist saate iga tsükli jaoks luua makseperioodid.</span><span class="sxs-lookup"><span data-stu-id="63ca9-247">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="63ca9-248">Igal makseperioodil on makse vaikekuupäev, mis põhineb teie sisestatud teabel.</span><span class="sxs-lookup"><span data-stu-id="63ca9-248">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="63ca9-249">Siiski saate erandite käsitlemiseks makseperioodi makse vaikekuupäeva muuta, näiteks kui maksekuupäev satub riigipühale.</span><span class="sxs-lookup"><span data-stu-id="63ca9-249">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="63ca9-250">Dayforce kasutab järgmist teavet.</span><span class="sxs-lookup"><span data-stu-id="63ca9-250">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="63ca9-251">Palgatsükkel (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-251">Pay cycle (required)</span></span>
- <span data-ttu-id="63ca9-252">Palgatsükli sagedus (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-252">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="63ca9-253">Perioodi alguskuupäev (esimene makseperiood on kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-253">Period start date (first pay period required)</span></span>
- <span data-ttu-id="63ca9-254">Makse vaikekuupäev (esimene makseperiood on kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-254">Default payment date (first pay period required)</span></span>

<span data-ttu-id="63ca9-255">See teave on integreeritud rakendusse Dayforce palgagruppidena ja on iga palgatsükli puhul eraldatud riigi või regiooniga.</span><span class="sxs-lookup"><span data-stu-id="63ca9-255">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="63ca9-256">Enne integreerimist peab olema loodud vähemalt üks makseperiood.</span><span class="sxs-lookup"><span data-stu-id="63ca9-256">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="63ca9-257">Dayforce loob palgagrupi kalendrid ja maksekuupäevad rakenduses Human Resources määratletud esimese makseperioodi alguskuupäeva ja makse vaikekuupäeva põhjal.</span><span class="sxs-lookup"><span data-stu-id="63ca9-257">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="63ca9-258">Tulukoodid</span><span class="sxs-lookup"><span data-stu-id="63ca9-258">Earning codes</span></span>

<span data-ttu-id="63ca9-259">Tulukoodid määratlevad kordumatult igat tüüpi tulud, mida töötajad saavad.</span><span class="sxs-lookup"><span data-stu-id="63ca9-259">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="63ca9-260">Koodidel on mitmeid tuludega seotud parameetreid, näiteks raamatupidamisreeglid, maksuseadused, aruandluse nõuded ja brutosumma võime.</span><span class="sxs-lookup"><span data-stu-id="63ca9-260">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="63ca9-261">Dayforce kasutab järgmist teavet.</span><span class="sxs-lookup"><span data-stu-id="63ca9-261">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="63ca9-262">Tulukood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-262">Earning Code (required)</span></span>
- <span data-ttu-id="63ca9-263">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="63ca9-263">Description</span></span>
- <span data-ttu-id="63ca9-264">Mõõtühik</span><span class="sxs-lookup"><span data-stu-id="63ca9-264">Unit of measure</span></span>
- <span data-ttu-id="63ca9-265">Produktiivne</span><span class="sxs-lookup"><span data-stu-id="63ca9-265">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="63ca9-266">Töötaja andmed</span><span class="sxs-lookup"><span data-stu-id="63ca9-266">Worker data</span></span>

<span data-ttu-id="63ca9-267">Töötajate kirjed on tähtsad teie personali- ja palgasüsteemide jaoks.</span><span class="sxs-lookup"><span data-stu-id="63ca9-267">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="63ca9-268">Teie sisestatud teavet saab kasutada töötajate ja nende isikliku teabe jälgimiseks.</span><span class="sxs-lookup"><span data-stu-id="63ca9-268">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="63ca9-269">Töötajate kohta saate hallata järgmist teavet.</span><span class="sxs-lookup"><span data-stu-id="63ca9-269">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="63ca9-270">**Üldine** – töötaja põhiteave, näiteks kontaktteave, demograafiline teave, tuvastamisteave, perekonna teave, sõjaväeteenistuse olek, välislähetuse teave ja isiklikud ning lähedase isiku kontaktandmed.</span><span class="sxs-lookup"><span data-stu-id="63ca9-270">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="63ca9-271">**Töösuhe** – töötaja töösuhte teave, näiteks töötaja palganud ettevõte või organisatsioon, määratud ametikoht, algus- ja lõppkuupäevad, töökõlblikkus, töölevõtutingimused, pension, puhkus ja ümberpaigutuse teave.</span><span class="sxs-lookup"><span data-stu-id="63ca9-271">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="63ca9-272">**Puhkused ja puudumised** – teave töötaja puudumiste kohta, näiteks töögraafikud, puudumiskanded ja puudumise seadistamine.</span><span class="sxs-lookup"><span data-stu-id="63ca9-272">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="63ca9-273">**Hüvitus ja palk** – teave töötaja hüvitusplaanide ja palgaarvestuse kohta, näiteks liitutud plaanid, preemiad, tööviljakus, komisjonitasu, maksuteave, pensionileminek ning palgast mahaarvamised.</span><span class="sxs-lookup"><span data-stu-id="63ca9-273">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="63ca9-274">Töötaja teabe sisestamisel pidage meeles järgmisi Dayforce’is kasutatavaid andmeid ja konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="63ca9-274">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="63ca9-275">Üldteave</span><span class="sxs-lookup"><span data-stu-id="63ca9-275">General information</span></span>

- <span data-ttu-id="63ca9-276">Töötaja number (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-276">Personnel number (required)</span></span>
- <span data-ttu-id="63ca9-277">Eesnimi (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-277">First name (required)</span></span>
- <span data-ttu-id="63ca9-278">Perekonnanimi (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-278">Last name (required)</span></span>
- <span data-ttu-id="63ca9-279">Teine eesnimi</span><span class="sxs-lookup"><span data-stu-id="63ca9-279">Middle name</span></span>
- <span data-ttu-id="63ca9-280">Staaž kuupäeval</span><span class="sxs-lookup"><span data-stu-id="63ca9-280">Seniority date</span></span>
- <span data-ttu-id="63ca9-281">Tuntud kui</span><span class="sxs-lookup"><span data-stu-id="63ca9-281">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="63ca9-282">Isikuandmed</span><span class="sxs-lookup"><span data-stu-id="63ca9-282">Personal information</span></span>

- <span data-ttu-id="63ca9-283">Perekonnaseis (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-283">Marital status (required)</span></span>
- <span data-ttu-id="63ca9-284">Sünnikuupäev (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-284">Birth date (required)</span></span>
- <span data-ttu-id="63ca9-285">Sugu (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-285">Gender (required)</span></span>
- <span data-ttu-id="63ca9-286">Puudega isik</span><span class="sxs-lookup"><span data-stu-id="63ca9-286">Person with disabilities</span></span>
- <span data-ttu-id="63ca9-287">Kodakondsusjärgse riigi regioon (ainult Mehhiko puhul)</span><span class="sxs-lookup"><span data-stu-id="63ca9-287">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="63ca9-288">Aadressiteave</span><span class="sxs-lookup"><span data-stu-id="63ca9-288">Address information</span></span>

- <span data-ttu-id="63ca9-289">Tänava nimi ja hoone number (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-289">Primary (required)</span></span>
- <span data-ttu-id="63ca9-290">Riik/regioon (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-290">Country/region (required)</span></span>
- <span data-ttu-id="63ca9-291">Sihtnumber (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-291">Postal code (required)</span></span>
- <span data-ttu-id="63ca9-292">Tänava number (kohustuslik) (ainult Mehhiko puhul)</span><span class="sxs-lookup"><span data-stu-id="63ca9-292">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="63ca9-293">Hoone tähis (ainult Mehhiko puhul)</span><span class="sxs-lookup"><span data-stu-id="63ca9-293">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="63ca9-294">Linn (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-294">City (required)</span></span>
- <span data-ttu-id="63ca9-295">Osariik (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-295">State (required)</span></span>
- <span data-ttu-id="63ca9-296">Maakond (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-296">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="63ca9-297">Kontaktteave</span><span class="sxs-lookup"><span data-stu-id="63ca9-297">Contact information</span></span> 

- <span data-ttu-id="63ca9-298">Tänava nimi ja hoone number (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-298">Primary (required)</span></span>
- <span data-ttu-id="63ca9-299">Kontaktnumber (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-299">Contact number (required)</span></span>
- <span data-ttu-id="63ca9-300">Sisetelefon</span><span class="sxs-lookup"><span data-stu-id="63ca9-300">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="63ca9-301">Palgateave ja tulukoodid</span><span class="sxs-lookup"><span data-stu-id="63ca9-301">Payroll information and earning codes</span></span>

<span data-ttu-id="63ca9-302">Töövõtjatele võidakse määrata teatud maksesagedusega konkreetsed tulud ja neil võivad olla eelistatud makseviisid.</span><span class="sxs-lookup"><span data-stu-id="63ca9-302">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="63ca9-303">Nende eelistuste ja sätete kasutamise tagamiseks kasutatakse Dayforce’is järgmisi välju.</span><span class="sxs-lookup"><span data-stu-id="63ca9-303">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="63ca9-304">Tulukoodid</span><span class="sxs-lookup"><span data-stu-id="63ca9-304">Earning codes</span></span>

- <span data-ttu-id="63ca9-305">Ametikoht (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-305">Position (required)</span></span>
- <span data-ttu-id="63ca9-306">Tulukood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-306">Earning Code (required)</span></span>
- <span data-ttu-id="63ca9-307">Maksesagedus (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-307">Frequency (required)</span></span>
- <span data-ttu-id="63ca9-308">Summa (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-308">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="63ca9-309">Palgateave</span><span class="sxs-lookup"><span data-stu-id="63ca9-309">Payroll information</span></span>

- <span data-ttu-id="63ca9-310">Makseviis</span><span class="sxs-lookup"><span data-stu-id="63ca9-310">Payment Method</span></span>
- <span data-ttu-id="63ca9-311">Majanduspiirkond (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-311">Economic Region (required)</span></span>
- <span data-ttu-id="63ca9-312">Töövõtja soodustuste ID</span><span class="sxs-lookup"><span data-stu-id="63ca9-312">Employee Benefits ID</span></span>
- <span data-ttu-id="63ca9-313">Riiklik isikukood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-313">National ID Number (required)</span></span>
- <span data-ttu-id="63ca9-314">Sõjaväeteenistuse number</span><span class="sxs-lookup"><span data-stu-id="63ca9-314">Military Service Number</span></span>
- <span data-ttu-id="63ca9-315">Vahetuse ID (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-315">Shift ID (required)</span></span>
- <span data-ttu-id="63ca9-316">Maksukood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-316">Tax Number (required)</span></span>
- <span data-ttu-id="63ca9-317">Ühingu ID (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-317">Union ID (required)</span></span>
- <span data-ttu-id="63ca9-318">Tööpäeva ID (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-318">Work Day ID (required)</span></span>
- <span data-ttu-id="63ca9-319">Tööloa number</span><span class="sxs-lookup"><span data-stu-id="63ca9-319">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="63ca9-320">Mehhiko toetab järgmisi makseviise: **sularaha**, **tšekk** (ettevõtte füüsiline tšekk) ja **elektrooniline makse**.</span><span class="sxs-lookup"><span data-stu-id="63ca9-320">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="63ca9-321">Kui makseviisi pole määratud, kasutatakse vaikevalikut **tšekk**.</span><span class="sxs-lookup"><span data-stu-id="63ca9-321">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="63ca9-322">Töösuhte üksikasjad</span><span class="sxs-lookup"><span data-stu-id="63ca9-322">Employment details</span></span>

<span data-ttu-id="63ca9-323">Töösuhte üksikasjade ajalugu on põhiline teave, millest tuletatakse rakenduses Dayforce töövõtja palkamise, töösuhte lõpetamise ja uuesti palkamise olekud.</span><span class="sxs-lookup"><span data-stu-id="63ca9-323">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="63ca9-324">Dayforce toetab korraga ainult ühte aktiivset töösuhte kirjet.</span><span class="sxs-lookup"><span data-stu-id="63ca9-324">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="63ca9-325">Töösuhte alguskuupäev (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-325">Employment start date (required)</span></span>
- <span data-ttu-id="63ca9-326">Töösuhte lõppkuupäev</span><span class="sxs-lookup"><span data-stu-id="63ca9-326">Employment end date</span></span>
- <span data-ttu-id="63ca9-327">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="63ca9-327">Start date</span></span>
- <span data-ttu-id="63ca9-328">Korrigeeritud alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="63ca9-328">Adjusted start date</span></span>
- <span data-ttu-id="63ca9-329">Töösuhte lõpetamise kuupäev (kohustuslik lõpetamisel)</span><span class="sxs-lookup"><span data-stu-id="63ca9-329">Termination date (required upon termination)</span></span>
- <span data-ttu-id="63ca9-330">Töösuhte lõpetamise põhjus (kohustuslik lõpetamisel)</span><span class="sxs-lookup"><span data-stu-id="63ca9-330">Termination reason (required upon termination)</span></span>

<span data-ttu-id="63ca9-331">Töövõtja tähtsaimad kuupäevad tuletatakse järgmisest teabest.</span><span class="sxs-lookup"><span data-stu-id="63ca9-331">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="63ca9-332">Inimressursid</span><span class="sxs-lookup"><span data-stu-id="63ca9-332">Human Resources</span></span>                | <span data-ttu-id="63ca9-333">Dayforce</span><span class="sxs-lookup"><span data-stu-id="63ca9-333">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63ca9-334">Kõige värskem palkamise kuupäev</span><span class="sxs-lookup"><span data-stu-id="63ca9-334">Most recent hire date</span></span> | <span data-ttu-id="63ca9-335">Praeguse lõpetamata töösuhte ajalookirje alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="63ca9-335">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="63ca9-336">Lõpetamiskuupäev</span><span class="sxs-lookup"><span data-stu-id="63ca9-336">Termination date</span></span>      | <span data-ttu-id="63ca9-337">Praeguse lõpetamata töösuhte ajalookirje lõpetamise kuupäev</span><span class="sxs-lookup"><span data-stu-id="63ca9-337">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="63ca9-338">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="63ca9-338">Start date</span></span>            | <span data-ttu-id="63ca9-339">Korrigeeritud alguskuupäev, alguskuupäev või praeguse passiivse töösuhte ajalookirje alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="63ca9-339">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="63ca9-340">Palkamise algne kuupäev</span><span class="sxs-lookup"><span data-stu-id="63ca9-340">Original hire date</span></span>    | <span data-ttu-id="63ca9-341">Varaseima töösuhte ajalookirje alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="63ca9-341">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="63ca9-342">Hüvitus</span><span class="sxs-lookup"><span data-stu-id="63ca9-342">Compensation</span></span>

<span data-ttu-id="63ca9-343">Tööhõiveperioodi jooksul peab iga töövõtja peamise ametikohaga olema seotud põhipalgaplaan.</span><span class="sxs-lookup"><span data-stu-id="63ca9-343">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="63ca9-344">See periood algab kuupäeval, mil töövõtja palgati (või töösuhte alguskuupäeval), ja jätkub kuni töösuhte lõpetamiseni.</span><span class="sxs-lookup"><span data-stu-id="63ca9-344">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="63ca9-345">Kehtivuse algus (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-345">Effective Date (required)</span></span>
- <span data-ttu-id="63ca9-346">Aegumiskuupäev</span><span class="sxs-lookup"><span data-stu-id="63ca9-346">Expiration date</span></span>
- <span data-ttu-id="63ca9-347">Palgamäär (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-347">Pay Rate (required)</span></span>
- <span data-ttu-id="63ca9-348">Palgamäära teisendamised (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-348">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="63ca9-349">Aastane vaste (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-349">Annual equivalent (required)</span></span>
- <span data-ttu-id="63ca9-350">Tunnine vaste (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-350">Hourly equivalent (required)</span></span>

<span data-ttu-id="63ca9-351">Kui tunnimääraga töövõtjal on mitu ametikohta, siis imporditakse peamise ametikoha põhipalk rakendusse Dayforce töövõtja taseme põhimäärana/-palgana.</span><span class="sxs-lookup"><span data-stu-id="63ca9-351">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="63ca9-352">Teiseste ametikohtade puhul salvestatakse Dayforce’is tunnimäär vastava ametikoha jaoks.</span><span class="sxs-lookup"><span data-stu-id="63ca9-352">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="63ca9-353">Kui kuupalgaga töötajal on mitu ametikohta, siis kasutatakse töövõtja taseme põhimäärana/-palgana kõikide aktiivsete ametikohtade tuletatud kumulatiivset tunnimäära ja aastapalka.</span><span class="sxs-lookup"><span data-stu-id="63ca9-353">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="63ca9-354">ID-numbrid</span><span class="sxs-lookup"><span data-stu-id="63ca9-354">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="63ca9-355">Isiku identifikaator</span><span class="sxs-lookup"><span data-stu-id="63ca9-355">Social Security identifier</span></span> 

<span data-ttu-id="63ca9-356">Igal töövõtjal peab olema üks peamine identifikaator.</span><span class="sxs-lookup"><span data-stu-id="63ca9-356">Every employee must have one primary identifier.</span></span> <span data-ttu-id="63ca9-357">Identifikaator peab olema isikukoodi- ehk **SSN**-tüüpi.</span><span class="sxs-lookup"><span data-stu-id="63ca9-357">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="63ca9-358">Rakenduses Dayforce tuletatakse see automaatselt töövõtja isiku identifikaatorina, mis on palkamiseks vajalik.</span><span class="sxs-lookup"><span data-stu-id="63ca9-358">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="63ca9-359">Peamine isikukood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-359">Primary (required)</span></span>
- <span data-ttu-id="63ca9-360">ID tüüp = SSN</span><span class="sxs-lookup"><span data-stu-id="63ca9-360">Identification Type = "SSN"</span></span>
- <span data-ttu-id="63ca9-361">Väljastamise kuupäev</span><span class="sxs-lookup"><span data-stu-id="63ca9-361">Issued Date</span></span>
- <span data-ttu-id="63ca9-362">Aegumiskuupäev</span><span class="sxs-lookup"><span data-stu-id="63ca9-362">Expiration Date</span></span>

<span data-ttu-id="63ca9-363">Töövõtjad saavad deklareerida mitu **SSN**-identifitseerimistüüpi ID-numbrit.</span><span class="sxs-lookup"><span data-stu-id="63ca9-363">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="63ca9-364">Dayforce’i integreeritakse vaid tähistusega **Peamine** kirje, olenemata sellest, kas number on aktiivne või aegunud.</span><span class="sxs-lookup"><span data-stu-id="63ca9-364">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="63ca9-365">Pangakontod ja väljamaksed</span><span class="sxs-lookup"><span data-stu-id="63ca9-365">Bank accounts and disbursements</span></span>

<span data-ttu-id="63ca9-366">Iga töötaja jaoks, kes soovib oma palka pangakonto ülekandena kätte saada, tuleb sisestada kehtiv pangakonto teave.</span><span class="sxs-lookup"><span data-stu-id="63ca9-366">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="63ca9-367">Inimressursid</span><span class="sxs-lookup"><span data-stu-id="63ca9-367">Human Resources</span></span>                         | <span data-ttu-id="63ca9-368">Dayforce</span><span class="sxs-lookup"><span data-stu-id="63ca9-368">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63ca9-369">Pangakonto number (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-369">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="63ca9-370">SWIFT-kood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-370">SWIFT code (required)</span></span>          | <span data-ttu-id="63ca9-371">Välja **Panga ID** kasutatakse palgaarvestuse töötlemiseks Mehhikos.</span><span class="sxs-lookup"><span data-stu-id="63ca9-371">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="63ca9-372">Filiaali kood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-372">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="63ca9-373">Pangakonto tüüp (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-373">Bank account type (required)</span></span>   | <span data-ttu-id="63ca9-374">Välja **Konto tüüp** kasutatakse palgaarvestuse töötlemiseks Mehhikos.</span><span class="sxs-lookup"><span data-stu-id="63ca9-374">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="63ca9-375">Toetatud väärtused on **Jooksevkonto** ja **Palgakonto**</span><span class="sxs-lookup"><span data-stu-id="63ca9-375">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="63ca9-376">Töövõtjad, kes soovivad oma palka pangakonto ülekannetena kätte saada, peavad esitama lingi jäägikontole, mis on juriidilise isiku alluvuses, kelle peamine aadress on Mehhikos ja kes on seotud Mehhiko panga kehtiva pangakontoga.</span><span class="sxs-lookup"><span data-stu-id="63ca9-376">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="63ca9-377">Kõiki ülejäänuid kontosid, mis pole jäägikontod, eiratakse.</span><span class="sxs-lookup"><span data-stu-id="63ca9-377">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="63ca9-378">Aadressiteave</span><span class="sxs-lookup"><span data-stu-id="63ca9-378">Address information</span></span>

<span data-ttu-id="63ca9-379">Igal töövõtjal peab olema üks peamine asukoht.</span><span class="sxs-lookup"><span data-stu-id="63ca9-379">Every employee must have one primary location.</span></span> <span data-ttu-id="63ca9-380">Dayforce’is kasutatakse seda asukohta, et määratleda töövõtja peamine elukoht maksustamise tarbeks.</span><span class="sxs-lookup"><span data-stu-id="63ca9-380">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="63ca9-381">Peamine elukoht (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-381">Primary (required)</span></span>
- <span data-ttu-id="63ca9-382">Riik/regioon (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-382">Country/region (required)</span></span>
- <span data-ttu-id="63ca9-383">Sihtnumber (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-383">Zip/postal code (required)</span></span>
- <span data-ttu-id="63ca9-384">Tänava nimi (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-384">Street (required)</span></span>
- <span data-ttu-id="63ca9-385">Tänava number (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-385">Street Number (required)</span></span>
- <span data-ttu-id="63ca9-386">Hoone tähis</span><span class="sxs-lookup"><span data-stu-id="63ca9-386">Building Complement</span></span>
- <span data-ttu-id="63ca9-387">Linn (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-387">City (required)</span></span>
- <span data-ttu-id="63ca9-388">Osariik (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-388">State (required)</span></span>
- <span data-ttu-id="63ca9-389">Maakond (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-389">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="63ca9-390">Andmete konfigureerimine palgaandmete loomiseks Ameerika Ühendriikides ja Kanadas</span><span class="sxs-lookup"><span data-stu-id="63ca9-390">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="63ca9-391">Kui loote palgaandmeid Ameerika Ühendriikide või Kanada töövõtjatele, siis peate konfigureerima järgmisi elemente.</span><span class="sxs-lookup"><span data-stu-id="63ca9-391">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="63ca9-392">Ametikohtadele tuleb määrata osakonnad.</span><span class="sxs-lookup"><span data-stu-id="63ca9-392">Departments are required on positions.</span></span>
- <span data-ttu-id="63ca9-393">Kulukeskused tuleb määratleda finantsdimensioonideks ja peavad olema vaike-finantsdimensiooni stringi esimene element.</span><span class="sxs-lookup"><span data-stu-id="63ca9-393">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="63ca9-394">Saate rakenduse Human Resources konfigureerida nõudma osakonna määratlemist ametikohtade poolt.</span><span class="sxs-lookup"><span data-stu-id="63ca9-394">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="63ca9-395">Selleks valige **Inimressursside ühised ametikohad > Ametikohad > Nõua ametikohtade puhul osakondi**.</span><span class="sxs-lookup"><span data-stu-id="63ca9-395">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="63ca9-396">Soovitame selle sätte integreerimiseks jõustada.</span><span class="sxs-lookup"><span data-stu-id="63ca9-396">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="63ca9-397">Töötüübid</span><span class="sxs-lookup"><span data-stu-id="63ca9-397">Job types</span></span>

<span data-ttu-id="63ca9-398">Töötüüpe kasutatakse sarnaste tööde kategooriatesse grupeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="63ca9-398">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="63ca9-399">Töötüübid on vajalikud palgaarvestuse töötlemiseks Ameerika Ühendriikides ja Kanadas.</span><span class="sxs-lookup"><span data-stu-id="63ca9-399">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="63ca9-400">Töötüübid on näiteks täistööaeg ja osaline tööaeg või kuupalk ning tunnipalk.</span><span class="sxs-lookup"><span data-stu-id="63ca9-400">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="63ca9-401">Töötüübid vastendatakse Dayforce’i tasutüüpidena, mis näitavad, kas töövõtja on tunni- või palgatöötaja.</span><span class="sxs-lookup"><span data-stu-id="63ca9-401">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="63ca9-402">Järgmised töötüübid ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="63ca9-402">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="63ca9-403">Töö tüüp</span><span class="sxs-lookup"><span data-stu-id="63ca9-403">Job type</span></span>   | <span data-ttu-id="63ca9-404">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="63ca9-404">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="63ca9-405">Tunnimäär</span><span class="sxs-lookup"><span data-stu-id="63ca9-405">Hourly</span></span>     | <span data-ttu-id="63ca9-406">Tunnimäär</span><span class="sxs-lookup"><span data-stu-id="63ca9-406">Hourly</span></span>      |
| <span data-ttu-id="63ca9-407">Põhipalk</span><span class="sxs-lookup"><span data-stu-id="63ca9-407">Salaried</span></span>   | <span data-ttu-id="63ca9-408">Põhipalk</span><span class="sxs-lookup"><span data-stu-id="63ca9-408">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="63ca9-409">Ametikoha tüübid</span><span class="sxs-lookup"><span data-stu-id="63ca9-409">Position types</span></span> 

<span data-ttu-id="63ca9-410">Ametikoha tüüpe kasutatakse selleks, et kirjeldada, kas ametikoht on täiskohaga, osalise tööajaga või midagi muud.</span><span class="sxs-lookup"><span data-stu-id="63ca9-410">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="63ca9-411">Ametikoha tüübid vastendatakse Dayforce’i tasuklassidena, mis näitavad, kas töövõtja on täis- või osalise tööajaga töötaja.</span><span class="sxs-lookup"><span data-stu-id="63ca9-411">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="63ca9-412">Järgmised ametikoha tüübid ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="63ca9-412">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="63ca9-413">Ametikoha tüüp</span><span class="sxs-lookup"><span data-stu-id="63ca9-413">Position type</span></span>   | <span data-ttu-id="63ca9-414">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="63ca9-414">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="63ca9-415">Täistööaeg</span><span class="sxs-lookup"><span data-stu-id="63ca9-415">Full-time</span></span>       | <span data-ttu-id="63ca9-416">Täistööajaga töövõtja</span><span class="sxs-lookup"><span data-stu-id="63ca9-416">Full time employee</span></span> |
| <span data-ttu-id="63ca9-417">Osaline tööaeg</span><span class="sxs-lookup"><span data-stu-id="63ca9-417">Part-time</span></span>       | <span data-ttu-id="63ca9-418">Osalise tööajaga töövõtja</span><span class="sxs-lookup"><span data-stu-id="63ca9-418">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="63ca9-419">Põhjuse koodid</span><span class="sxs-lookup"><span data-stu-id="63ca9-419">Reason codes</span></span>

<span data-ttu-id="63ca9-420">Põhjusekoodid annavad teavet töövõtja oleku kohta.</span><span class="sxs-lookup"><span data-stu-id="63ca9-420">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="63ca9-421">Põhjusekoodid vastendatakse Dayforce’i olekupõhjustena, mis näitavad töövõtja ametikoha või töösuhte oleku muutuse põhjust.</span><span class="sxs-lookup"><span data-stu-id="63ca9-421">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="63ca9-422">Järgmised põhjusekoodid ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="63ca9-422">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="63ca9-423">Põhjusekood</span><span class="sxs-lookup"><span data-stu-id="63ca9-423">Reason code</span></span>    | <span data-ttu-id="63ca9-424">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="63ca9-424">Description</span></span>      | <span data-ttu-id="63ca9-425">Rakendatavad stsenaariumid</span><span class="sxs-lookup"><span data-stu-id="63ca9-425">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="63ca9-426">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="63ca9-426">RESIGNATION</span></span>    | <span data-ttu-id="63ca9-427">Lahkumine</span><span class="sxs-lookup"><span data-stu-id="63ca9-427">Resignation</span></span>      | <span data-ttu-id="63ca9-428">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="63ca9-428">Terminate worker</span></span>     |
| <span data-ttu-id="63ca9-429">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="63ca9-429">TERMINATION</span></span>    | <span data-ttu-id="63ca9-430">Lõpetamine</span><span class="sxs-lookup"><span data-stu-id="63ca9-430">Termination</span></span>      | <span data-ttu-id="63ca9-431">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="63ca9-431">Terminate worker</span></span>     |
| <span data-ttu-id="63ca9-432">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="63ca9-432">RETIREMENT</span></span>     | <span data-ttu-id="63ca9-433">Pensionile jäämine</span><span class="sxs-lookup"><span data-stu-id="63ca9-433">Retirement</span></span>       | <span data-ttu-id="63ca9-434">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="63ca9-434">Terminate worker</span></span>     |
| <span data-ttu-id="63ca9-435">OTHER</span><span class="sxs-lookup"><span data-stu-id="63ca9-435">OTHER</span></span>          | <span data-ttu-id="63ca9-436">Muud põhjused</span><span class="sxs-lookup"><span data-stu-id="63ca9-436">Other Reasons</span></span>    | <span data-ttu-id="63ca9-437">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="63ca9-437">Terminate worker</span></span>     |
| <span data-ttu-id="63ca9-438">DEATH</span><span class="sxs-lookup"><span data-stu-id="63ca9-438">DEATH</span></span>          | <span data-ttu-id="63ca9-439">Surm</span><span class="sxs-lookup"><span data-stu-id="63ca9-439">Death</span></span>            | <span data-ttu-id="63ca9-440">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="63ca9-440">Terminate worker</span></span>     |
| <span data-ttu-id="63ca9-441">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="63ca9-441">LEAVEOFABSENCE</span></span> | <span data-ttu-id="63ca9-442">Puhkus</span><span class="sxs-lookup"><span data-stu-id="63ca9-442">Leave of Absence</span></span> | <span data-ttu-id="63ca9-443">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="63ca9-443">Terminate worker</span></span>     |
| <span data-ttu-id="63ca9-444">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="63ca9-444">CONTRACTEND</span></span>    | <span data-ttu-id="63ca9-445">Lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="63ca9-445">End of Contract</span></span>  | <span data-ttu-id="63ca9-446">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="63ca9-446">Terminate worker</span></span>     |
| <span data-ttu-id="63ca9-447">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="63ca9-447">SALARYCHANGE</span></span>   | <span data-ttu-id="63ca9-448">Palga muutus</span><span class="sxs-lookup"><span data-stu-id="63ca9-448">Change of Salary</span></span> | <span data-ttu-id="63ca9-449">Hüvitus</span><span class="sxs-lookup"><span data-stu-id="63ca9-449">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="63ca9-450">Perekonnaseis</span><span class="sxs-lookup"><span data-stu-id="63ca9-450">Marital status</span></span>

<span data-ttu-id="63ca9-451">Perekonnaseisu väärtused vastendatakse Dayforce’i ja tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.</span><span class="sxs-lookup"><span data-stu-id="63ca9-451">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="63ca9-452">Järgmine tabel näitab, kuidas perekonnaseisu väärtusi Dayforce’i vastendatakse.</span><span class="sxs-lookup"><span data-stu-id="63ca9-452">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="63ca9-453">Inimressursid</span><span class="sxs-lookup"><span data-stu-id="63ca9-453">Human Resources</span></span>                 | <span data-ttu-id="63ca9-454">Dayforce</span><span class="sxs-lookup"><span data-stu-id="63ca9-454">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="63ca9-455">Abielus</span><span class="sxs-lookup"><span data-stu-id="63ca9-455">Married</span></span>                | <span data-ttu-id="63ca9-456">Abielus</span><span class="sxs-lookup"><span data-stu-id="63ca9-456">Married</span></span>              |
| <span data-ttu-id="63ca9-457">Üksik</span><span class="sxs-lookup"><span data-stu-id="63ca9-457">Single</span></span>                 | <span data-ttu-id="63ca9-458">Üksik</span><span class="sxs-lookup"><span data-stu-id="63ca9-458">Single</span></span>               |
| <span data-ttu-id="63ca9-459">Lesk</span><span class="sxs-lookup"><span data-stu-id="63ca9-459">Widowed</span></span>                | <span data-ttu-id="63ca9-460">Lesk</span><span class="sxs-lookup"><span data-stu-id="63ca9-460">Widowed</span></span>              |
| <span data-ttu-id="63ca9-461">Lahutatud</span><span class="sxs-lookup"><span data-stu-id="63ca9-461">Divorced</span></span>               | <span data-ttu-id="63ca9-462">Lahutatud</span><span class="sxs-lookup"><span data-stu-id="63ca9-462">Divorced</span></span>             |
| <span data-ttu-id="63ca9-463">Registreeritud partnerlus</span><span class="sxs-lookup"><span data-stu-id="63ca9-463">Registered Partnership</span></span> | <span data-ttu-id="63ca9-464">Mitteabieluline kooselu</span><span class="sxs-lookup"><span data-stu-id="63ca9-464">Domestic Partnership</span></span> |
| <span data-ttu-id="63ca9-465">None</span><span class="sxs-lookup"><span data-stu-id="63ca9-465">None</span></span>                   | <span data-ttu-id="63ca9-466">None</span><span class="sxs-lookup"><span data-stu-id="63ca9-466">None</span></span>                 |
| <span data-ttu-id="63ca9-467">Kooselu</span><span class="sxs-lookup"><span data-stu-id="63ca9-467">Cohabiting</span></span>             | <span data-ttu-id="63ca9-468">Kooselu</span><span class="sxs-lookup"><span data-stu-id="63ca9-468">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="63ca9-469">Sugu</span><span class="sxs-lookup"><span data-stu-id="63ca9-469">Gender</span></span>

<span data-ttu-id="63ca9-470">Soo määratlused vastendatakse Dayforce’i ja tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.</span><span class="sxs-lookup"><span data-stu-id="63ca9-470">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="63ca9-471">Järgmine tabel näitab, kuidas soo määratlusi Dayforce’i vastendatakse.</span><span class="sxs-lookup"><span data-stu-id="63ca9-471">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="63ca9-472">Inimressursid</span><span class="sxs-lookup"><span data-stu-id="63ca9-472">Human Resources</span></span>       | <span data-ttu-id="63ca9-473">Dayforce</span><span class="sxs-lookup"><span data-stu-id="63ca9-473">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="63ca9-474">Mees</span><span class="sxs-lookup"><span data-stu-id="63ca9-474">Male</span></span>         | <span data-ttu-id="63ca9-475">Mees</span><span class="sxs-lookup"><span data-stu-id="63ca9-475">Male</span></span>            |
| <span data-ttu-id="63ca9-476">Naissoost</span><span class="sxs-lookup"><span data-stu-id="63ca9-476">Female</span></span>       | <span data-ttu-id="63ca9-477">Naissoost</span><span class="sxs-lookup"><span data-stu-id="63ca9-477">Female</span></span>          |
| <span data-ttu-id="63ca9-478">Mittespetsiifiline</span><span class="sxs-lookup"><span data-stu-id="63ca9-478">Non-specific</span></span> | <span data-ttu-id="63ca9-479">*Ei toetata*</span><span class="sxs-lookup"><span data-stu-id="63ca9-479">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="63ca9-480">Tulukoodid</span><span class="sxs-lookup"><span data-stu-id="63ca9-480">Earning codes</span></span>

<span data-ttu-id="63ca9-481">Tulukoodid määratlevad kordumatult igat tüüpi tulud, mida töötajad saavad.</span><span class="sxs-lookup"><span data-stu-id="63ca9-481">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="63ca9-482">Koodid hõlmavad mitmeid tuludega seotud parameetreid, näiteks raamatupidamisreeglid, maksuseadused, aruandluse nõuded ja brutosumma võime.</span><span class="sxs-lookup"><span data-stu-id="63ca9-482">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="63ca9-483">Kui kasutatakse toetuseta sagedust, siis kasutatakse arvutamise jaoks vaikimisi sagedust **Iga makse**.</span><span class="sxs-lookup"><span data-stu-id="63ca9-483">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="63ca9-484">Toetatud sagedused</span><span class="sxs-lookup"><span data-stu-id="63ca9-484">Supported frequencies</span></span>

- <span data-ttu-id="63ca9-485">Kõik</span><span class="sxs-lookup"><span data-stu-id="63ca9-485">All</span></span>
- <span data-ttu-id="63ca9-486">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="63ca9-486">EVERYPAY</span></span>
- <span data-ttu-id="63ca9-487">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="63ca9-487">EACHPAYPERIOD</span></span>
- <span data-ttu-id="63ca9-488">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="63ca9-488">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="63ca9-489">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="63ca9-489">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="63ca9-490">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="63ca9-490">1OFMTH</span></span>
- <span data-ttu-id="63ca9-491">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="63ca9-491">LASTOFMTH</span></span>
- <span data-ttu-id="63ca9-492">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="63ca9-492">2OFMTH</span></span>
- <span data-ttu-id="63ca9-493">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="63ca9-493">3OFMTH</span></span>
- <span data-ttu-id="63ca9-494">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="63ca9-494">4OFMTH</span></span>
- <span data-ttu-id="63ca9-495">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="63ca9-495">5OFMTH</span></span>
- <span data-ttu-id="63ca9-496">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="63ca9-496">1N2OFMTH</span></span>
- <span data-ttu-id="63ca9-497">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="63ca9-497">3N4OFMTH</span></span>
- <span data-ttu-id="63ca9-498">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="63ca9-498">1N3OFMTH</span></span>
- <span data-ttu-id="63ca9-499">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="63ca9-499">1N4OFMTH</span></span>
- <span data-ttu-id="63ca9-500">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="63ca9-500">2N3OFMTH</span></span>
- <span data-ttu-id="63ca9-501">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="63ca9-501">2N4OFMTH</span></span>
- <span data-ttu-id="63ca9-502">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="63ca9-502">1N2N3OFMTH</span></span>
- <span data-ttu-id="63ca9-503">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="63ca9-503">1N2N4OFMTH</span></span>
- <span data-ttu-id="63ca9-504">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="63ca9-504">1N3N4OFMTH</span></span>
- <span data-ttu-id="63ca9-505">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="63ca9-505">2N3N4OFMTH</span></span>
- <span data-ttu-id="63ca9-506">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="63ca9-506">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="63ca9-507">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="63ca9-507">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="63ca9-508">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="63ca9-508">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="63ca9-509">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="63ca9-509">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="63ca9-510">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="63ca9-510">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="63ca9-511">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="63ca9-511">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="63ca9-512">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="63ca9-512">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="63ca9-513">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="63ca9-513">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="63ca9-514">Aadressid</span><span class="sxs-lookup"><span data-stu-id="63ca9-514">Addresses</span></span>

<span data-ttu-id="63ca9-515">Teatud riigi või regiooni, osariigi ja maakonna (haldusüksuse) koodide tuvastamise jaoks on vaja kindlaid vorminguid, mida Dayforce ning riigi-/regioonisisesed pakkujad ära tunnevad.</span><span class="sxs-lookup"><span data-stu-id="63ca9-515">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="63ca9-516">Kuigi linnade vorming on paindlik, peab iga linn olema seotud osariigiga.</span><span class="sxs-lookup"><span data-stu-id="63ca9-516">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="63ca9-517">Inimressursid</span><span class="sxs-lookup"><span data-stu-id="63ca9-517">Human Resources</span></span>          | <span data-ttu-id="63ca9-518">Dayforce</span><span class="sxs-lookup"><span data-stu-id="63ca9-518">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="63ca9-519">Riik/regioon</span><span class="sxs-lookup"><span data-stu-id="63ca9-519">Country/Region</span></span>  | <span data-ttu-id="63ca9-520">Riigi kood</span><span class="sxs-lookup"><span data-stu-id="63ca9-520">Country Code</span></span>          |
| <span data-ttu-id="63ca9-521">Sihtnumber</span><span class="sxs-lookup"><span data-stu-id="63ca9-521">Zip/Postal Code</span></span> | <span data-ttu-id="63ca9-522">Sihtnumber</span><span class="sxs-lookup"><span data-stu-id="63ca9-522">Postal Code</span></span>           |
| <span data-ttu-id="63ca9-523">Osariik</span><span class="sxs-lookup"><span data-stu-id="63ca9-523">State</span></span>           | <span data-ttu-id="63ca9-524">Osariigi kood</span><span class="sxs-lookup"><span data-stu-id="63ca9-524">State Code</span></span>            |
| <span data-ttu-id="63ca9-525">Linn</span><span class="sxs-lookup"><span data-stu-id="63ca9-525">City</span></span>            | <span data-ttu-id="63ca9-526">Linn</span><span class="sxs-lookup"><span data-stu-id="63ca9-526">City</span></span>                  |
| <span data-ttu-id="63ca9-527">Maakond</span><span class="sxs-lookup"><span data-stu-id="63ca9-527">County</span></span>          | <span data-ttu-id="63ca9-528">Maakond (haldusüksus)</span><span class="sxs-lookup"><span data-stu-id="63ca9-528">County (Municipality)</span></span> |
| <span data-ttu-id="63ca9-529">Tänav</span><span class="sxs-lookup"><span data-stu-id="63ca9-529">Street</span></span>          | <span data-ttu-id="63ca9-530">Aadressirida 1</span><span class="sxs-lookup"><span data-stu-id="63ca9-530">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="63ca9-531">Maksuregioonid</span><span class="sxs-lookup"><span data-stu-id="63ca9-531">Tax regions</span></span>

<span data-ttu-id="63ca9-532">Maksuregioone kasutatakse palga loomisel sobiva maksu määramiseks.</span><span class="sxs-lookup"><span data-stu-id="63ca9-532">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="63ca9-533">Maksuregioonid vastendatakse Dayforce’i asukoha-aadressidena.</span><span class="sxs-lookup"><span data-stu-id="63ca9-533">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="63ca9-534">Maksuregiooni vaikevariant peab olema seotud töötaja aktiivse ametikohaga.</span><span class="sxs-lookup"><span data-stu-id="63ca9-534">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="63ca9-535">Maksuregioon (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-535">Tax region (required)</span></span>
- <span data-ttu-id="63ca9-536">Riik/regioon (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-536">Country/Region (required)</span></span>
- <span data-ttu-id="63ca9-537">Osariik (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-537">State (required)</span></span>
- <span data-ttu-id="63ca9-538">Maakond</span><span class="sxs-lookup"><span data-stu-id="63ca9-538">County</span></span> 
- <span data-ttu-id="63ca9-539">Linn (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="63ca9-539">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="63ca9-540">Andmete konfigureerimine palgaandmete loomiseks Mehhikos</span><span class="sxs-lookup"><span data-stu-id="63ca9-540">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="63ca9-541">Kui loote palgaandmeid Mehhiko töövõtjatele, siis peate konfigureerima järgmisi elemente.</span><span class="sxs-lookup"><span data-stu-id="63ca9-541">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="63ca9-542">Ametikohtadele tuleb määrata osakonnad.</span><span class="sxs-lookup"><span data-stu-id="63ca9-542">Departments are required on positions.</span></span>
- <span data-ttu-id="63ca9-543">Kulukeskused tuleb määratleda finantsdimensioonideks ja peavad olema vaike-finantsdimensiooni stringi esimene element.</span><span class="sxs-lookup"><span data-stu-id="63ca9-543">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="63ca9-544">Töötüübid</span><span class="sxs-lookup"><span data-stu-id="63ca9-544">Job types</span></span>

<span data-ttu-id="63ca9-545">Töötüüpe kasutatakse sarnaste tööde kategooriatesse grupeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="63ca9-545">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="63ca9-546">Mehhikos palgaarvestuse töötlemiseks on vajalikud töötüübid.</span><span class="sxs-lookup"><span data-stu-id="63ca9-546">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="63ca9-547">Töötüübid on näiteks täistööaeg ja osaline tööaeg või kuupalk ning tunnipalk.</span><span class="sxs-lookup"><span data-stu-id="63ca9-547">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="63ca9-548">Töötüübid vastendatakse Dayforce’i tasutüüpidena, mis näitavad, kas töövõtja on tunni- või palgatöötaja.</span><span class="sxs-lookup"><span data-stu-id="63ca9-548">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="63ca9-549">Järgmised töötüübid ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="63ca9-549">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="63ca9-550">Töö tüüp</span><span class="sxs-lookup"><span data-stu-id="63ca9-550">Job type</span></span>   | <span data-ttu-id="63ca9-551">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="63ca9-551">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="63ca9-552">Tunnimäär</span><span class="sxs-lookup"><span data-stu-id="63ca9-552">Hourly</span></span>     | <span data-ttu-id="63ca9-553">MX tunnimäär</span><span class="sxs-lookup"><span data-stu-id="63ca9-553">MX Hourly</span></span>   |
| <span data-ttu-id="63ca9-554">Põhipalk</span><span class="sxs-lookup"><span data-stu-id="63ca9-554">Salaried</span></span>   | <span data-ttu-id="63ca9-555">MX põhipalk</span><span class="sxs-lookup"><span data-stu-id="63ca9-555">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="63ca9-556">Positsioonitüübid</span><span class="sxs-lookup"><span data-stu-id="63ca9-556">Position types</span></span> 

<span data-ttu-id="63ca9-557">Ametikoha tüüpe kasutatakse selleks, et kirjeldada, kas ametikoht on täiskohaga, osalise tööajaga või midagi muud.</span><span class="sxs-lookup"><span data-stu-id="63ca9-557">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="63ca9-558">Ametikoha tüübid vastendatakse Dayforce’i tasuklassidena, mis näitavad, kas töövõtja on täis- või osalise tööajaga töötaja.</span><span class="sxs-lookup"><span data-stu-id="63ca9-558">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="63ca9-559">Järgmised ametikoha tüübid ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="63ca9-559">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="63ca9-560">Ametikoha tüüp</span><span class="sxs-lookup"><span data-stu-id="63ca9-560">Position type</span></span>   | <span data-ttu-id="63ca9-561">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="63ca9-561">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="63ca9-562">Täistööaeg</span><span class="sxs-lookup"><span data-stu-id="63ca9-562">Full-time</span></span>       | <span data-ttu-id="63ca9-563">Täistööajaga töövõtja</span><span class="sxs-lookup"><span data-stu-id="63ca9-563">Full time employee</span></span> |
| <span data-ttu-id="63ca9-564">Osaline tööaeg</span><span class="sxs-lookup"><span data-stu-id="63ca9-564">Part-time</span></span>       | <span data-ttu-id="63ca9-565">Osalise tööajaga töövõtja</span><span class="sxs-lookup"><span data-stu-id="63ca9-565">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="63ca9-566">Põhjuse koodid</span><span class="sxs-lookup"><span data-stu-id="63ca9-566">Reason codes</span></span>

<span data-ttu-id="63ca9-567">Põhjusekoodid annavad teavet töövõtja oleku kohta.</span><span class="sxs-lookup"><span data-stu-id="63ca9-567">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="63ca9-568">Põhjusekoodid vastendatakse Dayforce’i olekupõhjustena, mis näitavad töövõtja ametikoha või töösuhte oleku muutuse põhjust.</span><span class="sxs-lookup"><span data-stu-id="63ca9-568">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="63ca9-569">Järgmised põhjusekoodid ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="63ca9-569">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="63ca9-570">Põhjusekood</span><span class="sxs-lookup"><span data-stu-id="63ca9-570">Reason code</span></span>            | <span data-ttu-id="63ca9-571">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="63ca9-571">Description</span></span>                    | <span data-ttu-id="63ca9-572">Rakendatavad stsenaariumid</span><span class="sxs-lookup"><span data-stu-id="63ca9-572">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="63ca9-573">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="63ca9-573">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="63ca9-574">Lahkumine enne esimest palgamakset</span><span class="sxs-lookup"><span data-stu-id="63ca9-574">Departure before first payroll</span></span> | <span data-ttu-id="63ca9-575">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="63ca9-575">Terminate worker</span></span>     |
| <span data-ttu-id="63ca9-576">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="63ca9-576">RESIGNATION</span></span>            | <span data-ttu-id="63ca9-577">Lahkumine</span><span class="sxs-lookup"><span data-stu-id="63ca9-577">Resignation</span></span>                    | <span data-ttu-id="63ca9-578">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="63ca9-578">Terminate worker</span></span>     |
| <span data-ttu-id="63ca9-579">PENSION</span><span class="sxs-lookup"><span data-stu-id="63ca9-579">PENSION</span></span>                | <span data-ttu-id="63ca9-580">Pension</span><span class="sxs-lookup"><span data-stu-id="63ca9-580">Pension</span></span>                        | <span data-ttu-id="63ca9-581">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="63ca9-581">Terminate worker</span></span>     |
| <span data-ttu-id="63ca9-582">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="63ca9-582">TERMINATION</span></span>            | <span data-ttu-id="63ca9-583">Lõpetamine</span><span class="sxs-lookup"><span data-stu-id="63ca9-583">Termination</span></span>                    | <span data-ttu-id="63ca9-584">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="63ca9-584">Terminate worker</span></span>     |
| <span data-ttu-id="63ca9-585">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="63ca9-585">RETIREMENT</span></span>             | <span data-ttu-id="63ca9-586">Pensionile jäämine</span><span class="sxs-lookup"><span data-stu-id="63ca9-586">Retirement</span></span>                     | <span data-ttu-id="63ca9-587">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="63ca9-587">Terminate worker</span></span>     |
| <span data-ttu-id="63ca9-588">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="63ca9-588">ABSENTEE</span></span>               | <span data-ttu-id="63ca9-589">Puuduja</span><span class="sxs-lookup"><span data-stu-id="63ca9-589">Absentee</span></span>                       | <span data-ttu-id="63ca9-590">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="63ca9-590">Terminate worker</span></span>     |
| <span data-ttu-id="63ca9-591">OTHER</span><span class="sxs-lookup"><span data-stu-id="63ca9-591">OTHER</span></span>                  | <span data-ttu-id="63ca9-592">Muud põhjused</span><span class="sxs-lookup"><span data-stu-id="63ca9-592">Other Reasons</span></span>                  | <span data-ttu-id="63ca9-593">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="63ca9-593">Terminate worker</span></span>     |
| <span data-ttu-id="63ca9-594">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="63ca9-594">CLOSURE</span></span>                | <span data-ttu-id="63ca9-595">Ettevõte suletud</span><span class="sxs-lookup"><span data-stu-id="63ca9-595">Business Closure</span></span>               | <span data-ttu-id="63ca9-596">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="63ca9-596">Terminate worker</span></span>     |
| <span data-ttu-id="63ca9-597">DEATH</span><span class="sxs-lookup"><span data-stu-id="63ca9-597">DEATH</span></span>                  | <span data-ttu-id="63ca9-598">Surm</span><span class="sxs-lookup"><span data-stu-id="63ca9-598">Death</span></span>                          | <span data-ttu-id="63ca9-599">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="63ca9-599">Terminate worker</span></span>     |
| <span data-ttu-id="63ca9-600">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="63ca9-600">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="63ca9-601">Puhkus</span><span class="sxs-lookup"><span data-stu-id="63ca9-601">Leave of Absence</span></span>               | <span data-ttu-id="63ca9-602">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="63ca9-602">Terminate worker</span></span>     |
| <span data-ttu-id="63ca9-603">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="63ca9-603">CONTRACTEND</span></span>            | <span data-ttu-id="63ca9-604">Lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="63ca9-604">End of Contract</span></span>                | <span data-ttu-id="63ca9-605">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="63ca9-605">Terminate worker</span></span>     |
| <span data-ttu-id="63ca9-606">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="63ca9-606">SALARYCHANGE</span></span>           | <span data-ttu-id="63ca9-607">Palga muutus</span><span class="sxs-lookup"><span data-stu-id="63ca9-607">Change of Salary</span></span>               | <span data-ttu-id="63ca9-608">Hüvitus</span><span class="sxs-lookup"><span data-stu-id="63ca9-608">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="63ca9-609">Töösuhte tingimused</span><span class="sxs-lookup"><span data-stu-id="63ca9-609">Terms of employment</span></span>

<span data-ttu-id="63ca9-610">Töösuhte tingimusi kasutatakse töösuhte tingimuste kategooriate loomiseks.</span><span class="sxs-lookup"><span data-stu-id="63ca9-610">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="63ca9-611">Tingimused vastendatakse Dayforce’i töösuhte indikaatorväärtustena.</span><span class="sxs-lookup"><span data-stu-id="63ca9-611">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="63ca9-612">Järgmised töösuhte tingimused ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="63ca9-612">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="63ca9-613">Töösuhte tingimused</span><span class="sxs-lookup"><span data-stu-id="63ca9-613">Terms of employment</span></span>   | <span data-ttu-id="63ca9-614">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="63ca9-614">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="63ca9-615">Tavaline</span><span class="sxs-lookup"><span data-stu-id="63ca9-615">Regular</span></span>               | <span data-ttu-id="63ca9-616">Tavaline</span><span class="sxs-lookup"><span data-stu-id="63ca9-616">Regular</span></span>     |
| <span data-ttu-id="63ca9-617">Otse</span><span class="sxs-lookup"><span data-stu-id="63ca9-617">Direct</span></span>                | <span data-ttu-id="63ca9-618">Otse</span><span class="sxs-lookup"><span data-stu-id="63ca9-618">Direct</span></span>      |
| <span data-ttu-id="63ca9-619">Praktika</span><span class="sxs-lookup"><span data-stu-id="63ca9-619">Internship</span></span>            | <span data-ttu-id="63ca9-620">Praktika</span><span class="sxs-lookup"><span data-stu-id="63ca9-620">Internship</span></span>  |
| <span data-ttu-id="63ca9-621">Alaline</span><span class="sxs-lookup"><span data-stu-id="63ca9-621">Permanent</span></span>             | <span data-ttu-id="63ca9-622">Alaline</span><span class="sxs-lookup"><span data-stu-id="63ca9-622">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="63ca9-623">Perekonnaseis</span><span class="sxs-lookup"><span data-stu-id="63ca9-623">Marital status</span></span>

<span data-ttu-id="63ca9-624">Perekonnaseisu väärtused vastendatakse Dayforce’i ja tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.</span><span class="sxs-lookup"><span data-stu-id="63ca9-624">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="63ca9-625">Järgmine tabel näitab, kuidas perekonnaseisu väärtusi Dayforce’i vastendatakse.</span><span class="sxs-lookup"><span data-stu-id="63ca9-625">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="63ca9-626">Inimressursid</span><span class="sxs-lookup"><span data-stu-id="63ca9-626">Human Resources</span></span>                 | <span data-ttu-id="63ca9-627">Dayforce</span><span class="sxs-lookup"><span data-stu-id="63ca9-627">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="63ca9-628">Abielus</span><span class="sxs-lookup"><span data-stu-id="63ca9-628">Married</span></span>                | <span data-ttu-id="63ca9-629">Abielus</span><span class="sxs-lookup"><span data-stu-id="63ca9-629">Married</span></span>                   |
| <span data-ttu-id="63ca9-630">Üksik</span><span class="sxs-lookup"><span data-stu-id="63ca9-630">Single</span></span>                 | <span data-ttu-id="63ca9-631">Üksik</span><span class="sxs-lookup"><span data-stu-id="63ca9-631">Single</span></span>                    |
| <span data-ttu-id="63ca9-632">Lesk</span><span class="sxs-lookup"><span data-stu-id="63ca9-632">Widowed</span></span>                | <span data-ttu-id="63ca9-633">Lesk</span><span class="sxs-lookup"><span data-stu-id="63ca9-633">Widowed</span></span>                   |
| <span data-ttu-id="63ca9-634">Lahutatud</span><span class="sxs-lookup"><span data-stu-id="63ca9-634">Divorced</span></span>               | <span data-ttu-id="63ca9-635">Lahutatud</span><span class="sxs-lookup"><span data-stu-id="63ca9-635">Divorced</span></span>                  |
| <span data-ttu-id="63ca9-636">Registreeritud partnerlus</span><span class="sxs-lookup"><span data-stu-id="63ca9-636">Registered Partnership</span></span> | <span data-ttu-id="63ca9-637">Mitteabieluline kooselu</span><span class="sxs-lookup"><span data-stu-id="63ca9-637">Domestic Partnership</span></span>      |
| <span data-ttu-id="63ca9-638">None</span><span class="sxs-lookup"><span data-stu-id="63ca9-638">None</span></span>                   | <span data-ttu-id="63ca9-639">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="63ca9-639">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="63ca9-640">Kooselu</span><span class="sxs-lookup"><span data-stu-id="63ca9-640">Cohabiting</span></span>             | <span data-ttu-id="63ca9-641">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="63ca9-641">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="63ca9-642">Sugu</span><span class="sxs-lookup"><span data-stu-id="63ca9-642">Gender</span></span>

<span data-ttu-id="63ca9-643">Soo määratlused vastendatakse Dayforce’i ja tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.</span><span class="sxs-lookup"><span data-stu-id="63ca9-643">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="63ca9-644">Järgmine tabel näitab, kuidas soo määratlusi Dayforce’i vastendatakse.</span><span class="sxs-lookup"><span data-stu-id="63ca9-644">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="63ca9-645">Inimressursid</span><span class="sxs-lookup"><span data-stu-id="63ca9-645">Human Resources</span></span>       | <span data-ttu-id="63ca9-646">Dayforce</span><span class="sxs-lookup"><span data-stu-id="63ca9-646">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="63ca9-647">Mees</span><span class="sxs-lookup"><span data-stu-id="63ca9-647">Male</span></span>         | <span data-ttu-id="63ca9-648">Mees</span><span class="sxs-lookup"><span data-stu-id="63ca9-648">Male</span></span>                      |
| <span data-ttu-id="63ca9-649">Naissoost</span><span class="sxs-lookup"><span data-stu-id="63ca9-649">Female</span></span>       | <span data-ttu-id="63ca9-650">Naissoost</span><span class="sxs-lookup"><span data-stu-id="63ca9-650">Female</span></span>                    |
| <span data-ttu-id="63ca9-651">Mittespetsiifiline</span><span class="sxs-lookup"><span data-stu-id="63ca9-651">Non-specific</span></span> | <span data-ttu-id="63ca9-652">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="63ca9-652">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="63ca9-653">Makseviis</span><span class="sxs-lookup"><span data-stu-id="63ca9-653">Payment method</span></span>

<span data-ttu-id="63ca9-654">Makseviisid võimaldavad töövõtjal ja ettevõttel kirjeldada, kuidas töövõtjatele makstakse.</span><span class="sxs-lookup"><span data-stu-id="63ca9-654">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="63ca9-655">Makseviisid vastendatakse Dayforce’i ja tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.</span><span class="sxs-lookup"><span data-stu-id="63ca9-655">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="63ca9-656">Järgmine tabel näitab, kuidas makseviise Dayforce’i vastendatakse.</span><span class="sxs-lookup"><span data-stu-id="63ca9-656">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="63ca9-657">Inimressursid</span><span class="sxs-lookup"><span data-stu-id="63ca9-657">Human Resources</span></span>             | <span data-ttu-id="63ca9-658">Dayforce</span><span class="sxs-lookup"><span data-stu-id="63ca9-658">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="63ca9-659">Sularaha</span><span class="sxs-lookup"><span data-stu-id="63ca9-659">Cash</span></span>               | <span data-ttu-id="63ca9-660">Sularaha</span><span class="sxs-lookup"><span data-stu-id="63ca9-660">Cash</span></span>                      |
| <span data-ttu-id="63ca9-661">Elektrooniline makse</span><span class="sxs-lookup"><span data-stu-id="63ca9-661">Electronic Payment</span></span> | <span data-ttu-id="63ca9-662">Ülekanne</span><span class="sxs-lookup"><span data-stu-id="63ca9-662">Transfer</span></span>                  |
| <span data-ttu-id="63ca9-663">Kontrolli</span><span class="sxs-lookup"><span data-stu-id="63ca9-663">Check</span></span>              | <span data-ttu-id="63ca9-664">Tšekk</span><span class="sxs-lookup"><span data-stu-id="63ca9-664">Cheque</span></span>                    |
| <span data-ttu-id="63ca9-665">Pangaveksel</span><span class="sxs-lookup"><span data-stu-id="63ca9-665">Bank Draft</span></span>         | <span data-ttu-id="63ca9-666">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="63ca9-666">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="63ca9-667">Muud</span><span class="sxs-lookup"><span data-stu-id="63ca9-667">Other</span></span>              | <span data-ttu-id="63ca9-668">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="63ca9-668">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="63ca9-669">Pangakonto tüüp</span><span class="sxs-lookup"><span data-stu-id="63ca9-669">Bank account type</span></span>

<span data-ttu-id="63ca9-670">Pangakonto tüüpe kasutatakse elektrooniliste maksete tegemiseks töötajatele.</span><span class="sxs-lookup"><span data-stu-id="63ca9-670">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="63ca9-671">Pangakonto tüübid vastendatakse Dayforce’i ülekandekonto teabena.</span><span class="sxs-lookup"><span data-stu-id="63ca9-671">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="63ca9-672">Pangakonto tüübid tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.</span><span class="sxs-lookup"><span data-stu-id="63ca9-672">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="63ca9-673">Inimressursid</span><span class="sxs-lookup"><span data-stu-id="63ca9-673">Human Resources</span></span>            | <span data-ttu-id="63ca9-674">Dayforce</span><span class="sxs-lookup"><span data-stu-id="63ca9-674">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="63ca9-675">Jooksevkonto</span><span class="sxs-lookup"><span data-stu-id="63ca9-675">Checking Account</span></span>  | <span data-ttu-id="63ca9-676">Jooksevkonto</span><span class="sxs-lookup"><span data-stu-id="63ca9-676">CheckingAccount</span></span>           |
| <span data-ttu-id="63ca9-677">Palgakonto</span><span class="sxs-lookup"><span data-stu-id="63ca9-677">Payroll Account</span></span>   | <span data-ttu-id="63ca9-678">Palgakonto</span><span class="sxs-lookup"><span data-stu-id="63ca9-678">PayrollAccount</span></span>            |
| <span data-ttu-id="63ca9-679">Hoiukonto</span><span class="sxs-lookup"><span data-stu-id="63ca9-679">Savings Account</span></span>   | <span data-ttu-id="63ca9-680">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="63ca9-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="63ca9-681">BankGiroti konto</span><span class="sxs-lookup"><span data-stu-id="63ca9-681">BankGirot account</span></span> | <span data-ttu-id="63ca9-682">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="63ca9-682">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="63ca9-683">PlusGiroti konto</span><span class="sxs-lookup"><span data-stu-id="63ca9-683">PlusGirot account</span></span> | <span data-ttu-id="63ca9-684">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="63ca9-684">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="63ca9-685">Tulukoodid</span><span class="sxs-lookup"><span data-stu-id="63ca9-685">Earning codes</span></span>

<span data-ttu-id="63ca9-686">Tulukoodid määratlevad kordumatult igat tüüpi tulud, mida töötajad saavad.</span><span class="sxs-lookup"><span data-stu-id="63ca9-686">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="63ca9-687">Koodid hõlmavad mitmeid tuludega seotud parameetreid, näiteks raamatupidamisreeglid, maksuseadused, aruandluse nõuded ja brutosumma võime.</span><span class="sxs-lookup"><span data-stu-id="63ca9-687">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="63ca9-688">Kui kasutatakse toetuseta sagedust, siis kasutatakse arvutamise jaoks vaikimisi sagedust **Iga makse**.</span><span class="sxs-lookup"><span data-stu-id="63ca9-688">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="63ca9-689">Toetatud sagedused</span><span class="sxs-lookup"><span data-stu-id="63ca9-689">Supported frequencies</span></span>

- <span data-ttu-id="63ca9-690">Kõik</span><span class="sxs-lookup"><span data-stu-id="63ca9-690">All</span></span>
- <span data-ttu-id="63ca9-691">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="63ca9-691">EVERYPAY</span></span>
- <span data-ttu-id="63ca9-692">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="63ca9-692">EACHPAYPERIOD</span></span>
- <span data-ttu-id="63ca9-693">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="63ca9-693">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="63ca9-694">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="63ca9-694">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="63ca9-695">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="63ca9-695">1OFMTH</span></span>
- <span data-ttu-id="63ca9-696">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="63ca9-696">LASTOFMTH</span></span>
- <span data-ttu-id="63ca9-697">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="63ca9-697">2OFMTH</span></span>
- <span data-ttu-id="63ca9-698">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="63ca9-698">3OFMTH</span></span>
- <span data-ttu-id="63ca9-699">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="63ca9-699">4OFMTH</span></span>
- <span data-ttu-id="63ca9-700">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="63ca9-700">5OFMTH</span></span>
- <span data-ttu-id="63ca9-701">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="63ca9-701">1N2OFMTH</span></span>
- <span data-ttu-id="63ca9-702">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="63ca9-702">3N4OFMTH</span></span>
- <span data-ttu-id="63ca9-703">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="63ca9-703">1N3OFMTH</span></span>
- <span data-ttu-id="63ca9-704">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="63ca9-704">1N4OFMTH</span></span>
- <span data-ttu-id="63ca9-705">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="63ca9-705">2N3OFMTH</span></span>
- <span data-ttu-id="63ca9-706">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="63ca9-706">2N4OFMTH</span></span>
- <span data-ttu-id="63ca9-707">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="63ca9-707">1N2N3OFMTH</span></span>
- <span data-ttu-id="63ca9-708">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="63ca9-708">1N2N4OFMTH</span></span>
- <span data-ttu-id="63ca9-709">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="63ca9-709">1N3N4OFMTH</span></span>
- <span data-ttu-id="63ca9-710">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="63ca9-710">2N3N4OFMTH</span></span>
- <span data-ttu-id="63ca9-711">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="63ca9-711">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="63ca9-712">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="63ca9-712">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="63ca9-713">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="63ca9-713">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="63ca9-714">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="63ca9-714">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="63ca9-715">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="63ca9-715">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="63ca9-716">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="63ca9-716">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="63ca9-717">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="63ca9-717">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="63ca9-718">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="63ca9-718">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="63ca9-719">Aadressid</span><span class="sxs-lookup"><span data-stu-id="63ca9-719">Addresses</span></span>

<span data-ttu-id="63ca9-720">Teatud riigi või regiooni, osariigi ja maakonna (haldusüksuse) koodide tuvastamise jaoks on vaja kindlaid vorminguid, mida Dayforce ning riigi-/regioonisisesed pakkujad ära tunnevad.</span><span class="sxs-lookup"><span data-stu-id="63ca9-720">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="63ca9-721">Kuigi linnade vorming on paindlik, peab iga linn olema seotud osariigiga.</span><span class="sxs-lookup"><span data-stu-id="63ca9-721">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="63ca9-722">Inimressursid</span><span class="sxs-lookup"><span data-stu-id="63ca9-722">Human Resources</span></span>              | <span data-ttu-id="63ca9-723">Dayforce</span><span class="sxs-lookup"><span data-stu-id="63ca9-723">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="63ca9-724">Riik/regioon</span><span class="sxs-lookup"><span data-stu-id="63ca9-724">Country/Region</span></span>      | <span data-ttu-id="63ca9-725">Riigi kood</span><span class="sxs-lookup"><span data-stu-id="63ca9-725">Country Code</span></span>          |
| <span data-ttu-id="63ca9-726">Sihtnumber</span><span class="sxs-lookup"><span data-stu-id="63ca9-726">Zip/Postal Code</span></span>     | <span data-ttu-id="63ca9-727">Sihtnumber</span><span class="sxs-lookup"><span data-stu-id="63ca9-727">Postal Code</span></span>           |
| <span data-ttu-id="63ca9-728">Osariik</span><span class="sxs-lookup"><span data-stu-id="63ca9-728">State</span></span>               | <span data-ttu-id="63ca9-729">Osariigi kood</span><span class="sxs-lookup"><span data-stu-id="63ca9-729">State Code</span></span>            |
| <span data-ttu-id="63ca9-730">Linn</span><span class="sxs-lookup"><span data-stu-id="63ca9-730">City</span></span>                | <span data-ttu-id="63ca9-731">Linn</span><span class="sxs-lookup"><span data-stu-id="63ca9-731">City</span></span>                  |
| <span data-ttu-id="63ca9-732">Maakond</span><span class="sxs-lookup"><span data-stu-id="63ca9-732">County</span></span>              | <span data-ttu-id="63ca9-733">Maakond (haldusüksus)</span><span class="sxs-lookup"><span data-stu-id="63ca9-733">County (Municipality)</span></span> |
| <span data-ttu-id="63ca9-734">Tänav</span><span class="sxs-lookup"><span data-stu-id="63ca9-734">Street</span></span>              | <span data-ttu-id="63ca9-735">Aadressirida 1</span><span class="sxs-lookup"><span data-stu-id="63ca9-735">Address Line 1</span></span>        |
| <span data-ttu-id="63ca9-736">Majanumber</span><span class="sxs-lookup"><span data-stu-id="63ca9-736">Street Number</span></span>       | <span data-ttu-id="63ca9-737">Aadressirida 2</span><span class="sxs-lookup"><span data-stu-id="63ca9-737">Address Line 2</span></span>        |
| <span data-ttu-id="63ca9-738">Hoone tähis</span><span class="sxs-lookup"><span data-stu-id="63ca9-738">Building Complement</span></span> | <span data-ttu-id="63ca9-739">Aadressirida 5</span><span class="sxs-lookup"><span data-stu-id="63ca9-739">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="63ca9-740">Passi number</span><span class="sxs-lookup"><span data-stu-id="63ca9-740">Passport number</span></span>

<span data-ttu-id="63ca9-741">Töötajad saavad deklareerida passi teavet.</span><span class="sxs-lookup"><span data-stu-id="63ca9-741">Employees can declare passport information.</span></span> <span data-ttu-id="63ca9-742">See teave on identifitseerimistüüpi **Pass** ja integreeritakse Dayforce’i töövõtja Mehhiko-teabe osana.</span><span class="sxs-lookup"><span data-stu-id="63ca9-742">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="63ca9-743">Identifitseerimistüüp = pass</span><span class="sxs-lookup"><span data-stu-id="63ca9-743">Identification Type = "Passport"</span></span>
- <span data-ttu-id="63ca9-744">Väljastamise kuupäev</span><span class="sxs-lookup"><span data-stu-id="63ca9-744">Issued Date</span></span>
- <span data-ttu-id="63ca9-745">Aegumiskuupäev</span><span class="sxs-lookup"><span data-stu-id="63ca9-745">Expiration Date</span></span>

<span data-ttu-id="63ca9-746">Töövõtjad saavad deklareerida mitu **Pass**-identifitseerimistüüpi ID-numbrit.</span><span class="sxs-lookup"><span data-stu-id="63ca9-746">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="63ca9-747">Dayforce’i integreeritakse siiski ainult praegune aktiivne passikirje.</span><span class="sxs-lookup"><span data-stu-id="63ca9-747">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="63ca9-748">Kui kõik passikirjed on aegunud, siis integreeritakse Dayforce’i pass, mis väljastati viimasena.</span><span class="sxs-lookup"><span data-stu-id="63ca9-748">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]