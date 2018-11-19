---
title: Protsesside tegevused
description: "Selles teemas kirjeldatakse eri tüüpi tegevusi, mida saab kasutada värbamisprotsessis."
author: 
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
ms.author: rschloma
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: ccd9e2d0ff1f7fb6825c6823936b4013b3054f5d
ms.contentlocale: et-ee
ms.lasthandoff: 10/22/2018

---

# <a name="activities-in-the-hiring-processes"></a><span data-ttu-id="391ff-103">Värbamisprotsesside tegevused</span><span class="sxs-lookup"><span data-stu-id="391ff-103">Activities in the hiring processes</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="391ff-104">Microsoft Dynamics 365 for Talent: Attract võimaldab värbamisprotsessile lisada tegevusi.</span><span class="sxs-lookup"><span data-stu-id="391ff-104">Activities can be added as a part of the hiring process in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="391ff-105">Tegevusi saab lisada protsessimallile või neid saab lisada otse tööle värbamise protsessile.</span><span class="sxs-lookup"><span data-stu-id="391ff-105">Activities can be added to a process template, or they can be added directly to the hiring process in the job.</span></span> <span data-ttu-id="391ff-106">Pärast töö määratlemist valitakse protsessimall ja mallis sisalduvad tegevused rakendatakse tööle.</span><span class="sxs-lookup"><span data-stu-id="391ff-106">When a job is defined, a process template is selected, and the activities that are included in the template are applied to the job.</span></span> <span data-ttu-id="391ff-107">Kui mall on valimata, kasutatakse vaikemalli.</span><span class="sxs-lookup"><span data-stu-id="391ff-107">If a template isn't selected, the default template is used.</span></span> <span data-ttu-id="391ff-108">Värbamisprotsessi saab töö juures muuta ka pärast malli rakendamist.</span><span class="sxs-lookup"><span data-stu-id="391ff-108">The hiring process can also be modified on the job after the template is applied.</span></span>

> [!NOTE] 
> <span data-ttu-id="391ff-109">Protsessimallid on saadaval tervikliku värbamise lisandmooduli korral.</span><span class="sxs-lookup"><span data-stu-id="391ff-109">Process templates are available with the Comprehensive hiring add-on.</span></span>

## <a name="prospect-activity"></a><span data-ttu-id="391ff-110">Tegevus Potentsiaalselt sobiv kandidaat</span><span class="sxs-lookup"><span data-stu-id="391ff-110">Prospect activity</span></span>

<span data-ttu-id="391ff-111">Tegevus Potentsiaalselt sobiv kandidaat võimaldab tööle lisada potentsiaalselt sobivaid kandidaate.</span><span class="sxs-lookup"><span data-stu-id="391ff-111">The Prospect activity controls whether prospects can be added to a job.</span></span> <span data-ttu-id="391ff-112">Vaikimisi saab tööle lisada potentsiaalselt sobivaid kandidaate.</span><span class="sxs-lookup"><span data-stu-id="391ff-112">By default, prospects can be added to a job.</span></span> <span data-ttu-id="391ff-113">Tegevuse Potentsiaalselt sobiv kandidaat väljalülitamiseks määrake suvandi **Luba potentsiaalselt sobivad kandidaadid** olekuks **Väljas**.</span><span class="sxs-lookup"><span data-stu-id="391ff-113">To turn off the Prospect activity, set the **Enable prospects** option to **Off**.</span></span> <span data-ttu-id="391ff-114">Kui tegevus Potentsiaalselt sobiv kandidaat on sisse lülitatud, saavad personalijuhid potentsiaalselt sobivaid kandidaate lisada ja vaadata ning töö juures kuvatakse vahekaart **Potentsiaalselt sobiv kandidaat**.</span><span class="sxs-lookup"><span data-stu-id="391ff-114">When the Prospect activity is turned on, hiring managers can add and view prospects, and the **Prospect** tab is shown on the job.</span></span>

## <a name="application-activity"></a><span data-ttu-id="391ff-115">Tegevus Avaldus</span><span class="sxs-lookup"><span data-stu-id="391ff-115">Application activity</span></span>

