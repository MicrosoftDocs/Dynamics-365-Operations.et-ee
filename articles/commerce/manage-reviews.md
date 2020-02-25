---
title: Hinnangute ja arvustuste haldus
description: Selles teemas selgitatakse, kuidas rakenduse Microsoft Dynamics 365 Commerce hinnangute ja arvustuste modereerimise tööriista kasutades hallata hinnanguid ja arvustusi.
author: gvrmohanreddy
manager: annbe
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a7fa2ae3124a0a68b3890987c5dce2730e5c2183
ms.sourcegitcommit: 1e6c8163da5818196769eb278afb3a2335d0cbe3
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/05/2020
ms.locfileid: "3027238"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="47674-103">Hinnangute ja arvustuste haldus</span><span class="sxs-lookup"><span data-stu-id="47674-103">Manage ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="47674-104">Selles teemas selgitatakse, kuidas rakenduse Microsoft Dynamics 365 Commerce hinnangute ja arvustuste modereerimise tööriista kasutades hallata hinnanguid ja arvustusi.</span><span class="sxs-lookup"><span data-stu-id="47674-104">This topic explains how to manage ratings and reviews by using the Microsoft Dynamics 365 Commerce ratings and reviews moderation tool.</span></span>

## <a name="overview"></a><span data-ttu-id="47674-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="47674-105">Overview</span></span>

<span data-ttu-id="47674-106">Dynamics 365 Commerce kasutab Microsoft Azure’i kognitiivset teenust, et automaatselt ebasündsaid sõnu redigeerides arvustuse teksti modereerida.</span><span class="sxs-lookup"><span data-stu-id="47674-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="47674-107">Lisaks saavad moderaatorid kasutada hinnangute ja arvustuste modereerimise tööriista järgmiste käsitsi ülesannete jaoks.</span><span class="sxs-lookup"><span data-stu-id="47674-107">In addition, moderators can use the ratings and reviews moderation tool for the following manual tasks:</span></span>

- <span data-ttu-id="47674-108">Arvustuste modereerimine neile vastates või need eemaldades.</span><span class="sxs-lookup"><span data-stu-id="47674-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="47674-109">Kliendi arvustuste eemaldamine kliendi taotlusel.</span><span class="sxs-lookup"><span data-stu-id="47674-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="47674-110">Kõikide toodete hinnangute ja arvustuste andmete hulgi importimine Microsoft Power BI malli, et analüüsida hinnangute ja arvustuste suundumusi.</span><span class="sxs-lookup"><span data-stu-id="47674-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="access-ratings-and-reviews-moderation-features"></a><span data-ttu-id="47674-111">Juurdepääs hinnangute ja arvustuste modereerimisfunktsioonidele</span><span class="sxs-lookup"><span data-stu-id="47674-111">Access ratings and reviews moderation features</span></span>

<span data-ttu-id="47674-112">E-kaubanduse saidi haldustööriistas hinnangute ja arvustuste modereerimisfunktsioonidele juurdepääsuks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="47674-112">To access ratings and reviews moderation features in the e-Commerce site management tool, follow these steps.</span></span>

