---
title: Dayforce’iga integreerimise konfigureerimine
description: Rakenduste Microsoft Dynamics 365 Human Resources ja Ceridian Dayforce vaheline integratsioon oleneb mitmest selles teemas kirjeldatavast konfiguratsioonietapist. Enne palgatöötluse tegemist peate konfigureerima integratsiooni nii rakenduses Human Resources kui ka Dayforce.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: c66ec772ea66732e042f50081f04a6569852f211
ms.sourcegitcommit: ba340f836e472f13f263dec46a49847c788fca44
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 06/04/2020
ms.locfileid: "3431287"
---
# <a name="configure-integration-with-dayforce"></a><span data-ttu-id="2bd0b-104">Dayforce’iga integreerimise konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-104">Configure integration with Dayforce</span></span>

<span data-ttu-id="2bd0b-105">Rakenduste Microsoft Dynamics 365 Human Resources ja Ceridian Dayforce vaheline integratsioon oleneb mitmest selles teemas kirjeldatavast konfiguratsioonietapist.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-105">The integration between Microsoft Dynamics 365 Human Resources and Ceridian Dayforce relies on several configuration steps that are described in this article.</span></span> <span data-ttu-id="2bd0b-106">Enne palgatöötluse tegemist peate konfigureerima integratsiooni nii rakenduses Human Resources kui ka Dayforce.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-106">You must configure the integration in both Human Resources and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="2bd0b-107">Kui te kasutate palgatöötluste tegemiseks teenust, nagu Dayforce, siis peate rakenduses Human Resources integratsiooni lubama.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-107">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Human Resources.</span></span> <span data-ttu-id="2bd0b-108">Integratsiooni jaoks on rakendusest Human Resources vaja teatud andmeid.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-108">The integration requires specific data from Human Resources.</span></span> <span data-ttu-id="2bd0b-109">Seega peate kinnitama, et Dayforce’iga vastendatud andmed on rakenduses Human Resources konfigureeritud viisil, mis lubab integratsiooni.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-109">Therefore, you must verify that data that is mapped to Dayforce is configured in Human Resources in a manner that supports the integration.</span></span> <span data-ttu-id="2bd0b-110">Integratsioon kasutab järgmisi üldisi andmekategooriaid.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-110">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="2bd0b-111">Inimressursside andmed</span><span class="sxs-lookup"><span data-stu-id="2bd0b-111">Human resources data</span></span>
- <span data-ttu-id="2bd0b-112">Hüvituse andmed</span><span class="sxs-lookup"><span data-stu-id="2bd0b-112">Compensation data</span></span>
- <span data-ttu-id="2bd0b-113">Palgaandmed, näiteks palgatsüklid, makseperioodid ja tulukoodid</span><span class="sxs-lookup"><span data-stu-id="2bd0b-113">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="2bd0b-114">Töötaja andmed</span><span class="sxs-lookup"><span data-stu-id="2bd0b-114">Worker data</span></span>

<span data-ttu-id="2bd0b-115">Teemas kirjeldatakse integratsiooni lubamiseks vajalikke etappe.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-115">This article describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="2bd0b-116">Samuti selgitatakse integratsiooni jaoks vajalikke andmetüüpe ja konfigureerimise üksikasju.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-116">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="2bd0b-117">Integratsiooni lubamine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-117">Enable the integration</span></span>

<span data-ttu-id="2bd0b-118">Dayforce’iga ühendamiseks peate rakenduses Human Resources sisse lülitama integratsiooni ja sisestama konfigureerimisteabe.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-118">In Human Resources, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="2bd0b-119">Kui soovite, et loodav pearaamatu kanne imporditaks rakendusse Microsoft Dynamics 365 Finance, siis peate seadistama Microsoft Azure’i salvestuskonto ja sisestama Azure’i salvestusruumi ühendusstringi rakendusse Finance.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-119">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="2bd0b-120">Integratsiooni sisselülitamiseks rakenduses Human Resources järgige neid samme.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-120">To turn on the integration in Human Resources, follow these steps.</span></span>

1. <span data-ttu-id="2bd0b-121">Valige lehelt **Süsteemihaldus** suvand **Integratsiooni konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-121">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="2bd0b-122">Sisestage turvalise failiedastusprotokolli File Transfer Protocol (FTP) lõpp-punkt ja turvalise FTP kausta tee.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-122">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="2bd0b-123">Sisestage selle kasutaja kasutajanimi ja parool, kellel on vaja juurdepääsu turvalise FTP lõpp-punktile ja kausta teele.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-123">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="2bd0b-124">Testige ühendust vajaduse järgi ja määrake suvand **Palgaarvestuse integratsiooni lubamine** olekule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-124">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="2bd0b-125">Kui integratsioon on sisse lülitatud, luuakse andmete ekspordipakett ja -failid ning määratakse sagedus.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-125">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="2bd0b-126">Vajaduse korral saate seda sagedust muuta.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-126">You can change this frequency as you require.</span></span>

<span data-ttu-id="2bd0b-127">Lisateavet Azure’i talletamiskontode ja Azure’i salvestusruumi ühendusstringide kohta leiate järgmistest Azure’i teemadest.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-127">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure articles:</span></span>

