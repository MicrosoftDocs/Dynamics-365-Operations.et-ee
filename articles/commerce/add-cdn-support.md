---
title: Sisuedastusvõrgu (CDN) toe lisamine
description: See teema kirjeldab, kuidas lisada oma Microsoft Dynamics 365 Commerce keskkonnale sisuedastusvõrk (CDN).
author: brianshook
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d2d64f0de5287a764cb2e40b99a08084494bf53c
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945624"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="62e07-103">Sisuedastusvõrgu (CDN) toe lisamine</span><span class="sxs-lookup"><span data-stu-id="62e07-103">Add support for a content delivery network (CDN)</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="62e07-104">See teema kirjeldab, kuidas lisada oma Microsoft Dynamics 365 Commerce keskkonnale sisuedastusvõrk (CDN).</span><span class="sxs-lookup"><span data-stu-id="62e07-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

## <a name="overview"></a><span data-ttu-id="62e07-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="62e07-105">Overview</span></span>

<span data-ttu-id="62e07-106">Rakenduses Dynamics 365 Commerce e-kaubanduse keskkonda seadistades saate konfigureerida selle töötama koos oma CDN-i teenusega.</span><span class="sxs-lookup"><span data-stu-id="62e07-106">When you set up an e-Commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="62e07-107">Teie kohandatud domeeni saab lubada e-kaubanduse keskkonna ettevalmistamisprotsessi käigus.</span><span class="sxs-lookup"><span data-stu-id="62e07-107">Your custom domain can be enabled during the provisioning process for your e-Commerce environment.</span></span> <span data-ttu-id="62e07-108">Teise võimalusena saate kasutada teenusetaotlust, et seadistada see pärast ettevalmistusprotsessi lõpetamist.</span><span class="sxs-lookup"><span data-stu-id="62e07-108">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="62e07-109">E-kaubanduse keskkonna ettevalmistamisprotsess loob hostinime, mis on keskkonnaga seotud.</span><span class="sxs-lookup"><span data-stu-id="62e07-109">The provisioning process for the e-Commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="62e07-110">Sellel hostinimel on järgmine vorming, kus *e-kaubanduse-rentniku-nimi* on teie keskkonna nimi:</span><span class="sxs-lookup"><span data-stu-id="62e07-110">This host name has the following format, where *e-commerce-tenant-name* is the name of your environment:</span></span>

