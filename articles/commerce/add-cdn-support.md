---
title: Sisuedastusvõrgu (CDN) toe lisamine
description: See teema kirjeldab, kuidas lisada oma Microsoft Dynamics 365 Commerce keskkonnale sisuedastusvõrk (CDN).
author: brianshook
manager: annbe
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: d653b072eca134c765a5db5659b228648fc13c4a
ms.sourcegitcommit: 3fe4d9a33447aa8a62d704fbbf18aeb9cb667baa
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/12/2021
ms.locfileid: "5582715"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="0601c-103">Sisu edastamise võrgu (CDN) toe lisamine</span><span class="sxs-lookup"><span data-stu-id="0601c-103">Add support for a content delivery network (CDN)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="0601c-104">See teema kirjeldab, kuidas lisada oma Microsoft Dynamics 365 Commerce keskkonnale sisuedastusvõrk (CDN).</span><span class="sxs-lookup"><span data-stu-id="0601c-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="0601c-105">Kui seadistate e-kaubanduse keskkonda rakenduses Dynamics 365 Commerce, siis saate konfigureerida selle töötama koos oma CDN-i teenusega.</span><span class="sxs-lookup"><span data-stu-id="0601c-105">When you set up an e-commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="0601c-106">Teie kohandatud domeeni saab lubada e-kaubanduse keskkonna ettevalmistamisprotsessi käigus.</span><span class="sxs-lookup"><span data-stu-id="0601c-106">Your custom domain can be enabled during the provisioning process for your e-commerce environment.</span></span> <span data-ttu-id="0601c-107">Teise võimalusena saate kasutada teenusetaotlust, et seadistada see pärast ettevalmistusprotsessi lõpetamist.</span><span class="sxs-lookup"><span data-stu-id="0601c-107">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="0601c-108">E-kaubanduse keskkonna ettevalmistamisprotsess loob keskkonnaga seotud hostinime.</span><span class="sxs-lookup"><span data-stu-id="0601c-108">The provisioning process for the e-commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="0601c-109">Sellel hostinimel on järgmine vorming, kus \<*e-commerce-tenant-name*\> on teie keskkonna nimi.</span><span class="sxs-lookup"><span data-stu-id="0601c-109">This host name has the following format, where \<*e-commerce-tenant-name*\> is the name of your environment:</span></span>

<span data-ttu-id="0601c-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="0601c-110">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="0601c-111">Ettevalmistusprotsessi käigus loodud hostinimi või lõpp-punkt toetab turvasoklite kihi (SSL) serti ainult \*.commerce.dynamics.com-i jaoks.</span><span class="sxs-lookup"><span data-stu-id="0601c-111">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="0601c-112">See ei toeta kohandatud domeenide SSL-i.</span><span class="sxs-lookup"><span data-stu-id="0601c-112">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="0601c-113">Seega peate kohandatud domeenide SSL-i määrama oma CDN-is ja edastama liikluse CDN-ist kaubanduse loodud hostinimele või lõpp-punktile.</span><span class="sxs-lookup"><span data-stu-id="0601c-113">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="0601c-114">Lisaks teenindatakse lõpp-punktist Commerce’i *staatika* (JavaScripti või kaskaadlaadistiku \[CSS\] faile), mille Commerce genereeris (\*.commerce.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="0601c-114">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="0601c-115">Staatika saab vahemällu salvestada ainult siis, kui Commerce’i genereeritud hostinimi või lõpp-punkt lisatakse on CDN-i taha.</span><span class="sxs-lookup"><span data-stu-id="0601c-115">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="0601c-116">SSL-i seadistamine</span><span class="sxs-lookup"><span data-stu-id="0601c-116">Set up SSL</span></span>

<span data-ttu-id="0601c-117">SSL-i seadistamise ja staatika vahemällu salvestamise tagamiseks peate konfigureerima oma CDN-i nii, et see on seostatud teie keskkonna jaoks loodud Commerce’i nimega.</span><span class="sxs-lookup"><span data-stu-id="0601c-117">To help guarantee that SSL is set up, and that statics are cached, you must configure your CDN so that it is associated with the host name that Commerce generated for your environment.</span></span> <span data-ttu-id="0601c-118">Staatika jaoks peate salvestama vahemällu ka järgmise mustri:</span><span class="sxs-lookup"><span data-stu-id="0601c-118">You must also cache the following pattern for statics only:</span></span> 

<span data-ttu-id="0601c-119">/\_msdyn365/\_scnr/\*</span><span class="sxs-lookup"><span data-stu-id="0601c-119">/\_msdyn365/\_scnr/\*</span></span>

