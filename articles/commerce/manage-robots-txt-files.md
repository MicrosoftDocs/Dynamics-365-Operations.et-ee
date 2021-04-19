---
title: Robots.txt-failide haldamine
description: See teema kirjeldab failide robots.txt haldamist teenuses Microsoft Dynamics 365 Commerce.
author: BrianShook
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2019-12-18
ms.dyn365.ops.version: ''
ms.openlocfilehash: b9b832d6714447f8957095c8c87d48527087f12d
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794231"
---
# <a name="manage-robotstxt-files"></a><span data-ttu-id="afaed-103">Robots.txt-failide haldamine</span><span class="sxs-lookup"><span data-stu-id="afaed-103">Manage robots.txt files</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="afaed-104">See teema kirjeldab failide robots.txt haldamist teenuses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="afaed-104">This topic describes how to manage robots.txt files in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="afaed-105">Robotite välistamise standard või robots.txt on standard, mida veebisaidid kasutavad veebirobotitega suhtlemiseks.</span><span class="sxs-lookup"><span data-stu-id="afaed-105">The robots exclusion standard, or robots.txt, is a standard that websites use to communicate with web robots.</span></span> <span data-ttu-id="afaed-106">See juhendab veebiroboteid veebisaidi mis tahes alade osas, mida ei tohiks külastada.</span><span class="sxs-lookup"><span data-stu-id="afaed-106">It instructs web robots about any areas of a website that should not be visited.</span></span> <span data-ttu-id="afaed-107">Roboteid kasutavad sageli otsingumootorid veebisaitide indekseerimiseks.</span><span class="sxs-lookup"><span data-stu-id="afaed-107">Robots are often used by search engines to index websites.</span></span>

<span data-ttu-id="afaed-108">Robotite serverist välistamiseks loote serveris faili.</span><span class="sxs-lookup"><span data-stu-id="afaed-108">To exclude robots from a server, you create a file on the server.</span></span> <span data-ttu-id="afaed-109">Selles failis määrate robotite juurdepääsupoliitika.</span><span class="sxs-lookup"><span data-stu-id="afaed-109">In this file, you specify an access policy for robots.</span></span> <span data-ttu-id="afaed-110">Fail peab olema HTTP kaudu juurdepääsetav kohalikul URL-il **/robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="afaed-110">The file must be accessible via HTTP at the local URL **/robots.txt**.</span></span> <span data-ttu-id="afaed-111">Fail robots.txt aitab otsingumootoritel teie saidi sisu indekseerida.</span><span class="sxs-lookup"><span data-stu-id="afaed-111">The robots.txt file helps search engines index the content on your site.</span></span>

<span data-ttu-id="afaed-112">Dynamics 365 Commerce võimaldab teil faili robots.txt oma domeenile üles laadida.</span><span class="sxs-lookup"><span data-stu-id="afaed-112">Dynamics 365 Commerce lets you upload a robots.txt file for your domain.</span></span> <span data-ttu-id="afaed-113">Iga Commerce’i keskkonna domeeni jaoks saate üles laadida ühe robots.txt-faili ja seostada selle domeeniga.</span><span class="sxs-lookup"><span data-stu-id="afaed-113">For each domain in your Commerce environment, you can upload one robots.txt file and associate it with that domain.</span></span>

