---
title: Dynamics 365 Commerce'i hindamiskeskkonna konfigureerimine
description: Selles teemas selgitatakse, kuidas konfigureerida Microsoft Dynamics 365 Commerce’i hindamiskeskkond, kui see on ette valmistatud.
author: psimolin
manager: annbe
ms.date: 07/16/2020
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
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6a1ae960f0f530104af7bdea9a8fcb78b01571f5
ms.sourcegitcommit: 5175e3fae432016246244cf70fe05465f43de88c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 07/17/2020
ms.locfileid: "3599720"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="593c8-103">Dynamics 365 Commerce'i hindamiskeskkonna konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="593c8-103">Configure a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="593c8-104">Selles teemas selgitatakse, kuidas konfigureerida Microsoft Dynamics 365 Commerce’i hindamiskeskkond, kui see on ette valmistatud.</span><span class="sxs-lookup"><span data-stu-id="593c8-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce evaluation environment after it's provisioned.</span></span>

## <a name="overview"></a><span data-ttu-id="593c8-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="593c8-105">Overview</span></span>

<span data-ttu-id="593c8-106">Viige lõpule selle teema protseduurid alles pärast seda, kui rakenduse Commerce hindamiskeskkond on ette valmistatud.</span><span class="sxs-lookup"><span data-stu-id="593c8-106">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned.</span></span> <span data-ttu-id="593c8-107">Teavet selle kohta, kuidas Commerce’i hindamiskeskkonda ette valmistada, vaadake teemast [Commerce’i hindamiskeskkonna ettevalmistamine](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="593c8-107">For information about how to provision your Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

<span data-ttu-id="593c8-108">Pärast seda, kui teie Commerce'i hindamiskeskkond on täielikult ettevalmistatud, tuleb lõpule viia ettevalmistusjärgsed konfigureerimisetapid, enne kui saate hakata keskkonda hindama.</span><span class="sxs-lookup"><span data-stu-id="593c8-108">After your Commerce evaluation environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="593c8-109">Nende sammude lõpetamiseks peate kasutama teenust Microsoft Dynamics Lifecycle Services (LCS) ja rakendust Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="593c8-109">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS) and Dynamics 365 Commerce.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="593c8-110">Enne alustamist</span><span class="sxs-lookup"><span data-stu-id="593c8-110">Before you start</span></span>

1. <span data-ttu-id="593c8-111">Logige sisse [LCS portaali](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="593c8-111">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="593c8-112">Avage oma projekt.</span><span class="sxs-lookup"><span data-stu-id="593c8-112">Go to your project.</span></span>
1. <span data-ttu-id="593c8-113">Ülemises menüüs valige suvand **Pilve majutatud keskkonnad**.</span><span class="sxs-lookup"><span data-stu-id="593c8-113">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="593c8-114">Valige loendist oma keskkond.</span><span class="sxs-lookup"><span data-stu-id="593c8-114">Select your environment in the list.</span></span>
1. <span data-ttu-id="593c8-115">Valige paremal olevast keskkonna teabest **Keskkonda sisselogimine**.</span><span class="sxs-lookup"><span data-stu-id="593c8-115">In the environment information on the right, select **Log on to environment**.</span></span> <span data-ttu-id="593c8-116">Teid suunatakse Commerce'i peakontorisse.</span><span class="sxs-lookup"><span data-stu-id="593c8-116">You will be sent to Commerce headquarters.</span></span>
1. <span data-ttu-id="593c8-117">Veenduge, et **USRT** juriidiline isik on valitud ülemises parempoolses nurgas.</span><span class="sxs-lookup"><span data-stu-id="593c8-117">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

<span data-ttu-id="593c8-118">Commerce'i peakontori ettevalmistusjärgsete tegevuste käigus veenduge, et juriidiline isik **USRT** oleks alati valitud.</span><span class="sxs-lookup"><span data-stu-id="593c8-118">During post-provisioning activities in Commerce headquarters, make sure that the **USRT** legal entity is always selected.</span></span>

## <a name="configure-the-point-of-sale"></a><span data-ttu-id="593c8-119">Kassa konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="593c8-119">Configure the point of sale</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="593c8-120">Seosta töötaja oma identiteediga</span><span class="sxs-lookup"><span data-stu-id="593c8-120">Associate a worker with your identity</span></span>

<span data-ttu-id="593c8-121">Töötaja seostamiseks Commerce'i peakontoris oma identiteediga toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="593c8-121">To associate a worker with your identity, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="593c8-122">Kasutage vasakul asuvat menüüd, et avada **Moodulid \> Jaemüük ja kaubandus \> Töövõtjad \> Töötajad**.</span><span class="sxs-lookup"><span data-stu-id="593c8-122">Use the menu on the left to go to **Modules \> Retail and commerce \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="593c8-123">Otsige loendist ja valige kirje **000713 – Andrew Collette**.</span><span class="sxs-lookup"><span data-stu-id="593c8-123">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="593c8-124">Valige toimingupaanil **Kaubandus**.</span><span class="sxs-lookup"><span data-stu-id="593c8-124">On the Action Pane, select **Commerce**.</span></span>
1. <span data-ttu-id="593c8-125">Valige **Seosta olemasolev identiteet**.</span><span class="sxs-lookup"><span data-stu-id="593c8-125">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="593c8-126">Väljale **Meil**, mis on paremal pool väljast **Otsi meili abil**, sisestage oma meiliaadress.</span><span class="sxs-lookup"><span data-stu-id="593c8-126">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="593c8-127">Valige **Otsi**.</span><span class="sxs-lookup"><span data-stu-id="593c8-127">Select **Search**.</span></span>
1. <span data-ttu-id="593c8-128">Valige oma nimega kirje.</span><span class="sxs-lookup"><span data-stu-id="593c8-128">Select the record that has your name.</span></span>
1. <span data-ttu-id="593c8-129">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="593c8-129">Select **OK**.</span></span>
1. <span data-ttu-id="593c8-130">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="593c8-130">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="593c8-131">Pilve kassa aktiveerimist</span><span class="sxs-lookup"><span data-stu-id="593c8-131">Activate Cloud POS</span></span>

<span data-ttu-id="593c8-132">Pilve kassa aktiveerimiseks järgige LCS-is neid etappe.</span><span class="sxs-lookup"><span data-stu-id="593c8-132">To activate Cloud POS, follow these steps in LCS.</span></span>

1. <span data-ttu-id="593c8-133">Ülemises menüüs valige suvand **Pilve majutatud keskkonnad**.</span><span class="sxs-lookup"><span data-stu-id="593c8-133">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="593c8-134">Valige loendist oma keskkond.</span><span class="sxs-lookup"><span data-stu-id="593c8-134">Select your environment in the list.</span></span>
1. <span data-ttu-id="593c8-135">Valige paremal olevast keskkonna teabest **Pilve kassasse sisselogimine**.</span><span class="sxs-lookup"><span data-stu-id="593c8-135">In the environment information on the right, select **Log on to Cloud Point of Sale**.</span></span>
1. <span data-ttu-id="593c8-136">Valige **Edasi** dialoogiboksi **Enne alustamist** avamiseks.</span><span class="sxs-lookup"><span data-stu-id="593c8-136">Select **Next** to open the **Before you start** dialog box.</span></span>
1. <span data-ttu-id="593c8-137">Ärge muutke välja **Serveri URL**.</span><span class="sxs-lookup"><span data-stu-id="593c8-137">Leave the **Server URL** field as it is.</span></span> <span data-ttu-id="593c8-138">Valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="593c8-138">Select **Next**.</span></span>
1. <span data-ttu-id="593c8-139">Logige sisse oma Microsoft Azure Active Directory (Azure AD) konto abil.</span><span class="sxs-lookup"><span data-stu-id="593c8-139">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="593c8-140">Valige jaotises **Kaupluse nimi** suvand **San Francisco** ja seejärel valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="593c8-140">Under **Store name**, select **San Francisco**, and then select **Next**.</span></span>
1. <span data-ttu-id="593c8-141">Jaotise **Register ja seade** väärtuseks valige **SANFRAN-1**.</span><span class="sxs-lookup"><span data-stu-id="593c8-141">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="593c8-142">Valige **Aktiveeri**.</span><span class="sxs-lookup"><span data-stu-id="593c8-142">Select **Activate**.</span></span> <span data-ttu-id="593c8-143">Olete välja logitud ja viidud Kassa sisselogimise lehele.</span><span class="sxs-lookup"><span data-stu-id="593c8-143">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="593c8-144">Nüüd saate pilve kassasse sisse logida, kasutades operaatori ID-d **000713** ja parooli **123**.</span><span class="sxs-lookup"><span data-stu-id="593c8-144">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="593c8-145">Saidi seadistamine Commerce'is</span><span class="sxs-lookup"><span data-stu-id="593c8-145">Set up your site in Commerce</span></span>

<span data-ttu-id="593c8-146">Et alustada oma hindamise saidi seadistamist Commerce'is, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="593c8-146">To start to set up your evaluation site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="593c8-147">Logige saidiehitajasse sisse, kasutades URL-i, mille märkisite üles, kui te e-kaubanduse lähtestamist ette valmistasite (vt [e-kaubanduse lähtestamine](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="593c8-147">Sign in to site builder by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="593c8-148">Klõpsake saidil **Fabrikam**, et avada saidi häälestuse kast.</span><span class="sxs-lookup"><span data-stu-id="593c8-148">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="593c8-149">Valige domeen, mille sisestasite e-kaubanduse lähtestamisel.</span><span class="sxs-lookup"><span data-stu-id="593c8-149">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="593c8-150">Vaikimisi kanali jaoks valige **Fabrikami laiendatud e-pood**.</span><span class="sxs-lookup"><span data-stu-id="593c8-150">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="593c8-151">(Veenduge, et valite **laiendatud** e-poe.)</span><span class="sxs-lookup"><span data-stu-id="593c8-151">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="593c8-152">Vaikekeeleks valige **en-us**.</span><span class="sxs-lookup"><span data-stu-id="593c8-152">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="593c8-153">Jätke välja **tee** väärtus nii, nagu see on.</span><span class="sxs-lookup"><span data-stu-id="593c8-153">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="593c8-154">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="593c8-154">Select **OK**.</span></span> <span data-ttu-id="593c8-155">Kuvatakse saidi lehtede loend.</span><span class="sxs-lookup"><span data-stu-id="593c8-155">The list of pages on the site appears.</span></span>

## <a name="enable-jobs"></a><span data-ttu-id="593c8-156">Tööde lubamine</span><span class="sxs-lookup"><span data-stu-id="593c8-156">Enable jobs</span></span>

<span data-ttu-id="593c8-157">Commerce’is tööde lubamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="593c8-157">To enable jobs in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="593c8-158">Logige sisse keskkonda (HQ).</span><span class="sxs-lookup"><span data-stu-id="593c8-158">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="593c8-159">Kasutades menüüd vasakul, avage **Jaemüük ja kaubandus \> Päringud ja aruanded \> Pakett-tööd**.</span><span class="sxs-lookup"><span data-stu-id="593c8-159">Use the menu on the left to go to **Retail and commerce \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="593c8-160">Selle protseduuri ülejäänud sammud peavad olema täidetud iga järgmise töö puhul:</span><span class="sxs-lookup"><span data-stu-id="593c8-160">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="593c8-161">Jaemüügitellimuse meiliteavituse töötlemine</span><span class="sxs-lookup"><span data-stu-id="593c8-161">Process retail order email notification</span></span>
    * <span data-ttu-id="593c8-162">Toote saadavus</span><span class="sxs-lookup"><span data-stu-id="593c8-162">Product availability</span></span>
    * <span data-ttu-id="593c8-163">P-0001</span><span class="sxs-lookup"><span data-stu-id="593c8-163">P-0001</span></span>
    * <span data-ttu-id="593c8-164">Tellimuste tööde sünkroonimine</span><span class="sxs-lookup"><span data-stu-id="593c8-164">Synchronize orders job</span></span>

1. <span data-ttu-id="593c8-165">Kasutage kiirfiltrit, et otsida tööd, kasutades selle nime.</span><span class="sxs-lookup"><span data-stu-id="593c8-165">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="593c8-166">Kui töö olek on **Teostamine**, tehke järgmist:</span><span class="sxs-lookup"><span data-stu-id="593c8-166">If the status of the job is **Executing**, follow these steps:</span></span>

    1. <span data-ttu-id="593c8-167">Vali kirje.</span><span class="sxs-lookup"><span data-stu-id="593c8-167">Select the record.</span></span>
    1. <span data-ttu-id="593c8-168">Tegumiribal valikus **Pakett-töö**, klõpsake **Muuda olekut**.</span><span class="sxs-lookup"><span data-stu-id="593c8-168">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="593c8-169">Valige **Tühistamine** ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="593c8-169">Select **Canceling**, and then select **OK**.</span></span>

<span data-ttu-id="593c8-170">Saate seadistada ka kordumise intervalli iga ühe (1) minuti järel järgmiste tööde puhul.</span><span class="sxs-lookup"><span data-stu-id="593c8-170">Optionally, you can also set the recurrence interval to one (1) minute for the following jobs:</span></span>

* <span data-ttu-id="593c8-171">Jaemüügitellimuse meiliteavituse töötlemise töö</span><span class="sxs-lookup"><span data-stu-id="593c8-171">Process retail order email notification job</span></span>
* <span data-ttu-id="593c8-172">P-0001 töö</span><span class="sxs-lookup"><span data-stu-id="593c8-172">P-0001 job</span></span>
* <span data-ttu-id="593c8-173">Tellimuste tööde sünkroonimine</span><span class="sxs-lookup"><span data-stu-id="593c8-173">Synchronize orders job</span></span>

### <a name="run-full-data-synchronization"></a><span data-ttu-id="593c8-174">Kõikide andmete sünkroonimise käitamine</span><span class="sxs-lookup"><span data-stu-id="593c8-174">Run full data synchronization</span></span>

<span data-ttu-id="593c8-175">Commerce’is kõikide andmete sünkroonimise käitamiseks tehke Commerce'i peakontoris järgmist.</span><span class="sxs-lookup"><span data-stu-id="593c8-175">To run full data synchronization in Commerce, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="593c8-176">Kasutage vasakul asuvat menüüd, et avada **Moodulid \> Jaemüük ja kaubandus \> Peakontori häälestus \> Kaubanduse planeerija \> Kanali andmebaas**.</span><span class="sxs-lookup"><span data-stu-id="593c8-176">Use the menu on the left to go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="593c8-177">Valige muu kanal nimega **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="593c8-177">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="593c8-178">Valige tegumiribal suvand **Andmete täielik sünkroonimine**.</span><span class="sxs-lookup"><span data-stu-id="593c8-178">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="593c8-179">Sisestage jaotugraafikuna väärtus **9999**.</span><span class="sxs-lookup"><span data-stu-id="593c8-179">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="593c8-180">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="593c8-180">Select **OK**.</span></span>
1. <span data-ttu-id="593c8-181">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="593c8-181">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="593c8-182">Testige krediitkaardi teavet, et sooritada testoste.</span><span class="sxs-lookup"><span data-stu-id="593c8-182">Test credit card information to do test purchases</span></span>

<span data-ttu-id="593c8-183">Selleks, et sooritada testi kandeid saidil, saate kasutada järgmist testi krediitkaardi teavet.</span><span class="sxs-lookup"><span data-stu-id="593c8-183">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="593c8-184">**Kaardi number:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="593c8-184">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="593c8-185">**Aegumiskuupäev:** 10/20</span><span class="sxs-lookup"><span data-stu-id="593c8-185">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="593c8-186">**Kaardi tõendamise väärtus (CVV) kood:** 737</span><span class="sxs-lookup"><span data-stu-id="593c8-186">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="593c8-187">Te ei tohiks proovida kasutada tegeliku krediitkaardi teavet testi tegevuskohas mitte ühelgi juhul.</span><span class="sxs-lookup"><span data-stu-id="593c8-187">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="593c8-188">Järgmised etapid</span><span class="sxs-lookup"><span data-stu-id="593c8-188">Next steps</span></span>

<span data-ttu-id="593c8-189">Pärast ettevalmistamise ja konfigureerimise etappide lõpule viimist, olete valmis oma hindamiskeskkonda kasutama.</span><span class="sxs-lookup"><span data-stu-id="593c8-189">After the provisioning and configuration steps are completed, you can start to use your evaluation environment.</span></span> <span data-ttu-id="593c8-190">Kasutage Commerce'i saidiehitaja URL-i, et minna autorluskogemuse juurde.</span><span class="sxs-lookup"><span data-stu-id="593c8-190">Use the Commerce site builder URL to go to the authoring experience.</span></span> <span data-ttu-id="593c8-191">Kasutage Commerce'i saidi URL-i, et minna jaemüügi klientide saidikogemuse juurde.</span><span class="sxs-lookup"><span data-stu-id="593c8-191">Use the Commerce site URL to go to the retail customer site experience.</span></span>

<span data-ttu-id="593c8-192">Teavet selle kohta, kuidas Commerce’i hindamiskeskkonna valikulisi funktsioone konfigureerida, vaadake teemast [Commerce’i hindamiskeskkonna valikuliste funktsioonide konfigureerimine](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="593c8-192">To configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="593c8-193">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="593c8-193">Additional resources</span></span>

[<span data-ttu-id="593c8-194">Dynamics 365 Commerce'i hindamiskeskkonna ülevaade</span><span class="sxs-lookup"><span data-stu-id="593c8-194">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="593c8-195">Dynamics 365 Commerce'i hindamiskeskkonna ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="593c8-195">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="593c8-196">Dynamics 365 Commerce'i hindamiskeskkonna valikuliste funktsioonide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="593c8-196">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="593c8-197">BOPIS-e konfigureerimine Dynamics 365 Commerce'i hindamiskeskkonnas</span><span class="sxs-lookup"><span data-stu-id="593c8-197">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="593c8-198">Dynamics 365 Commerce'i hindamiskeskkonna KKK</span><span class="sxs-lookup"><span data-stu-id="593c8-198">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="593c8-199">Microsofti elutsükli teenused (LCS)</span><span class="sxs-lookup"><span data-stu-id="593c8-199">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="593c8-200">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="593c8-200">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="593c8-201">Microsoft Azure'i portaal</span><span class="sxs-lookup"><span data-stu-id="593c8-201">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="593c8-202">Dynamics 365 Commerce veebisait</span><span class="sxs-lookup"><span data-stu-id="593c8-202">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
