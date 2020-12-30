---
title: Toote hinnangute sünkroonimine Dynamics 365 Commerceis
description: Selles teemas kirjeldatakse, kuidas sünkroonida tootehinnanguid rakenduses Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: dec87b548f3a218e1f833b752305f373e893b14c
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411741"
---
# <a name="sync-product-ratings-in-dynamics-365-commerce"></a><span data-ttu-id="2e176-103">Toote hinnangute sünkroonimine Dynamics 365 Commerceis</span><span class="sxs-lookup"><span data-stu-id="2e176-103">Sync product ratings in Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="2e176-104">Selles teemas kirjeldatakse, kuidas sünkroonida tootehinnanguid rakenduses Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="2e176-104">This topic describes how to sync product ratings in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="2e176-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="2e176-105">Overview</span></span>

<span data-ttu-id="2e176-106">Tootehinnangute kasutamiseks omnikanalis, nt kassas (POS) ja kõnekeskustes, tuleb tootehinnangud hinnangute ja arvustuste teenusest importida Commerce’i kanali andmebaasi.</span><span class="sxs-lookup"><span data-stu-id="2e176-106">To consume product ratings in omnichannels, such as at the point of sale (POS) and in call centers, product ratings from the ratings and reviews service must be imported into the Commerce channel database.</span></span> <span data-ttu-id="2e176-107">Kui tootehinnangud omnikanalites saadavaks tehakse, aitavad need kliente kaudselt suhtluses müüjatega.</span><span class="sxs-lookup"><span data-stu-id="2e176-107">When product ratings are made available in omnichannels, they can help customers indirectly during their interactions with sales associates.</span></span>

<span data-ttu-id="2e176-108">Selles teemas kirjeldatakse järgmisi toiminguid.</span><span class="sxs-lookup"><span data-stu-id="2e176-108">This topic describes following tasks:</span></span>

1. <span data-ttu-id="2e176-109">Konfigureerige suvand **Tootehinnangute sünkroonimise töö** pakett-tööna, et sünkroonida tootehinnangud suvandist **Hinnangute ja arvustuste teenus**.</span><span class="sxs-lookup"><span data-stu-id="2e176-109">Configure **Product ratings sync job** as a batch job to synchronize product ratings from the **Ratings and Reviews service**.</span></span>
1. <span data-ttu-id="2e176-110">Kontrollimine, kas tootehinnangute sünkroonimise pakett-töö õnnestus.</span><span class="sxs-lookup"><span data-stu-id="2e176-110">Verify that the batch job for product rating synchronization was successful.</span></span>
1. <span data-ttu-id="2e176-111">Tootehinnangute muutmine kassas kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="2e176-111">Make product ratings available at the POS.</span></span>

## <a name="configure-a-batch-job-to-synchronize-product-ratings"></a><span data-ttu-id="2e176-112">Pakett-töö konfigureerimine tootehinnangute sünkroonimiseks</span><span class="sxs-lookup"><span data-stu-id="2e176-112">Configure a batch job to synchronize product ratings</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2e176-113">Enne alustamist veenduge, et installitud oleks rakenduse Dynamics 365 Commerce versioon 10.0.6 või uuem.</span><span class="sxs-lookup"><span data-stu-id="2e176-113">Before you start, make sure that version 10.0.6 or later of Dynamics 365 Commerce is installed.</span></span>

### <a name="initialize-the-commerce-scheduler"></a><span data-ttu-id="2e176-114">Kaubanduse ajasti lähtestamine</span><span class="sxs-lookup"><span data-stu-id="2e176-114">Initialize the commerce scheduler</span></span>

<span data-ttu-id="2e176-115">Kaubanduse ajasti lähtestamiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="2e176-115">To initialize the commerce scheduler, follow these steps.</span></span>

