---
title: Sisu tarne võrgu rakendamise suvandid
description: See teema annab ülevaate erinevatest võimalustest sisu tarnevõrgu (CDN) rakendamise kohta, mida saab kasutada Microsoft Dynamics 365 Commerce keskkondades. Need valikud on rakenduse Azure Front Door rakenduse Commerce antud eksemplarid ja Azure Front Door kliendi-eksemplarid.
author: BrianShook
ms.date: 03/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2020-11-01
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 9e98cf81f13b9181059bc96b95ac277a088311ea
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800707"
---
# <a name="content-delivery-network-implementation-options"></a><span data-ttu-id="e82f5-104">Sisu tarne võrgu rakendamise suvandid</span><span class="sxs-lookup"><span data-stu-id="e82f5-104">Content delivery network implementation options</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e82f5-105">See teema annab ülevaate erinevatest võimalustest sisu tarnevõrgu (CDN) rakendamise kohta, mida saab kasutada Microsoft Dynamics 365 Commerce keskkondades.</span><span class="sxs-lookup"><span data-stu-id="e82f5-105">This topic reviews the different options for content delivery network (CDN) implementation that can be used with Microsoft Dynamics 365 Commerce environments.</span></span> <span data-ttu-id="e82f5-106">Need valikud on rakenduse Azure Front Door rakenduse Commerce antud eksemplarid ja Azure Front Door kliendi-eksemplarid.</span><span class="sxs-lookup"><span data-stu-id="e82f5-106">These options include native, Commerce-provided instances of Azure Front Door and customer-owned instances of Azure Front Door.</span></span>

<span data-ttu-id="e82f5-107">Äriklientidel on mitu valikut, kui nad kaaluvad, millist CDN-teenust oma Ärikeskkonnas kasutada.</span><span class="sxs-lookup"><span data-stu-id="e82f5-107">Commerce customers have several options when they are considering which CDN service to use with their Commerce environment.</span></span> <span data-ttu-id="e82f5-108">Commerce on vabastatud põhilise Azure Front Door toega, mis katab baashostimis- ja kohandatud domeeninõudeid.</span><span class="sxs-lookup"><span data-stu-id="e82f5-108">Commerce is released with basic Azure Front Door support that covers basic hosting and custom domain requirements.</span></span> <span data-ttu-id="e82f5-109">Ettevõtete puhul, kes soovivad rohkem kontrolli ja spetsiifilisesid turvavõimeid, nagu veebirakenduse tulemüür (WAF), on parim valik kasutada kas Azure Front Doori kliendiomast eksemplari või välist CDN-teenust.</span><span class="sxs-lookup"><span data-stu-id="e82f5-109">For companies that want more control and more specific security abilities, such as a web application firewall (WAF), the best option might be to use either a customer-owned instance of Azure Front Door or an external CDN service.</span></span>

<span data-ttu-id="e82f5-110">Commerce'i keskkondades saab kasutada kolme CDN-i rakendusvalikut:</span><span class="sxs-lookup"><span data-stu-id="e82f5-110">The following three CDN implementation options can be used with Commerce environments:</span></span>

- <span data-ttu-id="e82f5-111">Saate kasutada Commerce'i pakutavat Azure Front Door eksemplari</span><span class="sxs-lookup"><span data-stu-id="e82f5-111">The Commerce-provided instance of Azure Front Door</span></span>
- <span data-ttu-id="e82f5-112">Kliendi omanduses olev Azure Front Door eksemplar (suurema kontrolli ja täiendavate turvafunktsioonide jaoks)</span><span class="sxs-lookup"><span data-stu-id="e82f5-112">A customer-owned instance of Azure Front Door (for increased control and additional security features)</span></span>
- <span data-ttu-id="e82f5-113">Väline CDN-teenus</span><span class="sxs-lookup"><span data-stu-id="e82f5-113">An external CDN service</span></span>

<span data-ttu-id="e82f5-114">Kõik kolm CDN-i rakendusvalikut annavad kohandatud domeenidest ainult dünaamilise HTML-sisu.</span><span class="sxs-lookup"><span data-stu-id="e82f5-114">All three CDN implementation options deliver only dynamic HTML content from custom domains.</span></span> <span data-ttu-id="e82f5-115">Commerce halddab Microsofti hallatud CDN-ide kaudu automaatselt kõigi JavaScript, kaskaadstiililehti (CSS), pilte, videosid ja muud staatilist sisu.</span><span class="sxs-lookup"><span data-stu-id="e82f5-115">Commerce automatically handles all JavaScript, Cascading Style Sheets (CSS), images, video, and other static content through Microsoft-managed CDNs.</span></span> <span data-ttu-id="e82f5-116">Teie valitud suvand määrab saadaolevad tegevusvõimalused, juhtimisvõimalused ja täiendavad turvavõimalused.</span><span class="sxs-lookup"><span data-stu-id="e82f5-116">The option that you choose determines the operational capabilities, control capabilities, and additional security capabilities that are available.</span></span>

