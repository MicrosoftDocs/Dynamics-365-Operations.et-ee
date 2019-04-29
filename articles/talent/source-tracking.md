---
title: Kandidaadi profiilide ja avalduste allikate jälgimine
description: Selles teemas antakse teavet kandidaatide profiilide ja avalduste allikate jälgimise kohta.
author: hachandr
manager: AnnBe
ms.date: 03/18/2019
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
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: ebc82ada31d2803800358cd9aecfe389ada8f0dc
ms.sourcegitcommit: dd1e1636d351a15f9c1b6808bea359417a9bd690
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 03/25/2019
ms.locfileid: "897456"
---
# <a name="track-sources-for-candidate-profiles-and-applications"></a><span data-ttu-id="10310-103">Kandidaadi profiilide ja avalduste allikate jälgimine</span><span class="sxs-lookup"><span data-stu-id="10310-103">Track sources for candidate profiles and applications</span></span> 

[!include[banner](../includes/banner.md)]

> [!NOTE] 
> <span data-ttu-id="10310-104">Selles teemas märgitud funktsioonid on saadaval eelväljaandes.</span><span class="sxs-lookup"><span data-stu-id="10310-104">Functionality noted in this topic is available as part of a preview review release.</span></span> <span data-ttu-id="10310-105">Sisu ja funktsioonid võivad muutuda.</span><span class="sxs-lookup"><span data-stu-id="10310-105">The content and the functionality are subject to change.</span></span> <span data-ttu-id="10310-106">Selle funktsiooni kasutamiseks paluge administraatoril see lubada, kasutades Attractis **administraatori sätteid**.</span><span class="sxs-lookup"><span data-stu-id="10310-106">To use this feature, ask an administrator to enable it using the **Admin settings** in Attract.</span></span> <span data-ttu-id="10310-107">Tulevases väljaandes pakutakse allika jälgimise aruandeid.</span><span class="sxs-lookup"><span data-stu-id="10310-107">A future release will provide source tracking reports.</span></span> <span data-ttu-id="10310-108">Lisateavet leiate teemast [Juurdepääs eelvaatefunktsioonidele rakenduses Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/access-preview-feature).</span><span class="sxs-lookup"><span data-stu-id="10310-108">For more information, see [Access preview features in Talent](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/access-preview-feature).</span></span>

<span data-ttu-id="10310-109">Kui kandidaadid töökohale kandideerivad, jälgib rakendus Attract automaatselt nende avalduste allikat, pakkudes teile väärtuslikku abiteavet värbamisprotsessi jaoks.</span><span class="sxs-lookup"><span data-stu-id="10310-109">When candidates apply for a job, Attract automatically tracks the source of their applications, providing you with valuable information to help you target your recruiting efforts.</span></span> <span data-ttu-id="10310-110">Värbajad ja personalijuhid võivad kandidaadi käsitsi tööle või talendikausta lisamisel valida ka avalduse allika.</span><span class="sxs-lookup"><span data-stu-id="10310-110">Recruiters and hiring managers can also select an application source while manually adding a candidate to a job or talent pool.</span></span>

<span data-ttu-id="10310-111">Saate vaadata avalduse allikat vahekaardil **Tegevus** avalduste tegevuse üksikasjade alt ja vahekaardi **Profiil** talendikaustades olevas avalduste ajaloos.</span><span class="sxs-lookup"><span data-stu-id="10310-111">You can view the application source in the application activity details under the **Activity** tab, as well as in the application history available under **Profile** in talent pools.</span></span> <span data-ttu-id="10310-112">Kandidaadi profiili võite leida vahekaardi **Profiil** avaldustes ja talendikaustades olevates kandidaatide üksikasjades.</span><span class="sxs-lookup"><span data-stu-id="10310-112">You can find a candidate's profile source in the candidate details under the **Profile** tab in both applications and talent pools.</span></span>

