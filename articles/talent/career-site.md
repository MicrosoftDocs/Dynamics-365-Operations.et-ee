---
title: "Karjäärisaidi funktsionaalsus Attractis"
description: "Selles artiklis antakse ülevaade kandidaatide leidmise karjäärisaidi funktsionaalsusest rakenduses Microsoft Dynamics 365 for Talent - Attract. See selgitab ka seda, kuidas seda funktsionaalsust seadistada."
author: josaw
manager: AnnBe
ms.date: 10/18/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Talent
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: e890e32049e930b70c2d0aac8aa8206ab999418a
ms.openlocfilehash: 452e3e92ea32ab5f1e3720ab81ff2f7ea18b2a06
ms.contentlocale: et-ee
ms.lasthandoff: 10/22/2018

---
# <a name="career-site-functionality-in-attract"></a><span data-ttu-id="64912-104">Karjäärisaidi funktsionaalsus Attractis</span><span class="sxs-lookup"><span data-stu-id="64912-104">Career site functionality in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="64912-105">Selles artiklis antakse ülevaade kandidaatide leidmise karjäärisaidi funktsionaalsusest rakenduses Microsoft Dynamics 365 for Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="64912-105">This article provides an overview of the candidate-facing career site functionality in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="64912-106">See selgitab ka seda, kuidas seda funktsionaalsust seadistada.</span><span class="sxs-lookup"><span data-stu-id="64912-106">It also explains how to set up this functionality.</span></span>

## <a name="overview"></a><span data-ttu-id="64912-107">Ülevaade</span><span class="sxs-lookup"><span data-stu-id="64912-107">Overview</span></span>

<span data-ttu-id="64912-108">Attract annab rentniku igale keskkonnale ühe karjäärisaidi.</span><span class="sxs-lookup"><span data-stu-id="64912-108">Attract provides one career site for each environment in a tenant.</span></span> <span data-ttu-id="64912-109">Näiteks kui organisatsioonil on arenduskeskkond ja katsekeskkond, eraldatakse üks karjäärisait arenduskeskkonnale ja teine karjäärisait eraldatakse katsekeskkonnale.</span><span class="sxs-lookup"><span data-stu-id="64912-109">For example, if an organization has a development environment and a test environment, one career site is provisioned for the development environment, and another career site is provisioned for the test environment.</span></span> <span data-ttu-id="64912-110">Iga karjäärisait on **täiesti isoleeritud** ja omab eraldi autentimise mehhanismi.</span><span class="sxs-lookup"><span data-stu-id="64912-110">Each career site is **completely isolated** and has its own authentication mechanism.</span></span> <span data-ttu-id="64912-111">Töid ja kandidaatide profiile karjäärisaitide vahel ei jagata.</span><span class="sxs-lookup"><span data-stu-id="64912-111">Jobs and candidate profiles aren't shared between career sites.</span></span>

<span data-ttu-id="64912-112">Vaikimisi on karjäärisait avalik.</span><span class="sxs-lookup"><span data-stu-id="64912-112">By default, the career site is public.</span></span> <span data-ttu-id="64912-113">Seega saavad kandidaadid näha kõiki väliseks märgitud töid ilma sisse logimata.</span><span class="sxs-lookup"><span data-stu-id="64912-113">Therefore, candidates can view all jobs that are marked as external without having to sign in.</span></span> <span data-ttu-id="64912-114">Siiski, kõik muud toimingud nõuavad kandidaadilt sisselogimist.</span><span class="sxs-lookup"><span data-stu-id="64912-114">However, all other actions require that candidates sign in.</span></span>

## <a name="career-site-management"></a><span data-ttu-id="64912-115">Karjäärisaidi haldus</span><span class="sxs-lookup"><span data-stu-id="64912-115">Career site management</span></span>

<span data-ttu-id="64912-116">Järgmisi karjäärisaidi elemente juhitakse sätete abil.</span><span class="sxs-lookup"><span data-stu-id="64912-116">The following items on the career site are controlled by settings:</span></span>

