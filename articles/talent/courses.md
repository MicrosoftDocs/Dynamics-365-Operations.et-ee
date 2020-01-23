---
title: Koolituskursuste seadistamine
description: Inimressursside administraatorid ja haldurid saavad kasutada kursuste funktsioone töötajatele pakutavate koolituste kohta teabe haldamiseks.
author: andreabichsel
manager: AnnBe
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.openlocfilehash: c68601b150e5c0963bfba0fa1c6c866abdd092cb
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: et-EE
ms.lasthandoff: 12/06/2019
ms.locfileid: "2898869"
---
# <a name="set-up-training-courses"></a><span data-ttu-id="a9c22-103">Koolituskursuste seadistamine</span><span class="sxs-lookup"><span data-stu-id="a9c22-103">Set up training courses</span></span>

<span data-ttu-id="a9c22-104">Inimressursside administraatorid ja haldurid saavad kasutada kursuste funktsioone töötajatele pakutavate koolituste kohta teabe haldamiseks.</span><span class="sxs-lookup"><span data-stu-id="a9c22-104">Human resources administrators and managers can use the courses features to maintain information about the training that's offered to workers.</span></span>

 <a name="set-up-prerequisites"></a><span data-ttu-id="a9c22-105"> Seadistuse eeltingimused</span><span class="sxs-lookup"><span data-stu-id="a9c22-105">Set up prerequisites</span></span>
---------------------

<span data-ttu-id="a9c22-106">Järgmine teave on vajalik ja tuleb seadistada enne kursuste loomist.</span><span class="sxs-lookup"><span data-stu-id="a9c22-106">The following information is required and must be set up before you create courses.</span></span>
-   <span data-ttu-id="a9c22-107">**Kursuste tüübid**</span><span class="sxs-lookup"><span data-stu-id="a9c22-107">**Course types**</span></span>

<span data-ttu-id="a9c22-108">Järgmine teave on valikuline teave, mille saate kursustele määrata.</span><span class="sxs-lookup"><span data-stu-id="a9c22-108">The following information is optional information that you can specify for courses.</span></span> <span data-ttu-id="a9c22-109">Kui teate, et kavatsete seda teavet kursuste kohta sisestada, tuleb see seadistada enne kursuse kirjete loomist.</span><span class="sxs-lookup"><span data-stu-id="a9c22-109">If you know that you will be entering this information for courses, you should set up this information before you create course records.</span></span>
-   <span data-ttu-id="a9c22-110">**Klassiruumide grupid**</span><span class="sxs-lookup"><span data-stu-id="a9c22-110">**Classroom groups**</span></span>
-   <span data-ttu-id="a9c22-111">**Kursuste grupid**</span><span class="sxs-lookup"><span data-stu-id="a9c22-111">**Course groups**</span></span>
-   <span data-ttu-id="a9c22-112">**Kursuste toimumiskohad**</span><span class="sxs-lookup"><span data-stu-id="a9c22-112">**Course locations**</span></span>
-   <span data-ttu-id="a9c22-113">**Klassiruumid**</span><span class="sxs-lookup"><span data-stu-id="a9c22-113">**Classrooms**</span></span>
-   <span data-ttu-id="a9c22-114">**Juhendajad**</span><span class="sxs-lookup"><span data-stu-id="a9c22-114">**Instructors**</span></span>

## <a name="course-types"></a><span data-ttu-id="a9c22-115">Kursuste tüübid</span><span class="sxs-lookup"><span data-stu-id="a9c22-115">Course types</span></span>
<span data-ttu-id="a9c22-116">Saate kursusi nende struktuuri või sisu alusel tüüpide järgi kategooriatesse paigutada.</span><span class="sxs-lookup"><span data-stu-id="a9c22-116">You can use course types to categorize courses according to the structure or content of the course.</span></span> <span data-ttu-id="a9c22-117">Saate luua kursuste tüüpe lehel **Kursuste tüübid**.</span><span class="sxs-lookup"><span data-stu-id="a9c22-117">You can create course types on the **Course types** page.</span></span> <span data-ttu-id="a9c22-118">Kursuse kirje loomisel tuleb valida kursuse tüüp.</span><span class="sxs-lookup"><span data-stu-id="a9c22-118">You must select a course type when you create a course record.</span></span>

