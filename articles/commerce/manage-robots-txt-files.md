---
title: Failide robots.txt haldamine
description: See teema kirjeldab failide robots.txt haldamist teenuses Microsoft Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.search.region: Global
ms.search.industry: retail
ms.author: brishoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: d248dae36e6e038749ee17a5a6ccb32f1dde0aed
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096839"
---
# <a name="manage-robotstxt-files"></a><span data-ttu-id="7069d-103">Failide robots.txt haldamine</span><span class="sxs-lookup"><span data-stu-id="7069d-103">Manage robots.txt files</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="7069d-104">See teema kirjeldab failide robots.txt haldamist teenuses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="7069d-104">This topic describes how to manage robots.txt files in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="7069d-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="7069d-105">Overview</span></span>

<span data-ttu-id="7069d-106">Robotite välistamise standard või robots.txt on standard, mida veebisaidid kasutavad veebirobotitega suhtlemiseks.</span><span class="sxs-lookup"><span data-stu-id="7069d-106">The robots exclusion standard, or robots.txt, is a standard that websites use to communicate with web robots.</span></span> <span data-ttu-id="7069d-107">See juhendab veebiroboteid veebisaidi mis tahes alade osas, mida ei tohiks külastada.</span><span class="sxs-lookup"><span data-stu-id="7069d-107">It instructs web robots about any areas of a website that should not be visited.</span></span> <span data-ttu-id="7069d-108">Roboteid kasutavad sageli otsingumootorid veebisaitide indekseerimiseks.</span><span class="sxs-lookup"><span data-stu-id="7069d-108">Robots are often used by search engines to index websites.</span></span>

<span data-ttu-id="7069d-109">Robotite serverist välistamiseks loote serveris faili.</span><span class="sxs-lookup"><span data-stu-id="7069d-109">To exclude robots from a server, you create a file on the server.</span></span> <span data-ttu-id="7069d-110">Selles failis määrate robotite juurdepääsupoliitika.</span><span class="sxs-lookup"><span data-stu-id="7069d-110">In this file, you specify an access policy for robots.</span></span> <span data-ttu-id="7069d-111">Fail peab olema HTTP kaudu juurdepääsetav kohalikul URL-il **/robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="7069d-111">The file must be accessible via HTTP at the local URL **/robots.txt**.</span></span> <span data-ttu-id="7069d-112">Fail robots.txt aitab otsingumootoritel teie saidi sisu indekseerida.</span><span class="sxs-lookup"><span data-stu-id="7069d-112">The robots.txt file helps search engines index the content on your site.</span></span>

<span data-ttu-id="7069d-113">Dynamics 365 Commerce võimaldab teil faili robots.txt oma domeenile üles laadida.</span><span class="sxs-lookup"><span data-stu-id="7069d-113">Dynamics 365 Commerce lets you upload a robots.txt file for your domain.</span></span> <span data-ttu-id="7069d-114">Iga Commerce’i keskkonna domeeni jaoks saate üles laadida ühe robots.txt-faili ja seostada selle domeeniga.</span><span class="sxs-lookup"><span data-stu-id="7069d-114">For each domain in your Commerce environment, you can upload one robots.txt file and associate it with that domain.</span></span>

