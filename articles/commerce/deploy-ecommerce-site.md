---
title: Uue e-kaubanduse rentniku juurutamine
description: Selles teemas kirjeldatakse, kuidas juurutada uut e-kaubanduse rentnikku, kasutades Microsoft Dynamicsi teenust Lifecycle Services (LCS).
author: psimolin
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 00f35b516dbf6ab4d4d9171c84a16b89f6afe832
ms.sourcegitcommit: adf196c51e2b6f532d99c177b4c6778cea8a2efc
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/02/2020
ms.locfileid: "3533271"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="5dcc2-103">Uue e-kaubanduse rentniku juurutamine</span><span class="sxs-lookup"><span data-stu-id="5dcc2-103">Deploy a new e-Commerce tenant</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5dcc2-104">Selles teemas kirjeldatakse, kuidas juurutada uut e-kaubanduse saiti, kasutades Microsoft Dynamicsi teenust Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="5dcc2-104">This topic describes how to deploy a new e-Commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="overview"></a><span data-ttu-id="5dcc2-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="5dcc2-105">Overview</span></span>

<span data-ttu-id="5dcc2-106">Microsoft Dynamicsi teenus Lifecycle Services (LCS) on pilvepõhine koostöö tööruum, mida partnerid ja kliendid saavad kasutada oma projektide ja keskkondade haldamiseks, Microsoft Dynamicsi toodete ja funktsioonide kohta uusima teabe vaatamiseks ning teenindusjuhtumite loomiseks, jälgimiseks ja sirvimiseks.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-106">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="5dcc2-107">E-kaubanduse haldusefunktsioonid on LCS-i integreeritud.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-107">E-Commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="5dcc2-108">Lisateavet LCS-i kohta vaadake teemast [Teenuse Lifecycle Services kasutusjuhend](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span><span class="sxs-lookup"><span data-stu-id="5dcc2-108">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="5dcc2-109">Alustamine</span><span class="sxs-lookup"><span data-stu-id="5dcc2-109">Get started</span></span>

<span data-ttu-id="5dcc2-110">Enne e-kaubanduse lähtestamist tuleb teil lähtestada projekt, keskkond ja Retail Cloud Scale Unit (RCSU).</span><span class="sxs-lookup"><span data-stu-id="5dcc2-110">Before you can initialize e-Commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="5dcc2-111">LCS-i lähtestamiseks peab teil olema kas projekti omaniku või keskkonnahalduri rolli õigused.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-111">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="5dcc2-112">Tootmise ja liivakasti keskkonna topoloogiad on toetatud.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-112">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="5dcc2-113">Lisateavet keskkondade kohta vaadake teemast [Keskkonna planeerimine](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span><span class="sxs-lookup"><span data-stu-id="5dcc2-113">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="5dcc2-114">Lisateavet RCSU kohta leiate teemast [Lähtesta Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="5dcc2-114">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="5dcc2-115">E-kaubanduse lähtestamine</span><span class="sxs-lookup"><span data-stu-id="5dcc2-115">Initialize e-Commerce</span></span>

<span data-ttu-id="5dcc2-116">Kasutage seda protseduuri, et lähtestada e-kaubanduse funktsiooni olemasolevas keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-116">Use this procedure to initialize the e-Commerce feature in an existing environment.</span></span>

<span data-ttu-id="5dcc2-117">Enne alustamist veenduge, et teil on järgmine vajalik teave.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-117">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="5dcc2-118">Kasutatav RCSU.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-118">The RCSU that will be used.</span></span>
- <span data-ttu-id="5dcc2-119">Microsoft Azure Active Directory turvagrupp, mida kasutatakse e-kaubanduse süsteemiadministraatorite jaoks.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-119">The Microsoft Azure Active Directory security group that will be used for e-Commerce system admins.</span></span>
- <span data-ttu-id="5dcc2-120">Microsoft Azure Active Directory turvagrupp, mida kasutatakse hinnangute ja arvustuste moderaatorite jaoks.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-120">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="5dcc2-121">Keskkonnaga seostatavad domeenid.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-121">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="5dcc2-122">Lisaks saate koguda järgmist valikulist teavet.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-122">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="5dcc2-123">Azure AD ettevõtja ja tarbija vaheline (B2C) teave.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-123">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="5dcc2-124">Rentniku nimi.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-124">Tenant Name.</span></span>
    - <span data-ttu-id="5dcc2-125">Kliendi ID.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-125">Client ID.</span></span>
    - <span data-ttu-id="5dcc2-126">Kohandatud sisselogimisdomeen.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-126">Login Custom Domain.</span></span>
    - <span data-ttu-id="5dcc2-127">Vastuse URL.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-127">Reply URL.</span></span>
    - <span data-ttu-id="5dcc2-128">Registreerumis- ja sisselogimispoliitika ID.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-128">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="5dcc2-129">Paroolilähtestuspoliitika ID.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-129">Reset password Policy ID.</span></span>
    - <span data-ttu-id="5dcc2-130">Profiilipoliitika ID redigeerimine.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-130">Edit Profile Policy ID.</span></span>

> [!NOTE]
> <span data-ttu-id="5dcc2-131">Seda teavet saab hiljem teenuse taotluse alusel lisada.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-131">This information can be added later, through a service request.</span></span>

<span data-ttu-id="5dcc2-132">Pärast nõutava teabe kogumist tehke e-kaubanduse lähtestamiseks järgmist.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-132">After you've collected the required information, follow these steps to initialize e-Commerce.</span></span>

1. <span data-ttu-id="5dcc2-133">Logige teenusesse [LCS](https://lcs.dynamics.com) sisse.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-133">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="5dcc2-134">Avage projekt, mis sisaldab keskkonda, kus soovite e-kaubandust lähtestada.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-134">Open the project that contains the environment where you want to initialize e-Commerce.</span></span>
1. <span data-ttu-id="5dcc2-135">Jaotises **Keskkond** valige keskkond.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-135">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="5dcc2-136">Jaotises **Keskkonna funktsioonid** valige link **Jaemüügi haldus**.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-136">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="5dcc2-137">Vahekaardil **E-kaubandus** valige **Seadistus**.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-137">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="5dcc2-138">Kuvatakse dialoogiaken, kus peate sisestama ettevalmistamiseks vajaliku teabe.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-138">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="5dcc2-139">Täitke nõutud teave ja seejärel minge järgmisele lehele.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-139">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="5dcc2-140">Järgmisel lehel täitke nõutud teave ja seejärel esitage vorm.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-140">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="5dcc2-141">Olete naasnud vahekaardile **E-kaubandus**, kus peaksite nägema, et lähtestamine on alanud.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-141">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="5dcc2-142">Lähtestamise oleku vaatamiseks kas vajutage **Lähtesta** või naaske hiljem vahekaardile **E-kaubandus**.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-142">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="5dcc2-143">Kui e-kaubandus on LCS-ist lähtestatud, valmistab süsteem ette mitu komponenti, mis on e-kaubanduse vahekaardile vajalikud ja seostab need keskkonnaga.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-143">When e-Commerce is initialized from LCS, the system provisions several components that are required for e-Commerce and associates them with the environment.</span></span> <span data-ttu-id="5dcc2-144">Pärast ettevalmistuse lõpuleviimist uuendatakse vahekaarti **E-kaubandus** lehel **Jaemüügi haldus**, et kajastada ettevalmistamist.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-144">After provisioning is complete, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="5dcc2-145">Lehel kuvatakse uusimad kohanduste juurutused ja kõikide teiste käimasolevate juurutuste olekud.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-145">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="5dcc2-146">See sisaldab ka linke e-kaubanduse saidile ja e-kaubanduse saidi ehitajat, kus saidid on tehtud.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-146">It also includes links to the e-Commerce site and the e-Commerce site builder where sites are authored.</span></span>

## <a name="access-site-builder"></a><span data-ttu-id="5dcc2-147">Juurdepääs saidiehitajale</span><span class="sxs-lookup"><span data-stu-id="5dcc2-147">Access site builder</span></span>

<span data-ttu-id="5dcc2-148">Saidiehitajale juurdepääsuks avage vahekaart **e-Commerce** LCS lehel **Jaemüügi haldur** ja valige link **e-Commerce'i saidihalduse tööriist**.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-148">To access site builder, go to the **e-Commerce** tab on the **Retail management** page in LCS and select the **e-Commerce site management tool** link.</span></span> <span data-ttu-id="5dcc2-149">Saidiehitaja sihtleht kuvab rentniku tasemel vaadet.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-149">The site builder landing page displays a tenant-level view.</span></span> <span data-ttu-id="5dcc2-150">Sellelt lehelt saate teha järgmist.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-150">From this page, you can:</span></span>

- <span data-ttu-id="5dcc2-151">Rentniku taseme sätete muutmine.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-151">Modify tenant-level settings.</span></span>
- <span data-ttu-id="5dcc2-152">Navigeerige mistahes loodud saidile ja omage vaatamiseks õigusi.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-152">Navigate to any site you have created, and have permission to view.</span></span> 
- <span data-ttu-id="5dcc2-153">Juurdepääs ülevaadete funktsioonidele, nagu modereerimine ja aruandlus.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-153">Access Reviews features such as moderation and reporting.</span></span>
- <span data-ttu-id="5dcc2-154">Uue saidi loomine.</span><span class="sxs-lookup"><span data-stu-id="5dcc2-154">Create a new site.</span></span> <span data-ttu-id="5dcc2-155">Lisateavet uue saidi loomise kohta vt jaotisest [Uue e-kaubanduse saidi loomine](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="5dcc2-155">For more information about how to create a new site, see [Create an e-Commerce site](create-ecommerce-site.md) .</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="5dcc2-156">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="5dcc2-156">Additional resources</span></span>

[<span data-ttu-id="5dcc2-157">Domeeninime konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="5dcc2-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="5dcc2-158">E-kaubanduse saidi loomine</span><span class="sxs-lookup"><span data-stu-id="5dcc2-158">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="5dcc2-159">Veebisaidi seostamine kanaliga</span><span class="sxs-lookup"><span data-stu-id="5dcc2-159">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="5dcc2-160">robots.txt-failide haldamine</span><span class="sxs-lookup"><span data-stu-id="5dcc2-160">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="5dcc2-161">URL-i hulgiümbersuunamiste üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="5dcc2-161">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="5dcc2-162">B2C rentniku seadistus Kaubanduses</span><span class="sxs-lookup"><span data-stu-id="5dcc2-162">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="5dcc2-163">Kasutaja sisselogimiseks kohandatud lehtede seadistamine</span><span class="sxs-lookup"><span data-stu-id="5dcc2-163">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="5dcc2-164">Mitme B2C rentniku konfigureerimine Kaubanduskeskkonnas</span><span class="sxs-lookup"><span data-stu-id="5dcc2-164">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="5dcc2-165">Sisuedastusvõrgu (CDN) toe lisamine</span><span class="sxs-lookup"><span data-stu-id="5dcc2-165">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="5dcc2-166">Asukohapõhise poetuvastuse lubamine</span><span class="sxs-lookup"><span data-stu-id="5dcc2-166">Enable location-based store detection</span></span>](enable-store-detection.md)
