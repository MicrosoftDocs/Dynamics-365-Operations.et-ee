---
title: Väikepaki saatmine
description: Sellest teemast leiate teavet väikepaki saatmise (SPS) funktsiooni kohta. See funktsioon võimaldab rakendusel Microsoft Dynamics 365 Supply Chain Management esitada üksikasju pakitud konteineri kohta vedajale ja seejärel saada sellelt vedajalt tagasi saadetise silt, tarnemäär ja jälgimisnumber.
author: Mirzaab
manager: tfehr
ms.date: 01/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRateEngine, TMSCarrier, CustTable, TMSShippingCarrierCustomerAccount, TMSSmallParcelShippingFeature
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-08
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 350193a0054ef879ece3dd2dfcc4105476981837
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 01/28/2021
ms.locfileid: "5078253"
---
# <a name="small-parcel-shipping"></a><span data-ttu-id="b1775-104">Väikepaki saatmine</span><span class="sxs-lookup"><span data-stu-id="b1775-104">Small parcel shipping</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1775-105">Väikepaki saatmise (SPS) funktsioon võimaldab rakendusel Microsoft Dynamics 365 Supply Chain Management suhelda otse vedajatega, pakkudes raamistikku vedaja API-de kaudu suhtlemiseks.</span><span class="sxs-lookup"><span data-stu-id="b1775-105">The small parcel shipping (SPS) feature enables Microsoft Dynamics 365 Supply Chain Management to interact directly with shipping carriers by providing a framework for communication through carrier APIs.</span></span> <span data-ttu-id="b1775-106">See funktsioon on kasulik, kui saadate individuaalseid müügitellimusi kommertsvedajate kaudu, mitte kasutades konteineriga saatmist või vähem kui koormatäis (LTL) saatmist.</span><span class="sxs-lookup"><span data-stu-id="b1775-106">This functionality is useful when you're shipping individual sales orders via commercial shipping carriers instead of using container shipping or less-than-truckload (LTL) shipping.</span></span>

<span data-ttu-id="b1775-107">SPS-i funktsioon suhtleb teie saadetise vedajaga spetsiaalse *määramootori* kaudu.</span><span class="sxs-lookup"><span data-stu-id="b1775-107">The SPS feature interacts with your shipping carrier through a dedicated *rate engine*.</span></span> <span data-ttu-id="b1775-108">Teie organisatsioon peab selle määramootori välja töötama koos teie vedaja või vedaja keskuse teenusega.</span><span class="sxs-lookup"><span data-stu-id="b1775-108">Your organization must develop this rate engine in collaboration with your carrier or carrier hub service.</span></span> <span data-ttu-id="b1775-109">Määramootor võimaldab rakendusel Supply Chain Management esitada üksikasju pakitud konteineri kohta teie vedajale ja seejärel saada sellelt vedajalt tagasi saadetise silt, tarnemäär ja jälgimisnumber.</span><span class="sxs-lookup"><span data-stu-id="b1775-109">The rate engine enables Supply Chain Management to submit details about a packed container to your carrier, and then receive a shipping label, shipping rate, and tracking number back from that carrier.</span></span>

<span data-ttu-id="b1775-110">Tagastatav tarnemäär lisatakse seotud müügitellimusele lisakuluna.</span><span class="sxs-lookup"><span data-stu-id="b1775-110">The shipping rate that is returned is added to the associated sales order as a miscellaneous charge.</span></span> <span data-ttu-id="b1775-111">Tagastatud saadetise sildi saab seejärel automaatselt printida, kasutades Zebra programmeerimiskeelega (ZPL) printerit ja kinnitada saadetisele.</span><span class="sxs-lookup"><span data-stu-id="b1775-111">The shipping label that is returned can then automatically be printed by using a Zebra Programming Language (ZPL) printer and applied to the shipment.</span></span> <span data-ttu-id="b1775-112">Vedaja skannib selle saadetise silti, kui võtab pakid teie laos peale.</span><span class="sxs-lookup"><span data-stu-id="b1775-112">The carrier will scan this shipping label when it picks up the packages at your warehouse.</span></span>

## <a name="prepare-your-system-to-support-sps"></a><span data-ttu-id="b1775-113">Süsteemi ettevalmistamine SPS-i toetamiseks</span><span class="sxs-lookup"><span data-stu-id="b1775-113">Prepare your system to support SPS</span></span>

<span data-ttu-id="b1775-114">Enne SPS-i funktsiooni kasutamist peate SPS-i funktsiooni funktsioonihalduses sisse lülitama, lisama oma määramootori ning häälestama selle toetamiseks moodulid **Transpordihaldus** ja **Laohaldus**.</span><span class="sxs-lookup"><span data-stu-id="b1775-114">Before you can start to use SPS functionality, you must turn on the SPS feature in Feature management, add your rate engine, and set up the **Transportation management** and **Warehouse management** modules to support it.</span></span>

### <a name="turn-on-the-sps-feature"></a><span data-ttu-id="b1775-115">Funktsiooni SPS sisselülitamine</span><span class="sxs-lookup"><span data-stu-id="b1775-115">Turn on the SPS feature</span></span>

<span data-ttu-id="b1775-116">Enne selle funktsiooni SPS kasutamist peate selle oma süsteemis sisse lülitama.</span><span class="sxs-lookup"><span data-stu-id="b1775-116">Before you can use the SPS feature, it must be turned on in your system.</span></span> <span data-ttu-id="b1775-117">Administraatorid saavad kasutada [Funktsioonihalduse](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) tööruumi, et kontrollida funktsiooni olekut ja vajadusel selle sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="b1775-117">Administrators can use the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="b1775-118">Seega on funktsioon loetletud järgmisel viisil.</span><span class="sxs-lookup"><span data-stu-id="b1775-118">There, the feature is listed in the following way:</span></span>

- <span data-ttu-id="b1775-119">**Moodul:** *Transpordihaldus*</span><span class="sxs-lookup"><span data-stu-id="b1775-119">**Module:** *Transportation management*</span></span>
- <span data-ttu-id="b1775-120">**Funktsiooni nimi:** *Väikepaki saatmine*</span><span class="sxs-lookup"><span data-stu-id="b1775-120">**Feature name:** *Small parcel shipping*</span></span>

### <a name="deploy-and-set-up-rate-engines"></a><span data-ttu-id="b1775-121">Määramootorite juurutamine ja häälestamine</span><span class="sxs-lookup"><span data-stu-id="b1775-121">Deploy and set up rate engines</span></span>