<span data-ttu-id="e82f5-117">Järgmisel joonisel on näidatud ülevaade pakkumiskutse protsessist.</span><span class="sxs-lookup"><span data-stu-id="e82f5-117">The following illustration shows an overview of the Commerce architecture.</span></span>

![Ülevaade kaubanduse ülesehitusest](media/Commerce_CDN-Option_ComparisonModels.png)

<span data-ttu-id="e82f5-119">Lisateavet Rakenduse Azure Front Door eksemplari häälestamise kohta ärisaidi jaoks vt [Lisa CDN-tugi](add-cdn-support.md).</span><span class="sxs-lookup"><span data-stu-id="e82f5-119">For more information about how to set up an instance of Azure Front Door for your Commerce site, see [Add CDN Support](add-cdn-support.md).</span></span>

## <a name="use-the-commerce-provided-azure-front-door-instance"></a><span data-ttu-id="e82f5-120">Saate kasutada Commerce'i pakutavat Azure Front Door eksemplari</span><span class="sxs-lookup"><span data-stu-id="e82f5-120">Use the Commerce-provided Azure Front Door instance</span></span>

<span data-ttu-id="e82f5-121">Järgmises tabelis loetletakse rakenduse Azure Front Door Commerce-antud eksemplari kasutamise plusse ja miinuseid sisu lõpp-punktide haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="e82f5-121">The following table lists the pros and cons of using the Commerce-provided instance of Azure Front Door to manage content endpoints.</span></span>

| <span data-ttu-id="e82f5-122">Plusse</span><span class="sxs-lookup"><span data-stu-id="e82f5-122">Pros</span></span> | <span data-ttu-id="e82f5-123">Miinuseid</span><span class="sxs-lookup"><span data-stu-id="e82f5-123">Cons</span></span> |
|------|------|
| <ul><li><span data-ttu-id="e82f5-124">Eksemplar kaasatakse ärikulusse.</span><span class="sxs-lookup"><span data-stu-id="e82f5-124">The instance is included in the Commerce cost.</span></span></li><li><span data-ttu-id="e82f5-125">Kuna ärimeeskond haldab eksemplari, on vajalik väiksem hooldus ja häälestusetappideks on ühiskasutusega etapid.</span><span class="sxs-lookup"><span data-stu-id="e82f5-125">Because the instance is managed by the Commerce team, less maintenance is required, and there are shared setup steps.</span></span></li><li><span data-ttu-id="e82f5-126">Azure'i majutatud infrastruktuur on skaleeritav, turvaline ja usaldusväärne.</span><span class="sxs-lookup"><span data-stu-id="e82f5-126">The Azure-hosted infrastructure is scalable, secure, and reliable.</span></span></li><li><span data-ttu-id="e82f5-127">Secure Sockets Layeri (SSL) sert nõuab kellaaja seadistust ja seda uuendatakse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="e82f5-127">The Secure Sockets Layer (SSL) certificate requires a one-time setup and is automatically renewed.</span></span></li><li><span data-ttu-id="e82f5-128">Ärimeeskond jälgib eksemplari vigade ja hälbide suhtes.</span><span class="sxs-lookup"><span data-stu-id="e82f5-128">The instance is monitored for errors and anomalies by the Commerce team.</span></span></li></ul> | <ul><li><span data-ttu-id="e82f5-129">WAFi ei toetata.</span><span class="sxs-lookup"><span data-stu-id="e82f5-129">A WAF isn't supported.</span></span></li><li><span data-ttu-id="e82f5-130">Konkreetseid kohandusi ega seadistuse korrigeerimisi pole.</span><span class="sxs-lookup"><span data-stu-id="e82f5-130">There are no specific customizations or setting adjustments.</span></span></li><li><span data-ttu-id="e82f5-131">Eksemplar sõltub ärimeeskonnast uuenduste või muudatuste puhul.</span><span class="sxs-lookup"><span data-stu-id="e82f5-131">The instance depends on the Commerce team for updates or changes.</span></span></li><li><span data-ttu-id="e82f5-132">Domeenide ja laiendusdomeenide integreerimiseks Azure'i DNS-iga on vaja eraldi Azure Front Door eksemplari.</span><span class="sxs-lookup"><span data-stu-id="e82f5-132">A separate Azure Front Door instance is required for apex domains, and extra work is required to integrate apex domains with Azure DNS.</span></span></li><li><span data-ttu-id="e82f5-133">Puudub telemeetria vastuste kohta sekundis (RPS) või kliendile pakutakse veamäära.</span><span class="sxs-lookup"><span data-stu-id="e82f5-133">No telemetry about responses per second (RPS) or the error rate is provided to the customer.</span></span></li></ul> |

