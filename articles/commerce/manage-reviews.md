---
title: Hinnangute ja arvustuste haldus
description: Selles teemas selgitatakse, kuidas hallata rakenduse Microsoft Dynamics 365 Commerce saidiehitajas hinnanguid ja arvustusi.
author: gvrmohanreddy
manager: annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-01
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0a70d0526fb2443605a6b11df3ee281d4dd12f1d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982562"
---
# <a name="manage-ratings-and-reviews"></a><span data-ttu-id="b64d5-103">Hinnangute ja arvustuste haldus</span><span class="sxs-lookup"><span data-stu-id="b64d5-103">Manage ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="b64d5-104">Selles teemas selgitatakse, kuidas hallata rakenduse Microsoft Dynamics 365 Commerce saidiehitajas hinnanguid ja arvustusi.</span><span class="sxs-lookup"><span data-stu-id="b64d5-104">This topic explains how to manage ratings and reviews in Microsoft Dynamics 365 Commerce site builder.</span></span>

## <a name="overview"></a><span data-ttu-id="b64d5-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="b64d5-105">Overview</span></span>

<span data-ttu-id="b64d5-106">Dynamics 365 Commerce kasutab Microsoft Azure’i kognitiivset teenust, et automaatselt ebasündsaid sõnu redigeerides arvustuse teksti modereerida.</span><span class="sxs-lookup"><span data-stu-id="b64d5-106">Dynamics 365 Commerce uses Microsoft Azure Cognitive Service to automatically moderate review text by redacting profane words.</span></span> <span data-ttu-id="b64d5-107">Lisaks saavad moderaatorid kasutada rakenduse Dynamics 365 Commerce saidiehitajat järgmiste käsitsi tehtavate ülesannete tegemiseks.</span><span class="sxs-lookup"><span data-stu-id="b64d5-107">In addition, moderators can use Dynamics 365 Commerce site builder to implement the following manual tasks:</span></span>

- <span data-ttu-id="b64d5-108">Arvustuste modereerimine neile vastates või need eemaldades.</span><span class="sxs-lookup"><span data-stu-id="b64d5-108">Moderate reviews by responding to them or removing them.</span></span>
- <span data-ttu-id="b64d5-109">Kliendi arvustuste eemaldamine kliendi taotlusel.</span><span class="sxs-lookup"><span data-stu-id="b64d5-109">Delete a customer's reviews at the customer's request.</span></span>
- <span data-ttu-id="b64d5-110">Kõikide toodete hinnangute ja arvustuste andmete hulgi importimine Microsoft Power BI malli, et analüüsida hinnangute ja arvustuste suundumusi.</span><span class="sxs-lookup"><span data-stu-id="b64d5-110">Bulk-import ratings and reviews data for all products into a Microsoft Power BI template, so that trends for ratings and reviews can be analyzed.</span></span>

## <a name="read-a-review"></a><span data-ttu-id="b64d5-111">Arvustuse lugemine</span><span class="sxs-lookup"><span data-stu-id="b64d5-111">Read a review</span></span> 

<span data-ttu-id="b64d5-112">Arvustuse lugemiseks rakenduse Commerce saidiehitajas toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="b64d5-112">To read to a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="b64d5-113">Avage **Avaleht \> Arvustused \> Modereerimine**.</span><span class="sxs-lookup"><span data-stu-id="b64d5-113">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="b64d5-114">Kasutage lehe üleval paremal otsinguvälja, et filtreerida kuvatavaid arvustusi toote ID, toote nime või arvustuse teksti alusel.</span><span class="sxs-lookup"><span data-stu-id="b64d5-114">Use the search field in the upper right of the page to filter the reviews that are shown by product ID, product name, or review text.</span></span>

<span data-ttu-id="b64d5-115">Täiendavad filtrid võimaldavad teil piirata arvustusi perioodi, hinnangu, kanali või mure oleku järgi (eemaldatud, vastatud või teatatud).</span><span class="sxs-lookup"><span data-stu-id="b64d5-115">Additional filters let you limit the reviews by period, rating, channel, or concern status (taken down, responded, or reported).</span></span>

