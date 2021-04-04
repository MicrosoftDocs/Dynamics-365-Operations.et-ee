---
title: Elektroonilise arvelduse lisandmooduli halduse komponendid
description: Sellest teemast leiate teavet komponentide kohta, mis on seotud elektroonilise arvelduse lisandmooduli haldusega.
author: gionoder
manager: AnnBe
ms.date: 03/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: 70ef47dd45200a14c9d780f3c280c554d0e52ac3
ms.sourcegitcommit: 543772ee97efe215cf6f2ec6e092cc1568919f20
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/13/2021
ms.locfileid: "5592570"
---
# <a name="electronic-invoicing-add-on-administration-components"></a><span data-ttu-id="6c711-103">Elektroonilise arvelduse lisandmooduli halduse komponendid</span><span class="sxs-lookup"><span data-stu-id="6c711-103">Electronic invoicing add-on administration components</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="6c711-104">Sellest teemast leiate teavet komponentide kohta, mis on seotud elektroonilise arvelduse lisandmooduli haldusega.</span><span class="sxs-lookup"><span data-stu-id="6c711-104">This topic provides information about the components that are related to administration of the Electronic invoicing add-on.</span></span> <span data-ttu-id="6c711-105">Samuti kirjeldab see, kuidas elektroonilise arvelduse lisandmooduli teenust konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="6c711-105">It also provides information about how to configure the Electronic invoicing add-on service.</span></span>

## <a name="azure"></a><span data-ttu-id="6c711-106">Azure</span><span class="sxs-lookup"><span data-stu-id="6c711-106">Azure</span></span>

<span data-ttu-id="6c711-107">Kasutage teenust Microsoft Azure võtmehoidla ja salvestuskonto saladuste loomiseks.</span><span class="sxs-lookup"><span data-stu-id="6c711-107">Use Microsoft Azure to create the secrets for the key vault and storage account.</span></span> <span data-ttu-id="6c711-108">Seejärel kasutage saladusi elektroonilise arvelduse lisandmooduli konfigureerimisel.</span><span class="sxs-lookup"><span data-stu-id="6c711-108">Then use the secrets in the configuration of the Electronic invoicing add-on.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="6c711-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="6c711-109">Lifecycle Services</span></span>

<span data-ttu-id="6c711-110">Kasutage LCS-i juurutusprojekti mikroteenuste jaoks lisandmooduli lubamiseks Microsoft Dynamicsi teenust Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="6c711-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the add-on for the microservices for your LCS deployment project.</span></span>