## <a name="course-setup-type"></a><span data-ttu-id="a9c22-119">Kursuse seadistuse tüüp</span><span class="sxs-lookup"><span data-stu-id="a9c22-119">Course setup type</span></span>
<span data-ttu-id="a9c22-120">Järgmises tabelis on antud kolm kursuste seadistuse tüüpi.</span><span class="sxs-lookup"><span data-stu-id="a9c22-120">The following table lists the three setup types for courses.</span></span> <span data-ttu-id="a9c22-121">Seadistuse tüübid määravad kursuse struktuuri.</span><span class="sxs-lookup"><span data-stu-id="a9c22-121">Setup types determine the structure of the course.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a9c22-122">Seadistuse tüüp</span><span class="sxs-lookup"><span data-stu-id="a9c22-122">Setup type</span></span></th>
<th><span data-ttu-id="a9c22-123">Kirjeldus</span><span class="sxs-lookup"><span data-stu-id="a9c22-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a9c22-124"><strong>Standardne</strong></span><span class="sxs-lookup"><span data-stu-id="a9c22-124"><strong>Standard</strong></span></span></td>
<td><span data-ttu-id="a9c22-125">Valige see tüüp ilma päevakavata kursuste puhul.</span><span class="sxs-lookup"><span data-stu-id="a9c22-125">Select this type for courses that will not have a daily agenda.</span></span> <span data-ttu-id="a9c22-126">See on uue kursuse loomisel seadistuse vaiketüüp.</span><span class="sxs-lookup"><span data-stu-id="a9c22-126">This is the default setup type when you create a new course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a9c22-127"><strong>Päevakord</strong></span><span class="sxs-lookup"><span data-stu-id="a9c22-127"><strong>Agenda</strong></span></span></td>
<td><span data-ttu-id="a9c22-128">Valige see tüüp mitme päeva jooksul toimuva kursuse iga päeva üksikasjade plaanimiseks.</span><span class="sxs-lookup"><span data-stu-id="a9c22-128">Select this type to plan the details of each day of a course that takes place over multiple days.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a9c22-129"><strong>Päevakord + seanss</strong></span><span class="sxs-lookup"><span data-stu-id="a9c22-129"><strong>Agenda + session</strong></span></span></td>
<td><span data-ttu-id="a9c22-130">Valige see tüüp keerukamate kursuste puhul.</span><span class="sxs-lookup"><span data-stu-id="a9c22-130">Select this type for the more complex courses.</span></span> <span data-ttu-id="a9c22-131">Näiteks saate jaotada kursuse päevakava teedeks ja sessioonideks.</span><span class="sxs-lookup"><span data-stu-id="a9c22-131">For example, you can divide the agenda for the course into tracks and sessions.</span></span>
<ul>
<li><span data-ttu-id="a9c22-132"><strong>Tee</strong> – teed on kursuse konkreetsed teemavaldkonnad.</span><span class="sxs-lookup"><span data-stu-id="a9c22-132"><strong>Track</strong> – Tracks are specific subject areas for a course.</span></span></li>
<li><span data-ttu-id="a9c22-133"><strong>Sessioonid</strong> – sessioonid jagavad teid ja aitavad tuvastada tee konkreetseid protsesse või võtteid.</span><span class="sxs-lookup"><span data-stu-id="a9c22-133"><strong>Sessions</strong> – Sessions divide up tracks and help identify specific processes or techniques that are relevant to the track.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a><span data-ttu-id="a9c22-134">Kursuse ülesanded</span><span class="sxs-lookup"><span data-stu-id="a9c22-134">Course tasks</span></span>
<span data-ttu-id="a9c22-135">Iga kursuse puhul saate täita järgmisi ülesandeid.</span><span class="sxs-lookup"><span data-stu-id="a9c22-135">For each course, you can complete the following tasks.</span></span>
- <span data-ttu-id="a9c22-136">Osalejate registreerimine</span><span class="sxs-lookup"><span data-stu-id="a9c22-136">Register participants</span></span>
- <span data-ttu-id="a9c22-137">Registreerimise lõpptähtaja määramine</span><span class="sxs-lookup"><span data-stu-id="a9c22-137">Specify a registration deadline</span></span>
- <span data-ttu-id="a9c22-138">Osalejate vähima ja suurima arvu määratlemine</span><span class="sxs-lookup"><span data-stu-id="a9c22-138">Define the minimum and maximum number of participants</span></span>
- <span data-ttu-id="a9c22-139">Kursuse asukoha ja klassiruumi määramine</span><span class="sxs-lookup"><span data-stu-id="a9c22-139">Assign a course location and classroom</span></span>
- <span data-ttu-id="a9c22-140">Kursusel osalejatele hotellide soovitamine</span><span class="sxs-lookup"><span data-stu-id="a9c22-140">Recommend hotels to course participants</span></span>
- <span data-ttu-id="a9c22-141">Kursuse kirjelduse loomine töötaja iseteeninduses reklaamimiseks.</span><span class="sxs-lookup"><span data-stu-id="a9c22-141">Create a course description, which you can then advertise on Employee self service</span></span>

  ><span data-ttu-id="a9c22-142">**Märkus.** Kursuse saate kustutada ainult siis, kui keegi pole sellele registreerunud.</span><span class="sxs-lookup"><span data-stu-id="a9c22-142">**Note** You can delete a course only if no one has registered for it.</span></span> 

