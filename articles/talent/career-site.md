---
title: Rakenduse Attract karjäärisaidi funktsionaalsus
description: See teema annab ülevaate kandidaatidele suunatud karjäärisaidi funktsionaalsusest rakenduses Attract.
author: josaw1
manager: AnnBe
ms.date: 02/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-02-12
ms.dyn365.ops.version: AX 7.1.0, Talent April 2018 update
ms.openlocfilehash: 087ab4034a1e601e7f3514c77d56ef54b0c5c52d
ms.sourcegitcommit: 1ee613a88edddab036d145f27f19d071a4b8ad24
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 02/13/2019
ms.locfileid: "389958"
---
# <a name="career-site-functionality-in-attract"></a><span data-ttu-id="6458a-103">Rakenduse Attract karjäärisaidi funktsionaalsus</span><span class="sxs-lookup"><span data-stu-id="6458a-103">Career site functionality in Attract</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="6458a-104">See teema annab ülevaate kandidaatidele suunatud karjäärisaidi funktsionaalsusest rakenduses Dynamics 365 for Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="6458a-104">This topic provides an overview of the candidate-facing career site functionality in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="6458a-105">Samuti selgitatakse, kuidas seda funktsionaalsust seadistada.</span><span class="sxs-lookup"><span data-stu-id="6458a-105">It also explains how to set up this functionality.</span></span>

<span data-ttu-id="6458a-106">Attract annab rentniku igale keskkonnale ühe karjäärisaidi.</span><span class="sxs-lookup"><span data-stu-id="6458a-106">Attract provides one career site for each environment in a tenant.</span></span> <span data-ttu-id="6458a-107">Näiteks kui organisatsioonil on arenduskeskkond ja katsekeskkond, eraldatakse üks karjäärisait arenduskeskkonnale ja teine karjäärisait katsekeskkonnale.</span><span class="sxs-lookup"><span data-stu-id="6458a-107">For example, if an organization has a development environment and a test environment, one career site is provisioned for the development environment, and another career site is provisioned for the test environment.</span></span> <span data-ttu-id="6458a-108">Iga karjäärisait on täiesti isoleeritud ja oma autentimismehhanismiga.</span><span class="sxs-lookup"><span data-stu-id="6458a-108">Each career site is completely isolated and has its own authentication mechanism.</span></span> <span data-ttu-id="6458a-109">Ühiseid töid ja kandidaatide profiile karjäärisaitidel pole.</span><span class="sxs-lookup"><span data-stu-id="6458a-109">Jobs and candidate profiles aren't shared between career sites.</span></span>

<span data-ttu-id="6458a-110">Vaikimisi on karjäärisaidid avalikud.</span><span class="sxs-lookup"><span data-stu-id="6458a-110">By default, the career site is public.</span></span> <span data-ttu-id="6458a-111">Kandidaadid saavad seetõttu vaadata kõiki väliseks märgitud töökohti ilma sisse logimata.</span><span class="sxs-lookup"><span data-stu-id="6458a-111">Therefore, candidates can view all jobs that are marked as external without having to sign in.</span></span> <span data-ttu-id="6458a-112">Kõigi muude toimingute jaoks aga peavad kandidaadid sisse logima.</span><span class="sxs-lookup"><span data-stu-id="6458a-112">However, all other actions require that candidates sign in.</span></span>

## <a name="career-site-management"></a><span data-ttu-id="6458a-113">Karjäärisaidi haldus</span><span class="sxs-lookup"><span data-stu-id="6458a-113">Career site management</span></span>

<span data-ttu-id="6458a-114">Alljärgnevate üksuste väärtuste määramiseks logige administraatorina rakendusse Attract sisse, valige menüüst **Sätted** (hammasratta kujutis) suvand **Halduskeskus** ja seejärel valige vahekaart **Ettevõtte andmed**.</span><span class="sxs-lookup"><span data-stu-id="6458a-114">To set the values for the following items, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu (the gear symbol), and then select the **Company information** tab.</span></span>

-   <span data-ttu-id="6458a-115">**Organisatsiooni nimi** – organisatsiooni nimi kuvatakse karjäärisaidi ülaosas oleval navigeerimisribal.</span><span class="sxs-lookup"><span data-stu-id="6458a-115">**Organization name** - The organization name appears on the navigation bar at the top of the career site.</span></span> <span data-ttu-id="6458a-116">Organisatsiooni nime valimise korral avaneb kandidaatidele leht, kus on toodud kõik vabad töökohad.</span><span class="sxs-lookup"><span data-stu-id="6458a-116">By selecting the organization name, candidates go to a page that lists all open jobs.</span></span>

