---
title: Elektroonilise arvelduse lisandmooduli halduse komponendid
description: Sellest teemast leiate teavet komponentide kohta, mis on seotud elektroonilise arvelduse lisandmooduli haldusega.
author: gionoder
manager: AnnBe
ms.date: 01/28/2021
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
ms.openlocfilehash: 6f630ebb694217c3bd52378a649933a670c090f2
ms.sourcegitcommit: e88c96d1cb817a22db81856cadb563c095ab2671
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/02/2021
ms.locfileid: "5104370"
---
# <a name="electronic-invoicing-add-on-administration-components"></a><span data-ttu-id="15e6b-103">Elektroonilise arvelduse lisandmooduli halduse komponendid</span><span class="sxs-lookup"><span data-stu-id="15e6b-103">Electronic invoicing add-on administration components</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

<span data-ttu-id="15e6b-104">Sellest teemast leiate teavet komponentide kohta, mis on seotud elektroonilise arvelduse lisandmooduli haldusega.</span><span class="sxs-lookup"><span data-stu-id="15e6b-104">This topic provides information about the components that are related to administration of the Electronic invoicing add-on.</span></span> <span data-ttu-id="15e6b-105">Samuti kirjeldab see, kuidas elektroonilise arvelduse lisandmooduli teenust konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="15e6b-105">It also provides information about how to configure the Electronic invoicing add-on service.</span></span>

## <a name="azure"></a><span data-ttu-id="15e6b-106">Azure</span><span class="sxs-lookup"><span data-stu-id="15e6b-106">Azure</span></span>

<span data-ttu-id="15e6b-107">Kasutage teenust Microsoft Azure võtmehoidla ja salvestuskonto saladuste loomiseks.</span><span class="sxs-lookup"><span data-stu-id="15e6b-107">Use Microsoft Azure to create the secrets for the key vault and storage account.</span></span> <span data-ttu-id="15e6b-108">Seejärel kasutage saladusi elektroonilise arvelduse lisandmooduli konfigureerimisel.</span><span class="sxs-lookup"><span data-stu-id="15e6b-108">Then use the secrets in the configuration of the Electronic invoicing add-on.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="15e6b-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="15e6b-109">Lifecycle Services</span></span>

<span data-ttu-id="15e6b-110">Kasutage LCS-i juurutusprojekti mikroteenuste jaoks lisandmooduli lubamiseks Microsoft Dynamicsi teenust Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="15e6b-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the add-on for the microservices for your LCS deployment project.</span></span>

<span data-ttu-id="15e6b-111">Valige LCS-is paan **Eelvaate funktsiooni haldamine** ja lülitage funktsioon **E-arvelduse teenus** sisse.</span><span class="sxs-lookup"><span data-stu-id="15e6b-111">In LCS, select the **Preview feature management** tile, and then turn on the **e-Invoicing Service** feature.</span></span>

## <a name="regulatory-configuration-services"></a><span data-ttu-id="15e6b-112">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="15e6b-112">Regulatory Configuration Services</span></span>

<span data-ttu-id="15e6b-113">Dynamics 365 Regulatory Configuration Services (RCS) on elektroonilise arvelduse lisandmooduli konfigureerimiseks kasutatav liides.</span><span class="sxs-lookup"><span data-stu-id="15e6b-113">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure the Electronic invoicing add-on.</span></span> <span data-ttu-id="15e6b-114">Selliseid ressursse nagu keskkonnad ja elektroonilise arvelduse funktsioonid luuakse, hallatakse ja majutatakse RCS-is.</span><span class="sxs-lookup"><span data-stu-id="15e6b-114">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="15e6b-115">Kui ressursid on valmis, avaldatakse need elektroonilise arvelduse lisandmooduli teenuses.</span><span class="sxs-lookup"><span data-stu-id="15e6b-115">When the resources are ready, they are published to the Electronic invoicing add-on service.</span></span>