![Modereerimise avaleht](media/rnr-moderation-home.png) 

## <a name="respond-to-a-review"></a><span data-ttu-id="b64d5-117">Arvustusele vastamine</span><span class="sxs-lookup"><span data-stu-id="b64d5-117">Respond to a review</span></span> 

<span data-ttu-id="b64d5-118">Mõnikord väljendavad toote ostnud kliendid rahulolu või rahulolematust või ei oska toodet kasutada.</span><span class="sxs-lookup"><span data-stu-id="b64d5-118">Sometimes, customers who purchased a product express their satisfaction or dissatisfaction, or they don't understand how to use the product.</span></span> <span data-ttu-id="b64d5-119">Moderaatorina saate sisestada arvustusele vastuse.</span><span class="sxs-lookup"><span data-stu-id="b64d5-119">As a moderator, you can post a response to a review.</span></span> <span data-ttu-id="b64d5-120">See vastus kuvatakse saidil koos arvustusega.</span><span class="sxs-lookup"><span data-stu-id="b64d5-120">This response appears together with the review on the site.</span></span> 

<span data-ttu-id="b64d5-121">Arvustusele vastamiseks rakenduse Commerce saidiehitajas toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="b64d5-121">To respond to a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="b64d5-122">Avage **Avaleht \> Arvustused \> Modereerimine**.</span><span class="sxs-lookup"><span data-stu-id="b64d5-122">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="b64d5-123">Otsige ja valige arvustus, mis vajab vastamist.</span><span class="sxs-lookup"><span data-stu-id="b64d5-123">Find and select the review that requires a response.</span></span>
1. <span data-ttu-id="b64d5-124">Parempoolsel atribuutide paanil valige suvand **Lisa vastus**.</span><span class="sxs-lookup"><span data-stu-id="b64d5-124">In the properties pane on the right, select **Add a response**.</span></span>
1. <span data-ttu-id="b64d5-125">Sisestage vastuse tekst ja nimi, mis tuleks vastajale näidata.</span><span class="sxs-lookup"><span data-stu-id="b64d5-125">Enter the response text and the name that should be shown for the responder.</span></span> <span data-ttu-id="b64d5-126">Vastaja vaikenimi on **Moderaator.**</span><span class="sxs-lookup"><span data-stu-id="b64d5-126">The default responder name is **Moderator**.</span></span>
1. <span data-ttu-id="b64d5-127">Kui olete lõpetanud, valige **Sisesta vastus**.</span><span class="sxs-lookup"><span data-stu-id="b64d5-127">When you've finished, select **Post response**.</span></span>

![Arvustusele vastamine](media/rnr-moderation-response.png) 

## <a name="take-down-a-review"></a><span data-ttu-id="b64d5-129">Arvustuse eemaldamine</span><span class="sxs-lookup"><span data-stu-id="b64d5-129">Take down a review</span></span> 

<span data-ttu-id="b64d5-130">Vahel on moderaatoritel äriliselt põhjendatud kliendi arvustused eemaldada.</span><span class="sxs-lookup"><span data-stu-id="b64d5-130">Sometimes, there is a business justification for moderators to take down customer reviews.</span></span> 

<span data-ttu-id="b64d5-131">Arvustuse eemaldamiseks rakenduse Commerce saidiehitajast toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="b64d5-131">To take down a review in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="b64d5-132">Avage **Avaleht \> Arvustused \> Modereerimine**.</span><span class="sxs-lookup"><span data-stu-id="b64d5-132">Go to **Home \> Reviews \> Moderation**.</span></span>
1. <span data-ttu-id="b64d5-133">Leidke ja valige arvustus, mis tuleb eemaldada.</span><span class="sxs-lookup"><span data-stu-id="b64d5-133">Find and select the review that must be taken down.</span></span>
1. <span data-ttu-id="b64d5-134">Valige paremal atribuudipaanil eemaldamise põhjus väljal **Arvustuse eemaldamine** ja seejärel valige suvand **Eemalda**.</span><span class="sxs-lookup"><span data-stu-id="b64d5-134">In the properties pane on the right, select a takedown reason under **Takedown Review**, and then select **Take down**.</span></span>
    
