---
title: "Küsimustiku laialisaatmine ja täitmine"
description: "See teema selgitab, kuidas saata laiali enda kavandatud küsimustikke, nii et need oleksid kättesaadavad inimesele või inimeste grupile, kes neid täidavad."
author: kherr75
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: kherr75
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 9a9883c44202c3fdb963c4dc3ebbb39155a911da
ms.contentlocale: et-ee
ms.lasthandoff: 09/29/2017

---

# <a name="distribute-and-complete-a-questionnaire"></a><span data-ttu-id="29270-103">Küsimustiku laialisaatmine ja täitmine</span><span class="sxs-lookup"><span data-stu-id="29270-103">Distribute and complete a questionnaire</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="29270-104">See teema selgitab, kuidas saata laiali enda kavandatud küsimustikke, nii et need oleksid kättesaadavad inimesele või inimeste grupile, kes neid täidavad.</span><span class="sxs-lookup"><span data-stu-id="29270-104">This topic explains how distribute the questionnaires that you design, so that they are available to the person or group of people who will complete them.</span></span> 

<span data-ttu-id="29270-105">Küsimustiku laialisaatmiseks on mitu võimalust.</span><span class="sxs-lookup"><span data-stu-id="29270-105">There are multiple ways to distribute a questionnaire:</span></span>

-   <span data-ttu-id="29270-106">Saate märkida küsimustiku aktiivseks.</span><span class="sxs-lookup"><span data-stu-id="29270-106">Mark the questionnaire as active.</span></span> <span data-ttu-id="29270-107">Küsimustik on siis saadaval kõigile töötajatele, kui küsimusegrupile pole määratud piiratud juurdepääsu.</span><span class="sxs-lookup"><span data-stu-id="29270-107">The questionnaire is then available to all employees, unless a questionnaire group is set up to restrict access to it.</span></span>
-   <span data-ttu-id="29270-108">Saate määrata õigused küsimustike grupile.</span><span class="sxs-lookup"><span data-stu-id="29270-108">Assign rights to a questionnaire group.</span></span> <span data-ttu-id="29270-109">Küsimustik on siis saadaval valitud grupi liikmetele.</span><span class="sxs-lookup"><span data-stu-id="29270-109">The questionnaire is then available to all members of the selected group.</span></span>
-   <span data-ttu-id="29270-110">Saate luua plaanitud vastamissessioone.</span><span class="sxs-lookup"><span data-stu-id="29270-110">Create planned answer sessions.</span></span> <span data-ttu-id="29270-111">Küsimustik on siis saadaval ainult kindlale isikule.</span><span class="sxs-lookup"><span data-stu-id="29270-111">The questionnaire is then available only to a particular person.</span></span>
-   <span data-ttu-id="29270-112">Saate luua graafiku.</span><span class="sxs-lookup"><span data-stu-id="29270-112">Create a schedule.</span></span> <span data-ttu-id="29270-113">Küsimustik võib siis olla saadaval mitmele inimesele.</span><span class="sxs-lookup"><span data-stu-id="29270-113">The questionnaire can then be available to multiple people.</span></span>

## <a name="marking-a-questionnaire-as-active"></a><span data-ttu-id="29270-114">Küsimustiku aktiivseks märkimine</span><span class="sxs-lookup"><span data-stu-id="29270-114">Marking a questionnaire as active</span></span>
<span data-ttu-id="29270-115">Määrates lehel **Küsimustikud** välja **Aktiivne** sätteks **Jah**, teete küsimustiku kõigile töövõtjatele täitmiseks kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="29270-115">By setting the **Active** field to **Yes** on the **Questionnaires** page, you make the questionnaire available for all employees to complete.</span></span> <span data-ttu-id="29270-116">Vastajad võivad täita küsimustikku mitu korda.</span><span class="sxs-lookup"><span data-stu-id="29270-116">Respondents can complete the questionnaire multiple times.</span></span> <span data-ttu-id="29270-117">See funktsioon on abiks, kui soovite koguda terve aasta jooksul pidevat tagasisidet.</span><span class="sxs-lookup"><span data-stu-id="29270-117">This functionality is useful if you want to gather continual feedback throughout the year.</span></span> <span data-ttu-id="29270-118">Näiteks võite koostada küsimustiku, mille kaudu töötajad saavad anda kohviku lõunateenuse kohta tagasisidet.</span><span class="sxs-lookup"><span data-stu-id="29270-118">For example, you can make a questionnaire that employees use to give feedback about the lunch service in the cafeteria.</span></span>

