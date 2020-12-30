---
title: Andmete eksportimine Attractist ja Onboardist
description: Andmete eksportimine Dynamics 365 Talent - Attractist ja Onboardist.
author: andreabichsel
manager: AnnBe
ms.date: 01/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2020-01-14
ms.dyn365.ops.version: Talent October 2019 update
ms.openlocfilehash: eb97a16c15476c2f34ec581a32a677fa6fee8739
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460869"
---
# <a name="export-data-from-attract-and-onboard"></a><span data-ttu-id="8b388-103">Andmete eksportimine Attractist ja Onboardist</span><span class="sxs-lookup"><span data-stu-id="8b388-103">Export data from Attract and Onboard</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="8b388-104">Nagu välja kuulutatud jaotises [Rakenduste Dynamics 365 Talent: Attract ja Dynamics 365 Talent: Onboard pensionile jäämine](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps), saadame rakendused Dynamics 365 Talent: Attract ja Dynamics 365 Talent: Onboard pensionile 1. veebruaril 2022.</span><span class="sxs-lookup"><span data-stu-id="8b388-104">As announced in [Retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard Apps](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps), we're retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard on February 1, 2022.</span></span> <span data-ttu-id="8b388-105">Et aidata kaasa teie migreerumisele mõnele muule tootele, pakuvad mõlemad rakendused nüüd andmete eksportimise võimalusi.</span><span class="sxs-lookup"><span data-stu-id="8b388-105">To help with your migration to another product, both apps now provide data export capabilities.</span></span>

## <a name="export-data-from-attract"></a><span data-ttu-id="8b388-106">Andmete eksportimine Attractist</span><span class="sxs-lookup"><span data-stu-id="8b388-106">Export data from Attract</span></span>

<span data-ttu-id="8b388-107">Saate oma andmeid eksportida ilma keskkonnale juurdepääsu piiramata.</span><span class="sxs-lookup"><span data-stu-id="8b388-107">You can export your data without restricting access to your environment.</span></span> <span data-ttu-id="8b388-108">Võite soovida seda teha testimise eesmärgil või meie andmestruktuuri mõistmiseks.</span><span class="sxs-lookup"><span data-stu-id="8b388-108">You might want to do this for testing purposes or to understand our data structure.</span></span> <span data-ttu-id="8b388-109">Kui olete valmis migreerima, piirake juurdepääsu oma Attracti keskkonnale, kasutades sellele protseduurile järgnevaid juhiseid.</span><span class="sxs-lookup"><span data-stu-id="8b388-109">When you're ready to migrate, restrict access to your Attract environment using the instructions after this procedure.</span></span> <span data-ttu-id="8b388-110">Eksportige oma andmed kindlasti uuesti.</span><span class="sxs-lookup"><span data-stu-id="8b388-110">Be sure to export your data again.</span></span> 