<span data-ttu-id="b1775-122">Supply Chain Management ei sisalda ühtegi määramootorit.</span><span class="sxs-lookup"><span data-stu-id="b1775-122">Supply Chain Management doesn't include any rate engines.</span></span> <span data-ttu-id="b1775-123">Teil tuleb hankida või luua mis tahes nõutav määramootor ja seejärel lisada see oma süsteemile.</span><span class="sxs-lookup"><span data-stu-id="b1775-123">You must obtain or create any rate engines that you require, and then add them to your system.</span></span> <span data-ttu-id="b1775-124">Samas pakub Microsoft määramootori demoversiooni, mida saate kasutada testimiseks.</span><span class="sxs-lookup"><span data-stu-id="b1775-124">However, Microsoft provides a demo rate engine that you can use for testing.</span></span>

#### <a name="download-and-deploy-the-demo-rate-engine"></a><span data-ttu-id="b1775-125">Määramootori demoversiooni allalaadimine ja juurutamine</span><span class="sxs-lookup"><span data-stu-id="b1775-125">Download and deploy the demo rate engine</span></span>

<span data-ttu-id="b1775-126">Määramootori demoversiooni hankimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="b1775-126">Follow these steps to get the demo rate engine.</span></span>

1. <span data-ttu-id="b1775-127">Laadige GitHubis alla [määramootori demoversiooni dünaamilise lingiga teek (DLL)](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS).</span><span class="sxs-lookup"><span data-stu-id="b1775-127">On GitHub, download the [dynamic-link library (DLL) for the demo rate engine](https://github.com/microsoft/Dynamics-365-FastTrack-Implementation-Assets/tree/master/SCM/SPS).</span></span>
1. <span data-ttu-id="b1775-128">Salvestage DLL oma Supply Chain Managementi serveris kaustas **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin**.</span><span class="sxs-lookup"><span data-stu-id="b1775-128">On your Supply Chain Management server, save the DLL in the **\\AOSService\\PackagesLocalDirectory\\ApplicationSuite\\bin** folder.</span></span>

#### <a name="create-and-deploy-functional-rate-engines"></a><span data-ttu-id="b1775-129">Funktsionaalsete määramootorite loomine ja juurutamine</span><span class="sxs-lookup"><span data-stu-id="b1775-129">Create and deploy functional rate engines</span></span>

<span data-ttu-id="b1775-130">Lisateavet selle kohta, kuidas funktsiooni määramootoreid luua ja juurutada nii, et neid saaks kasutada tootmis- või katsekeskkonnas, vaadake järgmistest teemadest.</span><span class="sxs-lookup"><span data-stu-id="b1775-130">For information about how to create and deploy functional rate engines so that they can be used in a production or test environment, see the following topics:</span></span>

- [<span data-ttu-id="b1775-131">Uue transpordihalduse mootori loomine</span><span class="sxs-lookup"><span data-stu-id="b1775-131">Create a new transportation management engine</span></span>](../transportation/create-new-transportation-management-engine.md)
- [<span data-ttu-id="b1775-132">Transpordihalduse mootorite häälestamine</span><span class="sxs-lookup"><span data-stu-id="b1775-132">Set up transportation management engines</span></span>](https://docs.microsoft.com/dynamicsax-2012/appuser-itpro/set-up-transportation-management-engines)

<span data-ttu-id="b1775-133">Lisateavet SPS-i määramootori loomise kohta vt järgmiselt ajaveebipostitusest [Väikepaki saatmine: kuidas kasutada väikepaki saatmise funktsiooni rakenduses Microsoft Dynamics 365](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).</span><span class="sxs-lookup"><span data-stu-id="b1775-133">For more information about how to create an SPS rate engine, see the following blog post: [Small Parcel Shipping: How to leverage small parcel shipping functionality in Microsoft Dynamics 365](https://hub.bhsolutions.com/creating-a-mock-parcel-engine-in-d365?submissionGuid=46a1fccf-80b0-4b70-a6a0-4bf45a8756b5).</span></span>

#### <a name="set-up-a-rate-engine-in-supply-chain-management"></a><span data-ttu-id="b1775-134">Määramootori häälestamine Supply Chain Managementis</span><span class="sxs-lookup"><span data-stu-id="b1775-134">Set up a rate engine in Supply Chain Management</span></span>

<span data-ttu-id="b1775-135">Pärast SPS-i määramootori loomist ja juurutamist järgige selle häälestamiseks järgmisi juhiseid.</span><span class="sxs-lookup"><span data-stu-id="b1775-135">After you've created and deployed a rate engine for SPS, follow these steps to set it up.</span></span>

1. <span data-ttu-id="b1775-136">Avage **Transpordihaldus \> Seadistus \> Mootorid \> Määramootor**.</span><span class="sxs-lookup"><span data-stu-id="b1775-136">Go to **Transportation management \> Setup \> Engines \> Rate engine**.</span></span>
1. <span data-ttu-id="b1775-137">Valige toimingupaanil suvand **Uus**, et lisada ruudustikku rida.</span><span class="sxs-lookup"><span data-stu-id="b1775-137">On the Action Pane, select **New** to add a row to the grid.</span></span>
1. <span data-ttu-id="b1775-138">Määrake uuel real järgmised väljad.</span><span class="sxs-lookup"><span data-stu-id="b1775-138">In the new row, set the following fields:</span></span>

    - <span data-ttu-id="b1775-139">**Hindamise mootor** – sisestage määramootori kordumatu nimi.</span><span class="sxs-lookup"><span data-stu-id="b1775-139">**Rating engine** – Enter a unique name for the rate engine.</span></span> <span data-ttu-id="b1775-140">Kui kasutate määramootori demoversiooni, sisestage *Määramootori demoversioon*.</span><span class="sxs-lookup"><span data-stu-id="b1775-140">If you're using the demo rate engine, enter *Demo rate engine*.</span></span>
    - <span data-ttu-id="b1775-141">**Nimi** – sisestage määramootori lühikirjeldus.</span><span class="sxs-lookup"><span data-stu-id="b1775-141">**Name** – Enter a short description of the rate engine.</span></span> <span data-ttu-id="b1775-142">Kui kasutate määramootori demoversiooni, sisestage *Määramootori demoversioon*.</span><span class="sxs-lookup"><span data-stu-id="b1775-142">If you're using the demo rate engine, enter *Demo rate engine*.</span></span>
    - <span data-ttu-id="b1775-143">**Hindamise metaandmete ID** – valige alus, mida tuleks kasutada määra arvutamiseks.</span><span class="sxs-lookup"><span data-stu-id="b1775-143">**Rating metadata ID** – Select the basis that should be used to calculate your rate.</span></span> <span data-ttu-id="b1775-144">Näiteks võib teie hinnamäära arvutada vahemaa põhjal.</span><span class="sxs-lookup"><span data-stu-id="b1775-144">For example, your rate might be calculated based on distance.</span></span> <span data-ttu-id="b1775-145">Kui kasutate määramootori demoversiooni, võite selle välja tühjaks jätta.</span><span class="sxs-lookup"><span data-stu-id="b1775-145">If you're using the demo rate engine, you can leave this field blank.</span></span>
    - <span data-ttu-id="b1775-146">**Mootori komplekt** – sisestage juurutatud DLL-i paketi failinimi.</span><span class="sxs-lookup"><span data-stu-id="b1775-146">**Engine assembly** – Enter the file name of the DLL package that you deployed.</span></span> <span data-ttu-id="b1775-147">Kui kasutate määramootori demoversiooni, sisestage *TMSSmallParcelShippingEngine.dll*.</span><span class="sxs-lookup"><span data-stu-id="b1775-147">If you're using the demo rate engine, enter *TMSSmallParcelShippingEngine.dll*.</span></span>
    - <span data-ttu-id="b1775-148">**Mootori klass** – sisestage klassi nimi, mis loodi teie määramootori jaoks.</span><span class="sxs-lookup"><span data-stu-id="b1775-148">**Engine class** – Enter the class name that was established for your rate engine.</span></span> <span data-ttu-id="b1775-149">Kui kasutate määramootori demoversiooni, sisestage *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*.</span><span class="sxs-lookup"><span data-stu-id="b1775-149">If you're using the demo rate engine, enter *TMSSmallParcelShippingEngine.SmallParcelShippingRateEngine*.</span></span>

## <a name="example-scenario"></a><span data-ttu-id="b1775-150">Näidisstsenaarium</span><span class="sxs-lookup"><span data-stu-id="b1775-150">Example scenario</span></span>

<span data-ttu-id="b1775-151">See näidise stsenaarium näitab, kuidas SPS-i seadistada ja kasutada pärast seda, kui olete oma süsteemi selles teemas kirjeldatud viisil ette valmistanud.</span><span class="sxs-lookup"><span data-stu-id="b1775-151">This example scenario shows how to set up and use SPS after you've prepared your system as described earlier in this topic.</span></span> <span data-ttu-id="b1775-152">See stsenaarium kasutab eelnevalt mainitud määramootori demoversiooni.</span><span class="sxs-lookup"><span data-stu-id="b1775-152">This scenario uses the previously mentioned demo rate engine.</span></span>

### <a name="make-demo-data-available"></a><span data-ttu-id="b1775-153">Demoandmete kättesaadavaks tegemine</span><span class="sxs-lookup"><span data-stu-id="b1775-153">Make demo data available</span></span>

<span data-ttu-id="b1775-154">Selle stsenaariumi kasutamiseks siin määratud demokirjete ja -väärtuste abil, peate kasutama süsteemi, kuhu on installitud standardsed [demoandmed](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md).</span><span class="sxs-lookup"><span data-stu-id="b1775-154">To work through this scenario by using the demo records and values that are specified here, you must be on a system where the standard [demo data](../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="b1775-155">Enne alustamist peate valima ka juriidilise isiku **USMF**.</span><span class="sxs-lookup"><span data-stu-id="b1775-155">Additionally, you must select the **USMF** legal entity before you begin.</span></span>

### <a name="set-up-the-scenario"></a><span data-ttu-id="b1775-156">Stsenaariumi seadistamine</span><span class="sxs-lookup"><span data-stu-id="b1775-156">Set up the scenario</span></span>

<span data-ttu-id="b1775-157">Selle näite stsenaariumi korral peab teil olema demo vedaja, vedaja grupp, pakkimispoliitika ja pakkimisprofiil.</span><span class="sxs-lookup"><span data-stu-id="b1775-157">For this example scenario, you must have a demo carrier, carrier group, packing policy, and packing profile.</span></span> <span data-ttu-id="b1775-158">Järgmistes alamjaotistes seletatakse, kuidas valmistada ette stsenaariumi jaoks vajalikke kirjeid.</span><span class="sxs-lookup"><span data-stu-id="b1775-158">The following subsections explain how to prepare the records that are required for the scenario.</span></span> <span data-ttu-id="b1775-159">Tootmisstsenaariumis sarnaneb seadistusprotsess tavaliselt siin kirjeldatud protsessile.</span><span class="sxs-lookup"><span data-stu-id="b1775-159">In a production scenario, the setup process typically resembles the process that is described here.</span></span> <span data-ttu-id="b1775-160">Samas määrate te erinevad väärtused.</span><span class="sxs-lookup"><span data-stu-id="b1775-160">However, you will set different values.</span></span>

#### <a name="set-up-carriers"></a><span data-ttu-id="b1775-161">Vedajate häälestamine</span><span class="sxs-lookup"><span data-stu-id="b1775-161">Set up carriers</span></span>

<span data-ttu-id="b1775-162">Vedaja häälestamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="b1775-162">Follow these steps to set up a carrier.</span></span>

1. <span data-ttu-id="b1775-163">Avage jaotis **Transpordihaldus \> Seadistus \> Vedajad \> Kättetoimetajad**.</span><span class="sxs-lookup"><span data-stu-id="b1775-163">Go to **Transportation management \> Setup \> Carriers \> Shipping carriers**.</span></span>
1. <span data-ttu-id="b1775-164">Vedaja lisamiseks valige toimingupaanilt suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="b1775-164">On the Action Pane, select **New** to add a carrier.</span></span>
1. <span data-ttu-id="b1775-165">Määrake päises järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="b1775-165">On the header, set the following values:</span></span>

    - <span data-ttu-id="b1775-166">**Saadetise vedaja:** *demo vedaja*</span><span class="sxs-lookup"><span data-stu-id="b1775-166">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="b1775-167">**Nimi:** *demo vedaja*</span><span class="sxs-lookup"><span data-stu-id="b1775-167">**Name:** *Demo Carrier*</span></span>
    - <span data-ttu-id="b1775-168">**Viis:** *maismaa*</span><span class="sxs-lookup"><span data-stu-id="b1775-168">**Mode:** *Ground*</span></span>

1. <span data-ttu-id="b1775-169">Määrake kiirkaardil **Ülevaade** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="b1775-169">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b1775-170">**Aktiveeri saadetise vedaja:** *jah*</span><span class="sxs-lookup"><span data-stu-id="b1775-170">**Activate shipping carrier:** *Yes*</span></span>
    - <span data-ttu-id="b1775-171">**Aktiveeri vedaja hinnang:** *jah*</span><span class="sxs-lookup"><span data-stu-id="b1775-171">**Activate carrier rating:** *Yes*</span></span>

1. <span data-ttu-id="b1775-172">Valige kiirkaardil **Teenused** suvand **Uus**, et lisada teenus ruudustikku.</span><span class="sxs-lookup"><span data-stu-id="b1775-172">On the **Services** FastTab, select **New** to add a service to the grid.</span></span>
1. <span data-ttu-id="b1775-173">Määrake uue teenuse jaoks järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="b1775-173">Set the following values for the new service:</span></span>

    - <span data-ttu-id="b1775-174">**Vedaja teenus:** *demo vedamisteenus*</span><span class="sxs-lookup"><span data-stu-id="b1775-174">**Carrier service:** *Demo carrier service*</span></span>
    - <span data-ttu-id="b1775-175">**Nimi:** *demo vedamisteenus*</span><span class="sxs-lookup"><span data-stu-id="b1775-175">**Name:** *Demo carrier service*</span></span>
    - <span data-ttu-id="b1775-176">**Transpordiviis:** *maapind*</span><span class="sxs-lookup"><span data-stu-id="b1775-176">**Transportation method:** *Ground*</span></span>

    <span data-ttu-id="b1775-177">Sisestage nõutud väärtused kõigi muude väljade jaoks.</span><span class="sxs-lookup"><span data-stu-id="b1775-177">Enter arbitrary values for all the other fields, as required.</span></span> <span data-ttu-id="b1775-178">(Kui salvestate uue saadetise vedaja kirje, luuakse uus tarneviis ja väli **Tarneviis** määratakse automaatselt.)</span><span class="sxs-lookup"><span data-stu-id="b1775-178">(When you save the new shipping carrier record, a new mode of delivery will be created, and the **Mode of delivery** field will be set automatically.)</span></span>

1. <span data-ttu-id="b1775-179">Hinnanguprofiili lisamiseks valige ruudustikus kiirkaardil **Hindamise profiilid** suvand **Uus**.</span><span class="sxs-lookup"><span data-stu-id="b1775-179">On the **Rating profiles** FastTab, select **New** to add a rating profile to the grid.</span></span>
1. <span data-ttu-id="b1775-180">Määrake uue profiili jaoks järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="b1775-180">Set the following values for the new profile:</span></span>

    - <span data-ttu-id="b1775-181">**Hindamise profiil:** *demo vedamisteenus*</span><span class="sxs-lookup"><span data-stu-id="b1775-181">**Rating profile:** *Demo carrier service*</span></span>
    - <span data-ttu-id="b1775-182">**Nimi:** *demo vedamisteenus*</span><span class="sxs-lookup"><span data-stu-id="b1775-182">**Name:** *Demo carrier service*</span></span>
    - <span data-ttu-id="b1775-183">**Määramootor:** *määramootori demoversioon*</span><span class="sxs-lookup"><span data-stu-id="b1775-183">**Rate engine:** *Demo rate engine*</span></span>

    <span data-ttu-id="b1775-184">Sisestage nõutud väärtused kõigi muude väljade jaoks.</span><span class="sxs-lookup"><span data-stu-id="b1775-184">Enter arbitrary values for all the other fields, as required.</span></span>

1. <span data-ttu-id="b1775-185">Valige toimingupaanil nupp **Salvesta**.</span><span class="sxs-lookup"><span data-stu-id="b1775-185">On the Action Pane, select **Save**.</span></span>

<span data-ttu-id="b1775-186">Lisateavet vedajate seadistamise kohta vt teemast [Vedajate häälestus](../transportation/tasks/set-up-shipping-carriers.md).</span><span class="sxs-lookup"><span data-stu-id="b1775-186">For more information about how to set up carriers, see [Set up shipping carriers](../transportation/tasks/set-up-shipping-carriers.md).</span></span>

#### <a name="set-up-carrier-service-accounts"></a><span data-ttu-id="b1775-187">Vedaja teenusekontode häälestamine</span><span class="sxs-lookup"><span data-stu-id="b1775-187">Set up carrier service accounts</span></span>

<span data-ttu-id="b1775-188">Vedaja teenusekonto häälestamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="b1775-188">Follow these steps to set up a carrier service account.</span></span>

1. <span data-ttu-id="b1775-189">Avage **Transpordihaldus \> Seadistus \> Hinnang \> Vedaja teenusekonto**.</span><span class="sxs-lookup"><span data-stu-id="b1775-189">Go to **Transportation management \> Setup \> Rating \> Carrier service account**.</span></span>
1. <span data-ttu-id="b1775-190">Valige toimingupaanil suvand **Uus**, et lisada vedaja teenusekonto.</span><span class="sxs-lookup"><span data-stu-id="b1775-190">On the Action Pane, select **New** to add a carrier service account.</span></span>
1. <span data-ttu-id="b1775-191">Määrake uue konto jaoks järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="b1775-191">Set the following values for the new account:</span></span>

    - <span data-ttu-id="b1775-192">**Saadetise vedaja:** *demo vedaja*</span><span class="sxs-lookup"><span data-stu-id="b1775-192">**Shipping Carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="b1775-193">**Vedaja teenus:** *demo vedamisteenus*</span><span class="sxs-lookup"><span data-stu-id="b1775-193">**Carrier service:** *Demo carrier service*</span></span>
    - <span data-ttu-id="b1775-194">**Vedaja kliendikonto number:** vedaja kliendikonto number, mida kasutatakse saadetise vedaja seose kinnitamiseks ja autentimiseks.</span><span class="sxs-lookup"><span data-stu-id="b1775-194">**Carrier customer account number:** The carrier customer account number that is used to verify and authenticate the connection to the shipping carrier.</span></span> <span data-ttu-id="b1775-195">Selle väärtuse annab teie vedaja.</span><span class="sxs-lookup"><span data-stu-id="b1775-195">Your carrier will provide this value.</span></span> <span data-ttu-id="b1775-196">Kui kasutate demoteenust, saate sisestada vaikeväärtuse.</span><span class="sxs-lookup"><span data-stu-id="b1775-196">If you're using the demo service, you can enter an arbitrary value.</span></span>
    - <span data-ttu-id="b1775-197">**Tegevuskoht:** *6*</span><span class="sxs-lookup"><span data-stu-id="b1775-197">**Site:** *6*</span></span>
    - <span data-ttu-id="b1775-198">**Ladu:** *62*</span><span class="sxs-lookup"><span data-stu-id="b1775-198">**Warehouse:** *62*</span></span>

    > [!NOTE]
    > <span data-ttu-id="b1775-199">Sageli on väärtus **Vedaja kliendikonto number** ainus väärtus, mis on vajalik ühenduse autentimiseks.</span><span class="sxs-lookup"><span data-stu-id="b1775-199">Often, the **Carrier customer account number** value is the only value that is required to authenticate the connection.</span></span> <span data-ttu-id="b1775-200">Samas kui teie vedaja nõuab siiski täiendavaid autentimisparameetreid, peaks teie organisatsioon seda lehekülge kohandada vastavalt vajadusele lisaväljade lisamiseks.</span><span class="sxs-lookup"><span data-stu-id="b1775-200">However, if your carrier requires additional authentication parameters, your organization should customize this page to add extra fields as appropriate.</span></span>

#### <a name="set-up-a-container-packing-policy"></a><span data-ttu-id="b1775-201">Konteineri pakkimise poliitika häälestamine</span><span class="sxs-lookup"><span data-stu-id="b1775-201">Set up a container packing policy</span></span>

<span data-ttu-id="b1775-202">Konteineri pakkimispoliitika häälestamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="b1775-202">Follow these steps to set up a container packing policy.</span></span>

1. <span data-ttu-id="b1775-203">Kui te pole veel ZPL-printeri definitsiooni häälestanud, kasutage selleks dokumendi marsruudivaliku agendi rakendust.</span><span class="sxs-lookup"><span data-stu-id="b1775-203">If you haven't already set up a ZPL printer definition, use the Document Routing Agent application to set it up.</span></span> <span data-ttu-id="b1775-204">Lisateavet vt [Dokumentide printimise ülevaade](../../fin-ops-core/dev-itpro/analytics/print-documents.md).</span><span class="sxs-lookup"><span data-stu-id="b1775-204">For more information, see [Document printing overview](../../fin-ops-core/dev-itpro/analytics/print-documents.md) and related topics.</span></span>
1. <span data-ttu-id="b1775-205">Avage jaotis **Laohaldus \> Seadistus \> Konteinerid \> Konteineri pakkimise poliitikad**.</span><span class="sxs-lookup"><span data-stu-id="b1775-205">Go to **Warehouse Management \> Setup \> Containers \> Container packing policies**.</span></span>
1. <span data-ttu-id="b1775-206">Valige toimingupaanil suvand **Uus**, et lisada konteineri pakkimise poliitika.</span><span class="sxs-lookup"><span data-stu-id="b1775-206">On the Action Pane, select **New** to add a container packing policy.</span></span>
1. <span data-ttu-id="b1775-207">Määrake uue poliitika päises järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="b1775-207">On the header of the new policy, set the following values:</span></span>

    - <span data-ttu-id="b1775-208">**Konteineri pakkimise poliitika:** *pakkimise demopoliitika*</span><span class="sxs-lookup"><span data-stu-id="b1775-208">**Container packing policy:** *Demo packing policy*</span></span>
    - <span data-ttu-id="b1775-209">**Kirjeldus:** poliitika kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="b1775-209">**Description:** A description of the policy</span></span>

1. <span data-ttu-id="b1775-210">Määrake kiirkaardil **Ülevaade** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="b1775-210">On the **Overview** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b1775-211">**Ladu:** *62*</span><span class="sxs-lookup"><span data-stu-id="b1775-211">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="b1775-212">**Lõpliku saadetise vaikeasukoht:** *Baydoor*</span><span class="sxs-lookup"><span data-stu-id="b1775-212">**Default location for final shipment:** *Baydoor*</span></span>
    - <span data-ttu-id="b1775-213">**Massiühik:** *KG*</span><span class="sxs-lookup"><span data-stu-id="b1775-213">**Weight unit:** *KG*</span></span>
    - <span data-ttu-id="b1775-214">**Konteineri sulgemise poliitika:** *Automaatne väljastamine*</span><span class="sxs-lookup"><span data-stu-id="b1775-214">**Container closing policy:** *Automatic release*</span></span>
    - <span data-ttu-id="b1775-215">**Konteineri väljastamise poliitika:** *tee kättesaadavaks saadetise lõppsihtkohas*</span><span class="sxs-lookup"><span data-stu-id="b1775-215">**Container release policy:** *Make available at final shipping location*</span></span>

1. <span data-ttu-id="b1775-216">Kiirkaardil **Konteineri manifest** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="b1775-216">On the **Container manifest** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b1775-217">**Automaatne manifest konteineri sulgemisel:** *jah*</span><span class="sxs-lookup"><span data-stu-id="b1775-217">**Automatic manifest at container close:** *Yes*</span></span>
    - <span data-ttu-id="b1775-218">**Konteineri manifesti nõuded:** *transpordihaldus*</span><span class="sxs-lookup"><span data-stu-id="b1775-218">**Manifest requirements for container:** *Transportation management*</span></span>
    - <span data-ttu-id="b1775-219">**Prindi konteineri sisu:** *ei*</span><span class="sxs-lookup"><span data-stu-id="b1775-219">**Print container contents:** *No*</span></span>

1. <span data-ttu-id="b1775-220">Kiirkaardil **Konteineri sildi printimine** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="b1775-220">On the **Carrier label printing** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b1775-221">**Prindi konteineri saadetise silt:** *alati*</span><span class="sxs-lookup"><span data-stu-id="b1775-221">**Print container shipping label:** *Always*</span></span>
    - <span data-ttu-id="b1775-222">**Printeri nimi:** ZPL-printeri nimi, mis prindib saadetise sildid</span><span class="sxs-lookup"><span data-stu-id="b1775-222">**Printer name:** The name of the ZPL printer that should print shipping labels</span></span>

#### <a name="set-up-a-packing-profile"></a><span data-ttu-id="b1775-223">Pakkimisprofiili häälestamine</span><span class="sxs-lookup"><span data-stu-id="b1775-223">Set up a packing profile</span></span>

<span data-ttu-id="b1775-224">Pakkimisprofiili häälestamiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="b1775-224">Follow these steps to set up a packing profile.</span></span>

1. <span data-ttu-id="b1775-225">Avage jaotis **Laohaldus \> Seadistus \> Pakkimine \> Pakkimisprofiilid**.</span><span class="sxs-lookup"><span data-stu-id="b1775-225">Go to **Warehouse Management \> Setup \> Packing \> Packing profiles**.</span></span>
1. <span data-ttu-id="b1775-226">Valige toimingupaanil suvand **Uus**, et lisada ruudustikku pakkimisprofiil.</span><span class="sxs-lookup"><span data-stu-id="b1775-226">On the Action Pane, select **New** to add a packing profile to the grid.</span></span>
1. <span data-ttu-id="b1775-227">Määrake uue profiili jaoks järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="b1775-227">Set the following values for the new profile:</span></span>

    - <span data-ttu-id="b1775-228">**Pakkimisprofiili ID:** *demo pakkimisprofiil*</span><span class="sxs-lookup"><span data-stu-id="b1775-228">**Packing profile ID:** *Demo packing profile*</span></span>
    - <span data-ttu-id="b1775-229">**Kirjeldus:** profiili kirjeldus.</span><span class="sxs-lookup"><span data-stu-id="b1775-229">**Description:** A description of the profile</span></span>
    - <span data-ttu-id="b1775-230">**Konteineri pakkimise poliitika:** *pakkimise demopoliitika*</span><span class="sxs-lookup"><span data-stu-id="b1775-230">**Container packing policy:** *Demo packing policy*</span></span>
    - <span data-ttu-id="b1775-231">**Konteineri ID-režiim:** *Automaatne*</span><span class="sxs-lookup"><span data-stu-id="b1775-231">**Container ID mode:** *Auto*</span></span>
    - <span data-ttu-id="b1775-232">**Konteineri tüüp:** *SmallBox*</span><span class="sxs-lookup"><span data-stu-id="b1775-232">**Container type:** *SmallBox*</span></span>

#### <a name="set-up-a-customer-to-use-the-sps-carrier"></a><span data-ttu-id="b1775-233">SPS-i vedaja kasutamiseks kliendi häälestamine</span><span class="sxs-lookup"><span data-stu-id="b1775-233">Set up a customer to use the SPS carrier</span></span>

<span data-ttu-id="b1775-234">Järgige neid samme kliendi häälestamiseks, nii et see saaks kasutada teie loodud vedajat.</span><span class="sxs-lookup"><span data-stu-id="b1775-234">Follow these steps to set up a customer so that it can use the carrier that you created.</span></span>

1. <span data-ttu-id="b1775-235">Avage **Müügireskontro \> Kliendid \> Kõik kliendid**.</span><span class="sxs-lookup"><span data-stu-id="b1775-235">Go to **Accounts receivable \> customers \> All customers**.</span></span>
1. <span data-ttu-id="b1775-236">Otsige ja valige ruudustikust klient *US-027.*</span><span class="sxs-lookup"><span data-stu-id="b1775-236">In the grid, find and select customer *US-027*.</span></span>
1. <span data-ttu-id="b1775-237">Valige toimingupaani vahekaardil **Üldine** grupis **Häälesta** suvand **Vedaja kliendikontod**.</span><span class="sxs-lookup"><span data-stu-id="b1775-237">On the Action Pane, on the **General** tab, in the **Set up** group, select **Carrier customer accounts**.</span></span>
1. <span data-ttu-id="b1775-238">Valige tegevuspaanil lehel **Vedaja kliendi kontod** suvand **Uus**, et lisada konto ruudustikku.</span><span class="sxs-lookup"><span data-stu-id="b1775-238">On the **Carrier customer accounts** page, on the Action Pane, select **New** to add an account to the grid.</span></span>
1. <span data-ttu-id="b1775-239">Määrake uue konto jaoks järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="b1775-239">Set the following values for the new account:</span></span>

    - <span data-ttu-id="b1775-240">**Saadetise vedaja:** *demo vedaja*</span><span class="sxs-lookup"><span data-stu-id="b1775-240">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="b1775-241">**Vedaja kliendikonto number:** *12345*(väärtus ei ole selle stsenaariumi puhul oluline, kuid sellele viidatakse järgmises jaotises.)</span><span class="sxs-lookup"><span data-stu-id="b1775-241">**Carrier customer account number:** *12345* (The value isn't important for this scenario, but it will be referred to in the next section.)</span></span>

### <a name="go-through-the-example-scenario"></a><span data-ttu-id="b1775-242">Läbige näidisstsenaarium</span><span class="sxs-lookup"><span data-stu-id="b1775-242">Go through the example scenario</span></span>

<span data-ttu-id="b1775-243">Pärast kõigi näidisandmete seadistamist eelmises jaotises kirjeldatud viisil olete valmis läbima näidisstsenaariumi.</span><span class="sxs-lookup"><span data-stu-id="b1775-243">After you've set up all the sample data as described in the previous section, you're ready to go through the example scenario.</span></span>

#### <a name="create-a-sales-order-and-process-the-work"></a><span data-ttu-id="b1775-244">Müügitellimuse loomine ja töö töötlemine</span><span class="sxs-lookup"><span data-stu-id="b1775-244">Create a sales order and process the work</span></span>

<span data-ttu-id="b1775-245">Müügitellimuse loomiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="b1775-245">Follow these steps to create a sales order.</span></span>

1. <span data-ttu-id="b1775-246">Avage **Müük ja turundus \> Müügitellimused \> Kõik müügitellimused**.</span><span class="sxs-lookup"><span data-stu-id="b1775-246">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="b1775-247">Müügitellimuse loomiseks valige **Uus**.</span><span class="sxs-lookup"><span data-stu-id="b1775-247">Select **New** to create a sales order.</span></span>
1. <span data-ttu-id="b1775-248">Määrake dialoogiboksi **Müügitellimuse loomine** väljal **Kliendi konto** suvandiks *US-027*.</span><span class="sxs-lookup"><span data-stu-id="b1775-248">In the **Create sales order** dialog box, set the **Customer account** field to *US-027*.</span></span>
1. <span data-ttu-id="b1775-249">Valige müügitellimuse loomiseks ja dialoogiboksi sulgemiseks **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1775-249">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="b1775-250">Avatakse uus müügitellimus.</span><span class="sxs-lookup"><span data-stu-id="b1775-250">The new sales order is opened.</span></span> <span data-ttu-id="b1775-251">Seadke kiirkaardil **Müügitellimuse päis** väli **Vedaja kliendikonto number** väärtus, mille sellele kliendile varem valisite (*12345*).</span><span class="sxs-lookup"><span data-stu-id="b1775-251">On the **Sales order header** FastTab, set the **Carrier customer account number** field to the value that you selected for this customer earlier (*12345*).</span></span>
1. <span data-ttu-id="b1775-252">Lisage jaotises **Müügitellimuse read** müügirida ja seadke selle jaoks järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="b1775-252">In the **Sales order lines** section, add a sales line, and set the following values for it:</span></span>

    - <span data-ttu-id="b1775-253">**Kauba kood:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="b1775-253">**Item number:** *A0002*</span></span>
    - <span data-ttu-id="b1775-254">**Kogus:** *1*</span><span class="sxs-lookup"><span data-stu-id="b1775-254">**Quantity:** *1*</span></span>
    - <span data-ttu-id="b1775-255">**Tegevuskoht:** *6*</span><span class="sxs-lookup"><span data-stu-id="b1775-255">**Site:** *6*</span></span>
    - <span data-ttu-id="b1775-256">**Ladu:** *62*</span><span class="sxs-lookup"><span data-stu-id="b1775-256">**Warehouse:** *62*</span></span>

1. <span data-ttu-id="b1775-257">Lülituge vaatele **Päis**.</span><span class="sxs-lookup"><span data-stu-id="b1775-257">Switch to the **Header** view.</span></span>
1. <span data-ttu-id="b1775-258">Määrake kiirkaardil **Kohaletoimetamine** järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="b1775-258">On the **Delivery** FastTab, set the following values:</span></span>

    - <span data-ttu-id="b1775-259">**Saadetise vedaja:** *demo vedaja*</span><span class="sxs-lookup"><span data-stu-id="b1775-259">**Shipping carrier:** *Demo Carrier*</span></span>
    - <span data-ttu-id="b1775-260">**Vedaja teenus:** *demo vedamisteenus*</span><span class="sxs-lookup"><span data-stu-id="b1775-260">**Carrier service:** *Demo carrier service*</span></span>

1. <span data-ttu-id="b1775-261">Minge tagasi vaatesse **Read**.</span><span class="sxs-lookup"><span data-stu-id="b1775-261">Switch back to the **Lines** view.</span></span> <span data-ttu-id="b1775-262">Kui teil palutakse uuendada müügiridade tarneviisi, valige **Jah**.</span><span class="sxs-lookup"><span data-stu-id="b1775-262">If you're prompted to update the mode of delivery for the sales lines, select **Yes**.</span></span>
1. <span data-ttu-id="b1775-263">Valige jaotises **Müügitellimuse read** varem seadistatud tellimuse rida ja seejärel valige **Varud \> Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="b1775-263">In the **Sales order lines** section, select the order line that you set up earlier, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="b1775-264">Valige lehel **Reserveerimine** suvand **Reserveeri saatepartii**, et reserveerida laos kogu valitud rea kogus.</span><span class="sxs-lookup"><span data-stu-id="b1775-264">On the **Reservation** page, select **Reserve lot** to reserve the selected line's full quantity in the warehouse.</span></span>
1. <span data-ttu-id="b1775-265">Müügitellimuse juurde naasmiseks sulgege leht **Reserveerimine**.</span><span class="sxs-lookup"><span data-stu-id="b1775-265">Close the **Reservation** page to return to the sales order.</span></span>
1. <span data-ttu-id="b1775-266">Valige toimingupaani vahekaardil **Ladu** suvand **Vabasta lattu**.</span><span class="sxs-lookup"><span data-stu-id="b1775-266">On the Action Pane, on the **Warehouse** tab, select **Release to warehouse**.</span></span>

    <span data-ttu-id="b1775-267">Töö on loodud kaupade teisaldamiseks komplekteerimise asukohast pakkejaama.</span><span class="sxs-lookup"><span data-stu-id="b1775-267">Work is created to move items from the picking location to the packing station.</span></span>

1. <span data-ttu-id="b1775-268">Jaotises **Müügitellimuse read** valige **Ladu \> Saadetise üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="b1775-268">In the **Sales order lines** section, select **Warehouse \> Shipment details**.</span></span>
1. <span data-ttu-id="b1775-269">Märkige ües saadetise ID lehel **Saadetise üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="b1775-269">On the **Shipment details** page, make a note of the shipment ID.</span></span> <span data-ttu-id="b1775-270">Vajate seda, kui pakite saadetist pakkimisjaamas.</span><span class="sxs-lookup"><span data-stu-id="b1775-270">You will need it when you pack the pack the shipment at the packing station.</span></span>
1. <span data-ttu-id="b1775-271">Müügitellimuse juurde naasmiseks sulgege leht **Saadetise üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="b1775-271">Close the **Shipment details** page to return to the sales order.</span></span>
1. <span data-ttu-id="b1775-272">Märkige müügitellimuse number üles ja avage **Laohaldus \> Töö \> Kogu töö**.</span><span class="sxs-lookup"><span data-stu-id="b1775-272">Make a note of the sales order number, and then go to **Warehouse management \> Work \> All work**.</span></span>
1. <span data-ttu-id="b1775-273">Kasutage müügitellimuse numbrit tellimuse jaoks loodud töö otsimiseks ja valimiseks.</span><span class="sxs-lookup"><span data-stu-id="b1775-273">Use the sales order number to find and select the work that was created for the order.</span></span>
1. <span data-ttu-id="b1775-274">Toiminguriba vahekaardil **Töö** valige suvand **Lõpeta töö**.</span><span class="sxs-lookup"><span data-stu-id="b1775-274">On the Action Pane, on the **Work** tab, select **Complete work**.</span></span>
1. <span data-ttu-id="b1775-275">Valige lehel **Lõpeta töö** väljal **Kasutaja ID** kasutaja ID.</span><span class="sxs-lookup"><span data-stu-id="b1775-275">On the **Work completion** page, in the **User ID** field, select a user ID.</span></span> <span data-ttu-id="b1775-276">Seejärel valige toimingupaanil suvand **Kinnita töö**.</span><span class="sxs-lookup"><span data-stu-id="b1775-276">Then, on the Action Pane, select **Validate work**.</span></span>
1. <span data-ttu-id="b1775-277">Kui töö läbib valideerimise, valige toiminguriba vahekaardil suvand **Lõpeta töö**.</span><span class="sxs-lookup"><span data-stu-id="b1775-277">If the work passes validation, select **Complete work** on the Action Pane.</span></span>

    <span data-ttu-id="b1775-278">Töö on märgitud lõpetatuks, et simuleerida kaupade liikumist pakkejaama.</span><span class="sxs-lookup"><span data-stu-id="b1775-278">The work is marked as completed to simulate the movement of items to the packing station.</span></span>

#### <a name="pack-the-shipment"></a><span data-ttu-id="b1775-279">Saadetise pakkimine</span><span class="sxs-lookup"><span data-stu-id="b1775-279">Pack the shipment</span></span>

<span data-ttu-id="b1775-280">Saadetise pakkimiseks tehke järgmist.</span><span class="sxs-lookup"><span data-stu-id="b1775-280">Follow these steps to pack the shipment.</span></span>

1. <span data-ttu-id="b1775-281">Avage **Laohaldus \> Seadistamine \> Töötaja** ja veenduge, et teie kasutajakonto on seostatud laohalduse töötaja kontoga.</span><span class="sxs-lookup"><span data-stu-id="b1775-281">Go to **Warehouse management \> Setup \> Worker**, and make sure that your user account is associated with a worker account for warehouse management.</span></span>
1. <span data-ttu-id="b1775-282">Avage jaotis **Laohaldus \> Komplekteerimine ja konteinerisse paigutamine \> Pakkimine**.</span><span class="sxs-lookup"><span data-stu-id="b1775-282">Go to **Warehouse management \> Picking and containerization \> Pack**.</span></span>
1. <span data-ttu-id="b1775-283">Dialoogiboksis **Pakkimisjaama valimine** määrake järgmised väärtused.</span><span class="sxs-lookup"><span data-stu-id="b1775-283">In the **Select packing station** dialog box, set the following values:</span></span>

    - <span data-ttu-id="b1775-284">**Tegevuskoht:** *6*</span><span class="sxs-lookup"><span data-stu-id="b1775-284">**Site:** *6*</span></span>
    - <span data-ttu-id="b1775-285">**Ladu:** *62*</span><span class="sxs-lookup"><span data-stu-id="b1775-285">**Warehouse:** *62*</span></span>
    - <span data-ttu-id="b1775-286">**Asukoht:** *Pakkimine*</span><span class="sxs-lookup"><span data-stu-id="b1775-286">**Location:** *Pack*</span></span>
    - <span data-ttu-id="b1775-287">**Pakkimisprofiili ID:** *demo pakkimisprofiil*</span><span class="sxs-lookup"><span data-stu-id="b1775-287">**Packing profile ID:** *Demo packing profile*</span></span>

1. <span data-ttu-id="b1775-288">Valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1775-288">Select **OK**.</span></span>
1. <span data-ttu-id="b1775-289">Kuvatakse leht **Pakkimine**.</span><span class="sxs-lookup"><span data-stu-id="b1775-289">The **Pack** page appears.</span></span> <span data-ttu-id="b1775-290">Tootmisstsenaariumis skannib töötaja litsentsiplaadi või saadetise ID.</span><span class="sxs-lookup"><span data-stu-id="b1775-290">In a production scenario, a worker will scan a license plate or shipment ID.</span></span> <span data-ttu-id="b1775-291">Kuid selle stsenaariumi puhul avage leht **Kõik saadetised** ja otsige saadetise numbrit, mille äsja lõite.</span><span class="sxs-lookup"><span data-stu-id="b1775-291">However, for this scenario, open the **All shipments** page, and look up the shipment number for the shipment that you just created.</span></span> <span data-ttu-id="b1775-292">Seejärel sisestage see väärtus väljale **Numbrimärk või saadetis** lehel **Pakkimine**.</span><span class="sxs-lookup"><span data-stu-id="b1775-292">Then enter this value in the **License plate or shipment** field on the **Pack** page.</span></span> <span data-ttu-id="b1775-293">Teise võimalusena sisestage saadetise ID, mille olete varem üles märkinud.</span><span class="sxs-lookup"><span data-stu-id="b1775-293">Alternatively, enter the shipment ID that you made a note of earlier.</span></span>
1. <span data-ttu-id="b1775-294">Valige toimingupaanil nupp **Uus konteiner**.</span><span class="sxs-lookup"><span data-stu-id="b1775-294">On the Action Pane, select **New container**.</span></span>
1. <span data-ttu-id="b1775-295">Kuvatavas dialoogiboksis kuvatakse uue konteineri üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="b1775-295">The dialog box that appears shows details about the new container.</span></span> <span data-ttu-id="b1775-296">Jätke vaikeväärtused ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1775-296">Leave the default values, and then select **OK**.</span></span>
1. <span data-ttu-id="b1775-297">Kauba pakkimiseks valige lehel **Pakkimine** kiirkaardil **Kauba pakkimine** väljal **Identifikaator** väärtus *A0002*.</span><span class="sxs-lookup"><span data-stu-id="b1775-297">On the **Pack** page, on the **Item packing** FastTab, in the **Identifier** field, select *A0002* to pack that item.</span></span> <span data-ttu-id="b1775-298">Kaup lisatakse konteinerisse.</span><span class="sxs-lookup"><span data-stu-id="b1775-298">The item is added to the container.</span></span>
1. <span data-ttu-id="b1775-299">Valige toimingupaanil suvand **Konteinerid saatmiseks**.</span><span class="sxs-lookup"><span data-stu-id="b1775-299">On the Action Pane, select **Containers for shipment**.</span></span>

    <span data-ttu-id="b1775-300">Ilmuval lehel **Konteinerid saatmiseks** on rida konteineri jaoks. mille lõite.</span><span class="sxs-lookup"><span data-stu-id="b1775-300">The **Containers for shipment** page that appears has a row for the container that you just created.</span></span> <span data-ttu-id="b1775-301">Sellel real on väli **Konteineri manifesti ID** praegu tühi, sest te pole veel saadetise silti ega jälgimisnumbrit vedajalt kätte saanud.</span><span class="sxs-lookup"><span data-stu-id="b1775-301">However, the **Container manifest ID** field in that row is currently blank, because you haven't yet received the shipping label and tracking number from the carrier.</span></span>

1. <span data-ttu-id="b1775-302">Valige toimingupaanil nupp **Sule konteiner**.</span><span class="sxs-lookup"><span data-stu-id="b1775-302">On the Action Pane, select **Close container**.</span></span>
1. <span data-ttu-id="b1775-303">Dialoogiboksis **Konteineri sulgemine** määrake välja **Brutokaal** väärtuseks *1 kg* ja seejärel valige **OK**.</span><span class="sxs-lookup"><span data-stu-id="b1775-303">In the **Close container** dialog box, set the **Gross weight** field to *1 kg*, and then select **OK**.</span></span>

    <span data-ttu-id="b1775-304">Saadetise silt tuleb nüüd printida varem valitud ZPL-printeriga.</span><span class="sxs-lookup"><span data-stu-id="b1775-304">The shipping label should now be printed on the ZPL printer that you selected earlier.</span></span> <span data-ttu-id="b1775-305">See peals sarnanema järgmise näitega.</span><span class="sxs-lookup"><span data-stu-id="b1775-305">It should resemble the following example.</span></span>

    <span data-ttu-id="b1775-306">![Saadetise sildi näide](media/sps-label-example.png "Saadetise sildi näide")</span><span class="sxs-lookup"><span data-stu-id="b1775-306">![Example shipping label](media/sps-label-example.png "Example shipping label")</span></span>

1. <span data-ttu-id="b1775-307">Pange tähele, et **Konteineri manifesti ID** ja **Veose koguväärtus** on vedajalt saadud.</span><span class="sxs-lookup"><span data-stu-id="b1775-307">Notice that the **Container manifest ID** and **Total freight** values have been added as received from the carrier.</span></span>