## <a name="delete-a-customers-reviews-at-the-customers-request"></a><span data-ttu-id="b64d5-135">Kliendi arvustuste eemaldamine kliendi taotlusel</span><span class="sxs-lookup"><span data-stu-id="b64d5-135">Delete a customer's reviews at the customer's request</span></span> 

<span data-ttu-id="b64d5-136">Mõnikord soovivad kliendid oma hinnangud ja arvustuste andmed e-kaubanduse veebisaitidelt jäädavalt kustutada.</span><span class="sxs-lookup"><span data-stu-id="b64d5-136">Sometimes, customers want their ratings and reviews data to be permanently deleted from an e-Commerce website.</span></span> <span data-ttu-id="b64d5-137">Moderaator, kes saab kliendilt eemaldamise taotluse, saab kliendi andmed eemaldada, kasutades läbivaatuse kustutamise funktsiooni.</span><span class="sxs-lookup"><span data-stu-id="b64d5-137">A moderator who receives a removal request from a customer can remove the customer's data by using the review deletion feature.</span></span> <span data-ttu-id="b64d5-138">Kliendiandmete otsimiseks ja kustutamiseks vajab moderaator meiliaadressi, mida klient sisselogimiseks ja arvustuste esitamiseks kasutas.</span><span class="sxs-lookup"><span data-stu-id="b64d5-138">To find and delete a customer's data, the moderator requires the email address that the customer used to sign in and provide reviews.</span></span> 

<span data-ttu-id="b64d5-139">Kliendiandmete leidmiseks ja kustutamiseks rakenduse Commerce saidiehitajas toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="b64d5-139">To find and delete customer data in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="b64d5-140">Avage **Avaleht \> Arvustused \> Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="b64d5-140">Go to **Home \> Reviews \> Delete**.</span></span>
1. <span data-ttu-id="b64d5-141">Sisestage kasti **Kasutajate otsing meiliaadressi järgi** kliendi meiliaadress ja valige seejärel käsk **Otsi**.</span><span class="sxs-lookup"><span data-stu-id="b64d5-141">In the **Search for users by email address** box, enter the customer's email address, and then select **Search**.</span></span>
1. <span data-ttu-id="b64d5-142">Kui kliendil on mis tahes arvustuste tegevusi (nt esitatud arvustused, hääletused teiste klientide arvustuste kasulikkuse kohta või kommentaarid teiste klientide arvustuste kohta), kuvatakse tulemused.</span><span class="sxs-lookup"><span data-stu-id="b64d5-142">If the customer has any review activity (for example, review submissions, votes about the helpfulness of another customer's reviews, or comments about another customer's review), the results are shown.</span></span> <span data-ttu-id="b64d5-143">Iga üksuse jaoks on nupp **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="b64d5-143">For each item, there is a **Delete** button.</span></span>
1. <span data-ttu-id="b64d5-144">Valige iga üksuse jaoks, mis tuleb kustutada, käsk **Kustuta**.</span><span class="sxs-lookup"><span data-stu-id="b64d5-144">For each item that must be deleted, select **Delete**.</span></span> <span data-ttu-id="b64d5-145">Kui teilt küsitakse kinnitust, valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="b64d5-145">When you're prompted for confirmation, select **Yes**.</span></span> 
    
![Kliendiandmete kustutamine](media/rnr-moderation-delete-reviews.png) 

