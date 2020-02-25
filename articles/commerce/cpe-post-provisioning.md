---
title: Dynamics 365 Commerce eelvaatekeskkonna konfigureerimine
description: Selles teemas selgitatakse, kuidas konfigureerida Microsoft Dynamics 365 Commerce’i eelvaatekeskkond, kui see on ette valmistatud.
author: psimolin
manager: annbe
ms.date: 12/10/2019
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
ms.openlocfilehash: 12d3a86698e9250f5d1645de51e0749c8d929f75
ms.sourcegitcommit: 4ed1d8ad8a0206a4172dbb41cc43f7d95073059c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024702"
---
# <a name="configure-a-dynamics-365-commerce-preview-environment"></a><span data-ttu-id="59ccc-103">Dynamics 365 Commerce eelvaatekeskkonna konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="59ccc-103">Configure a Dynamics 365 Commerce preview environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="59ccc-104">Selles teemas selgitatakse, kuidas konfigureerida Microsoft Dynamics 365 Commerce’i eelvaatekeskkond, kui see on ette valmistatud.</span><span class="sxs-lookup"><span data-stu-id="59ccc-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce preview environment after it's provisioned.</span></span>

## <a name="overview"></a><span data-ttu-id="59ccc-105">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="59ccc-105">Overview</span></span>

<span data-ttu-id="59ccc-106">Lõpetage selle teema protseduurid alles pärast seda, kui rakenduse Commerce eelvaatekeskkond on ette valmistatud.</span><span class="sxs-lookup"><span data-stu-id="59ccc-106">Complete the procedures in this topic only after your Commerce preview environment has been provisioned.</span></span> <span data-ttu-id="59ccc-107">Teavet selle kohta, kuidas Commerce’i eelvaatekeskkonda ette valmistada, vaadake teemast [Commerce’i eelvaatekeskkonna ettevalmistamine](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="59ccc-107">For information about how to provision your Commerce preview environment, see [Provision a Commerce preview environment](provisioning-guide.md).</span></span>

<span data-ttu-id="59ccc-108">Pärast seda, kui teie Commerce eelvaatekeskkond on eelnevalt lõpetatud, tuleb lõpule viia täiendavad konteeringu konfigureerimise etapid, enne kui saate hakata keskkonda hindama.</span><span class="sxs-lookup"><span data-stu-id="59ccc-108">After your Commerce preview environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="59ccc-109">Nende sammude lõpetamiseks peate kasutama Microsoft Dynamics elutsükli teenuseid (LCS), Dynamics 365 Commerceja Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="59ccc-109">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS), Dynamics 365 Commerce, and Dynamics 365 Retail.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="59ccc-110">Enne alustamist</span><span class="sxs-lookup"><span data-stu-id="59ccc-110">Before you start</span></span>

