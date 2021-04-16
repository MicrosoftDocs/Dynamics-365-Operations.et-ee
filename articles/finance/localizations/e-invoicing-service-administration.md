---
title: Elektroonilise arvelduse administratsioonikomponendid
description: Sellest teemast leiate teavet komponentide kohta, mis on seotud elektroonilise arvelduse administratsiooniga.
author: gionoder
ms.date: 03/29/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 2e859875e124796e49000cd5ea94cfb75ecd768a
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/01/2021
ms.locfileid: "5840024"
---
# <a name="electronic-invoicing-administration-components"></a><span data-ttu-id="0d1ce-103">Elektroonilise arvelduse administratsioonikomponendid</span><span class="sxs-lookup"><span data-stu-id="0d1ce-103">Electronic invoicing administration components</span></span>

[!include [banner](../includes/banner.md)]


<span data-ttu-id="0d1ce-104">Sellest teemast leiate teavet komponentide kohta, mis on seotud elektroonilise arvelduse administratsiooniga.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-104">This topic provides information about the components that are related to administration of Electronic invoicing.</span></span> <span data-ttu-id="0d1ce-105">Samuti pakub see teavet selle kohta, kuidas elektroonilise arvelduse teenust konfigureerida.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-105">It also provides information about how to configure the Electronic invoicing service.</span></span>

## <a name="azure"></a><span data-ttu-id="0d1ce-106">Azure</span><span class="sxs-lookup"><span data-stu-id="0d1ce-106">Azure</span></span>

<span data-ttu-id="0d1ce-107">Kasutage teenust Microsoft Azure võtmehoidla ja salvestuskonto saladuste loomiseks.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-107">Use Microsoft Azure to create the secrets for the key vault and storage account.</span></span> <span data-ttu-id="0d1ce-108">Seejärel kasutage saladusi elektroonilise arvelduse lisandmooduli konfigureerimisel.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-108">Then use the secrets in the configuration of Electronic invoicing.</span></span>

## <a name="lifecycle-services"></a><span data-ttu-id="0d1ce-109">Lifecycle Services</span><span class="sxs-lookup"><span data-stu-id="0d1ce-109">Lifecycle Services</span></span>

<span data-ttu-id="0d1ce-110">Kasutage Microsoft Dynamics Lifecycle Services (LCS) et võimaldada mikroteenused sinu LCS juurutamisprojektis.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-110">Use Microsoft Dynamics Lifecycle Services (LCS) to enable the microservices for your LCS deployment project.</span></span>

> [!NOTE]
> <span data-ttu-id="0d1ce-111">Mikroteenuse LCS-i install nõuab vähemalt 2. taseme virtuaalmasinat.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-111">The installation of the microservice in LCS requires at least a Tier 2 virtual machine.</span></span> <span data-ttu-id="0d1ce-112">Lisateavet keskkondade kohta vaadake teemast [Keskkonna planeerimine](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="0d1ce-112">For more information about environment planning, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
 

## <a name="regulatory-configuration-services"></a><span data-ttu-id="0d1ce-113">Regulatory Configuration Services</span><span class="sxs-lookup"><span data-stu-id="0d1ce-113">Regulatory Configuration Services</span></span>

<span data-ttu-id="0d1ce-114">Dynamics 365 Regulatory Configuration Services (RCS) on liides, mida kasutatakse Elektroonilise arvelduse konfigureerimiseks.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-114">Dynamics 365 Regulatory Configuration Services (RCS) is the interface that is used to configure Electronic invoicing.</span></span> <span data-ttu-id="0d1ce-115">Selliseid ressursse nagu keskkonnad ja elektroonilise arvelduse funktsioonid luuakse, hallatakse ja majutatakse RCS-is.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-115">Resources such as environments and electronic invoicing features are created, maintained, and hosted in RCS.</span></span> <span data-ttu-id="0d1ce-116">Kui ressursid on valmis, avaldatakse need elektroonilise arvelduse teenuses.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-116">When the resources are ready, they are published to Electronic invoicing service.</span></span>