> [!NOTE]
> - <span data-ttu-id="b64d5-147">Andmete süsteemist täielikuks eemaldamiseks võib kuluda kuni seitse päeva.</span><span class="sxs-lookup"><span data-stu-id="b64d5-147">It can take up to seven days for data to be completely removed from the system.</span></span> <span data-ttu-id="b64d5-148">Moderaatorid peaksid kliente sellest viivitusest teavitama.</span><span class="sxs-lookup"><span data-stu-id="b64d5-148">Moderators should notify customers about this delay.</span></span>
> - <span data-ttu-id="b64d5-149">Kui kliendid on muutnud konto sätetes oma nime, võidakse otsingutulemustes kuvada mitu üksust.</span><span class="sxs-lookup"><span data-stu-id="b64d5-149">If customers have changed their name in their account settings, multiple items might appear in the search results.</span></span> <span data-ttu-id="b64d5-150">Sel juhul peab moderaator kliendiandmete täielikuks kustutamiseks valima iga üksuse jaoks käsu **Kustuta.**</span><span class="sxs-lookup"><span data-stu-id="b64d5-150">In this case, to completely delete the customer's data, the moderator must select **Delete** for each item.</span></span> 

## <a name="download-ratings-and-reviews-data"></a><span data-ttu-id="b64d5-151">Hinnangute ja arvustuste andmete allalaadimine</span><span class="sxs-lookup"><span data-stu-id="b64d5-151">Download ratings and reviews data</span></span>

<span data-ttu-id="b64d5-152">Rakenduse Commerce saidiehitaja võimaldab moderaatoritel importida hinnangute ja arvustuste andmeid hulgi, et analüüsida nende suundumusi.</span><span class="sxs-lookup"><span data-stu-id="b64d5-152">Commerce site builder lets moderators import ratings and reviews data in bulk, so that they can analyze trends.</span></span> <span data-ttu-id="b64d5-153">Saadaval on Power BI mall, mis sisaldab põhilisi mõõdikuid.</span><span class="sxs-lookup"><span data-stu-id="b64d5-153">A Power BI template that includes basic metrics is available.</span></span> <span data-ttu-id="b64d5-154">Moderaatorid saavad kasutada seda malli, et ühendada hulgi imporditud andmed ja kuvada armatuurlaud.</span><span class="sxs-lookup"><span data-stu-id="b64d5-154">Moderators can use this template to connect bulk-imported data and view a dashboard.</span></span> <span data-ttu-id="b64d5-155">Nad ei pea looma kohandatud armatuurlauda.</span><span class="sxs-lookup"><span data-stu-id="b64d5-155">They don't have to create a custom dashboard.</span></span> <span data-ttu-id="b64d5-156">Samuti saavad moderaatorid kohandada Power BI malli, et see vastaks nende konkreetsetele vajadustele.</span><span class="sxs-lookup"><span data-stu-id="b64d5-156">Moderators can also customize the Power BI template to meet their specific needs.</span></span> 

<span data-ttu-id="b64d5-157">Arvustuste ja hinnangute andmete allalaadimiseks rakenduse Commerce saidiehitajas toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="b64d5-157">To download ratings and reviews data in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="b64d5-158">Avage **Avaleht \> Arvustused \> Aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="b64d5-158">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="b64d5-159">Valige suvand **Arvustuse andmete allalaadimine**, et laadida hinnangute ja kommentaaride andmed hulgi alla komaeraldusega väärtuste (CSV) vormingus.</span><span class="sxs-lookup"><span data-stu-id="b64d5-159">Select **Download review data** to download ratings and reviews data in bulk in comma-separated values (CSV) format.</span></span>

## <a name="view-ratings-and-reviews-trends"></a><span data-ttu-id="b64d5-160">Hinnangute ja arvustuste suundumuste vaatamine</span><span class="sxs-lookup"><span data-stu-id="b64d5-160">View ratings and reviews trends</span></span>

<span data-ttu-id="b64d5-161">Moderaatorid saavad laadida alla Power BI malli, et nad saaksid vaadata armatuurlaual suundumusi.</span><span class="sxs-lookup"><span data-stu-id="b64d5-161">Moderators can download the Power BI template so that they can view trends in a dashboard.</span></span>

<span data-ttu-id="b64d5-162">Arvustuste ja hinnangute suundumuste vaatamiseks rakenduse Commerce saidiehitajas toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="b64d5-162">To view ratings and reviews trends in Commerce site builder, follow these steps.</span></span>