1. <span data-ttu-id="2e176-116">Avage **Jaemüük ja kaubandus \> Peakontori seadistamine \> Kaubanduse ajasti \> Kaubanduse ajasti lähtestamine**.</span><span class="sxs-lookup"><span data-stu-id="2e176-116">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Initialize commerce scheduler**.</span></span> <span data-ttu-id="2e176-117">Võite ka sisestada otsingu „Kaubanduse ajasti lähtestamine”.</span><span class="sxs-lookup"><span data-stu-id="2e176-117">Alternatively, search for "Initialize commerce scheduler."</span></span>
1. <span data-ttu-id="2e176-118">Dialoogiboksis **Kaubanduse ajasti lähtestamine** veenduge, et suvand **Kustuta olemasolev konfiguratsioon** oleks määratud valikule **Ei** ja seejärel valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="2e176-118">In the **Initialize commerce scheduler** dialog box, make sure that the **Delete existing configuration** option is set to **No**, and then select **OK**.</span></span>

### <a name="verify-the-retailproductrating-subjob"></a><span data-ttu-id="2e176-119">Alamtöö RetailProductRating kontrollimine</span><span class="sxs-lookup"><span data-stu-id="2e176-119">Verify the RetailProductRating subjob</span></span>

<span data-ttu-id="2e176-120">Selleks et kontrollida, kas alamtöö **RetailProductRating** on olemas, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="2e176-120">To verify that the **RetailProductRating** subjob exists, follow these steps.</span></span>

1. <span data-ttu-id="2e176-121">Avage **Jaemüük ja kaubandus \> Peakontori seadistamine \> Kaubanduse ajasti \> Ajasti alamtööd**.</span><span class="sxs-lookup"><span data-stu-id="2e176-121">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Scheduler subjobs**.</span></span> <span data-ttu-id="2e176-122">Võite ka sisestada otsingu „Andmeedastaja alamtööd”.</span><span class="sxs-lookup"><span data-stu-id="2e176-122">Alternatively, search for "Scheduler subjobs."</span></span>
1. <span data-ttu-id="2e176-123">Alamtööde loendist otsige alamtööd **RetailProductRating**.</span><span class="sxs-lookup"><span data-stu-id="2e176-123">In the subjob list, find or search for the **RetailProductRating** subjob.</span></span>

<span data-ttu-id="2e176-124">Järgmisel joonisel on näha alamtöö üksikasjade näide rakenduses Commerce.</span><span class="sxs-lookup"><span data-stu-id="2e176-124">The following illustration shows an example of the subjob details in Commerce.</span></span>

![Alamtöö RetailProductRating üksikasjad](media/rnr-hq-ratings-sub-job.png)

> [!NOTE]
> <span data-ttu-id="2e176-126">Kui te ei leia alamtööd **RetailProductRating**, on võimalik, et olete enne kaubanduse ajasi lähtestamist juba käitanud töö **Tootehinnangute sünkroonimine** ja töö **1040 CDX**.</span><span class="sxs-lookup"><span data-stu-id="2e176-126">If you don't find the **RetailProductRating** subjob, you might already have run the **Sync product ratings** job and the **1040 CDX** job before you initialized the Commerce scheduler.</span></span> <span data-ttu-id="2e176-127">Sellisel juhul tehke töö **Andmete täielik sünkroonimine** käitamiseks järgmist.</span><span class="sxs-lookup"><span data-stu-id="2e176-127">In this case, follow these steps to run the **Full data sync** job.</span></span>

> 1. <span data-ttu-id="2e176-128">Avage **Jaemüük ja kaubandus \> Peakontori seadistamine \> Kaubanduse ajasti \> Kanali andmebaas**.</span><span class="sxs-lookup"><span data-stu-id="2e176-128">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span> <span data-ttu-id="2e176-129">Võite ka sisestada otsingu „Kanali andmebaas”.</span><span class="sxs-lookup"><span data-stu-id="2e176-129">Alternatively, search for "Channel database."</span></span>
> 1. <span data-ttu-id="2e176-130">Valige sünkroonimiseks kanali andmebaas.</span><span class="sxs-lookup"><span data-stu-id="2e176-130">Select the channel database to sync.</span></span>
> 1. <span data-ttu-id="2e176-131">Valige tegumiribal suvand **Andmete täielik sünkroonimine**.</span><span class="sxs-lookup"><span data-stu-id="2e176-131">On the action pane, select **Full data sync**.</span></span>
> 1. <span data-ttu-id="2e176-132">Valige rippmenüü dialoogiboksis **Jaotusgraafiku valimine** suvand **1040 – tooted** ja seejärel valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="2e176-132">In the **Select a distribution schedule** drop-down dialog box, select **1040 - products**, and then select **OK**.</span></span>
> 1. <span data-ttu-id="2e176-133">Korrake eelmise protseduuri etappe, et kontrollida, kas alamtöö **RetailProductRating** on loodud.</span><span class="sxs-lookup"><span data-stu-id="2e176-133">Repeat the steps of the previous procedure to verify that the **RetailProductRating** subjob has been created.</span></span>