<span data-ttu-id="0d1ce-117">RCS-i registreerimiseks vaata [Regulatory services](https://marketing.configure.global.dynamics.com/).</span><span class="sxs-lookup"><span data-stu-id="0d1ce-117">For RCS sign-up, see [Regulatory services](https://marketing.configure.global.dynamics.com/).</span></span>

<span data-ttu-id="0d1ce-118">Lisateavet RCS-i kohta vt teemast [Regulatory Configuration Services (RCS) – globaliseerimisfunktsioonid](rcs-globalization-feature.md).</span><span class="sxs-lookup"><span data-stu-id="0d1ce-118">For more information about RCS, see [Regulatory Configuration Services (RCS) - Globalization features](rcs-globalization-feature.md)</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="0d1ce-119">Elektroonilise arvelduse integratsioon</span><span class="sxs-lookup"><span data-stu-id="0d1ce-119">Integration with Electronic invoicing</span></span> 

<span data-ttu-id="0d1ce-120">Enne kui saate elektrooniliste arvete konfigureerimiseks RCS-i kasutada, peate konfigureerima RCS-i, et lubada andmevahetus elektroonilise arveldusega.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-120">Before you can use RCS to configure electronic invoices, you must configure RCS to allow for communication with Electronic invoicing.</span></span> <span data-ttu-id="0d1ce-121">See konfiguratsioon lõpetatakse lehe **Elektroonilise arvelduse parameetrid** vahekaardil lehel **Elektroonilise aruandluse lisandmoodul**.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-121">You complete this configuration on the **Electronic invoicing** tab of the **Electronic reporting parameters** page.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="0d1ce-122">Teenuse lõpp-punkt</span><span class="sxs-lookup"><span data-stu-id="0d1ce-122">Service endpoint</span></span>

<span data-ttu-id="0d1ce-123">Elektrooniline arveldus on saadaval mitmetes Azure'i geograafilistes andmekeskustes.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-123">Electronic invoicing is available in several Azure datacenter geographies.</span></span> <span data-ttu-id="0d1ce-124">Järgmises tabelis on toodud saadavus piirkonniti.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-124">The following table lists the availability per region.</span></span>

| <span data-ttu-id="0d1ce-125">Azure'i andmekeskuse geograafiline piirkond</span><span class="sxs-lookup"><span data-stu-id="0d1ce-125">Azure datacenter geography</span></span> |
|----------------------------|
| <span data-ttu-id="0d1ce-126">Ida-USA</span><span class="sxs-lookup"><span data-stu-id="0d1ce-126">East US</span></span>                    |
| <span data-ttu-id="0d1ce-127">Lääne-USA</span><span class="sxs-lookup"><span data-stu-id="0d1ce-127">West US</span></span>                    |
| <span data-ttu-id="0d1ce-128">Põhja-EL</span><span class="sxs-lookup"><span data-stu-id="0d1ce-128">North EU</span></span>                   |
| <span data-ttu-id="0d1ce-129">Lääne-EL</span><span class="sxs-lookup"><span data-stu-id="0d1ce-129">West EU</span></span>                    |

### <a name="service-environments"></a><span data-ttu-id="0d1ce-130">Teenusekeskkonnad</span><span class="sxs-lookup"><span data-stu-id="0d1ce-130">Service environments</span></span>

<span data-ttu-id="0d1ce-131">Teenusekeskkonnad on loogilised sektsioonid, mis luuakse elektroonilise arvelduse funktsioonides elektroonilise arvelduse käivitamise toetamiseks.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-131">Service environments are logical partitions that are created to support execution of the electronic invoicing features in Electronic invoicing.</span></span> <span data-ttu-id="0d1ce-132">Turvasaladused ja digitaalserdid ning juhtimine (st juurdepääsuload) peavad olema konfigureeritud teenusekeskkonna tasemel.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-132">The security secrets and digital certificates, and the governance (that is, access permissions), must be configured at the service environment level.</span></span>

<span data-ttu-id="0d1ce-133">Kliendid saavad luua nii palju teenusekeskkondi, kui nad soovivad.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-133">Customers can create as many service environments as they want.</span></span> <span data-ttu-id="0d1ce-134">Kõik teenusekeskkonnad, mille klient loob, on üksteisest sõltumatud.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-134">All the service environments that a customer creates are independent of each other.</span></span>

<span data-ttu-id="0d1ce-135">Teenusekeskkonnad saab luua ja neid saab hooldada RCS-is.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-135">Service environments must be created and maintained in RCS.</span></span> <span data-ttu-id="0d1ce-136">Kui teenusekeskkonnad on valmis, tuleb need elektroonilise arvelduses avaldada.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-136">When the service environments are ready, they must be published to Electronic invoicing.</span></span>

#### <a name="service-environment-status"></a><span data-ttu-id="0d1ce-137">Teenusekeskkonna olek</span><span class="sxs-lookup"><span data-stu-id="0d1ce-137">Service environment status</span></span>

<span data-ttu-id="0d1ce-138">Teenusekeskkondi saab hallata oleku kaudu.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-138">Service environments can be managed through status.</span></span> <span data-ttu-id="0d1ce-139">Saadaval on järgmised valikud.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-139">The possible options are:</span></span>

- <span data-ttu-id="0d1ce-140">**Pole avaldatud** – keskkond on loodud, kuid seda pole veel avaldatud.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-140">**Not published** – The environment has been created, but it hasn't yet been published.</span></span>
- <span data-ttu-id="0d1ce-141">**Avaldatud** – Keskkond on elektroonilise arvelduses avaldatud .</span><span class="sxs-lookup"><span data-stu-id="0d1ce-141">**Published** – The environment has been published to Electronic invoicing .</span></span>
- <span data-ttu-id="0d1ce-142">**Muudetud** – avaldatud keskkonna atribuute on muudetud, kuid muudatusi pole veel avaldatud.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-142">**Changed** – The attributes of a published environment have been changed, but the changes haven't yet been published.</span></span>

#### <a name="customer-secrets"></a><span data-ttu-id="0d1ce-143">Klientide saladused</span><span class="sxs-lookup"><span data-stu-id="0d1ce-143">Customer secrets</span></span>

<span data-ttu-id="0d1ce-144">Elektroonilise arvelduse teenus vastutab kõigi teie äriandmete talletamise eest Azure'i ressurssides, mis kuuluvad teie ettevõttele.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-144">The Electronic invoicing service is responsible for storing all your business data in the Azure resources that your company owns.</span></span> <span data-ttu-id="0d1ce-145">Kindlustamaks seda, et teenus korrektselt töötab ja et kõik äriandmed on nõutud ja loodud Elektroonilise arvelduse jaoks sobivalt saadaval,peate looma kaks peamist Azure-i ressurssi:</span><span class="sxs-lookup"><span data-stu-id="0d1ce-145">To ensure that the service works correctly, and that all the business data that is required for and generated by Electronic invoicing is accessed appropriately, you must create two main Azure resources:</span></span>

- <span data-ttu-id="0d1ce-146">Azure'i salvestuskonto (bloobimälu) elektrooniliste arvete talletamiseks</span><span class="sxs-lookup"><span data-stu-id="0d1ce-146">An Azure storage account (Blob storage) that will store electronic invoices</span></span>
- <span data-ttu-id="0d1ce-147">Azure'i võtmehoidla sertide ja salvestuskonto ühtse ressursi-indikaatori (URI) talletamiseks</span><span class="sxs-lookup"><span data-stu-id="0d1ce-147">An Azure key vault that will store certificates and the uniform resource identifier (URI) of the storage account</span></span>

> [!NOTE]
> <span data-ttu-id="0d1ce-148">Spetsiaalne võtmehoidla ja kliendi salvestuskonto peab Elektroonilise arvelduse jaoks olema määratud.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-148">A dedicated key vault and customer storage account must be allocated specifically for use with the Electronic invoicing .</span></span>

<span data-ttu-id="0d1ce-149">Lisateavet vt teemast [Azure'i salvestuskonto ja võtmehoidla loomine](e-invoicing-create-azure-storage-account-key-vault.md).</span><span class="sxs-lookup"><span data-stu-id="0d1ce-149">For more information, see [Create an Azure storage account and a key vault](e-invoicing-create-azure-storage-account-key-vault.md).</span></span>

#### <a name="users"></a><span data-ttu-id="0d1ce-150">Kasutajad</span><span class="sxs-lookup"><span data-stu-id="0d1ce-150">Users</span></span>

<span data-ttu-id="0d1ce-151">Iga teenusekeskkond peab loetlema kasutajad, kes saavad ühenduda Elektroonilise arvelduse jaoks Dynamics 365 Finance and Dynamics 365 Supply Chain Management -iga.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-151">Each service environment must list the users who can connect from Dynamics 365 Finance and Dynamics 365 Supply Chain Management in Electronic invoicing.</span></span>

#### <a name="publication"></a><span data-ttu-id="0d1ce-152">Avaldamine</span><span class="sxs-lookup"><span data-stu-id="0d1ce-152">Publication</span></span>

<span data-ttu-id="0d1ce-153">Enne teenusekeskkondade kasutamist tuleb need elektroonilises arvelduses avaldada.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-153">Service environments must be published to Electronic invoicing before they can be used.</span></span> <span data-ttu-id="0d1ce-154">Teenuste Finance ja Supply Chain Management kaudu pääseb juurde ainult avaldatud keskkondadele.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-154">Only published environments can be accessed by Finance and Supply Chain Management.</span></span> <span data-ttu-id="0d1ce-155">Peale selle tuleb teenusekeskkond avaldada, enne kui selle atribuutide värskendused elektroonilise arvelduse teenuses jõustuvad.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-155">Additionally, a service environment must be published before any updates to its attributes will take effect on the electronic invoicing service.</span></span>

### <a name="connected-applications"></a><span data-ttu-id="0d1ce-156">Ühendatud avaldused</span><span class="sxs-lookup"><span data-stu-id="0d1ce-156">Connected applications</span></span>

<span data-ttu-id="0d1ce-157">Ühendatud rakendused on teenuste Finance and Supply Chain Management eksemplarid, millega võite soovida RCS-i kaudu ühendust saada.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-157">Connected applications are the instances of Finance and Supply Chain Management that you might want to reach through RCS.</span></span> <span data-ttu-id="0d1ce-158">Peale rakenduse URL-i ja selle rentniku hõlmab ühendatud rakendus mandaate, mis võimaldavad RCS-il keskkonnaga ühenduse luua.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-158">Besides the application URL and its tenant, a connected application contains the credentials that enable RCS to connect to the environment.</span></span>

<span data-ttu-id="0d1ce-159">Ühendatud rakenduste abil saate konfigureerida osa elektroonilise arvelduse funktsioonist teenustes Finance ja Supply Chain Management, et kogu elektroonilise arvelduse funktsioon tööle saada.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-159">Through the connected applications, you can configure part of the electronic invoicing feature in Finance and Supply Chain Management to make the whole electronic invoicing feature work.</span></span>

## <a name="finance-and-supply-chain-management"></a><span data-ttu-id="0d1ce-160">Finance ja Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="0d1ce-160">Finance and Supply Chain Management</span></span>

### <a name="integration-with-electronic-invoicing"></a><span data-ttu-id="0d1ce-161">Elektroonilise arvelduse integratsioon</span><span class="sxs-lookup"><span data-stu-id="0d1ce-161">Integration with Electronic invoicing</span></span>

<span data-ttu-id="0d1ce-162">Enne kui saate teenuseid Finance ja Supply Chain Management elektroonilise arvelduse lisandmooduli kaudu elektrooniliste arvete väljastamiseks kasutada, tuleb lisandmoodul konfigureerida nii, et see lubaks teenusega suhtlemist.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-162">Before you can use Finance and Supply Chain Management to issue electronic invoices through Electronic invoicing, it must be configured to allow for communication with the service.</span></span>

#### <a name="electronic-invoicing-integration-feature"></a><span data-ttu-id="0d1ce-163">Elektroonilise arvelduse integratsiooni funktsioon</span><span class="sxs-lookup"><span data-stu-id="0d1ce-163">Electronic invoicing integration feature</span></span>

<span data-ttu-id="0d1ce-164">Teenuste Finance ja Supply Chain Management ning elektroonilise arvelduse lisandmooduli vahelise suhtluse lubamiseks peate tööruumis **Funktsioonihaldus** funktsiooni **Elektroonilise arvelduse lisandmooduli integreerimine** sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-164">To enable communication between Finance and Supply Chain Management and Electronic invoicing, you must turn on the **Electronic Invoicing integration** feature in the **Feature management** workspace.</span></span>

#### <a name="service-endpoint"></a><span data-ttu-id="0d1ce-165">Teenuse lõpp-punkt</span><span class="sxs-lookup"><span data-stu-id="0d1ce-165">Service endpoint</span></span>

<span data-ttu-id="0d1ce-166">Teenuse lõpp-punkt on elektroonilise arvelduse asukoha URL.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-166">The service endpoint is the URL where Electronic invoicing is located.</span></span> <span data-ttu-id="0d1ce-167">Enne kui saab väljastada elektroonilisi arveid, tuleb teenuse lõpp-punkt konfigureerida teenustes Finance ja Supply Chain Management nii, et see lubaks teenusega suhtlemist.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-167">Before electronic invoices can be issued, the service endpoint must be configured in Finance and Supply Chain Management to allow for communication with the service.</span></span>

<span data-ttu-id="0d1ce-168">Teenuse lõpp-punkti konfigureerimiseks minge **Organisatsiooni haldus \> Seadistus \> Elektroonilise dokumendi parameeter** ja seejärel sisestage vahekaardi **Edastusteenused** väljale **Elektroonilise arvelduse URL** URL, nagu on kirjeldatud jaotises **Teenuse lõpp-punkt** näidatud tabelis.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-168">To configure the service endpoint, go to **Organization administration \> Setup \> Electronic document parameter**, and then, on the **Submission services** tab, in the **Electronic invoicing URL** field, enter the URL as described in the table described in section **Service endpoint**.</span></span>

#### <a name="environments"></a><span data-ttu-id="0d1ce-169">Keskkonnad</span><span class="sxs-lookup"><span data-stu-id="0d1ce-169">Environments</span></span>

<span data-ttu-id="0d1ce-170">Keskkonna nimi, mis on sisestatud Finants ja Supply Chain Management -i viitab keskkonna nimele, mis on loodud RCS-is ja avaldatud Elektroonilises arvelduses.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-170">The environment name that is entered in Finance and Supply Chain Management refers to the name of the environment that is created in RCS and published to Electronic invoicing.</span></span>

<span data-ttu-id="0d1ce-171">Keskkond tuleb konfigureerida lehe **Elektroonilise dokumendi parameetrid** vahekaardil **Edastusteenused**, nii et kõik elektrooniliste arvete väljastamistaotlused hõlmavad keskkonda, kus elektroonilise arvelduse lisandmoodul saab määrata, milline elektroonilise arvelduse funktsioon peab taotlust töötlema.</span><span class="sxs-lookup"><span data-stu-id="0d1ce-171">The environment must be configured on the **Submission services** tab of the **Electronic document parameter** page, so that every request to issue electronic invoices contains the environment where Electronic invoicing can determine which electronic invoicing feature must process the request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0d1ce-172">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="0d1ce-172">Additional resources</span></span>

- [<span data-ttu-id="0d1ce-173">Elektrooniliste arvete konfigureerimine RCS-is</span><span class="sxs-lookup"><span data-stu-id="0d1ce-173">Configure electronic invoices in RCS</span></span>](e-invoicing-configuration-rcs.md)
- [<span data-ttu-id="0d1ce-174">Elektroonilise arvete väljastamine teenustes Finance ja Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="0d1ce-174">Issue electronic invoices in Finance and Supply Chain Management</span></span>](e-invoicing-issuing-electronic-invoices-finance-supply-chain-management.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