<span data-ttu-id="15e6b-116">Lisateavet RCS-i kohta vt teemast [Regulatory Configuration Services (RCS) – globaliseerimisfunktsioonid](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="15e6b-116">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-the-electronic-invoicing-add-on"></a><span data-ttu-id="15e6b-117">Elektroonilise arvelduse lisandmooduliga integreerimine</span><span class="sxs-lookup"><span data-stu-id="15e6b-117">Integration with the Electronic invoicing add-on</span></span>

<span data-ttu-id="15e6b-118">Enne kui saate elektrooniliste arvete konfigureerimiseks RCS-i kasutada, peate konfigureerima RCS-i, et lubada andmevahetus elektroonilise arvelduse lisandmooduliga.</span><span class="sxs-lookup"><span data-stu-id="15e6b-118">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with the Electronic invoicing add-on.</span></span> <span data-ttu-id="15e6b-119">See konfiguratsioon lõpetatakse lehe **Elektroonilise aruandluse parameetrid** vahekaardil **Elektroonilise aruandluse lisandmoodul**.</span><span class="sxs-lookup"><span data-stu-id="15e6b-119">You complete this configuration on the **Electronic invoicing add-on** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="15e6b-120">Teenuse lõpp-punkt</span><span class="sxs-lookup"><span data-stu-id="15e6b-120">Service endpoint</span></span>

<span data-ttu-id="15e6b-121">Elektroonilise arvelduse lisandmooduli lõpp-punkt võib olenevalt Azure'i andmekeskuse geograafilisest piirkonnast erineda.</span><span class="sxs-lookup"><span data-stu-id="15e6b-121">The URL of the Electronic invoicing add-on endpoint can vary according to the Azure datacenter geography.</span></span> <span data-ttu-id="15e6b-122">Järgmises tabelis on toodud saadavus piirkonniti.</span><span class="sxs-lookup"><span data-stu-id="15e6b-122">The following table lists the availability per region:</span></span>

| <span data-ttu-id="15e6b-123">Azure'i andmekeskuse geograafiline piirkond</span><span class="sxs-lookup"><span data-stu-id="15e6b-123">Azure datacenter geography</span></span> | <span data-ttu-id="15e6b-124">Teenuse lõpp-punkti URL</span><span class="sxs-lookup"><span data-stu-id="15e6b-124">Service endpoint URL</span></span>                                                       |
|----------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="15e6b-125">Ida-USA</span><span class="sxs-lookup"><span data-stu-id="15e6b-125">East US</span></span>                    | `https://electronicinvoicing.eus-il301.gateway.prod.island.powerapps.com/` |
| <span data-ttu-id="15e6b-126">Lääne-USA</span><span class="sxs-lookup"><span data-stu-id="15e6b-126">West US</span></span>                    | `https://electronicinvoicing.wus-il301.gateway.prod.island.powerapps.com/` |
| <span data-ttu-id="15e6b-127">Põhja-EL</span><span class="sxs-lookup"><span data-stu-id="15e6b-127">North EU</span></span>                   | `https://electronicinvoicing.neu-il301.gateway.prod.island.powerapps.com/` |
| <span data-ttu-id="15e6b-128">Lääne-EL</span><span class="sxs-lookup"><span data-stu-id="15e6b-128">West EU</span></span>                    | `https://electronicinvoicing.weu-il301.gateway.prod.island.powerapps.com/` |

#### <a name="application-id"></a><span data-ttu-id="15e6b-129">Rakenduse ID</span><span class="sxs-lookup"><span data-stu-id="15e6b-129">Application ID</span></span>

<span data-ttu-id="15e6b-130">Rakenduse ID on elektroonilise arvelduse lisandmooduli rakenduse ID.</span><span class="sxs-lookup"><span data-stu-id="15e6b-130">The application ID is the ID of the Electronic invoicing add-on application.</span></span> <span data-ttu-id="15e6b-131">Selles näites on see väärtus fikseeritud: **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span><span class="sxs-lookup"><span data-stu-id="15e6b-131">In this case, the value is fixed: **0cdb527f-a8d1-4bf8-9436-b352c68682b2**.</span></span>

#### <a name="lcs-environment-id"></a><span data-ttu-id="15e6b-132">LCS-i keskkonna ID</span><span class="sxs-lookup"><span data-stu-id="15e6b-132">LCS environment ID</span></span>

<span data-ttu-id="15e6b-133">LCS-i keskkonna ID on teie organisatsiooni LCS-i tellimuse ID.</span><span class="sxs-lookup"><span data-stu-id="15e6b-133">The LCS environment ID is the ID of your organization's LCS subscription.</span></span>

### <a name="service-environments"></a><span data-ttu-id="15e6b-134">Teenusekeskkonnad</span><span class="sxs-lookup"><span data-stu-id="15e6b-134">Service environments</span></span>

<span data-ttu-id="15e6b-135">Teenusekeskkonnad on loogilised sektsioonid, mis luuakse elektroonilise arvelduse lisandmoodulis elektroonilise arvelduse funktsioonide käivitamise toetamiseks.</span><span class="sxs-lookup"><span data-stu-id="15e6b-135">Service environments are logical partitions that are created to support execution of the electronic invoicing features in the Electronic invoicing add-on.</span></span> <span data-ttu-id="15e6b-136">Turvasaladused ja digitaalserdid ning juhtimine (st juurdepääsuload) peavad olema konfigureeritud teenusekeskkonna tasemel.</span><span class="sxs-lookup"><span data-stu-id="15e6b-136">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="15e6b-137">Kliendid saavad luua nii palju teenusekeskkondi, kui nad soovivad.</span><span class="sxs-lookup"><span data-stu-id="15e6b-137">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="15e6b-138">Kõik teenusekeskkonnad, mille klient loob, on üksteisest sõltumatud.</span><span class="sxs-lookup"><span data-stu-id="15e6b-138">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="15e6b-139">Teenusekeskkonnad saab luua ja neid saab hooldada RCS-is.</span><span class="sxs-lookup"><span data-stu-id="15e6b-139">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="15e6b-140">Kui teenusekeskkonnad on valmis, tuleb need elektroonilise arvelduse lisandmooduli teenuses avaldada.</span><span class="sxs-lookup"><span data-stu-id="15e6b-140">When the service environments are ready, they must be published to the Electronic invoicing add-on.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="15e6b-141">Teenusekeskkonna olek</span><span class="sxs-lookup"><span data-stu-id="15e6b-141">Service environment status</span></span>

<span data-ttu-id="15e6b-142">Teenusekeskkondi saab hallata oleku kaudu.</span><span class="sxs-lookup"><span data-stu-id="15e6b-142">Service environments can be managed through status.</span></span> <span data-ttu-id="15e6b-143">Saadaval on järgmised valikud.</span><span class="sxs-lookup"><span data-stu-id="15e6b-143">The possible options are:</span></span>

- <span data-ttu-id="15e6b-144">**Pole avaldatud** – keskkond on loodud, kuid seda pole veel avaldatud.</span><span class="sxs-lookup"><span data-stu-id="15e6b-144">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="15e6b-145">**Avaldatud** – keskkond on elektroonilise arvelduse lisandmoodulis avaldatud.</span><span class="sxs-lookup"><span data-stu-id="15e6b-145">**Published** – The environment has been published to the Electronic invoicing add-on.</span></span>
- <span data-ttu-id="15e6b-146">**Muudetud** – avaldatud keskkonna atribuute on muudetud, kuid muudatusi pole veel avaldatud.</span><span class="sxs-lookup"><span data-stu-id="15e6b-146">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="15e6b-147">Klientide saladused</span><span class="sxs-lookup"><span data-stu-id="15e6b-147">Customer secrets</span></span>

<span data-ttu-id="15e6b-148">Elektroonilise arvelduse lisandmooduli teenus vastutab kõigi teie äriandmete talletamise eest Azure'i ressurssides, mis kuuluvad teie ettevõttele.</span><span class="sxs-lookup"><span data-stu-id="15e6b-148">The Electronic invoicing add-on service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="15e6b-149">Et teenus töötaks korrektselt ning kõikidele äriandmetele, mida elektroonilise arvelduse lisandmoodul vajab ja kasutab, pääseks juurde vaid see lisandmoodul, peate looma kaks peamist Azure'i ressurssi.</span><span class="sxs-lookup"><span data-stu-id="15e6b-149">To ensure that the service works correctly, and that all the business data that is required for and generated by the Electronic invoicing add-on is accessed only by the add-on, you must create two main Azure resources:</span></span>

- <span data-ttu-id="15e6b-150">Azure'i salvestuskonto (bloobimälu) elektrooniliste arvete talletamiseks</span><span class="sxs-lookup"><span data-stu-id="15e6b-150">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="15e6b-151">Azure'i võtmehoidla sertide ja salvestuskonto ühtse ressursi-indikaatori (URI) talletamiseks</span><span class="sxs-lookup"><span data-stu-id="15e6b-151">An Azure key vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>

> [!NOTE]
> <span data-ttu-id="15e6b-152">Elektroonilise arvelduse lisandmooduli jaoks tuleb määrata spetsiaalne võtmehoidla ja kliendi salvestuskonto.</span><span class="sxs-lookup"><span data-stu-id="15e6b-152">A dedicated key vault and customer storage account must be allocated specifically for use with the Electronic invoicing add-on.</span></span>

<span data-ttu-id="15e6b-153">Lisateavet vt teemast [Azure'i salvestuskonto ja võtmehoidla loomine](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="15e6b-153">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

#### <a name="users"></a><span data-ttu-id="15e6b-154">Kasutajad</span><span class="sxs-lookup"><span data-stu-id="15e6b-154">Users</span></span>

<span data-ttu-id="15e6b-155">Iga teenusekeskkond peab loetlema kasutajad, kes saavad elektroonilise arvelduse lisandmoodulis teenuste Dynamics 365 Finance ja Dynamics 365 Supply Chain Management kaudu ühenduse luua.</span><span class="sxs-lookup"><span data-stu-id="15e6b-155">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in the Electronic invoicing add-on.</span></span>

#### <a name="publication"></a><span data-ttu-id="15e6b-156">Avaldamine</span><span class="sxs-lookup"><span data-stu-id="15e6b-156">Publication</span></span>

<span data-ttu-id="15e6b-157">Enne teenusekeskkondade kasutamist tuleb need elektroonilise arvelduse lisandmoodulis avaldada.</span><span class="sxs-lookup"><span data-stu-id="15e6b-157">Service environments must be published to the Electronic invoicing add-on before they can be used.</span></span> <span data-ttu-id="15e6b-158">Teenuste Finance ja Supply Chain Management kaudu pääseb juurde ainult avaldatud keskkondadele.</span><span class="sxs-lookup"><span data-stu-id="15e6b-158">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="15e6b-159">Peale selle tuleb teenusekeskkond avaldada, enne kui selle atribuutide värskendused elektroonilise arvelduse teenuses jõustuvad.</span><span class="sxs-lookup"><span data-stu-id="15e6b-159">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="15e6b-160">Ühendatud avaldused</span><span class="sxs-lookup"><span data-stu-id="15e6b-160">Connected applications</span></span>

<span data-ttu-id="15e6b-161">Ühendatud rakendused on teenuste Finance and Supply Chain Management eksemplarid, millega võite soovida RCS-i kaudu ühendust saada.</span><span class="sxs-lookup"><span data-stu-id="15e6b-161">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="15e6b-162">Peale rakenduse URL-i ja selle rentniku hõlmab ühendatud rakendus mandaate, mis võimaldavad RCS-il keskkonnaga ühenduse luua.</span><span class="sxs-lookup"><span data-stu-id="15e6b-162">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="15e6b-163">Ühendatud rakenduste abil saate konfigureerida osa elektroonilise arvelduse funktsioonist teenustes Finance ja Supply Chain Management, et kogu elektroonilise arvelduse funktsioon tööle saada.</span><span class="sxs-lookup"><span data-stu-id="15e6b-163">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="15e6b-164">Finance ja Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="15e6b-164">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing-add-on"></a><span data-ttu-id="15e6b-165">Elektroonilise arvelduse lisandmooduliga integreerimine</span><span class="sxs-lookup"><span data-stu-id="15e6b-165">Integration with Electronic invoicing add-on</span></span>

<span data-ttu-id="15e6b-166">Enne kui saate teenuseid Finance ja Supply Chain Management elektroonilise arvelduse lisandmooduli kaudu elektrooniliste arvete väljastamiseks kasutada, tuleb lisandmoodul konfigureerida nii, et see lubaks teenusega suhtlemist.</span><span class="sxs-lookup"><span data-stu-id="15e6b-166">Before you can use Finance and Supply Chain Management to issue electronic invoices through the Electronic invoicing add-on, the add-on must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-add-on-integration-feature"></a><span data-ttu-id="15e6b-167">Elektroonilise arvelduse lisandmooduli integreerimisfunktsioon</span><span class="sxs-lookup"><span data-stu-id="15e6b-167">Electronic invoicing add-on integration feature</span></span>

<span data-ttu-id="15e6b-168">Teenuste Finance ja Supply Chain Management ning elektroonilise arvelduse lisandmooduli vahelise suhtluse lubamiseks peate tööruumis **Funktsioonihaldus** funktsiooni **Elektroonilise arvelduse lisandmooduli integreerimine** sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="15e6b-168">To enable communication between Finance and Supply Chain Management and the Electronic invoicing add-on, you must turn on the **Electronic Invoicing add-on integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="15e6b-169">Teenuse lõpp-punkt</span><span class="sxs-lookup"><span data-stu-id="15e6b-169">Service endpoint</span></span>

<span data-ttu-id="15e6b-170">Teenuse lõpp-punkt on elektroonilise arvelduse lisandmooduli asukoha URL.</span><span class="sxs-lookup"><span data-stu-id="15e6b-170">The service endpoint is the URL where the Electronic invoicing add-on is located.</span></span> <span data-ttu-id="15e6b-171">Enne kui saab väljastada elektroonilisi arveid, tuleb teenuse lõpp-punkt konfigureerida teenustes Finance ja Supply Chain Management nii, et see lubaks teenusega suhtlemist.</span><span class="sxs-lookup"><span data-stu-id="15e6b-171">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="15e6b-172">Teenuse lõpp-punkti konfigureerimiseks avage **Organisatsiooni haldus \> Seadistus \> Elektroonilise dokumendi parameetrid** ja seejärel sisestage vahekaardi **Edastusteenused** väljale **Elektroonilise arvelduse lisandmooduli URL** URL, nagu on kirjeldatud jaotises **Teenuse lõpp-punkt** näidatud tabelis.</span><span class="sxs-lookup"><span data-stu-id="15e6b-172">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing add-on URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="15e6b-173">Keskkonnad</span><span class="sxs-lookup"><span data-stu-id="15e6b-173">Environments</span></span>

<span data-ttu-id="15e6b-174">Teenuses Finance ja Supply Chain Management sisestatud keskkonna nimi viitab selle keskkonna nimele, mis luuakse RCS-is ja avaldatakse elektroonilise arvelduse lisandmoodulis.</span><span class="sxs-lookup"><span data-stu-id="15e6b-174">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to the Electronic invoicing add-on.</span></span>

<span data-ttu-id="15e6b-175">Keskkond tuleb konfigureerida lehe **Elektroonilise dokumendi parameetrid** vahekaardil **Edastusteenused**, nii et kõik elektrooniliste arvete väljastamistaotlused hõlmavad keskkonda, kus elektroonilise arvelduse lisandmoodul saab määrata, milline elektroonilise arvelduse funktsioon peab taotlust töötlema.</span><span class="sxs-lookup"><span data-stu-id="15e6b-175">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where the Electronic invoicing add-on can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="15e6b-176">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="15e6b-176">Additional resources</span></span>

- [<span data-ttu-id="15e6b-177">Elektrooniliste arvete konfigureerimine RCS-is</span><span class="sxs-lookup"><span data-stu-id="15e6b-177">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="15e6b-178">Elektroonilise arvete väljastamine teenustes Finance ja Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="15e6b-178">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)