### <a name="import-product-ratings"></a><span data-ttu-id="2e176-134">Tootehinnangute importimine</span><span class="sxs-lookup"><span data-stu-id="2e176-134">Import product ratings</span></span>

<span data-ttu-id="2e176-135">Tootehinnangute importimiseks Commerce’i hinnangute ja arvustuste teenusest tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="2e176-135">To import product ratings into Commerce from the ratings and reviews service, follow these steps.</span></span>

1. <span data-ttu-id="2e176-136">Valige suvandid **Jaemüük ja kaubandus \> Kaupluse haldus \> Kaubanduse ajasti \> Tootehinnangute töö sünkroonimine**.</span><span class="sxs-lookup"><span data-stu-id="2e176-136">Go to **Retail and Commerce \> Headquarters setup \> Commerce scheduler \> Sync product ratings job**.</span></span> <span data-ttu-id="2e176-137">Võite ka sisestada otsingu „Tootehinnangute töö sünkroonimine”.</span><span class="sxs-lookup"><span data-stu-id="2e176-137">Alternatively, search for "Sync product ratings job."</span></span>
1. <span data-ttu-id="2e176-138">Dialoogiboksist **Tootehinnangute tõmbamine** kiirkaardil **Käivita taustal** valige suvand **Kordumine**.</span><span class="sxs-lookup"><span data-stu-id="2e176-138">In the **Pull product ratings** dialog box, on the **Run in the background** FastTab, select **Recurrence**.</span></span>
1. <span data-ttu-id="2e176-139">Seadistage dialoogiboksis **Kordumise määratlemine** kordumismuster.</span><span class="sxs-lookup"><span data-stu-id="2e176-139">In the **Define recurrence** dialog box, set up a recurrence pattern.</span></span> <span data-ttu-id="2e176-140">(Soovitatud väärtus on kaks tundi.) Ärge määrake kordumist, mis on vähem kui kaks tundi.</span><span class="sxs-lookup"><span data-stu-id="2e176-140">(The suggested value is two hours.) Don't schedule a recurrence that is less than one hour.</span></span>
1. <span data-ttu-id="2e176-141">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="2e176-141">Select **OK**.</span></span>
1. <span data-ttu-id="2e176-142">Määrake suvandi **Pakktöötlus** väärtuseks **Jah**.</span><span class="sxs-lookup"><span data-stu-id="2e176-142">Set the **Batch process** option to **Yes**.</span></span> <span data-ttu-id="2e176-143">See seadistus aitab tagada, et saate logisid auditeerida ja kontrollida pakett-töö käituste olekut.</span><span class="sxs-lookup"><span data-stu-id="2e176-143">This setting helps guarantee that you will be able to audit the logs and verify the status of batch job runs.</span></span>
1. <span data-ttu-id="2e176-144">Pakett-töö plaanimiseks valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="2e176-144">Select **OK** to schedule the batch job.</span></span>

<span data-ttu-id="2e176-145">Järgmisel joonisel on näha pakett-töö konfiguratsiooni näide Commerce’is.</span><span class="sxs-lookup"><span data-stu-id="2e176-145">The following illustration shows an example of batch job configuration in Commerce.</span></span>

![Tootehinnangute pakett-töö sünkroonimise konfiguratsioon](media/rnr-hq-batchjob-recurrence.png)

## <a name="verify-that-the-batch-job-for-product-rating-synchronization-was-successful"></a><span data-ttu-id="2e176-147">Kontrollimine, kas tootehinnangute sünkroonimise pakett-töö õnnestus</span><span class="sxs-lookup"><span data-stu-id="2e176-147">Verify that the batch job for product rating synchronization was successful</span></span>