-   <span data-ttu-id="6458a-117">**Organisatsiooni logo** – karjäärisaidi ülemises vasakus servas kuvatakse organisatsiooni logo kujutist.</span><span class="sxs-lookup"><span data-stu-id="6458a-117">**Organization logo** - An image of the organization's logo appears in the upper left of the career site.</span></span> <span data-ttu-id="6458a-118">Logo kujutise valimise korral avaneb kandidaatidele leht, kus on toodud kõik vabad töökohad.</span><span class="sxs-lookup"><span data-stu-id="6458a-118">By selecting the logo image, candidates go to a page that lists all open jobs.</span></span>

    >   [!NOTE] 
    >   <span data-ttu-id="6458a-119">Karjäärisaidil kuvatava logo kujutise fikseeritud kõrgus on 20 pikslit (px).</span><span class="sxs-lookup"><span data-stu-id="6458a-119">The logo image that appears on the career site has a fixed height of 20 pixels (px).</span></span> <span data-ttu-id="6458a-120">Halduskeskuse kaudu lisatud pildi suurus muudetakse sobivaks.</span><span class="sxs-lookup"><span data-stu-id="6458a-120">The image that you add in the Admin center is scaled to fit.</span></span> <span data-ttu-id="6458a-121">Olenevalt kujutisest võib laius seetõttu muutuda.</span><span class="sxs-lookup"><span data-stu-id="6458a-121">Therefore, depending on the image, the width might change.</span></span>
 
<span data-ttu-id="6458a-122">Alljärgnevate üksuste väärtuste määramiseks logige administraatorina rakendusse Attract sisse, valige menüüst **Sätted** suvand **Halduskeskus** ja seejärel valige vahekaart **Karjäärisaidi haldus**.</span><span class="sxs-lookup"><span data-stu-id="6458a-122">To set the values for the following items, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu, and then select the **Career site management** tab.</span></span>

-   <span data-ttu-id="6458a-123">**Otsingumootori optimeerimine** – kui see on lubatud, on kõik rakenduse Attract karjäärisaidile sisestatud avalikud töökohad leitavad otsingumootoritega, nagu Bing ja Google.</span><span class="sxs-lookup"><span data-stu-id="6458a-123">**Search Engine Optimization** - When enabled, all public jobs posted to Attract career site will be searchable using search engines like Bing and Google.</span></span>

    >   [!NOTE] 
    >   <span data-ttu-id="6458a-124">Selle sätte sisselülitamise ja otsingutulemite ilmumise vahel võib olla viivitus, mis oleneb kasutatavast otsingumootorist.</span><span class="sxs-lookup"><span data-stu-id="6458a-124">There might be a delay between turning this setting on and search results appearing, depending on the search engine that you are using.</span></span>
         
## <a name="career-site-urls"></a><span data-ttu-id="6458a-125">Karjäärisaidi URL-id</span><span class="sxs-lookup"><span data-stu-id="6458a-125">Career site URLs</span></span>

<span data-ttu-id="6458a-126">Alljärgnev loend sisaldab tavaliselt kasutatavaid karjäärisaitide URL-e ja teavet, kuidas neile juurde pääsed.</span><span class="sxs-lookup"><span data-stu-id="6458a-126">The following list contains the commonly used career site URLs and how to access them.</span></span>

-   <span data-ttu-id="6458a-127">**Karjäärisaidi avalehe URL** – karjäärisaidi avalehe URL-i vaatamiseks logige rakendusse Attract sisse administraatorina, valige menüüst **Sätted** suvand **Halduskeskus** ja seejärel valige vahekaart **Karjäärisaidi haldus**.</span><span class="sxs-lookup"><span data-stu-id="6458a-127">**Career site home page URL** - To view the career site home page URL, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu, and then select the **Career site management** tab.</span></span>

