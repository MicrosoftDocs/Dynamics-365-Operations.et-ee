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
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 662d26c0157377977bd1031cd7bb13a8e692f37e
ms.sourcegitcommit: 078befcd7f3531073ab2c08b365bcf132d6477b0
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/31/2020
ms.locfileid: "3646035"
---
# <a name="add-support-for-a-content-delivery-network-cdn"></a><span data-ttu-id="37527-103">Sisuedastusvõrgu (CDN) toe lisamine</span><span class="sxs-lookup"><span data-stu-id="37527-103">Add support for a content delivery network (CDN)</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="37527-104">See teema kirjeldab, kuidas lisada oma Microsoft Dynamics 365 Commerce keskkonnale sisuedastusvõrk (CDN).</span><span class="sxs-lookup"><span data-stu-id="37527-104">This topic describes how to add a content delivery network (CDN) to your Microsoft Dynamics 365 Commerce environment.</span></span>

## <a name="overview"></a><span data-ttu-id="37527-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="37527-105">Overview</span></span>

<span data-ttu-id="37527-106">Rakenduses Dynamics 365 Commerce e-kaubanduse keskkonda seadistades saate konfigureerida selle töötama koos oma CDN-i teenusega.</span><span class="sxs-lookup"><span data-stu-id="37527-106">When you set up an e-Commerce environment in Dynamics 365 Commerce, you can configure it to work with your CDN service.</span></span> 

<span data-ttu-id="37527-107">Teie kohandatud domeeni saab lubada e-kaubanduse keskkonna ettevalmistamisprotsessi käigus.</span><span class="sxs-lookup"><span data-stu-id="37527-107">Your custom domain can be enabled during the provisioning process for your e-Commerce environment.</span></span> <span data-ttu-id="37527-108">Teise võimalusena saate kasutada teenusetaotlust, et seadistada see pärast ettevalmistusprotsessi lõpetamist.</span><span class="sxs-lookup"><span data-stu-id="37527-108">Alternatively, you can use a service request to set it up after the provisioning process is completed.</span></span> <span data-ttu-id="37527-109">E-kaubanduse keskkonna ettevalmistamisprotsess loob hostinime, mis on keskkonnaga seotud.</span><span class="sxs-lookup"><span data-stu-id="37527-109">The provisioning process for the e-Commerce environment generates a host name that is associated with the environment.</span></span> <span data-ttu-id="37527-110">Sellel hostinimel on järgmine vorming, kus \<*e-commerce-tenant-name*\> on teie keskkonna nimi.</span><span class="sxs-lookup"><span data-stu-id="37527-110">This host name has the following format, where \<*e-commerce-tenant-name*\> is the name of your environment:</span></span>

<span data-ttu-id="37527-111">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span><span class="sxs-lookup"><span data-stu-id="37527-111">&lt;e-commerce-tenant-name&gt;.commerce.dynamics.com</span></span>

<span data-ttu-id="37527-112">Ettevalmistusprotsessi käigus loodud hostinimi või lõpp-punkt toetab turvasoklite kihi (SSL) serti ainult \*.commerce.dynamics.com-i jaoks.</span><span class="sxs-lookup"><span data-stu-id="37527-112">The host name or endpoint that is generated during the provisioning process supports a Secure Sockets Layer (SSL) certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="37527-113">See ei toeta kohandatud domeenide SSL-i.</span><span class="sxs-lookup"><span data-stu-id="37527-113">It doesn't support SSL for custom domains.</span></span> <span data-ttu-id="37527-114">Seega peate kohandatud domeenide SSL-i määrama oma CDN-is ja edastama liikluse CDN-ist kaubanduse loodud hostinimele või lõpp-punktile.</span><span class="sxs-lookup"><span data-stu-id="37527-114">Therefore, you must terminate SSL for custom domains in your CDN and forward traffic from the CDN to the host name or endpoint that Commerce generated.</span></span> 