<span data-ttu-id="2e176-148">Selleks et kontrollida, kas pakett-töö **Tootehinnangute sünkroonimine** õnnestus, tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="2e176-148">To verify that the **Sync product ratings** batch job was successful, follow these steps.</span></span>

1. <span data-ttu-id="2e176-149">Valige suvandid **Jaemüük ja kaubandus \> Süsteemiadministraator \> Päringud \> Pakett-tööd**, või kui kasutate ainult Commerce’i jaoks mõeldud varude arvestusühikut (SKU) valige suvandid **Jaemüük ja kaubandus \> Päringud ja aruanded \> Pakett-tööd**.</span><span class="sxs-lookup"><span data-stu-id="2e176-149">Go to **Retail and Commerce \> System administrator \> Inquiries \> Batch jobs** or, if you're using a Commerce-only stock keeping unit (SKU), **Retail and Commerce \> Inquiries and reports \> Batch jobs** instead.</span></span> <span data-ttu-id="2e176-150">Võite sisestada otsingu „Pakett-tööd”.</span><span class="sxs-lookup"><span data-stu-id="2e176-150">Alternatively, search for "Batch jobs."</span></span>
1. <span data-ttu-id="2e176-151">Pakett-töö üksikasjade vaatamiseks otsige pakett-töö loendist veerust **Töö kirjeldus** kirjeldust, mis sisaldab fraasi „Tootehinnangute tõmbamine”.</span><span class="sxs-lookup"><span data-stu-id="2e176-151">To view the details of the batch job, in the batch job list, in the **Job description** column, search for a description that contains "Pull product ratings."</span></span>
1. <span data-ttu-id="2e176-152">Valige töö ID, et vaadata pakett-töö üksikasju, nagu plaanitud alguskuupäev/-kellaaeg ja kordumise tekst.</span><span class="sxs-lookup"><span data-stu-id="2e176-152">Select the job ID to view the batch job details, such as the scheduled start date/time and the recurrence text.</span></span>

<span data-ttu-id="2e176-153">Järgmisel joonisel on näha näide pakett-töö üksikasjadest Commerce’is, kui pakett-töö on plaanitud käivituma kahetunnise intervalliga.</span><span class="sxs-lookup"><span data-stu-id="2e176-153">The following illustration shows an example of the batch job details in Commerce when the batch job is scheduled to run at two-hour intervals.</span></span>

![Tootehinnangute pakett-töö sünkroonimise üksikasjad](media/rnr-hq-batchjob-status-checking.png)

## <a name="make-product-ratings-available-at-the-pos"></a><span data-ttu-id="2e176-155">Tootehinnangute muutmine kassas kättesaadavaks</span><span class="sxs-lookup"><span data-stu-id="2e176-155">Make product ratings available at the POS</span></span>

<span data-ttu-id="2e176-156">Hinnangute ja arvustuste lahendus rakenduses Dynamics 365 Commerce on omnikanali lahendus.</span><span class="sxs-lookup"><span data-stu-id="2e176-156">The ratings and reviews solution in Dynamics 365 Commerce is an omnichannel solution.</span></span> <span data-ttu-id="2e176-157">Kuid vaikimisi tootehinnanguid kassas ei kuvata.</span><span class="sxs-lookup"><span data-stu-id="2e176-157">However, products ratings aren't shown at the POS by default.</span></span> <span data-ttu-id="2e176-158">Selleks et kliendid poodides näeksid hinnanguid ja arvustusi, kui müüjad neid aitavad, peate tootehinnangud kassas sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="2e176-158">To help customers in stores see ratings and reviews when they are being helped by sales associates, you must turn on product ratings at the POS.</span></span>

<span data-ttu-id="2e176-159">Tootehinnangute kassas sisselülitamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="2e176-159">To turn on product ratings at the POS, follow these steps.</span></span>

