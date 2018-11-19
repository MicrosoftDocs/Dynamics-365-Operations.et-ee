---
title: "Hankimine tööriistaga LinkedIn Recruiter"
description: "Selles teemas kirjeldatakse masinõppe kasutamist töökohtade ja töökoha kandidaatide soovituste saamiseks."
author: josaw
manager: AnnBe
ms.date: 10/15/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: 
ms.author: josaw
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: 2fc6bf25d303d7d8de8002a923a080b90dcfbeab
ms.openlocfilehash: 106103e2c3d8f3d89aac5140174e5794da22536f
ms.contentlocale: et-ee
ms.lasthandoff: 10/24/2018

---

# <a name="sourcing-with-linkedin-recruiter"></a><span data-ttu-id="b733f-103">Hankimine tööriistaga LinkedIn Recruiter</span><span class="sxs-lookup"><span data-stu-id="b733f-103">Sourcing with LinkedIn Recruiter</span></span>
[!include[banner](../includes/banner.md)]

<span data-ttu-id="b733f-104">LinkedIn on maailma suurim talentide andmebaas ja tihti esmane süsteem, mida tööandjad kasutavad oma täidetavatele töökohtadele kandidaatide leidmiseks ja nendega suhtlemiseks.</span><span class="sxs-lookup"><span data-stu-id="b733f-104">LinkedIn is the world’s largest talent database and often the primary system that recruiters use to find, communicate with, and source candidates for the jobs that recruiters are looking to fill.</span></span> <span data-ttu-id="b733f-105">LinkedIn Recruiteri integreerimine tööriistaga Dynamics 365 for Talent: Attract muudab kasutajatele palkamise ja andmete sünkroonimise kahe süsteemi vahel lihtsamaks.</span><span class="sxs-lookup"><span data-stu-id="b733f-105">LinkedIn Recruiter integration with Dynamics 365 for Talent: Attract makes it easier for users to hire, and to keep the data in sync between the two systems.</span></span>

> [!NOTE]
> <span data-ttu-id="b733f-106">Teil on vaja, et tervikliku palkamise lisamooduli ja LinkedIn Recruiteri kohad suudaksid kasutada LinkedIn Recruiteri integratsiooni Attractiga.</span><span class="sxs-lookup"><span data-stu-id="b733f-106">You need the Comprehensive hiring add-on and LinkedIn Recruiter seats to be able to use LinkedIn Recruiter integration with Attract.</span></span>

## <a name="set-up-linkedin-recruiter-with-attract"></a><span data-ttu-id="b733f-107">LinkedIn Recruiteri häälestamine Attractiga</span><span class="sxs-lookup"><span data-stu-id="b733f-107">Set up LinkedIn Recruiter with Attract</span></span> 

<span data-ttu-id="b733f-108">Enne, kui saate LinkedIn Recruiteri võimalusi kasutada, peate konfigureerima lepingu tasandil või ettevõtte tasandil ligipääsu oma Attracti eksemplariga.</span><span class="sxs-lookup"><span data-stu-id="b733f-108">Before you can use the LinkedIn Recruiter capabilities, you must configure contract-level or company-level access with your Attract instance.</span></span> <span data-ttu-id="b733f-109">Konfiguratsiooniprotsessi lõpuleviimiseks peate töötama kasutajaga, kes on teie LinkedIn Recruiteri lepingu administraator.</span><span class="sxs-lookup"><span data-stu-id="b733f-109">To complete the configuration process, you must work with the user who is an Admin on your LinkedIn Recruiter contract.</span></span> <span data-ttu-id="b733f-110">LinkedIn Recruiteri konfigureerimiseks Attractiga toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="b733f-110">Complete the following steps to configure LinkedIn Recruiter with Attract.</span></span>

1.  <span data-ttu-id="b733f-111">Logige Attracti administraatorina sisse ja valige **Administraatori sätted**.</span><span class="sxs-lookup"><span data-stu-id="b733f-111">Sign in to Attract as an Admin and go to **Admin Settings**.</span></span>

2.  <span data-ttu-id="b733f-112">Klõpsake vasakul paanil vahekaarti **LinkedIni integreerimine**.</span><span class="sxs-lookup"><span data-stu-id="b733f-112">On the left pane, click the **LinkedIn Integration** tab.</span></span>

