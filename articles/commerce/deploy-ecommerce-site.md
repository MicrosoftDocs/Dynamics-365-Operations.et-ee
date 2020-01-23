---
title: Uue e-kaubanduse rentniku juurutamine
description: Selles teemas kirjeldatakse, kuidas juurutada uut e-kaubanduse rentnikku, kasutades Microsoft Dynamicsi teenust Lifecycle Services (LCS).
author: psimolin
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: 10dab1e62446ff7f60ad48fd0841bde5cfd29e12
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945509"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="86f30-103">Uue e-kaubanduse rentniku juurutamine</span><span class="sxs-lookup"><span data-stu-id="86f30-103">Deploy a new e-Commerce tenant</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="86f30-104">Selles teemas kirjeldatakse, kuidas juurutada uut e-kaubanduse saiti, kasutades Microsoft Dynamicsi teenust Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="86f30-104">This topic describes how to deploy a new e-Commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="overview"></a><span data-ttu-id="86f30-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="86f30-105">Overview</span></span>
    
<span data-ttu-id="86f30-106">Microsoft Dynamicsi teenus Lifecycle Services (LCS) on pilvepõhine koostöö tööruum, mida partnerid ja kliendid saavad kasutada oma projektide ja keskkondade haldamiseks, Microsoft Dynamicsi toodete ja funktsioonide kohta uusima teabe vaatamiseks ning teenindusjuhtumite loomiseks, jälgimiseks ja sirvimiseks.</span><span class="sxs-lookup"><span data-stu-id="86f30-106">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="86f30-107">E-kaubanduse haldusefunktsioonid on LCS-i integreeritud.</span><span class="sxs-lookup"><span data-stu-id="86f30-107">E-Commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="86f30-108">Lisateavet LCS-i kohta vaadake teemast [Teenuse Lifecycle Services kasutusjuhend](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span><span class="sxs-lookup"><span data-stu-id="86f30-108">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="86f30-109">Alustamine</span><span class="sxs-lookup"><span data-stu-id="86f30-109">Get started</span></span>

<span data-ttu-id="86f30-110">Enne e-kaubanduse lähtestamist tuleb teil lähtestada projekt, keskkond ja Retail Cloud Scale Unit (RCSU).</span><span class="sxs-lookup"><span data-stu-id="86f30-110">Before you can initialize e-Commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="86f30-111">LCS-i lähtestamiseks peab teil olema kas projekti omaniku või keskkonnahalduri rolli õigused.</span><span class="sxs-lookup"><span data-stu-id="86f30-111">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="86f30-112">Tootmise ja liivakasti keskkonna topoloogiad on toetatud.</span><span class="sxs-lookup"><span data-stu-id="86f30-112">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="86f30-113">Lisateavet keskkondade kohta vaadake teemast [Keskkonna planeerimine](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span><span class="sxs-lookup"><span data-stu-id="86f30-113">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="86f30-114">Lisateavet RCSU kohta leiate teemast [Lähtesta Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="86f30-114">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="86f30-115">E-kaubanduse lähtestamine</span><span class="sxs-lookup"><span data-stu-id="86f30-115">Initialize e-Commerce</span></span>

<span data-ttu-id="86f30-116">Kasutage seda protseduuri, et lähtestada e-kaubanduse funktsiooni olemasolevas keskkonnas.</span><span class="sxs-lookup"><span data-stu-id="86f30-116">Use this procedure to initialize the e-Commerce feature in an existing environment.</span></span>

<span data-ttu-id="86f30-117">Enne alustamist veenduge, et teil on järgmine vajalik teave.</span><span class="sxs-lookup"><span data-stu-id="86f30-117">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="86f30-118">Kasutatav RCSU.</span><span class="sxs-lookup"><span data-stu-id="86f30-118">The RCSU that will be used.</span></span>
- <span data-ttu-id="86f30-119">Microsoft Azure Active Directory turvagrupp, mida kasutatakse e-kaubanduse süsteemiadministraatorite jaoks.</span><span class="sxs-lookup"><span data-stu-id="86f30-119">The Microsoft Azure Active Directory security group that will be used for e-Commerce system admins.</span></span>
- <span data-ttu-id="86f30-120">Microsoft Azure Active Directory turvagrupp, mida kasutatakse hinnangute ja arvustuste moderaatorite jaoks.</span><span class="sxs-lookup"><span data-stu-id="86f30-120">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="86f30-121">Keskkonnaga seostatavad domeenid.</span><span class="sxs-lookup"><span data-stu-id="86f30-121">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="86f30-122">Lisaks saate koguda järgmist valikulist teavet.</span><span class="sxs-lookup"><span data-stu-id="86f30-122">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="86f30-123">Azure AD ettevõtja ja tarbija vaheline (B2C) teave.</span><span class="sxs-lookup"><span data-stu-id="86f30-123">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="86f30-124">Rentniku nimi.</span><span class="sxs-lookup"><span data-stu-id="86f30-124">Tenant Name.</span></span>
    - <span data-ttu-id="86f30-125">Kliendi ID.</span><span class="sxs-lookup"><span data-stu-id="86f30-125">Client ID.</span></span>
    - <span data-ttu-id="86f30-126">Kohandatud sisselogimisdomeen.</span><span class="sxs-lookup"><span data-stu-id="86f30-126">Login Custom Domain.</span></span>
    - <span data-ttu-id="86f30-127">Vastuse URL.</span><span class="sxs-lookup"><span data-stu-id="86f30-127">Reply URL.</span></span>
    - <span data-ttu-id="86f30-128">Registreerumis- ja sisselogimispoliitika ID.</span><span class="sxs-lookup"><span data-stu-id="86f30-128">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="86f30-129">Paroolilähtestuspoliitika ID.</span><span class="sxs-lookup"><span data-stu-id="86f30-129">Reset password Policy ID.</span></span>
    - <span data-ttu-id="86f30-130">Profiilipoliitika ID redigeerimine.</span><span class="sxs-lookup"><span data-stu-id="86f30-130">Edit Profile Policy ID.</span></span>

[!NOTE]
<span data-ttu-id="86f30-131">Seda teavet saab hiljem teenuse taotluse alusel lisada.</span><span class="sxs-lookup"><span data-stu-id="86f30-131">This information can be added later, through a service request.</span></span>

<span data-ttu-id="86f30-132">Pärast nõutava teabe kogumist tehke e-kaubanduse lähtestamiseks järgmist.</span><span class="sxs-lookup"><span data-stu-id="86f30-132">After you've collected the required information, follow these steps to initialize e-Commerce.</span></span>

1. <span data-ttu-id="86f30-133">Logige teenusesse [LCS](https://lcs.dynamics.com) sisse.</span><span class="sxs-lookup"><span data-stu-id="86f30-133">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="86f30-134">Avage projekt, mis sisaldab keskkonda, kus soovite e-kaubandust lähtestada.</span><span class="sxs-lookup"><span data-stu-id="86f30-134">Open the project that contains the environment where you want to initialize e-Commerce.</span></span>
1. <span data-ttu-id="86f30-135">Jaotises **Keskkond** valige keskkond.</span><span class="sxs-lookup"><span data-stu-id="86f30-135">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="86f30-136">Jaotises **Keskkonna funktsioonid** valige link **Jaemüügi haldus**.</span><span class="sxs-lookup"><span data-stu-id="86f30-136">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="86f30-137">Vahekaardil **E-kaubandus** valige **Seadistus**.</span><span class="sxs-lookup"><span data-stu-id="86f30-137">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="86f30-138">Kuvatakse dialoogiaken, kus peate sisestama ettevalmistamiseks vajaliku teabe.</span><span class="sxs-lookup"><span data-stu-id="86f30-138">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="86f30-139">Täitke nõutud teave ja seejärel minge järgmisele lehele.</span><span class="sxs-lookup"><span data-stu-id="86f30-139">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="86f30-140">Järgmisel lehel täitke nõutud teave ja seejärel esitage vorm.</span><span class="sxs-lookup"><span data-stu-id="86f30-140">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="86f30-141">Olete naasnud vahekaardile **E-kaubandus**, kus peaksite nägema, et lähtestamine on alanud.</span><span class="sxs-lookup"><span data-stu-id="86f30-141">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="86f30-142">Lähtestamise oleku vaatamiseks kas vajutage **Lähtesta** või naaske hiljem vahekaardile **E-kaubandus**.</span><span class="sxs-lookup"><span data-stu-id="86f30-142">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="86f30-143">Kui e-kaubandus on LCS-ist lähtestatud, valmistab süsteem ette mitu komponenti, mis on e-kaubanduse vahekaardile vajalikud ja seostab need keskkonnaga.</span><span class="sxs-lookup"><span data-stu-id="86f30-143">When e-Commerce is initialized from LCS, the system provisions several components that are required for e-Commerce and associates them with the environment.</span></span> <span data-ttu-id="86f30-144">Pärast ettevalmistuse lõpuleviimist uuendatakse vahekaarti **E-kaubandus** lehel **Jaemüügi haldus**, et kajastada ettevalmistamist.</span><span class="sxs-lookup"><span data-stu-id="86f30-144">After provisioning is completed, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="86f30-145">Lehel kuvatakse uusimad kohanduste juurutused ja kõikide teiste käimasolevate juurutuste olekud.</span><span class="sxs-lookup"><span data-stu-id="86f30-145">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="86f30-146">See sisaldab ka linke e-kaubanduse saidile ja e-kaubanduse saidi halduse tööriistale (autorluse tööriist).</span><span class="sxs-lookup"><span data-stu-id="86f30-146">It also includes links to the e-Commerce site and the e-Commerce site management tool (the authoring tool).</span></span>

## <a name="access-the-authoring-environment"></a><span data-ttu-id="86f30-147">Juurdepääs autorluse keskkonnale</span><span class="sxs-lookup"><span data-stu-id="86f30-147">Access the authoring environment</span></span>

<span data-ttu-id="86f30-148">Autorlusele keskkonnale juurdepääsuks avage vahekaart **E-kaubandus** lehel **Jaemüügi haldus**.</span><span class="sxs-lookup"><span data-stu-id="86f30-148">To access the authoring environment, go to the **e-Commerce** tab on the **Retail management** page.</span></span> <span data-ttu-id="86f30-149">Sealt leiate oma e-kaubanduse saidi ja saidi halduse tööriista lingid.</span><span class="sxs-lookup"><span data-stu-id="86f30-149">There, you will find links to your e-Commerce site and the site management tool.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="86f30-150">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="86f30-150">Additional resources</span></span>

[<span data-ttu-id="86f30-151">Domeeninime konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="86f30-151">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="86f30-152">E-kaubanduse saidi loomine</span><span class="sxs-lookup"><span data-stu-id="86f30-152">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="86f30-153">Veebisaidi seostamine kanaliga</span><span class="sxs-lookup"><span data-stu-id="86f30-153">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="86f30-154">Robots.txt-failide haldamine</span><span class="sxs-lookup"><span data-stu-id="86f30-154">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="86f30-155">Kasutaja sisselogimiseks kohandatud lehtede seadistamine</span><span class="sxs-lookup"><span data-stu-id="86f30-155">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="86f30-156">Sisuedastusvõrgu (CDN) toe lisamine</span><span class="sxs-lookup"><span data-stu-id="86f30-156">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="86f30-157">Asukohapõhise poetuvastuse lubamine</span><span class="sxs-lookup"><span data-stu-id="86f30-157">Enable location-based store detection</span></span>](enable-store-detection.md)