## <a name="questionnaire-groups"></a><span data-ttu-id="29270-119">Küsimustikugrupid</span><span class="sxs-lookup"><span data-stu-id="29270-119">Questionnaire groups</span></span>
<span data-ttu-id="29270-120">Saate seadistada küsimustikugrupid ja lisada sinna siis vastavad, kellele küsimustik tuleks saata.</span><span class="sxs-lookup"><span data-stu-id="29270-120">You can set up questionnaire groups and then include the respondents that a questionnaire should be distributed to.</span></span> 

<span data-ttu-id="29270-121">Saate luua küsimustikugruppe järgmistelt lehtedelt.</span><span class="sxs-lookup"><span data-stu-id="29270-121">You can create questionnaire groups from the following pages:</span></span>

-   <span data-ttu-id="29270-122">**Küsimustikugrupid**– valitud küsimustikku saavad täita ainult küsimustikugrupis olevad inimesed.</span><span class="sxs-lookup"><span data-stu-id="29270-122">**Questionnaire groups** – Only individuals in a questionnaire group can complete a selected questionnaire.</span></span> <span data-ttu-id="29270-123">Näiteks on teie sihtrühm töövõtjad, seega koostate neile vastajatele mõeldud küsimustikugrupi.</span><span class="sxs-lookup"><span data-stu-id="29270-123">For example, your intended audience is contractors, so you create a questionnaire group that is specific to those respondents.</span></span>
-   <span data-ttu-id="29270-124">**Küsimustikugrupi liikmed** – saate lisada küsimustikugruppidesse inimesi.</span><span class="sxs-lookup"><span data-stu-id="29270-124">**Questionnaire group members** – You can add people to the questionnaire groups.</span></span>

<span data-ttu-id="29270-125">Küsimustikule küsimustikugrupi määramiseks klõpsake lehel **Küsimustikud** valikut **Kasutajaõigused**.</span><span class="sxs-lookup"><span data-stu-id="29270-125">To assign a questionnaire group to a questionnaire, on the **Questionnaires** page, click **User rights**.</span></span> <span data-ttu-id="29270-126">Pärast küsimustiku aktiivsena salvestamist saavad küsimustikugrupi liikmed küsimustiku täita.</span><span class="sxs-lookup"><span data-stu-id="29270-126">After the questionnaire is saved as active, the members of the questionnaire group can complete the questionnaire.</span></span> <span data-ttu-id="29270-127">See funktsioon on abiks, kui soovite testida küsimustikku valitud inimeste grupil, enne kui edastate selle suuremale grupile, või kui soovite suunata küsimustiku väga konkreetsele sihtrühmale.</span><span class="sxs-lookup"><span data-stu-id="29270-127">This functionality is helpful if you want to test a questionnaire on a select group of people before you roll it out to a larger group, or if you want to target a questionnaire to a very specific audience.</span></span>

## <a name="planned-answer-sessions-in-a-questionnaire"></a><span data-ttu-id="29270-128">Plaanitud vastamisseansid küsimustiku kohta</span><span class="sxs-lookup"><span data-stu-id="29270-128">Planned answer sessions in a questionnaire</span></span>
<span data-ttu-id="29270-129">Plaanitud vastamisseansid on küsimustikud, mille olete kavandanud ja millele vastajad valinud.</span><span class="sxs-lookup"><span data-stu-id="29270-129">Planned answer sessions are questionnaires that you've designed and selected the respondents for.</span></span> 

> <span data-ttu-id="29270-130">**Märkus.** Enne plaanitud vastamisseansside seadistamist tuleb kavandada küsimustik.</span><span class="sxs-lookup"><span data-stu-id="29270-130">**Note** Before you can set up planned answer sessions, you must design a questionnaire.</span></span> 