1. <span data-ttu-id="8b388-111">Avage [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span><span class="sxs-lookup"><span data-stu-id="8b388-111">Go to [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span></span>

2. <span data-ttu-id="8b388-112">Valige jaotises **Andmete eksport** käsk **Taotle andmeid eksportimist**.</span><span class="sxs-lookup"><span data-stu-id="8b388-112">Under **Data export**, select **Request a data export**.</span></span>

   ![[<span data-ttu-id="8b388-113">Attractist andmete ekspordi taotlemine</span><span class="sxs-lookup"><span data-stu-id="8b388-113">Request a data export from Attract</span></span>](./media/attract-onboard-export-data-attract-request.png)](./media/attract-onboard-export-data-attract-request.png)

3. <span data-ttu-id="8b388-114">Kui kuvatakse sõnumit **Teie taotlus on töötluses** valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="8b388-114">When the **Your request is being processed** message box appears, select **OK**.</span></span> <span data-ttu-id="8b388-115">Sõltuvalt ekspordi mahust võib andmete eksport võtta kuni 20 minutit.</span><span class="sxs-lookup"><span data-stu-id="8b388-115">The data export can take up to 20 minutes, depending on the size of your export.</span></span>

4. <span data-ttu-id="8b388-116">Kui eksport jõuab lõpuni, valige selle kõrval nupp **Laadi alla**.</span><span class="sxs-lookup"><span data-stu-id="8b388-116">When your export completes, select the **Download** button next to it.</span></span> 

   >[!NOTE]
   ><span data-ttu-id="8b388-117">Kõik andmete ekspordid on saadaval seitsme päeva jooksul, pärast mida link **Laadi alla** aegub.</span><span class="sxs-lookup"><span data-stu-id="8b388-117">All data exports are available for seven days, at which point the **Download** link expires.</span></span></br>
   
<span data-ttu-id="8b388-118">Alla laaditav fail sisaldab teie Attracti andmetega .zip faili, sealhulgas on järgmised kaustad.</span><span class="sxs-lookup"><span data-stu-id="8b388-118">The download contains a .zip file with your Attract data, including the following folders:</span></span>

| <span data-ttu-id="8b388-119">Kausta nimi</span><span class="sxs-lookup"><span data-stu-id="8b388-119">Folder name</span></span> | <span data-ttu-id="8b388-120">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="8b388-120">Description</span></span> |
| --- | --- |
| <span data-ttu-id="8b388-121">Administraatori sätted</span><span class="sxs-lookup"><span data-stu-id="8b388-121">Admin settings</span></span> | <span data-ttu-id="8b388-122">Attracti halduskeskuse konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="8b388-122">Attract admin center configurations.</span></span> |
| <span data-ttu-id="8b388-123">Kandidaadid</span><span class="sxs-lookup"><span data-stu-id="8b388-123">Candidates</span></span> | <span data-ttu-id="8b388-124">Kõik kandidaadid, kes lisati töödele või talendikaustadesse.</span><span class="sxs-lookup"><span data-stu-id="8b388-124">All candidates that were added to jobs or talent pools.</span></span> |
| <span data-ttu-id="8b388-125">E-kirjade mallid</span><span class="sxs-lookup"><span data-stu-id="8b388-125">Email templates</span></span> | <span data-ttu-id="8b388-126">Kõik keskkonnas konfigureeritud meilimallid.</span><span class="sxs-lookup"><span data-stu-id="8b388-126">All email templates that were configured for the environment.</span></span> |
| <span data-ttu-id="8b388-127">Tööpakkumiste paketi mallid</span><span class="sxs-lookup"><span data-stu-id="8b388-127">Job offer package templates</span></span> | <span data-ttu-id="8b388-128">Kõik loodud tööpakkumise paketi mallid ja nendega seotud konfiguratsioonid.</span><span class="sxs-lookup"><span data-stu-id="8b388-128">All job offer package templates that were created, plus their associated configurations.</span></span> |
| <span data-ttu-id="8b388-129">Tööpakkumise reeglite komplektid</span><span class="sxs-lookup"><span data-stu-id="8b388-129">Job offer rule sets</span></span> |  <span data-ttu-id="8b388-130">Kõik reeglitekomplektide failid, mis laaditi pakkumise haldamiseks üles.</span><span class="sxs-lookup"><span data-stu-id="8b388-130">All rule set files that were uploaded for offer management.</span></span> |
| <span data-ttu-id="8b388-131">Tööpakkumiste mallid</span><span class="sxs-lookup"><span data-stu-id="8b388-131">Job offer templates</span></span> | <span data-ttu-id="8b388-132">Kõik keskkonnas loodud tööpakkumise dokumendi mallid.</span><span class="sxs-lookup"><span data-stu-id="8b388-132">All job offer document templates created for the environment.</span></span> |
| <span data-ttu-id="8b388-133">Vabad töökohad</span><span class="sxs-lookup"><span data-stu-id="8b388-133">Job openings</span></span> | <span data-ttu-id="8b388-134">Kõik loodud tööd.</span><span class="sxs-lookup"><span data-stu-id="8b388-134">All created jobs.</span></span> <span data-ttu-id="8b388-135">Kustutatud töid ei ekspordita.</span><span class="sxs-lookup"><span data-stu-id="8b388-135">Deleted jobs aren't exported.</span></span> <span data-ttu-id="8b388-136">Alamkaustad sisaldavad kandidaatide avaldusi koos kandidaatide avalduste manuste allkaustadega ja pakkumiste pakettidega, kui see on kohaldatav.</span><span class="sxs-lookup"><span data-stu-id="8b388-136">The sub-folders contain candidate applications, with sub-folders for candidate application attachments and offer packages, where applicable.</span></span> |
| <span data-ttu-id="8b388-137">Vaba töökoha mall</span><span class="sxs-lookup"><span data-stu-id="8b388-137">Job opening templates</span></span> | <span data-ttu-id="8b388-138">Keskkonnas konfigureeritud tööprotsessi meilimallid.</span><span class="sxs-lookup"><span data-stu-id="8b388-138">Job process templates that were configured in the environment.</span></span> |
| <span data-ttu-id="8b388-139">Talendikaustad</span><span class="sxs-lookup"><span data-stu-id="8b388-139">Talent pools</span></span> | <span data-ttu-id="8b388-140">Kõik loodud talendikaustad, nende toetajate nimekirjad ja talendikaustade kandidaatide nimekirjad.</span><span class="sxs-lookup"><span data-stu-id="8b388-140">All created talent pools, their contributors lists, and the candidates lists for the talent pools.</span></span> |
| <span data-ttu-id="8b388-141">Töötajad</span><span class="sxs-lookup"><span data-stu-id="8b388-141">Workers</span></span> | <span data-ttu-id="8b388-142">Kõigi töötajate loend, kes on keskkonnas olemas ning nende rollid.</span><span class="sxs-lookup"><span data-stu-id="8b388-142">List of all the workers who are present in the environment, plus their roles.</span></span> |
| <span data-ttu-id="8b388-143">(juurkaust)</span><span class="sxs-lookup"><span data-stu-id="8b388-143">(root folder)</span></span> | <span data-ttu-id="8b388-144">JSON-skeemifaili, mis kirjeldab andmestruktuuri väljasid.</span><span class="sxs-lookup"><span data-stu-id="8b388-144">A JSON schema file that describes the data structure fields.</span></span> |

### <a name="restrict-access-to-attract"></a><span data-ttu-id="8b388-145">Attracti juurdepääsu piiramine</span><span class="sxs-lookup"><span data-stu-id="8b388-145">Restrict access to Attract</span></span>

<span data-ttu-id="8b388-146">Kui olete valmis migreerima, piirake mitte-administraatoritele juurdepääs oma Attracti keskkonnale ja eksportige oma andmed.</span><span class="sxs-lookup"><span data-stu-id="8b388-146">When you're ready to migrate, restrict non-admins from accessing your Attract environment and export your data.</span></span>

>[!IMPORTANT]
><span data-ttu-id="8b388-147">Juurdepääsu piiramine teie Attracti keskkonnale on püsiv ja seda ei saa tagasi võtta.</span><span class="sxs-lookup"><span data-stu-id="8b388-147">Restricting access to your Attract environment is permanent and can't be undone.</span></span> <span data-ttu-id="8b388-148">Kui soovite, et mitte-administraatoritest kasutajad säilitaksid juurdepääsu teie keskkonnale, jätke see samm vahele.</span><span class="sxs-lookup"><span data-stu-id="8b388-148">If you want non-admin users to continue accessing your environment, skip this step.</span></span>

1. <span data-ttu-id="8b388-149">Avage [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span><span class="sxs-lookup"><span data-stu-id="8b388-149">Go to [https://aka.ms/AttractDataExport](https://aka.ms/AttractDataExport).</span></span>

2. <span data-ttu-id="8b388-150">Et piirata mitte-administraatoritele juurdepääsu oma Attracti keskkonnale, valige jaotises **Piira sellele rakendusele juurdepääs** käsk **Piira kohe juurdepääs**.</span><span class="sxs-lookup"><span data-stu-id="8b388-150">To restrict non-admins from accessing your Attract environment, under **Restrict access to this app**, select **Restrict access now**.</span></span> <span data-ttu-id="8b388-151">Juurdepääsu piiramine võtab maha ka kõik sisestatud aktiivsed tööd.</span><span class="sxs-lookup"><span data-stu-id="8b388-151">Restricting access also unposts any active jobs that have been posted.</span></span>

   ![[<span data-ttu-id="8b388-152">Attracti juurdepääsu piiramine mitte-administraatoritele</span><span class="sxs-lookup"><span data-stu-id="8b388-152">Restrict non-admin access to Attract</span></span>](./media/attract-onboard-export-data-attract-restrict-access.png)](./media/attract-onboard-export-data-attract-restrict-access.png)

3. <span data-ttu-id="8b388-153">Kui näete hoiatust **See on püsiv muudatus**, valige **Keela juurdepääs**, et piirata püsivalt mitte-administraatoritele juurdepääs sellele keskkonnale.</span><span class="sxs-lookup"><span data-stu-id="8b388-153">When you see the warning **This is a permanent change**, select **Restrict access** to permanently restrict non-admin users from this environment.</span></span> <span data-ttu-id="8b388-154">Kui te pole valmis seda etappi lõpetama, valige käsk **Tühista**.</span><span class="sxs-lookup"><span data-stu-id="8b388-154">If you're not ready to complete this step, select **Cancel**.</span></span>

   ![[<span data-ttu-id="8b388-155">Hoiatus, et juurdepääsu piiramine on püsiv muudatus</span><span class="sxs-lookup"><span data-stu-id="8b388-155">Warning that restricting access is a permanent change</span></span>](./media/attract-onboard-export-data-attract-warning.png)](./media/attract-onboard-export-data-attract-warning.png)

   >[!NOTE]
   ><span data-ttu-id="8b388-156">Administraatorid pääsevad jätkuvalt juurde andmetele ekspordile ja isikuaruande leheküljele ka pärast Attracti keskkonna juurdepääsu piiramist.</span><span class="sxs-lookup"><span data-stu-id="8b388-156">Admins can continue to access the data export and person report pages after you restrict access to the Attract environment.</span></span>

## <a name="export-data-from-onboard"></a><span data-ttu-id="8b388-157">Andmete eksportimine Onboardist</span><span class="sxs-lookup"><span data-stu-id="8b388-157">Export data from Onboard</span></span>

<span data-ttu-id="8b388-158">Kui olete valmis, saate Onboardist laadida alla malle, juhiseid ja kandidaatide andmeid.</span><span class="sxs-lookup"><span data-stu-id="8b388-158">When you're ready, you can download templates, guides, and candidate data from Onboard.</span></span>

1. <span data-ttu-id="8b388-159">Avage [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).</span><span class="sxs-lookup"><span data-stu-id="8b388-159">Go to [https://aka.ms/OnboardDataExport](https://aka.ms/OnboardDataExport).</span></span>

2. <span data-ttu-id="8b388-160">Valige jaotises **Andmete eksport** käsk **Taotle andmeid eksportimist**.</span><span class="sxs-lookup"><span data-stu-id="8b388-160">Under **Data export**, select **Request a data export**.</span></span> 

   ![[<span data-ttu-id="8b388-161">Onboardist andmete ekspordi taotlemine</span><span class="sxs-lookup"><span data-stu-id="8b388-161">Request a data export from Onboard</span></span>](./media/attract-onboard-export-data-onboard-request.png)](./media/attract-onboard-export-data-onboard-request.png)

3. <span data-ttu-id="8b388-162">Kui kuvatakse sõnumit **Teie taotlus on töötluses** valige nupp **OK**.</span><span class="sxs-lookup"><span data-stu-id="8b388-162">When the **Your request is being processed** message box appears, select **OK**.</span></span> <span data-ttu-id="8b388-163">Sõltuvalt ekspordi mahust võib andmete eksport võtta kuni 20 minutit.</span><span class="sxs-lookup"><span data-stu-id="8b388-163">The data export can take up to 20 minutes, depending on the size of your export.</span></span>

4. <span data-ttu-id="8b388-164">Kui eksport jõuab lõpuni, valige selle kõrval nupp **Laadi alla**.</span><span class="sxs-lookup"><span data-stu-id="8b388-164">When your export completes, select the **Download** button next to it.</span></span> 

   ![[<span data-ttu-id="8b388-165">Andmete ekspordi allalaadimine Onboardist</span><span class="sxs-lookup"><span data-stu-id="8b388-165">Download data export from Onboard</span></span>](./media/attract-onboard-export-data-onboard-download.png)](./media/attract-onboard-export-data-onboard-download.png)

   >[!NOTE]
   ><span data-ttu-id="8b388-166">Teie andmete eksport on saadaval seitse päeva.</span><span class="sxs-lookup"><span data-stu-id="8b388-166">Your data export is available for seven days.</span></span> <span data-ttu-id="8b388-167">Pärast seitset päeva link **Laadi alla** aegub peate taotlema uut eksporti, kui peate oma andmed uuesti alla laadima.</span><span class="sxs-lookup"><span data-stu-id="8b388-167">After seven days, the **Download** link expires, and you must request a new export if you need to download your data again.</span></span> <span data-ttu-id="8b388-168">Kui alustate uute andmete eksporti, aeguvad kõik olemasolevad allalaadimised pärast uue ekspordi õnnestumist.</span><span class="sxs-lookup"><span data-stu-id="8b388-168">When you start a new data export, any existing downloads will expire after the new export succeeds.</span></span>

<span data-ttu-id="8b388-169">Allalaadimine on zip-fail, mis sisaldab järgmist.</span><span class="sxs-lookup"><span data-stu-id="8b388-169">The download is a .zip file that contains:</span></span>

- <span data-ttu-id="8b388-170">Kaust **Mallid**, mis sisaldab teie Onboardi malle Wordi dokumendi vormingus.</span><span class="sxs-lookup"><span data-stu-id="8b388-170">A **Templates** folder that contains your Onboard templates in Word document format.</span></span>

- <span data-ttu-id="8b388-171">Kaust **Juhised**, mis sisaldab teie Onboardi juhiseid Wordi dokumendi vormingus.</span><span class="sxs-lookup"><span data-stu-id="8b388-171">A **Guides** folder that contains your Onboard guides in Word document format.</span></span>

## <a name="see-also"></a><span data-ttu-id="8b388-172">Vt ka</span><span class="sxs-lookup"><span data-stu-id="8b388-172">See also</span></span>

[<span data-ttu-id="8b388-173">Dynamics 365 Talent: Attracti ja Dynamics 365 Talent: Onboardi pensionile saatmine</span><span class="sxs-lookup"><span data-stu-id="8b388-173">Retiring Dynamics 365 Talent: Attract and Dynamics 365 Talent: Onboard Apps</span></span>](https://community.dynamics.com/365/talent/b/dynamics365fortalent/posts/retiring-dynamics-365-talent-attract-and-onboard-apps)