<span data-ttu-id="0601c-120">Pärast antud kohandatud domeeniga Commerce’i keskkonna ettevalmistamist või pärast oma keskkonnale teenusetaotlust kasutades kohandatud domeeni sisestamist, suunake oma kohandatud domeen Commerce’i loodud hostinimele või lõpp-punktile.</span><span class="sxs-lookup"><span data-stu-id="0601c-120">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, point your custom domain to the host name or endpoint that Commerce generated.</span></span>

<span data-ttu-id="0601c-121">Nagu eelnevalt mainitud, toetab loodud hostinimi või lõpp-punkt SSL-i serti ainult \*.commerce.dynamics.com-i jaoks.</span><span class="sxs-lookup"><span data-stu-id="0601c-121">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="0601c-122">See ei toeta kohandatud domeenide SSL-i.</span><span class="sxs-lookup"><span data-stu-id="0601c-122">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="0601c-123">CDN-teenused</span><span class="sxs-lookup"><span data-stu-id="0601c-123">CDN services</span></span>

<span data-ttu-id="0601c-124">Commerce’i keskkonnaga saab kasutada mis tahes CDN-i teenust.</span><span class="sxs-lookup"><span data-stu-id="0601c-124">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="0601c-125">Järgmisena on toodud kaks näidet.</span><span class="sxs-lookup"><span data-stu-id="0601c-125">Here are two examples:</span></span>