> [!NOTE]
> <span data-ttu-id="6c711-111">Mikroteenuse lisandmooduli LCS-i install nõuab vähemalt 2. taseme virtuaalmasinat.</span><span class="sxs-lookup"><span data-stu-id="6c711-111">The installation of the microservice add-on in LCS requires at least a Tier 2 virtual machine.</span></span> <span data-ttu-id="6c711-112">Lisateavet keskkondade kohta vaadake teemast [Keskkonna planeerimine](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="6c711-112">For more information about environment planning, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
 

## <a name="regulatory-configuration-services"></a><span data-ttu-id="6c711-113">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="6c711-113">Regulatory Configuration Services</span></span>

<span data-ttu-id="6c711-114">Dynamics 365 Regulatory Configuration Services (RCS) on elektroonilise arvelduse lisandmooduli konfigureerimiseks kasutatav liides.</span><span class="sxs-lookup"><span data-stu-id="6c711-114">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure the Electronic invoicing add-on.</span></span> <span data-ttu-id="6c711-115">Selliseid ressursse nagu keskkonnad ja elektroonilise arvelduse funktsioonid luuakse, hallatakse ja majutatakse RCS-is.</span><span class="sxs-lookup"><span data-stu-id="6c711-115">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="6c711-116">Kui ressursid on valmis, avaldatakse need elektroonilise arvelduse lisandmooduli teenuses.</span><span class="sxs-lookup"><span data-stu-id="6c711-116">When the resources are ready, they are published to the Electronic invoicing add-on service.</span></span>

<span data-ttu-id="6c711-117">RCS-i registreerimiseks vaata [Regulatory services](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="6c711-117">For RCS sign-up, see [Regulatory services](https://marketing.configure.global.dynamics.com/).</span></span>

<span data-ttu-id="6c711-118">Lisateavet RCS-i kohta vt teemast [Regulatory Configuration Services (RCS) – globaliseerimisfunktsioonid](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="6c711-118">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="6c711-119">Elektroonilise arvelduse lisandmooduliga integreerimine</span><span class="sxs-lookup"><span data-stu-id="6c711-119">Integration with the Electronic invoicing add-on</span></span>

<span data-ttu-id="6c711-120">Enne kui saate elektrooniliste arvete konfigureerimiseks RCS-i kasutada, peate konfigureerima RCS-i, et lubada andmevahetus elektroonilise arvelduse lisandmooduliga.</span><span class="sxs-lookup"><span data-stu-id="6c711-120">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with the Electronic invoicing add-on.</span></span> <span data-ttu-id="6c711-121">See konfiguratsioon lõpetatakse lehe **Elektroonilise aruandluse parameetrid** vahekaardil **Elektroonilise aruandluse lisandmoodul**.</span><span class="sxs-lookup"><span data-stu-id="6c711-121">You complete this configuration on the **Electronic invoicing add-on** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="6c711-122">Teenuse lõpp-punkt</span><span class="sxs-lookup"><span data-stu-id="6c711-122">Service endpoint</span></span>

<span data-ttu-id="6c711-123">Elektroonilise arvelduse lisandmoodul juurutatakse järgmistes Azure'i geograafilistes piirkondades.</span><span class="sxs-lookup"><span data-stu-id="6c711-123">The Electronic invoicing add-on is available in several Azure datacenter geographies.</span></span> <span data-ttu-id="6c711-124">Järgmises tabelis on toodud saadavus piirkonniti.</span><span class="sxs-lookup"><span data-stu-id="6c711-124">The following table lists the availability per region.</span></span>

| <span data-ttu-id="6c711-125">Azure'i andmekeskuse geograafiline piirkond</span><span class="sxs-lookup"><span data-stu-id="6c711-125">Azure datacenter geography</span></span> |
|----------------------------|
| <span data-ttu-id="6c711-126">Ida-USA</span><span class="sxs-lookup"><span data-stu-id="6c711-126">East US</span></span>                    |
| <span data-ttu-id="6c711-127">Lääne-USA</span><span class="sxs-lookup"><span data-stu-id="6c711-127">West US</span></span>                    |
| <span data-ttu-id="6c711-128">Põhja-EL</span><span class="sxs-lookup"><span data-stu-id="6c711-128">North EU</span></span>                   |
| <span data-ttu-id="6c711-129">Lääne-EL</span><span class="sxs-lookup"><span data-stu-id="6c711-129">West EU</span></span>                    |

### <a name="service-environments"></a><span data-ttu-id="6c711-130">Teenusekeskkonnad</span><span class="sxs-lookup"><span data-stu-id="6c711-130">Service environments</span></span>

<span data-ttu-id="6c711-131">Teenusekeskkonnad on loogilised sektsioonid, mis luuakse elektroonilise arvelduse lisandmoodulis elektroonilise arvelduse funktsioonide käivitamise toetamiseks.</span><span class="sxs-lookup"><span data-stu-id="6c711-131">Service environments are logical partitions that are created to support execution of the electronic invoicing features in the Electronic invoicing add-on.</span></span> <span data-ttu-id="6c711-132">Turvasaladused ja digitaalserdid ning juhtimine (st juurdepääsuload) peavad olema konfigureeritud teenusekeskkonna tasemel.</span><span class="sxs-lookup"><span data-stu-id="6c711-132">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="6c711-133">Kliendid saavad luua nii palju teenusekeskkondi, kui nad soovivad.</span><span class="sxs-lookup"><span data-stu-id="6c711-133">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="6c711-134">Kõik teenusekeskkonnad, mille klient loob, on üksteisest sõltumatud.</span><span class="sxs-lookup"><span data-stu-id="6c711-134">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="6c711-135">Teenusekeskkonnad saab luua ja neid saab hooldada RCS-is.</span><span class="sxs-lookup"><span data-stu-id="6c711-135">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="6c711-136">Kui teenusekeskkonnad on valmis, tuleb need elektroonilise arvelduse lisandmooduli teenuses avaldada.</span><span class="sxs-lookup"><span data-stu-id="6c711-136">When the service environments are ready, they must be published to the Electronic invoicing add-on.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="6c711-137">Teenusekeskkonna olek</span><span class="sxs-lookup"><span data-stu-id="6c711-137">Service environment status</span></span>

<span data-ttu-id="6c711-138">Teenusekeskkondi saab hallata oleku kaudu.</span><span class="sxs-lookup"><span data-stu-id="6c711-138">Service environments can be managed through status.</span></span> <span data-ttu-id="6c711-139">Saadaval on järgmised valikud.</span><span class="sxs-lookup"><span data-stu-id="6c711-139">The possible options are:</span></span>

- <span data-ttu-id="6c711-140">**Pole avaldatud** – keskkond on loodud, kuid seda pole veel avaldatud.</span><span class="sxs-lookup"><span data-stu-id="6c711-140">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="6c711-141">**Avaldatud** – keskkond on elektroonilise arvelduse lisandmoodulis avaldatud.</span><span class="sxs-lookup"><span data-stu-id="6c711-141">**Published** – The environment has been published to the Electronic invoicing add-on.</span></span>
- <span data-ttu-id="6c711-142">**Muudetud** – avaldatud keskkonna atribuute on muudetud, kuid muudatusi pole veel avaldatud.</span><span class="sxs-lookup"><span data-stu-id="6c711-142">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="6c711-143">Klientide saladused</span><span class="sxs-lookup"><span data-stu-id="6c711-143">Customer secrets</span></span>

<span data-ttu-id="6c711-144">Elektroonilise arvelduse lisandmooduli teenus vastutab kõigi teie äriandmete talletamise eest Azure'i ressurssides, mis kuuluvad teie ettevõttele.</span><span class="sxs-lookup"><span data-stu-id="6c711-144">The Electronic invoicing add-on service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="6c711-145">Et teenus töötaks korrektselt ning kõikidele äriandmetele, mida elektroonilise arvelduse lisandmoodul vajab ja kasutab, pääseks juurde vaid see lisandmoodul, peate looma kaks peamist Azure'i ressurssi.</span><span class="sxs-lookup"><span data-stu-id="6c711-145">To ensure that the service works correctly, and that all the business data that is required for and generated by the Electronic invoicing add-on is accessed only by the add-on, you must create two main Azure resources:</span></span>

- <span data-ttu-id="6c711-146">Azure'i salvestuskonto (bloobimälu) elektrooniliste arvete talletamiseks</span><span class="sxs-lookup"><span data-stu-id="6c711-146">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="6c711-147">Azure'i võtmehoidla sertide ja salvestuskonto ühtse ressursi-indikaatori (URI) talletamiseks</span><span class="sxs-lookup"><span data-stu-id="6c711-147">An Azure key vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>

> [!NOTE]
> <span data-ttu-id="6c711-148">Elektroonilise arvelduse lisandmooduli jaoks tuleb määrata spetsiaalne võtmehoidla ja kliendi salvestuskonto.</span><span class="sxs-lookup"><span data-stu-id="6c711-148">A dedicated key vault and customer storage account must be allocated specifically for use with the Electronic invoicing add-on.</span></span>

<span data-ttu-id="6c711-149">Lisateavet vt teemast [Azure'i salvestuskonto ja võtmehoidla loomine](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="6c711-149">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

#### <a name="users"></a><span data-ttu-id="6c711-150">Kasutajad</span><span class="sxs-lookup"><span data-stu-id="6c711-150">Users</span></span>

<span data-ttu-id="6c711-151">Iga teenusekeskkond peab loetlema kasutajad, kes saavad elektroonilise arvelduse lisandmoodulis teenuste Dynamics 365 Finance ja Dynamics 365 Supply Chain Management kaudu ühenduse luua.</span><span class="sxs-lookup"><span data-stu-id="6c711-151">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in the Electronic invoicing add-on.</span></span>

#### <a name="publication"></a><span data-ttu-id="6c711-152">Avaldamine</span><span class="sxs-lookup"><span data-stu-id="6c711-152">Publication</span></span>

<span data-ttu-id="6c711-153">Enne teenusekeskkondade kasutamist tuleb need elektroonilise arvelduse lisandmoodulis avaldada.</span><span class="sxs-lookup"><span data-stu-id="6c711-153">Service environments must be published to the Electronic invoicing add-on before they can be used.</span></span> <span data-ttu-id="6c711-154">Teenuste Finance ja Supply Chain Management kaudu pääseb juurde ainult avaldatud keskkondadele.</span><span class="sxs-lookup"><span data-stu-id="6c711-154">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="6c711-155">Peale selle tuleb teenusekeskkond avaldada, enne kui selle atribuutide värskendused elektroonilise arvelduse teenuses jõustuvad.</span><span class="sxs-lookup"><span data-stu-id="6c711-155">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="6c711-156">Ühendatud avaldused</span><span class="sxs-lookup"><span data-stu-id="6c711-156">Connected applications</span></span>

<span data-ttu-id="6c711-157">Ühendatud rakendused on teenuste Finance and Supply Chain Management eksemplarid, millega võite soovida RCS-i kaudu ühendust saada.</span><span class="sxs-lookup"><span data-stu-id="6c711-157">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="6c711-158">Peale rakenduse URL-i ja selle rentniku hõlmab ühendatud rakendus mandaate, mis võimaldavad RCS-il keskkonnaga ühenduse luua.</span><span class="sxs-lookup"><span data-stu-id="6c711-158">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="6c711-159">Ühendatud rakenduste abil saate konfigureerida osa elektroonilise arvelduse funktsioonist teenustes Finance ja Supply Chain Management, et kogu elektroonilise arvelduse funktsioon tööle saada.</span><span class="sxs-lookup"><span data-stu-id="6c711-159">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="6c711-160">Finance ja Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="6c711-160">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing-add-on"></a><span data-ttu-id="6c711-161">Elektroonilise arvelduse lisandmooduliga integreerimine</span><span class="sxs-lookup"><span data-stu-id="6c711-161">Integration with Electronic invoicing add-on</span></span>

<span data-ttu-id="6c711-162">Enne kui saate teenuseid Finance ja Supply Chain Management elektroonilise arvelduse lisandmooduli kaudu elektrooniliste arvete väljastamiseks kasutada, tuleb lisandmoodul konfigureerida nii, et see lubaks teenusega suhtlemist.</span><span class="sxs-lookup"><span data-stu-id="6c711-162">Before you can use Finance and Supply Chain Management to issue electronic invoices through the Electronic invoicing add-on, the add-on must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="6c711-163">Elektroonilise arvelduse lisandmooduli integreerimisfunktsioon</span><span class="sxs-lookup"><span data-stu-id="6c711-163">Electronic invoicing add-on integration feature</span></span>

<span data-ttu-id="6c711-164">Teenuste Finance ja Supply Chain Management ning elektroonilise arvelduse lisandmooduli vahelise suhtluse lubamiseks peate tööruumis **Funktsioonihaldus** funktsiooni **Elektroonilise arvelduse lisandmooduli integreerimine** sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="6c711-164">To enable communication between Finance and Supply Chain Management and the Electronic invoicing add-on, you must turn on the **Electronic Invoicing add-on integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="6c711-165">Teenuse lõpp-punkt</span><span class="sxs-lookup"><span data-stu-id="6c711-165">Service endpoint</span></span>

<span data-ttu-id="6c711-166">Teenuse lõpp-punkt on elektroonilise arvelduse lisandmooduli asukoha URL.</span><span class="sxs-lookup"><span data-stu-id="6c711-166">The service endpoint is the URL where the Electronic invoicing add-on is located.</span></span> <span data-ttu-id="6c711-167">Enne kui saab väljastada elektroonilisi arveid, tuleb teenuse lõpp-punkt konfigureerida teenustes Finance ja Supply Chain Management nii, et see lubaks teenusega suhtlemist.</span><span class="sxs-lookup"><span data-stu-id="6c711-167">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="6c711-168">Teenuse lõpp-punkti konfigureerimiseks avage **Organisatsiooni haldus \> Seadistus \> Elektroonilise dokumendi parameetrid** ja seejärel sisestage vahekaardi **Edastusteenused** väljale **Elektroonilise arvelduse lisandmooduli URL** URL, nagu on kirjeldatud jaotises **Teenuse lõpp-punkt** näidatud tabelis.</span><span class="sxs-lookup"><span data-stu-id="6c711-168">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing add-on URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="6c711-169">Keskkonnad</span><span class="sxs-lookup"><span data-stu-id="6c711-169">Environments</span></span>

<span data-ttu-id="6c711-170">Teenuses Finance ja Supply Chain Management sisestatud keskkonna nimi viitab selle keskkonna nimele, mis luuakse RCS-is ja avaldatakse elektroonilise arvelduse lisandmoodulis.</span><span class="sxs-lookup"><span data-stu-id="6c711-170">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to the Electronic invoicing add-on.</span></span>

<span data-ttu-id="6c711-171">Keskkond tuleb konfigureerida lehe **Elektroonilise dokumendi parameetrid** vahekaardil **Edastusteenused**, nii et kõik elektrooniliste arvete väljastamistaotlused hõlmavad keskkonda, kus elektroonilise arvelduse lisandmoodul saab määrata, milline elektroonilise arvelduse funktsioon peab taotlust töötlema.</span><span class="sxs-lookup"><span data-stu-id="6c711-171">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where the Electronic invoicing add-on can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6c711-172">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="6c711-172">Additional resources</span></span>

- [<span data-ttu-id="6c711-173">Elektrooniliste arvete konfigureerimine RCS-is</span><span class="sxs-lookup"><span data-stu-id="6c711-173">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="6c711-174">Elektroonilise arvete väljastamine teenustes Finance ja Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="6c711-174">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