<span data-ttu-id="29270-131">Lehel **Plaanitud vastamisseanss** saate luua üksiku töötaja jaoks plaanitud vastamisseansi.</span><span class="sxs-lookup"><span data-stu-id="29270-131">On the **Planned answer session** page, you can create a planned answer session for an individual employee.</span></span> <span data-ttu-id="29270-132">Lehe loendis kuvatakse kõik kavandatud küsimustikud.</span><span class="sxs-lookup"><span data-stu-id="29270-132">The list on the page displays all planned questionnaires.</span></span> 

<span data-ttu-id="29270-133">Plaanitud vastuseseansse kasutatakse ka lehel **Küsimustikugraafikud**, kus saate küsimustikke plaanida mitme inimese jaoks.</span><span class="sxs-lookup"><span data-stu-id="29270-133">Planned answer sessions are also used on the **Questionnaire schedules** page, where you can plan questionnaires for multiple people:</span></span>

-   <span data-ttu-id="29270-134">Töötajad</span><span class="sxs-lookup"><span data-stu-id="29270-134">Employees</span></span>
-   <span data-ttu-id="29270-135">Kursusel osalejad</span><span class="sxs-lookup"><span data-stu-id="29270-135">Course participants</span></span>
-   <span data-ttu-id="29270-136">organisatsiooniühikud</span><span class="sxs-lookup"><span data-stu-id="29270-136">Organizational units</span></span>

<span data-ttu-id="29270-137">Iga inimene saab vastata küsimustikule ainult üks kord.</span><span class="sxs-lookup"><span data-stu-id="29270-137">Each person can answer the questionnaire only one time.</span></span>

## <a name="scheduling-a-questionnaire"></a><span data-ttu-id="29270-138">Küsimustiku plaanimine</span><span class="sxs-lookup"><span data-stu-id="29270-138">Scheduling a questionnaire</span></span>
<span data-ttu-id="29270-139">Soovi korral saate plaanida küsimustiku mitme vastaja jaoks.</span><span class="sxs-lookup"><span data-stu-id="29270-139">You can optionally schedule a questionnaire for multiple respondents.</span></span>

### <a name="planning-types"></a><span data-ttu-id="29270-140">Planeerimise tüübid</span><span class="sxs-lookup"><span data-stu-id="29270-140">Planning types</span></span>

<span data-ttu-id="29270-141">Plaanimise tüübid on vajalikud, kui soovite plaanida vastusesessioonid mitmele vastajale.</span><span class="sxs-lookup"><span data-stu-id="29270-141">Planning types are required if you want to schedule planned answer sessions for multiple respondents.</span></span> <span data-ttu-id="29270-142">Plaanimise tüüpe kasutatakse küsimustiku graafikute klassifitseerimiseks.</span><span class="sxs-lookup"><span data-stu-id="29270-142">Planning types are used to classify questionnaire schedules.</span></span> <span data-ttu-id="29270-143">Näiteks võite plaanida küsimustikke järgmistel eesmärkidel.</span><span class="sxs-lookup"><span data-stu-id="29270-143">For example, you can schedule questionnaires for the following purposes:</span></span>

-   <span data-ttu-id="29270-144">Hindamine</span><span class="sxs-lookup"><span data-stu-id="29270-144">Evaluation</span></span>
-   <span data-ttu-id="29270-145">Uuring</span><span class="sxs-lookup"><span data-stu-id="29270-145">Survey</span></span>
-   <span data-ttu-id="29270-146">Testimine</span><span class="sxs-lookup"><span data-stu-id="29270-146">Testing</span></span>

<span data-ttu-id="29270-147">Küsimustiku graafiku plaanimise tüüpe saab määrata lehel **Küsimustikugraafikud**.</span><span class="sxs-lookup"><span data-stu-id="29270-147">You can specify planning types for a questionnaire schedule on the **Questionnaire schedules** page.</span></span>

### <a name="reference-types-for-questionnaire"></a><span data-ttu-id="29270-148">Küsimustiku viitetüübid</span><span class="sxs-lookup"><span data-stu-id="29270-148">Reference types for questionnaire</span></span>

<span data-ttu-id="29270-149">Võite kasutada viitetüüpe vastajate kriteeriumide sisestamiseks, mida saab küsimustiku plaanimisel valida.</span><span class="sxs-lookup"><span data-stu-id="29270-149">You can use reference types to enter criteria for the respondents that you might select when you schedule a questionnaire.</span></span> 