<span data-ttu-id="62e07-111">&lt;e-kaubanduse-rentniku-nimi&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="62e07-111">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="62e07-112">Ettevalmistusprotsessi käigus loodud hostinimi või lõpp-punkt toetab turvasoklite kihi (SSL) serti ainult \*.commerce.dynamics.com-i jaoks.</span><span class="sxs-lookup"><span data-stu-id="62e07-112">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="62e07-113">See ei toeta kohandatud domeenide SSL-i.</span><span class="sxs-lookup"><span data-stu-id="62e07-113">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="62e07-114">Seega peate kohandatud domeenide SSL-i määrama oma CDN-is ja edastama liikluse CDN-ist kaubanduse loodud hostinimele või lõpp-punktile.</span><span class="sxs-lookup"><span data-stu-id="62e07-114">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="62e07-115">Lisaks teenindatakse lõpp-punktist Commerce’i *staatika* (JavaScripti või kaskaadlaadistiku \[CSS\] faile), mille Commerce genereeris (\*.commerce.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="62e07-115">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="62e07-116">Staatika saab vahemällu salvestada ainult siis, kui Commerce’i genereeritud hostinimi või lõpp-punkt lisatakse on CDN-i taha.</span><span class="sxs-lookup"><span data-stu-id="62e07-116">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="62e07-117">SSL-i seadistamine</span><span class="sxs-lookup"><span data-stu-id="62e07-117">Set up SSL</span></span>

<span data-ttu-id="62e07-118">SSL-i seadistamise ja staatika vahemällu salvestamise tagamiseks peate konfigureerima oma CDN-i nii, et see on seostatud teie keskkonna jaoks loodud Commerce’i nimega.</span><span class="sxs-lookup"><span data-stu-id="62e07-118">To help guarantee that SSL is set up, and that statics are cached, you must configure your CDN so that it is associated with the host name that Commerce generated for your environment.</span></span> <span data-ttu-id="62e07-119">Staatika jaoks peate salvestama vahemällu ka järgmise mustri:</span><span class="sxs-lookup"><span data-stu-id="62e07-119">You must also cache the following pattern for statics only:</span></span> 

<span data-ttu-id="62e07-120">/\_msdyn365/\_scnr/\*</span><span class="sxs-lookup"><span data-stu-id="62e07-120">/\_msdyn365/\_scnr/\*</span></span>

<span data-ttu-id="62e07-121">Pärast antud kohandatud domeeniga Commerce’i keskkonna ettevalmistamist või pärast oma keskkonnale teenusetaotlust kasutades kohandatud domeeni sisestamist, suunake oma kohandatud domeen Commerce’i loodud hostinimele või lõpp-punktile.</span><span class="sxs-lookup"><span data-stu-id="62e07-121">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, point your custom domain to the host name or endpoint that Commerce generated.</span></span>

<span data-ttu-id="62e07-122">Nagu eelnevalt mainitud, toetab loodud hostinimi või lõpp-punkt SSL-i serti ainult \*.commerce.dynamics.com-i jaoks.</span><span class="sxs-lookup"><span data-stu-id="62e07-122">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="62e07-123">See ei toeta kohandatud domeenide SSL-i.</span><span class="sxs-lookup"><span data-stu-id="62e07-123">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="62e07-124">CDN-teenused</span><span class="sxs-lookup"><span data-stu-id="62e07-124">CDN services</span></span>

<span data-ttu-id="62e07-125">Commerce’i keskkonnaga saab kasutada mis tahes CDN-i teenust.</span><span class="sxs-lookup"><span data-stu-id="62e07-125">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="62e07-126">Järgmisena on toodud kaks näidet.</span><span class="sxs-lookup"><span data-stu-id="62e07-126">Here are two examples:</span></span>

- <span data-ttu-id="62e07-127">**Microsoft Azure’i sisenemispunkti teenus** – Azure’i CDN-i lahendus.</span><span class="sxs-lookup"><span data-stu-id="62e07-127">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="62e07-128">Lisateavet Azure’i sisenemispunkti teenuse kohta vt [Azure’i sisenemispunkti teenuse dokumentatsioon](https://docs.microsoft.com/azure/frontdoor/).</span><span class="sxs-lookup"><span data-stu-id="62e07-128">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="62e07-129">**Akamai dünaamiline saidi kiirendi** – lisateavet vaadake teemast [Dünaamiline saidi kiirendi](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span><span class="sxs-lookup"><span data-stu-id="62e07-129">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="62e07-130">CDN häälestus</span><span class="sxs-lookup"><span data-stu-id="62e07-130">CDN setup</span></span>

<span data-ttu-id="62e07-131">CDN-i seadistamise protsess koosneb järgnevatest üldistest etappidest.</span><span class="sxs-lookup"><span data-stu-id="62e07-131">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="62e07-132">Lisage eesserveri host.</span><span class="sxs-lookup"><span data-stu-id="62e07-132">Add a front-end host.</span></span>
1. <span data-ttu-id="62e07-133">Konfigureerige lõppserveri kaust.</span><span class="sxs-lookup"><span data-stu-id="62e07-133">Configure a back-end pool.</span></span>
1. <span data-ttu-id="62e07-134">Seadistage marsruudivalik ja vahemällu salvestamine.</span><span class="sxs-lookup"><span data-stu-id="62e07-134">Set up rules for routing and caching.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="62e07-135">Eesserveri hosti lisamine</span><span class="sxs-lookup"><span data-stu-id="62e07-135">Add a front-end host</span></span>

<span data-ttu-id="62e07-136">Kasutada võib mis tahes CDN-i teenust, kuid näiteks selles teemas kasutatakse Azure’i sisenemispunkti teenust.</span><span class="sxs-lookup"><span data-stu-id="62e07-136">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="62e07-137">Teavet Azure’i sisenemispunkti teenuse seadistamise kohta vaadake teemast [Lühijuhend: suure saadavusega globaalse veebirakenduse jaoks sisenemispunkti loomine](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span><span class="sxs-lookup"><span data-stu-id="62e07-137">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-back-end-pool-in-azure-front-door-service"></a><span data-ttu-id="62e07-138">Azure’i sisenemispunkti teenuses lõppserveri kausta konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="62e07-138">Configure a back-end pool in Azure Front Door Service</span></span>

<span data-ttu-id="62e07-139">Azure’i sisenemispunkti teenuses lõppserveri kausta konfigureerimiseks järgige järgmisi etappe.</span><span class="sxs-lookup"><span data-stu-id="62e07-139">To configure a back-end pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="62e07-140">Lisage lõppserveri kaustale kohandatud hostiks **&lt;ecom-rentniku-nimi&gt;.commerce.dynamics.com**, millel on tühi lõppserveri hosti päis.</span><span class="sxs-lookup"><span data-stu-id="62e07-140">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a back-end pool as a custom host that has an empty back-end host header.</span></span>
1. <span data-ttu-id="62e07-141">Suvandis **Seisundiuuringud** väljal **Tee** sisestage **/keepalive**.</span><span class="sxs-lookup"><span data-stu-id="62e07-141">Under **Health probes**, in the **Path** field, enter **/keepalive**.</span></span>
1. <span data-ttu-id="62e07-142">Väljale **Intervallid (sekundid)** sisestage **255**.</span><span class="sxs-lookup"><span data-stu-id="62e07-142">In the **Intervals (seconds)** field, enter **255**.</span></span>
1. <span data-ttu-id="62e07-143">Suvandis **Koormusetasandus** säilitage vaikeväärtused.</span><span class="sxs-lookup"><span data-stu-id="62e07-143">Under **Load balancing**, leave the default values.</span></span>

<span data-ttu-id="62e07-144">Järgmisel illustratsioonil on näha Azure’i sisenemispunkti teenuse dialoogiaken **Lisa lõppserveri kaust**.</span><span class="sxs-lookup"><span data-stu-id="62e07-144">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service.</span></span>

![Tagaserveri dialoogiakna lisamine](./media/CDN_BackendPool.png)

### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="62e07-146">Azure’i sisenemispunkti teenuse reeglite seadistamine</span><span class="sxs-lookup"><span data-stu-id="62e07-146">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="62e07-147">Azure’i sisenemispunkti teenuse marsruudivaliku reegli seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="62e07-147">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="62e07-148">Lisage marsruudivaliku reegel.</span><span class="sxs-lookup"><span data-stu-id="62e07-148">Add a routing rule.</span></span>
1. <span data-ttu-id="62e07-149">Väljale **Nimi** sisestage suvand **vaikimisi**.</span><span class="sxs-lookup"><span data-stu-id="62e07-149">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="62e07-150">Väljal **Kinnitatud protokoll** valige **HTTP ja HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="62e07-150">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="62e07-151">Väljal **Eesserveri hostid** sisestage **dynamics-ecom-rentnik-nimi.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="62e07-151">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="62e07-152">Jaotises **Vastendamise mustrid** sisestage ülemisele väljale **/\***.</span><span class="sxs-lookup"><span data-stu-id="62e07-152">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="62e07-153">Jaotises **Marsruudi üksikasjad** määrake suvandi **Marsruudi tüüp** väärtuseks **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="62e07-153">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="62e07-154">Väljal **Tagaserveri kaust** valige **ecom-tagaserver**.</span><span class="sxs-lookup"><span data-stu-id="62e07-154">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="62e07-155">Valige väljagrupis **Edasisaatmise protokoll** suvand **Taotlusele vastendamine**.</span><span class="sxs-lookup"><span data-stu-id="62e07-155">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="62e07-156">Määrake suvand **URL-i ümberkirjutamine** väärtusele **Keelatud**.</span><span class="sxs-lookup"><span data-stu-id="62e07-156">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="62e07-157">Määrake suvand **Vahemällu salvestamine** väärtusele **Keelatud**.</span><span class="sxs-lookup"><span data-stu-id="62e07-157">Set the **Caching** option to **Disabled**.</span></span>

<span data-ttu-id="62e07-158">Azure’i sisenemispunkti teenuse vahemällu salvestamise reegli seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="62e07-158">To set up a caching rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="62e07-159">Lisage vahemällu salvestamise reegel.</span><span class="sxs-lookup"><span data-stu-id="62e07-159">Add a caching rule.</span></span>
1. <span data-ttu-id="62e07-160">Väljale **Nimi** sisestage suvand **staatika**.</span><span class="sxs-lookup"><span data-stu-id="62e07-160">In the **Name** field, enter **statics**.</span></span>
1. <span data-ttu-id="62e07-161">Väljal **Kinnitatud protokoll** valige **HTTP ja HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="62e07-161">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="62e07-162">Väljal **Eesserveri hostid** sisestage **dynamics-ecom-rentnik-nimi.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="62e07-162">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="62e07-163">Jaotises **Vastendamise mustrid** sisestage ülemisele väljale **/\_msdyn365/\_scnr/\***.</span><span class="sxs-lookup"><span data-stu-id="62e07-163">Under **Patterns to match**, in the upper field, **/\_msdyn365/\_scnr/\***.</span></span>
1. <span data-ttu-id="62e07-164">Jaotises **Marsruudi üksikasjad** määrake suvandi **Marsruudi tüüp** väärtuseks **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="62e07-164">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="62e07-165">Väljal **Tagaserveri kaust** valige **ecom-tagaserver**.</span><span class="sxs-lookup"><span data-stu-id="62e07-165">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="62e07-166">Valige väljagrupis **Edasisaatmise protokoll** suvand **Taotlusele vastendamine**.</span><span class="sxs-lookup"><span data-stu-id="62e07-166">In the **Forwarding protocol** field group, select the **Match request** option.</span></span>
1. <span data-ttu-id="62e07-167">Määrake suvand **URL-i ümberkirjutamine** väärtusele **Keelatud**.</span><span class="sxs-lookup"><span data-stu-id="62e07-167">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="62e07-168">Määrake suvand **Vahemällu salvestamine** väärtusele **Keelatud**.</span><span class="sxs-lookup"><span data-stu-id="62e07-168">Set the **Caching** option to **Disabled**.</span></span>
1. <span data-ttu-id="62e07-169">Väljal **Päringustringi vahemällu salvestamise käitumine** valige suvand **Salvesta vahemällu kõik ainulaadsed URL-id**.</span><span class="sxs-lookup"><span data-stu-id="62e07-169">In the **Query string caching behavior** field, select **Cache every unique URL**.</span></span>
1. <span data-ttu-id="62e07-170">Väljagrupis **Dünaamiline tihendamine** valige suvand **Luba**.</span><span class="sxs-lookup"><span data-stu-id="62e07-170">In the **Dynamic compression** field group, select the **Enabled** option.</span></span>

<span data-ttu-id="62e07-171">Järgmisel illustratsioonil on näha Azure’i sisenemispunkti teenuse dialoogiaken **Lisa reegel**.</span><span class="sxs-lookup"><span data-stu-id="62e07-171">The following illustration shows the **Add a rule** dialog box in Azure Front Door Service.</span></span>

![Reegli dialoogiakna lisamine](./media/CDN_CachingRule.png)

<span data-ttu-id="62e07-173">Pärast selle algse konfiguratsiooni juurutamist peate lisama Azure’i sisenemispunkti teenuse konfiguratsioonile oma kohandatud domeeni.</span><span class="sxs-lookup"><span data-stu-id="62e07-173">After this initial configuration is deployed, you must add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="62e07-174">Kohandatud domeeni lisamiseks (nt `www.fabrikam.com`) peate konfigureerima domeeni kanoonilise nime (CNAME).</span><span class="sxs-lookup"><span data-stu-id="62e07-174">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="62e07-175">Järgmisel illustratsioonil on näha Azure’i sisenemispunkti teenuse dialoogiaken **Konfiguratsioon CNAME**.</span><span class="sxs-lookup"><span data-stu-id="62e07-175">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![Dialoogiaken Konfiguratsioon CNAME](./media/CNAME_Configuration.png)

> [!NOTE]
> <span data-ttu-id="62e07-177">Kui domeen, mida kasutate, on juba aktiivne ja avaldatud, võtke ühendust toega, et lubada see domeen Azure’i sisenemispunkti teenusega testi seadistamiseks.</span><span class="sxs-lookup"><span data-stu-id="62e07-177">If the domain that you will use is already active and live, contact support to enable this domain with Azure Front Door Service to set up a test.</span></span>

<span data-ttu-id="62e07-178">Saate kasutada Azure’i sisenemispunkti teenust serdi haldamiseks või saate kasutada oma kohandatud domeeni serti.</span><span class="sxs-lookup"><span data-stu-id="62e07-178">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="62e07-179">Järgmisel illustratsioonil on näha Azure’i sisenemispunkti teenuse dialoogiaken **Kohandatud domeeni HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="62e07-179">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![Dialoogiaken Kohandatud domeeni HTTPS](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="62e07-181">Teie CDN peaks nüüd olema õigesti konfigureeritud, et seda saaks teie Commerce’i saidiga kasutada.</span><span class="sxs-lookup"><span data-stu-id="62e07-181">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="62e07-182">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="62e07-182">Additional resources</span></span>

[<span data-ttu-id="62e07-183">Domeeninime konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="62e07-183">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="62e07-184">Uue e-kaubanduse saidi juurutamine</span><span class="sxs-lookup"><span data-stu-id="62e07-184">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="62e07-185">E-kaubanduse saidi loomine</span><span class="sxs-lookup"><span data-stu-id="62e07-185">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="62e07-186">Veebisaidi seostamine kanaliga</span><span class="sxs-lookup"><span data-stu-id="62e07-186">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="62e07-187">robots.txt-failide haldamine</span><span class="sxs-lookup"><span data-stu-id="62e07-187">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="62e07-188">Kasutaja sisselogimiseks kohandatud lehtede seadistamine</span><span class="sxs-lookup"><span data-stu-id="62e07-188">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="62e07-189">Asukohapõhise poetuvastuse lubamine</span><span class="sxs-lookup"><span data-stu-id="62e07-189">Enable location-based store detection</span></span>](enable-store-detection.md)