<span data-ttu-id="391ff-116">Tegevus Avaldus on värbamisprotsessi mallis kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="391ff-116">The Application activity is required in the hiring process template.</span></span> <span data-ttu-id="391ff-117">Meilisõnumi saatmiseks kandidaatidele, kui nad on esitanud avalduse või lisatud etappi Avaldus, määrake suvandi **Saada kandidaadile meilisõnum** olekuks **Sees**.</span><span class="sxs-lookup"><span data-stu-id="391ff-117">To send email to candidates when they submit their application or are added to the Application stage, set the **Send mail to candidate** option to **On**.</span></span>

## <a name="scheduler-activity"></a><span data-ttu-id="391ff-118">Tegevus Plaanur</span><span class="sxs-lookup"><span data-stu-id="391ff-118">Scheduler activity</span></span>

<span data-ttu-id="391ff-119">Tegevus Plaanur ei ole kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="391ff-119">The Scheduler activity is optional.</span></span> <span data-ttu-id="391ff-120">Sellel tegevusel on kaks komponenti: Kandidaadi kättesaadavus ja Graafik.</span><span class="sxs-lookup"><span data-stu-id="391ff-120">This activity has two components: Candidate availability and Schedule.</span></span> <span data-ttu-id="391ff-121">Kandidaadi kättesaadavuse komponent võimaldab kasutada kandidaadi kättesaadavuse küsimiseks meili.</span><span class="sxs-lookup"><span data-stu-id="391ff-121">The Candidate availability component lets you use email to request a candidate's availability.</span></span> <span data-ttu-id="391ff-122">Graafiku komponent võimaldab planeerida töövestlusi kandidaadi ja värbamistöörühma vahel.</span><span class="sxs-lookup"><span data-stu-id="391ff-122">The Schedule component provides the ability to schedule interviews with the candidate and the hiring team.</span></span> <span data-ttu-id="391ff-123">Konfigureerida saab tegevuse Plaanur järgmisi suvandeid: **Küsi kandidaadi kättesaadavust**, **Võrgukoosolek** ja **Saada kandidaadile meilisõnum**.</span><span class="sxs-lookup"><span data-stu-id="391ff-123">In the Scheduler activity, the following options can be configured: **Request candidate availability**, **Online meeting**, and **Send mail to candidate**.</span></span>

- <span data-ttu-id="391ff-124">Kandidaatidele nende kättesaadavuse kohta küsimiseks meilisõnumi saatmiseks määrake suvandi **Küsi kandidaadi kättesaadavust** olekuks **Sees**.</span><span class="sxs-lookup"><span data-stu-id="391ff-124">To send email to candidates to request their availability, set the **Request candidate availability** option to **On**.</span></span> <span data-ttu-id="391ff-125">Kui määrate selle suvandi olekuks **Väljas**, seda etappi tööle värbamise protsessis ei kuvata.</span><span class="sxs-lookup"><span data-stu-id="391ff-125">If you set the option to **Off**, this step won't be shown in the hiring process on the job.</span></span>
- <span data-ttu-id="391ff-126">Videoülekande või konverentskõne tegemiseks rakendusega Skype for Business määrake välja **Võrgukoosolek** olekuks **Skype for Business**.</span><span class="sxs-lookup"><span data-stu-id="391ff-126">To live-stream or have a conference call by using Skype for Business, set the **Online meeting** field to **Skype for Business**.</span></span> <span data-ttu-id="391ff-127">Õige link **Liitu Skype’i koosolekuga** lisatakse seejärel intervjueerijatele saadetavale vestluskutsele.</span><span class="sxs-lookup"><span data-stu-id="391ff-127">The correct **Join Skype Meeting** link will then be added in the interview meeting request that is sent to interviewers.</span></span>
- <span data-ttu-id="391ff-128">Kandidaatidele graafiku lõplikuks kinnitamiseks meilisõnumi saatmiseks määrake suvandi **Saada kandidaadile meilisõnum** olekuks **Sees**.</span><span class="sxs-lookup"><span data-stu-id="391ff-128">To send email to candidates to finalize the schedule, set the **Send mail to candidate** option to **On**.</span></span> <span data-ttu-id="391ff-129">Kui määrate selle suvandi olekuks **Väljas**, saavad kandidaadid töövestluste graafiku ainult siis, kui logivad sisse kandidaadi portaali.</span><span class="sxs-lookup"><span data-stu-id="391ff-129">If you set the option to **Off**, candidates will receive the interview schedule only when they sign in to the Candidate portal.</span></span>