<span data-ttu-id="b733f-113">[![Attracti administraatori vaade LinkedIn Recruiteri integreerimise käivitamiseks](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span><span class="sxs-lookup"><span data-stu-id="b733f-113">[![Attract Admin view to start LinkedIn Recruiter integration](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span></span>

3.  <span data-ttu-id="b733f-114">Klõpsake seadistuse käivitamiseks **Ühenda** ja teid juhatatakse läbi LinkedIni sisselogimise protsessi.</span><span class="sxs-lookup"><span data-stu-id="b733f-114">Click **Connect** to start the setup and be guided through the LinkedIn sign-in process.</span></span>

4.  <span data-ttu-id="b733f-115">Kui teil on töökohad mitmes LinkedIni lepingus, valige leping, mida soovite Attracti süsteemiga ühendada.</span><span class="sxs-lookup"><span data-stu-id="b733f-115">If you have seats on multiple LinkedIn contracts, select the contract that you would like to connect to the Attract system.</span></span> <span data-ttu-id="b733f-116">Kui teil on töökoht ainult ühes LinkedIni lepingus, ei ole seda toimingut vaja.</span><span class="sxs-lookup"><span data-stu-id="b733f-116">If you have a seat on only one LinkedIn contract, this step will not be needed.</span></span>

5.  <span data-ttu-id="b733f-117">Nüüd laaditakse LinkedIni vidin teie administraatori sätetesse, kus see näitab integratsioonide loendit.</span><span class="sxs-lookup"><span data-stu-id="b733f-117">The LinkedIn widget will now load in your Admin settings with the list of integrations shown.</span></span> <span data-ttu-id="b733f-118">Klõpsake **Recruiter süsteemi ühendamine** all valikut **Taotlus**.</span><span class="sxs-lookup"><span data-stu-id="b733f-118">Under **Recruiter System connect**, click **Request**.</span></span>

<span data-ttu-id="b733f-119">[![Attracti administraatori vaade LinkedIn Recruiteri integreerimise taotlemiseks](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span><span class="sxs-lookup"><span data-stu-id="b733f-119">[![Attract Admin view to Request LinkedIn Recruiter integration](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span></span>

6.  <span data-ttu-id="b733f-120">Pärast Attractilt integratsiooni taotlemist, kuvatakse seda kui **Partner valmis** ja see on **Recruiteri administraatori sätted** alt sisselülitamiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="b733f-120">After the integration is requested from Attract, it will show as **Partner ready** and is ready to be turned on from **Recruiter Admin settings**.</span></span> <span data-ttu-id="b733f-121">Kui näete sellel lehel teadet **Teavita partnerit**, oodake paar sekundit, klõpsake teatel **Teavita partnerit** ja seejärel värskendage lehekülge.</span><span class="sxs-lookup"><span data-stu-id="b733f-121">If you see **Notify partner** on this page, wait a few seconds, click **Notify partner**, and then refresh the page.</span></span> <span data-ttu-id="b733f-122">Nüüd peaks olema kuvatud teade **Partner valmis**.</span><span class="sxs-lookup"><span data-stu-id="b733f-122">It should now show as **Partner ready**.</span></span>

<span data-ttu-id="b733f-123">[![Attracti administraatori vaade, mis näitab, et Attracti pool taotlusest on täidetud](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span><span class="sxs-lookup"><span data-stu-id="b733f-123">[![Attract Admin view to indicate Attract side of requests have been completed](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span></span>

<span data-ttu-id="b733f-124">Järgmise etapi läbimiseks peab teil olema oma LinkedIn Recruiteri lepingu administraatori privileeg.</span><span class="sxs-lookup"><span data-stu-id="b733f-124">To complete the next step, you need to have an Admin privilege on your LinkedIn Recruiter Contract.</span></span>

7.  <span data-ttu-id="b733f-125">Logige administraatori kontoga LinkedIni sisse ja minge üleval paremal asuva LinkedIn Recruiteri juurde.</span><span class="sxs-lookup"><span data-stu-id="b733f-125">Sign in to LinkedIn using the Admin account and go to LinkedIn Recruiter on the top right.</span></span> 

8. <span data-ttu-id="b733f-126">Klõpsake ekraani ülaosas olevas menüüs **Rohkem** valikule **Administraatori sätted** ja seejärel klõpsake **ATS** vahekaardil.</span><span class="sxs-lookup"><span data-stu-id="b733f-126">On the **More** menu at the top of the screen, click **Admin Settings**, and then click the **ATS** Tab.</span></span>

<span data-ttu-id="b733f-127">Attracti süsteem loetletakse koos mõne valikuga, mida saab sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="b733f-127">The Attract system will be listed with a couple of options that can be turned on.</span></span>

9. <span data-ttu-id="b733f-128">Kui soovite **In-ATS indikaatorile** ja **In-ATS profiilividinale** lubada ainult 1 klõpsuga eksportimise, valige **Ettevõtte tasemel juurdepääs**.</span><span class="sxs-lookup"><span data-stu-id="b733f-128">If you want to enable only 1-Click export for the **In-ATS indicator** and the **In-ATS Profile Widget**, select **Company-level access**.</span></span> <span data-ttu-id="b733f-129">Kui soovite lubada kõik ettevõtte tasemel ligipääsu funktsioonid ja InMail ajaloo, märkuste ajaloo ning InMail lühiprofiili ligipääsu, valige **lepingu tasemel juurdepääs**.</span><span class="sxs-lookup"><span data-stu-id="b733f-129">If you want to enable all of Company-level access features plus InMail history, Notes history, and the InMail stub profile access, select **Contract-level access**.</span></span>

10. <span data-ttu-id="b733f-130">Lülitage soovitud juurdepääsutase sisse oma LinkedIn Recruiteri **Administraator-ATS** sätetest.</span><span class="sxs-lookup"><span data-stu-id="b733f-130">Turn on the desired access level from your LinkedIn Recruiter **Admin-ATS** settings.</span></span>

<span data-ttu-id="b733f-131">[![Attracti integratsiooni sisse lülitamine LinkedIn Recruiteri administraatori vaatest](./media/EnableRSC.png)](./media/EnableRSC.png)</span><span class="sxs-lookup"><span data-stu-id="b733f-131">[![Turn on Attract integration from LinkedIn Recruiter Admin view](./media/EnableRSC.png)](./media/EnableRSC.png)</span></span>

12. <span data-ttu-id="b733f-132">Minge tagasi Attracti administraatori sätetesse rollis AttractAdmin ja valige vaheleht **LinkedIni integratsioon**. Nüüd peaksite nägema, et LinkedIni vidin laeb ja näitab sisse lülitatud valitud juurdepääsu tasemega **Lubatud**.</span><span class="sxs-lookup"><span data-stu-id="b733f-132">Go back to Attract Admin Settings as an AttractAdmin and select the **LinkedIn integration** tab. You should now see the LinkedIn widget load showing **Enabled** with the selected access level turned on.</span></span>

<span data-ttu-id="b733f-133">[![LinkedIn Recruiteri integreerimine lõpetatud](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span><span class="sxs-lookup"><span data-stu-id="b733f-133">[![LinkedIn Recruiter integration complete](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span></span>

## <a name="using-linkedin-recruiter-capabilities"></a><span data-ttu-id="b733f-134">LinkedIn Recruiteri võimaluste kasutamine</span><span class="sxs-lookup"><span data-stu-id="b733f-134">Using LinkedIn Recruiter capabilities</span></span>

<span data-ttu-id="b733f-135">Kui LinkedIn Recruiteri võimalused on Attracti administraatori poolt sisse lülitatud, saavad personalijuhid ja värbajad juurdepääsu.</span><span class="sxs-lookup"><span data-stu-id="b733f-135">After LinkedIn Recruiter capabilities has been enabled by the Attract Admin it is available for hiring managers and recruiters to access.</span></span> <span data-ttu-id="b733f-136">Nende võimaluste kasutamiseks ühendage **Kasutajasätete** alt oma LinkedIni konto.</span><span class="sxs-lookup"><span data-stu-id="b733f-136">To use these capabilities, connect your LinkedIn account under **User Settings**.</span></span> <span data-ttu-id="b733f-137">Kui nii administraatori kui ka kasutaja sätted on ühendatud, on saadaval mitmeid võimalusi.</span><span class="sxs-lookup"><span data-stu-id="b733f-137">Several capabilities will be available after both the Admin and User settings have been connected.</span></span>

### <a name="in-ats-profile-widget"></a><span data-ttu-id="b733f-138">In-ATS profiili vidin</span><span class="sxs-lookup"><span data-stu-id="b733f-138">In-ATS profile widget</span></span>

<span data-ttu-id="b733f-139">Saate Attractis vaadata kandidaadi LinkedIni profiili.</span><span class="sxs-lookup"><span data-stu-id="b733f-139">You can view the candidate’s LinkedIn profile in Attract.</span></span> <span data-ttu-id="b733f-140">LinkedIni vidin näitab kandidaadi profiili, kui ATS-i andmed kattuvad kasutajate LinkedIni andmetega.</span><span class="sxs-lookup"><span data-stu-id="b733f-140">The LinkedIn widget will display the candidate profile when the ATS information matches the LinkedIn information of its users.</span></span>

<span data-ttu-id="b733f-141">Profiili vaatamiseks minge kas töö või talendikausta kaudu kandidaadi profiili juurde.</span><span class="sxs-lookup"><span data-stu-id="b733f-141">To view a profile, go the candidate profile either from a job or talent pool.</span></span> <span data-ttu-id="b733f-142">Profiilividina laadimiseks valige kandidaadi profiilis vahekaart **LinkedIn**.</span><span class="sxs-lookup"><span data-stu-id="b733f-142">In the candidate profile, select the **LinkedIn** tab and the profile widget will load.</span></span> <span data-ttu-id="b733f-143">Näidake profiilividinat kasutades, kas see sobib.</span><span class="sxs-lookup"><span data-stu-id="b733f-143">Using the profile widget, indicate if this is the correct match.</span></span> <span data-ttu-id="b733f-144">Kui ei, leidke õige isik.</span><span class="sxs-lookup"><span data-stu-id="b733f-144">If it is not, find the correct person.</span></span> <span data-ttu-id="b733f-145">Sellelt lehelt saate kandidaadi ka oma LinkedIn Recruiteri projektidesse salvestada.</span><span class="sxs-lookup"><span data-stu-id="b733f-145">You can also save the candidate to your LinkedIn Recruiter projects from this page.</span></span>

### <a name="1-click-export"></a><span data-ttu-id="b733f-146">Ühe klõpsuga eksportimine</span><span class="sxs-lookup"><span data-stu-id="b733f-146">1-click export</span></span> 

<span data-ttu-id="b733f-147">LinkedInist kandidaatide otsimise ajal saate kandidaadid ühe klõpsuga hetkel vabade töökohtade juurde eksportida.</span><span class="sxs-lookup"><span data-stu-id="b733f-147">While sourcing candidates in LinkedIn, you can 1-click export the candidate to the jobs that you currently have open.</span></span> <span data-ttu-id="b733f-148">Ühe klõpsuga eksportimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="b733f-148">Complete the following steps for a 1-click export.</span></span> <span data-ttu-id="b733f-149">Enne nende etappide läbimist kontrollige, et teile on määratud töö personalijuhi või värbaja roll, ja et tööl oleks etapp **Potentsiaalselt sobiv kandidaat**.</span><span class="sxs-lookup"><span data-stu-id="b733f-149">Before you complete these steps, verify that you are a assigned the role of Hiring manager or Recruiter for the job and that the job has a **Prospect** stage.</span></span>

1.  <span data-ttu-id="b733f-150">Looge töö, määrake sobivad rollid ja aktiveerige töö.</span><span class="sxs-lookup"><span data-stu-id="b733f-150">Create the job, assign the appropriate roles, and activate the job.</span></span>

2.  <span data-ttu-id="b733f-151">Kui töö on aktiveeritud, liikuge LinkedIn Recruiterisse.</span><span class="sxs-lookup"><span data-stu-id="b733f-151">When the job is activated, navigate to LinkedIn Recruiter.</span></span>

3.  <span data-ttu-id="b733f-152">Leidke otsitav kandidaat ja minge tema profiilile.</span><span class="sxs-lookup"><span data-stu-id="b733f-152">Find the candidate that you are looking for and go to their profile.</span></span>

4.  <span data-ttu-id="b733f-153">Kontaktikaardi töö otsimise kasti abil leidke töö Attractis aktiveeritud töö pealkirja või töö ID-d kasutades.</span><span class="sxs-lookup"><span data-stu-id="b733f-153">Using the job search box in the contact card, find the job using the title or the Job ID that was activated in Attract.</span></span> <span data-ttu-id="b733f-154">Kui te tööd ei leia, klõpsake õige Attracti eksemplari leidmiseks valikul **Muuda ATS**.</span><span class="sxs-lookup"><span data-stu-id="b733f-154">If you don’t find the job, click **Change ATS** to find the correct Attract instance.</span></span>

5. <span data-ttu-id="b733f-155">Pärast töö valimist klõpsake valikul **Ekspordi**.</span><span class="sxs-lookup"><span data-stu-id="b733f-155">After the job is selected, click **Export**.</span></span> <span data-ttu-id="b733f-156">Kandidaat on nüüd Attracti sisse tõmmatud.</span><span class="sxs-lookup"><span data-stu-id="b733f-156">The candidate is now fetched by Attract.</span></span>

6.  <span data-ttu-id="b733f-157">Minge Attracti ja avage vastav töö.</span><span class="sxs-lookup"><span data-stu-id="b733f-157">Go to Attract and open the respective job.</span></span> <span data-ttu-id="b733f-158">Eksporditud kandidaadi leiate töö etapist **Potentsiaalselt sobiv kandidaat**.</span><span class="sxs-lookup"><span data-stu-id="b733f-158">You will find the candidate that you just exported in the **Prospect** stage of the job.</span></span>

### <a name="in-ats-indicator"></a><span data-ttu-id="b733f-159">In-ATS indikaator</span><span class="sxs-lookup"><span data-stu-id="b733f-159">In-ATS indicator</span></span> 

<span data-ttu-id="b733f-160">LinkedIn värbaja abil saate saate jälgida, kas kandidaat on kandideerinud teie organisatsioonis teistele töödele, vaadata, millistes erinevates tööle kandideerimise etappides nad on ning vaadata LinkedIn Recruiteris Attractist pärit tagasisidet ja kommentaare.</span><span class="sxs-lookup"><span data-stu-id="b733f-160">Using LinkedIn recruiter, you can track whether a candidate has applied to other jobs in your organization, look at where they are in different stages of job applications, and view the feedback and comments from Attract in LinkedIn Recruiter.</span></span>

1.  <span data-ttu-id="b733f-161">Avage LinkedIn Recruiter ja leidke otsitava kandidaadi profiil.</span><span class="sxs-lookup"><span data-stu-id="b733f-161">Open LinkedIn Recruiter and locate the candidate profile that you are looking for.</span></span>

2.  <span data-ttu-id="b733f-162">Kerige alla, et näha kandidaadi profiili jaotist **In-ATS**.</span><span class="sxs-lookup"><span data-stu-id="b733f-162">Scroll down to view the **In-ATS** section on the candidate’s profile.</span></span>

3.  <span data-ttu-id="b733f-163">Selle vidinaga saate vaadata LinkedIn Recruiteri vaate seest Attractis oleva kandidaadi kõiki andmeid.</span><span class="sxs-lookup"><span data-stu-id="b733f-163">You can use this widget to view all of the information about the candidate that’s present in Attract from within the LinkedIn Recruiter view.</span></span>

4.  <span data-ttu-id="b733f-164">Nendega seotud tööde, viimase oleku ja iga tööga seotud liikumise vaatamiseks valige vahekaart **Tööd ja olekud**.</span><span class="sxs-lookup"><span data-stu-id="b733f-164">Select the **Jobs & Statuses** tab to see jobs they are part of, the latest status, and how they have been moving against each job.</span></span>

5.  <span data-ttu-id="b733f-165">Intervjueerijate Attracti sisestatud tagasiside vaatamiseks valige vahekaart **Vestluse tagasiside**.</span><span class="sxs-lookup"><span data-stu-id="b733f-165">Select the **Interview Feedback** tab to see feedback that the interviewers have submitted in Attract.</span></span>

6.  <span data-ttu-id="b733f-166">Selle kandidaadi kohta Attracti jäädvustatud märkuste vaatamiseks valige vahekaart **Märkused**.</span><span class="sxs-lookup"><span data-stu-id="b733f-166">Select the **Notes** tab to see notes that have been captured for this applicant in Attract.</span></span>

### <a name="inmail-history"></a><span data-ttu-id="b733f-167">InMail ajalugu</span><span class="sxs-lookup"><span data-stu-id="b733f-167">InMail history</span></span>

<span data-ttu-id="b733f-168">LinkedIn InMail ajalugu on LinkedIn Recruiteriga saadaval lepingu tasandil juurdepääsuga.</span><span class="sxs-lookup"><span data-stu-id="b733f-168">The LinkedIn InMail history is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="b733f-169">Kui see on lubatud, saate vaadata oma kogu kandidaadiga seotud InMail ajalugu.</span><span class="sxs-lookup"><span data-stu-id="b733f-169">When it is enabled, you can view your entire InMail history with the candidate.</span></span> <span data-ttu-id="b733f-170">Samuti saate vaadata kes teie organisatsioonist on kandidaadiga veel inMaile vahetanud, kuid te ei saa vaadata nendevahelisi sõnumeid.</span><span class="sxs-lookup"><span data-stu-id="b733f-170">You can also see who else from your organization has exchanged InMail with the candidate, however you can't view the messages between them.</span></span>

<span data-ttu-id="b733f-171">InMail ajaloo vaatamiseks minge kandidaadi profiilile, minge vahekaardile **LinkedIn** ja kerige ajaloo vaatamiseks lehe allserva.</span><span class="sxs-lookup"><span data-stu-id="b733f-171">To view InMail history, go to a candidate’s profile, go to the **LinkedIn** tab and scroll to the bottom of the page to view the history.</span></span> <span data-ttu-id="b733f-172">InMail ajalugu saate vaadata ainult juhul, kui kandidaat on teie taotlusele vastanud ja oma profiili teiega LinkedInis jaganud.</span><span class="sxs-lookup"><span data-stu-id="b733f-172">You can view the InMail history only if the candidate has responded to your request and chosen to share their profile with you in LinkedIn.</span></span> <span data-ttu-id="b733f-173">InMaili sõnumid sünkroonitakse Attractiga iga paari tunni järel.</span><span class="sxs-lookup"><span data-stu-id="b733f-173">The messages from InMail sync with Attract every couple of hours.</span></span>

### <a name="notes-history"></a><span data-ttu-id="b733f-174">Märkuste ajalugu</span><span class="sxs-lookup"><span data-stu-id="b733f-174">Notes history</span></span> 

<span data-ttu-id="b733f-175">LinkedIni märkuste ajalugu on saadaval LinkedIn Recruiteri lepingu tasandil juurdepääsuga.</span><span class="sxs-lookup"><span data-stu-id="b733f-175">The LinkedIn notes history is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="b733f-176">Kui see on lubatud, saate vaadata märkusi, mis teie organisatsiooni erinevad värbajad on kandidaadi kohta jäädvustanud.</span><span class="sxs-lookup"><span data-stu-id="b733f-176">When it is enabled, you can view the notes that have been captured about the candidate by different recruiters from your organization.</span></span>

<span data-ttu-id="b733f-177">Märkuste ajaloo vaatamiseks minge kandidaadi profiilile, minge vahekaardile **LinkedIn** ja kerige ajaloo vaatamiseks lehe allserva.</span><span class="sxs-lookup"><span data-stu-id="b733f-177">To view Notes history, go to a candidate’s profile, go to the **LinkedIn** tab and scroll to the bottom of the page to view the history.</span></span> <span data-ttu-id="b733f-178">Saate vaadata kõiki LinkedIn Recruiterist pärit märkusi kandidaadi kohta.</span><span class="sxs-lookup"><span data-stu-id="b733f-178">You can view all the notes about the candidate from LinkedIn Recruiter.</span></span>

### <a name="inmail-stub-profile"></a><span data-ttu-id="b733f-179">InMail lühiprofiil</span><span class="sxs-lookup"><span data-stu-id="b733f-179">InMail stub profile</span></span>

<span data-ttu-id="b733f-180">InMail lühiprofiil on saadaval LinkedIn Recruiteri lepingu tasandil juurdepääsuga.</span><span class="sxs-lookup"><span data-stu-id="b733f-180">The InMail stub profile is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="b733f-181">Kui kandidaadid nõustuvad oma LinkedIn profiile jagama mistahes teie organisatsiooni kasutajaga, saate kandidaate Attractis jälgida ning igale kandidaadile luuakse uus kandidaadi kirje.</span><span class="sxs-lookup"><span data-stu-id="b733f-181">If candidates agree to share their LinkedIn profiles with any user in your organization, you can track the candidates in Attract and a new candidate record will be created for each candidate.</span></span>

<span data-ttu-id="b733f-182">Kandidaatide loendi vaatamiseks avage **Talendikaustad**, et näha süsteemi loodud LinkdedIni talentide kausta.</span><span class="sxs-lookup"><span data-stu-id="b733f-182">To view the list of candidates, go to **Talent pools** to see a system-created LinkedIn talent pool.</span></span> <span data-ttu-id="b733f-183">See talentide kaust sisaldab kandidaatide loendit ja nende LinkedInist saadud lühiprofiile, mis näitavad kandidaatide eesnime ja perekonnanime.</span><span class="sxs-lookup"><span data-stu-id="b733f-183">This talent pool contains the list candidates and their stub profiles as received from LinkedIn, showing the candidate's first name and last name.</span></span> <span data-ttu-id="b733f-184">Kandidaadi e-posti aadressi kuvatakse siis, kui kandidaat soovib oma e-posti aadressi jagada.</span><span class="sxs-lookup"><span data-stu-id="b733f-184">The candidate’s email ID will be displayed if the candidate had chosen to share their email address.</span></span>

