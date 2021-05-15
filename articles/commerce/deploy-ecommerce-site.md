---
title: Uue e-kaubanduse rentniku juurutamine
description: Selles teemas kirjeldatakse, kuidas juurutada uut Dynamics 365 Commerce'i e-kaubanduse saiti, kasutades teenust Microsoft Dynamics Lifecycle Services (LCS).
author: psimolin
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6b228babfd32a4191eeed2a6d924a8b99f1a5311
ms.sourcegitcommit: 9eadc7ca08e2db3fd208f5fc835551abe9d06dc8
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/22/2021
ms.locfileid: "5936702"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="9d77a-103">Uue e-kaubanduse rentniku juurutamine</span><span class="sxs-lookup"><span data-stu-id="9d77a-103">Deploy a new e-commerce tenant</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="9d77a-104">Selles teemas kirjeldatakse, kuidas juurutada uut Dynamics 365 Commerce'i e-kaubanduse saiti, kasutades teenust Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="9d77a-104">This topic describes how to deploy a new Dynamics 365 Commerce e-commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="9d77a-105">Microsoft Dynamicsi teenus Lifecycle Services (LCS) on pilvepõhine koostöö tööruum, mida partnerid ja kliendid saavad kasutada oma projektide ja keskkondade haldamiseks, Microsoft Dynamicsi toodete ja funktsioonide kohta uusima teabe vaatamiseks ning teenindusjuhtumite loomiseks, jälgimiseks ja sirvimiseks.</span><span class="sxs-lookup"><span data-stu-id="9d77a-105">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="9d77a-106">E-kaubanduse haldusefunktsioonid on LCS-i integreeritud.</span><span class="sxs-lookup"><span data-stu-id="9d77a-106">E-commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="9d77a-107">Lisateavet LCS-i kohta vaadake teemast [Teenuse Lifecycle Services kasutusjuhend](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span><span class="sxs-lookup"><span data-stu-id="9d77a-107">To learn more about LCS, see the [Lifecycle Services User Guide](/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="9d77a-108">Alustage</span><span class="sxs-lookup"><span data-stu-id="9d77a-108">Get started</span></span>