## <a name="feedback-activity"></a><span data-ttu-id="391ff-130">Tegevus Tagasiside</span><span class="sxs-lookup"><span data-stu-id="391ff-130">Feedback activity</span></span>

<span data-ttu-id="391ff-131">Tegevus Tagasiside ei ole kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="391ff-131">The Feedback activity is optional.</span></span> <span data-ttu-id="391ff-132">See tegevus võimaldab töövestluse osalejatel sisestada kandidaadile soovitusi.</span><span class="sxs-lookup"><span data-stu-id="391ff-132">This activity lets interview participants enter recommendations for an applicant.</span></span> <span data-ttu-id="391ff-133">Samuti saavad nad sisestada oma tagasisidekommentaarid.</span><span class="sxs-lookup"><span data-stu-id="391ff-133">They can also enter any feedback comments that they have.</span></span> <span data-ttu-id="391ff-134">Kui lülitate sisse suvandi **Tuleta tagasisides osalejad värbamistöörühmast**, sisestatakse värbaja, personalijuht ja intervjueerijad automaatselt tegevusse Tagasiside.</span><span class="sxs-lookup"><span data-stu-id="391ff-134">If you turn on the **Inherit feedback participants from Hiring Team** option, the recruiter, hiring manager, and interviewers are automatically entered in the Feedback activity.</span></span> <span data-ttu-id="391ff-135">Organisatsioonid võivad lubada intervjueerijatel enne tagasiside andmist vaadata teiste inimeste tagasisidet.</span><span class="sxs-lookup"><span data-stu-id="391ff-135">Organizations can allow interviewers to view the feedback of other people before they submit their own feedback.</span></span> <span data-ttu-id="391ff-136">Organisatsioonid võivad ka lubada pärast tagasiside andmist intervjueerijatel seda muuta.</span><span class="sxs-lookup"><span data-stu-id="391ff-136">Organizations can also allow interviewers to edit their feedback after they submit it.</span></span>

## <a name="interview-activity"></a><span data-ttu-id="391ff-137">Tegevus Töövestlus</span><span class="sxs-lookup"><span data-stu-id="391ff-137">Interview activity</span></span>

<span data-ttu-id="391ff-138">Tegevus Töövestlus ei ole kohustuslik.</span><span class="sxs-lookup"><span data-stu-id="391ff-138">The Interview activity is optional.</span></span> <span data-ttu-id="391ff-139">Sellel tegevusel on kolm komponenti: Kandidaadi kättesaadavus, Graafik ja Tagasiside.</span><span class="sxs-lookup"><span data-stu-id="391ff-139">This activity has three components: Candidate availability, Schedule, and Feedback.</span></span> <span data-ttu-id="391ff-140">Kandidaadi kättesaadavuse komponent võimaldab kasutada kandidaadi kättesaadavuse küsimiseks meili.</span><span class="sxs-lookup"><span data-stu-id="391ff-140">The Candidate availability component lets you use email to request a candidate's availability.</span></span> <span data-ttu-id="391ff-141">Graafiku komponent võimaldab planeerida töövestlusi kandidaadi ja värbamistöörühma vahel.</span><span class="sxs-lookup"><span data-stu-id="391ff-141">The Schedule component provides the ability to schedule interviews with the candidate and the hiring team.</span></span> <span data-ttu-id="391ff-142">Konfigureerida saab tegevuse Plaanur järgmisi suvandeid: **Küsi kandidaadi kättesaadavust**, **Võrgukoosolek** ja **Saada kandidaadile meilisõnum**.</span><span class="sxs-lookup"><span data-stu-id="391ff-142">In the Scheduler activity, the following options can be configured: **Request candidate availability**, **Online meeting**, and **Send mail to candidate**.</span></span>

