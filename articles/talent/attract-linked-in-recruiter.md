---
title: Hankimine tööriistaga LinkedIn Recruiter
description: Selles teemas kirjeldatakse masinõppe kasutamist töökohtade ja töökoha kandidaatide soovituste saamiseks.
author: andreabichsel
manager: AnnBe
ms.date: 12/07/2018
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
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 4ac7a302e5bf589beb2b560b0ff5818e90c67139
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 05/07/2019
ms.locfileid: "1517766"
---
# <a name="sourcing-with-linkedin-recruiter"></a><span data-ttu-id="5e7f5-103">Hankimine tööriistaga LinkedIn Recruiter</span><span class="sxs-lookup"><span data-stu-id="5e7f5-103">Sourcing with LinkedIn Recruiter</span></span>
[!include[banner](../includes/banner.md)]

<span data-ttu-id="5e7f5-104">LinkedIn on maailma suurim talentide andmebaas ja tihti esmane süsteem, mida tööandjad kasutavad oma täidetavatele töökohtadele kandidaatide leidmiseks ja nendega suhtlemiseks.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-104">LinkedIn is the world’s largest talent database and often the primary system that recruiters use to find, communicate with, and source candidates for the jobs that recruiters are looking to fill.</span></span> <span data-ttu-id="5e7f5-105">Platvormi LinkedIn Recruiter integreerimine rakendusega Dynamics 365 for Talent: Attract teeb kasutajate jaoks värbamise ja nende kahe süsteemi vahelise andmete sünkroonimise lihtsamaks.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-105">LinkedIn Recruiter integration with Dynamics 365 for Talent: Attract makes it easier for users to hire, and to keep the data in sync between the two systems.</span></span>

> [!NOTE]
> <span data-ttu-id="5e7f5-106">Platvormi LinkedIn Recruiter ja rakenduse Attract integratsiooni kasutamiseks on vaja tervikliku värbamise lisandmoodulit ja platvormi LinkedIn Recruiter töökohti.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-106">You need the Comprehensive hiring add-on and LinkedIn Recruiter seats to be able to use LinkedIn Recruiter integration with Attract.</span></span>

## <a name="set-up-linkedin-recruiter-with-attract"></a><span data-ttu-id="5e7f5-107">Platvormi LinkedIn Recruiter ja rakenduse Attract seadistamine</span><span class="sxs-lookup"><span data-stu-id="5e7f5-107">Set up LinkedIn Recruiter with Attract</span></span> 

<span data-ttu-id="5e7f5-108">Enne platvormi LinkedIn Recruiter võimaluste kasutamist peate konfigureerima lepingu või ettevõtte tasandil juurdepääsu oma Attracti eksemplarile.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-108">Before you can use the LinkedIn Recruiter capabilities, you must configure contract-level or company-level access with your Attract instance.</span></span> <span data-ttu-id="5e7f5-109">Konfigureerimise lõpuleviimiseks peate töötama kasutajaga, kes on platvormi LinkedIn Recruiter lepingu järgi administraator.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-109">To complete the configuration process, you must work with the user who is an Admin on your LinkedIn Recruiter contract.</span></span> <span data-ttu-id="5e7f5-110">Platvormi LinkedIn Recruiter konfigureerimiseks rakendusega Attract tehke järgmised toimingud.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-110">Complete the following steps to configure LinkedIn Recruiter with Attract.</span></span>

1.  <span data-ttu-id="5e7f5-111">Logige Attracti administraatorina sisse ja valige **Administraatori sätted**.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-111">Sign in to Attract as an Admin and go to **Admin Settings**.</span></span>

2.  <span data-ttu-id="5e7f5-112">Klõpsake vasakul paanil vahekaarti **LinkedIni integreerimine**.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-112">On the left pane, click the **LinkedIn Integration** tab.</span></span>