- [<span data-ttu-id="2bd0b-128">Azure’i salvestuskontod</span><span class="sxs-lookup"><span data-stu-id="2bd0b-128">About Azure storage accounts</span></span>](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="2bd0b-129">Azure’i salvestusruumi ühendusstringide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-129">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="2bd0b-130">Tehnilised üksikasjad, kui palga integratsioon on lubatud</span><span class="sxs-lookup"><span data-stu-id="2bd0b-130">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="2bd0b-131">Palga integreerimise sisselülitamisel on kaks peamist mõju.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-131">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="2bd0b-132">Luuakse andmete ekspordi projekt nimega "Palga integreerimise eksport".</span><span class="sxs-lookup"><span data-stu-id="2bd0b-132">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="2bd0b-133">See projekt sisaldab palga integreerimise jaoks nõutavaid üksusi ja välju.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-133">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="2bd0b-134">Projekti uurimiseks avage **Süsteemihaldus**, valige paan **Andmehaldus** ja avage projektiloendist andmete projekt.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-134">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="2bd0b-135">See pakett-töö käivitab andmete eksportimise projekti, krüptib tulemuste andmete paketi ja edastab andmete paketi faili SFTP-lõpp-punktile, mis on konfigureeritud kuval **integratsiooni konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-135">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="2bd0b-136">SFTP-lõpp-punkti edastatud andmete pakett krüptitakse, kasutades võtit, mis on paketile kordumatu.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-136">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="2bd0b-137">Võti on Azure võtmehoidlas, mis on kättesaadav ainult Ceridianile.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-137">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="2bd0b-138">Andmebaasi sisu ei saa dekrüptida ja uurida.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-138">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="2bd0b-139">Kui teil on vaja uurida andmepaketi sisu, peate eksportima projekti "Palga integreerimise eksport" käsitsi, selle alla laadima ja seejärel avama.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-139">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="2bd0b-140">Käsitsi eksportimine ei rakenda krüptimist ega edasta paketti.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-140">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="2bd0b-141">Andmete konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-141">Configure your data</span></span> 

<span data-ttu-id="2bd0b-142">Palgaarvestuse töötlemiseks peate konfigureerima personaliandmeid rakenduses Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-142">To process payroll, you must configure human resource data in Human Resources.</span></span> <span data-ttu-id="2bd0b-143">Peate määratlema organisatsiooni andmeid nagu tööd ja ametikohad, samuti teavet soodustuste ning kompensatsioonide kohta.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-143">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="2bd0b-144">Selle teabe hulka kuulub töövõtja palgaandmete loomiseks vajalik teave töösuhte, palga ja mahaarvamiste kohta.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-144">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="2bd0b-145">Personaliandmed</span><span class="sxs-lookup"><span data-stu-id="2bd0b-145">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="2bd0b-146">Soodustused</span><span class="sxs-lookup"><span data-stu-id="2bd0b-146">Benefits</span></span> 

<span data-ttu-id="2bd0b-147">Inimressursid pakuvad tööriistu, mis aitavad seadistada ja hallata soodustusi, mahaarvamisi ning töötajate hüvitusplaane, mida organisatsioon oma töötajatele pakub või nende puhul töötleb.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-147">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="2bd0b-148">Soodustuste loomisel pidage meeles järgmisi Dayforce’is kasutatavaid andmeid ja konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-148">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="2bd0b-149">Soodustusplaanid</span><span class="sxs-lookup"><span data-stu-id="2bd0b-149">Benefit plans</span></span>

- <span data-ttu-id="2bd0b-150">Plaan (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-150">Plan (required)</span></span>
- <span data-ttu-id="2bd0b-151">Tüüp (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-151">Type (required)</span></span>
- <span data-ttu-id="2bd0b-152">Palga mõju (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-152">Payroll impact (required)</span></span>
- <span data-ttu-id="2bd0b-153">Võlgnevuste sissenõudmine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-153">Recover arrears</span></span>
- <span data-ttu-id="2bd0b-154">Mahaarvamismeetod</span><span class="sxs-lookup"><span data-stu-id="2bd0b-154">Deduction method</span></span>
- <span data-ttu-id="2bd0b-155">Mahaarvamise prioriteet</span><span class="sxs-lookup"><span data-stu-id="2bd0b-155">Deduction priority</span></span>
- <span data-ttu-id="2bd0b-156">Perioodi piiramine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-156">Limit period</span></span>
- <span data-ttu-id="2bd0b-157">Piirsumma</span><span class="sxs-lookup"><span data-stu-id="2bd0b-157">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="2bd0b-158">Soodustused</span><span class="sxs-lookup"><span data-stu-id="2bd0b-158">Benefits</span></span>

- <span data-ttu-id="2bd0b-159">Plaan (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-159">Plan (required)</span></span>
- <span data-ttu-id="2bd0b-160">Tüüp (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-160">Type (required)</span></span>
- <span data-ttu-id="2bd0b-161">Suvand (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-161">Option (required)</span></span>
- <span data-ttu-id="2bd0b-162">Soodustuse ID (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-162">Benefit ID (required)</span></span>
- <span data-ttu-id="2bd0b-163">Sagedus</span><span class="sxs-lookup"><span data-stu-id="2bd0b-163">Frequency</span></span>
- <span data-ttu-id="2bd0b-164">Alus</span><span class="sxs-lookup"><span data-stu-id="2bd0b-164">Basis</span></span>
- <span data-ttu-id="2bd0b-165">Summa või määr</span><span class="sxs-lookup"><span data-stu-id="2bd0b-165">Amount or rate</span></span>
- <span data-ttu-id="2bd0b-166">Tulukood</span><span class="sxs-lookup"><span data-stu-id="2bd0b-166">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="2bd0b-167">Toetatud sagedused</span><span class="sxs-lookup"><span data-stu-id="2bd0b-167">Supported frequencies</span></span> 

- <span data-ttu-id="2bd0b-168">Iga nädal</span><span class="sxs-lookup"><span data-stu-id="2bd0b-168">Weekly</span></span>
- <span data-ttu-id="2bd0b-169">Kahe nädala tagant</span><span class="sxs-lookup"><span data-stu-id="2bd0b-169">Bi-weekly</span></span>
- <span data-ttu-id="2bd0b-170">Iga poole kuu tagant</span><span class="sxs-lookup"><span data-stu-id="2bd0b-170">Semi-monthly</span></span>
- <span data-ttu-id="2bd0b-171">Kord kuus</span><span class="sxs-lookup"><span data-stu-id="2bd0b-171">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="2bd0b-172">Toetatud alused</span><span class="sxs-lookup"><span data-stu-id="2bd0b-172">Supported bases</span></span> 

- <span data-ttu-id="2bd0b-173">Fikseeritud summa</span><span class="sxs-lookup"><span data-stu-id="2bd0b-173">Fixed amount</span></span>
- <span data-ttu-id="2bd0b-174">Tulu protsent</span><span class="sxs-lookup"><span data-stu-id="2bd0b-174">Percent of earnings</span></span>
- <span data-ttu-id="2bd0b-175">Produktiivsed tunnid</span><span class="sxs-lookup"><span data-stu-id="2bd0b-175">Productive hours</span></span>

<span data-ttu-id="2bd0b-176">Dayforce loob järgmised mahaarvamised palga mõju alusel, mis on määratletud soodustusplaanis.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-176">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="2bd0b-177">Valik rakenduses Human Resources</span><span class="sxs-lookup"><span data-stu-id="2bd0b-177">Selection in Human Resources</span></span>        | <span data-ttu-id="2bd0b-178">Tulemus rakenduses Dayforce</span><span class="sxs-lookup"><span data-stu-id="2bd0b-178">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="2bd0b-179">Puudub</span><span class="sxs-lookup"><span data-stu-id="2bd0b-179">None</span></span>                       | <span data-ttu-id="2bd0b-180">Mahaarvamist ei looda.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-180">No deduction is created.</span></span>                      |
| <span data-ttu-id="2bd0b-181">Ainult mahaarvamine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-181">Deduction only</span></span>             | <span data-ttu-id="2bd0b-182">Luuakse töövõtja mahaarvamine.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-182">An employee deduction is created.</span></span>             |
| <span data-ttu-id="2bd0b-183">Ainult lisamine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-183">Contribution only</span></span>          | <span data-ttu-id="2bd0b-184">Luuakse tööandja mahaarvamine.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-184">An employer deduction is created.</span></span>             |
| <span data-ttu-id="2bd0b-185">Mahaarvamine ja lisamine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-185">Deduction and contribution</span></span> | <span data-ttu-id="2bd0b-186">Luuakse töövõtja ja tööandja mahaarvamised.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-186">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="2bd0b-187">Lisateavet soodustusprogrammi määratlemise ja haldamise kohta vaadake järgmistest artiklitest.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-187">For more information about how to define and manage a benefits program, see the following articles:</span></span>

- [<span data-ttu-id="2bd0b-188">Töötaja soodustuste programmi pakkumine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-188">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="2bd0b-189">Uue soodustuse loomine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-189">Create a new benefit</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="2bd0b-190">Soodustuskõlblikkuse reeglite ja poliitikate määratlemine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-190">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="2bd0b-191">Töötajate soodustuste registreerimine ja eemaldamine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-191">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="2bd0b-192">Hüvitus</span><span class="sxs-lookup"><span data-stu-id="2bd0b-192">Compensation</span></span> 

<span data-ttu-id="2bd0b-193">Hüvituste haldust kasutatakse põhitasu ja preemiate jagamise juhtimiseks.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-193">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="2bd0b-194">Töötaja fikseeritud põhipalga ja preemia tõusu juhitakse põhipalga plaanide kaudu.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-194">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="2bd0b-195">Lisatasude (nt preemiate, tulemustasude aktsiate eelismüügi ja toetuste ning ühekordsete preemiate) maksmist juhitakse ergutussüsteemi plaanide kaudu.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-195">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="2bd0b-196">Dayforce kasutab hüvituse teavet töövõtja tunni- või aastamäära arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-196">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="2bd0b-197">Nõutavad on põhipalgaplaanid ja palgamäära teisendamised.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-197">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="2bd0b-198">Töövõtjad peavad olema seotud põhipalgaplaaniga.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-198">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="2bd0b-199">Lisateavet hüvitusplaanide kohta vaadake järgmistest artiklitest.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-199">For more information about compensation plans, see the following articles:</span></span>

- [<span data-ttu-id="2bd0b-200">Põhipalga plaanide loomine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-200">Create fixed compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="2bd0b-201">Ergutussüsteemi plaanide loomine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-201">Create variable compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="2bd0b-202">Palga/hüvituse struktuuri ja plaanide arendamine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-202">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="2bd0b-203">Hüvitusprotsess</span><span class="sxs-lookup"><span data-stu-id="2bd0b-203">Process compensation</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="2bd0b-204">Hüvitusprotsessi määratlemine ja tulemuste arvutamine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-204">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="2bd0b-205">Töötaja liitmine põhipalga plaaniga</span><span class="sxs-lookup"><span data-stu-id="2bd0b-205">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="2bd0b-206">Töötaja liitmine tulemustasu plaaniga</span><span class="sxs-lookup"><span data-stu-id="2bd0b-206">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="2bd0b-207">Tööd</span><span class="sxs-lookup"><span data-stu-id="2bd0b-207">Jobs</span></span> 

<span data-ttu-id="2bd0b-208">Töö on tööd tegeva isiku jaoks nõutavate ülesannete ja vastutuste kogum.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-208">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="2bd0b-209">Lisateavet vt järgmistest artiklitest.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-209">For more information, see the following articles:</span></span>

- [<span data-ttu-id="2bd0b-210">Töö komponentide seadistamine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-210">Setting up the components of a job</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="2bd0b-211">Uute tööde määratlemine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-211">Define new jobs</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="2bd0b-212">Ametikohad</span><span class="sxs-lookup"><span data-stu-id="2bd0b-212">Positions</span></span>

<span data-ttu-id="2bd0b-213">Ametikoht on töökoha üksik eksemplar.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-213">A position is an individual instance of a job.</span></span> <span data-ttu-id="2bd0b-214">Näiteks on ametikoht „müügijuht (Ida)” vaid üks tööga „müügijuht” seostatud ametikohti.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-214">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="2bd0b-215">Ametikoht kuulub osakonna alla.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-215">A position exists in a department.</span></span> <span data-ttu-id="2bd0b-216">Iga ametikohaga saab seostada vaid ühte töötajat.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-216">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="2bd0b-217">Ametikohtade seadistamisel pidage meeles järgmisi andmeid ja konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-217">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="2bd0b-218">Ametikoht (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-218">Position (required)</span></span>
- <span data-ttu-id="2bd0b-219">Kirjeldus (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-219">Description (required)</span></span>
- <span data-ttu-id="2bd0b-220">Töö (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-220">Job (required)</span></span>
- <span data-ttu-id="2bd0b-221">Osakond (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-221">Department (required)</span></span>
- <span data-ttu-id="2bd0b-222">Ametikoha tüüp (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-222">Position type (required)</span></span>
- <span data-ttu-id="2bd0b-223">Täistööaja vaste</span><span class="sxs-lookup"><span data-stu-id="2bd0b-223">Full-time equivalent</span></span>
- <span data-ttu-id="2bd0b-224">Iga-aastased regulaarsed tunnid (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-224">Annual regular hours (required)</span></span>
- <span data-ttu-id="2bd0b-225">Maksja juriidiline isik (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-225">Paid by legal entity (required)</span></span>
- <span data-ttu-id="2bd0b-226">Palgatsükkel (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-226">Pay cycle (required)</span></span>
- <span data-ttu-id="2bd0b-227">Vaike-finantsdimensioonid – kulukeskus (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-227">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="2bd0b-228">Töötaja määramine – töötaja, määramise algus, määramise lõpp, põhjuse kood</span><span class="sxs-lookup"><span data-stu-id="2bd0b-228">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="2bd0b-229">Kui ühes osakonnas on sama tööga seotud mitu ametikohta, siis konsolideeritakse need rakenduses Dayforce üheks ametikohaks.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-229">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="2bd0b-230">Lisateavet vt järgmistest artiklitest.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-230">For more information, see the following articles:</span></span>

- [<span data-ttu-id="2bd0b-231">Tööjõu korraldamine osakondade, tööde ja ametikohtade abil</span><span class="sxs-lookup"><span data-stu-id="2bd0b-231">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="2bd0b-232">Ametikohtade seadistamine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-232">Set up positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="2bd0b-233">Osakonnad</span><span class="sxs-lookup"><span data-stu-id="2bd0b-233">Departments</span></span>

<span data-ttu-id="2bd0b-234">Osakond on tootmisüksus, mis esindab organisatsiooni kategooriat või funktsionaalset ala.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-234">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="2bd0b-235">Osakond vastutab organisatsiooni kindla valdkonna eest, nagu müük, raamatupidamine või inimressursid.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-235">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="2bd0b-236">Saate osakondi kasutada funktsionaalsete alade aruannete koostamiseks.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-236">You can use departments to report on functional areas.</span></span> <span data-ttu-id="2bd0b-237">Osakonnad võivad vastutada kasumi ja kahjumi eest.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-237">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="2bd0b-238">Lisateavet vt järgmistest artiklitest.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-238">For more information, see the following articles:</span></span>

- [<span data-ttu-id="2bd0b-239">Osakonna loomine ja selle seostamine osakonnahierarhiaga</span><span class="sxs-lookup"><span data-stu-id="2bd0b-239">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="2bd0b-240">Uute osakondade määratlemine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-240">Define new departments</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="2bd0b-241">Palgatsüklid ja makseperioodid</span><span class="sxs-lookup"><span data-stu-id="2bd0b-241">Pay cycles and pay periods</span></span>

<span data-ttu-id="2bd0b-242">Palgatsükkel määrab, kui tihti palgamaksmine toimub ja konkreetsed päevad, millal töötajatele palka makstakse.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-242">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="2bd0b-243">Näiteks võib palgatsükli sageduseks olla üks kuu ja töövõtjatele makstakse seega kuu viimasel päeval.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-243">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="2bd0b-244">Või kui palgatsükli sageduseks on üks nädal, siis makstakse töövõtjatele näiteks teisipäeviti pärast makseperioodi lõppu.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-244">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="2bd0b-245">Palgatsükleid määratakse ametikohtadele selleks, et määrata, millal nendel ametikohtadel töötavatele töötajatele palka makstakse.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-245">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="2bd0b-246">Pärast palgatsüklite loomist saate iga tsükli jaoks luua makseperioodid.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-246">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="2bd0b-247">Igal makseperioodil on makse vaikekuupäev, mis põhineb teie sisestatud teabel.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-247">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="2bd0b-248">Siiski saate erandite käsitlemiseks makseperioodi makse vaikekuupäeva muuta, näiteks kui maksekuupäev satub riigipühale.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-248">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="2bd0b-249">Dayforce kasutab järgmist teavet.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-249">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="2bd0b-250">Palgatsükkel (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-250">Pay cycle (required)</span></span>
- <span data-ttu-id="2bd0b-251">Palgatsükli sagedus (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-251">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="2bd0b-252">Perioodi alguskuupäev (esimene makseperiood on kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-252">Period start date (first pay period required)</span></span>
- <span data-ttu-id="2bd0b-253">Makse vaikekuupäev (esimene makseperiood on kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-253">Default payment date (first pay period required)</span></span>

<span data-ttu-id="2bd0b-254">See teave on integreeritud rakendusse Dayforce palgagruppidena ja on iga palgatsükli puhul eraldatud riigi või regiooniga.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-254">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="2bd0b-255">Enne integreerimist peab olema loodud vähemalt üks makseperiood.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-255">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="2bd0b-256">Dayforce loob palgagrupi kalendrid ja maksekuupäevad rakenduses Human Resources määratletud esimese makseperioodi alguskuupäeva ja makse vaikekuupäeva põhjal.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-256">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Human Resources.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="2bd0b-257">Tulukoodid</span><span class="sxs-lookup"><span data-stu-id="2bd0b-257">Earning codes</span></span>

<span data-ttu-id="2bd0b-258">Tulukoodid määratlevad kordumatult igat tüüpi tulud, mida töötajad saavad.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-258">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="2bd0b-259">Koodidel on mitmeid tuludega seotud parameetreid, näiteks raamatupidamisreeglid, maksuseadused, aruandluse nõuded ja brutosumma võime.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-259">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="2bd0b-260">Dayforce kasutab järgmist teavet.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-260">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="2bd0b-261">Tulukood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-261">Earning Code (required)</span></span>
- <span data-ttu-id="2bd0b-262">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="2bd0b-262">Description</span></span>
- <span data-ttu-id="2bd0b-263">Mõõtühik</span><span class="sxs-lookup"><span data-stu-id="2bd0b-263">Unit of measure</span></span>
- <span data-ttu-id="2bd0b-264">Produktiivne</span><span class="sxs-lookup"><span data-stu-id="2bd0b-264">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="2bd0b-265">Töötaja andmed</span><span class="sxs-lookup"><span data-stu-id="2bd0b-265">Worker data</span></span>

<span data-ttu-id="2bd0b-266">Töötajate kirjed on tähtsad teie personali- ja palgasüsteemide jaoks.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-266">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="2bd0b-267">Teie sisestatud teavet saab kasutada töötajate ja nende isikliku teabe jälgimiseks.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-267">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="2bd0b-268">Töötajate kohta saate hallata järgmist teavet.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-268">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="2bd0b-269">**Üldine** – töötaja põhiteave, näiteks kontaktteave, demograafiline teave, tuvastamisteave, perekonna teave, sõjaväeteenistuse olek, välislähetuse teave ja isiklikud ning lähedase isiku kontaktandmed.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-269">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="2bd0b-270">**Töösuhe** – töötaja töösuhte teave, näiteks töötaja palganud ettevõte või organisatsioon, määratud ametikoht, algus- ja lõppkuupäevad, töökõlblikkus, töölevõtutingimused, pension, puhkus ja ümberpaigutuse teave.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-270">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="2bd0b-271">**Puhkused ja puudumised** – teave töötaja puudumiste kohta, näiteks töögraafikud, puudumiskanded ja puudumise seadistamine.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-271">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="2bd0b-272">**Hüvitus ja palk** – teave töötaja hüvitusplaanide ja palgaarvestuse kohta, näiteks liitutud plaanid, preemiad, tööviljakus, komisjonitasu, maksuteave, pensionileminek ning palgast mahaarvamised.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-272">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="2bd0b-273">Töötaja teabe sisestamisel pidage meeles järgmisi Dayforce’is kasutatavaid andmeid ja konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-273">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="2bd0b-274">Üldteave</span><span class="sxs-lookup"><span data-stu-id="2bd0b-274">General information</span></span>

- <span data-ttu-id="2bd0b-275">Töötaja number (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-275">Personnel number (required)</span></span>
- <span data-ttu-id="2bd0b-276">Eesnimi (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-276">First name (required)</span></span>
- <span data-ttu-id="2bd0b-277">Perekonnanimi (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-277">Last name (required)</span></span>
- <span data-ttu-id="2bd0b-278">Teine eesnimi</span><span class="sxs-lookup"><span data-stu-id="2bd0b-278">Middle name</span></span>
- <span data-ttu-id="2bd0b-279">Staaž kuupäeval</span><span class="sxs-lookup"><span data-stu-id="2bd0b-279">Seniority date</span></span>
- <span data-ttu-id="2bd0b-280">Tuntud kui</span><span class="sxs-lookup"><span data-stu-id="2bd0b-280">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="2bd0b-281">Isikuandmed</span><span class="sxs-lookup"><span data-stu-id="2bd0b-281">Personal information</span></span>

- <span data-ttu-id="2bd0b-282">Perekonnaseis (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-282">Marital status (required)</span></span>
- <span data-ttu-id="2bd0b-283">Sünnikuupäev (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-283">Birth date (required)</span></span>
- <span data-ttu-id="2bd0b-284">Sugu (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-284">Gender (required)</span></span>
- <span data-ttu-id="2bd0b-285">Puudega isik</span><span class="sxs-lookup"><span data-stu-id="2bd0b-285">Person with disabilities</span></span>
- <span data-ttu-id="2bd0b-286">Kodakondsusjärgse riigi regioon (ainult Mehhiko puhul)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-286">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="2bd0b-287">Aadressiteave</span><span class="sxs-lookup"><span data-stu-id="2bd0b-287">Address information</span></span>

- <span data-ttu-id="2bd0b-288">Tänava nimi ja hoone number (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-288">Primary (required)</span></span>
- <span data-ttu-id="2bd0b-289">Riik/regioon (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-289">Country/region (required)</span></span>
- <span data-ttu-id="2bd0b-290">Sihtnumber (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-290">Postal code (required)</span></span>
- <span data-ttu-id="2bd0b-291">Tänava number (kohustuslik) (ainult Mehhiko puhul)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-291">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="2bd0b-292">Hoone tähis (ainult Mehhiko puhul)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-292">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="2bd0b-293">Linn (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-293">City (required)</span></span>
- <span data-ttu-id="2bd0b-294">Osariik (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-294">State (required)</span></span>
- <span data-ttu-id="2bd0b-295">Maakond (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-295">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="2bd0b-296">Kontaktteave</span><span class="sxs-lookup"><span data-stu-id="2bd0b-296">Contact information</span></span> 

- <span data-ttu-id="2bd0b-297">Tänava nimi ja hoone number (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-297">Primary (required)</span></span>
- <span data-ttu-id="2bd0b-298">Kontaktnumber (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-298">Contact number (required)</span></span>
- <span data-ttu-id="2bd0b-299">Sisetelefon</span><span class="sxs-lookup"><span data-stu-id="2bd0b-299">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="2bd0b-300">Palgateave ja tulukoodid</span><span class="sxs-lookup"><span data-stu-id="2bd0b-300">Payroll information and earning codes</span></span>

<span data-ttu-id="2bd0b-301">Töövõtjatele võidakse määrata teatud maksesagedusega konkreetsed tulud ja neil võivad olla eelistatud makseviisid.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-301">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="2bd0b-302">Nende eelistuste ja sätete kasutamise tagamiseks kasutatakse Dayforce’is järgmisi välju.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-302">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="2bd0b-303">Tulukoodid</span><span class="sxs-lookup"><span data-stu-id="2bd0b-303">Earning codes</span></span>

- <span data-ttu-id="2bd0b-304">Ametikoht (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-304">Position (required)</span></span>
- <span data-ttu-id="2bd0b-305">Tulukood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-305">Earning Code (required)</span></span>
- <span data-ttu-id="2bd0b-306">Maksesagedus (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-306">Frequency (required)</span></span>
- <span data-ttu-id="2bd0b-307">Summa (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-307">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="2bd0b-308">Palgateave</span><span class="sxs-lookup"><span data-stu-id="2bd0b-308">Payroll information</span></span>

- <span data-ttu-id="2bd0b-309">Makseviis</span><span class="sxs-lookup"><span data-stu-id="2bd0b-309">Payment Method</span></span>
- <span data-ttu-id="2bd0b-310">Majanduspiirkond (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-310">Economic Region (required)</span></span>
- <span data-ttu-id="2bd0b-311">Töövõtja soodustuste ID</span><span class="sxs-lookup"><span data-stu-id="2bd0b-311">Employee Benefits ID</span></span>
- <span data-ttu-id="2bd0b-312">Riiklik isikukood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-312">National ID Number (required)</span></span>
- <span data-ttu-id="2bd0b-313">Sõjaväeteenistuse number</span><span class="sxs-lookup"><span data-stu-id="2bd0b-313">Military Service Number</span></span>
- <span data-ttu-id="2bd0b-314">Vahetuse ID (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-314">Shift ID (required)</span></span>
- <span data-ttu-id="2bd0b-315">Maksukood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-315">Tax Number (required)</span></span>
- <span data-ttu-id="2bd0b-316">Ühingu ID (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-316">Union ID (required)</span></span>
- <span data-ttu-id="2bd0b-317">Tööpäeva ID (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-317">Work Day ID (required)</span></span>
- <span data-ttu-id="2bd0b-318">Tööloa number</span><span class="sxs-lookup"><span data-stu-id="2bd0b-318">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="2bd0b-319">Mehhiko toetab järgmisi makseviise: **sularaha**, **tšekk** (ettevõtte füüsiline tšekk) ja **elektrooniline makse**.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-319">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="2bd0b-320">Kui makseviisi pole määratud, kasutatakse vaikevalikut **tšekk**.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-320">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="2bd0b-321">Töösuhte üksikasjad</span><span class="sxs-lookup"><span data-stu-id="2bd0b-321">Employment details</span></span>

<span data-ttu-id="2bd0b-322">Töösuhte üksikasjade ajalugu on põhiline teave, millest tuletatakse rakenduses Dayforce töövõtja palkamise, töösuhte lõpetamise ja uuesti palkamise olekud.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-322">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="2bd0b-323">Dayforce toetab korraga ainult ühte aktiivset töösuhte kirjet.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-323">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="2bd0b-324">Töösuhte alguskuupäev (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-324">Employment start date (required)</span></span>
- <span data-ttu-id="2bd0b-325">Töösuhte lõppkuupäev</span><span class="sxs-lookup"><span data-stu-id="2bd0b-325">Employment end date</span></span>
- <span data-ttu-id="2bd0b-326">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="2bd0b-326">Start date</span></span>
- <span data-ttu-id="2bd0b-327">Korrigeeritud alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="2bd0b-327">Adjusted start date</span></span>
- <span data-ttu-id="2bd0b-328">Töösuhte lõpetamise kuupäev (kohustuslik lõpetamisel)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-328">Termination date (required upon termination)</span></span>
- <span data-ttu-id="2bd0b-329">Töösuhte lõpetamise põhjus (kohustuslik lõpetamisel)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-329">Termination reason (required upon termination)</span></span>

<span data-ttu-id="2bd0b-330">Töövõtja tähtsaimad kuupäevad tuletatakse järgmisest teabest.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-330">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="2bd0b-331">Inimressursid</span><span class="sxs-lookup"><span data-stu-id="2bd0b-331">Human Resources</span></span>                | <span data-ttu-id="2bd0b-332">Dayforce</span><span class="sxs-lookup"><span data-stu-id="2bd0b-332">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bd0b-333">Kõige värskem palkamise kuupäev</span><span class="sxs-lookup"><span data-stu-id="2bd0b-333">Most recent hire date</span></span> | <span data-ttu-id="2bd0b-334">Praeguse lõpetamata töösuhte ajalookirje alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="2bd0b-334">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="2bd0b-335">Lõpetamiskuupäev</span><span class="sxs-lookup"><span data-stu-id="2bd0b-335">Termination date</span></span>      | <span data-ttu-id="2bd0b-336">Praeguse lõpetamata töösuhte ajalookirje lõpetamise kuupäev</span><span class="sxs-lookup"><span data-stu-id="2bd0b-336">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="2bd0b-337">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="2bd0b-337">Start date</span></span>            | <span data-ttu-id="2bd0b-338">Korrigeeritud alguskuupäev, alguskuupäev või praeguse passiivse töösuhte ajalookirje alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="2bd0b-338">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="2bd0b-339">Palkamise algne kuupäev</span><span class="sxs-lookup"><span data-stu-id="2bd0b-339">Original hire date</span></span>    | <span data-ttu-id="2bd0b-340">Varaseima töösuhte ajalookirje alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="2bd0b-340">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="2bd0b-341">Hüvitus</span><span class="sxs-lookup"><span data-stu-id="2bd0b-341">Compensation</span></span>

<span data-ttu-id="2bd0b-342">Tööhõiveperioodi jooksul peab iga töövõtja peamise ametikohaga olema seotud põhipalgaplaan.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-342">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="2bd0b-343">See periood algab kuupäeval, mil töövõtja palgati (või töösuhte alguskuupäeval), ja jätkub kuni töösuhte lõpetamiseni.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-343">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="2bd0b-344">Kehtivuse algus (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-344">Effective Date (required)</span></span>
- <span data-ttu-id="2bd0b-345">Aegumiskuupäev</span><span class="sxs-lookup"><span data-stu-id="2bd0b-345">Expiration date</span></span>
- <span data-ttu-id="2bd0b-346">Palgamäär (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-346">Pay Rate (required)</span></span>
- <span data-ttu-id="2bd0b-347">Palgamäära teisendamised (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-347">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="2bd0b-348">Aastane vaste (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-348">Annual equivalent (required)</span></span>
- <span data-ttu-id="2bd0b-349">Tunnine vaste (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-349">Hourly equivalent (required)</span></span>

<span data-ttu-id="2bd0b-350">Kui tunnimääraga töövõtjal on mitu ametikohta, siis imporditakse peamise ametikoha põhipalk rakendusse Dayforce töövõtja taseme põhimäärana/-palgana.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-350">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="2bd0b-351">Teiseste ametikohtade puhul salvestatakse Dayforce’is tunnimäär vastava ametikoha jaoks.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-351">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="2bd0b-352">Kui kuupalgaga töötajal on mitu ametikohta, siis kasutatakse töövõtja taseme põhimäärana/-palgana kõikide aktiivsete ametikohtade tuletatud kumulatiivset tunnimäära ja aastapalka.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-352">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="2bd0b-353">ID-numbrid</span><span class="sxs-lookup"><span data-stu-id="2bd0b-353">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="2bd0b-354">Isiku identifikaator</span><span class="sxs-lookup"><span data-stu-id="2bd0b-354">Social Security identifier</span></span> 

<span data-ttu-id="2bd0b-355">Igal töövõtjal peab olema üks peamine identifikaator.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-355">Every employee must have one primary identifier.</span></span> <span data-ttu-id="2bd0b-356">Identifikaator peab olema isikukoodi- ehk **SSN**-tüüpi.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-356">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="2bd0b-357">Rakenduses Dayforce tuletatakse see automaatselt töövõtja isiku identifikaatorina, mis on palkamiseks vajalik.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-357">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="2bd0b-358">Peamine isikukood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-358">Primary (required)</span></span>
- <span data-ttu-id="2bd0b-359">ID tüüp = SSN</span><span class="sxs-lookup"><span data-stu-id="2bd0b-359">Identification Type = "SSN"</span></span>
- <span data-ttu-id="2bd0b-360">Väljastamise kuupäev</span><span class="sxs-lookup"><span data-stu-id="2bd0b-360">Issued Date</span></span>
- <span data-ttu-id="2bd0b-361">Aegumiskuupäev</span><span class="sxs-lookup"><span data-stu-id="2bd0b-361">Expiration Date</span></span>

<span data-ttu-id="2bd0b-362">Töövõtjad saavad deklareerida mitu **SSN**-identifitseerimistüüpi ID-numbrit.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-362">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="2bd0b-363">Dayforce’i integreeritakse vaid tähistusega **Peamine** kirje, olenemata sellest, kas number on aktiivne või aegunud.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-363">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="2bd0b-364">Pangakontod ja väljamaksed</span><span class="sxs-lookup"><span data-stu-id="2bd0b-364">Bank accounts and disbursements</span></span>

<span data-ttu-id="2bd0b-365">Iga töötaja jaoks, kes soovib oma palka pangakonto ülekandena kätte saada, tuleb sisestada kehtiv pangakonto teave.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-365">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="2bd0b-366">Inimressursid</span><span class="sxs-lookup"><span data-stu-id="2bd0b-366">Human Resources</span></span>                         | <span data-ttu-id="2bd0b-367">Dayforce</span><span class="sxs-lookup"><span data-stu-id="2bd0b-367">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2bd0b-368">Pangakonto number (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-368">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="2bd0b-369">SWIFT-kood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-369">SWIFT code (required)</span></span>          | <span data-ttu-id="2bd0b-370">Välja **Panga ID** kasutatakse palgaarvestuse töötlemiseks Mehhikos.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-370">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="2bd0b-371">Filiaali kood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-371">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="2bd0b-372">Pangakonto tüüp (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-372">Bank account type (required)</span></span>   | <span data-ttu-id="2bd0b-373">Välja **Konto tüüp** kasutatakse palgaarvestuse töötlemiseks Mehhikos.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-373">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="2bd0b-374">Toetatud väärtused on **Jooksevkonto** ja **Palgakonto**</span><span class="sxs-lookup"><span data-stu-id="2bd0b-374">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="2bd0b-375">Töövõtjad, kes soovivad oma palka pangakonto ülekannetena kätte saada, peavad esitama lingi jäägikontole, mis on juriidilise isiku alluvuses, kelle peamine aadress on Mehhikos ja kes on seotud Mehhiko panga kehtiva pangakontoga.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-375">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="2bd0b-376">Kõiki ülejäänuid kontosid, mis pole jäägikontod, eiratakse.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-376">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="2bd0b-377">Aadressiteave</span><span class="sxs-lookup"><span data-stu-id="2bd0b-377">Address information</span></span>

<span data-ttu-id="2bd0b-378">Igal töövõtjal peab olema üks peamine asukoht.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-378">Every employee must have one primary location.</span></span> <span data-ttu-id="2bd0b-379">Dayforce’is kasutatakse seda asukohta, et määratleda töövõtja peamine elukoht maksustamise tarbeks.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-379">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="2bd0b-380">Peamine elukoht (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-380">Primary (required)</span></span>
- <span data-ttu-id="2bd0b-381">Riik/regioon (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-381">Country/region (required)</span></span>
- <span data-ttu-id="2bd0b-382">Sihtnumber (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-382">Zip/postal code (required)</span></span>
- <span data-ttu-id="2bd0b-383">Tänava nimi (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-383">Street (required)</span></span>
- <span data-ttu-id="2bd0b-384">Tänava number (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-384">Street Number (required)</span></span>
- <span data-ttu-id="2bd0b-385">Hoone tähis</span><span class="sxs-lookup"><span data-stu-id="2bd0b-385">Building Complement</span></span>
- <span data-ttu-id="2bd0b-386">Linn (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-386">City (required)</span></span>
- <span data-ttu-id="2bd0b-387">Osariik (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-387">State (required)</span></span>
- <span data-ttu-id="2bd0b-388">Maakond (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-388">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="2bd0b-389">Andmete konfigureerimine palgaandmete loomiseks Ameerika Ühendriikides ja Kanadas</span><span class="sxs-lookup"><span data-stu-id="2bd0b-389">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="2bd0b-390">Kui loote palgaandmeid Ameerika Ühendriikide või Kanada töövõtjatele, siis peate konfigureerima järgmisi elemente.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-390">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="2bd0b-391">Ametikohtadele tuleb määrata osakonnad.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-391">Departments are required on positions.</span></span>
- <span data-ttu-id="2bd0b-392">Kulukeskused tuleb määratleda finantsdimensioonideks ja peavad olema vaike-finantsdimensiooni stringi esimene element.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-392">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="2bd0b-393">Saate rakenduse Human Resources konfigureerida nõudma osakonna määratlemist ametikohtade poolt.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-393">You can configure Human Resources to require that Positions specify a Department.</span></span> <span data-ttu-id="2bd0b-394">Selleks valige **Inimressursside ühised ametikohad > Ametikohad > Nõua ametikohtade puhul osakondi**.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-394">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="2bd0b-395">Soovitame selle sätte integreerimiseks jõustada.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-395">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="2bd0b-396">Töötüübid</span><span class="sxs-lookup"><span data-stu-id="2bd0b-396">Job types</span></span>

<span data-ttu-id="2bd0b-397">Töötüüpe kasutatakse sarnaste tööde kategooriatesse grupeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-397">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="2bd0b-398">Töötüübid on vajalikud palgaarvestuse töötlemiseks Ameerika Ühendriikides ja Kanadas.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-398">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="2bd0b-399">Töötüübid on näiteks täistööaeg ja osaline tööaeg või kuupalk ning tunnipalk.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-399">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="2bd0b-400">Töötüübid vastendatakse Dayforce’i tasutüüpidena, mis näitavad, kas töövõtja on tunni- või palgatöötaja.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-400">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="2bd0b-401">Järgmised töötüübid ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-401">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="2bd0b-402">Töö tüüp</span><span class="sxs-lookup"><span data-stu-id="2bd0b-402">Job type</span></span>   | <span data-ttu-id="2bd0b-403">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="2bd0b-403">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="2bd0b-404">Tunnimäär</span><span class="sxs-lookup"><span data-stu-id="2bd0b-404">Hourly</span></span>     | <span data-ttu-id="2bd0b-405">Tunnimäär</span><span class="sxs-lookup"><span data-stu-id="2bd0b-405">Hourly</span></span>      |
| <span data-ttu-id="2bd0b-406">Põhipalk</span><span class="sxs-lookup"><span data-stu-id="2bd0b-406">Salaried</span></span>   | <span data-ttu-id="2bd0b-407">Põhipalk</span><span class="sxs-lookup"><span data-stu-id="2bd0b-407">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="2bd0b-408">Ametikoha tüübid</span><span class="sxs-lookup"><span data-stu-id="2bd0b-408">Position types</span></span> 

<span data-ttu-id="2bd0b-409">Ametikoha tüüpe kasutatakse selleks, et kirjeldada, kas ametikoht on täiskohaga, osalise tööajaga või midagi muud.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-409">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="2bd0b-410">Ametikoha tüübid vastendatakse Dayforce’i tasuklassidena, mis näitavad, kas töövõtja on täis- või osalise tööajaga töötaja.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-410">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="2bd0b-411">Järgmised ametikoha tüübid ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-411">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="2bd0b-412">Ametikoha tüüp</span><span class="sxs-lookup"><span data-stu-id="2bd0b-412">Position type</span></span>   | <span data-ttu-id="2bd0b-413">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="2bd0b-413">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="2bd0b-414">Täistööaeg</span><span class="sxs-lookup"><span data-stu-id="2bd0b-414">Full-time</span></span>       | <span data-ttu-id="2bd0b-415">Täistööajaga töövõtja</span><span class="sxs-lookup"><span data-stu-id="2bd0b-415">Full time employee</span></span> |
| <span data-ttu-id="2bd0b-416">Osaline tööaeg</span><span class="sxs-lookup"><span data-stu-id="2bd0b-416">Part-time</span></span>       | <span data-ttu-id="2bd0b-417">Osalise tööajaga töövõtja</span><span class="sxs-lookup"><span data-stu-id="2bd0b-417">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="2bd0b-418">Põhjuse koodid</span><span class="sxs-lookup"><span data-stu-id="2bd0b-418">Reason codes</span></span>

<span data-ttu-id="2bd0b-419">Põhjusekoodid annavad teavet töövõtja oleku kohta.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-419">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="2bd0b-420">Põhjusekoodid vastendatakse Dayforce’i olekupõhjustena, mis näitavad töövõtja ametikoha või töösuhte oleku muutuse põhjust.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-420">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="2bd0b-421">Järgmised põhjusekoodid ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-421">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="2bd0b-422">Põhjusekood</span><span class="sxs-lookup"><span data-stu-id="2bd0b-422">Reason code</span></span>    | <span data-ttu-id="2bd0b-423">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="2bd0b-423">Description</span></span>      | <span data-ttu-id="2bd0b-424">Rakendatavad stsenaariumid</span><span class="sxs-lookup"><span data-stu-id="2bd0b-424">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="2bd0b-425">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="2bd0b-425">RESIGNATION</span></span>    | <span data-ttu-id="2bd0b-426">Lahkumine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-426">Resignation</span></span>      | <span data-ttu-id="2bd0b-427">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-427">Terminate worker</span></span>     |
| <span data-ttu-id="2bd0b-428">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="2bd0b-428">TERMINATION</span></span>    | <span data-ttu-id="2bd0b-429">Lõpetamine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-429">Termination</span></span>      | <span data-ttu-id="2bd0b-430">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-430">Terminate worker</span></span>     |
| <span data-ttu-id="2bd0b-431">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="2bd0b-431">RETIREMENT</span></span>     | <span data-ttu-id="2bd0b-432">Pensionile jäämine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-432">Retirement</span></span>       | <span data-ttu-id="2bd0b-433">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-433">Terminate worker</span></span>     |
| <span data-ttu-id="2bd0b-434">OTHER</span><span class="sxs-lookup"><span data-stu-id="2bd0b-434">OTHER</span></span>          | <span data-ttu-id="2bd0b-435">Muud põhjused</span><span class="sxs-lookup"><span data-stu-id="2bd0b-435">Other Reasons</span></span>    | <span data-ttu-id="2bd0b-436">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-436">Terminate worker</span></span>     |
| <span data-ttu-id="2bd0b-437">DEATH</span><span class="sxs-lookup"><span data-stu-id="2bd0b-437">DEATH</span></span>          | <span data-ttu-id="2bd0b-438">Surm</span><span class="sxs-lookup"><span data-stu-id="2bd0b-438">Death</span></span>            | <span data-ttu-id="2bd0b-439">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-439">Terminate worker</span></span>     |
| <span data-ttu-id="2bd0b-440">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="2bd0b-440">LEAVEOFABSENCE</span></span> | <span data-ttu-id="2bd0b-441">Puhkus</span><span class="sxs-lookup"><span data-stu-id="2bd0b-441">Leave of Absence</span></span> | <span data-ttu-id="2bd0b-442">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-442">Terminate worker</span></span>     |
| <span data-ttu-id="2bd0b-443">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="2bd0b-443">CONTRACTEND</span></span>    | <span data-ttu-id="2bd0b-444">Lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-444">End of Contract</span></span>  | <span data-ttu-id="2bd0b-445">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-445">Terminate worker</span></span>     |
| <span data-ttu-id="2bd0b-446">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="2bd0b-446">SALARYCHANGE</span></span>   | <span data-ttu-id="2bd0b-447">Palga muutus</span><span class="sxs-lookup"><span data-stu-id="2bd0b-447">Change of Salary</span></span> | <span data-ttu-id="2bd0b-448">Hüvitus</span><span class="sxs-lookup"><span data-stu-id="2bd0b-448">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="2bd0b-449">Perekonnaseis</span><span class="sxs-lookup"><span data-stu-id="2bd0b-449">Marital status</span></span>

<span data-ttu-id="2bd0b-450">Perekonnaseisu väärtused vastendatakse Dayforce’i ja tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-450">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="2bd0b-451">Järgmine tabel näitab, kuidas perekonnaseisu väärtusi Dayforce’i vastendatakse.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-451">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="2bd0b-452">Inimressursid</span><span class="sxs-lookup"><span data-stu-id="2bd0b-452">Human Resources</span></span>                 | <span data-ttu-id="2bd0b-453">Dayforce</span><span class="sxs-lookup"><span data-stu-id="2bd0b-453">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="2bd0b-454">Abielus</span><span class="sxs-lookup"><span data-stu-id="2bd0b-454">Married</span></span>                | <span data-ttu-id="2bd0b-455">Abielus</span><span class="sxs-lookup"><span data-stu-id="2bd0b-455">Married</span></span>              |
| <span data-ttu-id="2bd0b-456">Üksik</span><span class="sxs-lookup"><span data-stu-id="2bd0b-456">Single</span></span>                 | <span data-ttu-id="2bd0b-457">Üksik</span><span class="sxs-lookup"><span data-stu-id="2bd0b-457">Single</span></span>               |
| <span data-ttu-id="2bd0b-458">Lesk</span><span class="sxs-lookup"><span data-stu-id="2bd0b-458">Widowed</span></span>                | <span data-ttu-id="2bd0b-459">Lesk</span><span class="sxs-lookup"><span data-stu-id="2bd0b-459">Widowed</span></span>              |
| <span data-ttu-id="2bd0b-460">Lahutatud</span><span class="sxs-lookup"><span data-stu-id="2bd0b-460">Divorced</span></span>               | <span data-ttu-id="2bd0b-461">Lahutatud</span><span class="sxs-lookup"><span data-stu-id="2bd0b-461">Divorced</span></span>             |
| <span data-ttu-id="2bd0b-462">Registreeritud partnerlus</span><span class="sxs-lookup"><span data-stu-id="2bd0b-462">Registered Partnership</span></span> | <span data-ttu-id="2bd0b-463">Mitteabieluline kooselu</span><span class="sxs-lookup"><span data-stu-id="2bd0b-463">Domestic Partnership</span></span> |
| <span data-ttu-id="2bd0b-464">None</span><span class="sxs-lookup"><span data-stu-id="2bd0b-464">None</span></span>                   | <span data-ttu-id="2bd0b-465">None</span><span class="sxs-lookup"><span data-stu-id="2bd0b-465">None</span></span>                 |
| <span data-ttu-id="2bd0b-466">Kooselu</span><span class="sxs-lookup"><span data-stu-id="2bd0b-466">Cohabiting</span></span>             | <span data-ttu-id="2bd0b-467">Kooselu</span><span class="sxs-lookup"><span data-stu-id="2bd0b-467">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="2bd0b-468">Sugu</span><span class="sxs-lookup"><span data-stu-id="2bd0b-468">Gender</span></span>

<span data-ttu-id="2bd0b-469">Soo määratlused vastendatakse Dayforce’i ja tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-469">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="2bd0b-470">Järgmine tabel näitab, kuidas soo määratlusi Dayforce’i vastendatakse.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-470">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="2bd0b-471">Inimressursid</span><span class="sxs-lookup"><span data-stu-id="2bd0b-471">Human Resources</span></span>       | <span data-ttu-id="2bd0b-472">Dayforce</span><span class="sxs-lookup"><span data-stu-id="2bd0b-472">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="2bd0b-473">Mees</span><span class="sxs-lookup"><span data-stu-id="2bd0b-473">Male</span></span>         | <span data-ttu-id="2bd0b-474">Mees</span><span class="sxs-lookup"><span data-stu-id="2bd0b-474">Male</span></span>            |
| <span data-ttu-id="2bd0b-475">Naissoost</span><span class="sxs-lookup"><span data-stu-id="2bd0b-475">Female</span></span>       | <span data-ttu-id="2bd0b-476">Naissoost</span><span class="sxs-lookup"><span data-stu-id="2bd0b-476">Female</span></span>          |
| <span data-ttu-id="2bd0b-477">Mittespetsiifiline</span><span class="sxs-lookup"><span data-stu-id="2bd0b-477">Non-specific</span></span> | <span data-ttu-id="2bd0b-478">*Ei toetata*</span><span class="sxs-lookup"><span data-stu-id="2bd0b-478">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="2bd0b-479">Tulukoodid</span><span class="sxs-lookup"><span data-stu-id="2bd0b-479">Earning codes</span></span>

<span data-ttu-id="2bd0b-480">Tulukoodid määratlevad kordumatult igat tüüpi tulud, mida töötajad saavad.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-480">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="2bd0b-481">Koodid hõlmavad mitmeid tuludega seotud parameetreid, näiteks raamatupidamisreeglid, maksuseadused, aruandluse nõuded ja brutosumma võime.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-481">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="2bd0b-482">Kui kasutatakse toetuseta sagedust, siis kasutatakse arvutamise jaoks vaikimisi sagedust **Iga makse**.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-482">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="2bd0b-483">Toetatud sagedused</span><span class="sxs-lookup"><span data-stu-id="2bd0b-483">Supported frequencies</span></span>

- <span data-ttu-id="2bd0b-484">Kõik</span><span class="sxs-lookup"><span data-stu-id="2bd0b-484">All</span></span>
- <span data-ttu-id="2bd0b-485">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="2bd0b-485">EVERYPAY</span></span>
- <span data-ttu-id="2bd0b-486">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="2bd0b-486">EACHPAYPERIOD</span></span>
- <span data-ttu-id="2bd0b-487">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="2bd0b-487">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="2bd0b-488">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="2bd0b-488">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="2bd0b-489">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="2bd0b-489">1OFMTH</span></span>
- <span data-ttu-id="2bd0b-490">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="2bd0b-490">LASTOFMTH</span></span>
- <span data-ttu-id="2bd0b-491">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="2bd0b-491">2OFMTH</span></span>
- <span data-ttu-id="2bd0b-492">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="2bd0b-492">3OFMTH</span></span>
- <span data-ttu-id="2bd0b-493">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2bd0b-493">4OFMTH</span></span>
- <span data-ttu-id="2bd0b-494">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="2bd0b-494">5OFMTH</span></span>
- <span data-ttu-id="2bd0b-495">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="2bd0b-495">1N2OFMTH</span></span>
- <span data-ttu-id="2bd0b-496">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2bd0b-496">3N4OFMTH</span></span>
- <span data-ttu-id="2bd0b-497">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="2bd0b-497">1N3OFMTH</span></span>
- <span data-ttu-id="2bd0b-498">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2bd0b-498">1N4OFMTH</span></span>
- <span data-ttu-id="2bd0b-499">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="2bd0b-499">2N3OFMTH</span></span>
- <span data-ttu-id="2bd0b-500">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2bd0b-500">2N4OFMTH</span></span>
- <span data-ttu-id="2bd0b-501">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="2bd0b-501">1N2N3OFMTH</span></span>
- <span data-ttu-id="2bd0b-502">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2bd0b-502">1N2N4OFMTH</span></span>
- <span data-ttu-id="2bd0b-503">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2bd0b-503">1N3N4OFMTH</span></span>
- <span data-ttu-id="2bd0b-504">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2bd0b-504">2N3N4OFMTH</span></span>
- <span data-ttu-id="2bd0b-505">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2bd0b-505">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="2bd0b-506">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="2bd0b-506">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="2bd0b-507">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="2bd0b-507">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="2bd0b-508">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="2bd0b-508">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="2bd0b-509">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="2bd0b-509">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="2bd0b-510">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="2bd0b-510">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="2bd0b-511">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="2bd0b-511">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="2bd0b-512">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="2bd0b-512">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="2bd0b-513">Aadressid</span><span class="sxs-lookup"><span data-stu-id="2bd0b-513">Addresses</span></span>

<span data-ttu-id="2bd0b-514">Teatud riigi või regiooni, osariigi ja maakonna (haldusüksuse) koodide tuvastamise jaoks on vaja kindlaid vorminguid, mida Dayforce ning riigi-/regioonisisesed pakkujad ära tunnevad.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-514">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="2bd0b-515">Kuigi linnade vorming on paindlik, peab iga linn olema seotud osariigiga.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-515">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="2bd0b-516">Inimressursid</span><span class="sxs-lookup"><span data-stu-id="2bd0b-516">Human Resources</span></span>          | <span data-ttu-id="2bd0b-517">Dayforce</span><span class="sxs-lookup"><span data-stu-id="2bd0b-517">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="2bd0b-518">Riik/regioon</span><span class="sxs-lookup"><span data-stu-id="2bd0b-518">Country/Region</span></span>  | <span data-ttu-id="2bd0b-519">Riigi kood</span><span class="sxs-lookup"><span data-stu-id="2bd0b-519">Country Code</span></span>          |
| <span data-ttu-id="2bd0b-520">Sihtnumber</span><span class="sxs-lookup"><span data-stu-id="2bd0b-520">Zip/Postal Code</span></span> | <span data-ttu-id="2bd0b-521">Sihtnumber</span><span class="sxs-lookup"><span data-stu-id="2bd0b-521">Postal Code</span></span>           |
| <span data-ttu-id="2bd0b-522">Osariik</span><span class="sxs-lookup"><span data-stu-id="2bd0b-522">State</span></span>           | <span data-ttu-id="2bd0b-523">Osariigi kood</span><span class="sxs-lookup"><span data-stu-id="2bd0b-523">State Code</span></span>            |
| <span data-ttu-id="2bd0b-524">Linn</span><span class="sxs-lookup"><span data-stu-id="2bd0b-524">City</span></span>            | <span data-ttu-id="2bd0b-525">Linn</span><span class="sxs-lookup"><span data-stu-id="2bd0b-525">City</span></span>                  |
| <span data-ttu-id="2bd0b-526">Maakond</span><span class="sxs-lookup"><span data-stu-id="2bd0b-526">County</span></span>          | <span data-ttu-id="2bd0b-527">Maakond (haldusüksus)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-527">County (Municipality)</span></span> |
| <span data-ttu-id="2bd0b-528">Tänav</span><span class="sxs-lookup"><span data-stu-id="2bd0b-528">Street</span></span>          | <span data-ttu-id="2bd0b-529">Aadressirida 1</span><span class="sxs-lookup"><span data-stu-id="2bd0b-529">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="2bd0b-530">Maksuregioonid</span><span class="sxs-lookup"><span data-stu-id="2bd0b-530">Tax regions</span></span>

<span data-ttu-id="2bd0b-531">Maksuregioone kasutatakse palga loomisel sobiva maksu määramiseks.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-531">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="2bd0b-532">Maksuregioonid vastendatakse Dayforce’i asukoha-aadressidena.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-532">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="2bd0b-533">Maksuregiooni vaikevariant peab olema seotud töötaja aktiivse ametikohaga.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-533">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="2bd0b-534">Maksuregioon (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-534">Tax region (required)</span></span>
- <span data-ttu-id="2bd0b-535">Riik/regioon (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-535">Country/Region (required)</span></span>
- <span data-ttu-id="2bd0b-536">Osariik (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-536">State (required)</span></span>
- <span data-ttu-id="2bd0b-537">Maakond</span><span class="sxs-lookup"><span data-stu-id="2bd0b-537">County</span></span> 
- <span data-ttu-id="2bd0b-538">Linn (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-538">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="2bd0b-539">Andmete konfigureerimine palgaandmete loomiseks Mehhikos</span><span class="sxs-lookup"><span data-stu-id="2bd0b-539">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="2bd0b-540">Kui loote palgaandmeid Mehhiko töövõtjatele, siis peate konfigureerima järgmisi elemente.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-540">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="2bd0b-541">Ametikohtadele tuleb määrata osakonnad.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-541">Departments are required on positions.</span></span>
- <span data-ttu-id="2bd0b-542">Kulukeskused tuleb määratleda finantsdimensioonideks ja peavad olema vaike-finantsdimensiooni stringi esimene element.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-542">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="2bd0b-543">Töötüübid</span><span class="sxs-lookup"><span data-stu-id="2bd0b-543">Job types</span></span>

<span data-ttu-id="2bd0b-544">Töötüüpe kasutatakse sarnaste tööde kategooriatesse grupeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-544">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="2bd0b-545">Mehhikos palgaarvestuse töötlemiseks on vajalikud töötüübid.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-545">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="2bd0b-546">Töötüübid on näiteks täistööaeg ja osaline tööaeg või kuupalk ning tunnipalk.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-546">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="2bd0b-547">Töötüübid vastendatakse Dayforce’i tasutüüpidena, mis näitavad, kas töövõtja on tunni- või palgatöötaja.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-547">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="2bd0b-548">Järgmised töötüübid ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-548">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="2bd0b-549">Töö tüüp</span><span class="sxs-lookup"><span data-stu-id="2bd0b-549">Job type</span></span>   | <span data-ttu-id="2bd0b-550">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="2bd0b-550">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="2bd0b-551">Tunnimäär</span><span class="sxs-lookup"><span data-stu-id="2bd0b-551">Hourly</span></span>     | <span data-ttu-id="2bd0b-552">MX tunnimäär</span><span class="sxs-lookup"><span data-stu-id="2bd0b-552">MX Hourly</span></span>   |
| <span data-ttu-id="2bd0b-553">Põhipalk</span><span class="sxs-lookup"><span data-stu-id="2bd0b-553">Salaried</span></span>   | <span data-ttu-id="2bd0b-554">MX põhipalk</span><span class="sxs-lookup"><span data-stu-id="2bd0b-554">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="2bd0b-555">Positsioonitüübid</span><span class="sxs-lookup"><span data-stu-id="2bd0b-555">Position types</span></span> 

<span data-ttu-id="2bd0b-556">Ametikoha tüüpe kasutatakse selleks, et kirjeldada, kas ametikoht on täiskohaga, osalise tööajaga või midagi muud.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-556">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="2bd0b-557">Ametikoha tüübid vastendatakse Dayforce’i tasuklassidena, mis näitavad, kas töövõtja on täis- või osalise tööajaga töötaja.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-557">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="2bd0b-558">Järgmised ametikoha tüübid ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-558">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="2bd0b-559">Ametikoha tüüp</span><span class="sxs-lookup"><span data-stu-id="2bd0b-559">Position type</span></span>   | <span data-ttu-id="2bd0b-560">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="2bd0b-560">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="2bd0b-561">Täistööaeg</span><span class="sxs-lookup"><span data-stu-id="2bd0b-561">Full-time</span></span>       | <span data-ttu-id="2bd0b-562">Täistööajaga töövõtja</span><span class="sxs-lookup"><span data-stu-id="2bd0b-562">Full time employee</span></span> |
| <span data-ttu-id="2bd0b-563">Osaline tööaeg</span><span class="sxs-lookup"><span data-stu-id="2bd0b-563">Part-time</span></span>       | <span data-ttu-id="2bd0b-564">Osalise tööajaga töövõtja</span><span class="sxs-lookup"><span data-stu-id="2bd0b-564">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="2bd0b-565">Põhjuse koodid</span><span class="sxs-lookup"><span data-stu-id="2bd0b-565">Reason codes</span></span>

<span data-ttu-id="2bd0b-566">Põhjusekoodid annavad teavet töövõtja oleku kohta.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-566">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="2bd0b-567">Põhjusekoodid vastendatakse Dayforce’i olekupõhjustena, mis näitavad töövõtja ametikoha või töösuhte oleku muutuse põhjust.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-567">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="2bd0b-568">Järgmised põhjusekoodid ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-568">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="2bd0b-569">Põhjusekood</span><span class="sxs-lookup"><span data-stu-id="2bd0b-569">Reason code</span></span>            | <span data-ttu-id="2bd0b-570">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="2bd0b-570">Description</span></span>                    | <span data-ttu-id="2bd0b-571">Rakendatavad stsenaariumid</span><span class="sxs-lookup"><span data-stu-id="2bd0b-571">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="2bd0b-572">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="2bd0b-572">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="2bd0b-573">Lahkumine enne esimest palgamakset</span><span class="sxs-lookup"><span data-stu-id="2bd0b-573">Departure before first payroll</span></span> | <span data-ttu-id="2bd0b-574">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-574">Terminate worker</span></span>     |
| <span data-ttu-id="2bd0b-575">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="2bd0b-575">RESIGNATION</span></span>            | <span data-ttu-id="2bd0b-576">Lahkumine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-576">Resignation</span></span>                    | <span data-ttu-id="2bd0b-577">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-577">Terminate worker</span></span>     |
| <span data-ttu-id="2bd0b-578">PENSION</span><span class="sxs-lookup"><span data-stu-id="2bd0b-578">PENSION</span></span>                | <span data-ttu-id="2bd0b-579">Pension</span><span class="sxs-lookup"><span data-stu-id="2bd0b-579">Pension</span></span>                        | <span data-ttu-id="2bd0b-580">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-580">Terminate worker</span></span>     |
| <span data-ttu-id="2bd0b-581">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="2bd0b-581">TERMINATION</span></span>            | <span data-ttu-id="2bd0b-582">Lõpetamine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-582">Termination</span></span>                    | <span data-ttu-id="2bd0b-583">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-583">Terminate worker</span></span>     |
| <span data-ttu-id="2bd0b-584">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="2bd0b-584">RETIREMENT</span></span>             | <span data-ttu-id="2bd0b-585">Pensionile jäämine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-585">Retirement</span></span>                     | <span data-ttu-id="2bd0b-586">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-586">Terminate worker</span></span>     |
| <span data-ttu-id="2bd0b-587">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="2bd0b-587">ABSENTEE</span></span>               | <span data-ttu-id="2bd0b-588">Puuduja</span><span class="sxs-lookup"><span data-stu-id="2bd0b-588">Absentee</span></span>                       | <span data-ttu-id="2bd0b-589">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-589">Terminate worker</span></span>     |
| <span data-ttu-id="2bd0b-590">OTHER</span><span class="sxs-lookup"><span data-stu-id="2bd0b-590">OTHER</span></span>                  | <span data-ttu-id="2bd0b-591">Muud põhjused</span><span class="sxs-lookup"><span data-stu-id="2bd0b-591">Other Reasons</span></span>                  | <span data-ttu-id="2bd0b-592">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-592">Terminate worker</span></span>     |
| <span data-ttu-id="2bd0b-593">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="2bd0b-593">CLOSURE</span></span>                | <span data-ttu-id="2bd0b-594">Ettevõte suletud</span><span class="sxs-lookup"><span data-stu-id="2bd0b-594">Business Closure</span></span>               | <span data-ttu-id="2bd0b-595">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-595">Terminate worker</span></span>     |
| <span data-ttu-id="2bd0b-596">DEATH</span><span class="sxs-lookup"><span data-stu-id="2bd0b-596">DEATH</span></span>                  | <span data-ttu-id="2bd0b-597">Surm</span><span class="sxs-lookup"><span data-stu-id="2bd0b-597">Death</span></span>                          | <span data-ttu-id="2bd0b-598">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-598">Terminate worker</span></span>     |
| <span data-ttu-id="2bd0b-599">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="2bd0b-599">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="2bd0b-600">Puhkus</span><span class="sxs-lookup"><span data-stu-id="2bd0b-600">Leave of Absence</span></span>               | <span data-ttu-id="2bd0b-601">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-601">Terminate worker</span></span>     |
| <span data-ttu-id="2bd0b-602">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="2bd0b-602">CONTRACTEND</span></span>            | <span data-ttu-id="2bd0b-603">Lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-603">End of Contract</span></span>                | <span data-ttu-id="2bd0b-604">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="2bd0b-604">Terminate worker</span></span>     |
| <span data-ttu-id="2bd0b-605">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="2bd0b-605">SALARYCHANGE</span></span>           | <span data-ttu-id="2bd0b-606">Palga muutus</span><span class="sxs-lookup"><span data-stu-id="2bd0b-606">Change of Salary</span></span>               | <span data-ttu-id="2bd0b-607">Hüvitus</span><span class="sxs-lookup"><span data-stu-id="2bd0b-607">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="2bd0b-608">Töösuhte tingimused</span><span class="sxs-lookup"><span data-stu-id="2bd0b-608">Terms of employment</span></span>

<span data-ttu-id="2bd0b-609">Töösuhte tingimusi kasutatakse töösuhte tingimuste kategooriate loomiseks.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-609">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="2bd0b-610">Tingimused vastendatakse Dayforce’i töösuhte indikaatorväärtustena.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-610">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="2bd0b-611">Järgmised töösuhte tingimused ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-611">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="2bd0b-612">Töösuhte tingimused</span><span class="sxs-lookup"><span data-stu-id="2bd0b-612">Terms of employment</span></span>   | <span data-ttu-id="2bd0b-613">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="2bd0b-613">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="2bd0b-614">Tavaline</span><span class="sxs-lookup"><span data-stu-id="2bd0b-614">Regular</span></span>               | <span data-ttu-id="2bd0b-615">Tavaline</span><span class="sxs-lookup"><span data-stu-id="2bd0b-615">Regular</span></span>     |
| <span data-ttu-id="2bd0b-616">Otse</span><span class="sxs-lookup"><span data-stu-id="2bd0b-616">Direct</span></span>                | <span data-ttu-id="2bd0b-617">Otse</span><span class="sxs-lookup"><span data-stu-id="2bd0b-617">Direct</span></span>      |
| <span data-ttu-id="2bd0b-618">Praktika</span><span class="sxs-lookup"><span data-stu-id="2bd0b-618">Internship</span></span>            | <span data-ttu-id="2bd0b-619">Praktika</span><span class="sxs-lookup"><span data-stu-id="2bd0b-619">Internship</span></span>  |
| <span data-ttu-id="2bd0b-620">Alaline</span><span class="sxs-lookup"><span data-stu-id="2bd0b-620">Permanent</span></span>             | <span data-ttu-id="2bd0b-621">Alaline</span><span class="sxs-lookup"><span data-stu-id="2bd0b-621">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="2bd0b-622">Perekonnaseis</span><span class="sxs-lookup"><span data-stu-id="2bd0b-622">Marital status</span></span>

<span data-ttu-id="2bd0b-623">Perekonnaseisu väärtused vastendatakse Dayforce’i ja tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-623">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="2bd0b-624">Järgmine tabel näitab, kuidas perekonnaseisu väärtusi Dayforce’i vastendatakse.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-624">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="2bd0b-625">Inimressursid</span><span class="sxs-lookup"><span data-stu-id="2bd0b-625">Human Resources</span></span>                 | <span data-ttu-id="2bd0b-626">Dayforce</span><span class="sxs-lookup"><span data-stu-id="2bd0b-626">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="2bd0b-627">Abielus</span><span class="sxs-lookup"><span data-stu-id="2bd0b-627">Married</span></span>                | <span data-ttu-id="2bd0b-628">Abielus</span><span class="sxs-lookup"><span data-stu-id="2bd0b-628">Married</span></span>                   |
| <span data-ttu-id="2bd0b-629">Üksik</span><span class="sxs-lookup"><span data-stu-id="2bd0b-629">Single</span></span>                 | <span data-ttu-id="2bd0b-630">Üksik</span><span class="sxs-lookup"><span data-stu-id="2bd0b-630">Single</span></span>                    |
| <span data-ttu-id="2bd0b-631">Lesk</span><span class="sxs-lookup"><span data-stu-id="2bd0b-631">Widowed</span></span>                | <span data-ttu-id="2bd0b-632">Lesk</span><span class="sxs-lookup"><span data-stu-id="2bd0b-632">Widowed</span></span>                   |
| <span data-ttu-id="2bd0b-633">Lahutatud</span><span class="sxs-lookup"><span data-stu-id="2bd0b-633">Divorced</span></span>               | <span data-ttu-id="2bd0b-634">Lahutatud</span><span class="sxs-lookup"><span data-stu-id="2bd0b-634">Divorced</span></span>                  |
| <span data-ttu-id="2bd0b-635">Registreeritud partnerlus</span><span class="sxs-lookup"><span data-stu-id="2bd0b-635">Registered Partnership</span></span> | <span data-ttu-id="2bd0b-636">Mitteabieluline kooselu</span><span class="sxs-lookup"><span data-stu-id="2bd0b-636">Domestic Partnership</span></span>      |
| <span data-ttu-id="2bd0b-637">None</span><span class="sxs-lookup"><span data-stu-id="2bd0b-637">None</span></span>                   | <span data-ttu-id="2bd0b-638">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="2bd0b-638">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="2bd0b-639">Kooselu</span><span class="sxs-lookup"><span data-stu-id="2bd0b-639">Cohabiting</span></span>             | <span data-ttu-id="2bd0b-640">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="2bd0b-640">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="2bd0b-641">Sugu</span><span class="sxs-lookup"><span data-stu-id="2bd0b-641">Gender</span></span>

<span data-ttu-id="2bd0b-642">Soo määratlused vastendatakse Dayforce’i ja tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-642">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="2bd0b-643">Järgmine tabel näitab, kuidas soo määratlusi Dayforce’i vastendatakse.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-643">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="2bd0b-644">Inimressursid</span><span class="sxs-lookup"><span data-stu-id="2bd0b-644">Human Resources</span></span>       | <span data-ttu-id="2bd0b-645">Dayforce</span><span class="sxs-lookup"><span data-stu-id="2bd0b-645">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="2bd0b-646">Mees</span><span class="sxs-lookup"><span data-stu-id="2bd0b-646">Male</span></span>         | <span data-ttu-id="2bd0b-647">Mees</span><span class="sxs-lookup"><span data-stu-id="2bd0b-647">Male</span></span>                      |
| <span data-ttu-id="2bd0b-648">Naissoost</span><span class="sxs-lookup"><span data-stu-id="2bd0b-648">Female</span></span>       | <span data-ttu-id="2bd0b-649">Naissoost</span><span class="sxs-lookup"><span data-stu-id="2bd0b-649">Female</span></span>                    |
| <span data-ttu-id="2bd0b-650">Mittespetsiifiline</span><span class="sxs-lookup"><span data-stu-id="2bd0b-650">Non-specific</span></span> | <span data-ttu-id="2bd0b-651">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="2bd0b-651">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="2bd0b-652">Makseviis</span><span class="sxs-lookup"><span data-stu-id="2bd0b-652">Payment method</span></span>

<span data-ttu-id="2bd0b-653">Makseviisid võimaldavad töövõtjal ja ettevõttel kirjeldada, kuidas töövõtjatele makstakse.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-653">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="2bd0b-654">Makseviisid vastendatakse Dayforce’i ja tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-654">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="2bd0b-655">Järgmine tabel näitab, kuidas makseviise Dayforce’i vastendatakse.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-655">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="2bd0b-656">Inimressursid</span><span class="sxs-lookup"><span data-stu-id="2bd0b-656">Human Resources</span></span>             | <span data-ttu-id="2bd0b-657">Dayforce</span><span class="sxs-lookup"><span data-stu-id="2bd0b-657">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="2bd0b-658">Sularaha</span><span class="sxs-lookup"><span data-stu-id="2bd0b-658">Cash</span></span>               | <span data-ttu-id="2bd0b-659">Sularaha</span><span class="sxs-lookup"><span data-stu-id="2bd0b-659">Cash</span></span>                      |
| <span data-ttu-id="2bd0b-660">Elektrooniline makse</span><span class="sxs-lookup"><span data-stu-id="2bd0b-660">Electronic Payment</span></span> | <span data-ttu-id="2bd0b-661">Ülekanne</span><span class="sxs-lookup"><span data-stu-id="2bd0b-661">Transfer</span></span>                  |
| <span data-ttu-id="2bd0b-662">Kontrolli</span><span class="sxs-lookup"><span data-stu-id="2bd0b-662">Check</span></span>              | <span data-ttu-id="2bd0b-663">Tšekk</span><span class="sxs-lookup"><span data-stu-id="2bd0b-663">Cheque</span></span>                    |
| <span data-ttu-id="2bd0b-664">Pangaveksel</span><span class="sxs-lookup"><span data-stu-id="2bd0b-664">Bank Draft</span></span>         | <span data-ttu-id="2bd0b-665">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="2bd0b-665">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="2bd0b-666">Muud</span><span class="sxs-lookup"><span data-stu-id="2bd0b-666">Other</span></span>              | <span data-ttu-id="2bd0b-667">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="2bd0b-667">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="2bd0b-668">Pangakonto tüüp</span><span class="sxs-lookup"><span data-stu-id="2bd0b-668">Bank account type</span></span>

<span data-ttu-id="2bd0b-669">Pangakonto tüüpe kasutatakse elektrooniliste maksete tegemiseks töötajatele.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-669">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="2bd0b-670">Pangakonto tüübid vastendatakse Dayforce’i ülekandekonto teabena.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-670">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="2bd0b-671">Pangakonto tüübid tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-671">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="2bd0b-672">Inimressursid</span><span class="sxs-lookup"><span data-stu-id="2bd0b-672">Human Resources</span></span>            | <span data-ttu-id="2bd0b-673">Dayforce</span><span class="sxs-lookup"><span data-stu-id="2bd0b-673">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="2bd0b-674">Jooksevkonto</span><span class="sxs-lookup"><span data-stu-id="2bd0b-674">Checking Account</span></span>  | <span data-ttu-id="2bd0b-675">Jooksevkonto</span><span class="sxs-lookup"><span data-stu-id="2bd0b-675">CheckingAccount</span></span>           |
| <span data-ttu-id="2bd0b-676">Palgakonto</span><span class="sxs-lookup"><span data-stu-id="2bd0b-676">Payroll Account</span></span>   | <span data-ttu-id="2bd0b-677">Palgakonto</span><span class="sxs-lookup"><span data-stu-id="2bd0b-677">PayrollAccount</span></span>            |
| <span data-ttu-id="2bd0b-678">Hoiukonto</span><span class="sxs-lookup"><span data-stu-id="2bd0b-678">Savings Account</span></span>   | <span data-ttu-id="2bd0b-679">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="2bd0b-679">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="2bd0b-680">BankGiroti konto</span><span class="sxs-lookup"><span data-stu-id="2bd0b-680">BankGirot account</span></span> | <span data-ttu-id="2bd0b-681">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="2bd0b-681">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="2bd0b-682">PlusGiroti konto</span><span class="sxs-lookup"><span data-stu-id="2bd0b-682">PlusGirot account</span></span> | <span data-ttu-id="2bd0b-683">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="2bd0b-683">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="2bd0b-684">Tulukoodid</span><span class="sxs-lookup"><span data-stu-id="2bd0b-684">Earning codes</span></span>

<span data-ttu-id="2bd0b-685">Tulukoodid määratlevad kordumatult igat tüüpi tulud, mida töötajad saavad.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-685">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="2bd0b-686">Koodid hõlmavad mitmeid tuludega seotud parameetreid, näiteks raamatupidamisreeglid, maksuseadused, aruandluse nõuded ja brutosumma võime.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-686">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="2bd0b-687">Kui kasutatakse toetuseta sagedust, siis kasutatakse arvutamise jaoks vaikimisi sagedust **Iga makse**.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-687">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="2bd0b-688">Toetatud sagedused</span><span class="sxs-lookup"><span data-stu-id="2bd0b-688">Supported frequencies</span></span>

- <span data-ttu-id="2bd0b-689">Kõik</span><span class="sxs-lookup"><span data-stu-id="2bd0b-689">All</span></span>
- <span data-ttu-id="2bd0b-690">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="2bd0b-690">EVERYPAY</span></span>
- <span data-ttu-id="2bd0b-691">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="2bd0b-691">EACHPAYPERIOD</span></span>
- <span data-ttu-id="2bd0b-692">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="2bd0b-692">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="2bd0b-693">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="2bd0b-693">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="2bd0b-694">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="2bd0b-694">1OFMTH</span></span>
- <span data-ttu-id="2bd0b-695">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="2bd0b-695">LASTOFMTH</span></span>
- <span data-ttu-id="2bd0b-696">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="2bd0b-696">2OFMTH</span></span>
- <span data-ttu-id="2bd0b-697">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="2bd0b-697">3OFMTH</span></span>
- <span data-ttu-id="2bd0b-698">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2bd0b-698">4OFMTH</span></span>
- <span data-ttu-id="2bd0b-699">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="2bd0b-699">5OFMTH</span></span>
- <span data-ttu-id="2bd0b-700">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="2bd0b-700">1N2OFMTH</span></span>
- <span data-ttu-id="2bd0b-701">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2bd0b-701">3N4OFMTH</span></span>
- <span data-ttu-id="2bd0b-702">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="2bd0b-702">1N3OFMTH</span></span>
- <span data-ttu-id="2bd0b-703">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2bd0b-703">1N4OFMTH</span></span>
- <span data-ttu-id="2bd0b-704">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="2bd0b-704">2N3OFMTH</span></span>
- <span data-ttu-id="2bd0b-705">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2bd0b-705">2N4OFMTH</span></span>
- <span data-ttu-id="2bd0b-706">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="2bd0b-706">1N2N3OFMTH</span></span>
- <span data-ttu-id="2bd0b-707">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2bd0b-707">1N2N4OFMTH</span></span>
- <span data-ttu-id="2bd0b-708">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2bd0b-708">1N3N4OFMTH</span></span>
- <span data-ttu-id="2bd0b-709">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2bd0b-709">2N3N4OFMTH</span></span>
- <span data-ttu-id="2bd0b-710">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="2bd0b-710">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="2bd0b-711">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="2bd0b-711">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="2bd0b-712">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="2bd0b-712">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="2bd0b-713">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="2bd0b-713">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="2bd0b-714">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="2bd0b-714">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="2bd0b-715">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="2bd0b-715">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="2bd0b-716">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="2bd0b-716">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="2bd0b-717">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="2bd0b-717">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="2bd0b-718">Aadressid</span><span class="sxs-lookup"><span data-stu-id="2bd0b-718">Addresses</span></span>

<span data-ttu-id="2bd0b-719">Teatud riigi või regiooni, osariigi ja maakonna (haldusüksuse) koodide tuvastamise jaoks on vaja kindlaid vorminguid, mida Dayforce ning riigi-/regioonisisesed pakkujad ära tunnevad.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-719">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="2bd0b-720">Kuigi linnade vorming on paindlik, peab iga linn olema seotud osariigiga.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-720">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="2bd0b-721">Inimressursid</span><span class="sxs-lookup"><span data-stu-id="2bd0b-721">Human Resources</span></span>              | <span data-ttu-id="2bd0b-722">Dayforce</span><span class="sxs-lookup"><span data-stu-id="2bd0b-722">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="2bd0b-723">Riik/regioon</span><span class="sxs-lookup"><span data-stu-id="2bd0b-723">Country/Region</span></span>      | <span data-ttu-id="2bd0b-724">Riigi kood</span><span class="sxs-lookup"><span data-stu-id="2bd0b-724">Country Code</span></span>          |
| <span data-ttu-id="2bd0b-725">Sihtnumber</span><span class="sxs-lookup"><span data-stu-id="2bd0b-725">Zip/Postal Code</span></span>     | <span data-ttu-id="2bd0b-726">Sihtnumber</span><span class="sxs-lookup"><span data-stu-id="2bd0b-726">Postal Code</span></span>           |
| <span data-ttu-id="2bd0b-727">Osariik</span><span class="sxs-lookup"><span data-stu-id="2bd0b-727">State</span></span>               | <span data-ttu-id="2bd0b-728">Osariigi kood</span><span class="sxs-lookup"><span data-stu-id="2bd0b-728">State Code</span></span>            |
| <span data-ttu-id="2bd0b-729">Linn</span><span class="sxs-lookup"><span data-stu-id="2bd0b-729">City</span></span>                | <span data-ttu-id="2bd0b-730">Linn</span><span class="sxs-lookup"><span data-stu-id="2bd0b-730">City</span></span>                  |
| <span data-ttu-id="2bd0b-731">Maakond</span><span class="sxs-lookup"><span data-stu-id="2bd0b-731">County</span></span>              | <span data-ttu-id="2bd0b-732">Maakond (haldusüksus)</span><span class="sxs-lookup"><span data-stu-id="2bd0b-732">County (Municipality)</span></span> |
| <span data-ttu-id="2bd0b-733">Tänav</span><span class="sxs-lookup"><span data-stu-id="2bd0b-733">Street</span></span>              | <span data-ttu-id="2bd0b-734">Aadressirida 1</span><span class="sxs-lookup"><span data-stu-id="2bd0b-734">Address Line 1</span></span>        |
| <span data-ttu-id="2bd0b-735">Majanumber</span><span class="sxs-lookup"><span data-stu-id="2bd0b-735">Street Number</span></span>       | <span data-ttu-id="2bd0b-736">Aadressirida 2</span><span class="sxs-lookup"><span data-stu-id="2bd0b-736">Address Line 2</span></span>        |
| <span data-ttu-id="2bd0b-737">Hoone tähis</span><span class="sxs-lookup"><span data-stu-id="2bd0b-737">Building Complement</span></span> | <span data-ttu-id="2bd0b-738">Aadressirida 5</span><span class="sxs-lookup"><span data-stu-id="2bd0b-738">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="2bd0b-739">Passi number</span><span class="sxs-lookup"><span data-stu-id="2bd0b-739">Passport number</span></span>

<span data-ttu-id="2bd0b-740">Töötajad saavad deklareerida passi teavet.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-740">Employees can declare passport information.</span></span> <span data-ttu-id="2bd0b-741">See teave on identifitseerimistüüpi **Pass** ja integreeritakse Dayforce’i töövõtja Mehhiko-teabe osana.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-741">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="2bd0b-742">Identifitseerimistüüp = pass</span><span class="sxs-lookup"><span data-stu-id="2bd0b-742">Identification Type = "Passport"</span></span>
- <span data-ttu-id="2bd0b-743">Väljastamise kuupäev</span><span class="sxs-lookup"><span data-stu-id="2bd0b-743">Issued Date</span></span>
- <span data-ttu-id="2bd0b-744">Aegumiskuupäev</span><span class="sxs-lookup"><span data-stu-id="2bd0b-744">Expiration Date</span></span>

<span data-ttu-id="2bd0b-745">Töövõtjad saavad deklareerida mitu **Pass**-identifitseerimistüüpi ID-numbrit.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-745">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="2bd0b-746">Dayforce’i integreeritakse siiski ainult praegune aktiivne passikirje.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-746">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="2bd0b-747">Kui kõik passikirjed on aegunud, siis integreeritakse Dayforce’i pass, mis väljastati viimasena.</span><span class="sxs-lookup"><span data-stu-id="2bd0b-747">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>