- <span data-ttu-id="64912-117">**Organisatsiooni nimi:** organisatsiooni nimi kuvatakse karjäärisaidi ülaosas navigeerimisribal.</span><span class="sxs-lookup"><span data-stu-id="64912-117">**Organization name:** The organization name appears on the navigation bar at the top of the career site.</span></span> <span data-ttu-id="64912-118">Valides organisatsiooni nime, lähevad kandidaadid lehele, kus on loetletud kõik avatud tööd.</span><span class="sxs-lookup"><span data-stu-id="64912-118">By selecting the organization name, candidates go to a page that lists all open jobs.</span></span>
- <span data-ttu-id="64912-119">**Organisatsiooni logo:** karjäärisaidi ülemises vasakus servas kuvatakse organisatsiooni logo kujutist.</span><span class="sxs-lookup"><span data-stu-id="64912-119">**Organization logo:** An image of the organization's logo appears in the upper left of the career site.</span></span> <span data-ttu-id="64912-120">Valides logo kujutise, lähevad kandidaadid lehele, kus on loetletud kõik avatud tööd.</span><span class="sxs-lookup"><span data-stu-id="64912-120">By selecting the logo image, candidates go to a page that lists all open jobs.</span></span>

<span data-ttu-id="64912-121">Organisatsiooni nime ja logo väärtuste seadistamiseks logige administraatorina Attracti sisse, valige menüü **Sätted** (hammasratta sümbol) alt **Halduskeskus** ja seejärel valige vahekaart **Ettevõtte andmed**.</span><span class="sxs-lookup"><span data-stu-id="64912-121">To set the values for the organization name and logo, sign in to Attract as an administrator, select **Admin center** on the **Settings** menu (the gear symbol), and then select the **Company information** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="64912-122">Karjäärisaidil näidatava logo kujutise fikseeritud kõrgus on 20 pikslit (px).</span><span class="sxs-lookup"><span data-stu-id="64912-122">The logo image that appears on the career site has a fixed height of 20 pixels (px).</span></span> <span data-ttu-id="64912-123">Halduskeskusest lisatud pildi suurus muudetakse sobivaks.</span><span class="sxs-lookup"><span data-stu-id="64912-123">The image that you add in the Admin center is scaled to fit.</span></span> <span data-ttu-id="64912-124">Seetõttu võib laius sõltuvalt pildist muutuda.</span><span class="sxs-lookup"><span data-stu-id="64912-124">Therefore, depending on the image, the width might change.</span></span>

## <a name="career-site-url"></a><span data-ttu-id="64912-125">Karjäärisaidi URL</span><span class="sxs-lookup"><span data-stu-id="64912-125">Career site URL</span></span>

