---
title: Rakenduste Talent ja Dayforce vahelise palgaarvestuse integratsiooni konfigureerimine
description: Selles teemas selgitatakse, kuidas konfigureerida rakenduste Microsoft Dynamics 365 Talent ja Ceridian Dayforce vahelist integratsiooni nii, et saaksite teha palgatöötlust.
author: andreabichsel
manager: AnnBe
ms.date: 06/24/2019
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
ms.openlocfilehash: ec1d14cb14ab709dfc1bead4be0785904efcce4e
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251035"
---
# <a name="configure-the-payroll-integration-between-talent-and-dayforce"></a><span data-ttu-id="d05e7-103">Palgaarvestuse integratsiooni konfigureerimine Talenti ja Dayforce’i vahel</span><span class="sxs-lookup"><span data-stu-id="d05e7-103">Configure the payroll integration between Talent and Dayforce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="d05e7-104">Rakenduste Microsoft Dynamics 365 Talent ja Ceridian Dayforce vaheline integratsioon sõltub mitmest konfiguratsioonietapist, mida kirjeldatakse selles teemas.</span><span class="sxs-lookup"><span data-stu-id="d05e7-104">The integration between Microsoft Dynamics 365 Talent and Ceridian Dayforce relies on several configuration steps that are described in this topic.</span></span> <span data-ttu-id="d05e7-105">Enne palgatöötluse tegemist peate konfigureerima integratsiooni nii rakenduses Talent kui ka Dayforce.</span><span class="sxs-lookup"><span data-stu-id="d05e7-105">You must configure the integration in both Talent and Dayforce before you can process a pay run.</span></span>

<span data-ttu-id="d05e7-106">Kui te kasutate palgatöötluste tegemiseks teenust nagu Dayforce, siis peate rakenduses Talent integratsiooni lubama.</span><span class="sxs-lookup"><span data-stu-id="d05e7-106">When you use a service such as Dayforce to complete pay runs, you must enable the integration in Talent.</span></span> <span data-ttu-id="d05e7-107">Integratsiooni jaoks on rakendusest Talent vaja teatud andmeid.</span><span class="sxs-lookup"><span data-stu-id="d05e7-107">The integration requires specific data from Talent.</span></span> <span data-ttu-id="d05e7-108">Seega peate kinnitama, et Dayforce’iga vastendatud andmed on rakenduses Talent konfigureeritud viisil, mis lubab integratsiooni.</span><span class="sxs-lookup"><span data-stu-id="d05e7-108">Therefore, you must verify that data that is mapped to Dayforce is configured in Talent in a manner that supports the integration.</span></span> <span data-ttu-id="d05e7-109">Integratsioon kasutab järgmisi üldisi andmekategooriaid.</span><span class="sxs-lookup"><span data-stu-id="d05e7-109">The integration uses the following broad categories of data:</span></span>

- <span data-ttu-id="d05e7-110">Inimressursside andmed</span><span class="sxs-lookup"><span data-stu-id="d05e7-110">Human resources data</span></span>
- <span data-ttu-id="d05e7-111">Hüvituse andmed</span><span class="sxs-lookup"><span data-stu-id="d05e7-111">Compensation data</span></span>
- <span data-ttu-id="d05e7-112">Palgaandmed, näiteks palgatsüklid, makseperioodid ja tulukoodid</span><span class="sxs-lookup"><span data-stu-id="d05e7-112">Payroll data, such as pay cycles, pay periods, and earning codes</span></span>
- <span data-ttu-id="d05e7-113">Töötaja andmed</span><span class="sxs-lookup"><span data-stu-id="d05e7-113">Worker data</span></span>

<span data-ttu-id="d05e7-114">Teemas kirjeldatakse etappe, mida peate integratsiooni lubamiseks läbima.</span><span class="sxs-lookup"><span data-stu-id="d05e7-114">This topic describes the steps that you must follow to enable the integration.</span></span> <span data-ttu-id="d05e7-115">Samuti selgitatakse integratsiooni jaoks vajalikke andmetüüpe ja konfigureerimise üksikasju.</span><span class="sxs-lookup"><span data-stu-id="d05e7-115">It also explains the types of data and the configuration details that the integration requires.</span></span>

## <a name="enable-the-integration"></a><span data-ttu-id="d05e7-116">Integratsiooni lubamine</span><span class="sxs-lookup"><span data-stu-id="d05e7-116">Enable the integration</span></span>

<span data-ttu-id="d05e7-117">Dayforce’iga ühendamiseks peate rakenduses Talent sisse lülitama integratsiooni ja sisestama konfigureerimisteabe.</span><span class="sxs-lookup"><span data-stu-id="d05e7-117">In Talent, you must turn on the integration and enter the configuration information to connect to Dayforce.</span></span> <span data-ttu-id="d05e7-118">Kui soovite, et loodav pearaamatu kanne imporditaks rakendusse Microsoft Dynamics 365 Finance, siis peate seadistama Microsoft Azure’i salvestuskonto ja sisestama Azure’i salvestusruumi ühendusstringi rakendusse Finance.</span><span class="sxs-lookup"><span data-stu-id="d05e7-118">If you want the general ledger transaction that is produced to be imported into Microsoft Dynamics 365 Finance, you must also set up a Microsoft Azure storage account and enter the Azure Storage connection string in Finance.</span></span>

<span data-ttu-id="d05e7-119">Rakenduses Talent integratsiooni sisselülitamiseks järgige järgmisi juhiseid.</span><span class="sxs-lookup"><span data-stu-id="d05e7-119">To turn on the integration in Talent, follow these steps.</span></span>

1. <span data-ttu-id="d05e7-120">Valige lehelt **Süsteemihaldus** suvand **Integratsiooni konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="d05e7-120">On the **System administration** page, select **Integration configuration**.</span></span>
2. <span data-ttu-id="d05e7-121">Sisestage turvalise failiedastusprotokolli File Transfer Protocol (FTP) lõpp-punkt ja turvalise FTP kausta tee.</span><span class="sxs-lookup"><span data-stu-id="d05e7-121">Enter the secure File Transfer Protocol (FTP) endpoint and the secure FTP folder path.</span></span>
3. <span data-ttu-id="d05e7-122">Sisestage selle kasutaja kasutajanimi ja parool, kellel on vaja juurdepääsu turvalise FTP lõpp-punktile ja kausta teele.</span><span class="sxs-lookup"><span data-stu-id="d05e7-122">Enter the user name and password of the user who will access the secure FTP endpoint and folder path.</span></span>
4. <span data-ttu-id="d05e7-123">Testige ühendust vajaduse järgi ja määrake suvand **Palgaarvestuse integratsiooni lubamine** olekule **Jah**.</span><span class="sxs-lookup"><span data-stu-id="d05e7-123">Test the connection, as required, and set the **Enable payroll integration** option to **Yes**.</span></span>

<span data-ttu-id="d05e7-124">Kui integratsioon on sisse lülitatud, luuakse andmete ekspordipakett ja -failid ning määratakse sagedus.</span><span class="sxs-lookup"><span data-stu-id="d05e7-124">When the integration is turned on, the data export package and files are created, and the frequency is set.</span></span> <span data-ttu-id="d05e7-125">Vajaduse korral saate seda sagedust muuta.</span><span class="sxs-lookup"><span data-stu-id="d05e7-125">You can change this frequency as you require.</span></span>

<span data-ttu-id="d05e7-126">Lisateavet Azure’i talletamiskontode ja Azure’i salvestusruumi ühendusstringide kohta leiate järgmistest Azure’i teemadest.</span><span class="sxs-lookup"><span data-stu-id="d05e7-126">For more information about Azure storage accounts and Azure Storage connection strings, see the following Azure topics:</span></span>

