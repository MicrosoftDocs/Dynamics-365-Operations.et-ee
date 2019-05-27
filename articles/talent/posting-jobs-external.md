---
title: Töökuulutuste sisestamine Attractist välistele karjäärisaitidele
description: Selles teemas selgitatakse, kuidas kasutada rakendust Dynamics 365 for Talent - Attract töökuulutuste sisestamiseks välistele värbamissaitidele
author: pganapmsft
manager: AnnBe
ms.date: 03/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-03-19
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: eca599ad189edae29ef2de496196b08799a5e745
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517811"
---
# <a name="post-jobs-to-external-career-sites-from-attract"></a><span data-ttu-id="2539d-103">Töökuulutuste sisestamine Attractist välistele karjäärisaitidele</span><span class="sxs-lookup"><span data-stu-id="2539d-103">Post jobs to external career sites from Attract</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2539d-104">Soovite, et teave teie vabadest ametikohtadest jõuaks võimalikult paljude kvalifitseeritud kandidaatideni.</span><span class="sxs-lookup"><span data-stu-id="2539d-104">You want to get your open positions in front of as many qualified candidates as possible.</span></span> <span data-ttu-id="2539d-105">Värbamissaidid nagu Broadbean aitavad teil seda eesmärki saavutada.</span><span class="sxs-lookup"><span data-stu-id="2539d-105">Recruiting sites such as Broadbean help you accomplish this goal.</span></span> <span data-ttu-id="2539d-106">Microsoft Dynamics 365 Talent: Attract võimaldab teil töökuulutusi Broadbeani sisestada ja Microsoft teeb selles vallas pidevalt uusi pakkumisi.</span><span class="sxs-lookup"><span data-stu-id="2539d-106">Microsoft Dynamics 365 Talent: Attract now lets you post jobs to Broadbean, and Microsoft is constantly providing new offerings in this area.</span></span>

## <a name="post-jobs-to-broadbean"></a><span data-ttu-id="2539d-107">Töökuulutuste sisestamine Broadbeani</span><span class="sxs-lookup"><span data-stu-id="2539d-107">Post jobs to Broadbean</span></span>

<span data-ttu-id="2539d-108">Enne töökuulutuste sisestamist Broadbeani peate konfigureerima Broadbeani integreerimise.</span><span class="sxs-lookup"><span data-stu-id="2539d-108">Before you can post jobs to Broadbean, you must configure the Broadbean integration.</span></span>