<span data-ttu-id="29270-150">Kasutage lehte **Viitetüübid** küsimustiku viitetüüpide seadistamiseks.</span><span class="sxs-lookup"><span data-stu-id="29270-150">Use the **Reference types** page to set up reference types for a questionnaire.</span></span> <span data-ttu-id="29270-151">Iga viitetüüp vastab Microsoft Dynamics 365 for Finance and Operationsi tabelile.</span><span class="sxs-lookup"><span data-stu-id="29270-151">Each reference type corresponds to a table in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="29270-152">Küsimustikugraafikute loomisel saate määrata eraldi tabelikirjeid või kirjete vahemikku, millega küsimustik seostatakse.</span><span class="sxs-lookup"><span data-stu-id="29270-152">When you create questionnaire schedules, you can specify individual records in the table or a range of records that the questionnaire will be associated with.</span></span> 

<span data-ttu-id="29270-153">Näiteks kui valite tabeli Kursused, saate määrata, millise konkreetse kursuse jaoks küsimustik on mõeldud.</span><span class="sxs-lookup"><span data-stu-id="29270-153">For example, if you select the Courses table, you can decide which specific course the questionnaire will be for.</span></span> <span data-ttu-id="29270-154">Kui seadistate viite kursuse tabelile, muutuvad mõned väljad ja nupud väljal **Kursused** kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="29270-154">When you set up a reference for the Courses table, some fields and buttons on the **Courses** page become available.</span></span>

### <a name="questionnaire-schedules"></a><span data-ttu-id="29270-155">Küsimustiku graafikud</span><span class="sxs-lookup"><span data-stu-id="29270-155">Questionnaire schedules</span></span>

<span data-ttu-id="29270-156">Võite kasutada küsimustikugraafikuid mitme plaanitud vastusesessiooni loomiseks kasutajagrupile viitetüübi põhjal.</span><span class="sxs-lookup"><span data-stu-id="29270-156">You can use questionnaire schedules to generate multiple planned answer sessions for a group of users, based on a reference type.</span></span> <span data-ttu-id="29270-157">Looge graafik lehel **Küsimustikugraafikud**.</span><span class="sxs-lookup"><span data-stu-id="29270-157">Create a schedule on the **Questionnaire schedules** page.</span></span> <span data-ttu-id="29270-158">Valige graafiku kategoriseerimiseks plaanimise tüüp ja valige ka viitetüüp, mida tuleb konkreetsete kasutajate puhul süsteemi päringute edastamisel kasutada.</span><span class="sxs-lookup"><span data-stu-id="29270-158">Select the planning type to categorize the schedule, and also select the reference type that should be used to query the system for specific users.</span></span> <span data-ttu-id="29270-159">Näiteks kui määrate viitetüübiks kursuse tabeli, saate valida konkreetse kursuse väljal **Viide**.</span><span class="sxs-lookup"><span data-stu-id="29270-159">For example, if you set the reference type to the Courses table, you can select a specific course in the **Reference** field.</span></span> 

<span data-ttu-id="29270-160">Klõpsake valikut **Seadistuse üksikasjad** küsimustiku ja muude kriteeriumide valimiseks.</span><span class="sxs-lookup"><span data-stu-id="29270-160">Click **Setup details** to select the questionnaire and other criteria.</span></span> <span data-ttu-id="29270-161">Näiteks saate määrata kriteeriumiks juhendaja nime, kui küsimustik on juhendaja hindamiseks.</span><span class="sxs-lookup"><span data-stu-id="29270-161">For example, specify the instructor's name as a criterion if the questionnaire is an evaluation of the instructor.</span></span> <span data-ttu-id="29270-162">Pärast seadistuse üksikasjade sisestamist loob süsteem päringusse lisatud vastajatele plaanitud vastusesessioonid.</span><span class="sxs-lookup"><span data-stu-id="29270-162">After you've finished entering the setup details, the system generates planned answer sessions for the users that are included in the query.</span></span> 