- <span data-ttu-id="0601c-126">**Microsoft Azure’i sisenemispunkti teenus** – Azure’i CDN-i lahendus.</span><span class="sxs-lookup"><span data-stu-id="0601c-126">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="0601c-127">Lisateavet Azure’i sisenemispunkti teenuse kohta vt [Azure’i sisenemispunkti teenuse dokumentatsioon](https://docs.microsoft.com/azure/frontdoor/).</span><span class="sxs-lookup"><span data-stu-id="0601c-127">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="0601c-128">**Akamai dünaamiline saidi kiirendi** – lisateavet vaadake teemast [Dünaamiline saidi kiirendi](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span><span class="sxs-lookup"><span data-stu-id="0601c-128">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="0601c-129">CDN häälestus</span><span class="sxs-lookup"><span data-stu-id="0601c-129">CDN setup</span></span>

<span data-ttu-id="0601c-130">CDN-i seadistamise protsess koosneb järgnevatest üldistest etappidest.</span><span class="sxs-lookup"><span data-stu-id="0601c-130">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="0601c-131">Lisage eesserveri host.</span><span class="sxs-lookup"><span data-stu-id="0601c-131">Add a front-end host.</span></span>
1. <span data-ttu-id="0601c-132">Konfigureerige tagaserverite kaust.</span><span class="sxs-lookup"><span data-stu-id="0601c-132">Configure a backend pool.</span></span>
1. <span data-ttu-id="0601c-133">Seadistage marsruudivalik ja vahemällu salvestamine.</span><span class="sxs-lookup"><span data-stu-id="0601c-133">Set up rules for routing and caching.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="0601c-134">Eesserveri hosti lisamine</span><span class="sxs-lookup"><span data-stu-id="0601c-134">Add a front-end host</span></span>

<span data-ttu-id="0601c-135">Kasutada võib mis tahes CDN-i teenust, kuid näiteks selles teemas kasutatakse Azure’i sisenemispunkti teenust.</span><span class="sxs-lookup"><span data-stu-id="0601c-135">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="0601c-136">Teavet Azure’i sisenemispunkti teenuse seadistamise kohta vaadake teemast [Lühijuhend: suure saadavusega globaalse veebirakenduse jaoks sisenemispunkti loomine](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span><span class="sxs-lookup"><span data-stu-id="0601c-136">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a><span data-ttu-id="0601c-137">Azure’i sisenemispunkti teenuses tagaserverite kausta konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="0601c-137">Configure a backend pool in Azure Front Door Service</span></span>

<span data-ttu-id="0601c-138">Azure’i sisenemispunkti teenuses tagaserverite kausta konfigureerimiseks järgige järgmisi etappe.</span><span class="sxs-lookup"><span data-stu-id="0601c-138">To configure a backend pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="0601c-139">Lisage tagaserverite kaustale kohandatud hostiks **&lt;ecom-tenant-name&gt;.commerce.dynamics.com**, millel on tühi tagaserveri hosti päis.</span><span class="sxs-lookup"><span data-stu-id="0601c-139">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a backend pool as a custom host that has an empty backend host header.</span></span>
1. <span data-ttu-id="0601c-140">Suvandis **Koormusetasandus** säilitage vaikeväärtused.</span><span class="sxs-lookup"><span data-stu-id="0601c-140">Under **Load balancing**, leave the default values.</span></span>

<span data-ttu-id="0601c-141">Järgmisel illustratsioonil on näha Azure’i sisenemispunkti teenuse dialoogiboks **Lisa tagaserver**, millesse on sisestatud tagaserveri hosti nimi.</span><span class="sxs-lookup"><span data-stu-id="0601c-141">The following illustration shows the **Add a backend** dialog box in Azure Front Door Service with the backend host name entered.</span></span>

![Tagaserveri dialoogiakna lisamine](./media/CDN_BackendPool.png)

<span data-ttu-id="0601c-143">Järgmisel illustratsioonil on näha Azure’i sisenemispunkti teenuse dialoogiboks **Lisa tagaserverite kaust** koos koormuse tasakaalustamise vaikeväärtustega.</span><span class="sxs-lookup"><span data-stu-id="0601c-143">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service with the default load balancing values.</span></span>

![Jätkuv tagaserveri dialoogiboksi lisamine](./media/CDN_BackendPool_2.png)

### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="0601c-145">Azure’i sisenemispunkti teenuse reeglite seadistamine</span><span class="sxs-lookup"><span data-stu-id="0601c-145">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="0601c-146">Azure’i sisenemispunkti teenuse marsruudivaliku reegli seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="0601c-146">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="0601c-147">Lisage marsruudivaliku reegel.</span><span class="sxs-lookup"><span data-stu-id="0601c-147">Add a routing rule.</span></span>
1. <span data-ttu-id="0601c-148">Väljale **Nimi** sisestage suvand **vaikimisi**.</span><span class="sxs-lookup"><span data-stu-id="0601c-148">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="0601c-149">Väljal **Kinnitatud protokoll** valige **HTTP ja HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="0601c-149">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="0601c-150">Väljal **Eesserveri hostid** sisestage **dynamics-ecom-rentnik-nimi.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="0601c-150">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="0601c-151">Jaotises **Vastendamise mustrid** sisestage ülemisele väljale **/\***.</span><span class="sxs-lookup"><span data-stu-id="0601c-151">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="0601c-152">Jaotises **Marsruudi üksikasjad** määrake suvandi **Marsruudi tüüp** väärtuseks **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="0601c-152">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="0601c-153">Väljal **Tagaserveri kaust** valige **ecom-tagaserver**.</span><span class="sxs-lookup"><span data-stu-id="0601c-153">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="0601c-154">Valige väljagrupis **Edasisaatmise protokoll** suvand **Taotlusele vastendamine**.</span><span class="sxs-lookup"><span data-stu-id="0601c-154">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="0601c-155">Määrake suvand **URL-i ümberkirjutamine** väärtusele **Keelatud**.</span><span class="sxs-lookup"><span data-stu-id="0601c-155">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="0601c-156">Määrake suvand **Vahemällu salvestamine** väärtusele **Keelatud**.</span><span class="sxs-lookup"><span data-stu-id="0601c-156">Set the **Caching** option to **Disabled**.</span></span>

<span data-ttu-id="0601c-157">Azure’i sisenemispunkti teenuse vahemällu salvestamise reegli seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="0601c-157">To set up a caching rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="0601c-158">Lisage vahemällu salvestamise reegel.</span><span class="sxs-lookup"><span data-stu-id="0601c-158">Add a caching rule.</span></span>
1. <span data-ttu-id="0601c-159">Väljale **Nimi** sisestage suvand **staatika**.</span><span class="sxs-lookup"><span data-stu-id="0601c-159">In the **Name** field, enter **statics**.</span></span>
1. <span data-ttu-id="0601c-160">Väljal **Kinnitatud protokoll** valige **HTTP ja HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="0601c-160">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="0601c-161">Väljal **Eesserveri hostid** sisestage **dynamics-ecom-rentnik-nimi.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="0601c-161">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="0601c-162">Jaotises **Vastendamise mustrid** sisestage ülemisele väljale **/\_msdyn365/\_scnr/\***.</span><span class="sxs-lookup"><span data-stu-id="0601c-162">Under **Patterns to match**, in the upper field, **/\_msdyn365/\_scnr/\***.</span></span>
1. <span data-ttu-id="0601c-163">Jaotises **Marsruudi üksikasjad** määrake suvandi **Marsruudi tüüp** väärtuseks **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="0601c-163">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="0601c-164">Väljal **Tagaserveri kaust** valige **ecom-tagaserver**.</span><span class="sxs-lookup"><span data-stu-id="0601c-164">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="0601c-165">Valige väljagrupis **Edasisaatmise protokoll** suvand **Taotlusele vastendamine**.</span><span class="sxs-lookup"><span data-stu-id="0601c-165">In the **Forwarding protocol** field group, select the **Match request** option.</span></span>
1. <span data-ttu-id="0601c-166">Määrake suvand **URL-i ümberkirjutamine** väärtusele **Keelatud**.</span><span class="sxs-lookup"><span data-stu-id="0601c-166">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="0601c-167">Määrake suvand **Vahemällu salvestamine** väärtusele **Keelatud**.</span><span class="sxs-lookup"><span data-stu-id="0601c-167">Set the **Caching** option to **Disabled**.</span></span>
1. <span data-ttu-id="0601c-168">Väljal **Päringustringi vahemällu salvestamise käitumine** valige suvand **Salvesta vahemällu kõik ainulaadsed URL-id**.</span><span class="sxs-lookup"><span data-stu-id="0601c-168">In the **Query string caching behavior** field, select **Cache every unique URL**.</span></span>
1. <span data-ttu-id="0601c-169">Väljagrupis **Dünaamiline tihendamine** valige suvand **Luba**.</span><span class="sxs-lookup"><span data-stu-id="0601c-169">In the **Dynamic compression** field group, select the **Enabled** option.</span></span>

<span data-ttu-id="0601c-170">Järgmisel illustratsioonil on näha Azure’i sisenemispunkti teenuse dialoogiaken **Lisa reegel**.</span><span class="sxs-lookup"><span data-stu-id="0601c-170">The following illustration shows the **Add a rule** dialog box in Azure Front Door Service.</span></span>

![Reegli dialoogiakna lisamine](./media/CDN_CachingRule.png)

> [!WARNING]
> <span data-ttu-id="0601c-172">Kui domeen, mida te kasutama hakkate, on juba aktiivne ja kasutusvalmis, looge teenuse [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) paanil **Tugi** tugiteenusepilet, et saada järgmiste sammude jaoks abi.</span><span class="sxs-lookup"><span data-stu-id="0601c-172">If the domain that you will use is already active and live, create a support ticket from the **Support** tile in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) to get assistance for your next steps.</span></span> <span data-ttu-id="0601c-173">Lisateavet leiate teemast [Finance and Operationsi rakenduste või teenuse Lifecycle Services (LCS) tugi](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="0601c-173">For more information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

<span data-ttu-id="0601c-174">Kui teie domeen on uus ja ei ole olemasolev kasutatav domeen, saate lisada oma kohandatud domeeni Azure'i sisenemispunkti teenuse konfiguratsiooni.</span><span class="sxs-lookup"><span data-stu-id="0601c-174">If your domain is new and is not a pre-existing live domain, you can add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="0601c-175">See võimaldab suunata veebiliiklust teie saidile Azure'i sisenemispunkti teenuse kaudu.</span><span class="sxs-lookup"><span data-stu-id="0601c-175">This will enable web traffic to direct to your site via the Azure Front Door instance.</span></span> <span data-ttu-id="0601c-176">Kohandatud domeeni lisamiseks (nt `www.fabrikam.com`) peate konfigureerima domeeni kanoonilise nime (CNAME).</span><span class="sxs-lookup"><span data-stu-id="0601c-176">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="0601c-177">Järgmisel illustratsioonil on näha Azure’i sisenemispunkti teenuse dialoogiaken **Konfiguratsioon CNAME**.</span><span class="sxs-lookup"><span data-stu-id="0601c-177">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![Dialoogiaken Konfiguratsioon CNAME](./media/CNAME_Configuration.png)

<span data-ttu-id="0601c-179">Saate kasutada Azure’i sisenemispunkti teenust serdi haldamiseks või saate kasutada oma kohandatud domeeni serti.</span><span class="sxs-lookup"><span data-stu-id="0601c-179">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="0601c-180">Järgmisel illustratsioonil on näha Azure’i sisenemispunkti teenuse dialoogiaken **Kohandatud domeeni HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="0601c-180">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![Dialoogiaken Kohandatud domeeni HTTPS](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="0601c-182">Üksikasjalikku teavet kohandatud domeeni lisamise kohta oma Azure'i sisenemispunkti leiate teemast [Kohandatud domeeni lisamine sisenemispunkti](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span><span class="sxs-lookup"><span data-stu-id="0601c-182">For detailed instructions on adding a custom domain to your Azure Front Door, see [Add a custom domain to your Front Door](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span></span>

<span data-ttu-id="0601c-183">Teie CDN peaks nüüd olema õigesti konfigureeritud, et seda saaks teie Commerce’i saidiga kasutada.</span><span class="sxs-lookup"><span data-stu-id="0601c-183">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0601c-184">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="0601c-184">Additional resources</span></span>

[<span data-ttu-id="0601c-185">Sisu tarne võrgu rakendamise suvandid</span><span class="sxs-lookup"><span data-stu-id="0601c-185">Content delivery network implementation options</span></span>](cdn-options.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