<span data-ttu-id="37527-115">Lisaks teenindatakse lõpp-punktist Commerce’i *staatika* (JavaScripti või kaskaadlaadistiku \[CSS\] faile), mille Commerce genereeris (\*.commerce.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="37527-115">Additionally, the *statics* (JavaScript or Cascading Style Sheets \[CSS\] files) from Commerce are served from the endpoint that Commerce generated (\*.commerce.dynamics.com).</span></span> <span data-ttu-id="37527-116">Staatika saab vahemällu salvestada ainult siis, kui Commerce’i genereeritud hostinimi või lõpp-punkt lisatakse on CDN-i taha.</span><span class="sxs-lookup"><span data-stu-id="37527-116">The statics can be cached only if the host name or endpoint that Commerce generated is put behind the CDN.</span></span>

## <a name="set-up-ssl"></a><span data-ttu-id="37527-117">SSL-i seadistamine</span><span class="sxs-lookup"><span data-stu-id="37527-117">Set up SSL</span></span>

<span data-ttu-id="37527-118">SSL-i seadistamise ja staatika vahemällu salvestamise tagamiseks peate konfigureerima oma CDN-i nii, et see on seostatud teie keskkonna jaoks loodud Commerce’i nimega.</span><span class="sxs-lookup"><span data-stu-id="37527-118">To help guarantee that SSL is set up, and that statics are cached, you must configure your CDN so that it is associated with the host name that Commerce generated for your environment.</span></span> <span data-ttu-id="37527-119">Staatika jaoks peate salvestama vahemällu ka järgmise mustri:</span><span class="sxs-lookup"><span data-stu-id="37527-119">You must also cache the following pattern for statics only:</span></span> 

<span data-ttu-id="37527-120">/\_msdyn365/\_scnr/\*</span><span class="sxs-lookup"><span data-stu-id="37527-120">/\_msdyn365/\_scnr/\*</span></span>

<span data-ttu-id="37527-121">Pärast antud kohandatud domeeniga Commerce’i keskkonna ettevalmistamist või pärast oma keskkonnale teenusetaotlust kasutades kohandatud domeeni sisestamist, suunake oma kohandatud domeen Commerce’i loodud hostinimele või lõpp-punktile.</span><span class="sxs-lookup"><span data-stu-id="37527-121">After you provision your Commerce environment with the custom domain that is provided, or after you provide the custom domain for your environment by using a service request, point your custom domain to the host name or endpoint that Commerce generated.</span></span>

<span data-ttu-id="37527-122">Nagu eelnevalt mainitud, toetab loodud hostinimi või lõpp-punkt SSL-i serti ainult \*.commerce.dynamics.com-i jaoks.</span><span class="sxs-lookup"><span data-stu-id="37527-122">As was previously mentioned, the generated host name or endpoint supports an SSL certificate only for \*.commerce.dynamics.com.</span></span> <span data-ttu-id="37527-123">See ei toeta kohandatud domeenide SSL-i.</span><span class="sxs-lookup"><span data-stu-id="37527-123">It doesn't support SSL for custom domains.</span></span>

## <a name="cdn-services"></a><span data-ttu-id="37527-124">CDN-teenused</span><span class="sxs-lookup"><span data-stu-id="37527-124">CDN services</span></span>

<span data-ttu-id="37527-125">Commerce’i keskkonnaga saab kasutada mis tahes CDN-i teenust.</span><span class="sxs-lookup"><span data-stu-id="37527-125">Any CDN service can be used with a Commerce environment.</span></span> <span data-ttu-id="37527-126">Järgmisena on toodud kaks näidet.</span><span class="sxs-lookup"><span data-stu-id="37527-126">Here are two examples:</span></span>

- <span data-ttu-id="37527-127">**Microsoft Azure’i sisenemispunkti teenus** – Azure’i CDN-i lahendus.</span><span class="sxs-lookup"><span data-stu-id="37527-127">**Microsoft Azure Front Door Service** – The Azure CDN solution.</span></span> <span data-ttu-id="37527-128">Lisateavet Azure’i sisenemispunkti teenuse kohta vt [Azure’i sisenemispunkti teenuse dokumentatsioon](https://docs.microsoft.com/azure/frontdoor/).</span><span class="sxs-lookup"><span data-stu-id="37527-128">For more information about Azure Front Door Service, see [Azure Front Door Service Documentation](https://docs.microsoft.com/azure/frontdoor/).</span></span>
- <span data-ttu-id="37527-129">**Akamai dünaamiline saidi kiirendi** – lisateavet vaadake teemast [Dünaamiline saidi kiirendi](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span><span class="sxs-lookup"><span data-stu-id="37527-129">**Akamai Dynamic Site Accelerator** – For more information, see [Dynamic Site Accelerator](https://www.akamai.com/us/en/products/performance/dynamic-site-accelerator.jsp).</span></span>

## <a name="cdn-setup"></a><span data-ttu-id="37527-130">CDN häälestus</span><span class="sxs-lookup"><span data-stu-id="37527-130">CDN setup</span></span>

<span data-ttu-id="37527-131">CDN-i seadistamise protsess koosneb järgnevatest üldistest etappidest.</span><span class="sxs-lookup"><span data-stu-id="37527-131">The CDN setup process consists of these general steps:</span></span>

1. <span data-ttu-id="37527-132">Lisage eesserveri host.</span><span class="sxs-lookup"><span data-stu-id="37527-132">Add a front-end host.</span></span>
1. <span data-ttu-id="37527-133">Konfigureerige tagaserverite kaust.</span><span class="sxs-lookup"><span data-stu-id="37527-133">Configure a backend pool.</span></span>
1. <span data-ttu-id="37527-134">Seadistage marsruudivalik ja vahemällu salvestamine.</span><span class="sxs-lookup"><span data-stu-id="37527-134">Set up rules for routing and caching.</span></span>

### <a name="add-a-front-end-host"></a><span data-ttu-id="37527-135">Eesserveri hosti lisamine</span><span class="sxs-lookup"><span data-stu-id="37527-135">Add a front-end host</span></span>

<span data-ttu-id="37527-136">Kasutada võib mis tahes CDN-i teenust, kuid näiteks selles teemas kasutatakse Azure’i sisenemispunkti teenust.</span><span class="sxs-lookup"><span data-stu-id="37527-136">Any CDN service can be used, but for the example in this topic, Azure Front Door Service is used.</span></span> 

<span data-ttu-id="37527-137">Teavet Azure’i sisenemispunkti teenuse seadistamise kohta vaadake teemast [Lühijuhend: suure saadavusega globaalse veebirakenduse jaoks sisenemispunkti loomine](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span><span class="sxs-lookup"><span data-stu-id="37527-137">For information about how to set up Azure Front Door Service, see [Quickstart: Create a Front Door for a highly available global web application](https://docs.microsoft.com/azure/frontdoor/quickstart-create-front-door).</span></span>

### <a name="configure-a-backend-pool-in-azure-front-door-service"></a><span data-ttu-id="37527-138">Azure’i sisenemispunkti teenuses tagaserverite kausta konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="37527-138">Configure a backend pool in Azure Front Door Service</span></span>

<span data-ttu-id="37527-139">Azure’i sisenemispunkti teenuses tagaserverite kausta konfigureerimiseks järgige järgmisi etappe.</span><span class="sxs-lookup"><span data-stu-id="37527-139">To configure a backend pool in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="37527-140">Lisage tagaserverite kaustale kohandatud hostiks **&lt;ecom-tenant-name&gt;.commerce.dynamics.com**, millel on tühi tagaserveri hosti päis.</span><span class="sxs-lookup"><span data-stu-id="37527-140">Add **&lt;ecom-tenant-name&gt;.commerce.dynamics.com** to a backend pool as a custom host that has an empty backend host header.</span></span>
1. <span data-ttu-id="37527-141">Suvandis **Koormusetasandus** säilitage vaikeväärtused.</span><span class="sxs-lookup"><span data-stu-id="37527-141">Under **Load balancing**, leave the default values.</span></span>

<span data-ttu-id="37527-142">Järgmisel illustratsioonil on näha Azure’i sisenemispunkti teenuse dialoogiboks **Lisa tagaserver**, millesse on sisestatud tagaserveri hosti nimi.</span><span class="sxs-lookup"><span data-stu-id="37527-142">The following illustration shows the **Add a backend** dialog box in Azure Front Door Service with the backend host name entered.</span></span>

![Tagaserveri dialoogiakna lisamine](./media/CDN_BackendPool.png)

<span data-ttu-id="37527-144">Järgmisel illustratsioonil on näha Azure’i sisenemispunkti teenuse dialoogiboks **Lisa tagaserverite kaust** koos koormuse tasakaalustamise vaikeväärtustega.</span><span class="sxs-lookup"><span data-stu-id="37527-144">The following illustration shows the **Add a backend pool** dialog box in Azure Front Door Service with the default load balancing values.</span></span>

![Jätkuv tagaserveri dialoogiboksi lisamine](./media/CDN_BackendPool_2.png)

### <a name="set-up-rules-in-azure-front-door-service"></a><span data-ttu-id="37527-146">Azure’i sisenemispunkti teenuse reeglite seadistamine</span><span class="sxs-lookup"><span data-stu-id="37527-146">Set up rules in Azure Front Door Service</span></span>

<span data-ttu-id="37527-147">Azure’i sisenemispunkti teenuse marsruudivaliku reegli seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="37527-147">To set up a routing rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="37527-148">Lisage marsruudivaliku reegel.</span><span class="sxs-lookup"><span data-stu-id="37527-148">Add a routing rule.</span></span>
1. <span data-ttu-id="37527-149">Väljale **Nimi** sisestage suvand **vaikimisi**.</span><span class="sxs-lookup"><span data-stu-id="37527-149">In the **Name** field, enter **default**.</span></span>
1. <span data-ttu-id="37527-150">Väljal **Kinnitatud protokoll** valige **HTTP ja HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="37527-150">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="37527-151">Väljal **Eesserveri hostid** sisestage **dynamics-ecom-rentnik-nimi.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="37527-151">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="37527-152">Jaotises **Vastendamise mustrid** sisestage ülemisele väljale **/\***.</span><span class="sxs-lookup"><span data-stu-id="37527-152">Under **Patterns to match**, in the upper field, enter **/\***.</span></span>
1. <span data-ttu-id="37527-153">Jaotises **Marsruudi üksikasjad** määrake suvandi **Marsruudi tüüp** väärtuseks **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="37527-153">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="37527-154">Väljal **Tagaserveri kaust** valige **ecom-tagaserver**.</span><span class="sxs-lookup"><span data-stu-id="37527-154">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="37527-155">Valige väljagrupis **Edasisaatmise protokoll** suvand **Taotlusele vastendamine**.</span><span class="sxs-lookup"><span data-stu-id="37527-155">In the **Forwarding protocol** field group, select the **Match request** option.</span></span> 
1. <span data-ttu-id="37527-156">Määrake suvand **URL-i ümberkirjutamine** väärtusele **Keelatud**.</span><span class="sxs-lookup"><span data-stu-id="37527-156">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="37527-157">Määrake suvand **Vahemällu salvestamine** väärtusele **Keelatud**.</span><span class="sxs-lookup"><span data-stu-id="37527-157">Set the **Caching** option to **Disabled**.</span></span>

<span data-ttu-id="37527-158">Azure’i sisenemispunkti teenuse vahemällu salvestamise reegli seadistamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="37527-158">To set up a caching rule in Azure Front Door Service, follow these steps.</span></span>

1. <span data-ttu-id="37527-159">Lisage vahemällu salvestamise reegel.</span><span class="sxs-lookup"><span data-stu-id="37527-159">Add a caching rule.</span></span>
1. <span data-ttu-id="37527-160">Väljale **Nimi** sisestage suvand **staatika**.</span><span class="sxs-lookup"><span data-stu-id="37527-160">In the **Name** field, enter **statics**.</span></span>
1. <span data-ttu-id="37527-161">Väljal **Kinnitatud protokoll** valige **HTTP ja HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="37527-161">In the **Accepted protocol** field, select **HTTP and HTTPS**.</span></span>
1. <span data-ttu-id="37527-162">Väljal **Eesserveri hostid** sisestage **dynamics-ecom-rentnik-nimi.azurefd.net**.</span><span class="sxs-lookup"><span data-stu-id="37527-162">In the **Frontend hosts** field, enter **dynamics-ecom-tenant-name.azurefd.net**.</span></span>
1. <span data-ttu-id="37527-163">Jaotises **Vastendamise mustrid** sisestage ülemisele väljale **/\_msdyn365/\_scnr/\***.</span><span class="sxs-lookup"><span data-stu-id="37527-163">Under **Patterns to match**, in the upper field, **/\_msdyn365/\_scnr/\***.</span></span>
1. <span data-ttu-id="37527-164">Jaotises **Marsruudi üksikasjad** määrake suvandi **Marsruudi tüüp** väärtuseks **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="37527-164">Under **Route Details**, set the **Route type** option to **Forward**.</span></span>
1. <span data-ttu-id="37527-165">Väljal **Tagaserveri kaust** valige **ecom-tagaserver**.</span><span class="sxs-lookup"><span data-stu-id="37527-165">In the **Backend pool** field, select **ecom-backend**.</span></span>
1. <span data-ttu-id="37527-166">Valige väljagrupis **Edasisaatmise protokoll** suvand **Taotlusele vastendamine**.</span><span class="sxs-lookup"><span data-stu-id="37527-166">In the **Forwarding protocol** field group, select the **Match request** option.</span></span>
1. <span data-ttu-id="37527-167">Määrake suvand **URL-i ümberkirjutamine** väärtusele **Keelatud**.</span><span class="sxs-lookup"><span data-stu-id="37527-167">Set the **URL rewrite** option to **Disabled**.</span></span>
1. <span data-ttu-id="37527-168">Määrake suvand **Vahemällu salvestamine** väärtusele **Keelatud**.</span><span class="sxs-lookup"><span data-stu-id="37527-168">Set the **Caching** option to **Disabled**.</span></span>
1. <span data-ttu-id="37527-169">Väljal **Päringustringi vahemällu salvestamise käitumine** valige suvand **Salvesta vahemällu kõik ainulaadsed URL-id**.</span><span class="sxs-lookup"><span data-stu-id="37527-169">In the **Query string caching behavior** field, select **Cache every unique URL**.</span></span>
1. <span data-ttu-id="37527-170">Väljagrupis **Dünaamiline tihendamine** valige suvand **Luba**.</span><span class="sxs-lookup"><span data-stu-id="37527-170">In the **Dynamic compression** field group, select the **Enabled** option.</span></span>

<span data-ttu-id="37527-171">Järgmisel illustratsioonil on näha Azure’i sisenemispunkti teenuse dialoogiaken **Lisa reegel**.</span><span class="sxs-lookup"><span data-stu-id="37527-171">The following illustration shows the **Add a rule** dialog box in Azure Front Door Service.</span></span>

![Reegli dialoogiakna lisamine](./media/CDN_CachingRule.png)

> [!WARNING]
> <span data-ttu-id="37527-173">Kui domeen, mida te kasutama hakkate, on juba aktiivne ja kasutusvalmis, looge teenuse [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) paanil **Tugi** tugiteenusepilet, et saada järgmiste sammude jaoks abi.</span><span class="sxs-lookup"><span data-stu-id="37527-173">If the domain that you will use is already active and live, create a support ticket from the **Support** tile in [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/) to get assistance for your next steps.</span></span> <span data-ttu-id="37527-174">Lisateavet leiate teemast [Finance and Operationsi rakenduste või teenuse Lifecycle Services (LCS) tugi](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="37527-174">For more information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

<span data-ttu-id="37527-175">Kui teie domeen on uus ja ei ole olemasolev kasutatav domeen, saate lisada oma kohandatud domeeni Azure'i sisenemispunkti teenuse konfiguratsiooni.</span><span class="sxs-lookup"><span data-stu-id="37527-175">If your domain is new and is not a pre-existing live domain, you can add your custom domain to the configuration for Azure Front Door Service.</span></span> <span data-ttu-id="37527-176">See võimaldab suunata veebiliiklust teie saidile Azure'i sisenemispunkti teenuse kaudu.</span><span class="sxs-lookup"><span data-stu-id="37527-176">This will enable web traffic to direct to your site via the Azure Front Door instance.</span></span> <span data-ttu-id="37527-177">Kohandatud domeeni lisamiseks (nt `www.fabrikam.com`) peate konfigureerima domeeni kanoonilise nime (CNAME).</span><span class="sxs-lookup"><span data-stu-id="37527-177">To add the custom domain (for example, `www.fabrikam.com`), you must configure a Canonical Name (CNAME) for the domain.</span></span>

<span data-ttu-id="37527-178">Järgmisel illustratsioonil on näha Azure’i sisenemispunkti teenuse dialoogiaken **Konfiguratsioon CNAME**.</span><span class="sxs-lookup"><span data-stu-id="37527-178">The following illustration shows the **CNAME configuration** dialog box in Azure Front Door Service.</span></span>

![Dialoogiaken Konfiguratsioon CNAME](./media/CNAME_Configuration.png)

<span data-ttu-id="37527-180">Saate kasutada Azure’i sisenemispunkti teenust serdi haldamiseks või saate kasutada oma kohandatud domeeni serti.</span><span class="sxs-lookup"><span data-stu-id="37527-180">You can use Azure Front Door Service to manage the certificate, or you can use your own certificate for the custom domain.</span></span>

<span data-ttu-id="37527-181">Järgmisel illustratsioonil on näha Azure’i sisenemispunkti teenuse dialoogiaken **Kohandatud domeeni HTTPS**.</span><span class="sxs-lookup"><span data-stu-id="37527-181">The following illustration shows the **Custom Domain HTTPS** dialog box in Azure Front Door Service.</span></span>

![Dialoogiaken Kohandatud domeeni HTTPS](./media/Custom_Domain_HTTPS.png)

<span data-ttu-id="37527-183">Üksikasjalikku teavet kohandatud domeeni lisamise kohta oma Azure'i sisenemispunkti leiate teemast [Kohandatud domeeni lisamine sisenemispunkti](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span><span class="sxs-lookup"><span data-stu-id="37527-183">For detailed instructions on adding a custom domain to your Azure Front Door, see [Add a custom domain to your Front Door](https://docs.microsoft.com/azure/frontdoor/front-door-custom-domain).</span></span>

<span data-ttu-id="37527-184">Teie CDN peaks nüüd olema õigesti konfigureeritud, et seda saaks teie Commerce’i saidiga kasutada.</span><span class="sxs-lookup"><span data-stu-id="37527-184">Your CDN should now be correctly configured so that it can be used with your Commerce site.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="37527-185">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="37527-185">Additional resources</span></span>

[<span data-ttu-id="37527-186">Domeeninime konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="37527-186">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="37527-187">Uue e-kaubanduse saidi juurutamine</span><span class="sxs-lookup"><span data-stu-id="37527-187">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="37527-188">E-kaubanduse saidi loomine</span><span class="sxs-lookup"><span data-stu-id="37527-188">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="37527-189">Veebisaidi seostamine kanaliga</span><span class="sxs-lookup"><span data-stu-id="37527-189">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="37527-190">robots.txt-failide haldamine</span><span class="sxs-lookup"><span data-stu-id="37527-190">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="37527-191">URL-i hulgiümbersuunamiste üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="37527-191">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="37527-192">B2C rentniku seadistus Kaubanduses</span><span class="sxs-lookup"><span data-stu-id="37527-192">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="37527-193">Kasutaja sisselogimiseks kohandatud lehtede seadistamine</span><span class="sxs-lookup"><span data-stu-id="37527-193">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="37527-194">Mitme B2C rentniku konfigureerimine Kaubanduskeskkonnas</span><span class="sxs-lookup"><span data-stu-id="37527-194">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="37527-195">Asukohapõhise poetuvastuse lubamine</span><span class="sxs-lookup"><span data-stu-id="37527-195">Enable location-based store detection</span></span>](enable-store-detection.md)