1. <span data-ttu-id="59ccc-111">Logige sisse [LCS portaali](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="59ccc-111">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="59ccc-112">Avage oma projekt.</span><span class="sxs-lookup"><span data-stu-id="59ccc-112">Go to your project.</span></span>
1. <span data-ttu-id="59ccc-113">Ülemises menüüs valige suvand **Pilve majutatud keskkonnad**.</span><span class="sxs-lookup"><span data-stu-id="59ccc-113">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="59ccc-114">Valige loendist oma keskkond.</span><span class="sxs-lookup"><span data-stu-id="59ccc-114">Select your environment in the list.</span></span>
1. <span data-ttu-id="59ccc-115">Valige paremal olevast keskkonna informatsioonist **Täielik teave**.</span><span class="sxs-lookup"><span data-stu-id="59ccc-115">In the environment information on the right, select **Full details**.</span></span>
1. <span data-ttu-id="59ccc-116">Valige **Logi sisse**, et avada menüü ja valige suvand **Logi keskkonda**.</span><span class="sxs-lookup"><span data-stu-id="59ccc-116">Select **Login** to open a menu, and then select **Log on to environment**.</span></span>
1. <span data-ttu-id="59ccc-117">Veenduge, et **USRT** juriidiline isik on valitud ülemises parempoolses nurgas.</span><span class="sxs-lookup"><span data-stu-id="59ccc-117">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

## <a name="configure-the-point-of-sale-in-lcs"></a><span data-ttu-id="59ccc-118">Müügikoha konfigureerimine LCS-is</span><span class="sxs-lookup"><span data-stu-id="59ccc-118">Configure the point of sale in LCS</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="59ccc-119">Seosta töötaja oma identiteediga</span><span class="sxs-lookup"><span data-stu-id="59ccc-119">Associate a worker with your identity</span></span>

<span data-ttu-id="59ccc-120">Töötaja seostamiseks LCS-is oma identiteediga toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="59ccc-120">To associate a worker with your identity in LCS, follow these steps.</span></span>

1. <span data-ttu-id="59ccc-121">Vasakul asuva menüü abil avage **Moodulid \> Jaemüük \> Töövõtjad \> Töötajad**.</span><span class="sxs-lookup"><span data-stu-id="59ccc-121">Use the menu on the left to go to **Modules \> Retail \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="59ccc-122">Otsige loendist ja valige kirje **000713 – Andrew Collette**.</span><span class="sxs-lookup"><span data-stu-id="59ccc-122">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="59ccc-123">Toimingupaanil valige käsk **Jaemüük**.</span><span class="sxs-lookup"><span data-stu-id="59ccc-123">On the Action Pane, select **Retail**.</span></span>
1. <span data-ttu-id="59ccc-124">Valige **Seosta olemasolev identiteet**.</span><span class="sxs-lookup"><span data-stu-id="59ccc-124">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="59ccc-125">Väljale **Meil**, mis on paremal pool väljast **Otsi meili abil**, sisestage oma meiliaadress.</span><span class="sxs-lookup"><span data-stu-id="59ccc-125">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="59ccc-126">Valige **Otsi**.</span><span class="sxs-lookup"><span data-stu-id="59ccc-126">Select **Search**.</span></span>
1. <span data-ttu-id="59ccc-127">Valige oma nimega kirje.</span><span class="sxs-lookup"><span data-stu-id="59ccc-127">Select the record that has your name.</span></span>
1. <span data-ttu-id="59ccc-128">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="59ccc-128">Select **OK**.</span></span>
1. <span data-ttu-id="59ccc-129">Valige käsk **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="59ccc-129">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="59ccc-130">Pilve kassa aktiveerimist</span><span class="sxs-lookup"><span data-stu-id="59ccc-130">Activate Cloud POS</span></span>

<span data-ttu-id="59ccc-131">Pilve POS aktiveerimiseks LCS-s toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="59ccc-131">To activate Cloud POS in LCS, follow these steps.</span></span>

1. <span data-ttu-id="59ccc-132">Ülemises menüüs valige suvand **Pilve majutatud keskkonnad**.</span><span class="sxs-lookup"><span data-stu-id="59ccc-132">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="59ccc-133">Valige loendist oma keskkond.</span><span class="sxs-lookup"><span data-stu-id="59ccc-133">Select your environment in the list.</span></span>
1. <span data-ttu-id="59ccc-134">Valige paremal olevast keskkonna informatsioonist **Täielik teave**.</span><span class="sxs-lookup"><span data-stu-id="59ccc-134">In the environment information on the right, select **Full details**.</span></span>
1. <span data-ttu-id="59ccc-135">Menüü avalmiseks valige **Logi sisse** ja seejärel valige **Logi sisse pilve kassasse** et avada kassa (POS).</span><span class="sxs-lookup"><span data-stu-id="59ccc-135">Select **Login** to open a menu, and then select **Log on to Cloud Point of Sale** to open the point of sale (POS).</span></span>
1. <span data-ttu-id="59ccc-136">Valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="59ccc-136">Select **Next**.</span></span>
1. <span data-ttu-id="59ccc-137">Logige sisse oma Microsoft Azure Active Directory (Azure AD) konto abil.</span><span class="sxs-lookup"><span data-stu-id="59ccc-137">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="59ccc-138">Välja **Kaupluse nimi** väärtuseks valige **San Francisco**.</span><span class="sxs-lookup"><span data-stu-id="59ccc-138">Under **Store name**, select **San Francisco**.</span></span>
1. <span data-ttu-id="59ccc-139">Valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="59ccc-139">Select **Next**.</span></span>
1. <span data-ttu-id="59ccc-140">Jaotise **Register ja seade** väärtuseks valige **SANFRAN-1**.</span><span class="sxs-lookup"><span data-stu-id="59ccc-140">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="59ccc-141">Valige **Aktiveeri**.</span><span class="sxs-lookup"><span data-stu-id="59ccc-141">Select **Activate**.</span></span> <span data-ttu-id="59ccc-142">Olete välja logitud ja viidud Kassa sisselogimise lehele.</span><span class="sxs-lookup"><span data-stu-id="59ccc-142">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="59ccc-143">Nüüd saate pilve kassasse sisse logida, kasutades operaatori ID-d **000713** ja parooli **123**.</span><span class="sxs-lookup"><span data-stu-id="59ccc-143">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="59ccc-144">Saidi seadistamine Commerce'is</span><span class="sxs-lookup"><span data-stu-id="59ccc-144">Set up your site in Commerce</span></span>

<span data-ttu-id="59ccc-145">Et alustada oma eelvaate saidi seadistamist Commerce'is, toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="59ccc-145">To start to set up your preview site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="59ccc-146">Logige saidi halduse tööriista sisse, kasutades URL-i, mis te tegite, kui te tegite e-kaubanduse lähtestamisel ettevalmistuse (vt [e-kaubanduse lähtestamine](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="59ccc-146">Sign in to the site management tool by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="59ccc-147">Klõpsake saidil **Fabrikam**, et avada saidi häälestuse kast.</span><span class="sxs-lookup"><span data-stu-id="59ccc-147">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="59ccc-148">Valige domeen, mille sisestasite e-kaubanduse lähtestamisel.</span><span class="sxs-lookup"><span data-stu-id="59ccc-148">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="59ccc-149">Vaikimisi kanali jaoks valige **Fabrikami laiendatud e-pood**.</span><span class="sxs-lookup"><span data-stu-id="59ccc-149">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="59ccc-150">(Veenduge, et valite **laiendatud** e-poe.)</span><span class="sxs-lookup"><span data-stu-id="59ccc-150">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="59ccc-151">Vaikekeeleks valige **en-us**.</span><span class="sxs-lookup"><span data-stu-id="59ccc-151">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="59ccc-152">Jätke välja **tee** väärtus nii, nagu see on.</span><span class="sxs-lookup"><span data-stu-id="59ccc-152">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="59ccc-153">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="59ccc-153">Select **OK**.</span></span> <span data-ttu-id="59ccc-154">Kuvatakse saidi lehtede loend.</span><span class="sxs-lookup"><span data-stu-id="59ccc-154">The list of pages on the site appears.</span></span>

## <a name="enable-jobs-in-retail"></a><span data-ttu-id="59ccc-155">Luba tööd jaemüügis</span><span class="sxs-lookup"><span data-stu-id="59ccc-155">Enable jobs in Retail</span></span>

<span data-ttu-id="59ccc-156">Jaemüügi tööde lubamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="59ccc-156">To enable jobs in Retail, follow these steps.</span></span>

1. <span data-ttu-id="59ccc-157">Logige sisse keskkonda (HQ).</span><span class="sxs-lookup"><span data-stu-id="59ccc-157">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="59ccc-158">Kasutades menüüd vasakul, avage **Jaemüük \> Päringud ja aruanded \> Pakett-tööd**.</span><span class="sxs-lookup"><span data-stu-id="59ccc-158">Use the menu on the left to go to **Retail \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="59ccc-159">Selle protseduuri ülejäänud sammud peavad olema täidetud iga järgmise töö puhul:</span><span class="sxs-lookup"><span data-stu-id="59ccc-159">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="59ccc-160">Jaemüügitellimuse meiliteavituse töötlemine</span><span class="sxs-lookup"><span data-stu-id="59ccc-160">Process retail order email notification</span></span>
    * <span data-ttu-id="59ccc-161">Toote saadavus</span><span class="sxs-lookup"><span data-stu-id="59ccc-161">Product availability</span></span>
    * <span data-ttu-id="59ccc-162">P-0001</span><span class="sxs-lookup"><span data-stu-id="59ccc-162">P-0001</span></span>
    * <span data-ttu-id="59ccc-163">Tellimuste tööde sünkroonimine</span><span class="sxs-lookup"><span data-stu-id="59ccc-163">Synchronize orders job</span></span>

1. <span data-ttu-id="59ccc-164">Kasutage kiirfiltrit, et otsida tööd, kasutades selle nime.</span><span class="sxs-lookup"><span data-stu-id="59ccc-164">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="59ccc-165">Kui töö olek on **Kinnipeetud**, tehke järgmist:</span><span class="sxs-lookup"><span data-stu-id="59ccc-165">If the status of the job is **Withhold**, follow these steps:</span></span>

    1. <span data-ttu-id="59ccc-166">Vali kirje.</span><span class="sxs-lookup"><span data-stu-id="59ccc-166">Select the record.</span></span>
    1. <span data-ttu-id="59ccc-167">Tegumiribal valikus **Pakett-töö**, klõpsake **Muuda olekut**.</span><span class="sxs-lookup"><span data-stu-id="59ccc-167">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="59ccc-168">Valige suvand **Ootel** ja seejärel nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="59ccc-168">Select **Waiting**, and then select **OK**.</span></span>

### <a name="run-full-data-synchronization-in-retail"></a><span data-ttu-id="59ccc-169">Kogu teabe sünkroonimise käivitamine jaemüügis</span><span class="sxs-lookup"><span data-stu-id="59ccc-169">Run full data synchronization in Retail</span></span>

<span data-ttu-id="59ccc-170">Täieliku andmeedastuse sünkroonimise käivitamiseks jaemüügis toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="59ccc-170">To run full data synchronization in Retail, follow these steps.</span></span>

1. <span data-ttu-id="59ccc-171">Vasakual asuva menüü abil avage **Moodulid \> Jaemüük \> Peakontori häälestus \> Jaemüügi planeerija \> Kanali andmebaas**.</span><span class="sxs-lookup"><span data-stu-id="59ccc-171">Use the menu on the left to go to **Modules \> Retail \> Headquarters setup \> Retail scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="59ccc-172">Kanal **Vaikimisi** valitakse vasakul olevast loendist.</span><span class="sxs-lookup"><span data-stu-id="59ccc-172">In the list on the left, the **Default** channel is selected.</span></span> <span data-ttu-id="59ccc-173">Valige muu saadaolev kanal.</span><span class="sxs-lookup"><span data-stu-id="59ccc-173">Select the other available channel.</span></span> <span data-ttu-id="59ccc-174">Selle kanali nimi on **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="59ccc-174">This channel is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="59ccc-175">Valige tegumiribal suvand **Andmete täielik sünkroonimine**.</span><span class="sxs-lookup"><span data-stu-id="59ccc-175">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="59ccc-176">Sisestage jaotugraafikuna väärtus **9999**.</span><span class="sxs-lookup"><span data-stu-id="59ccc-176">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="59ccc-177">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="59ccc-177">Select **OK**.</span></span>
1. <span data-ttu-id="59ccc-178">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="59ccc-178">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="59ccc-179">Testige krediitkaardi teavet, et sooritada testoste.</span><span class="sxs-lookup"><span data-stu-id="59ccc-179">Test credit card information to do test purchases</span></span>

<span data-ttu-id="59ccc-180">Selleks, et sooritada testi kandeid saidil, saate kasutada järgmist testi krediitkaardi teavet.</span><span class="sxs-lookup"><span data-stu-id="59ccc-180">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="59ccc-181">**Kaardi number:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="59ccc-181">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="59ccc-182">**Aegumiskuupäev:** 10/20</span><span class="sxs-lookup"><span data-stu-id="59ccc-182">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="59ccc-183">**Kaardi tõendamise väärtus (CVV) kood:** 737</span><span class="sxs-lookup"><span data-stu-id="59ccc-183">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="59ccc-184">Te ei tohiks proovida kasutada tegeliku krediitkaardi teavet testi tegevuskohas mitte ühelgi juhul.</span><span class="sxs-lookup"><span data-stu-id="59ccc-184">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="59ccc-185">Järgmised etapid</span><span class="sxs-lookup"><span data-stu-id="59ccc-185">Next steps</span></span>

<span data-ttu-id="59ccc-186">Pärast ettevalmistamise ja konfigureerimise sammude lõpetamist olete valmis oma eelvaate keskkonda hindama.</span><span class="sxs-lookup"><span data-stu-id="59ccc-186">After the provisioning and configuration steps are completed, you're ready to evaluate your preview environment.</span></span> <span data-ttu-id="59ccc-187">Kasutage rakenduse Commerce Site Management tööriista URL-i, et minna autorluse kogemuse juurde.</span><span class="sxs-lookup"><span data-stu-id="59ccc-187">Use the URL of the Commerce site management tool to go to the authoring experience.</span></span> <span data-ttu-id="59ccc-188">Kasutage rakenduse Commerce jaemüügi klientide saidi URL-i, et minna autorluse kogemuse juurde.</span><span class="sxs-lookup"><span data-stu-id="59ccc-188">Use the URL of the Commerce site to go to the retail customer site experience.</span></span>

<span data-ttu-id="59ccc-189">Teavet selle kohta, kuidas Commerce’i eelvaatekeskkonna valikulisi funktsioone konfigureerida, vaadake teemast [Commerce’i eelvaatekeskkonna valikuliste funktsioonide konfigureerimine](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="59ccc-189">To configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="59ccc-190">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="59ccc-190">Additional resources</span></span>

[<span data-ttu-id="59ccc-191">Dynamics 365 Commerce eelvaatekeskkonna ülevaade</span><span class="sxs-lookup"><span data-stu-id="59ccc-191">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="59ccc-192">Dynamics 365 Commerce'i eelvaatekeskkonna ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="59ccc-192">Provision a Dynamics 365 Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="59ccc-193">Dynamics 365 Commerce’i eelvaatekeskkonna valikuliste funktsioonide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="59ccc-193">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="59ccc-194">Dynamics 365 Commerce eelvaatekeskkonna KKK</span><span class="sxs-lookup"><span data-stu-id="59ccc-194">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="59ccc-195">Microsofti elutsükli teenused (LCS)</span><span class="sxs-lookup"><span data-stu-id="59ccc-195">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="59ccc-196">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="59ccc-196">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="59ccc-197">Microsoft Azure'i portaal</span><span class="sxs-lookup"><span data-stu-id="59ccc-197">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="59ccc-198">Dynamics 365 Commerce veebisait</span><span class="sxs-lookup"><span data-stu-id="59ccc-198">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