1. <span data-ttu-id="47674-113">Logige sisse [teenusesse Microsoft Lifecycle Services (LCS)](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="47674-113">Sign in to [Microsoft Lifecycle Services (LCS)](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="47674-114">Avage projekt, mis sisaldab keskkonda, kus soovite e-kaubandust lähtestada.</span><span class="sxs-lookup"><span data-stu-id="47674-114">Open the project that contains the environment where you want to initialize e-Commerce.</span></span>
1. <span data-ttu-id="47674-115">Jaotises **Keskkond** valige keskkond.</span><span class="sxs-lookup"><span data-stu-id="47674-115">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="47674-116">Jaotises **Keskkonna funktsioonid** valige käsk **Jaemüügi haldus**.</span><span class="sxs-lookup"><span data-stu-id="47674-116">Under **Environment features**, select **Retail manage**.</span></span>
1. <span data-ttu-id="47674-117">Vahekaardil **e-Commerce** jaotises **Lingid** valige suvand \***E-kaubanduse saidi haldustööriist**.</span><span class="sxs-lookup"><span data-stu-id="47674-117">On the **e-Commerce** tab under **Links**, select **e-Commerce Site management tool**.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="47674-118">Arvustuse lugemine</span><span class="sxs-lookup"><span data-stu-id="47674-118">Read a review</span></span> 

1. <span data-ttu-id="47674-119">Avage **Avaleht \> Arvustused \> Modereerimine**.</span><span class="sxs-lookup"><span data-stu-id="47674-119">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="47674-120">Kasutage lehe üleval paremal otsinguvälja, et filtreerida kuvatavaid arvustusi toote ID, toote nime või arvustuse teksti alusel.</span><span class="sxs-lookup"><span data-stu-id="47674-120">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="47674-121">Täiendavad filtrid võimaldavad teil piirata arvustusi perioodi, hinnangu, kanali või mure oleku järgi (eemaldatud, vastatud või teatatud).</span><span class="sxs-lookup"><span data-stu-id="47674-121">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![Modereerimise avaleht](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="47674-123">Arvustusele vastamine</span><span class="sxs-lookup"><span data-stu-id="47674-123">Respond to a review</span></span> 

<span data-ttu-id="47674-124">Mõnikord väljendavad toote ostnud kliendid rahulolu või rahulolematust või ei oska toodet kasutada.</span><span class="sxs-lookup"><span data-stu-id="47674-124">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="47674-125">Moderaatorina saate sisestada arvustusele vastuse.</span><span class="sxs-lookup"><span data-stu-id="47674-125">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="47674-126">See vastus kuvatakse saidil koos arvustusega.</span><span class="sxs-lookup"><span data-stu-id="47674-126">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="47674-127">Arvustusele vastamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="47674-127">To respond to a review, follow these steps.</span></span>

1. <span data-ttu-id="47674-128">Avage **Avaleht \> Arvustused \> Modereerimine**.</span><span class="sxs-lookup"><span data-stu-id="47674-128">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="47674-129">Otsige ja valige arvustus, mis vajab vastamist.</span><span class="sxs-lookup"><span data-stu-id="47674-129">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="47674-130">Parempoolsel atribuutide paanil valige suvand **Lisa vastus**.</span><span class="sxs-lookup"><span data-stu-id="47674-130">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="47674-131">Sisestage vastuse tekst ja nimi, mis tuleks vastajale näidata.</span><span class="sxs-lookup"><span data-stu-id="47674-131">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="47674-132">Vastaja vaikenimi on **Moderaator.**</span><span class="sxs-lookup"><span data-stu-id="47674-132">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="47674-133">Kui olete lõpetanud, valige **Sisesta vastus**.</span><span class="sxs-lookup"><span data-stu-id="47674-133">When you've finished, select **Post response**.</span></span>

![Arvustusele vastamine](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="47674-135">Arvustuse eemaldamine</span><span class="sxs-lookup"><span data-stu-id="47674-135">Take down a review</span></span> 

<span data-ttu-id="47674-136">Vahel on moderaatoritel äriliselt põhjendatud kliendi arvustused eemaldada.</span><span class="sxs-lookup"><span data-stu-id="47674-136">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="47674-137">Arvustusele eemaldamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="47674-137">To take down a review, follow these steps.</span></span>

1. <span data-ttu-id="47674-138">Avage **Avaleht \> Arvustused \> Modereerimine**.</span><span class="sxs-lookup"><span data-stu-id="47674-138">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="47674-139">Leidke ja valige arvustus, mis tuleb eemaldada.</span><span class="sxs-lookup"><span data-stu-id="47674-139">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="47674-140">Valige paremal atribuutide paanil eemaldamise põhjus ja seejärel valige suvand **Eemalda**.</span><span class="sxs-lookup"><span data-stu-id="47674-140">In the properties pane on the right, select a takedown reason, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="47674-141">Kliendi arvustuste eemaldamine kliendi taotlusel</span><span class="sxs-lookup"><span data-stu-id="47674-141">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="47674-142">Mõnikord soovivad kliendid oma hinnangud ja arvustuste andmed e-kaubanduse veebisaitidelt jäädavalt kustutada.</span><span class="sxs-lookup"><span data-stu-id="47674-142">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="47674-143">Moderaator, kes saab kliendilt eemaldamise taotluse, saab kliendi andmed eemaldada, kasutades läbivaatuse kustutamise funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="47674-143">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="47674-144">Kliendiandmete otsimiseks ja kustutamiseks vajab moderaator meiliaadressi, mida klient sisselogimiseks ja arvustuste esitamiseks kasutas.</span><span class="sxs-lookup"><span data-stu-id="47674-144">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="47674-145">Kliendiandmete otsimiseks ja kustutamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="47674-145">To find and delete customer data, follow these steps.</span></span>

1. <span data-ttu-id="47674-146">Avage **Avaleht \> Arvustused \> Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="47674-146">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="47674-147">Sisestage väljale **Kasutajate otsing meiliaadressi järgi** kliendi meiliaadress ja valige seejärel käsk **Otsi**.</span><span class="sxs-lookup"><span data-stu-id="47674-147">In the **Search for users by email address** field, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="47674-148">Kui kliendil on mis tahes arvustuste tegevusi (nt esitatud arvustused, hääletused teiste klientide arvustuste kasulikkuse kohta või kommentaarid teiste klientide arvustuste kohta), kuvatakse tulemused.</span><span class="sxs-lookup"><span data-stu-id="47674-148">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="47674-149">Iga üksuse jaoks on nupp **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="47674-149">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="47674-150">Valige iga üksuse jaoks, mis tuleb kustutada, käsk **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="47674-150">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="47674-151">Kui teilt küsitakse kinnitust, valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="47674-151">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![Kliendiandmete kustutamine](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="47674-153">Andmete süsteemist täielikuks eemaldamiseks võib kuluda kuni seitse päeva.</span><span class="sxs-lookup"><span data-stu-id="47674-153">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="47674-154">Moderaatorid peaksid kliente sellest viivitusest teavitama.</span><span class="sxs-lookup"><span data-stu-id="47674-154">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="47674-155">Kui kliendid on muutnud konto sätetes oma nime, võidakse otsingutulemustes kuvada mitu üksust.</span><span class="sxs-lookup"><span data-stu-id="47674-155">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="47674-156">Sel juhul peab moderaator kliendiandmete täielikuks kustutamiseks valima iga üksuse jaoks käsu **Kustuta.**</span><span class="sxs-lookup"><span data-stu-id="47674-156">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="47674-157">Hinnangute ja arvustuste andmete allalaadimine</span><span class="sxs-lookup"><span data-stu-id="47674-157">Download ratings and reviews data</span></span>

<span data-ttu-id="47674-158">Hinnangute ja arvustuste modereerimise tööriist võimaldab moderaatoritel importida hinnangute ja arvustuste andmeid hulgi, et analüüsida nende suundumusi.</span><span class="sxs-lookup"><span data-stu-id="47674-158">The ratings and reviews moderation tool lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="47674-159">Saadaval on Power BI mall, mis sisaldab põhilisi mõõdikuid.</span><span class="sxs-lookup"><span data-stu-id="47674-159">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="47674-160">Moderaatorid saavad kasutada seda malli, et ühendada hulgi imporditud andmed ja kuvada armatuurlaud.</span><span class="sxs-lookup"><span data-stu-id="47674-160">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="47674-161">Nad ei pea looma kohandatud armatuurlauda.</span><span class="sxs-lookup"><span data-stu-id="47674-161">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="47674-162">Samuti saavad moderaatorid kohandada Power BI malli, et see vastaks nende konkreetsetele vajadustele.</span><span class="sxs-lookup"><span data-stu-id="47674-162">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="47674-163">Hinnangute ja arvustuste andmete allalaadimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="47674-163">To download ratings and reviews data, follow these steps.</span></span>

1. <span data-ttu-id="47674-164">Avage **Avaleht \> Arvustused \> Aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="47674-164">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="47674-165">Valige suvand **Aruandluse andmete allalaadimine**, et laadida hinnangute ja kommentaaride andmed hulgi alla komaeraldusega väärtuste (CSV) vormingus.</span><span class="sxs-lookup"><span data-stu-id="47674-165">Select **Download reviews data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="47674-166">Hinnangute ja arvustuste suundumuste vaatamine</span><span class="sxs-lookup"><span data-stu-id="47674-166">View ratings and reviews trends</span></span>

<span data-ttu-id="47674-167">Moderaatorid saavad laadida alla Power BI malli, et nad saaksid vaadata armatuurlaual suundumusi.</span><span class="sxs-lookup"><span data-stu-id="47674-167">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="47674-168">Hinnangute ja arvustuste suundumuste vaatamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="47674-168">To view ratings and reviews trends, follow these steps.</span></span>

1. <span data-ttu-id="47674-169">Avage **Avaleht \> Arvustused \> Aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="47674-169">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="47674-170">Malli allalaadimiseks valige suvand **PowerBI mall**.</span><span class="sxs-lookup"><span data-stu-id="47674-170">Select **PowerBI template** to download the template.</span></span>

    ![Power BI malli allalaadimine](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="47674-172">Avage allalaaditud mall Power BI rakendust kasutades.</span><span class="sxs-lookup"><span data-stu-id="47674-172">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="47674-173">Sulgege ilmuv dialoogiaken **Juurdepääs veebisisule** ja seejärel sulgege kuvatav tõrketeade „Värskenda”.</span><span class="sxs-lookup"><span data-stu-id="47674-173">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="47674-174">Avage suvand **Avaleht**, valige **Päringute redigeerimine** ja valige seejärel **Andmeallika sätted**.</span><span class="sxs-lookup"><span data-stu-id="47674-174">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="47674-175">Valige dialoogiaknas **Andmeallika sätted** suvand **Muuda allikat**.</span><span class="sxs-lookup"><span data-stu-id="47674-175">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="47674-176">Sisestage väljale **URL** eelmises protseduuris allalaaditud arvustuste andmete tee (nt **c:\\arvustused\\ArvustusteAndmed.CSV**).</span><span class="sxs-lookup"><span data-stu-id="47674-176">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![URL-i väli komaeraldusega väärtuste dialoogiaknas](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="47674-178">Valige **OK** ja seejärel valige käsk **Rakenda muutused**.</span><span class="sxs-lookup"><span data-stu-id="47674-178">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="47674-179">Andmeallikale muudatuste rakendamiseks kulub üks kuni kaks minutit.</span><span class="sxs-lookup"><span data-stu-id="47674-179">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="47674-180">Hinnangute ja arvustuste suundumuste vaatamiseks valige suvand **Suundumuste leht**.</span><span class="sxs-lookup"><span data-stu-id="47674-180">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![Hinnangute ja arvustuste suundumused](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="47674-182">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="47674-182">Additional resources</span></span>

[<span data-ttu-id="47674-183">Hinnangute ja arvustuste ülevaade</span><span class="sxs-lookup"><span data-stu-id="47674-183">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="47674-184">Hinnangute ja arvustuste kasutamise valimine</span><span class="sxs-lookup"><span data-stu-id="47674-184">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="47674-185">Hinnangute ja arvustuste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="47674-185">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="47674-186">Toote hinnangute sünkroonimine rakenduses Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="47674-186">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