<span data-ttu-id="5e7f5-113">[![Attracti administraatori vaade LinkedIn Recruiteri integreerimise käivitamiseks](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span><span class="sxs-lookup"><span data-stu-id="5e7f5-113">[![Attract Admin view to start LinkedIn Recruiter integration](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)</span></span>

3.  <span data-ttu-id="5e7f5-114">Klõpsake seadistuse käivitamiseks **Ühenda** ja teid juhatatakse läbi LinkedIni sisselogimise protsessi.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-114">Click **Connect** to start the setup and be guided through the LinkedIn sign-in process.</span></span>

4.  <span data-ttu-id="5e7f5-115">Kui teil on töökohad mitmes LinkedIni lepingus, valige leping, mida soovite Attracti süsteemiga ühendada.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-115">If you have seats on multiple LinkedIn contracts, select the contract that you would like to connect to the Attract system.</span></span> <span data-ttu-id="5e7f5-116">Kui teil on töökoht ainult ühes LinkedIni lepingus, ei ole seda toimingut vaja.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-116">If you have a seat on only one LinkedIn contract, this step will not be needed.</span></span>

5.  <span data-ttu-id="5e7f5-117">Nüüd laaditakse LinkedIni vidin teie administraatori sätetesse, kus see näitab integratsioonide loendit.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-117">The LinkedIn widget will now load in your Admin settings with the list of integrations shown.</span></span> <span data-ttu-id="5e7f5-118">Klõpsake **Recruiter süsteemi ühendamine** all valikut **Taotlus**.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-118">Under **Recruiter System connect**, click **Request**.</span></span>

<span data-ttu-id="5e7f5-119">[![Attracti administraatori vaade LinkedIn Recruiteri integreerimise taotlemiseks](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span><span class="sxs-lookup"><span data-stu-id="5e7f5-119">[![Attract Admin view to Request LinkedIn Recruiter integration](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)</span></span>

6.  <span data-ttu-id="5e7f5-120">Pärast Attractilt integratsiooni taotlemist, kuvatakse seda kui **Partner valmis** ja see on **Recruiteri administraatori sätted** alt sisselülitamiseks valmis.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-120">After the integration is requested from Attract, it will show as **Partner ready** and is ready to be turned on from **Recruiter Admin settings**.</span></span> <span data-ttu-id="5e7f5-121">Kui näete sellel lehel teadet **Teavita partnerit**, oodake paar sekundit, klõpsake teatel **Teavita partnerit** ja seejärel värskendage lehekülge.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-121">If you see **Notify partner** on this page, wait a few seconds, click **Notify partner**, and then refresh the page.</span></span> <span data-ttu-id="5e7f5-122">Nüüd peaks olema kuvatud teade **Partner valmis**.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-122">It should now show as **Partner ready**.</span></span>

<span data-ttu-id="5e7f5-123">[![Attracti administraatori vaade, mis näitab, et Attracti pool taotlusest on täidetud](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span><span class="sxs-lookup"><span data-stu-id="5e7f5-123">[![Attract Admin view to indicate Attract side of requests have been completed](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)</span></span>

<span data-ttu-id="5e7f5-124">Järgmise etapi läbimiseks peab teil olema LinkedIn Recruiteri lepingu administraatori privileeg.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-124">To complete the next step, you need to have an Admin privilege on your LinkedIn Recruiter Contract.</span></span>

7.  <span data-ttu-id="5e7f5-125">Logige administraatori kontoga LinkedIni sisse ja avage üleval paremal asuv LinkedIn Recruiter.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-125">Sign in to LinkedIn using the Admin account and go to LinkedIn Recruiter on the top right.</span></span> 

8. <span data-ttu-id="5e7f5-126">Klõpsake ekraani ülaosas olevas menüüs **Rohkem** valikule **Administraatori sätted** ja seejärel klõpsake **ATS** vahekaardil.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-126">On the **More** menu at the top of the screen, click **Admin Settings**, and then click the **ATS** Tab.</span></span>

<span data-ttu-id="5e7f5-127">Attracti süsteem loetletakse koos mõne valikuga, mida saab sisse lülitada.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-127">The Attract system will be listed with a couple of options that can be turned on.</span></span>

9. <span data-ttu-id="5e7f5-128">Kui soovite **In-ATS indikaatorile** ja **In-ATS profiilividinale** lubada ainult 1 klõpsuga eksportimise, valige **Ettevõtte tasemel juurdepääs**.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-128">If you want to enable only 1-Click export for the **In-ATS indicator** and the **In-ATS Profile Widget**, select **Company-level access**.</span></span> <span data-ttu-id="5e7f5-129">Kui soovite lubada kõik ettevõttetasemel juurdepääsu funktsioonid ja InMaili ajaloo, märkuste ajaloo ning InMaili lühiprofiili juurdepääsu, valige suvand **Lepingu tasemel juurdepääs**.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-129">If you want to enable all of Company-level access features plus InMail history, Notes history, and the InMail stub profile access, select **Contract-level access**.</span></span>

10. <span data-ttu-id="5e7f5-130">Lülitage soovitud juurdepääsutase sisse oma LinkedIn Recruiteri **Administraator-ATS** sätetest.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-130">Turn on the desired access level from your LinkedIn Recruiter **Admin-ATS** settings.</span></span>

<span data-ttu-id="5e7f5-131">[![Attracti integratsiooni sisselülitamine LinkedIn Recruiteri administraatori vaatest](./media/EnableRSC.png)](./media/EnableRSC.png)</span><span class="sxs-lookup"><span data-stu-id="5e7f5-131">[![Turn on Attract integration from LinkedIn Recruiter Admin view](./media/EnableRSC.png)](./media/EnableRSC.png)</span></span>

12. <span data-ttu-id="5e7f5-132">Minge tagasi Attracti administraatori sätetesse rollis AttractAdmin ja valige vaheleht **LinkedIni integratsioon**. Nüüd peaksite nägema, et LinkedIni vidin laeb ja näitab sisse lülitatud valitud juurdepääsu tasemega **Lubatud**.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-132">Go back to Attract Admin Settings as an AttractAdmin and select the **LinkedIn integration** tab. You should now see the LinkedIn widget load showing **Enabled** with the selected access level turned on.</span></span>

<span data-ttu-id="5e7f5-133">[![LinkedIn Recruiter integratsioon on lõpetatud](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span><span class="sxs-lookup"><span data-stu-id="5e7f5-133">[![LinkedIn Recruiter integration complete](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)</span></span>

## <a name="using-linkedin-recruiter-capabilities"></a><span data-ttu-id="5e7f5-134">Platvormi LinkedIn Recruiter võimaluste kasutamine</span><span class="sxs-lookup"><span data-stu-id="5e7f5-134">Using LinkedIn Recruiter capabilities</span></span>

<span data-ttu-id="5e7f5-135">Pärast platvormi LinkedIn Recruiter võimaluste lubamist Attracti administraatori poolt on sellele juurdepääs värbamisjuhtidel ja värbajatel.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-135">After LinkedIn Recruiter capabilities has been enabled by the Attract Admin it is available for hiring managers and recruiters to access.</span></span> <span data-ttu-id="5e7f5-136">Nende võimaluste kasutamiseks ühendage **Kasutajasätete** alt oma LinkedIni konto.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-136">To use these capabilities, connect your LinkedIn account under **User Settings**.</span></span> <span data-ttu-id="5e7f5-137">Kui nii administraatori kui ka kasutaja sätted on ühendatud, on saadaval mitmeid võimalusi.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-137">Several capabilities will be available after both the Admin and User settings have been connected.</span></span>

### <a name="in-ats-profile-widget"></a><span data-ttu-id="5e7f5-138">In-ATS profiili vidin</span><span class="sxs-lookup"><span data-stu-id="5e7f5-138">In-ATS profile widget</span></span>

<span data-ttu-id="5e7f5-139">Saate Attractis vaadata kandidaadi LinkedIni profiili.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-139">You can view the candidate’s LinkedIn profile in Attract.</span></span> <span data-ttu-id="5e7f5-140">LinkedIni vidin näitab kandidaadi profiili, kui ATS-i andmed kattuvad kasutajate LinkedIni andmetega.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-140">The LinkedIn widget will display the candidate profile when the ATS information matches the LinkedIn information of its users.</span></span>

<span data-ttu-id="5e7f5-141">Profiili vaatamiseks minge kas töö või talendikausta kaudu kandidaadi profiili juurde.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-141">To view a profile, go the candidate profile either from a job or talent pool.</span></span> <span data-ttu-id="5e7f5-142">Profiilividina laadimiseks valige kandidaadi profiilis vahekaart **LinkedIn**.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-142">In the candidate profile, select the **LinkedIn** tab and the profile widget will load.</span></span> <span data-ttu-id="5e7f5-143">Sellel lehel saate ka salvestada kandidaadi oma LinkedIn Recruiteri projektidesse.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-143">You can also save the candidate to your LinkedIn Recruiter projects from this page.</span></span>
1. <span data-ttu-id="5e7f5-144">E-posti ja LinkedIni liikme ID (täpne vaste) vaste leidmisel LinkedInis kuvatakse kandidaadi profiili.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-144">If LinkedIn found the match based on email and LinkedIn member ID (exact match), the candidate's profile will be shown.</span></span> <span data-ttu-id="5e7f5-145">Kasutajal on endiselt võimalus profiili suvand linkida/linkimine tühistada.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-145">The user still has an option to link/unlink the profile.</span></span>

2. <span data-ttu-id="5e7f5-146">Kui LinkedIn ei leia kandidaati e-posti või liikme ID põhjal, kuvatakse võimalike kandidaatide vastete loend vastavalt kandidaadi nime järgi ja kasutaja saab valida neist ühe ning linkida profiili.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-146">If LinkedIn cannot find the candidate based on their email or member ID, it will show a list of possible candidate matches based on candidate name and the user can choose one of them and link the profile.</span></span>  

3. <span data-ttu-id="5e7f5-147">Kui LinkedIn ei leia kandidaadi nime, tuleb teade, et ei leitud ühtki vastet.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-147">If LinkedIn cannot find any candidate based on the name, it will return that no match was found.</span></span>

### <a name="1-click-export"></a><span data-ttu-id="5e7f5-148">Ühe klõpsuga eksportimine</span><span class="sxs-lookup"><span data-stu-id="5e7f5-148">1-click export</span></span> 

<span data-ttu-id="5e7f5-149">LinkedInist kandidaatide otsimise ajal saate kandidaadid ühe klõpsuga hetkel vabade töökohtade juurde eksportida.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-149">While sourcing candidates in LinkedIn, you can 1-click export the candidate to the jobs that you currently have open.</span></span> <span data-ttu-id="5e7f5-150">Ühe klõpsuga eksportimiseks toimige järgmiselt.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-150">Complete the following steps for a 1-click export.</span></span> <span data-ttu-id="5e7f5-151">Enne nende etappide läbimist kontrollige, et teile on määratud töö personalijuhi või värbaja roll, ja et tööl oleks etapp **Potentsiaalselt sobiv kandidaat**.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-151">Before you complete these steps, verify that you are a assigned the role of Hiring manager or Recruiter for the job and that the job has a **Prospect** stage.</span></span>

1.  <span data-ttu-id="5e7f5-152">Looge töö, määrake sobivad rollid ja aktiveerige töö.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-152">Create the job, assign the appropriate roles, and activate the job.</span></span>

2.  <span data-ttu-id="5e7f5-153">Kui töö on aktiveeritud, liikuge LinkedIn Recruiterisse.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-153">When the job is activated, navigate to LinkedIn Recruiter.</span></span>

3.  <span data-ttu-id="5e7f5-154">Leidke otsitav kandidaat ja minge tema profiilile.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-154">Find the candidate that you are looking for and go to their profile.</span></span>

4.  <span data-ttu-id="5e7f5-155">Kontaktikaardi töö otsimise kasti abil leidke töö Attractis aktiveeritud töö pealkirja või töö ID-d kasutades.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-155">Using the job search box in the contact card, find the job using the title or the Job ID that was activated in Attract.</span></span> <span data-ttu-id="5e7f5-156">Kui te tööd ei leia, klõpsake õige Attracti eksemplari leidmiseks valikul **Muuda ATS**.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-156">If you don’t find the job, click **Change ATS** to find the correct Attract instance.</span></span>

5. <span data-ttu-id="5e7f5-157">Pärast töö valimist klõpsake valikul **Ekspordi**.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-157">After the job is selected, click **Export**.</span></span> <span data-ttu-id="5e7f5-158">Kandidaat on nüüd Attracti sisse tõmmatud.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-158">The candidate is now fetched by Attract.</span></span>

6.  <span data-ttu-id="5e7f5-159">Minge Attracti ja avage vastav töö.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-159">Go to Attract and open the respective job.</span></span> <span data-ttu-id="5e7f5-160">Eksporditud kandidaadi leiate töö etapist **Potentsiaalselt sobiv kandidaat**.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-160">You will find the candidate that you just exported in the **Prospect** stage of the job.</span></span>

### <a name="in-ats-indicator"></a><span data-ttu-id="5e7f5-161">In-ATS indikaator</span><span class="sxs-lookup"><span data-stu-id="5e7f5-161">In-ATS indicator</span></span> 

<span data-ttu-id="5e7f5-162">Platvormi LinkedIn Recruiter abil saate jälgida, kas kandidaat on kandideerinud muudele töökohtadele teie organisatsioonis, vaadata, millistes töökohale kandideerimise eri etappides ta on ning vaadata platvormi LinkedIn Recruiter vahendusel rakendusest Attract pärit tagasisidet ja kommentaare.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-162">Using LinkedIn recruiter, you can track whether a candidate has applied to other jobs in your organization, look at where they are in different stages of job applications, and view the feedback and comments from Attract in LinkedIn Recruiter.</span></span>

1.  <span data-ttu-id="5e7f5-163">Avage LinkedIn Recruiter ja otsige üles soovitud kandidaadi profiil.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-163">Open LinkedIn Recruiter and locate the candidate profile that you are looking for.</span></span>

2.  <span data-ttu-id="5e7f5-164">Kerige alla, et näha kandidaadi profiili jaotist **In-ATS**.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-164">Scroll down to view the **In-ATS** section on the candidate’s profile.</span></span>

3.  <span data-ttu-id="5e7f5-165">Selle vidina abil saate vaadata platvormi LinkedIn Recruiter vaate kaudu kõiki kandidaadi andmeid, mis on rakenduses Attract.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-165">You can use this widget to view all of the information about the candidate that’s present in Attract from within the LinkedIn Recruiter view.</span></span>

4.  <span data-ttu-id="5e7f5-166">Nendega seotud tööde, viimase oleku ja iga tööga seotud liikumise vaatamiseks valige vahekaart **Tööd ja olekud**.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-166">Select the **Jobs & Statuses** tab to see jobs they are part of, the latest status, and how they have been moving against each job.</span></span>

5.  <span data-ttu-id="5e7f5-167">Intervjueerijate Attracti sisestatud tagasiside vaatamiseks valige vahekaart **Vestluse tagasiside**.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-167">Select the **Interview Feedback** tab to see feedback that the interviewers have submitted in Attract.</span></span>

6.  <span data-ttu-id="5e7f5-168">Selle kandidaadi kohta Attracti jäädvustatud märkuste vaatamiseks valige vahekaart **Märkused**.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-168">Select the **Notes** tab to see notes that have been captured for this applicant in Attract.</span></span>

> [!NOTE]
> <span data-ttu-id="5e7f5-169">Kandidaadi ja kandideerimise andmeid ei sünkroonita platvormiga LinkedIn Recruiter, kui kandidaat ei ole potentsiaalselt sobiva kandidaadi etapist edasi jõudnud.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-169">Candidate and application data will not be synced to LinkedIn Recruiter if the candidate hasn't moved past the prospect stage.</span></span>

### <a name="inmail-history"></a><span data-ttu-id="5e7f5-170">InMaili ajalugu</span><span class="sxs-lookup"><span data-stu-id="5e7f5-170">InMail history</span></span>

<span data-ttu-id="5e7f5-171">LinkedIn InMaili ajalugu on saadaval LinkedIn Recruiteri lepingu tasandil juurdepääsu korral.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-171">The LinkedIn InMail history is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="5e7f5-172">Kui see on lubatud, saate vaadata oma kogu kandidaadiga seotud InMaili ajalugu.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-172">When it is enabled, you can view your entire InMail history with the candidate.</span></span> <span data-ttu-id="5e7f5-173">Samuti saate vaadata, kes teie organisatsioonist on kandidaadiga veel InMaile vahetanud, kuid te ei saa vaadata nendevahelisi sõnumeid.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-173">You can also see who else from your organization has exchanged InMail with the candidate, however you can't view the messages between them.</span></span>

<span data-ttu-id="5e7f5-174">InMaili ajaloo vaatamiseks minge kandidaadi profiilile, vahekaardile **LinkedIn** ja kerige ajaloo vaatamiseks lehe alaserva.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-174">To view InMail history, go to a candidate’s profile, go to the **LinkedIn** tab and scroll to the bottom of the page to view the history.</span></span> <span data-ttu-id="5e7f5-175">Kui teil on olnud kandidaadiga arutelu, saate vaadata InMaili ajalugu.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-175">You can view InMail history if you have had a discussion with the candidate.</span></span> <span data-ttu-id="5e7f5-176">InMaili sõnumid sünkroonitakse Attractiga iga paari tunni järel.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-176">The messages from InMail will sync with Attract every couple of hours.</span></span>

### <a name="notes-history"></a><span data-ttu-id="5e7f5-177">Märkuste ajalugu</span><span class="sxs-lookup"><span data-stu-id="5e7f5-177">Notes history</span></span> 

<span data-ttu-id="5e7f5-178">LinkedIni märkmete ajalugu on saadaval LinkedIn Recruiteri lepingu tasandil juurdepääsu korral.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-178">The LinkedIn notes history is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="5e7f5-179">Kui see on lubatud, saate vaadata märkusi, mis teie organisatsiooni erinevad värbajad on kandidaadi kohta jäädvustanud.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-179">When it is enabled, you can view the notes that have been captured about the candidate by different recruiters from your organization.</span></span>

<span data-ttu-id="5e7f5-180">Märkuste ajaloo vaatamiseks minge kandidaadi profiilile, minge vahekaardile **LinkedIn** ja kerige ajaloo vaatamiseks lehe allserva.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-180">To view Notes history, go to a candidate’s profile, go to the **LinkedIn** tab and scroll to the bottom of the page to view the history.</span></span> <span data-ttu-id="5e7f5-181">Kõiki kandidaadi kohta olevaid märkmeid saate vaadata platvormi LinkedIn Recruiter vahendusel.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-181">You can view all the notes about the candidate from LinkedIn Recruiter.</span></span>

### <a name="inmail-stub-profile"></a><span data-ttu-id="5e7f5-182">InMaili lühiprofiil</span><span class="sxs-lookup"><span data-stu-id="5e7f5-182">InMail stub profile</span></span>

<span data-ttu-id="5e7f5-183">InMaili lühiprofiil on saadaval LinkedIn Recruiteri lepingu tasandil juurdepääsu korral.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-183">The InMail stub profile is available with contract-level access with LinkedIn Recruiter.</span></span> <span data-ttu-id="5e7f5-184">Kui kandidaadid nõustuvad oma LinkedIn profiile jagama mistahes teie organisatsiooni kasutajaga, saate kandidaate Attractis jälgida ning igale kandidaadile luuakse uus kandidaadi kirje.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-184">If candidates agree to share their LinkedIn profiles with any user in your organization, you can track the candidates in Attract and a new candidate record will be created for each candidate.</span></span> <span data-ttu-id="5e7f5-185">Kui kandidaat on juba olemas süsteemis e-posti aadressiga või on jaganud oma aadressi värbajaga, saate vaadata kandidaadi e-posti aadressi.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-185">You can view candidate's email address if the candidate already exists in the system with an email address or has chosen to share their address with the recruiter.</span></span>

<span data-ttu-id="5e7f5-186">Kandidaatide loendi vaatamiseks avage **Talendikaustad**, et näha süsteemi loodud LinkdedIni talentide kausta.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-186">To view the list of candidates, go to **Talent pools** to see a system-created LinkedIn talent pool.</span></span> <span data-ttu-id="5e7f5-187">See talentide kaust sisaldab kandidaatide loendit ja nende LinkedInist saadud lühiprofiile, mis näitavad kandidaatide eesnime ja perekonnanime.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-187">This talent pool contains the list candidates and their stub profiles as received from LinkedIn, showing the candidate's first name and last name.</span></span> <span data-ttu-id="5e7f5-188">Kandidaadi e-posti aadressi kuvatakse siis, kui kandidaat soovib oma e-posti aadressi jagada.</span><span class="sxs-lookup"><span data-stu-id="5e7f5-188">The candidate’s email ID will be displayed if the candidate had chosen to share their email address.</span></span>