<span data-ttu-id="7069d-115">Lisateavet faili robots.txt kohta leiate teemast [Veebirobotite lehed](https://www.robotstxt.org/).</span><span class="sxs-lookup"><span data-stu-id="7069d-115">For more information about the robots.txt file, visit [The Web Robots Pages](https://www.robotstxt.org/).</span></span>

## <a name="upload-a-robotstxt-file"></a><span data-ttu-id="7069d-116">Faili robots.txt üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="7069d-116">Upload a robots.txt file</span></span>

<span data-ttu-id="7069d-117">Pärast seda, kui olete loonud ja redigeerinud faili robots.txt vastavalt [robotite välistamise standardile](https://www.robotstxt.org/orig.html), veenduge, et fail oleks juurdepääsetav arvutis, kus kasutate Commerce’i autorluse tööriistu.</span><span class="sxs-lookup"><span data-stu-id="7069d-117">After you've created and edited your robots.txt file according to the [robots exclusion standard](https://www.robotstxt.org/orig.html), make sure that the file is accessible on the computer where you will use the Commerce authoring tools.</span></span> <span data-ttu-id="7069d-118">Faili nimi peab olema **robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="7069d-118">The file must be named **robots.txt**.</span></span> <span data-ttu-id="7069d-119">Parimate tulemuste saavutamiseks peab see olema standardis märgitud vormingus.</span><span class="sxs-lookup"><span data-stu-id="7069d-119">For best results, it must be in the format that is noted in the standard.</span></span> <span data-ttu-id="7069d-120">Iga Commerce’i klient vastutab oma robots.txt-faili sisu valideerimise ja haldamise eest.</span><span class="sxs-lookup"><span data-stu-id="7069d-120">Each Commerce customer is responsible for validating and maintaining the contents of its robots.txt file.</span></span> <span data-ttu-id="7069d-121">Faili robots.txt üleslaadimiseks peate olema Commerce’i süsteemiadministraatorina sisse logitud.</span><span class="sxs-lookup"><span data-stu-id="7069d-121">To upload a robots.txt file, you must be signed in to Commerce as a system admin.</span></span>

<span data-ttu-id="7069d-122">Faili robots.txt Commerce’is üleslaadimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="7069d-122">To upload a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="7069d-123">Logige Commerce’i süsteemiadministraatorina sisse.</span><span class="sxs-lookup"><span data-stu-id="7069d-123">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="7069d-124">Valige vasakpoolsel navigeerimispaanil selle laiendamiseks suvand **Rentniku sätted** (hammasratta sümboli kõrval).</span><span class="sxs-lookup"><span data-stu-id="7069d-124">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="7069d-125">Jaotises **Rentniku sätted** valige **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="7069d-125">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="7069d-126">Akna põhiosas kuvatakse kõigi teie keskkonnaga seotud domeenide loend.</span><span class="sxs-lookup"><span data-stu-id="7069d-126">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="7069d-127">Valige käsk **Halda**, et laadida fail robots.txt oma keskkonna domeeni jaoks üles.</span><span class="sxs-lookup"><span data-stu-id="7069d-127">Select **Manage** to upload a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="7069d-128">Parempoolses menüüs valige failiga robots.txt seostatud domeeni kõrval nupp **Laadi üles** (ülespoole suunatud nool).</span><span class="sxs-lookup"><span data-stu-id="7069d-128">On the menu on the right, select the **Upload** button (the upward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="7069d-129">Kuvatakse failibrauseri dialoogiboks.</span><span class="sxs-lookup"><span data-stu-id="7069d-129">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="7069d-130">Dialoogiboksis sirvige leidmiseks ja valige fail robots.txt, mille soovite seotud domeeni jaoks üles laadida, ja seejärel valige üleslaadimise lõpetamiseks käsk **Ava**.</span><span class="sxs-lookup"><span data-stu-id="7069d-130">In the dialog box, browse to and select the robots.txt file that you want to upload for the associated domain, and then select **Open** to complete the upload.</span></span>

> [!NOTE] 
> <span data-ttu-id="7069d-131">Üleslaadimise ajal kontrollib Commerce, kas fail on tekstifail, kuid see ei valideeri faili sisu.</span><span class="sxs-lookup"><span data-stu-id="7069d-131">During upload, Commerce verifies that the file is a text file, but it doesn't validate the file's contents.</span></span>

## <a name="download-a-robotstxt-file"></a><span data-ttu-id="7069d-132">Faili robots.txt allalaadimine</span><span class="sxs-lookup"><span data-stu-id="7069d-132">Download a robots.txt file</span></span>

<span data-ttu-id="7069d-133">Faili robots.txt Commerce’is allalaadimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="7069d-133">To download a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="7069d-134">Logige Commerce’i süsteemiadministraatorina sisse.</span><span class="sxs-lookup"><span data-stu-id="7069d-134">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="7069d-135">Valige vasakpoolsel navigeerimispaanil selle laiendamiseks suvand **Rentniku sätted** (hammasratta sümboli kõrval).</span><span class="sxs-lookup"><span data-stu-id="7069d-135">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="7069d-136">Jaotises **Rentniku sätted** valige **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="7069d-136">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="7069d-137">Akna põhiosas kuvatakse kõigi teie keskkonnaga seotud domeenide loend.</span><span class="sxs-lookup"><span data-stu-id="7069d-137">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="7069d-138">Valige käsk **Halda**, et laadida fail robots.txt oma keskkonna domeeni jaoks alla.</span><span class="sxs-lookup"><span data-stu-id="7069d-138">Select **Manage** to download a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="7069d-139">Parempoolses menüüs valige failiga robots.txt seostatud domeeni kõrval nupp **Laadi alla** (allapoole suunatud nool).</span><span class="sxs-lookup"><span data-stu-id="7069d-139">On the menu on the right, select the **Download** button (the downward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="7069d-140">Kuvatakse failibrauseri dialoogiboks.</span><span class="sxs-lookup"><span data-stu-id="7069d-140">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="7069d-141">Dialoogiboksis minge oma kohalikul kettal soovitud asukohta, kinnitage või sisestage faili nimi ja seejärel valige allalaadimise lõpetamiseks käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="7069d-141">In the dialog box, go to the desired location on your local drive, confirm or enter a file name, and then select **Save** to complete the download.</span></span>

> [!NOTE]
> <span data-ttu-id="7069d-142">Seda protseduuri saab kasutada ainult nende robot.txt-failide allalaadimiseks, mis olid eelnevalt üles laaditud Commerce’i autorluse tööriistade kaudu.</span><span class="sxs-lookup"><span data-stu-id="7069d-142">This procedure can be used to download only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="delete-a-robotstxt-file"></a><span data-ttu-id="7069d-143">Faili robots.txt kustutamine</span><span class="sxs-lookup"><span data-stu-id="7069d-143">Delete a robots.txt file</span></span>

<span data-ttu-id="7069d-144">Faili robots.txt Commerce’is kustutamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="7069d-144">To delete a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="7069d-145">Logige Commerce’i süsteemiadministraatorina sisse.</span><span class="sxs-lookup"><span data-stu-id="7069d-145">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="7069d-146">Valige vasakpoolsel navigeerimispaanil selle laiendamiseks suvand **Rentniku sätted** (hammasratta sümboli kõrval).</span><span class="sxs-lookup"><span data-stu-id="7069d-146">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="7069d-147">Jaotises **Rentniku sätted** valige **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="7069d-147">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="7069d-148">Akna põhiosas kuvatakse kõigi teie keskkonnaga seotud domeenide loend.</span><span class="sxs-lookup"><span data-stu-id="7069d-148">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="7069d-149">Valige käsk **Halda**, et kustutada fail robots.txt oma keskkonna domeeni jaoks.</span><span class="sxs-lookup"><span data-stu-id="7069d-149">Select **Manage** to delete a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="7069d-150">Parempoolses menüüs valige failiga robots.txt seostatud domeeni kõrval nupp **Kustuta** (prügikasti sümbol).</span><span class="sxs-lookup"><span data-stu-id="7069d-150">On the menu on the right, select the **Delete** button (the trash can symbol) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="7069d-151">Kuvatakse failibrauseri aken.</span><span class="sxs-lookup"><span data-stu-id="7069d-151">A file browser window appears.</span></span>
6. <span data-ttu-id="7069d-152">Failibrauseri aknas sirvige leidmiseks ja valige fail robots.txt, mille soovite domeeni jaoks kustutada, ja seejärel valige üleslaadimise lõpetamiseks käsk **Ava**.</span><span class="sxs-lookup"><span data-stu-id="7069d-152">In the file browser window, browse to and select the robots.txt file that you want to delete for the domain, and then select **Open**.</span></span> <span data-ttu-id="7069d-153">Kuvatakse hoiatusteate aken.</span><span class="sxs-lookup"><span data-stu-id="7069d-153">A warning message box appears.</span></span>
7. <span data-ttu-id="7069d-154">Teateaknas valige **Kustuta**, et kinitada faili robots.txt kustutamine.</span><span class="sxs-lookup"><span data-stu-id="7069d-154">In the message box, select **Delete** to confirm deletion of the robots.txt file.</span></span>

> [!NOTE] 
> <span data-ttu-id="7069d-155">Seda protseduuri saab kasutada ainult nende robot.txt-failide kustutamiseks, mis olid eelnevalt üles laaditud Commerce’i autorluse tööriistade kaudu.</span><span class="sxs-lookup"><span data-stu-id="7069d-155">This procedure can be used to delete only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="7069d-156">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="7069d-156">Additional resources</span></span>

[<span data-ttu-id="7069d-157">Domeeninime konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="7069d-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="7069d-158">Uue e-kaubanduse saidi juurutamine</span><span class="sxs-lookup"><span data-stu-id="7069d-158">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="7069d-159">Võrgupoe kanali häälestamine</span><span class="sxs-lookup"><span data-stu-id="7069d-159">Set up an online store channel</span></span>](online-stores.md)

[<span data-ttu-id="7069d-160">e-Commerce saidi loomine</span><span class="sxs-lookup"><span data-stu-id="7069d-160">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="7069d-161">Veebisaidi seostamine kanaliga</span><span class="sxs-lookup"><span data-stu-id="7069d-161">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="7069d-162">URL-i hulgiümbersuunamiste üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="7069d-162">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="7069d-163">B2C rentniku seadistus Kaubanduses</span><span class="sxs-lookup"><span data-stu-id="7069d-163">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="7069d-164">Kasutaja sisselogimiseks kohandatud lehtede seadistamine</span><span class="sxs-lookup"><span data-stu-id="7069d-164">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="7069d-165">Mitme B2C rentniku konfigureerimine Kaubanduskeskkonnas</span><span class="sxs-lookup"><span data-stu-id="7069d-165">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="7069d-166">Sisuedastusvõrgu (CDN) toe lisamine</span><span class="sxs-lookup"><span data-stu-id="7069d-166">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="7069d-167">Asukohapõhise poetuvastuse lubamine</span><span class="sxs-lookup"><span data-stu-id="7069d-167">Enable location-based store detection</span></span>](enable-store-detection.md)
