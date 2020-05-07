---
title: BOPIS-i konfigureerimine Dynamics 365 Commerce'i keskkonnas
description: Selles teemas selgitatakse, kuidas konfigureerida stsenaariumit „osta veebis, käi poes järel” (BOPIS) Microsoft Dynamics 365 Commerce'i keskkonnas pärast selle ettevalmistamist.
author: rubendel
manager: annbe
ms.date: 04/21/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: rubendel
ms.search.validFrom: 2020-04-20
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 956d66d09885d4d54655ce25b3aa7ba6a9c34cf4
ms.sourcegitcommit: dfef2faf881b2db1bd0f016df36e2b838105312b
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 04/22/2020
ms.locfileid: "3282792"
---
# <a name="configure-bopis-in-a-dynamics-365-commerce-environment"></a><span data-ttu-id="eadf1-103">BOPIS-i konfigureerimine Dynamics 365 Commerce'i keskkonnas</span><span class="sxs-lookup"><span data-stu-id="eadf1-103">Configure BOPIS in a Dynamics 365 Commerce environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="eadf1-104">Selles teemas selgitatakse, kuidas konfigureerida stsenaariumit „osta veebis, käi poes järel” (BOPIS) Microsoft Dynamics 365 Commerce'i keskkonnas pärast keskkonna ettevalmistamist.</span><span class="sxs-lookup"><span data-stu-id="eadf1-104">This topic explains how to configure buy online, pickup in store (BOPIS) in a Microsoft Dynamics 365 Commerce environment after the environment has been provisioned.</span></span>

## <a name="prerequisite"></a><span data-ttu-id="eadf1-105">Eeltingimus</span><span class="sxs-lookup"><span data-stu-id="eadf1-105">Prerequisite</span></span>