- <span data-ttu-id="391ff-143">Kandidaatidele nende kättesaadavuse kohta küsimiseks meilisõnumi saatmiseks määrake suvandi **Küsi kandidaadi kättesaadavust** olekuks **Sees**.</span><span class="sxs-lookup"><span data-stu-id="391ff-143">To send email to candidates to request their availability, set the **Request candidate availability** option to **On**.</span></span> <span data-ttu-id="391ff-144">Kui määrate selle suvandi olekuks **Väljas**, seda etappi tööle värbamise protsessis ei kuvata.</span><span class="sxs-lookup"><span data-stu-id="391ff-144">If you set the option to **Off**, this step won't be shown in the hiring process on the job.</span></span>
- <span data-ttu-id="391ff-145">Videoülekande või konverentskõne tegemiseks rakendusega Skype for Business määrake välja **Võrgukoosolek** olekuks **Skype for Business**.</span><span class="sxs-lookup"><span data-stu-id="391ff-145">To live-stream or have a conference call by using Skype for Business, set the **Online meeting** field to **Skype for Business**.</span></span> <span data-ttu-id="391ff-146">Õige link **Liitu Skype’i koosolekuga** lisatakse seejärel saadetavale vestluskutsele.</span><span class="sxs-lookup"><span data-stu-id="391ff-146">The correct **Join Skype Meeting** link will then be added in the interview meeting request.</span></span>
- <span data-ttu-id="391ff-147">Kandidaatidele graafiku lõplikuks kinnitamiseks meilisõnumi saatmiseks määrake suvandi **Saada kandidaadile meilisõnum** olekuks **Sees**.</span><span class="sxs-lookup"><span data-stu-id="391ff-147">To send email to candidates to finalize the schedule, set the **Send mail to candidate** option to **On**.</span></span> <span data-ttu-id="391ff-148">Kui määrate selle suvandi olekuks **Väljas**, saavad kandidaadid töövestluste graafiku ainult siis, kui logivad sisse kandidaadi portaali.</span><span class="sxs-lookup"><span data-stu-id="391ff-148">If you set the option to **Off**, candidates will receive the interview schedule only when they sign in to the Candidate portal.</span></span>

<span data-ttu-id="391ff-149">Tagasiside komponent võimaldab inimestel sisestada kandidaadile soovitusi.</span><span class="sxs-lookup"><span data-stu-id="391ff-149">The Feedback component lets people enter recommendations for an applicant.</span></span> <span data-ttu-id="391ff-150">Samuti saavad nad sisestada oma tagasisidekommentaarid.</span><span class="sxs-lookup"><span data-stu-id="391ff-150">They can also enter any feedback comments that they have.</span></span> <span data-ttu-id="391ff-151">Kui lülitate sisse suvandi **Tuleta tagasisides osalejad värbamistöörühmast**, sisestatakse värbaja, personalijuht ja intervjueerijad automaatselt komponenti Tagasiside.</span><span class="sxs-lookup"><span data-stu-id="391ff-151">If you turn on the **Inherit feedback participants from Hiring Team** option, the recruiter, hiring manager, and interviewers are automatically entered in the Feedback component.</span></span> <span data-ttu-id="391ff-152">Organisatsioonid võivad lubada intervjueerijatel enne tagasiside andmist vaadata teiste inimeste tagasisidet.</span><span class="sxs-lookup"><span data-stu-id="391ff-152">Organizations can allow interviewers to view the feedback of other people before they submit their own feedback.</span></span> <span data-ttu-id="391ff-153">Organisatsioonid võivad ka lubada pärast tagasiside andmist intervjueerijatel seda muuta.</span><span class="sxs-lookup"><span data-stu-id="391ff-153">Organizations can also allow interviewers to edit their feedback after they submit it.</span></span>