## <a name="course-statuses"></a><span data-ttu-id="a9c22-143">Kursuse olekud</span><span class="sxs-lookup"><span data-stu-id="a9c22-143">Course statuses</span></span>
<span data-ttu-id="a9c22-144">Järgmises tabelis on antud võimalikud kursuse olekud ja toimingud, mida saate teha, kui kursus on teatud olekuga.</span><span class="sxs-lookup"><span data-stu-id="a9c22-144">The following table lists the possible course statuses and the actions that you can complete when the course has a specific status.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a9c22-145">Olek</span><span class="sxs-lookup"><span data-stu-id="a9c22-145">Status</span></span></th>
<th><span data-ttu-id="a9c22-146">Tegevused</span><span class="sxs-lookup"><span data-stu-id="a9c22-146">Actions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a9c22-147"><strong>Loodud</strong></span><span class="sxs-lookup"><span data-stu-id="a9c22-147"><strong>Created</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="a9c22-148">Kursuseteabe sisestamine ja redigeerimine.</span><span class="sxs-lookup"><span data-stu-id="a9c22-148">Enter and modify course information.</span></span></li>
<li><span data-ttu-id="a9c22-149">Kursusele oleku <strong>Avatud</strong> määramine, et töötajad saaksid end kursusele registreerida.</span><span class="sxs-lookup"><span data-stu-id="a9c22-149">Change the course status to <strong>Open</strong> so that workers can register for the course.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a9c22-150"><strong>Ava</strong></span><span class="sxs-lookup"><span data-stu-id="a9c22-150"><strong>Open</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="a9c22-151">Kursusele osalejate registreerimine.</span><span class="sxs-lookup"><span data-stu-id="a9c22-151">Register participants for the course.</span></span></li>
<li><span data-ttu-id="a9c22-152">Kursuselt osalejate eemaldamine.</span><span class="sxs-lookup"><span data-stu-id="a9c22-152">Remove participants from the course.</span></span></li>
<li><span data-ttu-id="a9c22-153">Kursusel osalejate kinnitamine.</span><span class="sxs-lookup"><span data-stu-id="a9c22-153">Confirm participants for the course.</span></span></li>
<li><span data-ttu-id="a9c22-154">Kursuse olekuks saab määrata<strong> Suletud</strong> või <strong>Tühistatud</strong>.</span><span class="sxs-lookup"><span data-stu-id="a9c22-154">Change the course status to <strong>Closed</strong> or <strong>Canceled</strong>.</span></span></li>
<li><span data-ttu-id="a9c22-155">Nende osalejate jaoks, kelle olek on <strong>Kinnitatud</strong>, saab kavandada küsimustikke.</span><span class="sxs-lookup"><span data-stu-id="a9c22-155">Plan questionnaires for participants whose status is <strong>Confirmed</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a9c22-156"><strong>Suletud</strong></span><span class="sxs-lookup"><span data-stu-id="a9c22-156"><strong>Closed</strong></span></span></td>
<td><span data-ttu-id="a9c22-157">Saate kursuse uuesti avada.</span><span class="sxs-lookup"><span data-stu-id="a9c22-157">You can reopen the course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a9c22-158"><strong>Tühistatud</strong></span><span class="sxs-lookup"><span data-stu-id="a9c22-158"><strong>Canceled</strong></span></span></td>
<td><span data-ttu-id="a9c22-159">Saate kursuse uuesti avada.</span><span class="sxs-lookup"><span data-stu-id="a9c22-159">You can reopen the course.</span></span></td>
</tr>
</tbody>
</table>

## <a name="course-participants"></a><span data-ttu-id="a9c22-160">Kursusel osalejad</span><span class="sxs-lookup"><span data-stu-id="a9c22-160">Course participants</span></span>
<span data-ttu-id="a9c22-161">Kursusel osalejad on töötajad, kes koolituskursusel või sündmusel osalevad.</span><span class="sxs-lookup"><span data-stu-id="a9c22-161">Course participants are workers who participate in a training course or event.</span></span> <span data-ttu-id="a9c22-162">Saate registreerida osalejaid ainult avatud kursustele.</span><span class="sxs-lookup"><span data-stu-id="a9c22-162">You can only register participants for open courses.</span></span> <span data-ttu-id="a9c22-163">Minimaalne ja maksimaalne kursusele registreeritav osalejate arv määratakse kiirkaardil **Üldine** lehel **Kursused**.</span><span class="sxs-lookup"><span data-stu-id="a9c22-163">The minimum and maximum number of participants that you can register for a course is defined on the **General** FastTab on the **Courses** page.</span></span>

<a name="workflow"></a><span data-ttu-id="a9c22-164">Töövoog</span><span class="sxs-lookup"><span data-stu-id="a9c22-164">Workflow</span></span>
--------

<span data-ttu-id="a9c22-165">Töötajad, kes registreeruvad kursusele lehe **Töötaja iseteenindus** kaudu, saavad lasta oma registreerumisel läbida kinnitamise töövoo.</span><span class="sxs-lookup"><span data-stu-id="a9c22-165">Employees who register for a course through the **Employee self service** page can have their registration routed through workflow for approval.</span></span> <span data-ttu-id="a9c22-166">Te võite määrata töövookursusele lehe **Kursused** kiirkaardil **Üldine**.</span><span class="sxs-lookup"><span data-stu-id="a9c22-166">You can assign a workflow to a course on the **General** FastTab on the **Courses** page.</span></span>