<span data-ttu-id="e82f5-134">Järgmine näide näitab Commerce-toetatud Azure Front Door\`i eksemplari arhitektuuri.</span><span class="sxs-lookup"><span data-stu-id="e82f5-134">The following illustration shows the architecture of the Commerce-provided Azure Front Door instance.</span></span>

![Saate kasutada Commerce'i pakutavat Azure Front Door eksemplari](media/Commerce_CDN-Option_CommerceFrontDoor.png)

## <a name="use-a-customer-owned-azure-front-door-instance"></a><span data-ttu-id="e82f5-136">Kasuta kliendi-põhist Azure Front Door eksemplari</span><span class="sxs-lookup"><span data-stu-id="e82f5-136">Use a customer-owned Azure Front Door instance</span></span>

<span data-ttu-id="e82f5-137">Järgmises tabelis loetletakse rakenduse Azure Front Door Commerce-antud eksemplari kasutamise plusse ja miinuseid sisu lõpp-punktide haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="e82f5-137">The following table lists the pros and cons of using a customer-owned instance of Azure Front Door to manage content endpoints.</span></span>

| <span data-ttu-id="e82f5-138">Plusse</span><span class="sxs-lookup"><span data-stu-id="e82f5-138">Pros</span></span> | <span data-ttu-id="e82f5-139">Miinuseid</span><span class="sxs-lookup"><span data-stu-id="e82f5-139">Cons</span></span> |
|------|------|
| <ul><li><span data-ttu-id="e82f5-140">Seadistus on turvaline ja seda on lihtne hallata.</span><span class="sxs-lookup"><span data-stu-id="e82f5-140">Setup is secure and easy to manage.</span></span></li><li><span data-ttu-id="e82f5-141">Azure'i majutatud infrastruktuur on skaleeritav, turvaline ja usaldusväärne.</span><span class="sxs-lookup"><span data-stu-id="e82f5-141">The Azure-hosted infrastructure is scalable, secure, and reliable.</span></span></li><li><span data-ttu-id="e82f5-142">Eksemplar võimaldab WAF-i integreerimist ja granulaarreegli juhtimist trahvija astme turvalisusele, mis on häälestatud konkreetselt teie saidile.</span><span class="sxs-lookup"><span data-stu-id="e82f5-142">The instance allows for WAF integration and granular rule controls for finer-grade security that is tuned specifically for your site.</span></span></li><li><span data-ttu-id="e82f5-143">Eksemplar võimaldab SSL-sertifikaatide (nii kliendi omad kui ka Azure Front Door-hallatud) ja domeeni seostamist trahvija kontrolli.</span><span class="sxs-lookup"><span data-stu-id="e82f5-143">The instance allows for finer control of SSL certificates (both customer-owned and Azure Front Door–managed) and domain linking.</span></span></li><li><span data-ttu-id="e82f5-144">Eksemplar pakub apex domeenilahendust, kui see on ühendatud otse Azure DNS-iga.</span><span class="sxs-lookup"><span data-stu-id="e82f5-144">The instance offers an apex domain solution if it's paired directly with Azure DNS.</span></span></li><li><span data-ttu-id="e82f5-145">Antakse telemeetria ja teatis.</span><span class="sxs-lookup"><span data-stu-id="e82f5-145">Telemetry and alerting are provided.</span></span></li><li><span data-ttu-id="e82f5-146">Secure Sockets Layeri (SSL) sert nõuab kellaaja seadistust ja seda uuendatakse automaatselt.</span><span class="sxs-lookup"><span data-stu-id="e82f5-146">The SSL certificate requires a one-time setup and is automatically renewed.</span></span></li></ul> | <ul><li><span data-ttu-id="e82f5-147">Eksemplar on ise hallatav.</span><span class="sxs-lookup"><span data-stu-id="e82f5-147">The instance is self-managed.</span></span></li><li><span data-ttu-id="e82f5-148">Nõutakse algset teadmiste kogust.</span><span class="sxs-lookup"><span data-stu-id="e82f5-148">Initial knowledge ramp-up is required.</span></span></li></ul> |

<span data-ttu-id="e82f5-149">Järgmine näide näitab äri infrastruktuuri, mis sisaldab kliendi-omast Azure Front Door\`i eksemplari.</span><span class="sxs-lookup"><span data-stu-id="e82f5-149">The following illustration shows a Commerce infrastructure that includes a customer-owned Azure Front Door instance.</span></span>

![Järgmine näide näitab äri infrastruktuuri, mis sisaldab kliendi-omast Azure Front Door\`i eksemplari](media/Commerce_CDN-Option_CustomerOwnedAzureFrontDoor.png)

## <a name="use-an-external-cdn-service"></a><span data-ttu-id="e82f5-151">Väline CDN-teenus</span><span class="sxs-lookup"><span data-stu-id="e82f5-151">Use an external CDN service</span></span>

<span data-ttu-id="e82f5-152">Järgmises tabelis loetletakse välise CDN-teenuse kasutamise plussid ja miinused sisu lõpp-punktide haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="e82f5-152">The following table lists the pros and cons of using an external CDN service to manage content endpoints.</span></span>

| <span data-ttu-id="e82f5-153">Plusse</span><span class="sxs-lookup"><span data-stu-id="e82f5-153">Pros</span></span> | <span data-ttu-id="e82f5-154">Miinuseid</span><span class="sxs-lookup"><span data-stu-id="e82f5-154">Cons</span></span> |
|------|------|
| <ul><li><span data-ttu-id="e82f5-155">See valik on kasulik, kui olemasolev domeen on juba majutatud välisele CDN-ile.</span><span class="sxs-lookup"><span data-stu-id="e82f5-155">This option is useful when the existing domain is already hosted on an external CDN.</span></span></li><li><span data-ttu-id="e82f5-156">Konkurendi CDN-il (nt Atagem) võib olla rohkem WAF-võimalusi.</span><span class="sxs-lookup"><span data-stu-id="e82f5-156">Competitor CDNs (for example, Akamai) might have more WAF capabilities.</span></span></li></ul> | <ul><li><span data-ttu-id="e82f5-157">Eraldi leping ja täiendav kuluarvestus on nõutavad.</span><span class="sxs-lookup"><span data-stu-id="e82f5-157">A separate contract and additional costing are required.</span></span></li><li><span data-ttu-id="e82f5-158">SSL võib vajada lisakulusid.</span><span class="sxs-lookup"><span data-stu-id="e82f5-158">SSL might incur additional costs.</span></span></li><li><span data-ttu-id="e82f5-159">Kuna teenus on eraldi Azure'i pilvestruktuurist, tuleb hallata lisa infrastruktuuri.</span><span class="sxs-lookup"><span data-stu-id="e82f5-159">Because the service is separate from the Azure cloud structure, additional infrastructure must be managed.</span></span></li><li><span data-ttu-id="e82f5-160">Teenus võib nõuda pikemaid ajainvesteeringuid lõpp-punkti ja turvalisuse seadistusse.</span><span class="sxs-lookup"><span data-stu-id="e82f5-160">The service might require longer time investments in endpoint and security setup.</span></span></li><li><span data-ttu-id="e82f5-161">Teenus on ise hallatav.</span><span class="sxs-lookup"><span data-stu-id="e82f5-161">The service is self-managed.</span></span></li><li><span data-ttu-id="e82f5-162">Teenus on ise jälgitav.</span><span class="sxs-lookup"><span data-stu-id="e82f5-162">The service is self-monitored.</span></span></li></ul> |

<span data-ttu-id="e82f5-163">Järgmine näide näitab Äri infrastruktuuri, mis sisaldab välist CDN-teenust.</span><span class="sxs-lookup"><span data-stu-id="e82f5-163">The following illustration shows a Commerce infrastructure that includes an external CDN service.</span></span>

![Äri infrastruktuur, mis sisaldab välist CDN-teenust](media/Commerce_CDN-Option_ExternalFrontDoor.png)

## <a name="additional-resources"></a><span data-ttu-id="e82f5-165">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="e82f5-165">Additional resources</span></span>

[<span data-ttu-id="e82f5-166">Sisu edastamise võrgu (CDN) toe lisamine</span><span class="sxs-lookup"><span data-stu-id="e82f5-166">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)