<span data-ttu-id="29270-163">Klõpsake valikut **Plaanitud vastusesessioonid** graafiku vastusesessioonide vaatamiseks.</span><span class="sxs-lookup"><span data-stu-id="29270-163">Click **Planned answer sessions** to view the answer sessions for the schedule.</span></span> <span data-ttu-id="29270-164">Seejärel saate luua käsitsi täiendavaid plaanitud vastamisseansse või vastusteta plaanitud vastuseseansse kustutada.</span><span class="sxs-lookup"><span data-stu-id="29270-164">You can then manually create additional planned answer sessions or delete planned answer sessions that haven't been answered.</span></span> 

<span data-ttu-id="29270-165">Klõpsake valikuid **Funktsioonid** &gt; **Käivita**, et teha küsimustik seotud plaanitud vastuseseanssides kasutajatele kättesaadavaks.</span><span class="sxs-lookup"><span data-stu-id="29270-165">Click **Functions** &gt; **Start** to make the questionnaire available to the users in related planned answer sessions.</span></span> <span data-ttu-id="29270-166">Klõpsake valikut **Vastused** küsimustiku täidetud vastuste vaatamiseks.</span><span class="sxs-lookup"><span data-stu-id="29270-166">Click **Answers** to view the completed responses to the questionnaire.</span></span> <span data-ttu-id="29270-167">Soovi korral saate kopeerida küsimustiku graafiku sätteid, plaanitud vastamisseansse ja vastuseid uue küsimustiku graafikusse.</span><span class="sxs-lookup"><span data-stu-id="29270-167">You can optionally copy the questionnaire schedule settings, planned answer sessions, and answers to a new questionnaire schedule.</span></span>

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a><span data-ttu-id="29270-168">Vastajate teavitamine neile saadaolevatest küsimustikest</span><span class="sxs-lookup"><span data-stu-id="29270-168">Notifying respondents about questionnaires that are available to them</span></span>
<span data-ttu-id="29270-169">Kui küsimustiku laiali saadate, peate vastajatele teatama, et küsimustikud on neile kättesaadavad.</span><span class="sxs-lookup"><span data-stu-id="29270-169">When you distribute a questionnaire, you must notify respondents that questionnaires are available to them.</span></span> 

### <a name="notifying-respondents-about-a-planned-answer-session"></a><span data-ttu-id="29270-170">Vastajate teavitamine plaanitud vastamissessioonist</span><span class="sxs-lookup"><span data-stu-id="29270-170">Notifying respondents about a planned answer session</span></span>

<span data-ttu-id="29270-171">Kui kasutate plaanitud vastamisseanssi, peate teavitama inimest otse (nt telefoni või meili teel).</span><span class="sxs-lookup"><span data-stu-id="29270-171">If you use a planned answer session, you must notify the person directly, such as by telephone or email.</span></span>

### <a name="notifying-respondents-about-a-scheduling"></a><span data-ttu-id="29270-172">Vastajate teavitamine plaanimisest</span><span class="sxs-lookup"><span data-stu-id="29270-172">Notifying respondents about a scheduling</span></span>

<span data-ttu-id="29270-173">Lehel **Küsimustikugraafikud** saate ette valmistada ja saata meilid kõigile vastajatele, kellele küsimustik on määratud.</span><span class="sxs-lookup"><span data-stu-id="29270-173">Use the **Questionnaire schedules** page to prepare and send email to all respondents who are assigned to the questionnaire.</span></span> <span data-ttu-id="29270-174">Sisestage meili tekst vahekaardile **Meil töötaja iseteeninduse jaoks**. Pärast graafiku käivitamist klõpsake valikuid **Funktsioonid** &gt; **Saada meilisõnum** meilisõnumi koostamiseks ja vastajatele saatmiseks.</span><span class="sxs-lookup"><span data-stu-id="29270-174">Enter the email text on the **E-mail for employee self service** tab. After the schedule has been started, click **Functions** &gt; **Send e-mail** to generate and send the email to the respondents.</span></span> <span data-ttu-id="29270-175">Vastajad saavad siis veebisaidile sisse logida ja küsimustiku täita.</span><span class="sxs-lookup"><span data-stu-id="29270-175">Respondents can then sign in to the website and complete the questionnaire.</span></span> 

> <span data-ttu-id="29270-176">**Märkus.** Enne, kui saate meilifunktsiooni kasutada, peab teie IT-administraator sisestama meilisätted lehele **Meiliparameetrid**.</span><span class="sxs-lookup"><span data-stu-id="29270-176">**Note** Before you can use the email functionality, your IT administrator must enter the email settings on the **E-mail parameters** page.</span></span>