## <a name="powerapps-activity"></a><span data-ttu-id="391ff-154">Tegevus PowerApps</span><span class="sxs-lookup"><span data-stu-id="391ff-154">PowerApps activity</span></span>

<span data-ttu-id="391ff-155">Tegevus PowerApps võimaldab värbamisprotsessi manustada rakenduse Microsoft PowerApps.</span><span class="sxs-lookup"><span data-stu-id="391ff-155">The PowerApps activity lets you embed a Microsoft PowerApps app in your hiring process.</span></span> <span data-ttu-id="391ff-156">Rakendus võib olla kohustuslik kõigile kandidaatidele, ainult ettevõttesisestele kandidaatidele, ainult ettevõttevälistele kandidaatidele või mitte ühelegi kandidaadile.</span><span class="sxs-lookup"><span data-stu-id="391ff-156">The app can be required for all applicants, internal applicants only, external applicants only, or no applicants.</span></span> <span data-ttu-id="391ff-157">Kui see rakendus märgitakse kohustuslikuks, peab enne etapi alustamist selle lõpule viima.</span><span class="sxs-lookup"><span data-stu-id="391ff-157">If the app is marked as required, it must be completed before the stage can be advanced.</span></span> <span data-ttu-id="391ff-158">Kui see rakendus ei ole kohustuslikuks märgitud, pole see tegevus kohustuslik, ja etappi saab alustada isegi siis, kui rakendus on lõpule viimata.</span><span class="sxs-lookup"><span data-stu-id="391ff-158">If the app isn't marked as required, the activity is an optional step, and the stage can be advanced even if the app isn't completed.</span></span>