<span data-ttu-id="afaed-114">Lisateavet faili robots.txt kohta leiate teemast [Veebirobotite lehed](https://www.robotstxt.org/).</span><span class="sxs-lookup"><span data-stu-id="afaed-114">For more information about the robots.txt file, visit [The Web Robots Pages](https://www.robotstxt.org/).</span></span>

## <a name="upload-a-robotstxt-file"></a><span data-ttu-id="afaed-115">Faili robots.txt üleslaadimine</span><span class="sxs-lookup"><span data-stu-id="afaed-115">Upload a robots.txt file</span></span>

<span data-ttu-id="afaed-116">Pärast seda, kui olete loonud ja redigeerinud faili robots.txt vastavalt [robotite välistamise standardile](https://www.robotstxt.org/orig.html), veenduge, et fail oleks juurdepääsetav arvutis, kus kasutate Commerce’i autorluse tööriistu.</span><span class="sxs-lookup"><span data-stu-id="afaed-116">After you've created and edited your robots.txt file according to the [robots exclusion standard](https://www.robotstxt.org/orig.html), make sure that the file is accessible on the computer where you will use the Commerce authoring tools.</span></span> <span data-ttu-id="afaed-117">Faili nimi peab olema **robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="afaed-117">The file must be named **robots.txt**.</span></span> <span data-ttu-id="afaed-118">Parimate tulemuste saavutamiseks peab see olema standardis märgitud vormingus.</span><span class="sxs-lookup"><span data-stu-id="afaed-118">For best results, it must be in the format that is noted in the standard.</span></span> <span data-ttu-id="afaed-119">Iga Commerce’i klient vastutab oma robots.txt-faili sisu valideerimise ja haldamise eest.</span><span class="sxs-lookup"><span data-stu-id="afaed-119">Each Commerce customer is responsible for validating and maintaining the contents of its robots.txt file.</span></span> <span data-ttu-id="afaed-120">Faili robots.txt üleslaadimiseks peate olema Commerce’i süsteemiadministraatorina sisse logitud.</span><span class="sxs-lookup"><span data-stu-id="afaed-120">To upload a robots.txt file, you must be signed in to Commerce as a system admin.</span></span>

<span data-ttu-id="afaed-121">Faili robots.txt Commerce’is üleslaadimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="afaed-121">To upload a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="afaed-122">Logige Commerce’i süsteemiadministraatorina sisse.</span><span class="sxs-lookup"><span data-stu-id="afaed-122">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="afaed-123">Valige vasakpoolsel navigeerimispaanil selle laiendamiseks suvand **Rentniku sätted** (hammasratta sümboli kõrval).</span><span class="sxs-lookup"><span data-stu-id="afaed-123">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="afaed-124">Jaotises **Rentniku sätted** valige **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="afaed-124">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="afaed-125">Akna põhiosas kuvatakse kõigi teie keskkonnaga seotud domeenide loend.</span><span class="sxs-lookup"><span data-stu-id="afaed-125">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="afaed-126">Valige käsk **Halda**, et laadida fail robots.txt oma keskkonna domeeni jaoks üles.</span><span class="sxs-lookup"><span data-stu-id="afaed-126">Select **Manage** to upload a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="afaed-127">Parempoolses menüüs valige failiga robots.txt seostatud domeeni kõrval nupp **Laadi üles** (ülespoole suunatud nool).</span><span class="sxs-lookup"><span data-stu-id="afaed-127">On the menu on the right, select the **Upload** button (the upward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="afaed-128">Kuvatakse failibrauseri dialoogiboks.</span><span class="sxs-lookup"><span data-stu-id="afaed-128">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="afaed-129">Dialoogiboksis sirvige leidmiseks ja valige fail robots.txt, mille soovite seotud domeeni jaoks üles laadida, ja seejärel valige üleslaadimise lõpetamiseks käsk **Ava**.</span><span class="sxs-lookup"><span data-stu-id="afaed-129">In the dialog box, browse to and select the robots.txt file that you want to upload for the associated domain, and then select **Open** to complete the upload.</span></span>

> [!NOTE] 
> <span data-ttu-id="afaed-130">Üleslaadimise ajal kontrollib Commerce, kas fail on tekstifail, kuid see ei valideeri faili sisu.</span><span class="sxs-lookup"><span data-stu-id="afaed-130">During upload, Commerce verifies that the file is a text file, but it doesn't validate the file's contents.</span></span>

## <a name="download-a-robotstxt-file"></a><span data-ttu-id="afaed-131">Faili robots.txt allalaadimine</span><span class="sxs-lookup"><span data-stu-id="afaed-131">Download a robots.txt file</span></span>

<span data-ttu-id="afaed-132">Faili robots.txt Commerce’is allalaadimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="afaed-132">To download a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="afaed-133">Logige Commerce’i süsteemiadministraatorina sisse.</span><span class="sxs-lookup"><span data-stu-id="afaed-133">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="afaed-134">Valige vasakpoolsel navigeerimispaanil selle laiendamiseks suvand **Rentniku sätted** (hammasratta sümboli kõrval).</span><span class="sxs-lookup"><span data-stu-id="afaed-134">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="afaed-135">Jaotises **Rentniku sätted** valige **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="afaed-135">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="afaed-136">Akna põhiosas kuvatakse kõigi teie keskkonnaga seotud domeenide loend.</span><span class="sxs-lookup"><span data-stu-id="afaed-136">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="afaed-137">Valige käsk **Halda**, et laadida fail robots.txt oma keskkonna domeeni jaoks alla.</span><span class="sxs-lookup"><span data-stu-id="afaed-137">Select **Manage** to download a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="afaed-138">Parempoolses menüüs valige failiga robots.txt seostatud domeeni kõrval nupp **Laadi alla** (allapoole suunatud nool).</span><span class="sxs-lookup"><span data-stu-id="afaed-138">On the menu on the right, select the **Download** button (the downward-pointing arrow) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="afaed-139">Kuvatakse failibrauseri dialoogiboks.</span><span class="sxs-lookup"><span data-stu-id="afaed-139">A file browser dialog box appears.</span></span>
6. <span data-ttu-id="afaed-140">Dialoogiboksis minge oma kohalikul kettal soovitud asukohta, kinnitage või sisestage faili nimi ja seejärel valige allalaadimise lõpetamiseks käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="afaed-140">In the dialog box, go to the desired location on your local drive, confirm or enter a file name, and then select **Save** to complete the download.</span></span>

> [!NOTE]
> <span data-ttu-id="afaed-141">Seda protseduuri saab kasutada ainult nende robot.txt-failide allalaadimiseks, mis olid eelnevalt üles laaditud Commerce’i autorluse tööriistade kaudu.</span><span class="sxs-lookup"><span data-stu-id="afaed-141">This procedure can be used to download only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="delete-a-robotstxt-file"></a><span data-ttu-id="afaed-142">Faili robots.txt kustutamine</span><span class="sxs-lookup"><span data-stu-id="afaed-142">Delete a robots.txt file</span></span>

<span data-ttu-id="afaed-143">Faili robots.txt Commerce’is kustutamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="afaed-143">To delete a robots.txt file in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="afaed-144">Logige Commerce’i süsteemiadministraatorina sisse.</span><span class="sxs-lookup"><span data-stu-id="afaed-144">Sign in to Commerce as a system admin.</span></span>
2. <span data-ttu-id="afaed-145">Valige vasakpoolsel navigeerimispaanil selle laiendamiseks suvand **Rentniku sätted** (hammasratta sümboli kõrval).</span><span class="sxs-lookup"><span data-stu-id="afaed-145">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
3. <span data-ttu-id="afaed-146">Jaotises **Rentniku sätted** valige **Robots.txt**.</span><span class="sxs-lookup"><span data-stu-id="afaed-146">Under **Tenant Settings**, select **Robots.txt**.</span></span> <span data-ttu-id="afaed-147">Akna põhiosas kuvatakse kõigi teie keskkonnaga seotud domeenide loend.</span><span class="sxs-lookup"><span data-stu-id="afaed-147">A list of all the domains that are associated with your environment appears in the main part of the window.</span></span>
4. <span data-ttu-id="afaed-148">Valige käsk **Halda**, et kustutada fail robots.txt oma keskkonna domeeni jaoks.</span><span class="sxs-lookup"><span data-stu-id="afaed-148">Select **Manage** to delete a robots.txt file for a domain in your environment.</span></span>
5. <span data-ttu-id="afaed-149">Parempoolses menüüs valige failiga robots.txt seostatud domeeni kõrval nupp **Kustuta** (prügikasti sümbol).</span><span class="sxs-lookup"><span data-stu-id="afaed-149">On the menu on the right, select the **Delete** button (the trash can symbol) next to the domain that is associated with the robots.txt file.</span></span> <span data-ttu-id="afaed-150">Kuvatakse failibrauseri aken.</span><span class="sxs-lookup"><span data-stu-id="afaed-150">A file browser window appears.</span></span>
6. <span data-ttu-id="afaed-151">Failibrauseri aknas sirvige leidmiseks ja valige fail robots.txt, mille soovite domeeni jaoks kustutada, ja seejärel valige üleslaadimise lõpetamiseks käsk **Ava**.</span><span class="sxs-lookup"><span data-stu-id="afaed-151">In the file browser window, browse to and select the robots.txt file that you want to delete for the domain, and then select **Open**.</span></span> <span data-ttu-id="afaed-152">Kuvatakse hoiatusteate aken.</span><span class="sxs-lookup"><span data-stu-id="afaed-152">A warning message box appears.</span></span>
7. <span data-ttu-id="afaed-153">Teateaknas valige **Kustuta**, et kinitada faili robots.txt kustutamine.</span><span class="sxs-lookup"><span data-stu-id="afaed-153">In the message box, select **Delete** to confirm deletion of the robots.txt file.</span></span>

> [!NOTE] 
> <span data-ttu-id="afaed-154">Seda protseduuri saab kasutada ainult nende robot.txt-failide kustutamiseks, mis olid eelnevalt üles laaditud Commerce’i autorluse tööriistade kaudu.</span><span class="sxs-lookup"><span data-stu-id="afaed-154">This procedure can be used to delete only robots.txt files that were previously uploaded via the Commerce authoring tools.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="afaed-155">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="afaed-155">Additional resources</span></span>

[<span data-ttu-id="afaed-156">Domeeninime konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="afaed-156">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="afaed-157">Uue e-kaubanduse rentniku juurutamine</span><span class="sxs-lookup"><span data-stu-id="afaed-157">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="afaed-158">E-kaubanduse saidi loomine</span><span class="sxs-lookup"><span data-stu-id="afaed-158">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="afaed-159">Dynamics 365 Commerce'i saidi seostamine võrgukanaliga</span><span class="sxs-lookup"><span data-stu-id="afaed-159">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="afaed-160">Üleslaadimise URL suunab ümber hulgi</span><span class="sxs-lookup"><span data-stu-id="afaed-160">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="afaed-161">B2C-rentniku häälestus Commerce'is</span><span class="sxs-lookup"><span data-stu-id="afaed-161">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="afaed-162">Kasutaja sisselogimiseks kohandatud lehtede seadistamine</span><span class="sxs-lookup"><span data-stu-id="afaed-162">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="afaed-163">Mitme B2C rentniku konfigureerimine Kaubanduskeskkonnas</span><span class="sxs-lookup"><span data-stu-id="afaed-163">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="afaed-164">Sisuedastusvõrgu (CDN) toe lisamine</span><span class="sxs-lookup"><span data-stu-id="afaed-164">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="afaed-165">Asukohapõhise poetuvastuse lubamine</span><span class="sxs-lookup"><span data-stu-id="afaed-165">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