> [!NOTE]
> - <span data-ttu-id="2539d-109">Töökuulutuste sisestamiseks välistele veebisaitidele peab teil olema [tervikliku värbamise lisandmoodul](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span><span class="sxs-lookup"><span data-stu-id="2539d-109">To post jobs to external sites, you must have the [Comprehensive hiring add-on](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>
> - <span data-ttu-id="2539d-110">See funktsioon on praegu eelvaateversioonis.</span><span class="sxs-lookup"><span data-stu-id="2539d-110">This feature is currently in preview.</span></span> <span data-ttu-id="2539d-111">Kui soovite seda proovida, peate [selle sisse lülitama Attracti administraatori sätetega](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="2539d-111">If you want to try it, you must [turn it on in the Attract admin settings](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

### <a name="configure-broadbean-integration"></a><span data-ttu-id="2539d-112">Broadbeani integreerimise konfigureerimine</span><span class="sxs-lookup"><span data-stu-id="2539d-112">Configure Broadbean integration</span></span>

1. <span data-ttu-id="2539d-113">Attracti administraatorina sisse logimine.</span><span class="sxs-lookup"><span data-stu-id="2539d-113">Sign in to Attract as an admin.</span></span>
2. <span data-ttu-id="2539d-114">Valige lehe paremast ülanurgast nupp **Sätted** (hammasrattasümbol) ja seejärel valige **Administreerimiskeskus**.</span><span class="sxs-lookup"><span data-stu-id="2539d-114">Select the **Settings** button (the gear symbol) in the upper-right corner of the page, and then select **Admin center**.</span></span>
3. <span data-ttu-id="2539d-115">Lülitage integratsioon sisse vahekaardi **Tööportaalide sätted** jaotises **Luba Broadbeani integreerimine**.</span><span class="sxs-lookup"><span data-stu-id="2539d-115">On the **Job board settings** tab, in the **Enable Broadbean integration** section, turn on the integration.</span></span>
4. <span data-ttu-id="2539d-116">Looge Broadbeaniga ühendus ja sisestage oma andmed lahtritesse **Kasutajanimi, Kliendi ID, Krüptimise luba**.</span><span class="sxs-lookup"><span data-stu-id="2539d-116">Contact Broadbean, and enter your information in **Username, Client ID, Encryption Token**.</span></span>

> [!WARNING]
> <span data-ttu-id="2539d-117">Teie Broadbeani mandaadid on tundlikud ja konfidentsiaalsed.</span><span class="sxs-lookup"><span data-stu-id="2539d-117">Your Broadbean credentials are sensitive and confidential.</span></span> <span data-ttu-id="2539d-118">Seega talletage ja jagage neid vastutustundlikult.</span><span class="sxs-lookup"><span data-stu-id="2539d-118">Therefore, store and share them responsibly.</span></span> <span data-ttu-id="2539d-119">Mandaadid on nähtavad kõigile, kellel on Attractis administraatori roll.</span><span class="sxs-lookup"><span data-stu-id="2539d-119">Anyone who has an Administrator role in Attract can view these credentials.</span></span>

> [!NOTE]
> <span data-ttu-id="2539d-120">Microsoft ja Attract ei ole nende väärtuste loomise ning haldamisega seotud.</span><span class="sxs-lookup"><span data-stu-id="2539d-120">Microsoft and Attract aren't involved in creating and maintaining these values.</span></span> <span data-ttu-id="2539d-121">Mandaatide Attractis ajakohasena hoidmine ja nendega seotud võimalike probleemide lahendamine Broadbeanis on teie vastutus.</span><span class="sxs-lookup"><span data-stu-id="2539d-121">It's your responsibility to keep them up to date in Attract and to work with Broadbean to resolve any issues that involve your credentials.</span></span>

### <a name="post-a-job-to-broadbean"></a><span data-ttu-id="2539d-122">Töökuulutuse sisestamine Broadbeani</span><span class="sxs-lookup"><span data-stu-id="2539d-122">Post a job to Broadbean</span></span>

<span data-ttu-id="2539d-123">Kui Broadbean on sisse lülitatud, saavad värbajad ja administraatorid sellesse töökuulutuse sisestada.</span><span class="sxs-lookup"><span data-stu-id="2539d-123">After Broadbean has been turned on, recruiters and admins can post a job to it.</span></span> <span data-ttu-id="2539d-124">Teil peab töökuulutuse jaoks olema kandideerimise URL.</span><span class="sxs-lookup"><span data-stu-id="2539d-124">You must have an apply URL for the job.</span></span>

1. <span data-ttu-id="2539d-125">Avage Attractis töökuulutus, mida soovite Broadbeani sisestada.</span><span class="sxs-lookup"><span data-stu-id="2539d-125">In Attract, open the job that you want to post to Broadbean.</span></span>
2. <span data-ttu-id="2539d-126">Valige jaotises **Sisestamised** Broadbeanile vastav nupp **Sisesta kohe**.</span><span class="sxs-lookup"><span data-stu-id="2539d-126">In the **Postings** section, select the **Post Now** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="2539d-127">Järgige Broadbeani aknas juhiseid.</span><span class="sxs-lookup"><span data-stu-id="2539d-127">Follow the instructions in the Broadbean window.</span></span>

<span data-ttu-id="2539d-128">Attract jagab Broadbeaniga järgmist teavet.</span><span class="sxs-lookup"><span data-stu-id="2539d-128">Attract passes the following information to Broadbean:</span></span>

- <span data-ttu-id="2539d-129">Taotluse ID</span><span class="sxs-lookup"><span data-stu-id="2539d-129">Request ID</span></span>
- <span data-ttu-id="2539d-130">Ametinimetus</span><span class="sxs-lookup"><span data-stu-id="2539d-130">Job title</span></span>
- <span data-ttu-id="2539d-131">Töö kirjeldus</span><span class="sxs-lookup"><span data-stu-id="2539d-131">Job description</span></span>
- <span data-ttu-id="2539d-132">Töö asukoht</span><span class="sxs-lookup"><span data-stu-id="2539d-132">Job location</span></span>
- <span data-ttu-id="2539d-133">Kandideerimise URL</span><span class="sxs-lookup"><span data-stu-id="2539d-133">Apply URL</span></span>
- <span data-ttu-id="2539d-134">Värbamisteave</span><span class="sxs-lookup"><span data-stu-id="2539d-134">Recruiter information</span></span>

<span data-ttu-id="2539d-135">Kui Broadbean on sisestamise edukalt lõpetanud, kuvatakse Attractis töökuulutuse jaotises **Sisestamised** Broadbeani olekut kui **Sisestatud**.</span><span class="sxs-lookup"><span data-stu-id="2539d-135">After Broadbean successfully completes the posting, the **Postings** section of the job in Attract shows the Broadbean status as **Posted**.</span></span>

> [!NOTE]
> - <span data-ttu-id="2539d-136">Broadbeanis on nõutav väli **Tegevusvaldkond**.</span><span class="sxs-lookup"><span data-stu-id="2539d-136">Broadbean requires the **Industry** field.</span></span> <span data-ttu-id="2539d-137">Praegu on selle välja vaikimisi säte **IT**.</span><span class="sxs-lookup"><span data-stu-id="2539d-137">Currently, this field is set to **IT** by default.</span></span> <span data-ttu-id="2539d-138">Broadbeani töökuulutuse sisestamise aknas saate väärtuse siiski muuta õigeks tegevusvaldkonnaks.</span><span class="sxs-lookup"><span data-stu-id="2539d-138">However, you can change the value to the correct industry in the window for Broadbean job posting.</span></span>
> - <span data-ttu-id="2539d-139">Broadbeanil läheb aega teie töökuulutuse sisestamiseks kõikidesse valitud tööportaalidesse.</span><span class="sxs-lookup"><span data-stu-id="2539d-139">It takes some time for Broadbean to finish posting your job to all the job boards that you selected.</span></span> <span data-ttu-id="2539d-140">Seetõttu võib kuluda veidi aega enne kui Attract töökuulutuse olekut värskendab.</span><span class="sxs-lookup"><span data-stu-id="2539d-140">Therefore, there might be a slight delay before Attract provides a status update for the job.</span></span>

### <a name="view-a-broadbean-job-posting"></a><span data-ttu-id="2539d-141">Broadbeani töökuulutuse sisestuse kuvamine</span><span class="sxs-lookup"><span data-stu-id="2539d-141">View a Broadbean job posting</span></span>

<span data-ttu-id="2539d-142">Pärast töökuulutuse Broadbeani sisestamist saate seda kuvada Attracti kaudu.</span><span class="sxs-lookup"><span data-stu-id="2539d-142">After you post a job to Broadbean, you can view it from Attract.</span></span>

1. <span data-ttu-id="2539d-143">Avage Attractis töökuulutus, mida soovite Broadbeanis kuvada.</span><span class="sxs-lookup"><span data-stu-id="2539d-143">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="2539d-144">Valige jaotises **Sisestamised** Broadbeanile vastav kolmikpunkti nupp (**...**) ja seejärel valige **Kuva**.</span><span class="sxs-lookup"><span data-stu-id="2539d-144">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>

<span data-ttu-id="2539d-145">Broadbeani töökuulutuse sisestus kuvatakse uues aknas.</span><span class="sxs-lookup"><span data-stu-id="2539d-145">The Broadbean job posting appears in a new window.</span></span>

### <a name="update-a-broadbean-job-posting"></a><span data-ttu-id="2539d-146">Broadbeani töökuulutuse sisestuse värskendamine</span><span class="sxs-lookup"><span data-stu-id="2539d-146">Update a Broadbean job posting</span></span>

<span data-ttu-id="2539d-147">Broadbeani töökuulutuse sisestust saate värskendada kahel viisil.</span><span class="sxs-lookup"><span data-stu-id="2539d-147">You can update a Broadbean job posting in two ways.</span></span>

1. <span data-ttu-id="2539d-148">Avage Attractis töökuulutus, mida soovite Broadbeanis värskendada.</span><span class="sxs-lookup"><span data-stu-id="2539d-148">In Attract, open the job that you want to update.</span></span>
2. <span data-ttu-id="2539d-149">Valige jaotises **Sisestamised** Broadbeanile vastav nupp **Värskenda töökuulutust**.</span><span class="sxs-lookup"><span data-stu-id="2539d-149">In the **Postings** section, select the **Update Post** button that corresponds to Broadbean.</span></span>
3. <span data-ttu-id="2539d-150">Muutke töökuulutust Broadbeani aknas.</span><span class="sxs-lookup"><span data-stu-id="2539d-150">Edit the posting in the Broadbean window.</span></span>

<span data-ttu-id="2539d-151">või</span><span class="sxs-lookup"><span data-stu-id="2539d-151">–or–</span></span>

1. <span data-ttu-id="2539d-152">Avage Attractis töökuulutus, mida soovite Broadbeanis kuvada.</span><span class="sxs-lookup"><span data-stu-id="2539d-152">In Attract, open the job that you want to view on Broadbean.</span></span>
2. <span data-ttu-id="2539d-153">Valige jaotises **Sisestamised** Broadbeanile vastav kolmikpunkti nupp (**...**) ja seejärel valige **Kuva**.</span><span class="sxs-lookup"><span data-stu-id="2539d-153">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **View**.</span></span>
3. <span data-ttu-id="2539d-154">Muutke Broadbeani aknas töökuulutuse üksikasju ja seejärel sisestage töökuulutus uuesti.</span><span class="sxs-lookup"><span data-stu-id="2539d-154">In the Broadbean window, edit the job details, and then repost the job.</span></span> <span data-ttu-id="2539d-155">Töökuulutuse üksikasjad Attractis ei muutu.</span><span class="sxs-lookup"><span data-stu-id="2539d-155">The job details in Attract aren't changed.</span></span>

### <a name="remove-a-broadbean-job-posting"></a><span data-ttu-id="2539d-156">Broadbeani töökuulutuse sisestuse eemaldamine</span><span class="sxs-lookup"><span data-stu-id="2539d-156">Remove a Broadbean job posting</span></span>

<span data-ttu-id="2539d-157">Töökuulutuse sisestusi saate Broadbeanist vajaduse korral eemaldada.</span><span class="sxs-lookup"><span data-stu-id="2539d-157">You can remove a job posting from Broadbean as you require.</span></span>

1. <span data-ttu-id="2539d-158">Avage Attractis töökuulutus, mida soovite eemaldada.</span><span class="sxs-lookup"><span data-stu-id="2539d-158">In Attract, open the job that you want to remove.</span></span>
2. <span data-ttu-id="2539d-159">Valige jaotises **Sisestamised** Broadbeanile vastav kolmikpunkti nupp (**...**) ja seejärel valige **Eemalda töökuulutus**.</span><span class="sxs-lookup"><span data-stu-id="2539d-159">In the **Postings** section, select the ellipsis button (**...**) that corresponds to Broadbean, and then select **Remove Post**.</span></span>

<span data-ttu-id="2539d-160">Kui Broadbean on töökuulutuse eemaldanud, on Attractis Broadbeani üksusel **Sisesta kohe** nupp.</span><span class="sxs-lookup"><span data-stu-id="2539d-160">After Broadbean removes the job, the Broadbean item in Attract has a **Post Now** button.</span></span> <span data-ttu-id="2539d-161">Selle nupu olemasolu näitab, et töökuulutus on eemaldatud ja seda on võimalik uuesti sisestada.</span><span class="sxs-lookup"><span data-stu-id="2539d-161">The presence of this button indicates that the job has been removed and can be posted again.</span></span>

### <a name="troubleshoot-the-broadbean-integration"></a><span data-ttu-id="2539d-162">Broadbeani integreerimise tõrkeotsing</span><span class="sxs-lookup"><span data-stu-id="2539d-162">Troubleshoot the Broadbean integration</span></span>

<span data-ttu-id="2539d-163">Kui teil on Broadbeani töökuulutuse sisestamisega probleeme, proovige järgmist.</span><span class="sxs-lookup"><span data-stu-id="2539d-163">If you're having trouble posting a job to Broadbean, try these steps.</span></span>

1. <span data-ttu-id="2539d-164">Kontrollige, kas Attracti sisestatud Broadbeani mandaadid on kehtivad ja õiged.</span><span class="sxs-lookup"><span data-stu-id="2539d-164">Verify that the Broadbean credentials that you entered in Attract are valid and correct.</span></span>
2. <span data-ttu-id="2539d-165">Kui mandaadid on kehtivad ja õiged, võtke ühendust [Broadbeani toega](https://www.broadbean.com/resources/support/).</span><span class="sxs-lookup"><span data-stu-id="2539d-165">If the credentials are valid and correct, contact [Broadbean support](https://www.broadbean.com/resources/support/).</span></span>
3. <span data-ttu-id="2539d-166">Kui probleem ei lahene, võtke ühendust [Microsofti toega](./talent-support.md).</span><span class="sxs-lookup"><span data-stu-id="2539d-166">If the issue persists, contact [Microsoft support](./talent-support.md).</span></span>