-   <span data-ttu-id="6458a-128">**Üksiku töökuulutuse kandideerimise URL** – kui [sisestate välise töökoha](Creating-jobs-Attract.md#postings) esmakordselt, võite rakendusest Attract kopeerida lingi **Kandideeri**.</span><span class="sxs-lookup"><span data-stu-id="6458a-128">**Individual job post apply URL** - When you [post an external job](Creating-jobs-Attract.md#postings) for the first time, you can copy the **Apply** link from the Attract application.</span></span> <span data-ttu-id="6458a-129">Selle lingi URL on järgmises vormingus: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)</span><span class="sxs-lookup"><span data-stu-id="6458a-129">The URL for this link will be in the following format: [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>/apply](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e/apply)</span></span>

-   <span data-ttu-id="6458a-130">**Üksiku töökuulutuse URL** – töökuulutusee URL on kandideerimise URL-i alamstring.</span><span class="sxs-lookup"><span data-stu-id="6458a-130">**Individual job post URL** - The URL of the job post is a substring of the Apply URL.</span></span> <span data-ttu-id="6458a-131">See sisaldab kõike kuni töökoha numbrini.</span><span class="sxs-lookup"><span data-stu-id="6458a-131">It consists of everything up through the job number.</span></span> <span data-ttu-id="6458a-132">Seetõttu on eelneva kandideerimise URL-i töökuulutuse URL [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e)</span><span class="sxs-lookup"><span data-stu-id="6458a-132">Therefore, for the preceding Apply URL, the job post URL is [https://jobs.talent.dynamics.com/jobs/\<company_name\>/\<environment_number\>/\<job_number\>](https://jobs.talent.dynamics.com/jobs/%3ccompany_name%3e/%3cenvironment_number%3e/%3cjob_number%3e)</span></span>

## <a name="authentication-options"></a><span data-ttu-id="6458a-133">Autentimisvõimalused</span><span class="sxs-lookup"><span data-stu-id="6458a-133">Authentication options</span></span>

<span data-ttu-id="6458a-134">Kandidaatidel on rakenduse Attract karjäärisaidile sisselogimiseks järgmised võimalused:</span><span class="sxs-lookup"><span data-stu-id="6458a-134">Candidates have the following sign-in options for an Attract career site:</span></span>

-   <span data-ttu-id="6458a-135">isiklik konto:</span><span class="sxs-lookup"><span data-stu-id="6458a-135">Personal account:</span></span>

    -   <span data-ttu-id="6458a-136">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="6458a-136">LinkedIn</span></span>

    -   <span data-ttu-id="6458a-137">Microsoft</span><span class="sxs-lookup"><span data-stu-id="6458a-137">Microsoft</span></span>

    -   <span data-ttu-id="6458a-138">Google</span><span class="sxs-lookup"><span data-stu-id="6458a-138">Google</span></span>

    -   <span data-ttu-id="6458a-139">Facebook</span><span class="sxs-lookup"><span data-stu-id="6458a-139">Facebook</span></span>

-   <span data-ttu-id="6458a-140">töö- või koolikonto:</span><span class="sxs-lookup"><span data-stu-id="6458a-140">Work or school account:</span></span>

    -   <span data-ttu-id="6458a-141">Microsoft Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="6458a-141">Microsoft Azure Active Directory (Azure AD)</span></span>

<span data-ttu-id="6458a-142">Azure AD-ga sisselogimine on mõeldud ainult sisekandidaatidele.</span><span class="sxs-lookup"><span data-stu-id="6458a-142">Azure AD sign-in is intended only for internal candidates.</span></span> <span data-ttu-id="6458a-143">Seetõttu toimib see ainult sisekandidaatidega, kes kasutavad oma ettevõtte Azure AD identimisteavet.</span><span class="sxs-lookup"><span data-stu-id="6458a-143">Therefore, it works only for internal candidates who use their company Azure AD credentials.</span></span> <span data-ttu-id="6458a-144">Näiteks kandidaat, kes on hetkel ettevõtte Contoso Ltd töötaja, soovib kandideerida sellega mitteseotud ettevõtte Alpine Ski House töökohale.</span><span class="sxs-lookup"><span data-stu-id="6458a-144">For example, a candidate who is currently an employee of Contoso Ltd wants to apply for a job in an unrelated company, Alpine Ski House.</span></span> <span data-ttu-id="6458a-145">Sellisel juhul sisselogimine ei õnnestu, kui töövõtja üritab kasutada ettevõtte Contoso Ltd Azure AD identimisteavet.</span><span class="sxs-lookup"><span data-stu-id="6458a-145">In this case, the sign-in will be unsuccessful if the employee tries to use Azure AD credentials from Contoso Ltd.</span></span>

## <a name="create-and-maintain-a-profile"></a><span data-ttu-id="6458a-146">Profiili loomine ja haldamine</span><span class="sxs-lookup"><span data-stu-id="6458a-146">Create and maintain a profile</span></span>

<span data-ttu-id="6458a-147">Pärast karjäärisaidile sisselogimist saavad kandidaadid lehe ülaosas olevalt navigeerimisribalt oma profiili loomiseks ja haldamiseks kasutada valikut **Minu profiil**.</span><span class="sxs-lookup"><span data-stu-id="6458a-147">After candidates sign in to the career site, they can select **My profile** on the navigation bar at the top of the page to create and maintain their profile.</span></span>
<span data-ttu-id="6458a-148">Profiil sisaldab isikuandmeid, andmeid töökogemuse kohta, haridusandmeid, dokumente, linke ja andmeid oskuste kohta.</span><span class="sxs-lookup"><span data-stu-id="6458a-148">The profile includes personal information, information about work experience, education details, documents, links, and information about skill sets.</span></span> <span data-ttu-id="6458a-149">Pärast profiili loomist saab seda kasutada kandidaadile huvi pakkuvatele töökohtadele kandideerimiseks.</span><span class="sxs-lookup"><span data-stu-id="6458a-149">After a profile is created, it can be used to apply for jobs that the candidate is interested in.</span></span> <span data-ttu-id="6458a-150">Samuti aitavad profiilid rakendusel Attract kandidaatidele õigeid töökohti soovitada.</span><span class="sxs-lookup"><span data-stu-id="6458a-150">Profiles also help Attract recommend the right jobs to candidates.</span></span>

>   [!NOTE]
>   <span data-ttu-id="6458a-151">Kui kandidaat kasutab ühe ülevalpool nimetatud autentimisteenuse pakkuja abil sisselogimiseks meili ID-d, määratakse see meili ID vaikimisi profiiliga seotud kontaktmeili ID-ks.</span><span class="sxs-lookup"><span data-stu-id="6458a-151">If a candidate uses an email ID to sign in using one of the authentication providers listed above, that email ID will default to the contact email ID associated with the profile.</span></span> <span data-ttu-id="6458a-152">Viimast saab aga igal ajal muuta ja see on esimesest täiesti sõltumatu.</span><span class="sxs-lookup"><span data-stu-id="6458a-152">However, the latter can be changed at any time and is completely independent of the former.</span></span> <span data-ttu-id="6458a-153">Attract kasutab kogu meilisuhtluse jaoks alati kontaktmeili ID sidumist teie profiiliga.</span><span class="sxs-lookup"><span data-stu-id="6458a-153">Attract will always use the contact email ID to associate with your profile for all email communications.</span></span>

## <a name="find-the-right-job"></a><span data-ttu-id="6458a-154">Õige töökoha leidmine</span><span class="sxs-lookup"><span data-stu-id="6458a-154">Find the right job</span></span>

<span data-ttu-id="6458a-155">Töökohtade loendi lehel saavad kandidaadid otsingusõnu sisestades otsida kindlat töökohta.</span><span class="sxs-lookup"><span data-stu-id="6458a-155">On the job list page, candidates can search for a specific job by entering search terms.</span></span> <span data-ttu-id="6458a-156">Otsingufunktsioon otsib otsingusõnu ametinimetustest ja töökirjeldustest ning kuvab asjakohased töökohad tulemitena.</span><span class="sxs-lookup"><span data-stu-id="6458a-156">The search functionality looks for the search terms in job titles and job descriptions, and shows relevant jobs as results.</span></span> <span data-ttu-id="6458a-157">Kandidaadid saavad tulemusi igal ajal töökoha asukoha või tööfunktsiooni alusel filtreerida.</span><span class="sxs-lookup"><span data-stu-id="6458a-157">Candidates can filter the results at any time, based on the job location or job function.</span></span>

<span data-ttu-id="6458a-158">Samuti saavad kandidaadid karjäärisaidil vaadata soovitatud töökohti.</span><span class="sxs-lookup"><span data-stu-id="6458a-158">Candidates can also view a set of recommended jobs on the career site.</span></span> <span data-ttu-id="6458a-159">Kandidaatidele soovitatavad töökohad põhinevad kandidaadi varasematel kandideerimistel, profiilil ja elulookirjeldustel.</span><span class="sxs-lookup"><span data-stu-id="6458a-159">The jobs that are recommended to a candidate are based on the candidate's past applications, profile, and resumes.</span></span>

>   [!NOTE] 
>   <span data-ttu-id="6458a-160">Soovitatavad töökohad kuvatakse ainult siis, kui karjäärisaidile on sisestatud vähemalt 10 töökohta ja kandidaat on täitnud oma profiili lõpuni.</span><span class="sxs-lookup"><span data-stu-id="6458a-160">Job recommendations are shown only if at least 10 jobs are posted on the career site, and if the candidate has completed a profile.</span></span>

## <a name="apply-for-jobs"></a><span data-ttu-id="6458a-161">Töökohtadele kandideerimine</span><span class="sxs-lookup"><span data-stu-id="6458a-161">Apply for jobs</span></span>

<span data-ttu-id="6458a-162">Kui kandidaat leiab õige töökoha, saab ta kandideerida lehe **Töö üksikasjad** nupu **Kandideeri** abil.</span><span class="sxs-lookup"><span data-stu-id="6458a-162">After candidates find the right job, they can apply by using the **Apply** button on the **Job details** page.</span></span> <span data-ttu-id="6458a-163">Sellel hetkel saavad kandidaadid luua kas uue profiili või vaadata üle oma olemasoleva profiili andmed.</span><span class="sxs-lookup"><span data-stu-id="6458a-163">At this point, candidates can either create a new profile or review the information in their existing profile.</span></span>
<span data-ttu-id="6458a-164">Samuti saavad kandidaadid vajaduse korral üles laadida elulookirjelduse ja seejärel esitada avalduse töökohale kandideerimiseks.</span><span class="sxs-lookup"><span data-stu-id="6458a-164">Candidates can also upload a resume, as required, and then submit the job application.</span></span>

## <a name="check-application-status"></a><span data-ttu-id="6458a-165">Avalduse oleku kontrollimine</span><span class="sxs-lookup"><span data-stu-id="6458a-165">Check application status</span></span>

<span data-ttu-id="6458a-166">Pärast ühele või mitmele töökohale kandideerimist saavad kandidaadid oma avatud ja suletud avaldusi vaadata lehe ülaosas oleva navigeerimisriba valiku **Avaldused** kaudu.</span><span class="sxs-lookup"><span data-stu-id="6458a-166">After candidates apply for one or more jobs, they can select **Applications** on the navigation bar at the top of the page to view their open and closed applications.</span></span> <span data-ttu-id="6458a-167">Kui kandidaadid avavad ühe oma avaldustest, näevad nad hetkeseisu ja mistahes ootel olevat tegevust, mille nad peavad teostama.</span><span class="sxs-lookup"><span data-stu-id="6458a-167">When candidates open one of their applications, they see the current stage and any pending action items that they must complete.</span></span> <span data-ttu-id="6458a-168">Näiteks, kui kandidaat peab välja pakkuma võimalikud kuupäevad silmast silma vestluseks, kuvatakse lehel võimaliku valikud.</span><span class="sxs-lookup"><span data-stu-id="6458a-168">For example, if a candidate must provide potential dates for an in-person interview, the page shows the available options.</span></span>

## <a name="internal-jobs"></a><span data-ttu-id="6458a-169">Organisatsioonisisesed töökohad</span><span class="sxs-lookup"><span data-stu-id="6458a-169">Internal jobs</span></span>

<span data-ttu-id="6458a-170">Hetkel ei kuvata karjäärisaidil organisatsioonisiseseks märgitud ja rakenduse Attract karjäärisaidile sisestatud töökohti.</span><span class="sxs-lookup"><span data-stu-id="6458a-170">Currently, jobs that are marked as internal and posted to the Attract career site don't appear on the career site.</span></span> <span data-ttu-id="6458a-171">Need on juurdepääsetavad ainult otsese URL-i **Kandideeri** kaudu, mida saab kopeerida rakendusest Attract.</span><span class="sxs-lookup"><span data-stu-id="6458a-171">They are only accessible using the direct **Apply** URL that can be copied from the Attract application.</span></span>