1. <span data-ttu-id="2e176-160">Minge jaotisse **Jaemüük ja kaubandus \> Kaubanduse seadistamine \> Parameetrid \> Kaubanduse parameetrid**.</span><span class="sxs-lookup"><span data-stu-id="2e176-160">Go to **Retail and Commerce \> Commerce setup \> Parameters \> Commerce parameters**.</span></span> <span data-ttu-id="2e176-161">Võite ka sisestada otsingu „Kaubanduse parameetrid”.</span><span class="sxs-lookup"><span data-stu-id="2e176-161">Alternatively, search for "Commerce parameters."</span></span>
1. <span data-ttu-id="2e176-162">Valige vahekaardilt **Konfiguratsiooni parameetrid** suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="2e176-162">On the **Configuration parameters** tab, select **New**.</span></span>
1. <span data-ttu-id="2e176-163">Sisestage nimi, nt **RatingsAndReviews.EnableProductRatingsForRetailStores**, ja määrake väärtuseks **tõene**.</span><span class="sxs-lookup"><span data-stu-id="2e176-163">Enter a name such as **RatingsAndReviews.EnableProductRatingsForRetailStores**, and set the value to **true**.</span></span>
1. <span data-ttu-id="2e176-164">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="2e176-164">Select **Save**.</span></span>
1. <span data-ttu-id="2e176-165">Avage **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Jaotusgraafik**.</span><span class="sxs-lookup"><span data-stu-id="2e176-165">Go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span> <span data-ttu-id="2e176-166">Võite ka sisestada otsingu „Jaotusgraafik”.</span><span class="sxs-lookup"><span data-stu-id="2e176-166">Alternatively, search for "Distribution schedule."</span></span>
1. <span data-ttu-id="2e176-167">Valige tööde loendist suvand **1110** (**Globaalne konfiguratsioon**) ja seejärel valige käsk **Käivita kohe**.</span><span class="sxs-lookup"><span data-stu-id="2e176-167">In the job list, select **1110** (**Global configuration**), and then select **Run now**.</span></span>
1. <span data-ttu-id="2e176-168">Kui töö on edukalt käivitatud, kontrollige, kas tootehinnangud kuvatakse nüüd kassas.</span><span class="sxs-lookup"><span data-stu-id="2e176-168">After the job has successfully run, verify that products ratings are now shown at the POS.</span></span>

<span data-ttu-id="2e176-169">Järgmisel on joonisel on näha näide Kaubanduse parameetrite konfiguratsioonist tootehinnangute sisselülitamiseks kassas.</span><span class="sxs-lookup"><span data-stu-id="2e176-169">The following illustration shows an example of the configuration of the Commerce parameters to turn on product ratings at the POS.</span></span>

![Kaubanduse parameetrite konfiguratsioon tootehinnangute jaoks kassas](media/rnr-hq-enable-ratings-in-pos.png)

<span data-ttu-id="2e176-171">Järgmisel joonisel on näha näide tootehinnangutest kassas.</span><span class="sxs-lookup"><span data-stu-id="2e176-171">The following illustration shows an example of product ratings at the POS.</span></span>

![Tootehinnangud kassas](media/rnr-pos-catalog-ratings.png)

<span data-ttu-id="2e176-173">Järgmisel joonisel on näha näide tootehinnangutest kõnekeskuse kanalites.</span><span class="sxs-lookup"><span data-stu-id="2e176-173">The following illustration shows an example of product ratings in call center channels.</span></span>

![Tootehinnangud kõnekeskuse kanalis](media/rnr-call-center-ratings.png)

## <a name="additional-resources"></a><span data-ttu-id="2e176-175">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="2e176-175">Additional resources</span></span>

[<span data-ttu-id="2e176-176">Hinnangute ja arvustuste ülevaade</span><span class="sxs-lookup"><span data-stu-id="2e176-176">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="2e176-177">Hinnangute ja arvustuste kasutamise valimine</span><span class="sxs-lookup"><span data-stu-id="2e176-177">Opt in to use ratings and reviews</span></span>](opt-in-ratings-reviews.md)

[<span data-ttu-id="2e176-178">Hinnangute ja arvustuste haldus</span><span class="sxs-lookup"><span data-stu-id="2e176-178">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="2e176-179">Hinnangute ja arvustuste konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="2e176-179">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)