- [<span data-ttu-id="d05e7-127">Azure’i salvestuskontod</span><span class="sxs-lookup"><span data-stu-id="d05e7-127">About Azure storage accounts</span></span>](https://docs.microsoft.com/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [<span data-ttu-id="d05e7-128">Azure’i salvestusruumi ühendusstringide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="d05e7-128">Configure Azure Storage connection strings</span></span>](https://docs.microsoft.com/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a><span data-ttu-id="d05e7-129">Tehnilised üksikasjad, kui palga integratsioon on lubatud</span><span class="sxs-lookup"><span data-stu-id="d05e7-129">Technical details when payroll integration is enabled</span></span>

<span data-ttu-id="d05e7-130">Palga integreerimise sisselülitamisel on kaks peamist mõju.</span><span class="sxs-lookup"><span data-stu-id="d05e7-130">Turning on the payroll integration has two primary effects:</span></span>

- <span data-ttu-id="d05e7-131">Luuakse andmete ekspordi projekt nimega "Palga integreerimise eksport".</span><span class="sxs-lookup"><span data-stu-id="d05e7-131">A data export project named "Payroll integration export" is created.</span></span> <span data-ttu-id="d05e7-132">See projekt sisaldab palga integreerimise jaoks nõutavaid üksusi ja välju.</span><span class="sxs-lookup"><span data-stu-id="d05e7-132">This project contains the entities and fields required for the payroll integration.</span></span> <span data-ttu-id="d05e7-133">Projekti uurimiseks avage **Süsteemihaldus**, valige paan **Andmehaldus** ja avage projektiloendist andmete projekt.</span><span class="sxs-lookup"><span data-stu-id="d05e7-133">To examine the project, go to **System administration**, select the **Data management** tile, and then open the data project from the list of projects.</span></span>
- <span data-ttu-id="d05e7-134">See pakett-töö käivitab andmete eksportimise projekti, krüptib tulemuste andmete paketi ja edastab andmete paketi faili SFTP-lõpp-punktile, mis on konfigureeritud kuval **integratsiooni konfiguratsioon**.</span><span class="sxs-lookup"><span data-stu-id="d05e7-134">This batch job executes the data export project, encrypts the resulting data package, and transfers the data package file to the SFTP endpoint configured on the **Integration configuration** screen.</span></span>

> [!NOTE]
> <span data-ttu-id="d05e7-135">SFTP-lõpp-punkti edastatud andmete pakett krüptitakse, kasutades võtit, mis on paketile kordumatu.</span><span class="sxs-lookup"><span data-stu-id="d05e7-135">The data package transferred to the SFTP endpoint is encrypted using a key that is unique to the package.</span></span> <span data-ttu-id="d05e7-136">Võti on Azure võtmehoidlas, mis on kättesaadav ainult Ceridianile.</span><span class="sxs-lookup"><span data-stu-id="d05e7-136">The key is in an Azure Key Vault that is accessible only by Ceridian.</span></span> <span data-ttu-id="d05e7-137">Andmebaasi sisu ei saa dekrüptida ja uurida.</span><span class="sxs-lookup"><span data-stu-id="d05e7-137">It is not possible to decrypt and examine the data package contents.</span></span> <span data-ttu-id="d05e7-138">Kui teil on vaja uurida andmepaketi sisu, peate eksportima projekti "Palga integreerimise eksport" käsitsi, selle alla laadima ja seejärel avama.</span><span class="sxs-lookup"><span data-stu-id="d05e7-138">If you need to examine the contents of the data package, you need to export the "Payroll integration export" data project manually, download it, and then open it.</span></span> <span data-ttu-id="d05e7-139">Käsitsi eksportimine ei rakenda krüptimist ega edasta paketti.</span><span class="sxs-lookup"><span data-stu-id="d05e7-139">Manual export will not apply encryption or transfer the package.</span></span>

## <a name="configure-your-data"></a><span data-ttu-id="d05e7-140">Andmete konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="d05e7-140">Configure your data</span></span> 

<span data-ttu-id="d05e7-141">Palgaarvestuse töötlemiseks peate konfigureerima rakenduses Talent personaliandmeid.</span><span class="sxs-lookup"><span data-stu-id="d05e7-141">To process payroll, you must configure human resource data in Talent.</span></span> <span data-ttu-id="d05e7-142">Peate määratlema organisatsiooni andmeid nagu tööd ja ametikohad, samuti teavet soodustuste ning kompensatsioonide kohta.</span><span class="sxs-lookup"><span data-stu-id="d05e7-142">You must set up organizational data, such as jobs and positions, together with benefits and compensation information.</span></span> <span data-ttu-id="d05e7-143">Selle teabe hulka kuulub töövõtja palgaandmete loomiseks vajalik teave töösuhte, palga ja mahaarvamiste kohta.</span><span class="sxs-lookup"><span data-stu-id="d05e7-143">This information provides the employment, pay, and deduction information that is required in order to generate employee pay.</span></span>

### <a name="human-resource-data"></a><span data-ttu-id="d05e7-144">Personaliandmed</span><span class="sxs-lookup"><span data-stu-id="d05e7-144">Human resource data</span></span>

#### <a name="benefits"></a><span data-ttu-id="d05e7-145">Soodustused</span><span class="sxs-lookup"><span data-stu-id="d05e7-145">Benefits</span></span> 

<span data-ttu-id="d05e7-146">Inimressursid pakuvad tööriistu, mis aitavad seadistada ja hallata soodustusi, mahaarvamisi ning töötajate hüvitusplaane, mida organisatsioon oma töötajatele pakub või nende puhul töötleb.</span><span class="sxs-lookup"><span data-stu-id="d05e7-146">Human resources provides tools for the setup and maintenance of the benefits, deductions, and worker compensation plans that an organization offers or processes for its workers.</span></span>

<span data-ttu-id="d05e7-147">Soodustuste loomisel pidage meeles järgmisi Dayforce’is kasutatavaid andmeid ja konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="d05e7-147">When you create benefits, keep in mind the following data and configurations that are used in Dayforce.</span></span>

##### <a name="benefit-plans"></a><span data-ttu-id="d05e7-148">Soodustusplaanid</span><span class="sxs-lookup"><span data-stu-id="d05e7-148">Benefit plans</span></span>

- <span data-ttu-id="d05e7-149">Plaan (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-149">Plan (required)</span></span>
- <span data-ttu-id="d05e7-150">Tüüp (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-150">Type (required)</span></span>
- <span data-ttu-id="d05e7-151">Palga mõju (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-151">Payroll impact (required)</span></span>
- <span data-ttu-id="d05e7-152">Võlgnevuste sissenõudmine</span><span class="sxs-lookup"><span data-stu-id="d05e7-152">Recover arrears</span></span>
- <span data-ttu-id="d05e7-153">Mahaarvamismeetod</span><span class="sxs-lookup"><span data-stu-id="d05e7-153">Deduction method</span></span>
- <span data-ttu-id="d05e7-154">Mahaarvamise prioriteet</span><span class="sxs-lookup"><span data-stu-id="d05e7-154">Deduction priority</span></span>
- <span data-ttu-id="d05e7-155">Perioodi piiramine</span><span class="sxs-lookup"><span data-stu-id="d05e7-155">Limit period</span></span>
- <span data-ttu-id="d05e7-156">Piirsumma</span><span class="sxs-lookup"><span data-stu-id="d05e7-156">Limit amount</span></span>

##### <a name="benefits"></a><span data-ttu-id="d05e7-157">Soodustused</span><span class="sxs-lookup"><span data-stu-id="d05e7-157">Benefits</span></span>

- <span data-ttu-id="d05e7-158">Plaan (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-158">Plan (required)</span></span>
- <span data-ttu-id="d05e7-159">Tüüp (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-159">Type (required)</span></span>
- <span data-ttu-id="d05e7-160">Suvand (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-160">Option (required)</span></span>
- <span data-ttu-id="d05e7-161">Soodustuse ID (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-161">Benefit ID (required)</span></span>
- <span data-ttu-id="d05e7-162">Sagedus</span><span class="sxs-lookup"><span data-stu-id="d05e7-162">Frequency</span></span>
- <span data-ttu-id="d05e7-163">Alus</span><span class="sxs-lookup"><span data-stu-id="d05e7-163">Basis</span></span>
- <span data-ttu-id="d05e7-164">Summa või määr</span><span class="sxs-lookup"><span data-stu-id="d05e7-164">Amount or rate</span></span>
- <span data-ttu-id="d05e7-165">Tulukood</span><span class="sxs-lookup"><span data-stu-id="d05e7-165">Earning code</span></span>

##### <a name="supported-frequencies"></a><span data-ttu-id="d05e7-166">Toetatud sagedused</span><span class="sxs-lookup"><span data-stu-id="d05e7-166">Supported frequencies</span></span> 

- <span data-ttu-id="d05e7-167">Iga nädal</span><span class="sxs-lookup"><span data-stu-id="d05e7-167">Weekly</span></span>
- <span data-ttu-id="d05e7-168">Kahe nädala tagant</span><span class="sxs-lookup"><span data-stu-id="d05e7-168">Bi-weekly</span></span>
- <span data-ttu-id="d05e7-169">Iga poole kuu tagant</span><span class="sxs-lookup"><span data-stu-id="d05e7-169">Semi-monthly</span></span>
- <span data-ttu-id="d05e7-170">Kord kuus</span><span class="sxs-lookup"><span data-stu-id="d05e7-170">Monthly</span></span>

##### <a name="supported-bases"></a><span data-ttu-id="d05e7-171">Toetatud alused</span><span class="sxs-lookup"><span data-stu-id="d05e7-171">Supported bases</span></span> 

- <span data-ttu-id="d05e7-172">Fikseeritud summa</span><span class="sxs-lookup"><span data-stu-id="d05e7-172">Fixed amount</span></span>
- <span data-ttu-id="d05e7-173">Tulu protsent</span><span class="sxs-lookup"><span data-stu-id="d05e7-173">Percent of earnings</span></span>
- <span data-ttu-id="d05e7-174">Produktiivsed tunnid</span><span class="sxs-lookup"><span data-stu-id="d05e7-174">Productive hours</span></span>

<span data-ttu-id="d05e7-175">Dayforce loob järgmised mahaarvamised palga mõju alusel, mis on määratletud soodustusplaanis.</span><span class="sxs-lookup"><span data-stu-id="d05e7-175">Dayforce creates the following deductions, based on the payroll impact that is defined on the benefit plan.</span></span>

| <span data-ttu-id="d05e7-176">Valik rakenduses Talent</span><span class="sxs-lookup"><span data-stu-id="d05e7-176">Selection in Talent</span></span>        | <span data-ttu-id="d05e7-177">Tulemus rakenduses Dayforce</span><span class="sxs-lookup"><span data-stu-id="d05e7-177">Result in Dayforce</span></span>                            |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="d05e7-178">Pole</span><span class="sxs-lookup"><span data-stu-id="d05e7-178">None</span></span>                       | <span data-ttu-id="d05e7-179">Mahaarvamist ei looda.</span><span class="sxs-lookup"><span data-stu-id="d05e7-179">No deduction is created.</span></span>                      |
| <span data-ttu-id="d05e7-180">Ainult mahaarvamine</span><span class="sxs-lookup"><span data-stu-id="d05e7-180">Deduction only</span></span>             | <span data-ttu-id="d05e7-181">Luuakse töövõtja mahaarvamine.</span><span class="sxs-lookup"><span data-stu-id="d05e7-181">An employee deduction is created.</span></span>             |
| <span data-ttu-id="d05e7-182">Ainult lisamine</span><span class="sxs-lookup"><span data-stu-id="d05e7-182">Contribution only</span></span>          | <span data-ttu-id="d05e7-183">Luuakse tööandja mahaarvamine.</span><span class="sxs-lookup"><span data-stu-id="d05e7-183">An employer deduction is created.</span></span>             |
| <span data-ttu-id="d05e7-184">Mahaarvamine ja lisamine</span><span class="sxs-lookup"><span data-stu-id="d05e7-184">Deduction and contribution</span></span> | <span data-ttu-id="d05e7-185">Luuakse töövõtja ja tööandja mahaarvamised.</span><span class="sxs-lookup"><span data-stu-id="d05e7-185">Employee and employer deductions are created.</span></span> |

<span data-ttu-id="d05e7-186">Lisateavet soodustusprogrammi määratlemise ja haldamise kohta vaadake järgmistest teemadest.</span><span class="sxs-lookup"><span data-stu-id="d05e7-186">For more information about how to define and manage a benefits program, see the following topics:</span></span>

- [<span data-ttu-id="d05e7-187">Töötaja soodustuste programmi pakkumine</span><span class="sxs-lookup"><span data-stu-id="d05e7-187">Deliver an employee benefits program</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [<span data-ttu-id="d05e7-188">Uue soodustuse loomine</span><span class="sxs-lookup"><span data-stu-id="d05e7-188">Create a new benefit</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [<span data-ttu-id="d05e7-189">Soodustuskõlblikkuse reeglite ja poliitikate määratlemine</span><span class="sxs-lookup"><span data-stu-id="d05e7-189">Define benefit eligibility rules and policies</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [<span data-ttu-id="d05e7-190">Töötajate soodustuste registreerimine ja eemaldamine</span><span class="sxs-lookup"><span data-stu-id="d05e7-190">Enroll and remove benefits from workers</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a><span data-ttu-id="d05e7-191">Hüvitus</span><span class="sxs-lookup"><span data-stu-id="d05e7-191">Compensation</span></span> 

<span data-ttu-id="d05e7-192">Hüvituste haldust kasutatakse põhitasu ja preemiate jagamise juhtimiseks.</span><span class="sxs-lookup"><span data-stu-id="d05e7-192">Compensation management is used to control the delivery of base pay and awards.</span></span> <span data-ttu-id="d05e7-193">Töötaja fikseeritud põhipalga ja preemia tõusu juhitakse põhipalga plaanide kaudu.</span><span class="sxs-lookup"><span data-stu-id="d05e7-193">An employee's fixed base pay and merit increases are controlled through fixed compensation plans.</span></span> <span data-ttu-id="d05e7-194">Lisatasude (nt preemiate, tulemustasude aktsiate eelismüügi ja toetuste ning ühekordsete preemiate) maksmist juhitakse ergutussüsteemi plaanide kaudu.</span><span class="sxs-lookup"><span data-stu-id="d05e7-194">The payment of incentive pay, such as bonus payments, performance awards, stock options, and grants, and also one-time awards, are controlled through variable compensation plans.</span></span>

<span data-ttu-id="d05e7-195">Dayforce kasutab hüvituse teavet töövõtja tunni- või aastamäära arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="d05e7-195">Dayforce uses compensation information to calculate an employee's hourly or annual rate.</span></span> <span data-ttu-id="d05e7-196">Nõutavad on põhipalgaplaanid ja palgamäära teisendamised.</span><span class="sxs-lookup"><span data-stu-id="d05e7-196">Fixed compensation plans and pay rate conversions are required.</span></span> <span data-ttu-id="d05e7-197">Töövõtjad peavad olema seotud põhipalgaplaaniga.</span><span class="sxs-lookup"><span data-stu-id="d05e7-197">Employees must be associated with a fixed compensation plan.</span></span>

<span data-ttu-id="d05e7-198">Lisateavet hüvitusplaanide kohta vaadake järgmistest teemadest.</span><span class="sxs-lookup"><span data-stu-id="d05e7-198">For more information about compensation plans, see the following topics:</span></span>

- [<span data-ttu-id="d05e7-199">Põhipalga plaanide loomine</span><span class="sxs-lookup"><span data-stu-id="d05e7-199">Create fixed compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [<span data-ttu-id="d05e7-200">Ergutussüsteemi plaanide loomine</span><span class="sxs-lookup"><span data-stu-id="d05e7-200">Create variable compensation plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [<span data-ttu-id="d05e7-201">Palga/hüvituse struktuuri ja plaanide arendamine</span><span class="sxs-lookup"><span data-stu-id="d05e7-201">Develop salary/compensation structure and plans</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [<span data-ttu-id="d05e7-202">Hüvitusprotsess</span><span class="sxs-lookup"><span data-stu-id="d05e7-202">Process compensation</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/process-compensation)
- [<span data-ttu-id="d05e7-203">Hüvitusprotsessi määratlemine ja tulemuste arvutamine</span><span class="sxs-lookup"><span data-stu-id="d05e7-203">Define compensation process and calculate results</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [<span data-ttu-id="d05e7-204">Töötaja liitmine põhipalga plaaniga</span><span class="sxs-lookup"><span data-stu-id="d05e7-204">Enroll an employee in a fixed compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [<span data-ttu-id="d05e7-205">Töötaja liitmine tulemustasu plaaniga</span><span class="sxs-lookup"><span data-stu-id="d05e7-205">Enroll an employee in a variable compensation plan</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a><span data-ttu-id="d05e7-206">Tööd</span><span class="sxs-lookup"><span data-stu-id="d05e7-206">Jobs</span></span> 

<span data-ttu-id="d05e7-207">Töö on tööd tegeva isiku jaoks nõutavate ülesannete ja vastutuste kogum.</span><span class="sxs-lookup"><span data-stu-id="d05e7-207">A job is a collection of the tasks and responsibilities that are required of a person who performs a job.</span></span> <span data-ttu-id="d05e7-208">Lisateavet vt järgmistest teemadest:</span><span class="sxs-lookup"><span data-stu-id="d05e7-208">For more information, see the following topics:</span></span>

- [<span data-ttu-id="d05e7-209">Töö komponentide seadistamine</span><span class="sxs-lookup"><span data-stu-id="d05e7-209">Setting up the components of a job</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-job)
- [<span data-ttu-id="d05e7-210">Uute tööde määratlemine</span><span class="sxs-lookup"><span data-stu-id="d05e7-210">Define new jobs</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a><span data-ttu-id="d05e7-211">Ametikohad</span><span class="sxs-lookup"><span data-stu-id="d05e7-211">Positions</span></span>

<span data-ttu-id="d05e7-212">Ametikoht on töökoha üksik eksemplar.</span><span class="sxs-lookup"><span data-stu-id="d05e7-212">A position is an individual instance of a job.</span></span> <span data-ttu-id="d05e7-213">Näiteks on ametikoht „müügijuht (Ida)” vaid üks tööga „müügijuht” seostatud ametikohti.</span><span class="sxs-lookup"><span data-stu-id="d05e7-213">For example, the "Sales manager (East)" position is one of the positions that are associated with the "Sales manager" job.</span></span> <span data-ttu-id="d05e7-214">Ametikoht kuulub osakonna alla.</span><span class="sxs-lookup"><span data-stu-id="d05e7-214">A position exists in a department.</span></span> <span data-ttu-id="d05e7-215">Iga ametikohaga saab seostada vaid ühte töötajat.</span><span class="sxs-lookup"><span data-stu-id="d05e7-215">Only one worker can be associated with each position.</span></span>

<span data-ttu-id="d05e7-216">Ametikohtade seadistamisel pidage meeles järgmisi andmeid ja konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="d05e7-216">Keep the following data and configuration in mind when you set up positions:</span></span>

- <span data-ttu-id="d05e7-217">Ametikoht (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-217">Position (required)</span></span>
- <span data-ttu-id="d05e7-218">Kirjeldus (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-218">Description (required)</span></span>
- <span data-ttu-id="d05e7-219">Töö (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-219">Job (required)</span></span>
- <span data-ttu-id="d05e7-220">Osakond (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-220">Department (required)</span></span>
- <span data-ttu-id="d05e7-221">Ametikoha tüüp (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-221">Position type (required)</span></span>
- <span data-ttu-id="d05e7-222">Täistööaja vaste</span><span class="sxs-lookup"><span data-stu-id="d05e7-222">Full-time equivalent</span></span>
- <span data-ttu-id="d05e7-223">Iga-aastased regulaarsed tunnid (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-223">Annual regular hours (required)</span></span>
- <span data-ttu-id="d05e7-224">Maksja juriidiline isik (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-224">Paid by legal entity (required)</span></span>
- <span data-ttu-id="d05e7-225">Palgatsükkel (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-225">Pay cycle (required)</span></span>
- <span data-ttu-id="d05e7-226">Vaike-finantsdimensioonid – kulukeskus (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-226">Default financial dimension – Cost center (required)</span></span>
- <span data-ttu-id="d05e7-227">Töötaja määramine – töötaja, määramise algus, määramise lõpp, põhjuse kood</span><span class="sxs-lookup"><span data-stu-id="d05e7-227">Worker assignment – Worker, assignment start, assignment end, reason code</span></span>

<span data-ttu-id="d05e7-228">Kui ühes osakonnas on sama tööga seotud mitu ametikohta, siis konsolideeritakse need rakenduses Dayforce üheks ametikohaks.</span><span class="sxs-lookup"><span data-stu-id="d05e7-228">If multiple positions in the same department are associated with the same job, they are consolidated into a single position in Dayforce.</span></span>

<span data-ttu-id="d05e7-229">Lisateavet vt järgmistest teemadest:</span><span class="sxs-lookup"><span data-stu-id="d05e7-229">For more information, see the following topics:</span></span>

- [<span data-ttu-id="d05e7-230">Tööjõu korraldamine osakondade, tööde ja ametikohtade abil</span><span class="sxs-lookup"><span data-stu-id="d05e7-230">Organize your workforce using departments, jobs, and positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [<span data-ttu-id="d05e7-231">Ametikohtade seadistamine</span><span class="sxs-lookup"><span data-stu-id="d05e7-231">Set up positions</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a><span data-ttu-id="d05e7-232">Osakonnad</span><span class="sxs-lookup"><span data-stu-id="d05e7-232">Departments</span></span>

<span data-ttu-id="d05e7-233">Osakond on tootmisüksus, mis esindab organisatsiooni kategooriat või funktsionaalset ala.</span><span class="sxs-lookup"><span data-stu-id="d05e7-233">A department is an operating unit that represents a category or functional area of an organization.</span></span> <span data-ttu-id="d05e7-234">Osakond vastutab organisatsiooni kindla valdkonna eest, nagu müük, raamatupidamine või inimressursid.</span><span class="sxs-lookup"><span data-stu-id="d05e7-234">A department is responsible for a specific area of the organization, such as sales, accounting, or human resources.</span></span> <span data-ttu-id="d05e7-235">Saate osakondi kasutada funktsionaalsete alade aruannete koostamiseks.</span><span class="sxs-lookup"><span data-stu-id="d05e7-235">You can use departments to report on functional areas.</span></span> <span data-ttu-id="d05e7-236">Osakonnad võivad vastutada kasumi ja kahjumi eest.</span><span class="sxs-lookup"><span data-stu-id="d05e7-236">Departments might have profit and loss responsibility.</span></span>

<span data-ttu-id="d05e7-237">Lisateavet vt järgmistest teemadest:</span><span class="sxs-lookup"><span data-stu-id="d05e7-237">For more information, see the following topics:</span></span>

- [<span data-ttu-id="d05e7-238">Osakonna loomine ja selle seostamine osakonnahierarhiaga</span><span class="sxs-lookup"><span data-stu-id="d05e7-238">Create a department and associate it with the department hierarchy</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [<span data-ttu-id="d05e7-239">Uute osakondade määratlemine</span><span class="sxs-lookup"><span data-stu-id="d05e7-239">Define new departments</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a><span data-ttu-id="d05e7-240">Palgatsüklid ja makseperioodid</span><span class="sxs-lookup"><span data-stu-id="d05e7-240">Pay cycles and pay periods</span></span>

<span data-ttu-id="d05e7-241">Palgatsükkel määrab, kui tihti palgamaksmine toimub ja konkreetsed päevad, millal töötajatele palka makstakse.</span><span class="sxs-lookup"><span data-stu-id="d05e7-241">A pay cycle determines how often payroll is run and the specific days when workers are paid.</span></span> <span data-ttu-id="d05e7-242">Näiteks võib palgatsükli sageduseks olla üks kuu ja töövõtjatele makstakse seega kuu viimasel päeval.</span><span class="sxs-lookup"><span data-stu-id="d05e7-242">For example, a pay cycle might be monthly, and employees might be paid on the last day of the month.</span></span> <span data-ttu-id="d05e7-243">Või kui palgatsükli sageduseks on üks nädal, siis makstakse töövõtjatele näiteks teisipäeviti pärast makseperioodi lõppu.</span><span class="sxs-lookup"><span data-stu-id="d05e7-243">Alternatively, a pay cycle might be weekly, and employees might be paid on the Tuesday after the end of the pay period.</span></span> <span data-ttu-id="d05e7-244">Palgatsükleid määratakse ametikohtadele selleks, et määrata, millal nendel ametikohtadel töötavatele töötajatele palka makstakse.</span><span class="sxs-lookup"><span data-stu-id="d05e7-244">Pay cycles are assigned to positions to control when workers in those positions are paid.</span></span>

<span data-ttu-id="d05e7-245">Pärast palgatsüklite loomist saate iga tsükli jaoks luua makseperioodid.</span><span class="sxs-lookup"><span data-stu-id="d05e7-245">After you create pay cycles, you can generate pay periods for each cycle.</span></span> <span data-ttu-id="d05e7-246">Igal makseperioodil on makse vaikekuupäev, mis põhineb teie sisestatud teabel.</span><span class="sxs-lookup"><span data-stu-id="d05e7-246">Each pay period includes a default payment date that is based on information that you provide.</span></span> <span data-ttu-id="d05e7-247">Siiski saate erandite käsitlemiseks makseperioodi makse vaikekuupäeva muuta, näiteks kui maksekuupäev satub riigipühale.</span><span class="sxs-lookup"><span data-stu-id="d05e7-247">However, you can modify the default payment date in a pay period to allow for exceptions, such as when the payment date falls on a holiday.</span></span>

<span data-ttu-id="d05e7-248">Dayforce kasutab järgmist teavet.</span><span class="sxs-lookup"><span data-stu-id="d05e7-248">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="d05e7-249">Palgatsükkel (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-249">Pay cycle (required)</span></span>
- <span data-ttu-id="d05e7-250">Palgatsükli sagedus (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-250">Pay cycle frequency (required)</span></span>
- <span data-ttu-id="d05e7-251">Perioodi alguskuupäev (esimene makseperiood on kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-251">Period start date (first pay period required)</span></span>
- <span data-ttu-id="d05e7-252">Makse vaikekuupäev (esimene makseperiood on kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-252">Default payment date (first pay period required)</span></span>

<span data-ttu-id="d05e7-253">See teave on integreeritud rakendusse Dayforce palgagruppidena ja on iga palgatsükli puhul eraldatud riigi või regiooniga.</span><span class="sxs-lookup"><span data-stu-id="d05e7-253">This information is integrated with Dayforce as pay groups, and is separated by country or region for each pay cycle.</span></span> <span data-ttu-id="d05e7-254">Enne integreerimist peab olema loodud vähemalt üks makseperiood.</span><span class="sxs-lookup"><span data-stu-id="d05e7-254">At least one pay period must be generated before integration.</span></span> <span data-ttu-id="d05e7-255">Dayforce loob palgagrupi kalendrid ja maksekuupäevad rakenduses Talent määratletud esimese makseperioodi alguskuupäeva ja makse vaikekuupäeva põhjal.</span><span class="sxs-lookup"><span data-stu-id="d05e7-255">Dayforce generates pay group calendars and payment dates, based on the start date of the first pay period and the default payment date that is set up in Talent.</span></span>

#### <a name="earning-codes"></a><span data-ttu-id="d05e7-256">Tulukoodid</span><span class="sxs-lookup"><span data-stu-id="d05e7-256">Earning codes</span></span>

<span data-ttu-id="d05e7-257">Tulukoodid määratlevad kordumatult igat tüüpi tulud, mida töötajad saavad.</span><span class="sxs-lookup"><span data-stu-id="d05e7-257">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="d05e7-258">Koodidel on mitmeid tuludega seotud parameetreid, näiteks raamatupidamisreeglid, maksuseadused, aruandluse nõuded ja brutosumma võime.</span><span class="sxs-lookup"><span data-stu-id="d05e7-258">The codes have various parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span>

<span data-ttu-id="d05e7-259">Dayforce kasutab järgmist teavet.</span><span class="sxs-lookup"><span data-stu-id="d05e7-259">The following information is used in Dayforce:</span></span>

- <span data-ttu-id="d05e7-260">Tulukood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-260">Earning Code (required)</span></span>
- <span data-ttu-id="d05e7-261">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="d05e7-261">Description</span></span>
- <span data-ttu-id="d05e7-262">Mõõtühik</span><span class="sxs-lookup"><span data-stu-id="d05e7-262">Unit of measure</span></span>
- <span data-ttu-id="d05e7-263">Produktiivne</span><span class="sxs-lookup"><span data-stu-id="d05e7-263">Productive</span></span>

### <a name="worker-data"></a><span data-ttu-id="d05e7-264">Töötaja andmed</span><span class="sxs-lookup"><span data-stu-id="d05e7-264">Worker data</span></span>

<span data-ttu-id="d05e7-265">Töötajate kirjed on tähtsad teie personali- ja palgasüsteemide jaoks.</span><span class="sxs-lookup"><span data-stu-id="d05e7-265">Records for the various types of workers that you have are important to your human resources and payroll systems.</span></span> <span data-ttu-id="d05e7-266">Teie sisestatud teavet saab kasutada töötajate ja nende isikliku teabe jälgimiseks.</span><span class="sxs-lookup"><span data-stu-id="d05e7-266">The information that you enter can be used to track workers and personal information.</span></span>

<span data-ttu-id="d05e7-267">Töötajate kohta saate hallata järgmist teavet.</span><span class="sxs-lookup"><span data-stu-id="d05e7-267">You can maintain the following information for workers:</span></span>

- <span data-ttu-id="d05e7-268">**Üldine** – töötaja põhiteave, näiteks kontaktteave, demograafiline teave, tuvastamisteave, perekonna teave, sõjaväeteenistuse olek, välislähetuse teave ja isiklikud ning lähedase isiku kontaktandmed.</span><span class="sxs-lookup"><span data-stu-id="d05e7-268">**Basic** – Maintain basic information about a worker, such as contact information, demographic information, identification information, family information, military service status, expatriate information, and personal and emergency contacts.</span></span>
- <span data-ttu-id="d05e7-269">**Töösuhe** – töötaja töösuhte teave, näiteks töötaja palganud ettevõte või organisatsioon, määratud ametikoht, algus- ja lõppkuupäevad, töökõlblikkus, töölevõtutingimused, pension, puhkus ja ümberpaigutuse teave.</span><span class="sxs-lookup"><span data-stu-id="d05e7-269">**Employment** – Maintain information about a worker's employment, such as company or organization affiliation, position assignment, start and end dates, work eligibility, terms of employment, pension, vacation, and relocation information.</span></span>
- <span data-ttu-id="d05e7-270">**Puhkused ja puudumised** – teave töötaja puudumiste kohta, näiteks töögraafikud, puudumiskanded ja puudumise seadistamine.</span><span class="sxs-lookup"><span data-stu-id="d05e7-270">**Leave and absence** – Maintain information about a worker's absences, such as working calendars, absence transactions, and absence setup.</span></span>
- <span data-ttu-id="d05e7-271">**Hüvitus ja palk** – teave töötaja hüvitusplaanide ja palgaarvestuse kohta, näiteks liitutud plaanid, preemiad, tööviljakus, komisjonitasu, maksuteave, pensionileminek ning palgast mahaarvamised.</span><span class="sxs-lookup"><span data-stu-id="d05e7-271">**Compensation and payroll** – Maintain information about a worker's compensation plans and payroll information, such as plan enrollment, awards, performance, commission, tax information, retirement, and salary deductions.</span></span>

<span data-ttu-id="d05e7-272">Töötaja teabe sisestamisel pidage meeles järgmisi Dayforce’is kasutatavaid andmeid ja konfiguratsioone.</span><span class="sxs-lookup"><span data-stu-id="d05e7-272">When you enter worker information, keep in mind the following data and configurations that are used in Dayforce.</span></span>

#### <a name="general-information"></a><span data-ttu-id="d05e7-273">Üldteave</span><span class="sxs-lookup"><span data-stu-id="d05e7-273">General information</span></span>

- <span data-ttu-id="d05e7-274">Töötaja number (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-274">Personnel number (required)</span></span>
- <span data-ttu-id="d05e7-275">Eesnimi (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-275">First name (required)</span></span>
- <span data-ttu-id="d05e7-276">Perekonnanimi (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-276">Last name (required)</span></span>
- <span data-ttu-id="d05e7-277">Teine eesnimi</span><span class="sxs-lookup"><span data-stu-id="d05e7-277">Middle name</span></span>
- <span data-ttu-id="d05e7-278">Staaž kuupäeval</span><span class="sxs-lookup"><span data-stu-id="d05e7-278">Seniority date</span></span>
- <span data-ttu-id="d05e7-279">Tuntud kui</span><span class="sxs-lookup"><span data-stu-id="d05e7-279">Known as</span></span>

#### <a name="personal-information"></a><span data-ttu-id="d05e7-280">Isikuandmed</span><span class="sxs-lookup"><span data-stu-id="d05e7-280">Personal information</span></span>

- <span data-ttu-id="d05e7-281">Perekonnaseis (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-281">Marital status (required)</span></span>
- <span data-ttu-id="d05e7-282">Sünnikuupäev (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-282">Birth date (required)</span></span>
- <span data-ttu-id="d05e7-283">Sugu (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-283">Gender (required)</span></span>
- <span data-ttu-id="d05e7-284">Puudega isik</span><span class="sxs-lookup"><span data-stu-id="d05e7-284">Person with disabilities</span></span>
- <span data-ttu-id="d05e7-285">Kodakondsusjärgse riigi regioon (ainult Mehhiko puhul)</span><span class="sxs-lookup"><span data-stu-id="d05e7-285">Nationality country region (only for Mexico)</span></span>

#### <a name="address-information"></a><span data-ttu-id="d05e7-286">Aadressiteave</span><span class="sxs-lookup"><span data-stu-id="d05e7-286">Address information</span></span>

- <span data-ttu-id="d05e7-287">Tänava nimi ja hoone number (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-287">Primary (required)</span></span>
- <span data-ttu-id="d05e7-288">Riik/regioon (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-288">Country/region (required)</span></span>
- <span data-ttu-id="d05e7-289">Sihtnumber (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-289">Postal code (required)</span></span>
- <span data-ttu-id="d05e7-290">Tänava number (kohustuslik) (ainult Mehhiko puhul)</span><span class="sxs-lookup"><span data-stu-id="d05e7-290">Street Number (required) (Only for Mexico)</span></span>
- <span data-ttu-id="d05e7-291">Hoone tähis (ainult Mehhiko puhul)</span><span class="sxs-lookup"><span data-stu-id="d05e7-291">Building Complement (Only for Mexico)</span></span>
- <span data-ttu-id="d05e7-292">Linn (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-292">City (required)</span></span>
- <span data-ttu-id="d05e7-293">Osariik (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-293">State (required)</span></span>
- <span data-ttu-id="d05e7-294">Maakond (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-294">County (required)</span></span>

#### <a name="contact-information"></a><span data-ttu-id="d05e7-295">Kontaktteave</span><span class="sxs-lookup"><span data-stu-id="d05e7-295">Contact information</span></span> 

- <span data-ttu-id="d05e7-296">Tänava nimi ja hoone number (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-296">Primary (required)</span></span>
- <span data-ttu-id="d05e7-297">Kontaktnumber (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-297">Contact number (required)</span></span>
- <span data-ttu-id="d05e7-298">Sisetelefon</span><span class="sxs-lookup"><span data-stu-id="d05e7-298">Extension</span></span>

#### <a name="payroll-information-and-earning-codes"></a><span data-ttu-id="d05e7-299">Palgateave ja tulukoodid</span><span class="sxs-lookup"><span data-stu-id="d05e7-299">Payroll information and earning codes</span></span>

<span data-ttu-id="d05e7-300">Töövõtjatele võidakse määrata teatud maksesagedusega konkreetsed tulud ja neil võivad olla eelistatud makseviisid.</span><span class="sxs-lookup"><span data-stu-id="d05e7-300">Employees may be assigned specific earnings at a given frequency of payment and have a preferred payment method.</span></span> <span data-ttu-id="d05e7-301">Nende eelistuste ja sätete kasutamise tagamiseks kasutatakse Dayforce’is järgmisi välju.</span><span class="sxs-lookup"><span data-stu-id="d05e7-301">The following fields are used in Dayforce to help guarantee that those preferences and settings are used.</span></span>

##### <a name="earning-codes"></a><span data-ttu-id="d05e7-302">Tulukoodid</span><span class="sxs-lookup"><span data-stu-id="d05e7-302">Earning codes</span></span>

- <span data-ttu-id="d05e7-303">Ametikoht (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-303">Position (required)</span></span>
- <span data-ttu-id="d05e7-304">Tulukood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-304">Earning Code (required)</span></span>
- <span data-ttu-id="d05e7-305">Maksesagedus (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-305">Frequency (required)</span></span>
- <span data-ttu-id="d05e7-306">Summa (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-306">Amount (required)</span></span>

##### <a name="payroll-information"></a><span data-ttu-id="d05e7-307">Palgateave</span><span class="sxs-lookup"><span data-stu-id="d05e7-307">Payroll information</span></span>

- <span data-ttu-id="d05e7-308">Makseviis</span><span class="sxs-lookup"><span data-stu-id="d05e7-308">Payment Method</span></span>
- <span data-ttu-id="d05e7-309">Majanduspiirkond (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-309">Economic Region (required)</span></span>
- <span data-ttu-id="d05e7-310">Töövõtja soodustuste ID</span><span class="sxs-lookup"><span data-stu-id="d05e7-310">Employee Benefits ID</span></span>
- <span data-ttu-id="d05e7-311">Riiklik isikukood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-311">National ID Number (required)</span></span>
- <span data-ttu-id="d05e7-312">Sõjaväeteenistuse number</span><span class="sxs-lookup"><span data-stu-id="d05e7-312">Military Service Number</span></span>
- <span data-ttu-id="d05e7-313">Vahetuse ID (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-313">Shift ID (required)</span></span>
- <span data-ttu-id="d05e7-314">Maksukood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-314">Tax Number (required)</span></span>
- <span data-ttu-id="d05e7-315">Ühingu ID (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-315">Union ID (required)</span></span>
- <span data-ttu-id="d05e7-316">Tööpäeva ID (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-316">Work Day ID (required)</span></span>
- <span data-ttu-id="d05e7-317">Tööloa number</span><span class="sxs-lookup"><span data-stu-id="d05e7-317">Work Permit Number</span></span>

> [!NOTE]
> <span data-ttu-id="d05e7-318">Mehhiko toetab järgmisi makseviise: **sularaha**, **tšekk** (ettevõtte füüsiline tšekk) ja **elektrooniline makse**.</span><span class="sxs-lookup"><span data-stu-id="d05e7-318">For the payment method, Mexico supports **Cash**, **Check** (the company's physical check), and **Electronic Payment**.</span></span> <span data-ttu-id="d05e7-319">Kui makseviisi pole määratud, kasutatakse vaikevalikut **tšekk**.</span><span class="sxs-lookup"><span data-stu-id="d05e7-319">If np payment method is specified, **Check** is used by default.</span></span>

#### <a name="employment-details"></a><span data-ttu-id="d05e7-320">Töösuhte üksikasjad</span><span class="sxs-lookup"><span data-stu-id="d05e7-320">Employment details</span></span>

<span data-ttu-id="d05e7-321">Töösuhte üksikasjade ajalugu on põhiline teave, millest tuletatakse rakenduses Dayforce töövõtja palkamise, töösuhte lõpetamise ja uuesti palkamise olekud.</span><span class="sxs-lookup"><span data-stu-id="d05e7-321">Employment detail history is used as key information to derive an employee's hire, termination, and rehire statuses in Dayforce.</span></span> <span data-ttu-id="d05e7-322">Dayforce toetab korraga ainult ühte aktiivset töösuhte kirjet.</span><span class="sxs-lookup"><span data-stu-id="d05e7-322">Dayforce supports only one active employment record at a time.</span></span>

- <span data-ttu-id="d05e7-323">Töösuhte alguskuupäev (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-323">Employment start date (required)</span></span>
- <span data-ttu-id="d05e7-324">Töösuhte lõppkuupäev</span><span class="sxs-lookup"><span data-stu-id="d05e7-324">Employment end date</span></span>
- <span data-ttu-id="d05e7-325">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="d05e7-325">Start date</span></span>
- <span data-ttu-id="d05e7-326">Korrigeeritud alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="d05e7-326">Adjusted start date</span></span>
- <span data-ttu-id="d05e7-327">Töösuhte lõpetamise kuupäev (kohustuslik lõpetamisel)</span><span class="sxs-lookup"><span data-stu-id="d05e7-327">Termination date (required upon termination)</span></span>
- <span data-ttu-id="d05e7-328">Töösuhte lõpetamise põhjus (kohustuslik lõpetamisel)</span><span class="sxs-lookup"><span data-stu-id="d05e7-328">Termination reason (required upon termination)</span></span>

<span data-ttu-id="d05e7-329">Töövõtja tähtsaimad kuupäevad tuletatakse järgmisest teabest.</span><span class="sxs-lookup"><span data-stu-id="d05e7-329">An employee's key dates are derived by using the following information.</span></span>

| <span data-ttu-id="d05e7-330">Talent</span><span class="sxs-lookup"><span data-stu-id="d05e7-330">Talent</span></span>                | <span data-ttu-id="d05e7-331">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d05e7-331">Dayforce</span></span>                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d05e7-332">Kõige värskem palkamise kuupäev</span><span class="sxs-lookup"><span data-stu-id="d05e7-332">Most recent hire date</span></span> | <span data-ttu-id="d05e7-333">Praeguse lõpetamata töösuhte ajalookirje alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="d05e7-333">Employment start of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="d05e7-334">Lõpetamiskuupäev</span><span class="sxs-lookup"><span data-stu-id="d05e7-334">Termination date</span></span>      | <span data-ttu-id="d05e7-335">Praeguse lõpetamata töösuhte ajalookirje lõpetamise kuupäev</span><span class="sxs-lookup"><span data-stu-id="d05e7-335">Termination date of current non-terminated employment history record</span></span>                                 |
| <span data-ttu-id="d05e7-336">Alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="d05e7-336">Start date</span></span>            | <span data-ttu-id="d05e7-337">Korrigeeritud alguskuupäev, alguskuupäev või praeguse passiivse töösuhte ajalookirje alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="d05e7-337">Adjusted start date, start date, or employment start of current non-active employment history record</span></span> |
| <span data-ttu-id="d05e7-338">Palkamise algne kuupäev</span><span class="sxs-lookup"><span data-stu-id="d05e7-338">Original hire date</span></span>    | <span data-ttu-id="d05e7-339">Varaseima töösuhte ajalookirje alguskuupäev</span><span class="sxs-lookup"><span data-stu-id="d05e7-339">Employment start of earliest employment history record</span></span>                                               |

#### <a name="compensation"></a><span data-ttu-id="d05e7-340">Hüvitus</span><span class="sxs-lookup"><span data-stu-id="d05e7-340">Compensation</span></span>

<span data-ttu-id="d05e7-341">Tööhõiveperioodi jooksul peab iga töövõtja peamise ametikohaga olema seotud põhipalgaplaan.</span><span class="sxs-lookup"><span data-stu-id="d05e7-341">A fixed compensation plan must be associated with every employee's primary position throughout an employment period.</span></span> <span data-ttu-id="d05e7-342">See periood algab kuupäeval, mil töövõtja palgati (või töösuhte alguskuupäeval), ja jätkub kuni töösuhte lõpetamiseni.</span><span class="sxs-lookup"><span data-stu-id="d05e7-342">This period starts on the date that the employee was hired (or the employment start date) and continues until termination.</span></span>

- <span data-ttu-id="d05e7-343">Kehtivuse algus (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-343">Effective Date (required)</span></span>
- <span data-ttu-id="d05e7-344">Aegumiskuupäev</span><span class="sxs-lookup"><span data-stu-id="d05e7-344">Expiration date</span></span>
- <span data-ttu-id="d05e7-345">Palgamäär (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-345">Pay Rate (required)</span></span>
- <span data-ttu-id="d05e7-346">Palgamäära teisendamised (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-346">Pay Rate Conversions (required)</span></span>
- <span data-ttu-id="d05e7-347">Aastane vaste (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-347">Annual equivalent (required)</span></span>
- <span data-ttu-id="d05e7-348">Tunnine vaste (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-348">Hourly equivalent (required)</span></span>

<span data-ttu-id="d05e7-349">Kui tunnimääraga töövõtjal on mitu ametikohta, siis imporditakse peamise ametikoha põhipalk rakendusse Dayforce töövõtja taseme põhimäärana/-palgana.</span><span class="sxs-lookup"><span data-stu-id="d05e7-349">If an hourly employee has multiple positions, the fixed compensation of the primary position is imported into Dayforce as the employee-level base rate/salary.</span></span> <span data-ttu-id="d05e7-350">Teiseste ametikohtade puhul salvestatakse Dayforce’is tunnimäär vastava ametikoha jaoks.</span><span class="sxs-lookup"><span data-stu-id="d05e7-350">For non-primary positions, the hourly rate is saved to the corresponding position in Dayforce.</span></span>

<span data-ttu-id="d05e7-351">Kui kuupalgaga töötajal on mitu ametikohta, siis kasutatakse töövõtja taseme põhimäärana/-palgana kõikide aktiivsete ametikohtade tuletatud kumulatiivset tunnimäära ja aastapalka.</span><span class="sxs-lookup"><span data-stu-id="d05e7-351">If a salaried employee has multiple positions, the cumulative hour rate and annual salary across all active positions are derived and used as the employee-level base rate/salary.</span></span>

#### <a name="identification-numbers"></a><span data-ttu-id="d05e7-352">ID-numbrid</span><span class="sxs-lookup"><span data-stu-id="d05e7-352">Identification numbers</span></span>

##### <a name="social-security-identifier"></a><span data-ttu-id="d05e7-353">Isiku identifikaator</span><span class="sxs-lookup"><span data-stu-id="d05e7-353">Social Security identifier</span></span> 

<span data-ttu-id="d05e7-354">Igal töövõtjal peab olema üks peamine identifikaator.</span><span class="sxs-lookup"><span data-stu-id="d05e7-354">Every employee must have one primary identifier.</span></span> <span data-ttu-id="d05e7-355">Identifikaator peab olema isikukoodi- ehk **SSN**-tüüpi.</span><span class="sxs-lookup"><span data-stu-id="d05e7-355">This identifier must be of **SSN** identification type.</span></span> <span data-ttu-id="d05e7-356">Rakenduses Dayforce tuletatakse see automaatselt töövõtja isiku identifikaatorina, mis on palkamiseks vajalik.</span><span class="sxs-lookup"><span data-stu-id="d05e7-356">In Dayforce, it's automatically derived as the employee's Social Security identifier that is required for hire.</span></span>

- <span data-ttu-id="d05e7-357">Peamine isikukood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-357">Primary (required)</span></span>
- <span data-ttu-id="d05e7-358">ID tüüp = SSN</span><span class="sxs-lookup"><span data-stu-id="d05e7-358">Identification Type = "SSN"</span></span>
- <span data-ttu-id="d05e7-359">Väljastamise kuupäev</span><span class="sxs-lookup"><span data-stu-id="d05e7-359">Issued Date</span></span>
- <span data-ttu-id="d05e7-360">Aegumiskuupäev</span><span class="sxs-lookup"><span data-stu-id="d05e7-360">Expiration Date</span></span>

<span data-ttu-id="d05e7-361">Töövõtjad saavad deklareerida mitu **SSN**-identifitseerimistüüpi ID-numbrit.</span><span class="sxs-lookup"><span data-stu-id="d05e7-361">Employees can declare multiple identification numbers of the **SSN** identification type.</span></span> <span data-ttu-id="d05e7-362">Dayforce’i integreeritakse vaid tähistusega **Peamine** kirje, olenemata sellest, kas number on aktiivne või aegunud.</span><span class="sxs-lookup"><span data-stu-id="d05e7-362">However, only the record that is marked as **Primary** is integrated into Dayforce, regardless of whether the number is active or expired.</span></span>

#### <a name="bank-accounts-and-disbursements"></a><span data-ttu-id="d05e7-363">Pangakontod ja väljamaksed</span><span class="sxs-lookup"><span data-stu-id="d05e7-363">Bank accounts and disbursements</span></span>

<span data-ttu-id="d05e7-364">Iga töötaja jaoks, kes soovib oma palka pangakonto ülekandena kätte saada, tuleb sisestada kehtiv pangakonto teave.</span><span class="sxs-lookup"><span data-stu-id="d05e7-364">Valid bank account information must be entered for any employee who chooses to be paid via bank account transfers.</span></span>

| <span data-ttu-id="d05e7-365">Talent</span><span class="sxs-lookup"><span data-stu-id="d05e7-365">Talent</span></span>                         | <span data-ttu-id="d05e7-366">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d05e7-366">Dayforce</span></span>                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d05e7-367">Pangakonto number (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-367">Bank account number (required)</span></span> |                                                                                                             |
| <span data-ttu-id="d05e7-368">SWIFT-kood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-368">SWIFT code (required)</span></span>          | <span data-ttu-id="d05e7-369">Välja **Panga ID** kasutatakse palgaarvestuse töötlemiseks Mehhikos.</span><span class="sxs-lookup"><span data-stu-id="d05e7-369">**Bank ID** field used when processing payroll in Mexico.</span></span>                                                             |
| <span data-ttu-id="d05e7-370">Filiaali kood (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-370">Branch number (required)</span></span>       |                                                                                                             |
| <span data-ttu-id="d05e7-371">Pangakonto tüüp (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-371">Bank account type (required)</span></span>   | <span data-ttu-id="d05e7-372">Välja **Konto tüüp** kasutatakse palgaarvestuse töötlemiseks Mehhikos.</span><span class="sxs-lookup"><span data-stu-id="d05e7-372">**Account type** field used when processing payroll in Mexico.</span></span> <span data-ttu-id="d05e7-373">Toetatud väärtused on **Jooksevkonto** ja **Palgakonto**</span><span class="sxs-lookup"><span data-stu-id="d05e7-373">Supported values include **Checking** and **Payroll**.</span></span> |

> [!NOTE]
> <span data-ttu-id="d05e7-374">Töövõtjad, kes soovivad oma palka pangakonto ülekannetena kätte saada, peavad esitama lingi jäägikontole, mis on juriidilise isiku alluvuses, kelle peamine aadress on Mehhikos ja kes on seotud Mehhiko panga kehtiva pangakontoga.</span><span class="sxs-lookup"><span data-stu-id="d05e7-374">Employees who choose to be paid via bank account transfers must provide a link to a remainder account that is under a legal entity that has its primary address in Mexico and associated with a valid bank account from a Mexican bank.</span></span> <span data-ttu-id="d05e7-375">Kõiki ülejäänuid kontosid, mis pole jäägikontod, eiratakse.</span><span class="sxs-lookup"><span data-stu-id="d05e7-375">All other non-remainder accounts are ignored.</span></span>

#### <a name="address-information"></a><span data-ttu-id="d05e7-376">Aadressiteave</span><span class="sxs-lookup"><span data-stu-id="d05e7-376">Address information</span></span>

<span data-ttu-id="d05e7-377">Igal töövõtjal peab olema üks peamine asukoht.</span><span class="sxs-lookup"><span data-stu-id="d05e7-377">Every employee must have one primary location.</span></span> <span data-ttu-id="d05e7-378">Dayforce’is kasutatakse seda asukohta, et määratleda töövõtja peamine elukoht maksustamise tarbeks.</span><span class="sxs-lookup"><span data-stu-id="d05e7-378">In Dayforce, this location is used to determine the employee's primary residence for tax purposes.</span></span>

- <span data-ttu-id="d05e7-379">Peamine elukoht (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-379">Primary (required)</span></span>
- <span data-ttu-id="d05e7-380">Riik/regioon (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-380">Country/region (required)</span></span>
- <span data-ttu-id="d05e7-381">Sihtnumber (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-381">Zip/postal code (required)</span></span>
- <span data-ttu-id="d05e7-382">Tänava nimi (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-382">Street (required)</span></span>
- <span data-ttu-id="d05e7-383">Tänava number (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-383">Street Number (required)</span></span>
- <span data-ttu-id="d05e7-384">Hoone tähis</span><span class="sxs-lookup"><span data-stu-id="d05e7-384">Building Complement</span></span>
- <span data-ttu-id="d05e7-385">Linn (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-385">City (required)</span></span>
- <span data-ttu-id="d05e7-386">Osariik (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-386">State (required)</span></span>
- <span data-ttu-id="d05e7-387">Maakond (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-387">County (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a><span data-ttu-id="d05e7-388">Andmete konfigureerimine palgaandmete loomiseks Ameerika Ühendriikides ja Kanadas</span><span class="sxs-lookup"><span data-stu-id="d05e7-388">Configure your data to generate payroll in United States and Canada</span></span>

<span data-ttu-id="d05e7-389">Kui loote palgaandmeid Ameerika Ühendriikide või Kanada töövõtjatele, siis peate konfigureerima järgmisi elemente.</span><span class="sxs-lookup"><span data-stu-id="d05e7-389">If you're generating pay for employees in the United States and Canada, the following elements must be configured:</span></span>

- <span data-ttu-id="d05e7-390">Ametikohtadele tuleb määrata osakonnad.</span><span class="sxs-lookup"><span data-stu-id="d05e7-390">Departments are required on positions.</span></span>
- <span data-ttu-id="d05e7-391">Kulukeskused tuleb määratleda finantsdimensioonideks ja peavad olema vaike-finantsdimensiooni stringi esimene element.</span><span class="sxs-lookup"><span data-stu-id="d05e7-391">Cost centers must be set as financial dimensions and must be the first element in the default financial dimension string.</span></span>

> [!NOTE] 
> <span data-ttu-id="d05e7-392">Saate konfigureerida rakenduse Talent nõudma, et ametikohad määraksid osakonna.</span><span class="sxs-lookup"><span data-stu-id="d05e7-392">You can configure Talent to require that Positions specify a Department.</span></span> <span data-ttu-id="d05e7-393">Selleks valige **Inimressursside ühised ametikohad > Ametikohad > Nõua ametikohtade puhul osakondi**.</span><span class="sxs-lookup"><span data-stu-id="d05e7-393">To do this, go to **Human Resources Shared Positions > Positions > Require departments on positions**.</span></span> <span data-ttu-id="d05e7-394">Soovitame selle sätte integreerimiseks jõustada.</span><span class="sxs-lookup"><span data-stu-id="d05e7-394">We recommend that this setting be enforced for the integration.</span></span>

### <a name="job-types"></a><span data-ttu-id="d05e7-395">Töötüübid</span><span class="sxs-lookup"><span data-stu-id="d05e7-395">Job types</span></span>

<span data-ttu-id="d05e7-396">Töötüüpe kasutatakse sarnaste tööde kategooriatesse grupeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="d05e7-396">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="d05e7-397">Töötüübid on vajalikud palgaarvestuse töötlemiseks Ameerika Ühendriikides ja Kanadas.</span><span class="sxs-lookup"><span data-stu-id="d05e7-397">Job types are required in order to process payroll in the United States and Canada.</span></span> <span data-ttu-id="d05e7-398">Töötüübid on näiteks täistööaeg ja osaline tööaeg või kuupalk ning tunnipalk.</span><span class="sxs-lookup"><span data-stu-id="d05e7-398">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="d05e7-399">Töötüübid vastendatakse Dayforce’i tasutüüpidena, mis näitavad, kas töövõtja on tunni- või palgatöötaja.</span><span class="sxs-lookup"><span data-stu-id="d05e7-399">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="d05e7-400">Järgmised töötüübid ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="d05e7-400">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="d05e7-401">Töö tüüp</span><span class="sxs-lookup"><span data-stu-id="d05e7-401">Job type</span></span>   | <span data-ttu-id="d05e7-402">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="d05e7-402">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="d05e7-403">Tunnimäär</span><span class="sxs-lookup"><span data-stu-id="d05e7-403">Hourly</span></span>     | <span data-ttu-id="d05e7-404">Tunnimäär</span><span class="sxs-lookup"><span data-stu-id="d05e7-404">Hourly</span></span>      |
| <span data-ttu-id="d05e7-405">Põhipalk</span><span class="sxs-lookup"><span data-stu-id="d05e7-405">Salaried</span></span>   | <span data-ttu-id="d05e7-406">Põhipalk</span><span class="sxs-lookup"><span data-stu-id="d05e7-406">Salaried</span></span>    |

### <a name="position-types"></a><span data-ttu-id="d05e7-407">Ametikoha tüübid</span><span class="sxs-lookup"><span data-stu-id="d05e7-407">Position types</span></span> 

<span data-ttu-id="d05e7-408">Ametikoha tüüpe kasutatakse selleks, et kirjeldada, kas ametikoht on täiskohaga, osalise tööajaga või midagi muud.</span><span class="sxs-lookup"><span data-stu-id="d05e7-408">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="d05e7-409">Ametikoha tüübid vastendatakse Dayforce’i tasuklassidena, mis näitavad, kas töövõtja on täis- või osalise tööajaga töötaja.</span><span class="sxs-lookup"><span data-stu-id="d05e7-409">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="d05e7-410">Järgmised ametikoha tüübid ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="d05e7-410">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="d05e7-411">Ametikoha tüüp</span><span class="sxs-lookup"><span data-stu-id="d05e7-411">Position type</span></span>   | <span data-ttu-id="d05e7-412">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="d05e7-412">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="d05e7-413">Täistööaeg</span><span class="sxs-lookup"><span data-stu-id="d05e7-413">Full-time</span></span>       | <span data-ttu-id="d05e7-414">Täistööajaga töövõtja</span><span class="sxs-lookup"><span data-stu-id="d05e7-414">Full time employee</span></span> |
| <span data-ttu-id="d05e7-415">Osaline tööaeg</span><span class="sxs-lookup"><span data-stu-id="d05e7-415">Part-time</span></span>       | <span data-ttu-id="d05e7-416">Osalise tööajaga töövõtja</span><span class="sxs-lookup"><span data-stu-id="d05e7-416">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="d05e7-417">Põhjuse koodid</span><span class="sxs-lookup"><span data-stu-id="d05e7-417">Reason codes</span></span>

<span data-ttu-id="d05e7-418">Põhjusekoodid annavad teavet töövõtja oleku kohta.</span><span class="sxs-lookup"><span data-stu-id="d05e7-418">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="d05e7-419">Põhjusekoodid vastendatakse Dayforce’i olekupõhjustena, mis näitavad töövõtja ametikoha või töösuhte oleku muutuse põhjust.</span><span class="sxs-lookup"><span data-stu-id="d05e7-419">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="d05e7-420">Järgmised põhjusekoodid ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="d05e7-420">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="d05e7-421">Põhjusekood</span><span class="sxs-lookup"><span data-stu-id="d05e7-421">Reason code</span></span>    | <span data-ttu-id="d05e7-422">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="d05e7-422">Description</span></span>      | <span data-ttu-id="d05e7-423">Rakendatavad stsenaariumid</span><span class="sxs-lookup"><span data-stu-id="d05e7-423">Applicable scenarios</span></span> |
|----------------|------------------|----------------------|
| <span data-ttu-id="d05e7-424">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="d05e7-424">RESIGNATION</span></span>    | <span data-ttu-id="d05e7-425">Lahkumine</span><span class="sxs-lookup"><span data-stu-id="d05e7-425">Resignation</span></span>      | <span data-ttu-id="d05e7-426">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="d05e7-426">Terminate worker</span></span>     |
| <span data-ttu-id="d05e7-427">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="d05e7-427">TERMINATION</span></span>    | <span data-ttu-id="d05e7-428">Lõpetamine</span><span class="sxs-lookup"><span data-stu-id="d05e7-428">Termination</span></span>      | <span data-ttu-id="d05e7-429">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="d05e7-429">Terminate worker</span></span>     |
| <span data-ttu-id="d05e7-430">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="d05e7-430">RETIREMENT</span></span>     | <span data-ttu-id="d05e7-431">Pensionile jäämine</span><span class="sxs-lookup"><span data-stu-id="d05e7-431">Retirement</span></span>       | <span data-ttu-id="d05e7-432">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="d05e7-432">Terminate worker</span></span>     |
| <span data-ttu-id="d05e7-433">OTHER</span><span class="sxs-lookup"><span data-stu-id="d05e7-433">OTHER</span></span>          | <span data-ttu-id="d05e7-434">Muud põhjused</span><span class="sxs-lookup"><span data-stu-id="d05e7-434">Other Reasons</span></span>    | <span data-ttu-id="d05e7-435">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="d05e7-435">Terminate worker</span></span>     |
| <span data-ttu-id="d05e7-436">DEATH</span><span class="sxs-lookup"><span data-stu-id="d05e7-436">DEATH</span></span>          | <span data-ttu-id="d05e7-437">Surm</span><span class="sxs-lookup"><span data-stu-id="d05e7-437">Death</span></span>            | <span data-ttu-id="d05e7-438">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="d05e7-438">Terminate worker</span></span>     |
| <span data-ttu-id="d05e7-439">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="d05e7-439">LEAVEOFABSENCE</span></span> | <span data-ttu-id="d05e7-440">Puhkus</span><span class="sxs-lookup"><span data-stu-id="d05e7-440">Leave of Absence</span></span> | <span data-ttu-id="d05e7-441">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="d05e7-441">Terminate worker</span></span>     |
| <span data-ttu-id="d05e7-442">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="d05e7-442">CONTRACTEND</span></span>    | <span data-ttu-id="d05e7-443">Lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="d05e7-443">End of Contract</span></span>  | <span data-ttu-id="d05e7-444">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="d05e7-444">Terminate worker</span></span>     |
| <span data-ttu-id="d05e7-445">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="d05e7-445">SALARYCHANGE</span></span>   | <span data-ttu-id="d05e7-446">Palga muutus</span><span class="sxs-lookup"><span data-stu-id="d05e7-446">Change of Salary</span></span> | <span data-ttu-id="d05e7-447">Hüvitus</span><span class="sxs-lookup"><span data-stu-id="d05e7-447">Compensation</span></span>         |

### <a name="marital-status"></a><span data-ttu-id="d05e7-448">Perekonnaseis</span><span class="sxs-lookup"><span data-stu-id="d05e7-448">Marital status</span></span>

<span data-ttu-id="d05e7-449">Perekonnaseisu väärtused vastendatakse Dayforce’i ja tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.</span><span class="sxs-lookup"><span data-stu-id="d05e7-449">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d05e7-450">Järgmine tabel näitab, kuidas perekonnaseisu väärtusi Dayforce’i vastendatakse.</span><span class="sxs-lookup"><span data-stu-id="d05e7-450">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="d05e7-451">Talent</span><span class="sxs-lookup"><span data-stu-id="d05e7-451">Talent</span></span>                 | <span data-ttu-id="d05e7-452">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d05e7-452">Dayforce</span></span>             |
|------------------------|----------------------|
| <span data-ttu-id="d05e7-453">Abielus</span><span class="sxs-lookup"><span data-stu-id="d05e7-453">Married</span></span>                | <span data-ttu-id="d05e7-454">Abielus</span><span class="sxs-lookup"><span data-stu-id="d05e7-454">Married</span></span>              |
| <span data-ttu-id="d05e7-455">Üksik</span><span class="sxs-lookup"><span data-stu-id="d05e7-455">Single</span></span>                 | <span data-ttu-id="d05e7-456">Üksik</span><span class="sxs-lookup"><span data-stu-id="d05e7-456">Single</span></span>               |
| <span data-ttu-id="d05e7-457">Lesk</span><span class="sxs-lookup"><span data-stu-id="d05e7-457">Widowed</span></span>                | <span data-ttu-id="d05e7-458">Lesk</span><span class="sxs-lookup"><span data-stu-id="d05e7-458">Widowed</span></span>              |
| <span data-ttu-id="d05e7-459">Lahutatud</span><span class="sxs-lookup"><span data-stu-id="d05e7-459">Divorced</span></span>               | <span data-ttu-id="d05e7-460">Lahutatud</span><span class="sxs-lookup"><span data-stu-id="d05e7-460">Divorced</span></span>             |
| <span data-ttu-id="d05e7-461">Registreeritud partnerlus</span><span class="sxs-lookup"><span data-stu-id="d05e7-461">Registered Partnership</span></span> | <span data-ttu-id="d05e7-462">Mitteabieluline kooselu</span><span class="sxs-lookup"><span data-stu-id="d05e7-462">Domestic Partnership</span></span> |
| <span data-ttu-id="d05e7-463">None</span><span class="sxs-lookup"><span data-stu-id="d05e7-463">None</span></span>                   | <span data-ttu-id="d05e7-464">None</span><span class="sxs-lookup"><span data-stu-id="d05e7-464">None</span></span>                 |
| <span data-ttu-id="d05e7-465">Kooselu</span><span class="sxs-lookup"><span data-stu-id="d05e7-465">Cohabiting</span></span>             | <span data-ttu-id="d05e7-466">Kooselu</span><span class="sxs-lookup"><span data-stu-id="d05e7-466">Cohabiting</span></span>           |

### <a name="gender"></a><span data-ttu-id="d05e7-467">Sugu</span><span class="sxs-lookup"><span data-stu-id="d05e7-467">Gender</span></span>

<span data-ttu-id="d05e7-468">Soo määratlused vastendatakse Dayforce’i ja tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.</span><span class="sxs-lookup"><span data-stu-id="d05e7-468">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d05e7-469">Järgmine tabel näitab, kuidas soo määratlusi Dayforce’i vastendatakse.</span><span class="sxs-lookup"><span data-stu-id="d05e7-469">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="d05e7-470">Talent</span><span class="sxs-lookup"><span data-stu-id="d05e7-470">Talent</span></span>       | <span data-ttu-id="d05e7-471">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d05e7-471">Dayforce</span></span>        |
|--------------|-----------------|
| <span data-ttu-id="d05e7-472">Mees</span><span class="sxs-lookup"><span data-stu-id="d05e7-472">Male</span></span>         | <span data-ttu-id="d05e7-473">Mees</span><span class="sxs-lookup"><span data-stu-id="d05e7-473">Male</span></span>            |
| <span data-ttu-id="d05e7-474">Naine</span><span class="sxs-lookup"><span data-stu-id="d05e7-474">Female</span></span>       | <span data-ttu-id="d05e7-475">Naine</span><span class="sxs-lookup"><span data-stu-id="d05e7-475">Female</span></span>          |
| <span data-ttu-id="d05e7-476">Mittespetsiifiline</span><span class="sxs-lookup"><span data-stu-id="d05e7-476">Non-specific</span></span> | <span data-ttu-id="d05e7-477">*Ei toetata*</span><span class="sxs-lookup"><span data-stu-id="d05e7-477">*Not supported*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="d05e7-478">Tulukoodid</span><span class="sxs-lookup"><span data-stu-id="d05e7-478">Earning codes</span></span>

<span data-ttu-id="d05e7-479">Tulukoodid määratlevad kordumatult igat tüüpi tulud, mida töötajad saavad.</span><span class="sxs-lookup"><span data-stu-id="d05e7-479">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="d05e7-480">Koodid hõlmavad mitmeid tuludega seotud parameetreid, näiteks raamatupidamisreeglid, maksuseadused, aruandluse nõuded ja brutosumma võime.</span><span class="sxs-lookup"><span data-stu-id="d05e7-480">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="d05e7-481">Kui kasutatakse toetuseta sagedust, siis kasutatakse arvutamise jaoks vaikimisi sagedust **Iga makse**.</span><span class="sxs-lookup"><span data-stu-id="d05e7-481">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="d05e7-482">Toetatud sagedused</span><span class="sxs-lookup"><span data-stu-id="d05e7-482">Supported frequencies</span></span>

- <span data-ttu-id="d05e7-483">Kõik</span><span class="sxs-lookup"><span data-stu-id="d05e7-483">All</span></span>
- <span data-ttu-id="d05e7-484">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="d05e7-484">EVERYPAY</span></span>
- <span data-ttu-id="d05e7-485">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="d05e7-485">EACHPAYPERIOD</span></span>
- <span data-ttu-id="d05e7-486">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="d05e7-486">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="d05e7-487">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="d05e7-487">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="d05e7-488">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="d05e7-488">1OFMTH</span></span>
- <span data-ttu-id="d05e7-489">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="d05e7-489">LASTOFMTH</span></span>
- <span data-ttu-id="d05e7-490">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="d05e7-490">2OFMTH</span></span>
- <span data-ttu-id="d05e7-491">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d05e7-491">3OFMTH</span></span>
- <span data-ttu-id="d05e7-492">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d05e7-492">4OFMTH</span></span>
- <span data-ttu-id="d05e7-493">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="d05e7-493">5OFMTH</span></span>
- <span data-ttu-id="d05e7-494">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="d05e7-494">1N2OFMTH</span></span>
- <span data-ttu-id="d05e7-495">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d05e7-495">3N4OFMTH</span></span>
- <span data-ttu-id="d05e7-496">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d05e7-496">1N3OFMTH</span></span>
- <span data-ttu-id="d05e7-497">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d05e7-497">1N4OFMTH</span></span>
- <span data-ttu-id="d05e7-498">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d05e7-498">2N3OFMTH</span></span>
- <span data-ttu-id="d05e7-499">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d05e7-499">2N4OFMTH</span></span>
- <span data-ttu-id="d05e7-500">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d05e7-500">1N2N3OFMTH</span></span>
- <span data-ttu-id="d05e7-501">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d05e7-501">1N2N4OFMTH</span></span>
- <span data-ttu-id="d05e7-502">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d05e7-502">1N3N4OFMTH</span></span>
- <span data-ttu-id="d05e7-503">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d05e7-503">2N3N4OFMTH</span></span>
- <span data-ttu-id="d05e7-504">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d05e7-504">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="d05e7-505">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="d05e7-505">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="d05e7-506">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="d05e7-506">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="d05e7-507">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="d05e7-507">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="d05e7-508">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="d05e7-508">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="d05e7-509">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="d05e7-509">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="d05e7-510">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="d05e7-510">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="d05e7-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="d05e7-511">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="d05e7-512">Aadressid</span><span class="sxs-lookup"><span data-stu-id="d05e7-512">Addresses</span></span>

<span data-ttu-id="d05e7-513">Teatud riigi või regiooni, osariigi ja maakonna (haldusüksuse) koodide tuvastamise jaoks on vaja kindlaid vorminguid, mida Dayforce ning riigi-/regioonisisesed pakkujad ära tunnevad.</span><span class="sxs-lookup"><span data-stu-id="d05e7-513">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="d05e7-514">Kuigi linnade vorming on paindlik, peab iga linn olema seotud osariigiga.</span><span class="sxs-lookup"><span data-stu-id="d05e7-514">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="d05e7-515">Talent</span><span class="sxs-lookup"><span data-stu-id="d05e7-515">Talent</span></span>          | <span data-ttu-id="d05e7-516">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d05e7-516">Dayforce</span></span>              |
|-----------------|-----------------------|
| <span data-ttu-id="d05e7-517">Riik/regioon</span><span class="sxs-lookup"><span data-stu-id="d05e7-517">Country/Region</span></span>  | <span data-ttu-id="d05e7-518">Riigi kood</span><span class="sxs-lookup"><span data-stu-id="d05e7-518">Country Code</span></span>          |
| <span data-ttu-id="d05e7-519">Sihtnumber</span><span class="sxs-lookup"><span data-stu-id="d05e7-519">Zip/Postal Code</span></span> | <span data-ttu-id="d05e7-520">Sihtnumber</span><span class="sxs-lookup"><span data-stu-id="d05e7-520">Postal Code</span></span>           |
| <span data-ttu-id="d05e7-521">Osariik</span><span class="sxs-lookup"><span data-stu-id="d05e7-521">State</span></span>           | <span data-ttu-id="d05e7-522">Osariigi kood</span><span class="sxs-lookup"><span data-stu-id="d05e7-522">State Code</span></span>            |
| <span data-ttu-id="d05e7-523">Linn</span><span class="sxs-lookup"><span data-stu-id="d05e7-523">City</span></span>            | <span data-ttu-id="d05e7-524">Linn</span><span class="sxs-lookup"><span data-stu-id="d05e7-524">City</span></span>                  |
| <span data-ttu-id="d05e7-525">Maakond</span><span class="sxs-lookup"><span data-stu-id="d05e7-525">County</span></span>          | <span data-ttu-id="d05e7-526">Maakond (haldusüksus)</span><span class="sxs-lookup"><span data-stu-id="d05e7-526">County (Municipality)</span></span> |
| <span data-ttu-id="d05e7-527">Tänav</span><span class="sxs-lookup"><span data-stu-id="d05e7-527">Street</span></span>          | <span data-ttu-id="d05e7-528">Aadressirida 1</span><span class="sxs-lookup"><span data-stu-id="d05e7-528">Address Line 1</span></span>        |

### <a name="tax-regions"></a><span data-ttu-id="d05e7-529">Maksuregioonid</span><span class="sxs-lookup"><span data-stu-id="d05e7-529">Tax regions</span></span>

<span data-ttu-id="d05e7-530">Maksuregioone kasutatakse palga loomisel sobiva maksu määramiseks.</span><span class="sxs-lookup"><span data-stu-id="d05e7-530">Tax regions are used to determine the appropriate tax that should be applied during payroll generation.</span></span> <span data-ttu-id="d05e7-531">Maksuregioonid vastendatakse Dayforce’i asukoha-aadressidena.</span><span class="sxs-lookup"><span data-stu-id="d05e7-531">Tax regions are mapped to Dayforce as location addresses.</span></span> <span data-ttu-id="d05e7-532">Maksuregiooni vaikevariant peab olema seotud töötaja aktiivse ametikohaga.</span><span class="sxs-lookup"><span data-stu-id="d05e7-532">The default tax region must be associated with the worker's active position.</span></span> 

- <span data-ttu-id="d05e7-533">Maksuregioon (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-533">Tax region (required)</span></span>
- <span data-ttu-id="d05e7-534">Riik/regioon (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-534">Country/Region (required)</span></span>
- <span data-ttu-id="d05e7-535">Osariik (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-535">State (required)</span></span>
- <span data-ttu-id="d05e7-536">Maakond</span><span class="sxs-lookup"><span data-stu-id="d05e7-536">County</span></span> 
- <span data-ttu-id="d05e7-537">Linn (kohustuslik)</span><span class="sxs-lookup"><span data-stu-id="d05e7-537">City (required)</span></span>

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a><span data-ttu-id="d05e7-538">Andmete konfigureerimine palgaandmete loomiseks Mehhikos</span><span class="sxs-lookup"><span data-stu-id="d05e7-538">Configure your data to generate payroll in Mexico</span></span>

<span data-ttu-id="d05e7-539">Kui loote palgaandmeid Mehhiko töövõtjatele, siis peate konfigureerima järgmisi elemente.</span><span class="sxs-lookup"><span data-stu-id="d05e7-539">If you're generating pay for employees in Mexico, the following elements must be configured:</span></span>

- <span data-ttu-id="d05e7-540">Ametikohtadele tuleb määrata osakonnad.</span><span class="sxs-lookup"><span data-stu-id="d05e7-540">Departments are required on positions.</span></span>
- <span data-ttu-id="d05e7-541">Kulukeskused tuleb määratleda finantsdimensioonideks ja peavad olema vaike-finantsdimensiooni stringi esimene element.</span><span class="sxs-lookup"><span data-stu-id="d05e7-541">Cost centers must be set as financial dimensions and must be the first element in the Default Financial Dimension string.</span></span>

### <a name="job-types"></a><span data-ttu-id="d05e7-542">Töötüübid</span><span class="sxs-lookup"><span data-stu-id="d05e7-542">Job types</span></span>

<span data-ttu-id="d05e7-543">Töötüüpe kasutatakse sarnaste tööde kategooriatesse grupeerimiseks.</span><span class="sxs-lookup"><span data-stu-id="d05e7-543">Job types are used to group similar jobs into categories.</span></span> <span data-ttu-id="d05e7-544">Mehhikos palgaarvestuse töötlemiseks on vajalikud töötüübid.</span><span class="sxs-lookup"><span data-stu-id="d05e7-544">Job types are required in order to process payroll in Mexico.</span></span> <span data-ttu-id="d05e7-545">Töötüübid on näiteks täistööaeg ja osaline tööaeg või kuupalk ning tunnipalk.</span><span class="sxs-lookup"><span data-stu-id="d05e7-545">Examples of job types include full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="d05e7-546">Töötüübid vastendatakse Dayforce’i tasutüüpidena, mis näitavad, kas töövõtja on tunni- või palgatöötaja.</span><span class="sxs-lookup"><span data-stu-id="d05e7-546">Job types are mapped to Dayforce as pay types that indicate whether an employee is hourly or salaried.</span></span>

<span data-ttu-id="d05e7-547">Järgmised töötüübid ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="d05e7-547">The following job types and descriptions are required.</span></span>

| <span data-ttu-id="d05e7-548">Töö tüüp</span><span class="sxs-lookup"><span data-stu-id="d05e7-548">Job type</span></span>   | <span data-ttu-id="d05e7-549">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="d05e7-549">Description</span></span> |
|------------|-------------|
| <span data-ttu-id="d05e7-550">Tunnimäär</span><span class="sxs-lookup"><span data-stu-id="d05e7-550">Hourly</span></span>     | <span data-ttu-id="d05e7-551">MX tunnimäär</span><span class="sxs-lookup"><span data-stu-id="d05e7-551">MX Hourly</span></span>   |
| <span data-ttu-id="d05e7-552">Põhipalk</span><span class="sxs-lookup"><span data-stu-id="d05e7-552">Salaried</span></span>   | <span data-ttu-id="d05e7-553">MX põhipalk</span><span class="sxs-lookup"><span data-stu-id="d05e7-553">MX Salaried</span></span> |

### <a name="position-types"></a><span data-ttu-id="d05e7-554">Positsioonitüübid</span><span class="sxs-lookup"><span data-stu-id="d05e7-554">Position types</span></span> 

<span data-ttu-id="d05e7-555">Ametikoha tüüpe kasutatakse selleks, et kirjeldada, kas ametikoht on täiskohaga, osalise tööajaga või midagi muud.</span><span class="sxs-lookup"><span data-stu-id="d05e7-555">You use position types to describe whether the position is full-time, part-time, or something else.</span></span> <span data-ttu-id="d05e7-556">Ametikoha tüübid vastendatakse Dayforce’i tasuklassidena, mis näitavad, kas töövõtja on täis- või osalise tööajaga töötaja.</span><span class="sxs-lookup"><span data-stu-id="d05e7-556">Position types are mapped to Dayforce as pay classes that indicate whether an employee is full-time or part-time.</span></span>

<span data-ttu-id="d05e7-557">Järgmised ametikoha tüübid ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="d05e7-557">The following position types and descriptions are required.</span></span>

| <span data-ttu-id="d05e7-558">Ametikoha tüüp</span><span class="sxs-lookup"><span data-stu-id="d05e7-558">Position type</span></span>   | <span data-ttu-id="d05e7-559">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="d05e7-559">Description</span></span>        |
|-----------------|--------------------|
| <span data-ttu-id="d05e7-560">Täistööaeg</span><span class="sxs-lookup"><span data-stu-id="d05e7-560">Full-time</span></span>       | <span data-ttu-id="d05e7-561">Täistööajaga töövõtja</span><span class="sxs-lookup"><span data-stu-id="d05e7-561">Full time employee</span></span> |
| <span data-ttu-id="d05e7-562">Osaline tööaeg</span><span class="sxs-lookup"><span data-stu-id="d05e7-562">Part-time</span></span>       | <span data-ttu-id="d05e7-563">Osalise tööajaga töövõtja</span><span class="sxs-lookup"><span data-stu-id="d05e7-563">Part time employee</span></span> |

### <a name="reason-codes"></a><span data-ttu-id="d05e7-564">Põhjuse koodid</span><span class="sxs-lookup"><span data-stu-id="d05e7-564">Reason codes</span></span>

<span data-ttu-id="d05e7-565">Põhjusekoodid annavad teavet töövõtja oleku kohta.</span><span class="sxs-lookup"><span data-stu-id="d05e7-565">Reason codes provide information about the status of an employee.</span></span> <span data-ttu-id="d05e7-566">Põhjusekoodid vastendatakse Dayforce’i olekupõhjustena, mis näitavad töövõtja ametikoha või töösuhte oleku muutuse põhjust.</span><span class="sxs-lookup"><span data-stu-id="d05e7-566">Reason codes are mapped to Dayforce as status reasons that indicate the reason for changes to an employee's position or employment status.</span></span>

<span data-ttu-id="d05e7-567">Järgmised põhjusekoodid ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="d05e7-567">The following reason codes and descriptions are required.</span></span>

| <span data-ttu-id="d05e7-568">Põhjusekood</span><span class="sxs-lookup"><span data-stu-id="d05e7-568">Reason code</span></span>            | <span data-ttu-id="d05e7-569">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="d05e7-569">Description</span></span>                    | <span data-ttu-id="d05e7-570">Rakendatavad stsenaariumid</span><span class="sxs-lookup"><span data-stu-id="d05e7-570">Applicable scenarios</span></span> |
|------------------------|--------------------------------|----------------------|
| <span data-ttu-id="d05e7-571">DEPARTUREBEFOREPAYMENT</span><span class="sxs-lookup"><span data-stu-id="d05e7-571">DEPARTUREBEFOREPAYMENT</span></span> | <span data-ttu-id="d05e7-572">Lahkumine enne esimest palgamakset</span><span class="sxs-lookup"><span data-stu-id="d05e7-572">Departure before first payroll</span></span> | <span data-ttu-id="d05e7-573">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="d05e7-573">Terminate worker</span></span>     |
| <span data-ttu-id="d05e7-574">RESIGNATION</span><span class="sxs-lookup"><span data-stu-id="d05e7-574">RESIGNATION</span></span>            | <span data-ttu-id="d05e7-575">Lahkumine</span><span class="sxs-lookup"><span data-stu-id="d05e7-575">Resignation</span></span>                    | <span data-ttu-id="d05e7-576">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="d05e7-576">Terminate worker</span></span>     |
| <span data-ttu-id="d05e7-577">PENSION</span><span class="sxs-lookup"><span data-stu-id="d05e7-577">PENSION</span></span>                | <span data-ttu-id="d05e7-578">Pension</span><span class="sxs-lookup"><span data-stu-id="d05e7-578">Pension</span></span>                        | <span data-ttu-id="d05e7-579">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="d05e7-579">Terminate worker</span></span>     |
| <span data-ttu-id="d05e7-580">TERMINATION</span><span class="sxs-lookup"><span data-stu-id="d05e7-580">TERMINATION</span></span>            | <span data-ttu-id="d05e7-581">Lõpetamine</span><span class="sxs-lookup"><span data-stu-id="d05e7-581">Termination</span></span>                    | <span data-ttu-id="d05e7-582">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="d05e7-582">Terminate worker</span></span>     |
| <span data-ttu-id="d05e7-583">RETIREMENT</span><span class="sxs-lookup"><span data-stu-id="d05e7-583">RETIREMENT</span></span>             | <span data-ttu-id="d05e7-584">Pensionile jäämine</span><span class="sxs-lookup"><span data-stu-id="d05e7-584">Retirement</span></span>                     | <span data-ttu-id="d05e7-585">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="d05e7-585">Terminate worker</span></span>     |
| <span data-ttu-id="d05e7-586">ABSENTEE</span><span class="sxs-lookup"><span data-stu-id="d05e7-586">ABSENTEE</span></span>               | <span data-ttu-id="d05e7-587">Puuduja</span><span class="sxs-lookup"><span data-stu-id="d05e7-587">Absentee</span></span>                       | <span data-ttu-id="d05e7-588">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="d05e7-588">Terminate worker</span></span>     |
| <span data-ttu-id="d05e7-589">OTHER</span><span class="sxs-lookup"><span data-stu-id="d05e7-589">OTHER</span></span>                  | <span data-ttu-id="d05e7-590">Muud põhjused</span><span class="sxs-lookup"><span data-stu-id="d05e7-590">Other Reasons</span></span>                  | <span data-ttu-id="d05e7-591">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="d05e7-591">Terminate worker</span></span>     |
| <span data-ttu-id="d05e7-592">CLOSURE</span><span class="sxs-lookup"><span data-stu-id="d05e7-592">CLOSURE</span></span>                | <span data-ttu-id="d05e7-593">Ettevõte suletud</span><span class="sxs-lookup"><span data-stu-id="d05e7-593">Business Closure</span></span>               | <span data-ttu-id="d05e7-594">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="d05e7-594">Terminate worker</span></span>     |
| <span data-ttu-id="d05e7-595">DEATH</span><span class="sxs-lookup"><span data-stu-id="d05e7-595">DEATH</span></span>                  | <span data-ttu-id="d05e7-596">Surm</span><span class="sxs-lookup"><span data-stu-id="d05e7-596">Death</span></span>                          | <span data-ttu-id="d05e7-597">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="d05e7-597">Terminate worker</span></span>     |
| <span data-ttu-id="d05e7-598">LEAVEOFABSENCE</span><span class="sxs-lookup"><span data-stu-id="d05e7-598">LEAVEOFABSENCE</span></span>         | <span data-ttu-id="d05e7-599">Puhkus</span><span class="sxs-lookup"><span data-stu-id="d05e7-599">Leave of Absence</span></span>               | <span data-ttu-id="d05e7-600">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="d05e7-600">Terminate worker</span></span>     |
| <span data-ttu-id="d05e7-601">CONTRACTEND</span><span class="sxs-lookup"><span data-stu-id="d05e7-601">CONTRACTEND</span></span>            | <span data-ttu-id="d05e7-602">Lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="d05e7-602">End of Contract</span></span>                | <span data-ttu-id="d05e7-603">Töötajaga lepingu lõpetamine</span><span class="sxs-lookup"><span data-stu-id="d05e7-603">Terminate worker</span></span>     |
| <span data-ttu-id="d05e7-604">SALARYCHANGE</span><span class="sxs-lookup"><span data-stu-id="d05e7-604">SALARYCHANGE</span></span>           | <span data-ttu-id="d05e7-605">Palga muutus</span><span class="sxs-lookup"><span data-stu-id="d05e7-605">Change of Salary</span></span>               | <span data-ttu-id="d05e7-606">Hüvitus</span><span class="sxs-lookup"><span data-stu-id="d05e7-606">Compensation</span></span>         |

### <a name="terms-of-employment"></a><span data-ttu-id="d05e7-607">Töösuhte tingimused</span><span class="sxs-lookup"><span data-stu-id="d05e7-607">Terms of employment</span></span>

<span data-ttu-id="d05e7-608">Töösuhte tingimusi kasutatakse töösuhte tingimuste kategooriate loomiseks.</span><span class="sxs-lookup"><span data-stu-id="d05e7-608">Terms of employment are used to create categories of employment terms.</span></span> <span data-ttu-id="d05e7-609">Tingimused vastendatakse Dayforce’i töösuhte indikaatorväärtustena.</span><span class="sxs-lookup"><span data-stu-id="d05e7-609">The terms are mapped to Dayforce as employment indicator values.</span></span>

<span data-ttu-id="d05e7-610">Järgmised töösuhte tingimused ja kirjeldused on kohustuslikud.</span><span class="sxs-lookup"><span data-stu-id="d05e7-610">The following terms of employment and descriptions are required.</span></span>

| <span data-ttu-id="d05e7-611">Töösuhte tingimused</span><span class="sxs-lookup"><span data-stu-id="d05e7-611">Terms of employment</span></span>   | <span data-ttu-id="d05e7-612">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="d05e7-612">Description</span></span> |
|-----------------------|-------------|
| <span data-ttu-id="d05e7-613">Tavaline</span><span class="sxs-lookup"><span data-stu-id="d05e7-613">Regular</span></span>               | <span data-ttu-id="d05e7-614">Tavaline</span><span class="sxs-lookup"><span data-stu-id="d05e7-614">Regular</span></span>     |
| <span data-ttu-id="d05e7-615">Otse</span><span class="sxs-lookup"><span data-stu-id="d05e7-615">Direct</span></span>                | <span data-ttu-id="d05e7-616">Otse</span><span class="sxs-lookup"><span data-stu-id="d05e7-616">Direct</span></span>      |
| <span data-ttu-id="d05e7-617">Praktika</span><span class="sxs-lookup"><span data-stu-id="d05e7-617">Internship</span></span>            | <span data-ttu-id="d05e7-618">Praktika</span><span class="sxs-lookup"><span data-stu-id="d05e7-618">Internship</span></span>  |
| <span data-ttu-id="d05e7-619">Alaline</span><span class="sxs-lookup"><span data-stu-id="d05e7-619">Permanent</span></span>             | <span data-ttu-id="d05e7-620">Alaline</span><span class="sxs-lookup"><span data-stu-id="d05e7-620">Permanent</span></span>   |

### <a name="marital-status"></a><span data-ttu-id="d05e7-621">Perekonnaseis</span><span class="sxs-lookup"><span data-stu-id="d05e7-621">Marital status</span></span>

<span data-ttu-id="d05e7-622">Perekonnaseisu väärtused vastendatakse Dayforce’i ja tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.</span><span class="sxs-lookup"><span data-stu-id="d05e7-622">Marital status values are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d05e7-623">Järgmine tabel näitab, kuidas perekonnaseisu väärtusi Dayforce’i vastendatakse.</span><span class="sxs-lookup"><span data-stu-id="d05e7-623">The following table shows how marital status values are mapped to Dayforce.</span></span>

| <span data-ttu-id="d05e7-624">Talent</span><span class="sxs-lookup"><span data-stu-id="d05e7-624">Talent</span></span>                 | <span data-ttu-id="d05e7-625">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d05e7-625">Dayforce</span></span>                  |
|------------------------|---------------------------|
| <span data-ttu-id="d05e7-626">Abielus</span><span class="sxs-lookup"><span data-stu-id="d05e7-626">Married</span></span>                | <span data-ttu-id="d05e7-627">Abielus</span><span class="sxs-lookup"><span data-stu-id="d05e7-627">Married</span></span>                   |
| <span data-ttu-id="d05e7-628">Üksik</span><span class="sxs-lookup"><span data-stu-id="d05e7-628">Single</span></span>                 | <span data-ttu-id="d05e7-629">Üksik</span><span class="sxs-lookup"><span data-stu-id="d05e7-629">Single</span></span>                    |
| <span data-ttu-id="d05e7-630">Lesk</span><span class="sxs-lookup"><span data-stu-id="d05e7-630">Widowed</span></span>                | <span data-ttu-id="d05e7-631">Lesk</span><span class="sxs-lookup"><span data-stu-id="d05e7-631">Widowed</span></span>                   |
| <span data-ttu-id="d05e7-632">Lahutatud</span><span class="sxs-lookup"><span data-stu-id="d05e7-632">Divorced</span></span>               | <span data-ttu-id="d05e7-633">Lahutatud</span><span class="sxs-lookup"><span data-stu-id="d05e7-633">Divorced</span></span>                  |
| <span data-ttu-id="d05e7-634">Registreeritud partnerlus</span><span class="sxs-lookup"><span data-stu-id="d05e7-634">Registered Partnership</span></span> | <span data-ttu-id="d05e7-635">Mitteabieluline kooselu</span><span class="sxs-lookup"><span data-stu-id="d05e7-635">Domestic Partnership</span></span>      |
| <span data-ttu-id="d05e7-636">None</span><span class="sxs-lookup"><span data-stu-id="d05e7-636">None</span></span>                   | <span data-ttu-id="d05e7-637">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="d05e7-637">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="d05e7-638">Kooselu</span><span class="sxs-lookup"><span data-stu-id="d05e7-638">Cohabiting</span></span>             | <span data-ttu-id="d05e7-639">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="d05e7-639">*Not supported by Mexico*</span></span> |

### <a name="gender"></a><span data-ttu-id="d05e7-640">Sugu</span><span class="sxs-lookup"><span data-stu-id="d05e7-640">Gender</span></span>

<span data-ttu-id="d05e7-641">Soo määratlused vastendatakse Dayforce’i ja tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.</span><span class="sxs-lookup"><span data-stu-id="d05e7-641">Gender designations are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d05e7-642">Järgmine tabel näitab, kuidas soo määratlusi Dayforce’i vastendatakse.</span><span class="sxs-lookup"><span data-stu-id="d05e7-642">The following table shows how gender designations are mapped to Dayforce.</span></span>

| <span data-ttu-id="d05e7-643">Talent</span><span class="sxs-lookup"><span data-stu-id="d05e7-643">Talent</span></span>       | <span data-ttu-id="d05e7-644">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d05e7-644">Dayforce</span></span>                  |
|--------------|---------------------------|
| <span data-ttu-id="d05e7-645">Mees</span><span class="sxs-lookup"><span data-stu-id="d05e7-645">Male</span></span>         | <span data-ttu-id="d05e7-646">Mees</span><span class="sxs-lookup"><span data-stu-id="d05e7-646">Male</span></span>                      |
| <span data-ttu-id="d05e7-647">Naine</span><span class="sxs-lookup"><span data-stu-id="d05e7-647">Female</span></span>       | <span data-ttu-id="d05e7-648">Naine</span><span class="sxs-lookup"><span data-stu-id="d05e7-648">Female</span></span>                    |
| <span data-ttu-id="d05e7-649">Mittespetsiifiline</span><span class="sxs-lookup"><span data-stu-id="d05e7-649">Non-specific</span></span> | <span data-ttu-id="d05e7-650">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="d05e7-650">*Not supported by Mexico*</span></span> |

### <a name="payment-method"></a><span data-ttu-id="d05e7-651">Makseviis</span><span class="sxs-lookup"><span data-stu-id="d05e7-651">Payment method</span></span>

<span data-ttu-id="d05e7-652">Makseviisid võimaldavad töövõtjal ja ettevõttel kirjeldada, kuidas töövõtjatele makstakse.</span><span class="sxs-lookup"><span data-stu-id="d05e7-652">Payment methods give the employee and the company a way to describe how employees will be paid.</span></span> <span data-ttu-id="d05e7-653">Makseviisid vastendatakse Dayforce’i ja tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.</span><span class="sxs-lookup"><span data-stu-id="d05e7-653">Payment methods are mapped to Dayforce and translated, as appropriate, to the accepted values upon integration.</span></span>

<span data-ttu-id="d05e7-654">Järgmine tabel näitab, kuidas makseviise Dayforce’i vastendatakse.</span><span class="sxs-lookup"><span data-stu-id="d05e7-654">The following table shows how payment methods are mapped to Dayforce.</span></span>

| <span data-ttu-id="d05e7-655">Talent</span><span class="sxs-lookup"><span data-stu-id="d05e7-655">Talent</span></span>             | <span data-ttu-id="d05e7-656">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d05e7-656">Dayforce</span></span>                  |
|--------------------|---------------------------|
| <span data-ttu-id="d05e7-657">Sularaha</span><span class="sxs-lookup"><span data-stu-id="d05e7-657">Cash</span></span>               | <span data-ttu-id="d05e7-658">Sularaha</span><span class="sxs-lookup"><span data-stu-id="d05e7-658">Cash</span></span>                      |
| <span data-ttu-id="d05e7-659">Elektrooniline makse</span><span class="sxs-lookup"><span data-stu-id="d05e7-659">Electronic Payment</span></span> | <span data-ttu-id="d05e7-660">Ülekanne</span><span class="sxs-lookup"><span data-stu-id="d05e7-660">Transfer</span></span>                  |
| <span data-ttu-id="d05e7-661">Kontrolli</span><span class="sxs-lookup"><span data-stu-id="d05e7-661">Check</span></span>              | <span data-ttu-id="d05e7-662">Tšekk</span><span class="sxs-lookup"><span data-stu-id="d05e7-662">Cheque</span></span>                    |
| <span data-ttu-id="d05e7-663">Pangaveksel</span><span class="sxs-lookup"><span data-stu-id="d05e7-663">Bank Draft</span></span>         | <span data-ttu-id="d05e7-664">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="d05e7-664">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="d05e7-665">Muud</span><span class="sxs-lookup"><span data-stu-id="d05e7-665">Other</span></span>              | <span data-ttu-id="d05e7-666">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="d05e7-666">*Not supported by Mexico*</span></span> |

### <a name="bank-account-type"></a><span data-ttu-id="d05e7-667">Pangakonto tüüp</span><span class="sxs-lookup"><span data-stu-id="d05e7-667">Bank account type</span></span>

<span data-ttu-id="d05e7-668">Pangakonto tüüpe kasutatakse elektrooniliste maksete tegemiseks töötajatele.</span><span class="sxs-lookup"><span data-stu-id="d05e7-668">Bank account types are used for electronic payments to employees.</span></span> <span data-ttu-id="d05e7-669">Pangakonto tüübid vastendatakse Dayforce’i ülekandekonto teabena.</span><span class="sxs-lookup"><span data-stu-id="d05e7-669">Bank account types are mapped to Dayforce as transfer account information.</span></span> <span data-ttu-id="d05e7-670">Pangakonto tüübid tõlgitakse vajaduse korral integreerimise ajal sobivateks väärtusteks.</span><span class="sxs-lookup"><span data-stu-id="d05e7-670">The bank account types are translated, as appropriate, to the accepted values upon integration.</span></span>

| <span data-ttu-id="d05e7-671">Talent</span><span class="sxs-lookup"><span data-stu-id="d05e7-671">Talent</span></span>            | <span data-ttu-id="d05e7-672">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d05e7-672">Dayforce</span></span>                  |
|-------------------|---------------------------|
| <span data-ttu-id="d05e7-673">Jooksevkonto</span><span class="sxs-lookup"><span data-stu-id="d05e7-673">Checking Account</span></span>  | <span data-ttu-id="d05e7-674">Jooksevkonto</span><span class="sxs-lookup"><span data-stu-id="d05e7-674">CheckingAccount</span></span>           |
| <span data-ttu-id="d05e7-675">Palgakonto</span><span class="sxs-lookup"><span data-stu-id="d05e7-675">Payroll Account</span></span>   | <span data-ttu-id="d05e7-676">Palgakonto</span><span class="sxs-lookup"><span data-stu-id="d05e7-676">PayrollAccount</span></span>            |
| <span data-ttu-id="d05e7-677">Hoiukonto</span><span class="sxs-lookup"><span data-stu-id="d05e7-677">Savings Account</span></span>   | <span data-ttu-id="d05e7-678">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="d05e7-678">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="d05e7-679">BankGiroti konto</span><span class="sxs-lookup"><span data-stu-id="d05e7-679">BankGirot account</span></span> | <span data-ttu-id="d05e7-680">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="d05e7-680">*Not supported by Mexico*</span></span> |
| <span data-ttu-id="d05e7-681">PlusGiroti konto</span><span class="sxs-lookup"><span data-stu-id="d05e7-681">PlusGirot account</span></span> | <span data-ttu-id="d05e7-682">*Pole Mehhikos toetatud*</span><span class="sxs-lookup"><span data-stu-id="d05e7-682">*Not supported by Mexico*</span></span> |

### <a name="earning-codes"></a><span data-ttu-id="d05e7-683">Tulukoodid</span><span class="sxs-lookup"><span data-stu-id="d05e7-683">Earning codes</span></span>

<span data-ttu-id="d05e7-684">Tulukoodid määratlevad kordumatult igat tüüpi tulud, mida töötajad saavad.</span><span class="sxs-lookup"><span data-stu-id="d05e7-684">Earning codes uniquely identify every type of earnings that workers receive.</span></span> <span data-ttu-id="d05e7-685">Koodid hõlmavad mitmeid tuludega seotud parameetreid, näiteks raamatupidamisreeglid, maksuseadused, aruandluse nõuded ja brutosumma võime.</span><span class="sxs-lookup"><span data-stu-id="d05e7-685">The codes cover several parameters that are related to earnings, such as accounting rules, tax laws, reporting requirements, and gross-up capability.</span></span> <span data-ttu-id="d05e7-686">Kui kasutatakse toetuseta sagedust, siis kasutatakse arvutamise jaoks vaikimisi sagedust **Iga makse**.</span><span class="sxs-lookup"><span data-stu-id="d05e7-686">If an unsupported frequency is used, the **Every Pay** frequency is used by default for the calculation.</span></span>

#### <a name="supported-frequencies"></a><span data-ttu-id="d05e7-687">Toetatud sagedused</span><span class="sxs-lookup"><span data-stu-id="d05e7-687">Supported frequencies</span></span>

- <span data-ttu-id="d05e7-688">Kõik</span><span class="sxs-lookup"><span data-stu-id="d05e7-688">All</span></span>
- <span data-ttu-id="d05e7-689">EVERYPAY</span><span class="sxs-lookup"><span data-stu-id="d05e7-689">EVERYPAY</span></span>
- <span data-ttu-id="d05e7-690">EACHPAYPERIOD</span><span class="sxs-lookup"><span data-stu-id="d05e7-690">EACHPAYPERIOD</span></span>
- <span data-ttu-id="d05e7-691">EVRYOTHRPAYODD</span><span class="sxs-lookup"><span data-stu-id="d05e7-691">EVRYOTHRPAYODD</span></span>
- <span data-ttu-id="d05e7-692">EVRYOTHRPAYEVN</span><span class="sxs-lookup"><span data-stu-id="d05e7-692">EVRYOTHRPAYEVN</span></span>
- <span data-ttu-id="d05e7-693">1OFMTH</span><span class="sxs-lookup"><span data-stu-id="d05e7-693">1OFMTH</span></span>
- <span data-ttu-id="d05e7-694">LASTOFMTH</span><span class="sxs-lookup"><span data-stu-id="d05e7-694">LASTOFMTH</span></span>
- <span data-ttu-id="d05e7-695">2OFMTH</span><span class="sxs-lookup"><span data-stu-id="d05e7-695">2OFMTH</span></span>
- <span data-ttu-id="d05e7-696">3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d05e7-696">3OFMTH</span></span>
- <span data-ttu-id="d05e7-697">4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d05e7-697">4OFMTH</span></span>
- <span data-ttu-id="d05e7-698">5OFMTH</span><span class="sxs-lookup"><span data-stu-id="d05e7-698">5OFMTH</span></span>
- <span data-ttu-id="d05e7-699">1N2OFMTH</span><span class="sxs-lookup"><span data-stu-id="d05e7-699">1N2OFMTH</span></span>
- <span data-ttu-id="d05e7-700">3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d05e7-700">3N4OFMTH</span></span>
- <span data-ttu-id="d05e7-701">1N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d05e7-701">1N3OFMTH</span></span>
- <span data-ttu-id="d05e7-702">1N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d05e7-702">1N4OFMTH</span></span>
- <span data-ttu-id="d05e7-703">2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d05e7-703">2N3OFMTH</span></span>
- <span data-ttu-id="d05e7-704">2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d05e7-704">2N4OFMTH</span></span>
- <span data-ttu-id="d05e7-705">1N2N3OFMTH</span><span class="sxs-lookup"><span data-stu-id="d05e7-705">1N2N3OFMTH</span></span>
- <span data-ttu-id="d05e7-706">1N2N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d05e7-706">1N2N4OFMTH</span></span>
- <span data-ttu-id="d05e7-707">1N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d05e7-707">1N3N4OFMTH</span></span>
- <span data-ttu-id="d05e7-708">2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d05e7-708">2N3N4OFMTH</span></span>
- <span data-ttu-id="d05e7-709">1N2N3N4OFMTH - 1N2N3N4OFMTH</span><span class="sxs-lookup"><span data-stu-id="d05e7-709">1N2N3N4OFMTH - 1N2N3N4OFMTH</span></span>
- <span data-ttu-id="d05e7-710">2N3N4N5OFMth - 2N3N4N5OFMth</span><span class="sxs-lookup"><span data-stu-id="d05e7-710">2N3N4N5OFMth - 2N3N4N5OFMth</span></span>
- <span data-ttu-id="d05e7-711">1OFQTR - 1OFQTR</span><span class="sxs-lookup"><span data-stu-id="d05e7-711">1OFQTR - 1OFQTR</span></span>
- <span data-ttu-id="d05e7-712">LASTOFQTR – LASTOFQTR</span><span class="sxs-lookup"><span data-stu-id="d05e7-712">LASTOFQTR – LASTOFQTR</span></span>
- <span data-ttu-id="d05e7-713">LASTMTHOFQTR – LASTMTHOFQTR</span><span class="sxs-lookup"><span data-stu-id="d05e7-713">LASTMTHOFQTR – LASTMTHOFQTR</span></span>
- <span data-ttu-id="d05e7-714">1OFYEAR - 1OFYEAR</span><span class="sxs-lookup"><span data-stu-id="d05e7-714">1OFYEAR - 1OFYEAR</span></span>
- <span data-ttu-id="d05e7-715">LASTOFYEAR – LASTOFYEAR</span><span class="sxs-lookup"><span data-stu-id="d05e7-715">LASTOFYEAR – LASTOFYEAR</span></span>
- <span data-ttu-id="d05e7-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span><span class="sxs-lookup"><span data-stu-id="d05e7-716">NOVNDECOFYEAR - NOVNDECOFYEAR</span></span>

### <a name="addresses"></a><span data-ttu-id="d05e7-717">Aadressid</span><span class="sxs-lookup"><span data-stu-id="d05e7-717">Addresses</span></span>

<span data-ttu-id="d05e7-718">Teatud riigi või regiooni, osariigi ja maakonna (haldusüksuse) koodide tuvastamise jaoks on vaja kindlaid vorminguid, mida Dayforce ning riigi-/regioonisisesed pakkujad ära tunnevad.</span><span class="sxs-lookup"><span data-stu-id="d05e7-718">The identification of specific country or region, state, and county (municipality) codes requires specific formats that Dayforce and in-country/in-region providers can recognize.</span></span> <span data-ttu-id="d05e7-719">Kuigi linnade vorming on paindlik, peab iga linn olema seotud osariigiga.</span><span class="sxs-lookup"><span data-stu-id="d05e7-719">Although the format for cities is flexible, every city must be associated with a state.</span></span>

| <span data-ttu-id="d05e7-720">Talent</span><span class="sxs-lookup"><span data-stu-id="d05e7-720">Talent</span></span>              | <span data-ttu-id="d05e7-721">Dayforce</span><span class="sxs-lookup"><span data-stu-id="d05e7-721">Dayforce</span></span>              |
|---------------------|-----------------------|
| <span data-ttu-id="d05e7-722">Riik/regioon</span><span class="sxs-lookup"><span data-stu-id="d05e7-722">Country/Region</span></span>      | <span data-ttu-id="d05e7-723">Riigi kood</span><span class="sxs-lookup"><span data-stu-id="d05e7-723">Country Code</span></span>          |
| <span data-ttu-id="d05e7-724">Sihtnumber</span><span class="sxs-lookup"><span data-stu-id="d05e7-724">Zip/Postal Code</span></span>     | <span data-ttu-id="d05e7-725">Sihtnumber</span><span class="sxs-lookup"><span data-stu-id="d05e7-725">Postal Code</span></span>           |
| <span data-ttu-id="d05e7-726">Osariik</span><span class="sxs-lookup"><span data-stu-id="d05e7-726">State</span></span>               | <span data-ttu-id="d05e7-727">Osariigi kood</span><span class="sxs-lookup"><span data-stu-id="d05e7-727">State Code</span></span>            |
| <span data-ttu-id="d05e7-728">Linn</span><span class="sxs-lookup"><span data-stu-id="d05e7-728">City</span></span>                | <span data-ttu-id="d05e7-729">Linn</span><span class="sxs-lookup"><span data-stu-id="d05e7-729">City</span></span>                  |
| <span data-ttu-id="d05e7-730">Maakond</span><span class="sxs-lookup"><span data-stu-id="d05e7-730">County</span></span>              | <span data-ttu-id="d05e7-731">Maakond (haldusüksus)</span><span class="sxs-lookup"><span data-stu-id="d05e7-731">County (Municipality)</span></span> |
| <span data-ttu-id="d05e7-732">Tänav</span><span class="sxs-lookup"><span data-stu-id="d05e7-732">Street</span></span>              | <span data-ttu-id="d05e7-733">Aadressirida 1</span><span class="sxs-lookup"><span data-stu-id="d05e7-733">Address Line 1</span></span>        |
| <span data-ttu-id="d05e7-734">Majanumber</span><span class="sxs-lookup"><span data-stu-id="d05e7-734">Street Number</span></span>       | <span data-ttu-id="d05e7-735">Aadressirida 2</span><span class="sxs-lookup"><span data-stu-id="d05e7-735">Address Line 2</span></span>        |
| <span data-ttu-id="d05e7-736">Hoone tähis</span><span class="sxs-lookup"><span data-stu-id="d05e7-736">Building Complement</span></span> | <span data-ttu-id="d05e7-737">Aadressirida 5</span><span class="sxs-lookup"><span data-stu-id="d05e7-737">Address Line 5</span></span>        |

### <a name="passport-number"></a><span data-ttu-id="d05e7-738">Passi number</span><span class="sxs-lookup"><span data-stu-id="d05e7-738">Passport number</span></span>

<span data-ttu-id="d05e7-739">Töötajad saavad deklareerida passi teavet.</span><span class="sxs-lookup"><span data-stu-id="d05e7-739">Employees can declare passport information.</span></span> <span data-ttu-id="d05e7-740">See teave on identifitseerimistüüpi **Pass** ja integreeritakse Dayforce’i töövõtja Mehhiko-teabe osana.</span><span class="sxs-lookup"><span data-stu-id="d05e7-740">This information is of the **Passport** identification type and is integrated into Dayforce as part of an employee's Mexico-specific information.</span></span>

- <span data-ttu-id="d05e7-741">Identifitseerimistüüp = pass</span><span class="sxs-lookup"><span data-stu-id="d05e7-741">Identification Type = "Passport"</span></span>
- <span data-ttu-id="d05e7-742">Väljastamise kuupäev</span><span class="sxs-lookup"><span data-stu-id="d05e7-742">Issued Date</span></span>
- <span data-ttu-id="d05e7-743">Aegumiskuupäev</span><span class="sxs-lookup"><span data-stu-id="d05e7-743">Expiration Date</span></span>

<span data-ttu-id="d05e7-744">Töövõtjad saavad deklareerida mitu **Pass**-identifitseerimistüüpi ID-numbrit.</span><span class="sxs-lookup"><span data-stu-id="d05e7-744">Employees can declare multiple identification numbers of the **Passport** identification type.</span></span> <span data-ttu-id="d05e7-745">Dayforce’i integreeritakse siiski ainult praegune aktiivne passikirje.</span><span class="sxs-lookup"><span data-stu-id="d05e7-745">However, only the current active passport entry is integrated into Dayforce.</span></span> <span data-ttu-id="d05e7-746">Kui kõik passikirjed on aegunud, siis integreeritakse Dayforce’i pass, mis väljastati viimasena.</span><span class="sxs-lookup"><span data-stu-id="d05e7-746">If all passport entries are expired, the passport that was most recently issued is integrated into Dayforce.</span></span>