<span data-ttu-id="eadf1-106">Lõpetage selle teema protseduurid alles pärast seda, kui rakenduse Commerce eelvaatekeskkond on ette valmistatud ja konfigureeritud.</span><span class="sxs-lookup"><span data-stu-id="eadf1-106">Complete the procedures in this topic only after your Commerce preview environment has been provisioned and configured.</span></span> <span data-ttu-id="eadf1-107">Teavet selle kohta, kuidas oma keskkonda ette valmistada ja konfigureerida, vaadake teemadest [Dynamics 365 Commerce'i eelvaatekeskkonna ettevalmistamine](provisioning-guide.md) ja [Dynamics 365 Commerce'i eelvaatekeskkonna konfigureerimine](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning).</span><span class="sxs-lookup"><span data-stu-id="eadf1-107">For information about how to provision and configure your environment, see [Provision a Dynamics 365 Commerce preview environment](provisioning-guide.md) and [Configure a Dynamics 365 Commerce preview environment](https://docs.microsoft.com/dynamics365/commerce/cpe-post-provisioning).</span></span>

<span data-ttu-id="eadf1-108">Pärast seda, kui teie Commerce'i keskkond on lõpuni ette valmistatud ja konfigureeritud, saate seda teemat kasutada BOPIS-i stsenaariumide lubamiseks.</span><span class="sxs-lookup"><span data-stu-id="eadf1-108">After your Commerce environment has been provisioned and configured end to end, you can use this topic to enable BOPIS scenarios.</span></span>

## <a name="configure-the-pos"></a><span data-ttu-id="eadf1-109">Kassa konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="eadf1-109">Configure the POS</span></span>

### <a name="configure-modern-pos"></a><span data-ttu-id="eadf1-110">Modern POS-i konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="eadf1-110">Configure Modern POS</span></span>

<span data-ttu-id="eadf1-111">BOPIS-i stsenaariumide jaoks, mis hõlmavad krediitkaardimakseid, on vaja riistvarajaama.</span><span class="sxs-lookup"><span data-stu-id="eadf1-111">BOPIS scenarios that involve a credit card payment require a hardware station.</span></span> <span data-ttu-id="eadf1-112">Riistvarajaam on integreeritud rakendusse Modern POS Windowsi ja Androidi klientidele.</span><span class="sxs-lookup"><span data-stu-id="eadf1-112">The hardware station is built into Modern POS for Windows and Android clients.</span></span> <span data-ttu-id="eadf1-113">Kui kasutate Cloud POS-i või Modern POS-i iOS-i jaoks, peab kassa (POS) klient olema ühendatud ühiskasutatava riistvarajaamaga.</span><span class="sxs-lookup"><span data-stu-id="eadf1-113">If you're using Cloud POS or Modern POS for iOS, the point of sale (POS) client must be paired with a shared hardware station.</span></span> <span data-ttu-id="eadf1-114">See teema selgitab, kuidas konfigureerida BOPIS-i Windowsi ja Androidi klientide jaoks.</span><span class="sxs-lookup"><span data-stu-id="eadf1-114">This topic explains how to configure BOPIS for Windows and Android clients.</span></span> <span data-ttu-id="eadf1-115">Lisateavet ühiskasutatava riistvarajaama seadistamise kohta leiate jaotisest [Jaemüügi riistvarajaama konfigureerimine ja installimine](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation).</span><span class="sxs-lookup"><span data-stu-id="eadf1-115">For information about how to set up a shared hardware station, see [Configure and install Retail hardware station](https://docs.microsoft.com/dynamics365/commerce/retail-hardware-station-configuration-installation).</span></span>

1. <span data-ttu-id="eadf1-116">Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Registrid**.</span><span class="sxs-lookup"><span data-stu-id="eadf1-116">Go to **Retail and Commerce \> Channel setup \> POS setup \> Registers**.</span></span>
2. <span data-ttu-id="eadf1-117">Valige register **SANFRAN-5** ja seejärel valige **Redigeeri**.</span><span class="sxs-lookup"><span data-stu-id="eadf1-117">Select register **SANFRAN-5**, and then select **Edit**.</span></span>
3. <span data-ttu-id="eadf1-118">Muutke väli **Riistvaraprofiil** väärtuselt **HW002** väärtusele **HW001** ja seejärel valige **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="eadf1-118">Change the value of the **Hardware profile** field from **HW002** to **HW001**, and then select **Save**.</span></span>
4. <span data-ttu-id="eadf1-119">Muudatuste sünkroonimiseks minge **Jaemüük ja kaubandus \> Jaemüügi ja kaubanduse IT \> Jaotusgraafik**.</span><span class="sxs-lookup"><span data-stu-id="eadf1-119">To synchronize the changes, go to **Retail and Commerce \> Retail and Commerce IT \> Distribution schedule**.</span></span>
5. <span data-ttu-id="eadf1-120">Valige jaotusgraafik **1090** ja seejärel valige toimingupaanil käsk **Käita kohe**.</span><span class="sxs-lookup"><span data-stu-id="eadf1-120">Select distribution schedule **1090**, and then, on the Action Pane, select **Run now**.</span></span>
6. <span data-ttu-id="eadf1-121">Valige **Jah** ja seejärel **OK**, et algatada andmete sünkroonimine.</span><span class="sxs-lookup"><span data-stu-id="eadf1-121">Select **Yes** and then **OK** to initiate data synchronization.</span></span> 

### <a name="install-modern-pos"></a><span data-ttu-id="eadf1-122">Modern POS-i installimine</span><span class="sxs-lookup"><span data-stu-id="eadf1-122">Install Modern POS</span></span>

1. <span data-ttu-id="eadf1-123">Avage **Jaemüük ja kaubandus \> Kanali seadistus \> Kassa seadistus \> Seadmed**.</span><span class="sxs-lookup"><span data-stu-id="eadf1-123">Go to **Retail and Commerce \> Channel setup \> POS setup \> Devices**.</span></span>
2. <span data-ttu-id="eadf1-124">Valige seade **SANFRANCIS-5**.</span><span class="sxs-lookup"><span data-stu-id="eadf1-124">Select device **SANFRANCIS-5**.</span></span>
3. <span data-ttu-id="eadf1-125">Valige tegumipaanilt **Laadi alla** ja valige siis **Konfiguratsioonifail**.</span><span class="sxs-lookup"><span data-stu-id="eadf1-125">On the Action Pane, select **Download**, and then select **Configuration file**.</span></span>
4. <span data-ttu-id="eadf1-126">Valige käsk **Laadi alla** ja seejärel **Retail Modern POS**.</span><span class="sxs-lookup"><span data-stu-id="eadf1-126">Select **Download**, and then select **Retail Modern POS**.</span></span> 
5. <span data-ttu-id="eadf1-127">Kui faili **ModernPOSSetup.exe** allalaadimine on lõpule viidud, valige **Ava fail**.</span><span class="sxs-lookup"><span data-stu-id="eadf1-127">When download of the **ModernPOSSetup.exe** file is completed, select **Open file**.</span></span>

    ![Ava fail](./dev-itpro/media/PAYMENTS/openfile.png)

6. <span data-ttu-id="eadf1-129">Valige **Järgmine**, et installimisprotsess lõpule viia.</span><span class="sxs-lookup"><span data-stu-id="eadf1-129">Select **Next** to go through the installation process.</span></span> <span data-ttu-id="eadf1-130">Kui installimine on lõpule viidud, valige **Sule**.</span><span class="sxs-lookup"><span data-stu-id="eadf1-130">When installation is completed, select **Close**.</span></span>

### <a name="activate-modern-pos"></a><span data-ttu-id="eadf1-131">Modern POS-i aktiveerimine</span><span class="sxs-lookup"><span data-stu-id="eadf1-131">Activate Modern POS</span></span>

1. <span data-ttu-id="eadf1-132">Valige Windowsi töölaual nupp **Start** ja sisestage **Retail Modern POS**.</span><span class="sxs-lookup"><span data-stu-id="eadf1-132">On the Windows desktop, select the **Start** button, and enter **Retail Modern POS**.</span></span>
2. <span data-ttu-id="eadf1-133">Valige aktiveerimise käivitamiseks rakendus **Retail Modern POS**.</span><span class="sxs-lookup"><span data-stu-id="eadf1-133">Select the **Retail Modern POS** application to initiate activation.</span></span>
3. <span data-ttu-id="eadf1-134">Valige **Edasi**.</span><span class="sxs-lookup"><span data-stu-id="eadf1-134">Select **Next**.</span></span> <span data-ttu-id="eadf1-135">Väljad **Serveri URL**, **Seadme ID** ja **Registri number** peaksid olema eelhäälestatud, kasutades eelmises protsessis allalaaditud konfiguratsioonifaili teavet.</span><span class="sxs-lookup"><span data-stu-id="eadf1-135">The **Server URL**, **Device ID**, and **Register number** fields should be preset by using information from the configuration file that you downloaded in the previous procedure.</span></span>
4. <span data-ttu-id="eadf1-136">Valige **Aktiveeri**.</span><span class="sxs-lookup"><span data-stu-id="eadf1-136">Select **Activate**.</span></span>
5. <span data-ttu-id="eadf1-137">Kuvatakse dialoogiboks autentimiseks.</span><span class="sxs-lookup"><span data-stu-id="eadf1-137">An authentication dialog box appears.</span></span> <span data-ttu-id="eadf1-138">Valige konto, mis kasutab e-posti aadressi, mis oli varem seotud töötajaga **000713 – Andrew Collette**.</span><span class="sxs-lookup"><span data-stu-id="eadf1-138">Select the account that uses the email address that was previously associated with worker **000713 - Andrew Collette**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="eadf1-139">Kui te pole veel töötajat oma identiteediga seostanud, siis aktiveerimine nurjub.</span><span class="sxs-lookup"><span data-stu-id="eadf1-139">If you haven't yet associated a worker with your identity, activation will be unsuccessful.</span></span> <span data-ttu-id="eadf1-140">Sellisel juhul järgige teema [Dynamics 365 Commerce'i eelvaatekeskkonna konfigureerimine](cpe-post-provisioning.md#associate-a-worker-with-your-identity) jaotises „Seosta töötaja oma identiteediga” toodud samme.</span><span class="sxs-lookup"><span data-stu-id="eadf1-140">In this case, follow the steps under the "Associate a worker with your identity" section in the [Configure a Dynamics 365 Commerce preview environment](cpe-post-provisioning.md#associate-a-worker-with-your-identity) topic.</span></span>
    
6. <span data-ttu-id="eadf1-141">Kui teil palutakse lasta oma organisatsioonil seadet hallata, valige **Ainult see rakendus**.</span><span class="sxs-lookup"><span data-stu-id="eadf1-141">When you're prompted to let your organization manage the device, select **This app only**.</span></span>
7. <span data-ttu-id="eadf1-142">Kui aktiveerimine on lõpule viidud, valige **Alustamine**.</span><span class="sxs-lookup"><span data-stu-id="eadf1-142">When activation is completed, select **Get started**.</span></span>

### <a name="enable-bopis-in-modern-pos"></a><span data-ttu-id="eadf1-143">BOPIS-i lubamine rakenduses Modern POS</span><span class="sxs-lookup"><span data-stu-id="eadf1-143">Enable BOPIS in Modern POS</span></span>

1. <span data-ttu-id="eadf1-144">Logige rakendusse Modern POS sisse, kasutades operaatori ID-d **000713** ja parooli **123**.</span><span class="sxs-lookup"><span data-stu-id="eadf1-144">Sign in to Modern POS by using **000713** as the operator ID and **123** as the password.</span></span>
2. <span data-ttu-id="eadf1-145">Sissejuhatava video esitamise ajal märkige dialoogiboksi alumises vasakus nurgas kaks ruutu ja sulgege seejärel dialoogiboks.</span><span class="sxs-lookup"><span data-stu-id="eadf1-145">While the introductory walkthrough video is playing, select the two check boxes in the lower-left corner of the dialog box, and then close the dialog box.</span></span>
3. <span data-ttu-id="eadf1-146">Kui teil ei paluta vahetust sulgeda, kerige **Tervituslehel** paremale, valige käsk **Sule vahetus** ja seejärel logige kassasse tagasi sisse.</span><span class="sxs-lookup"><span data-stu-id="eadf1-146">If you aren't prompted to close the shift, scroll to the right on the **Welcome** page, select **Close shift**, and then sign back in to the POS.</span></span>
4. <span data-ttu-id="eadf1-147">Pärast sisselogimist, valige **Kassavälise toimingu tegemine**, kui teilt seda küsitakse.</span><span class="sxs-lookup"><span data-stu-id="eadf1-147">After you're signed in, when you're prompted, select **Perform a non-drawer operation**.</span></span>
5. <span data-ttu-id="eadf1-148">Kerige **Tervituslehel** paremale ja valige toiming **Riistvarajaama valimine**.</span><span class="sxs-lookup"><span data-stu-id="eadf1-148">On the **Welcome** page, scroll to the right, and select the **Select hardware station** operation.</span></span>
6. <span data-ttu-id="eadf1-149">Valige **Halda**, seadke suvandi **Riistvarajaama kasutamine** väärtuseks **Sees** ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="eadf1-149">Select **Manage**, set the **Use hardware station** option to **On**, and then select **OK**.</span></span>
7. <span data-ttu-id="eadf1-150">Logige kassast välja ja siis uuesti sisse.</span><span class="sxs-lookup"><span data-stu-id="eadf1-150">Sign out of the POS, and then sign back in.</span></span>
8. <span data-ttu-id="eadf1-151">Kui olete sisse loginud, valige **Ava uus vahetus** ja seejärel valige **Sahtel**.</span><span class="sxs-lookup"><span data-stu-id="eadf1-151">After you're signed in, select **Open a new shift**, and then select **Drawer**.</span></span>

## <a name="complete-a-bopis-scenario"></a><span data-ttu-id="eadf1-152">BOPISi stsenaariumi lõpuleviimine</span><span class="sxs-lookup"><span data-stu-id="eadf1-152">Complete a BOPIS scenario</span></span>

### <a name="create-a-storefront-order-for-in-store-pickup"></a><span data-ttu-id="eadf1-153">Poetellimuse loomine kauplusest kättesaamise jaoks</span><span class="sxs-lookup"><span data-stu-id="eadf1-153">Create a storefront order for in-store pickup</span></span>

1. <span data-ttu-id="eadf1-154">Minge URL-i juurde, mille määrasite keskkonna konfigureerimise ajal sammu [E-kaubanduse lähtestamine](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce) käigus.</span><span class="sxs-lookup"><span data-stu-id="eadf1-154">Go to the URL that you specified in the [Initialize e-Commerce](https://docs.microsoft.com/dynamics365/commerce/provisioning-guide#initialize-e-commerce) step during environment configuration.</span></span>
2. <span data-ttu-id="eadf1-155">Valige kaup ja valige **Lisa ostukorvi**.</span><span class="sxs-lookup"><span data-stu-id="eadf1-155">Select an item, and select **Add to cart**.</span></span>
3. <span data-ttu-id="eadf1-156">Ostukorvi lehel valige äsja loodud tellimuse rea jaoks **Tulen järele**.</span><span class="sxs-lookup"><span data-stu-id="eadf1-156">On the shopping bag page, select **Pick this up** for the order line that you just added.</span></span>
4. <span data-ttu-id="eadf1-157">Dialoogiboksis **Kaupluse valimine** sisestage **San Francisco** ja seejärel klõpsake nuppu **Otsi**.</span><span class="sxs-lookup"><span data-stu-id="eadf1-157">In the **Select a store** dialog box, enter **San Francisco**, and then select the **Search** button.</span></span>
5. <span data-ttu-id="eadf1-158">Leidke otsingutulemustest San Francisco kauplus ja valige **Tulen siia järele**.</span><span class="sxs-lookup"><span data-stu-id="eadf1-158">In the list of results, find the San Francisco store, and select **Pick up here**.</span></span>
6. <span data-ttu-id="eadf1-159">Valige ostukorvi lehel valik **Külalisena maksmine**.</span><span class="sxs-lookup"><span data-stu-id="eadf1-159">On the shopping bag page, select **Checkout as Guest**.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="eadf1-160">Maksmise jätkamiseks peate küpsiseteatisega nõustuma.</span><span class="sxs-lookup"><span data-stu-id="eadf1-160">To continue with checkout, you must accept the cookie notice.</span></span> <span data-ttu-id="eadf1-161">See teade kuvatakse maksmislehe üleval ribana.</span><span class="sxs-lookup"><span data-stu-id="eadf1-161">This notice appears as a banner at the top of the checkout page.</span></span>

7. <span data-ttu-id="eadf1-162">Krediitkaardiga maksmise puhul sisestage järgmised üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="eadf1-162">For the credit card payment method, enter the following details:</span></span>

    - <span data-ttu-id="eadf1-163">**Kaardiomaniku nimi:** sisestage mis tahes nimi.</span><span class="sxs-lookup"><span data-stu-id="eadf1-163">**Cardholder name:** Enter any name.</span></span>
    - <span data-ttu-id="eadf1-164">**Kaardi number:** sisestage **4111-1111-1111-1111**.</span><span class="sxs-lookup"><span data-stu-id="eadf1-164">**Card number:** Enter **4111-1111-1111-1111**.</span></span>
    - <span data-ttu-id="eadf1-165">**Aegumiskuupäev:** sisestage **10/20**.</span><span class="sxs-lookup"><span data-stu-id="eadf1-165">**Expiration date:** Enter **10/20**.</span></span>
    - <span data-ttu-id="eadf1-166">**Kaardi tõendamise väärtuse (CVV) kood:** sisestage **737**.</span><span class="sxs-lookup"><span data-stu-id="eadf1-166">**Card verification value (CVV) code:** Enter **737**.</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="eadf1-167">Te ei tohiks proovida kasutada tegeliku krediitkaardi teavet testi tegevuskohas mitte ühelgi juhul.</span><span class="sxs-lookup"><span data-stu-id="eadf1-167">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

8. <span data-ttu-id="eadf1-168">Jätkake maksmist, sisestades arve aadressi üksikasjad ja seejärel valige **Salvesta ja jätka**.</span><span class="sxs-lookup"><span data-stu-id="eadf1-168">Continue with checkout by entering details of the billing address, and then select **Save and continue**.</span></span>
9. <span data-ttu-id="eadf1-169">Kui tellimus on valmis, valige **Maksmine**.</span><span class="sxs-lookup"><span data-stu-id="eadf1-169">When the order is ready to be placed, select **Checkout**.</span></span>

### <a name="synchronize-online-orders-to-the-back-office"></a><span data-ttu-id="eadf1-170">Võrgutellimuste sünkroonimine kontoriga</span><span class="sxs-lookup"><span data-stu-id="eadf1-170">Synchronize online orders to the back office</span></span>

<span data-ttu-id="eadf1-171">Lisateavet võrgutellimuste sünkroonimise kohta vaadake teemast [Veebimüügi ja -maksete sisestamine](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments).</span><span class="sxs-lookup"><span data-stu-id="eadf1-171">For information about how to synchronize online orders, see [Posting of online sales and payments](https://docs.microsoft.com/dynamics365/commerce/tasks/posting-online-sales-payments).</span></span>

### <a name="pick-up-an-order-in-the-store"></a><span data-ttu-id="eadf1-172">Tellimuse kättesaamine kauplusest</span><span class="sxs-lookup"><span data-stu-id="eadf1-172">Pick up an order in the store</span></span>

1. <span data-ttu-id="eadf1-173">Logige kassasse sisse.</span><span class="sxs-lookup"><span data-stu-id="eadf1-173">Sign in to the POS.</span></span>
2. <span data-ttu-id="eadf1-174">Valige **Tervitusekraanil** suvand **Tellimuse täitmine**</span><span class="sxs-lookup"><span data-stu-id="eadf1-174">On the **Welcome** screen, select **Order fulfillment**</span></span>
3. <span data-ttu-id="eadf1-175">Valige kättesaamiseks mõeldud kaupade loendist võrgus tehtud tellimuse rida.</span><span class="sxs-lookup"><span data-stu-id="eadf1-175">In the list of items for pickup, select the line from the order that was placed online.</span></span>
4. <span data-ttu-id="eadf1-176">Kui tellimuse rida on valitud, valige **Kättesaamine**.</span><span class="sxs-lookup"><span data-stu-id="eadf1-176">While the order line is selected, select **Pick up**.</span></span>

    <span data-ttu-id="eadf1-177">Rea kaup lisatakse tehingu ekraanile ja makstav summa on **0,00 $**.</span><span class="sxs-lookup"><span data-stu-id="eadf1-177">The line item is added to the transaction screen, and **$0.00** is shown as the balance that is due.</span></span>

5. <span data-ttu-id="eadf1-178">Valige makstav summa **0,00 $** või valige tehingu tegemiseks mis tahes makseviis.</span><span class="sxs-lookup"><span data-stu-id="eadf1-178">Select the balance due of **$0.00**, or select any payment method to conclude the transaction.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="eadf1-179">Tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="eadf1-179">Troubleshooting</span></span>

### <a name="online-orders-that-are-retrieved-in-the-pos-have-a-non-zero-balance-due"></a><span data-ttu-id="eadf1-180">Kassasse toodud võrgutellimustel on nullist erinev summa</span><span class="sxs-lookup"><span data-stu-id="eadf1-180">Online orders that are retrieved in the POS have a non-zero balance due</span></span>

<span data-ttu-id="eadf1-181">Kui tellimusele tullakse kauplusesse järele, veenduge juhul, kui summa pole 0 (null), et Modern POS oleks kasutusel ja et riistvarajaam oleks aktiivne.</span><span class="sxs-lookup"><span data-stu-id="eadf1-181">When an order is retrieved for in-store pickup, if the balance due isn't 0 (zero), make sure that Modern POS is being used, and that the hardware station is active.</span></span> <span data-ttu-id="eadf1-182">Kui kasutatakse Cloud POS-i või Modern POS-i iOS-i jaoks, veenduge, et ühiskasutatav riistvarajaam oleks aktiivne.</span><span class="sxs-lookup"><span data-stu-id="eadf1-182">If Cloud POS or Modern POS for iOS is being used, make sure that a shared hardware station is active.</span></span> <span data-ttu-id="eadf1-183">Internetis tehtud maksete toomiseks on vaja mingit tüüpi aktiivset riistvarajaama.</span><span class="sxs-lookup"><span data-stu-id="eadf1-183">Some form of active hardware station is required to retrieve payments that were made online.</span></span>

### <a name="general-issues-with-payment-capture"></a><span data-ttu-id="eadf1-184">Üldised probleemid makse hõivamisega</span><span class="sxs-lookup"><span data-stu-id="eadf1-184">General issues with payment capture</span></span>

<span data-ttu-id="eadf1-185">Kõigi üldiste probleemide puhul peaksite alati esimesena uurima Modern POS-i või interneti teabeteenuste haldamise (IIS) riistvarajaama sündmustelogisid.</span><span class="sxs-lookup"><span data-stu-id="eadf1-185">For all general issues, you should always consult the Modern POS or Internet Information Services (IIS) Hardware Station event logs as a first step.</span></span> <span data-ttu-id="eadf1-186">Need logid leiate Windowsi sündmustelogi järgmistes sõlmedes.</span><span class="sxs-lookup"><span data-stu-id="eadf1-186">You can find these logs under the following nodes in the Windows event log:</span></span>

- <span data-ttu-id="eadf1-187">Rakenduste ja teenuste logid \> Microsoft \> Dynamics \> Commerce – Modern POS</span><span class="sxs-lookup"><span data-stu-id="eadf1-187">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-ModernPOS</span></span>
- <span data-ttu-id="eadf1-188">Rakenduste ja teenuste logid \> Microsoft \> Dynamics \> Commerce – riistvarajaam</span><span class="sxs-lookup"><span data-stu-id="eadf1-188">Application and Services Logs \> Microsoft \> Dynamics \> Commerce-Hardware Station</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eadf1-189">Lisaressursid</span><span class="sxs-lookup"><span data-stu-id="eadf1-189">Additional resources</span></span>

[<span data-ttu-id="eadf1-190">Dynamics 365 Commerce’i eelvaatekeskkonna ülevaade</span><span class="sxs-lookup"><span data-stu-id="eadf1-190">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="eadf1-191">Dynamics 365 Commerce'i eelvaatekeskkonna ettevalmistamine</span><span class="sxs-lookup"><span data-stu-id="eadf1-191">Provision a Dynamics 365 Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="eadf1-192">Dynamics 365 Commerce’i eelvaatekeskkonna valikuliste funktsioonide konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="eadf1-192">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="eadf1-193">Dynamics 365 Commerce eelvaatekeskkonna KKK</span><span class="sxs-lookup"><span data-stu-id="eadf1-193">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="eadf1-194">Microsofti elutsükli teenused (LCS)</span><span class="sxs-lookup"><span data-stu-id="eadf1-194">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="eadf1-195">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="eadf1-195">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="eadf1-196">Microsoft Azure'i portaal</span><span class="sxs-lookup"><span data-stu-id="eadf1-196">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="eadf1-197">Dynamics 365 Commerce veebisait</span><span class="sxs-lookup"><span data-stu-id="eadf1-197">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="eadf1-198">Adyeni makse ülekandmine</span><span class="sxs-lookup"><span data-stu-id="eadf1-198">Adyen payment connector</span></span>](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector?tabs=8-1-3)

[<span data-ttu-id="eadf1-199">Veebimaksevahendite salvestamine Adyeni konnektori abil</span><span class="sxs-lookup"><span data-stu-id="eadf1-199">Saving online payment instruments with the Adyen connector</span></span>](https://docs.microsoft.com/dynamics365/commerce/dev-itpro/adyen-connector-listpi)

[<span data-ttu-id="eadf1-200">Omnikanali maksete ülevaade</span><span class="sxs-lookup"><span data-stu-id="eadf1-200">Omni-channel payments overview</span></span>](https://docs.microsoft.com/dynamics365/commerce/omni-channel-payments)