## <a name="ending-a-scheduled-questionnaire"></a><span data-ttu-id="29270-177">Plaanitud küsimustiku lõpetamine</span><span class="sxs-lookup"><span data-stu-id="29270-177">Ending a scheduled questionnaire</span></span>
<span data-ttu-id="29270-178">Plaanitud küsimustiku saate lõpetada pärast seda, kui kõik vastajad on neile määratud vastuseseansid sooritanud.</span><span class="sxs-lookup"><span data-stu-id="29270-178">You can end a scheduled questionnaire after all respondents have completed their assigned answer sessions.</span></span> <span data-ttu-id="29270-179">Pärast plaanitud küsimustiku lõpetamist ei saa selle sätteid uude graafikusse kopeerida.</span><span class="sxs-lookup"><span data-stu-id="29270-179">After a scheduled questionnaire is ended, you can't copy its settings to a new schedule.</span></span> 

> <span data-ttu-id="29270-180">**Märkus.** Kui vähemalt üks vastaja pole küsimustikku täitnud, kuid soovite siiski plaanimise lõpetada, peate esmalt kustutama need vastajad loendist lehel **Plaanitud vastamissessioon**.</span><span class="sxs-lookup"><span data-stu-id="29270-180">**Note** If one or more respondents haven't completed the questionnaire, but you still want to end the scheduling, you must first delete those respondents from the list on the **Planned answer session** page.</span></span> <span data-ttu-id="29270-181">Seejärel saate graafiku lõpetada.</span><span class="sxs-lookup"><span data-stu-id="29270-181">You can then end the schedule.</span></span>

## <a name="completing-questionnaires"></a><span data-ttu-id="29270-182">Küsimustike täitmine</span><span class="sxs-lookup"><span data-stu-id="29270-182">Completing questionnaires</span></span>
<span data-ttu-id="29270-183">Pärast küsimustiku kavandamist ja laiali saatmist saavad valitud vastajad selle täita.</span><span class="sxs-lookup"><span data-stu-id="29270-183">After you've designed and distributed a questionnaire, the questionnaire can be completed by selected respondents.</span></span> <span data-ttu-id="29270-184">Saate täita küsimustikud, mis on saadaval kahes kohas:</span><span class="sxs-lookup"><span data-stu-id="29270-184">You can complete the questionnaires that are available to you from two locations:</span></span>

-   <span data-ttu-id="29270-185">Klõpsake navigeerimispaanil valikuid **Küsimustikud** &gt; **Laialisaatmine** &gt; **Küsimustiku täitmine**.</span><span class="sxs-lookup"><span data-stu-id="29270-185">In the navigation pane, click **Questionnaires** &gt; **Distribute** &gt; **Complete a questionnaire**.</span></span>
-   <span data-ttu-id="29270-186">Klõpsake töötaja iseteeninduses valikut **Täidetavad küsimustikud**.</span><span class="sxs-lookup"><span data-stu-id="29270-186">In Employee self-service, click **Questionnaires to complete**.</span></span>

<span data-ttu-id="29270-187">Küsimustikud saab teha kättesaadavaks kindlatele kasutajatele või kasutajagruppidele või kõigile kasutajatele võrgus.</span><span class="sxs-lookup"><span data-stu-id="29270-187">Questionnaires can made be available to specific users or groups of users, or to all users in a network.</span></span>

<a name="see-also"></a><span data-ttu-id="29270-188">Vt ka</span><span class="sxs-lookup"><span data-stu-id="29270-188">See also</span></span>
--------

[<span data-ttu-id="29270-189">Küsimustike kavandamine</span><span class="sxs-lookup"><span data-stu-id="29270-189">Designing questionnaires</span></span>](design-questionnaires.md)

[<span data-ttu-id="29270-190">Küsimustike kasutamine</span><span class="sxs-lookup"><span data-stu-id="29270-190">Using questionnaires</span></span>](questionnaires.md)

[<span data-ttu-id="29270-191">Küsimustike tulemuste vaatamine ja hindamine</span><span class="sxs-lookup"><span data-stu-id="29270-191">Viewing and evaluating the results of questionnaires</span></span>](evaluate-questionnaire-results.md)