<span data-ttu-id="64912-126">Kui te esmakordselt [sisestate välise töö](./Creating-jobs-Attract.md#postings), võite **Rakenda** lingi Attracti rakendusest kopeerida.</span><span class="sxs-lookup"><span data-stu-id="64912-126">When you [post an external job](./Creating-jobs-Attract.md#postings) for the first time, you can copy the **Apply** link from the Attract application.</span></span> <span data-ttu-id="64912-127">Selle lingi URL on järgmises vormingus: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`</span><span class="sxs-lookup"><span data-stu-id="64912-127">The URL for this link will be in the following format: `https://jobs.talent.dynamics.com/jobs/<company_name>/<environment_number>/<job_number>/apply`</span></span>

<span data-ttu-id="64912-128">Karjäärisaidi URL on URL-i **Rakenda** alamstring.</span><span class="sxs-lookup"><span data-stu-id="64912-128">The URL of the career site is a substring of the **Apply** URL.</span></span> <span data-ttu-id="64912-129">See sisaldab kõike, kuni ettevõtte nimeni.</span><span class="sxs-lookup"><span data-stu-id="64912-129">It consists of everything up through the company name.</span></span> <span data-ttu-id="64912-130">Seepärast on eelnevale **Rakenda** URL-ile karjäärisaidi URL `https://jobs.talent.dynamics.com/jobs/<company_name>/`.</span><span class="sxs-lookup"><span data-stu-id="64912-130">Therefore, for the preceding **Apply** URL, the career site URL is `https://jobs.talent.dynamics.com/jobs/<company_name>/`.</span></span>

## <a name="authentication-options"></a><span data-ttu-id="64912-131">Autentimise valikud</span><span class="sxs-lookup"><span data-stu-id="64912-131">Authentication options</span></span>

<span data-ttu-id="64912-132">Kandidaatidel on Attracti karjäärisaidile sisselogimiseks järgmised võimalused.</span><span class="sxs-lookup"><span data-stu-id="64912-132">Candidates have the following sign-in options for an Attract career site:</span></span>

- <span data-ttu-id="64912-133">Isiklik konto:</span><span class="sxs-lookup"><span data-stu-id="64912-133">Personal account:</span></span>

    - <span data-ttu-id="64912-134">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="64912-134">LinkedIn</span></span>
    - <span data-ttu-id="64912-135">Microsoft – WHS</span><span class="sxs-lookup"><span data-stu-id="64912-135">Microsoft</span></span>
    - <span data-ttu-id="64912-136">Google</span><span class="sxs-lookup"><span data-stu-id="64912-136">Google</span></span>
    - <span data-ttu-id="64912-137">Facebook</span><span class="sxs-lookup"><span data-stu-id="64912-137">Facebook</span></span>

- <span data-ttu-id="64912-138">Töö- või koolikonto:</span><span class="sxs-lookup"><span data-stu-id="64912-138">Work or school account:</span></span>

    - <span data-ttu-id="64912-139">Windows Azure Active Directory (Azure AD)</span><span class="sxs-lookup"><span data-stu-id="64912-139">Microsoft Azure Active Directory (Azure AD)</span></span>

<span data-ttu-id="64912-140">Azure AD sisselogimine on mõeldud ainult sisemistele kandidaatidele.</span><span class="sxs-lookup"><span data-stu-id="64912-140">Azure AD sign-in is intended only for internal candidates.</span></span> <span data-ttu-id="64912-141">Seetõttu toimib see ainult sisemistele kandidaatidele, kes kasutavad oma ettevõtte Azure AD mandaate.</span><span class="sxs-lookup"><span data-stu-id="64912-141">Therefore, it works only for internal candidates who use their company Azure AD credentials.</span></span> <span data-ttu-id="64912-142">Näiteks kandidaat, kes on hetkel Contoso Ltd töötaja, soovib kandideerida kõrvalise ettevõtte, Alpine Ski House, tööle.</span><span class="sxs-lookup"><span data-stu-id="64912-142">For example, a candidate who is currently an employee of Contoso Ltd wants to apply for a job in an unrelated company, Alpine Ski House.</span></span> <span data-ttu-id="64912-143">Sellisel juhul sisselogimine ebaõnnestub, kui töötaja proovige kasutada oma Contoso Ltd. Azure AD mandaate.</span><span class="sxs-lookup"><span data-stu-id="64912-143">In this case, the sign-in will be unsuccessful if the employee tries to use his or her Azure AD credentials from Contoso Ltd.</span></span>

## <a name="create-and-maintain-a-profile"></a><span data-ttu-id="64912-144">Profiili loomine ja haldamine</span><span class="sxs-lookup"><span data-stu-id="64912-144">Create and maintain a profile</span></span>

<span data-ttu-id="64912-145">Pärast kandidaatide karjäärisaidile sisselogimist saavad nad lehe ülaosast navigeerimisribalt valida **Minu profiil**, et omale profiil luua ja seda hallata.</span><span class="sxs-lookup"><span data-stu-id="64912-145">After candidates sign in to the career site, they can select **My profile** on the navigation bar at the top of the page to create and maintain their profile.</span></span> <span data-ttu-id="64912-146">Profiil sisaldab isikuandmeid, töökogemuse andmeid, hariduse üksikasju, dokumente, linke ja andmeid oskuste kohta.</span><span class="sxs-lookup"><span data-stu-id="64912-146">The profile includes personal information, information about work experience, education details, documents, links, and information about skill sets.</span></span> <span data-ttu-id="64912-147">Pärast profiili loomist saab seda kasutada kandidaadile huvi pakkuvatele töödele kandideerimiseks.</span><span class="sxs-lookup"><span data-stu-id="64912-147">After a profile is created, it can be used to apply for jobs that the candidate is interested in.</span></span> <span data-ttu-id="64912-148">Profiilid aitavad ka Attractil kandidaatidele õigeid töid soovitada.</span><span class="sxs-lookup"><span data-stu-id="64912-148">Profiles also help Attract recommend the right jobs to candidates.</span></span>

## <a name="find-the-right-job"></a><span data-ttu-id="64912-149">Õige töö leidmine</span><span class="sxs-lookup"><span data-stu-id="64912-149">Find the right job</span></span>

<span data-ttu-id="64912-150">Tööde loendi lehel saavad kandidaadid konkreetset tööd otsida sisestades otsingusõnu.</span><span class="sxs-lookup"><span data-stu-id="64912-150">On the job list page, candidates can search for a specific job by entering search terms.</span></span> <span data-ttu-id="64912-151">Otsingu funktsionaalsus otsib otsingusõnu töö pealkirjadest ja töö kirjeldustest ning näitab tulemusena vastavaid töid.</span><span class="sxs-lookup"><span data-stu-id="64912-151">The search functionality looks for the search terms in job titles and job descriptions, and shows relevant jobs as results.</span></span> <span data-ttu-id="64912-152">Kandidaadid saavad tulemusi igal ajal vastavalt töö asukohale või töö funktsioonile filtreerida.</span><span class="sxs-lookup"><span data-stu-id="64912-152">Candidates can filter the results at any time, based on the job location or job function.</span></span>

<span data-ttu-id="64912-153">Kandidaadid saavad karjäärisaidil vaadata ka soovitatud töid.</span><span class="sxs-lookup"><span data-stu-id="64912-153">Candidates can also view a set of recommended jobs on the career site.</span></span> <span data-ttu-id="64912-154">Kandidaatidele soovitatud tööd põhinevad kandidaadi varasematel kandideerimistel, profiilil ja elulookirjeldusel.</span><span class="sxs-lookup"><span data-stu-id="64912-154">The jobs that are recommended to a candidate are based on the candidate's past applications, profile, and resumes.</span></span>

> [!NOTE]
> <span data-ttu-id="64912-155">Töö soovitused kuvatakse ainult siis, kui karjäärisaidile on postitatud vähemalt 10 tööd ja kui kandidaat on täitnud oma profiili.</span><span class="sxs-lookup"><span data-stu-id="64912-155">Job recommendations are shown only if at least 10 jobs are posted on the career site, and if the candidate has completed his or her profile.</span></span>

## <a name="apply-for-jobs"></a><span data-ttu-id="64912-156">Töökohtadele kandideerimine</span><span class="sxs-lookup"><span data-stu-id="64912-156">Apply for jobs</span></span>

<span data-ttu-id="64912-157">Kui kandidaadid leiavad õige töö, saavad nad kandideerida, kasutades töö üksikasjade lehel olevat nuppu **Esita avaldus**.</span><span class="sxs-lookup"><span data-stu-id="64912-157">After candidates find the right job, they can apply by using the **Apply** button on the job details page.</span></span> <span data-ttu-id="64912-158">Sellel hetkel saavad kandidaadid luua kas täiesti uue profiili või vaadata üle oma olemasoleva profiili andmed.</span><span class="sxs-lookup"><span data-stu-id="64912-158">At this point, candidates can either create a brand-new profile or review the information in their existing profile.</span></span> <span data-ttu-id="64912-159">Kui see on nõutud, saavad kandidaadid üles laadida oma elulookirjelduse ja seejärel tööavalduse esitada.</span><span class="sxs-lookup"><span data-stu-id="64912-159">Candidates can also upload a resume, as required, and then submit the job application.</span></span>

## <a name="check-application-status"></a><span data-ttu-id="64912-160">Avalduse oleku kontrollimine</span><span class="sxs-lookup"><span data-stu-id="64912-160">Check application status</span></span>

<span data-ttu-id="64912-161">Kui kandidaadid kandideerivad ühele või enamale tööle, saavad nad oma avatud ja suletud kandideerimiste vaatamiseks valida lehe ülaservas olevalt navigeerimisribalt **Avaldused**.</span><span class="sxs-lookup"><span data-stu-id="64912-161">After candidates apply for one or more jobs, they can select **Applications** on the navigation bar at the top of the page to view their open and closed applications.</span></span> <span data-ttu-id="64912-162">Kui kandidaadid ühe oma avaldustest avavad, näevad nad hetkeseisu ja mistahes ootel olevat tegevust, mille nad peavad teostama.</span><span class="sxs-lookup"><span data-stu-id="64912-162">When candidates open one of their applications, they see the current stage and any pending action items that they must complete.</span></span> <span data-ttu-id="64912-163">Näiteks, kui kandidaat peab välja pakkuma võimalikud kuupäevad silmast silma vestluseks, kuvatakse lehel tema valikuid.</span><span class="sxs-lookup"><span data-stu-id="64912-163">For example, if a candidate must provide potential dates for an in-person interview, the page shows his or her options.</span></span>

## <a name="internal-jobs"></a><span data-ttu-id="64912-164">Sisemised tööd</span><span class="sxs-lookup"><span data-stu-id="64912-164">Internal jobs</span></span>

<span data-ttu-id="64912-165">Hetkel ei kuvata sisemiseks märgitud ja Attracti karjäärisaidile sisestatud töid karjäärisaidil.</span><span class="sxs-lookup"><span data-stu-id="64912-165">Currently, jobs that are marked as internal and posted to the Attract career site don't appear on the career site.</span></span> <span data-ttu-id="64912-166">Need on juurdepääsetavad ainult läbi otsese URL-i **Esita avaldus**, mille saab kopeerida Attracti rakendusest.</span><span class="sxs-lookup"><span data-stu-id="64912-166">They are accessible only via the direct **Apply** URL that can be copied from the Attract application.</span></span>