<span data-ttu-id="391ff-159">Värbamisprotsessi jaoks tegevuse PowerApps salvestamiseks peate sisestama PowerAppsi ID.</span><span class="sxs-lookup"><span data-stu-id="391ff-159">To save the PowerApps activity to the hiring process, you must enter a PowerApps ID.</span></span> <span data-ttu-id="391ff-160">PowerAppsi ID leidmiseks valige [PowerApps](https://web.powerapps.com), **Rakendused** ja seejärel **Üksikasjad**.</span><span class="sxs-lookup"><span data-stu-id="391ff-160">To find the PowerApps ID, go to [PowerApps](https://web.powerapps.com), select **Apps**, and then select **Details**.</span></span>

<span data-ttu-id="391ff-161">Kui valite suvandi **Luba osalejate lisamine sellele tegevusele**, saab rakendusele, mis kasutab tegevust PowerApps, lisada kaasautoreid.</span><span class="sxs-lookup"><span data-stu-id="391ff-161">If you select the **Allow adding participants for this activity** option, additional contributors can be added for an application that uses the PowerApps activity.</span></span> <span data-ttu-id="391ff-162">Näiteks organisatsioon on loonud PowerAppsi rakenduse, mis on tehniliste rollide jaoks peetavate töövestluste küsimuste teek.</span><span class="sxs-lookup"><span data-stu-id="391ff-162">For example, an organization has created a PowerApps app that is a library of interview questions for technical roles.</span></span> <span data-ttu-id="391ff-163">See organisatsioon otsib parasjagu uut tarkvaraarendajat ja on lisanud tegevuse PowerApps tarkvaraarendaja rolli värbamisprotsessile.</span><span class="sxs-lookup"><span data-stu-id="391ff-163">The organization is now hiring a new software developer and has added the PowerApps activity to the hiring process for the Software Developer role.</span></span> <span data-ttu-id="391ff-164">Kui valitud on suvand **Luba osalejate lisamine sellele tegevusele**, saab värbaja või personalijuht, kes vaatab tarkvaraarendaja rolli jaoks olevat kandidaati, tegevusse PowerApps inimesi lisada.</span><span class="sxs-lookup"><span data-stu-id="391ff-164">If the **Allow adding participants for this activity** option is selected, a recruiter or hiring manager who is viewing an applicant for the Software Developer role can add people to the PowerApps activity.</span></span> <span data-ttu-id="391ff-165">Need inimesed saavad siis vaadata töövestluse küsimustega rakendust.</span><span class="sxs-lookup"><span data-stu-id="391ff-165">Those people can then view the app that has the interview questions.</span></span>

> [!NOTE]
> <span data-ttu-id="391ff-166">Tegevus PowerApps on saadaval ainult tervikliku värbamise lisandmooduli korral.</span><span class="sxs-lookup"><span data-stu-id="391ff-166">The PowerApps activity is available only with the Comprehensive hiring add-on.</span></span>

## <a name="youtube-activity"></a><span data-ttu-id="391ff-167">Tegevus YouTube</span><span class="sxs-lookup"><span data-stu-id="391ff-167">YouTube activity</span></span>

<span data-ttu-id="391ff-168">Tegevus YouTube võimaldab värbamisprotsessi osana jagada YouTube’i videot.</span><span class="sxs-lookup"><span data-stu-id="391ff-168">The YouTube activity lets you share a YouTube video as part of your hiring process.</span></span> <span data-ttu-id="391ff-169">Värbamisprotsessi jaoks tegevuse YouTube salvestamiseks on vajalik YouTube’i video URL.</span><span class="sxs-lookup"><span data-stu-id="391ff-169">To save the YouTube activity to the hiring process, you must specify the URL of the YouTube video.</span></span> <span data-ttu-id="391ff-170">Nii nagu tegevuse PowerApps korral, saate lubada ka sellele tegevusele osalejate lisamist.</span><span class="sxs-lookup"><span data-stu-id="391ff-170">As for the PowerApps activity, you can allow participants to be added to the activity.</span></span> <span data-ttu-id="391ff-171">Kui valite suvandi **Näita ainult kandidaadile**, näidatakse videot ainult kandidaatidele.</span><span class="sxs-lookup"><span data-stu-id="391ff-171">If you select the **Show only to candidate** option, the video is shown only as part of the candidate experience.</span></span> <span data-ttu-id="391ff-172">Seda ei näidata Attractis olevas värbamisprotsessis.</span><span class="sxs-lookup"><span data-stu-id="391ff-172">It isn't shown in the hiring process in Attract.</span></span>

> [!NOTE]
> <span data-ttu-id="391ff-173">Tegevus YouTube on saadaval ainult tervikliku värbamise lisandmooduli korral.</span><span class="sxs-lookup"><span data-stu-id="391ff-173">The YouTube activity is available only with the Comprehensive hiring add-on.</span></span>

## <a name="web-content-activity"></a><span data-ttu-id="391ff-174">Tegevus Veebisisu</span><span class="sxs-lookup"><span data-stu-id="391ff-174">Web content activity</span></span>

<span data-ttu-id="391ff-175">Tegevus Veebisisu võimaldab teil värbamisprotsessi manustada veebisisu.</span><span class="sxs-lookup"><span data-stu-id="391ff-175">The Web content activity lets you embed online content in your hiring process.</span></span> <span data-ttu-id="391ff-176">Värbamisprotsessi jaoks tegevuse Veebisisu salvestamiseks on vajalik sisu URL.</span><span class="sxs-lookup"><span data-stu-id="391ff-176">To save the Web content activity to the hiring process, you must specify the URL of the content.</span></span> <span data-ttu-id="391ff-177">Nii nagu tegevuste PowerApps ja YouTube korral, saate lubada ka sellele tegevusele osalejate lisamist.</span><span class="sxs-lookup"><span data-stu-id="391ff-177">As for the PowerApps and YouTube activities, you can allow participants to be added to the activity.</span></span> <span data-ttu-id="391ff-178">Kui valite suvandi **Näita ainult kandidaadile**, näidatakse sisu ainult kandidaatidele.</span><span class="sxs-lookup"><span data-stu-id="391ff-178">If you select the **Show only to candidate** option, the content is shown only as part of the candidate experience.</span></span> <span data-ttu-id="391ff-179">Seda ei näidata Attractis olevas värbamisprotsessis.</span><span class="sxs-lookup"><span data-stu-id="391ff-179">It isn't shown in the hiring process in Attract.</span></span> <span data-ttu-id="391ff-180">Te saate valida kuvatava sisu suuruse.</span><span class="sxs-lookup"><span data-stu-id="391ff-180">You can select the size of the content that is shown.</span></span>

> [!NOTE]
> <span data-ttu-id="391ff-181">Tegevus Veebisisu on saadaval ainult tervikliku värbamise lisandmooduli korral.</span><span class="sxs-lookup"><span data-stu-id="391ff-181">The Web content activity is available only with the Comprehensive hiring add-on.</span></span>

## <a name="microsoft-forms-activity"></a><span data-ttu-id="391ff-182">Tegevus Microsoft Forms</span><span class="sxs-lookup"><span data-stu-id="391ff-182">Microsoft Forms activity</span></span>

<span data-ttu-id="391ff-183">Tegevus Microsoft Forms võimaldab värbamisprotsessi manustada Microsoft Formsi vormi.</span><span class="sxs-lookup"><span data-stu-id="391ff-183">The Microsoft Forms activity lets you embed a Microsoft Forms form in your hiring process.</span></span> <span data-ttu-id="391ff-184">Microsoft Forms võimaldab teil luua viktoriine, uuringuid ja küsitlusi.</span><span class="sxs-lookup"><span data-stu-id="391ff-184">Microsoft Forms lets you create quizzes, surveys, and polls.</span></span> <span data-ttu-id="391ff-185">Värbamisprotsessi jaoks tegevuse Microsoft Forms salvestamiseks on vajalik vormi URL.</span><span class="sxs-lookup"><span data-stu-id="391ff-185">To save the Microsoft Forms activity to the hiring process, you must specify of the URL of the form.</span></span> <span data-ttu-id="391ff-186">Nii nagu tegevuste PowerApps, YouTube ja Veebisisu korral, saate lubada ka sellele tegevusele osalejate lisamist.</span><span class="sxs-lookup"><span data-stu-id="391ff-186">As for the PowerApps, YouTube, and Web content activities, you can allow participants to be added to the activity.</span></span> <span data-ttu-id="391ff-187">Kui valite suvandi **Näita ainult kandidaadile**, näidatakse vormi ainult kandidaatidele.</span><span class="sxs-lookup"><span data-stu-id="391ff-187">If you select the **Show only to candidate** option, the form is shown only as part of the candidate experience.</span></span> <span data-ttu-id="391ff-188">Seda ei näidata Attractis olevas värbamisprotsessis.</span><span class="sxs-lookup"><span data-stu-id="391ff-188">It isn't shown in the hiring process in Attract.</span></span>

<span data-ttu-id="391ff-189">Rakendusega Microsoft Forms saavad autorid muuta oma sätteid, et organisatsioonivälised kasutajad saaksid nende küsitlustele või viktoriinile vastata.</span><span class="sxs-lookup"><span data-stu-id="391ff-189">In Microsoft Forms, authors can change their settings to let users outside their organization respond to their survey or quiz.</span></span> <span data-ttu-id="391ff-190">Sel juhul on kasutajate vastused anonüümsed.</span><span class="sxs-lookup"><span data-stu-id="391ff-190">In this case, users submit responses anonymously.</span></span> <span data-ttu-id="391ff-191">Kui soovite näha, kes on teie küsitlusele või viktoriinile vastanud, saate küsitluse või viktoriini osana paluda vastajatel sisestada oma nimi.</span><span class="sxs-lookup"><span data-stu-id="391ff-191">If you want to see who has filled out your survey or quiz, you can require that respondents enter their names as part of the survey or quiz.</span></span>

> [!NOTE]
> <span data-ttu-id="391ff-192">Tegevus Microsoft Forms on saadaval ainult tervikliku värbamise lisandmooduli korral.</span><span class="sxs-lookup"><span data-stu-id="391ff-192">The Microsoft Forms activity is available only with the Comprehensive hiring add-on.</span></span>