<span data-ttu-id="9d77a-109">Enne e-kaubanduse lähtestamist tuleb teil lähtestada projekt, keskkond ja Retail Cloud Scale Unit (RCSU).</span><span class="sxs-lookup"><span data-stu-id="9d77a-109">Before you can initialize e-commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="9d77a-110">LCS-i lähtestamiseks peab teil olema kas projekti omaniku või keskkonnahalduri rolli õigused.</span><span class="sxs-lookup"><span data-stu-id="9d77a-110">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="9d77a-111">Tootmise ja liivakasti keskkonna topoloogiad on toetatud.</span><span class="sxs-lookup"><span data-stu-id="9d77a-111">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="9d77a-112">Lisateavet keskkondade kohta vaadake teemast [Keskkonna planeerimine](/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span><span class="sxs-lookup"><span data-stu-id="9d77a-112">For more information about environments, see [Environment planning](/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="9d77a-113">Lisateavet RCSU kohta leiate teemast [Lähtesta Retail Cloud Scale Unit](/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="9d77a-113">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="9d77a-114">E-kaubanduse lähtestamine</span><span class="sxs-lookup"><span data-stu-id="9d77a-114">Initialize e-commerce</span></span>

<span data-ttu-id="9d77a-115">Kasutage seda protseduuri, et lähtestada e-kaubanduse funktsioon olemasolevas keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="9d77a-115">Use this procedure to initialize the e-commerce feature in an existing environment.</span></span>

<span data-ttu-id="9d77a-116">Enne alustamist veenduge, et teil on järgmine vajalik teave.</span><span class="sxs-lookup"><span data-stu-id="9d77a-116">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="9d77a-117">Kasutatav RCSU.</span><span class="sxs-lookup"><span data-stu-id="9d77a-117">The RCSU that will be used.</span></span>
- <span data-ttu-id="9d77a-118">Microsoft Azure Active Directory turbegrupp, mida kasutatakse e-kaubanduse süsteemiadministraatorite jaoks.</span><span class="sxs-lookup"><span data-stu-id="9d77a-118">The Microsoft Azure Active Directory security group that will be used for e-commerce system admins.</span></span>
- <span data-ttu-id="9d77a-119">Microsoft Azure Active Directory turvagrupp, mida kasutatakse hinnangute ja arvustuste moderaatorite jaoks.</span><span class="sxs-lookup"><span data-stu-id="9d77a-119">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="9d77a-120">Keskkonnaga seostatavad domeenid.</span><span class="sxs-lookup"><span data-stu-id="9d77a-120">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="9d77a-121">Lisaks saate koguda järgmist valikulist teavet.</span><span class="sxs-lookup"><span data-stu-id="9d77a-121">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="9d77a-122">Azure AD ettevõtja ja tarbija vaheline (B2C) teave.</span><span class="sxs-lookup"><span data-stu-id="9d77a-122">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="9d77a-123">Rentniku nimi.</span><span class="sxs-lookup"><span data-stu-id="9d77a-123">Tenant Name.</span></span>
    - <span data-ttu-id="9d77a-124">Kliendi ID.</span><span class="sxs-lookup"><span data-stu-id="9d77a-124">Client ID.</span></span>
    - <span data-ttu-id="9d77a-125">Kohandatud sisselogimisdomeen.</span><span class="sxs-lookup"><span data-stu-id="9d77a-125">Login Custom Domain.</span></span>
    - <span data-ttu-id="9d77a-126">Vastuse URL.</span><span class="sxs-lookup"><span data-stu-id="9d77a-126">Reply URL.</span></span>
    - <span data-ttu-id="9d77a-127">Registreerumis- ja sisselogimispoliitika ID.</span><span class="sxs-lookup"><span data-stu-id="9d77a-127">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="9d77a-128">Paroolilähtestuspoliitika ID.</span><span class="sxs-lookup"><span data-stu-id="9d77a-128">Reset password Policy ID.</span></span>
    - <span data-ttu-id="9d77a-129">Profiilipoliitika ID redigeerimine.</span><span class="sxs-lookup"><span data-stu-id="9d77a-129">Edit Profile Policy ID.</span></span>

> [!NOTE]
> <span data-ttu-id="9d77a-130">Seda teavet saab hiljem teenuse taotluse alusel lisada.</span><span class="sxs-lookup"><span data-stu-id="9d77a-130">This information can be added later, through a service request.</span></span>

<span data-ttu-id="9d77a-131">Pärast nõutava teabe kogumist tehke e-kaubanduse lähtestamiseks järgmist.</span><span class="sxs-lookup"><span data-stu-id="9d77a-131">After you've collected the required information, follow these steps to initialize e-commerce.</span></span>

1. <span data-ttu-id="9d77a-132">Logige teenusesse [LCS](https://lcs.dynamics.com) sisse.</span><span class="sxs-lookup"><span data-stu-id="9d77a-132">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="9d77a-133">Avage projekt, mis sisaldab keskkonda, kus soovite e-kaubandust lähtestada.</span><span class="sxs-lookup"><span data-stu-id="9d77a-133">Open the project that contains the environment where you want to initialize e-commerce.</span></span>
1. <span data-ttu-id="9d77a-134">Jaotises **Keskkond** valige keskkond.</span><span class="sxs-lookup"><span data-stu-id="9d77a-134">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="9d77a-135">Jaotises **Keskkonna funktsioonid** valige link **Jaemüügi haldus**.</span><span class="sxs-lookup"><span data-stu-id="9d77a-135">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="9d77a-136">Vahekaardil **E-kaubandus** valige **Seadistus**.</span><span class="sxs-lookup"><span data-stu-id="9d77a-136">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="9d77a-137">Kuvatakse dialoogiaken, kus peate sisestama ettevalmistamiseks vajaliku teabe.</span><span class="sxs-lookup"><span data-stu-id="9d77a-137">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="9d77a-138">Täitke nõutud teave ja seejärel minge järgmisele lehele.</span><span class="sxs-lookup"><span data-stu-id="9d77a-138">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="9d77a-139">Järgmisel lehel täitke nõutud teave ja seejärel esitage vorm.</span><span class="sxs-lookup"><span data-stu-id="9d77a-139">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="9d77a-140">Olete naasnud vahekaardile **E-kaubandus**, kus peaksite nägema, et lähtestamine on alanud.</span><span class="sxs-lookup"><span data-stu-id="9d77a-140">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="9d77a-141">Lähtestamise oleku vaatamiseks kas vajutage **Lähtesta** või naaske hiljem vahekaardile **E-kaubandus**.</span><span class="sxs-lookup"><span data-stu-id="9d77a-141">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="9d77a-142">Kui e-kaubandus on LCS-ist lähtestatud, valmistab süsteem ette mitu komponenti, mis on e-kaubandusele vajalikud, ja seostab need keskkonnaga.</span><span class="sxs-lookup"><span data-stu-id="9d77a-142">When e-commerce is initialized from LCS, the system provisions several components that are required for e-commerce and associates them with the environment.</span></span> <span data-ttu-id="9d77a-143">Pärast ettevalmistuse lõpuleviimist uuendatakse vahekaarti **E-kaubandus** lehel **Jaemüügi haldus**, et kajastada ettevalmistamist.</span><span class="sxs-lookup"><span data-stu-id="9d77a-143">After provisioning is complete, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="9d77a-144">Lehel kuvatakse uusimad kohanduste juurutused ja kõikide teiste käimasolevate juurutuste olekud.</span><span class="sxs-lookup"><span data-stu-id="9d77a-144">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="9d77a-145">See sisaldab ka linke e-kaubanduse saidile ja Commerce'i saidiehitajat, kus saidid on tehtud.</span><span class="sxs-lookup"><span data-stu-id="9d77a-145">It also includes links to the e-commerce site and the Commerce site builder where sites are authored.</span></span>

## <a name="access-commerce-site-builder"></a><span data-ttu-id="9d77a-146">Juurdepääs Commerce'i saidiehitajale</span><span class="sxs-lookup"><span data-stu-id="9d77a-146">Access Commerce site builder</span></span>

<span data-ttu-id="9d77a-147">Commerce'i saidiehitajale juurdepääsuks avage vahekaart **E-kaubandus** LCS-i lehel **Jaemüügi haldus** ja valige link **E-kaubanduse saidihalduse tööriist**.</span><span class="sxs-lookup"><span data-stu-id="9d77a-147">To access Commerce site builder, go to the **e-Commerce** tab on the **Retail management** page in LCS and select the **e-Commerce site management tool** link.</span></span> <span data-ttu-id="9d77a-148">Saidiehitaja sihtleht kuvab rentniku tasemel vaadet.</span><span class="sxs-lookup"><span data-stu-id="9d77a-148">The site builder landing page displays a tenant-level view.</span></span> <span data-ttu-id="9d77a-149">Sellelt lehelt saate teha järgmist.</span><span class="sxs-lookup"><span data-stu-id="9d77a-149">From this page, you can:</span></span>

- <span data-ttu-id="9d77a-150">Rentniku taseme sätete muutmine.</span><span class="sxs-lookup"><span data-stu-id="9d77a-150">Modify tenant-level settings.</span></span>
- <span data-ttu-id="9d77a-151">Navigeerige mistahes loodud saidile ja omage vaatamiseks õigusi.</span><span class="sxs-lookup"><span data-stu-id="9d77a-151">Navigate to any site you have created, and have permission to view.</span></span> 
- <span data-ttu-id="9d77a-152">Juurdepääs ülevaadete funktsioonidele, nagu modereerimine ja aruandlus.</span><span class="sxs-lookup"><span data-stu-id="9d77a-152">Access Reviews features such as moderation and reporting.</span></span>
- <span data-ttu-id="9d77a-153">Uue saidi loomine.</span><span class="sxs-lookup"><span data-stu-id="9d77a-153">Create a new site.</span></span> <span data-ttu-id="9d77a-154">Lisateavet uue saidi loomise kohta vt jaotisest [E-kaubanduse saidi loomine](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="9d77a-154">For more information about how to create a new site, see [Create an e-commerce site](create-ecommerce-site.md) .</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="9d77a-155">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="9d77a-155">Additional resources</span></span>

[<span data-ttu-id="9d77a-156">Domeeninime konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="9d77a-156">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="9d77a-157">E-kaubanduse saidi loomine</span><span class="sxs-lookup"><span data-stu-id="9d77a-157">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="9d77a-158">Dynamics 365 Commerce'i saidi seostamine võrgukanaliga</span><span class="sxs-lookup"><span data-stu-id="9d77a-158">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="9d77a-159">Robots.txt-failide haldamine</span><span class="sxs-lookup"><span data-stu-id="9d77a-159">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="9d77a-160">Üleslaadimise URL suunab ümber hulgi</span><span class="sxs-lookup"><span data-stu-id="9d77a-160">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="9d77a-161">B2C rentniku seadistus Kaubanduses</span><span class="sxs-lookup"><span data-stu-id="9d77a-161">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="9d77a-162">Kasutaja sisselogimiseks kohandatud lehtede seadistamine</span><span class="sxs-lookup"><span data-stu-id="9d77a-162">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="9d77a-163">Mitme B2C rentniku konfigureerimine Kaubanduskeskkonnas</span><span class="sxs-lookup"><span data-stu-id="9d77a-163">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="9d77a-164">Sisuedastusvõrgu (CDN) toe lisamine</span><span class="sxs-lookup"><span data-stu-id="9d77a-164">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="9d77a-165">Asukohapõhise poetuvastuse lubamine</span><span class="sxs-lookup"><span data-stu-id="9d77a-165">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]