> [!NOTE] 
> <span data-ttu-id="10310-113">Protsessimallid leiate [tervikliku värbamise lisandmoodulist](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span><span class="sxs-lookup"><span data-stu-id="10310-113">You can find process templates in the [Comprehensive hiring add-on](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/attract-comprehensive-hiring).</span></span>

## <a name="pre-configured-sources"></a><span data-ttu-id="10310-114">Eelkonfigureeritud allikad</span><span class="sxs-lookup"><span data-stu-id="10310-114">Pre-configured sources</span></span>

<span data-ttu-id="10310-115">Vaikallikate loend sisaldab tavapäraseid avalduste allikaid.</span><span class="sxs-lookup"><span data-stu-id="10310-115">The default source list contains common application sources.</span></span> <span data-ttu-id="10310-116">Mõnel allika tüübil, näiteks **Tööportaal** ja **Suhtlusvõrk**, on täiendavad allika üksikasjad.</span><span class="sxs-lookup"><span data-stu-id="10310-116">Some source types, like **Job board** and **Social Network**, have additional source details.</span></span> <span data-ttu-id="10310-117">Näiteks kuuluvad allika tüübi **Suhtlusvõrk** alla Facebook ja Twitter.</span><span class="sxs-lookup"><span data-stu-id="10310-117">For example, **Social Network** includes Facebook and Twitter.</span></span> <span data-ttu-id="10310-118">Allika tüüp **Viitamine** võimaldab teil viitajaks määrata ettevõttesisese töötaja.</span><span class="sxs-lookup"><span data-stu-id="10310-118">The **Referral** source type allows you to specify an internal employee as the referrer.</span></span> <span data-ttu-id="10310-119">Vaikeallikate loendisse kuuluvad järgmised eelkonfigureeritud allikad.</span><span class="sxs-lookup"><span data-stu-id="10310-119">The default source list includes the following pre-configured sources:</span></span>

-   <span data-ttu-id="10310-120">Attracti karjäärisait</span><span class="sxs-lookup"><span data-stu-id="10310-120">Attract career site</span></span>

-   <span data-ttu-id="10310-121">Tööbüroo</span><span class="sxs-lookup"><span data-stu-id="10310-121">Agency</span></span>

-   <span data-ttu-id="10310-122">Karjäärimess</span><span class="sxs-lookup"><span data-stu-id="10310-122">Career Fair</span></span>

-   <span data-ttu-id="10310-123">Ettevõtte turundus</span><span class="sxs-lookup"><span data-stu-id="10310-123">Company Marketing</span></span>

-   <span data-ttu-id="10310-124">Konverentsid ja ärimessid</span><span class="sxs-lookup"><span data-stu-id="10310-124">Conferences & Trade shows</span></span>

-   <span data-ttu-id="10310-125">Kutseliit</span><span class="sxs-lookup"><span data-stu-id="10310-125">Professional Association</span></span>

-   <span data-ttu-id="10310-126">Tööportaal</span><span class="sxs-lookup"><span data-stu-id="10310-126">Job board</span></span>

    -   <span data-ttu-id="10310-127">Indeed</span><span class="sxs-lookup"><span data-stu-id="10310-127">Indeed</span></span>

    -   <span data-ttu-id="10310-128">Seek</span><span class="sxs-lookup"><span data-stu-id="10310-128">Seek</span></span>

    -   <span data-ttu-id="10310-129">CareerBuilder</span><span class="sxs-lookup"><span data-stu-id="10310-129">CareerBuilder</span></span>

    -   <span data-ttu-id="10310-130">Google Jobs</span><span class="sxs-lookup"><span data-stu-id="10310-130">Google Jobs</span></span>

    -   <span data-ttu-id="10310-131">Xing</span><span class="sxs-lookup"><span data-stu-id="10310-131">Xing</span></span>

    -   <span data-ttu-id="10310-132">Glassdoor</span><span class="sxs-lookup"><span data-stu-id="10310-132">Glassdoor</span></span>

    -   <span data-ttu-id="10310-133">Monster Jobs</span><span class="sxs-lookup"><span data-stu-id="10310-133">Monster Jobs</span></span>

-   <span data-ttu-id="10310-134">Ajakirjad ja trükised</span><span class="sxs-lookup"><span data-stu-id="10310-134">Magazines & Publications</span></span>

-   <span data-ttu-id="10310-135">Suhtlusvõrk</span><span class="sxs-lookup"><span data-stu-id="10310-135">Social Network</span></span>

    -   <span data-ttu-id="10310-136">Facebook</span><span class="sxs-lookup"><span data-stu-id="10310-136">Facebook</span></span>

    -   <span data-ttu-id="10310-137">Twitter</span><span class="sxs-lookup"><span data-stu-id="10310-137">Twitter</span></span>

-   <span data-ttu-id="10310-138">Ülikoolis värbamine</span><span class="sxs-lookup"><span data-stu-id="10310-138">University Recruiting</span></span>

-   <span data-ttu-id="10310-139">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="10310-139">LinkedIn</span></span>

-   <span data-ttu-id="10310-140">Töökuulutus ajalehes</span><span class="sxs-lookup"><span data-stu-id="10310-140">Classifieds</span></span>

-   <span data-ttu-id="10310-141">Viitamine</span><span class="sxs-lookup"><span data-stu-id="10310-141">Referral</span></span>

-   <span data-ttu-id="10310-142">Värbaja lisatud</span><span class="sxs-lookup"><span data-stu-id="10310-142">Added by Recruiter</span></span>

-   <span data-ttu-id="10310-143">Muud</span><span class="sxs-lookup"><span data-stu-id="10310-143">Other</span></span>

## <a name="customize-the-source-list"></a><span data-ttu-id="10310-144">Allikate loendi kohandamine</span><span class="sxs-lookup"><span data-stu-id="10310-144">Customize the source list</span></span> 

<span data-ttu-id="10310-145">Saate allikate loendit täiendada, et kaasata täiendavaid avalduste allikaid.</span><span class="sxs-lookup"><span data-stu-id="10310-145">You can extend the source list to include additional application sources.</span></span> <span data-ttu-id="10310-146">Loendi kohandamiseks järgige juhiseid teemas [Suvandikomplektide laiendamine Attractis](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract).</span><span class="sxs-lookup"><span data-stu-id="10310-146">To customize this list, follow the instructions in [Extending Option Sets in Attract](https://docs.microsoft.com/en-us/dynamics365/unified-operations/talent/extensibility-attract#extending-option-sets-in-attract).</span></span> <span data-ttu-id="10310-147">Redigeerige olemit **TalentSource**, et lisada täiendavaid allikaid.</span><span class="sxs-lookup"><span data-stu-id="10310-147">Edit the **TalentSource** entity to include additional sources.</span></span> 

<span data-ttu-id="10310-148">Kasutajaliidese kahjustamise vältimiseks ärge redigeerige ega muutke olemi **TalentCategory** loetelu (enum) väärtusi (mitte nimesid) järgmiste üksuste puhul.</span><span class="sxs-lookup"><span data-stu-id="10310-148">To avoid negatively impacting the user interface (UI), don't edit or delete the **TalentCategory** enum values (not names) for the following:</span></span>

- <span data-ttu-id="10310-149">**Viitamine**</span><span class="sxs-lookup"><span data-stu-id="10310-149">**Referral**</span></span>
- <span data-ttu-id="10310-150">**LinkedIn**</span><span class="sxs-lookup"><span data-stu-id="10310-150">**LinkedIn**</span></span>
- <span data-ttu-id="10310-151">**Muud**</span><span class="sxs-lookup"><span data-stu-id="10310-151">**Other**</span></span>

<span data-ttu-id="10310-152">Selle asemel saate laiendada olemi **TalentSource** loetelu (enum), et lisada muid allika tüüpe.</span><span class="sxs-lookup"><span data-stu-id="10310-152">Instead, you can extend the **TalentSource** enum to add other types of sources.</span></span>