1. <span data-ttu-id="b64d5-163">Avage **Avaleht \> Arvustused \> Aruandlus**.</span><span class="sxs-lookup"><span data-stu-id="b64d5-163">Go to **Home \> Reviews \> Reporting**.</span></span>
1. <span data-ttu-id="b64d5-164">Malli allalaadimiseks valige suvand **PowerBI mall**.</span><span class="sxs-lookup"><span data-stu-id="b64d5-164">Select **PowerBI template** to download the template.</span></span>

    ![Laadige alla Power BI mall](media/rnr-moderation-reports.png) 

1. <span data-ttu-id="b64d5-166">Avage allalaaditud mall Power BI rakendust kasutades.</span><span class="sxs-lookup"><span data-stu-id="b64d5-166">Open the downloaded template by using the Power BI app.</span></span> <span data-ttu-id="b64d5-167">Sulgege ilmuv dialoogiaken **Juurdepääs veebisisule** ja seejärel sulgege kuvatav tõrketeade „Värskenda”.</span><span class="sxs-lookup"><span data-stu-id="b64d5-167">Close the **Access to web content** dialog box that appears, and then close the "Refresh" error message that appears.</span></span>
1. <span data-ttu-id="b64d5-168">Avage suvand **Avaleht**, valige **Päringute redigeerimine** ja valige seejärel **Andmeallika sätted**.</span><span class="sxs-lookup"><span data-stu-id="b64d5-168">Go to **Home**, select **Edit queries**, and then select **Data source settings**.</span></span>
1. <span data-ttu-id="b64d5-169">Valige dialoogiaknas **Andmeallika sätted** suvand **Muuda allikat**.</span><span class="sxs-lookup"><span data-stu-id="b64d5-169">In the **Data source settings** dialog box, select **Change Source**.</span></span>
1. <span data-ttu-id="b64d5-170">Sisestage väljale **URL** eelmises protseduuris allalaaditud arvustuste andmete tee (nt **c:\\arvustused\\ArvustusteAndmed.CSV**).</span><span class="sxs-lookup"><span data-stu-id="b64d5-170">In the **URL** field, enter the path of the reviews data that you downloaded in the previous procedure (for example, **c:\\reviews\\ReviewsData.csv**).</span></span>

    ![URL-i väli komaeraldusega väärtuste dialoogiaknas](media/rnr-powerbi-datasource-settings.png) 

1. <span data-ttu-id="b64d5-172">Valige **OK** ja seejärel valige käsk **Rakenda muutused**.</span><span class="sxs-lookup"><span data-stu-id="b64d5-172">Select **OK**, and then select **Apply changes**.</span></span> <span data-ttu-id="b64d5-173">Andmeallikale muudatuste rakendamiseks kulub üks kuni kaks minutit.</span><span class="sxs-lookup"><span data-stu-id="b64d5-173">It will take one to two minutes to apply your changes to the data source.</span></span>
1. <span data-ttu-id="b64d5-174">Hinnangute ja arvustuste suundumuste vaatamiseks valige suvand **Suundumuste leht**.</span><span class="sxs-lookup"><span data-stu-id="b64d5-174">Select **Trends sheet** to view ratings and reviews trends.</span></span>

    ![Hinnangute ja arvustuste suundumused](media/rnr-powerbi-dashboard-template.png) 
    
## <a name="additional-resources"></a><span data-ttu-id="b64d5-176">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="b64d5-176">Additional resources</span></span>

[<span data-ttu-id="b64d5-177">Hinnangute ja arvustuste ülevaade</span><span class="sxs-lookup"><span data-stu-id="b64d5-177">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="b64d5-178">Hinnangute ja arvustuste kasutamise valimine</span><span class="sxs-lookup"><span data-stu-id="b64d5-178">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="b64d5-179">Hinnangute ja arvustuste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="b64d5-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="b64d5-180">Toote hinnangute sünkroonimine rakenduses Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="b64d5-180">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
